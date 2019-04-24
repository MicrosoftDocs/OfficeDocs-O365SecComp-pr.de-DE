---
title: Suchen nach Daten in einer Untersuchung
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
ms.openlocfilehash: 5f52f26c4443addd0e108794e1d3635a9b8efb98
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258053"
---
# <a name="search-for-data-in-an-investigation"></a>Suchen nach Daten in einer Untersuchung

Auf der Registerkarte **Suche** in einer Daten Untersuchung können Sie mithilfe von Schlüsselwörtern und Bedingungen nach verlegten, vertraulichen oder vertraulichen Daten in Inhaltsspeicherorten in Office 365 suchen. 

Nachdem Sie eine Suche ausgeführt haben, können Sie Statistiken zu den von der Suche zurückgegebenen Elementen anzeigen, beispielsweise die inhaltsspeicherorte mit den meisten Elementen, die mit der Suchabfrage übereinstimmen. Sie können auch eine Vorschau einer Teilmenge der Ergebnisse anzeigen. Nachdem Sie die Dokumente identifiziert haben, die Sie weiter untersuchen möchten, können Sie die Ergebnisse der Suche einem Beweissatz hinzufügen, der für weitere Prozesse und Analysen festgelegt ist.

## <a name="create-a-search"></a>Create a search

1. Klicken Sie in einer Untersuchung auf die Registerkarte **Suchvorgänge** , und klicken Sie dann auf **neue Suche**. 

    Ein Assistent wird angezeigt, in dem Sie durch den Prozess der Erstellung einer Suche geleitet werden.

2. Geben Sie einen Such Namen und eine optionale Beschreibung für die Suche ein.

3. Definieren Sie Ihre Suchkriterien. Sie können Bedingungen für die Suche hinzufügen, indem Sie die vordefinierten Bedingungs Karten verwenden oder Sucheigenschaften Namen in der Stichwortabfrage verwenden. Weitere Informationen finden Sie unter [Erstellen von Suchabfragen](build-search-queries.md).

4. Wählen Sie die zu durchsuchenden inhaltsspeicherorte (Datenquellen) aus. Sie können die Suche Bereich, indem Sie die inhaltsspeicherorte bestimmter Personen von Interesse (wenn Sie die Untersuchung hinzugefügt haben). Wenn Sie Personen, die für die Untersuchung von Interesse sind, hinzugefügt haben, können Sie Sie hinzufügen, indem Sie die Schritte unter [Verwalten von Personen von Interesse](manage-people-of-interest.md#add-people-of-interest)ausführen.
 
    In einigen Fällen müssen Sie möglicherweise zuerst alle inhaltsspeicherorte in Ihrer Organisation durchsuchen. Alternativ können Sie Speicherorte suchen, die nicht einer bestimmten Person gehören. In diesen Szenarien können Sie entweder Ihre gesamte Organisation oder alle Standorte für einen bestimmten Office 365-Dienst (beispielsweise Exchange, SharePoint, OneDrive oder Teams) durchsuchen.

5. Speichern Sie die Suche, und führen Sie Sie aus.

Nachdem die Suche erstellt wurde, wird eine Flyout-Seite mit Details zur Suche angezeigt. Beachten Sie, dass die Schaltflächen **Statistiken** und **Vorschau** anfänglich abgeblendet sind, da die Suche nicht abgeschlossen ist. Sie können den Fortschritt verfolgen, indem Sie die Spalte **Status** auf der Registerkarte **Suchen** überwachen.

## <a name="view-statistics-and-search-results"></a>Anzeigen von Statistiken und Suchergebnissen

Nachdem Sie eine Daten Ermittlungs Suche erstellt und gestartet haben, verwendet das Tool die Suchkriterien (Suchabfrage und inhaltsspeicherorte), die Sie definiert haben, und durchsucht einen Index im Live-Dienst nach Elementen, die Ihren Suchkriterien entsprechen. Es gibt drei Komponenten einer Suche, die zurückgegeben werden, wenn die Suche abgeschlossen ist: 

- **Estimate** -da die Suche nur einen Index durchsucht (statt der tatsächlichen inhaltsspeicherorte), sind die Ergebnisse einer Suche eine Schätzung (basierend auf dem, was im Index gefunden wurde, der mit den Suchergebnissen übereinstimmt). Eine Zusammenfassung der Schätzung wird auf der Such Flyout-Seite unter **Status**angezeigt. Beachten Sie, dass der Status des Vorkalkulations Prozesses für eine Suche auf der Registerkarte **Suchvorgänge** in der Spalte **Estimate Status** angezeigt wird. Wenn die Such Schätzung abgeschlossen ist, wird dieser Status auf **erfolgreich**festgelegt.

- **Statistics** -Statistics liefert detailliertere Informationen zu den Suchergebnissen. Dazu gehört Folgendes:

    - Zusammenfassung-Statistiken ähnlich wie die Suchergebnisse, die auf der Seite Flyout angezeigt werden.
    - Top Locations-Statistiken über die Anzahl der Elemente, die mit der Suchabfrage an den einzelnen Inhaltsverzeichnissen übereinstimmen, die durchsucht wurden. 
    - Abfragen-detaillierte Statistiken über die Suchabfrage, einschließlich der Anzahl der Elemente, die mit jeder Bedingung in einer Suchabfrage übereinstimmen.

    Klicken Sie auf der Seite Flyout auf **Statistiken** , um diese Statistiken anzuzeigen. Beachten Sie, dass diese Schaltfläche inaktiv ist, bis der Wert des vorKalkulations **Status** auf der Registerkarte **Suchen** auf **erfolgreich**festgelegt ist. Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistiken](search-statistics.md).

