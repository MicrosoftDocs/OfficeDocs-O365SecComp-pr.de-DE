---
title: Anzeigen der Bezeichnungsnutzung mit der Analyse der Bezeichnungen
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Nachdem Sie Ihre Aufbewahrungsbezeichnungen und Vertraulichkeitsbezeichnungen erstellt haben, können Sie überprüfen, wie sie mandantenübergreifend verwendet werden. Mithilfe der Analyse der Bezeichnungen im Microsoft 365 Compliance Center und Microsoft 365 Security Center können Sie schnell sehen, welche Bezeichnungen am häufigsten verwendet werden und wo sie angewendet werden.
ms.openlocfilehash: d0289eb79dca04262ef61d58a8e622ae6d7cbe93
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254558"
---
# <a name="view-label-usage-with-label-analytics"></a><span data-ttu-id="00420-104">Anzeigen der Bezeichnungsnutzung mit der Analyse der Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="00420-104">View label usage with label analytics</span></span>

<span data-ttu-id="00420-105">Nachdem Sie Ihre Aufbewahrungsbezeichnungen und Vertraulichkeitsbezeichnungen erstellt haben, können Sie überprüfen, wie sie mandantenübergreifend verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="00420-105">After you create your retention labels and sensitivity labels, you’ll want to see how they’re being used across your tenant.</span></span> <span data-ttu-id="00420-106">Mithilfe der Analyse der Bezeichnungen im Microsoft 365 Compliance Center und Microsoft 365 Security Center können Sie schnell sehen, welche Bezeichnungen am häufigsten verwendet werden und wo sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="00420-106">With label analytics in the Microsoft 365 compliance center and Microsoft 365 security center, you can quickly see which labels are used the most and where they’re being applied.</span></span>

<span data-ttu-id="00420-107">Mit der Analyse der Bezeichnungen können Sie beispielsweise Folgendes anzeigen:</span><span class="sxs-lookup"><span data-stu-id="00420-107">For example, with label analytics, you can view the:</span></span>

- <span data-ttu-id="00420-108">Gesamtzahl der Aufbewahrungsbezeichnungen und Vertraulichkeitsbezeichnungen, die auf Inhalte angewandt wurden.</span><span class="sxs-lookup"><span data-stu-id="00420-108">Total number of retention labels and sensitivity labels applied to content.</span></span>
- <span data-ttu-id="00420-109">Topbezeichnungen und die Anzahl der Anwendungen jeder Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="00420-109">Top labels and the count of how many times each label was applied.</span></span>
- <span data-ttu-id="00420-110">Stellen, an denen Bezeichnungen angewendet werden, und die Anzahl jeder Stelle.</span><span class="sxs-lookup"><span data-stu-id="00420-110">Locations where labels are applied and the count for each location.</span></span>
- <span data-ttu-id="00420-111">Anzahl der Dateien und Ordner, bei denen die Aufbewahrungsbezeichnung geändert oder entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="00420-111">Count for how many files and folders had their retention label changed or removed.</span></span>

