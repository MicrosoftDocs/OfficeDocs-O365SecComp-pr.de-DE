---
title: Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/7/2015
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8079f193-1b40-4081-9e5d-d0e50dfbcc59
description: Kunden in einigen Fällen des Askwhat der Unterschied zwischen Junk-e-Mail und Massen-e-Mails? Der Zweck dieses Themas wird um den Unterschied zu erläutern und Informationen über die verschiedenen Optionen bereitzustellen, die für beide in Exchange Online und Exchange Online Protection (EOP) verfügbar sind.
ms.openlocfilehash: ea3f27bdd9ec2aa586dd55139825fc90390ca736
ms.sourcegitcommit: b4e69c54c7bf405d37dfeadc5611803bea9554e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/04/2019
ms.locfileid: "27733301"
---
# <a name="whats-the-difference-between-junk-email-and-bulk-email"></a><span data-ttu-id="9b380-103">Worin besteht der Unterschied zwischen Junk-E-Mail und Massen-E-Mail?</span><span class="sxs-lookup"><span data-stu-id="9b380-103">What's the difference between junk email and bulk email?</span></span>

<span data-ttu-id="9b380-p101">Kunden fragen mitunter, worin der Unterschied zwischen Junk-E-Mail und Massen-E-Mail bestehe. Zweck dieses Themas ist die Erläuterung des Unterschieds und Bereitstellung von Informationen zu den verschiedenen Optionen, die sowohl in Exchange Online als auch Exchange Online Protection (EOP) zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="9b380-p101">Customers sometimes ask "what's the difference between junk email and bulk email messages?" The purpose of this topic is to explain the difference and to provide information about the different options that are available for both in Exchange Online and Exchange Online Protection (EOP).</span></span>
  
 <span data-ttu-id="9b380-106">**Was ist Junk-E-Mail?**</span><span class="sxs-lookup"><span data-stu-id="9b380-106">**What's junk email?**</span></span>
  
<span data-ttu-id="9b380-p102">Junk-E-Mail-Nachrichten sind Spamnachrichten, d. h. unerwünschte E-Mail-Nachrichten, die vom Dienst herausgefiltert werden. Standardmäßig weist der Dienst Spamnachrichten basierend auf der Zuverlässigkeit der IP-Adresse des Absenders zurück. Doch wenn eine Nachricht die IP-Adressüberprüfung besteht, aber von den Inhaltsfiltern als Spam eingestuft wird, dann wird die Nachricht in den Junk-E-Mail-Ordner der vorgesehenen Empfänger gesendet.</span><span class="sxs-lookup"><span data-stu-id="9b380-p102">Junk email messages are "spam" messages, which are unsolicited (and typically unwanted) email messages that are filtered by the service. By default, the service rejects the spam message based on the reputation of the sending IP address. However, if it passes IP inspection but is classified as spam by the content filters, the message is sent to the Junk Email folder of the intended recipients.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9b380-p103">Die Aktion, die auf Nachrichten angewendet wird, die die Inhaltsfilterung durchlaufen haben, kann mithilfe von Inhaltsfilterrichtlinien im Exchange Admin Center (EAC) konfiguriert werden (siehe [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md)). Wenn Sie mit der Spameinstufung nicht einverstanden sind, können Sie Nachrichten, die Sie für Spam bzw. nicht für Spam halten, Microsoft auf mehrere Weisen melden (siehe [Übermitteln von Spam-, Nicht-Spamnachrichten und Nachrichten, die als betrügerische Phishing-Angriffe angesehen werden, an Microsoft zur Analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md)).</span><span class="sxs-lookup"><span data-stu-id="9b380-p103">The action performed on content-filtered messages is configurable via content filter policies in the Exchange admin center (EAC), as described in [Configure your spam filter policies](configure-your-spam-filter-policies.md). Also, if you disagree with the spam classification, you can report messages that you consider to be spam or non-spam to Microsoft in several ways, as described in [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).</span></span> 
  
 <span data-ttu-id="9b380-112">**Was ist Massen-E-Mail?**</span><span class="sxs-lookup"><span data-stu-id="9b380-112">**What's bulk email?**</span></span>
  
