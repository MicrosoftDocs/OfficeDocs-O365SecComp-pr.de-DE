---
title: Office 365 Überwachung und Testen von Mandanten Grenzen
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
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Zusammenfassung: eine Erläuterung dazu, wie Microsoft Mandanten Grenzen für Office 365 überwacht und testet.'
ms.openlocfilehash: 25b6f713d766b4b12e1c250b54421ad99dff8a1c
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090937"
---
# <a name="monitoring-and-testing-tenant-boundaries"></a>Überwachen und Testen von Mandantengrenzen
Microsoft überwacht und überprüft die Schwachstellen und Sicherheitsrisiken in Mandanten Grenzen kontinuierlich, einschließlich der Überwachung von Angriffen, Berechtigungs Verletzungen und Ressourcenknappheit. Wir verwenden auch mehrere interne Systeme, um die unangemessene Ressourcenauslastung kontinuierlich zu überwachen, was bei Erkennung die integrierte Drosselung auslöst.

Office 365 verfügt über interne Überwachungssysteme, die kontinuierlich auf Ausfälle überwachen und eine automatische Wiederherstellung steuern, wenn ein Defekt erkannt wird. Office 365-Systeme analysieren Abweichungen des Dienstverhaltens und initiieren selbst Heilungsprozesse, die in das System integriert sind. In Office 365 wird auch die Überwachung von außen verwendet, bei der die Überwachung von mehreren Standorten aus von vertrauenswürdigen Drittanbieterdiensten (für die unabhängige SLA-Überprüfung) und unsere eigenen Rechenzentren durchgeführt wird, um Warnungen zu erhöhen. Für Diagnosen haben wir umfangreiche Protokollierung, Überwachung und Ablaufverfolgung. Detaillierte Ablaufverfolgung und Überwachung helfen uns dabei, Probleme zu isolieren und eine schnelle und effektive Ursachenanalyse durchzuführen.

Während Office 365 über automatisierte Wiederherstellungsaktionen verfügt, stehen Microsoft-On-Call-Techniker rund um die Uhr zur Verfügung, um alle Sicherheits Eskalationen mit Schweregrad 1 zu untersuchen, und die nach Untersuchungsberichte zu jedem Dienst Vorfall tragen zu kontinuierlichem Lernen bei und Verbesserung. Dieses Team umfasst Supporttechniker, Produktentwickler, Programmmanager, Produktmanager und Führungskräfte. Unsere On-Call-Experten bieten eine rechtzeitige Sicherung und können häufig Wiederherstellungsaktionen automatisieren, sodass das nächste Mal, wenn ein Ereignis auftritt, selbst geheilt werden kann.

