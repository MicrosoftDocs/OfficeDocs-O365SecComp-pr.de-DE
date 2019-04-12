---
title: Überwachen der Freigabe für die Suche nach Ressourcen, die für externe Benutzer freigegeben wurden
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Die Freigabe ist eine wichtige Aktivität in SharePoint Online und OneDrive for Business. Administratoren können jetzt die Freigabe Überwachung im Office 365-Überwachungsprotokoll verwenden, um zu bestimmen, wie die Freigabe in Ihrer Organisation verwendet wird. '
ms.openlocfilehash: 08b511acdf74edac5b2d595d1b60bdd84d630918
ms.sourcegitcommit: 6c9340e4eb221bf81472ff3f1ae25ae21aaf5297
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/11/2019
ms.locfileid: "31813946"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="8d7e0-104">Überwachen der Freigabe für die Suche nach Ressourcen, die für externe Benutzer freigegeben wurden</span><span class="sxs-lookup"><span data-stu-id="8d7e0-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="8d7e0-105">Die Freigabe ist eine wichtige Aktivität in SharePoint Online und OneDrive for Business und wird in Office 365-Organisationen am häufigsten verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-105">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations.</span></span> <span data-ttu-id="8d7e0-106">Administratoren können jetzt die Freigabe Überwachung im Office 365-Überwachungsprotokoll verwenden, um zu bestimmen, wie die Freigabe in Ihrer Organisation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-106">Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="8d7e0-107">Das SharePoint-Freigabe Schema</span><span class="sxs-lookup"><span data-stu-id="8d7e0-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="8d7e0-108">Freigabe Ereignisse (ohne Freigaberichtlinien und Freigabe verknüpfungsereignisse) unterscheiden sich von Datei-und ordnerbezogenen Ereignissen auf eine primäre Art und Weise: ein Benutzer führt eine Aktion aus, die für einen anderen Benutzer etwas bewirkt.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-108">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user.</span></span> <span data-ttu-id="8d7e0-109">Benutzer A gibt beispielsweise dem Benutzer B Zugriff auf eine Datei.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-109">For example, User A gives User B access to a file.</span></span> <span data-ttu-id="8d7e0-110">In diesem Beispiel ist Benutzer A der *amtierende Benutzer* und Benutzer B der *Zielbenutzer*.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-110">In this example, User A is the  *acting user*  and User B is the  *target user*.</span></span> <span data-ttu-id="8d7e0-111">Im SharePoint-Datei Schema wirkt sich die Aktion des handelnden Benutzers nur auf die Datei selbst aus.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-111">In the SharePoint File schema, the acting user's action only affects the file itself.</span></span> <span data-ttu-id="8d7e0-112">Wenn Benutzer A eine Datei öffnet, ist der handelnde Benutzer nur \*\*\*\* für das fileaccessed-Ereignis erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-112">When User A opens a file, the only information needed in the **FileAccessed** event is the acting user.</span></span> <span data-ttu-id="8d7e0-113">Um diesen Unterschied zu beheben, gibt es ein separates Schema, das als *SharePoint-Freigabe Schema*bezeichnet wird und weitere Informationen zu Freigabe Ereignissen erfasst.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-113">To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events.</span></span> <span data-ttu-id="8d7e0-114">Auf diese Weise wird sichergestellt, dass Administratoren mehr über die Freigabe einer Ressource und den Benutzer verfügen, für den die Ressource freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-114">This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="8d7e0-115">Das Freigabe Schema enthält zwei zusätzliche Felder im Überwachungsprotokoll im Zusammenhang mit Freigabe Ereignissen:</span><span class="sxs-lookup"><span data-stu-id="8d7e0-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="8d7e0-116">**TargetUserOrGroupName** -speichert den UPN oder den Namen des Zielbenutzers oder der Gruppe, für die eine Ressource freigegeben wurde (Benutzer B im vorherigen Beispiel).</span><span class="sxs-lookup"><span data-stu-id="8d7e0-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="8d7e0-117">**TargetUserOrGroupType** – gibt an, ob der Zielbenutzer oder die Gruppe Mitglied, Gast, Gruppe oder Partner ist.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="8d7e0-118">Diese beiden Felder, zusätzlich zu anderen Eigenschaften aus dem Office 365-Überwachungsprotokoll Schema wie Benutzer, Vorgang und Datum, können den vollständigen Bericht darüber mitteilen, *welche* Benutzer *welche* Ressource für *wen* und *wann*freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="8d7e0-119">Es gibt eine andere Schemaeigenschaft, die für die Freigabe Story wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-119">There's another schema property that's important to the sharing story.</span></span> <span data-ttu-id="8d7e0-120">Die **EventData** -Eigenschaft speichert zusätzliche Informationen zu Freigabe Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-120">The **EventData** property stores additional information about sharing events.</span></span> <span data-ttu-id="8d7e0-121">Wenn ein Benutzer beispielsweise eine Website für einen anderen Benutzer freigibt, wird dies erreicht, indem der Zielbenutzer einer SharePoint-Gruppe hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-121">For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group.</span></span> <span data-ttu-id="8d7e0-122">Die **EventData** -Eigenschaft erfasst diese zusätzlichen Informationen, um den Kontext für Administratoren bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-122">The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="8d7e0-123">Das SharePoint-Freigabemodell und Freigabe Ereignisse</span><span class="sxs-lookup"><span data-stu-id="8d7e0-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="8d7e0-124">Die Freigabe wird tatsächlich durch drei separate Ereignisse definiert \*\*\*\*: sharingset, **SharingInvitationCreated**und **SharingInvitaitonAccepted**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-124">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**.</span></span> <span data-ttu-id="8d7e0-125">Hier ist der Arbeitsablauf für die Protokollierung von Freigabe Ereignissen im Office 365-Überwachungsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-125">Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Ablaufdiagramm zur Funktionsweise der Freigabe Überwachung](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="8d7e0-127">Wenn ein Benutzer (der amtierende Benutzer) eine Ressource für einen anderen Benutzer (den Zielbenutzer) freigeben möchte, überprüft SharePoint (oder OneDrive for Business) zunächst, ob die e-Mail-Adresse des Zielbenutzers bereits einem Benutzerkonto im Verzeichnis der Organisation zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-127">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory.</span></span> <span data-ttu-id="8d7e0-128">Wenn sich der Zielbenutzer im Verzeichnis der Organisation befindet, führt SharePoint Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="8d7e0-128">If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="8d7e0-129">Weist den Zielbenutzer sofort Berechtigungen für den Zugriff auf die Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="8d7e0-130">Sendet eine Freigabe Benachrichtigung an die e-Mail-Adresse des Zielbenutzers.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="8d7e0-131">Protokolliert ein **sharingset** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="8d7e0-132">Wenn sich ein Benutzerkonto für den Zielbenutzer nicht im Verzeichnis der Organisation befindet, führt SharePoint Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="8d7e0-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="8d7e0-133">Erstellt eine Freigabeeinladung und sendet Sie an die e-Mail-Adresse des Zielbenutzers.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="8d7e0-134">Protokolliert ein **SharingInvitationCreated** -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="8d7e0-135">Das **SharingInvitationCreated** -Ereignis wird immer mit externer oder Gast Freigabe verknüpft, wenn der Zielbenutzer keinen Zugriff auf die freigegebene Ressource hat.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="8d7e0-136">Wenn der Zielbenutzer die Freigabeeinladung akzeptiert, die Ihnen gesendet wird (durch Klicken auf den Link in der Einladung), protokolliert SharePoint ein **SharingInvitationAccepted** -Ereignis und weist die Zielbenutzer Berechtigungen für den Zugriff auf die Ressource zu.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-136">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource.</span></span> <span data-ttu-id="8d7e0-137">Außerdem werden zusätzliche Informationen zum Zielbenutzer protokolliert, beispielsweise die Identität des Benutzers, an den die Einladung gesendet wurde, und der Benutzer, der die Einladung tatsächlich akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-137">Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation.</span></span> <span data-ttu-id="8d7e0-138">In einigen Fällen können diese Benutzer (oder e-Mail-Adressen) unterschiedlich sein.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-138">In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="8d7e0-139">Identifizieren von Ressourcen, die für externe Benutzer freigegeben sind</span><span class="sxs-lookup"><span data-stu-id="8d7e0-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="8d7e0-140">Eine allgemeine Anforderung für Administratoren ist das Erstellen einer Liste aller Ressourcen, die für Benutzer außerhalb der Organisation freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-140">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization.</span></span> <span data-ttu-id="8d7e0-141">Mithilfe der Freigabe Überwachung in Office 365 können Administratoren diese Liste generieren.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-141">By using sharing auditing in Office 365, administrators can now generate this list.</span></span> <span data-ttu-id="8d7e0-142">Die gehen so:</span><span class="sxs-lookup"><span data-stu-id="8d7e0-142">Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="8d7e0-143">Schritt 1: Suchen nach Freigabe Ereignissen und Exportieren der Ergebnisse in eine CSV-Datei</span><span class="sxs-lookup"><span data-stu-id="8d7e0-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="8d7e0-144">Der erste Schritt besteht darin, im Office 365-Überwachungsprotokoll nach Freigabe Ereignissen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-144">The first step is to search the Office 365 audit log for sharing events.</span></span> <span data-ttu-id="8d7e0-145">Weitere Informationen (einschließlich der erforderlichen Berechtigungen) zum Durchsuchen des Überwachungsprotokolls finden Sie unter [Durchsuchen des Überwachungsprotokolls im Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="8d7e0-145">For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Security & Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="8d7e0-146">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="8d7e0-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="8d7e0-147">Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="8d7e0-148">Klicken Sie im linken Bereich des Security & Compliance Centers auf **Such**  > **Überwachungsprotokoll Suche**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-148">In the left pane of the Security & Compliance Center, click **Search**  > **Audit log search**.</span></span>
    
    <span data-ttu-id="8d7e0-149">Die Seite **Überwachungsprotokoll Suche** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="8d7e0-150">Klicken Sie unter **Aktivitäten**auf **freigabeaktivitäten** , um nur nach Freigabe Ereignissen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![Wählen Sie unter Aktivitäten die Option freigabeaktivitäten aus.](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="8d7e0-152">Wählen Sie einen Datums-und Uhrzeitbereich aus, um nach den Freigabe Ereignissen zu suchen, die in diesem Zeitraum aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="8d7e0-153">Klicken Sie auf **Suchen** , um die Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="8d7e0-154">Wenn die Suche abgeschlossen ist und die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse** \> exportieren, um **alle Ergebnisse herunterzuladen**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="8d7e0-155">Nachdem Sie die Option Exportieren ausgewählt haben, wird unten im Fenster eine Meldung angezeigt, in der Sie aufgefordert werden, die CSV-Datei zu öffnen oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="8d7e0-156">Klicken Sie auf Speichern unter, und speichern Sie die CSV-Datei in einem Ordner auf dem lokalen Computer. \*\*\*\* \*\*\*\* \></span><span class="sxs-lookup"><span data-stu-id="8d7e0-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="8d7e0-157">Schritt 2: Filtern der CSV-Datei für Ressourcen, die für externe Benutzer freigegeben sind</span><span class="sxs-lookup"><span data-stu-id="8d7e0-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="8d7e0-158">Der nächste Schritt besteht darin, die CSV-Datei \*\*\*\* für die freigabeset-und **SharingInvitationCreated** -Ereignisse zu filtern und die Ereignisse anzuzeigen, bei denen die **TargetUserOrGroupType** -Eigenschaft **Gast**ist.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-158">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**.</span></span> <span data-ttu-id="8d7e0-159">Hierzu verwenden Sie die Power Query-Funktion in Excel.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-159">You'll use the Power Query feature in Excel to do this.</span></span> <span data-ttu-id="8d7e0-160">Das folgende Verfahren wird in Excel 2016 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-160">The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="8d7e0-161">Öffnen Sie in Excel 2016 eine leere Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="8d7e0-162">Klicken Sie auf die Registerkarte **Daten** .</span><span class="sxs-lookup"><span data-stu-id="8d7e0-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="8d7e0-163">Klicken Sie auf **neue Abfrage** \> **aus Datei** \> **aus CSV**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![Wählen Sie auf der Registerkarte Daten die Option Neue Abfrage aus, wählen Sie aus Datei aus, und wählen Sie dann aus CSV aus.](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="8d7e0-165">Öffnen Sie die CSV-Datei, die Sie in Schritt 1 heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="8d7e0-166">Die CSV-Datei wird im Abfrage-Editor geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-166">The CSV file is opened in the Query Editor.</span></span> <span data-ttu-id="8d7e0-167">Beachten Sie, dass es vier Spalten gibt: **Zeit**, **Benutzer**, **Aktion**und **Detail**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-167">Note that there are four columns: **Time**, **User**, **Action**, and **Detail**.</span></span> <span data-ttu-id="8d7e0-168">Die **Detail** -Spalte ist ein Multi-Property-Feld.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-168">The **Detail** column is a multi-property field.</span></span> <span data-ttu-id="8d7e0-169">Im nächsten Schritt erstellen Sie eine neue Spalte für jede der Eigenschaften in der **Detail** Spalte.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-169">The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="8d7e0-170">Wählen Sie die Spalte **Detail** aus, und klicken Sie dann auf der Registerkarte **Start** auf **Spalte** \> **nach Trennzeichen**teilen.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![Klicken Sie auf der Registerkarte Start auf Spalte teilen, und klicken Sie dann auf nach Trennzeichen](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="8d7e0-172">Gehen Sie in der **Spalte geteilt durch Trennzeichen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="8d7e0-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="8d7e0-173">Wählen Sie unter Trenn **Zeichen auswählen oder eingeben**die Option **Komma**aus.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="8d7e0-174">Wählen \*\*\*\* Sie unter Split **bei jedem Vorkommen des Trennzeichens**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="8d7e0-175">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-175">Click **OK**.</span></span>
    
    <span data-ttu-id="8d7e0-176">Die **Detail** Spalte wird in mehrere Spalten aufgeteilt.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-176">The **Detail** column is split into multiple columns.</span></span> <span data-ttu-id="8d7e0-177">Jede neue Spalte heißt **Detail. 1**, **Detail. 2**, **Detail. 3**usw.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-177">Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on.</span></span> <span data-ttu-id="8d7e0-178">Sie werden feststellen, dass die Werte in jeder Zelle in den Spalten **Details. n** dem Namen der Eigenschaft vorangestellt werden. beispielsweise **Operation: sharingset**, **Operation: SharingInvitationAccepted**und **Operation: SharingInvitationCreated**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-178">You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![Die Detail Spalte wird in mehrere Spalten aufgeteilt, eine für jede Eigenschaft.](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="8d7e0-180">Klicken Sie auf der Registerkarte **Datei** auf \*\*Laden schließen &amp; \*\* , um den Abfrage-Editor zu schließen und die Datei in einer Excel-Arbeitsmappe zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="8d7e0-181">Im nächsten Schritt wird die Datei so gefiltert, dass nur die **freigabeset** -und **SharingInvitationCreated** -Ereignisse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="8d7e0-182">Wechseln Sie zur Registerkarte **Start** , und wählen Sie dann die Spalte **Aktion** aus.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="8d7e0-183">Deaktivieren Sie in der Dropdownliste **Sortier &amp; Filter** alle Optionen, und wählen Sie dann **freigabeset** und **SharingInvitationCreated**aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="8d7e0-184">Excel zeigt die Zeilen für die **freigabeset** -und **SharingInvitationCreated** -Ereignisse an.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="8d7e0-185">Wechseln Sie zu der Spalte mit dem Namen **Detail. 17** (oder einer Spalte, die die **TargetUserOrGroupType** -Eigenschaft enthält), und wählen Sie Sie aus.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="8d7e0-186">Deaktivieren Sie in der Dropdownliste **Sortier &amp; Filter** alle Optionen, und wählen Sie dann **TargetUserOrGroupType: Gast**aus, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="8d7e0-187">Excel zeigt nun die Zeilen für **SharingInvitationCreated** -und **Sharing** -Ereignisse an, wobei sich der Zielbenutzer außerhalb Ihrer Organisation befindet, da externe Benutzer durch den Wert **TargetUserOrGroupType: Guest**identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="8d7e0-188">In der folgenden Tabelle sind alle Benutzer in der Organisation aufgeführt, die in einem bestimmten Zeitraum Ressourcen für einen Gastbenutzer freigegeben haben.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Freigabe Ereignisse in Office 365-Überwachungsprotokoll](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="8d7e0-190">Obwohl es nicht in der vorherigen Tabelle enthalten ist, gibt die **Detail. 10** -Spalte (oder die Spalte mit der **objectID** -Eigenschaft) die Ressource an, die für den Zielbenutzer freigegeben wurde; Beispiel `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="8d7e0-191">Wenn Sie ermitteln möchten, wann ein Gastbenutzer tatsächlich Berechtigungen für den Zugriff auf eine Ressource zugewiesen hat (im Gegensatz zu den Ressourcen, die für diesen freigegeben wurden), wiederholen Sie die Schritte 10, 11 und 12, und Filtern Sie nach dem **SharingInvitationAccepted** und dem freigabeset. \*\* \*\*Ereignisse in Schritt 10.</span><span class="sxs-lookup"><span data-stu-id="8d7e0-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
