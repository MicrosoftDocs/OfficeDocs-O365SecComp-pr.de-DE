---
title: Schutz vor Denial-of-Service-anGriffen in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Übersicht über Denial-of-Service-Angriffe (DoS).
ms.openlocfilehash: 246704bff18c07d9b76281ae3c7071cd0d747630
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220505"
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
