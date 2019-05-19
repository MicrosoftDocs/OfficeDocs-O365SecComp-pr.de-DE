---
title: Verwenden eines Skripts zum Hinzufügen von Benutzern zu einem Haltestatus in einem eDiscovery-Fall im Security & Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/23/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
ms.assetid: bad352ff-d5d2-45d8-ac2a-6cb832f10e73
description: Ausführen eines Skripts zum schnellen Hinzufügen von Postfächern und OneDrive für Unternehmen Websites zu einem neuen Haltestatus, der einem eDiscovery-Fall im Security & Compliance Center zugeordnet ist.
ms.openlocfilehash: c680e584a6f729b3d6d0d74b84ddd0e03da6dc9a
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156227"
---
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-security--compliance-center"></a>Verwenden eines Skripts zum Hinzufügen von Benutzern zu einem Haltestatus in einem eDiscovery-Fall im Security & Compliance Center

Das Security & Compliance Center bietet viele Windows PowerShell-Cmdlets, mit denen Sie zeitaufwändige Aufgaben im Zusammenhang mit dem Erstellen und Verwalten von eDiscovery-Fällen automatisieren können. Mit dem eDiscovery Case-Tool im Security & Compliance Center können Sie derzeit eine große Anzahl von Speicherorten für Depot Inhalte Zeit-und Vorbereitungs bereitstellen. Vor dem Erstellen eines Haltestatus müssen Sie beispielsweise die URL für jede OneDrive für Unternehmen Website erfassen, die Sie in die Warteschleife stellen möchten. Anschließend müssen Sie für jeden Benutzer, den Sie in die Warteschleife setzen möchten, das Postfach und die OneDrive für Unternehmen Website in das Archiv eintragen. In zukünftigen Versionen des Security & Compliance Center wird dies einfacher. Bis dahin können Sie das Skript in diesem Artikel verwenden, um diesen Prozess zu automatisieren.
  
