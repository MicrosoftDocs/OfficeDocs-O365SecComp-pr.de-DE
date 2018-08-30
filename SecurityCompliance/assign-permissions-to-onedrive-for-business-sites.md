---
title: Zuweisen von eDiscovery-Berechtigungen für OneDrive for Business-Websites
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/27/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: 422858ff-917b-46d4-9e5b-3397f60eee4d
description: Das eDiscovery Center in SharePoint Online können Sie alle OneDrive for Business-Websites in Ihrer Organisation für bestimmte Schlüsselwörter, vertrauliche Informationen und andere Suchkriterien suchen. Jeder Benutzer in Ihrer Organisation ist der Besitzer der ihre OneDrive for Business-Website, die sich in der Websitesammlung, die mit dem Namen befindet https://domain-my.sharepoint.com. Standardmäßig können ein globaler Office 365-Administrator oder Compliance Manager das eDiscovery Center in SharePoint Online um eine beliebige OneDrive for Business-Websites zu suchen. Zum Suchen einer OneDrive for Business-Website, Administratoren oder Compliance-Manager muss ein Websitesammlungsadministrator für diese OneDrive for Business-Site.
ms.openlocfilehash: 48f84dfe21f0f99913ba2c27123d6c0e1f8bc03f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529473"
---
# <a name="assign-ediscovery-permissions-to-onedrive-for-business-sites"></a><span data-ttu-id="cce4d-106">Zuweisen von eDiscovery-Berechtigungen für OneDrive for Business-Websites</span><span class="sxs-lookup"><span data-stu-id="cce4d-106">Assign eDiscovery permissions to OneDrive for Business sites</span></span>

<span data-ttu-id="cce4d-p102">Das eDiscovery Center in SharePoint Online können Sie alle OneDrive for Business-Websites in Ihrer Organisation für bestimmte Schlüsselwörter, vertrauliche Informationen und andere Suchkriterien suchen. Jeder Benutzer in Ihrer Organisation ist der Besitzer der ihre OneDrive for Business-Website, die sich in der Websitesammlung, die mit dem Namen befindet https://domain-my.sharepoint.com. Standardmäßig können ein globaler Office 365-Administrator oder Compliance Manager das eDiscovery Center in SharePoint Online um eine beliebige OneDrive for Business-Websites zu suchen. Zum Suchen einer OneDrive for Business-Website, Administratoren oder Compliance-Manager muss ein Websitesammlungsadministrator für diese OneDrive for Business-Site.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p102">You can use the eDiscovery Center in SharePoint Online to search all OneDrive for Business sites in your organization for certain keywords, sensitive information, and other search criteria. Each user in your organization is the owner of their OneDrive for Business site, which is located in the site collection named https://domain-my.sharepoint.com. By default, an Office 365 global administrator or compliance manager can't use the eDiscovery Center in SharePoint Online to search any OneDrive for Business sites. To search a OneDrive for Business site, administrators or compliance managers must be a site collection administrator for that OneDrive for Business site.</span></span> 
  
<span data-ttu-id="cce4d-111">Dieser Artikel führt Sie durch die Schritte zum Manager ein Websitesammlungsadministrator für jede OneDrive for Business-Site ein Administrator oder Compliance in Ihrer Organisation zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cce4d-111">This article guides you through the steps to make an administrator or compliance manager a site collection administrator for every OneDrive for Business site in your organization.</span></span> 
  
