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
search.appverid: MOE150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Verwenden Sie die Datei Results.csv oder nicht-indizierten Items.csv aus einer vorhandenen Inhaltssuche, um eine ID-Liste-Suche erstellen, die eine bestimmte e-Mail-Nachrichten zurückgibt. -ID-Liste Suche in der Regel verwendet, um Postfachelemente teilweise indizierten zurückzugeben.
ms.openlocfilehash: 9a7583c8f83626afb8dc0452bf72d834c8a28275
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038278"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a><span data-ttu-id="8b0ce-104">Vorbereiten einer CSV-Datei für ein Inhaltssuche in Office 365-ID-Liste</span><span class="sxs-lookup"><span data-stu-id="8b0ce-104">Prepare a CSV file for an ID list Content Search in Office 365</span></span>

<span data-ttu-id="8b0ce-p102">Sie können nach bestimmten Postfach e-Mail-Nachrichten und andere Postfachelemente mithilfe einer Liste der Exchange-IDs suchen. Um eine ID-Liste-Suche (formell als eine gezielte Suche bezeichnet) zu erstellen, senden Sie eine durch Trennzeichen getrennten Werten (CSV)-Datei, die bestimmte Postfachelemente zu suchenden identifiziert. Für diese CSV-Datei verwenden Sie die **Results.csv** oder den **Indizierten Items.csv** -Datei, die eingebunden werden, wenn Sie exportieren die Ergebnisse der Inhalt oder ein Inhaltssuche-Bericht aus, und suchen Sie vorhandene Content. Klicken Sie dann bearbeiten Sie eine dieser Dateien an, dass die einzelnen Elemente zum Suchen nach, und erstellen Sie eine neue Suche der ID-Liste und übermitteln die CSV-Datei.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p102">You can search for specific mailbox email messages and other mailbox items using a list of Exchange IDs. To create an ID list search (formally called a targeted search), you submit a comma separated value (CSV) file that identifies the specific mailbox items to search for. For this CSV file you use the **Results.csv** file or the **Unindexed Items.csv** file that are included when you export the Content Search results or export a Content Search report from and existing Content Search. Then you edit one of these files to indicate the specific items to search for, and then create a new ID list search and submit the CSV file.</span></span> 
  
<span data-ttu-id="8b0ce-109">Nachfolgend finden Sie ein schnellen Überblick über den Prozess zum Erstellen einer ID-Liste Suche.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-109">Here's a quick overview of the process for creating an ID list search.</span></span>
  
1. <span data-ttu-id="8b0ce-110">Erstellen und Ausführen einer neuen oder geführte Inhaltssuche in das Wertpapier &amp; Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-110">Create and run a new or guided Content Search in the Security &amp; Compliance Center.</span></span>
    
