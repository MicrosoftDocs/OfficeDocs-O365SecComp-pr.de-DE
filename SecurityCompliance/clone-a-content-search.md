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
ms.assetid: 7b40eeaa-544c-4534-b89b-9f79998e374c
description: Verwenden Sie das Windows PowerShell-Skript in diesem Artikel schnell Klonen einer vorhandenen Inhaltssuche in das Wertpapier &amp; Compliane Center suchen. Wenn Sie ein Klonen eine Suche, wird eine neue Suche (unter einem neuen Namen) erstellt, die die gleichen Eigenschaften wie die ursprüngliche Suche enthält. Sie können dann die neue Suche bearbeiten (durch Ändern der Stichwortabfrage oder der Datumsbereich), und führen Sie ihn.
ms.openlocfilehash: fd2ea0d8fa812d23e7479b664b13c786a62d5a38
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038048"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="a7a8c-105">Klonen einer Inhaltssuche in Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="a7a8c-105">Clone a Content Search in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="a7a8c-p102">Erstellen eine Inhaltssuche in Office 365-Sicherheit &amp; Compliance Center, das viele Postfächer oder SharePoint durchsucht und OneDrive for Business-Websites kann einen Moment dauern. Angeben der Websites suchen kann auch sein fehleranfällig, wenn Sie eine URL falsch eingegeben. Um diese Probleme zu vermeiden, können die Windows PowerShell-Skripts in diesem Artikel Sie schnell Klonen einer vorhandenen Content-Suche. Wenn Sie ein Klonen eine Suche, wird eine neue Suche (mit einem anderen Namen) erstellt, die die gleichen Eigenschaften (wie die Speicherorte für Inhalte und die Suchabfrage) wie die ursprüngliche Suche enthält. Sie bearbeiten die neue Suche (durch Ändern der Stichwortabfrage oder der Datumsbereich), und führen Sie es.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-p102">Creating a Content Search in Office 365 Security &amp; Compliance Center that searches a lot of mailboxes or SharePoint and OneDrive for Business sites can take awhile. Specifying the sites to search can also be prone to errors if you mistype a URL. To avoid these issues, you can use the Windows PowerShell script in this article to quickly clone an existing Content Search. When a you clone a search, a new search (with a different name) is created that contains the same properties (such as the content locations and the search query) as the original search. Then you can edit the new search (by changing the keyword query or the date range) and run it.</span></span>
  
<span data-ttu-id="a7a8c-111">Warum Klonen Content-Suche?</span><span class="sxs-lookup"><span data-stu-id="a7a8c-111">Why clone Content Searches?</span></span>
  
- <span data-ttu-id="a7a8c-112">Führen zum Vergleichen der Ergebnisse auf anderes Stichwort Suchabfragen auf der gleichen Speicherorte für Inhalte.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-112">To compare the results of different keyword search queries run on the same content locations.</span></span>
    
- <span data-ttu-id="a7a8c-113">Speichern Sie eine große Anzahl von Speicherorte für Inhalte erneut eingeben, wenn Sie eine neue Suche erstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-113">To save you from having to re-enter a large number of content locations when you create a new search.</span></span>
    
- <span data-ttu-id="a7a8c-114">Um die Größe der Suchergebnisse zu verringern; Wenn Sie eine Suche, die so exportieren Sie zu viele Ergebnisse zurückgibt verfügen, können Sie beispielsweise Klonen die Suche und fügen Sie eine Suche Bedingung basierend auf einen Datumsbereich aus, um die Anzahl der Suchergebnisse zu verringern.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-114">To decrease the size of the search results; for example, if you have a search that returns too many results to export, you can clone the search and then add a search condition based on a date range to reduce the number of search results.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="a7a8c-115">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="a7a8c-115">Before you begin</span></span>

- <span data-ttu-id="a7a8c-116">Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center zum Ausführen des Skripts in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-116">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script described in this topic.</span></span>
    
- <span data-ttu-id="a7a8c-p103">Das Skript enthält minimale Fehlerbehandlung. Der primäre Zweck des Skripts ist ein Inhaltssuche schnell klonen.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-p103">The script includes minimal error handling. The primary purpose of the script is to quickly clone a content search.</span></span>
    
- <span data-ttu-id="a7a8c-119">Das Skript erstellt eine neue Inhaltssuche, aber es kann nicht gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-119">The script creates a new Content Search, but doesn't start it.</span></span>
    
- <span data-ttu-id="a7a8c-p104">Dieses Skript berücksichtigt, ob die Content-Suche, die Sie Klonen einer eDiscovery-Fall zugeordnet ist. Wenn die Suche eine Anfrage zugeordnet ist, wird die neue Suche auch die gleiche Groß-/Kleinschreibung zugeordnet werden. Wenn die vorhandene Suche keine Anfrage zugeordnet ist, wird die neue Suche auf der Seite **Inhaltssuche** in das Wertpapier aufgeführt &amp; Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-p104">This script takes into account whether the Content Search that you're cloning is associated with an eDiscovery case. If the search is associated with a case, the new search will also be associated with the same case. If the existing search isn't associated with a case, the new search will be listed on the **Content search** page in the Security &amp; Compliance Center.</span></span> 
    
