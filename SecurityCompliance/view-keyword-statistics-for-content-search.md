---
title: Anzeigen von Schlüsselwortstatistiken für Inhaltssuchergebnisse
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/30/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 9701a024-c52e-43f0-b545-9a53478aec04
description: Verwenden Sie das Feature Suchstatistik zum Anzeigen und Vergleichen von Statistiken für mehrere Content-Suche in Office 365-Sicherheit &amp; Compliance Center. Sie können auch die Schlüsselwortliste konfigurieren, beim Erstellen oder eine Suchabfrage bearbeiten um erweiterte Statistiken zu erhalten, die zeigen, wie viele Elemente jedes Schlüsselwort oder Stichwortbegriff übereinstimmt.
ms.openlocfilehash: 0f0258f228e296e48def8de16aabc068901dffc7
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "27209806"
---
# <a name="view-keyword-statistics-for-content-search-results"></a>Anzeigen von Schlüsselwortstatistiken für Inhaltssuchergebnisse

Nachdem Sie erstellen und einer Inhaltssuche ausführen, können Sie Statistiken zu der geschätzten Suchergebnisse anzeigen. Dies umfasst eine Zusammenfassung der Suchergebnisse (vergleichbar mit der Zusammenfassung der geschätzten Suchergebnisse im Detailbereich angezeigt) die Abfragestatistiken wie die Anzahl der Speicherorte für Inhalte mit Elementen, die die Suchabfrage erfüllen und den Namen der Speicherorte für Inhalte die die meisten übereinstimmenden Elemente aufweisen. Sie können Statistiken für einen oder mehrere Content-Suche anzeigen. Auf diese Weise können Sie schnell vergleichen Sie die Ergebnisse für mehrere Suchen und bestimmen, welche Informationen die Effektivität von Suchabfragen.
  
Darüber hinaus können Sie neue und vorhandene Suche zum Zurückgeben von Statistiken für jedes Schlüsselwort in einer Suchabfrage konfigurieren. Auf diese Weise können Sie die Anzahl der Ergebnisse für jedes Schlüsselwort in einer Abfrage und zum Vergleichen von der schlüsselwortstatistiken aus mehreren Suchvorgängen verglichen werden soll.
  
Sie können auch die Suchstatistik und schlüsselwortstatistiken in eine CSV-Datei herunterladen. Auf diese Weise können Sie die Filter- und Funktionen in Excel verwenden, um Ergebnisse zu vergleichen, und bereiten Berichte für die Suchergebnisse.
  
## <a name="get-statistics-for-content-searches"></a>Abrufen von Statistiken für Content-Suche

So zeigen Sie Statistiken für Content-Suche an:
  
1. In der Office 365-Sicherheit &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Inhaltssuche**.
    
2. In der Liste der Suchvorgänge, wählen Sie eine oder mehrere Suchvorgänge und klicken Sie dann auf **Suchstatistik**![Suchstatistik Schaltfläche](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png).
    
    ![Wählen Sie mehrere Suchen und klicken Sie dann auf Suchstatistik](media/1195c6c3-2e00-469d-8c29-85c1c7ebe6c7.png)
  
