---
title: Verwenden der Inhaltssuche zum Durchsuchen des Postfachs und der OneDrive for Business-Website nach einer Liste von Benutzern
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: Verwenden Sie die Inhaltssuche und das Skript in diesem Artikel zum Durchsuchen der Postfächer und OneDrive für eine Gruppe von Benutzern.
ms.openlocfilehash: 2f0954bf7822ca6c82165ad20b2c732ab0594257
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31001278"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a><span data-ttu-id="b7059-103">Verwenden der Inhaltssuche zum Durchsuchen des Postfachs und der OneDrive for Business-Website nach einer Liste von Benutzern</span><span class="sxs-lookup"><span data-stu-id="b7059-103">Use Content Search to search the mailbox and OneDrive for Business site for a list of users</span></span>

<span data-ttu-id="b7059-104">Das Security & Compliance Center bietet eine Reihe von Windows PowerShell-Cmdlets, mit denen Sie zeitaufwändige eDiscovery-bezogene Aufgaben automatisieren können.</span><span class="sxs-lookup"><span data-stu-id="b7059-104">The Security & Compliance Center provides a number of Windows PowerShell cmdlets that let you automate time-consuming eDiscovery-related tasks.</span></span> <span data-ttu-id="b7059-105">Derzeit wird das Erstellen einer Inhaltssuche im Security & Compliance Center zum Durchsuchen einer Vielzahl von Speicherorten für Depot Inhalte Zeit und Vorbereitung benötigt.</span><span class="sxs-lookup"><span data-stu-id="b7059-105">Currently, creating a Content Search in the Security & Compliance Center to search a large number of custodian content locations takes time and preparation.</span></span> <span data-ttu-id="b7059-106">Bevor Sie eine Suche erstellen, müssen Sie die URL für jede OneDrive for Business-Website sammeln und dann jedes Postfach und jede neDrive for Business-Website zur Suche hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b7059-106">Before you create a search, you have to collect the URL for each OneDrive for Business site and then add each mailbox and O neDrive for Business site to the search.</span></span> <span data-ttu-id="b7059-107">In zukünftigen Versionen ist dies im Security & Compliance Center einfacher.</span><span class="sxs-lookup"><span data-stu-id="b7059-107">In future releases, this will be easier to do in the Security & Compliance Center.</span></span> <span data-ttu-id="b7059-108">Bis dahin können Sie dieses Verfahren mithilfe des Skripts in diesem Artikel automatisieren.</span><span class="sxs-lookup"><span data-stu-id="b7059-108">Until then, you can use the script in this article to automate this process.</span></span> <span data-ttu-id="b7059-109">Mit diesem Skript werden Sie aufgefordert, den Namen der mysite-Domäne Ihrer Organisation einzugeben (beispielsweise **contoso** in https://contoso-my.sharepoint.com)der URL, eine Liste der Benutzer-e-Mail-Adressen, den Namen der neuen Inhaltssuche und die zu verwendende Suchabfrage.</span><span class="sxs-lookup"><span data-stu-id="b7059-109">This script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), a list of user email addresses, the name of the new Content Search, and the search query to use.</span></span> <span data-ttu-id="b7059-110">Das Skript ruft die OneDrive for Business-URL für jeden Benutzer in der Liste ab und erstellt dann eine Inhaltssuche, die das Postfach und die OneDrive for Business-Website für jeden Benutzer in der Liste unter Verwendung der von Ihnen bereitgestellten Suchabfrage durchsucht.</span><span class="sxs-lookup"><span data-stu-id="b7059-110">The script gets the OneDrive for Business URL for each user in the list, and then it creates and starts a Content Search that searches the mailbox and OneDrive for Business site for each user in the list, using the search query that you provide.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="b7059-111">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="b7059-111">Before you begin</span></span>

