---
title: Erhöhen des Kontingents für wiederherstellbare Elemente für im In-Situ-Speicher befindliche Postfächer
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: 'Aktivieren Sie das Archivpostfach, und aktivieren Sie die automatische Erweiterung der Archivierung, um die Größe des Ordners "Wiederherstellbare Elemente" für ein Postfach in Office 365 zu erhöhen. '
ms.openlocfilehash: 701821074294441525315c3db77daeccd5700935
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296538"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a><span data-ttu-id="fa11a-103">Erhöhen des Kontingents für wiederherstellbare Elemente für im In-Situ-Speicher befindliche Postfächer</span><span class="sxs-lookup"><span data-stu-id="fa11a-103">Increase the Recoverable Items quota for mailboxes on hold</span></span>

<span data-ttu-id="fa11a-p101">Die standardmäßige Aufbewahrungsrichtlinie "Default MRM Policy", die automatisch auf neue Postfächer in Exchange Online angewendet wird, enthält ein Aufbewahrungs mit dem Namen "Wiederherstellbare Elemente 14 Tage in Archiv verschieben". Mit diesem Aufbewahrungs werden Elemente aus dem Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner "Wiederherstellbare Elemente" im Archivpostfach des Benutzers verschoben, nachdem die Aufbewahrungsdauer für ein Element von 14 Tagen abgelaufen ist. Damit dies geschieht, muss das Archivpostfach des Benutzers aktiviert sein. Wenn das Archivpostfach nicht aktiviert ist, wird keine Aktion ausgeführt, was bedeutet, dass Elemente im Ordner "Wiederherstellbare Elemente" für ein gespeichertes Postfach nicht nach Ablauf des Aufbewahrungszeitraums von 14 Tagen in das Archivpostfach verschoben werden. Da nichts aus einem Postfach gelöscht wird, ist es möglich, dass das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" überschritten wird, insbesondere, wenn das Archivpostfach des Benutzers nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa11a-p101">The default retention policy—named Default MRM Policy—that is automatically applied to new mailboxes in Exchange Online contains a retention tag named Recoverable Items 14 days move to archive. This retention tag moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox after the 14-day retention period expires for an item. For this to happen, the user's archive mailbox must be enabled. If the archive mailbox isn't enabled, no action is taken, which means that items in the Recoverable Items folder for a mailbox on hold aren't moved to the archive mailbox after the 14-day retention period expires. Because nothing is deleted from a mailbox on hold, it's possible that the storage quota for the Recoverable Items folder might be exceeded, especially if the user's archive mailbox isn't enabled.</span></span> 
  
<span data-ttu-id="fa11a-p102">Um die Wahrscheinlichkeit zu verringern, dass dieser Grenzwert überschritten wird, wird das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" automatisch von 30 GB auf 100 GB erhöht, wenn ein Haltebereich für ein Postfach in Exchange Online gespeichert wird. Wenn das Archivpostfach aktiviert ist, wird das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" im Archivpostfach ebenfalls von 30 GB auf 100 GB erhöht. Wenn das Feature für die automatische Erweiterung der Archivierung in Exchange Online aktiviert ist, ist das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" im Archiv des Benutzers unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="fa11a-p102">To help reduce the chance of exceeding this limit, the storage quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when a hold is placed on a mailbox in Exchange Online. If the archive mailbox is enabled, the storage quota for the Recoverable Items folder in the archive mailbox is also increased from 30 GB to 100 GB. If the auto-expanding archiving feature in Exchange Online is enabled, the storage quota for the Recoverable Items folder in the user's archive will be unlimited.</span></span>
  
 <span data-ttu-id="fa11a-112"> In der folgenden Tabelle sind die Speicherkontingente für den Ordner „Wiederherstellbare Elemente“ zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="fa11a-112">The following table summarizes the storage quota for the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="fa11a-113">**Speicherort des Ordners „Wiederherstellbare Elemente“**</span><span class="sxs-lookup"><span data-stu-id="fa11a-113">**Location of Recoverable Items folder**</span></span>|<span data-ttu-id="fa11a-114">**Nicht aufzubewahrende Postfächer**</span><span class="sxs-lookup"><span data-stu-id="fa11a-114">**Mailboxes not on hold**</span></span>|<span data-ttu-id="fa11a-115">**Aufzubewahrende Postfächer**</span><span class="sxs-lookup"><span data-stu-id="fa11a-115">**Mailboxes on hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa11a-116">Primäres Postfach</span><span class="sxs-lookup"><span data-stu-id="fa11a-116">Primary mailbox</span></span>  <br/> |<span data-ttu-id="fa11a-117">30 GB</span><span class="sxs-lookup"><span data-stu-id="fa11a-117">30 GB</span></span>  <br/> |<span data-ttu-id="fa11a-118">100 GB</span><span class="sxs-lookup"><span data-stu-id="fa11a-118">100 GB</span></span>  <br/> |
