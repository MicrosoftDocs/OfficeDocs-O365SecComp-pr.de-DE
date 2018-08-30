---
title: Schutz vor Denial-of-Service-Angriffen in Office 365
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
description: Eine Übersicht über Denial-of-Service (DoS) Angriffe.
ms.openlocfilehash: b5a51ae332b32142d9ab993a29763b2160c3ce97
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528844"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="1fe07-103">Schutz vor Denial-of-Service-Angriffen in Office 365</span><span class="sxs-lookup"><span data-stu-id="1fe07-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="1fe07-104">Einführung</span><span class="sxs-lookup"><span data-stu-id="1fe07-104">Introduction</span></span>
<span data-ttu-id="1fe07-105">Microsoft bietet eine trustworthy Infrastruktur für mehr als 200 Cloud-Dienste, einschließlich Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype und Xbox Live, die in unserer globalen Cloud gehostet werden Infrastruktur von mehr als 100 Rechenzentren.</span><span class="sxs-lookup"><span data-stu-id="1fe07-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="1fe07-p101">Als globale Organisation eine erhebliche Internetauftritt und viele wichtigsten Internet-Eigenschaften, die Clouddienste bereitstellen, ist Microsoft eine große, allgemeine Ziel für Hacker und andere böswilligen Personen. Die Netzwerk - Schicht für die Kommunikation zwischen Clients und der Microsoft-Cloud – ist der größten Zielgruppen vor böswilligen Angriffen. Tatsächlich seit vielen Jahren wurde Microsoft fortlaufend und dauerhaft unter einer Form von Netzwerk-basierte berichtet. In fast allen Fällen ist mindestens eine der Eigenschaften von Microsoft Internet eines Angriffs aufgetreten. Ohne zuverlässigen und beständigen Risikominderung-Systemen, die Verteidigung gegen diese Angriffe können, wäre Microsofts Cloud-Dienste offline und Kunden nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1fe07-p101">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals. The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks. In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack. At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack. Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="1fe07-111">Microsoft verwendet Verteidigung Sicherheitsprinzipien, um dessen Clouddiensten und Netzwerke schützen.</span><span class="sxs-lookup"><span data-stu-id="1fe07-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="1fe07-112">Definition und Symptome von Denial-of-Service-Angriffen</span><span class="sxs-lookup"><span data-stu-id="1fe07-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="1fe07-p102">Eine Möglichkeit, Angriffe auf Netzwerkdienste ist die Erstellung viele Anforderungen anhand eines Diensts Hosts zu überlasten Netzwerk und Servern Dienst für legitime Benutzer abgelehnt werden sollen. Dies wird als Denial-of-Service-Angriff (DoS) bezeichnet. Wenn der Angriff durch mehrere Akteure, Endpunkte und/oder Vektoren ausgeführt wird, wird es als einer verteilten Denial-of-Service-Angriff (DDoS) bezeichnet. Obwohl die Möglichkeit, Motive und Ziele variieren, bestehen DoS und DDoS-Angriffen in der Regel die Arbeit von Personen oder einer Person, um eine Internet-Website oder ein Dienst nicht ordnungsgemäß funktioniert oder überhaupt, vorübergehend oder auf unbestimmte Zeit zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="1fe07-p102">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users. This is referred to as a denial-of-service (DoS) attack. When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack. Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="1fe07-117">[Vereinigte Staaten Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) definiert Symptome von DoS-Angriffen enthalten:</span><span class="sxs-lookup"><span data-stu-id="1fe07-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="1fe07-118">Ungewöhnlich langsame netzwerkleistung (beim Öffnen von Dateien oder den Zugriff auf Internet-Sites)</span><span class="sxs-lookup"><span data-stu-id="1fe07-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="1fe07-119">Ausfall einer Website</span><span class="sxs-lookup"><span data-stu-id="1fe07-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="1fe07-120">Fehler beim Zugriff auf eine Website</span><span class="sxs-lookup"><span data-stu-id="1fe07-120">Inability to access a Web site</span></span>
- <span data-ttu-id="1fe07-121">Erhebliche Steigerung empfangener spam</span><span class="sxs-lookup"><span data-stu-id="1fe07-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="1fe07-122">Trennen der Verbindung über eine drahtlose oder drahtgebundene Verbindung zum Internet</span><span class="sxs-lookup"><span data-stu-id="1fe07-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="1fe07-123">Langfristige Verlust des Zugriffs auf die Web- oder alle Internetdienste</span><span class="sxs-lookup"><span data-stu-id="1fe07-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fe07-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="1fe07-124">Related Topics</span></span>
- [<span data-ttu-id="1fe07-125">Wesentliche Prinzipien Schutz vor Denial-of-Service-Angriffen</span><span class="sxs-lookup"><span data-stu-id="1fe07-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="1fe07-126">Microsoft Defense Denial-of-Service-Strategie</span><span class="sxs-lookup"><span data-stu-id="1fe07-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="1fe07-127">Verteidigen Microsoft Cloud-Dienste vor Denial-of-Service-Angriffen</span><span class="sxs-lookup"><span data-stu-id="1fe07-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
