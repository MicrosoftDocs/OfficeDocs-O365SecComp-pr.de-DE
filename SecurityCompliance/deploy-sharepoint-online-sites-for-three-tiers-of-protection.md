---
title: Bereitstellen von SharePoint Online-Websites für drei Schutzebenen
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 06/05/2018
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
ms.assetid: 1e8e3cfd-b878-4088-b941-9940363a5fae
description: 'Zusammenfassung: Erstellen und Konfigurieren von SharePoint Online-Teamwebsites für verschiedene Ebenen des Informationsschutzes.'
ms.openlocfilehash: 54392194f7ac5ce90337df3f33e23db595b1aa5c
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2018
ms.locfileid: "25345827"
---
# <a name="deploy-sharepoint-online-sites-for-three-tiers-of-protection"></a><span data-ttu-id="bf8ea-103">Bereitstellen von SharePoint Online-Websites für drei Schutzebenen</span><span class="sxs-lookup"><span data-stu-id="bf8ea-103">Deploy SharePoint Online sites for three tiers of protection</span></span>

 <span data-ttu-id="bf8ea-104">**Zusammenfassung:** Erstellen und Konfigurieren von SharePoint Online-Teamwebsites für verschiedene Ebenen des Informationsschutzes.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-104">**Summary:** Create and configure SharePoint Online team sites for various levels of information protection.</span></span>
  
<span data-ttu-id="bf8ea-p101">Verwenden Sie die Schritte in diesem Artikel, um Richtlinien für grundlegende, vertrauliche und streng vertrauliche SharePoint Online-Teamwebsites zu entwerfen. Weitere Informationen zu diesen drei Schutzebenen finden Sie unter [Sichern von SharePoint Online-Websites und -Dateien](secure-sharepoint-online-sites-and-files.md).</span><span class="sxs-lookup"><span data-stu-id="bf8ea-p101">Use the steps in this article to design and deploy baseline, sensitive, and highly confidential SharePoint Online team sites. For more information about these three tiers of protection, see [Secure SharePoint Online sites and files](secure-sharepoint-online-sites-and-files.md).</span></span>
  
## <a name="baseline-sharepoint-online-team-sites"></a><span data-ttu-id="bf8ea-107">Grundlegende SharePoint Online-Teamwebsites</span><span class="sxs-lookup"><span data-stu-id="bf8ea-107">Baseline SharePoint Online team sites</span></span>

<span data-ttu-id="bf8ea-p102">Der grundlegende Schutz enthält jeweils öffentliche und private Teamwebsites. Öffentliche Teamwebsites können von allen Benutzern in der Organisation ermittelt werden und alle haben Zugriff auf diese. Nur Mitglieder der Office 365-Gruppe, die mit der Teamwebsite verknüpft sind, können die privaten Websites ermitteln und auf diese zugreifen. Diese beiden Arten von Teamwebsites erlauben Mitgliedern, die Website für andere Personen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-p102">Baseline protection includes both public and private team sites. Public team sites can be discovered and accessed by anybody in the organization. Private sites can only be discovered and accessed by members of the Office 365 group associated with the team site. Both of these types of team sites allow members to share the site with others.</span></span>
  
### <a name="public"></a><span data-ttu-id="bf8ea-112">Öffentlich</span><span class="sxs-lookup"><span data-stu-id="bf8ea-112">Public</span></span>

<span data-ttu-id="bf8ea-113">Um eine grundlegende SharePoint Online-Teamwebsite mit öffentlichem Zugriff und Berechtigungen zu erstellen, tun Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-113">To create a baseline SharePoint Online team site with public access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="bf8ea-p103">Melden Sie sich beim Office 365-Portal mit einem Konto an, das auch zum Verwalten der SharePoint Online-Teamwebsite verwendet wird (SharePoint Online-Administrator). Hilfe finden Sie unter [Wo kann ich mich bei Office 365 Business anmelden?](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="bf8ea-p103">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator). For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="bf8ea-116">Klicken Sie in der Liste von Kacheln auf **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-116">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="bf8ea-117">Klicken Sie in der neuen Registerkarte **SharePoint** in Ihrem Browser auf **+ Website erstellen**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-117">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="bf8ea-118">Klicken Sie auf der Seite **Website erstellen** auf **Teamwebsite**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-118">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="bf8ea-119">Geben Sie unter **Name der Website** einen Namen für die öffentliche Teamwebsite ein.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-119">In **Site name**, type a name for the public team site.</span></span> 
    
