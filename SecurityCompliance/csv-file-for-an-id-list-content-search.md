---
title: Vorbereiten einer CSV-Datei für ein Inhaltssuche in Office 365-ID-Liste
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Verwenden Sie die Datei Results.csv oder nicht-indizierten Items.csv aus einer vorhandenen Inhaltssuche, um eine ID-Liste-Suche erstellen, die eine bestimmte e-Mail-Nachrichten zurückgibt. -ID-Liste Suche in der Regel verwendet, um Postfachelemente teilweise indizierten zurückzugeben.
ms.openlocfilehash: 28e4a66e5c9be1817881004b1e4b3a3e6d4bfdb9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529846"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a>Vorbereiten einer CSV-Datei für ein Inhaltssuche in Office 365-ID-Liste

Sie können nach bestimmten Postfach e-Mail-Nachrichten und andere Postfachelemente mithilfe einer Liste der Exchange-IDs suchen. Um eine ID-Liste-Suche (formell als eine gezielte Suche bezeichnet) zu erstellen, senden Sie eine durch Trennzeichen getrennten Werten (CSV)-Datei, die bestimmte Postfachelemente zu suchenden identifiziert. Für diese CSV-Datei verwenden Sie die **Results.csv** oder den **Indizierten Items.csv** -Datei, die eingebunden werden, wenn Sie exportieren die Ergebnisse der Inhalt oder ein Inhaltssuche-Bericht aus, und suchen Sie vorhandene Content. Klicken Sie dann bearbeiten Sie eine dieser Dateien an, dass die einzelnen Elemente zum Suchen nach, und erstellen Sie eine neue Suche der ID-Liste und übermitteln die CSV-Datei. 
  
Nachfolgend finden Sie ein schnellen Überblick über den Prozess zum Erstellen einer ID-Liste Suche.
  
1. Erstellen und Ausführen einer neuen oder geführte Inhaltssuche in das Wertpapier &amp; Compliance Center.
    
2. Exportieren Sie die Ergebnisse für die Inhaltssuche oder exportieren Sie den Bericht für die Inhaltssuche. Weitere Informationen finden Sie unter:
    
    - [Exportieren von Suchergebnissen aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md)
    
    - [Exportieren eines Berichts für die Inhaltssuche](export-a-content-search-report.md)
    
