---
title: Verwalten von OAuth-Apps mit Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: OAuth apps in Office 365 Cloud-App-Sicherheit helfen Ihnen, die apps zu verwalten, die Ihre Benutzer für die Verwendung mit Office 365-Daten herunterladen
ms.openlocfilehash: 510cb64f2267c99b783f86a69f7b7a84db8d84dd
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219825"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a><span data-ttu-id="56dcf-103">Verwalten von OAuth-Apps mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="56dcf-103">Manage OAuth apps using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="56dcf-104">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="56dcf-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="56dcf-105">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="56dcf-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="56dcf-106">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="56dcf-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="56dcf-107">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="56dcf-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="56dcf-108">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="56dcf-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="56dcf-109">Planung starten</span><span class="sxs-lookup"><span data-stu-id="56dcf-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="56dcf-110">Starten der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="56dcf-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="56dcf-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="56dcf-111">You are here!</span></span>  <br/> [<span data-ttu-id="56dcf-112">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="56dcf-112">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="56dcf-p101">People Love apps und Sie laden Sie oft, insbesondere apps, die Leute denken, wird Zeit sparen, indem Sie es einfacher, ihre Arbeit oder Schulinformationen zu erhalten. Einige apps können jedoch möglicherweise ein Sicherheitsrisiko für Ihre Organisation darstellen, je nachdem, auf welche Informationen Sie zugreifen und wie diese Informationen verarbeitet werden. Mit [Office 365 Cloud App Security](office-365-cas-overview.md), wenn Sie ein globaler oder Sicherheitsadministrator sind, können Sie OAuth-Apps für Ihre Organisation verwalten. Sie können sehen, welche apps Benutzer mit Office 365-Daten verwenden, welche Berechtigungen diese apps haben und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="56dcf-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage OAuth apps for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="56dcf-117">In diesem Artikel wird beschrieben, wo Sie OAuth-apps verwalten, wie Sie eine APP genehmigen, verbieten oder melden und wie Sie eine APP-Abfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="56dcf-117">This article describes where to go to manage OAuth apps, how to approve, ban, or report an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a><span data-ttu-id="56dcf-118">So finden Sie die Seite "Verwalten von OAuth-Apps"</span><span class="sxs-lookup"><span data-stu-id="56dcf-118">How to find the Manage OAuth apps page</span></span>

