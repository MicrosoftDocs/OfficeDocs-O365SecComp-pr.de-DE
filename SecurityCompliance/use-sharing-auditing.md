---
title: Verwenden Sie die Freigabe der Überwachung in das Überwachungsprotokoll Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 2/13/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- BCS160
- MET150
ms.assetid: 50bbf89f-7870-4c2a-ae14-42635e0cfc01
description: 'Die Freigabe ist eine Aktivität in SharePoint Online und OneDrive für Unternehmen. Administratoren können nun Freigabe Überwachung in der Office 365-Überwachungsprotokoll um zu bestimmen, wie gemeinsame Nutzung in ihrer Organisation verwendet wird. '
ms.openlocfilehash: 511f8b0e61d450659d78177d5b87fac9ee636cd4
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529561"
---
# <a name="use-sharing-auditing-in-the-office-365-audit-log"></a><span data-ttu-id="6a4d1-104">Verwenden Sie die Freigabe der Überwachung in das Überwachungsprotokoll Office 365</span><span class="sxs-lookup"><span data-stu-id="6a4d1-104">Use sharing auditing in the Office 365 audit log</span></span>

<span data-ttu-id="6a4d1-p102">Die Freigabe ist eine Aktivität in SharePoint Online und OneDrive für Unternehmen, und es in Office 365-Organisationen weit verbreitet ist. Administratoren können nun Freigabe Überwachung in der Office 365-Überwachungsprotokoll um zu bestimmen, wie gemeinsame Nutzung in ihrer Organisation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p102">Sharing is a key activity in SharePoint Online and OneDrive for Business, and it's widely used in Office 365 organizations. Administrators can now use sharing auditing in the Office 365 audit log to determine how sharing is being used in their organization.</span></span> 
  
## <a name="the-sharepoint-sharing-schema"></a><span data-ttu-id="6a4d1-107">Das Freigeben von SharePoint-schema</span><span class="sxs-lookup"><span data-stu-id="6a4d1-107">The SharePoint Sharing schema</span></span>

<span data-ttu-id="6a4d1-p103">Anwendungsfreigabe-Ereignisse (außer Freigaberichtlinie und Freigabe link Ereignisse) unterscheiden sich von Datei und Ordner-bezogenen Ereignisse in eine primäre Möglichkeit: ein Benutzer ist einer Aktion, die auf einen anderen Benutzer einige auswirkt. Beispielsweise erhalten Benutzer A Benutzer B Zugriff auf eine Datei. In diesem Beispiel Benutzer A ist der *Benutzer fungiert* und Benutzer B den *Zielbenutzer*. In der SharePoint-Datei Schema wirkt sich auf die handelnden Aktion des Benutzers nur die Datei selbst. Wenn Benutzer A öffnet eine Datei, die nur im Ereignis **FileAccessed** erforderlichen Informationen der handelnden Benutzer hat. Um diesen Unterschied zu beheben, ist es ein separates Schema, *Freigeben von SharePoint-Schema*, das Weitere Informationen zum Freigeben von Ereignissen erfasst wird aufgerufen. Dadurch wird sichergestellt, dass Administratoren über einen besseren Einblick in die, die eine Ressource freigegeben und der Benutzer die Ressource freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p103">Sharing events (excluding sharing policy and sharing link events) are different from file- and folder-related events in one primary way: one user is taking an action that has some effect on another user. For example, User A gives User B access to a file. In this example, User A is the  *acting user*  and User B is the  *target user*. In the SharePoint File schema, the acting user's action only affects the file itself. When User A opens a file, the only information needed in the **FileAccessed** event is the acting user. To address this difference, there is a separate schema, called the  *SharePoint Sharing schema*, that captures more information about sharing events. This ensures that administrators have more insight into who shared a resource and the user the resource was shared with.</span></span> 
  
<span data-ttu-id="6a4d1-115">Das Schema für die Freigabe bietet zwei weitere Felder im Zusammenhang mit der Freigabe von Ereignissen in das Überwachungsprotokoll geschrieben:</span><span class="sxs-lookup"><span data-stu-id="6a4d1-115">The Sharing schema provides two additional fields in the audit log related to sharing events:</span></span> 
  
