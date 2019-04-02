---
title: Suchstatistiken
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
ms.openlocfilehash: 986c3f3cbb19cd0f66b18db274e68a3bf8414952
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030128"
---
# <a name="search-statistics"></a><span data-ttu-id="56448-102">Suchstatistiken</span><span class="sxs-lookup"><span data-stu-id="56448-102">Search statistics</span></span>

<span data-ttu-id="56448-103">Eine effektive Möglichkeit zum Überprüfen der Suchergebnisse bei der Untersuchung eines Daten Vorfalls, um die Statistiken über Ihre Suchergebnisse anzuzeigen, um sicherzustellen, dass Sie Ihren Erwartungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56448-103">An effective way to validate your search results when investigation a data incident is to view the statistics about your search results to make sure they align with your expectations.</span></span> <span data-ttu-id="56448-104">Wenn eine Suche ausgeführt wird, werden die folgenden allgemeinen Statistiken unter **Status** auf der Seite Suchdetails-Flyout angezeigt:</span><span class="sxs-lookup"><span data-stu-id="56448-104">When a search as finished running, the following high-level statistics are displayed under **Status** on the search details flyout page:</span></span>

![Such statisics auf Suchdetails-Flyout-Seite](../media/SearchDetailsFlyout.png)

- <span data-ttu-id="56448-106">Die geschätzte Anzahl und Größe der Elemente, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56448-106">The estimated number and size of items that matched the search criteria.</span></span>

- <span data-ttu-id="56448-107">Die Anzahl und Größe von teilweise indizierten Elementen (auch als nicht indizierte *Elemente*bezeichnet), die nicht durchsuchbar sind, aber in den Inhaltsspeicherorten gefunden wurden, die in der Suche enthalten waren.</span><span class="sxs-lookup"><span data-stu-id="56448-107">The number and size of partially indexed items (also called *unindexed items*) that aren't searchable but that were found in the content locations that were included in the search.</span></span>

- <span data-ttu-id="56448-108">Die Anzahl der Postfächer und Websites, die durchsucht wurden.</span><span class="sxs-lookup"><span data-stu-id="56448-108">The number of mailboxes and sites that were searched.</span></span>

<span data-ttu-id="56448-109">Wenn Sie detailliertere Statistiken anzeigen möchten, klicken Sie auf der Seite Suchdetails-Flyout auf **Statistiken** .</span><span class="sxs-lookup"><span data-stu-id="56448-109">To view more detailed statistics, click **Statistics** on the search details flyout page.</span></span> <span data-ttu-id="56448-110">Auf der Seite **Suchstatistiken** können Sie die Suchzusammenfassung, den Top-Speicherort mit Elementen, die mit den Suchergebnissen übereinstimmen, sowie detaillierte Statistiken zur Suchabfrage anzeigen.</span><span class="sxs-lookup"><span data-stu-id="56448-110">On the **Search statistics** page, you can view the search summary, the top location that contained items that matched the search results, and detailed statistics about the search query.</span></span>

![Dropdownliste für Suchstatistiken](../media/SearchStatisticsDropDownList.png)

## <a name="summary"></a><span data-ttu-id="56448-112">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="56448-112">Summary</span></span>

<span data-ttu-id="56448-113">In der **Zusammenfassungs** Ansicht können die Suchergebnisse nach Standorttyp aufgeschlüsselt angezeigt werden (beispielsweise sind Speicherorte Exchange-Postfächer und SharePoint-Websites).</span><span class="sxs-lookup"><span data-stu-id="56448-113">In the **Summary** view, you can see the search results broken down by location type (for example, locations include Exchange mailboxes and SharePoint sites).</span></span> <span data-ttu-id="56448-114">Die folgenden Informationen werden für jeden Standorttyp angezeigt:</span><span class="sxs-lookup"><span data-stu-id="56448-114">The following information is displayed for each location type:</span></span>

- <span data-ttu-id="56448-115">Die Anzahl der Standorte mit Elementen, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56448-115">The number of locations that had items that matched the search criteria.</span></span>

- <span data-ttu-id="56448-116">Die Gesamtzahl der Elemente aus jedem Speicherorttyp, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56448-116">The total number of items from each location type that matched the search criteria.</span></span>

