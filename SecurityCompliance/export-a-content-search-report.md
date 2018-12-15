---
title: Exportieren eines Inhaltssuchberichts
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Anstelle von Export von tatsächlichen Ergebnissen einer Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center, können Sie nur einen Bericht der Suchergebnisse exportieren. Der Bericht enthält eine Zusammenfassung der Ergebnisse der und ein Dokument mit ausführlichen Informationen über jedes Element, das exportiert werden würde.
ms.openlocfilehash: e15c6550d58701abe9b268455deca0aef60265fb
ms.sourcegitcommit: 1bc36cd57ab1604f057e2b5d336cf1893ba00125
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2018
ms.locfileid: "27283141"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="91d3a-104">Exportieren eines Inhaltssuchberichts</span><span class="sxs-lookup"><span data-stu-id="91d3a-104">Export a Content Search report</span></span>

<span data-ttu-id="91d3a-105">Anstelle von exportieren die vollständige Unterstützung der Suche von Suchergebnissen aus einer Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center (und aus einer Inhaltssuche, die einem eDiscovery-Fall zugeordnet ist), können Sie dieselben Berichte, die nur exportieren generiert werden, wenn Sie Exportieren von Suchergebnissen.</span><span class="sxs-lookup"><span data-stu-id="91d3a-105">Instead of exporting the full set of search results from a Content Search in the Office 365 Security &amp; Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can just export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="91d3a-p102">Beim Exportieren eines Berichts wird es in einen Ordner heruntergeladen, die den gleichen Namen wie die Inhaltssuche hat, aber, die mit *_ReportsOnly* angehängt ist. Beispielsweise wird die Inhaltssuche *ContosoCase0815* genannt, wird Sie dann der Bericht in einen Ordner namens *ContosoCase0815_ReportsOnly* heruntergeladen. Eine Liste von Dokumenten, die im Bericht enthalten sind, finden Sie unter [Was ist im Bericht enthalten](#whats-included-in-the-report).</span><span class="sxs-lookup"><span data-stu-id="91d3a-p102">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with  *_ReportsOnly*  . For example, if the Content Search is named  *ContosoCase0815*  , then the report is downloaded to a folder named  *ContosoCase0815_ReportsOnly*  . For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="91d3a-109">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="91d3a-109">Before you begin</span></span>

- <span data-ttu-id="91d3a-p103">Um einen Bericht Inhaltssuche zu exportieren, müssen Sie die Verwaltungsrolle Compliance-Suche in der Office 365-Sicherheit zugewiesen werden &amp; Compliance Center. Integrierte eDiscovery-Manager und Organization Management Rollengruppen wird diese Rolle zugewiesen. Es ist nicht in der Standardeinstellung der Rollengruppe "Organisationsverwaltung" zugewiesen. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="91d3a-p103">To export a Content Search report, you have to be assigned the Compliance Search management role in the Office 365 Security &amp; Compliance Center. This role is assigned to the built-in eDiscovery Manager and Organization Management role groups. It isn't assigned by default to the Organization Management role group. For more information, see [Assign eDiscovery permissions in the Office 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="91d3a-p104">Wenn Sie einen Bericht exportieren, werden die Daten vorübergehend in einem eindeutigen Windows Azure-Speicher-Bereich in der Microsoft-Cloud gespeichert, bevor sie sich an Ihren lokalen Computer heruntergeladen wird. Achten Sie darauf Ihrer Organisation kann an den Endpunkt in Azure, ist eine Verbindung herstellen \*\* \*. blob.core.windows.net\*\* (der Platzhalter stellt einen eindeutigen Bezeichner für Ihren Export). Suche Ergebnisse werden die Daten aus dem Bereich der Azure-Speicher gelöscht zwei Wochen, nachdem er erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p104">When you export a report, the data is temporarily stored in a unique Windows Azure storage area in the Microsoft cloud before it's downloaded to your local computer. Be sure your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export). The search results data is deleted from the Azure storage area two weeks after it's created.</span></span> 
    
