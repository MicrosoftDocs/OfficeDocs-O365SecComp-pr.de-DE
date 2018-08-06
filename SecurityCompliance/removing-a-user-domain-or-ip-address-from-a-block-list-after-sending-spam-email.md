---
title: Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/20/2018
ms.audience: ITPro
ms.topic: article
f1_keywords:
- ms.exch.eac.ActionCenter
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 712cfcc1-31e8-4e51-8561-b64258a8f1e5
description: 'Wenn Benutzer ständig E-Mails von Office 365 senden, die als Spam klassifiziert werden, werden diese blockiert, sodass sie keine weiteren E-Mails senden können. '
ms.openlocfilehash: ce52ddfd96b582911bb519c15bbfe90351946db8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026332"
---
# <a name="removing-a-user-domain-or-ip-address-from-a-block-list-after-sending-spam-email"></a><span data-ttu-id="cfaa7-103">Entfernen von Benutzern, Domänen oder IP-Adressen aus einer Sperrliste nach dem Senden von Spamnachrichten</span><span class="sxs-lookup"><span data-stu-id="cfaa7-103">Removing a user, domain, or IP address from a block list after sending spam email</span></span>

<span data-ttu-id="cfaa7-104">Wenn Benutzer ständig E-Mails von Office 365 senden, die als Spam klassifiziert werden, werden diese blockiert, sodass sie keine weiteren E-Mails senden können. </span><span class="sxs-lookup"><span data-stu-id="cfaa7-104">If a user continuously sends email messages from Office 365 that is classified as spam, they will be blocked from sending any more messages.</span></span> 
  
<span data-ttu-id="cfaa7-105">
Wenn Absender blockiert sind und keine E-Mails senden können, erhalten sie einen Unzustellbarkeitsbericht (oder eine Meldung, dass beim Senden der Nachricht ein Fehler aufgetreten ist) mit Informationen, wie sie vorgehen müssen, um die Blockierung aufzuheben.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-105">When a sender is blocked from sending emails messages, they receive a Non-Delivery Report (NDR or email failed to send message) that provides specific information about the steps that they have to take to unblock themselves.</span></span>
  
<span data-ttu-id="cfaa7-p101">Nicht nur können einzelne Benutzern durch die Domänen Service, sondern auf bestimmte Websites blockiert und IP-Adressen können auch blockiert werden. In einigen Fällen können Domänen oder Websites einer Sperrliste hinzugefügt werden einfach, da sie in einer Spam-Nachricht angezeigt werden. Als der Office 365-Administrator können Sie versuchen, erhalten Benutzer, Websites, Domänen und IP-Adressen von Drittanbieter-Sperrlisten entfernt. Verwenden Sie die Links in der Tabelle unten in diesem Thema, um jede Drittanbieter zu kontaktieren, und folgen Sie den Anweisungen. Wenn eine Person außerhalb von Office 365 mit Ihrem Office 365-Konto Nachrichten senden kann, ihr Konto möglicherweise auf die Liste der blockierten Absender externe beendet wurden einrichten. Benutzer außerhalb von Office 365 können sich selbst aus der Liste blockierter Absender So entfernen Sie mithilfe der [Self-service-delisting Portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx)versuchen.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-p101">Not only can individual users be blocked by the service, but specific websites, domains, and IP addresses can also be blocked. In some cases, domains or websites can be added to a block list just because they appear in a spam message. As the Office 365 admin, you can try to get users, websites, domains, and IP addresses removed from third-party block lists. Use the links in the table at the bottom of this topic to contact each third party, and then follow the instructions. If someone outside Office 365 cannot send messages to your Office 365 account, their account may have ended up on the external blocked senders list. Users outside Office 365 can try to remove themselves from the blocked senders list by using the [self-service delisting portal](https://technet.microsoft.com/library/mt661881%28v=exchg.150%29.aspx).</span></span>
  
