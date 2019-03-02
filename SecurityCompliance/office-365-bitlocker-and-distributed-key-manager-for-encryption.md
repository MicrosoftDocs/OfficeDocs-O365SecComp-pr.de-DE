---
title: Office 365 BitLocker für Verschlüsselung
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Zusammenfassung: Informationen zu BitLocker für die Verschlüsselung in der Cloud.'
ms.openlocfilehash: 293c7a3cef3ae2c55a0b12df139baf5302dd3b04
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357426"
---
# <a name="bitlocker-and-distributed-key-manager-dkm-for-encryption"></a>BitLocker und Distributed Key Manager (DKM) für die Verschlüsselung

Office 365-Server verwenden BitLocker für die Verschlüsselung von Laufwerken mit Kundendaten auf Volume-Ebene. BitLocker-Verschlüsselung ist eine Datenverschlüsselungsfunktion, die in Windows integriert ist. BitLocker ist eine der Technologien, die zum Schutz vor Bedrohungen verwendet werden, falls andere Prozesse oder Steuerelemente hinfällig werden (z. B. Zugriffssteuerung oder Access Control oder Recycling von Hardware), sodass andere Personen möglicherweise physischen Zugriff auf Laufwerke mit Kundendaten erlangen könnten. In diesem Fall eliminiert BitLocker das potenzielle Risiko für Datendiebstahl oder Offenlegung aufgrund von verloren gegangener, gestohlener oder nicht ordnungsgemäß außer Betrieb gesetzter Computer und Datenträger.

BitLocker wird mit einer AES-256-Bit-Verschlüsselung auf Datenträgern mit Kundendaten in Exchange Online, SharePoint Online und Skype for Business bereitgestellt. Datenträgersektoren werden mit einem vollständigen Volumen VerschlüsselungsSchlüssel (FVEK) verschlüsselt, der mit dem Volume-Hauptschlüssel (VMK) verschlüsselt ist, der wiederum an das TPM (Trusted Platform Module) auf dem Server gebunden ist. Der VMK schützt die FVEK direkt, und der Schutz der VMK wird daher kritisch. Die folgende Abbildung zeigt ein Beispiel für die BitLocker-Schlüsselschutz Kette für einen bestimmten Server (in diesem Fall die Verwendung eines Exchange Online-Servers).

In der folgenden Tabelle wird die BitLocker-Schlüsselschutz Kette für einen bestimmten Server (in diesem Fall ein Exchange Online-Server) beschrieben.

| SCHLÜSSELSCHUTZ | GRANULARITÄT | WIE GENERIERT? | WO WIRD ES GESPEICHERT? | Schutz |
|--------------------------------------------------------------------------------|-------------------------------------------------|----------------|-------------------------|--------------------------------------------------------------------------------------------------|
| AES 256-Bit-externer Schlüssel | Pro Server | BitLocker-APIs | TPM oder Secret Safe | Lockbox/Zugriffssteuerung |
|  |  |  | Post Fach Server Registrierung | TPM verschlüsselt |
| 48 stelliges numerisches Kennwort | Pro Datenträger | BitLocker-APIs | Active Directory | Lockbox/Zugriffssteuerung |
| X. 509-Zertifikat als Daten wiederHerstellungs-Agent (DRA) auch als Public Key Protector bezeichnet | Umgebung (beispielsweise Exchange Online Multitenant) | Microsoft-ZERTIFIZIERUNGsSTELLE | Buildsystem | Kein Benutzer hat das vollständige Kennwort für den privaten Schlüssel. Das Kennwort ist unter physischer Schutz. |


Die BitLocker-Schlüsselverwaltung umfasst die Verwaltung von Wiederherstellungsschlüsseln, die zum Entsperren/Wiederherstellen verschlüsselter Datenträger in einem Office 365-Rechenzentrum verwendet werden. Office 365 speichert die Hauptschlüssel in einer gesicherten Freigabe, auf die nur Personen zugreifen können, die überprüft und genehmigt wurden. Die Anmeldeinformationen für die Schlüssel werden in einem gesicherten Repository für Zugriffssteuerungsdaten (was wir als "Secret Store" bezeichnet) gespeichert, was eine hohe Ebene der elevations-und Verwaltungs Genehmigungen für den Zugriff auf die Verwendung eines Just-in-Time-Zugriffs erweiterungstools erfordert.

BitLocker unterstützt Schlüssel, die in zwei Verwaltungskategorien fallen:

- Mit BitLocker verwaltete Schlüssel, die in der Regel kurzlebig sind und an die Lebensdauer einer Betriebssysteminstanz gebunden sind, die auf einem Server oder auf einem bestimmten Datenträger installiert ist. Diese Schlüssel werden gelöscht und während der Server Neuinstallation oder Datenträgerformatierung zurückgesetzt.

- BitLocker-Wiederherstellungsschlüssel, die außerhalb von BitLocker verwaltet werden, jedoch zur Datenträger Entschlüsselung verwendet werden. BitLocker verwendet Wiederherstellungsschlüssel für das Szenario, in dem ein Betriebssystem neu installiert wird, und es sind bereits verschlüsselte Datenträger vorhanden. WiederHerstellungsschlüssel werden auch von Überwachungstests für die verwaltete Verfügbarkeit in Exchange Online verwendet, bei denen ein Responder möglicherweise einen Datenträger entsperren muss.

BitLocker-geschützte Volumes werden mit einem vollständigen Volumen Verschlüsselungsschlüssel verschlüsselt, der wiederum mit einem Volume-Hauptschlüssel verschlüsselt wird. BitLocker verwendet FIPS-konforme Algorithmen, um sicherzustellen, dass Verschlüsselungsschlüssel nie im Klartext gespeichert oder über den Draht gesendet werden. Die Office 365-Implementierung des Customer Data-at-Rest-Schutzes weicht nicht von der standardmäßigen BitLocker-Implementierung ab.