- <span data-ttu-id="b7059-112">Sie müssen Mitglied der eDiscovery-Manager-Rollengruppe im Security & Compliance Center und ein globaler SharePoint Online-Administrator sein, um das Skript in Schritt 3 ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="b7059-112">You have to be a member of the eDiscovery Manager role group in the Security & Compliance Center and a SharePoint Online global administrator to run the script in Step 3.</span></span>
    
- <span data-ttu-id="b7059-113">Stellen Sie sicher, dass Sie die Liste der Benutzer, die Sie in Schritt 2 erstellen, und das Skript in Schritt 3 in demselben Ordner speichern.</span><span class="sxs-lookup"><span data-stu-id="b7059-113">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder.</span></span> <span data-ttu-id="b7059-114">Dadurch wird das Ausführen des Skripts vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="b7059-114">That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="b7059-115">Das Skript enthält eine minimale Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="b7059-115">The script includes minimal error handling.</span></span> <span data-ttu-id="b7059-116">Der Hauptzweck besteht darin, die Mailbox und die OneDrive for Business-Website der einzelnen Benutzer schnell und einfach zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="b7059-116">It's primary purpose is to quickly and easily search the mailbox and OneDrive for Business site of each user.</span></span>
    
- <span data-ttu-id="b7059-117">Die in diesem Thema bereitgestellten Beispielskripts werden unter keinem Microsoft Standard-Support Programm oder-Dienst unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7059-117">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service.</span></span> <span data-ttu-id="b7059-118">Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b7059-118">The sample scripts are provided AS IS without warranty of any kind.</span></span> <span data-ttu-id="b7059-119">Microsoft lehnt alle i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied Garantien einschließlich, ohne Einschränkung, implizite Garantien der Marktgängigkeit oder der Eignung für einen bestimmten Zweck ab.</span><span class="sxs-lookup"><span data-stu-id="b7059-119">Microsoft further disclaims all i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose.</span></span> <span data-ttu-id="b7059-120">Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen.</span><span class="sxs-lookup"><span data-stu-id="b7059-120">The entire risk arising out of the use or performance of the sample scripts and documentation remains with you.</span></span> <span data-ttu-id="b7059-121">Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b7059-121">In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="b7059-122">Schritt 1: Installieren der SharePoint Online-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="b7059-122">Step 1: Install the SharePoint Online Management Shell</span></span>
<span data-ttu-id="b7059-123"><a name="step1"> </a></span><span class="sxs-lookup"><span data-stu-id="b7059-123"></span></span>

<span data-ttu-id="b7059-124">Der erste Schritt besteht darin, die SharePoint Online-Verwaltungsshell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b7059-124">The first step is to install the SharePoint Online Management Shell.</span></span> <span data-ttu-id="b7059-125">Sie müssen die Shell nicht in diesem Verfahren verwenden, aber Sie müssen Sie installieren, da Sie die erforderlichen Voraussetzungen für das Skript enthält, das Sie in Schritt 3 ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7059-125">You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3.</span></span> <span data-ttu-id="b7059-126">Diese Voraussetzungen ermöglichen es dem Skript, mit SharePoint Online zu kommunizieren, um die URLs für die OneDrive für Business-Websites abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b7059-126">These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="b7059-127">Wechseln Sie zu [Einrichten der Windows PowerShell-Umgebung für die SharePoint Online-Verwaltungsshell](https://go.microsoft.com/fwlink/p/?LinkID=286318) , und führen Sie Schritt 1 und Schritt 2 aus, um die SharePoint Online-Verwaltungsshell zu installieren.</span><span class="sxs-lookup"><span data-stu-id="b7059-127">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell.</span></span>
  
## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="b7059-128">Schritt 2: Generieren einer Liste von Benutzern</span><span class="sxs-lookup"><span data-stu-id="b7059-128">Step 2: Generate a list of users</span></span>
<span data-ttu-id="b7059-129"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="b7059-129"></span></span>

