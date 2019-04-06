---
title: Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
description: Zero-Hour Auto Purge (ZAP) ist eine e-Mail-Schutzfunktion, die Nachrichten mit Spam oder Schadsoftware erkennt, die bereits an die Posteingänge Ihrer Benutzer übermittelt wurden, und dann den schädlichen Inhalt harmlos macht. Wie ZAP Dies bewirkt, hängt vom Typ der erkannten bösartigen Inhalte ab.
ms.openlocfilehash: 7a357b50a75012408d6958ce528fddf8c203540a
ms.sourcegitcommit: e24f70699021c4f4ba56508ad0afb6f65010c357
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/05/2019
ms.locfileid: "31479631"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a><span data-ttu-id="dcdb4-104">Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="dcdb4-104">Zero-hour auto purge - protection against spam and malware</span></span>

## <a name="overview"></a><span data-ttu-id="dcdb4-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="dcdb4-105">Overview</span></span>

<span data-ttu-id="dcdb4-106">Zero-Hour Auto Purge (ZAP) ist eine e-Mail-Schutzfunktion, die Nachrichten mit Phishing, Spam oder Schadsoftware erkennt, die bereits an die Posteingänge Ihrer Benutzer übermittelt wurden, und dann den schädlichen Inhalt harmlos macht.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-106">Zero-hour auto purge (ZAP) is an email protection feature that detects messages with phish, spam, or malware that have already been delivered to your users' inboxes, and then renders the malicious content harmless.</span></span> <span data-ttu-id="dcdb4-107">Wie ZAP Dies bewirkt, hängt vom Typ der erkannten bösartigen Inhalte ab. e-Mails können aufgrund von e-Mail-Inhalten, URLs oder Anlagen gezappt werden.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-107">How ZAP does this depends on the type of malicious content detected; mail can be zapped due to mail content, URLs, or attachments.</span></span>
  
<span data-ttu-id="dcdb4-108">ZAP ist mit dem Exchange Online Protection-Standard verfügbar, der in jedem Office 365-Abonnement enthalten ist, das Exchange Online-Postfächer enthält.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-108">ZAP is available with the default Exchange Online Protection that is included with any Office 365 subscription that contains Exchange Online mailboxes.</span></span>

<span data-ttu-id="dcdb4-109">ZAP ist standardmäßig aktiviert, aber die folgenden Bedingungen müssen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="dcdb4-109">ZAP is turned on by default, but the following conditions must be met:</span></span>
  
- <span data-ttu-id="dcdb4-110">**Spam Aktion** ist so eingestellt, dass die **Nachricht in den Junk-e-Mail-Ordner verschoben**wird.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-110">**Spam action** is set to **Move message to Junk Email folder**.</span></span> <span data-ttu-id="dcdb4-111">Sie können auch eine neue Spamfilter Richtlinie erstellen, die nur für eine Gruppe von Benutzern gilt, wenn Sie nicht möchten, dass alle Postfächer durch ZAP angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-111">You can also create a new spam filter policy that applies only to a set of users if you don't want all mailboxes to be screened by ZAP.</span></span>

- <span data-ttu-id="dcdb4-112">Benutzer haben Ihre standardmäßigen Junk-e-Mail-Einstellungen beibehalten und den Junk-e-Mail-Schutz nicht deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-112">Users have kept their default junk mail settings, and have not turned off junk email protection.</span></span> <span data-ttu-id="dcdb4-113">(Weitere Informationen zu Benutzeroptionen in Outlook finden Sie unter [Ändern des schutzgrads im Junk-e-Mail-Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) .)</span><span class="sxs-lookup"><span data-stu-id="dcdb4-113">(See [Change the level of protection in the Junk Email Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) for details about user options in Outlook.)</span></span> 
  
## <a name="how-zap-works"></a><span data-ttu-id="dcdb4-114">Funktionsweise von ZAP</span><span class="sxs-lookup"><span data-stu-id="dcdb4-114">How ZAP works</span></span>

<span data-ttu-id="dcdb4-115">Office 365 aktualisiert Anti-Spam-Modul und Schadsoftware-Signaturen in Echtzeit täglich.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-115">Office 365 updates anti-spam engine and malware signatures in real-time on a daily basis.</span></span> <span data-ttu-id="dcdb4-116">Ihre Benutzer erhalten jedoch möglicherweise weiterhin bösartige Nachrichten an ihre Posteingänge aus einer Vielzahl von Gründen, einschließlich, wenn der Inhalt nach der Zustellung an Benutzer Waffen bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-116">However, your users might still get malicious messages delivered to their inboxes for a variety of reasons, including if content is weaponized after being delivered to users.</span></span> <span data-ttu-id="dcdb4-117">ZAP behebt dies, indem Aktualisierungen der Office 365-Spam-und Schadsoftware-Signaturen ständig überwacht werden.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-117">ZAP addresses this by continually monitoring updates to the Office 365 spam and malware signatures.</span></span> <span data-ttu-id="dcdb4-118">ZAP kann zuvor übermittelte Nachrichten finden und entfernen, die sich bereits in den Posteingängen der Benutzer befinden.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-118">ZAP can find and remove previously delivered messages that are already in users' inboxes.</span></span>

