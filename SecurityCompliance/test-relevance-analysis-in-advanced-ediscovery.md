---
title: Test Relevanz-Analyse in Office 365 Advanced eDiscovery
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Erfahren Sie, wie Sie die Registerkarte Test nach der Batch Berechnung in Office 365 Advanced eDiscovery verwenden, um die allgemeine Verarbeitungsqualität zu testen, zu vergleichen und zu validieren.  '
ms.openlocfilehash: 735a6d8088b4696e2ebc348db435a11914bd0b10
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259973"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="9ae2a-103">Test Relevanz-Analyse in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9ae2a-103">Test Relevance analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="9ae2a-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="9ae2a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="9ae2a-106">Auf der Registerkarte Test in Advanced eDiscovery können Sie die allgemeine Verarbeitungsqualität testen, vergleichen und überprüfen.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-106">The Test tab in Advanced eDiscovery enables you to test, compare, and validate the overall quality of processing.</span></span> <span data-ttu-id="9ae2a-107">Diese Tests werden nach der Batch Berechnung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-107">These tests are performed after Batch calculation.</span></span> <span data-ttu-id="9ae2a-108">Durch das Taggen der Dateien in der Auflistung trifft ein Experte das abschließende Urteil darüber, ob jede markierte Datei tatsächlich für den Fall relevant ist.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-108">By tagging the files in the collection, an expert makes the final judgment about whether each tagged file is actually relevant to the case.</span></span> 
  
<span data-ttu-id="9ae2a-109">In Szenarios mit mehreren Problemen werden in der Regel Tests pro Problem durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-109">In single and multiple-issue scenarios, tests are typically performed per issue.</span></span> <span data-ttu-id="9ae2a-110">Ergebnisse können nach jedem Test angezeigt werden, und Testergebnisse können mit angegebenen Beispiel Testdateien überarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-110">Results can be viewed after each test, and test results can be reworked with specified sample test files.</span></span>
  
## <a name="testing-the-rest"></a><span data-ttu-id="9ae2a-111">Testen des Rests</span><span class="sxs-lookup"><span data-stu-id="9ae2a-111">Testing the rest</span></span>

<span data-ttu-id="9ae2a-112">Der Test "Test the Rest" dient zum Überprüfen von Entscheidungen zum Abschneiden, beispielsweise zur Überprüfung von Dateien, die auf den letzten erweiterten eDiscovery-Ergebnissen basieren.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-112">The "Test the Rest" test is used to validate culling decisions, for example, to review only files above a specific Relevance cutoff score based on the final Advanced eDiscovery results.</span></span> <span data-ttu-id="9ae2a-113">Der Experte prüft ein Beispiel von Dateien unter einer ausgewählten Cutoff-Bewertung, um die Anzahl der relevanten Dateien innerhalb dieser Gruppe zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-113">The expert reviews a sample of files under a selected cutoff score to evaluate the number of relevant files within that set.</span></span>
  
<span data-ttu-id="9ae2a-114">Dieser Test bietet Statistiken und einen Vergleich zwischen dem überPrüfungs Satz und dem Test der Rest-Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-114">This test provides statistics and a comparison between the Review set and the Test the Rest population.</span></span> <span data-ttu-id="9ae2a-115">Die Ergebnisse des Übersichts Satzes werden anhand der Relevanz während des Trainings berechnet.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-115">The results of the review set are those calculated by Relevance during Training.</span></span> <span data-ttu-id="9ae2a-116">Die Ergebnisse sind Berechnungen, basierend auf Einstellungen und Eingabeparametern, wie zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9ae2a-116">The results include calculations , based on settings and input parameters, such as:</span></span>
  
- <span data-ttu-id="9ae2a-117">Testen Sie die Beispiel Statistiken zur Anzahl der Dateien in einem Beispiel, und ermitteln Sie die relevanten Dateien.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-117">Test sample statistics of the number of files in a sample and identified relevant files.</span></span> 
    
- <span data-ttu-id="9ae2a-118">Tabellarischer Vergleich der Populations Parameter des Übersichts Satzes und des Rests, beispielsweise der Anzahl von Dateien, der geschätzten Anzahl der relevanten Dateien, des geschätzten Umfangs und der durchschnittlichen Kosten für die Suche nach einer zusätzlichen relevanten Datei.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-118">Tabular comparison of the Population parameters of the Review set and the Rest, for example, the number of files, estimated number of relevant files, estimated richness, and the average cost of finding an additional relevant file.</span></span> <span data-ttu-id="9ae2a-119">Einstellungen für Kosten Parameter können vom Administrator festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-119">Cost parameter settings can be set by the administrator.</span></span>
    
