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
# <a name="office-365-encryption-for-data-in-transit"></a><span data-ttu-id="684bf-103">Office 365-Verschlüsselung für Daten während der Übertragung</span><span class="sxs-lookup"><span data-stu-id="684bf-103">Office 365 encryption for data in transit</span></span>

<span data-ttu-id="684bf-104">Zusätzlich zum Schutz von Kundendaten im Ruhezustand verwendet Microsoft-verschlüsselungstechnologien um zu Office 365-Kundendaten während der Übertragung zu schützen.</span><span class="sxs-lookup"><span data-stu-id="684bf-104">In addition to protecting customer data at rest, Microsoft uses encryption technologies to protect Office 365 customer data in transit.</span></span> 

<span data-ttu-id="684bf-105">Daten werden während der Übertragung:</span><span class="sxs-lookup"><span data-stu-id="684bf-105">Data is in transit:</span></span>
- <span data-ttu-id="684bf-106">Bei ein Clientcomputer mit einem Office 365-Server kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="684bf-106">when a client machine communicates with an Office 365 server;</span></span>
- <span data-ttu-id="684bf-107">Wenn ein Office 365-Server mit einem anderen Office 365-Server kommuniziert. und</span><span class="sxs-lookup"><span data-stu-id="684bf-107">when an Office 365 server communicates with another Office 365 server; and</span></span>
- <span data-ttu-id="684bf-108">Wenn ein Office 365-Server mit einem nicht - Office 365-Server (z. B. Versendung e-Mails an einen fremden e-Mail-Server Exchange Online) kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="684bf-108">when an Office 365 server communicates with a non-Office 365 server (e.g., Exchange Online delivering email to a foreign email server).</span></span>

<span data-ttu-id="684bf-p101">Inter-Datacenter-Kommunikation zwischen Office 365-Servern erfolgt über TLS oder IPsec und alle Kunden auszufüllende Server eine sichere Sitzung mit TLS mit Clientcomputern Aushandeln (z. B. Exchange Online verwendet TLS 1.2 mit Stärke 256-Bit-Verschlüsselung wird verwendet (FIPS 140-2-Ebene 2 überprüft). (Siehe [technische Details über die Verschlüsselung in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) für eine Liste der TLS-Verschlüsselung-Versionen von Office 365 unterstützt.) Dies gilt für die Protokolle, die von den Clients wie Outlook, Skype für Unternehmen und Outlook im Web (z. B. HTTP, POP3, usw.) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="684bf-p101">Inter-datacenter communications between Office 365 servers takes place over TLS or IPsec, and all customer-facing servers negotiate a secure session using TLS with client machines (e.g., Exchange Online uses TLS 1.2 with 256-bit cipher strength is used (FIPS 140-2 Level 2-validated). (See [Technical reference details about encryption in Office 365](https://support.office.com/article/Technical-reference-details-about-encryption-in-Office-365-862CBE93-4268-4EF9-BA79-277545ECF221) for a list of TLS cipher suites supported by Office 365.) This applies to the protocols that are used by clients such as Outlook, Skype for Business, and Outlook on the web (e.g., HTTP, POP3, etc.).</span></span>

<span data-ttu-id="684bf-p102">Öffentliche Zertifikate werden von Microsoft IT SSL ausgestellt von SSLAdmin, ein internes Microsoft-Tool zum Schutz Vertraulichkeit der übertragenen Informationen. Alle von Microsoft IT ausgestellten Zertifikate müssen mindestens 2.048 Bit lang Länge und [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) Compliance erfordert SSLAdmin, um sicherzustellen, dass nur für öffentliche IP-Adressen im Besitz von Microsoft Zertifikate ausgestellt werden. IP-Adressen, für die dieses Kriterium erfüllen, werden durch ein Prozess, der Ausnahme weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="684bf-p102">The public certificates are issued by Microsoft IT SSL using SSLAdmin, an internal Microsoft tool to protect confidentiality of transmitted information. All certificates issued by Microsoft IT have a minimum of 2048 bits in length, and [Webtrust](http://www.webtrust.org/homepage-documents/item70372.pdf) compliance requires SSLAdmin to make sure that certificates are issued only to public IP addresses owned by Microsoft. Any IP addresses that fail to meet this criterion are routed through an exception process.</span></span>

<span data-ttu-id="684bf-p103">Alle Details der Implementierung wie die Version von TLS verwendet wird, ob Forward Secrecy (EA) aktiviert ist, die Reihenfolge der Verschlüsselungsanbieter-Suites usw., sind öffentlich verfügbar. Eine Möglichkeit, diese Informationen finden Sie unter ist die Verwendung eine Drittanbieter-Website, wie etwa Qualys SSL Labs (www.ssllabs.com). Im folgenden finden Sie die Links zu automatisierten Testseiten aus Qualys, die Informationen für die folgenden Dienste an:</span><span class="sxs-lookup"><span data-stu-id="684bf-p103">All implementation details such as the version of TLS being used, whether Forward Secrecy (FS) is enabled, the order of cipher suites, etc., are available publicly. One way to see these details is to use a third-party website, such as Qualys SSL Labs (www.ssllabs.com). Below are the links to automated test pages from Qualys that display information for the following services:</span></span>
- [<span data-ttu-id="684bf-117">Office 365-Portal</span><span class="sxs-lookup"><span data-stu-id="684bf-117">Office 365 Portal</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=portal.office.com&hideResults=on)
- [<span data-ttu-id="684bf-118">Exchange Online</span><span class="sxs-lookup"><span data-stu-id="684bf-118">Exchange Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=outlook.office365.com&hideResults=on)
- [<span data-ttu-id="684bf-119">SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="684bf-119">SharePoint Online</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=microsoft-my.sharepoint.com&hideResults=on)
- [<span data-ttu-id="684bf-120">Skype für Unternehmen (SIP)</span><span class="sxs-lookup"><span data-stu-id="684bf-120">Skype for Business (SIP)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=sipdir.online.lync.com)
- [<span data-ttu-id="684bf-121">Skype für Unternehmen (Web)</span><span class="sxs-lookup"><span data-stu-id="684bf-121">Skype for Business (Web)</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=webdir.online.lync.com&hideResults=on)
- [<span data-ttu-id="684bf-122">Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="684bf-122">Exchange Online Protection</span></span>](https://ssl-tools.net/mailservers/microsoft-com.mail.protection.outlook.com)
- [<span data-ttu-id="684bf-123">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="684bf-123">Microsoft Teams</span></span>](https://www.ssllabs.com/ssltest/analyze.html?d=teams.microsoft.com&latest)

<span data-ttu-id="684bf-124">Für Exchange Online Protection unterscheiden sich von Mandanten Namen URLs. alle Kunden können jedoch Office 365 mit **Microsoft-com.mail.protection.outlook.com**testen.</span><span class="sxs-lookup"><span data-stu-id="684bf-124">For Exchange Online Protection, URLs vary by tenant names; however, all customers can test Office 365 using **microsoft-com.mail.protection.outlook.com**.</span></span>
