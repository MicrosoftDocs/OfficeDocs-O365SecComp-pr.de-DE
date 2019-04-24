---
title: Verwenden des Relevance-Moduls zum Analysieren von Daten nach belegen
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
ms.openlocfilehash: 3aa37a6778947934759eb652a9367559b9ef838b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32257283"
---
# <a name="use-the-relevance-module-to-analyze-data-in-evidence"></a><span data-ttu-id="d4d37-102">Verwenden des Relevance-Moduls zum Analysieren von Daten nach belegen</span><span class="sxs-lookup"><span data-stu-id="d4d37-102">Use the Relevance module to analyze data in evidence</span></span>

<span data-ttu-id="d4d37-103">In Daten Untersuchungen (Preview) enthält das Relevanz-Modul die Relevanz von Schulungen und die Überprüfung von Dateien im Zusammenhang mit einer Untersuchung.</span><span class="sxs-lookup"><span data-stu-id="d4d37-103">In Data Investigations (Preview), the Relevance module includes the Relevance training and review of files related to an investigation.</span></span> <span data-ttu-id="d4d37-104">Der Relevanz-Workflow wird angezeigt und wie folgt beschrieben:</span><span class="sxs-lookup"><span data-stu-id="d4d37-104">The Relevance workflow is shown and described as follows:</span></span>
  
