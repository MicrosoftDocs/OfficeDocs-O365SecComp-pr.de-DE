---
title: Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 8401f520-8e7c-467b-9e06-4a9fdb2ba548
description: Sie können eine Exchange-Transport Regel erstellen, um zu verhindern, dass Ihre Benutzer e-Mail-Nachrichten zur Analyse an Microsoft senden und in ihren eigenen Sicherheitsprozessen verwenden.
ms.openlocfilehash: 7ee8fb2bca1071ccd4080379485c1670a5e66a73
ms.sourcegitcommit: 06d6e63225f912d0f3c6bb836c61eb11c1dbe97a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/22/2019
ms.locfileid: "30206408"
---
# <a name="use-mail-flow-rules-to-see-what-your-users-are-reporting-to-microsoft"></a><span data-ttu-id="aeadb-103">Verwenden von Nachrichtenflussregeln, um anzuzeigen, was Ihre Benutzer an Microsoft melden</span><span class="sxs-lookup"><span data-stu-id="aeadb-103">Use mail flow rules to see what your users are reporting to Microsoft</span></span>

<span data-ttu-id="aeadb-p101">Es gibt mehrere Möglichkeiten, wie Sie falsch positive und falsch negative Nachrichten zur Analyse an Microsoft senden können. Als Administrator können Sie Nachrichtenfluss Regeln verwenden, um zu sehen, was Ihre Benutzer an Microsoft als Spam-, nicht-Spam-und Phishing-Scams melden. Weitere Informationen finden Sie unter [Submit Spam, Non-Spam, and Phishing Scam messages to Microsoft for Analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Umgekehrt können Sie eine Exchange-Transport Regel erstellen, um zu verhindern, dass Ihre Benutzer e-Mail-Nachrichten zur Analyse an Microsoft senden und in ihren eigenen Sicherheitsprozessen verwenden.</span><span class="sxs-lookup"><span data-stu-id="aeadb-p101">There are multiple ways you can send false positive and false negative messages to Microsoft for analysis. As an administrator, you can use mail flow rules to see what your users are reporting to Microsoft as spam, non-spam, and phishing scams. For more information, see [Submit spam, non-spam, and phishing scam messages to Microsoft for analysis](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md). Conversely, you can create an Exchange Transport rule to prevent your users from sending email messages to Microsoft for analysis and use them in your own security processes.</span></span>
  
## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="aeadb-108">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="aeadb-108">What do you need to know before you begin?</span></span>

<span data-ttu-id="aeadb-109">Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="aeadb-109">Estimated time to complete: 5 minutes</span></span>
  
<span data-ttu-id="aeadb-p102">Bevor Sie dieses Verfahren ausführen können, müssen Ihnen Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Transport Regeln" im Thema [Messaging Policy and Compliance Permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) and the "Outlook on the Web Mailbox Policies" im Thema [Clients and Mobile Devices Permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) .</span><span class="sxs-lookup"><span data-stu-id="aeadb-p102">You need to be assigned permissions before you can perform this procedure or procedures. To see what permissions you need, see the "Transport rules" entry in the [Messaging policy and compliance permissions](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx) topic and the "Outlook on the web mailbox policies" entry in the [Clients and mobile devices permissions](http://technet.microsoft.com/library/57eca42a-5a7f-4c65-89f0-7a84f2dbea19.aspx) topic.</span></span> 
  
<span data-ttu-id="aeadb-112">Informationen zu Tastenkombinationen für die Verfahren in diesem Thema finden Sie unter **Keyboard shortcuts in Exchange 2013**.</span><span class="sxs-lookup"><span data-stu-id="aeadb-112">For information about keyboard shortcuts that may apply to the procedures in this topic, see **Keyboard shortcuts in the Exchange admin center**.</span></span>
  
## <a name="use-the-eac-to-create-a-mail-flow-rule-to-view-users-manual-junk-phishing-and-not-junk-reports"></a><span data-ttu-id="aeadb-113">Verwenden Sie die Exchange-Verwaltungskonsole, um eine Nachrichtenflussregel zu erstellen, um Berichte zu Junk-E-Mails, Phishing und Nicht-Junk-E-Mails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aeadb-113">Use the EAC to create a mail flow rule to view users' manual junk, phishing, and not junk reports</span></span>

1. <span data-ttu-id="aeadb-114">Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="aeadb-114">In the EAC, navigate to **Mail flow** \> **Rules**.</span></span>
    
2. <span data-ttu-id="aeadb-115">Klicken Sie auf ![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif) und wählen Sie dann **Neue Regel erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="aeadb-115">Click ![Add Icon](media/ITPro-EAC-AddIcon.gif) and then select **Create a new rule**.</span></span>
    
3. <span data-ttu-id="aeadb-116">Benennen Sie die Regel, und klicken Sie dann auf **Weitere Optionen**.</span><span class="sxs-lookup"><span data-stu-id="aeadb-116">Give the rule a name and then click **More options**.</span></span>
    
4. <span data-ttu-id="aeadb-117">Unter **Diese Regel anwenden, wenn...** können Sie **Empfänger** und anschließend **Adresse enthält eines dieser Wörter** wählen.</span><span class="sxs-lookup"><span data-stu-id="aeadb-117">Under **Apply this rule if**, select **The recipient** and then choose **address includes any of these words**.</span></span>
    
5. <span data-ttu-id="aeadb-118">Im Feld **Wörter oder Ausdrücke angeben** müssen Sie folgende Änderungen vornehmen:</span><span class="sxs-lookup"><span data-stu-id="aeadb-118">In the **specify words or phrases** box, do the following:</span></span> 
    - <span data-ttu-id="aeadb-p103">Geben `abuse@messaging.microsoft.com` Sie ein, ![und klicken](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol `junk@office365.microsoft.com` hinzufügen, ![und geben](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol hinzufügen. Diese e-Mail-Adressen werden verwendet, um falsch negative Nachrichten an Microsoft zu senden.</span><span class="sxs-lookup"><span data-stu-id="aeadb-p103">Type `abuse@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). These email addresses are used to submit false negative messages to Microsoft.</span></span>
    - <span data-ttu-id="aeadb-p104">Geben `phish@office365.microsoft.com` Sie ein, ![und klicken](media/ITPro-EAC-AddIcon.gif)Sie auf Symbol hinzufügen. Diese e-Mail-Adresse wird verwendet, um verpasste Phishing-Nachrichten an Microsoft zu senden.</span><span class="sxs-lookup"><span data-stu-id="aeadb-p104">Type `phish@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). This email address is used to submit missed phishing messages to Microsoft.</span></span>
    - <span data-ttu-id="aeadb-p105">Geben `false_positive@messaging.microsoft.com` Sie ein, ![und klicken](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol `not_junk@office365.microsoft.com` hinzufügen, ![und geben](media/ITPro-EAC-AddIcon.gif)Sie dann auf Symbol hinzufügen. Diese e-Mail-Adressen werden verwendet, um falsch positive Nachrichten an Microsoft zu senden.</span><span class="sxs-lookup"><span data-stu-id="aeadb-p105">Type `false_positive@messaging.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif), and then type `not_junk@office365.microsoft.com` and then click ![Add Icon](media/ITPro-EAC-AddIcon.gif). These email addresses are used to submit false positive messages to Microsoft.</span></span>
    - <span data-ttu-id="aeadb-125">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="aeadb-125">Click **ok**.</span></span>
    
6. <span data-ttu-id="aeadb-126">Wählen Sie unter **Folgendes ausführen** die Option **Bcc der Nachricht an...** aus, und wählen Sie dann die Postfächer aus, in denen Sie Nachrichten erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="aeadb-126">Under **Do the following**, select **Bcc the message to...** and then and then select the mailboxes where you'd like to receive the messages.</span></span> 
    
7. <span data-ttu-id="aeadb-p106">Wenn Sie möchten, können Sie eine Auswahl treffen, um die Regel zu überwachen, die Regel zu testen, die Regel während eines bestimmten Zeitraums zu aktivieren und andere Optionen auszuwählen. Es wird empfohlen, die Regel für einen Zeitraum zu testen, bevor Sie Sie erzwingen. Weitere Informationen finden Sie unter [Verfahren für Nachrichtenfluss Regeln](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span><span class="sxs-lookup"><span data-stu-id="aeadb-p106">If you'd like, you can make selections to audit the rule, test the rule, activate the rule during a specific time period, and other selections. We recommend testing the rule for a period before you enforce it. See [Procedures for mail flow rules](https://docs.microsoft.com/Exchange/policy-and-compliance/mail-flow-rules/mail-flow-rule-procedures).</span></span> 
    
8. <span data-ttu-id="aeadb-p107">Klicken Sie auf die Schaltfläche **Speichern**, um die Regel zu speichern. Sie wird in der Liste der Regeln angezeigt.</span><span class="sxs-lookup"><span data-stu-id="aeadb-p107">Click the **save** button to save the rule. It appears in your list of rules.</span></span> 
    
<span data-ttu-id="aeadb-132">Nachdem Sie die Regel erstellt und durchgesetzt haben, werden sämtliche von Ihrer Organisation aus an vorgegebene E-Mail-Adressen gesendeten Nachrichten in das angegebene Postfach kopiert.</span><span class="sxs-lookup"><span data-stu-id="aeadb-132">After you create and enforce the rule, any messages that are sent from your organization to specified email addresses will be copied to the specified mailbox.</span></span>
  

