---
title: Schützen von SharePoint Online-Dateien mit Office 365-Bezeichnungen und Verhindern von Datenverlust
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/12/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-solutions
localization_priority: Priority
search.appverid:
- MET150
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: c9f837af-8d71-4df1-a285-dedb1c5618b3
description: 'Zusammenfassung: Wenden Sie Richtlinien von Office 365-Bezeichnungen und der Verhinderung von Datenverlust (DLP) für SharePoint Online-Teamwebsites mit unterschiedlichen Ebenen des Informationsschutzes an.'
ms.openlocfilehash: fd2fedf23b4e65bd32642b8528548f8a85533051
ms.sourcegitcommit: 6ff0233b5a1a07595f8b4d55db6b1327bcaa174c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2019
ms.locfileid: "28023443"
---
# <a name="protect-sharepoint-online-files-with-office-365-labels-and-dlp"></a><span data-ttu-id="ce2ba-103">Schützen von SharePoint Online-Dateien mit Office 365-Bezeichnungen und Verhindern von Datenverlust</span><span class="sxs-lookup"><span data-stu-id="ce2ba-103">Protect SharePoint Online files with Office 365 labels and DLP</span></span>

 <span data-ttu-id="ce2ba-104">**Zusammenfassung:** Wenden Sie Richtlinien von Office 365-Bezeichnungen und der Verhinderung von Datenverlust (DLP) für SharePoint Online-Teamwebsites mit unterschiedlichen Ebenen des Informationsschutzes an.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-104">**Summary:** Apply Office 365 labels and data loss prevention (DLP) policies for SharePoint Online team sites with various levels of information protection.</span></span>
  
