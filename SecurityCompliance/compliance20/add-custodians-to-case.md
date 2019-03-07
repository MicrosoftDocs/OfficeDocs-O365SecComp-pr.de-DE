---
title: Hinzufügen von Bewahrern zu einem Advanced eDiscovery (Preview)-Fall
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: fe208f4a9f7927d8481d5c6ec8b901baafb98626
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455297"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="ccdba-102">Hinzufügen von Bewahrern zu einem Advanced eDiscovery (Preview)-Fall</span><span class="sxs-lookup"><span data-stu-id="ccdba-102">Add custodians to an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="ccdba-103">Mit Advanced eDiscovery (Preview) können Sie das integrierte Depot Verwaltungstool nutzen, um Ihre Workflows rund um die Verwaltung von Verwaltern und die Identifizierung relevanter, Freiheits enthaltener Datenquellen in einem Fall zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="ccdba-103">Using Advanced eDiscovery (Preview), you can leverage the built-in custodian management tool to coordinate your workflows around managing custodians and identifying relevant, custodial data sources within a case.</span></span> <span data-ttu-id="ccdba-104">Wenn Sie eine Depotbank hinzufügen, kann das System die primären Exchange-Postfächer und die OneDrive for Business-Website automatisch identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ccdba-104">When you add a custodian, the system can automatically identify, and place holds on their primary Exchange mailbox and OneDrive for Business site.</span></span> <span data-ttu-id="ccdba-105">Wenn Sie Ihre Ermittlung durchführen, können Sie auch zusätzliche Postfächer oder Websites aufdecken und zuordnen, auf die ein Verwalter in der Vergangenheit oder Teams zugegriffen hat, von denen ein Verwalter heute Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="ccdba-105">As you conduct your discovery, you might also uncover and map additional mailboxes or sites that a custodian accessed in the past or Teams that a custodian is a member of today.</span></span>

<span data-ttu-id="ccdba-106">Verwenden Sie den folgenden Workflow, um Verwalter in Advanced eDiscovery (Preview)-Fällen im Security & Compliance Center hinzuzufügen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ccdba-106">Use the following workflow to add and manage custodians in Advanced eDiscovery (Preview) cases within the Security & Compliance Center.</span></span> 

![Registerkarte Depotverwaltung](../media/CustodianMgtPage.png)


## <a name="step-1-identify-potential-custodians"></a><span data-ttu-id="ccdba-108">Schritt 1: Identifizieren potenzieller Verwalter</span><span class="sxs-lookup"><span data-stu-id="ccdba-108">Step 1: Identify potential custodians</span></span>

<span data-ttu-id="ccdba-109">Der erste Schritt besteht darin, die geeigneten Verwalter für Ihre Angelegenheit zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ccdba-109">The first step is to identify the appropriate custodians for your matter.</span></span> <span data-ttu-id="ccdba-110">Um einem Fall Verwalter hinzuzufügen, müssen Sie Mitglied der Rollengruppe "eDiscovery-Manager" oder "eDiscovery-Admins" sein.</span><span class="sxs-lookup"><span data-stu-id="ccdba-110">To add custodians to a case, you must be a member of the eDiscovery Managers or eDiscovery Admins role group.</span></span>   

![Identifizieren potenzieller Verwalter](../media/AddCustodianStep1.png)

<span data-ttu-id="ccdba-112">So fügen Sie einem vorhandenen Advanced eDiscovery (Preview)-Fall Verwalter hinzu:</span><span class="sxs-lookup"><span data-stu-id="ccdba-112">To add custodians to an existing Advanced eDiscovery (Preview) case:</span></span>

1. <span data-ttu-id="ccdba-113">Wechseln Sie auf der Seite **Advanced eDiscovery (Preview)** zu Ihrem Fall.</span><span class="sxs-lookup"><span data-stu-id="ccdba-113">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>
 
2. <span data-ttu-id="ccdba-114">Nachdem Sie einen Fall ausgewählt haben, wechseln Sie zur \*\*\*\* Registerkarte depotbanks, und klicken Sie auf **+ Depotbank hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="ccdba-114">After you have selected a case, go to the **Custodians** tab and click **+ Add Custodian**.</span></span> 
 
