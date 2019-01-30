---
title: Arbeiten mit der Kommunikation in erweiterten eDiscovery (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: b27d6cca0382b18123cae4106f77ce0dcdf5e525
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607839"
---
# <a name="working-with-communications-in-advanced-ediscovery-preview"></a>Arbeiten mit der Kommunikation in erweiterten eDiscovery (Preview)

Erweiterte eDiscovery (Preview) ermöglicht rechtliche Abteilungen, um ihre Prozesse um nachverfolgen und Verteilen von rechtliche Aufbewahrungspflicht Benachrichtigungen zu vereinfachen. Die Verwaltungsberechtigter Communications-Funktion ermöglicht rechtliche Abteilungen verwalten und ihre gesamte rechtliche Aufbewahrungspflicht Prozesse – von Benachrichtigungen und Erinnerungen Eskalationen – alle an einem Ort zu automatisieren.

## <a name="what-is-a-legal-hold-notification"></a>Was ist eine Benachrichtigung über eine rechtliche Aufbewahrungspflicht?

Eine Anmerkung zur rechtlichen Aufbewahrungspflicht (auch bekannt als eine *Aufbewahrung für eventuelle halten*) wird eine Benachrichtigung an Mitarbeiter, Zeitarbeiter oder andere Verwalter von Daten aus einer Organisation rechtsabteilung gesendet. Diese Benachrichtigungen weisen Verwalter beibehalten auf elektronischem Wege gespeicherte Informationen (ESI) als auch Material, die für eine aktive oder anstehender Rechtsangelegenheiten relevant sein können. Rechtliche Teams müssen wissen, dass jede Verwaltungsberechtigter empfangen, lesen, und verstanden und vereinbart haben, die bestimmten Anweisungen entsprechen.

## <a name="the-legal-hold-notification-process"></a>Halten Sie die Legal Benachrichtigungsprozess

Eine Organisation verfügt über eine Abgabe relevanten Informationen beibehalten, wenn es über eine bevorstehende Rechtsstreitigkeiten oder behördlichen Untersuchung lernen. Um den permanentes Anforderungen zu erfüllen, sollte die Organisation potenzielle Verwalter zu deren Abgabe relevanten Informationen zu erhalten unverzüglich. 

Mit erweiterten eDiscovery (Preview) können rechtliche Teams erstellen und Anpassen ihrer rechtliche Aufbewahrungspflicht Benachrichtigung Workflow. Das Feature Verwaltungsberechtigter Communications ermöglicht rechtlichen Teams so konfigurieren Sie die folgenden Hinweise und Workflows:

1. **Beachten Sie die Veröffentlichungslizenz**: eine rechtliche Aufbewahrungspflicht Bekanntmachung wird ausgegeben, (oder initiiert) durch eine Benachrichtigung über die rechtsabteilung Verwalter, die die relevanten Informationen über die Groß-/Kleinschreibung des Gegenstands möglicherweise. Diese Meldung weist diese Verwalter alle Informationen zu erhalten, die für die Ermittlung notwendig sein können. 
   
2.  **Beachten Sie die erneute Ausstellung**: während der Fall Verwalter gegebenenfalls zusätzliche beibehalten oder weniger Informationen als wurde zuvor angewiesen. Für dieses Szenario können Sie die vorhandenen Warteschleife Bekanntmachung aktualisieren und Ihrer Verwalter erneut ausstellen.

3.  **Beachten Sie die Freigabe**: Sobald eine Frage aufgelöst wird, und der Verwaltungsberechtigte nicht mehr ein permanentes ist, der Verwaltungsberechtigte freigegeben werden kann, sodass Informationen nicht mehr beibehalten, wenn nicht erforderlich. Darüber hinaus wird der Verwaltungsberechtigte benachrichtigt werden, die sie nicht mehr unter Beibehaltung der Zoll und mit ausstehenden Anweisungen zur ihrer Aktivität fortsetzen sind.

4. **Erinnerungen und Eskalationen**: In einigen Fällen nur einen entsprechender Hinweis ausstellen ist nicht genug sind, um gerichtlichen Ermittlungen erfüllen. Mit jeder Benachrichtigung können rechtliche Teams eine Reihe von Erinnerung und Ausweitung Workflows an, die automatisch Nachsorge mit nicht reagiert Verwalter planen.

    - **Erinnerungen**: Nachdem eine rechtliche Aufbewahrungspflicht Bekanntmachung ausgestellt oder einen Satz von Verwalter erneut ausgestellt wurde, eine Organisation möglicherweise richten Sie Erinnerungen für Benachrichtigung nicht reagiert Verwalter. 

    - **Eskalationen**: In einigen Fällen Wenn ein Verwaltungsberechtigter nicht reagiert, auch nachdem sich Erinnerungen, bleibt juristische Team kann Einrichten eines Workflows für die Ausweitung der Verwaltungsberechtigte und seinen Manager benachrichtigen.

## <a name="role-groups-and-permissions"></a>Rollengruppen und Berechtigungen 

Rechtliche Teams können steuern und ihre Groß-/Kleinschreibung Aktivität von eDiscovery-bezogene Rollengruppen und Berechtigungen in der & Security Compliance Center segmentieren. 

Um rechtliche Aufbewahrungspflicht Benachrichtigungen verwalten zu erstellen, muss ein Benutzer die folgenden integrierten Rollengruppen gehören:

- **eDiscovery-Manager** - Mitglieder dieser Rollengruppe können erstellen und Verwalten von eDiscovery-Fällen. Sie können hinzufügen und Entfernen von Mitgliedern, Verwalter platzieren und Speicherorte für Inhalte auf halten, rechtliche Aufbewahrungspflicht Benachrichtigungen verwalten, erstellen und bearbeiten Inhalte durchsucht eine Anfrage zugeordnet, exportieren Sie die Ergebnisse einer Suche Inhalte und Vorbereiten von Suchergebnissen für die Analyse in erweitert eDiscovery (Preview). Es gibt zwei Untergruppen in dieser Rollengruppe. Der Unterschied zwischen diesen Untergruppen basiert auf Bereich.

  - **eDiscovery-Manager** - anzeigen und verwalten sie erstellen oder ein Mitglied der eDiscovery-Fälle. Eine andere eDiscovery-Manager erstellt eine Anfrage, jedoch keine zweite eDiscovery-Manager als Mitglied in diesem Fall hinzufügen, werden nicht die zweite eDiscovery-Manager anzeigen oder die Groß-/Kleinschreibung auf der Seite eDiscovery in die & Security Compliance Center öffnen. eDiscovery-Manager kann auch ihre Fällen in erweiterten eDiscovery (Preview) für Analysis-Aufgaben zugreifen.

  - **eDiscovery-Administrator** - können eine eDiscovery-Manager tun kann alle Groß-/Kleinschreibung Verwaltungsaufgaben ausführen. Darüber hinaus können eine eDiscovery-Administrator:
    
    - Anzeigen aller Fälle, die auf der Seite eDiscovery-Fälle aufgeführt sind.
    - Verwalten Sie jedem Fall in der Organisation, nachdem sie sich als Mitglied der Groß-/Kleinschreibung hinzufügen.
    - Groß-/Kleinschreibung Zugriff auf Daten in erweiterten eDiscovery (Preview) für eine Anfrage in der Organisation.

Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit & Compliance Center](../assign-ediscovery-permissions.md).