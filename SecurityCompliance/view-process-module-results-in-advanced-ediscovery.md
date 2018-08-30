---
title: Anzeigen von Ergebnisse der Prozess-Modul in Office 365 erweiterte eDiscovery
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
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'Informationen Sie zu Updates für die Ergebnisse eines Moduls Prozess in Office 365 erweiterte eDiscovery, einschließlich Vorgangsstatus und zusammenfassende Prozess ausgeführt.  '
ms.openlocfilehash: 01093b0230aaf78ab7ccf1235f0874a0b69aa1bd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528866"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="12a35-103">Anzeigen von Ergebnisse der Prozess-Modul in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="12a35-103">View Process module results in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="12a35-104">Nach dem **Vorbereiten** \> **Prozess** wird initiiert, können Sie Status und die Ergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="12a35-104">After **Prepare** \> **Process** is initiated, you can view progress and results.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="12a35-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="12a35-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="process-task-status"></a><span data-ttu-id="12a35-107">Process Vorgangsstatus</span><span class="sxs-lookup"><span data-stu-id="12a35-107">Process task status</span></span>

<span data-ttu-id="12a35-108">Unter **Prepare** \> **Prozess** \> **Ergebnisse**, die auf der Seite wird der aktuelle Status (Wenn Prozess derzeit ausgeführt wird) oder den letzten Prozess Status Aufgabenstatus wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="12a35-108">In **Prepare** \> **Process** \> **Results**, the page shows the current status (if Process is currently running) or the last Process status task status as shown in the following example.</span></span>
  