3. <span data-ttu-id="ccdba-115">Wählen Sie die Verwalter aus, die Sie der Anfrage hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="ccdba-115">Choose the custodians that you want to add to the case.</span></span> <span data-ttu-id="ccdba-116">Sie können zunächst eingeben, um die Benutzer aus Azure Active Directory Ihrer Organisation zu suchen und auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-116">You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="ccdba-117">Nachdem Sie die Liste der Verwalter abgeschlossen haben, klicken Sie auf **weiter** , um mit der Identifizierung potenzieller Datenquellen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-117">After you have finalized the list of custodians, click **Next** to begin identifying potential data sources.</span></span> 
  
## <a name="optional-step-2-select-custodian-data-sources"></a><span data-ttu-id="ccdba-118">Optional Schritt 2: Auswählen von Depotbank-Datenquellen</span><span class="sxs-lookup"><span data-stu-id="ccdba-118">(Optional) Step 2: Select custodian data sources</span></span>

<span data-ttu-id="ccdba-119">Nachdem Sie einem Fall Verwalter hinzugefügt haben, können Sie Office 365 für die Identifizierung und Aufbewahrung der primären Depotbank-Datenquellen nutzen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-119">After you have added custodians to a case, you can leverage Office 365 to help you identify and preserve the primary custodian data sources.</span></span> <span data-ttu-id="ccdba-120">Im nächsten Schritt dieses Workflows werden die Datenquellen ausgewählt, die den in Schritt 1 angegebenen depotbanks gehören.</span><span class="sxs-lookup"><span data-stu-id="ccdba-120">The next step in this workflow is to select the data sources owned by the custodians specified in Step 1.</span></span> 

![Wählen Sie Datenquellen für FreiheitsEntzug aus](../media/AddCustodianStep2.png)

<span data-ttu-id="ccdba-122">So identifizieren Sie Depotbank-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="ccdba-122">To identify custodian data sources:</span></span> 

1. <span data-ttu-id="ccdba-123">Wählen Sie für jede Depotbank **Exchange** aus, wenn das primäre Exchange-Postfach des Depot Systems automatisch ermittelt und hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ccdba-123">For each custodian, select **Exchange** if you would like the system to automatically identify and add the custodian's primary Exchange mailbox.</span></span> 
 
2. <span data-ttu-id="ccdba-124">Wählen Sie für jede Depotbank **OneDrive** aus, wenn Sie möchten, dass das System die primäre ONEDRIVE-URL der Depotbank automatisch identifiziert und hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="ccdba-124">For each custodian, select **OneDrive** if you would like the system to automatically identify and add the custodian's primary OneDrive URL.</span></span> 

    <span data-ttu-id="ccdba-125">Nachdem Sie Ihre Auswahl getroffen haben, versucht das System automatisch, die Datenquellen zu identifizieren und zu Ihrem Fall hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-125">After you've made your selections, they system will automatically try to identify the data sources and add them to your case.</span></span>
 
4. <span data-ttu-id="ccdba-126">Klicken Sie auf **weiter** , um mit dem Zuordnen zusätzlicher Datenquellen zur Depotbank zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-126">Click **Next** to begin mapping additional data sources to your custodian.</span></span>

## <a name="optional-step-3-map-additional-data-sources"></a><span data-ttu-id="ccdba-127">Optional Schritt 3: Zuordnen zusätzlicher Datenquellen</span><span class="sxs-lookup"><span data-stu-id="ccdba-127">(Optional) Step 3: Map additional data sources</span></span>

<span data-ttu-id="ccdba-128">Je nach Fall möchten Sie möglicherweise auch Postfächer hinzufügen, die ein bestimmter Depotbank in der Vergangenheit verwendet haben kann, Gruppen, in denen ein Depotbank derzeit Mitglied ist, oder Websites, auf die ein Verwalter in der Vergangenheit Zugriff hatte.</span><span class="sxs-lookup"><span data-stu-id="ccdba-128">Depending on your case, you may also want to add mailboxes that a given custodian may have used in the past, groups where a custodian is currently a member, or sites that a custodian had access to in the past.</span></span> <span data-ttu-id="ccdba-129">Zusätzlich zu den primären Depotbank-Datenquellen können Sie zusätzliche Office 365-Datenquellen einem depotverwalter hinzufügen oder Office 365 nutzen, um potenziell relevante Datenquellen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ccdba-129">In addition to primary custodian data sources, you can add additional Office 365 data sources to a custodian or leverage Office 365 to help you identify potentially relevant data sources as well.</span></span> 

![Zuordnen zusätzlicher Datenquellen](../media/AddCustodianStep3.PNG)

