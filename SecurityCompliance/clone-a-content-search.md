---
title: Klonen einer Inhaltssuche in Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 4/26/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Verwenden Sie das Windows PowerShell-Skript in diesem Artikel schnell Klonen einer vorhandenen Inhaltssuche in das Wertpapier &amp; Compliane Center suchen. Wenn Sie ein Klonen eine Suche, wird eine neue Suche (unter einem neuen Namen) erstellt, die die gleichen Eigenschaften wie die ursprüngliche Suche enthält. Sie können dann die neue Suche bearbeiten (durch Ändern der Stichwortabfrage oder der Datumsbereich), und führen Sie ihn.
ms.openlocfilehash: a4f801e3de281e8caf8aeb7d1c2bd48f0facb77c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529323"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a>Klonen einer Inhaltssuche in Office 365-Sicherheit &amp; Compliance Center

Erstellen eine Inhaltssuche in Office 365-Sicherheit &amp; Compliance Center, das viele Postfächer oder SharePoint durchsucht und OneDrive for Business-Websites kann einen Moment dauern. Angeben der Websites suchen kann auch sein fehleranfällig, wenn Sie eine URL falsch eingegeben. Um diese Probleme zu vermeiden, können die Windows PowerShell-Skripts in diesem Artikel Sie schnell Klonen einer vorhandenen Content-Suche. Wenn Sie ein Klonen eine Suche, wird eine neue Suche (mit einem anderen Namen) erstellt, die die gleichen Eigenschaften (wie die Speicherorte für Inhalte und die Suchabfrage) wie die ursprüngliche Suche enthält. Sie bearbeiten die neue Suche (durch Ändern der Stichwortabfrage oder der Datumsbereich), und führen Sie es.
  
Warum Klonen Content-Suche?
  
- Führen zum Vergleichen der Ergebnisse auf anderes Stichwort Suchabfragen auf der gleichen Speicherorte für Inhalte.
    
- Speichern Sie eine große Anzahl von Speicherorte für Inhalte erneut eingeben, wenn Sie eine neue Suche erstellen müssen.
    
- Um die Größe der Suchergebnisse zu verringern; Wenn Sie eine Suche, die so exportieren Sie zu viele Ergebnisse zurückgibt verfügen, können Sie beispielsweise Klonen die Suche und fügen Sie eine Suche Bedingung basierend auf einen Datumsbereich aus, um die Anzahl der Suchergebnisse zu verringern.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center zum Ausführen des Skripts in diesem Thema beschrieben.
    
- Das Skript enthält minimale Fehlerbehandlung. Der primäre Zweck des Skripts ist ein Inhaltssuche schnell klonen.
    
- Das Skript erstellt eine neue Inhaltssuche, aber es kann nicht gestartet werden.
    
- Dieses Skript berücksichtigt, ob die Content-Suche, die Sie Klonen einer eDiscovery-Fall zugeordnet ist. Wenn die Suche eine Anfrage zugeordnet ist, wird die neue Suche auch die gleiche Groß-/Kleinschreibung zugeordnet werden. Wenn die vorhandene Suche keine Anfrage zugeordnet ist, wird die neue Suche auf der Seite **Inhaltssuche** in das Wertpapier aufgeführt &amp; Compliance Center. 
    
- Das Beispielskript bereitgestellt, die in diesem Thema wird unter keinem standard Support-Programm von Microsoft oder der Dienst nicht unterstützt. Das Beispielskript wird wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt alle konkludente Garantien einschließlich, aber nicht beschränkt auf konkludente Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck. Das gesamte Risiko aus der Verwendung oder der Leistung der Beispielskript und der Dokumentation liegt bei Ihnen. In keinem Fall muss Microsoft, seine Autoren oder ein Benutzer die Erstellung, Produktion oder Übermittlung der Skripts else beteiligt für Schäden jeglicher Art (einschließlich, aber nicht beschränkt auf Schäden für den Verlust von Gewinn Business, Business Unterbrechung, Verlust von Unternehmensinformationen, Folge- oder) aus der Verwendung des oder der Fehler beim Verwenden der Beispielskripts oder der Dokumentation, haftbar gemacht werden, auch wenn Microsoft die Möglichkeit solcher Schäden hingewiesen wurde.
  
## <a name="step-1-run-the-script-to-clone-a-search"></a>Schritt 1: Ausführen des Skripts zum Klonen einer Suche

Das Skript in diesem Schritt wird eine neue Inhaltssuche durch Klonen einer vorhandenen Farm erstellt. Wenn Sie dieses Skript ausführen, werden Sie für die folgenden Informationen aufgefordert:
  
- **Ihre Anmeldeinformationen** – das Skript wird unter Verwendung Ihrer Anmeldeinformationen für die Verbindung für die Sicherheit &amp; Compliance Center für Office 365-Organisation mit Windows PowerShell. Wie bereits erwähnt, müssen Sie Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center, um das Skript auszuführen. 
    
- **Der Name der vorhandenen Suche** – Dies ist die Content-Suche, die Sie kopieren möchten. 
    
- **Der Name der neuen Suche, die erstellt werden sollen** – Wenn Sie diesen Wert leer lassen, wird das Skript einen Namen für die neue Suche erstellen, die auf den Namen der Suche basiert, die Sie klonen. 
    
Klonen Sie eine Suche:
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `CloneSearch.ps1`.
    
  ```
  # This PowerShell script clones an existing Content Search in the Office 365 Security &amp; Compliance Center
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
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)"
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
    
3. Führen Sie das Skript; Zum Beispiel:
    
    ```
    .\CloneSearch.ps1
    ```

4. Geben Sie nach Ihren Anmeldeinformationen gefragt Ihre e-Mail-Adresse und das Kennwort ein, und klicken Sie dann auf **OK**.
    
5. Geben Sie den folgenden Informationen bei entsprechender Aufforderung durch das Skript. Geben Sie jede Informationseinheit, und drücken Sie dann die **EINGABETASTE**.
    
    - Der Name der vorhandenen Suche.
    
    - Der Name der neuen Suche.
    
    Das Skript erstellt die neue Inhaltssuche, aber es kann nicht gestartet werden. Dies gibt die Möglichkeit zum Bearbeiten, und führen Sie die Suche im nächsten Schritt. Sie können die Eigenschaften der neuen Suche durch Ausführen des Cmdlets **Get-ComplianceSearch** oder indem Sie auf der Seite **Inhaltssuche** oder **eDiscovery** in das Wertpapier anzeigen &amp; Compliance Center, je nachdem, ob die neue Suche ist eine Anfrage zugeordnet ist. 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a>Schritt 2: Bearbeiten, und führen Sie die geklonte Suche in das Wertpapier &amp; Compliance Center

Nach dem die haben Ausführen des Skripts zum Klonen einer vorhandenen Inhaltssuche, wird im nächsten Schritt wird, fahren Sie mit der Sicherheit &amp; Compliance Center bearbeiten, und führen Sie die neue Suche. Wie bereits erwähnt, können Sie eine Suche bearbeiten, indem die Keyword Search-Abfrage ändern und hinzufügen oder Entfernen von Bedingungen suchen. Weitere Informationen finden Sie unter:
  
- [Content-Suche in Office 365](content-search.md)
    
- [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
    
- [eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](ediscovery-cases.md)