- <span data-ttu-id="6a4d1-116">**TargetUserOrGroupName** - speichert die UPN oder den Namen des Zielbenutzers oder der Gruppe, dass eine Ressource für (im vorherigen Beispiel Benutzer B) freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-116">**TargetUserOrGroupName** - Stores the UPN or name of the target user or group that a resource was shared with (User B in the previous example).</span></span> 
    
- <span data-ttu-id="6a4d1-117">**TargetUserOrGroupType** - bestimmt, ob der Zielbenutzer oder die Gruppe ein Mitglied, Gast, Gruppe oder Partner ist.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-117">**TargetUserOrGroupType** - Identifies whether the target user or group is a Member, Guest, Group, or Partner.</span></span> 
    
<span data-ttu-id="6a4d1-118">Diese beiden Felder, zusätzlich zu anderen Eigenschaften aus der Office 365 audit Log Schema wie Benutzer-, Vorgang und Datum umfassende über *welche* Benutzer shared *welche* Ressourcen mit *denen* und zu welchen *Zeitpunkten*informieren können.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-118">These two fields, in addition to other properties from the Office 365 audit log schema such as User, Operation, and Date can tell the full story about  *which*  user shared  *what*  resource with  *whom*  and  *when*.</span></span> 
  
<span data-ttu-id="6a4d1-p104">Es gibt eine andere Schemaeigenschaft, die die Freigabe Story wichtig ist. Die **EventData** -Eigenschaft speichert zusätzliche Informationen über die Freigabe von Ereignissen. Beispielsweise wenn ein Benutzer eine Website mit einem anderen Benutzer gemeinsam, dies erfolgt durch den Target-Benutzer einer SharePoint-Gruppe hinzugefügt. Die **EventData** -Eigenschaft erfasst diese zusätzlichen Informationen um Kontext für Administratoren bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p104">There's another schema property that's important to the sharing story. The **EventData** property stores additional information about sharing events. For example, when a user shares a site with another user, this is accomplished by adding the target user to a SharePoint group. The **EventData** property captures this additional information to provide context for administrators.</span></span> 

## <a name="the-sharepoint-sharing-model-and-sharing-events"></a><span data-ttu-id="6a4d1-123">Die SharePoint-Objektmodell Freigabe und Freigeben von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="6a4d1-123">The SharePoint Sharing model and sharing events</span></span>

<span data-ttu-id="6a4d1-p105">Freigabe wird durch drei separate Ereignisse tatsächlich definiert: **SharingSet**, **SharingInvitationCreated**und **SharingInvitaitonAccepted**. Hier ist der Workflow für Ereignisse wie Freigabe im Überwachungsprotokoll Office 365 angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p105">Sharing is actually defined by three separate events: **SharingSet**, **SharingInvitationCreated**, and **SharingInvitaitonAccepted**. Here's the work flow for how sharing events are logged in the Office 365 audit log.</span></span> 
  
![Flussdiagramm der Funktionsweise der Freigabe der Überwachung](media/d83dd40f-919b-484f-bfd6-5dc8de31bff6.png)
  
<span data-ttu-id="6a4d1-p106">Wenn ein Benutzer (handelnden Benutzer) Freigeben einer Ressource mit einem anderen Benutzer (Zielbenutzer) möchte, überprüft SharePoint (oder OneDrive für Unternehmen) zuerst, wenn die e-Mail-Adresse des Zielbenutzers bereits ein Benutzerkonto im Verzeichnis der Organisation zugeordnet ist. Wenn die Zielbenutzer im Verzeichnis der Organisation ist, führt SharePoint Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p106">When a user (the acting user) wants to share a resource with another user (the target user), SharePoint (or OneDrive for Business) first checks if the email address of the target user is already associated with a user account in the organization's directory. If the target user is in the organization's directory, SharePoint does the following:</span></span>
  
-  <span data-ttu-id="6a4d1-129">Sofort weist die Ziel von Benutzerberechtigungen für die Ressource zugreifen.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-129">Immediately assigns the target user permissions to access the resource.</span></span> 
    
