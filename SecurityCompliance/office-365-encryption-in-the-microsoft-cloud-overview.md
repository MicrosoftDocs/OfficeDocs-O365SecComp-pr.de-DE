---
title: Verschlüsselung in der Microsoft-Cloud
ms.author: krowley
author: kccross
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Eine Übersicht über die Verschlüsselung in der Microsoft-Cloud.
ms.openlocfilehash: 8d4b94908e9847062ff5f4612b8726b44a36a59f
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30275945"
---
# <a name="encryption-in-the-microsoft-cloud"></a>Verschlüsselung in der Microsoft-Cloud

Kundendaten innerhalb von Microsoft Enterprise Cloud Services werden durch eine Vielzahl von Technologien und Prozessen geschützt, einschließlich verschiedener Verschlüsselungs Formen. (Office 365 Kundendaten in diesem Dokument umfassen Exchange Online-Postfachinhalte (e-Mail-Text, Kalendereinträge und der Inhalt von e-Mail-Anlagen sowie gegebenenfalls Skype for Business-Inhalte), SharePoint Online-Websiteinhalte und die in Websites und Dateien, die in OneDrive for Business oder Skype for Business hochgeladen werden.) Microsoft verwendet mehrere Verschlüsselungsmethoden, Protokolle und Chiffren für seine Produkte und Dienste, um einen sicheren Weg für Kundendaten bereitzustellen, um über unsere Cloud-Dienste zu reisen, und um die Vertraulichkeit von Kundendaten zu schützen, die in Unsere Cloud-Dienste. Microsoft verwendet einige der stärksten, sichersten Verschlüsselungsprotokolle, die verfügbar sind, um Barrieren gegen unbefugten Zugriff auf Kundendaten bereitzustellen. Die OrdnungsGemäße Schlüsselverwaltung ist auch ein wesentliches Element der bewährten Verschlüsselungsmethoden, und Microsoft arbeitet, um sicherzustellen, dass alle von Microsoft verwalteten Verschlüsselungsschlüssel ordnungsgemäß gesichert sind.

