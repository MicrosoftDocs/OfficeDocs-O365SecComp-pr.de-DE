---
title: Führen Sie das Modul Prozess und Laden von Daten in Office 365 erweiterte eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Hier erfahren Sie, wie Sie die Office 365-Sicherheit &amp; Compliance Center zu Office 365 erweiterte eDiscovery zugreifen, und führen Sie das Prozess-Modul für eine Anfrage.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529462"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a><span data-ttu-id="1d59a-103">Führen Sie das Modul Prozess und Laden von Daten in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1d59a-103">Run the Process module and load data in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="1d59a-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="1d59a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="1d59a-106">In diesem Abschnitt wird die Funktionalität des Moduls Prozess erweiterte eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="1d59a-106">This section describes the functionality of the Advanced eDiscovery Process module.</span></span> 
  
<span data-ttu-id="1d59a-p102">Zusätzlich zur Dateidaten kann in Metadaten wie Dateityp, Erweiterung, Standort oder Pfad, Erstellungsdatum und Uhrzeit, Autor, Verwaltungsberechtigter und Betreff, geladen werden erweiterte eDiscovery und für jeden Fall gespeichert. Einigen Metadaten, die wird beispielsweise von erweiterten eDiscovery berechnet, wenn systemeigene Dateien geladen werden.</span><span class="sxs-lookup"><span data-stu-id="1d59a-p102">In addition to file data, metadata such as file type, extension, location or path, creation date and time, author, custodian, and subject, can be loaded into Advanced eDiscovery and saved for each case. Some metadata is calculated by Advanced eDiscovery, for example, when native files are loaded.</span></span> 
  
<span data-ttu-id="1d59a-p103">Erweiterte eDiscovery bietet System Metadatenwerte wie nahezu doppelte Gruppen oder Relevanz Bewertungen. Andere Metadaten wie der Datei Anmerkungen, kann vom Administrator hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1d59a-p103">Advanced eDiscovery provides system metadata values, such as Near-duplicate groupings or Relevance scores. Other metadata, such as file annotations, can be added by the Administrator.</span></span> 
  
## <a name="running-process"></a><span data-ttu-id="1d59a-111">Laufenden Prozess</span><span class="sxs-lookup"><span data-stu-id="1d59a-111">Running Process</span></span>

> [!NOTE]
> <span data-ttu-id="1d59a-p104">Batch-Nummern werden in eine Datei während der Prozess zugewiesen, um die Überwachung der Dateien zu ermöglichen. Die Anzahl der Batch kann auch die Identifikation des Prozesses Batches für Anwendereingabe Optionen. Zusätzliche Filter stehen zum Filtern nach Batch Anzahl und Sitzungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="1d59a-p104">Batch numbers are assigned to a file during Process to allow the tracking of files. The batch number also enables identification of Process batches for reprocessing options. Additional filters are available for filtering by batch number and sessions.</span></span> 
  
<span data-ttu-id="1d59a-115">Führen Sie die folgenden Schritte aus, um den Prozess ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1d59a-115">Perform the following steps to run Process.</span></span>
  