<span data-ttu-id="b7059-130">Das Skript in Schritt 3 erstellt eine Inhaltssuche, um die Postfächer und OneDrive-Konten nach einer Liste von Benutzern zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="b7059-130">The script in Step 3 will create a Content Search to search the mailboxes and OneDrive accounts for a list of users.</span></span> <span data-ttu-id="b7059-131">Sie können die e-Mail-Adressen einfach in eine Textdatei eingeben, oder Sie können einen Befehl in Windows PowerShell ausführen, um eine Liste der e-Mail-Adressen abzurufen und Sie in einer Datei zu speichern (im gleichen Ordner, in dem Sie das Skript in Schritt 3 speichern).</span><span class="sxs-lookup"><span data-stu-id="b7059-131">You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="b7059-132">Hier ist ein [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) -Befehl, den Sie untersuchen können, um eine Liste der e-Mail-Adressen für alle Benutzer in Ihrer Organisation zu erhalten `Users.txt`und diese in einer Textdatei mit dem Namen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="b7059-132">Here's an [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) command that you can runt to get a list of email addresses for all users in your organization and save it to a text file named `Users.txt`.</span></span> 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

<span data-ttu-id="b7059-133">Nachdem Sie diesen Befehl ausgeführt haben, müssen Sie die Datei öffnen und den Header entfernen, der den Eigenschaftennamen enthält `PrimarySmtpAddress`.</span><span class="sxs-lookup"><span data-stu-id="b7059-133">After you run this command, be sure to open the file and remove the header that contains the property name,  `PrimarySmtpAddress`.</span></span> <span data-ttu-id="b7059-134">Die Textdatei sollte nur eine Liste von e-Mail-Adressen enthalten, und nichts anderes.</span><span class="sxs-lookup"><span data-stu-id="b7059-134">The text file should just contain a list of email addresses, and nothing else.</span></span> <span data-ttu-id="b7059-135">Stellen Sie sicher, dass vor oder nach der Liste der e-Mail-Adressen keine leeren Zeilen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b7059-135">Make sure there are no blank rows before or after the list of email addresses.</span></span>
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a><span data-ttu-id="b7059-136">Schritt 3: Ausführen des Skripts zum Erstellen und Starten der Suche</span><span class="sxs-lookup"><span data-stu-id="b7059-136">Step 3: Run the script to create and start the search</span></span>

<span data-ttu-id="b7059-137">Wenn Sie das Skript in diesem Schritt ausführen, werden Sie aufgefordert, die folgenden Informationen einzugeben.</span><span class="sxs-lookup"><span data-stu-id="b7059-137">When you run the script in this step, it will prompt you for the following information.</span></span> <span data-ttu-id="b7059-138">Stellen Sie sicher, dass diese Informationen bereit sind, bevor Sie das Skript ausführen.</span><span class="sxs-lookup"><span data-stu-id="b7059-138">Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="b7059-139">**Ihre Benutzeranmeldeinformationen** – das Skript verwendet Ihre Anmeldeinformationen für den Zugriff auf SharePoint Online, um die OneDrive for Business-URLs abzurufen und eine Verbindung mit dem Security _AMP_ Compliance Center mit Remote-PowerShell herzustellen.</span><span class="sxs-lookup"><span data-stu-id="b7059-139">**Your user credentials** - The script will use your credentials to access SharePoint Online to get the OneDrive for Business URLs and to connect to the Security & Compliance Center with remote PowerShell.</span></span> 
    