<span data-ttu-id="ccdba-131">Zuordnen von Postfächern, Websites oder Teams zu einem bestimmten Depot:</span><span class="sxs-lookup"><span data-stu-id="ccdba-131">To map mailboxes, sites, or teams to a specific custodian:</span></span>
1. <span data-ttu-id="ccdba-132">Wählen Sie **Hinzufügen** aus, um einem bestimmten Verwalter inhaltsspeicherorte wie Postfächer, Websites und Teams zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-132">Select **Add** to assign content locations, like mailboxes, sites, and Teams, to a specific custodian.</span></span> 

2. <span data-ttu-id="ccdba-133">Geben Sie im Flyout Folgendes an: ![Zuordnen von Datenquellen](../media/AddCustodianStep4.PNG)</span><span class="sxs-lookup"><span data-stu-id="ccdba-133">In the flyout, specify the following: ![Map Data Sources](../media/AddCustodianStep4.PNG)</span></span>
  -  <span data-ttu-id="ccdba-134">**Exchange-Postfächer** – klicken Sie auf **Benutzer, Gruppen oder Teams auswählen** , und klicken Sie dann erneut auf **Benutzer, Gruppen oder Teams auswählen** .</span><span class="sxs-lookup"><span data-stu-id="ccdba-134">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again.</span></span> <span data-ttu-id="ccdba-135">Zum Angeben von Postfächern, die dem ausgewählten depotverwalter zugewiesen werden sollen, verwenden Sie das Suchfeld, um nach Benutzerpostfächern und Verteilergruppen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-135">To specify mailboxes to assign to the selected custodian, use the search box to find user mailboxes and distribution groups.</span></span> <span data-ttu-id="ccdba-136">Sie können auch das zugeordnete Postfach für eine Office 365-Gruppe oder ein Microsoft-Team zuweisen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-136">You can also assign the associated mailbox for an Office 365 Group or a Microsoft Team.</span></span> <span data-ttu-id="ccdba-137">Aktivieren Sie das Kontrollkästchen Benutzer, Gruppe, Team, klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="ccdba-137">Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ccdba-138">Wenn Sie auf Benutzer, Gruppen oder Teams zum Angeben von Postfächern klicken, ist die angezeigte Post Fachauswahl leer.</span><span class="sxs-lookup"><span data-stu-id="ccdba-138">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty.</span></span> <span data-ttu-id="ccdba-139">Dies ist beabsichtigt, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ccdba-139">This is by design to enhance performance.</span></span> <span data-ttu-id="ccdba-140">Wenn Sie Personen zu dieser Liste hinzufügen möchten, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="ccdba-140">To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
     - <span data-ttu-id="ccdba-141">**SharePoint-Websites** – klicken Sie auf **Websites auswählen** , und klicken Sie dann erneut auf **Websites auswählen** , um zusätzliche SharePoint-und OneDrive für Business-Websites anzugeben, die Sie dem ausgewählten depotverwalter zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="ccdba-141">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you would like to assign to the selected custodian.</span></span> <span data-ttu-id="ccdba-142">Sie können auch die URL für die SharePoint-Website für eine Office 365-Gruppe oder ein Microsoft-Team hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-142">You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team.</span></span> <span data-ttu-id="ccdba-143">Geben Sie die URL für jede Website ein, die Sie zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="ccdba-143">Type the URL for each site that you want to assign.</span></span> <span data-ttu-id="ccdba-144">Klicken Sie auf **auswählen**und dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="ccdba-144">Click **Choose**, and then click **Done**.</span></span>
     - <span data-ttu-id="ccdba-145">**Microsoft Teams** – klicken Sie auf **Teams auswählen** , und klicken Sie dann erneut auf **Teams auswählen** , um eine Liste der Microsoft-Team Gruppen anzuzeigen, von denen die Depotbank heute Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="ccdba-145">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the custodian is a member of today.</span></span> <span data-ttu-id="ccdba-146">Wählen Sie die Teams aus, die Sie Ihrem depotverwalter hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="ccdba-146">Select the Teams that you would like to add to your custodian.</span></span> <span data-ttu-id="ccdba-147">Nach der Auswahl identifiziert das System automatisch & wählen Sie die zugeordnete SharePoint-Website und das Gruppenpostfach aus, die diesem Microsoft-Team zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="ccdba-147">Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team.</span></span> <span data-ttu-id="ccdba-148">Klicken Sie auf **auswählen**und dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="ccdba-148">Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="ccdba-149">Um zusätzliche Microsoft Teams hinzuzufügen, müssen Sie das Postfach und die SharePoint-Website, wie oben dargestellt, separat hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-149">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="ccdba-150">Nachdem Sie die Zuordnung Ihrer Quellen abgeschlossen haben, können Sie die Gesamtanzahl der Postfächer, Websites und Teams für die Verwalter anzeigen, die Sie soeben hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="ccdba-150">After you have finished mapping your sources, you can view the total mailboxes, sites, and Teams for the custodians that you have just added.</span></span> <span data-ttu-id="ccdba-151">Wenn Sie die für einen bestimmten Verwalter relevanten Datenquellen finalisiert haben, wird diese Zuordnung verwaltet und auf die eDiscovery-Sammlung, Verarbeitung und Überprüfung von Workflows ausgedehnt.</span><span class="sxs-lookup"><span data-stu-id="ccdba-151">When you've finalized the data sources relevant for a specific custodian, this mapping will be maintained and extended to the eDiscovery collection, processing, and review workflows.</span></span> 

