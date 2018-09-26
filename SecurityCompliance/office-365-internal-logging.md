---
title: Office 365 interne Protokollierung für Office 365-Entwicklung
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Eine Erläuterung der wie interne Protokollierung für Office 365 Engineering teams funktioniert.
ms.openlocfilehash: 4cade759fb4c095565b4e1f85ce15ed546177082
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038188"
---
# <a name="internal-logging-for-office-365-engineering"></a>Interne Protokollierung für Office 365 Engineering
Zusätzlich zu den Ereignissen und die Protokolldaten für Kunden zur Verfügung ist auch ein interner Datenerfassung, die für Mitarbeiter des Office 365 verfügbar ist. Viele verschiedene Typen von Protokolldaten werden von Office 365-Servern in einer internen, big Daten computing-Dienst namens Cosmos hochgeladen. Jedes Team Service hochgeladen Überwachungsprotokolle aus den jeweiligen Server in die Datenbank Cosmos für Aggregation und Analysen. Diese Datenübertragung erfolgt über eine FIPS 140-2-validiert TLS-Verbindung speziell genehmigte Ports und Protokolle, die mithilfe des Tools proprietäre Automation Office Daten Loader (ODL). Die Tools, die zum Sammeln von in Office 365 verwendet und Überwachungseinträge Prozess nicht permanente zulassen oder nicht rückgängig gemacht werden Änderungen an den ursprünglichen Datensatz Inhalts- oder Zeit Sortierung überwachen.

Service-Teams verwenden Cosmos als zentrales Repository, um eine Analyse der Anwendungsverwendung, bis auf System und betrieblichen messen und suchen Sie nach Mängel und Muster, die Sicherheit Probleme hindeuten durchführen. Jedes Team Service uploads Grundlinie der Protokolle in Cosmos, je nach zur Analyse gewünschter, die häufig enthalten:
- Ereignisprotokolle
- AppLocker-Protokolle
- Leistungsdaten
- System Center-Daten
- Call Detail Records
- Daten Quality of experience
- IIS-Webserver-Protokolle
- SQL Server-Protokolle
- Syslog-Daten
- Sicherheit von Überwachungsprotokollen

Vor dem Hochladen von Daten in Cosmos, wird die ODL-Anwendung ein scrubbing Service verschleiern alle Felder, die Kundendaten, wie etwa Mandanten und Endbenutzer identifizierbare Informationen enthalten, und ersetzen diese Felder mit einem Hashwert verwendet. Die anonymes und Hash-Protokolle sind umgeschrieben und klicken Sie dann in Cosmos hochgeladen werden. Service-Teams ausführen Bereichsbezogene Abfragen ihre Daten in Cosmos für die Korrelation, warnen und Bericht. Die Dauer der Beibehaltung des Änderungsprotokolls Daten Audit in Cosmos ist von den Serviceteams festgestellt wird. Die meisten Überwachungsprotokolldaten werden für 90 Tage oder mehr Sicherheit Vorfall Untersuchungen unterstützen und gesetzlichen Aufbewahrung Anforderungen erfüllt beibehalten.

Zugriff auf Office 365 in Cosmos gespeicherten Daten ist auf autorisierte Personen beschränkt. Microsoft beschränkt die Verwaltung von Überwachungsfunktionen auf der begrenzten Anzahl Service-Teammitglieder, die Audit-Funktionen, die verantwortlich sind. Diese Teammitglieder müssen keinen die Möglichkeit zum Ändern oder Löschen von Daten aus Cosmos, und alle Änderungen an Protokollierungsmechanismen für Cosmos aufgezeichnet und überwacht werden.

Jedes Team Dienst greift auf die Protokolldaten für die Analyse durch autorisieren bestimmte Anwendungen, um bestimmte Analysen durchzuführen. Beispielsweise verwendet das Sicherheit in Office 365-Team Daten aus Cosmos über eine proprietäre Ereignisprotokoll-Parser zum Korrelieren, Benachrichtigung und bearbeitungsfähige Berichte auf mögliche verdächtige Aktivitäten in der Office 365-produktionsumgebung. Die Berichte über diese Daten dienen zur Behebung von Sicherheitsrisiken und zur Verbesserung der allgemeinen Leistung des Diensts. Wenn eine bestimmte benachrichtigungs- oder einen weiteren Untersuchung erforderlich sind, können Servicemitarbeiter anfordern Daten wieder in Office 365-Dienst importiert werden. Seit das spezifische Protokoll von Cosmos importiert wird ist verschlüsselt und Service-Mitarbeiter haben keinen Zugriff auf Entschlüsselungsschlüssel, das Zielprotokoll wird programmgesteuert über ein Entschlüsselung-Dienst, der bewertete Ergebnisse zurückgibt, die an die Mitarbeiter autorisierten Service übergeben. Aus dieser Übung gefundenen Sicherheitslücken gemeldet und mithilfe des Microsoft Security standard Problemmanagement Kanäle weitergeleitet werden.
