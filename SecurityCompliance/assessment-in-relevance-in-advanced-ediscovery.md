---
title: Grundlegendes zu Assessment in Relevanz in Office 365 erweiterte eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: 'Rufen Sie eine Übersicht über die Bewertungsphase und seiner Rolle bei der Bestimmung der Umfang der Probleme während der Relevanz Schulung in Office 365 erweiterte eDiscovery.  '
ms.openlocfilehash: a54a4134609b16568586f3cb6b60ebdeba860bac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529461"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a><span data-ttu-id="0e8f4-103">Grundlegendes zu Assessment in Relevanz in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0e8f4-103">Understand Assessment in Relevance in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="0e8f4-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="0e8f4-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="0e8f4-p102">Erweiterte eDiscovery ermöglicht frühe Bewertung, beispielsweise für die definierten Probleme und die Daten für eine Anfrage importiert. Erweiterte eDiscovery ermöglicht den Experten für einen angenommene Ansatz Entscheidungen treffen Sie auf Überprüfung Dokumentprojekt anwenden.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-p102">Advanced eDiscovery enables early assessment, for example, for the defined issues and the data imported for a case. Advanced eDiscovery enables the expert to make decisions pertaining to an adopted approach and to apply them to the document review project.</span></span>
  
## <a name="understanding-assessment"></a><span data-ttu-id="0e8f4-108">Grundlegendes zur Bewertung</span><span class="sxs-lookup"><span data-stu-id="0e8f4-108">Understanding assessment</span></span>

<span data-ttu-id="0e8f4-p103">Bewertung überprüft der Experte einen zufällig ausgewählten Satz von mindestens 500-Dateien, die verwendet werden, um den Umfang der Probleme zu ermitteln und Statistiken zu erstellen, die die Schulung Ergebnisse widerspiegeln. Assessment ist erfolgreich, wenn genügend relevanten Dateien gefunden werden, ein statistische Niveau erreicht, die erweiterte eDiscovery Relevanz genaue Statistiken bereitstellen und tatsächlich die Stabilisierung Stelle der Schulung bestimmen helfen.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-p103">In Assessment, the expert reviews a random set of at least 500 files, which are used to determine the richness of the issues and to produce statistics that reflect the training results. Assessment is successful when enough relevant files are found to reach a statistical level that will help Advanced eDiscovery Relevance to provide accurate statistics and to effectively determine the stabilization point in the training process.</span></span> 
  
<span data-ttu-id="0e8f4-p104">Je höher die Anzahl der relevanten in die Bewertung festgelegt sind, desto genauer die Statistiken und die Effektivität des Algorithmus Stabilität Dateien. Die Anzahl der relevanten Dateien innerhalb der Bewertung Dateien hängt vom Umfang des Problems. Wie umfangreich ist der geschätzte Prozentsatz der entsprechenden Dateien in der Gruppe für ein Problem relevant. Probleme mit einer höheren Funktionsvielfalt werden eine größere Anzahl von relevanten Dateien schneller als Probleme mit niedrigeren Funktionsvielfalt erreichen. Probleme mit sehr niedrige Funktionsvielfalt (beispielsweise 2 % oder weniger) erfordern eine sehr große Bewertung gesetzt, um eine beträchtliche Anzahl von relevanten Dateien zu.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-p104">The higher the number of relevant files in the assessment set, the more accurate the statistics and the effectiveness of the stability algorithm. The number of relevant files within the assessment files depends on the richness of the issue. Richness is the estimated percent of relevant files in the set relevant to an issue. Issues with higher richness will reach a higher number of relevant files more quickly than issues with lower richness. Issues with extremely low richness (for example, 2% or less) will require a very large assessment set to reach a significant number of Relevant files.</span></span>
  
<span data-ttu-id="0e8f4-p105">Die Statistiken, die in den Registerkarten nachverfolgen und Decide während der Schulung und nach der Batch Berechnung vorgelegt werden, umfassen Abschätzung der Rückruf für verschiedene Überprüfung festgelegt. Innerhalb der Statistik, Einschätzung, die auf einer Stichprobe basieren festgelegt (in diesem Fall die Assessment-Dateien) enthalten, dem der Fehler und die Vertrauensstufe der jeweilige Fehler Rand. Beispielsweise möglicherweise geschätzte Rückruf 80 % Rand Fehler von Plus oder minus 5 % mit einer Vertrauensstufe von 95 %. Dies bedeutet, dass der geschätzte Rückruf ist tatsächlich 75-85 % dieser Schätzung 95 % Confidence hat. Je größer der Bewertung festgelegt, wird des Rands des Fehlers kleiner und die Statistiken verständlich sind.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-p105">The statistics, which are presented in the Track and Decide tabs during training and after Batch calculation, include estimations of recall for different review sets. In statistics, estimations that are based on a sample set (in this case, the assessment files) include the margin of error and the confidence level of that error margin. For example, estimated recall of 80% might have a margin of error of plus or minus 5% with a confidence level of 95%. This means that the estimated recall is actually 75%-85% and this estimation has 95% confidence. The larger the assessment set, the margin of error becomes smaller and the statistics are more accurate.</span></span> 
  
