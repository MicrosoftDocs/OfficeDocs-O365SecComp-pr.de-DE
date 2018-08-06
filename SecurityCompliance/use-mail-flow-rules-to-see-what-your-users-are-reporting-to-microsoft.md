---
title: Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 8/23/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Sie können eine Exchange-Transportregel zum verhindern, dass Ihre Benutzer am Senden von e-Mail-Nachrichten an Microsoft zur Analyse und deren Verwendung in Ihrer eigenen Sicherheitsprozesse erstellen
ms.openlocfilehash: f2376668e2a1a16eba9913178a100fc31763b227
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026772"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="04e36-103">Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden</span><span class="sxs-lookup"><span data-stu-id="04e36-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="04e36-p101">Es gibt mehrere Methoden, die Sie false positive und false negative Nachrichten an Microsoft zur Analyse senden können. E-Mail-Flussregeln können Sie als Administrator finden Sie unter was Ihre Benutzer an Microsoft als Spam, nicht-Spam und Phishing-Angriffen reporting. Weitere Informationen finden Sie unter [Submit Spam, nicht-Spam und Phishing-Betrug Nachrichten an Microsoft zur Analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Im Gegensatz dazu können Sie eine Exchange-Transportregel zum verhindern, dass Ihre Benutzer am Senden von e-Mail-Nachrichten an Microsoft zur Analyse und deren Verwendung in Ihrer eigenen Sicherheitsprozesse erstellen.</span><span class="sxs-lookup"><span data-stu-id="04e36-p101">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis. As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Conversely, you can create an Exchange Transport rule to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="04e36-108">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="04e36-108">What do you need to know before you begin?</span></span>
<span data-ttu-id="04e36-109"><a name="sectionSection0"> </a></span><span class="sxs-lookup"><span data-stu-id="04e36-109"></span></span>

<span data-ttu-id="04e36-110">Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="04e36-110">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="04e36-p102">Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unterEintrag „Transportregeln" im Thema [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) und Eintrag „Outlook Web App-Postfachrichtlinien" im Thema [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx).</span><span class="sxs-lookup"><span data-stu-id="04e36-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic and the "Outlook Web App mailbox policies" entry in the [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) topic.</span></span> 
  
<span data-ttu-id="04e36-113">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="04e36-113">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="04e36-114">Verwenden Sie die Exchange-Verwaltungskonsole, um eine Nachrichtenflussregel zu erstellen, um Berichte zu Junk-E-Mails, Phishing und Nicht-Junk-E-Mails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="04e36-114">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>
<span data-ttu-id="04e36-115"><a name="sectionSection1"> </a></span><span class="sxs-lookup"><span data-stu-id="04e36-115"></span></span>

1. <span data-ttu-id="04e36-116">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="04e36-116">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="04e36-117">Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png) und wählen Sie dann **Neue Regel erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="04e36-117">Click ![Add Icon](media/ITPro-EAC-AddIcon.png) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="04e36-118">Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.</span><span class="sxs-lookup"><span data-stu-id="04e36-118">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="04e36-119">Unter **Diese Regel anwenden, wenn...** können Sie **Empfänger** und anschließend **Adresse enthält eines dieser Wörter** wählen.</span><span class="sxs-lookup"><span data-stu-id="04e36-119">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>
    
5. <span data-ttu-id="04e36-120">Im Feld **Wörter oder Ausdrücke angeben** müssen Sie folgende Änderungen vornehmen:</span><span class="sxs-lookup"><span data-stu-id="04e36-120">In the **specify words or phrases** box, do the following:</span></span> 
    - <span data-ttu-id="04e36-p103">Geben Sie **abuse@messaging.microsoft.com** ein, und klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Geben Sie anschließend **junk@office365.microsoft.com** ein, und klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Diese E-Mail-Adressen werden verwendet, um falsch negative Nachrichten an Microsoft zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="04e36-p103">Type **abuse@messaging.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png), and then type **junk@office365.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). These email addresses are used to submit false negative messages to Microsoft.</span></span>
    - <span data-ttu-id="04e36-p104">Geben Sie **phish@office365.microsoft.com** ein, und klicken Sie dann auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Diese E-Mail-Adresse wird verwendet, um verpasste Phishingnachrichten an Microsoft zu senden.</span><span class="sxs-lookup"><span data-stu-id="04e36-p104">Type **phish@office365.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). This email address is used to submit missed phishing messages to Microsoft.</span></span>
    - <span data-ttu-id="04e36-p105">Geben Sie **false_positive@messaging.microsoft.com** ein, und klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Geben Sie anschließend **not_junk@office365.microsoft.com** ein, und klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png). Diese E-Mail-Adressen werden verwendet, um falsch positive Nachrichten an Microsoft zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="04e36-p105">Type **false_positive@messaging.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png), and then type **not_junk@office365.microsoft.com** and then click ![Add Icon](media/ITPro-EAC-AddIcon.png). These email addresses are used to submit false positive messages to Microsoft.</span></span>
    - <span data-ttu-id="04e36-127">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="04e36-127">Click **ok**.</span></span>
    
6. <span data-ttu-id="04e36-128">Wählen Sie unter **Folgendes ausführen** die Option **Bcc der Nachricht an...** aus, und wählen Sie dann die Postfächer aus, in denen Sie Nachrichten erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="04e36-128">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span> 
    
7. <span data-ttu-id="04e36-p106">Auf Wunsch können Sie unter anderem auch Einstellungen zur Überwachung der Regel, zum Testen der Regel und zum Aktivieren der Regel in einem bestimmten Zeitraum vornehmen. Wir empfehlen, die Regel über eine bestimmte Zeit zu testen, bevor Sie sie erzwingen. Weitere Informationen zu diesen Optionen finden Sie unter [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx).</span><span class="sxs-lookup"><span data-stu-id="04e36-p106">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. [Manage Transport Rules](http://technet.microsoft.com/library/e7a81372-b6d7-4d1f-bc9e-a845a7facac2.aspx) contains more information about these selections.</span></span> 
    
8. <span data-ttu-id="04e36-p107">Klicken Sie auf die Schaltfläche **Speichern**, um die Regel zu speichern. Sie wird in der Liste der Regeln angezeigt.</span><span class="sxs-lookup"><span data-stu-id="04e36-p107">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="04e36-134">Nachdem Sie die Regel erstellt und durchgesetzt haben, werden sämtliche von Ihrer Organisation aus an vorgegebene E-Mail-Adressen gesendeten Nachrichten in das angegebene Postfach kopiert.</span><span class="sxs-lookup"><span data-stu-id="04e36-134">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
  