- **Preview** -wenn die Suche abgeschlossen ist, können Sie die tatsächlichen Elemente aus einer Beispiel Teilmenge der Suchergebnisse anzeigen, die von der Suche zurückgegeben werden. In der systemeigenen Ansicht des Elementtyps können Sie auch die Metadaten zu dem Element anzeigen. Auf diese Weise können Sie schnell feststellen, ob Ihre Suchergebnisse Ihren Erwartungen entsprechen oder ob Sie die Suche bearbeiten und erneut ausführen müssen. Klicken Sie auf der Flyout-Seite auf **Vorschau** , um Elemente aus den Suchergebnissen anzuzeigen. Beachten Sie, dass diese Schaltfläche inaktiv ist, bis der Wert des **Vorschaustatus** auf der Registerkarte **Suchvorgänge** auf **erfolgreich**festgelegt ist.
 
> [!NOTE]
> Die Statuswerte für die Spalten " **Estimate Status** " und " **Preview Status** " auf der Registerkarte " **Suchen** " werden **in Bearbeitung**und **erfolgreich**über **mittelt**. Wenn bei der Suche ein Fehler auftritt, wird der Status **fehlgeschlagen** angezeigt.

## <a name="add-search-results-to-evidence"></a>Hinzufügen von Suchergebnissen zu beweisen

Wenn Sie mit den Ergebnissen einer Suche zufrieden sind und Sie bereit sind, diese Suchergebnisse zu analysieren und zu beheben, können Sie Sie zu einem Evidence-Satz in der Untersuchung hinzufügen. Wenn Sie einem Evidence-Satz auf der Registerkarte **Evidence** Elemente hinzufügen, werden die folgenden beiden Schritte ausgeführt:

- Alle Elemente in den Suchergebnissen werden aus der Datenquelle im Live-Dienst kopiert und an einen sicheren Azure-Speicherort in der Microsoft-Cloud kopiert.

- Alle Elemente (einschließlich des Inhalts und der Metadaten) werden neu indiziert, sodass alle Daten im Evidence-Satz während der Untersuchung vollständig durchsuchbar sind. Das erneute Indizieren der Daten führt zu gründlichen und sehr schnellen Suchvorgängen, wenn Sie die Daten in dem bei der Untersuchung festgelegten Nachweis durchsuchen.

Ein Vorteil des Kopierens der Live-Daten in einen in Azure festgelegten Nachweis besteht darin, dass Sie bei zeitabhängigen oder kritischen Vorfällen schnell den Schaden enthalten können, indem Sie sofort verdächtige Inhalte in der ursprünglichen Datenquelle im Live-Dienst löschen und dann der Vorfall durch Analysieren der Beweise, die in die isolierte Umgebung des Azure-Speicherorts kopiert wurden. 

Das Kopieren der ursprünglichen Daten in den Evidence-Satz erleichtert auch die Untersuchung, indem Sie erweiterte Analysetools wie die Erkennung von Designs, die Erkennung nahezu doppelter Informationen und die Identifizierung von e-Mail-Threads bereitstellen.

Bei Bedarf können Sie auch Daten aus nicht-Office 365-Datenquellen zu einem Evidence-Satz hinzufügen, damit diese zusammen mit den von Office 365 gesammelten Daten gespeichert werden.

Wenn Sie einer festgelegten Gruppe Daten hinzufügen möchten, wählen Sie auf der Registerkarte **Suchvorgänge** eine Suche aus, und klicken Sie dann auf der Seite Flyout auf **Ergebnisse zu beweisen** . Beachten Sie, dass Sie einem vorhandenen Evidence-Satz Daten hinzufügen oder einen neuen Evidence-Satz erstellen können.

### <a name="tracking-the-progress-of-adding-search-results-to-evidence"></a>NachVerfolgen des Fortschritts des Hinzufügens von Suchergebnissen zu beweisen

Das Hinzufügen von Daten zu einem Beweissatz ist ein langwieriger Prozess. Der Prozess umfasst das Sammeln der Elemente, die die ursprüngliche Datenquelle aus Office 365 (beispielsweise von Postfächern und Websites), kopieren Sie Sie in den Azure-Speicherort (dieser Kopiervorgang wird auch als *Einnahme*), und dann die Elemente erneut indizieren. Sie können den Fortschritt entweder auf der Registerkarte **Aufträge** oder auf der Registerkarte **Suchvorgänge** in der Spalte **hinzugefügte Daten nach** verfolgen. Nachdem die Verarbeitung der Beweis Verarbeitung abgeschlossen ist, können Sie zur Registerkarte **Beweise** wechseln, auf den nachweissatz klicken und dann die Untersuchung starten, indem Sie die relevanten Daten nach Bedarf durchsuchen, überprüfen, Tagging und exportieren.