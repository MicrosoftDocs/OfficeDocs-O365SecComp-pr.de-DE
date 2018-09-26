---
title: Massenbearbeitung Content-Suche in der Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/29/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 39e4654a-9588-41f6-892b-c33ab57bfbe2
description: Verwenden des Bulk Search-Editors in die Office 365-Sicherheit &amp; Compliance Center, um die Abfrage und Inhalte Speicherorte für eine oder mehrere Inhalte Suchvorgänge schnell zu ändern.
ms.openlocfilehash: 9d6d48ff42bb3c99a30b9da1020253a5af24679b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038178"
---
# <a name="bulk-edit-content-searches-in-the-office-365-security-amp-compliance-center"></a>Massenbearbeitung Content-Suche in der Office 365-Sicherheit &amp; Compliance Center

Sie können den Massen Search-Editor in die Office 365-Sicherheit &amp; Compliance Center, um mehrere Content-Suche zur selben Zeit bearbeiten. Mit diesem Tool können Sie schnell die Abfrage- und Inhalte Speicherorte für eine oder mehrere Suchvorgänge ändern. Können Sie führen die Suchvorgänge erneut aus, und rufen Sie neue geschätzten Suchergebnisse für die überarbeiteten suchen. Im Editor können Sie Abfragen und Speicherorte für Inhalte aus einer Microsoft Excel-Datei oder eine Textdatei kopieren und einfügen. Dies bedeutet, dass Sie das Tool Suchstatistik verwenden können, Anzeigen von Statistiken für einen oder mehrere Suchvorgänge, exportieren die Statistiken in eine CSV-Datei, in dem Sie die Abfragen und Speicherorte für Inhalte in Excel bearbeiten können. Klicken Sie dann verwenden Sie den Massen Search-Editor, der überarbeiteten Abfragen und Speicherorte für Inhalte für die Suchvorgänge hinzuzufügen. Nachdem Sie einen oder mehrere Suchvorgänge bearbeitet haben, können Sie sie neu starten und neue geschätzten Suchergebnisse erhalten möchten.
  
Weitere Informationen zur Verwendung des Tools Suchstatistik finden Sie unter [schlüsselwortstatistiken für die Inhaltssuche Ergebnisse anzeigen](view-keyword-statistics-for-content-search.md).
  
## <a name="use-the-bulk-search-editor-to-change-queries"></a>Ändern der Abfragen mithilfe des Bulk-Search-Editors

1. In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Inhaltssuche**.
    
2. In der Liste der Suchvorgänge, wählen Sie eine oder mehrere Suchen und dann auf **Bulk Suche Editor** ![Schaltfläche Bulk Suche Editor](media/1ddb3d18-2f00-4a7b-98a6-817ca5ec7014.png).
    
    ![Wählen Sie einen oder mehrere Suchvorgänge aus, und klicken Sie auf Bulk Search-editor](media/600c9716-89a2-4451-b111-fa7cfaad2006.png)
  
    Die folgende Informationen wird auf der Seite **Abfragen** des Bulk Search-Editors angezeigt. 
    
    ![Massen Suchseite Editor zeigt die Abfragen für die ausgewählten suchen](media/189659af-cc78-4479-b0bc-a93decad2f6c.png)
  
    a. die **Suche** Spalte zeigt den Namen des Content-Suche. Wie bereits zuvor erwähnt können Sie die Abfrage für mehrere Suchvorgänge bearbeiten. 
    
    b in der Spalte **Abfrage** zeigt die Abfrage für die Inhaltssuche in der Spalte **Suche** aufgeführt. Wenn die Abfrage mit dem Listenfeature Schlüsselwort erstellt wurde, werden die Schlüsselwörter durch den Text getrennt ** `(c:s)` **. Dies gibt an, dass die Schlüsselwörter mithilfe der **OR** -Operator verbunden sind. Darüber hinaus enthält die Abfrage Bedingungen, die Schlüsselwörter und die Bedingungen werden getrennt durch den Text ** `(c:c)` **. Dies gibt an, dass die Keywords (oder Schlüsselwort Phasen) an die Bedingungen durch den **AND** -Operator verbunden sind. Beispielsweise in der vorherigen Screenshot der für die Suche ContosoSearch1, der KQL-Abfrage, die entspricht `customer (c:s) pricing(c:c)(date=2000-01-01..2016-09-30)` wäre `(customer OR pricing) AND (date=2002-01-01..2016-09-30)`.
    
