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
ms.openlocfilehash: 025fd90373313f762ce1d1dab8d48286e32e3cbb
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527183"
---
# <a name="add-data-to-a-review-set-from-another-review-set"></a><span data-ttu-id="75b78-102">Hinzufügen von Daten zu einem Übersichts Satz aus einem anderen überprüfungssatz</span><span class="sxs-lookup"><span data-stu-id="75b78-102">Add data to a review set from another review set</span></span>

<span data-ttu-id="75b78-103">In einigen Fällen kann es erforderlich sein, einen Teil der Dokumente aus einem Übersichts Satz zu schnitzen und einzeln in einem anderen Übersichts Satz zusammenzuarbeiten.</span><span class="sxs-lookup"><span data-stu-id="75b78-103">In some cases, it may be necessary to carve out a portion of documents from one review set and work with them individually in another review set.</span></span>  <span data-ttu-id="75b78-104">Dies ist besonders nützlich, wenn Sie Inhalte in einem Übersichts Satz abgeschlachtet haben und Analytics für die Teilmenge der Daten ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="75b78-104">This is especially useful if you've culled content in a review set and want to run analytics on the subset of data.</span></span>

<span data-ttu-id="75b78-105">Verwenden Sie den folgenden Workflow, um Inhalt von einem Übersichts Satz zu einem anderen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="75b78-105">Use the following workflow to add content from one review set to another.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="75b78-106">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="75b78-106">Before you begin</span></span>

<span data-ttu-id="75b78-107">Bevor Sie beginnen, müssen Sie einen neuen Übersichts Satz erstellen, dem Sie die Daten hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="75b78-107">Before you start, you'll need to create a new review set to add the data to.</span></span>  <span data-ttu-id="75b78-108">Auf der Registerkarte Übersichts **Sätze** des Falls kann ein neuer Übersichts Satz hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="75b78-108">A new review set can be added on the **Review sets** tab of the case.</span></span> <span data-ttu-id="75b78-109">Weitere Informationen finden Sie unter [Manage Review Sets](managing-review-sets.md).</span><span class="sxs-lookup"><span data-stu-id="75b78-109">For more information, see [Manage review sets](managing-review-sets.md).</span></span>

## <a name="step-1-identify-content-to-add-to-another-review-set"></a><span data-ttu-id="75b78-110">Schritt 1: Identifizieren von Inhalten, die einem anderen überprüfungssatz hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="75b78-110">Step 1: Identify content to add to another review set</span></span>

<span data-ttu-id="75b78-111">Sie können Inhalte zu einem Übersichts Satz hinzufügen, indem Sie e-Mails und Dokumente im Dokumentraster oder alle Elemente in einem Suchergebnis auswählen.</span><span class="sxs-lookup"><span data-stu-id="75b78-111">You can add content to a review set by selecting emails and documents in the document grid or all items in a search result.</span></span>  <span data-ttu-id="75b78-112">Wenn Sie ausgewählte Elemente hinzufügen möchten, wählen Sie die Elemente aus, klicken Sie auf **Aktion**, und klicken Sie dann auf **zu einem anderen überprüfungssatz hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="75b78-112">If choosing to add selected items, select the items, click **Action**, and then click **Add to another review set**.</span></span>

![Zu einem anderen Übersichts Satz hinzufügen](../media/64f2a4d4-eba3-4ab3-a3ba-d519feea3142.png)

## <a name="step-2-specify-options-for-adding-to-another-review-set"></a><span data-ttu-id="75b78-114">Schritt 2: Angeben von Optionen für das Hinzufügen zu einem anderen überprüfungssatz</span><span class="sxs-lookup"><span data-stu-id="75b78-114">Step 2: Specify options for adding to another review set</span></span>

<span data-ttu-id="75b78-115">Wählen Sie auf der Seite **zu einem anderen** Übersichts Flyout hinzufügen den Übersichts Satz aus, dem Sie die Elemente hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="75b78-115">In the **Add to another review set** flyout page, choose the review set you want to add the items to.</span></span> <span data-ttu-id="75b78-116">Wählen Sie aus, ob **alle Suchergebnisse** oder **ausgewählte Elemente**hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75b78-116">Choose whether to add **All search results** or **Selected items**.</span></span>  <span data-ttu-id="75b78-117">Zusätzliche Informationen bieten Optionen zum Einschließen aller Metadaten aus den Elementen und schließlich, ob die Dokument Tags in den neuen Übersichts Satz aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="75b78-117">Additional information provides options to include all metadata from the items and finally whether or not the document tags should be included in the new review set.</span></span>  <span data-ttu-id="75b78-118">Nachdem Sie auf **OK** geklickt haben, wird ein neuer Auftrag erstellt, um den Inhalt zu einem Übersichts Satz hinzuzufügen. Sie können den Fortschritt des Auftrags auf der Registerkarte **Auftrag** überwachen. Weitere Informationen finden Sie unter [Manage Jobs](managing-jobs-ediscovery20.md).</span><span class="sxs-lookup"><span data-stu-id="75b78-118">After clicking **Ok** a new job will be created to add the content to a review set; you can monitor the progress of that job on the **Job** tab. For more information, see [Manage jobs](managing-jobs-ediscovery20.md).</span></span>

![Zu einem anderen Übersichts Satz hinzufügen](../media/6440ee44-68fd-44d7-b43a-3a477345525c.png)
