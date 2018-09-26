---
title: Erstellen, Berichten über und Löschen mehrerer Inhaltssuchen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: Erfahren Sie, wie zum Automatisieren von Aufgaben wie erstellen Suchen und Ausführen von Berichten über PowerShell-Skripts in der Office 365-Sicherheit Inhaltssuche &amp; Compliance Center.
ms.openlocfilehash: a32c003dfd9a27ea8c38b29b31001b612368bc4a
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038138"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a>Erstellen, Berichten über und Löschen mehrerer Inhaltssuchen

 Schnell erstellen und reporting Discovery Suchvorgänge ist häufig ein wichtiger Schritt in eDiscovery und Untersuchungen, wenn Sie über die zugrunde liegenden Daten, und der Umfang und die Qualität der Ihre Suchanfragen informieren möchten. Zur einfacheren dazu, die Sicherheit &amp; Compliance Center bietet eine Reihe von Windows PowerShell-Cmdlets zeitaufwendige Inhaltssuche Aufgaben automatisieren. Diese Skripts bieten eine schnelle und problemlose Möglichkeit, eine Reihe von Suchvorgänge erstellen, und führen Sie Berichte der geschätzten Suchergebnisse, die Ihnen bei der Bestimmung der Menge der betreffenden Daten helfen kann. Die Skripts können auch verschiedene Versionen von Suchvorgängen, die Ergebnisse verglichen werden soll, die jeweils erzeugt erstellen. Diese Skripts können Sie schnell und effizient zu identifizieren und ausgemerzte Ihrer Daten. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center in diesem Thema ausführen, die Skripts, die beschrieben werden. 
    
- Um eine Liste der URLs für die OneDrive for Business-Websites in Ihrer Organisation zu sammeln, die Sie in der CSV-Datei in Schritt 1 hinzufügen können, finden Sie unter [Erstellen einer Liste der OneDrive Positionen in Ihrer Organisation](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a). 
    
- Achten Sie darauf, dass Sie alle Dateien zu speichern, die Sie in diesem Thema, um im gleichen Ordner erstellen. Die wird zum Ausführen der Skripts erleichtern.
    
- Die Skripts enthalten minimale Fehlerbehandlung. Ihre primäre Zweck ist schnell erstellen, melden und mehrere Content-Suche löschen.
    
- Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a>Schritt 1: Erstellen einer CSV-Datei, die Informationen zu der Suchvorgänge, die Sie ausführen möchten, enthält

Die durch Trennzeichen getrennten Werten (CSV)-Datei, die Sie in diesem Schritt erstellen enthält eine Zeile für jeden Benutzer, den suchen möchten. Sie können das Postfach des Benutzers Exchange Online (einschließlich Archivpostfach, wenn es aktiviert ist) und ihre OneDrive for Business-Website suchen. Oder Sie können nur das Postfach oder die OneDrive for Business-Website suchen. Sie können auch eine andere Website in Ihrer SharePoint Online-Organisation suchen. Das Skript, das Sie in Schritt 3 ausführen, wird eine separate Suche für jede Zeile in der CSV-Datei erstellt. 
  
1. Kopieren Sie und fügen Sie den folgenden Text in eine TXT-Datei mit dem Editor. Speichern Sie diese Datei in einem Ordner auf Ihrem lokalen Computer. Sie sparen für diesen Ordner sowie die anderen Skripts.
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    Die erste Zeile oder die Kopfzeile der Datei enthält die Parameter, die vom **New-ComplianceSearch** -Cmdlet (in das Skript in Schritt 3) zum Erstellen einer neuen Content-Suche verwendet werden. Jeder Parametername wird durch ein Komma getrennt. Stellen Sie sicher, dass es keine sind keine Leerzeichen in der Kopfzeile. Jede Zeile unter der Überschrift stellt die Parameterwerte für jedes Suchergebnis. Achten Sie darauf, dass Sie die Platzhalterdaten in der CSV-Datei durch den tatsächlichen Daten ersetzen. 
    
