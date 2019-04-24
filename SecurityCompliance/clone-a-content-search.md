---
title: Klonen einer Inhaltssuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Verwenden Sie das Windows PowerShell-Skript in diesem Artikel, um eine vorhandene Inhaltssuche im Compliance Center in Office 365 oder Microsoft 365 schnell zu klonen. Wenn Sie eine Suche Klonen, wird eine neue Suche (mit einem neuen Namen) erstellt, die die gleichen Eigenschaften wie die ursprüngliche Suche enthält. Dann können Sie die neue Suche bearbeiten (indem Sie die Stichwortabfrage oder den Datumszeitraum ändern) und dann ausführen.
ms.openlocfilehash: b08ccb6fbaf2dc9d92e0814fe9f92ea77c731147
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243346"
---
# <a name="clone-a-content-search"></a>Klonen einer Inhaltssuche

Das Erstellen einer Inhaltssuche im Compliance Center in Office 365 oder Microsoft 365, die eine Vielzahl von Postfächern oder SharePoint-und OneDrive für Business-Websites durchsucht, kann eine Weile dauern. Das Angeben der zu durchsuchenden Websites kann auch fehleranfällig sein, wenn Sie eine URL-Adresse nicht mehr eingeben. Um diese Probleme zu vermeiden, können Sie das Windows PowerShell-Skript in diesem Artikel verwenden, um eine vorhandene Inhaltssuche schnell zu klonen. Wenn Sie eine Suche Klonen, wird eine neue Suche (mit einem anderen Namen) erstellt, die die gleichen Eigenschaften (wie die inhaltsspeicherorte und die Suchabfrage) als ursprüngliche Suche enthält. Dann können Sie die neue Suche bearbeiten (indem Sie die Stichwortabfrage oder den Datumszeitraum ändern) und ausführen.
  
Gründe für das Klonen von Inhalts suchen
  
- Zum Vergleichen der Ergebnisse unterschiedlicher Keyword-Suchabfragen, die an denselben Inhaltsspeicherorten ausgeführt werden.
    
- Sie müssen beim Erstellen einer neuen Suche eine Vielzahl von Inhaltsspeicherorten erneut eingeben.
    
- So verringern Sie die Größe der Suchergebnisse Wenn Sie beispielsweise eine Suche haben, die zu viele Ergebnisse zum Exportieren zurückgibt, können Sie die Suche Klonen und dann eine Suchbedingung basierend auf einem Datumsbereich hinzufügen, um die Anzahl der Suchergebnisse zu reduzieren.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen Mitglied der eDiscovery-Manager-Rollengruppe im Security & Compliance Center sein, um das in diesem Thema beschriebene Skript ausführen zu können.
    
- Das Skript enthält eine minimale Fehlerbehandlung. Der Hauptzweck des Skripts besteht darin, eine Inhaltssuche schnell zu klonen.
    
- Das Skript erstellt eine neue Inhaltssuche, startet Sie jedoch nicht.
    
- Dieses Skript berücksichtigt, ob die Inhaltssuche, die Sie Klonen, einem eDiscovery-Fall zugeordnet ist. Wenn die Suche mit einem Fall verknüpft ist, wird die neue Suche auch mit dem gleichen Fall verknüpft. Wenn die vorhandene Suche keinem Fall zugeordnet ist, wird die neue Suche auf der Seite " **Inhaltssuche** " im Compliance Center aufgeführt. 
    
- Das Beispielskript in diesem Thema wird unter keinem Microsoft Standard-Support Programm oder-Dienst unterstützt. Das Beispielskript wird ohne Gewähr bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Das gesamte Risiko, das sich aus der Verwendung oder Leistung des Beispielskripts und der Dokumentation ergibt, liegt bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.
  
## <a name="step-1-run-the-script-to-clone-a-search"></a>Schritt 1: Ausführen des Skripts zum Klonen einer Suche

Mit dem Skript in diesem Schritt wird eine neue Inhaltssuche erstellt, indem eine vorhandene geklont wird. Wenn Sie dieses Skript ausführen, werden Sie aufgefordert, die folgenden Informationen einzugeben:
  
- **Ihre Benutzeranmeldeinformationen** – das Skript verwendet Ihre Anmeldeinformationen zum Herstellen einer Verbindung mit dem Security _AMP_ Compliance Center für ihre Office 365-Organisation mit Windows PowerShell. Wie bereits erwähnt, müssen Sie ein Mitglied der eDiscovery-Manager-Rollengruppe im Security & compCompliance Center sein, um das Skript auszuführen. 
    
- **Der Name der vorhandenen Suche** – hierbei handelt es sich um die Inhaltssuche, die Sie klonen möchten. 
    
