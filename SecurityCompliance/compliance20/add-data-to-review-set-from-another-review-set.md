---
title: Hinzufügen von Daten aus einem Übersichts Satz zu einem anderen überprüfungssatz
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
ms.openlocfilehash: 3a4d0d309daa5af9830f98215ca09321429785ee
ms.sourcegitcommit: 25595bc8fae96bc23b7b6d7102a22f37878987c0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/07/2019
ms.locfileid: "33641651"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a><span data-ttu-id="a097b-102">Hinzufügen von Daten zu einem Übersichts Satz aus einem anderen überprüfungssatz</span><span class="sxs-lookup"><span data-stu-id="a097b-102">Add data to a review set from another review set</span></span>

<span data-ttu-id="a097b-103">In einigen Fällen kann es erforderlich sein, einen Teil der Dokumente aus einem Übersichts Satz zu schnitzen und einzeln in einem anderen Übersichts Satz zusammenzuarbeiten.</span><span class="sxs-lookup"><span data-stu-id="a097b-103">In some cases, it may be necessary to carve out a portion of documents from one review set and work with them individually in another review set.</span></span>  <span data-ttu-id="a097b-104">Dies ist besonders nützlich, wenn Sie Inhalte in einem Übersichts Satz abgeschlachtet haben und Analytics für die Teilmenge der Daten ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="a097b-104">This is especially useful if you've culled content in a review set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="a097b-105">Folgen Sie dem Workflow in diesem Artikel, um Inhalt von einem Übersichts Satz zu einem anderen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a097b-105">Follow the workflow in this article to add content from one review set to another.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="a097b-106">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="a097b-106">Before you begin</span></span>

<span data-ttu-id="a097b-107">Bevor Sie beginnen, müssen Sie einen neuen Übersichts Satz erstellen, dem Sie die Daten hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="a097b-107">Before you start, you'll need to create a new review set to add the data to.</span></span>  <span data-ttu-id="a097b-108">Auf der Registerkarte Übersichts **Sätze** des Falls kann ein neuer Übersichts Satz hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a097b-108">A new review set can be added on the **Review sets** tab of the case.</span></span> <span data-ttu-id="a097b-109">Weitere Informationen finden Sie unter [Erstellen eines](managing-review-sets.md#create-a-review-set)Übersichts Satzes.</span><span class="sxs-lookup"><span data-stu-id="a097b-109">For more information, see [Create a review set](managing-review-sets.md#create-a-review-set).</span></span>

## <a name="step-1-identify-content-to-add-to-another-review-set"></a><span data-ttu-id="a097b-110">Schritt 1: Identifizieren von Inhalten, die einem anderen überprüfungssatz hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="a097b-110">Step 1: Identify content to add to another review set</span></span>

<span data-ttu-id="a097b-111">Sie können Inhalte aus einem Übersichts Satz zu einem anderen hinzufügen, indem Sie bestimmte Dokumente im Quell Übersichts Satz oder b seleting alle Elemente auswählen, die von der Übersichts Satz Abfrage zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a097b-111">You can add content from one review set to another one by selecting specific documents in the source review set or b seleting all items returned by review set query.</span></span>  <span data-ttu-id="a097b-112">Wenn Sie ausgewählte Elemente hinzufügen, wählen Sie die Elemente aus, klicken Sie auf **Aktion**, und klicken Sie dann auf **zu einem anderen überprüfungssatz hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a097b-112">If you're adding selected items, select the items, click **Action**, and then click **Add to another review set**.</span></span>

![Zu einem anderen Übersichts Satz hinzufügen](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a><span data-ttu-id="a097b-114">Schritt 2: Angeben von Optionen für das Hinzufügen zu einem anderen überprüfungssatz</span><span class="sxs-lookup"><span data-stu-id="a097b-114">Step 2: Specify options for adding to another review set</span></span>

<span data-ttu-id="a097b-115">Wählen Sie auf der Seite **zu einer anderen Option für Übersichts Optionen hinzufügen** den Übersichts Satz aus, dem Sie die Elemente hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="a097b-115">In the **Add to another review set options** flyout page, choose the review set you want to add the items to.</span></span> <span data-ttu-id="a097b-116">Wählen Sie aus, ob **alle Suchergebnisse** oder **ausgewählte Elemente**hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a097b-116">Choose whether to add **All search results** or **Selected items**.</span></span>  <span data-ttu-id="a097b-117">Zusätzliche Informationen bieten Optionen zum Einbeziehen aller Metadaten aus den Elementen und die Angabe, ob die Tags (durch Aktivieren des Kontrollkästchens **Beschriftungen** ) aus dem Quell Übersichts Satz eingeschlossen werden sollen, wenn die Dokumente dem neuen überprüfungssatz hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a097b-117">Additional information provides options to include all metadata from the items and whether to include the tags (by selecting the **Labels** checkbox) from the source review set when the documents are added to the new review set.</span></span>  

![Zu einem anderen Übersichts Satz hinzufügen](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)

<span data-ttu-id="a097b-119">Nachdem Sie auf **OK**geklickt haben, wird ein neuer Auftrag (mit dem Namen **Hinzufügen von Daten zu einem anderen**überprüfungssatz) erstellt, um den Inhalt zu einem anderen Übersichts Satz hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a097b-119">After you click **Ok**, a new job (named **Adding data to another review set**) is created to add the content to a another review set.</span></span>  <span data-ttu-id="a097b-120">Sie können zur Registerkarte **Jobs** wechseln und den Fortschritt dieses Auftrags überwachen.</span><span class="sxs-lookup"><span data-stu-id="a097b-120">You can go to **Jobs** tab and monitor the progress of this job.</span></span> <span data-ttu-id="a097b-121">Weitere Informationen finden Sie unter [Manage Jobs](managing-jobs-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="a097b-121">For more information, see [Manage jobs](managing-jobs-ediscovery20.md).</span></span>
