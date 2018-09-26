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
# <a name="use-a-script-to-add-users-to-a-hold-in-an-ediscovery-case-in-the-office-365-security-amp-compliance-center"></a>Verwenden Sie ein Skript zum Hinzufügen von Benutzern zu einem Haltestatus in einer eDiscovery-Fall in die Office 365-Sicherheit &amp; Compliance Center

Die Office 365-Sicherheit &amp; Compliance Center bietet viele der Windows PowerShell-Cmdlets, mit denen Sie automatisieren zeitaufwändige Aufgaben im Zusammenhang mit erstellen und Verwalten von eDiscovery-Fälle. Verwenden Sie das Groß-/Kleinschreibung eDiscovery-Tool derzeit in die Sicherheit &amp; Compliance Center, um eine große Anzahl von Verwaltungsberechtigten Speicherorte für Inhalte in die Warteschleife stellen nimmt Zeit und Vorbereitung. Bevor Sie einen Haltestatus erstellen, müssen Sie beispielsweise die URL für jede OneDrive for Business-Website zu erfassen, die Sie in die Warteschleife stellen möchten. Für jeden Benutzer, den Sie in die Warteschleife stellen möchten, müssen Sie dann ihr Postfach und ihre OneDrive for Business-Site dem Haltestatus hinzufügen. In zukünftigen Versionen des Wertpapiers &amp; Compliance Center, dies wird einfacher abrufen. Bis zu diesem Zeitpunkt können Sie das Skript in diesem Artikel verwenden, um diese zu automatisieren.
  
