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
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: c36e0a2228db042d50361460e2e22f13556e8715
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218215"
---
# <a name="add-custodians-to-an-advanced-ediscovery-preview-case"></a><span data-ttu-id="af3e9-102">Hinzufügen von Bewahrern zu einem Advanced eDiscovery (Preview)-Fall</span><span class="sxs-lookup"><span data-stu-id="af3e9-102">Add custodians to an Advanced eDiscovery (Preview) case</span></span>

<span data-ttu-id="af3e9-p101">Mit Advanced eDiscovery (Preview) können Sie das integrierte Depot Verwaltungstool nutzen, um Ihre Workflows rund um die Verwaltung von Verwaltern und die Identifizierung relevanter, Freiheits enthaltener Datenquellen in einem Fall zu koordinieren. Wenn Sie eine Depotbank hinzufügen, kann das System die primären Exchange-Postfächer und die OneDrive for Business-Website automatisch identifizieren. Wenn Sie Ihre Ermittlung durchführen, können Sie auch zusätzliche Postfächer oder Websites aufdecken und zuordnen, auf die ein Verwalter in der Vergangenheit oder Teams zugegriffen hat, von denen ein Verwalter heute Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p101">Using Advanced eDiscovery (Preview), you can leverage the built-in custodian management tool to coordinate your workflows around managing custodians and identifying relevant, custodial data sources within a case. When you add a custodian, the system can automatically identify, and place holds on their primary Exchange mailbox and OneDrive for Business site. As you conduct your discovery, you might also uncover and map additional mailboxes or sites that a custodian accessed in the past or Teams that a custodian is a member of today.</span></span>

<span data-ttu-id="af3e9-106">Verwenden Sie den folgenden Workflow, um Verwalter in Advanced eDiscovery (Preview)-Fällen im Security & Compliance Center hinzuzufügen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="af3e9-106">Use the following workflow to add and manage custodians in Advanced eDiscovery (Preview) cases within the Security & Compliance Center.</span></span> 

## <a name="step-1-identify-potential-custodians"></a><span data-ttu-id="af3e9-107">Schritt 1: Identifizieren potenzieller Verwalter</span><span class="sxs-lookup"><span data-stu-id="af3e9-107">Step 1: Identify potential custodians</span></span>

<span data-ttu-id="af3e9-p102">Der erste Schritt besteht darin, die geeigneten Verwalter für Ihre Angelegenheit zu identifizieren. Um einem Fall Verwalter hinzuzufügen, müssen Sie Mitglied der Rollengruppe "eDiscovery-Manager" oder "eDiscovery-Admins" sein.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p102">The first step is to identify the appropriate custodians for your matter. To add custodians to a case, you must be a member of the eDiscovery Managers or eDiscovery Admins role group.</span></span>   

<span data-ttu-id="af3e9-110">So fügen Sie einem vorhandenen Advanced eDiscovery (Preview)-Fall Verwalter hinzu:</span><span class="sxs-lookup"><span data-stu-id="af3e9-110">To add custodians to an existing Advanced eDiscovery (Preview) case:</span></span>

1. <span data-ttu-id="af3e9-111">Wechseln Sie auf der Seite **Advanced eDiscovery (Preview)** zu Ihrem Fall.</span><span class="sxs-lookup"><span data-stu-id="af3e9-111">From the **Advanced eDiscovery (Preview)** page, go to your case.</span></span>
 
2. <span data-ttu-id="af3e9-112">Nachdem Sie einen Fall ausgewählt haben, wechseln Sie zur \*\*\*\* Registerkarte depotbanks, und klicken Sie auf **+ Depotbank hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="af3e9-112">After you have selected a case, go to the **Custodians** tab and click **+ Add Custodian**.</span></span> 
 
3. <span data-ttu-id="af3e9-p103">Wählen Sie die Verwalter aus, die Sie der Anfrage hinzufügen möchten. Sie können zunächst eingeben, um die Benutzer aus Azure Active Directory Ihrer Organisation zu suchen und auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p103">Choose the custodians that you want to add to the case. You can start by typing to search and select the users from your organization's Azure Active Directory.</span></span>
 
