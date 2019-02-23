---
title: Verwenden des Relevanz-Moduls in Office 365 Advanced eDiscovery
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: 'Erfahren Sie mehr über das Relevanz-Modul in Office 365 Advanced eDiscovery, einschließlich eines Workflows und Richtlinien und Schritte für Schulung und Dateiüberprüfung.  '
ms.openlocfilehash: ad44066c8b00bccacf1f4fe2088aa84096c4db84
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217455"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="4a06b-103">Verwenden des Relevanz-Moduls in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4a06b-103">Use the Relevance module in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="4a06b-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="4a06b-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="4a06b-p102">In Advanced eDiscovery umfasst das Relevance-Modul die Relevanz von Schulungen und Überprüfungen von Dateien im Zusammenhang mit einem Fall. Der Relevanz-Workflow wird angezeigt und wie folgt beschrieben:</span><span class="sxs-lookup"><span data-stu-id="4a06b-p102">In Advanced eDiscovery, the Relevance module includes the Relevance training and review of files related to a case. The Relevance workflow is shown and described as follows:</span></span>
  
![Relevanzworkflow](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="4a06b-109">**Zyklen der Bewertung und Nachverfolgung**:</span><span class="sxs-lookup"><span data-stu-id="4a06b-109">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="4a06b-110">**Bewertung**: Advanced eDiscovery ermöglicht eine frühe Bewertung basierend auf einer Zufallsstichprobe von Dateien und verwendet diese Bewertung, um Entscheidungen zu treffen, um die Leistung des vorher sagenden Codierungsprozesses zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4a06b-110">**Assessment**: Advanced eDiscovery enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="4a06b-111">**Track**: Erweiterte eDiscovery berechnet und zeigt Zwischenergebnisse der Bewertung an, während die statistische Gültigkeit des Prozesses überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="4a06b-111">**Track**: Advanced eDiscovery calculates and displays interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="4a06b-112">**Schulungs-und Überwachungs Zyklen**:</span><span class="sxs-lookup"><span data-stu-id="4a06b-112">**Cycles of training and tracking**:</span></span>
    
  - <span data-ttu-id="4a06b-113">**Tag**: Advanced eDiscovery lernt anhand der iterativen Überprüfungen und Markierungen von einzelnen Dateien, welche Relevanz-Kriterien für jedes Problem gelten.</span><span class="sxs-lookup"><span data-stu-id="4a06b-113">**Tag**: Advanced eDiscovery learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="4a06b-114">**Track**: Erweiterte eDiscovery berechnet und zeigt zwischenErgebnisse der Relevanz-Schulung, während die statistische Gültigkeit des Prozesses überwacht wird.</span><span class="sxs-lookup"><span data-stu-id="4a06b-114">**Track**: Advanced eDiscovery calculates and displays interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="4a06b-115">**Batch Berechnung**: die erweiterte eDiscovery verwendet die akkumulierten und erlernten Relevanz-Kriterien, wendet Sie auf die gesamte Dateisammlung an und generiert Relevanzwerte für jede Datei.</span><span class="sxs-lookup"><span data-stu-id="4a06b-115">**Batch calculation**: Advanced eDiscovery takes the accumulated and learned Relevance criteria, applies it to the entire file collection, and generates Relevance scores for each file.</span></span>
    
- <span data-ttu-id="4a06b-116">**Entscheiden**: Advanced eDiscovery zeigt die Ergebnisse der Analyse an, die nach der Batch Berechnung auf den gesamten Fall angewendet werden, und zeigt Daten zum Durchführen von Dokument Überprüfungs Entscheidungen an.</span><span class="sxs-lookup"><span data-stu-id="4a06b-116">**Decide**: Advanced eDiscovery displays the results of the analysis applied to the entire case after Batch calculation and displays data for making document review decisions.</span></span>
    
- <span data-ttu-id="4a06b-117">**Test**: Erweiterte eDiscovery-Ergebnisse können getestet werden, um die Gültigkeit und Wirksamkeit der erweiterten eDiscovery-Verarbeitung zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4a06b-117">**Test**: Advanced eDiscovery results can be tested to verify the validity and effectiveness of the Advanced eDiscovery processing.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="4a06b-118">Richtlinien für Relevanz Schulungen und Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="4a06b-118">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="4a06b-119">Es folgt eine Übersicht über die Richtlinien für die Relevanz von Schulungen und Überprüfungen:</span><span class="sxs-lookup"><span data-stu-id="4a06b-119">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="4a06b-p103">**Fehler und**Inkonsistenzen: Wenn während des Trainings Markierungsfehler auftreten, kehren Sie zu früheren Datei Beispielen zurück, um Sie zu korrigieren. Wenn zu viele Fehler zu korrigieren sind oder eine neue Perspektive für den Fall oder das Problem vorliegt, sollten die Relevanz-Kriterien vom Administrator neu definiert werden, und das Relevanz-Training wurde erneut gestartet.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p103">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them. If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="4a06b-122">**Tagging und Schulung**:</span><span class="sxs-lookup"><span data-stu-id="4a06b-122">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="4a06b-p104">Dateien sollten nur auf der Grundlage von Inhalten gekennzeichnet werden. Berücksichtigen Sie keine Metadaten wie Depot, Datum oder Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p104">Files should be tagged based on content only. Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="4a06b-125">Beachten Sie beim Taggen von Dateien keine Datumsbereiche im Text.</span><span class="sxs-lookup"><span data-stu-id="4a06b-125">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="4a06b-126">Berücksichtigen Sie beim Taggen von Dateien keine eingebetteten Grafiken.</span><span class="sxs-lookup"><span data-stu-id="4a06b-126">Do not consider embedded graphical images when tagging files.</span></span>
    
  - <span data-ttu-id="4a06b-p105">Wenn Sie eine Datei mit dem Symbol für die **formatierte Textansicht** beim Markieren anzeigen, sollten Sie die Formatierung von Text nicht berücksichtigen. Beispielsweise wird ein Wort, das durchgestrichen angezeigt wird (eine horizontale Linie durch sein Zentrum, die den Löschvorgang angibt) weiterhin als Teil des analysierten Texts als relevant betrachtet.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p105">If viewing a file using the **formatted text view** icon while tagging, do not consider the formatting of text. For example, a word displayed with a strikethrough (a horizontal line through its center indicating deletion) is still considered by Relevance as part of the analyzed text.</span></span> 
    
  - <span data-ttu-id="4a06b-p106">Text ignorieren, der auf Relevanz angewendet wird (wie vom Fall-Manager oder Administrator festgelegt) wird in der angezeigten Dateiinhalt in der Textansicht relevant entfernt. Wenn die Werte für Ignore Text definiert wurden, nachdem Relevanz Training bereits gestartet wurde, wird der neue ignorierte Text auf Beispieldateien angewendet, die von dem Punkt erstellt wurden, an dem Sie definiert wurde. Das Feature Text ignorieren sollte vorsichtig verwendet werden, da die Verwendung die Leistung der Dateianalyse reduzieren kann.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p106">Ignore text applied to Relevance (as set by the Case Manager or Administrator) will be removed in the displayed file content in the text view in Relevance. If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined. The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="4a06b-p107">Verwenden Sie die Option **Tagging überspringen** nur bei Bedarf. Erweiterte eDiscovery wird nicht basierend auf übersprungenen Dateien trainiert. Wenn es schwierig ist, zu beurteilen, ob eine Datei relevant ist, sollten Sie bei der Bewertung, wann immer möglich, nicht über **springen**, sondern als relevant (R) oder nicht relevant (Nr) markieren. Wenn Advanced eDiscovery das Training auswertet, kann dann gesehen werden, wie gut diese Dateitypen verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p107">Use the **Skip tagging** option only when necessary. Advanced eDiscovery does not train based on skipped files. In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**. When Advanced eDiscovery evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="4a06b-136">Auch Dateien mit sehr kleinem extrahiertem Text sollten, wenn möglich, als R/NR als "Skip" markiert werden.</span><span class="sxs-lookup"><span data-stu-id="4a06b-136">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="4a06b-137">Tagging kann sich auf die Klassifizierung auswirken, solange die Datei lesbar ist und als R/NR gekennzeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4a06b-137">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="4a06b-138">Die Dateisequenz Nummer in der Liste angezeigte Beispieldateien auf der Registerkarte **Tag** ermöglicht es dem Benutzer, zur ursprünglichen angezeigten Reihenfolge der Dateien zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="4a06b-138">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="4a06b-p108">Sie können zu einem beliebigen Beispiel zurückkehren und das Tagging der Assessment-und Trainingssatz Dateien ändern. Die Änderungen werden beim Erstellen des nächsten Beispiels angewendet.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p108">You can go back to any sample and change the tagging of the assessment and training set files. The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="4a06b-141">Gescannte Excel-Dateien im PDF-Format sollten beim Taggen von Dateien genauso behandelt werden wie native Excel-Dateien.</span><span class="sxs-lookup"><span data-stu-id="4a06b-141">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="4a06b-p109">Wenn Sie Zweifel bezüglich des Relevanz-Taggings einer Datei haben, konsultieren Sie einen Experten. Das falsche Tagging während der Relevanz-Schulung kann zu einem späteren Zeitpunkt im Prozess zu Zeitverlusten führen und sich auch negativ auf die Qualität der Gesamtergebnisse auswirken.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p109">When in doubt regarding the Relevance tagging of a file, consult an expert. Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="4a06b-144">Schlüsselwörter, die in Stichwortlisten definiert wurden, werden in Farben angezeigt, damit der Benutzer relevante Dateien beim taggen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4a06b-144">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="4a06b-p110">**Batch Berechnung**: Dateien, die vom Experten als R/Nr markiert wurden, erhalten eine Bewertung von 0 oder 100. Dies gilt für das Tagging vor der Batch Berechnung. Wenn der Experte das Problem nach der Batch Berechnung in den Leerlauf umgeschaltet hat und dieses Problem weiterhin kennzeichnet, werden die neu markierten Ergebnisse nicht 100/0, sondern die ursprüngliche Partitur.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p110">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100. This applies to tagging made before Batch calculation. If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="4a06b-148">**Probleme und Samplingmodus**: Probleme werden normalerweise deaktiviert, wenn die Arbeit an diesen abgeschlossen ist (Relevanz-Schulung wird stabilisiert und die Batch Berechnung durchgeführt), wenn die Probleme abgebrochen werden oder wenn ein anderer Benutzer an den Problemen arbeitet.</span><span class="sxs-lookup"><span data-stu-id="4a06b-148">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="4a06b-149">Schritte in Relevanz Schulung</span><span class="sxs-lookup"><span data-stu-id="4a06b-149">Steps in Relevance training</span></span>

<span data-ttu-id="4a06b-p111">Auf der Registerkarte **Relevanz \> verfolgen** bietet Advanced eDiscovery Empfehlungen für die Fortsetzung der Verarbeitung mit den folgenden Schritten. Die Implikationen werden im folgenden beschrieben, wenn jeder der folgenden Schritte im Relevanz-Schulungsprozess empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p111">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps. The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="4a06b-152">Tagging/Continue Tagging: Dateiüberprüfung und Relevanz-Tagging, die von einem Experten für jede Datei und jedes Problem innerhalb eines Beispiels ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4a06b-152">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="4a06b-153">Implikation: ein vorhandenes Beispiel muss markiert werden.</span><span class="sxs-lookup"><span data-stu-id="4a06b-153">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="4a06b-154">Bewertung/Fortsetzung der Bewertung: ermöglicht die vorzeitige Validierung der Relevanz der Groß-/Kleinschreibung und eine vorläufige Ansicht der Relevanz der für den aktuellen Fall importierten Datei Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="4a06b-154">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="4a06b-155">Implikation: mehr Bewertung ist erforderlich oder empfohlen.</span><span class="sxs-lookup"><span data-stu-id="4a06b-155">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="4a06b-156">Schulung/Fortbildung: Prozess, bei dem Advanced eDiscovery vom Experten, der die Dateibeispiele kennzeichnet, erlernt und die Möglichkeit erhält, Relevanz-Kriterien für jedes Problem im Kontext jedes Falls zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4a06b-156">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="4a06b-157">Implikation: das Problem benötigt mehr Schulung; Das nächste Beispiel sollte erstellt und gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4a06b-157">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="4a06b-p112">Batch Berechnung: Relevanzprozess, bei dem Advanced eDiscovery das während der Schulung erworbene Wissen einnimmt und es auf die gesamte Datei Auffüllung anwenden kann. Alle Dateien in der entsprechenden Dateigruppe werden auf Relevanz ausgewertet und einem Relevanz-Wert zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p112">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population. All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="4a06b-160">Implikation: das Problem wurde stabilisiert, und die Batch Berechnung kann ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4a06b-160">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="4a06b-161">Catch-up: Relevanz gibt an, wann ein Experte ein Beispiel von Dateien überprüft und markiert, die aus einer zusätzlichen Datei Auslastung während eines Szenarios für die parallele Auslastung ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="4a06b-161">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="4a06b-162">Implikation: Es wurde eine neue Ladung hinzugefügt, und der Nachholbedarf ist erforderlich, um weiter zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4a06b-162">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="4a06b-163">Tag Inkonsistenzen: Prozess identifiziert über einen erweiterten eDiscovery-Algorithmus Inkonsistenzen im Datei Kennzeichnungs Prozess, die sich negativ auf die Analyse auswirken können.</span><span class="sxs-lookup"><span data-stu-id="4a06b-163">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="4a06b-164">Implikation: im nächsten Beispiel werden Dateien enthalten, die in vorherigen Beispielen markiert wurden, und Ihr Tagging muss erneut ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4a06b-164">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="4a06b-165">Klassifizierung aktualisieren: ermöglicht dem Benutzer das Anwenden von Markierungs-oder Seeding Änderungen.</span><span class="sxs-lookup"><span data-stu-id="4a06b-165">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="4a06b-166">Implikation: Tagging-und Seeding Änderungen können angewendet werden, ohne dass ein weiteres Beispiel für die Relevanz manuell ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="4a06b-166">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="4a06b-167">In der Warteschleife: der Relevanz-Schulungsprozess ist abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4a06b-167">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="4a06b-168">Implikation: an dieser Stelle ist keine Relevanz-Schulung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4a06b-168">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="4a06b-169">Obwohl Advanced eDiscovery Sie durch den Prozess führt, mit empfohlenen nächsten Schritten in unterschiedlichen Phasen, können Sie auch zwischen Registerkarten und Seiten navigieren und Entscheidungen treffen, um Situationen zu beheben, die für Ihren Einzelfall, Ihr Problem oder Ihre Prozess zur Dokumentüberprüfung.</span><span class="sxs-lookup"><span data-stu-id="4a06b-169">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="4a06b-p113">Es ist möglich, erweiterte eDiscovery-Verarbeitungsoptionen für die nächste Schritt Verarbeitung zu akzeptieren oder zu überschreiben. Wenn Sie einen anderen als den empfohlenen nächsten Schritt ausführen möchten, klicken Sie auf den **nächsten Schritt** , der in der erweiterten Problemanzeige im Dialogfeld angezeigt wird, klicken Sie neben dem nächsten Schritt auf die Schaltfläche **ändern** , und wählen Sie eine andere Option für nächsten Schritt aus.</span><span class="sxs-lookup"><span data-stu-id="4a06b-p113">It is possible to accept or override Advanced eDiscovery Next step processing choices. If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4a06b-172">Einige Optionen bleiben nach dem entriegeln möglicherweise deaktiviert, da Sie nicht für die Verwendung an diesem Punkt des Prozesses unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="4a06b-172">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4a06b-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a06b-173">See also</span></span>

[<span data-ttu-id="4a06b-174">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="4a06b-174">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="4a06b-175">Bedeutung der Bewertung</span><span class="sxs-lookup"><span data-stu-id="4a06b-175">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4a06b-176">Tagging und Bewertung</span><span class="sxs-lookup"><span data-stu-id="4a06b-176">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4a06b-177">Tagging-und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="4a06b-177">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4a06b-178">Nachverfolgen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="4a06b-178">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4a06b-179">Entscheiden basierend auf den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="4a06b-179">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="4a06b-180">Testen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="4a06b-180">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

