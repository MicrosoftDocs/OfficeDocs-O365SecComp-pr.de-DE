---
title: Erstellen, Ausführen von Berichten und Löschen mehrerer Inhaltssuchen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/26/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
ms.assetid: 1d463dda-a3b5-4675-95d4-83db19c9c4a3
description: In diesem Artikel erfahren Sie, wie Sie Inhalts Suchaufgaben wie das Erstellen von Suchvorgängen und das Ausführen von Berichten über PowerShell-Skripts im Security & Compliance Center in Office 365 automatisieren.
ms.openlocfilehash: 96d10e274cd83a4785170239302d55e74d40ca84
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258438"
---
# <a name="create-report-on-and-delete-multiple-content-searches"></a>Erstellen, Ausführen von Berichten und Löschen mehrerer Inhaltssuchen

 Das schnelle Erstellen und melden von Ermittlungs suchen ist häufig ein wichtiger Schritt in eDiscovery und Untersuchungen, wenn Sie versuchen, Informationen zu den zugrunde liegenden Daten sowie zur Reichhaltigkeit und Qualität Ihrer Suchvorgänge zu erhalten. Um Ihnen dabei zu helfen, bietet die Security & Compliance Center PowerShell eine Reihe von Cmdlets, mit denen zeitaufwändige Inhalts Suchaufgaben automatisiert werden. Diese Skripts bieten eine schnelle und einfache Möglichkeit, eine Reihe von Suchvorgängen zu erstellen, und führen dann Berichte der geschätzten Suchergebnisse aus, die Sie bei der Bestimmung der fraglichen Datenmenge unterstützen können. Sie können die Skripts auch verwenden, um unterschiedliche Versionen der Suchvorgänge zu erstellen, um die jeweils produzierten Ergebnisse zu vergleichen. Diese Skripts helfen Ihnen dabei, Ihre Daten schnell und effizient zu identifizieren und zu ermitteln. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen Mitglied der eDiscovery-Manager-Rollengruppe im Security & Compliance Center sein, um die in diesem Thema beschriebenen Skripts ausführen zu können. 
    
- Informationen zum Erfassen einer Liste der URLs für die OneDrive für Business-Websites in Ihrer Organisation, die Sie der CSV-Datei in Schritt 1 hinzufügen können, finden Sie unter [Erstellen einer Liste aller OneDrive-Standorte in Ihrer Organisation](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a). 
    
- Speichern Sie alle Dateien, die Sie in diesem Thema erstellen, in demselben Ordner. Dies erleichtert das Ausführen der Skripts.
    
- Die Skripts bieten eine minimale Fehlerbehandlung. Ihr primärer Zweck besteht darin, mehrere Inhalts suchVorgänge schnell zu erstellen, zu melden und zu löschen.
    
- Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a>Schritt 1: Erstellen einer CSV-Datei mit Informationen zu den Suchvorgängen, die ausgeführt werden sollen

Die CSV-Datei (Comma Separated Value), die Sie in diesem Schritt erstellen, enthält eine Zeile für jeden Benutzer, der durchsucht werden soll. Sie können das Exchange Online-Postfach des Benutzers (einschließlich des Archivpostfachs, wenn es aktiviert ist) und dessen OneDrive für Unternehmen-Website durchsuchen. Sie können auch nur das Postfach oder die OneDrive for Business-Website durchsuchen. Sie können auch eine beliebige Website in Ihrer SharePoint Online-Organisation durchsuchen. Das Skript, das Sie in Schritt 3 ausführen, erstellt eine separate Suche für jede Zeile in der CSV-Datei. 
  
1. Kopieren Sie den folgenden Text, und fügen Sie ihn mit NotePad in eine txt-Datei ein. Speichern Sie diese Datei in einem Ordner auf dem lokalen Computer. Sie speichern auch die anderen Skripts in diesem Ordner.
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    In der ersten Zeile oder Kopfzeile der Datei werden die Parameter aufgelistet, die vom **New-ComplianceSearch-** Cmdlet (im Skript in Schritt 3) zum Erstellen einer neuen Inhaltssuche verwendet werden. Die einzelnen Parameternamen werden jeweils durch ein Komma getrennt. Stellen Sie sicher, dass keine Leerzeichen in der Kopfzeile vorhanden sind. Jede Zeile unter der Kopfzeile stellt die Parameterwerte für jede Suche dar. Stellen Sie sicher, dass Sie die Platzhalterdaten in der CSV-Datei durch ihre tatsächlichen Daten ersetzen. 
    
