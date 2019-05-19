---
title: Nicht registrierte Domänen-e-Mails
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 10/17/2018
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection:
- M365-security-compliance
description: Wenn Sie ein hohes Volumen an e-Mails mit nicht registrierter Domäne senden, riskieren Sie, dass Ihre e-Mails blockiert werden. Lesen Sie diesen Artikel, um mehr zu erfahren.
ms.openlocfilehash: 207b71ab7e144af9709e7485d61c936e07271a11
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156297"
---
# <a name="unregistered-domain-email-what-you-need-to-know"></a><span data-ttu-id="c7ebc-104">Nicht registrierte Domänen-e-Mails: was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="c7ebc-104">Unregistered Domain Email: What you need to know</span></span>

<span data-ttu-id="c7ebc-105">Office 365 ermöglicht Mandanten das Weiterleiten einiger Nachrichten über Exchange Online Protection (EoP).</span><span class="sxs-lookup"><span data-stu-id="c7ebc-105">Office 365 allows for tenants to relay some messages through Exchange Online Protection (EOP).</span></span> <span data-ttu-id="c7ebc-106">Ein unterstütztes Beispiel hierfür wäre, wenn Benutzer ein Office 365 Postfach haben und eine externe Person e-Mails sendet, die e-Mail-Weiterleitung jedoch so konfiguriert ist, dass Sie an das externe Postfach des Benutzers zurückgeht.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-106">One supported example of this would be when users have an Office 365 mailbox and someone external sends them email but email forwarding is configured so that it goes back out to the user's external mailbox.</span></span> <span data-ttu-id="c7ebc-107">Dies ist am häufigsten in Bildungsumgebungen, in denen Kursteilnehmer ihre persönliche e-Mail-Schnittstelle nutzen, aber immer noch e-Mails im Zusammenhang mit der Schule erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-107">This is most common in education environments where students want to leverage their personal email interface but still get emails related to school.</span></span> <span data-ttu-id="c7ebc-108">Ein weiteres Beispiel ist, wenn sich Kunden in einem Hybrid Szenario befinden und über lokale Server verfügen, die e-Mails aus EoP senden.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-108">Another example is when customers are in a hybrid scenario and have on-premises servers that send email out of EOP.</span></span>

## <a name="problems-with-unregistered-domains"></a><span data-ttu-id="c7ebc-109">Probleme mit nicht registrierten Domänen</span><span class="sxs-lookup"><span data-stu-id="c7ebc-109">Problems with unregistered domains</span></span>

<span data-ttu-id="c7ebc-110">Das Problem besteht darin, dass lokale Server kompromittiert werden und am Ende eine große Menge an Spam von EoP weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-110">The problem is when on-premises servers get compromised and end up relaying a large volume of spam out of EOP.</span></span> <span data-ttu-id="c7ebc-111">In fast allen Fällen werden die richtigen Connectors eingerichtet, aber e-Mails werden von nicht registrierten, auch als Nichtbereitstellung bezeichneten Domänen gesendet.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-111">In almost all cases, the right connectors are set up but email is being sent from unregistered, also known as unprovisioned, domains.</span></span> <span data-ttu-id="c7ebc-112">Office 365 ermöglicht eine angemessene Menge an e-Mails aus nicht registrierten Domänen, aber eine akzeptierte Domäne sollte im Admin Center für jede Domäne konfiguriert werden, von der Sie den Versand planen.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-112">Office 365 does allow a reasonable amount of mail to come from unregistered domains, but an Accepted Domain should be configured in the Admin Center for each domain you plan on sending out of.</span></span>

<span data-ttu-id="c7ebc-113">Nachdem die Mandanten kompromittiert wurden, wird verhindert, dass ausgehende e-Mails für nicht registrierte Domänen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-113">Once compromised, tenants will be prevented from sending outbound mail for unregistered domains.</span></span> <span data-ttu-id="c7ebc-114">Benutzer erhalten einen Unzustellbarkeitsbericht (Non-Delivery Report, NDR), der Folgendes angibt:</span><span class="sxs-lookup"><span data-stu-id="c7ebc-114">Users will receive a Non-Delivery Report (NDR) that states:</span></span>

- <span data-ttu-id="c7ebc-115">550 5.7.750-Dienst ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-115">550 5.7.750 Service unavailable.</span></span> <span data-ttu-id="c7ebc-116">Vom Senden von nicht registrierten Domänen blockierter Client</span><span class="sxs-lookup"><span data-stu-id="c7ebc-116">Client blocked from sending from unregistered domains</span></span>

## <a name="unblocking-tenant-in-order-to-send-again"></a><span data-ttu-id="c7ebc-117">Aufheben der Blockierung von Mandanten, um erneut zu senden</span><span class="sxs-lookup"><span data-stu-id="c7ebc-117">Unblocking tenant in order to send again</span></span>

<span data-ttu-id="c7ebc-118">Es gibt verschiedene Dinge, die Sie ausführen müssen, wenn Sie für das Senden von nicht registrierten Domänen blockiert werden:</span><span class="sxs-lookup"><span data-stu-id="c7ebc-118">There are several things you need to do if you get blocked for sending from unregistered domains:</span></span>