2. <span data-ttu-id="8b0ce-p103">Exportieren Sie die Ergebnisse für die Inhaltssuche oder exportieren Sie den Bericht für die Inhaltssuche. Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p103">Export the content search results or export the content search report. For more information, see:</span></span>
    
    - [<span data-ttu-id="8b0ce-113">Exportieren von Suchergebnissen aus der Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="8b0ce-113">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
    - [<span data-ttu-id="8b0ce-114">Exportieren eines Inhaltssuchberichts</span><span class="sxs-lookup"><span data-stu-id="8b0ce-114">Export a Content Search report</span></span>](export-a-content-search-report.md)
    
3. <span data-ttu-id="8b0ce-p104">Bearbeiten Sie der Datei **Results.csv** oder den **Indizierten Items.csv** , und ermitteln Sie die spezifischen Postfach-Elemente, die Sie bei der Suche der ID-Liste einschließen möchten. Finden Sie die [Anweisungen](#prepare-the-csv-file-for-an-id-list-search) für die Vorbereitung einer CSV-Datei für die Suche eine ID-Liste aus.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p104">Edit the **Results.csv** file or the **Unindexed Items.csv** and identify the specific mailbox items that you want to include in the ID list search. See the [instructions](#prepare-the-csv-file-for-an-id-list-search) for preparing a CSV file for an ID list search.</span></span> 
    
4. <span data-ttu-id="8b0ce-p105">Erstellen Sie eine neue ID-Liste (siehe die [Anweisungen](#create-an-id-list-search)) suchen und übermitteln Sie die CSV-Datei, die Sie vorbereitet. Die Search-Abfrage, die erstellt wird, wird nur für die Elemente in der CSV-Datei ausgewählt gesucht.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p105">Create a new ID list search (see the [instructions](#create-an-id-list-search)) and submit the CSV file that you prepared. The search query that's created will only search for the items selected in the CSV file.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8b0ce-p106">ID-Liste Suchvorgänge werden nur für Postfachelemente unterstützt. Sie können nicht SharePoint suchen und diese Dokumente in einer ID OneDrive auflisten suchen.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p106">ID list searches are only supported for mailbox items. You can't search for SharePoint and OneDrive documents in an ID list search.</span></span> 
  
 <span data-ttu-id="8b0ce-p107">**Gründe für das Erstellen einer ID-Liste Suche?** Wenn Sie nicht feststellen sind, ist ein Element auf eine eDiscovery-Anforderung auf Grundlage der Metadaten in den Dateien **Results.csv** oder **Nicht-indizierten Items.csv** reagieren, können Sie eine ID-Liste Suche verwenden, um finden, Vorschau anzeigen Sie, und klicken Sie dann exportieren Sie, dass das Element zu ermitteln, ob es wurde auf die Groß-/Kleinschreibung reagieren, sind Sie untersuchen. -ID-Liste Suche werden in der Regel zum Suchen nach und Zurückgeben von einem bestimmten Satz von nicht indizierten Elementen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p107">**Why create an ID list search?** If you're unable to determine if an item is responsive to an eDiscovery request based on the metadata in the **Results.csv** or **Unindexed Items.csv** files, you can use an ID list search to find, preview, and then export that item to determine if it's responsive to the case you're investigating. ID list searches are typically used to search for and return a specific set of unindexed items.</span></span> 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a><span data-ttu-id="8b0ce-124">Vorbereiten der CSV-Datei für die Suche eine ID-Liste</span><span class="sxs-lookup"><span data-stu-id="8b0ce-124">Prepare the CSV file for an ID list search</span></span>

<span data-ttu-id="8b0ce-p108">Nachdem Sie die Suchergebnisse oder den Bericht für ein Inhaltssuche exportiert haben, können Sie die folgenden Schritte aus, um die CSV-Datei für eine ID-Liste Suche Vorbereiten Ausführen. Diese CSV-Datei wird jedes Element in der Liste-ID-Suche zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p108">After you export the search results or report for a content search, you can perform the following steps to prepare the CSV file for an ID list search. This CSV file will identify every item in the ID list search.</span></span>
  
<span data-ttu-id="8b0ce-p109">Beachten Sie, dass eine CSV-Datei aus einer Suche, die SharePoint-Websites und OneDrive Konten enthalten können, aber Sie können *nur* Postfachelemente für die Suche eine ID-Liste auswählen. Wenn Sie ein Dokument in SharePoint oder OneDrive auswählen, wird die CSV-Datei Überprüfung fehlschlägt, bei der Erstellung einer ID-Liste Suche.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p109">Note that you can use a CSV file from a search that included SharePoint sites and OneDrive accounts, but you can select  *only*  mailbox items for an ID list search. If you select a document in SharePoint or OneDrive, the CSV file will fail validation when you create an ID list search.</span></span> 
  
1. <span data-ttu-id="8b0ce-129">Öffnen Sie die Datei **Results.csv** oder **Nicht-indizierten Items.csv** in Excel.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-129">Open the **Results.csv** or **Unindexed Items.csv** file in Excel.</span></span> 
    
2. <span data-ttu-id="8b0ce-p110">Einfügen einer neuen Spalteninhalts, und nennen Sie sie **ausgewählte**. Es ist unerheblich, in dem Sie die Spalte eingefügt. Zu diesem Zweck erwägen sie zum linken Rand der ersten Spalte eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p110">Insert a new column and name it **Selected**. It doesn't matter where you insert the column. For convenience, consider inserting it to the left of the first column.</span></span>
    
3. <span data-ttu-id="8b0ce-p111">Geben Sie in der Spalte **ausgewählt** **Ja** in der Zelle, die das Element entspricht, die Sie suchen möchten. Wiederholen Sie diesen Schritt für jedes Element, das Sie suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p111">In the **Selected** column, type **Yes** in the cell that corresponds to the item that you want to search for. Repeat this step for every item that you want to search for.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="8b0ce-p112">Wenn Sie die CSV-Datei in Excel öffnen, wird das Datenformat für die **Dokument-ID** -Spalte in **Allgemeine**geändert. Dies führt die Dokument-ID für ein Element in wissenschaftliche Schreibweise anzeigen. Angenommen, Sie verfügen über das Dokument, das ID des "481037338205" als "4.81037E + 11" angezeigt wird zum Ausführen der nächsten Schritte, um das Datenformat der **Dokument-ID** -Spalte in **Anzahl** wiederherzustellenden das richtige Format für die Dokument-ID ändern Wenn Sie dies tun, schlägt fehl, die Suche der ID-Liste, die die CSV-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p112">When you open the CSV file in Excel, the data format for the **Document ID** column is changed to **General**. This results in displaying the document ID for an item in scientific notation. For example, the document ID of "481037338205" is displayed as "4.81037E+11" You have to perform the next steps to change the data format of the **Document ID** column to **Number** to restore the correct format for the document ID. If you don't do this, the ID list search that uses the CSV file will fail.</span></span> 
  
4. <span data-ttu-id="8b0ce-139">Maustaste auf das gesamte **Dokument-ID** -Spalte, und wählen Sie **Zellen formatieren**.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-139">Right-click the entire **Document ID** column and select **Format Cells**.</span></span>
    
5. <span data-ttu-id="8b0ce-140">Klicken Sie im Feld **Kategorie** auf **Zahl**.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-140">In the **Category** box, click **Number**.</span></span>
    
6. <span data-ttu-id="8b0ce-p113">Ändern Sie die Anzahl der Dezimalstellen in **0**, und klicken Sie dann auf **OK** , um die Änderungen zu speichern. Beachten Sie, dass die Werte in der Dokument-ID-Spalte in Zahlen umgewandelt werden.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p113">Change the number of decimal places to **0**, and then click **OK** to save your changes. Notice that the values in the Document ID column are changed to numbers.</span></span> 
    
    <span data-ttu-id="8b0ce-143">Es folgt ein Beispiel für die CSV-Datei, die für die Inhaltssuche eine ID-Liste gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-143">Here's an example of the a CSV file that's ready to be submitted for a ID list content search.</span></span>
    
    ![Beispiel für eine CSV-Datei für eine gezielte Inhaltssuche](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. <span data-ttu-id="8b0ce-p114">Die CSV-Datei zu speichern oder **Speichern unter** verwenden, um das Speichern der Datei mit anderen Dateinamen. Werden Sie in beiden Fällen sicher, dass Sie die Datei mit der CSV-Format speichern.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p114">Save the CSV file or use **Save As** to the save the file with different file name. In both cases, be sure to save the file with the CSV format.</span></span> 
  
## <a name="create-an-id-list-search"></a><span data-ttu-id="8b0ce-147">Erstellen einer ID-Liste-Suche</span><span class="sxs-lookup"><span data-stu-id="8b0ce-147">Create an ID list search</span></span>

<span data-ttu-id="8b0ce-148">Im nächste Schritt wird zum Erstellen einer neuen ID-Liste Inhaltssuche und übermitteln die CSV-Datei, die Sie im vorherigen Schritt vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-148">The next step is to create a new ID list Content Search and submit the CSV file that you prepared in the previous step.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8b0ce-p115">Sie sollten eine ID-Liste Suche nicht mehr als 2 Tage nach dem Exportieren die Ergebnisse oder einen Bericht aus einer Inhaltssuche erstellen. Wenn die Suche erzeugt oder melden, in denen mehr als 2 Tage zurückliegt exportiert, sollten Sie die Suchergebnisse oder den Bericht zum Generieren von aktualisierter CSV-Dateien erneut exportieren. Sie können dann vorbereiten eine der aktualisierten CSV-Dateien und verwenden, um eine ID-Liste-Suche erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p115">You should create an ID list search no more than 2 days after exporting the results or report from a Content Search. If the search results or report where exported more than 2 days ago, you should re-export the search results or report to generate updated CSV files. Then you can prepare one of the updated CSV files and use it to create an ID list search.</span></span> 
  
1. <span data-ttu-id="8b0ce-152">In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Inhaltssuche**.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-152">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Content search**.</span></span>
    
2. <span data-ttu-id="8b0ce-153">Auf **der Seite,** klicken Sie auf den Pfeil neben ![Symbol hinzufügen](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **neue Suche**, und klicken Sie dann auf **Suchen nach ID-Liste**.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-153">On the **Search** page, click the arrow next to ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**, and then click **Search by ID List**.</span></span>
    
    ![Klicken Sie auf Suchen nach ID-Liste von der neuen Suche Dropdown-Liste](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. <span data-ttu-id="8b0ce-155">Klicken Sie auf die flyoutmenü **zum Suchen nach ID-Liste** den Namen der Suche (und optional beschreiben Sie es), und klicken Sie auf **Durchsuchen** , und wählen Sie im vorherigen Schritt die CSV-Datei, die Sie vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-155">On the **Search by ID List** flyout, name the search (and optionally describe it) and then click **Browse** and select the CSV file that you prepared in the previous step.</span></span> 
    
    <span data-ttu-id="8b0ce-p116">Office 365 versucht, die CSV-Datei zu überprüfen. Wenn die Überprüfung fehlschlägt, wird eine Fehlermeldung angezeigt, die möglicherweise die Überprüfungsfehler bei der Problembehandlung hilfreich. Die CSV-Datei muss erfolgreich überprüft werden, um eine ID-Liste-Suche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p116">Office 365 attempts to validate the CSV file. If the validation is unsuccessful, an error message is displayed that might help you troubleshoot the validation errors. The CSV file has to be successfully validated to create an ID list search.</span></span>
    
4. <span data-ttu-id="8b0ce-159">Datei wird nach der CSV erfolgreich überprüft, klicken Sie auf **Suchen** , um die Suche der ID-Liste zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-159">After the CSV file is successfully validated, click **Search** to create the ID list search.</span></span> 
    
    <span data-ttu-id="8b0ce-160">Es folgt ein Beispiel der geschätzten Suchergebnisse und die Abfrage, die für die Suche eine ID-Liste generiert wird.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-160">Here's an example of the estimated search results and the query that's generated for an ID list search.</span></span>
    
    ![Search-Abfrage für eine gezielte Inhaltssuche im Detailbereich](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    <span data-ttu-id="8b0ce-162">Beachten Sie, dass die Anzahl der geschätzten in Statistiken für die ID-Suche angezeigten Elemente übereinstimmen soll, die Anzahl der Elemente, die Sie in der CSV-Datei ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-162">Note that the number of estimated items displayed in statistics for the ID search should match the number of items that you selected in the CSV file.</span></span>
    
5. <span data-ttu-id="8b0ce-163">Vorschau oder exportieren Sie die von der ID-Liste Suche zurückgegebenen Elemente.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-163">Preview or export the items returned by the ID list search.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8b0ce-p117">Wenn Sie ein Postfach nach dem Erstellen einer ID-Liste Suche verschieben, werden nicht die Abfrage für die Suche die angegebenen Elemente zurück. Dies liegt daran die **DocumentId** -Eigenschaft für Postfachelemente werden geändert, wenn ein Postfach verschoben wird. In seltenen Instanz, wenn ein Postfach nach der Erstellung einer ID-Liste Suche verschoben wird, erstellen Sie eine neue Inhaltssuche (oder aktualisieren Sie die Suchergebnisse für die vorhandenen Inhaltssuche) und klicken Sie dann Export der Suche Ergebnisse oder einen Bericht in aktualisierten CSV-Dateien zu generieren, die verwendet werden können  Um eine neue Suche der ID-Liste zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8b0ce-p117">If you move a mailbox after creating an ID list search, the query for the search won't return the specified items. That's because the **DocumentId** property for mailbox items are changed when a mailbox is moved. In the rare instance when a mailbox is moved after you create an ID list search, you should create a new content search (or update the search results for the existing content search) and then export the search results or report to generate updated CSV files that can be used to create a new ID list search.</span></span> 