2. Öffnen Sie die txt-Datei in Excel, und verwenden Sie dann die Informationen in der folgenden Tabelle, um die Datei mit Informationen zu jeder Suche zu bearbeiten. 
    
    |**Parameter**|**Beschreibung**|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |Die SMTP-Adresse des Postfachs des Benutzers.  <br/> |
    | `SharePointLocation` <br/> |Die URL für die OneDrive für die Business-Website des Benutzers oder die URL für eine beliebige Website in Ihrer Organisation. Verwenden Sie für die URL für OneDrive for Business-Websites das folgende ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `Format:. Beispiel:  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.  <br/> |
    | `ContentMatchQuery` <br/> |Die Suchabfrage für die Suche. Weitere Informationen zum Erstellen einer Suchabfrage finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).  <br/> |
    | `StartDate` <br/> |Für e-Mails das Datum, an dem oder nachdem eine Nachricht von einem Empfänger empfangen oder vom Absender gesendet wurde. Für Dokumente auf SharePoint-oder OneDrive für Business-Websites das Datum, an dem oder nachdem ein Dokument zuletzt geändert wurde.  <br/> |
    | `EndDate` <br/> |Bei e-Mails wurde das Datum, an dem eine Nachricht vom Benutzer gesendet wurde, an oder vor dem Senden gesendet. Für Dokumente auf SharePoint-oder OneDrive für Business-Websites das Datum, an dem oder bevor ein Dokument zuletzt geändert wurde.  <br/> |
   
3. Speichern Sie die Excel-Datei als CSV-Datei in einem Ordner auf dem lokalen Computer. Das Skript, das Sie in Schritt 3 erstellen, verwendet die Informationen in dieser CSV-Datei, um die Suchvorgänge zu erstellen. 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a>Schritt 2: Herstellen einer Verbindung mit Security & Compliance Center PowerShell

Der nächste Schritt besteht darin, eine Verbindung zur Security & Compliance Center-PowerShell für Ihre Organisation herzustellen.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `ConnectSCC.ps1`. Speichern Sie die Datei in dem Ordner, in dem Sie die CSV-Datei gespeichert haben, in Schritt 1.
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Security & Compliance Center)" 
    ```

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem sich das Skript befindet, das Sie im vorherigen Schritt erstellt haben, und führen Sie das Skript aus. Zum Beispiel:
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a>Schritt 3: Ausführen des Skripts zum Erstellen und Starten der Suche

Das Skript in diesem Schritt erstellt eine separate Inhaltssuche für jede Zeile in der CSV-Datei, die Sie in Schritt 1 erstellt haben. Wenn Sie dieses Skript ausführen, werden Sie aufgefordert, zwei Werte einzugeben:
  
- **ID der suchgruppe** -dieser Name bietet eine einfache Möglichkeit zum Organisieren der Suchvorgänge, die aus der CSV-Datei erstellt werden. Jede erstellte Suche wird mit der ID der Suchgruppe benannt, und dann wird eine Nummer an den Namen der Suche angehängt. Wenn Sie beispielsweise **ContosoCase** für die ID der suchgruppe eingeben, werden die suchVorgänge als **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**usw. bezeichnet. Beachten Sie, dass der von Ihnen eingegebene Name Groß-/Kleinschreibung beachtet. Wenn Sie die Suchgruppen-ID in Schritt 4 und Schritt 5 verwenden, müssen Sie den gleichen Groß-/Kleinschreibung wie beim Erstellen verwenden. 
    
- **CSV-Datei** : der Name der CSV-Datei, die Sie in Schritt 1 erstellt haben. Stellen Sie sicher, dass Sie den vollständigen Dateinamen verwenden, die CSV-Dateierweiterung einbeziehen; Beispiel: `ContosoCase.csv`.
    
So führen Sie das Skript aus

1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `CreateSearches.ps1`. Speichern Sie die Datei in dem Ordner, in dem Sie die anderen Dateien gespeichert haben.
    
  ```Powershell
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

2. Wechseln Sie in Windows PowerShell zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript aus; Zum Beispiel:
    
    ```Powershell
    .\CreateSearches.ps1
    ```

3. Geben Sie an der Eingabeaufforderungen für die **Suchgruppen-ID** einen Suchgruppen Namen ein, und drücken Sie dann die **Eingabe**Taste. Beispiel: `ContosoCase`. Beachten Sie, dass bei diesem Namen die Groß-/Kleinschreibung beachtet wird, sodass Sie Sie in den nachfolgenden Schritten auf die gleiche Art eingeben müssen.
    
4. Geben Sie an der Eingabeaufforderungen für die **Quell-CSV** -Datei den Namen der CSV-Datei ein, einschließlich der CSV-Dateierweiterung. Beispiel: `ContosoCase.csv`.
    
5. Drücken **Sie die Eingabe** Taste, um das Skript zu starten. 
    
    Das Skript zeigt den Fortschritt beim Erstellen und Ausführen der Suche an. Wenn das Skript abgeschlossen ist, wird es an die Ansage zurückgegeben. 
    
    ![Beispielausgabe vom Ausführen des Skripts zum Erstellen mehrerer Kompatibilitäts Suchvorgänge](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a>Schritt 4: Ausführen des Skripts zum Melden der Such Schätzungen

Nachdem Sie die Suchvorgänge erstellt haben, besteht der nächste Schritt darin, ein Skript auszuführen, in dem ein einfacher Bericht über die Anzahl der Suchtreffer für jede in Schritt 3 erstellte Suche angezeigt wird. Der Bericht enthält auch die Größe der Ergebnisse für jede Suche und die Gesamtzahl der Treffer und die Gesamtgröße aller Suchvorgänge. Wenn Sie das Bericht Erstellungsskript ausführen, werden Sie aufgefordert, die ID der Suchgruppe und einen CSV-Dateinamen einzugeben, wenn Sie den Bericht in einer CSV speichern möchten.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `SearchReport.ps1`. Speichern Sie die Datei in dem Ordner, in dem Sie die anderen Dateien gespeichert haben.
    
  ```Powershell
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

