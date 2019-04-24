---
title: Verwenden Sie die Inhaltssuche, um das Postfach und die OneDrive for Business-Website nach einer Liste mit Benutzern zu durchsuchen.
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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260933"
---
# <a name="use-content-search-to-search-the-mailbox-and-onedrive-for-business-site-for-a-list-of-users"></a>Verwenden Sie die Inhaltssuche, um das Postfach und die OneDrive for Business-Website nach einer Liste mit Benutzern zu durchsuchen.

Das Security & Compliance Center bietet eine Reihe von Windows PowerShell-Cmdlets, mit denen Sie zeitaufwändige eDiscovery-bezogene Aufgaben automatisieren können. Derzeit wird das Erstellen einer Inhaltssuche im Security & Compliance Center zum Durchsuchen einer Vielzahl von Speicherorten für Depot Inhalte Zeit und Vorbereitung benötigt. Bevor Sie eine Suche erstellen, müssen Sie die URL für jede OneDrive for Business-Website sammeln und dann jedes Postfach und jede neDrive for Business-Website zur Suche hinzufügen. In zukünftigen Versionen ist dies im Security & Compliance Center einfacher. Bis dahin können Sie dieses Verfahren mithilfe des Skripts in diesem Artikel automatisieren. Mit diesem Skript werden Sie aufgefordert, den Namen der mysite-Domäne Ihrer Organisation einzugeben (beispielsweise **contoso** in https://contoso-my.sharepoint.com)der URL, eine Liste der Benutzer-e-Mail-Adressen, den Namen der neuen Inhaltssuche und die zu verwendende Suchabfrage. Das Skript ruft die OneDrive for Business-URL für jeden Benutzer in der Liste ab und erstellt dann eine Inhaltssuche, die das Postfach und die OneDrive for Business-Website für jeden Benutzer in der Liste unter Verwendung der von Ihnen bereitgestellten Suchabfrage durchsucht. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen Mitglied der eDiscovery-Manager-Rollengruppe im Security & Compliance Center und ein globaler SharePoint Online-Administrator sein, um das Skript in Schritt 3 ausführen zu können.
    
- Stellen Sie sicher, dass Sie die Liste der Benutzer, die Sie in Schritt 2 erstellen, und das Skript in Schritt 3 in demselben Ordner speichern. Dadurch wird das Ausführen des Skripts vereinfacht.
    
- Das Skript enthält eine minimale Fehlerbehandlung. Der Hauptzweck besteht darin, die Mailbox und die OneDrive for Business-Website der einzelnen Benutzer schnell und einfach zu durchsuchen.
    
- Die in diesem Thema bereitgestellten Beispielskripts werden unter keinem Microsoft Standard-Support Programm oder-Dienst unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft lehnt alle i[https://go.microsoft.com/fwlink/p/?LinkId=517283](https://go.microsoft.com/fwlink/p/?LinkId=517283)mplied Garantien einschließlich, ohne Einschränkung, implizite Garantien der Marktgängigkeit oder der Eignung für einen bestimmten Zweck ab. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.
    
## <a name="step-1-install-the-sharepoint-online-management-shell"></a>Schritt 1: Installieren der SharePoint Online-Verwaltungsshell
<a name="step1"> </a>

Der erste Schritt besteht darin, die SharePoint Online-Verwaltungsshell zu installieren. Sie müssen die Shell nicht in diesem Verfahren verwenden, aber Sie müssen Sie installieren, da Sie die erforderlichen Voraussetzungen für das Skript enthält, das Sie in Schritt 3 ausführen. Diese Voraussetzungen ermöglichen es dem Skript, mit SharePoint Online zu kommunizieren, um die URLs für die OneDrive für Business-Websites abzurufen.
  
Wechseln Sie zu [Einrichten der Windows PowerShell-Umgebung für die SharePoint Online-Verwaltungsshell](https://go.microsoft.com/fwlink/p/?LinkID=286318) , und führen Sie Schritt 1 und Schritt 2 aus, um die SharePoint Online-Verwaltungsshell zu installieren.
  
## <a name="step-2-generate-a-list-of-users"></a>Schritt 2: Generieren einer Liste von Benutzern
<a name="step2"> </a>

Das Skript in Schritt 3 erstellt eine Inhaltssuche, um die Postfächer und OneDrive-Konten nach einer Liste von Benutzern zu durchsuchen. Sie können die e-Mail-Adressen einfach in eine Textdatei eingeben, oder Sie können einen Befehl in Windows PowerShell ausführen, um eine Liste der e-Mail-Adressen abzurufen und Sie in einer Datei zu speichern (im gleichen Ordner, in dem Sie das Skript in Schritt 3 speichern).
  
Hier ist ein [Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283) -Befehl, den Sie untersuchen können, um eine Liste der e-Mail-Adressen für alle Benutzer in Ihrer Organisation zu erhalten `Users.txt`und diese in einer Textdatei mit dem Namen zu speichern. 
  
```
Get-Mailbox -ResultSize unlimited -Filter { RecipientTypeDetails -eq 'UserMailbox'} | Select-Object PrimarySmtpAddress > Users.txt
```

Nachdem Sie diesen Befehl ausgeführt haben, müssen Sie die Datei öffnen und den Header entfernen, der den Eigenschaftennamen enthält `PrimarySmtpAddress`. Die Textdatei sollte nur eine Liste von e-Mail-Adressen enthalten, und nichts anderes. Stellen Sie sicher, dass vor oder nach der Liste der e-Mail-Adressen keine leeren Zeilen vorhanden sind.
  
## <a name="step-3-run-the-script-to-create-and-start-the-search"></a>Schritt 3: Ausführen des Skripts zum Erstellen und Starten der Suche

Wenn Sie das Skript in diesem Schritt ausführen, werden Sie aufgefordert, die folgenden Informationen einzugeben. Stellen Sie sicher, dass diese Informationen bereit sind, bevor Sie das Skript ausführen.
  
- **Ihre Benutzeranmeldeinformationen** – das Skript verwendet Ihre Anmeldeinformationen für den Zugriff auf SharePoint Online, um die OneDrive for Business-URLs abzurufen und eine Verbindung mit dem Security _AMP_ Compliance Center mit Remote-PowerShell herzustellen. 
    
- **Name der mysite-Domäne** -die Domäne mysite ist die Domäne, die alle OneDrive für Business-Websites in Ihrer Organisation enthält. Wenn beispielsweise die URL für Ihre Domäne "mysite" **https://contoso-my.sharepoint.com**lautet, geben Sie ein `contoso` , wenn Sie vom Skript aufgefordert werden, den Namen Ihrer Domäne "mysite" einzugeben. 
    
- **Pfadname der Textdatei aus Schritt 2** : der Pfadname der Textdatei, die Sie in Schritt 2 erstellt haben. Wenn sich die Textdatei und das Skript im gleichen Ordner befinden, geben Sie den Namen der Textdatei ein. Geben Sie andernfalls den vollständigen Pfadnamen für die Textdatei ein. 
    
- **Name der Inhaltssuche** – der Name der Inhaltssuche, die vom Skript erstellt wird. 
    
- **Suchabfrage** : die Suchabfrage, die mit der Inhaltssuche verwendet wird, wird erstellt und ausgeführt. Weitere Informationen zu Suchabfragen finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).


**So führen Sie das Skript aus:**
    
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `SearchEXOOD4B.ps1`. Speichern Sie die Datei in dem Ordner, in dem Sie die Liste der Benutzer in Schritt 2 gespeichert haben.
    
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

2. Öffnen Sie Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben, und in der Liste der Benutzer aus Schritt 2.
    
3. Starten Sie das Skript; Zum Beispiel:
    
    ```
    .\SearchEXOOD4B.ps1
    ```

4. Wenn Sie zur Eingabe Ihrer Anmeldeinformationen aufgefordert werden, geben Sie Ihre e-Mail-Adresse und Ihr Kennwort ein, und klicken Sie auf **OK**. 
    
5. Geben Sie die folgenden Informationen ein, wenn Sie vom Skript dazu aufgefordert werden. Geben Sie jede Information ein, und drücken **Sie die Eingabe**Taste.
    
    - Der Name der mysite-Domäne. 
    
    - Der Pfadname der Textdatei, die die Liste der Benutzer enthält.
    
    - Ein Name für die Inhaltssuche.
    
    - Die Suchabfrage (lassen Sie dieses Feld leer, um alle Elemente in den Inhaltsspeicherorten zurückzugeben).
    
    Das Skript ruft die URLs für jede OneDrive for Business-Website ab und erstellt und startet dann die Suche. Sie können entweder das Cmdlet **Get-ComplianceSearch** in Security _AMP_ Compliance Center PowerShell ausführen, um die Suchstatistiken und-Ergebnisse anzuzeigen, oder Sie können zur Seite " **Inhaltssuche** " im Security & Compliance Center wechseln, um Informationen anzuzeigen. über die Suche. 
