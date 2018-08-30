---
title: Entscheidung basierend auf den Ergebnissen in Office 365 erweiterte eDiscovery
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
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Hier erfahren Sie, wie die Registerkarte Decide in Office 365 erweiterte eDiscovery, dass Daten, die Ihnen dabei helfen, die richtige Größe der Menge der Groß-/Kleinschreibung Dateien überprüfen bestimmen. '
ms.openlocfilehash: 58a181e00ad5843ccbbde4dcb47050eccf199225
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529166"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="26d97-103">Entscheidung basierend auf den Ergebnissen in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="26d97-103">Decision based on the results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="26d97-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="26d97-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
 <span data-ttu-id="26d97-106">In erweiterten eDiscovery bietet die Registerkarte Decide zusätzliche Informationen zum Anzeigen und Verwenden von Decision Support-Statistiken zum Bestimmen der Größe der Menge der Groß-/Kleinschreibung Dateien überprüfen.</span><span class="sxs-lookup"><span data-stu-id="26d97-106">In Advanced eDiscovery, the Decide tab provides additional information for viewing and using decision-support statistics for determining the size of the review set of case files.</span></span> 
  
## <a name="using-the-decide-tab"></a><span data-ttu-id="26d97-107">Mithilfe der Registerkarte Decide</span><span class="sxs-lookup"><span data-stu-id="26d97-107">Using the Decide tab</span></span>

![Relevanzentscheidung](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
<span data-ttu-id="26d97-109">Auf dieser Registerkarte umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="26d97-109">This tab includes the following:</span></span>
  
- <span data-ttu-id="26d97-110">**Problem**: Hier können Sie das Problem von Interesse aus der Liste auswählen.</span><span class="sxs-lookup"><span data-stu-id="26d97-110">**Issue**: From here, you can select the issue of interest from the list.</span></span> 
    
- <span data-ttu-id="26d97-p102">**Überprüfung-Rückruf Verhältnis**: Erweiterte Vergleich von eDiscovery-Überprüfung nach Relevanz Bewertungen. Der Grenzwert Punkt im Diagramm stellt den Prozentsatz der Dateien, um zu prüfen, einen Faktor Relevanz zugeordnet. Dies ist die Relevanz Testphase und als ein Export Schwellenwert für culling verwendet. Der standardmäßige trennwert Punkt für die Anzahl der Dateien, um zu prüfen wird an der Stelle, in dem das Gleichgewicht zwischen Rückruf und Precision optimal ist. Der tatsächliche trennwert Punkt sollte vom Benutzer je nach Zielen und die Kosten Kompromiss (% Überarbeitung) und das Risiko (% Rückruf) bestimmt werden. Verwenden den Schieberegler, können Sie den trennwert Punkt anpassen und finden Sie unter Auswirkungen auf das Diagramm und die Parameter, wenn Sie den Prozentsatz der relevanten Dateien abgerufen werden sollen, und vor dem Überprüfen einer Entscheidung anpassen.</span><span class="sxs-lookup"><span data-stu-id="26d97-p102">**Review-recall ratio**: Comparison of Advanced eDiscovery review according to Relevance scores. The Cutoff point in the chart represents the percentage of files to review, mapped to a Relevance score. This is used in the Relevance Test phase and as an Export threshold for culling. The default cutoff point, for the number of files to review is at the point in which the balance between Recall and Precision is optimal. The actual cutoff point should be determined by the user depending on objectives and the cost tradeoff (%review) and risk (%recall).Using the slider, you can adjust the cutoff point and see the effect on the graph and parameters, when adjusting the percent of relevant files to be retrieved, and before validating a decision.</span></span>
    
- <span data-ttu-id="26d97-p103">**Parameter**: Lesen, denken Sie daran, nächste relevant und Gesamtkosten-Parameter sind kumulative berechnete Statistiken für die Überprüfung in Bezug auf die Auflistung für die gesamte Groß-/Kleinschreibung festgelegt. Definitionen für diese Parameter sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="26d97-p103">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case. Definitions for these parameters are as follows:</span></span>
    
    <span data-ttu-id="26d97-118">**Überprüfen**: Prozentsatz der Dateien überprüfen basierend auf dieser Grenzwert.</span><span class="sxs-lookup"><span data-stu-id="26d97-118">**Review**: Percentage of files to review based on this cutoff.</span></span> 
    
    <span data-ttu-id="26d97-119">**Denken Sie daran**: Prozentsatz der entsprechenden Dateien in der Gruppe überprüfen.</span><span class="sxs-lookup"><span data-stu-id="26d97-119">**Recall**: Percentage of relevant files in the review set.</span></span> 
    
    <span data-ttu-id="26d97-120">**Nächsten relevanten**: Kosten, um zu prüfen, und identifizieren eine zusätzliche relevante Datei, die bei der Überprüfung zurzeit nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="26d97-120">**Next relevant**: Cost to review and identify an additional relevant file that is not currently in the review set.</span></span> 
    
    <span data-ttu-id="26d97-p104">**Gesamtkosten**: Kosten für die Überprüfung dieser Prozentsatz der Groß-/Kleinschreibung-Dateien. Von der Groß-/Kleinschreibung Manager können Einstellungen für die Kosten Parameter festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="26d97-p104">**Total cost**: Cost for reviewing this percentage of the case files. Cost parameter settings can be set by the Case manager.</span></span>
    
- <span data-ttu-id="26d97-p105">**Verteilung relevanzbewertung**: Dateien in die dunklen Grau Anzeige auf der linken Seite unterhalb der trennwert Score sind. Eine QuickInfo zeigt die Relevanz Bewertung und der zugehörigen Prozentsatz der Dateien in die Überprüfungsdatei in Bezug auf die Gesamtzahl der Dateien festgelegt.</span><span class="sxs-lookup"><span data-stu-id="26d97-p105">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score. A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
<span data-ttu-id="26d97-p106">Erweiterte Detailbereich werden weitere Details angezeigt. Dateien in der Auflistung Zahlen enthalten nicht leere ist oder unspezifisch Dateien. Produktfamilie Dateien Zahlen darstellen, Dateien, die nicht im Relevanz geladen, aber weiterhin im Rahmen der Produktfamilie gezählt.</span><span class="sxs-lookup"><span data-stu-id="26d97-p106">The expanded Details pane displays additional details. Files in collection figures do not include empty or nebulous files. Family files figures represent files that are not loaded in Relevance, yet still counted as part of the family.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26d97-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26d97-128">See also</span></span>

[<span data-ttu-id="26d97-129">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="26d97-129">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="26d97-130">Grundlegendes zur Bewertung in Relevanz</span><span class="sxs-lookup"><span data-stu-id="26d97-130">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="26d97-131">Kategorien und Bewertung</span><span class="sxs-lookup"><span data-stu-id="26d97-131">Tagging and Assessment</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="26d97-132">Ausführen der Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="26d97-132">Performing Relevance training</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="26d97-133">Nachverfolgen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="26d97-133">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="26d97-134">Testen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="26d97-134">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

