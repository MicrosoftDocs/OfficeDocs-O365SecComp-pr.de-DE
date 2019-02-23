---
title: Wiederholen einer Inhaltssuche zum Beheben eines Inhaltsspeicherort Fehlers
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: Verwenden Sie die Schaltfläche wiederHolen zum Auflösen von Inhalts suchVorgängen, die Inhaltsspeicherort Fehler aufweisen.
ms.openlocfilehash: 032d93ef0990ed1dd7c1ea7bf2ba16653b3a862f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218855"
---
# <a name="retry-a-content-search-to-resolve-a-content-location-error"></a><span data-ttu-id="f168b-103">Wiederholen einer Inhaltssuche zum Beheben eines Inhaltsspeicherort Fehlers</span><span class="sxs-lookup"><span data-stu-id="f168b-103">Retry a Content Search to resolve a content location error</span></span>

<span data-ttu-id="f168b-104">Wenn Sie die Inhaltssuche im Office 365 Security & Compliance Center verwenden, um eine sehr große Anzahl von Postfächern zu durchsuchen (beispielsweisedurch suchen von 100.000-Postfächern oder mehr in einer einzelnen Inhaltssuche), werden möglicherweise Suchfehler angezeigt, die den folgenden ähneln:</span><span class="sxs-lookup"><span data-stu-id="f168b-104">When you use Content Search in the Office 365 Security & Compliance Center to search a very large number of mailboxes (for example, searching 100,000 mailboxes or more in a single Content Search), you may get search errors that are similar to the following:</span></span>

```
Error

The search on the following locations failed:

User1@contoso.com: Problem in processing the request. Please try again later. If you keep getting this error, contact your admin. (CS008-009)

User2@contoso.com: Application error occurred. Please try again later. (CS012-002)
```

<span data-ttu-id="f168b-p101">Diese Fehler (mit Fehlercodes von CS008-009 und CS012-002) deuten darauf hin, dass die Inhaltssuche bestimmte inhaltsspeicherorte nicht durchsuchen konnte. in diesem Beispiel wurden zwei Postfächer nicht durchsucht. Diese Fehler werden auf der Seite mit dem Statusdetails-Flyout der Inhaltssuche angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f168b-p101">These errors (with error codes of CS008-009 and CS012-002) indicate that Content Search failed to search specific content locations; in this example, two mailboxes weren't searched. These errors are displayed on the status details flyout page of the Content Search.</span></span>

## <a name="cause-of-content-location-errors"></a><span data-ttu-id="f168b-107">Ursache von Inhaltsspeicherort Fehlern</span><span class="sxs-lookup"><span data-stu-id="f168b-107">Cause of content location errors</span></span>

<span data-ttu-id="f168b-p102">Beim Durchsuchen einer hohen Anzahl von Postfächern wird die Suche über Tausende von Servern in einem Microsoft-Datencenter verteilt. Zu einem beliebigen Zeitpunkt können bestimmte Server im Neustartstatus oder bei einem Failover auf redundante Kopien sein. In beiden Fällen wird die Anforderung der Inhaltssuche zum Abrufen von Daten Timeout. Im vorherigen Beispiel waren die Fehler für die Postfächer, die fehlgeschlagen waren, das Ergebnis des Such Timeouts.</span><span class="sxs-lookup"><span data-stu-id="f168b-p102">When searching a large number of mailboxes, the search is distributed across thousands of servers in a Microsoft datacenter. At any one time, specific servers could be in reboot state or in the process of failing over to redundant copies. In either of these cases, the Content Search's request to retrieve data will timeout. In the previous example, the errors for the mailboxes that failed were the result of the search timing out.</span></span>

## <a name="resolving-content-location-errors"></a><span data-ttu-id="f168b-112">Auflösen von Inhaltsspeicherort Fehlern</span><span class="sxs-lookup"><span data-stu-id="f168b-112">Resolving content location errors</span></span>

<span data-ttu-id="f168b-p103">Das Neustarten der Suche führt häufig zu ähnlichen Fehlern auf verschiedenen Servern. Anstatt die Suche neu zu starten, klicken Sie oben auf der Suchergebnisseite auf die Schaltfläche wieder **holen** .</span><span class="sxs-lookup"><span data-stu-id="f168b-p103">Restarting the search will often result in similar errors on different servers. Instead of restarting the search, click the **Retry** button that is displayed at the top of the search results page.</span></span>

![Klicken Sie auf die Schaltfläche wiederholen, um Fehler bei der Inhalts Lokalisierung zu beheben](media/retrycontentsearch3.png)

<span data-ttu-id="f168b-p104">Dies führt dazu, dass die Suche nur für die Postfächer erneut versucht wird, bei denen ein Fehler aufgetreten ist. Wenn Sie die Suche wiederholen, werden die anderen Ergebnisse, die erfolgreich zurückgegeben wurden, beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f168b-p104">This will result in the retrying the search only for the mailboxes that failed. When you retry the search, the other results that were successfully returned are retained.</span></span>

