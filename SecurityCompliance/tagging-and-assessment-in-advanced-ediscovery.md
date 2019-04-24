---
title: Tagging und Bewertung in Office 365 Advanced eDiscovery
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
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: 'Überprüfen Sie die Schritte zur Durchführung von Assessment-Schulungen, einschließlich Taggingdateien, und überprüfen Sie die Ergebnisse der Bewertung in Office 365 Advanced eDiscovery. '
ms.openlocfilehash: 02dae23b6489b40243272beea1d79e871ca6a911
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260358"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a><span data-ttu-id="f2ab5-103">Tagging und Bewertung in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f2ab5-103">Tagging and Assessment in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="f2ab5-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="f2ab5-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="f2ab5-106">In diesem Abschnitt wird das Verfahren für das Modul Advanced eDiscovery Relevance Assessment beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-106">This section describes the procedure for the Advanced eDiscovery Relevance Assessment module.</span></span> 
  
## <a name="performing-assessment-training-and-analysis"></a><span data-ttu-id="f2ab5-107">Durchführen von Assessment-Schulungen und-Analysen</span><span class="sxs-lookup"><span data-stu-id="f2ab5-107">Performing Assessment training and analysis</span></span>

1. <span data-ttu-id="f2ab5-108">Klicken Sie auf der Registerkarte \*\* \> Relevanz verfolgen\*\* auf **Bewertung** , um die Fall Bewertung zu starten.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-108">In the **Relevance \> Track** tab, click **Assessment** to start case assessment.</span></span> 
    
    <span data-ttu-id="f2ab5-109">In diesem Verfahren wird beispielsweise ein Beispiel für eine Bewertung von 500-Dateien erstellt, und die Registerkarte **Tag** wird angezeigt, die das Markierungsfeld enthält, die Dateiinhalte und andere Tagging-Optionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-109">For example purposes in this procedure, a sample assessment set of 500 files is created and the **Tag** tab is displayed, which contains the Tagging panel, displayed file content and other tagging options.</span></span> 
    
    ![Registerkarte "Relevanz" für die Bewertung](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. <span data-ttu-id="f2ab5-111">Überprüfen Sie jede Datei im Beispiel, bestimmen Sie die Relevanz der Datei für jeden Fall Problem, und markieren Sie die Datei mithilfe der Tasten Relevanz (R), nicht relevant (NR) und \*\*\*\* überspringen im Bereich des taggingbereichs.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-111">Review each file in the sample, determine the file's relevance for each case issue, and tag the file using the Relevance (R), Not relevant (NR) and Skip buttons in the **Tagging panel** pane.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="f2ab5-112">Die Bewertung erfordert 500 gekennzeichnete Dateien.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-112">Assessment requires 500 tagged files.</span></span> <span data-ttu-id="f2ab5-113">Wenn Dateien übersprungen werden, erhalten Sie weitere zu markierende Dateien.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-113">If files are "skipped", you will receive more files to tag.</span></span> 
  
3. <span data-ttu-id="f2ab5-114">Nachdem Sie alle Dateien im Beispiel gekennzeichnet haben, klicken Sie auf **berechnen**.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-114">After tagging all files in the sample, click **Calculate**.</span></span> 
    
    <span data-ttu-id="f2ab5-115">Die aktuelle Fehlergrenze und der Umfang der Bewertung werden auf der Registerkarte **Relevanz verfolgen** mit erweiterten Details pro Problem berechnet und angezeigt (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="f2ab5-115">The Assessment current error margin and richness are calculated and displayed in the **Relevance Track** tab, with expanded details per issue, as shown below.</span></span> <span data-ttu-id="f2ab5-116">Weitere Informationen zu diesem Dialog werden im späteren Abschnitt "überPrüfen der Ergebnisse der Bewertung" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-116">More details about this dialog are described in the later section "Reviewing Assessments results".</span></span> 
    
    ![Relevanz Track-Bewertung](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > <span data-ttu-id="f2ab5-118">Standardmäßig wird empfohlen, mit dem standardmäßigen nächsten Schritt fortzufahren, wenn die Anzeige des Bewertungs Fortschritts für das Problem abgeschlossen wurde, was darauf hinweist, dass das Bewertungs Beispiel überprüft wurde und ausreichende relevante Dateien markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-118">By default, we recommend that you proceed to the default Next step when the Assessment progress indicator for the issue has completed, indicating that the assessment sample was reviewed and sufficient relevant files were tagged.</span></span> <span data-ttu-id="f2ab5-119">> andernfalls können Sie, wenn Sie die Ergebnisse der Registerkarte " **Spur** " anzeigen und die Fehlergrenze und den nächsten Schritt steuern möchten, auf neben dem **nächsten Schritt** **ändern** klicken, die Option **Bewertung fortsetzen**und dann auf **OK**klicken.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-119">> Otherwise, if you want to view the **Track** tab results and control the margin of error and the next step, click **Modify** adjacent to **Next Step**, select **Continue assessment**, and then click **OK**.</span></span> 
  
1. <span data-ttu-id="f2ab5-120">Klicken Sie rechts neben dem Kontrollkästchen **Bewertung** auf **ändern** , um Bewertungsparameter pro Problem anzuzeigen und anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-120">Click **Modify** to the right of the **Assessment** check box to view and specify assessment parameters per issue.</span></span> <span data-ttu-id="f2ab5-121">Ein Dialogfeld zur **Beurteilungs Stufe** für jedes Problem wird angezeigt, wie im folgenden Beispiel dargestellt:</span><span class="sxs-lookup"><span data-stu-id="f2ab5-121">An **Assessment level** dialog for each issue is displayed, as shown in the following example:</span></span> 
    
    ![Fall Problem bei Beurteilungs Ebene](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    <span data-ttu-id="f2ab5-123">Die folgenden Parameter für das Problem werden im Dialogfeld Beurteilungs **Stufe** berechnet und angezeigt:</span><span class="sxs-lookup"><span data-stu-id="f2ab5-123">The following parameters for the issue are calculated and displayed in the **Assessment level** dialog:</span></span> 
    
    <span data-ttu-id="f2ab5-124">**Ziel Fehlermarge für Rückruf Schätzungen**: basierend auf diesem Wert wird die geschätzte Anzahl der zu überprüfenden zusätzlichen Dateien berechnet.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-124">**Target error margin for recall estimates**: Based on this value, the estimated number of additional files necessary to review is calculated.</span></span> <span data-ttu-id="f2ab5-125">Der für den Rückruf verwendete Margin-Wert ist größer als 75% und mit einem Konfidenzniveau von 95%.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-125">The margin used for recall is greater than 75% and with a 95% confidence level.</span></span> 
    
    <span data-ttu-id="f2ab5-126">**Weitere erforderliche Testdateien**: gibt an, wie viele Dateien erforderlich sind, wenn die Anforderungen des aktuellen Fehler Rands nicht erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-126">**Additional assessment files required**: Indicates how many more files are necessary if the current error margin's requirements have not been met.</span></span> 
    
2. <span data-ttu-id="f2ab5-127">So passen Sie den aktuellen Fehler Rand an und sehen die Auswirkungen unterschiedlicher Fehler Ränder (pro Problem):</span><span class="sxs-lookup"><span data-stu-id="f2ab5-127">To adjust the current error margin and see the effect of different error margins (per issue):</span></span>
    
1. <span data-ttu-id="f2ab5-128">Wählen Sie in der Liste **Problem auswählen** ein Problem aus.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-128">In the **Select issue** list, select an issue.</span></span> 
    
2. <span data-ttu-id="f2ab5-129">Geben Sie unter **Ziel Fehlermarge für Rückruf Schätzungen**einen neuen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-129">In **Target error margin for recall estimates**, enter a new value.</span></span>
    
3. <span data-ttu-id="f2ab5-130">Klicken Sie auf **Werte aktualisieren** , um die Auswirkungen der Anpassungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-130">Click **Update values** to see the impact of the adjustments.</span></span> 
    
3. <span data-ttu-id="f2ab5-131">Klicken Sie im Dialogfeld **Bewertung** auf **erweitert** , um die folgenden zusätzlichen Parameter und Details anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="f2ab5-131">Click **Advanced** in the **Assessment level** dialog to see the following additional parameters and details:</span></span> 
    
    ![Beurteilungs Ebene Case Issue Advanced View](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    <span data-ttu-id="f2ab5-133">**Geschätzte Reichhaltigkeit**: geschätzte Reichhaltigkeit gemäß den aktuellen Bewertungsergebnissen</span><span class="sxs-lookup"><span data-stu-id="f2ab5-133">**Estimated richness**: Estimated richness according to the current assessment results</span></span>
    
    <span data-ttu-id="f2ab5-134">**Für angenommene Rückrufaktion**: Standardmäßig gilt die Ziel Fehlermarge für den rückruf über 75%.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-134">**For assumed recall**: By default, the target error margin applies to recall above 75%.</span></span> <span data-ttu-id="f2ab5-135">Klicken Sie auf **Bearbeiten** , wenn Sie diesen Parameter ändern und die Fehlergrenze für einen anderen Bereich von Rückruf Werten steuern möchten.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-135">Click **Edit** if you want to change this parameter and control the margin of error on a different range of recall values.</span></span> 
    
    <span data-ttu-id="f2ab5-136">**Zuverlässigkeitsstufe**: Standardmäßig ist der empfohlene Fehlerbereich für das Vertrauen 95%.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-136">**Confidence level**: By default, the recommended error margin for confidence is 95%.</span></span> <span data-ttu-id="f2ab5-137">Klicken Sie auf **Bearbeiten** , wenn Sie diesen Parameter ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-137">Click **Edit** if you want to change this parameter.</span></span> 
    
    <span data-ttu-id="f2ab5-138">Erwartete reichhaltige **Fehlermarge**: Angesichts der aktualisierten Werte ist dies der erwartete Fehlerspielraum des Reichtums, nachdem alle zusätzlichen Bewertungsdateien überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-138">**Expected richness error margin**: Given the updated values, this is the expected margin of error of the richness, after all additional assessment files are reviewed.</span></span>
    
    <span data-ttu-id="f2ab5-139">**Erforderliche zusätzliche Analysedateien**: Angesichts der aktualisierten Werte muss die Anzahl zusätzlicher Evaluierungs Dateien, die überprüft werden müssen, um das Ziel zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-139">**Additional assessment files required**: Given the updated values, the number of additional assessment files that need to be reviewed to reach the target.</span></span>
    
    <span data-ttu-id="f2ab5-140">**Erforderliche Gesamt Beurteilungs Dateien**: Angesichts der aktualisierten Werte sind die Gesamtbewertung für die Überprüfung erforderlichen Dateien erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-140">**Total assessment files required**: Given the updated values, total assessment files required for review.</span></span>
    
    <span data-ttu-id="f2ab5-141">**Erwartete Anzahl der relevanten Dateien in der Bewertung**: Angesichts der aktualisierten Werte wird die erwartete Anzahl von relevanten Dateien in der gesamten Bewertung nachgeprüft, nachdem alle zusätzlichen Bewertungsdateien überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-141">**Expected number of relevant files in assessment**: Given the updated values, the expected number of relevant files in the entire assessment after all additional assessment files are reviewed.</span></span>
    
4. <span data-ttu-id="f2ab5-142">Klicken Sie auf **Werte neu berechnen**, wenn Parameter geändert werden.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-142">Click **Recalculate values**, if parameters are changed.</span></span> <span data-ttu-id="f2ab5-143">Wenn Sie fertig sind, klicken Sie bei einem Problem auf **OK** , um die Änderungen zu speichern (oder als **nächstes** , wenn mehrere Probleme zu überprüfende oder \*\*\*\* zu ändern sind, und schließen Sie dann).</span><span class="sxs-lookup"><span data-stu-id="f2ab5-143">When you are done, if there is one issue, click **OK** to save the changes (or **Next** when there are multiple issues to review or modify and then **Finish**).</span></span> 
    
    <span data-ttu-id="f2ab5-144">Wenn es mehrere Probleme gibt, wird, nachdem alle Probleme überprüft oder angepasst wurden, \*\*\*\* ein Zusammenfassungs Dialogfeld angezeigt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-144">When there are multiple issues, after all issues have been reviewed or adjusted, an **Assessment level: summary** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Zusammenfassung der Beurteilungs Ebene](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    <span data-ttu-id="f2ab5-146">Gehen Sie nach erfolgreichem Abschluss der Bewertung zur nächsten Stufe in Relevanz Training.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-146">Upon successful completion of assessment, proceed to the next stage in Relevance training.</span></span>
    
## <a name="reviewing-assessment-results"></a><span data-ttu-id="f2ab5-147">ÜberPrüfen der Bewertungsergebnisse</span><span class="sxs-lookup"><span data-stu-id="f2ab5-147">Reviewing assessment results</span></span>

<span data-ttu-id="f2ab5-148">Nachdem ein Bewertungs Beispiel markiert wurde, werden die Bewertungsergebnisse berechnet und auf der Registerkarte Relevanz verfolgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-148">After an Assessment sample is tagged, the assessment results are calculated and displayed in the Relevance Track tab.</span></span>
  
<span data-ttu-id="f2ab5-149">Die folgenden Ergebnisse werden in der erweiterten Spuranzeige angezeigt:</span><span class="sxs-lookup"><span data-stu-id="f2ab5-149">The following results are displayed in the expanded Track display:</span></span> 
  
- <span data-ttu-id="f2ab5-150">Bewertung aktueller Fehlermarge für Rückruf Schätzungen</span><span class="sxs-lookup"><span data-stu-id="f2ab5-150">Assessment current error margin for recall estimates</span></span>
    
- <span data-ttu-id="f2ab5-151">Geschätzter Umfang</span><span class="sxs-lookup"><span data-stu-id="f2ab5-151">Estimated richness</span></span>
    
- <span data-ttu-id="f2ab5-152">Erforderliche zusätzliche Evaluierungs Dateien (zur Überprüfung)</span><span class="sxs-lookup"><span data-stu-id="f2ab5-152">Additional assessment files required (for review)</span></span>
    
<span data-ttu-id="f2ab5-153">Die Bewertung Current Error Margin ist der von Advanced eDiscovery Empfohlene Fehler Rand.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-153">The Assessment current error margin is the error margin recommended by Advanced eDiscovery.</span></span> <span data-ttu-id="f2ab5-154">Die für die "zusätzlichen Assessment-Dateien erforderlich" angezeigte Nummer entspricht dieser Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-154">The number displayed for the "Additional assessment files required" corresponds to that recommendation.</span></span>
  
<span data-ttu-id="f2ab5-155">Die Anzeige des Bewertungs Fortschritts zeigt den Grad des Abschlusses der Bewertung bei der aktuellen Fehlergrenze an.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-155">The Assessment progress indicator shows the level of completion of the assessment, given the current error margin.</span></span> <span data-ttu-id="f2ab5-156">Wenn die Bewertung durchgeführt wird, wird ein weiteres Bewertungs Beispiel gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-156">When assessment is underway, the user will tag another assessment sample.</span></span>
  
<span data-ttu-id="f2ab5-157">Wenn die Beurteilungs Fortschrittsanzeige die Bewertung als abgeschlossen anzeigt, ist die Bewertung der Test Beispiel Überprüfung abgeschlossen und ausreichende relevante Dateien wurden markiert.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-157">When the assessment progress indicator shows assessment as complete, that means the assessment sample review was completed and sufficient relevant files were tagged.</span></span> 
  
<span data-ttu-id="f2ab5-158">Die erweiterte Spuranzeige zeigt den empfohlenen nächsten Schritt, die Bewertungsstatistiken und den Zugriff auf detaillierte Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-158">The expanded Track display shows the recommended next step, the assessment statistics, and access to detailed results.</span></span>
  
<span data-ttu-id="f2ab5-159">Wenn der Umfang sehr gering ist, ist die Anzahl der zusätzlichen Bewertungsdateien, die erforderlich sind, um eine minimale Anzahl von relevanten Dateien zu erreichen, um nützliche Statistiken zu erstellen, sehr hoch.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-159">When richness is very low, the number of additional assessment files needed to reach a minimal number of relevant files to produce useful statistics is very high.</span></span> <span data-ttu-id="f2ab5-160">Advanced eDiscovery empfiehlt dann die Weiterbildung.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-160">Advanced eDiscovery will then recommend moving on to training.</span></span> <span data-ttu-id="f2ab5-161">Die Anzeige für den Fortschrittsstatus wird schattiert angezeigt, und es sind keine Statistiken verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-161">The assessment progress indicator will be shaded, and no statistics will be available.</span></span> 
  
<span data-ttu-id="f2ab5-162">Fehlt eine statistisch basierte Stabilisierung, gibt es Ergebnisse mit einer niedrigeren Genauigkeitsstufe und Zuverlässigkeitsstufe.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-162">In the absence of statistically based stabilization, there will be results with a lower level of accuracy and confidence level.</span></span> <span data-ttu-id="f2ab5-163">Diese Ergebnisse können jedoch verwendet werden, um relevante Dateien zu finden, wenn Sie den Prozentsatz der gefundenen relevanten Dateien nicht kennen müssen.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-163">However, these results can be used to find relevant files when you do not need to know the percentage of relevant files found.</span></span> <span data-ttu-id="f2ab5-164">Auf ähnliche Weise kann dieser Status verwendet werden, um Probleme mit geringem Umfang zu trainieren, bei denen die Relevanz-Ergebnisse den Zugriff auf Dateien beschleunigen können, die für ein bestimmtes Problem relevant sind.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-164">Similarly, this status can be used to train issues with low richness, where Relevance scores can accelerate access to files relevant to a specific issue.</span></span>
  
> [!TIP]
> <span data-ttu-id="f2ab5-165">Auf der Registerkarte \*\* \> Relevanz verfolgen\*\* , erweiterte Problemanzeige, sind die folgenden Anzeigeoptionen verfügbar: > der Empfohlene nächste Schritt, wie **Nächster Schritt: Tagging** kann umgangen werden (pro Problem), indem Sie auf die Schaltfläche **ändern** , um die , und wählen Sie dann einen anderen Schritt im **nächsten Schritt**aus.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-165">In the **Relevance \> Track** tab, expanded issue display, the following viewing options are available: > The recommended next step, such as **Next step: Tagging** can be bypassed (per issue) by clicking the **Modify** button to its right, and then selecting an different step in the **Next step**.</span></span> <span data-ttu-id="f2ab5-166">Wenn die Anzeige für den Beurteilungs Fortschritt nicht abgeschlossen ist, ist die Bewertung die nächste empfohlene Option, um mehr Bewertungsdateien zu kennzeichnen und die Genauigkeit der Statistiken zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-166">When the assessment progress indicator has not completed, assessment will be the next recommended option, to tag more assessment files and increase statistics accuracy.</span></span> <span data-ttu-id="f2ab5-167">> Sie können den Fehler Rand ändern und seine Auswirkungen bewerten, indem Sie auf **ändern**klicken und im **Dialogfeld Beurteilungs Stufe**den **Ziel Fehlerbereich für Rückruf Schätzungen**ändern und auf **Werte aktualisieren**klicken.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-167">> You can change the error margin and assess its impact, by clicking **Modify**, and in the **Assessment level dialog**, changing the **Target error margin for recall estimates**, and clicking **Update values**.</span></span> <span data-ttu-id="f2ab5-168">Außerdem können Sie in diesem Dialogfeld Erweiterte Optionen anzeigen, indem Sie auf **erweitert**klicken.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-168">Also, in this dialog, you can view advanced options, by clicking **Advanced**.</span></span> <span data-ttu-id="f2ab5-169">> Sie können zusätzliche Statistiken zum Bewertungs Level und deren Auswirkungen anzeigen, indem Sie auf **Ansicht**klicken.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-169">> You can view additional assessment level statistics and their impact by clicking **View**.</span></span> <span data-ttu-id="f2ab5-170">Im Dialogfeld Detail Ergebnisse angezeigt werden Statistiken pro Problem zur Verfügung gestellt, wenn mindestens 500 markierte Bewertungsdateien vorhanden sind und mindestens 18 Dateien für das Problem relevant sind.</span><span class="sxs-lookup"><span data-stu-id="f2ab5-170">In the displayed Detail results dialog, statistics are available per issue, when there are at least 500 tagged assessment files and at least 18 files are tagged as Relevant for the issue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f2ab5-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2ab5-171">See also</span></span>

[<span data-ttu-id="f2ab5-172">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f2ab5-172">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="f2ab5-173">Bedeutung der Bewertung</span><span class="sxs-lookup"><span data-stu-id="f2ab5-173">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f2ab5-174">Tagging-und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="f2ab5-174">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f2ab5-175">Nachverfolgen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="f2ab5-175">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f2ab5-176">Entscheiden basierend auf den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="f2ab5-176">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f2ab5-177">Testen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="f2ab5-177">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

