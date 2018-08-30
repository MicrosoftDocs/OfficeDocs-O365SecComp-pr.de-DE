---
title: Null-Stunden automatisch löschen - Schutz vor Spam und malware
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: Null-Stunden automatisch löschen (ZAP) ist eine e-Mail-Schutz-Funktion, die Nachrichten mit Spam oder Schadsoftware erkannt, die bereits an die Posteingänge der Benutzer gesendet wurden, und klicken Sie dann den schädlichem Inhalt unschädlichen rendert. Wie ZAP dies funktioniert, hängt von den Typ des schädlichem Inhalt erkannt.
ms.openlocfilehash: dc8901dc7c1db5b323ccbeee610647b8a302fcb3
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529055"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="0b4f4-104">Null-Stunden automatisch löschen - Schutz vor Spam und malware</span><span class="sxs-lookup"><span data-stu-id="0b4f4-104">Zero-hour auto purge - protection against spam and malware</span></span>

<span data-ttu-id="0b4f4-p102">Null-Stunden automatisch löschen (ZAP) ist eine e-Mail-Schutz-Funktion, die Nachrichten mit Spam oder Schadsoftware erkannt, die bereits an die Posteingänge der Benutzer gesendet wurden, und klicken Sie dann den schädlichem Inhalt unschädlichen rendert. Wie ZAP dies funktioniert, hängt von den Typ des schädlichem Inhalt erkannt.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with spam or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected.</span></span>
  
<span data-ttu-id="0b4f4-107">ZAP ist mit Exchange Online Protection, die mit einem beliebigen Office 365-Abonnement enthalten ist, die Exchange Online-Postfächer enthält standardmäßig verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-107">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>
  
## <a name="how-does-zap-work"></a><span data-ttu-id="0b4f4-108">Wie funktioniert ZAP?</span><span class="sxs-lookup"><span data-stu-id="0b4f4-108">How does ZAP work?</span></span>

<span data-ttu-id="0b4f4-p103">Office 365 aktualisiert Anti-Spam-Modul- und Malware-Signaturen in Echtzeit auf täglicher Basis. Jedoch könnte die Benutzer weiterhin bösartige Nachrichten an ihre Posteingänge für eine Vielzahl von Gründe, wenn der Inhalt weaponized wurde zu einem Zeitpunkt, nachdem es zuerst an Benutzer übermittelt wurde erhalten. Entfernen von Adressen dies durch die Überwachung ständig mit Office 365 Spam und Malware Signaturen, aktualisiert können und daher suchen und Entfernen zuvor bereitgestellte Nachrichten bereits im Posteingang. Für e-Mail-Nachrichten, die bereits als Spam erkannt wurde, verschiebt ZAP ungelesene Nachrichten an die Junk-e-Mail-Ordner des Benutzers. Für neu erkannte Schadsoftware entfernt ZAP Anlagen aus der e-Mail-Nachricht, unabhängig davon, ob die e-Mail-Nachricht gelesen wurde. Umgekehrt gilt für Nachrichten, die fälschlicherweise als bösartige klassifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-p103">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including when the content was weaponized at a time after it was first delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures, and can therefore find and remove previously delivered messages already in inboxes. For mail that was already identified as spam, ZAP moves unread messages to the user's Junk mail folder. For newly detected malware, ZAP removes the attachments from the email message, regardless of whether the mail was read or not. The reverse is true for messages that were incorrectly classified as malicious.</span></span>
  
<span data-ttu-id="0b4f4-115">Die ZAP-Aktion ist nahtlos, für den Postfachbenutzer, kann er nicht informiert wird, dass die e-Mail-Nachricht verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-115">The ZAP action is seamless for the mailbox user, he or she is not notified the mail has been moved.</span></span>
  