Im Skript werden Sie zur Angabe des Namens der mysite-Domäne Ihrer Organisation aufgefordert (beispielsweise " **contoso** " https://contoso-my.sharepoint.com)in der URL, der Name eines vorhandenen eDiscovery-Falls, der Name des neuen haltebereichs, der dem Fall zugeordnet ist, eine Liste der e-Mail-Adressen der gewünschten Benutzer zum Anhalten und eine Suchabfrage, die verwendet werden soll, wenn Sie einen abfragebasierten Haltebereich erstellen möchten. Das Skript ruft dann die URL für die OneDrive für Unternehmen Website für jeden Benutzer in der Liste ab, erstellt den neuen Haltestatus und fügt dann das Postfach und die OneDrive für Unternehmen Website für jeden Benutzer in der Liste in den Haltebereich ein. Das Skript generiert auch Protokolldateien, die Informationen zum neuen Haltestatus enthalten. 
  
Hier sind die Schritte, um dies zu erreichen:
  
[Schritt 1: Installieren der SharePoint Online-Verwaltungsshell](#step-1-install-the-sharepoint-online-management-shell)
  
[Schritt 2: Generieren einer Liste von Benutzern](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[Schritt 3: Ausführen des Skripts zum Erstellen eines Haltestatus und Hinzufügen von Benutzern](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen Mitglied der Rollengruppe "eDiscovery-Manager" im Security & Compliance Center und ein SharePoint Online globaler Administrator sein, um das Skript in Schritt 3 auszuführen. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Office 365 Security & Compliance Center](assign-ediscovery-permissions.md).
    
- Es können maximal 1.000 Postfächer und 100-Websites zu einem Haltestatus hinzugefügt werden, der einem eDiscovery-Fall im Security & Compliance Center zugeordnet ist. Wenn Sie davon ausgehen, dass jeder Benutzer, den Sie in der Warteschleife platzieren möchten, über eine OneDrive für Unternehmen Website verfügt, können Sie mithilfe des Skripts in diesem Artikel maximal 100 Benutzer zu einem Haltestatus hinzufügen. 
    
- Achten Sie darauf, dass Sie die Liste der Benutzer, die Sie in Schritt 2 und das Skript in Schritt 3 erstellen, in demselben Ordner speichern. Dadurch wird das Ausführen des Skripts vereinfacht.
    
- Das Skript fügt die Liste der Benutzer zu einem neuen Haltestatus hinzu, der einem vorhandenen Fall zugeordnet ist. Stellen Sie sicher, dass der Fall, dem Sie den Haltebereich zuordnen möchten, erstellt wird, bevor Sie das Skript ausführen.
    
- Das Skript enthält eine minimale Fehlerbehandlung. Der primäre Zweck besteht darin, das Postfach und die OneDrive für Unternehmen Website jedes Benutzers schnell und einfach aufzubewahren.
    
- Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.

## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Schritt 1: Installieren der SharePoint Online-Verwaltungsshell

Der erste Schritt besteht darin, die SharePoint Online-Verwaltungsshell zu installieren, falls Sie noch nicht auf Ihrem lokalen Computer installiert ist. Sie müssen die Shell in diesem Verfahren nicht verwenden, aber Sie müssen Sie installieren, da Sie Voraussetzungen enthält, die für das in Schritt 3 ausgeführte Skript erforderlich sind. Diese Voraussetzungen ermöglichen es dem Skript, mit SharePoint Online zu kommunizieren, um die URLs für die OneDrive für Unternehmen Websites abzurufen.
  
Wechseln Sie zum [Einrichten der SharePoint Online Verwaltungsshell Windows PowerShell Umgebung](https://go.microsoft.com/fwlink/p/?LinkID=286318) , und führen Sie Schritt 1 und Schritt 2 aus, um die SharePoint Online-Verwaltungsshell auf dem lokalen Computer zu installieren. 

## <a name="step-2-generate-a-list-of-users"></a>Schritt 2: Generieren einer Liste von Benutzern
<a name="step2"> </a>

Mit dem Skript in Schritt 3 wird ein Haltestatus erstellt, der einem eDiscovery-Fall zugeordnet ist, sowie das Hinzufügen der Postfächer und OneDrive für Unternehmen Websites einer Liste von Benutzern in den Haltebereich. Sie können die e-Mail-Adressen einfach in eine Textdatei eingeben oder einen Befehl in Windows PowerShell ausführen, um eine Liste mit e-Mail-Adressen zu erhalten und diese in einer Datei zu speichern (in demselben Ordner, in dem Sie das Skript in Schritt 3 speichern werden).
  
Es folgt ein PowerShell-Befehl (den Sie mit der Remote-PowerShell ausführen, die mit Ihrer Exchange Online Organisation verbunden ist), um eine Liste der e-Mail-Adressen für alle Benutzer in Ihrer Organisation abzurufen und in einer Textdatei mit dem Namen "HoldUsers. txt" zu speichern.
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

Nachdem Sie diesen Befehl ausgeführt haben, öffnen Sie die Textdatei, und entfernen Sie die Kopfzeile, die `PrimarySmtpAddress`den Eigenschaftennamen enthält. Entfernen Sie dann alle e-Mail-Adressen außer denjenigen für die Benutzer, die Sie dem Haltestatus hinzufügen möchten, den Sie in Schritt 3 erstellen. Stellen Sie sicher, dass keine leeren Zeilen vor oder nach der Liste der e-Mail-Adressen vorhanden sind.
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a>Schritt 3: Ausführen des Skripts zum Erstellen eines Haltestatus und Hinzufügen von Benutzern
<a name="step3"> </a>

Wenn Sie das Skript in diesem Schritt ausführen, werden Sie aufgefordert, die folgenden Informationen einzugeben. Stellen Sie sicher, dass diese Informationen vor dem Ausführen des Skripts verfügbar sind.
  
- **Ihre Benutzeranmeldeinformationen** – das Skript verwendet Ihre Anmeldeinformationen, um eine Verbindung mit dem Security & Compliance Center mit Remote-PowerShell herzustellen. Außerdem werden diese Anmeldeinformationen für den Zugriff auf SharePoint Online verwendet, um die OneDrive für Unternehmen-URLs für die Liste der Benutzer abzurufen.
    
- **Name Ihrer mysite-Domäne** : die mysite-Domäne ist die Domäne, die alle OneDrive für Unternehmen Websites in Ihrer Organisation enthält. Wenn beispielsweise die URL für Ihre mysite-Domäne lautet **https://contoso-my.sharepoint.com**, geben `contoso` Sie ein, wenn Sie vom Skript nach dem Namen Ihrer mysite-Domäne gefragt werden. 
    
- **Name der Groß-/Kleinschreibung** -der Name eines vorhandenen Falls. Mit dem Skript wird ein neuer Haltebereich erstellt, der diesem Fall zugeordnet ist.
    
- **Name des Haltestatus** -der Name des haltebereichs, der vom Skript erstellt und mit dem angegebenen Fall verknüpft wird.
    
- **Suchabfrage für einen abfragebasierten halte** Status-Sie können einen abfragebasierten Speicher erstellen, sodass nur der Inhalt, der die angegebenen Suchkriterien erfüllt, in der Warteschleife gespeichert wird. Um den gesamten Inhalt aufzubewahren, drücken Sie die **EINGABETASTE** , wenn Sie zur Eingabe einer Suchabfrage aufgefordert werden. 
    
- Gibt an, ob das Skript aktiviert **werden soll oder nicht,** nachdem es erstellt wurde, oder wenn das Skript den Haltebereich erstellen kann, ohne es zu aktivieren. Wenn das Skript nicht aktiviert ist, können Sie es später im Security & Compliance Center oder durch Ausführen der folgenden PowerShell-Befehle aktivieren: 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- **Name der Textdatei mit der Liste der Benutzer** -der Name der Textdatei aus Schritt 2, die die Liste der Benutzer enthält, die dem Haltestatus hinzugefügt werden sollen. Wenn sich diese Datei im gleichen Ordner wie das Skript befindet, geben Sie einfach den Namen der Datei ein (beispielsweise "HoldUsers. txt"). Wenn sich die Textdatei in einem anderen Ordner befindet, geben Sie den vollständigen Pfadnamen der Datei ein.
    
Nachdem Sie die Informationen gesammelt haben, für die das Skript Sie auffordert, besteht der letzte Schritt darin, das Skript auszuführen, um den neuen Haltestatus zu erstellen und ihm Benutzer hinzuzufügen.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell Skriptdatei unter Verwendung eines filename-Suffixes von. ps1; Beispiel: `AddUsersToHold.ps1`.
    
  ```
  #script begin
  " " 
  write-host "***********************************************"
  write-host "   Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery cases - Add users to a hold   " -foregroundColor yellow -backgroundcolor darkgreen 
  write-host "***********************************************"
  " " 
  # Get user credentials &amp; Connect to Office 365 SCC, SPO
  $credentials = Get-Credential -Message "Specify your credentials to connect to the Security & Compliance Center and SharePoint Online"
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

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.
    
3. Ausführen des Skripts; Zum Beispiel:
    
      ```
    .\AddUsersToHold.ps1
      ```

4. Geben Sie die Informationen ein, die Sie vom Skript angefordert haben.
    
    Das Skript stellt eine Verbindung mit der Security & Compliance Center PowerShell her und erstellt dann den neuen Haltebereich im eDiscovery-Fall und fügt die Postfächer und die OneDrive für Unternehmen für die Benutzer in der Liste hinzu. Sie können den Fall auf der **eDiscovery** -Seite im Security & Compliance Center aufrufen, um den neuen Haltestatus anzuzeigen. 
    
Nachdem das Skript ausgeführt wurde, werden die folgenden Protokolldateien erstellt und in dem Ordner gespeichert, in dem sich das Skript befindet.
  
- **LocationsOnHold. txt** – enthält eine Liste von Postfächern und OneDrive für Unternehmen Websites, die vom Skript erfolgreich gespeichert wurden.
    
- **LocationsNotOnHold. txt** – enthält eine Liste von Postfächern und OneDrive für Unternehmen Websites, die das Skript nicht in der Warteschleife aufbewahren konnte. Wenn ein Benutzer über ein Postfach verfügt, jedoch nicht über einen OneDrive für Unternehmen-Standort, wird der Benutzer in die Liste der OneDrive für Unternehmen-Websites aufgenommen, die nicht in der Warteschleife gespeichert wurden.
    
- **GetCaseHoldPolicy. txt** – enthält die Ausgabe des Cmdlets **Get-CaseHoldPolicy** für den neuen Haltestatus, den das Skript nach dem Erstellen des neuen Haltestatus ausgeführt hat. Die Informationen, die von diesem Cmdlet zurückgegeben werden, umfassen eine Liste der Benutzer, deren Postfächer und OneDrive für Unternehmen Websites gespeichert wurden, und ob der Haltebereich aktiviert oder deaktiviert ist. 
    
- **GetCaseHoldRule. txt** – enthält die Ausgabe des Cmdlets **Get-CaseHoldRule** für den neuen Haltestatus, den das Skript nach dem Erstellen des neuen Haltestatus ausgeführt hat. Die Informationen, die von diesem Cmdlet zurückgegeben werden, enthalten die Suchabfrage, wenn Sie das Skript zum Erstellen eines abfragebasierten haltebereichs verwendet haben. 
