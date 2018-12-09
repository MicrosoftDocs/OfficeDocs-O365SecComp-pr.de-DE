---
title: Wiederholen Sie eine Suche Inhalt, um einen Inhaltsspeicherort Fehler zu beheben
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Verwenden Sie die Schaltfläche "Wiederholen" für Resolve Inhalte durchsucht, die Inhaltsspeicherort Fehler enthalten.
ms.openlocfilehash: 0fdc11593fec42e1f9f9b76fbbb408d9c16fd183
ms.sourcegitcommit: d5f841744b716fcf368c670009b61441f5a5eed2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2018
ms.locfileid: "27210186"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="5a965-103">Wiederholen Sie eine Suche Inhalt, um einen Inhaltsspeicherort Fehler zu beheben</span><span class="sxs-lookup"><span data-stu-id="5a965-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="5a965-104">Wenn Sie eine große Anzahl von Postfächern (z. B. Suche 100.000 Postfächer oder mehrere in einer einzelnen Inhaltssuche) suchen Inhaltssuche in die Office 365-Sicherheit und Compliance Center verwenden, erhalten Sie möglicherweise Search-Fehler, die den folgenden ähneln:</span><span class="sxs-lookup"><span data-stu-id="5a965-104">When you use Content Search in the Office 365 Security & Compliance Center to search a very large number of mailboxes (for example, searching 100,000 mailboxes or more in a single Content Search), you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="5a965-p101">Diese Fehler (mit Fehlercodes CS008-009 und CS012-002) anzugeben, dass Inhalte Suche beim Durchsuchen der Speicherorte für bestimmte Inhalte Fehler; In diesem Beispiel wurden nicht zwei Postfächer durchsucht. Diese Fehler werden auf der Seite Status Details flyoutmenü, der die Inhaltssuche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5a965-p101">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched. These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="5a965-107">Ursache für Fehler Content-location</span><span class="sxs-lookup"><span data-stu-id="5a965-107">Cause of content location errors</span></span>

<span data-ttu-id="5a965-p102">Wenn Sie eine große Anzahl von Postfächern zu suchen, wird die Suche auf Tausende von Servern in einem Microsoft-Datencenter verteilt. Eine jederzeit konnte bestimmte Server im Zustand Neustart oder beim Ausführen eines Failovers für redundante Kopien sein. In beiden Fällen wird die Inhaltssuche-Anforderung zum Abrufen von Daten Timeout. Im vorherigen Beispiel wurden die Fehler für die Postfächer, die nicht das Ergebnis der Suche Timeout.</span><span class="sxs-lookup"><span data-stu-id="5a965-p102">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter. At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies. In either of these cases, the Content Search's request to retrieve data will timeout. In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="5a965-112">Auflösen von Fehlern Content-location</span><span class="sxs-lookup"><span data-stu-id="5a965-112">Resolving content location errors</span></span>

<span data-ttu-id="5a965-p103">Neustarten der Suche führt häufig zu ähnliche Fehler auf unterschiedlichen Servern. Anstatt einen Neustart für die Suche aus, klicken Sie auf die Schaltfläche **Wiederholen** , die am oberen Rand der Seite mit den Suchergebnissen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5a965-p103">Restarting the search will often result in similar errors on different servers. Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Klicken Sie auf die Schaltfläche "Wiederholen", um Inhaltsspeicherort Fehler zu beheben](media/retrycontentsearch3.png)

<span data-ttu-id="5a965-p104">Dadurch wird die Suche nur für die Postfächer, die nicht wiederholen. Wenn Sie die Suche wiederholen, bleiben die anderen Ergebnisse, die erfolgreich zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="5a965-p104">This will result in the retrying the search only for the mailboxes that failed. When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="5a965-118">Tipps zur Vermeidung von Inhaltsspeicherort Fehler</span><span class="sxs-lookup"><span data-stu-id="5a965-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="5a965-119">Hier sind einige Fehlerursachen Inhaltsspeicherort hinzufügen und einige Tipps zur einfacheren vermeiden, große Anzahl von Postfächern zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5a965-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="5a965-p105">Das Postfach, das durchsucht wird möglicherweise aufgrund Benutzeraktivität ausgelastet. In diesem Fall möglicherweise selbst, um zu verhindern, dass das Postfach zu einem Ausfall des Suchdiensts drosseln. Um dies zu vermeiden, führen Sie Suchvorgänge während der Geschäftszeiten.</span><span class="sxs-lookup"><span data-stu-id="5a965-p105">The mailbox being searched might be busy due to user activity. In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable. To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="5a965-p106">Die Suchabfrage möglicherweise zu viel Inhalt aus dem Postfach abgerufen werden. Wenn möglich, versuchen Sie, die Suche mithilfe von Schlüsselwörtern, Datumsbereiche und Suchkriterien einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="5a965-p106">The search query might be retrieving too much content from the mailbox. If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="5a965-p107">Zu viele Schlüsselwörter oder Schlüsselwort Ausdrücke beim Erstellen einer Suchabfrage mithilfe der [Liste der Schlüsselwörter](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Beim Ausführen einer Suchabfrage, die der Liste Schlüsselwörter verwendet, führt der Dienst im Wesentlichen eine separate Suche für jede Zeile in der Schlüsselwortliste, sodass Statistiken generiert werden können. Wenn Sie die Liste der Schlüsselwörter in Suchabfragen verwenden, minimieren Sie die Anzahl der Zeilen in der Schlüsselwortliste oder Teilen Sie die Zahl Schlüsselwörter in kleinere Listen, und erstellen Sie eine andere Suche für jede Schlüsselwortliste.</span><span class="sxs-lookup"><span data-stu-id="5a965-p107">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated. If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5a965-128">Zur Verringerung der Probleme aufgrund von großen Listen Sie nun auf ein Maximum von 20 Zeilen in der Schlüsselwortliste einer Suchabfrage begrenzt.</span><span class="sxs-lookup"><span data-stu-id="5a965-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="5a965-p108">Zu viele Suchvorgänge werden mit demselben Postfach zur selben Zeit ausgeführt wird. Versuchen Sie wenn möglich, eine Suche auf eine beliebige ein Postfach zu einem Zeitpunkt auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5a965-p108">Too many searches are being performed on the same mailbox at the same time. If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="5a965-p109">Suchen in einem einzelnen Suchvorgang zu viele Postfächer. Die Wahrscheinlichkeit der Inhaltsspeicherort Fehler erhöht, wenn eine große Anzahl von Postfächern zu suchen. Versuchen Sie nach Möglichkeit, mehrere Suchvorgänge durchgeführt werden, damit jeder Suche eine Teilmenge der Postfächer in Ihrer Organisation enthält.</span><span class="sxs-lookup"><span data-stu-id="5a965-p109">Searching too many mailboxes in a single search. The probability of content location errors increases when searching a very large number of mailboxes. If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="5a965-p110">Erforderliche Wartung wird für das Postfach durchgeführt. Obwohl diese Ursache wahrscheinlich selten auftritt, warten Sie einen Moment während nach dem Empfang des Inhaltsspeicherort Fehlers, und wiederholen Sie die Suche.</span><span class="sxs-lookup"><span data-stu-id="5a965-p110">Required maintenance is being performed on the mailbox. Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
