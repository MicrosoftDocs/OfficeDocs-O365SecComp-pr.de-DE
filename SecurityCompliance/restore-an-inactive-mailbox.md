---
title: Wiederherstellen eines inaktiven Postfachs in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/28/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 97e06a7a-ef9a-4ce8-baea-18b9e20449a3
description: Wenn ein neuer Mitarbeiter oder ein anderer Benutzer Zugriff auf die Inhalte eines inaktiven Postfachs in Office 365 benötigt, können Sie den Inhalt des inaktiven Postfachs in einem vorhandenen Postfach wiederherstellen (oder zusammenführen).
ms.openlocfilehash: fa3572ef34a905ae2216672ed42507f0c712accb
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296618"
---
# <a name="restore-an-inactive-mailbox-in-office-365"></a><span data-ttu-id="90836-103">Wiederherstellen eines inaktiven Postfachs in Office 365</span><span class="sxs-lookup"><span data-stu-id="90836-103">Restore an inactive mailbox in Office 365</span></span>

<span data-ttu-id="90836-p101">Ein inaktives Postfach (eine Art vorläufig gelöschtes Postfach) wird verwendet, um die E-Mails eines ehemaligen Mitarbeiters aufzubewahren, nachdem dieser die Organisation verlassen hat. Wenn ein anderer Mitarbeiter die Zuständigkeiten des ehemaligen Mitarbeiters übernimmt oder dieser Mitarbeiter in Ihre Organisation zurückkehrt, gibt es zwei Möglichkeiten, den Inhalt des inaktiven Postfachs wieder für einen Benutzer verfügbar zu machen:</span><span class="sxs-lookup"><span data-stu-id="90836-p101">An inactive mailbox (which is a type of soft-deleted mailbox) is used to retain a former employee's email after he or she leaves your organization. If another employee takes on the job responsibilities of the departed employee or if that employee returns to your organization, there are two ways that you can make the contents of the inactive mailbox available to a user:</span></span> 
  
- <span data-ttu-id="90836-p102">**Rückspeichern eines inaktiven Postfachs** Wenn ein anderer Mitarbeiter die Zuständigkeiten des ehemaligen Mitarbeiters übernimmt oder ein anderer Benutzer Zugriff auf die Inhalte des inaktiven Postfachs benötigt, können Sie den Inhalt des inaktiven Postfachs in ein vorhandenes Postfach rückspeichern (oder ihn mit diesem zusammenführen). Sie können auch das Archiv aus einem inaktiven Postfach rückspeichern. Nach dem Rückspeichern bleibt das inaktive Postfach als ein solches erhalten. In diesem Thema werden die Verfahren zum Rückspeichern eines inaktiven Postfachs beschrieben.</span><span class="sxs-lookup"><span data-stu-id="90836-p102">**Restore an inactive mailbox** If another employee takes on the job responsibilities of the departed employee, or if another user needs access to the contents of the inactive mailbox, you can restore (or merge) the contents of the inactive mailbox to an existing mailbox. You can also restore the archive from an inactive mailbox. After it's restored, the inactive mailbox is preserved and is retained as an inactive mailbox. This topic describes the procedures for restoring an inactive mailbox.</span></span> 
    