- <span data-ttu-id="6a4d1-130">Sendet eine Freigabe Benachrichtigung an die e-Mail-Adresse des Zielbenutzers.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-130">Sends a sharing notification to the email address of the target user.</span></span>
    
- <span data-ttu-id="6a4d1-131">Ein Ereignis **SharingSet** protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-131">Logs a **SharingSet** event.</span></span> 
    
 <span data-ttu-id="6a4d1-132">Wenn ein Benutzerkonto für die Zielbenutzer im Verzeichnis der Organisation nicht ist, führt SharePoint Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="6a4d1-132">If a user account for the target user isn't in the organization's directory, SharePoint does the following:</span></span> 
  
- <span data-ttu-id="6a4d1-133">Erstellt eine Einladung zur Freigabe, und sendet ihn an die e-Mail-Adresse des Zielbenutzers.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-133">Creates a sharing invitation and sends it to the email address of the target user.</span></span>
    
- <span data-ttu-id="6a4d1-134">Ein Ereignis **SharingInvitationCreated** protokolliert.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-134">Logs a **SharingInvitationCreated** event.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="6a4d1-135">Das Ereignis **SharingInvitationCreated** ist am besten immer zugeordnet, mit externen oder Gast freigeben, wenn der Zielbenutzer Zugriff auf die Ressource hat, die gemeinsam genutzt wurde.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-135">The **SharingInvitationCreated** event is most always associated with external or guest sharing when the target user doesn't have access to the resource that was shared.</span></span> 
  
<span data-ttu-id="6a4d1-p107">Wenn der Zielbenutzer die Einladung zur Freigabe annimmt, die an sie gesendet wurde (durch Klicken auf den Link in der Einladung), SharePoint meldet ein **SharingInvitationAccepted** -Ereignis und weist die Ziel von Benutzerberechtigungen für die Ressource zugreifen. Weitere Informationen zu den Zielbenutzer wird auch protokolliert, wie die Identität des Benutzers, der die Einladung gesendet wurde und der Benutzer, der tatsächlich die Einladung annehmen. In einigen Fällen können diese Benutzer (oder die e-Mail-Adressen) abweichen.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p107">When the target user accepts the sharing invitation that's sent to them (by clicking the link in the invitation), SharePoint logs a **SharingInvitationAccepted** event and assigns the target user permissions to access the resource. Additional information about the target user is also logged, such as the identity of the user that the invitation was sent to and the user who actually accepted the invitation. In some case, these users (or email addresses) might be different.</span></span> 
  

  
## <a name="how-to-identify-resources-shared-with-external-users"></a><span data-ttu-id="6a4d1-139">So identifizieren Sie Ressourcen mit externen Benutzern</span><span class="sxs-lookup"><span data-stu-id="6a4d1-139">How to identify resources shared with external users</span></span>

<span data-ttu-id="6a4d1-p108">Eine allgemeine Anforderung für Administratoren wird eine Liste aller Ressourcen erstellen, die mit Benutzern außerhalb der Organisation freigegeben wurden. Mithilfe der Freigabe in Office 365 Überwachung können Administratoren diese Liste jetzt generieren. Hier ist wie.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p108">A common requirement for administrators is creating a list of all resources that have been shared with users outside of the organization. By using sharing auditing in Office 365, administrators can now generate this list. Here's how.</span></span>
  
### <a name="step-1-search-for-sharing-events-and-export-the-results-to-a-csv-file"></a><span data-ttu-id="6a4d1-143">Schritt 1: Freigeben von Ereignissen suchen und die Ergebnisse in einer CSV-Datei exportieren</span><span class="sxs-lookup"><span data-stu-id="6a4d1-143">Step 1: Search for sharing events and export the results to a CSV file</span></span>

<span data-ttu-id="6a4d1-p109">Im erste Schritt wird das Überwachungsprotokoll Office 365 für die Freigabe von Ereignissen gesucht. Weitere Informationen (einschließlich der erforderlichen Berechtigungen) zur Suche im Überwachungsprotokolls finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p109">The first step is to search the Office 365 audit log for sharing events. For more details (including the required permissions) about searching the audit log, see [Search the audit log in the Office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).</span></span>
  
