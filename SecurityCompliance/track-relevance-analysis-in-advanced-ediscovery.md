---
title: Nachverfolgen der Relevanz-Analyse in Office 365 Advanced eDiscovery
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
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
description: 'In diesem Artikel erfahren Sie, wie Sie den Status und die Ergebnisse der Relevanz für Anfragen in Office 365 Advanced eDiscovery anzeigen und interpretieren.  '
ms.openlocfilehash: 8bdfd2ddb88215b7217d1cc4cdacf2e775a0d977
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264407"
---
# <a name="track-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="951ff-103">Nachverfolgen der Relevanz-Analyse in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="951ff-103">Track Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="951ff-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="951ff-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="951ff-106">In Advanced eDiscovery wird auf der Registerkarte Relevanz verfolgen die berechnete Gültigkeit der Relevanz-Schulung angezeigt, die auf der Registerkarte Tag ausgeführt wird, und gibt den nächsten Schritt an, der für den iterativen Schulungsprozess relevant ist.</span><span class="sxs-lookup"><span data-stu-id="951ff-106">In Advanced eDiscovery, the Relevance Track tab displays the calculated validity of the Relevance training performed in the Tag tab and indicates the next step to take in the iterative training process in Relevance.</span></span> 
  
## <a name="tracking-relevance-training-status"></a><span data-ttu-id="951ff-107">Status der Tracking Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="951ff-107">Tracking Relevance training status</span></span>

