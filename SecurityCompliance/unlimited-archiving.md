---
title: Übersicht über die uneingeschränkte Archivierung in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 37cdbb02-a24a-4093-8bdb-2a7f0b3a19ee
description: Erfahren Sie mehr über automatisch erweitert die Archivierung in Office 365, unbegrenzte Archivierung für Exchange Online-Postfächer enthält.
ms.openlocfilehash: a762a0fb8295a645957404c1c88881f40329f7a1
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782122"
---
# <a name="overview-of-unlimited-archiving-in-office-365"></a><span data-ttu-id="e49ad-103">Übersicht über die uneingeschränkte Archivierung in Office 365</span><span class="sxs-lookup"><span data-stu-id="e49ad-103">Overview of unlimited archiving in Office 365</span></span>

<span data-ttu-id="e49ad-p101">In Office 365 bieten archivpostfächer den Benutzern zusätzliche Postfach Speicherplatz. Nach dem Postfach eines Benutzers Archivieren aktiviert ist, ist bis zu 100 GB zusätzlicher Speicher verfügbar. Wenn das Speicherkontingent 100 GB erreicht ist, mussten wenden Sie sich an Microsoft zu Anforderung zusätzlicher Speicherplatz für ein Archivpostfach Organisationen. Dies ist nicht mehr der Fall. Das neue Feature der unbegrenzte Archivierung in Office 365 (bezeichnet *Archivierung erweiterbares*) bietet eine unbegrenzte an Speicherplatz in archivpostfächer. Nun, wenn das Speicherkontingent in das Archivpostfach erreicht ist, Office 365 wird automatisch erhöht, die Größe des Archivs, d. h., Benutzer werden nicht, nicht genügend Speicherplatz Postfach ausgeführt und Administratoren nicht zusätzlichen Speicher für archivpostfächer anfordern müssen .</span><span class="sxs-lookup"><span data-stu-id="e49ad-p101">In Office 365, archive mailboxes provide users with additional mailbox storage space. After a user's archive mailbox is enabled, up to 100 GB of additional storage is available. When the 100 GB storage quota is reached, organizations had to contact Microsoft to request additional storage space for an archive mailbox. That's no longer the case. The new unlimited archiving feature in Office 365 (called *auto-expanding archiving*) provides an unlimited amount of storage in archive mailboxes. Now, when the storage quota in the archive mailbox is reached, Office 365 automatically increases the size of the archive, which means that users won't run out of mailbox storage space and administrators won't have to request additional storage for archive mailboxes.</span></span>
  