1. <span data-ttu-id="6a4d1-146">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="6a4d1-146">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="6a4d1-147">Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-147">Sign in to Office 365 using your work or school account.</span></span>
    
3. <span data-ttu-id="6a4d1-148">Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung**, und klicken Sie auf **Audit Log suchen**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-148">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation**, and then click **Audit log search**.</span></span>
    
    <span data-ttu-id="6a4d1-149">**Audit Log** Suchseite wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-149">The **Audit log search** page is displayed.</span></span> 
    
4. <span data-ttu-id="6a4d1-150">Klicken Sie auf **Freigabe Aktivitäten** aus, die nur für die Freigabe von Ereignissen suchen, klicken Sie unter **Aktivitäten**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-150">Under **Activities**, click **Sharing activities** to search only for sharing events.</span></span> 
    
    ![Wählen Sie unter Aktivitäten Freigabe Aktivitäten](media/46bb25b7-1eb2-4adf-903a-cc9ab58639f9.png)
  
5.  <span data-ttu-id="6a4d1-152">Wählen Sie einen Bereich für Datum und Uhrzeit, die Freigabe Ereignisse zu erhalten, die innerhalb dieses Zeitraums aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-152">Select a date and time range to find the sharing events that occurred within that period.</span></span> 
    
6. <span data-ttu-id="6a4d1-153">Klicken Sie auf **Suchen** , um die Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-153">Click **Search** to run the search.</span></span> 
    
7. <span data-ttu-id="6a4d1-154">Wenn die Suche abgeschlossen ist ausgeführt werden und die Ergebnisse angezeigt werden, klicken Sie auf **Ergebnisse exportieren** \> **alle Ergebnisse herunterladen**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-154">When the search is finished running and the results are displayed , click **Export results** \> **Download all results**.</span></span>
    
    <span data-ttu-id="6a4d1-155">Nachdem Sie die Export-Option auswählen, wird eine Meldung am unteren Rand des Fensters angezeigt, die Sie zum Öffnen oder speichern die CSV-Datei auffordert.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-155">After you select the export option, a message is displayed at the bottom of the window that prompts you to open or save the CSV file.</span></span>
    
8. <span data-ttu-id="6a4d1-156">Klicken Sie auf **Speichern** \> **Speichern unter** , und speichern Sie die CSV-Datei in einen Ordner auf Ihrem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-156">Click **Save** \> **Save as** and save the CSV file to a folder on your local computer.</span></span> 
    

  
### <a name="step-2-filter-the-csv-file-for-resources-shared-with-external-users"></a><span data-ttu-id="6a4d1-157">Schritt 2: Filtern der CSV-Datei für Ressourcen mit externen Benutzern</span><span class="sxs-lookup"><span data-stu-id="6a4d1-157">Step 2: Filter the CSV file for resources shared with external users</span></span>

<span data-ttu-id="6a4d1-p110">Der nächste Schritt besteht im CSV-Format für die Ereignisse **SharingSet** und **SharingInvitationCreated** filtern und Anzeigen dieser Ereignisse wobei **Gast**ist die **TargetUserOrGroupType** -Eigenschaft. Verwenden Sie die Abfrage Power-Funktion in Excel dazu. Das folgende Verfahren wird in Excel 2016 ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p110">The next step is to filter the CSV for the **SharingSet** and **SharingInvitationCreated** events, and to display those events where the **TargetUserOrGroupType** property is **Guest**. You'll use the Power Query feature in Excel to do this. The following procedure is performed in Excel 2016.</span></span> 
  
1. <span data-ttu-id="6a4d1-161">Öffnen Sie in Excel 2016 eine leere Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-161">In Excel 2016, open a blank workbook.</span></span>
    
2. <span data-ttu-id="6a4d1-162">Klicken Sie auf die Registerkarte **Daten**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-162">Click the **Data** tab.</span></span> 
    
3. <span data-ttu-id="6a4d1-163">Klicken Sie auf **Neue Abfrage** \> **aus Datei** \> **CSV aus**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-163">Click **New Query** \> **From file** \> **From CSV**.</span></span>
    
    ![Wählen Sie auf der Registerkarte Daten neue Abfrage, wählen Sie aus der Datei, und wählen Sie dann aus der CSV](media/5170ab34-b449-40ea-bd3f-f1432c1c5973.png)
  
