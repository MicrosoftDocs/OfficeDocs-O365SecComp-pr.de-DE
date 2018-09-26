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
# <a name="create-report-on-and-delete-multiple-content-searches"></a><span data-ttu-id="6ac61-103">Erstellen, Berichten über und Löschen mehrerer Inhaltssuchen</span><span class="sxs-lookup"><span data-stu-id="6ac61-103">Create, report on, and delete multiple Content Searches</span></span>

 <span data-ttu-id="6ac61-p101">Schnell erstellen und reporting Discovery Suchvorgänge ist häufig ein wichtiger Schritt in eDiscovery und Untersuchungen, wenn Sie über die zugrunde liegenden Daten, und der Umfang und die Qualität der Ihre Suchanfragen informieren möchten. Zur einfacheren dazu, die Sicherheit &amp; Compliance Center bietet eine Reihe von Windows PowerShell-Cmdlets zeitaufwendige Inhaltssuche Aufgaben automatisieren. Diese Skripts bieten eine schnelle und problemlose Möglichkeit, eine Reihe von Suchvorgänge erstellen, und führen Sie Berichte der geschätzten Suchergebnisse, die Ihnen bei der Bestimmung der Menge der betreffenden Daten helfen kann. Die Skripts können auch verschiedene Versionen von Suchvorgängen, die Ergebnisse verglichen werden soll, die jeweils erzeugt erstellen. Diese Skripts können Sie schnell und effizient zu identifizieren und ausgemerzte Ihrer Daten.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p101">Quickly creating and reporting discovery searches is often an important step in eDiscovery and investigations when you're trying to learn about the underlying data, and the richness and quality of your searches. To help you do this, the Security &amp; Compliance Center offers a set of Windows PowerShell cmdlets to automate time-consuming Content Search tasks. These scripts provide a quick and easy way to create a number of searches, and then run reports of the estimated search results that can help you determine the quantity of data in question. You can also use the scripts to create different versions of searches to compare the results each one produces. These scripts can help you to quickly and efficiently identify and cull your data.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="6ac61-109">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="6ac61-109">Before you begin</span></span>

- <span data-ttu-id="6ac61-110">Sie müssen ein Mitglied der Rollengruppe eDiscovery-Manager in das Wertpapier sein &amp; Compliance Center in diesem Thema ausführen, die Skripts, die beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6ac61-110">You have to be a member of the eDiscovery Manager role group in the Security &amp; Compliance Center to run the scripts that are described in this topic.</span></span> 
    
