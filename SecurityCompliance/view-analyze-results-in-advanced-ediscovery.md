---
title: Anzeigen von Analyseergebnissen in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 5974f3c2-89fe-4c5f-ac7b-57f214437f7e
description: 'Hier erfahren Sie, wo die Ergebnisse des Analyseprozesses in Office 365 Advanced eDiscovery angezeigt werden, einschließlich Definitionen der angezeigten Aufgabenoptionen.  '
ms.openlocfilehash: 990bcbb3c6626521d40f7ce057c764200d5047b5
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32267105"
---
# <a name="view-analyze-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="29dea-103">Anzeigen von Analyseergebnissen in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="29dea-103">View Analyze results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="29dea-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="29dea-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="29dea-106">In Advanced eDiscovery können Fortschritte und Ergebnisse für den Analyseprozess in einer Vielzahl von Displays angezeigt werden, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="29dea-106">In Advanced eDiscovery, progress and results for the Analyze process can be viewed in a variety of displays as described below.</span></span>
  
## <a name="view-analyze-task-status"></a><span data-ttu-id="29dea-107">Anzeigen des Vorgangsstatus</span><span class="sxs-lookup"><span data-stu-id="29dea-107">View Analyze task status</span></span>

<span data-ttu-id="29dea-108">In **Prepare \> analyze \> results \> Task Status**wird der Status während und nach der Analyse der Prozessausführung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29dea-108">In **Prepare \> Analyze \> Results \> Task status**, the status is displayed during and after Analyze process execution.</span></span> 
  
![Aufgabenstatus analysieren](media/d0372978-ce08-4f4e-a1fc-aa918ae44364.png)
  
<span data-ttu-id="29dea-110">Welche Aufgaben angezeigt werden, hängt von den ausgewählten Optionen ab.</span><span class="sxs-lookup"><span data-stu-id="29dea-110">The tasks displayed may vary depending on the options selected.</span></span> 
  
- <span data-ttu-id="29dea-111">**ND/et: Setup**: Prepares for the Run, beispielsweise legt die Parameter Run und Case fest.</span><span class="sxs-lookup"><span data-stu-id="29dea-111">**ND/ET: setup**: Prepares for the run, for example, sets run and case parameters.</span></span>
    
- <span data-ttu-id="29dea-112">**ND/et: ND-Berechnung**: verarbeitet die nahezu duplizierte Analyse von Dateien.</span><span class="sxs-lookup"><span data-stu-id="29dea-112">**ND/ET: ND calculation**: Processes Near-duplicate analysis of files.</span></span>
    
- <span data-ttu-id="29dea-113">**ND/et: et-Berechnung**: führt eine e-Mail-Thread Analyse für den gesamten e-Mail-Satz durch.</span><span class="sxs-lookup"><span data-stu-id="29dea-113">**ND/ET: ET calculation**: Performs Email Thread analysis on the entire email set.</span></span>
    
- <span data-ttu-id="29dea-114">**ND/et: Pivots und Ähnlichkeiten**: führt Pivot-und Datei Ähnlichkeits Verarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="29dea-114">**ND/ET: pivots and similarities**: Performs pivot and file similarity processing.</span></span>
    
- <span data-ttu-id="29dea-115">**ND/et: Metadata Update**: finalisiert die neuen Daten, die für die Dateien in der Datenbank gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="29dea-115">**ND/ET: metadata update**: Finalizes the new data collected on the files in the database.</span></span>
    
- <span data-ttu-id="29dea-116">**Designs: Design Berechnung**: führt die Design Analyse aus.</span><span class="sxs-lookup"><span data-stu-id="29dea-116">**Themes: themes calculation**: Runs themes analysis.</span></span> <span data-ttu-id="29dea-117">(Nur angezeigt, wenn ausgewählt.)</span><span class="sxs-lookup"><span data-stu-id="29dea-117">(Displayed only if selected.)</span></span>
    
