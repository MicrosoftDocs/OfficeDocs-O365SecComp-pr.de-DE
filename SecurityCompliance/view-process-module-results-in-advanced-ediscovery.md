---
title: Anzeigen der Ergebnisse des Prozess Moduls in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'In diesem Artikel erfahren Sie, wie Sie die Ergebnisse eines in Office 365 Advanced eDiscovery ausgeführten Prozess Moduls finden, einschließlich Vorgangsstatus und Prozesszusammenfassung.  '
ms.openlocfilehash: 4bbdbf68f71e3459ff2ddcd8ba3fb33e52f16825
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157797"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="11cd5-103">Anzeigen der Ergebnisse des Prozess Moduls in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="11cd5-103">View Process module results in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="11cd5-104">Nachdem der **Vorbereitungs** \> **Prozess** initiiert wurde, können Sie den Status und die Ergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="11cd5-104">After **Prepare** \> **Process** is initiated, you can view progress and results.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="11cd5-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="11cd5-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="process-task-status"></a><span data-ttu-id="11cd5-107">Prozessaufgaben Status</span><span class="sxs-lookup"><span data-stu-id="11cd5-107">Process task status</span></span>

<span data-ttu-id="11cd5-108">In **Prepare** \> **Process** \> **results**zeigt die Seite den aktuellen Status (wenn der Prozess derzeit ausgeführt wird) oder den Status des letzten Prozessstatus Vorgangs an, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="11cd5-108">In **Prepare** \> **Process** \> **Results**, the page shows the current status (if Process is currently running) or the last Process status task status as shown in the following example.</span></span>
  