- <span data-ttu-id="91d3a-117">Der Computer, den Sie zum Exportieren der Suchergebnisse verwenden, muss die folgenden Voraussetzungen erfüllen:

</span><span class="sxs-lookup"><span data-stu-id="91d3a-117">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="91d3a-118">32- oder 64-Bit-Versionen von Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="91d3a-118">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="91d3a-119">Microsoft .NET Framework 4.7</span><span class="sxs-lookup"><span data-stu-id="91d3a-119">Microsoft .NET Framework 4.7</span></span>
    
  - <span data-ttu-id="91d3a-120">Einen unterstützten Browser:</span><span class="sxs-lookup"><span data-stu-id="91d3a-120">A supported browser:</span></span>
    
    - <span data-ttu-id="91d3a-121">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="91d3a-121">Microsoft Edge</span></span>
    
      <span data-ttu-id="91d3a-122">oder</span><span class="sxs-lookup"><span data-stu-id="91d3a-122">or</span></span>
    
    - <span data-ttu-id="91d3a-123">Microsoft Internet Explorer 10 und höhere Versionen</span><span class="sxs-lookup"><span data-stu-id="91d3a-123">Microsoft Internet Explorer 10 and later versions</span></span>
    
    <span data-ttu-id="91d3a-p105">**Hinweis:** Microsoft herstellen nicht Drittanbieter-Erweiterungen oder Add-ons für ClickOnce-Anwendungen. Exportieren von Suchergebnissen mithilfe von einem nicht unterstützten Browser mit Drittanbieter-Erweiterungen oder Add-ons wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p105">**Note:** Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications. Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 

- <span data-ttu-id="91d3a-p106">Wenn die geschätzte Gesamtgröße der von einem Inhaltssuche zurückgegebenen Ergebnisse 20 übersteigt&nbsp;TB, Exportieren des Berichts schlägt fehl. Versuchen Sie zum erfolgreichen Exportieren des Berichts, den Bereich einzuschränken, und führen Sie die Suche erneut aus, damit die geschätzte Größe der Ergebnisse kleiner als 20 ist&nbsp;TB.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p106">If the estimated total size of the results returned by a Content Search exceeds 20&nbsp;TB, exporting the report will fail. To successfully export the report, try to narrow the scope and re-run the search so the estimated size of the results is less than 20&nbsp;TB.</span></span>

## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="91d3a-128">Generieren und Herunterladen eines Berichts für die Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="91d3a-128">Generate and download a Content Search report</span></span>

<span data-ttu-id="91d3a-129">Die Schritte zum Generieren und zum Herunterladen eines Berichts Inhaltssuche sind sehr ähnlich tatsächlich Suchergebnisse exportieren.</span><span class="sxs-lookup"><span data-stu-id="91d3a-129">The steps to generate and download a Content Search report are very similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="91d3a-130">Schritt 1: Generieren Sie den Bericht für den export</span><span class="sxs-lookup"><span data-stu-id="91d3a-130">Step 1: Generate the report for export</span></span>

<span data-ttu-id="91d3a-p107">Der erste Schritt besteht darin, den Bericht vorzubereiten, für den Download auf Ihrem Computer exportieren. Cloud-Wenn Sie den Bericht, den Bericht, Dokumente in einen Bereich Azure-Speicher in der Microsoft hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p107">The first step is to prepare the report for downloading to your computer exporting. When you the report, the report documents are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="91d3a-133">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="91d3a-133">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="91d3a-134">Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="91d3a-134">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="91d3a-135">Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Suche &amp; Untersuchung** \> **Inhaltssuche**.</span><span class="sxs-lookup"><span data-stu-id="91d3a-135">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**.</span></span>
    
