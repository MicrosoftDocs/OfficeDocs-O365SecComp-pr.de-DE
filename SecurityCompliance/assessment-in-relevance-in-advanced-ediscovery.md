---
title: Grundlegendes zur Beurteilung in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: Hier erhalten Sie einen Überblick über die Bewertungsstufe und ihre Rolle bei der Ermittlung der reichhaltigen Probleme beim Relevanz-Training in Office 365 Advanced eDiscovery.
ms.openlocfilehash: 1ddaa7ef37f762d7b63bb6c0c51193ff382b8d6b
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212975"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a><span data-ttu-id="e9eec-103">Grundlegendes zur Beurteilung in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="e9eec-103">Understand Assessment in Relevance in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="e9eec-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="e9eec-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="e9eec-p102">Advanced eDiscovery ermöglicht eine frühe Bewertung, beispielsweise für die definierten Probleme und die für einen Fall importierten Daten. Advanced eDiscovery ermöglicht es dem Experten, Entscheidungen über eine angenommene Vorgehensweise zu treffen und diese auf das Dokument Übersichts Projekt anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="e9eec-p102">Advanced eDiscovery enables early assessment, for example, for the defined issues and the data imported for a case. Advanced eDiscovery enables the expert to make decisions pertaining to an adopted approach and to apply them to the document review project.</span></span>
  
## <a name="understanding-assessment"></a><span data-ttu-id="e9eec-108">Grundlegendes zur Bewertung</span><span class="sxs-lookup"><span data-stu-id="e9eec-108">Understanding assessment</span></span>

<span data-ttu-id="e9eec-p103">In der Bewertung prüft der Experte eine zufällige Gruppe von mindestens 500-Dateien, die verwendet werden, um die Reichhaltigkeit der Probleme zu bestimmen und um Statistiken zu erstellen, die die Trainingsergebnisse widerspiegeln. Die Bewertung ist erfolgreich, wenn genügend relevante Dateien gefunden werden, um einen statistischen Grad zu erreichen, der die FortgeSchrittene eDiscovery-Relevanz für genaue Statistiken und zur effektiven Bestimmung des Stabilisierungs Punkts im Schulungsprozess unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e9eec-p103">In Assessment, the expert reviews a random set of at least 500 files, which are used to determine the richness of the issues and to produce statistics that reflect the training results. Assessment is successful when enough relevant files are found to reach a statistical level that will help Advanced eDiscovery Relevance to provide accurate statistics and to effectively determine the stabilization point in the training process.</span></span> 
  
<span data-ttu-id="e9eec-p104">Je höher die Anzahl der relevanten Dateien in der Bewertung ist, desto genauer sind die Statistiken und die Effektivität des Stabilitäts Algorithmus. Die Anzahl der relevanten Dateien in den Evaluierungs Dateien hängt vom Umfang des Problems ab. Reichtum ist der geschätzte Prozentsatz der relevanten Dateien in der Gruppe, die für ein Problem relevant ist. Probleme mit höherer Reichweite erreichen eine höhere Anzahl von relevanten Dateien schneller als Probleme mit geringem Umfang. Probleme mit extrem geringem Reichtum (beispielsweise 2% oder weniger) erfordern eine sehr umfangreiche Bewertung, um eine beträchtliche Anzahl von relevanten Dateien zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="e9eec-p104">The higher the number of relevant files in the assessment set, the more accurate the statistics and the effectiveness of the stability algorithm. The number of relevant files within the assessment files depends on the richness of the issue. Richness is the estimated percent of relevant files in the set relevant to an issue. Issues with higher richness will reach a higher number of relevant files more quickly than issues with lower richness. Issues with extremely low richness (for example, 2% or less) will require a very large assessment set to reach a significant number of Relevant files.</span></span>
  
<span data-ttu-id="e9eec-p105">Die Statistiken, die während des Trainings und nach der Batch Berechnung auf den Registerkarten "Titel" und "Entscheidung" angezeigt werden, enthalten Schätzungen des Rückrufs für verschiedene Übersichts Sätze. In Statistiken sind Schätzungen, die auf einer Beispiel Gruppe basieren (in diesem Fall die Bewertungsdateien), die Fehlertoleranz und die Zuverlässigkeitsstufe dieses fehlerbereichs. Beispielsweise kann der geschätzte Rückruf von 80% einen Fehlerwert von Plus oder minus 5% mit einer Konfidenz Stufe von 95% aufweisen. Dies bedeutet, dass der geschätzte Rückruf tatsächlich 75%-85% ist und diese Schätzung 95% vertrauenswürdig ist. Je größer der Bewertungs Satz ist, desto geringer ist der Fehlerspielraum, und die Statistiken sind genauer.</span><span class="sxs-lookup"><span data-stu-id="e9eec-p105">The statistics, which are presented in the Track and Decide tabs during training and after Batch calculation, include estimations of recall for different review sets. In statistics, estimations that are based on a sample set (in this case, the assessment files) include the margin of error and the confidence level of that error margin. For example, estimated recall of 80% might have a margin of error of plus or minus 5% with a confidence level of 95%. This means that the estimated recall is actually 75%-85% and this estimation has 95% confidence. The larger the assessment set, the margin of error becomes smaller and the statistics are more accurate.</span></span> 
  
