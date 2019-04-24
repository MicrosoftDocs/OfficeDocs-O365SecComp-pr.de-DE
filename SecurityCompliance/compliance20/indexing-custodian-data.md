---
title: Erweiterte Indizierung der Daten von Verwaltungsberechtigten
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
ms.openlocfilehash: 1521aadca42c8119ae341065865b227fb16ffcf3
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251943"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="1416c-102">Erweiterte Indizierung der Daten von Verwaltungsberechtigten</span><span class="sxs-lookup"><span data-stu-id="1416c-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="1416c-103">Wenn eine Depotbank zu einem Advanced eDiscovery (Preview)-Fall hinzugefügt wird, werden alle Inhalte in Office 365, die als teilweise indiziert angesehen wurden, erneut verarbeitet, damit Sie vollständig durchsuchbar sind.</span><span class="sxs-lookup"><span data-stu-id="1416c-103">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.</span></span>  <span data-ttu-id="1416c-104">Dieser Vorgang wird als *Erweiterte Indizierung*bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1416c-104">This process is called *Advanced indexing*.</span></span> <span data-ttu-id="1416c-105">Inhalte können teilweise aus verschiedenen Gründen indiziert werden, einschließlich der Existenz von Bildern, nicht unterstützten Dateitypen oder bei der Indizierung von Dateigrößenbeschränkungen.</span><span class="sxs-lookup"><span data-stu-id="1416c-105">Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.</span></span>

<span data-ttu-id="1416c-106">Weitere Informationen zur Verarbeitungsunterstützung in Office 365 und teilweise indizierten Elementen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="1416c-106">To learn more about processing support in Office 365 and partially indexed items, see:</span></span>

- [<span data-ttu-id="1416c-107">Unterstützte Dateitypen in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1416c-107">Supported file types in Advanced eDiscovery</span></span>](supported-filetypes-ediscovery20.md)
- [<span data-ttu-id="1416c-108">Teilweise indizierte Elemente in der Inhaltssuche in Office 365</span><span class="sxs-lookup"><span data-stu-id="1416c-108">Partially indexed items in Content Search in Office 365</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)
- [<span data-ttu-id="1416c-109">Von der Exchange-Suche indizierte Dateiformate</span><span class="sxs-lookup"><span data-stu-id="1416c-109">File formats indexed by Exchange Search</span></span>](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)
- [<span data-ttu-id="1416c-110">Standardmäßig durchforstete Dateinamenerweiterungen und analysierte Dateitypen in SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="1416c-110">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="1416c-111">Anzeigen erweiterter Indizierungs Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="1416c-111">Viewing Advanced indexing results</span></span>

<span data-ttu-id="1416c-112">Nach Abschluss des erweiterten Indizierungsprozesses können Sie sich über die Effektivität der erneuten Verarbeitung informieren.</span><span class="sxs-lookup"><span data-stu-id="1416c-112">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.</span></span>  <span data-ttu-id="1416c-113">In der Ansicht Depot Indizierung werden alle dem *Hybrid Index*hinzugefügten Elemente aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1416c-113">In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.</span></span>  <span data-ttu-id="1416c-114">Im Hybrid Index werden die neu verarbeiteten Inhalte von Advanced eDiscovery (Preview) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1416c-114">The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="1416c-115">Das Diagramm enthält außerdem die Anzahl der Elemente, für die eine Korrektur erforderlich ist, und einen weiteren Diagramm mit Fehlern nach Dateityp.</span><span class="sxs-lookup"><span data-stu-id="1416c-115">The graph also includes the number of items that require remediation and another graph of errors by file type.</span></span> <span data-ttu-id="1416c-116">Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="1416c-116">For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="1416c-117">Aktualisieren erweiterter Indizes für Verwalter</span><span class="sxs-lookup"><span data-stu-id="1416c-117">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="1416c-118">Wenn einem erweiterten eDiscovery-Fall (Preview) ein Depot hinzugefügt wird, werden alle teilweise indizierten Elemente erneut verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1416c-118">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed.</span></span> <span data-ttu-id="1416c-119">Im Laufe der Zeit können jedoch mehr teilweise indizierte Elemente zum Postfach-oder OneDrive-Konto eines Benutzers hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1416c-119">However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.</span></span>  <span data-ttu-id="1416c-120">Bei Bedarf können Sie die Indizes aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1416c-120">When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="1416c-121">Das Aktualisieren von Depot Indizes ist ein langwieriger Prozess.</span><span class="sxs-lookup"><span data-stu-id="1416c-121">Updating custodian indexes is a long running process.</span></span> <span data-ttu-id="1416c-122">Es wird empfohlen, die Indizes in einem Fall nicht mehr als einmal pro Tag zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="1416c-122">It's recommended that you don't update indexes more than once per day in a case.</span></span>
