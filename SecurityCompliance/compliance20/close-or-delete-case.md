---
title: Schließen oder Löschen eines Falls
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
ms.openlocfilehash: 30697bfafdd7db69444b97345733f3d8ec5be92a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155167"
---
# <a name="close-or-delete-a-case"></a><span data-ttu-id="3726d-102">Schließen oder Löschen eines Falls</span><span class="sxs-lookup"><span data-stu-id="3726d-102">Close or delete a case</span></span>

<span data-ttu-id="3726d-103">Wenn der von einem eDiscovery-Fall unterstützte rechtliche Fall oder die Untersuchung abgeschlossen ist, können Sie den Fall schließen.</span><span class="sxs-lookup"><span data-stu-id="3726d-103">When the legal case or investigation supported by an eDiscovery case is completed, you can close the case.</span></span> <span data-ttu-id="3726d-104">Hier erfahren Sie, was passiert, wenn Sie einen Fall schließen:</span><span class="sxs-lookup"><span data-stu-id="3726d-104">Here's what happens when you close a case:</span></span>

- <span data-ttu-id="3726d-105">Wenn der Fall alle inhaltsspeicherorte enthält, sind diese Haltestatus deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3726d-105">If the case contains any content locations on hold, those holds will be turned off.</span></span> <span data-ttu-id="3726d-106">Dies kann dazu führen, dass Inhalte dauerhaft gelöscht oder gelöscht werden, entweder durch den Benutzer oder durch einen automatisierten Prozess, beispielsweise eine Löschrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="3726d-106">This might result in content being permanently deleted or purged, either by the user or by an automated process, such as a deletion policy.</span></span>

- <span data-ttu-id="3726d-107">Durch das Schließen eines Case werden nur die haltebereiche deaktiviert, die diesem Fall zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3726d-107">Closing a case only turns off the holds that are associated with that case.</span></span> <span data-ttu-id="3726d-108">Wenn andere haltebereiche an einem Inhaltsspeicherort platziert werden (beispielsweise ein Beweissicherungsverfahren.</span><span class="sxs-lookup"><span data-stu-id="3726d-108">If other holds are place on a content location (such as a Litigation Hold.</span></span> <span data-ttu-id="3726d-109">eine Erhaltungs Richtlinie oder ein Haltestatus aus einem anderen eDiscovery-Fall) diese Aufbewahrungen werden weiterhin beibehalten.</span><span class="sxs-lookup"><span data-stu-id="3726d-109">a Preservation Policy, or a hold from a different eDiscovery case) those holds will still be maintained.</span></span>

- <span data-ttu-id="3726d-110">Der Fall wird weiterhin auf der Seite "eDiscovery" im Security & Compliance Center aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3726d-110">The case is still listed on the eDiscovery page in the Security & Compliance Center.</span></span> <span data-ttu-id="3726d-111">Die Details, Aufbewahrungen, Suchvorgänge und Elemente eines geschlossenen Falls werden beibehalten.</span><span class="sxs-lookup"><span data-stu-id="3726d-111">The details, holds, searches, and members of a closed case are retained.</span></span>

- <span data-ttu-id="3726d-112">Sie können einen Fall bearbeiten, nachdem er geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3726d-112">You can edit a case after it's closed.</span></span> <span data-ttu-id="3726d-113">Beispielsweise können Sie Mitglieder hinzufügen oder entfernen, suchen erstellen, Suchergebnisse exportieren und das Suchergebnis für die Analyse in Advanced eDiscovery vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="3726d-113">For example, you can add or removing members, create searches, export search results, and prepare search result for analysis in Advanced eDiscovery.</span></span> <span data-ttu-id="3726d-114">Der Hauptunterschied zwischen aktiven und geschlossenen Fällen besteht darin, dass die haltebereiche deaktiviert sind, wenn ein Fall geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="3726d-114">The primary difference between active and closed cases is that holds are turned off when a case is closed.</span></span>

<span data-ttu-id="3726d-115">So schließen Sie einen Fall:</span><span class="sxs-lookup"><span data-stu-id="3726d-115">To close a case:</span></span>

1. <span data-ttu-id="3726d-116">Wechseln Sie auf der Seite **Erweiterte eDiscovery** zu Ihrem Fall.</span><span class="sxs-lookup"><span data-stu-id="3726d-116">From the **Advanced eDiscovery** page, go to your case.</span></span>

2. <span data-ttu-id="3726d-117">Wechseln Sie zu **Einstellungen** , und wählen Sie **Fall Informationen**aus.</span><span class="sxs-lookup"><span data-stu-id="3726d-117">Go to **Settings** and select **Case Information**.</span></span> 

3. <span data-ttu-id="3726d-118">Klicken Sie auf **Fall schließen**.</span><span class="sxs-lookup"><span data-stu-id="3726d-118">Click **Close Case**.</span></span> 

<span data-ttu-id="3726d-119">So löschen Sie einen Fall:</span><span class="sxs-lookup"><span data-stu-id="3726d-119">To delete a case:</span></span>

1. <span data-ttu-id="3726d-120">Wechseln Sie auf der Seite **Erweiterte eDiscovery** zu Ihrem Fall.</span><span class="sxs-lookup"><span data-stu-id="3726d-120">From the **Advanced eDiscovery** page, go to your case.</span></span>

2. <span data-ttu-id="3726d-121">Wechseln Sie zu **Einstellungen** , und wählen Sie **Fall Informationen**aus.</span><span class="sxs-lookup"><span data-stu-id="3726d-121">Go to **Settings** and select **Case Information**.</span></span> 

3. <span data-ttu-id="3726d-122">Klicken Sie auf **Fall löschen**.</span><span class="sxs-lookup"><span data-stu-id="3726d-122">Click **Delete Case**.</span></span> 