4. <span data-ttu-id="af3e9-115">Nachdem Sie die Liste der Verwalter abgeschlossen haben, klicken Sie auf **weiter** , um mit der Identifizierung potenzieller Datenquellen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="af3e9-115">After you have finalized the list of custodians, click **Next** to begin identifying potential data sources.</span></span> 
   
## <a name="optional-step-2-select-custodian-data-sources"></a><span data-ttu-id="af3e9-116">Optional Schritt 2: Auswählen von Depotbank-Datenquellen</span><span class="sxs-lookup"><span data-stu-id="af3e9-116">(Optional) Step 2: Select custodian data sources</span></span>

<span data-ttu-id="af3e9-p104">Nachdem Sie einem Fall Verwalter hinzugefügt haben, können Sie Office 365 für die Identifizierung und Aufbewahrung der primären Depotbank-Datenquellen nutzen. Im nächsten Schritt dieses Workflows werden die Datenquellen ausgewählt, die den in Schritt 1 angegebenen depotbanks gehören.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p104">After you have added custodians to a case, you can leverage Office 365 to help you identify and preserve the primary custodian data sources. The next step in this workflow is to select the data sources owned by the custodians specified in Step 1.</span></span> 

<span data-ttu-id="af3e9-119">So identifizieren Sie Depotbank-Datenquellen:</span><span class="sxs-lookup"><span data-stu-id="af3e9-119">To identify custodian data sources:</span></span> 

1. <span data-ttu-id="af3e9-120">Wählen Sie für jede Depotbank **Exchange** aus, wenn das primäre Exchange-Postfach des Depot Systems automatisch ermittelt und hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="af3e9-120">For each custodian, select **Exchange** if you would like the system to automatically identify and add the custodian's primary Exchange mailbox.</span></span> 
 
2. <span data-ttu-id="af3e9-121">Wählen Sie für jede Depotbank **OneDrive** aus, wenn Sie möchten, dass das System die primäre ONEDRIVE-URL der Depotbank automatisch identifiziert und hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="af3e9-121">For each custodian, select **OneDrive** if you would like the system to automatically identify and add the custodian's primary OneDrive URL.</span></span> 

    <span data-ttu-id="af3e9-122">Nachdem Sie Ihre Auswahl getroffen haben, versucht das System automatisch, die Datenquellen zu identifizieren und zu Ihrem Fall hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="af3e9-122">After you've made your selections, they system will automatically try to identify the data sources and add them to your case.</span></span>
 
4. <span data-ttu-id="af3e9-123">Klicken Sie auf **weiter** , um mit dem Zuordnen zusätzlicher Datenquellen zur Depotbank zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="af3e9-123">Click **Next** to begin mapping additional data sources to your custodian.</span></span>

## <a name="optional-step-3-map-additional-data-sources"></a><span data-ttu-id="af3e9-124">Optional Schritt 3: Zuordnen zusätzlicher Datenquellen</span><span class="sxs-lookup"><span data-stu-id="af3e9-124">(Optional) Step 3: Map additional data sources</span></span>

<span data-ttu-id="af3e9-p105">Je nach Fall möchten Sie möglicherweise auch Postfächer hinzufügen, die ein bestimmter Depotbank in der Vergangenheit verwendet haben kann, Gruppen, in denen ein Depotbank derzeit Mitglied ist, oder Websites, auf die ein Verwalter in der Vergangenheit Zugriff hatte. Zusätzlich zu den primären Depotbank-Datenquellen können Sie zusätzliche Office 365-Datenquellen einem depotverwalter hinzufügen oder Office 365 nutzen, um potenziell relevante Datenquellen zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p105">Depending on your case, you may also want to add mailboxes that a given custodian may have used in the past, groups where a custodian is currently a member, or sites that a custodian had access to in the past. In addition to primary custodian data sources, you can add additional Office 365 data sources to a custodian or leverage Office 365 to help you identify potentially relevant data sources as well.</span></span> 

<span data-ttu-id="af3e9-127">Zuordnen von Postfächern, Websites oder Teams zu einem bestimmten Depot:</span><span class="sxs-lookup"><span data-stu-id="af3e9-127">To map mailboxes, sites, or teams to a specific custodian:</span></span>

