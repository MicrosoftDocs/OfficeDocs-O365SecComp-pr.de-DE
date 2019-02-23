---
title: Erkennen von Quasiduplikaten
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 40270fa1e3a6f7cdf0dd2a83650aa36a935d9a6d
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213125"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="219f5-102">Erkennen von Quasiduplikaten</span><span class="sxs-lookup"><span data-stu-id="219f5-102">Near duplicate detection</span></span>

<span data-ttu-id="219f5-p101">Betrachten Sie eine Gruppe von Dokumenten, die überprüft werden sollen, wobei eine Teilmenge auf derselben Vorlage basiert und größtenteils die gleiche Standardsprache hat, mit ein paar unterschieden hier und dort. Wenn ein Prüfer diese Teilmenge identifizieren, eine gründlich überprüfen und die Unterschiede für den Rest überprüfen könnte, würden Sie keine eindeutigen Informationen verpasst haben, während Sie nur einen Bruchteil der Zeit, die Sie dazu ergriffen hätte, alle Dokumente zu decken lesen. In der Nähe von doppelten Erkennungs Gruppen werden Text ähnliche Dokumente zusammengeführt, damit Sie den Überprüfungsprozess effizienter gestalten können.</span><span class="sxs-lookup"><span data-stu-id="219f5-p101">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there. If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover. Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="219f5-106">Wie funktioniert dies?</span><span class="sxs-lookup"><span data-stu-id="219f5-106">How does it work?</span></span>

<span data-ttu-id="219f5-p102">Wenn die Erkennung nahezu doppelt ausgeführt wird, analysiert das System jedes Dokument mit Text. Dann vergleicht es jedes Dokument gegeneinander, um zu bestimmen, ob Ihre Ähnlichkeit größer als der festgelegte Schwellenwert ist. Wenn dies der Fall ist, werden die Dokumente gruppiert. Nachdem alle Dokumente verglichen und gruppiert wurden, wird ein Dokument aus jeder Gruppe als "Pivot" markiert; Wenn Sie Ihre Dokumente überprüfen, können Sie zuerst ein Pivot überprüfen und die anderen Dokumente in derselben fast doppelt vorhandenen Gruppe überprüfen, wobei der Fokus auf dem Unterschied zwischen dem Pivot und dem Dokument liegt, das sich im Rückblick befindet.</span><span class="sxs-lookup"><span data-stu-id="219f5-p102">When near duplicate detection is run, the system parses every document with text. Then, it compares every document against each other to determine whether their similarity is greater than the set threshold. If it is, the documents are grouped together. Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>