> [!NOTE]
> <span data-ttu-id="56dcf-p102">OAuth-apps werden im Sicherheitsportal der Office 365 Cloud App verwaltet. Sie müssen ein globaler Administrator oder Sicherheitsadministrator sein, um die folgende Aufgabe ausführen zu können. Weitere Informationen finden Sie unter [Permissions in the Office &amp; 365 Security Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="56dcf-p102">OAuth apps are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="56dcf-122">Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="56dcf-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="56dcf-123">Wählen Sie **OAuth-apps** **untersuchen** \> aus.</span><span class="sxs-lookup"><span data-stu-id="56dcf-123">Choose **Investigate** \> **OAuth apps**.</span></span><br/><span data-ttu-id="56dcf-124">![Wählen Sie im O365-CAS-Portal untersuchen aus.](media/OCAS-OAuthApps.png)</span><span class="sxs-lookup"><span data-stu-id="56dcf-124">![In the O365 CAS portal, choose Investigate.](media/OCAS-OAuthApps.png)</span></span><br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a><span data-ttu-id="56dcf-125">Was Sie auf der Seite "Verwalten von OAuth-Apps" sehen</span><span class="sxs-lookup"><span data-stu-id="56dcf-125">What you'll see on the Manage OAuth apps page</span></span>

<span data-ttu-id="56dcf-126">In der folgenden Tabelle werden die Steuerelemente und Optionen beschrieben, die auf der Seite OAuth-apps verwalten zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="56dcf-126">The following table describes the controls and options available on the Manage OAuth apps page.</span></span>
  
|<span data-ttu-id="56dcf-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="56dcf-127">**Item**</span></span>|<span data-ttu-id="56dcf-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="56dcf-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56dcf-129">Basis Symbol in der APP-Abfrage Leiste</span><span class="sxs-lookup"><span data-stu-id="56dcf-129">Basic icon in the app query bar</span></span>  <br/> ![Symbol für einfache Abfrageansicht für Abfragen](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="56dcf-131">Wählen Sie diese Option aus, um zur erweiterten Ansicht zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="56dcf-131">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="56dcf-132">(Wenn Sie " **Basic**" sehen, verwenden Sie die erweiterte Ansicht)</span><span class="sxs-lookup"><span data-stu-id="56dcf-132">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="56dcf-133">Symbol "Erweitert" in der APP-Abfrage Leiste</span><span class="sxs-lookup"><span data-stu-id="56dcf-133">Advanced icon in the app query bar</span></span>  <br/> ![Symbol, das die erweiterte Abfrageansicht für Abfragen angibt](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="56dcf-135">Wählen Sie diese Option aus, um zur Standardansicht zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="56dcf-135">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="56dcf-136">(Wenn Sie " **erweitert**" sehen, verwenden Sie die Standardansicht.)</span><span class="sxs-lookup"><span data-stu-id="56dcf-136">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="56dcf-137">Öffnen oder Schließen aller Details-Symbol in der APP-Liste</span><span class="sxs-lookup"><span data-stu-id="56dcf-137">Open or close all details icon in the app list</span></span>  <br/> ![Klicken Sie auf dieses Symbol, um alle Details für alle apps zu öffnen oder zu schließen.](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="56dcf-139">Wählen Sie dieses Symbol aus, um mehr oder weniger Details zu den einzelnen apps anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="56dcf-139">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="56dcf-140">Export Symbol in der APP-Liste</span><span class="sxs-lookup"><span data-stu-id="56dcf-140">Export icon in the app list</span></span>  <br/> ![Klicken Sie auf dieses Symbol, um eine CSV-Datei aller apps zu exportieren.](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="56dcf-142">Wählen Sie dieses Symbol aus, um eine CSV-Datei zu exportieren, die eine Liste der apps, die Anzahl der Benutzer für jede APP, Berechtigungen für die APP, Berechtigungsstufe, App-Status und Community-Nutzungs Ebene enthält.</span><span class="sxs-lookup"><span data-stu-id="56dcf-142">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="56dcf-143">Name</span><span class="sxs-lookup"><span data-stu-id="56dcf-143">Name</span></span>  <br/> |<span data-ttu-id="56dcf-p103">Verwenden Sie diese Option, um den Namen einer APP anzuzeigen. Wählen Sie den Namen aus, um weitere Informationen anzuzeigen, beispielsweise die Beschreibung, den Herausgeber, die APP-Website und die APP-ID.</span><span class="sxs-lookup"><span data-stu-id="56dcf-p103">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="56dcf-146">Autorisiert von</span><span class="sxs-lookup"><span data-stu-id="56dcf-146">Authorized by</span></span>  <br/> |<span data-ttu-id="56dcf-p104">Verwenden Sie diese Informationen, um zu sehen, wie viele Benutzer eine APP autorisiert haben, auf Ihr Office 365-Konto zuzugreifen. Wählen Sie die Nummer aus, um weitere Informationen anzuzeigen, beispielsweise eine Liste von Benutzerkonten.</span><span class="sxs-lookup"><span data-stu-id="56dcf-p104">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="56dcf-149">Berechtigungsstufe</span><span class="sxs-lookup"><span data-stu-id="56dcf-149">Permissions Level</span></span>  <br/> ![Symbol, das die permisiions-Ebene für eine APP angibt](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="56dcf-p105">Verwenden Sie diese, um zu sehen, wie viel Zugriff eine APP auf Office 365-Daten hat. Berechtigungsstufen deuten auf **niedrig**, **Mittel**oder **hoch**hin, wobei **Low** darauf hindeuten kann, dass die app nur auf das Profil und den Namen eines Benutzers zugreift. Wählen Sie die Ebene aus, um weitere Informationen anzuzeigen, beispielsweise Berechtigungen, die der APP erteilt wurden, die Community-Nutzung und die zugehörigen Aktivitäten im [Steuerungsprotokoll](suspend-or-restore-an-account-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="56dcf-p105">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="56dcf-154">Zuletzt autorisiert</span><span class="sxs-lookup"><span data-stu-id="56dcf-154">Last authorized</span></span> <br/> |<span data-ttu-id="56dcf-155">Verwenden Sie diese, um das Datum und die Uhrzeit anzuzeigen, zu der eine OAuth-App zuletzt autorisiert wurde, um auf die Office 365-Daten Ihrer Organisation zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="56dcf-155">Use this to see the date and time an OAuth app was last authorized to access your organization's Office 365 data.</span></span> <br/>  |
|<span data-ttu-id="56dcf-156">Aktionen</span><span class="sxs-lookup"><span data-stu-id="56dcf-156">Actions</span></span><br/>![OAuth-apps](media/OCAS-OAuthAppApproveBanReport.png)<br/> |<span data-ttu-id="56dcf-158">Verwenden Sie diese Funktion, um eine App als genehmigt oder gesperrt zu markieren, eine OAuth-APP an Microsoft zu melden oder Sie als unbestimmt zu belassen.</span><span class="sxs-lookup"><span data-stu-id="56dcf-158">Use this to see or to mark an app as Approved or Banned, report an OAuth app to Microsoft, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="56dcf-159">Kennzeichnen einer App als genehmigt</span><span class="sxs-lookup"><span data-stu-id="56dcf-159">Mark an app as approved</span></span>

<span data-ttu-id="56dcf-160">Suchen Sie auf der Seite **OAuth-apps verwalten** die APP, die Sie genehmigen möchten, und klicken Sie auf das Symbol **App als genehmigt markieren** .</span><span class="sxs-lookup"><span data-stu-id="56dcf-160">On the **Manage OAuth apps** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Auswählen des Symbols "App als genehmigt"](media/OCAS-MarkOAuthApproved.png)
  
<span data-ttu-id="56dcf-162">Das Symbol wird grün, und die APP wird für alle Office 365-Benutzer genehmigt.</span><span class="sxs-lookup"><span data-stu-id="56dcf-162">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="56dcf-p106">Wenn Sie eine App als genehmigt markieren, hat dies keinen Einfluss auf den Endbenutzer. Wenn Sie die genehmigten apps visuell markieren, können Sie diese von apps trennen, die noch nicht überprüft wurden.</span><span class="sxs-lookup"><span data-stu-id="56dcf-p106">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="56dcf-165">Sperren einer APP</span><span class="sxs-lookup"><span data-stu-id="56dcf-165">Ban an app</span></span>

1. <span data-ttu-id="56dcf-166">Suchen Sie auf der Seite **OAuth-apps verwalten** die APP, die Sie verbieten möchten, und klicken Sie auf das Symbol **App als gesperrt markieren** .</span><span class="sxs-lookup"><span data-stu-id="56dcf-166">On the **Manage OAuth apps** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span><br/><span data-ttu-id="56dcf-167">![Auswählen des Symbols app AS Banned](media/OCAS-MarkOAuthBanned.png)</span><span class="sxs-lookup"><span data-stu-id="56dcf-167">![Choose the Mark app as banned icon](media/OCAS-MarkOAuthBanned.png)</span></span>
  
2. <span data-ttu-id="56dcf-p107">Behalten Sie im Feld Benachrichtigungsmeldung den vorhandenen Text bei, oder passen Sie den Text an. Legen Sie fest, ob die Benutzer wissen möchten, dass Ihre APP gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="56dcf-p107">In the notification message box, keep the existing text as it is, or customize the text. Choose whether to let users know that their app has been banned.</span></span> <br/>![Die e-Mail-Vorlage für eine gesperrte App](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. <span data-ttu-id="56dcf-171">Wählen Sie **Ban-App**aus.</span><span class="sxs-lookup"><span data-stu-id="56dcf-171">Choose **Ban app**.</span></span>

## <a name="report-an-oauth-app-to-microsoft"></a><span data-ttu-id="56dcf-172">Melden einer OAuth-APP an Microsoft</span><span class="sxs-lookup"><span data-stu-id="56dcf-172">Report an OAuth app to Microsoft</span></span>

<span data-ttu-id="56dcf-173">Wenn Sie eine OAuth-App zur Analyse an Microsoft übermitteln möchten, können Sie diese APP melden.</span><span class="sxs-lookup"><span data-stu-id="56dcf-173">If you want to submit an OAuth app to Microsoft for analysis, you can report that app.</span></span>

1. <span data-ttu-id="56dcf-174">Suchen Sie auf der Seite **OAuth-apps verwalten** die APP, die Sie zur Analyse übermitteln möchten.</span><span class="sxs-lookup"><span data-stu-id="56dcf-174">On the **Manage OAuth apps** page, locate the app you want to submit for analysis.</span></span>

2. <span data-ttu-id="56dcf-175">Wählen Sie die vertikalen Auslassungspunkte aus, und wählen Sie dann **Bericht-app...**.</span><span class="sxs-lookup"><span data-stu-id="56dcf-175">Choose the vertical ellipsis, and then choose **Report app...**.</span></span><br/><span data-ttu-id="56dcf-176">![Melden einer OAuth-App](media/OCAS-MarkOAuthReported.png)</span><span class="sxs-lookup"><span data-stu-id="56dcf-176">![Report an OAuth app](media/OCAS-MarkOAuthReported.png)</span></span><br/>

3. <span data-ttu-id="56dcf-p108">Geben Sie im Dialogfeld **diese APP melden** in der Dropdownliste ihre Bedenken an. Standardmäßig ist **diese APP bösartig** ausgewählt. Sie können jedoch eine der anderen verfügbaren Optionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="56dcf-p108">In the **Report this app** dialog box, use the drop-down list to indicate your concern. By default, **This app is malicious** is selected. However, you can choose on one of the other available options. </span></span><br/><span data-ttu-id="56dcf-180">![Melden einer OAuth-App](media/OCAS-ReportOAuthApp.png)</span><span class="sxs-lookup"><span data-stu-id="56dcf-180">![Report an OAuth app](media/OCAS-ReportOAuthApp.png)</span></span><br/>

4. <span data-ttu-id="56dcf-181">Empfohlen Halten Sie die Option, Kontakt mit Ihnen ausgewählt, und bestätigen (oder bearbeiten) Sie die e-Mail-Adresse aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="56dcf-181">(Recommended) Keep the option to contact you selected, and confirm (or edit) the email address listed.</span></span>

5. <span data-ttu-id="56dcf-182">Wählen Sie **Übermitteln** aus.</span><span class="sxs-lookup"><span data-stu-id="56dcf-182">Choose **Submit**.</span></span> 
    
## <a name="create-an-app-query"></a><span data-ttu-id="56dcf-183">Erstellen einer APP-Abfrage</span><span class="sxs-lookup"><span data-stu-id="56dcf-183">Create an app query</span></span>

<span data-ttu-id="56dcf-184">Es wird empfohlen, die erweiterte Ansicht zu verwenden, die wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="56dcf-184">We recommend using the Advanced view, which looks like this:</span></span> 

![Erweiterte Ansicht](media/OCAS-OAuthAppsAdvQueryView.png)

<span data-ttu-id="56dcf-p109">Wenn Sie in der APP-Abfrage Leiste auf **erweitert**sehen, verwenden Sie die Standardansicht. Klicken (oder tippen) Sie auf **erweitert** , um zur erweiterten Ansicht zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="56dcf-p109">In the app query bar, if you see **Advanced**, you're using the Basic view. Click (or tap) **Advanced** to go to the Advanced view.</span></span> 

![Einfache Ansicht](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. <span data-ttu-id="56dcf-189">Verwenden Sie in der Abfrage Leiste die Liste **Filter auswählen** , um eine Option auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="56dcf-189">In the query bar, use the **Select a filter** list to choose an option.</span></span> 
    - <span data-ttu-id="56dcf-190">**App** Apps mit bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="56dcf-190">**App** Apps with certain names</span></span>
    - <span data-ttu-id="56dcf-191">**App-Status** Apps basierend auf Ihrem Status (genehmigt, gesperrt oder nicht festgelegt)</span><span class="sxs-lookup"><span data-stu-id="56dcf-191">**App state** Apps based on their state (Approved, Banned, or Undetermined)</span></span>
    - <span data-ttu-id="56dcf-192">**Community-Verwendung** Apps, die auf Community-Nutzungs Ebenen basieren (seltene, ungewöhnliche oder häufige)</span><span class="sxs-lookup"><span data-stu-id="56dcf-192">**Community use** Apps based on community use levels (Rare, Uncommon, or Common)</span></span>
    - <span data-ttu-id="56dcf-193">**Berechtigungsstufe** Apps basierend auf bestimmten Berechtigungsstufen</span><span class="sxs-lookup"><span data-stu-id="56dcf-193">**Permission level** Apps based on certain permission levels</span></span> 
    - <span data-ttu-id="56dcf-194">**Berechtigungen** Apps, die bestimmte Berechtigungen erfordern</span><span class="sxs-lookup"><span data-stu-id="56dcf-194">**Permissions** Apps that require certain permissions</span></span>
    - <span data-ttu-id="56dcf-195">**Herausgeber**  Apps von bestimmten Herausgebern</span><span class="sxs-lookup"><span data-stu-id="56dcf-195">**Publisher**  Apps from certain publishers</span></span>
    - <span data-ttu-id="56dcf-196">**Benutzer** Apps, die ein bestimmter Benutzer autorisiert hat</span><span class="sxs-lookup"><span data-stu-id="56dcf-196">**User** Apps that a certain user authorized</span></span>
   
2. <span data-ttu-id="56dcf-197">Wählen Sie **gleich** oder **nicht gleich**aus, und geben Sie dann einen Wert für Ihren Filter an.</span><span class="sxs-lookup"><span data-stu-id="56dcf-197">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
3. <span data-ttu-id="56dcf-198">Um weitere Filter hinzuzufügen, wählen Sie das Pluszeichen (</span><span class="sxs-lookup"><span data-stu-id="56dcf-198">To add more filters, select the plus sign (</span></span>![Hinzufügen eines Filter Symbols für die Abfrage von apps](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="56dcf-200">), und wiederholen Sie die Schritte 2 und 3.</span><span class="sxs-lookup"><span data-stu-id="56dcf-200">), and then repeat steps 2 and 3.</span></span>
    
4. <span data-ttu-id="56dcf-201">Wenn Sie einen Filter entfernen möchten, wählen Sie das x (</span><span class="sxs-lookup"><span data-stu-id="56dcf-201">To remove a filter, select the x (</span></span>![Entfernen eines Filter Symbols für die Abfrage von apps](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="56dcf-203">) neben einem Filternamen.</span><span class="sxs-lookup"><span data-stu-id="56dcf-203">) next to a filter name.</span></span>
    
<span data-ttu-id="56dcf-204">Die Filter werden automatisch angewendet, und die apps-Liste wird entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="56dcf-204">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="56dcf-205">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="56dcf-205">Next steps</span></span>

- [<span data-ttu-id="56dcf-206">Überarbeiten und Aktionen für Warnungen</span><span class="sxs-lookup"><span data-stu-id="56dcf-206">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="56dcf-207">Über [Wachen von Webprotokollen und Datenquellen für Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="56dcf-207">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="56dcf-208">Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="56dcf-208">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

