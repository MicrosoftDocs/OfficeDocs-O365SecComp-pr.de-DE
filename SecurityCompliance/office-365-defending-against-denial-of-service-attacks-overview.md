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
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a>Schutz vor Denial-of-Service-anGriffen in Office 365

## <a name="introduction"></a>Einführung
Microsoft bietet eine vertrauenswürdige Infrastruktur für mehr als 200 Cloud-Dienste, einschließlich Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype und Xbox Live, die in unserer globalen Cloud gehostet werden. Infrastruktur von mehr als 100 Rechenzentren.

Als globale Organisation mit einem beträchtlichen Internetauftritt und vielen prominenten Interneteigenschaften, die Cloud-Dienste bereitstellen, ist Microsoft ein großes, gemeinsames Ziel für Hacker und andere böswillige Personen. Das Netzwerk – die Kommunikationsschicht zwischen Clients und der Microsoft-Cloud – ist eines der größten Ziele für böswillige Angriffe. Tatsächlich ist Microsoft seit vielen Jahren ständig und beharrlich unter einer Form netzwerkbasierter Cyberangriff. Zu fast allen Zeiten hat mindestens eine der Internet Eigenschaften von Microsoft irgendeine Form von Angriffen. Ohne zuverlässige und beständige Schadensbegrenzende Systeme, die diese Angriffe abwehren können, wären die Cloud-Dienste von Microsoft Offline und nicht für Kunden verfügbar.

Microsoft verwendet grundlegende Sicherheitsprinzipien zum Schutz seiner Cloud-Dienste und-Netzwerke. 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a>Definition und Symptome von Denial-of-Service-anGriffen
Eine Möglichkeit zum angreifen von Netzwerkdiensten besteht darin, viele Anforderungen an die Hosts eines Diensts zu stellen, um das Netzwerk und die Server zu überlasten, um den Dienst für legitime Benutzer zu verweigern. Dies wird als Denial-of-Service-Angriff (DoS) bezeichnet. Wenn der Angriff von mehreren Aktoren, Endpunkten und/oder Vektoren ausgeführt wird, wird er als verteilten Denial-of-Service-Angriff (DDoS) bezeichnet. Obwohl die Mittel, Motive und Zielsetzungen unterschiedlich sind, bestehen DoS-und DDoS-Angriffe im Allgemeinen aus den Bemühungen einer Person oder Personen, um zu verhindern, dass eine Internet-Website oder ein Dienst ordnungsgemäß oder überhaupt, weder vorübergehend noch unbefristet, funktioniert.

Das [United States Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) definiert die Symptome von DOS-Angriffen, die Folgendes umfasst:
- Ungewöhnlich langsame Netzwerkleistung (beim Öffnen von Dateien oder Zugriff auf Internet Websites)
- Nichtverfügbarkeit einer Website
- Zugriff auf eine Website nicht möglich
- Drastischer Anstieg der empfangenen Spam-Mails
- Trennen einer drahtlosen oder verkabelten Internet Verbindung
- Langfristiger Verlust des Zugriffs auf das Web oder irgendwelche Internet Dienste

## <a name="related-topics"></a>Verwandte Themen
- [Wichtige Grundsätze zum Schutz vor Denial-of-Service-Angriffen](office-365-core-principles-of-defense-against-dos-attacks.md)
- [Denial-of-Service-VerteidigungsStrategie von Microsoft](office-365-microsoft-dos-defense-strategy.md)
- [Schützen von Microsoft Cloud Services vor Denial-of-Service-anGriffen](office-365-defending-cloud-services-against-dos-attacks.md)