![Prozessmodul-Aufgabenstatus](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
<span data-ttu-id="12a35-110">Die angezeigten Aufgaben variieren je nach den ausgewählten Optionen Prozess.</span><span class="sxs-lookup"><span data-stu-id="12a35-110">The displayed tasks may vary depending on the Process options selected.</span></span> 
  
- <span data-ttu-id="12a35-111">**Inventar**: Erweiterte eDiscovery durchlaufen und alle Dateien, die für den Vorgang ausgewählt und führt die grundlegenden Datensammlung.</span><span class="sxs-lookup"><span data-stu-id="12a35-111">**Inventory**: Advanced eDiscovery iterates through all files selected for Process and performs basic data collection.</span></span>
    
- <span data-ttu-id="12a35-112">**Calculate-Signaturen**: die digitalen Signaturen MD5 berechnet.</span><span class="sxs-lookup"><span data-stu-id="12a35-112">**Calculate signatures**: Calculates the MD5 digital signatures.</span></span>
    
- <span data-ttu-id="12a35-p102">**Verbindung Extraction**: extrahiert innere oder enthaltenen Dateien rekursiv aus zusammengesetzter-Dateien (beispielsweise PST ZIP, MSG). Extrahierte Dateien werden im Ordner "Case" von der Groß-/Kleinschreibung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12a35-p102">**Compounds extraction**: Extracts inner or contained files recursively from compound files (for example, PST, ZIP, MSG). Extracted files are stored in the case folder of the case.</span></span>
    
- <span data-ttu-id="12a35-115">**Synchronisieren von Datenbank**: interne Datenbank Prozess.</span><span class="sxs-lookup"><span data-stu-id="12a35-115">**Synchronizing database**: Internal database process.</span></span>
    
- <span data-ttu-id="12a35-p103">**Kopieren von Dateien**: Kopien von Dateien. Für diese Aufgabe wird immer angezeigt, auch wenn die Option Dateien erweiterte Kopie ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="12a35-p103">**File copy**: Copies Process files. This task is always displayed, even when the advanced Copy files option is selected.</span></span>
    
- <span data-ttu-id="12a35-p104">**Extraktion von Text**: systemeigene Dateien vorhanden sind, extrahiert erweiterte eDiscovery Text aus diesen Dateien DTSearch verwenden. Der extrahierte Text, der diese Dateien als Textdateien im Ordner "Case" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="12a35-p104">**Text extraction**: When there are native files, Advanced eDiscovery extracts text from these files using DTSearch. The extracted text of these files is stored as text files in the case folder.</span></span>
    
- <span data-ttu-id="12a35-120">**Aktualisieren von Metadaten**: die geladene Metadaten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="12a35-120">**Updating metadata**: Processes the loaded metadata.</span></span> 
    
- <span data-ttu-id="12a35-121">**Abschluss**: Interner, die Daten der schließt geladen Groß-/Kleinschreibung Dateien (beispielsweise identifizieren Fehler- und Erfolgsmeldungen-Dateien).</span><span class="sxs-lookup"><span data-stu-id="12a35-121">**Finalizing**: Internal processing that finalizes data of loaded case files (for example, identify error and success files).</span></span> 
    
<span data-ttu-id="12a35-p105">Taskstatus: nach Abschluss des Tasks angezeigt. Während der Ausführung der Aufgaben, wird zur Dauer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12a35-p105">Task status: Displayed after task completion. While tasks are running, run duration is displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="12a35-124">Abgeschlossene Aufgaben umfassen möglicherweise auch Summen für Dateien, die Verarbeitung abgeschlossen oder Dateien mit Fehlern.</span><span class="sxs-lookup"><span data-stu-id="12a35-124">Completed tasks may also include totals for files that completed processing or files with errors.</span></span> 
  
> [!TIP]
> <span data-ttu-id="12a35-p106">"Abbrechen" bietet die Rollbackoption halten Sie die Ausführung der Prozess und klicken Sie dann auf den vorherigen Data Populator Rollback oder verarbeitete Daten gespeichert. Rollback löscht alle verarbeitete Daten. Wenn Sie nicht möchten, dass die verarbeiteten Daten an (beispielsweise planen, diese Dateien erneut zu laden), wählen Sie die "Abbrechen" Option in diesem Fenster zu wählen, führen Sie ein Rollback nicht verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="12a35-p106">"Cancel" provides a rollback option to stop Process execution and then roll back to the previous data population or saved processed data. Rollback clears all processed data. If you do not want the processed data to be lost (for example, you plan to reload these files), select the "Cancel" option in this window to choose not to roll back.</span></span> 
  
## <a name="process-summary"></a><span data-ttu-id="12a35-128">Prozesszusammenfassung</span><span class="sxs-lookup"><span data-stu-id="12a35-128">Process summary</span></span>

<span data-ttu-id="12a35-129">Unter Prepare \> Prozess \> Ergebnisse \> Process Zusammenfassung, wird eine Aufschlüsselung der geladene Dateiergebnisse entsprechend erfolgreiche Verarbeitung und Fehler Ergebnisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="12a35-129">In Prepare \> Process \> Results \> Process summary, a breakdown of loaded file results is displayed according to successful file processing and error results.</span></span>
  
<span data-ttu-id="12a35-130">Die Bereiche präsentieren grafisch dargestellt der importierten Dateistatistiken, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="12a35-130">The panes present a graphical display of imported file statistics, as follows:</span></span>
  
- <span data-ttu-id="12a35-131">**Zusammenfassung Prozess angesammelt**d: alle Dateien in die Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="12a35-131">**Process summary accumulate**d: All files in the case.</span></span>
    
- <span data-ttu-id="12a35-132">**Zusammenfassung zuletzt verarbeitet**: Dateien aus dem letzten Sitzung oder Aktion geladen.</span><span class="sxs-lookup"><span data-stu-id="12a35-132">**Process summary last**: Files loaded from the last session or action.</span></span> 
    
- <span data-ttu-id="12a35-133">**Letzte Familien**: Familie Informationen in die Groß-/Kleinschreibung (falls vorhanden).</span><span class="sxs-lookup"><span data-stu-id="12a35-133">**Families last**: Family information in the case (if any).</span></span>
    
- <span data-ttu-id="12a35-134">Wenn **Seed** Dateien hinzugefügt wurden, wird die Anzahl der Startwert Dateien pro Problem aufgeführt, die für die Dateien definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="12a35-134">If **Seed** files were added, the number of seed files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="12a35-135">Wenn die Markierung von **Seed** Dateien ausgefallen ist, wird, die auch hingewiesen.</span><span class="sxs-lookup"><span data-stu-id="12a35-135">If the marking of **Seed** files failed, that is also noted.</span></span> 
    
- <span data-ttu-id="12a35-136">Wenn **vor dem markierte** Dateien hinzugefügt wurden, wird die Anzahl der Überprüfung vor dem markierten Dateien pro Problem aufgeführt, die für die Dateien definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="12a35-136">If **Pre-tagged** files were added, the number of pre-tagged files is listed per issue that was defined for the files.</span></span> 
    
    <span data-ttu-id="12a35-137">Wenn das Markieren von Dateien **vor dem tagged** ausgefallen ist, ist, die auch darauf hingewiesen.</span><span class="sxs-lookup"><span data-stu-id="12a35-137">If the marking of **Pre-tagged** files failed, that is also noted.</span></span> 
    
![Zusammenfassung des Prozessmoduls](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a><span data-ttu-id="12a35-139">Prozesszusammenfassung gesammelt und die letzte Diagramme</span><span class="sxs-lookup"><span data-stu-id="12a35-139">Process summary accumulated and last charts</span></span>

<span data-ttu-id="12a35-140">Die linke Balken umfasst, Quelle + extrahierten Dateien: also alle Dateien gefunden.</span><span class="sxs-lookup"><span data-stu-id="12a35-140">The left bar includes Source + extracted files: which is all files found.</span></span> 
  
<span data-ttu-id="12a35-141">Das Recht, verarbeitet, umfasst:</span><span class="sxs-lookup"><span data-stu-id="12a35-141">The right bar, Processed, includes:</span></span>
  
- <span data-ttu-id="12a35-142">Dateien mit Ladefehler</span><span class="sxs-lookup"><span data-stu-id="12a35-142">Files with load errors</span></span>
    
- <span data-ttu-id="12a35-143">Erfolgreich geladenen Dateien, unter anderem der folgenden:</span><span class="sxs-lookup"><span data-stu-id="12a35-143">Successfully loaded files, which may include:</span></span> 
    
  - <span data-ttu-id="12a35-144">**Vorhandene**: Dateien, die geladen wurden, bevor und werden jetzt (einschließlich Duplikate) erneut geladen.</span><span class="sxs-lookup"><span data-stu-id="12a35-144">**Existing**: Files that were loaded before and are now loaded again (including duplicates).</span></span>
    
  - <span data-ttu-id="12a35-145">**Text**: eindeutige Dateien mit Text.</span><span class="sxs-lookup"><span data-stu-id="12a35-145">**Text**: Unique files with text.</span></span>
    
  - <span data-ttu-id="12a35-146">**Nicht-Text**: Textdateien, leere systemeigene Textdateien, nicht-Text-Dateien zu leeren.</span><span class="sxs-lookup"><span data-stu-id="12a35-146">**Non-text**: Empty text files, empty native text files, native non-text files.</span></span> 
    
  - <span data-ttu-id="12a35-147">**Doppelte**s: Duplicate-Dateien mit Text.</span><span class="sxs-lookup"><span data-stu-id="12a35-147">**Duplicate**s: Duplicate files with text.</span></span>
    
## <a name="last-process-errors"></a><span data-ttu-id="12a35-148">Letzte Prozess-Fehler</span><span class="sxs-lookup"><span data-stu-id="12a35-148">Last process errors</span></span>

<span data-ttu-id="12a35-149">Unter Prepare \> Prozess \> Ergebnisse \> letzten Prozess Fehler, Details der Fehler in der letzten Sitzung oder ausgeführte Aktion angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="12a35-149">In Prepare \> Process \> Results \> Last process errors, details of the errors in the last session or action performed are displayed.</span></span>
  
![Prozessmodulfehler](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a><span data-ttu-id="12a35-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12a35-151">See also</span></span>

[<span data-ttu-id="12a35-152">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="12a35-152">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="12a35-153">Das Prozess-Modul ausgeführt, und Laden von Daten</span><span class="sxs-lookup"><span data-stu-id="12a35-153">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

