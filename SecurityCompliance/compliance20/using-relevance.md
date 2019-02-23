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
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 53f1906b28c6c6b467e147951e7c55aa7358a4a7
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215435"
---
# <a name="use-the-relevance-module-to-analyze-data-in-advanced-ediscovery-preview"></a><span data-ttu-id="8b368-102">Verwenden des Relevance-Moduls zum Analysieren von Daten in Advanced eDiscovery (Preview)</span><span class="sxs-lookup"><span data-stu-id="8b368-102">Use the Relevance module to analyze data in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="8b368-p101">In Advanced eDiscovery (Preview) enthält das Relevance-Modul die Relevanz von Schulungen und Überprüfungen von Dateien im Zusammenhang mit einem Fall. Der Relevanz-Workflow wird angezeigt und wie folgt beschrieben:</span><span class="sxs-lookup"><span data-stu-id="8b368-p101">In Advanced eDiscovery (Preview), the Relevance module includes the Relevance training and review of files related to a case. The Relevance workflow is shown and described as follows:</span></span>
  
![Relevanzworkflow](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="8b368-106">**Zyklen der Bewertung und Nachverfolgung**:</span><span class="sxs-lookup"><span data-stu-id="8b368-106">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="8b368-107">**Bewertung**: ermöglicht eine frühe Bewertung basierend auf einer Zufallsstichprobe von Dateien und verwendet diese Bewertung, um Entscheidungen zu treffen, um die Leistung des vorher sagenden Codierungsprozesses zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="8b368-107">**Assessment**: Enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="8b368-108">**Track**: berechnen und Anzeigen von Zwischenergebnissen der Bewertung, während die statistische Gültigkeit des Prozesses überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="8b368-108">**Track**: Calculate and display interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="8b368-109">**Zyklen der Schulung und Nachverfolgung**</span><span class="sxs-lookup"><span data-stu-id="8b368-109">**Cycles of training and tracking**</span></span>
    
  - <span data-ttu-id="8b368-110">**Tag**: Advanced EDiscovery (Preview) erfahren Sie anhand der iterativen Überprüfungen und Markierungen einzelner Dateien, welche Relevanz-Kriterien für jedes Problem gelten.</span><span class="sxs-lookup"><span data-stu-id="8b368-110">**Tag**: Advanced eDiscovery (Preview) learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="8b368-111">**Track**: berechnen und Anzeigen von zwischenErgebnissen der Relevanz-Schulung bei gleichzeitiger Überwachung der statistischen Gültigkeit des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="8b368-111">**Track**: Calculate and display interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="8b368-112">**Batch Berechnung**: die akkumulierten und gelernten Relevanz-Kriterien werden auf die gesamte Dateisammlung angewendet, und für jede Datei wird ein relevanzwert generiert.</span><span class="sxs-lookup"><span data-stu-id="8b368-112">**Batch calculation**: The accumulated and learned Relevance criteria is applied to the entire file collection, and a Relevance score is generated for each file.</span></span>
    
- <span data-ttu-id="8b368-113">**Entscheiden**: die Ergebnisse der Analyse, die auf den gesamten Fall angewendet werden, werden nach der Batch Berechnung angezeigt, und es werden Daten zum Überprüfen der Dokumentüberprüfung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8b368-113">**Decide**: The results of the analysis applied to the entire case is displayed after Batch calculation, and data used to make document review decisions is displayed.</span></span>
    
- <span data-ttu-id="8b368-114">**Test**: Ergebnisse können getestet werden, um die Gültigkeit und Wirksamkeit der Advanced EDiscovery (Preview)-Verarbeitung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8b368-114">**Test**: Results can be tested to verify the validity and effectiveness of the Advanced eDiscovery (Preview) processing.</span></span>

- <span data-ttu-id="8b368-115">**Suche**: Sobald der Relevanz-Workflow abgeschlossen ist, können Sie die Ausgabe wie zum Beispiel "Read Perzentil" eines Dokuments für Ihr Problem verwenden, wenn Sie eine Abfrage innerhalb des Arbeitssatzes ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b368-115">**Search**: Once the Relevance workflow is complete, you can use the output such as read percentile of a document for your issue when you run a query within your working set.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="8b368-116">Richtlinien für Relevanz Schulungen und Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="8b368-116">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="8b368-117">Es folgt eine Übersicht über die Richtlinien für die Relevanz von Schulungen und Überprüfungen:</span><span class="sxs-lookup"><span data-stu-id="8b368-117">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="8b368-p102">**Fehler und**Inkonsistenzen: Wenn während des Trainings Markierungsfehler auftreten, kehren Sie zu früheren Datei Beispielen zurück, um Sie zu korrigieren. Wenn zu viele Fehler zu korrigieren sind oder eine neue Perspektive für den Fall oder das Problem vorliegt, sollten die Relevanz-Kriterien vom Administrator neu definiert werden, und das Relevanz-Training wurde erneut gestartet.</span><span class="sxs-lookup"><span data-stu-id="8b368-p102">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them. If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="8b368-120">**Tagging und Schulung**:</span><span class="sxs-lookup"><span data-stu-id="8b368-120">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="8b368-p103">Dateien sollten nur auf der Grundlage von Inhalten gekennzeichnet werden. Berücksichtigen Sie keine Metadaten wie Depot, Datum oder Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="8b368-p103">Files should be tagged based on content only. Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="8b368-123">Beachten Sie beim Taggen von Dateien keine Datumsbereiche im Text.</span><span class="sxs-lookup"><span data-stu-id="8b368-123">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="8b368-124">Berücksichtigen Sie beim Taggen von Dateien keine eingebetteten Grafiken.</span><span class="sxs-lookup"><span data-stu-id="8b368-124">Do not consider embedded graphical images when tagging files.</span></span>
     
  - <span data-ttu-id="8b368-p104">Text ignorieren, der auf Relevanz angewendet wird, wird in der angezeigten Dateiinhalt in der Textansicht relevant entfernt. Wenn die Werte für Ignore Text definiert wurden, nachdem Relevanz Training bereits gestartet wurde, wird der neue ignorierte Text auf Beispieldateien angewendet, die von dem Punkt erstellt wurden, an dem Sie definiert wurde. Das Feature Text ignorieren sollte vorsichtig verwendet werden, da die Verwendung die Leistung der Dateianalyse reduzieren kann.</span><span class="sxs-lookup"><span data-stu-id="8b368-p104">Ignore text applied to Relevance will be removed in the displayed file content in the text view in Relevance. If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined. The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="8b368-p105">Verwenden Sie die Option **Tagging überspringen** nur bei Bedarf. Advanced eDiscovery (Preview) wird nicht basierend auf übersprungenen Dateien trainiert. Wenn es schwierig ist, zu beurteilen, ob eine Datei relevant ist, sollten Sie bei der Bewertung, wann immer möglich, nicht über **springen**, sondern als relevant (R) oder nicht relevant (Nr) markieren. Wenn Advanced eDiscovery (Preview) das Training auswertet, kann dann gesehen werden, wie gut diese Dateitypen verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="8b368-p105">Use the **Skip tagging** option only when necessary. Advanced eDiscovery (Preview) does not train based on skipped files. In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**. When Advanced eDiscovery (Preview) evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="8b368-132">Auch Dateien mit sehr kleinem extrahiertem Text sollten, wenn möglich, als R/NR als "Skip" markiert werden.</span><span class="sxs-lookup"><span data-stu-id="8b368-132">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="8b368-133">Tagging kann sich auf die Klassifizierung auswirken, solange die Datei lesbar ist und als R/NR gekennzeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8b368-133">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="8b368-134">Die Dateisequenz Nummer in der Liste angezeigte Beispieldateien auf der Registerkarte **Tag** ermöglicht es dem Benutzer, zur ursprünglichen angezeigten Reihenfolge der Dateien zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="8b368-134">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="8b368-p106">Sie können zu einem beliebigen Beispiel zurückkehren und das Tagging der Assessment-und Trainingssatz Dateien ändern. Die Änderungen werden beim Erstellen des nächsten Beispiels angewendet.</span><span class="sxs-lookup"><span data-stu-id="8b368-p106">You can go back to any sample and change the tagging of the assessment and training set files. The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="8b368-137">Gescannte Excel-Dateien im PDF-Format sollten beim Taggen von Dateien genauso behandelt werden wie native Excel-Dateien.</span><span class="sxs-lookup"><span data-stu-id="8b368-137">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="8b368-p107">Wenn Sie Zweifel bezüglich des Relevanz-Taggings einer Datei haben, konsultieren Sie einen Experten. Das falsche Tagging während der Relevanz-Schulung kann zu einem späteren Zeitpunkt im Prozess zu Zeitverlusten führen und sich auch negativ auf die Qualität der Gesamtergebnisse auswirken.</span><span class="sxs-lookup"><span data-stu-id="8b368-p107">When in doubt regarding the Relevance tagging of a file, consult an expert. Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="8b368-140">Schlüsselwörter, die in Stichwortlisten definiert wurden, werden in Farben angezeigt, damit der Benutzer relevante Dateien beim taggen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8b368-140">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="8b368-p108">**Batch Berechnung**: Dateien, die vom Experten als R/Nr markiert wurden, erhalten eine Bewertung von 0 oder 100. Dies gilt für das Tagging vor der Batch Berechnung. Wenn der Experte das Problem nach der Batch Berechnung in den Leerlauf umgeschaltet hat und dieses Problem weiterhin kennzeichnet, werden die neu markierten Ergebnisse nicht 100/0, sondern die ursprüngliche Partitur.</span><span class="sxs-lookup"><span data-stu-id="8b368-p108">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100. This applies to tagging made before Batch calculation. If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="8b368-144">**Probleme und Samplingmodus**: Probleme werden normalerweise deaktiviert, wenn die Arbeit an diesen abgeschlossen ist (Relevanz-Schulung wird stabilisiert und die Batch Berechnung durchgeführt), wenn die Probleme abgebrochen werden oder wenn ein anderer Benutzer an den Problemen arbeitet.</span><span class="sxs-lookup"><span data-stu-id="8b368-144">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="8b368-145">Schritte in Relevanz Schulung</span><span class="sxs-lookup"><span data-stu-id="8b368-145">Steps in Relevance training</span></span>

<span data-ttu-id="8b368-p109">Auf der Registerkarte **Relevanz \> verfolgen** bietet Advanced eDiscovery Empfehlungen für die Fortsetzung der Verarbeitung mit den folgenden Schritten. Die Implikationen werden im folgenden beschrieben, wenn jeder der folgenden Schritte im Relevanz-Schulungsprozess empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="8b368-p109">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps. The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="8b368-148">Tagging/Continue Tagging: Dateiüberprüfung und Relevanz-Tagging, die von einem Experten für jede Datei und jedes Problem innerhalb eines Beispiels ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8b368-148">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="8b368-149">Implikation: ein vorhandenes Beispiel muss markiert werden.</span><span class="sxs-lookup"><span data-stu-id="8b368-149">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="8b368-150">Bewertung/Fortsetzung der Bewertung: ermöglicht die vorzeitige Validierung der Relevanz der Groß-/Kleinschreibung und eine vorläufige Ansicht der Relevanz der für den aktuellen Fall importierten Datei Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="8b368-150">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="8b368-151">Implikation: mehr Bewertung ist erforderlich oder empfohlen.</span><span class="sxs-lookup"><span data-stu-id="8b368-151">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="8b368-152">Schulung/Fortbildung: Prozess, bei dem Advanced eDiscovery vom Experten, der die Dateibeispiele kennzeichnet, erlernt und die Möglichkeit erhält, Relevanz-Kriterien für jedes Problem im Kontext jedes Falls zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8b368-152">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="8b368-153">Implikation: das Problem benötigt mehr Schulung; Das nächste Beispiel sollte erstellt und gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8b368-153">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="8b368-p110">Batch Berechnung: Relevanzprozess, bei dem Advanced eDiscovery das während der Schulung erworbene Wissen einnimmt und es auf die gesamte Datei Auffüllung anwenden kann. Alle Dateien in der entsprechenden Dateigruppe werden auf Relevanz ausgewertet und einem Relevanz-Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="8b368-p110">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population. All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="8b368-156">Implikation: das Problem wurde stabilisiert, und die Batch Berechnung kann ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8b368-156">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="8b368-157">Catch-up: Relevanz gibt an, wann ein Experte ein Beispiel von Dateien überprüft und markiert, die aus einer zusätzlichen Datei Auslastung während eines Szenarios für die parallele Auslastung ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="8b368-157">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="8b368-158">Implikation: Es wurde eine neue Ladung hinzugefügt, und der Nachholbedarf ist erforderlich, um weiter zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8b368-158">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="8b368-159">Tag Inkonsistenzen: Prozess identifiziert über einen erweiterten eDiscovery-Algorithmus Inkonsistenzen im Datei Kennzeichnungs Prozess, die sich negativ auf die Analyse auswirken können.</span><span class="sxs-lookup"><span data-stu-id="8b368-159">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="8b368-160">Implikation: im nächsten Beispiel werden Dateien enthalten, die in vorherigen Beispielen markiert wurden, und Ihr Tagging muss erneut ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8b368-160">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="8b368-161">Klassifizierung aktualisieren: ermöglicht dem Benutzer das Anwenden von Markierungs-oder Seeding Änderungen.</span><span class="sxs-lookup"><span data-stu-id="8b368-161">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="8b368-162">Implikation: Tagging-und Seeding Änderungen können angewendet werden, ohne dass ein weiteres Beispiel für die Relevanz manuell ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="8b368-162">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="8b368-163">In der Warteschleife: der Relevanz-Schulungsprozess ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8b368-163">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="8b368-164">Implikation: an dieser Stelle ist keine Relevanz-Schulung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8b368-164">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="8b368-165">Obwohl Advanced eDiscovery Sie durch den Prozess führt, mit empfohlenen nächsten Schritten in unterschiedlichen Phasen, können Sie auch zwischen Registerkarten und Seiten navigieren und Entscheidungen treffen, um Situationen zu beheben, die für Ihren Einzelfall, Ihr Problem oder Ihre Prozess zur Dokumentüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="8b368-165">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="8b368-p111">Es ist möglich, erweiterte eDiscovery-Verarbeitungsoptionen für die nächste Schritt Verarbeitung zu akzeptieren oder zu überschreiben. Wenn Sie einen anderen als den empfohlenen nächsten Schritt ausführen möchten, klicken Sie auf den **nächsten Schritt** , der in der erweiterten Problemanzeige im Dialogfeld angezeigt wird, klicken Sie neben dem nächsten Schritt auf die Schaltfläche **ändern** , und wählen Sie eine andere Option für nächsten Schritt aus.</span><span class="sxs-lookup"><span data-stu-id="8b368-p111">It is possible to accept or override Advanced eDiscovery Next step processing choices. If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8b368-168">Einige Optionen bleiben nach dem entriegeln möglicherweise deaktiviert, da Sie nicht für die Verwendung an diesem Punkt des Prozesses unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8b368-168">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="8b368-169">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8b368-169">More information</span></span>

[<span data-ttu-id="8b368-170">Bedeutung der Bewertung</span><span class="sxs-lookup"><span data-stu-id="8b368-170">Understanding Assessment in Relevance</span></span>](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8b368-171">Tagging und Bewertung</span><span class="sxs-lookup"><span data-stu-id="8b368-171">Tagging and Assessment</span></span>](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8b368-172">Tagging-und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="8b368-172">Tagging and Relevance training</span></span>](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8b368-173">Nachverfolgen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="8b368-173">Tracking Relevance analysis</span></span>](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8b368-174">Entscheiden basierend auf den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="8b368-174">Deciding based on the results</span></span>](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8b368-175">Testen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="8b368-175">Testing Relevance analysis</span></span>](../test-relevance-analysis-in-advanced-ediscovery.md)

[<span data-ttu-id="8b368-176">Abfrage innerhalb des Arbeitssatzes</span><span class="sxs-lookup"><span data-stu-id="8b368-176">Query within working set</span></span>](working-set-search.md)
