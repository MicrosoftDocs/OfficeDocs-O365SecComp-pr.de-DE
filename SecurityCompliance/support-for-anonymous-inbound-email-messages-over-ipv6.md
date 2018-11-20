---
title: Unterstützung für anonym eingehende E-Mail-Nachrichten über IPv6
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
ms.assetid: b68df621-0a5f-4824-8abc-41e0c4fd1398
description: Informationen Sie zum Konfigurieren der Unterstützung für anonyme Nachrichten von IPv6-Quellen für Exchange Online Protection und Exchange Online.
ms.openlocfilehash: 0d324ce6e0ff0ff9104ef597176b09a5a319abc7
ms.sourcegitcommit: 75b985b2574f4be70cf352498ea300b3d99dd338
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2018
ms.locfileid: "26255810"
---
# <a name="support-for-anonymous-inbound-email-messages-over-ipv6"></a>Unterstützung für anonym eingehende E-Mail-Nachrichten über IPv6

Exchange Online Protection (EOP) und Exchange Online unterstützt empfangen anonyme eingehende e-Mails über IPv6-Kommunikation vom Absender, die keine Nachrichten über Transport Layer Security (TLS) senden. Sie können Anmeldungsverfahren in Empfang von Nachrichten über IPv6 durch diese Funktionalität von Microsoft Support anfordern, öffnen Sie das Office 365 Administrationscenter unter [https://portal.office.com/adminportal/home](https://portal.office.com/adminportal/home), auf Sie **Unterstützung**, und klicken Sie dann auf **neue Serviceanfrage**). Wenn Sie Anmeldungsverfahren zu IPv6 in nicht benötigen Sie weiterhin über IPv4-Nachrichten empfangen.
  
Absender, die Nachrichten über IPv6 an den Dienst übermitteln, müssen die folgenden beiden Anforderungen erfüllen:
  
1. Die sendende IPv6-Adresse muss einen gültigen PTR-Eintrag aufweisen ([Reverse-DNS-Datensatz](https://en.wikipedia.org/wiki/Reverse_DNS_lookup) der sendenden IPv6-Adresse). 
    
2. Der Absender muss entweder die SPF-Verifizierung (definiert in [RFC 7208](https://tools.ietf.org/html/rfc7208)) oder die [DKIM-Verifizierung](http://dkim.org/) (definiert in [RFC 6376](https://www.rfc-editor.org/rfc/rfc6376.txt)) bestehen.
    
Diese Anforderungen müssen ungeachtet Ihrer Konfiguration vor der Aktivierung von IPv6 erfüllt sein. Wenn beide Anforderungen erfüllt sind, durchläuft die Nachricht das normale E-Mail-Filterverfahren des Dienstes. Wird nur eine der beiden erfüllt, wird die Nachricht mit einer der folgenden 450-Antworten zurückgewiesen:
  
-  `450 4.7.25 Service unavailable, sending IPv6 address [2a01:111:f200:2004::240] must have reverse DNS record.`
    
-  `450 4.7.26 Service unavailable, message sent over IPv6 [2a01:111:f200:2004::240] must pass either SPF or DKIM validation.`
    
Wenn Sie nicht gewählt haben, Nachrichten über IPv6 zu empfangen, und der Absender versucht, eine Nachricht über IPv6 zu erzwingen, indem er manuell eine Verbindung zum Mailserver herstellt, wird die Nachricht mit einer 550-Antwort zurückgewiesen, die in etwa folgendermaßen aussieht:
  
 `550 5.2.1 Service unavailable, [contoso.com] does not accept email over IPv6.`
  
## <a name="for-more-information"></a>Weitere Informationen

[Unterstützung für die Validierung von mit DKIM signierten Nachrichten](support-for-validation-of-dkim-signed-messages.md)
  

