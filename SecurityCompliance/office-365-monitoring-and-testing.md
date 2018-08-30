---
title: Office 365 überwachen und Testen von Mandanten Grenzen
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
description: 'Zusammenfassung: Erläutert, wie Microsoft überwacht und Tests Mandanten Grenzen für Office 365.'
ms.openlocfilehash: 4d57c7497bfe8bf9939f3ae785ab9fbc670bd0ae
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529185"
---
# <a name="monitoring-and-testing-tenant-boundaries"></a>Überwachen und Testen von Mandanten Grenzen
Microsoft fortlaufend überwacht und explizit Sicherheitslücken und Sicherheitslücken im Mandanten Grenzen, einschließlich der Überwachung für Intrusion, Berechtigung Verletzung Versuche und Blockieren von Ressourcen überprüft. Wir können auch mehrere interne Systeme überwachen kontinuierlich von ungeeignetes Ressourcenverwendung, das wenn erkannt, integrierten Drosselung auslöst.

Office 365 verfügt über interne Überwachung Systeme, die kontinuierlich für alle Fehler überwachen und Laufwerk automatisierte Wiederherstellung, wenn Fehler erkannt wird. Office 365-Systeme Abweichung Service Verhalten zu analysieren und initiieren korrigierten Prozesse, die in das System integriert sind. Office 365 verwendet auch außen Überwachung in der Überwachung von beide mehrere Standorte aus vertrauenswürdigen Drittanbieter-Dienste (für die Prüfung der unabhängigen SLA) und unsere eigenen Rechenzentren Benachrichtigungen auslösen ausgeführt wird. Für die Diagnose haben wir umfassende Protokollierung, Überwachung und Protokollierung. Führen Analysis differenzierte verfolgen und Überwachen der hilft uns Isolieren von Problemen und schnelle und effektive Root ausführen.

Während der Office 365-Wiederherstellungsaktionen automatisierte hat, sofern möglich, Microsoft auf Abruf Ingenieure sind verfügbar 24 x 7 alle Schweregrad 1 Sicherheit Eskalationen untersuchen und postmortalen prüft der trägt jeder Dienst Vorfall zur kontinuierlichen Learning und zur Verbesserung der. Dieses Team enthält Supporttechniker, Produktentwickler, Programm-Manager, Produktmanager und senior führende. Unsere auf Abruf Professionals stellen eine Reserve für rechtzeitige und häufig können Wiederherstellungsaktionen, automatisieren, so dass beim nächsten ein Ereignis eintritt, es selbst vernarbte sein kann.

