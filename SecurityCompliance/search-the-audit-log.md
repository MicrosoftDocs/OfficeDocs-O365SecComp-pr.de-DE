---
title: Durchsuchen des Überwachungsprotokolls nach Benutzer-und Administratoraktivitäten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/18/2018
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
ROBOTS: NOINDEX, NOFOLLOW
search.appverid: MOE150
ms.assetid: 57ca5138-0ae0-4d34-bd40-240441ef2fb6
description: 'Das Office 365 Überwachungsprotokoll ist ein einheitliches Überwachungsprotokoll. Warum ein einheitliches Überwachungsprotokoll? Da Ereignisse von den meisten Office 365 Diensten, die Sie als Organisation abonniert haben, in einem einzigen Überwachungsprotokoll aufgezeichnet werden, das Sie durchsuchen können. Das bedeutet, dass Sie in diesen Diensten nach Benutzer-und Administratoraktivitäten suchen können:'
ms.openlocfilehash: 1d3f45d24a8d1a83c20f5d36b12ced761e00f936
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158777"
---
# <a name="search-the-audit-log-for-user-and-admin-activity-in-office-365"></a><span data-ttu-id="2ad3d-106">Durchsuchen des Überwachungsprotokolls nach Benutzer-und Administratoraktivitäten in Office 365</span><span class="sxs-lookup"><span data-stu-id="2ad3d-106">Search the audit log for user and admin activity in Office 365</span></span>

<span data-ttu-id="2ad3d-107">Das Office 365 Überwachungsprotokoll ist ein einheitliches Überwachungsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="2ad3d-107">The Office 365 audit log is a unified audit log.</span></span> <span data-ttu-id="2ad3d-108">Warum ein einheitliches Überwachungsprotokoll?</span><span class="sxs-lookup"><span data-stu-id="2ad3d-108">Why a unified audit log?</span></span> <span data-ttu-id="2ad3d-109">Da Ereignisse von den meisten Office 365 Diensten, die Sie als Organisation abonniert haben, in einem einzigen Überwachungsprotokoll aufgezeichnet werden, das Sie durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="2ad3d-109">Because events from most Office 365 services that you're organization subscribes to are recorded in a single audit log that you can search.</span></span> <span data-ttu-id="2ad3d-110">Das bedeutet, dass Sie in diesen Diensten nach Benutzer-und Administratoraktivitäten suchen können:</span><span class="sxs-lookup"><span data-stu-id="2ad3d-110">That means you can search for user and admin activity in these services:</span></span> 
  
- <span data-ttu-id="2ad3d-111">SharePoint</span><span class="sxs-lookup"><span data-stu-id="2ad3d-111">SharePoint</span></span>
- <span data-ttu-id="2ad3d-112">OneDrive</span><span class="sxs-lookup"><span data-stu-id="2ad3d-112">OneDrive</span></span>
- <span data-ttu-id="2ad3d-113">Exchange</span><span class="sxs-lookup"><span data-stu-id="2ad3d-113">Exchange</span></span>
- <span data-ttu-id="2ad3d-114">Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="2ad3d-114">Azure Active Directory</span></span>
- <span data-ttu-id="2ad3d-115">Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2ad3d-115">Microsoft Teams</span></span>
- <span data-ttu-id="2ad3d-116">eDiscovery</span><span class="sxs-lookup"><span data-stu-id="2ad3d-116">eDiscovery</span></span>
- <span data-ttu-id="2ad3d-117">Power BI</span><span class="sxs-lookup"><span data-stu-id="2ad3d-117">Power BI</span></span>
- <span data-ttu-id="2ad3d-118">Yammer</span><span class="sxs-lookup"><span data-stu-id="2ad3d-118">Yammer</span></span>
- <span data-ttu-id="2ad3d-119">Sway</span><span class="sxs-lookup"><span data-stu-id="2ad3d-119">Sway</span></span>
- <span data-ttu-id="2ad3d-120">Microsoft Stream</span><span class="sxs-lookup"><span data-stu-id="2ad3d-120">Microsoft Stream</span></span>
   
 ## <a name="set-up-auditing"></a><span data-ttu-id="2ad3d-121">Einrichten der Überwachung</span><span class="sxs-lookup"><span data-stu-id="2ad3d-121">Set up auditing</span></span>
  
<span data-ttu-id="2ad3d-122">Es gibt wenige Schritte, die Sie ausführen müssen, bevor Sie das Office 365 Überwachungsprotokoll durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="2ad3d-122">There's few things you have to do before you can search the Office 365 audit log.</span></span>
  
- <span data-ttu-id="2ad3d-123">[Aktivieren Sie die Überwachungsprotokoll Suche](turn-audit-log-search-on-or-off.md) , um die Aufzeichnung von Ereignissen zu starten, nach denen Sie suchen können.</span><span class="sxs-lookup"><span data-stu-id="2ad3d-123">[Turn on audit log search](turn-audit-log-search-on-or-off.md) to start recording events that you can search for</span></span> 
    
- <span data-ttu-id="2ad3d-124">[Aktivieren der postfachüberwachung](enable-mailbox-auditing.md) , damit Sie nach Post fachbezogenen Ereignissen suchen können; beispielsweise wenn sich ein Benutzer bei seinem Postfach anmeldet oder Elemente aus dem Ordner "refundable Items" löscht.</span><span class="sxs-lookup"><span data-stu-id="2ad3d-124">[Enable mailbox auditing](enable-mailbox-auditing.md) so you can search for mailbox-related events; such as when a user signs in to their mailbox or purges items from their Recoverable Items folder</span></span> 
    
 ## <a name="search-the-audit-log"></a><span data-ttu-id="2ad3d-125">Durchsuchen des Überwachungsprotokolls</span><span class="sxs-lookup"><span data-stu-id="2ad3d-125">Search the audit log</span></span>
  
<span data-ttu-id="2ad3d-126">Nachdem Sie die Überwachung aktiviert haben, suchen Sie in mehreren Office 365 Diensten nach Hunderten von einzelnen Ereignistypen.</span><span class="sxs-lookup"><span data-stu-id="2ad3d-126">After you turn on auditing, you search for hundreds of individual types of events from multiple Office 365 services.</span></span>
  
- <span data-ttu-id="2ad3d-127">[Durchsuchen des Überwachungsprotokolls](search-the-audit-log-in-security-and-compliance.md) nach Benutzer-und Administratoraktivitäten</span><span class="sxs-lookup"><span data-stu-id="2ad3d-127">[Search the audit log](search-the-audit-log-in-security-and-compliance.md) for user and admin activities</span></span> 
    
- <span data-ttu-id="2ad3d-128">Grundlegendes zu [den detaillierten Eigenschaften](detailed-properties-in-the-office-365-audit-log.md) in jedem Überwachungsdatensatz, der in den Suchergebnissen enthalten ist</span><span class="sxs-lookup"><span data-stu-id="2ad3d-128">[Understand the detailed properties](detailed-properties-in-the-office-365-audit-log.md) in each auditing record included in the search results</span></span> 
    
- <span data-ttu-id="2ad3d-129">[Suchen nach eDiscovery-bezogenen Aktivitäten](search-for-ediscovery-activities-in-the-audit-log.md) , die von Administratoren und Compliance-Managern ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="2ad3d-129">[Search for eDiscovery-related activities](search-for-ediscovery-activities-in-the-audit-log.md) performed by admins and compliance managers</span></span> 