- <span data-ttu-id="29dea-118">**Vorgangsstatus**: diese Leitung wird nach Abschluss der Aufgabe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29dea-118">**Task status**: This line is displayed after task completion.</span></span> <span data-ttu-id="29dea-119">Während Vorgänge ausgeführt werden, wird die Ausführungsdauer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29dea-119">While tasks are running, run duration is displayed.</span></span>
    
> [!NOTE]
> <span data-ttu-id="29dea-120">Die Analyseergebnisse von Near-Duplikaten und e-Mail-Threads (ND und ED) beziehen sich auf die Anzahl der zu verarbeitenden Dokumente.</span><span class="sxs-lookup"><span data-stu-id="29dea-120">The Analyze results of Near-duplicates and Email Threads (ND and ED) applies to the number of documents to be processed.</span></span> <span data-ttu-id="29dea-121">Es enthält nicht exakte Duplikatdateien.</span><span class="sxs-lookup"><span data-stu-id="29dea-121">It does not include Exact duplicate files.</span></span> 
  
## <a name="view-near-duplicates-and-email-threads-status"></a><span data-ttu-id="29dea-122">Anzeigen von Near-Duplikaten und e-Mail-Threads Status</span><span class="sxs-lookup"><span data-stu-id="29dea-122">View Near-duplicates and Email Threads status</span></span>

<span data-ttu-id="29dea-123">Die Ergebnisse der **Ziel** Auffüllung zeigen die Anzahl von Dokumenten, e-Mails, Anlagen und Fehlern in der Zielauffüllung an.</span><span class="sxs-lookup"><span data-stu-id="29dea-123">The **Target** population results display the number of documents, emails, attachments, and errors in the target population.</span></span> 
  
<span data-ttu-id="29dea-124">Die Ergebnisse der **Dokumente** zeigen die Anzahl der Pivots, die eindeutigen Duplikate und die exakten doppelten Dateien an.</span><span class="sxs-lookup"><span data-stu-id="29dea-124">The **Documents** results display the number of pivots, unique near-duplicates, and exact duplicate files.</span></span> 
  
<span data-ttu-id="29dea-125">In \*\*\*\* den e-Mail-Ergebnissen wird die Anzahl der inklusiv-inklusive-minus-, Unique-inklusive-Kopien und die restlichen e-Mails angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29dea-125">The **Emails** results display the number of inclusive, inclusive minus, unique inclusive copies, and the rest of the email messages.</span></span> <span data-ttu-id="29dea-126">Die verschiedenen Typen von e-Mail-Ergebnissen sind:</span><span class="sxs-lookup"><span data-stu-id="29dea-126">The different types of email results are:</span></span> 
  
- <span data-ttu-id="29dea-127">**Inclusive**: eine inklusive e-Mail ist der abschließende Knoten in einem e-Mail-Thread und enthält alle vorherigen Verlauf dieses Threads.</span><span class="sxs-lookup"><span data-stu-id="29dea-127">**Inclusive**: An inclusive email is the terminating node in an email thread and contains all the previous history of that thread.</span></span> <span data-ttu-id="29dea-128">Daher kann der Prüfer sich sicher auf die inklusive e-Mail konzentrieren, ohne die vorherigen Nachrichten im Thread lesen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="29dea-128">As a result, the reviewer can safely focus on the inclusive email, without the need to read the previous messages in the thread.</span></span> 
    
- <span data-ttu-id="29dea-129">**Inklusive minus**: eine inklusiv-e-Mail wird als inklusive minus festgelegt, wenn es eine oder mehrere verschiedene Anlagen gibt, die den Eltern der Inclusive-Nachricht zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="29dea-129">**Inclusive minus**: An inclusive email is designated as inclusive minus if there are one or more different attachments associated with the parents of the inclusive message.</span></span> <span data-ttu-id="29dea-130">In diesem Kontext wird der Begriff Parent für Nachrichten verwendet, die sich nach oben im e-Mail-Thread oder Unterhaltungen befinden, die in dieser spezifischen inclusive-e-Mail enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="29dea-130">In this context, the term Parent is used for messages located upwards on the email thread or conversations included in that specific inclusive email.</span></span> <span data-ttu-id="29dea-131">Ein Prüfer kann die inklusive minus-Anzeige als Signal verwenden, dass es zwar nicht notwendig ist, den Inhalt der inklusiven e-Mail-Eltern zu überprüfen, es jedoch hilfreich sein kann, die Anlagen zu überprüfen, die mit den übergeordneten Pfad-Eltern verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="29dea-131">A reviewer can use the inclusive minus indication as a signal that although it might not be necessary to review the content of the inclusive email parents, it may be useful to review the attachments associated with the inclusive path parents.</span></span> 
    
