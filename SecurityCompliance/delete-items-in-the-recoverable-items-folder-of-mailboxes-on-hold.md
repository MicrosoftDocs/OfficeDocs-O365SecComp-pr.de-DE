---
title: Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von Cloud-basierten Postfächern in Hold-Admin-Hilfe
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Für Administratoren: Löschen Sie Elemente im Ordner "Wiederherstellbare Elemente" eines Benutzers für ein Exchange Online-Postfach, auch wenn das Postfach in der gesetzlichen Aufbewahrungspflicht steht. Dies ist eine effektive Möglichkeit zum Löschen von Daten, die versehentlich in Office 365 verschüttet wurden.'
ms.openlocfilehash: f3518dc1009b4e95472473f76e6cd41011bc6b3e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216955"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a><span data-ttu-id="14a43-104">Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von Cloud-basierten Postfächern in Hold-Admin-Hilfe</span><span class="sxs-lookup"><span data-stu-id="14a43-104">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold - Admin Help</span></span>

<span data-ttu-id="14a43-p102">Der Ordner "Wiederherstellbare Elemente" für ein Exchange Online-Postfach ist vorhanden, um vor versehentlichen oder böswilligen Löschungen zu schützen. Es wird auch verwendet, um Elemente zu speichern, die von den Office 365-Kompatibilitätsfeatures, wie zum Beispiel Aufbewahrungs-und eDiscovery-suchen, gespeichert werden. In einigen Situationen können Organisationen jedoch Daten enthalten, die versehentlich im Ordner "Wiederherstellbare Elemente" aufbewahrt wurden, die Sie löschen müssen. Beispielsweise kann ein Benutzer unwissentlich eine e-Mail-Nachricht mit vertraulichen Informationen oder Informationen, die schwerwiegende geschäftliche Konsequenzen haben können, senden oder weiterleiten. Auch wenn die Nachricht dauerhaft gelöscht wird, wird Sie möglicherweise unbegrenzt aufbewahrt, da für das Postfach eine rechtliche Aufbewahrungspflicht festgestellt wurde. Dieses Szenario wird als Datenüberlauf bezeichnet, da Daten versehentlich in Office 365 verschüttet wurden. In diesen Situationen können Sie Elemente im Ordner "Wiederherstellbare Elemente" eines Benutzers für ein Exchange Online-Postfach löschen, auch wenn das Postfach mit einer der verschiedenen halte Features in Office 365 in der Warteschleife gespeichert wird. Zu diesen Aufbewahrungsarten gehört das Rechtsschutzverfahren, in-situ-Speicher, eDiscovery-Haltestatus und Office 365-Archivierungsrichtlinien &amp; , die im Office 365 Security Compliance Center erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="14a43-p102">The Recoverable Items folder for an Exchange Online mailbox exists to protect from accidental or malicious deletions. It's also used to store items that are retained and accessed by Office 365 compliance features, such as holds and eDiscovery searches. However, in some situations organizations might have data that's been unintentionally retained in the Recoverable Items folder that they must delete. For example, a user might unknowingly send or forward an email message that contains sensitive information or information that may have serious business consequences. Even if the message is permanently deleted, it might be retained indefinitely because a legal hold has been placed on the mailbox. This scenario is known as data spillage because data has been unintentionally spilled into Office 365. In these situations, you can delete items in a user's Recoverable Items folder for an Exchange Online mailbox, even if that mailbox is placed on hold with one of the different hold features in Office 365. These types of holds include Litigation Holds, In-Place Holds, eDiscovery holds, and Office 365 retention policies created in the Office 365 Security &amp; Compliance Center.</span></span> 
  
 <span data-ttu-id="14a43-p103">In diesem Artikel wird erläutert, wie Sie Elemente aus dem Ordner "Wiederherstellbare Elemente" für in der Warteschleife aktivierte Cloud-basierte Postfächer löschen. Dieses Verfahren beinhaltet das Deaktivieren des Zugriffs auf das Postfach und das Deaktivieren der Wiederherstellung einzelner Elemente, das Deaktivieren des Assistenten für verwaltete Ordner von der Verarbeitung des Postfachs, das vorübergehende Entfernen des haltebereichs, das Löschen von Elementen aus dem Ordner "Wiederherstellbare Elemente" und das anschließende Wiederherstellen die vorherige Konfiguration des Postfachs. Hier ist der Prozess:</span><span class="sxs-lookup"><span data-stu-id="14a43-p103">This article explains how to delete items from the Recoverable Items folder for cloud-based mailboxes that are on hold. This procedure involves disabling access to the mailbox and disabling single item recovery, disabling the Managed Folder Assistant from processing the mailbox, temporarily removing the hold, deleting items from the Recoverable Items folder, and then reverting the mailbox to its previous configuration. Here's the process:</span></span> 
  