Unabhängig von der Kundenkonfiguration werden die in Microsoft Enterprise Cloud Services gespeicherten Kundendaten mithilfe einer oder mehrerer Verschlüsselungs Formen geschützt. (Die Validierung der Crypto-Richtlinie und deren Erzwingung wird von mehreren Drittanbieter Prüfern unabhängig voneinander überprüft, und Berichte über diese Prüfungen stehen im [Service Trust Portal](https://aka.ms/stp)zur Verfügung.)

Microsoft stellt dienstseitige Technologien bereit, die Kundendaten auf Rest-und Transit Ebene verschlüsseln. Für Kundendaten im Ruhezustand verwendet Microsoft Azure beispielsweise [BitLocker](https://docs.microsoft.com/windows/device-security/bitlocker/bitlocker-overview) und [dm-crypt](https://en.wikipedia.org/wiki/Dm-crypt), und Microsoft Office 365 verwendet BitLocker, [Azure Storage Service Encryption](https://azure.microsoft.com/documentation/articles/storage-service-encryption/), Distributed [Key Manager](https://support.office.com/article/989ba10c-f73f-4efb-ad1b-af3322e5f376) (DKM) und Office 365 Service Verschlüsselung. Für Kundendaten in Transit, Azure, Office 365, Microsoft Commercial Support, Microsoft Dynamics 365, Microsoft Power BI und Visual Studio Team Services werden Industriestandard sichere Transportprotokolle wie IPsec (Internet Protocol Security) und Transport Layer Security (TLS) zwischen Microsoft-Datencentern und zwischen Benutzergeräten und Microsoft-Datencentern.

Zusätzlich zu der von Microsoft bereitgestellten Baseline-Ebene der kryptografischen Sicherheit enthalten unsere Cloud-Dienste auch zusätzliche Kryptografie-Optionen, die Sie verwalten können. Sie können beispielsweise die Verschlüsselung für Datenverkehr zwischen Ihren virtuellen Computern (VMs) und ihren Benutzern aktivieren. Mit [virtuellen Azure-Netzwerken](https://azure.microsoft.com/services/virtual-network/)können Sie das standardMäßige IPSec-Protokoll verwenden, um den Datenverkehr zwischen dem VPN-Gateway und Azure des Unternehmens sowie zwischen den VMS im virtuellen Netzwerk zu verschlüsseln. Darüber hinaus können Sie mit [neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md) verschlüsselte e-Mails an alle Benutzer senden.

In Übereinstimmung mit dem Betriebs Sicherheits Standard der Public Key-Infrastruktur, der Bestandteil der [Microsoft-Sicherheitsrichtlinie](https://servicetrust.microsoft.com/ViewPage/TrustDocuments?command=Download&downloadType=Document&downloadId=5868ecc8-50b7-4f91-b43f-640e2b99e86e&docTab=6d000410-c9e9-11e7-9a91-892aae8839ad_FAQ%20and%20White%20Papers)ist, nutzt Microsoft die kryptografischen Funktionen des Windows-Betriebssystems für Zertifikate und Authentifizierungsmechanismen, einschließlich der Verwendung von kryptografischen Modulen, die den FIPS-140-2-Standard ( [Federal Information Processing Standards](http://csrc.nist.gov/publications/PubsFIPS.html) ) der US-Regierung erfüllen. (Relevante NIST-Zertifikat Nummern für Microsoft finden Sie unterhttp://csrc.nist.gov/groups/STM/cmvp/documents/140-1/1401vend.htm.)

> Hinweis Um auf die Microsoft-Sicherheitsrichtlinie als Ressource zuzugreifen, müssen Sie sich mit Ihrem Geschäfts-oder Schulkonto anmelden. Wenn Sie noch kein Abonnement haben, [können Sie sich für eine ﻿kostenlose Testversion registrieren](https://servicetrust.microsoft.com/Home/TrialSubscriptions).

FIPS 140-2 ist ein Standard, der speziell für die Validierung von Produktmodulen entwickelt wurde, die Kryptografie anstelle der Produkte, die Sie verwenden, implementieren. Kryptografische Module, die innerhalb eines Diensts implementiert werden, können als Erfüllung der Anforderungen für Hash-Stärke, Schlüsselverwaltung und ähnliches zertifiziert werden. Wenn kryptografische Funktionen verwendet werden, um die Vertraulichkeit, Integrität und Verfügbarkeit von Daten in Microsoft Cloud Services zu schützen, erfüllen die verwendeten Module und Chiffren den FIPS 140-2-Standard.

Microsoft bescheinigt die zugrunde liegenden kryptografischen Module, die in unseren Cloud-Diensten verwendet werden, mit den neuen Versionen des Windows-Betriebssystems:
- Azure und Azure U.S. Government
- Dynamics 365 und Dynamics 365 U.S. Government
- Office 365, Office 365 U.S. Government und Office 365 U.S. Government Defense

Die Verschlüsselung von Office 365-Kundendaten im Ruhezustand wird von mehreren dienstseitigen Technologien bereitgestellt, einschließlich BitLocker, DKM, Azure Storage Service-Verschlüsselung und Dienst Verschlüsselung in Exchange Online, Skype for Business, OneDrive for Business und SharePoint Online. Die Office 365-Dienst Verschlüsselung enthält eine Option zum Verwenden von Kunden verwalteten Verschlüsselungsschlüsseln, die in Azure Key Vault gespeichert sind. Diese Customer-Managed Key-Option, die als [Office 365-Kundenschlüssel](https://support.office.com/article/f2cd475a-e592-46cf-80a3-1bfb0fa17697)bezeichnet wird, ist für Exchange Online, SharePoint Online, Skype for Business und OneDrive for Business verfügbar.

Für Kundendaten während der Übertragung verhandeln alle Office 365-Server sichere Sitzungen standardmäßig mit TLS mit Clientcomputern, um Kundendaten zu schützen.  Dies gilt für Protokolle auf allen Geräten, die von Clients verwendet werden, wie Skype for Business, Outlook und Outlook im Web, mobilen Clients und Webbrowsern.

(Alle kundenorientierten Server verhandeln standardmäßig mit TLS 1,2, aber wir unterstützen auch die Aushandlung zu einem niedrigeren Standard, falls erforderlich.)

## <a name="related-links"></a>Verwandte Links

- [Verschlüsselung in Azure](office-365-azure-encryption.md)
- [BitLocker und Distributed Key Manager (DKM) für die Verschlüsselung](office-365-bitlocker-and-distributed-key-manager-for-encryption.md)
- [Office 365-Dienstverschlüsselung](office-365-service-encryption.md)
- [Office 365-Verschlüsselung für Skype for Business, OneDrive for Business, SharePoint Online und Exchange Online](office-365-encryption-for-skype-onedrive-sharepoint-and-exchange.md)
- [Verschlüsselung von Daten während der Übertragung](office-365-encryption-for-data-in-transit.md)
- [Vom Kunden verwaltete Verschlüsselungsfunktionen](office-365-customer-managed-encryption-features.md)
- [Verschlüsselungsrisiken und Schutzfunktionen](office-365-encryption-risks-and-protections.md)
- [Verschlüsselung in Microsoft Dynamics 365](office-365-encryption-in-microsoft-dynamics-365.md)