---
title: Abfragen der Daten in einem Übersichts Satz
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
ms.openlocfilehash: 395cc01238f4dbc91de5dd652e10121f5e0cc926
ms.sourcegitcommit: 4ce350f8f3eb597587945a8ac9b33e9793440c64
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/01/2019
ms.locfileid: "33527174"
---
# <a name="query-the-data-in-a-review-set"></a><span data-ttu-id="180eb-102">Abfragen der Daten in einem Übersichts Satz</span><span class="sxs-lookup"><span data-stu-id="180eb-102">Query the data in a review set</span></span>

<span data-ttu-id="180eb-103">In den meisten Fällen ist es hilfreich, tiefer in die in einem Übersichts Satz zu überprüfenden Inhalte einzudringen und diese effizienter zu überarbeiten.</span><span class="sxs-lookup"><span data-stu-id="180eb-103">In most cases, it will be useful to be able to dig deeper into what is there in a review set and organize them to review more efficiently.</span></span> <span data-ttu-id="180eb-104">Mithilfe von Abfragen in einem Übersichts Satz können Sie sich auf eine Teilmenge von Dokumenten konzentrieren, die den von Ihnen festgelegten Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="180eb-104">Queries within a review set enables you to do so by letting you focus on a subset of documents that meet the criteria defined by you at once.</span></span>

## <a name="creating-and-running-a-query-within-a-review-set"></a><span data-ttu-id="180eb-105">Erstellen und Durchführen einer Abfrage in einem Übersichts Satz</span><span class="sxs-lookup"><span data-stu-id="180eb-105">Creating and running a query within a review set</span></span>

<span data-ttu-id="180eb-106">Klicken Sie im Übersichts Satz auf "neue Abfrage", um eine Abfrage in Ihrem Übersichts Satz zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="180eb-106">In order to create and run a query within your review set, click on "New Query" in your review set.</span></span> <span data-ttu-id="180eb-107">Nachdem Sie die Abfrage benannt und die Bedingungen definiert haben, klicken Sie auf "Speichern", um die Abfrage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="180eb-107">After you name your query and define the conditions, click "Save" to run the query.</span></span> <span data-ttu-id="180eb-108">Klicken Sie zum Ausführen einer zuvor gespeicherten Abfrage einfach auf die gespeicherte Abfrage.</span><span class="sxs-lookup"><span data-stu-id="180eb-108">To run a query that has been previously saved, simply click on the saved query.</span></span> <span data-ttu-id="180eb-109">Eine Liste der Metadaten, nach denen Sie suchen können, finden Sie unter [Document Metadata fields](document-metadata-fields.md) .</span><span class="sxs-lookup"><span data-stu-id="180eb-109">Refer to [Document metadata fields](document-metadata-fields.md) for a list of metadata you can search by.</span></span>

## <a name="building-your-query"></a><span data-ttu-id="180eb-110">Erstellen der Abfrage</span><span class="sxs-lookup"><span data-stu-id="180eb-110">Building your query</span></span>

<span data-ttu-id="180eb-111">Sie können Ihre Abfrage mit einer Kombination aus Bedingungs Karten und Abfragesprache in der Bedingungs Karte für Schlüsselwörter erstellen.</span><span class="sxs-lookup"><span data-stu-id="180eb-111">You can build your query using a combination of condition cards and query language in the Keywords condition card.</span></span> <span data-ttu-id="180eb-112">Sie können Bedingungs Karten als Block gruppieren, um eine komplexere Abfrage zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="180eb-112">You can group condition cards together as a block to craft a more complex query.</span></span>

### <a name="condition-card"></a><span data-ttu-id="180eb-113">Bedingungs Karte</span><span class="sxs-lookup"><span data-stu-id="180eb-113">Condition card</span></span>

<span data-ttu-id="180eb-114">Jedes durchsuchbare Feld in einem Übersichts Satz verfügt über eine entsprechende Konditions Karte, die Sie zum Erstellen der Abfrage verwenden können.</span><span class="sxs-lookup"><span data-stu-id="180eb-114">Every searchable field in a review set has a corresponding condition card that you can use to build your query.</span></span>

