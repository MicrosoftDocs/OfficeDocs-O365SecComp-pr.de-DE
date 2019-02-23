---
title: Durchsuchen des Überwachungsprotokolls nach Benutzer- und Administratoraktivitäten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: 'Das Office 365-Überwachungsprotokoll ist ein einheitliches Überwachungsprotokoll. Warum ein einheitliches Überwachungsprotokoll? Da Ereignisse aus den meisten Office 365-Diensten, die Sie in der Organisation abonnieren, in einem einzigen Überwachungsprotokoll aufgezeichnet werden, das Sie durchsuchen können. Das führt dazu, dass Sie in diesen Diensten nach Benutzer-und Administratoraktivitäten suchen können:'
ms.openlocfilehash: ec67c63cff57f95bacabd120c466922870b595b4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214085"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="2a33d-106">Durchsuchen des Überwachungsprotokolls nach Benutzer- und Administratoraktivitäten in Office 365</span><span class="sxs-lookup"><span data-stu-id="2a33d-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="2a33d-p102">Das Office 365-Überwachungsprotokoll ist ein einheitliches Überwachungsprotokoll. Warum ein einheitliches Überwachungsprotokoll? Da Ereignisse aus den meisten Office 365-Diensten, die Sie in der Organisation abonnieren, in einem einzigen Überwachungsprotokoll aufgezeichnet werden, das Sie durchsuchen können. Das führt dazu, dass Sie in diesen Diensten nach Benutzer-und Administratoraktivitäten suchen können:</span><span class="sxs-lookup"><span data-stu-id="2a33d-p102">The Office 365 audit log is a unified audit log. Why a unified audit log? Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search. That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="2a33d-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="2a33d-111">SharePoint</span></span>
- <span data-ttu-id="2a33d-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="2a33d-112">OneDrive</span></span>
- <span data-ttu-id="2a33d-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="2a33d-113">Exchange</span></span>
- <span data-ttu-id="2a33d-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2a33d-114">Azure Active Directory</span></span>
- <span data-ttu-id="2a33d-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2a33d-115">Microsoft Teams</span></span>
- <span data-ttu-id="2a33d-116">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="2a33d-116">eDiscovery</span></span>
- <span data-ttu-id="2a33d-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="2a33d-117">Power BI</span></span>
- <span data-ttu-id="2a33d-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="2a33d-118">Yammer</span></span>
- <span data-ttu-id="2a33d-119">Sway</span><span class="sxs-lookup"><span data-stu-id="2a33d-119">Sway</span></span>
- <span data-ttu-id="2a33d-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="2a33d-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="2a33d-121">Einrichten der Überwachung</span><span class="sxs-lookup"><span data-stu-id="2a33d-121">Set up auditing</span></span>
  
<span data-ttu-id="2a33d-122">Es gibt einige Schritte, die Sie ausführen müssen, bevor Sie das Office 365-Überwachungsprotokoll durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="2a33d-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="2a33d-123">[Aktivieren Sie die Überwachungsprotokoll Suche](turn-audit-log-search-on-or-off.md) , um mit der Aufzeichnung von Ereignissen zu beginnen, nach denen Sie suchen können.</span><span class="sxs-lookup"><span data-stu-id="2a33d-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="2a33d-124">[Aktivieren Sie die postfachüberwachung](enable-mailbox-auditing.md) , um nach Post fachbezogenen Ereignissen zu suchen. beispielsweise wenn sich ein Benutzer bei seinem Postfach anmeldet oder Elemente aus seinem Ordner "Wiederherstellbare Elemente" löscht</span><span class="sxs-lookup"><span data-stu-id="2a33d-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="2a33d-125">Durchsuchen des Überwachungsprotokolls</span><span class="sxs-lookup"><span data-stu-id="2a33d-125">Search the audit log</span></span>
  
<span data-ttu-id="2a33d-126">Nachdem Sie die Überwachung aktiviert haben, suchen Sie in mehreren Office 365-Diensten nach Hunderten von einzelnen Ereignistypen.</span><span class="sxs-lookup"><span data-stu-id="2a33d-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="2a33d-127">[Durchsuchen des Überwachungsprotokolls](search-the-audit-log-in-security-and-compliance.md) nach Benutzer-und Administratoraktivitäten</span><span class="sxs-lookup"><span data-stu-id="2a33d-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="2a33d-128">GrundLegendes zu [den detaillierten Eigenschaften](detailed-properties-in-the-office-365-audit-log.md) in jedem in den Suchergebnissen enthaltenen Überwachungsdatensatz</span><span class="sxs-lookup"><span data-stu-id="2a33d-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="2a33d-129">[Suche nach eDiscovery-bezogenen Aktivitäten](search-for-ediscovery-activities-in-the-audit-log.md) , die von Administratoren und Compliance-Managern ausgeführt wurden</span><span class="sxs-lookup"><span data-stu-id="2a33d-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