<span data-ttu-id="cce4d-112">Finden Sie [Weitere Informationen](#more-information) im Abschnitt Tipps zur Verwendung des Skripts in diesem Artikel, einschließlich Überarbeitung des Skripts in Schritt 3, um einen Benutzer als Websitesammlungsadministrator aus OneDrive for Business-Websites zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="cce4d-112">See the [More information](#more-information) section for tips about using the script in this article, including revising the script in Step 3 to remove a user as a site collection administrator from OneDrive for Business sites.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="cce4d-113">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="cce4d-113">Before you begin</span></span>

- <span data-ttu-id="cce4d-p103">Installieren Sie die SharePoint Online-Verwaltungsshell. Weitere Informationen finden Sie unter [Einrichten der Windows PowerShell-Umgebung für die SharePoint Online-Verwaltungsshell ](https://go.microsoft.com/fwlink/p/?LinkID=286318).</span><span class="sxs-lookup"><span data-stu-id="cce4d-p103">Install the SharePoint Online Management Shell. For information, see [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318).</span></span>
    
- <span data-ttu-id="cce4d-116">Führen Sie das Skript in Schritt 3 jedes Mal alle OneDrive for Business-Websites in Ihrer Organisation einen Benutzer als Administrator einer Websitesammlung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="cce4d-116">Run the script in Step 3 each time you want to assign a user as a site collection administrator to any OneDrive for Business sites in your organization.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="cce4d-p104">Ein Administrator oder Compliance Manager, ein Websitesammlungsadministrator für OneDrive for Business-Websites können Benutzer OneDrive for Business-Dokumentbibliotheken zu öffnen und die gleichen als Besitzer Aufgaben ist. Es ist wichtig, steuern und überwachen, die eDiscovery-Berechtigungen zu OneDrive for Business-Websites in Ihrer Organisation zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p104">An administrator or compliance manager who is a site collection administrator for OneDrive for Business sites can open users' OneDrive for Business document libraries and perform the same tasks as the owner. It's important to control and monitor who has been assigned eDiscovery permissions to OneDrive for Business sites in your organization.</span></span> 
  
- <span data-ttu-id="cce4d-p105">Das in diesem Artikel beschriebene Beispielskript wird unter keinem standard Support-Programm von Microsoft oder der Dienst nicht unterstützt. Das Beispielskript wird wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt alle konkludente Garantien einschließlich, aber nicht beschränkt auf konkludente Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck. Das gesamte Risiko aus der Verwendung oder der Leistung der Beispielskript und der Dokumentation liegt bei Ihnen. In keinem Fall muss Microsoft, seine Autoren oder jeder anderen Beteiligten in die Erstellung, die Produktion oder die Bereitstellung des Skripts für Schäden jeglicher Art (einschließlich, aber nicht beschränkt auf Schäden für den Verlust von Gewinn Business, Business Unterbrechung, Verlust von Unternehmensinformationen, Folge- oder) aus der Verwendung des oder der Fehler beim das Beispielskript oder Dokumentation verwenden haftbar gemacht werden, auch wenn Microsoft die Möglichkeit solcher Schäden hingewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p105">The sample script provided in this article isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the script be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample script or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-collect-a-list-of-all-onedrive-for-business-sites"></a><span data-ttu-id="cce4d-124">Schritt 1: Sammeln Sie eine Liste aller onedrive for Business-Websites</span><span class="sxs-lookup"><span data-stu-id="cce4d-124">Step 1: Collect a list of all OneDrive for Business sites</span></span>

<span data-ttu-id="cce4d-p106">Der erste Schritt ist zum Erstellen einer Liste aller onedrive for Business-Websites in Ihrer Organisation. Anweisungen finden Sie unter [Erstellen einer Liste der OneDrive Positionen in Ihrer Organisation](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). Dieses Skript in diesem Artikel erstellt eine Textdatei, die eine Liste aller OneDrive-Websites enthält. Das Skript, das Sie in Schritt 3 ausführen, weist einen angegebenen Benutzer als Administrator einer Websitesammlung zu jedem OneDrive for Business-Website aufgeführt, die in der Textdatei, die in diesem Schritt erstellt wird. Der folgende Text enthält ein Beispiel, wie die Liste der Websites in dieser Datei formatiert werden soll. Sie können bei Bedarf Websites aus dieser Datei entfernen.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p106">The first step is to create a list of all OneDrive for Business sites in your organization. For instructions, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/8e200cb2-c768-49cb-88ec-53493e8ad80a). This script in this article creates a text file that contains a list of all OneDrive sites. The script that you run in Step 3 assigns a specified user as a site collection administrator to each OneDrive for Business site listed in the text file that's created in this step. The following text provides an example of how the list of sites in this file should be formatted. You can remove sites from this file if necessary.</span></span>

```
/personal/annb_contoso_onmicrosoft_com/
/personal/carolt_contoso_onmicrosoft_com/
/personal/esterv_contoso_onmicrosoft_com/
/personal/hollyh_contoso_onmicrosoft_com/
/personal/jeffl_contoso_onmicrosoft_com/
/personal/joeh_contoso_onmicrosoft_com/
/personal/kaia_contoso_onmicrosoft_com/
```

## <a name="step-2-connect-sharepoint-online-management-shell-to-your-organization"></a><span data-ttu-id="cce4d-131">Schritt 2: SharePoint Online-Verwaltungsshell Herstellen einer Verbindung mit Ihrer Organisation</span><span class="sxs-lookup"><span data-stu-id="cce4d-131">Step 2: Connect SharePoint Online Management Shell to your organization</span></span>

1. <span data-ttu-id="cce4d-132">Öffnen Sie auf Ihrem lokalen Computer die SharePoint Online-Verwaltungsshell, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="cce4d-132">On your local computer, open the SharePoint Online Management Shell, and run the following command:</span></span>

    ```
    $credentials = Get-Credential
    ```

2. <span data-ttu-id="cce4d-133">Geben Sie im Dialogfeld **Bei Windows PowerShell anmelden** den Benutzernamen und das Kennwort für Ihr globales Office 365-Administratorkonto an, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="cce4d-133">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global administrator account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="cce4d-134">Führen Sie den folgenden Befehl aus, um eine Verbindung zwischen der Shell und Ihrem SharePoint Online-Unternehmen herzustellen:</span><span class="sxs-lookup"><span data-stu-id="cce4d-134">Run the following command to connect the Shell to your SharePoint Online organization:</span></span>
    
    ```
    Connect-SPOService -Url https://<your organization name>-admin.sharepoint.com -credential $credentials
    ```
   
4. <span data-ttu-id="cce4d-135">Um zu prüfen, ob Sie mit Ihrer SharePoint Online-Organisation verbunden sind, führen Sie den folgenden Befehl aus, um eine Liste aller Websites in Ihrer Organisation abzurufen:</span><span class="sxs-lookup"><span data-stu-id="cce4d-135">To verify that you are connected to your SharePoint Online organization, run the following command to get a list of all the sites in your organization:</span></span>
    
    ```
    Get-SPOSite
    ```

## <a name="step-3-assign-a-user-as-a-site-collection-administrator-to-onedrive-for-business-sites"></a><span data-ttu-id="cce4d-136">Schritt 3: Zuweisen eines Benutzers als Websitesammlungsadministrator für OneDrive for Business-Websites</span><span class="sxs-lookup"><span data-stu-id="cce4d-136">Step 3: Assign a user as a site collection administrator to OneDrive for Business sites</span></span>

<span data-ttu-id="cce4d-p107">Im nächste Schritt wird das Ausführen eines Skripts, das einen angegebenen Benutzer als Websitesammlungsadministrator in jeder OneDrive for Business-Standort in Ihrer Organisation zuweist. Dieses Skript nutzt die Liste der OneDrive for Business-Websites, die Sie in Schritt 1 erstellt haben. Wie bereits erwähnt müssen Sie dieses Skript jedes Mal ausführen, die Sie einen Benutzer als Administrator einer Websitesammlung zu OneDrive for Business-Websites zuweisen möchten.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p107">The next step is to run a script that assigns a specified user as a site collection administrator in every OneDrive for Business site in your organization. This script uses the list of OneDrive for Business sites that you created in Step 1. As previously stated, you have to run this script each time that you want to assign a user as a site collection administrator to OneDrive for Business sites.</span></span>
  
1. <span data-ttu-id="cce4d-p108">Speichern Sie den folgenden Text in einer Textdatei. Sie können als Dateinamen beispielsweise "OD4BAssignSCA.txt" wählen.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p108">Save the following text to a text file. For example, you could save it to a file named OD4BAssignSCA.txt.</span></span>

    ```
    # Start logging, so if this script fails, you can look at the last successful change,
    # remove any OneDrive for Business paths that worked it from the input file, and then rerun the script.

    Start-Transcript

    # URL for your organization's SPO admin service

    $AdminURI = "https://<your organization name>-admin.sharepoint.com"

    # User account for an Office 365 global admin in your organization

    $AdminAccount = "<global admin account>"

    # Compliance manager to be made site collection admin on each MySite

    $eDiscoveryUser = "<eDiscovery user account>"

    # URL for your tenant's MySite domain

    $MySitePrefix = "https://<your organization name>-my.sharepoint.com"

    # Where should we read the list of MySites?
    # This file should contain partial MySite paths formatted as follows, one per line; for example
    # /personal/junminh_contoso_onmicrosoft_com/

    $MySiteListFile = 'C:\Users\<youralias>\Desktop\ListOfMysites.txt'

    # Begin by connecting to the service
    Connect-SPOService -Url $AdminURI -Credential $AdminAccount

    # Make a reader for our list of MySites

    $reader = [System.IO.File]::OpenText($MySiteListFile)

    try {
      for(;;) {

    # Read a line
          $line = $reader.ReadLine()
    # Stop if it doesn't exist
          if ($line -eq $null) { break }

    # Turn the line into a complete SharePoint site path by merging $MySitePrefix
    # Formatted like this: "https://contoso-my.sharepoint.com"
    # ...with each partial MySite path in the file, formatted like this:
    # "/personal/junminh_contoso_onmicrosoft_com/"

          $fullsitepath = "$MySitePrefix$line"

    Write-Host "Operating on $fullsitepath "

    # We need to remove the last "/" to work around an issue.
    # "/personal/junminh_contoso_onmicrosoft_com/"
    # becomes "/personal/junminh_contoso_onmicrosoft_com"

    $fullsitepath = $fullsitepath.trimend("/")

    # Make the specified eDiscovery user a site collection admin on the OneDrive for Business site
    Write-Host "Making $eDiscoveryUser a Site Collection Admin"
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
      }
    }
    finally {
      $reader.Close()
    }
    Write-Host "Done!"
    Stop-Transcript
    Write-Host "Log written."
    ```

2. <span data-ttu-id="cce4d-p109">Bearbeiten Sie die folgenden Variablen am Anfang der Skriptdatei, und verwenden Sie die Informationen, die für die Organisation spezifisch sind. In den folgenden Beispielen wird davon ausgegangen, dass der Domänennamen Ihrer Organisation contoso.onmicrosoft.com ist. Achten Sie darauf, um die Werte für die Variablen mit doppelte Anführungszeichen umgeben ("").</span><span class="sxs-lookup"><span data-stu-id="cce4d-p109">Edit the following variables in the beginning of the script file, and use information that's specific to your organization. The following examples assume that the domain name of your organization is contoso.onmicrosoft.com. Be sure to surround the values for the variables with double-quotation marks (" ").</span></span>
    
    - <span data-ttu-id="cce4d-145">**$AdminURI** - Dies gibt den URI für die SharePoint Online-Verwaltungsdienst, beispielsweise `"https://contoso-admin.sharepoint.com"`.</span><span class="sxs-lookup"><span data-stu-id="cce4d-145">**$AdminURI** - This specifies the URI for your SharePoint Online admin service, for example,  `"https://contoso-admin.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="cce4d-146">**$AdminAccount** - Hiermit wird ein globales Administratorkonto in Office 365-Organisation, beispielsweise `"admin@contoso.onmicrosoft.com"`.</span><span class="sxs-lookup"><span data-stu-id="cce4d-146">**$AdminAccount** - This specifies a global administrator account in your Office 365 organization, for example,  `"admin@contoso.onmicrosoft.com"`.</span></span>
    
    - <span data-ttu-id="cce4d-147">**$eDiscoveryUser** - Hiermit wird das Benutzerkonto ein Administrator oder Compliance-Manager, beispielsweise als Websitesammlungsadministrator für jede OneDrive for Business-Website in Ihrer Organisation zugewiesen werden `"annb@contoso.onmicrosoft.com"`.</span><span class="sxs-lookup"><span data-stu-id="cce4d-147">**$eDiscoveryUser** - This specifies the user account of an administrator or compliance manager who will be assigned as a site collection administrator for every OneDrive for Business site in your organization, for example,  `"annb@contoso.onmicrosoft.com"`.</span></span>
    
      > [!NOTE]
      > <span data-ttu-id="cce4d-148">Ändern Sie das Benutzerkonto, das durch die Variable **$eDiscoveryUser** angegeben und erneut führen Sie des Skripts einen anderen Benutzer als Administrator einer Websitesammlung, um der OneDrive for Business-Websites zuzuweisen, die durch die Variable **$MySiteListFile** angegeben sind aus.</span><span class="sxs-lookup"><span data-stu-id="cce4d-148">Change the user account specified by the **$eDiscoveryUser** variable and re-run the script to assign a different user as a site collection administrator to the OneDrive for Business sites that are specified by the **$MySiteListFile** variable.</span></span> 
  
    - <span data-ttu-id="cce4d-p110">**$MySitePrefix** Dies gibt die URL für die MySite Domäne Ihrer Organisation an. Dies ist die Domäne, die alle die OneDrive for Business-Websites in Ihrer Organisation, beispielsweise enthält `"https://contoso-my.sharepoint.com"`.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p110">**$MySitePrefix**This specifies the URL for your organization's MySite domain. This is the domain that contains all the OneDrive for Business sites in your organization, for example,  `"https://contoso-my.sharepoint.com"`.</span></span>
    
    - <span data-ttu-id="cce4d-p111">**$MySiteListFile** Dies gibt den vollständigen Pfad der Textdatei, die Sie in Schritt 1 erstellt haben. Diese Datei enthält eine Liste von OneDrive für Websites mit Geschäftsdaten in Ihrer Organisation, beispielsweise `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Achten Sie darauf, um den Wert für diese Variable mit einfache Anführungszeichen umgeben (""). Beachten Sie, dass Sie den Speicherort angeben müssen, dass Sie in Schritt 1 zu Textdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p111">**$MySiteListFile**This specifies the full path of the text file that you created in Step 1. This file contains a list of OneDrive for Business sites in your organization, for example,  `'C:\Users\<youralias>\Desktop\ListOfMysites.txt'`. Be sure to surround the value for this variable with single-quotation marks (' '). Note that you should specify the location that you saved the text file to in Step 1.</span></span>
    
3. <span data-ttu-id="cce4d-p112">Speichern Sie die Textdatei als PowerShell-Datei, indem Sie die Dateinamenerweiterung in ".ps1" ändern. Speichern Sie beispielsweise die Datei "OD4BAssignSCA.txt" als "OD4BAssignSCA.ps1".</span><span class="sxs-lookup"><span data-stu-id="cce4d-p112">Save the text file as a PowerShell script file by changing the file name suffix to .ps1. For example, save the file OD4BAssignSCA.txt as OD4BAssignSCA.ps1.</span></span>
    
4. <span data-ttu-id="cce4d-157">Wechseln Sie in der SharePoint Online-Verwaltungsshell zum Ordner mit dem im vorherigen PowerShell-Schritt erstellten Skript, und führen Sie es aus. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cce4d-157">In SharePoint Online Management Shell, go to the folder that contains the PowerShell script that you created in the previous step, and then run the script, for example:</span></span>
    
    ```
    .\OD4BAssignSCA.ps1
    ```

    <span data-ttu-id="cce4d-p113">Sie werden aufgefordert, das Kennwort für das Administratorkonto einzugeben, die Sie in das Skript angegeben. Wenn das Skript die Nachricht erfolgreich ausgeführt wird `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` wird für jede OneDrive for Business-Website, die in der Eingabedatei durch **$MySiteListFile**angegebenen aufgeführt wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p113">You will be prompted to enter the password for the administrator account that you specified in the script. If the script runs successfully, the message `"Making  _\<user specified by $eDiscoveryUser\>_ a Site Collection Admin"` is displayed for each OneDrive for Business site that's listed in the input file specified by **$MySiteListFile**.</span></span>

## <a name="more-information"></a><span data-ttu-id="cce4d-160">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cce4d-160">More information</span></span>

- <span data-ttu-id="cce4d-p114">Das Skript, das Sie in Schritt 3 ausgeführt haben verwendet das **Set-SPOUser** -Cmdlet, um den angegebenen Benutzer als Administrator einer Websitesammlung zu jeder OneDrive for Business zuweisen, die in der Datei angegeben durch die Variable **$MySiteListFile** aufgeführt wird. Wenn Sie eine große Organisation mit Hunderttausenden von Benutzern verfügen, berücksichtigen Sie Folgendes ein, um das Zuweisen von eDiscovery-Berechtigungen verwalten zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p114">The script that you ran in Step 3 uses the **Set-SPOUser** cmdlet to assign the specified user as a site collection administrator to every OneDrive for Business that's listed in the file specified by the **$MySiteListFile** variable. If you have a very large organization with thousands of users, consider doing the following to make it easier to manage assigning eDiscovery permissions.</span></span> 
    
  - <span data-ttu-id="cce4d-163">Bearbeiten Sie die Datei, die Sie in Schritt 1 erstellt haben, die die Liste der OneDrive for Business-Websites enthält, sodass sie nur die Sites enthält, für die Benutzer sind, die aktive juristische Anfragen beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="cce4d-163">Edit the file that you created in Step 1 that contains the list of OneDrive for Business sites so that it includes only the sites for users are that are involved in active legal cases.</span></span>
    
  - <span data-ttu-id="cce4d-p115">Zuweisen von Berechtigungen zu nicht mehr als 2.500 OneDrive for Business-Websites pro Tag. Nehmen wir beispielsweise an, mit denen Sie 10.000 OneDrive for Business-Websites in Ihrer Organisation. Sie können die Liste in Schritt 1 zum Erfassen aller Websites erstellen. Diese Datei können Sie dann die vier Dateien erstellt, die jeweils 2.500 Benutzer enthalten. Klicken Sie auf den ersten Tag führen Sie das Skript in Schritt 3, um die zuerst 2.500 OneDrive for Business-Websites Berechtigungen zuzuweisen. Am zweiten Tag klicken Sie führen Sie das Skript für die nächsten 2.500 OneDrive for Business-Websites, und so weiter.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p115">Assign permissions to no more than 2,500 OneDrive for Business sites per day. For example, let's say you have 10,000 OneDrive for Business sites in your organization. You could create the list in Step 1 to collect all the sites. Then you could use that file to create four files that each contain 2,500 users. On the first day, you would run the script in Step 3 to assign permissions to the first 2,500 OneDrive for Business sites. On the second day, you would run the script for the next 2,500 OneDrive for Business sites, and so on.</span></span>
    
- <span data-ttu-id="cce4d-p116">Notieren Sie sich die OneDrive for Business-Websites, die zugewiesen wurden, eDiscovery-Berechtigungen und der Benutzer, der als Administrator der Websitesammlung zugewiesen ist. Nach dem Zuweisen von Berechtigungen können Sie beispielsweise die Textdatei mit der Liste der OneDrive for Business-Websites zu speichern und fügen Sie eine Zeile hinzu, die den Benutzer identifiziert, die als Administrator der Websitesammlung zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p116">Keep a record of the OneDrive for Business sites that were assigned eDiscovery permissions and the user who is assigned as the site collection administrator. For example, after you assign permissions, you can save the text file that contains the list of OneDrive for Business sites and add a line to it that identifies the user who is assigned as the site collection administrator.</span></span>
    
- <span data-ttu-id="cce4d-p117">Benutzer können die Liste der Site Collection Administratoren für ihre OneDrive for Business-Website anzeigen. Da Benutzer Websitesammlungsadministrator für ihre eigenen OneDrive for Business-Website sind, können sie Websitesammlungsadministratoren entfernen. Berücksichtigen Sie Folgendes ein, um zu mindern das Risiko von Benutzern, entfernen den Benutzer, der eDiscovery-Berechtigungen für Websites mit Geschäftsdaten zu OneDrive zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cce4d-p117">Users can view the list of site collection administators for their OneDrive for Business site. Because users are site collection administrator for their own OneDrive for Business site, they can remove site collection administrators. Consider doing the following to mitigate the chance of users removing the user who is assigned eDiscovery permissions to OneDrive for Business sites.</span></span>
    
  - <span data-ttu-id="cce4d-175">Teilen Sie den Benutzern, dass für eDiscovery und Compliance, Compliance-beauftragte als Administrator einer Websitesammlung zu OneDrive für Websites mit Geschäftsdaten in Ihrer Organisation zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="cce4d-175">Communicate to users that for eDiscovery and compliance purposes, a compliance officer has been assigned as a site collection administrator to OneDrive for Business sites in your organization.</span></span>
    
  - <span data-ttu-id="cce4d-176">Führen Sie das Skript erneut in Schritt 3, falls erforderlich, um einen Benutzer als Administrator der Websitesammlung für OneDrive for Business-Websites neu zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="cce4d-176">Re-run the script in Step 3, if necessary, to re-assign a user as the site collection administrator for OneDrive for Business sites.</span></span>
    
- <span data-ttu-id="cce4d-p118">Sie können auch das Skript, das Sie in Schritt 3 ausgeführt haben, um einen Benutzer als Administrator der Websitesammlung aus OneDrive for Business-Websites zu entfernen. Wenn einen Benutzer als Administrator einer Websitesammlung entfernen möchten, müssen Sie aus den folgenden Befehl (gegen Ende des Skripts) zu ändern:</span><span class="sxs-lookup"><span data-stu-id="cce4d-p118">You can also use the script that you ran in Step 3 to remove a user as the site collection administrator from OneDrive for Business sites. To remove a user as a site collection administrator, you have to change the following command (near the end of the script) from:</span></span> 

    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $true
    ```

    <span data-ttu-id="cce4d-179">in:</span><span class="sxs-lookup"><span data-stu-id="cce4d-179">to:</span></span>
    
    ```
    Set-SPOUser -Site $fullsitepath -LoginName $eDiscoveryUser -IsSiteCollectionAdmin $false
    ```

    <span data-ttu-id="cce4d-180">Sie können auch die folgende Zeile im Skript wie folgt ändern. Von:</span><span class="sxs-lookup"><span data-stu-id="cce4d-180">You can also change the following line in the script from:</span></span>

    ```
    "Making $eDiscoveryUser a Site Collection Admin"
    ```

    <span data-ttu-id="cce4d-181">in:</span><span class="sxs-lookup"><span data-stu-id="cce4d-181">to:</span></span>
    
    ```
    "Removing $eDiscoveryUser as a Site Collection Admin"
    ```

    <span data-ttu-id="cce4d-182">Nachdem Sie diese Änderungen vorgenommen haben, speichern Sie das Skript mit einem anderen Namen, beispielsweise OD4BRemoveSCA.ps1, und ihn verwenden Sie, um einen Benutzer als Administrator einer Websitesammlung aus einer Gruppe von OneDrive for Business-Websites zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="cce4d-182">After you make these changes, save the script with a different name, such as OD4BRemoveSCA.ps1, and then use it to remove a user as a site collection administrator from a group of OneDrive for Business sites.</span></span>
