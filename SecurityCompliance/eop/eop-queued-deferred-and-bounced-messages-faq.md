---
title: Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 9d015a0d-52a0-484d-9a08-121d04f973d3
description: Dieses Thema bietet Antworten auf häufig gestellte Fragen zu Nachrichten, die während des Microsoft Exchange Online Protection (EOP)-Filterungsprozesses in eine Warteschlange eingereiht, verzögert oder nicht zugestellt wurden.
ms.openlocfilehash: e8fdb07d11a1f540e94b82730eb848a97f51523a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256263"
---
# <a name="eop-queued-deferred-and-bounced-messages-faq"></a><span data-ttu-id="60214-103">Häufig gestellte Fragen zu durch EOP in Warteschlangen eingereihten, verzögerten oder nicht zugestellten Nachrichten</span><span class="sxs-lookup"><span data-stu-id="60214-103">EOP queued, deferred, and bounced messages FAQ</span></span>

<span data-ttu-id="60214-104">Dieses Thema bietet Antworten auf häufig gestellte Fragen zu Nachrichten, die während des Microsoft Exchange Online Protection (EOP)-Filterungsprozesses in eine Warteschlange eingereiht, verzögert oder nicht zugestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="60214-104">This topic provides answers to frequently asked questions about messages that have been queued, deferred, or bounced during the Microsoft Exchange Online Protection (EOP) filtering process.</span></span>
  
 <span data-ttu-id="60214-105">**F. Warum werden E-Mails in eine Warteschlange eingereiht?**</span><span class="sxs-lookup"><span data-stu-id="60214-105">**Q. Why is mail queuing?**</span></span>
  
<span data-ttu-id="60214-p101">A. Nachrichten werden in eine Warteschlange eingereiht oder zurückgestellt, wenn vom Dienst keine Verbindung zum Server des Empfängers hergestellt werden kann, um sie zuzustellen. Nachrichten werden nicht zurückgestellt, wenn vom Netzwerk des Empfängers ein Fehler der 500er-Serie zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="60214-p101">A. Messages are queued or deferred if the service is unable to make a connection to the recipient server for delivery. It will not defer messages if a 500-series error is returned from the recipient network.</span></span>
  
 <span data-ttu-id="60214-109">**F. Wie kommt es zu einer Zurückstellung von Nachrichten?**</span><span class="sxs-lookup"><span data-stu-id="60214-109">**Q. How does a message become deferred?**</span></span>
  
<span data-ttu-id="60214-p102">A. Nachrichten werden zurückgehalten, wenn keine Verbindung zum Server des Empfängers hergestellt werden kann und von diesem ein "temporärer Fehler" (z. B. "Verbindungstimeout" oder "Verbindung abgelehnt") oder ein Fehler der 400er-Serie zurückgegeben wird. Liegt ein dauerhafter Fehler vor (z. B. ein Fehler der 500er-Serie), wird die Nachricht an den Absender zurückgesendet.</span><span class="sxs-lookup"><span data-stu-id="60214-p102">A. Messages will be held when a connection to the recipient server cannot be made and the recipient's server is returning a "temporary failure" such as a connection time-out, connection refused, or a 400-series error. If there is a permanent failure, such as a 500-series error, then the message will be returned to the sender.</span></span>
  
 <span data-ttu-id="60214-113">**F. Wie lange werden Nachrichten zurückgestellt, und in welchem Intervall wird der Übertragungsversuch wiederholt?**</span><span class="sxs-lookup"><span data-stu-id="60214-113">**Q. How long does a message remain in deferral and what is the retry interval?**</span></span>
  
<span data-ttu-id="60214-114">A.</span><span class="sxs-lookup"><span data-stu-id="60214-114">A.</span></span> <span data-ttu-id="60214-115">Zurückgestellte Nachrichten bleiben 2 Tage lang in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="60214-115">Messages in deferral will remain in our queues for 2 days.</span></span> <span data-ttu-id="60214-116">Wiederholungsversuche hängen davon ab, welcher Fehler vom E-Mail-System des Empfängers zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="60214-116">Message retry attempts are based on the error we get back from the recipient's mail system.</span></span> <span data-ttu-id="60214-117">Die ersten paar Verzögerungen sind 15 Minuten oder weniger, bei nachfolgenden Wiederholungen (in den nächsten zwölf Jahren) wird das Intervall über mehrere Versuche auf maximal 60 Minuten erhöht.</span><span class="sxs-lookup"><span data-stu-id="60214-117">The first few deferrals are 15 minutes or less, with subsequent retries (over the next half dozen or so) increasing the interval over multiple retries to a max of 60 minutes.</span></span> <span data-ttu-id="60214-118">Die Intervalldauer-Erweiterung ist dynamisch und unter Berücksichtigung mehrerer Variablen wie Warteschlangengrößen und interner Nachrichtenpriorität.</span><span class="sxs-lookup"><span data-stu-id="60214-118">The interval duration expansion is dynamic, taking into consideration multiple variables like queue sizes and internal message priority.</span></span> <span data-ttu-id="60214-119">In Basic ist es 15 Minuten (oder weniger), um zu starten und dann von dort in den nächsten Stunden auf 60 Minuten zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="60214-119">In basic, it's 15 minutes (or less) to start, then expanding from there over the next few hours to 60 mins max.</span></span>
  
 <span data-ttu-id="60214-120">**F. Wie werden Nachrichten aus einer Warteschlange verteilt, nachdem mein E-Mail-Server wiederhergestellt ist?**</span><span class="sxs-lookup"><span data-stu-id="60214-120">**Q. After your email server is restored, how are queued messages distributed?**</span></span>
  
<span data-ttu-id="60214-p104">A. Nach der Wiederherstellung Ihres E-Mail-Servers werden alle in eine Warteschlange eingereihten Nachrichten automatisch in der Reihenfolge verarbeitet, in der sie empfangen und in die Warteschlange eingereiht wurden, bevor der Server nicht mehr zur Verfügung stand.</span><span class="sxs-lookup"><span data-stu-id="60214-p104">A. After your email server is restored, all queued messages are automatically processed in the order in which they were received and queued when the server became unavailable.</span></span> 
  