3. Um eine Abfrage zu bearbeiten, klicken Sie auf die Zelle der Abfrage, die Sie ändern, und führen Sie einen der folgenden Schritte möchten. Beachten Sie, dass die Zelle durch eine blaue Feld eingeschlossen wird, wenn Sie darauf klicken.
    
   - Geben Sie die neue Abfrage in der Zelle. Beachten Sie, dass Sie einen Teil der Abfrage nicht bearbeiten können. Sie müssen die gesamte Abfrage eingeben.
    
      Oder
    
    - Fügen Sie eine neue Abfrage in der Zelle. Dabei wird vorausgesetzt, dass Sie den Abfragetext aus einer Datei, wie eine Textdatei oder einer Excel-Datei kopiert haben.
    
4. Nachdem Sie eine oder mehrere Abfragen auf der Seite **Abfragen** bearbeitet haben, klicken Sie auf **Speichern**.
    
    Die überarbeitete Abfrage wird in der Spalte **Abfrage** für die ausgewählte Suche angezeigt. 
    
5. Klicken Sie auf **Schließen** , um den Massen Search-Editor zu schließen. 
    
6. Klicken Sie auf der Seite **Inhaltssuche** wählen Sie die Suche, die Sie bearbeitet haben, und klicken Sie auf Suche **Starten** , um die Suche mithilfe der überarbeiteten Abfrage neu zu starten. 
    
Hier sind einige Tipps für die Bearbeitung von Abfragen mit dem Bulk Search-Editor ein:
  
- Kopieren Sie die vorhandene Abfrage in einer Textdatei (mithilfe von **STRG-C** ). Bearbeiten Sie die Abfrage in der Textdatei, und kopieren Sie die überarbeitete Abfrage und fügen Sie ihn (mit **STRG V** ) wieder in die Zelle auf der Seite **Abfragen** . 
    
- Sie können auch Abfragen aus anderen Programmen (wie Microsoft Word oder Microsoft Excel) kopieren. Beachten Sie jedoch, dass Sie nicht unterstützte Zeichen versehentlich auf eine Abfrage mit dem Bulk Search-Editor Hinzufügen. Die beste Möglichkeit zum verhindern, dass nicht unterstützte Zeichen ist, geben die Abfrage in einer Zelle auf der Seite **Abfragen** . Alternativ können Sie eine Abfrage aus Word oder Excel kopieren und fügen Sie ihn an der Datei in einem nur-Text-Editor wie Microsoft Notepad. Klicken Sie dann speichern Sie die Datei, und wählen Sie in der Dropdownliste **Codierung** **ANSI** . Dadurch werden alle Formatierungen und nicht unterstützten Zeichen entfernt. Sie können dann kopieren und fügen Sie die Abfrage aus der Textdatei auf der Seite **Abfragen** . 
    
  
## <a name="use-the-bulk-search-editor-to-change-content-locations"></a>Verwenden des Bulk Search-Editors so ändern Sie die Speicherorte für Inhalte

1. Massen suchen Sie im Editor für eine oder mehrere ausgewählte Suchvorgänge auf **Aktivieren Bulk Speicherort-Editor**, und klicken Sie dann auf den Link **Speicherorte** , der auf der Seite angezeigt wird. 
    
    Die folgende Informationen wird auf der Seite **Speicherorte** der Bulk Search-Editor angezeigt. 
    
    ![Klicken Sie auf Enable Bulk Speicherort-Editor, und klicken Sie auf Speicherorte zum Hinzufügen oder Entfernen von Speicherorte für Inhalte](media/a5a468ce-bd63-4c53-bc37-ff64cf769e59.png)
  
    a. **Postfächer suchen**in diesem Abschnitt zeigt eine Spalte für jede ausgewählte Inhaltssuche und eine Zeile für jedes Postfach, das in der Suche enthalten ist. Ein Häkchen zeigt an, dass das Postfach in der Suche enthalten ist. Sie können zusätzliche Postfächer mit einem Search hinzufügen, indem Sie die e-Mail-Adresse des Postfachs in eine leere Zeile eingeben und dann auf das Kontrollkästchen für die Inhaltssuche, die Sie hinzufügen möchten. Oder Sie können ein Postfach aus einer Suche entfernen, indem Sie das Kontrollkästchen deaktivieren.
    
    **SharePoint-Websites zu suchen**, die in diesem Abschnitt eine Zeile für jeden Standort SharePoint- und OneDrive anzeigt, die in den einzelnen enthalten b ausgewählt Inhaltssuche. Ein Häkchen zeigt an, dass die Website in die Suche einbezogen wird. Sie können zusätzliche Websites mit einem Search durch Eingabe der URL für die Website in einer leeren Zeile hinzufügen und dann und klicken Sie auf das Kontrollkästchen für die Inhaltssuche die gewünschten hinzufügen zu. Oder Sie können eine Website von einer Suche entfernen, indem Sie das Kontrollkästchen deaktivieren.
    
    c. **andere Optionen zur Suche**in diesem Abschnitt gibt an, ob Öffentliche Ordner und nicht-indizierten Elemente in der Suche enthalten sind. Diese aufnehmen möchten, stellen Sie sicher, dass das Kontrollkästchen aktiviert ist. Deaktivieren Sie das Kontrollkästchen, um diese zu entfernen.
    