- <span data-ttu-id="56448-117">Die Gesamtgröße der Elemente aus jedem Speicherorttyp, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56448-117">The total size of items from each location type that matched the search criteria.</span></span>

## <a name="top-locations"></a><span data-ttu-id="56448-118">Top-Standorte</span><span class="sxs-lookup"><span data-stu-id="56448-118">Top locations</span></span>

<span data-ttu-id="56448-119">In der Ansicht der **oberen Speicherorte** werden die einzelnen inhaltsspeicherorte mit den meisten Elementen angezeigt, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56448-119">In the **Top locations** view, you see the individual content locations with the most items that matched the search criteria.</span></span> <span data-ttu-id="56448-120">Für jeden Inhaltsspeicherort werden die folgenden Informationen angezeigt:</span><span class="sxs-lookup"><span data-stu-id="56448-120">For each content location, the following information is displayed:</span></span>

- <span data-ttu-id="56448-121">Der Name des Speicherorts; die e-Mail-Adresse für Postfächer und die URL für SharePoint-Websites</span><span class="sxs-lookup"><span data-stu-id="56448-121">The name of the location; the email address for mailboxes and the URL for SharePoint sites</span></span>

- <span data-ttu-id="56448-122">Der Speicherorttyp</span><span class="sxs-lookup"><span data-stu-id="56448-122">The location type</span></span>

- <span data-ttu-id="56448-123">Anzahl der Elemente, die den Suchkriterien entsprechen</span><span class="sxs-lookup"><span data-stu-id="56448-123">Number of items that matched the search criteria</span></span>

- <span data-ttu-id="56448-124">Die Gesamtgröße aller Elemente, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56448-124">The total size of all items that matched the search criteria.</span></span>

## <a name="queries"></a><span data-ttu-id="56448-125">Abfragen</span><span class="sxs-lookup"><span data-stu-id="56448-125">Queries</span></span>

<span data-ttu-id="56448-126">In der Ansicht **Abfragen** können Sie detaillierte Statistiken für jede Komponente der Suchabfrage anzeigen.</span><span class="sxs-lookup"><span data-stu-id="56448-126">In the **Queries** view, you can see detailed statistics for each component of the search query.</span></span> <span data-ttu-id="56448-127">Wenn Sie die Stichwortliste in der Suchabfrage verwendet haben, können Sie in der Ansicht **Abfragen** Erweiterte Statistiken anzeigen, die zeigen, wie viele Elemente mit den einzelnen Schlüsselwörtern oder Schlüsselwörtern übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="56448-127">If you used the keyword list in the search query, you can view enhanced statistics in the **Queries** view  that show how many items match each keyword or keyword phrase.</span></span> <span data-ttu-id="56448-128">Auf diese Weise können Sie schnell erkennen, welche Teile der Abfrage am meisten (und am wenigsten) effektiv sind.</span><span class="sxs-lookup"><span data-stu-id="56448-128">This can help you quickly identify which parts of the query are the most (and least) effective.</span></span> 

<span data-ttu-id="56448-129">Die folgenden Informationen werden in der Ansicht **Abfragen** angezeigt:</span><span class="sxs-lookup"><span data-stu-id="56448-129">The following information is displayed in the **Queries** view:</span></span>

 - <span data-ttu-id="56448-130">**Speicherorttyp** – der Typ des Inhaltsspeicherorts für die in der Zeile angezeigten Statistiken.</span><span class="sxs-lookup"><span data-stu-id="56448-130">**Location type** - The type of content location for the statistics displayed in the row.</span></span>

- <span data-ttu-id="56448-131">**Teil-in** dieser Spalte wird einer der folgenden Werte angezeigt: **Primary** oder **Keyword**.</span><span class="sxs-lookup"><span data-stu-id="56448-131">**Part** - This column will display one of the following values: **Primary** or **Keyword**.</span></span> <span data-ttu-id="56448-132">**Primary** bedeutet, dass die Zeile Statistiken über die gesamte Abfrage darstellt. **Stichwort** : die Statistiken in der Zeile gelten für eine der Abfragekomponenten.</span><span class="sxs-lookup"><span data-stu-id="56448-132">**Primary** means the row presents statistics on the entire query; **Keyword** means the statistics in the row are for one of the query components.</span></span>

