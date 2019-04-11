---
title: Suchen nach Daten in einer Untersuchung
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
ms.openlocfilehash: 5f52f26c4443addd0e108794e1d3635a9b8efb98
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030154"
---
# <a name="search-for-data-in-an-investigation"></a><span data-ttu-id="833fe-102">Suchen nach Daten in einer Untersuchung</span><span class="sxs-lookup"><span data-stu-id="833fe-102">Search for data in an investigation</span></span>

<span data-ttu-id="833fe-103">Auf der Registerkarte **Suche** in einer Daten Untersuchung können Sie mithilfe von Schlüsselwörtern und Bedingungen nach verlegten, vertraulichen oder vertraulichen Daten in Inhaltsspeicherorten in Office 365 suchen.</span><span class="sxs-lookup"><span data-stu-id="833fe-103">On the **Search** tab in a data investigation, you can search for misplaced, confidential, or sensitive data in content locations in Office 365 using keywords and conditions.</span></span> 

<span data-ttu-id="833fe-104">Nachdem Sie eine Suche ausgeführt haben, können Sie Statistiken zu den von der Suche zurückgegebenen Elementen anzeigen, beispielsweise die inhaltsspeicherorte mit den meisten Elementen, die mit der Suchabfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="833fe-104">After you run a search, you can view statistics on the items returned by the search, such as the content locations that had the most items that matched the search query.</span></span> <span data-ttu-id="833fe-105">Sie können auch eine Vorschau einer Teilmenge der Ergebnisse anzeigen.</span><span class="sxs-lookup"><span data-stu-id="833fe-105">You can also preview a subset of the results.</span></span> <span data-ttu-id="833fe-106">Nachdem Sie die Dokumente identifiziert haben, die Sie weiter untersuchen möchten, können Sie die Ergebnisse der Suche einem Beweissatz hinzufügen, der für weitere Prozesse und Analysen festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="833fe-106">After you've identified the set of documents that want to further investigate, you can add the results of the search to an evidence set to further process and analyze.</span></span>

## <a name="create-a-search"></a><span data-ttu-id="833fe-107">Create a search</span><span class="sxs-lookup"><span data-stu-id="833fe-107">Create a search</span></span>

1. <span data-ttu-id="833fe-108">Klicken Sie in einer Untersuchung auf die Registerkarte **Suchvorgänge** , und klicken Sie dann auf **neue Suche**.</span><span class="sxs-lookup"><span data-stu-id="833fe-108">In an investigation, click the **Searches** tab, and then click **New search**.</span></span> 

    <span data-ttu-id="833fe-109">Ein Assistent wird angezeigt, in dem Sie durch den Prozess der Erstellung einer Suche geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="833fe-109">A wizard is displayed that will guide you through the process of creating a search.</span></span>

2. <span data-ttu-id="833fe-110">Geben Sie einen Such Namen und eine optionale Beschreibung für die Suche ein.</span><span class="sxs-lookup"><span data-stu-id="833fe-110">Enter a search name and an optional description for the search.</span></span>

