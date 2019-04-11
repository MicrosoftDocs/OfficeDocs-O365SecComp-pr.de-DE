---
title: Optimieren des Schutzes gegen Phishing in Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Administratoren können erfahren, warum und wie Phishing-Nachrichten durchgemacht wurden und was Sie tun müssen, um künftig weitere Phishing-Nachrichten zu verhindern.
ms.openlocfilehash: efda9e16c23e4533b6951e43ac085b7640e84576
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2019
ms.locfileid: "30937822"
---
# <a name="tune-anti-phishing-protection-in-office-365"></a><span data-ttu-id="edf37-103">Optimieren des Schutzes gegen Phishing in Office 365</span><span class="sxs-lookup"><span data-stu-id="edf37-103">Tune anti-phishing protection in Office 365</span></span>

<span data-ttu-id="edf37-104">Obwohl Office 365 mit einer Vielzahl von Antiphishingfunktionen geliefert wird, die standardmäßig aktiviert sind, ist es möglich, dass einige Phishing-Nachrichten zu ihren Postfächern weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="edf37-104">Although Office 365 comes with a variety of anti-phishing features that are enabled by default, it's possible that some phishing messages could still get through to your mailboxes.</span></span> <span data-ttu-id="edf37-105">In diesem Thema wird beschrieben, was Sie tun können, um zu ermitteln, warum eine Phishing-Nachricht eingegangen ist und was Sie tun können, um die Einstellungen zum Schutz vor Phishing in Ihrer Exchange Online-Organisation zu ändern, _ohne dass sich dies versehentlich verschlechtert_.</span><span class="sxs-lookup"><span data-stu-id="edf37-105">This topic describes what you can do to discover why a phishing message got through, and what you can do to adjust the anti-phishing settings in your Exchange Online organization _without accidentally making things worse_.</span></span>

## <a name="first-things-first-deal-with-any-compromised-accounts-and-make-sure-you-block-any-more-phishing-messages-from-getting-through"></a><span data-ttu-id="edf37-106">Die ersten Schritte: befassen Sie sich mit kompromittierten Konten, und stellen Sie sicher, dass Sie keine weiteren Phishing-Nachrichten mehr blockieren.</span><span class="sxs-lookup"><span data-stu-id="edf37-106">First things first: deal with any compromised accounts and make sure you block any more phishing messages from getting through</span></span>

<span data-ttu-id="edf37-107">Wenn das Konto eines Empfängers aufgrund der Phishing-Nachricht kompromittiert wurde, befolgen Sie die Schritte unter [Antworten auf ein kompromittiertes e-Mail-Konto in Office 365](responding-to-a-compromised-email-account.md).</span><span class="sxs-lookup"><span data-stu-id="edf37-107">If a recipient's account was compromised as a result of the phishing message, follow the steps in [Responding to a compromised email account in Office 365](responding-to-a-compromised-email-account.md).</span></span>

<span data-ttu-id="edf37-108">Wenn Ihr Abonnement Advanced Threat Protection (ATP) enthält, können Sie mithilfe von [Office 365 Threat Intelligence](office-365-ti.md) andere Benutzer identifizieren, die auch die Phishing-Nachricht erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="edf37-108">If your subscription includes Advanced Threat Protection (ATP), you can use [Office 365 Threat Intelligence](office-365-ti.md) to identify other users who also received the phishing message.</span></span> <span data-ttu-id="edf37-109">Sie haben zusätzliche Optionen zum Blockieren von Phishing-Nachrichten:</span><span class="sxs-lookup"><span data-stu-id="edf37-109">You have additional options to block phishing messages:</span></span>

- [<span data-ttu-id="edf37-110">ATP-sichere Links</span><span class="sxs-lookup"><span data-stu-id="edf37-110">ATP Safe Links</span></span>](set-up-atp-safe-links-policies.md)

- [<span data-ttu-id="edf37-111">Sichere Anlagen in ATP</span><span class="sxs-lookup"><span data-stu-id="edf37-111">ATP Safe Attachments</span></span>](set-up-atp-safe-attachments-policies.md)