![Vorgangsstatus des Prozess Moduls](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
<span data-ttu-id="11cd5-110">Die angezeigten Vorgänge können je nach den ausgewählten Prozessoptionen variieren.</span><span class="sxs-lookup"><span data-stu-id="11cd5-110">The displayed tasks may vary depending on the Process options selected.</span></span> 
  
- <span data-ttu-id="11cd5-111">**Inventory**: Advanced eDiscovery durchläuft alle für den Prozess ausgewählten Dateien und führt grundlegende Datensammlungen aus.</span><span class="sxs-lookup"><span data-stu-id="11cd5-111">**Inventory**: Advanced eDiscovery iterates through all files selected for Process and performs basic data collection.</span></span>
    
- <span data-ttu-id="11cd5-112">**Calculate Signatures**: berechnet die digitalen MD5-Signaturen.</span><span class="sxs-lookup"><span data-stu-id="11cd5-112">**Calculate signatures**: Calculates the MD5 digital signatures.</span></span>
    
- <span data-ttu-id="11cd5-113">**Compounds-Extraktion**: extrahiert interne oder enthaltene Dateien rekursiv aus Verbunddateien (beispielsweise PST, ZIP, msg).</span><span class="sxs-lookup"><span data-stu-id="11cd5-113">**Compounds extraction**: Extracts inner or contained files recursively from compound files (for example, PST, ZIP, MSG).</span></span> <span data-ttu-id="11cd5-114">Extrahierte Dateien werden im Fallordner des Falls gespeichert.</span><span class="sxs-lookup"><span data-stu-id="11cd5-114">Extracted files are stored in the case folder of the case.</span></span>
    
- <span data-ttu-id="11cd5-115">**Datenbank wird synchronisiert**: interner Datenbankprozess.</span><span class="sxs-lookup"><span data-stu-id="11cd5-115">**Synchronizing database**: Internal database process.</span></span>
    
- <span data-ttu-id="11cd5-116">**Dateikopie**: kopiert Prozessdateien.</span><span class="sxs-lookup"><span data-stu-id="11cd5-116">**File copy**: Copies Process files.</span></span> <span data-ttu-id="11cd5-117">Diese Aufgabe wird immer angezeigt, auch wenn die Option Erweiterte Dateien kopieren ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="11cd5-117">This task is always displayed, even when the advanced Copy files option is selected.</span></span>
    
- <span data-ttu-id="11cd5-118">**Textextraktion**: bei systemeigenen Dateien extrahiert Advanced eDiscovery Text aus diesen Dateien mithilfe von DTSearch.</span><span class="sxs-lookup"><span data-stu-id="11cd5-118">**Text extraction**: When there are native files, Advanced eDiscovery extracts text from these files using DTSearch.</span></span> <span data-ttu-id="11cd5-119">Der extrahierte Text dieser Dateien wird als Textdateien im Fallordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="11cd5-119">The extracted text of these files is stored as text files in the case folder.</span></span>
    
- <span data-ttu-id="11cd5-120">**Aktualisieren von Metadaten**: verarbeitet die geladenen Metadaten.</span><span class="sxs-lookup"><span data-stu-id="11cd5-120">**Updating metadata**: Processes the loaded metadata.</span></span> 
    
- <span data-ttu-id="11cd5-121">**Finalisieren**: interne Verarbeitung, die die Daten der geladenen Fall Dateien abschließt (beispielsweise Fehler-und Erfolgs Dateien identifizieren).</span><span class="sxs-lookup"><span data-stu-id="11cd5-121">**Finalizing**: Internal processing that finalizes data of loaded case files (for example, identify error and success files).</span></span> 
    
<span data-ttu-id="11cd5-122">Vorgangsstatus: wird nach Abschluss des Vorgangs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11cd5-122">Task status: Displayed after task completion.</span></span> <span data-ttu-id="11cd5-123">Während Vorgänge ausgeführt werden, wird die Ausführungsdauer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11cd5-123">While tasks are running, run duration is displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="11cd5-124">Abgeschlossene Aufgaben können auch Summen für Dateien enthalten, die die Verarbeitung abgeschlossen haben, oder Dateien mit Fehlern.</span><span class="sxs-lookup"><span data-stu-id="11cd5-124">Completed tasks may also include totals for files that completed processing or files with errors.</span></span> 
  
> [!TIP]
> <span data-ttu-id="11cd5-125">"Cancel" bietet eine Rollback-Option, um die Prozessausführung zu beenden und dann auf die vorherige Datenauffüllung oder gespeicherte verarbeitete Daten zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="11cd5-125">"Cancel" provides a rollback option to stop Process execution and then roll back to the previous data population or saved processed data.</span></span> <span data-ttu-id="11cd5-126">Rollback löscht alle verarbeiteten Daten.</span><span class="sxs-lookup"><span data-stu-id="11cd5-126">Rollback clears all processed data.</span></span> <span data-ttu-id="11cd5-127">Wenn Sie nicht möchten, dass die verarbeiteten Daten verloren gehen (beispielsweise möchten Sie diese Dateien erneut laden), wählen Sie die Option "Abbrechen" in diesem Fenster aus, um kein Rollback durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="11cd5-127">If you do not want the processed data to be lost (for example, you plan to reload these files), select the "Cancel" option in this window to choose not to roll back.</span></span> 
  
## <a name="process-summary"></a><span data-ttu-id="11cd5-128">Prozesszusammenfassung</span><span class="sxs-lookup"><span data-stu-id="11cd5-128">Process summary</span></span>

<span data-ttu-id="11cd5-129">In Prepare \> Process \> results \> Process Summary wird eine Aufschlüsselung der geladenen Datei Ergebnisse entsprechend der erfolgreichen Dateiverarbeitung und Fehlerergebnisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11cd5-129">In Prepare \> Process \> Results \> Process summary, a breakdown of loaded file results is displayed according to successful file processing and error results.</span></span>
  
<span data-ttu-id="11cd5-130">In den Bereichen wird eine grafische Anzeige der importierten Dateistatistiken wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="11cd5-130">The panes present a graphical display of imported file statistics, as follows:</span></span>
  
- <span data-ttu-id="11cd5-131">**Prozesszusammenfassung**d: alle Dateien im Fall akkumulieren.</span><span class="sxs-lookup"><span data-stu-id="11cd5-131">**Process summary accumulate**d: All files in the case.</span></span>
    
- <span data-ttu-id="11cd5-132">**Prozesszusammenfassung zuletzt**: Dateien, die aus der letzten Sitzung oder Aktion geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="11cd5-132">**Process summary last**: Files loaded from the last session or action.</span></span> 
    
- <span data-ttu-id="11cd5-133">**Familien zuletzt**: Familieninformationen im Fall (sofern vorhanden).</span><span class="sxs-lookup"><span data-stu-id="11cd5-133">**Families last**: Family information in the case (if any).</span></span>
    
- <span data-ttu-id="11cd5-134">Wenn **Seed** -Dateien hinzugefügt wurden, wird die Anzahl der Seed-Dateien pro Problem aufgeführt, die für die Dateien definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="11cd5-134">If **Seed** files were added, the number of seed files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="11cd5-135">Wenn die Markierung von **Seed** -Dateien fehlgeschlagen ist, wird dies ebenfalls angegeben.</span><span class="sxs-lookup"><span data-stu-id="11cd5-135">If the marking of **Seed** files failed, that is also noted.</span></span> 
    
- <span data-ttu-id="11cd5-136">Wenn Dateien mit vordefinierten **Tags** hinzugefügt wurden, wird die Anzahl der vordefinierten Dateien pro Problem aufgeführt, das für die Dateien definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="11cd5-136">If **Pre-tagged** files were added, the number of pre-tagged files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="11cd5-137">Wenn die Markierung von Dateien mit vordefinierten **Tags** fehlgeschlagen ist, wird dies ebenfalls angegeben.</span><span class="sxs-lookup"><span data-stu-id="11cd5-137">If the marking of **Pre-tagged** files failed, that is also noted.</span></span> 
    
![Zusammenfassung des Prozess Moduls](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a><span data-ttu-id="11cd5-139">Kumuliertes und letztes Diagramm für Prozesszusammenfassung</span><span class="sxs-lookup"><span data-stu-id="11cd5-139">Process summary accumulated and last charts</span></span>

<span data-ttu-id="11cd5-140">Die linke Leiste enthält Quellen + extrahierte Dateien: alle gefundenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="11cd5-140">The left bar includes Source + extracted files: which is all files found.</span></span> 
  
<span data-ttu-id="11cd5-141">Die rechte Leiste, die verarbeitet wird, umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="11cd5-141">The right bar, Processed, includes:</span></span>
  
- <span data-ttu-id="11cd5-142">Dateien mit Ladefehlern</span><span class="sxs-lookup"><span data-stu-id="11cd5-142">Files with load errors</span></span>
    
- <span data-ttu-id="11cd5-143">Erfolgreich geladene Dateien, was Folgendes beinhalten kann:</span><span class="sxs-lookup"><span data-stu-id="11cd5-143">Successfully loaded files, which may include:</span></span> 
    
  - <span data-ttu-id="11cd5-144">**Vorhanden**: Dateien, die zuvor geladen wurden und nun erneut geladen wurden (einschließlich Duplikate).</span><span class="sxs-lookup"><span data-stu-id="11cd5-144">**Existing**: Files that were loaded before and are now loaded again (including duplicates).</span></span>
    
  - <span data-ttu-id="11cd5-145">**Text**: eindeutige Dateien mit Text.</span><span class="sxs-lookup"><span data-stu-id="11cd5-145">**Text**: Unique files with text.</span></span>
    
  - <span data-ttu-id="11cd5-146">**Nicht Text**: leere Textdateien, leere systemeigene Textdateien, systemeigene nicht-Textdateien.</span><span class="sxs-lookup"><span data-stu-id="11cd5-146">**Non-text**: Empty text files, empty native text files, native non-text files.</span></span> 
    
  - <span data-ttu-id="11cd5-147">**Duplikate**s: doppelte Dateien mit Text.</span><span class="sxs-lookup"><span data-stu-id="11cd5-147">**Duplicate**s: Duplicate files with text.</span></span>
    
## <a name="last-process-errors"></a><span data-ttu-id="11cd5-148">Letzte Prozessfehler</span><span class="sxs-lookup"><span data-stu-id="11cd5-148">Last process errors</span></span>

<span data-ttu-id="11cd5-149">In Prepare \> Process \> results \> Last Process Errors werden Details der Fehler in der letzten Sitzung oder ausgeführten Aktion angezeigt.</span><span class="sxs-lookup"><span data-stu-id="11cd5-149">In Prepare \> Process \> Results \> Last process errors, details of the errors in the last session or action performed are displayed.</span></span>
  
![Prozessmodul Fehler](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a><span data-ttu-id="11cd5-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11cd5-151">See also</span></span>

[<span data-ttu-id="11cd5-152">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="11cd5-152">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="11cd5-153">Ausführung des Prozess Moduls und Laden von Daten</span><span class="sxs-lookup"><span data-stu-id="11cd5-153">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

