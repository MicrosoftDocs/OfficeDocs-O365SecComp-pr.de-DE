---
title: 'Exchange-Verwaltungskonsole in Exchange Online Protection '
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
description: Die Exchange-Verwaltungskonsole (EAC) ist die webbasierte Verwaltungskonsole für Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: 99640e561b41e47a74e7c22f0bbdcacd0dd80bd7
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026312"
---
# <a name="exchange-admin-center-in-exchange-online-protection"></a><span data-ttu-id="3032c-103">Exchange-Verwaltungskonsole in Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="3032c-103">Exchange admin center in Exchange Online Protection</span></span> 

<span data-ttu-id="3032c-104">Die Exchange-Verwaltungskonsole (EAC) ist die webbasierte Verwaltungskonsole für Microsoft Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="3032c-104">The Exchange admin center (EAC) is the web-based management console for Microsoft Exchange Online Protection (EOP).</span></span> 
  
<span data-ttu-id="3032c-p101">Suchen Sie die Exchange 2013-Version dieses Themas? Weitere Informationen finden Sie unter [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span><span class="sxs-lookup"><span data-stu-id="3032c-p101">Looking for the Exchange 2013 version of this topic? See [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span></span>
  
<span data-ttu-id="3032c-p102">Suchen Sie die Exchange Online-Version dieses Themas? Weitere Informationen finden Sie unter [Exchange admin center in Exchange Online](http://technet.microsoft.com/library/ace44f6b-4084-4f9c-89b3-e0317962472b.aspx).</span><span class="sxs-lookup"><span data-stu-id="3032c-p102">Looking for the Exchange Online version of this topic? See [Exchange admin center in Exchange Online](http://technet.microsoft.com/library/ace44f6b-4084-4f9c-89b3-e0317962472b.aspx).</span></span>
  
## <a name="accessing-the-eac"></a><span data-ttu-id="3032c-109">Zugreifen auf die Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="3032c-109">Accessing the EAC</span></span>

<span data-ttu-id="3032c-p103">In den meisten Fällen greifen EOP-Kunden über das Office 365 Admin Center auf die Exchange-Verwaltungskonsole (EAC) zu. Einen Link zu EOP finden Sie im Dropdownmenü der **Admin**-Kachel, die sich neben der **Ich**-Kachel befindet. Klicken Sie auf die **Admin**-Kachel, und wählen Sie im Dropdownmenü **Exchange Online Protection**, um die Exchange-Verwaltungskonsole aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3032c-p103">In most cases, EOP customers will access the EAC through the Office 365 admin center. You can find a link to EOP in the drop-down menu in the **Admin** tile, which is next to the **Me** tile. Click the **Admin** tile and select **Exchange Online Protection** from the drop down menu to be taken to the EAC.</span></span> 
  
<span data-ttu-id="3032c-p104">Sie können auch über den folgenden URL direkt auf das EAC-Zeichen auf der Seite zugreifen: https://admin.protection.outlook.com/ecp/\<companydomain\>. Beispiel: https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. Nachdem Sie Ihre Benutzeranmeldeinformationen eingegeben haben, gelangen Sie direkt zur Exchange-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="3032c-p104">You can also access the EAC sign in page directly via the following URL: https://admin.protection.outlook.com/ecp/\<companydomain\>. For example, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. After specifying your user credentials you will be taken directly into the EAC.</span></span>
  
## <a name="common-user-interface-elements-in-the-eac"></a><span data-ttu-id="3032c-116">Allgemeine Elemente der Benutzeroberfläche in der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="3032c-116">Common user interface elements in the EAC</span></span>
<span data-ttu-id="3032c-117"><a name="BKMK_CommonUserInterfaceElements"> </a></span><span class="sxs-lookup"><span data-stu-id="3032c-117"></span></span>

<span data-ttu-id="3032c-118">In diesem Abschnitt werden die Elemente der Benutzeroberfläche der Exchange-Verwaltungskonsole beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3032c-118">This section describes the user interface elements that are found in the EAC.</span></span>
  
![EOP-AdminCenter](media/EOP-AdminCenter.png)
  
### <a name="feature-pane"></a><span data-ttu-id="3032c-120">Featurebereich</span><span class="sxs-lookup"><span data-stu-id="3032c-120">Feature Pane</span></span>

<span data-ttu-id="3032c-p105">Dies ist die erste Navigationsebene für die meisten Aufgaben, die Sie in der Exchange-Verwaltungskonsole ausführen. Der Featurebereich ist nach Funktionsbereichen organisiert.</span><span class="sxs-lookup"><span data-stu-id="3032c-p105">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>
  
1. <span data-ttu-id="3032c-123">**Empfänger** Mit diesem Feature können Sie interne Benutzer und externe Kontakte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3032c-123">**Recipients** This is where you'll view internal users and external contacts.</span></span> 
    
2. <span data-ttu-id="3032c-124">**Berechtigungen** Mit diesem Feature können Sie Administratorrollen verwalten.</span><span class="sxs-lookup"><span data-stu-id="3032c-124">**Permissions** This where you'll manage administrator roles.</span></span> 
    
3. <span data-ttu-id="3032c-125">**Verwaltung der Richtlinientreue** Hier finden Sie Überwachungsprotokolle und Berichte wie den Administrator-Rollengruppenbericht.</span><span class="sxs-lookup"><span data-stu-id="3032c-125">**Compliance Management** This is where you'll find audit logs and reports, such as the administrator role group report.</span></span> 
    
4. <span data-ttu-id="3032c-126">**Schutz** Mit diesem Feature können Sie Antischadsoftware- und Antispamschutz für Ihre Organisation sowie isolierte Nachrichten verwalten.</span><span class="sxs-lookup"><span data-stu-id="3032c-126">**Protection** This is where you'll manage anti-malware and anti-spam protection for your organization, as well as manage messages in quarantine.</span></span> 
    
5. <span data-ttu-id="3032c-127">**Nachrichtenfluss** Mit diesem Feature können Sie Regeln, akzeptierte Domänen und Connectors verwalten sowie festlegen, wo die Nachrichtenablaufverfolgung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3032c-127">**Mail Flow** This is where you'll manage rules, accepted domains, and connectors, as well as where you'll go to perform message trace.</span></span> 
    
### <a name="tabs"></a><span data-ttu-id="3032c-128">Registerkarten</span><span class="sxs-lookup"><span data-stu-id="3032c-128">Tabs</span></span>

<span data-ttu-id="3032c-p106">Die Registerkarten sind Ihre zweite Ebene der Navigation. Alle Featurebereiche enthalten verschiedene Registerkarten, die jeweils ein Feature repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="3032c-p106">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>
  
### <a name="toolbar"></a><span data-ttu-id="3032c-131">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="3032c-131">Toolbar</span></span>

<span data-ttu-id="3032c-p107">Für die meisten Registerkarten wird eine Symbolleiste angezeigt, nachdem Sie auf sie geklickt haben. Die Symbolleiste enthält Symbole, die jeweils eine bestimmte Aktion auslösen. Die folgende Tabelle beschreibt die Symbole und deren Aktionen.</span><span class="sxs-lookup"><span data-stu-id="3032c-p107">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>
  
|<span data-ttu-id="3032c-135">**Symbol**</span><span class="sxs-lookup"><span data-stu-id="3032c-135">**Icon**</span></span>|<span data-ttu-id="3032c-136">**Name**</span><span class="sxs-lookup"><span data-stu-id="3032c-136">**Name**</span></span>|<span data-ttu-id="3032c-137">**Action**</span><span class="sxs-lookup"><span data-stu-id="3032c-137">**Action**</span></span>|
|:-----|:-----|:-----|
|![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.png)           <br/> |<span data-ttu-id="3032c-139">Hinzufügen, Neu</span><span class="sxs-lookup"><span data-stu-id="3032c-139">Add, New</span></span>  <br/> |<span data-ttu-id="3032c-p108">Über dieses Symbol können Sie ein neues Objekt erstellen. Bei einigen dieser Symbole gibt es einen dazugehörigen nach unten zeigenden Pfeil, auf den Sie klicken können, um weitere Objekte anzuzeigen, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="3032c-p108">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>  <br/> |
|![Bearbeitungssymbol](media/ITPro-EAC-EditIcon.png)           <br/> |<span data-ttu-id="3032c-143">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="3032c-143">Edit</span></span>  <br/> |<span data-ttu-id="3032c-144">Über dieses Symbol können Sie ein Objekt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="3032c-144">Use this icon to edit an object.</span></span>  <br/> |
|![Löschen (Symbol)](media/ITPro-EAC-DeleteIcon.png)           <br/> |<span data-ttu-id="3032c-146">Löschen</span><span class="sxs-lookup"><span data-stu-id="3032c-146">Delete</span></span>  <br/> |<span data-ttu-id="3032c-p109">Über dieses Symbol können Sie ein Objekt löschen. Bei einigen Löschsymbolen gibt es einen nach unten zeigenden Pfeil, auf den Sie zum Einblenden weiterer Optionen klicken können.</span><span class="sxs-lookup"><span data-stu-id="3032c-p109">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>  <br/> |
|![Suchen (Symbol)](media/ITPro-EAC-.png)           <br/> |<span data-ttu-id="3032c-150">Suche</span><span class="sxs-lookup"><span data-stu-id="3032c-150">Search</span></span>  <br/> |<span data-ttu-id="3032c-151">Über dieses Symbol können Sie ein Suchfeld öffnen, in das Sie den Suchbegriff für ein zu suchendes Objekt eingeben können.</span><span class="sxs-lookup"><span data-stu-id="3032c-151">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>  <br/> |
|![Aktualisieren (Symbol)](media/ITPro-EAC-RefreshIcon.png)           <br/> |<span data-ttu-id="3032c-153">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="3032c-153">Refresh</span></span>  <br/> |<span data-ttu-id="3032c-154">Über dieses Symbol können Sie die Listenansicht aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3032c-154">Use this icon to refresh the list view.</span></span>  <br/> |
|![Weitere Optionen (Symbol)](media/ITPro-EAC-MoreOptionsIcon.png)           <br/> |<span data-ttu-id="3032c-156">Weitere Optionen</span><span class="sxs-lookup"><span data-stu-id="3032c-156">More options</span></span>  <br/> |<span data-ttu-id="3032c-p110">Über dieses Symbol können Sie mehrere Aktionen anzeigen, die Sie auf die Objekte dieser Registerkarte anwenden können. Wenn Sie z. B. unter **Empfänger \> Benutzer** auf dieses Symbol klicken, wird die Option **Erweiterte Suche** angezeigt.  </span><span class="sxs-lookup"><span data-stu-id="3032c-p110">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.  </span></span><br/> |
|![NACH-OBEN-TASTE (Symbol)](media/ITPro-EAC-UpArrowIcon.png)![NACH-UNTEN-TASTE (Symbol)](media/ITPro-EAC-DownArrowIcon.png)           <br/> |<span data-ttu-id="3032c-161">Pfeil nach oben und Pfeil nach unten</span><span class="sxs-lookup"><span data-stu-id="3032c-161">Up arrow and down arrow</span></span>  <br/> |<span data-ttu-id="3032c-162">Mithilfe dieser Symbole können Sie die Priorität eines Objekts nach oben oder unten verschieben.</span><span class="sxs-lookup"><span data-stu-id="3032c-162">Use these icons to move an object's priority up or down.</span></span>  <br/> |
|![Entfernen (Symbol)](media/ITPro-EAC-RemoveIcon.png)           <br/> |<span data-ttu-id="3032c-164">Entfernen</span><span class="sxs-lookup"><span data-stu-id="3032c-164">Remove</span></span>  <br/> |<span data-ttu-id="3032c-165">Über dieses Symbol können Sie Objekte aus einer Liste entfernen.</span><span class="sxs-lookup"><span data-stu-id="3032c-165">Use this icon to remove objects from a list.</span></span>  <br/> |
   
### <a name="list-view"></a><span data-ttu-id="3032c-166">Listenansicht</span><span class="sxs-lookup"><span data-stu-id="3032c-166">List View</span></span>

<span data-ttu-id="3032c-p111">Wenn Sie auf eine Registerkarte klicken, sehen Sie in den meisten Fällen eine Listenansicht. In der Listenansicht der Exchange-Verwaltungskonsole können ungefähr 10.000 Objekte angezeigt werden. Darüber hinaus können Sie die Ergebnisse seitenweise anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3032c-p111">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>
  
### <a name="details-pane"></a><span data-ttu-id="3032c-170">Detailbereich</span><span class="sxs-lookup"><span data-stu-id="3032c-170">Details Pane</span></span>

<span data-ttu-id="3032c-p112">Wenn Sie in der Listenansicht ein Objekt auswählen, werden Informationen zu diesem Objekt im Detailbereich angezeigt. In einigen Fällen enthält der Detailbereich Verwaltungsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="3032c-p112">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>
  
### <a name="me-tile-and-help"></a><span data-ttu-id="3032c-173">Ich-Kachel und Hilfe</span><span class="sxs-lookup"><span data-stu-id="3032c-173">Me tile and Help</span></span>

<span data-ttu-id="3032c-p113">Über die **Ich**-Kachel können Sie sich bei der Exchange-Verwaltungskonsole abmelden und als ein anderer Benutzer anmelden. Über das Dropdownmenü der **Hilfe**![Hilfe (Symbol)](media/ITPro-EAC-HelpIcon.png) können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="3032c-p113">The **Me** tile allows you to sign out the EAC and sign in as a different user. From the **Help**![Help Icon](media/ITPro-EAC-HelpIcon.png) drop-down menu, you can perform the following actions:</span></span> 
  
1. <span data-ttu-id="3032c-176">**Hilfe** Klicken Sie auf ![Hilfe (Symbol)](media/ITPro-EAC-HelpIcon.png), damit der Inhalt der Onlinehilfe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="3032c-176">**Help** Click ![Help Icon](media/ITPro-EAC-HelpIcon.png) to view the online help content.</span></span> 
    
2. <span data-ttu-id="3032c-p114">**Hilfe-Sprechblase deaktivieren** In der Hilfe-Sprechblase wird Kontexthilfe für Felder angezeigt, wenn Sie ein Objekt erstellen oder bearbeiten. Sie können die Hilfe-Sprechblase deaktivieren bzw. aktivieren, wenn sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3032c-p114">**Disable Help bubble** The Help bubble displays contextual help for fields when you create or edit an object. You can turn off the Help bubble or turn it on if it has been disabled.</span></span> 
    
3. <span data-ttu-id="3032c-179">**Copyright** Klicken Sie auf diesen Link, um den Copyright-Hinweis für Exchange Online Protection zu lesen.</span><span class="sxs-lookup"><span data-stu-id="3032c-179">**Copyright** Click this link to read the copyright notice for Exchange Online Protection.</span></span> 
    
4. <span data-ttu-id="3032c-180">**Datenschutz** Klicken Sie hier, um die Datenschutzrichtlinien für Exchange Online Protection zu lesen.</span><span class="sxs-lookup"><span data-stu-id="3032c-180">**Privacy** Click to read the privacy policy for Exchange Online Protection.</span></span> 
    
## <a name="supported-browsers"></a><span data-ttu-id="3032c-181">Unterstützte Browser</span><span class="sxs-lookup"><span data-stu-id="3032c-181">Supported Browsers</span></span>
<span data-ttu-id="3032c-182"><a name="BKMK_SupportedBrowsers"> </a></span><span class="sxs-lookup"><span data-stu-id="3032c-182"></span></span>

<span data-ttu-id="3032c-p115">Für eine optimale Nutzung des EAC sollten Sie immer die neuesten Browser, Office-Clients und Apps verwenden. Zudem wird empfohlen, dass Sie Softwareupdates installieren, sobald sie verfügbar werden. Weitere Informationen zu den unterstützten Browsern und zu den Systemanforderungen für den Dienst finden Sie unter [Office 365-Systemanforderungen](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span><span class="sxs-lookup"><span data-stu-id="3032c-p115">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps. We also recommend that you install software updates when they become available. For more information about the supported browsers and system requirements for the service, see [Office 365 System Requirements](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span></span> 
  
## <a name="supported-languages-in-eop"></a><span data-ttu-id="3032c-186">Unterstützte Sprachen in EOP</span><span class="sxs-lookup"><span data-stu-id="3032c-186">Supported languages in EOP</span></span>
<span data-ttu-id="3032c-187"><a name="BKMK_SupportedLanguages"> </a></span><span class="sxs-lookup"><span data-stu-id="3032c-187"></span></span>

<span data-ttu-id="3032c-188">Die folgenden Sprachen werden für Exchange Online Protection unterstützt und zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="3032c-188">The following languages are supported and available for Exchange Online Protection.</span></span>
  
- <span data-ttu-id="3032c-189">Amharisch</span><span class="sxs-lookup"><span data-stu-id="3032c-189">Amharic</span></span>
    
- <span data-ttu-id="3032c-190">Arabisch</span><span class="sxs-lookup"><span data-stu-id="3032c-190">Arabic</span></span>
    
- <span data-ttu-id="3032c-191">Baskisch (Baskisch)</span><span class="sxs-lookup"><span data-stu-id="3032c-191">Basque (Basque)</span></span>
    
- <span data-ttu-id="3032c-192">Bengali (Indien)</span><span class="sxs-lookup"><span data-stu-id="3032c-192">Bengali (India)</span></span>
    
- <span data-ttu-id="3032c-193">Bulgarisch</span><span class="sxs-lookup"><span data-stu-id="3032c-193">Bulgarian</span></span>
    
- <span data-ttu-id="3032c-194">Katalanisch</span><span class="sxs-lookup"><span data-stu-id="3032c-194">Catalan</span></span>
    
- <span data-ttu-id="3032c-195">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="3032c-195">Chinese (Simplified)</span></span>
    
- <span data-ttu-id="3032c-196">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="3032c-196">Chinese (Traditional)</span></span>
    
- <span data-ttu-id="3032c-197">Kroatisch</span><span class="sxs-lookup"><span data-stu-id="3032c-197">Croatian</span></span>
    
- <span data-ttu-id="3032c-198">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="3032c-198">Czech</span></span>
    
- <span data-ttu-id="3032c-199">Dänisch</span><span class="sxs-lookup"><span data-stu-id="3032c-199">Danish</span></span>
    
- <span data-ttu-id="3032c-200">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="3032c-200">Dutch</span></span>
    
- <span data-ttu-id="3032c-201">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="3032c-201">Dutch</span></span>
    
- <span data-ttu-id="3032c-202">Englisch</span><span class="sxs-lookup"><span data-stu-id="3032c-202">English</span></span>
    
- <span data-ttu-id="3032c-203">Estnisch</span><span class="sxs-lookup"><span data-stu-id="3032c-203">Estonian</span></span>
    
- <span data-ttu-id="3032c-204">Filipino (Philippinen)</span><span class="sxs-lookup"><span data-stu-id="3032c-204">Filipino (Philippines)</span></span>
    
- <span data-ttu-id="3032c-205">Finnisch</span><span class="sxs-lookup"><span data-stu-id="3032c-205">Finnish</span></span>
    
- <span data-ttu-id="3032c-206">Französisch</span><span class="sxs-lookup"><span data-stu-id="3032c-206">French</span></span>
    
- <span data-ttu-id="3032c-207">Galicisch</span><span class="sxs-lookup"><span data-stu-id="3032c-207">Galician</span></span>
    
- <span data-ttu-id="3032c-208">Deutsch</span><span class="sxs-lookup"><span data-stu-id="3032c-208">German</span></span>
    
- <span data-ttu-id="3032c-209">Griechisch</span><span class="sxs-lookup"><span data-stu-id="3032c-209">Greek</span></span>
    
- <span data-ttu-id="3032c-210">Gujarati</span><span class="sxs-lookup"><span data-stu-id="3032c-210">Gujarati</span></span>
    
- <span data-ttu-id="3032c-211">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="3032c-211">Hebrew</span></span>
    
- <span data-ttu-id="3032c-212">Hindi</span><span class="sxs-lookup"><span data-stu-id="3032c-212">Hindi</span></span>
    
- <span data-ttu-id="3032c-213">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="3032c-213">Hungarian</span></span>
    
- <span data-ttu-id="3032c-214">Isländisch</span><span class="sxs-lookup"><span data-stu-id="3032c-214">Icelandic</span></span>
    
- <span data-ttu-id="3032c-215">Indonesisch</span><span class="sxs-lookup"><span data-stu-id="3032c-215">Indonesian</span></span>
    
- <span data-ttu-id="3032c-216">Italienisch</span><span class="sxs-lookup"><span data-stu-id="3032c-216">Italian</span></span>
    
- <span data-ttu-id="3032c-217">Japanisch</span><span class="sxs-lookup"><span data-stu-id="3032c-217">Japanese</span></span>
    
- <span data-ttu-id="3032c-218">Kannada</span><span class="sxs-lookup"><span data-stu-id="3032c-218">Kannada</span></span>
    
- <span data-ttu-id="3032c-219">Kasachisch</span><span class="sxs-lookup"><span data-stu-id="3032c-219">Kazakh</span></span>
    
- <span data-ttu-id="3032c-220">Kisuaheli</span><span class="sxs-lookup"><span data-stu-id="3032c-220">Kiswahili</span></span>
    
- <span data-ttu-id="3032c-221">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="3032c-221">Korean</span></span>
    
- <span data-ttu-id="3032c-222">Lettisch</span><span class="sxs-lookup"><span data-stu-id="3032c-222">Latvian</span></span>
    
- <span data-ttu-id="3032c-223">Litauisch</span><span class="sxs-lookup"><span data-stu-id="3032c-223">Lithuanian</span></span>
    
- <span data-ttu-id="3032c-224">Malaiisch (Brunei Darussalam)</span><span class="sxs-lookup"><span data-stu-id="3032c-224">Malay (Brunei Darussalam)</span></span>
    
- <span data-ttu-id="3032c-225">Malaiisch (Malaysia)</span><span class="sxs-lookup"><span data-stu-id="3032c-225">Malay (Malaysia)</span></span>
    
- <span data-ttu-id="3032c-226">Malayalam</span><span class="sxs-lookup"><span data-stu-id="3032c-226">Malayalam</span></span>
    
- <span data-ttu-id="3032c-227">Marathi</span><span class="sxs-lookup"><span data-stu-id="3032c-227">Marathi</span></span>
    
- <span data-ttu-id="3032c-228">Norwegisch (Bokmål)</span><span class="sxs-lookup"><span data-stu-id="3032c-228">Norwegian (Bokmål)</span></span>
    
- <span data-ttu-id="3032c-229">Norwegisch (Nynorsk)</span><span class="sxs-lookup"><span data-stu-id="3032c-229">Norwegian (Nynorsk)</span></span>
    
- <span data-ttu-id="3032c-230">Odia</span><span class="sxs-lookup"><span data-stu-id="3032c-230">Oriya</span></span>
    
- <span data-ttu-id="3032c-231">Persisch</span><span class="sxs-lookup"><span data-stu-id="3032c-231">Persian</span></span>
    
- <span data-ttu-id="3032c-232">Polnisch</span><span class="sxs-lookup"><span data-stu-id="3032c-232">Polish</span></span>
    
- <span data-ttu-id="3032c-233">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="3032c-233">Portuguese (Brazil)</span></span>
    
- <span data-ttu-id="3032c-234">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="3032c-234">Portuguese (Portugal)</span></span>
    
- <span data-ttu-id="3032c-235">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="3032c-235">Romanian</span></span>
    
- <span data-ttu-id="3032c-236">Russisch</span><span class="sxs-lookup"><span data-stu-id="3032c-236">Russian</span></span>
    
- <span data-ttu-id="3032c-237">Serbisch (Kyrillisch, Serbien)</span><span class="sxs-lookup"><span data-stu-id="3032c-237">Serbian (Cyrillic, Serbia)</span></span>
    
- <span data-ttu-id="3032c-238">Serbisch (Lateinisch)</span><span class="sxs-lookup"><span data-stu-id="3032c-238">Serbian (Latin)</span></span>
    
- <span data-ttu-id="3032c-239">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="3032c-239">Slovak</span></span>
    
- <span data-ttu-id="3032c-240">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="3032c-240">Slovenian</span></span>
    
- <span data-ttu-id="3032c-241">Spanisch</span><span class="sxs-lookup"><span data-stu-id="3032c-241">Spanish</span></span>
    
- <span data-ttu-id="3032c-242">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="3032c-242">Swedish</span></span>
    
- <span data-ttu-id="3032c-243">Tamil</span><span class="sxs-lookup"><span data-stu-id="3032c-243">Tamil</span></span>
    
- <span data-ttu-id="3032c-244">Telugu</span><span class="sxs-lookup"><span data-stu-id="3032c-244">Telugu</span></span>
    
- <span data-ttu-id="3032c-245">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="3032c-245">Thai</span></span>
    
- <span data-ttu-id="3032c-246">Türkisch</span><span class="sxs-lookup"><span data-stu-id="3032c-246">Turkish</span></span>
    
- <span data-ttu-id="3032c-247">Ukrainisch</span><span class="sxs-lookup"><span data-stu-id="3032c-247">Ukrainian</span></span>
    
- <span data-ttu-id="3032c-248">Urdu</span><span class="sxs-lookup"><span data-stu-id="3032c-248">Urdu</span></span>
    
- <span data-ttu-id="3032c-249">Vietnamesisch</span><span class="sxs-lookup"><span data-stu-id="3032c-249">Vietnamese</span></span>
    
- <span data-ttu-id="3032c-250">Walisisch</span><span class="sxs-lookup"><span data-stu-id="3032c-250">Welsh</span></span>
    

