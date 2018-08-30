---
title: Testen von Relevanz Analyse in Office 365 erweiterte eDiscovery
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Erfahren Sie, wie auf die Registerkarte Test nach Batch Berechnung in Office 365 erweiterte eDiscovery verwenden, um zu testen, vergleichen und überprüfen die allgemeine Qualität der Verarbeitung.  '
ms.openlocfilehash: 782859fe3b6bb3d00945c477928131cd1154446d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529470"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="15c91-103">Testen von Relevanz Analyse in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="15c91-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="15c91-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="15c91-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="15c91-p102">Die Registerkarte Test in erweiterten eDiscovery können Sie testen, vergleichen und überprüfen die allgemeine Qualität der Verarbeitung. Diese Tests werden nach Batch Berechnung ausgeführt. Durch die Kennzeichnung der Dateien in der Auflistung, wird ein Experte für die abschließende Entscheidung darüber, ob jede markierte Datei tatsächlich für die Groß-/Kleinschreibung relevant ist.</span><span class="sxs-lookup"><span data-stu-id="15c91-p102">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing. These tests are performed after Batch calculation. By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="15c91-p103">In einzelnen und mehreren Problem Szenarien sind Tests pro Problem in der Regel ausgeführt. Ergebnisse nach jedem Test angezeigt werden können, und Testergebnisse mit angegebenen Test-Beispieldateien überarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="15c91-p103">In single and multiple-issue scenarios, tests are typically performed per issue. Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="15c91-111">Testen die restlichen</span><span class="sxs-lookup"><span data-stu-id="15c91-111">Testing the rest</span></span>