[<span data-ttu-id="14a43-116">Schritt 1: Sammeln von Informationen über das Postfach</span><span class="sxs-lookup"><span data-stu-id="14a43-116">Step 1: Collect information about the mailbox</span></span>](#step-1-collect-information-about-the-mailbox)

[<span data-ttu-id="14a43-117">Schritt 2: Vorbereiten des Postfachs</span><span class="sxs-lookup"><span data-stu-id="14a43-117">Step 2: Prepare the mailbox</span></span>](#step-2-prepare-the-mailbox)

[<span data-ttu-id="14a43-118">Schritt 3: Entfernen aller haltebereiche aus dem Postfach</span><span class="sxs-lookup"><span data-stu-id="14a43-118">Step 3: Remove all holds from the mailbox</span></span>](#step-3-remove-all-holds-from-the-mailbox)

[<span data-ttu-id="14a43-119">Schritt 4: Entfernen des Verzögerungs Speichers aus dem Postfach</span><span class="sxs-lookup"><span data-stu-id="14a43-119">Step 4: Remove the delay hold from the mailbox</span></span>](#step-4-remove-the-delay-hold-from-the-mailbox)

[<span data-ttu-id="14a43-120">Schritt 5: Löschen von Elementen im Ordner "Wiederherstellbare Elemente"</span><span class="sxs-lookup"><span data-stu-id="14a43-120">Step 5: Delete items in the Recoverable Items folder</span></span>](#step-5-delete-items-in-the-recoverable-items-folder)

[<span data-ttu-id="14a43-121">Schritt 6: Zurücksetzen des Postfachs in den vorherigen Zustand</span><span class="sxs-lookup"><span data-stu-id="14a43-121">Step 6: Revert the mailbox to its previous state</span></span>](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> <span data-ttu-id="14a43-p104">Die in diesem Artikel beschriebenen Verfahren führen dazu, dass Daten dauerhaft aus einem Exchange Online-Postfach gelöscht werden. Das heißt, dass Nachrichten, die Sie aus dem Ordner "Wiederherstellbare Elemente" löschen, nicht wiederhergestellt werden können und nicht für rechtliche Ermittlungen oder andere Compliance-Zwecke zur Verfügung stehen. Wenn Sie Nachrichten aus einem Postfach löschen möchten, das im Rahmen eines Rechtsstreits, eines in-situ-Speichers, einer eDiscovery-Speicherung oder einer im Office 365 Security &amp; Compliance Center erstellten Office 365-Aufbewahrungsrichtlinie aufbewahrt wird, erkundigen Sie sich bei ihrer Datensatzverwaltung oder den gesetzlichen Bestimmungen. Abteilungen vor dem Entfernen des haltebereichs. Ihre Organisation verfügt möglicherweise über eine Richtlinie, die definiert, ob ein Postfach in der Warteschleife oder ein Vorfall mit Daten ausschütten Vorrang hat.</span><span class="sxs-lookup"><span data-stu-id="14a43-p104">The procedures outlined in this article will result in data being permanently deleted (purged) from an Exchange Online mailbox. That means messages that you delete from the Recoverable Items folder can't be recovered and won't be available for legal discovery or other compliance purposes. If you want to delete messages from a mailbox that's placed on hold as part of a Litigation Hold, In-Place Hold, eDiscovery hold, or Office 365 retention policy created in the Office 365 Security &amp; Compliance Center, check with your records management or legal departments before removing the hold. Your organization might have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="14a43-126">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="14a43-126">Before you begin</span></span>

- <span data-ttu-id="14a43-127">Sie müssen beide der folgenden Verwaltungsrollen in Exchange Online zugewiesen sein, um nach Nachrichten aus dem Ordner "Wiederherstellbare Elemente" in Schritt 5 zu suchen und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="14a43-127">You have to be assigned both of the following management roles in Exchange Online to search for and delete messages from the Recoverable Items folder in Step 5.</span></span>
    
  - <span data-ttu-id="14a43-p105">**Postfachsuche** – mit dieser Rolle können Sie Postfächer in Ihrer Organisation durchsuchen. Exchange-Administratoren werden standardmäßig nicht dieser Rolle zugewiesen. Wenn Sie diese Rolle zuweisen möchten, fügen Sie sich selbst als Mitglied der Rollengruppe "Discoveryverwaltung" in Exchange Online hinzu.</span><span class="sxs-lookup"><span data-stu-id="14a43-p105">**Mailbox Search** - This role lets you to search mailboxes in your organization. Exchange administrators aren't assigned this role by default. To assign yourself this role, add yourself as a member of the Discovery Management role group in Exchange Online.</span></span> 
    
  - <span data-ttu-id="14a43-p106">**Post Fach Import** – mit dieser Rolle können Sie Nachrichten aus dem Postfach eines Benutzers löschen. Diese Rolle wird standardmäßig keiner Rollengruppe zugewiesen. Zum Löschen von Nachrichten aus Benutzerpostfächern können Sie die Rolle "Post Fach Import-Export" zur Rollengruppe "Organisationsverwaltung" in Exchange Online hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="14a43-p106">**Mailbox Import Export** - This role lets you to delete messages from a user's mailbox. By default, this role isn't assigned to any role group. To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> 
    
- <span data-ttu-id="14a43-p107">Das in diesem Artikel beschriebene Verfahren wird für inaktive Postfächer nicht unterstützt. Das liegt daran, dass Sie nach dem Entfernen eine Aufbewahrungsrichtlinie (oder eine Office-365-Richtlinie) nicht mehr auf ein inaktives Postfach anwenden können. Wenn Sie einen Haltebereich aus einem inaktiven Postfach entfernen, wird er in ein normales gelöschtes Postfach geändert und dauerhaft aus Ihrer Organisation gelöscht, nachdem es vom Assistenten für verwaltete Ordner verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="14a43-p107">The procedure described in this article isn't supported for inactive mailboxes. That's because you can't re-apply a hold (or Office 365 retention policy) to an inactive mailbox after you remove it. When you remove a hold from an inactive mailbox, it's changed to a normal soft-deleted mailbox and will be permanently deleted from your organization after it's processed by the Managed Folder Assistant.</span></span>
    
- <span data-ttu-id="14a43-p108">Sie können dieses Verfahren nicht für ein Postfach ausführen, das einer Office 365-Aufbewahrungsrichtlinie zugewiesen wurde, die mit einer Aufbewahrungs Sperre gesperrt wurde. Das liegt daran, dass Sie durch eine Aufbewahrungs Sperre das Entfernen oder ausschließen des Postfachs aus der Office 365-Aufbewahrungsrichtlinie und das Deaktivieren des Assistenten für verwaltete Ordner für das Postfach verhindern. Weitere Informationen zum Sperren von Aufbewahrungsrichtlinien finden Sie unter [Sperren einer Aufbewahrungsrichtlinie](retention-policies.md#locking-a-retention-policy).</span><span class="sxs-lookup"><span data-stu-id="14a43-p108">You can't perform this procedure for a mailbox that has been assigned to an Office 365 retention policy that's been locked with a Preservation Lock. That's because a Preservation Lock prevents you from removing or excluding the mailbox from the Office 365 retention policy and from disabling the Managed Folder Assistant on the mailbox. For more information about locking retention policies, see [Locking a retention policy](retention-policies.md#locking-a-retention-policy).</span></span>
    
- <span data-ttu-id="14a43-p109">Wenn ein Postfach nicht gehalten wird (oder die Wiederherstellung einzelner Elemente nicht aktiviert ist), können Sie die Elemente einfach aus dem Ordner "Wiederherstellbare Elemente" löschen. Weitere Informationen dazu finden Sie unter [Suchen nach und Löschen von Nachrichten ](https://go.microsoft.com/fwlink/?linkid=852453).</span><span class="sxs-lookup"><span data-stu-id="14a43-p109">If a mailbox isn't placed on hold (or doesn't have single item recovery enabled), you can simply delete the items from the Recoverable Items folder. For more information about how to do this, see [Search for and delete messages ](https://go.microsoft.com/fwlink/?linkid=852453).</span></span>
  
## <a name="step-1-collect-information-about-the-mailbox"></a><span data-ttu-id="14a43-142">Schritt 1: Sammeln von Informationen über das Postfach</span><span class="sxs-lookup"><span data-stu-id="14a43-142">Step 1: Collect information about the mailbox</span></span>

<span data-ttu-id="14a43-p110">Dieser erste Schritt besteht darin, ausgewählte Eigenschaften aus dem Zielpostfach zu sammeln, die sich auf diese Prozedur auswirken. Notieren Sie sich diese Einstellungen, oder speichern Sie Sie in einer Textdatei, da Sie einige dieser Eigenschaften ändern und dann auf die ursprünglichen Werte in Schritt 6 zurücksetzen, nachdem Sie Elemente aus dem Ordner "Wiederherstellbare Elemente" gelöscht haben. Hier finden Sie eine Liste der Postfacheigenschaften, die Sie sammeln müssen.</span><span class="sxs-lookup"><span data-stu-id="14a43-p110">This first step is to collect selected properties from the target mailbox that will affect this procedure. Be sure to write down these settings or save them to a text file because you'll change some of these properties and then revert back to the original values in Step 6, after you delete items from the Recoverable Items folder. Here's a list of the mailbox properties you need to collect.</span></span>
  
-  <span data-ttu-id="14a43-146">*SingleItemRecoveryEnabled* und *Parameter RetainDeletedItemsFor* ; Falls erforderlich, deaktivieren Sie einzelne Wiederherstellung, und erweitern Sie den Aufbewahrungszeitraum für gelöschte Elemente in Schritt 3.</span><span class="sxs-lookup"><span data-stu-id="14a43-146">*SingleItemRecoveryEnabled*  and  *RetainDeletedItemsFor*  ; if necessary, you'll disable single recovery and increase the deleted items retention period in Step 3.</span></span> 
    
-  <span data-ttu-id="14a43-p111">*LitigationHoldEnabled* und *InPlaceHolds* ; Sie müssen alle für das Postfach festgelegten haltebereiche identifizieren, damit Sie Sie vorübergehend in Schritt 3 entfernen können. Im Abschnitt [Weitere Informationen](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) finden Sie Tipps dazu, wie Sie den Typ Hold identifizieren, der möglicherweise in einem Postfach gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="14a43-p111">*LitigationHoldEnabled*  and  *InPlaceHolds*  ; you need to identify all the holds placed on the mailbox so that you can temporarily remove them in Step 3. See the [More information](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> 
    
<span data-ttu-id="14a43-p112">Darüber hinaus müssen Sie die Einstellungen für den Post Fach Clientzugriff abrufen, damit Sie Sie vorübergehend deaktivieren können, damit der Besitzer (oder andere Benutzer) während dieses Verfahrens nicht auf das Postfach zugreifen kann. Schließlich können Sie die aktuelle Größe und Anzahl der Elemente im Ordner "Wiederherstellbare Elemente" abrufen. Nachdem Sie Elemente im Ordner "Wiederherstellbare Elemente" in Schritt 5 gelöscht haben, verwenden Sie diese Informationen, um zu überprüfen, ob die Elemente tatsächlich entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="14a43-p112">Additionally, you need to get the mailbox client access settings so you can temporarily disable them so the owner (or other users) can't access the mailbox during this procedure. Finally, you can get the current size and number of items in the Recoverable Items folder. After you delete items in the Recoverable Items folder in Step 5, you'll use this information to verify that items were actually removed.</span></span>
  
1. <span data-ttu-id="14a43-p113">Stellen [Sie eine Verbindung mit Exchange Online PowerShell her](https://go.microsoft.com/fwlink/?linkid=396554). Achten Sie darauf, einen Benutzernamen und ein Kennwort für ein Administratorkonto zu verwenden, dem die entsprechenden Verwaltungsrollen in Exchange Online zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="14a43-p113">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Be sure to use a user name and password for an administrator account that's been assigned the appropriate management roles in Exchange Online.</span></span> 
    
2. <span data-ttu-id="14a43-154">Führen Sie den folgenden Befehl aus, um Informationen zur Wiederherstellung einzelner Elemente und zur Aufbewahrungsdauer für gelöschte Elemente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14a43-154">Run the following command to get information about single item recovery and the deleted item retention period.</span></span>

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   <span data-ttu-id="14a43-p114">Wenn die Wiederherstellung einzelner Elemente aktiviert ist, müssen Sie Sie in Schritt 2 deaktivieren. Wenn der Aufbewahrungszeitraum für gelöschte Elemente für 30 Tage (der Höchstwert in Exchange Online) nicht festgelegt ist, können Sie ihn in Schritt 2 erweitern.</span><span class="sxs-lookup"><span data-stu-id="14a43-p114">If single item recovery is enabled, you'll have to disable it in Step 2. If the deleted item retention period isn't set for 30 days (the maximum value in Exchange Online), then you can increase it in Step 2.</span></span> 
    
3. <span data-ttu-id="14a43-157">Führen Sie den folgenden Befehl aus, um die Einstellungen für den Postfachzugriff für das Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14a43-157">Run the following command to get the mailbox access settings for the mailbox.</span></span> 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   <span data-ttu-id="14a43-158">In Schritt 2 werden alle diese Zugriffsmethoden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="14a43-158">You'll disable all of these access methods in Step 2.</span></span>
    
4. <span data-ttu-id="14a43-159">Führen Sie den folgenden Befehl aus, um Informationen zu den Haltebereichen und Office 365-Aufbewahrungsrichtlinien für das Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14a43-159">Run the following command to get information about the holds and Office 365 retention policies applied to the mailbox.</span></span>
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > <span data-ttu-id="14a43-160">Wenn die *InPlaceHolds* -Eigenschaft zu viele Werte enthält und nicht alle angezeigt werden, können Sie den `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` Befehl ausführen, um jeden Wert in einer separaten Zeile anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="14a43-160">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
5. <span data-ttu-id="14a43-161">Führen Sie den folgenden Befehl aus, um Informationen zu organisationsweiten Office 365-Aufbewahrungsrichtlinien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14a43-161">Run the following command to get information about any organization-wide Office 365 retention policies.</span></span> 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   <span data-ttu-id="14a43-162">Wenn Ihre Organisation über organisationsweite Office 365-Aufbewahrungsrichtlinien verfügt, müssen Sie das Postfach in Schritt 3 aus diesen Richtlinien ausschließen.</span><span class="sxs-lookup"><span data-stu-id="14a43-162">If your organization has any organization-wide Office 365 retention policies, you'll have to exclude the mailbox from these policies in Step 3.</span></span>

   > [!TIP]
    > <span data-ttu-id="14a43-163">Wenn die *InPlaceHolds* -Eigenschaft zu viele Werte enthält und nicht alle angezeigt werden, können Sie den `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` Befehl ausführen, um jeden Wert in einer separaten Zeile anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="14a43-163">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
6. <span data-ttu-id="14a43-164">Führen Sie den folgenden Befehl aus, um die aktuelle Größe und Gesamtanzahl von Elementen in Ordnern und Unterordnern im Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14a43-164">Run the following command to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="14a43-165">Wenn das Archivpostfach des Benutzers aktiviert ist, führen Sie den folgenden Befehl aus, um die Größe und Gesamtanzahl von Elementen in Ordnern und Unterordnern im Ordner "Wiederherstellbare Elemente" in Ihrem Archivpostfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14a43-165">If the user's archive mailbox is enabled, run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in their archive mailbox.</span></span> 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="14a43-p115">Wenn Sie Elemente in Schritt 5 löschen, können Sie auswählen, ob Elemente im Ordner "Wiederherstellbare Elemente" im primären Archivpostfach des Benutzers gelöscht oder nicht gelöscht werden sollen. Beachten Sie, dass Elemente in einem zusätzlichen Archivpostfach nicht gelöscht werden, wenn die automatische Erweiterung der Archivierung für das Postfach aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="14a43-p115">When you delete items in Step 5, you can choose to delete or not delete items in the Recoverable Items folder in the user's primary archive mailbox. Note that if auto-expanding archiving is enabled for the mailbox, items in an auxiliary archive mailbox won't be deleted.</span></span>
  
## <a name="step-2-prepare-the-mailbox"></a><span data-ttu-id="14a43-168">Schritt 2: Vorbereiten des Postfachs</span><span class="sxs-lookup"><span data-stu-id="14a43-168">Step 2: Prepare the mailbox</span></span>

<span data-ttu-id="14a43-169">Nachdem Sie Informationen zum Postfach gesammelt und gespeichert haben, besteht der nächste Schritt im Vorbereiten des Postfachs, indem Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="14a43-169">After collecting and saving information about the mailbox, the next step is to prepare the mailbox by performing the following tasks:</span></span> 
  
- <span data-ttu-id="14a43-170">**Deaktivieren Sie den Clientzugriff auf das Postfach** , sodass der Postfachbesitzer während dieses Verfahrens nicht auf sein Postfach zugreifen und Änderungen an den Postfachdaten vornehmen kann.</span><span class="sxs-lookup"><span data-stu-id="14a43-170">**Disable client access to mailbox** so that the mailbox owner can't access their mailbox and make any changes to the mailbox data during this procedure.</span></span> 
    
- <span data-ttu-id="14a43-171">**Verlängern Sie die Aufbewahrungsdauer für gelöschte** Elemente auf 30 Tage (den Höchstwert in Exchange Online), sodass Elemente nicht aus dem Ordner "Wiederherstellbare Elemente" gelöscht werden, bevor Sie Sie in Schritt 5 löschen können.</span><span class="sxs-lookup"><span data-stu-id="14a43-171">**Increase the deleted item retention period** to 30 days (the maximum value in Exchange Online) so that items aren't purged from the Recoverable Items folder before you can delete them in Step 5.</span></span> 
    
- <span data-ttu-id="14a43-172">**Deaktivieren Sie die Wiederherstellung einzelner** Elemente, damit Elemente (für die Dauer des Aufbewahrungszeitraums für gelöschte Elemente) nicht aufbewahrt werden, nachdem Sie Sie aus dem Ordner "Wiederherstellbare Elemente" in Schritt 5 gelöscht haben.</span><span class="sxs-lookup"><span data-stu-id="14a43-172">**Disable single Item recovery** so that items won't be retained (for the duration of the deleted item retention period) after you delete them from the Recoverable Items folder in Step 5.</span></span> 
    
- <span data-ttu-id="14a43-173">**Deaktivieren Sie den Assistenten für verwaltete Ordner** , sodass er das Postfach nicht verarbeitet und die Elemente, die Sie in Schritt 5 löschen, nicht aufbewahren.</span><span class="sxs-lookup"><span data-stu-id="14a43-173">**Disable the Managed Folder Assistant** so that it doesn't process the mailbox and retain the items that you delete in Step 5.</span></span> 
    
<span data-ttu-id="14a43-174">Führen Sie die folgenden Schritte in Exchange Online PowerShell aus.</span><span class="sxs-lookup"><span data-stu-id="14a43-174">Perform the following steps in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="14a43-p116">Führen Sie den folgenden Befehl aus, um den gesamten Clientzugriff auf das Postfach zu deaktivieren. Bei der Befehlssyntax wird davon ausgegangen, dass alle Clientzugriffsmethoden für das Postfach aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="14a43-p116">Run the following command to disable all client access to the mailbox. The command syntax assumes that all client access methods were enabled on the mailbox.</span></span>

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > <span data-ttu-id="14a43-p117">Es kann bis zu 60 Minuten dauern, bis alle Clientzugriffsmethoden für das Postfach deaktiviert wurden. Beachten Sie, dass durch das Deaktivieren dieser Zugriffsmethoden der Postfachbesitzer, den Sie derzeit angemeldet haben, nicht getrennt wird. Wenn der Besitzer nicht angemeldet ist, kann er nicht mehr auf sein Postfach zugreifen, nachdem diese Zugriffsmethoden deaktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="14a43-p117">It might take up to 60 minutes to disable all client access methods to the mailbox. Note that disabling these access methods won't disconnect the mailbox owner they're currently signed in. If the owner isn't signed in, then they won't be able to access their mailbox after these access methods are disabled.</span></span> 
  
2. <span data-ttu-id="14a43-p118">Führen Sie den folgenden Befehl aus, um die Aufbewahrungsdauer für gelöschte Elemente um maximal 30 Tage zu verlängern. Dabei wird davon ausgegangen, dass die aktuelle Einstellung weniger als 30 Tage beträgt.</span><span class="sxs-lookup"><span data-stu-id="14a43-p118">Run the following command to increase the deleted item retention period the maximum of 30 days. This assumes that the current setting is less than 30 days.</span></span> 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. <span data-ttu-id="14a43-182">Führen Sie den folgenden Befehl aus, um die Wiederherstellung einzelner Elemente zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="14a43-182">Run the following command to disable single item recovery.</span></span>
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > <span data-ttu-id="14a43-p119">Es kann bis zu 60 Minuten dauern, bis die Wiederherstellung einzelner Elemente deaktiviert ist. Löschen Sie keine Elemente im Ordner "Wiederherstellbare Elemente", bis dieser Zeitraum abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="14a43-p119">It might take up to 60 minutes to disable single item recovery. Don't delete items in the Recoverable Items folder until this period has elapsed.</span></span> 
  
4. <span data-ttu-id="14a43-p120">Führen Sie den folgenden Befehl aus, um zu verhindern, dass der Assistent für verwaltete Ordner das Postfach verarbeitet. Wie bereits erläutert, können Sie den Assistenten für verwaltete Ordner nur deaktivieren, wenn keine Office 365-Aufbewahrungsrichtlinie mit einer erHaltungs Sperre auf das Postfach angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="14a43-p120">Run the following command to prevent the Managed Folder Assistant from processing the mailbox. As previously explained, you can disable the Managed Folder Assistant only if an Office 365 retention policy with a Preservation Lock is not applied to the mailbox.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a><span data-ttu-id="14a43-187">Schritt 3: Entfernen aller haltebereiche aus dem Postfach</span><span class="sxs-lookup"><span data-stu-id="14a43-187">Step 3: Remove all holds from the mailbox</span></span>

<span data-ttu-id="14a43-p121">Der letzte Schritt, bevor Sie Elemente aus dem Ordner "Wiederherstellbare Elemente" löschen können, besteht darin, alle haltebereiche (die Sie in Schritt 1 identifiziert haben) für das Postfach zu entfernen. Alle haltebereiche müssen entfernt werden, damit Elemente nicht aufbewahrt werden, nachdem Sie Sie aus dem Ordner "Wiederherstellbare Elemente" gelöscht haben. Die folgenden Abschnitte enthalten Informationen zum Entfernen unterschiedlicher Aufbewahrungs Typen für ein Postfach. Im Abschnitt [Weitere Informationen](#more-information) finden Sie Tipps dazu, wie Sie den Typ Hold identifizieren, der möglicherweise in einem Postfach gespeichert wird. Weitere Informationen finden Sie unter [Vorgehensweise beim Identifizieren des Aufbewahrungs Typs für ein Exchange Online-Postfach](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="14a43-p121">The last step before you can delete items from the Recoverable Items folder is to remove all holds (that you identified in Step 1) placed on the mailbox. All holds must be removed so that items won't be retained after you delete them from the Recoverable Items folder. The following sections contain information about removing different types of holds on a mailbox. See the [More information](#more-information) section for tips about how to identify the type hold that might be placed on a mailbox. For additional information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>
  
> [!CAUTION]
> <span data-ttu-id="14a43-193">Wie bereits erwähnt, erkundigen Sie sich bei ihrer Datensatzverwaltung oder Rechtsabteilung vor dem Entfernen eines haltebereichs aus einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="14a43-193">As previously stated, check with your records management or legal departments before removing a hold from a mailbox.</span></span> 
  
 ### <a name="litigation-hold"></a><span data-ttu-id="14a43-194">Beweissicherungsverfahren</span><span class="sxs-lookup"><span data-stu-id="14a43-194">Litigation Hold</span></span>
  
<span data-ttu-id="14a43-195">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Beweissicherung aus dem Postfach zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="14a43-195">Run the following command in Exchange Online PowerShell to remove a Litigation Hold from the mailbox.</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> <span data-ttu-id="14a43-p122">Ähnlich wie bei der Deaktivierung der Clientzugriffsmethoden und der Wiederherstellung einzelner Elemente kann es bis zu 60 Minuten dauern, bis die Beweissicherung entfernt wurde. Löschen Sie keine Elemente aus dem Ordner "Wiederherstellbare Elemente", bis dieser Zeitraum abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="14a43-p122">Similar to disabling the client access methods and single item recovery, it might take up to 60 minutes to remove the Litigation Hold. Don't delete items from the Recoverable Items folder until this period has elapsed.</span></span> 
  
 ### <a name="in-place-hold"></a><span data-ttu-id="14a43-198">Compliance-Archiv</span><span class="sxs-lookup"><span data-stu-id="14a43-198">In-Place Hold</span></span>
  
<span data-ttu-id="14a43-p123">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den in-situ-Speicher für das Postfach zu identifizieren. Verwenden Sie die GUID für den in-situ-Speicher, den Sie in Schritt 1 identifiziert haben.</span><span class="sxs-lookup"><span data-stu-id="14a43-p123">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's placed on the mailbox. Use the GUID for the In-Place Hold that you identified in Step 1.</span></span> 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
<span data-ttu-id="14a43-p124">Nachdem Sie den in-situ-Speicher identifiziert haben, können Sie die Exchange-Verwaltungskonsole (EAC) oder Exchange Online PowerShell verwenden, um das Postfach aus dem Haltebereich zu entfernen. Weitere Informationen finden Sie unter [erstellen oder Entfernen eines in-situ-](https://go.microsoft.com/fwlink/?linkid=852668)Speichers.</span><span class="sxs-lookup"><span data-stu-id="14a43-p124">After you identify the In-Place Hold, you can use the Exchange admin center (EAC) or Exchange Online PowerShell to remove the mailbox from the hold. For more information, see [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span></span>
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a><span data-ttu-id="14a43-203">Office 365-Aufbewahrungsrichtlinien, die auf bestimmte Postfächer angewendet werden</span><span class="sxs-lookup"><span data-stu-id="14a43-203">Office 365 retention policies applied to specific mailboxes</span></span>
  
<span data-ttu-id="14a43-p125">Führen Sie den folgenden Befehl in [office 365 &amp; Security Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) aus, um die auf das postfach angewendete Office 365-Aufbewahrungsrichtlinie zu identifizieren. Verwenden Sie die GUID (ohne das `mbx` Präfix `skp` oder) für die Aufbewahrungsrichtlinie, die Sie in Schritt 1 identifiziert haben.</span><span class="sxs-lookup"><span data-stu-id="14a43-p125">Run the following command in [Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the Office 365 retention policy that is applied to the mailbox. Use the GUID (not including the  `mbx` or  `skp` prefix) for the retention policy that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
<span data-ttu-id="14a43-206">Nachdem Sie die Aufbewahrungsrichtlinie identifiziert haben, wechseln Sie zur Seite Aufbewahrungszeit für &amp; die **Datenverwaltung** \> \*\*\*\* im Security Compliance Center, bearbeiten Sie die Aufbewahrungsrichtlinie, die Sie im vorherigen Schritt identifiziert haben, und entfernen Sie das Postfach aus der Liste der Empfänger, die in der Aufbewahrungsrichtlinie enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="14a43-206">After you identify the retention policy, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy that you identified in the previous step, and remove the mailbox from the list of recipients that are included in the retention policy.</span></span> 
  
 ### <a name="organization-wide-office-365-retention-policies"></a><span data-ttu-id="14a43-207">Organisationsweite Office 365-Aufbewahrungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="14a43-207">Organization-wide Office 365 retention policies</span></span>
  
<span data-ttu-id="14a43-p126">Organisationsweite und Exchange-weite Office 365-Aufbewahrungsrichtlinien werden auf jedes Postfach in der Organisation angewendet. Sie werden auf Organisationsebene (nicht auf die Postfachebene) angewendet und werden zurückgegeben, wenn Sie das Cmdlet **Get-OrganizationConfig** in Schritt 1 ausführen. Führen Sie den folgenden Befehl [in &amp; Security Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) aus, um die organisationsweiten Office 365-Aufbewahrungsrichtlinien zu identifizieren. Verwenden Sie die GUID (ohne `mbx` Präfix) für die organisationsweiten Aufbewahrungsrichtlinien, die Sie in Schritt 1 identifiziert haben.</span><span class="sxs-lookup"><span data-stu-id="14a43-p126">Organization-wide and Exchange-wide Office 365 retention policies are applied to every mailbox in the organization. They are applied at the organization level (not the mailbox level) and are returned when you run the **Get-OrganizationConfig** cmdlet in Step 1. Run the following command in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the organization-wide Office 365 retention policies. Use the GUID (not including the  `mbx` prefix) for the organization-wide retention policies that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

<span data-ttu-id="14a43-p127">nachdem sie die organisationsweiten Office 365-aufbewahrungsrichtlinien identifiziert haben, navigieren sie im &amp; Security Compliance Center zur seite zur **aufbewahrung** der **datenverwaltung** \> , und bearbeiten sie jede organisationsweite aufbewahrungsrichtlinie, die sie im vorherigen Schritt, und fügen Sie das Postfach zur Liste der ausgeschlossenen Empfänger hinzu. Dadurch wird das Postfach des Benutzers aus der Aufbewahrungsrichtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="14a43-p127">After you identify the organization-wide Office 365 retention policies, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit each organization-wide retention policy that you identified in the previous step, and add the mailbox to the list of excluded recipients. Doing this will remove the user's mailbox from the retention policy.</span></span> 

### <a name="office-365-retention-labels"></a><span data-ttu-id="14a43-214">Office 365-Aufbewahrungs Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="14a43-214">Office 365 retention labels</span></span>

<span data-ttu-id="14a43-p128">Wenn ein Benutzer eine Bezeichnung anwendet, die so konfiguriert ist, dass Inhalte aufbewahrt oder aufbewahrt und dann Inhalte in einem beliebigen Ordner oder Element in Ihrem Postfach gelöscht werden, wird die *ComplianceTagHoldApplied* -Postfacheigenschaft auf **true**festgelegt. Wenn dies der Fall ist, wird das Postfach als in der Warteschleife gehalten, so als ob es in einem Rechtsstreit gehalten oder einer Office 365-Aufbewahrungsrichtlinie zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="14a43-p128">Whenever a user applies a label that's configured to retain content or retain and then delete content to any folder or item in their mailbox, the *ComplianceTagHoldApplied* mailbox property is set to **True**. When this happens, the mailbox is considered to be on hold, just as if it was placed on Litigation Hold or assigned to an Office 365 retention policy.</span></span>

<span data-ttu-id="14a43-217">Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den Wert der *ComplianceTagHoldApplied* -Eigenschaft anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="14a43-217">To view the value of the *ComplianceTagHoldApplied* property, run the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

<span data-ttu-id="14a43-p129">Nachdem Sie festgestellt haben, dass ein Postfach in der Warteschleife ist, weil eine Aufbewahrungs Bezeichnung auf einen Ordner oder ein Element angewendet wird, können Sie das Inhaltssuche-Tool im Security & Compliance Center verwenden, um mithilfe der ComplianceTag-Suchbedingung nach beschrifteten Elementen zu suchen. Weitere Informationen finden Sie im Abschnitt "Suchbedingungen" in [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span><span class="sxs-lookup"><span data-stu-id="14a43-p129">After you've identified that a mailbox is on hold because a retention label is applied to a folder or item, you can use the Content Search tool in the Security & Compliance Center to search for labeled items by using the ComplianceTag search condition. For more information, see the "Search conditions" section in [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md#conditions-for-common-properties).</span></span>

<span data-ttu-id="14a43-220">Weitere Informationen zu Bezeichnungen finden Sie unter [Overview of Office 365 Labels](labels.md).</span><span class="sxs-lookup"><span data-stu-id="14a43-220">For more information about labels, see [Overview of Office 365 labels](labels.md).</span></span>

 ### <a name="ediscovery-case-holds"></a><span data-ttu-id="14a43-221">eDiscovery-Fall enthält</span><span class="sxs-lookup"><span data-stu-id="14a43-221">eDiscovery case holds</span></span>
  
<span data-ttu-id="14a43-p130">Führen Sie die folgenden Befehle [in &amp; Security Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) aus, um den Haltebereich zu identifizieren, der einem eDiscovery-Fall zugeordnet ist, der auf das Postfach angewendet wird. Verwenden Sie die GUID (ohne `UniH` Präfix) für den eDiscovery-Speicher, den Sie in Schritt 1 identifiziert haben. Beachten Sie, dass mit dem zweiten Befehl der Name des eDiscovery-falls angezeigt wird, dem der Haltebereich zugeordnet ist. der dritte Befehl zeigt den Namen des Haltestatus an.</span><span class="sxs-lookup"><span data-stu-id="14a43-p130">Run the following commands in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the hold associated with an eDiscovery case that's applied to the mailbox. Use the GUID (not including the  `UniH` prefix) for the eDiscovery hold that you identified in Step 1. Note that the second command displays the name of the eDiscovery case the hold is associated with; the third command displays the name of the hold.</span></span> 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

<span data-ttu-id="14a43-p131">Nachdem Sie den Namen des eDiscovery-Falls und den Haltestatus ermittelt haben, wechseln Sie im &amp; Security Compliance Center zur \> **eDiscovery** -Seite für die \*\*Suche &amp; \*\* , öffnen Sie den Fall, und entfernen Sie das Postfach aus dem Haltebereich. Weitere Informationen finden Sie unter [Verwalten von eDiscovery-Fällen im Office 365 &amp; Security Compliance Center](manage-ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="14a43-p131">After you've identified the name of the eDiscovery case and the hold, go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and remove the mailbox from the hold. For more information, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md).</span></span>
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a><span data-ttu-id="14a43-227">Schritt 4: Entfernen des Verzögerungs Speichers aus dem Postfach</span><span class="sxs-lookup"><span data-stu-id="14a43-227">Step 4: Remove the delay hold from the mailbox</span></span>

<span data-ttu-id="14a43-p132">Nachdem ein Aufbewahrungs aus einem Postfach entfernt wurde, wird der Wert der *DelayHoldApplied* -Postfacheigenschaft auf **true**festgelegt. Dies tritt auf, wenn der Assistent für verwaltete Ordner das nächste Mal das Postfach verarbeitet und erkennt, dass ein Haltebereich entfernt wurde. Dies wird als *Verzögerungs Sperre* bezeichnet und bedeutet, dass das tatsächliche Entfernen des Haltestatus für 30 Tage verzögert wird, um zu verhindern, dass Daten dauerhaft aus dem Postfach gelöscht werden. (Der Zweck einer Verzögerungs Sperre besteht darin, Administratoren die Möglichkeit zu geben, Postfachelemente zu suchen oder wiederherzustellen, die nach dem Entfernen eines Haltestatus gelöscht werden.)  Wenn ein Verzögerungs Speicher für das Postfach gespeichert wird, wird das Postfach für eine unbegrenzte Dauer nach wie vor als für das Postfach aktiviert gehalten. Nach 30 Tagen wird die Verzögerungsdauer abgelaufen, und Office 365 versucht automatisch, die Verzögerungsdauer zu entfernen (indem Sie die *DelayHoldApplied* -Eigenschaft auf **false**festlegen), sodass der Haltebereich tatsächlich entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="14a43-p132">After any type of hold is removed from a mailbox, the value of the *DelayHoldApplied* mailbox property is set to **True**. This occurs the next time the Managed Folder Assistant processes the mailbox and detects that a hold has been removed. This is called a *delay hold* and means the actual removal of the hold is delayed for 30 days to prevent data from being permanently deleted from the mailbox. (The purpose of a delay hold is to give admins an opportunity to search for or recover mailbox items that will be purged after a hold is removed.)  When a delay hold is placed on the mailbox, the mailbox is still considered to be on hold for an unlimited duration, as if the mailbox was on Litigation Hold. After 30 days, the delay hold expires, and Office 365 will automatically attempt to remove the delay hold (by setting the *DelayHoldApplied* property to **False**) so that the hold is actually removed.</span></span> 

<span data-ttu-id="14a43-p133">Bevor Sie Elemente in Schritt 5 löschen können, müssen Sie die Verzögerungsdauer aus dem Postfach entfernen. Bestimmen Sie zunächst, ob die Verzögerungs Sperre auf das Postfach angewendet wird, indem Sie den folgenden Befehl in Exchange Online PowerShell ausführen:</span><span class="sxs-lookup"><span data-stu-id="14a43-p133">Before you can delete items in Step 5, you have to remove the delay hold from the mailbox. First, determine if the delay hold is applied to the mailbox by running the following command in Exchange Online PowerShell:</span></span>

```
Get-Mailbox <username> | FL DelayHoldApplied
```

<span data-ttu-id="14a43-p134">Wenn der Wert der *DelayHoldApplied* -Eigenschaft auf **false**festgelegt ist, wurde keine Verzögerungsdauer für das Postfach gespeichert. Sie können zu Schritt 5 wechseln und Elemente im Ordner "Wiederherstellbare Elemente" löschen.</span><span class="sxs-lookup"><span data-stu-id="14a43-p134">If the value of the *DelayHoldApplied* property is set to **False**, a delay hold has not been placed on the mailbox. You can go to Step 5 and delete items in the Recoverable Items folder.</span></span>

<span data-ttu-id="14a43-237">Wenn der Wert der *DelayHoldApplied* -Eigenschaft auf **true**festgelegt ist, führen Sie den folgenden Befehl aus, um die Verzögerungsdauer zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="14a43-237">If the value of the *DelayHoldApplied* property is set to **True**, run the following command to remove the delay hold:</span></span>

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
<span data-ttu-id="14a43-238">Beachten Sie, dass Sie in Exchange Online zur Verwendung des *RemoveDelayHoldApplied* -Parameters die rechtliche Aufbewahrungspflicht zugewiesen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="14a43-238">Note that you must be assigned the Legal Hold role in Exchange Online to use the *RemoveDelayHoldApplied* parameter.</span></span>

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a><span data-ttu-id="14a43-239">Schritt 5: Löschen von Elementen im Ordner "Wiederherstellbare Elemente"</span><span class="sxs-lookup"><span data-stu-id="14a43-239">Step 5: Delete items in the Recoverable Items folder</span></span>

<span data-ttu-id="14a43-p135">Jetzt können Sie Elemente im Ordner "Wiederherstellbare Elemente" tatsächlich löschen, indem Sie das Cmdlet [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) in Exchange Online PowerShell verwenden. Beim Ausführen des Cmdlets **Search-Mailbox** haben Sie drei Optionen.</span><span class="sxs-lookup"><span data-stu-id="14a43-p135">Now you're ready to actually delete items in the Recoverable Items folder by using the [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet in Exchange Online PowerShell. You have three options when running the **Search-Mailbox** cmdlet.</span></span> 
  
- <span data-ttu-id="14a43-242">Kopieren Sie die Elemente vor dem Löschen in ein Zielpostfach, damit Sie die Elemente ggf. überarbeiten können, bevor Sie Sie löschen.</span><span class="sxs-lookup"><span data-stu-id="14a43-242">Copy items to a target mailbox before you delete them so that you can review the items, if necessary, before you delete them.</span></span>
    
- <span data-ttu-id="14a43-243">Kopieren Sie Elemente in ein Zielpostfach, und löschen Sie Sie im gleichen Befehl.</span><span class="sxs-lookup"><span data-stu-id="14a43-243">Copy items to a target mailbox and delete them in the same command.</span></span>
    
- <span data-ttu-id="14a43-244">Elemente löschen, ohne Sie in ein Zielpostfach zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="14a43-244">Delete items without copying them to a target mailbox.</span></span> 
    
<span data-ttu-id="14a43-p136">Beachten Sie, dass Elemente im Ordner "Wiederherstellbare Elemente" im primären Archivpostfach des Benutzers auch gelöscht werden, wenn Sie das Cmdlet " **Search-Mailbox** " ausführen. Um dies zu verhindern, können Sie die *DoNotIncludeArchive* -Option einbeziehen. Und wie bereits erwähnt, wenn die automatische Erweiterung der Archivierung für das Postfach aktiviert ist, löscht das \* \* Search-Mailbox \* \*-Cmdlet keine Elemente in einem zusätzlichen Archivpostfach. Weitere Informationen zum automatisch expandierenden Archiv finden Sie unter [Übersicht über die unbegrenzte Archivierung in Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="14a43-p136">Note that items in the Recoverable Items folder in the user's primary archive mailbox will also be deleted when you run the **Search-Mailbox** cmdlet. To prevent this, you can include the  *DoNotIncludeArchive*  switch. And as previously stated, if auto-expanding archiving is enabled for the mailbox, the \*\* Search-Mailbox \*\* cmdlet doesn't deleted items in an auxiliary archive mailbox. For more information about auto-expanding archive, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="14a43-p137">Wenn Sie eine Suchabfrage (durch Verwendung des Parameters  *SearchQuery*  ) einschließen, gibt das Cmdlet **Search-Mailbox** maximal 10.000 Elemente in den Suchergebnissen zurück. Wenn Sie also eine Suchabfrage einschließen, müssen Sie den Befehl **Search-Mailbox** möglicherweise mehrere Male ausführen, um mehr als 10.000 Elemente zu löschen.</span><span class="sxs-lookup"><span data-stu-id="14a43-p137">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results. Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
  
<span data-ttu-id="14a43-p138">Die folgenden Beispiele zeigen die Befehlssyntax für jede dieser Optionen. In diesen Beispielen wird `-SearchQuery size>0` der Parameterwert verwendet, mit dem alle Elemente aus allen Unterordnern im Ordner "Wiederherstellbare Elemente" gelöscht werden. Wenn Sie nur Elemente löschen müssen, die bestimmten Bedingungen entsprechen, können Sie auch den *SearchQuery* -Parameter verwenden, um andere Bedingungen anzugeben, beispielsweise den Betreff einer Nachricht oder einen Datumsbereich. [Weitere Beispiele zur Verwendung des SearchQuery-Parameters](#other-examples-of-using-the-searchquery-parameter) finden Sie weiter unten.</span><span class="sxs-lookup"><span data-stu-id="14a43-p138">The following examples show the command syntax for each of these options. These examples use the  `-SearchQuery size>0` parameter value, which deletes all items from all subfolders in the Recoverable Items folder. If you need to delete only items that match specific conditions, you can also use the  *SearchQuery*  parameter to specify other conditions, such as the subject of a message or a date range. See the [other examples of using the SearchQuery parameter](#other-examples-of-using-the-searchquery-parameter) below.</span></span> 
  
### <a name="example-1"></a><span data-ttu-id="14a43-255">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14a43-255">Example 1</span></span>

<span data-ttu-id="14a43-p139">In diesem Beispiel werden alle Elemente im Ordner "Wiederherstellbare Elemente" des Benutzers in einen Ordner im Discovery-Such Postfach Ihrer Organisation kopiert. Auf diese Weise können Sie die Elemente überarbeiten, bevor Sie sie endgültig löschen.</span><span class="sxs-lookup"><span data-stu-id="14a43-p139">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox. This lets you review the items before you permanently delete them.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

<span data-ttu-id="14a43-p140">Im vorherigen Beispiel ist es nicht erforderlich, Elemente in das Such Postfach für die Suche zu kopieren. Sie können Nachrichten in ein beliebiges Zielpostfach kopieren. Um den Zugriff auf potenziell vertrauliche Postfachdaten zu verhindern, wird jedoch empfohlen, Nachrichten in ein Postfach zu kopieren, das Zugriff auf autorisiertes Personal hat. Standardmäßig ist der Zugriff auf das standardmäßige Discovery-Such Postfach auf Mitglieder der Rollengruppe "Discoveryverwaltung" in Exchange Online beschränkt.</span><span class="sxs-lookup"><span data-stu-id="14a43-p140">In the previous example, it isn't required to copy items to the Discovery Search Mailbox. You can copy messages to any target mailbox. However, to prevent access to potentially sensitive mailbox data, we recommend copying messages to a mailbox that has access restricted to authorized personnel. By default, access to the default Discovery Search Mailbox is restricted to members of the Discovery Management role group in Exchange Online.</span></span> 
  
### <a name="example-2"></a><span data-ttu-id="14a43-262">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="14a43-262">Example 2</span></span>

<span data-ttu-id="14a43-263">In diesem Beispiel werden alle Elemente im Ordner "Wiederherstellbare Elemente" des Benutzers in einen Ordner im Discovery-Such Postfach Ihrer Organisation kopiert und dann die Elemente aus dem Ordner "Wiederherstellbare Elemente" des Benutzers gelöscht.</span><span class="sxs-lookup"><span data-stu-id="14a43-263">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox and then deletes the items from the user's Recoverable Items folder.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a><span data-ttu-id="14a43-264">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="14a43-264">Example 3</span></span>

<span data-ttu-id="14a43-265">In diesem Beispiel werden alle Elemente im Ordner "Wiederherstellbare Elemente" des Benutzers gelöscht, ohne Sie in ein Zielpostfach zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="14a43-265">This example deletes all items in the user's Recoverable Items folder, without copying them to a target mailbox.</span></span> 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a><span data-ttu-id="14a43-266">Weitere Beispiele für die Verwendung des SearchQuery-Parameters</span><span class="sxs-lookup"><span data-stu-id="14a43-266">Other examples of using the SearchQuery parameter</span></span>

<span data-ttu-id="14a43-p141">Hier einige Beispiele für die Verwendung des *SearchQuery* -Parameters zum Suchen bestimmter Nachrichten. Wenn Sie den Parameter *SearchQuery* verwenden, um nach bestimmten Elementen zu suchen, können Sie die Suchergebnisse in ein Zielpostfach kopieren, um die Suchergebnisse zu überprüfen und dann die Abfrage zu überarbeiten, bevor Sie die Ergebnisse einer Suche löschen.</span><span class="sxs-lookup"><span data-stu-id="14a43-p141">Here are a few examples of using the  *SearchQuery*  parameter to find specific messages. If you use the  *SearchQuery*  parameter to search for specific items, consider copying the search results to a target mailbox so that you can review the search results and then revise the query if necessary before you delete the results of a search.</span></span> 
  
<span data-ttu-id="14a43-269">In diesem Beispiel werden Nachrichten zurückgegeben, die einen bestimmten Ausdruck im Feld Subject enthalten.</span><span class="sxs-lookup"><span data-stu-id="14a43-269">This example returns messages that contain a specific phrase in the Subject field.</span></span>
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

<span data-ttu-id="14a43-270">In diesem Beispiel werden Nachrichten zurückgegeben, die innerhalb des angegebenen Datumsbereich gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="14a43-270">This example returns messages that were sent within the specified date range.</span></span>
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
<span data-ttu-id="14a43-271">In diesem Beispiel werden Nachrichten zurückgegeben, die an die angegebene Person gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="14a43-271">This example returns messages that were sent to the specified person.</span></span>

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a><span data-ttu-id="14a43-272">Überprüfen, ob Elemente gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="14a43-272">Verify that items were deleted</span></span>

<span data-ttu-id="14a43-p142">Um zu überprüfen, ob Sie Elemente erfolgreich aus dem Ordner "Wiederherstellbare Elemente" eines Postfachs gelöscht haben, verwenden Sie das Cmdlet **Get-MailboxFolderStatistics** in Exchange Online PowerShell, um die Größe und Anzahl der Elemente im Ordner "Wiederherstellbare Elemente" zu überprüfen. Sie können diese Statistiken mit den in Schritt 1 gesammelten vergleichen.</span><span class="sxs-lookup"><span data-stu-id="14a43-p142">To verify that you've successfully deleted items from the Recoverable Items folder of a mailbox, use **Get-MailboxFolderStatistics** cmdlet in Exchange Online PowerShell to check the size and number of items in Recoverable Items folder. You can compare these statistics with the ones you collected in Step 1.</span></span> 
  
<span data-ttu-id="14a43-275">Führen Sie den folgenden Befehl in aus, um die aktuelle Größe und Gesamtanzahl von Elementen in Ordnern und Unterordnern im Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14a43-275">Run the following command in to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
<span data-ttu-id="14a43-276">Führen Sie den folgenden Befehl aus, um die Größe und die Gesamtanzahl von Elementen in Ordnern und Unterordnern im Ordner "Wiederherstellbare Elemente" im Archivpostfach des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14a43-276">Run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in the user's archive mailbox.</span></span> 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a><span data-ttu-id="14a43-277">Schritt 6: Zurücksetzen des Postfachs in den vorherigen Zustand</span><span class="sxs-lookup"><span data-stu-id="14a43-277">Step 6: Revert the mailbox to its previous state</span></span>

<span data-ttu-id="14a43-p143">Der letzte Schritt besteht darin, das Postfach wieder auf die vorherige Konfiguration zurückzusetzen. Dies ist das Zurücksetzen der Eigenschaften, die Sie in Schritt 2 geändert haben, und erneutes Anwenden der haltebereiche, die Sie in Schritt 3 entfernt haben. Hierzu gehören:</span><span class="sxs-lookup"><span data-stu-id="14a43-p143">The final step is to revert the mailbox back to its previous configuration. This means resetting the properties that you changed in Step 2 and re-applying the holds that you removed in Step 3. This includes:</span></span>
  
- <span data-ttu-id="14a43-p144">Ändern des Aufbewahrungszeitraums für gelöschte Elemente wieder auf den vorherigen Wert. Alternativ können Sie diese Einstellung nur auf 30 Tage festlegen, den Maximalwert in Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="14a43-p144">Changing the deleted item retention period back to its previous value. Alternatively, you can just leave this set to 30 days, the maximum value in Exchange Online.</span></span>
    
- <span data-ttu-id="14a43-283">Wieder aktivieren der Wiederherstellung einzelner Elemente.</span><span class="sxs-lookup"><span data-stu-id="14a43-283">Re-enabling single Item recovery.</span></span>
    
- <span data-ttu-id="14a43-284">Erneutes Aktivieren der Clientzugriffsmethoden, damit der Besitzer auf sein Postfach zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="14a43-284">Re-enabling the client access methods so that the owner can access their mailbox.</span></span>
    
- <span data-ttu-id="14a43-285">Erneutes Anwenden der Speicher-und Office 365-Aufbewahrungsrichtlinien, die Sie entfernt haben.</span><span class="sxs-lookup"><span data-stu-id="14a43-285">Re-applying the holds and Office 365 retention policies that you removed.</span></span>
    
- <span data-ttu-id="14a43-286">Erneutes Aktivieren des Assistenten für verwaltete Ordner zur Verarbeitung des Postfachs.</span><span class="sxs-lookup"><span data-stu-id="14a43-286">Re-enabling the Managed Folder Assistant to process the mailbox.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="14a43-287">Es wird empfohlen, dass Sie 24 Stunden nach der erneuten Anwendung einer Aufbewahrungs-oder Office 365-Speicherrichtlinie warten, bevor Sie den Assistenten für verwaltete Ordner erneut aktivieren, um das Postfach zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="14a43-287">We recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant to process the mailbox.</span></span> 
  
<span data-ttu-id="14a43-288">Führen Sie die folgenden Schritte (in der angegebenen Reihenfolge) in Exchange Online PowerShell aus.</span><span class="sxs-lookup"><span data-stu-id="14a43-288">Perform the following steps (in the specified sequence) in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="14a43-p145">Führen Sie den folgenden Befehl aus, um den Aufbewahrungszeitraum für gelöschte Elemente wieder auf den ursprünglichen Wert zu ändern. Dabei wird davon ausgegangen, dass die vorherige Einstellung weniger als 30 Tage beträgt; Beispiel: 14 Tage.</span><span class="sxs-lookup"><span data-stu-id="14a43-p145">Run the following command to change the deleted item retention period back to its original value. This assumes that the previous setting is less than 30 days; for example 14 days.</span></span> 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. <span data-ttu-id="14a43-291">Führen Sie den folgenden Befehl aus, um die Wiederherstellung einzelner Elemente wieder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="14a43-291">Run the following command to re-enable single item recovery.</span></span>
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. <span data-ttu-id="14a43-292">Führen Sie den folgenden Befehl aus, um alle Clientzugriffsmethoden für das Postfach erneut zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="14a43-292">Run the following command to re-enable all client access methods to the mailbox.</span></span>
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. <span data-ttu-id="14a43-p146">Wenden Sie die in Schritt 3 entfernten haltebereiche erneut an. Verwenden Sie je nach Aufbewahrungs eines der folgenden Verfahren.</span><span class="sxs-lookup"><span data-stu-id="14a43-p146">Re-apply the holds that you removed in Step 3. Depending on the type of hold, use one of the following procedures.</span></span>
    
    <span data-ttu-id="14a43-295">**Beweissicherungsverfahren**</span><span class="sxs-lookup"><span data-stu-id="14a43-295">**Litigation Hold**</span></span>
    
    <span data-ttu-id="14a43-296">Führen Sie den folgenden Befehl aus, um die Beweissicherung für das Postfach erneut zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="14a43-296">Run the following command to re-enable a Litigation Hold for the mailbox.</span></span>
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    <span data-ttu-id="14a43-297">**In-Place Hold**</span><span class="sxs-lookup"><span data-stu-id="14a43-297">**In-Place Hold**</span></span>
    
    <span data-ttu-id="14a43-298">Verwenden Sie die EAC (oder Exchange Online PowerShell), um das Postfach wieder dem in-situ-Speicher hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="14a43-298">Use the EAC (or Exchange Online PowerShell) to add the mailbox back to the In-Place Hold.</span></span> 
    
    <span data-ttu-id="14a43-299">**Office 365-Aufbewahrungsrichtlinien, die auf bestimmte Postfächer angewendet werden**</span><span class="sxs-lookup"><span data-stu-id="14a43-299">**Office 365 retention policies applied to specific mailboxes**</span></span>
    
    <span data-ttu-id="14a43-p147">Verwenden Sie das &amp; Security Compliance Center, um das Postfach der Office 365-Aufbewahrungsrichtlinie wieder hinzuzufügen. Wechseln Sie zur Seite Aufbewahrungs **Zeit der Datenverwaltung** \> \*\*\*\* im Security &amp; Compliance Center, bearbeiten Sie die Aufbewahrungsrichtlinie, und fügen Sie das Postfach zurück zur Liste der Empfänger, auf die die Aufbewahrungsrichtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="14a43-p147">Use the Security &amp; Compliance Center to add the mailbox back to the Office 365 retention policy. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy, and add the mailbox back to the list of recipients that the retention policy is applied to.</span></span> 
    
    <span data-ttu-id="14a43-302">**Organisationsweite Office 365-Aufbewahrungsrichtlinien**</span><span class="sxs-lookup"><span data-stu-id="14a43-302">**Organization-wide Office 365 retention policies**</span></span>
    
    <span data-ttu-id="14a43-p148">Wenn Sie eine organisationsweite oder Exchange-weite Aufbewahrungsrichtlinie entfernt haben, indem Sie Sie aus der Richtlinie ausschließen, &amp; verwenden Sie das Security Compliance Center, um das Postfach aus der Liste der ausgeschlossenen Benutzer zu entfernen. Wechseln Sie im &amp; Security Compliance Center zur Seite Aufbewahrungszeit der **Datenverwaltung** \> \*\*\*\* , bearbeiten Sie die organisationsweite Aufbewahrungsrichtlinie, und entfernen Sie das Postfach aus der Liste der ausgeschlossenen Empfänger. Auf diese Weise wird die Aufbewahrungsrichtlinie erneut auf das Postfach des Benutzers angewendet.</span><span class="sxs-lookup"><span data-stu-id="14a43-p148">If you removed an organization-wide or Exchange-wide retention policy by excluding it from the policy, then use the Security &amp; Compliance Center to remove the mailbox from the list of excluded users. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the organization-wide retention policy, and remove the mailbox from the list of excluded recipients. Doing this will re-apply the retention policy to the user's mailbox.</span></span> 
    
    <span data-ttu-id="14a43-306">**eDiscovery-Fall enthält**</span><span class="sxs-lookup"><span data-stu-id="14a43-306">**eDiscovery case holds**</span></span>
    
    <span data-ttu-id="14a43-p149">Verwenden Sie das &amp; Security Compliance Center, um das Postfach mit einem eDiscovery-Fall zu versehen. Wechseln Sie im &amp; Security Compliance Center zur **eDiscovery** -Seite für die \*\* &amp; Such Untersuchung\*\* \> , öffnen Sie den Fall, und fügen Sie das Postfach wieder in den Haltebereich ein.</span><span class="sxs-lookup"><span data-stu-id="14a43-p149">Use the Security &amp; Compliance Center to add the mailbox back the hold that's associated with an eDiscovery case. Go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and add the mailbox back to the hold.</span></span> 
    
5. <span data-ttu-id="14a43-p150">Führen Sie den folgenden Befehl aus, damit der Assistent für verwaltete Ordner das Postfach erneut verarbeiten kann. Wie bereits erwähnt, empfiehlt es sich, dass Sie 24 Stunden nach der erneuten Anwendung eines haltebereichs oder einer Office 365-Aufbewahrungsrichtlinie warten, bevor Sie den Assistenten für verwaltete Ordner erneut aktivieren.</span><span class="sxs-lookup"><span data-stu-id="14a43-p150">Run the following command to allow the Managed Folder Assistant to process the mailbox again. As previously stated, we recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. <span data-ttu-id="14a43-311">Um zu überprüfen, ob das Postfach wieder auf die vorherige Konfiguration zurückgesetzt wurde, können Sie die folgenden Befehle ausführen und die Einstellungen dann mit denjenigen vergleichen, die Sie in Schritt 1 gesammelt haben.</span><span class="sxs-lookup"><span data-stu-id="14a43-311">To verify that the mailbox has been reverted back to its previous configuration, you can run the following commands and then compare the settings to the ones that you collected in Step 1.</span></span>

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a><span data-ttu-id="14a43-312">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="14a43-312">More information</span></span>

<span data-ttu-id="14a43-p151">Im folgenden finden Sie eine Tabelle, in der beschrieben wird, wie unterschiedliche Aufbewahrungs Typen basierend auf den Werten in der *InPlaceHolds* -Eigenschaft identifiziert werden, wenn Sie die Cmdlets **Get-Mailbox** oder **Get-OrganizationConfig** ausführen. Ausführlichere Informationen finden Sie unter [Vorgehensweise beim Identifizieren des Aufbewahrungs Typs für ein Exchange Online-Postfach](identify-a-hold-on-an-exchange-online-mailbox.md).</span><span class="sxs-lookup"><span data-stu-id="14a43-p151">Here's a table that describes how to identify different types of holds based on the values in the  *InPlaceHolds*  property when you run the **Get-Mailbox** or **Get-OrganizationConfig** cmdlets. For more detailed information, see [How to identify the type of hold placed on an Exchange Online mailbox](identify-a-hold-on-an-exchange-online-mailbox.md).</span></span>

<span data-ttu-id="14a43-315">Wie bereits erläutert, müssen Sie alle Haltestatus-und Office 365-Aufbewahrungsrichtlinien aus einem Postfach entfernen, bevor Sie Elemente im Ordner "Wiederherstellbare Elemente" erfolgreich löschen können.</span><span class="sxs-lookup"><span data-stu-id="14a43-315">As previously explained, you have to remove all holds and Office 365 retention policies from a mailbox before you can successfully delete items in the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="14a43-316">**Haltebereichstyp**</span><span class="sxs-lookup"><span data-stu-id="14a43-316">**Hold type**</span></span>|<span data-ttu-id="14a43-317">**Beispielwert**</span><span class="sxs-lookup"><span data-stu-id="14a43-317">**Example value**</span></span>|<span data-ttu-id="14a43-318">**So identifizieren Sie den Haltestatus**</span><span class="sxs-lookup"><span data-stu-id="14a43-318">**How to identify the hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="14a43-319">Beweissicherungsverfahren</span><span class="sxs-lookup"><span data-stu-id="14a43-319">Litigation Hold</span></span>  <br/> | `True` <br/> |<span data-ttu-id="14a43-320">Die  *LitigationHoldEnabled*  -Eigenschaft wird festgelegt auf  `True`.</span><span class="sxs-lookup"><span data-stu-id="14a43-320">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="14a43-321">Compliance-Archiv</span><span class="sxs-lookup"><span data-stu-id="14a43-321">In-Place Hold</span></span>  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |<span data-ttu-id="14a43-p152">Die *InPlaceHolds* -Eigenschaft enthält die GUID des in-situ-Speichers, der für das Postfach platziert wird. Sie können feststellen, dass dies ein in-situ-Speicher ist, da die GUID nicht mit einem Präfix beginnt.</span><span class="sxs-lookup"><span data-stu-id="14a43-p152">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the mailbox. You can tell this is an In-Place Hold because the GUID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="14a43-324">Sie können den `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` Befehl in Exchange Online PowerShell verwenden, um Informationen zum in-situ-Speicher für das Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="14a43-324">You can use the  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` command in Exchange Online PowerShell to get information about the In-Place Hold on the mailbox.</span></span>  <br/> |
| <span data-ttu-id="14a43-325">Office 365-Aufbewahrungsrichtlinien im &amp; Security Compliance Center, die auf bestimmte Postfächer angewendet werden</span><span class="sxs-lookup"><span data-stu-id="14a43-325">Office 365 retention policies in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> <span data-ttu-id="14a43-326">oder</span><span class="sxs-lookup"><span data-stu-id="14a43-326">or</span></span>  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |<span data-ttu-id="14a43-p153">Wenn Sie das Cmdlet **Get-Mailbox** ausführen, enthält die *InPlaceHolds* -Eigenschaft auch guids von Office 365-Aufbewahrungsrichtlinien, die auf das Postfach angewendet werden. Sie können Aufbewahrungsrichtlinien identifizieren, da die GUID mit `mbx` dem Präfix beginnt. Wenn die GUID der Aufbewahrungsrichtlinie mit dem `skp` Präfix beginnt, bedeutet dies, dass die Aufbewahrungsrichtlinie auf Skype for Business-Unterhaltungen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="14a43-p153">When you run the **Get-Mailbox** cmdlet, the  *InPlaceHolds*  property also contains GUIDs of Office 365 retention policies applied to the mailbox. You can identify retention policies because the GUID starts with the  `mbx` prefix. Note that if the GUID of the retention policy starts with the  `skp` prefix, that indicates that the retention policy is applied to Skype for Business conversations.  </span></span><br/> <span data-ttu-id="14a43-330">Führen Sie den folgenden Befehl in Security &amp; Compliance Center PowerShell aus, um die Office 365-Aufbewahrungsrichtlinie zu identifizieren, die auf das Postfach angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="14a43-330">To identity the Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/> <br/>`Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="14a43-331">Entfernen Sie unbedingt das `mbx` Präfix oder `skp` , wenn Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="14a43-331">Be sure to remove the  `mbx` or  `skp` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="14a43-332">Organisationsweite Office 365-Aufbewahrungsrichtlinien im Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="14a43-332">Organization-wide Office 365 retention policies in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="14a43-333">Kein Wert</span><span class="sxs-lookup"><span data-stu-id="14a43-333">No value</span></span>  <br/> <span data-ttu-id="14a43-334">oder</span><span class="sxs-lookup"><span data-stu-id="14a43-334">or</span></span>  <br/>  <span data-ttu-id="14a43-335">`-mbxe9b52bf7ab3b46a286308ecb29624696`(gibt an, dass das Postfach von einer organisationsweiten Richtlinie ausgeschlossen ist)</span><span class="sxs-lookup"><span data-stu-id="14a43-335">`-mbxe9b52bf7ab3b46a286308ecb29624696` (indicates that the mailbox is excluded from an organization-wide policy)</span></span>  <br/> |<span data-ttu-id="14a43-336">Auch wenn die *InPlaceHolds* -Eigenschaft beim Ausführen des Cmdlets **Get-Mailbox** leer ist, gibt es möglicherweise noch eine oder mehrere organisationsweite Office 365-Aufbewahrungsrichtlinien, die auf das Postfach angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="14a43-336">Even if the  *InPlaceHolds*  property is empty when you run the **Get-Mailbox** cmdlet, there still might be one or more organization-wide Office 365 retention policies applied to the mailbox.</span></span>  <br/> <span data-ttu-id="14a43-p154">Um dies zu überprüfen, können Sie `Get-OrganizationConfig | FL InPlaceHolds` den Befehl in Exchange Online PowerShell ausführen, um eine Liste der GUIDs für organisationsweite Office 365-Aufbewahrungsrichtlinien abzurufen. Die GUID für organisationsweite Aufbewahrungsrichtlinien, die auf Exchange-Postfächer `mbx` angewendet werden, beginnen mit dem Präfix; Beispiel `mbxa3056bb15562480fadb46ce523ff7b02`.</span><span class="sxs-lookup"><span data-stu-id="14a43-p154">To verify this, you can run the  `Get-OrganizationConfig | FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  </span></span><br/> <span data-ttu-id="14a43-339">Führen Sie den folgenden Befehl in Security &amp; Compliance Center PowerShell aus, um die organisationsweite Office 365-Aufbewahrungsrichtlinie zu identifizieren, die auf das Postfach angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="14a43-339">To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/><span data-ttu-id="14a43-340">Beachten Sie, dass, wenn ein Postfach von einer organisationsweiten Office 365-Aufbewahrungsrichtlinie ausgeschlossen wird, die GUID für die Aufbewahrungsrichtlinie in der *InPlaceHolds* -Eigenschaft des Postfachs des Benutzers angezeigt wird, wenn Sie das Cmdlet **Get-Mailbox** ausführen. Es wird durch das Präfix `-mbx`identifiziert; Zum Beispiel`-mbxe9b52bf7ab3b46a286308ecb29624696`</span><span class="sxs-lookup"><span data-stu-id="14a43-340">Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696`</span></span> <br/> |
|<span data-ttu-id="14a43-341">eDiscovery-Fall in der Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="14a43-341">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |<span data-ttu-id="14a43-p155">Die *InPlaceHolds* -Eigenschaft enthält auch die GUID aller Haltestatus, der einem eDiscovery-Fall im &amp; Security Compliance Center zugeordnet ist, der möglicherweise im Postfach gespeichert wird. Sie können feststellen, dass dies eine eDiscovery-Groß-/Kleinschreibung ist, `UniH` da die GUID mit dem Präfix beginnt.</span><span class="sxs-lookup"><span data-stu-id="14a43-p155">The  *InPlaceHolds*  property also contains the GUID of any hold associated with an eDiscovery case in the Security &amp; Compliance Center that might be placed on the mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="14a43-p156">Sie können das `Get-CaseHoldPolicy` Cmdlet im Security &amp; Compliance Center PowerShell verwenden, um Informationen über den eDiscovery-Fall abzurufen, dem das Postfach zugeordnet ist. Beispielsweise können Sie den Befehl `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` ausführen, um den Namen der Groß-/Kleinschreibung im Postfach anzuzeigen. Achten Sie darauf, das `UniH` Präfix zu entfernen, wenn Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="14a43-p156">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the mailbox is associated with. For example, you can run the command  `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  </span></span><br/><br/> <span data-ttu-id="14a43-347">Führen Sie die folgenden Befehle aus, um den eDiscovery-Fall zu identifizieren, dem das Postfach zugeordnet ist:</span><span class="sxs-lookup"><span data-stu-id="14a43-347">To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:</span></span><br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name`