6. <span data-ttu-id="bf8ea-120">Geben Sie im Feld **Beschreibung der Teamwebsite** eine Beschreibung der Website ein.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-120">In **Team site description**, type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="bf8ea-121">Wählen Sie unter **Datenschutzeinstellungen** die Option **Öffentlich - Alle Benutzer in der Organisation können auf diese Website zugreifen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-121">In **Privacy settings**, select **Public - anyone in the organization can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="bf8ea-122">Klicken Sie im Bereich **Wer soll hinzugefügt werden?** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-122">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="bf8ea-123">Nachfolgend sehen Sie die daraus resultierende Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-123">Here is your resulting configuration.</span></span>
  
![Grundschutz für eine öffentliche SharePoint Online-Teamwebsite.](media/bcd46b8d-3f89-4398-80ce-4da17ee85e03.png)
  
### <a name="private"></a><span data-ttu-id="bf8ea-125">Private</span><span class="sxs-lookup"><span data-stu-id="bf8ea-125">Private</span></span>

<span data-ttu-id="bf8ea-126">Um eine grundlegende SharePoint Online-Teamwebsite mit privatem Zugriff und Berechtigungen zu erstellen, tun Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-126">To create a baseline SharePoint Online team site with private access and permissions, do the following:</span></span>
  
1. <span data-ttu-id="bf8ea-p104">Melden Sie sich beim Office 365-Portal mit einem Konto an, das auch zum Verwalten der SharePoint Online-Teamwebsite verwendet wird (SharePoint Online-Administrator). Hilfe finden Sie unter [Wo kann ich mich bei Office 365 Business anmelden?](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="bf8ea-p104">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator). For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="bf8ea-129">Klicken Sie in der Liste von Kacheln auf **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-129">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="bf8ea-130">Klicken Sie in der neuen Registerkarte **SharePoint** in Ihrem Browser auf **+ Website erstellen**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-130">On the new **SharePoint** tab in your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="bf8ea-131">Klicken Sie auf der Seite **Website erstellen** auf **Teamwebsite**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-131">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="bf8ea-132">Geben Sie unter **Name der Website** einen Namen für die private Teamwebsite ein.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-132">In **Site name**, type a name for the private team site.</span></span> 
    
6. <span data-ttu-id="bf8ea-133">Geben Sie unter **Beschreibung der Teamwebsite** eine Beschreibung des Zwecks der Website ein.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-133">In **Team site description,** type a description of the purpose of the site.</span></span>
    
7. <span data-ttu-id="bf8ea-134">Wählen Sie unter **Datenschutzeinstellungen** die Option **Privat - nur Mitglieder können auf diese Website zugreifen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-134">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="bf8ea-135">Geben Sie im Bereich **Who do you want to add?** (Wen möchten Sie hinzufügen?) unter **Mitglieder hinzufügen** die Namen der Benutzerkonten ein, die über Zugriff auf diese private Teamwebsite verfügen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-135">On the **Who do you want to add?** pane, in **Add members**, type the names of user accounts that have access to this private team site.</span></span>
    
9. <span data-ttu-id="bf8ea-136">Wenn Sie mit dem Hinzufügen der ersten Gruppe von Mitgliedern zur Website fertig sind, klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-136">When you are done adding the initial set of members to the site, click **Finish**</span></span>
    
<span data-ttu-id="bf8ea-137">Nachfolgend sehen Sie die daraus resultierende Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-137">Here is your resulting configuration.</span></span>
  
![Grundschutz für eine private SharePoint Online-Teamwebsite.](media/91769026-37e3-4383-ac3c-dbf7aca98e41.png)
  
## <a name="sensitive-sharepoint-online-team-sites"></a><span data-ttu-id="bf8ea-139">Vertrauliche SharePoint Online-Teamwebsites</span><span class="sxs-lookup"><span data-stu-id="bf8ea-139">Sensitive SharePoint Online team sites</span></span>

