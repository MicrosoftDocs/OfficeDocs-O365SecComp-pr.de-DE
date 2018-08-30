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
search.appverid:
- MET150
ms.assetid: 97921f0e-832f-40c7-b56d-414faede5191
description: Die Exchange-Verwaltungskonsole (EAC) ist die webbasierte Verwaltungskonsole für Microsoft Exchange Online Protection (EOP).
ms.openlocfilehash: 144907110af9fcbec1c6399e0695abb705bef409
ms.sourcegitcommit: e9dca2d6a7838f98bb7eca127fdda2372cda402c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2018
ms.locfileid: "23002944"
---
# <a name="exchange-admin-center-in-exchange-online-protection"></a><span data-ttu-id="7d28a-103">Exchange-Verwaltungskonsole in Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="7d28a-103">Exchange admin center in Exchange Online Protection</span></span> 

<span data-ttu-id="7d28a-104">Die Exchange-Verwaltungskonsole (EAC) ist die webbasierte Verwaltungskonsole für Microsoft Exchange Online Protection (EOP).</span><span class="sxs-lookup"><span data-stu-id="7d28a-104">The Exchange admin center (EAC) is the web-based management console for Microsoft Exchange Online Protection (EOP).</span></span> 
  
<span data-ttu-id="7d28a-p101">Suchen Sie die Exchange 2013-Version dieses Themas? Weitere Informationen finden Sie unter [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span><span class="sxs-lookup"><span data-stu-id="7d28a-p101">Looking for the Exchange 2013 version of this topic? See [Exchange admin center in Exchange 2013](http://technet.microsoft.com/library/a9aea11a-6ba3-4f4a-a76e-79072e7cfc7d.aspx).</span></span>
  
<span data-ttu-id="7d28a-p102">Suchen Sie die Exchange Online-Version dieses Themas? Weitere Informationen finden Sie unter [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span><span class="sxs-lookup"><span data-stu-id="7d28a-p102">Looking for the Exchange Online version of this topic? See [Exchange admin center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).</span></span>
  
## <a name="accessing-the-eac"></a><span data-ttu-id="7d28a-109">Zugreifen auf die Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="7d28a-109">Accessing the EAC</span></span>

<span data-ttu-id="7d28a-p103">In den meisten Fällen greifen EOP-Kunden über das Office 365 Admin Center auf die Exchange-Verwaltungskonsole (EAC) zu. Einen Link zu EOP finden Sie im Dropdownmenü der **Admin**-Kachel, die sich neben der **Ich**-Kachel befindet. Klicken Sie auf die **Admin**-Kachel, und wählen Sie im Dropdownmenü **Exchange Online Protection**, um die Exchange-Verwaltungskonsole aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p103">In most cases, EOP customers will access the EAC through the Office 365 admin center. You can find a link to EOP in the drop-down menu in the **Admin** tile, which is next to the **Me** tile. Click the **Admin** tile and select **Exchange Online Protection** from the drop down menu to be taken to the EAC.</span></span> 
  
<span data-ttu-id="7d28a-p104">Sie können auch über den folgenden URL direkt auf das EAC-Zeichen auf der Seite zugreifen: https://admin.protection.outlook.com/ecp/\<companydomain\>. Beispiel: https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. Nachdem Sie Ihre Benutzeranmeldeinformationen eingegeben haben, gelangen Sie direkt zur Exchange-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p104">You can also access the EAC sign in page directly via the following URL: https://admin.protection.outlook.com/ecp/\<companydomain\>. For example, https://admin.protection.outlook.com/ecp/contoso.onmicrosoft.com. After specifying your user credentials you will be taken directly into the EAC.</span></span>
  
## <a name="common-user-interface-elements-in-the-eac"></a><span data-ttu-id="7d28a-116">Allgemeine Elemente der Benutzeroberfläche in der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="7d28a-116">Common user interface elements in the EAC</span></span>

<span data-ttu-id="7d28a-117">In diesem Abschnitt werden die Elemente der Benutzeroberfläche der Exchange-Verwaltungskonsole beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d28a-117">This section describes the user interface elements that are found in the EAC.</span></span>
  
![EOP-AdminCenter](media/EOP-AdminCenter.png)
  
### <a name="feature-pane"></a><span data-ttu-id="7d28a-119">Featurebereich</span><span class="sxs-lookup"><span data-stu-id="7d28a-119">Feature Pane</span></span>

<span data-ttu-id="7d28a-p105">Dies ist die erste Navigationsebene für die meisten Aufgaben, die Sie in der Exchange-Verwaltungskonsole ausführen. Der Featurebereich ist nach Funktionsbereichen organisiert.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p105">This is the first level of navigation for most of the tasks you'll perform in the EAC. The feature pane is organized by feature areas.</span></span>
  
1. <span data-ttu-id="7d28a-122">**Empfänger** Mit diesem Feature können Sie interne Benutzer und externe Kontakte anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7d28a-122">**Recipients** This is where you'll view internal users and external contacts.</span></span> 
    
2. <span data-ttu-id="7d28a-123">**Berechtigungen** Mit diesem Feature können Sie Administratorrollen verwalten.</span><span class="sxs-lookup"><span data-stu-id="7d28a-123">**Permissions** This where you'll manage administrator roles.</span></span> 
    
3. <span data-ttu-id="7d28a-124">**Verwaltung der Richtlinientreue** Hier finden Sie Überwachungsprotokolle und Berichte wie den Administrator-Rollengruppenbericht.</span><span class="sxs-lookup"><span data-stu-id="7d28a-124">**Compliance Management** This is where you'll find audit logs and reports, such as the administrator role group report.</span></span> 
    
4. <span data-ttu-id="7d28a-125">**Schutz** Mit diesem Feature können Sie Antischadsoftware- und Antispamschutz für Ihre Organisation sowie isolierte Nachrichten verwalten.</span><span class="sxs-lookup"><span data-stu-id="7d28a-125">**Protection** This is where you'll manage anti-malware and anti-spam protection for your organization, as well as manage messages in quarantine.</span></span> 
    
5. <span data-ttu-id="7d28a-126">**Nachrichtenfluss** Mit diesem Feature können Sie Regeln, akzeptierte Domänen und Connectors verwalten sowie festlegen, wo die Nachrichtenablaufverfolgung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7d28a-126">**Mail Flow** This is where you'll manage rules, accepted domains, and connectors, as well as where you'll go to perform message trace.</span></span> 
    
### <a name="tabs"></a><span data-ttu-id="7d28a-127">Registerkarten</span><span class="sxs-lookup"><span data-stu-id="7d28a-127">Tabs</span></span>

<span data-ttu-id="7d28a-p106">Die Registerkarten sind Ihre zweite Ebene der Navigation. Alle Featurebereiche enthalten verschiedene Registerkarten, die jeweils ein Feature repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p106">The tabs are your second level of navigation. Each of the feature areas contains various tabs, each representing a feature.</span></span>
  
### <a name="toolbar"></a><span data-ttu-id="7d28a-130">Symbolleiste</span><span class="sxs-lookup"><span data-stu-id="7d28a-130">Toolbar</span></span>

<span data-ttu-id="7d28a-p107">Für die meisten Registerkarten wird eine Symbolleiste angezeigt, nachdem Sie auf sie geklickt haben. Die Symbolleiste enthält Symbole, die jeweils eine bestimmte Aktion auslösen. Die folgende Tabelle beschreibt die Symbole und deren Aktionen.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p107">When you click most tabs, you'll see a toolbar. The toolbar has icons that perform a specific action. The following table describes the icons and their actions.</span></span>
  
|<span data-ttu-id="7d28a-134">**Symbol**</span><span class="sxs-lookup"><span data-stu-id="7d28a-134">**Icon**</span></span>|<span data-ttu-id="7d28a-135">**Name**</span><span class="sxs-lookup"><span data-stu-id="7d28a-135">**Name**</span></span>|<span data-ttu-id="7d28a-136">**Action**</span><span class="sxs-lookup"><span data-stu-id="7d28a-136">**Action**</span></span>|
|:-----|:-----|:-----|
|![Hinzufügen (Symbol)](media/ITPro-EAC-AddIcon.gif)           <br/> |<span data-ttu-id="7d28a-138">Hinzufügen, Neu</span><span class="sxs-lookup"><span data-stu-id="7d28a-138">Add, New</span></span>  <br/> |<span data-ttu-id="7d28a-p108">Über dieses Symbol können Sie ein neues Objekt erstellen. Bei einigen dieser Symbole gibt es einen dazugehörigen nach unten zeigenden Pfeil, auf den Sie klicken können, um weitere Objekte anzuzeigen, die Sie erstellen können.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p108">Use this icon to create a new object. Some of these icons have an associated down arrow you can click to show additional objects you can create.</span></span>  <br/> |
|![Bearbeitungssymbol](media/ITPro-EAC-EditIcon.gif)           <br/> |<span data-ttu-id="7d28a-142">Bearbeiten</span><span class="sxs-lookup"><span data-stu-id="7d28a-142">Edit</span></span>  <br/> |<span data-ttu-id="7d28a-143">Über dieses Symbol können Sie ein Objekt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="7d28a-143">Use this icon to edit an object.</span></span>  <br/> |
|![Löschen (Symbol)](media/ITPro-EAC-DeleteIcon.gif)           <br/> |<span data-ttu-id="7d28a-145">Löschen</span><span class="sxs-lookup"><span data-stu-id="7d28a-145">Delete</span></span>  <br/> |<span data-ttu-id="7d28a-p109">Über dieses Symbol können Sie ein Objekt löschen. Bei einigen Löschsymbolen gibt es einen nach unten zeigenden Pfeil, auf den Sie zum Einblenden weiterer Optionen klicken können.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p109">Use this icon to delete an object. Some delete icons have a down arrow you can click to show additional options.</span></span>  <br/> |
|![Suchen (Symbol)](media/ITPro-EAC-.gif)           <br/> |<span data-ttu-id="7d28a-149">Suche</span><span class="sxs-lookup"><span data-stu-id="7d28a-149">Search</span></span>  <br/> |<span data-ttu-id="7d28a-150">Über dieses Symbol können Sie ein Suchfeld öffnen, in das Sie den Suchbegriff für ein zu suchendes Objekt eingeben können.</span><span class="sxs-lookup"><span data-stu-id="7d28a-150">Use this icon to open a search box in which you can type the search phrase for an object you want to find.</span></span>  <br/> |
|![Aktualisieren (Symbol)](media/ITPro-EAC-RefreshIcon.gif)           <br/> |<span data-ttu-id="7d28a-152">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="7d28a-152">Refresh</span></span>  <br/> |<span data-ttu-id="7d28a-153">Über dieses Symbol können Sie die Listenansicht aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7d28a-153">Use this icon to refresh the list view.</span></span>  <br/> |
|![Weitere Optionen (Symbol)](media/ITPro-EAC-MoreOptionsIcon.gif)           <br/> |<span data-ttu-id="7d28a-155">Weitere Optionen</span><span class="sxs-lookup"><span data-stu-id="7d28a-155">More options</span></span>  <br/> |<span data-ttu-id="7d28a-p110">Über dieses Symbol können Sie mehrere Aktionen anzeigen, die Sie auf die Objekte dieser Registerkarte anwenden können. Wenn Sie z. B. unter **Empfänger \> Benutzer** auf dieses Symbol klicken, wird die Option **Erweiterte Suche** angezeigt.  </span><span class="sxs-lookup"><span data-stu-id="7d28a-p110">Use this icon to view more actions you can perform for that tab's objects. For example, in **Recipients \> Users** clicking this icon shows the option to perform an **Advanced Search**.  </span></span><br/> |
|![NACH-OBEN-TASTE (Symbol)](media/ITPro-EAC-UpArrowIcon.gif)![NACH-UNTEN-TASTE (Symbol)](media/ITPro-EAC-DownArrowIcon.gif)           <br/> |<span data-ttu-id="7d28a-160">Pfeil nach oben und Pfeil nach unten</span><span class="sxs-lookup"><span data-stu-id="7d28a-160">Up arrow and down arrow</span></span>  <br/> |<span data-ttu-id="7d28a-161">Mithilfe dieser Symbole können Sie die Priorität eines Objekts nach oben oder unten verschieben.</span><span class="sxs-lookup"><span data-stu-id="7d28a-161">Use these icons to move an object's priority up or down.</span></span>  <br/> |
|![Entfernen (Symbol)](media/ITPro-EAC-RemoveIcon.gif)           <br/> |<span data-ttu-id="7d28a-163">Entfernen</span><span class="sxs-lookup"><span data-stu-id="7d28a-163">Remove</span></span>  <br/> |<span data-ttu-id="7d28a-164">Über dieses Symbol können Sie Objekte aus einer Liste entfernen.</span><span class="sxs-lookup"><span data-stu-id="7d28a-164">Use this icon to remove objects from a list.</span></span>  <br/> |
   
### <a name="list-view"></a><span data-ttu-id="7d28a-165">Listenansicht</span><span class="sxs-lookup"><span data-stu-id="7d28a-165">List View</span></span>

<span data-ttu-id="7d28a-p111">Wenn Sie auf eine Registerkarte klicken, sehen Sie in den meisten Fällen eine Listenansicht. In der Listenansicht der Exchange-Verwaltungskonsole können ungefähr 10.000 Objekte angezeigt werden. Darüber hinaus können Sie die Ergebnisse seitenweise anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p111">When you select a tab, in most cases you'll see a list view. The viewable limit with the EAC list view is approximately 10,000 objects. In addition, paging is included so that you can page to results.</span></span>
  
### <a name="details-pane"></a><span data-ttu-id="7d28a-169">Detailbereich</span><span class="sxs-lookup"><span data-stu-id="7d28a-169">Details Pane</span></span>

<span data-ttu-id="7d28a-p112">Wenn Sie in der Listenansicht ein Objekt auswählen, werden Informationen zu diesem Objekt im Detailbereich angezeigt. In einigen Fällen enthält der Detailbereich Verwaltungsaufgaben.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p112">When you select an object from the list view, information about that object is displayed in the details pane. In some cases the details pane includes management tasks.</span></span>
  
### <a name="me-tile-and-help"></a><span data-ttu-id="7d28a-172">Ich-Kachel und Hilfe</span><span class="sxs-lookup"><span data-stu-id="7d28a-172">Me tile and Help</span></span>

<span data-ttu-id="7d28a-p113">Über die **Ich**-Kachel können Sie sich bei der Exchange-Verwaltungskonsole abmelden und als ein anderer Benutzer anmelden. Über das Dropdownmenü der **Hilfe**![Hilfe (Symbol)](media/ITPro-EAC-HelpIcon.gif) können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="7d28a-p113">The **Me** tile allows you to sign out the EAC and sign in as a different user. From the **Help**![Help Icon](media/ITPro-EAC-HelpIcon.gif) drop-down menu, you can perform the following actions:</span></span> 
  
1. <span data-ttu-id="7d28a-175">**Hilfe** Klicken Sie auf ![Hilfe (Symbol)](media/ITPro-EAC-HelpIcon.gif), damit der Inhalt der Onlinehilfe angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7d28a-175">**Help** Click ![Help Icon](media/ITPro-EAC-HelpIcon.gif) to view the online help content.</span></span> 
    
2. <span data-ttu-id="7d28a-p114">**Hilfe-Sprechblase deaktivieren** In der Hilfe-Sprechblase wird Kontexthilfe für Felder angezeigt, wenn Sie ein Objekt erstellen oder bearbeiten. Sie können die Hilfe-Sprechblase deaktivieren bzw. aktivieren, wenn sie deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7d28a-p114">**Disable Help bubble** The Help bubble displays contextual help for fields when you create or edit an object. You can turn off the Help bubble or turn it on if it has been disabled.</span></span> 
    
3. <span data-ttu-id="7d28a-178">**Copyright** Klicken Sie auf diesen Link, um den Copyright-Hinweis für Exchange Online Protection zu lesen.</span><span class="sxs-lookup"><span data-stu-id="7d28a-178">**Copyright** Click this link to read the copyright notice for Exchange Online Protection.</span></span> 
    
4. <span data-ttu-id="7d28a-179">**Datenschutz** Klicken Sie hier, um die Datenschutzrichtlinien für Exchange Online Protection zu lesen.</span><span class="sxs-lookup"><span data-stu-id="7d28a-179">**Privacy** Click to read the privacy policy for Exchange Online Protection.</span></span> 
    
## <a name="supported-browsers"></a><span data-ttu-id="7d28a-180">Unterstützte Browser</span><span class="sxs-lookup"><span data-stu-id="7d28a-180">Supported Browsers</span></span>

<span data-ttu-id="7d28a-p115">Für eine optimale Nutzung des EAC sollten Sie immer die neuesten Browser, Office-Clients und Apps verwenden. Zudem wird empfohlen, dass Sie Softwareupdates installieren, sobald sie verfügbar werden. Weitere Informationen zu den unterstützten Browsern und zu den Systemanforderungen für den Dienst finden Sie unter [Office 365-Systemanforderungen](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span><span class="sxs-lookup"><span data-stu-id="7d28a-p115">For the best experience using the EAC, we recommend that you always use the latest browsers, Office clients, and apps. We also recommend that you install software updates when they become available. For more information about the supported browsers and system requirements for the service, see [Office 365 System Requirements](https://go.microsoft.com/fwlink/p/?LinkID=402699).</span></span> 
  
## <a name="supported-languages-in-eop"></a><span data-ttu-id="7d28a-184">Unterstützte Sprachen in EOP</span><span class="sxs-lookup"><span data-stu-id="7d28a-184">Supported languages in EOP</span></span>

<span data-ttu-id="7d28a-185">Die folgenden Sprachen werden für Exchange Online Protection unterstützt und zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="7d28a-185">The following languages are supported and available for Exchange Online Protection.</span></span>
  
- <span data-ttu-id="7d28a-186">Amharisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-186">Amharic</span></span>
    
- <span data-ttu-id="7d28a-187">Arabisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-187">Arabic</span></span>
    
- <span data-ttu-id="7d28a-188">Baskisch (Baskisch)</span><span class="sxs-lookup"><span data-stu-id="7d28a-188">Basque (Basque)</span></span>
    
- <span data-ttu-id="7d28a-189">Bengali (Indien)</span><span class="sxs-lookup"><span data-stu-id="7d28a-189">Bengali (India)</span></span>
    
- <span data-ttu-id="7d28a-190">Bulgarisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-190">Bulgarian</span></span>
    
- <span data-ttu-id="7d28a-191">Katalanisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-191">Catalan</span></span>
    
- <span data-ttu-id="7d28a-192">Chinesisch (vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="7d28a-192">Chinese (Simplified)</span></span>
    
- <span data-ttu-id="7d28a-193">Chinesisch (traditionell)</span><span class="sxs-lookup"><span data-stu-id="7d28a-193">Chinese (Traditional)</span></span>
    
- <span data-ttu-id="7d28a-194">Kroatisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-194">Croatian</span></span>
    
- <span data-ttu-id="7d28a-195">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-195">Czech</span></span>
    
- <span data-ttu-id="7d28a-196">Dänisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-196">Danish</span></span>
    
- <span data-ttu-id="7d28a-197">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-197">Dutch</span></span>
    
- <span data-ttu-id="7d28a-198">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-198">Dutch</span></span>
    
- <span data-ttu-id="7d28a-199">Englisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-199">English</span></span>
    
- <span data-ttu-id="7d28a-200">Estnisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-200">Estonian</span></span>
    
- <span data-ttu-id="7d28a-201">Filipino (Philippinen)</span><span class="sxs-lookup"><span data-stu-id="7d28a-201">Filipino (Philippines)</span></span>
    
- <span data-ttu-id="7d28a-202">Finnisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-202">Finnish</span></span>
    
- <span data-ttu-id="7d28a-203">Französisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-203">French</span></span>
    
- <span data-ttu-id="7d28a-204">Galicisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-204">Galician</span></span>
    
- <span data-ttu-id="7d28a-205">Deutsch</span><span class="sxs-lookup"><span data-stu-id="7d28a-205">German</span></span>
    
- <span data-ttu-id="7d28a-206">Griechisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-206">Greek</span></span>
    
- <span data-ttu-id="7d28a-207">Gujarati</span><span class="sxs-lookup"><span data-stu-id="7d28a-207">Gujarati</span></span>
    
- <span data-ttu-id="7d28a-208">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-208">Hebrew</span></span>
    
- <span data-ttu-id="7d28a-209">Hindi</span><span class="sxs-lookup"><span data-stu-id="7d28a-209">Hindi</span></span>
    
- <span data-ttu-id="7d28a-210">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-210">Hungarian</span></span>
    
- <span data-ttu-id="7d28a-211">Isländisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-211">Icelandic</span></span>
    
- <span data-ttu-id="7d28a-212">Indonesisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-212">Indonesian</span></span>
    
- <span data-ttu-id="7d28a-213">Italienisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-213">Italian</span></span>
    
- <span data-ttu-id="7d28a-214">Japanisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-214">Japanese</span></span>
    
- <span data-ttu-id="7d28a-215">Kannada</span><span class="sxs-lookup"><span data-stu-id="7d28a-215">Kannada</span></span>
    
- <span data-ttu-id="7d28a-216">Kasachisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-216">Kazakh</span></span>
    
- <span data-ttu-id="7d28a-217">Kisuaheli</span><span class="sxs-lookup"><span data-stu-id="7d28a-217">Kiswahili</span></span>
    
- <span data-ttu-id="7d28a-218">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-218">Korean</span></span>
    
- <span data-ttu-id="7d28a-219">Lettisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-219">Latvian</span></span>
    
- <span data-ttu-id="7d28a-220">Litauisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-220">Lithuanian</span></span>
    
- <span data-ttu-id="7d28a-221">Malaiisch (Brunei Darussalam)</span><span class="sxs-lookup"><span data-stu-id="7d28a-221">Malay (Brunei Darussalam)</span></span>
    
- <span data-ttu-id="7d28a-222">Malaiisch (Malaysia)</span><span class="sxs-lookup"><span data-stu-id="7d28a-222">Malay (Malaysia)</span></span>
    
- <span data-ttu-id="7d28a-223">Malayalam</span><span class="sxs-lookup"><span data-stu-id="7d28a-223">Malayalam</span></span>
    
- <span data-ttu-id="7d28a-224">Marathi</span><span class="sxs-lookup"><span data-stu-id="7d28a-224">Marathi</span></span>
    
- <span data-ttu-id="7d28a-225">Norwegisch (Bokmål)</span><span class="sxs-lookup"><span data-stu-id="7d28a-225">Norwegian (Bokmål)</span></span>
    
- <span data-ttu-id="7d28a-226">Norwegisch (Nynorsk)</span><span class="sxs-lookup"><span data-stu-id="7d28a-226">Norwegian (Nynorsk)</span></span>
    
- <span data-ttu-id="7d28a-227">Odia</span><span class="sxs-lookup"><span data-stu-id="7d28a-227">Oriya</span></span>
    
- <span data-ttu-id="7d28a-228">Persisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-228">Persian</span></span>
    
- <span data-ttu-id="7d28a-229">Polnisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-229">Polish</span></span>
    
- <span data-ttu-id="7d28a-230">Portugiesisch (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="7d28a-230">Portuguese (Brazil)</span></span>
    
- <span data-ttu-id="7d28a-231">Portugiesisch (Portugal)</span><span class="sxs-lookup"><span data-stu-id="7d28a-231">Portuguese (Portugal)</span></span>
    
- <span data-ttu-id="7d28a-232">Rumänisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-232">Romanian</span></span>
    
- <span data-ttu-id="7d28a-233">Russisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-233">Russian</span></span>
    
- <span data-ttu-id="7d28a-234">Serbisch (Kyrillisch, Serbien)</span><span class="sxs-lookup"><span data-stu-id="7d28a-234">Serbian (Cyrillic, Serbia)</span></span>
    
- <span data-ttu-id="7d28a-235">Serbisch (Lateinisch)</span><span class="sxs-lookup"><span data-stu-id="7d28a-235">Serbian (Latin)</span></span>
    
- <span data-ttu-id="7d28a-236">Slowakisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-236">Slovak</span></span>
    
- <span data-ttu-id="7d28a-237">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-237">Slovenian</span></span>
    
- <span data-ttu-id="7d28a-238">Spanisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-238">Spanish</span></span>
    
- <span data-ttu-id="7d28a-239">Schwedisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-239">Swedish</span></span>
    
- <span data-ttu-id="7d28a-240">Tamil</span><span class="sxs-lookup"><span data-stu-id="7d28a-240">Tamil</span></span>
    
- <span data-ttu-id="7d28a-241">Telugu</span><span class="sxs-lookup"><span data-stu-id="7d28a-241">Telugu</span></span>
    
- <span data-ttu-id="7d28a-242">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-242">Thai</span></span>
    
- <span data-ttu-id="7d28a-243">Türkisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-243">Turkish</span></span>
    
- <span data-ttu-id="7d28a-244">Ukrainisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-244">Ukrainian</span></span>
    
- <span data-ttu-id="7d28a-245">Urdu</span><span class="sxs-lookup"><span data-stu-id="7d28a-245">Urdu</span></span>
    
- <span data-ttu-id="7d28a-246">Vietnamesisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-246">Vietnamese</span></span>
    
- <span data-ttu-id="7d28a-247">Walisisch</span><span class="sxs-lookup"><span data-stu-id="7d28a-247">Welsh</span></span>
    

