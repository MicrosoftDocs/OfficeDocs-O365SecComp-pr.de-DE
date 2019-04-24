---
title: Massenbearbeitung von Inhalts suchen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/29/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 39e4654a-9588-41f6-892b-c33ab57bfbe2
description: Verwenden Sie den Massen Such Editor im Security and Compliance Center in Office 365 oder Microsoft 365, um die Abfrage-und inhaltsspeicherorte für eine oder mehrere Inhalts suchVorgänge schnell zu ändern.
ms.openlocfilehash: 3a484ad689b1c638e0e14ed1643edea0f2f56c09
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243846"
---
# <a name="bulk-edit-content-searches"></a>Massenbearbeitung von Inhalts suchen

Sie können den Massen Such-Editor im Inhaltssuche-Tool verwenden, um mehrere Suchvorgänge gleichzeitig zu bearbeiten. Mit diesem Tool können Sie die Abfrage-und inhaltsspeicherorte für eine oder mehrere Suchvorgänge schnell ändern. Dann können Sie die Suchvorgänge erneut ausführen und neue geschätzte Suchergebnisse für die überarbeiteten suchen abrufen. Der Editor ermöglicht auch das Kopieren und Einfügen von Abfragen und Inhaltsspeicherorten aus einer Microsoft Excel-Datei oder-Textdatei. Sie können das Suchstatistik Tool verwenden, um die Statistiken einer oder mehrerer Suchvorgänge anzuzeigen, die Statistiken in eine CSV-Datei zu exportieren, in der Sie die Abfragen und inhaltsspeicherorte in Excel bearbeiten können. Anschließend verwenden Sie den Massen Such-Editor, um die überarbeiteten Abfragen und inhaltsspeicherorte zu den Suchvorgängen hinzuzufügen. Nachdem Sie eine oder mehrere Suchvorgänge überarbeitet haben, können Sie Sie neu starten und neue geschätzte Suchergebnisse erhalten.
  
Weitere Informationen zur Verwendung des Suchstatistik Tools finden Sie unter [View Keyword Statistics for Content Search results](view-keyword-statistics-for-content-search.md).
  
## <a name="use-the-bulk-search-editor-to-change-queries"></a>Verwenden des Massen Such-Editors zum Ändern von Abfragen