<span data-ttu-id="bf8ea-140">Eine vertrauliche SharePoint Online-Teamwebsite ist eine isolierte Teamwebsite. Das heißt, dass die Berechtigungen über die Mitgliedschaft in SharePoint-Gruppen statt der Mitgliedschaft in der Office 365-Gruppe, die der Teamwebsite zugeordnet ist, gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-140">A sensitive SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="bf8ea-141">Beim Erstellen einer isolierten Teamwebsite gibt es zwei Hauptschritte.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-141">To create an isolated team site, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="bf8ea-142">Schritt 1: Entwerfen Ihrer isolierten Website</span><span class="sxs-lookup"><span data-stu-id="bf8ea-142">Step 1: Design your isolated site</span></span>

<span data-ttu-id="bf8ea-143">Um eine isolierte Teamwebsite zu erstellen, müssen Sie Folgendes festlegen:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-143">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="bf8ea-144">Ihre SharePoint-Gruppen und -Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-144">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="bf8ea-145">Der Satz der Zugriffsgruppen, die Mitglieder Ihrer SharePoint-Gruppen sein werden.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-145">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="bf8ea-146">Der empfohlene Satz von Zugriffsgruppen ist einer für Websitemitglieder, einer für Website-Viewer und einer für Websiteadministratoren.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-146">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="bf8ea-147">Ob Sie verschachtelte Gruppen innerhalb Ihrer Zugriffsgruppen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-147">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="bf8ea-148">Beispielsweise sehen die empfohlene Gruppenstruktur und Berechtigungsstufen wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-148">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="bf8ea-149">**SharePoint-Gruppe**</span><span class="sxs-lookup"><span data-stu-id="bf8ea-149">**SharePoint group**</span></span>|<span data-ttu-id="bf8ea-150">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="bf8ea-150">**Permission level**</span></span>|<span data-ttu-id="bf8ea-151">**Zugriffsgruppe (Beispiele)**</span><span class="sxs-lookup"><span data-stu-id="bf8ea-151">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf8ea-152">[Websitename] Mitglieder</span><span class="sxs-lookup"><span data-stu-id="bf8ea-152">[site name] Members</span></span>  <br/> |<span data-ttu-id="bf8ea-153">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="bf8ea-153">Edit</span></span>  <br/> |<span data-ttu-id="bf8ea-154">[Websitename] Mitglieder</span><span class="sxs-lookup"><span data-stu-id="bf8ea-154">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="bf8ea-155">[Websitename] Besucher</span><span class="sxs-lookup"><span data-stu-id="bf8ea-155">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="bf8ea-156">Überwachungsdaten</span><span class="sxs-lookup"><span data-stu-id="bf8ea-156">Read</span></span>  <br/> |<span data-ttu-id="bf8ea-157">[Websitename] Viewer</span><span class="sxs-lookup"><span data-stu-id="bf8ea-157">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="bf8ea-158">[Websitename] Besitzer</span><span class="sxs-lookup"><span data-stu-id="bf8ea-158">[site name] Owners</span></span>  <br/> |<span data-ttu-id="bf8ea-159">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="bf8ea-159">Full control</span></span>  <br/> |<span data-ttu-id="bf8ea-160">[Websitename] Administratoren</span><span class="sxs-lookup"><span data-stu-id="bf8ea-160">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="bf8ea-p105">Die SharePoint-Gruppen und -Berechtigungsstufen werden standardmäßig für eine Teamwebsite erstellt. Sie müssen die Namen Ihrer Zugriffsgruppen bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-p105">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="bf8ea-163">Informationen zum Entwurfsprozess finden Sie unter [Entwerfen einer isolierten SharePoint Online-Teamwebsite](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="bf8ea-163">For the details of the design process, see [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="bf8ea-164">Schritt 2: Bereitstellen Ihrer isolierten Website</span><span class="sxs-lookup"><span data-stu-id="bf8ea-164">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="bf8ea-165">Um Ihre isolierte Website bereitzustellen, müssen Sie zunächst Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-165">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="bf8ea-166">Bestimmen Sie die Benutzerkonten und -gruppen, die jeder Zugriffsgruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-166">Determine the user accounts and groups to add to each of your access groups.</span></span>
    
- <span data-ttu-id="bf8ea-167">Erstellen Sie die Zugriffsgruppen, und fügen Sie die Benutzer und Gruppenmitglieder hinzu.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-167">Create the access groups and add the user and group members.</span></span>
    
<span data-ttu-id="bf8ea-168">Detaillierte Schritte finden Sie in **Phase 1** unter [Bereitstellen einer isolierten SharePoint Online-Teamwebsite](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="bf8ea-168">For the detailed steps, see **Phase 1** of [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="bf8ea-169">Erstellen Sie als Nächstes mit den folgenden Schritten die SharePoint Online-Teamwebsite.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-169">Next, you create the SharePoint Online team site with these steps.</span></span>
  
1. <span data-ttu-id="bf8ea-p106">Melden Sie sich beim Office 365-Portal mit einem Konto an, das auch zum Verwalten der SharePoint Online-Teamwebsite verwendet wird (SharePoint Online-Administrator). Hilfe finden Sie unter [Wo kann ich mich bei Office 365 Business anmelden?](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span><span class="sxs-lookup"><span data-stu-id="bf8ea-p106">Sign in to the Office 365 portal with an account that will also be used to administer the SharePoint Online team site (a SharePoint Online administrator). For help, see [Where to sign in to Office 365](https://support.office.com/Article/Where-to-sign-in-to-Office-365-e9eb7d51-5430-4929-91ab-6157c5a050b4).</span></span>
    
2. <span data-ttu-id="bf8ea-172">Klicken Sie in der Liste von Kacheln auf **SharePoint**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-172">In the list of tiles, click **SharePoint**.</span></span>
    
3. <span data-ttu-id="bf8ea-173">Klicken Sie auf der neuen Registerkarte **SharePoint** in Ihrem Browser auf **+ Website erstellen**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-173">In the new **SharePoint** tab of your browser, click **+ Create site**.</span></span>
    
4. <span data-ttu-id="bf8ea-174">Klicken Sie auf der Seite **Website erstellen** auf **Teamwebsite**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-174">On the **Create a site** page, click **Team site**.</span></span>
    
5. <span data-ttu-id="bf8ea-175">Geben Sie unter **Name der Website** einen Namen für die private Teamwebsite ein.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-175">In **Site name**, type a name for the private team site.</span></span>
    
6. <span data-ttu-id="bf8ea-176">Geben Sie in der Beschreibung für die **Teamwebsite** eine optionale Beschreibung ein.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-176">In **Team site description**, type an optional description.</span></span>
    
7. <span data-ttu-id="bf8ea-177">Wählen Sie unter **Datenschutzeinstellungen** die Option **Privat - nur Mitglieder können auf diese Website zugreifen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-177">In **Privacy settings**, select **Private - only members can access this site**, and then click **Next**.</span></span>
    
8. <span data-ttu-id="bf8ea-178">Klicken Sie im Bereich **Wer soll hinzugefügt werden?** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-178">On the **Who do you want to add?** pane, click **Finish**.</span></span>
    
<span data-ttu-id="bf8ea-179">Konfigurieren Sie dann auf der neuen SharePoint Online-Teamwebsite die Berechtigungen mithilfe folgender Schritte.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-179">Next, from the new SharePoint Online team site, configure permissions with these steps.</span></span>
  
1. <span data-ttu-id="bf8ea-p107">Ermitteln Sie den UPN (User Principal Name) des IT-Administrators oder der anderen Person, die für das Beantworten und Bearbeiten von Anfragen hinsichtlich des Zugriffs auf die Website zuständig ist (Beispiel für einen UPN: belindan@contoso.com). Notieren Sie den UPN hier: ![](./media/Common-Images/TableLine.png).</span><span class="sxs-lookup"><span data-stu-id="bf8ea-p107">Determine the User Principal Name (UPN) of the IT administrator or other person who will be responsible for responding to and addressing requests for access to the site (belindan@contoso.com is an example of a UPN). Write that UPN here: ![](./media/Common-Images/TableLine.png).</span></span>
    
2. <span data-ttu-id="bf8ea-182">Klicken Sie in der Symbolleiste auf das Symbol „Einstellungen“ und anschließend auf **Websiteberechtigungen**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-182">In the tool bar, click the settings icon, and then click **Site permissions**.</span></span>
    
3. <span data-ttu-id="bf8ea-183">Klicken Sie im Bereich **Websiteberechtigungen** auf **Erweiterte Berechtigungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-183">In the **Site permissions** pane, click **Advanced permissions settings**.</span></span>
    
4. <span data-ttu-id="bf8ea-184">Klicken Sie auf der neuen Registerkarte **Berechtigungen** in Ihrem Browser auf **Zugriffseinstellungen anfordern**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-184">On the new **Permissions** tab of your browser, click **Access Request Settings**.</span></span>
    
5. <span data-ttu-id="bf8ea-185">Im Dialogfeld **Einstellungen für Zugriffsanforderungen**:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-185">In the **Access Requests Settings** dialog box:</span></span>
    
  - <span data-ttu-id="bf8ea-186">Deaktivieren Sie die Kontrollkästchen **Mitgliedern das Freigeben der Website sowie einzelner Dateien und Ordner erlauben** und **Mitgliedern erlauben, andere Benutzer der Gruppe "Websitemitglieder" einzuladen**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-186">Clear the **Allow members to share the site and individual files and folders** and **Allow members to invite others to the site members group** check boxes.</span></span>
    
  - <span data-ttu-id="bf8ea-187">Geben Sie den UPN Ihres IT-Administrators aus Schritt 1 unter **Alle Zugriffsanforderungen senden**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-187">Type the UPN of your IT administrator from step 1 in **Send all requests for access**.</span></span>
    
  - <span data-ttu-id="bf8ea-188">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-188">Click **OK**.</span></span>
    
6. <span data-ttu-id="bf8ea-189">Klicken Sie auf der Registerkarte **Berechtigungen** Ihres Browsers auf **[Websitename] Mitglieder** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-189">On the **Permissions** tab of your browser, click **[site name] Members** in the list.</span></span>
    
7. <span data-ttu-id="bf8ea-190">Klicken Sie unter **Benutzer und Gruppen** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-190">In **People and Groups**, click **New**.</span></span>
    
8. <span data-ttu-id="bf8ea-191">Geben Sie im Dialogfeld **Freigeben** den Namen der Zugriffsgruppe Ihrer Websitemitglieder für diese Website an, wählen Sie ihn aus, und klicken Sie dann auf **Freigeben**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-191">In the **Share** dialog box, type the name of your site members access group for this site, select it, and then click **Share**.</span></span>
    
9. <span data-ttu-id="bf8ea-192">Klicken Sie auf die Schaltfläche „Zurück“ in Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-192">Click the back button on your browser.</span></span>
    
10. <span data-ttu-id="bf8ea-193">Klicken Sie auf **Besitzer von [Websitename]** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-193">Click **[site name] Owners** in the list.</span></span>
    
11. <span data-ttu-id="bf8ea-194">Klicken Sie auf der Seite **Benutzer und Gruppen** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-194">In **People and Groups**, click **New**.</span></span>
    
12. <span data-ttu-id="bf8ea-195">Geben Sie im Dialogfeld **Freigeben** den Namen der Zugriffsgruppe des Websiteadministrators für diese Website an, wählen Sie ihn aus, und klicken Sie dann auf **Freigeben**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-195">In the **Share** dialog box, type the name of the site administrators access group for this site, select it, and then click **Share**.</span></span>
    
13. <span data-ttu-id="bf8ea-196">Klicken Sie auf die Schaltfläche „Zurück“ in Ihrem Browser.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-196">Click the back button on your browser.</span></span>
    
14. <span data-ttu-id="bf8ea-197">Klicken Sie auf **Besucher von [Websitename]** in der Liste.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-197">Click **[site name] Visitors** in the list.</span></span>
    
15. <span data-ttu-id="bf8ea-198">Klicken Sie auf der Seite **Benutzer und Gruppen** auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-198">In **People and Groups**, click **New**.</span></span>
    
16. <span data-ttu-id="bf8ea-199">Geben Sie im Dialogfeld **Freigeben** den Namen der Zugriffsgruppe der Websiteviewer für diese Website an, wählen Sie ihn aus, und klicken Sie dann auf **Freigeben**.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-199">In the **Share** dialog box, type the name of the site viewers access group for this site, select it, and then click **Share**.</span></span>
    
17. <span data-ttu-id="bf8ea-200">Schließen Sie die Registerkarte **Berechtigungen** Ihres Browsers.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-200">Close the **Permissions** tab of your browser.</span></span>
    
<span data-ttu-id="bf8ea-201">Die Ergebnisse dieser Berechtigungseinstellungen sehen folgendermaßen aus:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-201">The results of these permission settings are:</span></span>
  
- <span data-ttu-id="bf8ea-202">Die SharePoint-Gruppe **Besitzer von [Websitename]** enthält die Zugriffsgruppe des Websiteadministrators, in der alle Mitglieder über die Berechtigungsstufe **Vollzugriff** verfügen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-202">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="bf8ea-203">Die SharePoint-Gruppe **[Websitename] Mitglieder** enthält die Zugriffsgruppe der Websitemitglieder, in der alle Mitglieder über die Berechtigungsstufe **Bearbeiten** verfügen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-203">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="bf8ea-204">Die SharePoint-Gruppe **[Websitename] Besucher** enthält die Zugriffsgruppe der Websitebesucher, in der alle Mitglieder über die Berechtigungsstufe **Lesen** verfügen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-204">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="bf8ea-205">Die Möglichkeit, dass Mitglieder andere Mitglieder einladen, ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-205">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="bf8ea-206">Die Möglichkeit, dass Nicht-Mitglieder Zugriff anfordern, ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-206">The ability for non-members to request access is enabled.</span></span>
    
<span data-ttu-id="bf8ea-207">Nachfolgend sehen Sie die daraus resultierende Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-207">Here is your resulting configuration.</span></span>
  
![Schutzebene „Vertraulich“ für eine isolierte SharePoint Online-Teamwebsite.](media/7a6ab9c6-560a-4674-ac39-8175644dbe6f.png)
  
<span data-ttu-id="bf8ea-209">Die Mitglieder der Website können nun über Gruppenmitgliedschaft in einer der Zugriffsgruppen sicher an den Ressourcen der Website zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-209">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="highly-confidential-sharepoint-online-team-sites"></a><span data-ttu-id="bf8ea-210">Streng vertrauliche SharePoint Online-Teamwebsites</span><span class="sxs-lookup"><span data-stu-id="bf8ea-210">Highly confidential SharePoint Online team sites</span></span>

<span data-ttu-id="bf8ea-211">Eine streng vertrauliche SharePoint Online-Teamwebsite ist eine isolierte Teamwebsite, was bedeutet, dass Berechtigungen über die Mitgliedschaft in SharePoint-Gruppen und nicht über die Mitgliedschaft in der Office 365-Gruppe gesteuert werden, die mit der Teamwebsite verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-211">A highly confidential SharePoint Online team site is an isolated team site, which means that permissions are controlled through membership in SharePoint groups instead of membership in the Office 365 group associated with the team site.</span></span>
  
<span data-ttu-id="bf8ea-212">Für die Erstellung einer isolierten Teamwebsite für streng vertrauliche Informationen und Kollaboration sind zwei Schritte nötig.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-212">To create an isolated team site for highly confidential information and collaboration, there are two main steps.</span></span>
  
### <a name="step-1-design-your-isolated-site"></a><span data-ttu-id="bf8ea-213">Schritt 1: Entwerfen Ihrer isolierten Website</span><span class="sxs-lookup"><span data-stu-id="bf8ea-213">Step 1: Design your isolated site</span></span>

<span data-ttu-id="bf8ea-214">Um eine isolierte Teamwebsite zu erstellen, müssen Sie Folgendes festlegen:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-214">To design your isolated team site, you need to determine:</span></span>
  
- <span data-ttu-id="bf8ea-215">Ihre SharePoint-Gruppen und -Berechtigungsstufen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-215">Your SharePoint groups and permission levels.</span></span>
    
- <span data-ttu-id="bf8ea-216">Der Satz der Zugriffsgruppen, die Mitglieder Ihrer SharePoint-Gruppen sein werden.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-216">The set of access groups that will be members of your SharePoint groups.</span></span>
    
     <span data-ttu-id="bf8ea-217">Der empfohlene Satz von Zugriffsgruppen ist einer für Websitemitglieder, einer für Website-Viewer und einer für Websiteadministratoren.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-217">The recommended set of access groups is one for site members, one for site viewers, and one for site administrators.</span></span>
    
- <span data-ttu-id="bf8ea-218">Ob Sie verschachtelte Gruppen innerhalb Ihrer Zugriffsgruppen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-218">Whether you will use nested groups within your access groups.</span></span>
    
<span data-ttu-id="bf8ea-219">Beispielsweise sehen die empfohlene Gruppenstruktur und Berechtigungsstufen wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-219">For example, the recommended group structure and permission levels look like this:</span></span>
  
|<span data-ttu-id="bf8ea-220">**SharePoint-Gruppe**</span><span class="sxs-lookup"><span data-stu-id="bf8ea-220">**SharePoint group**</span></span>|<span data-ttu-id="bf8ea-221">**Berechtigungsstufe**</span><span class="sxs-lookup"><span data-stu-id="bf8ea-221">**Permission level**</span></span>|<span data-ttu-id="bf8ea-222">**Zugriffsgruppe (Beispiele)**</span><span class="sxs-lookup"><span data-stu-id="bf8ea-222">**Access group (examples)**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bf8ea-223">[Websitename] Mitglieder</span><span class="sxs-lookup"><span data-stu-id="bf8ea-223">[site name] Members</span></span>  <br/> |<span data-ttu-id="bf8ea-224">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="bf8ea-224">Edit</span></span>  <br/> |<span data-ttu-id="bf8ea-225">[Websitename] Mitglieder</span><span class="sxs-lookup"><span data-stu-id="bf8ea-225">[site name] Members</span></span>  <br/> |
|<span data-ttu-id="bf8ea-226">[Websitename] Besucher</span><span class="sxs-lookup"><span data-stu-id="bf8ea-226">[site name] Visitors</span></span>  <br/> |<span data-ttu-id="bf8ea-227">Überwachungsdaten</span><span class="sxs-lookup"><span data-stu-id="bf8ea-227">Read</span></span>  <br/> |<span data-ttu-id="bf8ea-228">[Websitename] Viewer</span><span class="sxs-lookup"><span data-stu-id="bf8ea-228">[site name] Viewers</span></span>  <br/> |
|<span data-ttu-id="bf8ea-229">[Websitename] Besitzer</span><span class="sxs-lookup"><span data-stu-id="bf8ea-229">[site name] Owners</span></span>  <br/> |<span data-ttu-id="bf8ea-230">Vollzugriff</span><span class="sxs-lookup"><span data-stu-id="bf8ea-230">Full control</span></span>  <br/> |<span data-ttu-id="bf8ea-231">[Websitename] Administratoren</span><span class="sxs-lookup"><span data-stu-id="bf8ea-231">[site name] Admins</span></span>  <br/> |
   
<span data-ttu-id="bf8ea-p108">Die SharePoint-Gruppen und -Berechtigungsstufen werden standardmäßig für eine Teamwebsite erstellt. Sie müssen die Namen Ihrer Zugriffsgruppen bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-p108">The SharePoint groups and permission levels are created by default for a team site. You need to determine the names of your access groups.</span></span>
  
<span data-ttu-id="bf8ea-234">Informationen zum Entwurfsprozess finden Sie unter [Entwerfen einer isolierten SharePoint Online-Teamwebsite](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="bf8ea-234">For the details of the design process, see [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
### <a name="step-2-deploy-your-isolated-site"></a><span data-ttu-id="bf8ea-235">Schritt 2: Bereitstellen Ihrer isolierten Website</span><span class="sxs-lookup"><span data-stu-id="bf8ea-235">Step 2: Deploy your isolated site</span></span>

<span data-ttu-id="bf8ea-236">Um Ihre isolierte Website bereitzustellen, müssen Sie zunächst Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-236">To deploy your isolated site, you first need to:</span></span>
  
- <span data-ttu-id="bf8ea-237">Ermitteln Sie die Benutzer und Gruppenmitglieder der einzelnen Zugriffsgruppen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-237">Determine the user and group members of each of your access groups</span></span>
    
- <span data-ttu-id="bf8ea-238">Erstellen Sie die Zugriffsgruppen, und fügen Sie die Benutzer und Gruppenmitglieder hinzu.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-238">Create the access groups and add the user and group members</span></span>
    
- <span data-ttu-id="bf8ea-239">Erstellen einer isoliertem Teamwebsite, die Ihre Zugriffsgruppen verwendet</span><span class="sxs-lookup"><span data-stu-id="bf8ea-239">Create an isolated team site that uses your access groups</span></span>
    
<span data-ttu-id="bf8ea-240">Detaillierte Schritte finden Sie unter [Bereitstellen einer isolierten SharePoint Online-Teamwebsite](deploy-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="bf8ea-240">For the detailed steps, see [Deploy an isolated SharePoint Online team site](deploy-an-isolated-sharepoint-online-team-site.md).</span></span>
  
<span data-ttu-id="bf8ea-241">Nachfolgend sind die Ergebnisse dieser Berechtigungseinstellungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="bf8ea-241">The results of the permission settings are:</span></span>
  
- <span data-ttu-id="bf8ea-242">Die SharePoint-Gruppe **Besitzer von [Websitename]** enthält die Zugriffsgruppe des Websiteadministrators, in der alle Mitglieder über die Berechtigungsstufe **Vollzugriff** verfügen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-242">The **[site name] Owners** SharePoint group contains the site administrators access group, in which all the members have the **Full control** permission level.</span></span>
    
- <span data-ttu-id="bf8ea-243">Die SharePoint-Gruppe **[Websitename] Mitglieder** enthält die Zugriffsgruppe der Websitemitglieder, in der alle Mitglieder über die Berechtigungsstufe **Bearbeiten** verfügen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-243">The **[site name] Members** SharePoint group contains the site members access group, in which all the members have the **Edit** permission level.</span></span>
    
- <span data-ttu-id="bf8ea-244">Die SharePoint-Gruppe **[Websitename] Besucher** enthält die Zugriffsgruppe der Websitebesucher, in der alle Mitglieder über die Berechtigungsstufe **Lesen** verfügen.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-244">The **[site name] Visitors** SharePoint group contains the site viewers access group, in which all the members have the **Read** permission level.</span></span>
    
- <span data-ttu-id="bf8ea-245">Die Möglichkeit, dass Mitglieder andere Mitglieder einladen, ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-245">The ability for members to invite other members is disabled.</span></span>
    
- <span data-ttu-id="bf8ea-246">Die Möglichkeit, dass Nicht-Mitglieder Zugriff anfordern, ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-246">The ability for non-members to request access is disabled.</span></span>
    
<span data-ttu-id="bf8ea-247">Nachfolgend sehen Sie die daraus resultierende Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-247">Here is your resulting configuration.</span></span>
  
![Schutzebene „Streng vertraulich“ für eine isolierte SharePoint Online-Teamwebsite.](media/196359ab-d7ed-4fcf-97b4-61820a74aca4.png)
  
<span data-ttu-id="bf8ea-249">Die Mitglieder der Website können nun über Gruppenmitgliedschaft in einer der Zugriffsgruppen sicher an den Ressourcen der Website zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf8ea-249">The members of the site, through group membership in one of the access groups, can now securely collaborate on the resources of the site.</span></span>
  
## <a name="next-step"></a><span data-ttu-id="bf8ea-250">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="bf8ea-250">Next step</span></span>

[<span data-ttu-id="bf8ea-251">Schützen von SharePoint Online-Dateien mit Office 365-Bezeichnungen und Verhindern von Datenverlust</span><span class="sxs-lookup"><span data-stu-id="bf8ea-251">Protect SharePoint Online files with Office 365 labels and DLP</span></span>](protect-sharepoint-online-files-with-office-365-labels-and-dlp.md)
    
## <a name="see-also"></a><span data-ttu-id="bf8ea-252">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf8ea-252">See also</span></span>

[<span data-ttu-id="bf8ea-253">Sichern von SharePoint Online-Websites und -Dateien</span><span class="sxs-lookup"><span data-stu-id="bf8ea-253">Secure SharePoint Online sites and files</span></span>](secure-sharepoint-online-sites-and-files.md)
  
[<span data-ttu-id="bf8ea-254">Sichern von SharePoint Online-Websites in einer Entwicklungs-/Testumgebung</span><span class="sxs-lookup"><span data-stu-id="bf8ea-254">Secure SharePoint Online sites in a dev/test environment</span></span>](secure-sharepoint-online-sites-in-a-dev-test-environment.md)
  
[<span data-ttu-id="bf8ea-255">Microsoft-Sicherheitsleitfaden für politische Kampagnen, gemeinnützigen Organisationen und andere agile Organisationen</span><span class="sxs-lookup"><span data-stu-id="bf8ea-255">Microsoft Security Guidance for Political Campaigns, Nonprofits, and Other Agile Organizations</span></span>](microsoft-security-guidance-for-political-campaigns-nonprofits-and-other-agile-o.md)
  
[<span data-ttu-id="bf8ea-256">Cloudakzeptanz und Hybridlösungen</span><span class="sxs-lookup"><span data-stu-id="bf8ea-256">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)




