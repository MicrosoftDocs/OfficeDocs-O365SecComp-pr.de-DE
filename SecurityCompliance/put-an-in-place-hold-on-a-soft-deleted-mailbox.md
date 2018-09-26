---
title: Einfügen eines In-situ für ein vorläufig gelöschtes Postfach in Exchange Online
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/18/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: 421f72bd-dd43-4be1-82f5-0ae9ac43bd00
description: Erfahren Sie, wie Sie einen In-Situ-Speicher für ein vorläufig gelöschtes Postfach erstellen können, damit es inaktiv wird und der Inhalt bewahrt wird. Anschließend können Sie zum Durchsuchen des inaktiven Postfachs die Microsoft eDiscovery-Tools verwenden.
ms.openlocfilehash: b4ef4ee26e98c8234f64d0879391f8fec89ffd3c
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038248"
---
# <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-in-exchange-online"></a><span data-ttu-id="c8baf-104">Einfügen eines In-situ für ein vorläufig gelöschtes Postfach in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c8baf-104">Put an In-Place Hold on a soft-deleted mailbox in Exchange Online</span></span>

<span data-ttu-id="c8baf-p102">Erfahren Sie, wie Sie einen In-Situ-Speicher für ein vorläufig gelöschtes Postfach erstellen können, damit es inaktiv wird und der Inhalt bewahrt wird. Anschließend können Sie zum Durchsuchen des inaktiven Postfachs die Microsoft eDiscovery-Tools verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8baf-p102">Learn how to create an In-Place Hold for a soft-deleted mailbox to make it inactive and preserve its contents. Then you can use Microsoft eDiscovery tools to search the inactive mailbox.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c8baf-p103">Wir haben den Stichtag (1. Juli 2017) für das Erstellen neuer In-Situ-Speicher in Exchange Online (in Office 365 und eigenständigen Exchange Online-Plänen) verschoben. Im späteren Verlauf dieses Jahres oder Anfang des nächsten Jahres können Sie keine neuen In-Situ-Speicher mehr in Exchange Online erstellen. Als Alternative zur Verwendung von In-Situ-Speichern können Sie [eDiscovery-Fälle](https://go.microsoft.com/fwlink/?linkid=780738) oder [Aufbewahrungsrichtlinien](https://go.microsoft.com/fwlink/?linkid=827811) im Office 365-Sicherheit &amp; Compliance Center verwenden. Sobald die Erstellung neuer In-Situ-Speicher eingestellt ist, können vorhandene In-Situ-Speicher weiterhin geändert werden, und das Erstellen neuer In-Situ-Speicher in Exchange Server 2013- und Exchange-Hybridbereitstellungen wird weiterhin unterstützt. Und Sie können weiterhin Postfächer im Beweissicherungsverfahren platzieren.</span><span class="sxs-lookup"><span data-stu-id="c8baf-p103">We've postponed the July 1, 2017 deadline for creating new In-Place Holds in Exchange Online (in Office 365 and Exchange Online standalone plans). But later this year or early next year, you won't be able to create new In-Place Holds in Exchange Online. As an alternative to using In-Place Holds, you can use [eDiscovery cases](https://go.microsoft.com/fwlink/?linkid=780738) or [retention policies](https://go.microsoft.com/fwlink/?linkid=827811) in the Office 365 Security &amp; Compliance Center. After we decommission new In-Place Holds, you'll still be able to modify existing In-Place Holds, and creating new In-Place Holds in Exchange Server 2013 and Exchange hybrid deployments will still be supported. And, you'll still be able to place mailboxes on Litigation Hold.</span></span> 
  
<span data-ttu-id="c8baf-p104">Sie müssen möglicherweise eine Situation, in dem eine Person hat Ihre Organisation verlassen, und ihre entsprechendes Benutzerkonto und Postfach gelöscht wurden. Anschließend stellen Sie fest, dass die Informationen in das Postfach, das beibehalten werden soll. Was können Sie tun? Wenn die Aufbewahrungszeit für gelöschte Postfächer abgelaufen ist, können Sie auf das gelöschte Postfach (mit der Bezeichnung eines vorläufig gelöschten Postfachs) halten an In-Place Hold und ein inaktives Postfachs erleichtern. Ein *inaktives Postfach* wird verwendet, um einem früheren Mitarbeiter e-Mail beibehalten, nachdem er in Ihrer Organisation verlassen hat. Der Inhalt eines inaktiven Postfachs wird beibehalten, für die Dauer der In-Place Hold, die für das vorläufig gelöschte Postfach gesetzt wird, wenn sie als inaktiv festgelegt wurde. Nach das Postfach inaktive erfolgt, suchen Sie das Postfach mithilfe von Compliance-eDiscovery in Exchange Online, Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center oder das eDiscovery Center in SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="c8baf-p104">You might have a situation where a person has left your organization, and their corresponding user account and mailbox were deleted. Afterwards, you realize there's information in the mailbox that needs to be preserved. What can you do? If the deleted mailbox retention period hasn't expired, you can put an In-Place Hold on the deleted mailbox (called a  soft-deleted mailbox ) and make it an inactive mailbox. An  *inactive mailbox*  is used to preserve a former employee's email after he or she leaves your organization. The contents of an inactive mailbox are preserved for the duration of the In-Place Hold that was is placed on the soft-deleted mailbox when it was made inactive. After the mailbox is made inactive, you can search the mailbox by using In-Place eDiscovery in Exchange Online, Content Search in the Office 365 Security &amp; Compliance Center, or the eDiscovery Center in SharePoint Online.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c8baf-p105">In Exchange Online ist ein vorläufig gelöschtes Postfach ein Postfach, das zwar gelöscht wurde, aber innerhalb eines bestimmten Aufbewahrungszeitraums wiederhergestellt werden kann. Dieser Aufbewahrungszeitraum für vorläufig gelöschte Postfächer beträgt in Exchange Online 30 Tage. Das bedeutet, dass das Postfach innerhalb von 30 Tagen nach dem vorläufigen Löschen wiederhergestellt werden kann. Nach 30 Tagen wird ein vorläufig gelöschtes Postfach für das dauerhafte Löschen markiert und kann dann nicht mehr wiederhergestellt oder inaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="c8baf-p105">In Exchange Online, a soft-deleted mailbox is a mailbox that's been deleted but can be recovered within a specific retention period. The soft-deleted mailbox retention period in Exchange Online is 30 days. This means that the mailbox can be recovered (or made an inactive mailbox) within 30 days of being deleted. After 30 days, a soft-deleted mailbox is marked for permanent deletion and can't be recovered or made inactive.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="c8baf-123">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="c8baf-123">Before you begin</span></span>
<span data-ttu-id="c8baf-124"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="c8baf-124"></span></span>

- <span data-ttu-id="c8baf-p106">Sie müssen das **New-MailboxSearch** -Cmdlet in Windows PowerShell verwenden, um einen In-Situ-Speicher für ein vorläufig gelöschtes Postfach zu erstellen. Sie können nicht das Exchange-Verwaltungskonsole (EAC) oder das eDiscovery Center in SharePoint Online verwenden.</span><span class="sxs-lookup"><span data-stu-id="c8baf-p106">You have to use the **New-MailboxSearch** cmdlet in Windows PowerShell to put an In-Place Hold on a soft-deleted mailbox. You can't use the Exchange admin center (EAC) or the eDiscovery Center in SharePoint Online.</span></span> 
    
- <span data-ttu-id="c8baf-127">Wie Sie mit Windows PowerShell eine Verbindung mit Exchange Online herstellen, können Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554) nachlesen.</span><span class="sxs-lookup"><span data-stu-id="c8baf-127">To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="c8baf-128">Führen Sie den folgenden Befehl aus, um die Identitätsinformationen zu den vorläufig gelöschten Postfächern in Ihrer Organisation abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c8baf-128">Run the following command to get identity information about the soft-deleted mailboxes in your organization.</span></span> 
    
  ```
  Get-Mailbox -SoftDeletedMailbox | FL Name,WhenSoftDeleted,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
  ```

