---
title: Durchsuchen aller Postfächer und Websites mit dem eDiscovery Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 56e2978f-71b6-4141-b769-ad856d31bbec
description: In der eDiscovery Center in Office 365 können Sie alle Postfächer von Exchange Online, SharePoint Online-Websites und OneDrive for Business-Websites in einer einzigen eDiscovery-Suche suchen. Um alle Inhaltsquellen in der Organisation zu suchen, muss ein eDiscovery-Manager die entsprechenden eDiscovery-Berechtigungen für jede Inhaltsquelle zugewiesen werden.
ms.openlocfilehash: b3508d5929ca2b5b7a937eb2dccf677a2968cbbc
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529292"
---
# <a name="search-all-mailboxes-and-sites-using-the-ediscovery-center"></a><span data-ttu-id="65f95-104">Durchsuchen aller Postfächer und Websites mit dem eDiscovery Center</span><span class="sxs-lookup"><span data-stu-id="65f95-104">Search all mailboxes and sites using the eDiscovery Center</span></span>

<span data-ttu-id="65f95-p102">In der eDiscovery Center in Office 365 können Sie alle Postfächer von Exchange Online, SharePoint Online-Websites und OneDrive for Business-Websites in einer einzigen eDiscovery-Suche suchen. Um alle Inhaltsquellen in der Organisation zu suchen, muss ein eDiscovery-Manager die entsprechenden eDiscovery-Berechtigungen für jede Inhaltsquelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="65f95-p102">In the eDiscovery Center in Office 365, you can search all Exchange Online mailboxes, SharePoint Online sites, and OneDrive for Business sites in a single eDiscovery search. To search all content sources in the organization, an eDiscovery manager must be assigned the appropriate eDiscovery permissions for each content source.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="65f95-107">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="65f95-107">Before you begin</span></span>

- <span data-ttu-id="65f95-p103">Ein eDiscovery-Manager muss über die entsprechenden Berechtigungen zum Durchsuchen einer Inhaltsquelle verfügen. Weitere Informationen zum Zuweisen von eDiscovery-Berechtigungen für Postfächer und Websites finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="65f95-p103">An eDiscovery manager must be assigned the appropriate permissions to search a content source. For more information about assigning eDiscovery permissions to mailboxes and sites, see the following:</span></span> 
    
  - [<span data-ttu-id="65f95-110">Zuweisen von eDiscovery-Berechtigungen in Exchange</span><span class="sxs-lookup"><span data-stu-id="65f95-110">Assign eDiscovery permissions in Exchange</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526886)
    
  - [<span data-ttu-id="65f95-111">Zuweisen von eDiscovery-Berechtigungen in SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="65f95-111">Assign eDiscovery permissions in SharePoint Online</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=526885)
    
  - [<span data-ttu-id="65f95-112">Zuweisen von eDiscovery-Berechtigungen für OneDrive for Business-Websites</span><span class="sxs-lookup"><span data-stu-id="65f95-112">Assign eDiscovery permissions to OneDrive for Business sites</span></span>](assign-permissions-to-onedrive-for-business-sites.md)
    
- <span data-ttu-id="65f95-p104">Sie können maximal 10.000 Postfächer und eine unbegrenzte Anzahl von SharePoint Online und OneDrive for Business-Websites in einer einzigen eDiscovery Search-Abfrage suchen. Wenn Sie die bestimmter Websites suchen angeben, ist der Grenzwert jedoch 100 Websites.</span><span class="sxs-lookup"><span data-stu-id="65f95-p104">You can search a maximum of 10,000 mailboxes and an unlimited number of SharePoint Online and OneDrive for Business sites in a single eDiscovery search query. However, if you specify the specific sites to search, the limit is 100 sites.</span></span>
    
