---
title: Verwalten von OAuth-Apps mit Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: OAuth-apps in Office 365-Cloud-App-Sicherheit können Sie apps verwalten, die Ihre Benutzer für die Verwendung mit Office 365 Daten herunterladen
ms.openlocfilehash: ae32e3c6b15f4ad4794a3dd08c3992adaeba655c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603686"
---
# <a name="manage-oauth-apps-using-office-365-cloud-app-security"></a><span data-ttu-id="148a9-103">Verwalten von OAuth-Apps mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="148a9-103">Manage OAuth apps using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="148a9-104">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="148a9-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="148a9-105">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="148a9-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="148a9-106">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="148a9-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="148a9-107">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="148a9-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="148a9-108">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="148a9-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="148a9-109">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="148a9-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="148a9-110">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="148a9-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="148a9-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="148a9-111">You are here!</span></span>  <br/> [<span data-ttu-id="148a9-112">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="148a9-112">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="148a9-p101">Erfolgreicher apps und sie diese häufig herunterladen, insbesondere apps, die für die Personensuche Reaktionszeiten werden sparen Sie Zeit, die an die geschäftliche abzurufen oder Schule Informationen zu erleichtern. Jedoch einige apps können ein Sicherheitsrisiko für Ihre Organisation potenziell handeln, je nachdem, welche Informationen sie zugreifen und wie diese Informationen verarbeiten. Mit [Office 365-Cloud-App-Sicherheit](office-365-cas-overview.md)Wenn Sie einen Administrator global oder Sicherheit sind können Sie OAuth-apps für Ihre Organisation verwalten. Sie können sehen, die apps Personen verwenden welche Berechtigungen mit Office 365-Daten, die apps haben, und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="148a9-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage OAuth apps for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="148a9-117">In diesem Artikel wird beschrieben, wo Sie OAuth apps verwalten, wie genehmigen, Sperren oder melden einer app und wie Sie eine app-Abfrage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="148a9-117">This article describes where to go to manage OAuth apps, how to approve, ban, or report an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-oauth-apps-page"></a><span data-ttu-id="148a9-118">So finden Sie die OAuth verwalten apps-Seite</span><span class="sxs-lookup"><span data-stu-id="148a9-118">How to find the Manage OAuth apps page</span></span>

> [!NOTE]
> <span data-ttu-id="148a9-p102">OAuth-apps werden in der Cloud App Sicherheit in Office 365-Portal verwaltet. Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der folgenden Aufgabe sein. Um weitere finden Sie unter informieren [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="148a9-p102">OAuth apps are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="148a9-122">Klicken Sie auf das Portal Cloud App-Sicherheit ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) und zur Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="148a9-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="148a9-123">Wählen Sie **untersuchen** \> **OAuth-apps**.</span><span class="sxs-lookup"><span data-stu-id="148a9-123">Choose **Investigate** \> **OAuth apps**.</span></span><br/><span data-ttu-id="148a9-124">![Wählen Sie im Portal O365 CAS überprüfen.](media/OCAS-OAuthApps.png)</span><span class="sxs-lookup"><span data-stu-id="148a9-124">![In the O365 CAS portal, choose Investigate.](media/OCAS-OAuthApps.png)</span></span><br/>
  
## <a name="what-youll-see-on-the-manage-oauth-apps-page"></a><span data-ttu-id="148a9-125">Was sehen Sie auf der Seite verwalten OAuth-apps</span><span class="sxs-lookup"><span data-stu-id="148a9-125">What you'll see on the Manage OAuth apps page</span></span>

<span data-ttu-id="148a9-126">In der folgenden Tabelle werden die Steuerelemente und die verfügbaren Optionen auf der Seite verwalten OAuth apps beschrieben.</span><span class="sxs-lookup"><span data-stu-id="148a9-126">The following table describes the controls and options available on the Manage OAuth apps page.</span></span>
  
