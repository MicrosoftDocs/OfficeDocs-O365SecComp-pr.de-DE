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
# <a name="create-report-on-and-delete-multiple-content-searches"></a><span data-ttu-id="eb5db-103">Erstellen, Ausführen von Berichten und Löschen mehrerer Inhaltssuchen</span><span class="sxs-lookup"><span data-stu-id="eb5db-103">Create, report on, and delete multiple Content Searches</span></span>

 <span data-ttu-id="eb5db-104">Das schnelle Erstellen und melden von Ermittlungs suchen ist häufig ein wichtiger Schritt in eDiscovery und Untersuchungen, wenn Sie versuchen, Informationen zu den zugrunde liegenden Daten sowie zur Reichhaltigkeit und Qualität Ihrer Suchvorgänge zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="eb5db-104">Quickly creating and reporting discovery searches is often an important step in eDiscovery and investigations when you're trying to learn about the underlying data, and the richness and quality of your searches.</span></span> <span data-ttu-id="eb5db-105">Um Ihnen dabei zu helfen, bietet die Security & Compliance Center PowerShell eine Reihe von Cmdlets, mit denen zeitaufwändige Inhalts Suchaufgaben automatisiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb5db-105">To help you do this, the Security & Compliance Center PowerShell offers a set of cmdlets to automate time-consuming Content Search tasks.</span></span> <span data-ttu-id="eb5db-106">Diese Skripts bieten eine schnelle und einfache Möglichkeit, eine Reihe von Suchvorgängen zu erstellen, und führen dann Berichte der geschätzten Suchergebnisse aus, die Sie bei der Bestimmung der fraglichen Datenmenge unterstützen können.</span><span class="sxs-lookup"><span data-stu-id="eb5db-106">These scripts provide a quick and easy way to create a number of searches, and then run reports of the estimated search results that can help you determine the quantity of data in question.</span></span> <span data-ttu-id="eb5db-107">Sie können die Skripts auch verwenden, um unterschiedliche Versionen der Suchvorgänge zu erstellen, um die jeweils produzierten Ergebnisse zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-107">You can also use the scripts to create different versions of searches to compare the results each one produces.</span></span> <span data-ttu-id="eb5db-108">Diese Skripts helfen Ihnen dabei, Ihre Daten schnell und effizient zu identifizieren und zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="eb5db-108">These scripts can help you to quickly and efficiently identify and cull your data.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="eb5db-109">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="eb5db-109">Before you begin</span></span>

- <span data-ttu-id="eb5db-110">Sie müssen Mitglied der eDiscovery-Manager-Rollengruppe im Security & Compliance Center sein, um die in diesem Thema beschriebenen Skripts ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="eb5db-110">You have to be a member of the eDiscovery Manager role group in the Security & Compliance Center to run the scripts that are described in this topic.</span></span> 
    
