---
title: Verwenden von DMARC zum Überprüfen von E-Mails in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.custom: TN2DMC
ms.assetid: 4a05898c-b8e4-4eab-bd70-ee912e349737
description: Informationen Sie zum Konfigurieren von domänenbasierten Nachrichtenauthentifizierung, Berichte und Konformität (DMARC) zum Überprüfen von Office 365-Organisation gesendeten Nachrichten.
ms.openlocfilehash: 2f8e712028b5b5ee8950b48780083a20c7dce6ab
ms.sourcegitcommit: bd1762ccf63c7d2ad8b49a936115171c72fb2c0f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "27750044"
---
# <a name="use-dmarc-to-validate-email-in-office-365"></a><span data-ttu-id="ca190-103">Verwenden von DMARC zum Überprüfen von E-Mails in Office 365</span><span class="sxs-lookup"><span data-stu-id="ca190-103">Use DMARC to validate email in Office 365</span></span>

<span data-ttu-id="ca190-p101">Domänenbasierte Authentifizierung von Nachrichten, Berichte und Konformität ([DMARC](https://dmarc.org)) arbeitet mit Sender Policy Framework (SPF) und DomainKeys Identified Mail (DKIM) zur Authentifizierung von e-Mail-Absender und sicherzustellen, dass Zielsysteme e-Mail-Nachrichten von vertrauen Ihre Domäne. Implementieren von DMARC mit SPF und DKIM bietet zusätzlichen Schutz gegen spoofing und Phishing-e-Mail. Fail SPF oder DKIM prüft DMARC hilft Empfang von e-Mail-Systemen feststellen, welche Aktionen mit Nachrichten von Ihrer Domäne gesendete.</span><span class="sxs-lookup"><span data-stu-id="ca190-p101">Domain-based Message Authentication, Reporting, and Conformance ([DMARC](https://dmarc.org)) works with Sender Policy Framework (SPF) and DomainKeys Identified Mail (DKIM) to authenticate mail senders and ensure that destination email systems trust messages sent from your domain. Implementing DMARC with SPF and DKIM provides additional protection against spoofing and phishing email. DMARC helps receiving mail systems determine what to do with messages sent from your domain that fail SPF or DKIM checks.</span></span>
  
## <a name="how-do-spf-and-dmarc-work-together-to-protect-email-in-office-365"></a><span data-ttu-id="ca190-107">Wie arbeiten SPF und DMARC zusammen, um E-Mails in Office 365 zu schützen?</span><span class="sxs-lookup"><span data-stu-id="ca190-107">How do SPF and DMARC work together to protect email in Office 365?</span></span>
<span data-ttu-id="ca190-108"><a name="SPFandDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-108"></span></span>

 <span data-ttu-id="ca190-p102">Eine E-Mail-Nachricht kann mehrere Ersteller- oder Absenderadressen enthalten. Diese Adressen können für verschiedene Zwecke verwendet werden. Sehen Sie sich beispielsweise die folgenden Adressen an:</span><span class="sxs-lookup"><span data-stu-id="ca190-p102">An email message may contain multiple originator, or sender, addresses. These addresses are used for different purposes. For example, consider these addresses:</span></span> 
  
- <span data-ttu-id="ca190-p103">**"Mail From" Adresse**: identifiziert den Absender und gibt an, wohin return Benachrichtigungen senden, wenn Probleme mit der Zustellung der Nachricht, wie ein Unzustellbarkeitsbericht Mitteilungen auftreten. Dies wird in den Umschlag Teil einer e-Mail-Nachricht angezeigt und in der Regel nicht von der e-Mail-Anwendung angezeigt wird. Dies ist die Adresse 5321.MailFrom oder die Reverse-Adresse bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ca190-p103">**"Mail From" address**: Identifies the sender and specifies where to send return notices if any problems occur with the delivery of the message, such as non-delivery notices. This appears in the envelope portion of an email message and is not usually displayed by your email application. This is sometimes called the 5321.MailFrom address or the reverse-path address.</span></span>
    
- <span data-ttu-id="ca190-p104">**"Von"-Adresse**: die Adresse als von-Adresse Ihre e-Mail-Anwendung angezeigt. Diese Adresse identifiziert den Autor der e-Mail. D. h., das Postfach von der Person oder ein System zum Schreiben der Nachricht verantwortlich. Dies ist die Adresse 5322.From bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ca190-p104">**"From" address**: The address displayed as the From address by your mail application. This address identifies the author of the email. That is, the mailbox of the person or system responsible for writing the message. This is sometimes called the 5322.From address.</span></span>
    
<span data-ttu-id="ca190-p105">SPF verwendet einen DNS-TXT-Eintrag, um eine Liste der autorisierten sendenden IP-Adressen für eine bestimmte Domäne bereitzustellen. In der Regel werden SPF-Prüfungen nur für die „5321.MailFrom"-Adresse durchgeführt. Dies bedeutet, dass die „5322.From"-Adresse nicht authentifiziert wird, wenn Sie nur SPF verwenden. Aufgrund dessen kann es dazu kommen, dass ein Benutzer eine Nachricht erhält, die die SPF-Prüfung besteht, jedoch eine Spoof-5322.From-Absenderadresse aufweist. Betrachten Sie beispielsweise das folgende SMTP-Transkript:</span><span class="sxs-lookup"><span data-stu-id="ca190-p105">SPF uses a DNS TXT record to provide a list of authorized sending IP addresses for a given domain. Normally, SPF checks are only performed against the 5321.MailFrom address. This means that the 5322.From address is not authenticated when you use SPF by itself. This allows for a scenario where a user can receive a message which passes an SPF check but has a spoofed 5322.From sender address. For example, consider this SMTP transcript:</span></span>
  
```
S: Helo woodgrovebank.com
S: Mail from: phish@phishing.contoso.com
S: Rcpt to: astobes@tailspintoys.com
S: data
S: To: "Andrew Stobes" <astobes@tailspintoys.com>
S: From: "Woodgrove Bank Security" <security@woodgrovebank.com>
S: Subject: Woodgrove Bank - Action required
S:
S: Greetings User,
S: 
S: We need to verify your banking details.
S: Please click the following link to verify that we have the right information for your account.
S: 
S: http://short.url/woodgrovebank/updateaccount/12-121.aspx
S:
S: Thank you,
S: Woodgrove Bank
S: .
```

<span data-ttu-id="ca190-124">In diesem Transkript lauten die Absenderadressen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ca190-124">In this transcript, the sender addresses are as follows:</span></span>
  
- <span data-ttu-id="ca190-125">„E-Mail von"-Adresse (5321.MailFrom): phish@phishing.contoso.com</span><span class="sxs-lookup"><span data-stu-id="ca190-125">Mail from address (5321.MailFrom): phish@phishing.contoso.com</span></span>
    
- <span data-ttu-id="ca190-126">„Von"-Adresse (5322.From): security@woodgrovebank.com</span><span class="sxs-lookup"><span data-stu-id="ca190-126">From address (5322.From): security@woodgrovebank.com</span></span>
    
<span data-ttu-id="ca190-p106">Wenn Sie SPF konfiguriert haben, führt der empfangende Server eine Prüfung der Absenderadresse „phish@phishing.contoso.com“ durch. Wenn die Nachricht aus einer gültigen Quelle der Domäne „phishing.contoso.com“ stammt, besteht sie die SPF-Prüfung. Da der E-Mail-Client nur die Absenderadresse anzeigt, sieht der Benutzer, dass diese Nachricht von „security@woodgrovebank.com“ stammt. Wenn nur SPF verwendet wird, wird die Gültigkeit von „woodgrovebank.com“ nicht authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="ca190-p106">If you configured SPF, then the receiving server performs a check against the Mail from address phish@phishing.contoso.com. If the message came from a valid source for the domain phishing.contoso.com then the SPF check passes. Since the email client only displays the From address, the user sees that this message came from security@woodgrovebank.com. With SPF alone, the validity of woodgrovebank.com was never authenticated.</span></span>
  
<span data-ttu-id="ca190-p107">Wenn Sie DMARC verwenden, führt der empfangende Server auch eine Prüfung der Absenderadresse durch. Wenn im obigen Beispiel ein DMARC-TXT-Eintrag für „woodgrovebank.com“ vorhanden ist, besteht die Absenderadresse die Prüfung nicht.</span><span class="sxs-lookup"><span data-stu-id="ca190-p107">When you use DMARC, the receiving server also performs a check against the From address. In the example above, if there is a DMARC TXT record in place for woodgrovebank.com, then the check against the From address fails.</span></span>
  
## <a name="what-is-a-dmarc-txt-record"></a><span data-ttu-id="ca190-133">Was ist ein DMARC-TXT-Eintrag?</span><span class="sxs-lookup"><span data-stu-id="ca190-133">What is a DMARC TXT record?</span></span>
<span data-ttu-id="ca190-134"><a name="WhatisDMARC"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-134"></span></span>

<span data-ttu-id="ca190-p108">Wie die DNS-Einträge für SPF ist der Eintrag für DMARC ein DNS-Texteintrag (TXT), der vor Spoofing- und Phishing-E-Mails schützt. Sie veröffentlichen DMARC-TXT-Einträge in DNS. DMARC-TXT-Einträge prüfen den Ursprung von E-Mail-Nachrichten, indem sie die IP-Adresse des Absenders mit dem vorgeblichen Besitzer der Absenderdomäne vergleichen. Durch den DMARC-TXT-Eintrag werden autorisierte Server für ausgehende E-Mails gekennzeichnet. Die Ziel-E-Mail-Systeme können dann überprüfen, ob die empfangenen Nachrichten von autorisierten Servern für ausgehende E-Mails stammen.</span><span class="sxs-lookup"><span data-stu-id="ca190-p108">Like the DNS records for SPF, the record for DMARC is a DNS text (TXT) record that helps prevent spoofing and phishing. You publish DMARC TXT records in DNS. DMARC TXT records validate the origin of email messages by verifying the IP address of an email's author against the alleged owner of the sending domain. The DMARC TXT record identifies authorized outbound email servers. Destination email systems can then verify that messages they receive originate from authorized outbound email servers.</span></span>
  
<span data-ttu-id="ca190-140">Der DMARC-TXT-Eintrag von Microsoft sieht in etwa wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="ca190-140">Microsoft's DMARC TXT record looks something like this:</span></span>
  
```
_dmarc.microsoft.com.   3600    IN      TXT     "v=DMARC1; p=none; pct=100; rua=mailto:d@rua.agari.com; ruf=mailto:d@ruf.agari.com; fo=1" 
```

<span data-ttu-id="ca190-p109">Microsoft sendet seine DMARC-Berichte an [Agari](https://agari.com), einen Drittanbieter. Agari sammelt und analysiert DMARC-Berichte.</span><span class="sxs-lookup"><span data-stu-id="ca190-p109">Microsoft sends its DMARC reports to [Agari](https://agari.com), a 3rd party. Agari collects and analyzes DMARC reports.</span></span>
  
## <a name="implement-dmarc-for-inbound-mail"></a><span data-ttu-id="ca190-143">Implementieren von DMARC für eingehende E-Mail-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="ca190-143">Implement DMARC for inbound mail</span></span>
<span data-ttu-id="ca190-144"><a name="implementDMARCinbound"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-144"></span></span>

<span data-ttu-id="ca190-p110">Sie müssen nichts weiter tun, um DMARC für E-Mails einzurichten, die Sie in Office 365 erhalten. Dies haben wir bereits für Sie erledigt. Wenn Sie mehr darüber erfahren möchten, was mit E-Mail-Nachrichten geschieht, die unsere DMARC-Prüfungen nicht bestehen, finden Sie weitere Informationen unter [So behandelt Office 365 eingehende E-Mail-Nachrichten, die DMARC-Prüfungen nicht bestehen](use-dmarc-to-validate-email.md#inbounddmarcfail).</span><span class="sxs-lookup"><span data-stu-id="ca190-p110">You don't have to do a thing to set up DMARC for mail that you receive in Office 365. We've taken care of everything for you. If you want to learn what happens to mail that fails to pass our DMARC checks, see [How Office 365 handles inbound email that fails DMARC](use-dmarc-to-validate-email.md#inbounddmarcfail).</span></span>
  
## <a name="implement-dmarc-for-outbound-mail-from-office-365"></a><span data-ttu-id="ca190-148">Implementieren von DMARC für von Office 365 ausgehende Nachrichten</span><span class="sxs-lookup"><span data-stu-id="ca190-148">Implement DMARC for outbound mail from Office 365</span></span>
<span data-ttu-id="ca190-149"><a name="implementDMARCoutbound"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-149"></span></span>

<span data-ttu-id="ca190-p111">Wenn Sie Office 365 verwenden und keine benutzerdefinierte Domäne verwenden, d. h. wenn Sie die Domäne „onmicrosoft.com" verwenden, müssen Sie keine weiteren Schritte zum Konfigurieren oder Implementieren von DMARC für Ihre Organisation durchführen. SPF ist bereits eingerichtet, und Office 365 generiert automatisch eine DKIM-Signatur für Ihre ausgehenden E-Mails. Weitere Informationen zu dieser Signatur finden Sie unter [Standardverhalten für DKIM und Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span><span class="sxs-lookup"><span data-stu-id="ca190-p111">If you use Office 365 but you aren't using a custom domain, that is, you use onmicrosoft.com, you don't need to do anything else to configure or implement DMARC for your organization. SPF is already set up for you and Office 365 automatically generates a DKIM signature for your outgoing mail. For more information about this signature, see [Default behavior for DKIM and Office 365](use-dkim-to-validate-outbound-email.md#DefaultDKIMbehavior).</span></span>
  
 <span data-ttu-id="ca190-p112">Wenn Sie eine benutzerdefinierte Domäne haben oder zusätzlich zu Office 365 lokale Exchange-Server verwenden, müssen Sie DMARC für Ihre ausgehenden E-Mail-Nachrichten manuell implementieren. Das Implementieren von DMARC für Ihre benutzerdefinierte Domäne umfasst die folgenden Schritte:</span><span class="sxs-lookup"><span data-stu-id="ca190-p112">If you have a custom domain or you are using on-premises Exchange servers in addition to Office 365, you need to manually implement DMARC for your outbound mail. Implementing DMARC for your custom domain includes these steps:</span></span> 
  
- [<span data-ttu-id="ca190-155">Schritt 1: Identifizieren gültiger E-Mail-Nachrichtenquellen für Ihre Domäne</span><span class="sxs-lookup"><span data-stu-id="ca190-155">Step 1: Identify valid sources of mail for your domain</span></span>](use-dmarc-to-validate-email.md#IdentifyValidSources)
    
- [<span data-ttu-id="ca190-156">Schritt 2: Einrichten von SPF für Ihre Domäne in Office 365</span><span class="sxs-lookup"><span data-stu-id="ca190-156">Step 2: Set up SPF for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigSPF)
    
- [<span data-ttu-id="ca190-157">Schritt 3: Einrichten von DKIM für Ihre benutzerdefinierte Domäne in Office 365</span><span class="sxs-lookup"><span data-stu-id="ca190-157">Step 3: Set up DKIM for your custom domain in Office 365</span></span>](use-dmarc-to-validate-email.md#ConfigDKIM)
    
- [<span data-ttu-id="ca190-158">Schritt 4: Erstellen des DMARC-TXT-Eintrags für Ihre Domäne in Office 365</span><span class="sxs-lookup"><span data-stu-id="ca190-158">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>](use-dmarc-to-validate-email.md#CreateDMARCRecord)
    
### <a name="step-1-identify-valid-sources-of-mail-for-your-domain"></a><span data-ttu-id="ca190-159">Schritt 1: Identifizieren gültiger E-Mail-Nachrichtenquellen für Ihre Domäne</span><span class="sxs-lookup"><span data-stu-id="ca190-159">Step 1: Identify valid sources of mail for your domain</span></span>
<span data-ttu-id="ca190-160"><a name="IdentifyValidSources"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-160"></span></span>

<span data-ttu-id="ca190-p113">Wenn Sie SPF bereits eingerichtet haben, ist dieser Schritt für Sie bereits erledigt. Für DMARC müssen Sie jedoch noch andere Punkte berücksichtigen. Beim Ermitteln von E-Mail-Nachrichtenquellen für Ihre Domäne müssen Sie die folgenden beiden Fragen beantworten:</span><span class="sxs-lookup"><span data-stu-id="ca190-p113">If you have already set up SPF then you have already gone through this exercise. However, for DMARC, there are additional considerations. When identifying sources of mail for your domain there are two questions you need to answer:</span></span>
  
- <span data-ttu-id="ca190-164">Welche IP-Adressen senden Nachrichten aus meiner Domäne?</span><span class="sxs-lookup"><span data-stu-id="ca190-164">What IP addresses send messages from my domain?</span></span>
    
- <span data-ttu-id="ca190-165">Was E-Mail-Nachrichten betrifft, die von Drittanbietern in meinem Auftrag gesendet werden: Stimmen die Domänen für „5321.MailFrom" und „5322.From" überein?</span><span class="sxs-lookup"><span data-stu-id="ca190-165">For mail sent from third parties on my behalf, will the 5321.MailFrom and 5322.From domains match?</span></span>
    
### <a name="step-2-set-up-spf-for-your-domain-in-office-365"></a><span data-ttu-id="ca190-166">Schritt 2: Einrichten von SPF für Ihre Domäne in Office 365</span><span class="sxs-lookup"><span data-stu-id="ca190-166">Step 2: Set up SPF for your domain in Office 365</span></span>
<span data-ttu-id="ca190-167"><a name="ConfigSPF"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-167"></span></span>

<span data-ttu-id="ca190-168">Sie haben nun eine Liste aller gültigen Absender erstellt und können die Schritte unter [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="ca190-168">Now that you have a list of all your valid senders you can follow the steps to [Set up SPF in Office 365 to help prevent spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md).</span></span>
  
<span data-ttu-id="ca190-169">Beispiel: Angenommen, „contoso.com" sendet E-Mail-Nachrichten von Exchange Online, einem lokalen Exchange-Server mit der IP-Adresse 192.168.0.1 und einer Webanwendung mit der IP-Adresse 192.168.100.100, dann sieht der SPF-TXT-Eintrag wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="ca190-169">For example, assuming contoso.com sends mail from Exchange Online, an on-premises Exchange server whose IP address is 192.168.0.1, and a web application whose IP address is 192.168.100.100, the SPF TXT record would look like this:</span></span>
  
```
contoso.com  IN  TXT  " v=spf1 ip4:192.168.0.1 ip4:192.168.100.100 include:spf.protection.outlook.com -all"
```

<span data-ttu-id="ca190-170">Es ist eine bewährte Methode sicherzustellen, dass Ihr SPF-TXT-Eintrag auch Absenderadressen von Drittanbietern berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="ca190-170">As a best practice, ensure that your SPF TXT record takes into account third-party senders.</span></span>
  
### <a name="step-3-set-up-dkim-for-your-custom-domain-in-office-365"></a><span data-ttu-id="ca190-171">Schritt 3: Einrichten von DKIM für Ihre benutzerdefinierte Domäne in Office 365</span><span class="sxs-lookup"><span data-stu-id="ca190-171">Step 3: Set up DKIM for your custom domain in Office 365</span></span>
<span data-ttu-id="ca190-172"><a name="ConfigDKIM"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-172"></span></span>

<span data-ttu-id="ca190-p114">Nachdem Sie SPF eingerichtet haben, müssen Sie DKIM einrichten. Mit DKIM können Sie E-Mail-Nachrichten in der Kopfzeile der Nachricht eine digitale Signatur hinzufügen. Wenn Sie DKIM nicht einrichten und stattdessen Office 365 ermöglichen, die DKIM-Standardkonfiguration für Ihre Domäne zu verwenden, funktioniert DMARC möglicherweise nicht. Dies kommt daher, dass die DKIM-Standardkonfiguration die anfängliche Domäne „onmicrosoft.com" als „5322.From"-Adresse verwendet und nicht Ihre benutzerdefinierte Domäne. Dies erzwingt einen Konflikt zwischen den „5321.MailFrom"- und „5322.From"-Adressen in allen E-Mail-Nachrichten, die über Ihre Domäne gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ca190-p114">Once you have set up SPF, you need to set up DKIM. DKIM lets you add a digital signature to email messages in the message header. If you do not set up DKIM and instead allow Office 365 to use the default DKIM configuration for your domain, DMARC may fail. This is because the default DKIM configuration uses your initial onmicrosoft.com domain as the 5322.From address, not your custom domain. This forces a mismatch between the 5321.MailFrom and the 5322.From addresses in all email sent from your domain.</span></span>
  
<span data-ttu-id="ca190-p115">Wenn Sie über Drittanbieter verfügen, die in Ihrem Auftrag E-Mail-Nachrichten senden, und die „5321.MailFrom"- und „5322.From"-Adressen einer von diesen Anbietern gesendeten E-Mail-Nachricht nicht übereinstimmen, dann besteht diese E-Mail-Nachricht die DMARC-Prüfung nicht. Um dies zu vermeiden, müssen Sie DKIM für Ihre Domäne speziell mit diesen Drittanbietern als Absendern einrichten. Dadurch kann Office 365 E-Mail-Nachrichten dieses Drittanbieterdiensts authentifizieren. Allerdings können auch andere, wie beispielsweise Yahoo, Google Mail und Comcast, E-Mail-Nachrichten, die von Ihrem Drittanbieter an sie gesendet wurden, als von Ihnen gesendet authentifizieren. Dies ist nützlich, da es Ihren Kunden ermöglicht, eine Vertrauensstellung mit Ihrer Domäne unabhängig davon zu erstellen, wo sich das Postfach befindet. Gleichzeitig markiert Office 365 eine Nachricht aufgrund von Spoofing nicht als Spam, da sie die Authentifizierungsprüfungen für Ihre Domäne besteht.</span><span class="sxs-lookup"><span data-stu-id="ca190-p115">If you have third-party senders that send mail on your behalf and the mail they send has mismatched 5321.MailFrom and 5322.From addresses, DMARC will fail for that email. To avoid this, you need to set up DKIM for your domain specifically with that third-party sender. This allows Office 365 to authenticate email from this 3rd-party service. However, it also allows others, for example, Yahoo, Gmail, and Comcast, to verify email sent to them by the third-party as if it was email sent by you. This is beneficial because it allows your customers to build trust with your domain no matter where their mailbox is located, and at the same time Office 365 won't mark a message as spam due to spoofing because it passes authentication checks for your domain.</span></span>
  
<span data-ttu-id="ca190-183">Anleitungen zum Einrichten von DKIM für Ihre Domäne, einschließlich der Einrichtung von DKIM für Drittanbieter als Absender, die Ihre Domäne verwenden, finden Sie unter [Verwenden von DKIM zum Überprüfen ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet werden](use-dkim-to-validate-outbound-email.md).</span><span class="sxs-lookup"><span data-stu-id="ca190-183">For instructions on setting up DKIM for your domain, including how to set up DKIM for third-party senders so they can spoof your domain, see [Use DKIM to validate outbound email sent from your custom domain in Office 365](use-dkim-to-validate-outbound-email.md).</span></span>
  
### <a name="step-4-form-the-dmarc-txt-record-for-your-domain-in-office-365"></a><span data-ttu-id="ca190-184">Schritt 4: Erstellen des DMARC-TXT-Eintrags für Ihre Domäne in Office 365</span><span class="sxs-lookup"><span data-stu-id="ca190-184">Step 4: Form the DMARC TXT record for your domain in Office 365</span></span>
<span data-ttu-id="ca190-185"><a name="CreateDMARCRecord"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-185"></span></span>

<span data-ttu-id="ca190-p116">Obwohl es auch andere Syntaxoptionen gibt, die hier nicht genannt werden, sind dies die am häufigsten verwendeten Syntaxoptionen für Office 365. Erstellen Sie den DMARC-TXT-Eintrag für Ihre Domäne im folgenden Format:</span><span class="sxs-lookup"><span data-stu-id="ca190-p116">Although there are other syntax options that are not mentioned here, these are the most commonly used options for Office 365. Form the DMARC TXT record for your domain in the format:</span></span>
  
```
_dmarc.domain  TTL  IN  TXT  "v=DMARC1; pct=100; p=policy"
```

<span data-ttu-id="ca190-188">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="ca190-188">where:</span></span>
  
- <span data-ttu-id="ca190-p117">*Domäne* ist die Domäne, den, die Sie schützen möchten. Standardmäßig schützt der Eintrag e-Mail-Nachrichten von der Domäne und allen Unterdomänen. Wenn Sie angeben, z. B. \_dmarc.contoso.com, und klicken Sie dann auf DMARC schützt e-Mail-Nachrichten von der Domäne und allen Unterdomänen, wie housewares.contoso.com oder plumbing.contoso.com.</span><span class="sxs-lookup"><span data-stu-id="ca190-p117">*domain* is the domain you want to protect. By default, the record protects mail from the domain and all subdomains. For example, if you specify \_dmarc.contoso.com, then DMARC protects mail from the domain and all subdomains, such as housewares.contoso.com or plumbing.contoso.com.</span></span> 
    
- <span data-ttu-id="ca190-p118">*TTL* sollte immer das Äquivalent von einer Stunde. Die Einheit für TTL, entweder Stunden (1 Stunde), Minuten (60 Minuten), oder Sekunden (3600 Sekunden) variiert je nach der Registrierung für Ihre Domäne.</span><span class="sxs-lookup"><span data-stu-id="ca190-p118">*TTL* should always be the equivalent of one hour. The unit used for TTL, either hours (1 hour), minutes (60 minutes), or seconds (3600 seconds), will vary depending on the registrar for your domain.</span></span> 
    
- <span data-ttu-id="ca190-194">*Pct = 100* gibt an, dass diese Regel für 100 % der e-Mail verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ca190-194">*pct=100* indicates that this rule should be used for 100% of email.</span></span>
    
- <span data-ttu-id="ca190-p119">*Richtlinie* gibt an, welche Richtlinie der empfangende Server, denen Sie folgen, wenn DMARC ein Fehler auftritt. Sie können die Richtlinie auf keine festgelegt, isolieren, oder ablehnen.</span><span class="sxs-lookup"><span data-stu-id="ca190-p119">*policy* specifies what policy you want the receiving server to follow if DMARC fails. You can set the policy to none, quarantine, or reject.</span></span> 
    
<span data-ttu-id="ca190-197">Um mehr darüber zu erfahren, welche Optionen Sie verwenden sollten, machen Sie sich mit den Konzepten unter [Bewährte Methoden zum Implementieren von DMARC in Office 365](use-dmarc-to-validate-email.md#DMARCbestpractices) vertraut.</span><span class="sxs-lookup"><span data-stu-id="ca190-197">For information about which options to use, become familiar with the concepts in [Best practices for implementing DMARC in Office 365](use-dmarc-to-validate-email.md#DMARCbestpractices).</span></span>
  
<span data-ttu-id="ca190-198">Beispiele:</span><span class="sxs-lookup"><span data-stu-id="ca190-198">Examples:</span></span>
  
- <span data-ttu-id="ca190-199">Richtlinie auf „none" festgelegt</span><span class="sxs-lookup"><span data-stu-id="ca190-199">Policy set to none</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=none"
    ```

- <span data-ttu-id="ca190-200">Richtlinien auf „quarantine" festgelegt</span><span class="sxs-lookup"><span data-stu-id="ca190-200">Policy set to quarantine</span></span>
  
    ```
    _dmarc.contoso.com 3600 IN  TXT  "v=DMARC1; p=quarantine"
    ```

- <span data-ttu-id="ca190-201">Richtlinie auf „reject" festgelegt</span><span class="sxs-lookup"><span data-stu-id="ca190-201">Policy set to reject</span></span>
  
    ```
    _dmarc.contoso.com  3600 IN  TXT  "v=DMARC1; p=reject"
    ```

<span data-ttu-id="ca190-p120">Nachdem Sie den Eintrag erstellt haben, müssen Sie den Eintrag bei Ihrer Domänenregistrierungsstelle aktualisieren. Anleitungen zum Hinzufügen des DMARC-TXT-Eintrags zu Ihren DNS-Einträgen für Office 365 finden Sie unter [Erstellen von DNS-Einträgen für Office 365, wenn Sie Ihre DNS-Einträge verwalten](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).</span><span class="sxs-lookup"><span data-stu-id="ca190-p120">Once you have formed your record, you need to update the record at your domain registrar. For instructions on adding the DMARC TXT record to your DNS records for Office 365, see [Create DNS records for Office 365 when you manage your DNS records](https://support.office.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23).</span></span>
  
## <a name="best-practices-for-implementing-dmarc-in-office-365"></a><span data-ttu-id="ca190-204">Bewährte Methoden zum Implementieren von DMARC in Office 365</span><span class="sxs-lookup"><span data-stu-id="ca190-204">Best practices for implementing DMARC in Office 365</span></span>
<span data-ttu-id="ca190-205"><a name="DMARCbestpractices"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-205"></span></span>

<span data-ttu-id="ca190-p121">Sie können DMARC allmählich implementieren, ohne den übrigen E-Mail-Nachrichtenfluss zu beeinträchtigen. Erstellen und implementieren Sie einen Rolloutplan, der den hier beschriebenen Schritten folgt. Führen Sie die einzelnen Schritte zunächst für eine Unterdomäne, dann weitere Unterdomänen und schließlich für die Domäne der obersten Ebene in Ihrer Organisation aus, bevor Sie mit dem nächsten Schritt fortfahren.</span><span class="sxs-lookup"><span data-stu-id="ca190-p121">You can implement DMARC gradually without impacting the rest of your mail flow. Create and implement a roll out plan that follows these steps. Do each of these steps first with a sub-domain, then other sub-domains, and finally with the top-level domain in your organization before moving on to the next step.</span></span>
  
1. <span data-ttu-id="ca190-209">Überwachen der Auswirkungen, die die Implementierung von DMARC hat</span><span class="sxs-lookup"><span data-stu-id="ca190-209">Monitor the impact of implementing DMARC</span></span>
    
    <span data-ttu-id="ca190-p122">Beginnen Sie mit einem einfachen Überwachungsmoduseintrag für eine Unterdomäne oder eine Domäne, der erfordert, dass DMARC-Empfänger Ihnen Statistiken zu Nachrichten schicken, die sie bei der Verwendung der Domäne sehen. Ein Überwachungsmoduseintrag ist ein DMARC-TXT-Eintrag, für den als Richtlinie „none" (keine) festgelegt wurde (p=none). Viele Unternehmen veröffentlichen einen DMARC-TXT-Eintrag mit „p=none", da sie sich nicht sicher sind, wie viele E-Mail-Nachrichten möglicherweise verloren gehen, wenn sie eine restriktivere DMARC-Richtlinie anwenden.</span><span class="sxs-lookup"><span data-stu-id="ca190-p122">Start with a simple monitoring-mode record for a sub-domain or domain that requests that DMARC receivers send you statistics about messages that they see using that domain. A monitoring-mode record is a DMARC TXT record that has its policy set to none (p=none). Many companies publish a DMARC TXT record with p=none because they are unsure about how much email they may lose by publishing a more restrictive DMARC policy.</span></span> 
    
    <span data-ttu-id="ca190-p123">Sie können dies sogar durchführen, bevor Sie in Ihrer Messaginginfrastruktur SPF oder DKIM implementiert haben. Sie können E-Mail-Nachrichten jedoch erst dann effektiv mit DMARC in Quarantäne verschieben oder ablehnen, wenn Sie SPF und DKIM implementiert haben. Bei der Einführung von SPF und DKIM stellen die von DMARC generierten Berichte die Anzahl und Quellen der Nachrichten bereit, die diese Prüfungen bestehen und nicht bestehen. So können Sie problemlos erkennen, wie viel des autorisierten Nachrichtenverkehrs abgedeckt wird, und Sie können auftretende Probleme beheben. Außerdem sehen Sie allmählich, wie viele betrügerische Nachrichten gesendet werden und von wo aus.</span><span class="sxs-lookup"><span data-stu-id="ca190-p123">You can do this even before you've implemented SPF or DKIM in your messaging infrastructure. However, you won't be able to effectively quarantine or reject mail by using DMARC until you also implement SPF and DKIM. As you introduce SPF and DKIM, the reports generated through DMARC will provide the numbers and sources of messages that pass these checks, and those that don't. You can easily see how much of your legitimate traffic is or isn't covered by them, and troubleshoot any problems. You'll also begin to see how many fraudulent messages are being sent, and from where.</span></span>
    
2. <span data-ttu-id="ca190-218">Anfordern, dass externe E-Mail-Systeme Nachrichten isolieren, die die DMARC-Prüfung nicht bestehen</span><span class="sxs-lookup"><span data-stu-id="ca190-218">Request that external mail systems quarantine mail that fails DMARC</span></span>
    
    <span data-ttu-id="ca190-p124">Wenn Sie denken, dass der gesamte oder der meiste autorisierte Nachrichtenverkehr durch SPF und DKIM geschützt ist und Ihnen die Auswirkungen der Implementierung von DMARC bewusst sind, können Sie eine Quarantänerichtlinie implementieren. Eine Quarantänerichtlinie ist ein DMARC-TXT-Eintrag, dessen Richtlinie auf „quarantine" festgelegt ist (p=quarantine). Hierdurch fordern Sie DMARC-Empfänger dazu auf, Nachrichten von Ihrer Domäne, die die DMARC-Prüfung nicht bestehen, in die lokale Entsprechung eines Spamordners zu verschieben, anstatt in den Posteingang der Empfänger.</span><span class="sxs-lookup"><span data-stu-id="ca190-p124">When you believe that all or most of your legitimate traffic is protected by SPF and DKIM, and you understand the impact of implementing DMARC, you can implement a quarantine policy. A quarantine policy is a DMARC TXT record that has its policy set to quarantine (p=quarantine). By doing this, you are asking DMARC receivers to put messages from your domain that fail DMARC into the local equivalent of a spam folder instead of your customers' inboxes.</span></span>
    
3. <span data-ttu-id="ca190-222">Anfordern, dass externe E-Mail-Systeme keine Nachrichten akzeptieren, die die DMARC-Prüfung nicht bestehen</span><span class="sxs-lookup"><span data-stu-id="ca190-222">Request that external mail systems not accept messages that fail DMARC</span></span>
    
    <span data-ttu-id="ca190-p125">Der letzte Schritt ist das Implementieren einer Ablehnungsrichtlinie. Eine Ablehnungsrichtlinie ist ein DMARC-TXT-Eintrag, dessen Richtlinie auf „reject" festgelegt ist (p=reject). Wenn Sie dies festlegen, fordern Sie DMARC-Empfänger auf, keine Nachrichten zu akzeptieren, die die DMARC-Prüfungen nicht bestehen.</span><span class="sxs-lookup"><span data-stu-id="ca190-p125">The final step is implementing a reject policy. A reject policy is a DMARC TXT record that has its policy set to reject (p=reject). When you do this, you're asking DMARC receivers not to accept messages that fail the DMARC checks.</span></span> 
    
## <a name="how-office-365-handles-outbound-email-that-fails-dmarc"></a><span data-ttu-id="ca190-226">So behandelt Office 365 ausgehende E-Mail-Nachrichten, die DMARC-Prüfungen nicht bestehen</span><span class="sxs-lookup"><span data-stu-id="ca190-226">How Office 365 handles outbound email that fails DMARC</span></span>
<span data-ttu-id="ca190-227"><a name="outbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-227"></span></span>

<span data-ttu-id="ca190-p126">Wenn eine Nachricht ausgehend aus Office 365 und schlägt DMARC und, Sie die Richtlinie auf p legen haben = Quarantäne oder p = ablehnen, wird die Nachricht über den [Pool mit hohem Risiko Zustellungen für ausgehende Nachrichten](high-risk-delivery-pool-for-outbound-messages.md)weitergeleitet. Es ist keine Außerkraftsetzung für ausgehende e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="ca190-p126">If a message is outbound from Office 365 and fails DMARC, and you have set the policy to p=quarantine or p=reject, the message is routed through the [High-risk delivery pool for outbound messages](high-risk-delivery-pool-for-outbound-messages.md). There is no override for outbound email.</span></span>
  
<span data-ttu-id="ca190-p127">Wenn Sie eine DMARC-Ablehnungsrichtlinie veröffentlichen (p=reject), kann kein anderer Kunde in Office 365 Ihre Domäne an Ihrer Stelle verwenden, da Nachrichten die SPF- und DKIM-Prüfungen für Ihre Domäne nicht bestehen, wenn eine ausgehende Nachricht über den Dienst weitergeleitet wird. Wenn Sie jedoch eine DMARC-Ablehnungsrichtlinie veröffentlichen und nicht die gesamte E-Mail-Authentifizierung über Office 365 abgewickelt wird, wird ein Teil der eingehenden Nachrichten (wie zuvor beschrieben) als Spam gekennzeichnet, oder Nachrichten werden abgelehnt, wenn Sie SPF nicht veröffentlichen und versuchen, sie über den Dienst als ausgehend weiterzuleiten. Diese geschieht zum Beispiel dann, wenn Sie beim Erstellen des DMARC-TXT-Eintrags vergessen, einige IP-Adressen für Server und Apps einzubeziehen, die E-Mail-Nachrichten im Auftrag Ihrer Domäne senden.</span><span class="sxs-lookup"><span data-stu-id="ca190-p127">If you publish a DMARC reject policy (p=reject), no other customer in Office 365 can spoof your domain because messages will not be able to pass SPF or DKIM for your domain when relaying a message outbound through the service. However, if you do publish a DMARC reject policy but don't have all of your email authenticated through Office 365, some of it may be marked as spam for inbound email (as described above), or it will be rejected if you do not publish SPF and try to relay it outbound through the service. This happens, for example, if you forget to include some of the IP addresses for servers and apps that send mail on behalf of your domain when you form your DMARC TXT record.</span></span>
  
## <a name="how-office-365-handles-inbound-email-that-fails-dmarc"></a><span data-ttu-id="ca190-233">So behandelt Office 365 eingehende E-Mail-Nachrichten, die DMARC-Prüfungen nicht bestehen</span><span class="sxs-lookup"><span data-stu-id="ca190-233">How Office 365 handles inbound email that fails DMARC</span></span>
<span data-ttu-id="ca190-234"><a name="inbounddmarcfail"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-234"></span></span>

<span data-ttu-id="ca190-p128">Wenn die DMARC-Richtlinie des sendenden Servers „p=reject" lautet, kennzeichnet EOP die Nachricht als Spam, anstatt sie abzulehnen. Anders ausgedrückt behandelt Office 365 eingehende E-Mail-Nachrichten mit den Richtlinien „p=reject" und „p=quarantine" gleich.</span><span class="sxs-lookup"><span data-stu-id="ca190-p128">If the DMARC policy of the sending server is p=reject, EOP marks the message as spam instead of rejecting it. In other words, for inbound email, Office 365 treats p=reject and p=quarantine the same way.</span></span>
  
<span data-ttu-id="ca190-p129">Office 365 ist so konfiguriert, da einige autorisierte E-Mail-Nachrichten die DMARC-Prüfung möglicherweise nicht bestehen. Eine Nachricht besteht die DMARC-Prüfung zum Beispiel möglicherweise nicht, wenn sie an eine Mailingliste gesendet wird, die die Nachricht an alle Teilnehmer auf der Liste weiterleitet. Wenn Office 365 diese Nachrichten ablehnen würde, könnten autorisierte E-Mail-Nachrichten für Benutzer verloren gehen, ohne dass die Benutzer sie auf andere Weise abrufen können. Diese Nachrichten bestehen die DMARC-Prüfung daher weiterhin nicht, werden jedoch als Spam gekennzeichnet und nicht abgelehnt. Falls gewünscht, können Benutzer diese Nachrichten immer noch anhand einer der folgenden Methoden in ihrem Posteingang erhalten:</span><span class="sxs-lookup"><span data-stu-id="ca190-p129">Office 365 is configured like this because some legitimate email may fail DMARC. For example, a message might fail DMARC if it is sent to a mailing list that then relays the message to all list participants. If Office 365 rejected these messages, people could lose legitimate email and have no way to retrieve it. Instead, these messages will still fail DMARC but they will be marked as spam and not rejected. If desired, users can still get these messages in their inbox through these methods:</span></span>
  
- <span data-ttu-id="ca190-242">Benutzer fügen mithilfe des E-Mail-Clients sichere Absender einzeln hinzu</span><span class="sxs-lookup"><span data-stu-id="ca190-242">Users add safe senders individually by using their email client</span></span>
    
- <span data-ttu-id="ca190-243">Administratoren erstellen eine Exchange-Transportregel (ETR) für alle Benutzer, die Nachrichten dieser bestimmten Absender zulassen</span><span class="sxs-lookup"><span data-stu-id="ca190-243">Administrators create an Exchange transport rule (ETR) for all users that allows messages for those particular senders.</span></span> 
    
## <a name="troubleshooting-your-dmarc-implementation"></a><span data-ttu-id="ca190-244">Problembehandlung bei der DMARC-Implementierung</span><span class="sxs-lookup"><span data-stu-id="ca190-244">Troubleshooting your DMARC implementation</span></span>
<span data-ttu-id="ca190-245"><a name="dmarctroubleshoot"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-245"></span></span>

<span data-ttu-id="ca190-246">Wenn Sie die MX-Einträge Ihrer Domäne so konfiguriert haben, dass EOP nicht der erste Eintrag ist, werden für Ihre Domäne keine DMARC-Fehler erzwungen.</span><span class="sxs-lookup"><span data-stu-id="ca190-246">If you have configured your domain's MX records where EOP is not the first entry, DMARC failures will not be enforced for your domain.</span></span> 
  
<span data-ttu-id="ca190-p130">Wenn Sie Office 365-Kunde sind und der primäre MX-Eintrag Ihrer Domäne nicht auf EOP verweist, können Sie die Vorteile von DMARC nicht nutzen. DMARC funktioniert beispielsweise nicht, wenn Sie den MX-Eintrag auf Ihren lokalen E-Mail-Server verweisen und anschließend E-Mail-Nachrichten mithilfe eines Connectors an EOP weiterleiten. In diesem Szenario ist die Empfängerdomäne eine der akzeptierten Domänen, EOP ist jedoch nicht der primäre MX-Eintrag. Nehmen Sie zum Beispiel einmal an, dass „contoso.com" seinen MX auf sich selbst verweist und EOP als sekundären MX-Eintrag verwendet. Der MX-Eintrag von „contoso.com" sieht dann wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="ca190-p130">If you're an Office 365 customer, and your domain's primary MX record does not point to EOP, you will not get the benefits of DMARC. For example, DMARC won't work if you point the MX record to your on-premises mail server and then route email to EOP by using a connector. In this scenario, the receiving domain is one of your Accepted-Domains but EOP is not the primary MX. For example, suppose contoso.com points its MX at itself and uses EOP as a secondary MX record, contoso.com's MX record looks like the following:</span></span>
  
```
contoso.com     3600   IN  MX  0  mail.contoso.com
contoso.com     3600   IN  MX  10 contoso-com.mail.protection.outlook.com
```

<span data-ttu-id="ca190-p131">Alle oder die meisten, e-Mail wird zuerst an mail.contoso.com weitergeleitet werden, da die primäre MX ist, und klicken Sie dann Mail zu EOP weitergeleitet wird. In einigen Fällen möglicherweise auch nicht in allen Listen Sie EOP als einen MX-Eintrag und einfach zu verknüpfen von Connectors auf Ihre e-Mail-Adresse weiterleiten. EOP hat keinen den ersten Eintrag für die DMARC Überprüfung durchgeführt werden soll. Es wird nur die Überprüfung sichergestellt, wie wir bestimmte nicht möglich, dass alle auf-Standort/nicht-O365 Server DMARC Überprüfungen ausgeführt werden.  DMARC ist berechtigt, erzwungen werden für einen Kunden-Domäne (nicht Server), wenn Sie der DMARC TXT-Eintrag einrichten, aber der empfangende Server die Durchsetzung durchgeführt wird.  Wenn Sie EOP als der empfangende Server eingerichtet haben, ist EOP DMARC erzwingen.</span><span class="sxs-lookup"><span data-stu-id="ca190-p131">All, or most, email will first be routed to mail.contoso.com since it's the primary MX, and then mail will get routed to EOP. In some cases, you might not even list EOP as an MX record at all and simply hook up connectors to route your email. EOP does not have to be the first entry for DMARC validation to be done. It just ensures the validation, as we cannot be certain that all on-premise/non-O365 servers will do DMARC checks.  DMARC is eligible to be enforced for a customer’s domain (not server) when you set up the DMARC TXT record, but it is up to the receiving server to actually do the enforcement.  If you set up EOP as the receiving server, then EOP does the DMARC enforcement.</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="ca190-257">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ca190-257">For more information</span></span>
<span data-ttu-id="ca190-258"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-258"></span></span>

<span data-ttu-id="ca190-p132">Sie möchten mehr über DMARC erfahren? Die folgenden Ressourcen können nützlich sein.</span><span class="sxs-lookup"><span data-stu-id="ca190-p132">Want more information about DMARC? These resources can help.</span></span>
  
- <span data-ttu-id="ca190-261">[Antispam-Nachrichtenkopfzeilen](anti-spam-message-headers.md) umfasst die Syntax- und Kopfzeilenfelder, die von Office 365 für DMARC-Überprüfungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca190-261">[Anti-spam message headers](anti-spam-message-headers.md) includes the syntax and header fields used by Office 365 for DMARC checks.</span></span> 
    
- <span data-ttu-id="ca190-262">Sehen Sie sich die [DMARC Training Series](https://www.m3aawg.org/activities/training/dmarc-training-series) von M <sup>3</sup>AAWG (Messaging, Malware, Mobile Anti-Abuse Working Group) an.</span><span class="sxs-lookup"><span data-stu-id="ca190-262">Take the [DMARC Training Series](https://www.m3aawg.org/activities/training/dmarc-training-series) from M <sup>3</sup>AAWG (Messaging, Malware, Mobile Anti-Abuse Working Group).</span></span>
    
- <span data-ttu-id="ca190-263">Verwenden Sie die Checkliste von [dmarcian](https://space.dmarcian.com/deployment/).</span><span class="sxs-lookup"><span data-stu-id="ca190-263">Use the checklist at [dmarcian](https://space.dmarcian.com/deployment/).</span></span>
    
- <span data-ttu-id="ca190-264">Schauen Sie direkt an der Quelle nach: [DMARC.org](https://dmarc.org).</span><span class="sxs-lookup"><span data-stu-id="ca190-264">Go directly to the source at [DMARC.org](https://dmarc.org).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ca190-265">See also</span><span class="sxs-lookup"><span data-stu-id="ca190-265">See also</span></span>
<span data-ttu-id="ca190-266"><a name="sectionSection8"> </a></span><span class="sxs-lookup"><span data-stu-id="ca190-266"></span></span>

[<span data-ttu-id="ca190-267">Verwenden des Sender Policy Framework (SPF) durch Office 365 zum Verhindern von Spoofing</span><span class="sxs-lookup"><span data-stu-id="ca190-267">How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing</span></span>](how-office-365-uses-spf-to-prevent-spoofing.md)
  
[<span data-ttu-id="ca190-268">Einrichten von SPF in Office 365 zum Verhindern von Spoofing</span><span class="sxs-lookup"><span data-stu-id="ca190-268">Set up SPF in Office 365 to help prevent spoofing</span></span>](set-up-spf-in-office-365-to-help-prevent-spoofing.md)
  
[<span data-ttu-id="ca190-269">Verwenden von DKIM zum Überprüfen ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet werden</span><span class="sxs-lookup"><span data-stu-id="ca190-269">Use DKIM to validate outbound email sent from your custom domain in Office 365</span></span>](use-dkim-to-validate-outbound-email.md)

