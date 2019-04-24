---
title: Schutz vor Denial-of-Service-anGriffen in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Übersicht über Denial-of-Service-Angriffe (DoS).
ms.openlocfilehash: a7e67fcc87867190f345c5dad14e38a473420eab
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262817"
---
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a><span data-ttu-id="2342f-103">Schutz vor Denial-of-Service-anGriffen in Office 365</span><span class="sxs-lookup"><span data-stu-id="2342f-103">Defending Against Denial-of-Service Attacks in Office 365</span></span>

## <a name="introduction"></a><span data-ttu-id="2342f-104">Einführung</span><span class="sxs-lookup"><span data-stu-id="2342f-104">Introduction</span></span>
<span data-ttu-id="2342f-105">Microsoft bietet eine vertrauenswürdige Infrastruktur für mehr als 200 Cloud-Dienste, einschließlich Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype und Xbox Live, die in unserer globalen Cloud gehostet werden. Infrastruktur von mehr als 100 Rechenzentren.</span><span class="sxs-lookup"><span data-stu-id="2342f-105">Microsoft delivers a trustworthy infrastructure for more than 200 cloud services, including Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype, and Xbox Live that are hosted in our global cloud infrastructure of more than 100 datacenters.</span></span>

<span data-ttu-id="2342f-106">Als globale Organisation mit einem beträchtlichen Internetauftritt und vielen prominenten Interneteigenschaften, die Cloud-Dienste bereitstellen, ist Microsoft ein großes, gemeinsames Ziel für Hacker und andere böswillige Personen.</span><span class="sxs-lookup"><span data-stu-id="2342f-106">As a global organization with a significant Internet presence and many prominent Internet properties that provide cloud services, Microsoft is a large, common target for hackers and other malicious individuals.</span></span> <span data-ttu-id="2342f-107">Das Netzwerk – die Kommunikationsschicht zwischen Clients und der Microsoft-Cloud – ist eines der größten Ziele für böswillige Angriffe.</span><span class="sxs-lookup"><span data-stu-id="2342f-107">The network--the communication layer between clients and the Microsoft Cloud--is one of the biggest targets of malicious attacks.</span></span> <span data-ttu-id="2342f-108">Tatsächlich ist Microsoft seit vielen Jahren ständig und beharrlich unter einer Form netzwerkbasierter Cyberangriff.</span><span class="sxs-lookup"><span data-stu-id="2342f-108">In fact, for many years, Microsoft has been continuously and persistently under some form of network-based cyberattack.</span></span> <span data-ttu-id="2342f-109">Zu fast allen Zeiten hat mindestens eine der Internet Eigenschaften von Microsoft irgendeine Form von Angriffen.</span><span class="sxs-lookup"><span data-stu-id="2342f-109">At almost all times, at least one of Microsoft's Internet properties is experiencing some form of attack.</span></span> <span data-ttu-id="2342f-110">Ohne zuverlässige und beständige Schadensbegrenzende Systeme, die diese Angriffe abwehren können, wären die Cloud-Dienste von Microsoft Offline und nicht für Kunden verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2342f-110">Without reliable and persistent mitigation systems that can defend against these attacks, Microsoft's cloud services would be offline and unavailable to customers.</span></span>

