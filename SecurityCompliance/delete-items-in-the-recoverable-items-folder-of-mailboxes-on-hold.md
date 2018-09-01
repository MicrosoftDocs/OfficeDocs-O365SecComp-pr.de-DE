---
title: Löschen von Elementen im Ordner "wiederherstellbare Elemente" des cloudbasierten Postfächer in der Warteschleife - Admin-Hilfe
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/21/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Für Administratoren: Löschen von Elementen in den Ordner eines Benutzers wiederherstellbare Elemente für ein Exchange Online-Postfach, auch wenn dieses Postfach rechtliche Aufbewahrungspflicht platziert wird. Dies ist eine effektive Möglichkeit zum Löschen von Daten, die in Office 365 versehentlich verschüttet ist.'
ms.openlocfilehash: c984bcaa35a9bc7bc30e11d68ba8f7f0ce75b64d
ms.sourcegitcommit: 31e0d94244c76a9f5118efee8bbc93395d080f91
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2018
ms.locfileid: "23796881"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a><span data-ttu-id="27adc-104">Löschen von Elementen im Ordner "wiederherstellbare Elemente" des cloudbasierten Postfächer in der Warteschleife - Admin-Hilfe</span><span class="sxs-lookup"><span data-stu-id="27adc-104">Delete items in the Recoverable Items folder of cloud-based mailboxes on hold - Admin Help</span></span>

<span data-ttu-id="27adc-p102">"Wiederherstellbare Elemente" für ein Exchange Online-Postfach zum Schutz vor versehentlichen oder böswilligen Löschvorgängen vorhanden ist. Es wird auch verwendet zum Speichern von Elementen, die werden beibehalten und Office 365-Compliance-Features wie Haltestatus und eDiscovery-Suchvorgänge zugreifen. Jedoch möglicherweise Organisationen in manchen Fällen Daten haben, die versehentlich im Ordner "wiederherstellbare Elemente" beibehalten worden ist, die sie löschen müssen. Ein Benutzer kann beispielsweise unwissentlich senden oder Weiterleiten eine e-Mail-Nachricht, die enthält vertrauliche Informationen oder Informationen, die schwerwiegende Business Konsequenzen haben kann. Auch wenn die Nachricht dauerhaft gelöscht wird, kann es auf unbestimmte Zeit aufbewahrt werden, da eine rechtliche Aufbewahrungspflicht für das Postfach versetzt wurde. In diesem Szenario wird als Daten stellen bezeichnet, da Daten in Office 365 versehentlich verschüttet hat. In diesen Fällen können Sie Elemente in den Ordner eines Benutzers wiederherstellbare Elemente für ein Exchange Online-Postfach löschen, auch wenn dieses Postfach mit einer der anderen Warteschleife Features in Office 365 gehalten wird. Diese Arten von Haltestatus umfassen Rechtsstreitigkeiten enthält, Compliance-Archive, eDiscovery-Archive und Office 365-Aufbewahrungsrichtlinien erstellt in der Office 365-Sicherheit &amp; Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="27adc-p102">The Recoverable Items folder for an Exchange Online mailbox exists to protect from accidental or malicious deletions. It's also used to store items that are retained and accessed by Office 365 compliance features, such as holds and eDiscovery searches. However, in some situations organizations might have data that's been unintentionally retained in the Recoverable Items folder that they must delete. For example, a user might unknowingly send or forward an email message that contains sensitive information or information that may have serious business consequences. Even if the message is permanently deleted, it might be retained indefinitely because a legal hold has been placed on the mailbox. This scenario is known as data spillage because data has been unintentionally spilled into Office 365. In these situations, you can delete items in a user's Recoverable Items folder for an Exchange Online mailbox, even if that mailbox is placed on hold with one of the different hold features in Office 365. These types of holds include Litigation Holds, In-Place Holds, eDiscovery holds, and Office 365 retention policies created in the Office 365 Security &amp; Compliance Center.</span></span> 
  
 <span data-ttu-id="27adc-p103">In diesem Artikel wird erläutert, wie Elemente aus dem Ordner wiederherstellbare Elemente für cloudbasierte Postfächer zu löschen, die in der Warteschleife sind. Bei diesem Verfahren werden deaktiviert den Zugriff auf das Postfach und Deaktivieren der Wiederherstellung einzelner Elemente, deaktivieren den Assistenten für verwaltete Ordner aus der Verarbeitung des Postfachs, vorübergehend den Haltestatus entfernen, Löschen von Elementen aus dem Ordner "wiederherstellbare Elemente" und anschließend wiederherstellen das Postfach auf die vorherige Konfiguration. Hier wird der Prozess:</span><span class="sxs-lookup"><span data-stu-id="27adc-p103">This article explains how to delete items from the Recoverable Items folder for cloud-based mailboxes that are on hold. This procedure involves disabling access to the mailbox and disabling single item recovery, disabling the Managed Folder Assistant from processing the mailbox, temporarily removing the hold, deleting items from the Recoverable Items folder, and then reverting the mailbox to its previous configuration. Here's the process:</span></span> 
  