![Relevanz-Workflow](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="d4d37-106">**Zyklen der Bewertung und Nachverfolgung**:</span><span class="sxs-lookup"><span data-stu-id="d4d37-106">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="d4d37-107">**Bewertung**: ermöglicht eine frühe Bewertung basierend auf einer Zufallsstichprobe von Dateien und verwendet diese Bewertung, um Entscheidungen zu treffen, um die Leistung des vorher sagenden Codierungsprozesses zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="d4d37-107">**Assessment**: Enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="d4d37-108">**Track**: berechnen und Anzeigen von Zwischenergebnissen der Bewertung, während die statistische Gültigkeit des Prozesses überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="d4d37-108">**Track**: Calculate and display interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="d4d37-109">**Zyklen der Schulung und Nachverfolgung**</span><span class="sxs-lookup"><span data-stu-id="d4d37-109">**Cycles of training and tracking**</span></span>
    
  - <span data-ttu-id="d4d37-110">**Tag**: Daten Untersuchungen (Preview) erfahren Sie anhand der iterativen Überprüfung und des Taggings einzelner Dateien, welche Relevanz-Kriterien für jedes Problem gelten.</span><span class="sxs-lookup"><span data-stu-id="d4d37-110">**Tag**: Data Investigations (Preview) learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="d4d37-111">**Track**: berechnen und Anzeigen von zwischenErgebnissen der Relevanz-Schulung bei gleichzeitiger Überwachung der statistischen Gültigkeit des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="d4d37-111">**Track**: Calculate and display interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="d4d37-112">**Batch Berechnung**: die akkumulierten und gelernten Relevanz-Kriterien werden auf die gesamte Dateisammlung angewendet, und für jede Datei wird ein relevanzwert generiert.</span><span class="sxs-lookup"><span data-stu-id="d4d37-112">**Batch calculation**: The accumulated and learned Relevance criteria is applied to the entire file collection, and a Relevance score is generated for each file.</span></span>
    
- <span data-ttu-id="d4d37-113">**Entscheiden**: die Ergebnisse der Analyse, die auf den gesamten Fall angewendet werden, werden nach der Batch Berechnung angezeigt, und es werden Daten zum Überprüfen der Dokumentüberprüfung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4d37-113">**Decide**: The results of the analysis applied to the entire case is displayed after Batch calculation, and data used to make document review decisions is displayed.</span></span>
    
- <span data-ttu-id="d4d37-114">**Test**: Ergebnisse können getestet werden, um die Gültigkeit und Wirksamkeit der Daten Untersuchungen (Vorschau) zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="d4d37-114">**Test**: Results can be tested to verify the validity and effectiveness of the Data Investigations (Preview) processing.</span></span>

- <span data-ttu-id="d4d37-115">**Suche**: Sobald der Relevanz-Workflow abgeschlossen ist, können Sie die Ausgabe wie zum Beispiel "Read Perzentil" eines Dokuments für Ihr Problem verwenden, wenn Sie eine Abfrage innerhalb des Arbeitssatzes ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4d37-115">**Search**: Once the Relevance workflow is complete, you can use the output such as read percentile of a document for your issue when you run a query within your working set.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="d4d37-116">Richtlinien für Relevanz Schulungen und Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="d4d37-116">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="d4d37-117">Es folgt eine Übersicht über die Richtlinien für die Relevanz von Schulungen und Überprüfungen:</span><span class="sxs-lookup"><span data-stu-id="d4d37-117">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="d4d37-118">**Fehler und**Inkonsistenzen: Wenn während des Trainings Markierungsfehler auftreten, kehren Sie zu früheren Datei Beispielen zurück, um Sie zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="d4d37-118">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them.</span></span> <span data-ttu-id="d4d37-119">Wenn zu viele Fehler zu korrigieren sind oder eine neue Perspektive für den Fall oder das Problem vorliegt, sollten die Relevanz-Kriterien vom Administrator neu definiert werden, und das Relevanz-Training wurde erneut gestartet.</span><span class="sxs-lookup"><span data-stu-id="d4d37-119">If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="d4d37-120">**Tagging und Schulung**:</span><span class="sxs-lookup"><span data-stu-id="d4d37-120">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="d4d37-121">Dateien sollten nur auf der Grundlage von Inhalten gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-121">Files should be tagged based on content only.</span></span> <span data-ttu-id="d4d37-122">Berücksichtigen Sie keine Metadaten wie Depot, Datum oder Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="d4d37-122">Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="d4d37-123">Beachten Sie beim Taggen von Dateien keine Datumsbereiche im Text.</span><span class="sxs-lookup"><span data-stu-id="d4d37-123">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="d4d37-124">Berücksichtigen Sie beim Taggen von Dateien keine eingebetteten Grafiken.</span><span class="sxs-lookup"><span data-stu-id="d4d37-124">Do not consider embedded graphical images when tagging files.</span></span>
     
  - <span data-ttu-id="d4d37-125">Text ignorieren, der auf Relevanz angewendet wird, wird in der angezeigten Dateiinhalt in der Textansicht relevant entfernt.</span><span class="sxs-lookup"><span data-stu-id="d4d37-125">Ignore text applied to Relevance will be removed in the displayed file content in the text view in Relevance.</span></span> <span data-ttu-id="d4d37-126">Wenn die Werte für Ignore Text definiert wurden, nachdem Relevanz Training bereits gestartet wurde, wird der neue ignorierte Text auf Beispieldateien angewendet, die von dem Punkt erstellt wurden, an dem Sie definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d4d37-126">If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined.</span></span> <span data-ttu-id="d4d37-127">Das Feature Text ignorieren sollte vorsichtig verwendet werden, da die Verwendung die Leistung der Dateianalyse reduzieren kann.</span><span class="sxs-lookup"><span data-stu-id="d4d37-127">The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="d4d37-128">Verwenden Sie die Option **Tagging überspringen** nur bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d4d37-128">Use the **Skip tagging** option only when necessary.</span></span> <span data-ttu-id="d4d37-129">Daten Untersuchungen (Preview) werden nicht basierend auf übersprungenen Dateien trainiert.</span><span class="sxs-lookup"><span data-stu-id="d4d37-129">Data Investigations (Preview) does not train based on skipped files.</span></span> <span data-ttu-id="d4d37-130">Wenn es schwierig ist, zu beurteilen, ob eine Datei relevant ist, sollten Sie bei der Bewertung, wann immer möglich, nicht über **springen**, sondern als relevant (R) oder nicht relevant (Nr) markieren.</span><span class="sxs-lookup"><span data-stu-id="d4d37-130">In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**.</span></span> <span data-ttu-id="d4d37-131">Wenn Daten Untersuchungen (Preview) das Training auswertet, kann dann gesehen werden, wie gut diese Dateitypen verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-131">When Data Investigations (Preview) evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="d4d37-132">Auch Dateien mit sehr kleinem extrahiertem Text sollten, wenn möglich, als R/NR als "Skip" markiert werden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-132">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="d4d37-133">Tagging kann sich auf die Klassifizierung auswirken, solange die Datei lesbar ist und als R/NR gekennzeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4d37-133">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="d4d37-134">Die Dateisequenz Nummer in der Liste angezeigte Beispieldateien auf der Registerkarte **Tag** ermöglicht es dem Benutzer, zur ursprünglichen angezeigten Reihenfolge der Dateien zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="d4d37-134">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="d4d37-135">Sie können zu einem beliebigen Beispiel zurückkehren und das Tagging der Assessment-und Trainingssatz Dateien ändern.</span><span class="sxs-lookup"><span data-stu-id="d4d37-135">You can go back to any sample and change the tagging of the assessment and training set files.</span></span> <span data-ttu-id="d4d37-136">Die Änderungen werden beim Erstellen des nächsten Beispiels angewendet.</span><span class="sxs-lookup"><span data-stu-id="d4d37-136">The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="d4d37-137">Gescannte Excel-Dateien im PDF-Format sollten beim Taggen von Dateien genauso behandelt werden wie native Excel-Dateien.</span><span class="sxs-lookup"><span data-stu-id="d4d37-137">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="d4d37-138">Wenn Sie Zweifel bezüglich des Relevanz-Taggings einer Datei haben, konsultieren Sie einen Experten.</span><span class="sxs-lookup"><span data-stu-id="d4d37-138">When in doubt regarding the Relevance tagging of a file, consult an expert.</span></span> <span data-ttu-id="d4d37-139">Das falsche Tagging während der Relevanz-Schulung kann zu einem späteren Zeitpunkt im Prozess zu Zeitverlusten führen und sich auch negativ auf die Qualität der Gesamtergebnisse auswirken.</span><span class="sxs-lookup"><span data-stu-id="d4d37-139">Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="d4d37-140">Schlüsselwörter, die in Stichwortlisten definiert wurden, werden in Farben angezeigt, damit der Benutzer relevante Dateien beim taggen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d4d37-140">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="d4d37-141">**Batch Berechnung**: Dateien, die vom Experten als R/Nr markiert wurden, erhalten eine Bewertung von 0 oder 100.</span><span class="sxs-lookup"><span data-stu-id="d4d37-141">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100.</span></span> <span data-ttu-id="d4d37-142">Dies gilt für das Tagging vor der Batch Berechnung.</span><span class="sxs-lookup"><span data-stu-id="d4d37-142">This applies to tagging made before Batch calculation.</span></span> <span data-ttu-id="d4d37-143">Wenn der Experte das Problem nach der Batch Berechnung in den Leerlauf umgeschaltet hat und dieses Problem weiterhin kennzeichnet, werden die neu markierten Ergebnisse nicht 100/0, sondern die ursprüngliche Partitur.</span><span class="sxs-lookup"><span data-stu-id="d4d37-143">If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="d4d37-144">**Probleme und Samplingmodus**: Probleme werden normalerweise deaktiviert, wenn die Arbeit an diesen abgeschlossen ist (Relevanz-Schulung wird stabilisiert und die Batch Berechnung durchgeführt), wenn die Probleme abgebrochen werden oder wenn ein anderer Benutzer an den Problemen arbeitet.</span><span class="sxs-lookup"><span data-stu-id="d4d37-144">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="d4d37-145">Schritte in Relevanz Schulung</span><span class="sxs-lookup"><span data-stu-id="d4d37-145">Steps in Relevance training</span></span>

<span data-ttu-id="d4d37-146">Auf der Registerkarte **Relevanz \> verfolgen** werden mit den folgenden Schritten Empfehlungen zur Verarbeitung von Daten untersucht.</span><span class="sxs-lookup"><span data-stu-id="d4d37-146">In the **Relevance \> Track** tab, Data investigations provides recommendations on how to proceed in the processing, with the following next steps.</span></span> <span data-ttu-id="d4d37-147">Die Implikationen werden im folgenden beschrieben, wenn jeder der folgenden Schritte im Relevanz-Schulungsprozess empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="d4d37-147">The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="d4d37-148">Tagging/Continue Tagging: Dateiüberprüfung und Relevanz-Tagging, die von einem Experten für jede Datei und jedes Problem innerhalb eines Beispiels ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-148">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="d4d37-149">Implikation: ein vorhandenes Beispiel muss markiert werden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-149">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="d4d37-150">Bewertung/Fortsetzung der Bewertung: ermöglicht die vorzeitige Validierung der Relevanz der Groß-/Kleinschreibung und eine vorläufige Ansicht der Relevanz der für den aktuellen Fall importierten Datei Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="d4d37-150">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="d4d37-151">Implikation: mehr Bewertung ist erforderlich oder empfohlen.</span><span class="sxs-lookup"><span data-stu-id="d4d37-151">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="d4d37-152">Schulung/Fortbildung: Prozess, bei dem Daten Untersuchungen vom Experten erlernt werden, der die Dateibeispiele kennzeichnet und die Möglichkeit erhält, Relevanz-Kriterien zu identifizieren, die für jedes Problem im Kontext jedes Falls relevant sind.</span><span class="sxs-lookup"><span data-stu-id="d4d37-152">Training / Continue training: Process during which Data investigations learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="d4d37-153">Implikation: das Problem benötigt mehr Schulung; Das nächste Beispiel sollte erstellt und gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-153">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="d4d37-154">Batch Berechnung: Relevanzprozess, bei dem Daten Untersuchungen das während der Schulung erworbene Wissen übernehmen und auf die gesamte Datei Auffüllung anwenden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-154">Batch calculation: Relevance process in which Data investigations takes the knowledge acquired during the training stage and applies it to the entire file population.</span></span> <span data-ttu-id="d4d37-155">Alle Dateien in der entsprechenden Dateigruppe werden auf Relevanz ausgewertet und einem Relevanz-Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d4d37-155">All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="d4d37-156">Implikation: das Problem wurde stabilisiert, und die Batch Berechnung kann ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-156">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="d4d37-157">Catch-up: Relevanz gibt an, wann ein Experte ein Beispiel von Dateien überprüft und markiert, die aus einer zusätzlichen Datei Auslastung während eines Szenarios für die parallele Auslastung ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-157">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="d4d37-158">Implikation: Es wurde eine neue Ladung hinzugefügt, und der Nachholbedarf ist erforderlich, um weiter zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d4d37-158">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="d4d37-159">Tag Inkonsistenzen: Prozess identifiziert über einen Daten Ermittlungs Algorithmus Inkonsistenzen im Datei Kennzeichnungs Prozess, die sich negativ auf die Analyse auswirken können.</span><span class="sxs-lookup"><span data-stu-id="d4d37-159">Tag inconsistencies: Process identifies, via an Data investigations algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="d4d37-160">Implikation: im nächsten Beispiel werden Dateien enthalten, die in vorherigen Beispielen markiert wurden, und Ihr Tagging muss erneut ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-160">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="d4d37-161">Klassifizierung aktualisieren: ermöglicht dem Benutzer das Anwenden von Markierungs-oder Seeding Änderungen.</span><span class="sxs-lookup"><span data-stu-id="d4d37-161">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="d4d37-162">Implikation: Tagging-und Seeding Änderungen können angewendet werden, ohne dass ein weiteres Beispiel für die Relevanz manuell ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d4d37-162">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="d4d37-163">In der Warteschleife: der Relevanz-Schulungsprozess ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d4d37-163">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="d4d37-164">Implikation: an dieser Stelle ist keine Relevanz-Schulung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4d37-164">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="d4d37-165">Daten Untersuchungen führen Sie zwar durch den Prozess, mit empfohlenen nächsten Schritten in unterschiedlichen Phasen können Sie aber auch zwischen Registerkarten und Seiten navigieren und Entscheidungen treffen, um Situationen zu behandeln, die für Ihren Einzelfall, Ihr Problem oder Ihre Prozess zur Dokumentüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="d4d37-165">Although Data investigations guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="d4d37-166">Es ist möglich, Daten Untersuchungen zu akzeptieren oder zu überschreiben, die bei der Verarbeitung von Auswahlmöglichkeiten auftreten.</span><span class="sxs-lookup"><span data-stu-id="d4d37-166">It is possible to accept or override Data investigations Next step processing choices.</span></span> <span data-ttu-id="d4d37-167">Wenn Sie einen anderen als den empfohlenen nächsten Schritt ausführen möchten, klicken Sie auf den **nächsten Schritt** , der in der erweiterten Problemanzeige im Dialogfeld angezeigt wird, klicken Sie neben dem nächsten Schritt auf die Schaltfläche **ändern** , und wählen Sie eine andere Option für nächsten Schritt aus.</span><span class="sxs-lookup"><span data-stu-id="d4d37-167">If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d4d37-168">Einige Optionen bleiben nach dem entriegeln möglicherweise deaktiviert, da Sie nicht für die Verwendung an diesem Punkt des Prozesses unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d4d37-168">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="d4d37-169">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4d37-169">More information</span></span>

[<span data-ttu-id="d4d37-170">Bedeutung der Bewertung</span><span class="sxs-lookup"><span data-stu-id="d4d37-170">Understanding Assessment in Relevance</span></span>](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d4d37-171">Tagging und Bewertung</span><span class="sxs-lookup"><span data-stu-id="d4d37-171">Tagging and assessment</span></span>](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d4d37-172">Tagging-und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="d4d37-172">Tagging and Relevance training</span></span>](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d4d37-173">Nachverfolgen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="d4d37-173">Tracking Relevance analysis</span></span>](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d4d37-174">Entscheiden basierend auf den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="d4d37-174">Deciding based on the results</span></span>](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="d4d37-175">Testen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="d4d37-175">Testing Relevance analysis</span></span>](../test-relevance-analysis-in-advanced-ediscovery.md)

[<span data-ttu-id="d4d37-176">Abfragen der Daten nach belegen</span><span class="sxs-lookup"><span data-stu-id="d4d37-176">Query the data in evidence</span></span>](evidence-query.md)
