---
title: Beispielbenachrichtigung, wenn ein Absender aufgrund des Versendens von ausgehendem Spam blockiert wird
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/2/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: c33fd406-a4c8-4ac8-ad85-123996c5cded
description: 'Wenn ein Absender vom Dienst blockiert wird, weil er ausgehenden Spam sendet, erhält der angegebene Domänenadministrator, wenn Sie Konfigurieren der Richtlinie für ausgehende Spamnachrichten, eine E-Mail-Benachrichtigung ähnlich der folgenden:'
ms.openlocfilehash: c9954d3ea16582a66185d574bcb5fc8a1aeebbf9
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027462"
---
# <a name="sample-notification-when-a-sender-is-blocked-sending-outbound-spam"></a><span data-ttu-id="75609-103">Beispielbenachrichtigung, wenn ein Absender aufgrund des Versendens von ausgehendem Spam blockiert wird</span><span class="sxs-lookup"><span data-stu-id="75609-103">Sample notification when a sender is blocked sending outbound spam</span></span>

<span data-ttu-id="75609-104">Wenn ein Absender vom Dienst blockiert wird, weil er ausgehenden Spam sendet, erhält der angegebene Domänenadministrator, wenn Sie [Konfigurieren der Richtlinie für ausgehende Spamnachrichten](configure-the-outbound-spam-policy.md), eine E-Mail-Benachrichtigung ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="75609-104">When a sender is blocked from the service due to sending outbound spam, the domain admin specified when you [Configure the outbound spam policy](configure-the-outbound-spam-policy.md) will receive a notification email similar to the following:</span></span> 
  
 <span data-ttu-id="75609-105">**Absenderadresse:** spamalerts@microsoft.com</span><span class="sxs-lookup"><span data-stu-id="75609-105">**Sender address:** spamalerts@microsoft.com</span></span> 
  
 <span data-ttu-id="75609-106">**Betreff:** Benachrichtigung wegen ausgehendem Spam - \<  *Kontoname*  \> wurde für das Senden von ausgehenden E-Mails blockiert</span><span class="sxs-lookup"><span data-stu-id="75609-106">**Subject:** Outbound spam notification - \<  *account name*  \> blocked from sending outbound mail</span></span> 
  
 <span data-ttu-id="75609-107">**Nachrichtentext:** Dies ist eine automatische Antwort vom Spamanalysesystem von Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="75609-107">**Body:** This is an automated reply from the Exchange Online Protection Spam Analysis System.</span></span> 
  
<span data-ttu-id="75609-p101">Sie werden kontaktiert, da wir große Mengen als Spam gekennzeichnete E-Mails oder ein anderes verdächtiges Verhalten ausgehend von Ihrer Organisation bemerkt haben. Für die folgenden E-Mail-Konten wurde das Senden von E-Mails blockiert (E-Mail-Empfang ist weiterhin möglich):</span><span class="sxs-lookup"><span data-stu-id="75609-p101">You are being contacted because we have detected high volumes of email marked as spam, or other suspicious behavior, originating from your organization. The following email accounts have been blocked from sending email (they can still receive email):</span></span>
  
<span data-ttu-id="75609-110">\< *Kontoname*  \></span><span class="sxs-lookup"><span data-stu-id="75609-110">\< *account name*  \></span></span> 
  
<span data-ttu-id="75609-p102">Es ist wahrscheinlich, dass dieses E-Mail-Konto angegriffen wurde. Führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="75609-p102">It is likely that this email account has been compromised. Please follow these steps:</span></span>
  
1. <span data-ttu-id="75609-113">Beheben Sie dieses Problem auf Ihrer Seite durch folgende Maßnahmen:</span><span class="sxs-lookup"><span data-stu-id="75609-113">Resolve this issue on your side by:</span></span>
    
  - <span data-ttu-id="75609-114">Ändern Sie das Kennwort des Kontos.</span><span class="sxs-lookup"><span data-stu-id="75609-114">Changing the password of the account.</span></span>
    
  - <span data-ttu-id="75609-115">Ermitteln Sie, wie das Konto angegriffen wurde.</span><span class="sxs-lookup"><span data-stu-id="75609-115">Determining how the account was compromised.</span></span>
    
  - <span data-ttu-id="75609-116">Ergreifen Sie Vorsichtsmaßnahmen, um sicherzustellen, dass dieses Sicherheitsrisiko nicht erneut ausgenutzt wird.</span><span class="sxs-lookup"><span data-stu-id="75609-116">Taking precautions to ensure that this vulnerability will not be exploited again.</span></span>
    
  - <span data-ttu-id="75609-117">Bestätigen Sie, dass alle problematischen Nachrichten aus Ihrer Postausgangswarteschlange gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="75609-117">Confirming that your outbound mail queue has been cleared of all offending messages.</span></span>
    
2. <span data-ttu-id="75609-118">Wenden Sie sich über Ihren normalen Kontaktkanal an den Microsoft-Support.</span><span class="sxs-lookup"><span data-stu-id="75609-118">Contact Microsoft support by using your regular contact channel.</span></span>
    
3. <span data-ttu-id="75609-119">Erläutern Sie, dass für einen Ihrer Benutzer das Senden von E-Mails blockiert und das Problem behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="75609-119">Explain that you have a user that is blocked from sending mail and that the problem has been dealt with.</span></span>
    
4. <span data-ttu-id="75609-120">Der Mitarbeiter erstellt ein Supportticket mit den angegebenen Informationen und leitet es weiter, damit die Blockierung der E-Mail-Adresse oder Domäne aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="75609-120">The agent will create a support ticket with the information that you provide and escalate it to have the email address or domain unblocked.</span></span>
    
5. <span data-ttu-id="75609-121">Nachdem die Blockierung der E-Mail-Adresse aufgehoben wurde und vorausgesetzt, dass keine anderen Probleme bestehen, werden Sie kontaktiert und über die Aufhebung der Blockierung informiert.</span><span class="sxs-lookup"><span data-stu-id="75609-121">After the address has been unblocked, and pending no other issues, you will be contacted and alerted to the unblocking.</span></span>
    
<span data-ttu-id="75609-122">Vielen Dank für Ihre Unterstützung bei der Kontrolle von unerwünschten E-Mails.</span><span class="sxs-lookup"><span data-stu-id="75609-122">Thank you for assisting us in controlling unwanted email.</span></span>
  
<span data-ttu-id="75609-123">Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="75609-123">Exchange Online Protection.</span></span>
  
<span data-ttu-id="75609-124">\*\*HINWEIS: Antworten Sie nicht auf diese E-Mail, da sie von einer nicht überwachten Adresse gesendet wurde.\*\*</span><span class="sxs-lookup"><span data-stu-id="75609-124">\*\*NOTE - Please do not respond to this email as it is sent from an unmonitored address\*\*</span></span>
  
> [!TIP]
> <span data-ttu-id="75609-125">Sie können auch Kontaktieren des Supports über die Optionen unter [Hilfe und Support für EOP](eop/help-and-support-for-eop.md)dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="75609-125">You can also contact support via the options documented at [Help and support for EOP](eop/help-and-support-for-eop.md).</span></span> 
  

