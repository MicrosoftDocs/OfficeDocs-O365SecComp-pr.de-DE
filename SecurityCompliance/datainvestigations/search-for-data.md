---
title: Suchen nach Daten in einer Untersuchung
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 3e9e1cb6a434a0b8e5f7b723630812e9cdeda36d
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153637"
---
# <a name="search-for-data-in-an-investigation"></a>Suchen nach Daten in einer Untersuchung

Auf der Registerkarte **Suchen** in einer Datenermittlung können Sie in Office 365 mithilfe von Schlüsselwörtern und Bedingungen nach ungespeicherten, vertraulichen oder vertraulichen Daten in den Inhaltsspeicherorten suchen. 

Nachdem Sie eine Suche ausgeführt haben, können Sie Statistiken zu den von der Suche zurückgegebenen Elementen anzeigen, beispielsweise die inhaltsspeicherorte mit den meisten Elementen, die mit der Suchabfrage übereinstimmen. Sie können auch eine Vorschau einer Teilmenge der Ergebnisse anzeigen. Nachdem Sie die Gruppe von Dokumenten identifiziert haben, die weiter untersucht werden sollen, können Sie die Ergebnisse der Suche einem Beweissatz hinzufügen, um Sie weiter zu verarbeiten und zu analysieren.

## <a name="create-a-search"></a>Create a search

1. Klicken Sie in einer Untersuchung auf die Registerkarte **Suchen** , und klicken Sie dann auf **neue Suche**. 

    Ein Assistent wird angezeigt, der Sie durch den Prozess der Erstellung einer Suche führt.

2. Geben Sie einen Such Namen und eine optionale Beschreibung für die Suche ein.

3. Definieren Sie Ihre Suchkriterien. Sie können Bedingungen für die Suche hinzufügen, indem Sie die vordefinierten Bedingungs Karten verwenden oder Sucheigenschaften Namen in der Stichwortabfrage verwenden. Weitere Informationen finden Sie unter [Erstellen von Suchabfragen](build-search-queries.md).

4. Wählen Sie die zu durchsuchenden inhaltsspeicherorte (Datenquellen) aus. Sie können die Suche Bereichen, indem Sie die inhaltsspeicherorte bestimmter interessierter Personen auswählen (sofern Sie die Untersuchung hinzugefügt haben). Wenn Sie für die Untersuchung interessante Personen hinzugefügt haben, können Sie diese hinzufügen, indem Sie die Schritte unter [Verwalten von Personen mit Interesse](manage-people-of-interest.md#add-people-of-interest)ausführen.
 
    In einigen Fällen müssen Sie möglicherweise zunächst alle inhaltsspeicherorte in Ihrer Organisation durchsuchen. Alternativ dazu müssen Sie möglicherweise Speicherorte durchsuchen, die nicht einer bestimmten Person gehören. In diesen Szenarien können Sie auswählen, ob Sie Ihre gesamte Organisation oder alle Standorte nach einem bestimmten Office 365 Diensten (wie Exchange, SharePoint, OneDrive oder Teams) durchsuchen möchten.

5. Speichern Sie die Suche, und führen Sie Sie aus.

Nachdem die Suche erstellt wurde, wird eine Flyout-Seite mit Details zur Suche angezeigt. Beachten Sie, dass die Schaltflächen **Statistik** und **Vorschau** anfänglich abgeblendet sind, da die Suche nicht abgeschlossen wurde. Sie können den Fortschritt der Überwachung verfolgen, indem Sie die Spalte **Status** auf der Registerkarte **Suchen** überwachen.

## <a name="view-statistics-and-search-results"></a>Anzeigen von Statistiken und Suchergebnissen

Nachdem Sie eine Daten Ermittlungs Suche erstellt und gestartet haben, verwendet das Tool die von Ihnen definierten Suchkriterien (Suchabfrage und inhaltsspeicherorte) und durchsucht einen Index im Live-Dienst für Elemente, die Ihren Suchkriterien entsprechen. Es gibt drei Komponenten einer Suche, die zurückgegeben werden, wenn die Suche abgeschlossen ist: 

- **Estimate** -da die Suche nur einen Index (statt die tatsächlichen inhaltsspeicherorte) durchsucht, sind die Ergebnisse einer Suche eine Schätzung (basierend auf dem, was im Index gefunden wurde, der den Suchergebnissen entsprach). Eine Zusammenfassung der Schätzung wird auf der Flyout-Seite "Suche" unter **Status**angezeigt. Beachten Sie, dass der Status für den Schätzprozess für eine Suche auf der Registerkarte **Suchen** in der Spalte **Estimate Status** angezeigt wird. Wenn die Such Schätzung abgeschlossen ist, wird dieser Status auf **erfolgreich**festgelegt.

- **Statistics** -Statistics bieten ausführlichere Informationen zu den Suchergebnissen. Dazu gehört Folgendes:

    - Zusammenfassung-Statistiken ähnlich den Such schätzungs Ergebnissen, die auf der Flyout-Seite angezeigt werden.
    - Top Locations-Statistiken zur Anzahl der Elemente, die mit der Suchabfrage in jedem durchsuchten Inhaltsspeicherort übereinstimmen. 
    - Abfragen – detaillierte Statistiken zur Suchabfrage, einschließlich der Anzahl von Elementen, die mit jeder Bedingung in einer Suchabfrage übereinstimmen.

    Klicken Sie auf der Flyout-Seite auf **Statistik** , um diese Statistiken anzuzeigen. Beachten Sie, dass diese Schaltfläche inaktiv ist, bis der Wert des Vorkalkulations **Status** auf der Registerkarte **Suchen** auf **erfolgreich**festgelegt ist. Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistiken](search-statistics.md).

