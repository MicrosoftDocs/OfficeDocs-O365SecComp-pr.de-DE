---
title: Aktivieren von archivpostfächern in die Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Verwenden Sie die Office 365-Sicherheit &amp; Compliance Center um archivpostfächer zur Unterstützung Ihrer Organisation, Beibehaltung von eDiscovery, und halten Sie Anforderungen zu aktivieren.
ms.openlocfilehash: 1c290cf19b396221dac702efd1395911e8a51631
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "28327097"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="82ccc-103">Aktivieren von archivpostfächern in die Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="82ccc-103">Enable archive mailboxes in the Office 365 Security &amp; Compliance Center</span></span>
  
<span data-ttu-id="82ccc-p101">Archivierung in Office 365 (auch als Compliance-Archivierung bezeichnet) bietet Benutzern zusätzliche Postfach Speicherplatz. Nachdem Sie archivpostfächer aktivieren, Benutzer zugreifen und Speichern von Nachrichten in ihren archivpostfächern mithilfe von Microsoft Outlook und Outlook Web App-Benutzer können auch verschieben oder Kopieren von Nachrichten zwischen ihren primären Postfachs und deren Archivpostfach. Sie können auch aus dem Ordner wiederherstellbare Elemente in ihrem Archivpostfach gelöschte Elemente wiederherstellen, mit dem Tool gelöschte Elemente wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p101">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space. After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook Web App. Users can also move or copy messages between their primary mailbox and their archive mailbox. They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="82ccc-p102">Office 365 bietet eine unbegrenzte Zeitspanne Archivspeicher mit dem erweiterbares Archivierung Feature. Wenn erweiterbares Archivierung aktiviert ist, und klicken Sie dann das anfängliche Speicherkontingent im Archivpostfach des Benutzers erreicht ist, fügt zusätzlichen Speicherplatz automatisch von Office 365 hinzu. Dies bedeutet, die Benutzer werden nicht ausgeführt, nicht genügend Speicherplatz Postfach und Sie müssen nicht alles zunächst nach der verwalten aktivieren das Archivpostfach und schalten Sie erweiterbares Archivierung für Ihre Organisation. Weitere Informationen finden Sie unter [Übersicht über die uneingeschränkte Archivierung in Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="82ccc-p102">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature. When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space. This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization. For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="82ccc-112">Bevor Sie beginnen:</span><span class="sxs-lookup"><span data-stu-id="82ccc-112">Before you begin</span></span>