4. <span data-ttu-id="6a4d1-165">Öffnen Sie die CSV-Datei, die Sie heruntergeladen haben, in Schritt 1.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-165">Open the CSV file that you downloaded in Step 1.</span></span>
    
    <span data-ttu-id="6a4d1-p111">Die CSV-Datei wird im Abfrage-Editor geöffnet. Beachten Sie, dass es vier Spalten: **Zeit**, **Benutzer**, **Aktion**und **Details**. Die **Detail** -Spalte ist ein Feld mit mehreren Eigenschaften. Im nächste Schritt wird eine neue Spalte für die einzelnen Eigenschaften in der Spalte **Details** zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p111">The CSV file is opened in the Query Editor. Note that there are four columns: **Time**, **User**, **Action**, and **Detail**. The **Detail** column is a multi-property field. The next step is to create a new column for each of the properties in the **Detail** column.</span></span> 
    
5. <span data-ttu-id="6a4d1-170">Wählen Sie die Spalte **Details** , und klicken Sie dann auf der Registerkarte **Start** auf **Geteilte Spalte** \> **Durch Trennzeichen**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-170">Select the **Detail** column, and then on the **Home** tab, click **Split Column** \> **By Delimiter**.</span></span>
    
    ![Klicken Sie auf der Registerkarte Start auf geteilte Spalte, und klicken Sie dann auf durch Trennzeichen](media/aeb503e8-565b-42ea-91e2-9f127a74c00c.png)
  
6. <span data-ttu-id="6a4d1-172">Klicken Sie im Fenster **Geteilte Spalte durch Trennzeichen** folgendermaßen Sie vor:</span><span class="sxs-lookup"><span data-stu-id="6a4d1-172">In the **Split Column by Delimiter** window, do the following:</span></span> 
    
      - <span data-ttu-id="6a4d1-173">Wählen Sie unter **Wählen Sie aus, oder geben Sie als Trennzeichen** **Komma**ein.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-173">Under **Select or enter delimiter**, select **Comma**.</span></span>
    
      - <span data-ttu-id="6a4d1-174">Wählen Sie unter **Teilen** **bei jedem Vorkommen von Trennzeichen**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-174">Under **Split**, select **At each occurrence of the delimiter**.</span></span>
    
7. <span data-ttu-id="6a4d1-175">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-175">Click **OK**.</span></span>
    
    <span data-ttu-id="6a4d1-p112">Die **Detail** -Spalte wird in mehreren Spalten aufgeteilt. Jede neue Spalte heißt **Detail.1**, **Detail.2**, **Detail.3**und So weiter. Sie sehen, dass die Werte in jeder Zelle in den Spalten **Detail.n** mit dem Namen der Eigenschaft als Präfix vorangestellt ist; Angenommen, **Vorgang: SharingSet**, **Vorgang: SharingInvitationAccepted**und **Vorgang: SharingInvitationCreated**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-p112">The **Detail** column is split into multiple columns. Each new column is named **Detail.1**, **Detail.2**, **Detail.3**, and so on. You'll notice the values in each cell in the **Detail.n** columns are prefixed with the name of the property; for example, **Operation:SharingSet**, **Operation:SharingInvitationAccepted**, and **Operation:SharingInvitationCreated**.</span></span>
    
    ![Die Detail-Spalte wird in mehreren Spalten für jede Eigenschaft aufgeteilt.](media/4b104ead-0313-4bd4-b2a9-f143ccb378ac.png)
  
8. <span data-ttu-id="6a4d1-180">Klicken Sie auf der Registerkarte **Datei** auf **Schließen &amp; Load** schließen Sie den Abfrage-Editor, und öffnen Sie die Datei in einer Excel-Arbeitsmappe.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-180">On the **File** tab, click **Close &amp; Load** to close the Query Editor and open the file in an Excel workbook.</span></span> 
    
    <span data-ttu-id="6a4d1-181">Im nächste Schritt ist zum Filtern der Datei, um nur die Ereignisse **SharingSet** und **SharingInvitationCreated** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-181">The next step is to filter the file to only display the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