|<span data-ttu-id="148a9-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="148a9-127">**Item**</span></span>|<span data-ttu-id="148a9-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="148a9-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="148a9-129">Grundlegende Symbol in der app-Leiste Abfrage</span><span class="sxs-lookup"><span data-stu-id="148a9-129">Basic icon in the app query bar</span></span>  <br/> ![Symbol, grundlegende Abfrageansicht für die Abfrage angibt.](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="148a9-131">Wählen Sie diese Option, um die erweiterte Ansicht wechseln.</span><span class="sxs-lookup"><span data-stu-id="148a9-131">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="148a9-132">(Wenn Sie **grundlegende**angezeigt wird, die erweiterte Ansicht verwenden Sie)</span><span class="sxs-lookup"><span data-stu-id="148a9-132">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="148a9-133">Erweiterte Symbol in der app-Leiste Abfrage</span><span class="sxs-lookup"><span data-stu-id="148a9-133">Advanced icon in the app query bar</span></span>  <br/> ![Symbol, erweiterte Abfrageansicht für die Abfrage angibt.](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="148a9-135">Wählen Sie diese Option, um die grundlegende Ansicht wechseln.</span><span class="sxs-lookup"><span data-stu-id="148a9-135">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="148a9-136">(Wenn Sie **Erweitert**angezeigt wird, werden Sie die grundlegende Ansicht verwenden.)</span><span class="sxs-lookup"><span data-stu-id="148a9-136">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="148a9-137">Öffnen Sie oder schließen Sie alle Detailsymbol in der app-Liste</span><span class="sxs-lookup"><span data-stu-id="148a9-137">Open or close all details icon in the app list</span></span>  <br/> ![Klicken Sie auf dieses Symbol, um das Öffnen oder schließen Sie alle Details für alle apps](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="148a9-139">Wählen Sie dieses Symbol, um mehr oder weniger Details zu einzelnen app anzeigen.</span><span class="sxs-lookup"><span data-stu-id="148a9-139">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="148a9-140">Exportsymbol in der app-Liste</span><span class="sxs-lookup"><span data-stu-id="148a9-140">Export icon in the app list</span></span>  <br/> ![Klicken Sie auf dieses Symbol, um alle Apps eine Csv-Datei exportieren](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="148a9-142">Wählen Sie dieses Symbol, um eine CSV-Datei zu exportieren, die eine Liste von apps, die Anzahl von Benutzern für die jeweilige app die app, Berechtigungsstufe, app-Status und Community Verwendung Ebene zugeordneten Berechtigungen enthält.</span><span class="sxs-lookup"><span data-stu-id="148a9-142">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="148a9-143">Name</span><span class="sxs-lookup"><span data-stu-id="148a9-143">Name</span></span>  <br/> |<span data-ttu-id="148a9-p103">Verwenden Sie diese auf den Namen der eine App auswählen finden Sie unter dem Namen zum Anzeigen von Informationen, Beschreibung, Publisher, app-Website und app-ID.</span><span class="sxs-lookup"><span data-stu-id="148a9-p103">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="148a9-146">Autorisiert durch</span><span class="sxs-lookup"><span data-stu-id="148a9-146">Authorized by</span></span>  <br/> |<span data-ttu-id="148a9-p104">Verwenden Sie diese Option, um anzuzeigen, wie viele Benutzer Zugriff auf ihre Office 365-Konto eine app autorisiert haben. Wählen Sie die Nummer, um weitere Informationen, wie eine Liste der Benutzerkonten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="148a9-p104">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="148a9-149">Berechtigungsstufe</span><span class="sxs-lookup"><span data-stu-id="148a9-149">Permissions Level</span></span>  <br/> ![Symbol, das die Permisiions Ebene für eine app angibt](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="148a9-p105">Verwenden Sie diese Option, um anzuzeigen, wie viel eine app auf Office 365-Daten zugreifen können. Berechtigungsstufen angeben, **Niedrig**, **Mittel**oder **Hoch**, wobei **Niedrig** hinweisen können, dass die app nur Profile und den Namen des Benutzers zugreift. Wählen Sie die Ebene, um weitere Informationen, wie Berechtigungen erteilt der app, Community-Verwendung und verwandte Aktivität im [Governance Protokoll](suspend-or-restore-an-account-in-ocas.md)anzeigen.</span><span class="sxs-lookup"><span data-stu-id="148a9-p105">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="148a9-154">Zuletzt autorisiert</span><span class="sxs-lookup"><span data-stu-id="148a9-154">Last authorized</span></span> <br/> |<span data-ttu-id="148a9-155">Verwenden Sie diese Option, um finden Sie unter Datum und Uhrzeit, eine app OAuth letzten Zugriff auf Ihre Organisation Office 365-Daten autorisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="148a9-155">Use this to see the date and time an OAuth app was last authorized to access your organization's Office 365 data.</span></span> <br/>  |
|<span data-ttu-id="148a9-156">Aktionen</span><span class="sxs-lookup"><span data-stu-id="148a9-156">Actions</span></span><br/>![OAuth-apps](media/OCAS-OAuthAppApproveBanReport.png)<br/> |<span data-ttu-id="148a9-158">Verwenden Sie diese finden Sie unter oder um eine app als genehmigt oder gesperrten, markieren eine OAuth-app an Microsoft melden, oder lassen sie als unbestimmten.</span><span class="sxs-lookup"><span data-stu-id="148a9-158">Use this to see or to mark an app as Approved or Banned, report an OAuth app to Microsoft, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="148a9-159">Markieren Sie eine app genehmigt hat</span><span class="sxs-lookup"><span data-stu-id="148a9-159">Mark an app as approved</span></span>

