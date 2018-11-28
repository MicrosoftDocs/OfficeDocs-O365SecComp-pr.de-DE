---
title: Aktivieren des Berichtsnachrichts-Add-Ins
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 11/19/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
description: Erfahren Sie, wie der Bericht-add-in für Outlook und Outlook im Web, für einzelne Benutzer oder der gesamten Organisation zu aktivieren.
ms.openlocfilehash: f35899d3f0be9ee07cb6dae5c5fec40395948340
ms.sourcegitcommit: 2cf7f5bb282c971d33e00f65d9982a3f14aec74e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/27/2018
ms.locfileid: "26706369"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="58161-103">Aktivieren des Berichtsnachrichts-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="58161-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="58161-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="58161-104">Overview</span></span>

<span data-ttu-id="58161-p101">Der Bericht-add-in für Outlook und Outlook im Web ermöglicht Personen auf einfache Weise falsch klassifizierte e-Mail, ob die sichere oder böswilliges, in der Regel für die Analyse Unwichtigstes. Microsoft verwendet diese Informationen, um die Effektivität des e-Mail-Schutz Technologien verbessern. Darüber hinaus Wenn Ihre Organisation [Office 365 erweiterte Threat Protection](office-365-atp.md) oder [Office 365 Bedrohungsanalyse](office-365-ti.md)verwendet wird, enthält das Bericht-add-in Ihrer Organisation Security Team nützliche Informationen, die sie verwenden können, um zu prüfen und aktualisieren Sicherheitsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="58161-p101">The Report Message add-in for Outlook and Outlook on the Web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="58161-p102">Nehmen wir beispielsweise bei Personen viele Nachrichten als Phishing melden möchten. Diese Informationen Flächen in das [Dashboard Sicherheit](security-dashboard.md) und sonstige Berichte. Security-Team Ihrer Organisation können diese Informationen als eine Angabe, die Anti-Phishing-Richtlinien möglicherweise aktualisiert werden. Oder wenn Personen viele Nachrichten protokolliert werden, die als Junk-e-Mail Junk gekennzeichnet wurden, mithilfe des Bericht-add-Ins, Security-Team Ihrer Organisation müssen möglicherweise passen Sie die [Anti-Spam-Richtlinien](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="58161-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="58161-112">Das Add-in Berichtnachricht funktioniert mit Ihrem Office 365-Abonnement und die folgenden Produkte:</span><span class="sxs-lookup"><span data-stu-id="58161-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="58161-113">Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="58161-113">Outlook on the Web</span></span>
 - <span data-ttu-id="58161-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="58161-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="58161-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58161-115">Outlook 2016</span></span>
 - <span data-ttu-id="58161-116">Outlook 2016 für Mac</span><span class="sxs-lookup"><span data-stu-id="58161-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="58161-117">Outlook im Lieferumfang von Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="58161-117">Outlook included with Office 365 ProPlus</span></span>
  
<span data-ttu-id="58161-118">Wenn Sie einen einzelnen Benutzer sind, können Sie [den Bericht-add-in für sich selbst zu aktivieren](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="58161-118">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="58161-p103">Wenn Sie ein globaler Office 365-Administrator oder Exchange Online-Administrator sind und Exchange so konfiguriert ist, dass OAuth-Authentifizierung verwenden, können Sie [den Bericht-add-in für Ihre Organisation zu aktivieren](#get-and-enable-the-report-message-add-in-for-your-organization). Die Nachricht-Add-In für Berichts ist nun durch [Zentralisierte Bereitstellung](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="58161-p103">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="58161-121">Die Meldung Bericht-add-in für sich selbst</span><span class="sxs-lookup"><span data-stu-id="58161-121">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="58161-122">Suchen Sie in [Microsoft Elemente verwenden](https://appsource.microsoft.com/marketplace/apps)für den [Bericht-add-in](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="58161-122">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="58161-123">Wählen Sie **erhalten IT jetzt**.</span><span class="sxs-lookup"><span data-stu-id="58161-123">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="58161-124">![Melden Sie Meldung – jetzt abrufen](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="58161-124">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="58161-p104">Beachten Sie die Bestimmungen der Verwendung und der Datenschutzrichtlinie. Wählen Sie dann **Weiter**aus.</span><span class="sxs-lookup"><span data-stu-id="58161-p104">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="58161-127">Melden Sie sich bei Ihrem Office 365-e-Mail mit Ihrer Arbeit oder Schule-Konto (zur Verwendung von Business) oder Ihrem Microsoft-Konto (zur persönlichen Verwendung).</span><span class="sxs-lookup"><span data-stu-id="58161-127">Sign in to your Office 365 email using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="58161-128">Nachdem das Add-in installiert und aktiviert ist, sehen Sie die folgenden Symbole:</span><span class="sxs-lookup"><span data-stu-id="58161-128">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="58161-129">In Outlook sieht das Symbol:</span><span class="sxs-lookup"><span data-stu-id="58161-129">In Outlook the icon looks like this:</span></span> <br/> ![Bericht Nachricht-Add-in für Outlook Symbol](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="58161-131">In Outlook Web App sieht das Symbol:</span><span class="sxs-lookup"><span data-stu-id="58161-131">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook auf das Symbol Nachricht für Web-Bericht-Add-in](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

<span data-ttu-id="58161-133">Als nächsten Schritt erfahren Sie, wie Sie zur [Verwendung des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="58161-133">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="58161-134">Abrufen und das Bericht-add-in für Ihre Organisation zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="58161-134">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58161-p105">Sie müssen ein globaler Office 365-Administrator oder Exchange Online-Administrator, zum Abschließen dieser Aufgabe sein. Darüber hinaus muss Exchange konfiguriert sein, um OAuth-Authentifizierung zum Weitere Informationen finden Sie unter [Anforderungen an Exchange (zentralisierte Bereitstellung von add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="58161-p105">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="58161-137">Wechseln Sie auf die [Dienste & Seite-add-ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in der neuen Microsoft-365-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="58161-137">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="58161-138">![Dienste und Add-Ins Seite in der neuen Microsoft-365-Verwaltungskonsole](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="58161-138">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="58161-139">Wählen Sie **+ -Add-in bereitstellen**.</span><span class="sxs-lookup"><span data-stu-id="58161-139">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="58161-140">![Wählen Sie Add-In bereitstellen](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="58161-140">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="58161-141">Überprüfen Sie die Informationen im Fenster Neues Add-In, und wählen Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="58161-141">In the New Add-In screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="58161-142">![Neue Add-in-details](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="58161-142">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="58161-143">Wählen Sie **ich ein Add-in aus dem Office Store hinzufügen möchten**, und wählen Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="58161-143">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="58161-144">![Ich möchte eine neue Add-In hinzufügen](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="58161-144">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="58161-145">Durchsuchen Sie und in der Liste der Ergebnisse, die neben den Bericht Nachricht-Add-In für Berichts-Nachricht, wählen Sie hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="58161-145">Search for Report Message, and in the list of results, next to the Report Message Add-In, choose Add.</span></span><br/>![Bericht-Nachricht gesucht, und wählen Sie dann hinzufügen](media/NewAddInScreen3.png)<br/>
    
6. <span data-ttu-id="58161-147">Überprüfen Sie die Informationen auf dem Bildschirm Bericht, und wählen Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="58161-147">On the Report Message screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="58161-148">![Bericht Nachrichtendetails](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="58161-148">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="58161-149">Geben Sie die Standardeinstellungen für Benutzer für Outlook, und wählen Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="58161-149">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="58161-150">![Melden Sie Meldung Standardeinstellungen für Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="58161-150">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="58161-151">Geben Sie wer das Bericht-Add-in, und wählen Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="58161-151">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="58161-152">![Wer die Nachricht Bericht-add-in](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="58161-152">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="58161-153">[Einrichten einer Regel zum Abrufen einer Kopie der e-Mail-Nachrichten von den Benutzern gemeldet](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users) werden sollten</span><span class="sxs-lookup"><span data-stu-id="58161-153">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users)</span></span>

<span data-ttu-id="58161-p106">Je nachdem, was Sie mit dem Assistenten ausgewählt müssen die Personen in Ihrer Organisation des [Berichtnachricht-add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) zur Verfügung. Personen in Ihrer Organisation werden die folgenden Symbole angezeigt:</span><span class="sxs-lookup"><span data-stu-id="58161-p106">Depending on what you selected using the wizard, people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="58161-156">In Outlook sieht das Symbol:</span><span class="sxs-lookup"><span data-stu-id="58161-156">In Outlook the icon looks like this:</span></span> <br/> ![Bericht Nachricht-Add-in für Outlook Symbol](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="58161-158">In Outlook Web App sieht das Symbol:</span><span class="sxs-lookup"><span data-stu-id="58161-158">In Outlook Web App the icon looks like this:</span></span><br/>![Outlook auf das Symbol Nachricht für Web-Bericht-Add-in](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="58161-160">Richten Sie eine Regel zum Abrufen einer Kopie der e-Mail-Nachrichten von den Benutzern gemeldet</span><span class="sxs-lookup"><span data-stu-id="58161-160">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="58161-161">Sie müssen Exchange Online-Administrator zum Ausführen dieser Aufgabe sein.</span><span class="sxs-lookup"><span data-stu-id="58161-161">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="58161-p107">Sie können eine Regel einrichten, um eine Kopie der e-Mail-Nachrichten von Benutzern in Ihrer Organisation gemeldet abzurufen. Sie führen Sie diesen, nachdem Sie heruntergeladen und des Berichtnachricht-add-Ins für Ihre Organisation aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="58161-p107">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="58161-164">Wählen Sie in der Exchange-Verwaltungskonsole, **e-Mail-Fluss** \> **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="58161-164">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="58161-165">Wählen Sie **+** \> **neue Regel erstellen**.</span><span class="sxs-lookup"><span data-stu-id="58161-165">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="58161-166">Geben Sie im Feld **Name** einen Namen, beispielsweise Übermittlungen.</span><span class="sxs-lookup"><span data-stu-id="58161-166">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="58161-167">Wählen Sie in der Liste **diese Regel anwenden, wenn** **die Empfängeradresse enthält...** aus.</span><span class="sxs-lookup"><span data-stu-id="58161-167">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="58161-168">Klicken Sie im Bildschirm **Wörter oder Ausdrücke angeben** hinzufügen `junk@office365.microsoft.com` und `phish@office365.microsoft.com`, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="58161-168">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="58161-169">![Geben Sie die Junk-e- und Phishing e-Mail-Adressen für die Regel](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="58161-169">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="58161-170">Wählen Sie in der Liste **die folgenden Schritte aus...** **Bcc der Nachricht an...**.</span><span class="sxs-lookup"><span data-stu-id="58161-170">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="58161-171">Fügen Sie ein globaler Administrator, Sicherheitsadministrator und/oder Sicherheit Leser, die eine Kopie der einzelnen Personen an Microsoft gemeldet e-Mail-Nachricht erhalten sollen, und wählen Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="58161-171">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="58161-172">![Fügen Sie eine globale oder eine Sicherheitsgruppe Administrator, um eine Kopie jeder gemeldeten Nachricht empfangen hinzu](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="58161-172">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="58161-173">Wählen Sie **diese Regel mit Schweregrad**aus, und wählen Sie **Mittel**.</span><span class="sxs-lookup"><span data-stu-id="58161-173">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="58161-174">Wählen Sie unter **Wählen Sie einen Modus für diese Regel** **erzwingen**.</span><span class="sxs-lookup"><span data-stu-id="58161-174">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="58161-175">![Eine Regel richten Sie ein, um eine Kopie jeder Nachricht gemeldeten abzurufen](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="58161-175">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="58161-176">Klicken Sie auf **Save**.</span><span class="sxs-lookup"><span data-stu-id="58161-176">Choose **Save**.</span></span> 
    
<span data-ttu-id="58161-p108">Mit dieser Regel vorhanden Wenn eine Person in Ihrer Organisation eine e-Mail-Nachricht mit dem Bericht add-in, meldet erhalten Ihrer globaler Administrator, Sicherheitsadministrator und/oder Sicherheit Reader eine Kopie der Nachricht. Diese Informationen können Sie festlegen oder Richtlinien, wie [Links zu Office 365 ATP sicherer](atp-safe-links.md) Richtlinien anpassen.</span><span class="sxs-lookup"><span data-stu-id="58161-p108">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies.</span></span> 

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="58161-179">Überprüfen Sie oder bearbeiten Sie der Einstellungen für den Bericht-add-in</span><span class="sxs-lookup"><span data-stu-id="58161-179">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="58161-180">Sie können überprüfen und bearbeiten die Standardeinstellungen für den Bericht Nachricht Add-In auf der [Seite Dienste und Add-Ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="58161-180">You can review and edit the default settings for the Report Message Add-In in the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="58161-181">Sie müssen ein globaler Office 365-Administrator oder Exchange Online-Administrator, zum Abschließen dieser Aufgabe sein.</span><span class="sxs-lookup"><span data-stu-id="58161-181">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="58161-182">Wechseln Sie auf die [Dienste & Seite-add-ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in der neuen Microsoft-365-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="58161-182">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the new Microsoft 365 admin center.</span></span><br/><span data-ttu-id="58161-183">![Dienste und Add-Ins Seite in der neuen Microsoft-365-Verwaltungskonsole](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="58161-183">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="58161-184">Suchen Sie und wählen Sie die Nachricht-Add-In für Berichts.</span><span class="sxs-lookup"><span data-stu-id="58161-184">Find and select the Report Message Add-In.</span></span><br/>![Suchen Sie und wählen Sie des Berichtnachricht-add-Ins aus](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="58161-186">Überprüfen Sie auf dem Bildschirm Berichtnachricht und bearbeiten Sie der Einstellungen entsprechend den Anforderungen Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="58161-186">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Einstellungen für den Bericht-add-in](media/EditReportMessageAddIn.png)<br/> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="58161-188">Informationen Sie zur Verwendung des Berichtnachricht-add-Ins</span><span class="sxs-lookup"><span data-stu-id="58161-188">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="58161-189">Finden Sie unter [Verwenden des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="58161-189">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="58161-190">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="58161-190">Related topics</span></span>

[<span data-ttu-id="58161-191">Verwenden des Add-Ins Nachricht melden</span><span class="sxs-lookup"><span data-stu-id="58161-191">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="58161-192">Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="58161-192">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="58161-193">Anzeigen von Berichten für Office 365 erweiterte Threat Protection</span><span class="sxs-lookup"><span data-stu-id="58161-193">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="58161-194">Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="58161-194">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

