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
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: f8f1a92f001bf8f9e23f54bbb05fbbcf443bf4b9
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218665"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="6e2f2-102">Erweiterte Indizierung der Daten von Verwaltungsberechtigten</span><span class="sxs-lookup"><span data-stu-id="6e2f2-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="6e2f2-p101">Wenn eine Depotbank zu einem Advanced eDiscovery (Preview)-Fall hinzugefügt wird, werden alle Inhalte in Office 365, die als teilweise indiziert angesehen wurden, erneut verarbeitet, damit Sie vollständig durchsuchbar sind.  Dieser Vorgang wird als *Erweiterte Indizierung*bezeichnet. Inhalte können teilweise aus verschiedenen Gründen indiziert werden, einschließlich der Existenz von Bildern, nicht unterstützten Dateitypen oder bei der Indizierung von Dateigrößenbeschränkungen.  Weitere Informationen zu teilweise indizierten Elementen finden Sie unter [teilweise indizierte Elemente in der Inhaltssuche in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span><span class="sxs-lookup"><span data-stu-id="6e2f2-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="6e2f2-107">Anzeigen erweiterter Indizierungs Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="6e2f2-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="6e2f2-p102">Nach Abschluss des erweiterten Indizierungsprozesses können Sie sich über die Effektivität der erneuten Verarbeitung informieren.  In der Ansicht Depot Indizierung werden alle dem *Hybrid Index*hinzugefügten Elemente aufgelistet.  Im Hybrid Index werden die neu verarbeiteten Inhalte von Advanced eDiscovery (Preview) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6e2f2-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="6e2f2-p103">Das Diagramm enthält außerdem die Anzahl der Elemente, für die eine Korrektur erforderlich ist, und einen weiteren Diagramm mit Fehlern nach Dateityp. Weitere Informationen finden Sie unter [Fehlerkorrektur bei der Verarbeitung von Daten](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="6e2f2-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="6e2f2-113">Aktualisieren erweiterter Indizes für Verwalter</span><span class="sxs-lookup"><span data-stu-id="6e2f2-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="6e2f2-p104">Wenn einem erweiterten eDiscovery-Fall (Preview) ein Depot hinzugefügt wird, werden alle teilweise indizierten Elemente erneut verarbeitet. Im Laufe der Zeit können jedoch mehr teilweise indizierte Elemente zum Postfach-oder OneDrive-Konto eines Benutzers hinzugefügt werden.  Bei Bedarf können Sie die Indizes aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6e2f2-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="6e2f2-p105">Das Aktualisieren von Depot Indizes ist ein langwieriger Prozess. Es wird empfohlen, die Indizes in einem Fall nicht mehr als einmal pro Tag zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="6e2f2-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