<span data-ttu-id="0e8f4-p106">Nachdem der Experte eine erste Einschätzung Menge von 500 Dateien überprüft, kann Relevanz den aktuellen Rand von Fehler der Rückruf Werte zu bestimmen. Relevanz wird auch einen standardmäßigen Rand des Fehlers festgelegt, die es empfiehlt erreichen, um die Bewertung zu optimieren. Es folgen einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="0e8f4-p106">After the expert reviews an initial assessment set of 500 files, Relevance is able to determine the current margin of error of the recall values. Relevance will also set a default margin of error that it recommends to reach to optimize the assessment set. Following are some examples:</span></span>
  
- <span data-ttu-id="0e8f4-124">Wenn die Bewertung bereits einen Rand des Fehlers von Plus oder minus 10 % bereitgestellt wurde, wird Relevanz wird empfohlen, zu Schulungen verschieben, klicken Sie auf (keine zusätzliche Bewertung ist erforderlich).</span><span class="sxs-lookup"><span data-stu-id="0e8f4-124">If the assessment set already yielded a margin of error of plus or minus 10%, Relevance will recommend to move on to training (no additional assessment review is needed).</span></span> 
    
- <span data-ttu-id="0e8f4-125">Wenn der Bewertung Satz einen Rand des Fehlers von Plus oder minus 13 % brachte, möglicherweise Relevanz wird die Überprüfung von einem anderen Satz von Assessment Dateien in einen kleineren Rand erreichen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-125">If the assessment set yielded a margin of error of plus or minus 13%, Relevance might recommend the review of another set of assessment files to reach a smaller margin.</span></span> 
    
- <span data-ttu-id="0e8f4-126">Wenn Funktionsvielfalt sehr gering ist, wird Relevanz möglicherweise empfehlen Assessment stoppen, obwohl der Rand des Fehlers (wobei Statistiken nicht praktikabel) groß ist, da festgelegten Assessment benötigt, um eine nützliche Rand von Fehler zu erreichen ist zu groß.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-126">If richness is extremely low, Relevance might recommend stopping assessment even though the margin of error is large (making statistics impractical), because the assessment set needed to reach a useful margin of error is too large.</span></span>
    
<span data-ttu-id="0e8f4-p107">Jedes Problem verfügt über eine eigene Funktionsvielfalt, aktuellen Rand von Fehler, und daher geschätzte Anzahl der zusätzliche Assessment-Dateien. Der nächste Satz Assessment wird entsprechend die maximale Anzahl von Dateien (bis zu 1.000 in einem einzigen Satz) erstellt.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-p107">Each issue has its own richness, current margin of error, and as a result, estimated number of additional assessment files. The next assessment set is created according to the maximum number of files (up to 1,000 in a single set).</span></span>
  
<span data-ttu-id="0e8f4-p108">Können Sie die Relevanz Empfehlungen akzeptieren oder den aktuellen Rand von Fehler entsprechend Ihren Anforderungen anpassen. Der aktuellen standardmäßigen Rand des Fehlers wird für den Wiederaufruf gleich mindestens 75 % bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0e8f4-p108">You can accept the Relevance recommendations or adjust the current margin of error according to your needs. The default current margin of error is determined for recall at equal or above 75%.</span></span>
  
> [!NOTE]
> <span data-ttu-id="0e8f4-p109">Die Phase Assessment kann umgangen werden, in der **Relevanz \> nachverfolgen** Registerkarte in der erweiterten Ansicht für ein Problem, indem Sie das Kontrollkästchen **Assessment** pro Problem, und klicken Sie dann für "alle Probleme" deaktivieren. Dementsprechend, werden es jedoch keine Statistiken für dieses Problem. > Deaktivieren des Kontrollkästchens **Assessment** kann nur ausgeführt werden, bevor Assessment ausgeführt wird. In dem Fall mehrere Probleme vorhanden sind, wird zur Bewertung umgangen nur, wenn das Kontrollkästchen für jedes Problem deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="0e8f4-p109">The Assessment stage can be bypassed, in the **Relevance \> Track** tab in the expanded view for an issue, by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e8f4-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e8f4-135">See also</span></span>

[<span data-ttu-id="0e8f4-136">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0e8f4-136">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="0e8f4-137">Kategorien und Bewertung</span><span class="sxs-lookup"><span data-stu-id="0e8f4-137">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0e8f4-138">Kategorien und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="0e8f4-138">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0e8f4-139">Nachverfolgen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="0e8f4-139">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0e8f4-140">Entscheiden je nach den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="0e8f4-140">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="0e8f4-141">Testen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="0e8f4-141">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

