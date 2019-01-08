---
title: Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
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
ms.openlocfilehash: 1e90e69018b7640bb36011287abd5bcd77d43358
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749319"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="9df0f-104">Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="9df0f-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="9df0f-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9df0f-105">Overview</span></span>

<span data-ttu-id="9df0f-p102">Null-Stunden automatisch löschen (ZAP) ist eine e-Mail-Schutz-Funktion, die Nachrichten mit Phishing, Spam oder Schadsoftware erkannt, die bereits an die Posteingänge der Benutzer gesendet wurden, und klicken Sie dann rendert schädlichem Inhalt unschädlichen. Wie ZAP dies funktioniert, hängt von den Typ des schädlichem Inhalt erkannt. e-Mail-Nachrichten kann von e-Mail-Inhalten, URLs oder Anlagen zapped werden.</span><span class="sxs-lookup"><span data-stu-id="9df0f-p102">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless. How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="9df0f-108">ZAP ist mit Exchange Online Protection, die mit einem beliebigen Office 365-Abonnement enthalten ist, die Exchange Online-Postfächer enthält standardmäßig verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9df0f-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="9df0f-109">ZAP ist standardmäßig aktiviert, jedoch müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="9df0f-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="9df0f-110">**Spam-Aktion** ist eine **Nachricht in Junk-e-Mail-Ordner verschieben**festlegen.</span><span class="sxs-lookup"><span data-stu-id="9df0f-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <br/><span data-ttu-id="9df0f-111">Sie können auch eine neue Richtlinie des Spam-Filter erstellen, die nur für eine Gruppe von Benutzern angewendet wird, wenn Sie nicht möchten, dass alle Postfächer von ZAP überwachten sein.</span><span class="sxs-lookup"><span data-stu-id="9df0f-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="9df0f-p103">Benutzer haben ihre standardmäßige Junk-e-Mail-Einstellungen gespeichert und junk-e-Mail-Schutz nicht deaktiviert haben. (Informationen zu den Benutzeroptionen in Outlook finden Sie unter [Ändern der Schutz in den Junk-e-Mail-Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) .)</span><span class="sxs-lookup"><span data-stu-id="9df0f-p103">Users have kept their default junk mail settings, and have not turned off junk email protection. (See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-does-zap-work"></a><span data-ttu-id="9df0f-114">Wie funktioniert ZAP?</span><span class="sxs-lookup"><span data-stu-id="9df0f-114">How does ZAP work?</span></span>

<span data-ttu-id="9df0f-p104">Office 365 aktualisiert Anti-Spam-Modul- und Malware-Signaturen in Echtzeit auf täglicher Basis. Jedoch könnte die Benutzer weiterhin bösartige Nachrichten an ihre Posteingänge für eine Vielzahl von Gründen, einschließlich, wenn Inhalte nach der Übermittlung an Benutzer weaponized ist erhalten. Entfernen Sie Adressen dies durch die Überwachung ständig mit Office 365 Spam und Malware Signaturen aktualisiert. ZAP kann suchen und Entfernen zuvor zugestellte Nachrichten, die bereits im Posteingang Benutzer sind.</span><span class="sxs-lookup"><span data-stu-id="9df0f-p104">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis. However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users. ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures. ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span> 

- <span data-ttu-id="9df0f-119">Für e-Mail-Nachrichten, die als Spam gekennzeichnet ist, verschiebt ZAP ungelesene Nachrichten an Benutzer Junk-e-Mail-Ordner.</span><span class="sxs-lookup"><span data-stu-id="9df0f-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span> 

- <span data-ttu-id="9df0f-120">Für e-Mail-Nachrichten, die als Spam gekennzeichnet ist, verschiebt ZAP Nachrichten an Benutzer Junk-e-Mail-Ordner, unabhängig davon, ob die e-Mail-Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="9df0f-120">For mail that is identified as spam, ZAP moves messages to users' Junk mail folder, regardless of whether the email has been read.</span></span>

- <span data-ttu-id="9df0f-121">Für neu erkannte Schadsoftware entfernt ZAP Anlagen in e-Mail-Nachrichten, unabhängig davon, ob die e-Mail-Nachricht gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="9df0f-121">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span> 
  
<span data-ttu-id="9df0f-122">Die ZAP-Aktion ist für den Postfachbenutzer nahtlos. Sie werden nicht benachrichtigt, wenn eine e-Mail-Nachricht verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="9df0f-122">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span>
  
