---
title: Analysieren von Daten in einer Überprüfungsgruppe in Advanced eDiscovery
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
ms.openlocfilehash: cfed07d473f2af367de4cb2e9fe924a29e4123cd
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155207"
---
# <a name="analyze-data-in-a-review-set-in-advanced-ediscovery"></a><span data-ttu-id="68931-102">Analysieren von Daten in einer Überprüfungsgruppe in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="68931-102">Analyze data in a review set in Advanced eDiscovery</span></span>

<span data-ttu-id="68931-103">Wenn die Anzahl der gesammelten Dokumente groß ist, kann es sehr schwierig sein, Sie alle zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="68931-103">When the number of collected documents is large, it can be quite difficult to review them all.</span></span> <span data-ttu-id="68931-104">Advanced eDiscovery stellt eine Reihe von Tools zum Analysieren der Dokumente zur Verfügung, um das Volumen von Dokumenten zu reduzieren, die ohne Verlust von Informationen überprüft werden sollen, und um Ihnen dabei zu helfen, die Dokumente auf kohärente Weise zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="68931-104">Advanced eDiscovery provides a number of tools to analyze the documents to reduce the volume of documents to be reviewed without any loss in information, and to help you organize the documents in a coherent manner.</span></span> <span data-ttu-id="68931-105">Weitere Informationen zu diesen Funktionen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="68931-105">To learn more about these capabilities, see:</span></span>

- [<span data-ttu-id="68931-106">Erkennen von Quasiduplikaten</span><span class="sxs-lookup"><span data-stu-id="68931-106">Near duplicate detection</span></span>](near-duplicates.md)

- [<span data-ttu-id="68931-107">E-Mail-Threading</span><span class="sxs-lookup"><span data-stu-id="68931-107">Email threading</span></span>](email-threading.md)

- [<span data-ttu-id="68931-108">Designs</span><span class="sxs-lookup"><span data-stu-id="68931-108">Themes</span></span>](themes.md)

<span data-ttu-id="68931-109">So analysieren Sie Daten in einem Überprüfungs Satzes:</span><span class="sxs-lookup"><span data-stu-id="68931-109">To analyze data in a review set:</span></span>

1. <span data-ttu-id="68931-110">Konfigurieren Sie die Analyse Einstellungen für Ihren Fall.</span><span class="sxs-lookup"><span data-stu-id="68931-110">Configure analytics settings for your case.</span></span> <span data-ttu-id="68931-111">Weitere Informationen finden Sie unter [Configure Search and Analytics Settings](configure-search-analytics-settings.md).</span><span class="sxs-lookup"><span data-stu-id="68931-111">For more information, see [Configure search and analytics settings](configure-search-analytics-settings.md).</span></span>

2. <span data-ttu-id="68931-112">Öffnen Sie den Überprüfungs Satzes, den Sie analysieren möchten.</span><span class="sxs-lookup"><span data-stu-id="68931-112">Open the review set you want to analyze.</span></span>

3. <span data-ttu-id="68931-113">Klicken Sie auf Überprüfungs **Sätze verwalten**.</span><span class="sxs-lookup"><span data-stu-id="68931-113">Click **Manage review set**.</span></span>

4. <span data-ttu-id="68931-114">Klicken Sie auf **analysieren**.</span><span class="sxs-lookup"><span data-stu-id="68931-114">Click **Analyze**.</span></span>

<span data-ttu-id="68931-115">Sie können den Fortschritt der Analyse auf der Registerkarte **Aufträge** der Anfrage überprüfen.</span><span class="sxs-lookup"><span data-stu-id="68931-115">You can check the progress of analysis on the **Jobs** tab of the case.</span></span>

 <span data-ttu-id="68931-116">Nachdem die Analyse abgeschlossen ist, können Sie den Analysebericht anzeigen, Abfragen in ihrer Überprüfung ausführen, die auf Ausgaben der Analyse festgelegt sind (siehe [Abfrage innerhalb](review-set-search.md)des Überprüfungs Satzes) und verwandte Dokumente eines bestimmten Dokuments anzeigen (siehe Überprüfen von [Daten im](reviewing-data-in-review-set.md)Überprüfungs).</span><span class="sxs-lookup"><span data-stu-id="68931-116">After analysis is completed, you can view analytics report, run queries within your review set on outputs of the analysis (see [Query within your review set](review-set-search.md)), and see related documents of a given document (see [Reviewing data in review set](reviewing-data-in-review-set.md)).</span></span>

## <a name="analytics-report"></a><span data-ttu-id="68931-117">Analysebericht</span><span class="sxs-lookup"><span data-stu-id="68931-117">Analytics report</span></span>

<span data-ttu-id="68931-118">So zeigen Sie einen Analysebericht für eine Überprüfungsgruppe an:</span><span class="sxs-lookup"><span data-stu-id="68931-118">To view a analytics report for a review set:</span></span>

1. <span data-ttu-id="68931-119">Öffnen Sie den Überprüfungs-Datensatz.</span><span class="sxs-lookup"><span data-stu-id="68931-119">Open the review set.</span></span>

2. <span data-ttu-id="68931-120">Klicken Sie auf Überprüfungs **Sätze verwalten**.</span><span class="sxs-lookup"><span data-stu-id="68931-120">Click **Manage review set**.</span></span>

3. <span data-ttu-id="68931-121">Klicken Sie auf **Bericht**.</span><span class="sxs-lookup"><span data-stu-id="68931-121">Click **Report**.</span></span>

<span data-ttu-id="68931-122">Der Bericht enthält vier Komponenten aus der Analyse:</span><span class="sxs-lookup"><span data-stu-id="68931-122">The report has four components from analysis:</span></span>

- <span data-ttu-id="68931-123">\*\*\*\* Aufschlüsselung – wie viele e-Mail-Nachrichten, Anlagen und lose Dokumente wurden im Überprüfungs Satz gefunden.</span><span class="sxs-lookup"><span data-stu-id="68931-123">**Breakdown** - How many email messages, attachments, and loose documents were found in the review set.</span></span>

- <span data-ttu-id="68931-124">**Dokumente (ohne Anlagen)** – wie viele Lose Dokumente waren Pivots, eindeutig in der Nähe von Duplikaten eines Pivots oder ein exaktes Duplikat eines anderen Dokuments.</span><span class="sxs-lookup"><span data-stu-id="68931-124">**Documents (excluding attachments)** - How many loose documents were pivots, unique near duplicates of a pivot, or an exact duplicate of another document.</span></span>

- <span data-ttu-id="68931-125">**E-Mails** -wie viele e-Mail-Nachrichten inklusive, einschließlich Kopien, einschließlich minus oder keines der oben genannten waren.</span><span class="sxs-lookup"><span data-stu-id="68931-125">**Emails** - How many email messages were inclusives, inclusive copies, inclusive minuses, or none of the above.</span></span>

- <span data-ttu-id="68931-126">**Attachments** -wie viele e-Mail-Anlagen wurden eindeutig oder Duplikate einer anderen e-Mail-Anlage in der Überprüfungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="68931-126">**Attachments** - How many email attachments were unique or duplicates of a another email attachment in the review set.</span></span>