Das Skript werden Sie aufgefordert, den Namen des MeineWebsite-Domäne Ihrer Organisation (beispielsweise **"Contoso"** in der URL https://contoso-my.sharepoint.com), den Namen eines vorhandenen eDiscovery-Fall, den Namen des neuen Haltestatus, die dem Fall zugeordneten, eine Liste von e-Mail-Adressen der Benutzer Sie benötigen Platzieren Sie auf halten und eine Suchabfrage verwenden, wenn Sie eine abfragebasierte Aufbewahrung erstellen möchten. Das Skript ruft dann die URL für die OneDrive for Business-Site für jeden Benutzer in der Liste, den neuen Haltebereich erstellt und dann hinzugefügt für das Postfach und OneDrive for Business-Site für jeden Benutzer in der Liste den Haltestatus. Das Skript generiert auch Protokolldateien, die Informationen zu den neuen Haltestatus enthalten. 
  
Hier sind die Schritte zu diesem Zweck müssen:
  
[Schritt 1: Installieren der SharePoint Online-Verwaltungsshell](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step1)
  
[Schritt 2: Eine Liste der Benutzer generieren](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step2)
  
[Schritt 3: Ausführen des Skripts zum Erstellen eines Haltestatus und Hinzufügen von Benutzern](use-a-script-to-add-users-to-a-hold-in-ediscovery.md#step3)
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center und ein globaler SharePoint Online-Administrator zum Ausführen des Skripts in Schritt 3. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
    
- Maximal 1.000 Postfächer und 100 Websites zu einem Haltestatus, die einem eDiscovery-Fall in das Wertpapier zugeordnet wurde hinzugefügt werden kann &amp; Compliance Center. Unter der Annahme, dass alle Benutzer, die Sie in die Warteschleife stellen möchten ein OneDrive for Business-Website verfügt, können Sie maximal 100 Benutzer zu einem Haltestatus mithilfe des Skripts in diesem Artikel hinzufügen. 
    
- Achten Sie darauf, dass die Liste der Benutzer zu speichern, die Sie in Schritt2 und das Skript in Schritt 3 im gleichen Ordner erstellen. Die wird zum Ausführen des Skripts erleichtern.
    
- Das Skript fügt die Liste der Benutzer zu einem neuen Haltestatus, der eine vorhandene Anfrage zugeordnet ist. Stellen Sie sicher, dass die Groß-/Kleinschreibung, der Sie den Haltestatus mit zuordnen möchten erstellt wird, bevor Sie das Skript ausführen.
    
- Das Skript enthält minimale Fehlerbehandlung. Der primäre Zweck ist, um schnell und einfach das Postfach zu platzieren, und halten Sie OneDrive for Business-Website für jeden Benutzer.
    
- Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.

## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Schritt 1: Installieren der SharePoint Online-Verwaltungsshell

Der erste Schritt besteht, die SharePoint Online-Verwaltungsshell zu installieren, wenn es nicht bereits auf dem lokalen Computer installiert ist. Sie müssen zum Verwenden der Shell in diesem Verfahren, aber Sie installieren, da es enthält die erforderlichen Komponenten erforderlich, von dem Skript, das Sie in Schritt 3 ausführen müssen. Diese erforderlichen Komponenten ermöglichen das Skript zur Kommunikation mit SharePoint Online, um die URLs für die OneDrive for Business-Websites erhalten.
  
Wechseln Sie zum [Einrichten von SharePoint Online-Verwaltungsshell Windows PowerShell--Umgebung](https://go.microsoft.com/fwlink/p/?LinkID=286318) , und führen Sie Schritt 1 und Schritt2, um die SharePoint Online-Verwaltungsshell auf dem lokalen Computer zu installieren. 

## <a name="step-2-generate-a-list-of-users"></a>Schritt 2: Eine Liste der Benutzer generieren
<a name="step2"> </a>

Das Skript in Schritt 3 wird das Erstellen eines Haltestatus, das mit einem eDiscovery-Fall und Hinzufügen der Postfächer und OneDrive für Websites mit Geschäftsdaten aus einer Liste von Benutzern, die Sperre zugeordnet ist. Sie können nur die e-Mail-Adressen in einer Textdatei eingeben, oder führen Sie einen Befehl in Windows PowerShell zum Abrufen einer Liste von e-Mail-Adressen und diese in einer Datei (befindet sich in demselben Ordner, den Sie das Skript in Schritt 3 sparen) speichern.
  
Nachfolgend finden Sie ein PowerShell-Befehl (, die Sie ausführen, mithilfe von remote-PowerShell mit Ihrer Exchange Online-Organisation verbunden ist) zum Abrufen einer Liste von e-Mail-Adressen für alle Benutzer in Ihrer Organisation, und speichern Sie eine Textdatei mit dem Namen HoldUsers.txt.
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > HoldUsers.txt
```

Nachdem Sie führen Sie diesen Befehl, öffnen Sie die Textdatei und den Header entfernen, der Name der Eigenschaft enthält `PrimarySmtpAddress`. Entfernen Sie alle e-Mail-Adressen außer derjenigen, die für die Benutzer, die Sie dem Haltestatus hinzufügen, die Sie in Schritt 3 erstellen, möchten. Stellen Sie sicher, dass keine leeren Zeilen vor oder nach der Liste der e-Mail-Adressen vorhanden sind.
  

  
## <a name="step-3-run-the-script-to-create-a-hold-and-add-users"></a>Schritt 3: Ausführen des Skripts zum Erstellen eines Haltestatus und Hinzufügen von Benutzern
<a name="step3"> </a>

Wenn Sie das Skript in diesem Schritt ausführen, fordert es Sie für die folgenden Informationen. Achten Sie darauf, dass Sie diese Informationen bereit, bevor Sie das Skript ausgeführt haben.
  
- **Ihre Anmeldeinformationen** – das Skript wird unter Verwendung Ihrer Anmeldeinformationen für die Verbindung für die Sicherheit &amp; Compliance Center mit remote-PowerShell. Es wird auch diese Anmeldeinformationen verwenden, um SharePoint Online, um die OneDrive for Business-URLs für die Liste der Benutzer abrufen zuzugreifen.
    
- **Namen der Domäne MeineWebsite** - MeineWebsite der Domäne ist die Domäne, die alle die OneDrive for Business-Websites in Ihrer Organisation enthält. Beispielsweise ist die URL für Ihre Domäne MySite **https://contoso-my.sharepoint.com**, und klicken Sie dann Eingabe der `contoso` Wenn des Skripts aufgefordert, den Namen Ihrer Domäne MySite. 
    
- Der **Name der Anfrage** – den Namen einer vorhandenen Anfrage. Das Skript erstellt einen neuen Haltestatus, der in diesem Fall zugeordnet ist.
    
- **Name des Haltestatus** – der Name des Haltestatus das Skript erstellen und Zuordnen der angegebenen Groß-/Kleinschreibung.
    
- **Halten Sie Search-Abfrage für ein abfragebasiertes** - Sie können eine abfragebasierte Aufbewahrung erstellen, sodass nur die Inhalte, die die angegebenen Suchkriterien erfüllt in die Warteschleife gestellt wird. Um den gesamten Inhalt im Archiv zu platzieren, drücken Sie die **EINGABETASTE** , wenn Sie für eine Suchabfrage aufgefordert werden. 
    
- **Ob Sie die Sperre aktivieren** - können Sie das Skript den Haltestatus einschalten, nachdem er erstellt wird oder Sie können das Skript den Haltestatus erstellen, ohne zu aktivieren. Wenn Sie nicht über das Skript die Sperre aktivieren verfügen, können Sie es auf aktivieren, weiter unten in der Sicherheit &amp; Compliance Center oder indem Sie die folgenden PowerShell-Befehle ausführen: 
    
  ```
  Set-CaseHoldPolicy -Identity <name of the hold> -Enabled $true
  ```

  ```
  Set-CaseHoldRule -Identity <name of the hold> -Disabled $false
  ```

- Der **Name der Textdatei mit der Liste der Benutzer** – den Namen der Textdatei aus Schritt2 mit der Liste der Benutzer dem Haltestatus hinzufügen. Wenn diese Datei im selben Ordner wie das Skript gespeichert ist, geben Sie einfach den Namen der Datei (beispielsweise HoldUsers.txt). Wenn die Textdatei in einen anderen Ordner befindet, geben Sie den vollständigen Pfadnamen der Datei.
    
Nachdem Sie die Informationen gesammelt haben, der das Skript für aufgefordert werden, ist der letzte Schritt zum Ausführen des Skripts zum Erstellen des neuen Haltebereich und Benutzer hinzuzufügen.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `AddUsersToHold.ps1`.
    
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

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.
    
3. Führen Sie das Skript; Zum Beispiel:
    
      ```
    .\AddUsersToHold.ps1
      ```

4. Geben Sie die Informationen, der das Skript für aufgefordert werden.
    
    Das Skript stellt eine Verbindung zur Sicherheit und Compliance Center PowerShell, und klicken Sie dann erstellt die neue Warteschleife in der eDiscovery-Fall und die Postfächer und OneDrive für Unternehmen für die Benutzer in der Liste hinzugefügt. Sie können die Groß-/Kleinschreibung auf der Seite **eDiscovery** in das Wertpapier wechseln &amp; Compliance Center, um den neuen Haltestatus anzuzeigen. 
    
Nach Abschluss des Skripts ausgeführt, es werden die folgenden Protokolldateien erstellt und speichert sie in den Ordner, der das Skript gespeichert ist.
  
- **LocationsOnHold.txt** - enthält eine Liste der Postfächer und OneDrive für Websites mit Geschäftsdaten, die das Skript erfolgreich auf platziert enthalten sein.
    
- **LocationsNotOnHold.txt** - enthält eine Liste der Postfächer und OneDrive for Business-Websites, die das Skript nicht in die Warteschleife stellen. Wenn ein Benutzer ein Postfach, aber keiner OneDrive for Business-Website verfügt, würde der Benutzer in der Liste der OneDrive for Business-Websites in die Warteschleife gestellt wurden nicht enthalten.
    
- **GetCaseHoldPolicy.txt** - enthält die Ausgabe des Cmdlets **Get-CaseHoldPolicy** für den neuen Haltestatus, die das Skript ausgeführt wurde, nach dem Erstellen des neuen Haltebereich. Mit diesem Cmdlet zurückgegebene Informationen enthält eine Liste der Benutzer, deren Postfächer und OneDrive for Business-Websites abgelegt wurden, festlegen möchten, und gibt an, ob die Sperre aktiviert oder deaktiviert ist. 
    
- **GetCaseHoldRule.txt** - enthält die Ausgabe des Cmdlets **Get-CaseHoldRule** für den neuen Haltestatus, die das Skript ausgeführt wurde, nach dem Erstellen des neuen Haltebereich. Mit diesem Cmdlet zurückgegebene Informationen enthält die Suchabfrage, wenn Sie das Skript zum Erstellen eines Haltestatus abfragebasierter verwendet. 
