---
title: Aktivieren des Berichtsnachrichts-Add-Ins
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie der Bericht-add-in für Outlook und Outlook im Web, für einzelne Benutzer oder der gesamten Organisation zu aktivieren.
ms.openlocfilehash: 8c061d14d11aa868567487186c5dcca534b86215
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995156"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="d0fca-103">Aktivieren des Berichtsnachrichts-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="d0fca-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="d0fca-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="d0fca-104">Overview</span></span>

<span data-ttu-id="d0fca-p101">Der Bericht-add-in für Outlook und Outlook im Web ermöglicht Personen auf einfache Weise falsch klassifizierte e-Mail, ob die sichere oder böswilliges, in der Regel für die Analyse Unwichtigstes. Microsoft verwendet diese Informationen, um die Effektivität des e-Mail-Schutz Technologien verbessern. Darüber hinaus Wenn Ihre Organisation [Office 365 erweiterte Threat Protection](office-365-atp.md) oder [Office 365 Bedrohungsanalyse](office-365-ti.md)verwendet wird, enthält das Bericht-add-in Ihrer Organisation Security Team nützliche Informationen, die sie verwenden können, um zu prüfen und aktualisieren Sicherheitsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="d0fca-p101">The Report Message add-in for Outlook and Outlook on the web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="d0fca-p102">Nehmen wir beispielsweise bei Personen viele Nachrichten als Phishing melden möchten. Diese Informationen Flächen in das [Dashboard Sicherheit](security-dashboard.md) und sonstige Berichte. Security-Team Ihrer Organisation können diese Informationen als eine Angabe, die Anti-Phishing-Richtlinien möglicherweise aktualisiert werden. Oder wenn Personen viele Nachrichten protokolliert werden, die als Junk-e-Mail Junk gekennzeichnet wurden, mithilfe des Bericht-add-Ins, Security-Team Ihrer Organisation müssen möglicherweise passen Sie die [Anti-Spam-Richtlinien](configure-the-anti-spam-policies.md).</span><span class="sxs-lookup"><span data-stu-id="d0fca-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="d0fca-112">Das Add-in Berichtnachricht funktioniert mit Ihrem Office 365-Abonnement und die folgenden Produkte:</span><span class="sxs-lookup"><span data-stu-id="d0fca-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="d0fca-113">Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="d0fca-113">Outlook on the web</span></span>
 - <span data-ttu-id="d0fca-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="d0fca-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="d0fca-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0fca-115">Outlook 2016</span></span>
 - <span data-ttu-id="d0fca-116">Outlook 2016 für Mac</span><span class="sxs-lookup"><span data-stu-id="d0fca-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="d0fca-117">Outlook im Lieferumfang von Office 365 ProPlus</span><span class="sxs-lookup"><span data-stu-id="d0fca-117">Outlook included with Office 365 ProPlus</span></span>

> [!NOTE]
> <span data-ttu-id="d0fca-p103">Der Bericht-add-in für Outlook und Outlook im Web ist dasselbe wie die [Junk-e-Mail-Filter für Outlook](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)nicht genau über wenngleich beide e-Mail als Junk, keine Junk-e- oder Phishing-Versuch markiert verwendet werden können. Der Bericht-add-in für Outlook und Outlook im Web benachrichtigt Microsoft Informationen zu falsch klassifizierte e-Mail während der Junk-e-Mail-Filter für Outlook zum Organisieren von e-Mail-Nachrichten im Postfach des Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d0fca-p103">The Report Message add-in for Outlook and Outlook on the web is not exactly the same thing as the [Outlook Junk Email Filter](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), although both can be used to mark email as junk, not junk, or a phishing attempt. The Report Message add-in for Outlook and Outlook on the web notifies Microsoft about misclassified email, whereas the Outlook Junk Email Filter is used to organize email messages in a user's mailbox.</span></span> 
  
