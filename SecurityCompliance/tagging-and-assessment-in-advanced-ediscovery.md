---
title: Kategorien und Bewertung in Office 365 erweiterte eDiscovery
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
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: 'Überprüfen Sie die Schritte zum Ausführen der Bewertung Training, einschließlich Markieren von Dateien und zur der Bewertungsergebnisse im Office 365 erweiterte eDiscovery überprüfen. '
ms.openlocfilehash: 0f67dd4780a29536888231f556c18fe887f230ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529320"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a><span data-ttu-id="9c1bb-103">Kategorien und Bewertung in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9c1bb-103">Tagging and Assessment in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="9c1bb-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="9c1bb-106">In diesem Abschnitt wird das Verfahren für die erweiterte eDiscovery Relevanz Assessment Modul.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-106">This section describes the procedure for the Advanced eDiscovery Relevance Assessment module.</span></span> 
  
## <a name="performing-assessment-training-and-analysis"></a><span data-ttu-id="9c1bb-107">Schulung zur Bewertung und Analysen durchführen</span><span class="sxs-lookup"><span data-stu-id="9c1bb-107">Performing Assessment training and analysis</span></span>

1. <span data-ttu-id="9c1bb-108">In der **Relevanz \> nachverfolgen** auf **Assessment** um Groß-/Kleinschreibung Bewertung zu starten.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-108">In the **Relevance \> Track** tab, click **Assessment** to start case assessment.</span></span> 
    
    <span data-ttu-id="9c1bb-109">Beispielsweise Zwecke in diesem Verfahren, eine Reihe von 500 Dateien Beispieldaten-Bewertung wird erstellt, und die Registerkarte **Tag** wird angezeigt, die den Bereich Kategorien, angezeigte Dateiinhalte und andere Kategorien Optionen enthält.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-109">For example purposes in this procedure, a sample assessment set of 500 files is created and the **Tag** tab is displayed, which contains the Tagging panel, displayed file content and other tagging options.</span></span> 
    
    ![Registerkarte „Relevanztag“ für Bewertung](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. <span data-ttu-id="9c1bb-111">Überprüfen Sie jede Datei in der Stichprobe, Bestimmen der Relevanz für jedes Groß-/Kleinschreibung Problem der Datei, und markieren Sie die Datei mithilfe der Relevance (R) nicht relevant (Nr.) und überspringen Schaltflächen im Bereich **Kategorien Systemsteuerung** .</span><span class="sxs-lookup"><span data-stu-id="9c1bb-111">Review each file in the sample, determine the file's relevance for each case issue, and tag the file using the Relevance (R), Not relevant (NR) and Skip buttons in the **Tagging panel** pane.</span></span> 
    
    > [!NOTE]
    >  <span data-ttu-id="9c1bb-p102">Assessment erfordert 500 markierte Dateien. Wenn Dateien "übersprungen" sind, erhalten Sie weitere Dateien zu markieren.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p102">Assessment requires 500 tagged files. If files are "skipped", you will receive more files to tag.</span></span> 
  
3. <span data-ttu-id="9c1bb-114">Klicken Sie nachdem Sie alle Dateien in der Stichprobe tagging auf **berechnen**.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-114">After tagging all files in the sample, click **Calculate**.</span></span> 
    
    <span data-ttu-id="9c1bb-p103">Die Bewertung aktuellen Fehler Rand und wie umfangreich berechnet und in der Registerkarte **Relevanz nachverfolgen** mit erweiterten Details pro Problem, angezeigt wird, wie unten dargestellt. Weitere Informationen zu diesem Dialogfeld werden später im Abschnitt "Überarbeiten Bewertung Ergebnisse" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p103">The Assessment current error margin and richness are calculated and displayed in the **Relevance Track** tab, with expanded details per issue, as shown below. More details about this dialog are described in the later section "Reviewing Assessments results".</span></span> 
    
    ![Relevanznachverfolgung – Bewertung](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > <span data-ttu-id="9c1bb-p104">Standardmäßig wird empfohlen, dass Sie mit dem nächsten Schritt Standard vornehmen, wenn die Statusanzeige zur Bewertung für das Problem abgeschlossen wurde, gibt an, dass das Bewertung Beispiel überprüft wurde und ausreichend relevante Dateien markiert wurden. > Andernfalls, wenn Sie die **Nachverfolgen** Registerkarte Ergebnisse und die Kontrolle der Rand von Fehler- und im nächsten Schritt anzeigen möchten, klicken Sie auf **Ändern** neben der **Nächste Schritt darin**, wählen Sie **Weiter zur Bewertung**und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p104">By default, we recommend that you proceed to the default Next step when the Assessment progress indicator for the issue has completed, indicating that the assessment sample was reviewed and sufficient relevant files were tagged. > Otherwise, if you want to view the **Track** tab results and control the margin of error and the next step, click **Modify** adjacent to **Next Step**, select **Continue assessment**, and then click **OK**.</span></span> 
  
1. <span data-ttu-id="9c1bb-p105">Klicken Sie auf **Ändern** rechts neben das Kontrollkästchen **Assessment** zum Anzeigen und Bewertung Parameter pro Problem angeben. Ein Dialogfeld **Assessment Ebene** für jedes Problem wird angezeigt, wie im folgenden Beispiel dargestellt:</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p105">Click **Modify** to the right of the **Assessment** check box to view and specify assessment parameters per issue. An **Assessment level** dialog for each issue is displayed, as shown in the following example:</span></span> 
    
    ![Fallproblem mit Bewertungsebene](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    <span data-ttu-id="9c1bb-123">Die folgenden Parameter für das Problem werden berechnet und im Dialogfeld **Assessment Ebene** angezeigt:</span><span class="sxs-lookup"><span data-stu-id="9c1bb-123">The following parameters for the issue are calculated and displayed in the **Assessment level** dialog:</span></span> 
    
    <span data-ttu-id="9c1bb-p106">**Ziel Fehler Seitenrand für den Wiederaufruf schätzt**: basierend auf diesen Wert, wird die geschätzte Anzahl der zusätzliche Dateien erforderlich, um zu prüfen berechnet. Der Seitenrand für den Rückruf verwendet ist mehr als 75 % und mit einer 95 % Confidence Level.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p106">**Target error margin for recall estimates**: Based on this value, the estimated number of additional files necessary to review is calculated. The margin used for recall is greater than 75% and with a 95% confidence level.</span></span> 
    
    <span data-ttu-id="9c1bb-126">**Zusätzliche Assessment Dateien erforderlich**: Gibt an, wie viele weitere Dateien sind erforderlich, wenn der aktuelle Fehler Seitenrand Anforderungen nicht erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-126">**Additional assessment files required**: Indicates how many more files are necessary if the current error margin's requirements have not been met.</span></span> 
    
2. <span data-ttu-id="9c1bb-127">So passen Sie den aktuellen Fehler Rand und finden Sie unter den Effekt der anderen Fehler Ränder (pro Problem):</span><span class="sxs-lookup"><span data-stu-id="9c1bb-127">To adjust the current error margin and see the effect of different error margins (per issue):</span></span>
    
1. <span data-ttu-id="9c1bb-128">Wählen Sie in der Liste **Wählen Sie Problem** ein Problem.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-128">In the **Select issue** list, select an issue.</span></span> 
    
2. <span data-ttu-id="9c1bb-129">Geben Sie im **Ziel Fehler Seitenrand für den Wiederaufruf schätzt**einen neuen Wert ein.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-129">In **Target error margin for recall estimates**, enter a new value.</span></span>
    
3. <span data-ttu-id="9c1bb-130">Klicken Sie auf **Werte aktualisieren** , um die Auswirkungen der die Korrekturen finden Sie unter.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-130">Click **Update values** to see the impact of the adjustments.</span></span> 
    
3. <span data-ttu-id="9c1bb-131">Klicken Sie auf **Erweitert** im Dialogfeld **Assessment Ebene** , auf die folgenden zusätzlichen Parameter und ausführliche Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="9c1bb-131">Click **Advanced** in the **Assessment level** dialog to see the following additional parameters and details:</span></span> 
    
    ![Bewertungsebene: erweiterte Ansicht für Fallproblem](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    <span data-ttu-id="9c1bb-133">**Geschätzte Funktionsvielfalt**: geschätzte Funktionsvielfalt gemäß den aktuellen Bewertungsergebnisse zur</span><span class="sxs-lookup"><span data-stu-id="9c1bb-133">**Estimated richness**: Estimated richness according to the current assessment results</span></span>
    
    <span data-ttu-id="9c1bb-p107">**Für den Rückruf angenommenen**: standardmäßig am Rand der Ziel-Fehler angewendet wird, um mehr als 75 % zurückzurufen. Klicken Sie auf **Bearbeiten** , wenn Sie möchten, ändern Sie diesen Parameter und Steuern des Rands von Fehler auf einem anderen Wertebereich Rückruf.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p107">**For assumed recall**: By default, the target error margin applies to recall above 75%. Click **Edit** if you want to change this parameter and control the margin of error on a different range of recall values.</span></span> 
    
    <span data-ttu-id="9c1bb-p108">**Vertrauensebene**: Standardmäßig ist die empfohlene Fehler Seitenrands Confidence 95 %. Wenn Sie diesen Parameter ändern möchten, klicken Sie auf **Bearbeiten** .</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p108">**Confidence level**: By default, the recommended error margin for confidence is 95%. Click **Edit** if you want to change this parameter.</span></span> 
    
    <span data-ttu-id="9c1bb-138">**Erwartete Funktionsvielfalt Fehler Rand**: anhand der aktualisierten Werte, dies ist der erwartete Rand von Fehler wie umfangreich die, nachdem alle zusätzlichen Assessment-Dateien überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-138">**Expected richness error margin**: Given the updated values, this is the expected margin of error of the richness, after all additional assessment files are reviewed.</span></span>
    
    <span data-ttu-id="9c1bb-139">**Zusätzliche Assessment Dateien erforderlich**: anhand der aktualisierten Werte, die Anzahl der zusätzlichen Assessment Dateien, die zum Erreichen der des Ziels des Vorgangs überprüft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-139">**Additional assessment files required**: Given the updated values, the number of additional assessment files that need to be reviewed to reach the target.</span></span>
    
    <span data-ttu-id="9c1bb-140">**Insgesamt Assessment Dateien erforderlich**: anhand der aktualisierten Werte, für die Überprüfung erforderliche Assessment Dateien insgesamt.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-140">**Total assessment files required**: Given the updated values, total assessment files required for review.</span></span>
    
    <span data-ttu-id="9c1bb-141">**Erwartete Anzahl der relevanten Dateien in Assessment**: anhand der aktualisierten Werte, die erwartete Anzahl von relevanten Dateien in der gesamten Bewertung, nachdem alle zusätzlichen Assessment-Dateien überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-141">**Expected number of relevant files in assessment**: Given the updated values, the expected number of relevant files in the entire assessment after all additional assessment files are reviewed.</span></span>
    
4. <span data-ttu-id="9c1bb-p109">Klicken Sie auf die **Werte neu zu berechnen**, wenn Parameter geändert werden. Wenn Sie fertig sind, wenn ein Problem vorliegt, klicken Sie auf **OK** , um die Änderungen (oder **Weiter** , wenn es sind mehrere Probleme überprüfen oder ändern und dann auf **Fertig stellen**) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p109">Click **Recalculate values**, if parameters are changed. When you are done, if there is one issue, click **OK** to save the changes (or **Next** when there are multiple issues to review or modify and then **Finish**).</span></span> 
    
    <span data-ttu-id="9c1bb-144">Wenn mehrere Probleme vorhanden sind, nachdem alle Probleme überprüft oder korrigiert, wurden eine **Assessment Ebene: Zusammenfassung** Dialogfeld wird angezeigt, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-144">When there are multiple issues, after all issues have been reviewed or adjusted, an **Assessment level: summary** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Zusammenfassung der Bewertungsebene](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    <span data-ttu-id="9c1bb-146">Fahren Sie nach dem erfolgreichen Abschluss der Bewertung in die nächste Phase Relevanz Schulung fort.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-146">Upon successful completion of assessment, proceed to the next stage in Relevance training.</span></span>
    
## <a name="reviewing-assessment-results"></a><span data-ttu-id="9c1bb-147">Überprüfen der Bewertungsergebnisse</span><span class="sxs-lookup"><span data-stu-id="9c1bb-147">Reviewing assessment results</span></span>

<span data-ttu-id="9c1bb-148">Nachdem ein Beispiel zur Bewertung markiert ist, werden die Bewertungsergebnisse zur berechnet und auf der Registerkarte Relevanz nachverfolgen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-148">After an Assessment sample is tagged, the assessment results are calculated and displayed in the Relevance Track tab.</span></span>
  
<span data-ttu-id="9c1bb-149">Die folgenden Ergebnisse angezeigt werden im erweiterten Track-Anzeige:</span><span class="sxs-lookup"><span data-stu-id="9c1bb-149">The following results are displayed in the expanded Track display:</span></span> 
  
- <span data-ttu-id="9c1bb-150">Schätzt die aktuellen Fehler Seitenrand für den Wiederaufruf Bewertung</span><span class="sxs-lookup"><span data-stu-id="9c1bb-150">Assessment current error margin for recall estimates</span></span>
    
- <span data-ttu-id="9c1bb-151">Geschätzte Funktionsvielfalt</span><span class="sxs-lookup"><span data-stu-id="9c1bb-151">Estimated richness</span></span>
    
- <span data-ttu-id="9c1bb-152">Zusätzliche Assessment-Dateien (zur Überarbeitung) erforderlich</span><span class="sxs-lookup"><span data-stu-id="9c1bb-152">Additional assessment files required (for review)</span></span>
    
<span data-ttu-id="9c1bb-p110">Assessment aktuelle Fehler Rand wird der Fehler Rand von erweiterten eDiscovery empfohlen. Dieser Empfehlung entspricht die Anzahl für "zusätzliche Assessment erforderlichen Dateien" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p110">The Assessment current error margin is the error margin recommended by Advanced eDiscovery. The number displayed for the "Additional assessment files required" corresponds to that recommendation.</span></span>
  
<span data-ttu-id="9c1bb-p111">Die Bewertung-Statusanzeige wird der Fertigstellung der Bewertung, erhält den aktuellen Fehler Rand. Wenn der Bewertung aktiviert wird, wird der Benutzer ein weiteres Beispiel für Assessment markieren.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p111">The Assessment progress indicator shows the level of completion of the assessment, given the current error margin. When assessment is underway, the user will tag another assessment sample.</span></span>
  
<span data-ttu-id="9c1bb-157">Wenn die Statusanzeige Assessment Assessment als abgeschlossen angezeigt wird, bedeutet, dass die Bewertung Beispiel abgeschlossen wurde und ausreichend relevante Dateien markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-157">When the assessment progress indicator shows assessment as complete, that means the assessment sample review was completed and sufficient relevant files were tagged.</span></span> 
  
<span data-ttu-id="9c1bb-158">Erweiterte Track-Anzeige sind empfohlene Nächstes, die Statistiken zur Bewertung und Zugriff auf ausführliche Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-158">The expanded Track display shows the recommended next step, the assessment statistics, and access to detailed results.</span></span>
  
<span data-ttu-id="9c1bb-p112">Wenn Umfang sehr gering ist, ist die Anzahl der zusätzlichen Assessment Dateien erforderlich, um eine minimale Anzahl von relevanten Dateien nützliche Statistiken zu erreichen sehr hoch. Erweiterte eDiscovery wird dann empfehlen zur Schulung übergeht. Die Statusanzeige Assessment wird grau schattiert dargestellt werden, und keine Statistiken zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p112">When richness is very low, the number of additional assessment files needed to reach a minimal number of relevant files to produce useful statistics is very high. Advanced eDiscovery will then recommend moving on to training. The assessment progress indicator will be shaded, and no statistics will be available.</span></span> 
  
<span data-ttu-id="9c1bb-p113">Keine der Stabilisierung statistisch basiert werden Ergebnisse mit einen geringeren Genauigkeit und Confidence Level. Allerdings können diese Ergebnisse, relevante Dateien zu finden, wenn Sie nicht wissen, den Prozentsatz der relevanten gefundenen Dateitypen müssen verwendet werden. In ähnlicher Weise kann dieser Status verwendet werden zu schulen Probleme mit geringer Funktionsvielfalt, in dem können Relevanz Bewertungen Zugriff auf Dateien an einem bestimmten Problem relevant zu beschleunigen.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p113">In the absence of statistically based stabilization, there will be results with a lower level of accuracy and confidence level. However, these results can be used to find relevant files when you do not need to know the percentage of relevant files found. Similarly, this status can be used to train issues with low richness, where Relevance scores can accelerate access to files relevant to a specific issue.</span></span>
  
> [!TIP]
> <span data-ttu-id="9c1bb-p114">In der **Relevanz \> nachverfolgen** Registerkarte Erweiterte Problem anzeigen, stehen die folgenden Optionen zum Anzeigen: > den empfohlene nächsten Schritt, z. B. **nächsten Schritt: Tagging** können (pro Problem) umgangen werden, indem Sie auf die Schaltfläche **Ändern** , um dessen rechts, und klicken Sie dann im **nächsten Schritt**Auswählen eines anderen Schritts. Wenn Sie die Statusanzeige Assessment nicht abgeschlossen wurde, müssen zur Bewertung die empfohlene Option zum Markieren von weitere Assessment-Dateien und Statistiken Genauigkeit erhöhen. > Sie können den Rand Fehler ändern und seine Auswirkung bewerten, indem Sie auf **Ändern**, und **Bewertung Ebene Dialogfeld**, das **Ziel Fehler Seitenrand für den Wiederaufruf schätzt**, ändern und auf **Update Werte**. In diesem Dialogfeld können Sie darüber hinaus erweiterte Optionen anzeigen, indem Sie auf **Erweitert**. > Sie können zusätzliche Assessment Ebene Verwendungsstatistiken und deren Einfluss anzeigen, indem Sie auf **Ansicht**. Die angezeigten Ergebnisse Dialogfeld mit den Details stehen in Statistiken pro Problem, wenn mindestens 500 markierte Assessment-Dateien vorhanden sind und mindestens 18 Dateien als Relevant für das Problem markiert sind.</span><span class="sxs-lookup"><span data-stu-id="9c1bb-p114">In the **Relevance \> Track** tab, expanded issue display, the following viewing options are available: > The recommended next step, such as **Next step: Tagging** can be bypassed (per issue) by clicking the **Modify** button to its right, and then selecting an different step in the **Next step**. When the assessment progress indicator has not completed, assessment will be the next recommended option, to tag more assessment files and increase statistics accuracy. > You can change the error margin and assess its impact, by clicking **Modify**, and in the **Assessment level dialog**, changing the **Target error margin for recall estimates**, and clicking **Update values**. Also, in this dialog, you can view advanced options, by clicking **Advanced**. > You can view additional assessment level statistics and their impact by clicking **View**. In the displayed Detail results dialog, statistics are available per issue, when there are at least 500 tagged assessment files and at least 18 files are tagged as Relevant for the issue.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9c1bb-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c1bb-171">See also</span></span>

[<span data-ttu-id="9c1bb-172">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9c1bb-172">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="9c1bb-173">Grundlegendes zur Bewertung in Relevanz</span><span class="sxs-lookup"><span data-stu-id="9c1bb-173">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9c1bb-174">Kategorien und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="9c1bb-174">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9c1bb-175">Nachverfolgen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="9c1bb-175">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9c1bb-176">Entscheiden je nach den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="9c1bb-176">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9c1bb-177">Testen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="9c1bb-177">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

