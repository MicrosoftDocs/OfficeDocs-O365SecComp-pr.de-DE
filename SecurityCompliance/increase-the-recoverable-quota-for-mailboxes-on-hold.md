---
title: Erhöhen des Kontingents für wiederherstellbare Elemente für im In-Situ-Speicher befindliche Postfächer
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/22/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: 'Aktivieren Sie das Archivpostfach, und schalten Sie automatisch erweitert, um die Größe des Ordners "wiederherstellbare Elemente" für ein Postfach in Office 365 erhöhen Archivierung. '
ms.openlocfilehash: 2e7149ef10152a11dc638c04b61a261440b539b8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528976"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a><span data-ttu-id="34b10-103">Erhöhen des Kontingents für wiederherstellbare Elemente für im In-Situ-Speicher befindliche Postfächer</span><span class="sxs-lookup"><span data-stu-id="34b10-103">Increase the Recoverable Items quota for mailboxes on hold</span></span>

<span data-ttu-id="34b10-p101">Standardaufbewahrungsrichtlinie – mit dem Namen MRM-Standardrichtlinie – d. h. automatisch angewendet auf neue Postfächer in Exchange Online enthält ein aufbewahrungstag benannten wiederherstellbare Elemente, 14 Tage in Archiv verschieben. In diesem aufbewahrungstag Verschiebt Elemente aus dem Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner "wiederherstellbare Elemente" im Archivpostfach des Benutzers nach Ablauf die Aufbewahrungszeit 14 Tagen für ein Element. Für dazu muss Archivpostfach des Benutzers aktiviert sein. Wenn das Archivpostfach nicht aktiviert ist, wird keine Aktion ausgeführt, was bedeutet, dass Elemente im Ordner für ein Postfach auf halten wiederherstellbaren Elementen in das Archivpostfach verschoben werden nicht nach Ablauf die Aufbewahrungszeit 14 Tagen. Da nichts aus einem Postfach in der Warteschleife gelöscht wird, ist es möglich, dass das Speicherkontingent für den Ordner wiederherstellbare Elemente überschritten werden kann, insbesondere dann, wenn das Postfach des Benutzers Archiv nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="34b10-p101">The default retention policy—named Default MRM Policy—that is automatically applied to new mailboxes in Exchange Online contains a retention tag named Recoverable Items 14 days move to archive. This retention tag moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox after the 14-day retention period expires for an item. For this to happen, the user's archive mailbox must be enabled. If the archive mailbox isn't enabled, no action is taken, which means that items in the Recoverable Items folder for a mailbox on hold aren't moved to the archive mailbox after the 14-day retention period expires. Because nothing is deleted from a mailbox on hold, it's possible that the storage quota for the Recoverable Items folder might be exceeded, especially if the user's archive mailbox isn't enabled.</span></span> 
  
<span data-ttu-id="34b10-p102">Um das Risiko Überschreitung dieses Grenzwerts reduzieren, ist das Speicherkontingent für den Ordner wiederherstellbare Elemente automatisch Erhöhung von 30 GB auf 100 GB bei ein Haltestatus für ein Postfach im Exchange Online platziert wird. Wenn das Archivpostfach aktiviert ist, wird das Speicherkontingent für den Ordner "wiederherstellbare Elemente" im Archivpostfach auch von 30 GB auf 100 GB erhöht. Wenn feature erweiterbares Archivierung in Exchange Online ist aktiviert, das Speicherkontingent für den Ordner "wiederherstellbare Elemente" in das benutzerarchiv unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="34b10-p102">To help reduce the chance of exceeding this limit, the storage quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when a hold is placed on a mailbox in Exchange Online. If the archive mailbox is enabled, the storage quota for the Recoverable Items folder in the archive mailbox is also increased from 30 GB to 100 GB. If the auto-expanding archiving feature in Exchange Online is enabled, the storage quota for the Recoverable Items folder in the user's archive will be unlimited.</span></span>
  
 <span data-ttu-id="34b10-112"> In der folgenden Tabelle sind die Speicherkontingente für den Ordner „Wiederherstellbare Elemente“ zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="34b10-112">The following table summarizes the storage quota for the Recoverable Items folder.</span></span> 
  