<span data-ttu-id="ce2ba-p101">Führen Sie die in diesem Artikel aufgeführten Schritte durch, um Office 365-Bezeichnungen und DLP-Richtlinien für SharePoint Online-Teamwebsites mit Basisschutz, Schutz vertraulicher und streng vertraulicher Daten zu entwerfen und bereitzustellen. Weitere Informationen zu diesen drei Ebenen des Schutzes finden Sie unter [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="ce2ba-p101">Use the steps in this article to design and deploy Office 365 labels and DLP policies for baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="how-this-works"></a><span data-ttu-id="ce2ba-107">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="ce2ba-107">How this works</span></span>
1. <span data-ttu-id="ce2ba-p102">Erstellen Sie die gewünschten Bezeichnungen und veröffentlichen Sie sie. Es kann bis zu 12 Stunden dauern, bis die Bezeichnungen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-p102">Create the desired labels and publish these. It can take up to 12 hours for these to be published.</span></span>
2. <span data-ttu-id="ce2ba-110">Bearbeiten Sie für die gewünschten SharePoint-Websites die Einstellungen für die Dokumentbibliothek, um eine Bezeichnung auf Elemente in der Bibliothek anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-110">For the desired SharePoint sites, edit the document library settings to apply a label to items in the library.</span></span>
3. <span data-ttu-id="ce2ba-111">Erstellen Sie DLP-Richtlinien, um Aktionen basierend auf den Bezeichnungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-111">Create DLP policies to take action based on the labels.</span></span>

<span data-ttu-id="ce2ba-p103">Wenn Benutzer ein Dokument zur Bibliothek hinzufügen, erhält das Dokument standardmäßig die zugewiesene Bezeichnung. Benutzer können die Bezeichnung bei Bedarf ändern. Wenn ein Benutzer ein Dokument außerhalb der Organisation freigibt, überprüft DLP, ob eine Bezeichnung zugewiesen ist, und ergreift entsprechende Maßnahmen, wenn eine DLP-Richtlinie der Bezeichnung entspricht. DLP prüft auch auf andere Richtlinienübereinstimmungen, wie z. B. den Schutz von Dateien mit Kreditkartennummern, wenn diese Art von Richtlinie konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-p103">When users add a document to the library, the document will receive the assigned label by default. Users can change the label, if needed. When a user shares a document outside the organization, DLP will check to see if a label is assigned and take action if a DLP policy matches the label. DLP will look for other policy matches as well, such as protecting files with credit card numbers if this type of policy is configured.</span></span> 

## <a name="office-365-labels-for-your-sharepoint-online-sites"></a><span data-ttu-id="ce2ba-116">Office 365-Bezeichnungen für Ihre SharePoint Online-Websites</span><span class="sxs-lookup"><span data-stu-id="ce2ba-116">Office 365 labels for your SharePoint Online sites</span></span>

<span data-ttu-id="ce2ba-117">Es gibt drei Phasen beim Erstellen und anschließenden Zuweisen von Office 365-Bezeichnungen zu SharePoint Online-Teamwebsites.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-117">There are three phases to creating and then assigning Office 365 labels to SharePoint Online team sites.</span></span>
  
### <a name="phase-1-determine-the-office-365-label-names"></a><span data-ttu-id="ce2ba-118">Phase 1: Bestimmen der Office 365-Bezeichnungsnamen</span><span class="sxs-lookup"><span data-stu-id="ce2ba-118">Phase 1: Determine the Office 365 label names</span></span>

<span data-ttu-id="ce2ba-p104">In dieser Phase bestimmen Sie die Namen Ihrer Office 365-Bezeichnungen für die vier Ebenen des Informationsschutzes, der auf SharePoint Online-Teamwebsites angewendet wird. Die folgende Tabelle listet die empfohlenen Namen für jede Ebene auf.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-p104">In this phase, you determine the names of your Office 365 labels for the four levels of information protection applied to SharePoint Online team sites. The following table lists the recommended names for each level.</span></span>
  
|<span data-ttu-id="ce2ba-121">**Schutzebene der SharePoint Online-Teamwebsite**</span><span class="sxs-lookup"><span data-stu-id="ce2ba-121">**SharePoint Online team site protection level**</span></span>|<span data-ttu-id="ce2ba-122">**Bezeichnungsname**</span><span class="sxs-lookup"><span data-stu-id="ce2ba-122">**Label name**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce2ba-123">Grundlegend-Öffentlich</span><span class="sxs-lookup"><span data-stu-id="ce2ba-123">Baseline-Public</span></span>  <br/> |<span data-ttu-id="ce2ba-124">Intern Öffentlich</span><span class="sxs-lookup"><span data-stu-id="ce2ba-124">Internal public</span></span>  <br/> |
|<span data-ttu-id="ce2ba-125">Grundlegend-Privat</span><span class="sxs-lookup"><span data-stu-id="ce2ba-125">Baseline-Private</span></span>  <br/> |<span data-ttu-id="ce2ba-126">Private</span><span class="sxs-lookup"><span data-stu-id="ce2ba-126">Private</span></span>  <br/> |
|<span data-ttu-id="ce2ba-127">Vertraulich</span><span class="sxs-lookup"><span data-stu-id="ce2ba-127">Sensitive</span></span>  <br/> |<span data-ttu-id="ce2ba-128">Vertraulich</span><span class="sxs-lookup"><span data-stu-id="ce2ba-128">Sensitive</span></span>  <br/> |
|<span data-ttu-id="ce2ba-129">Streng vertraulich</span><span class="sxs-lookup"><span data-stu-id="ce2ba-129">Highly Confidential</span></span>  <br/> |<span data-ttu-id="ce2ba-130">Streng vertraulich</span><span class="sxs-lookup"><span data-stu-id="ce2ba-130">Highly Confidential</span></span>  <br/> |
   
### <a name="phase-2-create-the-office-365-labels"></a><span data-ttu-id="ce2ba-131">Phase 2: Erstellen von Office 365-Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="ce2ba-131">Phase 2: Create the Office 365 labels</span></span>

<span data-ttu-id="ce2ba-132">In dieser Phase erstellen und veröffentlichen Sie Ihre bestimmten Bezeichnungen für die unterschiedlichen Ebenen des Informationsschutzes.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-132">In this phase, you create and then publish your determined labels for the different levels of information protection.</span></span>
  
<span data-ttu-id="ce2ba-133">Zum Erstellen der Bezeichnungen können Sie das Office 365 Admin Center oder Microsoft PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-133">To create the labels, you can use the Office 365 Admin center or Microsoft PowerShell.</span></span>
  
### <a name="create-office-365-labels-with-the-office-365-admin-center"></a><span data-ttu-id="ce2ba-134">Erstellen von Office 365-Bezeichnungen mit dem Office 365 Admin Center</span><span class="sxs-lookup"><span data-stu-id="ce2ba-134">Create Office 365 labels with the Office 365 Admin center</span></span>

1. <span data-ttu-id="ce2ba-p105">Melden Sie sich mit einem Konto beim Office 365-Portal an, das über die Rolle „Sicherheitsadministrator" oder Unternehmensadministrator" verfügt. Hilfe finden Sie unter [Wo kann ich mich bei Office 365 Business anmelden?](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="ce2ba-p105">Sign in to the Office 365 portal with an account that has the Security Administrator or Company Administrator role. For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="ce2ba-137">Klicken Sie auf der Registerkarte **Microsoft Office Home** auf die Kachel **Admin**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-137">From the **Microsoft Office Home** tab, click the **Admin** tile.</span></span>
    
3. <span data-ttu-id="ce2ba-138">Klicken Sie auf der neuen Registerkarte **Office Admin Center** im Browser auf **Admin Center > Security &amp; Compliance**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-138">From the new **Office Admin center** tab of your browser, click **Admin centers > Security &amp; Compliance**.</span></span>
    
4. <span data-ttu-id="ce2ba-139">Klicken Sie auf der neuen Registerkarte **Start - Security &amp; Compliance** im Browser auf **Klassifizierungen > Bezeichnungen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-139">From the new **Home - Security &amp; Compliance** tab of your browser, click **Classifications > Labels**.</span></span>
    
5. <span data-ttu-id="ce2ba-140">Klicken Sie im Bereich **Start > Bezeichnungen** auf die Registerkarte **Aufbewahrung**, und klicken Sie dann auf **Bezeichnung erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-140">From the **Home > Labels** pane, click the **Retention** tab, and then click **Create a label**.</span></span>
    
6. <span data-ttu-id="ce2ba-141">Geben Sie im Bereich zum **Benennen der Bezeichnung** den Namen für die Bezeichnung und eine Beschreibung für Administratoren und Benutzer ein, und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-141">On the **Name your label** pane, type the name of the label and a description for admins and users, and then click **Next**.</span></span>

7. <span data-ttu-id="ce2ba-142">Klicken Sie im Bereich **Bezeichnungseinstellungen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-142">On the **Label settings** pane, click **Next**.</span></span>
    
8. <span data-ttu-id="ce2ba-143">Klicken Sie im Bereich **Einstellungen überprüfen** auf **Erstellen**, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-143">On the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="ce2ba-144">Wiederholen Sie die Schritte 5 bis 8 für weitere Bezeichnungen.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-144">Repeat steps 5-8 for your additional labels.</span></span>
    
### <a name="create-office-365-labels-with-powershell"></a><span data-ttu-id="ce2ba-145">Erstellen von Office 365-Bezeichnungen mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="ce2ba-145">Create Office 365 labels with PowerShell</span></span>

1. <span data-ttu-id="ce2ba-146">[Stellen Sie mithilfe von Remote-PowerShell eine Verbindung mit dem Office 365 Security &amp; Compliance Center](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409) her, und geben Sie die Anmeldeinformationen eines Kontos an, das über die Rolle „Sicherheitsadministrator“ oder „Unternehmensadministrator“ verfügt.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-146">[Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409) and specify the credentials of an account that has the Security Administrator or Company Administrator role.</span></span>
    
2. <span data-ttu-id="ce2ba-147">Füllen Sie die Liste der Bezeichnungsnamen aus, und führen Sie dann diese Befehle an der PowerShell-Eingabeaufforderung aus:</span><span class="sxs-lookup"><span data-stu-id="ce2ba-147">Fill out the list of label names, and then run these commands at the PowerShell command prompt:</span></span>
    
  ```
  $labelNames=@(<list of label names, each enclosed in quotes and separated by commas>)
ForEach ($element in $labelNames){ New-ComplianceTag -Name $element }
  ```

### <a name="publish-your-new-labels"></a><span data-ttu-id="ce2ba-148">Veröffentlichen neuer Bezeichnungen</span><span class="sxs-lookup"><span data-stu-id="ce2ba-148">Publish your new labels</span></span>

<span data-ttu-id="ce2ba-149">Führen Sie dann diese Schritte aus, um die neuen Office 365-Bezeichnungen zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-149">Next, use these steps to publish the new Office 365 labels.</span></span>
  
1. <span data-ttu-id="ce2ba-150">Klicken Sie im Bereich **Start > Bezeichnungen** von Security &amp; Compliance Center auf die Registerkarte **Aufbewahrung**, und klicken Sie dann auf **Bezeichnungen veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-150">From the **Home > Labels** pane of the Security &amp; Compliance Center, click the **Retention** tab, and then click **Publish labels**.</span></span>
    
2. <span data-ttu-id="ce2ba-151">Klicken Sie im Bereich **Zu veröffentlichende Bezeichnungen wählen** auf **Zu veröffentlichende Bezeichnungen wählen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-151">On the **Choose labels to publish** pane, click **Choose labels to publish**.</span></span>
    
3. <span data-ttu-id="ce2ba-152">Klicken Sie im Bereich **Choose labels** (Bezeichnungen auswählen) auf **Hinzufügen**, wählen Sie alle vier Bezeichnungen aus.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-152">On the **Choose labels** pane, click **Add** and select all four labels.</span></span>
    
4. <span data-ttu-id="ce2ba-153">Klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-153">Click **Done**.</span></span>
    
5. <span data-ttu-id="ce2ba-154">Klicken Sie im Bereich **Zu veröffentlichende Bezeichnungen wählen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-154">On the **Choose labels to publish** pane, click **Next**.</span></span>
    
6. <span data-ttu-id="ce2ba-155">Klicken Sie im Bereich **Speicherorte auswählen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-155">On the **Choose locations** pane, click **Next**.</span></span>
    
7. <span data-ttu-id="ce2ba-156">Geben Sie im Bereich zum **Benennen der Richtlinie** einen Namen für den Bezeichnungssatz unter **Name** ein, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-156">On the **Name your policy** pane, type a name for your set of labels in **Name**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="ce2ba-157">Klicken Sie im Bereich **Einstellungen überprüfen** auf **Bezeichnungen veröffentlichen**, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-157">On the **Review your settings** pane, click **Publish labels**, and then click **Close**.</span></span>

    
### <a name="phase-3-apply-the-office-365-labels-to-your-sharepoint-online-sites"></a><span data-ttu-id="ce2ba-158">Phase 3: Anwenden von Office 365-Bezeichnungen auf Ihre SharePoint-Websites</span><span class="sxs-lookup"><span data-stu-id="ce2ba-158">Phase 3: Apply the Office 365 labels to your SharePoint Online sites</span></span>

<span data-ttu-id="ce2ba-159">Verwenden Sie die Schritte, um die Office 365-Bezeichnungen auf die Dokumentordner Ihrer SharePoint Online-Teamwebsites anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-159">Use these steps to apply the Office 365 labels to the documents folders of your SharePoint Online team sites.</span></span>
  
1. <span data-ttu-id="ce2ba-160">Klicken Sie auf der Registerkarte **Microsoft Office Home** des Browsers auf die Kachel **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-160">From the **Microsoft Office Home** tab of your browser, click the **SharePoint** tile.</span></span>
    
2. <span data-ttu-id="ce2ba-161">Klicken Sie auf der neuen Registerkarte **SharePoint** in Ihrem Browser auf eine Website, der eine Office 365-Bezeichnung zugewiesen werden muss.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-161">On the new **SharePoint** tab in your browser, click a site that needs an Office 365 label assigned.</span></span>
    
3. <span data-ttu-id="ce2ba-162">Klicken Sie auf der Registerkarte für die SharePoint-Website Ihres Browsers auf **Dokumente**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-162">In the new SharePoint site tab of your browser, click **Documents**.</span></span>
    
4. <span data-ttu-id="ce2ba-163">Klicken Sie auf das Symbol „Einstellungen“, und klicken Sie dann auf **Bibliothekseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-163">Click the settings icon, and then click **Library settings**.</span></span>
    
5. <span data-ttu-id="ce2ba-164">Klicken Sie unter **Berechtigungen und Verwaltung** auf **Bezeichnung auf Elemente in dieser Bibliothek anwenden**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-164">Under **Permissions and Management**, click **Apply label to items in this library**.</span></span>
    
6. <span data-ttu-id="ce2ba-165">Wählen Sie unter **Einstellungen – Bezeichnung anwenden** die entsprechende Bezeichnung, und klicken Sie dann auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-165">In **Settings-Apply Label**, select the appropriate label, and then click **Save**.</span></span>
    
7. <span data-ttu-id="ce2ba-166">Schließen Sie die Registerkarte für die SharePoint Online-Website.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-166">Close the tab for the SharePoint Online site.</span></span>
    
8. <span data-ttu-id="ce2ba-167">Wiederholen Sie die Schritte 3 bis 8, um Ihren zusätzlichen SharePoint Online-Websites Office 365-Bezeichnungen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-167">Repeat steps 3-8 to assign Office 365 labels to your additional SharePoint Online sites.</span></span>
    
<span data-ttu-id="ce2ba-168">Nachfolgend sehen Sie die daraus resultierende Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-168">Here is your resulting configuration.</span></span>
  
![Office 365-Bezeichnungen für die vier Arten von SharePoint Online-Teamwebsites.](media/e0a4fdd2-1c30-4d93-8af4-a6f0c6c29966.png)
  
## <a name="dlp-policies-for-your-sharepoint-online-sites"></a><span data-ttu-id="ce2ba-170">DLP-Richtlinien für Ihre SharePoint Online-Websites</span><span class="sxs-lookup"><span data-stu-id="ce2ba-170">DLP policies for your SharePoint Online sites</span></span>

<span data-ttu-id="ce2ba-171">Gehen Sie wie folgt vor, um eine DLP-Richtlinie zu konfigurieren, die Benutzer benachrichtigt, wenn sie ein Dokument auf einer vertraulichen SharePoint Online-Teamwebsite mit Benutzern außerhalb der Organisation teilen.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-171">Use these steps to configure a DLP policy that notifies users when they share a document on a SharePoint Online sensitive team site outside the organization.</span></span>

1. <span data-ttu-id="ce2ba-172">Klicken Sie auf der Registerkarte **Microsoft Office Home** auf die Kachel **Admin**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-172">From the **Microsoft Office Home** tab, click the **Admin** tile.</span></span>
    
2. <span data-ttu-id="ce2ba-173">Klicken Sie auf der neuen Registerkarte **Office Admin Center** im Browser auf **Admin Center > Security &amp; Compliance**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-173">From the new **Office Admin center** tab of your browser, click **Admin centers > Security &amp; Compliance**.</span></span>
    
3. <span data-ttu-id="ce2ba-174">Klicken Sie auf der Registerkarte **Security &amp; Compliance** in Ihrem Browser auf **Verhinderung von Datenverlust > Richtlinie**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-174">On the new **Security &amp; Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>
    
4. <span data-ttu-id="ce2ba-175">Klicken Sie im Bereich **Verhinderung von Datenverlust** auf **+ Richtlinie erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-175">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>
    
5. <span data-ttu-id="ce2ba-176">Klicken Sie im Bereich **Mit einer Vorlage beginnen oder eine benutzerdefinierte Richtlinie erstellen** auf **Benutzerdefiniert**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-176">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="ce2ba-177">Geben Sie im Bereich **Benennen Sie Ihre Richtlinie** unter **Name** den Namen der DLP-Richtlinie für die Vertraulichkeitsebene ein, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-177">In the **Name your policy** pane, type the name for the sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="ce2ba-178">Klicken Sie im Bereich **Speicherorte auswählen** auf **Bestimmte Speicherorte auswählen**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-178">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="ce2ba-179">Deaktivieren Sie in der Liste der Speicherorte **Exchange-E-Mail** und **OneDrive-Konten**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-179">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="ce2ba-180">Klicken Sie im Bereich **Anpassen des zu schützenden Inhaltstyps** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-180">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="ce2ba-181">In der **wählen Sie die Typen der Inhalte zum Schutz** Bereich, klicken Sie auf **hinzufügen** im Dropdown-Listenfeld, und klicken Sie dann auf **Etiketten**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-181">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>
    
10. <span data-ttu-id="ce2ba-182">Klicken Sie im Bereich **Bezeichnungen** auf **+ Hinzufügen**, wählen Sie die Bezeichnung **Vertraulich** aus, klicken Sie auf **Hinzufügen**, und klicken Sie dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-182">In the **Labels** pane, click **+ Add**, select the **Sensitive** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="ce2ba-183">Klicken Sie im Bereich **Typen des zu schützenden Inhalts auswählen** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-183">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="ce2ba-184">Klicken Sie im Bereich **Anpassen des zu schützenden Inhaltstyps** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-184">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>

13. <span data-ttu-id="ce2ba-185">Klicken Sie im Bereich **Was möchten Sie tun, wenn vertrauliche Informationen erkannt werden?** auf **Richtlinientipptext anpassen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-185">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="ce2ba-186">Klicken Sie im Bereich **Richtlinentipps und E-Mail-Benachrichtigungen anpassen** auf **Richtlinientipptext anpassen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-186">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="ce2ba-187">Geben oder fügen Sie in das Textfeld einen der folgenden Tipps ein, abhängig davon, ob Sie Azure Information Protection zum Schutz streng vertraulicher Dateien implementiert haben:</span><span class="sxs-lookup"><span data-stu-id="ce2ba-187">In the text box, type or paste in one of the following tips, depending on if you implemented Azure Information Protection to protect highly confidential files:</span></span>
    
  - <span data-ttu-id="ce2ba-p106">Wenn Sie eine Datei für einen Benutzer außerhalb der Organisation freigeben möchten, laden Sie die Datei herunter, und öffnen Sie sie. Klicken Sie auf „Datei“ > „Dokument schützen“ > „Mit Kennwort verschlüsseln“, und geben Sie dann ein sicheres Kennwort ein. Senden Sie das Kennwort in einer separaten E-Mail oder auf andere Weise.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-p106">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
  - <span data-ttu-id="ce2ba-p107">Streng vertrauliche Dateien werden durch Verschlüsselung geschützt. Nur externe Benutzer, die Berechtigungen für diese Dateien von Ihrer IT-Abteilung erhalten haben, können diese lesen.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-p107">Highly confidential files are protected with encryption. Only external users who are granted permissions to these files by your IT department can read them.</span></span>
    
    <span data-ttu-id="ce2ba-193">Sie können auch einen eigenen Tipp in Bezug auf die Richtlinie eingeben oder einfügen, der den Benutzern erläutert, wie sie Dateien außerhalb der Organisation freigeben.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-193">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="ce2ba-194">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-194">Click **OK**.</span></span>
    
17. <span data-ttu-id="ce2ba-195">Klicken Sie im Bereich **Was möchten Sie tun, wenn vertrauliche Informationen erkannt werden?** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-195">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="ce2ba-196">Klicken Sie im Bereich **Möchten Sie die Richtlinie aktivieren oder zunächst testen?** auf **Ja, Richtlinie aktivieren**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-196">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="ce2ba-197">Klicken Sie im Bereich **Einstellungen überprüfen** auf **Erstellen**, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-197">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="ce2ba-198">Hier sehen Sie die sich ergebende Konfiguration für vertrauliche SharePoint Online-Teamwebsites.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-198">Here is your resulting configuration for sensitive SharePoint Online team sites.</span></span>
  
![DLP-Richtlinie für eine isolierte SharePoint Online-Teamwebsite mit der Office 365-Bezeichnung „Vertraulich“.](media/2ff4cc53-87a8-43e3-b637-3068d88409f3.png)
  
<span data-ttu-id="ce2ba-200">Verwenden Sie anschließend diese Schritte, um eine DLP-Richtlinie zu konfigurieren, die Benutzer blockiert, wenn sie ein Dokument auf einer vertraulichen SharePoint Online-Teamwebsite außerhalb einer Organisation freigeben.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-200">Next, use these steps to configure a DLP policy that blocks users when they share a document on a SharePoint Online highly confidential team site outside the organization.</span></span>
  
1. <span data-ttu-id="ce2ba-201">Klicken Sie auf der Registerkarte **Microsoft Office Home** im Browser auf die Kachel **Security &amp; Compliance**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-201">From the **Microsoft Office Home** tab in your browser, click the **Security &amp; Compliance** tile.</span></span>
    
2. <span data-ttu-id="ce2ba-202">Klicken Sie auf der Registerkarte **Security &amp; Compliance** in Ihrem Browser auf **Verhinderung von Datenverlust > Richtlinie**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-202">On the new **Security &amp; Compliance** tab in your browser, click **Data loss prevention > Policy**.</span></span>
    
3. <span data-ttu-id="ce2ba-203">Klicken Sie im Bereich **Verhinderung von Datenverlust** auf **+ Richtlinie erstellen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-203">In the **Data loss prevention** pane, click **+ Create a policy**.</span></span>
    
4. <span data-ttu-id="ce2ba-204">Klicken Sie im Bereich **Mit einer Vorlage beginnen oder eine benutzerdefinierte Richtlinie erstellen** auf **Benutzerdefiniert**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-204">In the **Start with a template or create a custom policy** pane, click **Custom**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="ce2ba-205">Geben Sie im Bereich **Benennen Sie Ihre Richtlinie** unter **Name** den Namen der DLP-Richtlinie für die streng vertrauliche Ebene ein, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-205">In the **Name your policy** pane, type the name for the highly sensitive level DLP policy in **Name**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="ce2ba-206">Klicken Sie im Bereich **Speicherorte auswählen** auf **Bestimmte Speicherorte auswählen**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-206">In the **Choose locations** pane, click **Let me choose specific locations**, and then click **Next**.</span></span>
    
7. <span data-ttu-id="ce2ba-207">Deaktivieren Sie in der Liste der Speicherorte **Exchange-E-Mail** und **OneDrive-Konten**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-207">In the list of locations, disable the **Exchange email** and **OneDrive accounts** locations, and then click **Next**.</span></span>
    
8. <span data-ttu-id="ce2ba-208">Klicken Sie im Bereich **Typen von vertraulichen Informationen anpassen, die geschützt werden sollen** auf **Bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-208">In the **Customize the types of sensitive info you want to protect** pane, click **Edit**.</span></span>
    
9. <span data-ttu-id="ce2ba-209">In der **wählen Sie die Typen der Inhalte zum Schutz** Bereich, klicken Sie auf **hinzufügen** im Dropdown-Listenfeld, und klicken Sie dann auf **Etiketten**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-209">In the **Choose the types of content to protect** pane, click **Add** in the drop-down box, and then click **Labels**.</span></span>
    
10. <span data-ttu-id="ce2ba-210">Klicken Sie im Bereich **Bezeichnungen** auf **+ Hinzufügen**, wählen Sie die Bezeichnung **Streng vertraulich** aus, klicken Sie auf **Hinzufügen**, und klicken Sie dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-210">In the **Labels** pane, click **+ Add**, select the **Highly Confidential** label, click **Add**, and then click **Done**.</span></span>
    
11. <span data-ttu-id="ce2ba-211">Klicken Sie im Bereich **Typen des zu schützenden Inhalts auswählen** auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-211">In the **Choose the types of content to protect** pane, click **Save**.</span></span>
    
12. <span data-ttu-id="ce2ba-212">Klicken Sie im Bereich **Customize the types of sensitive info you want to protect** (Anpassen der Typen an vertraulichen Informationen, die Sie schützen möchten) auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-212">In the **Customize the types of sensitive info you want to protect** pane, click **Next**.</span></span>
    
13. <span data-ttu-id="ce2ba-213">Klicken Sie im Bereich **What do you want to do if we detect sensitive info?** (Was möchten Sie tun, wenn vertrauliche Informationen erkannt werden?) auf **Customize the tip and email** (Den Tipp und die E-Mail anpassen).</span><span class="sxs-lookup"><span data-stu-id="ce2ba-213">In the **What do you want to do if we detect sensitive info?** pane, click **Customize the tip and email**.</span></span>
    
14. <span data-ttu-id="ce2ba-214">Klicken Sie im Bereich **Customize policy tips and email notifications** (Anpassen der Richtlinientipps und der E-Mail-Benachrichtigungen) auf **Customize the policy tip text** (Den Tipptext der Richtlinie als nächstes anpassen).</span><span class="sxs-lookup"><span data-stu-id="ce2ba-214">In the **Customize policy tips and email notifications** pane, click **Customize the policy tip text**.</span></span>
    
15. <span data-ttu-id="ce2ba-215">Geben Sie Folgendes in das Textfeld ein, oder fügen Sie es ein:</span><span class="sxs-lookup"><span data-stu-id="ce2ba-215">In the text box, type or paste in the following:</span></span>
    
  - <span data-ttu-id="ce2ba-p108">Wenn Sie eine Datei für einen Benutzer außerhalb der Organisation freigeben möchten, laden Sie die Datei herunter, und öffnen Sie sie. Klicken Sie auf „Datei“ > „Dokument schützen“ > „Mit Kennwort verschlüsseln“, und geben Sie dann ein sicheres Kennwort ein. Senden Sie das Kennwort in einer separaten E-Mail oder auf andere Weise.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-p108">To share with a user outside the organization, download the file and then open it. Click File, then Protect Document, and then Encrypt with Password, and then specify a strong password. Send the password in a separate email or other means of communication.</span></span>
    
    <span data-ttu-id="ce2ba-219">Sie können auch einen eigenen Tipp in Bezug auf die Richtlinie eingeben oder einfügen, der den Benutzern erläutert, wie sie Dateien außerhalb der Organisation freigeben.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-219">Alternately, type or paste in your own policy tip that instructs users on how to share a file outside your organization.</span></span>
    
16. <span data-ttu-id="ce2ba-220">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-220">Click **OK**.</span></span>
    
17. <span data-ttu-id="ce2ba-221">Klicken Sie im Bereich **Was möchten Sie tun, wenn vertrauliche Informationen erkannt werden?** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-221">In the **What do you want to do if we detect sensitive info?** pane, click **Next**.</span></span>
    
18. <span data-ttu-id="ce2ba-222">Klicken Sie im Bereich **Möchten Sie die Richtlinie aktivieren oder zunächst testen?** auf **Ja, Richtlinie aktivieren**, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-222">In the **Do you want to turn on the policy or test things out first?** pane, click **Yes, turn it on right away**, and then click **Next**.</span></span>
    
19. <span data-ttu-id="ce2ba-223">Klicken Sie im Bereich **Einstellungen überprüfen** auf **Erstellen**, und klicken Sie dann auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-223">In the **Review your settings** pane, click **Create**, and then click **Close**.</span></span>
    
<span data-ttu-id="ce2ba-224">Hier sehen Sie die sich ergebende Konfiguration für streng vertrauliche SharePoint Online-Teamwebsites.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-224">Here is your resulting configuration for high confidentiality SharePoint Online team sites.</span></span>
  
![DLP-Richtlinie für eine isolierte SharePoint Online-Teamwebsite mit der Office 365-Bezeichnung „Streng vertraulich“.](media/f705d3d0-23c9-4333-8b70-ad3b91f835ea.png)
  
## <a name="next-step"></a><span data-ttu-id="ce2ba-226">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="ce2ba-226">Next step</span></span>

[<span data-ttu-id="ce2ba-227">Schützen von SharePoint Online-Dateien mit Azure Information Protection</span><span class="sxs-lookup"><span data-stu-id="ce2ba-227">Protect SharePoint Online files with Azure Information Protection</span></span>](protect-sharepoint-online-files-with-azure-information-protection.md)
    
## <a name="see-also"></a><span data-ttu-id="ce2ba-228">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce2ba-228">See Also</span></span>

[<span data-ttu-id="ce2ba-229">Sichern von SharePoint Online-Websites und -Dateien</span><span class="sxs-lookup"><span data-stu-id="ce2ba-229">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="ce2ba-230">Sichern von SharePoint Online-Websites in einer Entwicklungs-/Testumgebung</span><span class="sxs-lookup"><span data-stu-id="ce2ba-230">Secure SharePoint Online sites in a dev/test environment</span></span>](secure-sharepoint-online-sites-in-a-dev-test-environment.md)
  
[<span data-ttu-id="ce2ba-231">Microsoft-Sicherheitsleitfaden für politische Kampagnen, gemeinnützigen Organisationen und andere agile Organisationen</span><span class="sxs-lookup"><span data-stu-id="ce2ba-231">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="ce2ba-232">Cloudakzeptanz und Hybridlösungen</span><span class="sxs-lookup"><span data-stu-id="ce2ba-232">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)


