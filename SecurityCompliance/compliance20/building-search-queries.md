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
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: e62d486b102fa035ae21b379d30bb0657b82acc9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242503"
---
# <a name="build-search-queries"></a><span data-ttu-id="b340a-102">Erstellen von Suchabfragen</span><span class="sxs-lookup"><span data-stu-id="b340a-102">Build search queries</span></span>

<span data-ttu-id="b340a-103">Beim Erstellen einer Abfrage können Sie verschiedene Schlüsselwörter und Bedingungen verwenden, um zu definieren, welche Elemente gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="b340a-103">In building your query, you can use various keywords and conditions to define which items to find.</span></span>

## <a name="keyword-searches"></a><span data-ttu-id="b340a-104">Stichwortsuche</span><span class="sxs-lookup"><span data-stu-id="b340a-104">Keyword searches</span></span>

<span data-ttu-id="b340a-105">Geben Sie im Feld **Stichwörter** eine Suchabfrage ein.</span><span class="sxs-lookup"><span data-stu-id="b340a-105">Type a search query in **Keywords** box.</span></span> <span data-ttu-id="b340a-106">Sie können Schlüsselwörter, Nachrichteneigenschaften , z. B. Sende- und Empfangsdatum, oder Dokumenteigenschaften angeben, z. B. Dateinamen oder das Datum der letzten Dokumentänderung.</span><span class="sxs-lookup"><span data-stu-id="b340a-106">You can specify keywords, message properties such as sent and received dates, or document properties such as file names or the date that a document was last changed.</span></span> <span data-ttu-id="b340a-107">Sie können komplexere Abfragen verwenden, die einen booleschen Operator verwenden, beispielsweise **and**, **or**, **Not**und **near**.</span><span class="sxs-lookup"><span data-stu-id="b340a-107">You can use a more complex queries that use a Boolean operator, such as **AND**, **OR**, **NOT**, and **NEAR**.</span></span> <span data-ttu-id="b340a-108">Sie können auch nach vertraulichen Informationen (wie Sozialversicherungsnummern) in Dokumenten suchen oder nach Dokumenten suchen, die extern freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="b340a-108">You can also search for sensitive information (such as social security numbers) in documents, or search for documents that have been shared externally.</span></span> <span data-ttu-id="b340a-109">Wenn Sie das Schlüsselwortfeld leer lassen, werden alle Inhalte an den angegebenen Inhaltsspeicherorten in die Suchergebnisse eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b340a-109">If you leave the keyword box empty, all content located in the specified content locations will be included in the search results.</span></span>
    
<span data-ttu-id="b340a-110">Alternativ können Sie auf das Kontrollkästchen **Keyword-Liste anzeigen** klicken und in jeder Zeile ein Stichwort eingeben.</span><span class="sxs-lookup"><span data-stu-id="b340a-110">Alternatively, you can click the **Show keyword list** checkbox and the type a keyword in each row.</span></span> <span data-ttu-id="b340a-111">Wenn Sie dies tun, werden die Schlüsselwörter in jeder Zeile durch einen logischen Operator ( **c:s**) verbunden, der in der Funktionalität mit dem **or** -Operator in der erstellten Suchabfrage vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="b340a-111">If you do this, the keywords on each row are connected by a logical operator ( **c:s**) that is similar in functionality to the **OR** operator in the search query that's created.</span></span> 
    
<span data-ttu-id="b340a-112">Gründe für die Verwendung der Keyword-Liste</span><span class="sxs-lookup"><span data-stu-id="b340a-112">Why use the keyword list?</span></span> <span data-ttu-id="b340a-113">Sie können Statistiken abrufen, die zeigen, wie viele Elemente mit jedem Stichwort übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b340a-113">You can get statistics that show how many items match each keyword.</span></span> <span data-ttu-id="b340a-114">Auf diese Weise können Sie schnell erkennen, welche Schlüsselwörter am meisten (und am wenigsten) wirksam sind.</span><span class="sxs-lookup"><span data-stu-id="b340a-114">This can help you quickly identify which keywords are the most (and least) effective.</span></span> <span data-ttu-id="b340a-115">Sie können auch eine Schlüsselwortphrase (umgeben von Klammern) in einer Zeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="b340a-115">You can also use a keyword phrase (surrounded by parentheses) in a row.</span></span> <span data-ttu-id="b340a-116">Weitere Informationen zu Suchstatistiken finden Sie unter [Suchstatistik](search-statistics.md).</span><span class="sxs-lookup"><span data-stu-id="b340a-116">For more information about search statistics, see [Search statistic](search-statistics.md).</span></span>

## <a name="conditions"></a><span data-ttu-id="b340a-117">Bedingungen</span><span class="sxs-lookup"><span data-stu-id="b340a-117">Conditions</span></span>
    
<span data-ttu-id="b340a-118">Sie können Suchbedingungen hinzufügen, um eine Suche einzuschränken und eine genauere Ergebnismenge zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b340a-118">You can add search conditions to narrow a search and return a more refined set of results.</span></span> <span data-ttu-id="b340a-119">Jede Bedingung fügt eine Klausel zu der Suchabfrage hinzu, die erstellt und beim Starten der Suche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b340a-119">Each condition adds a clause to the search query that is created and run when you start the search.</span></span> <span data-ttu-id="b340a-120">Eine Bedingung ist logisch mit der Stichwortabfrage (angegeben im Stichwortfeld) durch einen logischen Operator (**c:c**) verbunden, der in der Funktionalität mit dem **and-** Operator vergleichbar ist.</span><span class="sxs-lookup"><span data-stu-id="b340a-120">A condition is logically connected to the keyword query (specified in the keyword box) by a logical operator (**c:c**) that is similar in functionality to the **AND** operator.</span></span> <span data-ttu-id="b340a-121">Dies führt dazu, dass Elemente sowohl die Stichwortabfrage als auch eine oder mehrere Bedingungen erfüllen müssen, die in die Ergebnisse eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b340a-121">That means that items have to satisfy both the keyword query and one or more conditions to be included in the results.</span></span> <span data-ttu-id="b340a-122">Auf diese Weise können Sie Ihre Ergebnisse mit Bedingungen eingrenzen.</span><span class="sxs-lookup"><span data-stu-id="b340a-122">This is how conditions help to narrow your results.</span></span> <span data-ttu-id="b340a-123">Eine Liste und Beschreibung der Bedingungen, die Sie in einer Suchabfrage verwenden können, finden Sie im Abschnitt "Suchbedingungen" in [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](../keyword-queries-and-search-conditions.md#search-conditions).</span><span class="sxs-lookup"><span data-stu-id="b340a-123">For a list and description of conditions that you can use in a search query, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](../keyword-queries-and-search-conditions.md#search-conditions).</span></span>


