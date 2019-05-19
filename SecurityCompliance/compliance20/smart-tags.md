---
title: Einrichten von Smarttags für die Erkennung von Anwalts-Client-Berechtigungen in Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 5310acad1aa1bc2e01cbabee69dd7bb38084bd9a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34153967"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a><span data-ttu-id="02f9d-102">Einrichten von Smarttags für die ml-unterstützte Überprüfung in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="02f9d-102">Set up smart tags for ML-assisted review in Advanced eDiscovery</span></span>

<span data-ttu-id="02f9d-103">Maschinelle Lernfunktionen in Advanced eDiscovery sollen helfen, den Entscheidungsprozess in Dokumenten effizienter zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="02f9d-103">Machine learning capabilities in Advanced eDiscovery are meant to help make decision process on documents more efficient.</span></span> <span data-ttu-id="02f9d-104">Smarttags sind eine Möglichkeit, die Lernfunktionen des Computers in die Position zu versetzen, an der die Entscheidungen erfasst werden: Tags und Tag-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="02f9d-104">Smart tags is a way to bring the machine learning capabilities into where the decisions are recorded: tags and tag groups.</span></span> <span data-ttu-id="02f9d-105">Wenn Sie eine smarttaggruppe erstellen, werden die Entscheidungen des ml-Modells, das der Gruppe zugeordnet ist, Inline mit den Tags in der Gruppe angezeigt, damit Sie die Informationen Inline anzeigen können, wo Sie am ehesten Sinn ergeben.</span><span class="sxs-lookup"><span data-stu-id="02f9d-105">When you create a smart tag group, then the decisions of the ML model mapped to the group will be shown in-line with the tags in the group to help you see the information in-line, where they contextually make most sense.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="02f9d-106">Vorgehensweise Einrichten einer smarttaggruppe</span><span class="sxs-lookup"><span data-stu-id="02f9d-106">How to set up a smart tag group</span></span>

1. <span data-ttu-id="02f9d-107">Wechseln Sie in einem Überprüfungs Satzes zu **Manage Review-Gruppe** -> **Manage Tags**.</span><span class="sxs-lookup"><span data-stu-id="02f9d-107">In a review set, go to **Manage review set** -> **Manage tags**.</span></span>

2. <span data-ttu-id="02f9d-108">Klicken Sie auf die Dropdownliste neben **Transpondergruppe hinzufügen** , und wählen Sie **smarttaggruppe hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="02f9d-108">Click on the drop-down next to **Add tag group** and select **Add smart tag group**.</span></span>

3. <span data-ttu-id="02f9d-109">Wählen Sie das Modell aus, das Sie dieser Gruppe zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="02f9d-109">Select the model you want to map to this group.</span></span> <span data-ttu-id="02f9d-110">Dadurch werden ein Tag-Abschnitt und n untergeordnete Tags erstellt, wobei n für die Anzahl der möglichen Ausgaben des Modells steht.</span><span class="sxs-lookup"><span data-stu-id="02f9d-110">This will create a tag section and N child tags, where N is the number of possible outputs of the model.</span></span> <span data-ttu-id="02f9d-111">Beispielsweise weist das Client-Berechtigungs Erkennungs Modell zwei mögliche Ausgaben auf – privilegierte und nicht privilegierte; durch die Auswahl dieses Modells werden zwei untergeordnete Tags in der Überprüfungsgruppe erstellt, die jeweils einer der möglichen Ausgaben entsprechen.</span><span class="sxs-lookup"><span data-stu-id="02f9d-111">For instance, attorney-client privilege detection model has two possible outputs - privileged and not privileged; selecting this model will create two child tags in the review set, each corresponding to one of the possible outputs.</span></span>

4. <span data-ttu-id="02f9d-112">Benennen Sie die Transpondergruppe und die Tags entsprechend ihrer Größe um.</span><span class="sxs-lookup"><span data-stu-id="02f9d-112">Rename the tag group and tags as you see fit.</span></span>

## <a name="how-to-use-a-smart-tag-group"></a><span data-ttu-id="02f9d-113">Vorgehensweise verwenden einer smarttaggruppe</span><span class="sxs-lookup"><span data-stu-id="02f9d-113">How to use a smart tag group</span></span>

<span data-ttu-id="02f9d-114">Wenn Sie ein Dokument überprüfen, werden die Ergebnisse des Modells neben dem entsprechenden Transponderwert verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="02f9d-114">When reviewing a document, the model's results will be exposed next to the appropriate tag value.</span></span> <span data-ttu-id="02f9d-115">Wenn Sie beispielsweise über eine smarttaggruppe für die Erkennung von Anwalts-und Client Rechten verfügen und ein Dokument überprüfen, das das Modell als potenziell privilegiert hat, wird der Grund dafür neben dem entsprechenden Tag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02f9d-115">For instance, if you have a smart tag group for attorney-client privilege detection and you review a document that the model has decided is potentially privileged, you will see the reason for that next to the appropriate tag.</span></span> <span data-ttu-id="02f9d-116">Es ist wichtig zu beachten, dass das Tag nicht automatisch angewendet wird; für alle Absichten und Zwecke fungieren Tags innerhalb einer smarttaggruppe genauso wie normale Tags, mit dem Unterschied, dass Sie die Modellergebnisse neben Ihnen verfügbar machen, wenn dies angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="02f9d-116">It is important to note that the tag is not automatically applied; for all intents and purposes, tags within a smart tag group act just like normal tags, except that they expose the model results next to them when appropriate.</span></span>