9. <span data-ttu-id="6a4d1-182">Wechseln Sie auf der Registerkarte **Start** , und wählen Sie dann aus der Spalte **Aktion** .</span><span class="sxs-lookup"><span data-stu-id="6a4d1-182">Go to the **Home** tab, and then select the **Action** column.</span></span> 
    
10. <span data-ttu-id="6a4d1-183">In der **sortieren &amp; Filter** Dropdown-Listenfeld, löschen Sie alle ausgewählten Optionen, klicken Sie dann wählen **SharingSet** und **SharingInvitationCreated**, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-183">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **SharingSet** and **SharingInvitationCreated**, and click **OK**.</span></span>
    
    <span data-ttu-id="6a4d1-184">Excel zeigt die Zeilen für die Ereignisse **SharingSet** und **SharingInvitationCreated** .</span><span class="sxs-lookup"><span data-stu-id="6a4d1-184">Excel displays the rows for the **SharingSet** and **SharingInvitationCreated** events.</span></span> 
    
11. <span data-ttu-id="6a4d1-185">Besuchen Sie die Spalte mit dem Namen **Detail.17** (oder Spalte die **TargetUserOrGroupType** -Eigenschaft enthält), und wählen Sie sie aus.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-185">Go to the column named **Detail.17** (or whichever column contains the **TargetUserOrGroupType** property) and select it.</span></span> 
    
12. <span data-ttu-id="6a4d1-186">In der **sortieren &amp; Filter** Dropdown-Listenfeld, löschen Sie alle ausgewählten Optionen, wählen Sie **TargetUserOrGroupType:Guest**, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-186">In the **Sort &amp; Filter** drop-down list, clear all selections, then select **TargetUserOrGroupType:Guest**, and click **OK**.</span></span>
    
    <span data-ttu-id="6a4d1-187">Excel zeigt jetzt die Zeilen für **SharingInvitationCreated** und **SharingSet** -Ereignisse und den Zielbenutzer außerhalb Ihrer Organisation, da externe Benutzer den Wert **TargetUserOrGroupType:Guest**identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-187">Now Excel displays the rows for **SharingInvitationCreated** and **SharingSet** events AND where the target user is outside of your organization, because external users are identified by the value **TargetUserOrGroupType:Guest**.</span></span> 
    
<span data-ttu-id="6a4d1-188">Die folgende Tabelle zeigt alle Benutzer in der Organisation, die freigegebenen Ressourcen mit einem Gäste Benutzer innerhalb eines angegebenen Zeitraums.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-188">The following table shows all users in the organization who shared resources with a guest user within a specified date range.</span></span>
  
![Überwachungsprotokoll Sharing Ereignisse in Office 365](media/0e0ecbe3-c794-4ca6-a2ca-63478fb3bb34.png)
  
<span data-ttu-id="6a4d1-190">Obwohl es nicht in der vorherigen Tabelle enthalten ist, identifiziert der Spalte **Detail.10** (oder Spalte die **ObjectId** -Eigenschaft enthält) Ressource, die für die Zielbenutzer freigegeben wurde; beispielsweise `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-190">Although it's not included in the previous table, the **Detail.10** column (or whichever column contains the **ObjectId** property) identifies the resource that was shared with the target user; for example  `ObjectId:https:\/\/contoso-my.sharepoint.com\/personal\/sarad_contoso_com\/Documents\/Southwater Proposal.docx`.</span></span>
  
> [!TIP]
> <span data-ttu-id="6a4d1-191">Wenn Sie bestimmen möchten wenn Gast wurde tatsächlich zugewiesen Berechtigungen zum Zugriff auf eine Ressource (also nicht nur die Ressourcen, wo sie freigegeben), wiederholen Sie die Schritte 10, 11 und 12 und filter für die **SharingInvitationAccepted** und **SharingSet **Ereignisse in Schritt 10.</span><span class="sxs-lookup"><span data-stu-id="6a4d1-191">If you want to identify when a guest user was actually assigned permissions to access a resource (as opposed to just the resources that where shared with them), repeat Steps 10, 11, and 12, and filter on the **SharingInvitationAccepted** and **SharingSet** events in Step 10.</span></span> 