4. <span data-ttu-id="91d3a-136">Wählen Sie auf der Seite **Inhaltssuche** eine Suche ein.</span><span class="sxs-lookup"><span data-stu-id="91d3a-136">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="91d3a-137">Klicken Sie im Detailbereich unter **Bericht auf einen Computer exportieren**auf **Bericht generieren**.</span><span class="sxs-lookup"><span data-stu-id="91d3a-137">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="91d3a-p108">Wenn die Ergebnisse für eine Suche älter als 7 Tage sind, werden Sie aufgefordert, um die Suchergebnisse zu aktualisieren. In diesem Fall Abbrechen Sie den Export, klicken Sie im Detailbereich für die ausgewählte Suche auf **Update-Suchergebnisse** und starten Sie den Berichtsexport erneut, nachdem die Ergebnisse aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p108">If the results for a search are older than 7 days, you are prompted to update the search results. If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="91d3a-140">Wählen Sie auf der Seite **Exportieren eines Berichts** unter **diese Einträge aus der Suche einschließen**eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="91d3a-140">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="91d3a-141">Nur indizierte Elemente exportieren</span><span class="sxs-lookup"><span data-stu-id="91d3a-141">Export only indexed items</span></span>
    
    - <span data-ttu-id="91d3a-142">Indizierte und nicht indizierte Elemente exportieren</span><span class="sxs-lookup"><span data-stu-id="91d3a-142">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="91d3a-143">Nur nicht indizierte Elemente exportieren</span><span class="sxs-lookup"><span data-stu-id="91d3a-143">Export only unindexed items</span></span>
    
    <span data-ttu-id="91d3a-144">Weitere Informationen zu nicht indizierten Elementen finden Sie unter [teilweise indizierte Elemente in Inhaltssuche](partially-indexed-items-in-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="91d3a-144">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="91d3a-p109">Verhindern Sie, dass die Suchstatistik für alle Versionen von SharePoint-Dokumenten enthält. Diese Option ist nur dann, wenn die Inhaltsquellen der Suche umfasst SharePoint oder OneDrive for Business-Websites.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p109">Choose to include search statistics for all versions of SharePoint documents. This option appears only if the content sources of the search includes SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="91d3a-147">Klicken Sie auf **Bericht generieren**.</span><span class="sxs-lookup"><span data-stu-id="91d3a-147">Click **Generate report**.</span></span>
    
    <span data-ttu-id="91d3a-p110">Der Bericht der Suchergebnisse vorbereitet wird für das Herunterladen, was bedeutet, dass die Berichtsdokumente in den Bereich der Azure-Speicher in der Cloud Microsoft hochgeladen werden soll. Wenn der Bericht zum Download bereit ist, wird der **Bericht herunterladen** Link im Detailbereich unter **Bericht auf einen Computer exportieren** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p110">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure storage area in the Microsoft cloud. When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="91d3a-p111">Sie können auch einen Bericht für ein Inhaltssuche exportieren, die einem eDiscovery-Fall zugeordnet ist. Wechseln Sie zu diesem Zweck zu **Suche &amp; Untersuchung** \> **eDiscovery**, wählen Sie eine Anfrage aus, und klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Klicken Sie auf der Seite **sucht** , wählen Sie eine Suche aus, und klicken Sie dann auf **Exportieren** ![Exportieren von Suchergebnissen Symbol](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Exportieren eines Berichts**.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p111">You can also export a report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Searches** page, select a search, and then click **Export** ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="91d3a-153">Schritt 2: Herunterladen des Berichts</span><span class="sxs-lookup"><span data-stu-id="91d3a-153">Step 2: Download the report</span></span>

<span data-ttu-id="91d3a-154">Im nächste Schritt wird um den Bericht aus dem Bereich der Azure-Speicher auf dem lokalen Computer herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="91d3a-154">The next step is to download the report from the Azure storage area to your local computer.</span></span>
  
1. <span data-ttu-id="91d3a-155">Klicken Sie im Detailbereich für die Suche, dass Sie den Bericht für, unter **Exportieren Bericht auf einen Computer**generiert auf **Bericht herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="91d3a-155">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="91d3a-156">Die Downloadseite **Bericht** wird angezeigt und enthält die folgenden Informationen zu den Bericht bis zum an Ihrem Computer heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="91d3a-156">The **Download report** page is displayed and contains the following information about the report till be downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="91d3a-157">Die Anzahl der Elemente, die heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="91d3a-157">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="91d3a-158">Die geschätzte Gesamtgröße der Elemente, die heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="91d3a-158">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="91d3a-p112">Ob indiziert oder nicht-indizierten exportiert werden. Nicht indizierte Elemente sind Elemente, die ein bekanntes Format haben, werden verschlüsselt oder aus anderen Gründen indiziert wurden nicht.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p112">Whether indexed or unindexed will be exported. Unindexed items are items that have an recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="91d3a-161">Unabhängig davon, ob Versionen von SharePoint-Dokumente heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="91d3a-161">Whether or not versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="91d3a-p113">Der Status des Exportvorgangs Bericht. Sie können beginnen, den Bericht herunterladen, auch wenn die Vorbereitung des Berichts nicht abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p113">The status of the report export process. You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="91d3a-p114">Klicken Sie unter **Schlüssel exportieren**auf **in die Zwischenablage kopieren**. Sie verwenden dieser Schlüssel in Schritt 5, um den Bericht herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p114">Under **Export key**, click **Copy to clipboard**. You will use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="91d3a-166">Da jeder kann installieren und das eDiscovery-Export-Tool starten und dann dieser Schlüssel verwenden, um den Bericht Suche herunterzuladen, müssen Sie unbedingt müssen Sie Vorsichtsmaßnahmen gegen dieser Schlüssel schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="91d3a-166">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="91d3a-167">Klicken Sie auf **Bericht herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="91d3a-167">Click **Download report**.</span></span>
    
4. <span data-ttu-id="91d3a-168">Wenn Sie aufgefordert werden, installieren Sie **MicrosoftOffice 365 eDiscovery-Exporttool**, klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="91d3a-168">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="91d3a-169">Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 2 kopiert haben, in das entsprechende Feld ein.</span><span class="sxs-lookup"><span data-stu-id="91d3a-169">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="91d3a-170">Klicken Sie auf **Durchsuchen** , um den Speicherort angeben, in dem Sie den Bericht herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="91d3a-170">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="91d3a-171">Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**.</span><span class="sxs-lookup"><span data-stu-id="91d3a-171">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="91d3a-p115">Die **eDiscovery-Exporttool** zeigt Statusinformationen über den Exportvorgang, einschließlich eine Schätzung der Anzahl (und Größe) der verbleibenden Elemente heruntergeladen werden. Wenn der Exportvorgang abgeschlossen ist, können Sie die Dateien in den Speicherort zugreifen, in dem sie heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p115">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded. When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="91d3a-p116">Sie können den Bericht für ein Inhaltssuche herunterladen, die einem eDiscovery-Fall zugeordnet ist. Wechseln Sie zu diesem Zweck zu **Suche &amp; Untersuchung** \> **eDiscovery**, wählen Sie eine Anfrage aus, und klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). Klicken Sie auf der Seite **exportiert** wählen Sie einen Bericht exportieren, und klicken Sie dann im Detailbereich auf **Bericht herunterladen** .</span><span class="sxs-lookup"><span data-stu-id="91d3a-p116">You can download the report for a Content Search that's associated with an eDiscovery case. To do this, go to **Search &amp; investigation** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif). On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="91d3a-177">Was ist in den Bericht einbezogen.</span><span class="sxs-lookup"><span data-stu-id="91d3a-177">What's included in the report</span></span>

<span data-ttu-id="91d3a-178">Wenn Sie generieren und eines Berichts zu den Ergebnissen einer Inhaltssuche exportieren, sind die folgenden Dokumente heruntergeladen werden:</span><span class="sxs-lookup"><span data-stu-id="91d3a-178">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="91d3a-p117">**Zusammenfassung exportieren** - eine Excel-Dokument, das eine Zusammenfassung des Exports enthält. Hierzu zählen Informationen wie die Anzahl der Inhaltsquellen, die durchsucht wurden, die Anzahl der Suchergebnisse aus jeder Inhaltsspeicherort, die geschätzte Anzahl der Elemente, die tatsächliche Anzahl von Elementen, die exportiert werden würde und der geschätzten und der tatsächlichen Größe der Elemente würde exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p117">**Export Summary** - An Excel document that contains a summary of the export. This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="91d3a-p118">Wenn Sie beim Exportieren des Berichts nicht indizierter Elemente einschließen, werden die Anzahl der nicht-indizierten Elemente in die Gesamtzahl der geschätzten Suchergebnisse und die Gesamtzahl der heruntergeladenen Suchergebnisse (Wenn Sie waren so exportieren Sie die Suchergebnisse), die in aufgeführt sind die Exportieren Sie Zusammenfassungsbericht. Anders ausgedrückt, entspricht die Gesamtanzahl der Elemente, die heruntergeladen werden würde die Gesamtzahl der erwarteten Ergebnisse und die Gesamtzahl der nicht-indizierten Elementen.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p118">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report. In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="91d3a-183">**Manifest** - eine Manifestdatei (im XML-Format), das Informationen über jedes Element in den Suchergebnissen enthalten enthält.</span><span class="sxs-lookup"><span data-stu-id="91d3a-183">**Manifest** - A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="91d3a-p119">**Ergebnisse** - eine Excel-Dokument, das eine Zeile mit Informationen zu den einzelnen indizierten Elementen enthält, die mit den Suchergebnissen exportiert werden würde. Für e-Mails die, das Ergebnis-Protokoll enthält Informationen zu jeder Nachricht, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="91d3a-p119">**Results** - An Excel document that contains a row with information about each indexed item that would be exported with the search results. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="91d3a-186">Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).</span><span class="sxs-lookup"><span data-stu-id="91d3a-186">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="91d3a-187">Das Datum, an dem die Nachricht gesendet oder empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="91d3a-187">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="91d3a-188">Die Betreffzeile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="91d3a-188">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="91d3a-189">Absender und Empfänger der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="91d3a-189">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="91d3a-190">Für Dokumente aus SharePoint und OneDrive for Business-Websites, das Ergebnisse-Protokoll enthält Informationen über jedes Dokument einschließlich:</span><span class="sxs-lookup"><span data-stu-id="91d3a-190">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="91d3a-191">Die URL für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="91d3a-191">The URL for the document.</span></span>
    
  - <span data-ttu-id="91d3a-192">Die URL für die Websitesammlung, in dem das Dokument gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="91d3a-192">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="91d3a-193">Das Datum, das das Dokument zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="91d3a-193">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="91d3a-194">Der Name des Dokuments (der in der Spalte Betreff im Protokoll Ergebnis befindet).</span><span class="sxs-lookup"><span data-stu-id="91d3a-194">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="91d3a-195">Die Anzahl der Zeilen in **der Ergebnisbericht** sollte die Gesamtzahl der Suchergebnisse entsprechen, die minus der Gesamtanzahl der Elemente aufgeführt, die im Bericht **Nicht indizierten Elementen** gedownloadet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="91d3a-195">The number of rows in the **Results** report should be equal to the total number of search results that would be downloaded minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="91d3a-p120">**Nicht-indizierten Elementen** - eine Excel-Dokument, das Informationen über alle nicht-indizierten Elemente enthält, die in den Suchergebnissen enthalten sein wird. Wenn Sie beim Erstellen des Berichts der Suchergebnisse nicht indizierter Elemente einschließen, in diesem Bericht wird weiterhin heruntergeladen werden, aber leer.</span><span class="sxs-lookup"><span data-stu-id="91d3a-p120">**Unindexed Items** - An Excel document that contains information about any unindexed items that would be included in the search results. If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
