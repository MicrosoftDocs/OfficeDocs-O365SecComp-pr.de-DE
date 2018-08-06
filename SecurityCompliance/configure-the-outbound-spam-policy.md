---
title: Konfigurieren der Richtlinie für ausgehende Spamnachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/10/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
description: Die Filterung ausgehender Spamnachrichten ist immer aktiviert, wenn Sie den Dienst für das Senden ausgehender E-Mails verwenden und dadurch Organisationen, die den Dienst nutzen, und ihre jeweiligen Empfänger schützen.
ms.openlocfilehash: 3a3e07731e16da148131ceb6f555e84ed94f7ae5
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026302"
---
# <a name="configure-the-outbound-spam-policy"></a><span data-ttu-id="f7b1f-103">Konfigurieren der Richtlinie für ausgehende Spamnachrichten</span><span class="sxs-lookup"><span data-stu-id="f7b1f-103">Configure the outbound spam policy</span></span>

<span data-ttu-id="f7b1f-p101">Die Filterung ausgehender Spamnachrichten ist immer aktiviert, wenn Sie den Dienst für das Senden ausgehender E-Mails verwenden und dadurch Organisationen, die den Dienst nutzen, und ihre jeweiligen Empfänger schützen. Ebenso wie die Filterung eingehender Nachrichten besteht die Filterung ausgehender Nachrichten aus einer Verbindungsfilterung und einer Inhaltsfilterung, wobei die Einstellungen für den ausgehenden Filter nicht konfiguriert werden können. Wenn eine ausgehende Nachricht als Spam identifiziert wird, wird sie durch den Pool für besonders riskante Zustellungen geleitet, der die Wahrscheinlichkeit reduziert, dass der normale Pool für ausgehende IP-Adressen einer Sperrliste hinzugefügt wird. Falls ein Kunde auch weiterhin ausgehende Spamnachrichten über den Dienst sendet, wird er für das Senden von Nachrichten gesperrt. Die Filterung ausgehender Spamnachrichten kann zwar nicht deaktiviert oder geändert werden, aber Sie können verschiedene unternehmensweite Spameinstellungen über die Standardrichtlinie für ausgehende Spamnachrichten konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-p101">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients. Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable. If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list. If a customer continues to send outbound spam through the service, they will be blocked from sending messages. Although outbound spam filtering cannot be disabled or changed, you can configure several company-wide outbound spam settings via the default outbound spam policy.</span></span> 
  
<span data-ttu-id="f7b1f-109">Das folgende Video zeigt, wie die Richtlinie für ausgehende Spamnachrichten konfiguriert wird:</span><span class="sxs-lookup"><span data-stu-id="f7b1f-109">The following video shows how to configure the outbound spam policy:</span></span>
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/1f20d655-0d3d-4141-9cae-e57f5a6cffe8?autoplay=false]
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="f7b1f-110">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="f7b1f-110">What do you need to know before you begin?</span></span>
<span data-ttu-id="f7b1f-111"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="f7b1f-111"></span></span>

<span data-ttu-id="f7b1f-112">Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="f7b1f-112">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="f7b1f-p102">Sie müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren oder Verfahren ausführen können. Welche Berechtigungen Sie benötigen, finden Sie unter der "Anti-Spam-Eintrag im Thema [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f7b1f-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Anti-spam entry in the [Feature Permissions in Exchange Online](http://technet.microsoft.com/library/15073ce1-0917-403b-8839-02a2ebc96e16.aspx) topic.</span></span> 
  
