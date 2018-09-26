---
title: Suchen Sie das Überwachungsprotokoll für Benutzer- und Admin-Aktivität in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: 'Das Überwachungsprotokoll Office 365 ist ein unified Überwachungsprotokoll. Warum einer einheitlichen Audit protokolliert? Da Ereignisse aus, dass Sie die Organisation sind die meisten Office 365-Dienste abonniert werden in einer einzelnen Überwachungsprotokoll aufgezeichnet, die durchsucht werden. Dies bedeutet, dass Sie für Benutzer und Admin-Aktivität in diese Dienste suchen können:'
ms.openlocfilehash: 230502f331babeef8f89eacce0d19a7756cb96fc
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038028"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="2a1a0-106">Suchen Sie das Überwachungsprotokoll für Benutzer- und Admin-Aktivität in Office 365</span><span class="sxs-lookup"><span data-stu-id="2a1a0-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="2a1a0-p102">Das Überwachungsprotokoll Office 365 ist ein unified Überwachungsprotokoll. Warum einer einheitlichen Audit protokolliert? Da Ereignisse aus, dass Sie die Organisation sind die meisten Office 365-Dienste abonniert werden in einer einzelnen Überwachungsprotokoll aufgezeichnet, die durchsucht werden. Dies bedeutet, dass Sie für Benutzer und Admin-Aktivität in diese Dienste suchen können:</span><span class="sxs-lookup"><span data-stu-id="2a1a0-p102">The Office 365 audit log is a unified audit log. Why a unified audit log? Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search. That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="2a1a0-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="2a1a0-111">SharePoint</span></span>
- <span data-ttu-id="2a1a0-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="2a1a0-112">OneDrive</span></span>
- <span data-ttu-id="2a1a0-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="2a1a0-113">Exchange</span></span>
- <span data-ttu-id="2a1a0-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a1a0-114">Azure Active Directory</span></span>
- <span data-ttu-id="2a1a0-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2a1a0-115">Microsoft Teams</span></span>
- <span data-ttu-id="2a1a0-116">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="2a1a0-116">eDiscovery</span></span>
- <span data-ttu-id="2a1a0-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="2a1a0-117">Power BI</span></span>
- <span data-ttu-id="2a1a0-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="2a1a0-118">Yammer</span></span>
- <span data-ttu-id="2a1a0-119">Sway</span><span class="sxs-lookup"><span data-stu-id="2a1a0-119">Sway</span></span>
- <span data-ttu-id="2a1a0-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="2a1a0-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="2a1a0-121">Einrichten der Überwachung</span><span class="sxs-lookup"><span data-stu-id="2a1a0-121">Set up auditing</span></span>
  
<span data-ttu-id="2a1a0-122">Es gibt einige Dinge, die Sie tun, bevor das Office 365-Überwachungsprotokoll durchsucht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2a1a0-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="2a1a0-123">[Aktivieren der Suche für Audit Log](turn-audit-log-search-on-or-off.md) Aufzeichnen von Ereignissen zu starten, denen Sie für suchen können</span><span class="sxs-lookup"><span data-stu-id="2a1a0-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="2a1a0-124">[Aktivieren der Überwachung von Postfächern](enable-mailbox-auditing.md) , damit Sie für Ereignisse im Zusammenhang mit dem Postfach suchen können; beispielsweise wenn ein Benutzer auf ihre Postfach oder Benutzerkontenverwaltung Elemente aus ihren Ordner "wiederherstellbare Elemente" anmeldet</span><span class="sxs-lookup"><span data-stu-id="2a1a0-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="2a1a0-125">Durchsuchen des Überwachungsprotokolls</span><span class="sxs-lookup"><span data-stu-id="2a1a0-125">Search the audit log</span></span>
  
<span data-ttu-id="2a1a0-126">Nachdem Sie die Überwachung einzuschalten, suchen Sie nach Hunderten von einzelnen Arten von Ereignissen aus mehreren Office 365-Dienste.</span><span class="sxs-lookup"><span data-stu-id="2a1a0-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="2a1a0-127">[Suchen Sie das Überwachungsprotokoll](search-the-audit-log-in-security-and-compliance.md) für Benutzer- und Admin-Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="2a1a0-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="2a1a0-128">[Verstehen die Detailangaben zu den Eigenschaften](detailed-properties-in-the-office-365-audit-log.md) in jedem auditing Datensatz in den Suchergebnissen enthalten</span><span class="sxs-lookup"><span data-stu-id="2a1a0-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="2a1a0-129">[Suchen nach eDiscovery-bezogene Aktivitäten](search-for-ediscovery-activities-in-the-audit-log.md) , die von Administratoren und Compliance-Manager durchgeführt</span><span class="sxs-lookup"><span data-stu-id="2a1a0-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
