---
title: Verwenden Sie Inhaltssuche in Office 365 für zielgerichtete Auflistungen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Verwenden Sie Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center gezielte Websitesammlungen ausführen. Eine Sammlung bedeutet, dass Sie davon überzeugt sind, dass auf eine Anfrage reagieren oder privilegierten Elemente in einem bestimmten Postfach oder einer Website Ordner befinden. Verwenden Sie das Skript in diesem Artikel erhalten Sie die Ordner-ID oder den Pfad für die bestimmten Ordner Postfach oder einer Website, die Sie suchen möchten.
ms.openlocfilehash: 094fa4de4b8de9782a9bafb2eb8fb6ef3c52b46b
ms.sourcegitcommit: 06ae71741875f604bcc7a4e01b0b62cc768cbe97
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/13/2018
ms.locfileid: "27245062"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a><span data-ttu-id="27482-105">Verwenden Sie Inhaltssuche in Office 365 für zielgerichtete Auflistungen</span><span class="sxs-lookup"><span data-stu-id="27482-105">Use Content Search in Office 365 for targeted collections</span></span>

<span data-ttu-id="27482-p102">Das Inhaltssuche-Feature in die Office 365-Sicherheit &amp; Compliance Center nicht zur Verfügung, eine direkte Weise in der Benutzeroberfläche zum Durchsuchen bestimmter Ordner in Exchange-Postfächern oder SharePoint und OneDrive for Business-Websites. Es ist jedoch möglich, bestimmte Ordner (eine *Auflistung zielorientierten*genannt) zu suchen, indem Sie die Ordner-ID oder den Pfad in die eigentliche Suche-Abfragesyntax. Verwenden zum Ausführen einer Sammlung Inhaltssuche ist nützlich, wenn Sie davon überzeugt sind, dass auf eine Anfrage reagieren oder privilegierten Elemente in einem bestimmten Postfach oder einer Website Ordner befinden. Das Skript können in diesem Artikel Sie um die Ordner-ID für Postfachordner oder der Pfad zum Ordner auf einer SharePoint- und OneDrive for Business-Website zu erhalten. Anschließend können Sie die Ordner-ID oder den Pfad in einer Suchabfrage zurückzugebenden Elemente im Ordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="27482-p102">The Content Search feature in the Office 365 Security &amp; Compliance Center doesn't provide a direct way in the UI to search specific folders in Exchange mailboxes or SharePoint and OneDrive for Business sites. However, it's possible to search specific folders (called a *targeted collection*) by specifying the folder ID or path in the actual search query syntax. Using Content Search to perform a targeted collection is useful when you're confident that items responsive to a case or privileged items are located in a specific mailbox or site folder. You can use the script in this article to obtain the folder ID for mailbox folders or the path for folders on a SharePoint and OneDrive for Business site. Then you can use the folder ID or path in a search query to return items located in the folder.</span></span>
  
## <a name="before-you-begin"></a><span data-ttu-id="27482-111">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="27482-111">Before you begin</span></span>

