---
title: Listen sicherer und blockierter Absender in Exchange Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/22/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 111ab6b0-2dd2-4a87-a928-4931df6b3c4d
description: Als Exchange Online- oder Exchange Online Protection-Administrator (EOP) können Sie sicherstellen, dass eine E-Mail-Nachricht, die den Dienst durchläuft, nicht als Spam gekennzeichnet wird. Eine Möglichkeit hierzu ist das Erstellen von Listen mit sicheren Absendern und blockierten Absendern für die Personen in Ihrer Organisation.
ms.openlocfilehash: fcb43f990750782788dc6f459dd5c7d296146a38
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22028082"
---
# <a name="safe-sender-and-blocked-sender-lists-in-exchange-online"></a><span data-ttu-id="32ebf-104">Listen sicherer und blockierter Absender in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="32ebf-104">Safe sender and blocked sender lists in Exchange Online</span></span>

<span data-ttu-id="32ebf-p102">Als Exchange Online- oder Exchange Online Protection-Administrator (EOP) können Sie sicherstellen, dass eine E-Mail-Nachricht, die den Dienst durchläuft, nicht als Spam gekennzeichnet wird. Eine Möglichkeit hierzu ist das Erstellen von Listen mit sicheren Absendern und blockierten Absendern für die Personen in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="32ebf-p102">As an Exchange Online or Exchange Online Protection (EOP) administrator, you can help ensure that an email message traveling through the service isn't marked as spam. One way to do this is to create safe sender and blocked sender lists for the people in your organization.</span></span> 
  
 <span data-ttu-id="32ebf-107">*Informationen zum Verwenden dieser Listen als Administrator finden Sie in der aktuellen Version der Tipps und Verfahren unter* [Verhindern der Kennzeichnung von falsch positiver E-Mail als Spam mithilfe einer Liste sicherer Adressen oder anderer Techniken](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span><span class="sxs-lookup"><span data-stu-id="32ebf-107">*See the updated version of the tips and procedures for how to work with these lists as an admin in* [Prevent false positive email marked as spam with a safelist or other techniques](https://go.microsoft.com/fwlink/p/?LinkID=534224).</span></span> 
  
<span data-ttu-id="32ebf-108">Wenn Sie kein Administrator sind und einfach nur Ihre eigenen Junk-E-Mails in Outlook mithilfe einer Liste sicherer Absender verwalten möchten, sehen Sie sich die Schritte in diesem Überblick [der Junk-Filter](https://go.microsoft.com/fwlink/?LinkId=817222) an.</span><span class="sxs-lookup"><span data-stu-id="32ebf-108">If you're not an admin, and you just want to manage your own junk email in Outlook by using a safe sender list, check out the steps in this overview of [the Junk Email Filter](https://go.microsoft.com/fwlink/?LinkId=817222).</span></span> 
  
## <a name="what-is-the-safe-and-blocked-sender-limits-in-exchange-online"></a><span data-ttu-id="32ebf-109">Was sind die Grenzwerte sicherer und blockierter Absender in Exchange Online?</span><span class="sxs-lookup"><span data-stu-id="32ebf-109">What is the safe and blocked sender limits in Exchange Online?</span></span>

<span data-ttu-id="32ebf-p103">Die Grenzwerte sicherer und blockierter Absender in Exchange Online unterscheiden sich von den Grenzwerten von Active Directory und Outlook. Dies sind:</span><span class="sxs-lookup"><span data-stu-id="32ebf-p103">The safe and blocked sender limits in Exchange Online differ from the Active Directory and Outlook limits. They are:</span></span>
  
- <span data-ttu-id="32ebf-112">Grenzwert sicherer Absender: 1.024</span><span class="sxs-lookup"><span data-stu-id="32ebf-112">Safe sender limit: 1,024</span></span>
    
- <span data-ttu-id="32ebf-113">Grenzwert blockierter Absender: 500</span><span class="sxs-lookup"><span data-stu-id="32ebf-113">Blocked sender limit: 500</span></span>
    
<span data-ttu-id="32ebf-114">Hinweis:</span><span class="sxs-lookup"><span data-stu-id="32ebf-114">Note:</span></span>
  
<span data-ttu-id="32ebf-p104">Möglicherweise tritt der in KB 2590466 beschriebene Fehler auf (Die folgende Fehlermeldung wird in Outlook Web App für Exchange Server 2010 angezeigt: „Junk-E-Mail-Überprüfungsfehler"). Um dieses Problem zu beheben, deaktivieren Sie das Kontrollkästchen „E-Mails von meinen Kontakten vertrauen". Alternativ können Sie auch die Anzahl an E-Mail-Adressen reduzieren, die in dem standardmäßigen Ordner „Kontakte" enthalten sind, damit dieser Wert nicht den Grenzwert von 1.024 in Exchange Online überschreitet, der für das Attribut „MaxSafeSenders" festgelegt ist. Weitere Informationen über dieses Attribut und das Cmdlet „Set-Mailbox" finden Sie in dem folgenden Artikel:</span><span class="sxs-lookup"><span data-stu-id="32ebf-p104">You may experience the error that is described in KB 2590466 ("You receive the error "Junk e-mail validation error" in Outlook Web App for Exchange Server 2010"). To resolve this issue, clear the "Trust emails from my contacts" check box. Alternatively, decrease the amount of email addresses that are in your default Contacts folder to bring it within the maximum allowed limit of 1,024 in Exchange Online that is set for "MaxSafeSenders" attribute. For more information about this attribute and the Set-Mailbox cmdlet, seethe following topic:</span></span>
  
[<span data-ttu-id="32ebf-119">Set-Mailbox</span><span class="sxs-lookup"><span data-stu-id="32ebf-119">Set-Mailbox</span></span>](https://docs.microsoft.com/en-us/powershell/module/exchange/mailboxes/Set-Mailbox?view=exchange-ps)
  
## <a name="see-also"></a><span data-ttu-id="32ebf-120">See also</span><span class="sxs-lookup"><span data-stu-id="32ebf-120">See also</span></span>

[<span data-ttu-id="32ebf-121">Sender filtering in Exchange 2016</span><span class="sxs-lookup"><span data-stu-id="32ebf-121">Sender filtering in Exchange 2016</span></span>](http://technet.microsoft.com/library/b833f864-ff10-46a0-a653-28fb9ba30896.aspx)

