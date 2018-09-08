---
title: Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 09/05/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 'Wenn Benutzer ständig E-Mails von Office 365 senden, die als Spam klassifiziert werden, werden diese blockiert, sodass sie keine weiteren E-Mails senden können. '
ms.openlocfilehash: ff5bb010f45b0c89e08239f0e37885bd7ae5c7cd
ms.sourcegitcommit: 234a22c61859133ed5e7988a9551a569781518a4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/07/2018
ms.locfileid: "23875787"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="d5584-103">Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten</span><span class="sxs-lookup"><span data-stu-id="d5584-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="d5584-104">Wenn Benutzer ständig E-Mails von Office 365 senden, die als Spam klassifiziert werden, werden diese blockiert, sodass sie keine weiteren E-Mails senden können. </span><span class="sxs-lookup"><span data-stu-id="d5584-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="d5584-105">
Wenn Absender blockiert sind und keine E-Mails senden können, erhalten sie einen Unzustellbarkeitsbericht (oder eine Meldung, dass beim Senden der Nachricht ein Fehler aufgetreten ist) mit Informationen, wie sie vorgehen müssen, um die Blockierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="d5584-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="d5584-p101">Nicht nur können einzelne Benutzern durch die Domänen Service, sondern auf bestimmte Websites blockiert und IP-Adressen können auch blockiert werden. In einigen Fällen können Domänen oder Websites einer Sperrliste hinzugefügt werden einfach, da sie in einer Spam-Nachricht angezeigt werden. Als der Office 365-Administrator können Sie versuchen, erhalten Benutzer, Websites, Domänen und IP-Adressen von Drittanbieter-Sperrlisten entfernt. Verwenden Sie die Links in der Tabelle unten in diesem Thema, um jede Drittanbieter zu kontaktieren, und folgen Sie den Anweisungen. Wenn eine Person außerhalb von Office 365 mit Ihrem Office 365-Konto Nachrichten senden kann, ihr Konto möglicherweise auf die Liste der blockierten Absender externe beendet wurden einrichten. Benutzer außerhalb von Office 365 können sich selbst aus der Liste blockierter Absender So entfernen Sie mithilfe der [Self-service-delisting Portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx)versuchen.</span><span class="sxs-lookup"><span data-stu-id="d5584-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="d5584-p102">Sie können ausgehende Spameinstellungen konfigurieren, damit Sie eine Benachrichtigung erhalten, wenn ein Office 365-Benutzer blockiert ist und keine E-Mail senden kann, die als Spam klassifiziert wurden. Wenn das Problem mit dem Benutzerpostfach behoben ist, können Sie die Blockierung für diesen Absender aufheben.</span><span class="sxs-lookup"><span data-stu-id="d5584-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="d5584-114">Aufheben der Blockierung eines gesperrten Office 365-E-Mail-Kontos</span><span class="sxs-lookup"><span data-stu-id="d5584-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="d5584-p103">Sie führen Sie diese Aufgabe in der Office 365-Sicherheit und Compliance Center (SCC). [Wechseln Sie zu der Office 365-Sicherheit und Compliance Center](go-to-the-securitycompliance-center.md) , ausführliche Informationen zum SCC.</span><span class="sxs-lookup"><span data-stu-id="d5584-p103">You complete this task in the Office 365 Security & Compliance Center (SCC). [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md) for more details about SCC.</span></span>