2. Öffnen Sie die TXT-Datei in Excel, und klicken Sie dann anhand der Informationen in der folgenden Tabelle zum Bearbeiten der Datei mit Informationen für jedes Suchergebnis. 
    
    |**Parameter**|**Beschreibung**|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |Die SMTP-Adresse des Postfachs des Benutzers.  <br/> |
    | `SharePointLocation` <br/> |Die URL für den Benutzer OneDrive for Business-Website oder die URL einer beliebigen Website in Ihrer Organisation. Für die URL für OneDrive for Business-Websites, verwenden Sie dieses Format: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `. Beispielsweise `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.<br/> |
    | `ContentMatchQuery` <br/> |Die Search-Abfrage für die Suche. Weitere Informationen zum Erstellen einer Suchabfrage finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md).<br/> |
    | `StartDate` <br/> |Für e-Mails die, das Datum an oder nach einer Nachricht oder erhalten wurde von einem Empfänger vom Absender gesendet. Für Dokumente in SharePoint OneDrive for Business-Websites das Datum, an oder nach einem Dokument zuletzt geändert wurde.  <br/> |
    | `EndDate` <br/> |Für e-Mails die, das Datum an oder vor einer Nachricht vom gesendet wurde durch den Benutzer gesendet. Für Dokumente in SharePoint OneDrive for Business-Websites das Datum an oder vor einem Dokument zuletzt geändert wurde.  <br/> |
   
3. Speichern Sie die Excel-Datei als CSV-Datei in einen Ordner auf Ihrem lokalen Computer. Das Skript, das Sie in Schritt 3 erstellen werden die Informationen in der CSV-Datei verwenden, um die Suche zu erstellen. 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Schritt 2: Verbinden Sie mit Sicherheits- und Compliance Center PowerShell

Im nächsten Schritt wird zum Verbinden von Windows PowerShell für die Sicherheit &amp; Compliance Center für Ihre Organisation.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `ConnectSCC.ps1`. Speichern Sie die Datei im gleichen Ordner, die Sie in Schritt 1 die CSV-Datei gespeichert.
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem das Skript, das Sie im vorherigen Schritt erstellt haben befindet, und führen Sie das Skript; Zum Beispiel:
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a>Schritt 3: Ausführen des Skripts zum Erstellen und starten Sie die Suche

Das Skript in diesem Schritt Erstellen einer separaten Inhaltssuche für jede Zeile in der CSV-Datei, die Sie in Schritt 1 erstellt haben. Wenn Sie dieses Skript ausführen, werden Sie für die beiden Werte aufgefordert:
  
- **Suche Gruppen-ID** - dieser Name bietet eine einfache Möglichkeit zum Organisieren von der suchen, die aus der CSV-Datei erstellt werden. Jeder Suche, die erstellt wird mit der Gruppe-ID namens ist, und klicken Sie dann auf den Namen der Suche eine Zahl angehängt ist. Angenommen, wenn Sie **ContosoCase** für die Suche Gruppen-ID eingeben, klicken Sie dann die suchen **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**und So weiter heißen. Beachten Sie, dass die eingegebene Name Groß-/Kleinschreibung beachtet wird. Wenn Sie die Suche Gruppen-ID in Schritt 4 und 5 Schritt verwenden, müssen Sie die gleiche Groß-/Kleinschreibung verwenden wie beim Erstellen. 
    
- **CSV-Datei** – der Name der CSV-Datei, die Sie in Schritt 1 erstellt haben. Achten Sie darauf, umfassen die Verwendung der vollständige Dateiname, schließen Sie die Erweiterung der CSV-Datei. beispielsweise `ContosoCase.csv`.
    
So führen Sie das Skript aus

1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `CreateSearches.ps1`. Speichern Sie die Datei im gleichen Ordner, in dem Sie die anderen Dateien gespeichert haben.
    
  ```
  # Get the Search Group ID and the location of the CSV input file
  $searchGroup = Read-Host 'Search Group ID'
  $csvFile = Read-Host 'Source CSV file'
    
  # Do a quick check to make sure our group name will not collide with other searches
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    $searchName = $searchGroup +'_' + $searchCounter
    $search = Get-ComplianceSearch $searchName -EA SilentlyContinue
    if ($search)
    {
        Write-Error "The Search Group ID conflicts with existing searches.  Please choose a search group name and restart the script."
        return
    }
    $searchCounter++
  }
    
  $searchCounter = 1
  import-csv $csvFile |
    ForEach-Object{
    
    # Create the query
    $query = $_.ContentMatchQuery
    if(($_.StartDate -or $_.EndDate))
    {
          # Add the appropriate date restrictions.  NOTE: Using the Date condition property here because it works across Exchange, SharePoint, and OneDrive for Business.
          # For Exchange, the Date condition property maps to the Sent and Received dates; for SharePoint and OneDrive for Business, it maps to Created and Modified dates.
          if($query)
          {
              $query += " AND"
          }
          $query += " ("
          if($_.StartDate)
          {
              $query += "Date >= " + $_.StartDate
          }
          if($_.EndDate)
          {
              if($_.StartDate)
              {
                  $query += " AND "
              }
              $query += "Date <= " + $_.EndDate
          }
          $query += ")"
    }
      
      # -ExchangeLocation can't be set to an empty string, set to null if there's no location.
      $exchangeLocation = $null
      if ( $_.ExchangeLocation)
      {
           $exchangeLocation = $_.ExchangeLocation
      }
    
    # Create and run the search        
    $searchName = $searchGroup +'_' + $searchCounter
    Write-Host "Creating and running search: " $searchName -NoNewline
    $search = New-ComplianceSearch -Name $searchName -ExchangeLocation $exchangeLocation -SharePointLocation $_.SharePointLocation -ContentMatchQuery $query
    
    # Start and wait for each search to complete
    Start-ComplianceSearch $search.Name
    while ((Get-ComplianceSearch $search.Name).Status -ne "Completed")
    {
        Write-Host " ." -NoNewline
        Start-Sleep -s 3
    }
    Write-Host ""
    
    $searchCounter++
  }
  ```

