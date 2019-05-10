---
title: Nicht überprüfter Absender
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Um zu verhindern, dass Phishing-Nachrichten zu Ihrem Postfach gelangen, überprüfen Outlook.com und Outlook im Web, ob der Absender der Empfänger ist und verdächtige Nachrichten als Junk-e-Mail kennzeichnet.
ms.openlocfilehash: 5d4315afb33964e7c466384366b7315287cf6298
ms.sourcegitcommit: d24f50347c671cf5d2d8afec2f80d37d18af8b5d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2019
ms.locfileid: "33867843"
---
# <a name="unverified-sender"></a><span data-ttu-id="7614b-103">Nicht überprüfter Absender</span><span class="sxs-lookup"><span data-stu-id="7614b-103">Unverified Sender</span></span>

<span data-ttu-id="7614b-104">Um zu verhindern, dass Phishing-Nachrichten zu Ihrem Postfach gelangen, überprüfen Outlook.com und Outlook im Web, ob der Absender der Empfänger ist und verdächtige Nachrichten als Junk-e-Mail kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="7614b-104">To prevent phishing messages from reaching your mailbox, Outlook.com and Outlook on the web verify that the sender is who they say they are and mark suspicious messages as junk email.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7614b-105">Wenn eine Nachricht als Phishing-Betrug gekennzeichnet ist, wird Outlook.com und Outlook im Web eine Warnung am oberen Rand der Seite angezeigt, aber alle Links in der Nachricht können weiterhin geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="7614b-105">When a message is marked as a phishing scam, Outlook.com and Outlook on the web display a warning at the top of the page, but any links in the message can still be opened.</span></span>

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a><span data-ttu-id="7614b-106">Wie kann ich eine verdächtige Nachricht im Posteingang identifizieren?</span><span class="sxs-lookup"><span data-stu-id="7614b-106">How can I identify a suspicious message in my inbox?</span></span>

<span data-ttu-id="7614b-107">Outlook.com und Outlook im Web zeigen Indikatoren an, wenn der Absender einer Nachricht nicht identifiziert werden kann, oder Ihre Identität unterscheidet sich von dem, was in der von-Adresse angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7614b-107">Outlook.com and Outlook on the web show indicators when the sender of a message either can't be identified or their identity is different from what you see in the From address.</span></span>

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a><span data-ttu-id="7614b-108">Verwalten der Nachrichten, die die nicht verifizierte Absender Behandlung erhalten</span><span class="sxs-lookup"><span data-stu-id="7614b-108">How to manage which messages receive the unverified sender treatment</span></span> 

<span data-ttu-id="7614b-109">Wenn Sie ein Office 365-Kunde sind, können Sie diese Funktion über das Security & Compliance Center verwalten.</span><span class="sxs-lookup"><span data-stu-id="7614b-109">If you are an Office 365 customer you can manage this feature through the Security & Compliance Center.</span></span> 

