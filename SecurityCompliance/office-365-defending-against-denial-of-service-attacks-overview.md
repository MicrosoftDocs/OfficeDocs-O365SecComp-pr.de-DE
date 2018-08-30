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
# <a name="defending-against-denial-of-service-attacks-in-office-365"></a>Schutz vor Denial-of-Service-Angriffen in Office 365

## <a name="introduction"></a>Einführung
Microsoft bietet eine trustworthy Infrastruktur für mehr als 200 Cloud-Dienste, einschließlich Microsoft Azure, Microsoft Bing, Microsoft Office 365, Microsoft Dynamics 365, Microsoft OneDrive, Skype und Xbox Live, die in unserer globalen Cloud gehostet werden Infrastruktur von mehr als 100 Rechenzentren.

Als globale Organisation eine erhebliche Internetauftritt und viele wichtigsten Internet-Eigenschaften, die Clouddienste bereitstellen, ist Microsoft eine große, allgemeine Ziel für Hacker und andere böswilligen Personen. Die Netzwerk - Schicht für die Kommunikation zwischen Clients und der Microsoft-Cloud – ist der größten Zielgruppen vor böswilligen Angriffen. Tatsächlich seit vielen Jahren wurde Microsoft fortlaufend und dauerhaft unter einer Form von Netzwerk-basierte berichtet. In fast allen Fällen ist mindestens eine der Eigenschaften von Microsoft Internet eines Angriffs aufgetreten. Ohne zuverlässigen und beständigen Risikominderung-Systemen, die Verteidigung gegen diese Angriffe können, wäre Microsofts Cloud-Dienste offline und Kunden nicht verfügbar.

Microsoft verwendet Verteidigung Sicherheitsprinzipien, um dessen Clouddiensten und Netzwerke schützen. 

## <a name="definition-and-symptoms-of-denial-of-service-attacks"></a>Definition und Symptome von Denial-of-Service-Angriffen
Eine Möglichkeit, Angriffe auf Netzwerkdienste ist die Erstellung viele Anforderungen anhand eines Diensts Hosts zu überlasten Netzwerk und Servern Dienst für legitime Benutzer abgelehnt werden sollen. Dies wird als Denial-of-Service-Angriff (DoS) bezeichnet. Wenn der Angriff durch mehrere Akteure, Endpunkte und/oder Vektoren ausgeführt wird, wird es als einer verteilten Denial-of-Service-Angriff (DDoS) bezeichnet. Obwohl die Möglichkeit, Motive und Ziele variieren, bestehen DoS und DDoS-Angriffen in der Regel die Arbeit von Personen oder einer Person, um eine Internet-Website oder ein Dienst nicht ordnungsgemäß funktioniert oder überhaupt, vorübergehend oder auf unbestimmte Zeit zu verhindern.

[Vereinigte Staaten Computer Emergency Readiness Team](https://www.us-cert.gov/) (US-CERT) definiert Symptome von DoS-Angriffen enthalten:
- Ungewöhnlich langsame netzwerkleistung (beim Öffnen von Dateien oder den Zugriff auf Internet-Sites)
- Ausfall einer Website
- Fehler beim Zugriff auf eine Website
- Erhebliche Steigerung empfangener spam
- Trennen der Verbindung über eine drahtlose oder drahtgebundene Verbindung zum Internet
- Langfristige Verlust des Zugriffs auf die Web- oder alle Internetdienste

## <a name="related-topics"></a>Verwandte Themen
- [Wesentliche Prinzipien Schutz vor Denial-of-Service-Angriffen](office-365-core-principles-of-defense-against-dos-attacks.md)
- [Microsoft Defense Denial-of-Service-Strategie](office-365-microsoft-dos-defense-strategy.md)
- [Verteidigen Microsoft Cloud-Dienste vor Denial-of-Service-Angriffen](office-365-defending-cloud-services-against-dos-attacks.md)