- <span data-ttu-id="6ac61-111">Um eine Liste der URLs für die OneDrive for Business-Websites in Ihrer Organisation zu sammeln, die Sie in der CSV-Datei in Schritt 1 hinzufügen können, finden Sie unter [Erstellen einer Liste der OneDrive Positionen in Ihrer Organisation](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span><span class="sxs-lookup"><span data-stu-id="6ac61-111">To collect a list of the URLs for the OneDrive for Business sites in your organization that you can add to the CSV file in Step 1, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span></span> 
    
- <span data-ttu-id="6ac61-p102">Achten Sie darauf, dass Sie alle Dateien zu speichern, die Sie in diesem Thema, um im gleichen Ordner erstellen. Die wird zum Ausführen der Skripts erleichtern.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p102">Be sure to save all the files that you create in this topic to the same folder. That will make it easier to run the scripts.</span></span>
    
- <span data-ttu-id="6ac61-p103">Die Skripts enthalten minimale Fehlerbehandlung. Ihre primäre Zweck ist schnell erstellen, melden und mehrere Content-Suche löschen.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p103">The scripts include minimal error handling. Their primary purpose is to quickly create, report on, and delete multiple Content Searches.</span></span>
    
- <span data-ttu-id="6ac61-p104">Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a><span data-ttu-id="6ac61-121">Schritt 1: Erstellen einer CSV-Datei, die Informationen zu der Suchvorgänge, die Sie ausführen möchten, enthält</span><span class="sxs-lookup"><span data-stu-id="6ac61-121">Step 1: Create a CSV file that contains information about the searches you want to run</span></span>

<span data-ttu-id="6ac61-p105">Die durch Trennzeichen getrennten Werten (CSV)-Datei, die Sie in diesem Schritt erstellen enthält eine Zeile für jeden Benutzer, den suchen möchten. Sie können das Postfach des Benutzers Exchange Online (einschließlich Archivpostfach, wenn es aktiviert ist) und ihre OneDrive for Business-Website suchen. Oder Sie können nur das Postfach oder die OneDrive for Business-Website suchen. Sie können auch eine andere Website in Ihrer SharePoint Online-Organisation suchen. Das Skript, das Sie in Schritt 3 ausführen, wird eine separate Suche für jede Zeile in der CSV-Datei erstellt.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p105">The comma separated value (CSV) file that you create in this step contains a row for each user that want to search. You can search the user's Exchange Online mailbox (which includes the archive mailbox, if it's enabled) and their OneDrive for Business site. Or you can search just the mailbox or the OneDrive for Business site. You can also search any site in your SharePoint Online organization. The script that you run in Step 3 will create a separate search for each row in the CSV file.</span></span> 
  
1. <span data-ttu-id="6ac61-p106">Kopieren Sie und fügen Sie den folgenden Text in eine TXT-Datei mit dem Editor. Speichern Sie diese Datei in einem Ordner auf Ihrem lokalen Computer. Sie sparen für diesen Ordner sowie die anderen Skripts.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p106">Copy and paste the following text into a .txt file using NotePad. Save this file to a folder on your local computer. You'll save the other scripts to this folder as well.</span></span>
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    <span data-ttu-id="6ac61-p107">Die erste Zeile oder die Kopfzeile der Datei enthält die Parameter, die vom **New-ComplianceSearch** -Cmdlet (in das Skript in Schritt 3) zum Erstellen einer neuen Content-Suche verwendet werden. Jeder Parametername wird durch ein Komma getrennt. Stellen Sie sicher, dass es keine sind keine Leerzeichen in der Kopfzeile. Jede Zeile unter der Überschrift stellt die Parameterwerte für jedes Suchergebnis. Achten Sie darauf, dass Sie die Platzhalterdaten in der CSV-Datei durch den tatsächlichen Daten ersetzen.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p107">The first row, or header row, of the file lists the parameters that will be used by **New-ComplianceSearch** cmdlet (in the script in Step 3) to create a new Content Searches. Each parameter name is separated by a comma. Make sure there aren't any spaces in the header row. Each row under the header row represents the parameter values for each search. Be sure to replace the placeholder data in the CSV file with your actual data.</span></span> 
    
2. <span data-ttu-id="6ac61-135">Öffnen Sie die TXT-Datei in Excel, und klicken Sie dann anhand der Informationen in der folgenden Tabelle zum Bearbeiten der Datei mit Informationen für jedes Suchergebnis.</span><span class="sxs-lookup"><span data-stu-id="6ac61-135">Open the .txt file in Excel, and then use the information in the following table to edit the file with information for each search.</span></span> 
    
    |<span data-ttu-id="6ac61-136">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="6ac61-136">**Parameter**</span></span>|<span data-ttu-id="6ac61-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ac61-137">**Description**</span></span>|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |<span data-ttu-id="6ac61-138">Die SMTP-Adresse des Postfachs des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="6ac61-138">The SMTP address of the user's mailbox.</span></span>  <br/> |
    | `SharePointLocation` <br/> |<span data-ttu-id="6ac61-p108">Die URL für den Benutzer OneDrive for Business-Website oder die URL einer beliebigen Website in Ihrer Organisation. Für die URL für OneDrive for Business-Websites, verwenden Sie dieses Format: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `. Beispielsweise `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p108">The URL for the user's OneDrive for Business site or the URL for any site in your organization. For the URL for OneDrive for Business sites, use this format: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `. For example,  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.  </span></span><br/> |
    | `ContentMatchQuery` <br/> |<span data-ttu-id="6ac61-p109">Die Search-Abfrage für die Suche. Weitere Informationen zum Erstellen einer Suchabfrage finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="6ac61-p109">The search query for the search. For more information about creating a search query, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).  </span></span><br/> |
    | `StartDate` <br/> |<span data-ttu-id="6ac61-p110">Für e-Mails die, das Datum an oder nach einer Nachricht oder erhalten wurde von einem Empfänger vom Absender gesendet. Für Dokumente in SharePoint OneDrive for Business-Websites das Datum, an oder nach einem Dokument zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p110">For email, the date on or after a message was received by a recipient or sent by the sender. For documents on SharePoint or OneDrive for Business sites, the date on or after a document was last modified.</span></span>  <br/> |
    | `EndDate` <br/> |<span data-ttu-id="6ac61-p111">Für e-Mails die, das Datum an oder vor einer Nachricht vom gesendet wurde durch den Benutzer gesendet. Für Dokumente in SharePoint OneDrive for Business-Websites das Datum an oder vor einem Dokument zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p111">For email, the date on or before a message was sent by a sent by the user. For documents on SharePoint or OneDrive for Business sites, the date on or before a document was last modified.</span></span>  <br/> |
   