<span data-ttu-id="148a9-160">Klicken Sie auf der Seite **Verwalten OAuth-apps** suchen Sie die app aus, den, die Sie genehmigen möchten, und wählen Sie das Symbol **Mark app als genehmigt** .</span><span class="sxs-lookup"><span data-stu-id="148a9-160">On the **Manage OAuth apps** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Wählen Sie die app Mark als genehmigte Symbol](media/OCAS-MarkOAuthApproved.png)
  
<span data-ttu-id="148a9-162">Das Symbol wird grün und die app für alle Ihre Office 365-Benutzer freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="148a9-162">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="148a9-p106">Wenn Sie eine app genehmigt markieren, ist es keine Auswirkung auf die Endbenutzer. Visuell Markieren von apps, die genehmigt wurden hilft bei der um sie von apps zu trennen, die noch überarbeitet wurden noch nicht bei.</span><span class="sxs-lookup"><span data-stu-id="148a9-p106">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="148a9-165">Sperren einer app</span><span class="sxs-lookup"><span data-stu-id="148a9-165">Ban an app</span></span>

1. <span data-ttu-id="148a9-166">Suchen Sie auf der Seite **Verwalten OAuth-apps** die app aus, die Sie sperren möchten, und wählen Sie das Symbol **Mark app als gesperrte** .</span><span class="sxs-lookup"><span data-stu-id="148a9-166">On the **Manage OAuth apps** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span><br/><span data-ttu-id="148a9-167">![Wählen Sie die app Mark als gesperrte Symbol](media/OCAS-MarkOAuthBanned.png)</span><span class="sxs-lookup"><span data-stu-id="148a9-167">![Choose the Mark app as banned icon](media/OCAS-MarkOAuthBanned.png)</span></span>
  
2. <span data-ttu-id="148a9-p107">Klicken Sie im Meldungsfeld Benachrichtigung nicht vorhandenen Text geändert werden, oder passen Sie den Text. Wählen Sie, ob, damit Benutzer wissen, dass ihre app gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="148a9-p107">In the notification message box, keep the existing text as it is, or customize the text. Choose whether to let users know that their app has been banned.</span></span> <br/>![Die e-Mail-Vorlage für eine gesperrte-app](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)<br/>
  
3. <span data-ttu-id="148a9-171">Wählen Sie **app Sperren**.</span><span class="sxs-lookup"><span data-stu-id="148a9-171">Choose **Ban app**.</span></span>

