---
title: Verwenden von Spambenachrichtigungen für Benutzer zum Freigeben und Melden von isolierten Nachrichten in Office 365
ms.author: krowley
author: kccross
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
description: Wenn Ihr Administrator die Benachrichtigungen für Benutzer aktiviert, erhalten Sie eine Benachrichtigung, die an Ihr Postfach gesendete Nachrichten auflistet, die als Spam, Massen oder Phishing-Nachrichten identifiziert wurden. Sie können Nachrichten nach der Benachrichtigung freigeben oder melden.
ms.openlocfilehash: eb51d8f73ff00781b74cfba4e580668710ce7a76
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216395"
---
# <a name="use-user-spam-notifications-to-release-and-report-quarantined-messages-in-office-365"></a><span data-ttu-id="5cac8-104">Verwenden von Spambenachrichtigungen für Benutzer zum Freigeben und Melden von isolierten Nachrichten in Office 365</span><span class="sxs-lookup"><span data-stu-id="5cac8-104">Use user spam notifications to release and report quarantined messages in Office 365</span></span>

<span data-ttu-id="5cac8-105">Wenn Ihr Administrator Spambenachrichtigungen für Benutzer aktiviert, erhalten Sie eine Benachrichtigung, die an Ihr Postfach adressierte Nachrichten auflistet, die als Spam identifiziert und stattdessen isoliert wurden.</span><span class="sxs-lookup"><span data-stu-id="5cac8-105">If your admin enables spam notifications for users, you'll receive a notification message that lists messages addressed to your mailbox that were identified as spam and quarantined instead.</span></span>
  
> [!TIP]
> <span data-ttu-id="5cac8-106">Wenn Sie ein Administrator sind und dieses Feature aktivieren möchten, können Sie die Option auswählen, wenn Sie [eine standardmäßige Antispampolitik ändern](https://go.microsoft.com/fwlink/?LinkId=800313).</span><span class="sxs-lookup"><span data-stu-id="5cac8-106">If you're an administrator and want to enable this feature, you can choose the option when you [modify a default anti-spam policy](https://go.microsoft.com/fwlink/?LinkId=800313).</span></span> 
  
<span data-ttu-id="5cac8-p102">Die Nachricht, die Sie erhalten, enthält die Anzahl von Nachrichten in Spamquarantäne und das Datum und die Uhrzeit (in UTC) der letzten Nachricht in der Liste. Die Liste enthält für jede Nachricht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5cac8-p102">The message you receive includes the number of spam-quarantined messages you have, and the date and time (in Universal Coordinated Time or UTC) of the last message in the list. The list includes the following for each message:</span></span>
  
- <span data-ttu-id="5cac8-109">**Absender** Der Absender Name und die e-Mail-Adresse der isolierten Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5cac8-109">**Sender** The send name and email address of the quarantined message.</span></span> 
    
- <span data-ttu-id="5cac8-110">**Betreff** Der Betreffzeilentext der in Quarantäne verschobenen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5cac8-110">**Subject** The subject line text of the quarantined message.</span></span> 
    
- <span data-ttu-id="5cac8-111">**Datum** Datum und Uhrzeit (UTC-Angabe) der Verschiebung der Nachricht in Quarantäne.</span><span class="sxs-lookup"><span data-stu-id="5cac8-111">**Date** The date and time (in UTC) that the message was quarantined.</span></span> 
    
- <span data-ttu-id="5cac8-112">**Größe** Die Größe der Nachricht in Kilobyte (KBs).</span><span class="sxs-lookup"><span data-stu-id="5cac8-112">**Size** The size of the message, in kilobytes (KBs).</span></span> 
    
<span data-ttu-id="5cac8-113">Derzeit gibt es zwei Aktionen, die Sie mit einer isolierten Nachricht durchführen können:</span><span class="sxs-lookup"><span data-stu-id="5cac8-113">Currently, there are two actions you can take with a quarantined message:</span></span>
  
- <span data-ttu-id="5cac8-114">Im **Posteingang freigeben** Wählen Sie diese Option aus, um die Nachricht an Ihren Posteingang zu senden, wo Sie Sie anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="5cac8-114">**Release to Inbox** Choose this to send the message to your inbox, where you can view it.</span></span> 
    
- <span data-ttu-id="5cac8-p103">**Bericht als nicht-Junk** Wählen Sie diese Option aus, um eine Kopie der Nachricht zur Analyse an Microsoft zu senden. Das Spam-Team bewertet und analysiert die Nachricht, und je nach Ergebnis der Analyse werden die Anti-Spam-Filterregeln angepasst, um die Nachricht zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="5cac8-p103">**Report as Not Junk** Choose this to send a copy of the message to Microsoft for analysis. The spam team evaluates and analyzes the message, and, depending on the results of the analysis, adjusts the anti-spam filter rules to allow the message through.</span></span> 
    
<span data-ttu-id="5cac8-117">Beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5cac8-117">Be aware of the following:</span></span>
  
- <span data-ttu-id="5cac8-p104">Nachrichten, die unter Quarantäne gestellt werden, da Sie mit einer Nachrichtenfluss Regel übereinstimmen, sind nicht in Benutzer isolierten Nachrichten enthalten. Nur Nachrichten in Spamquarantäne werden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5cac8-p104">Messages that are quarantined because they matched a mail flow rule are not included in user quarantined messages. Only spam-quarantined messages are listed.</span></span>
    
- <span data-ttu-id="5cac8-120">Sie können eine Nachricht nur einmal freigeben und als falsch positiv markiert (keine Junk-E-Mail) melden.</span><span class="sxs-lookup"><span data-stu-id="5cac8-120">You can only release a message and report it as a false positive (not junk) once.</span></span>
    

