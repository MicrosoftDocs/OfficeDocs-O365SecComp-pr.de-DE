---
title: Erfassen von Daten für einen Fall in Advanced eDiscovery (Preview)
ms.author: esclee
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
ms.openlocfilehash: fb4b36841394576c44667f9677507c5655179e45
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455417"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery-preview"></a><span data-ttu-id="6d256-102">Erfassen von Daten für einen Fall in Advanced eDiscovery (Preview)</span><span class="sxs-lookup"><span data-stu-id="6d256-102">Collect data for a case in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="6d256-103">Nachdem Sie Verwalter und Datenquellen identifiziert haben, die für Ihren Fall von Interesse sind, ist es an der Zeit, die Dokumente zu identifizieren, in die Sie eintauchen möchten.</span><span class="sxs-lookup"><span data-stu-id="6d256-103">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into.</span></span> <span data-ttu-id="6d256-104">Sie können das Such Tool in Advanced eDiscovery (Preview) verwenden, um diese in Office 365 zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6d256-104">You can use the Search tool in Advanced eDiscovery (Preview) to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="6d256-105">Nachdem Sie eine Suche ausgeführt haben, können Sie Statistiken zu den abgerufenen Elementen wie den Standorten mit den meisten Elementen anzeigen, die mit der Suchabfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="6d256-105">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query.</span></span> <span data-ttu-id="6d256-106">Sie können auch eine Vorschau einer Teilmenge der Ergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6d256-106">You can also preview a subset of the results.</span></span> <span data-ttu-id="6d256-107">Wenn Sie die Gruppe von Dokumenten identifiziert haben, die Sie genauer untersuchen möchten, können Sie die Suchergebnisse einem Arbeitssatz hinzufügen und verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6d256-107">When you've identified the set of documents that want to further examine, you can add the search results to a working set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="6d256-108">Create a search</span><span class="sxs-lookup"><span data-stu-id="6d256-108">Create a search</span></span>

<span data-ttu-id="6d256-109">Wenn Sie auf der Registerkarte **Suchvorgänge** auf **neue Suche** klicken, wird ein Assistent gestartet, der Sie beim Erstellen einer Suche unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6d256-109">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search.</span></span> <span data-ttu-id="6d256-110">Ausführliche Informationen zum Erstellen einer Suche finden Sie unter [Erstellen einer Suche zum Sammeln von Daten](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="6d256-110">For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="6d256-111">Nachdem eine Suche erstellt wurde, wird eine Flyout-Seite mit Details angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6d256-111">After a search is created, a flyout page with details is displayed.</span></span> <span data-ttu-id="6d256-112">Beachten Sie, dass die Schaltflächen **Statistiken** und **Vorschau** anfänglich abgeblendet sind, da die Suche noch nicht abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="6d256-112">Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet.</span></span> <span data-ttu-id="6d256-113">Sie können den Fortschritt der Suche auf der Registerkarte **Suchvorgänge** verfolgen.</span><span class="sxs-lookup"><span data-stu-id="6d256-113">You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="6d256-114">Anzeigen von Suchergebnissen und Statistiken</span><span class="sxs-lookup"><span data-stu-id="6d256-114">View search results and statistics</span></span>
<span data-ttu-id="6d256-115">Es gibt zwei Komponenten einer Inhaltssuche: Statistiken (Schätzungen) und Vorschau.</span><span class="sxs-lookup"><span data-stu-id="6d256-115">There are two components of a content search: Statistics (Estimates) and Preview.</span></span> <span data-ttu-id="6d256-116">Sobald jede dieser Komponenten abgeschlossen ist, wird der Status in den entsprechenden Spalten auf der Registerkarte " **Suchen** " von "von" von "über **mittelt** " **in "in Bearbeitung** " angezeigt. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="6d256-116">As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="6d256-117">Klicken Sie nach Abschluss der Such Schätzung auf die Suche, um die Seite Flyout anzuzeigen, in der einige allgemeine Statistiken zu den Ergebnissen der Suche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6d256-117">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search.</span></span> <span data-ttu-id="6d256-118">Zu diesem Zeitpunkt ist die Schaltfläche **Statistik** aktiv.</span><span class="sxs-lookup"><span data-stu-id="6d256-118">At this point, the **Statistics** button will be active.</span></span> <span data-ttu-id="6d256-119">Sie können darauf klicken, um Suchstatistiken anzuzeigen, wie beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="6d256-119">You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="6d256-120">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="6d256-120">Summary</span></span>
- <span data-ttu-id="6d256-121">Top-Standorte</span><span class="sxs-lookup"><span data-stu-id="6d256-121">Top locations</span></span>
- <span data-ttu-id="6d256-122">Abfragen</span><span class="sxs-lookup"><span data-stu-id="6d256-122">Queries</span></span>

<span data-ttu-id="6d256-123">Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistiken](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="6d256-123">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="6d256-124">Sobald die Vorschau abgeschlossen ist, ist die Schaltfläche **Vorschau** aktiv.</span><span class="sxs-lookup"><span data-stu-id="6d256-124">Once preview is completed, the **Preview** button will be active.</span></span> <span data-ttu-id="6d256-125">Klicken Sie darauf, um eine Vorschau einer abgetasteten Teilmenge der Ergebnisse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="6d256-125">Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-working-set"></a><span data-ttu-id="6d256-126">Hinzufügen von Suchergebnissen zu einem Workingset</span><span class="sxs-lookup"><span data-stu-id="6d256-126">Adding search results to a working set</span></span>

<span data-ttu-id="6d256-127">Wenn Sie bereit sind, die gesamten Ergebnisse einer Suche zu sammeln und zu verarbeiten, können Sie Sie einem Arbeitssatz hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6d256-127">When you are ready to collect and process the entire results of a search, you can do so by adding it to a working set.</span></span> <span data-ttu-id="6d256-128">Weitere Informationen finden Sie unter [Hinzufügen von Daten zu einem Workingset](add-data-to-working-set.md).</span><span class="sxs-lookup"><span data-stu-id="6d256-128">For details, see [Add data to a working set](add-data-to-working-set.md).</span></span> 