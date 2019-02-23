---
title: Office 365 Internal Logging für Office 365 Engineering
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Eine Erläuterung der Funktionsweise der internen Protokollierung für Office 365-Entwicklungsteams.
ms.openlocfilehash: 68f8763b9a647de462f402e40a4c78749343dfd9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216495"
---
# <a name="internal-logging-for-office-365-engineering"></a>Interne Protokollierung für Office 365 Engineering
Zusätzlich zu den für Kunden verfügbaren Ereignissen und Protokolldaten gibt es auch ein internes Protokoll Datenerfassungssystem, das Office 365-Ingenieuren zur Verfügung steht. Viele verschiedene Typen von Protokolldaten werden von Office 365-Servern auf einen internen, großen Datenverarbeitungsdienst namens Cosmos hochgeladen. Jedes Dienst Team lädt Überwachungsprotokolle von ihren jeweiligen Servern in die Cosmos-Datenbank für Aggregation und Analyse hoch. Diese Datenübertragung erfolgt über eine FIPS 140-2-validierte TLS-Verbindung auf speziell genehmigten Ports und Protokollen mithilfe eines proprietären Automatisierungstools namens Office Data Loader (ODL). Die Tools, die in Office 365 zum Erfassen und Verarbeiten von Überwachungsdatensätzen verwendet werden, lassen keine dauerhaften oder irreversiblen Änderungen am ursprünglichen Inhalt oder der Zeitreihen Folge des Überwachungsdatensatzes zu.

Service Teams verwenden Cosmos als zentrales Repository, um eine Analyse der Anwendungsnutzung durchzuführen, die System-und Betriebsleistung zu messen und nach Anomalien und Mustern zu suchen, die auf Probleme oder Sicherheitsprobleme hindeuten können. Jedes Dienst Team lädt eine Basis von Protokollen in Cosmos hoch, je nachdem, was Sie analysieren möchten, und zwar oft:
- Ereignisprotokolle
- AppLocker-Protokolle
- Leistungsdaten
- System Center-Daten
- Anruf Detaildatensätze
- Quality of Experience-Daten
- IIS-Webserverprotokolle
- SQL Server-Protokolle
- Syslog-Daten
- Sicherheitsüberwachungsprotokolle

Vor dem Hochladen von Daten in Cosmos verwendet die ODL-Anwendung einen Scrubbing-Dienst, um alle Felder zu verbergen, die Kundendaten wie Mandanteninformationen und Endbenutzer identifizierbare Informationen enthalten, und diese Felder durch einen Hashwert zu ersetzen. Die anonymisierten und gehashten Protokolle werden umgeschrieben und dann in Cosmos hochgeladen. Dienst Teams führen bereichsbezogene Abfragen mit Ihren Daten in Cosmos aus, um Korrelationen, Warnungen und Berichte zu erhalten. Der Zeitraum der Aufbewahrungszeit für Überwachungsprotokolle in Cosmos wird von den Service Teams bestimmt. die meisten Überwachungsprotokolldaten werden 90 Tage lang aufbewahrt, um Sicherheitsverletzungen zu unterstützen und die gesetzlichen Aufbewahrungsanforderungen zu erfüllen.

Der Zugriff auf Office 365-Daten, die in Cosmos gespeichert sind, ist auf autorisierte Mitarbeiter beschränkt. Microsoft schränkt die Verwaltung der Überwachungsfunktionalität auf die eingeschränkte Teilmenge der Dienst Teammitglieder ein, die für die Überwachungsfunktionalität zuständig sind. Diese Teammitglieder haben nicht die Möglichkeit, Daten aus Cosmos zu ändern oder zu löschen, und alle Änderungen an den Protokollierungsmechanismen für Cosmos werden aufgezeichnet und überwacht.

Jedes Dienst Team greift zur Analyse auf seine Protokolldaten zu, indem bestimmte Anwendungen autorisiert werden, bestimmte Analysen durchzuführen. Beispielsweise verwendet das Office 365-Sicherheitsteam Daten aus Cosmos über einen proprietären Ereignisprotokoll Parser, um Berichte über mögliche verdächtige Aktivitäten in der Office 365-Produktionsumgebung zu korrelieren, zu benachrichtigen und zu generieren. Die Berichte aus diesen Daten werden verwendet, um Sicherheitsrisiken zu beheben und die Gesamtleistung des Diensts zu verbessern. Wenn für eine bestimmte Warnung oder einen Bericht weitere Untersuchungen erforderlich sind, kann das Servicepersonal anfordern, dass Daten wieder in den Office 365-Dienst importiert werden. Da das spezifische Protokoll, das aus Cosmos importiert wird, verschlüsselt ist und das Dienstpersonal keinen Zugriff auf Entschlüsselungsschlüssel hat, wird das Zielprotokoll programmgesteuert über einen Entschlüsselungs Dienst weitergeleitet, der bereichsbezogene Ergebnisse an das autorisierte Servicepersonal zurückgibt. Alle Sicherheitsanfälligkeiten aus dieser Übung werden mithilfe der standardmäßigen Verwaltungs Kanäle für Sicherheitsvorfälle von Microsoft gemeldet und eskaliert.
