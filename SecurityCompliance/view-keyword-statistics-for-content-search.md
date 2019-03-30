---
title: Anzeigen von Schlüsselwortstatistiken für Inhaltssuchergebnisse
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/30/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 9701a024-c52e-43f0-b545-9a53478aec04
description: Verwenden Sie die Suchstatistik Funktion, um Statistiken für mehrere Inhalts suchVorgänge im Security & Compliance Center anzuzeigen und zu vergleichen. Sie können die Stichwortliste auch beim Erstellen oder Bearbeiten einer Suchabfrage konfigurieren, um Erweiterte Statistiken zu erhalten, die zeigen, wie viele Elemente mit den einzelnen Schlüsselwörtern oder Schlüsselwörtern übereinstimmen.
ms.openlocfilehash: 5e4cca18f6a50f2647265f02dab7ab3f20f513fc
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001128"
---
# <a name="view-keyword-statistics-for-content-search-results"></a>Anzeigen von Schlüsselwortstatistiken für Inhaltssuchergebnisse

Nach dem Erstellen und Ausführen einer Inhaltssuche können Sie Statistiken zu den geschätzten Suchergebnissen anzeigen. Dies enthält eine Zusammenfassung der Suchergebnisse (ähnlich der Zusammenfassung der geschätzten Suchergebnisse, die im Detailbereich angezeigt werden), die Abfragestatistiken wie die Anzahl der inhaltsspeicherorte mit Elementen, die mit der Suchabfrage übereinstimmen, und der Name der inhaltsspeicherorte , die die meisten übereinstimmenden Elemente aufweisen. Sie können Statistiken für eine oder mehrere Inhalts Suchvorgänge anzeigen. Auf diese Weise können Sie die Ergebnisse für mehrere Suchvorgänge schnell vergleichen und Entscheidungen zur Effektivität ihrer Suchabfragen treffen.
  
Darüber hinaus können Sie neue und vorhandene suchen konfigurieren, um Statistiken für jedes Schlüsselwort in einer Suchabfrage zurückzugeben. Auf diese Weise können Sie die Anzahl der Ergebnisse für jedes Schlüsselwort in einer Abfrage vergleichen und die schlüsselwortstatistik von mehreren suchen vergleichen.
  
Sie können die Suchstatistiken und Keyword-Statistiken auch in eine CSV-Datei herunterladen. Auf diese Weise können Sie die Filter-und Sortierfunktionen in Excel verwenden, um Ergebnisse zu vergleichen und Berichte für Ihre Suchergebnisse vorzubereiten.
  
## <a name="get-statistics-for-content-searches"></a>Abrufen von Statistiken für Inhalts suchVorgänge

So zeigen Sie Statistiken für Inhalts suchVorgänge an
  
1. Navigieren Sie im Security & Compliance Center zur **Such** \> **Inhaltssuche**.
    
2. Wählen Sie in der Liste der Suchvorgänge eine oder mehrere Suchvorgänge aus, ****![und klicken Sie dann auf](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png)Statistik Suchstatistik-Schaltfläche Durchsuchen.
    
    ![Wählen Sie mehrere Suchvorgänge aus, und klicken Sie dann auf Suchstatistiken](media/1195c6c3-2e00-469d-8c29-85c1c7ebe6c7.png)
  