[<span data-ttu-id="27adc-116">Schritt 1: Sammeln von Informationen über das Postfach</span><span class="sxs-lookup"><span data-stu-id="27adc-116">Step 1: Collect information about the mailbox</span></span>](#step-1-collect-information-about-the-mailbox)

[<span data-ttu-id="27adc-117">Schritt 2: Vorbereiten des Postfachs</span><span class="sxs-lookup"><span data-stu-id="27adc-117">Step 2: Prepare the mailbox</span></span>](#step-2-prepare-the-mailbox)

[<span data-ttu-id="27adc-118">Schritt 3: Entfernen Sie alle Haltestatus aus dem Postfach</span><span class="sxs-lookup"><span data-stu-id="27adc-118">Step 3: Remove all holds from the mailbox</span></span>](#step-3-remove-all-holds-from-the-mailbox)

[<span data-ttu-id="27adc-119">Schritt 4: Löschen von Elementen im Ordner "wiederherstellbare Elemente"</span><span class="sxs-lookup"><span data-stu-id="27adc-119">Step 4: Delete items in the Recoverable Items folder</span></span>](#step-4-delete-items-in-the-recoverable-items-folder)

[<span data-ttu-id="27adc-120">Schritt 5: Das Postfach in den vorherigen Zustand zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="27adc-120">Step 5: Revert the mailbox to its previous state</span></span>](#step-5-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> <span data-ttu-id="27adc-p104">Die Verfahren in diesem Artikel beschriebenen führt Daten dauerhaft gelöscht (gelöscht) von einem Exchange Online-Postfach. Das bedeutet, dass Nachrichten, die Sie aus dem Ordner wiederherstellbare Elemente löschen können nicht wiederhergestellt werden nicht für die Offenlegungspflicht oder sonstige Zwecke Compliance verfügbar. Wenn Sie möchten, um Nachrichten aus einem Postfach zu löschen, die als Teil einer Aufbewahrung für eventuelle Rechtsstreitigkeiten, Compliance-Archiv, in die Warteschleife gestellt wird eDiscovery halten oder Office 365 Aufbewahrungsrichtlinie erstellt, in die Office 365-Sicherheit &amp; Compliance Center, erkundigen Sie sich bei der Verwaltung von Datensätzen und Legal Abteilungen, bevor Sie den Haltestatus entfernen. Ihre Organisation möglicherweise eine Richtlinie, die definiert, ob ein Postfach auf halten oder ein Daten stellen Vorfall Vorrang.</span><span class="sxs-lookup"><span data-stu-id="27adc-p104">The procedures outlined in this article will result in data being permanently deleted (purged) from an Exchange Online mailbox. That means messages that you delete from the Recoverable Items folder can't be recovered and won't be available for legal discovery or other compliance purposes. If you want to delete messages from a mailbox that's placed on hold as part of a Litigation Hold, In-Place Hold, eDiscovery hold, or Office 365 retention policy created in the Office 365 Security &amp; Compliance Center, check with your records management or legal departments before removing the hold. Your organization might have a policy that defines whether a mailbox on hold or a data spillage incident takes priority.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="27adc-125">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="27adc-125">Before you begin</span></span>

- <span data-ttu-id="27adc-126">Sie müssen beide der folgenden Verwaltungsrollen in Exchange Online suchen und Löschen von Nachrichten aus dem Ordner "wiederherstellbare Elemente" in Schritt 4 zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="27adc-126">You have to be assigned both of the following management roles in Exchange Online to search for and delete messages from the Recoverable Items folder in Step 4.</span></span>
    
  - <span data-ttu-id="27adc-p105">**Postfachsuche** – diese Rolle können Sie Postfächer in Ihrer Organisation zu suchen. Exchange-Administratoren sind nicht dieser Rolle standardmäßig zugewiesen. Wenn sich diese Rolle zuweisen möchten, tragen Sie sich als Mitglied der Rollengruppe "Discoveryverwaltung" im Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="27adc-p105">**Mailbox Search** - This role lets you to search mailboxes in your organization. Exchange administrators aren't assigned this role by default. To assign yourself this role, add yourself as a member of the Discovery Management role group in Exchange Online.</span></span> 
    
  - <span data-ttu-id="27adc-p106">**Postfach Import/Export** - dieser Rolle können Sie Nachrichten aus dem Postfach eines Benutzers zu löschen. Standardmäßig ist nicht dieser Rolle alle Rollengruppe zugewiesen. Um Nachrichten aus den Postfächern der Benutzer zu löschen, können Sie die Rolle Postfach Import/Export der Rollengruppe "Organisationsverwaltung" im Exchange Online hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="27adc-p106">**Mailbox Import Export** - This role lets you to delete messages from a user's mailbox. By default, this role isn't assigned to any role group. To delete messages from users' mailboxes, you can add the Mailbox Import Export role to the Organization Management role group in Exchange Online.</span></span> 
    
- <span data-ttu-id="27adc-p107">In diesem Artikel beschriebene Verfahren wird für inaktive Postfächer nicht unterstützt. Das, da Sie eine Warteschleife (oder Office 365 Aufbewahrungsrichtlinie) erneut anwenden können nicht zu eines inaktiven Postfachs ist, nachdem Sie ihn entfernen. Wenn Sie eines inaktiven Postfachs einen Haltestatus aufheben, wird in einem normalen vorläufig gelöschten Postfach geändert und werden unwiederbringlich aus Ihrer Organisation gelöscht werden, nachdem er vom Assistenten für verwaltete Ordner verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="27adc-p107">The procedure described in this article isn't supported for inactive mailboxes. That's because you can't re-apply a hold (or Office 365 retention policy) to an inactive mailbox after you remove it. When you remove a hold from an inactive mailbox, it's changed to a normal soft-deleted mailbox and will be permanently deleted from your organization after it's processed by the Managed Folder Assistant.</span></span>
    
- <span data-ttu-id="27adc-p108">Dieses Verfahren für ein Postfach nicht möglich, die ein Office 365-Aufbewahrungsrichtlinie zugewiesen wurde, die mit einer Sperre permanentes gesperrt ist. Dies liegt daran eine Beibehaltung der Sperre verhindert, dass Sie zu entfernen oder ohne das Postfach aus der Office 365-Aufbewahrungsrichtlinie und den Assistenten für verwaltete Ordner für das Postfach zu deaktivieren. Weitere Informationen zu Aufbewahrungsrichtlinien Sperren finden Sie unter [Sperren einer Aufbewahrungsrichtlinie](retention-policies.md#locking-a-retention-policy).</span><span class="sxs-lookup"><span data-stu-id="27adc-p108">You can't perform this procedure for a mailbox that has been assigned to an Office 365 retention policy that's been locked with a Preservation Lock. That's because a Preservation Lock prevents you from removing or excluding the mailbox from the Office 365 retention policy and from disabling the Managed Folder Assistant on the mailbox. For more information about locking retention policies, see [Locking a retention policy](retention-policies.md#locking-a-retention-policy).</span></span>
    
- <span data-ttu-id="27adc-p109">Wenn ein Postfach wird nicht in die Warteschleife gestellt (oder verfügt nicht über Wiederherstellung einzelner Elemente aktiviert), können Sie einfach die Elemente aus dem Ordner wiederherstellbare Elemente löschen. Weitere Informationen hierzu finden Sie unter [Suchen und Löschen von Nachrichten ](https://go.microsoft.com/fwlink/?linkid=852453).</span><span class="sxs-lookup"><span data-stu-id="27adc-p109">If a mailbox isn't placed on hold (or doesn't have single item recovery enabled), you can simply delete the items from the Recoverable Items folder. For more information about how to do this, see [Search for and delete messages ](https://go.microsoft.com/fwlink/?linkid=852453).</span></span>
  
## <a name="step-1-collect-information-about-the-mailbox"></a><span data-ttu-id="27adc-141">Schritt 1: Sammeln von Informationen über das Postfach</span><span class="sxs-lookup"><span data-stu-id="27adc-141">Step 1: Collect information about the mailbox</span></span>

<span data-ttu-id="27adc-p110">Dieser erste Schritt besteht darin ausgewählte Eigenschaften aus dem Zielpostfach sammeln, die für dieses Verfahren gelten. Achten Sie darauf, notieren Sie sich diese Einstellungen oder da Sie einige dieser Eigenschaften ändern, und klicken Sie dann auf die ursprünglichen Werte in Schritt 5 zurückgesetzt, nach dem Löschen von Elementen aus dem Ordner wiederherstellbare Elemente in einer Textdatei speichern. Es folgt eine Liste mit den Postfacheigenschaften benötigten sammeln.</span><span class="sxs-lookup"><span data-stu-id="27adc-p110">This first step is to collect selected properties from the target mailbox that will affect this procedure. Be sure to write down these settings or save them to a text file because you'll change some of these properties and then revert back to the original values in Step 5, after you delete items from the Recoverable Items folder. Here's a list of the mailbox properties you need to collect.</span></span>
  
-  <span data-ttu-id="27adc-145">*SingleItemRecoveryEnabled* und *RetainDeletedItemsFor* ; Falls erforderlich, Sie einzelne Wiederherstellung deaktivieren und erhöhen die Aufbewahrungszeit von gelöschten Elemente in Schritt 3.</span><span class="sxs-lookup"><span data-stu-id="27adc-145">*SingleItemRecoveryEnabled*  and  *RetainDeletedItemsFor*  ; if necessary, you'll disable single recovery and increase the deleted items retention period in Step 3.</span></span> 
    
-  <span data-ttu-id="27adc-p111">*LitigationHoldEnabled* und *InPlaceHolds* ; Sie müssen alle Haltestatus, die für das Postfach platziert werden, sodass Sie sie in Schritt 3 vorübergehend entfernen können. Finden Sie [Weitere Informationen](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) im Abschnitt Tipps dazu, wie Sie den Typ Haltestatus zu identifizieren, der für ein Postfach platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="27adc-p111">*LitigationHoldEnabled*  and  *InPlaceHolds*  ; you need to identify all the holds placed on the mailbox so that you can temporarily remove them in Step 3. See the [More information](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> 
    
<span data-ttu-id="27adc-p112">Darüber hinaus müssen Sie das Postfach Clientzugriffseinstellungen abrufen, damit Sie vorübergehend deaktivieren, damit der Besitzer (oder andere Benutzer) während dieses Vorgangs Zugriff auf das Postfach ist nicht möglich. Schließlich können Sie die aktuelle Größe und Anzahl der Elemente im Ordner "wiederherstellbare Elemente" abrufen. Nachdem Sie Elemente im Ordner "wiederherstellbare Elemente" in Schritt 4 zu löschen, verwenden Sie diese Informationen, um sicherzustellen, dass Elemente tatsächlich entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="27adc-p112">Additionally, you need to get the mailbox client access settings so you can temporarily disable them so the owner (or other users) can't access the mailbox during this procedure. Finally, you can get the current size and number of items in the Recoverable Items folder. After you delete items in the Recoverable Items folder in Step 4, you'll use this information to verify that items were actually removed.</span></span>
  
1. <span data-ttu-id="27adc-p113">[Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Achten Sie darauf, dass Sie einen Benutzernamen und ein Kennwort für ein Administratorkonto verwenden, das die entsprechenden Verwaltungsrollen in Exchange Online zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="27adc-p113">[Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Be sure to use a user name and password for an administrator account that's been assigned the appropriate management roles in Exchange Online.</span></span> 
    
2. <span data-ttu-id="27adc-153">Führen Sie den folgenden Befehl zum Abrufen von Informationen zur Wiederherstellung einzelner Elemente und die Aufbewahrungszeit für gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="27adc-153">Run the following command to get information about single item recovery and the deleted item retention period.</span></span>

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   <span data-ttu-id="27adc-p114">Wenn die Wiederherstellung einzelner Elemente aktiviert ist, müssen Sie in Schritt2 zu deaktivieren. Wenn die Aufbewahrungszeit für gelöschte 30 Tage lang nicht festgelegt (der maximale Wert in Exchange Online), und klicken Sie dann in Schritt2 zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="27adc-p114">If single item recovery is enabled, you'll have to disable it in Step 2. If the deleted item retention period isn't set for 30 days (the maximum value in Exchange Online), then you can increase it in Step 2.</span></span> 
    
3. <span data-ttu-id="27adc-156">Führen Sie den folgenden Befehl aus, um das Postfach Access-Einstellungen für das Postfach abzurufen.</span><span class="sxs-lookup"><span data-stu-id="27adc-156">Run the following command to get the mailbox access settings for the mailbox.</span></span> 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   <span data-ttu-id="27adc-157">Sie müssen alle diese Zugriffsmethoden in Schritt2 deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="27adc-157">You'll disable all of these access methods in Step 2.</span></span>
    
4. <span data-ttu-id="27adc-158">Führen Sie den folgenden Befehl zum Abrufen von Informationen zu den Haltestatus und Office 365-Aufbewahrungsrichtlinien an das Postfach angewendet.</span><span class="sxs-lookup"><span data-stu-id="27adc-158">Run the following command to get information about the holds and Office 365 retention policies applied to the mailbox.</span></span>
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > <span data-ttu-id="27adc-159">Wenn in der Eigenschaft *InPlaceHolds* zu viele Werte vorhanden sind, und nicht alle angezeigt werden, können Sie Ausführen der `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` Befehl aus, um jeden Wert in einer separaten Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27adc-159">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
5. <span data-ttu-id="27adc-160">Führen Sie den folgenden Befehl zum Abrufen von Informationen über alle organisationsweiten Office 365-Aufbewahrungsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="27adc-160">Run the following command to get information about any organization-wide Office 365 retention policies.</span></span> 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   <span data-ttu-id="27adc-161">Wenn Ihre Organisation eine beliebige organisationsweiten Office 365-Aufbewahrungsrichtlinien verfügt, müssen Sie das Postfach aus dieser Richtlinien in Schritt 3 ausschließen.</span><span class="sxs-lookup"><span data-stu-id="27adc-161">If your organization has any organization-wide Office 365 retention policies, you'll have to exclude the mailbox from these policies in Step 3.</span></span>

   > [!TIP]
    > <span data-ttu-id="27adc-162">Wenn in der Eigenschaft *InPlaceHolds* zu viele Werte vorhanden sind, und nicht alle angezeigt werden, können Sie Ausführen der `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` Befehl aus, um jeden Wert in einer separaten Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="27adc-162">If there are too many values in the  *InPlaceHolds*  property and not all of them are displayed, you can run the  `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` command to display each value on a separate line.</span></span> 
  
6. <span data-ttu-id="27adc-163">Führen Sie den folgenden Befehl aus, um die aktuelle Größe und die Gesamtanzahl der Elemente in Ordner und Unterordner im Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="27adc-163">Run the following command to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="27adc-164">Wenn das Postfach des Benutzers Archiv aktiviert ist, führen Sie den folgenden Befehl zum Abrufen der Größe und der Gesamtzahl der Elemente in Ordner und Unterordner im Ordner "wiederherstellbare Elemente" in ihrem Postfach archivieren.</span><span class="sxs-lookup"><span data-stu-id="27adc-164">If the user's archive mailbox is enabled, run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in their archive mailbox.</span></span> 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   <span data-ttu-id="27adc-p115">Wenn Sie in Schritt 4 Elemente löschen, können Sie auswählen, zu löschen oder Elemente im Ordner "wiederherstellbare Elemente" im primären Archivpostfach des Benutzers nicht löschen. Beachten Sie, dass bei erweiterbares Archivierung für das Postfach aktiviert ist, wird nicht Elemente in einem Hilfs-Archivpostfach gelöscht.</span><span class="sxs-lookup"><span data-stu-id="27adc-p115">When you delete items in Step 4, you can choose to delete or not delete items in the Recoverable Items folder in the user's primary archive mailbox. Note that if auto-expanding archiving is enabled for the mailbox, items in an auxiliary archive mailbox won't be deleted.</span></span>
  
## <a name="step-2-prepare-the-mailbox"></a><span data-ttu-id="27adc-167">Schritt 2: Vorbereiten des Postfachs</span><span class="sxs-lookup"><span data-stu-id="27adc-167">Step 2: Prepare the mailbox</span></span>

<span data-ttu-id="27adc-168">Nach dem Erfassen und Speichern von Informationen über das Postfach, werden im nächste Schritt das Postfach vorbereiten, indem Sie die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="27adc-168">After collecting and saving information about the mailbox, the next step is to prepare the mailbox by performing the following tasks:</span></span> 
  
- <span data-ttu-id="27adc-169">**Clientzugriff auf das Postfach zu deaktivieren** , damit der Postfachbesitzer Zugriff auf ihre Postfächer und ändern Sie die Postfachdaten während dieses Vorgangs ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="27adc-169">**Disable client access to mailbox** so that the mailbox owner can't access their mailbox and make any changes to the mailbox data during this procedure.</span></span> 
    
- <span data-ttu-id="27adc-170">**Erhöhen Sie die Aufbewahrungszeit für gelöschte** auf 30 Tage (Höchstwert in Exchange Online), sodass Elemente aus dem Ordner wiederherstellbare Elemente gelöscht werden nicht, bevor Sie in Schritt 4 gelöscht werden können.</span><span class="sxs-lookup"><span data-stu-id="27adc-170">**Increase the deleted item retention period** to 30 days (the maximum value in Exchange Online) so that items aren't purged from the Recoverable Items folder before you can delete them in Step 4.</span></span> 
    
- <span data-ttu-id="27adc-171">(Für die Dauer der Aufbewahrungszeit für gelöschte) werden nicht so Elementen, **Deaktivieren Sie die Wiederherstellung einzelnen Elemente** aufbewahrt werden, nach dem Löschen aus dem Ordner "wiederherstellbare Elemente" in Schritt 4.</span><span class="sxs-lookup"><span data-stu-id="27adc-171">**Disable single Item recovery** so that items won't be retained (for the duration of the deleted item retention period) after you delete them from the Recoverable Items folder in Step 4.</span></span> 
    
- <span data-ttu-id="27adc-172">**Deaktivieren Sie den Assistenten für verwaltete Ordner** , damit das alles nicht das Postfach zu verarbeiten und die Elemente, die Sie in Schritt 4 löschen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="27adc-172">**Disable the Managed Folder Assistant** so that it doesn't process the mailbox and retain the items that you delete in Step 4.</span></span> 
    
<span data-ttu-id="27adc-173">Führen Sie die folgenden Schritte aus, in Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27adc-173">Perform the following steps in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="27adc-p116">Führen Sie den folgenden Befehl aus, um alle Clientzugriff auf das Postfach zu deaktivieren. Die Befehlssyntax wird davon ausgegangen, dass alle Methoden für den Clientzugriff auf das Postfach aktiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="27adc-p116">Run the following command to disable all client access to the mailbox. The command syntax assumes that all client access methods were enabled on the mailbox.</span></span>

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > <span data-ttu-id="27adc-p117">Es kann so deaktivieren Sie alle Methoden für den Clientzugriff an das Postfach von bis zu 60 Minuten dauern. Beachten Sie, dass diese Zugriffsmethoden deaktivieren den Postfachbesitzer Trennen wird nicht, den sie bereits angemeldet sind. Wenn der Besitzer angemeldet ist nicht, werden nicht diese werden auf ihre Postfächer zugreifen, nachdem diese Zugriffsmethoden deaktiviert werden können.</span><span class="sxs-lookup"><span data-stu-id="27adc-p117">It might take up to 60 minutes to disable all client access methods to the mailbox. Note that disabling these access methods won't disconnect the mailbox owner they're currently signed in. If the owner isn't signed in, then they won't be able to access their mailbox after these access methods are disabled.</span></span> 
  
2. <span data-ttu-id="27adc-p118">Führen Sie den folgenden Befehl aus, um die Aufbewahrungszeit für gelöschte maximal 30 Tage zu erhöhen. Dabei wird vorausgesetzt, dass die aktuelle Einstellung weniger als 30 Tage ist.</span><span class="sxs-lookup"><span data-stu-id="27adc-p118">Run the following command to increase the deleted item retention period the maximum of 30 days. This assumes that the current setting is less than 30 days.</span></span> 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. <span data-ttu-id="27adc-181">Führen Sie den folgenden Befehl zum Deaktivieren der Wiederherstellung einzelner Elemente.</span><span class="sxs-lookup"><span data-stu-id="27adc-181">Run the following command to disable single item recovery.</span></span>
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > <span data-ttu-id="27adc-p119">Es kann bis zu 60 Minuten Wiederherstellung einzelner Elemente deaktivieren dauern. Löschen von Elementen im Ordner "wiederherstellbare Elemente" nicht erst nach Ablauf dieses Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="27adc-p119">It might take up to 60 minutes to disable single item recovery. Don't delete items in the Recoverable Items folder until this period has elapsed.</span></span> 
  
4. <span data-ttu-id="27adc-p120">Führen Sie den folgenden Befehl zum Assistenten für verwaltete Ordner verhindern, dass das Postfach zu verarbeiten. Wie bereits erklärt können Sie den Assistenten für verwaltete Ordner deaktivieren nur, wenn eine Aufbewahrungsrichtlinie Office 365 mit einer Sperre permanentes nicht auf das Postfach angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="27adc-p120">Run the following command to prevent the Managed Folder Assistant from processing the mailbox. As previously explained, you can disable the Managed Folder Assistant only if an Office 365 retention policy with a Preservation Lock is not applied to the mailbox.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a><span data-ttu-id="27adc-186">Schritt 3: Entfernen Sie alle Haltestatus aus dem Postfach</span><span class="sxs-lookup"><span data-stu-id="27adc-186">Step 3: Remove all holds from the mailbox</span></span>

<span data-ttu-id="27adc-p121">Der letzte Schritt, bevor Sie Elemente aus dem Ordner wiederherstellbare Elemente löschen können ist, entfernen alle Haltestatus (, die Sie in Schritt 1 identifiziert) für das Postfach platziert. Alle Haltestatus müssen entfernt werden, sodass Elemente wird nicht beibehalten werden, nachdem Sie diese aus dem Ordner wiederherstellbare Elemente löschen. Die folgenden Abschnitte enthalten Informationen zum Entfernen von verschiedenen Typen von Haltestatus für ein Postfach. Finden Sie [Weitere Informationen](#more-information) im Abschnitt Tipps dazu, wie Sie den Typ Haltestatus zu identifizieren, der für ein Postfach platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="27adc-p121">The last step before you can delete items from the Recoverable Items folder is to remove all holds (that you identified in Step 1) placed on the mailbox. All holds must be removed so that items won't be retained after you delete them from the Recoverable Items folder. The following sections contain information about removing different types of holds on a mailbox. See the [More information](#more-information) section for tips about how to identify the type hold that might be placed on a mailbox.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="27adc-191">Wie bereits zuvor erwähnt überprüfen Sie mit der datensatzverwaltung oder der rechtlichen Abteilungen vor einen Haltestatus aus einem Postfach entfernen.</span><span class="sxs-lookup"><span data-stu-id="27adc-191">As previously stated, check with your records management or legal departments before removing a hold from a mailbox.</span></span> 
  
 ### <a name="litigation-hold"></a><span data-ttu-id="27adc-192">Beweissicherungsverfahren</span><span class="sxs-lookup"><span data-stu-id="27adc-192">Litigation Hold</span></span>
  
<span data-ttu-id="27adc-193">Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Aufbewahrung für eventuelle Rechtsstreitigkeiten aus dem Postfach entfernt.</span><span class="sxs-lookup"><span data-stu-id="27adc-193">Run the following command in Exchange Online PowerShell to remove a Litigation Hold from the mailbox.</span></span>

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> <span data-ttu-id="27adc-p122">Ähnlich wie die Methoden für den Clientzugriff und die Wiederherstellung einzelner Elemente deaktivieren, kann es zum Entfernen der Aufbewahrung für eventuelle Rechtsstreitigkeiten bis zu 60 Minuten dauern. Löschen von Elementen nicht aus dem Ordner wiederherstellbare Elemente, bis dieser Zeitraum abgelaufen ist.</span><span class="sxs-lookup"><span data-stu-id="27adc-p122">Similar to disabling the client access methods and single item recovery, it might take up to 60 minutes to remove the Litigation Hold. Don't delete items from the Recoverable Items folder until this period has elapsed.</span></span> 
  
 ### <a name="in-place-hold"></a><span data-ttu-id="27adc-196">Compliance-Archiv</span><span class="sxs-lookup"><span data-stu-id="27adc-196">In-Place Hold</span></span>
  
<span data-ttu-id="27adc-p123">Führen Sie den folgenden Befehl in Exchange Online PowerShell, um die Compliance-Archivs zu ermitteln, die für das Postfach befindet. Verwenden Sie die GUID für die Compliance-Archivs, die Sie in Schritt 1 identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27adc-p123">Run the following command in Exchange Online PowerShell to identify the In-Place Hold that's placed on the mailbox. Use the GUID for the In-Place Hold that you identified in Step 1.</span></span> 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
<span data-ttu-id="27adc-p124">Nachdem Sie die In-Place Hold identifiziert haben, können Sie die Exchange-Verwaltungskonsole (EAC) oder Exchange Online PowerShell verwenden, an um das Postfach aus dem Haltestatus zu entfernen. Weitere Informationen finden Sie unter [Create or Remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span><span class="sxs-lookup"><span data-stu-id="27adc-p124">After you identify the In-Place Hold, you can use the Exchange admin center (EAC) or Exchange Online PowerShell to remove the mailbox from the hold. For more information, see [Create or remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).</span></span>
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a><span data-ttu-id="27adc-201">Office 365 Aufbewahrungsrichtlinien auf bestimmte Postfächer angewendet</span><span class="sxs-lookup"><span data-stu-id="27adc-201">Office 365 retention policies applied to specific mailboxes</span></span>
  
<span data-ttu-id="27adc-p125">Führen den folgenden Befehl [Sicherheit in Office 365 &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) , die Office 365-Aufbewahrungsrichtlinie zu identifizieren, die auf das Postfach angewendet wird. Verwenden Sie die GUID (einschließlich nicht die `mbx` oder `skp` Präfix) für die Aufbewahrungsrichtlinie, die Sie in Schritt 1 identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27adc-p125">Run the following command in [Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the Office 365 retention policy that is applied to the mailbox. Use the GUID (not including the  `mbx` or  `skp` prefix) for the retention policy that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
<span data-ttu-id="27adc-204">Nachdem Sie die Aufbewahrungsrichtlinie identifiziert haben, wechseln Sie zu dem **Datum Governance** \> **Aufbewahrung** Seite in das Wertpapier &amp; Compliance Center, bearbeiten Sie die Aufbewahrungsrichtlinie, die Sie im vorherigen Schritt identifiziert haben, und entfernen Sie das Postfach aus der Liste der Empfänger, die in der Aufbewahrungsrichtlinie enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="27adc-204">After you identify the retention policy, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy that you identified in the previous step, and remove the mailbox from the list of recipients that are included in the retention policy.</span></span> 
  
 ### <a name="organization-wide-office-365-retention-policies"></a><span data-ttu-id="27adc-205">Office 365-Aufbewahrungsrichtlinien organisationsweiten</span><span class="sxs-lookup"><span data-stu-id="27adc-205">Organization-wide Office 365 retention policies</span></span>
  
<span data-ttu-id="27adc-p126">Organisationsweite und Exchange-Wide Office 365-Aufbewahrungsrichtlinien gelten für alle Postfächer in der Organisation. Sie werden auf Organisationsebene (nicht die Postfachebene) angewendet und werden zurückgegeben, wenn Sie das Cmdlet **Get-OrganizationConfig** in Schritt 1 ausführen. Führen den folgenden Befehl [Sicherheit &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) zum Identifizieren der gesamten Organisation Office 365-Aufbewahrungsrichtlinien. Verwenden Sie die GUID (einschließlich nicht die `mbx` Präfix) für die Organisation geltende Aufbewahrungsrichtlinien, die Sie in Schritt 1 identifiziert.</span><span class="sxs-lookup"><span data-stu-id="27adc-p126">Organization-wide and Exchange-wide Office 365 retention policies are applied to every mailbox in the organization. They are applied at the organization level (not the mailbox level) and are returned when you run the **Get-OrganizationConfig** cmdlet in Step 1. Run the following command in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the organization-wide Office 365 retention policies. Use the GUID (not including the  `mbx` prefix) for the organization-wide retention policies that you identified in Step 1.</span></span> 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

<span data-ttu-id="27adc-p127">Nachdem Sie die gesamte Organisation Office 365-Aufbewahrungsrichtlinien identifiziert haben, wechseln Sie zu dem **Datum Governance** \> **Aufbewahrung** Seite in das Wertpapier &amp; Compliance Center bearbeiten für jede Organisation geltende Aufbewahrungsrichtlinie, die Sie in identifiziert die vorherigen Schritt, und fügen Sie das Postfach in die Liste der ausgeschlossenen Empfänger. Hierdurch wird das Postfach des Benutzers aus der Aufbewahrungsrichtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="27adc-p127">After you identify the organization-wide Office 365 retention policies, go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit each organization-wide retention policy that you identified in the previous step, and add the mailbox to the list of excluded recipients. Doing this will remove the user's mailbox from the retention policy.</span></span> 
  
 ### <a name="ediscovery-case-holds"></a><span data-ttu-id="27adc-212">eDiscovery-Fall enthält</span><span class="sxs-lookup"><span data-stu-id="27adc-212">eDiscovery case holds</span></span>
  
<span data-ttu-id="27adc-p128">Führen die folgenden Befehle [Sicherheit &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) identifiziert den Haltestatus Zusammenhang mit einem eDiscovery-Fall, die an das Postfach angewendet wird. Verwenden Sie die GUID (einschließlich nicht die `UniH` Präfix) für die eDiscovery halten, dass Sie in Schritt 1 identifiziert haben. Beachten Sie, dass der zweite Befehl den Namen der eDiscovery-Fall anzeigt, die der Haltebereich zugeordnet ist. Der dritte Befehl zeigt den Namen des Haltestatus.</span><span class="sxs-lookup"><span data-stu-id="27adc-p128">Run the following commands in [Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) to identify the hold associated with an eDiscovery case that's applied to the mailbox. Use the GUID (not including the  `UniH` prefix) for the eDiscovery hold that you identified in Step 1. Note that the second command displays the name of the eDiscovery case the hold is associated with; the third command displays the name of the hold.</span></span> 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

<span data-ttu-id="27adc-p129">Nachdem Sie den Namen des eDiscovery-Fall und den Haltestatus identifiziert haben, wechseln Sie zu der **Suche &amp; Untersuchung** \> **eDiscovery** -Seite in das Wertpapier &amp; Compliance Center, öffnen Sie die Groß-/Kleinschreibung, und das Postfach aus dem Haltestatus zu entfernen. Weitere Informationen finden Sie unter [Verwalten von eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](manage-ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="27adc-p129">After you've identified the name of the eDiscovery case and the hold, go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and remove the mailbox from the hold. For more information, see [Manage eDiscovery cases in the Office 365 Security &amp; Compliance Center](manage-ediscovery-cases.md).</span></span>
  
## <a name="step-4-delete-items-in-the-recoverable-items-folder"></a><span data-ttu-id="27adc-218">Schritt 4: Löschen von Elementen im Ordner "wiederherstellbare Elemente"</span><span class="sxs-lookup"><span data-stu-id="27adc-218">Step 4: Delete items in the Recoverable Items folder</span></span>

<span data-ttu-id="27adc-p130">Sie können nun Elemente im Ordner "wiederherstellbare Elemente" tatsächlich zu löschen, indem Sie mit dem Cmdlet [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) in Exchange Online PowerShell. Ihnen stehen drei Optionen, wenn das **Search-Mailbox** -Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27adc-p130">Now you're ready to actually delete items in the Recoverable Items folder by using the [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) cmdlet in Exchange Online PowerShell. You have three options when running the **Search-Mailbox** cmdlet.</span></span> 
  
- <span data-ttu-id="27adc-221">Kopieren Sie Elemente in einer Zielpostfach, bevor Sie diese löschen, damit Sie die Elemente bei Bedarf überprüfen können, bevor Sie gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="27adc-221">Copy items to a target mailbox before you delete them so that you can review the items, if necessary, before you delete them.</span></span>
    
- <span data-ttu-id="27adc-222">Kopieren von Elementen in einem Zielpostfach und im gleichen Befehl zu löschen.</span><span class="sxs-lookup"><span data-stu-id="27adc-222">Copy items to a target mailbox and delete them in the same command.</span></span>
    
- <span data-ttu-id="27adc-223">Löschen Sie Elemente, ohne sie in einer Zielpostfach kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="27adc-223">Delete items without copying them to a target mailbox.</span></span> 
    
<span data-ttu-id="27adc-p131">Notiz, die Elemente im Ordner "wiederherstellbare Elemente" im primären Archivpostfach des Benutzers werden ebenfalls gelöscht werden, bei der Ausführung der ** Search-Mailbox ** Cmdlet. Um dies zu verhindern, können Sie die Option *DoNotIncludeArchive* einschließen. Wie bereits zuvor erwähnt, wenn erweiterbares Archivierung für das Postfach aktiviert ist, und die ** Search-Mailbox ** Cmdlet nicht Elemente in einem Hilfs-Archivpostfach gelöscht. Weitere Informationen zu automatisch erweitert archivieren, finden Sie unter [Übersicht über die uneingeschränkte Archivierung in Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="27adc-p131">Note that items in the Recoverable Items folder in the user's primary archive mailbox will also be deleted when you run the ** Search-Mailbox ** cmdlet. To prevent this, you can include the  *DoNotIncludeArchive*  switch. And as previously stated, if auto-expanding archiving is enabled for the mailbox, the ** Search-Mailbox ** cmdlet doesn't deleted items in an auxiliary archive mailbox. For more information about auto-expanding archive, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="27adc-p132">Wenn Sie eine Suchabfrage (durch Verwendung des Parameters  *SearchQuery*  ) einschließen, gibt das Cmdlet **Search-Mailbox** maximal 10.000 Elemente in den Suchergebnissen zurück. Wenn Sie also eine Suchabfrage einschließen, müssen Sie den Befehl **Search-Mailbox** möglicherweise mehrere Male ausführen, um mehr als 10.000 Elemente zu löschen.</span><span class="sxs-lookup"><span data-stu-id="27adc-p132">If you include a search query (by using the  *SearchQuery*  parameter), the **Search-Mailbox** cmdlet will return a maximum of 10,000 items in the search results. Therefore if you include a search query, you might have to run the **Search-Mailbox** command multiple times to delete more than 10,000 items.</span></span> 
  
<span data-ttu-id="27adc-p133">Die folgenden Beispiele zeigen die Befehlssyntax für jede dieser Optionen an. Diese Beispiele verwenden die `-SearchQuery size>0` Wert des Parameters, der alle Elemente in allen Unterordnern im Ordner "wiederherstellbare Elemente" gelöscht. Wenn Sie nur Elemente löschen, die bestimmte Bedingungen erfüllen müssen, können Sie auch den Parameter *SearchQuery* verwenden, Sonstiges wie den Betreff einer Nachricht oder einen Datumsbereich angeben. Finden Sie [Weitere Beispiele für die Verwendung des Parameters SearchQuery](#other-examples-of-using-the-searchquery-parameter) unten.</span><span class="sxs-lookup"><span data-stu-id="27adc-p133">The following examples show the command syntax for each of these options. These examples use the  `-SearchQuery size>0` parameter value, which deletes all items from all subfolders in the Recoverable Items folder. If you need to delete only items that match specific conditions, you can also use the  *SearchQuery*  parameter to specify other conditions, such as the subject of a message or a date range. See the [other examples of using the SearchQuery parameter](#other-examples-of-using-the-searchquery-parameter) below.</span></span> 
  
### <a name="example-1"></a><span data-ttu-id="27adc-234">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27adc-234">Example 1</span></span>

<span data-ttu-id="27adc-p134">In diesem Beispiel werden alle Elemente in den Ordner des Benutzers wiederherstellbare Elemente in einen Ordner in Ihrer Organisation Discoverysuchpostfach kopiert. Auf diese Weise können Sie die Elemente lesen, bevor Sie endgültig löschen.</span><span class="sxs-lookup"><span data-stu-id="27adc-p134">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox. This lets you review the items before you permanently delete them.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

<span data-ttu-id="27adc-p135">Im vorherigen Beispiel ist nicht erforderlich zum Kopieren von Elementen auf dem Discoverysuchpostfach. Sie können eine beliebige Zielpostfach Nachrichten kopieren. Wird jedoch empfohlen, um Zugriff auf sensible Postfachdaten zu verhindern, das Kopieren von Nachrichten an ein Postfach, Zugriff auf autorisierte Personen beschränkt ist. Standardmäßig wird auf den Standardwert Discoverysuchpostfach eingeschränkten Zugriff auf Mitglieder der Rollengruppe "Discoveryverwaltung" im Exchange Online.</span><span class="sxs-lookup"><span data-stu-id="27adc-p135">In the previous example, it isn't required to copy items to the Discovery Search Mailbox. You can copy messages to any target mailbox. However, to prevent access to potentially sensitive mailbox data, we recommend copying messages to a mailbox that has access restricted to authorized personnel. By default, access to the default Discovery Search Mailbox is restricted to members of the Discovery Management role group in Exchange Online.</span></span> 
  
### <a name="example-2"></a><span data-ttu-id="27adc-241">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="27adc-241">Example 2</span></span>

<span data-ttu-id="27adc-242">Dieses Beispiel kopiert alle Elemente in den Ordner des Benutzers wiederherstellbare Elemente in einen Ordner in Ihrer Organisation Discoverysuchpostfach und löscht dann die Elemente aus den Ordner des Benutzers wiederherstellbare Elemente.</span><span class="sxs-lookup"><span data-stu-id="27adc-242">This example copies all items in the user's Recoverable Items folder to a folder in your organization's Discovery Search Mailbox and then deletes the items from the user's Recoverable Items folder.</span></span>

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a><span data-ttu-id="27adc-243">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="27adc-243">Example 3</span></span>

<span data-ttu-id="27adc-244">Dieses Beispiel löscht alle Elemente in den Ordner des Benutzers wiederherstellbare Elemente, ohne sie in einer Zielpostfach kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="27adc-244">This example deletes all items in the user's Recoverable Items folder, without copying them to a target mailbox.</span></span> 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a><span data-ttu-id="27adc-245">Andere Beispiele für die Verwendung des Parameters SearchQuery</span><span class="sxs-lookup"><span data-stu-id="27adc-245">Other examples of using the SearchQuery parameter</span></span>

<span data-ttu-id="27adc-p136">Hier sind einige Beispiele für die Verwendung des Parameters *SearchQuery* bestimmte Nachrichten suchen. Wenn Sie den Parameter *SearchQuery* zum Suchen nach bestimmten Objekten verwenden, sollten Sie die Suchergebnisse in eine Zielpostfach kopieren, damit Sie die Suchergebnisse überprüfen und Überarbeiten die Abfrage bei Bedarf ein, bevor Sie die Ergebnisse einer Suche löschen können.</span><span class="sxs-lookup"><span data-stu-id="27adc-p136">Here are a few examples of using the  *SearchQuery*  parameter to find specific messages. If you use the  *SearchQuery*  parameter to search for specific items, consider copying the search results to a target mailbox so that you can review the search results and then revise the query if necessary before you delete the results of a search.</span></span> 
  
<span data-ttu-id="27adc-248">Dieses Beispiel gibt die Nachrichten, die einen bestimmten Ausdruck in das Feld Betreff enthalten.</span><span class="sxs-lookup"><span data-stu-id="27adc-248">This example returns messages that contain a specific phrase in the Subject field.</span></span>
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

<span data-ttu-id="27adc-249">Dieses Beispiel gibt die Nachrichten, die innerhalb des angegebenen Datumsbereichs gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="27adc-249">This example returns messages that were sent within the specified date range.</span></span>
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
<span data-ttu-id="27adc-250">Dieses Beispiel gibt die Nachrichten, die an die angegebene Person gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="27adc-250">This example returns messages that were sent to the specified person.</span></span>

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a><span data-ttu-id="27adc-251">Stellen Sie sicher, dass Elemente gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="27adc-251">Verify that items were deleted</span></span>

<span data-ttu-id="27adc-p137">Zum bestätigen, dass Sie erfolgreich Elemente aus dem Ordner wiederherstellbare Elemente eines Postfachs gelöscht haben, verwenden Sie **Get-mailboxfolderstatistics abrufen** Cmdlet in Exchange Online PowerShell so überprüfen Sie die Größe und Anzahl der Elemente im Ordner "wiederherstellbare Elemente". Sie können diese Statistiken, mit denen vergleichen, die Sie in Schritt 1 gesammelt.</span><span class="sxs-lookup"><span data-stu-id="27adc-p137">To verify that you've successfully deleted items from the Recoverable Items folder of a mailbox, use **Get-MailboxFolderStatistics** cmdlet in Exchange Online PowerShell to check the size and number of items in Recoverable Items folder. You can compare these statistics with the ones you collected in Step 1.</span></span> 
  
<span data-ttu-id="27adc-254">Führen Sie den folgenden Befehl die aktuelle Größe und die Gesamtanzahl der Elemente im Ordner und Unterordner im Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers abgerufen.</span><span class="sxs-lookup"><span data-stu-id="27adc-254">Run the following command in to get the current size and total number of items in folders and subfolders in the Recoverable Items folder in the user's primary mailbox.</span></span> 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
<span data-ttu-id="27adc-255">Führen Sie den folgenden Befehl aus, um die Größe und die Gesamtanzahl der Elemente im Ordner und Unterordner im Ordner "wiederherstellbare Elemente" im Archivpostfach des Benutzers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="27adc-255">Run the following command to get the size and total number of items in folders and subfolders in the Recoverable Items folder in the user's archive mailbox.</span></span> 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-5-revert-the-mailbox-to-its-previous-state"></a><span data-ttu-id="27adc-256">Schritt 5: Das Postfach in den vorherigen Zustand zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="27adc-256">Step 5: Revert the mailbox to its previous state</span></span>

<span data-ttu-id="27adc-p138">Der letzte Schritt ist das Postfach wieder auf die vorherige Konfiguration wiederherzustellen. Dies bedeutet, dass Zurücksetzen der Eigenschaften, die Sie in Schritt2 geändert und zum erneuten Anwenden der Haltestatus an, denen Sie in Schritt 3 entfernt. Dazu gehören:</span><span class="sxs-lookup"><span data-stu-id="27adc-p138">The final step is to revert the mailbox back to its previous configuration. This means resetting the properties that you changed in Step 2 and re-applying the holds that you removed in Step 3. This includes:</span></span>
  
- <span data-ttu-id="27adc-p139">Ändern der Aufbewahrungszeit für gelöschte auf den vorherigen Wert zurück. Alternativ können Sie dies in Exchange auf 30 Tage, den Höchstwert festgelegt Online lassen.</span><span class="sxs-lookup"><span data-stu-id="27adc-p139">Changing the deleted item retention period back to its previous value. Alternatively, you can just leave this set to 30 days, the maximum value in Exchange Online.</span></span>
    
- <span data-ttu-id="27adc-262">Erneutes Aktivieren Wiederherstellung einzelnen Elemente.</span><span class="sxs-lookup"><span data-stu-id="27adc-262">Re-enabling single Item recovery.</span></span>
    
- <span data-ttu-id="27adc-263">Erneutes Aktivieren der Methods für den Clientzugriff, damit der Besitzer ihre Postfächer zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="27adc-263">Re-enabling the client access methods so that the owner can access their mailbox.</span></span>
    
- <span data-ttu-id="27adc-264">Erneutes Anwenden der Haltestatus und Office 365-Aufbewahrungsrichtlinien, die Sie entfernt.</span><span class="sxs-lookup"><span data-stu-id="27adc-264">Re-applying the holds and Office 365 retention policies that you removed.</span></span>
    
- <span data-ttu-id="27adc-265">Erneutes Aktivieren der Assistenten für verwaltete Ordner das Postfach zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="27adc-265">Re-enabling the Managed Folder Assistant to process the mailbox.</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="27adc-266">Es wird empfohlen, dass Sie warten, 24 Stunden erneut anwenden einer Warteschleife oder die Office 365 Retention Policy (und sichergestellt haben, dass es vorhanden ist), bevor Sie erneut den Assistenten für verwaltete Ordner verarbeitet das Postfach aktivieren.</span><span class="sxs-lookup"><span data-stu-id="27adc-266">We recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant to process the mailbox.</span></span> 
  
<span data-ttu-id="27adc-267">Führen Sie die folgenden Schritte aus (in der angegebenen Reihenfolge) in Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="27adc-267">Perform the following steps (in the specified sequence) in Exchange Online PowerShell.</span></span>
  
1. <span data-ttu-id="27adc-p140">Führen Sie der folgende Befehl zum Ändern der Aufbewahrungszeit für gelöschte wieder in den ursprünglichen Wert. Dabei wird davon ausgegangen, dass die vorherige Einstellung weniger als 30 Tage ist; Beispiel: 14 Tage.</span><span class="sxs-lookup"><span data-stu-id="27adc-p140">Run the following command to change the deleted item retention period back to its original value. This assumes that the previous setting is less than 30 days; for example 14 days.</span></span> 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. <span data-ttu-id="27adc-270">Führen Sie den folgenden Befehl zur Wiederherstellung einzelner Elemente wieder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="27adc-270">Run the following command to re-enable single item recovery.</span></span>
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. <span data-ttu-id="27adc-271">Führen Sie den folgenden Befehl aus, um alle Methoden für den Clientzugriff an das Postfach wieder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="27adc-271">Run the following command to re-enable all client access methods to the mailbox.</span></span>
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. <span data-ttu-id="27adc-p141">Weisen Sie erneut den Haltestatus, die Sie in Schritt 3 entfernt. Je nach Typ des Haltestatus verwenden Sie eines der folgenden Verfahren.</span><span class="sxs-lookup"><span data-stu-id="27adc-p141">Re-apply the holds that you removed in Step 3. Depending on the type of hold, use one of the following procedures.</span></span>
    
    <span data-ttu-id="27adc-274">**Beweissicherungsverfahren**</span><span class="sxs-lookup"><span data-stu-id="27adc-274">**Litigation Hold**</span></span>
    
    <span data-ttu-id="27adc-275">Führen Sie den folgenden Befehl aus, um eine Aufbewahrung für eventuelle Rechtsstreitigkeiten für das Postfach wieder zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="27adc-275">Run the following command to re-enable a Litigation Hold for the mailbox.</span></span>
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    <span data-ttu-id="27adc-276">**In-Place Hold**</span><span class="sxs-lookup"><span data-stu-id="27adc-276">**In-Place Hold**</span></span>
    
    <span data-ttu-id="27adc-277">Verwenden Sie die Exchange-Verwaltungskonsole (oder Exchange Online PowerShell), um das Postfach zurück, der In-Place Hold hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="27adc-277">Use the EAC (or Exchange Online PowerShell) to add the mailbox back to the In-Place Hold.</span></span> 
    
    <span data-ttu-id="27adc-278">**Office 365 Aufbewahrungsrichtlinien auf bestimmte Postfächer angewendet**</span><span class="sxs-lookup"><span data-stu-id="27adc-278">**Office 365 retention policies applied to specific mailboxes**</span></span>
    
    <span data-ttu-id="27adc-p142">Verwenden Sie die Sicherheit &amp; Compliance Center das Postfach wieder in die Office 365-Aufbewahrungsrichtlinie hinzu. Wechseln Sie zu dem **Datum Governance** \> **Aufbewahrung** Seite in das Wertpapier &amp; Compliance Center, bearbeiten Sie die Aufbewahrungsrichtlinie, und fügen Sie das Postfach zurück zur Liste der Empfänger an, die auf die Aufbewahrungsrichtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="27adc-p142">Use the Security &amp; Compliance Center to add the mailbox back to the Office 365 retention policy. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the retention policy, and add the mailbox back to the list of recipients that the retention policy is applied to.</span></span> 
    
    <span data-ttu-id="27adc-281">**Office 365-Aufbewahrungsrichtlinien organisationsweiten**</span><span class="sxs-lookup"><span data-stu-id="27adc-281">**Organization-wide Office 365 retention policies**</span></span>
    
    <span data-ttu-id="27adc-p143">Wenn Sie einer Organisation geltende oder Exchange geltende Aufbewahrungsrichtlinie entfernt, indem Sie es aus der Richtlinie ausschließen, verwenden Sie die Sicherheit &amp; Compliance Center Entfernen des Postfachs aus der Liste der Benutzer ausgeschlossen. Wechseln Sie zu dem **Datum Governance** \> **Aufbewahrung** Seite in das Wertpapier &amp; Compliance Center bearbeiten die Organisation geltende Aufbewahrungsrichtlinie und das Postfach aus der Liste der ausgeschlossenen Empfänger zu entfernen. Auf diese Weise wird die Aufbewahrungsrichtlinie auf das Postfach des Benutzers erneut angewendet.</span><span class="sxs-lookup"><span data-stu-id="27adc-p143">If you removed an organization-wide or Exchange-wide retention policy by excluding it from the policy, then use the Security &amp; Compliance Center to remove the mailbox from the list of excluded users. Go to the **Date governance** \> **Retention** page in the Security &amp; Compliance Center, edit the organization-wide retention policy, and remove the mailbox from the list of excluded recipients. Doing this will re-apply the retention policy to the user's mailbox.</span></span> 
    
    <span data-ttu-id="27adc-285">**eDiscovery-Fall enthält**</span><span class="sxs-lookup"><span data-stu-id="27adc-285">**eDiscovery case holds**</span></span>
    
    <span data-ttu-id="27adc-p144">Verwenden Sie die Sicherheit &amp; Compliance Center das Postfach hinzufügen sichern den Haltestatus, die einem eDiscovery-Fall zugeordnet ist. Wechseln Sie zu der **Suche &amp; Untersuchung** \> **eDiscovery** -Seite in das Wertpapier &amp; Compliance Center, öffnen Sie die Groß-/Kleinschreibung, und das Postfach wieder dem Haltestatus hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="27adc-p144">Use the Security &amp; Compliance Center to add the mailbox back the hold that's associated with an eDiscovery case. Go to the **Search &amp; investigation** \> **eDiscovery** page in the Security &amp; Compliance Center, open the case, and add the mailbox back to the hold.</span></span> 
    
5. <span data-ttu-id="27adc-p145">Führen Sie den folgenden Befehl aus, um den Assistenten für verwaltete Ordner erneut verarbeitet das Postfach zuzulassen. Wie bereits erwähnt, es wird empfohlen, dass Sie warten, 24 Stunden erneut anwenden einer Warteschleife oder die Office 365 Retention Policy (und sichergestellt haben, dass es vorhanden ist), bevor Sie erneut den Assistenten für verwaltete Ordner aktivieren.</span><span class="sxs-lookup"><span data-stu-id="27adc-p145">Run the following command to allow the Managed Folder Assistant to process the mailbox again. As previously stated, we recommend that you wait 24 hours after re-applying a hold or Office 365 retention policy (and verifying that it's in place) before you re-enable the Managed Folder Assistant.</span></span> 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. <span data-ttu-id="27adc-290">Um sicherzustellen, dass das Postfach wieder auf die vorherige Konfiguration wiederhergestellt wurde, können folgende Befehle ausführen, und vergleichen Sie die Einstellungen auf diejenigen aus, denen Sie in Schritt 1 gesammelt.</span><span class="sxs-lookup"><span data-stu-id="27adc-290">To verify that the mailbox has been reverted back to its previous configuration, you can run the following commands and then compare the settings to the ones that you collected in Step 1.</span></span>

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a><span data-ttu-id="27adc-291">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="27adc-291">More information</span></span>

<span data-ttu-id="27adc-p146">Hier ist eine Tabelle, die beschreibt, wie verschiedene Arten von Haltestatus basierend auf den Werten in der *InPlaceHolds* -Eigenschaft, bei der Ausführung der Cmdlets **Get-Mailbox** oder **Get-OrganizationConfig** zu identifizieren. Wie bereits erläutert, müssen Sie alle Haltestatus entfernen und Aufbewahrungsrichtlinien aus einem Postfach, bevor Sie Office 365 können erfolgreich Löschen von Elementen im Ordner "wiederherstellbare Elemente".</span><span class="sxs-lookup"><span data-stu-id="27adc-p146">Here's a table that describes how to identify different types of holds based on the values in the  *InPlaceHolds*  property when you run the **Get-Mailbox** or **Get-OrganizationConfig** cmdlets. As previously explained, you have to remove all holds and Office 365 retention policies from a mailbox before you can successfully delete items in the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="27adc-294">**Haltebereichstyp**</span><span class="sxs-lookup"><span data-stu-id="27adc-294">**Hold type**</span></span>|<span data-ttu-id="27adc-295">**Beispielwert**</span><span class="sxs-lookup"><span data-stu-id="27adc-295">**Example value**</span></span>|<span data-ttu-id="27adc-296">**So identifizieren Sie den Haltestatus**</span><span class="sxs-lookup"><span data-stu-id="27adc-296">**How to identify the hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="27adc-297">Beweissicherungsverfahren</span><span class="sxs-lookup"><span data-stu-id="27adc-297">Litigation Hold</span></span>  <br/> | `True` <br/> |<span data-ttu-id="27adc-298">Die  *LitigationHoldEnabled*  -Eigenschaft wird festgelegt auf  `True`.</span><span class="sxs-lookup"><span data-stu-id="27adc-298">The  *LitigationHoldEnabled*  property is set to  `True`.</span></span>  <br/> |
|<span data-ttu-id="27adc-299">Compliance-Archiv</span><span class="sxs-lookup"><span data-stu-id="27adc-299">In-Place Hold</span></span>  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |<span data-ttu-id="27adc-p147">Die *InPlaceHolds* -Eigenschaft enthält die GUID der der Compliance-Archivs, das für das Postfach befindet. Sie können erkennen, dass dies eine In-Place Hold ist, da die GUID nicht mit einem Präfix beginnt.</span><span class="sxs-lookup"><span data-stu-id="27adc-p147">The  *InPlaceHolds*  property contains the GUID of the In-Place Hold that's placed on the mailbox. You can tell this is an In-Place Hold because the GUID doesn't start with a prefix.  </span></span><br/> <span data-ttu-id="27adc-302">Sie können den Befehl  \`Get-MailboxSearch -InPlaceHoldIdentity <hold GUID></span><span class="sxs-lookup"><span data-stu-id="27adc-302">You can use the  \`Get-MailboxSearch -InPlaceHoldIdentity <hold GUID></span></span> | <span data-ttu-id="27adc-303">FL "Command in Exchange Online PowerShell Abrufen von Informationen zu den In-Place Hold für das Postfach.</span><span class="sxs-lookup"><span data-stu-id="27adc-303">FL\` command in Exchange Online PowerShell to get information about the In-Place Hold on the mailbox.</span></span>  <br/> |
| <span data-ttu-id="27adc-304">Office 365-Aufbewahrungsrichtlinien in das Wertpapier &amp; Compliance Center auf bestimmte Postfächer angewendet</span><span class="sxs-lookup"><span data-stu-id="27adc-304">Office 365 retention policies in the Security &amp; Compliance Center applied to specific mailboxes</span></span>  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> <span data-ttu-id="27adc-305">oder</span><span class="sxs-lookup"><span data-stu-id="27adc-305">or</span></span>  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |<span data-ttu-id="27adc-p148">Wenn Sie das Cmdlet **Get-Mailbox** ausführen, enthält die *InPlaceHolds* -Eigenschaft auch GUIDs der Office 365-Aufbewahrungsrichtlinien an das Postfach angewendet. Sie können Aufbewahrungsrichtlinien identifizieren, weil die GUID mit beginnt die `mbx` Präfix. Beachten Sie, dass die GUID der Aufbewahrungsrichtlinie mit beginnt die `skp` Präfix, die das gibt an, dass die Aufbewahrungsrichtlinie auf Skype für Business Unterhaltungen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="27adc-p148">When you run the **Get-Mailbox** cmdlet, the  *InPlaceHolds*  property also contains GUIDs of Office 365 retention policies applied to the mailbox. You can identify retention policies because the GUID starts with the  `mbx` prefix. Note that if the GUID of the retention policy starts with the  `skp` prefix, that indicates that the retention policy is applied to Skype for Business conversations.  </span></span><br/> <span data-ttu-id="27adc-309">Identität der Office 365-Aufbewahrungsrichtlinie, die an das Postfach angewendet wird, führen Sie den folgenden Befehl in der Sicherheit &amp; Compliance Center PowerShell:</span><span class="sxs-lookup"><span data-stu-id="27adc-309">To identity the Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell:</span></span> <br/> <br/><span data-ttu-id="27adc-310">"Get-RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="27adc-310">\`Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="27adc-311">FL Name`<br/><br/>Be sure to remove the  `Mbx` or  `Skp' Präfix, wenn Sie diesen Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="27adc-311">FL Name`<br/><br/>Be sure to remove the  `mbx` or  `skp\` prefix when you run this command.</span></span>  <br/> |
|<span data-ttu-id="27adc-312">Organisationsweite Office 365-Aufbewahrungsrichtlinien in das Wertpapier &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="27adc-312">Organization-wide Office 365 retention policies in the Security &amp; Compliance Center</span></span>  <br/> |<span data-ttu-id="27adc-313">Kein Wert</span><span class="sxs-lookup"><span data-stu-id="27adc-313">No value</span></span>  <br/> <span data-ttu-id="27adc-314">oder</span><span class="sxs-lookup"><span data-stu-id="27adc-314">or</span></span>  <br/>  <span data-ttu-id="27adc-315">`-mbxe9b52bf7ab3b46a286308ecb29624696`(gibt an, dass das Postfach von eine unternehmensweite Richtlinie ausgeschlossen ist)</span><span class="sxs-lookup"><span data-stu-id="27adc-315">`-mbxe9b52bf7ab3b46a286308ecb29624696` (indicates that the mailbox is excluded from an organization-wide policy)</span></span>  <br/> |<span data-ttu-id="27adc-316">Selbst wenn die *InPlaceHolds* -Eigenschaft leer ist, wenn Sie das **Get-Mailbox** -Cmdlet ausführen, weiterhin möglicherweise mindestens einen organisationsweiten Office 365 Aufbewahrungsrichtlinien auf das Postfach angewendet.</span><span class="sxs-lookup"><span data-stu-id="27adc-316">Even if the  *InPlaceHolds*  property is empty when you run the **Get-Mailbox** cmdlet, there still might be one or more organization-wide Office 365 retention policies applied to the mailbox.</span></span>  <br/> <span data-ttu-id="27adc-317">Um dies zu überprüfen, führen Sie das "Get-OrganizationConfig</span><span class="sxs-lookup"><span data-stu-id="27adc-317">To verify this, you can run the  \`Get-OrganizationConfig</span></span> | <span data-ttu-id="27adc-318">FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `Mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell: <br/><br/> `Get-RetentionCompliancePolicy<retention policy GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="27adc-318">FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell: <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix></span></span> | <span data-ttu-id="27adc-319">FL Name`<br/><br/>Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `Mbx -`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696'</span><span class="sxs-lookup"><span data-stu-id="27adc-319">FL Name`<br/><br/>Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `-mbx`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696\`</span></span> <br/> |
|<span data-ttu-id="27adc-320">eDiscovery-Fall in der Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="27adc-320">eDiscovery case hold in the Security &amp; Compliance Center</span></span>  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |<span data-ttu-id="27adc-p149">Die *InPlaceHolds* -Eigenschaft enthält auch die GUID des eine Sperre einer eDiscovery-Fall in das Wertpapier zugeordnet &amp; Compliance Center, die für das Postfach verwendet werden kann. Sie können erkennen, dies ist ein eDiscovery Groß-/Kleinschreibung halten, da die GUID mit beginnt die `UniH` Präfix.</span><span class="sxs-lookup"><span data-stu-id="27adc-p149">The  *InPlaceHolds*  property also contains the GUID of any hold associated with an eDiscovery case in the Security &amp; Compliance Center that might be placed on the mailbox. You can tell this is an eDiscovery case hold because the GUID starts with the  `UniH` prefix.  </span></span><br/> <span data-ttu-id="27adc-p150">Sie können die `Get-CaseHoldPolicy` -Cmdlet in Security &amp; Compliance Center PowerShell Abrufen von Informationen zu eDiscovery-Fall, die die Sperre für das Postfach zugeordnet ist. Beispielsweise können Sie den Befehl ausführen "Get-CaseHoldPolicy<hold GUID without prefix></span><span class="sxs-lookup"><span data-stu-id="27adc-p150">You can use the  `Get-CaseHoldPolicy` cmdlet in Security &amp; Compliance Center PowerShell to get information about the eDiscovery case that the hold on the mailbox is associated with. For example, you can run the command  \`Get-CaseHoldPolicy <hold GUID without prefix></span></span> | <span data-ttu-id="27adc-325">FL Name` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix> `<br/><br/>`Get-ComplianceCase $CaseHold.CaseId</span><span class="sxs-lookup"><span data-stu-id="27adc-325">FL Name` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId</span></span> | <span data-ttu-id="27adc-326">FL Name'</span><span class="sxs-lookup"><span data-stu-id="27adc-326">FL Name\`</span></span>