<span data-ttu-id="180eb-115">Es gibt mehrere Arten von Bedingungs Karten:</span><span class="sxs-lookup"><span data-stu-id="180eb-115">There are multiple types of condition cards:</span></span>
- <span data-ttu-id="180eb-116">FREETEXT: FREETEXT-Bedingungs Karte wird für Textfelder wie Subject verwendet.</span><span class="sxs-lookup"><span data-stu-id="180eb-116">Freetext: freetext condition card is used for text fields such as subject.</span></span> <span data-ttu-id="180eb-117">Sie können mehrere Suchbegriffe auflisten, indem Sie Sie mit einem Komma voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="180eb-117">You can list multiple search terms by separating them out with a comma.</span></span>
- <span data-ttu-id="180eb-118">Datum: die Bedingungs Karte für das Datum wird für Datumsfelder wie Datum der letzten Änderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="180eb-118">Date: date condition card is used for date fields such as last modified date.</span></span>
- <span data-ttu-id="180eb-119">Suchoptionen: die Bedingungs Karte für Suchoptionen enthält eine Liste der möglichen Werte für das jeweilige Feld in Ihrem Übersichts Satz.</span><span class="sxs-lookup"><span data-stu-id="180eb-119">Search options: search options condition card will provide a list of possible values for the particular field in your review set.</span></span> <span data-ttu-id="180eb-120">Dieser Wert wird für Felder wie "Sender" verwendet, bei denen eine begrenzte Anzahl von möglichen Werten in Ihrem Übersichts Satz vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="180eb-120">This is used for fields, such as sender, where there is a finite number of possible values in your review set.</span></span>
- <span data-ttu-id="180eb-121">Stichwort: Stichwort Bedingungs Karte ist eine bestimmte Instanz von FREETEXT-Bedingungs Karte, die Sie für die Suche nach Begriffen verwenden können, oder verwenden Sie die KQL-ähnliche Abfragesprache in.</span><span class="sxs-lookup"><span data-stu-id="180eb-121">Keyword: keyword condition card is a specific instance of freetext condition card that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="180eb-122">Weitere Informationen finden Sie weiter unten.</span><span class="sxs-lookup"><span data-stu-id="180eb-122">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="180eb-123">Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="180eb-123">Query language</span></span>

<span data-ttu-id="180eb-124">Zusätzlich zu den Bedingungs Karten können Sie eine KQL-ähnliche Abfragesprache in der Stichwörter Karte verwenden, um Ihre Abfrage zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="180eb-124">In addition to condition cards, you can use a KQL-like query language in the Keywords card to craft your query.</span></span> <span data-ttu-id="180eb-125">Die Abfragesprache unterstützt die standardmäßige KQL-Syntax wie and, or, Not und Near (n).</span><span class="sxs-lookup"><span data-stu-id="180eb-125">The query language supports standard KQL syntax like AND, OR, NOT, and NEAR(n).</span></span> <span data-ttu-id="180eb-126">Außerdem werden Platzhalter mit einem Zeichen (?) und Platzhalter mit mehreren Zeichen (\*) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="180eb-126">It also supports single-character wildcard (?) and multi-character wildcard (\*).</span></span>

## <a name="filter"></a><span data-ttu-id="180eb-127">Filter</span><span class="sxs-lookup"><span data-stu-id="180eb-127">Filter</span></span>

<span data-ttu-id="180eb-128">Zusätzlich zu den Abfragen, die Sie speichern können, können Sie mithilfe von Filtern zusätzliche Bedingungen direkt an die Abfrageergebnisse überlagern.</span><span class="sxs-lookup"><span data-stu-id="180eb-128">In addition to queries that you can save, you can overlay additional conditions on the fly to your query results using filters.</span></span> <span data-ttu-id="180eb-129">Filter unterscheiden sich von Abfragen in einigen wichtigen Bereichen:</span><span class="sxs-lookup"><span data-stu-id="180eb-129">Filters differ from queries in a few significant ways:</span></span>
- <span data-ttu-id="180eb-130">Filter sind vorübergehend (d. h., Sie werden nicht über verschiedene Sitzungen beibehalten), während Abfragen im Übersichts Satz gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="180eb-130">Filters are transient (i.e. they do not persist over different sessions), whereas queries are saved to the review set.</span></span>
- <span data-ttu-id="180eb-131">Filter sind immer Additiv; Filter gelten im oberen Bereich der Abfrage, die Sie derzeit anwenden, wohingegen durch das Anwenden einer Abfrage die Abfrage wirksam ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="180eb-131">Filters are always additive; filters will apply on top of the query you have in effect at the moment, whereas applying a query will replace the query in effect.</span></span>