## <a name="report-an-oauth-app-to-microsoft"></a><span data-ttu-id="148a9-172">Eine app OAuth an Microsoft melden</span><span class="sxs-lookup"><span data-stu-id="148a9-172">Report an OAuth app to Microsoft</span></span>

<span data-ttu-id="148a9-173">Wenn Sie eine OAuth-app für die Analyse an Microsoft übermitteln möchten, können Sie diese app melden.</span><span class="sxs-lookup"><span data-stu-id="148a9-173">If you want to submit an OAuth app to Microsoft for analysis, you can report that app.</span></span>

1. <span data-ttu-id="148a9-174">Suchen Sie auf der Seite **apps OAuth verwalten** die app aus, die Sie zur Analyse senden möchten.</span><span class="sxs-lookup"><span data-stu-id="148a9-174">On the **Manage OAuth apps** page, locate the app you want to submit for analysis.</span></span>

2. <span data-ttu-id="148a9-175">Wählen Sie die vertikale Ellipse und dann auf **Bericht App..**.</span><span class="sxs-lookup"><span data-stu-id="148a9-175">Choose the vertical ellipsis, and then choose **Report app...**.</span></span><br/><span data-ttu-id="148a9-176">![Melden einer OAuth-app](media/OCAS-MarkOAuthReported.png)</span><span class="sxs-lookup"><span data-stu-id="148a9-176">![Report an OAuth app](media/OCAS-MarkOAuthReported.png)</span></span><br/>

3. <span data-ttu-id="148a9-p108">Klicken Sie im Dialogfeld **Bericht diese app** verwenden Sie die Dropdown-Liste an, dass Ihr Problem. **Diese app wird böswilliger** ist standardmäßig ausgewählt. Sie können jedoch auf eine der verfügbaren Optionen.</span><span class="sxs-lookup"><span data-stu-id="148a9-p108">In the **Report this app** dialog box, use the drop-down list to indicate your concern. By default, **This app is malicious** is selected. However, you can choose on one of the other available options. </span></span><br/><span data-ttu-id="148a9-180">![Melden einer OAuth-app](media/OCAS-ReportOAuthApp.png)</span><span class="sxs-lookup"><span data-stu-id="148a9-180">![Report an OAuth app](media/OCAS-ReportOAuthApp.png)</span></span><br/>

4. <span data-ttu-id="148a9-181">(Empfohlen) Lassen Sie die Option zum ausgewählten Kontakt, und bestätigen (oder bearbeiten) die e-Mail-Adresse aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="148a9-181">(Recommended) Keep the option to contact you selected, and confirm (or edit) the email address listed.</span></span>

5. <span data-ttu-id="148a9-182">Wählen Sie **Übermitteln** aus.</span><span class="sxs-lookup"><span data-stu-id="148a9-182">Choose **Submit**.</span></span> 
    
## <a name="create-an-app-query"></a><span data-ttu-id="148a9-183">Erstellen Sie eine app-Abfrage</span><span class="sxs-lookup"><span data-stu-id="148a9-183">Create an app query</span></span>

<span data-ttu-id="148a9-184">Es wird empfohlen, mit der erweiterten Ansicht, der wie folgt aussieht:</span><span class="sxs-lookup"><span data-stu-id="148a9-184">We recommend using the Advanced view, which looks like this:</span></span> 

![Erweiterte Ansicht](media/OCAS-OAuthAppsAdvQueryView.png)

<span data-ttu-id="148a9-p109">In der app-Leiste Abfrage, wenn Sie **Erweitert**, sehen verwenden Sie die Basisansicht. **Erweitert** aus, um die erweiterte Ansicht wechseln klicken (oder tippen).</span><span class="sxs-lookup"><span data-stu-id="148a9-p109">In the app query bar, if you see **Advanced**, you're using the Basic view. Click (or tap) **Advanced** to go to the Advanced view.</span></span> 