1. <span data-ttu-id="d5584-117">Unter Verwendung eines Kontos arbeiten oder Schule, die über Office 365 globaler Administrator verfügt, melden Sie sich bei Office 365-Sicherheit und Compliance Center und erweitern in der Liste auf der linken Seite **Threat Management**, wählen Sie **Überprüfen**und wählen Sie dann **eingeschränkt Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="d5584-117">Using a work or school account that has Office 365 global administrator privileges, sign into the Office 365 Security and Compliance Center and in the list on the left, expand **Threat Management**, choose **Review**, and then choose **Restricted Users**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="d5584-118">Fahren Sie direkt mit der **Benutzer mit eingeschränkten Rechten** Seite in das Wertpapier &amp; Compliance Center, verwenden Sie diese URL: >[https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span><span class="sxs-lookup"><span data-stu-id="d5584-118">To go directly to the **Restricted Users** page in the Security &amp; Compliance Center, use this URL: > [https://protection.office.com/?hash=/restrictedusers](https://protection.office.com/?hash=/restrictedusers)</span></span>

2. <span data-ttu-id="d5584-p104">Diese Seite enthält die Liste der Benutzer, die am Senden von e-Mails an außerhalb Ihrer Organisation blockiert wurden.  Suchen Sie den Benutzer, die, den Sie auf **Zulassen**Einschränkungen auf Entfernen, und klicken Sie dann auf möchten.</span><span class="sxs-lookup"><span data-stu-id="d5584-p104">This page will contain the list of users that have been blocked from sending mail to outside of your organization.  Find the user you wish to remove restrictions on and then click on **Unblock**.</span></span>

3. <span data-ttu-id="d5584-121">Klicken Sie zur Bestätigung der Änderung auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d5584-121">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d5584-p105">Es besteht ein Grenzwert auf die Anzahl der Versuche, die ein Konto durch den Administrator des Mandanten entsperrt werden können Wenn der Grenzwert für einen Benutzer überschritten wurde, wird eine Fehlermeldung angezeigt. Sie müssen dann Support wenden, um den Benutzer aufheben der Blockierung.</span><span class="sxs-lookup"><span data-stu-id="d5584-p105">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. You will then need to contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="d5584-124">Drittanbieter-Blockierungslisten</span><span class="sxs-lookup"><span data-stu-id="d5584-124">Third-party block lists</span></span>

|<span data-ttu-id="d5584-125">**Name der Liste**</span><span class="sxs-lookup"><span data-stu-id="d5584-125">**List Name**</span></span>|<span data-ttu-id="d5584-126">**Abwahlportal**</span><span class="sxs-lookup"><span data-stu-id="d5584-126">**Delisting Portal**</span></span>|<span data-ttu-id="d5584-127">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="d5584-127">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d5584-128">URIBL</span><span class="sxs-lookup"><span data-stu-id="d5584-128">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="d5584-129">URIBL-website</span><span class="sxs-lookup"><span data-stu-id="d5584-129">URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="d5584-130">SURBL</span><span class="sxs-lookup"><span data-stu-id="d5584-130">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="d5584-131">Einführung in SURBL URI Reputation Daten</span><span class="sxs-lookup"><span data-stu-id="d5584-131">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="d5584-132">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="d5584-132">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="d5584-133">Grundlegendes zu DNSBL filtern</span><span class="sxs-lookup"><span data-stu-id="d5584-133">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="d5584-134">Invaluement</span><span class="sxs-lookup"><span data-stu-id="d5584-134">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="d5584-135">Anti Anti-Spam-Liste</span><span class="sxs-lookup"><span data-stu-id="d5584-135">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="d5584-136">Phishtank</span><span class="sxs-lookup"><span data-stu-id="d5584-136">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="d5584-137">PhishTank – häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="d5584-137">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="d5584-138">Exchange Online Protection verwendet auch Drittanbieter-Sperrlisten für Spam-Filterung.</span><span class="sxs-lookup"><span data-stu-id="d5584-138">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="d5584-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d5584-139">For more information</span></span>

[<span data-ttu-id="d5584-140">Konfigurieren der Richtlinie für ausgehende Spamnachrichten</span><span class="sxs-lookup"><span data-stu-id="d5584-140">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="d5584-141">Pool für besonders riskante Zustellungen für ausgehende Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d5584-141">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="d5584-142">Verwenden des Listenentfernungsportals, um sich selbst aus der Liste der blockierten Absender von Office 365 zu entfernen</span><span class="sxs-lookup"><span data-stu-id="d5584-142">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

