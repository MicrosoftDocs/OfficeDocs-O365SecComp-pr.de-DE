---
title: Verwenden von Nachrichtenfluss Regeln zum Konfigurieren der Massen-e-Mail-Filterung in Exchange Online Protection
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
ms.collection:
- M365-security-compliance
description: Administratoren erfahren, wie Sie e-Mail-Flussregeln in Exchange Online Protection für die Massen-e-Mail-Filterung verwenden.
ms.openlocfilehash: 43f0af6fe41bc7f8f4a62d0d87dbd825fb868f7b
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693284"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a><span data-ttu-id="faf37-103">Verwenden von Nachrichtenfluss Regeln zum Konfigurieren der Massen-e-Mail-Filterung in Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="faf37-103">Use mail flow rules to configure bulk email filtering in Exchange Online Protection</span></span>

<span data-ttu-id="faf37-p101">Sie können den unternehmensweiten Inhaltsfilter für Spam und Massen-E-Mails über die Standardrichtlinien für die Spam-Inhaltsfilterung festlegen. Informationen zum Festlegen der Richtlinien für die Inhaltsfilterung finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) und [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/Set-HostedContentFilterPolicy?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="faf37-p101">You can set company-wide content filters for spam and bulk email using the default spam content-filter policies. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) and [Set-HostedContentFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/Set-HostedContentFilterPolicy?view=exchange-ps) on how to set the content filter policies.</span></span> 
  