2. In Windows PowerShell wechseln zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript. Zum Beispiel:
    
    ```
    .\CreateSearches.ps1
    ```

3. **Suche Gruppen-ID** dazu aufgefordert werden Geben Sie einen Suchbegriff für die Gruppe ein, und drücken Sie die **EINGABETASTE**; beispielsweise `ContosoCase`. Denken Sie daran, dass bei diesem Namen Groß-/Kleinschreibung beachtet wird, müssen Sie die gleiche Weise wie in der nachfolgenden Schritte eingeben.
    
4. Geben Sie an der Eingabeaufforderung **Quelle CSV-Datei** den Namen der CSV-Datei, einschließlich das CSV-Datei; beispielsweise `ContosoCase.csv`.
    
5. Drücken Sie die **EINGABETASTE** , um den Vorgang fortzusetzen, Ausführen des Skripts. 
    
    Das Skript zeigt den Fortschritt des Erstellens und Ausführens die suchen. Wenn das Skript abgeschlossen ist, wird an der Eingabeaufforderung zurückgegeben. 
    
    ![Beispielausgabe für das Ausführen des Skripts zum Erstellen mehrere Compliancesuchen](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a>Schritt 4: Ausführen schätzt des Skripts für die Suche Unwichtigstes

Nachdem die Suche erstellt wurde, besteht der nächste Schritt das Ausführen eines Skripts, das die Anzahl der Suche Treffer bei jeder Suche ein einfaches Berichts angezeigt wird, das in Schritt 3 erstellt wurde. Der Bericht enthält auch die Größe der Ergebnisse für jede Suche und die Gesamtzahl der Treffer und die Gesamtgröße aller Suchvorgänge. Wenn Sie das reporting Skript ausführen, werden Sie aufgefordert für die Suche Gruppen-ID und einen Dateinamen für die CSV-Wenn Sie den Bericht in eine CSV-Datei speichern möchten.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `SearchReport.ps1`. Speichern Sie die Datei im gleichen Ordner, in dem Sie die anderen Dateien gespeichert haben.
    
  ```
  $searchGroup = Read-Host 'Search Group ID'
  $outputFile = Read-Host 'Enter a file name or file path to save the report to a .csv file. Leave blank to only display the report'
  $searches = Get-ComplianceSearch | ?{$_.Name -clike $searchGroup + "_*"}
  $allSearchStats = @()
  foreach ($partialObj in $searches)
  {
      $search = Get-ComplianceSearch $partialObj.Name
      $sizeMB = [System.Math]::Round($search.Size / 1MB, 2)
      $searchStatus = $search.Status
      if($search.Errors)
      {
          $searchStatus = "Failed"
      }elseif($search.NumFailedSources -gt 0)
      {
          $searchStatus = "Failed Sources"
      }
      $searchStats = New-Object PSObject
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Name -Value $search.Name
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name ContentMatchQuery -Value $search.ContentMatchQuery
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Status -Value $searchStatus
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name Items -Value $search.Items
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size" -Value $search.Size
      Add-Member -InputObject $searchStats -MemberType NoteProperty -Name "Size(MB)" -Value $sizeMB
      $allSearchStats += $searchStats
  }
  # Calculate the totals
  $allItems = ($allSearchStats | Measure-Object Items -Sum).Sum
  # Convert the total size to MB and round to the nearst 100th
  $allSize = ($allSearchStats | Measure-Object 'Size' -Sum).Sum
  $allSizeMB = [System.Math]::Round($allSize  / 1MB, 2)
  # Get the total successful searches and total of all searches
  $allSuccessCount = ($allSearchStats |?{$_.Status -eq "Completed"}).Count
  $allCount = $allSearchStats.Count
  $allStatus = [string]$allSuccessCount + " of " + [string]$allCount
  # Totals Row
  $totalSearchStats = New-Object PSObject
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Name -Value "Total"
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Status -Value $allStatus
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name Items -Value $allItems
  Add-Member -InputObject $totalSearchStats -MemberType NoteProperty -Name "Size(MB)" -Value $allSizeMB
  $allSearchStats += $totalSearchStats
  # Just get the columns we're interested in showing
  $allSearchStatsPrime = $allSearchStats | Select-Object Name, Status, Items, "Size(MB)", ContentMatchQuery
  # Print the results to the screen
  $allSearchStatsPrime |ft -AutoSize -Wrap
  # Save the results to a CSV file
  if ($outputFile)
  {
      $allSearchStatsPrime | Export-Csv -Path $outputFile -NoTypeInformation
  }
  ```

2. In Windows PowerShell wechseln zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript. Zum Beispiel:
    
    ```
    .\SearchReport.ps1
    ```

3. **Suche Gruppen-ID** dazu aufgefordert werden Geben Sie einen Suchbegriff für die Gruppe ein, und drücken Sie die **EINGABETASTE**; beispielsweise `ContosoCase`. Denken Sie daran, dass bei diesem Namen wird zwischen Groß-und Kleinschreibung, sodass Sie es eingeben müssen die gleiche Weise wie haben Sie bei der Ausführung des Skripts in Schritt 3.
    
4. Geben Sie an der Eingabeaufforderung **Dateipfad zum Speichern des Berichts in eine CSV-Datei (leer lassen, um nur den Bericht anzeigen)** einen Dateinamen des vollständigen Dateipfads (einschließlich das CSV-Datei) ein, wenn Sie den Bericht in eine CSV-Datei speichern möchten. Der Name der CSV-Datei, einschließlich das CSV-Datei. Geben Sie beispielsweise `ContosoCaseReport.csv` speichern in das aktuelle Verzeichnis oder Sie geben konnte `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` auf einem anderen Ordner zu speichern. Sie können auch die Aufforderung leer lassen den Bericht anzeigen, aber nicht in einer Datei speichern. 
    
5. Drücken Sie die **EINGABETASTE**.
    
    Das Skript zeigt den Fortschritt des Erstellens und Ausführens die suchen. Wenn das Skript abgeschlossen ist, wird der Bericht angezeigt. 
    
    ![Führen Sie den Suchbericht aus, um die Schätzwerte für die Suchgruppe anzuzeigen.](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> Wenn das Postfach oder die Site als einen Inhaltsspeicherort in mehr als eine Suche in einer Gruppe Suche angegeben wird, kann die Schätzung für das gesamte Ergebnisse im Bericht (für die Anzahl der Elemente und die Gesamtgröße) Ergebnisse für die gleichen Elemente enthalten. Dies liegt daran die dieselbe e-Mail-Nachricht oder das Dokument nur einmal gezählt werden, wenn er die Abfrage für unterschiedliche Suchen durchführen, in der Gruppe Suche übereinstimmt. 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a>Schritt 5: Führen Sie das Skript, um die Suche zu löschen.

Da Sie viele Suchvorgänge erstellen können, erleichtert dieses letzte Skript nur schnell die Suchen löschen, die Sie in Schritt 3 erstellt haben. Wie die anderen Skripts aufgefordert, diese auch die Kennung der Suche. Beim Ausführen dieses Skripts werden alle Suchvorgänge mit der Gruppe-ID in den Suchbegriff gelöscht. 
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `DeleteSearches.ps1`. Speichern Sie die Datei im gleichen Ordner, in dem Sie die anderen Dateien gespeichert haben.
    
  ```
  # Delete all searches in a search group
  $searchGroup = Read-Host 'Search Group ID'
  Get-ComplianceSearch |
      ForEach-Object{
      # If the name matches the search group name pattern (case sensitive), delete the search
      if ($_.Name -cmatch $searchGroup + "_\d+")
      {
          Write-Host "Deleting search: " $_.Name
          Remove-ComplianceSearch $_.Name -Confirm:$false
      }
  }
  ```

2. In Windows PowerShell wechseln zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript. Zum Beispiel:
    
    ```
    .\DeleteSearches.ps1
    ```

3. **Suche Gruppen-ID** dazu aufgefordert werden Geben Sie einen Gruppennamen Suche für die Suche, die Sie löschen möchten, und drücken Sie die **EINGABETASTE**; beispielsweise `ContosoCase`. Denken Sie daran, dass bei diesem Namen wird zwischen Groß-und Kleinschreibung, sodass Sie es eingeben müssen die gleiche Weise wie haben Sie bei der Ausführung des Skripts in Schritt 3.
    
    Das Skript zeigt den Namen der einzelnen Suche, der gelöscht wird.
    
    ![Führen Sie das Skript zum Löschen der Suchvorgänge in der Suchgruppe aus.](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