<span data-ttu-id="cfaa7-p102">Sie können ausgehende Spameinstellungen konfigurieren, damit Sie eine Benachrichtigung erhalten, wenn ein Office 365-Benutzer blockiert ist und keine E-Mail senden kann, die als Spam klassifiziert wurden. Wenn das Problem mit dem Benutzerpostfach behoben ist, können Sie die Blockierung für diesen Absender aufheben.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-p102">You can configure outbound spam settings so that you get anotification when an Office 365 user is blocked from sending email that's classified as spam. After the problem with the user's mailbox is resolved, you can remove the block on that sender.</span></span>
  
## <a name="unblock-a-blocked-office-365-email-account"></a><span data-ttu-id="cfaa7-114">Aufheben der Blockierung eines gesperrten Office 365-E-Mail-Kontos</span><span class="sxs-lookup"><span data-stu-id="cfaa7-114">Unblock a blocked Office 365 email account</span></span>

<span data-ttu-id="cfaa7-p103">Sie führen Sie diese Aufgabe in der Exchange-Verwaltungskonsole (EAC). Checken Sie [Exchange-Verwaltungskonsole in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) ausführliche Informationen zu der Exchange-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-p103">You complete this task in the Exchange admin center (EAC). Check out [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md) for details about the EAC.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cfaa7-117">Das Wartungscenter wird nur angezeigt, wenn Sie sich im EAC für Exchange Online befinden.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-117">You won't see the action center unless you're in the EAC for Exchange Online.</span></span> 
  
1. <span data-ttu-id="cfaa7-118">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **Aktion Center**.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-118">In the EAC, navigate to **protection** \> **action center**.</span></span>
    
    ![Navigieren Sie im Exchange Admin Center zum Wartungscenter](media/9bbf0844-7b34-4a86-a2b7-8c7e9c8519a3.png)
  
2. <span data-ttu-id="cfaa7-120">Wählen Sie das Symbol **Suche** aus, und geben Sie die SMTP-Adresse des blockierten Benutzers ein.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-120">Select the **Search** icon, and then enter the SMTP address of the blocked user.</span></span> 
    
    ![Suchen nach einem gesperrten Benutzer im Wartungscenter](media/f931b5a0-7115-4d95-9f6f-b403436031ba.png)
  
3. <span data-ttu-id="cfaa7-122">Klicken Sie im Bereich „Beschreibung“ auf **Sperrung des Kontos aufheben**.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-122">Click **Unblock Account** in the description pane.</span></span> 
    
    ![Aufheben der Blockierung eines Benutzers im Wartungscenter](media/c5d5b1b9-8416-45aa-9631-881e94d1d056.png)
  
4. <span data-ttu-id="cfaa7-124">Klicken Sie zur Bestätigung der Änderung auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-124">Click **Yes** to confirm the change.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="cfaa7-p104">Es gibt eine Einschränkung dabei, wie oft ein Mandantenadministrator die Blockierung für ein Konto aufheben darf. Wenn der Grenzwert für einen Benutzer überschritten wurde, wird eine Fehlermeldung angezeigt. Wenden Sie sich an den Support, um den Benutzer zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-p104">There's a limit to the number of times that an account can be unblocked by the tenant admin. If the limit for a user has been exceeded, an error message appears. Contact Support to unblock the user.</span></span> 
  
## <a name="third-party-block-lists"></a><span data-ttu-id="cfaa7-127">Drittanbieter-Blockierungslisten</span><span class="sxs-lookup"><span data-stu-id="cfaa7-127">Third-party block lists</span></span>