- <span data-ttu-id="c8baf-129">Weitere Informationen zu inaktiven Postfächern finden Sie unter [Inaktive Postfächer in Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8baf-129">For more information about inactive mailboxes, see [Inactive mailboxes in Exchange Online](http://technet.microsoft.com/library/2f2948c5-1c5a-4643-865c-b36e4ac1414b.aspx).</span></span>
    
## <a name="put-an-in-place-hold-on-a-soft-deleted-mailbox-to-make-it-an-inactive-mailbox"></a><span data-ttu-id="c8baf-130">Erstellen eines In-Situ-Speichers für ein vorläufig gelöschtes Postfach, um daraus ein inaktives Postfach zu machen</span><span class="sxs-lookup"><span data-stu-id="c8baf-130">Put an In-Place Hold on a soft-deleted mailbox to make it an inactive mailbox</span></span>
<span data-ttu-id="c8baf-131"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="c8baf-131"></span></span>

<span data-ttu-id="c8baf-p107">Verwenden Sie das **New-MailboxSearch** -Cmdlet, um aus dem vorläufig gelöschten Postfach ein inaktives Postfach zu machen. Weitere Informationen finden Sie unter [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8baf-p107">Use the **New-MailboxSearch** cmdlet to make a soft-deleted mailbox an inactive mailbox. For more information, see [New-MailboxSearch](http://technet.microsoft.com/library/74303b47-bb49-407c-a43b-590356eae35c.aspx).</span></span>
  
1. <span data-ttu-id="c8baf-134">Erstellen Sie eine Variable, die die Eigenschaften des vorläufig gelöschten Postfachs enthält.</span><span class="sxs-lookup"><span data-stu-id="c8baf-134">Create a variable that contains the properties of the soft-deleted mailbox.</span></span> 
    
  ```
  $SoftDeletedMailbox = Get-Mailbox -SoftDeletedMailbox -Identity <identity of soft-deleted mailbox>
  ```

    > [!IMPORTANT]
    > <span data-ttu-id="c8baf-p108">Verwenden Sie im vorherigen Befehl den Wert der Eigenschaft **DistinguishedName** oder **ExchangeGuid** zum Identifizieren des vorläufig gelöschten Postfachs. Diese Eigenschaften sind für jedes Postfach in Ihrer Organisation eindeutig, wobei ein aktives und ein inaktives Postfach die gleiche primäre SMTP-Adresse haben können.</span><span class="sxs-lookup"><span data-stu-id="c8baf-p108">In the previous command, use the value of the **DistinguishedName** or **ExchangeGuid** property to identify the soft-deleted mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active mailbox and a soft-deleted mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="c8baf-p109">Erstellen Sie einen In-Situ-Speicher und wenden Sie ihn auf das vorläufig gelöschte Postfach an. In diesem Beispiel wird nicht angegeben, wie lange der Speicher aktiv sein soll. Das bedeutet, dass Elemente auf unbestimmte Zeit oder bis der In-Situ-Speicher für das inaktive Postfach entfernt wird, beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="c8baf-p109">Create an In-Place Hold and place it on the soft-deleted mailbox. In this example, no hold duration is specified. This means items will be held indefinitely or until the hold is removed from the inactive mailbox.</span></span>
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true
  
  ```

    <span data-ttu-id="c8baf-p110">Beim Erstellen des In-Situ-Speichers können Sie auch eine Aufbewahrungsdauer angeben. In diesem Beispiel werden Elemente im inaktiven Postfach für ca. 7 Jahre aufbewahrt.</span><span class="sxs-lookup"><span data-stu-id="c8baf-p110">You can also specify a hold duration when you create the In-Place Hold. This example holds items in the inactive mailbox for approximately 7 years.</span></span>
    
  ```
  New-MailboxSearch -Name "InactiveMailboxHold" -SourceMailboxes $SoftDeletedMailbox.DistinguishedName -InPlaceHoldEnabled $true -ItemHoldPeriod 2777
  ```

3. <span data-ttu-id="c8baf-142">Führen Sie nach ein paar Augenblicken einen der folgenden Befehle aus, um sicherzustellen, dass es sich bei dem vorläufig gelöschten Postfach um ein inaktives Postfach handelt.</span><span class="sxs-lookup"><span data-stu-id="c8baf-142">After a few moments, run one of the following commands to verify that the soft-deleted mailbox is an inactive mailbox.</span></span>
    
  ```
  Get-Mailbox -InactiveMailboxOnly
  ```

    <span data-ttu-id="c8baf-143">Oder</span><span class="sxs-lookup"><span data-stu-id="c8baf-143">Or</span></span>
    
  ```
  Get-Mailbox -InactiveMailboxOnly -Identity $SoftDeletedMailbox.DistinguishedName  | FL IsInactiveMailbox
  ```

## <a name="more-information"></a><span data-ttu-id="c8baf-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c8baf-144">More information</span></span>
<span data-ttu-id="c8baf-145"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="c8baf-145"></span></span>

<span data-ttu-id="c8baf-p111">Nachdem Sie aus einem vorläufig gelöschten Postfach ein inaktives Postfach gemacht haben, gibt es eine Reihe von Methoden, mit denen Sie das Postfach verwalten können. Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="c8baf-p111">After you make a soft-deleted mailbox an inactive mailbox, there are a number of ways you can manage the mailbox. For more information, see:</span></span>
  
- [<span data-ttu-id="c8baf-148">Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c8baf-148">Change the hold duration for an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/96eb634e-af2f-454e-8014-b698396811c4.aspx)
    
- [<span data-ttu-id="c8baf-149">Wiederherstellen eines inaktiven Postfachs in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c8baf-149">Recover an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/283838b4-66ba-4c34-b221-e1a3875e1d29.aspx)
    
- [<span data-ttu-id="c8baf-150">Rückspeichern eines inaktiven Postfachs in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c8baf-150">Restore an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/1fb02feb-49e5-4485-aec5-9f1537b772b6.aspx)
    
- [<span data-ttu-id="c8baf-151">Aufheben der Aufbewahrung für ein inaktives Postfach in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="c8baf-151">Remove a hold from an inactive mailbox in Exchange Online</span></span>](http://technet.microsoft.com/library/930a98c3-cd81-4aaa-8e22-19714cb2b731.aspx)
    

