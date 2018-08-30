---
title: Grundlegendes zu Dokument Ähnlichkeit in Office 365 erweiterte eDiscovery
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
ms.assetid: 4d4cb381-4c9a-4165-a455-609d525c7a88
description: 'Überprüfen Sie die Funktionsweise von Dokument Ähnlichkeit-Wert, der minimale Ebene der Ähnlichkeit für zwei Dateien in Ihrer Nähe Duplikate gezogen werden in Office 365 erweiterte eDiscovery. '
ms.openlocfilehash: 39cd8c31204f0164f6b52c71fa707253cb22758a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529281"
---
# <a name="understand-document-similarity-in-office-365-advanced-ediscovery"></a><span data-ttu-id="8f8fa-103">Grundlegendes zu Dokument Ähnlichkeit in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8f8fa-103">Understand document similarity in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="8f8fa-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="8f8fa-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="8f8fa-106">In erweiterten eDiscovery ist Dokument Ähnlichkeit die minimale Ebene der Ähnlichkeit von zwei Dokumenten berücksichtigt werden, als in der Nähe Duplikate erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-106">In Advanced eDiscovery, Document Similarity is the minimal level of resemblance required for two documents to be considered as near-duplicates.</span></span>
  
> [!TIP]
> <span data-ttu-id="8f8fa-p102">Für die meisten Geschäftsanwendungen wird empfohlen, einen Wert Ähnlichkeit von 60-75 % verwenden. Für sehr niedrige Qualität optischen zeichenerkennung (OCR) Material niedrigerer Ähnlichkeit Werte angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-p102">For most business applications, it is recommended to use a Similarity value of 60%-75%. For very poor quality optical character recognition (OCR) material, lower Similarity values can be applied.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8f8fa-109">Nach dem Festlegen und für einen bestimmten Fall ausgeführt hat, kann der Wert der Ähnlichkeit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-109">After it's set and run for a given case, the Similarity value cannot be changed.</span></span> 
  
<span data-ttu-id="8f8fa-p103">Innerhalb eines Satzes Near-Duplicate (ND) möglicherweise Dokumente mit einer Ebene der Ähnlichkeit unter dem Schwellenwert Ähnlichkeit. Für ein Dokument an eine Menge ND teilnehmen muss mindestens ein Dokument in der mit einer Ebene der Ähnlichkeit überschreiten der Ähnlichkeit festlegen ND vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-p103">Within a Near-duplicate (ND) set, there may be documents with a level of resemblance below the Similarity threshold. For a document to join an ND set, there must be at least one document in the ND set with a level of resemblance exceeding the Similarity.</span></span> 
  
<span data-ttu-id="8f8fa-112">Nehmen wir beispielsweise an die Ähnlichkeit auf 80 % festgelegt ist, Dokument F1 ähnelt Dokument F2 auf einer Ebene der 85 % und Dokument F2 ähnelt Dokument F3 in Höhe von 90 %.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-112">For example, assume the Similarity is set to 80%, document F1 resembles document F2 at a level of 85%, and document F2 resembles document F3 at a level of 90%.</span></span> 
  
<span data-ttu-id="8f8fa-p104">Dokument F1 kann jedoch Dokument F3 auf einer Ebene nur 70 % ähneln sich unter dem Schwellenwert für handelt. Legen Sie dennoch in diesem Beispiel Dokumente F1, F2 und F3, die alle in der eine ND angezeigt werden. In ähnlicher Weise den Wert 80 % Ähnlichkeit verwenden, wir möglicherweise zwei Sätze, EquiSet-1 und EquiSet-2 erstellt haben. EquiSet-1 enthält Dokumente E1 und E2. Equiset-2 enthält die Dokumente F1, F2 und F3.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-p104">However, document F1 may resemble document F3 at a level of only 70%, which is below the threshold. Nonetheless, in this example, documents F1, F2, and F3 all appear in the one ND set. Similarly, using a Similarity value of 80%, we may have created two sets, EquiSet-1 and EquiSet-2. EquiSet-1 contains documents E1 and E2. Equiset-2 contains documents F1, F2, and F3.</span></span> 
  
<span data-ttu-id="8f8fa-118">Die Ebenen der Ähnlichkeit sind wie folgt dargestellt:</span><span class="sxs-lookup"><span data-stu-id="8f8fa-118">The levels of resemblance are illustrated as follows:</span></span>
  
![Dokumentähnlichkeit](media/3907ea7d-e28a-4027-8fc3-be090dd39144.gif)
  
<span data-ttu-id="8f8fa-p105">Wird davon ausgegangen Sie, dass ein anderes Dokument, X1, nun eingefügt wird. Der Ähnlichkeit zwischen X1 und E3 ist 87 %. In ähnlicher Weise wird die Ähnlichkeit zwischen X1 und F1 92 %. Daher EquiSet -1,-2 EquiSet und X1 werden jetzt kombiniert in einem ND festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-p105">Assume that another document, X1, is now inserted. The resemblance between X1 and E3 is 87%. Similarly, the resemblance between X1 and F1 is 92%. As a result, EquiSet -1, EquiSet -2, and X1 are now combined into one ND set.</span></span>
  
![Dokumentähnlichkeit](media/d140d347-33d5-475a-af04-594a0f2ab13d.gif)
  
> [!NOTE]
> <span data-ttu-id="8f8fa-125">Wenn zwei Dokumente sind einem ND Satz zugeordnet, zusammen in den gleichen Satz ND bleiben wird, auch wenn zusätzliche Dokumente werden hinzugefügt, das Festlegen oder die legt zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-125">If any two documents are assigned to one ND set, they will remain together in the same ND set, even if additional documents are added to the set or if the sets are merged.</span></span> 
  
<span data-ttu-id="8f8fa-126">Nach dem legt zusammengeführt werden, kann das Pivot-Dokument ändern, wenn eine Reihe neuer Dokumente hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8f8fa-126">After sets are merged, the Pivot document can change when new documents are added to a set.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f8fa-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f8fa-127">See also</span></span>

[<span data-ttu-id="8f8fa-128">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="8f8fa-128">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="8f8fa-129">Festlegen von Optionen für Analyse</span><span class="sxs-lookup"><span data-stu-id="8f8fa-129">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8f8fa-130">Die Einstellung Text ignorieren</span><span class="sxs-lookup"><span data-stu-id="8f8fa-130">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8f8fa-131">Analysieren der Einstellung Erweiterte Einstellungen</span><span class="sxs-lookup"><span data-stu-id="8f8fa-131">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="8f8fa-132">Anzeigen von Ergebnissen der Analyse</span><span class="sxs-lookup"><span data-stu-id="8f8fa-132">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

