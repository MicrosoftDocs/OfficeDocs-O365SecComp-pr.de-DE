---
title: Häufig gestellte Fragen (FAQ) zur Quarantäne
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 6/16/2017
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: c440b2ac-cafa-4be5-ba4c-14278a7990ae
ms.collection:
- M365-security-compliance
description: Unter diesem Thema werden häufig gestellte Fragen und Antworten zur gehosteten Quarantäne bereitgestellt.
ms.openlocfilehash: 381eb0aba25d7149c2f164f9e0173034568d5eff
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276025"
---
# <a name="quarantine-faq"></a><span data-ttu-id="be5bd-103">Häufig gestellte Fragen (FAQ) zur Quarantäne</span><span class="sxs-lookup"><span data-stu-id="be5bd-103">Quarantine FAQ</span></span>

<span data-ttu-id="be5bd-p101">Unter diesem Thema werden häufig gestellte Fragen und Antworten zur gehosteten Quarantäne bereitgestellt. Die Antworten richten sich an Kunden von Microsoft Exchange Online und Exchange Online Protection.</span><span class="sxs-lookup"><span data-stu-id="be5bd-p101">This topic provides frequently asked questions and answers about the hosted quarantine. Answers are applicable for Microsoft Exchange Online and Exchange Online Protection customers.</span></span>
  
 <span data-ttu-id="be5bd-106">**F: Wie kann ich Nachrichten mit Schadsoftware in Quarantäne verwalten?**</span><span class="sxs-lookup"><span data-stu-id="be5bd-106">**Q. How do I manage malware-quarantined messages in quarantine?**</span></span>
  