- <span data-ttu-id="65f95-115">Finden Sie [Weitere Informationen](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) im Abschnitt für eine Beschreibung der Grenzen, bei der Anzeige der Ergebnisse der bei der Suche alle Postfächer und Websites.</span><span class="sxs-lookup"><span data-stu-id="65f95-115">See the [More information](search-all-mailboxes-and-sites-with-ediscovery.md#moreinfo) section for a description of the limits when viewing the results when searching all mailboxes and sites.</span></span> 
    
- <span data-ttu-id="65f95-116">Weitere Informationen zum Erstellen von Suchabfragen in das eDiscovery Center finden Sie unter [Erstellen und Ausführen von eDiscovery-Abfragen](https://go.microsoft.com/fwlink/p/?LinkID=404032).</span><span class="sxs-lookup"><span data-stu-id="65f95-116">For more information about creating search queries in the eDiscovery Center, see [Create and run eDiscovery queries](https://go.microsoft.com/fwlink/p/?LinkID=404032).</span></span>
    
## <a name="search-all-locations"></a><span data-ttu-id="65f95-117">Durchsuchen aller Speicherorte</span><span class="sxs-lookup"><span data-stu-id="65f95-117">Search all locations</span></span>

1. <span data-ttu-id="65f95-118">Öffnen Sie im eDiscovery Center den eDiscovery-Fall, für den die Suchabfrage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="65f95-118">In the eDiscovery Center, open the eDiscovery case that you want to run the search query for.</span></span>
    
2. <span data-ttu-id="65f95-119">Klicken Sie unter **Suchen und Exportieren**klicken Sie auf eine vorhandene Abfrage oder klicken Sie auf **Neues Element** , um eine neue Suchabfrage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="65f95-119">Under **Search and Export**, click an existing query or click **New item** to create a new search query.</span></span> 
    
3. <span data-ttu-id="65f95-120">Klicken Sie auf der Seite „Suchabfrage“ im Abschnitt **Quellen** auf **Abfragebereich ändern**.</span><span class="sxs-lookup"><span data-stu-id="65f95-120">On the search query page, in the **Sources** section, click **Modify Query Scope**.</span></span>
    
4. <span data-ttu-id="65f95-121">Klicken Sie auf der Seite **Abfragebereich ändern** auf **Alles durchsuchen**, und wählen Sie die zu durchsuchenden Speicherorte für Inhalte.</span><span class="sxs-lookup"><span data-stu-id="65f95-121">On the **Modify Query Scope** page, click **Search everything**, and select the content locations to search.</span></span>
    
  - <span data-ttu-id="65f95-122">Wählen Sie **Exchange** um alle Postfächer zu suchen.</span><span class="sxs-lookup"><span data-stu-id="65f95-122">Select **Exchange** to search all mailboxes.</span></span> 
    
  - <span data-ttu-id="65f95-123">Wählen Sie **SharePoint** , alle SharePoint Online und OneDrive for Business-Websites zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="65f95-123">Select **SharePoint** to search all SharePoint Online and OneDrive for Business sites.</span></span> 
    
  - <span data-ttu-id="65f95-124">Wählen Sie sowohl **Exchange** und **SharePoint** aus, um alle Speicherorte für Inhalte in Ihrer Organisation zu suchen.</span><span class="sxs-lookup"><span data-stu-id="65f95-124">Select both **Exchange** and **SharePoint** to search all content locations in your organization.</span></span> 
    
![Durchsuchen aller Postfächer und Websites](media/e1f919ab-5596-43bb-a3c9-626cd41067b3.gif)
  
5. <span data-ttu-id="65f95-126">Klicken Sie auf **OK**, um die Änderungen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="65f95-126">Click **OK** to save the changes.</span></span> 
    
6. <span data-ttu-id="65f95-p105">Schließen Sie die Suchabfrage ab, oder überprüfen Sie weitere Informationen auf der Seite „Suchabfrage“, z. B. Schlüsselwortabfrage, Datumsbereich, Eingrenzen bestimmter zu durchsuchenden Inhaltstypen. Klicken Sie auf **Suche**, wenn Sie die Abfrage ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="65f95-p105">Complete or revise other information on the search query page, such as the keyword query, the date range, or narrowing the specific types of content to search for. When you're ready to run the query, click **Search**.</span></span> 
    
## <a name="more-information"></a><span data-ttu-id="65f95-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="65f95-129">More information</span></span>
<span data-ttu-id="65f95-130"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="65f95-130"></span></span>

- <span data-ttu-id="65f95-131">Die ersten 500 Postfächer und die ersten 500 Websites mit den meisten Ergebnissen sind auf der Seite **Abfrage** unter **Quellen** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="65f95-131">The top 500 mailboxes and the top 500 sites with the most results are listed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="65f95-132">Die Gesamtanzahl der in allen Inhaltsquellen gefundenen Elemente und deren kombinierte Gesamtgröße werden auf der Seite **Abfrage** unter **Quellen** angezeigt. 
</span><span class="sxs-lookup"><span data-stu-id="65f95-132">The total number of items found in all content sources and their combined total size are displayed under **Sources** on the **Query** page.</span></span> 
    
- <span data-ttu-id="65f95-133">Sie können eine Vorschau der 200 neuesten Suchergebnisse aus Exchange-Postfächern oder SharePoint-Websites auf der Seite **Abfrage** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="65f95-133">You can preview the 200 most recent search results located in Exchange mailboxes or SharePoint sites on the **Query** page.</span></span> 
    
    <span data-ttu-id="65f95-134">Der folgende Screenshot zeigt ein Beispiel für die Suchergebnisse, die auf der Seite **Abfrage** beim Durchsuchen aller Postfächer und Websites angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="65f95-134">The following screenshot shows an example of the search results displayed on the **Query** page when you search all mailboxes and sites.</span></span> 
    
    ![Screenshot der Ergebnisse beim Durchsuchen aller Standorte](media/4bf430f6-41ab-4bf6-afa9-33c3f6fd8b16.gif)
  

