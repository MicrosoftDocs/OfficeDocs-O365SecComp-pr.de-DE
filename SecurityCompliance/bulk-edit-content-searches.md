---
title: Massenbearbeitung von Inhalts suchen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/29/2016
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 39e4654a-9588-41f6-892b-c33ab57bfbe2
description: Verwenden Sie den Massen Such-Editor im Security and Compliance Center in Office 365 oder Microsoft 365, um die Abfrage-und inhaltsspeicherorte für eine oder mehrere Inhalts suchen schnell zu ändern.
ms.openlocfilehash: 69d2a40a28fd435873eae9b19ad2c8ad1e25d27c
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2019
ms.locfileid: "35435115"
---
# <a name="bulk-edit-content-searches"></a>Massenbearbeitung von Inhalts suchen

Sie können den Massen Such-Editor im Inhalts Such Tool verwenden, um mehrere Suchvorgänge gleichzeitig zu bearbeiten. Mit diesem Tool können Sie die Abfrage-und inhaltsspeicherorte für eine oder mehrere Suchvorgänge schnell ändern. Anschließend können Sie die Suchvorgänge erneut ausführen und neue geschätzte Suchergebnisse für die geänderten Suchvorgänge abrufen. Mit dem Editor können Sie auch Abfragen und inhaltsspeicherorte aus einer Microsoft Excel Datei oder Textdatei kopieren und einfügen. Dies bedeutet, dass Sie das Suchstatistik Tool verwenden können, um die Statistiken einer oder mehrerer Suchvorgänge anzuzeigen, exportieren Sie die Statistik in eine CSV-Datei, in der Sie die Abfragen und inhaltsspeicherorte in Excel bearbeiten können. Anschließend verwenden Sie den Massen Such-Editor, um die geänderten Abfragen und inhaltsspeicherorte zu den Suchvorgängen hinzuzufügen. Nachdem Sie eine oder mehrere Suchvorgänge überarbeitet haben, können Sie Sie erneut starten und neue geschätzte Suchergebnisse abrufen.
  
Weitere Informationen zur Verwendung des Suchstatistik Tools finden Sie unter [Anzeigen von Schlüsselwort Statistiken für Inhalts Suchergebnisse](view-keyword-statistics-for-content-search.md).
  
## <a name="use-the-bulk-search-editor-to-change-queries"></a>Verwenden des Massen Such-Editors zum Ändern von Abfragen