3. <span data-ttu-id="6ac61-p112">Speichern Sie die Excel-Datei als CSV-Datei in einen Ordner auf Ihrem lokalen Computer. Das Skript, das Sie in Schritt 3 erstellen werden die Informationen in der CSV-Datei verwenden, um die Suche zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p112">Save the Excel file as a CSV file to a folder on your local computer. The script that you create in Step 3 will use the information in this CSV file to create the searches.</span></span> 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a><span data-ttu-id="6ac61-150">Schritt 2: Verbinden Sie mit Sicherheits- und Compliance Center PowerShell</span><span class="sxs-lookup"><span data-stu-id="6ac61-150">Step 2: Connect to Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="6ac61-151">Im nächsten Schritt wird zum Verbinden von Windows PowerShell für die Sicherheit &amp; Compliance Center für Ihre Organisation.</span><span class="sxs-lookup"><span data-stu-id="6ac61-151">The next step is to connect Windows PowerShell to the Security &amp; Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="6ac61-p113">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `ConnectSCC.ps1`. Speichern Sie die Datei im gleichen Ordner, die Sie in Schritt 1 die CSV-Datei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p113">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`. Save the file to the same folder that you saved the CSV file to in Step 1.</span></span>
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. <span data-ttu-id="6ac61-154">Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem das Skript, das Sie im vorherigen Schritt erstellt haben befindet, und führen Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6ac61-154">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a><span data-ttu-id="6ac61-155">Schritt 3: Ausführen des Skripts zum Erstellen und starten Sie die Suche</span><span class="sxs-lookup"><span data-stu-id="6ac61-155">Step 3: Run the script to create and start the searches</span></span>

<span data-ttu-id="6ac61-p114">Das Skript in diesem Schritt Erstellen einer separaten Inhaltssuche für jede Zeile in der CSV-Datei, die Sie in Schritt 1 erstellt haben. Wenn Sie dieses Skript ausführen, werden Sie für die beiden Werte aufgefordert:</span><span class="sxs-lookup"><span data-stu-id="6ac61-p114">The script in this step will create a separate Content Search for each row in the CSV file that you created in Step 1. When you run this script, you'll be prompted for two values:</span></span>
  
- <span data-ttu-id="6ac61-p115">**Suche Gruppen-ID** - dieser Name bietet eine einfache Möglichkeit zum Organisieren von der suchen, die aus der CSV-Datei erstellt werden. Jeder Suche, die erstellt wird mit der Gruppe-ID namens ist, und klicken Sie dann auf den Namen der Suche eine Zahl angehängt ist. Angenommen, wenn Sie **ContosoCase** für die Suche Gruppen-ID eingeben, klicken Sie dann die suchen **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**und So weiter heißen. Beachten Sie, dass die eingegebene Name Groß-/Kleinschreibung beachtet wird. Wenn Sie die Suche Gruppen-ID in Schritt 4 und 5 Schritt verwenden, müssen Sie die gleiche Groß-/Kleinschreibung verwenden wie beim Erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p115">**Search Group ID** - This name provides an easy way to organize the searches that are created from the CSV file. Each search that's created is named with the Search Group ID, and then a number is appended to the search name. For example, if you enter **ContosoCase** for the Search Group ID, then the searches are named **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**, and so on. Note that the name you type is case sensitive. When you use the Search Group ID in Step 4 and Step 5, you have to use the same case as you did when you created it.</span></span> 
    
- <span data-ttu-id="6ac61-p116">**CSV-Datei** – der Name der CSV-Datei, die Sie in Schritt 1 erstellt haben. Achten Sie darauf, umfassen die Verwendung der vollständige Dateiname, schließen Sie die Erweiterung der CSV-Datei. beispielsweise `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p116">**CSV file** - The name of the CSV file that you created in Step 1. Be sure to include the use the full filename, include the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
<span data-ttu-id="6ac61-165">So führen Sie das Skript aus</span><span class="sxs-lookup"><span data-stu-id="6ac61-165">To run the script:</span></span>

1. <span data-ttu-id="6ac61-p117">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `CreateSearches.ps1`. Speichern Sie die Datei im gleichen Ordner, in dem Sie die anderen Dateien gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p117">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CreateSearches.ps1`. Save the file to the same folder where you saved the other files.</span></span>
    
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