- <span data-ttu-id="dcdb4-119">Bei e-Mails, die als Spam identifiziert werden, verschiebt ZAP ungelesene Nachrichten in den Junk-e-Mail-Ordner der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-119">For mail that is identified as spam, ZAP moves unread messages to users' Junk mail folder.</span></span>

- <span data-ttu-id="dcdb4-120">Bei e-Mails, die als Phishing identifiziert werden, verschiebt ZAP Nachrichten in den Junk-e-Mail-Ordner der Benutzer, unabhängig davon, ob die e-Mail gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-120">For mail that is identified as phish, ZAP moves messages to users' Junk mail folder, regardless of whether the email has been read.</span></span>

- <span data-ttu-id="dcdb4-121">Bei neu erkannter Schadsoftware entfernt ZAP Anhänge von e-Mail-Nachrichten, unabhängig davon, ob die e-Mail gelesen wurde.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-121">For newly detected malware, ZAP removes attachments from email messages, regardless of whether the email has been read.</span></span>
  
<span data-ttu-id="dcdb4-122">Die ZAP-Aktion ist für den Postfachbenutzer nahtlos. Sie werden nicht benachrichtigt, wenn eine e-Mail-Nachricht verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-122">The ZAP action is seamless for the mailbox user; they are not notified if an email message is moved.</span></span>
  
