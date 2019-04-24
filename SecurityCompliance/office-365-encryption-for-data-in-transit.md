---
title: Office 365-Verschlüsselung für Daten während der Übertragung
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
- Strat_O365_Enterprise
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Zusammenfassung: eine kurze Erläuterung, wie Microsoft Daten während der Übertragung verschlüsselt.'
ms.openlocfilehash: ba1317a0a2a685d0f3ac2216939d04e402503e49
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262797"
---
# <a name="office-365-encryption-for-data-in-transit"></a>Office 365-Verschlüsselung für Daten während der Übertragung

Zusätzlich zum Schutz von Kundendaten im Ruhezustand verwendet Microsoft Verschlüsselungstechnologien, um Office 365-Kundendaten während der Übertragung zu schützen. 

Die Daten werden übermittelt:

- Wenn ein Clientcomputer mit einem Office 365-Server kommuniziert;
- Wenn ein Office 365-Server mit einem anderen Office 365-Server kommuniziert; und
- Wenn ein Office 365-Server mit einem nicht-Office 365-Server kommuniziert (beispielsweise Exchange Online, der e-Mails an einen fremden e-Mail-Server zustellt).

Die Kommunikation zwischen Datencentern zwischen Office 365-Servern erfolgt über TLS oder IPsec, und alle kundenorientierten Server verhandeln eine sichere Sitzung mit TLS mit Clientcomputern (beispielsweise verwendet Exchange Online TLS 1,2 mit 256-Bit-Verschlüsselungsstärke wird verwendet (FIPS 140-2 Level 2-validiert). (Siehe [technische Referenzdetails zur Verschlüsselung in office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) für eine Liste der von Office 365 unterstützten TLS-Verschlüsselungs Pakete.) Dies gilt für die Protokolle, die von Clients wie Outlook, Skype for Business und Outlook im Web (beispielsweise HTTP, POP3 usw.) verwendet werden.

Die öffentlichen Zertifikate werden von Microsoft IT SSL mithilfe von SSLAdmin, einem internen Microsoft-Tool zum Schutz der Vertraulichkeit von übermittelten Informationen, ausgegeben. Alle von Microsoft ausgegebenen Zertifikate haben ein Minimum von 2048 Bit Länge, und [](http://www.webtrust.org/homepage-documents/item70372.pdf) die WebTrust-Compliance erfordert SSLAdmin, um sicherzustellen, dass Zertifikate nur für öffentliche IP-Adressen ausgestellt werden, die im Besitz von Microsoft sind. Alle IP-Adressen, die dieses Kriterium nicht erfüllen, werden durch einen Ausnahme Prozess weitergeleitet.

Alle Implementierungsdetails wie die verwendete TLS-Version, ob das Forward-Geheimhaltungsverfahren (FS) aktiviert ist, die Reihenfolge der Verschlüsselungs Pakete usw. sind öffentlich verfügbar. Eine Möglichkeit, diese Details anzuzeigen, ist die Verwendung einer Drittanbieterwebsite wie Qualys SSL Labs (www.ssllabs.com). Nachfolgend finden Sie die Links zu automatisierten Testseiten von Qualys, die Informationen für die folgenden Dienste anzeigen:

- [Office 365-Portal](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype for Business (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype for Business (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Für Exchange Online Protection variieren URLs nach Mandantennamen; Allerdings können alle Kunden Office 365 mit **Microsoft-com.Mail.Protection.Outlook.com**testen.
