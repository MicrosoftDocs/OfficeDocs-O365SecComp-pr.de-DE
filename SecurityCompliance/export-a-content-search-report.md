---
title: Exportieren eines Berichts für die Inhaltssuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.CustomizeExportReport
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 5c8c1db6-d8ac-4dbb-8a7a-f65d452169b9
description: Anstatt die tatsächlichen Ergebnisse einer Inhaltssuche im Security & Compliance Center in Office 365 zu exportieren, können Sie einfach einen Suchergebnisbericht exportieren. Der Bericht enthält eine Zusammenfassung der Suchergebnisse und ein Dokument mit detaillierten Informationen zu jedem Element, das exportiert würde.
ms.openlocfilehash: 57c8a9be5c53998570f6ff15a49df69e27745e26
ms.sourcegitcommit: 6c9340e4eb221bf81472ff3f1ae25ae21aaf5297
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2019
ms.locfileid: "31813926"
---
# <a name="export-a-content-search-report"></a><span data-ttu-id="c7d72-104">Exportieren eines Berichts für die Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="c7d72-104">Export a Content Search report</span></span>

<span data-ttu-id="c7d72-105">Anstatt den vollständigen Satz von Suchergebnissen aus einer Inhaltssuche im Security & Compliance Center (und aus einer Inhaltssuche, die mit einem eDiscovery-Fall verknüpft ist) zu exportieren, können Sie die gleichen Berichte exportieren, die beim Exportieren der Suche generiert werden. Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="c7d72-105">Instead of exporting the full set of search results from a Content Search in the Security & Compliance Center (and from a Content Search that's associated with an eDiscovery case), you can just export the same reports that are generated when you export search results.</span></span>
  
<span data-ttu-id="c7d72-106">Wenn Sie einen Bericht exportieren, wird er in einen Ordner heruntergeladen, der den gleichen Namen wie die Inhaltssuche hat, aber mit *_ReportsOnly* angefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c7d72-106">When you export a report, it's downloaded to a folder that has the same name as the Content Search, but that's appended with  *_ReportsOnly*  .</span></span> <span data-ttu-id="c7d72-107">Wenn die Inhaltssuche beispielsweise " *ContosoCase0815* " heißt, wird der Bericht in einen Ordner mit dem Namen *ContosoCase0815_ReportsOnly* heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="c7d72-107">For example, if the Content Search is named  *ContosoCase0815*  , then the report is downloaded to a folder named  *ContosoCase0815_ReportsOnly*  .</span></span> <span data-ttu-id="c7d72-108">Eine Liste der Dokumente, die im Bericht enthalten sind, finden Sie unter [What es included in the Report](#whats-included-in-the-report).</span><span class="sxs-lookup"><span data-stu-id="c7d72-108">For a list of documents that are included in the report, see [What's included in the report](#whats-included-in-the-report).</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="c7d72-109">Bevor Sie beginnen:</span><span class="sxs-lookup"><span data-stu-id="c7d72-109">Before you begin</span></span>

- <span data-ttu-id="c7d72-110">Um einen Bericht über Inhaltssuche zu exportieren, muss Ihnen die Rolle Compliance Search Management im Security & Compliance Center zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-110">To export a Content Search report, you have to be assigned the Compliance Search management role in the Security & Compliance Center.</span></span> <span data-ttu-id="c7d72-111">Diese Rolle wird den integrierten eDiscovery-Manager-und Organisations Verwaltungsrollengruppen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c7d72-111">This role is assigned to the built-in eDiscovery Manager and Organization Management role groups.</span></span> <span data-ttu-id="c7d72-112">Sie wird der Rollengruppe Organisationsverwaltung nicht standardmäßig zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="c7d72-112">It isn't assigned by default to the Organization Management role group.</span></span> <span data-ttu-id="c7d72-113">Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="c7d72-113">For more information, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="c7d72-114">Beim Exportieren eines Berichts werden die Daten vorübergehend in einem eindeutigen Windows Azure-Speicherbereich in der Microsoft-Cloud gespeichert, bevor Sie auf Ihren lokalen Computer heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-114">When you export a report, the data is temporarily stored in a unique Windows Azure storage area in the Microsoft cloud before it's downloaded to your local computer.</span></span> <span data-ttu-id="c7d72-115">stellen sie sicher, dass ihre organisation eine verbindung mit dem endpunkt in Azure herstellen kann, nämlich \*\* \*. blob.core.windows.net\*\* (der platzhalter stellt einen eindeutigen bezeichner für den export dar).</span><span class="sxs-lookup"><span data-stu-id="c7d72-115">Be sure your organization can connect to the endpoint in Azure, which is **\*.blob.core.windows.net** (the wildcard represents a unique identifier for your export).</span></span> <span data-ttu-id="c7d72-116">Die Suchergebnis Daten werden zwei Wochen nach der Erstellung aus dem Azure-Speicherbereich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c7d72-116">The search results data is deleted from the Azure storage area two weeks after it's created.</span></span> 
    
- <span data-ttu-id="c7d72-117">Der Computer, den Sie zum Exportieren der Suchergebnisse verwenden, muss die folgenden Voraussetzungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c7d72-117">The computer you use to export the search results has to meet the following system requirements:</span></span>
    
  - <span data-ttu-id="c7d72-118">32- oder 64-Bit-Versionen von Windows 7 und höher</span><span class="sxs-lookup"><span data-stu-id="c7d72-118">32- or 64-bit versions of Windows 7 and later versions</span></span>
    
  - <span data-ttu-id="c7d72-119">Microsoft .NET Framework 4,7</span><span class="sxs-lookup"><span data-stu-id="c7d72-119">Microsoft .NET Framework 4.7</span></span>
    
  - <span data-ttu-id="c7d72-120">Einen unterstützten Browser:</span><span class="sxs-lookup"><span data-stu-id="c7d72-120">A supported browser:</span></span>
    
    - <span data-ttu-id="c7d72-121">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c7d72-121">Microsoft Edge</span></span>
    
      <span data-ttu-id="c7d72-122">oder</span><span class="sxs-lookup"><span data-stu-id="c7d72-122">or</span></span>
    
    - <span data-ttu-id="c7d72-123">Microsoft Internet Explorer 10 und höhere Versionen</span><span class="sxs-lookup"><span data-stu-id="c7d72-123">Microsoft Internet Explorer 10 and later versions</span></span>
    
    <span data-ttu-id="c7d72-124">**Hinweis:** Microsoft stellt keine Drittanbietererweiterungen oder Add-ons für ClickOnce-Anwendungen her.</span><span class="sxs-lookup"><span data-stu-id="c7d72-124">**Note:** Microsoft doesn't manufacture third-party extensions or add-ons for ClickOnce applications.</span></span> <span data-ttu-id="c7d72-125">Das Exportieren von Suchergebnissen mithilfe eines nicht unterstützten Browsers mit Drittanbietererweiterungen oder Add-ons wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c7d72-125">Exporting search results using an unsupported browser with third-party extensions or add-ons isn't supported.</span></span> 

- <span data-ttu-id="c7d72-126">Wenn die geschätzte Gesamtgröße der von einer Inhaltssuche zurückgegebenen Ergebnisse 20&nbsp;TB überschreitet, tritt beim Exportieren des Berichts ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="c7d72-126">If the estimated total size of the results returned by a Content Search exceeds 20&nbsp;TB, exporting the report will fail.</span></span> <span data-ttu-id="c7d72-127">Um den Bericht erfolgreich zu exportieren, versuchen Sie, den Bereich einzugrenzen und die Suche erneut auszuführen, damit die geschätzte Größe der Ergebnisse weniger&nbsp;als 20 TB beträgt.</span><span class="sxs-lookup"><span data-stu-id="c7d72-127">To successfully export the report, try to narrow the scope and re-run the search so the estimated size of the results is less than 20&nbsp;TB.</span></span>

- <span data-ttu-id="c7d72-128">Das Exportieren von Inhalts Suchberichten gilt für die maximale Anzahl von Exporten, die gleichzeitig ausgeführt werden, und die maximale Anzahl von Exporten, die ein einzelner Benutzer ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="c7d72-128">Exporting Content Search reports counts against the maximum number of exports running at the same time and the maximum number of exports that a single user can run.</span></span> <span data-ttu-id="c7d72-129">Weitere Informationen zu Export Grenzwerten finden Sie unter [Exportieren von Inhalts Suchergebnissen](export-search-results.md#export-limits).</span><span class="sxs-lookup"><span data-stu-id="c7d72-129">For more information about export limits, see [Export Content Search results](export-search-results.md#export-limits).</span></span>

## <a name="generate-and-download-a-content-search-report"></a><span data-ttu-id="c7d72-130">Generieren und Herunterladen eines Inhalts Suchberichts</span><span class="sxs-lookup"><span data-stu-id="c7d72-130">Generate and download a Content Search report</span></span>

<span data-ttu-id="c7d72-131">Die Schritte zum Generieren und Herunterladen eines Inhalts Suchberichts ähneln dem tatsächlichen Exportieren der Suchergebnisse.</span><span class="sxs-lookup"><span data-stu-id="c7d72-131">The steps to generate and download a Content Search report are very similar to actually exporting search results.</span></span>
  
## <a name="step-1-generate-the-report-for-export"></a><span data-ttu-id="c7d72-132">Schritt 1: Generieren des Berichts für den Export</span><span class="sxs-lookup"><span data-stu-id="c7d72-132">Step 1: Generate the report for export</span></span>

<span data-ttu-id="c7d72-133">Der erste Schritt besteht darin, den Bericht für das Herunterladen auf Ihren Computer vorzubereiten, der exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="c7d72-133">The first step is to prepare the report for downloading to your computer exporting.</span></span> <span data-ttu-id="c7d72-134">Beim Bericht werden die Berichtsdokumente in einen Azure-Speicherbereich in der Microsoft-Cloud hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="c7d72-134">When you the report, the report documents are uploaded to an Azure storage area in the Microsoft cloud.</span></span>
  
1. <span data-ttu-id="c7d72-135">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="c7d72-135">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="c7d72-136">Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="c7d72-136">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="c7d72-137">Klicken Sie im linken Bereich des Security & Compliance Centers auf **Suche** \> **Inhaltssuche**.</span><span class="sxs-lookup"><span data-stu-id="c7d72-137">In the left pane of the Security & Compliance Center, click **Search** \> **Content search**.</span></span>
    
4. <span data-ttu-id="c7d72-138">Wählen Sie auf der Seite **Inhaltssuche** eine Suche aus.</span><span class="sxs-lookup"><span data-stu-id="c7d72-138">On the **Content search** page, select a search.</span></span> 
    
5. <span data-ttu-id="c7d72-139">Klicken Sie im Detailbereich unter **Bericht auf einem Computer exportieren**auf **Bericht generieren**.</span><span class="sxs-lookup"><span data-stu-id="c7d72-139">In the details pane, under **Export report to a computer**, click **Generate report**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c7d72-140">Wenn die Suchergebnisse älter als 7 Tage sind, werden Sie aufgefordert, die Suchergebnisse zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c7d72-140">If the results for a search are older than 7 days, you are prompted to update the search results.</span></span> <span data-ttu-id="c7d72-141">Wenn dies der Fall ist, brechen Sie den Export ab, klicken Sie im Detailbereich für die ausgewählte Suche auf **Suchergebnisse aktualisieren** , und starten Sie dann den Berichtsexport erneut, nachdem die Ergebnisse aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-141">If this happens, cancel the export, click **Update search results** in the details pane for the selected search, and then start the report export again after the results are updated.</span></span> 
  
6. <span data-ttu-id="c7d72-142">Wählen Sie auf der Seite **Bericht exportieren** unter **diese Elemente aus der Suche einbeziehen**eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="c7d72-142">On the **Export a report** page, under **Include these items from the search**, choose one of the following options:</span></span>
    
    - <span data-ttu-id="c7d72-143">Nur indizierte Elemente exportieren</span><span class="sxs-lookup"><span data-stu-id="c7d72-143">Export only indexed items</span></span>
    
    - <span data-ttu-id="c7d72-144">Indizierte und nicht indizierte Elemente exportieren</span><span class="sxs-lookup"><span data-stu-id="c7d72-144">Export indexed and unindexed items</span></span>
    
    - <span data-ttu-id="c7d72-145">Nur nicht indizierte Elemente exportieren</span><span class="sxs-lookup"><span data-stu-id="c7d72-145">Export only unindexed items</span></span>
    
    <span data-ttu-id="c7d72-146">Weitere Informationen zu nicht indizierten Elementen finden Sie unter [teilweise indizierte Elemente in der Inhaltssuche](partially-indexed-items-in-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="c7d72-146">For more information about unindexed items, see [Partially indexed items in Content Search](partially-indexed-items-in-content-search.md).</span></span>
    
7. <span data-ttu-id="c7d72-147">Wählen Sie aus, dass Suchstatistiken für alle Versionen von SharePoint-Dokumenten eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7d72-147">Choose to include search statistics for all versions of SharePoint documents.</span></span> <span data-ttu-id="c7d72-148">Diese Option wird nur angezeigt, wenn die Inhaltsquellen der Suche SharePoint oder OneDrive for Business-Websites enthalten.</span><span class="sxs-lookup"><span data-stu-id="c7d72-148">This option appears only if the content sources of the search includes SharePoint or OneDrive for Business sites.</span></span>
    
8. <span data-ttu-id="c7d72-149">Klicken Sie auf **Bericht generieren**.</span><span class="sxs-lookup"><span data-stu-id="c7d72-149">Click **Generate report**.</span></span>
    
    <span data-ttu-id="c7d72-150">Der Suchergebnisbericht wird zum Herunterladen vorbereitet, was bedeutet, dass die Berichtsdokumente in den Azure-Speicherbereich in der Microsoft-Cloud hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-150">The search results report is prepared for downloading, which means the report documents will be uploaded to the Azure storage area in the Microsoft cloud.</span></span> <span data-ttu-id="c7d72-151">Wenn der Bericht zum Herunterladen bereit ist, wird der Link zum **herunterladen** des Berichts unter **Bericht auf einem Computer exportieren** im Detailbereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c7d72-151">When the report is ready for download, the **Download report** link is displayed under **Export report to a computer** in the details pane.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c7d72-152">Sie können einen Bericht auch für eine Inhaltssuche exportieren, die mit einem eDiscovery-Fall verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="c7d72-152">You can also export a report for a Content Search that's associated with an eDiscovery case.</span></span> <span data-ttu-id="c7d72-153">Wechseln Sie dazu zu **eDiscovery** \> **eDiscovery**, wählen Sie einen Fall aus, und klicken Sie auf Bearbeitungs](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)Symbol **Bearbeiten** ![.</span><span class="sxs-lookup"><span data-stu-id="c7d72-153">To do this, go to **eDiscovery** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span> <span data-ttu-id="c7d72-154">Wählen Sie auf der Seite Such **Vorgänge** eine Suche aus, und \*\*\*\* ![klicken Sie dann auf Export](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> Suchergebnis Symbol exportieren, um **einen Bericht zu exportieren**.</span><span class="sxs-lookup"><span data-stu-id="c7d72-154">On the **Searches** page, select a search, and then click **Export** ![Export search results icon](media/47205c65-babd-4b3a-bd7b-98dfd92883ba.png) \> **Export a report**.</span></span> 
  
## <a name="step-2-download-the-report"></a><span data-ttu-id="c7d72-155">Schritt 2: Herunterladen des Berichts</span><span class="sxs-lookup"><span data-stu-id="c7d72-155">Step 2: Download the report</span></span>

<span data-ttu-id="c7d72-156">Im nächsten Schritt wird der Bericht aus dem Azure-Speicherbereich auf Ihren lokalen Computer heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="c7d72-156">The next step is to download the report from the Azure storage area to your local computer.</span></span>
  
1. <span data-ttu-id="c7d72-157">Klicken Sie im Detailbereich für die Suche, für die Sie den Bericht erstellt haben, unter **Bericht auf Computer exportieren**auf **Bericht herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="c7d72-157">In the details pane for the search that you generated the report for, under **Export report to a computer**, click **Download report**.</span></span>
    
    <span data-ttu-id="c7d72-158">Die Seite zum **herunterladen des Berichts** wird angezeigt und enthält die folgenden Informationen zum Bericht, bis Sie auf Ihren Computer heruntergeladen werden können.</span><span class="sxs-lookup"><span data-stu-id="c7d72-158">The **Download report** page is displayed and contains the following information about the report till be downloaded to your computer.</span></span> 
    
    - <span data-ttu-id="c7d72-159">Die Anzahl der Elemente, die heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-159">The number of items that will be downloaded.</span></span>
    
    - <span data-ttu-id="c7d72-160">Die geschätzte Gesamtgröße der Elemente, die heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-160">The estimated total size of the items that will be downloaded.</span></span>
    
    - <span data-ttu-id="c7d72-161">Ob indiziert oder nicht indiziert wird exportiert.</span><span class="sxs-lookup"><span data-stu-id="c7d72-161">Whether indexed or unindexed will be exported.</span></span> <span data-ttu-id="c7d72-162">Nicht indizierte Elemente sind Elemente, die ein erkanntes Format aufweisen, verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-162">Unindexed items are items that have an recognized format, are encrypted, or weren't indexed for other reasons.</span></span>
    
    - <span data-ttu-id="c7d72-163">Gibt an, ob Versionen von SharePoint-Dokumenten heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-163">Whether or not versions of SharePoint documents will be downloaded.</span></span>
    
    - <span data-ttu-id="c7d72-164">Der Status des Berichtsexport Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c7d72-164">The status of the report export process.</span></span> <span data-ttu-id="c7d72-165">Sie können den Download des Berichts auch dann starten, wenn die Vorbereitung des Berichts nicht abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="c7d72-165">You can start downloading the report even if the preparation of the report isn't complete.</span></span>
    
2. <span data-ttu-id="c7d72-166">Klicken Sie unter **Schlüssel exportieren** auf **In Zwischenablage kopieren**.</span><span class="sxs-lookup"><span data-stu-id="c7d72-166">Under **Export key**, click **Copy to clipboard**.</span></span> <span data-ttu-id="c7d72-167">Sie verwenden diesen Schlüssel in Schritt 5, um den Bericht herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="c7d72-167">You will use this key in step 5 to download the report.</span></span>
    
    > [!IMPORTANT]
    > <span data-ttu-id="c7d72-168">Da jeder das eDiscovery-Export Tool installieren und starten und dann diesen Schlüssel zum Herunterladen des Suchberichts verwenden kann, müssen Sie Vorkehrungen treffen, um diesen Schlüssel genau so zu schützen, als würden Sie Kennwörter oder andere sicherheitsrelevante Informationen schützen.</span><span class="sxs-lookup"><span data-stu-id="c7d72-168">Because anyone can install and start the eDiscovery Export tool, and then use this key to download the search report, be sure to take precautions to protect this key just like you would protect passwords or other security-related information.</span></span> 
  
3. <span data-ttu-id="c7d72-169">Klicken Sie auf **Bericht herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="c7d72-169">Click **Download report**.</span></span>
    
4. <span data-ttu-id="c7d72-170">Wenn Sie aufgefordert werden, das **microsoft office 365 eDiscovery-Export Tool**zu installieren, klicken Sie auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="c7d72-170">If you're prompted to install the **MicrosoftOffice 365 eDiscovery Export Tool**, click **Install**.</span></span>
    
5. <span data-ttu-id="c7d72-171">Fügen Sie im **eDiscovery-Exporttool** den Export-Schlüssel, den Sie in Schritt 2 kopiert haben, in das entsprechende Feld ein.</span><span class="sxs-lookup"><span data-stu-id="c7d72-171">In the **eDiscovery Export Tool**, paste the export key that you copied in step 2 in the appropriate box.</span></span>
    
6. <span data-ttu-id="c7d72-172">Klicken Sie auf **Durchsuchen** , um den Speicherort für den Bericht anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c7d72-172">Click **Browse** to specify the location where you want to download the report.</span></span> 
    
7. <span data-ttu-id="c7d72-173">Klicken Sie zum Herunterladen der Suchergebnisse auf Ihren Computer auf **Starten**.</span><span class="sxs-lookup"><span data-stu-id="c7d72-173">Click **Start** to download the search results to your computer.</span></span> 
    
    <span data-ttu-id="c7d72-174">Das **eDiscovery-Export Tool** zeigt Statusinformationen zum Exportvorgang an, einschließlich einer Schätzung der Anzahl (und der Größe) der verbleibenden zu ladenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="c7d72-174">The **eDiscovery Export Tool** displays status information about the export process, including an estimate of the number (and size) of the remaining items to be downloaded.</span></span> <span data-ttu-id="c7d72-175">Nach Abschluss des Exportvorgangs können Sie auf die Dateien am Speicherort zugreifen, an dem Sie heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-175">When the export process is complete, you can access the files in the location where they were downloaded.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c7d72-176">Sie können den Bericht für eine Inhaltssuche herunterladen, die einem eDiscovery-Fall zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c7d72-176">You can download the report for a Content Search that's associated with an eDiscovery case.</span></span> <span data-ttu-id="c7d72-177">Wechseln Sie dazu zu **eDiscovery** \> **eDiscovery**, wählen Sie einen Fall aus, und klicken Sie auf Bearbeitungs](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)Symbol **Bearbeiten** ![.</span><span class="sxs-lookup"><span data-stu-id="c7d72-177">To do this, go to **eDiscovery** \> **eDiscovery**, select a case, and click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span> <span data-ttu-id="c7d72-178">Wählen Sie \*\*\*\* auf der Seite Exports einen Berichtsexport aus, und klicken Sie dann im Detailbereich auf **Bericht herunterladen** .</span><span class="sxs-lookup"><span data-stu-id="c7d72-178">On the **Exports** page, select an report export, and then click **Download report** in the details pane.</span></span> 
  
## <a name="whats-included-in-the-report"></a><span data-ttu-id="c7d72-179">Inhalt des Berichts</span><span class="sxs-lookup"><span data-stu-id="c7d72-179">What's included in the report</span></span>

<span data-ttu-id="c7d72-180">Wenn Sie einen Bericht zu den Ergebnissen einer Inhaltssuche generieren und exportieren, werden die folgenden Dokumente heruntergeladen:</span><span class="sxs-lookup"><span data-stu-id="c7d72-180">When you generate and export a report about the results of a Content Search, the following documents are downloaded:</span></span>
  
- <span data-ttu-id="c7d72-181">**Export Zusammenfassung** – ein Excel-Dokument, das eine Zusammenfassung des Exports enthält.</span><span class="sxs-lookup"><span data-stu-id="c7d72-181">**Export Summary** - An Excel document that contains a summary of the export.</span></span> <span data-ttu-id="c7d72-182">Hierzu gehören Informationen wie die Anzahl der durchsuchten Inhaltsquellen, die Anzahl der Suchergebnisse von jedem Inhaltsspeicherort, die geschätzte Anzahl von Elementen, die tatsächliche Anzahl von Elementen, die exportiert werden sollen, sowie die geschätzte und tatsächliche Größe von Elementen. , die exportiert werden würden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-182">This includes information such as the number of content sources that were searched, the number of search results from each content location, the estimated number of items, the actual number of items that would be exported, and the estimated and actual size of items that would be exported.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="c7d72-183">Wenn Sie beim Exportieren des Berichts nicht indizierte Elemente einschließen, ist die Anzahl der nicht indizierten Elemente in der Gesamtzahl der geschätzten Suchergebnisse und in der Gesamtzahl der heruntergeladenen Suchergebnisse enthalten (wenn Sie die Suchergebnisse exportieren), die im Zusammenfassungsbericht exportieren.</span><span class="sxs-lookup"><span data-stu-id="c7d72-183">If you include unindexed items when exporting the report, the number of unindexed items are included in the total number of estimated search results and in the total number of downloaded search results (if you were to export the search results) that are listed in the Export Summary report.</span></span> <span data-ttu-id="c7d72-184">Anders ausgedrückt: die Gesamtzahl der heruntergeladenen Elemente entspricht der Gesamtzahl der geschätzten Ergebnisse und der Gesamtanzahl der nicht indizierten Elemente.</span><span class="sxs-lookup"><span data-stu-id="c7d72-184">In other words, the total number of items that would be downloaded is equal to the total number of estimated results and the total number of unindexed items.</span></span> 
  
- <span data-ttu-id="c7d72-185">**Manifest** – eine Manifestdatei (im XML-Format), die Informationen zu jedem in den Suchergebnissen enthaltenen Element enthält.</span><span class="sxs-lookup"><span data-stu-id="c7d72-185">**Manifest** - A manifest file (in XML format) that contains information about each item included in the search results.</span></span> 
    
- <span data-ttu-id="c7d72-186">**Results** – ein Excel-Dokument, das eine Zeile mit Informationen zu jedem indizierten Element enthält, das mit den Suchergebnissen exportiert würde.</span><span class="sxs-lookup"><span data-stu-id="c7d72-186">**Results** - An Excel document that contains a row with information about each indexed item that would be exported with the search results.</span></span> <span data-ttu-id="c7d72-187">Für e-Mails enthält das Ergebnisprotokoll Informationen zu den einzelnen Nachrichten, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="c7d72-187">For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="c7d72-188">Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).</span><span class="sxs-lookup"><span data-stu-id="c7d72-188">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="c7d72-189">Das Datum, an dem die Nachricht gesendet oder empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="c7d72-189">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="c7d72-190">Die Betreffzeile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c7d72-190">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="c7d72-191">Absender und Empfänger der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c7d72-191">The sender and recipients of the message.</span></span>
    
    <span data-ttu-id="c7d72-192">Für Dokumente aus SharePoint und OneDrive for Business-Websites enthält das Ergebnisprotokoll Informationen zu jedem Dokument, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="c7d72-192">For documents from SharePoint and OneDrive for Business sites, the Results log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="c7d72-193">Die URL für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="c7d72-193">The URL for the document.</span></span>
    
  - <span data-ttu-id="c7d72-194">Die URL für die Websitesammlung, in der sich das Dokument befindet.</span><span class="sxs-lookup"><span data-stu-id="c7d72-194">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="c7d72-195">Das Datum, an dem das Dokument zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c7d72-195">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="c7d72-196">Der Name des Dokuments (das sich in der Spalte Betreff im Ergebnisprotokoll befindet).</span><span class="sxs-lookup"><span data-stu-id="c7d72-196">The name of the document (which is located in the Subject column in the result log).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="c7d72-197">Die Anzahl der Zeilen im **Ergebnis** Bericht sollte der Gesamtzahl der gedownloadeten Suchergebnisse minus der Gesamtanzahl der im Bericht "nicht **indizierte Elemente** " aufgeführten Elemente entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c7d72-197">The number of rows in the **Results** report should be equal to the total number of search results that would be downloaded minus the total number of items listed in the **Unindexed Items** report.</span></span> 
  
- <span data-ttu-id="c7d72-198">Nicht **indizierte Elemente** – ein Excel-Dokument mit Informationen zu nicht indizierten Elementen, die in die Suchergebnisse eingeschlossen werden würden.</span><span class="sxs-lookup"><span data-stu-id="c7d72-198">**Unindexed Items** - An Excel document that contains information about any unindexed items that would be included in the search results.</span></span> <span data-ttu-id="c7d72-199">Wenn Sie beim Generieren des Suchergebnis Berichts keine nicht indizierten Elemente hinzufügen, wird dieser Bericht weiterhin heruntergeladen, ist aber leer.</span><span class="sxs-lookup"><span data-stu-id="c7d72-199">If you don't include unindexed items when you generate the search results report, this report will still be downloaded, but will be empty.</span></span>