Microsoft führt eine gründliche Überprüfung nach dem Vorfall durch, wenn ein Office 365-Sicherheitsvorfall auftritt, unabhängig von der Größe der Auswirkungen. Eine Post-Incident-Überprüfung besteht aus einer Analyse, was passiert ist, wie wir reagiert haben und wie wir ähnliche Vorfälle in der Zukunft verhindern. Im Interesse der Transparenz und der Rechenschaftspflicht teilen wir die Post-Incident-Überprüfungen für wichtige Dienst Vorfälle mit betroffenen Kunden. Ausführliche Informationen finden Sie unter [Office 365 Security Incident Management](http://aka.ms/Office365SIM).

## <a name="assume-breach-methodology"></a>Annahme einer Verletzungs Methodik
Basierend auf einer detaillierten Analyse der Sicherheitstrends befürwortet und unterstreicht Microsoft die Notwendigkeit zusätzlicher Investitionen in reaktive Sicherheitsprozesse und-Technologien, die sich auf die Erkennung und Reaktion auf neue Bedrohungen konzentrieren, statt ausschließlich auf die Verhinderung von Bedrohungen. Aufgrund von Änderungen an der Bedrohungslandschaft und der eingehenden Analyse hat Microsoft seine Sicherheitsstrategie weiterentwickelt, um Sicherheitsverletzungen zu vermeiden, die für die Bewältigung von Verstößen besser gerüstet sind, wenn Sie auftreten – eine Strategie, die wichtige Sicherheitsereignisse nicht berücksichtigt. als eine Frage von if, but when.

Auch wenn die von Microsoft [angenommenEn Verstöße](https://www.microsoft.com/en-us/TrustCenter/Security/default.aspx) gegen die Vorgehensweisen bereits seit vielen Jahren gelten, wissen viele Kunden nicht, dass die Arbeit im Hintergrund ausgeführt wird, um die Microsoft-Cloud zu schützen. Nehmen Sie an, dass eine Verletzung eine Denkweise darstellt, die Sicherheitsinvestitionen, Entwurfsentscheidungen und betriebliche Sicherheitsmethoden führt. Gehen Sie davon aus, dass Verstöße die Vertrauensstellung in Anwendungen, Diensten, Identitäten und Netzwerken einschränken, indem Sie alle – interne und externe – als unsicher und bereits kompromittiert behandeln. Obwohl die Strategie zur Annahme von Verstößen nicht aus einer tatsächlichen Verletzung von Microsoft Enterprise-oder Cloud-Diensten stammt, wurde anerkannt, dass viele Organisationen in der gesamten Branche trotz aller Versuche, diese zu verhindern, verletzt wurden. Die Verhinderung von Verstößen ist zwar ein wichtiger Teil der Vorgänge einer Organisation, diese müssen jedoch kontinuierlich getestet und erweitert werden, um moderne Gegner und Fortgeschrittene Bedrohungen effektiv zu bewältigen. Damit sich eine Organisation auf eine Verletzung vorbereiten kann, müssen Sie zunächst stabile, wiederholbare und vollständig getestete Sicherheits Reaktionsverfahren erstellen und warten.

Während sicherheitsVerletzungen zu verhindern, wie beispielsweise Bedrohungsmodellierung, Codeüberprüfungen und Sicherheitstests, sind im Rahmen des [Sicherheits Entwicklungslebenszyklus](http://www.microsoft.com/security/sdl/default.aspx)sehr nützlich, über die Annahme, dass eine Verletzung zahlreiche Vorteile bietet, die der allgemeinen Sicherheit Rechnung tragen, indem ausüben und Messen von reaktiven Funktionen bei Verstößen.

Bei Microsoft haben wir uns bemüht, dies durch laufende Kriegsspiele Übungen und Live Site Penetrationstests für unsere Sicherheits Reaktionspläne zu erreichen, mit dem Ziel, unsere Erkennungs-und Reaktionsmöglichkeiten zu verbessern. Microsoft simuliert regelmäßige Verstöße gegen die Praxis, führt eine kontinuierliche Sicherheitsüberwachung durch und praktiziert das Sicherheitsvorfall-Management, um die Sicherheit von Office 365, Azure und anderen Microsoft Cloud-Diensten zu überprüfen und zu verbessern.

Microsoft führt die Sicherheitsstrategie für die übernehmen-Verletzung mit zwei Kerngruppen aus:
- Rote Teams (Angreifer)
- Blaue Teams (Verteidiger)

Sowohl Microsoft Azure als auch Office 365 Mitarbeiter trennen Vollzeit-rote Teams und blaue Teams.

Als "[rotes Teaming](http://go.microsoft.com/fwlink/?linkid=518599)" bezeichnet, besteht der Ansatz darin, Azure und Office 365-Systeme und-Vorgänge zu testen, die dieselben Taktiken, Techniken und Verfahren wie echte Gegner gegen die Live-Produktionsinfrastruktur verwenden, ohne die Vorwissen der Engineering-oder Operations Teams. Dadurch werden die Sicherheits Erkennungs-und-Antwortfunktionen von Microsoft getestet und Produktions Schwachstellen, Konfigurationsfehler, ungültige Annahmen und andere Sicherheitsprobleme auf kontrollierte Weise ermittelt. Jeder roten Team Verletzung folgt eine vollständige Offenlegung zwischen beiden Teams, um Lücken zu identifizieren, die Ergebnisse zu behandeln und die Gegenreaktion zu verbessern.

**Hinweis**: bei roten Teaming-oder Live-Website Penetrationstests werden keine Kundendaten absichtlich gezielt ausgerichtet. Die Tests sind gegen die Office 365-und Azure-Infrastruktur und-Plattformen sowie die eigenen Mandanten, Anwendungen und Daten von Microsoft. Kundenmandanten, Anwendungen und Inhalte, die in Office 365 oder Azure gehostet werden, werden nie gezielt.

## <a name="red-teams"></a>Rote Teams
Das rote Team ist eine Gruppe von Vollzeitmitarbeitern in Microsoft, die sich auf den Verstoß gegen die Infrastruktur, die Plattform von Microsoft und die eigenen Mandanten und Anwendungen von Microsoft konzentriert. Sie sind der dedizierte Widersacher (eine Gruppe ethischer Hacker), der gezielte und beständige Angriffe auf Online Dienste (Microsoft-Infrastruktur, Plattformen und Anwendungen, aber keine Anwendungen oder Inhalte von Endkunden) durchführt.

Die Rolle des roten Teams besteht in der Angriffs-und Durchdringungs Umgebung mit den gleichen Schritten wie bei einem Gegner:
 
![Bruch Stufen](media/office-365-isolation-breach-stages.png)

Unter anderem versuchen rote Teams, Mandanten Isolations Grenzen zu verletzen, um Fehler oder Lücken in unserem Isolierungs Design zu finden.

## <a name="blue-teams"></a>Blaue Teams
Das blaue Team besteht aus einer dedizierten Gruppe von Sicherheits Respondern oder Mitgliedern aus der gesamten Sicherheitsvorfall-Reaktions-, Engineering-und Betriebsorganisation. Unabhängig von Ihrem Make-up sind Sie unabhängig und arbeiten getrennt vom roten Team. Das blaue Team folgt auf bewährte Sicherheitsprozesse und verwendet die neuesten Tools und Technologien, um Angriffe und Durchdringung zu finden und darauf zu reagieren. Genau wie bei realen Angriffen weiß das Team Blue nicht, wann oder wie die Angriffe des roten Teams auftreten oder welche Methoden verwendet werden können. Ihre Aufgabe besteht darin, ob es sich um einen roten Team Angriff oder um einen tatsächlichen Angriff handelt, um alle Sicherheitsvorfälle zu erfassen und darauf zu reagieren. Aus diesem Grund ist das blaue Team kontinuierlich On-Call und muss auf Verstöße bei roten Teams auf die gleiche Weise reagieren wie bei anderen Verstößen.

Wenn ein Gegner, wie beispielsweise ein rotes Team, eine Umgebung verletzt hat, muss das blaue Team:
- Sammeln von nachweisen, die der Widersacher hinterlassen hat
- Erkennen des Beweises als Anhaltspunkt für eine Gefährdung
- Benachrichtigen der entsprechenden Entwicklungs-und Operations Teams
- Selektieren der Warnungen, um zu bestimmen, ob Sie weitere Untersuchungen rechtfertigen
- Kontext aus der Umgebung sammeln, um den Verstoß zu übertreffen
- Bilden Sie einen Sanierungsplan, um den Gegner zu enthalten oder zu entfernen.
- Ausführen des Behebungs Plans und Wiederherstellung nach Verstößen

Diese Schritte bilden die Sicherheitsvorfall Antwort, die parallel zum Widersacher ausgeführt wird (siehe unten):
 
![Antwort Phasen für Verstöße](media/office-365-isolation-breach-response-stages.png)

Verstöße gegen rote Teams ermöglichen die Ausübung der Fähigkeit des blauen Teams, reale Angriffe durchgängig zu erfassen und darauf zu reagieren. Am wichtigsten ist, dass die Anwendung geübter Sicherheitsvorfälle vor einer echten Verletzung zulässt. Aufgrund von roten Team Verstößen erhöht das blaue Team außerdem Ihr Situationsbewusstsein, das beim Umgang mit zukünftigen Verstößen (vom roten Team oder einem anderen Gegner) wertvoll sein kann. Während des Erkennungs-und Reaktionsprozesses produziert das blaue Team eine umsetzbare Intelligenz und erhält einen Einblick in die tatsächlichen Bedingungen der Umgebung (en), die Sie verteidigen möchten. Häufig geschieht dies über Datenanalyse und Forensik, die vom blauen Team ausgeführt werden, wenn Sie auf Angriffe durch rote Teams reagieren und Bedrohungs Indikatoren wie Indikatoren für Kompromisse einrichten. Ähnlich wie das rote Team Lücken in der Sicherheitsgeschichte identifiziert, identifizieren blaue Teams Lücken in ihrer Fähigkeit, zu erkennen und zu reagieren. Außerdem kann das blaue Team, da die roten Teams reale Angriffe modellieren, präzise auf ihre Fähigkeit oder Unfähigkeit hin beurteilt werden, um mit bestimmten und hartnäckigen Gegnern umzugehen. Schließlich messen die Verstöße bei roten Teams sowohl die Bereitschaft als auch die Auswirkungen unserer Gegenmaßnahmen.