1. Wechseln Sie [https://protection.office.com](https://protection.office.com)zu, und klicken Sie dann auf **Such** \> **Inhaltssuche**.
    
2. Wählen Sie in der Liste der Suchvorgänge eine oder mehrere Suchvorgänge aus, **** ![und klicken Sie dann auf Massensuche](media/1ddb3d18-2f00-4a7b-98a6-817ca5ec7014.png)-Editor-Massen Such-Editor-Schaltfläche.
    
    ![Wählen Sie eine oder mehrere Suchvorgänge aus, und klicken Sie dann auf Massen Such-Editor](media/600c9716-89a2-4451-b111-fa7cfaad2006.png)
  
    Die folgenden Informationen werden auf der Seite **Abfragen** des Massen Such-Editors angezeigt. 
    
    ![Auf der Seite Massensuche-Editor werden die Abfragen für die ausgewählten Suchvorgänge angezeigt.](media/189659af-cc78-4479-b0bc-a93decad2f6c.png)
  
    a. In der Spalte **Suchen** wird der Name der Inhaltssuche angezeigt. Wie bereits erwähnt, können Sie die Abfrage für mehrere Suchvorgänge bearbeiten. 
    
    b. In der **Abfrage** Spalte wird die Abfrage für die Inhaltssuche angezeigt, die in der Spalte **Suchen** aufgeführt ist. Wenn die Abfrage mit dem Keyword-Listenfeature erstellt wurde, werden die Schlüsselwörter durch den Text * `(c:s)`* getrennt **. Dies deutet darauf hin, dass die Schlüsselwörter durch den **or** -Operator verbunden sind. Wenn die Abfragebedingungen enthält, werden die Schlüsselwörter und Bedingungen zusätzlich durch den Text * * `(c:c)`getrennt **. Dies deutet darauf hin, dass die Schlüsselwörter (oder Keyword-Phasen) durch den **and-** Operator mit den Bedingungen verbunden sind. Im vorherigen Screenshot beispielsweise lautet die for Search-ContosoSearch1 die KQL-Abfrage, die dem entspricht `customer (c:s) pricing(c:c)(date=2000-01-01..2016-09-30)` `(customer OR pricing) AND (date=2002-01-01..2016-09-30)`.
    
3. Klicken Sie zum Bearbeiten einer Abfrage in die Zelle der Abfrage, die Sie ändern möchten, und führen Sie eine der folgenden Aktionen aus. Beachten Sie, dass die Zelle durch ein blaues Feld umrandet wird, wenn Sie darauf klicken.
    
   - Geben Sie die neue Abfrage in die Zelle ein. Beachten Sie, dass Sie einen Teil der Abfrage nicht bearbeiten können. Sie müssen die gesamte Abfrage eingeben.
    
      Oder
    
    - Fügt eine neue Abfrage in die Zelle ein. Dabei wird davon ausgegangen, dass Sie den Abfragetext aus einer Datei wie einer Textdatei oder einer Excel-Datei kopiert haben.
    
4. Nachdem Sie eine oder mehrere Abfragen auf der Seite **Abfragen** bearbeitet haben, klicken Sie auf **Speichern**.
    
    Die geänderte Abfrage wird in der **Abfrage** Spalte für die ausgewählte Suche angezeigt. 
    
5. Klicken Sie auf **Schließen** , um den Massen Such-Editor zu schließen. 
    
6. Wählen Sie auf der Seite **Inhaltssuche** die Suche aus, die Sie bearbeitet haben, und klicken Sie auf Suche **starten** , um die Suche mit der geänderten Abfrage neu zu starten. 
    
Hier finden Sie einige Tipps zum Bearbeiten von Abfragen mit dem Massen Such-Editor:
  
- Kopieren Sie die vorhandene Abfrage (mithilfe von **STRG C** ) in eine Textdatei. Bearbeiten Sie die Abfrage in der Textdatei, kopieren Sie die geänderte Abfrage, und fügen Sie Sie in der Zelle auf der Seite **Abfragen** mit **STRG V** wieder ein. 
    
- Sie können auch Abfragen aus anderen Anwendungen (beispielsweise Microsoft Word oder Microsoft Excel) kopieren. Beachten Sie jedoch, dass Sie mit dem Massen Such-Editor versehentlich nicht unterstützte Zeichen zu einer Abfrage hinzufügen können. Die beste Möglichkeit, nicht unterstützte Zeichen zu verhindern, besteht darin, die Abfrage einfach in eine Zelle auf der Seite **Abfragen** einzugeben. Alternativ können Sie eine Abfrage aus Word oder Excel kopieren und in einem Nur-Text-Editor, z. B. Microsoft Editor, in eine Datei einfügen. Speichern Sie dann die Textdatei, und wählen Sie **ANSI** in der Dropdownliste **Codierung** aus. Dadurch werden alle Formatierungen und nicht unterstützten Zeichen entfernt. Anschließend können Sie die Abfrage aus der Textdatei auf der Seite **Abfragen** kopieren und einfügen. 
    
  
## <a name="use-the-bulk-search-editor-to-change-content-locations"></a>Verwenden des Massen Such-Editors zum Ändern von Inhaltsspeicherorten

1. Klicken Sie im Massen Such-Editor für eine oder mehrere ausgewählte Suchvorgänge auf **Massen Speicherort-Editor aktivieren**, und klicken Sie dann auf den Link **Standorte** , der auf der Seite angezeigt wird. 
    
    Die folgenden Informationen werden auf der Seite **Speicherorte** des Massen Such-Editors angezeigt. 
    
    ![Klicken Sie auf Massen Speicherort-Editor aktivieren, und klicken Sie dann auf Speicherorte zum Hinzufügen oder Entfernen von Inhaltsspeicherorten](media/a5a468ce-bd63-4c53-bc37-ff64cf769e59.png)
  
    a. **Zu durchsuchende Postfächer** In diesem Abschnitt wird eine Spalte für jede ausgewählte Inhaltssuche und Zeile für jedes Postfach angezeigt, das in der Suche enthalten ist. Ein Häkchen gibt an, dass das Postfach in die Suche einbezogen wird. Sie können einer Suche zusätzliche Postfächer hinzufügen, indem Sie die e-Mail-Adresse des Postfachs in eine leere Zeile eingeben und dann auf das Kontrollkästchen für die Inhaltssuche klicken, die Sie hinzufügen möchten. Sie können ein Postfach auch aus einer Suche entfernen, indem Sie das Kontrollkästchen deaktivieren.
    
    b. **Zu durchsuchende SharePoint-Websites** In diesem Abschnitt wird eine Zeile für jede SharePoint-und OneDrive-Website angezeigt, die in jeder ausgewählten Inhaltssuche enthalten ist. Ein Häkchen gibt an, dass die Website in die Suche einbezogen wird. Sie können einer Suche weitere Websites hinzufügen, indem Sie die URL für die Website in eine leere Zeile eingeben und dann auf das Kontrollkästchen für die Inhaltssuche klicken, die Sie hinzufügen möchten. Oder Sie können eine Website aus einer Suche entfernen, indem Sie das Kontrollkästchen deaktivieren.
    
    c. **Andere Suchoptionen** Dieser Abschnitt gibt an, ob nicht indizierte Elemente und öffentliche Ordner in die Suche einbezogen werden. Um diese einzubeziehen, stellen Sie sicher, dass das Kontrollkästchen aktiviert ist. Um Sie zu entfernen, deaktivieren Sie das Kontrollkästchen.
    
2. Nachdem Sie einen oder mehrere der Abschnitte auf der Seite **Speicherorte** bearbeitet haben, klicken Sie auf **Speichern**.
    
    Die überarbeiteten inhaltsspeicherorte werden im entsprechenden Abschnitt für die ausgewählten Suchvorgänge angezeigt.
    
3. Klicken Sie auf **Schließen** , um den Massen Such-Editor zu schließen. 
    
4. Wählen Sie auf der Seite **Inhaltssuche** die von Ihnen bearbeitete Suche aus, und klicken Sie auf Suche **starten** , um die Suche mithilfe der überarbeiteten inhaltsspeicherorte neu zu starten. 
    
Hier finden Sie einige Tipps zum Bearbeiten von Inhaltsspeicherorten mit dem Massen Such-Editor:
  
- Sie können Inhalts suchen bearbeiten, um alle Postfächer oder Websites in der Organisation zu durchsuchen, indem Sie **alle** in eine leere Zeile im Abschnitt **Postfächer in Suche** oder **SharePoint-Websites zum Suchen** eingeben und dann auf das Kontrollkästchen klicken. 
    
- Sie können mehrere inhaltsspeicherorte zu einer oder mehreren Suchvorgängen hinzufügen, indem Sie mehrere Zeilen aus einer Textdatei oder einer Excel-Datei kopieren und anschließend in einen Abschnitt auf der Seite **Speicherorte** einfügen. Nachdem Sie neue Speicherorte hinzugefügt haben, müssen Sie das Kontrollkästchen für jede Suche aktivieren, der Sie den Speicherort hinzufügen möchten. 
    
    > [!TIP]
    > Um eine Liste der e-Mail-Adressen für alle Benutzer in Ihrer Organisation zu erstellen, führen Sie den PowerShell-Befehl in Schritt 2 in [Schritt 2: Generieren einer Liste von Benutzern](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md#step-2-generate-a-list-of-users)aus. Oder führen Sie die Schritte unter [Get a list of all User OneDrive URLs in Ihrer Organisation](https://docs.microsoft.com/onedrive/list-onedrive-urls) aus, um eine Liste aller OneDrive für Unternehmen Websites in Ihrer Organisation zu generieren. Beachten Sie, dass Sie die URL für die mysite-Domäne Ihrer Organisation Anfügen müssen (beispielsweise https://contoso-my.sharepoint.com) an die OneDrive für Unternehmen Websites, die durch das Skript erstellt wurden. Nachdem Sie eine Liste mit e-Mail-Adressen oder OneDrive für Unternehmen Websites erhalten haben, können Sie diese kopieren und auf der Seite **Speicherorte** im Massen Such-Editor einfügen. 
  
- Nachdem Sie auf **Speichern** klicken, um die Änderungen im Massen Such-Editor zu speichern, wird die e-Mail-Adresse für Postfächer überprüft, die Sie einer Suche hinzugefügt haben. Wenn die e-Mail-Adresse nicht vorhanden ist, wird eine Fehlermeldung angezeigt, die besagt, dass das Postfach nicht gefunden werden kann. Beachten Sie, dass URLs für Websites nicht überprüft werden. 
  

