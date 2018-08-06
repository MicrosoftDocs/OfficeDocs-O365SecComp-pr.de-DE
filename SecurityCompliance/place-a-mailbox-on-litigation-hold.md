---
title: Aktivieren des Beweissicherungsverfahrens für ein Postfach
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Durch die Aktivierung des Beweissicherungsverfahrens für ein Postfach werden auch alle Postfachinhalte aufbewahrt, einschließlich gelöschter Elemente und Originalversionen geänderter Elemente. '
ms.openlocfilehash: 8f440f5fc0bc7dafd639bdf8136808aa2f3bd35f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026442"
---
# <a name="place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="676c9-103">Aktivieren des Beweissicherungsverfahrens für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="676c9-103">Place a mailbox on Litigation Hold</span></span>
 
<span data-ttu-id="676c9-p101">Durch die Aktivierung des Beweissicherungsverfahrens für ein Postfach werden auch alle Postfachinhalte aufbewahrt, einschließlich gelöschter Elemente und Originalversionen geänderter Elemente. Wenn Sie für das Postfach eines Benutzers das Beweissicherungsverfahren aktivieren, wird auch der Inhalt im Archivpostfach archiviert, wenn dieses aktiviert ist. Gelöschte und geänderte Elemente werden eine bestimmte Zeit lang aufbewahrt oder bis Sie das Beweissicherungsverfahren für das Postfach deaktivieren. Alle diese Postfachelemente werden bei einer [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx)-Suche zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="676c9-p101">Place a mailbox on Litigation Hold to preserve all mailbox content, including deleted items and original versions of modified items. When you place a user' mailbox on Litigation Hold, content in the user's archive mailbox (if it's enabled) is also placed on hold. Deleted and modified items are preserved for a specified period, or until you remove the mailbox from Litigation Hold. All such mailbox items are returned in an [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx) search.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="676c9-p102">Aufbewahrung für eventuelle Rechtsstreitigkeiten behält Elemente im Ordner "wiederherstellbare Elemente" im Postfach des Benutzers. Je nach Anzahl und Größe der Elemente gelöscht oder geändert erhöhen Sie die Größe des Ordners "wiederherstellbare Elemente" des Postfachs schnell. Ordner "wiederherstellbare Elemente" ist standardmäßig mit einer hohen Vorgabe konfiguriert. In Exchange Online wird dieses Kontingent automatisch erhöht, wenn Sie ein Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten platzieren. Server 2013 in Exchange wird empfohlen, dass Sie Postfächer überwachen, die in die Aufbewahrung für eventuelle Rechtsstreitigkeiten wöchentlich, stellen Sie sicher, dass sie die Grenzwerte für die Kontingente wiederherstellbare Elemente erreicht nicht platziert werden.</span><span class="sxs-lookup"><span data-stu-id="676c9-p102">Litigation Hold preserves items in the Recoverable Items folder in the user's mailbox. Depending on number and size of items deleted or modified, the size of the Recoverable Items folder of the mailbox may increase quickly. The Recoverable Items folder is configured with a high quota by default. In Exchange Online, this quota is automatically increased when you place a mailbox on Litigation Hold. In Exchange Server 2013, we recommend that you monitor mailboxes that are placed on Litigation Hold on a weekly basis to ensure they don't reach the limits of the Recoverable Items quotas.</span></span> 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="676c9-113">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="676c9-113">What do you need to know before you begin?</span></span>
<span data-ttu-id="676c9-114"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="676c9-114"></span></span>

- <span data-ttu-id="676c9-115">Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="676c9-115">Estimated time to complete: 5 minutes</span></span>
    
- <span data-ttu-id="676c9-116">Es dauert bis zu 60 Minuten, bis die Einstellung für das Beweissicherungsverfahren in Kraft tritt.</span><span class="sxs-lookup"><span data-stu-id="676c9-116">The Litigation Hold setting may take up to 60 minutes to take effect.</span></span>
    
- <span data-ttu-id="676c9-p103">Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter „In-Situ-Archiv" im Thema [Berechtigungen für Messagingrichtlinien und -kompatibilität](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx).</span><span class="sxs-lookup"><span data-stu-id="676c9-p103">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "In-Place Hold" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic.</span></span> 
    
- <span data-ttu-id="676c9-p104">Um ein Exchange Online-Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten zu platzieren, müssen sie eine Lizenz Exchange Online (Plan 2) zugewiesen werden. Wenn ein Postfach mit eine Exchange Online (Plan 1)-Lizenz zugewiesen ist, müssten Sie weisen Sie ihr eine separate Lizenz der Exchange Online-Archivierung auf platziert halten.</span><span class="sxs-lookup"><span data-stu-id="676c9-p104">To place an Exchange Online mailbox on Litigation Hold, it must be assigned an Exchange Online (Plan 2) license. If a mailbox is assigned an Exchange Online (Plan 1) license, you would have to assign it a separate Exchange Online Archiving license to place it on hold.</span></span>
    
- <span data-ttu-id="676c9-p105">Wenn Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten für ein Benutzerpostfach einleiten, wird wie bereits erklärt auch Inhalt im Archivpostfach des Benutzers in der Warteschleife platziert. Wenn Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten für eine lokale primären Postfach in einer Exchange-hybridbereitstellung setzen, wird das Cloud-basierten Archivpostfach (sofern aktiviert) auch in der Warteschleife platziert.</span><span class="sxs-lookup"><span data-stu-id="676c9-p105">As previously explained, when you place a Litigation Hold on a user's mailbox, content in the user's archive mailbox is also placed on hold. If you place a Litigation Hold on an on-premises primary mailbox in an Exchange hybrid deployment, the cloud-based archive mailbox (if enabled) is also placed on hold.</span></span>
    
- <span data-ttu-id="676c9-p106">In Exchange Online wird das Kontingent für "wiederherstellbare Elemente" auf 100 GB automatisch erhöht, wenn Sie ein Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten platzieren. Die Standardgröße dieses Ordners ist 30 GB.</span><span class="sxs-lookup"><span data-stu-id="676c9-p106">In Exchange Online, the quota for the Recoverable Items folder is automatically increased to 100 GB when you place a mailbox on Litigation Hold. The default size of this folder is 30 GB.</span></span>
    
- <span data-ttu-id="676c9-p107">Aufbewahrung für eventuelle Rechtsstreitigkeiten behält gelöschte Elemente und behält auch ursprüngliche Versionen geänderter Objekte, bis die Sperre entfernt wurde. Sie können optional eine Dauer halten angeben, die ein Postfach-Element für die angegebene Dauer Periode behält. Wenn Sie einen Haltestatus Dauer angeben, wird ab dem Datum berechnet eine Nachricht empfangen oder ein Postfach-Element erstellt wird. Verwenden Sie Elemente, die den angegebenen Kriterien übereinstimmen, eine In-Place Hold zum Erstellen eines Haltestatus abfragebasierter. Weitere Informationen hierzu finden Sie unter [Erstellen oder Entfernen einer In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span><span class="sxs-lookup"><span data-stu-id="676c9-p107">Litigation Hold preserves deleted items and also preserves original versions of modified items until the hold is removed. You can optionally specify a hold duration, which preserves a mailbox item for the specified duration period. If you specify a hold duration period, it's calculated from the date a message is received or a mailbox item is created. To preserve items that meet your specified criteria, use an In-Place Hold to create a query-based hold. For details, see [Create or Remove an In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).</span></span>
    
- <span data-ttu-id="676c9-p108">Wenn Sie die Shell verwenden um ein Exchange Online-Postfachs in die Warteschleife zu stellen, müssen Sie Exchange Online PowerShell verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span><span class="sxs-lookup"><span data-stu-id="676c9-p108">To use the Shell to place an Exchange Online mailbox on hold, you have to use Exchange Online PowerShell. For more information, see [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).</span></span>
    
- <span data-ttu-id="676c9-p109">Das Festlegen eines Beweissicherungsverfahrens für ein Postfach für öffentliche Ordner wird nicht unterstützt. Sie müssen einen In-Situ-Speicher verwenden, um eine Speicherung für öffentliche Ordner festzulegen.</span><span class="sxs-lookup"><span data-stu-id="676c9-p109">Placing a Litigation Hold on a public folder mailbox isn't supported. You have to use In-Place Hold to place a hold on public folders.</span></span>
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a><span data-ttu-id="676c9-134">Verwenden von EAC zum Aktivieren des Beweissicherungsverfahrens für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="676c9-134">Use the EAC to place a mailbox on Litigation Hold</span></span>
<span data-ttu-id="676c9-135"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="676c9-135"></span></span>

1. <span data-ttu-id="676c9-136">Navigieren Sie zu **Empfänger** \> **Postfächer**.</span><span class="sxs-lookup"><span data-stu-id="676c9-136">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="676c9-137">Klicken Sie in der Liste der Benutzerpostfächer auf das Postfach, für das Sie die Beweissicherungsverfahren aktivieren möchten, und klicken Sie dann auf **Bearbeiten**![Bearbeitungssymbol](media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="676c9-137">In the list of user mailboxes, click the mailbox that you want to place on Litigation Hold, and then click **Edit**![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>
    
3. <span data-ttu-id="676c9-138">Klicken Sie auf der Eigenschaftenseite des Postfachs auf **Postfachfunktionen.**</span><span class="sxs-lookup"><span data-stu-id="676c9-138">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="676c9-139">Klicken Sie unter **Beweissicherungsverfahren: Deaktiviert** auf **Aktivieren**, um für das Postfach das Beweissicherungsverfahren zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="676c9-139">Under **Litigation hold: Disabled**, click **Enable** to place the mailbox on Litigation Hold.</span></span> 
    
5. <span data-ttu-id="676c9-140">Geben Sie auf der Seite **Beweissicherungsverfahren** die folgenden optionalen Informationen ein:</span><span class="sxs-lookup"><span data-stu-id="676c9-140">On the **Litigation Hold** page, enter the following optional information:</span></span> 
    
  - <span data-ttu-id="676c9-p110">**Dauer des Beweissicherungsverfahrens (Tage)** Verwenden Sie dieses Feld zum Angeben, wie lange Postfachelemente aufbewahrt werden, wenn für das Postfach das Beweissicherungsverfahren aktiviert wird. Der Zeitraum beginnt mit dem Datum, an dem das Postfachelement empfangen oder erstellt wurde. Wenn Sie dieses Feld leer lassen, werden Elemente unbegrenzt aufbewahrt oder bis die Aufbewahrung entfernt wird. Geben Sie die Dauer in Tagen an.</span><span class="sxs-lookup"><span data-stu-id="676c9-p110">**Litigation hold duration (days)** Use this box to specify how long mailbox items are held when the mailbox is placed on Litigation Hold. The duration is calculated from the date a mailbox item is received or created. If you leave this box blank, items are held indefinitely or until the hold is removed. Use days to specify the duration.</span></span> 
    
  - <span data-ttu-id="676c9-p111">**Hinweis** Können Sie in diesem Feld um den Benutzer zu informieren, die, den Ihr Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten ist. Die Notiz wird im Postfach des Benutzers angezeigt, wenn sie Outlook 2010 oder höher verwenden.</span><span class="sxs-lookup"><span data-stu-id="676c9-p111">**Note** Use this box to inform the user their mailbox is on Litigation Hold. The note will appear in the user's mailbox if they're using Outlook 2010 or later.</span></span> 
    
  - <span data-ttu-id="676c9-p112">**URL** Verwenden Sie dieses Feld, um den Benutzer zu einer Website Weitere Informationen zur Aufbewahrung für eventuelle Rechtsstreitigkeiten zu leiten. Diese URL wird im Postfach des Benutzers angezeigt, wenn sie Outlook 2010 oder höher verwenden.</span><span class="sxs-lookup"><span data-stu-id="676c9-p112">**URL** Use this box to direct the user to a website for more information about Litigation Hold. This URL appears in the user's mailbox if they are using Outlook 2010 or later.</span></span> 
    
6. <span data-ttu-id="676c9-149">Klicken Sie auf **Speichern** auf der Seite **Beweissicherungsverfahren**, und klicken Sie dann auf der Postfacheigenschaftsseite auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="676c9-149">Click **Save** on the **Litigation Hold** page, and then click **Save** on the mailbox properties page.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a><span data-ttu-id="676c9-150">Verwenden der Shell zum Aktivieren des unbegrenzten Beweissicherungsverfahrens für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="676c9-150">Use the Shell to place a mailbox on Litigation Hold indefinitely</span></span>
<span data-ttu-id="676c9-151"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="676c9-151"></span></span>

<span data-ttu-id="676c9-p113">In diesem Beispiel wird das Beweissicherungsverfahren für das Postfach "bsuneja@contoso.com" aktiviert. Elemente im Postfach werden unbegrenzt aufbewahrt oder bis die Aufbewahrung entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="676c9-p113">This example places the mailbox bsuneja@contoso.com on Litigation Hold. Items in the mailbox are held indefinitely or until the hold is removed.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> <span data-ttu-id="676c9-154">Wenn Sie für ein Postfach das unbegrenzte Beweissicherungsverfahren aktivieren (indem Sie keine Dauer angeben), wird der Wert für die  _LitigationHoldDuration_-Eigenschaft des Postfachs auf  `Unlimited` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="676c9-154">When you place a mailbox on Litigation Hold indefinitely (by not specifying a duration period), the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span> 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a><span data-ttu-id="676c9-155">Verwenden der Shell zum Aktivieren eines Postfachs für das Beweissicherungsverfahren und Beibehalten von Elementen für eine bestimmte Dauer</span><span class="sxs-lookup"><span data-stu-id="676c9-155">Use the Shell to place a mailbox on Litigation Hold and preserve items for a specified duration</span></span>
<span data-ttu-id="676c9-156"><a name="sectionSection3"> </a></span><span class="sxs-lookup"><span data-stu-id="676c9-156"></span></span>

<span data-ttu-id="676c9-157">In diesem Beispiel wird das Beweissicherungsverfahren für das Postfach "mailbox bsuneja@contoso.com" aktiviert, und Elemente werden für 2.555 Tage (etwa 7 Jahre) beibehalten.</span><span class="sxs-lookup"><span data-stu-id="676c9-157">This example places the mailbox bsuneja@contoso.com on Litigation Hold and preserves items for 2555 days (approximately 7 years).</span></span> 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a><span data-ttu-id="676c9-158">Verwenden der Shell zum Aktivieren des Beweissicherungsverfahrens für alle Postfächer für eine bestimmte Dauer</span><span class="sxs-lookup"><span data-stu-id="676c9-158">Use the Shell to place all mailboxes on Litigation Hold for a specified duration</span></span>
<span data-ttu-id="676c9-159"><a name="sectionSection4"> </a></span><span class="sxs-lookup"><span data-stu-id="676c9-159"></span></span>

<span data-ttu-id="676c9-p114">In Ihrer Organisation ist es möglicherweise erforderlich, dass alle Postfachdaten für einen bestimmten Zeitraum beibehalten werden. Bedenken Sie Folgendes, bevor Sie für alle Postfächer in einer Organisation das Beweissicherungsverfahren aktivieren:</span><span class="sxs-lookup"><span data-stu-id="676c9-p114">Your organization may require that all mailbox data be preserved for a specific period of time. Before you place all mailboxes in an organization on Litigation Hold, consider the following:</span></span>
  
<span data-ttu-id="676c9-162">In diesem Beispiel wird für alle Benutzerpostfächer in der Organisation für ein Jahr (365 Tage) das Beweissicherungsverfahren aktiviert.</span><span class="sxs-lookup"><span data-stu-id="676c9-162">This example places all user mailboxes in the organization on Litigation Hold for one year (365 days).</span></span>
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

<span data-ttu-id="676c9-163">Im Beispiel wird das Cmdlet [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) verwendet, um alle Postfächer in der Organisation abzurufen. Es wird ein Empfängerfilter angegeben, um alle Benutzerpostfächer einzubeziehen. Anschließend wird die Liste der Postfächer an das [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx)-Cmdlet umgeleitet, um das Beweissicherungsverfahren und die Aufbewahrungsdauer zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="676c9-163">The example uses the [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) cmdlet to retrieve all mailboxes in the organization, specifies a recipient filter to include all user mailboxes, and then pipes the list of mailboxes to the [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) cmdlet to enable the Litigation Hold and hold duration.</span></span> 
  
<span data-ttu-id="676c9-164">Führen Sie den vorherigen Befehl ohne den Parameter  _LitigationHoldDuration_ aus, um alle Benutzerpostfächer unbegrenzt aufzubewahren.</span><span class="sxs-lookup"><span data-stu-id="676c9-164">To place all user mailboxes on an indefinite hold, run the previous command but don't include the  _LitigationHoldDuration_ parameter.</span></span> 
  
<span data-ttu-id="676c9-165">Im Abschnitt [Weitere Informationen](#moreinfo.md) finden Sie Beispiele für die Verwendung von anderen Empfängereigenschaften in einem Filter zum Einbeziehen oder Ausschließen von mindestens einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="676c9-165">See the [More information](#moreinfo.md) section for examples of using other recipient properties in a filter to include or exclude one or more mailboxes.</span></span> 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a><span data-ttu-id="676c9-166">Verwenden der Shell zum Aufheben des Beweissicherungsverfahrens für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="676c9-166">Use the Shell to remove a mailbox from Litigation Hold</span></span>
<span data-ttu-id="676c9-167"><a name="sectionSection5"> </a></span><span class="sxs-lookup"><span data-stu-id="676c9-167"></span></span>

<span data-ttu-id="676c9-168">In diesem Beispiel wird das Beweissicherungsverfahren für das Postfach "bsuneja@contoso.com" aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="676c9-168">This example removes the mailbox bsuneja@contoso.com from Litigation Hold.</span></span>
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

<span data-ttu-id="676c9-169">P</span><span class="sxs-lookup"><span data-stu-id="676c9-169">P</span></span>
## <a name="how-do-you-know-this-worked"></a><span data-ttu-id="676c9-170">Woher wissen Sie, dass dieses Verfahren erfolgreich war?</span><span class="sxs-lookup"><span data-stu-id="676c9-170">How do you know this worked?</span></span>
<span data-ttu-id="676c9-171"><a name="sectionSection6"> </a></span><span class="sxs-lookup"><span data-stu-id="676c9-171"></span></span>

<span data-ttu-id="676c9-172">Führen Sie eine der folgenden Aktionen aus, um sicherzustellen, dass Sie das Beweissicherungsverfahren für ein Postfach erfolgreich aktiviert haben:</span><span class="sxs-lookup"><span data-stu-id="676c9-172">To verify that you have successfully placed a mailbox on Litigation Hold, do the one of the following:</span></span>
  
- <span data-ttu-id="676c9-173">In der Exchange-Verwaltungskonsole:</span><span class="sxs-lookup"><span data-stu-id="676c9-173">In the EAC:</span></span>
    
1. <span data-ttu-id="676c9-174">Navigieren Sie zu **Empfänger** \> **Postfächer**.</span><span class="sxs-lookup"><span data-stu-id="676c9-174">Go to **Recipients** \> **Mailboxes**.</span></span>
    
2. <span data-ttu-id="676c9-175">Klicken Sie in der Liste der Benutzerpostfächer auf das Postfach, dessen Einstellungen für das Beweissicherungsverfahren Sie überprüfen möchten, und klicken Sie dann auf **Bearbeiten**![Bearbeitungssymbol](media/ITPro-EAC-EditIcon.png).</span><span class="sxs-lookup"><span data-stu-id="676c9-175">In the list of user mailboxes, click the mailbox that you want to verify Litigation Hold settings for, and then click **Edit**![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>
    
3. <span data-ttu-id="676c9-176">Klicken Sie auf der Eigenschaftenseite des Postfachs auf **Postfachfunktionen.**</span><span class="sxs-lookup"><span data-stu-id="676c9-176">On the mailbox properties page, click **Mailbox features.**</span></span>
    
4. <span data-ttu-id="676c9-177">Stellen Sie unter **Beweissicherungsverfahren** sicher, dass die Aufbewahrung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="676c9-177">Under **Litigation hold**, verify that hold is enabled.</span></span>
    
5. <span data-ttu-id="676c9-p115">Klicken Sie auf **Details anzeigen**, um zu prüfen, wann und durch wen das Beweissicherungsverfahren für das Postfach aktiviert wurde. Sie können die Werte in den optionalen Feldern **Dauer des Beweissicherungsverfahrens (Tage)**, **Hinweis** und **URL** auch prüfen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="676c9-p115">Click **View details** to verify when the mailbox was placed on Litigation Hold and by whom. You can also verify or change the values in the optional **Litigation hold duration (days)**, **Note**, and **URL** boxes.</span></span> 
    
- <span data-ttu-id="676c9-180">Führen Sie in der Shell einen der folgenden Befehle aus:</span><span class="sxs-lookup"><span data-stu-id="676c9-180">In the Shell, run one of the following commands:</span></span>
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    <span data-ttu-id="676c9-181">oder</span><span class="sxs-lookup"><span data-stu-id="676c9-181">or</span></span>
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    <span data-ttu-id="676c9-182">Wenn das unbegrenzte Beweissicherungsverfahren für ein Postfach aktiviert ist, ist der Wert für die Eigenschaft  _LitigationHoldDuration_ des Postfachs auf  `Unlimited` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="676c9-182">If a mailbox is placed on Litigation Hold indefinitely, the value for the  _LitigationHoldDuration_ property mailbox is set to  `Unlimited`.</span></span>
    
## <a name="more-information"></a><span data-ttu-id="676c9-183">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="676c9-183">More information</span></span>
<span data-ttu-id="676c9-184"><a name="moreinfo"> </a></span><span class="sxs-lookup"><span data-stu-id="676c9-184"></span></span>

- <span data-ttu-id="676c9-185">Wenn Ihre Organisation verlangt, dass alle Postfachdaten für einen bestimmten Zeitraum beibehalten werden müssen, ziehen Sie Folgendes in Betracht, bevor Sie das Beweissicherungsverfahren für alle Postfächer in einer Organisation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="676c9-185">If your organization requires that all mailbox data has to preserved for a specific period of time, consider the following before you place all mailboxes in an organization on Litigation Hold.</span></span>
    
  - <span data-ttu-id="676c9-p116">Wenn Sie den vorherigen Befehl verwenden, um eine Aufbewahrung für alle Postfächer in einer Organisation (oder eine Teilmenge an Postfächern, die mit einem angegebenen Empfängerfilter übereinstimmen) zu aktivieren, wird die Aufbewahrung nur für die Postfächer aktiviert, die zum Zeitpunkt der Befehlsausführung vorhanden sind. Wenn Sie später neue Postfächer erstellen, müssen Sie den Befehl erneut ausführen, um die neuen Postfächer aufzubewahren. Wenn Sie oft neue Postfächer erstellen, können Sie den Befehl als geplante Aufgabe so oft wie erforderlich ausführen.</span><span class="sxs-lookup"><span data-stu-id="676c9-p116">When you use the previous command to place a hold on all mailboxes in an organization (or a subset of mailboxes matching a specified recipient filter) only mailboxes that exist at the time that you run the command are placed on hold. If you create new mailboxes later, you have to run the command again to place the new mailboxes on hold. If you create new mailboxes often, you can run the command as a scheduled task as frequently as required.</span></span>
    
  - <span data-ttu-id="676c9-p117">Platzieren aller Postfächer auf Aufbewahrung für eventuelle Rechtsstreitigkeiten kann Postfachgrößen erheblich beeinträchtigen. Planen Sie in einer Exchange Server 2013-Organisation genügend Speicher verwendet, um die Beibehaltung der Anforderungen Ihrer Organisation zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="676c9-p117">Placing all mailboxes on Litigation Hold can significantly impact mailbox sizes. In an Exchange Server 2013 organization, plan for adequate storage to meet your organization's preservation requirements.</span></span>
    
  - <span data-ttu-id="676c9-p118">Ordner "wiederherstellbare Elemente" hat einen eigenen Speichergrenzwert damit Elemente im Ordner nicht zu den Speichergrenzwert Postfach zählen. Wie bereits erklärt Postfachdaten für einen längeren Zeitraum beibehalten Wachstum des Ordners wiederherstellbare Elemente im Postfach des Benutzers gelöscht und archivieren. Um für die höhere Beanspruchung in Exchange Online zu unterstützen, wird das Kontingent für "wiederherstellbare Elemente" automatisch Erhöhung von 30 GB auf 100 GB beim Platzieren eines Postfachs auf Aufbewahrung für eventuelle Rechtsstreitigkeiten.</span><span class="sxs-lookup"><span data-stu-id="676c9-p118">The Recoverable Items folder has its own storage limit, so items in the folder don't count towards the mailbox storage limit. As previously explained, preserving mailbox data for a long period of time will result in growth of the Recoverable Items folder in a user's mailbox and archive. To accommodate for this increase in Exchange Online, the quota for the Recoverable Items folder is automatically increased from 30 GB to 100 GB when you place a mailbox on Litigation Hold.</span></span> 
    
    <span data-ttu-id="676c9-p119">In Exchange ist Server 2013, standardmäßig den maximalen Speicherplatz für den Ordner "wiederherstellbare Elemente" auch 30 GB. Es wird empfohlen, dass Sie die Größe dieses Ordners, um sicherzustellen, dass den Grenzwert erreicht werden nicht in regelmäßigen Abständen überwachen. Weitere Informationen finden Sie unter [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span><span class="sxs-lookup"><span data-stu-id="676c9-p119">In Exchange Server 2013, the default storage limit for the Recoverable Items folder is also 30 GB. We recommend that you periodically monitor the size of this folder to ensure it doesn't reach the limit. For more information, see [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).</span></span>
    
- <span data-ttu-id="676c9-p120">Der vorherige Befehl zum Platzieren aller Postfächer im Archiv verwendet einen Empfängerfilter, der alle Benutzerpostfächer zurückgibt. Sie können andere Empfängereigenschaften zum Zurückgeben einer Liste von bestimmten Postfächern verwenden, die Sie an das Cmdlet **Set-Mailbox** umleiten können, um für diese Postfächer ein Beweissicherungsverfahren zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="676c9-p120">The previous command to place a hold on all mailboxes uses a recipient filter that returns all user mailboxes. You can use other recipient properties to return a list of specific mailboxes that you can then pipe to the **Set-Mailbox** cmdlet to place a Litigation Hold on those mailboxes.</span></span> 
    
    <span data-ttu-id="676c9-p121">Hier sind einige Beispiele dafür, wie mit den Cmdlets **Get-Mailbox** und **Get-Recipient** eine Teilmenge an Postfächern basierend auf allgemeinen Benutzer- oder Postfacheigenschaften zurückgegeben wird. In diesen Beispielen wird davon ausgegangen, dass entsprechende Postfacheigenschaften (wie  _CustomAttributeN_ oder  _Department_) aufgefüllt wurden.</span><span class="sxs-lookup"><span data-stu-id="676c9-p121">Here are some examples of using the **Get-Mailbox** and **Get-Recipient** cmdlets to return a subset of mailboxes based on common user or mailbox properties. These examples assume that relevant mailbox properties (such as  _CustomAttributeN_ or  _Department_) have been populated.</span></span>
    
  ```
  Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'CustomAttribute15 -eq "OneYearLitigationHold"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'Department -eq "HR"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'PostalCode -eq "98052"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'StateOrProvince -eq "WA"'
  ```

  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -ne "DiscoveryMailbox"}
  ```

    <span data-ttu-id="676c9-p122">Sie können andere Benutzerpostfacheigenschaften in einem Filter verwenden, um Postfächer einzubeziehen bzw. auszuschließen. Weitere Informationen finden Sie unter [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span><span class="sxs-lookup"><span data-stu-id="676c9-p122">You can use other user mailbox properties in a filter to include or exclude mailboxes. For details, see [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).</span></span>
    

