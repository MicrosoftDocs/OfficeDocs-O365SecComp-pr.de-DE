---
title: Verwenden Sie ein Skript zum Hinzufügen von Benutzern zu einem Haltestatus in einer eDiscovery-Fall in die Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/23/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: Führen Sie ein Skript, um schnell Postfächer und OneDrive for Business-Websites zu einem neuen Haltestatus, die einem eDiscovery-Fall in die Office 365-Sicherheit zugeordnet ist &amp; Compliance Center.
ms.openlocfilehash: 2c93deb14bc8c1f89dab7bb054d2e94db06cfbd5
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038258"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="d9ae7-103">Verwenden Sie ein Skript zum Hinzufügen von Benutzern zu einem Haltestatus in einer eDiscovery-Fall in die Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="d9ae7-103">Use a script to add users to a hold in an eDiscovery case in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="d9ae7-p101">Die Office 365-Sicherheit &amp; Compliance Center bietet viele der Windows PowerShell-Cmdlets, mit denen Sie automatisieren zeitaufwändige Aufgaben im Zusammenhang mit erstellen und Verwalten von eDiscovery-Fälle. Verwenden Sie das Groß-/Kleinschreibung eDiscovery-Tool derzeit in die Sicherheit &amp; Compliance Center, um eine große Anzahl von Verwaltungsberechtigten Speicherorte für Inhalte in die Warteschleife stellen nimmt Zeit und Vorbereitung. Bevor Sie einen Haltestatus erstellen, müssen Sie beispielsweise die URL für jede OneDrive for Business-Website zu erfassen, die Sie in die Warteschleife stellen möchten. Für jeden Benutzer, den Sie in die Warteschleife stellen möchten, müssen Sie dann ihr Postfach und ihre OneDrive for Business-Site dem Haltestatus hinzufügen. In zukünftigen Versionen des Wertpapiers &amp; Compliance Center, dies wird einfacher abrufen. Bis zu diesem Zeitpunkt können Sie das Skript in diesem Artikel verwenden, um diese zu automatisieren.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p101">The Office 365 Security &amp; Compliance Center provides lots of Windows PowerShell cmdlets that let you automate time-consuming tasks related to creating and managing eDiscovery cases. Currently, using the eDiscovery case tool in the Security &amp; Compliance Center to place a large number of custodian content locations on hold takes time and preparation. For example, before you create a hold, you have to collect the URL for each OneDrive for Business site that you want to place on hold. Then for each user you want to place on hold, you have to add their mailbox and their OneDrive for Business site to the hold. In future releases of the Security &amp; Compliance Center, this will get easier to do. Until then, you can use the script in this article to automate this process.</span></span>
  
