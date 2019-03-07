---
title: Abfragen der Daten in einem Arbeitssatz
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
ms.openlocfilehash: 2523072181307cce510f0f318834329b2c70b376
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30454987"
---
# <a name="query-the-data-in-a-working-set"></a><span data-ttu-id="5bef7-102">Abfragen der Daten in einem Arbeitssatz</span><span class="sxs-lookup"><span data-stu-id="5bef7-102">Query the data in a working set</span></span>

<span data-ttu-id="5bef7-103">In den meisten Fällen ist es hilfreich, tiefer in die in einem Workingset enthaltenen Elemente einzudringen und diese effizienter zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="5bef7-103">In most cases, it will be useful to be able to dig deeper into what is there in a working set and organize them to review more efficiently.</span></span> <span data-ttu-id="5bef7-104">Mit Abfragen in einem Arbeitssatz können Sie sich auf eine Teilmenge von Dokumenten konzentrieren, die den von Ihnen definierten Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5bef7-104">Queries within a working set enables you to do so by letting you focus on a subset of documents that meet the criteria defined by you at once.</span></span>

## <a name="creating-and-running-a-query-within-a-working-set"></a><span data-ttu-id="5bef7-105">Erstellen und Durchführen einer Abfrage in einem Arbeitssatz</span><span class="sxs-lookup"><span data-stu-id="5bef7-105">Creating and running a query within a working set</span></span>

<span data-ttu-id="5bef7-106">Klicken Sie im Arbeitsbereich auf "neue Abfrage", um eine Abfrage in Ihrem Arbeitssatz zu erstellen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5bef7-106">In order to create and run a query within your working set, click on "New Query" in your working set.</span></span> <span data-ttu-id="5bef7-107">Nachdem Sie die Abfrage benannt und die Bedingungen definiert haben, klicken Sie auf "Speichern", um die Abfrage auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5bef7-107">After you name your query and define the conditions, click "Save" to run the query.</span></span> <span data-ttu-id="5bef7-108">Klicken Sie zum Ausführen einer zuvor gespeicherten Abfrage einfach auf die gespeicherte Abfrage.</span><span class="sxs-lookup"><span data-stu-id="5bef7-108">To run a query that has been previously saved, simply click on the saved query.</span></span> <span data-ttu-id="5bef7-109">Eine Liste der Metadaten, nach denen Sie suchen können, finden Sie unter [Document Metadata fields](document-metadata-fields.md) .</span><span class="sxs-lookup"><span data-stu-id="5bef7-109">Refer to [Document metadata fields](document-metadata-fields.md) for a list of metadata you can search by.</span></span>

## <a name="building-your-query"></a><span data-ttu-id="5bef7-110">Erstellen der Abfrage</span><span class="sxs-lookup"><span data-stu-id="5bef7-110">Building your query</span></span>

<span data-ttu-id="5bef7-111">Sie können Ihre Abfrage mit einer Kombination aus Bedingungs Karten und Abfragesprache in der Bedingungs Karte für Schlüsselwörter erstellen.</span><span class="sxs-lookup"><span data-stu-id="5bef7-111">You can build your query using a combination of condition cards and query language in the Keywords condition card.</span></span>

### <a name="condition-card"></a><span data-ttu-id="5bef7-112">Bedingungs Karte</span><span class="sxs-lookup"><span data-stu-id="5bef7-112">Condition card</span></span>

<span data-ttu-id="5bef7-113">Jedes durchsuchbare Feld in einem Arbeitssatz verfügt über eine entsprechende Konditions Karte, die Sie zum Erstellen der Abfrage verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5bef7-113">Every searchable field in a working set has a corresponding condition card that you can use to build your query.</span></span>

<span data-ttu-id="5bef7-114">Es gibt mehrere Arten von Bedingungs Karten:</span><span class="sxs-lookup"><span data-stu-id="5bef7-114">There are multiple types of condition cards:</span></span>
- <span data-ttu-id="5bef7-115">FREETEXT: FREETEXT-Bedingungs Karte wird für Textfelder wie Subject verwendet.</span><span class="sxs-lookup"><span data-stu-id="5bef7-115">Freetext: freetext condition card is used for text fields such as subject.</span></span> <span data-ttu-id="5bef7-116">Sie können mehrere Suchbegriffe auflisten, indem Sie Sie mit einem Komma voneinander trennen.</span><span class="sxs-lookup"><span data-stu-id="5bef7-116">You can list multiple search terms by separating them out with a comma.</span></span>
- <span data-ttu-id="5bef7-117">Datum: die Bedingungs Karte für das Datum wird für Datumsfelder wie Datum der letzten Änderung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5bef7-117">Date: date condition card is used for date fields such as last modified date.</span></span>
- <span data-ttu-id="5bef7-118">Suchoptionen: die Bedingungs Karte für Suchoptionen enthält eine Liste der möglichen Werte für das jeweilige Feld in Ihrem Arbeitssatz.</span><span class="sxs-lookup"><span data-stu-id="5bef7-118">Search options: search options condition card will provide a list of possible values for the particular field in your working set.</span></span> <span data-ttu-id="5bef7-119">Dies wird für Felder wie "Sender" verwendet, bei denen eine begrenzte Anzahl von möglichen Werten in Ihrem Workingset vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5bef7-119">This is used for fields such as sender, where there is a finite number of possible values in your working set.</span></span>
- <span data-ttu-id="5bef7-120">Stichwort: Stichwort Bedingungs Karte ist eine bestimmte Instanz von FREETEXT-Bedingungs Karte, die Sie für die Suche nach Begriffen verwenden können, oder verwenden Sie die KQL-ähnliche Abfragesprache in.</span><span class="sxs-lookup"><span data-stu-id="5bef7-120">Keyword: keyword condition card is a specific instance of freetext condition card that you can use to search for terms, or use KQL-like query language in.</span></span> <span data-ttu-id="5bef7-121">Weitere Informationen finden Sie weiter unten.</span><span class="sxs-lookup"><span data-stu-id="5bef7-121">See below for more detail.</span></span>

### <a name="query-language"></a><span data-ttu-id="5bef7-122">Abfragesprache</span><span class="sxs-lookup"><span data-stu-id="5bef7-122">Query language</span></span>

<span data-ttu-id="5bef7-123">Zusätzlich zu den Bedingungs Karten können Sie eine KQL-ähnliche Abfragesprache in der Stichwörter Karte verwenden, um Ihre Abfrage zu gestalten.</span><span class="sxs-lookup"><span data-stu-id="5bef7-123">In addition to condition cards, you can use a KQL-like query language in the Keywords card to craft your query.</span></span> <span data-ttu-id="5bef7-124">Die Abfragesprache unterstützt die standardmäßige KQL-Syntax wie AND, OR, NOT und NEAR (n).</span><span class="sxs-lookup"><span data-stu-id="5bef7-124">The query language supports standard KQL syntax like AND, OR, NOT, and NEAR(n).</span></span> <span data-ttu-id="5bef7-125">Außerdem werden Platzhalter mit einem Zeichen (?) und Platzhalter mit mehreren Zeichen (\*) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5bef7-125">It also supports single-character wildcard (?) and multi-character wildcard (\*).</span></span>