<span data-ttu-id="f7b1f-115">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Tastenkombinationen in der Exchange-Verwaltungskonsole**.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-115">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
<span data-ttu-id="f7b1f-p103">Das folgende Verfahren kann auch über remote-PowerShell erfolgen. Verwenden Sie das Cmdlet [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) , um Ihre Einstellungen, und das [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) zum Bearbeiten Ihrer Einstellungen für ausgehende Spamnachrichten Richtlinie zu prüfen. Weitere Informationen zu Windows PowerShell verwenden, um die Verbindung mit Exchange Online Protection finden Sie unter [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). So verwenden Sie Windows PowerShell für die Verbindung zu Exchange Online finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="f7b1f-p103">The following procedure can also be performed via remote PowerShell. Use the [Get-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/8f15c83c-c10a-4d9d-b135-35321430bdc2.aspx) cmdlet to review your settings, and the [Set-HostedOutboundSpamFilterPolicy](http://technet.microsoft.com/library/665d1b04-d4b5-4a0e-811a-4e37096ccbfd.aspx) to edit your outbound spam policy settings. To learn how to use Windows PowerShell to connect to Exchange Online Protection, see [Connect to Exchange Online Protection PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627290). To learn how to use Windows PowerShell to connect to Exchange Online, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
  
## <a name="use-the-eac-to-edit-the-default-outbound-spam-policy"></a><span data-ttu-id="f7b1f-120">Bearbeiten der Standardrichtlinie für ausgehende Spamnachrichten mithilfe der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="f7b1f-120">Use the EAC to edit the default outbound spam policy</span></span>
<span data-ttu-id="f7b1f-121"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="f7b1f-121"></span></span>

<span data-ttu-id="f7b1f-122">Verwenden Sie das folgende Verfahren, um die Standardrichtlinie für ausgehende Spamnachrichten zu bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="f7b1f-122">Use the following procedure to edit the default outbound spam policy:</span></span>
  
### <a name="to-configure-the-default-outbound-spam-policy"></a><span data-ttu-id="f7b1f-123">So konfigurieren Sie die Standardrichtlinie für ausgehende Spamnachrichten</span><span class="sxs-lookup"><span data-stu-id="f7b1f-123">To configure the default outbound spam policy</span></span>

1. <span data-ttu-id="f7b1f-124">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Ausgehende Spamnachrichten**, und doppelklicken Sie dann auf die Standardrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-124">In the Exchange admin center (EAC), navigate to **Protection** \> **Outbound spam**, and then double-click the default policy.</span></span>
    
2. <span data-ttu-id="f7b1f-125">Wählen Sie die Menüoption **Einstellungen für ausgehenden Spam** aus.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-125">Select the **Outbound spam preferences** menu option.</span></span> 
    
3. <span data-ttu-id="f7b1f-126">Aktivieren Sie folgende Kontrollkästchen für ausgehende Nachrichten, und geben Sie dann eine oder mehrere zugehörige E-Mail-Adressen in dem nebenstehenden Eingabefeld ein (es kann sich dabei um Verteilerlisten handelt, wenn diese gültige SMTP-Ziele ergeben):</span><span class="sxs-lookup"><span data-stu-id="f7b1f-126">Select the following check boxes pertaining to outbound messages, and then specify an associated email address or addresses in the accompanying input box (these can be distribution lists if they resolve as valid SMTP destinations):</span></span>
    
1. <span data-ttu-id="f7b1f-p104">**Eine Kopie aller verdächtigen ausgehenden E-Mails an folgende E-Mail-Adressen senden**. Dabei handelt es sich um Nachrichten, die vom Filter als Spam markiert wurden (unabhängig von der SCL-Bewertung). Sie werden vom Filter nicht zurückgewiesen, sondern durch den Pool für besonders riskante Zustellungen geleitet. Trennen Sie mehrere Adressen durch ein Semikolon. Beachten Sie, dass die angegebenen Empfänger die Nachrichten als "Bcc" (Blind Carbon Copy, nicht sichtbare Kopie) erhalten (in den Feldern "Von" und "An" sind der ursprüngliche Sender und Empfänger angegeben).</span><span class="sxs-lookup"><span data-stu-id="f7b1f-p104">**Send a copy of all suspicious outbound email messages to the following email address or addresses**. These are messages that are marked as spam by the filter (regardless of the SCL rating). They are not rejected by the filter but are routed through the higher risk delivery pool. Separate multiple addresses with a semicolon. Note that the recipients specified will receive the messages as a Blind carbon copy (Bcc) address (the From and To fields are the original sender and recipient).</span></span>
    
2. <span data-ttu-id="f7b1f-p105">**Senden Sie eine Benachrichtigung an die folgende E-Mail-Adresse, wenn ein Absender für das Senden ausgehender Spamnachrichten blockiert wird**. Trennen Sie mehrere Adressen durch ein Semikolon.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-p105">**Send a notification to the following email address when a sender is blocked sending outbound spam**. Separate multiple addresses with a semicolon.</span></span>
    
    <span data-ttu-id="f7b1f-p106">Wenn eine auffällige Menge an Spamnachrichten von einem bestimmten Benutzer stammt, wird dieser Benutzer für das Senden von E-Mails gesperrt. Der Administrator der Domäne, der in dieser Einstellung angegeben ist, wird darüber informiert, dass ausgehende Nachrichten für diesen Benutzer blockiert werden. Ein Beispiel für diese Benachrichtigung finden Sie unter [Beispielbenachrichtigung, wenn ein Absender aufgrund des Versendens von ausgehendem Spam blockiert wird](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Informationen zur erneuten Aktivierung finden Sie unter [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span><span class="sxs-lookup"><span data-stu-id="f7b1f-p106">When a significant amount of spam is originating from a particular user, the user is disabled from sending email messages. The administrator for the domain, who is specified using this setting, will be informed that outbound messages are blocked for this user. To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>
    
4. <span data-ttu-id="f7b1f-p107">Klicken Sie auf **Speichern**. Im Bereich auf der rechten Seite wird eine Zusammenfassung der Standardrichtlinieneinstellungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7b1f-p107">Click **save**. A summary of your default policy settings appears in the right pane.</span></span>
    
## <a name="for-more-information"></a><span data-ttu-id="f7b1f-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f7b1f-140">For more information</span></span>
<span data-ttu-id="f7b1f-141"><a name="sectionSection2"> </a></span><span class="sxs-lookup"><span data-stu-id="f7b1f-141"></span></span>

[<span data-ttu-id="f7b1f-142">Pool für besonders riskante Zustellungen für ausgehende Nachrichten</span><span class="sxs-lookup"><span data-stu-id="f7b1f-142">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)
  
[<span data-ttu-id="f7b1f-143">Anti-Spam-Schutz – häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="f7b1f-143">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
  