<span data-ttu-id="d9ae7-p102">Das Skript werden Sie aufgefordert, den Namen des MeineWebsite-Domäne Ihrer Organisation (beispielsweise **"Contoso"** in der URL https://contoso-my.sharepoint.com), den Namen eines vorhandenen eDiscovery-Fall, den Namen des neuen Haltestatus, die dem Fall zugeordneten, eine Liste von e-Mail-Adressen der Benutzer Sie benötigen Platzieren Sie auf halten und eine Suchabfrage verwenden, wenn Sie eine abfragebasierte Aufbewahrung erstellen möchten. Das Skript ruft dann die URL für die OneDrive for Business-Site für jeden Benutzer in der Liste, den neuen Haltebereich erstellt und dann hinzugefügt für das Postfach und OneDrive for Business-Site für jeden Benutzer in der Liste den Haltestatus. Das Skript generiert auch Protokolldateien, die Informationen zu den neuen Haltestatus enthalten.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p102">The script prompts you for the name of your organization's MySite domain (for example, **contoso** in the URL https://contoso-my.sharepoint.com), the name of an existing eDiscovery case, the name of the new hold that associated with the case, a list of email addresses of the users you want to put on hold, and a search query to use if you want to create a query-based hold. The script then gets the URL for the OneDrive for Business site for each user in the list, creates the new hold, and then adds the mailbox and OneDrive for Business site for each user in the list to the hold. The script also generates log files that contain information about the new hold.</span></span> 
  
<span data-ttu-id="d9ae7-113">Hier sind die Schritte zu diesem Zweck müssen:</span><span class="sxs-lookup"><span data-stu-id="d9ae7-113">Here are the steps to make this happen:</span></span>
  
[<span data-ttu-id="d9ae7-114">Schritt 1: Installieren der SharePoint Online-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="d9ae7-114">Step 1: Install the SharePoint Online Management Shell</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[<span data-ttu-id="d9ae7-115">Schritt 2: Eine Liste der Benutzer generieren</span><span class="sxs-lookup"><span data-stu-id="d9ae7-115">Step 2: Generate a list of users</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[<span data-ttu-id="d9ae7-116">Schritt 3: Ausführen des Skripts zum Erstellen eines Haltestatus und Hinzufügen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="d9ae7-116">Step 3: Run the script to create a hold and add users</span></span>](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a><span data-ttu-id="d9ae7-117">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="d9ae7-117">Before you begin</span></span>

- <span data-ttu-id="d9ae7-p103">Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center und ein globaler SharePoint Online-Administrator zum Ausführen des Skripts in Schritt 3. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center and a SharePoint Online global administrator to run the script in Step 3. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="d9ae7-p104">Maximal 1.000 Postfächer und 100 Websites zu einem Haltestatus, die einem eDiscovery-Fall in das Wertpapier zugeordnet wurde hinzugefügt werden kann &amp; Compliance Center. Unter der Annahme, dass alle Benutzer, die Sie in die Warteschleife stellen möchten ein OneDrive for Business-Website verfügt, können Sie maximal 100 Benutzer zu einem Haltestatus mithilfe des Skripts in diesem Artikel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p104">A maximum of 1,000 mailboxes and 100 sites can be added to a hold that's associated with an eDiscovery case in the Security &amp; Compliance Center. Assuming that every user that you want to place on hold has a OneDrive for Business site, you can add a maximum of 100 users to a hold using the script in this article.</span></span> 
    
- <span data-ttu-id="d9ae7-p105">Achten Sie darauf, dass die Liste der Benutzer zu speichern, die Sie in Schritt2 und das Skript in Schritt 3 im gleichen Ordner erstellen. Die wird zum Ausführen des Skripts erleichtern.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p105">Be sure to save the list of users that you create in Step 2 and the script in Step 3 to the same folder. That will make it easier to run the script.</span></span>
    
- <span data-ttu-id="d9ae7-p106">Das Skript fügt die Liste der Benutzer zu einem neuen Haltestatus, der eine vorhandene Anfrage zugeordnet ist. Stellen Sie sicher, dass die Groß-/Kleinschreibung, der Sie den Haltestatus mit zuordnen möchten erstellt wird, bevor Sie das Skript ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p106">The script adds the list of users to a new hold that is associated with an existing case. Be sure the case that you want to associate the hold with is created before you run the script.</span></span>
    
- <span data-ttu-id="d9ae7-p107">Das Skript enthält minimale Fehlerbehandlung. Der primäre Zweck ist, um schnell und einfach das Postfach zu platzieren, und halten Sie OneDrive for Business-Website für jeden Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p107">The script includes minimal error handling. Its primary purpose is to quickly and easily place the mailbox and OneDrive for Business site of each user on hold.</span></span>
    
- <span data-ttu-id="d9ae7-p108">Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p108">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>

## <a name="step-1-install-the-sharepoint-online-management-shell"></a><span data-ttu-id="d9ae7-133">Schritt 1: Installieren der SharePoint Online-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="d9ae7-133">Step 1: Install the SharePoint Online Management Shell</span></span>

<span data-ttu-id="d9ae7-p109">Der erste Schritt besteht, die SharePoint Online-Verwaltungsshell zu installieren, wenn es nicht bereits auf dem lokalen Computer installiert ist. Sie müssen zum Verwenden der Shell in diesem Verfahren, aber Sie installieren, da es enthält die erforderlichen Komponenten erforderlich, von dem Skript, das Sie in Schritt 3 ausführen müssen. Diese erforderlichen Komponenten ermöglichen das Skript zur Kommunikation mit SharePoint Online, um die URLs für die OneDrive for Business-Websites erhalten.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p109">The first step is to install the SharePoint Online Management Shell if it's not already installed on your local computer. You don't have to use the shell in this procedure, but you have to install it because it contains pre-requisites required by the script that you run in Step 3. These prerequisites allow the script to communicate with SharePoint Online to get the URLs for the OneDrive for Business sites.</span></span>
  
<span data-ttu-id="d9ae7-137">Wechseln Sie zum [Einrichten von SharePoint Online-Verwaltungsshell Windows PowerShell--Umgebung](https://go.microsoft.com/fwlink/p/?LinkID=286318) , und führen Sie Schritt 1 und Schritt2, um die SharePoint Online-Verwaltungsshell auf dem lokalen Computer zu installieren.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-137">Go to [Set up the SharePoint Online Management Shell Windows PowerShell environment](https://go.microsoft.com/fwlink/p/?LinkID=286318) and perform Step 1 and Step 2 to install the SharePoint Online Management Shell on your local computer.</span></span> 

## <a name="step-2-generate-a-list-of-users"></a><span data-ttu-id="d9ae7-138">Schritt 2: Eine Liste der Benutzer generieren</span><span class="sxs-lookup"><span data-stu-id="d9ae7-138">Step 2: Generate a list of users</span></span>
<span data-ttu-id="d9ae7-139"><a name="step2"> </a></span><span class="sxs-lookup"><span data-stu-id="d9ae7-139"></span></span>

<span data-ttu-id="d9ae7-p110">Das Skript in Schritt 3 wird das Erstellen eines Haltestatus, das mit einem eDiscovery-Fall und Hinzufügen der Postfächer und OneDrive für Websites mit Geschäftsdaten aus einer Liste von Benutzern, die Sperre zugeordnet ist. Sie können nur die e-Mail-Adressen in einer Textdatei eingeben, oder führen Sie einen Befehl in Windows PowerShell zum Abrufen einer Liste von e-Mail-Adressen und diese in einer Datei (befindet sich in demselben Ordner, den Sie das Skript in Schritt 3 sparen) speichern.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p110">The script in Step 3 will create a hold that's associated with an eDiscovery case, and the add the mailboxes and OneDrive for Business sites of a list of users to the hold. You can just type the email addresses in a text file, or you can run a command in Windows PowerShell to get a list of email addresses and save them to a file (located in same folder that you'll save the script to in Step 3).</span></span>
  
<span data-ttu-id="d9ae7-142">Nachfolgend finden Sie ein PowerShell-Befehl (, die Sie ausführen, mithilfe von remote-PowerShell mit Ihrer Exchange Online-Organisation verbunden ist) zum Abrufen einer Liste von e-Mail-Adressen für alle Benutzer in Ihrer Organisation, und speichern Sie eine Textdatei mit dem Namen HoldUsers.txt.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-142">Here's a PowerShell command (that you run by using remote PowerShell connected to your Exchange Online organization) to get a list of email addresses for all users in your organization and save it to a text file named HoldUsers.txt.</span></span>
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

<span data-ttu-id="d9ae7-p111">Nachdem Sie führen Sie diesen Befehl, öffnen Sie die Textdatei und den Header entfernen, der Name der Eigenschaft enthält `PrimarySmtpAddress`. Entfernen Sie alle e-Mail-Adressen außer derjenigen, die für die Benutzer, die Sie dem Haltestatus hinzufügen, die Sie in Schritt 3 erstellen, möchten. Stellen Sie sicher, dass keine leeren Zeilen vor oder nach der Liste der e-Mail-Adressen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p111">After you run this command, open the text file and remove the header that contains the property name,  `PrimarySmtpAddress`. Then remove all email addresses except the ones for the users that you want to add to the hold that you'll create in Step 3. Make sure there are no blank rows before or after the list of email addresses.</span></span>
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a><span data-ttu-id="d9ae7-146">Schritt 3: Ausführen des Skripts zum Erstellen eines Haltestatus und Hinzufügen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="d9ae7-146">Step 3: Run the script to create a hold and add users</span></span>
<span data-ttu-id="d9ae7-147"><a name="step3"> </a></span><span class="sxs-lookup"><span data-stu-id="d9ae7-147"></span></span>

<span data-ttu-id="d9ae7-p112">Wenn Sie das Skript in diesem Schritt ausführen, fordert es Sie für die folgenden Informationen. Achten Sie darauf, dass Sie diese Informationen bereit, bevor Sie das Skript ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p112">When you run the script in this step, it will prompt you for the following information. Be sure to have this information ready before you run the script.</span></span>
  
- <span data-ttu-id="d9ae7-p113">**Ihre Anmeldeinformationen** – das Skript wird unter Verwendung Ihrer Anmeldeinformationen für die Verbindung für die Sicherheit &amp; Compliance Center mit remote-PowerShell. Es wird auch diese Anmeldeinformationen verwenden, um SharePoint Online, um die OneDrive for Business-URLs für die Liste der Benutzer abrufen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p113">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center with remote PowerShell. It will also use these credentials to access SharePoint Online to get the OneDrive for Business URLs for the list of users.</span></span>
    
- <span data-ttu-id="d9ae7-p114">**Namen der Domäne MeineWebsite** - MeineWebsite der Domäne ist die Domäne, die alle die OneDrive for Business-Websites in Ihrer Organisation enthält. Beispielsweise ist die URL für Ihre Domäne MySite **https://contoso-my.sharepoint.com**, und klicken Sie dann Eingabe der `contoso` Wenn des Skripts aufgefordert, den Namen Ihrer Domäne MySite.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p114">**Name of your MySite domain** - The MySite domain is the domain that contains all the OneDrive for Business sites in your organization. For example, if the URL for your MySite domain is **https://contoso-my.sharepoint.com**, then you would enter  `contoso` when the script prompts you for the name of your MySite domain.</span></span> 
    
- <span data-ttu-id="d9ae7-p115">Der **Name der Anfrage** – den Namen einer vorhandenen Anfrage. Das Skript erstellt einen neuen Haltestatus, der in diesem Fall zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p115">**Name of the case** - The name of an existing case. The script will create a new hold that is associated with this case.</span></span>
    
- <span data-ttu-id="d9ae7-156">**Name des Haltestatus** – der Name des Haltestatus das Skript erstellen und Zuordnen der angegebenen Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-156">**Name of the hold** - The name of the hold the script will create and associate with the specified case.</span></span>
    
- <span data-ttu-id="d9ae7-p116">**Halten Sie Search-Abfrage für ein abfragebasiertes** - Sie können eine abfragebasierte Aufbewahrung erstellen, sodass nur die Inhalte, die die angegebenen Suchkriterien erfüllt in die Warteschleife gestellt wird. Um den gesamten Inhalt im Archiv zu platzieren, drücken Sie die **EINGABETASTE** , wenn Sie für eine Suchabfrage aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p116">**Search query for a query-based hold** - You can create a query-based hold so that only the content that meets the specified search criteria is placed on hold. To place all content on hold, just press **Enter** when you're prompted for a search query.</span></span> 
    
- <span data-ttu-id="d9ae7-p117">**Ob Sie die Sperre aktivieren** - können Sie das Skript den Haltestatus einschalten, nachdem er erstellt wird oder Sie können das Skript den Haltestatus erstellen, ohne zu aktivieren. Wenn Sie nicht über das Skript die Sperre aktivieren verfügen, können Sie es auf aktivieren, weiter unten in der Sicherheit &amp; Compliance Center oder indem Sie die folgenden PowerShell-Befehle ausführen:</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p117">**Whether or not to turn the hold on** - You can have the script turn the hold on after it's created or you can have the script create the hold without enabling it. If you don't have the script turn on the hold, you can turn it on later in the Security &amp; Compliance Center or by running the following PowerShell commands:</span></span> 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- <span data-ttu-id="d9ae7-p118">Der **Name der Textdatei mit der Liste der Benutzer** – den Namen der Textdatei aus Schritt2 mit der Liste der Benutzer dem Haltestatus hinzufügen. Wenn diese Datei im selben Ordner wie das Skript gespeichert ist, geben Sie einfach den Namen der Datei (beispielsweise HoldUsers.txt). Wenn die Textdatei in einen anderen Ordner befindet, geben Sie den vollständigen Pfadnamen der Datei.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p118">**Name of the text file with the list of users** - The name of the text file from Step 2 that contains the list of users to add to the hold. If this file is located in the same folder as the script, just type the name of the file (for example, HoldUsers.txt). If the text file is in another folder, type the full pathname of the file.</span></span>
    
<span data-ttu-id="d9ae7-164">Nachdem Sie die Informationen gesammelt haben, der das Skript für aufgefordert werden, ist der letzte Schritt zum Ausführen des Skripts zum Erstellen des neuen Haltebereich und Benutzer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-164">After you've collected the information that the script will prompt you for, the final step is to run the script to create the new hold and add users to it.</span></span>
  
1. <span data-ttu-id="d9ae7-165">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `AddUsersToHold.ps1`.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-165">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `AddUsersToHold.ps1`.</span></span>
    
  ```
  #script begin
  " " 
  write-host "***********************************************"
  write-host "   Office 365 Security &amp; Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery cases - Add users to a hold   " -foregroundColor yellow -backgroundcolor darkgreen 
  write-host "***********************************************"
  " " 
  # Get user credentials &amp; Connect to Office 365 SCC, SPO
  $credentials = Get-Credential -Message "Specify your credentials to connect to the Office 365 Security &amp; Compliance Center and SharePoint Online"
  $s = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri "https://ps.compliance.protection.outlook.com/powershell-liveid" -Credential $credentials -Authentication Basic -AllowRedirection -SessionOption (New-PSSessionOption -SkipCACheck -SkipCNCheck -SkipRevocationCheck)
  $a = Import-PSSession $s -AllowClobber
      if (!$s)
      {
          Write-Error "Couldn't create PowerShell session."
          return;
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
          Write-Error "The SharePoint Online Management Shell isn't installed. Please install it from: http://go.microsoft.com/fwlink/p/?LinkId=255251 and then re-run this script."
          return;
      }
  }
  if (!$spCreds)
  {
      $spCreds = New-Object Microsoft.SharePoint.Client.SharePointOnlineCredentials($credentials.UserName, $credentials.Password)
  }
  # Get the user's MySite domain name. We use this to create the admin URL and root URL for OneDrive for Business
  ""
  $mySiteDomain = Read-Host "Enter the name of your organization's MySite domain. For example, 'contoso' for 'https://contoso-my.sharepoint.com'"
  ""
  # Get other required information
  do{
  $casename = Read-Host "Enter the name of the case"
  $caseexists = (get-compliancecase -identity "$casename" -erroraction SilentlyContinue).isvalid
  if($caseexists -ne 'True')
  {""
  write-host "A case named '$casename' doesn't exist. Please specify the name of an existing case, or create a new case and then re-run the script." -foregroundColor Yellow
  ""}
  }While($caseexists -ne 'True')
  ""
  do{
  $holdName = Read-Host "Enter the name of the new hold"
  $holdexists=(get-caseholdpolicy -identity "$holdname" -case "$casename" -erroraction SilentlyContinue).isvalid
  if($holdexists -eq 'True')
  {""
  write-host "A hold named '$holdname' already exists. Please specify a new hold name." -foregroundColor Yellow
  ""}
  }While($holdexists -eq 'True')
  ""
  $holdQuery = Read-Host "Enter a search query to create a query-based hold, or press Enter to hold all content"
  ""
  $holdstatus = read-host "Do you want the hold enabled after it's created? (Yes/No)"
  do{
  ""
  $inputfile = read-host "Enter the name of the text file that contains the email addresses of the users to add to the hold"
  ""
  $fileexists = test-path -path $inputfile
  if($fileexists -ne 'True'){write-host "$inputfile doesn't exist. Please enter a valid file name." -foregroundcolor Yellow}
  }while($fileexists -ne 'True')
  #Import the list of addresses from the txt file.  Trim any excess spaces and make sure all addresses 
      #in the list are unique.
    [array]$emailAddresses = Get-Content $inputfile -ErrorAction SilentlyContinue | where {$_.trim() -ne ""}  | foreach{ $_.Trim() }
    [int]$dupl = $emailAddresses.count
    [array]$emailAddresses = $emailAddresses | select-object -unique
    $dupl -= $emailAddresses.count
  #Validate email addresses so the hold creation does not run in to an error.
  if($emailaddresses.count -gt 0){
  write-host ($emailAddresses).count "addresses were found in the text file. There were $dupl duplicate entries in the file." -foregroundColor Yellow
  ""
  Write-host "Validating the email addresses. Please wait..." -foregroundColor Yellow
  ""
  $finallist =@()
  foreach($emailAddress in $emailAddresses)
  {
  if((get-recipient $emailaddress -erroraction SilentlyContinue).isvalid -eq 'True')
  {$finallist += $emailaddress}
  else {"Unable to find the user $emailaddress"
  [array]$excludedlist += $emailaddress}
  }
  ""
  #find user's OneDrive Site URL using email address
  Write-Host "Getting the URL for each user's OneDrive for Business site." -foregroundColor Yellow
  ""
  $AdminUrl = "https://$mySiteDomain-admin.sharepoint.com"
  $mySiteUrlRoot = "https://$mySiteDomain-my.sharepoint.com"
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
  $urls = @()
  foreach($emailAddress in $emailAddresses)
  {
        try{
          $prop = $UserProfileService.GetUserProfileByName("i:0#.f|membership|$emailAddress") | Where-Object { $_.Name -eq "PersonalSpace" }
          $url = $prop.values[0].value
        if($url -ne $null){
          $furl = $mySiteUrlRoot + $url
          $urls += $furl
          Write-Host "- $emailAddress => $furl"
        [array]$ODadded += $furl}
    else{    
          Write-Warning "Couldn't locate OneDrive for $emailAddress"
        [array]$ODExluded += $emailAddress
      }}
    catch { 
    Write-Warning "Could not locate OneDrive for $emailAddress"
    [array]$ODExluded += $emailAddress
    Continue }
  }
  if(($finallist.count -gt 0) -or ($urls.count -gt 0)){
  ""
  Write-Host "Creating the hold named $holdname. Please wait..." -foregroundColor Yellow
  if(($holdstatus -eq "Y") -or ($holdstatus -eq  "y") -or ($holdstatus -eq "yes") -or ($holdstatus -eq "YES")){
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $True | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery | out-null
  }
  else{
  New-CaseHoldPolicy -Name "$holdName" -Case "$casename" -ExchangeLocation $finallist -SharePointLocation $urls -Enabled $false | out-null
  New-CaseHoldRule -Name "$holdName" -Policy "$holdname" -ContentMatchQuery $holdQuery -disabled $true | out-null
  }
  ""
  }
  else {"No valid locations were identified. Therefore, the hold wasn't created."}
  #write log files (if needed)
  $newhold=Get-CaseHoldPolicy -Identity "$holdname" -Case "$casename" -erroraction SilentlyContinue
  $newholdrule=Get-CaseHoldRule -Identity "$holdName" -erroraction SilentlyContinue
  if(($ODAdded.count -gt 0) -or ($ODExluded.count -gt 0) -or ($finallist.count -gt 0) -or ($excludedlist.count -gt 0) -or ($newhold.isvalid -eq 'True') -or ($newholdrule.isvalid -eq 'True'))
  {
  Write-Host "Generating output files..." -foregroundColor Yellow
  if($ODAdded.count -gt 0){
  "OneDrive Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.SharePointLocation.name | add-content .\LocationsOnHold.txt}
  if($ODExluded.count -gt 0){ 
  "Users without OneDrive locations" | add-content .\LocationsNotOnHold.txt
  "================================" | add-content .\LocationsNotOnHold.txt
  $ODExluded | add-content .\LocationsNotOnHold.txt}
  if($finallist.count -gt 0){
  " " | add-content .\LocationsOnHold.txt
  "Exchange Locations" | add-content .\LocationsOnHold.txt
  "==================" | add-content .\LocationsOnHold.txt 
  $newhold.ExchangeLocation.name | add-content .\LocationsOnHold.txt}
  if($excludedlist.count -gt 0){
  " "| add-content .\LocationsNotOnHold.txt
  "Mailboxes not added to the hold" | add-content .\LocationsNotOnHold.txt
  "===============================" | add-content .\LocationsNotOnHold.txt
  $excludedlist | add-content .\LocationsNotOnHold.txt}
  $FormatEnumerationLimit=-1
  if($newhold.isvalid -eq 'True'){$newhold|fl >.\GetCaseHoldPolicy.txt}
  if($newholdrule.isvalid -eq 'True'){$newholdrule|Fl >.\GetCaseHoldRule.txt}
  }
  }
  else {"The hold wasn't created because no valid entries were found in the text file."}
  ""
  Write-host "Script complete!" -foregroundColor Yellow
  ""
  #script end
  ```

2. <span data-ttu-id="d9ae7-166">Öffnen Sie auf dem lokalen Computer Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-166">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="d9ae7-167">Führen Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d9ae7-167">Run the script; for example:</span></span>
    
      ```
    .\AddUsersToHold.ps1
      ```

4. <span data-ttu-id="d9ae7-168">Geben Sie die Informationen, der das Skript für aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-168">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="d9ae7-p119">Das Skript stellt eine Verbindung zur Sicherheit und Compliance Center PowerShell, und klicken Sie dann erstellt die neue Warteschleife in der eDiscovery-Fall und die Postfächer und OneDrive für Unternehmen für die Benutzer in der Liste hinzugefügt. Sie können die Groß-/Kleinschreibung auf der Seite **eDiscovery** in das Wertpapier wechseln &amp; Compliance Center, um den neuen Haltestatus anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p119">The script connects to Security & Compliance Center PowerShell, and then creates the new hold in the eDiscovery case and adds the mailboxes and OneDrive for Business for the users in the list. You can go to the case on the **eDiscovery** page in the Security &amp; Compliance Center to view the new hold.</span></span> 
    
<span data-ttu-id="d9ae7-171">Nach Abschluss des Skripts ausgeführt, es werden die folgenden Protokolldateien erstellt und speichert sie in den Ordner, der das Skript gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-171">After the script is finished running, it creates the following log files, and saves them to the folder where the script is located.</span></span>
  
- <span data-ttu-id="d9ae7-172">**LocationsOnHold.txt** - enthält eine Liste der Postfächer und OneDrive für Websites mit Geschäftsdaten, die das Skript erfolgreich auf platziert enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-172">**LocationsOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script successfully placed on hold.</span></span>
    
- <span data-ttu-id="d9ae7-p120">**LocationsNotOnHold.txt** - enthält eine Liste der Postfächer und OneDrive for Business-Websites, die das Skript nicht in die Warteschleife stellen. Wenn ein Benutzer ein Postfach, aber keiner OneDrive for Business-Website verfügt, würde der Benutzer in der Liste der OneDrive for Business-Websites in die Warteschleife gestellt wurden nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p120">**LocationsNotOnHold.txt** - Contains a list of mailboxes and OneDrive for Business sites that the script did not place on hold. If a user has a mailbox, but not a OneDrive for Business site, the user would be included in the list of OneDrive for Business sites that weren't placed on hold.</span></span>
    
- <span data-ttu-id="d9ae7-p121">**GetCaseHoldPolicy.txt** - enthält die Ausgabe des Cmdlets **Get-CaseHoldPolicy** für den neuen Haltestatus, die das Skript ausgeführt wurde, nach dem Erstellen des neuen Haltebereich. Mit diesem Cmdlet zurückgegebene Informationen enthält eine Liste der Benutzer, deren Postfächer und OneDrive for Business-Websites abgelegt wurden, festlegen möchten, und gibt an, ob die Sperre aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p121">**GetCaseHoldPolicy.txt** - Contains the output of the **Get-CaseHoldPolicy** cmdlet for the new hold, which the script ran after creating the new hold. The information returned by this cmdlet includes a list of users whose mailboxes and OneDrive for Business sites were placed on hold and whether the hold is enabled or disabled.</span></span> 
    
- <span data-ttu-id="d9ae7-p122">**GetCaseHoldRule.txt** - enthält die Ausgabe des Cmdlets **Get-CaseHoldRule** für den neuen Haltestatus, die das Skript ausgeführt wurde, nach dem Erstellen des neuen Haltebereich. Mit diesem Cmdlet zurückgegebene Informationen enthält die Suchabfrage, wenn Sie das Skript zum Erstellen eines Haltestatus abfragebasierter verwendet.</span><span class="sxs-lookup"><span data-stu-id="d9ae7-p122">**GetCaseHoldRule.txt** - Contains the output of the **Get-CaseHoldRule** cmdlet for the new hold, which the script ran after creating the new hold. The information returned by this cmdlet includes the search query if you used the script to create a query-based hold.</span></span> 
