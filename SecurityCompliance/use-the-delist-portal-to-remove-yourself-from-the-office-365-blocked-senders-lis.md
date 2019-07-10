---
title: Verwenden des Listenentfernungsportals, um sich selbst aus der Liste der blockierten Absender von Office 365 zu entfernen
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 04/18/2016
audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0bcecdd4-3343-4cc0-9e58-e19d4de515e8
ms.collection:
- M365-security-compliance
description: Erhalten Sie eine Fehlermeldung, wenn Sie versuchen, eine E-Mail an einen Empfänger zu senden, dessen E-Mail-Adresse sich in Office 365 befindet? Wenn Sie glauben, dass Sie die Fehlermeldung nicht erhalten sollten, können Sie das Listenentfernungsportal verwenden, um sich selbst aus der Liste der blockierten Absender von Office 365 zu entfernen.
ms.openlocfilehash: 18ec4956b8d37308e7ec35c8fc28f24d36cd2763
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2019
ms.locfileid: "35598431"
---
# <a name="use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-list"></a><span data-ttu-id="f6006-104">Verwenden des Listenentfernungsportals, um sich selbst aus der Liste der blockierten Absender von Office 365 zu entfernen</span><span class="sxs-lookup"><span data-stu-id="f6006-104">Use the delist portal to remove yourself from the Office 365 blocked senders list</span></span>

<span data-ttu-id="f6006-p102">Erhalten Sie eine Fehlermeldung, wenn Sie versuchen, eine E-Mail an einen Empfänger zu senden, dessen E-Mail-Adresse sich in Office 365 befindet? Wenn Sie glauben, dass Sie die Fehlermeldung nicht erhalten sollten, können Sie das Listenentfernungsportal verwenden, um sich selbst aus der Liste der blockierten Absender von Office 365 zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f6006-p102">Are you getting an error message when you try to send an email to a recipient whose email address is in Office 365? If you think you should not be receiving the error message, you can use the delist portal to remove yourself from the Office 365 blocked senders list.</span></span>
  
## <a name="what-is-the-office-365-blocked-senders-list"></a><span data-ttu-id="f6006-107">Was ist die Liste der blockierten Absender von Office 365?</span><span class="sxs-lookup"><span data-stu-id="f6006-107">What is the Office 365 blocked senders list?</span></span>

<span data-ttu-id="f6006-p103">Microsoft verwendet die Liste der blockierten Absender, um seine Kunden vor Spam, Spoofing und Phishingangriffen zu schützen. Die IP-Adresse Ihres E-Mail-Servers, d. h. die Adresse, mit der sich Ihr E-Mail-Server im Internet identifiziert, wurde aus einem von vielen möglichen Gründen als mögliche Bedrohung für Office 365 kategorisiert. Wenn Office 365 die IP-Adresse zu der Liste hinzufügt, wird jede weitere Kommunikation zwischen der IP-Adresse und unseren Kunden über unsere Rechenzentren verhindert.</span><span class="sxs-lookup"><span data-stu-id="f6006-p103">Microsoft uses the blocked senders list to protect its customers from spam, spoofing, and phishing attacks. Your mail server's IP address, that is, the address your mail server uses to identify itself on the Internet, was tagged as a potential threat to Office 365 for one of a variety of reasons. When Office 365 adds the IP address to the list, it prevents all further communication between the IP address and any of our customers through our datacenters.</span></span>
  
<span data-ttu-id="f6006-111">Sie merken, dass Sie der Liste hinzugefügt wurden, wenn Sie auf eine E-Mail eine Antwort erhalten, die in etwa folgende Fehlermeldung enthält:</span><span class="sxs-lookup"><span data-stu-id="f6006-111">You will know you have been added to the list when you receive a response to a mail message that includes an error that looks something like this:</span></span>
  
> <span data-ttu-id="f6006-112">550 5.7.606-649 Zugriff verweigert, verbannte Absender IP [_IP-Adresse_]; Wenn Sie die Entfernung aus dieser Liste anfordern https://sender.office.com/ möchten, besuchen Sie die Anweisungen, und befolgen Sie diese.</span><span class="sxs-lookup"><span data-stu-id="f6006-112">550 5.7.606-649 Access denied, banned sending IP [_IP address_]; To request removal from this list please visit https://sender.office.com/ and follow the directions.</span></span> <span data-ttu-id="f6006-113">Weitere Informationen finden Sie unter [e-Mail-Unzustellbarkeitsberichte in Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).</span><span class="sxs-lookup"><span data-stu-id="f6006-113">For more information please see [Email non-delivery reports in Office 365](http://go.microsoft.com/fwlink/?LinkID=526653).</span></span>
  
