---
title: Erstellen von Suchabfragen
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
ms.openlocfilehash: 8e7f3d798d3b6cfe25d57b941ed2be1d8d5e92b6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216985"
---
# <a name="build-search-queries"></a><span data-ttu-id="8b2a9-102">Erstellen von Suchabfragen</span><span class="sxs-lookup"><span data-stu-id="8b2a9-102">Build search queries</span></span>

<span data-ttu-id="8b2a9-103">Beim Erstellen einer Abfrage können Sie verschiedene Schlüsselwörter und Bedingungen verwenden, um zu definieren, welche Elemente gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b2a9-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="8b2a9-104">Stichwortsuche</span><span class="sxs-lookup"><span data-stu-id="8b2a9-104">Keyword searches</span></span>

<span data-ttu-id="8b2a9-p101">Geben Sie im Feld **Stichwörter** eine Suchabfrage ein. Sie können Schlüsselwörter, Nachrichteneigenschaften wie gesendete und empfangene Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, an dem ein Dokument zuletzt geändert wurde, angeben. Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**und **near**. Sie können auch nach vertraulichen Informationen (wie Sozialversicherungsnummern) in Dokumenten suchen oder nach Dokumenten suchen, die extern freigegeben wurden. Wenn Sie das Schlüsselwortfeld leer lassen, werden alle Inhalte an den angegebenen Inhaltsspeicherorten in die Suchergebnisse eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8b2a9-p101">Type a search query in **Keywords** box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="8b2a9-p102">Alternativ können Sie auf das Kontrollkästchen **Keyword-Liste anzeigen** klicken und in jeder Zeile ein Stichwort eingeben. Wenn Sie dies tun, werden die Schlüsselwörter in jeder Zeile durch einen logischen Operator ( **c:s**) verbunden, der in der Funktionalität mit dem **or** -Operator in der erstellten Suchabfrage vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="8b2a9-p102">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row. If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="8b2a9-p103">Gründe für die Verwendung der Keyword-Liste Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit jedem Stichwort übereinstimmen. Auf diese Weise können Sie schnell erkennen, welche Schlüsselwörter am meisten (und am wenigsten) wirksam sind. Sie können auch eine Schlüsselwortphrase (umgeben von Klammern) in einer Zeile verwenden. Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistik](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="8b2a9-p103">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="8b2a9-117">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="8b2a9-117">Conditions</span></span>
    
<span data-ttu-id="8b2a9-p104">Sie können Suchbedingungen hinzufügen, um eine Suche einzuschränken und eine genauere Ergebnismenge zurückzugeben. Jede Bedingung fügt eine Klausel zu der Suchabfrage hinzu, die erstellt und beim Starten der Suche ausgeführt wird. Eine Bedingung ist logisch mit der Stichwortabfrage (angegeben im Stichwortfeld) durch einen logischen Operator (**c:c**) verbunden, der in der Funktionalität mit dem **and-** Operator vergleichbar ist. Dies führt dazu, dass Elemente sowohl die Stichwortabfrage als auch eine oder mehrere Bedingungen erfüllen müssen, die in die Ergebnisse eingeschlossen werden sollen. Auf diese Weise können Sie Ihre Ergebnisse einschränken. Eine Liste und Beschreibung der Bedingungen, die Sie in einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchbedingungen" in [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="8b2a9-p104">You can add search conditions to narrow a search and return a more refined set of results. Each condition adds a clause to the search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator. That means that items have to satisfy both the keyword query and one or more conditions to be included in the results. This is how conditions help to narrow your results. For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