<span data-ttu-id="2342f-111">Microsoft verwendet grundlegende Sicherheitsprinzipien zum Schutz seiner Cloud-Dienste und-Netzwerke.</span><span class="sxs-lookup"><span data-stu-id="2342f-111">Microsoft uses defense-in-depth security principles to protect its cloud services and networks.</span></span> 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a><span data-ttu-id="2342f-112">Definition und Symptome von Denial-of-Service-anGriffen</span><span class="sxs-lookup"><span data-stu-id="2342f-112">Definition and Symptoms of Denial-of-Service Attacks</span></span>
<span data-ttu-id="2342f-113">Eine Möglichkeit zum angreifen von Netzwerkdiensten besteht darin, viele Anforderungen an die Hosts eines Diensts zu stellen, um das Netzwerk und die Server zu überlasten, um den Dienst für legitime Benutzer zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="2342f-113">One way to attack network services is to create many requests against a service's hosts to overwhelm the network and servers to deny service to legitimate users.</span></span> <span data-ttu-id="2342f-114">Dies wird als Denial-of-Service-Angriff (DoS) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2342f-114">This is referred to as a denial-of-service (DoS) attack.</span></span> <span data-ttu-id="2342f-115">Wenn der Angriff von mehreren Aktoren, Endpunkten und/oder Vektoren ausgeführt wird, wird er als verteilten Denial-of-Service-Angriff (DDoS) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2342f-115">When the attack is performed by multiple actors, endpoints, and/or vectors, it is referred to as a distributed denial-of-service (DDoS) attack.</span></span> <span data-ttu-id="2342f-116">Obwohl die Mittel, Motive und Zielsetzungen unterschiedlich sind, bestehen DoS-und DDoS-Angriffe im Allgemeinen aus den Bemühungen einer Person oder Personen, um zu verhindern, dass eine Internet-Website oder ein Dienst ordnungsgemäß oder überhaupt, weder vorübergehend noch unbefristet, funktioniert.</span><span class="sxs-lookup"><span data-stu-id="2342f-116">Although the means, motives, and targets vary, DoS and DDoS attacks generally consist of the efforts of a person or persons to prevent an Internet site or service from functioning correctly or at all, either temporarily or indefinitely.</span></span>

<span data-ttu-id="2342f-117">Das [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) definiert die Symptome von DOS-Angriffen, die Folgendes umfasst:</span><span class="sxs-lookup"><span data-stu-id="2342f-117">The [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) defines symptoms of DoS attacks to include:</span></span>
- <span data-ttu-id="2342f-118">Ungewöhnlich langsame Netzwerkleistung (beim Öffnen von Dateien oder Zugriff auf Internet Websites)</span><span class="sxs-lookup"><span data-stu-id="2342f-118">Unusually slow network performance (when opening files or accessing Internet sites)</span></span>
- <span data-ttu-id="2342f-119">Nichtverfügbarkeit einer Website</span><span class="sxs-lookup"><span data-stu-id="2342f-119">Unavailability of a Web site</span></span>
- <span data-ttu-id="2342f-120">Zugriff auf eine Website nicht möglich</span><span class="sxs-lookup"><span data-stu-id="2342f-120">Inability to access a Web site</span></span>
- <span data-ttu-id="2342f-121">Drastischer Anstieg der empfangenen Spam-Mails</span><span class="sxs-lookup"><span data-stu-id="2342f-121">Dramatic increase in received spam</span></span>
- <span data-ttu-id="2342f-122">Trennen einer drahtlosen oder verkabelten Internet Verbindung</span><span class="sxs-lookup"><span data-stu-id="2342f-122">Disconnection of a wireless or wired Internet connection</span></span>
- <span data-ttu-id="2342f-123">Langfristiger Verlust des Zugriffs auf das Web oder irgendwelche Internet Dienste</span><span class="sxs-lookup"><span data-stu-id="2342f-123">Long-term loss of access to the Web or any Internet services</span></span>

## <a name="related-topics"></a><span data-ttu-id="2342f-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2342f-124">Related Topics</span></span>
- [<span data-ttu-id="2342f-125">Wichtige Grundsätze zum Schutz vor Denial-of-Service-Angriffen</span><span class="sxs-lookup"><span data-stu-id="2342f-125">Core Principles of Defense Against Denial-of-Service Attacks</span></span>](office-365-core-principles-of-defense-against-dos-attacks.md)
- [<span data-ttu-id="2342f-126">Denial-of-Service-VerteidigungsStrategie von Microsoft</span><span class="sxs-lookup"><span data-stu-id="2342f-126">Microsoft's Denial-of-Service Defense Strategy</span></span>](office-365-microsoft-dos-defense-strategy.md)
- [<span data-ttu-id="2342f-127">Schützen von Microsoft Cloud Services vor Denial-of-Service-anGriffen</span><span class="sxs-lookup"><span data-stu-id="2342f-127">Defending Microsoft Cloud Services Against Denial-of-Service Attacks</span></span>](office-365-defending-cloud-services-against-dos-attacks.md)