1. <span data-ttu-id="9ae2a-120">Öffnen Sie die Registerkarte **Relevanz \> testen** .</span><span class="sxs-lookup"><span data-stu-id="9ae2a-120">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="9ae2a-121">Klicken Sie auf der Registerkarte **Test** auf **neuer Test**.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-121">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="9ae2a-122">Das Dialogfeld **Test erstellen** wird angezeigt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-122">The **Create test** dialog is displayed, as shown in the following example.</span></span> 
    
    ![Relevanz Testen der Rest-Ergebnisse](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. <span data-ttu-id="9ae2a-124">Geben \*\*\*\* Sie unter Testname und **Beschreibung**den Namen und die Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-124">In **Test name**, and **Description**, type the name and description.</span></span>
    
4. <span data-ttu-id="9ae2a-125">Wählen Sie \*\*\*\* in der Liste Testtyp **die Option Rest testen** aus.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-125">In the **Test type** list, select **Test the Rest**</span></span>
    
5. <span data-ttu-id="9ae2a-126">Wählen Sie in der Liste **Problem/Kategorie** den Problem Namen aus.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-126">In the **Issue / Category** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="9ae2a-127">Wählen Sie in der Liste **Laden** die Option Laden aus.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-127">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="9ae2a-128">Übernehmen Sie in **% Lesen**den Standardwert, oder wählen Sie einen Wert für das Cutoff-Relevanz-Ergebnis aus.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-128">In **Read %**, accept the default value or select a value for the cutoff Relevance score.</span></span> 
    
8. <span data-ttu-id="9ae2a-129">, \*\*\*\* Oder übernehmen Sie den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-129">In **Set size**, or accept the default value.</span></span> <span data-ttu-id="9ae2a-130">Beachten Sie, dass die Wiederherstellungs Symbole die Standardwerte wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-130">Note that the restore icons will restore the default values.</span></span>
    
9. <span data-ttu-id="9ae2a-131">Klicken Sie auf **Tagging starten**.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-131">Click **Start tagging**.</span></span> <span data-ttu-id="9ae2a-132">Ein Test Beispiel wird generiert.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-132">A test sample is generated.</span></span>
    
10. <span data-ttu-id="9ae2a-133">Überarbeiten und markieren Sie die einzelnen Dateien auf der Registerkarte \*\* \> relevanztag\*\* , und klicken Sie anschließend auf **berechnen**.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-133">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span>
    
11. <span data-ttu-id="9ae2a-134">Auf der Registerkarte Test können Sie auf **Ergebnisse anzeigen** klicken, um die Testergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-134">In the Test tab, you can click **View results** to see the test results.</span></span> <span data-ttu-id="9ae2a-135">Ein Beispiel ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-135">An example is shown in the following figure.</span></span> 
    
    ![Testen der Rest-Ergebnisse](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
<span data-ttu-id="9ae2a-137">In der obigen Abbildung enthält der Abschnitt **Beispiel Parameter** der Tabelle Details zur Anzahl der Dateien im Beispiel, die vom Experten gekennzeichnet wurden, und die Anzahl der relevanten Dateien, die in diesem Beispiel gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-137">In the figure above, the **Sample parameters** section of the table contains details about the number of files in the sample tagged by the expert, and the number of relevant files found in that sample.</span></span> 
  
<span data-ttu-id="9ae2a-138">Der Abschnitt " **Population Parameters** " der Tabelle enthält die Testergebnisse, einschließlich der Überprüfung festgelegten Anzahl von Dateien mit einer Punktzahl unter dem ausgewählten Grenzwert und der "Rest"-Auffüllung von Dateien mit einer Bewertung über dem ausgewählten Grenzwert.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-138">The **Population parameters** section of the table contains the test results, including the Review set population of files with a score below the selected cutoff and "The Rest" population of files with a score above the selected cutoff.</span></span> <span data-ttu-id="9ae2a-139">Für jede Auffüllung werden die folgenden Ergebnisse angezeigt:</span><span class="sxs-lookup"><span data-stu-id="9ae2a-139">For each population, the following results are displayed:</span></span> 
  
- <span data-ttu-id="9ae2a-140">Enthält Dateien mit dem Read%-Grenzwert</span><span class="sxs-lookup"><span data-stu-id="9ae2a-140">Includes files with read % - Stated cutoff</span></span>
    
- <span data-ttu-id="9ae2a-141">Die Gesamtzahl der Dateien</span><span class="sxs-lookup"><span data-stu-id="9ae2a-141">The total number of files</span></span> 
    
- <span data-ttu-id="9ae2a-142">Die geschätzte Anzahl der relevanten Dateien</span><span class="sxs-lookup"><span data-stu-id="9ae2a-142">The estimated number of relevant files</span></span> 
    
- <span data-ttu-id="9ae2a-143">Die geschätzte Reichhaltigkeit</span><span class="sxs-lookup"><span data-stu-id="9ae2a-143">The estimated richness</span></span> 
    
- <span data-ttu-id="9ae2a-144">Die durchschnittlichen Überprüfungen der Suche nach einer anderen relevanten Datei</span><span class="sxs-lookup"><span data-stu-id="9ae2a-144">The average review cost of finding another relevant file</span></span>
    
## <a name="testing-the-slice"></a><span data-ttu-id="9ae2a-145">Testen des Segments</span><span class="sxs-lookup"><span data-stu-id="9ae2a-145">Testing the slice</span></span>

<span data-ttu-id="9ae2a-146">Der Test "Slice testen" führt Tests ähnlich dem Test "Test the Rest" durch, jedoch auf ein Segment der Dateigruppe gemäß der Relevanz Read%.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-146">The "Test the Slice" test performs testing similar to the "Test the Rest" test, but to a segment of the file set as specified by Relevance Read %.</span></span>
  
1. <span data-ttu-id="9ae2a-147">Öffnen Sie die Registerkarte **Relevanz \> testen** .</span><span class="sxs-lookup"><span data-stu-id="9ae2a-147">Open the **Relevance \> Test** tab.</span></span> 
    
2. <span data-ttu-id="9ae2a-148">Klicken Sie auf der Registerkarte **Test** auf **neuer Test**.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-148">In the **Test** tab, click **New test**.</span></span> <span data-ttu-id="9ae2a-149">Das Dialogfeld **Test erstellen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-149">The **Create test** dialog is displayed.</span></span> 
    
3. <span data-ttu-id="9ae2a-150">Geben \*\*\*\* Sie im Feld Testname und- **Beschreibung**die Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-150">In **Test name** and **Description**, type the information.</span></span>
    
4. <span data-ttu-id="9ae2a-151">Wählen Sie \*\*\*\* in der Liste Testtyp **die Option Slice testen**aus.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-151">In the **Test type** list, select **Test the Slice**.</span></span>
    
5. <span data-ttu-id="9ae2a-152">Wählen Sie in der Liste **Problem** den Problem Namen aus.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-152">In the **Issue** list, select the issue name.</span></span> 
    
6. <span data-ttu-id="9ae2a-153">Wählen Sie in der Liste **Laden** die Option Laden aus.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-153">In the **Load** list, select the load.</span></span> 
    
7. <span data-ttu-id="9ae2a-154">Übernehmen **Sie in% zwischen gelesen**die Standardwerte niedrig und hoch, oder wählen Sie Werte für die Ergebnisse der Cutoff-Relevanz aus.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-154">In **Read % between**, accept the default low and high range values or select values for the cutoff Relevance scores.</span></span> 
    
8. <span data-ttu-id="9ae2a-155">Wählen Sie unter **festGelegte Größe**einen Wert aus, oder übernehmen Sie den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-155">In **Set size**, select a value or accept the default value.</span></span>
    
    <span data-ttu-id="9ae2a-156">Die Wiederherstellungs Symbole stellen den Standardwert wieder her.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-156">The restore icons will restore the default value.</span></span>
    
9. <span data-ttu-id="9ae2a-157">Klicken Sie auf **Tagging starten**.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-157">Click **Start tagging**.</span></span> <span data-ttu-id="9ae2a-158">Ein Test Beispiel wird generiert.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-158">A test sample is generated.</span></span>
    
10. <span data-ttu-id="9ae2a-159">Überarbeiten und markieren Sie die einzelnen Dateien auf der Registerkarte \*\* \> relevanztag\*\* , und klicken Sie anschließend auf **berechnen**.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-159">Review and tag each of the files in the **Relevance \> Tag** tab and when done, click **Calculate**.</span></span> 
    
11. <span data-ttu-id="9ae2a-160">Auf der Registerkarte Test können Sie auf **Ergebnisse anzeigen** klicken, um die Testergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9ae2a-160">In the Test tab, you can click **View results** to see the test results.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="9ae2a-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ae2a-161">See also</span></span>

[<span data-ttu-id="9ae2a-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9ae2a-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="9ae2a-163">Bedeutung der Bewertung</span><span class="sxs-lookup"><span data-stu-id="9ae2a-163">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9ae2a-164">Tagging und Bewertung</span><span class="sxs-lookup"><span data-stu-id="9ae2a-164">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9ae2a-165">Tagging-und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="9ae2a-165">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9ae2a-166">Nachverfolgen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="9ae2a-166">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9ae2a-167">Entscheiden basierend auf den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="9ae2a-167">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)