![Basisansicht](media/OCAS-OAuthAppsBasicQueryView.png)
    
1. <span data-ttu-id="148a9-189">Verwenden Sie in der Adressleiste die Abfrage der Liste **Wählen Sie einen Filter** auf eine Option.</span><span class="sxs-lookup"><span data-stu-id="148a9-189">In the query bar, use the **Select a filter** list to choose an option.</span></span> 
    - <span data-ttu-id="148a9-190">**App** Apps mit bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="148a9-190">**App** Apps with certain names</span></span>
    - <span data-ttu-id="148a9-191">**App-Status** Apps basierend auf deren Status (genehmigt, gesperrten oder unbestimmt)</span><span class="sxs-lookup"><span data-stu-id="148a9-191">**App state** Apps based on their state (Approved, Banned, or Undetermined)</span></span>
    - <span data-ttu-id="148a9-192">**Verwenden der Community** Verwenden Sie Apps basierend auf Community Ebenen (seltene, Uncommon oder gemeinsamen)</span><span class="sxs-lookup"><span data-stu-id="148a9-192">**Community use** Apps based on community use levels (Rare, Uncommon, or Common)</span></span>
    - <span data-ttu-id="148a9-193">**Berechtigungsstufe** Apps basierend auf bestimmte Berechtigungsstufen</span><span class="sxs-lookup"><span data-stu-id="148a9-193">**Permission level** Apps based on certain permission levels</span></span> 
    - <span data-ttu-id="148a9-194">**Berechtigungen** Apps, die bestimmte Berechtigungen erfordern</span><span class="sxs-lookup"><span data-stu-id="148a9-194">**Permissions** Apps that require certain permissions</span></span>
    - <span data-ttu-id="148a9-195">**Publisher**  Apps, die von bestimmten Herausgebern</span><span class="sxs-lookup"><span data-stu-id="148a9-195">**Publisher**  Apps from certain publishers</span></span>
    - <span data-ttu-id="148a9-196">**Benutzer** Apps, die ein bestimmter Benutzer autorisiert</span><span class="sxs-lookup"><span data-stu-id="148a9-196">**User** Apps that a certain user authorized</span></span>
   
2. <span data-ttu-id="148a9-197">Wählen Sie **gleich** oder **ungleich**aus, und geben Sie einen Wert für den Filter.</span><span class="sxs-lookup"><span data-stu-id="148a9-197">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
3. <span data-ttu-id="148a9-198">Um weitere Filter hinzuzufügen, wählen Sie das Pluszeichen (+) (</span><span class="sxs-lookup"><span data-stu-id="148a9-198">To add more filters, select the plus sign (</span></span>![Fügen Sie ein Filter-Symbol für das Abfragen von apps](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="148a9-200">), und wiederholen Sie die Schritte 2 und 3.</span><span class="sxs-lookup"><span data-stu-id="148a9-200">), and then repeat steps 2 and 3.</span></span>
    
4. <span data-ttu-id="148a9-201">Wählen Sie zum Entfernen eines Filters aus der x (</span><span class="sxs-lookup"><span data-stu-id="148a9-201">To remove a filter, select the x (</span></span>![Entfernen Sie ein Filter-Symbol für das Abfragen von apps](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="148a9-203">) neben dem Namen eines Filters.</span><span class="sxs-lookup"><span data-stu-id="148a9-203">) next to a filter name.</span></span>
    
<span data-ttu-id="148a9-204">Die Filter werden automatisch angewendet, und die Liste apps wird entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="148a9-204">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="148a9-205">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="148a9-205">Next steps</span></span>

- [<span data-ttu-id="148a9-206">Lesen und Ausführen einer Aktion Warnungen</span><span class="sxs-lookup"><span data-stu-id="148a9-206">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="148a9-207">Überprüfen Sie Ihre [Web-Datenverkehr Protokolle und Datenquellen für Office 365-Cloud-App-Sicherheit](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="148a9-207">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="148a9-208">Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="148a9-208">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