3. Klicken Sie auf der Seite **Suchstatistiken** auf einen der folgenden Links, um Statistiken zu den ausgewählten Suchvorgängen anzuzeigen. 
    
    **Summary**
    
    Auf dieser Seite werden Statistiken angezeigt, die denen ähneln, die im Detailbereich auf der Seite für die **Inhaltssuche** angezeigt werden. Die Statistik für alle ausgewählten suchen wird angezeigt. Beachten Sie, dass Sie die ausgewählten Suchvorgänge auf dieser Seite erneut ausführen können, um die Statistiken zu aktualisieren. 
    
    ![Zusammenfassung der Statistiken für die ausgewählten Suchvorgänge](media/abb663eb-b3d6-4f4c-a99f-55d20b0848af.png)
  
    a.  Der Name der Inhaltssuche. Wie bereits erwähnt, können Sie Statistiken für mehrere Suchvorgänge anzeigen und vergleichen.
    
    b. Der Typ des Inhaltsspeicherorts, der durchsucht wurde. In jeder Zeile werden Statistiken für Postfächer, Websites und öffentliche Ordner aus der angegebenen Suche angezeigt.
    
    c. Die Anzahl der inhaltsspeicherorte, die Elemente enthalten, die mit der Suchabfrage übereinstimmen. Bei Postfächern enthält diese Statistik auch die Anzahl der Archivpostfächer, die Elemente enthalten, die mit der Suchabfrage übereinstimmen.
    
    d. Die Gesamtzahl der Elemente aller angegebenen inhaltsspeicherorte, die mit der Suchabfrage übereinstimmen. Beispiele für Elementtypen sind e-Mail-Nachrichten, Kalenderelemente und Dokumente. Wenn ein Element mehrere Instanzen eines Schlüsselwortes enthält, nach dem gesucht wird, wird es nur einmal in der Gesamtanzahl der Elemente gezählt. Wenn Sie beispielsweise nach Wörtern "Stock" oder "Betrug" suchen und eine e-Mail-Nachricht drei Instanzen des Wortes "Stock" enthält, wird Sie nur einmal in der Spalte **Items** gezählt. 
    
    e. Die Gesamtgröße aller Elemente, die am angegebenen Inhaltsspeicherort gefunden wurden, die mit der Suchabfrage übereinstimmen. 
    
    **Abfragen**
    
    Auf dieser Seite werden Statistiken zur Suchabfrage angezeigt.
    
    ![Suchabfrage Statistik für die ausgewählten Suchvorgänge](media/dc817526-dfb9-43d3-a14c-4c58077eb7bb.png)
  
    a. Der Name der Inhaltssuche, für die die Zeile Abfragestatistiken enthält.
    
    b. Der Typ des Inhaltsspeicherorts, auf den die Abfragestatistiken angewendet werden.
    
    c. Diese Spalte gibt an, auf welchen Teil der Suchabfrage die Statistiken angewendet werden. **Primary** gibt die gesamte Suchabfrage an. Wenn Sie beim Erstellen oder Bearbeiten einer Suchabfrage eine Stichwortliste verwenden, sind die Statistiken für die einzelnen Komponenten der Abfrage in dieser Tabelle enthalten. Weitere Informationen finden Sie im Abschnitt [Get Keyword Statistics for Content searches](#get-keyword-statistics-for-content-searches) in diesem Artikel. 
    
    d. Diese Spalte enthält die tatsächliche Suchabfrage, die vom Tool für die Inhaltssuche ausgeführt wird. Beachten Sie, dass das Tool automatisch einige zusätzliche Komponenten zu der erstellten Abfrage hinzufügt. 

    - Wenn Sie nach allen Inhalten in Postfächern suchen (indem Sie keine Schlüsselwörter angeben), ist `size>=0` die eigentliche Schlüsselwortabfrage so, dass alle Elemente zurückgegeben werden. 
    
     - Beim Durchsuchen von SharePoint Online-und OneDrive für Business-Websites werden die beiden folgenden Komponenten hinzugefügt:
    
          **Nicht IsExternalContent: 1** -schließt Inhalte aus einer lokalen SharePoint-Organisation aus. 
    
          **Nicht IsOneNotePage: 1** -schließt alle OneNote-Dateien aus, da es sich dabei um Duplikate eines Dokuments handeln würde, das mit der Suchabfrage übereinstimmt. 

    
    e. Die Anzahl der inhaltsspeicherorte (angegeben in der Spalte * * Location Type * *), die Elemente enthalten, die mit der in der **Abfrage** Spalte aufgeführten Suchabfrage übereinstimmen. 
    
    f. Die Anzahl der Elemente (aus dem angegebenen Inhaltsspeicherort), die mit der in der **Abfrage** Spalte aufgeführten Suchabfrage übereinstimmen. Wie bereits erläutert, wird ein Element, das mehrere Instanzen eines Schlüsselwortes enthält, nach dem gesucht wird, nur einmal in dieser Spalte gezählt. 
    
    g. Die Gesamtgröße aller Elemente, die im angegebenen Inhaltsspeicherort gefunden wurden und mit der Suchabfrage in der Spalte **Abfrage** übereinstimmen. 
    
    **Top-Standorte**
    
    Auf dieser Seite werden Statistiken zur Anzahl der Elemente angezeigt, die mit der Suchabfrage in jedem durchsuchten Inhaltsspeicherort übereinstimmen. Die Top 1.000-Speicherorte werden angezeigt. Wenn Sie Statistiken für mehrere Suchvorgänge anzeigen, werden die Top-1.000-Speicherorte für jede Suche angezeigt. Beachten Sie, dass ein Inhaltsspeicherort nicht auf dieser Seite enthalten ist, wenn er keine Elemente enthält, die mit der Suchabfrage übereinstimmen.
    
    ![Statistiken zur Anzahl der Elemente, die in den gesuchten Inhaltsspeicherorten gefunden wurden](media/35a820b0-85d9-45d1-9a0c-c74bec803e67.png)
  
    a. Der Name des Inhaltsspeicherorts.
    
    b. Der Typ des Inhaltsspeicherorts, auf den die Standort Statistiken angewendet werden.
    
    c. Für jede Suche, für die Sie Statistiken anzeigen, gibt es Spalten. In dieser Spalte wird die Anzahl (und Gesamtgröße) von Elementen angezeigt, die mit der Suchabfrage an den einzelnen Inhaltsspeicherorten übereinstimmen. Beachten Sie, dass beim Anzeigen von Statistiken für mehrere Suchvorgänge das "NA" in dieser Spalte angibt, dass der Inhaltsspeicherort nicht in die Suche einbezogen wurde. 

## <a name="get-keyword-statistics-for-content-searches"></a>Stichwort Statistiken für Inhaltssuche abrufen

Wie zuvor erläutert, werden auf der Seite **Abfragen** die Suchabfrage und die Anzahl (und die Größe) der Elemente angezeigt, die mit der Abfrage übereinstimmen. Wenn Sie beim Erstellen oder Bearbeiten einer Suchabfrage eine Stichwortliste verwenden, erhalten Sie Erweiterte Statistiken, die zeigen, wie viele Elemente mit den einzelnen Schlüsselwörtern oder Schlüsselwörtern übereinstimmen. Auf diese Weise können Sie schnell erkennen, welche Teile der Abfrage am meisten (und am wenigsten) effektiv sind. Wenn beispielsweise ein Schlüsselwort eine hohe Anzahl von Elementen zurückgibt, können Sie die Stichwortabfrage verfeinern, um die Suchergebnisse einzuschränken. Sie können eine Stichwortliste einrichten, wenn Sie eine Inhaltssuche erstellen oder bearbeiten. 


So erstellen Sie eine Stichwortliste und zeigen Schlüsselwort Statistiken für eine Inhaltssuche an
  
1. Navigieren Sie im Security & Compliance Center zur **Such** \> **Inhaltssuche**.
    
2. Klicken Sie in der Liste der Inhaltssuche auf und eine Suche, und klicken **** ![Sie dann auf](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)Bearbeitungssymbol bearbeiten.
    
3. Klicken Sie auf **Abfrage** , und führen Sie die folgenden Schritte aus: 
    
    ![Aktivieren Sie das Kontrollkästchen Stichwortliste anzeigen, und geben Sie in jeder Zeile ein Schlüsselwort ein.](media/73ef46dd-3d5c-415d-b5e7-c3559caaafe2.png)
  
    a. Aktivieren Sie das Kontrollkästchen **Keyword-Liste anzeigen** . 
    
    b. Geben Sie ein Stichwort oder eine Stichwort Phase in eine Zeile in der Schlüsselwörter-Tabelle ein. Geben Sie beispielsweise in der ersten Zeile **Budget** ein, und geben Sie dann **Sicherheit** in der zweiten Zeile ein. 
    
4. Klicken Sie nach dem Hinzufügen der Schlüsselwörter, die Sie suchen und Statistiken erhalten möchten, auf **Suchen** , um die überarbeitete Suche auszuführen. 
    
5. Wenn die Suche abgeschlossen ist, wählen Sie Sie in der Liste der Suchvorgänge aus, **** ![und klicken Sie dann auf](media/9bf56d43-25bf-4f53-a4be-f4d55102310c.png)Statistik Suchstatistik-Schaltfläche Durchsuchen. Sie können Schlüsselwort Statistiken auch für mehrere Suchvorgänge anzeigen und vergleichen.
    
6. Klicken Sie auf der Seite **Suchstatistiken** auf **Abfrage** , um die schlüsselwortstatistik für die ausgewählten Suchvorgänge anzuzeigen. 
    
    ![Die Statistiken für die einzelnen Schlüsselwörter für die ausgewählten Suchvorgänge werden angezeigt.](media/e7910fa9-af93-4df9-92d0-e1e3e089e14f.png)
  
    Wie im vorherigen Screenshot gezeigt, werden die Statistiken für jedes Schlüsselwort angezeigt; Hierzu gehören: 
    
    - Die schlüsselwortstatistik für jeden Inhaltstyp, der in der Suche enthalten ist.
    
    - Die tatsächliche Suchabfrage für jedes Schlüsselwort, das alle Bedingungen aus der Suchabfrage enthält. 
    
    - Die vollständige Suchabfrage (als **primär** in der Spalte " **Teile** " bezeichnet) und die Statistiken für die vollständige Abfrage. Hinweis Dies sind die gleichen Statistiken, die auf **** der Zusammenfassungsseite angezeigt werden. 

> [!NOTE]
> Um Probleme zu vermeiden, die durch umfangreiche Stichwortlisten verursacht werden, sind Sie jetzt auf maximal 20 Zeilen in der Stichwortliste einer Suchabfrage beschränkt.
