---
title: Verwenden von Spambenachrichtigungen für Benutzer zum Freigeben und Melden von isolierten Nachrichten in Office 365
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/12/2018
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
ms.openlocfilehash: 7f68b70298fca7d8ed5f5e5b8dc9c727c3a6a6c1
ms.sourcegitcommit: 5eb664b6ecef94aef4018a75684ee4ae66c486bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/08/2019
ms.locfileid: "30492724"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="17789-104">Verwenden von Spambenachrichtigungen für Benutzer zum Freigeben und Melden von isolierten Nachrichten in Office 365</span><span class="sxs-lookup"><span data-stu-id="17789-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="17789-105">Wenn Ihr Administrator Spambenachrichtigungen für Benutzer aktiviert, erhalten Sie eine Benachrichtigung, die an Ihr Postfach adressierte Nachrichten auflistet, die als Spam identifiziert und stattdessen isoliert wurden.</span><span class="sxs-lookup"><span data-stu-id="17789-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="17789-106">Wenn Sie ein Administrator sind und dieses Feature aktivieren möchten, können Sie die Option auswählen, wenn Sie [eine standardmäßige Antispampolitik ändern](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="17789-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="17789-107">Die Nachricht, die Sie erhalten, enthält die Anzahl von Nachrichten in Spamquarantäne und das Datum und die Uhrzeit (in UTC) der letzten Nachricht in der Liste.</span><span class="sxs-lookup"><span data-stu-id="17789-107">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list.</span></span> <span data-ttu-id="17789-108">Die Liste enthält für jede Nachricht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="17789-108">The list includes the following for each message:</span></span>
  
- <span data-ttu-id="17789-109">**Absender** Der Absender Name und die e-Mail-Adresse der isolierten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="17789-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="17789-110">**Betreff** Der Betreffzeilentext der in Quarantäne verschobenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="17789-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="17789-111">**Datum** Datum und Uhrzeit (UTC-Angabe) der Verschiebung der Nachricht in Quarantäne.</span><span class="sxs-lookup"><span data-stu-id="17789-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="17789-112">**Größe** Die Größe der Nachricht in Kilobyte (KBs).</span><span class="sxs-lookup"><span data-stu-id="17789-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="17789-113">Derzeit gibt es zwei Aktionen, die Sie mit einer isolierten Nachricht durchführen können:</span><span class="sxs-lookup"><span data-stu-id="17789-113">Currently, there are two actions you can take with a quarantined message:</span></span>
  
- <span data-ttu-id="17789-114">Im **Posteingang freigeben** Wählen Sie diese Option aus, um die Nachricht an Ihren Posteingang zu senden, wo Sie Sie anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="17789-114">**Release to Inbox** Choose this to send the message to your inbox, where you can view it.</span></span> 
    
- <span data-ttu-id="17789-115">**Bericht als nicht-Junk** Wählen Sie diese Option aus, um eine Kopie der Nachricht zur Analyse an Microsoft zu senden.</span><span class="sxs-lookup"><span data-stu-id="17789-115">**Report as Not Junk** Choose this to send a copy of the message to Microsoft for analysis.</span></span> <span data-ttu-id="17789-116">Das Spamteam bewertet und analysiert die Nachricht und passt, je nach Analyseergebnis, die Antispamfilterregeln so an, dass die Nachricht übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="17789-116">The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span> 
    
<span data-ttu-id="17789-117">Beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="17789-117">Be aware of the following:</span></span>
  
- <span data-ttu-id="17789-118">Nachrichten, die unter Quarantäne gestellt werden, da Sie mit einer Nachrichtenfluss Regel übereinstimmen, sind nicht in Benutzer isolierten Nachrichten enthalten.</span><span class="sxs-lookup"><span data-stu-id="17789-118">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages.</span></span> <span data-ttu-id="17789-119">Es werden nur Spamquarantäne-Nachrichten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="17789-119">Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="17789-120">Sie können eine Nachricht nur einmal freigeben und als falsch positiv markiert (keine Junk-E-Mail) melden.</span><span class="sxs-lookup"><span data-stu-id="17789-120">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