2. <span data-ttu-id="6ac61-168">In Windows PowerShell wechseln zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6ac61-168">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```
    .\CreateSearches.ps1
    ```

3. <span data-ttu-id="6ac61-p118">**Suche Gruppen-ID** dazu aufgefordert werden Geben Sie einen Suchbegriff für die Gruppe ein, und drücken Sie die **EINGABETASTE**; beispielsweise `ContosoCase`. Denken Sie daran, dass bei diesem Namen Groß-/Kleinschreibung beachtet wird, müssen Sie die gleiche Weise wie in der nachfolgenden Schritte eingeben.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p118">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example,  `ContosoCase`. Remember that this name is case sensitive, so you'll have to type it the same way in the subsequent steps.</span></span>
    
4. <span data-ttu-id="6ac61-171">Geben Sie an der Eingabeaufforderung **Quelle CSV-Datei** den Namen der CSV-Datei, einschließlich das CSV-Datei; beispielsweise `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="6ac61-171">At the **Source CSV file** prompt, type the name of the CSV file, including the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
5. <span data-ttu-id="6ac61-172">Drücken Sie die **EINGABETASTE** , um den Vorgang fortzusetzen, Ausführen des Skripts.</span><span class="sxs-lookup"><span data-stu-id="6ac61-172">Press **Enter** to continue running the script.</span></span> 
    
    <span data-ttu-id="6ac61-p119">Das Skript zeigt den Fortschritt des Erstellens und Ausführens die suchen. Wenn das Skript abgeschlossen ist, wird an der Eingabeaufforderung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p119">The script displays the progress of creating and running the searches. When the script is complete, it returns to the prompt.</span></span> 
    
    ![Beispielausgabe für das Ausführen des Skripts zum Erstellen mehrere Compliancesuchen](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a><span data-ttu-id="6ac61-176">Schritt 4: Ausführen schätzt des Skripts für die Suche Unwichtigstes</span><span class="sxs-lookup"><span data-stu-id="6ac61-176">Step 4: Run the script to report the search estimates</span></span>

<span data-ttu-id="6ac61-p120">Nachdem die Suche erstellt wurde, besteht der nächste Schritt das Ausführen eines Skripts, das die Anzahl der Suche Treffer bei jeder Suche ein einfaches Berichts angezeigt wird, das in Schritt 3 erstellt wurde. Der Bericht enthält auch die Größe der Ergebnisse für jede Suche und die Gesamtzahl der Treffer und die Gesamtgröße aller Suchvorgänge. Wenn Sie das reporting Skript ausführen, werden Sie aufgefordert für die Suche Gruppen-ID und einen Dateinamen für die CSV-Wenn Sie den Bericht in eine CSV-Datei speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p120">After you create the searches, the next step is to run a script that displays a simple report of the number of search hits for each search that was created in Step 3. The report also includes the size of results for each search, and the total number of hits and total size of all searches. When you run the reporting script, you'll be prompted for the Search Group ID, and a CSV filename if you want to save the report to a CSV file.</span></span>
  
1. <span data-ttu-id="6ac61-p121">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `SearchReport.ps1`. Speichern Sie die Datei im gleichen Ordner, in dem Sie die anderen Dateien gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p121">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchReport.ps1`. Save the file to the same folder where you saved the other files.</span></span>
    
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

2. <span data-ttu-id="6ac61-182">In Windows PowerShell wechseln zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6ac61-182">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```
    .\SearchReport.ps1
    ```

3. <span data-ttu-id="6ac61-p122">**Suche Gruppen-ID** dazu aufgefordert werden Geben Sie einen Suchbegriff für die Gruppe ein, und drücken Sie die **EINGABETASTE**; beispielsweise `ContosoCase`. Denken Sie daran, dass bei diesem Namen wird zwischen Groß-und Kleinschreibung, sodass Sie es eingeben müssen die gleiche Weise wie haben Sie bei der Ausführung des Skripts in Schritt 3.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p122">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example  `ContosoCase`. Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
4. <span data-ttu-id="6ac61-p123">Geben Sie an der Eingabeaufforderung **Dateipfad zum Speichern des Berichts in eine CSV-Datei (leer lassen, um nur den Bericht anzeigen)** einen Dateinamen des vollständigen Dateipfads (einschließlich das CSV-Datei) ein, wenn Sie den Bericht in eine CSV-Datei speichern möchten. Der Name der CSV-Datei, einschließlich das CSV-Datei. Geben Sie beispielsweise `ContosoCaseReport.csv` speichern in das aktuelle Verzeichnis oder Sie geben konnte `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` auf einem anderen Ordner zu speichern. Sie können auch die Aufforderung leer lassen den Bericht anzeigen, aber nicht in einer Datei speichern.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p123">At the **File path to save the report to a CSV file (leave blank to just display the report)** prompt, type a file name of complete filename path (including the .csv file extension) if you want to save the report to a CSV file. name of the CSV file, including the .csv file extension. For example, you could type  `ContosoCaseReport.csv` to save it to the current directory or you could type  `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` to save it to a different folder. You can also leave the prompt blank to display the report but not save it to a file.</span></span> 
    
5. <span data-ttu-id="6ac61-189">Drücken Sie die **EINGABETASTE**.</span><span class="sxs-lookup"><span data-stu-id="6ac61-189">Press **Enter**.</span></span>
    
    <span data-ttu-id="6ac61-p124">Das Skript zeigt den Fortschritt des Erstellens und Ausführens die suchen. Wenn das Skript abgeschlossen ist, wird der Bericht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p124">The script displays the progress of creating and running the searches. When the script is complete, the report is displayed.</span></span> 
    
    ![Führen Sie den Suchbericht aus, um die Schätzwerte für die Suchgruppe anzuzeigen.](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> <span data-ttu-id="6ac61-p125">Wenn das Postfach oder die Site als einen Inhaltsspeicherort in mehr als eine Suche in einer Gruppe Suche angegeben wird, kann die Schätzung für das gesamte Ergebnisse im Bericht (für die Anzahl der Elemente und die Gesamtgröße) Ergebnisse für die gleichen Elemente enthalten. Dies liegt daran die dieselbe e-Mail-Nachricht oder das Dokument nur einmal gezählt werden, wenn er die Abfrage für unterschiedliche Suchen durchführen, in der Gruppe Suche übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p125">If the same mailbox or site is specified as a content location in more than one search in a search group, the total results estimate in the report (for both the number of items and the total size) might include results for the same items. That's because the same email message or document will be counted more than once if it matches the query for different searches in the search group.</span></span> 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a><span data-ttu-id="6ac61-195">Schritt 5: Führen Sie das Skript, um die Suche zu löschen.</span><span class="sxs-lookup"><span data-stu-id="6ac61-195">Step 5: Run the script to delete the searches</span></span>

<span data-ttu-id="6ac61-p126">Da Sie viele Suchvorgänge erstellen können, erleichtert dieses letzte Skript nur schnell die Suchen löschen, die Sie in Schritt 3 erstellt haben. Wie die anderen Skripts aufgefordert, diese auch die Kennung der Suche. Beim Ausführen dieses Skripts werden alle Suchvorgänge mit der Gruppe-ID in den Suchbegriff gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p126">Because you might be creating a lot of searches, this last script just makes it easy to quickly delete the searches you created in Step 3. Like the other scripts, this one also prompts you for the Search Group ID. All searches with the Search Group ID in the search name will be deleted when you run this script.</span></span> 
  
1. <span data-ttu-id="6ac61-p127">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `DeleteSearches.ps1`. Speichern Sie die Datei im gleichen Ordner, in dem Sie die anderen Dateien gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p127">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `DeleteSearches.ps1`. Save the file to the same folder where you saved the other files.</span></span>
    
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

2. <span data-ttu-id="6ac61-201">In Windows PowerShell wechseln zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6ac61-201">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```
    .\DeleteSearches.ps1
    ```

3. <span data-ttu-id="6ac61-p128">**Suche Gruppen-ID** dazu aufgefordert werden Geben Sie einen Gruppennamen Suche für die Suche, die Sie löschen möchten, und drücken Sie die **EINGABETASTE**; beispielsweise `ContosoCase`. Denken Sie daran, dass bei diesem Namen wird zwischen Groß-und Kleinschreibung, sodass Sie es eingeben müssen die gleiche Weise wie haben Sie bei der Ausführung des Skripts in Schritt 3.</span><span class="sxs-lookup"><span data-stu-id="6ac61-p128">At the **Search Group ID** prompt, type a search group name for the searches that you want to delete, and then press **Enter**; for example,  `ContosoCase`. Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
    <span data-ttu-id="6ac61-204">Das Skript zeigt den Namen der einzelnen Suche, der gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="6ac61-204">The script displays the name of each search that's deleted.</span></span>
    
    ![Führen Sie das Skript zum Löschen der Suchvorgänge in der Suchgruppe aus.](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
