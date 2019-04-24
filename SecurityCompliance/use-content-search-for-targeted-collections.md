---
title: Verwenden der Inhaltssuche in Office 365 für zielgerichtete Auflistungen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: MOE150
ms.assetid: e3cbc79c-5e97-43d3-8371-9fbc398cd92e
description: Verwenden Sie die Inhaltssuche im Security & Compliance Center, um zielgerichtete Auflistungen auszuführen. Eine zielgerichtete Sammlung stellt sicher, dass Elemente, die auf eine Groß-/Kleinschreibung oder privilegierte Elemente reagieren, sich in einem bestimmten Postfach oder Websiteordner befinden. Verwenden Sie das Skript in diesem Artikel, um die Ordner-ID oder den Pfad für die bestimmten Postfach-oder Websiteordner abzurufen, die Sie durchsuchen möchten.
ms.openlocfilehash: 3d9a82926a08b3f7f1f245146e70d79617e7a413
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264012"
---
# <a name="use-content-search-in-office-365-for-targeted-collections"></a>Verwenden der Inhaltssuche in Office 365 für zielgerichtete Auflistungen

Die Inhaltssuche im Office 365 Security &amp; Compliance Center bietet keine direkte Möglichkeit zur Suche bestimmter Ordner in Exchange-Postfächern oder SharePoint-und OneDrive für Business-Websites. Es ist jedoch möglich, bestimmte Ordner (als *Zielsammlung*bezeichnet) durchsuchen, indem Sie die Ordner-ID-Eigenschaft für die Eigenschaft e-Mail oder Pfad (DocumentLink) für Websites in der tatsächlichen Suchabfrage Syntax angeben. Die Verwendung der Inhaltssuche zum Durchführen einer zielgerichteten Sammlung ist nützlich, wenn Sie sicher sind, dass Elemente, die auf eine Groß-/Kleinschreibung reagieren oder privilegierte Elemente in einem bestimmten Postfach oder Websiteordner befinden. Sie können das Skript in diesem Artikel verwenden, um die Ordner-ID für Postfachordner oder den Pfad (DocumentLink) für Ordner auf einer SharePoint-und OneDrive for Business-Website abzurufen. Dann können Sie die Ordner-ID oder den Pfad in einer Suchabfrage verwenden, um Elemente im Ordner zurückzugeben.

> [!NOTE]
> Zum Zurückgeben von Inhalten in einem Ordner in einer SharePoint-oder OneDrive for Business-Website verwendet das Skript in diesem Thema die verwaltete DocumentLink-Eigenschaft anstelle der Path-Eigenschaft. Die DocumentLink-Eigenschaft ist robuster als die Path-Eigenschaft, da Sie den gesamten Inhalt in einem Ordner zurückgibt, während die Path-Eigenschaft keine Mediendateien zurückgibt.

## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen Mitglied der eDiscovery-Manager-Rollengruppe im Security &amp; Compliance Center sein, um das Skript in Schritt 1 ausführen zu können. Weitere Informationen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen](assign-ediscovery-permissions.md).
    
    Darüber hinaus müssen Sie die Rolle e-Mail-Empfänger in Ihrer Exchange Online-Organisation zugewiesen werden. Dies ist erforderlich, um das Cmdlet **Get-MailboxFolderStatistics** auszuführen, das im Skript in Schritt 1 enthalten ist. Standardmäßig wird die Rolle "e-Mail-Empfänger" den Rollengruppen "Organisationsverwaltung" und "Empfängerverwaltung" in Exchange Online zugewiesen. Weitere Informationen zum Zuweisen von Berechtigungen in Exchange Online finden Sie unter [Verwalten von Rollengruppenmitgliedern](https://go.microsoft.com/fwlink/p/?linkid=692102). Sie können auch eine benutzerdefinierte Rollengruppe erstellen, ihr die Rolle e-Mail-Empfänger zuweisen und dann die Mitglieder hinzufügen, die das Skript in Schritt 1 ausführen müssen. Weitere Informationen finden Sie unter [Verwalten von Rollengruppen](https://go.microsoft.com/fwlink/p/?linkid=730688).
    
- Jedes Mal, wenn Sie das Skript in Schritt 1 ausführen, wird eine neue Remote-PowerShell-Sitzung erstellt. Sie können also alle für Sie verfügbaren Remote-PowerShell-Sitzungen verwenden. Um dies zu verhindern, können Sie den folgenden Befehl ausführen, um die Verbindung mit den aktiven Remote-PowerShell-Sitzungen zu trennen.
    
  ```
  Get-PSSession | Remove-PSSession
  ```

    Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
- Das Skript enthält eine minimale Fehlerbehandlung. Der Hauptzweck des Skripts besteht darin, schnell eine Liste von Postfachordner-IDs oder Website Pfaden anzuzeigen, die in der Suchabfrage Syntax einer Inhaltssuche verwendet werden können, um eine gezielte Sammlung auszuführen.
    
- Das Beispielskript in diesem Thema wird unter keinem Microsoft Standard-Support Programm oder-Dienst unterstützt. Das Beispielskript wird ohne Gewähr bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Das gesamte Risiko, das sich aus der Verwendung oder Leistung des Beispielskripts und der Dokumentation ergibt, liegt bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.
  
## <a name="step-1-run-the-script-to-get-a-list-of-folders-for-a-mailbox-or-site"></a>Schritt 1: Ausführen des Skripts zum Abrufen einer Liste von Ordnern für ein Postfach oder eine Website

Das Skript, das Sie in diesem ersten Schritt ausführen, gibt eine Liste der Postfachordner oder SharePoint-und OneDrive für Business-Ordner sowie die entsprechende Ordner-ID oder den entsprechenden Pfad für jeden Ordner zurück. Wenn Sie dieses Skript ausführen, werden Sie aufgefordert, die folgenden Informationen einzugeben.
  
- **E-Mail-Adresse oder Website-URL** Geben Sie eine e-Mail-Adresse der Depotbank ein, um eine Liste der Exchange-Postfachordner und Ordner-IDs zurückzugeben. Oder geben Sie die URL für eine SharePoint-Website oder eine OneDrive for Business-Website ein, um eine Liste der Pfade für die angegebene Website zurückzugeben. Im Folgenden finden Sie einige Beispiele: 
    
  - **Exchange** -stacig@contoso.onmicrosoft.com 
    
  - **Share** - https://contoso.sharepoint.com/sites/marketing 
    
  - **OneDrive for Business** - https://contoso-my.sharepoint.com/personal/stacig_contoso_onmicrosoft_com 
    
- **Ihre Benutzeranmeldeinformationen** – das Skript verwendet Ihre Anmeldeinformationen zum Herstellen einer Verbindung mit Exchange Online und dem Security _AMP_ Compliance Center mit Remote-PowerShell. Wie bereits erläutert, müssen Sie die entsprechenden Berechtigungen für die erfolgreiche Ausführung dieses Skripts zugewiesen haben.
    
So zeigen Sie eine Liste von Postfachordnern oder Website documentlink (Pfad) an
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `GetFolderSearchParameters.ps1`.
    
  ```
  #########################################################################################################
  # This PowerShell script will prompt you for:                             #
  #    * Admin credentials for a user who can run the Get-MailboxFolderStatistics cmdlet in Exchange    #
  #      Online and who is an eDiscovery Manager in the Security & Compliance Center.           #
  # The script will then:                                           #
  #    * If an email address is supplied: list the folders for the target mailbox.          #
  #    * If a SharePoint or OneDrive for Business site is supplied: list the documentlinks (folder paths) #
  #    * for the site.                                                                                  #
  #    * In both cases, the script supplies the correct search properties (folderid: or documentlink:)  #
  #      appended to the folder ID or documentlink to use in a Content Search.              #
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
  # Authenticate with Exchange Online and the Security & Compliance Center (Exchange Online Protection - EOP)
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
      # Authenticate with the Security & Compliance Center
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
              Write-Host "DocumentLink:""$rawUrl"""
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
    
3. Führen Sie das Skript aus; Zum Beispiel:
    
      ```
      .\GetFolderSearchParameters.ps1
      ```

4. Geben Sie die Informationen ein, für die Sie das Skript auffordert.
    
    Das Skript zeigt eine Liste der Postfachordner oder Websiteordner für den angegebenen Benutzer an. Lassen Sie dieses Fenster geöffnet, damit Sie eine Ordner-ID oder einen documentlink-Namen kopieren und in eine Suchabfrage in Schritt 2 einfügen können.
    
    > [!TIP]
    > Anstatt eine Liste von Ordnern auf dem Bildschirm anzuzeigen, können Sie die Ausgabe des Skripts in eine Textdatei umleiten. Diese Datei wird in dem Ordner gespeichert, in dem sich das Skript befindet. Wenn Sie beispielsweise die Skriptausgabe in eine Textdatei umleiten möchten, führen Sie den folgenden Befehl in `.\GetFolderSearchParameters.ps1 > StacigFolderIds.txt` Schritt 3 aus: dann können Sie eine Ordner-ID oder documentlink aus der Datei kopieren, um Sie in einer Suchabfrage zu verwenden.
  
### <a name="script-output-for-mailbox-folders"></a>Skriptausgabe für Postfachordner

Wenn Sie Postfachordner-IDs erhalten, stellt das Skript mithilfe der Remote-PowerShell eine Verbindung mit Exchange Online her, führt das Cmdlet **Get-MailboxFolderStatisics** aus und zeigt dann die Liste der Ordner aus dem angegebenen Postfach an. Für jeden Ordner im Postfach zeigt das Skript den Namen des Ordners in der Spalte **folderPath** und die Ordner-ID in der Spalte **FolderQuery** an. Darüber hinaus fügt das Skript das Präfix der **Ordner** -ID (die den Namen der Postfacheigenschaft ist) zur Ordner Kennung hinzu. Da es sich bei der **Folder** -Eigenschaft um eine durchsuchbare Eigenschaft `folderid:<folderid>` handelt, verwenden Sie in einer Suchabfrage in Schritt 2, um diesen Ordner zu durchsuchen. 

> [!IMPORTANT]
> Das Skript in diesem Artikel enthält die Codierungslogik, mit der die von **Get-MailboxFolderStatistics** zurückgegebenen 64-Zeichen-Ordner-ID-Werte in dasselbe 48-Zeichenformat konvertiert werden, das für die Suche indiziert ist. Wenn Sie das Cmdlet **Get-MailboxFolderStatistics** in PowerShell ausführen, um eine Ordner-ID zu erhalten (anstatt das Skript in diesem Artikel auszuführen), schlägt eine Suchabfrage fehl, die diesen Ordner-ID-Wert verwendet. Sie müssen das Skript ausführen, um die ordnungsgemäß formatierten Ordner-IDs abzurufen, die in einer Inhaltssuche verwendet werden können.
  
Hier sehen Sie ein Beispiel der Ausgabe, die vom Skript für Postfachordner zurückgegeben wird.
  
![Beispiel für die Liste der Postfachordner und Ordner-IDs, die vom Skript zurückgegeben werden](media/cd739207-eb84-4ebf-a03d-703f3d3a797d.png)
  
Das Beispiel in Schritt 2 zeigt die Abfrage, die zum Durchsuchen des Unterordners "Purges" im Ordner "Wiederherstellbare Elemente" des Benutzers verwendet wird.
  
### <a name="script-output-for-site-folders"></a>Skriptausgabe für Websiteordner

Wenn Sie den Pfad der **documentlink** -Eigenschaft aus SharePoint-oder OneDrive for Business-Websites erhalten, stellt das Skript eine Verbindung mit dem Security _AMP_ Compliance Center mithilfe von Remote-PowerShell her, erstellt eine neue Inhaltssuche, die die Website nach Ordnern durchsucht, und zeigt dann eine Liste der Ordner an der angegebenen Website an. Das Skript zeigt den Namen der einzelnen Ordner an und fügt der Ordner-URL das Präfix **documentlink** hinzu. Da die **documentlink** -Eigenschaft eine durchsuchbare Eigenschaft ist, verwenden `documentlink:<path>` Sie Property: Value-Paar in einer Suchabfrage in Schritt 2, um diesen Ordner zu durchsuchen. 
  
NachFolgend finden Sie ein Beispiel der Ausgabe, die vom Skript für Websiteordner zurückgegeben wird.
  
![Beispiel für die Liste der documentlink-Namen für Websiteordner, die vom Skript zurückgegeben werden](media/519e8347-7365-4067-af78-96c465dc3d15.png)
  
## <a name="step-2-use-a-folder-id-or-documentlink-to-perform-a-targeted-collection"></a>Schritt 2: Verwenden einer Ordner-ID oder documentlink zum Ausführen einer Zielsammlung

Nachdem Sie das Skript ausgeführt haben, um eine Liste der Ordner-IDs oder documentlinks für einen bestimmten Benutzer zu sammeln, gehen Sie als nächster Schritt zum Security & Compliance Center und erstellen eine neue Inhaltssuche, um einen bestimmten Ordner zu durchsuchen. Sie verwenden das `folderid:<folderid>` -oder `documentlink:<path>` -Eigenschaft:-Wert-Paar in der Suchabfrage, die Sie im Schlüsselwort Feld für die Inhaltssuche konfigurieren (oder als Wert für den *ContentMatchQuery* -Parameter, wenn Sie das **New-ComplianceSearch-** Cmdlet verwenden). Sie können die `folderid` or `documentlink` -Eigenschaft mit anderen Suchparametern oder Suchbedingungen kombinieren. Wenn Sie die `folderid` or `documentlink` -Eigenschaft nur in die Abfrage einbeziehen, gibt die Suche alle Elemente zurück, die sich im angegebenen Ordner befinden. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit dem Konto und den Anmeldeinformationen an, die Sie zum Ausführen des Skripts in Schritt 1 verwendet haben.
    
3. Klicken Sie im linken Bereich des Security & Compliance Centers auf **Such** \> **Inhaltssuche**, und klicken Sie **** ![dann auf neues](media/O365-MDM-CreatePolicy-AddIcon.gif)Symbol hinzufügen.
    
4. Geben Sie auf der Seite **Neue Suche** einen Namen für die Inhaltssuche ein. Dieser Name muss in der Organisation eindeutig sein. 
    
5. Führen **Sie unter wo sollen wir suchen**, eine der folgenden Aktionen aus, je nachdem, ob Sie einen Postfachordner oder einen Websiteordner durchsuchen:
    
    - Klicken Sie auf **bestimmte Postfächer auswählen, um zu suchen** , und fügen Sie dann das gleiche Postfach hinzu, das Sie beim Ausführen des Skripts in Schritt 1 angegeben haben. 
    
      Oder
    
    - Klicken Sie auf **bestimmte Websites auswählen** , um die Suche durch zu durchsuchen, und fügen Sie dann die gleiche Website-URL hinzu, die Sie beim Ausführen des Skripts in Schritt 1 angegeben haben. 
    
6. Klicken Sie auf **Weiter**.
    
7. Fügen Sie im Feld Stichwort auf der Seite **Was möchten Sie uns** suchen nach den `folderid:<folderid>` oder `documentlink:<path>` -Wert ein, der von dem Skript in Schritt 1 zurückgegeben wurde. 
    
    Beispielsweise wird die Abfrage im folgenden Screenshot nach einem beliebigen Element im Unterordner "Purges" im Ordner "Wiederherstellbare Elemente" des Benutzers suchen (der Wert `folderid` der-Eigenschaft für den Unterordner purges wird im Screenshot in Schritt 1 angezeigt):
    
    ![Fügen Sie die Ordner-oder documentlink in das Stichwortfeld der Suchabfrage ein.](media/84057516-b663-48a4-a78f-8032a8f8da80.png)
  
8. Klicken Sie auf **Suchen** , um die gezielte Sammlungs Suche zu starten. 
  
### <a name="examples-of-search-queries-for-targeted-collections"></a>Beispiele für Suchabfragen für zielgerichtete Auflistungen

Im folgenden finden Sie einige Beispiele für `folderid` die `documentlink` Verwendung der Eigenschaften und in einer Suchabfrage, um eine zielgerichtete Sammlung auszuführen. Beachten Sie, dass Platzhalter verwendet `folderid:<folderid>` werden `documentlink:<path>` , um Platz zu sparen. 
  
- In diesem Beispiel werden drei verschiedene Postfachordner durchsucht. Sie können eine ähnliche Abfragesyntax verwenden, um die verborgenen Ordner im Ordner "Wiederherstellbare Elemente" eines Benutzers zu durchsuchen.
    
  ```
  folderid:<folderid> OR folderid:<folderid> OR folderid:<folderid>
  ```

- In diesem Beispiel wird ein Postfachordner nach Elementen durchsucht, die einen exakten Ausdruck enthalten.
    
  ```
  folderid:<folderid> AND "Contoso financial results"
  ```

- In diesem Beispiel wird ein Websiteordner (und alle Unterordner) nach Dokumenten durchsucht, die die Buchstaben "NDA" im Titel enthalten.
    
  ```
  documentlink:<path> AND filename:nda
  ```

- In diesem Beispiel wird ein Websiteordner (und ein beliebiger Unterordner) nach Dokumenten gesucht, die in einem Datumsbereich geändert wurden.
    
  ```
  documentlink:<path> AND (lastmodifiedtime>=01/01/2017 AND lastmodifiedtime<=01/21/2017)
  ```
  
## <a name="more-information"></a>Weitere Informationen

Beachten Sie beim Verwenden des Skripts in diesem Artikel die folgenden Punkte, um zielgerichtete Auflistungen auszuführen.
  
- Das Skript entfernt keine Ordner aus den Ergebnissen. Daher sind einige in den Ergebnissen aufgeführte Ordner möglicherweise nicht durchsuchbar (oder geben keine Elemente zurück), da Sie vom System generierte Inhalte enthalten.
    
- Dieses Skript gibt nur Ordnerinformationen für das primäre Postfach des Benutzers zurück. Es werden keine Informationen zu Ordnern im Archivpostfach des Benutzers zurückgegeben.
    
- Beim Durchsuchen von Postfachordnern wird nur der angegebene Ordner durch `folderid` sucht; Unterordner werden nicht durchsucht. Zum Durchsuchen von Unterordnern müssen Sie die Ordner-ID für den Unterordner verwenden, den Sie durchsuchen möchten. 
    
- Beim Durchsuchen von Websiteordnern wird der durch die `documentlink` Eigenschaft identifizierte Ordner und alle Unterordner durchsucht. 
    
- Beim Exportieren der Ergebnisse einer Suche, in der Sie die `folderid` Eigenschaft nur in der Suchabfrage angegeben haben, können Sie die erste Exportoption auswählen, "alle Elemente, ausgenommen diejenigen, die ein unbekanntes Format aufweisen, verschlüsselt sind oder aus anderen Gründen nicht indiziert wurden." Alle Elemente im Ordner werden immer unabhängig von Ihrem Indizierungsstatus exportiert, da die Ordner-ID immer indiziert ist.