<span data-ttu-id="f6006-114">wobei  _IP address_ die IP-Adresse des Computers ist, auf dem der E-Mail-Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6006-114">where  _IP address_ is the IP address of the computer on which the mail server runs.</span></span> 
  
### <a name="to-use-the-office-365-delist-portal-to-remove-yourself-from-the-blocked-senders-list"></a><span data-ttu-id="f6006-115">So verwenden Sie das Listenentfernungsportal von Office 365, um sich selbst aus der Liste der blockierten Absender zu entfernen</span><span class="sxs-lookup"><span data-stu-id="f6006-115">To use the Office 365 delist portal to remove yourself from the blocked senders list</span></span>

1. <span data-ttu-id="f6006-116">Wechseln Sie in einem Webbrowser zu [https://sender.office.com](https://sender.office.com).</span><span class="sxs-lookup"><span data-stu-id="f6006-116">In a web browser, go to [https://sender.office.com](https://sender.office.com).</span></span>
    
2. <span data-ttu-id="f6006-p105">Folgen Sie den Anweisungen auf dem Bildschirm. Verwenden Sie die E-Mail-Adresse, an die die Fehlermeldung gesendet wurde, und die IP-Adresse, die in der Fehlermeldung angegeben ist. Sie können nur eine E-Mail-Adresse und eine IP-Adresse pro Besuch eingeben.</span><span class="sxs-lookup"><span data-stu-id="f6006-p105">Follow the instructions on the page. Ensure that you use the email address to which the error message was sent, and the IP address that is specified in the error message. You can only enter one email address and one IP address per visit.</span></span>
    
3. <span data-ttu-id="f6006-120">Klicken Sie auf **Senden**.</span><span class="sxs-lookup"><span data-stu-id="f6006-120">Click **Submit**.</span></span>
    
    <span data-ttu-id="f6006-121">Das Portal sendet eine E-Mail an die E-Mail-Adresse, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="f6006-121">The portal sends an email to the email address that you supply.</span></span> <span data-ttu-id="f6006-122">Die e-Mail sieht in etwa wie folgt aus: ![Screenshot der empfangenen e-Mail, wenn Sie eine Anforderung über das Delist-Portal senden](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span><span class="sxs-lookup"><span data-stu-id="f6006-122">The email will look something like the following: ![Screenshot of email received when you submit a request through the delist portal](media/bf13e4f7-f68c-4e46-baa7-b6ab4cfc13f3.png)</span></span>
  
4. <span data-ttu-id="f6006-123">Klicken Sie auf den Bestätigungslink in der E-Mail, die vom Listenentfernungsportal an Sie gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f6006-123">Click the confirmation link in the email sent to you by the delisting portal.</span></span>
    
    <span data-ttu-id="f6006-124">Damit kehren Sie zum Azure-Listenentfernungsportal zurück.</span><span class="sxs-lookup"><span data-stu-id="f6006-124">This brings you back to the delist portal.</span></span>
    
5. <span data-ttu-id="f6006-125">Klicken Sie im Listenentfernungsportal auf **IP aus Liste entfernen**.</span><span class="sxs-lookup"><span data-stu-id="f6006-125">In the delist portal, click **Delist IP**.</span></span>
    
    <span data-ttu-id="f6006-p107">Nachdem Sie die IP-Adresse aus der Liste der blockierten Absender entfernt haben, werden E-Mails von dieser IP-Adresse Empfängern mit Office 365 wieder zugestellt. Stellen Sie daher sicher, dass die E-Mails von dieser IP-Adresse keine beleidigenden oder böswilligen Inhalte aufweisen, da die IP-Adresse anderenfalls erneut blockiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6006-p107">After the IP address is removed from the blocked senders list, email messages from that IP address will be delivered to recipients who use Office 365. So, make sure you're confident that email sent from that IP address won't be abusive or malicious; otherwise, the IP address might be blocked again.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="f6006-128">Es kann bis zu 24 Stunden dauern, oder die Ergebnisse können stark variieren, bevor Einschränkungen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="f6006-128">It may take up to 24 hours or results can vary widely before restrictions are removed.</span></span>
    
<span data-ttu-id="f6006-129">In diesem Artikel erfahren Sie [, wie Sie verhindern können, dass echte e-Mails in Office 365 als Spam markiert](prevent-email-from-being-marked-as-spam.md ) und [ausgehende Spam in Office 365 gesteuert](outbound-spam-controls.md) werden, um zu verhindern, dass IP auf die schwarze Liste gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f6006-129">Read about [How to prevent real email from being marked as spam in Office 365](prevent-email-from-being-marked-as-spam.md ) and [Controlling outbound spam in Office 365](outbound-spam-controls.md) to prevent IP from being blacklisted.</span></span>