<span data-ttu-id="9df0f-123">Listen, [e-Mail-Flussregeln](https://go.microsoft.com/fwlink/p/?LinkId=722755)und Endbenutzer Regeln zulassen oder zusätzliche Filter haben Vorrang vor ZAP.</span><span class="sxs-lookup"><span data-stu-id="9df0f-123">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="9df0f-124">Um zu überprüfen, oder richten Sie eine Spam-Filter-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="9df0f-124">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="9df0f-125">Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365.</span><span class="sxs-lookup"><span data-stu-id="9df0f-125">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="9df0f-126">Wählen Sie unter **Threat Management** **Anti-Spam**aus.</span><span class="sxs-lookup"><span data-stu-id="9df0f-126">Under **Threat management**, choose **Anti-spam**.</span></span>

3. <span data-ttu-id="9df0f-127">Überprüfen Sie die Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="9df0f-127">Review the standard settings.</span></span> 

4. <span data-ttu-id="9df0f-p105">Wenn Sie Ihre Einstellungen anpassen möchten, wählen Sie die Registerkarte **Benutzerdefiniert** aus, und aktivieren Sie **Benutzerdefinierte Einstellungen**. Bearbeiten Sie Ihre Einstellungen, und wenn Sie möchten, wählen Sie **+ Erstellen einer Richtlinie** um eine neue Richtlinie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9df0f-p105">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**. Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span> 
    
## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="9df0f-130">Um festzustellen, ob ZAP Ihrer Nachricht verschoben.</span><span class="sxs-lookup"><span data-stu-id="9df0f-130">To see if ZAP moved your message</span></span>

<span data-ttu-id="9df0f-131">Wenn um festzustellen, ob ZAP Ihre Nachricht verschoben werden soll, können Sie entweder die [Threat Protection Statusbericht](view-email-security-reports.md#threat-protection-status-report) (oder [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span><span class="sxs-lookup"><span data-stu-id="9df0f-131">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) (or [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span></span>
    
## <a name="to-disable-zap"></a><span data-ttu-id="9df0f-132">So deaktivieren Sie ZAP</span><span class="sxs-lookup"><span data-stu-id="9df0f-132">To disable ZAP</span></span>
  
<span data-ttu-id="9df0f-133">Wenn Sie deaktivieren möchten für Ihre Office 365-Mandanten entfernen, oder eine Gruppe von Benutzern, verwenden Sie den **ZapEnabled** -Parameter des [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), ein EOP-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9df0f-133">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>
    
<span data-ttu-id="9df0f-134">Im folgenden Beispiel wird ZAP für eine inhaltsfilterrichtlinie namens "Test" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9df0f-134">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="9df0f-135">Häufig gestellte Fragen (FAQ)</span><span class="sxs-lookup"><span data-stu-id="9df0f-135">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="9df0f-136">Was passiert, wenn eine legitime Nachricht in den Junk-e-Mailordner verschoben wird?</span><span class="sxs-lookup"><span data-stu-id="9df0f-136">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="9df0f-p106">Befolgen Sie den normalen reporting-Prozess für falsch positive ein. Der einzige Grund für die Nachricht aus dem Posteingang in den Junk-e-Mailordner verschoben werden wird, da der Dienst festgestellt hat, dass die Nachricht Spam war wäre oder böswilliges.</span><span class="sxs-lookup"><span data-stu-id="9df0f-p106">You should follow the normal reporting process for false-positives. The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="9df0f-139">Was geschieht, wenn ich Office 365 Quarantäne anstelle der Junk-e-Mailordner verwenden?</span><span class="sxs-lookup"><span data-stu-id="9df0f-139">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="9df0f-140">ZAP nicht Sie Nachrichten in Quarantäne aus dem Posteingang zu diesem Zeitpunkt verschieben.</span><span class="sxs-lookup"><span data-stu-id="9df0f-140">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="9df0f-141">Was geschieht, wenn ich eine benutzerdefinierte e-Mail-Flussregel haben (blockieren / Regel zulassen)?</span><span class="sxs-lookup"><span data-stu-id="9df0f-141">What If I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="9df0f-p107">Regelanzahl durch Administratoren (e-Mail-Flussregeln) oder blockieren und zulassen Regeln haben Vorrang vor. Solche Nachrichten werden von der Funktion Kriterien ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9df0f-p107">Rules created by admins (mail flow rules) or Block and Allow rules take precedence. Such messages are excluded from the feature criteria.</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="9df0f-144">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9df0f-144">Related Topics</span></span>

[<span data-ttu-id="9df0f-145">Antispamschutz für Office 365-E-Mails</span><span class="sxs-lookup"><span data-stu-id="9df0f-145">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="9df0f-146">Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen</span><span class="sxs-lookup"><span data-stu-id="9df0f-146">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](block-email-spam-to-prevent-false-negatives.md)
  

