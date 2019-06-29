---
title: Suchen und untersuchen schädlicher e-Mails, die zugestellt wurden (Office 365 Untersuchung und Reaktion auf Bedrohungen
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/19/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 8f54cd33-4af7-4d1b-b800-68f8818e5b2a
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Sie mithilfe von Bedrohungs Ermittlungs-und-Antwortfunktionen böswillige e-Mails suchen und untersuchen.
ms.openlocfilehash: 5f8c615bed07b75cd3c06ec48f5ba73586f0f6d5
ms.sourcegitcommit: 011bfa60cafdf47900aadf96a17eb275efa877c4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/29/2019
ms.locfileid: "35394290"
---
# <a name="find-and-investigate-malicious-email-that-was-delivered-office-365-advanced-threat-protection-plan-2"></a><span data-ttu-id="2b014-103">Suchen und untersuchen schädlicher e-Mails, die zugestellt wurden (Office 365 Advanced Threat Protection-Plan 2)</span><span class="sxs-lookup"><span data-stu-id="2b014-103">Find and investigate malicious email that was delivered (Office 365 Advanced Threat Protection Plan 2)</span></span>

<span data-ttu-id="2b014-104">[Office 365 Advanced Threat Protection](office-365-atp.md) können Sie Aktivitäten untersuchen, die Ihre Benutzer gefährden und Maßnahmen zum Schutz Ihrer Organisation ergreifen.</span><span class="sxs-lookup"><span data-stu-id="2b014-104">[Office 365 Advanced Threat Protection](office-365-atp.md) lets you to investigate activities that put your users at risk and take action to protect your organization.</span></span> <span data-ttu-id="2b014-105">Wenn Sie beispielsweise Teil des Sicherheitsteams Ihrer Organisation sind, können Sie nach verdächtigen e-Mail-Nachrichten suchen und diese untersuchen, die Ihren Benutzern zugestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="2b014-105">For example, if you are part of your organization's security team, you can find and investigate suspicious email messages that were delivered to your users.</span></span> <span data-ttu-id="2b014-106">Sie können dies mithilfe von [Threat Explorer (oder Echtzeiterkennung)](threat-explorer.md)durchführen.</span><span class="sxs-lookup"><span data-stu-id="2b014-106">You can do this by using [Threat Explorer (or real-time detections)](threat-explorer.md).</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="2b014-107">Bevor Sie beginnen...</span><span class="sxs-lookup"><span data-stu-id="2b014-107">Before you begin...</span></span>

<span data-ttu-id="2b014-108">Stellen Sie sicher, dass folgende Anforderungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="2b014-108">Make sure that the following requirements are met:</span></span>
  
- <span data-ttu-id="2b014-109">Ihre Organisation verfügt über [Office 365 Advanced Threat Protection](office-365-atp.md) (Plan 1 oder Plan 2) und [Lizenzen werden Benutzern zugewiesen](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).</span><span class="sxs-lookup"><span data-stu-id="2b014-109">Your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (Plan 1 or Plan 2) and [licenses are assigned to users](https://docs.microsoft.com/en-us/office365/admin/subscriptions-and-billing/assign-licenses-to-users).</span></span>
    
- <span data-ttu-id="2b014-110">[Office 365 Überwachungsprotokollierung](turn-audit-log-search-on-or-off.md) ist für Ihre Organisation aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2b014-110">[Office 365 audit logging](turn-audit-log-search-on-or-off.md) is turned on for your organization.</span></span> 
    
- <span data-ttu-id="2b014-111">Ihre Organisation verfügt über Richtlinien, die für Antispam-, Antischadsoftware-und Anti-Phishing-Maßnahmen und so weiter definiert sind.</span><span class="sxs-lookup"><span data-stu-id="2b014-111">Your organization has policies defined for anti-spam, anti-malware, anti-phishing, and so on.</span></span> <span data-ttu-id="2b014-112">Weitere Informationen finden Sie unter [Protect Against Threats in Office 365](protect-against-threats.md).</span><span class="sxs-lookup"><span data-stu-id="2b014-112">See [Protect against threats in Office 365](protect-against-threats.md).</span></span>
    
- <span data-ttu-id="2b014-113">Sie sind ein Office 365 globaler Administrator oder haben dem Security &amp; Compliance Center entweder den Sicherheitsadministrator oder die Such-und Säuberungs Rolle zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2b014-113">You are an Office 365 global administrator, or you have either the Security Administrator or the Search and Purge role assigned in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="2b014-114">Siehe [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="2b014-114">See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
    
## <a name="dealing-with-suspicious-emails"></a><span data-ttu-id="2b014-115">Umgang mit verdächtigen e-Mails</span><span class="sxs-lookup"><span data-stu-id="2b014-115">Dealing with suspicious emails</span></span>

<span data-ttu-id="2b014-116">Böswillige Angreifer senden möglicherweise e-Mails an Ihre Benutzer, um zu versuchen, Ihre Anmeldeinformationen zu Phishing und Zugriff auf Ihre Unternehmensgeheimnisse zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2b014-116">Malicious attackers may be sending mail to your users to try and phish their credentials and gain access to your corporate secrets!</span></span> <span data-ttu-id="2b014-117">Um dies zu verhindern, sollten Sie die Threat Protection-Dienste in Office 365 verwenden, einschließlich [Exchange Online Protection](eop/exchange-online-protection-overview.md) und [Advanced Threat Protection](office-365-atp.md).</span><span class="sxs-lookup"><span data-stu-id="2b014-117">To prevent this, you should use the threat protection services in Office 365, including [Exchange Online Protection](eop/exchange-online-protection-overview.md) and [Advanced Threat Protection](office-365-atp.md).</span></span> <span data-ttu-id="2b014-118">Es gibt jedoch Situationen, in denen ein Angreifer e-Mails an Benutzer senden kann, die eine URL enthalten, und diese URL erst später auf böswilligen Inhalt (Schadsoftware usw.) verweist.</span><span class="sxs-lookup"><span data-stu-id="2b014-118">However, there are times when an attacker could send mail to your users containing a URL and only later on make that URL point to malicious content (malware, etc.).</span></span> <span data-ttu-id="2b014-119">Alternativ erkennen Sie möglicherweise zu spät, dass ein Benutzer in Ihrer Organisation kompromittiert wurde, und während dieser Benutzer kompromittiert wurde, hat ein Angreifer dieses Konto verwendet, um e-Mails an andere Benutzer in Ihrem Unternehmen zu senden.</span><span class="sxs-lookup"><span data-stu-id="2b014-119">Alternately, you may realize too late that a user in your organization has been compromised, and while that user was compromised, an attacker used that account to send email to other users in your company.</span></span> <span data-ttu-id="2b014-120">Im Rahmen der Bereinigung beider Szenarien möchten Sie möglicherweise e-Mail-Nachrichten von Benutzer Posteingängen entfernen.</span><span class="sxs-lookup"><span data-stu-id="2b014-120">As part of cleaning up both of these scenarios, you may want to remove email messages from user inboxes.</span></span> <span data-ttu-id="2b014-121">In solchen Situationen können Sie [Threat Explorer (oder Echtzeiterkennung)](threat-explorer.md) nutzen, um diese e-Mail-Nachrichten zu suchen und zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2b014-121">In situations like these, you can leverage [Threat Explorer (or real-time detections)](threat-explorer.md) to find and remove those email messages!</span></span>

## <a name="where-re-routed-emails-are-located-after-actions-are-taken"></a><span data-ttu-id="2b014-122">Wo nach dem Ausführen von Aktionen erneut weitergeleitete e-Mails abgelegt werden</span><span class="sxs-lookup"><span data-stu-id="2b014-122">Where re-routed emails are located after actions are taken</span></span>

<span data-ttu-id="2b014-123">Threat Explorer bei der Echtzeiterkennung wurden die Felder Zustellungs Aktion und Zustellungs Speicherort an der Stelle des Zustellungs Status hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="2b014-123">Threat Explorer real-time detections has added the Delivery Action and Delivery Location fields in the place of Delivery Status.</span></span> <span data-ttu-id="2b014-124">Dadurch wird ein vollständigeres Bild davon erzielt, wo Ihre e-Mails landen.</span><span class="sxs-lookup"><span data-stu-id="2b014-124">This results in a more complete picture of where your emails land.</span></span> <span data-ttu-id="2b014-125">Ein Teil des Ziels dieser Änderung besteht darin, die Suche für Sicherheitsleute einfacher zu machen, aber das Ergebnis ist, dass der Speicherort der Problem-e-Mails auf einen Blick zu erkennen ist.</span><span class="sxs-lookup"><span data-stu-id="2b014-125">Part of the goal of this change is to make hunting easier for Security Ops people, but the net result is knowing the location of problem emails at a glance.</span></span>

<span data-ttu-id="2b014-126">Der Zustellungs Status wird nun in zwei Spalten aufgeteilt:</span><span class="sxs-lookup"><span data-stu-id="2b014-126">Delivery Status is now broken out into two columns:</span></span>

- <span data-ttu-id="2b014-127">**Zustellungs Aktion** – wie lautet der Status dieser e-Mail?</span><span class="sxs-lookup"><span data-stu-id="2b014-127">**Delivery Action** - What is the status of this email?</span></span>
- <span data-ttu-id="2b014-128">**Zustellungs Speicherort** – wohin wurde diese e-Mail weitergeleitet?</span><span class="sxs-lookup"><span data-stu-id="2b014-128">**Delivery Location** - Where was this email routed as a result?</span></span>

<span data-ttu-id="2b014-129">Zustellungs Aktion ist die Aktion, die aufgrund vorhandener Richtlinien oder Erkennungen auf eine e-Mail angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2b014-129">Delivery Action is the action taken on an email due to existing policies or detections.</span></span> <span data-ttu-id="2b014-130">Hier sind die möglichen Aktionen, die eine e-Mail ausführen kann:</span><span class="sxs-lookup"><span data-stu-id="2b014-130">Here are the possible actions an email can take:</span></span>

1. <span data-ttu-id="2b014-131">**Zugestellt** – e-Mails wurden im Posteingang oder Ordner eines Benutzers zugestellt, und der Benutzer kann direkt darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2b014-131">**Delivered** – email was delivered to inbox or folder of a user and the user can directly access it.</span></span>
2. <span data-ttu-id="2b014-132">**Junked** – e-Mails wurden entweder an den Junk-Ordner des Benutzers oder den Ordner "gelöscht" gesendet, und der Benutzer hat Zugriff auf e-Mails in seinem Junk-oder Deleted-Ordner.</span><span class="sxs-lookup"><span data-stu-id="2b014-132">**Junked** – email was sent to either user’s junk folder or deleted folder, and the user has access to emails in their Junk or Deleted folder.</span></span>
3. <span data-ttu-id="2b014-133">**Blockiert** – alle e-Mails, die unter Quarantäne gestellt werden, die fehlgeschlagen sind oder gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="2b014-133">**Blocked** – any emails that's quarantined, that  failed, or was dropped.</span></span> <span data-ttu-id="2b014-134">Auf diesen Zugriff kann der Benutzer vollständig zugreifen!</span><span class="sxs-lookup"><span data-stu-id="2b014-134">This is completely inaccessible by the user!</span></span>
4. <span data-ttu-id="2b014-135">**Ersetzt** – jede e-Mail-Nachricht, bei der böswillige Anlagen durch txt-Dateien ersetzt werden, in denen der Anhang als böswillig bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="2b014-135">**Replaced** – any email where malicious attachments are replaced by .txt files that state the attachment was malicious.</span></span>
 
<span data-ttu-id="2b014-136">Der Übermittlungsort zeigt die Ergebnisse von Richtlinien und Erkennungen an, die nach der Zustellung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2b014-136">Delivery location shows the results of policies and detections that run post-delivery.</span></span> <span data-ttu-id="2b014-137">Sie ist mit einer Zustellungs Aktion verknüpft.</span><span class="sxs-lookup"><span data-stu-id="2b014-137">It's linked to a Delivery Action.</span></span> <span data-ttu-id="2b014-138">Dieses Feld wurde hinzugefügt, um Einblicke in die Aktion zu geben, die ausgeführt wird, wenn ein Problem mit e-Mails gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="2b014-138">This field was added to give insight into the action taken when a problem mail is found.</span></span> <span data-ttu-id="2b014-139">Im folgenden sind die möglichen Werte für den Zustellungs Speicherort zu finden:</span><span class="sxs-lookup"><span data-stu-id="2b014-139">Here are the possible values of delivery location:</span></span>

1. <span data-ttu-id="2b014-140">**Posteingang oder Ordner** – die e-Mail befindet sich im Posteingang oder in einem Ordner (entsprechend Ihren e-Mail-Regeln).</span><span class="sxs-lookup"><span data-stu-id="2b014-140">**Inbox or folder** – The email is in inbox or a folder (according to your email rules).</span></span>
2. <span data-ttu-id="2b014-141">**On-Prem oder External** – das Postfach ist nicht in der Cloud vorhanden, sondern lokal.</span><span class="sxs-lookup"><span data-stu-id="2b014-141">**On-prem or external** – The mailbox doesn’t exist on cloud but is on -premises.</span></span>
3. <span data-ttu-id="2b014-142">**Junk-Ordner** – die e-Mail im Ordner Junk eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="2b014-142">**Junk folder** – The email in in the Junk folder of a user.</span></span>
4. <span data-ttu-id="2b014-143">**Ordner "Gelöschte Elemente"** – die e-Mail im Ordner "Gelöschte Elemente" eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="2b014-143">**Deleted items folder** – The email in the Deleted items folder of a user.</span></span>
5. <span data-ttu-id="2b014-144">**Quarantine** – die e-Mail-Nachricht in Quarantäne und befindet sich nicht im Postfach eines Benutzers.</span><span class="sxs-lookup"><span data-stu-id="2b014-144">**Quarantine** – The email in quarantine, and is not in a user’s mailbox.</span></span>
6. <span data-ttu-id="2b014-145">**Fehler** – die e-Mail konnte das Postfach nicht erreichen.</span><span class="sxs-lookup"><span data-stu-id="2b014-145">**Failed** – The email failed to reach the mailbox.</span></span>
7. <span data-ttu-id="2b014-146">**Fallen gelassen** – die e-Mail wird irgendwo in der Nachrichtenübermittlung verloren.</span><span class="sxs-lookup"><span data-stu-id="2b014-146">**Dropped** – The email gets lost somewhere in the Mailflow.</span></span>
  
## <a name="find-and-delete-suspicious-email-that-was-delivered"></a><span data-ttu-id="2b014-147">Suchen und löschen verdächtiger e-Mails, die zugestellt wurden</span><span class="sxs-lookup"><span data-stu-id="2b014-147">Find and delete suspicious email that was delivered</span></span>

> [!TIP]
> <span data-ttu-id="2b014-148">Threat Explorer (manchmal auch als Explorer bezeichnet) ist ein leistungsfähiger Bericht, der mehrere Zwecke wie das Suchen und Löschen von Nachrichten, das Identifizieren der IP-Adresse eines böswilligen e-Mail-Absenders oder das Starten eines Vorfalls zur weiteren Untersuchung dienen kann.</span><span class="sxs-lookup"><span data-stu-id="2b014-148">Threat Explorer (sometimes called Explorer), is a powerful report that can serve multiple purposes, such as finding and deleting messages, identifying the IP address of a malicious email sender, or starting an incident for further investigation.</span></span> <span data-ttu-id="2b014-149">Das folgende Verfahren konzentriert sich auf die Verwendung von Explorer zum Suchen und Löschen von böswilligen e-Mails aus Empfängerpostfächern.</span><span class="sxs-lookup"><span data-stu-id="2b014-149">The following procedure focuses on using Explorer to find and delete malicious email from recipients mailboxes.</span></span>

<span data-ttu-id="2b014-150">So zeigen Sie die Änderungen am früheren Feld "Zustellungs Status" an (jetzt Zustellungs Aktion und Zustellungs Speicherort):</span><span class="sxs-lookup"><span data-stu-id="2b014-150">To see the changes to the former Delivery Status field (now Delivery Action and Delivery Location):</span></span> 

1. <span data-ttu-id="2b014-151">Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an.</span><span class="sxs-lookup"><span data-stu-id="2b014-151">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365.</span></span> <span data-ttu-id="2b014-152">Dadurch gelangen Sie zum Security &amp; Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="2b014-152">This takes you to the Security &amp; Compliance Center.</span></span> 
    
2. <span data-ttu-id="2b014-153">Klicken Sie im linken Navigationsbereich auf **Threat Management** \> **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="2b014-153">In the left navigation, choose **Threat management** \> **Explorer**.</span></span>

![Screenshot des Bedrohungs-Explorers.](media/Threat Explorer Delivery Action and Delivery Location.PNG)

<!--Comment>
    
3. In the View menu, choose **All email**.<br/>![Use the View menu to choose between Email and Content reports](media/d39013ff-93b6-42f6-bee5-628895c251c2.png)
  
4. Notice the labels that appear in the report, such as **Delivered**, **Unknown**, or **Delivered to junk**.<br/>![Threat Explorer showing data for all email](media/208826ed-a85e-446f-b276-b5fdc312fbcb.png)<br/>(Depending on the actions that were taken on email messages for your organization, you might see additional labels, such as **Blocked** or **Replaced**.)
    
5. In the report, choose **Delivered** to view only emails that ended up in users' inboxes.<br/>![Clicking "Delivered to junk" removes that data from view](media/e6fb2e47-461e-4f6f-8c65-c331bd858758.png)
  
6. Below the chart, review the **Email** list below the chart.<br/>![Below the chart, view a list of email messages that were detected](media/dfb60590-1236-499d-97da-86c68621e2bc.png)
  
7. In the list, choose an item to view more details about that email message. For example, you can click the subject line to view information about the sender, recipients, attachments, and other similar email messages.<br/>![You can view additional information about an item, including details and any attachments](media/5a5707c3-d62a-4610-ae7b-900fff8708b2.png)
  
8. After viewing information about email messages, select one or more items in the list to activate **+ Actions**.
    
9. Use the **+ Actions** list to apply an action, such as **Move to deleted** items. This will delete the selected messages from the recipients' mailboxes.<br/>![When you select one or more email messages, you can choose from several available actions](media/ef12e10c-60a7-4f66-8f76-68d77ae26de1.png)
  
-->
## <a name="related-topics"></a><span data-ttu-id="2b014-155">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="2b014-155">Related topics</span></span>

[<span data-ttu-id="2b014-156">Office 365 Advanced Threat Protection-Plan 2</span><span class="sxs-lookup"><span data-stu-id="2b014-156">Office 365 Advanced Threat Protection Plan 2</span></span>](office-365-ti.md)
  
[<span data-ttu-id="2b014-157">Schutz vor Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="2b014-157">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="2b014-158">Anzeigen von Berichten für Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="2b014-158">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)
  

