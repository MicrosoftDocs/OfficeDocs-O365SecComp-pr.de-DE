---
title: Einrichten von Smarttags für die Rechtsanwalt-Erkennung von Client Rechten in Advanced eDiscovery
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
ROBOTS: NOINDEX, NOFOLLOW
description: ''
ms.openlocfilehash: 721426f23aec862bcefbd13b8e61415dac3aeb27
ms.sourcegitcommit: aa8ea45d5854f8906714e0a407937585ec7993ad
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2019
ms.locfileid: "33951699"
---
# <a name="set-up-smart-tags-for-ml-assisted-review-in-advanced-ediscovery"></a><span data-ttu-id="fe2ed-102">Einrichten von Smarttags für die ml-gestützte Überprüfungen in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="fe2ed-102">Set up smart tags for ML-assisted review in Advanced eDiscovery</span></span>

<span data-ttu-id="fe2ed-103">Maschinelle Lernfunktionen in Advanced eDiscovery sollen dazu beitragen, den Entscheidungsprozess für Dokumente effizienter zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-103">Machine learning capabilities in Advanced eDiscovery are meant to help make decision process on documents more efficient.</span></span> <span data-ttu-id="fe2ed-104">Smarttags sind eine Möglichkeit, um die Computer Lernfunktionen in den Bereichen zu integrieren, in denen die Entscheidungen aufgezeichnet werden: Tags und Tag-Gruppen.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-104">Smart tags is a way to bring the machine learning capabilities into where the decisions are recorded: tags and tag groups.</span></span> <span data-ttu-id="fe2ed-105">Wenn Sie eine smarttaggruppe erstellen, werden die Entscheidungen des ml-Modells, das der Gruppe zugeordnet ist, Inline mit den Tags in der Gruppe angezeigt, damit Sie die Informationen Inline sehen können, wo Sie im Kontext am sinnvollsten sind.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-105">When you create a smart tag group, then the decisions of the ML model mapped to the group will be shown in-line with the tags in the group to help you see the information in-line, where they contextually make most sense.</span></span>

## <a name="how-to-set-up-a-smart-tag-group"></a><span data-ttu-id="fe2ed-106">Einrichten einer smarttaggruppe</span><span class="sxs-lookup"><span data-stu-id="fe2ed-106">How to set up a smart tag group</span></span>

1. <span data-ttu-id="fe2ed-107">Gehen Sie in einem Übersichts Satz zu **Manage Review Set** -> **Manage Tags**.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-107">In a review set, go to **Manage review set** -> **Manage tags**.</span></span>

2. <span data-ttu-id="fe2ed-108">Klicken Sie auf die Dropdownliste neben **Tag hinzufügen** , und wählen Sie **smarttaggruppe hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-108">Click on the drop-down next to **Add tag group** and select **Add smart tag group**.</span></span>

3. <span data-ttu-id="fe2ed-109">Wählen Sie das Modell aus, das Sie dieser Gruppe zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-109">Select the model you want to map to this group.</span></span> <span data-ttu-id="fe2ed-110">Dadurch werden ein Tag-Abschnitt und n untergeordnete Tags erstellt, wobei n die Anzahl der möglichen Ausgaben des Modells ist.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-110">This will create a tag section and N child tags, where N is the number of possible outputs of the model.</span></span> <span data-ttu-id="fe2ed-111">Beispielsweise hat das "Attorney-Client-Berechtigungs Erkennungs Modell" zwei mögliche Ausgänge-privileged und nicht privilegierte; Bei Auswahl dieses Modells werden zwei untergeordnete Tags im Übersichts Satz erstellt, die jeweils einer der möglichen Ausgaben entsprechen.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-111">For instance, attorney-client privilege detection model has two possible outputs - privileged and not privileged; selecting this model will create two child tags in the review set, each corresponding to one of the possible outputs.</span></span>

4. <span data-ttu-id="fe2ed-112">Benennen Sie die beschriftungsgruppe und die Markierungen entsprechend um.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-112">Rename the tag group and tags as you see fit.</span></span>

## <a name="how-to-use-a-smart-tag-group"></a><span data-ttu-id="fe2ed-113">Verwenden einer smarttaggruppe</span><span class="sxs-lookup"><span data-stu-id="fe2ed-113">How to use a smart tag group</span></span>

<span data-ttu-id="fe2ed-114">Beim Überprüfen eines Dokuments werden die Ergebnisse des Modells neben dem entsprechenden Tag-Wert angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-114">When reviewing a document, the model's results will be exposed next to the appropriate tag value.</span></span> <span data-ttu-id="fe2ed-115">Wenn Sie beispielsweise über eine smarttaggruppe für die Erkennung von Anwalts-und Clientberechtigungen verfügen und Sie ein Dokument überprüfen, das das Modell als potenziell privilegiert festgelegt hat, sehen Sie den Grund dafür neben dem entsprechenden Tag.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-115">For instance, if you have a smart tag group for attorney-client privilege detection and you review a document that the model has decided is potentially privileged, you will see the reason for that next to the appropriate tag.</span></span> <span data-ttu-id="fe2ed-116">Beachten Sie, dass das-Tag nicht automatisch angewendet wird. in allen Absichten und Zwecken fungieren Tags innerhalb einer smarttaggruppe genau wie normale Tags, mit dem Unterschied, dass Sie bei Bedarf die Modellergebnisse offen legen.</span><span class="sxs-lookup"><span data-stu-id="fe2ed-116">It is important to note that the tag is not automatically applied; for all intents and purposes, tags within a smart tag group act just like normal tags, except that they expose the model results next to them when appropriate.</span></span>