1. Wechseln Sie [https://protection.office.com](https://protection.office.com)zu, und klicken Sie dann auf **Inhaltssuche** **Durchsuchen** \> .
    
2. Wählen Sie in der Liste der Suchvorgänge eine oder mehrere Suchvorgänge aus, **** ![und klicken Sie dann auf Massen Such](media/1ddb3d18-2f00-4a7b-98a6-817ca5ec7014.png)Editor-Schaltfläche für Massensuche.
    
    ![Wählen Sie eine oder mehrere Suchvorgänge aus, und klicken Sie dann auf Massen Sucheditor](media/600c9716-89a2-4451-b111-fa7cfaad2006.png)
  
    Die folgenden Informationen werden auf der Seite **Abfragen** des Massen Such-Editors angezeigt. 
    
    ![Auf der Seite für den Massen Sucheditor werden die Abfragen für die ausgewählten Suchvorgänge angezeigt.](media/189659af-cc78-4479-b0bc-a93decad2f6c.png)
  
    a. In der Spalte **Suchen** wird der Name der Inhaltssuche angezeigt. Wie bereits erwähnt, können Sie die Abfrage für mehrere Suchvorgänge bearbeiten. 
    
    b. In der Spalte **Abfrage** wird die Abfrage für die in der Spalte **Suchen** aufgeführte Inhaltssuche angezeigt. Wenn die Abfrage mithilfe des Schlüsselwortlisten-Features erstellt wurde, werden die Schlüsselwörter durch den Text `(c:s)`* * getrennt **. Dies gibt an, dass die Schlüsselwörter durch den **or** -Operator verbunden werden. Wenn die Abfragebedingungen enthält, werden außerdem die Schlüsselwörter und die Bedingungen durch den Text * * `(c:c)`getrennt **. Dies gibt an, dass die Schlüsselwörter (oder Schlüsselwort Phasen) mit den Bedingungen des **and-** Operators verbunden sind. Beispiel: im vorherigen Screenshot der for Search-ContosoSearch1 die KQL-Abfrage, die äquivalent zu `customer (c:s) pricing(c:c)(date=2000-01-01..2016-09-30)` wäre. `(customer OR pricing) AND (date=2002-01-01..2016-09-30)`
    
3. Klicken Sie zum Bearbeiten einer Abfrage in die Zelle der Abfrage, die Sie ändern möchten, und führen Sie eine der folgenden Aktionen aus. Beachten Sie, dass die Zelle von einem blauen Feld umgeben wird, wenn Sie darauf klicken.
    
   - Geben Sie die neue Abfrage in die Zelle ein. Beachten Sie, dass ein Teil der Abfrage nicht bearbeitet werden kann. Sie müssen die gesamte Abfrage eingeben.
    
      Oder
    
    - Fügt eine neue Abfrage in die Zelle ein. Dabei wird davon ausgegangen, dass Sie den Abfragetext aus einer Datei wie eine Textdatei oder eine Excel-Datei kopiert haben.
    
4. Nachdem Sie auf der Seite **Abfragen** eine oder mehrere Abfragen bearbeitet haben, klicken Sie auf **Speichern**.
    
    Die überarbeitete Abfrage wird in der Spalte **Abfrage** für die ausgewählte Suche angezeigt. 
    
5. Klicken Sie auf **Beenden** , um den Massen Such Editor zu beenden. 
    
6. Wählen Sie auf der Seite **Inhaltssuche** die Suche aus, die Sie bearbeitet haben, und klicken Sie auf Suche **starten** , um die Suche mithilfe der überarbeiteten Abfrage neu zu starten. 
    
Im folgenden finden Sie einige Tipps zum Bearbeiten von Abfragen mithilfe des Massen Such-Editors:
  
- Kopieren Sie die vorhandene Abfrage (mithilfe von **STRG + C** ) in eine Textdatei. Bearbeiten Sie die Abfrage in der Textdatei, kopieren Sie die überarbeitete Abfrage, und fügen Sie Sie (mit **STRG V** ) wieder in die Zelle auf der Seite **Abfragen** ein. 
    
- Sie können auch Abfragen aus anderen Anwendungen (wie Microsoft Word oder Microsoft Excel) kopieren. Beachten Sie jedoch, dass Sie möglicherweise versehentlich nicht unterstützte Zeichen zu einer Abfrage mithilfe des Massen Such-Editors hinzufügen. Die beste Möglichkeit, nicht unterstützte Zeichen zu verhindern, ist das Eingeben der Abfrage in eine Zelle auf der Seite **Abfragen** . Alternativ können Sie eine Abfrage aus Word oder Excel kopieren und in einem Nur-Text-Editor, z. B. Microsoft Editor, in eine Datei einfügen. Speichern Sie dann die Textdatei, und wählen Sie **ANSI** in der Dropdownliste **Codierung** aus. Dadurch werden alle Formatierungen und nicht unterstützten Zeichen entfernt. Anschließend können Sie die Abfrage aus der Textdatei kopieren und in die Seite **Abfragen** einfügen. 
    
  
## <a name="use-the-bulk-search-editor-to-change-content-locations"></a>Verwenden des Massen Such-Editors zum Ändern von Inhaltsspeicherorten

1. Klicken Sie im Massen Such-Editor für eine oder mehrere ausgewählte Suchvorgänge auf **Massen Speicherort-Editor aktivieren**, und klicken Sie dann auf den Link **Standorte** , der auf der Seite angezeigt wird. 
    
    Die folgenden Informationen werden auf der Seite **Speicherorte** des Massen Such-Editors angezeigt. 
    
    ![Klicken Sie auf Massen Speicherort-Editor aktivieren, und klicken Sie dann auf Standorte, um inhaltsspeicherorte hinzuzufügen oder zu entfernen](media/a5a468ce-bd63-4c53-bc37-ff64cf769e59.png)
  
    a. **Zu durchsuchende Postfächer** In diesem Abschnitt wird eine Spalte für jede ausgewählte Inhaltssuche und Zeile für jedes Postfach angezeigt, das in der Suche enthalten ist. Ein Häkchen gibt an, dass das Postfach in der Suche enthalten ist. Sie können einer Suche zusätzliche Postfächer hinzufügen, indem Sie die e-Mail-Adresse des Postfachs in eine leere Zeile eingeben und dann auf das Kontrollkästchen für die Inhaltssuche klicken, der Sie Sie hinzufügen möchten. Sie können auch ein Postfach aus einer Suche entfernen, indem Sie das Kontrollkästchen deaktivieren.
    
    b. **Zu durchsuchende SharePoint-Websites** In diesem Abschnitt wird für jede SharePoint-und OneDrive-Website, die in jeder ausgewählten Inhaltssuche enthalten ist, eine Zeile angezeigt. Ein Häkchen gibt an, dass die Website in der Suche enthalten ist. Sie können einer Suche zusätzliche Websites hinzufügen, indem Sie die URL für die Website in eine leere Zeile eingeben und dann auf das Kontrollkästchen für die Inhaltssuche klicken, der Sie Sie hinzufügen möchten. Sie können auch eine Website aus einer Suche entfernen, indem Sie das Kontrollkästchen deaktivieren.
    
    c. **Weitere Suchoptionen** Dieser Abschnitt gibt an, ob nicht indizierte Elemente und öffentliche Ordner in die Suche einbezogen werden. Um diese einzuschließen, stellen Sie sicher, dass das Kontrollkästchen aktiviert ist. Deaktivieren Sie das Kontrollkästchen, um Sie zu entfernen.
    
2. Nachdem Sie einen oder mehrere Abschnitte auf der Seite **Speicherorte** bearbeitet haben, klicken Sie auf **Speichern**.
    
    Die überarbeiteten inhaltsspeicherorte werden im entsprechenden Abschnitt für die ausgewählten Suchvorgänge angezeigt.
    
3. Klicken Sie auf **Beenden** , um den Massen Such Editor zu beenden. 
    
4. Wählen Sie auf der Seite **Inhaltssuche** die Suche aus, die Sie bearbeitet haben, und klicken Sie auf Suche **starten** , um die Suche mithilfe der überarbeiteten inhaltsspeicherorte neu zu starten. 
    
Im folgenden finden Sie einige Tipps zum Bearbeiten von Inhaltsspeicherorten mithilfe des Massen Such-Editors:
  
- Sie können die Inhaltssuche bearbeiten, um alle Postfächer oder Websites in der Organisation zu durchsuchen, indem Sie im Abschnitt **Postfächer zu durchsuchende** oder zu durchsuchende **SharePoint-Websites** **alle** in eine leere Zeile eingeben und dann auf das Kontrollkästchen klicken. 
    
- Sie können einer oder mehreren Suchvorgängen mehrere inhaltsspeicherorte hinzufügen, indem Sie mehrere Zeilen aus einer Textdatei oder einer Excel-Datei kopieren und Sie dann in einen Abschnitt auf der Seite **Speicherorte** einfügen. Nachdem Sie neue Speicherorte hinzugefügt haben, müssen Sie das Kontrollkästchen für jede Suche aktivieren, der Sie den Speicherort hinzufügen möchten. 
    
    > [!TIP]
    > Um eine Liste der e-Mail-Adressen für alle Benutzer in Ihrer Organisation zu generieren, führen Sie den PowerShell-Befehl in Schritt 2 in [use Content Search aus, um das Postfach und die OneDrive for Business-Website nach einer Liste von Benutzern zu durchsuchen](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md#step2). Oder verwenden Sie das Skript in [Erstellen einer Liste aller OneDrive-Speicherorte in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a) , um eine Liste aller OneDrive für Business-Websites in Ihrer Organisation zu generieren. Beachten Sie, dass Sie die URL für Ihre organization's mysite-Domäne (beispielsweise https://contoso-my.sharepoint.com) an die OneDrive for Business-Websites, die durch das Skript erstellt werden) anfügen müssen. Nachdem Sie eine Liste von e-Mail-Adressen oder OneDrive für Business-Websites haben, können Sie diese kopieren und auf der Seite " **Standorte** " im Massen Such-Editor einfügen. 
  
- Nachdem Sie auf **Speichern** klicken, um die Änderungen im Massen Such Editor zu speichern, wird die e-Mail-Adresse für Postfächer, die Sie einer Suche hinzugefügt haben, überprüft. Wenn die e-Mail-Adresse nicht vorhanden ist, wird eine Fehlermeldung angezeigt, die besagt, dass das Postfach nicht gefunden werden kann. Beachten Sie, dass URLs für Websites nicht validiert werden. 
  