- <span data-ttu-id="7614b-110">Im Office 365 Security & Compliance Center können mandantenadministratoren die Funktion durch den Schutz vor Spoofing unter der Anti-Phishing-Richtlinie ein-oder ausschalten.</span><span class="sxs-lookup"><span data-stu-id="7614b-110">In the Office 365 Security & Compliance Center, tenant admins can turn the feature on, or off, through the Anti-spoofing protection under the Anti-Phish policy.</span></span> <span data-ttu-id="7614b-111">Darüber hinaus kann es über das Cmdlet Set-AntiPhishPolicy verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="7614b-111">Additionally, it can be managed through the ‘Set-AntiPhishPolicy’ cmdlet.</span></span> <span data-ttu-id="7614b-112">Weitere Informationen finden Sie unter Schutz vor Phishing in Office 365 und Set-AntiPhishPolicy.</span><span class="sxs-lookup"><span data-stu-id="7614b-112">For more details, see Anti-phishing protection in Office 365 and Set-AntiPhishPolicy.</span></span>

    ![Bearbeiten nicht authentifizierter Absender in der grafischen Benutzeroberfläche.](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- <span data-ttu-id="7614b-114">Wenn ein Administrator ein falsch positives Ergebnis ermittelt hat und ein Absender nicht die nicht verifizierte Absender Behandlung erhalten soll, können Sie eine der folgenden Aktionen ausführen, um den Absender der Spoof Intelligence-Zulassungsliste für Vortäuschungen hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="7614b-114">If an admin has identified a false positive, and a sender should not be receiving the unverified sender treatment they can take one of the following actions to add the sender to the Spoof Intelligence spoof allow list:</span></span>
        
    - <span data-ttu-id="7614b-115">Fügen Sie das Domänenpaar über Spoof Intelligence Insight hinzu.</span><span class="sxs-lookup"><span data-stu-id="7614b-115">Add the domain pair through the Spoof Intelligence Insight.</span></span> <span data-ttu-id="7614b-116">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise: Spoof Intelligence Insight</span><span class="sxs-lookup"><span data-stu-id="7614b-116">For more details, see Walkthrough: spoof intelligence insight</span></span>
                
    - <span data-ttu-id="7614b-117">Fügen Sie das Domänenpaar über das PhishFilterPolicy-Cmdlet hinzu.</span><span class="sxs-lookup"><span data-stu-id="7614b-117">Add the domain pair through the PhishFilterPolicy cmdlet.</span></span> <span data-ttu-id="7614b-118">Weitere Informationen finden Sie unter Set-PhishFilterPolicy und Schutz vor Spoofing in Office 365</span><span class="sxs-lookup"><span data-stu-id="7614b-118">For more details, see Set-PhishFilterPolicy and Anti-spoofing protection in Office 365</span></span>

<span data-ttu-id="7614b-119">Darüber hinaus wenden wir die nicht verifizierte Absender Behandlung nicht an, wenn Sie über eine Zulassungsliste für Administratoren an den Posteingang übermittelt wurde, einschließlich e-Mail-Transport Regeln (ETRs), sichere Domänenliste (Anti-Spam-Richtlinie), Liste sicherer Absender oder Benutzer hat diesen Benutzer als "sicheren Absender" in seinem Inbox.</span><span class="sxs-lookup"><span data-stu-id="7614b-119">Additionally, we do not apply the unverified sender treatment if it was delivered to the inbox via an admin allow list, including Email Transport Rules (ETRs), Safe Domain List (Anti-Spam Policy), Safe Sender List or a user has set this user as a “Safe Sender” in their inbox.</span></span>

### <a name="you-see-a--in-the-sender-image"></a><span data-ttu-id="7614b-120">Sie sehen ein '? ' im Absender Bild</span><span class="sxs-lookup"><span data-stu-id="7614b-120">You see a '?' in the sender image</span></span>

<span data-ttu-id="7614b-121">Wenn Outlook.com und Outlook im Web die Identität des Absenders nicht mithilfe von e-Mail-Authentifizierungstechniken überprüfen können, wird im Absender Foto ein "?" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7614b-121">When Outlook.com and Outlook on the web can't verify the identity of the sender using email authentication techniques, they display a '?' in the sender photo.</span></span> 

![Nachricht wurde nicht erfolgreich überprüft](media/message-did-not-pass-verification.jpg)

<span data-ttu-id="7614b-123">Nicht jede Nachricht, die sich nicht authentifizieren kann, ist bösartig.</span><span class="sxs-lookup"><span data-stu-id="7614b-123">Not every message that fails to authenticate is malicious.</span></span> <span data-ttu-id="7614b-124">Sie sollten jedoch bei der Interaktion mit Nachrichten, die sich nicht authentifizieren, vorsichtig sein, wenn Sie den Absender nicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="7614b-124">However, you should be careful about interacting with messages that don't authenticate if you don't recognize the sender.</span></span> <span data-ttu-id="7614b-125">Oder, wenn Sie einen Absender erkennen, der normalerweise kein "?" im Absender Bild hat, aber Sie plötzlich beginnen, ihn zu sehen, könnte dies ein Zeichen sein, dass der Absender gefälscht wird.</span><span class="sxs-lookup"><span data-stu-id="7614b-125">Or, if you recognize a sender that normally doesn't have a '?' in the sender image, but you suddenly start seeing it, that could be a sign the sender is being spoofed.</span></span>

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a><span data-ttu-id="7614b-126">Die Adresse des Absenders unterscheidet sich von der Absenderadresse</span><span class="sxs-lookup"><span data-stu-id="7614b-126">The sender's address is different than what appears in the From address</span></span>

<span data-ttu-id="7614b-127">Die e-Mail-Adresse, die in einer Nachricht angezeigt wird, unterscheidet sich häufig von dem, was Sie in der Absenderadresse sehen.</span><span class="sxs-lookup"><span data-stu-id="7614b-127">Frequently, the email address you see in a message is different than what you see in the From address.</span></span> <span data-ttu-id="7614b-128">Manchmal versuchen Phisher, Sie zu täuschen, dass der Absender eine andere Person als die ist, die Sie wirklich sind.</span><span class="sxs-lookup"><span data-stu-id="7614b-128">Sometimes phishers try to trick you into thinking that the sender is someone other than who they really are.</span></span>

<span data-ttu-id="7614b-129">Wenn Outlook.com und Outlook im Web einen Unterschied zwischen der tatsächlichen Adresse des Absenders und der Adresse der Absenderadresse feststellen, wird der tatsächliche Absender mit dem Via-Tag angezeigt, das unterstrichen wird.</span><span class="sxs-lookup"><span data-stu-id="7614b-129">When Outlook.com and Outlook on the web detect a difference between the sender's actual address and the address on the From address, they show the actual sender using the via tag, which will be underlined.</span></span>

![nicht überprüfter Absender-Alternativtext](media/unverified-sender-feature1.png)

<span data-ttu-id="7614b-131">In diesem Beispiel wird die sendende `suspicious.com` Domäne authentifiziert, aber der Absender `unknown@contoso.com` in der von-Adresse.</span><span class="sxs-lookup"><span data-stu-id="7614b-131">In this example, the sending domain `suspicious.com` is authenticated, but the sender put `unknown@contoso.com` in the From address.</span></span>

<span data-ttu-id="7614b-132">Nicht jede Nachricht mit einem Via-Tag ist misstrauisch.</span><span class="sxs-lookup"><span data-stu-id="7614b-132">Not every message with a via tag is suspicious.</span></span> <span data-ttu-id="7614b-133">Wenn Sie jedoch keine Nachricht mit einem Via-Tag erkennen, sollten Sie bei der Interaktion mit ihr vorsichtig sein.</span><span class="sxs-lookup"><span data-stu-id="7614b-133">However, if you don't recognize a message with a via tag, you should be cautious about interacting with it.</span></span>

<span data-ttu-id="7614b-134">In Outlook.com und im neuen Outlook im Web können Sie mit dem Mauszeiger auf den Namen oder die Adresse eines Absenders in der Nachrichtenliste zeigen, um die e-Mail-Adresse anzuzeigen, ohne die Nachricht öffnen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="7614b-134">In Outlook.com and the new Outlook on the web, you can hover your cursor over a sender's name or address in the message list to see their email address, without needing to open the message.</span></span>

![Erste Schritte mit OneDrive](media/get-started-with-onedrive-message.png)

<span data-ttu-id="7614b-136">Woher wissen Sie, ob Sie das neue Outlook im Web verwenden?</span><span class="sxs-lookup"><span data-stu-id="7614b-136">How do you know if you're using the new Outlook on the web?</span></span> <span data-ttu-id="7614b-137">Sehen Sie sich die folgenden Beispiele an:</span><span class="sxs-lookup"><span data-stu-id="7614b-137">See the following examples:</span></span>

![Outlook vs Office 365](media/outlook-vs-outlook365.png)

## <a name="frequently-asked-questions"></a><span data-ttu-id="7614b-139">Häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="7614b-139">Frequently asked questions</span></span>

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a><span data-ttu-id="7614b-140">Welche Kriterien werden von Outlook.com und Outlook im Web verwendet, um die Eigenschaften "?" und "Via" hinzuzufügen?</span><span class="sxs-lookup"><span data-stu-id="7614b-140">What criteria does Outlook.com and Outlook on the web use to add the '?' and the 'via' properties?</span></span>

<span data-ttu-id="7614b-141">Für die "?" im Absender Bild: Outlook.com erfordert, dass die Nachricht entweder SPF-oder DKIM-Authentifizierung übergibt.</span><span class="sxs-lookup"><span data-stu-id="7614b-141">For the '?' in the sender image:  Outlook.com requires that the message pass either SPF or DKIM authentication.</span></span> <span data-ttu-id="7614b-142">Weitere Informationen finden Sie unter [Einrichten von SPF in Office 365 zur](set-up-spf-in-office-365-to-help-prevent-spoofing.md) Verhinderung von Spoofing und [Verwenden von DKIM zum Überprüfen ausgehender e-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet](use-dkim-to-validate-outbound-email.md)werden.</span><span class="sxs-lookup"><span data-stu-id="7614b-142">For more details, see [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) and [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>

<span data-ttu-id="7614b-143">Für das via-Tag: Wenn sich die Domäne in der von-Adresse von der Domäne in der DKIM-Signatur oder von der SMTP-e-Mail von unterscheidet, zeigt Outlook.com die Domäne in einem dieser beiden Felder an (bevorzugt die DKIM-Signatur).</span><span class="sxs-lookup"><span data-stu-id="7614b-143">For the via tag: If the domain in the From address is different from the domain in the DKIM signature or the SMTP MAIL FROM, Outlook.com displays the domain in one of those two fields (preferring the DKIM signature).</span></span>

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a><span data-ttu-id="7614b-144">Können diese Eigenschaften mit IP-Zulässigkeit, Exchange-Transport Regel oder sicheren Absendern außer Kraft gesetzt werden?</span><span class="sxs-lookup"><span data-stu-id="7614b-144">Can I override these properties with IP Allows, Exchange Transport Rule Allows, or safe senders?</span></span>

<span data-ttu-id="7614b-145">Sie können diese Eigenschaften nicht außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="7614b-145">You can't override these properties.</span></span>

### <a name="how-do-i-remove-these-properties"></a><span data-ttu-id="7614b-146">Wie entferne ich diese Eigenschaften?</span><span class="sxs-lookup"><span data-stu-id="7614b-146">How do I remove these properties?</span></span>

<span data-ttu-id="7614b-147">Für das "?" im Absender Bild: als Absender sollten Sie Ihre Nachricht entweder mit SPF oder DKIM authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="7614b-147">For the '?' in the sender image: As a sender, you should authenticate your message with either SPF or DKIM.</span></span>

<span data-ttu-id="7614b-148">Für das via-Tag: als Absender sollten Sie sicherstellen, dass entweder die Domäne in der DKIM-Signatur oder die SMTP-e-Mail-Nachricht mit der Domäne in der von-Adresse identisch oder eine Unterdomäne ist.</span><span class="sxs-lookup"><span data-stu-id="7614b-148">For the via tag: As a sender, you should ensure that either the domain in the DKIM signature or the SMTP MAIL FROM is the same as, or is a subdomain of, the domain in the From address.</span></span>

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a><span data-ttu-id="7614b-149">Zeigt Outlook.com und Outlook im Web dies für jede Nachricht an, die die Authentifizierung nicht übergibt?</span><span class="sxs-lookup"><span data-stu-id="7614b-149">Does Outlook.com and Outlook on the web show this for every message that doesn’t pass authentication?</span></span>

<span data-ttu-id="7614b-150">Nicht unbedingt.</span><span class="sxs-lookup"><span data-stu-id="7614b-150">Not necessarily.</span></span> <span data-ttu-id="7614b-151">Outlook.com und Outlook im Web haben möglicherweise andere Eigenschaften in der Nachricht, um den Absender zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="7614b-151">Outlook.com and Outlook on the web may have other properties within the message to authenticate the sender.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7614b-152">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="7614b-152">Related topics</span></span>

[<span data-ttu-id="7614b-153">Schützen Ihres Outlook.com-e-Mail-Kontos</span><span class="sxs-lookup"><span data-stu-id="7614b-153">Help protect your Outlook.com email account</span></span>](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[<span data-ttu-id="7614b-154">Behandeln von Missbrauch, Phishing oder Spoofing in Outlook.com</span><span class="sxs-lookup"><span data-stu-id="7614b-154">Deal with abuse, phishing, or spoofing in Outlook.com</span></span>](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[<span data-ttu-id="7614b-155">Filtern von Junk-e-Mails und Spam in Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="7614b-155">Filter junk email and spam in Outlook on the web</span></span>](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