|<span data-ttu-id="cfaa7-128">**Name der Liste**</span><span class="sxs-lookup"><span data-stu-id="cfaa7-128">**List Name**</span></span>|<span data-ttu-id="cfaa7-129">**Abwahlportal**</span><span class="sxs-lookup"><span data-stu-id="cfaa7-129">**Delisting Portal**</span></span>|<span data-ttu-id="cfaa7-130">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="cfaa7-130">**For more information**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cfaa7-131">URIBL</span><span class="sxs-lookup"><span data-stu-id="cfaa7-131">URIBL</span></span>  <br/> |[https://admin.uribl.com/?section=lookup](https://admin.uribl.com/?section=lookup) <br/> |[<span data-ttu-id="cfaa7-132">URIBL-website</span><span class="sxs-lookup"><span data-stu-id="cfaa7-132"> URIBL website </span></span>](https://uribl.com/) <br/> |
|<span data-ttu-id="cfaa7-133">SURBL</span><span class="sxs-lookup"><span data-stu-id="cfaa7-133">SURBL</span></span>  <br/> |[http://www.surbl.org/surbl-analysis](http://www.surbl.org/surbl-analysis) <br/> |[<span data-ttu-id="cfaa7-134">Einführung in SURBL URI Reputation Daten</span><span class="sxs-lookup"><span data-stu-id="cfaa7-134">Introducing SURBL URI reputation data</span></span>](http://www.surbl.org/) <br/> |
|<span data-ttu-id="cfaa7-135">Spamhaus </span><span class="sxs-lookup"><span data-stu-id="cfaa7-135">Spamhaus</span></span>  <br/> |[https://www.spamhaus.org/lookup/](https://www.spamhaus.org/lookup/) <br/> |[<span data-ttu-id="cfaa7-136">Grundlegendes zu DNSBL filtern</span><span class="sxs-lookup"><span data-stu-id="cfaa7-136">Understanding DNSBL Filtering</span></span>](https://www.spamhaus.org/whitepapers/dnsbl_function/) <br/> |
|<span data-ttu-id="cfaa7-137">Invaluement</span><span class="sxs-lookup"><span data-stu-id="cfaa7-137">invaluement</span></span>  <br/> |[http://dnsbl.invaluement.com/lookup/](http://dnsbl.invaluement.com/lookup/) <br/> |[<span data-ttu-id="cfaa7-138">Anti Anti-Spam-Liste</span><span class="sxs-lookup"><span data-stu-id="cfaa7-138">invaluement anti-spam list</span></span>](http://dnsbl.invaluement.com/) <br/> |
|<span data-ttu-id="cfaa7-139">Phishtank</span><span class="sxs-lookup"><span data-stu-id="cfaa7-139">Phishtank</span></span>  <br/> |[https://www.phishtank.com/](https://www.phishtank.com/) <br/> |[<span data-ttu-id="cfaa7-140">PhishTank – häufig gestellte Fragen</span><span class="sxs-lookup"><span data-stu-id="cfaa7-140">PhishTank FAQ</span></span>](https://www.phishtank.com/faq.php) <br/> |
   
> [!NOTE]
> <span data-ttu-id="cfaa7-141">Exchange Online Protection verwendet auch Drittanbieter-Sperrlisten für Spam-Filterung.</span><span class="sxs-lookup"><span data-stu-id="cfaa7-141">Exchange Online Protection also uses third-party block lists for spam filtering.</span></span> 
   
## <a name="for-more-information"></a><span data-ttu-id="cfaa7-142">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cfaa7-142">For more information</span></span>

[<span data-ttu-id="cfaa7-143">Konfigurieren der Richtlinie für ausgehende Spamnachrichten</span><span class="sxs-lookup"><span data-stu-id="cfaa7-143">Configure the outbound spam policy</span></span>](configure-the-outbound-spam-policy.md)
  
[<span data-ttu-id="cfaa7-144">Pool für besonders riskante Zustellungen für ausgehende Nachrichten</span><span class="sxs-lookup"><span data-stu-id="cfaa7-144">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="cfaa7-145">Verwenden des Listenentfernungsportals, um sich selbst aus der Liste der blockierten Absender von Office 365 zu entfernen</span><span class="sxs-lookup"><span data-stu-id="cfaa7-145">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md)
  

  

