---
title: Klonen einer Inhaltssuche im Office 365 Security &amp; Compliance Center
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
description: Verwenden Sie das Windows PowerShell-Skript in diesem Artikel, um eine vorhandene Inhaltssuche in der &amp; Security Compliane Center-Suche schnell zu klonen. Wenn Sie eine Suche Klonen, wird eine neue Suche (mit einem neuen Namen) erstellt, die die gleichen Eigenschaften wie die ursprüngliche Suche enthält. Dann können Sie die neue Suche bearbeiten (indem Sie die Stichwortabfrage oder den Datumszeitraum ändern) und dann ausführen.
ms.openlocfilehash: 15f1ca5d00f03f510745fef7ae8418192a9eb448
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213545"
---
# <a name="clone-a-content-search-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="5fe40-105">Klonen einer Inhaltssuche im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="5fe40-105">Clone a Content Search in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="5fe40-p102">Das Erstellen einer Inhaltssuche im Office 365 &amp; Security Compliance Center, das viele Postfächer oder SharePoint-und OneDrive für Business-Websites durchsucht, kann eine Weile dauern. Das Angeben der zu durchsuchenden Websites kann auch fehleranfällig sein, wenn Sie eine URL-Adresse nicht mehr eingeben. Um diese Probleme zu vermeiden, können Sie das Windows PowerShell-Skript in diesem Artikel verwenden, um eine vorhandene Inhaltssuche schnell zu klonen. Wenn Sie eine Suche Klonen, wird eine neue Suche (mit einem anderen Namen) erstellt, die die gleichen Eigenschaften (wie die inhaltsspeicherorte und die Suchabfrage) als ursprüngliche Suche enthält. Dann können Sie die neue Suche bearbeiten (indem Sie die Stichwortabfrage oder den Datumszeitraum ändern) und ausführen.</span><span class="sxs-lookup"><span data-stu-id="5fe40-p102">Creating a Content Search in Office 365 Security &amp; Compliance Center that searches a lot of mailboxes or SharePoint and OneDrive for Business sites can take awhile. Specifying the sites to search can also be prone to errors if you mistype a URL. To avoid these issues, you can use the Windows PowerShell script in this article to quickly clone an existing Content Search. When a you clone a search, a new search (with a different name) is created that contains the same properties (such as the content locations and the search query) as the original search. Then you can edit the new search (by changing the keyword query or the date range) and run it.</span></span>
  
<span data-ttu-id="5fe40-111">Gründe für das Klonen von Inhalts suchen</span><span class="sxs-lookup"><span data-stu-id="5fe40-111">Why clone Content Searches?</span></span>
  
- <span data-ttu-id="5fe40-112">Zum Vergleichen der Ergebnisse unterschiedlicher Keyword-Suchabfragen, die an denselben Inhaltsspeicherorten ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5fe40-112">To compare the results of different keyword search queries run on the same content locations.</span></span>
    
- <span data-ttu-id="5fe40-113">Sie müssen beim Erstellen einer neuen Suche eine Vielzahl von Inhaltsspeicherorten erneut eingeben.</span><span class="sxs-lookup"><span data-stu-id="5fe40-113">To save you from having to re-enter a large number of content locations when you create a new search.</span></span>
    
- <span data-ttu-id="5fe40-114">So verringern Sie die Größe der Suchergebnisse Wenn Sie beispielsweise eine Suche haben, die zu viele Ergebnisse zum Exportieren zurückgibt, können Sie die Suche Klonen und dann eine Suchbedingung basierend auf einem Datumsbereich hinzufügen, um die Anzahl der Suchergebnisse zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="5fe40-114">To decrease the size of the search results; for example, if you have a search that returns too many results to export, you can clone the search and then add a search condition based on a date range to reduce the number of search results.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="5fe40-115">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="5fe40-115">Before you begin</span></span>

- <span data-ttu-id="5fe40-116">Sie müssen Mitglied der eDiscovery-Manager-Rollengruppe im Security &amp; Compliance Center sein, um das in diesem Thema beschriebene Skript ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="5fe40-116">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script described in this topic.</span></span>
    
- <span data-ttu-id="5fe40-p103">Das Skript enthält eine minimale Fehlerbehandlung. Der Hauptzweck des Skripts besteht darin, eine Inhaltssuche schnell zu klonen.</span><span class="sxs-lookup"><span data-stu-id="5fe40-p103">The script includes minimal error handling. The primary purpose of the script is to quickly clone a content search.</span></span>
    