- <span data-ttu-id="edf37-112">[Anti-Phishing-Richtlinien für ATP](set-up-anti-phishing-policies.md).</span><span class="sxs-lookup"><span data-stu-id="edf37-112">[ATP anti-phishing policies](set-up-anti-phishing-policies.md).</span></span> <span data-ttu-id="edf37-113">Beachten Sie, dass Sie die **erweiterten Phishing-Schwellenwerte** in der Richtlinie von **Standard** auf **aggressiv**, \*\*\*\* aggressiver oder aggressiver erweitern können. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="edf37-113">Note that you can temporarily increase the **Advanced phishing thresholds** in the policy from **Standard** to **Aggressive**, **More aggressive**, or **Most aggressive**.</span></span>

<span data-ttu-id="edf37-114">Überprüfen Sie, ob diese ATP-Funktionen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="edf37-114">Verify these ATP features are turned on.</span></span>

## <a name="report-the-phishing-message-to-microsoft"></a><span data-ttu-id="edf37-115">Melden der Phishing-Nachricht an Microsoft</span><span class="sxs-lookup"><span data-stu-id="edf37-115">Report the phishing message to Microsoft</span></span>

<span data-ttu-id="edf37-116">Das Melden von Phishing-Nachrichten ist hilfreich beim Optimieren der Filter, die zum Schutz aller Kunden in Office 365 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="edf37-116">Reporting phishing messages is helpful in tuning the filters that are used to protect all customers in Office 365.</span></span>

