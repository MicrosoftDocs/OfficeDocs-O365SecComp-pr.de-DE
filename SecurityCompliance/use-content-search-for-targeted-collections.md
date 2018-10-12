---
title: Verwenden Sie Inhaltssuche in Office 365 für zielgerichtete Auflistungen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Verwenden Sie Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center gezielte Websitesammlungen ausführen. Eine Sammlung bedeutet, dass Sie davon überzeugt sind, dass auf eine Anfrage reagieren oder privilegierten Elemente in einem bestimmten Postfach oder einer Website Ordner befinden. Verwenden Sie das Skript in diesem Artikel erhalten Sie die Ordner-ID oder den Pfad für die bestimmten Ordner Postfach oder einer Website, die Sie suchen möchten.
ms.openlocfilehash: f4bb63a193a11e7467b3b296b2bdfa50657ae65a
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522286"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a>Verwenden Sie Inhaltssuche in Office 365 für zielgerichtete Auflistungen

Das Inhaltssuche-Feature in die Office 365-Sicherheit &amp; Compliance Center nicht zur Verfügung, eine direkte Weise in der Benutzeroberfläche zum Durchsuchen bestimmter Ordner in Exchange-Postfächern oder SharePoint und OneDrive for Business-Websites. Es ist jedoch möglich, bestimmte Ordner (einen zielgerichteten Collection bezeichnet) zu suchen, indem Sie die Ordner-ID oder den Pfad in die eigentliche Suche-Abfragesyntax. Verwenden zum Ausführen einer Sammlung Inhaltssuche ist nützlich, wenn Sie davon überzeugt sind, dass auf eine Anfrage reagieren oder privilegierten Elemente in einem bestimmten Postfach oder einer Website Ordner befinden. Das Skript können in diesem Artikel Sie um die Ordner-ID für Postfachordner oder der Pfad zum Ordner auf einer SharePoint- und OneDrive for Business-Website zu erhalten. Anschließend können Sie die Ordner-ID oder den Pfad in einer Suchabfrage zurückzugebenden Elemente im Ordner gespeichert.
  
## <a name="before-you-begin"></a>Vorbemerkung

- Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center zum Ausführen des Skripts in Schritt 1. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
    
    Darüber hinaus müssen Sie die Rolle des E-Mail-Empfänger in Ihrer Exchange Online-Organisation zugewiesen werden. Dies ist erforderlich, um das Cmdlet **Get-mailboxfolderstatistics abrufen** ausgeführt werden, die in das Skript in Schritt 1 enthalten ist. Standardmäßig ist die E-Mail-Empfänger-Rolle zu Rollengruppen Organization Management und Recipient Management in Exchange Online zugewiesen. Weitere Informationen zum Zuweisen von Berechtigungen in Exchange Online finden Sie unter [Manage Role Gruppenmitglieder](https://go.microsoft.com/fwlink/p/?linkid=692102). Sie könnten auch erstellen eine benutzerdefinierten Rollengruppe, die E-Mail-Empfänger Rolle zuweisen, und fügen Sie die Mitglieder, die zum Ausführen des Skripts in Schritt 1 müssen. Weitere Informationen finden Sie unter [Rollengruppen verwalten](https://go.microsoft.com/fwlink/p/?linkid=730688).
    
- Jedes Mal, wenn Sie das Skript in Schritt 1 ausführen, wird eine neue remote-PowerShell-Sitzung erstellt. So können Sie Sie alle remote PowerShell Sessions zur Verfügung. Um dies zu verhindern, können Sie den folgenden Befehl zum Trennen von aktiven remote PowerShell-Sitzungen ausführen.
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Das Skript enthält minimale Fehlerbehandlung. Der primäre Zweck des Skripts ist um schnell zeigt eine Liste der Postfachordner IDs oder Website Pfade, die in der Syntax Search-Abfrage ein Inhaltssuche zur Durchführung einer Sammlung verwendet werden können.
    
- Das Beispielskript bereitgestellt, die in diesem Thema wird unter keinem standard Support-Programm von Microsoft oder der Dienst nicht unterstützt. Das Beispielskript wird wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt alle konkludente Garantien einschließlich, aber nicht beschränkt auf konkludente Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck. Das gesamte Risiko aus der Verwendung oder der Leistung der Beispielskript und der Dokumentation liegt bei Ihnen. In keinem Fall muss Microsoft, seine Autoren oder ein Benutzer die Erstellung, Produktion oder Übermittlung der Skripts else beteiligt für Schäden jeglicher Art (einschließlich, aber nicht beschränkt auf Schäden für den Verlust von Gewinn Business, Business Unterbrechung, Verlust von Unternehmensinformationen, Folge- oder) aus der Verwendung des oder der Fehler beim Verwenden der Beispielskripts oder der Dokumentation, haftbar gemacht werden, auch wenn Microsoft die Möglichkeit solcher Schäden hingewiesen wurde.
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a>Schritt 1: Führen Sie das Skript aus, um eine Liste der Ordner für ein Postfach oder Website abrufen

Das Skript, das Sie in dieser ersten Schritt ausführen, wird eine Liste der Postfachordner oder SharePoint oder OneDrive for Business-Ordner und die entsprechenden Ordner-ID oder Pfad für jeden Ordner zurück. Wenn Sie dieses Skript ausführen, fordert es Sie für die folgenden Informationen.
  
- **E-Mail-Adresse oder Website-URL** Geben Sie eine e-Mail-Adresse der Verwaltungsberechtigte zum Zurückgeben einer Liste der Exchange-Postfachordner und IDs Faltung. Oder geben Sie die URL für eine SharePoint-Website oder eine OneDrive for Business-Website, um eine Liste der Pfade für die angegebene Website zurückzugeben. Es folgen einige Beispiele: 
    
  - **Exchange** - stacig@contoso.onmicrosoft.com 
    
  - **SharePoint** - https://contoso.sharepoint.com/sites/marketing 
    
  - **OneDrive für Unternehmen** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com 
    
- **Ihre Anmeldeinformationen** – das Skript wird unter Verwendung Ihrer Anmeldeinformationen für die Verbindung zu Exchange Online und die Sicherheit &amp; Compliance Center mit remote-PowerShell. Wie bereits erklärt müssen Sie die entsprechenden Berechtigungen zum erfolgreichen Ausführen dieses Skripts zugewiesen.
    
Zeigt eine Liste der Postfachordner oder Pfadnamen Website:
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `GetFolderSearchParameters.ps1`.
    
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
          # Create a Complinace Search Action and wait for it to complete. The folders will be listed in the .Results parameter
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

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.
    
3. Führen Sie das Skript; Zum Beispiel:
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. Geben Sie die Informationen, der das Skript für aufgefordert werden.
    
    Das Skript zeigt eine Liste der Postfachordnern oder Site-Ordner für den angegebenen Benutzer. Lassen Sie dieses Fenster öffnen, damit Sie einen Ordnernamen-ID oder den Pfad zu kopieren und fügen Sie ihn in eine Suchabfrage in Schritt2 können.
    
    > [!TIP]
    > Statt eine Liste der Ordner auf dem Computerbildschirm angezeigt, können Sie die Ausgabe des Skripts in eine Textdatei umgeleitet. Diese Datei wird in den Ordner gespeichert werden, in das Skript gespeichert ist. Das Skript Ausgabe in eine Textdatei umleiten möchten, führen Sie beispielsweise den folgenden Befehl in Schritt 3: `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` und klicken Sie dann einen Ordner-ID oder den Pfad aus der Datei in eine Suchabfrage verwenden kopieren können.
  
### <a name="script-output-for-mailbox-folders"></a>Ausgabe des Skripts für Postfachordner

Wenn Sie Postfachordner IDs erhalten, müssen Sie das Skript stellt eine Verbindung mit Exchange Online mithilfe von remote-PowerShell, wird das Cmdlet **Get-MailboxFolderStatisics** ausgeführt, und klicken Sie dann zeigt die Liste der Ordner aus dem angegebenen Postfach. Für jeden Ordner im Postfach zeigt das Skript den Namen des Ordners in der Spalte **FolderPath** und die Ordner-ID in der Spalte **FolderQuery** . Darüber hinaus fügt das Skript das Präfix des **FolderId** (die den Namen der Postfach-Eigenschaft ist) der Ordner-ID. Da die **Folderid** -Eigenschaft einer Eigenschaft durchsuchbar ist, verwenden Sie `folderid:<folderid>` bei einer Suchabfrage in Schritt2, um den Ordner zu suchen. 
  
Es folgt ein Beispiel der Ausgabe von dem Skript für Postfachordner zurückgegeben.
  
![Beispiel für die Liste der Postfachordner und Ordner vom Skript zurückgegebenen IDs](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
Das Beispiel in Schritt2 zeigt die Abfrage für die Suche Unterordner "bereinigt" in den Ordner des Benutzers wiederherstellbare Elemente verwendet.
  
### <a name="script-output-for-site-folders"></a>Ausgabe des Skripts für Websiteordner

Wenn Sie Pfade aus SharePoint oder OneDrive for Business-Websites erhalten, müssen Sie das Skript stellt eine Verbindung mit der Sicherheit &amp; Compliance Center mithilfe von remote PowerShell erstellt eine neue Inhaltssuche, die durchsucht der Website für die Ordner, und klicken Sie dann eine Liste der Ordner angezeigt befindet sich in der angegebenen Website. Das Skript werden die Namen der einzelnen Ordner angezeigt und die URL der Ordner das Präfix des **Pfad** (bei dem es sich um den Namen der Websiteeigenschaft handelt) hinzugefügt. Da die **Path** -Eigenschaft einer Eigenschaft durchsuchbar ist, verwenden Sie `path:<path>` bei einer Suchabfrage in Schritt2, um den Ordner zu suchen. 
  
Es folgt ein Beispiel der Ausgabe von dem Skript für Websiteordner zurückgegeben.
  
![Beispiel für die Liste der Pfadnamen für Websiteordner zurückgegeben, die von dem Skript](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-path-to-perform-a-targeted-collection"></a>Schritt 2: Verwenden Sie einen Ordner-ID oder den Pfad zum Ausführen einer Sammlung

Nach dem Ausführen des Skripts, um eine Liste der Ordner IDs oder Pfade für einen bestimmten Benutzer zu erfassen den nächsten Schritt, fahren Sie mit der Sicherheit &amp; Compliance Center, und erstellen Sie eine neue Inhaltssuche, um einen bestimmten Ordner zu suchen. Verwenden Sie die `folderid:<folderid>` oder `path:<path>` -Eigenschaft in der Abfrage, die Sie konfigurieren im Feld Schlüsselwort Inhaltssuche (oder als Wert für den Parameter *ContentMatchQuery* , wenn Sie das Cmdlet **New-ComplianceSearch** verwenden). Sie können kombinieren, die `folderid` oder `path` Eigenschaft mit anderen Parameter suchen oder Bedingungen zu suchen. Wenn nur die `folderid` oder `path` Eigenschaft in der Abfrage, die Suche gibt alle Elemente im angegebenen Ordner zurück. 
  
> [!NOTE]
> Mithilfe der `path` -Eigenschaft auf OneDrive Speicherorte durchsuchen wird nicht Mediendateien wie PNG, TIFF oder WAV-Dateien in den Suchergebnissen zurück. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit dem Konto und die Anmeldeinformationen, die Sie zum Ausführen des Skripts in Schritt 1 verwendet.
    
3. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Suche &amp; Untersuchung** \> **Inhaltssuche**, und klicken Sie dann auf **New** ![Symbol hinzufügen](media/O365-MDM-CreatePolicy-AddIcon.gif).
    
4. Geben Sie auf der Seite **Neue Suche** einen Namen für die Inhaltssuche ein. Dieser Name muss in der Organisation eindeutig sein. 
    
5. Klicken Sie unter **Wo möchten Sie uns suchen**, führen Sie einen der folgenden, abhängig davon, ob Ihre Suche in einem Postfachordner oder einen Website-Ordner:
    
    - Klicken Sie auf **bestimmte Postfächer auswählen, um zu suchen** , und fügen Sie dasselbe Postfach, das Sie bei der Ausführung des Skripts in Schritt 1 angegeben. 
    
      Oder
    
    - Klicken Sie auf **Auswählen bestimmter Websites suchen** , um zu suchen, und fügen Sie die gleiche URL der Website, die Sie bei der Ausführung des Skripts in Schritt 1 angegeben. 
    
6. Klicken Sie auf **Weiter**.
    
7. Fügen Sie in das Feld Stichwort auf der Seite **Was möchten Sie uns, suchen Sie nach** der `folderid:<folderid>` oder `path:<path>` -Wert, der durch das Skript in Schritt 1 zurückgegeben wurde. 
    
    Beispielsweise wird die Abfrage im folgenden Screenshot für jedes Element im Unterordner "in den Ordner des Benutzers wiederherstellbare Elemente" Benutzerkontenverwaltung gesucht (der Wert der `folderid` -Eigenschaft für den Unterordner Benutzerkontenverwaltung ist Siehe die Bildschirmaufnahme in Schritt 1):
    
    ![Fügen Sie der Folderid oder den Pfad in das Feld Schlüsselwort, der die Suchabfrage](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. Klicken Sie auf **Suchen** , um die vorgesehene Sammlung Suche zu starten. 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a>Beispiele für Suchabfragen für eine gezielte Sammlungen

Es folgen einige Beispiele für die Verwendung der `folderid` und `path` Eigenschaften in einer Suchanfrage an eine gezielte Auflistung ausführen. Beachten Sie, dass Platzhalter für verwendeten `folderid:<folderid>` und `path:<path>` um Speicherplatz einzusparen. 
  
- In diesem Beispiel sucht drei verschiedenen Postfachordner. Ähnliche Abfragesyntax können verborgene Ordner in den Ordner eines Benutzers wiederherstellbare Elemente durchsuchen.
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- In diesem Beispiel sucht einen Postfachordner für Elemente, die einen exakten Ausdruck enthalten.
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- In diesem Beispiel werden Dokumente, die die Buchstaben "NDA" im Titel enthalten einen Website-Ordner (und alle Unterordner) gesucht.
    
  ```
  path:<path> AND filename:nda
  ```

- In diesem Beispiel sucht einen Website-Ordner (und alle Unterordner) für Dokumente innerhalb eines Datumsbereichs geändert wurden.
    
  ```
  path:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a>Weitere Informationen

Berücksichtigen Sie die folgenden Punkte berücksichtigen, bei der mithilfe des Skripts in diesem Artikel und Ausführen von Auflistungen Ziel.
  
- Das Skript entfernen keine Ordner in den Suchergebnissen. Damit in einige Ordner aufgeführt möglicherweise die Ergebnisse werden nicht durchsuchbaren (oder keine Elemente zurückgeben), da sie vom System generierte Inhalte enthalten.
    
- Dieses Skript gibt nur Informationen für das Postfach des Benutzers primären Ordner zurück. Er wird nicht Informationen zu Ordnern im Archivpostfach des Benutzers zurückgegeben.
    
- Bei der Suche Postfachordner, nur die angegebenen Ordner (identifiziert durch seine `folderid` -Eigenschaft) wird durchsucht. Unterordner wird nicht durchsucht werden. Um Unterordner zu suchen, müssen Sie verwenden die `folderid` für den Unterordner, die Sie suchen möchten. 
    
- Bei der Suche-Ordner, den Ordner (identifiziert durch seine `path` Eigenschaft) und alle Unterordner werden durchsucht. 
    
- Wie bereits zuvor erwähnt, können keine `path` Eigenschaft zu suchenden Mediendateien wie PNG, TIFF oder WAV-Dateien, OneDrive Speicherorten gespeichert. Verwenden Sie eine andere [Websiteeigenschaft](keyword-queries-and-search-conditions.md#searchable-site-properties) , um für die Mediendateien in OneDrive-Ordner suchen. 