- <span data-ttu-id="27482-p103">Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center zum Ausführen des Skripts in Schritt 1. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="27482-p103">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the script in Step 1. For more information, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
    <span data-ttu-id="27482-p104">Darüber hinaus müssen Sie die Rolle des E-Mail-Empfänger in Ihrer Exchange Online-Organisation zugewiesen werden. Dies ist erforderlich, um das Cmdlet **Get-mailboxfolderstatistics abrufen** ausgeführt werden, die in das Skript in Schritt 1 enthalten ist. Standardmäßig ist die E-Mail-Empfänger-Rolle zu Rollengruppen Organization Management und Recipient Management in Exchange Online zugewiesen. Weitere Informationen zum Zuweisen von Berechtigungen in Exchange Online finden Sie unter [Manage Role Gruppenmitglieder](https://go.microsoft.com/fwlink/p/?linkid=692102). Sie könnten auch erstellen eine benutzerdefinierten Rollengruppe, die E-Mail-Empfänger Rolle zuweisen, und fügen Sie die Mitglieder, die zum Ausführen des Skripts in Schritt 1 müssen. Weitere Informationen finden Sie unter [Rollengruppen verwalten](https://go.microsoft.com/fwlink/p/?linkid=730688).</span><span class="sxs-lookup"><span data-stu-id="27482-p104">Additionally, you have to be assigned the Mail Recipients role in your Exchange Online organization. This is required to run the **Get-MailboxFolderStatistics** cmdlet, which is included in the script in Step 1. By default, the Mail Recipients role is assigned to the Organization Management and Recipient Management role groups in Exchange Online. For more information about assigning permissions in Exchange Online, see [Manage role group members](https://go.microsoft.com/fwlink/p/?linkid=692102). You could also create a custom role group, assign the Mail Recipients role to it, and then add the members who need to run the script in Step 1. For more information, see [Manage role groups](https://go.microsoft.com/fwlink/p/?linkid=730688).</span></span>
    
- <span data-ttu-id="27482-p105">Jedes Mal, wenn Sie das Skript in Schritt 1 ausführen, wird eine neue remote-PowerShell-Sitzung erstellt. So können Sie Sie alle remote PowerShell Sessions zur Verfügung. Um dies zu verhindern, können Sie den folgenden Befehl zum Trennen von aktiven remote PowerShell-Sitzungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="27482-p105">Each time you run the script in Step 1, a new remote PowerShell session is created. So you could use up all the remote PowerShell sessions available to you. To prevent this from happening, you can run the following command to disconnect your active remote PowerShell sessions.</span></span>
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    <span data-ttu-id="27482-123">Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span><span class="sxs-lookup"><span data-stu-id="27482-123">For more information, see [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).</span></span>
    
- <span data-ttu-id="27482-p106">Das Skript enthält minimale Fehlerbehandlung. Der primäre Zweck des Skripts ist um schnell zeigt eine Liste der Postfachordner IDs oder Website Pfade, die in der Syntax Search-Abfrage ein Inhaltssuche zur Durchführung einer Sammlung verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="27482-p106">The script includes minimal error handling. The primary purpose of the script is to quickly display a list of mailbox folder IDs or site paths that can be used in the search query syntax of a Content Search to perform a targeted collection.</span></span>
    
- <span data-ttu-id="27482-p107">Das Beispielskript bereitgestellt, die in diesem Thema wird unter keinem standard Support-Programm von Microsoft oder der Dienst nicht unterstützt. Das Beispielskript wird wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt alle konkludente Garantien einschließlich, aber nicht beschränkt auf konkludente Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck. Das gesamte Risiko aus der Verwendung oder der Leistung der Beispielskript und der Dokumentation liegt bei Ihnen. In keinem Fall muss Microsoft, seine Autoren oder ein Benutzer die Erstellung, Produktion oder Übermittlung der Skripts else beteiligt für Schäden jeglicher Art (einschließlich, aber nicht beschränkt auf Schäden für den Verlust von Gewinn Business, Business Unterbrechung, Verlust von Unternehmensinformationen, Folge- oder) aus der Verwendung des oder der Fehler beim Verwenden der Beispielskripts oder der Dokumentation, haftbar gemacht werden, auch wenn Microsoft die Möglichkeit solcher Schäden hingewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="27482-p107">The sample script provided in this topic isn't supported under any Microsoft standard support program or service. The sample script is provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample script and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a><span data-ttu-id="27482-131">Schritt 1: Führen Sie das Skript aus, um eine Liste der Ordner für ein Postfach oder Website abrufen</span><span class="sxs-lookup"><span data-stu-id="27482-131">Step 1: Run the script to get a list of folders for a mailbox or site</span></span>

<span data-ttu-id="27482-p108">Das Skript, das Sie in dieser ersten Schritt ausführen, wird eine Liste der Postfachordner oder SharePoint oder OneDrive for Business-Ordner und die entsprechenden Ordner-ID oder Pfad für jeden Ordner zurück. Wenn Sie dieses Skript ausführen, fordert es Sie für die folgenden Informationen.</span><span class="sxs-lookup"><span data-stu-id="27482-p108">The script that you run in this first step will return a list of mailbox folders or SharePoint or OneDrive for Business folders, and the corresponding folder ID or path for each folder. When you run this script, it will prompt you for the following information.</span></span>
  
- <span data-ttu-id="27482-p109">**E-Mail-Adresse oder Website-URL** Geben Sie eine e-Mail-Adresse der Verwaltungsberechtigte um eine Liste der Exchange-Postfachordner und Ordner IDs zurückzugeben. Oder geben Sie die URL für eine SharePoint-Website oder eine OneDrive for Business-Website, um eine Liste der Pfade für die angegebene Website zurückzugeben. Es folgen einige Beispiele:</span><span class="sxs-lookup"><span data-stu-id="27482-p109">**Email address or site URL** Type an email address of the custodian to return a list of Exchange mailbox folders and folder IDs. Or type the URL for a SharePoint site or a OneDrive for Business site to return a list of paths for the specified site. Here are some examples:</span></span> 
    
  - <span data-ttu-id="27482-137">**Exchange** - stacig@contoso.onmicrosoft.com</span><span class="sxs-lookup"><span data-stu-id="27482-137">**Exchange** - stacig@contoso.onmicrosoft.com</span></span> 
    
  - <span data-ttu-id="27482-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span><span class="sxs-lookup"><span data-stu-id="27482-138">**SharePoint** - https://contoso.sharepoint.com/sites/marketing</span></span> 
    
  - <span data-ttu-id="27482-139">**OneDrive für Unternehmen** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span><span class="sxs-lookup"><span data-stu-id="27482-139">**OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com</span></span> 
    
- <span data-ttu-id="27482-p110">**Ihre Anmeldeinformationen** – das Skript wird unter Verwendung Ihrer Anmeldeinformationen für die Verbindung zu Exchange Online und die Sicherheit &amp; Compliance Center mit remote-PowerShell. Wie bereits erklärt müssen Sie die entsprechenden Berechtigungen zum erfolgreichen Ausführen dieses Skripts zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="27482-p110">**Your user credentials** - The script will use your credentials to connect to Exchange Online and the Security &amp; Compliance Center with remote PowerShell. As previously explained, you have to assigned the appropriate permissions to successfully run this script.</span></span>
    
<span data-ttu-id="27482-142">Zeigt eine Liste der Postfachordner oder Pfadnamen Website:</span><span class="sxs-lookup"><span data-stu-id="27482-142">To display a list of mailbox folders or site path names:</span></span>
  
1. <span data-ttu-id="27482-143">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `GetFolderSearchParameters.ps1`.</span><span class="sxs-lookup"><span data-stu-id="27482-143">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `GetFolderSearchParameters.ps1`.</span></span>
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security &amp; Compliance Center.           #
  # The script will then:                                           #
  #    * If an email address is supplied: list the folders for the target mailbox.          #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the folder paths for the site. #
  #    * In both cases, the script supplies the correct search properties (folderid: or path:)      #
  #      appended to the folder ID or path ID to use in a Content Search.               #
  # Notes:                                              #
  #    * For SharePoint and OneDrive for Business, the paths are searched recursively; this means the   #
  #      the current folder and all sub-folders are searched.                       #
  #    * For Exchange, only the specified folder will be searched; this means sub-folders in the folder #
  #      will not be searched.  To search sub-folders, you need to use the specify the folder ID for    #
  #      each sub-folder that you want to search.                               #
  #    * For Exchange, only folders in the user's primary mailbox will be returned by the script.       #
  #########################################################################################################
  # Collect the target email address or SharePoint Url
  $addressOrSite = Read-Host "Enter an email address or a URL for a SharePoint or OneDrive for Business site"
  # Authenticate with Exchange Online and the Security &amp; Compliance Center (Exchange Online Protection - EOP)
  if (!$credentials)
  {
      $credentials = Get-Credential
  }
  if ($addressOrSite.IndexOf("@") -ige 0)
  {
      # List the folder Ids for the target mailbox
      $emailAddress = $addressOrSite
      # Authenticate with Exchange Online
      if (!$ExoSession)
      {
          $ExoSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.outlook.com/powershell-liveid/ -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $ExoSession -AllowClobber -DisableNameChecking
      }
      $folderQueries = @()
      $folderStatistics = Get-MailboxFolderStatistics $emailAddress
      foreach ($folderStatistic in $folderStatistics)
      {
          $folderId = $folderStatistic.FolderId;
          $folderPath = $folderStatistic.FolderPath;
          $encoding= [System.Text.Encoding]::GetEncoding("us-ascii")
          $nibbler= $encoding.GetBytes("0123456789ABCDEF");
          $folderIdBytes = [Convert]::FromBase64String($folderId);
          $indexIdBytes = New-Object byte[] 48;
          $indexIdIdx=0;
          $folderIdBytes | select -skip 23 -First 24 | %{$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -shr 4];$indexIdBytes[$indexIdIdx++]=$nibbler[$_ -band 0xF]}
          $folderQuery = "folderid:$($encoding.GetString($indexIdBytes))";
          $folderStat = New-Object PSObject
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderPath -Value $folderPath
          Add-Member -InputObject $folderStat -MemberType NoteProperty -Name FolderQuery -Value $folderQuery
          $folderQueries += $folderStat
      }
      Write-Host "-----Exchange Folders-----"
      $folderQueries |ft
  }
  elseif ($addressOrSite.IndexOf("http") -ige 0)
  {
      $searchName = "SPFoldersSearch"
      $searchActionName = "SPFoldersSearch_Preview"
      # List the folders for the SharePoint or OneDrive for Business Site
      $siteUrl = $addressOrSite
      # Authenticate with the Security &amp; Compliance Center
      if (!$SccSession)
      {
          $SccSession = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $credentials -Authentication Basic -AllowRedirection
          Import-PSSession $SccSession -AllowClobber -DisableNameChecking
      }
      # Clean-up, if the script was aborted, the search we created might not have been deleted.  Try to do so now.
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
      # Create a Content Search against the SharePoint Site or OneDrive for Business site and only search for folders; wait for the search to complete
      $complianceSearch = New-ComplianceSearch -Name $searchName -ContentMatchQuery "contenttype:folder" -SharePointLocation $siteUrl
      Start-ComplianceSearch $searchName
      do{
          Write-host "Waiting for search to complete..."
          Start-Sleep -s 5
          $complianceSearch = Get-ComplianceSearch $searchName
      }while ($complianceSearch.Status -ne 'Completed')
      if ($complianceSearch.Items -gt 0)
      {
          # Create a Compliance Search Action and wait for it to complete. The folders will be listed in the .Results parameter
          $complianceSearchAction = New-ComplianceSearchAction -SearchName $searchName -Preview
          do
          {
              Write-host "Waiting for search action to complete..."
              Start-Sleep -s 5
              $complianceSearchAction = Get-ComplianceSearchAction $searchActionName
          }while ($complianceSearchAction.Status -ne 'Completed')
          # Get the results and print out the folders
          $results = $complianceSearchAction.Results
          $matches = Select-String "Data Link:.+[,}]" -Input $results -AllMatches
          foreach ($match in $matches.Matches)
          {
              $rawUrl = $match.Value
              $rawUrl = $rawUrl -replace "Data Link: " -replace "," -replace "}"
              Write-Host "path:""$rawUrl"""
          }
      }
      else
      {
          Write-Host "No folders were found for $siteUrl"
      }
      Remove-ComplianceSearch $searchName -Confirm:$false -ErrorAction 'SilentlyContinue'
  }
  else
  {
      Write-Error "Couldn't recognize $addressOrSite as an email address or a site URL"
  }
  ```

2. <span data-ttu-id="27482-144">Öffnen Sie auf dem lokalen Computer Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="27482-144">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span>
    
3. <span data-ttu-id="27482-145">Führen Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="27482-145">Run the script; for example:</span></span>
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. <span data-ttu-id="27482-146">Geben Sie die Informationen, der das Skript für aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="27482-146">Enter the information that the script prompts you for.</span></span>
    
    <span data-ttu-id="27482-p111">Das Skript zeigt eine Liste der Postfachordnern oder Site-Ordner für den angegebenen Benutzer. Lassen Sie dieses Fenster öffnen, damit Sie einen Ordnernamen-ID oder den Pfad zu kopieren und fügen Sie ihn in eine Suchabfrage in Schritt2 können.</span><span class="sxs-lookup"><span data-stu-id="27482-p111">The script displays a list of mailbox folders or site folder for the specified user. Let this window open so that you can copy a folder ID or path name and paste it in to a search query in Step 2.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="27482-p112">Statt eine Liste der Ordner auf dem Computerbildschirm angezeigt, können Sie die Ausgabe des Skripts in eine Textdatei umgeleitet. Diese Datei wird in den Ordner gespeichert werden, in das Skript gespeichert ist. Das Skript Ausgabe in eine Textdatei umleiten möchten, führen Sie beispielsweise den folgenden Befehl in Schritt 3: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` und klicken Sie dann einen Ordner-ID oder den Pfad aus der Datei in eine Suchabfrage verwenden kopieren können.</span><span class="sxs-lookup"><span data-stu-id="27482-p112">Instead of displaying a list of folders on the computer screen, you can re-direct the output of the script to a text file. This file will be saved to the folder where the script is located. For example, to redirect the script output to a text file, run the following command in Step 3:  `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Then you can copy a folder ID or path from the file to use in a search query.</span></span>
  
### <a name="script-output-for-mailbox-folders"></a><span data-ttu-id="27482-152">Ausgabe des Skripts für Postfachordner</span><span class="sxs-lookup"><span data-stu-id="27482-152">Script output for mailbox folders</span></span>

<span data-ttu-id="27482-p113">Wenn Sie Postfachordner IDs erhalten, müssen Sie das Skript stellt eine Verbindung mit Exchange Online mithilfe von remote-PowerShell, wird das Cmdlet **Get-MailboxFolderStatisics** ausgeführt, und klicken Sie dann zeigt die Liste der Ordner aus dem angegebenen Postfach. Für jeden Ordner im Postfach zeigt das Skript den Namen des Ordners in der Spalte **FolderPath** und die Ordner-ID in der Spalte **FolderQuery** . Darüber hinaus fügt das Skript das Präfix des **FolderId** (die den Namen der Postfach-Eigenschaft ist) der Ordner-ID. Da die **Folderid** -Eigenschaft einer Eigenschaft durchsuchbar ist, verwenden Sie `folderid:<folderid>` bei einer Suchabfrage in Schritt2, um den Ordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="27482-p113">If you're getting mailbox folder IDs, the script connects to Exchange Online by using remote PowerShell, runs the **Get-MailboxFolderStatisics** cmdlet, and then displays the list of the folders from the specified mailbox. For every folder in the mailbox, the script displays the name of the folder in the **FolderPath** column and the folder ID in the **FolderQuery** column. Additionally, the script adds the prefix of **folderId** (which is the name of the mailbox property) to the folder ID. Because the **folderid** property is a searchable property, you'll use  `folderid:<folderid>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="27482-157">Es folgt ein Beispiel der Ausgabe von dem Skript für Postfachordner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27482-157">Here's an example of the output returned by the script for mailbox folders.</span></span>
  