<span data-ttu-id="faf37-106">Wenn Sie weitere Optionen zum Filtern von Massennachrichten benötigen, können Sie Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) erstellen, um nach Textmustern oder Ausdrücken zu suchen, die häufig in Massen-e-Mails gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="faf37-106">If you want to more options to filter bulk messages, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases frequently found in bulk emails.</span></span> <span data-ttu-id="faf37-107">Alle Nachrichten, die diese Merkmale enthalten, werden als Spam markiert.</span><span class="sxs-lookup"><span data-stu-id="faf37-107">Any message containing these characteristics will be marked as spam.</span></span> <span data-ttu-id="faf37-108">Mithilfe dieser Regeln können Sie die Menge an unterwünschten Massen-E-Mails verringern, die Ihre Organisation empfängt.</span><span class="sxs-lookup"><span data-stu-id="faf37-108">Using these rules can help reduce the amount of unwanted bulk email your organization receives.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="faf37-109">Bevor Sie die in diesem Thema dokumentierten Nachrichtenfluss Regeln erstellen, sollten Sie zuerst lesen, [was der Unterschied zwischen Junk-e-Mail und Massen-e-Mails ist?](what-s-the-difference-between-junk-email-and-bulk-email.md) und [Werte für Massen Beschwerden](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="faf37-109">Before creating the mail flow rules documented this topic, we recommend that you first read [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk Complaint Level values](bulk-complaint-level-values.md).</span></span><br><span data-ttu-id="faf37-p103">Durch die folgenden Verfahren wird eine Nachricht für Ihre gesamte Organisation als Spam markiert. Sie können jedoch eine andere Bedingung hinzufügen, damit diese Regeln nur für bestimmte Empfänger in Ihrer Organisation gelten. Auf diese Weise können die aggressiven Filtereinstellungen für Massen-E-Mails nur für einige wenige Benutzer gelten, die verstärkt anvisiert werden, während der Rest Ihrer Benutzer (die zumeist die Massen-E-Mails erhalten, für die sie sich registriert haben) nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="faf37-p103"> The following procedures mark a message as spam for your entire organization. However, you can add another condition to apply these rules only to specific recipients in your organization. This way, the aggressive bulk email filtering settings can apply to a few users who are highly targeted, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span> 
  
## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a><span data-ttu-id="faf37-113">Erstellen einer e-Mail-Fluss Regel zum Filtern von Massen-e-Mails basierend auf Textmustern</span><span class="sxs-lookup"><span data-stu-id="faf37-113">Create a mail flow rule to filter bulk email messages based on text patterns</span></span>

1. <span data-ttu-id="faf37-114">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="faf37-114">In the Exchange admin center (EAC), go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="faf37-115">Klicken Sie auf Symbol](media/ITPro-EAC-AddIcon.gif) hinzufügen, und wählen Sie dann **neue Regel erstellen**aus. \*\*\*\* ![</span><span class="sxs-lookup"><span data-stu-id="faf37-115">Click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="faf37-116">Geben Sie einen Namen für die Regel ein.</span><span class="sxs-lookup"><span data-stu-id="faf37-116">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="faf37-p104">Klicken Sie auf **Weitere Optionen**. Aktivieren Sie unter **Diese Regel anwenden, wenn,** die Option **Betreff oder Nachrichtentext** \> **Betreff oder Nachrichtentext entspricht diesen Textmustern**.</span><span class="sxs-lookup"><span data-stu-id="faf37-p104">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body matches these text patterns**.</span></span>
    
5. <span data-ttu-id="faf37-119">Geben Sie im Dialogfeld **Wörter oder Ausdrücke angeben** die folgenden häufig in Massen-E-Mails vorkommenden regulären Ausdrücke nacheinander ein, und klicken Sie auf **OK**, sobald Sie fertig sind:</span><span class="sxs-lookup"><span data-stu-id="faf37-119">In the **specify words or phrases** dialog box, add the following regular expressions commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - `If you are unable to view the content of this email\, please`
    
   - `\>(safe )?unsubscribe( here)?\</a\>`
    
   - `If you do not wish to receive further communications like this\, please`
    
   - `\<img height\="?1"? width\="?1"? sr\c=.?http\://`
    
   - `To stop receiving these+emails\:http\://`
    
   - `To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)`
    
   - `no longer (wish )?(to )?(be sent|receive) w+ email`
    
   - `If you are unable to view the content of this email\, please click here`
    
   - `To ensure you receive (your daily deals|our e-?mails)\, add`
    
   - `If you no longer wish to receive these emails`
    
   - `to change your (subscription preferences|preferences or unsubscribe)`
    
   - `click (here to|the) unsubscribe`
    
   <span data-ttu-id="faf37-120">Die obige Liste ist kein umfassender Satz regulärer Ausdrücke, die in Massen-e-Mails gefunden werden. Weitere können bei Bedarf hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="faf37-120">The above list isn't an exhaustive set of regular expressions found in bulk emails; more can be added or removed as needed.</span></span> <span data-ttu-id="faf37-121">Dies ist jedoch ein guter Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="faf37-121">However, it's a good starting point.</span></span><br><span data-ttu-id="faf37-122">Die Suche nach Wörtern oder Textmustern im Betreff oder anderen Kopfzeilenfeldern in der Nachricht tritt auf, *nachdem* die Nachricht aus der MIME-Inhalts Übertragungscodierungsmethode dekodiert wurde, die zum Übertragen der binären Nachricht zwischen SMTP-Servern im ASCII-Text verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="faf37-122">The search for words or text patterns in the subject or other header fields in the message occurs  *after*  the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text.</span></span> <span data-ttu-id="faf37-123">Sie können keine Bedingungen oder Ausnahmen für die Suche nach Rohwerten (in der Regel Base64-codiert) im Betreff oder in anderen Kopfzeilenfeldern in Nachrichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="faf37-123">You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span> 
    
6. <span data-ttu-id="faf37-124">Wählen Sie unter **Gehen Sie folgendermaßen vor...** die Option **Nachrichteneigenschaften ändern** \> **SCL-Bewertung (Spam Confidence Level) festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="faf37-124">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="faf37-125">Legen Sie im Dialogfeld **SCL angeben** den SCL auf **5**, **6** oder **9** fest, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="faf37-125">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="faf37-p107">Wenn der SCL auf 5 oder 6 festgelegt wird, wird die **Spam**-Aktion ausgeführt, und wenn der SCL auf 9 festgelegt wird, wird die Aktion **Nachricht mit hoher Spamwahrscheinlichkeit** ausgeführt, wie in der Inhaltsfilterrichtlinie konfiguriert. Der Dienst führt die in der Inhaltsfilterrichtlinie festgelegte Aktion aus. Die Standardaktion ist, die Nachricht an den Junk-E-Mail-Ordner der Empfänger zuzustellen. Es können allerdings, wie in [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) beschrieben, andere Aktionen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="faf37-p107">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   <span data-ttu-id="faf37-129">Wenn die Nachricht von der konfigurierten Aktion isoliert wird, anstatt Sie an den Junk-e-Mail-Ordner der Empfänger zu senden, wird die Nachricht an die Administrator Quarantäne als eine Übereinstimmung mit der Nachrichtenfluss Regel gesendet und ist nicht in der Spamquarantäne für Endbenutzer oder über Endbenutzer verfügbar. Spambenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="faf37-129">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="faf37-130">Weitere Informationen zu SCL-Werten im Dienst finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="faf37-130">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
8. <span data-ttu-id="faf37-131">Speichern Sie die Regel.</span><span class="sxs-lookup"><span data-stu-id="faf37-131">Save the rule.</span></span>
    
## <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a><span data-ttu-id="faf37-132">Erstellen einer e-Mail-Fluss Regel zum Filtern von Massen-e-Mails basierend auf Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="faf37-132">Create a mail flow rule to filter bulk email messages based on phrases</span></span>

1. <span data-ttu-id="faf37-133">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="faf37-133">In the EAC, go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="faf37-134">Klicken Sie auf Symbol](media/ITPro-EAC-AddIcon.gif) hinzufügen, und wählen Sie dann **neue Regel erstellen**aus. \*\*\*\* ![</span><span class="sxs-lookup"><span data-stu-id="faf37-134">Click **Add** ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="faf37-135">Geben Sie einen Namen für die Regel ein.</span><span class="sxs-lookup"><span data-stu-id="faf37-135">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="faf37-p108">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span><span class="sxs-lookup"><span data-stu-id="faf37-p108">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span></span>
    
5. <span data-ttu-id="faf37-138">Geben Sie im Dialogfeld **Wörter oder Ausdrücke angeben** die folgenden häufig in Massen-E-Mails vorkommenden Ausdrücke nacheinander ein, und klicken Sie auf **OK**, sobald Sie fertig sind:</span><span class="sxs-lookup"><span data-stu-id="faf37-138">In the **specify words or phrases** dialog box, add the following phrases commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - `to change your preferences or unsubscribe`
    
   - `Modify email preferences or unsubscribe`
    
   - `This is a promotional email`
    
   - `You are receiving this email because you requested a subscription`
    
   - `click here to unsubscribe`
    
   - `You have received this email because you are subscribed`
    
   - `If you no longer wish to receive our email newsletter`
    
   - `to unsubscribe from this newsletter`
    
   - `If you have trouble viewing this email`
    
   - `This is an advertisement`
    
   - `you would like to unsubscribe or change your`
    
   - `view this email as a webpage`
    
   - `You are receiving this email because you are subscribed`
    
   <span data-ttu-id="faf37-139">Diese Liste ist kein vollständiger Satz von Ausdrücken, die in Massen-e-Mails enthalten sind. Weitere können bei Bedarf hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="faf37-139">This list isn't an exhaustive set of phrases found in bulk emails; more can be added or removed as needed.</span></span> <span data-ttu-id="faf37-140">Dies ist jedoch ein guter Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="faf37-140">However, it's a good starting point.</span></span>
    
6. <span data-ttu-id="faf37-141">Wählen Sie unter **Gehen Sie folgendermaßen vor...** die Option **Nachrichteneigenschaften ändern** \> **SCL-Bewertung (Spam Confidence Level) festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="faf37-141">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="faf37-142">Legen Sie im Dialogfeld **SCL angeben** den SCL auf **5**, **6** oder **9** fest, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="faf37-142">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="faf37-p110">Wenn der SCL auf 5 oder 6 festgelegt wird, wird die **Spam**-Aktion ausgeführt, und wenn der SCL auf 9 festgelegt wird, wird die Aktion **Nachricht mit hoher Spamwahrscheinlichkeit** ausgeführt, wie in der Inhaltsfilterrichtlinie konfiguriert. Der Dienst führt die in der Inhaltsfilterrichtlinie festgelegte Aktion aus. Die Standardaktion ist, die Nachricht an den Junk-E-Mail-Ordner der Empfänger zuzustellen. Es können allerdings, wie in [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) beschrieben, andere Aktionen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="faf37-p110">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   <span data-ttu-id="faf37-146">Wenn die Nachricht von der konfigurierten Aktion isoliert wird, anstatt Sie an den Junk-e-Mail-Ordner der Empfänger zu senden, wird die Nachricht an die Administrator Quarantäne als eine Übereinstimmung mit der Nachrichtenfluss Regel gesendet und ist nicht in der Spamquarantäne für Endbenutzer oder über Endbenutzer verfügbar. Spambenachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="faf37-146">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="faf37-147">Weitere Informationen zu SCL-Werten im Dienst finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="faf37-147">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>

8. <span data-ttu-id="faf37-148">Speichern Sie die Regel.</span><span class="sxs-lookup"><span data-stu-id="faf37-148">Save the rule.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="faf37-149">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="faf37-149">For more information</span></span>

[<span data-ttu-id="faf37-150">Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?</span><span class="sxs-lookup"><span data-stu-id="faf37-150">What's the difference between junk email and bulk email?</span></span>](what-s-the-difference-between-junk-email-and-bulk-email.md)

[<span data-ttu-id="faf37-151">BCL-Werte (Bulk Complaint Level)</span><span class="sxs-lookup"><span data-stu-id="faf37-151">Bulk Complaint Level values</span></span>](bulk-complaint-level-values.md)

[<span data-ttu-id="faf37-152">Konfigurieren von Spamfilterrichtlinien</span><span class="sxs-lookup"><span data-stu-id="faf37-152">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)

[<span data-ttu-id="faf37-153">Erweiterte Spam Filterungsoptionen</span><span class="sxs-lookup"><span data-stu-id="faf37-153">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