- <span data-ttu-id="eb5db-111">Informationen zum Erfassen einer Liste der URLs für die OneDrive für Business-Websites in Ihrer Organisation, die Sie der CSV-Datei in Schritt 1 hinzufügen können, finden Sie unter [Erstellen einer Liste aller OneDrive-Standorte in Ihrer Organisation](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span><span class="sxs-lookup"><span data-stu-id="eb5db-111">To collect a list of the URLs for the OneDrive for Business sites in your organization that you can add to the CSV file in Step 1, see [Create a list of all OneDrive locations in your organization](https://support.office.com/article/Create-a-list-of-all-OneDrive-locations-in-your-organization-8e200cb2-c768-49cb-88ec-53493e8ad80a).</span></span> 
    
- <span data-ttu-id="eb5db-112">Speichern Sie alle Dateien, die Sie in diesem Thema erstellen, in demselben Ordner.</span><span class="sxs-lookup"><span data-stu-id="eb5db-112">Be sure to save all the files that you create in this topic to the same folder.</span></span> <span data-ttu-id="eb5db-113">Dies erleichtert das Ausführen der Skripts.</span><span class="sxs-lookup"><span data-stu-id="eb5db-113">That will make it easier to run the scripts.</span></span>
    
- <span data-ttu-id="eb5db-114">Die Skripts bieten eine minimale Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="eb5db-114">The scripts include minimal error handling.</span></span> <span data-ttu-id="eb5db-115">Ihr primärer Zweck besteht darin, mehrere Inhalts suchVorgänge schnell zu erstellen, zu melden und zu löschen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-115">Their primary purpose is to quickly create, report on, and delete multiple Content Searches.</span></span>
    
- <span data-ttu-id="eb5db-p104">Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.</span><span class="sxs-lookup"><span data-stu-id="eb5db-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-create-a-csv-file-that-contains-information-about-the-searches-you-want-to-run"></a><span data-ttu-id="eb5db-121">Schritt 1: Erstellen einer CSV-Datei mit Informationen zu den Suchvorgängen, die ausgeführt werden sollen</span><span class="sxs-lookup"><span data-stu-id="eb5db-121">Step 1: Create a CSV file that contains information about the searches you want to run</span></span>

<span data-ttu-id="eb5db-122">Die CSV-Datei (Comma Separated Value), die Sie in diesem Schritt erstellen, enthält eine Zeile für jeden Benutzer, der durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="eb5db-122">The comma separated value (CSV) file that you create in this step contains a row for each user that want to search.</span></span> <span data-ttu-id="eb5db-123">Sie können das Exchange Online-Postfach des Benutzers (einschließlich des Archivpostfachs, wenn es aktiviert ist) und dessen OneDrive für Unternehmen-Website durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-123">You can search the user's Exchange Online mailbox (which includes the archive mailbox, if it's enabled) and their OneDrive for Business site.</span></span> <span data-ttu-id="eb5db-124">Sie können auch nur das Postfach oder die OneDrive for Business-Website durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-124">Or you can search just the mailbox or the OneDrive for Business site.</span></span> <span data-ttu-id="eb5db-125">Sie können auch eine beliebige Website in Ihrer SharePoint Online-Organisation durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-125">You can also search any site in your SharePoint Online organization.</span></span> <span data-ttu-id="eb5db-126">Das Skript, das Sie in Schritt 3 ausführen, erstellt eine separate Suche für jede Zeile in der CSV-Datei.</span><span class="sxs-lookup"><span data-stu-id="eb5db-126">The script that you run in Step 3 will create a separate search for each row in the CSV file.</span></span> 
  
1. <span data-ttu-id="eb5db-127">Kopieren Sie den folgenden Text, und fügen Sie ihn mit NotePad in eine txt-Datei ein.</span><span class="sxs-lookup"><span data-stu-id="eb5db-127">Copy and paste the following text into a .txt file using NotePad.</span></span> <span data-ttu-id="eb5db-128">Speichern Sie diese Datei in einem Ordner auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="eb5db-128">Save this file to a folder on your local computer.</span></span> <span data-ttu-id="eb5db-129">Sie speichern auch die anderen Skripts in diesem Ordner.</span><span class="sxs-lookup"><span data-stu-id="eb5db-129">You'll save the other scripts to this folder as well.</span></span>
    
    ```
    ExchangeLocation,SharePointLocation,ContentMatchQuery,StartDate,EndDate
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2000,12/31/2005
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2006,12/31/2010
    sarad@contoso.onmicrosoft.com,https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com,(lawsuit OR legal),1/1/2011,3/21/2016
    ,https://contoso.sharepoint.com/sites/contoso,,,3/21/2016
    ,https://contoso-my.sharepoint.com/personal/davidl_contoso_onmicrosoft_com,,1/1/2015,
    ,https://contoso-my.sharepoint.com/personal/janets_contoso_onmicrosoft_com,,1/1/2015,
    ```

    <span data-ttu-id="eb5db-130">In der ersten Zeile oder Kopfzeile der Datei werden die Parameter aufgelistet, die vom **New-ComplianceSearch-** Cmdlet (im Skript in Schritt 3) zum Erstellen einer neuen Inhaltssuche verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eb5db-130">The first row, or header row, of the file lists the parameters that will be used by **New-ComplianceSearch** cmdlet (in the script in Step 3) to create a new Content Searches.</span></span> <span data-ttu-id="eb5db-131">Die einzelnen Parameternamen werden jeweils durch ein Komma getrennt.</span><span class="sxs-lookup"><span data-stu-id="eb5db-131">Each parameter name is separated by a comma.</span></span> <span data-ttu-id="eb5db-132">Stellen Sie sicher, dass keine Leerzeichen in der Kopfzeile vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="eb5db-132">Make sure there aren't any spaces in the header row.</span></span> <span data-ttu-id="eb5db-133">Jede Zeile unter der Kopfzeile stellt die Parameterwerte für jede Suche dar.</span><span class="sxs-lookup"><span data-stu-id="eb5db-133">Each row under the header row represents the parameter values for each search.</span></span> <span data-ttu-id="eb5db-134">Stellen Sie sicher, dass Sie die Platzhalterdaten in der CSV-Datei durch ihre tatsächlichen Daten ersetzen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-134">Be sure to replace the placeholder data in the CSV file with your actual data.</span></span> 
    
2. <span data-ttu-id="eb5db-135">Öffnen Sie die txt-Datei in Excel, und verwenden Sie dann die Informationen in der folgenden Tabelle, um die Datei mit Informationen zu jeder Suche zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="eb5db-135">Open the .txt file in Excel, and then use the information in the following table to edit the file with information for each search.</span></span> 
    
    |<span data-ttu-id="eb5db-136">**Parameter**</span><span class="sxs-lookup"><span data-stu-id="eb5db-136">**Parameter**</span></span>|<span data-ttu-id="eb5db-137">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="eb5db-137">**Description**</span></span>|
    |:-----|:-----|
    | `ExchangeLocation` <br/> |<span data-ttu-id="eb5db-138">Die SMTP-Adresse des Postfachs des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="eb5db-138">The SMTP address of the user's mailbox.</span></span>  <br/> |
    | `SharePointLocation` <br/> |<span data-ttu-id="eb5db-139">Die URL für die OneDrive für die Business-Website des Benutzers oder die URL für eine beliebige Website in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="eb5db-139">The URL for the user's OneDrive for Business site or the URL for any site in your organization.</span></span> <span data-ttu-id="eb5db-140">Verwenden Sie für die URL für OneDrive for Business-Websites das folgende ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `Format:.</span><span class="sxs-lookup"><span data-stu-id="eb5db-140">For the URL for OneDrive for Business sites, use this format: ` https://<your organization>-my.sharepoint.com/personal/<user alias>_<your organization>_onmicrosoft_com `.</span></span> <span data-ttu-id="eb5db-141">Beispiel:  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-141">For example,  `https://contoso-my.sharepoint.com/personal/sarad_contoso_onmicrosoft_com`.</span></span>  <br/> |
    | `ContentMatchQuery` <br/> |<span data-ttu-id="eb5db-142">Die Suchabfrage für die Suche.</span><span class="sxs-lookup"><span data-stu-id="eb5db-142">The search query for the search.</span></span> <span data-ttu-id="eb5db-143">Weitere Informationen zum Erstellen einer Suchabfrage finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="eb5db-143">For more information about creating a search query, see [Keyword queries and search conditions for Content Search](keyword-queries-and-search-conditions.md).</span></span>  <br/> |
    | `StartDate` <br/> |<span data-ttu-id="eb5db-144">Für e-Mails das Datum, an dem oder nachdem eine Nachricht von einem Empfänger empfangen oder vom Absender gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="eb5db-144">For email, the date on or after a message was received by a recipient or sent by the sender.</span></span> <span data-ttu-id="eb5db-145">Für Dokumente auf SharePoint-oder OneDrive für Business-Websites das Datum, an dem oder nachdem ein Dokument zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="eb5db-145">For documents on SharePoint or OneDrive for Business sites, the date on or after a document was last modified.</span></span>  <br/> |
    | `EndDate` <br/> |<span data-ttu-id="eb5db-146">Bei e-Mails wurde das Datum, an dem eine Nachricht vom Benutzer gesendet wurde, an oder vor dem Senden gesendet.</span><span class="sxs-lookup"><span data-stu-id="eb5db-146">For email, the date on or before a message was sent by a sent by the user.</span></span> <span data-ttu-id="eb5db-147">Für Dokumente auf SharePoint-oder OneDrive für Business-Websites das Datum, an dem oder bevor ein Dokument zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="eb5db-147">For documents on SharePoint or OneDrive for Business sites, the date on or before a document was last modified.</span></span>  <br/> |
   
3. <span data-ttu-id="eb5db-148">Speichern Sie die Excel-Datei als CSV-Datei in einem Ordner auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="eb5db-148">Save the Excel file as a CSV file to a folder on your local computer.</span></span> <span data-ttu-id="eb5db-149">Das Skript, das Sie in Schritt 3 erstellen, verwendet die Informationen in dieser CSV-Datei, um die Suchvorgänge zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-149">The script that you create in Step 3 will use the information in this CSV file to create the searches.</span></span> 
  
## <a name="step-2-connect-to-security--compliance-center-powershell"></a><span data-ttu-id="eb5db-150">Schritt 2: Herstellen einer Verbindung mit Security & Compliance Center PowerShell</span><span class="sxs-lookup"><span data-stu-id="eb5db-150">Step 2: Connect to Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="eb5db-151">Der nächste Schritt besteht darin, eine Verbindung zur Security & Compliance Center-PowerShell für Ihre Organisation herzustellen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-151">The next step is to connect to the Security & Compliance Center PowerShell for your organization.</span></span>
  
1. <span data-ttu-id="eb5db-152">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `ConnectSCC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-152">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> <span data-ttu-id="eb5db-153">Speichern Sie die Datei in dem Ordner, in dem Sie die CSV-Datei gespeichert haben, in Schritt 1.</span><span class="sxs-lookup"><span data-stu-id="eb5db-153">Save the file to the same folder that you saved the CSV file to in Step 1.</span></span>
    
    ```
    # Get login credentials 
    $UserCredential = Get-Credential 
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
    Import-PSSession $Session -AllowClobber -DisableNameChecking 
    $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Security & Compliance Center)" 
    ```

2. <span data-ttu-id="eb5db-154">Öffnen Sie auf dem lokalen Computer Windows PowerShell, wechseln Sie zu dem Ordner, in dem sich das Skript befindet, das Sie im vorherigen Schritt erstellt haben, und führen Sie das Skript aus. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eb5db-154">On your local computer, open Windows PowerShell, go to the folder where the script that you created in the previous step is located, and then run the script; for example:</span></span>
    
    ```
    .\ConnectSCC.ps1
    ```
  
## <a name="step-3-run-the-script-to-create-and-start-the-searches"></a><span data-ttu-id="eb5db-155">Schritt 3: Ausführen des Skripts zum Erstellen und Starten der Suche</span><span class="sxs-lookup"><span data-stu-id="eb5db-155">Step 3: Run the script to create and start the searches</span></span>

<span data-ttu-id="eb5db-156">Das Skript in diesem Schritt erstellt eine separate Inhaltssuche für jede Zeile in der CSV-Datei, die Sie in Schritt 1 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="eb5db-156">The script in this step will create a separate Content Search for each row in the CSV file that you created in Step 1.</span></span> <span data-ttu-id="eb5db-157">Wenn Sie dieses Skript ausführen, werden Sie aufgefordert, zwei Werte einzugeben:</span><span class="sxs-lookup"><span data-stu-id="eb5db-157">When you run this script, you'll be prompted for two values:</span></span>
  
- <span data-ttu-id="eb5db-158">**ID der suchgruppe** -dieser Name bietet eine einfache Möglichkeit zum Organisieren der Suchvorgänge, die aus der CSV-Datei erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eb5db-158">**Search Group ID** - This name provides an easy way to organize the searches that are created from the CSV file.</span></span> <span data-ttu-id="eb5db-159">Jede erstellte Suche wird mit der ID der Suchgruppe benannt, und dann wird eine Nummer an den Namen der Suche angehängt.</span><span class="sxs-lookup"><span data-stu-id="eb5db-159">Each search that's created is named with the Search Group ID, and then a number is appended to the search name.</span></span> <span data-ttu-id="eb5db-160">Wenn Sie beispielsweise **ContosoCase** für die ID der suchgruppe eingeben, werden die suchVorgänge als **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**usw. bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="eb5db-160">For example, if you enter **ContosoCase** for the Search Group ID, then the searches are named **ContosoCase_1**, **ContosoCase_2**, **ContosoCase_3**, and so on.</span></span> <span data-ttu-id="eb5db-161">Beachten Sie, dass der von Ihnen eingegebene Name Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="eb5db-161">Note that the name you type is case sensitive.</span></span> <span data-ttu-id="eb5db-162">Wenn Sie die Suchgruppen-ID in Schritt 4 und Schritt 5 verwenden, müssen Sie den gleichen Groß-/Kleinschreibung wie beim Erstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="eb5db-162">When you use the Search Group ID in Step 4 and Step 5, you have to use the same case as you did when you created it.</span></span> 
    
- <span data-ttu-id="eb5db-163">**CSV-Datei** : der Name der CSV-Datei, die Sie in Schritt 1 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="eb5db-163">**CSV file** - The name of the CSV file that you created in Step 1.</span></span> <span data-ttu-id="eb5db-164">Stellen Sie sicher, dass Sie den vollständigen Dateinamen verwenden, die CSV-Dateierweiterung einbeziehen; Beispiel: `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-164">Be sure to include the use the full filename, include the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
<span data-ttu-id="eb5db-165">So führen Sie das Skript aus</span><span class="sxs-lookup"><span data-stu-id="eb5db-165">To run the script:</span></span>

1. <span data-ttu-id="eb5db-166">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `CreateSearches.ps1`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-166">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `CreateSearches.ps1`.</span></span> <span data-ttu-id="eb5db-167">Speichern Sie die Datei in dem Ordner, in dem Sie die anderen Dateien gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="eb5db-167">Save the file to the same folder where you saved the other files.</span></span>
    
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

2. <span data-ttu-id="eb5db-168">Wechseln Sie in Windows PowerShell zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript aus; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eb5db-168">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\CreateSearches.ps1
    ```

3. <span data-ttu-id="eb5db-169">Geben Sie an der Eingabeaufforderungen für die **Suchgruppen-ID** einen Suchgruppen Namen ein, und drücken Sie dann die **Eingabe**Taste. Beispiel: `ContosoCase`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-169">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example,  `ContosoCase`.</span></span> <span data-ttu-id="eb5db-170">Beachten Sie, dass bei diesem Namen die Groß-/Kleinschreibung beachtet wird, sodass Sie Sie in den nachfolgenden Schritten auf die gleiche Art eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-170">Remember that this name is case sensitive, so you'll have to type it the same way in the subsequent steps.</span></span>
    
4. <span data-ttu-id="eb5db-171">Geben Sie an der Eingabeaufforderungen für die **Quell-CSV** -Datei den Namen der CSV-Datei ein, einschließlich der CSV-Dateierweiterung. Beispiel: `ContosoCase.csv`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-171">At the **Source CSV file** prompt, type the name of the CSV file, including the .csv file extension; for example,  `ContosoCase.csv`.</span></span>
    
5. <span data-ttu-id="eb5db-172">Drücken **Sie die Eingabe** Taste, um das Skript zu starten.</span><span class="sxs-lookup"><span data-stu-id="eb5db-172">Press **Enter** to continue running the script.</span></span> 
    
    <span data-ttu-id="eb5db-173">Das Skript zeigt den Fortschritt beim Erstellen und Ausführen der Suche an.</span><span class="sxs-lookup"><span data-stu-id="eb5db-173">The script displays the progress of creating and running the searches.</span></span> <span data-ttu-id="eb5db-174">Wenn das Skript abgeschlossen ist, wird es an die Ansage zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="eb5db-174">When the script is complete, it returns to the prompt.</span></span> 
    
    ![Beispielausgabe vom Ausführen des Skripts zum Erstellen mehrerer Kompatibilitäts Suchvorgänge](media/37d59b0d-5f89-4dbc-9e2d-0e88e2ed7b4c.png)
  
## <a name="step-4-run-the-script-to-report-the-search-estimates"></a><span data-ttu-id="eb5db-176">Schritt 4: Ausführen des Skripts zum Melden der Such Schätzungen</span><span class="sxs-lookup"><span data-stu-id="eb5db-176">Step 4: Run the script to report the search estimates</span></span>

<span data-ttu-id="eb5db-177">Nachdem Sie die Suchvorgänge erstellt haben, besteht der nächste Schritt darin, ein Skript auszuführen, in dem ein einfacher Bericht über die Anzahl der Suchtreffer für jede in Schritt 3 erstellte Suche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="eb5db-177">After you create the searches, the next step is to run a script that displays a simple report of the number of search hits for each search that was created in Step 3.</span></span> <span data-ttu-id="eb5db-178">Der Bericht enthält auch die Größe der Ergebnisse für jede Suche und die Gesamtzahl der Treffer und die Gesamtgröße aller Suchvorgänge.</span><span class="sxs-lookup"><span data-stu-id="eb5db-178">The report also includes the size of results for each search, and the total number of hits and total size of all searches.</span></span> <span data-ttu-id="eb5db-179">Wenn Sie das Bericht Erstellungsskript ausführen, werden Sie aufgefordert, die ID der Suchgruppe und einen CSV-Dateinamen einzugeben, wenn Sie den Bericht in einer CSV speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="eb5db-179">When you run the reporting script, you'll be prompted for the Search Group ID, and a CSV filename if you want to save the report to a CSV file.</span></span>
  
1. <span data-ttu-id="eb5db-180">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `SearchReport.ps1`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-180">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `SearchReport.ps1`.</span></span> <span data-ttu-id="eb5db-181">Speichern Sie die Datei in dem Ordner, in dem Sie die anderen Dateien gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="eb5db-181">Save the file to the same folder where you saved the other files.</span></span>
    
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

2. <span data-ttu-id="eb5db-182">Wechseln Sie in Windows PowerShell zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript aus; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eb5db-182">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\SearchReport.ps1
    ```

3. <span data-ttu-id="eb5db-183">Geben Sie an der Eingabeaufforderungen für die **Suchgruppen-ID** einen Suchgruppen Namen ein, und drücken Sie dann die **Eingabe**Taste. Beispiel `ContosoCase`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-183">At the **Search Group ID** prompt, type a search group name, and then press **Enter**; for example  `ContosoCase`.</span></span> <span data-ttu-id="eb5db-184">Beachten Sie, dass bei diesem Namen die Groß-/Kleinschreibung beachtet wird, sodass Sie Sie so eingeben müssen, wie Sie es auch beim Ausführen des Skripts in Schritt 3 getan haben.</span><span class="sxs-lookup"><span data-stu-id="eb5db-184">Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
4. <span data-ttu-id="eb5db-185">Geben Sie im **Dateipfad zum Speichern des Berichts in einer CSV-Datei (lassen Sie leer, um die Meldung nur anzuzeigen)** einen Dateinamen Vollständiger Dateiname (einschließlich der CSV-Dateierweiterung) ein, wenn Sie den Bericht in einer CSV-Datei speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="eb5db-185">At the **File path to save the report to a CSV file (leave blank to just display the report)** prompt, type a file name of complete filename path (including the .csv file extension) if you want to save the report to a CSV file.</span></span> <span data-ttu-id="eb5db-186">der Name der CSV-Datei, einschließlich der CSV-Dateierweiterung.</span><span class="sxs-lookup"><span data-stu-id="eb5db-186">name of the CSV file, including the .csv file extension.</span></span> <span data-ttu-id="eb5db-187">Sie können beispielsweise eingeben `ContosoCaseReport.csv` , um es im aktuellen Verzeichnis zu speichern, oder Sie können `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` eingeben, um es in einem anderen Ordner zu speichern.</span><span class="sxs-lookup"><span data-stu-id="eb5db-187">For example, you could type  `ContosoCaseReport.csv` to save it to the current directory or you could type  `C:\Users\admin\OneDrive for Business\ContosoCase\ContosoCaseReport.csv` to save it to a different folder.</span></span> <span data-ttu-id="eb5db-188">Sie können die Eingabeaufforderungen auch leer lassen, um den Bericht anzuzeigen, aber nicht in einer Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="eb5db-188">You can also leave the prompt blank to display the report but not save it to a file.</span></span> 
    
5. <span data-ttu-id="eb5db-189">Drücken Sie **EINGABE**.</span><span class="sxs-lookup"><span data-stu-id="eb5db-189">Press **Enter**.</span></span>
    
    <span data-ttu-id="eb5db-190">Das Skript zeigt den Fortschritt beim Erstellen und Ausführen der Suche an.</span><span class="sxs-lookup"><span data-stu-id="eb5db-190">The script displays the progress of creating and running the searches.</span></span> <span data-ttu-id="eb5db-191">Nach Abschluss des Skripts wird der Bericht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eb5db-191">When the script is complete, the report is displayed.</span></span> 
    
    ![Ausführen des Suchberichts zum Anzeigen der Schätzungen für die suchgruppe](media/3b5f2595-71d5-4a14-9214-fad156c981f8.png)
  
> [!NOTE]
> <span data-ttu-id="eb5db-193">Wenn das gleiche Postfach oder die gleiche Website als Inhaltsspeicherort in mehr als einer Suche in einer suchgruppe angegeben wird, kann die geschätzte Summe der Ergebnisse im Bericht (für die Anzahl der Elemente und die Gesamtgröße) Ergebnisse für dieselben Elemente aufweisen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-193">If the same mailbox or site is specified as a content location in more than one search in a search group, the total results estimate in the report (for both the number of items and the total size) might include results for the same items.</span></span> <span data-ttu-id="eb5db-194">Das liegt daran, dass dieselbe e-Mail-Nachricht oder dasselbe Dokument mehr als einmal gezählt wird, wenn Sie mit der Abfrage für verschiedene Suchvorgänge in der suchgruppe übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="eb5db-194">That's because the same email message or document will be counted more than once if it matches the query for different searches in the search group.</span></span> 
  
## <a name="step-5-run-the-script-to-delete-the-searches"></a><span data-ttu-id="eb5db-195">Schritt 5: Ausführen des Skripts zum Löschen der Suchvorgänge</span><span class="sxs-lookup"><span data-stu-id="eb5db-195">Step 5: Run the script to delete the searches</span></span>

<span data-ttu-id="eb5db-196">Da Sie vielleicht viele Suchvorgänge durchführen, ist es mit diesem letzten Skript einfach, die in Schritt 3 erstellten Suchvorgänge schnell zu löschen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-196">Because you might be creating a lot of searches, this last script just makes it easy to quickly delete the searches you created in Step 3.</span></span> <span data-ttu-id="eb5db-197">Wie die anderen Skripts werden Sie auch aufgefordert, die ID der Suchgruppe EINZUGEBEN.</span><span class="sxs-lookup"><span data-stu-id="eb5db-197">Like the other scripts, this one also prompts you for the Search Group ID.</span></span> <span data-ttu-id="eb5db-198">Alle Suchvorgänge mit der Suchgruppen-ID im Suchnamen werden gelöscht, wenn Sie dieses Skript ausführen.</span><span class="sxs-lookup"><span data-stu-id="eb5db-198">All searches with the Search Group ID in the search name will be deleted when you run this script.</span></span> 
  
1. <span data-ttu-id="eb5db-199">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `DeleteSearches.ps1`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-199">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `DeleteSearches.ps1`.</span></span> <span data-ttu-id="eb5db-200">Speichern Sie die Datei in dem Ordner, in dem Sie die anderen Dateien gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="eb5db-200">Save the file to the same folder where you saved the other files.</span></span>
    
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

2. <span data-ttu-id="eb5db-201">Wechseln Sie in Windows PowerShell zu dem Ordner, in dem Sie das Skript im vorherigen Schritt gespeichert haben, und führen Sie das Skript aus; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eb5db-201">In Windows PowerShell, go to the folder where you saved the script in the previous step, and then run the script; for example:</span></span>
    
    ```Powershell
    .\DeleteSearches.ps1
    ```

3. <span data-ttu-id="eb5db-202">Geben Sie an der Eingabeaufforderungen für die **Suchgruppen-ID** einen Suchgruppen Namen für die Suchvorgänge ein, die Sie löschen möchten, und drücken Sie dann die **Eingabe**Taste. Beispiel: `ContosoCase`.</span><span class="sxs-lookup"><span data-stu-id="eb5db-202">At the **Search Group ID** prompt, type a search group name for the searches that you want to delete, and then press **Enter**; for example,  `ContosoCase`.</span></span> <span data-ttu-id="eb5db-203">Beachten Sie, dass bei diesem Namen die Groß-/Kleinschreibung beachtet wird, sodass Sie Sie so eingeben müssen, wie Sie es auch beim Ausführen des Skripts in Schritt 3 getan haben.</span><span class="sxs-lookup"><span data-stu-id="eb5db-203">Remember that this name is case sensitive, so you'll have to type it the same way you did when you ran the script in Step 3.</span></span>
    
    <span data-ttu-id="eb5db-204">Das Skript zeigt den Namen jeder gelöschten Suche an.</span><span class="sxs-lookup"><span data-stu-id="eb5db-204">The script displays the name of each search that's deleted.</span></span>
    
    ![Ausführen des Skripts zum Löschen der Suchvorgänge in der Gruppe "Suche"](media/9d97b9d6-a539-4d9b-a4e4-e99989144ec7.png)
