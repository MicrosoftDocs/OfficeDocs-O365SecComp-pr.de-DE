---
title: Aktivieren des Berichtsnachrichts-Add-Ins
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/18/2019
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 4250c4bc-6102-420b-9e0a-a95064837676
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Sie das Berichtnachrichten-Add-in für Outlook und Outlook im Web für einzelne Benutzer oder Ihre gesamte Organisation aktivieren können.
ms.openlocfilehash: c184b7ac1baef297d65e6e93e4e7a085920d87b0
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341426"
---
# <a name="enable-the-report-message-add-in"></a><span data-ttu-id="288ec-103">Aktivieren des Berichtsnachrichts-Add-Ins</span><span class="sxs-lookup"><span data-stu-id="288ec-103">Enable the Report Message add-in</span></span>

## <a name="overview"></a><span data-ttu-id="288ec-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="288ec-104">Overview</span></span>

<span data-ttu-id="288ec-p101">Das Berichtnachrichten-Add-in für Outlook und Outlook im Web ermöglicht es Benutzern, problemlos falsch klassifizierte e-Mails, ob sicher oder bösartig, an Microsoft und ihre Partner zur Analyse zu melden. Microsoft verwendet diese Übermittlungen, um die Effektivität von e-Mail-Schutztechnologien zu verbessern. Wenn in Ihrer Organisation [office 365 Advanced Threat Protection](office-365-atp.md) oder [Office 365 Threat Intelligence](office-365-ti.md)verwendet wird, stellt das Add-in "Berichtnachricht" Darüber hinaus für das Sicherheitsteam Ihrer Organisation nützliche Informationen zur Verfügung, die Sie zum überarbeiten und aktualisieren verwenden können. Sicherheitsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="288ec-p101">The Report Message add-in for Outlook and Outlook on the web enables people to easily report misclassified email, whether safe or malicious, to Microsoft and its affiliates for analysis. Microsoft uses these submissions to improve the effectiveness of email protection technologies. In addition, if your organization is using [Office 365 Advanced Threat Protection](office-365-atp.md) or [Office 365 Threat Intelligence](office-365-ti.md), the Report Message add-in provides your organization's security team with useful information they can use to review and update security policies.</span></span> 

<span data-ttu-id="288ec-p102">Nehmen wir beispielsweise an, dass Benutzer viele Nachrichten als Phishing melden. Diese Informations Oberflächen werden im [Sicherheits Dashboard](security-dashboard.md) und in anderen Berichten angezeigt. Das Sicherheitsteam Ihrer Organisation kann diese Informationen als Hinweis dafür verwenden, dass Anti-Phishing-Richtlinien möglicherweise aktualisiert werden müssen. Oder wenn Personen viele Nachrichten melden, die mit dem Add-in "Berichtnachricht" als Junk-e-Mail als nicht-Junk markiert wurden, muss das Sicherheitsteam Ihrer Organisation möglicherweise [Anti-Spam-Richtlinien](configure-the-anti-spam-policies.md)anpassen.</span><span class="sxs-lookup"><span data-stu-id="288ec-p102">For example, suppose that people are reporting a lot of messages as phishing. This information surfaces in the [Security Dashboard](security-dashboard.md) and other reports. Your organization's security team can use this information as an indication that anti-phishing policies might need to be updated. Or, if people are reporting a lot of messages that were flagged as junk mail as Not Junk by using the Report Message add-in, your organization's security team might need to adjust [anti-spam policies](configure-the-anti-spam-policies.md).</span></span> 

<span data-ttu-id="288ec-112">Das Berichtnachrichten-Add-in funktioniert mit Ihrem Office 365-Abonnement und den folgenden Produkten:</span><span class="sxs-lookup"><span data-stu-id="288ec-112">The Report Message add-in works with your Office 365 subscription and the following products:</span></span>
 - <span data-ttu-id="288ec-113">Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="288ec-113">Outlook on the web</span></span>
 - <span data-ttu-id="288ec-114">Outlook 2013 SP1</span><span class="sxs-lookup"><span data-stu-id="288ec-114">Outlook 2013 SP1</span></span>
 - <span data-ttu-id="288ec-115">Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="288ec-115">Outlook 2016</span></span>
 - <span data-ttu-id="288ec-116">Outlook 2016 für Mac</span><span class="sxs-lookup"><span data-stu-id="288ec-116">Outlook 2016 for Mac</span></span>
 - <span data-ttu-id="288ec-117">Outlook im Lieferumfang von Office 365 proPlus</span><span class="sxs-lookup"><span data-stu-id="288ec-117">Outlook included with Office 365 ProPlus</span></span>