<span data-ttu-id="0b4f4-116">Listen, [e-Mail-Flussregeln](https://go.microsoft.com/fwlink/p/?LinkId=722755)und Endbenutzer Regeln zulassen oder zusätzliche Filter haben Vorrang vor ZAP.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-116">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
 <span data-ttu-id="0b4f4-117">**Inhalt dieses Artikels:**</span><span class="sxs-lookup"><span data-stu-id="0b4f4-117">**In this article:**</span></span>
  
> [<span data-ttu-id="0b4f4-118">Legen Sie die Richtlinie für Spam-filter</span><span class="sxs-lookup"><span data-stu-id="0b4f4-118">Set spam filter policy</span></span>](zero-hour-auto-purge.md#BK_SetSpam)
    
> [<span data-ttu-id="0b4f4-119">Überprüfen Sie, ob ZAP Ihrer Nachricht verschoben.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-119">See if ZAP moved your message</span></span>](zero-hour-auto-purge.md#BK_DidZAPMove)
    
> [<span data-ttu-id="0b4f4-120">ZAP deaktivieren</span><span class="sxs-lookup"><span data-stu-id="0b4f4-120">Disable ZAP</span></span>](zero-hour-auto-purge.md#BK_Posh)
    
> [<span data-ttu-id="0b4f4-121">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="0b4f4-121">FAQ</span></span>](zero-hour-auto-purge.md#BK_FAQ)
    
## <a name="working-with-zap"></a><span data-ttu-id="0b4f4-122">Arbeiten mit ZAP</span><span class="sxs-lookup"><span data-stu-id="0b4f4-122">Working with ZAP</span></span>

<span data-ttu-id="0b4f4-123">ZAP ist standardmäßig aktiviert, aber Sie müssen sicherstellen, dass eine Reihe von Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="0b4f4-123">ZAP is turned on by default, but you do have to make sure a couple of conditions are met:</span></span>
  
- <span data-ttu-id="0b4f4-124">Richtlinie für Spam-Filter wird auf die [Nachricht in Junk-e-Mail-Ordner verschieben](zero-hour-auto-purge.md#BK_SetSpam)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-124">Spam filter policy is set to [Move message to Junk Email folder](zero-hour-auto-purge.md#BK_SetSpam).</span></span>
    
    <span data-ttu-id="0b4f4-125">Sie können auch eine neue Richtlinie des Spam-Filter erstellen, die nur für eine Gruppe von Benutzern angewendet wird, wenn Sie nicht möchten, dass alle Postfächer von ZAP überwachten sein.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-125">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>
    
- <span data-ttu-id="0b4f4-126">Des Benutzers [Optionen \> Junk-e-Mail-](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).</span><span class="sxs-lookup"><span data-stu-id="0b4f4-126">The user's [Options \> Junk Email](https://support.office.com/article/068FA430-F8D7-4518-A8DA-8BC74958F05F).</span></span>
    
<span data-ttu-id="0b4f4-127">Wenn Sie [überprüfen, ob ZAP Ihre Nachricht verschoben](zero-hour-auto-purge.md#BK_DidZAPMove)möchten, können Sie das Exchange Online Tool für die nachrichtenablaufverfolgung.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-127">If you want [to see if ZAP moved your message](zero-hour-auto-purge.md#BK_DidZAPMove), you can use the Exchange Online message trace tool.</span></span>
  
<span data-ttu-id="0b4f4-128">Administratoren können auch [Deaktivieren ZAP](zero-hour-auto-purge.md#BK_Posh) mithilfe von PowerShell.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-128">Admins can also [disable ZAP](zero-hour-auto-purge.md#BK_Posh) by using PowerShell.</span></span> 
  
 <span data-ttu-id="0b4f4-129">**Richtlinie für Spam-Filter festlegen**</span><span class="sxs-lookup"><span data-stu-id="0b4f4-129">**To set spam filter policy**</span></span>
  
1. <span data-ttu-id="0b4f4-130">Melden Sie sich bei der [Where zur Anmeldung bei Office 365 für Unternehmen](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) , und wählen Sie **Protection** \> **Spam-Filter**.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-130">Sign in to the [Where to sign in to Office 365 for business](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) and choose **protection** \> **spam filter**.</span></span> 
    
    ![In der Exchange-Verwaltungskonsole "Schutz" und dann Spam-filter](media/0463c879-63fa-4a6c-9b03-e980d5ef3954.PNG)
  
2. <span data-ttu-id="0b4f4-132">Wählen Sie die Filterrichtlinie, die Sie anpassen möchten, oder wählen Sie **Hinzufügen**![Symbol hinzufügen](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) einen neuen Anwendungspool erstellen.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-132">Either choose the filter policy you want to adjust, or choose **add**![Add icon](media/8ee52980-254b-440b-99a2-18d068de62d3.gif) to create a new one.</span></span> 
    
    <span data-ttu-id="0b4f4-p104">In der vorherigen Screenshot ist die Richtlinie namens "Default", aber wenn Sie zusätzliche Spam Filterrichtlinien erstellen Sie können Geben sie einen anderen Namen. Sie können nur eine begrenzte Auswahl von Benutzern auch die Richtlinie zuweisen.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-p104">In the previous screen shot, the policy is named "Default", but if you create additional spam filter policies you can give them a different name. You can also apply the policy to only a limited set of users.</span></span>
    
3. <span data-ttu-id="0b4f4-135">Klicken Sie im Richtlinienfenster wählen Sie **Spam und Massen-Aktionen**, und stellen Sie sicher, dass **Spam** **Verschieben**der Nachricht an die Junk-e-Mail-Ordner festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-135">In the policy window, choose **spam and bulk actions**, and make sure that **Spam** is set to **Move message to Junk Email folder**.</span></span> 
    
    <span data-ttu-id="0b4f4-136">Wenn Sie **Speichern** zu diesem Zeitpunkt auswählen, gilt die Richtlinie zu Ihrem Office 365-Mandanten.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-136">If you choose **Save** at this point, the policy applies to your Office 365 tenant.</span></span> 
    
    ![Festlegen von Spam und Massen-Aktionen Mpve der Nachricht an die Junk-e-Mail-Ordner](media/4332cfb3-89e1-48ba-8da8-9286f2fa1089.PNG)
  
4. <span data-ttu-id="0b4f4-p105">Wenn Sie eine neue Richtlinie erstellt und die Richtlinie nur einen Satz von Benutzer gelten sollen, Scroll **Angewendet auf** Abschnitt Filter im Fenster Richtlinie und in den Menüsteuerelementen im wählen Sie die **Empfänger**, **Domäne**oder **Gruppenmitgliedschaften** Sie Möchten Sie die Richtlinie angewendet werden soll. Sie können auch zusätzliche Bedingungen und Ausnahmen festlegen.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-p105">If you created a new policy, and you want to apply the policy to only a set of users, scroll to the **Applied To** section in the policy filter window, and in the menu controls choose the **recipients**, **domain**, or **group memberships** you want to apply the policy to. You can also set additional conditions and exceptions.</span></span> 
    
    ![Wählen Sie im Abschnitt angewendet auf die Empfänger](media/19ca10db-c0f4-432c-b3de-ad4101a23de6.PNG)
  
    <span data-ttu-id="0b4f4-141">Wählen Sie die Richtlinie auf die ausgewählten Benutzer anwenden **zu speichern** .</span><span class="sxs-lookup"><span data-stu-id="0b4f4-141">Choose **Save** to apply the policy to the selected users.</span></span> 
    
 <span data-ttu-id="0b4f4-142">**Um festzustellen, ob ZAP Ihrer Nachricht verschoben.**</span><span class="sxs-lookup"><span data-stu-id="0b4f4-142">**To see if ZAP moved your message**</span></span>
  
- <span data-ttu-id="0b4f4-143">[Feststellen und beheben Probleme bei der e-Mail-Übermittlung als ein Office 365 für Unternehmen Admin](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) können Sie ermitteln, ob die Nachricht vom ZAP verschoben wurde:</span><span class="sxs-lookup"><span data-stu-id="0b4f4-143">You can use the [Find and fix email delivery issues as an Office 365 for business admin](https://support.office.com/article/e7758b99-1896-41db-bf39-51e2dba21de6) to determine if the message was moved by ZAP:</span></span> 
    
    <span data-ttu-id="0b4f4-144">Suchen Sie nach dem Text "null-Stunden automatisch löschen (ZAP)" in Ihre Trace-Details, um eine Nachricht zu identifizieren, die vom ZAP verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-144">Look for the text "Zero-Hour Auto Purge (ZAP)" in your trace details to identify a message that was moved by ZAP.</span></span>
    
 <span data-ttu-id="0b4f4-145">**So deaktivieren Sie ZAP**</span><span class="sxs-lookup"><span data-stu-id="0b4f4-145">**To disable ZAP**</span></span>
  
- <span data-ttu-id="0b4f4-146">Wenn Sie deaktivieren möchten für Ihre Office 365-Mandanten entfernen, oder eine Gruppe von Benutzern, verwenden Sie den **ZapEnabled** -Parameter des [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), ein EOP-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-146">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
    <span data-ttu-id="0b4f4-147">Im folgenden Beispiel wird ZAP für eine inhaltsfilterrichtlinie namens "Test" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-147">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
||
|:-----|
|
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

|
   
## <a name="faq"></a><span data-ttu-id="0b4f4-148">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="0b4f4-148">FAQ</span></span>
<span data-ttu-id="0b4f4-149"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="0b4f4-149"></span></span>

 <span data-ttu-id="0b4f4-150">**Was passiert, wenn eine legitime Nachricht in den Junk-e-Mailordner verschoben wird?**</span><span class="sxs-lookup"><span data-stu-id="0b4f4-150">**What happens if a legitimate message is moved to the junk mail folder?**</span></span>
  
<span data-ttu-id="0b4f4-p106">Befolgen Sie den normalen reporting-Prozess für falsch positive ein. Der einzige Grund für die Nachricht aus dem Posteingang in den Junk-e-Mailordner verschoben werden wird, da der Dienst festgestellt hat, dass die Nachricht Spam war wäre oder böswilliges.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
 <span data-ttu-id="0b4f4-153">**Was geschieht, wenn ich Office 365 Quarantäne anstelle der Junk-e-Mailordner verwenden?**</span><span class="sxs-lookup"><span data-stu-id="0b4f4-153">**What if I use the Office 365 quarantine instead of the junk mail folder?**</span></span>
  
<span data-ttu-id="0b4f4-154">ZAP nicht Sie Nachrichten in Quarantäne aus dem Posteingang zu diesem Zeitpunkt verschieben.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-154">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
 <span data-ttu-id="0b4f4-155">**Was geschieht, wenn ich eine benutzerdefinierte e-Mail-Flussregel haben (blockieren / Regel zulassen)?**</span><span class="sxs-lookup"><span data-stu-id="0b4f4-155">**What If I have a custom mail flow rule (Block/ Allow Rule)?**</span></span>
  
<span data-ttu-id="0b4f4-p107">Regelanzahl durch Administratoren (e-Mail-Flussregeln) oder blockieren und zulassen Regeln haben Vorrang vor. Solche Nachrichten werden von der Funktion Kriterien ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0b4f4-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="0b4f4-158">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="0b4f4-158">Related Topics</span></span>
<span data-ttu-id="0b4f4-159"><a name="BK_FAQ"> </a></span><span class="sxs-lookup"><span data-stu-id="0b4f4-159"></span></span>

[<span data-ttu-id="0b4f4-160">Antispamschutz für Office 365-E-Mails</span><span class="sxs-lookup"><span data-stu-id="0b4f4-160">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="0b4f4-161">Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen</span><span class="sxs-lookup"><span data-stu-id="0b4f4-161">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

