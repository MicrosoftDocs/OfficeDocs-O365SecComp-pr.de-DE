---
title: Überwachen der Freigabe für die Suche nach Ressourcen, die für externe Benutzer freigegeben wurden
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Die Freigabe ist eine wichtige Aktivität in SharePoint Online und OneDrive für Unternehmen. Administratoren können jetzt die Freigabe Überwachung im Office 365 Überwachungsprotokoll verwenden, um zu bestimmen, wie die Freigabe in Ihrer Organisation verwendet wird. '
ms.openlocfilehash: e2865d35e988d8c0e42a6c51f78507db8b170d4c
ms.sourcegitcommit: b262d40f6daf06be26e7586f37b736e09f8a4511
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/02/2019
ms.locfileid: "35435239"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="9576f-104">Überwachen der Freigabe für die Suche nach Ressourcen, die für externe Benutzer freigegeben wurden</span><span class="sxs-lookup"><span data-stu-id="9576f-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="9576f-105">Die Freigabe ist eine wichtige Aktivität in SharePoint Online und OneDrive für Unternehmen und wird in Office 365 Organisationen häufig verwendet.</span><span class="sxs-lookup"><span data-stu-id="9576f-105">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations.</span></span> <span data-ttu-id="9576f-106">Administratoren können jetzt die Freigabe Überwachung im Office 365 Überwachungsprotokoll verwenden, um zu bestimmen, wie die Freigabe in Ihrer Organisation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9576f-106">Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="9576f-107">Das SharePoint-Freigabe Schema</span><span class="sxs-lookup"><span data-stu-id="9576f-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="9576f-108">Freigabe Ereignisse (ohne Freigaberichtlinie und Freigabe Link Ereignisse) unterscheiden sich in erster Linie von Datei-und ordnerbezogenen Ereignissen: ein Benutzer führt eine Aktion aus, die sich auf einen anderen Benutzer auswirkt.</span><span class="sxs-lookup"><span data-stu-id="9576f-108">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user.</span></span> <span data-ttu-id="9576f-109">Benutzer a gibt beispielsweise Benutzer B Zugriff auf eine Datei.</span><span class="sxs-lookup"><span data-stu-id="9576f-109">For example, User A gives User B access to a file.</span></span> <span data-ttu-id="9576f-110">In diesem Beispiel ist Benutzer A der *stellvertretende Benutzer* , und Benutzer B ist der *Zielbenutzer*.</span><span class="sxs-lookup"><span data-stu-id="9576f-110">In this example, User A is the  *acting user*  and User B is the  *target user*.</span></span> <span data-ttu-id="9576f-111">Im SharePoint-Datei Schema wirkt sich die Aktion des handelnden Benutzers nur auf die Datei selbst aus.</span><span class="sxs-lookup"><span data-stu-id="9576f-111">In the SharePoint File schema, the acting user's action only affects the file itself.</span></span> <span data-ttu-id="9576f-112">Wenn Benutzer a eine Datei öffnet, sind die einzigen Informationen, die \*\*\*\* im fileaccessed-Ereignis erforderlich sind, der Benutzer, der fungiert.</span><span class="sxs-lookup"><span data-stu-id="9576f-112">When User A opens a file, the only information needed in the **FileAccessed** event is the acting user.</span></span> <span data-ttu-id="9576f-113">Um diesen Unterschied zu beheben, gibt es ein separates Schema, das als *SharePoint-Freigabe Schema*bezeichnet wird und in dem weitere Informationen zur Freigabe von Ereignissen erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="9576f-113">To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events.</span></span> <span data-ttu-id="9576f-114">Dadurch wird sichergestellt, dass Administratoren mehr Einblick in die Person haben, die eine Ressource gemeinsam genutzt hat, und den Benutzer, für den die Ressource freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9576f-114">This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="9576f-115">Das Freigabe Schema stellt zwei zusätzliche Felder im Überwachungsprotokoll im Zusammenhang mit Freigabe Ereignissen bereit:</span><span class="sxs-lookup"><span data-stu-id="9576f-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="9576f-116">**TargetUserOrGroupName** – speichert den UPN oder den Namen des Zielbenutzers oder der Zielgruppe, für die eine Ressource freigegeben wurde (Benutzer B im vorherigen Beispiel).</span><span class="sxs-lookup"><span data-stu-id="9576f-116">**TargetUserOrGroupName** – Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="9576f-117">**TargetUserOrGroupType** – gibt an, ob der Zielbenutzer oder die Zielgruppe ein Mitglied, Gast, eine Gruppe oder ein Partner ist.</span><span class="sxs-lookup"><span data-stu-id="9576f-117">**TargetUserOrGroupType** – Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="9576f-118">Diese beiden Felder können zusätzlich zu anderen Eigenschaften aus dem Office 365 Überwachungsprotokoll Schema wie "Benutzer", "Vorgang" und "Datum" die vollständige Übersicht darüber geben, *welcher* Benutzer *welche* Ressource mit *wem* und *wann*freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="9576f-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="9576f-119">Es gibt eine andere Schemaeigenschaft, die für den Freigabe Text wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="9576f-119">There's another schema property that's important to the sharing story.</span></span> <span data-ttu-id="9576f-120">Die **EventData** -Eigenschaft speichert zusätzliche Informationen zu Freigabe Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="9576f-120">The **EventData** property stores additional information about sharing events.</span></span> <span data-ttu-id="9576f-121">Wenn ein Benutzer beispielsweise eine Website für einen anderen Benutzer freigibt, wird dies erreicht, indem der Zielbenutzer einer SharePoint-Gruppe hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="9576f-121">For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group.</span></span> <span data-ttu-id="9576f-122">Die **EventData** -Eigenschaft erfasst diese zusätzlichen Informationen, um Administratoren Kontext bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9576f-122">The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="9576f-123">Das SharePoint-Freigabemodell und Freigabe Ereignisse</span><span class="sxs-lookup"><span data-stu-id="9576f-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="9576f-124">Die Freigabe wird durch drei separate Ereignisse definiert \*\*\*\*: "sharingset", " **SharingInvitationCreated**" und " **SharingInvitaitonAccepted**".</span><span class="sxs-lookup"><span data-stu-id="9576f-124">Sharing is defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**.</span></span> <span data-ttu-id="9576f-125">Hier ist der Workflow für die Protokollierung von Freigabe Ereignissen im Office 365 Überwachungsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="9576f-125">Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Flussdiagramm zur Funktionsweise der Freigabe Überwachung](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="9576f-127">Wenn ein Benutzer (der stellvertretender Benutzer) eine Ressource für einen anderen Benutzer (den Zielbenutzer) freigeben möchte, überprüft SharePoint (oder OneDrive für Unternehmen) zunächst, ob die e-Mail-Adresse des Zielbenutzers bereits einem Benutzerkonto im Verzeichnis der Organisation zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9576f-127">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory.</span></span> <span data-ttu-id="9576f-128">Wenn sich der Zielbenutzer im Verzeichnis der Organisation befindet, führt SharePoint Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="9576f-128">If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="9576f-129">Weist sofort die Zielbenutzer Berechtigungen für den Zugriff auf die Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="9576f-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="9576f-130">Sendet eine Freigabe Benachrichtigung an die e-Mail-Adresse des Zielbenutzers.</span><span class="sxs-lookup"><span data-stu-id="9576f-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="9576f-131">Protokolliert ein **sharingset** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9576f-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="9576f-132">Wenn sich ein Benutzerkonto für den Zielbenutzer nicht im Verzeichnis der Organisation befindet, führt SharePoint Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="9576f-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="9576f-133">Erstellt eine Freigabeeinladung und sendet Sie an die e-Mail-Adresse des Zielbenutzers.</span><span class="sxs-lookup"><span data-stu-id="9576f-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="9576f-134">Protokolliert ein **SharingInvitationCreated** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="9576f-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="9576f-135">Das **SharingInvitationCreated** -Ereignis ist meistens immer mit externer oder Gast Freigabe verbunden, wenn der Zielbenutzer keinen Zugriff auf die freigegebene Ressource hat.</span><span class="sxs-lookup"><span data-stu-id="9576f-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="9576f-136">Wenn der Zielbenutzer die an Sie gesendete Freigabeeinladung annimmt (durch Klicken auf den Link in der Einladung), protokolliert SharePoint ein **SharingInvitationAccepted** -Ereignis und weist den Zielbenutzer Berechtigungen für den Zugriff auf die Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="9576f-136">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource.</span></span> <span data-ttu-id="9576f-137">Weitere Informationen zum Zielbenutzer werden ebenfalls protokolliert, beispielsweise die Identität des Benutzers, an den die Einladung gesendet wurde, und der Benutzer, der die Einladung tatsächlich angenommen hat.</span><span class="sxs-lookup"><span data-stu-id="9576f-137">Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation.</span></span> <span data-ttu-id="9576f-138">In einigen Fällen können diese Benutzer (oder e-Mail-Adressen) unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="9576f-138">In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="9576f-139">Vorgehensweise identifizieren von Ressourcen, die für externe Benutzer freigegeben sind</span><span class="sxs-lookup"><span data-stu-id="9576f-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="9576f-140">Eine häufige Anforderung an Administratoren ist das Erstellen einer Liste aller Ressourcen, die für Benutzer außerhalb der Organisation freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="9576f-140">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization.</span></span> <span data-ttu-id="9576f-141">Wenn Sie die Freigabe Überwachung in Office 365 verwenden, können Administratoren diese Liste jetzt generieren.</span><span class="sxs-lookup"><span data-stu-id="9576f-141">By using sharing auditing in Office 365, administrators can now generate this list.</span></span> <span data-ttu-id="9576f-142">Die gehen so:</span><span class="sxs-lookup"><span data-stu-id="9576f-142">Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="9576f-143">Schritt 1: Suchen nach Freigabe Ereignissen und Exportieren der Ergebnisse in eine CSV-Datei</span><span class="sxs-lookup"><span data-stu-id="9576f-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="9576f-144">Der erste Schritt besteht darin, das Office 365 Überwachungsprotokoll nach Freigabe Ereignissen zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="9576f-144">The first step is to search the Office 365 audit log for sharing events.</span></span> <span data-ttu-id="9576f-145">Weitere Informationen (einschließlich der erforderlichen Berechtigungen) zum Durchsuchen des Überwachungsprotokolls finden Sie unter [Durchsuchen des Überwachungsprotokolls im Security #a0 Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="9576f-145">For more information (including the required permissions) about searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="9576f-146">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="9576f-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="9576f-147">Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="9576f-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="9576f-148">Klicken Sie im linken Bereich des Security #a0 Compliance Centers auf **Such**  > **Überwachungsprotokoll Suche**.</span><span class="sxs-lookup"><span data-stu-id="9576f-148">In the left pane of the Security & Compliance Center, click **Search**  > **Audit log search**.</span></span>
    
    <span data-ttu-id="9576f-149">Die Seite **Überwachungsprotokoll Suche** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9576f-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="9576f-150">Klicken Sie unter **Aktivitäten**auf **Freigabe-und Zugriffs Anforderungs Aktivitäten** , um nach Freigabe bezogenen Ereignissen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="9576f-150">Under **Activities**, click **Sharing and access request activities** to search for sharing-related events.</span></span> 
    
    ![Wählen Sie unter Aktivitäten die Option Freigabe-und Zugriffs Anforderungs Aktivitäten aus.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="9576f-152">Wählen Sie einen Datums-und Zeitbereich aus, um die Freigabe Ereignisse zu finden, die innerhalb dieses Zeitraums aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="9576f-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="9576f-153">Klicken Sie auf **Suchen** , um die Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9576f-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="9576f-154">Wenn die Suche abgeschlossen ist und die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse** \> exportieren **alle Ergebnisse herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="9576f-154">When the search is finished running and the results are displayed, click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="9576f-155">Nachdem Sie die Option Exportieren ausgewählt haben, wird am unteren Rand des Fensters eine Meldung angezeigt, in der Sie aufgefordert werden, die CSV-Datei zu öffnen oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="9576f-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="9576f-156">Klicken Sie auf Save **As** **Speichern** \> und speichern Sie die CSV-Datei in einem Ordner auf Ihrem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="9576f-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 

### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="9576f-157">Schritt 2: Filtern der CSV-Datei nach Ressourcen, die für externe Benutzer freigegeben sind</span><span class="sxs-lookup"><span data-stu-id="9576f-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="9576f-158">Der nächste Schritt besteht darin, die CSV-Datei \*\*\*\* für das sharingset-und das **SharingInvitationCreated** -Ereignis zu filtern und die Ereignisse anzuzeigen, bei denen die **TargetUserOrGroupType** -Eigenschaft **Gast**ist.</span><span class="sxs-lookup"><span data-stu-id="9576f-158">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**.</span></span> <span data-ttu-id="9576f-159">Verwenden Sie dazu das Tool Power Query Editor in Excel.</span><span class="sxs-lookup"><span data-stu-id="9576f-159">You use the Power Query Editor tool in Excel to do this.</span></span> <span data-ttu-id="9576f-160">Eine Schritt-für-Schritt-Anleitung finden Sie unter [exportieren, konfigurieren und Anzeigen von Überwachungsprotokolldaten Sätzen](export-view-audit-log-records.md).</span><span class="sxs-lookup"><span data-stu-id="9576f-160">For step-by-step instructions, see [Export, configure, and view audit log records](export-view-audit-log-records.md).</span></span> 

<span data-ttu-id="9576f-161">Nachdem Sie die Anweisungen im vorherigen Thema zum Vorbereiten der CSV-Datei befolgt haben, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="9576f-161">After you've followed the instructions in the previous topic to prepare the CSV file, do the following:</span></span>
    
1. <span data-ttu-id="9576f-162">Öffnen Sie die CSV-Datei, die Sie mit dem Power Query-Editor vorbereitet haben.</span><span class="sxs-lookup"><span data-stu-id="9576f-162">Open the CSV file that you prepared with the Power Query Editor.</span></span> 

2. <span data-ttu-id="9576f-163">Klicken Sie auf der Registerkarte **Start** auf **#a0 Filter sortieren**, und klicken Sie dann auf **Filter**.</span><span class="sxs-lookup"><span data-stu-id="9576f-163">On the **Home** tab, click **Sort & Filter**, and then click **Filter**.</span></span>
    
3. <span data-ttu-id="9576f-164">Deaktivieren Sie in der Dropdownliste **Sortier #a0 Filter** in der Spalte **Vorgänge** alle Optionen, und wählen \*\*\*\* Sie dann freigabeset und **SharingInvitationCreated**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9576f-164">In the **Sort & Filter** dropdown list on the **Operations** column, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="9576f-165">Excel zeigt die Zeilen für das **sharingset** -und das **SharingInvitationCreated** -Ereignis an.</span><span class="sxs-lookup"><span data-stu-id="9576f-165">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
4. <span data-ttu-id="9576f-166">Wechseln Sie zur Spalte mit dem Namen **TargetUserOrGroupType** , und wählen Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="9576f-166">Go to the column named **TargetUserOrGroupType** and select it.</span></span> 
    
5. <span data-ttu-id="9576f-167">Deaktivieren Sie in der Dropdownliste **Sortier #a0 Filter** die Option alle Auswahlen, wählen Sie **TargetUserOrGroupType: Gast**aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9576f-167">In the **Sort & Filter** dropdown list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="9576f-168">In Excel werden nun die Zeilen für **SharingInvitationCreated** -und **sharingset** -Ereignisse sowie die Position des Zielbenutzers außerhalb Ihrer Organisation angezeigt, da externe Benutzer durch den Wert **TargetUserOrGroupType: Guest**identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9576f-168">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="9576f-169">In der folgenden Tabelle sind alle Benutzer in der Organisation aufgeführt, die Ressourcen mit einem Gastbenutzer innerhalb eines angegebenen Datumsbereichs freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="9576f-169">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Freigeben von Ereignissen in Office 365 Überwachungsprotokoll](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="9576f-171">Obwohl es nicht in der vorherigen Tabelle enthalten ist, gibt die **objectID** -Eigenschaft die Ressource an, die für den Zielbenutzer freigegeben wurde; zum Beispiel `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="9576f-171">Although it's not included in the previous table, the **ObjectId** property identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="9576f-172">Wenn Sie ermitteln möchten, ob einem Gastbenutzer tatsächlich Berechtigungen für den Zugriff auf eine Ressource zugewiesen wurden (im Gegensatz zu den Ressourcen, die für Sie freigegeben wurden), wiederholen Sie die Schritte 2, 3 und 4, und Filtern Sie nach dem **SharingInvitationAccepted** und dem **freigabeset** . Ereignisse in Schritt 5.</span><span class="sxs-lookup"><span data-stu-id="9576f-172">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 2, 3, and 4, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 5.</span></span> 