<span data-ttu-id="9b380-p104">Massen-E-Mail ist ein Typ von E-Mail-Nachrichten, der schwieriger zu klassifizieren ist. Während Junk-E-Mail eine ständige Bedrohung darstellt, enthalten Massen-E-Mails eine Werbe- oder Marketingbotschaft, die meist nicht wiederholt gesendet wird. Massen-E-Mail wird von einigen Benutzern gewünscht, die sich ggf. sogar absichtlich für den Empfang dieser Nachrichten angemeldet haben, während andere Benutzer diese Nachrichtentypen als Spam betrachten. Einige Benutzer möchten beispielsweise Werbe-E-Mails von der Contoso Corporation oder Einladungen zu einer bevorstehenden Konferenz zur Internetsicherheit erhalten, während für andere Benutzer diese Nachrichten Spam sind.</span><span class="sxs-lookup"><span data-stu-id="9b380-p104">Bulk email, also referred to as gray mail, is a type of email message that's more difficult to classify. Whereas junk email is a constant threat, bulk email is typically comprised of an advertisement or marketing message that's not likely to get sent repeatedly. Bulk email is wanted by some users, and in fact they may have deliberately signed up to receive these messages, while other users may consider these types of messages to be spam. For example, some users want to receive advertising emails from the Contoso Corporation or invitations to an upcoming conference on cyber security, while other users consider such emails to be spam.</span></span>
  
## <a name="how-to-manage-bulk-email"></a><span data-ttu-id="9b380-117">Umgang mit Massen-E-Mails</span><span class="sxs-lookup"><span data-stu-id="9b380-117">How to manage bulk email</span></span>

<span data-ttu-id="9b380-p105">Der Umgang mit Massen-E-Mails ist nicht ganz einfach, denn wenn alle Massen-E-Mails als Spam eingestuft werden, beschweren sich ggf. die Benutzer, die diese erhalten möchten, und melden sie als falsch positive (Nicht-Spam) Nachricht, die fälschlicherweise als Spam eingestuft wurde. Wenn sämtliche Massen-E-Mails dagegen zugelassen werden, beschweren sich ggf. die Benutzer, die diese nicht wollen, und melden sie als nicht abgefangene Spamnachricht, die fälschlicherweise in ihrem Posteingang gelandet ist.</span><span class="sxs-lookup"><span data-stu-id="9b380-p105">How to manage bulk email isn't a clear cut decision, because if all bulk email is classified as spam, the users that want it may complain and submit it as a false positive (non-spam) message that was wrongly marked as spam. On the other hand, if all bulk email is let through, the users that don't want it may complain and submit it as a missed spam message (false negative) that wrongly arrived in their inbox.</span></span>
  
### <a name="enable-bulk-mail-sensitivity-control-in-the-content-filter-policy"></a><span data-ttu-id="9b380-120">Aktivieren der erweiterten Option zur Filterung von Spam-Massensendungen</span><span class="sxs-lookup"><span data-stu-id="9b380-120">Enable bulk mail sensitivity control in the content filter policy</span></span>

<span data-ttu-id="9b380-p106">Je nach Ihrem Unternehmen Richtlinie in Massen-e-Mails können Administratoren einen Schwellenwert Zuweisen der Massen-e-Mail auswählen. Die Einstellung kann über inhaltsfilterrichtlinien in der Exchange-Verwaltungskonsole konfiguriert werden. Checken Sie [Konfigurieren Ihrer Spam-Filter-Richtlinien](configure-your-spam-filter-policies.md) für die Schritte. Sie können eine Schwellenwert für die Einstellung von 1 bis 9, wobei 1 die meisten Massen-e-Mail als Spam markiert und 9 können die meisten Massen-e-Mail übermittelt werden. Der Dienst führt dann die konfigurierte Aktion, beispielsweise das Senden der Nachricht in der Aufgabenliste des Empfängers Junk-e-Mail-Ordner.</span><span class="sxs-lookup"><span data-stu-id="9b380-p106">Depending on your company's policy on bulk email messages, admins can select a threshold to assign the bulk email. The setting is configurable via content filter policies in the EAC. Check out [Configure your spam filter policies](configure-your-spam-filter-policies.md) for the steps. You can choose a threshold setting from 1-9, where 1 marks most bulk email as spam, and 9 allows most bulk email to be delivered. The service then performs the configured action, such as sending the message to the recipient's Junk Email folder.</span></span> 
  

