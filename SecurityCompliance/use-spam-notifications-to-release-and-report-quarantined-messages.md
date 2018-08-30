---
title: Verwenden von spambenachrichtigungen für Benutzer zum Freigeben und Melden von Nachrichten in Quarantäne in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 5/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 56de4ed5-b0aa-4195-9f46-033d7cc086bc
description: Wenn Ihr Administrator die Benachrichtigungen für Benutzer aktiviert, erhalten Sie eine Benachrichtigung, die an Ihr Postfach gesendete Nachrichten sind aufgeführt, die als Spam, Massen oder Phishing-Nachrichten erkannt wurden. Sie können Version oder den Bericht Nachrichten nach benachrichtigt wird.
ms.openlocfilehash: e355a94af5ac295503a8e205b1a896afc1c54fb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529197"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="feba4-104">Verwenden von spambenachrichtigungen für Benutzer zum Freigeben und Melden von Nachrichten in Quarantäne in Office 365</span><span class="sxs-lookup"><span data-stu-id="feba4-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="feba4-105">Der Admin-spambenachrichtigungen für Benutzer aktiviert, erhalten Sie eine Benachrichtigung, in der Nachrichten an Ihr Postfach, die als Spam identifiziert wurden und unter Quarantäne gestellte e-Mails stattdessen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="feba4-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="feba4-106">Wenn Sie Administrator an, und dieses Feature aktivieren möchten sind, können Sie wählen Sie die Option Wenn Sie [eine standardmäßige Anti-Spam-Richtlinie zu ändern](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="feba4-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="feba4-p102">Die empfangenen Nachricht enthält die Anzahl der Nachrichten in Spam-Quarantäne, die Ihnen, sowie Datum und Uhrzeit (in koordinierter Weltzeit oder UTC) der letzten Nachricht in der Liste. Die Liste enthält für jede Nachricht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="feba4-p102">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list. The list includes the following for each message:</span></span>
  
- <span data-ttu-id="feba4-109">**Absender** Der Send Name und e-Mail-Adresse der in Quarantäne verschobenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="feba4-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="feba4-110">**Betreff** Der Betreffzeilentext der in Quarantäne verschobenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="feba4-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="feba4-111">**Datum** Datum und Uhrzeit (UTC-Angabe) der Verschiebung der Nachricht in Quarantäne.</span><span class="sxs-lookup"><span data-stu-id="feba4-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="feba4-112">**Größe** Die Größe der Nachricht, in Kilobyte (KB).</span><span class="sxs-lookup"><span data-stu-id="feba4-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="feba4-113">Zurzeit stehen zwei Aktionen, die Sie, mit einer Nachricht in Quarantäne ergreifen können:</span><span class="sxs-lookup"><span data-stu-id="feba4-113">Currently, there are two actions you can take with a quarantined message:</span></span>
  
- <span data-ttu-id="feba4-114">**Freigabe für Posteingang** Wählen Sie diese Option zum Senden der Nachricht an Ihren Posteingang, in dem Sie es anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="feba4-114">**Release to Inbox** Choose this to send the message to your inbox, where you can view it.</span></span> 
    
- <span data-ttu-id="feba4-p103">**Als Junk melden** Wählen Sie diese Option, um eine Kopie der Nachricht an Microsoft zur Analyse senden. Das Team Spam ausgewertet wird und analysiert die Nachricht und, abhängig von den Ergebnissen der Analyse, passt die Anti-Spam-Filterregeln, um die Nachricht über ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="feba4-p103">**Report as Not Junk** Choose this to send a copy of the message to Microsoft for analysis. The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span> 
    
<span data-ttu-id="feba4-117">Beachten Sie sollten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="feba4-117">Be aware of the following:</span></span>
  
- <span data-ttu-id="feba4-p104">Nachrichten, die isoliert werden, da sie eine e-Mail-Flussregel übereinstimmen sind nicht in Nachrichten unter Quarantäne gestellte e-Mails Benutzers enthalten. Es werden nur Nachrichten in Spam-Quarantäne aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="feba4-p104">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages. Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="feba4-120">Sie können eine Nachricht nur einmal freigeben und als falsch positiv markiert (keine Junk-E-Mail) melden.</span><span class="sxs-lookup"><span data-stu-id="feba4-120">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

