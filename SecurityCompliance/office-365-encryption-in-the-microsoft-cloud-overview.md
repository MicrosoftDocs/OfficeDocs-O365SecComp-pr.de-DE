---
title: Verschlüsselung in der Microsoft-Cloud
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
description: Eine Übersicht der in der Microsoft-Cloud-Verschlüsselung.
ms.openlocfilehash: b8dee7ca7a791878763b885ada40a1d87f074e8e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529869"
---
# <a name="encryption-in-the-microsoft-cloud"></a>Verschlüsselung in der Microsoft-Cloud

Kundendaten innerhalb von Microsoft Enterprise-Cloud-Diensten ist durch eine Vielzahl von Technologien und Prozesse, einschließlich der verschiedenen Formen der Verschlüsselung geschützt. (Office 365 Kundendaten in diesem Dokument enthält Exchange Online Inhalt von Postfächern (e-Mail-Body, Kalendereinträge und den Inhalt der E-mail-Anlagen und gegebenenfalls Skype für Geschäftsinhalten), SharePoint Online Websiteinhalt und Speicherort der Dateien in Websites und Dateien zu OneDrive for Business oder Skype für Unternehmen hochgeladen.) Microsoft verwendet mehrere Verschlüsselungsmethoden, Protokolle und Verschlüsselungen in seiner Produkte und Dienste um zu unterstützen, geben Sie einen sicheren Pfad für Kundendaten über unsere Clouddienste weitergeleitet, und helfen, die Vertraulichkeit der Kundendaten zu schützen, die in der gespeichert ist Unsere Clouddienste. Microsoft setzt einige der stärksten, sicherste Verschlüsselungsprotokolle Hindernisse vor unbefugten Zugriff auf Kundendaten zu bieten. Ordnungsgemäße Key Management ist auch eine entscheidende Verschlüsselung bewährte Methoden und Microsoft möchte sicherstellen, dass alle Microsoft-Mitarbeiter Verschlüsselungsschlüssel ordnungsgemäß gesichert werden.

