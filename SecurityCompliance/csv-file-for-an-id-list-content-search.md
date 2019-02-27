---
title: Vorbereiten einer CSV-Datei für eine Inhaltssuche in der ID-Liste in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 3/21/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: 82c97bb4-2b64-4edc-804d-cedbda525d22
description: Verwenden Sie die Datei results. CSV oder unindexed Items. CSV aus einer vorhandenen Inhaltssuche, um eine ID-Listensuche zu erstellen, die bestimmte e-Mail-Nachrichten zurückgibt. ID-Listen suchen werden normalerweise verwendet, um teilweise indizierte Postfachelemente zurückzugeben.
ms.openlocfilehash: 558a8512ed133995b2cc1d0d8b78fd7f08d11168
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296738"
---
# <a name="prepare-a-csv-file-for-an-id-list-content-search-in-office-365"></a><span data-ttu-id="79782-104">Vorbereiten einer CSV-Datei für eine Inhaltssuche in der ID-Liste in Office 365</span><span class="sxs-lookup"><span data-stu-id="79782-104">Prepare a CSV file for an ID list Content Search in Office 365</span></span>

<span data-ttu-id="79782-p102">Sie können mithilfe einer Liste von Exchange-IDs nach bestimmten e-Mail-Nachrichten und anderen Postfachelementen suchen. Um eine ID-Listensuche (formell als gezielte Suche bezeichnet) zu erstellen, übermitteln Sie eine CSV-Datei (Comma Separated Value), die die zu suchenden Postfachelemente identifiziert. Für diese CSV-Datei verwenden Sie die Datei **results. CSV** oder die unindizierte **Items. CSV** -Datei, die beim Exportieren der Inhalts Suchergebnisse oder beim Exportieren eines Inhalts Suchberichts aus einer vorhandenen Inhaltssuche enthalten sind. Bearbeiten Sie dann eine dieser Dateien, um die zu suchenden Elemente anzugeben, und erstellen Sie dann eine neue ID-Listensuche, und übermitteln Sie die CSV-Datei.</span><span class="sxs-lookup"><span data-stu-id="79782-p102">You can search for specific mailbox email messages and other mailbox items using a list of Exchange IDs. To create an ID list search (formally called a targeted search), you submit a comma separated value (CSV) file that identifies the specific mailbox items to search for. For this CSV file you use the **Results.csv** file or the **Unindexed Items.csv** file that are included when you export the Content Search results or export a Content Search report from and existing Content Search. Then you edit one of these files to indicate the specific items to search for, and then create a new ID list search and submit the CSV file.</span></span> 
  
<span data-ttu-id="79782-109">Im folgenden finden Sie eine kurze Übersicht über das Verfahren zum Erstellen einer ID-Listensuche.</span><span class="sxs-lookup"><span data-stu-id="79782-109">Here's a quick overview of the process for creating an ID list search.</span></span>
  
1. <span data-ttu-id="79782-110">Erstellen Sie eine neue oder geführte Inhaltssuche im Security &amp; Compliance Center, und führen Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="79782-110">Create and run a new or guided Content Search in the Security &amp; Compliance Center.</span></span>
    
