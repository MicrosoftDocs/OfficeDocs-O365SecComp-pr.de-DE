---
title: Erkennen von Quasiduplikaten
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 7ae5e695091d140089f979f28793876a2df77251
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34150577"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="0d941-102">Erkennen von Quasiduplikaten</span><span class="sxs-lookup"><span data-stu-id="0d941-102">Near duplicate detection</span></span>

<span data-ttu-id="0d941-103">Betrachten Sie eine Reihe von Dokumenten, die überprüft werden sollen, in denen eine Teilmenge auf derselben Vorlage basiert und meist die gleiche Standardsprache mit einigen Unterschieden.</span><span class="sxs-lookup"><span data-stu-id="0d941-103">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there.</span></span> <span data-ttu-id="0d941-104">Wenn ein Prüfer diese Teilmenge identifizieren konnte, überprüfen Sie eine von Ihnen gründlich, und überprüfen Sie die Unterschiede für den Rest, würden Sie keine eindeutigen Informationen verpasst haben, wobei nur ein Bruchteil der Zeit, die Sie zum Lesen aller Dokument Deckung zur Deckung genommen hätte.</span><span class="sxs-lookup"><span data-stu-id="0d941-104">If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover.</span></span> <span data-ttu-id="0d941-105">In der Nähe von doppelten Erkennung Gruppen werden Text ähnliche Dokumente zusammengefasst, die Ihnen dabei helfen, den Überprüfungsprozess effizienter zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="0d941-105">Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="0d941-106">Wie funktioniert dies?</span><span class="sxs-lookup"><span data-stu-id="0d941-106">How does it work?</span></span>

<span data-ttu-id="0d941-107">Wenn die Erkennung in der Nähe von Duplikaten ausgeführt wird, analysiert das System jedes Dokument mit Text.</span><span class="sxs-lookup"><span data-stu-id="0d941-107">When near duplicate detection is run, the system parses every document with text.</span></span> <span data-ttu-id="0d941-108">Anschließend vergleicht es jedes Dokument gegeneinander, um zu bestimmen, ob seine Ähnlichkeit größer als der festgelegte Schwellenwert ist.</span><span class="sxs-lookup"><span data-stu-id="0d941-108">Then, it compares every document against each other to determine whether their similarity is greater than the set threshold.</span></span> <span data-ttu-id="0d941-109">Wenn dies der Fall ist, werden die Dokumente zusammen gruppiert.</span><span class="sxs-lookup"><span data-stu-id="0d941-109">If it is, the documents are grouped together.</span></span> <span data-ttu-id="0d941-110">Nachdem alle Dokumente verglichen und gruppiert wurden, wird ein Dokument aus jeder Gruppe als "Pivot" gekennzeichnet. Wenn Sie Ihre Dokumente überprüfen, können Sie zuerst einen Pivot überprüfen und die anderen Dokumente in derselben nahe doppelten Gruppe überprüfen, wobei Sie sich auf den Unterschied zwischen dem Pivot und dem Dokument konzentrieren, das sich in der Überprüfung befindet.</span><span class="sxs-lookup"><span data-stu-id="0d941-110">Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>