1. <span data-ttu-id="af3e9-128">Wählen Sie **Aktualisieren** aus, um einem bestimmten Verwalter inhaltsspeicherorte wie Postfächer, Websites und Teams zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="af3e9-128">Select **Update** to assign content locations, like mailboxes, sites, and Teams to a specific custodian.</span></span> 

2. <span data-ttu-id="af3e9-129">Geben Sie im Flyout Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="af3e9-129">In the flyout, specify the following:</span></span>
   
  -  <span data-ttu-id="af3e9-p106">**Exchange-Postfächer** – klicken Sie auf **Benutzer, Gruppen oder Teams auswählen** , und klicken Sie dann erneut auf **Benutzer, Gruppen oder Teams auswählen** . Zum Angeben von Postfächern, die dem ausgewählten depotverwalter zugewiesen werden sollen, verwenden Sie das Suchfeld, um nach Benutzerpostfächern und Verteilergruppen zu suchen. Sie können auch das zugeordnete Postfach für eine Office 365-Gruppe oder ein Microsoft-Team zuweisen. Aktivieren Sie das Kontrollkästchen Benutzer, Gruppe, Team, klicken Sie auf **auswählen**, und klicken Sie dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p106">**Exchange Mailboxes** - Click **Choose users, groups, or Teams** and then click **Choose users, groups, or teams** again. To specify mailboxes to assign to the selected custodian, use the search box to find user mailboxes and distribution groups. You can also assign the associated mailbox for an Office 365 Group or a Microsoft Team. Select the user, group, team check box, click **Choose**, and then click **Done**.</span></span>

      > [!NOTE]
      > <span data-ttu-id="af3e9-p107">Wenn Sie auf Benutzer, Gruppen oder Teams zum Angeben von Postfächern klicken, ist die angezeigte Post Fachauswahl leer. Dies ist beabsichtigt, um die Leistung zu verbessern. Wenn Sie Personen zu dieser Liste hinzufügen möchten, geben Sie einen Namen (mindestens 3 Zeichen) in das Suchfeld ein.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p107">When you click Choose users, groups, or teams to specify mailboxes, the mailbox picker that's displayed is empty. This is by design to enhance performance. To add people to this list, type a name (a minimum of 3 characters) in the search box.</span></span>
     
   - <span data-ttu-id="af3e9-p108">**SharePoint-Websites** – klicken Sie auf **Websites auswählen** , und klicken Sie dann erneut auf **Websites auswählen** , um zusätzliche SharePoint-und OneDrive für Business-Websites anzugeben, die Sie dem ausgewählten depotverwalter zuweisen möchten. Sie können auch die URL für die SharePoint-Website für eine Office 365-Gruppe oder ein Microsoft-Team hinzufügen. Geben Sie die URL für jede Website ein, die Sie zuweisen möchten. Klicken Sie auf **auswählen**und dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p108">**SharePoint Sites** - Click **Choose sites** and then click **Choose sites** again to specify additional SharePoint and OneDrive for Business sites that you would like to assign to the selected custodian. You can also add the URL for the SharePoint site for an Office 365 Group or a Microsoft Team. Type the URL for each site that you want to assign. Click **Choose**, and then click **Done**.</span></span>
   - <span data-ttu-id="af3e9-p109">**Microsoft Teams** – klicken Sie auf **Teams auswählen** , und klicken Sie dann erneut auf **Teams auswählen** , um eine Liste der Microsoft-Team Gruppen anzuzeigen, von denen die Depotbank heute Mitglied ist. Wählen Sie die Teams aus, die Sie Ihrem depotverwalter hinzufügen möchten. Nach der Auswahl identifiziert das System automatisch & wählen Sie die zugeordnete SharePoint-Website und das Gruppenpostfach aus, die diesem Microsoft-Team zugeordnet sind. Klicken Sie auf **auswählen**und dann auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p109">**Microsoft Teams** – Click **Choose Teams** and then click **Choose Teams** again to view a list of Microsoft Team groups that the custodian is a member of today. Select the Teams that you would like to add to your custodian. Once selected, the system will automatically identify & select the associated SharePoint site and Group Mailbox associated to that Microsoft Team. Click **Choose**, and then click **Done**.</span></span>
        
      > [!NOTE]
      > <span data-ttu-id="af3e9-145">Um zusätzliche Microsoft Teams hinzuzufügen, müssen Sie das Postfach und die SharePoint-Website, wie oben dargestellt, separat hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="af3e9-145">To add additional Microsoft Teams, you will need to separately add the mailbox and SharePoint site as shown above.</span></span>

