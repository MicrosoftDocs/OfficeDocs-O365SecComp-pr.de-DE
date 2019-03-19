---
title: Nicht registrierte Domänen-e-Mails
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/17/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Wenn Sie eine große Anzahl von nicht registrierten Domänen-e-Mails senden, besteht das Risiko, dass Ihre e-Mails blockiert werden. Lesen Sie diesen Artikel, um mehr zu erfahren.
ms.openlocfilehash: 21c403c8072902565f63048782b06c531cdbceb0
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670540"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="3a35d-104">Nicht registrierte Domänen-e-Mails: was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="3a35d-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="3a35d-105">Office 365 ermöglicht es den Mandanten, einige Nachrichten über Exchange Online Protection (EOP) weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="3a35d-105">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP).</span></span> <span data-ttu-id="3a35d-106">Ein unterstütztes Beispiel dafür wäre, wenn Benutzer ein Office 365-Postfach haben und eine externe Person e-Mails sendet, die e-Mail-Weiterleitung jedoch so konfiguriert ist, dass Sie an das externe Postfach des Benutzers zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="3a35d-106">One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox.</span></span> <span data-ttu-id="3a35d-107">Dies ist am häufigsten in Bildungsumgebungen, in denen Schüler ihre persönliche e-Mail-Schnittstelle nutzen möchten, aber immer noch e-Mails im Zusammenhang mit der Schule.</span><span class="sxs-lookup"><span data-stu-id="3a35d-107">This is most common in education environments where students want to leverage their personal email interface but still get emails related to school.</span></span> <span data-ttu-id="3a35d-108">Ein weiteres Beispiel ist, wenn sich Kunden in einem Hybrid Szenario befinden und über lokale Server verfügen, die e-Mails aus EOP senden.</span><span class="sxs-lookup"><span data-stu-id="3a35d-108">Another example is when customers are in a hybrid scenario and have on-premises servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="3a35d-109">Probleme mit nicht registrierten Domänen</span><span class="sxs-lookup"><span data-stu-id="3a35d-109">Problems with unregistered domains</span></span>

<span data-ttu-id="3a35d-110">Das Problem besteht darin, dass lokale Server kompromittiert werden und am Ende eine umfangreiche Anzahl von Spam-EOP.</span><span class="sxs-lookup"><span data-stu-id="3a35d-110">The problem is when on-premises servers get compromised and end up relaying a large volume of spam out of EOP.</span></span> <span data-ttu-id="3a35d-111">In fast allen Fällen werden die richtigen Connectors eingerichtet, aber e-Mails werden von nicht registrierten, auch als nicht zugestellt, bezeichneten Domänen gesendet.</span><span class="sxs-lookup"><span data-stu-id="3a35d-111">In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains.</span></span> <span data-ttu-id="3a35d-112">Office 365 ermöglicht eine angemessene Menge an e-Mails aus nicht registrierten Domänen, aber eine akzeptierte Domäne sollte im Admin Center für jede Domäne konfiguriert werden, von der aus Sie das Senden planen.</span><span class="sxs-lookup"><span data-stu-id="3a35d-112">Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="3a35d-113">Nach der Kompromittierung werden die Mandanten daran gehindert, ausgehende e-Mails für nicht registrierte Domänen zu senden.</span><span class="sxs-lookup"><span data-stu-id="3a35d-113">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains.</span></span> <span data-ttu-id="3a35d-114">Benutzer erhalten einen Unzustellbarkeitsbericht (NDR) mit den folgenden Angaben:</span><span class="sxs-lookup"><span data-stu-id="3a35d-114">Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="3a35d-115">550 5.7.750-Dienst ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3a35d-115">550 5.7.750 Service unavailable.</span></span> <span data-ttu-id="3a35d-116">Vom Senden von nicht registrierten Domänen blockierter Client</span><span class="sxs-lookup"><span data-stu-id="3a35d-116">Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="3a35d-117">Aufheben der Blockierung des Mandanten zum erneuten Senden</span><span class="sxs-lookup"><span data-stu-id="3a35d-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="3a35d-118">Es gibt mehrere Schritte, die Sie ausführen müssen, wenn Sie für das Senden von nicht registrierten Domänen gesperrt werden:</span><span class="sxs-lookup"><span data-stu-id="3a35d-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="3a35d-119">Stellen Sie sicher, dass Sie alle Ihre Domänen in Microsoft 365 Admin Center registrieren.</span><span class="sxs-lookup"><span data-stu-id="3a35d-119">Make sure that you register all of your domains in Microsoft 365 admin center.</span></span> <span data-ttu-id="3a35d-120">Weitere Informationen finden Sie [hier](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="3a35d-120">More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="3a35d-121">Suchen Sie nach ungewöhnlichen Konnektoren.</span><span class="sxs-lookup"><span data-stu-id="3a35d-121">Look for unusual connectors.</span></span> <span data-ttu-id="3a35d-122">Böswillige Akteure erstellen häufig neue eingehende Connectors in Ihrem Office 365-Mandanten, um Spam zu senden.</span><span class="sxs-lookup"><span data-stu-id="3a35d-122">Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam.</span></span> <span data-ttu-id="3a35d-123">Weitere Informationen zur Überprüfung ihrer Konnektoren finden Sie [hier](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="3a35d-123">More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="3a35d-124">Sperren Sie Ihre lokalen Server, und stellen Sie sicher, dass Sie nicht beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="3a35d-124">Lock down your on-premises servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="3a35d-125">Hier gibt es viele Faktoren, insbesondere, wenn es sich dabei um Drittanbieterserver handelt.</span><span class="sxs-lookup"><span data-stu-id="3a35d-125">There are many factors involved here, especially if these are third-party servers.</span></span> <span data-ttu-id="3a35d-126">Unabhängig davon müssen Sie bestätigen können, dass alle e-Mails, die Ihre Server verlassen, legitim sind.</span><span class="sxs-lookup"><span data-stu-id="3a35d-126">Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="3a35d-127">Nachdem Sie fertig sind, müssen Sie den Microsoft-Support anrufen und bitten, ihren Mandanten zu entsperrten, dass er von nicht registrierten Domänen erneut sendet.</span><span class="sxs-lookup"><span data-stu-id="3a35d-127">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.</span></span>  <span data-ttu-id="3a35d-128">Das Bereitstellen des Fehlercodes ist hilfreich, aber Sie müssen nachweisen, dass Ihre Umgebung gesichert ist und dass Spam nicht erneut gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3a35d-128">Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again.</span></span> <span data-ttu-id="3a35d-129">Weitere Informationen zum Öffnen eines Support Falls finden Sie [hier](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="3a35d-129">More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="3a35d-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a35d-130">For more information</span></span>

[<span data-ttu-id="3a35d-131">Antispamschutz für Office 365-E-Mails</span><span class="sxs-lookup"><span data-stu-id="3a35d-131">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="3a35d-132">Unzustellbarkeitsberichte für E-Mails in Office 365</span><span class="sxs-lookup"><span data-stu-id="3a35d-132">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="3a35d-133">Konfigurieren der E-Mail-Weiterleitung für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="3a35d-133">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="3a35d-134">Einrichten eines Multifunktionsgeräts oder einer Anwendung zum Senden von E-Mails mit Office 365</span><span class="sxs-lookup"><span data-stu-id="3a35d-134">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="3a35d-135">[Verwalten von akzeptierten Domänen in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="3a35d-135">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
