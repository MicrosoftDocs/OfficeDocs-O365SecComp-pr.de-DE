---
title: Designs
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 7c9d1a52acef48d96816fefbb1c836032d262b93
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32240977"
---
# <a name="themes"></a><span data-ttu-id="685de-102">Designs</span><span class="sxs-lookup"><span data-stu-id="685de-102">Themes</span></span>
<span data-ttu-id="685de-103">Wie schreibt ein Benutzer ein Dokument?</span><span class="sxs-lookup"><span data-stu-id="685de-103">How does a person write a document?</span></span> <span data-ttu-id="685de-104">Sie beginnen im Allgemeinen mit einem oder mehreren Ideen, die Sie im Dokument vermitteln möchten, und verfassen mit Wörtern, die sich an den Ideen ausrichten.</span><span class="sxs-lookup"><span data-stu-id="685de-104">They generally start with one or more ideas they want to convey in the document, and compose using words that align with the ideas.</span></span> <span data-ttu-id="685de-105">Je verbreiteter eine Idee ist, desto häufiger sind die Wörter, die mit dieser Idee in Verbindung stehen, in der Regel.</span><span class="sxs-lookup"><span data-stu-id="685de-105">The more prevalent an idea is, the more frequent the words that are related to that idea tend to be.</span></span> <span data-ttu-id="685de-106">Dies informiert darüber, wie Benutzer Dokumente auch nutzen; wichtig beim Lesen eines Dokuments ist die Idee, die das Dokument zu vermitteln versucht, und welche Ideen dort angezeigt werden und welche Beziehungen zwischen den Ideen bestehen.</span><span class="sxs-lookup"><span data-stu-id="685de-106">This informs how people consume documents as well; the important thing to get from reading a document is the ideas that the document is trying to convey, and which ideas appear where, and what the relationships between the ideas are.</span></span>

<span data-ttu-id="685de-107">Dies kann erweitert werden, um zu erfahren, wie eine Person eine Reihe von Dokumenten nutzen möchte.</span><span class="sxs-lookup"><span data-stu-id="685de-107">This can be extended to how a person wants to consume a set of documents.</span></span> <span data-ttu-id="685de-108">Sie möchten sehen, welche Ideen in den Sets enthalten sind und welche Dokumente über diese Ideen sprechen.</span><span class="sxs-lookup"><span data-stu-id="685de-108">They want to see which ideas are present in the sets, and which documents are talking about those ideas.</span></span> <span data-ttu-id="685de-109">Wenn Sie ein bestimmtes Dokument suchen, möchten Sie auch Dokumente anzeigen können, die ähnliche Ideen besprechen.</span><span class="sxs-lookup"><span data-stu-id="685de-109">Also, if they find a particular document of interest, they want to be able to see documents that discuss similar ideas.</span></span>

<span data-ttu-id="685de-110">Das Designmodul versucht, die Grundlagen der Menschen über Dokumente zu imitieren, indem die in einem Arbeitssatz besprochenen Designs analysiert und Dokumenten zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="685de-110">Themes module tries to mimic how humans reason about documents, by analyzing the "themes" that are discussed in a working set and assigning them to documents.</span></span> <span data-ttu-id="685de-111">Die Designs gehen einen Schritt weiter und identifizieren pro Dokument das "dominante Design"; d.h. das Design, das am meisten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="685de-111">Themes goes one step further and identifies per document the "dominant theme"; i.e. the theme that appears the most.</span></span>

## <a name="how-does-themes-work"></a><span data-ttu-id="685de-112">Wie funktionieren Designs?</span><span class="sxs-lookup"><span data-stu-id="685de-112">How does Themes work?</span></span>
<span data-ttu-id="685de-113">Designs analysiert Dokumente mit Text in einem Arbeitssatz, um allgemeine Designs zu analysieren, die in den Dokumenten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="685de-113">Themes analyzes documents with text in a working set to parse out common themes that appear accross the documents.</span></span> <span data-ttu-id="685de-114">Dann werden diese Designs den Dokumenten zugewiesen, in denen Sie angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="685de-114">Then, it assigns those themes to the documents in which they appear.</span></span> <span data-ttu-id="685de-115">Außerdem werden alle Wörter mit Wörtern in den Dokumenten gekennzeichnet, die für das Design repräsentativ sind.</span><span class="sxs-lookup"><span data-stu-id="685de-115">It also labels each with words used in the documents that are representative of the theme.</span></span> <span data-ttu-id="685de-116">Da es sich bei einem Dokument um mehr als einen Gegenstand handeln kann, ist in vielen Fällen einem Dokument mehr als ein Design zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="685de-116">Since a document can be about more than one subject matter, in many cases a document has more than one themes assigned to it.</span></span> <span data-ttu-id="685de-117">Das Design, das am deutlichsten in einem Dokument angezeigt wird, wird als dominierendes Design festgelegt.</span><span class="sxs-lookup"><span data-stu-id="685de-117">The theme that appears most prominently in a document is designated as its dominant theme.</span></span>