<span data-ttu-id="af3e9-p110">Nachdem Sie die Zuordnung Ihrer Quellen abgeschlossen haben, können Sie die Gesamtanzahl der Postfächer, Websites und Teams für die Verwalter anzeigen, die Sie soeben hinzugefügt haben. Wenn Sie die für einen bestimmten Verwalter relevanten Datenquellen finalisiert haben, wird diese Zuordnung verwaltet und auf die eDiscovery-Sammlung, Verarbeitung und Überprüfung von Workflows ausgedehnt.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p110">After you have finished mapping your sources, you can view the total mailboxes, sites, and Teams for the custodians that you have just added. When you've finalized the data sources relevant for a specific custodian, this mapping will be maintained and extended to the eDiscovery collection, processing, and review workflows.</span></span> 

## <a name="optional-step-4-place-custodians-on-hold"></a><span data-ttu-id="af3e9-148">Optional Schritt 4: Platzieren Sie Verwalter in der Warteschleife</span><span class="sxs-lookup"><span data-stu-id="af3e9-148">(Optional) Step 4: Place custodians on hold</span></span>

 <span data-ttu-id="af3e9-p111">Nachdem Sie die Verwalter und Datenquellen, die Sie zu Ihrem Fall hinzufügen möchten, abgeschlossen haben, können Sie optional einige oder alle Ihre Verwalter aufbewahren. Wenn Sie eine Aufbewahrungsstelle aufbewahren, werden die diesem Benutzer zugeordneten Inhalte aufbewahrt, bis Sie die Depotbank aus dem Fall freigeben oder den Haltestatus löschen. In einigen Fällen möchten Sie möglicherweise Verwalter zu einem Fall hinzufügen, ohne Sie zu halten.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p111">After you have finalized the custodians and data sources that you would like to add to your case, you can optionally place some or all of your custodians on hold. When you place a custodian on hold, the content mapped to that user is held until you release the custodian from the case or until you delete the hold. In some cases, you may want to add custodians to a case without placing them on hold.</span></span> 

<span data-ttu-id="af3e9-152">So platzieren Sie die ausgewählten Verwalter und Datenquellen in der Warteschleife:</span><span class="sxs-lookup"><span data-stu-id="af3e9-152">To place the selected custodians and data sources on hold:</span></span>

1. <span data-ttu-id="af3e9-p112">Überprüfen Sie Ihre Depot Auswahl, und aktivieren Sie das Kontrollkästchen, um die Aufbewahrungszeit für jede Depotbank zu platzieren. Sobald eine Depotbank in der Warteschleife gehalten wird, wird automatisch eine Richtlinie für den Aufbewahrungs Schutz erstellt, die alle Depot Quellen enthält. Wenn die Option nicht aktiviert ist, wird die Depotbank & ausgewählte Datenquellen zu dem Fall hinzugefügt, aber der Inhalt wird nicht beibehalten.</span><span class="sxs-lookup"><span data-stu-id="af3e9-p112">Verify your custodian selections and select the checkbox to place each custodian on hold.Once a custodian is placed on hold, a custodian hold policy containing all custodial sources will automatically be created. If the option is not checked, the custodian & selected data sources will be added to the case but the content will not be preserved.</span></span>

2. <span data-ttu-id="af3e9-155">Wechseln Sie zur Registerkarte halte **Status** , und wählen Sie die **Aufbewahrungsrichtlinie**aus.</span><span class="sxs-lookup"><span data-stu-id="af3e9-155">Go to the **Holds** tab and select the **Custodian Hold Policy**.</span></span> 

3. <span data-ttu-id="af3e9-156">Klicken Sie auf **Bearbeiten** , um alle ausgewählten Depotbank-Datenquellen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="af3e9-156">Click **Edit** to view all the selected custodian data sources.</span></span>