![Beispiel für die Liste der Postfachordner und Ordner vom Skript zurückgegebenen IDs](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
<span data-ttu-id="27482-159">Das Beispiel in Schritt2 zeigt die Abfrage für die Suche Unterordner "bereinigt" in den Ordner des Benutzers wiederherstellbare Elemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="27482-159">The example in Step 2 shows the query used to search the Purges subfolder in the user's Recoverable Items folder.</span></span>
  
### <a name="script-output-for-site-folders"></a><span data-ttu-id="27482-160">Ausgabe des Skripts für Websiteordner</span><span class="sxs-lookup"><span data-stu-id="27482-160">Script output for site folders</span></span>

<span data-ttu-id="27482-p114">Wenn Sie Pfade aus SharePoint oder OneDrive for Business-Websites erhalten, müssen Sie das Skript stellt eine Verbindung mit der Sicherheit &amp; Compliance Center mithilfe von remote PowerShell erstellt eine neue Inhaltssuche, die durchsucht der Website für die Ordner, und klicken Sie dann eine Liste der Ordner angezeigt befindet sich in der angegebenen Website. Das Skript werden die Namen der einzelnen Ordner angezeigt und die URL der Ordner das Präfix des **Pfad** (bei dem es sich um den Namen der Websiteeigenschaft handelt) hinzugefügt. Da die **Path** -Eigenschaft einer Eigenschaft durchsuchbar ist, verwenden Sie `path:<path>` bei einer Suchabfrage in Schritt2, um den Ordner zu suchen.</span><span class="sxs-lookup"><span data-stu-id="27482-p114">If you're getting paths from SharePoint or OneDrive for Business sites, the script connects to the Security &amp; Compliance Center using remote PowerShell, creates a new Content Search that searches the site for folders, and then displays a list of the folders located in the specified site. The script displays the name of each folder and adds the prefix of **path** (which is the name of the site property) to the folder URL. Because the **path** property is a searchable property, you'll use  `path:<path>` in a search query in Step 2 to search that folder.</span></span> 
  
<span data-ttu-id="27482-164">Es folgt ein Beispiel der Ausgabe von dem Skript für Websiteordner zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27482-164">Here's an example of the output returned by the script for site folders.</span></span>
  
![Beispiel für die Liste der Pfadnamen für Websiteordner zurückgegeben, die von dem Skript](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a><span data-ttu-id="27482-166">Schritt 2: Verwenden Sie einen Ordner-ID oder den Pfad zum Ausführen einer Sammlung</span><span class="sxs-lookup"><span data-stu-id="27482-166">Step 2: Use a folder ID or path to perform a targeted collection</span></span>

<span data-ttu-id="27482-p115">Nach dem Ausführen des Skripts, um eine Liste der Ordner IDs oder Pfade für einen bestimmten Benutzer zu erfassen den nächsten Schritt, fahren Sie mit der Sicherheit &amp; Compliance Center, und erstellen Sie eine neue Inhaltssuche, um einen bestimmten Ordner zu suchen. Verwenden Sie die `folderid:<folderid>` oder `path:<path>` -Eigenschaft in der Abfrage, die Sie konfigurieren im Feld Schlüsselwort Inhaltssuche (oder als Wert für den Parameter *ContentMatchQuery* , wenn Sie das Cmdlet **New-ComplianceSearch** verwenden). Sie können kombinieren, die `folderid` oder `path` Eigenschaft mit anderen Parameter suchen oder Bedingungen zu suchen. Wenn nur die `folderid` oder `path` Eigenschaft in der Abfrage, die Suche gibt alle Elemente im angegebenen Ordner zurück.</span><span class="sxs-lookup"><span data-stu-id="27482-p115">After you've run the script to collect a list of folder IDs or paths for a specific user, the next step to go to the Security &amp; Compliance Center and create a new Content Search to search a specific folder. You'll use the  `folderid:<folderid>` or  `path:<path>` property in the search query that you configure in the Content Search keyword box (or as the value for the  *ContentMatchQuery*  parameter if you use the **New-ComplianceSearch** cmdlet). You can combine the  `folderid` or  `path` property with other search parameters or search conditions. If you only include the  `folderid` or  `path` property in the query, the search will return all items located in the specified folder.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="27482-171">Mithilfe der `path` -Eigenschaft auf OneDrive Speicherorte durchsuchen wird nicht Mediendateien wie PNG, TIFF oder WAV-Dateien in den Suchergebnissen zurück.</span><span class="sxs-lookup"><span data-stu-id="27482-171">Using the  `path` property to search OneDrive locations won't return media files, such as .png, .tiff, or .wav files, in the search results.</span></span> 
  
1. <span data-ttu-id="27482-172">Wechseln Sie zu [https://protection.office.com](https://protection.office.com).</span><span class="sxs-lookup"><span data-stu-id="27482-172">Go to [https://protection.office.com](https://protection.office.com).</span></span>
    
2. <span data-ttu-id="27482-173">Melden Sie sich bei Office 365 mit dem Konto und die Anmeldeinformationen, die Sie zum Ausführen des Skripts in Schritt 1 verwendet.</span><span class="sxs-lookup"><span data-stu-id="27482-173">Sign in to Office 365 using the account and credentials that you used to run the script in Step 1.</span></span>
    
3. <span data-ttu-id="27482-174">Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **Inhaltssuche**, und klicken Sie dann auf **New** ![Symbol hinzufügen](media/O365-MDM-CreatePolicy-AddIcon.gif).</span><span class="sxs-lookup"><span data-stu-id="27482-174">In the left pane of the Security &amp; Compliance Center, click **Search &amp; investigation** \> **Content search**, and then click **New** ![Add icon](media/O365-MDM-CreatePolicy-AddIcon.gif).</span></span>
    
4. <span data-ttu-id="27482-p116">Geben Sie auf der Seite **Neue Suche** einen Namen für die Inhaltssuche ein. Dieser Name muss in der Organisation eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="27482-p116">On the **New search** page, type a name for the Content Search. This name has to be unique in your organization.</span></span> 
    
5. <span data-ttu-id="27482-177">Unter **Wo möchten Sie uns suchen**, führen Sie einen der folgenden basierend auf gibt an, ob Sie einen Postfachordner oder einem Website-Ordner suchen:</span><span class="sxs-lookup"><span data-stu-id="27482-177">Under **Where do you want us to look**, do one of the following, based on whether you're searching a mailbox folder or a site folder:</span></span>
    
    - <span data-ttu-id="27482-178">Klicken Sie auf **bestimmte Postfächer auswählen, um zu suchen** , und fügen Sie dasselbe Postfach, das Sie bei der Ausführung des Skripts in Schritt 1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="27482-178">Click **Choose specific mailboxes to search** and then add the same mailbox that you specified when you ran the script in Step 1.</span></span> 
    
      <span data-ttu-id="27482-179">Oder</span><span class="sxs-lookup"><span data-stu-id="27482-179">Or</span></span>
    
    - <span data-ttu-id="27482-180">Klicken Sie auf **Auswählen bestimmter Websites suchen** , um zu suchen, und fügen Sie die gleiche URL der Website, die Sie bei der Ausführung des Skripts in Schritt 1 angegeben.</span><span class="sxs-lookup"><span data-stu-id="27482-180">Click **Choose specific sites to search** to search and then add the same site URL that you specified when you ran the script in Step 1.</span></span> 
    
6. <span data-ttu-id="27482-181">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="27482-181">Click **Next**.</span></span>
    
7. <span data-ttu-id="27482-182">Fügen Sie in das Feld Stichwort auf der Seite **Was möchten Sie uns, suchen Sie nach** der `folderid:<folderid>` oder `path:<path>` -Wert, der durch das Skript in Schritt 1 zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="27482-182">In the keyword box on the **What do you want us to look for** page, paste the  `folderid:<folderid>` or  `path:<path>` value that was returned by the script in Step 1.</span></span> 
    
    <span data-ttu-id="27482-183">Beispielsweise wird die Abfrage im folgenden Screenshot für jedes Element im Unterordner "in den Ordner des Benutzers wiederherstellbare Elemente" Benutzerkontenverwaltung gesucht (der Wert der `folderid` -Eigenschaft für den Unterordner Benutzerkontenverwaltung ist Siehe die Bildschirmaufnahme in Schritt 1):</span><span class="sxs-lookup"><span data-stu-id="27482-183">For example, the query in the following screenshot will search for any item in the Purges subfolder in the user's Recoverable Items folder (the value of the `folderid` property for the Purges subfolder is shown in the screenshot in Step 1):</span></span>
    
    ![Fügen Sie der Folderid oder den Pfad in das Feld Schlüsselwort, der die Suchabfrage](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. <span data-ttu-id="27482-185">Klicken Sie auf **Suchen** , um die vorgesehene Sammlung Suche zu starten.</span><span class="sxs-lookup"><span data-stu-id="27482-185">Click **Search** to start the targeted collection search.</span></span> 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a><span data-ttu-id="27482-186">Beispiele für Suchabfragen für eine gezielte Sammlungen</span><span class="sxs-lookup"><span data-stu-id="27482-186">Examples of search queries for targeted collections</span></span>

<span data-ttu-id="27482-p117">Es folgen einige Beispiele für die Verwendung der `folderid` und `path` Eigenschaften in einer Suchanfrage an eine gezielte Auflistung ausführen. Beachten Sie, dass Platzhalter für verwendeten `folderid:<folderid>` und `path:<path>` um Speicherplatz einzusparen.</span><span class="sxs-lookup"><span data-stu-id="27482-p117">Here are some examples of using the  `folderid` and  `path` properties in a search query to perform a targeted collection. Note that placeholders are used for  `folderid:<folderid>` and  `path:<path>` to save space.</span></span> 
  
- <span data-ttu-id="27482-p118">In diesem Beispiel sucht drei verschiedenen Postfachordner. Ähnliche Abfragesyntax können verborgene Ordner in den Ordner eines Benutzers wiederherstellbare Elemente durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="27482-p118">This example searches three different mailbox folders. You could use similar query syntax to search the hidden folders in a user's Recoverable Items folder.</span></span>
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- <span data-ttu-id="27482-191">In diesem Beispiel sucht einen Postfachordner für Elemente, die einen exakten Ausdruck enthalten.</span><span class="sxs-lookup"><span data-stu-id="27482-191">This example searches a mailbox folder for items that contain an exact phrase.</span></span>
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- <span data-ttu-id="27482-192">In diesem Beispiel werden Dokumente, die die Buchstaben "NDA" im Titel enthalten einen Website-Ordner (und alle Unterordner) gesucht.</span><span class="sxs-lookup"><span data-stu-id="27482-192">This example searches a site folder (and any subfolders) for documents that contain the letters "NDA" in the title.</span></span>
    
  ```
  path:<path> AND filename:nda
  ```

- <span data-ttu-id="27482-193">In diesem Beispiel sucht einen Website-Ordner (und alle Unterordner) für Dokumente innerhalb eines Datumsbereichs geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="27482-193">This example searches a site folder (and any subfolder) for documents there were changed within a date range.</span></span>
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a><span data-ttu-id="27482-194">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="27482-194">More information</span></span>

<span data-ttu-id="27482-195">Berücksichtigen Sie die folgenden Punkte berücksichtigen, bei der mithilfe des Skripts in diesem Artikel vorgesehenen Websitesammlungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="27482-195">Keep the following things in mind when using the script in this article to perform targeted collections.</span></span>
  
- <span data-ttu-id="27482-p119">Das Skript entfernen keine Ordner in den Suchergebnissen. Damit in einige Ordner aufgeführt möglicherweise die Ergebnisse werden nicht durchsuchbaren (oder keine Elemente zurückgeben), da sie vom System generierte Inhalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="27482-p119">The script doesn't remove any folders from the results. So some folders listed in the results might be unsearchable (or return zero items) because they contain system-generated content.</span></span>
    
- <span data-ttu-id="27482-p120">Dieses Skript gibt nur Informationen für das Postfach des Benutzers primären Ordner zurück. Er wird nicht Informationen zu Ordnern im Archivpostfach des Benutzers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="27482-p120">This script only returns folder information for the user's primary mailbox. It doesn't return information about folders in the user's archive mailbox.</span></span>
    
- <span data-ttu-id="27482-p121">Bei der Suche Postfachordner, nur die angegebenen Ordner (identifiziert durch seine `folderid` -Eigenschaft) wird durchsucht. Unterordner wird nicht durchsucht werden. Um Unterordner zu suchen, müssen Sie die Ordner-ID für den Unterordner verwenden, die Sie suchen möchten.</span><span class="sxs-lookup"><span data-stu-id="27482-p121">When searching mailbox folders, only the specified folder (identified by its  `folderid` property) will be searched. Subfolders won't be searched. To search sub-folders, you need to use the  folder ID for the sub-folder that you want to search.</span></span> 
    
- <span data-ttu-id="27482-203">Bei der Suche-Ordner, den Ordner (identifiziert durch seine `path` Eigenschaft) und alle Unterordner werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="27482-203">When searching site folders, the folder (identified by its  `path` property) and all sub-folders will be searched.</span></span> 
    
- <span data-ttu-id="27482-p122">Wie bereits zuvor erwähnt, können keine `path` Eigenschaft zu suchenden Mediendateien wie PNG, TIFF oder WAV-Dateien, OneDrive Speicherorten gespeichert. Verwenden Sie eine andere [Websiteeigenschaft](keyword-queries-and-search-conditions.md#searchable-site-properties) , um für die Mediendateien in OneDrive-Ordner suchen.</span><span class="sxs-lookup"><span data-stu-id="27482-p122">As previously stated, you can't use  `path` property to search for media files, such as .png, .tiff, or .wav files, located in OneDrive locations. Use a different [site property](keyword-queries-and-search-conditions.md#searchable-site-properties) to search for media files in OneDrive folders.</span></span> 

- <span data-ttu-id="27482-p123">Wenn Sie die Ergebnisse einer Suche exportieren in dem angegebenen Sie nur die `folderid` -Eigenschaft in der Suchabfrage; Sie können auswählen, der erste Export option "alle Elemente, ausgenommen solche, die ein unbekanntes Format, haben werden verschlüsselt oder aus anderen Gründen indiziert wurden nicht." Alle Elemente im Ordner werden immer unabhängig von deren Indizierungsstatus exportiert werden, da die Ordner-ID immer indiziert ist.</span><span class="sxs-lookup"><span data-stu-id="27482-p123">When exporting the results of a search in which you only specified the `folderid` property in the search query, you can choose the first export option, "All items, excluding ones that have an unrecognized format, are encrypted, or weren't indexed for other reasons." All items in the folder will always be exported regardless of their indexing status because the folder ID is always indexed.</span></span>
