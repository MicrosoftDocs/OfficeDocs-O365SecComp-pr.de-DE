---
title: Erweiterte Indizierung von Verwaltungsberechtigten Daten
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 158af8acf4acdb8ad6650c377a23b44ed28c6f54
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607762"
---
# <a name="advanced-indexing-of-custodian-data"></a><span data-ttu-id="d35fb-102">Erweiterte Indizierung von Verwaltungsberechtigten Daten</span><span class="sxs-lookup"><span data-stu-id="d35fb-102">Advanced indexing of custodian data</span></span>

<span data-ttu-id="d35fb-p101">Wenn ein Verwaltungsberechtigter zu einem Fall erweiterte eDiscovery (Preview) hinzugefügt wird, ist keine Inhalte in Office 365, die als gilt als wurde teilweise indiziert erneut verarbeiteten vollständig durchsuchbare machen.  Dieser Vorgang wird als *erweiterte Indizierung*bezeichnet. Inhalte kann teilweise für eine Reihe von Gründe für das Vorhandensein von Bildern, nicht unterstützte Dateitypen oder bei Auftreten von Indizierung maximale Dateigröße indiziert werden.  Weitere Informationen zum teilweise indizierte Elemente finden Sie unter [teilweise indizierte Elemente in Inhaltssuche in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span><span class="sxs-lookup"><span data-stu-id="d35fb-p101">When a custodian is added to an Advanced eDiscovery (Preview) case, any content in Office 365 that was deemed as partially indexed is re-processed to make it fully searchable.  This process is called *Advanced indexing*. Content can be partially indexed for a number of reasons including the existence of images, unsupported file types or when indexing file size limits are encountered.  To learn more about partially indexed items, see [Partially indexed items in Content Search in Office 365](https://docs.microsoft.com/en-us/office365/securitycompliance/partially-indexed-items-in-content-search).</span></span>

## <a name="viewing-advanced-indexing-results"></a><span data-ttu-id="d35fb-107">Anzeigen von Ergebnissen der erweiterte Indizierung</span><span class="sxs-lookup"><span data-stu-id="d35fb-107">Viewing Advanced indexing results</span></span>

<span data-ttu-id="d35fb-p102">Nachdem der erweiterte Indizierung abgeschlossen ist, können Sie einen Überblick über die Effektivität des erneute Verarbeitung abrufen.  In der Ansicht Verwaltungsberechtigter Indizierung enthält das Diagramm alle Elemente auf den *Hybriden Index*hinzugefügt.  Der Hybrid-Index ist, wo den Inhalt erneut verarbeiteten auf Erweiterte eDiscovery (Preview) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="d35fb-p102">After the Advanced indexing process is completed, you can get an understanding of the effectiveness of re-processing.  In the Custodian Indexing view, the graph lists all items added to the *hybrid index*.  The hybrid index is where Advanced eDiscovery (Preview) stores the re-processed content.</span></span>

<span data-ttu-id="d35fb-p103">Das Diagramm enthält auch die Anzahl der Elemente, die Remediation erfordern und eine andere Grafik von Fehlern nach Dateityp. Weitere Informationen finden Sie unter [Error Remediation beim Verarbeiten von Daten](error-remediation.md).</span><span class="sxs-lookup"><span data-stu-id="d35fb-p103">The graph also includes the number of items that require remediation and another graph of errors by file type. For more information, see [Error remediation when processing data](error-remediation.md).</span></span>

## <a name="updating-advanced-indexes-for-custodians"></a><span data-ttu-id="d35fb-113">Aktualisieren von erweiterten Indizes für Verwalter</span><span class="sxs-lookup"><span data-stu-id="d35fb-113">Updating Advanced indexes for custodians</span></span>

<span data-ttu-id="d35fb-p104">Wenn ein Verwaltungsberechtigter zu einem Fall erweiterte eDiscovery (Preview) hinzugefügt wird, werden alle teilweise indizierte Elemente erneut verarbeitet. Mit der Zeit können mehr teilweise indizierte Elemente Postfach oder OneDrive-Konto des Benutzers hinzugefügt werden.  Bei Bedarf können Sie die Indizes aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d35fb-p104">When a custodian is added to an Advanced eDiscovery (Preview) case, all partially indexed items are re-processed. However, as time passes, more partially indexed items may be added to a user's mailbox or OneDrive account.  When needed, you can update the indexes.</span></span>

> [!NOTE]
> <span data-ttu-id="d35fb-p105">Aktualisieren von Indizes Verwaltungsberechtigter ist ein langer Prozess. Es wird empfohlen, dass Sie Indizes nur einmal pro Tag in dem Fall nicht aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d35fb-p105">Updating custodian indexes is a long running process. It's recommended that you don't update indexes more than once per day in a case.</span></span>
