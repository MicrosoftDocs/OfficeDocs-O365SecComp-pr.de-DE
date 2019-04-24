---
title: Verwenden von Spambenachrichtigungen für Benutzer zum Freigeben und Melden von isolierten Nachrichten in Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 03/14/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
ms.collection:
- M365-security-compliance
description: Wenn Ihr Administrator die Benachrichtigungen für Benutzer aktiviert, erhalten Sie eine Benachrichtigung, die an Ihr Postfach gesendete Nachrichten auflistet, die als Spam, Massen oder Phishing-Nachrichten identifiziert wurden. Sie können Nachrichten nach der Benachrichtigung freigeben oder melden.
ms.openlocfilehash: de67987b0028102bdf61889ce54ca4215182e279
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263437"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="2843e-104">Verwenden von Spambenachrichtigungen für Benutzer zum Freigeben und Melden von isolierten Nachrichten in Office 365</span><span class="sxs-lookup"><span data-stu-id="2843e-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="2843e-105">Wenn Ihr Administrator Spambenachrichtigungen für Benutzer aktiviert, erhalten Sie eine Benachrichtigung, die an Ihr Postfach adressierte Nachrichten auflistet, die als Spam identifiziert und stattdessen isoliert wurden.</span><span class="sxs-lookup"><span data-stu-id="2843e-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="2843e-106">Wenn Sie ein Administrator sind und dieses Feature aktivieren möchten, können Sie die Option auswählen, wenn Sie [eine standardmäßige Antispampolitik ändern](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="2843e-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="2843e-107">Die Nachricht, die Sie erhalten, enthält die Anzahl von Nachrichten in Spamquarantäne und das Datum und die Uhrzeit (in UTC) der letzten Nachricht in der Liste.</span><span class="sxs-lookup"><span data-stu-id="2843e-107">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list.</span></span> <span data-ttu-id="2843e-108">Die Liste enthält für jede Nachricht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2843e-108">The list includes the following for each message:</span></span>
  
- <span data-ttu-id="2843e-109">**Absender** Der Absender Name und die e-Mail-Adresse der isolierten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2843e-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="2843e-110">**Betreff** Der Betreffzeilentext der in Quarantäne verschobenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="2843e-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="2843e-111">**Datum** Datum und Uhrzeit (UTC-Angabe) der Verschiebung der Nachricht in Quarantäne.</span><span class="sxs-lookup"><span data-stu-id="2843e-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="2843e-112">**Größe** Die Größe der Nachricht in Kilobyte (KBs).</span><span class="sxs-lookup"><span data-stu-id="2843e-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="2843e-113">Dies sind die Aktionen, die Sie mit einer isolierten Nachricht ausführen können:</span><span class="sxs-lookup"><span data-stu-id="2843e-113">These are the actions that you can take with a quarantined message:</span></span>

- <span data-ttu-id="2843e-114">Zeigen Sie eine **Vorschau** der Nachricht an, wenn Sie eine Vorschau des Inhalts oder der Kopfzeile vor der Aktion anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="2843e-114">**Preview** the message if you would like to preview the content or header prior to taking action.</span></span>

- <span data-ttu-id="2843e-115">**Laden** Sie die Nachricht herunter, wenn Sie die Nachricht und die Anhänge (falls vorhanden) auf Ihrem Gerät vor der Aktion überarbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="2843e-115">**Download** the message if you would like to review the message and attachments (if any) on your device prior to taking action.</span></span>

- <span data-ttu-id="2843e-116">**Release** , wenn es sich bei der Nachricht nicht um Spam handelt und Sie möchten, dass Office 365 die Nachricht an Ihr Postfach sendet.</span><span class="sxs-lookup"><span data-stu-id="2843e-116">**Release** if the message isn’t spam and you want Office 365 to send the message to your mailbox.</span></span>

- <span data-ttu-id="2843e-117">**Release _AMP_ Allow Absender** , wenn die Nachricht nicht Spam ist und Sie möchten, dass Office 365 den Absender zur Liste sicherer Absender und Empfänger für zukünftige e-Mails hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2843e-117">**Release & Allow Sender** if the message isn’t spam and you want Office 365 to add the sender to your safe senders and recipients list for future emails.</span></span> <span data-ttu-id="2843e-118">Denken Sie daran, dass Ihr Administrator möglicherweise andere organisationsweite Allow/Block-Konfigurationen besitzt, die Ihre Liste sicherer Absender außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="2843e-118">Keep in mind that your admin may have other organization wide allow/block configurations that override your safe sender list.</span></span>

- <span data-ttu-id="2843e-119">**Veröffentlichen Sie _AMP_ Bericht**, wenn es sich bei der Nachricht nicht um Spam handelt und Sie die Nachricht an Ihr Postfach senden und zu Analyseberichten möchten.</span><span class="sxs-lookup"><span data-stu-id="2843e-119">**Release & Report**, if the message isn’t spam and you want to send the message to your mailbox and report it to Microsoft for analysis.</span></span>

- <span data-ttu-id="2843e-120">**Blockieren** Wenn Sie möchten, dass Office 365 den Absender zu Ihrer Liste blockierter Absender hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="2843e-120">**Block** if you want Office 365 to add the sender to your blocked senders list.</span></span>

<span data-ttu-id="2843e-121">Beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2843e-121">Be aware of the following:</span></span>
  
- <span data-ttu-id="2843e-122">Nachrichten, die unter Quarantäne gestellt werden, da Sie mit einer Nachrichtenfluss Regel übereinstimmen, sind nicht in Benutzer isolierten Nachrichten enthalten.</span><span class="sxs-lookup"><span data-stu-id="2843e-122">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages.</span></span> <span data-ttu-id="2843e-123">Es werden nur Spamquarantäne-Nachrichten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2843e-123">Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="2843e-124">Sie können eine Nachricht nur einmal freigeben und als falsch positiv markiert (keine Junk-E-Mail) melden.</span><span class="sxs-lookup"><span data-stu-id="2843e-124">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

