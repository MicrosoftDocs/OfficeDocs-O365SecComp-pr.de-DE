---
title: Erweiterte Indizierung von Daten für eine Untersuchung
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
ms.openlocfilehash: 9537cf743b89da7167ce3a37a5915027f4eb717a
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030158"
---
# <a name="advanced-indexing-of-data-for-an-investigation"></a><span data-ttu-id="f5f6a-102">Erweiterte Indizierung von Daten für eine Untersuchung</span><span class="sxs-lookup"><span data-stu-id="f5f6a-102">Advanced indexing of data for an investigation</span></span>

<span data-ttu-id="f5f6a-103">Der Inhalt des Live-Systems kann aus einer Reihe von Gründen teilweise indiziert werden, einschließlich der Existenz von Bildern, nicht unterstützten Dateitypen oder bei der Indizierung von Dateigrößenbeschränkungen.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-103">Content in the live system can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.</span></span> <span data-ttu-id="f5f6a-104">Wenn Sie mit hohem Risikodaten Überlauf arbeiten, möchten Sie sicherstellen, dass die Suche alle Daten erfasst, die Sie untersuchen möchten.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-104">When you are dealing with high risk data spill, you want to make sure that your search captured all data that you want to investigate.</span></span> <span data-ttu-id="f5f6a-105">Wenn eine betroffene Person zu einer Datenermittlung hinzugefügt wird, werden alle Inhalte in Office 365, die als teilweise indiziert angesehen wurden, erneut verarbeitet, damit Sie vollständig durchsuchbar sind.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-105">When a person of interest is added to a Data investigation, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.</span></span> <span data-ttu-id="f5f6a-106">Dieser Vorgang wird als *Erweiterte Indizierung*bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-106">This process is called *Advanced indexing*.</span></span> 

<span data-ttu-id="f5f6a-107">Weitere Informationen zur Verarbeitungsunterstützung in Office 365 und teilweise indizierten Elementen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="f5f6a-107">To learn more about processing support in Office 365 and partially indexed items, see:</span></span>

- [<span data-ttu-id="f5f6a-108">Unterstützte Dateitypen in Daten Untersuchungen</span><span class="sxs-lookup"><span data-stu-id="f5f6a-108">Supported file types in Data Investigations</span></span>](supported-filetypes-datainvestigations.md)

- [<span data-ttu-id="f5f6a-109">Teilweise indizierte Elemente in der Inhaltssuche in Office 365</span><span class="sxs-lookup"><span data-stu-id="f5f6a-109">Partially indexed items in Content Search in Office 365</span></span>](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search)

- [<span data-ttu-id="f5f6a-110">Von der Exchange-Suche indizierte Dateiformate</span><span class="sxs-lookup"><span data-stu-id="f5f6a-110">File formats indexed by Exchange Search</span></span>](https://docs.microsoft.com/en-us/exchange/file-formats-indexed-by-exchange-search-exchange-2013-help)

- [<span data-ttu-id="f5f6a-111">Standardmäßig durchforstete Dateinamenerweiterungen und analysierte Dateitypen in SharePoint Server</span><span class="sxs-lookup"><span data-stu-id="f5f6a-111">Default crawled file name extensions and parsed file types in SharePoint Server</span></span>](https://docs.microsoft.com/en-us/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types)

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="f5f6a-112">Anzeigen erweiterter Indizierungs Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="f5f6a-112">Viewing Advanced indexing results</span></span>

<span data-ttu-id="f5f6a-113">Nach Abschluss des erweiterten Indizierungsprozesses können Sie sich über die Effektivität der erneuten Verarbeitung informieren.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-113">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.</span></span>  <span data-ttu-id="f5f6a-114">In der Ansicht Interessen Indizes werden alle Elemente aufgelistet, die dem *Hybrid Index*hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-114">In the People of interest indexing view, the graph lists all items added to the *hybrid index*.</span></span>  <span data-ttu-id="f5f6a-115">Der Hybrid Index enthält Daten Untersuchungen (Preview), in denen der erneut verarbeitete Inhalt gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-115">The hybrid index is where Data Investigations (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="f5f6a-116">Das Diagramm enthält außerdem die Anzahl der Elemente, für die eine Korrektur erforderlich ist, und einen weiteren Diagramm mit Fehlern nach Dateityp.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-116">The graph also includes the number of items that require remediation and another graph of errors by file type.</span></span> <span data-ttu-id="f5f6a-117">Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="f5f6a-117">For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-people-of-interest"></a><span data-ttu-id="f5f6a-118">Aktualisieren erweiterter Indizes für Personen von Interesse</span><span class="sxs-lookup"><span data-stu-id="f5f6a-118">Updating Advanced indexes for people of interest</span></span>

<span data-ttu-id="f5f6a-119">Wenn eine Person von Interesse zu einer Datenermittlung hinzugefügt wird, werden alle teilweise indizierten Elemente erneut verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-119">When a person of interest is added to a data investigation, all partially indexed items are re-processed.</span></span> <span data-ttu-id="f5f6a-120">Im Laufe der Zeit können jedoch mehr teilweise indizierte Elemente zum Postfach-oder OneDrive-Konto eines Benutzers hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-120">However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.</span></span>  <span data-ttu-id="f5f6a-121">Bei Bedarf können Sie die Indizes aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-121">When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="f5f6a-122">Das Aktualisieren von Personen mit interessanten Indizes ist ein langwieriger Prozess.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-122">Updating people of interest indexes is a long running process.</span></span> <span data-ttu-id="f5f6a-123">Es wird empfohlen, dass Sie Indizes nicht mehr als einmal pro Tag in einer Untersuchung aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="f5f6a-123">It's recommended that you don't update indexes more than once per day in an investigation.</span></span>