2. Wechseln Sie in Windows PowerShell zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript aus; Zum Beispiel:
    
    ```Powershell
    .\SearchReport.ps1
    ```

3. Geben Sie an der Eingabeaufforderungen für die **Suchgruppen-ID** einen Suchgruppen Namen ein, und drücken Sie dann die **Eingabe**Taste. Beispiel `ContosoCase`. Beachten Sie, dass bei diesem Namen die Groß-/Kleinschreibung beachtet wird, sodass Sie Sie so eingeben müssen, wie Sie es auch beim Ausführen des Skripts in Schritt 3 getan haben.
    
4. Geben Sie im **Dateipfad zum Speichern des Berichts in einer CSV-Datei (lassen Sie leer, um die Meldung nur anzuzeigen)** einen Dateinamen Vollständiger Dateiname (einschließlich der CSV-Dateierweiterung) ein, wenn Sie den Bericht in einer CSV-Datei speichern möchten. der Name der CSV-Datei, einschließlich der CSV-Dateierweiterung. Sie können beispielsweise eingeben `ContosoCaseReport.csv` , um es im aktuellen Verzeichnis zu speichern, oder Sie können `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` eingeben, um es in einem anderen Ordner zu speichern. Sie können die Eingabeaufforderungen auch leer lassen, um den Bericht anzuzeigen, aber nicht in einer Datei zu speichern. 
    
5. Drücken Sie **EINGABE**.
    
    Das Skript zeigt den Fortschritt beim Erstellen und Ausführen der Suche an. Nach Abschluss des Skripts wird der Bericht angezeigt. 
    
    ![Ausführen des Suchberichts zum Anzeigen der Schätzungen für die suchgruppe](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> Wenn das gleiche Postfach oder die gleiche Website als Inhaltsspeicherort in mehr als einer Suche in einer suchgruppe angegeben wird, kann die geschätzte Summe der Ergebnisse im Bericht (für die Anzahl der Elemente und die Gesamtgröße) Ergebnisse für dieselben Elemente aufweisen. Das liegt daran, dass dieselbe e-Mail-Nachricht oder dasselbe Dokument mehr als einmal gezählt wird, wenn Sie mit der Abfrage für verschiedene Suchvorgänge in der suchgruppe übereinstimmt. 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a>Schritt 5: Ausführen des Skripts zum Löschen der Suchvorgänge

Da Sie vielleicht viele Suchvorgänge durchführen, ist es mit diesem letzten Skript einfach, die in Schritt 3 erstellten Suchvorgänge schnell zu löschen. Wie die anderen Skripts werden Sie auch aufgefordert, die ID der Suchgruppe EINZUGEBEN. Alle Suchvorgänge mit der Suchgruppen-ID im Suchnamen werden gelöscht, wenn Sie dieses Skript ausführen. 
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `DeleteSearches.ps1`. Speichern Sie die Datei in dem Ordner, in dem Sie die anderen Dateien gespeichert haben.
    
  ```Powershell
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

2. Wechseln Sie in Windows PowerShell zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript aus; Zum Beispiel:
    
    ```Powershell
    .\DeleteSearches.ps1
    ```

3. Geben Sie an der Eingabeaufforderungen für die **Suchgruppen-ID** einen Suchgruppen Namen für die Suchvorgänge ein, die Sie löschen möchten, und drücken Sie dann die **Eingabe**Taste. Beispiel: `ContosoCase`. Beachten Sie, dass bei diesem Namen die Groß-/Kleinschreibung beachtet wird, sodass Sie Sie so eingeben müssen, wie Sie es auch beim Ausführen des Skripts in Schritt 3 getan haben.
    
    Das Skript zeigt den Namen jeder gelöschten Suche an.
    
    ![Ausführen des Skripts zum Löschen der Suchvorgänge in der Gruppe "Suche"](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