3. <span data-ttu-id="833fe-111">Definieren Sie Ihre Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="833fe-111">Define your search criteria.</span></span> <span data-ttu-id="833fe-112">Sie können Bedingungen für die Suche hinzufügen, indem Sie die vordefinierten Bedingungs Karten verwenden oder Sucheigenschaften Namen in der Stichwortabfrage verwenden.</span><span class="sxs-lookup"><span data-stu-id="833fe-112">You can add conditions for the search by using the pre-built condition cards or by using search property names in the keyword query.</span></span> <span data-ttu-id="833fe-113">Weitere Informationen finden Sie unter [Erstellen von Suchabfragen](build-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="833fe-113">For more information, see [Build search queries](build-search-queries.md).</span></span>

4. <span data-ttu-id="833fe-114">Wählen Sie die zu durchsuchenden inhaltsspeicherorte (Datenquellen) aus.</span><span class="sxs-lookup"><span data-stu-id="833fe-114">Choose the content locations (data sources) to search.</span></span> <span data-ttu-id="833fe-115">Sie können die Suche Bereich, indem Sie die inhaltsspeicherorte bestimmter Personen von Interesse (wenn Sie die Untersuchung hinzugefügt haben).</span><span class="sxs-lookup"><span data-stu-id="833fe-115">You can scope the search by selecting the content locations of specific people of interest (if you added any to the investigation).</span></span> <span data-ttu-id="833fe-116">Wenn Sie Personen, die für die Untersuchung von Interesse sind, hinzugefügt haben, können Sie Sie hinzufügen, indem Sie die Schritte unter [Verwalten von Personen von Interesse](manage-people-of-interest.md#add-people-of-interest)ausführen.</span><span class="sxs-lookup"><span data-stu-id="833fe-116">If you have added people of interest to the investigation, you can add them by following the steps in [Manage people of interest](manage-people-of-interest.md#add-people-of-interest).</span></span>
 
    <span data-ttu-id="833fe-117">In einigen Fällen müssen Sie möglicherweise zuerst alle inhaltsspeicherorte in Ihrer Organisation durchsuchen. Alternativ können Sie Speicherorte suchen, die nicht einer bestimmten Person gehören.</span><span class="sxs-lookup"><span data-stu-id="833fe-117">In some cases, you may first need to search all content locations in your organization; alternatively, you may need to search locations that aren't owned by a specific person.</span></span> <span data-ttu-id="833fe-118">In diesen Szenarien können Sie entweder Ihre gesamte Organisation oder alle Standorte für einen bestimmten Office 365-Dienst (beispielsweise Exchange, SharePoint, OneDrive oder Teams) durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="833fe-118">In this scenarios, you can choose to search your entire organization, or all locations for a specific Office 365 services (such as Exchange, SharePoint, OneDrive of Business, or Teams.</span></span>

5. <span data-ttu-id="833fe-119">Speichern Sie die Suche, und führen Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="833fe-119">Save and run the search.</span></span>

<span data-ttu-id="833fe-120">Nachdem die Suche erstellt wurde, wird eine Flyout-Seite mit Details zur Suche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="833fe-120">After the search is created, a flyout page is displayed with details about the search.</span></span> <span data-ttu-id="833fe-121">Beachten Sie, dass die Schaltflächen **Statistiken** und **Vorschau** anfänglich abgeblendet sind, da die Suche nicht abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="833fe-121">Note that the **Statistics** and **Preview** buttons are initially grayed out because the search hasn't completed.</span></span> <span data-ttu-id="833fe-122">Sie können den Fortschritt verfolgen, indem Sie die Spalte **Status** auf der Registerkarte **Suchen** überwachen.</span><span class="sxs-lookup"><span data-stu-id="833fe-122">You can keep track of the progress of by monitoring the **Status** column on the **Searches** tab.</span></span>

## <a name="view-statistics-and-search-results"></a><span data-ttu-id="833fe-123">Anzeigen von Statistiken und Suchergebnissen</span><span class="sxs-lookup"><span data-stu-id="833fe-123">View statistics and search results</span></span>

<span data-ttu-id="833fe-124">Nachdem Sie eine Daten Ermittlungs Suche erstellt und gestartet haben, verwendet das Tool die Suchkriterien (Suchabfrage und inhaltsspeicherorte), die Sie definiert haben, und durchsucht einen Index im Live-Dienst nach Elementen, die Ihren Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="833fe-124">After you create and start a data investigation search, the tool uses the search criteria (the search query and content locations) that you defined and searches an index in the live service for items that match your search criteria.</span></span> <span data-ttu-id="833fe-125">Es gibt drei Komponenten einer Suche, die zurückgegeben werden, wenn die Suche abgeschlossen ist:</span><span class="sxs-lookup"><span data-stu-id="833fe-125">There are three components of a search that are returned when the search is complete:</span></span> 

- <span data-ttu-id="833fe-126">**Estimate** -da die Suche nur einen Index durchsucht (statt der tatsächlichen inhaltsspeicherorte), sind die Ergebnisse einer Suche eine Schätzung (basierend auf dem, was im Index gefunden wurde, der mit den Suchergebnissen übereinstimmt).</span><span class="sxs-lookup"><span data-stu-id="833fe-126">**Estimate** - Because the search only searches an index (rather than the actual content locations), the results of a search are an estimate (based on what was found in the index that matched the search results).</span></span> <span data-ttu-id="833fe-127">Eine Zusammenfassung der Schätzung wird auf der Such Flyout-Seite unter **Status**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="833fe-127">A summary of the estimate is displayed on the search flyout page under **Status**.</span></span> <span data-ttu-id="833fe-128">Beachten Sie, dass der Status des Vorkalkulations Prozesses für eine Suche auf der Registerkarte **Suchvorgänge** in der Spalte **Estimate Status** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="833fe-128">Note that the status for the estimate process for a search is displayed on the **Searches** tab in the **Estimate status** column.</span></span> <span data-ttu-id="833fe-129">Wenn die Such Schätzung abgeschlossen ist, wird dieser Status auf **erfolgreich**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="833fe-129">When the search estimate is complete, this status is set to **Successful**.</span></span>

- <span data-ttu-id="833fe-130">**Statistics** -Statistics liefert detailliertere Informationen zu den Suchergebnissen.</span><span class="sxs-lookup"><span data-stu-id="833fe-130">**Statistics** - Statistics provide more detailed information about the search results.</span></span> <span data-ttu-id="833fe-131">Dazu gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="833fe-131">This includes the following:</span></span>

    - <span data-ttu-id="833fe-132">Zusammenfassung-Statistiken ähnlich wie die Suchergebnisse, die auf der Seite Flyout angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="833fe-132">Summary - Statistics similar to the search estimate results displayed on the flyout page.</span></span>
    - <span data-ttu-id="833fe-133">Top Locations-Statistiken über die Anzahl der Elemente, die mit der Suchabfrage an den einzelnen Inhaltsverzeichnissen übereinstimmen, die durchsucht wurden.</span><span class="sxs-lookup"><span data-stu-id="833fe-133">Top locations - Statistics about the number of items that match the search query in each content location that was searched.</span></span> 
    - <span data-ttu-id="833fe-134">Abfragen-detaillierte Statistiken über die Suchabfrage, einschließlich der Anzahl der Elemente, die mit jeder Bedingung in einer Suchabfrage übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="833fe-134">Queries - Detailed statistics about the search query, including the number of items that match each condition in a search query.</span></span>

    <span data-ttu-id="833fe-135">Klicken Sie auf der Seite Flyout auf **Statistiken** , um diese Statistiken anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="833fe-135">Click **Statistics** on the flyout page to view these statistics.</span></span> <span data-ttu-id="833fe-136">Beachten Sie, dass diese Schaltfläche inaktiv ist, bis der Wert des vorKalkulations **Status** auf der Registerkarte **Suchen** auf **erfolgreich**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="833fe-136">Note that this button is inactive until the value of the **Estimate status** on the **Searches** tab is set to **Successful**.</span></span> <span data-ttu-id="833fe-137">Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistiken](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="833fe-137">For more information about search statistics, see [Search statistics](search-statistics.md).</span></span>

- <span data-ttu-id="833fe-138">**Preview** -wenn die Suche abgeschlossen ist, können Sie die tatsächlichen Elemente aus einer Beispiel Teilmenge der Suchergebnisse anzeigen, die von der Suche zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="833fe-138">**Preview** - When the search is complete, you can view the actual items from a sample subset of the search results returned by the search.</span></span> <span data-ttu-id="833fe-139">In der systemeigenen Ansicht des Elementtyps können Sie auch die Metadaten zu dem Element anzeigen.</span><span class="sxs-lookup"><span data-stu-id="833fe-139">YOu can view in the native view of the item type, any you can also view metadata about the item.</span></span> <span data-ttu-id="833fe-140">Auf diese Weise können Sie schnell feststellen, ob Ihre Suchergebnisse Ihren Erwartungen entsprechen oder ob Sie die Suche bearbeiten und erneut ausführen müssen.</span><span class="sxs-lookup"><span data-stu-id="833fe-140">This is a good way to quickly determine if your search results are what you expected or if you need to edit the search and re-run it.</span></span> <span data-ttu-id="833fe-141">Klicken Sie auf der Flyout-Seite auf **Vorschau** , um Elemente aus den Suchergebnissen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="833fe-141">Click  **Preview** on the flyout page to view items from the search results.</span></span> <span data-ttu-id="833fe-142">Beachten Sie, dass diese Schaltfläche inaktiv ist, bis der Wert des **Vorschaustatus** auf der Registerkarte **Suchvorgänge** auf **erfolgreich**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="833fe-142">Note that this button is inactive until the value of the **Preview status** on the **Searches** tab is set to **Successful**.</span></span>
 
> [!NOTE]
> <span data-ttu-id="833fe-143">Die Statuswerte für die Spalten " **Estimate Status** " und " **Preview Status** " auf der Registerkarte " **Suchen** " werden **in Bearbeitung**und **erfolgreich**über **mittelt**.</span><span class="sxs-lookup"><span data-stu-id="833fe-143">The status values for the **Estimate status** and **Preview status** columns on the **Searches** tab are **Submitted**, **In progress**, and **Successful**.</span></span> <span data-ttu-id="833fe-144">Wenn bei der Suche ein Fehler auftritt, wird der Status **fehlgeschlagen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="833fe-144">If there is an error with the search, the status of **Failed** is displayed.</span></span>

## <a name="add-search-results-to-evidence"></a><span data-ttu-id="833fe-145">Hinzufügen von Suchergebnissen zu beweisen</span><span class="sxs-lookup"><span data-stu-id="833fe-145">Add search results to evidence</span></span>

<span data-ttu-id="833fe-146">Wenn Sie mit den Ergebnissen einer Suche zufrieden sind und Sie bereit sind, diese Suchergebnisse zu analysieren und zu beheben, können Sie Sie zu einem Evidence-Satz in der Untersuchung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="833fe-146">When you're satisfied with the results of a search and you're ready to analyze and remediate those search results, you can add them to an evidence set in the investigation.</span></span> <span data-ttu-id="833fe-147">Wenn Sie einem Evidence-Satz auf der Registerkarte **Evidence** Elemente hinzufügen, werden die folgenden beiden Schritte ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="833fe-147">When you add items to an evidence set on the **Evidence** tab, the following two things occur:</span></span>

- <span data-ttu-id="833fe-148">Alle Elemente in den Suchergebnissen werden aus der Datenquelle im Live-Dienst kopiert und an einen sicheren Azure-Speicherort in der Microsoft-Cloud kopiert.</span><span class="sxs-lookup"><span data-stu-id="833fe-148">All items in the search results are copied from the data source in the live service, and copied to a secure Azure storage location in the Microsoft cloud.</span></span>

- <span data-ttu-id="833fe-149">Alle Elemente (einschließlich des Inhalts und der Metadaten) werden neu indiziert, sodass alle Daten im Evidence-Satz während der Untersuchung vollständig durchsuchbar sind.</span><span class="sxs-lookup"><span data-stu-id="833fe-149">All items (including the content and metadata) are re-indexed so that all data in the evidence set is fully searchable during your investigation.</span></span> <span data-ttu-id="833fe-150">Das erneute Indizieren der Daten führt zu gründlichen und sehr schnellen Suchvorgängen, wenn Sie die Daten in dem bei der Untersuchung festgelegten Nachweis durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="833fe-150">Re-indexing the data results in thorough and very fast searches when you search the data in the evidence set during your investigation.</span></span>

<span data-ttu-id="833fe-151">Ein Vorteil des Kopierens der Live-Daten in einen in Azure festgelegten Nachweis besteht darin, dass Sie bei zeitabhängigen oder kritischen Vorfällen schnell den Schaden enthalten können, indem Sie sofort verdächtige Inhalte in der ursprünglichen Datenquelle im Live-Dienst löschen und dann der Vorfall durch Analysieren der Beweise, die in die isolierte Umgebung des Azure-Speicherorts kopiert wurden.</span><span class="sxs-lookup"><span data-stu-id="833fe-151">One advantage of copying the live data to an evidence set in Azure is that for time-sensitive or critical incidents, you can quickly contain the damage by immediately deleting suspicious content in the original data source in the live service and then investigating the incident by analyzing the evidence that was copied to the quarantined environment of the Azure storage location.</span></span> 

<span data-ttu-id="833fe-152">Das Kopieren der ursprünglichen Daten in den Evidence-Satz erleichtert auch die Untersuchung, indem Sie erweiterte Analysetools wie die Erkennung von Designs, die Erkennung nahezu doppelter Informationen und die Identifizierung von e-Mail-Threads bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="833fe-152">Copying the original data to the evidence set also facilitates your investigation by providing you with advanced analytics tools such as themes detection, near-duplicate detection, and email thread identification.</span></span>

<span data-ttu-id="833fe-153">Bei Bedarf können Sie auch Daten aus nicht-Office 365-Datenquellen zu einem Evidence-Satz hinzufügen, damit diese zusammen mit den von Office 365 gesammelten Daten gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="833fe-153">If necessary, you can also add data from non-Office 365 data sources to an evidence set so that it's stored along with the data you collect from Office 365.</span></span>

<span data-ttu-id="833fe-154">Wenn Sie einer festgelegten Gruppe Daten hinzufügen möchten, wählen Sie auf der Registerkarte **Suchvorgänge** eine Suche aus, und klicken Sie dann auf der Seite Flyout auf **Ergebnisse zu beweisen** .</span><span class="sxs-lookup"><span data-stu-id="833fe-154">To add data to an an evidenced set, select a search on the **Searches** tab, and then clicking **Add results to evidence** on the flyout page.</span></span> <span data-ttu-id="833fe-155">Beachten Sie, dass Sie einem vorhandenen Evidence-Satz Daten hinzufügen oder einen neuen Evidence-Satz erstellen können.</span><span class="sxs-lookup"><span data-stu-id="833fe-155">Note that you can add data to an existing evidence set or create a new evidence set on the fly.</span></span>

### <a name="tracking-the-progress-of-adding-search-results-to-evidence"></a><span data-ttu-id="833fe-156">NachVerfolgen des Fortschritts des Hinzufügens von Suchergebnissen zu beweisen</span><span class="sxs-lookup"><span data-stu-id="833fe-156">Tracking the progress of adding search results to evidence</span></span>

<span data-ttu-id="833fe-157">Das Hinzufügen von Daten zu einem Beweissatz ist ein langwieriger Prozess.</span><span class="sxs-lookup"><span data-stu-id="833fe-157">Adding data to an evidence set is a long-running process.</span></span> <span data-ttu-id="833fe-158">Der Prozess umfasst das Sammeln der Elemente, die die ursprüngliche Datenquelle aus Office 365 (beispielsweise von Postfächern und Websites), kopieren Sie Sie in den Azure-Speicherort (dieser Kopiervorgang wird auch als *Einnahme*), und dann die Elemente erneut indizieren.</span><span class="sxs-lookup"><span data-stu-id="833fe-158">The process includes collecting the items the original data source from Office 365 ( for example, from mailboxes and sites), copying them to the Azure storage location (this copying process is also called *ingestion*), and then re-indexing the items.</span></span> <span data-ttu-id="833fe-159">Sie können den Fortschritt entweder auf der Registerkarte **Aufträge** oder auf der Registerkarte **Suchvorgänge** in der Spalte **hinzugefügte Daten nach** verfolgen.</span><span class="sxs-lookup"><span data-stu-id="833fe-159">You can either track the progress on the **Jobs** tab or on the **Searches** tab in the **Added data to evidence** column.</span></span> <span data-ttu-id="833fe-160">Nachdem die Verarbeitung der Beweis Verarbeitung abgeschlossen ist, können Sie zur Registerkarte **Beweise** wechseln, auf den nachweissatz klicken und dann die Untersuchung starten, indem Sie die relevanten Daten nach Bedarf durchsuchen, überprüfen, Tagging und exportieren.</span><span class="sxs-lookup"><span data-stu-id="833fe-160">After the processing of evidence processing is completed, you can go to the **Evidence** tab, click the evidence set, and then start your investigation by searching, reviewing, tagging, and exporting the relevant data as necessary.</span></span>