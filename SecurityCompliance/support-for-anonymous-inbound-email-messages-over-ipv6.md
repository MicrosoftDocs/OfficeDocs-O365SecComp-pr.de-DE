---
title: Unterstützung für anonym eingehende E-Mail-Nachrichten über IPv6
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/4/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
description: Exchange Online Protection (EOP) und Exchange Online unterstützt empfangen anonyme eingehende e-Mails über IPv6-Kommunikation vom Absender, die keine Nachrichten über Transport Layer Security (TLS) senden. Sie können Anmeldungsverfahren in Empfang von Nachrichten über IPv6 durch diese Funktionalität durch das Office 365 Administrationscenter am Öffnen von UNRESOLVED_TOKEN_VAL(exMCSS) anfordern https://portal.office.com/adminportal/home, auf Sie Unterstützung, und klicken Sie dann auf neue Serviceanfrage). Wenn Sie Anmeldungsverfahren zu IPv6 in nicht benötigen Sie weiterhin über IPv4-Nachrichten empfangen.
ms.openlocfilehash: 93575c57bb6eac5e0f92066dab3e6ed8b5f4b215
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23003014"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a><span data-ttu-id="9cda9-105">Unterstützung für anonym eingehende E-Mail-Nachrichten über IPv6</span><span class="sxs-lookup"><span data-stu-id="9cda9-105">Support for anonymous inbound email messages over IPv6</span></span>

<span data-ttu-id="9cda9-p102">Exchange Online Protection (EOP) und Exchange Online unterstützen das Empfangen von anonymen eingehenden E-Mails über IPv6 von Absendern, die keine Nachrichten über Transport Layer Security (TLS) senden. Sie können sich für das Empfangen von Nachrichten über IPv6 aussprechen, indem Sie diese Funktion über UNRESOLVED_TOKEN_VAL(exMCSS) anfordern (öffnen Sie das Office 365 Admin Center unter [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), klicken Sie auf **Support** und dann auf **Neue Serviceanfrage**). Wenn Sie sich nicht für IPv6 entscheiden, erhalten Sie weiterhin Nachrichten über IPv4.</span><span class="sxs-lookup"><span data-stu-id="9cda9-p102">Exchange Online Protection (EOP) and Exchange Online support receiving anonymous inbound email messages over IPv6 communications from senders who don't send messages over Transport Layer Security (TLS). You can opt-in to receive messages over IPv6 by requesting this functionality from UNRESOLVED_TOKEN_VAL(exMCSS) by opening the Office 365 admin center at [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), clicking **Support**, and then clicking **New service request**). If you don't opt-in to IPv6 you'll continue to receive messages over IPv4.</span></span>
  
<span data-ttu-id="9cda9-109">Absender, die Nachrichten über IPv6 an den Dienst übermitteln, müssen die folgenden beiden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="9cda9-109">Senders who transmit messages to the service over IPv6 must comply with the following two requirements:</span></span>
  
1. <span data-ttu-id="9cda9-110">Die sendende IPv6-Adresse muss einen gültigen PTR-Eintrag aufweisen ([Reverse-DNS-Datensatz](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) der sendenden IPv6-Adresse).</span><span class="sxs-lookup"><span data-stu-id="9cda9-110">The sending IPv6 address must have a valid PTR record ([reverse DNS record](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) of the sending IPv6 address).</span></span> 
    
2. <span data-ttu-id="9cda9-111">Der Absender muss entweder die SPF-Verifizierung (definiert in [RFC 7208](https://tools.ietf.org/html/rfc7208)) oder die [DKIM-Verifizierung](http://dkim.org/) (definiert in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)) bestehen.</span><span class="sxs-lookup"><span data-stu-id="9cda9-111">The sender must pass either SPF verification (defined in [RFC 7208](https://tools.ietf.org/html/rfc7208)) or [DKIM verification](http://dkim.org/) (defined in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)).</span></span>
    
<span data-ttu-id="9cda9-p103">Diese Anforderungen müssen ungeachtet Ihrer Konfiguration vor der Aktivierung von IPv6 erfüllt sein. Wenn beide Anforderungen erfüllt sind, durchläuft die Nachricht das normale E-Mail-Filterverfahren des Dienstes. Wird nur eine der beiden erfüllt, wird die Nachricht mit einer der folgenden 450-Antworten zurückgewiesen:</span><span class="sxs-lookup"><span data-stu-id="9cda9-p103">Meeting these requirements is mandatory regardless of your configuration prior to opting-in to IPv6. If both requirements are met, the message will go through normal email message filtering provided by the service. If one or the other isn't met, the message will be rejected with one of the following 450 responses:</span></span>
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
<span data-ttu-id="9cda9-115">Wenn Sie nicht gewählt haben, Nachrichten über IPv6 zu empfangen, und der Absender versucht, eine Nachricht über IPv6 zu erzwingen, indem er manuell eine Verbindung zum Mailserver herstellt, wird die Nachricht mit einer 550-Antwort zurückgewiesen, die in etwa folgendermaßen aussieht:</span><span class="sxs-lookup"><span data-stu-id="9cda9-115">If you aren't opted in to receive messages over IPv6 and the sender tries to force a message over IPv6 by manually connecting to the mail server, the message will be rejected with a 550 response that looks similar to the following:</span></span>
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a><span data-ttu-id="9cda9-116">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="9cda9-116">For more information</span></span>

[<span data-ttu-id="9cda9-117">Unterstützung für die Validierung von mit DKIM signierten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="9cda9-117">Support for validation of DKIM signed messages</span></span>](support-for-validation-of-dkim-signed-messages.md)
  