3. Klicken Sie auf der Seite **Suchstatistik** auf eine der folgenden Links, um Statistiken über die ausgewählten Suchläufe anzuzeigen. 
    
    **Zusammenfassung**
    
    Diese Seite zeigt Statistiken ähnelt derjenigen, die im Detailbereich auf der Seite für die **Inhaltssuche** angezeigt. Statistiken für alle ausgewählten Suchvorgänge werden angezeigt. Beachten Sie, dass Sie auch die ausgewählten Suchen von dieser Seite so aktualisieren Sie die Statistiken erneut ausführen können. 
    
    ![Übersicht über die Statistiken für die ausgewählten suchen](media/abb663eb-b3d6-4f4c-a99f-55d20b0848af.png)
  
    a. der Name des Content-Suche. Wie bereits zuvor erwähnt können Sie anzeigen und Vergleichen von Statistiken für mehrere Suchvorgänge.
    
    b. der Typ des Content-Location, die durchsucht wurde. Jede Zeile Statistik für Postfächer, Websites und Öffentliche Ordner aus der angegebenen Suche angezeigt.
    
    c. der Anzahl der Speicherorte für Inhalte, enthält Elemente, die die Suchabfrage entsprechen. Für Postfächer enthält diese Statistik auch die Anzahl der archivpostfächer, die Elemente enthält, die die Suchabfrage entsprechen.
    
    d. die Gesamtanzahl der Elemente aller angegebene Speicherorte für Inhalte, die mit die Abfrage übereinstimmen. Beispiele für Elementtypen sind e-Mail-Nachrichten, Kalenderelemente und Dokumenten. Wenn ein Element mehrere Instanzen eines Stichworts, die enthält nach dem gesucht wird, wird er nur einmal in die Gesamtanzahl der Elemente gezählt. Beispielsweise wird übereinstimmenden Wörter "Stock" oder "Betrug" und eine e-Mail-Nachricht enthält drei Vorkommen des Worts "Stock", er nur einmal in der Spalte **Elemente** gezählt. 
    
    e. die Gesamtgröße aller Elemente, die in der angegebenen Inhaltsspeicherort gefunden wurden, die die Suchabfrage entsprechen. 
    
    **Abfragen**
    
    Auf dieser Seite Statistik zur Suchabfrage angezeigt.
    
    ![Search-Abfragestatistiken für die ausgewählten suchen](media/dc817526-dfb9-43d3-a14c-4c58077eb7bb.png)
  
    a. der Name des Content-Suche, die die Zeile Abfragestatistiken für die enthält.
    
    b. der Typ des Content-Location, die für die Abfrage Statistiken verfügbar sind.
    
    c. diese Spalte gibt an, welcher Teil der Suchabfrage die Statistiken für verfügbar sind. **Primäre** gibt die gesamte Suchabfrage an. Wenn Sie eine Schlüsselwortliste beim Erstellen oder eine Suchabfrage bearbeiten verwenden, sind in dieser Tabelle Statistiken für die einzelnen Komponenten der Abfrage enthalten. Finden Sie in diesem Artikel finden Sie weitere Informationen im Abschnitt [schlüsselwortstatistiken für Content-Suche erhalten möchten](#get-keyword-statistics-for-content-searches) . 
    
    d. diese Spalte enthält die eigentliche Suche abzufragen, die vom Inhaltssuche-Tool ausführen. Beachten Sie, dass das Tool automatisch einige zusätzliche Komponenten auf die Abfrage hinzufügt, den Sie erstellen. 

    - Wenn Sie für alle in Postfächern Inhalte (durch keine Schlüsselwörter Angabe), die tatsächliche Schlüssel Wort Abfrage suchen ist `size>=0` , damit alle Elemente zurückgegeben werden. 
    
     - Wenn Sie SharePoint Online und OneDrive for Business-Websites suchen, werden die beiden folgenden Komponenten hinzugefügt:
    
          **Nicht IsExternalContent:1** - schließt alle Inhalte aus einer lokalen SharePoint-Organisation. 
    
          **Nicht IsOneNotePage:1** - schließt alle OneNote-Dateien, da diese Duplikate eines beliebigen Dokuments wäre, die mit die Suchabfrage übereinstimmt. 

    
    e. die Anzahl der Speicherorte für Inhalte (angegebenen durch die ** Speicherorttyp ** Spalte), die Elemente, die die Suchabfrage aufgeführt, die in der Spalte **Abfrage** entsprechen enthalten. 
    
    f. die Anzahl der Elemente (aus der angegebenen Inhaltsspeicherort), die die Suchabfrage aufgeführt, die in der Spalte **Abfrage** übereinstimmen. Wie bereits erklärt, wenn ein Element mehrere Instanzen eines Stichworts enthält, das für, durchsucht wird es werden nur einmal gezählt in dieser Spalte. 
    
    g. die Gesamtgröße aller Elemente, die (in der angegebenen Inhaltsspeicherort) gefunden wurden, die die Suchabfrage in der Spalte **Abfrage** übereinstimmen. 
    
    **Obere Speicherorte**
    
    Diese Seite zeigt Statistiken zur Anzahl der Elemente, die die Suchabfrage in jedem Inhaltsspeicherort entsprechen, die durchsucht wurde. Die Speicherorte der oberen 1.000 werden angezeigt. Wenn Sie die Statistiken für mehrere Suchvorgänge anzeigen, werden die obersten 1.000 Speicherorte für jedes Suchergebnis angezeigt. Beachten Sie, dass ein Inhaltsspeicherort auf dieser Seite enthalten nicht zur Verfügung, wenn es keine Elemente enthalten, die die Suchabfrage entsprechen.
    
    ![Statistiken zur Anzahl der Elemente in der Speicherorte für Inhalte, die durchsucht wurden gefunden](media/35a820b0-85d9-45d1-9a0c-c74bec803e67.png)
  
    a. der Name der Inhaltsspeicherort.
    
    b. der Typ des Content-Location, die für die Statistiken Speicherort verfügbar sind.
    
    c Spalten für jedes Suchergebnis, das Sie Statistiken für Anzeigen sind vorhanden. Diese Spalte zeigt die Anzahl (und die Gesamtgröße der) der Elemente, die die Suchabfrage in jedem Inhaltsspeicherort entsprechen. Beachten Sie, dass Sie Statistiken für mehrere Suchvorgänge anzeigen, "NA" in dieser Spalte gibt an, dass der Speicherort des Inhalte in, dass die Suche enthalten war nicht. 

## <a name="get-keyword-statistics-for-content-searches"></a>Rufen Sie schlüsselwortstatistiken für Content-Suche

Wie vorherige erläutert, die Seite **Abfragen** zeigt die Suchabfrage und die Anzahl (und Größe) von Elementen, die mit die Abfrage übereinstimmen. Wenn Sie eine Schlüsselwortliste beim Erstellen oder eine Suchabfrage bearbeiten verwenden, können Sie erweiterte Statistik abrufen, die zeigen, wie viele Elemente jedes Schlüsselwort oder Stichwortbegriff übereinstimmt. Dadurch können Sie schnell erkennen, welche Teile der Abfrage die am häufigsten (und mindestens) wirksam werden. Wenn ein Schlüsselwort eine große Anzahl von Elementen zurückgibt, können Sie verfeinern die Schlüsselwort-Abfrage aus, um die Suchergebnisse einzuschränken. Sie können eine Schlüsselwortliste beim Erstellen oder einer Inhaltssuche bearbeiten einrichten. 




  
So erstellen Sie eine Schlüsselwortliste und schlüsselwortstatistiken für ein Inhaltssuche anzuzeigen:
  
1. In der Office 365-Sicherheit &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Inhaltssuche**.
    
2. In der Liste der Content-Suche auf, und eine Suche und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
3. Klicken Sie auf **Abfrage** , und führen Sie die folgenden Schritte aus: 
    
    ![Klicken Sie auf das Kontrollkästchen anzeigen Schlüsselwort Liste, und geben Sie ein Schlüsselwort in jeder Zeile](media/73ef46dd-3d5c-415d-b5e7-c3559caaafe2.png)
  
    a. Klicken Sie auf das Kontrollkästchen **Schlüsselwortliste anzeigen** . 
    
    b. Geben Sie b. ein Schlüsselwort oder Schlüsselwort Phase in einer Zeile in der Tabelle Schlüsselwörter. Beispielsweise geben Sie in der ersten Zeile **Budget** ein, und geben Sie **Sicherheit** in der zweiten Zeile. 
    
4. Nach dem Hinzufügen der Schlüsselwörter, die Sie zum Suchen und Abrufen von Statistiken für möchten, klicken Sie auf **Suchen** , um die überarbeitete Suche auszuführen. 
    
5. Wenn die Suche abgeschlossen ist, wählen Sie ihn in der Liste der Suchvorgänge, und klicken Sie dann auf **Suchstatistik** ![Suchstatistik Schaltfläche](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png). Sie können auch anzeigen und vergleichen schlüsselwortstatistiken für mehrere suchen.
    
6. Klicken Sie auf der Seite **Suchstatistik** auf **Abfrage** aus, um die schlüsselwortstatistiken für die ausgewählte Suchläufe anzuzeigen. 
    
    ![Die Statistiken für jedes Schlüsselwort für die ausgewählte durchsucht werden angezeigt.](media/e7910fa9-af93-4df9-92d0-e1e3e089e14f.png)
  
    Wie in der vorherigen Screenshot dargestellt werden die Statistiken für jedes Schlüsselwort angezeigt. Dazu gehören: 
    
    - Die schlüsselwortstatistiken für jede Art von Inhaltsspeicherort in der Suche enthalten.
    
    - Die tatsächlichen Suchabfrage für jedes Schlüsselwort, die etwaige Auflagen aus der die Suchabfrage enthält. 
    
    - Die vollständige Suchabfrage (als **primäre** in der Spalte **Teil** identifiziert) und die Statistiken für die Abfrage abgeschlossen. Beachten Sie, dass diese die gleichen Statistiken auf der Seite **Zusammenfassung** angezeigt werden. 

> [!NOTE]
> Zur Verringerung der Probleme aufgrund von großen Listen Sie nun auf ein Maximum von 20 Zeilen in der Schlüsselwortliste einer Suchabfrage begrenzt.