|<span data-ttu-id="fa11a-119">Archivpostfach<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="fa11a-119">Archive mailbox<sup>\*</sup></span></span> <br/> |<span data-ttu-id="fa11a-120">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="fa11a-120">Unlimited</span></span>  <br/> |<span data-ttu-id="fa11a-121">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="fa11a-121">Unlimited</span></span>  <br/> |
|<span data-ttu-id="fa11a-122">**Gesamtspeicherkontingent für den Ordner „Wiederherstellbare Elemente“**</span><span class="sxs-lookup"><span data-stu-id="fa11a-122">**Total storage quota for the Recoverable Items folder**</span></span> <br/> |<span data-ttu-id="fa11a-123">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="fa11a-123">Unlimited</span></span>  <br/> |<span data-ttu-id="fa11a-124">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="fa11a-124">Unlimited</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="fa11a-p103"><sup>\*</sup>Das anfängliche Speicherkontingent für das Archivpostfach beträgt 100 GB für Benutzer mit einer Exchange Online-Lizenz (Plan 2). Wenn die automatische Erweiterung der Archivierung jedoch für Postfächer aktiviert ist, wird das Speicherkontingent für das Archivpostfach und den Ordner "Wiederherstellbare Elemente" auf 110 GB erhöht. Bei Bedarf wird zusätzlicher Archivspeicher Platz zur Verfügung gestellt, was eine unbegrenzte Menge an Archivspeicher zur Folge hat. Weitere Informationen zur automatischen Erweiterung der Archivierung finden Sie unter [Übersicht über die unbegrenzte Archivierung in Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="fa11a-p103"><sup>\*</sup> The initial storage quota for the archive mailbox is 100 GB for users with an Exchange Online (Plan 2) license. However, when auto-expanding archiving is turned on for mailboxes on hold, the storage quota for both the archive mailbox and the Recoverable Items folder is increased to 110 GB. Additional archive storage space will be provisioned when necessary which results in an unlimited amount of archive storage. For more information about auto-expanding archiving, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
<span data-ttu-id="fa11a-129">Wenn das Speicherkontingent für den Ordner „Wiederherstellbare Elemente“ im primären Postfach eines aufzubewahrenden Postfachs seinen Grenzwert bald erreicht, können Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="fa11a-129">When the storage quota for the Recoverable Items folder in the primary mailbox of a mailbox on hold is close to reaching its limit, you can do the following things:</span></span>
  
- <span data-ttu-id="fa11a-p104">**Aktivieren Sie das Archivpostfach, und** aktivieren Sie die automatische Erweiterung der Archivierung-Sie können eine unbegrenzte Speicherkapazität für den Ordner "Wiederherstellbare Elemente" aktivieren, indem Sie einfach das Archivpostfach aktivieren und dann das Feature für die automatische Erweiterung der Archivierung in Exchange Online. Dies führt zu 110 GB für den Ordner "Wiederherstellbare Elemente" im primären Postfach und eine unbegrenzte Speicherkapazität für den Ordner "Wiederherstellbare Elemente" im Archiv des Benutzers. Weitere Informationen finden Sie unter Vorgehensweise: [aktivieren &amp; von archivpostfächern im Office 365 Security Compliance Center](enable-archive-mailboxes.md) und Aktivieren der unlimitierten [Archivierung in Office 365](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="fa11a-p104">**Enable the archive mailbox and turn on auto-expanding archiving** - You can enable an unlimited storage capacity for the Recoverable Items folder simply by enabling the archive mailbox and then turning on the auto-expanding archiving feature in Exchange Online. This results in 110 GB for the Recoverable Items folder in the primary mailbox and an unlimited amount of storage capacity for the Recoverable Items folder in the user's archive. See how: [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="fa11a-p105">Nachdem Sie das Archiv für ein Postfach aktiviert haben, das das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" nicht überschreitet, können Sie den Assistenten für verwaltete Ordner ausführen, um den Assistenten für die Verarbeitung des Postfachs manuell auszulösen, sodass abgelaufene Elemente verschoben werden. Ordner "Wiederherstellbare Elemente" im Archivpostfach. Weitere Informationen finden Sie unter [Schritt 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) . Beachten Sie, dass andere Elemente im Postfach des Benutzers möglicherweise in das neue Archivpostfach verschoben werden. Sie sollten dem Benutzer mitteilen, dass dies nach der Aktivierung des Archivpostfachs möglicherweise geschieht.</span><span class="sxs-lookup"><span data-stu-id="fa11a-p105">After you enable the archive for a mailbox that's close to exceeding the storage quota for the Recoverable Items folder, you might want to run the Managed Folder Assistant to manually trigger the assistant to process the mailbox so that expired items are moved the Recoverable Items folder in the archive mailbox. See [Step 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) for instructions. Note that other items in the user's mailbox might be moved to the new archive mailbox. Consider telling the user that this may happen after you enable the archive mailbox.</span></span> 
  
- <span data-ttu-id="fa11a-p106">**Erstellen einer benutzerdefinierten Aufbewahrungsrichtlinie für Postfächer in der Warteschleife** – zusätzlich zur Aktivierung des Archivpostfachs und der automatischen Erweiterung der Archivierung von Postfächern im Rechtsstreit oder in-situ-Speicherung möchten Sie möglicherweise auch eine benutzerdefinierte Aufbewahrungsrichtlinie für Postfächer erstellen. situ. Auf diese Weise können Sie eine Aufbewahrungsrichtlinie auf Postfächer anwenden, die sich von der standardmäßigen MRM-Richtlinie unterscheidet, die auf Postfächer angewendet wird, die nicht in der Warteschleife gespeichert sind. Auf diese Weise können Sie Aufbewahrungstags anwenden, die speziell für Postfächer vorgesehen sind. Dazu gehört das Erstellen eines neuen Aufbewahrungstags für den Ordner "Wiederherstellbare Elemente".</span><span class="sxs-lookup"><span data-stu-id="fa11a-p106">**Create a custom retention policy for mailboxes on hold** - In addition to enabling the archive mailbox and auto-expanding archiving for mailboxes on Litigation Hold or In-Place Hold, you might also want to create a custom retention policy for mailboxes on hold. This let's you apply a retention policy to mailboxes on hold that's different from the Default MRM Policy that's applied to mailboxes that aren't on hold. This lets you to apply retention tags that are specifically designed for mailboxes on hold. This includes creating a new retention tag for the Recoverable Items folder.</span></span> 
    
<span data-ttu-id="fa11a-141">Im restlichen Thema werden die schrittweisen Anweisungen zum Erstellen einer benutzerdefinierten Aufbewahrungsrichtlinie für aufzubewahrende Postfächer erläutert.</span><span class="sxs-lookup"><span data-stu-id="fa11a-141">The remainder of this topic describes the step-by-step procedures to create a custom retention policy for mailboxes on hold.</span></span>
  
[<span data-ttu-id="fa11a-142">Schritt 1: Erstellen eines benutzerdefinierten Aufbewahrungstags für den Ordner „Wiederherstellbare Elemente“</span><span class="sxs-lookup"><span data-stu-id="fa11a-142">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

<span data-ttu-id="fa11a-143">[[Schritt 2: Erstellen einer neuen Aufbewahrungsrichtlinie für Postfächer in der Warteschleife](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span><span class="sxs-lookup"><span data-stu-id="fa11a-143">[[Step 2: Create a new retention policy for mailboxes on hold](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span></span>

[<span data-ttu-id="fa11a-144">Schritt 3: Anwenden der neuen Aufbewahrungsrichtlinie auf aufzubewahrende Postfächer</span><span class="sxs-lookup"><span data-stu-id="fa11a-144">Step 3: Apply the new retention policy to mailboxes on hold</span></span>](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[<span data-ttu-id="fa11a-145">(Optional) Schritt 4: Ausführen des Assistenten für verwaltete Ordner zum Anwenden der neuen Aufbewahrungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="fa11a-145">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a><span data-ttu-id="fa11a-146">Schritt 1: Erstellen eines benutzerdefinierten Aufbewahrungstags für den Ordner „Wiederherstellbare Elemente“</span><span class="sxs-lookup"><span data-stu-id="fa11a-146">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>

<span data-ttu-id="fa11a-p107">Der erste Schritt besteht darin, ein benutzerdefiniertes Aufbewahrungs (als Aufbewahrungsrichtlinientag oder RPT bezeichnet) für den Ordner "Wiederherstellbare Elemente" zu erstellen. Wie bereits erläutert, verschiebt dieser RPT Elemente aus dem Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner "Wiederherstellbare Elemente" im Archivpostfach des Benutzers. Sie müssen PowerShell verwenden, um eine RPT für den Ordner "Wiederherstellbare Elemente" zu erstellen. Die Exchange-Verwaltungskonsole kann nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa11a-p107">The first step is to create a custom retention tag (called a retention policy tag or RPT) for the Recoverable Items folder. As previously explained, this RPT moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox. You have to use PowerShell to create an RPT for the Recoverable Items folder. You can't use the Exchange admin center (EAC).</span></span> 
  
1. [<span data-ttu-id="fa11a-151">Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa11a-151">Connect to Exchange Online using remote PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. <span data-ttu-id="fa11a-152">Führen Sie den folgenden Befehl zum Erstellen eines Aufbewahrungstags für den Ordner „Wiederherstellbare Elemente“ aus: </span><span class="sxs-lookup"><span data-stu-id="fa11a-152">Run the following command to create a new RPT for the Recoverable Items folder:</span></span> 
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    <span data-ttu-id="fa11a-p108">Durch den folgenden Befehl wird beispielsweise ein Aufbewahrungstag für den Ordner „Wiederherstellbare Elemente“ mit dem Namen „Wiederherstellbare Elemente, 30 Tage, für aufzubewahrende Postfächer“ mit einem Aufbewahrungszeitraum von 30 Tagen erstellt. Dies bedeutet, dass ein Element, nachdem es 30 Tage lang im Ordner „Wiederherstellbare Elemente“ gespeichert war, in den Ordner „Wiederherstellbare Elemente“ im Archivpostfach des Benutzers verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="fa11a-p108">For example, the following command creates a RPT for the Recoverable Items folder named "Recoverable Items 30 days for mailboxes on hold", with a retention period of 30 days. This means that after an item has been in the Recoverable Items folder for 30 days, it will be moved to the Recoverable Items folder in the user's archive mailbox.</span></span>
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > <span data-ttu-id="fa11a-p109">Es wird empfohlen, dass der Aufbewahrungszeitraum (definiert durch den _AgeLimitForRetention_ -Parameter) für die zurückzuGebenden Elemente RPT mit dem Aufbewahrungszeitraum für gelöschte Elemente für die Postfächer identisch ist, auf die die RPT angewendet wird. Dadurch kann ein Benutzer den gesamten Aufbewahrungszeitraum für gelöschte Elemente wiederherstellen, bevor er in das Archivpostfach verschoben wird. Im vorherigen Beispiel wurde der Aufbewahrungszeitraum auf 30 Tage festgelegt, basierend auf der Annahme, dass der Aufbewahrungszeitraum für gelöschte Elemente auch 30 Tage beträgt. Ein Exchange Online-Postfach ist so konfiguriert, dass gelöschte Elemente standardmäßig 14 Tage aufbewahrt werden. Sie können diese Einstellung jedoch auf maximal 30 Tage ändern. Weitere Informationen finden Sie unter [Ändern des Aufbewahrungszeitraums für gelöschte Elemente für ein Postfach in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span><span class="sxs-lookup"><span data-stu-id="fa11a-p109">We recommend that the retention period (defined by the  _AgeLimitForRetention_ parameter) for the Recoverable Items RPT is the same as the deleted item retention period for the mailboxes that the RPT will be applied to. This allows a user the entire deleted item retention period to recover deleted items before they are moved to the archive mailbox. In the previous example, the retention period was set to 30 days based on the assumption that the deleted item retention period for mailboxes is also 30 days. An Exchange Online mailbox is configured to retain deleted items for 14 days, by default. But you can change this setting to a maximum of 30 days. For more information, see [Change the deleted item retention period for a mailbox in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span></span> 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a><span data-ttu-id="fa11a-161">Schritt 2: Erstellen einer neuen Aufbewahrungsrichtlinie für aufzubewahrende Postfächer</span><span class="sxs-lookup"><span data-stu-id="fa11a-161">Step 2: Create a new retention policy for mailboxes on hold</span></span>

<span data-ttu-id="fa11a-p110">Der nächste Schritt besteht darin, eine neue Aufbewahrungsrichtlinie zu erstellen und dieser Aufbewahrungstags hinzuzufügen, einschließlich der Aufbewahrungstags für wiederherstellbare Elemente, die Sie in Schritt 1 erstellt haben. Diese neue Richtlinie wird im nächsten Schritt auf aufzubewahrende Postfächer angewendet. </span><span class="sxs-lookup"><span data-stu-id="fa11a-p110">The next step is to create a new retention policy and add retention tags to it, including the Recoverable Items RPT that you created in Step 1. This new policy will be applied to mailboxes on hold in the next step.</span></span> 
  
<span data-ttu-id="fa11a-p111">Bevor Sie die neue Aufbewahrungsrichtlinie erstellen, ermitteln Sie die zusätzlichen Aufbewahrungstags, die Sie hinzufügen möchten. Eine Liste der Aufbewahrungstags, die der Standard-MRM-Richtlinie hinzugefügt werden, sowie Informationen zum Erstellen neuer Aufbewahrungstags finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="fa11a-p111">Before you create the new retention policy, determine the additional retention tags that you want to add. For a list of the retention tags that are added to the Default MRM Policy and for information about creating new retention tags, see the following:</span></span>
  
- [<span data-ttu-id="fa11a-166">Standardmäßige AufbewahrungsRichtlinie in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="fa11a-166">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [<span data-ttu-id="fa11a-167">Standardordner, die Aufbewahrungsrichtlinientags unterstützen</span><span class="sxs-lookup"><span data-stu-id="fa11a-167">Default folders that support Retention Policy Tags</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- <span data-ttu-id="fa11a-168">Der Abschnitt "Erstellen eines Aufbewahrungstags" im Thema [Erstellen einer Aufbewahrungsrichtlinie](https://go.microsoft.com/fwlink/p/?LinkId=404422) .</span><span class="sxs-lookup"><span data-stu-id="fa11a-168">The "Create a retention tag" section in the [Create a Retention Policy](https://go.microsoft.com/fwlink/p/?LinkId=404422) topic.</span></span>
    
<span data-ttu-id="fa11a-169">Sie können die EAC oder Exchange Online PowerShell verwenden, um eine Aufbewahrungsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa11a-169">You can use the EAC or Exchange Online PowerShell to create a retention policy.</span></span>
  
### <a name="use-the-eac-to-create-a-retention-policy"></a><span data-ttu-id="fa11a-170">Erstellen einer Aufbewahrungsrichtlinie mithilfe der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="fa11a-170">Use the EAC to create a retention policy</span></span>
  
1. <span data-ttu-id="fa11a-171">Wechseln Sie in der Exchange- **Verwaltungs** \> Konsole zu **Aufbewahrungsrichtlinien**für Compliance \*\*\*\* ![-Verwaltung,](media/ITPro-EAC-AddIcon.gif)und klicken Sie dann auf hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="fa11a-171">In the EAC, go to **Compliance management** \> **Retention policies**, and then click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
2. <span data-ttu-id="fa11a-172">Geben Sie auf der Seite **Neue Aufbewahrungsrichtlinie** unter **Name** einen Namen ein, der den Zweck der Aufbewahrungsrichtlinie beschreibt, z. B. **MRM Policy for Mailboxes on Hold**. </span><span class="sxs-lookup"><span data-stu-id="fa11a-172">On the **New retention policy** page, under **Name**, type a name that describes the purpose of the retention policy; for example, **MRM Policy for Mailboxes on Hold**.</span></span> 
    
3. <span data-ttu-id="fa11a-173">Klicken Sie unter **Aufbewahrungstags**auf Add](media/ITPro-EAC-AddIcon.gif)-Symbol **Hinzufügen** ![.</span><span class="sxs-lookup"><span data-stu-id="fa11a-173">Under **Retention tags**, click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="fa11a-174">Wählen Sie in der Liste mit Aufbewahrungstags das Aufbewahrungstag für wiederherstellbare Elemente aus, das Sie in Schritt 1 erstellt haben, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="fa11a-174">In the list of retention tags, select the Recoverable Items RPT that you created in Step 1, and then click **Add**.</span></span>
    
    ![Wählen Sie das benutzerdefinierte Aufbewahrungstag „Wiederherstellbare Elemente“ aus.](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. <span data-ttu-id="fa11a-p112">Wählen Sie zusätzliche Aufbewahrungstags aus, die der Aufbewahrungsrichtlinie hinzugefügt werden sollen. Sie können beispielsweise dieselben Tags hinzufügen, die in der Standard-MRM-Richtlinie enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="fa11a-p112">Select additional retention tags to add to the retention policy. For example, you might want to add the same tags that are included in the Default MRM Policy.</span></span>
    
6. <span data-ttu-id="fa11a-178">Klicken Sie auf **OK**, wenn Sie mit dem Hinzufügen von Aufbewahrungstags fertig sind.</span><span class="sxs-lookup"><span data-stu-id="fa11a-178">When you're finished adding retention tags, click **OK**.</span></span>
    
7. <span data-ttu-id="fa11a-179">Klicken Sie auf **Speichern**, um die neue Aufbewahrungsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa11a-179">Click **Save** to create the new retention policy.</span></span> 
    
    <span data-ttu-id="fa11a-180">Im Detailbereich werden Aufbewahrungstags verknüpft mit der Aufbewahrungsrichtlinie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa11a-180">Notice that the retention tags linked to the retention policy are displayed in the details pane.</span></span>
    
    ![Im Detailbereich werden Aufbewahrungstags verknüpft mit der Aufbewahrungsrichtlinie angezeigt.](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a><span data-ttu-id="fa11a-182">Verwenden von Exchange Online PowerShell zum Erstellen einer Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fa11a-182">Use Exchange Online PowerShell to create a retention policy</span></span>
  
<span data-ttu-id="fa11a-183">Führen Sie zum Erstellen einer neuen Aufbewahrungsrichtlinie für aufzubewahrende Postfächer den folgenden Befehl aus: </span><span class="sxs-lookup"><span data-stu-id="fa11a-183">Run the following command to create new retention policy for mailboxes on hold.</span></span> 
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

<span data-ttu-id="fa11a-184">Durch den folgenden Befehl wird beispielsweise die Aufbewahrungsrichtlinie erstellt und mit Aufbewahrungstags verknüpft, die in der vorherigen Abbildung dargestellt sind.</span><span class="sxs-lookup"><span data-stu-id="fa11a-184">For example, the following command creates the retention policy and linked retention tags that is displayed in the previous illustration.</span></span>
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a><span data-ttu-id="fa11a-185">Schritt 3: Anwenden der neuen Aufbewahrungsrichtlinie auf aufzubewahrende Postfächer</span><span class="sxs-lookup"><span data-stu-id="fa11a-185">Step 3: Apply the new retention policy to mailboxes on hold</span></span>

<span data-ttu-id="fa11a-p113">Der letzte Schritt besteht darin, die neue Aufbewahrungsrichtlinie, die Sie in Schritt 2 erstellt haben, auf Postfächer in Ihrer Organisation anzuwenden. Sie können die EAC oder Exchange Online PowerShell verwenden, um die Aufbewahrungsrichtlinie auf ein einzelnes Postfach oder auf mehrere Postfächer anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="fa11a-p113">The last step is to apply the new retention policy that you created in Step 2 to mailboxes on hold in your organization. You can use the EAC or Exchange Online PowerShell to apply the retention policy to a single mailbox or to multiple mailboxes.</span></span> 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a><span data-ttu-id="fa11a-188">Anwenden der neuen Aufbewahrungsrichtlinie mithilfe der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="fa11a-188">Use the EAC to apply the new retention policy</span></span>
  
1. <span data-ttu-id="fa11a-189">Navigieren Sie zu **Empfänger** \> **Postfächer**.</span><span class="sxs-lookup"><span data-stu-id="fa11a-189">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="fa11a-190">Wählen Sie in der Listenansicht das Postfach aus, auf das Sie die Aufbewahrungsrichtlinie anwenden möchten, \*\*\*\* ![und klicken Sie](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)dann auf Bearbeitungssymbol bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="fa11a-190">In the list view, select the mailbox you want to apply the retention policy to, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
3. <span data-ttu-id="fa11a-191">Klicken Sie auf der Seite **Benutzerpostfach** auf **Postfachfunktionen**.</span><span class="sxs-lookup"><span data-stu-id="fa11a-191">On the **User Mailbox** page, click **Mailbox features**.</span></span>
    
4. <span data-ttu-id="fa11a-192">Wählen Sie unter **Aufbewahrungsrichtlinie** die Aufbewahrungsrichtlinie aus, die Sie in Schritt 2 erstellt haben, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="fa11a-192">Under **Retention policy**, select the retention policy that you created in Step 2, and then click **Save**.</span></span>
    
<span data-ttu-id="fa11a-193">Sie können auch die Exchange-Verwaltungskonsole verwenden, um die Aufbewahrungsrichtlinie auf mehrere Postfächer anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="fa11a-193">You can also use the EAC to apply the retention policy to multiple mailboxes.</span></span>
  
1. <span data-ttu-id="fa11a-194">Navigieren Sie zu **Empfänger** \> **Postfächer**.</span><span class="sxs-lookup"><span data-stu-id="fa11a-194">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="fa11a-195">Verwenden Sie in der Listenansicht die UMSCHALT- oder die STRG-TASTE, um mehrere Postfächer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="fa11a-195">In the list view, use the Shift or Ctrl keys to select multiple mailboxes.</span></span>
    
3. <span data-ttu-id="fa11a-196">Klicken Sie im Detailbereich auf **Weitere Optionen**.</span><span class="sxs-lookup"><span data-stu-id="fa11a-196">In the details pane, click **More options**.</span></span>
    
4. <span data-ttu-id="fa11a-197">Klicken Sie unter **Aufbewahrungsrichtlinie** auf **Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="fa11a-197">Under **Retention Policy**, click **Update**.</span></span>
    
5. <span data-ttu-id="fa11a-198">Wählen Sie auf der Seite**Massenzuweisung von Aufbewahrungsrichtlinie** die Aufbewahrungsrichtlinie aus, die Sie in Schritt 2 erstellt haben, und klicken Sie dann auf **Speichern**. </span><span class="sxs-lookup"><span data-stu-id="fa11a-198">On the **Bulk assign retention policy** page, select the retention policy that you created in Step 2, and then click **Save**.</span></span> 
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a><span data-ttu-id="fa11a-199">Verwenden von Exchange Online PowerShell zum Anwenden der neuen Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fa11a-199">Use Exchange Online PowerShell to apply the new retention policy</span></span>
  
<span data-ttu-id="fa11a-p114">Sie können Exchange Online PowerShell verwenden, um eine neue Aufbewahrungsrichtlinie auf ein einzelnes Postfach anzuwenden. Die wirkliche Leistungsfähigkeit von PowerShell besteht darin, dass Sie Sie verwenden können, um schnell alle Postfächer in Ihrer Organisation zu identifizieren, die in einem Rechtsstreit halten oder in der Lage sind, und dann die neue Aufbewahrungsrichtlinie auf alle Postfächer anwenden, die in einem einzigen Befehl aufbewahrt werden. Im folgenden finden Sie einige Beispiele für die Verwendung von Exchange PowerShell zum Anwenden einer Aufbewahrungsrichtlinie auf ein oder mehrere Postfächer. In allen Beispielen wird die in Schritt 2 erstellte Aufbewahrungsrichtlinie angewendet.</span><span class="sxs-lookup"><span data-stu-id="fa11a-p114">You can use Exchange Online PowerShell to apply a new retention policy to a single mailbox. But the real power of PowerShell is that you can use it to quickly identify all the mailboxes in your organization that are on either Litigation Hold or In-Place Hold, and then apply the new retention policy to all mailboxes on hold in a single command. Here are some examples of using Exchange PowerShell to apply a retention policy to one or more mailboxes. All of the examples apply the retention policy that was created in Step 2.</span></span>
  
<span data-ttu-id="fa11a-204">In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf das Postfach von Pilar Pinilla angewendet.</span><span class="sxs-lookup"><span data-stu-id="fa11a-204">This example applies the new retention policy to Pilar Pinilla's mailbox.</span></span>
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="fa11a-205">In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf alle Postfächer im Beweissicherungsverfahren angewendet.</span><span class="sxs-lookup"><span data-stu-id="fa11a-205">This example applies the new retention policy to all mailboxes in the organization that are on Litigation Hold.</span></span>
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="fa11a-206">In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf alle Postfächer in der Organisation angewendet, die sich im In-Situ-Speicher befinden.</span><span class="sxs-lookup"><span data-stu-id="fa11a-206">This example applies the new retention policy to all mailboxes in the organization that are on In-Place Hold.</span></span>
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="fa11a-207">Sie können das Cmdlet **Get-Mailbox** verwenden, um zu überprüfen, dass die neue Aufbewahrungsrichtlinie angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fa11a-207">You can use the **Get-Mailbox** cmdlet to verify that the new retention policy was applied.</span></span> 
  
<span data-ttu-id="fa11a-208">Nachfolgend finden Sie einige Beispiele, mit denen Sie überprüfen können, dass über die Befehle in den vorherigen Beispielen die Aufbewahrungsrichtlinie „MRM-Richtlinie für Postfächer im In-Situ-Speicher“ auf Postfächer im Beweissicherungsverfahren und auf Postfächer im In-Situ-Speicher angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="fa11a-208">Here are some examples to verify that the commands in the previous examples applied the "MRM Policy for Mailboxes on Hold" retention policy to mailboxes on Litigation Hold and mailboxes on In-Place Hold.</span></span>
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a><span data-ttu-id="fa11a-209">(Optional) Schritt 4: Ausführen des Assistenten für verwaltete Ordner zum Anwenden der neuen Aufbewahrungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="fa11a-209">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>

<span data-ttu-id="fa11a-p115">Nachdem Sie die neue Aufbewahrungsrichtlinie auf Postfächer angewendet haben, kann es bis zu 7 Tage dauern, bis der Assistent für verwaltete Ordner diese Postfächer mithilfe der Einstellungen in der neuen Aufbewahrungsrichtlinie verarbeitet. Anstatt auf die Ausführung des Assistenten für verwaltete Ordner zu warten, können Sie das Cmdlet **Start-ManagedFolderAssistant** verwenden, um den Assistenten manuell auszulösen, um die Postfächer zu verarbeiten, auf die Sie die neue Aufbewahrungsrichtlinie angewendet haben.</span><span class="sxs-lookup"><span data-stu-id="fa11a-p115">After you apply the new retention policy to mailboxes on hold, it can take up to 7 days in Exchange Online for the Managed Folder Assistant to process these mailboxes using the settings in the new retention policy. Instead of waiting for the Managed Folder Assistant to run, you can use the **Start-ManagedFolderAssistant** cmdlet to manually trigger the assistant to process the mailboxes that you applied the new retention policy to.</span></span> 
  
<span data-ttu-id="fa11a-212">Führen Sie den folgenden Befehl aus, um den Assistenten für verwaltete Ordner für das Postfach von Pilar Pinilla zu starten.</span><span class="sxs-lookup"><span data-stu-id="fa11a-212">Run the following command to start the Managed Folder Assistant for Pilar Pinilla's mailbox.</span></span>
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

<span data-ttu-id="fa11a-213">Führen Sie die folgenden Befehle aus, um den Assistenten für verwaltete Ordner für alle aufzubewahrenden Postfächer zu starten:</span><span class="sxs-lookup"><span data-stu-id="fa11a-213">Run the following commands to start the Managed Folder Assistant for all mailboxes on hold.</span></span>
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a><span data-ttu-id="fa11a-214">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fa11a-214">More information</span></span>

- <span data-ttu-id="fa11a-p116">Nachdem Sie das Archivpostfach eines Benutzers aktiviert haben, sollten Sie dem Benutzer mitteilen, dass andere Elemente in Ihrem Postfach (nicht nur Elemente im Ordner "Wiederherstellbare Elemente") möglicherweise in das Archivpostfach verschoben werden. Der Grund ist, dass die standardmäßige MRM-Richtlinie, die Exchange Online-Postfächern zugewiesen ist, ein Aufbewahrungs (Standard 2 Jahre in Archiv verschieben) enthält, das zwei Jahre nach dem Datum, an dem das Element an das Postfach zugestellt oder vom Benutzer. Weitere Informationen finden Sie unter [standardmäßige Aufbewahrungsrichtlinie in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span><span class="sxs-lookup"><span data-stu-id="fa11a-p116">After you enable a user's archive mailbox, consider telling the user that other items in their mailbox (not just items in the Recoverable Items folder) might be moved to the archive mailbox. This is because the Default MRM Policy that's assigned to Exchange Online mailboxes contains a retention tag (named Default 2 years move to archive) that moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see [Default Retention Policy in Exchange Online ](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span></span>
    
- <span data-ttu-id="fa11a-p117">Nachdem Sie das Archivpostfach eines Benutzers aktiviert haben, können Sie auch dem Benutzer mitteilen, dass er gelöschte Elemente im Ordner "Wiederherstellbare Elemente" im Archivpostfach zurücksetzen kann. Sie können dies in Outlook tun, indem Sie den Ordner " **Gelöschte Elemente** " im Archivpostfach auswählen und dann auf der Registerkarte **Start** auf **Gelöschte Elemente vom Server wiederherstellen** klicken. Weitere Informationen zum Wiederherstellen gelöschter Elemente finden Sie unter [Recover Deleted Items in Outlook for Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span><span class="sxs-lookup"><span data-stu-id="fa11a-p117">After you enable a user's archive mailbox, you might also tell the user that they can recover deleted items in the Recoverable Items folder in their archive mailbox. They can do this in Outlook by selecting the **Deleted Items** folder in the archive mailbox, and then clicking **Recover Deleted Items from Server** on the **Home** tab. For more information about recovering deleted items, see [Recover deleted items in Outlook for Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span></span> 