## <a name="optional-step-4-place-custodians-on-hold"></a><span data-ttu-id="ccdba-152">Optional Schritt 4: Platzieren Sie Verwalter in der Warteschleife</span><span class="sxs-lookup"><span data-stu-id="ccdba-152">(Optional) Step 4: Place custodians on hold</span></span>

![Platz](../media/AddCustodianStep5.PNG)

<span data-ttu-id="ccdba-154">Nachdem Sie die Verwalter und Datenquellen, die Sie zu Ihrem Fall hinzufügen möchten, abgeschlossen haben, können Sie optional einige oder alle Ihre Verwalter aufbewahren.</span><span class="sxs-lookup"><span data-stu-id="ccdba-154">After you have finalized the custodians and data sources that you would like to add to your case, you can optionally place some or all of your custodians on hold.</span></span> <span data-ttu-id="ccdba-155">Wenn Sie eine Aufbewahrungsstelle aufbewahren, werden die diesem Benutzer zugeordneten Inhalte aufbewahrt, bis Sie die Depotbank aus dem Fall freigeben oder den Haltestatus löschen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-155">When you place a custodian on hold, the content mapped to that user is held until you release the custodian from the case or until you delete the hold.</span></span> <span data-ttu-id="ccdba-156">In einigen Fällen möchten Sie möglicherweise Verwalter zu einem Fall hinzufügen, ohne Sie zu halten.</span><span class="sxs-lookup"><span data-stu-id="ccdba-156">In some cases, you may want to add custodians to a case without placing them on hold.</span></span> 

<span data-ttu-id="ccdba-157">So platzieren Sie die ausgewählten Verwalter und Datenquellen in der Warteschleife:</span><span class="sxs-lookup"><span data-stu-id="ccdba-157">To place the selected custodians and data sources on hold:</span></span>

1. <span data-ttu-id="ccdba-158">Überprüfen Sie Ihre Depot Auswahl, und aktivieren Sie das Kontrollkästchen, um die Aufbewahrungszeit für jede Depotbank zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="ccdba-158">Verify your custodian selections and select the checkbox to place each custodian on hold.</span></span> <span data-ttu-id="ccdba-159">Nachdem eine Depotbank in der Warteschleife gehalten wurde, wird automatisch eine Depotbank-Aufbewahrungsrichtlinie erstellt, die alle Depot Quellen enthält.</span><span class="sxs-lookup"><span data-stu-id="ccdba-159">After a custodian is placed on hold, a custodian hold policy containing all custodial sources will be automatically created.</span></span> <span data-ttu-id="ccdba-160">Wenn die Option nicht aktiviert ist, werden die Depotbank und die ausgewählten Datenquellen dem Fall hinzugefügt, aber der Inhalt wird nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="ccdba-160">If the option is not checked, the custodian and selected data sources will be added to the case but the content will not be preserved.</span></span>

2. <span data-ttu-id="ccdba-161">Wechseln Sie zur Registerkarte halte **Status** , und wählen Sie die **Aufbewahrungsrichtlinie**aus.</span><span class="sxs-lookup"><span data-stu-id="ccdba-161">Go to the **Holds** tab and select the **Custodian Hold Policy**.</span></span> 

3. <span data-ttu-id="ccdba-162">Klicken Sie auf **Bearbeiten** , um alle ausgewählten Depotbank-Datenquellen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ccdba-162">Click **Edit** to view all the selected custodian data sources.</span></span>

   