1. <span data-ttu-id="951ff-108">Sehen Sie sich die folgenden Details in Relevanz Track für die Fall Probleme an, wie im folgenden Beispiel des Dialogfelds **Problem Name** unten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="951ff-108">View the following details in Relevance Track for the case issues, as shown in the following example of an **Issue name** dialog below.</span></span> 
    
  - <span data-ttu-id="951ff-109">**Bewertung**: Diese Fortschrittsanzeige zeigt, in welchem Maße die Relevanz-Schulung zu diesem Zeitpunkt das Bewertungs Ziel im Hinblick auf die Fehlertoleranz erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="951ff-109">**Assessment**: This progress indicator shows to what degree the Relevance training performed to this point has achieved the assessment target in terms of margin of error.</span></span> <span data-ttu-id="951ff-110">Die Reichhaltigkeit der Ergebnisse der Relevanz-Schulung wird ebenfalls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="951ff-110">The richness of the Relevance training results is also displayed.</span></span> 
    
  - <span data-ttu-id="951ff-111">**Schulung**: Diese farbcodierte Fortschrittsanzeige und QuickInfo-Anzeige gibt die Stabilität des Trainings Ergebnisses und eine numerische Skala an, in der die Anzahl der Relevanz-Schulungsbeispiele für jedes Problem angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="951ff-111">**Training**: This color-coded progress indicator and tool-tip display indicates the Relevance training results stability and a numeric scale showing the number of Relevance training samples tagged for each issue.</span></span> <span data-ttu-id="951ff-112">Der Experte überwacht den Fortschritt des iterativen Relevanz-Schulungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="951ff-112">The expert monitors the progress of the iterative Relevance training process.</span></span> 
    
  - <span data-ttu-id="951ff-113">**Batch Berechnung**: Diese Fortschrittsanzeige enthält Informationen zum Abschließen der Batch Berechnung.</span><span class="sxs-lookup"><span data-stu-id="951ff-113">**Batch calculation**: This progress indicator provides information about the completion of Batch calculation.</span></span>
    
  - <span data-ttu-id="951ff-114">**Nächster Schritt**: zeigt die Empfehlung für den nächsten Schritt an, der ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="951ff-114">**Next step**: Displays the recommendation for the next step to be performed.</span></span> 
    
    <span data-ttu-id="951ff-115">In dem Beispiel wird eine erfolgreich abgeschlossene Bewertung für ein Problem angezeigt, die durch die Anzeige des abgeschlossenen Farb Fortschritts und des Häkchens angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="951ff-115">In the example, a successfully completed Assessment for an issue is shown, indicated by the completed color progress indicator and the checkmark.</span></span> <span data-ttu-id="951ff-116">Tagging ist im Gange, aber der Fall gilt weiterhin als instabil (Stabilitäts Status wird auch in einem ToolTip angezeigt).</span><span class="sxs-lookup"><span data-stu-id="951ff-116">Tagging is underway, but the case is still considered unstable (stability status also shown in a tool-tip).</span></span> <span data-ttu-id="951ff-117">Die nächste Schritt Empfehlung ist "Training".</span><span class="sxs-lookup"><span data-stu-id="951ff-117">The next step recommendation is "Training".</span></span> 
    
    ![Relevanz Track Training Schritt 1](media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    <span data-ttu-id="951ff-119">In der erweiterten Ansicht werden zusätzliche Informationen und Optionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="951ff-119">The expanded view displays additional information and options.</span></span> <span data-ttu-id="951ff-120">Der angezeigte aktuelle Fehler Rand ist der Fehler Rand des Rückrufs im aktuellen Status der Bewertung, wenn die vorhandenen (bereits gekennzeichneten) Bewertungsdateien vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="951ff-120">The displayed current error margin is the error margin of the recall in the current state of assessment, given the existing (already tagged) assessment files.</span></span>
    
    > [!NOTE]
    >  <span data-ttu-id="951ff-121">Die Bewertungsstufe kann umgangen werden, indem das Kontrollkästchen **Bewertung** pro Problem und dann für "alle Probleme" deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="951ff-121">The Assessment stage can be bypassed by clearing the **Assessment** check box per issue and then for "all issues".</span></span> <span data-ttu-id="951ff-122">Daher gibt es für dieses Problem keine Statistiken.</span><span class="sxs-lookup"><span data-stu-id="951ff-122">However, as a result, there will be no statistics for this issue.</span></span> <span data-ttu-id="951ff-123">> das Kontrollkästchen **Bewertung** kann nur ausgeführt werden, bevor die Bewertung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="951ff-123">> Clearing the **Assessment** check box can only be done before assessment is performed.</span></span> <span data-ttu-id="951ff-124">Wenn in einem Fall mehrere Probleme vorhanden sind, wird die Bewertung nur umgangen, wenn das Kontrollkästchen für jedes Problem deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="951ff-124">Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
    <span data-ttu-id="951ff-125">Wenn die Bewertung mit dem ersten Beispielsatz von Dateien nicht abgeschlossen ist, kann die Bewertung als nächster Schritt zum Taggen weiterer Dateien erfolgen.</span><span class="sxs-lookup"><span data-stu-id="951ff-125">When assessment is not completed with the first sample set of files, assessment might be the next step for tagging more files.</span></span> 
    
    <span data-ttu-id="951ff-126">In **Relevanz** \> **Track**geben die Fortschrittsanzeige und die QuickInfo des Trainings die geschätzte Anzahl zusätzlicher Beispiele an, die zum Erreichen der Stabilität benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="951ff-126">In **Relevance** \> **Track**, the training progress indicator and tool-tip indicate the estimated number of additional samples needed to reach stability.</span></span> <span data-ttu-id="951ff-127">Diese Schätzung stellt eine Richtlinie für die erforderliche zusätzliche Schulung dar.</span><span class="sxs-lookup"><span data-stu-id="951ff-127">This estimate provides a guideline for the additional training needed.</span></span>
    
    ![Relevanz Track-Schulung](media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. <span data-ttu-id="951ff-129">Wenn Sie mit dem Tagging fertig sind und das Training fortsetzen müssen, klicken Sie auf **Training**.</span><span class="sxs-lookup"><span data-stu-id="951ff-129">When you're done tagging and if you need to continue training, click **Training**.</span></span> <span data-ttu-id="951ff-130">Ein weiterer Beispielsatz von Dateien wird aus dem geladenen Datei Satz für zusätzliche Schulungen generiert.</span><span class="sxs-lookup"><span data-stu-id="951ff-130">Another sample set of files is generated from the loaded file set for additional training.</span></span> <span data-ttu-id="951ff-131">Sie kehren dann zur Registerkarte Tag zurück, um weitere Dateien zu markieren und zu trainieren.</span><span class="sxs-lookup"><span data-stu-id="951ff-131">You are then returned to the Tag tab to tag and train more files.</span></span>
    
### <a name="reaching-stable-training-levels"></a><span data-ttu-id="951ff-132">Erreichen stabiler Schulungsstufen</span><span class="sxs-lookup"><span data-stu-id="951ff-132">Reaching stable training levels</span></span>

<span data-ttu-id="951ff-133">Nachdem die Bewertungsdateien ein stabiles Ausbildungsniveau erreicht haben, ist Advanced eDiscovery für die Batch Berechnung bereit.</span><span class="sxs-lookup"><span data-stu-id="951ff-133">After the assessment files have attained a stable level of training, Advanced eDiscovery is ready for Batch calculation.</span></span>
  
> [!NOTE]
> <span data-ttu-id="951ff-134">Der nächste Schritt ist NormalerWeise nach drei stabilen Übungsbeispielen "Batch Berechnung".</span><span class="sxs-lookup"><span data-stu-id="951ff-134">Usually, after three stable training samples, the next step is "Batch calculation".</span></span> <span data-ttu-id="951ff-135">Es kann beispielsweise Ausnahmen geben, wenn Änderungen am Tagging von Dateien aus früheren Beispielen oder beim Hinzufügen von Seed-Dateien vorgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="951ff-135">There may be exceptions, for example, when there were changes to the tagging of files from earlier samples or when seed files were added.</span></span> 
  
### <a name="performing-batch-calculation"></a><span data-ttu-id="951ff-136">Ausführen der Batch Berechnung</span><span class="sxs-lookup"><span data-stu-id="951ff-136">Performing Batch calculation</span></span>

<span data-ttu-id="951ff-137">Die Batch Berechnung wird als nächster Schritt ausgeführt, nachdem das Training erfolgreich abgeschlossen wurde (wenn ein stabiler Trainingsstatus durch die Fortschrittsanzeige angezeigt wird, ein Häkchen und ein stabiler Status in der QuickInfo.) Die Batch Berechnung wendet das während der Relevanz-Schulung erworbene Wissen auf die gesamte Datei Auffüllung an, um die Relevanz der Dateien zu bewerten und Relevanzwerte zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="951ff-137">Batch calculation is executed as the next step after training is successfully completed (when a stable training status is shown by the progress bar, a checkmark and stable status in the tool-tip.) Batch calculation applies the knowledge acquired during the Relevance training to the entire file population, to assess the files' relevance and to assign Relevance scores.</span></span>
  
<span data-ttu-id="951ff-138">Wenn es mehr als ein Problem gibt, erfolgt die Batch Berechnung pro Problem.</span><span class="sxs-lookup"><span data-stu-id="951ff-138">When there is more than one issue, Batch calculation is done per issue.</span></span> <span data-ttu-id="951ff-139">Während der Batch Berechnung wird der Fortschritt während der Verarbeitung aller Dateien überwacht.</span><span class="sxs-lookup"><span data-stu-id="951ff-139">During Batch calculation, progress is monitored while processing all of the files.</span></span> 
  
<span data-ttu-id="951ff-140">Hier ist der Empfohlene nächste Schritt "None", was bedeutet, dass an dieser Stelle keine zusätzliche iterative Relevanz-Schulung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="951ff-140">Here, the recommended next step is "None", which indicates that no additional iterative Relevance training is required at this point.</span></span> <span data-ttu-id="951ff-141">Die nächste Phase ist die Registerkarte **Relevanz \> entscheiden** .</span><span class="sxs-lookup"><span data-stu-id="951ff-141">The next phase is the **Relevance \> Decide** tab.</span></span> 
  
<span data-ttu-id="951ff-142">Wenn Sie nach der Batch Berechnung neue Dateien importieren möchten, kann der Administrator die importierten Dateien einer neuen Belastung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="951ff-142">If you want to import new files after Batch calculation, the administrator can add the imported files to a new load.</span></span>
  
> [!NOTE]
> <span data-ttu-id="951ff-143">Wenn Sie während der Batch Berechnung auf **Abbrechen** klicken, speichert der Prozess, was bereits ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="951ff-143">If you click **Cancel** during Batch calculation, the process saves what was already executed.</span></span> <span data-ttu-id="951ff-144">Wenn Sie die Batch Berechnung erneut ausführen, wird der Prozess vom zuletzt ausgeführten Punkt fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="951ff-144">If you run Batch calculation again, the process will continue from the last executed point.</span></span> 
  
### <a name="assessing-tagging-consistency"></a><span data-ttu-id="951ff-145">Bewerten der Tagging-Konsistenz</span><span class="sxs-lookup"><span data-stu-id="951ff-145">Assessing tagging consistency</span></span>

<span data-ttu-id="951ff-146">Wenn es Inkonsistenzen bei der Dateikennzeichnung gibt, kann dies Auswirkungen auf die Analyse haben.</span><span class="sxs-lookup"><span data-stu-id="951ff-146">If there are inconsistencies in file tagging, it can affect the analysis.</span></span> <span data-ttu-id="951ff-147">Der erweiterte eDiscovery-Tagging-Konsistenz Prozess kann verwendet werden, wenn die Ergebnisse nicht optimal sind oder Konsistenz zweifelhaft ist.</span><span class="sxs-lookup"><span data-stu-id="951ff-147">The Advanced eDiscovery tagging consistency process can be used when results are not optimal or consistency is in doubt.</span></span> <span data-ttu-id="951ff-148">Eine Liste der möglichen inkonsistenten getaggten Dateien wird zurückgegeben, und Sie können bei Bedarf überprüft und neu markiert werden.</span><span class="sxs-lookup"><span data-stu-id="951ff-148">A list of possible inconsistently tagged files is returned, and they can be reviewed and re-tagged, as necessary.</span></span>
  
> [!NOTE]
> <span data-ttu-id="951ff-149">Nach sieben oder mehr Trainingsrunden nach der Bewertung kann die Tagging-Konsistenz in **Relevanz** \> **Track** \> **Issue** \> **detailed results** \> **Training Progress**angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="951ff-149">After seven or more training rounds following assessment, tagging consistency can be viewed in **Relevance** \> **Track** \> **Issue** \> **Detailed results** \> **Training progress**.</span></span> <span data-ttu-id="951ff-150">Diese Überprüfungen werden jeweils einzeln durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="951ff-150">This review is done for one issue at a time.</span></span> 
  
1. <span data-ttu-id="951ff-151">Erweitern Sie in **Relevanz \> Track**die Zeile eines Problems.</span><span class="sxs-lookup"><span data-stu-id="951ff-151">In **Relevance \> Track**, expand an issue's row.</span></span>
    
2. <span data-ttu-id="951ff-152">Klicken Sie rechts **neben nächster Schritt**auf **ändern**.</span><span class="sxs-lookup"><span data-stu-id="951ff-152">To the right of **Next step**, click **Modify**.</span></span>
    
3. <span data-ttu-id="951ff-153">Wählen \*\*\*\* Sie Inkonsistenzen als **Nächster Schritt** aus, nachdem Sie sieben Übungsbeispiele ausgewählt haben, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="951ff-153">Select **Tag inconsistencies** as the **Next step** option, after seven training samples and click **OK**.</span></span>
    
4. <span data-ttu-id="951ff-154">Wählen \*\*\*\* Sie Inkonsistenzen aus.</span><span class="sxs-lookup"><span data-stu-id="951ff-154">Select **Tag inconsistencies**.</span></span> <span data-ttu-id="951ff-155">Die Registerkarte **Tag** wird geöffnet, und es wird eine Liste der Inkonsistenzen angezeigt, die bei Bedarf neu gekennzeichnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="951ff-155">The **Tag** tab opens displaying a list of the inconsistencies to re-tag as necessary.</span></span> 
    
5. <span data-ttu-id="951ff-156">Klicken Sie auf **berechnen** , um die Änderungen zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="951ff-156">Click **Calculate** to submit the changes.</span></span> <span data-ttu-id="951ff-157">Der nächste Schritt nach dem Tagging von Inkonsistenzen ist "Training".</span><span class="sxs-lookup"><span data-stu-id="951ff-157">The next step after tagging inconsistencies is "Training".</span></span> 
    
## <a name="viewing-and-using-relevance-results"></a><span data-ttu-id="951ff-158">Anzeigen und Verwenden von Relevanz-Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="951ff-158">Viewing and using Relevance results</span></span>

<span data-ttu-id="951ff-159">Erweitern Sie auf der Registerkarte **Relevanz \> verfolgen** die Zeile eines Problems, und klicken Sie neben **detaillierte Ergebnisse**auf **Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="951ff-159">In the **Relevance \> Track** tab, expand an issue's row, and next to **Detailed results**, click **View**.</span></span> <span data-ttu-id="951ff-160">Die detaillierten Ergebnisbereiche werden angezeigt (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="951ff-160">The Detailed results panes are displayed, as shown and described below.</span></span>
  
![Relevanz-Schulung detaillierte Ergebnisse](media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a><span data-ttu-id="951ff-162">Tagging-Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="951ff-162">Tagging summary</span></span>

 <span data-ttu-id="951ff-163">In dem unten gezeigten Beispiel \*\*\*\* werden die Gesamtwerte für alle Bewertungs-, Schulungs-und Catch-up-Datei Kennzeichnungs Prozesse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="951ff-163">In the example shown below, the **Tagging summary** displays totals for each of Assessment, Training, and Catch-up file tagging processes.</span></span> 
  
![Übersicht über Relevanz-Titel-Tagging](media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a><span data-ttu-id="951ff-165">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="951ff-165">Keywords</span></span>

<span data-ttu-id="951ff-166">Bei einem Schlüsselwort handelt es sich um eine eindeutige Zeichenfolge, ein Wort, einen Ausdruck oder eine Folge von Wörtern in einer Datei, die von Advanced eDiscovery identifiziert wurde, als einen wichtigen Indikator dafür, ob eine Datei relevant ist.</span><span class="sxs-lookup"><span data-stu-id="951ff-166">A keyword is a unique string, word, phrase, or sequence of words in a file identified by Advanced eDiscovery as a significant indicator of whether a file is relevant.</span></span> <span data-ttu-id="951ff-167">Das Schlüsselwort und die Gewichtung der Spalten "include" in Dateien, die als relevant markiert sind, und die Spalten "Exclude" listet Schlüsselwörter und Gewichte in Dateien auf, die als nicht relevant markiert sind.</span><span class="sxs-lookup"><span data-stu-id="951ff-167">The "Include" columns list keyword and weights in files tagged as Relevant, and the "Exclude" columns lists keywords and weights in files tagged as Not relevant.</span></span>
  
<span data-ttu-id="951ff-168">Erweiterte eDiscovery weist negative oder positive Schlüsselwort Gewichtungswerte zu.</span><span class="sxs-lookup"><span data-stu-id="951ff-168">Advanced eDiscovery assigns negative or positive keyword weight values.</span></span> <span data-ttu-id="951ff-169">Je höher die Gewichtung ist, desto höher ist die Wahrscheinlichkeit, dass eine Datei, in der das Stichwort angezeigt wird, bei der Batch Berechnung eine höhere Relevanz erzielt.</span><span class="sxs-lookup"><span data-stu-id="951ff-169">The higher the weight, the higher the likelihood that a file in which the keyword appears is assigned a higher Relevance score during Batch calculation.</span></span> 
  
<span data-ttu-id="951ff-170">Die erweiterte eDiscovery-Liste mit Schlüsselwörtern kann verwendet werden, um eine von einem Experten erstellte Liste oder eine indirekte Plausibilitätsprüfung zu einem beliebigen Zeitpunkt im Datei Prüfungsprozess zu ergänzen.</span><span class="sxs-lookup"><span data-stu-id="951ff-170">The Advanced eDiscovery list of keywords can be used to supplement a list built by an expert or as an indirect sanity check at any point in the file review process.</span></span>
  
### <a name="training-progress"></a><span data-ttu-id="951ff-171">Schulungs Fortschritt</span><span class="sxs-lookup"><span data-stu-id="951ff-171">Training progress</span></span>

<span data-ttu-id="951ff-172">Der **Fortschritts Fortschritt** -Bereich enthält eine Trainingsfortschritts Grafik und eine Anzeige des Qualitäts Indikators, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="951ff-172">The **Training Progress** pane includes a training progress graph and quality indicator display, as shown in the example below.</span></span> 
  
![Relevanz nachVerfolgen des Schulungs Fortschritts](media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
 <span data-ttu-id="951ff-174">**Ausbildungs Qualitätsindikator**: zeigt die Bewertung der Tagging-Konsistenz wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="951ff-174">**Training quality indicator**: Displays the rating of the tagging consistency as follows:</span></span>
  
- <span data-ttu-id="951ff-175">**Gut**: Dateien werden konsistent gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="951ff-175">**Good**: Files are tagged consistently.</span></span> <span data-ttu-id="951ff-176">(Grünes Licht wird angezeigt)</span><span class="sxs-lookup"><span data-stu-id="951ff-176">(Green light displayed)</span></span>
    
- <span data-ttu-id="951ff-177">**Mittel**: einige Dateien werden möglicherweise inkonsistent gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="951ff-177">**Medium**: Some files may be tagged inconsistently.</span></span> <span data-ttu-id="951ff-178">(Gelbes Licht wird angezeigt)</span><span class="sxs-lookup"><span data-stu-id="951ff-178">(Yellow light displayed)</span></span>
    
- <span data-ttu-id="951ff-179">**Warnung**: viele Dateien werden möglicherweise inkonsistent gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="951ff-179">**Warning**: Many files may be tagged inconsistently.</span></span> <span data-ttu-id="951ff-180">(Rotes Licht wird angezeigt)</span><span class="sxs-lookup"><span data-stu-id="951ff-180">(Red light displayed)</span></span>
    
 <span data-ttu-id="951ff-181">**Trainingsfortschritts Diagramm**: zeigt den Grad der Relevanz Training Stabilität nach einer Reihe von Relevanz trainingszyklen im Vergleich zu den F-Measure-Wert.</span><span class="sxs-lookup"><span data-stu-id="951ff-181">**Training progress graph**: Shows the degree of Relevance training stability after a number of Relevance training cycles in comparison to the F-measure value.</span></span> <span data-ttu-id="951ff-182">Bei der Verschiebung von links nach rechts über den Graphen verengt sich das Konfidenzintervall und wird zusammen mit dem F-Measure durch erweiterte eDiscovery-Relevanz verwendet, um die Stabilität zu bestimmen, wenn die Relevanz-Schulungsergebnisse optimiert werden.</span><span class="sxs-lookup"><span data-stu-id="951ff-182">As we move from the left to the right across the graph, the confidence interval narrows and is used, along with the F-measure, by Advanced eDiscovery Relevance to determine stability when the Relevance training results are optimized.</span></span>
  
> [!NOTE]
> <span data-ttu-id="951ff-183">Relevanz verwendet F2, eine F-Measure-Metrik, bei der Rückruf doppelt so viel Gewicht erhält wie Precision.</span><span class="sxs-lookup"><span data-stu-id="951ff-183">Relevance uses F2, an F-measure metric where Recall receives twice as much weight as Precision.</span></span> <span data-ttu-id="951ff-184">Für Fälle mit hoher reichgröße (mehr als 25%) verwendet Relevanz F1 (1:1-Verhältnis).</span><span class="sxs-lookup"><span data-stu-id="951ff-184">For cases with high richness (over 25%), Relevance uses F1 (1:1 ratio).</span></span> <span data-ttu-id="951ff-185">Das F-Measure-Verhältnis kann in den **erweiterten Einstellungen**für **Relevanz Setup** \> konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="951ff-185">The F-measure ratio can be configured in **Relevance setup** \> **Advanced settings**.</span></span> 
  
### <a name="batch-calculation-results"></a><span data-ttu-id="951ff-186">Ergebnisse der Batch Berechnung</span><span class="sxs-lookup"><span data-stu-id="951ff-186">Batch calculation results</span></span>

<span data-ttu-id="951ff-187">Der Bereich **Batch Berechnungsergebnisse** enthält die Anzahl der Dateien, die für Relevanz bewertet wurden, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="951ff-187">The **Batch calculation results** pane includes the number of files that were scored for Relevance, as follows:</span></span> 
  
- <span data-ttu-id="951ff-188">**Success**</span><span class="sxs-lookup"><span data-stu-id="951ff-188">**Success**</span></span>
    
- <span data-ttu-id="951ff-189">**Empty**: enthält keinen Text, beispielsweise nur Leerzeichen/Tabstopps</span><span class="sxs-lookup"><span data-stu-id="951ff-189">**Empty**: Contains no text, for example, only spaces/tabs</span></span>
    
- <span data-ttu-id="951ff-190">**Fehler**: aufgrund einer übermäßigen Größe oder nicht lesbar</span><span class="sxs-lookup"><span data-stu-id="951ff-190">**Failed**: Due to excessive size or could not be read</span></span>
    
- <span data-ttu-id="951ff-191">**Ignoriert**: aufgrund von übermäßiger Größe</span><span class="sxs-lookup"><span data-stu-id="951ff-191">**Ignored**: Due to excessive size</span></span>
    
- <span data-ttu-id="951ff-192">**Nebel**: enthält keinen bedeutungslosen Text oder keine für das Problem relevanten Features</span><span class="sxs-lookup"><span data-stu-id="951ff-192">**Nebulous**: Contains meaningless text or no features relevant to the issue</span></span>
    
> [!NOTE]
> <span data-ttu-id="951ff-193">Leer, failed, ignored oder neblig erhalten eine Relevanz-Bewertung von-1.</span><span class="sxs-lookup"><span data-stu-id="951ff-193">Empty, Failed, Ignored, or Nebulous will receive a Relevance score of -1.</span></span> 
  
### <a name="training-statistics"></a><span data-ttu-id="951ff-194">Schulungs Statistiken</span><span class="sxs-lookup"><span data-stu-id="951ff-194">Training statistics</span></span>

<span data-ttu-id="951ff-195">Im Bereich **Trainingsstatistik** werden Statistiken und Diagramme basierend auf Ergebnissen aus Advanced eDiscovery Relevance Training angezeigt.</span><span class="sxs-lookup"><span data-stu-id="951ff-195">The **Training statistics** pane displays statistics and graphs based on results from Advanced eDiscovery Relevance training.</span></span> 
  
![Relevanz Track Training Statistics](media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
<span data-ttu-id="951ff-197">Diese Ansicht zeigt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="951ff-197">This view shows the following:</span></span>
  
- <span data-ttu-id="951ff-198">**Review-Recall Ratio**: Vergleich der Ergebnisse nach Relevanz-Bewertungen in einer hypothetisch linearen Übersetzung.</span><span class="sxs-lookup"><span data-stu-id="951ff-198">**Review-recall ratio**: Comparison of results according to Relevance scores in a hypothetically linear review.</span></span> <span data-ttu-id="951ff-199">ReCall wird aufgrund des Übersichts Satzes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="951ff-199">Recall is estimated given the review set size set.</span></span>
    
- <span data-ttu-id="951ff-200">**Parameter**: kumulative berechnete Statistiken im Zusammenhang mit dem Übersichts Satz im Verhältnis zur Datei Auffüllung für den gesamten Fall.</span><span class="sxs-lookup"><span data-stu-id="951ff-200">**Parameters**: Cumulative calculated statistics pertaining to the review set in relation to the file population for the entire case.</span></span>
    
- <span data-ttu-id="951ff-201">**Review**: Prozentsatz der zu überprüfenden Dateien basierend auf diesem Cutoff.</span><span class="sxs-lookup"><span data-stu-id="951ff-201">**Review**: Percentage of files to review based on this cutoff.</span></span>
    
- <span data-ttu-id="951ff-202">**Recall**: Prozentsatz der relevanten Dateien im Übersichts Satz.</span><span class="sxs-lookup"><span data-stu-id="951ff-202">**Recall**: Percentage of Relevant files in the review set.</span></span> 
    
- <span data-ttu-id="951ff-203">**Verteilung nach Relevanz Bewertung**: Dateien in der dunkelgrauen Anzeige Links befinden sich unterhalb der Cutoff-Bewertung.</span><span class="sxs-lookup"><span data-stu-id="951ff-203">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score.</span></span> <span data-ttu-id="951ff-204">Ein QuickInfo zeigt den Relevanzwert und den zugehörigen Prozentsatz der Dateien in der Übersichtsdatei im Verhältnis zu den Gesamtdateien an.</span><span class="sxs-lookup"><span data-stu-id="951ff-204">A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="951ff-205">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="951ff-205">See also</span></span>

[<span data-ttu-id="951ff-206">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="951ff-206">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="951ff-207">Bedeutung der Bewertung</span><span class="sxs-lookup"><span data-stu-id="951ff-207">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="951ff-208">Durchführen und Überprüfen der Bewertung</span><span class="sxs-lookup"><span data-stu-id="951ff-208">Performing and reviewing Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="951ff-209">Durchführen von Relevanz-Schulungen</span><span class="sxs-lookup"><span data-stu-id="951ff-209">Performing Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="951ff-210">EntscheidungsFindung anhand der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="951ff-210">Making decisions based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="951ff-211">Testen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="951ff-211">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

