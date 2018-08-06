---
title: Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: Dieses Thema bietet Antworten auf häufig gestellte Fragen zu Nachrichten, die während des Microsoft Exchange Online Protection (EOP)-Filterungsprozesses in eine Warteschlange eingereiht, verzögert oder nicht zugestellt wurden.
ms.openlocfilehash: 17e5955195c4e38299712fb9161822984b2a643a
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026222"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="61a7a-103">Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="61a7a-103">EOP queued, deferred, and bounced messages FAQ</span></span>

<span data-ttu-id="61a7a-104">Dieses Thema bietet Antworten auf häufig gestellte Fragen zu Nachrichten, die während des Microsoft Exchange Online Protection (EOP)-Filterungsprozesses in eine Warteschlange eingereiht, verzögert oder nicht zugestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="61a7a-104">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Microsoft Exchange Online Protection (EOP) filtering process.</span></span>
  
 <span data-ttu-id="61a7a-105">**F. Warum werden E-Mails in eine Warteschlange eingereiht?**</span><span class="sxs-lookup"><span data-stu-id="61a7a-105">**Q. Why is mail queuing?**</span></span>
  
<span data-ttu-id="61a7a-p101">A. Nachrichten werden in eine Warteschlange eingereiht oder zurückgestellt, wenn vom Dienst keine Verbindung zum Server des Empfängers hergestellt werden kann, um sie zuzustellen. Nachrichten werden nicht zurückgestellt, wenn vom Netzwerk des Empfängers ein Fehler der 500er-Serie zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="61a7a-p101">A. Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery. It will not defer messages if a 500-series error is returned from the recipient network.</span></span>
  
 <span data-ttu-id="61a7a-109">**F. Wie kommt es zu einer Zurückstellung von Nachrichten?**</span><span class="sxs-lookup"><span data-stu-id="61a7a-109">**Q. How does a message become deferred?**</span></span>
  
<span data-ttu-id="61a7a-p102">A. Nachrichten werden zurückgehalten, wenn keine Verbindung zum Server des Empfängers hergestellt werden kann und von diesem ein "temporärer Fehler" (z. B. "Verbindungstimeout" oder "Verbindung abgelehnt") oder ein Fehler der 400er-Serie zurückgegeben wird. Liegt ein dauerhafter Fehler vor (z. B. ein Fehler der 500er-Serie), wird die Nachricht an den Absender zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="61a7a-p102">A. Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error. If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>
  
 <span data-ttu-id="61a7a-113">**F. Wie lange werden Nachrichten zurückgestellt, und in welchem Intervall wird der Übertragungsversuch wiederholt?**</span><span class="sxs-lookup"><span data-stu-id="61a7a-113">**Q. How long does a message remain in deferral and what is the retry interval?**</span></span>
  
<span data-ttu-id="61a7a-p103">A. Zurückgestellte Nachrichten bleiben 2 Tage lang in der Warteschlange. Wiederholungsversuche hängen davon ab, welcher Fehler vom E-Mail-System des Empfängers zurückgegeben wird. Das Wiederholungsintervall für die Übertragung von Nachrichten beträgt im Durchschnitt 5 Minuten.</span><span class="sxs-lookup"><span data-stu-id="61a7a-p103">A. Messages in deferral will remain in our queues for 2 days. Message retry attempts are based on the error we get back from the recipient's mail system. On average, messages are retried every 5 minutes.</span></span>
  
 <span data-ttu-id="61a7a-118">**F. Wie werden Nachrichten aus einer Warteschlange verteilt, nachdem mein E-Mail-Server wiederhergestellt ist?**</span><span class="sxs-lookup"><span data-stu-id="61a7a-118">**Q. After your email server is restored, how are queued messages distributed?**</span></span>
  
<span data-ttu-id="61a7a-p104">A. Nach der Wiederherstellung Ihres E-Mail-Servers werden alle in eine Warteschlange eingereihten Nachrichten automatisch in der Reihenfolge verarbeitet, in der sie empfangen und in die Warteschlange eingereiht wurden, bevor der Server nicht mehr zur Verfügung stand.</span><span class="sxs-lookup"><span data-stu-id="61a7a-p104">A. After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span> 
  

