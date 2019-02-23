---
title: Ausführen des Prozessmoduls und Laden von Daten in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Informationen zur Verwendung des Office 365 Security &amp; Compliance Center für den Zugriff auf Office 365 Advanced eDiscovery und zum Ausführen des Prozess Moduls für einen Fall.  '
ms.openlocfilehash: 95c73c034ed2ffa1c45f9aacd8463c497a842859
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217605"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="03141-103">Ausführen des Prozessmoduls und Laden von Daten in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="03141-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="03141-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="03141-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="03141-106">In diesem Abschnitt wird die Funktionalität des erweiterten eDiscovery-Prozess Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="03141-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="03141-p102">Zusätzlich zu Dateidaten können Metadaten wie Dateityp, Erweiterung, Speicherort oder Pfad, Erstellungsdatum und-Uhrzeit, Autor, Depotbank und Betreff in Advanced eDiscovery geladen und für jeden Fall gespeichert werden. Einige Metadaten werden beispielsweise von Advanced eDiscovery berechnet, wenn systemeigene Dateien geladen werden.</span><span class="sxs-lookup"><span data-stu-id="03141-p102">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case. Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="03141-p103">Erweiterte eDiscovery stellt System Metadatenwerte bereit, beispielsweise beinahe doppelt vorhandene Gruppierungen oder Relevanz-Ergebnisse. Andere Metadaten, wie etwa Datei Anmerkungen, können vom Administrator hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="03141-p103">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores. Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="03141-111">Ausgeführter Prozess</span><span class="sxs-lookup"><span data-stu-id="03141-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="03141-p104">Batch Nummern werden während des Prozesses einer Datei zugewiesen, um die Nachverfolgung von Dateien zu ermöglichen. Die Chargennummer ermöglicht auch die Identifizierung von Prozess Batches für Wiederaufbereitungs Optionen. Für die Filterung nach Batch Nummern und Sitzungen stehen zusätzliche Filter zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="03141-p104">Batch numbers are assigned to a file during Process to allow the tracking of files. The batch number also enables identification of Process batches for reprocessing options. Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="03141-115">Führen Sie die folgenden Schritte aus, um Process auszuführen.</span><span class="sxs-lookup"><span data-stu-id="03141-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="03141-116">[Öffnen Sie das Office 365 &amp; Security Compliance Center](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="03141-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="03141-117">Wechseln Sie **zur &amp; Such Untersuchung** \> **eDiscovery** , und klicken Sie dann auf **zur erweiterten eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="03141-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="03141-118">Wählen Sie in Erweiterte eDiscovery in der Seite angezeigte **Anfragen** den entsprechenden Fall aus, und klicken Sie auf **Gehe zu Groß-/Kleinschreibung**.</span><span class="sxs-lookup"><span data-stu-id="03141-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="03141-119">Wählen Sie unter **Prepare** \> **Process** \> **Setup**einen Container aus der Liste der verfügbaren Container aus.</span><span class="sxs-lookup"><span data-stu-id="03141-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Klicken Sie auf Prozess, um die Suchergebnisse der Anfrage hinzuzufügen.](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="03141-121">Klicken Sie auf **Erweiterte Einstellungen...** , wenn Sie den Container als Seed-Dateien oder als vordefinierte Dateien hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="03141-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="03141-p105">Verwenden Sie Seed-Dateien, um das Training bei Problemen mit geringem Reichtum (in der Regel 2% oder weniger) zu beschleunigen. Bei Seed-Dateien empfiehlt es sich, eine Vielzahl von deutlich relevanten Dateien auszuwählen und ungefähr 20-50 Samen pro Problem zu verarbeiten (zu viele seeddateien können Relevanz-Ergebnisse verzerren). Seed-Dateien sollten von derselben Person überprüft werden, die das Problem trainieren wird.</span><span class="sxs-lookup"><span data-stu-id="03141-p105">Use seed files to accelerate training for issues with low richness (usually 2%, or less). For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results). Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="03141-p106">Verwenden Sie vordefinierte Dateien, um die Relevanz-Schulung zu automatisieren. Sie sollten mindestens 1.500-Dateien markieren und den Anteil relevanter und nicht relevanter Dateien genauso wie in der Sammlung, die der Relevanz hinzugefügt wurde, beibehalten. Diese Dateien sollten manuell gekennzeichnet werden, und Sie sollten auf die Qualität der Markierung Vertrauen.</span><span class="sxs-lookup"><span data-stu-id="03141-p106">Use pre-tagged files to automate Relevance training. You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance. These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Screenshot der Seite "Erweiterte Einstellungen" für die Verarbeitung von Batchdateien](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="03141-129">Im Abschnitt **Seed** :</span><span class="sxs-lookup"><span data-stu-id="03141-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="03141-p107">Wählen Sie **als Seed-Dateien markieren** aus, um den Container als Seed-Dateien zu kennzeichnen. Sie müssen Sie auch wählen, um Sie pro Problem aus der Dropdownliste **für Problem** zuzuweisen. Wählen Sie im Dropdown \*\*\*\* - **Tag** entweder **relevant** oder irrelevant aus.</span><span class="sxs-lookup"><span data-stu-id="03141-p107">Choose **Mark as seed files** to mark the container as seed files. You also need choose to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="03141-133">Nachdem Sie Dateien als Startwert festgelegt haben, können Sie Sie nicht als **Pre-Tagged**markieren. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="03141-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="03141-134">Im Abschnitt **Pre-Tagged files** :</span><span class="sxs-lookup"><span data-stu-id="03141-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="03141-p108">Wählen Sie **als vordefinierte Dateien markieren** aus, um den Container als vorgetaggte Dateien zu markieren. Sie müssen Sie auch pro Problem aus der Dropdownliste **für Problem** zuweisen. Wählen Sie im Dropdown \*\*\*\* - **Tag** entweder **relevant** oder irrelevant aus.</span><span class="sxs-lookup"><span data-stu-id="03141-p108">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files. You also need to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="03141-138">Nachdem Sie Dateien als vorDefinierte **Tags**festgelegt haben, können Sie \*\*\*\* Sie nicht als Startwert markieren.</span><span class="sxs-lookup"><span data-stu-id="03141-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="03141-p109">Im Abschnitt **e-Mail-Tagging** . Legen Sie fest, welcher Teil einer verarbeiteten e-Mail als Seed oder Pre-Tagged gekennzeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="03141-p109">In the **Email tagging** section. set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="03141-p110">Klicken Sie zunächst auf **Prozess**. Nach Abschluss des Vorgangs werden die Ergebnisse des Prozesses angezeigt.</span><span class="sxs-lookup"><span data-stu-id="03141-p110">To begin, click **Process**. When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="03141-143">Optional Wenn Sie einer bestimmten Depotbank Datenquellen zuweisen müssen, können Sie \*\*\*\* \> Depotnamen in Verwalter **Verwalten** und zuweisen, die Verwalter in **Verwalter** \> **zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="03141-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="03141-144">Wenn Sie den Fall hinzufügen, können Sie erneut verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="03141-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03141-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03141-145">See also</span></span>

[<span data-ttu-id="03141-146">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="03141-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="03141-147">Anzeigen der Ergebnisse des Prozess Moduls</span><span class="sxs-lookup"><span data-stu-id="03141-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

