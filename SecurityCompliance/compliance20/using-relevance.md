---
title: Verwenden des Relevance-Moduls zum Analysieren von Daten in Advanced eDiscovery (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 6e94adc6e6b7fb7d8757b161ffdf01066cadac7a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242120"
---
# <a name="use-the-relevance-module-to-analyze-data-in-advanced-ediscovery-preview"></a><span data-ttu-id="a60c9-102">Verwenden des Relevance-Moduls zum Analysieren von Daten in Advanced eDiscovery (Preview)</span><span class="sxs-lookup"><span data-stu-id="a60c9-102">Use the Relevance module to analyze data in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="a60c9-103">In Advanced eDiscovery (Preview) enthält das Relevance-Modul die Relevanz von Schulungen und Überprüfungen von Dateien im Zusammenhang mit einem Fall.</span><span class="sxs-lookup"><span data-stu-id="a60c9-103">In Advanced eDiscovery (Preview), the Relevance module includes the Relevance training and review of files related to a case.</span></span> <span data-ttu-id="a60c9-104">Um den Relevanz-Workflow zu verwenden, wechseln Sie zu Arbeitsmappe verwalten in einem Arbeitssatz, und klicken Sie auf Relevanz anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a60c9-104">In order to use the Relevance workflow, go to Manage Working Set within a working set and click on Show Relevance.</span></span> <span data-ttu-id="a60c9-105">Es gibt einige Schritte, die Sie ausführen müssen, bevor Sie den Workflow starten können:</span><span class="sxs-lookup"><span data-stu-id="a60c9-105">There are a couple of steps you need to complete before you can start the workflow:</span></span>
- <span data-ttu-id="a60c9-106">Prozess: jeder dem Workingset hinzugefügte Auslastungs Satz wird hier als Container angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a60c9-106">Process: each load set added to the working set will show up as a "container" here.</span></span> <span data-ttu-id="a60c9-107">Sie müssen diese Dokumente verarbeiten, bevor Sie Sie zum Relevanz-Modul hinzufügen können. Dies ist auch der Ort, an dem Sie Sie als Seeds oder als Pre-Tagged für ein bestimmtes Problem markieren können.</span><span class="sxs-lookup"><span data-stu-id="a60c9-107">You need to process these documents before you can add them to Relevance module; this is also where you can mark them as seed or pre-tagged for a specific issue.</span></span>
- <span data-ttu-id="a60c9-108">Zur Relevanz hinzufügen: unter \> Relevanz laden können Sie Dokumente, die zu Relevanz verarbeitet wurden, hinzufügen, um Sie für Schulungen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="a60c9-108">Add to Relevance: Under Relevance \> Loads, you can add documents that have been processed to Relevance to make them available for training.</span></span>

<span data-ttu-id="a60c9-109">Der Relevanz-Workflow wird angezeigt und wie folgt beschrieben:</span><span class="sxs-lookup"><span data-stu-id="a60c9-109">The Relevance workflow is shown and described as follows:</span></span>
  
![Relevanz-Workflow](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="a60c9-111">**Zyklen der Bewertung und Nachverfolgung**:</span><span class="sxs-lookup"><span data-stu-id="a60c9-111">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="a60c9-112">**Bewertung**: ermöglicht eine frühe Bewertung basierend auf einer Zufallsstichprobe von Dateien und verwendet diese Bewertung, um Entscheidungen zu treffen, um die Leistung des vorher sagenden Codierungsprozesses zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a60c9-112">**Assessment**: Enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="a60c9-113">**Track**: berechnen und Anzeigen von Zwischenergebnissen der Bewertung, während die statistische Gültigkeit des Prozesses überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="a60c9-113">**Track**: Calculate and display interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="a60c9-114">**Zyklen der Schulung und Nachverfolgung**</span><span class="sxs-lookup"><span data-stu-id="a60c9-114">**Cycles of training and tracking**</span></span>
    
  - <span data-ttu-id="a60c9-115">**Tag**: Advanced EDiscovery (Preview) erfahren Sie anhand der iterativen Überprüfungen und Markierungen einzelner Dateien, welche Relevanz-Kriterien für jedes Problem gelten.</span><span class="sxs-lookup"><span data-stu-id="a60c9-115">**Tag**: Advanced eDiscovery (Preview) learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="a60c9-116">**Track**: berechnen und Anzeigen von zwischenErgebnissen der Relevanz-Schulung bei gleichzeitiger Überwachung der statistischen Gültigkeit des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="a60c9-116">**Track**: Calculate and display interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="a60c9-117">**Batch Berechnung**: die akkumulierten und gelernten Relevanz-Kriterien werden auf die gesamte Dateisammlung angewendet, und für jede Datei wird ein relevanzwert generiert.</span><span class="sxs-lookup"><span data-stu-id="a60c9-117">**Batch calculation**: The accumulated and learned Relevance criteria is applied to the entire file collection, and a Relevance score is generated for each file.</span></span>
    
- <span data-ttu-id="a60c9-118">**Entscheiden**: die Ergebnisse der Analyse, die auf den gesamten Fall angewendet werden, werden nach der Batch Berechnung angezeigt, und es werden Daten zum Überprüfen der Dokumentüberprüfung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a60c9-118">**Decide**: The results of the analysis applied to the entire case is displayed after Batch calculation, and data used to make document review decisions is displayed.</span></span>
    
- <span data-ttu-id="a60c9-119">**Test**: Ergebnisse können getestet werden, um die Gültigkeit und Wirksamkeit der Advanced EDiscovery (Preview)-Verarbeitung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="a60c9-119">**Test**: Results can be tested to verify the validity and effectiveness of the Advanced eDiscovery (Preview) processing.</span></span>

- <span data-ttu-id="a60c9-120">**Suche**: Sobald der Relevanz-Workflow abgeschlossen ist, können Sie die Ausgabe wie zum Beispiel "Read Perzentil" eines Dokuments für Ihr Problem verwenden, wenn Sie eine Abfrage innerhalb des Arbeitssatzes ausführen.</span><span class="sxs-lookup"><span data-stu-id="a60c9-120">**Search**: Once the Relevance workflow is complete, you can use the output such as read percentile of a document for your issue when you run a query within your working set.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="a60c9-121">Richtlinien für Relevanz Schulungen und Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="a60c9-121">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="a60c9-122">Es folgt eine Übersicht über die Richtlinien für die Relevanz von Schulungen und Überprüfungen:</span><span class="sxs-lookup"><span data-stu-id="a60c9-122">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="a60c9-123">**Fehler und**Inkonsistenzen: Wenn während des Trainings Markierungsfehler auftreten, kehren Sie zu früheren Datei Beispielen zurück, um Sie zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="a60c9-123">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them.</span></span> <span data-ttu-id="a60c9-124">Wenn zu viele Fehler zu korrigieren sind oder eine neue Perspektive für den Fall oder das Problem vorliegt, sollten die Relevanz-Kriterien vom Administrator neu definiert werden, und das Relevanz-Training wurde erneut gestartet.</span><span class="sxs-lookup"><span data-stu-id="a60c9-124">If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="a60c9-125">**Tagging und Schulung**:</span><span class="sxs-lookup"><span data-stu-id="a60c9-125">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="a60c9-126">Dateien sollten nur auf der Grundlage von Inhalten gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-126">Files should be tagged based on content only.</span></span> <span data-ttu-id="a60c9-127">Berücksichtigen Sie keine Metadaten wie Depot, Datum oder Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="a60c9-127">Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="a60c9-128">Beachten Sie beim Taggen von Dateien keine Datumsbereiche im Text.</span><span class="sxs-lookup"><span data-stu-id="a60c9-128">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="a60c9-129">Berücksichtigen Sie beim Taggen von Dateien keine eingebetteten Grafiken.</span><span class="sxs-lookup"><span data-stu-id="a60c9-129">Do not consider embedded graphical images when tagging files.</span></span>
     
  - <span data-ttu-id="a60c9-130">Text ignorieren, der auf Relevanz angewendet wird, wird in der angezeigten Dateiinhalt in der Textansicht relevant entfernt.</span><span class="sxs-lookup"><span data-stu-id="a60c9-130">Ignore text applied to Relevance will be removed in the displayed file content in the text view in Relevance.</span></span> <span data-ttu-id="a60c9-131">Wenn die Werte für Ignore Text definiert wurden, nachdem Relevanz Training bereits gestartet wurde, wird der neue ignorierte Text auf Beispieldateien angewendet, die von dem Punkt erstellt wurden, an dem Sie definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a60c9-131">If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined.</span></span> <span data-ttu-id="a60c9-132">Das Feature Text ignorieren sollte vorsichtig verwendet werden, da die Verwendung die Leistung der Dateianalyse reduzieren kann.</span><span class="sxs-lookup"><span data-stu-id="a60c9-132">The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="a60c9-133">Verwenden Sie die Option **Tagging überspringen** nur bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="a60c9-133">Use the **Skip tagging** option only when necessary.</span></span> <span data-ttu-id="a60c9-134">Advanced eDiscovery (Preview) wird nicht basierend auf übersprungenen Dateien trainiert.</span><span class="sxs-lookup"><span data-stu-id="a60c9-134">Advanced eDiscovery (Preview) does not train based on skipped files.</span></span> <span data-ttu-id="a60c9-135">Wenn es schwierig ist, zu beurteilen, ob eine Datei relevant ist, sollten Sie bei der Bewertung, wann immer möglich, nicht über **springen**, sondern als relevant (R) oder nicht relevant (Nr) markieren.</span><span class="sxs-lookup"><span data-stu-id="a60c9-135">In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**.</span></span> <span data-ttu-id="a60c9-136">Wenn Advanced eDiscovery (Preview) das Training auswertet, kann dann gesehen werden, wie gut diese Dateitypen verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-136">When Advanced eDiscovery (Preview) evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="a60c9-137">Auch Dateien mit sehr kleinem extrahiertem Text sollten, wenn möglich, als R/NR als "Skip" markiert werden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-137">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="a60c9-138">Tagging kann sich auf die Klassifizierung auswirken, solange die Datei lesbar ist und als R/NR gekennzeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="a60c9-138">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="a60c9-139">Die Dateisequenz Nummer in der Liste angezeigte Beispieldateien auf der Registerkarte **Tag** ermöglicht es dem Benutzer, zur ursprünglichen angezeigten Reihenfolge der Dateien zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="a60c9-139">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="a60c9-140">Sie können zu einem beliebigen Beispiel zurückkehren und das Tagging der Assessment-und Trainingssatz Dateien ändern.</span><span class="sxs-lookup"><span data-stu-id="a60c9-140">You can go back to any sample and change the tagging of the assessment and training set files.</span></span> <span data-ttu-id="a60c9-141">Die Änderungen werden beim Erstellen des nächsten Beispiels angewendet.</span><span class="sxs-lookup"><span data-stu-id="a60c9-141">The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="a60c9-142">Gescannte Excel-Dateien im PDF-Format sollten beim Taggen von Dateien genauso behandelt werden wie native Excel-Dateien.</span><span class="sxs-lookup"><span data-stu-id="a60c9-142">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="a60c9-143">Wenn Sie Zweifel bezüglich des Relevanz-Taggings einer Datei haben, konsultieren Sie einen Experten.</span><span class="sxs-lookup"><span data-stu-id="a60c9-143">When in doubt regarding the Relevance tagging of a file, consult an expert.</span></span> <span data-ttu-id="a60c9-144">Das falsche Tagging während der Relevanz-Schulung kann zu einem späteren Zeitpunkt im Prozess zu Zeitverlusten führen und sich auch negativ auf die Qualität der Gesamtergebnisse auswirken.</span><span class="sxs-lookup"><span data-stu-id="a60c9-144">Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="a60c9-145">Schlüsselwörter, die in Stichwortlisten definiert wurden, werden in Farben angezeigt, damit der Benutzer relevante Dateien beim taggen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a60c9-145">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="a60c9-146">**Batch Berechnung**: Dateien, die vom Experten als R/Nr markiert wurden, erhalten eine Bewertung von 0 oder 100.</span><span class="sxs-lookup"><span data-stu-id="a60c9-146">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100.</span></span> <span data-ttu-id="a60c9-147">Dies gilt für das Tagging vor der Batch Berechnung.</span><span class="sxs-lookup"><span data-stu-id="a60c9-147">This applies to tagging made before Batch calculation.</span></span> <span data-ttu-id="a60c9-148">Wenn der Experte das Problem nach der Batch Berechnung in den Leerlauf umgeschaltet hat und dieses Problem weiterhin kennzeichnet, werden die neu markierten Ergebnisse nicht 100/0, sondern die ursprüngliche Partitur.</span><span class="sxs-lookup"><span data-stu-id="a60c9-148">If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="a60c9-149">**Probleme und Samplingmodus**: Probleme werden normalerweise deaktiviert, wenn die Arbeit an diesen abgeschlossen ist (Relevanz-Schulung wird stabilisiert und die Batch Berechnung durchgeführt), wenn die Probleme abgebrochen werden oder wenn ein anderer Benutzer an den Problemen arbeitet.</span><span class="sxs-lookup"><span data-stu-id="a60c9-149">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="a60c9-150">Schritte in Relevanz Schulung</span><span class="sxs-lookup"><span data-stu-id="a60c9-150">Steps in Relevance training</span></span>

<span data-ttu-id="a60c9-151">Auf der Registerkarte **Relevanz \> verfolgen** bietet Advanced eDiscovery Empfehlungen für die Fortsetzung der Verarbeitung mit den folgenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="a60c9-151">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps.</span></span> <span data-ttu-id="a60c9-152">Die Implikationen werden im folgenden beschrieben, wenn jeder der folgenden Schritte im Relevanz-Schulungsprozess empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="a60c9-152">The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="a60c9-153">Tagging/Continue Tagging: Dateiüberprüfung und Relevanz-Tagging, die von einem Experten für jede Datei und jedes Problem innerhalb eines Beispiels ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-153">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="a60c9-154">Implikation: ein vorhandenes Beispiel muss markiert werden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-154">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="a60c9-155">Bewertung/Fortsetzung der Bewertung: ermöglicht die vorzeitige Validierung der Relevanz der Groß-/Kleinschreibung und eine vorläufige Ansicht der Relevanz der für den aktuellen Fall importierten Datei Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="a60c9-155">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="a60c9-156">Implikation: mehr Bewertung ist erforderlich oder empfohlen.</span><span class="sxs-lookup"><span data-stu-id="a60c9-156">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="a60c9-157">Schulung/Fortbildung: Prozess, bei dem Advanced eDiscovery vom Experten, der die Dateibeispiele kennzeichnet, erlernt und die Möglichkeit erhält, Relevanz-Kriterien für jedes Problem im Kontext jedes Falls zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a60c9-157">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="a60c9-158">Implikation: das Problem benötigt mehr Schulung; Das nächste Beispiel sollte erstellt und gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-158">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="a60c9-159">Batch Berechnung: Relevanzprozess, bei dem Advanced eDiscovery das während der Schulung erworbene Wissen einnimmt und es auf die gesamte Datei Auffüllung anwenden kann.</span><span class="sxs-lookup"><span data-stu-id="a60c9-159">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population.</span></span> <span data-ttu-id="a60c9-160">Alle Dateien in der entsprechenden Dateigruppe werden auf Relevanz ausgewertet und einem Relevanz-Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a60c9-160">All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="a60c9-161">Implikation: das Problem wurde stabilisiert, und die Batch Berechnung kann ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-161">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="a60c9-162">Catch-up: Relevanz gibt an, wann ein Experte ein Beispiel von Dateien überprüft und markiert, die aus einer zusätzlichen Datei Auslastung während eines Szenarios für die parallele Auslastung ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-162">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="a60c9-163">Implikation: Es wurde eine neue Ladung hinzugefügt, und der Nachholbedarf ist erforderlich, um weiter zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a60c9-163">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="a60c9-164">Tag Inkonsistenzen: Prozess identifiziert über einen erweiterten eDiscovery-Algorithmus Inkonsistenzen im Datei Kennzeichnungs Prozess, die sich negativ auf die Analyse auswirken können.</span><span class="sxs-lookup"><span data-stu-id="a60c9-164">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="a60c9-165">Implikation: im nächsten Beispiel werden Dateien enthalten, die in vorherigen Beispielen markiert wurden, und Ihr Tagging muss erneut ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-165">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="a60c9-166">Klassifizierung aktualisieren: ermöglicht dem Benutzer das Anwenden von Markierungs-oder Seeding Änderungen.</span><span class="sxs-lookup"><span data-stu-id="a60c9-166">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="a60c9-167">Implikation: Tagging-und Seeding Änderungen können angewendet werden, ohne dass ein weiteres Beispiel für die Relevanz manuell ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a60c9-167">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="a60c9-168">In der Warteschleife: der Relevanz-Schulungsprozess ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="a60c9-168">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="a60c9-169">Implikation: an dieser Stelle ist keine Relevanz-Schulung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a60c9-169">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="a60c9-170">Obwohl Advanced eDiscovery Sie durch den Prozess führt, mit empfohlenen nächsten Schritten in unterschiedlichen Phasen, können Sie auch zwischen Registerkarten und Seiten navigieren und Entscheidungen treffen, um Situationen zu beheben, die für Ihren Einzelfall, Ihr Problem oder Ihre Prozess zur Dokumentüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="a60c9-170">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="a60c9-171">Es ist möglich, erweiterte eDiscovery-Verarbeitungsoptionen für die nächste Schritt Verarbeitung zu akzeptieren oder zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="a60c9-171">It is possible to accept or override Advanced eDiscovery Next step processing choices.</span></span> <span data-ttu-id="a60c9-172">Wenn Sie einen anderen als den empfohlenen nächsten Schritt ausführen möchten, klicken Sie auf den **nächsten Schritt** , der in der erweiterten Problemanzeige im Dialogfeld angezeigt wird, klicken Sie neben dem nächsten Schritt auf die Schaltfläche **ändern** , und wählen Sie eine andere Option für nächsten Schritt aus.</span><span class="sxs-lookup"><span data-stu-id="a60c9-172">If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a60c9-173">Einige Optionen bleiben nach dem entriegeln möglicherweise deaktiviert, da Sie nicht für die Verwendung an diesem Punkt des Prozesses unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a60c9-173">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="a60c9-174">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a60c9-174">More information</span></span>

[<span data-ttu-id="a60c9-175">Bedeutung der Bewertung</span><span class="sxs-lookup"><span data-stu-id="a60c9-175">Understanding Assessment in Relevance</span></span>](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a60c9-176">Tagging und Bewertung</span><span class="sxs-lookup"><span data-stu-id="a60c9-176">Tagging and Assessment</span></span>](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a60c9-177">Tagging-und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="a60c9-177">Tagging and Relevance training</span></span>](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a60c9-178">Nachverfolgen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="a60c9-178">Tracking Relevance analysis</span></span>](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a60c9-179">Entscheiden basierend auf den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="a60c9-179">Deciding based on the results</span></span>](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="a60c9-180">Testen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="a60c9-180">Testing Relevance analysis</span></span>](../test-relevance-analysis-in-advanced-ediscovery.md)

[<span data-ttu-id="a60c9-181">Abfrage innerhalb des Arbeitssatzes</span><span class="sxs-lookup"><span data-stu-id="a60c9-181">Query within working set</span></span>](working-set-search.md)
