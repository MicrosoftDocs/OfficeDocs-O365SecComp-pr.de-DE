---
title: Erstellen von Suchabfragen
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
ms.openlocfilehash: c337b49491fca11e0ba5bc13d22ac3e54038c400
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695071"
---
# <a name="build-search-queries"></a><span data-ttu-id="d87a8-102">Erstellen von Suchabfragen</span><span class="sxs-lookup"><span data-stu-id="d87a8-102">Build search queries</span></span>

<span data-ttu-id="d87a8-103">In der Abfrage erstellen, können Sie verschiedene Schlüsselwörter und Bedingungen um zu definieren, welche Elemente gefunden verwenden.</span><span class="sxs-lookup"><span data-stu-id="d87a8-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="d87a8-104">Schlüsselwortsuchen</span><span class="sxs-lookup"><span data-stu-id="d87a8-104">Keyword searches</span></span>

<span data-ttu-id="d87a8-p101">Geben Sie im Feld **Stichwörter** eine Suchabfrage. Sie können angeben, Schlüsselwörter, Nachricht Eigenschaften wie gesendet und empfangen, Datumsangaben oder Dokumenteigenschaften wie Dateinamen oder das Datum, das ein Dokument zuletzt geändert wurde. Sie können eine komplexere Abfragen verwenden, die einen booleschen Operators, wie **AND**, **OR**, **nicht**und **NEAR**verwenden. Sie können auch suchen für vertrauliche Informationen (wie Sozialversicherungsnummern) in Dokumenten, oder suchen Sie nach Dokumenten, die extern freigegeben haben. Wenn Sie das Schlüsselwort Feld leer lassen, werden alle Inhalte, die in der angegebenen Speicherorte für Inhalte befindet sich in den Suchergebnissen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="d87a8-p101">Type a search query in **Keywords** box. You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed. You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**. You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally. If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="d87a8-p102">Alternativ können Sie das Kontrollkästchen **Schlüsselwortliste anzeigen** und den Typ ein Schlüsselworts in jede Zeile klicken. Wenn Sie dies tun, sind die Schlüsselwörter für jede Zeile ein logischer Operator ( **C:s**) vorhanden, die Funktionalität der **OR** -Operator in der Suchabfrage ähnlich ist, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="d87a8-p102">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row. If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="d87a8-p103">Gründe für die Verwendung der Schlüsselwortliste Sie können Statistiken abrufen, die zeigen, wie viele Elemente jedes Schlüsselwort überein. Dadurch können Sie schnell erkennen, welche Schlüsselwörter der am häufigsten (und mindestens) wirksam werden. Sie können auch eine Stichwortbegriff (in Klammern eingeschlossen sind) in einer Zeile. Weitere Informationen zu Suchstatistik finden Sie unter [Search-Statistik](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="d87a8-p103">Why use the keyword list? You can get statistics that show how many items match each keyword. This can help you quickly identify which keywords are the most (and least) effective. You can also use a keyword phrase (surrounded by parentheses) in a row. For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="d87a8-117">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="d87a8-117">Conditions</span></span>
    
<span data-ttu-id="d87a8-p104">Sie können die Suchkriterien, um eine Suche einzugrenzen und eine genauere Ergebnisse zurückgeben hinzufügen. Jede Bedingung hinzugefügt Search-Abfrage, die erstellt und ausgeführt werden, wenn Sie die Suche starten eine-Klausel. Eine Bedingung ist logisch mit der Stichwortabfrage (im Schlüsselwort angegeben) durch einen logischen Operator (**c: c**) verbunden, die an den **und** -Operator vergleichbar ist. Dies bedeutet, dass Elemente erfüllen der Stichwortabfrage und einen oder mehrere Bedingungen, die in den Ergebnissen berücksichtigt werden müssen. Dies ist die Bedingungen wie helfen, um Ihre Suchergebnisse einzuschränken. Eine Liste und eine Beschreibung der Bedingungen, die Sie bei einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchen Conditions" in [Stichwortabfragen und Suchkriterien für die Inhaltssuche](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="d87a8-p104">You can add search conditions to narrow a search and return a more refined set of results. Each condition adds a clause to the search query that is created and run when you start the search. A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator. That means that items have to satisfy both the keyword query and one or more conditions to be included in the results. This is how conditions help to narrow your results. For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