- <span data-ttu-id="b7059-140">**Name der mysite-Domäne** -die Domäne mysite ist die Domäne, die alle OneDrive für Business-Websites in Ihrer Organisation enthält.</span><span class="sxs-lookup"><span data-stu-id="b7059-140">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization.</span></span> <span data-ttu-id="b7059-141">Wenn beispielsweise die URL für Ihre Domäne "mysite" **https://contoso-my.sharepoint.com**lautet, geben Sie ein `contoso` , wenn Sie vom Skript aufgefordert werden, den Namen Ihrer Domäne "mysite" einzugeben.</span><span class="sxs-lookup"><span data-stu-id="b7059-141">For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="b7059-142">**Pfadname der Textdatei aus Schritt 2** : der Pfadname der Textdatei, die Sie in Schritt 2 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b7059-142">**Pathname of the text file from Step 2** - The pathname of the text file that you created in Step 2.</span></span> <span data-ttu-id="b7059-143">Wenn sich die Textdatei und das Skript im gleichen Ordner befinden, geben Sie den Namen der Textdatei ein.</span><span class="sxs-lookup"><span data-stu-id="b7059-143">If the text file and the script are located in the same folder, then enter the name of the text file.</span></span> <span data-ttu-id="b7059-144">Geben Sie andernfalls den vollständigen Pfadnamen für die Textdatei ein.</span><span class="sxs-lookup"><span data-stu-id="b7059-144">Otherwise, enter the complete pathname for the text file.</span></span> 
    
- <span data-ttu-id="b7059-145">**Name der Inhaltssuche** – der Name der Inhaltssuche, die vom Skript erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b7059-145">**Name of the Content Search** - The name of the Content Search that will be created by the script.</span></span> 
    
- <span data-ttu-id="b7059-146">**Suchabfrage** : die Suchabfrage, die mit der Inhaltssuche verwendet wird, wird erstellt und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b7059-146">**Search query** - The search query that will be used with the Content Search is created and run.</span></span> <span data-ttu-id="b7059-147">Weitere Informationen zu Suchabfragen finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="b7059-147">For more information about search queries, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>


<span data-ttu-id="b7059-148">**So führen Sie das Skript aus:**</span><span class="sxs-lookup"><span data-stu-id="b7059-148">**To run the script:**</span></span>
    
