---
title: Entscheidungen basierend auf den Ergebnissen in Office 365 Advanced eDiscovery
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
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Erfahren Sie, wie die Registerkarte "entscheiden" in Office 365 Advanced eDiscovery Daten enthält, die Sie bei der Bestimmung der richtigen Größe der Fall Dateien unterstützen können. '
ms.openlocfilehash: c4767e703d03ef5dbdb808332e873d22094d7bca
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216105"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="f0201-103">Entscheidungen basierend auf den Ergebnissen in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f0201-103">Decision based on the results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="f0201-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="f0201-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
 <span data-ttu-id="f0201-106">In Advanced eDiscovery bietet die Registerkarte entscheiden zusätzliche Informationen zum Anzeigen und Verwenden von Entscheidungs Unterstützungs Statistiken, um die Größe der Fall Dateien zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f0201-106">In Advanced eDiscovery, the Decide tab provides additional information for viewing and using decision-support statistics for determining the size of the review set of case files.</span></span> 
  
## <a name="using-the-decide-tab"></a><span data-ttu-id="f0201-107">Verwenden der Registerkarte "entscheiden"</span><span class="sxs-lookup"><span data-stu-id="f0201-107">Using the Decide tab</span></span>

![Relevanzentscheidung](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
<span data-ttu-id="f0201-109">Diese Registerkarte umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f0201-109">This tab includes the following:</span></span>
  
- <span data-ttu-id="f0201-110">**Problem**: von hier aus können Sie das gewünschte Problem aus der Liste auswählen.</span><span class="sxs-lookup"><span data-stu-id="f0201-110">**Issue**: From here, you can select the issue of interest from the list.</span></span> 
    
- <span data-ttu-id="f0201-p102">**Review-Recall Ratio**: Vergleich der erweiterten eDiscovery-Überprüfungen gemäß Relevanz-Bewertungen. Der Grenzpunkt im Diagramm gibt den Prozentsatz der zu überprüfenden Dateien an, die einem Relevanzwert zugeordnet sind. Dies wird in der Relevanz-Testphase und als Export Schwellenwert für das Culling verwendet. Der Standardgrenzwert für die Anzahl der zu überprüfenden Dateien ist der Punkt, an dem das Gleichgewichtzwischen Rückruf und Genauigkeit optimal ist. Der tatsächliche Grenzwert sollte vom Benutzer abhängig von den Zielsetzungen und dem Kostennachteil (% Review) und Risiko (% Recall) bestimmt werden. Mithilfe des Schiebereglers können Sie den Cutoff-Punkt anpassen und die Auswirkungen auf das Diagramm und die Parameter anzeigen, wenn Sie den Prozentsatz der relevanten Dateien, die abgerufen werden sollen, anpassen und bevor Sie eine Entscheidung überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f0201-p102">**Review-recall ratio**: Comparison of Advanced eDiscovery review according to Relevance scores. The Cutoff point in the chart represents the percentage of files to review, mapped to a Relevance score. This is used in the Relevance Test phase and as an Export threshold for culling. The default cutoff point, for the number of files to review is at the point in which the balance between Recall and Precision is optimal. The actual cutoff point should be determined by the user depending on objectives and the cost tradeoff (%review) and risk (%recall).Using the slider, you can adjust the cutoff point and see the effect on the graph and parameters, when adjusting the percent of relevant files to be retrieved, and before validating a decision.</span></span>
    
- <span data-ttu-id="f0201-p103">**Parameter**: Review, Recall, Next relevant and Total Cost Parameters sind kumulative berechnete Statistiken, die sich auf den Übersichts Satz beziehen, der im Zusammenhang mit der Sammlung für den gesamten Fall gilt. Definitionen für diese Parameter:</span><span class="sxs-lookup"><span data-stu-id="f0201-p103">**Parameters**: Review, Recall, Next relevant and Total cost parameters are cumulative calculated statistics pertaining to the review set in relation to the collection for the entire case. Definitions for these parameters are as follows:</span></span>
    
    <span data-ttu-id="f0201-118">**Review**: Prozentsatz der zu überprüfenden Dateien basierend auf diesem Cutoff.</span><span class="sxs-lookup"><span data-stu-id="f0201-118">**Review**: Percentage of files to review based on this cutoff.</span></span> 
    
    <span data-ttu-id="f0201-119">**Recall**: Prozentsatz der relevanten Dateien im Übersichts Satz.</span><span class="sxs-lookup"><span data-stu-id="f0201-119">**Recall**: Percentage of relevant files in the review set.</span></span> 
    
    <span data-ttu-id="f0201-120">**Als nächstes relevant**: Kosten zum Überprüfen und Identifizieren einer zusätzlichen relevanten Datei, die sich derzeit nicht im Übersichts Satz befindet.</span><span class="sxs-lookup"><span data-stu-id="f0201-120">**Next relevant**: Cost to review and identify an additional relevant file that is not currently in the review set.</span></span> 
    
    <span data-ttu-id="f0201-p104">**Gesamtkosten**: Kosten für die Überprüfung dieses Prozentsatzes der Fall Dateien. Einstellungen für Kosten Parameter können vom Fall-Manager festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f0201-p104">**Total cost**: Cost for reviewing this percentage of the case files. Cost parameter settings can be set by the Case manager.</span></span>
    
- <span data-ttu-id="f0201-p105">**Verteilung nach Relevanz Bewertung**: Dateien in der dunkelgrauen Anzeige Links befinden sich unterhalb der Cutoff-Bewertung. Ein QuickInfo zeigt den Relevanzwert und den zugehörigen Prozentsatz der Dateien in der Übersichtsdatei im Verhältnis zu den Gesamtdateien an.</span><span class="sxs-lookup"><span data-stu-id="f0201-p105">**Distribution by relevance score**: Files in the dark gray display to the left are below the cutoff score. A tool-tip displays the Relevance score and the related percentage of files in the review file set in relation to the total files.</span></span>
    
<span data-ttu-id="f0201-p106">Im erweiterten Detailbereich werden zusätzliche Details angezeigt. Dateien in Sammlungs Abbildungen enthalten keine leeren oder nebligen Dateien. Bei Familiendateien handelt es sich um Dateien, die nicht in Relevanz geladen, aber noch als Teil der Familie gezählt werden.</span><span class="sxs-lookup"><span data-stu-id="f0201-p106">The expanded Details pane displays additional details. Files in collection figures do not include empty or nebulous files. Family files figures represent files that are not loaded in Relevance, yet still counted as part of the family.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f0201-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0201-128">See also</span></span>

[<span data-ttu-id="f0201-129">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="f0201-129">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="f0201-130">Bedeutung der Bewertung</span><span class="sxs-lookup"><span data-stu-id="f0201-130">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f0201-131">Tagging und Bewertung</span><span class="sxs-lookup"><span data-stu-id="f0201-131">Tagging and Assessment</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f0201-132">Durchführen von Relevanz-Schulungen</span><span class="sxs-lookup"><span data-stu-id="f0201-132">Performing Relevance training</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f0201-133">Nachverfolgen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="f0201-133">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="f0201-134">Testen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="f0201-134">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

