---
title: Verwenden Sie das Modul Relevanz in Office 365 erweiterte eDiscovery
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: 'Lernen Sie das Modul Relevanz in Office 365 erweiterte eDiscovery, einschließlich eines Workflows und Richtlinien und Schritte zur Schulung und Datei überprüfen.  '
ms.openlocfilehash: 2cf75ef95291c5393367ce01fb0cd660f9b99145
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529212"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="30e90-103">Verwenden Sie das Modul Relevanz in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="30e90-103">Use the Relevance module in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="30e90-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="30e90-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="30e90-p102">Erweiterte eDiscovery enthält das Modul Relevanz der Relevanz Schulung und Überprüfung von Dateien im Zusammenhang mit der Fall. Der Relevanz Workflow wird angezeigt und wie folgt beschrieben:</span><span class="sxs-lookup"><span data-stu-id="30e90-p102">In Advanced eDiscovery, the Relevance module includes the Relevance training and review of files related to a case. The Relevance workflow is shown and described as follows:</span></span>
  
![Relevanzworkflow](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- <span data-ttu-id="30e90-109">**Zyklen der Bewertung und Nachverfolgen von Änderungen**:</span><span class="sxs-lookup"><span data-stu-id="30e90-109">**Cycles of assessment and tracking**:</span></span>
    
  - <span data-ttu-id="30e90-110">**Assessment**: Erweiterte eDiscovery ermöglicht frühe Assessment basierend auf einer Stichprobe von Dateien und wird mit dieser Bewertung Entscheidungen, die Leistung der vorhersehbare Codierung bestimmen angewendet.</span><span class="sxs-lookup"><span data-stu-id="30e90-110">**Assessment**: Advanced eDiscovery enables early assessment based on a random sample of files and uses this assessment to apply decisions to determine the performance of the predictive coding process.</span></span> 
    
  - <span data-ttu-id="30e90-111">**Titel**: Erweiterte eDiscovery berechnet und anzeigt Zwischenergebnisse der Bewertung bei der Überwachung statistische Gültigkeit des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="30e90-111">**Track**: Advanced eDiscovery calculates and displays interim results of the assessment while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="30e90-112">**Zyklen Schulung und Nachverfolgen von Änderungen**:</span><span class="sxs-lookup"><span data-stu-id="30e90-112">**Cycles of training and tracking**:</span></span>
    
  - <span data-ttu-id="30e90-113">**Tag**: Erweiterte eDiscovery lernen Relevanz Kriterien speziell für jedes Problem basierend auf der Experte iterative überprüfen und Kategorien der einzelnen Dateien.</span><span class="sxs-lookup"><span data-stu-id="30e90-113">**Tag**: Advanced eDiscovery learns Relevance criteria specific to each issue based on the expert's iterative review and tagging of individual files.</span></span>
    
  - <span data-ttu-id="30e90-114">**Titel**: Erweiterte eDiscovery berechnet und anzeigt Zwischenergebnisse der Schulung Relevanz bei der Überwachung statistische Gültigkeit des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="30e90-114">**Track**: Advanced eDiscovery calculates and displays interim results of the Relevance training while monitoring statistical validity of the process.</span></span> 
    
- <span data-ttu-id="30e90-115">**Batch-Berechnung**: Erweiterte eDiscovery übernimmt die kumulierte und gelernten Relevanz Kriterien, betrifft die gesamte Dateisammlung und Relevanz der Ergebnisse für jede Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="30e90-115">**Batch calculation**: Advanced eDiscovery takes the accumulated and learned Relevance criteria, applies it to the entire file collection, and generates Relevance scores for each file.</span></span>
    
- <span data-ttu-id="30e90-116">**Decide**: Erweiterte eDiscovery zeigt die Ergebnisse der Analyse auf die gesamte Groß-/Kleinschreibung nach Batch Berechnung angewendet, und zeigt die Daten für das Dokument überprüfen Entscheidung.</span><span class="sxs-lookup"><span data-stu-id="30e90-116">**Decide**: Advanced eDiscovery displays the results of the analysis applied to the entire case after Batch calculation and displays data for making document review decisions.</span></span>
    
- <span data-ttu-id="30e90-117">**Test**: Erweiterte eDiscovery-Suchergebnissen zum Überprüfen der Gültigkeit und Effektivität der eDiscovery-erweiterte Verarbeitung getestet werden können.</span><span class="sxs-lookup"><span data-stu-id="30e90-117">**Test**: Advanced eDiscovery results can be tested to verify the validity and effectiveness of the Advanced eDiscovery processing.</span></span>
    
## <a name="guidelines-for-relevance-training-and-review"></a><span data-ttu-id="30e90-118">Richtlinien für die Relevanz Schulung und überprüfen</span><span class="sxs-lookup"><span data-stu-id="30e90-118">Guidelines for Relevance training and review</span></span>

<span data-ttu-id="30e90-119">Es folgt eine Übersicht über Richtlinien für die Relevanz Schulung und überprüfen:</span><span class="sxs-lookup"><span data-stu-id="30e90-119">Following is an overview of guidelines for Relevance training and review:</span></span>
  
- <span data-ttu-id="30e90-p103">**Fehler und Inkonsistenzen**: Kategorien Fehler während des Trainings vorgenommen wurde, kehren Sie zur vorherigen Datei herunter, die zu korrigieren. Wenn aufgrund zu vieler Fehler an den richtigen vorhanden sind, oder es eine neue Perspektive der Groß-/Kleinschreibung oder Problem ist, die Relevanz Kriterien sollten vom Administrator neu definiert werden, und die Relevanz Schulung neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="30e90-p103">**Errors and inconsistencies**: If tagging errors are made during training, return to previous file samples to correct them. If there are too many errors to correct or there is a new perspective of the case or issue, the Relevance criteria should be redefined by the Administrator, and the Relevance training restarted.</span></span>
    
- <span data-ttu-id="30e90-122">**Tag und Schulung**:</span><span class="sxs-lookup"><span data-stu-id="30e90-122">**Tagging and training**:</span></span> 
    
  - <span data-ttu-id="30e90-p104">Dateien sollten basierend auf dem Inhalt nur markiert werden. Metadaten wie der Verwaltungsberechtigte, Datum oder Dateipfad nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="30e90-p104">Files should be tagged based on content only. Do not consider metadata, such as custodian, date, or file path.</span></span> 
    
  - <span data-ttu-id="30e90-125">Berücksichtigen Sie den Datum nicht Bereich Angaben im Text beim Markieren von Dateien.</span><span class="sxs-lookup"><span data-stu-id="30e90-125">Do not consider date range indications in the text when tagging files.</span></span>
    
  - <span data-ttu-id="30e90-126">Berücksichtigt beim Markieren von Dateien keine eingebettete Grafiken.</span><span class="sxs-lookup"><span data-stu-id="30e90-126">Do not consider embedded graphical images when tagging files.</span></span>
    
  - <span data-ttu-id="30e90-p105">Wenn eine Datei in das Symbol **formatierten Textansicht** beim tagging anzeigen, die Formatierung von Text nicht berücksichtigt. Beispielsweise wird ein Wort durchgestrichen (eine horizontale Linie durch seine Mitte, der angibt, löschen) nach Relevanz als Teil der analysierten Text weiterhin betrachtet.</span><span class="sxs-lookup"><span data-stu-id="30e90-p105">If viewing a file using the **formatted text view** icon while tagging, do not consider the formatting of text. For example, a word displayed with a strikethrough (a horizontal line through its center indicating deletion) is still considered by Relevance as part of the analyzed text.</span></span> 
    
  - <span data-ttu-id="30e90-p106">Ignorieren angewendetem zur Relevanz (gemäß Festlegung von der Groß-/Kleinschreibung Manager oder Administrator) Text wird in der Relevanz in der angezeigten Datei in der Textansicht entfernt. Wenn die Werte für Text ignorieren nach Relevanz Schulung bereits Schritte definiert wurden, wird der neue Text ignorierte auf Beispieldateien aus den Punkt in dem er definiert wurde erstellt angewendet werden. Das Feature Text ignorieren sollte mit Bedacht, verwendet werden, da die Verwendung die Leistung von Dateianalyse verringern kann</span><span class="sxs-lookup"><span data-stu-id="30e90-p106">Ignore text applied to Relevance (as set by the Case Manager or Administrator) will be removed in the displayed file content in the text view in Relevance. If the values for Ignore text were defined after Relevance training already started, the new ignored text will be applied to sample files created from the point in which it was defined. The Ignore Text feature should be used cautiously, as its use may reduce the performance of file analysis</span></span>
    
  - <span data-ttu-id="30e90-p107">Verwenden Sie die **Überspringen tagging** Option nur bei Bedarf. Erweiterte eDiscovery wird nicht basierend auf Übersprungene Dateien Schulen. Bewertung, wenn es schwierig ist, sagen, ob eine Datei relevant ist ist es besser, Tag als Relevant (R) oder nicht relevant (Nr.) nach Möglichkeit statt **Überspringen**auswählen. Wenn erweiterte eDiscovery Training ausgewertet wird, kann diese klicken Sie dann wie gut diese Dateitypen verarbeitet wurden angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="30e90-p107">Use the **Skip tagging** option only when necessary. Advanced eDiscovery does not train based on skipped files. In assessment, if it's hard to tell whether a file is relevant, it is better to tag as Relevant (R) or Not relevant (NR) whenever possible rather than selecting **Skip**. When Advanced eDiscovery evaluates training, it can then be seen how well these types of files were processed.</span></span>
    
  - <span data-ttu-id="30e90-136">Selbst Dateien, die mit einer sehr geringen extrahierte Text sollte in Schulung nicht als "Überspringen", wenn möglich, sondern als R/Nr. markiert werden.</span><span class="sxs-lookup"><span data-stu-id="30e90-136">Even files with a very small amount of extracted text should be tagged in training as R/NR, rather than as "Skip", when possible.</span></span> 
    
  - <span data-ttu-id="30e90-137">Kategorien, kann die Klassifizierung auswirken, solange die Datei gelesen werden kann und als R/Nr. markiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="30e90-137">Tagging can impact the classifier as long as the file is readable and can be tagged as R/NR.</span></span>
    
  - <span data-ttu-id="30e90-138">Die Datei Sequenznummer in der angezeigten Liste der Beispiel-Dateien auf der Registerkarte **Tag** ermöglicht es dem Benutzer wieder an die ursprüngliche Reihenfolge der Dateien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="30e90-138">The file sequence number on the displayed Sample files list on the **Tag** tab allows the user to return to the original displayed order of the files.</span></span> 
    
  - <span data-ttu-id="30e90-p108">Können Sie zurück zur Beispiele, und ändern Sie die Kennzeichnung der Bewertung und Schulung Dateien festgelegt. Beim Erstellen von im nächsten Beispiels werden die Änderungen angewendet.</span><span class="sxs-lookup"><span data-stu-id="30e90-p108">You can go back to any sample and change the tagging of the assessment and training set files. The changes will be applied when creating the next sample.</span></span>
    
  - <span data-ttu-id="30e90-141">Überprüften Excel, die Dateien im PDF-Format müssen behandelt als systemeigene Excel-Dateien beim Markieren von Dateien.</span><span class="sxs-lookup"><span data-stu-id="30e90-141">Scanned Excel files in PDF format should be treated the same as native Excel files when tagging files.</span></span>
    
  - <span data-ttu-id="30e90-p109">Wenden Sie im unsicheren bezüglich der Relevanz Markieren einer Datei sich an einen Experten. Falsche Kategorien während der Relevanz Schulung kann dazu führen, dass später im Vorgang Verlust von Zeit und möglicherweise auch eine negative Auswirkung auf die Qualität der Gesamtergebnisse.</span><span class="sxs-lookup"><span data-stu-id="30e90-p109">When in doubt regarding the Relevance tagging of a file, consult an expert. Incorrect tagging during the Relevance training can lead to lost time later in the process and may also have a negative impact on the quality of the overall results.</span></span>
    
  - <span data-ttu-id="30e90-144">Schlüsselwörter, die definiert wurden in-Schlüsselwort werden in Farben, um die relevante Dateien während tagging identifizieren Benutzerhilfe Listen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="30e90-144">Keywords that were defined in Keyword lists will be displayed in colors to help the user identify relevant files while tagging.</span></span>
    
- <span data-ttu-id="30e90-p110">**Batch-Berechnung**: Dateien, die markiert wurden, erhalten diese R/Nr. mithilfe der Experte eine integritätsbewertung von 0 und 100. Dies gilt für tagging vor dem Batch Berechnung vorgenommen. Wenn der Experte das Problem im Leerlauf nach Batch Berechnung gewechselt und Fortsetzung dieses Problem markieren, werden die neu markierten Faktoren nicht 100/0, sondern vielmehr die ursprüngliche Bewertung.</span><span class="sxs-lookup"><span data-stu-id="30e90-p110">**Batch calculation**: Files that were tagged as R/NR by the expert will receive a score of either 0 or 100. This applies to tagging made before Batch calculation. If the expert switched the issue to Idle after Batch Calculation and continued tagging this issue, the newly tagged scores will not be 100/0 but rather the original score.</span></span>
    
- <span data-ttu-id="30e90-148">**Probleme und sampling Modus**: Probleme werden in der Regel deaktiviert, wenn Arbeit abgeschlossen ist (Relevanz Schulung ist konstant und Batch Berechnung ausgeführt wurde), wenn die Probleme abgebrochen werden, oder wenn ein anderer Benutzer die Fragen funktionsfähig ist.</span><span class="sxs-lookup"><span data-stu-id="30e90-148">**Issues and sampling mode**: Issues are usually turned Off when work on them is completed (Relevance training is stabilized and Batch calculation was performed), when the issues are canceled, or when another user is working on the issues.</span></span>
    
## <a name="steps-in-relevance-training"></a><span data-ttu-id="30e90-149">Schritte im Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="30e90-149">Steps in Relevance training</span></span>

<span data-ttu-id="30e90-p111">In der **Relevanz \> nachverfolgen** Registerkarte Erweiterte eDiscovery Leitfaden zur Vorgehensweise bei der Verarbeitung, mit den folgenden Schritten weiter. Bei jeder der folgenden Schritte im Prozess Schulung Relevanz empfohlen wird, werden die Auswirkungen nachfolgend beschrieben.</span><span class="sxs-lookup"><span data-stu-id="30e90-p111">In the **Relevance \> Track** tab, Advanced eDiscovery provides recommendations on how to proceed in the processing, with the following next steps. The implications are described below when each of the following steps is recommended in the Relevance training process.</span></span> 
  
- <span data-ttu-id="30e90-152">Markieren / Continue-tagging: Datei überprüfen und die Relevanz tagging durchgeführte Experte für jede Datei und Problem innerhalb einer Stichprobe.</span><span class="sxs-lookup"><span data-stu-id="30e90-152">Tagging / Continue tagging: File review and Relevance tagging performed by an expert for each file and issue within a sample.</span></span>
    
  - <span data-ttu-id="30e90-153">Implikation: Vorhandenen Beispiels markiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="30e90-153">Implication: An existing sample needs to be tagged.</span></span>
    
- <span data-ttu-id="30e90-154">Bewertung / Continue-Bewertung: ermöglicht frühe Validierung von Groß-/Kleinschreibung Problem Relevanz und eine vorläufige Ansicht der Relevanz von der Datei Auffüllung für die aktuelle Groß-/Kleinschreibung importiert.</span><span class="sxs-lookup"><span data-stu-id="30e90-154">Assessment / Continue assessment: Enables early validation of case issue relevance and a preliminary view of the relevance of the file population imported for the current case.</span></span>
    
  - <span data-ttu-id="30e90-155">Implikation: Weitere Bewertung erforderlich oder empfohlen.</span><span class="sxs-lookup"><span data-stu-id="30e90-155">Implication: More assessment is required or recommended.</span></span>
    
- <span data-ttu-id="30e90-156">Schulung / Continue-Training: Prozess während der erweitert eDiscovery vom Experten, die die Datei tagging ist lernen Beispiele und erhält die Möglichkeit zum Identifizieren der Relevanz Kriterien für jedes Problem im Kontext des Einzelfall relevant sind.</span><span class="sxs-lookup"><span data-stu-id="30e90-156">Training / Continue training: Process during which Advanced eDiscovery learns from the expert who is tagging the file samples and acquires the ability to identify Relevance criteria pertinent to each issue within the context of each case.</span></span>
    
  - <span data-ttu-id="30e90-157">Implikation: Das Problem Bedarf weitere Schulungen. Im nächste Beispiel sollte erstellt und markiert werden.</span><span class="sxs-lookup"><span data-stu-id="30e90-157">Implication: The issue needs more training; the next sample should be created and tagged.</span></span> 
    
- <span data-ttu-id="30e90-p112">Batch-Berechnung: Relevanz Prozess in welche erweitert eDiscovery nimmt die während der Phase der Schulung erworbene Kenntnisse und die gesamte Datei Auffüllung betrifft. Alle Dateien in der Dateigruppe relevanten sind für Relevanz bewertet und einen Faktor Relevanz zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="30e90-p112">Batch calculation: Relevance process in which Advanced eDiscovery takes the knowledge acquired during the training stage and applies it to the entire file population. All files in the pertinent file group are assessed for relevance and assigned a Relevance score.</span></span>
    
  - <span data-ttu-id="30e90-160">Implikation: Das Problem hat konstant und Batch Berechnung ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="30e90-160">Implication: The issue has stabilized, and Batch calculation can be performed.</span></span>
    
- <span data-ttu-id="30e90-161">Synchronisieren: Relevanz gibt an, wann ein Experte überprüft und tags eine Stichprobe Dateien aus Laden einer zusätzlichen Datei ausgewählt, während ein Szenario lädt Gang (engl.).</span><span class="sxs-lookup"><span data-stu-id="30e90-161">Catch-up: Relevance indicates when an expert reviews and tags a sample of files selected from an additional file load during a Rolling Loads scenario.</span></span>
    
  - <span data-ttu-id="30e90-162">Implikation: Eine neue Last wurde hinzugefügt, und synchronisieren weiterzuarbeiten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="30e90-162">Implication: A new load has been added, and Catch-up is required to continue working.</span></span>
    
- <span data-ttu-id="30e90-163">Markieren von Inkonsistenzen: Prozess identifiziert, über eine erweiterte eDiscovery-Algorithmus Inkonsistenzen in der Datei tagging-Prozess, die sich negativ auf die Analyse auswirken können.</span><span class="sxs-lookup"><span data-stu-id="30e90-163">Tag inconsistencies: Process identifies, via an Advanced eDiscovery algorithm, inconsistencies in the file tagging process that may negatively impact the analysis.</span></span>
    
  - <span data-ttu-id="30e90-164">Implikation: Im nächste Beispiel enthält Dateien, die markiert wurden in den vorherigen Beispielen und deren tagging muss wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="30e90-164">Implication: The next sample will include files that have been tagged in previous samples, and their tagging must be redone.</span></span>
    
- <span data-ttu-id="30e90-165">Aktualisieren der Klassifizierung: ermöglicht dem Benutzer das tagging oder seeding Änderungen anwenden.</span><span class="sxs-lookup"><span data-stu-id="30e90-165">Update classifier: Allows the user to apply tagging or seeding changes.</span></span>
    
  - <span data-ttu-id="30e90-166">Implikation: Kategorien und seeding Änderungen können angewendet werden ohne ein weiteres Beispiel der Relevanz manuell ausführen.</span><span class="sxs-lookup"><span data-stu-id="30e90-166">Implication: Tagging and seeding changes can be applied without needing to manually run another Relevance sample.</span></span>
    
- <span data-ttu-id="30e90-167">In der Warteschleife: die Relevanz Training abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="30e90-167">On hold: The Relevance training process is completed.</span></span>
    
  - <span data-ttu-id="30e90-168">Implikation: Keine Relevanz Schulung ist erforderlich, zu diesem Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="30e90-168">Implication: No Relevance training is required at this point.</span></span>
    
<span data-ttu-id="30e90-169">Obwohl erweiterte eDiscovery Sie durch den Prozess mit weitere Schritte in verschiedenen Phasen empfohlen führt, außerdem können Sie zwischen den Seiten und Registerkarten navigieren und Auswahlmöglichkeiten für Situationen vornehmen, die für Ihre Einzelfall Problem relevant sind möglicherweise oder Überprüfung des Dokuments.</span><span class="sxs-lookup"><span data-stu-id="30e90-169">Although Advanced eDiscovery guides you through the process, with recommended Next steps at different stages, it also allows you to navigate between tabs and pages, and to make choices to address situations that may be pertinent to your individual case, issue, or document review process.</span></span> 
  
<span data-ttu-id="30e90-p113">Es ist möglich, übernehmen oder erweiterte eDiscovery Nächstes Verarbeitung Auswahlmöglichkeiten überschreiben. Wenn Sie möchten, führen Sie einen Schritt als Nächstes empfohlen, klicken Sie auf der **nächste Schritt** in der erweiterten Problem Anzeige im Dialogfeld aufgeführt, klicken Sie auf die Schaltfläche **Ändern** neben im nächsten Schritt, und wählen Sie eine andere Option für nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="30e90-p113">It is possible to accept or override Advanced eDiscovery Next step processing choices. If you want to perform a step other than the recommended Next step, click the **Next step** listed in the expanded issue display in the dialog, click the **Modify** button next to the Next step, and select another Next step option.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="30e90-172">Einige Optionen bleiben deaktivierte nach entsperren, wie sie für die Verwendung im Prozess zu diesem Zeitpunkt nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="30e90-172">Some options may remain disabled after unlocking as they are not supported for use at that point in the process.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="30e90-173">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30e90-173">See also</span></span>

[<span data-ttu-id="30e90-174">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="30e90-174">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="30e90-175">Grundlegendes zur Bewertung in Relevanz</span><span class="sxs-lookup"><span data-stu-id="30e90-175">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="30e90-176">Kategorien und Bewertung</span><span class="sxs-lookup"><span data-stu-id="30e90-176">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="30e90-177">Kategorien und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="30e90-177">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="30e90-178">Nachverfolgen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="30e90-178">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="30e90-179">Entscheiden je nach den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="30e90-179">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="30e90-180">Testen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="30e90-180">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