Unabhängig von der Konfiguration des Kunden ist innerhalb von Microsoft Enterprise Clouddiensten gespeicherte Kundendaten mit einem oder mehreren Formularen Verschlüsselungsgrad geschützt. (Validierung von unsere Kryptografie Richtlinien und die Erzwingung wird unabhängig voneinander überprüft, indem mehrere Drittanbieter-Auditoren und Berichte über diese Überwachungen stehen auf dem [Dienstportal vertrauen](https://aka.ms/stp).)

Microsoft bietet dienstseitige-Technologien, die Kundendaten im Ruhezustand und bei der Übertragung verschlüsselt. Beispiel für Kundendaten im Ruhezustand Microsoft Azure verwendet, [BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) und [DM Crypt](https://en.wikipedia.org/wiki/Dm-crypt)und Microsoft Office 365 verwendet BitLocker, [Azure Storage Service Encryption](https://azure.microsoft.com/documentation/articles/storage-service-encryption/), [Verteilten Schlüssel-Manager](https://support.office.com/article/989ba10c-f73f-4efb-ad1b-af3322e5f376) (DKM) und Office 365-Dienst Verschlüsselung. Verwenden Sie für Kundendaten während der Übertragung, Azure, Office 365, kommerzielle Support von Microsoft, Microsoft Dynamics 365, Microsoft Power BI und Visual Studio Team Services sicheren Transport Industriestandard-Protokolle, wie Internet Protocol Security (IPsec) und Transport Layer Security (TLS) zwischen Microsoft-Rechenzentren und Benutzer Geräte und Microsoft-Rechenzentren.

Neben der Baseline Sicherheitsstufe kryptografische von Microsoft bereitgestellt wurden zählen unsere Clouddienste auch zusätzlicher kryptografischer-Optionen, die Sie verwalten können. Beispielsweise können Sie die Verschlüsselung für den Datenverkehr zwischen ihrer virtuellen Azure-Computern (VMs) und der entsprechenden Benutzer aktivieren. Mit [Azure-virtuelle Netzwerke](https://azure.microsoft.com/services/virtual-network/)können Sie das Protokoll der Branchenstandard IPsec zum Verschlüsseln von Datenverkehr zwischen Ihrem Unternehmen VPN-Gateway und Azure sowie zwischen den virtuellen Computern auf Ihr virtuelles Netzwerk befinden. Darüber hinaus darüber hinaus können [die neuen Funktionen von Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md) Sie verschlüsselte e-Mail-Nachrichten an alle Personen senden.

Nach der öffentlichen Schlüssel Infrastruktur betriebliche Security Standard, die eine Komponente der [Codezugriffssicherheits-Richtlinie von Microsoft](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5868ecc8-50b7-4f91-b43f-640e2b99e86e&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ%20and%20White%20Papers)ist, nutzt Microsoft die Verschlüsselungsfunktionen in Windows-Betriebssystems für Zertifikate enthalten und Authentifizierungsmechanismen, die die Verwendung von kryptografischen Module enthält, die der US-Regierung [Federal Information Processing Standards](http://csrc.nist.gov/publications/PubsFIPS.html) (FIPS) 140-2-Standard entsprechen. (Relevante NIST Zertifikat Zahlen für Microsoft finden Sie unterhttp://csrc.nist.gov/groups/STM/cmvp/documents/140-1/1401vend.htm.)

> [HINWEIS] Zugriff auf die Microsoft-Sicherheitsrichtlinie als Ressource müssen Sie mit Ihrem arbeiten oder Schule-Konto anmelden. Wenn Sie nicht über ein Abonnement noch, [Sie können melden Sie sich für eine kostenlose Testversion](https://servicetrust.microsoft.com/Home/TrialSubscriptions)verfügen.

FIPS 140-2 ist ein Standard, die speziell für das Produkt-Module, die die Produkte, die sie verwenden, sondern Kryptografie implementieren überprüfen. Kryptografische Module, die in einem Dienst implementiert werden können als die Anforderungen für Hash Stärke, Key Management und ähnliche meeting zertifiziert werden. Jedes Mal, wenn Verschlüsselungsfunktionen beschäftigt sind, um die Vertraulichkeit, Integrität oder Verfügbarkeit der Daten in die Microsoft Cloud Services zu schützen erfüllen die Module und Chiffre verwendet den FIPS 140-2-Standard.

Microsoft zertifiziert die zugrunde liegenden kryptografischen Modulen in unsere Cloud-Diensten mit jeder Version des Betriebssystems Windows verwendet:
- Azure und Azure US-Regierung
- Dynamics 365 und Dynamics 365 US-Regierung
- Office 365, Office 365 US-Regierung und Office 365 US-Regierung Verteidigung

Verschlüsselung von Office 365-Kundendaten im Ruhezustand wird durch mehrere dienstseitige Technologien, einschließlich BitLocker, DKM, Azure Storage Service Verschlüsselung und die Verschlüsselung der Service im Exchange Online, Skype für Unternehmen, OneDrive für Unternehmen und SharePoint bereitgestellt Online. Office 365-Dienst Verschlüsselung umfasst eine Option zum Kunden verwalteten Verschlüsselungsschlüssel verwenden, die in Azure Schlüssel Vault gespeichert sind. Diese Kunden-Mitarbeiter wichtige Option namens [Office 365-Kunden-Taste](https://support.office.com/article/f2cd475a-e592-46cf-80a3-1bfb0fa17697), ist für Exchange Online, SharePoint Online, Skype für Unternehmen und OneDrive für Unternehmen verfügbar.

Für Kundendaten während der Übertragung aushandeln allen Office 365-Servern sichere Sitzungen, die Verwendung von TLS standardmäßig mit Clientcomputern den Schutz von Kundendaten.  Dies gilt für Protokolle auf jedem Gerät von Clients wie beispielsweise Skype für Unternehmen, Outlook und Outlook auf den Web-, mobilen Clients und Web-Browser verwendet.

(Alle Kunden auszufüllende Server aushandeln auf TLS 1.2 standardmäßig, aber wir unterstützen außerdem aushandeln nach unten zu einem niedrigeren Standard, falls erforderlich).

## <a name="related-links"></a>Verwandte Links

- [Verschlüsselung in Azure](office-365-azure-encryption.md)
- [BitLocker und verteilten Key Manager (DKM) für die Verschlüsselung](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)
- [Verschlüsselung für Office 365-Dienst](office-365-service-encryption.md)
- [Office 365-Verschlüsselung für Skype für Unternehmen, OneDrive für Unternehmen, SharePoint Online und Exchange Online](office-365-encryption-for-skype-onedrive-sharepoint-and-exchange.md)
- [Verschlüsselung für Daten während der Übertragung](office-365-encryption-for-data-in-transit.md)
- [Kunden-Mitarbeiter Verschlüsselungsfunktionen](office-365-customer-managed-encryption-features.md)
- [Verschlüsselung Risiken und Schutzebenen](office-365-encryption-risks-and-protections.md)
- [Verschlüsselung in Microsoft Dynamics 365](office-365-encryption-in-microsoft-dynamics-365.md)