<span data-ttu-id="dcdb4-123">Zulassungslisten, [Nachrichtenfluss Regeln](https://go.microsoft.com/fwlink/p/?LinkId=722755)und Endbenutzer Regeln oder zusätzliche Filter haben Vorrang vor zap.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-123">Allow lists, [mail flow rules](https://go.microsoft.com/fwlink/p/?LinkId=722755), and end user rules or additional filters take precedence over ZAP.</span></span>
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a><span data-ttu-id="dcdb4-124">So überarbeiten Sie eine Spamfilter Richtlinie</span><span class="sxs-lookup"><span data-stu-id="dcdb4-124">To review or set up a spam filter policy</span></span>
  
1. <span data-ttu-id="dcdb4-125">Wechseln Sie [https://protection.office.com](https://protection.office.com) zu und melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-125">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span>

2. <span data-ttu-id="dcdb4-126">Wählen Sie unter **Bedrohungs Verwaltung**die Option **Antispam**aus.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-126">Under **Threat management**, choose **Anti-spam**.</span></span>

3. <span data-ttu-id="dcdb4-127">Überarbeiten Sie die Standardeinstellungen.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-127">Review the standard settings.</span></span>

4. <span data-ttu-id="dcdb4-128">Wenn Sie Ihre Einstellungen anpassen möchten, wählen Sie die Registerkarte **Benutzerdefiniert** aus, und aktivieren Sie **benutzerdefinierte Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-128">If you want to customize your settings, select the **Custom** tab, and turn on **Custom settings**.</span></span> <span data-ttu-id="dcdb4-129">Bearbeiten Sie Ihre Einstellungen, und wählen Sie dann **eine Richtlinie erstellen** , um eine neue Richtlinie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-129">Edit your settings and if you want, choose **+ Create a policy** to add a new policy.</span></span>

## <a name="to-see-if-zap-moved-your-message"></a><span data-ttu-id="dcdb4-130">So überprüfen Sie, ob ZAP Ihre Nachricht verschoben hat</span><span class="sxs-lookup"><span data-stu-id="dcdb4-130">To see if ZAP moved your message</span></span>

<span data-ttu-id="dcdb4-131">Wenn Sie sehen möchten, ob ZAP Ihre Nachricht verschoben hat, können Sie entweder den [Status Bericht](view-email-security-reports.md#threat-protection-status-report) für den Bedrohungsschutz (oder den Bedrohungs- [Explorer](use-explorer-in-security-and-compliance.md)) verwenden.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-131">If you want to see if ZAP moved your message, you can use either the [Threat Protection Status report](view-email-security-reports.md#threat-protection-status-report) (or [Threat Explorer](use-explorer-in-security-and-compliance.md)).</span></span>

## <a name="to-disable-zap"></a><span data-ttu-id="dcdb4-132">So deaktivieren Sie ZAP</span><span class="sxs-lookup"><span data-stu-id="dcdb4-132">To disable ZAP</span></span>
  
<span data-ttu-id="dcdb4-133">Wenn Sie ZAP für Ihren Office 365-Mandanten oder eine Gruppe von Benutzern deaktivieren möchten, verwenden Sie den **ZapEnabled** -Parameter von [Set-HOSTEDCONTENTFILTERPOLICY dient zum](https://go.microsoft.com/fwlink/p/?LinkId=722758), einem EoP-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-133">If you want to disable ZAP for your Office 365 tenant, or a set of users, use the **ZapEnabled** parameter of [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), an EOP cmdlet.</span></span>

<span data-ttu-id="dcdb4-134">Im folgenden Beispiel ist ZAP für eine Inhaltsfilter Richtlinie mit dem Namen "Test" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-134">In the following example, ZAP is disabled for a content filter policy named "Test".</span></span>

```Powershell
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a><span data-ttu-id="dcdb4-135">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="dcdb4-135">FAQ</span></span>

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a><span data-ttu-id="dcdb4-136">Was geschieht, wenn eine legitime Nachricht in den Junk-e-Mail-Ordner verschoben wird?</span><span class="sxs-lookup"><span data-stu-id="dcdb4-136">What happens if a legitimate message is moved to the junk mail folder?</span></span>
  
<span data-ttu-id="dcdb4-137">Sie sollten den normalen Berichtsprozess für [falsch positive Ergebnisse](prevent-email-from-being-marked-as-spam.md)befolgen.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-137">You should follow the normal reporting process for [false-positives](prevent-email-from-being-marked-as-spam.md).</span></span> <span data-ttu-id="dcdb4-138">Der einzige Grund, warum die Nachricht aus dem Posteingang in den Junk-e-Mail-Ordner verschoben würde, liegt darin, dass der Dienst festgestellt hat, dass es sich um Spam oder bösartige Nachricht handelt.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-138">The only reason the message would be moved from the inbox to the junk mail folder would be because the service has determined that the message was spam or malicious.</span></span>
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a><span data-ttu-id="dcdb4-139">Was geschieht, wenn ich die Office 365-Quarantäne anstelle des Junk-e-Mail-Ordners verwende?</span><span class="sxs-lookup"><span data-stu-id="dcdb4-139">What if I use the Office 365 quarantine instead of the junk mail folder?</span></span>
  
<span data-ttu-id="dcdb4-140">ZAP verschiebt Nachrichten zu diesem Zeitpunkt nicht aus dem Posteingang in die Quarantäne.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-140">ZAP doesn't move messages into quarantine from the Inbox at this time.</span></span>
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a><span data-ttu-id="dcdb4-141">Was geschieht, wenn ich über eine benutzerdefinierte e-Mail-Fluss Regel (Block/Allow Rule) verfüge?</span><span class="sxs-lookup"><span data-stu-id="dcdb4-141">What If I have a custom mail flow rule (Block/ Allow Rule)?</span></span>
  
<span data-ttu-id="dcdb4-142">Von Administratoren erstellte Regeln (Nachrichtenfluss Regeln) oder Sperr-und Zulassungsregeln haben Vorrang.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-142">Rules created by admins (mail flow rules) or Block and Allow rules take precedence.</span></span> <span data-ttu-id="dcdb4-143">Solche Nachrichten werden von den Feature-Kriterien ausgeschlossen, sodass der Nachrichtenfluss der Regelaktion (Block/Allow Rule) folgt.</span><span class="sxs-lookup"><span data-stu-id="dcdb4-143">Such messages are excluded from the feature criteria so the mail flow will follow the rule action (Block/Allow Rule).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="dcdb4-144">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dcdb4-144">Related Topics</span></span>

[<span data-ttu-id="dcdb4-145">Antispamschutz für Office 365-E-Mails</span><span class="sxs-lookup"><span data-stu-id="dcdb4-145">Office 365 Email Anti-Spam Protection</span></span>](anti-spam-protection.md)
  
[<span data-ttu-id="dcdb4-146">Blockieren von Spam-E-Mail mit dem Office 365-Spamfilter zur Vermeidung von Problemen mit falsch negativen Nachrichten</span><span class="sxs-lookup"><span data-stu-id="dcdb4-146">Block email spam with the Office 365 spam filter to prevent false negative issues</span></span>](reduce-spam-email.md)