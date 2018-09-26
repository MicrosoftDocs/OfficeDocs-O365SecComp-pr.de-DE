---
title: Verwenden der Inhaltssuche zum Durchsuchen des Postfachs und der OneDrive for Business-Website nach einer Liste von Benutzern
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/3/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 5f4f8206-2d6a-4cb2-bbc6-7a0698703cc0
description: Verwenden Sie Inhaltssuche und das Skript in diesem Artikel, um Postfächer und OneDrive for Business-Websites für eine Gruppe von Benutzern zu suchen.
ms.openlocfilehash: e7f16ec0ca34d9f7f6155cab7e473119de3966cb
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038168"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a>Verwenden der Inhaltssuche zum Durchsuchen des Postfachs und der OneDrive for Business-Website nach einer Liste von Benutzern

Die Office 365-Sicherheit &amp; Compliance Center bietet eine Reihe von Windows PowerShell-Cmdlets, mit denen Sie zeitaufwendige eDiscovery-bezogene Aufgaben automatisieren können. Aktuell, eine Suche Inhalte erstellen, in das Wertpapier &amp; Compliance Center, um eine große Anzahl von Speicherorte für Inhalte Verwaltungsberechtigter suchen nimmt Zeit und Vorbereitung. Bevor Sie eine Suche erstellen, müssen Sie sammeln die URL für jede OneDrive for Business-Site und dann die Suche für jedes Postfach und O NeDrive für Business-Website hinzuzufügen. In zukünftigen Versionen werden einfacher in das Wertpapier &amp; Compliance Center. Bis zu diesem Zeitpunkt können Sie das Skript in diesem Artikel verwenden, um diese zu automatisieren. Mit diesem Skript werden Sie aufgefordert, den Namen des MeineWebsite-Domäne Ihrer Organisation (beispielsweise **"Contoso"** in der URL https://contoso-my.sharepoint.com), eine Liste von Benutzer-e-Mail-Adressen, den Namen der neuen Inhaltssuche und die Suchabfrage verwenden. Das Skript ruft die OneDrive for Business-URL für jeden Benutzer in der Liste, und klicken Sie dann wird erstellt und startet eine Inhaltssuche, das das Postfach durchsucht und OneDrive for Business-Site für jeden Benutzer in der Liste mit der Abfrage, die Sie bereitstellen. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center und ein globaler SharePoint Online-Administrator zum Ausführen des Skripts in Schritt 3.
    
- Achten Sie darauf, dass die Liste der Benutzer zu speichern, die Sie in Schritt2 und das Skript in Schritt 3 im gleichen Ordner erstellen. Die wird zum Ausführen des Skripts erleichtern.
    
- Das Skript enthält minimale Fehlerbehandlung. Der primäre Zweck ist schnell und einfach die Postfach- und OneDrive for Business-Website für jeden Benutzer suchen.
    
- In diesem Thema bereitgestellten Beispielskripts werden unter keinem standard Support-Programm von Microsoft oder der Dienst nicht unterstützt. Die Beispielskripts werden wie besehen ohne jede Gewährleistung bereitgestellt. Microsoft schließt alle ich[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)implizite Garantien einschließlich, aber nicht beschränkt auf alle konkludente Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck. Das gesamte Risiko aus der Verwendung oder der Leistung der Beispielskripts und der Dokumentation liegt bei Ihnen. In keinem Fall muss Microsoft, seine Autoren oder ein Benutzer die Erstellung, Produktion oder Übermittlung der Skripts else beteiligt für Schäden jeglicher Art (einschließlich, aber nicht beschränkt auf Schäden für den Verlust von Gewinn Business, Business Unterbrechung, Verlust von Unternehmensinformationen, Folge- oder) aus der Verwendung des oder der Fehler beim Verwenden der Beispielskripts oder der Dokumentation, haftbar gemacht werden, auch wenn Microsoft die Möglichkeit solcher Schäden hingewiesen wurde.
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Schritt 1: Installieren der SharePoint Online-Verwaltungsshell
<a name="step1"> </a>

Der erste Schritt besteht darin SharePoint Online-Verwaltungsshell zu installieren. Sie müssen zum Verwenden der Shell in diesem Verfahren, aber Sie installieren, da es enthält die erforderlichen Komponenten erforderlich, von dem Skript, das Sie in Schritt 3 ausführen müssen. Diese erforderlichen Komponenten ermöglichen das Skript zur Kommunikation mit SharePoint Online, um die URLs für die OneDrive for Business-Websites erhalten.
  
Wechseln Sie zum [Einrichten von SharePoint Online-Verwaltungsshell Windows PowerShell--Umgebung](https://go.microsoft.com/fwlink/p/?LinkID=286318) , und führen Sie Schritt 1 und Schritt2, um die SharePoint Online-Verwaltungsshell zu installieren.
  
## <a name="step-2-generate-a-list-of-users"></a>Schritt 2: Eine Liste der Benutzer generieren
<a name="step2"> </a>

Das Skript in Schritt 3 erstellt eine Inhaltssuche, um die Postfächer und OneDrive-Konten für eine Liste von Benutzern zu suchen. Sie können nur die e-Mail-Adressen in einer Textdatei eingeben, oder führen Sie einen Befehl in Windows PowerShell zum Abrufen einer Liste von e-Mail-Adressen und diese in einer Datei (befindet sich in demselben Ordner, den Sie das Skript in Schritt 3 sparen) speichern.
  
Hier ist ein [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) -Befehl, können Sie zum Abrufen einer Liste von e-Mail-Adressen für alle Benutzer in Ihrer Organisation, und speichern Sie eine Textdatei mit dem Namen Runt `Users.txt`. 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

Nachdem Sie diesen Befehl ausführen, müssen Sie unbedingt öffnen Sie die Datei, und Entfernen des Headers, der Name der Eigenschaft enthält `PrimarySmtpAddress`. Die Datei sollte nur eine Liste der e-Mail-Adressen und nichts anderes enthalten. Stellen Sie sicher, dass keine leeren Zeilen vor oder nach der Liste der e-Mail-Adressen vorhanden sind.
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a>Schritt 3: Ausführen des Skripts zum Erstellen und starten Sie die Suche

Wenn Sie das Skript in diesem Schritt ausführen, fordert es Sie für die folgenden Informationen. Achten Sie darauf, dass Sie diese Informationen bereit, bevor Sie das Skript ausgeführt haben.
  
- **Ihre Anmeldeinformationen** – das Skript wird unter Verwendung Ihrer Anmeldeinformationen für den Zugriff von SharePoint Online, die OneDrive for Business-URLs abgerufen und die Verbindung für die Sicherheit auf &amp; Compliance Center mit remote-PowerShell. 
    
- **Namen der Domäne MeineWebsite** - MeineWebsite der Domäne ist die Domäne, die alle die OneDrive for Business-Websites in Ihrer Organisation enthält. Beispielsweise ist die URL für Ihre Domäne MySite **https://contoso-my.sharepoint.com**, und klicken Sie dann Eingabe der `contoso` Wenn des Skripts aufgefordert, den Namen Ihrer Domäne MySite. 
    
- **Pfadname der Textdatei aus Schritt2** – der Pfadname der Textdatei, die Sie in Schritt2 erstellt haben. Wenn die Textdatei und das Skript im selben Ordner gespeichert sind, geben Sie den Namen der Textdatei. Geben Sie andernfalls den vollständigen Pfadnamen für die Textdatei. 
    
- **Name der Content Suche** – den Namen des Content-Suche, die von dem Skript erstellt werden. 
    
- **Suchabfrage** - Search-Abfrage, die für die Inhaltssuche verwendet wird erstellt und ausgeführt. Weitere Informationen zu Suchabfragen finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md).


**Ausführen des Skripts:**
    
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `SearchEXOOD4B.ps1`. Speichern Sie die Datei im gleichen Ordner, in dem Sie die Liste der Benutzer in Schritt2 gespeichert haben.
    
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

2. Öffnen Sie Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript und die Liste der Benutzer aus Schritt2 gespeichert.
    
3. Starten Sie das Skript. Zum Beispiel:
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. Geben Sie nach Ihren Anmeldeinformationen gefragt Ihre e-Mail-Adresse und das Kennwort ein, und klicken Sie dann auf **OK**. 
    
5. Geben Sie den folgenden Informationen bei entsprechender Aufforderung durch das Skript. Geben Sie jede Informationseinheit, und drücken Sie dann die **EINGABETASTE**.
    
    - Der Name der Domäne MySite. 
    
    - Der Pfadname der Textdatei, die die Liste der Benutzer enthält.
    
    - Ein Name für die Inhaltssuche.
    
    - Die Suchabfrage (diesem leer lassen alle Elemente in der Speicherorte für Inhalte zurückgeben).
    
    Das Skript ruft die URLs für jede OneDrive for Business-Site, und klicken Sie dann erstellt und startet die Suche. Sie können entweder mit dem Cmdlet **Get-ComplianceSearch** ausführen, in Sicherheit und Compliance Center PowerShell der Suchstatistik und das Ergebnis angezeigt, oder Sie können wechseln Sie zur Seite **Inhaltssuche** in das Wertpapier &amp; Compliance Center anzeigen Informationen über die Suche. 
