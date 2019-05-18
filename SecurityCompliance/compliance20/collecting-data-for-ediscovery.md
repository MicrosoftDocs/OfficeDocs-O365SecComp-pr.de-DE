---
title: Sammeln von Daten für einen Fall in Advanced eDiscovery
ms.author: esclee
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
ms.openlocfilehash: 8e67c3c8a693e627bade9e581f0f1e246bf6802a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151887"
---
# <a name="collect-data-for-a-case-in-advanced-ediscovery"></a><span data-ttu-id="ce9b3-102">Sammeln von Daten für einen Fall in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ce9b3-102">Collect data for a case in Advanced eDiscovery</span></span>

<span data-ttu-id="ce9b3-103">Nachdem Sie Verwalter und Datenquellen identifiziert haben, die für Ihren Fall von Interesse sind, müssen Sie die Dokumente identifizieren, in die Sie eintauchen möchten.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-103">Once you have identified custodians and data sources that are of interest for your case, it's time to identify the set of documents to delve into.</span></span> <span data-ttu-id="ce9b3-104">Sie können das Such Tool in Advanced eDiscovery verwenden, um diese von Freiheits-und nicht-Freiheits belassenen Speicherorten in Office 365 zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-104">You can use the Search tool in Advanced eDiscovery to identify these from custodial and non-custodial locations in Office 365.</span></span>

<span data-ttu-id="ce9b3-105">Nachdem Sie eine Suche ausgeführt haben, können Sie Statistiken zu den abgerufenen Elementen wie den Speicherorten anzeigen, die die meisten Elemente hatten, die mit der Suchabfrage übereinstimmten.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-105">After you run a search, you will be able to view statistics on the retrieved items such as the locations that had the most items that matched the search query.</span></span> <span data-ttu-id="ce9b3-106">Sie können auch eine Vorschau einer Teilmenge der Ergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-106">You can also preview a subset of the results.</span></span> <span data-ttu-id="ce9b3-107">Wenn Sie die Gruppe von Dokumenten identifiziert haben, die weiter untersucht werden sollen, können Sie die Suchergebnisse zu einem Überprüfungs Sätze hinzufügen, um Sie zu sammeln und zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-107">When you've identified the set of documents that want to further examine, you can add the search results to a review set to collect and process.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="ce9b3-108">Create a search</span><span class="sxs-lookup"><span data-stu-id="ce9b3-108">Create a search</span></span>

<span data-ttu-id="ce9b3-109">Wenn Sie auf der Registerkarte **Suchen** auf **neue Suche** klicken, wird ein Assistent gestartet, der Sie durch das Erstellen einer Suche führt.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-109">Clicking **New search** on the **Searches** tab will start a wizard that guides you through creating a search.</span></span> <span data-ttu-id="ce9b3-110">Ausführliche Informationen zum Erstellen einer Suche finden Sie unter [Erstellen einer Suche zum Erfassen von Daten](create-search-to-collect-data.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b3-110">For detailed information on how to create a search, see [Create a search to collect data](create-search-to-collect-data.md).</span></span>

<span data-ttu-id="ce9b3-111">Nachdem eine Suche erstellt wurde, wird eine Flyout-Seite mit Details angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-111">After a search is created, a flyout page with details is displayed.</span></span> <span data-ttu-id="ce9b3-112">Beachten Sie, dass die Schaltflächen **Statistik** und **Vorschau** anfänglich abgeblendet sind, da die Suche noch nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-112">Note that the **Statistics** and **Preview** buttons are initially grayed out because the search has not completed yet.</span></span> <span data-ttu-id="ce9b3-113">Sie können den Fortschritt der Suche auf der Registerkarte **Suchen** verfolgen.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-113">You can keep track of the progress of the search on the **Searches** tab.</span></span>

## <a name="view-search-results-and-statistics"></a><span data-ttu-id="ce9b3-114">Anzeigen von Suchergebnissen und Statistiken</span><span class="sxs-lookup"><span data-stu-id="ce9b3-114">View search results and statistics</span></span>
<span data-ttu-id="ce9b3-115">Es gibt zwei Komponenten einer Inhaltssuche: Statistik (Schätzungen) und Vorschau.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-115">There are two components of a content search: Statistics (Estimates) and Preview.</span></span> <span data-ttu-id="ce9b3-116">Nachdem jede dieser Komponenten abgeschlossen ist, wird der Status angezeigt, der in den entsprechenden Spalten auf der Registerkarte **Suchen** in geändert von von über **mittelte** zu **in** ausgeführt in **abgeschlossen**angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-116">As each of these components complete, you will see the status displayed in the corresponding columns on the **Searches** tab change from from **Submitted** to **In progress** to **Completed**.</span></span>

<span data-ttu-id="ce9b3-117">Wenn die Such Schätzung abgeschlossen ist, klicken Sie auf die Suche, um die Flyout-Seite anzuzeigen, in der einige allgemeine Statistiken zu den Ergebnissen der Suche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-117">Once the search estimate is completed, click the search to display the flyout page, which will display some high-level statistics about the results of the search.</span></span> <span data-ttu-id="ce9b3-118">Zu diesem Zeitpunkt ist die Schaltfläche **Statistik** aktiv.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-118">At this point, the **Statistics** button will be active.</span></span> <span data-ttu-id="ce9b3-119">Sie können darauf klicken, um Suchstatistiken anzuzeigen, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="ce9b3-119">You can click it to see search statistics, such as:</span></span>

- <span data-ttu-id="ce9b3-120">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ce9b3-120">Summary</span></span>
- <span data-ttu-id="ce9b3-121">Top-Standorte</span><span class="sxs-lookup"><span data-stu-id="ce9b3-121">Top locations</span></span>
- <span data-ttu-id="ce9b3-122">Abfragen</span><span class="sxs-lookup"><span data-stu-id="ce9b3-122">Queries</span></span>

<span data-ttu-id="ce9b3-123">Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistiken](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b3-123">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

<span data-ttu-id="ce9b3-124">Sobald die Vorschau abgeschlossen ist, wird die Schaltfläche **Vorschau** aktiv.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-124">Once preview is completed, the **Preview** button will be active.</span></span> <span data-ttu-id="ce9b3-125">Klicken Sie darauf, um eine ausgewählte Teilmenge der Ergebnisse in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-125">Click it to preview a sampled subset of the results.</span></span>

## <a name="adding-search-results-to-a-review-set"></a><span data-ttu-id="ce9b3-126">Hinzufügen von Suchergebnissen zu einer Überprüfungsgruppe</span><span class="sxs-lookup"><span data-stu-id="ce9b3-126">Adding search results to a review set</span></span>

<span data-ttu-id="ce9b3-127">Wenn Sie bereit sind, die gesamten Ergebnisse einer Suche zu sammeln und zu verarbeiten, können Sie dies tun, indem Sie es zu einem Überprüfungs Satzes hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ce9b3-127">When you are ready to collect and process the entire results of a search, you can do so by adding it to a review set.</span></span> <span data-ttu-id="ce9b3-128">Ausführliche Informationen finden Sie unter [Hinzufügen von Daten zu einem Überprüfungs Sätze](add-data-to-review-set.md).</span><span class="sxs-lookup"><span data-stu-id="ce9b3-128">For details, see [Add data to a review set](add-data-to-review-set.md).</span></span> 