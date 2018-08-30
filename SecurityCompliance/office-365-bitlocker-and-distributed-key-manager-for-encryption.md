---
title: Office 365 BitLocker-Verschlüsselung
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Informationen zu BitLocker-Verschlüsselung in der Cloud.'
ms.openlocfilehash: 86c6bc9282d7c2b0a7d4e08d4636c8f9c2fa5db8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529467"
---
# <a name="bitlocker-and-distributed-key-manager-dkm-for-encryption"></a>BitLocker und verteilten Key Manager (DKM) für die Verschlüsselung
Office 365-Server verwenden BitLocker für die Verschlüsselung von Laufwerken mit Kundendaten auf Volume-Ebene. BitLocker-Verschlüsselung ist eine Datenverschlüsselungsfunktion, die in Windows integriert ist. BitLocker ist eine der Technologien, die zum Schutz vor Bedrohungen verwendet werden, falls andere Prozesse oder Steuerelemente hinfällig werden (z. B. Zugriffssteuerung oder Access Control oder Recycling von Hardware), sodass andere Personen möglicherweise physischen Zugriff auf Laufwerke mit Kundendaten erlangen könnten. In diesem Fall eliminiert BitLocker das potenzielle Risiko für Datendiebstahl oder Offenlegung aufgrund von verloren gegangener, gestohlener oder nicht ordnungsgemäß außer Betrieb gesetzter Computer und Datenträger. 

BitLocker wird mit AES Advanced Encryption Standard () 256-Bit-Verschlüsselung für Datenträger mit Kundendaten in Exchange Online, SharePoint Online und Skype für Unternehmen bereitgestellt. Datenträger Bereiche werden mit einer vollständigen Volume Encryption Key (FVEK), verschlüsselt, die mit dem Hauptschlüssel (Volume VMK), verschlüsselt werden sollen, die wiederum an das Modul TPM (Trusted Platform) auf dem Server gebunden ist. Der VMK schützt direkt der FVEK und daher schützen den VMK wird zu einem wichtigen. Die folgende Abbildung zeigt ein Beispiel für die Zertifikatskette der BitLocker-Sicherheit für den Schlüssel für einen bestimmten Server (in diesem Fall mit einem Server mit Exchange Online).

Die folgende Tabelle beschreibt die Zertifikatskette der BitLocker-Sicherheit für den Schlüssel für einen bestimmten Server (in diesem Fall ein Exchange Online-Server).

| KEY-SCHUTZ | GRANULARITÄT | WIE GENERIERTEN? | WO SIND SIE GESPEICHERT? | SCHUTZ |
|--------------------------------------------------------------------------------|-------------------------------------------------|----------------|-------------------------|--------------------------------------------------------------------------------------------------|
| 256-Bit-AES-externe Schlüssel | Pro Server | BitLocker-APIs | TPM oder geheimen Safe | Lockbox / Zugriffssteuerung |
|  |  |  | Mailbox-Server-Registrierung | TPM verschlüsselt |
| 48 Ziffern bestehenden numerischen Kennwort | Pro Datenträger | BitLocker-APIs | Active Directory | Lockbox / Zugriffssteuerung |
| X. 509-Zertifikat als Daten Recovery Agent (DRA) auch öffentliche Schlüssel Schutzkomponente bezeichnet. | Umgebung (z. B. Exchange Online Multitenant) | Microsoft-Zertifizierungsstelle | System erstellen | Kein ein Benutzer hat das vollständige Kennwort für den privaten Schlüssel. Das Kennwort ist unter physischen Schutz. |


BitLocker-Schlüsselverwaltungsdienst umfasst die Verwaltung von Recovery-Schlüssel, die zum Entsperren und Wiederherstellen von verschlüsselten Datenträger in ein Office 365-Datencenter verwendet werden. Office 365 speichert die Hauptschlüssel in einer gesicherten freigeben, nur von Personen, die überwachten und genehmigt zugegriffen werden. Die Anmeldeinformationen für die Schlüssel befinden sich in einem sicheren Repository für Zugriffssteuerungsdaten (was wir einen "geheimen Speicher" aufrufen), erfordert ein hohes Maß an EoP und Verwaltung Genehmigungen für den Zugriff auf über ein Just-in-Time-Access Elevation-Tool.

BitLocker unterstützt zwei Management Kategorien Schlüssel:
- BitLocker-Mitarbeiter Schlüssel, die im Allgemeinen kurzlebige und der Lebensdauer einer Betriebssystem-Instanz auf einem Server installiert oder auf einem bestimmten Datenträger gebunden sind. Diese Schlüssel werden gelöscht und während Server Neuinstallation oder Datenträger Formatierung zurückgesetzt.
- BitLocker Recovery-Schlüssel, die außerhalb von BitLocker verwaltet jedoch für die Entschlüsselung Datenträger verwendet werden. BitLocker verwendet Wiederherstellungsschlüssel für das Szenario, in dem ein Betriebssystem neu installiert wird und verschlüsselten Daten Datenträger bereits vorhanden sein. Recovery-Schlüssel werden auch durch die verwaltete Verfügbarkeit monitoring Tests in Exchange Online, in denen ein Responder muss möglicherweise auf einen Datenträger entsperren verwendet.

BitLocker-geschützten Volumes werden mit einer vollständigen Volume Verschlüsselungsschlüssel verschlüsselt, das wiederum mit eines Volumehauptschlüssels verschlüsselt wird. BitLocker verwendet FIPS-kompatible Algorithmen, um sicherzustellen, dass Verschlüsselungsschlüssel noch nie gespeichert oder über das Netzwerk als Klartext gesendet werden. Die Office 365-Implementierung der Customer-an-Rest-Schutz nicht von der standardmäßige BitLocker-Implementierung abweichen.