Microsoft führt eine sorgfältige nach dem Vorfall Überprüfung jedes Mal, wenn ein Office 365 Sicherheitsvorfall unabhängig davon das Ausmaß der Auswirkung stattfindet. Nach dem Vorfalls umfasst eine Analyse der Änderungen bei der, wie wir reagiert und wie wir ähnliche Vorfällen in der Zukunft zu verhindern. Im Interesse der Transparenz und Accountability freigeben wir nach dem des Vorfalls für alle wichtigen Dienstereignisse betroffenen Kunden. Einzelheiten hierzu finden Sie unter [Office 365 Vorfall Sicherheitsverwaltung](http://aka.ms/Office365SIM).

## <a name="assume-breach-methodology"></a>Verletzung Methodik annehmen
Basierend auf detaillierte Analyse der Trends, Sicherheit, Microsoft ist und die Notwendigkeit für zusätzliche Investitionen in reaktive Sicherheitsprozesse und Technologien, die auf die Erkennung von und Reaktion auf neue Bedrohungen, statt dass ausschließlich die Vermeidung von konzentrieren hervorgehoben die Risiken. Aufgrund von Änderungen im Querformat Bedrohung und eingehenderen Analysen eingeschränkt Microsoft seine Sicherheitsstrategie nur verhindern Sicherheitslücken auf eine besser ausgestattet Umgang mit Verstößen, wenn sie treten – eine Strategie für die hält Haupt-Sicherheitsereignisse nicht Grundsätzlich If, aber bei.

Microsofts [Wird davon ausgegangen Verletzung](https://www.microsoft.com/en-us/TrustCenter/Security/default.aspx) Methoden direkten seit vielen Jahren wurden, sind viele Kunden erkennt die Arbeit im Hintergrund verstärken der Sicherheit von Microsoft-Cloud. Wird davon ausgegangen Sie, dass eine Einstellung, die Investitionen in Sicherheit, Designentscheidungen und betriebsbereit Sicherheitsmaßnahmen führt ist. Verletzung Grenzwerte für die Vertrauensstellung in platziert Anwendungen, Dienste, Identitäten und Netzwerke behandelt werden alle angenommen – interne und externe – wie unsichere und bereits beschädigte. Obwohl die Strategie Verletzung wird vorausgesetzt aus einer Verletzung tatsächlichen aller Microsoft Enterprise oder in der Cloud-Dienste nicht übernommen wurde, gab es eine identifizierter, dass viele Organisationen trotz alle Versuche, damit es nicht in der Branche verletzt worden waren. Verhindern Verstöße ist ein wichtiger Bestandteil des Unternehmens Vorgänge diese Methoden müssen fortlaufend getestet und erweitert, um effektiv modernen Angreifer beheben und erweiterte persistent Bedrohungen. Für jede Organisation zur Vorbereitung einer Verletzung müssen sie zuerst erstellen und Verwalten von robuste, wiederholbare und sorgfältig getestet Antwort Sicherheitsverfahren.

Während Verletzung zu verhindern, dass Sicherheitsprozesse, wie das Erstellen von Bedrohungsmodellen Reviews (engl. Code), und Testen der Sicherheit sind sehr nützlich als Teil des [Security Development Lifecycle](http://www.microsoft.com/security/sdl/default.aspx)Verletzung wird davon ausgegangen bietet zahlreiche Vorteile, mit deren Hilfe-Konto zur allgemeinen Sicherheit durch ausüben und reaktive Funktionen im Falle einer Verletzung messen.

Bei Microsoft legen wir Out dazu über laufende war-games Übungen und Livewebsite Eindringversuche für unsere Security Response-Pläne mit dem Ziel, unseren Erkennung und Antwort-Funktion zu verbessern. Microsoft regelmäßig Praxis Verstöße simuliert, kontinuierliche Sicherheit Überwachung und Methoden Sicherheit Vorfälle überprüfen und erhöhen Sie die Sicherheit von Office 365, Azure und andere Microsoft-Cloud-Dienste tätig.

Microsoft führt die Verwendung von zwei Gruppen von Core Verletzung wird davon ausgegangen Sicherheitsstrategie aus:
- Red-Teams (Angreifer)
- Blue-Teams (Verteidiger)

Microsoft Azure und Office 365 Personal Vollzeitmitarbeiter in Rot Teams und Blau Teams zu trennen.

Als "[Rot Teaming](http://go.microsoft.com/fwlink/?linkid=518599)" bezeichnet, der Ansatz besteht darin, Testen von Azure und Office 365-Systeme und Vorgänge unter Verwendung von Taktiken, Methoden und Verfahren als real Angreifer, gegen die Produktion-Infrastruktur, ohne die Vorkenntnisse über die Engineering oder Betriebsteams. Auf diese Weise Testen des Microsoft Security erkannt und Antwort-Funktionen und hilft feststellen Produktion Sicherheitsrisiken, Konfigurationsfehler, ungültige Annahmen und andere Sicherheitsprobleme kontrolliert. Jede rot Team Verletzung folgt vollständige Offenlegung zwischen den beiden Teams zu Lücken identifizieren und beheben Ergebnisse verbessern Verletzung Antwort.

**Hinweis**: keine Kundendaten zielt absichtlich während Rot Teaming oder Livewebsite Durchdringungstests. Die Tests sind vor Office 365 und Azure-Infrastruktur und -Plattformen als auch von Microsoft Mandanten, Anwendungen und Daten. Kunden-Mandanten, Anwendungen und Inhalte in Office 365 oder Azure gehostet werden nie geplant.

## <a name="red-teams"></a>Rote Teams
Das rote Team ist eine Gruppe von Vollzeit-Mitarbeiter innerhalb von Microsoft, die der Schwerpunkt auf Verstöße gegen Microsoft-Infrastruktur, Plattform und des Microsoft-Mandanten und Anwendungen liegt. Sie sind der dedizierten Angreifer (eine Gruppe von ethische Hacker) zielgerichteten und beständigen Angriffe auf Online-Dienste (Microsoft-Infrastruktur, Plattformen und Applikationen jedoch nicht End-Kunden Applications oder Inhalte) ausführen.

Die Rolle des Teams Rot ist an treibt die gleichen Schritte unter Umgebungen zugelassen und Angriffe auf:
 
![Verletzung Phasen](media/office-365-isolation-breach-stages.png)

Neben anderen Funktionen Versuch Rot Teams speziell verletzen Mandanten Isolation Grenzen um Bugs oder Lücken in unseren Isolation Design zu suchen.

## <a name="blue-teams"></a>Blue-Teams
Das blaue Team besteht aus einem speziellen Satz von Sicherheit Respondern oder Mitglieder aus über die Sicherheitsstrategie, Engineering und Vorgänge Organisationen. Unabhängig von ihrer schließen ein unabhängiger sind und funktionieren separat von der rote Team. Die blaue Team folgt hergestellt Sicherheit verarbeitet und die neuesten Tools und -Technologien zu erkennen und reagieren auf Angriffe und Durchdringungstests verwendet. Genau wie Praxis-Angriffen ist das blaue Team nicht bekannt, wann oder wie das rote Team Angriffe stattfindet oder welche Methoden verwendet werden können. Ihre Arbeit ist, ob es sich um einen Angriff Rot Team oder eine tatsächliche Angriffs, ist die Erkennung von und Reaktion auf alle sicherheitsrelevanten Ereignisse. Aus diesem Grund das blaue Team kontinuierlich Anruf und muss die gleiche Weise, wie sie bei einer anderen Verletzung würde für Rot Team Verstöße reagieren.

Wenn treibt wie ein rotes Team, eine Umgebung verletzt hat, müssen das blaue Team:
- Sammeln von links von der Angreifer Nachweis
- Erkennen des Beweis als Angabe der Gefährdung
- Warnung der entsprechenden Engineering und einen optimalen Betrieb Teams
- Untersuchen Sie die Alarme, um festzustellen, ob sie weitere Untersuchung gerechtfertigt ist
- Sammeln von Kontext aus der Umgebung aus, um die Verletzung Bereich
- Bilden eines Plans zur Anwendungswartung enthalten, oder erzwingen Ihrer Zurücksetzung der Angreifer
- Ausführen des Plans für die Wartung und Wiederherstellen von Verletzungen

Diese Schritte bilden die Sicherheitsstrategie, die parallel zu den Angreifer wie folgt ausgeführt wird:
 
![Verletzung Antwortphasen](media/office-365-isolation-breach-response-stages.png)

Wahrnehmung der des Teams von blue-Funktion zum Erkennen und reagieren auf Praxis Angriffe End-to-End ermöglichen Rot Team Verstöße. Der wichtigste ermöglicht es geübt Sicherheitsstrategie vor eine echte Verletzung. Darüber hinaus verbessert das blaue Team aufgrund von roten Team Verstöße, ihre Situation, der beim Umgang mit verwiesen (, ob von der rote Team oder eine andere Angreifer) hilfreich sein kann. In der Erkennung und Antworten auf Besprechungsanfragen das blaue Team bearbeitungsfähige Intelligence erzeugt und erhält Einblick in die tatsächlichen Formatierungen der Umwelt(en), die sie schützen möchten. Häufig erfolgt dies über Datenanalyse und Analysen, die beim Aufruf von Rot Team Angriffen sowie durch Bedrohung Indikatoren, wie Indikatoren für Kompromiss reagiert Blau Teams, ausgeführt. Viel wie wie das rote Team Lücken im Abschnitt Sicherheit identifiziert, identifizieren Sie Blau Teams Lücken in ihrer Fähigkeit zum Erkennen und reagieren. Da die rote Teams Praxis Angriffe modellieren, kann darüber hinaus das blaue Team genau auf Möglichkeit oder nicht, für den Umgang mit bestimmt und beständigen Angreifer bewertet. Schließlich messen Rot Team Verstöße Bereitschafts- und Auswirkung von unseren Verletzung Antwort.