<span data-ttu-id="d0fca-120">Wenn Sie einen einzelnen Benutzer sind, können Sie [den Bericht-add-in für sich selbst zu aktivieren](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="d0fca-120">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="d0fca-p104">Wenn Sie ein globaler Office 365-Administrator oder Exchange Online-Administrator sind und Exchange so konfiguriert ist, dass OAuth-Authentifizierung verwenden, können Sie [den Bericht-add-in für Ihre Organisation zu aktivieren](#get-and-enable-the-report-message-add-in-for-your-organization). Die Nachricht-Add-In für Berichts ist nun durch [Zentralisierte Bereitstellung](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d0fca-p104">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="d0fca-123">Die Meldung Bericht-add-in für sich selbst</span><span class="sxs-lookup"><span data-stu-id="d0fca-123">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="d0fca-124">Suchen Sie in [Microsoft Elemente verwenden](https://appsource.microsoft.com/marketplace/apps)für den [Bericht-add-in](https://appsource.microsoft.com/product/office/wa104381180).</span><span class="sxs-lookup"><span data-stu-id="d0fca-124">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="d0fca-125">Wählen Sie **erhalten IT jetzt**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-125">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="d0fca-126">![Melden Sie Meldung – jetzt abrufen](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-126">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="d0fca-p105">Beachten Sie die Bestimmungen der Verwendung und der Datenschutzrichtlinie. Wählen Sie dann **Weiter**aus.</span><span class="sxs-lookup"><span data-stu-id="d0fca-p105">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="d0fca-129">Melden Sie sich bei Office 365 mit Ihrer Arbeit oder Schule Konto (zur Verwendung von Business) oder Ihrem Microsoft-Konto (zur persönlichen Verwendung).</span><span class="sxs-lookup"><span data-stu-id="d0fca-129">Sign in to Office 365 using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="d0fca-130">Nachdem das Add-in installiert und aktiviert ist, sehen Sie die folgenden Symbole:</span><span class="sxs-lookup"><span data-stu-id="d0fca-130">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="d0fca-131">In Outlook sieht das Symbol:</span><span class="sxs-lookup"><span data-stu-id="d0fca-131">In Outlook, the icon looks like this:</span></span> <br/> ![Melden Sie Meldung Add-In-Symbol für Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="d0fca-133">In Outlook Web App (oder in Outlook im Web) sieht das Symbol:</span><span class="sxs-lookup"><span data-stu-id="d0fca-133">In Outlook Web App (or Outlook on the web), the icon looks like this:</span></span><br/>![Outlook auf das Symbol Berichtnachricht-add-ins web](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="d0fca-135">Als nächsten Schritt erfahren Sie, wie Sie zur [Verwendung des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="d0fca-135">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="d0fca-136">Abrufen und das Bericht-add-in für Ihre Organisation zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="d0fca-136">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0fca-p106">Sie müssen ein globaler Office 365-Administrator oder Exchange Online-Administrator, zum Abschließen dieser Aufgabe sein. Darüber hinaus muss Exchange konfiguriert sein, um OAuth-Authentifizierung zum Weitere Informationen finden Sie unter [Anforderungen an Exchange (zentralisierte Bereitstellung von add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d0fca-p106">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="d0fca-139">Wechseln Sie zur [Seite für Dienste &-add-ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in der Microsoft-365-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="d0fca-139">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="d0fca-140">![Dienste und Add-Ins Seite in der neuen Microsoft-365-Verwaltungskonsole](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-140">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="d0fca-141">Wählen Sie **+ -Add-in bereitstellen**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-141">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="d0fca-142">![Wählen Sie Add-In bereitstellen](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-142">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="d0fca-143">Überprüfen Sie die Informationen im Fenster **Neues Add-In** , und wählen Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-143">In the **New Add-In** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="d0fca-144">![Neue Add-in-details](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-144">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="d0fca-145">Wählen Sie **ich ein Add-in aus dem Office Store hinzufügen möchten**, und wählen Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-145">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="d0fca-146">![Ich möchte eine neue Add-In hinzufügen](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-146">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="d0fca-147">Durchsuchen Sie und in der Liste der Ergebnisse, neben dem **Bericht Nachricht-Add-In**für **Berichts-Nachricht**, wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-147">Search for **Report Message**, and in the list of results, next to the **Report Message Add-In**, choose **Add**.</span></span><br/><span data-ttu-id="d0fca-148">![Bericht-Nachricht gesucht, und wählen Sie dann hinzufügen](media/NewAddInScreen3.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-148">![Search for Report Message and then choose Add](media/NewAddInScreen3.png)</span></span><br/>
    
6. <span data-ttu-id="d0fca-149">Überprüfen Sie die Informationen auf dem Bildschirm **Bericht** , und wählen Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-149">On the **Report Message** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="d0fca-150">![Bericht Nachrichtendetails](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-150">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="d0fca-151">Geben Sie die Standardeinstellungen für Benutzer für Outlook, und wählen Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-151">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="d0fca-152">![Melden Sie Meldung Standardeinstellungen für Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-152">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="d0fca-153">Geben Sie wer das Bericht-Add-in, und wählen Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-153">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="d0fca-154">![Wer die Nachricht Bericht-add-in](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-154">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="d0fca-155">Wir empfehlen [eine Regel zum Abrufen einer Kopie der e-Mail-Nachrichten von den Benutzern gemeldet einrichten](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span><span class="sxs-lookup"><span data-stu-id="d0fca-155">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span></span>

<span data-ttu-id="d0fca-p107">Personen in Ihrer Organisation müssen je nachdem, was Sie ausgewählt haben, wenn Sie das Add-in (Schritte 7-8 oben), Einrichten des [Berichtnachricht-Add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) zur Verfügung. Personen in Ihrer Organisation werden die folgenden Symbole angezeigt:</span><span class="sxs-lookup"><span data-stu-id="d0fca-p107">Depending on what you selected when you set up the add-in (steps 7-8 above), people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="d0fca-158">In Outlook sieht das Symbol:</span><span class="sxs-lookup"><span data-stu-id="d0fca-158">In Outlook, the icon looks like this:</span></span> <br/> ![Bericht Nachricht-Add-in für Outlook Symbol](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="d0fca-160">In Outlook Web App (oder in Outlook im Web) sieht das Symbol:</span><span class="sxs-lookup"><span data-stu-id="d0fca-160">In Outlook Web App (or Outlook on the web), the icon looks like this:</span></span><br/>![Outlook auf das Symbol Nachricht für Web-Bericht-Add-in](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="d0fca-162">Wenn Sie Benutzer über das Add-in Bericht darüber informieren, fügen Sie einen Hyperlink zum [Verwenden des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="d0fca-162">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="d0fca-163">Richten Sie eine Regel zum Abrufen einer Kopie der e-Mail-Nachrichten von den Benutzern gemeldet</span><span class="sxs-lookup"><span data-stu-id="d0fca-163">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d0fca-164">Sie müssen Exchange Online-Administrator zum Ausführen dieser Aufgabe sein.</span><span class="sxs-lookup"><span data-stu-id="d0fca-164">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="d0fca-p108">Sie können eine Regel einrichten, um eine Kopie der e-Mail-Nachrichten von Benutzern in Ihrer Organisation gemeldet abzurufen. Sie führen Sie diesen, nachdem Sie heruntergeladen und des Berichtnachricht-add-Ins für Ihre Organisation aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="d0fca-p108">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="d0fca-167">Wählen Sie in der Exchange-Verwaltungskonsole, **e-Mail-Fluss** \> **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-167">In the Exchange Admin Center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="d0fca-168">Wählen Sie **+** \> **neue Regel erstellen**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-168">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="d0fca-169">Geben Sie im Feld **Name** einen Namen, beispielsweise Übermittlungen.</span><span class="sxs-lookup"><span data-stu-id="d0fca-169">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="d0fca-170">Wählen Sie in der Liste **diese Regel anwenden, wenn** **die Empfängeradresse enthält...** aus.</span><span class="sxs-lookup"><span data-stu-id="d0fca-170">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="d0fca-171">Klicken Sie im Bildschirm **Wörter oder Ausdrücke angeben** hinzufügen `junk@office365.microsoft.com` und `phish@office365.microsoft.com`, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-171">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="d0fca-172">![Geben Sie die Junk-e- und Phishing e-Mail-Adressen für die Regel](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-172">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="d0fca-173">Wählen Sie in der Liste **die folgenden Schritte aus...** **Bcc der Nachricht an...**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-173">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="d0fca-174">Fügen Sie ein globaler Administrator, Sicherheitsadministrator und/oder Sicherheit Leser, die eine Kopie der einzelnen Personen an Microsoft gemeldet e-Mail-Nachricht erhalten sollen, und wählen Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-174">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="d0fca-175">![Fügen Sie eine globale oder eine Sicherheitsgruppe Administrator, um eine Kopie jeder gemeldeten Nachricht empfangen hinzu](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-175">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="d0fca-176">Wählen Sie **diese Regel mit Schweregrad**aus, und wählen Sie **Mittel**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-176">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="d0fca-177">Wählen Sie unter **Wählen Sie einen Modus für diese Regel** **erzwingen**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-177">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="d0fca-178">![Eine Regel richten Sie ein, um eine Kopie jeder Nachricht gemeldeten abzurufen](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-178">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="d0fca-179">Klicken Sie auf **Save**.</span><span class="sxs-lookup"><span data-stu-id="d0fca-179">Choose **Save**.</span></span> 
    
<span data-ttu-id="d0fca-p109">Mit dieser Regel vorhanden Wenn eine Person in Ihrer Organisation eine e-Mail-Nachricht mit dem Bericht add-in, meldet erhalten Ihrer globaler Administrator, Sicherheitsadministrator und/oder Sicherheit Reader eine Kopie der Nachricht. Diese Informationen können Sie festlegen oder Richtlinien, wie [Links zu Office 365 ATP sicherer](atp-safe-links.md) Richtlinien oder Ihre [Anti-Spam-](anti-spam-protection.md) Einstellungen anpassen.</span><span class="sxs-lookup"><span data-stu-id="d0fca-p109">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies, or your [anti-spam](anti-spam-protection.md) settings.</span></span> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="d0fca-182">Informationen Sie zur Verwendung des Berichtnachricht-add-Ins</span><span class="sxs-lookup"><span data-stu-id="d0fca-182">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="d0fca-183">Finden Sie unter [Verwenden des Berichtnachricht-add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="d0fca-183">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="d0fca-184">Überprüfen Sie oder bearbeiten Sie der Einstellungen für den Bericht-add-in</span><span class="sxs-lookup"><span data-stu-id="d0fca-184">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="d0fca-185">Sie können überprüfen und bearbeiten die Standardeinstellungen für den Bericht-add-in auf der [Seite für Dienste &-Add-Ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span><span class="sxs-lookup"><span data-stu-id="d0fca-185">You can review and edit the default settings for the Report Message add-in on the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="d0fca-186">Sie müssen ein globaler Office 365-Administrator oder Exchange Online-Administrator, zum Abschließen dieser Aufgabe sein.</span><span class="sxs-lookup"><span data-stu-id="d0fca-186">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="d0fca-187">Wechseln Sie zur [Seite für Dienste &-add-ins](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in der Microsoft-365-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="d0fca-187">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="d0fca-188">![Dienste und Add-Ins Seite in der neuen Microsoft-365-Verwaltungskonsole](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="d0fca-188">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="d0fca-189">Suchen Sie und wählen Sie die Add-in-Bericht.</span><span class="sxs-lookup"><span data-stu-id="d0fca-189">Find and select the Report Message add-in.</span></span><br/>![Suchen Sie und wählen Sie des Berichtnachricht-add-Ins aus](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="d0fca-191">Überprüfen Sie auf dem Bildschirm Berichtnachricht und bearbeiten Sie der Einstellungen entsprechend den Anforderungen Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="d0fca-191">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Einstellungen für den Bericht-add-in](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a><span data-ttu-id="d0fca-193">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="d0fca-193">Related topics</span></span>

[<span data-ttu-id="d0fca-194">Verwenden des Add-Ins Nachricht melden</span><span class="sxs-lookup"><span data-stu-id="d0fca-194">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="d0fca-195">Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="d0fca-195">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="d0fca-196">Anzeigen von Berichten für Office 365 erweiterte Threat Protection</span><span class="sxs-lookup"><span data-stu-id="d0fca-196">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="d0fca-197">Verwenden Sie in das Wertpapier Explorer &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="d0fca-197">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