- <span data-ttu-id="a7a8c-p105">Das Beispielskript bereitgestellt, die in diesem Thema wird unter keinem standard Support-Programm von Microsoft oder der Dienst nicht unterstützt. Das Beispielskript wird wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt alle konkludente Garantien einschließlich, aber nicht beschränkt auf konkludente Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck. Das gesamte Risiko aus der Verwendung oder der Leistung der Beispielskript und der Dokumentation liegt bei Ihnen. In keinem Fall muss Microsoft, seine Autoren oder ein Benutzer die Erstellung, Produktion oder Übermittlung der Skripts else beteiligt für Schäden jeglicher Art (einschließlich, aber nicht beschränkt auf Schäden für den Verlust von Gewinn Business, Business Unterbrechung, Verlust von Unternehmensinformationen, Folge- oder) aus der Verwendung des oder der Fehler beim Verwenden der Beispielskripts oder der Dokumentation, haftbar gemacht werden, auch wenn Microsoft die Möglichkeit solcher Schäden hingewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-p105">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-clone-a-search"></a><span data-ttu-id="a7a8c-128">Schritt 1: Ausführen des Skripts zum Klonen einer Suche</span><span class="sxs-lookup"><span data-stu-id="a7a8c-128">Step 1: Run the script to clone a search</span></span>

<span data-ttu-id="a7a8c-p106">Das Skript in diesem Schritt wird eine neue Inhaltssuche durch Klonen einer vorhandenen Farm erstellt. Wenn Sie dieses Skript ausführen, werden Sie für die folgenden Informationen aufgefordert:</span><span class="sxs-lookup"><span data-stu-id="a7a8c-p106">The script in this step will create a new Content Search by cloning an existing one. When you run this script, you'll be prompted for the following information:</span></span>
  
- <span data-ttu-id="a7a8c-p107">**Ihre Anmeldeinformationen** – das Skript wird unter Verwendung Ihrer Anmeldeinformationen für die Verbindung für die Sicherheit &amp; Compliance Center für Office 365-Organisation mit Windows PowerShell. Wie bereits erwähnt, müssen Sie Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center, um das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-p107">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center for your Office 365 organization with Windows PowerShell. As previously stated, you have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script.</span></span> 
    
- <span data-ttu-id="a7a8c-133">**Der Name der vorhandenen Suche** – Dies ist die Content-Suche, die Sie kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-133">**The name of the existing search** - This is the Content Search that you want to clone.</span></span> 
    
- <span data-ttu-id="a7a8c-134">**Der Name der neuen Suche, die erstellt werden sollen** – Wenn Sie diesen Wert leer lassen, wird das Skript einen Namen für die neue Suche erstellen, die auf den Namen der Suche basiert, die Sie klonen.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-134">**The name of the new search that will be created** - If you leave this value blank, the script will create a name for the new search that is based on the name of the search that you're cloning.</span></span> 
    
<span data-ttu-id="a7a8c-135">Klonen Sie eine Suche:</span><span class="sxs-lookup"><span data-stu-id="a7a8c-135">To clone a search:</span></span>
  
1. <span data-ttu-id="a7a8c-136">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `CloneSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-136">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CloneSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="a7a8c-137">Öffnen Sie Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-137">Open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="a7a8c-138">Führen Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="a7a8c-138">Run the script; for example:</span></span>
    
    ```
    .\CloneSearch.ps1
    ```

4. <span data-ttu-id="a7a8c-139">Geben Sie nach Ihren Anmeldeinformationen gefragt Ihre e-Mail-Adresse und das Kennwort ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-139">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span>
    
5. <span data-ttu-id="a7a8c-p108">Geben Sie den folgenden Informationen bei entsprechender Aufforderung durch das Skript. Geben Sie jede Informationseinheit, und drücken Sie dann die **EINGABETASTE**.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-p108">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="a7a8c-142">Der Name der vorhandenen Suche.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-142">The name of the existing search.</span></span>
    
    - <span data-ttu-id="a7a8c-143">Der Name der neuen Suche.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-143">The name of the new search.</span></span>
    
    <span data-ttu-id="a7a8c-p109">Das Skript erstellt die neue Inhaltssuche, aber es kann nicht gestartet werden. Dies gibt die Möglichkeit zum Bearbeiten, und führen Sie die Suche im nächsten Schritt. Sie können die Eigenschaften der neuen Suche durch Ausführen des Cmdlets **Get-ComplianceSearch** oder indem Sie auf der Seite **Inhaltssuche** oder **eDiscovery** in das Wertpapier anzeigen &amp; Compliance Center, je nachdem, ob die neue Suche ist eine Anfrage zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="a7a8c-p109">The script creates the new Content Search, but doesn't start it. This gives you a chance to edit and run the search in the next step. You can view the properties of the new search by running the **Get-ComplianceSearch** cmdlet or by going to the **Content search** or **eDiscovery** page in the Security &amp; Compliance Center, depending on whether or not the new search is associated with a case.</span></span> 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a><span data-ttu-id="a7a8c-147">Schritt 2: Bearbeiten, und führen Sie die geklonte Suche in das Wertpapier &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="a7a8c-147">Step 2: Edit and run the cloned search in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="a7a8c-p110">Nach dem die haben Ausführen des Skripts zum Klonen einer vorhandenen Inhaltssuche, wird im nächsten Schritt wird, fahren Sie mit der Sicherheit &amp; Compliance Center bearbeiten, und führen Sie die neue Suche. Wie bereits erwähnt, können Sie eine Suche bearbeiten, indem die Keyword Search-Abfrage ändern und hinzufügen oder Entfernen von Bedingungen suchen. Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="a7a8c-p110">After the you've run the script to clone an existing Content Search, the next step is to go to the Security &amp; Compliance Center to edit and run the new search. As previously stated, you can edit a search by changing the keyword search query and adding or removing search conditions. For more information, see:</span></span>
  
- [<span data-ttu-id="a7a8c-151">Content-Suche in Office 365</span><span class="sxs-lookup"><span data-stu-id="a7a8c-151">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="a7a8c-152">Stichwortabfragen und Suchbedingungen für die Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="a7a8c-152">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="a7a8c-153">eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="a7a8c-153">eDiscovery cases in the Office 365 Security &amp; Compliance Center</span></span>](ediscovery-cases.md)