1. <span data-ttu-id="b7059-149">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `SearchEXOOD4B.ps1`.</span><span class="sxs-lookup"><span data-stu-id="b7059-149">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchEXOOD4B.ps1`.</span></span> <span data-ttu-id="b7059-150">Speichern Sie die Datei in dem Ordner, in dem Sie die Liste der Benutzer in Schritt 2 gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="b7059-150">Save the file to the same folder where you saved the list of users in Step 2.</span></span>
    
  ```
  # This PowerShell script will prompt you for the following information:
  #    * Your user credentials 
  #    * The name of your organization's MySite domain                                              
  #    * The pathname for the text file that contains a list of user email addresses
  #    * The name of the Content Search that will be created
  #    * The search query string
  # The script will then:
  #    * Find the OneDrive for Business site for each user in the text file
  #    * Create and start a Content Search using the above information
  # Get user credentials
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  # Get the user's MySite domain name.  We use this to create the admin URL and root URL for OneDrive for Business
  $mySiteDomain = Read-Host "What is your organization's MySite domain?  For example,  'contoso' for 'https://contoso-my.sharepoint.com'"
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
  # Get other required information
  $inputfile = read-host "Enter the file name of the text file that contains the email addresses for the users you want to search"
  $searchName = Read-Host "Enter the name for the new search"
  $searchQuery = Read-Host "Enter the search query you want to use"
  $emailAddresses = Get-Content $inputfile | where {$_ -ne ""}  | foreach{ $_.Trim() }
  # Connect to Office 365
  if (!$s -or !$a)
  {
      $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
      $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Could not create PowerShell session."
          return;
      }
  }
  # Load the SharePoint assemblies from the SharePoint Online Management Shell
  # To install, go to http://go.microsoft.com/fwlink/p/?LinkId=255251
  if (!$SharePointClient -or !$SPRuntime -or !$SPUserProfile)
  {
      $SharePointClient = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client")
      $SPRuntime = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.Runtime")
      $SPUserProfile = [System.Reflection.Assembly]::LoadWithPartialName("Microsoft.SharePoint.Client.UserProfiles")
      if (!$SharePointClient)
      {
          Write-Error "SharePoint Online Management Shell isn't installed, please install from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then run this script again"
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Add the path of the User Profile Service to the SPO admin URL, then create a new webservice proxy to access it
  $proxyaddr = "$AdminUrl/_vti_bin/UserProfileService.asmx?wsdl"
  $UserProfileService= New-WebServiceProxy -Uri $proxyaddr -UseDefaultCredential False
  $UserProfileService.Credentials = $credentials
  # Take care of auth cookies
  $strAuthCookie = $spCreds.GetAuthenticationCookie($AdminUrl)
  $uri = New-Object System.Uri($AdminUrl)
  $container = New-Object System.Net.CookieContainer
  $container.SetCookies($uri, $strAuthCookie)
  $UserProfileService.CookieContainer = $container
  Write-Host "Getting each user's OneDrive for Business URL"
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
      try
      {
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" } 
          $url = $prop.values[0].value
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "-$emailAddress => $furl"
      }
      catch
      {
          Write-Warning "Could not locate OneDrive for $emailAddress"
      }
  }
  Write-Host "Creating and starting the search"
  $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $emailAddresses -SharePointLocation $urls -ContentMatchQuery $searchQuery
  # Finally, start the search and then display the status
  if($search)
  {
      Start-ComplianceSearch $search.Name
      Get-ComplianceSearch $search.Name
  }
  
  ```

2. <span data-ttu-id="b7059-151">Öffnen Sie Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben, und in der Liste der Benutzer aus Schritt 2.</span><span class="sxs-lookup"><span data-stu-id="b7059-151">Open Windows PowerShell and go to the folder where you saved the script and the list of users from Step 2.</span></span>
    
3. <span data-ttu-id="b7059-152">Starten Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b7059-152">Start the script; for example:</span></span>
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. <span data-ttu-id="b7059-153">Wenn Sie zur Eingabe Ihrer Anmeldeinformationen aufgefordert werden, geben Sie Ihre e-Mail-Adresse und Ihr Kennwort ein, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="b7059-153">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="b7059-154">Geben Sie die folgenden Informationen ein, wenn Sie vom Skript dazu aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b7059-154">Enter following information when prompted by the script.</span></span> <span data-ttu-id="b7059-155">Geben Sie jede Information ein, und drücken **Sie die Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="b7059-155">Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="b7059-156">Der Name der mysite-Domäne.</span><span class="sxs-lookup"><span data-stu-id="b7059-156">The name of your MySite domain.</span></span> 
    
    - <span data-ttu-id="b7059-157">Der Pfadname der Textdatei, die die Liste der Benutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="b7059-157">The pathname of the text file that contains the list of users.</span></span>
    
    - <span data-ttu-id="b7059-158">Ein Name für die Inhaltssuche.</span><span class="sxs-lookup"><span data-stu-id="b7059-158">A name for the Content Search.</span></span>
    
    - <span data-ttu-id="b7059-159">Die Suchabfrage (lassen Sie dieses Feld leer, um alle Elemente in den Inhaltsspeicherorten zurückzugeben).</span><span class="sxs-lookup"><span data-stu-id="b7059-159">The search query (leave this blank to return all items in the content locations).</span></span>
    
    <span data-ttu-id="b7059-160">Das Skript ruft die URLs für jede OneDrive for Business-Website ab und erstellt und startet dann die Suche.</span><span class="sxs-lookup"><span data-stu-id="b7059-160">The script gets the URLs for each OneDrive for Business site and then creates and starts the search.</span></span> <span data-ttu-id="b7059-161">Sie können entweder das Cmdlet **Get-ComplianceSearch** in Security _AMP_ Compliance Center PowerShell ausführen, um die Suchstatistiken und-Ergebnisse anzuzeigen, oder Sie können zur Seite " **Inhaltssuche** " im Security & Compliance Center wechseln, um Informationen anzuzeigen. über die Suche.</span><span class="sxs-lookup"><span data-stu-id="b7059-161">You can either run the **Get-ComplianceSearch** cmdlet in Security & Compliance Center PowerShell to display the search statistics and results, or you can go to the **Content search** page in the Security & Compliance Center to view information about the search.</span></span> 