<span data-ttu-id="edf37-117">Senden Sie die Phishing-Nachricht _als Anlage_ in einer neuen, ansonsten leeren nachricht an **Phish@office365.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="edf37-117">Send the phishing message _as an attachment_ in a new, otherwise empty message to **phish@office365.microsoft.com**.</span></span> <span data-ttu-id="edf37-118">Die ursprüngliche Nachricht nicht nur weiterleiten; Andernfalls können die ursprünglichen Nachrichtenkopfzeilen nicht untersucht werden.</span><span class="sxs-lookup"><span data-stu-id="edf37-118">Don't just forward the original message; otherwise, we can't examine the original message headers.</span></span> <span data-ttu-id="edf37-119">Sie können auch das [Berichtnachrichten](https://docs.microsoft.com/office365/securitycompliance/enable-the-report-message-add-in) -Add-in in Outlook oder Outlook im Web (früher als Outlook Web App bezeichnet) verwenden.</span><span class="sxs-lookup"><span data-stu-id="edf37-119">Or, you can use the [Report Message](https://docs.microsoft.com/office365/securitycompliance/enable-the-report-message-add-in) add-in in Outlook or Outlook on the web (formerly known as Outlook Web App).</span></span>

<span data-ttu-id="edf37-120">Weitere Informationen finden Sie unter [Übermitteln von Spam-, Nicht-Spamnachrichten und Nachrichten, die als betrügerische Phishing-Angriffe angesehen werden, an Microsoft zur Analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span><span class="sxs-lookup"><span data-stu-id="edf37-120">For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span>

## <a name="inspect-the-message-headers"></a><span data-ttu-id="edf37-121">ÜberPrüfen der Nachrichtenkopfzeilen</span><span class="sxs-lookup"><span data-stu-id="edf37-121">Inspect the message headers</span></span>

<span data-ttu-id="edf37-122">Sie können die Kopfzeilen der Phishing-Nachricht überprüfen, um festzustellen, ob es etwas gibt, was Sie selbst tun können, um zu verhindern, dass mehr Phishing-Nachrichten durchkommen.</span><span class="sxs-lookup"><span data-stu-id="edf37-122">You can examine the headers of the phishing message to see if there's anything that you can do yourself to prevent more phishing messages from coming through.</span></span> <span data-ttu-id="edf37-123">Mit anderen Worten: die Untersuchung der Kopfzeilen von Nachrichten kann Ihnen dabei helfen, Einstellungen in Ihrer Organisation zu identifizieren, die für das Zulassen der Phishing-Nachrichten verantwortlich waren.</span><span class="sxs-lookup"><span data-stu-id="edf37-123">In other words, examining the messages headers can help you identify any settings in your organization that were responsible for allowing the phishing messages in.</span></span>

<span data-ttu-id="edf37-124">Insbesondere sollten Sie das **X-Forefront-Antispam-Report-** Kopfzeilenfeld in den Nachrichtenkopfzeilen auf Hinweise zu übersprungenen Spam-oder Phishing-Filtern im SFV-Wert (Spamfilter Urteil) überprüfen.</span><span class="sxs-lookup"><span data-stu-id="edf37-124">Specifically, you should check the **X-Forefront-Antispam-Report** header field in the message headers for indications of skipped spam or phish filtering in the Spam Filtering Verdict (SFV) value.</span></span> <span data-ttu-id="edf37-125">Nachrichten, die die Filterung überspringen, `SCL:-1`haben einen Eintrag von, was besagt, dass eine Ihrer Einstellungen diese Nachricht durch Überschreiben der Spam-oder Phishing-Urteile erlaubt, die vom Dienst bestimmt wurden.</span><span class="sxs-lookup"><span data-stu-id="edf37-125">Messages that skip filtering will have an entry of `SCL:-1`, which means one of your settings allowed this message through by overriding the spam or phish verdicts that were determined by the service.</span></span> <span data-ttu-id="edf37-126">Weitere Informationen zum Abrufen von Nachrichtenkopfzeilen und eine vollständige Liste aller verfügbaren Antispam-und Antiphishing-Nachrichtenkopfzeilen finden Sie unter [Antispam-Nachrichtenkopfzeilen](https://docs.microsoft.com/office365/SecurityCompliance/anti-spam-message-headers).</span><span class="sxs-lookup"><span data-stu-id="edf37-126">For more details on how to get message headers and the complete list of all available anti-spam and anti-phish message headers, see [Anti-spam message headers](https://docs.microsoft.com/office365/SecurityCompliance/anti-spam-message-headers).</span></span>

## <a name="best-practices-to-stay-protected"></a><span data-ttu-id="edf37-127">Bewährte Methoden zum Schutz vor</span><span class="sxs-lookup"><span data-stu-id="edf37-127">Best practices to stay protected</span></span>

- <span data-ttu-id="edf37-128">Führen Sie auf monatlicher Basis [office 365 Secure Score](office-365-secure-score.md) aus, um die Sicherheitseinstellungen ihrer Office 365-Organisation zu bewerten.</span><span class="sxs-lookup"><span data-stu-id="edf37-128">On a monthly basis, run [Office 365 Secure Score](office-365-secure-score.md) to assess your Office 365 organization's security settings.</span></span>

- <span data-ttu-id="edf37-129">Überarbeiten Sie regelmäßig den [Spoof Intelligence-Bericht](learn-about-spoof-intelligence.md) , und aktivieren Sie den [Schutz vor Spoofing in der Anti-Phishing-Richtlinie](learn-about-spoof-intelligence.md#configuring-the-anti-spoofing-policy) , um verdächtige Nachrichten zu **isolieren** , anstatt Sie an den Junk-e-Mail-Ordner des Benutzers zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="edf37-129">Periodically review the [Spoof intelligence report](learn-about-spoof-intelligence.md) and [enable anti-spoofing protection in the anti-phishing policy](learn-about-spoof-intelligence.md#configuring-the-anti-spoofing-policy) to **quarantine** suspicious messages instead of delivering them to the user's Junk Email folder.</span></span>

- <span data-ttu-id="edf37-130">Überarbeiten Sie den [Status Bericht über Bedrohungen](view-reports-for-atp.md#threat-protection-status-report).</span><span class="sxs-lookup"><span data-stu-id="edf37-130">Periodically review the [Threat Protection Status report](view-reports-for-atp.md#threat-protection-status-report).</span></span>

- <span data-ttu-id="edf37-131">Einige Kunden lassen versehentlich Phishing-Nachrichten durch, indem Sie Ihre eigenen Domänen in der Liste Absender oder zugelassene Domäne in Anti-Spam-Richtlinien platzieren.</span><span class="sxs-lookup"><span data-stu-id="edf37-131">Some customers inadvertently allow phishing messages through by putting their own domains in the Allow sender or Allow domain list in anti-spam policies.</span></span> <span data-ttu-id="edf37-132">Wenn Sie dies tun, müssen Sie äußerste Vorsicht walten lassen.</span><span class="sxs-lookup"><span data-stu-id="edf37-132">If you choose to do this, you must use extreme caution.</span></span> <span data-ttu-id="edf37-133">Diese Konfiguration erlaubt zwar einige legitime Nachrichten, aber auch schädliche Nachrichten, die normalerweise durch die Office 365-Spam-und/oder Phishing-Filter blockiert würden.</span><span class="sxs-lookup"><span data-stu-id="edf37-133">Although this configuration will allow some legitimate messages through, it will also allow malicious messages that would normally be blocked by the Office 365 spam and/or phish filters.</span></span>

  <span data-ttu-id="edf37-134">Die beste Möglichkeit für den Umgang mit legitimen Nachrichten, die von Office 365 (falsch positive) blockiert werden und Absender in Ihrer Domäne betreffen, besteht darin, die SPF-, DKIM-und DMARC-Einträge in DNS für _alle_ e-Mail-Domänen in Office 365 vollständig und vollständig zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="edf37-134">The best way to deal with legitimate messages that are blocked by Office 365 (false positives) that involve senders in your domain is to fully and completely configure the SPF, DKIM, and DMARC records in DNS for _all_ of your email domains in Office 365:</span></span>

  - <span data-ttu-id="edf37-135">Stellen Sie sicher, dass Ihr SPF-Eintrag _alle_ e-Mail-Quellen für Absender in Ihrer Domäne identifiziert (Drittanbieterdienste nicht vergessen!).</span><span class="sxs-lookup"><span data-stu-id="edf37-135">Verify that your SPF record identifies _all_ sources of email for senders in your domain (don't forget third-party services!).</span></span>

  - <span data-ttu-id="edf37-136">Verwenden Sie Hard Fail\-(), um sicherzustellen, dass unbefugte Absender von e-Mail-Systemen, die so konfiguriert sind, abgelehnt werden.</span><span class="sxs-lookup"><span data-stu-id="edf37-136">Use hard fail (\-) to ensure that unauthorized senders are rejected by email systems that are configured to do so.</span></span> <span data-ttu-id="edf37-137">Sie können [Spoof Intelligence](https://docs.microsoft.com/office365/securitycompliance/learn-about-spoof-intelligence) verwenden, um Absender zu identifizieren, die Ihre Domäne verwenden, damit Sie autorisierte Drittanbieter Absender in ihren SPF-Eintrag aufnehmen können.</span><span class="sxs-lookup"><span data-stu-id="edf37-137">You can use [spoof intelligence](https://docs.microsoft.com/office365/securitycompliance/learn-about-spoof-intelligence) to help identify senders that are using your domain so that you can include authorized third-party senders in your SPF record.</span></span>

  <span data-ttu-id="edf37-138">Konfigurationsanweisungen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="edf37-138">For configuration instructions, see:</span></span>
  
  - [<span data-ttu-id="edf37-139">Einrichten von SPF in Office 365 zum Verhindern von Spoofing</span><span class="sxs-lookup"><span data-stu-id="edf37-139">Set up SPF in Office 365 to help prevent spoofing</span></span>](set-up-spf-in-office-365-to-help-prevent-spoofing.md)

  - [<span data-ttu-id="edf37-140">Verwenden von DKIM zum Überprüfen ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet werden</span><span class="sxs-lookup"><span data-stu-id="edf37-140">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md)

  - [<span data-ttu-id="edf37-141">Verwenden von DMARC zum Überprüfen von e-Mails in Office 365</span><span class="sxs-lookup"><span data-stu-id="edf37-141">Use DMARC to validate email in Office 365</span></span>](use-dmarc-to-validate-email.md)

- <span data-ttu-id="edf37-142">Es wird empfohlen, nach Möglichkeit e-Mails für Ihre Domäne direkt an Office 365 zu senden.</span><span class="sxs-lookup"><span data-stu-id="edf37-142">Whenever possible, we recommend that you deliver email for your domain directly to Office 365.</span></span> <span data-ttu-id="edf37-143">Zeigen Sie mit anderen Worten den MX-Eintrag Ihrer Office 365-Domäne auf Office 365.</span><span class="sxs-lookup"><span data-stu-id="edf37-143">In other words, point your Office 365 domain's MX record to Office 365.</span></span> <span data-ttu-id="edf37-144">Exchange Online Protection (EOP) ist in der Lage, den bestmöglichen Schutz für Ihre Cloud-Benutzer bereitzustellen, wenn Ihre e-Mails direkt an Office 365 zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="edf37-144">Exchange Online Protection (EOP) is able to provide the best protection for your cloud users when their mail is delivered directly to Office 365.</span></span> <span data-ttu-id="edf37-145">Wenn Sie ein Drittanbieter-e-Mail-Hygienesystem vor EOP verwenden müssen, stellen Sie sicher, dass Sie die Anweisungen [hier](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-mail-flow-using-third-party-cloud)befolgt haben.</span><span class="sxs-lookup"><span data-stu-id="edf37-145">If you must use a third-party email hygiene system in front of EOP, ensure you have followed the guidance [here](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-mail-flow-using-third-party-cloud).</span></span>

- <span data-ttu-id="edf37-146">Die Multi-Factor-Authentifizierung (MFA) ist eine wirklich gute Möglichkeit, um kompromittierte Konten zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="edf37-146">Multi factor authentication (MFA) is a really good way to prevent compromised accounts.</span></span> <span data-ttu-id="edf37-147">Sie sollten unbedingt die Aktivierung von MFA für alle Ihre Benutzer erwägen.</span><span class="sxs-lookup"><span data-stu-id="edf37-147">You should strongly consider enabling MFA for all of your users.</span></span> <span data-ttu-id="edf37-148">Beginnen Sie bei einem phasenweisen Ansatz, indem Sie MFA für die sensibelsten Benutzer (Administratoren, Führungskräfte usw.) aktivieren, bevor Sie MFA für alle aktivieren.</span><span class="sxs-lookup"><span data-stu-id="edf37-148">For a phased approach, start by enabling MFA for your most sensitive users (admins, executives, etc.) before you enable MFA for everyone.</span></span> <span data-ttu-id="edf37-149">Weitere Informationen finden Sie unter [Einrichten der mehr](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication)stufigen Authentifizierung.</span><span class="sxs-lookup"><span data-stu-id="edf37-149">For instructions, see [Set up multi-factor authentication](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication).</span></span>

- <span data-ttu-id="edf37-150">WeiterLeitungsregeln an externe Empfänger werden häufig von Angreifern zum Extrahieren von Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="edf37-150">Forwarding rules to external recipients are often used by attackers to extract data.</span></span> <span data-ttu-id="edf37-151">Verwenden Sie die Informationen zum Überwachen von **Post Fach Weiterleitungsregeln** in [Office 365 Secure Score](office-365-secure-score.md) , um Weiterleitungsregeln an externe Empfänger zu finden und sogar zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="edf37-151">Use the **Review mailbox forwarding rules** information in [Office 365 Secure Score](office-365-secure-score.md) to find and even prevent forwarding rules to external recipients.</span></span> <span data-ttu-id="edf37-152">Weitere Informationen finden Sie unter [mildernde Client External forwardIng Rules with Secure Score](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/).</span><span class="sxs-lookup"><span data-stu-id="edf37-152">For more information, see [Mitigating Client External Forwarding Rules with Secure Score](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/).</span></span>