<span data-ttu-id="e49ad-110">Für eine schrittweise Anleitung zum Aktivieren der automatischen Erweitern Archivierung, finden Sie unter [Aktivieren unbegrenzte Archivierung in Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="e49ad-110">For step-by-step instructions for turning on auto-expanding archiving, see [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="e49ad-p102">Erweiterbares auch Archivierung unterstützt freigegebene Postfächer. Um das Archiv für ein freigegebenes Postfach zu aktivieren, ist eine Lizenz für Exchange Online – Plan 2 oder eine Lizenz Exchange Online – Plan 1 mit Exchange Online-Archivierung-Lizenz erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e49ad-p102">Auto-expanding archiving also supports shared mailboxes. To enable the archive for a shared mailbox, an Exchange Online Plan 2 license or an Exchange Online Plan 1 license with an Exchange Online Archiving license is required.</span></span> 
  
## <a name="how-auto-expanding-archiving-works"></a><span data-ttu-id="e49ad-113">Funktionsweise der Archivierung wie erweiterbares</span><span class="sxs-lookup"><span data-stu-id="e49ad-113">How auto-expanding archiving works</span></span>

<span data-ttu-id="e49ad-p103">Wie bereits erklärt, zusätzliche Postfach wird Speicherplatz erstellt, wenn Archivpostfach des Benutzers aktiviert ist. Erweiterbares Archivierung aktiviert, prüft die Office 365 in regelmäßigen Abständen die Größe des archivpostfachs. Wenn ein Archivpostfach erreicht bald Speichergrenzwert erhält, erstellt Office 365 automatisch zusätzlicher Speicherplatz für das Archiv. Wenn der Benutzer nicht genügend diese zusätzlichen Speicherplatz ausgeführt wird, fügt Office 365 mehr Speicherplatz in Archiv des Benutzers an. Dieser Prozess wird automatisch, was bedeutet, dass Administratoren anfordern zusätzliche Archivspeicher oder Verwalten der Archivierung automatisch erweitert haben.</span><span class="sxs-lookup"><span data-stu-id="e49ad-p103">As previously explained, additional mailbox storage space is created when a user's archive mailbox is enabled. When auto-expanding archiving is enabled, Office 365 periodically checks the size of the archive mailbox. When an archive mailbox gets close to its storage limit, Office 365 automatically creates additional storage space for the archive. If the user runs out of this additional storage space, Office 365 adds more storage space to the user's archive. This process happens automatically, which means administrators don't have to request additional archive storage or manage auto-expanding archiving.</span></span> 
  
<span data-ttu-id="e49ad-119">Nachfolgend finden Sie ein schnellen Überblick über den Prozess.</span><span class="sxs-lookup"><span data-stu-id="e49ad-119">Here's a quick overview of the process.</span></span>
  
![Übersicht über die Archivierung automatisch erweitert](media/74355385-d990-44fe-8a87-6c3639d1f63f.png)
  
1. <span data-ttu-id="e49ad-p104">Archivierung ist für ein Benutzerpostfach oder ein freigegebenes Postfach aktiviert. Ein Archivpostfach mit 100 GB freier Speicherplatz wird erstellt, und das Warnung Kontingent für das Archivpostfach auf 90 GB festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e49ad-p104">Archiving is enabled for a user mailbox or a shared mailbox. An archive mailbox with 100 GB of storage space is created, and the warning quota for the archive mailbox is set to 90 GB.</span></span>
    
2. <span data-ttu-id="e49ad-p105">Ein Administrator kann erweiterbares Archivierung für das Postfach. Klicken Sie dann, wenn das Archivpostfach (einschließlich des Ordners wiederherstellbare Elemente) 90 GB erreicht, wird es in einem Archiv erweiterbares konvertiert und Office 365 fügt Speicherplatz in das Archiv. Beachten Sie, dass dauert bis zu 30 Tage für den zusätzlichen Speicherplatz bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e49ad-p105">An administrator enables auto-expanding archiving for the mailbox. Then, when the archive mailbox (including the Recoverable Items folder) reaches 90 GB, it's converted to an auto-expanding archive, and Office 365 adds storage space to the archive. Note that it can take up to 30 days for the additional storage space to be provisioned.</span></span>
    
3. <span data-ttu-id="e49ad-126">Office 365 fügt mehr Speicherplatz automatisch in das Archiv bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="e49ad-126">Office 365 automatically adds more storage space to the archive when necessary.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e49ad-p106">Wenn ein Postfach in die Warteschleife gestellt oder um eine Aufbewahrungsrichtlinie für Office 365 zugeordnet ist, wird das Speicherkontingent für die Archivierung Maibox auf 110 GB erhöht, wenn erweiterbares Archivierung aktiviert ist. Auf ähnliche Weise wird die Kontingentgrenzwert auf 100 GB erhöht.</span><span class="sxs-lookup"><span data-stu-id="e49ad-p106">If a mailbox is placed on hold or assigned to an Office 365 retention policy, the storage quota for the archive maibox is increased to 110 GB when auto-expanding archiving is enabled. Similarly, the archive warning quota is increased to 100 GB.</span></span>

## <a name="what-gets-moved-to-the-additional-archive-storage-space"></a><span data-ttu-id="e49ad-129">Was wird auf den Speicherplatz zusätzliche Archiv verschoben?</span><span class="sxs-lookup"><span data-stu-id="e49ad-129">What gets moved to the additional archive storage space?</span></span>

<span data-ttu-id="e49ad-p107">Um Archivspeicher erweiterbares effizient zu nutzen, möglicherweise Ordner verschoben werden. Office 365 wird bestimmt, welche Ordner verschoben, wenn das Archiv zusätzlicher Speicher hinzugefügt wird. Wenn ein Ordner verschoben wird, wird automatisch ein Unterordner unter dem ursprünglichen Ordner im Archiv Teil der Ordnerliste in Outlook erstellt. Diese neue Unterordner verweist auf die Elemente, die verschoben wurden. Die Benennungskonvention, die Office 365 wird verwendet, um nennen Sie diesen Ordner ist ** \<Ordnername\>_yyyy (auf erstellt mmm TT, JJJJ H_mm)**, wobei:</span><span class="sxs-lookup"><span data-stu-id="e49ad-p107">To make efficient use of auto-expanding archive storage, folders might get moved. Office 365 determines which folders get moved when additional storage is added to the archive. When a folder is moved, a subfolder is automatically created under the original folder in the archive portion of the folder list in Outlook. This new subfolder points to the items that were moved. The naming convention that Office 365 uses to name this folder is **\<folder name\>_yyyy (Created on mmm dd, yyyy h_mm)**, where:</span></span> 
  
- <span data-ttu-id="e49ad-135">**JJJJ** ist das Jahr, den, das die Nachrichten im Ordner empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="e49ad-135">**yyyy** is the year the messages in the folder were received.</span></span> 
    
- <span data-ttu-id="e49ad-136">**mmm TT, JJJJ H_m** ist das Datum und die Uhrzeit, die der Unterordner von Office 365, im UTC-Format, basierend auf der Zeitzone des Benutzers und der regionalen Einstellungen in Outlook erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e49ad-136">**mmm dd, yyyy h_m** is the date and time that the subfolder was created by Office 365, in UTC format, based on the user's time zone and regional settings in Outlook.</span></span> 
    
<span data-ttu-id="e49ad-137">Die folgenden Screenshots anzeigen eine Ordnerliste vor und nach Nachrichten in einem Archiv automatisch erweitert verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="e49ad-137">The following screen shots show a folder list before and after messages are moved in an auto-expanded archive.</span></span>
  
 <span data-ttu-id="e49ad-138">**Vor dem Hinzufügen zusätzlichen Speichers**</span><span class="sxs-lookup"><span data-stu-id="e49ad-138">**Before additional storage is added**</span></span>
  
![Ordnerliste Archivpostfach bevor erweiterbares Archiv bereitgestellt ist.](media/5d6d6420-e562-4912-aaab-1c111762b3f6.png)
  
 <span data-ttu-id="e49ad-140">**Nach dem Hinzufügen zusätzlichen Speichers**</span><span class="sxs-lookup"><span data-stu-id="e49ad-140">**After additional storage is added**</span></span>
  
![Ordnerliste Archivpostfach nach erweiterbares Archiv bereitgestellt ist.](media/c03c5f51-23fa-4fc2-b887-7e7e5cce30da.png)
  
## <a name="outlook-requirements-for-accessing-items-in-an-auto-expanded-archive"></a><span data-ttu-id="e49ad-142">Outlook-Anforderungen für den Zugriff auf Elemente in einem Archiv automatisch erweitert</span><span class="sxs-lookup"><span data-stu-id="e49ad-142">Outlook requirements for accessing items in an auto-expanded archive</span></span>

<span data-ttu-id="e49ad-143">Um Nachrichten zugreifen, die in einem Archiv automatisch erweitert gespeichert sind, müssen Benutzer eine der folgenden Outlook-Clients verwenden:</span><span class="sxs-lookup"><span data-stu-id="e49ad-143">To access messages that are stored in an auto-expanded archive, users have to use one of the following Outlook clients:</span></span>
  
- <span data-ttu-id="e49ad-144">Outlook 2016 für Windows</span><span class="sxs-lookup"><span data-stu-id="e49ad-144">Outlook 2016 for Windows</span></span>
    
- <span data-ttu-id="e49ad-145">Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="e49ad-145">Outlook on the web</span></span> 
    
- <span data-ttu-id="e49ad-146">Outlook 2016 für Mac</span><span class="sxs-lookup"><span data-stu-id="e49ad-146">Outlook 2016 for Mac</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e49ad-p108">Outlook 2013-Benutzer können nur Zugriff auf Elemente, die ursprünglich in ihre Archivpostfach gespeichert wurden. Sie werden kann nicht für den Zugriffselemente, die in zusätzliche Archivspeicher verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="e49ad-p108">Outlook 2013 users can only access items that were originally stored in their archive mailbox. They won't be able to access items that are moved to additional archive storage.</span></span> 
  
<span data-ttu-id="e49ad-149">Hier sind einige Punkte, berücksichtigen Sie beim Verwenden von Outlook oder Outlook im Web zum Zugriff auf Nachrichten in einem Archiv automatisch erweitert gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e49ad-149">Here are some things to consider when using Outlook or Outlook on the web to access messages stored in an auto-expanded archive.</span></span>
  
- <span data-ttu-id="e49ad-150">Sie können ein beliebiger Ordner im Archivpostfach, einschließlich Schriftarten, die in den Bereich für die automatische erweiterte Speicherung verschoben wurden zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e49ad-150">You can access any folder in your archive mailbox, including ones that were moved to the auto-expanded storage area.</span></span>
    
- <span data-ttu-id="e49ad-p109">Sie können nach Elementen suchen, die in einen Bereich zusätzlicher Speicher verschoben wurden, nur, indem Sie den Ordner selbst suchen. Dies bedeutet, dass Sie den Archivordner in Ordnerliste, um die **Aktuellen Ordner** als den Suchbereich auswählen aus. Enthält ein Ordner in einem automatisch erweitert Speicherbereich Unterordner, müssen Sie auf ähnliche Weise jedem Unterordner separat zu suchen.</span><span class="sxs-lookup"><span data-stu-id="e49ad-p109">You can search for items that were moved to an additional storage area only by searching the folder itself. This means you have to select the archive folder in the folder list to select the **Current Folder** option as the search scope. Similarly, if a folder in an auto-expanded storage area contains subfolders, you have to search each subfolder separately.</span></span> 
    
- <span data-ttu-id="e49ad-154">Anzahl der Element in Outlook und Lese-/ungelesen zählt (in Outlook und Outlook im Web) in einem Archiv automatisch erweitert ist möglicherweise nicht korrekt.</span><span class="sxs-lookup"><span data-stu-id="e49ad-154">Item counts in Outlook and Read/Unread counts (in Outlook and Outlook on the web ) in an auto-expanded archive might not be accurate.</span></span>
    
- <span data-ttu-id="e49ad-155">Sie können Löschen von Elementen in einem Unterordner, der auf einen Speicherbereich automatische erweitert verweist, aber der Ordner selbst kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e49ad-155">You can delete items in a subfolder that points to an auto-expanded storage area, but the folder itself can't be deleted.</span></span>
    
- <span data-ttu-id="e49ad-156">Sie können das Feature gelöschte Elemente wiederherstellen Wiederherstellen eines Elements, das in einem Speicher automatisch erweitert gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="e49ad-156">You can't use the Recover Deleted Items feature to recover an item that was deleted from an auto-expanded storage area.</span></span>
  
## <a name="auto-expanding-archiving-and-other-office-365-compliance-features"></a><span data-ttu-id="e49ad-157">Erweiterbares Archivierung und andere Office 365 Compliance-features</span><span class="sxs-lookup"><span data-stu-id="e49ad-157">Auto-expanding archiving and other Office 365 compliance features</span></span>

<span data-ttu-id="e49ad-158">In diesem Abschnitt wird die Funktionalität zwischen erweiterbares Archivierung und andere Office 365 Compliance und Daten Governance Features erläutert.</span><span class="sxs-lookup"><span data-stu-id="e49ad-158">This section explains the functionality between auto-expanding archiving and other Office 365 compliance and data governance features.</span></span>
  
- <span data-ttu-id="e49ad-159">**eDiscovery** - bei Verwendung ein Office 365 eDiscovery-Tools, z. B. Inhaltssuche oder Compliance-eDiscovery, die Bereiche zusätzlicher Speicher in einem Archiv automatisch erweitert werden ebenfalls durchsucht.</span><span class="sxs-lookup"><span data-stu-id="e49ad-159">**eDiscovery** - When you use an Office 365 eDiscovery tool, such as Content Search or In-Place eDiscovery, the additional storage areas in an auto-expanded archive are also searched.</span></span>
    
- <span data-ttu-id="e49ad-160">**Aufbewahrung** - Wenn Sie ein Postfach gehalten in Exchange Online mithilfe von Tools wie Aufbewahrung für eventuelle Rechtsstreitigkeiten oder eDiscovery-Fall Archive und Aufbewahrungsrichtlinien in die Office 365-Sicherheit &amp; Compliance Center, Inhalt befindet sich in einem Archiv automatisch erweitert ist auch in der Warteschleife platziert.</span><span class="sxs-lookup"><span data-stu-id="e49ad-160">**Retention** - When you put a mailbox on hold by using tools such as Litigation Hold in Exchange Online or eDiscovery case holds and retention policies in the Office 365 Security &amp; Compliance Center, content located in an auto-expanded archive is also placed on hold.</span></span>
    
- <span data-ttu-id="e49ad-161">**Messaging-datensatzverwaltung (MRM)** - Wenn Sie Löschrichtlinien MRM in Exchange Online verwenden, um abgelaufene Postfachelemente, befindet sich im Archiv automatisch erweitert abgelaufene Elemente endgültig löschen, werden ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="e49ad-161">**Messaging records management (MRM)** - If you use MRM deletion policies in Exchange Online to permanently delete expired mailbox items, expired items located in the auto-expanded archive will also be deleted.</span></span>
    
- <span data-ttu-id="e49ad-p110">**Importieren von Dienst** - Sie können den Dienst Office 365 importieren zum Importieren von PST-Dateien des Benutzers automatisch erweitert Archiv verwenden. Sie können bis zu 100 GB an Daten aus PST-Dateien in Archivpostfach des Benutzers importieren.</span><span class="sxs-lookup"><span data-stu-id="e49ad-p110">**Import service** - You can use the Office 365 Import service to import PST files to a user's auto-expanded archive. You can import up to 100 GB of data from PST files to the user's archive mailbox.</span></span> 

## <a name="more-information"></a><span data-ttu-id="e49ad-164">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e49ad-164">More information</span></span>

<span data-ttu-id="e49ad-165">Ausführliche technische Informationen zur Archivierung, finden Sie unter erweiterbares [Office 365: Archive – häufig gestellte Fragen erweiterbares](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span><span class="sxs-lookup"><span data-stu-id="e49ad-165">For more technical details about auto-expanding archiving, see [Office 365: Auto-Expanding Archives FAQ](https://blogs.technet.microsoft.com/exchange/2018/04/09/office-365-auto-expanding-archives-faq/).</span></span>