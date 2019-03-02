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
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357606"
---
# <a name="office-365-encryption-for-data-in-transit"></a><span data-ttu-id="6a561-103">Office 365-Verschlüsselung für Daten während der Übertragung</span><span class="sxs-lookup"><span data-stu-id="6a561-103">Office 365 encryption for data in transit</span></span>

<span data-ttu-id="6a561-104">Zusätzlich zum Schutz von Kundendaten im Ruhezustand verwendet Microsoft Verschlüsselungstechnologien, um Office 365-Kundendaten während der Übertragung zu schützen.</span><span class="sxs-lookup"><span data-stu-id="6a561-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect Office 365 customer data in transit.</span></span> 

<span data-ttu-id="6a561-105">Die Daten werden übermittelt:</span><span class="sxs-lookup"><span data-stu-id="6a561-105">Data is in transit:</span></span>

- <span data-ttu-id="6a561-106">Wenn ein Clientcomputer mit einem Office 365-Server kommuniziert;</span><span class="sxs-lookup"><span data-stu-id="6a561-106">when a client machine communicates with an Office 365 server;</span></span>
- <span data-ttu-id="6a561-107">Wenn ein Office 365-Server mit einem anderen Office 365-Server kommuniziert; und</span><span class="sxs-lookup"><span data-stu-id="6a561-107">when an Office 365 server communicates with another Office 365 server; and</span></span>
- <span data-ttu-id="6a561-108">Wenn ein Office 365-Server mit einem nicht-Office 365-Server kommuniziert (beispielsweise Exchange Online, der e-Mails an einen fremden e-Mail-Server zustellt).</span><span class="sxs-lookup"><span data-stu-id="6a561-108">when an Office 365 server communicates with a non-Office 365 server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="6a561-p101">Die Kommunikation zwischen Datencentern zwischen Office 365-Servern erfolgt über TLS oder IPsec, und alle kundenorientierten Server verhandeln eine sichere Sitzung mit TLS mit Clientcomputern (beispielsweise verwendet Exchange Online TLS 1,2 mit 256-Bit-Verschlüsselungsstärke wird verwendet (FIPS 140-2 Level 2-validiert). (Siehe [technische Referenzdetails zur Verschlüsselung in office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) für eine Liste der von Office 365 unterstützten TLS-Verschlüsselungs Pakete.) Dies gilt für die Protokolle, die von Clients wie Outlook, Skype for Business und Outlook im Web (beispielsweise HTTP, POP3 usw.) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6a561-p101">Inter-datacenter communications between Office 365 servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated). (See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="6a561-p102">Die öffentlichen Zertifikate werden von Microsoft IT SSL mithilfe von SSLAdmin, einem internen Microsoft-Tool zum Schutz der Vertraulichkeit von übermittelten Informationen, ausgegeben. Alle von Microsoft ausgegebenen Zertifikate haben ein Minimum von 2048 Bit Länge, und [](http://www.webtrust.org/homepage-documents/item70372.pdf) die WebTrust-Compliance erfordert SSLAdmin, um sicherzustellen, dass Zertifikate nur für öffentliche IP-Adressen ausgestellt werden, die im Besitz von Microsoft sind. Alle IP-Adressen, die dieses Kriterium nicht erfüllen, werden durch einen Ausnahme Prozess weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="6a561-p102">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information. All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft. Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="6a561-p103">Alle Implementierungsdetails wie die verwendete TLS-Version, ob das Forward-Geheimhaltungsverfahren (FS) aktiviert ist, die Reihenfolge der Verschlüsselungs Pakete usw. sind öffentlich verfügbar. Eine Möglichkeit, diese Details anzuzeigen, ist die Verwendung einer Drittanbieterwebsite wie Qualys SSL Labs (www.ssllabs.com). Nachfolgend finden Sie die Links zu automatisierten Testseiten von Qualys, die Informationen für die folgenden Dienste anzeigen:</span><span class="sxs-lookup"><span data-stu-id="6a561-p103">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly. One way to see these details is to use a third-party website, such as Qualys SSL Labs (www.ssllabs.com). Below are the links to automated test pages from Qualys that display information for the following services:</span></span>

- [<span data-ttu-id="6a561-117">Office 365-Portal</span><span class="sxs-lookup"><span data-stu-id="6a561-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="6a561-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="6a561-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="6a561-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="6a561-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="6a561-120">Skype for Business (SIP)</span><span class="sxs-lookup"><span data-stu-id="6a561-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="6a561-121">Skype for Business (Web)</span><span class="sxs-lookup"><span data-stu-id="6a561-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="6a561-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="6a561-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="6a561-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="6a561-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="6a561-124">Für Exchange Online Protection variieren URLs nach Mandantennamen; Allerdings können alle Kunden Office 365 mit **Microsoft-com.Mail.Protection.Outlook.com**testen.</span><span class="sxs-lookup"><span data-stu-id="6a561-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Office 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