<span data-ttu-id="82ccc-p103">Sie müssen die Rolle des E-Mail-Empfänger in Exchange Online zu aktivieren oder Deaktivieren von archivpostfächern zugewiesen werden. Standardmäßig wird diese Rolle Rollengruppen "Recipient Management" und "Organisationsverwaltung" auf der Seite **Berechtigungen** in der Exchange-Verwaltungskonsole zugewiesen. Wenn Sie die Seite **Archiv** in das Wertpapier sehen &amp; Compliance Center, bitten Sie Ihren Administrator, um Sie über die erforderlichen Berechtigungen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p103">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes. By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. If you don't see the **Archive** page in the Security &amp; Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="82ccc-116">Aktivieren eines Archivpostfachs</span><span class="sxs-lookup"><span data-stu-id="82ccc-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="82ccc-117">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="82ccc-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="82ccc-118">Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="82ccc-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="82ccc-119">Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Governance** \> **Archiv**.</span><span class="sxs-lookup"><span data-stu-id="82ccc-119">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="82ccc-p104">Die Seite **Archiv** wird angezeigt. Die Spalte **Archivpostfach** gibt für jeden Benutzer an, ob das Archivpostfach aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p104">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="82ccc-122">Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="82ccc-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![Klicken Sie im Detailbereich des ausgewählten Benutzers an das Archivpostfach aktivieren auf Aktivieren](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="82ccc-124">Klicken Sie im Detailbereich für den ausgewählten Benutzer auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="82ccc-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="82ccc-p105">Eine Warnung wird angezeigt, die besagt, dass Elemente im Postfach des Benutzers, die älter sind als die Archivierungsrichtlinie Postfach zugeordnet sind, wenn Sie das Archivpostfach aktivieren, in das neue Archivpostfach verschoben werden sollen. Die Standardrichtlinie für das Archivieren, die Teil der Aufbewahrungsrichtlinie zu Exchange Online-Postfächern zugewiesen ist Verschiebt Elemente in das Archivpostfach zwei Jahre nach dem Datum, das der Artikel an das Postfach zugestellt oder vom Benutzer erstellt wurde. Weitere Informationen finden Sie im Abschnitt **Weitere Informationen** in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p105">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox. The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="82ccc-128">Klicken Sie auf **Ja**, um das Archivpostfach zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="82ccc-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="82ccc-p106">Es kann einen Moment, erstellen Sie das Archivpostfach dauern. Bei der Erstellung, **Archivpostfach: aktiviert** wird im Detailbereich für den ausgewählten Benutzer angezeigt. Möglicherweise müssen Sie auf **Aktualisieren** klicken ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p106">It might take a few moments to create the archive mailbox. When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="82ccc-p107">Sie können auch mehrere Archivpostfächer gleichzeitig aktivieren, indem Sie mehrere Benutzer mit deaktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="82ccc-134">Deaktivieren eines Archivpostfachs</span><span class="sxs-lookup"><span data-stu-id="82ccc-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="82ccc-p108">Sie können auch die Seite **Archiv** in das Wertpapier &amp; Compliance Center Archivpostfach des Benutzers zu deaktivieren. Wenn Sie ein Archivpostfach deaktiviert haben, können Sie sie zum primären Postfach des Benutzers innerhalb von 30 Tagen deaktivieren sie wieder herstellen. In diesem Fall werden der ursprüngliche Inhalt des archivpostfachs wiederhergestellt. Nach 30 Tagen wird der Inhalt des ursprünglichen archivpostfachs werden dauerhaft gelöscht und können nicht wiederhergestellt werden. Damit wird Sie das Archiv mehr als 30 Tage nach dem Deaktivieren wieder zu aktivieren, eine neue Archivpostfach erstellt.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p108">You can also use the **Archive** page in the Security &amp; Compliance Center to disable a user's archive mailbox. After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it. In this case, the original contents of the archive mailbox are restored. After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered. So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="82ccc-p109">Beachten Sie, dass die Standardrichtlinie für die Archivierung, den Postfächern der Benutzer verschiebt Elemente in das Archivpostfach zwei Jahre nach dem Datum das Element zugewiesen wird übermittelt. Wenn Sie dem Postfach eines Benutzers archivieren deaktivieren, auf Postfachelemente wird keine Aktion ausgeführt werden, und bleiben sie in der primären Postfach des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p109">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered. If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="82ccc-142">Um ein Archivpostfach zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="82ccc-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="82ccc-143">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="82ccc-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="82ccc-144">Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="82ccc-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="82ccc-145">Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Governance** \> **Archiv**.</span><span class="sxs-lookup"><span data-stu-id="82ccc-145">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="82ccc-p110">Die Seite **Archiv** wird angezeigt. Die Spalte **Archivpostfach** gibt für jeden Benutzer an, ob das Archivpostfach aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="82ccc-148">Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="82ccc-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="82ccc-149">Klicken Sie im Detailbereich auf **Deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="82ccc-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="82ccc-150">Eine Warnmeldung wird angezeigt, sagen, dass Sie 30 Tage bis das Archivpostfach erneut aktivieren müssen, und nach 30 Tagen alle Informationen in das Archiv dauerhaft gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="82ccc-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="82ccc-151">Klicken Sie auf **Ja**, um das Archivpostfach zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="82ccc-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="82ccc-p111">Es kann einen Moment, deaktivieren Sie das Archivpostfach dauern. Wenn es deaktiviert ist, **Archivpostfach: deaktiviert** wird im Detailbereich für den ausgewählten Benutzer angezeigt. Möglicherweise müssen Sie auf **Aktualisieren** klicken ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) zum Aktualisieren der Informationen im Detailbereich.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p111">It might take a few moments to disable the archive mailbox. When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="82ccc-p112">Sie können auch mehrere Archivpostfächer gleichzeitig deaktivieren, indem Sie mehrere Benutzer mit aktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="82ccc-157">Verwenden von Exchange Online PowerShell aktivieren oder Deaktivieren von archivpostfächern</span><span class="sxs-lookup"><span data-stu-id="82ccc-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="82ccc-p113">Sie können auch Exchange Online PowerShell verwenden, um archivpostfächer zu aktivieren. Der Hauptgrund-PowerShell verwendet wird, dass Sie schnell das Archivpostfach für alle Benutzer in Ihrer Organisation aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p113">You can also use Exchange Online PowerShell to enable archive mailboxes. The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="82ccc-p114">Der erste Schritt besteht Verbindung mit Exchange Online PowerShell. Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="82ccc-p114">The first step is to connect to Exchange Online PowerShell. For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="82ccc-162">Nachdem Sie Exchange Online verbunden sind, können Sie die Befehle in den folgenden Abschnitten zum Aktivieren oder Deaktivieren von archivpostfächern ausführen.</span><span class="sxs-lookup"><span data-stu-id="82ccc-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="82ccc-163">Aktivieren von Archivpostfächern</span><span class="sxs-lookup"><span data-stu-id="82ccc-163">Enable archive mailboxes</span></span>

<span data-ttu-id="82ccc-164">Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="82ccc-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="82ccc-165">Führen Sie den folgenden Befehl aus, um das Archivpostfach für alle Benutzer in Ihrer Organisation zu aktivieren (, deren Archivpostfach derzeit nicht aktiviert ist).</span><span class="sxs-lookup"><span data-stu-id="82ccc-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="82ccc-166">Deaktivieren von Archivpostfächern</span><span class="sxs-lookup"><span data-stu-id="82ccc-166">Disable archive mailboxes</span></span>

<span data-ttu-id="82ccc-167">Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="82ccc-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="82ccc-168">Führen Sie den folgenden Befehl aus, um das Archivpostfach für alle Benutzer in Ihrer Organisation zu deaktivieren (, deren Archivpostfach derzeit aktiviert ist).</span><span class="sxs-lookup"><span data-stu-id="82ccc-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="82ccc-169">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="82ccc-169">More information</span></span>
  
- <span data-ttu-id="82ccc-p115">Archivpostfächer helfen Ihnen und den Benutzern Ihrer Organisation Aufbewahrung, eDiscovery, erfüllen und halten Sie Anforderungen. Beispielsweise können Sie Ihrer Organisation Exchange Aufbewahrungsrichtlinie Inhalt von Postfächern in der Benutzer Archivpostfach verschieben. Bei Verwendung der Suchfunktion von Inhalten in das Wertpapier &amp; Compliance Center zum Suchen des Postfachs eines Benutzers nach bestimmten Inhalten, Archivpostfach des Benutzers wird auch durchsucht werden. Und wenn Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten platzieren oder eine Office 365-Aufbewahrungsrichtlinie auf dem Postfach eines Benutzers anwenden, werden auch Elemente in das Archivpostfach beibehalten.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p115">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements. For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox. When you use the Content Search tool in the Security &amp; Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched. And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="82ccc-p116">Wenn ein Archivpostfach aktiviert ist, können Benutzer Nachrichten in ihrem Archivpostfach speichern. Benutzer können auf ihre archivpostfächer zugreifen mithilfe von Microsoft Outlook und Outlook Web App verwenden eine der folgenden Clientanwendungen, die Benutzer können Nachrichten in ihren Archivpostfach anzuzeigen und verschieben oder Kopieren von Nachrichten zwischen ihren primären Postfachs und deren Archivpostfach. Benutzer können auch gelöschte Elemente aus dem Ordner wiederherstellbare Elemente in ihrem Archivpostfach wiederherstellen, mit dem Tool gelöschte Elemente wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="82ccc-p116">When an archive mailbox is enabled, users can store messages in their archive mailbox. Users can access their archive mailboxes by using Microsoft Outlook and Outlook Web App. Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox. Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
- <span data-ttu-id="82ccc-p117">Nach dem Archivieren Sie die Postfächer aktiviert sind, kann Ihre Organisation Exchange Standardaufbewahrungsrichtlinie (Messaging Records Management oder MRM-Richtlinie auch genannt) nutzen, die automatisch auf jedes Postfach zugeordnet ist. Wenn ein Archivpostfach aktiviert ist, führt der Exchange-Standardaufbewahrungsrichtlinie automatisch Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="82ccc-p117">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox. When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="82ccc-180">Verschieben von Elementen, die 2 Jahre alt oder älter sind, aus dem primären Postfach eines Benutzers in dessen Archivpostfach</span><span class="sxs-lookup"><span data-stu-id="82ccc-180">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="82ccc-181">Verschieben von Elementen, die 14 Tage alt oder älter sind, aus dem Ordner „Wiederherstellbare Elemente" im primären Postfach des Benutzers zum Ordner „Wiederherstellbare Elemente" im Archivpostfach .</span><span class="sxs-lookup"><span data-stu-id="82ccc-181">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="82ccc-182">Weitere Informationen zu archivpostfächer und Exchange-Aufbewahrungsrichtlinien finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="82ccc-182">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
  
    
  - [<span data-ttu-id="82ccc-183">Aufbewahrungstags und Aufbewahrungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="82ccc-183">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="82ccc-184">Default Aufbewahrungsrichtlinien in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="82ccc-184">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="82ccc-185">Richten Sie ein Archiv und Löschung Richtlinie für Postfächer in Ihrer Organisation Office 365</span><span class="sxs-lookup"><span data-stu-id="82ccc-185">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