- <span data-ttu-id="5fe40-119">Das Skript erstellt eine neue Inhaltssuche, startet Sie jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="5fe40-119">The script creates a new Content Search, but doesn't start it.</span></span>
    
- <span data-ttu-id="5fe40-p104">Dieses Skript berücksichtigt, ob die Inhaltssuche, die Sie Klonen, einem eDiscovery-Fall zugeordnet ist. Wenn die Suche mit einem Fall verknüpft ist, wird die neue Suche auch mit dem gleichen Fall verknüpft. Wenn die vorhandene Suche keinem Fall zugeordnet ist, wird die neue Suche auf der Seite " **Inhaltssuche** " im Security &amp; Compliance Center aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fe40-p104">This script takes into account whether the Content Search that you're cloning is associated with an eDiscovery case. If the search is associated with a case, the new search will also be associated with the same case. If the existing search isn't associated with a case, the new search will be listed on the **Content search** page in the Security &amp; Compliance Center.</span></span> 
    
- <span data-ttu-id="5fe40-p105">Das Beispielskript in diesem Thema wird unter keinem Microsoft Standard-Support Programm oder-Dienst unterstützt. Das Beispielskript wird ohne Gewähr bereitgestellt. Microsoft lehnt weiterhin alle impliziten Garantien ab, einschließlich der impliziten Garantien der Marktgängigkeit oder der Eignung für einen bestimmten Zweck. Das gesamte Risiko, das sich aus der Verwendung oder Leistung des Beispielskripts und der Dokumentation ergibt, liegt bei Ihnen. In keinem Fall sind Microsoft, seine Autoren oder andere Personen, die an der Erstellung, Produktion oder Bereitstellung der Skripte beteiligt sind, haftbar für Schäden jeglicher Art (einschließlich, ohne Einschränkung, Schäden für Verlust von Geschäftsgewinnen, Betriebsunterbrechung, Verlust von geschäftliche Informationen oder sonstige Vermögensschäden, die sich aus der Verwendung oder nicht Verwendung der Beispielskripts oder Dokumentation ergeben, auch wenn Microsoft über die Möglichkeit solcher Schäden informiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5fe40-p105">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-clone-a-search"></a><span data-ttu-id="5fe40-128">Schritt 1: Ausführen des Skripts zum Klonen einer Suche</span><span class="sxs-lookup"><span data-stu-id="5fe40-128">Step 1: Run the script to clone a search</span></span>

<span data-ttu-id="5fe40-p106">Mit dem Skript in diesem Schritt wird eine neue Inhaltssuche erstellt, indem eine vorhandene geklont wird. Wenn Sie dieses Skript ausführen, werden Sie aufgefordert, die folgenden Informationen einzugeben:</span><span class="sxs-lookup"><span data-stu-id="5fe40-p106">The script in this step will create a new Content Search by cloning an existing one. When you run this script, you'll be prompted for the following information:</span></span>
  
- <span data-ttu-id="5fe40-p107">**Ihre Benutzeranmeldeinformationen** – das Skript verwendet Ihre Anmeldeinformationen zum Herstellen einer Verbindung &amp; mit dem Security Compliance Center für Ihre Office 365-Organisation mit Windows PowerShell. Wie bereits erwähnt, müssen Sie ein Mitglied der eDiscovery-Manager-Rollengruppe im Security &amp; Compliance Center sein, um das Skript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5fe40-p107">**Your user credentials** - The script will use your credentials to connect to the Security &amp; Compliance Center for your Office 365 organization with Windows PowerShell. As previously stated, you have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script.</span></span> 
    
- <span data-ttu-id="5fe40-133">**Der Name der vorhandenen Suche** – hierbei handelt es sich um die Inhaltssuche, die Sie klonen möchten.</span><span class="sxs-lookup"><span data-stu-id="5fe40-133">**The name of the existing search** - This is the Content Search that you want to clone.</span></span> 
    
- <span data-ttu-id="5fe40-134">**Der Name der neuen Suche, die erstellt wird** -Wenn Sie diesen Wert leer lassen, erstellt das Skript einen Namen für die neue Suche, der auf dem Namen der zu klonenden Suche basiert.</span><span class="sxs-lookup"><span data-stu-id="5fe40-134">**The name of the new search that will be created** - If you leave this value blank, the script will create a name for the new search that is based on the name of the search that you're cloning.</span></span> 
    
<span data-ttu-id="5fe40-135">So Klonen Sie eine Suche:</span><span class="sxs-lookup"><span data-stu-id="5fe40-135">To clone a search:</span></span>
  
1. <span data-ttu-id="5fe40-136">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `CloneSearch.ps1`.</span><span class="sxs-lookup"><span data-stu-id="5fe40-136">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CloneSearch.ps1`.</span></span>
    
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

2. <span data-ttu-id="5fe40-137">Öffnen Sie Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="5fe40-137">Open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="5fe40-138">Führen Sie das Skript aus; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5fe40-138">Run the script; for example:</span></span>
    
    ```
    .\CloneSearch.ps1
    ```

4. <span data-ttu-id="5fe40-139">Wenn Sie zur Eingabe Ihrer Anmeldeinformationen aufgefordert werden, geben Sie Ihre e-Mail-Adresse und Ihr Kennwort ein, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5fe40-139">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span>
    
5. <span data-ttu-id="5fe40-p108">Geben Sie die folgenden Informationen ein, wenn Sie vom Skript dazu aufgefordert werden. Geben Sie jede Information ein, und drücken **Sie die Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="5fe40-p108">Enter following information when prompted by the script. Type each piece of information and then press **Enter**.</span></span>
    
    - <span data-ttu-id="5fe40-142">Der Name der vorhandenen Suche.</span><span class="sxs-lookup"><span data-stu-id="5fe40-142">The name of the existing search.</span></span>
    
    - <span data-ttu-id="5fe40-143">Der Name der neuen Suche.</span><span class="sxs-lookup"><span data-stu-id="5fe40-143">The name of the new search.</span></span>
    
    <span data-ttu-id="5fe40-p109">Das Skript erstellt die neue Inhaltssuche, startet Sie jedoch nicht. Dadurch haben Sie die Möglichkeit, die Suche im nächsten Schritt zu bearbeiten und auszuführen. Sie können die Eigenschaften der neuen Suche anzeigen, indem Sie das Cmdlet **Get-ComplianceSearch** ausführen oder im Security &amp; Compliance Center auf die Seite **Inhaltssuche** oder **eDiscovery** wechseln, je nachdem, ob die neue Suche mit einer Groß-/Kleinschreibung verknüpft.</span><span class="sxs-lookup"><span data-stu-id="5fe40-p109">The script creates the new Content Search, but doesn't start it. This gives you a chance to edit and run the search in the next step. You can view the properties of the new search by running the **Get-ComplianceSearch** cmdlet or by going to the **Content search** or **eDiscovery** page in the Security &amp; Compliance Center, depending on whether or not the new search is associated with a case.</span></span> 
  
## <a name="step-2-edit-and-run-the-cloned-search-in-the-security-amp-compliance-center"></a><span data-ttu-id="5fe40-147">Schritt 2: Bearbeiten und Ausführen der geklonten Suche im Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="5fe40-147">Step 2: Edit and run the cloned search in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="5fe40-p110">Nachdem Sie das Skript ausgeführt haben, um eine vorhandene Inhaltssuche zu klonen, besteht der nächste Schritt im Security &amp; Compliance Center, um die neue Suche zu bearbeiten und auszuführen. Wie bereits erwähnt, können Sie eine Suche bearbeiten, indem Sie die Keyword-Suchabfrage ändern und Suchbedingungen hinzufügen oder entfernen. Weitere Informationen finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="5fe40-p110">After the you've run the script to clone an existing Content Search, the next step is to go to the Security &amp; Compliance Center to edit and run the new search. As previously stated, you can edit a search by changing the keyword search query and adding or removing search conditions. For more information, see:</span></span>
  
- [<span data-ttu-id="5fe40-151">Inhaltssuche in Office 365</span><span class="sxs-lookup"><span data-stu-id="5fe40-151">Content Search in Office 365</span></span>](content-search.md)
    
- [<span data-ttu-id="5fe40-152">Stichwortabfragen und Suchbedingungen für die Inhaltssuche</span><span class="sxs-lookup"><span data-stu-id="5fe40-152">Keyword queries and search conditions for Content Search</span></span>](keyword-queries-and-search-conditions.md)
    
- [<span data-ttu-id="5fe40-153">eDiscovery-Fälle im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="5fe40-153">eDiscovery cases in the Office 365 Security &amp; Compliance Center</span></span>](ediscovery-cases.md)