3. Bearbeiten Sie der Datei **Results.csv** oder den **Indizierten Items.csv** , und ermitteln Sie die spezifischen Postfach-Elemente, die Sie bei der Suche der ID-Liste einschließen möchten. Finden Sie die [Anweisungen](#prepare-the-csv-file-for-an-id-list-search) für die Vorbereitung einer CSV-Datei für die Suche eine ID-Liste aus. 
    
4. Erstellen Sie eine neue ID-Liste (siehe die [Anweisungen](#create-an-id-list-search)) suchen und übermitteln Sie die CSV-Datei, die Sie vorbereitet. Die Search-Abfrage, die erstellt wird, wird nur für die Elemente in der CSV-Datei ausgewählt gesucht.
    
> [!NOTE]
> ID-Liste Suchvorgänge werden nur für Postfachelemente unterstützt. Sie können nicht SharePoint suchen und diese Dokumente in einer ID OneDrive auflisten suchen. 
  
 **Gründe für das Erstellen einer ID-Liste Suche?** Wenn Sie nicht feststellen sind, ist ein Element auf eine eDiscovery-Anforderung auf Grundlage der Metadaten in den Dateien **Results.csv** oder **Nicht-indizierten Items.csv** reagieren, können Sie eine ID-Liste Suche verwenden, um finden, Vorschau anzeigen Sie, und klicken Sie dann exportieren Sie, dass das Element zu ermitteln, ob es wurde auf die Groß-/Kleinschreibung reagieren, sind Sie untersuchen. -ID-Liste Suche werden in der Regel zum Suchen nach und Zurückgeben von einem bestimmten Satz von nicht indizierten Elementen verwendet. 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a>Vorbereiten der CSV-Datei für die Suche eine ID-Liste

Nachdem Sie die Suchergebnisse oder den Bericht für ein Inhaltssuche exportiert haben, können Sie die folgenden Schritte aus, um die CSV-Datei für eine ID-Liste Suche Vorbereiten Ausführen. Diese CSV-Datei wird jedes Element in der Liste-ID-Suche zu identifizieren.
  
Beachten Sie, dass eine CSV-Datei aus einer Suche, die SharePoint-Websites und OneDrive Konten enthalten können, aber Sie können *nur* Postfachelemente für die Suche eine ID-Liste auswählen. Wenn Sie ein Dokument in SharePoint oder OneDrive auswählen, wird die CSV-Datei Überprüfung fehlschlägt, bei der Erstellung einer ID-Liste Suche. 
  
1. Öffnen Sie die Datei **Results.csv** oder **Nicht-indizierten Items.csv** in Excel. 
    
2. Einfügen einer neuen Spalteninhalts, und nennen Sie sie **ausgewählte**. Es ist unerheblich, in dem Sie die Spalte eingefügt. Zu diesem Zweck erwägen sie zum linken Rand der ersten Spalte eingefügt.
    
3. Geben Sie in der Spalte **ausgewählt** **Ja** in der Zelle, die das Element entspricht, die Sie suchen möchten. Wiederholen Sie diesen Schritt für jedes Element, das Sie suchen möchten. 
    
    > [!IMPORTANT]
    > Wenn Sie die CSV-Datei in Excel öffnen, wird das Datenformat für die **Dokument-ID** -Spalte in **Allgemeine**geändert. Dies führt die Dokument-ID für ein Element in wissenschaftliche Schreibweise anzeigen. Angenommen, Sie verfügen über das Dokument, das ID des "481037338205" als "4.81037E + 11" angezeigt wird zum Ausführen der nächsten Schritte, um das Datenformat der **Dokument-ID** -Spalte in **Anzahl** wiederherzustellenden das richtige Format für die Dokument-ID ändern Wenn Sie dies tun, schlägt fehl, die Suche der ID-Liste, die die CSV-Datei verwendet. 
  
4. Maustaste auf das gesamte **Dokument-ID** -Spalte, und wählen Sie **Zellen formatieren**.
    
5. Klicken Sie im Feld **Kategorie** auf **Zahl**.
    
6. Ändern Sie die Anzahl der Dezimalstellen in **0**, und klicken Sie dann auf **OK** , um die Änderungen zu speichern. Beachten Sie, dass die Werte in der Dokument-ID-Spalte in Zahlen umgewandelt werden. 
    
    Es folgt ein Beispiel für die CSV-Datei, die für die Inhaltssuche eine ID-Liste gesendet werden kann.
    
    ![Beispiel für eine CSV-Datei für eine gezielte Inhaltssuche](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. Die CSV-Datei zu speichern oder **Speichern unter** verwenden, um das Speichern der Datei mit anderen Dateinamen. Werden Sie in beiden Fällen sicher, dass Sie die Datei mit der CSV-Format speichern. 
  
## <a name="create-an-id-list-search"></a>Erstellen einer ID-Liste-Suche

Im nächste Schritt wird zum Erstellen einer neuen ID-Liste Inhaltssuche und übermitteln die CSV-Datei, die Sie im vorherigen Schritt vorbereitet.
  
> [!IMPORTANT]
> Sie sollten eine ID-Liste Suche nicht mehr als 2 Tage nach dem Exportieren die Ergebnisse oder einen Bericht aus einer Inhaltssuche erstellen. Wenn die Suche erzeugt oder melden, in denen mehr als 2 Tage zurückliegt exportiert, sollten Sie die Suchergebnisse oder den Bericht zum Generieren von aktualisierter CSV-Dateien erneut exportieren. Sie können dann vorbereiten eine der aktualisierten CSV-Dateien und verwenden, um eine ID-Liste-Suche erstellen. 
  
1. In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Inhaltssuche**.
    
2. Auf **der Seite,** klicken Sie auf den Pfeil neben ![Symbol hinzufügen](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **neue Suche**, und klicken Sie dann auf **Suchen nach ID-Liste**.
    
    ![Klicken Sie auf Suchen nach ID-Liste von der neuen Suche Dropdown-Liste](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. Klicken Sie auf die flyoutmenü **zum Suchen nach ID-Liste** den Namen der Suche (und optional beschreiben Sie es), und klicken Sie auf **Durchsuchen** , und wählen Sie im vorherigen Schritt die CSV-Datei, die Sie vorbereitet. 
    
    Office 365 versucht, die CSV-Datei zu überprüfen. Wenn die Überprüfung fehlschlägt, wird eine Fehlermeldung angezeigt, die möglicherweise die Überprüfungsfehler bei der Problembehandlung hilfreich. Die CSV-Datei muss erfolgreich überprüft werden, um eine ID-Liste-Suche zu erstellen.
    
4. Datei wird nach der CSV erfolgreich überprüft, klicken Sie auf **Suchen** , um die Suche der ID-Liste zu erstellen. 
    
    Es folgt ein Beispiel der geschätzten Suchergebnisse und die Abfrage, die für die Suche eine ID-Liste generiert wird.
    
    ![Search-Abfrage für eine gezielte Inhaltssuche im Detailbereich](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    Beachten Sie, dass die Anzahl der geschätzten in Statistiken für die ID-Suche angezeigten Elemente übereinstimmen soll, die Anzahl der Elemente, die Sie in der CSV-Datei ausgewählt haben.
    
5. Vorschau oder exportieren Sie die von der ID-Liste Suche zurückgegebenen Elemente.
    
> [!NOTE]
> Wenn Sie ein Postfach nach dem Erstellen einer ID-Liste Suche verschieben, werden nicht die Abfrage für die Suche die angegebenen Elemente zurück. Dies liegt daran die **DocumentId** -Eigenschaft für Postfachelemente werden geändert, wenn ein Postfach verschoben wird. In seltenen Instanz, wenn ein Postfach nach der Erstellung einer ID-Liste Suche verschoben wird, erstellen Sie eine neue Inhaltssuche (oder aktualisieren Sie die Suchergebnisse für die vorhandenen Inhaltssuche) und klicken Sie dann Export der Suche Ergebnisse oder einen Bericht in aktualisierten CSV-Dateien zu generieren, die verwendet werden können  Um eine neue Suche der ID-Liste zu erstellen. 