|<span data-ttu-id="34b10-113">**Speicherort des Ordners „Wiederherstellbare Elemente“**</span><span class="sxs-lookup"><span data-stu-id="34b10-113">**Location of Recoverable Items folder**</span></span>|<span data-ttu-id="34b10-114">**Nicht aufzubewahrende Postfächer**</span><span class="sxs-lookup"><span data-stu-id="34b10-114">**Mailboxes not on hold**</span></span>|<span data-ttu-id="34b10-115">**Aufzubewahrende Postfächer**</span><span class="sxs-lookup"><span data-stu-id="34b10-115">**Mailboxes on hold**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="34b10-116">Primäres Postfach</span><span class="sxs-lookup"><span data-stu-id="34b10-116">Primary mailbox</span></span>  <br/> |<span data-ttu-id="34b10-117">30 GB</span><span class="sxs-lookup"><span data-stu-id="34b10-117">30 GB</span></span>  <br/> |<span data-ttu-id="34b10-118">100 GB</span><span class="sxs-lookup"><span data-stu-id="34b10-118">100 GB</span></span>  <br/> |
|<span data-ttu-id="34b10-119">Archivpostfach<sup>\*</sup></span><span class="sxs-lookup"><span data-stu-id="34b10-119">Archive mailbox<sup>\*</sup></span></span> <br/> |<span data-ttu-id="34b10-120">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="34b10-120">Unlimited</span></span>  <br/> |<span data-ttu-id="34b10-121">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="34b10-121">Unlimited</span></span>  <br/> |
|<span data-ttu-id="34b10-122">**Gesamtspeicherkontingent für den Ordner „Wiederherstellbare Elemente“**</span><span class="sxs-lookup"><span data-stu-id="34b10-122">**Total storage quota for the Recoverable Items folder**</span></span> <br/> |<span data-ttu-id="34b10-123">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="34b10-123">Unlimited</span></span>  <br/> |<span data-ttu-id="34b10-124">Unbegrenzt</span><span class="sxs-lookup"><span data-stu-id="34b10-124">Unlimited</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="34b10-p103"><sup>\*</sup>Das ursprüngliche Speicherkontingent für das Archivpostfach beträgt 100 GB für Benutzer mit einer Lizenz für Exchange Online (Plan 2). Wenn die Archivierung erweiterbares aktiviert ist, ist das Speicherkontingent für die benutzerarchiv und des Ordners "wiederherstellbare Elemente" in das Archiv unbegrenzt. Weitere Informationen zum Erweitern von automatischen Archivierung, finden Sie unter [Übersicht über die uneingeschränkte Archivierung in Office 365](unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="34b10-p103"><sup>\*</sup> The initial storage quota for the archive mailbox is 100 GB for users with an Exchange Online (Plan 2) license. However, when auto-expanding archiving is turned on, the storage quota for the user's archive and the Recoverable Items folder in the archive is unlimited. For more information about auto-expanding archiving, see [Overview of unlimited archiving in Office 365](unlimited-archiving.md).</span></span> 
  
<span data-ttu-id="34b10-128">Wenn das Speicherkontingent für den Ordner „Wiederherstellbare Elemente“ im primären Postfach eines aufzubewahrenden Postfachs seinen Grenzwert bald erreicht, können Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="34b10-128">When the storage quota for the Recoverable Items folder in the primary mailbox of a mailbox on hold is close to reaching its limit, you can do the following things:</span></span>
  
- <span data-ttu-id="34b10-p104">**Aktivieren Sie das Archivpostfach und Aktivieren von erweiterbares Archivierung** – können Sie einen unbegrenzte Speicherkapazität für "wiederherstellbare Elemente" einfach durch das Archivpostfach aktivieren und dann das automatisch erweitert, Archivierung Feature in Exchange Online. Dies führt 100 GB für den Ordner "wiederherstellbare Elemente" in das primäre Postfach und eine unbegrenzte Zeitspanne Speicherkapazität für den Ordner wiederherstellbare Elemente im Archiv des Benutzers. Finden Sie unter wie: [Aktivieren von archivpostfächern in die Office 365-Sicherheit &amp; Compliance Center](enable-archive-mailboxes.md) und [unbegrenzte Archivierung in Office 365 zu aktivieren](enable-unlimited-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="34b10-p104">**Enable the archive mailbox and turn on auto-expanding archiving** - You can enable an unlimited storage capacity for the Recoverable Items folder simply by enabling the archive mailbox and then turning on the auto-expanding archiving feature in Exchange Online. This results in 100 GB for the Recoverable Items folder in the primary mailbox and an unlimited amount of storage capacity for the Recoverable Items folder in the user's archive. See how: [Enable archive mailboxes in the Office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) and [Enable unlimited archiving in Office 365](enable-unlimited-archiving.md).</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="34b10-p105">Nachdem Sie das Archiv für ein Postfach aktiviert haben, die fast für "wiederherstellbare Elemente" das Speicherkontingent überschritten ist, Sie möglicherweise ausführen möchten, der Assistent für verwaltete Ordner manuell Auslösen der Assistent, um das Postfach verarbeitet werden, damit abgelaufene Elemente verschoben werden, um die Ordner wiederherstellbare Elemente im Archivpostfach. Weitere Informationen finden Sie in [Schritt 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) . Beachten Sie, dass andere Elemente im Postfach des Benutzers in das neue Archivpostfach verschoben werden können. Berücksichtigen Sie den Anwender darüber, dass dies geschehen kann, nachdem Sie das Archivpostfach aktivieren.</span><span class="sxs-lookup"><span data-stu-id="34b10-p105">After you enable the archive for a mailbox that's close to exceeding the storage quota for the Recoverable Items folder, you might want to run the Managed Folder Assistant to manually trigger the assistant to process the mailbox so that expired items are moved the Recoverable Items folder in the archive mailbox. See [Step 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) for instructions. Note that other items in the user's mailbox might be moved to the new archive mailbox. Consider telling the user that this may happen after you enable the archive mailbox.</span></span> 
  
- <span data-ttu-id="34b10-p106">**Erstellen eine benutzerdefinierten Aufbewahrungsrichtlinie für Postfächer auf halten** - zusätzlich zu aktivieren das Archivpostfach und erweiterbares Archivierung für Postfächer Beweissicherungsverfahren oder Compliance-Archiv, auch sollten Sie zum Erstellen einer benutzerdefinierten Aufbewahrungsrichtlinie für Postfächer auf halten. Dies wenden wir Sie eine Aufbewahrungsrichtlinie auf Postfächer in der Warteschleife, die von der MRM-Standardrichtlinie abweicht, die auf Postfächer angewendet wird, die nicht in der Warteschleife sind. Auf diese Weise können Sie um aufbewahrungstags anzuwenden, die speziell für Postfächer in der Warteschleife entwickelt wurden. Dazu gehört das Erstellen eines neuen aufbewahrungstags für "wiederherstellbare Elemente".</span><span class="sxs-lookup"><span data-stu-id="34b10-p106">**Create a custom retention policy for mailboxes on hold** - In addition to enabling the archive mailbox and auto-expanding archiving for mailboxes on Litigation Hold or In-Place Hold, you might also want to create a custom retention policy for mailboxes on hold. This let's you apply a retention policy to mailboxes on hold that's different from the Default MRM Policy that's applied to mailboxes that aren't on hold. This lets you to apply retention tags that are specifically designed for mailboxes on hold. This includes creating a new retention tag for the Recoverable Items folder.</span></span> 
    
<span data-ttu-id="34b10-140">Im restlichen Thema werden die schrittweisen Anweisungen zum Erstellen einer benutzerdefinierten Aufbewahrungsrichtlinie für aufzubewahrende Postfächer erläutert.</span><span class="sxs-lookup"><span data-stu-id="34b10-140">The remainder of this topic describes the step-by-step procedures to create a custom retention policy for mailboxes on hold.</span></span>
  
[<span data-ttu-id="34b10-141">Schritt 1: Erstellen eines benutzerdefinierten Aufbewahrungstags für den Ordner „Wiederherstellbare Elemente“</span><span class="sxs-lookup"><span data-stu-id="34b10-141">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

<span data-ttu-id="34b10-142">[[Schritt2: erstellen eine neuen Aufbewahrungsrichtlinie für Postfächer in der Warteschleife](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span><span class="sxs-lookup"><span data-stu-id="34b10-142">[[Step 2: Create a new retention policy for mailboxes on hold](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)</span></span>

[<span data-ttu-id="34b10-143">Schritt 3: Anwenden der neuen Aufbewahrungsrichtlinie auf aufzubewahrende Postfächer</span><span class="sxs-lookup"><span data-stu-id="34b10-143">Step 3: Apply the new retention policy to mailboxes on hold</span></span>](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[<span data-ttu-id="34b10-144">(Optional) Schritt 4: Ausführen des Assistenten für verwaltete Ordner zum Anwenden der neuen Aufbewahrungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="34b10-144">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a><span data-ttu-id="34b10-145">Schritt 1: Erstellen eines benutzerdefinierten Aufbewahrungstags für den Ordner „Wiederherstellbare Elemente“</span><span class="sxs-lookup"><span data-stu-id="34b10-145">Step 1: Create a custom retention tag for the Recoverable Items folder</span></span>

<span data-ttu-id="34b10-p107">Der erste Schritt ist zum Erstellen eines benutzerdefinierten aufbewahrungstags (Aufbewahrungsrichtlinien-Tag oder Berichtskopf genannt) für den Ordner "wiederherstellbare Elemente". Wie bereits erklärt verschiebt diese außer Elemente aus dem Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner "wiederherstellbare Elemente" im Archivpostfach des Benutzers. Sie müssen PowerShell verwenden, um ein Aufbewahrungsrichtlinientag für "wiederherstellbare Elemente" zu erstellen. Sie können nicht im Exchange Administrationscenter (EAC) verwenden.</span><span class="sxs-lookup"><span data-stu-id="34b10-p107">The first step is to create a custom retention tag (called a retention policy tag or RPT) for the Recoverable Items folder. As previously explained, this RPT moves items from the Recoverable Items folder in the user's primary mailbox to the Recoverable Items folder in the user's archive mailbox. You have to use PowerShell to create an RPT for the Recoverable Items folder. You can't use the Exchange admin center (EAC).</span></span> 
  
1. [<span data-ttu-id="34b10-150">Connect to Exchange Online using remote PowerShell</span><span class="sxs-lookup"><span data-stu-id="34b10-150">Connect to Exchange Online using remote PowerShell</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. <span data-ttu-id="34b10-151">Führen Sie den folgenden Befehl zum Erstellen eines Aufbewahrungstags für den Ordner „Wiederherstellbare Elemente“ aus: </span><span class="sxs-lookup"><span data-stu-id="34b10-151">Run the following command to create a new RPT for the Recoverable Items folder:</span></span> 
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    <span data-ttu-id="34b10-p108">Durch den folgenden Befehl wird beispielsweise ein Aufbewahrungstag für den Ordner „Wiederherstellbare Elemente“ mit dem Namen „Wiederherstellbare Elemente, 30 Tage, für aufzubewahrende Postfächer“ mit einem Aufbewahrungszeitraum von 30 Tagen erstellt. Dies bedeutet, dass ein Element, nachdem es 30 Tage lang im Ordner „Wiederherstellbare Elemente“ gespeichert war, in den Ordner „Wiederherstellbare Elemente“ im Archivpostfach des Benutzers verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="34b10-p108">For example, the following command creates a RPT for the Recoverable Items folder named "Recoverable Items 30 days for mailboxes on hold", with a retention period of 30 days. This means that after an item has been in the Recoverable Items folder for 30 days, it will be moved to the Recoverable Items folder in the user's archive mailbox.</span></span>
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > <span data-ttu-id="34b10-p109">Es wird empfohlen, dass der Aufbewahrungszeitraum für die wiederherstellbare Elemente außer (definiert durch den Parameter _' AgeLimitForRetention '_ ) ist, als die Aufbewahrungszeit für Postfächer, die auf der Berichtskopf angewendet wird. Dadurch kann der Benutzer die gesamte Aufbewahrungszeit Wiederherstellen gelöschter Objekte, bevor sie in das Archivpostfach verschoben werden. Im vorherigen Beispiel wurde die Aufbewahrungsdauer auf 30 Tage basierend auf der Annahme, die die Aufbewahrungszeit für Postfächer auch 30 Tage ist festgelegt. Exchange Online-Postfachs ist für gelöschte Elemente 14 Tage lang aufbewahrt werden standardmäßig konfiguriert. Sie können jedoch ändern diese Einstellung auf ein Maximum von 30 Tagen. Weitere Informationen finden Sie unter [Ändern der Aufbewahrungszeit für ein Postfach im Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span><span class="sxs-lookup"><span data-stu-id="34b10-p109">We recommend that the retention period (defined by the  _AgeLimitForRetention_ parameter) for the Recoverable Items RPT is the same as the deleted item retention period for the mailboxes that the RPT will be applied to. This allows a user the entire deleted item retention period to recover deleted items before they are moved to the archive mailbox. In the previous example, the retention period was set to 30 days based on the assumption that the deleted item retention period for mailboxes is also 30 days. An Exchange Online mailbox is configured to retain deleted items for 14 days, by default. But you can change this setting to a maximum of 30 days. For more information, see [Change the deleted item retention period for a mailbox in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940).</span></span> 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a><span data-ttu-id="34b10-160">Schritt 2: Erstellen einer neuen Aufbewahrungsrichtlinie für aufzubewahrende Postfächer</span><span class="sxs-lookup"><span data-stu-id="34b10-160">Step 2: Create a new retention policy for mailboxes on hold</span></span>

<span data-ttu-id="34b10-p110">Der nächste Schritt besteht darin, eine neue Aufbewahrungsrichtlinie zu erstellen und dieser Aufbewahrungstags hinzuzufügen, einschließlich der Aufbewahrungstags für wiederherstellbare Elemente, die Sie in Schritt 1 erstellt haben. Diese neue Richtlinie wird im nächsten Schritt auf aufzubewahrende Postfächer angewendet. </span><span class="sxs-lookup"><span data-stu-id="34b10-p110">The next step is to create a new retention policy and add retention tags to it, including the Recoverable Items RPT that you created in Step 1. This new policy will be applied to mailboxes on hold in the next step.</span></span> 
  
<span data-ttu-id="34b10-p111">Bevor Sie die neue Aufbewahrungsrichtlinie erstellen, ermitteln Sie die zusätzlichen Aufbewahrungstags, die Sie hinzufügen möchten. Eine Liste der Aufbewahrungstags, die der Standard-MRM-Richtlinie hinzugefügt werden, sowie Informationen zum Erstellen neuer Aufbewahrungstags finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="34b10-p111">Before you create the new retention policy, determine the additional retention tags that you want to add. For a list of the retention tags that are added to the Default MRM Policy and for information about creating new retention tags, see the following:</span></span>
  
- [<span data-ttu-id="34b10-165">Default Aufbewahrungsrichtlinien in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="34b10-165">Default Retention Policy in Exchange Online </span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [<span data-ttu-id="34b10-166">Standardordner, die Aufbewahrungsrichtlinientags unterstützen</span><span class="sxs-lookup"><span data-stu-id="34b10-166">Default folders that support Retention Policy Tags</span></span>](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- <span data-ttu-id="34b10-167">Abschnitt "erstellen Sie ein aufbewahrungstag" im Thema [Create a Retention Policy](https://go.microsoft.com/fwlink/p/?LinkId=404422) .</span><span class="sxs-lookup"><span data-stu-id="34b10-167">The "Create a retention tag" section in the [Create a Retention Policy](https://go.microsoft.com/fwlink/p/?LinkId=404422) topic.</span></span>
    
<span data-ttu-id="34b10-168">Der Exchange-Verwaltungskonsole oder die Exchange Online PowerShell können Sie um eine Aufbewahrungsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34b10-168">You can use the EAC or Exchange Online PowerShell to create a retention policy.</span></span>
  
### <a name="use-the-eac-to-create-a-retention-policy"></a><span data-ttu-id="34b10-169">Erstellen einer Aufbewahrungsrichtlinie mithilfe der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="34b10-169">Use the EAC to create a retention policy</span></span>
  
1. <span data-ttu-id="34b10-170">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Verwaltung der Richtlinientreue** \> **Aufbewahrungsrichtlinien**, und klicken Sie dann auf **Hinzufügen** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="34b10-170">In the EAC, go to **Compliance management** \> **Retention policies**, and then click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
2. <span data-ttu-id="34b10-171">Geben Sie auf der Seite **Neue Aufbewahrungsrichtlinie** unter **Name** einen Namen ein, der den Zweck der Aufbewahrungsrichtlinie beschreibt, z. B. **MRM Policy for Mailboxes on Hold**. </span><span class="sxs-lookup"><span data-stu-id="34b10-171">On the **New retention policy** page, under **Name**, type a name that describes the purpose of the retention policy; for example, **MRM Policy for Mailboxes on Hold**.</span></span> 
    
3. <span data-ttu-id="34b10-172">Klicken Sie auf **Hinzufügen** , klicken Sie unter **Retention Tags**, ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="34b10-172">Under **Retention tags**, click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="34b10-173">Wählen Sie in der Liste mit Aufbewahrungstags das Aufbewahrungstag für wiederherstellbare Elemente aus, das Sie in Schritt 1 erstellt haben, und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="34b10-173">In the list of retention tags, select the Recoverable Items RPT that you created in Step 1, and then click **Add**.</span></span>
    
    ![Wählen Sie das benutzerdefinierte Aufbewahrungstag „Wiederherstellbare Elemente“ aus.](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. <span data-ttu-id="34b10-p112">Wählen Sie zusätzliche Aufbewahrungstags aus, die der Aufbewahrungsrichtlinie hinzugefügt werden sollen. Sie können beispielsweise dieselben Tags hinzufügen, die in der Standard-MRM-Richtlinie enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="34b10-p112">Select additional retention tags to add to the retention policy. For example, you might want to add the same tags that are included in the Default MRM Policy.</span></span>
    
6. <span data-ttu-id="34b10-177">Klicken Sie auf **OK**, wenn Sie mit dem Hinzufügen von Aufbewahrungstags fertig sind.</span><span class="sxs-lookup"><span data-stu-id="34b10-177">When you're finished adding retention tags, click **OK**.</span></span>
    
7. <span data-ttu-id="34b10-178">Klicken Sie auf **Speichern**, um die neue Aufbewahrungsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34b10-178">Click **Save** to create the new retention policy.</span></span> 
    
    <span data-ttu-id="34b10-179">Im Detailbereich werden Aufbewahrungstags verknüpft mit der Aufbewahrungsrichtlinie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="34b10-179">Notice that the retention tags linked to the retention policy are displayed in the details pane.</span></span>
    
    ![Im Detailbereich werden Aufbewahrungstags verknüpft mit der Aufbewahrungsrichtlinie angezeigt.](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a><span data-ttu-id="34b10-181">Verwenden Sie Exchange Online PowerShell, um eine Aufbewahrungsrichtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="34b10-181">Use Exchange Online PowerShell to create a retention policy</span></span>
  
<span data-ttu-id="34b10-182">Führen Sie zum Erstellen einer neuen Aufbewahrungsrichtlinie für aufzubewahrende Postfächer den folgenden Befehl aus: </span><span class="sxs-lookup"><span data-stu-id="34b10-182">Run the following command to create new retention policy for mailboxes on hold.</span></span> 
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

<span data-ttu-id="34b10-183">Durch den folgenden Befehl wird beispielsweise die Aufbewahrungsrichtlinie erstellt und mit Aufbewahrungstags verknüpft, die in der vorherigen Abbildung dargestellt sind.</span><span class="sxs-lookup"><span data-stu-id="34b10-183">For example, the following command creates the retention policy and linked retention tags that is displayed in the previous illustration.</span></span>
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a><span data-ttu-id="34b10-184">Schritt 3: Anwenden der neuen Aufbewahrungsrichtlinie auf aufzubewahrende Postfächer</span><span class="sxs-lookup"><span data-stu-id="34b10-184">Step 3: Apply the new retention policy to mailboxes on hold</span></span>

<span data-ttu-id="34b10-p113">Der letzte Schritt ist die neue Aufbewahrungsrichtlinie angewendet, die Sie in Schritt2 auf Postfächer in der Warteschleife in Ihrer Organisation erstellt. Der Exchange-Verwaltungskonsole oder die Exchange Online PowerShell können Sie die Aufbewahrungsrichtlinie auf ein einzelnes Postfach oder auf mehrere Postfächer anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="34b10-p113">The last step is to apply the new retention policy that you created in Step 2 to mailboxes on hold in your organization. You can use the EAC or Exchange Online PowerShell to apply the retention policy to a single mailbox or to multiple mailboxes.</span></span> 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a><span data-ttu-id="34b10-187">Anwenden der neuen Aufbewahrungsrichtlinie mithilfe der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="34b10-187">Use the EAC to apply the new retention policy</span></span>
  
1. <span data-ttu-id="34b10-188">Navigieren Sie zu **Empfänger** \> **Postfächer**.</span><span class="sxs-lookup"><span data-stu-id="34b10-188">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="34b10-189">In der Listenansicht, wählen Sie das Postfach, das Sie die Aufbewahrungsrichtlinie auf anwenden möchten, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span><span class="sxs-lookup"><span data-stu-id="34b10-189">In the list view, select the mailbox you want to apply the retention policy to, and then click **Edit** ![Edit icon](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).</span></span>
    
3. <span data-ttu-id="34b10-190">Klicken Sie auf der Seite **Benutzerpostfach** auf **Postfachfunktionen**.</span><span class="sxs-lookup"><span data-stu-id="34b10-190">On the **User Mailbox** page, click **Mailbox features**.</span></span>
    
4. <span data-ttu-id="34b10-191">Wählen Sie unter **Aufbewahrungsrichtlinie** die Aufbewahrungsrichtlinie aus, die Sie in Schritt 2 erstellt haben, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="34b10-191">Under **Retention policy**, select the retention policy that you created in Step 2, and then click **Save**.</span></span>
    
<span data-ttu-id="34b10-192">Sie können auch die Exchange-Verwaltungskonsole verwenden, um die Aufbewahrungsrichtlinie auf mehrere Postfächer anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="34b10-192">You can also use the EAC to apply the retention policy to multiple mailboxes.</span></span>
  
1. <span data-ttu-id="34b10-193">Navigieren Sie zu **Empfänger** \> **Postfächer**.</span><span class="sxs-lookup"><span data-stu-id="34b10-193">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="34b10-194">Verwenden Sie in der Listenansicht die UMSCHALT- oder die STRG-TASTE, um mehrere Postfächer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="34b10-194">In the list view, use the Shift or Ctrl keys to select multiple mailboxes.</span></span>
    
3. <span data-ttu-id="34b10-195">Klicken Sie im Detailbereich auf **Weitere Optionen**.</span><span class="sxs-lookup"><span data-stu-id="34b10-195">In the details pane, click **More options**.</span></span>
    
4. <span data-ttu-id="34b10-196">Klicken Sie unter **Aufbewahrungsrichtlinie** auf **Aktualisieren**.</span><span class="sxs-lookup"><span data-stu-id="34b10-196">Under **Retention Policy**, click **Update**.</span></span>
    
5. <span data-ttu-id="34b10-197">Wählen Sie auf der Seite**Massenzuweisung von Aufbewahrungsrichtlinie** die Aufbewahrungsrichtlinie aus, die Sie in Schritt 2 erstellt haben, und klicken Sie dann auf **Speichern**. </span><span class="sxs-lookup"><span data-stu-id="34b10-197">On the **Bulk assign retention policy** page, select the retention policy that you created in Step 2, and then click **Save**.</span></span> 
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a><span data-ttu-id="34b10-198">Verwenden Sie Exchange Online PowerShell, um die neue Aufbewahrungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="34b10-198">Use Exchange Online PowerShell to apply the new retention policy</span></span>
  
<span data-ttu-id="34b10-p114">Exchange Online PowerShell können Sie eine neue Aufbewahrungsrichtlinie auf ein einzelnes Postfach anwenden. Aber die wirkliche Stärke von PowerShell besteht darin, dass Sie schnell alle identifizieren, die die Postfächer in Ihrer Organisation, die entweder Beweissicherungsverfahren oder Compliance-Archiv, und wenden Sie die neue Aufbewahrungsrichtlinie auf alle Postfächer auf einem einzelnen Befehl enthalten können. Hier sind einige Beispiele für die Verwendung von Exchange PowerShell anwenden eine Aufbewahrungsrichtlinie auf eine oder mehrere Postfächer. Alle Beispiele gelten die Aufbewahrungsrichtlinie, die in Schritt2 erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="34b10-p114">You can use Exchange Online PowerShell to apply a new retention policy to a single mailbox. But the real power of PowerShell is that you can use it to quickly identify all the mailboxes in your organization that are on either Litigation Hold or In-Place Hold, and then apply the new retention policy to all mailboxes on hold in a single command. Here are some examples of using Exchange PowerShell to apply a retention policy to one or more mailboxes. All of the examples apply the retention policy that was created in Step 2.</span></span>
  
<span data-ttu-id="34b10-203">In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf das Postfach von Pilar Pinilla angewendet.</span><span class="sxs-lookup"><span data-stu-id="34b10-203">This example applies the new retention policy to Pilar Pinilla's mailbox.</span></span>
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="34b10-204">In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf alle Postfächer im Beweissicherungsverfahren angewendet.</span><span class="sxs-lookup"><span data-stu-id="34b10-204">This example applies the new retention policy to all mailboxes in the organization that are on Litigation Hold.</span></span>
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="34b10-205">In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf alle Postfächer in der Organisation angewendet, die sich im In-Situ-Speicher befinden.</span><span class="sxs-lookup"><span data-stu-id="34b10-205">This example applies the new retention policy to all mailboxes in the organization that are on In-Place Hold.</span></span>
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

<span data-ttu-id="34b10-206">Sie können das Cmdlet **Get-Mailbox** verwenden, um zu überprüfen, dass die neue Aufbewahrungsrichtlinie angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="34b10-206">You can use the **Get-Mailbox** cmdlet to verify that the new retention policy was applied.</span></span> 
  
<span data-ttu-id="34b10-207">Nachfolgend finden Sie einige Beispiele, mit denen Sie überprüfen können, dass über die Befehle in den vorherigen Beispielen die Aufbewahrungsrichtlinie „MRM-Richtlinie für Postfächer im In-Situ-Speicher“ auf Postfächer im Beweissicherungsverfahren und auf Postfächer im In-Situ-Speicher angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="34b10-207">Here are some examples to verify that the commands in the previous examples applied the "MRM Policy for Mailboxes on Hold" retention policy to mailboxes on Litigation Hold and mailboxes on In-Place Hold.</span></span>
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a><span data-ttu-id="34b10-208">(Optional) Schritt 4: Ausführen des Assistenten für verwaltete Ordner zum Anwenden der neuen Aufbewahrungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="34b10-208">(Optional) Step 4: Run the Managed Folder Assistant to apply the new retention settings</span></span>

<span data-ttu-id="34b10-p115">Nachdem Sie die neue Aufbewahrungsrichtlinie auf Postfächer in der Warteschleife anwenden, kann es bis zu sieben Tage in Exchange Online für den Assistenten für verwaltete Ordner diese Postfächer mithilfe der Einstellungen in die neue Aufbewahrungsrichtlinie verarbeitet dauern. Das Cmdlet **Start-ManagedFolderAssistant** können Sie anstelle der Assistent für verwaltete Ordner ausgeführt werden muss, manuell Auslösen der Assistent zum Verarbeiten der Postfächer, denen Sie auf die neue Aufbewahrungsrichtlinie angewendet.</span><span class="sxs-lookup"><span data-stu-id="34b10-p115">After you apply the new retention policy to mailboxes on hold, it can take up to 7 days in Exchange Online for the Managed Folder Assistant to process these mailboxes using the settings in the new retention policy. Instead of waiting for the Managed Folder Assistant to run, you can use the **Start-ManagedFolderAssistant** cmdlet to manually trigger the assistant to process the mailboxes that you applied the new retention policy to.</span></span> 
  
<span data-ttu-id="34b10-211">Führen Sie den folgenden Befehl aus, um den Assistenten für verwaltete Ordner für das Postfach von Pilar Pinilla zu starten.</span><span class="sxs-lookup"><span data-stu-id="34b10-211">Run the following command to start the Managed Folder Assistant for Pilar Pinilla's mailbox.</span></span>
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

<span data-ttu-id="34b10-212">Führen Sie die folgenden Befehle aus, um den Assistenten für verwaltete Ordner für alle aufzubewahrenden Postfächer zu starten:</span><span class="sxs-lookup"><span data-stu-id="34b10-212">Run the following commands to start the Managed Folder Assistant for all mailboxes on hold.</span></span>
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a><span data-ttu-id="34b10-213">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="34b10-213">More information</span></span>

- <span data-ttu-id="34b10-p116">Nachdem Sie Archivpostfach des Benutzers aktiviert haben, sollten Sie den Anwender darüber, dass andere Elemente in ihrem Postfach (nicht nur Elemente im Ordner "wiederherstellbare Elemente") in das Archivpostfach verschoben werden können. Dies ist, da der MRM-Standardrichtlinie, die Exchange Online-Postfächern zugewiesen ist, ein aufbewahrungstag (benannte Standard 2 Jahre, in Archiv verschieben), die Elemente in das Archivpostfach zwei Jahre nach dem Datum verschiebt das Element an das Postfach übermittelt wurde oder enthält von erstellt die Benutzer. Weitere Informationen finden Sie unter [Default Retention Policy in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span><span class="sxs-lookup"><span data-stu-id="34b10-p116">After you enable a user's archive mailbox, consider telling the user that other items in their mailbox (not just items in the Recoverable Items folder) might be moved to the archive mailbox. This is because the Default MRM Policy that's assigned to Exchange Online mailboxes contains a retention tag (named Default 2 years move to archive) that moves items to the archive mailbox two years after the date the item was delivered to the mailbox or created by the user. For more information, see [Default Retention Policy in Exchange Online ](https://go.microsoft.com/fwlink/p/?LinkId=746954)</span></span>
    
- <span data-ttu-id="34b10-p117">Nachdem Sie Archivpostfach des Benutzers aktiviert haben, erfahren Sie möglicherweise auch, dass der Benutzer, den sie wiederherstellen können, Elemente im Ordner "wiederherstellbare Elemente" in ihrem Archivpostfach gelöscht. Sie können in Outlook dazu auswählen den Ordner **Gelöschte Elemente** in das Archivpostfach, und klicken auf der Registerkarte **Start** **Vom Server gelöschte Elemente wiederherstellen** . Weitere Informationen zum Wiederherstellen von gelöschten Elementen finden Sie unter [Gelöschte Elemente in Outlook für Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span><span class="sxs-lookup"><span data-stu-id="34b10-p117">After you enable a user's archive mailbox, you might also tell the user that they can recover deleted items in the Recoverable Items folder in their archive mailbox. They can do this in Outlook by selecting the **Deleted Items** folder in the archive mailbox, and then clicking **Recover Deleted Items from Server** on the **Home** tab. For more information about recovering deleted items, see [Recover deleted items in Outlook for Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829).</span></span> 
