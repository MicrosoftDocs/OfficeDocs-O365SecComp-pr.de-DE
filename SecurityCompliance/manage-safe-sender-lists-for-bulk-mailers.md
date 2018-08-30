---
title: Verwalten sicherer Absenderlisten für Absender von Massen-E-Mails
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d48db4a3-9fbe-45e2-bbaa-1017ffdf96f8
description: 'Wenn Sie Listen sicherer Absender verwenden möchten, sollten Sie wissen, dass die Verarbeitung in Exchange Online Protection (EOP) und Outlook auf verschiedene Weise erfolgt. Der Dienst berücksichtigt sichere Absender und Domänen, indem er die RFC 5321.MailFrom-Adresse und die RFC 5322.From-Adresse prüft, während Outlook die RFC 5322.From-Adresse zur Liste sicherer Absender eines Benutzers hinzufügt. (Anmerkung: Der Dienst prüft sowohl die 5321.MailFrom-Adresse als auch die 5322.From-Adresse auf blockierte Absender und Domänen.)'
ms.openlocfilehash: 9442bb39e15b9db9a826472dd6110a8fa14130c6
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002994"
---
# <a name="manage-safe-sender-lists-for-bulk-mailers"></a><span data-ttu-id="361ea-105">Verwalten sicherer Absenderlisten für Absender von Massen-E-Mails</span><span class="sxs-lookup"><span data-stu-id="361ea-105">Manage safe sender lists for bulk mailers</span></span>

<span data-ttu-id="361ea-p102">Wenn Sie Listen sicherer Absender verwenden möchten, sollten Sie wissen, dass die Verarbeitung in Exchange Online Protection (EOP) und Outlook auf verschiedene Weise erfolgt. Der Dienst berücksichtigt sichere Absender und Domänen, indem er die RFC 5321.MailFrom-Adresse und die RFC 5322.From-Adresse prüft, während Outlook die RFC 5322.From-Adresse zur Liste sicherer Absender eines Benutzers hinzufügt. (Anmerkung: Der Dienst prüft sowohl die 5321.MailFrom-Adresse als auch die 5322.From-Adresse auf blockierte Absender und Domänen.)</span><span class="sxs-lookup"><span data-stu-id="361ea-p102">If you want to use safe sender lists, you should know that Exchange Online Protection (EOP) and Outlook handle processing differently. The service respects safe senders and domains by inspecting the RFC 5321.MailFrom address and the RFC 5322.From address, while Outlook adds the RFC 5322.From address to a user's safe sender list. (Note: The service inspects both the 5321.MailFrom address and 5322.From address for blocked senders and domains.)</span></span>
  
<span data-ttu-id="361ea-p103">Die Adresse SMTP MAIL FROM, auch als RFC 5321.MailFrom-Adresse bekannt, ist die E-Mail-Adresse, die zur Durchführung von SPF-Prüfungen verwendet wird, und, wenn die E-Mail nicht zugestellt werden kann, der Pfad, an den die unzustellbare Nachricht gesendet wird. Es ist diese E-Mail-Adresse, die standardmäßig in den Nachrichtenkopfzeilen im Return-Path angegeben wird, es ist aber möglich, dass der Absender eine andere Return-Path-Adresse festlegt.</span><span class="sxs-lookup"><span data-stu-id="361ea-p103">The SMTP MAIL FROM address, otherwise known as the RFC 5321.MailFrom address, is the email address that's used to perform SPF checks, and if the mail can't be delivered, the path to which the bounced message is delivered. It's this email address that is placed into the Return-Path in the message headers by default, though it's possible for the sender to designate a different Return-Path address.</span></span>
  
<span data-ttu-id="361ea-111">Die Adresse "Von:" in den Nachrichtenkopfzeilen, auch als RFC 5322.From-Adresse bekannt, ist die E-Mail-Adresse, die im E-Mail-Client, z. B. Outlook, angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="361ea-111">The From: address in the message headers, otherwise known as the RFC 5322.From address, is the email address that is displayed in the mail client such as Outlook.</span></span>
  
<span data-ttu-id="361ea-p104">Häufig sind die Adressen 5321.MailFrom und 5322.From gleich. Dies ist z. B. bei der Kommunikation zwischen zwei privaten Nutzern normal. Wenn allerdings die E-Mail im Auftrag eines anderen Benutzers gesendet wird, sind die Adressen häufig verschieden. Dies ist am häufigsten bei Massen-E-Mail-Nachrichten der Fall.</span><span class="sxs-lookup"><span data-stu-id="361ea-p104">Much of the time, the 5321.MailFrom and 5322.From addresses are the same. This is typical for person-to-person communication. However, when email is sent on behalf of someone else, the addresses are frequently different. This usually happens most often for bulk email messages.</span></span>
  
<span data-ttu-id="361ea-p105">Nehmen wir z. B. an, dass die Fluglinie Blue Yonder Airlines die Firma Margie's Travel damit beauftragt hat, ihre Werbe-E-Mails zu versenden. Sie finden dann eine E-Mail in Ihrem Posteingang vor, die vom Absender blueyonder@news.blueyonderairlines.com stammt. In diesem Fall ist die 5321.MailFrom-Adresse blueyonder.airlines@margiestravel.com, und blueyonder@news.blueyonderairlines.com ist die 5322.From-Adresse, die Sie in Outlook sehen. Da der Dienst die RFC 5322.From-Adresse akzeptiert, können Sie sie in Outlook einfach als einen sicheren Absender hinzufügen, um zu verhindern, dass diese Nachricht gefiltert wird.</span><span class="sxs-lookup"><span data-stu-id="361ea-p105">For example, suppose that the airline Blue Yonder Airlines has contracted out Margie's Travel to send out its email advertising. You then get a message in your inbox from sender blueyonder@news.blueyonderairlines.com. In this case, the 5321.MailFrom address is blueyonder.airlines@margiestravel.com, and blueyonder@news.blueyonderairlines.com is the 5322.From address which is the one you see in Outlook. Because the service respects the RFC 5322.From address, to prevent this message from getting filtered, you can simply add the RFC 5322.From address as a safe sender in Outlook.</span></span>
  