2. <span data-ttu-id="79782-p103">Exportieren der Inhalts Suchergebnisse oder Exportieren des Inhalts Suchberichts. Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="79782-p103">Export the content search results or export the content search report. For more information, see:</span></span>
    
    - [<span data-ttu-id="79782-113">Exportieren von Inhalts Suchergebnissen aus dem Office 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="79782-113">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
    - [<span data-ttu-id="79782-114">Exportieren eines Inhaltssuchberichts</span><span class="sxs-lookup"><span data-stu-id="79782-114">Export a Content Search report</span></span>](export-a-content-search-report.md)
    
3. <span data-ttu-id="79782-p104">Bearbeiten Sie die Datei **results. CSV** oder die unindizierten **Elemente. CSV** , und identifizieren Sie die bestimmten Postfachelemente, die Sie in die ID-Listensuche einbeziehen möchten. Weitere Informationen finden Sie in den [Anweisungen](#prepare-the-csv-file-for-an-id-list-search) zum Vorbereiten einer CSV-Datei für eine ID-Listensuche.</span><span class="sxs-lookup"><span data-stu-id="79782-p104">Edit the **Results.csv** file or the **Unindexed Items.csv** and identify the specific mailbox items that you want to include in the ID list search. See the [instructions](#prepare-the-csv-file-for-an-id-list-search) for preparing a CSV file for an ID list search.</span></span> 
    
4. <span data-ttu-id="79782-p105">Erstellen Sie eine neue ID-Listensuche (siehe die [Anweisungen](#create-an-id-list-search)), und übermitteln Sie die von Ihnen VORBEREITETE CSV-Datei. Die Suchabfrage, die erstellt wird, sucht nur nach den in der CSV-Datei ausgewählten Elementen.</span><span class="sxs-lookup"><span data-stu-id="79782-p105">Create a new ID list search (see the [instructions](#create-an-id-list-search)) and submit the CSV file that you prepared. The search query that's created will only search for the items selected in the CSV file.</span></span>
    
> [!NOTE]
> <span data-ttu-id="79782-p106">ID-Listen suchen werden nur für Postfachelemente unterstützt. Sie können nicht in einer ID-Listensuche nach SharePoint-und OneDrive-Dokumenten suchen.</span><span class="sxs-lookup"><span data-stu-id="79782-p106">ID list searches are only supported for mailbox items. You can't search for SharePoint and OneDrive documents in an ID list search.</span></span> 
  
 <span data-ttu-id="79782-p107">**Gründe für das Erstellen einer ID-Listensuche** Wenn Sie nicht ermitteln können, ob ein Element auf eine eDiscovery-Anforderung basierend auf den Metadaten in den Dateien " **results.** CSV" oder "unindiziered **Items. CSV** " reagiert, verwenden Sie eine ID-Listensuche, um dieses Element zu suchen, in der Vorschau anzuzeigen und es dann zu exportieren, um zu ermitteln, ob es reagiert auf den Fall, den Sie untersuchen. ID-Listen suchen werden normalerweise verwendet, um nach einem bestimmten Satz von nicht indizierten Elementen zu suchen und diesen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="79782-p107">**Why create an ID list search?** If you're unable to determine if an item is responsive to an eDiscovery request based on the metadata in the **Results.csv** or **Unindexed Items.csv** files, you can use an ID list search to find, preview, and then export that item to determine if it's responsive to the case you're investigating. ID list searches are typically used to search for and return a specific set of unindexed items.</span></span> 
  
## <a name="prepare-the-csv-file-for-an-id-list-search"></a><span data-ttu-id="79782-124">Vorbereiten der CSV-Datei für eine ID-Listensuche</span><span class="sxs-lookup"><span data-stu-id="79782-124">Prepare the CSV file for an ID list search</span></span>

<span data-ttu-id="79782-p108">Nachdem Sie die Suchergebnisse oder den Bericht für eine Inhaltssuche exportiert haben, können Sie die folgenden Schritte ausführen, um die CSV-Datei für eine ID-Listensuche vorzubereiten. Diese CSV-Datei identifiziert jedes Element in der ID-Listensuche.</span><span class="sxs-lookup"><span data-stu-id="79782-p108">After you export the search results or report for a content search, you can perform the following steps to prepare the CSV file for an ID list search. This CSV file will identify every item in the ID list search.</span></span>
  
<span data-ttu-id="79782-p109">Beachten Sie, dass Sie eine CSV-Datei aus einer Suche mit SharePoint-Websites und OneDrive-Konten verwenden können, aber Sie können *nur* Postfachelemente für eine ID-Listensuche auswählen. Wenn Sie ein Dokument in SharePoint oder OneDrive auswählen, schlägt die Überprüfung der CSV-Datei fehl, wenn Sie eine ID-Listensuche erstellen.</span><span class="sxs-lookup"><span data-stu-id="79782-p109">Note that you can use a CSV file from a search that included SharePoint sites and OneDrive accounts, but you can select  *only*  mailbox items for an ID list search. If you select a document in SharePoint or OneDrive, the CSV file will fail validation when you create an ID list search.</span></span> 
  
1. <span data-ttu-id="79782-129">Öffnen Sie die Datei **results. CSV** oder unindexed **Items. CSV** in Excel.</span><span class="sxs-lookup"><span data-stu-id="79782-129">Open the **Results.csv** or **Unindexed Items.csv** file in Excel.</span></span> 
    
2. <span data-ttu-id="79782-p110">Fügt eine neue Spalte und einen Namen \*\*\*\* ein. Es spielt keine Rolle, wo Sie die Spalte einfügen. Zur Vereinfachung empfiehlt es sich, es Links von der ersten Spalte einzufügen.</span><span class="sxs-lookup"><span data-stu-id="79782-p110">Insert a new column and name it **Selected**. It doesn't matter where you insert the column. For convenience, consider inserting it to the left of the first column.</span></span>
    
3. <span data-ttu-id="79782-p111">Geben Sie in der **ausgewählten** Spalte **Ja** in der Zelle ein, die dem Element entspricht, nach dem Sie suchen möchten. Wiederholen Sie diesen Schritt für jedes Element, nach dem Sie suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="79782-p111">In the **Selected** column, type **Yes** in the cell that corresponds to the item that you want to search for. Repeat this step for every item that you want to search for.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="79782-p112">Wenn Sie die CSV-Datei in Excel öffnen, wird das Datenformat für die **Dokument-ID-** Spalte in **Allgemein**geändert. Dadurch wird die Dokument-ID für ein Element in wissenschaftlicher Schreibweise angezeigt. Die Dokument-ID "481037338205" wird beispielsweise als "4.81037 E + 11" angezeigt, wenn Sie die nächsten Schritte ausführen müssen, um das Datenformat der **Dokument-ID-** Spalte in **Number** zu ändern, um das richtige Format für die Dokument-ID wiederherzustellen. Wenn Sie dies nicht tun, schlägt die ID-Listensuche, die die CSV-Datei verwendet, fehl.</span><span class="sxs-lookup"><span data-stu-id="79782-p112">When you open the CSV file in Excel, the data format for the **Document ID** column is changed to **General**. This results in displaying the document ID for an item in scientific notation. For example, the document ID of "481037338205" is displayed as "4.81037E+11" You have to perform the next steps to change the data format of the **Document ID** column to **Number** to restore the correct format for the document ID. If you don't do this, the ID list search that uses the CSV file will fail.</span></span> 
  
4. <span data-ttu-id="79782-139">Klicken Sie mit der rechten Maustaste auf die gesamte **Dokument-ID** -Spalte, und wählen Sie **Zellen formatieren**aus.</span><span class="sxs-lookup"><span data-stu-id="79782-139">Right-click the entire **Document ID** column and select **Format Cells**.</span></span>
    
5. <span data-ttu-id="79782-140">Klicken Sie im Feld **Kategorie** auf **Zahl**.</span><span class="sxs-lookup"><span data-stu-id="79782-140">In the **Category** box, click **Number**.</span></span>
    
6. <span data-ttu-id="79782-p113">Ändern Sie die Anzahl der Dezimalstellen in **0**, und klicken Sie dann auf **OK** , um die Änderungen zu speichern. Beachten Sie, dass die Werte in der Spalte Dokument-ID in Zahlen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="79782-p113">Change the number of decimal places to **0**, and then click **OK** to save your changes. Notice that the values in the Document ID column are changed to numbers.</span></span> 
    
    <span data-ttu-id="79782-143">Nachfolgend finden Sie ein Beispiel für eine CSV-Datei, die für die Inhaltssuche einer ID-Liste eingereicht werden kann.</span><span class="sxs-lookup"><span data-stu-id="79782-143">Here's an example of the a CSV file that's ready to be submitted for a ID list content search.</span></span>
    
    ![Beispiel einer CSV-Datei für eine gezielte Inhaltssuche](media/8371b8cb-1638-496e-9be1-fe1565757d67.png)
  
7. <span data-ttu-id="79782-p114">Speichern Sie die CSV-Datei \*\*\*\* , oder speichern Sie die Datei mit einem anderen Dateinamen speichern unter. In beiden Fällen müssen Sie die Datei im CSV-Format speichern.</span><span class="sxs-lookup"><span data-stu-id="79782-p114">Save the CSV file or use **Save As** to the save the file with different file name. In both cases, be sure to save the file with the CSV format.</span></span> 
  
## <a name="create-an-id-list-search"></a><span data-ttu-id="79782-147">Erstellen einer ID-Listensuche</span><span class="sxs-lookup"><span data-stu-id="79782-147">Create an ID list search</span></span>

<span data-ttu-id="79782-148">Im nächsten Schritt erstellen Sie eine neue ID-Listeninhalts Suche und übermitteln die CSV-Datei, die Sie im vorherigen Schritt vorbereitet haben.</span><span class="sxs-lookup"><span data-stu-id="79782-148">The next step is to create a new ID list Content Search and submit the CSV file that you prepared in the previous step.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="79782-p115">Sie sollten eine ID-Listensuche nicht mehr als 2 Tage nach dem Export der Ergebnisse oder Berichte aus einer Inhaltssuche erstellen. Wenn die Suchergebnisse oder der Bericht vor mehr als zwei Tagen exportiert wurden, sollten Sie die Suchergebnisse oder den Bericht erneut exportieren, um aktualisierte CSV-Dateien zu generieren. Anschließend können Sie eine der aktualisierten CSV-Dateien vorbereiten und diese verwenden, um eine ID-Listensuche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="79782-p115">You should create an ID list search no more than 2 days after exporting the results or report from a Content Search. If the search results or report where exported more than 2 days ago, you should re-export the search results or report to generate updated CSV files. Then you can prepare one of the updated CSV files and use it to create an ID list search.</span></span> 
  
1. <span data-ttu-id="79782-152">Navigieren Sie im &amp; Security Compliance Center zu Such \*\*Suche &amp; \*\* \> - **Inhaltssuche**.</span><span class="sxs-lookup"><span data-stu-id="79782-152">In the Security &amp; Compliance Center, go to **Search &amp; investigation** \> **Content search**.</span></span>
    
2. <span data-ttu-id="79782-153">Klicken Sie auf der Seite **Suchen** auf den Pfeil neben ![Symbol](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **neue Suche**hinzufügen, und klicken Sie dann auf **nach ID-Liste suchen**.</span><span class="sxs-lookup"><span data-stu-id="79782-153">On the **Search** page, click the arrow next to ![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) **New search**, and then click **Search by ID List**.</span></span>
    
    ![Klicken Sie in der Dropdownliste neue Suche auf nach ID-Liste suchen.](media/e65f9942-09b2-4127-865e-e64029a590df.png)
  
3. <span data-ttu-id="79782-155">Geben Sie im Flyout **Suche nach ID-Liste** die Suche an (und beschreiben Sie Sie optional), und klicken Sie dann auf **Durchsuchen** , und wählen Sie die CSV-Datei aus, die Sie im vorherigen Schritt vorbereitet haben.</span><span class="sxs-lookup"><span data-stu-id="79782-155">On the **Search by ID List** flyout, name the search (and optionally describe it) and then click **Browse** and select the CSV file that you prepared in the previous step.</span></span> 
    
    <span data-ttu-id="79782-p116">Office 365 versucht, die CSV-Datei zu überprüfen. Wenn die Überprüfung nicht erfolgreich ist, wird eine Fehlermeldung angezeigt, die Ihnen bei der Behandlung der Validierungsfehler helfen kann. Die CSV-Datei muss erfolgreich validiert werden, um eine ID-Listensuche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="79782-p116">Office 365 attempts to validate the CSV file. If the validation is unsuccessful, an error message is displayed that might help you troubleshoot the validation errors. The CSV file has to be successfully validated to create an ID list search.</span></span>
    
4. <span data-ttu-id="79782-159">Nachdem die CSV-Datei erfolgreich überprüft wurde, klicken Sie auf **Suchen** , um die ID-Listensuche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="79782-159">After the CSV file is successfully validated, click **Search** to create the ID list search.</span></span> 
    
    <span data-ttu-id="79782-160">NachFolgend finden Sie ein Beispiel für die geschätzten Suchergebnisse und die Abfrage, die für eine ID-Listensuche generiert wird.</span><span class="sxs-lookup"><span data-stu-id="79782-160">Here's an example of the estimated search results and the query that's generated for an ID list search.</span></span>
    
    ![Suchabfrage für eine gezielte Inhaltssuche im Detailbereich](media/dbd9e570-c04b-4056-a8a7-37e9916ec683.png)
  
    <span data-ttu-id="79782-162">Beachten Sie, dass die Anzahl der geschätzten Elemente, die in der Statistik für die ID-Suche angezeigt werden, mit der Anzahl der Elemente übereinstimmen sollte, die Sie in der CSV-Datei ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="79782-162">Note that the number of estimated items displayed in statistics for the ID search should match the number of items that you selected in the CSV file.</span></span>
    
5. <span data-ttu-id="79782-163">Vorschau oder Exportieren der Elemente, die von der ID-Listensuche zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="79782-163">Preview or export the items returned by the ID list search.</span></span>
    
> [!NOTE]
> <span data-ttu-id="79782-p117">Wenn Sie ein Postfach nach dem Erstellen einer ID-Listensuche verschieben, gibt die Abfrage für die Suche nicht die angegebenen Elemente zurück. Der Grund dafür ist, dass die **Document** -Eigenschaft für Postfachelemente geändert wird, wenn ein Postfach verschoben wird. In den seltenen Fällen, in denen ein Postfach verschoben wird, nachdem Sie eine ID-Listensuche erstellt haben, sollten Sie eine neue Inhaltssuche erstellen (oder die Suchergebnisse für die vorhandene Inhaltssuche aktualisieren) und dann die Suchergebnisse oder den Bericht exportieren, um aktualisierte CSV-Dateien zu generieren, die verwendet werden können.  , um eine neue ID-Listensuche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="79782-p117">If you move a mailbox after creating an ID list search, the query for the search won't return the specified items. That's because the **DocumentId** property for mailbox items are changed when a mailbox is moved. In the rare instance when a mailbox is moved after you create an ID list search, you should create a new content search (or update the search results for the existing content search) and then export the search results or report to generate updated CSV files that can be used to create a new ID list search.</span></span> 