<span data-ttu-id="15c91-p104">Der Test "Testen von Rest" wird verwendet, beispielsweise Cullingverfahren Entscheidungen zu überprüfen, um nur Dateien über eine bestimmte Relevanz trennwert Score basierend auf die endgültige erweiterte eDiscovery-Ergebnisse zu überprüfen. Der Experte prüft ein Beispiel für Dateien, die einen ausgewählten trennwert Faktor für die Anzahl der relevanten Dateien innerhalb dieser Gruppe ausgewertet werden soll.</span><span class="sxs-lookup"><span data-stu-id="15c91-p104">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results. The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="15c91-p105">Bei diesem Test enthält Statistiken und einen Vergleich zwischen den Satz überprüfen und das Testen die Rest-Auffüllung. Die Ergebnisse der Überprüfung Menge gelten als nach Relevanz während des Trainings berechnet. Die Ergebnisse enthalten Berechnungen, basierend auf Einstellungen und Eingabeparameter, wie beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="15c91-p105">This test provides statistics and a comparison between the Review set and the Test the Rest population. The results of the review set are those calculated by Relevance during Training. The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="15c91-117">Testen Sie Beispiel-Statistik der Anzahl von Dateien in einer Beispielcode und identifizierten relevanten Dateien.</span><span class="sxs-lookup"><span data-stu-id="15c91-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="15c91-p106">Tabellarische Vergleich der Auffüllung Parameter für die Überprüfung und die restlichen, beispielsweise die Anzahl der Dateien, geschätzte Anzahl der relevanten Dateien, geschätzte Umfang und die durchschnittlichen Kosten eine zusätzliche relevante Datei suchen. Einstellungen für die Kosten-Parameter können vom Administrator festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="15c91-p106">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file. Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="15c91-120">Öffnen der **Relevanz \> Test** Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="15c91-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="15c91-p107">Klicken Sie in der Registerkarte **Testen** auf **neu zu testen**. Klicken Sie im Dialogfeld **Erstellen testen** wird angezeigt, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="15c91-p107">In the **Test** tab, click **New test**. The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Relevanztest der REST-Ergebnisse](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="15c91-124">Geben Sie im **Test-Name**und **Beschreibung**den Namen und eine Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="15c91-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="15c91-125">Wählen Sie in der Liste **Testtyp** **Test den Rest**</span><span class="sxs-lookup"><span data-stu-id="15c91-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="15c91-126">In der **Problem / Kategorie** , wählen Sie den Namen des Problems.</span><span class="sxs-lookup"><span data-stu-id="15c91-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="15c91-127">Aktivieren Sie in der Liste **Laden** laden.</span><span class="sxs-lookup"><span data-stu-id="15c91-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="15c91-128">Akzeptieren Sie in **% Lesen**den Standardwert, oder wählen Sie einen Wert für die trennwert Relevanz Bewertung.</span><span class="sxs-lookup"><span data-stu-id="15c91-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="15c91-p108">In der **Größe festgelegt**oder übernehmen Sie den Standardwert. Beachten Sie, dass die Symbole wiederherstellen die Standardwerte wiederhergestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="15c91-p108">In **Set size**, or accept the default value. Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="15c91-p109">Klicken Sie auf **Start, markieren**. Ein Beispiel für Test wird generiert.</span><span class="sxs-lookup"><span data-stu-id="15c91-p109">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="15c91-133">Überprüfen Sie, und markieren Sie die Dateien in die **Relevanz \> Tag** Registerkarte, und klicken Sie dann auf **berechnen**.</span><span class="sxs-lookup"><span data-stu-id="15c91-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="15c91-p110">In der Registerkarte Test können Sie die **Ergebnisse anzeigen** , um die Testergebnisse finden Sie unter klicken. Ein Beispiel ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="15c91-p110">In the Test tab, you can click **View results** to see the test results. An example is shown in the following figure.</span></span> 
    
    ![REST-Ergebnisse testen](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="15c91-137">In der obigen Abbildung enthält im Abschnitt **Beispiel-Parameter** der Tabelle Details über die Anzahl der Dateien in der Stichprobe mithilfe der Experte markiert und die Anzahl der relevanten Dateien in diesem Beispiel gefunden.</span><span class="sxs-lookup"><span data-stu-id="15c91-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="15c91-p111">Im Abschnitt **Parameter Auffüllen** der Tabelle enthält die Testergebnisse, einschließlich der Überprüfung Set Auffüllung mit einem Faktor unterhalb der ausgewählten größere Dateien und Auffüllen von Dateien mit einer Bewertung oberhalb der ausgewählten größere "The Rest". Für jede Auffüllung werden die folgenden Ergebnisse angezeigt:</span><span class="sxs-lookup"><span data-stu-id="15c91-p111">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff. For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="15c91-140">Enthält die Dateien mit Lesen % - erwähnt Grenzwert</span><span class="sxs-lookup"><span data-stu-id="15c91-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="15c91-141">Die Gesamtzahl der Dateien</span><span class="sxs-lookup"><span data-stu-id="15c91-141">The total number of files</span></span> 
    
- <span data-ttu-id="15c91-142">Die geschätzte Anzahl der relevanten Dateien</span><span class="sxs-lookup"><span data-stu-id="15c91-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="15c91-143">Die geschätzte Vielfalt</span><span class="sxs-lookup"><span data-stu-id="15c91-143">The estimated richness</span></span> 
    
- <span data-ttu-id="15c91-144">Die durchschnittliche überprüfen Kosten der Suche nach einem anderen relevanten Datei</span><span class="sxs-lookup"><span data-stu-id="15c91-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="15c91-145">Testen das Segment</span><span class="sxs-lookup"><span data-stu-id="15c91-145">Testing the slice</span></span>

<span data-ttu-id="15c91-146">"Testen des Segments" Test ähnelt dem "Testen der Rest" Testen führt testen, jedoch in der Datei ein Segment festlegen, gemäß Relevanz lesen %.</span><span class="sxs-lookup"><span data-stu-id="15c91-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="15c91-147">Öffnen der **Relevanz \> Test** Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="15c91-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="15c91-p112">Klicken Sie in der Registerkarte **Testen** auf **neu zu testen**. Klicken Sie im Dialogfeld **Erstellen testen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="15c91-p112">In the **Test** tab, click **New test**. The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="15c91-150">Geben Sie im **Test-Name** und **Beschreibung**die Informationen aus.</span><span class="sxs-lookup"><span data-stu-id="15c91-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="15c91-151">Wählen Sie in der Liste **Testtyp** **Test Segments**.</span><span class="sxs-lookup"><span data-stu-id="15c91-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="15c91-152">Wählen Sie in der Liste **Problem** den Problem Namen ein.</span><span class="sxs-lookup"><span data-stu-id="15c91-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="15c91-153">Aktivieren Sie in der Liste **Laden** laden.</span><span class="sxs-lookup"><span data-stu-id="15c91-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="15c91-154">**Zwischen % Lesen**akzeptieren Sie die Standardwerte für die unteren und oberen Bereich oder wählen Sie Werte für den trennwert Relevanz Bewertungen.</span><span class="sxs-lookup"><span data-stu-id="15c91-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="15c91-155">**Festlegen der Größe**wählen Sie einen Wert oder übernehmen Sie den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="15c91-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="15c91-156">Den Standardwert werden die Wiederherstellung Symbole wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="15c91-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="15c91-p113">Klicken Sie auf **Start, markieren**. Ein Beispiel für Test wird generiert.</span><span class="sxs-lookup"><span data-stu-id="15c91-p113">Click **Start tagging**. A test sample is generated.</span></span>
    
10. <span data-ttu-id="15c91-159">Überprüfen Sie, und markieren Sie die Dateien in die **Relevanz \> Tag** Registerkarte, und klicken Sie dann auf **berechnen**.</span><span class="sxs-lookup"><span data-stu-id="15c91-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="15c91-160">In der Registerkarte Test können Sie die **Ergebnisse anzeigen** , um die Testergebnisse finden Sie unter klicken.</span><span class="sxs-lookup"><span data-stu-id="15c91-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="15c91-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15c91-161">See also</span></span>

[<span data-ttu-id="15c91-162">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="15c91-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="15c91-163">Grundlegendes zur Bewertung in Relevanz</span><span class="sxs-lookup"><span data-stu-id="15c91-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="15c91-164">Kategorien und Bewertung</span><span class="sxs-lookup"><span data-stu-id="15c91-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="15c91-165">Kategorien und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="15c91-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="15c91-166">Nachverfolgen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="15c91-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="15c91-167">Entscheiden je nach den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="15c91-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