- <span data-ttu-id="56448-133">**Condition** – die tatsächliche Abfragekomponente der Suchabfrage, auf die sich die Zeile bezieht.</span><span class="sxs-lookup"><span data-stu-id="56448-133">**Condition** - The actual query component of the search query the row refers to.</span></span> <span data-ttu-id="56448-134">Wenn der Wert in der Spalte **Teilen** **primär**ist, werden die Statistiken für die gesamte Suchabfrage angezeigt; Wenn der Wert **Schlüsselwort**ist, wird die Statistik für die Komponente der Abfrage angezeigt, die in der Spalte **Abfrage** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="56448-134">If the value in the **Part** column is **Primary**, then the statistics for the entire search query are displayed; if the value is **Keyword**, then the statistics for the component of the query shown in the **Query** column are displayed.</span></span> <span data-ttu-id="56448-135">Wenn beispielsweise die Stichwortliste verwendet wurde, wird die Statistik eines der Schlüsselwörter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="56448-135">For example, if the keyword list was used, then the statistics one of the keywords are displayed.</span></span>

  <span data-ttu-id="56448-136">Im folgenden finden Sie weitere Informationen zu den in der Spalte **Abfragen** angezeigten Statistiken:</span><span class="sxs-lookup"><span data-stu-id="56448-136">Here are some other things to know about the statistics displayed in the **Queries** column:</span></span>
  
  - <span data-ttu-id="56448-137">Wenn Sie nach allen Inhalten in Postfächern suchen (indem Sie keine Schlüsselwörter angeben), lautet die tatsächliche Abfrage **(Größe > = 0)** , sodass alle Elemente zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="56448-137">When you search for all content in mailboxes (by not specifying any keywords), the actual query is **(size >= 0)** so that all items are returned</span></span>
  
  - <span data-ttu-id="56448-138">Beim Durchsuchen von SharePoint-und OneDrive-Websites werden der Suchabfrage die beiden folgenden Komponenten hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="56448-138">When you search SharePoint and OneDrive sites, the two following components are added to the search query:</span></span>
    
    <span data-ttu-id="56448-139">**Nicht IsExternalContent: 1** -Dies schließt Inhalte aus einer lokalen SharePoint-Organisation aus.</span><span class="sxs-lookup"><span data-stu-id="56448-139">**NOT IsExternalContent:1** - This excludes any content from an on-premises SharePoint organization</span></span>
    
    <span data-ttu-id="56448-140">**Nicht isOneNotePage: 1** -Dies schließt alle OneNote-Dateien aus, da es sich dabei um Duplikate eines Dokuments handeln würde, das mit der Suchabfrage übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="56448-140">**NOT isOneNotePage:1** - This excludes all OneNote files because these would be duplicates of any document that matches the search query.</span></span>

- <span data-ttu-id="56448-141">**Standorte in der Suche** Die Anzahl der inhaltsspeicherorte mit Elementen, die mit der Suchabfrage für die in der Zeile angezeigte Komponente/Bedingung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="56448-141">**Locations in search** The number of content locations that had items that matched the search query for the part/condition displayed in the row.</span></span> <span data-ttu-id="56448-142">Beachten Sie, dass Archivpostfächer als separater Speicherort gezählt werden, wenn Sie Elemente enthalten, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="56448-142">Note that archive mailboxes are counted as a separate location if they contain items that match the search criteria.</span></span>

- <span data-ttu-id="56448-143">**Items** – die Gesamtzahl der Elemente, die mit den Suchkriterien für die in der Zeile angezeigte Komponente/Bedingung übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="56448-143">**Items** - The total number of items that matched the search criteria for the part/condition displayed in the row.</span></span>

- <span data-ttu-id="56448-144">**Size** – die Gesamtzahl der Elemente, die mit den Suchkriterien für die in der Zeile angezeigte Komponente/Bedingung übereinstimmten.</span><span class="sxs-lookup"><span data-stu-id="56448-144">**Size** - The total number of items that matched the search criteria for the part/condition displayed in the row.</span></span>