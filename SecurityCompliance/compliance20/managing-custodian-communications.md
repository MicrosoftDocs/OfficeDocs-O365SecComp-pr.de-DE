---
title: Arbeiten mit Kommunikation in Advanced eDiscovery (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 916691e1f2470ef9e9e54d9dfe06c5277a92ba53
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32241252"
---
# <a name="work-with-communications-in-advanced-ediscovery-preview"></a>Arbeiten mit Kommunikation in Advanced eDiscovery (Preview)

Advanced eDiscovery (Preview) ermöglicht Rechtsabteilungen, Ihre Prozesse bei der Nachverfolgung und Verteilung von Benachrichtigungen über zugelassene Aufbewahrungen zu vereinfachen. Die Depotbank-Kommunikationsfunktion ermöglicht es den Rechtsabteilungen, Ihre gesamten legalen Aufbewahrungs Prozesse – von Benachrichtigungen, Erinnerungen und Eskalationen – an einem Ort zu verwalten und zu automatisieren.

## <a name="what-is-a-legal-hold-notification"></a>Was ist eine rechtliche Aufbewahrungs Benachrichtigung?

Eine rechtliche Aufbewahrungspflicht (auch als *Gerichtsverfahren*bezeichnet) ist eine Benachrichtigung, die von der Rechtsabteilung einer Organisation an Mitarbeiter, Kontingent Mitarbeiter oder andere Datenverwalter gesendet wird. Diese Benachrichtigungen beauftragen Verwalter zur Aufbewahrung elektronisch gespeicherter Informationen (ESI) sowie Material, das für eine aktive oder bevorstehende Rechtsmaterie relevant sein kann. Juristische Teams müssen wissen, dass jeder Verwalter die angegebenen Anweisungen erhalten, gelesen und verstanden hat.

## <a name="the-legal-hold-notification-process"></a>Benachrichtigungsprozess für zugelassene Aufbewahrung

Eine Organisation hat die Pflicht, relevante Informationen zu erhalten, wenn Sie sich über eine drohende gerichtliche oder behördliche Untersuchung erfährt. Um die Aufbewahrungsanforderungen einzuhalten, sollte die Organisation unverzüglich potenzielle Verwalter über ihre Pflicht zur Aufbewahrung relevanter Informationen informieren. 

Mit Advanced eDiscovery (Preview) können juristische Teams ihren gesetzlichen Aufbewahrungs Status für Benachrichtigungen erstellen und anpassen. Die Funktion für die Depot Kommunikation ermöglicht es juristischen Teams, die folgenden Hinweise und Workflows zu konfigurieren:

1. **Veröffentlichungshinweis**: eine gesetzliche Aufbewahrungspflicht wird durch eine Benachrichtigung der Rechtsabteilung an Verwalter ausgestellt (oder eingeleitet), die über relevante Informationen zu diesem Fall verfügen könnten. Dieser Hinweis weist diese Verwalter an, alle Informationen beizubehalten, die möglicherweise für die Ermittlung benötigt werden. 
   
2.  **ErneutEr Veröffentlichungshinweis**: in einem Fall können Verwalter zusätzliche oder weniger Informationen erhalten, als Sie zuvor angewiesen wurden. In diesem Szenario können Sie den vorhandenen Haltestatus aktualisieren und ihn erneut an Ihre Verwalter ausgeben.

3.  **Veröffentlichungshinweis**: Sobald eine Angelegenheit gelöst ist und die Depotbank keine Aufbewahrungspflicht mehr unterliegt, kann die Depotbank freigegeben werden, damit Informationen nicht mehr aufbewahrt werden, wenn Sie nicht benötigt werden. Darüber hinaus wird Ihr Depotbank benachrichtigt, dass Sie nicht mehr zu den Erhaltungs Pflichten und den ausstehenden Anweisungen für die Wiederaufnahme ihrer Aktivität berechtigt sind.

4. **Erinnerungen und Eskalationen**: in einigen Fällen genügt es nicht, nur eine Nachricht zu veröffentlichen, um die gesetzlichen Anforderungen zu erfüllen. Mit jeder Benachrichtigung können juristische Teams eine Reihe von Mahn-und Eskalations Workflows planen, um automatisch Nachverfolgung mit nicht reagierenden Verwalter zu führen.

    - **Erinnerungen**: Nachdem eine gesetzliche Aufbewahrungsfrist für eine Reihe von Verwalter ausgestellt oder erneut ausgestellt wurde, kann eine Organisation Erinnerungen für die Warnung nicht reagierender Verwalter einrichten. 

    - **Eskalationen**: Wenn eine Depotbank auch nach einer Reihe von Erinnerungen nicht mehr reagiert, kann das juristische Team einen Eskalations Workflow einrichten, um die Depotbank und ihren Vorgesetzten zu benachrichtigen.

## <a name="role-groups-and-permissions"></a>Rollengruppen und Berechtigungen 

Juristische Teams können Ihre Fall Aktivitäten mithilfe von eDiscovery-bezogenen Rollengruppen und Berechtigungen im Security & Compliance Center Steuern und segmentieren. 

Zum Erstellen und Verwalten von Benachrichtigungen für zugelassene Aufbewahrung muss ein Benutzer Teil der folgenden Rollengruppen sein:

- **eDiscovery-Manager** : Mitglieder dieser Rollengruppe können eDiscovery-Fälle erstellen und verwalten. Sie können Mitglieder hinzufügen und entfernen, Aufbewahrungs-und inhaltsspeicherorte aufbewahren, Benachrichtigungen über zugelassene Aufbewahrungen verwalten, Inhalts suchen erstellen und bearbeiten, die mit einem Fall verknüpft sind, die Ergebnisse einer Inhaltssuche exportieren und Suchergebnisse für die Analyse in Advanced vorbereiten. eDiscovery (Vorschau). Diese Rollengruppe enthält zwei Untergruppen. Die Differenz zwischen diesen Untergruppen basiert auf dem Bereich.

  - **eDiscovery Manager** – kann die eDiscovery-Fälle anzeigen und verwalten, die Sie erstellen oder Mitglied sind. Wenn ein anderer eDiscovery-Manager einen Fall erstellt, aber keinen zweiten eDiscovery-Manager als Mitglied dieses Falls hinzufügt, kann der zweite eDiscovery-Manager den Fall auf der eDiscovery-Seite im Security & Compliance Center nicht anzeigen oder öffnen. eDiscovery-Manager können auch auf ihre Fälle in Advanced eDiscovery (Preview) zugreifen, um Analyseaufgaben auszuführen.

  - **eDiscovery-Administrator** – kann alle Fall Verwaltungsaufgaben durchführen, die ein eDiscovery-Manager ausführen kann. Darüber hinaus können eDiscovery-Administratoren folgende Aktionen durchführen:
    
    - Anzeigen aller Fälle, die auf der Seite eDiscovery-Fälle aufgeführt sind.
    - Verwalten Sie alle Fälle in der Organisation, nachdem Sie sich selbst als Mitglied der Anfrage hinzugefügt haben.
    - Access Case Data in Advanced eDiscovery (Preview) für jeden Fall in der Organisation.

Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Office 365 Security _AMP_ Compliance Center](../assign-ediscovery-permissions.md).