- <span data-ttu-id="90836-p103">**Wiederherstellen eines** inaktiven Postfachs Wenn der abgesetzte Mitarbeiter zu Ihrer Organisation zurückkehrt oder ein neuer Mitarbeiter zur Übernahme der Aufgaben des abberufenen Mitarbeiters eingestellt wird, können Sie die Inhalte des inaktiven Postfachs wiederherstellen. Diese Methode konvertiert das inaktive Postfach in ein neues Postfach, das den Inhalt des inaktiven Postfachs enthält. Nach der Wiederherstellung ist das inaktive Postfach nicht mehr vorhanden. Eine schrittweise Anleitung finden Sie unter [Wiederherstellen eines inaktiven Postfachs in Office 365](recover-an-inactive-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="90836-p103">**Recover an inactive mailbox** If the departed employee returns to your organization, or if a new employee is hired to take on the job responsibilities of the departed employee, you can recover the contents of the inactive mailbox. This method converts the inactive mailbox to a new mailbox that contains the contents of the inactive mailbox. After it's recovered, the inactive mailbox no longer exists. For the step-by-step procedures, see [Recover an inactive mailbox in Office 365](recover-an-inactive-mailbox.md).</span></span>
    
<span data-ttu-id="90836-114">Im Abschnitt **Weitere Informationen** in diesem Artikel finden Sie weitere Informationen zu den Unterschieden zwischen der Wiederherstellung eines inaktiven Postfachs.</span><span class="sxs-lookup"><span data-stu-id="90836-114">See the **More information** section in this article for more details about the differences between restoring and recovering an inactive mailbox.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="90836-115">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="90836-115">Before you begin</span></span>

- <span data-ttu-id="90836-p104">Zum Wiederherstellen eines inaktiven Postfachs müssen Sie Exchange Online PowerShell verwenden. Die Exchange-Verwaltungskonsole kann nicht verwendet werden. Schrittweise Anleitungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="90836-p104">You have to use Exchange Online PowerShell to restore an inactive mailbox. You can't use the Exchange admin center (EAC). For step-by-step instructions, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554).</span></span>
    
- <span data-ttu-id="90836-119">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um Identitätsinformationen für die inaktiven Postfächer in Ihrer Organisation abzurufen.</span><span class="sxs-lookup"><span data-stu-id="90836-119">Run the following command in Exchange Online PowerShell to get identity information for the inactive mailboxes in your organization.</span></span> 
    
    ```
    Get-Mailbox -InactiveMailboxOnly | FL Name,DistinguishedName,ExchangeGuid,PrimarySmtpAddress
    ```

     <span data-ttu-id="90836-120">Verwenden Sie die von diesem Befehl zurückgegebenen Informationen zum Rückspeichern eines bestimmten inaktiven Postfachs.</span><span class="sxs-lookup"><span data-stu-id="90836-120">Use the information returned by this command to restore a specific inactive mailbox.</span></span>
    
- <span data-ttu-id="90836-121">Weitere Informationen zu inaktiven Postfächern finden Sie unter inAktive [Postfächer in Office 365](inactive-mailboxes-in-office-365.md).</span><span class="sxs-lookup"><span data-stu-id="90836-121">For more information about inactive mailboxes, see [Inactive mailboxes in Office 365](inactive-mailboxes-in-office-365.md).</span></span>
    
## <a name="restore-an-inactive-mailbox"></a><span data-ttu-id="90836-122">Rückspeichern eines inaktiven Postfachs</span><span class="sxs-lookup"><span data-stu-id="90836-122">Restore an inactive mailbox</span></span>

<span data-ttu-id="90836-p105">Verwenden Sie das Cmdlet **New-MailboxRestoreRequest** mit den Parametern  _SourceMailbox_ und  _TargetMailbox_, um den Inhalt eines inaktiven Postfachs in ein vorhandenes Postfach rückzuspeichern. Weitere Informationen zu diesem Cmdlet finden Sie unter [New-MailboxRestoreRequest](https://go.microsoft.com/fwlink/?linkid=856298).</span><span class="sxs-lookup"><span data-stu-id="90836-p105">Use the **New-MailboxRestoreRequest** cmdlet with the  _SourceMailbox_ and  _TargetMailbox_ parameters to restore the contents of an inactive mailbox to an existing mailbox. For more information about using this cmdlet, see [New-MailboxRestoreRequest](https://go.microsoft.com/fwlink/?linkid=856298).</span></span>
  
1. <span data-ttu-id="90836-125">Erstellen Sie eine Variable, die die Eigenschaften des inaktiven Postfachs enthält.</span><span class="sxs-lookup"><span data-stu-id="90836-125">Create a variable that contains the properties of the inactive mailbox.</span></span> 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="90836-p106">Verwenden Sie im vorherigen Befehl den Wert der Eigenschaft **DistinguishedName** oder **ExchangeGUID** zum Identifizieren des inaktiven Postfachs. Diese Eigenschaften sind für jedes Postfach in Ihrer Organisation eindeutig, wobei ein aktives und ein inaktives Postfach die gleiche primäre SMTP-Adresse haben können.</span><span class="sxs-lookup"><span data-stu-id="90836-p106">In the previous command, use the value of the **DistinguishedName** or **ExchangeGUID** property to identify the inactive mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active and an inactive mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="90836-p107">Speichern Sie den Inhalt des inaktiven Postfachs in ein vorhandenes Postfach zurück. Die Inhalte des inaktiven Postfachs (Quellpostfachs) werden in den entsprechenden Ordnern im vorhandenen Postfach (Zielpostfach) zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="90836-p107">Restore the contents of the inactive mailbox to an existing mailbox. The contents of the inactive mailbox (source mailbox) will be merged into the corresponding folders in the existing mailbox (target mailbox).</span></span>
    
    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -AllowLegacyDNMismatch
    ```
   
   <span data-ttu-id="90836-p108">Alternativ können Sie einen übergeordneten Ordner im Zielpostfach angeben, in den die Inhalte aus dem inaktiven Postfach rückgespeichert werden sollen. Wenn der angegebene Zielordner oder die angegebene Zielordnerstruktur nicht bereits im Zielpostfach vorhanden ist, wird es bzw. sie während des Rückspeichervorgangs erstellt.</span><span class="sxs-lookup"><span data-stu-id="90836-p108">Alternatively, you can specify a top-level folder in the target mailbox in which to restore the contents from the inactive mailbox. If the specified target folder or target folder structure doesn't already exist in the target mailbox, it is created during the restore process.</span></span> 
    
    <span data-ttu-id="90836-132">Im folgenden Beispiel werden Postfachelemente und Unterordner aus einem inaktiven Postfach in die übergeordnete Ordnerstruktur des Zielpostfachs in einen Ordner namens "Inactive Mailbox" kopiert.</span><span class="sxs-lookup"><span data-stu-id="90836-132">This example copies mailbox items and subfolders from an inactive mailbox to a folder named "Inactive Mailbox" in the top-level folder structure of the target mailbox.</span></span>
    
   ```
   New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -TargetMailbox newemployee@contoso.com -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
   ```
  
## <a name="restore-the-archive-from-an-inactive-mailbox"></a><span data-ttu-id="90836-133">Rückspeichern des Archivs aus einem inaktiven Postfach</span><span class="sxs-lookup"><span data-stu-id="90836-133">Restore the archive from an inactive mailbox</span></span>

<span data-ttu-id="90836-p109">Wenn ein inaktives Postfach ein Archivpostfach enthält, können Sie es auch im Archivpostfach eines vorhandenen Postfachs rückspeichern. Zum Rückspeichern des Archivs aus einem inaktiven Postfach müssen Sie die Schalter  _SourceIsArchive_ und  _TargetIsAchive_ dem Befehl hinzufügen, der zum Rückspeichern eines inaktiven Postfachs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90836-p109">If an inactive mailbox has an archive mailbox, you can also restore it to the archive mailbox of an existing mailbox. To restore the archive from an inactive mailbox, you have to add the  _SourceIsArchive_ and  _TargetIsAchive_ switches to the command used to restore an inactive mailbox.</span></span> 
  
1. <span data-ttu-id="90836-136">Erstellen Sie eine Variable, die die Eigenschaften des inaktiven Postfachs enthält.</span><span class="sxs-lookup"><span data-stu-id="90836-136">Create a variable that contains the properties of the inactive mailbox.</span></span> 
    
    ```
    $InactiveMailbox = Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox>
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="90836-p110">Verwenden Sie im vorherigen Befehl den Wert der Eigenschaft **DistinguishedName** oder **ExchangeGUID** zum Identifizieren des inaktiven Postfachs. Diese Eigenschaften sind für jedes Postfach in Ihrer Organisation eindeutig, wobei ein aktives und ein inaktives Postfach die gleiche primäre SMTP-Adresse haben können.</span><span class="sxs-lookup"><span data-stu-id="90836-p110">In the previous command, use the value of the **DistinguishedName** or **ExchangeGUID** property to identify the inactive mailbox. These properties are unique for each mailbox in your organization, whereas it's possible that an active and an inactive mailbox might have the same primary SMTP address.</span></span> 
  
2. <span data-ttu-id="90836-p111">Speichern Sie den Inhalt des Archivs aus dem inaktiven Postfach (Quellarchiv) in das Archiv eines vorhandenen Postfachs (Zielarchiv) zurück. Im folgenden Beispiel wird der Inhalt aus dem Quellarchiv in einen Ordner namens "Inactive Mailbox" im Archiv des Zielpostfachs kopiert.</span><span class="sxs-lookup"><span data-stu-id="90836-p111">Restore the contents of the archive from the inactive mailbox (source archive) to the archive of an existing mailbox (target archive). In this example, the contents from the source archive are copied to a folder named "Inactive Mailbox Archive" in the archive of the target mailbox.</span></span>

    ```
    New-MailboxRestoreRequest -SourceMailbox $InactiveMailbox.DistinguishedName -SourceIsArchive -TargetMailbox newemployee@contoso.com -TargetIsArchive -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
    ```

  
## <a name="more-information"></a><span data-ttu-id="90836-141">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="90836-141">More information</span></span>

- <span data-ttu-id="90836-p112">**Was ist der Hauptunterschied zwischen dem Wiederherstellen und dem Rückspeichern eines inaktiven Postfachs?** Wenn Sie ein inaktives Postfach wiederherstellen, wird das Postfach im Grunde in ein neues Postfach umgewandelt. Der Inhalt und die Ordnerstruktur des inaktiven Postfachs werden beibehalten, und das Postfach wird mit einem neuen Benutzerkonto verknüpft. Nach der Wiederherstellung ist das inaktive Postfach nicht mehr vorhanden. Alle Änderungen am Inhalt des neuen Postfachs wirken sich auf den Inhalt aus, der ursprünglich im inaktiven Postfach archiviert wurde. Wenn Sie ein inaktives Postfach hingegen rückspeichern, wird der Inhalt lediglich in ein anderes Postfach kopiert. Das inaktive Postfach bleibt als ein solches erhalten. Änderungen am Inhalt des Zielpostfachs wirken sich nicht auf den ursprünglichen Inhalt des inaktiven Postfachs aus. Das inaktive Postfach kann weiterhin mithilfe der [Inhaltssuche](run-a-content-search-in-the-security-and-compliance-center.md) im Office 365 Security &amp; Compliance Center durchsucht werden. Sein Inhalt kann in ein anderes Postfach rückgespeichert werden, oder es kann zu einem späteren Zeitpunkt wiederhergestellt oder gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="90836-p112">**What's the main difference between recovering and restoring an inactive mailbox?** When you recover an inactive mailbox, the mailbox is basically converted to a new mailbox, the contents and folder structure of the inactive mailbox are retained, and the mailbox is linked to a new user account. After it's recovered, the inactive mailbox no longer exists, and any changes made to the content in the new mailbox will affect the content that was originally on hold in the inactive mailbox. Conversely, when you restore an inactive mailbox, the contents are merely copied to another mailbox. The inactive mailbox is preserved and remains an inactive mailbox. Any changes made to the content in the target mailbox won't affect the original content held in the inactive mailbox. The inactive mailbox can still be searched by using the [Content Search tool](run-a-content-search-in-the-security-and-compliance-center.md) in the Office 365 Security &amp; Compliance Center, its contents can be restored to another mailbox, or it can be recovered or deleted at a later date.</span></span> 
    
- <span data-ttu-id="90836-p113">**Wie suchen Sie nach inaktiven Postfächern?** Zum Abrufen einer Liste der inaktiven Postfächer in Ihrer Organisation und Anzeigen von Informationen, die für das Rückspeichern eines inaktiven Postfachs nützlich sind, können Sie den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="90836-p113">**How do you find inactive mailboxes?** To get a list of the inactive mailboxes in your organization and display information that is useful for restoring an inactive mailbox, you can run this command.</span></span> 

  ```
  Get-Mailbox -InactiveMailboxOnly | FL Name,PrimarySMTPAddress,DistinguishedName,ExchangeGUID,LegacyExchangeDN,ArchiveStatus
  ```

- <span data-ttu-id="90836-p114">**Verwenden Sie ein Beweissicherungsverfahren oder eine Office 365-Aufbewahrungsrichtlinie zum Aufbewahren von Inhalten in inaktiven Postfächern.** Wenn Sie den Status eines inaktiven Postfachs nach dem Rückspeichern beibehalten möchten, können Sie für das Zielpostfach das [Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286) aktivieren oder eine [Office 365- Aufbewahrungsrichtlinie](retention-policies.md) anwenden, bevor Sie das inaktive Postfach rückspeichern. Dies verhindert das dauerhafte Löschen von Elementen aus dem inaktiven Postfach, nachdem sie in das Zielpostfach rückgespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="90836-p114">**Use a Litigation Hold or Office 365 retention policy to retain inactive mailbox content.** If you want to retain the state of an inactive mailbox after it's restored, you can place the target mailbox on [Litigation Hold](https://go.microsoft.com/fwlink/?linkid=856286) or apply an [Office 365 retention policy](retention-policies.md) before you restore the inactive mailbox. This will prevent the permanent deletion of any items from the inactive mailbox after they're restored to the target mailbox.</span></span> 
    
- <span data-ttu-id="90836-p115">**Aktivieren Sie die Aufbewahrungszeit für das Zielpostfach, bevor Sie ein inaktives Postfach wiederherstellen.** Da Postfachelemente aus einem inaktiven Postfach alt sein könnten, empfiehlt es sich, die Aufbewahrungszeit für das Zielpostfach zu aktivieren, bevor Sie ein inaktives Postfach wiederherstellen. Wenn Sie die Aufbewahrungszeit für ein Postfach aktivieren, wird die zugewiesene Aufbewahrungsrichtlinie erst verarbeitet, wenn die Aufbewahrungsdauer entfernt wird oder bis der Aufbewahrungszeitraum abgelaufen ist. Dadurch erhält der Besitzer des Zielpostfachs Zeit, alte Nachrichten aus dem inaktiven Postfach zu verwalten. Andernfalls kann die Aufbewahrungsrichtlinie alte Elemente löschen (oder Elemente in das Archivpostfach verschieben, sofern aktiviert), die basierend auf den für das Zielpostfach konfigurierten Aufbewahrungseinstellungen abgelaufen sind. Weitere Informationen finden Sie unter [platzieren der Aufbewahrungszeit für ein Postfach in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856300).</span><span class="sxs-lookup"><span data-stu-id="90836-p115">**Enable retention hold on the target mailbox before you restore an inactive mailbox.** Because mailbox items from an inactive mailbox could be old, you might consider enabling retention hold on the target mailbox before you restore an inactive mailbox. When you put a mailbox on retention hold, the retention policy that's assigned to it won't be processed until the retention hold is removed or until the retention hold period expires. This gives the owner of the target mailbox time to manage old messages from the inactive mailbox. Otherwise, the retention policy might delete old items (or move items to the archive mailbox, if it's enabled) that have expired based on the retention settings configured for the target mailbox. For more information, see [Place a mailbox on retention hold in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856300).</span></span>
    
- <span data-ttu-id="90836-p116">**Welche Funktion hat die Option „AllowLegacyDNMismatch"?** In den vorherigen Beispielen zum Rückspeichern eines inaktiven Postfachs wird die Option **AllowLegacyDNMismatch** verwendet, um das Rückspeichern des inaktiven Postfachs in ein anderes Zielpostfach zu erlauben. Ziel eines typischen Rückspeicherszenarios ist das Rückspeichern von Inhalten, bei denen das Quell- und Zielpostfach identisch sind. Standardmäßig prüft das Cmdlet **New-MailboxRestoreRequest** daher, ob der Wert der Eigenschaft **LegacyExchangeDN** für das Quell- und Zielpostfach identisch ist. Durch diese Prüfung wird vermieden, dass Sie versehentlich ein Quellpostfach im falschen Zielpostfach rückspeichern. Wenn Sie versuchen, ein inaktives Postfach ohne die Option **AllowLegacyDNMismatch** rückzuspeichern, kann es zu einem Fehler kommen, wenn das Quell- und Zielpostfach unterschiedliche Werte für die Eigenschaft **LegacyExchangeDN** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="90836-p116">**What does the AllowLegacyDNMismatch switch do?** In the previous examples to restore an inactive mailbox, the **AllowLegacyDNMismatch** switch is used to allow restoring the inactive mailbox to a different target mailbox. In a typical restore scenario, the goal is to restore content where the source and target mailboxes are the same mailbox. So by default, the **New-MailboxRestoreRequest** cmdlet checks to make sure that the value of the **LegacyExchangeDN** property on the source and target mailboxes is the same. This helps prevents you from accidentally restoring a source mailbox into the wrong target mailbox. If you try to restore an inactive mailbox without using the **AllowLegacyDNMismatch** switch, the command might fail if the source and target mailboxes have different values for the **LegacyExchangeDN** property.</span></span> 
    
- <span data-ttu-id="90836-p117">**Sie können andere Parameter mit dem Cmdlet "New-MailboxRestoreRequest" verwenden, um verschiedene Rückspeicherszenarien für inaktive Postfächer zu implementieren.** Sie können beispielsweise den folgenden Befehl ausführen, um das Archiv aus dem inaktiven Postfach im primären Postfach des Zielpostfachs rückzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="90836-p117">**You can use other parameters with the New-MailboxRestoreRequest cmdlet to implement different restore scenarios for inactive mailboxes.** For example, you can run this command to restore the archive from the inactive mailbox into the primary mailbox of the target mailbox.</span></span> 
    
  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -SourceIsArchive -TargetMailbox <target mailbox> -TargetRootFolder "Inactive Mailbox Archive" -AllowLegacyDNMismatch
  ```

  <span data-ttu-id="90836-168">Mit dem folgenden Befehl können auch das inaktive primäre Postfach im Archiv des Zielpostfachs rückspeichern.</span><span class="sxs-lookup"><span data-stu-id="90836-168">You can also restore the inactive primary mailbox into the archive of the target mailbox by running this command.</span></span>

  ```
  New-MailboxRestoreRequest -SourceMailbox <inactive mailbox> -TargetMailbox <target mailbox> -TargetIsArchive -TargetRootFolder "Inactive Mailbox" -AllowLegacyDNMismatch
  ```

- <span data-ttu-id="90836-p118">**Welche Funktion hat der Parameter "TargetRootFolder"?** Wie bereits erläutert, können Sie den Parameter **TargetRootFolder** verwenden, um einen Ordner in der oberen Ebene der Ordnerstruktur (den Stammordner) im Zielpostfach anzugeben, in den der Inhalt des inaktiven Postfachs rückgespeichert werden soll. Wenn Sie diesen Parameter nicht verwenden, werden Postfachelemente aus dem inaktiven Postfach in den entsprechenden Standardordnern des Zielpostfachs zusammengeführt, und benutzerdefinierte Ordner werden im Stammverzeichnis des Zielpostfachs neu erstellt. Die folgenden Abbildungen veranschaulichen die Unterschiede zwischen Verwendung oder Nichtverwendung des Parameters **TargetRootFolder**.</span><span class="sxs-lookup"><span data-stu-id="90836-p118">**What does the TargetRootFolder parameter do?** As previously explained, you can use the **TargetRootFolder** parameter to specify a folder in the top of the folder structure (also called the root) in the target mailbox in which to restore the contents of the inactive mailbox. If you don't use this parameter, mailbox items from the inactive mailbox are merged into the corresponding default folders of the target mailbox, and custom folders are re-created in the root of the target mailbox. The following illustrations highlight these differences between not using and using the **TargetRootFolder** parameter.</span></span> 
    
    <span data-ttu-id="90836-173">**Ordnerhierarchie im Zielpostfach, wenn der Parameter "TargetRootFolder" nicht verwendet wird**</span><span class="sxs-lookup"><span data-stu-id="90836-173">**Folder hierarchy in the target mailbox when the TargetRootFolder parameter isn't used**</span></span>
    
    ![Screenshot: Der Parameter „TargetRootFolder' wird nicht verwendet.](media/76a759af-f483-4d1c-8cc7-243435b5562e.png)
  
    <span data-ttu-id="90836-175">**Ordnerhierarchie im Zielpostfach, wenn der Parameter "TargetRootFolder" verwendet wird**</span><span class="sxs-lookup"><span data-stu-id="90836-175">**Folder hierarchy in the target mailbox when the TargetRootFolder parameter is used**</span></span>
    
    ![Screenshot: Der Parameter „TargetRootFolder' wird verwendet.](media/300da592-7323-48db-b8a4-07012259d113.png)

  