- **Vorschau** – wenn die Suche abgeschlossen ist, können Sie die tatsächlichen Elemente aus einer Stichproben Teilmenge der Suchergebnisse anzeigen, die von der Suche zurückgegeben werden. In der systemeigenen Ansicht des Elementtyps können Sie auch die Metadaten des Elements anzeigen. Dies ist eine gute Möglichkeit, schnell festzustellen, ob Ihre Suchergebnisse Ihren Erwartungen entsprechen oder ob Sie die Suche bearbeiten und erneut ausführen müssen. Klicken Sie auf der Flyout-Seite auf **Vorschau** , um Elemente aus den Suchergebnissen anzuzeigen. Beachten Sie, dass diese Schaltfläche inaktiv ist, bis der Wert des **Vorschaustatus** auf der Registerkarte **Suchen** auf **erfolgreich**festgelegt ist.
 
> [!NOTE]
> Die Statuswerte für die **Spalten Estimate Status** and **Preview Status** auf der Registerkarte **Suchen** werden **ausgeführt**und **erfolgreich** **gesendet**. Wenn ein Fehler bei der Suche vorliegt, wird der Status **fehlgeschlagen** angezeigt.

## <a name="add-search-results-to-evidence"></a>Hinzufügen von Suchergebnissen zu beweisen

Wenn Sie mit den Ergebnissen einer Suche zufrieden sind und diese Suchergebnisse analysieren und korrigieren möchten, können Sie Sie zu einem in der Untersuchung festgelegten Beweis hinzufügen. Wenn Sie einem Evidence-Element auf der Registerkarte **Beweise** Elemente hinzufügen, treten die folgenden zwei Dinge auf:

- Alle Elemente in den Suchergebnissen werden aus der Datenquelle im Live-Dienst kopiert und in einen sicheren Azure-Speicherort in der Microsoft-Cloud kopiert.

- Alle Elemente (einschließlich der Inhalte und Metadaten) werden erneut indiziert, sodass alle Daten im Evidence-Satzes während der Untersuchung vollständig durchsuchbar sind. Durch das erneute Indizieren der Daten werden gründliche und sehr schnelle Suchvorgänge durchsucht, wenn Sie während der Untersuchung die Daten im Beweissatzes durchsuchen.

Ein Vorteil beim Kopieren der Livedaten in einen Beweissatz in Azure besteht darin, dass Sie für zeitkritische oder kritische Vorfälle schnell den Schaden durch sofortiges löschen verdächtiger Inhalte in der ursprünglichen Datenquelle im Live-Dienst und anschließend untersuchen können. der Vorfall durch Analysieren der Beweise, die in die Quarantäne Umgebung des Azure-Speicherorts kopiert wurden. 

Das Kopieren der ursprünglichen Daten in den Beweissatz erleichtert auch ihre Untersuchung, indem Sie erweiterte Analysetools wie die Erkennung von Designs, die Erkennung praktischer Duplikate und die e-Mail-Threadidentifikation bereitstellen.

Falls erforderlich, können Sie auch Daten aus nicht Office 365 Datenquellen zu einem Beweissatz hinzufügen, sodass dieser zusammen mit den Daten gespeichert wird, die Sie in Office 365 sammeln.

Zum Hinzufügen von Daten zu einem belegten Datensatz wählen Sie auf der Registerkarte **Suchen** eine Suche aus, und klicken Sie dann auf der Flyout-Seite auf **Ergebnisse zu Beweismitteln hinzufügen** . Beachten Sie, dass Sie Daten zu einem vorhandenen Beweissatz hinzufügen oder on-the-Fly eine neue Beweis Gruppe erstellen können.

### <a name="tracking-the-progress-of-adding-search-results-to-evidence"></a>Nachverfolgen des Fortschritts beim Hinzufügen von Suchergebnissen zu beweisen

Das Hinzufügen von Daten zu einem Evidence-Datensatz ist ein langwieriger Prozess. Der Prozess umfasst das Sammeln der Elemente, die die ursprüngliche Datenquelle aus Office 365 (beispielsweise aus Postfächern und Websites), kopieren Sie Sie in den Azure-Speicherort (dieser Kopiervorgang wird auch als *Einnahme*bezeichnet) und dann erneut indizieren der Elemente. Sie können den Fortschritt entweder auf der Registerkarte **Aufträge** oder auf der Registerkarte **Suchen** in der Spalte **hinzugefügte Daten in Evidence nach** verfolgen. Nachdem die Verarbeitung der Beweis Verarbeitung abgeschlossen ist, können Sie zur Registerkarte **Beweise** wechseln, auf den Beweissatz klicken und dann Ihre Untersuchung starten, indem Sie die relevanten Daten nach Bedarf suchen, überprüfen, markieren und exportieren.