> [!NOTE]
> <span data-ttu-id="288ec-p103">Das Berichtnachrichten-Add-in für Outlook und Outlook im Web ist nicht genau dasselbe wie der [Outlook-Junk-e-Mail-Filter](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), obwohl beide verwendet werden können, um e-Mails als Junk, nicht als Junk oder als Phishing-Versuch zu kennzeichnen. Das Berichtnachrichten-Add-in für Outlook und Outlook im Web benachrichtigt Microsoft über falsch klassifizierte e-Mails, wohingegen der Outlook-Junk-e-Mail-Filter zum Organisieren von e-Mail-Nachrichten im Postfach eines Benutzers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="288ec-p103">The Report Message add-in for Outlook and Outlook on the web is not exactly the same thing as the [Outlook Junk Email Filter](https://support.office.com/article/Overview-of-the-Junk-Email-Filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089), although both can be used to mark email as junk, not junk, or a phishing attempt. The Report Message add-in for Outlook and Outlook on the web notifies Microsoft about misclassified email, whereas the Outlook Junk Email Filter is used to organize email messages in a user's mailbox.</span></span> 
  
<span data-ttu-id="288ec-120">Wenn Sie ein einzelner Benutzer sind, können Sie [das Berichtnachrichten-Add-in für sich selbst aktivieren](#get-the-report-message-add-in-for-yourself).</span><span class="sxs-lookup"><span data-stu-id="288ec-120">If you're an individual user, you can [enable the Report Message add-in for yourself](#get-the-report-message-add-in-for-yourself).</span></span> 
  
<span data-ttu-id="288ec-p104">Wenn Sie ein globaler Office 365-Administrator oder ein Exchange Online-Administrator sind und Exchange für die Verwendung der OAuth-Authentifizierung konfiguriert ist, können Sie [das Add-in für die Berichtnachricht für Ihre Organisation aktivieren](#get-and-enable-the-report-message-add-in-for-your-organization). Das Berichtnachrichten-Add-in ist jetzt über eine [zentralisierte Bereitstellung](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="288ec-p104">If you're an Office 365 global administrator or an Exchange Online administrator, and Exchange is configured to use OAuth authentication, you can [enable the Report Message add-in for your organization](#get-and-enable-the-report-message-add-in-for-your-organization). The Report Message Add-In is now available through [Centralized Deployment](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins).</span></span>
    
## <a name="get-the-report-message-add-in-for-yourself"></a><span data-ttu-id="288ec-123">Abrufen des Berichtsnachrichten-Add-Ins für sich selbst</span><span class="sxs-lookup"><span data-stu-id="288ec-123">Get the Report Message add-in for yourself</span></span>

1. <span data-ttu-id="288ec-124">Suchen Sie in [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps)nach dem [Add-in "Berichtnachricht](https://appsource.microsoft.com/product/office/wa104381180)".</span><span class="sxs-lookup"><span data-stu-id="288ec-124">In [Microsoft AppSource](https://appsource.microsoft.com/marketplace/apps), search for the [Report Message add-in](https://appsource.microsoft.com/product/office/wa104381180).</span></span>
    
2. <span data-ttu-id="288ec-125">Wählen Sie **get it now**aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-125">Choose **GET IT NOW**.</span></span><br/><span data-ttu-id="288ec-126">![Berichtnachricht-get it now](media/ReportMessageGETITNOW.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-126">![Report Message - Get It Now](media/ReportMessageGETITNOW.png)</span></span><br/> 
    
3. <span data-ttu-id="288ec-p105">Lesen Sie die Nutzungsbedingungen und Datenschutzrichtlinien. Klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="288ec-p105">Review the terms of use and privacy policy. Then choose **Continue**.</span></span> 
    
4. <span data-ttu-id="288ec-129">Melden Sie sich mit Ihrem Geschäfts-oder Schulkonto (für geschäftliche Zwecke) oder Ihrem Microsoft-Konto (für den persönlichen Gebrauch) bei Office 365 an.</span><span class="sxs-lookup"><span data-stu-id="288ec-129">Sign in to Office 365 using your work or school account (for business use) or your Microsoft account (for personal use).</span></span>
    
<span data-ttu-id="288ec-130">Nachdem das Add-in installiert und aktiviert wurde, werden die folgenden Symbole angezeigt:</span><span class="sxs-lookup"><span data-stu-id="288ec-130">After the add-in is installed and enabled, you'll see the following icons:</span></span> 

- <span data-ttu-id="288ec-131">In Outlook sieht das Symbol wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="288ec-131">In Outlook, the icon looks like this:</span></span> <br/> ![Add-in-Symbol für Berichtnachricht für Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="288ec-133">In Outlook im Web (früher als Outlook Web App bezeichnet) sieht das Symbol wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="288ec-133">In Outlook on the web (formerly known as Outlook Web App), the icon looks like this:</span></span><br/>![Add-in-Symbol für Outlook im Web-Bericht](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="288ec-135">Als nächsten Schritt erfahren Sie, wie Sie [das Add-in "Berichtnachricht" verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="288ec-135">As a next step, learn how to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>
  
## <a name="get-and-enable-the-report-message-add-in-for-your-organization"></a><span data-ttu-id="288ec-136">Abrufen und Aktivieren des Berichtsnachrichten-Add-Ins für Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="288ec-136">Get and enable the Report Message add-in for your organization</span></span>

> [!IMPORTANT]
> <span data-ttu-id="288ec-p106">Sie müssen ein globaler Office 365-Administrator oder ein Exchange Online-Administrator sein, um diese Aufgabe ausführen zu können. Darüber hinaus muss Exchange für die Verwendung der OAuth-Authentifizierung konfiguriert werden, um weitere Informationen zu erhalten, siehe [Exchange Requirements (zentralisierte Bereitstellung von Add-Ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span><span class="sxs-lookup"><span data-stu-id="288ec-p106">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task. In addition, Exchange must be configured to use OAuth authentication To learn more, see [Exchange requirements (Centralized Deployment of add-ins)](https://docs.microsoft.com/office365/admin/manage/centralized-deployment-of-add-ins&view=o365-worldwide#exchange-requirements).</span></span> 

1. <span data-ttu-id="288ec-139">Wechseln Sie zur [Seite &-Add-Ins für Dienste](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) im Microsoft 365 Admin Center.</span><span class="sxs-lookup"><span data-stu-id="288ec-139">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="288ec-140">![Seite "Dienste und Add-Ins" im neuen Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-140">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/> 
    
2. <span data-ttu-id="288ec-141">Wählen Sie **+ Add-in bereitstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-141">Choose **+ Deploy Add-in**.</span></span><br/><span data-ttu-id="288ec-142">![Wählen Sie Add-in bereitstellen](media/ServicesAddIns-ChooseDeployAddIn.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-142">![Choose Deploy Add-In](media/ServicesAddIns-ChooseDeployAddIn.png)</span></span><br/> 
    
3. <span data-ttu-id="288ec-143">Lesen Sie im **neuen Add-in-** Bildschirm die Informationen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="288ec-143">In the **New Add-In** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="288ec-144">![Neue Add-in-Details](media/NewAddInScreen1.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-144">![New Add-In details](media/NewAddInScreen1.png)</span></span><br/>
    
4. <span data-ttu-id="288ec-145">Wählen Sie **Ich möchte ein Add-in aus dem Office Store hinzufügen**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="288ec-145">Select **I want to add an Add-In from the Office Store**, and then choose **Next**.</span></span><br/><span data-ttu-id="288ec-146">![Ich möchte ein neues Add-in hinzufügen](media/NewAddInScreen2.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-146">![I want to add an new Add-In](media/NewAddInScreen2.png)</span></span><br/> 
    
5. <span data-ttu-id="288ec-147">Suchen Sie nach **Bericht Meldung**, und wählen Sie in der Ergebnisliste neben dem **Add-in Berichtnachricht**die Option **Hinzufügen**aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-147">Search for **Report Message**, and in the list of results, next to the **Report Message Add-In**, choose **Add**.</span></span><br/><span data-ttu-id="288ec-148">![Suchen Sie nach Bericht Meldung, und wählen Sie dann hinzufügen](media/NewAddInScreen3.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-148">![Search for Report Message and then choose Add](media/NewAddInScreen3.png)</span></span><br/>
    
6. <span data-ttu-id="288ec-149">Lesen Sie auf dem Bildschirm **Bericht Meldung** die Informationen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="288ec-149">On the **Report Message** screen, review the information, and then choose **Next**.</span></span><br/><span data-ttu-id="288ec-150">![Berichtnachrichten Details](media/ReportMessageAdd-InNewScreen4.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-150">![Report Message details](media/ReportMessageAdd-InNewScreen4.png)</span></span><br/>

7. <span data-ttu-id="288ec-151">Geben Sie die Benutzer Standardeinstellungen für Outlook an, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="288ec-151">Specify the user default settings for Outlook, and  then choose **Next**.</span></span><br/><span data-ttu-id="288ec-152">![Berichtsnachrichten-Standardeinstellungen für Outlook](media/ReportMessageOptionsScreen5.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-152">![Report Message default settings for Outlook](media/ReportMessageOptionsScreen5.png)</span></span><br/>

8. <span data-ttu-id="288ec-153">Geben Sie an, wer das Add-in für Berichtnachrichten abrufen soll, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="288ec-153">Specify who gets the Report Message Add-in, and then choose **Save**.</span></span> <br/><span data-ttu-id="288ec-154">![Wer ruft das Add-in für Berichtnachrichten ab](media/ReportMessageOptionsScreen6.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-154">![Who gets the Report Message add-in](media/ReportMessageOptionsScreen6.png)</span></span><br/>

> [!TIP]
> <span data-ttu-id="288ec-155">Es [wird empfohlen, eine Regel einzurichten, um eine Kopie der von Ihren Benutzern gemeldeten e-Mail-Nachrichten abzurufen](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span><span class="sxs-lookup"><span data-stu-id="288ec-155">We recommend [setting up a rule to get a copy of email messages reported by your users](#set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users).</span></span>

<span data-ttu-id="288ec-p107">Je nachdem, was Sie beim Einrichten des Add-ins ausgewählt haben (Schritte 7-8 oben), wird den Benutzern in Ihrer Organisation das [Add-in "Berichtnachricht](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) " zur Verfügung gestellt. Personen in Ihrer Organisation werden die folgenden Symbole angezeigt:</span><span class="sxs-lookup"><span data-stu-id="288ec-p107">Depending on what you selected when you set up the add-in (steps 7-8 above), people in your organization will have the [Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2) available. People in your organization will see the following icons:</span></span> 

- <span data-ttu-id="288ec-158">In Outlook sieht das Symbol wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="288ec-158">In Outlook, the icon looks like this:</span></span> <br/> ![Add-in-Symbol für Berichtnachricht für Outlook](media/OutlookReportMessageIcon.png)<br/>
- <span data-ttu-id="288ec-160">In Outlook im Web sieht das Symbol wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="288ec-160">In Outlook on the web, the icon looks like this:</span></span><br/>![Add-in-Symbol für Outlook im Web-Bericht](media/d9326d0b-1769-4bc2-ae58-51f0ebc69a17.png)<br/>

> [!TIP]
> <span data-ttu-id="288ec-162">Wenn Sie Benutzer über das Berichtnachrichten-Add-in Benachrichtigen, fügen Sie einen Link hinzu, um [das Berichtnachrichten-Add-in zu verwenden](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="288ec-162">When you notify users about the Report Message add-in, include a link to [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="set-up-a-rule-to-get-a-copy-of-email-messages-reported-by-your-users"></a><span data-ttu-id="288ec-163">Einrichten einer Regel zum Abrufen einer Kopie von e-Mail-Nachrichten, die von Ihren Benutzern gemeldet werden</span><span class="sxs-lookup"><span data-stu-id="288ec-163">Set up a rule to get a copy of email messages reported by your users</span></span>

> [!IMPORTANT]
> <span data-ttu-id="288ec-164">Zum Ausführen dieser Aufgabe müssen Sie Exchange Online-Administrator sein.</span><span class="sxs-lookup"><span data-stu-id="288ec-164">You must be an Exchange Online Administrator to perform this task.</span></span>
  
<span data-ttu-id="288ec-p108">Sie können eine Regel einrichten, um eine Kopie der von Benutzern in Ihrer Organisation gemeldeten e-Mail-Nachrichten abzurufen. Führen Sie dies aus, nachdem Sie das Add-in Berichtsnachricht für Ihre Organisation heruntergeladen und aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="288ec-p108">You can set up a rule to get a copy of email messages reported by users in your organization. You do this after you have downloaded and enabled the Report Message add-in for your organization.</span></span>
  
1. <span data-ttu-id="288ec-167">Wählen Sie im Exchange Admin Center **Nachrichtenfluss** \> **Regeln**aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-167">In the Exchange admin center, choose **mail flow** \> **rules**.</span></span> 
    
2. <span data-ttu-id="288ec-168">Wählen **+** \> Sie **neue Regel erstellen**aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-168">Choose **+** \> **Create a new rule**.</span></span> 
    
3. <span data-ttu-id="288ec-169">Geben Sie in das Feld **Name** einen Namen ein, beispielsweise Übermittlungen.</span><span class="sxs-lookup"><span data-stu-id="288ec-169">In the **Name** box, type a name, such as Submissions.</span></span>
    
4. <span data-ttu-id="288ec-170">Wählen Sie in der Liste **diese Regel anwenden, wenn** **die Empfängeradresse enthält...**.</span><span class="sxs-lookup"><span data-stu-id="288ec-170">In the **Apply this rule if** list, choose **The recipient address includes...**.</span></span> 
    
5. <span data-ttu-id="288ec-171">Fügen Sie im Bildschirm **Wörter oder Ausdrücke angeben den Text** hinzu `junk@office365.microsoft.com` , und `phish@office365.microsoft.com`wählen Sie dann **OK**aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-171">In the **specify words or phrases** screen, add `junk@office365.microsoft.com` and `phish@office365.microsoft.com`, and then choose **OK**.</span></span><br/><span data-ttu-id="288ec-172">![Angeben der Junk-und Phishing-e-Mail-Adressen für die Regel](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-172">![Specify the junk and phish email addresses for the rule](media/018c1833-f336-4333-a45c-f2e8b75cd698.png)</span></span><br/>
  
6. <span data-ttu-id="288ec-173">Wählen Sie in der Liste **führen Sie die folgenden** aus... **die Meldung Bcc an..**. aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-173">In the **Do the following...** list, choose **Bcc the message to...**.</span></span> 
    
7. <span data-ttu-id="288ec-174">Fügen Sie einen globalen Administrator, Sicherheitsadministrator und/oder Sicherheits Leser hinzu, der eine Kopie jeder e-Mail erhalten soll, die Personen an Microsoft melden, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="288ec-174">Add a global administrator, security administrator, and/or security reader who should receive a copy of each email message that people report to Microsoft, and then choose **OK**.</span></span><br/><span data-ttu-id="288ec-175">![Hinzufügen eines globalen oder Sicherheitsadministrators zum Empfangen einer Kopie jeder gemeldeten Nachricht](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-175">![Add a global or security administrator to receive a copy of each reported message](media/a91ab9d1-66f2-4a2e-9dc1-f9f81a2298ad.png)</span></span><br/>
  
8. <span data-ttu-id="288ec-176">Wählen Sie **diese Regel mit Schweregrad überwachen**aus, und wählen Sie **Mittel**aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-176">Select **Audit this rule with severity level**, and choose **Medium**.</span></span> 
    
9. <span data-ttu-id="288ec-177">Wählen Sie unter **Wählen Sie einen Modus für diese Regel**aus die Option **erzwingen**aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-177">Under **Choose a mode for this rule**, choose **Enforce**.</span></span><br/><span data-ttu-id="288ec-178">![Einrichten einer Regel zum Abrufen einer Kopie jeder gemeldeten Nachricht](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-178">![Set up a rule to get a copy of each reported message](media/f1cd95ce-e40d-4a8a-8f48-893469eba691.png)</span></span><br/>
  
10. <span data-ttu-id="288ec-179">Klicken Sie auf **Save**.</span><span class="sxs-lookup"><span data-stu-id="288ec-179">Choose **Save**.</span></span> 
    
<span data-ttu-id="288ec-p109">Wenn diese Regel gilt, erhalten Benutzer, die in Ihrer Organisation eine e-Mail-Nachricht mit dem Berichtnachrichten-Add-in melden, ihren globalen Administrator, Sicherheitsadministrator und/oder Sicherheits Leser eine Kopie dieser Nachricht. Mit diesen Informationen können Sie Richtlinien wie [Office 365 ATP](atp-safe-links.md) -Richtlinien für sichere Links oder Ihre Antispameinstellungen einrichten [](anti-spam-protection.md) oder anpassen.</span><span class="sxs-lookup"><span data-stu-id="288ec-p109">With this rule in place, whenever someone in your organization reports an email message using the Report Message add-in, your global administrator, security administrator, and/or security reader will receive a copy of that message. This information can enable you to set up or adjust policies, such as [Office 365 ATP Safe Links](atp-safe-links.md) policies, or your [anti-spam](anti-spam-protection.md) settings.</span></span> 

## <a name="learn-how-to-use-the-report-message-add-in"></a><span data-ttu-id="288ec-182">Informationen zur Verwendung des Berichtnachrichten-Add-ins</span><span class="sxs-lookup"><span data-stu-id="288ec-182">Learn how to use the Report Message add-in</span></span>

<span data-ttu-id="288ec-183">Weitere Informationen finden Sie unter [Verwenden des Berichtnachrichten-Add-ins](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span><span class="sxs-lookup"><span data-stu-id="288ec-183">See [Use the Report Message add-in](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2).</span></span>

## <a name="review-or-edit-settings-for-the-report-message-add-in"></a><span data-ttu-id="288ec-184">Überarbeiten oder Bearbeiten von Einstellungen für das Berichtnachrichten-Add-in</span><span class="sxs-lookup"><span data-stu-id="288ec-184">Review or edit settings for the Report Message add-in</span></span>

<span data-ttu-id="288ec-185">Sie können die Standardeinstellungen für das Berichtnachrichten-Add-in auf der [Seite &-Add-Ins für Dienste](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns)überarbeiten und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="288ec-185">You can review and edit the default settings for the Report Message add-in on the [Services & Add-Ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="288ec-186">Sie müssen ein globaler Office 365-Administrator oder ein Exchange Online-Administrator sein, um diese Aufgabe ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="288ec-186">You must be an Office 365 global administrator or an Exchange Online Administrator to complete this task.</span></span>
    
1. <span data-ttu-id="288ec-187">Wechseln Sie zur [Seite &-Add-Ins für Dienste](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) im Microsoft 365 Admin Center.</span><span class="sxs-lookup"><span data-stu-id="288ec-187">Go to the [Services & add-ins page](https://admin.microsoft.com/AdminPortal/Home#/Settings/ServicesAndAddIns) in the Microsoft 365 admin center.</span></span><br/><span data-ttu-id="288ec-188">![Seite "Dienste und Add-Ins" im neuen Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span><span class="sxs-lookup"><span data-stu-id="288ec-188">![Services and Add-Ins page in the new Microsoft 365 Admin Center](media/ServicesAddInsPageNewM365AdminCenter.png)</span></span><br/>

2. <span data-ttu-id="288ec-189">Suchen und wählen Sie das Add-in Berichtnachricht aus.</span><span class="sxs-lookup"><span data-stu-id="288ec-189">Find and select the Report Message add-in.</span></span><br/>![Suchen und auswählen des Add-Ins "Berichtnachricht"](media/FindReportMessageAddIn.png)<br/> 
    
3. <span data-ttu-id="288ec-191">Überprüfung und Bearbeitung der Einstellungen für Ihre Organisation auf dem Bildschirm Bericht Meldung.</span><span class="sxs-lookup"><span data-stu-id="288ec-191">On the Report Message screen, review and edit settings as appropriate for your organization.</span></span><br/>![Einstellungen für das Berichtnachrichten-Add-in](media/EditReportMessageAddIn.png)<br/> 
  
## <a name="related-topics"></a><span data-ttu-id="288ec-193">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="288ec-193">Related topics</span></span>

[<span data-ttu-id="288ec-194">Verwenden des Add-Ins Nachricht melden</span><span class="sxs-lookup"><span data-stu-id="288ec-194">Use the Report Message add-in</span></span>](https://support.office.com/article/b5caa9f1-cdf3-4443-af8c-ff724ea719d2)
  
[<span data-ttu-id="288ec-195">Anzeigen von e-Mail-Sicherheits &amp; Berichten im Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="288ec-195">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)

[<span data-ttu-id="288ec-196">Anzeigen von Berichten für Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="288ec-196">View reports for Office 365 Advanced Threat Protection</span></span>](view-reports-for-atp.md)

[<span data-ttu-id="288ec-197">Verwenden des Explorers im Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="288ec-197">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
  