<span data-ttu-id="00420-112">Sie finden die Analyse der Bezeichnungen im [Microsoft 365 Compliance Center](https://compliance.microsoft.com/labelanalytics) oder [Microsoft 365 Security Center](https://security.microsoft.com/labelanalytics) > **Klassifizierung** > **Analyse der Bezeichnungen**.</span><span class="sxs-lookup"><span data-stu-id="00420-112">You can find label analytics in the [Microsoft 365 compliance center](https://compliance.microsoft.com/labelanalytics) or [Microsoft 365 security center](https://security.microsoft.com/labelanalytics) > **Classification** > **Label analytics**.</span></span>

![Seite zur Analyse der Bezeichnungen](media/label-analytics-page.png)

## <a name="sensitivity-label-usage"></a><span data-ttu-id="00420-114">Vertraulichkeitsbezeichnungsnutzung</span><span class="sxs-lookup"><span data-stu-id="00420-114">Sensitivity label usage</span></span>

<span data-ttu-id="00420-115">Die Daten zur Verwendung der Vertraulichkeitsbezeichnung werden aus den Berichten für Azure Information Protection abgerufen. Weitere Informationen hierzu finden Sie unter [Zentrale Berichterstellung für Azure Information Protection](https://docs.microsoft.com/de-DE/azure/information-protection/reports-aip).</span><span class="sxs-lookup"><span data-stu-id="00420-115">The data on sensitivity label usage is pulled from the reports for Azure Information Protection – for more information, see [Central reporting for Azure Information Protection](https://docs.microsoft.com/de-DE/azure/information-protection/reports-aip).</span></span>

<span data-ttu-id="00420-116">Beachten Sie, dass für die Azure Information Protection-Berichte [Voraussetzungen](https://docs.microsoft.com/de-DE/azure/information-protection/reports-aip#prerequisites-for-azure-information-protection-analytics) gelten, die auch für die Analyse der Bezeichnungen im Hinblick auf Vertraulichkeitsbezeichnungen im Microsoft 365 Compliance Center und Microsoft 365 Security Center gelten.</span><span class="sxs-lookup"><span data-stu-id="00420-116">Note that the Azure Information Protection reports have [prerequisites](https://docs.microsoft.com/de-DE/azure/information-protection/reports-aip#prerequisites-for-azure-information-protection-analytics) that also apply to label analytics on sensitivity labels in the Microsoft 365 compliance center and Microsoft 365 security center.</span></span> <span data-ttu-id="00420-117">Sie benötigen z. B. ein Azure-Abonnement, das die Protokollanalyse enthält, da diese Berichte durch das Senden von Informationen zu Überwachungsereignissen von Azure Information Protection-Clients und -Scannern an einen zentralen Speicherort basierend auf dem Azure Log Analytics-Dienst entstehen.</span><span class="sxs-lookup"><span data-stu-id="00420-117">For example, you need an Azure subscription that includes the Log Analytics because these reports are a result of sending information protection audit events from Azure Information Protection clients and scanners to a centralized location based on Azure Log Analytics service.</span></span>

<span data-ttu-id="00420-118">Für die Vertraulichkeitsbezeichnungsnutzung:</span><span class="sxs-lookup"><span data-stu-id="00420-118">For sensitivity label usage:</span></span>

- <span data-ttu-id="00420-119">Es gibt keine Latenz in den Daten.</span><span class="sxs-lookup"><span data-stu-id="00420-119">There is no latency in the data.</span></span> <span data-ttu-id="00420-120">Dies ist ein Echtzeitbericht.</span><span class="sxs-lookup"><span data-stu-id="00420-120">This is a real-time report.</span></span>
- <span data-ttu-id="00420-121">Wenn Sie die Anzahl für jede Topbezeichnung anzeigen möchten, zeigen Sie auf das Balkendiagramm und lesen Sie die QuickInfo, die angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="00420-121">To see the count for each top label, point to the bar graph and read the tool tip that appears.</span></span>
- <span data-ttu-id="00420-122">Der Bericht zeigt, wo Vertraulichkeitsbezeichnungen pro App angewendet werden (während Aufbewahrungsbezeichnungen pro Standort angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="00420-122">The report shows where sensitivity labels are applied per app (whereas retention labels are shown per location).</span></span>

![Bericht zur Vertraulichkeitsbezeichnungsnutzung](media/sensitivity-label-usage-report.png)

## <a name="retention-label-usage"></a><span data-ttu-id="00420-124">Aufbewahrungsbezeichnungsnutzung</span><span class="sxs-lookup"><span data-stu-id="00420-124">Retention label usage</span></span>

<span data-ttu-id="00420-125">Dieser Bericht zeigt einen schnellen Überblick über die Topbezeichnungen und darüber, wo sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="00420-125">This report shows a quick view of what the top labels are and where they’re applied.</span></span> <span data-ttu-id="00420-126">Weitere Informationen zur Bezeichnung von Inhalten in SharePoint und OneDrive finden Sie unter [Anzeigen der Bezeichnungsaktivität für Dokumente](view-label-activity-for-documents.md).</span><span class="sxs-lookup"><span data-stu-id="00420-126">For more detailed information on how content in SharePoint and OneDrive is labeled, see [View label activity for documents](view-label-activity-for-documents.md).</span></span>

<span data-ttu-id="00420-127">Für die Aufbewahrungsbezeichnungsnutzung:</span><span class="sxs-lookup"><span data-stu-id="00420-127">For retention label usage:</span></span>

- <span data-ttu-id="00420-128">Daten werden wöchentlich aggregiert, sodass es bis zu sieben Tage dauern kann, bis Daten im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="00420-128">Data is aggregated weekly, so it may take up to seven days for data to appear in the report.</span></span>
- <span data-ttu-id="00420-129">Wenn Sie die Anzahl für jede Topbezeichnung anzeigen möchten, zeigen Sie auf das Balkendiagramm und lesen Sie die QuickInfo, die angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="00420-129">To see the count for each top label, point to the bar graph and read the tool tip that appears.</span></span>
- <span data-ttu-id="00420-130">Der Bericht zeigt, wo Aufbewahrungsbezeichnungen pro Standort angewendet werden (während Vertraulichkeitsbezeichnungen pro Standort angezeigt werden).</span><span class="sxs-lookup"><span data-stu-id="00420-130">The report shows where retention labels are applied per location (whereas sensitivity labels are shown per app).</span></span>
- <span data-ttu-id="00420-131">Bei Aufbewahrungsbezeichnungen ist dies eine Zusammenfassung der Daten in Ihrem Mandanten. Es wird nicht nach einem bestimmten Datumsbereich gefiltert.</span><span class="sxs-lookup"><span data-stu-id="00420-131">For retention labels, this is a summary of the all-time data in your tenant; it’s not filtered to a specific date range.</span></span> <span data-ttu-id="00420-132">Im Gegensatz dazu zeigt der [Bezeichnungsaktivitäten-Explorer](view-label-activity-for-documents.md) nur Daten aus den letzten 30 Tagen.</span><span class="sxs-lookup"><span data-stu-id="00420-132">By contrast, the [Label Activity Explorer](view-label-activity-for-documents.md) shows data from only the past 30 days.</span></span>

![Nutzungsbericht für Aufbewahrungsbezeichnungen](media/retention-label-usage-report.png)

## <a name="view-all-content-with-a-specific-retention-label"></a><span data-ttu-id="00420-134">Anzeigen aller Inhalte mit einer bestimmten Aufbewahrungsbezeichnung</span><span class="sxs-lookup"><span data-stu-id="00420-134">View all content with a specific retention label</span></span>

<span data-ttu-id="00420-135">Im Nutzungsbericht für Aufbewahrungsbezeichnungen können Sie schnell alle Inhalte mit dieser Bezeichnung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="00420-135">From the retention label usage report, you can quickly explore all content with that label applied.</span></span> <span data-ttu-id="00420-136">(Beachten Sie, dass wir derzeit an diesem Feature arbeiten, damit weniger Schritte erforderlich sind, um alle beschrifteten Inhalte anzuzeigen.)</span><span class="sxs-lookup"><span data-stu-id="00420-136">(Note that we're currently working on this feature, so that it will take fewer steps to view all the labeled content.)</span></span>

<span data-ttu-id="00420-137">Wählen Sie zuerst **Details anzeigen** unten im Bericht aus.</span><span class="sxs-lookup"><span data-stu-id="00420-137">First, choose **View Details** at the bottom of the report.</span></span>

![Option „Details anzeigen“ unten im Nutzungsbericht für Aufbewahrungsbezeichnungen](media/retention-label-usage-view-details.png)

<span data-ttu-id="00420-139">Wählen Sie dann eine Aufbewahrungsbezeichnung > **Elemente erkunden** im rechten Bereich.</span><span class="sxs-lookup"><span data-stu-id="00420-139">Then choose a retention label > **Explore items** in the right pane.</span></span>

![Option „Elemente erkunden“ im rechten Bereich](media/retention-label-usage-explore-items.png)

<span data-ttu-id="00420-141">Für diese Bezeichnung können Sie die Registerkarte **Aktivität** auswählen, um die Anzahl der Elemente mit dieser Bezeichnung nach Standort anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="00420-141">For that label, you can choose the **Activity** tab to view a count of items with that label by location.</span></span>

![Registerkarte „Aktivität“ für eine Aufbewahrungsbezeichnung](media/retention-label-usage-activity-tab.png)

<span data-ttu-id="00420-143">Sie können auch die Registerkarte **Elemente mit dieser Bezeichnung** auswählen. Dann können Sie eine Aufschlüsselung bestimmter Standorte anzeigen:</span><span class="sxs-lookup"><span data-stu-id="00420-143">You can also choose the **Items with this label** tab. Then you can drill into specific locations:</span></span>

- <span data-ttu-id="00420-144">Bei Exchange Online sehen Sie eine Liste der Postfächer mit der Anzahl der bezeichneten Elemente in jedem Postfach.</span><span class="sxs-lookup"><span data-stu-id="00420-144">For Exchange Online, you see a list of mailboxes with the count of labeled items in each mailbox.</span></span>
- <span data-ttu-id="00420-145">Bei SharePoint Online und OneDrive for Business wird eine Liste der Websitesammlungen und OneDrive-Konten mit der Anzahl der bezeichneten Elemente an jedem Standort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00420-145">For SharePoint Online and OneDrive for Business, you see a list of site collections and OneDrive accounts with the count of labeled items in each location.</span></span>

<span data-ttu-id="00420-146">Wenn Sie ein Postfach oder eine Websitesammlung auswählen, können Sie eine Liste mit Elementen mit dieser Aufbewahrungsbezeichnung an diesem Standort anzeigen.</span><span class="sxs-lookup"><span data-stu-id="00420-146">When you choose a mailbox or site collection, you can view a list of items with that retention label in that location.</span></span>

![Elemente mit dieser Bezeichnungsregisterkarte, die alle Elemente mit dieser Aufbewahrungsbezeichnung anzeigt](media/retention-label-usage-content-explorer.png)

## <a name="permissions"></a><span data-ttu-id="00420-148">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="00420-148">Permissions</span></span>

<span data-ttu-id="00420-149">Wenn Sie die Analyse der Bezeichnungen anzeigen möchten, muss Ihnen eine der folgenden Rollen in Azure Active Directory zugewiesen sein:</span><span class="sxs-lookup"><span data-stu-id="00420-149">To view label analytics, you must be assigned one of the following roles in Azure Active Directory:</span></span>

- <span data-ttu-id="00420-150">Globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="00420-150">Global administrator</span></span>
- <span data-ttu-id="00420-151">Compliance-Administrator</span><span class="sxs-lookup"><span data-stu-id="00420-151">Compliance administrator</span></span>
- <span data-ttu-id="00420-152">Sicherheitsadministrator</span><span class="sxs-lookup"><span data-stu-id="00420-152">Security administrator</span></span>
- <span data-ttu-id="00420-153">Benutzer mit Leseberechtigung für Sicherheitsfunktionen</span><span class="sxs-lookup"><span data-stu-id="00420-153">Security reader</span></span>

<span data-ttu-id="00420-154">Beachten Sie außerdem, dass diese Berichte Azure Monitor verwenden, um die Daten in einem Protokollanalysearbeitsbereich Ihres Unternehmens zu speichern.</span><span class="sxs-lookup"><span data-stu-id="00420-154">In addition, note these reports use Azure Monitor to store the data in a Log Analytics workspace that your organization owns.</span></span> <span data-ttu-id="00420-155">Aus diesem Grund sollte der Benutzer als Benutzer mit Leseberechtigung zum Azure Monitoring-Arbeitsbereich hinzugefügt werden, der die Daten enthält. Weitere Informationen finden Sie unter [Erforderliche Berechtigungen für Azure Information Protection-Analysen](https://docs.microsoft.com/de-DE/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics).</span><span class="sxs-lookup"><span data-stu-id="00420-155">Therefore, the user should be added as a reader to the Azure Monitoring worksapce that holds the data - for more information, see [Permissions required for Azure Information Protection analytics](https://docs.microsoft.com/de-DE/azure/information-protection/reports-aip#permissions-required-for-azure-information-protection-analytics).</span></span>