2. Nachdem Sie eine oder mehrere der in den Abschnitten auf der Seite **Speicherorte** bearbeitet haben, klicken Sie auf **Speichern**.
    
    Die überarbeitete Speicherorte für Inhalte werden im entsprechenden Abschnitt für die ausgewählten suchen angezeigt.
    
3. Klicken Sie auf **Schließen** , um den Massen Search-Editor zu schließen. 
    
4. Klicken Sie auf der Seite **Durchsuchen von Inhalten** wählen Sie die Suche, die Sie bearbeitet haben, und klicken Sie auf Suche **Starten** , um die Suche mit der überarbeiteten Speicherorte für Inhalte neu zu starten. 
    
Hier sind einige Tipps zur Bearbeitung Speicherorte für Inhalte mit dem Bulk Search-Editor ein:
  
- Sie können die Content-Suche, um alle Postfächer oder Websites in der Organisation zu suchen, indem Sie **Alle** in eine leere Zeile im Abschnitt **Postfächer zu suchen** oder **SharePoint-Websites suchen** eingeben und dann auf das Kontrollkästchen bearbeiten. 
    
- Sie können mehrere Speicherorte für Inhalte für eine oder mehrere Suchvorgänge hinzufügen, indem mehrere Zeilen aus einer Textdatei oder einer Excel-Datei kopiert und dann zu einem Abschnitt auf der Seite **Speicherorte** eingefügt haben. Nachdem Sie neue Standorte hinzugefügt haben, müssen Sie unbedingt das Kontrollkästchen bei jeder Suche, dem Sie den Speicherort hinzufügen möchten. 
    
    > [!TIP]
    > Um eine Liste der e-Mail-Adressen für alle Benutzer in Ihrer Organisation generiert werden soll, führen Sie den PowerShell-Befehl in Schritt2 in [Content suchen verwenden, um das Postfach und die OneDrive for Business-Website für eine Liste von Benutzern suchen](search-the-mailbox-and-onedrive-for-business-for-a-list-of-users.md#step2). Oder verwenden Sie das Skript in [Erstellen Sie eine Liste mit allen Speicherorten von OneDrive in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a) , um eine Liste mit allen OneDrive for Business-Websites in Ihrer Organisation zu generieren. Beachten Sie, dass Sie fügen Sie die URL für müssen Ihre des-MeineWebsite Domäne Organisation (beispielsweise https://contoso-my.sharepoint.com) zu den OneDrive for Business-Websites, die von dem Skript erstellt wird. Nachdem Sie die Liste der e-Mail-Adressen oder OneDrive for Business-Websites haben, können Sie kopieren und fügen sie auf der Seite **Speicherorte** im Bulk Search-Editor. 
  
- Klicken Sie auf **Speichern** , um die Änderungen im Bulk Search-Editor zu speichern, wird die e-Mail-Adresse für Postfächer, die Sie eine Suche hinzugefügt überprüft werden. Wenn die e-Mail-Adresse nicht vorhanden ist, wird eine Fehlermeldung angezeigt, dass das Postfach nicht gefunden werden kann. Beachten Sie, dass die URLs für Websites überprüft werden nicht. 
  