- **Der Name der neuen Suche, die erstellt wird** -Wenn Sie diesen Wert leer lassen, erstellt das Skript einen Namen für die neue Suche, der auf dem Namen der zu klonenden Suche basiert. 
    
So Klonen Sie eine Suche:
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `CloneSearch.ps1`.
    
  ```
  # This PowerShell script clones an existing Content Search in the Office 365 security and compliance center.
  # Get login credentials from the user
  if(!$UserCredential)
  {
      $UserCredential = Get-Credential
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection
      if (!$Session)
      {
          Write-Error "Couldn't create a remote PowerShell session."
          return
      }
      Import-PSSession $Session -AllowClobber -DisableNameChecking
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Security & Compliance Center)"
  }
  # Ask for the name of the search you want to clone
  $searchName = Read-Host 'Enter the name of the search that you want to clone'
  # Ask for the name of the new search
  $newSearchName = Read-Host 'Enter a name for the new search [leave blank to automatically generate a name]'
  $originalSearch = Get-ComplianceSearch $searchName -EA SilentlyContinue
  # Make sure we have a valid search before continuing
  if(!$originalSearch)
  {
      Write-Error "Couldn't find search: $searchName"
      return
  }
  $searchNameCounter = 1
  # Find a suitable name for the new search
  while(!$newSearchName)
  {
      $newSearchName = $originalSearch.Name + "_" + $searchNameCounter
      $tempSearch = Get-ComplianceSearch $newSearchName -EA SilentlyContinue
      if ($tempSearch)
      {
          $newSearchName = $null
          $searchNameCounter++
      }
  }
  $caseName
  # Determine if the search is part of a case; if so get the case name
  if ($originalSearch.CaseId)
  {
      $searchCase = Get-ComplianceCase $originalSearch.CaseId
      $caseName = $searchCase.Name
  }
  # Need to cast this value as a Boolean the old fashion way
  $allowNotFoundExchangeLocationsEnabled = $false
  if ($originalSearch.AllowNotFoundExchangeLocationsEnabled)
  {
      $allowNotFoundExchangeLocationsEnabled = $true
  }
  $newSearch = New-ComplianceSearch -Name $newSearchName -AllowNotFoundExchangeLocationsEnabled $allowNotFoundExchangeLocationsEnabled -Case $caseName -ContentMatchQuery $originalSearch.ContentMatchQuery -Description $originalSearch.Description -ExchangeLocation $originalSearch.ExchangeLocation -ExchangeLocationExclusion $originalSearch.ExchangeLocationExclusion -Language $originalSearch.Language -SharePointLocation $originalSearch.SharePointLocation -SharePointLocationExclusion $originalSearch.SharePointLocationExclusion -PublicFolderLocation $originalSearch.PublicFolderLocation
  if ($newSearch)
  {
      Write-Host $newSearch.Name "was successfully created" -ForegroundColor Yellow
  }
  ```

2. Öffnen Sie Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.
    
3. Führen Sie das Skript aus; Zum Beispiel:
    
    ```
    .\CloneSearch.ps1
    ```

4. Wenn Sie zur Eingabe Ihrer Anmeldeinformationen aufgefordert werden, geben Sie Ihre e-Mail-Adresse und Ihr Kennwort ein, und klicken Sie auf **OK**.
    
5. Geben Sie die folgenden Informationen ein, wenn Sie vom Skript dazu aufgefordert werden. Geben Sie jede Information ein, und drücken **Sie die Eingabe**Taste.
    
    - Der Name der vorhandenen Suche.
    
    - Der Name der neuen Suche.
    
    Das Skript erstellt die neue Inhaltssuche, startet Sie jedoch nicht. Dadurch haben Sie die Möglichkeit, die Suche im nächsten Schritt zu bearbeiten und auszuführen. Sie können die Eigenschaften der neuen Suche anzeigen, indem Sie das Cmdlet **Get-ComplianceSearch** ausführen oder die Seite **Inhaltssuche** oder **eDiscovery** im Compliance Center aufrufen, je nachdem, ob die neue Suche einem Fall zugeordnet ist oder nicht. 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-compliance-center"></a>Schritt 2: Bearbeiten und Ausführen der geklonten Suche im Compliance Center

Nachdem Sie das Skript ausgeführt haben, um eine vorhandene Inhaltssuche zu klonen, besteht der nächste Schritt im Compliance Center, um die neue Suche zu bearbeiten und auszuführen. Wie bereits erwähnt, können Sie eine Suche bearbeiten, indem Sie die Keyword-Suchabfrage ändern und Suchbedingungen hinzufügen oder entfernen. Weitere Informationen finden Sie unter:
  
- [Inhaltssuche in Office 365](content-search.md)
    
- [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
    
- [eDiscovery-Fälle](ediscovery-cases.md)