1. <span data-ttu-id="c7ebc-119">Stellen Sie sicher, dass Sie alle Ihre Domänen im Microsoft 365 Admin Center registrieren.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-119">Make sure that you register all of your domains in Microsoft 365 admin center.</span></span> <span data-ttu-id="c7ebc-120">Weitere Informationen finden Sie [hier](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="c7ebc-120">More information can be found [here](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>

2. <span data-ttu-id="c7ebc-121">Suchen Sie nach ungewöhnlichen Konnektoren.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-121">Look for unusual connectors.</span></span> <span data-ttu-id="c7ebc-122">Böswillige Akteure erstellen häufig neue eingehende Connectors in Ihrem Office 365 Mandanten, um Spam zu senden.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-122">Malicious actors will often create new inbound connectors in your Office 365 tenant to send spam.</span></span> <span data-ttu-id="c7ebc-123">Weitere Informationen zum Überprüfen der Connectors finden Sie [hier](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span><span class="sxs-lookup"><span data-stu-id="c7ebc-123">More information on checking your connectors can be found [here](https://docs.microsoft.com/en-us/powershell/module/exchange/mail-flow/get-inboundconnector?view=exchange-ps).</span></span> 

3. <span data-ttu-id="c7ebc-124">Sperren Sie Ihre lokalen Server, und stellen Sie sicher, dass Sie nicht beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-124">Lock down your on-premises servers and ensure that they are not compromised.</span></span>

> [!TIP]
> <span data-ttu-id="c7ebc-125">Es gibt viele Faktoren, vor allem, wenn es sich um Drittanbieterserver handelt.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-125">There are many factors involved here, especially if these are third-party servers.</span></span> <span data-ttu-id="c7ebc-126">Unabhängig davon müssen Sie in der Lage sein zu bestätigen, dass alle e-Mails, die Ihre Server verlassen, legitim sind.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-126">Regardless, you will need to be able confirm that  all mail leaving your servers are legitimate.</span></span>

4. <span data-ttu-id="c7ebc-127">Sobald Sie fertig sind, müssen Sie den Microsoft-Support anrufen und bitten, ihren Mandanten aufheben zu lassen, dass er von nicht registrierten Domänen erneut gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-127">Once done, you will need to call Microsoft Support and ask to get your tenant unblocked to send from unregistered domains again.</span></span>  <span data-ttu-id="c7ebc-128">Die Bereitstellung des Fehlercodes ist hilfreich, aber Sie müssen nachweisen, dass Ihre Umgebung gesichert ist und dass kein Spam mehr gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="c7ebc-128">Providing the error code is helpful, but you will need to prove that your environment is secured and that spam will not be sent again.</span></span> <span data-ttu-id="c7ebc-129">Weitere Informationen zum Öffnen eines Support Falls finden Sie [hier](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span><span class="sxs-lookup"><span data-stu-id="c7ebc-129">More information on opening a support case can be found [here](https://support.office.com/en-us/article/Contact-support-for-business-products-Admin-Help-32a17ca7-6fa0-4870-8a8d-e25ba4ccfd4b#ID0EAADAAA=online).</span></span>
  
## <a name="for-more-information"></a><span data-ttu-id="c7ebc-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c7ebc-130">For more information</span></span>

[<span data-ttu-id="c7ebc-131">Antispamschutz für Office 365-E-Mails</span><span class="sxs-lookup"><span data-stu-id="c7ebc-131">Office 365 email anti-spam protection</span></span>](anti-spam-protection.md)

[<span data-ttu-id="c7ebc-132">Unzustellbarkeitsberichte für E-Mails in Office 365</span><span class="sxs-lookup"><span data-stu-id="c7ebc-132">Email non-delivery reports in Office 365</span></span>](https://support.office.com/article/email-non-delivery-reports-in-office-365-51daa6b9-2e35-49c4-a0c9-df85bf8533c3)

[<span data-ttu-id="c7ebc-133">Konfigurieren der E-Mail-Weiterleitung für ein Postfach</span><span class="sxs-lookup"><span data-stu-id="c7ebc-133">Configure email forwarding for a mailbox</span></span>](https://docs.microsoft.com/en-us/exchange/recipients-in-exchange-online/manage-user-mailboxes/configure-email-forwarding)

[<span data-ttu-id="c7ebc-134">Einrichten eines Multifunktionsgeräts oder einer Anwendung zum Senden von E-Mails mit Office 365</span><span class="sxs-lookup"><span data-stu-id="c7ebc-134">How to set up a multifunction device or application to send email using Office 365</span></span>](https://support.office.com/en-us/article/How-to-set-up-a-multifunction-device-or-application-to-send-email-using-Office-365-69f58e99-c550-4274-ad18-c805d654b4c4)

<span data-ttu-id="c7ebc-135">[Verwalten von akzeptierten Domänen in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span><span class="sxs-lookup"><span data-stu-id="c7ebc-135">[Manage accepted domains in Exchange Online](https://docs.microsoft.com/en-us/exchange/mail-flow-best-practices/manage-accepted-domains/manage-accepted-domains).</span></span>
