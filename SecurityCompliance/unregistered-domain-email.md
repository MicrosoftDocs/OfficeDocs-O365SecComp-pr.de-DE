---
title: Nicht registrierte Domäne E-Mail
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
description: Wenn Sie eine große Menge von nicht registrierte Domäne e-Mail senden, laufen Sie Gefahr Ihrer e-Mail blockiert. Lesen Sie diesen Artikel, um mehr zu erfahren.
ms.openlocfilehash: 30d7887be0429195380f2c4ae1a328904dffd69c
ms.sourcegitcommit: 6d72cdb882b93edf6dfddb5ff2e6d8a16e2fa0bc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/17/2018
ms.locfileid: "25596728"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="d4594-104">Nicht registrierte Domäne Email: Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="d4594-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="d4594-p102">Office 365 ermöglicht Mandanten, einige Nachrichten über Exchange Online Protection (EOP) weiterzuleiten. Unterstützte beispielsweise wäre, wenn Benutzer verfügen über ein Office 365-Postfach und eine externe Person diese e-Mail sendet, aber e-Mail-Weiterleitung konfiguriert ist, sodass es wieder auf das Postfach des Benutzers externen out wechselt. Dies ist die am häufigsten verwendeten in Education-Umgebungen, in dem Kursteilnehmer möchten ihre persönlichen e-Mail-Schnittstelle nutzen erhalten aber immer noch im Zusammenhang mit Schule-e-Mails. Ein weiteres Beispiel ist, wenn Kunden befinden sich in einem hybridszenario und lokale Server, auf denen EOP e-Mails senden.</span><span class="sxs-lookup"><span data-stu-id="d4594-p102">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP). One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox. This is most common in education environments where students want to leverage their personal email interface but still get emails related to school. Another example is when customers are in a hybrid scenario and have on-premise servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="d4594-109">Probleme mit nicht registrierte Domänen</span><span class="sxs-lookup"><span data-stu-id="d4594-109">Problems with unregistered domains</span></span>

<span data-ttu-id="d4594-p103">Das Problem ist, wenn am Standort Server gefährdet abrufen und eine große Menge von Spam aus EOP Weiterleitung am Ende. In fast allen Fällen die richtige Verbinder eingerichtet sind, aber von nicht aufgehoben, auch bekannt als vorbereitete Domänen e-Mail gesendet wird. Office 365 lässt einen angemessenen Zeitraum e-Mail-Nachrichten an nicht registrierte Domänen stammen, aber in der Verwaltungskonsole für jede Domäne, die Sie zum Senden von planen sollte eine akzeptierte Domäne konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d4594-p103">The problem is when on-premise servers get compromised and end up relaying a large volume of spam out of EOP. In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains. Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="d4594-p104">Nachdem gefährdet ist, werden Mandanten senden ausgehenden e-Mails für nicht registrierte Domänen gehindert werden. Benutzer werden ein Unzustellbarkeitsbericht (Non-Delivery Report, NDR) angezeigt, die besagt:</span><span class="sxs-lookup"><span data-stu-id="d4594-p104">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains. Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="d4594-p105">550 5.7.750 Dienst nicht verfügbar. Client verhindert, dass nicht registrierte Domänen senden</span><span class="sxs-lookup"><span data-stu-id="d4594-p105">550 5.7.750 Service unavailable. Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="d4594-117">Aufheben der Blockierung Mandanten, um erneut zu senden</span><span class="sxs-lookup"><span data-stu-id="d4594-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="d4594-118">Es gibt verschiedene Dinge tun, wenn Sie zum Senden von nicht registrierte Domänen blockiert werden:</span><span class="sxs-lookup"><span data-stu-id="d4594-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="d4594-p106">Stellen Sie sicher, dass alle Domänen in Office 365 Administrationscenter zu registrieren. Weitere Informationen finden Sie [hier](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="d4594-p106">Make sure that you register all of your domains in Office 365 admin center. More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="d4594-p107">Suchen Sie nach ungewöhnliche Connectors. Bösartige Akteure erstellt in Ihrer Office 365-Mandanten zum Senden von Spam häufig neue eingehende Connectors. Finden Sie weitere Informationen zum Einchecken Connectors [hier](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="d4594-p107">Look for unusual connectors. Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam. More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="d4594-124">Sperren von den Servern am Standort, und stellen Sie sicher, dass sie nicht beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="d4594-124">Lock down your on-premise servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="d4594-p108">Sind viele Faktoren hier, insbesondere dann, wenn dies Drittanbieter-Servern sind. Unabhängig davon, Sie müssen in der Lage sein zu bestätigen, dass alle e-Mails, die Ihre Server verlassen legitime sind.</span><span class="sxs-lookup"><span data-stu-id="d4594-p108">There are many factors involved here, especially if these are third-party servers. Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="d4594-p109">Abschließend müssen Sie Microsoft Support anrufen, und bitten Sie abzurufenden Ihres Mandanten nicht mehr blockiert, um erneut aus nicht registrierte Domänen zu senden.  Bereitstellen den Fehlercode ist hilfreich, jedoch müssen Sie nachweisen, dass Ihre Umgebung gesichert wird und dass Spam nicht erneut gesendet werden. Weitere Informationen zum Öffnen einer Supportanfrage finden Sie [hier](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="d4594-p109">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.  Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again. More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="d4594-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d4594-130">For more information</span></span>

[<span data-ttu-id="d4594-131">Office 365 email anti-spam protection</span><span class="sxs-lookup"><span data-stu-id="d4594-131">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="d4594-132">Unzustellbarkeitsberichte für E-Mails in Office 365</span><span class="sxs-lookup"><span data-stu-id="d4594-132">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="d4594-133">Konfigurieren der E-Mail-Weiterleitung für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="d4594-133">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="d4594-134">Einrichten eines Multifunktionsgeräts oder einer Anwendung zum Senden von E-Mails mithilfe von Office 365</span><span class="sxs-lookup"><span data-stu-id="d4594-134">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="d4594-135">[Verwalten akzeptierte Domänen im Exchange, Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="d4594-135">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