1. <span data-ttu-id="1d59a-116">[Öffnen Sie die Office 365-Sicherheit &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span><span class="sxs-lookup"><span data-stu-id="1d59a-116">[Open the Office 365 Security &amp; Compliance Center](go-to-the-securitycompliance-center.md) .</span></span> 
    
2. <span data-ttu-id="1d59a-117">Wechseln Sie zu **Suche &amp; Untersuchung** \> **eDiscovery** , und klicken Sie dann auf **Gehe zu erweiterten eDiscovery**.</span><span class="sxs-lookup"><span data-stu-id="1d59a-117">Go to **Search &amp; investigation** \> **eDiscovery** and then click **Go to Advanced eDiscovery**.</span></span>
    
3. <span data-ttu-id="1d59a-118">Erweiterte eDiscovery wählen Sie die entsprechende Anfrage in der angezeigten Seite **Fällen** und dann auf **Gehe zu Fall**.</span><span class="sxs-lookup"><span data-stu-id="1d59a-118">In Advanced eDiscovery, select the appropriate case in the displayed **Cases** page and click **Go to case**.</span></span>
    
4. <span data-ttu-id="1d59a-119">Unter **Prepare** \> **Prozess** \> **Setup**, wählen Sie eine Container aus der Liste der verfügbaren Container aus.</span><span class="sxs-lookup"><span data-stu-id="1d59a-119">In **Prepare** \> **Process** \> **Setup**, select a container from the list of available containers.</span></span>
    
    ![Klicken Sie auf fortsetzen, um die Suchergebnisse die Groß-/Kleinschreibung hinzuzufügen](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. <span data-ttu-id="1d59a-121">Klicken Sie auf **Erweiterte Einstellungen...** , wenn Sie den Container als Ausgangswert Dateien oder als vor dem markierten Dateien hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="1d59a-121">Click **Advanced settings...** if you want to add the container as seed files or as pre-tagged files.</span></span> 
    
    <span data-ttu-id="1d59a-p105">Seed Dateien die Schulung für Probleme mit geringer Funktionsvielfalt beschleunigen verwenden (in der Regel 2 % oder weniger). Seed-Dateien, wird empfohlen, dass Sie wählen Sie eine Vielzahl von Messagingsysteme relevanten Dateien und zu verarbeiten 20 – 50 Basis pro Problem (zu viele Seed-Dateien können Relevanz Ergebnisse verzerren). Durch die gleiche Person, die das Problem Schulen wird, sollte SEED Dateien überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="1d59a-p105">Use seed files to accelerate training for issues with low richness (usually 2%, or less). For seed files, it is recommended that you select a variety of distinctly relevant files and process about 20-50 seeds per issue (too many seed files can skew Relevance results). Seed files should be reviewed by the same person who will train the issue.</span></span>
    
    <span data-ttu-id="1d59a-p106">Verwenden Sie vor dem markierte Dateien Relevanz Schulungen zu automatisieren. Sie sollten mindestens 1.500 Dateien, und beibehalten dem Anteil der-relevanten Dateien für die Überprüfung relevante genauso wie in der Auflistung, Relevanz hinzugefügt wurde. Diese Dateien manuell markiert werden soll, und Sie sollten sich die Qualität von Kategorien sicher sein.</span><span class="sxs-lookup"><span data-stu-id="1d59a-p106">Use pre-tagged files to automate Relevance training. You should tag at least 1,500 files, and keep the proportion of relevant to non-relevant files the same as in the collection added to Relevance. These files should be manually tagged, and you should be confident in the quality of tagging.</span></span>
    
    ![Screenshot der erweiterte Einstellungsseite für die Verarbeitung von Batchdateien](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - <span data-ttu-id="1d59a-129">Im Abschnitt **Seed** :</span><span class="sxs-lookup"><span data-stu-id="1d59a-129">In the **Seed** section:</span></span> 
    
    <span data-ttu-id="1d59a-p107">Wählen Sie **als Ausgangswert Dateien markieren** markieren Sie den Container als Ausgangswert-Dateien. Sie müssen auch das **Problem** Dropdown-pro Problem zuweisen auswählen. Wählen Sie aus der Dropdownliste **Tag** **Relevant** oder **nicht relevant** .</span><span class="sxs-lookup"><span data-stu-id="1d59a-p107">Choose **Mark as seed files** to mark the container as seed files. You also need choose to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="1d59a-133">Nachdem Sie die Dateien als **Ausgangswert**festlegen, können nicht Sie sie als **vorab markierte**markieren.</span><span class="sxs-lookup"><span data-stu-id="1d59a-133">Once you set files as **Seed**, you cannot mark them as **Pre-tagged**.</span></span> 
  
  - <span data-ttu-id="1d59a-134">Im Abschnitt **vor dem markierten Dateien** :</span><span class="sxs-lookup"><span data-stu-id="1d59a-134">In the **Pre-tagged files** section:</span></span> 
    
    <span data-ttu-id="1d59a-p108">Wählen Sie **als vorab markierte Dateien markieren** markieren Sie den Container als vor dem markierten Dateien. Sie müssen auch diese pro Problem in der **für Problem** Dropdown-Liste zuordnen. Wählen Sie aus der Dropdownliste **Tag** **Relevant** oder **nicht relevant** .</span><span class="sxs-lookup"><span data-stu-id="1d59a-p108">Choose **Mark as pre-tagged files** to mark the container as pre-tagged files. You also need to assign them per issue from the **For issue** drop-down. Choose either **Relevant** or **Not relevant** from the **Tag** drop-down.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="1d59a-138">Nachdem Sie Dateien als **markierte vor dem**festlegen, können nicht Sie sie als **Ausgangswert**markieren.</span><span class="sxs-lookup"><span data-stu-id="1d59a-138">Once you set files as **Pre-tagged**, you cannot mark them as **Seed**.</span></span> 
  
  - <span data-ttu-id="1d59a-p109">Im Abschnitt **E-Mail zu markieren** . festlegen, welcher Teil einer verarbeiteten e-Mail sind, als Seed oder vor dem markierten markiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d59a-p109">In the **Email tagging** section. set which part of a processed email are to be marked as Seed or Pre-tagged.</span></span> 
    
6. <span data-ttu-id="1d59a-p110">Klicken Sie zunächst auf **Prozess**. Wenn abgeschlossen ist, werden die Prozess-Ergebnisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d59a-p110">To begin, click **Process**. When completed, the Process results are displayed.</span></span>
    
7. <span data-ttu-id="1d59a-143">(Optional) Wenn Sie ein bestimmtes Verwaltungsberechtigter Datenquellen zuweisen müssen, können Sie hinzufügen und bearbeiten Sie Verwaltungsberechtigter Namen in der **Verwalter** \> **Verwalten** und zuweisen Verwalter in **Verwalter** \> **zuweisen**.</span><span class="sxs-lookup"><span data-stu-id="1d59a-143">(Optional) If you need to assign data sources to a specific custodian, you can add and edit custodian names in **Custodians** \> **Manage** and assign custodians in **Custodians** \> **Assign**.</span></span> 
    
<span data-ttu-id="1d59a-144">Wenn Sie die Groß-/Kleinschreibung hinzugefügt haben, können Sie dann erneut verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1d59a-144">If you add to the case, then you can process again.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1d59a-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d59a-145">See also</span></span>

[<span data-ttu-id="1d59a-146">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1d59a-146">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="1d59a-147">Anzeigen von Ergebnissen der Prozess Modul</span><span class="sxs-lookup"><span data-stu-id="1d59a-147">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

