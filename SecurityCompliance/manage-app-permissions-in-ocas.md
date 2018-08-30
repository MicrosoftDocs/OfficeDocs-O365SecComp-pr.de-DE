---
title: Verwalten von app-Berechtigungen, die mit Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/22/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 2062c312-b1e4-4ce7-8cb2-ea39bc0dfdad
description: App-Berechtigungen in Office 365-Cloud-App-Sicherheit können Sie apps verwalten, die Ihre Benutzer für die Verwendung mit Office 365 Daten herunterladen
ms.openlocfilehash: 7bda35bbbf3a16cd1d386adcb03b1c7c4176913a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529842"
---
# <a name="manage-app-permissions-using-office-365-cloud-app-security"></a><span data-ttu-id="d805e-103">Verwalten von app-Berechtigungen, die mit Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d805e-103">Manage app permissions using Office 365 Cloud App Security</span></span>

<span data-ttu-id="d805e-104">Office 365 Advanced Security Management ist jetzt Office 365-Cloud-App-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="d805e-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="d805e-105">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="d805e-105">****Evaluation** \>**</span></span>|<span data-ttu-id="d805e-106">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="d805e-106">****Planning** \>**</span></span>|<span data-ttu-id="d805e-107">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="d805e-107">****Deployment** \>**</span></span>|<span data-ttu-id="d805e-108">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="d805e-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="d805e-109">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="d805e-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="d805e-110">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="d805e-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="d805e-111">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="d805e-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="d805e-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="d805e-112">You are here!</span></span>  <br/> [<span data-ttu-id="d805e-113">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d805e-113">Next steps</span></span>](manage-app-permissions-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="d805e-p101">Erfolgreicher apps und sie diese häufig herunterladen, insbesondere apps, die für die Personensuche Reaktionszeiten werden sparen Sie Zeit, die an die geschäftliche abzurufen oder Schule Informationen zu erleichtern. Jedoch einige apps können ein Sicherheitsrisiko für Ihre Organisation potenziell handeln, je nachdem, welche Informationen sie zugreifen und wie diese Informationen verarbeiten. Mit [Office 365-Cloud-App-Sicherheit](office-365-cas-overview.md)Wenn Sie einen Administrator global oder Sicherheit sind können Sie app-Berechtigungen für Ihre Organisation verwalten. Sie können sehen, die apps Personen verwenden welche Berechtigungen mit Office 365-Daten, die apps haben, und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="d805e-p101">People love apps and they download them often, especially apps that people think will save time by making it easier to get at their work or school information. However, some apps could potentially be a security risk to your organization, depending on what information they access and how they handle that information. With [Office 365 Cloud App Security](office-365-cas-overview.md), if you are a global or security administrator, you can manage app permissions for your organization. You can see the apps people are using with Office 365 data, what permissions those apps have, and more.</span></span> 
  
<span data-ttu-id="d805e-118">In diesem Artikel wird beschrieben, wo Sie zum Verwalten von app-Berechtigungen, zum Genehmigen oder Sperren einer app und wie Sie eine app-Abfrage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d805e-118">This article describes where to go to manage app permissions, how to approve or ban an app, and how to create an app query.</span></span>
  
## <a name="how-to-find-the-manage-app-permissions-page"></a><span data-ttu-id="d805e-119">So finden Sie die Seite Berechtigungen app verwalten</span><span class="sxs-lookup"><span data-stu-id="d805e-119">How to find the Manage app permissions page</span></span>
<span data-ttu-id="d805e-120"><a name="findappperms"> </a></span><span class="sxs-lookup"><span data-stu-id="d805e-120"></span></span>

> [!NOTE]
> <span data-ttu-id="d805e-p102">App-Berechtigungen werden in der Cloud App Sicherheit in Office 365-Portal verwaltet. Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der folgenden Aufgabe sein. Um weitere finden Sie unter informieren [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d805e-p102">App permissions are managed in the Office 365 Cloud App Security portal. You must be a global administrator or security administrator to perform the following task. To learn more see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
1. <span data-ttu-id="d805e-p103">Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.)</span><span class="sxs-lookup"><span data-stu-id="d805e-p103">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="d805e-126">Wechseln Sie zu **Benachrichtigungen** \> **Verwalten erweiterte Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="d805e-126">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="d805e-127">Klicken (oder tippen) **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="d805e-127">Click (or tap) **Go to Office 365 Cloud App Security**.</span></span>
    
    ![In das Wertpapier &amp; Compliance Center, wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
    > [!NOTE]
    > <span data-ttu-id="d805e-p104">Wenn Office 365-Cloud-App-Sicherheit noch nicht aktiviert ist, können Sie das auf dieser Seite tun. Finden Sie unter [machen Sie sich bereit für Office 365-Cloud-App-Sicherheit](get-ready-for-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="d805e-p104">If Office 365 Cloud App Security is not turned on yet, you can do that on this page. See [Get ready for Office 365 Cloud App Security](get-ready-for-office-365-cas.md).</span></span> 
  
4. <span data-ttu-id="d805e-131">Wählen Sie **untersuchen** \> **App-Berechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="d805e-131">Choose **Investigate** \> **App permissions**.</span></span>
    
    ![Wählen Sie im Portal O365 CAS überprüfen.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)
  
## <a name="what-youll-see-on-the-manage-app-permissions-page"></a><span data-ttu-id="d805e-133">Was sehen Sie auf der Seite verwalten app-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="d805e-133">What you'll see on the Manage app permissions page</span></span>
<span data-ttu-id="d805e-134"><a name="whatsonpage"> </a></span><span class="sxs-lookup"><span data-stu-id="d805e-134"></span></span>

<span data-ttu-id="d805e-135">In der folgenden Tabelle werden die Steuerelemente und die verfügbaren Optionen auf der Seite Manage app Berechtigungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d805e-135">The following table describes the controls and options available on the Manage app permissions page.</span></span>
  
|<span data-ttu-id="d805e-136">**Element**</span><span class="sxs-lookup"><span data-stu-id="d805e-136">**Item**</span></span>|<span data-ttu-id="d805e-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d805e-137">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d805e-138">Grundlegende Symbol in der app-Leiste Abfrage</span><span class="sxs-lookup"><span data-stu-id="d805e-138">Basic icon in the app query bar</span></span>  <br/> ![Symbol, der angibt, grundlegende Abfrageansicht für das Abfragen von app-Berechtigungen](media/a459bc51-e86b-43d5-a0ee-661b9fb4afc9.png)|<span data-ttu-id="d805e-140">Wählen Sie diese Option, um die erweiterte Ansicht wechseln.</span><span class="sxs-lookup"><span data-stu-id="d805e-140">Select this to switch to the Advanced view.</span></span>  <br/> <span data-ttu-id="d805e-141">(Wenn Sie **grundlegende**angezeigt wird, die erweiterte Ansicht verwenden Sie)</span><span class="sxs-lookup"><span data-stu-id="d805e-141">(If you see **Basic**, you are using the Advanced view)</span></span>  <br/> |
|<span data-ttu-id="d805e-142">Erweiterte Symbol in der app-Leiste Abfrage</span><span class="sxs-lookup"><span data-stu-id="d805e-142">Advanced icon in the app query bar</span></span>  <br/> ![Symbol, das angibt, Abfrageansicht für das Abfragen von app-Berechtigungen für die erweiterte](media/9958d832-2c81-45ed-a642-d926310ba6b6.png)|<span data-ttu-id="d805e-144">Wählen Sie diese Option, um die grundlegende Ansicht wechseln.</span><span class="sxs-lookup"><span data-stu-id="d805e-144">Select this to switch to the Basic view.</span></span>  <br/> <span data-ttu-id="d805e-145">(Wenn Sie **Erweitert**angezeigt wird, werden Sie die grundlegende Ansicht verwenden.)</span><span class="sxs-lookup"><span data-stu-id="d805e-145">(If you see **Advanced**, you are using the Basic view.)</span></span>  <br/> |
|<span data-ttu-id="d805e-146">Öffnen Sie oder schließen Sie alle Detailsymbol in der app-Liste</span><span class="sxs-lookup"><span data-stu-id="d805e-146">Open or close all details icon in the app list</span></span>  <br/> ![Klicken Sie auf dieses Symbol, um das Öffnen oder schließen Sie alle Details für alle apps](media/018fa996-10e8-48ff-986e-55f2b69a5753.png)|<span data-ttu-id="d805e-148">Wählen Sie dieses Symbol, um mehr oder weniger Details zu einzelnen app anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d805e-148">Select this icon to view more or fewer details about each app.</span></span>  <br/> |
|<span data-ttu-id="d805e-149">Exportsymbol in der app-Liste</span><span class="sxs-lookup"><span data-stu-id="d805e-149">Export icon in the app list</span></span>  <br/> ![Klicken Sie auf dieses Symbol, um alle Apps eine Csv-Datei exportieren](media/98446851-fd96-4d09-9bb0-831db33090c1.png)|<span data-ttu-id="d805e-151">Wählen Sie dieses Symbol, um eine CSV-Datei zu exportieren, die eine Liste von apps, die Anzahl von Benutzern für die jeweilige app die app, Berechtigungsstufe, app-Status und Community Verwendung Ebene zugeordneten Berechtigungen enthält.</span><span class="sxs-lookup"><span data-stu-id="d805e-151">Select this icon to export a CSV file that contains a list of apps, number of users for each app, permissions associated with the app, permissions level, app state, and community use level.</span></span>  <br/> |
|<span data-ttu-id="d805e-152">Name</span><span class="sxs-lookup"><span data-stu-id="d805e-152">Name</span></span>  <br/> |<span data-ttu-id="d805e-p105">Verwenden Sie diese auf den Namen der eine App auswählen finden Sie unter dem Namen zum Anzeigen von Informationen, Beschreibung, Publisher, app-Website und app-ID.</span><span class="sxs-lookup"><span data-stu-id="d805e-p105">Use this to see the name of an app. Select the name to view more information, such as its description, publisher, app website and app ID.</span></span>  <br/> |
|<span data-ttu-id="d805e-155">Autorisiert durch</span><span class="sxs-lookup"><span data-stu-id="d805e-155">Authorized by</span></span>  <br/> |<span data-ttu-id="d805e-p106">Verwenden Sie diese Option, um anzuzeigen, wie viele Benutzer Zugriff auf ihre Office 365-Konto eine app autorisiert haben. Wählen Sie die Nummer, um weitere Informationen, wie eine Liste der Benutzerkonten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d805e-p106">Use this to see how many users have authorized an app to access their Office 365 account. Select the number to view more information, such as a list of user accounts.</span></span>  <br/> |
|<span data-ttu-id="d805e-158">Berechtigungsstufe</span><span class="sxs-lookup"><span data-stu-id="d805e-158">Permissions Level</span></span>  <br/> ![Symbol, das die Permisiions Ebene für eine app angibt](media/aaebdd29-35b6-4c62-aef1-7c7817bd803d.png)|<span data-ttu-id="d805e-p107">Verwenden Sie diese Option, um anzuzeigen, wie viel eine app auf Office 365-Daten zugreifen können. Berechtigungsstufen angeben, **Niedrig**, **Mittel**oder **Hoch**, wobei **Niedrig** hinweisen können, dass die app nur Profile und den Namen des Benutzers zugreift. Wählen Sie die Ebene, um weitere Informationen, wie Berechtigungen erteilt der app, Community-Verwendung und verwandte Aktivität im [Governance Protokoll](suspend-or-restore-an-account-in-ocas.md)anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d805e-p107">Use this to see how much access an app has to Office 365 data. Permissions levels indicate **Low**, **Medium**, or **High**, where **Low** might indicate that the app only accesses a user's profile and name. Select the level to view more information, such as permissions granted to the app, community use, and related activity in the [Governance log](suspend-or-restore-an-account-in-ocas.md).  </span></span><br/> |
|<span data-ttu-id="d805e-163">App-Status ( **gesperrten**, **genehmigt**oder **unbestimmt**)</span><span class="sxs-lookup"><span data-stu-id="d805e-163">App state ( **Banned**, **Approved**, or **Undetermined**)</span></span>  <br/> <span data-ttu-id="d805e-164">![App-Berechtigungen Symbole, nachdem die wird zugelassen, blockiert oder keine Aktion durch den ein Administrator ausgeführt wurde](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)</span><span class="sxs-lookup"><span data-stu-id="d805e-164">![App permissions icons after being allowed, blocked, or no action has been taken by an admin](media/5748bd02-cd59-4bd1-a36f-d25a186e8055.png)</span></span>|<span data-ttu-id="d805e-165">Hiermit können Sie um eine app als genehmigt oder gesperrten zu markieren, oder lassen sie als unbestimmten.</span><span class="sxs-lookup"><span data-stu-id="d805e-165">Use this to mark an app as Approved or Banned, or leave it as undetermined.</span></span>  <br/> |
   
## <a name="mark-an-app-as-approved"></a><span data-ttu-id="d805e-166">Markieren Sie eine app genehmigt hat</span><span class="sxs-lookup"><span data-stu-id="d805e-166">Mark an app as approved</span></span>
<span data-ttu-id="d805e-167"><a name="approveapp"> </a></span><span class="sxs-lookup"><span data-stu-id="d805e-167"></span></span>

<span data-ttu-id="d805e-168">Klicken Sie auf der Seite **app-Berechtigungen verwalten** suchen Sie die app aus, den, die Sie genehmigen möchten,, und wählen Sie das Symbol **Mark app als genehmigt** .</span><span class="sxs-lookup"><span data-stu-id="d805e-168">On the **Manage app permissions** page, locate the app you want to approve, and choose the **Mark app as approved** icon.</span></span> 
  
![Wählen Sie die app Mark als genehmigte Symbol](media/dd1b7690-441a-48c9-9c3a-58466513c63d.png)
  
<span data-ttu-id="d805e-170">Das Symbol wird grün und die app für alle Ihre Office 365-Benutzer freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d805e-170">The icon turns green, and the app is approved for all your Office 365 users.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d805e-p108">Wenn Sie eine app genehmigt markieren, ist es keine Auswirkung auf die Endbenutzer. Visuell Markieren von apps, die genehmigt wurden hilft bei der um sie von apps zu trennen, die noch überarbeitet wurden noch nicht bei.</span><span class="sxs-lookup"><span data-stu-id="d805e-p108">When you mark an app as approved, there is no effect on the end user. Visually marking the apps that are approved helps to separate them from apps that haven't been reviewed yet.</span></span> 
  
## <a name="ban-an-app"></a><span data-ttu-id="d805e-173">Sperren einer app</span><span class="sxs-lookup"><span data-stu-id="d805e-173">Ban an app</span></span>
<span data-ttu-id="d805e-174"><a name="banapp"> </a></span><span class="sxs-lookup"><span data-stu-id="d805e-174"></span></span>

1. <span data-ttu-id="d805e-175">Suchen Sie die app aus, die Sie sperren möchten, und wählen Sie das Symbol **Mark app als gesperrte** , auf der Seite **app-Berechtigungen verwalten** .</span><span class="sxs-lookup"><span data-stu-id="d805e-175">On the **Manage app permissions** page, locate the app you want to ban, and choose the **Mark app as banned** icon.</span></span> 
    
    ![Wählen Sie die app Mark als gesperrte Symbol](media/b9b1c5f6-fde7-46d5-8589-1564d05702b3.png)
  
2. <span data-ttu-id="d805e-177">Wählen Sie, ob, damit Benutzer wissen, dass ihre app gesperrt wurde.</span><span class="sxs-lookup"><span data-stu-id="d805e-177">Choose whether to let users know that their app has been banned.</span></span>
    
    <span data-ttu-id="d805e-178">(Empfohlen) Um Benutzer wissen zu lassen, wählen Sie **Notify-Benutzer, die Zugriff auf diese gesperrten app gewährt**, fügen Sie hinzu oder bearbeiten Sie eine benutzerdefinierte Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="d805e-178">(Recommended) To let users know, select **Notify users who granted access to this banned app**, and add or edit a custom notification message.</span></span>
    
    <span data-ttu-id="d805e-179">Damit können Benutzer wissen nicht, deaktivieren Sie **Notify-Benutzer, die Zugriff auf diese gesperrten app gewährt**.</span><span class="sxs-lookup"><span data-stu-id="d805e-179">To not let users know, clear **Notify users who granted access to this banned app**.</span></span>
    
    ![Die e-Mail-Vorlage für eine gesperrte-app](media/6d132700-5f7f-472c-bfb5-a44549e69c16.jpg)
  
3. <span data-ttu-id="d805e-181">Wählen Sie **app Sperren**.</span><span class="sxs-lookup"><span data-stu-id="d805e-181">Choose **Ban app**.</span></span>
    
## <a name="create-an-app-query"></a><span data-ttu-id="d805e-182">Erstellen Sie eine app-Abfrage</span><span class="sxs-lookup"><span data-stu-id="d805e-182">Create an app query</span></span>
<span data-ttu-id="d805e-183"><a name="createapp"> </a></span><span class="sxs-lookup"><span data-stu-id="d805e-183"></span></span>

1. <span data-ttu-id="d805e-p109">In der Abfrage app-Leiste Wenn Sie **Erweitert**angezeigt wird, klicken Sie auf (oder tippen Sie auf) es so wechseln zur erweiterten Ansicht. (Wenn Sie Basic angezeigt wird, verwenden Sie die erweiterte Ansicht, nicht die Ansicht geändert werden.)</span><span class="sxs-lookup"><span data-stu-id="d805e-p109">In the app query bar, if you see **Advanced**, click (or tap) it to go to the Advanced view. (If you see Basic, you are using the Advanced view; keep your view as it is.)</span></span>
    
2. <span data-ttu-id="d805e-p110">Verwenden Sie der Liste **Wählen Sie einen Filter** , um eine Option zu wählen. In der folgenden Tabelle sind die verfügbaren Filteroptionen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="d805e-p110">Use the **Select a filter** list to choose an option. The following table summarizes your available filter options.</span></span> 
    
|<span data-ttu-id="d805e-188">**Verwenden Sie diesen filter**</span><span class="sxs-lookup"><span data-stu-id="d805e-188">**Use this filter**</span></span>|<span data-ttu-id="d805e-189">**Um Folgendes anzuzeigen**</span><span class="sxs-lookup"><span data-stu-id="d805e-189">**To display**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d805e-190">**App**</span><span class="sxs-lookup"><span data-stu-id="d805e-190">**App**</span></span> <br/> |<span data-ttu-id="d805e-191">Apps mit bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="d805e-191">Apps with certain names</span></span>  <br/> |
|<span data-ttu-id="d805e-192">**App-Status**</span><span class="sxs-lookup"><span data-stu-id="d805e-192">**App state**</span></span> <br/> |<span data-ttu-id="d805e-193">Apps basierend auf deren Status (genehmigt, gesperrten oder unbestimmt)</span><span class="sxs-lookup"><span data-stu-id="d805e-193">Apps based on their state (Approved, Banned, or Undetermined)</span></span>  <br/> |
|<span data-ttu-id="d805e-194">**Community-Verwendung**</span><span class="sxs-lookup"><span data-stu-id="d805e-194">**Community use**</span></span> <br/> |<span data-ttu-id="d805e-195">Verwenden Sie Apps basierend auf Community Ebenen (seltene, Uncommon oder gemeinsamen)</span><span class="sxs-lookup"><span data-stu-id="d805e-195">Apps based on community use levels (Rare, Uncommon, or Common)</span></span>  <br/> |
|<span data-ttu-id="d805e-196">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="d805e-196">**Permission level**</span></span> <br/> |<span data-ttu-id="d805e-197">Apps basierend auf bestimmte Berechtigungsstufen</span><span class="sxs-lookup"><span data-stu-id="d805e-197">Apps based on certain permission levels</span></span>  <br/> |
|<span data-ttu-id="d805e-198">**Berechtigungen**</span><span class="sxs-lookup"><span data-stu-id="d805e-198">**Permissions**</span></span> <br/> |<span data-ttu-id="d805e-199">Apps, die bestimmte Berechtigungen erfordern</span><span class="sxs-lookup"><span data-stu-id="d805e-199">Apps that require certain permissions</span></span>  <br/> |
|<span data-ttu-id="d805e-200">**Herausgeber**</span><span class="sxs-lookup"><span data-stu-id="d805e-200">**Publisher**</span></span> <br/> |<span data-ttu-id="d805e-201">Apps, die von bestimmten Herausgebern</span><span class="sxs-lookup"><span data-stu-id="d805e-201">Apps from certain publishers</span></span>  <br/> |
|<span data-ttu-id="d805e-202">**Benutzer**</span><span class="sxs-lookup"><span data-stu-id="d805e-202">**User**</span></span> <br/> |<span data-ttu-id="d805e-203">Apps, die ein bestimmter Benutzer autorisiert</span><span class="sxs-lookup"><span data-stu-id="d805e-203">Apps that a certain user authorized</span></span>  <br/> |
   
3. <span data-ttu-id="d805e-204">Wählen Sie **gleich** oder **ungleich**aus, und geben Sie einen Wert für den Filter.</span><span class="sxs-lookup"><span data-stu-id="d805e-204">Select **equals** or **does not equal**, and then specify a value for your filter.</span></span>
    
4. <span data-ttu-id="d805e-205">Um weitere Filter hinzuzufügen, wählen Sie das Pluszeichen (+) (</span><span class="sxs-lookup"><span data-stu-id="d805e-205">To add more filters, select the plus sign (</span></span>![Fügen Sie ein Filter-Symbol für das Abfragen von apps](media/771b2958-67cd-4e14-9302-283ef238cae5.jpg)<span data-ttu-id="d805e-207">), und wiederholen Sie die Schritte 2 und 3.</span><span class="sxs-lookup"><span data-stu-id="d805e-207">), and then repeat steps 2 and 3.</span></span>
    
5. <span data-ttu-id="d805e-208">Wählen Sie zum Entfernen eines Filters aus der x (</span><span class="sxs-lookup"><span data-stu-id="d805e-208">To remove a filter, select the x (</span></span>![Entfernen Sie ein Filter-Symbol für das Abfragen von apps](media/5339277f-555d-4749-8dcc-d2574250556e.jpg)<span data-ttu-id="d805e-210">) neben dem Namen eines Filters.</span><span class="sxs-lookup"><span data-stu-id="d805e-210">) next to a filter name.</span></span>
    
<span data-ttu-id="d805e-211">Die Filter werden automatisch angewendet, und die Liste apps wird entsprechend aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d805e-211">The filters are applied automatically, and the apps list is updated accordingly.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="d805e-212">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d805e-212">Next steps</span></span>
<span data-ttu-id="d805e-213"><a name="nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="d805e-213"></span></span>

- [<span data-ttu-id="d805e-214">Lesen und Ausführen einer Aktion Warnungen</span><span class="sxs-lookup"><span data-stu-id="d805e-214">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="d805e-215">Überprüfen Sie Ihre [Web-Datenverkehr Protokolle und Datenquellen für Office 365-Cloud-App-Sicherheit](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="d805e-215">Review your [Web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="d805e-216">Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="d805e-216">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