## <a name="tips-to-avoid-content-location-errors"></a><span data-ttu-id="f168b-118">Tipps zur Vermeidung von Inhaltsspeicherort Fehlern</span><span class="sxs-lookup"><span data-stu-id="f168b-118">Tips to avoid content location errors</span></span>

<span data-ttu-id="f168b-119">Im folgenden finden Sie einige zusätzliche Ursachen für Fehler im Inhaltsspeicherort und einige Tipps, die Ihnen bei der Suche nach einer hohen Anzahl von Postfächern helfen.</span><span class="sxs-lookup"><span data-stu-id="f168b-119">Here are some addition causes of content location errors and some tips to help you avoid them when searching large numbers of mailboxes.</span></span>

- <span data-ttu-id="f168b-p105">Das zu durchsuchende Postfach ist aufgrund der Benutzeraktivität möglicherweise ausgelastet. In diesem Fall kann der Suchdienst sich selbst Drosseln, um zu verhindern, dass das Postfach nicht mehr verfügbar ist. Um dies zu vermeiden, führen Sie Suchvorgänge außerhalb der Geschäftszeiten aus.</span><span class="sxs-lookup"><span data-stu-id="f168b-p105">The mailbox being searched might be busy due to user activity. In this case, the search service might throttle itself to prevent the mailbox from becoming unavailable. To avoid this, try running searches during non-business hours.</span></span>

- <span data-ttu-id="f168b-p106">Die Suchabfrage kann zu viele Inhalte aus dem Postfach abrufen. Versuchen Sie nach Möglichkeit, den Bereich der Suche mithilfe von Stichwörtern, Datumsbereichen und Suchbedingungen einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="f168b-p106">The search query might be retrieving too much content from the mailbox. If possible, try to narrow the scope of the search by using keywords, date ranges, and search conditions.</span></span>

- <span data-ttu-id="f168b-p107">Zu viele Schlüsselwörter oder Stichwort Ausdrücke beim Erstellen einer Suchabfrage mithilfe der [Stichwörter Liste](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). Wenn Sie eine Suchabfrage ausführen, die die Stichwörter Liste verwendet, führt der Dienst im Wesentlichen eine separate Suche für jede Zeile in der Schlüsselwortliste aus, damit Statistiken generiert werden können. Wenn Sie die Liste Stichwörter in Suchabfragen verwenden, minimieren Sie die Anzahl der Zeilen in der Keyword-Liste, oder Teilen Sie die Zahlen Schlüsselwörter in kleinere Listen auf, und erstellen Sie eine andere Suche für jede Keyword-Liste.</span><span class="sxs-lookup"><span data-stu-id="f168b-p107">Too many keywords or keyword phrases when you create a search query using the [keywords list](view-keyword-statistics-for-content-search.md#get-keyword-statistics-for-content-searches). When you run a search query that uses the keywords list, the service essentially runs a separate search for each row in the keyword list so that statistics can be generated. If you're using the keywords list in search queries, minimize the number of rows in the keyword list or divide the number keywords into smaller lists and create a different search for each keyword list.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f168b-128">Um Probleme zu vermeiden, die durch umfangreiche Stichwortlisten verursacht werden, sind Sie jetzt auf maximal 20 Zeilen in der Stichwortliste einer Suchabfrage beschränkt.</span><span class="sxs-lookup"><span data-stu-id="f168b-128">To help reduce issues caused by large keyword lists, you're now limited to a maximum of 20 rows in the keyword list of a search query.</span></span>

- <span data-ttu-id="f168b-p108">Zu viele Suchvorgänge werden gleichzeitig für dasselbe Postfach durchgeführt. Versuchen Sie nach Möglichkeit, eine Suche gleichzeitig an einem beliebigen Postfach auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f168b-p108">Too many searches are being performed on the same mailbox at the same time. If possible, try to run one search at a time on any one mailbox.</span></span>

- <span data-ttu-id="f168b-p109">Durchsuchen zu vieler Postfächer in einer einzelnen Suche. Bei der Suche nach einer sehr großen Anzahl von Postfächern erhöht sich die Wahrscheinlichkeit von Inhaltsspeicherort Fehlern. Versuchen Sie nach Möglichkeit, mehrere Suchvorgänge auszuführen, damit jede Suche eine Teilmenge der Postfächer in Ihrer Organisation enthält.</span><span class="sxs-lookup"><span data-stu-id="f168b-p109">Searching too many mailboxes in a single search. The probability of content location errors increases when searching a very large number of mailboxes. If possible, try to run multiple searches so that each search includes a subset of  mailboxes in your organization.</span></span>

- <span data-ttu-id="f168b-p110">Erforderliche Wartung für das Postfach. Obwohl diese Ursache wahrscheinlich selten auftritt, warten Sie eine Weile nach Erhalt des Inhaltsspeicher Fehlers, und wiederholen Sie die Suche.</span><span class="sxs-lookup"><span data-stu-id="f168b-p110">Required maintenance is being performed on the mailbox. Though this cause probably occurs infrequently, wait a little while after receiving the content location error and then retry the search.</span></span>