- <span data-ttu-id="29dea-132">**Inklusive Kopie**: eine inklusiv-e-Mail wird als inklusive Kopie festgelegt, wenn es sich um die Kopie einer anderen Nachricht handelt, die als inklusive oder inklusive minus gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="29dea-132">**Inclusive copy**: An inclusive email is designated as inclusive copy if it's the copy of another message marked as inclusive or inclusive minus.</span></span> <span data-ttu-id="29dea-133">Anders ausgedrückt: Diese Nachricht hat denselben Betreff und Text wie eine andere inklusive Nachricht und befindet sich als solche im gleichen Knoten.</span><span class="sxs-lookup"><span data-stu-id="29dea-133">In other words, this message has the same subject and body as another inclusive message and, as such, co-resides in the same node.</span></span> <span data-ttu-id="29dea-134">Da inclusive Copy-Nachrichten denselben Inhalt enthalten, können Sie in der Regel beim Überprüfungsprozess übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="29dea-134">Because inclusive copy messages contain the same content, they can usually be skipped in the review process.</span></span> 
    
- <span data-ttu-id="29dea-135">**Der Rest**: Dies gibt e-Mails an, die keinen eindeutigen Inhalt enthalten und daher nicht in eine der vorherigen drei Kategorien fallen.</span><span class="sxs-lookup"><span data-stu-id="29dea-135">**The rest**: This indicates email that doesn't contain any unique content, and therefore doesn't fall into any of the previous three categories.</span></span> <span data-ttu-id="29dea-136">Diese e-Mail-Nachrichten müssen nicht überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="29dea-136">These email messages don't need to be reviewed.</span></span> <span data-ttu-id="29dea-137">Wenn eine Nachricht eine Anlage enthält, die nicht in einer späteren inclusive-e-Mail enthalten ist, muss die Anlage möglicherweise überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="29dea-137">If a message contains an attachment that isn't on a later inclusive email, then the attachment might need to be reviewed.</span></span> <span data-ttu-id="29dea-138">Dies wird durch das vorhanden sein einer inklusiven minus-e-Mail innerhalb des Threads angezeigt.</span><span class="sxs-lookup"><span data-stu-id="29dea-138">This is indicated by the existence of an inclusive minus email within the thread.</span></span>
    
<span data-ttu-id="29dea-139">Die Ergebnisse der **Anlagen** zeigen die Anzahl der Anlagen gemäß diesem Typ als Unique und Duplikate an.</span><span class="sxs-lookup"><span data-stu-id="29dea-139">The **Attachments** results display the number of attachments, according to such type as unique and duplicates.</span></span> 
  
![Near-Duplikate und e-Mail-Threads](media/54491303-0ee3-4739-b42e-d1ee486842fd.png)
  
## <a name="see-also"></a><span data-ttu-id="29dea-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29dea-141">See also</span></span>

[<span data-ttu-id="29dea-142">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="29dea-142">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="29dea-143">Grundlegendes zur Dokument Ähnlichkeit</span><span class="sxs-lookup"><span data-stu-id="29dea-143">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="29dea-144">Festlegen von Analyseoptionen</span><span class="sxs-lookup"><span data-stu-id="29dea-144">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="29dea-145">Festlegen des Texts ignorieren</span><span class="sxs-lookup"><span data-stu-id="29dea-145">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="29dea-146">Einstellung "Erweiterte Einstellungen analysieren"</span><span class="sxs-lookup"><span data-stu-id="29dea-146">Setting Analyze advanced settings</span></span>](view-analyze-results-in-advanced-ediscovery.md)

