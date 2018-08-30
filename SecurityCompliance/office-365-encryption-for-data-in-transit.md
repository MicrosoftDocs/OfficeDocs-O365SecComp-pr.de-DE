---
title: Office 365-Verschlüsselung für Daten während der Übertragung
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
description: 'Zusammenfassung: Eine kurze Erläuterung der wie Microsoft Daten während der Übertragung verschlüsselt.'
ms.openlocfilehash: 8f4781cf1127fb1b6bf742c267c76e3df39b8209
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528905"
---
# <a name="office-365-encryption-for-data-in-transit"></a>Office 365-Verschlüsselung für Daten während der Übertragung

Zusätzlich zum Schutz von Kundendaten im Ruhezustand verwendet Microsoft-verschlüsselungstechnologien um zu Office 365-Kundendaten während der Übertragung zu schützen. 

Daten werden während der Übertragung:
- Bei ein Clientcomputer mit einem Office 365-Server kommuniziert.
- Wenn ein Office 365-Server mit einem anderen Office 365-Server kommuniziert. und
- Wenn ein Office 365-Server mit einem nicht - Office 365-Server (z. B. Versendung e-Mails an einen fremden e-Mail-Server Exchange Online) kommuniziert.

Inter-Datacenter-Kommunikation zwischen Office 365-Servern erfolgt über TLS oder IPsec und alle Kunden auszufüllende Server eine sichere Sitzung mit TLS mit Clientcomputern Aushandeln (z. B. Exchange Online verwendet TLS 1.2 mit Stärke 256-Bit-Verschlüsselung wird verwendet (FIPS 140-2-Ebene 2 überprüft). (Siehe [technische Details über die Verschlüsselung in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) für eine Liste der TLS-Verschlüsselung-Versionen von Office 365 unterstützt.) Dies gilt für die Protokolle, die von den Clients wie Outlook, Skype für Unternehmen und Outlook im Web (z. B. HTTP, POP3, usw.) verwendet werden.

Öffentliche Zertifikate werden von Microsoft IT SSL ausgestellt von SSLAdmin, ein internes Microsoft-Tool zum Schutz Vertraulichkeit der übertragenen Informationen. Alle von Microsoft IT ausgestellten Zertifikate müssen mindestens 2.048 Bit lang Länge und [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) Compliance erfordert SSLAdmin, um sicherzustellen, dass nur für öffentliche IP-Adressen im Besitz von Microsoft Zertifikate ausgestellt werden. IP-Adressen, für die dieses Kriterium erfüllen, werden durch ein Prozess, der Ausnahme weitergeleitet.

Alle Details der Implementierung wie die Version von TLS verwendet wird, ob Forward Secrecy (EA) aktiviert ist, die Reihenfolge der Verschlüsselungsanbieter-Suites usw., sind öffentlich verfügbar. Eine Möglichkeit, diese Informationen finden Sie unter ist die Verwendung eine Drittanbieter-Website, wie etwa Qualys SSL Labs (www.ssllabs.com). Im folgenden finden Sie die Links zu automatisierten Testseiten aus Qualys, die Informationen für die folgenden Dienste an:
- [Office 365-Portal](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [Exchange Online](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [SharePoint Online](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [Skype für Unternehmen (SIP)](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [Skype für Unternehmen (Web)](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [Exchange Online Protection](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [Microsoft Teams](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

Für Exchange Online Protection unterscheiden sich von Mandanten Namen URLs. alle Kunden können jedoch Office 365 mit **Microsoft-com.mail.protection.outlook.com**testen.