<span data-ttu-id="be5bd-p102">Sie müssen das Security &amp; Compliance Center verwenden, um Nachrichten anzuzeigen und zu arbeiten, die in Quarantäne gesendet wurden, da Sie Schadsoftware enthalten. Weitere Informationen finden Sie unter [Isolieren von e-Mail-Nachrichten in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span><span class="sxs-lookup"><span data-stu-id="be5bd-p102">You need to use the Security &amp; Compliance Center in order to view and work with messages that were sent to quarantine because they contain malware. For more information, see [Quarantine email messages in Office 365](https://support.office.com/article/Quarantine-email-messages-in-Office-365-4c234874-015e-4768-8495-98fcccfc639b).</span></span>
  
 <span data-ttu-id="be5bd-109">**F. Wie wird der Dienst konfiguriert, damit Spamnachrichten in Quarantäne gesendet werden?**</span><span class="sxs-lookup"><span data-stu-id="be5bd-109">**Q. How do I configure the service to send spam-quarantined messages to the quarantine?**</span></span>
  
<span data-ttu-id="be5bd-p103">A. Standardmäßig werden durch die Inhaltsfilterung abgefangene Nachrichten an den Junk-E-Mail-Ordner des Empfängers gesendet. Als Administrator können Sie Richtlinien für die Inhaltsfilterung jedoch auch so konfigurieren, dass Spamnachrichten stattdessen in Quarantäne verschoben werden. Weitere Informationen zu den verschiedenen Aktionen, die bei inhaltsgefilterten Nachrichten durchgeführt werden können, finden Sie unter [Konfigurieren von Spamfilterrichtlinien](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="be5bd-p103">A. By default, content-filtered messages are sent to the recipients Junk Email folder. However, admins can configure content filter policies to send spam-quarantined messages to the quarantine instead. For more information about the different actions that can be performed on content-filtered messages, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="be5bd-114">**F. Bietet der Dienst Administrator- und Endbenutzerverwaltung von Nachrichten in der Spamquarantäne?**</span><span class="sxs-lookup"><span data-stu-id="be5bd-114">**Q. Does the service have administrator and end user management of spam-quarantined messages?**</span></span>
  
<span data-ttu-id="be5bd-p104">A. Administratoren können in der Exchange-Verwaltungskonsole nach E-Mails suchen, die sich in Quarantäne befinden, und Details zu diesen Nachrichten anzeigen. Nach dem Auffinden der Nachricht können Sie sie für bestimmte Benutzer freigeben und dem Microsoft-Spamanalyseteam optional als falsch positiv (kein Junk) melden. Weitere Informationen finden Sie unter [Finden und Freigeben von Nachrichten in Quarantäne als Administrator](find-and-release-quarantined-messages-as-an-administrator.md).</span><span class="sxs-lookup"><span data-stu-id="be5bd-p104">A. As an administrator, you can search for and view details about all quarantined email messages in the Exchange admin center (EAC). After locating the message, you can release it to specific users and optionally report it as a false positive (not junk) to the Microsoft Spam Analysis Team. For more information, see [Find and release quarantined messages as an administrator](find-and-release-quarantined-messages-as-an-administrator.md).</span></span>
  
<span data-ttu-id="be5bd-119">Als Endbenutzer können Sie Ihre eigenen Nachrichten in der Spamquarantäne verwalten über:</span><span class="sxs-lookup"><span data-stu-id="be5bd-119">As an end user, you can manage your own spam-quarantined messages via:</span></span> 
  
- <span data-ttu-id="be5bd-p105">Der Spam-Quarantäne-Benutzeroberfläche. Weitere Informationen finden Sie unter [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).</span><span class="sxs-lookup"><span data-stu-id="be5bd-p105">The spam quarantine user interface. For more information, see [Find and Release Quarantined Messages (End Users)](http://technet.microsoft.com/library/e439b560-827a-4807-abd3-6b861c1ff786.aspx).</span></span>
        
 <span data-ttu-id="be5bd-122">**Wie gewähre ich meinen Endbenutzern Zugriff auf die Spamquarantäne?**</span><span class="sxs-lookup"><span data-stu-id="be5bd-122">**Q. How do I grant access to the spam quarantine for my end users?**</span></span>
  
<span data-ttu-id="be5bd-p106">A. für den Zugriff auf die Spamquarantäne für Endbenutzer müssen Endbenutzer eine gültige Office 365-Benutzer-ID und ein Kennwort besitzen. EOP-Kunden, die lokale Postfächer schützen, müssen gültige e-Mail-Benutzer sein, die über die Verzeichnissynchronisierung oder die EAC erstellt werden. Weitere Informationen zum Verwalten von Benutzern finden Sie unter EOP-Administratoren unter [Verwalten von e-Mail-Benutzern in EoP](eop/manage-mail-users-in-eop.md). Für eigenständige EOP-Kunden empfehlen wir die Verwendung der Verzeichnissynchronisierung und die Aktivierung der verzeichnisbasierten Edge-Blockierung; Weitere Informationen finden Sie unter [Use Directory based Edge Blocking to Reject Messages Sent to invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span><span class="sxs-lookup"><span data-stu-id="be5bd-p106">A. In order to access the end user spam quarantine, end users must have a valid Office 365 user ID and password. EOP customers protecting on-premises mailboxes must be valid email users created via directory synchronization or the EAC. For more information about managing users, EOP admins can refer to [Manage mail users in EOP](eop/manage-mail-users-in-eop.md). For EOP standalone customers, we recommend using directory synchronization and enabling Directory Based Edge Blocking; for more information, see [Use Directory Based Edge Blocking to Reject Messages Sent to Invalid Recipients](http://technet.microsoft.com/library/ca7b7416-92ed-40ad-abdb-695be46ea2e4.aspx).</span></span>
  
 <span data-ttu-id="be5bd-128">**Q. Können auch andere Nachrichten als Spam in Quarantäne gesendet werden?**</span><span class="sxs-lookup"><span data-stu-id="be5bd-128">**Q. Can anything other than spam be sent to the quarantine?**</span></span>
  
<span data-ttu-id="be5bd-p107">A. Nachrichten, die der Transportregel entsprechen, können ebenfalls in Administrator-Quarantäne gesendet werden, wenn die Aktion entsprechend konfiguriert ist. Die Endbenutzer-Quarantäne ist nur für Spam vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="be5bd-p107">A. Messages that match a transport rule can also be sent to the administrator quarantine, if that's the configured action. The end user quarantine is for spam only.</span></span>
  
 <span data-ttu-id="be5bd-132">**F. Wie lange bleiben Nachrichten in der Quarantäne?**</span><span class="sxs-lookup"><span data-stu-id="be5bd-132">**Q. For how long are messages kept in the quarantine?**</span></span>
  
<span data-ttu-id="be5bd-p108">A. Standardmäßig werden Nachrichten in Spamquarantäne in der Quarantäne für 30 Tage aufbewahrt, während isolierte Nachrichten, die einer Transportregel entsprechen, 7 Tage lang in der Quarantäne aufbewahrt werden. Nach diesem Zeitraum werden die Nachrichten gelöscht und können nicht abgerufen werden. Der Aufbewahrungszeitraum für isolierte Nachrichten, die einer Transportregel entsprechen, ist nicht konfigurierbar. Die Aufbewahrungsdauer für Nachrichten in Spam-Quarantäne kann jedoch über die Einstellung **Spam für (Tage)** in ihren Inhaltsfilter Richtlinien gesenkt werden. Weitere Informationen finden Sie unter [configure your Spamfilter Policies](configure-your-spam-filter-policies.md).</span><span class="sxs-lookup"><span data-stu-id="be5bd-p108">A. By default, spam-quarantined messages are kept in the quarantine for 30 days, while quarantined messages that matched a transport rule are kept in the quarantine for 7 days. After this period of time the messages are deleted and are not retrievable. The retention period for quarantined messages that matched a transport rule is not configurable. However, the retention period for spam-quarantined messages can be lowered via the **Retain spam for (days)** setting in your content filter policies. For more information, see [Configure your spam filter policies](configure-your-spam-filter-policies.md).</span></span>
  
 <span data-ttu-id="be5bd-139">**F. Kann ich mehr als eine Quarantänenachricht gleichzeitig freigeben oder melden?**</span><span class="sxs-lookup"><span data-stu-id="be5bd-139">**Q. Can I release or report more than one quarantined message at a time?**</span></span>
  
<span data-ttu-id="be5bd-p109">A. Im EAC oder der Spamquarantäne für Endbenutzer können derzeit nicht mehrere Nachrichten gleichzeitig freigegeben oder gemeldet werden. Administratoren können dazu allerdings ein Windows Remote-PowerShell-Skript erstellen. Verwenden Sie das [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx)-Cmdlet, um nach Nachrichten zu suchen, und das [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx)-Cmdlet, um sie freizugeben.</span><span class="sxs-lookup"><span data-stu-id="be5bd-p109">A. The ability to release or report multiple messages at once is not currently available in the EAC or the end user spam quarantine. However, admins can create a remote Windows PowerShell script to accomplish this task. Use the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for messages, and the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet to release them.</span></span> 
  
 <span data-ttu-id="be5bd-144">**F. Werden bei der Suche nach in der Quarantäne isolierte Nachrichten Platzhalterzeichen unterstützt? Kann ich für eine bestimmte Domäne nach Nachricht in Quarantäne suchen?**</span><span class="sxs-lookup"><span data-stu-id="be5bd-144">**Q. Are wildcards supported when searching for quarantined messages? Can I search for quarantined messages for a specific domain?**</span></span>
  
<span data-ttu-id="be5bd-p110">A. Platzhalterzeichen werden bei der Angabe von Suchkriterien im Admin Center von Exchange nicht unterstützt. Wenn Sie beispielsweise nach einem Absender suchen, müssen Sie die vollständige E-Mail-Adresse angeben.</span><span class="sxs-lookup"><span data-stu-id="be5bd-p110">A. Wildcards are not supported when specifying search criteria in the Exchange admin center. For example, when searching for a sender, you must specify the full email address.</span></span>
  
<span data-ttu-id="be5bd-148">Administratoren können Windows Remote-PowerShell verwenden, um mit dem Cmdlet [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) nach Nachrichten in Quarantäne für eine bestimmte Domäne (z. B. "contoso.com") zu suchen:</span><span class="sxs-lookup"><span data-stu-id="be5bd-148">Using remote Windows PowerShell, admins can specify the [Get-QuarantineMessage](http://technet.microsoft.com/library/88026da1-8dbc-49e7-80e8-112a32773c34.aspx) cmdlet to search for quarantined messages for a specific domain (for example, contoso.com):</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```

<span data-ttu-id="be5bd-p111">Die Ergebnisse können an das Cmdlet [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) übergeben werden. Fügen Sie den Parameter "-ReleaseToAll" hinzu, um die Nachricht für alle Empfänger freizugeben. Nachdem eine Nachricht freigegeben wurde, kann nicht nicht nochmals freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="be5bd-p111">The results can be passed to the [Release-QuarantineMessage](http://technet.microsoft.com/library/4a3aa05c-238f-46f2-b8dd-b0e3c38eab3e.aspx) cmdlet. Include the -ReleaseToAll parameter to release the message to all recipients. Once a message is released, it can't be released again.</span></span> 
  
```
Get-QuarantineMessage | ? {$_.Senderaddress -like "*@contoso.com"}
```


