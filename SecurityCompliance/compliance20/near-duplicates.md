---
title: Erkennung von Duplikaten in Ihrer Nähe.
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: a3f5945ee4ba0a1bc78ab6c8ccc9af934d392232
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607780"
---
# <a name="near-duplicate-detection"></a><span data-ttu-id="07182-102">Erkennung von Duplikaten in Ihrer Nähe.</span><span class="sxs-lookup"><span data-stu-id="07182-102">Near duplicate detection</span></span>

<span data-ttu-id="07182-p101">Erwägen Sie eine Gruppe von Dokumenten überprüft werden, in denen eine Teilmenge basiert auf derselben Vorlage und hauptsächlich der Textbausteine Sprachversion, mit einigen Unterschieden hier und da hat. Wenn ein Bearbeiter konnte diese Teilmenge zu identifizieren, finden Sie in einem von ihnen sorgfältig, und überprüfen Sie die Unterschiede für den Rest, würden sie nicht eindeutige Informationen verpasste beim Offlineschalten von nur eines Bruchs der Zeit, die alle Dokumente Abdeckung zu Abdeckung lesen hätte. Erkennung von Duplikaten NEAR gruppiert Textbefehl ähnliche Dokumente zusammen, mit denen Sie Ihre Überprüfungsprozess effizienter werden.</span><span class="sxs-lookup"><span data-stu-id="07182-p101">Consider a set of documents to be reviewed in which a subset is based on the same template and has mostly the same boilerplate language, with a few differences here and there. If a reviewer could identify this subset, review one of them thoroughly, and review the differences for the rest, they would not have missed any unique information while taking only a fraction of time that would have taken them to read all documents cover to cover. Near duplicate detection groups textually similar documents together to help you make your review process more efficient.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="07182-106">Wie funktioniert dies?</span><span class="sxs-lookup"><span data-stu-id="07182-106">How does it work?</span></span>

<span data-ttu-id="07182-p102">Wenn in Ihrer Nähe Erkennung von Duplikaten ausgeführt wird, analysiert das System jedes Dokument mit Text. Anschließend wird jedes Dokument gegeneinander, um festzustellen, ob ihre Ähnlichkeit größer als der festgelegte Schwellenwert ist verglichen. Es ist, werden die Dokumente zusammengefasst. Nachdem alle Dokumente im Vergleich und gruppiert wurden, wird ein Dokument aus jeder Gruppe als "Pivot"; gekennzeichnet. in Ihre Dokumente überprüfen, können Sie einen Pivot zuerst überprüfen und Lesen Sie die anderen Dokumente in der gleichen nahezu doppelte Set Konzentration auf den Unterschied zwischen den Pivot und das Dokument, das in Review ist.</span><span class="sxs-lookup"><span data-stu-id="07182-p102">When near duplicate detection is run, the system parses every document with text. Then, it compares every document against each other to determine whether their similarity is greater than the set threshold. If it is, the documents are grouped together. Once all documents have been compared and grouped, a document from each group is marked as the "pivot"; in reviewing your documents, you can review a pivot first and review the other documents in the same near duplicate set, focusing on the difference between the pivot and the document that is in review.</span></span>