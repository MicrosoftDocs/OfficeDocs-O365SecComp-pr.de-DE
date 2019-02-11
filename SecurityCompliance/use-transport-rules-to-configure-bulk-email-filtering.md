---
title: Verwenden von e-Mail-Flussregeln zum Konfigurieren von Massen-e-Mail-Filterung in Exchange Online Protection
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2889c82e-fab0-4e85-87b0-b001b2ccd4f7
description: Administratoren können erfahren Sie, wie Sie e-Mail-Flussregeln in Exchange Online Protection für Massen-e-Mail-Filterung verwenden.
ms.openlocfilehash: ce95872d3d80436dce4c62037caea9a5f735726d
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "27382806"
---
# <a name="use-mail-flow-rules-to-configure-bulk-email-filtering-in-exchange-online-protection"></a><span data-ttu-id="89acd-103">Verwenden von e-Mail-Flussregeln zum Konfigurieren von Massen-e-Mail-Filterung in Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="89acd-103">Use mail flow rules to configure bulk email filtering in Exchange Online Protection</span></span>

<span data-ttu-id="89acd-p101">Sie können den unternehmensweiten Inhaltsfilter für Spam und Massen-E-Mails über die Standardrichtlinien für die Spam-Inhaltsfilterung festlegen. Informationen zum Festlegen der Richtlinien für die Inhaltsfilterung finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) und [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx).</span><span class="sxs-lookup"><span data-stu-id="89acd-p101">You can set company-wide content filters for spam and bulk email using the default spam content-filter policies. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) and [Set-HostedContentFilterPolicy](http://technet.microsoft.com/library/f597aa65-baa7-49d0-8832-2a300073f211.aspx) on how to set the content filter policies.</span></span> 
  
<span data-ttu-id="89acd-p102">Wenn Sie weitere Optionen zum Filtern von Massennachrichten möchten, können Sie e-Mail-Flussregeln (auch als Transportregeln bezeichnet) zum Suchen nach Textmustern oder Phrasen, die häufig in Massen-e-Mails erstellen. Alle Nachrichten, die diese Merkmale aufweisen wird als Spam gekennzeichnet. Mithilfe dieser Regeln hilft bei der Reduzierung des unerwünschte Massen-e-Mail, die Ihre Organisation empfängt.</span><span class="sxs-lookup"><span data-stu-id="89acd-p102">If you want to more options to filter bulk messages, you can create mail flow rules (also known as transport rules) to search for text patterns or phrases frequently found in bulk emails. Any message containing these characteristics will be marked as spam. Using these rules can help reduce the amount of unwanted bulk email your organization receives.</span></span>
  
<span data-ttu-id="89acd-109">**Hinweise**:</span><span class="sxs-lookup"><span data-stu-id="89acd-109">**Notes**:</span></span>

- <span data-ttu-id="89acd-110">Vor dem Erstellen der Mail Flow Regeln in diesem Thema dokumentiert, es wird empfohlen, zunächst das Thema [Was ist der Unterschied zwischen Junk-e-Mail und Massen-e-Mail?](what-s-the-difference-between-junk-email-and-bulk-email.md) und [Massen kompatibles Ebene Werte](bulk-complaint-level-values.md).</span><span class="sxs-lookup"><span data-stu-id="89acd-110">Before creating the mail flow rules documented this topic, we recommend that you first read [What's the difference between junk email and bulk email?](what-s-the-difference-between-junk-email-and-bulk-email.md) and [Bulk Complaint Level values](bulk-complaint-level-values.md).</span></span> 
  
- <span data-ttu-id="89acd-p103">Durch die folgenden Verfahren wird eine Nachricht für Ihre gesamte Organisation als Spam markiert. Sie können jedoch eine andere Bedingung hinzufügen, damit diese Regeln nur für bestimmte Empfänger in Ihrer Organisation gelten. Auf diese Weise können die aggressiven Filtereinstellungen für Massen-E-Mails nur für einige wenige Benutzer gelten, die verstärkt anvisiert werden, während der Rest Ihrer Benutzer (die zumeist die Massen-E-Mails erhalten, für die sie sich registriert haben) nicht betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="89acd-p103">The following procedures mark a message as spam for your entire organization. However, you can add another condition to apply these rules only to specific recipients in your organization. This way, the aggressive bulk email filtering settings can apply to a few users who are highly targeted, while the rest of your users (who mostly get the bulk email they signed up for) aren't impacted.</span></span> 
  
### <a name="create-mail-flow-rule-to-filter-bulk-email-messages-based-on-text-patterns"></a><span data-ttu-id="89acd-114">Erstellen von e-Mail-Flussregel zum Filtern von Massen-e-Mails basierend auf Textmustern</span><span class="sxs-lookup"><span data-stu-id="89acd-114">Create mail flow rule to filter bulk email messages based on text patterns</span></span>

1. <span data-ttu-id="89acd-115">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="89acd-115">In the Exchange admin center (EAC), go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="89acd-116">Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und wählen Sie dann **Neue Regel erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="89acd-116">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="89acd-117">Geben Sie einen Namen für die Regel ein.</span><span class="sxs-lookup"><span data-stu-id="89acd-117">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="89acd-p104">Klicken Sie auf **Weitere Optionen**. Aktivieren Sie unter **Diese Regel anwenden, wenn,** die Option **Betreff oder Nachrichtentext** \> **Betreff oder Nachrichtentext entspricht diesen Textmustern**.</span><span class="sxs-lookup"><span data-stu-id="89acd-p104">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body matches these text patterns**.</span></span>
    
5. <span data-ttu-id="89acd-120">Geben Sie im Dialogfeld **Wörter oder Ausdrücke angeben** die folgenden häufig in Massen-E-Mails vorkommenden regulären Ausdrücke nacheinander ein, und klicken Sie auf **OK**, sobald Sie fertig sind:</span><span class="sxs-lookup"><span data-stu-id="89acd-120">In the **specify words or phrases** dialog box, add the following regular expressions commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="89acd-121">Wenn Sie den Inhalt dieser E-Mail nicht anzeigen können\,</span><span class="sxs-lookup"><span data-stu-id="89acd-121">If you are unable to view the content of this email\, please</span></span>
    
   - <span data-ttu-id="89acd-122">\\>(sicher )?melden Sie sich ab( hier)?\\</a\\></span><span class="sxs-lookup"><span data-stu-id="89acd-122">\\>(safe )?unsubscribe( here)?\\</a\\></span></span>
    
   - <span data-ttu-id="89acd-123">Wenn Sie keine weitere Kommunikation dieser Art mehr erhalten möchten\,</span><span class="sxs-lookup"><span data-stu-id="89acd-123">If you do not wish to receive further communications like this\, please</span></span>
    
   - <span data-ttu-id="89acd-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span><span class="sxs-lookup"><span data-stu-id="89acd-p105">\\<img height\="?1"? width\="?1"? src\=.?http\://</span></span>
    
   - <span data-ttu-id="89acd-127">So beenden Sie die empfangen von \s+e-mails\:http\ -e-Mails\:http\://</span><span class="sxs-lookup"><span data-stu-id="89acd-127">To stop receiving these\s+emails\:http\://</span></span>
    
   - <span data-ttu-id="89acd-128">Um \w+ (E\-?Brief|E?-?Mail|Newsletter) abzubestellen</span><span class="sxs-lookup"><span data-stu-id="89acd-128">To unsubscribe from \w+ (e\-?letter|e?-?mail|newsletter)</span></span>
    
   - <span data-ttu-id="89acd-129">keine \w+ E-Mail (mehr )?(gesendet bekommen möchten|erhalten möchten)</span><span class="sxs-lookup"><span data-stu-id="89acd-129">no longer (wish )?(to )?(be sent|receive) \w+ email</span></span>
    
   - <span data-ttu-id="89acd-130">Wenn Sie den Inhalt dieser E-Mail nicht anzeigen können\, klicken Sie hier</span><span class="sxs-lookup"><span data-stu-id="89acd-130">If you are unable to view the content of this email\, please click here</span></span>
    
   - <span data-ttu-id="89acd-131">Um sicherzustellen, dass (Ihre täglichen Geschäfte | unsere e-?mails)\, hinzufügen</span><span class="sxs-lookup"><span data-stu-id="89acd-131">To ensure you receive (your daily deals|our e-?mails)\, add</span></span>
    
   - <span data-ttu-id="89acd-132">Wenn Sie diese E-Mails nicht mehr erhalten möchten</span><span class="sxs-lookup"><span data-stu-id="89acd-132">If you no longer wish to receive these emails</span></span>
    
   - <span data-ttu-id="89acd-133">um Ihre (Abonnementeinstellungen zu ändern|Einstellungen zu ändern oder sich abzumelden)</span><span class="sxs-lookup"><span data-stu-id="89acd-133">to change your (subscription preferences|preferences or unsubscribe)</span></span>
    
   - <span data-ttu-id="89acd-134">klicken Sie (hier zum|auf) Abmelden</span><span class="sxs-lookup"><span data-stu-id="89acd-134">click (here to|the) unsubscribe</span></span>
    
   <span data-ttu-id="89acd-135">**Hinweise**:</span><span class="sxs-lookup"><span data-stu-id="89acd-135">**Notes**:</span></span>

   - <span data-ttu-id="89acd-p106">Die obige Liste keine vollständige Reihe von regulären Ausdrücken in Massen-e-Mails. Weitere können je nach Bedarf hinzugefügt oder entfernt werden. Es ist jedoch einen guten Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="89acd-p106">The above list isn't an exhaustive set of regular expressions found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
   - <span data-ttu-id="89acd-p107">Die Suche nach Wörtern oder Textmustern im Betreff oder anderen Kopffelder in der Nachricht tritt auf, *nachdem* die Nachricht aus der MIME-Content-Übertragung Codierung zum Übertragen der binären Nachricht zwischen SMTP-Server in ASCII-Text verwendete Methode decodiert wurden. Sie können Bedingungen oder Ausnahmen für die Suche (in der Regel Base64)-codierten Werte der Betreff oder anderen Kopffelder in Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="89acd-p107">The search for words or text patterns in the subject or other header fields in the message occurs  *after*  the message has been decoded from the MIME content transfer encoding method that was used to transmit the binary message between SMTP servers in ASCII text. You can't use conditions or exceptions to search for the raw (typically, Base64) encoded values of the subject or other header fields in messages.</span></span> 
    
6. <span data-ttu-id="89acd-140">Wählen Sie unter **Gehen Sie folgendermaßen vor...** die Option **Nachrichteneigenschaften ändern** \> **SCL-Bewertung (Spam Confidence Level) festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="89acd-140">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="89acd-141">Legen Sie im Dialogfeld **SCL angeben** den SCL auf **5**, **6** oder **9** fest, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="89acd-141">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="89acd-p108">Wenn der SCL auf 5 oder 6 festgelegt wird, wird die **Spam**-Aktion ausgeführt, und wenn der SCL auf 9 festgelegt wird, wird die Aktion **Nachricht mit hoher Spamwahrscheinlichkeit** ausgeführt, wie in der Inhaltsfilterrichtlinie konfiguriert. Der Dienst führt die in der Inhaltsfilterrichtlinie festgelegte Aktion aus. Die Standardaktion ist, die Nachricht an den Junk-E-Mail-Ordner der Empfänger zuzustellen. Es können allerdings, wie in [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) beschrieben, andere Aktionen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="89acd-p108">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="89acd-145">Wenn Ihre konfigurierte Aktion zum Isolieren der Nachricht, anstatt an den Empfänger Junk-e-Mail-Ordner senden, wird die Nachricht in Quarantäne Administrator gesendet werden als Übereinstimmung mit einer e-Mail-Fluss und kann nicht in der Endbenutzer-Spamquarantäne oder über die Endbenutzer verfügbar ist Spam-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="89acd-145">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="89acd-146">Weitere Informationen zu SCL-Werten im Dienst finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="89acd-146">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>
    
8. <span data-ttu-id="89acd-147">Speichern Sie die Regel.</span><span class="sxs-lookup"><span data-stu-id="89acd-147">Save the rule.</span></span>
    
### <a name="create-a-mail-flow-rule-to-filter-bulk-email-messages-based-on-phrases"></a><span data-ttu-id="89acd-148">Erstellen einer e-Mail-Flussregel zum Filtern von Massen-e-Mails basierend auf Ausdrücken</span><span class="sxs-lookup"><span data-stu-id="89acd-148">Create a mail flow rule to filter bulk email messages based on phrases</span></span>

1. <span data-ttu-id="89acd-149">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="89acd-149">In the EAC, go to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="89acd-150">Klicken Sie auf **Hinzufügen**![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif), und wählen Sie dann **Neue Regel erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="89acd-150">Click **Add**![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="89acd-151">Geben Sie einen Namen für die Regel ein.</span><span class="sxs-lookup"><span data-stu-id="89acd-151">Specify a name for the rule.</span></span>
    
4. <span data-ttu-id="89acd-p109">Klicken Sie auf **Weitere Optionen**. Wählen Sie unter **diese Regel anwenden, wenn** **der Betreff oder Nachrichtentext** \> **Betreff oder Nachrichtentext enthält eines dieser Wörter**.</span><span class="sxs-lookup"><span data-stu-id="89acd-p109">Click **More options**. Under **Apply this rule if**, select **The subject or body** \> **subject or body includes any of these words**.</span></span>
    
5. <span data-ttu-id="89acd-154">Geben Sie im Dialogfeld **Wörter oder Ausdrücke angeben** die folgenden häufig in Massen-E-Mails vorkommenden Ausdrücke nacheinander ein, und klicken Sie auf **OK**, sobald Sie fertig sind:</span><span class="sxs-lookup"><span data-stu-id="89acd-154">In the **specify words or phrases** dialog box, add the following phrases commonly found in bulk emails, one at a time, and click **ok** when you're done:</span></span> 
    
   - <span data-ttu-id="89acd-155">zum Ändern Ihrer Einstellungen oder Abmelden</span><span class="sxs-lookup"><span data-stu-id="89acd-155">to change your preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="89acd-156">Ändern Sie Ihre E-Mail-Einstellungen, oder melden Sie sich ab</span><span class="sxs-lookup"><span data-stu-id="89acd-156">Modify email preferences or unsubscribe</span></span>
    
   - <span data-ttu-id="89acd-157">Dies ist eine Werbe-E-Mail</span><span class="sxs-lookup"><span data-stu-id="89acd-157">This is a promotional email</span></span>
    
   - <span data-ttu-id="89acd-158">Sie erhalten diese E-Mail, da Sie ein Abonnement angefordert haben</span><span class="sxs-lookup"><span data-stu-id="89acd-158">You are receiving this email because you requested a subscription</span></span>
    
   - <span data-ttu-id="89acd-159">klicken Sie hier, um sich abzumelden</span><span class="sxs-lookup"><span data-stu-id="89acd-159">click here to unsubscribe</span></span>
    
   - <span data-ttu-id="89acd-160">Sie haben diese E-Mail erhalten, da Sie sich dafür angemeldet haben</span><span class="sxs-lookup"><span data-stu-id="89acd-160">You have received this email because you are subscribed</span></span>
    
   - <span data-ttu-id="89acd-161">Wenn Sie unseren E-Mail-Newsletter nicht mehr erhalten möchten</span><span class="sxs-lookup"><span data-stu-id="89acd-161">If you no longer wish to receive our email newsletter</span></span>
    
   - <span data-ttu-id="89acd-162">melden Sie sich von diesem Newsletter ab</span><span class="sxs-lookup"><span data-stu-id="89acd-162">to unsubscribe from this newsletter</span></span>
    
   - <span data-ttu-id="89acd-163">Wenn Sie Probleme haben, diese E-Mail anzuzeigen</span><span class="sxs-lookup"><span data-stu-id="89acd-163">If you have trouble viewing this email</span></span>
    
   - <span data-ttu-id="89acd-164">Dies ist eine Werbeanzeige</span><span class="sxs-lookup"><span data-stu-id="89acd-164">This is an advertisement</span></span>
    
   - <span data-ttu-id="89acd-165">möchten Sie sich abmelden oder Ihre Adresse ändern</span><span class="sxs-lookup"><span data-stu-id="89acd-165">you would like to unsubscribe or change your</span></span>
    
   - <span data-ttu-id="89acd-166">Diese E-Mail als Webseite anzeigen</span><span class="sxs-lookup"><span data-stu-id="89acd-166">view this email as a webpage</span></span>
    
   - <span data-ttu-id="89acd-167">Sie erhalten diese E-Mail, da Sie sich dafür angemeldet haben</span><span class="sxs-lookup"><span data-stu-id="89acd-167">You are receiving this email because you are subscribed</span></span>
    
   <span data-ttu-id="89acd-p110">**Hinweis**: erneut, diese Liste ist eine umfassende Gruppe von Ausdrücke in Massen-e-Mails; nicht Weitere können je nach Bedarf hinzugefügt oder entfernt werden. Es ist jedoch einen guten Ausgangspunkt.</span><span class="sxs-lookup"><span data-stu-id="89acd-p110">**Note**: Once again, this list isn't an exhaustive set of phrases found in bulk emails; more can be added or removed as needed. However, it's a good starting point.</span></span>
    
6. <span data-ttu-id="89acd-170">Wählen Sie unter **Gehen Sie folgendermaßen vor...** die Option **Nachrichteneigenschaften ändern** \> **SCL-Bewertung (Spam Confidence Level) festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="89acd-170">Under **Do the following**, select **Modify the message properties** \> **set the spam confidence level (SCL)**.</span></span>
    
7. <span data-ttu-id="89acd-171">Legen Sie im Dialogfeld **SCL angeben** den SCL auf **5**, **6** oder **9** fest, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="89acd-171">In the **specify SCL** dialog box, set the SCL to **5**, **6**, or **9**, and click **ok**.</span></span>
    
   <span data-ttu-id="89acd-p111">Wenn der SCL auf 5 oder 6 festgelegt wird, wird die **Spam**-Aktion ausgeführt, und wenn der SCL auf 9 festgelegt wird, wird die Aktion **Nachricht mit hoher Spamwahrscheinlichkeit** ausgeführt, wie in der Inhaltsfilterrichtlinie konfiguriert. Der Dienst führt die in der Inhaltsfilterrichtlinie festgelegte Aktion aus. Die Standardaktion ist, die Nachricht an den Junk-E-Mail-Ordner der Empfänger zuzustellen. Es können allerdings, wie in [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md) beschrieben, andere Aktionen konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="89acd-p111">Setting the SCL to 5 or 6 takes the **Spam** action, while setting the SCL to 9 takes the **High confidence spam** action, as configured in the content filter policy. The service will perform the action set in the content filter policy. The default action is to deliver the message to the recipients' Junk Email folder, but different actions can be configured as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="89acd-175">Wenn Ihre konfigurierte Aktion zum Isolieren der Nachricht, anstatt an den Empfänger Junk-e-Mail-Ordner senden, wird die Nachricht in Quarantäne Administrator gesendet werden als Übereinstimmung mit einer e-Mail-Fluss und kann nicht in der Endbenutzer-Spamquarantäne oder über die Endbenutzer verfügbar ist Spam-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="89acd-175">If your configured action is to quarantine the message rather than send it to the recipients' Junk Email folder, the message will be sent to the administrator quarantine as a mail flow rule match, and it will not be available in the end user spam quarantine or via end-user spam notifications.</span></span> 
  
   <span data-ttu-id="89acd-176">Weitere Informationen zu SCL-Werten im Dienst finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).</span><span class="sxs-lookup"><span data-stu-id="89acd-176">For more information about SCL values in the service, see [Spam confidence levels](spam-confidence-levels.md).</span></span>

8. <span data-ttu-id="89acd-177">Speichern Sie die Regel.</span><span class="sxs-lookup"><span data-stu-id="89acd-177">Save the rule.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="89acd-178">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="89acd-178">For more information</span></span>

[<span data-ttu-id="89acd-179">Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?</span><span class="sxs-lookup"><span data-stu-id="89acd-179">What's the difference between junk email and bulk email?</span></span>](what-s-the-difference-between-junk-email-and-bulk-email.md)

[<span data-ttu-id="89acd-180">BCL-Werte (Bulk Complaint Level)</span><span class="sxs-lookup"><span data-stu-id="89acd-180">Bulk Complaint Level values</span></span>](bulk-complaint-level-values.md)

[<span data-ttu-id="89acd-181">Konfigurieren von Spamfilterrichtlinien</span><span class="sxs-lookup"><span data-stu-id="89acd-181">Configure your spam filter policies</span></span>](configure-your-spam-filter-policies.md)

[<span data-ttu-id="89acd-182">Erweiterte spamfilterungsoptionen</span><span class="sxs-lookup"><span data-stu-id="89acd-182">Advanced spam filtering  options</span></span>](advanced-spam-filtering-asf-options.md)
