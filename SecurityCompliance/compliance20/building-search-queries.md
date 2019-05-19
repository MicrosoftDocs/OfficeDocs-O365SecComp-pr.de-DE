---
title: Erstellen von Suchabfragen
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
ms.openlocfilehash: a33ecb6e1a2549b6bdc3bde9897b8a75e742b482
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151927"
---
# <a name="build-search-queries"></a><span data-ttu-id="23da7-102">Erstellen von Suchabfragen</span><span class="sxs-lookup"><span data-stu-id="23da7-102">Build search queries</span></span>

<span data-ttu-id="23da7-103">Bei der Erstellung Ihrer Abfrage können Sie verschiedene Schlüsselwörter und Bedingungen verwenden, um zu definieren, welche Elemente gesucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="23da7-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="23da7-104">Stichwortsuche</span><span class="sxs-lookup"><span data-stu-id="23da7-104">Keyword searches</span></span>

<span data-ttu-id="23da7-105">Geben Sie im Feld **Schlüsselwörter** eine Suchabfrage ein.</span><span class="sxs-lookup"><span data-stu-id="23da7-105">Type a search query in **Keywords** box.</span></span> <span data-ttu-id="23da7-106">Sie können Schlüsselwörter, Nachrichteneigenschaften , z. B. Sende- und Empfangsdatum, oder Dokumenteigenschaften angeben, z. B. Dateinamen oder das Datum der letzten Dokumentänderung.</span><span class="sxs-lookup"><span data-stu-id="23da7-106">You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed.</span></span> <span data-ttu-id="23da7-107">Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**und **near**.</span><span class="sxs-lookup"><span data-stu-id="23da7-107">You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="23da7-108">Sie können auch nach vertraulichen Informationen (wie etwa Sozialversicherungsnummern) in Dokumenten suchen oder nach Dokumenten suchen, die extern freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="23da7-108">You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally.</span></span> <span data-ttu-id="23da7-109">Wenn Sie das Feld Schlüsselwort leer lassen, werden alle Inhalte, die sich an den angegebenen Inhaltsspeicherorten befinden, in die Suchergebnisse eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="23da7-109">If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="23da7-110">Alternativ können Sie auf das Kontrollkästchen **Keyword-Liste anzeigen** und in jede Zeile ein Schlüsselwort eingeben.</span><span class="sxs-lookup"><span data-stu-id="23da7-110">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row.</span></span> <span data-ttu-id="23da7-111">Wenn Sie dies tun, werden die Schlüsselwörter für jede Zeile durch einen logischen Operator ( **c:s**) verbunden, der in der Funktionalität des **or** -Operators in der erstellten Suchabfrage ähnelt.</span><span class="sxs-lookup"><span data-stu-id="23da7-111">If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="23da7-112">Gründe für die Verwendung der Stichwortliste</span><span class="sxs-lookup"><span data-stu-id="23da7-112">Why use the keyword list?</span></span> <span data-ttu-id="23da7-113">Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit den einzelnen Schlüsselwörtern übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="23da7-113">You can get statistics that show how many items match each keyword.</span></span> <span data-ttu-id="23da7-114">Auf diese Weise können Sie schnell erkennen, welche Stichwörter am häufigsten (und am wenigsten) effektiv sind.</span><span class="sxs-lookup"><span data-stu-id="23da7-114">This can help you quickly identify which keywords are the most (and least) effective.</span></span> <span data-ttu-id="23da7-115">Sie können auch eine Stichwort Phrase (umgeben von Klammern) in einer Zeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="23da7-115">You can also use a keyword phrase (surrounded by parentheses) in a row.</span></span> <span data-ttu-id="23da7-116">Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistik](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="23da7-116">For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="23da7-117">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="23da7-117">Conditions</span></span>
    
<span data-ttu-id="23da7-118">Sie können Suchbedingungen hinzufügen, um eine Suche einzuschränken und eine verfeinerte Ergebnismenge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="23da7-118">You can add search conditions to narrow a search and return a more refined set of results.</span></span> <span data-ttu-id="23da7-119">Jede Bedingung fügt der Suchabfrage, die erstellt und ausgeführt wird, eine Klausel hinzu, wenn Sie die Suche starten.</span><span class="sxs-lookup"><span data-stu-id="23da7-119">Each condition adds a clause to the search query that is created and run when you start the search.</span></span> <span data-ttu-id="23da7-120">Eine Bedingung ist logisch mit der Stichwortabfrage (im Feld Schlüsselwort angegeben) durch einen logischen Operator (**c:c**) verbunden, der in der Funktionalität des **and-** Operators ähnelt.</span><span class="sxs-lookup"><span data-stu-id="23da7-120">A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator.</span></span> <span data-ttu-id="23da7-121">Das bedeutet, dass Elemente sowohl die Stichwortabfrage als auch eine oder mehrere Bedingungen erfüllen müssen, die in den Ergebnissen enthalten sein sollen.</span><span class="sxs-lookup"><span data-stu-id="23da7-121">That means that items have to satisfy both the keyword query and one or more conditions to be included in the results.</span></span> <span data-ttu-id="23da7-122">Auf diese Weise können Sie Ihre Ergebnisse mit Bedingungen eingrenzen.</span><span class="sxs-lookup"><span data-stu-id="23da7-122">This is how conditions help to narrow your results.</span></span> <span data-ttu-id="23da7-123">Eine Liste und eine Beschreibung der Bedingungen, die Sie in einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchbedingungen" unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="23da7-123">For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


