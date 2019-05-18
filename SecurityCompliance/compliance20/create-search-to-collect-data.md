---
title: Erstellen einer Suche zum Sammeln von Daten
ms.author: markjjo
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
ms.openlocfilehash: 360ba6a67d43a0b78b1104ae64885697009bb222
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155107"
---
# <a name="create-a-search-to-collect-data"></a><span data-ttu-id="3d0f7-102">Erstellen einer Suche zum Sammeln von Daten</span><span class="sxs-lookup"><span data-stu-id="3d0f7-102">Create a search to collect data</span></span>

<span data-ttu-id="3d0f7-103">Auf der Registerkarte **Suchen** in Ihrem Fall können Sie eine neue Suche erstellen, indem Sie auf **neue Suche** klicken und dem Assistenten folgen.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-103">On the **Searches** tab in your case, you can create a new search by clicking **New search** and following the wizard.</span></span>

## <a name="name-your-search-and-give-description"></a><span data-ttu-id="3d0f7-104">Benennen Sie Ihre Suche und geben Sie eine Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d0f7-104">Name your search and give description</span></span>

<span data-ttu-id="3d0f7-105">Jede Suche mit einem Fall sollte einen eindeutigen Namen haben.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-105">Each search with a case should have a unique name.</span></span> <span data-ttu-id="3d0f7-106">Optional können Sie eine Beschreibung für Ihre Suche angeben.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-106">You can optionally provide a description for your search.</span></span> 

## <a name="define-your-conditions"></a><span data-ttu-id="3d0f7-107">Definieren der Bedingungen</span><span class="sxs-lookup"><span data-stu-id="3d0f7-107">Define your conditions</span></span>

<span data-ttu-id="3d0f7-108">Sie können die Bedingungen für Ihre Suche mithilfe der vordefinierten Bedingungs Karten oder der Verwendung von Keyword Query Language (KQL) definieren.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-108">You can define the conditions for your search using the pre-built condition cards or using Keyword Query Language (KQL).</span></span> <span data-ttu-id="3d0f7-109">Weitere Informationen finden Sie unter [Erstellen von Suchabfragen](building-search-queries.md).</span><span class="sxs-lookup"><span data-stu-id="3d0f7-109">For more information, see [Build search queries](building-search-queries.md).</span></span>

## <a name="choose-the-custodians-to-search-from"></a><span data-ttu-id="3d0f7-110">Wählen Sie die zu suchenden Verwalter aus.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-110">Choose the custodians to search from</span></span>

<span data-ttu-id="3d0f7-111">Nachdem Sie Ihre Bedingungen definiert haben, müssen Sie auswählen, welche Standorte Sie durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-111">Once you have defined your conditions, you need to choose which locations you want to search.</span></span> <span data-ttu-id="3d0f7-112">Eine Möglichkeit besteht darin, die Verwalter anzugeben, die Sie bereits zu dem Fall hinzugefügt haben, den Sie durchsuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-112">One way to do it is by specifying which custodians you have already added to the case you want to search.</span></span> <span data-ttu-id="3d0f7-113">Wenn Sie eine Depotbank auswählen, führen Sie die Suche anhand aller Datenquellen aus, die der Depotbank zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-113">By selecting a custodian, you will run the search against all data sources mapped to the custodian.</span></span> <span data-ttu-id="3d0f7-114">Weitere Informationen zum Hinzufügen von depotbanks zu Ihrem Fall und zur Verwaltung ihrer Datenquellen finden Sie unter [work with depotbanks](managing-custodians.md) .</span><span class="sxs-lookup"><span data-stu-id="3d0f7-114">See [Work with custodians](managing-custodians.md) for more information on how to add custodians to your case and manage their data sources.</span></span>

## <a name="choose-non-custodial-locations"></a><span data-ttu-id="3d0f7-115">Auswählen von Speicherorten ohne Freiheitsentzug</span><span class="sxs-lookup"><span data-stu-id="3d0f7-115">Choose non-custodial locations</span></span>

<span data-ttu-id="3d0f7-116">In einigen Fällen möchten Sie möglicherweise Datenquellen durchsuchen, die nicht einer Depotbank zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3d0f7-116">In some cases, you may wish to search data sources that are not mapped to a custodian.</span></span> <span data-ttu-id="3d0f7-117">In diesem Fall können Sie die Speicherorte angeben, die Sie durchsuchen möchten, oder alle inhaltsspeicherorte nach einem bestimmten Office 365 Dienst durchsuchen (beispielsweisedurch Suchen aller Exchange-Postfächer oder aller SharePoint-und OneDrive für Unternehmen-Websites).</span><span class="sxs-lookup"><span data-stu-id="3d0f7-117">In this case, you can specify the locations you would like to search, or choose to search all content locations for a specific Office 365 service (such as searching all Exchange mailboxes or all SharePoint and OneDrive for Business sites).</span></span>