<span data-ttu-id="e9eec-p106">Nachdem der Experte einen anfänglichen Bewertungs Satz von 500-Dateien überprüft hat, kann die Relevanz den aktuellen Fehler Rand der Rückruf Werte bestimmen. Relevanz wird auch einen standardmäßigen Fehler Rand festlegen, der zur Optimierung des Bewertungs Satzes empfohlen wird. Es folgen einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="e9eec-p106">After the expert reviews an initial assessment set of 500 files, Relevance is able to determine the current margin of error of the recall values. Relevance will also set a default margin of error that it recommends to reach to optimize the assessment set. Following are some examples:</span></span>
  
- <span data-ttu-id="e9eec-124">Wenn für den assessmentsatz bereits eine Fehlergrenze von Plus oder minus 10% vorliegt, wird empfohlen, zur Schulung zu wechseln (es ist keine zusätzliche Bewertung erforderlich).</span><span class="sxs-lookup"><span data-stu-id="e9eec-124">If the assessment set already yielded a margin of error of plus or minus 10%, Relevance will recommend to move on to training (no additional assessment review is needed).</span></span> 
    
- <span data-ttu-id="e9eec-125">Wenn der Beurteilungs Satz eine Fehlergrenze von Plus oder minus 13% ergab, kann die Relevanz die Überprüfung eines anderen Satzes von Bewertungsdateien empfehlen, um einen geringeren Seitenrand zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="e9eec-125">If the assessment set yielded a margin of error of plus or minus 13%, Relevance might recommend the review of another set of assessment files to reach a smaller margin.</span></span> 
    
- <span data-ttu-id="e9eec-126">Wenn der Umfang äußerst gering ist, empfiehlt es sich möglicherweise, die Bewertung zu beenden, obwohl die Fehlergrenze hoch ist (Statistiken sind nicht praktikabel), da die zum Erreichen einer nützlichen Fehlergrenze erforderliche Bewertung zu umfangreich ist.</span><span class="sxs-lookup"><span data-stu-id="e9eec-126">If richness is extremely low, Relevance might recommend stopping assessment even though the margin of error is large (making statistics impractical), because the assessment set needed to reach a useful margin of error is too large.</span></span>
    
<span data-ttu-id="e9eec-p107">Jedes Problem hat seinen eigenen Umfang, den aktuellen Fehlerspielraum und als Ergebnis die geschätzte Anzahl zusätzlicher Evaluierungs Dateien. Der nächste Bewertungs Satz wird entsprechend der maximalen Anzahl von Dateien (bis zu 1.000 in einem einzelnen Satz) erstellt.</span><span class="sxs-lookup"><span data-stu-id="e9eec-p107">Each issue has its own richness, current margin of error, and as a result, estimated number of additional assessment files. The next assessment set is created according to the maximum number of files (up to 1,000 in a single set).</span></span>
  
<span data-ttu-id="e9eec-p108">Sie können die Relevanz-Empfehlungen akzeptieren oder den aktuellen Fehlerspielraum gemäß Ihren Anforderungen anpassen. Der standardmäßige aktuelle Fehler ist für den Rückruf bei gleich oder über 75% bestimmt.</span><span class="sxs-lookup"><span data-stu-id="e9eec-p108">You can accept the Relevance recommendations or adjust the current margin of error according to your needs. The default current margin of error is determined for recall at equal or above 75%.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e9eec-p109">Die Bewertungsstufe kann auf der Registerkarte \*\* \> Relevanz verfolgen\*\* in der erweiterten Ansicht für ein Problem umgangen werden, indem das Kontrollkästchen **Bewertung** pro Problem und dann für alle Probleme deaktiviert wird. Daher gibt es für dieses Problem keine Statistiken. > das Kontrollkästchen **Bewertung** kann nur ausgeführt werden, bevor die Bewertung durchgeführt wird. Wenn in einem Fall mehrere Probleme vorhanden sind, wird die Bewertung nur umgangen, wenn das Kontrollkästchen für jedes Problem deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e9eec-p109">The Assessment stage can be bypassed, in the **Relevance \> Track** tab in the expanded view for an issue, by clearing the **Assessment** check box per issue and then for "all issues". However, as a result, there will be no statistics for this issue. > Clearing the **Assessment** check box can only be done before assessment is performed. Where multiple issues exist in a case, assessment is bypassed only if the check box is cleared for each issue</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9eec-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9eec-135">See also</span></span>

[<span data-ttu-id="e9eec-136">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="e9eec-136">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="e9eec-137">Tagging und Bewertung</span><span class="sxs-lookup"><span data-stu-id="e9eec-137">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="e9eec-138">Tagging-und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="e9eec-138">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="e9eec-139">Nachverfolgen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="e9eec-139">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="e9eec-140">Entscheiden basierend auf den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="e9eec-140">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="e9eec-141">Testen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="e9eec-141">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

