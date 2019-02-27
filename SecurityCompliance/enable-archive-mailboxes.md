---
title: Aktivieren von archivpostfächern im Office 365 &amp; Security Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.ArchivingHelp
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: 268a109e-7843-405b-bb3d-b9393b2342ce
description: Verwenden Sie das Office 365 &amp; Security Compliance Center, um Archivpostfächer zu aktivieren, um die Nachrichten Aufbewahrungs-, eDiscovery-und halte Anforderungen Ihrer Organisation zu unterstützen.
ms.openlocfilehash: 763097925ed0910fe9a66e5c556b8a2995df74e6
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296058"
---
# <a name="enable-archive-mailboxes-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="7a708-103">Aktivieren von archivpostfächern im Office 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="7a708-103">Enable archive mailboxes in the Office 365 Security &amp; Compliance Center</span></span>
  
<span data-ttu-id="7a708-p101">Die Archivierung in Office 365 (auch als in-Place-Archivierung bezeichnet) bietet Benutzern zusätzlichen Speicherplatz für Postfächer. Nachdem Sie Archivpostfächer aktiviert haben, können Benutzer mithilfe von Microsoft Outlook und Outlook im Web (früher als Outlook Web App bezeichnet) auf Nachrichten in ihren archivpostfächern zugreifen und diese speichern. Benutzer können auch Nachrichten zwischen Ihrem primären Postfach und Ihrem Archivpostfach verschieben oder kopieren. Sie können auch gelöschte Elemente aus dem Ordner "Wiederherstellbare Elemente" im Archivpostfach wiederherstellen, indem Sie das Tool "Gelöschte Elemente" verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a708-p101">Archiving in Office 365 (also called In-Place Archiving) provides users with additional mailbox storage space. After you turn on archive mailboxes, users can access and store messages in their archive mailboxes by using Microsoft Outlook and Outlook on the web (formerly known as Outlook Web App). Users can also move or copy messages between their primary mailbox and their archive mailbox. They can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
> [!TIP]
> <span data-ttu-id="7a708-p102">Office 365 bietet eine unbegrenzte Menge an Archivspeicher mit der automatisch expandierenden Archivierungsfunktion. Wenn die automatische Erweiterung der Archivierung aktiviert ist und dann das anfängliche Speicherkontingent im Archivpostfach eines Benutzers erreicht wird, fügt Office 365 automatisch zusätzlichen Speicherplatz hinzu. Dies führt dazu, dass für die Benutzer kein Speicherplatz mehr zur Verfügung steht und Sie nach der anfänglichen Aktivierung des Archivpostfachs und der automatischen Erweiterung der Archivierung für Ihre Organisation nichts verwalten müssen. Weitere Informationen finden Sie unter [Übersicht über unbegrenzte Archivierung in Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="7a708-p102">Office 365 provides an unlimited amount of archive storage with the auto-expanding archiving feature. When auto-expanding archiving is turned on, and then the initial storage quota in a user's archive mailbox is reached, Office 365 automatically adds additional storage space. This means that users won't run out of mailbox storage space and you won't have to manage anything after you initially enable the archive mailbox and turn on auto-expanding archiving for your organization. For more information, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="7a708-112">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="7a708-112">Before you begin</span></span>

<span data-ttu-id="7a708-p103">Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden, um Archivpostfächer zu aktivieren oder zu deaktivieren. Diese Rolle wird standardmäßig den Rollengruppen "Empfängerverwaltung" und "Organisationsverwaltung" auf der Seite " **Berechtigungen** " im Exchange Admin Center zugewiesen. Wenn die Seite **Archiv** im Security &amp; Compliance Center nicht angezeigt wird, bitten Sie den Administrator, Ihnen die erforderlichen Berechtigungen zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="7a708-p103">You have to be assigned the Mail Recipients role in Exchange Online to enable or disable archive mailboxes. By default, this role is assigned to the Recipient Management and Organization Management role groups on the **Permissions** page in the Exchange admin center. If you don't see the **Archive** page in the Security &amp; Compliance Center, ask your administrator to assign you the necessary permissions.</span></span> 
  
## <a name="enable-an-archive-mailbox"></a><span data-ttu-id="7a708-116">Aktivieren eines Archivpostfachs</span><span class="sxs-lookup"><span data-stu-id="7a708-116">Enable an archive mailbox</span></span>
  
1. <span data-ttu-id="7a708-117">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="7a708-117">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="7a708-118">Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="7a708-118">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="7a708-119">Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Data Governance** \> **Archive**.</span><span class="sxs-lookup"><span data-stu-id="7a708-119">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="7a708-p104">Die Seite **Archiv** wird angezeigt. Die Spalte **Archivpostfach** gibt für jeden Benutzer an, ob das Archivpostfach aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7a708-p104">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="7a708-122">Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="7a708-122">In the list of mailboxes, select the user that you want to enable the archive mailbox for.</span></span>
    
    ![Klicken Sie im Detailbereich des ausgewählten Benutzers auf aktivieren, um das Archivpostfach zu aktivieren.](media/8b53cdec-d5c9-4c28-af11-611f95c37b34.png)
  
5. <span data-ttu-id="7a708-124">Klicken Sie im Detailbereich für den ausgewählten Benutzer auf **aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="7a708-124">In the details pane for the selected user, click **Enable**.</span></span> 
    
    <span data-ttu-id="7a708-p105">Es wird eine Warnung angezeigt, dass beim Aktivieren des Archivpostfachs Elemente im Postfach des Benutzers, die älter als die dem Postfach zugewiesene Archivierungsrichtlinie sind, in das neue Archivpostfach verschoben werden. Die Standardarchiv Richtlinie, die Teil der Aufbewahrungsrichtlinie ist, die Exchange Online-Postfächern zugewiesen ist, verschiebt Elemente zwei Jahre nach dem Datum, an dem das Element an das Postfach zugestellt oder vom Benutzer erstellt wurde, in das Archivpostfach. Weitere Informationen finden Sie im Abschnitt **Weitere Informationen** in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="7a708-p105">A warning is displayed saying that if you enable the archive mailbox, items in the user's mailbox that are older than the archiving policy assigned to the mailbox will be moved to the new archive mailbox. The default archive policy that is part of the retention policy assigned to Exchange Online mailboxes moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see the **More info** section in this article.</span></span> 
    
6. <span data-ttu-id="7a708-128">Klicken Sie auf **Ja**, um das Archivpostfach zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a708-128">Click **Yes** to enable the archive mailbox.</span></span> 
    
    <span data-ttu-id="7a708-p106">Es kann einen Moment dauern, bis das Archivpostfach erstellt wurde. Wenn es erstellt wird, wird **Archivpostfach: aktiviert** im Detailbereich für den ausgewählten Benutzer angezeigt. Möglicherweise müssen Sie \*\*\*\* ![auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren klicken, um die Informationen im Detailbereich zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7a708-p106">It might take a few moments to create the archive mailbox. When it's created, **Archive mailbox: enabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="7a708-p107">Sie können auch mehrere Archivpostfächer gleichzeitig aktivieren, indem Sie mehrere Benutzer mit deaktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="7a708-p107">You can also bulk-enable archive mailboxes by selecting multiple users with disabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Enable** in the details pane.</span></span> 
  
## <a name="disable-an-archive-mailbox"></a><span data-ttu-id="7a708-134">Deaktivieren eines Archivpostfachs</span><span class="sxs-lookup"><span data-stu-id="7a708-134">Disable an archive mailbox</span></span>
  
<span data-ttu-id="7a708-p108">Sie können auch die Seite **Archiv** im Security &amp; Compliance Center verwenden, um das Archivpostfach eines Benutzers zu deaktivieren. Nachdem Sie ein Archivpostfach deaktiviert haben, können Sie es innerhalb von 30 Tagen nach der Deaktivierung wieder mit dem primären Postfach des Benutzers verbinden. In diesem Fall werden die ursprünglichen Inhalte des Archivpostfachs wiederhergestellt. Nach 30 Tagen werden die Inhalte des ursprünglichen Archivpostfachs dauerhaft gelöscht und können nicht wiederhergestellt werden. Wenn Sie das Archiv also mehr als 30 Tage nach dem Deaktivieren erneut aktivieren, wird ein neues Archivpostfach erstellt.</span><span class="sxs-lookup"><span data-stu-id="7a708-p108">You can also use the **Archive** page in the Security &amp; Compliance Center to disable a user's archive mailbox. After you disable an archive mailbox, you can reconnect it to the user's primary mailbox within 30 days of disabling it. In this case, the original contents of the archive mailbox are restored. After 30 days, the contents of the original archive mailbox are permanently deleted and can't be recovered. So if you re-enable the archive more than 30 days after disabling it, a new archive mailbox is created.</span></span> 
  
<span data-ttu-id="7a708-p109">Beachten Sie, dass die standardmäßigen archivrichtlinien, die den Postfächern von Benutzern zugewiesen sind, zwei Jahre nach dem Datum, an dem das Element zugestellt wurde, Elemente in das Archivpostfach verschieben Wenn Sie das Archivpostfach eines Benutzers deaktivieren, werden keine Aktionen für Postfachelemente durchgeführt, und Sie verbleiben im primären Postfach des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7a708-p109">Note that the default archive policy assigned to users' mailboxes moves items to the archive mailbox two years after the date the item is delivered. If you disable a user's archive mailbox, no action will be taken on mailbox items and they will remain in the user's primary mailbox.</span></span>
  
<span data-ttu-id="7a708-142">So deaktivieren Sie ein Archivpostfach</span><span class="sxs-lookup"><span data-stu-id="7a708-142">To disable an archive mailbox:</span></span>
  
1. <span data-ttu-id="7a708-143">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="7a708-143">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="7a708-144">Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="7a708-144">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="7a708-145">Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Data Governance** \> **Archive**.</span><span class="sxs-lookup"><span data-stu-id="7a708-145">In the left pane of the Security &amp; Compliance Center, click **Data governance** \> **Archive**.</span></span>
    
    <span data-ttu-id="7a708-p110">Die Seite **Archiv** wird angezeigt. Die Spalte **Archivpostfach** gibt für jeden Benutzer an, ob das Archivpostfach aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7a708-p110">The **Archive** page is displayed. The **Archive mailbox** column indicates whether an archive mailbox is enabled or disabled for each user.</span></span> 
    
4. <span data-ttu-id="7a708-148">Wählen Sie in der Liste der Postfächer den Benutzer aus, dessen Archivpostfach Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="7a708-148">In the list of mailboxes, select the user that you want to disable the archive mailbox for.</span></span>
    
5. <span data-ttu-id="7a708-149">Klicken Sie im Detailbereich auf **Deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="7a708-149">In the details pane, click **Disable**.</span></span> 
    
    <span data-ttu-id="7a708-150">Eine Warnmeldung wird angezeigt, die besagt, dass Sie 30 Tage Zeit haben, um das Archivpostfach wieder zu aktivieren, und dass nach 30 Tagen alle Informationen im Archiv dauerhaft gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="7a708-150">A warning message is displayed saying that you'll have 30 days to re-enable the archive mailbox, and that after 30 days, all information in the archive will be permanently deleted.</span></span> 
    
6. <span data-ttu-id="7a708-151">Klicken Sie auf **Ja**, um das Archivpostfach zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a708-151">Click **Yes** to disable the archive mailbox.</span></span> 
    
    <span data-ttu-id="7a708-p111">Es kann einen Moment dauern, bis das Archivpostfach deaktiviert wurde. Wenn es deaktiviert ist, wird **Archivpostfach: deaktiviert** im Detailbereich für den ausgewählten Benutzer angezeigt. Möglicherweise müssen Sie \*\*\*\* ![auf Aktualisierungssymbol](media/O365-MDM-Policy-RefreshIcon.gif) aktualisieren klicken, um die Informationen im Detailbereich zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7a708-p111">It might take a few moments to disable the archive mailbox. When it's disabled, **Archive mailbox: disabled** is displayed in the details pane for the selected user. You might have to click **Refresh** ![Refresh icon](media/O365-MDM-Policy-RefreshIcon.gif) to update the information in the details pane.</span></span> 
    
> [!TIP]
> <span data-ttu-id="7a708-p112">Sie können auch mehrere Archivpostfächer gleichzeitig deaktivieren, indem Sie mehrere Benutzer mit aktivierten Postfächern auswählen. (Verwenden Sie dazu die UMSCHALT- oder die STRG-Taste.) Klicken Sie nach der Auswahl mehrerer Postfächer im Detailbereich auf **Deaktivieren**.</span><span class="sxs-lookup"><span data-stu-id="7a708-p112">You can also bulk-disable archive mailboxes by selecting multiple users with enabled archive mailboxes (use the Shift or Ctrl keys). After selecting multiple mailboxes, click **Disable** in the details pane.</span></span> 
  
## <a name="use-exchange-online-powershell-to-enable-or-disable-archive-mailboxes"></a><span data-ttu-id="7a708-157">Verwenden von Exchange Online PowerShell zum Aktivieren oder Deaktivieren von archivpostfächern</span><span class="sxs-lookup"><span data-stu-id="7a708-157">Use Exchange Online PowerShell to enable or disable archive mailboxes</span></span>

<span data-ttu-id="7a708-p113">Sie können auch Exchange Online PowerShell verwenden, um Archivpostfächer zu aktivieren. Der Hauptgrund für die Verwendung von PowerShell besteht darin, dass Sie das Archivpostfach für alle Benutzer in Ihrer Organisation schnell aktivieren können.</span><span class="sxs-lookup"><span data-stu-id="7a708-p113">You can also use Exchange Online PowerShell to enable archive mailboxes. The primary reason to use PowerShell is that you can quickly enable the archive mailbox for all users in your organization.</span></span>

<span data-ttu-id="7a708-p114">Der erste Schritt besteht darin, eine Verbindung mit Exchange Online PowerShell herzustellen. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="7a708-p114">The first step is to connect to Exchange Online PowerShell. For instructions, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span>

<span data-ttu-id="7a708-162">Nachdem Sie eine Verbindung mit Exchange Online hergestellt haben, können Sie die Befehle in den folgenden Abschnitten ausführen, um Archivpostfächer zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a708-162">After you're connected to Exchange Online, you can run the commands in the following sections to enable or disable archive mailboxes.</span></span>

### <a name="enable-archive-mailboxes"></a><span data-ttu-id="7a708-163">Aktivieren von Archivpostfächern</span><span class="sxs-lookup"><span data-stu-id="7a708-163">Enable archive mailboxes</span></span>

<span data-ttu-id="7a708-164">Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a708-164">Run the following command to enable the archive mailbox for a single user.</span></span>
    
  ```
  Enable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="7a708-165">Führen Sie den folgenden Befehl aus, um das Archivpostfach für alle Benutzer in Ihrer Organisation zu aktivieren (deren Archivpostfach derzeit nicht aktiviert ist).</span><span class="sxs-lookup"><span data-stu-id="7a708-165">Run the following command to enable the archive mailbox for all users in your organization (whose archive mailbox is currently not enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "None" -AND RecipientTypeDetails -eq "UserMailbox"} | Enable-Mailbox -Archive
  ```
  
### <a name="disable-archive-mailboxes"></a><span data-ttu-id="7a708-166">Deaktivieren von Archivpostfächern</span><span class="sxs-lookup"><span data-stu-id="7a708-166">Disable archive mailboxes</span></span>

<span data-ttu-id="7a708-167">Führen Sie den folgenden Befehl aus, um das Archivpostfach für einen einzelnen Benutzer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="7a708-167">Run the following command to disable the archive mailbox for a single user.</span></span>
    
  ```
  Disable-Mailbox -Identity <username> -Archive
  ```

<span data-ttu-id="7a708-168">Führen Sie den folgenden Befehl aus, um das Archivpostfach für alle Benutzer in Ihrer Organisation zu deaktivieren (deren Archivpostfach derzeit aktiviert ist).</span><span class="sxs-lookup"><span data-stu-id="7a708-168">Run the following command to disable the archive mailbox for all users in your organization (whose archive mailbox is currently enabled).</span></span>
    
  ```
  Get-Mailbox -Filter {ArchiveStatus -Eq "Active" -AND RecipientTypeDetails -eq "UserMailbox"} | Disable-Mailbox -Archive
  ```

## <a name="more-information"></a><span data-ttu-id="7a708-169">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7a708-169">More information</span></span>
  
- <span data-ttu-id="7a708-p115">Archivpostfächer helfen Ihnen und ihren Benutzern, die Aufbewahrungs-, eDiscovery-und halte Anforderungen Ihrer Organisation zu erfüllen. Sie können beispielsweise die Exchange-Aufbewahrungsrichtlinie Ihrer Organisation verwenden, um Postfachinhalte in das Archivpostfach der Benutzer zu verschieben. Wenn Sie das Inhaltssuche-Tool im Security &amp; Compliance Center verwenden, um das Postfach eines Benutzers nach bestimmten Inhalten zu durchsuchen, wird auch das Archivpostfach des Benutzers durchsucht. Außerdem werden Elemente im Archivpostfach beibehalten, wenn Sie eine Aufbewahrungsrichtlinie für Office 365 auf das Postfach eines Benutzers anwenden.</span><span class="sxs-lookup"><span data-stu-id="7a708-p115">Archive mailboxes help you and your users to meet your organization's retention, eDiscovery, and hold requirements. For example, you can use your organization's Exchange retention policy to move mailbox content to users' archive mailbox. When you use the Content Search tool in the Security &amp; Compliance Center to search a user's mailbox for specific content, the user's archive mailbox will also be searched. And, when you place a Litigation Hold or apply an Office 365 retention policy to a user's mailbox, items in the archive mailbox are also retained.</span></span>
  
- <span data-ttu-id="7a708-p116">Wenn ein Archivpostfach aktiviert ist, können Benutzer Nachrichten in Ihrem Archivpostfach speichern. Benutzer können mithilfe von Microsoft Outlook und Outlook im Web auf Ihre Archivpostfächer zugreifen. Mithilfe einer dieser Clientanwendungen können Benutzer Nachrichten in Ihrem Archivpostfach anzeigen und Nachrichten zwischen Ihrem primären Postfach und Ihrem Archivpostfach verschieben oder kopieren. Benutzer können auch gelöschte Elemente aus dem Ordner "Wiederherstellbare Elemente" im Archivpostfach wiederherstellen, indem Sie das Tool "Gelöschte Elemente" verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a708-p116">When an archive mailbox is enabled, users can store messages in their archive mailbox. Users can access their archive mailboxes by using Microsoft Outlook and Outlook on the web. Using either of these client applications, users can view messages in their archive mailbox and move or copy messages between their primary mailbox and their archive mailbox. Users can also recover deleted items from the Recoverable Items folder in their archive mailbox by using the Recover Deleted Items tool.</span></span> 
  
- <span data-ttu-id="7a708-p117">Nachdem Archivpostfächer aktiviert wurden, kann Ihre Organisation die standardmäßige Exchange-Aufbewahrungsrichtlinie nutzen (auch als Messaging Records Management oder MRM Policy bezeichnet), die jedem Postfach automatisch zugewiesen wird. Wenn ein Archivpostfach aktiviert ist, führt die Exchange-Standardaufbewahrungsrichtlinie automatisch folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="7a708-p117">After archive mailboxes are enabled, your organization can take advantage of the default Exchange retention policy (also called Messaging Records Management or MRM policy) that is automatically assigned to every mailbox. When an archive mailbox is enabled, the default Exchange retention policy automatically does the following:</span></span> 
  
    - <span data-ttu-id="7a708-180">Verschieben von Elementen, die 2 Jahre alt oder älter sind, aus dem primären Postfach eines Benutzers in dessen Archivpostfach</span><span class="sxs-lookup"><span data-stu-id="7a708-180">Moves items that are two years or older from a user's primary mailbox to their archive mailbox.</span></span> 
    
    - <span data-ttu-id="7a708-181">Verschieben von Elementen, die 14 Tage alt oder älter sind, aus dem Ordner „Wiederherstellbare Elemente" im primären Postfach des Benutzers zum Ordner „Wiederherstellbare Elemente" im Archivpostfach .</span><span class="sxs-lookup"><span data-stu-id="7a708-181">Moves items that are 14 days or older from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in their archive mailbox.</span></span>
    
- <span data-ttu-id="7a708-182">Weitere Informationen zu archivpostfächern und Exchange-Aufbewahrungsrichtlinien finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="7a708-182">For more information about archive mailboxes and Exchange retention policies, see:</span></span>
  
    
  - [<span data-ttu-id="7a708-183">Aufbewahrungstags und Aufbewahrungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="7a708-183">Retention tags and retention policies</span></span>](https://go.microsoft.com/fwlink/?LinkId=404424)
    
  - [<span data-ttu-id="7a708-184">Standardmäßige AufbewahrungsRichtlinie in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="7a708-184">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/?linkid=839418)
    
  - [<span data-ttu-id="7a708-185">Einrichten einer Archivierungs-und Löschrichtlinie für Postfächer in Ihrer Office 365-Organisation</span><span class="sxs-lookup"><span data-stu-id="7a708-185">Set up an archive and deletion policy for mailboxes in your Office 365 organization</span></span>](set-up-an-archive-and-deletion-policy-for-mailboxes.md)
