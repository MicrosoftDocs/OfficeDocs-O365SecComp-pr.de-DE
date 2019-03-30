---
title: Erstellen eines Berichts zu Haltebereichen in eDiscovery-Fällen in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: Verwenden Sie das Skript in diesem Artikel, um einen Bericht zu generieren, der Informationen zu allen Haltebereichen enthält, die eDiscovery-Fällen im Compliance Center in Office 365 oder Microsoft 365 zugeordnet sind.
ms.openlocfilehash: db5a462087dd20ed71f87efe2fd83b821654f1b9
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000878"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a><span data-ttu-id="fefed-103">Erstellen eines Berichts zu Haltebereichen in eDiscovery-Fällen in Office 365</span><span class="sxs-lookup"><span data-stu-id="fefed-103">Create a report on holds in eDiscovery cases in Office 365</span></span>
  
<span data-ttu-id="fefed-104">Mit dem Skript in diesem Artikel können eDiscovery-Administratoren und eDiscovery-Manager einen Bericht generieren, der Informationen zu allen Haltebereichen enthält, die eDiscovery-Fällen im Compliance Center in Office 365 oder Microsoft 365 zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fefed-104">The script in this article lets eDiscovery administrators and eDiscovery managers generate a report that contains information about all holds that are associated with eDiscovery cases in the the compliance center in Office 365 or Microsoft 365.</span></span> <span data-ttu-id="fefed-105">Der Bericht enthält Informationen wie den Namen des Falls, dem ein Haltebereich zugeordnet ist, die inhaltsspeicherorte, die in die Warteschleife gestellt werden, und ob die Aufbewahrung Abfrage basiert ist.</span><span class="sxs-lookup"><span data-stu-id="fefed-105">The report contains information such as the name of the case a hold is associated with, the content locations that are placed on hold, and whether the hold is query-based.</span></span> <span data-ttu-id="fefed-106">Wenn es Fälle gibt, in denen keine haltebereiche vorhanden sind, erstellt das Skript einen zusätzlichen Bericht mit einer Liste von Fällen ohne Aufbewahrung.</span><span class="sxs-lookup"><span data-stu-id="fefed-106">If there are cases that don't have any holds, the script will create an additional report with a list of cases without holds.</span></span>

<span data-ttu-id="fefed-107">Im Abschnitt [Weitere Informationen](#more-information) finden Sie eine ausführliche Beschreibung der im Bericht enthaltenen Informationen.</span><span class="sxs-lookup"><span data-stu-id="fefed-107">See the [More information](#more-information) section for a detailed description of the information included in the report.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="fefed-108">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="fefed-108">Before you begin</span></span>

- <span data-ttu-id="fefed-109">Wenn Sie einen Bericht zu allen eDiscovery-Fällen in Ihrer Organisation generieren möchten, müssen Sie ein eDiscovery-Administrator in Ihrer Organisation sein.</span><span class="sxs-lookup"><span data-stu-id="fefed-109">To generate a report on all eDiscovery cases in your organization, you have to be an eDiscovery Administrator in your organization.</span></span> <span data-ttu-id="fefed-110">Wenn Sie ein eDiscovery-Manager sind, enthält der Bericht nur Informationen zu den Fällen, auf die Sie zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="fefed-110">If you are an eDiscovery Manager, the report will only include information about the cases that you can access.</span></span> <span data-ttu-id="fefed-111">Weitere Informationen zu eDiscovery-Berechtigungen finden Sie unter [assign eDiscovery Permissions](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="fefed-111">For more information about eDiscovery permissions, see [Assign eDiscovery permissions](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="fefed-112">Das Skript in diesem Artikel hat eine minimale Fehlerbehandlung.</span><span class="sxs-lookup"><span data-stu-id="fefed-112">The script in this article has minimal error handling.</span></span> <span data-ttu-id="fefed-113">Der Hauptzweck besteht darin, Schnellbericht zu den Haltebereichen zu erstellen, die den eDiscovery-Fällen in Ihrer Organisation zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="fefed-113">The primary purpose is to quickly create report about the holds that are associated with the eDiscovery cases in your organization.</span></span>
    
- <span data-ttu-id="fefed-p104">Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.</span><span class="sxs-lookup"><span data-stu-id="fefed-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-connect-to-the-security--compliance-center-powershell"></a><span data-ttu-id="fefed-119">Schritt 1: Herstellen einer Verbindung mit der Security & Compliance Center-PowerShell</span><span class="sxs-lookup"><span data-stu-id="fefed-119">Step 1: Connect to the Security & Compliance Center PowerShell</span></span>

<span data-ttu-id="fefed-120">Der erste Schritt besteht darin, eine Verbindung zum Security & Compliance Center für Ihre Organisation herzustellen.</span><span class="sxs-lookup"><span data-stu-id="fefed-120">The first step is to connect to the Security & Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="fefed-121">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `ConnectSCC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="fefed-121">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Security & Compliance Center)" 
    ```

2. <span data-ttu-id="fefed-122">Öffnen Sie auf dem lokalen Computer Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="fefed-122">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="fefed-123">Führen Sie das Skript aus; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fefed-123">Run the script; for example:</span></span>

    ```
    .\ConnectSCC.ps1
    ```
   
4. <span data-ttu-id="fefed-124">Wenn Sie zur Eingabe Ihrer Anmeldeinformationen aufgefordert werden, geben Sie Ihre e-Mail-Adresse und Ihr Kennwort ein, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="fefed-124">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a><span data-ttu-id="fefed-125">Schritt 2: Ausführen des Skripts zum Melden von Haltebereichen im Zusammenhang mit eDiscovery-Fällen</span><span class="sxs-lookup"><span data-stu-id="fefed-125">Step 2: Run the script to report on holds associated with eDiscovery cases</span></span>

<span data-ttu-id="fefed-126">Nachdem Sie eine Verbindung mit Security & Compliance Center PowerShell hergestellt haben, besteht der nächste Schritt darin, das Skript zu erstellen und auszuführen, das Informationen zu den eDiscovery-Fällen in Ihrer Organisation sammelt.</span><span class="sxs-lookup"><span data-stu-id="fefed-126">After you've connected to Security & Compliance Center PowerShell, the next step is to create and run the script that collects information about the eDiscovery cases in your organization.</span></span> 
  
1. <span data-ttu-id="fefed-127">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: CaseHoldsReport. ps1.</span><span class="sxs-lookup"><span data-stu-id="fefed-127">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, CaseHoldsReport.ps1.</span></span> 
    
  ```
#script begin
" " 
write-host "***********************************************"
write-host "   Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
write-host "        eDiscovery cases - Holds report         " -foregroundColor yellow -backgroundcolor darkgreen 
write-host "***********************************************"
" " 
#prompt users to specify a path to store the output files
$time=get-date
$Path = Read-Host 'Enter a file path to save the report to a .csv file'
$outputpath=$Path+'\'+'CaseHoldsReport'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
$noholdsfilepath=$Path+'\'+'CaseswithNoHolds'+' '+$time.day+'-'+$time.month+'-'+$time.year+' '+$time.hour+'.'+$time.minute+'.csv'
#add case details to the csv file
function add-tocasereport{
Param([string]$casename,
[String]$casestatus,
[datetime]$casecreatedtime,
[string]$casemembers,
[datetime]$caseClosedDateTime,
[string]$caseclosedby,
[string]$holdname,
[String]$Holdenabled,
[string]$holdcreatedby,
[string]$holdlastmodifiedby,
[string]$ExchangeLocation,
[string]$sharePointlocation,
[string]$ContentMatchQuery,
[datetime]$holdcreatedtime,
[datetime]$holdchangedtime
)
$addRow = New-Object PSObject 
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case name" -Value $casename
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case status" -Value $casestatus
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case members" -Value $casemembers
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case created time" -Value $casecreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed time" -Value $caseClosedDateTime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Case closed by" -Value $caseclosedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold name" -Value $holdname
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold enabled" -Value $Holdenabled
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created by" -Value $holdcreatedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold last changed by" -Value $holdlastmodifiedby
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Exchange locations" -Value  $ExchangeLocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "SharePoint locations" -Value $sharePointlocation
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold query" -Value $ContentMatchQuery
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold created time (UTC)" -Value $holdcreatedtime
Add-Member -InputObject $addRow -MemberType NoteProperty -Name "Hold changed time (UTC)" -Value $holdchangedtime
$allholdreport = $addRow | Select-Object "Case name","Case status","Hold name","Hold enabled","Case members", "Case created time","Case closed time","Case closed by","Exchange locations","SharePoint locations","Hold query","Hold created by","Hold created time (UTC)","Hold last changed by","Hold changed time (UTC)"
$allholdreport | export-csv -path $outputPath -notypeinfo -append -Encoding ascii 
}
#get information on the cases and pass values to the case report function
" "
write-host "Gathering a list of cases and holds..."
" "
$edc =Get-ComplianceCase -ErrorAction SilentlyContinue
foreach($cc in $edc)
{
write-host "Working on case :" $cc.name
if($cc.status -eq 'Closed')
{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
add-tocasereport -casename $cc.name -casestatus $cc.Status -caseclosedby $cc.closedby -caseClosedDateTime $cc.ClosedDateTime -casemembers $cmembers 
}
else{
$cmembers = ((Get-ComplianceCaseMember -Case $cc.name).windowsLiveID)-join ';'
$policies = Get-CaseHoldPolicy -Case $cc.Name | %{ Get-CaseHoldPolicy $_.Name -Case $_.CaseId -DistributionDetail}
if ($policies -ne $NULL)
{
foreach ($policy in $policies)
{
$rule=Get-CaseHoldRule -Policy $policy.name
add-tocasereport -casename $cc.name -casemembers $cmembers -casestatus $cc.Status -casecreatedtime $cc.CreatedDateTime -holdname $policy.name -holdenabled $policy.enabled -holdcreatedby $policy.CreatedBy -holdlastmodifiedby $policy.LastModifiedBy -ExchangeLocation (($policy.exchangelocation.name)-join ';') -SharePointLocation (($policy.sharePointlocation.name)-join ';') -ContentMatchQuery $rule.ContentMatchQuery -holdcreatedtime $policy.WhenCreatedUTC -holdchangedtime $policy.WhenChangedUTC
}
}
else{
write-host "No hold policies found in case:" $cc.name -foregroundColor 'Yellow'
" "
[string]$cc.name | out-file -filepath $noholdsfilepath -append 
}
}
}

" "
Write-host "Script complete! Report files saved to this folder: '$Path'"
" "
#script end
  ```

2. <span data-ttu-id="fefed-128">Wechseln Sie in der Windows PowerShell-Sitzung, die in Schritt 1 geöffnet wurde, zu dem Ordner, in dem Sie das Skript gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="fefed-128">In the Windows PowerShell session that opened in Step 1, go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="fefed-129">Führen Sie das Skript aus; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="fefed-129">Run the script; for example:</span></span>

    ```
    .\CaseHoldsReport.ps1
    ```

    <span data-ttu-id="fefed-130">Das Skript fordert einen Zielordner an, in dem der Bericht gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="fefed-130">The script will prompt for a target folder to save the report to.</span></span> 
    
4. <span data-ttu-id="fefed-131">Geben Sie den vollständigen Pfadnamen des Ordners ein, in dem der Bericht gespeichert werden soll, und drücken Sie dann die **Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="fefed-131">Type the full path name of the folder to save the report to, and then press **Enter**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="fefed-132">Zum Speichern des Berichts in demselben Ordner, in dem sich das Skript befindet, geben Sie einen Punkt (".") ein, wenn Sie für einen Zielordner aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="fefed-132">To save the report in the same folder that the script is located in, type a period (".") when prompted for a target folder.</span></span> <span data-ttu-id="fefed-133">Zum Speichern des Berichts in einem Unterordner in dem Ordner, in dem sich das Skript befindet, geben Sie einfach den Namen des Unterordners ein.</span><span class="sxs-lookup"><span data-stu-id="fefed-133">To save the report in a subfolder in the folder where the script is located, just type the name of the subfolder.</span></span> 
  
    <span data-ttu-id="fefed-134">Das Skript fängt an, Informationen zu allen eDiscovery-Fällen in Ihrer Organisation zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="fefed-134">The script starts to collect information about all the eDiscovery cases in your organization.</span></span> <span data-ttu-id="fefed-135">Greifen Sie während des Skripts nicht auf die Berichtsdatei zu.</span><span class="sxs-lookup"><span data-stu-id="fefed-135">Don't access the report file while the script is running.</span></span> <span data-ttu-id="fefed-136">Nach Abschluss des Skripts wird in der Windows PowerShell-Sitzung eine Bestätigungsmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fefed-136">After the script is complete, a confirmation message is displayed in the Windows PowerShell session.</span></span> <span data-ttu-id="fefed-137">Nachdem diese Meldung angezeigt wurde, können Sie auf den Bericht in dem Ordner zugreifen, den Sie in Schritt 4 angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="fefed-137">After this message is displayed, you can access the report in the folder that you specified in Step 4.</span></span> <span data-ttu-id="fefed-138">Der Dateiname für den Bericht lautet `CaseHoldsReport<DateTimeStamp>.csv`.</span><span class="sxs-lookup"><span data-stu-id="fefed-138">The file name for the report is `CaseHoldsReport<DateTimeStamp>.csv`.</span></span>

    <span data-ttu-id="fefed-139">Außerdem erstellt das Skript einen Bericht mit einer Liste von Fällen, die keine haltebereiche enthalten.</span><span class="sxs-lookup"><span data-stu-id="fefed-139">Addtionally, the script also creates a report with a list of cases that don't have any holds.</span></span> <span data-ttu-id="fefed-140">Der Dateiname für diesen Bericht lautet `CaseswithNoHolds<DateTimeStamp>.csv`.</span><span class="sxs-lookup"><span data-stu-id="fefed-140">The file name for this report is `CaseswithNoHolds<DateTimeStamp>.csv`.</span></span>
    
    <span data-ttu-id="fefed-141">Nachfolgend finden Sie ein Beispiel für die Verwendung des CaseHoldsReport. ps1-Skripts.</span><span class="sxs-lookup"><span data-stu-id="fefed-141">Here's an example of running the CaseHoldsReport.ps1 script.</span></span> 
    
    ![Die Ausgabe nach dem Ausführen des CaseHoldsReport. ps1-Skripts](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a><span data-ttu-id="fefed-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="fefed-143">More information</span></span>

<span data-ttu-id="fefed-144">Der Fall enthält Bericht, der erstellt wird, wenn Sie das Skript in diesem Artikel ausführen enthält die folgenden Informationen zu den einzelnen Haltebereichen.</span><span class="sxs-lookup"><span data-stu-id="fefed-144">The case holds report that's created when you run the script in this article contains the following information about each hold.</span></span> <span data-ttu-id="fefed-145">Wie bereits erläutert, müssen Sie ein eDiscovery-Administrator sein, um Informationen für alle haltebereiche in Ihrer Organisation zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="fefed-145">As previously explained, you have to be an eDiscovery Administrator to return information for all holds in your organization.</span></span> <span data-ttu-id="fefed-146">Weitere Informationen zu Case Holds finden Sie unter [eDiscovery Cases](ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="fefed-146">For more information about case holds, see [eDiscovery cases](ediscovery-cases.md).</span></span>
  
  - <span data-ttu-id="fefed-147">Der Name des haltebereichs und der Name des eDiscovery-Falls, dem der Haltebereich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fefed-147">The name of the hold and the name of the eDiscovery case that the hold is associated with.</span></span>
    
  - <span data-ttu-id="fefed-148">Gibt an, ob der eDiscovery-Fall aktiv oder geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fefed-148">Whether or not the eDiscovery case is active or closed.</span></span>
    
  - <span data-ttu-id="fefed-149">Gibt an, ob der Haltestatus aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fefed-149">Whether or not the hold is enabled or disabled.</span></span>
    
  - <span data-ttu-id="fefed-150">Die Mitglieder des eDiscovery-Falls, dem der Haltebereich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fefed-150">The members of the eDiscovery case that the hold is associated with.</span></span> <span data-ttu-id="fefed-151">Fall Mitglieder können eine Groß-/Kleinschreibung abhängig von den Ihnen zugewiesenen eDiscovery-Berechtigungen anzeigen oder verwalten.</span><span class="sxs-lookup"><span data-stu-id="fefed-151">Case members can view or manage a case, depending on the eDiscovery permissions they've been assigned.</span></span>
    
  - <span data-ttu-id="fefed-152">Die Uhrzeit und das Datum, an dem die Anfrage erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="fefed-152">The time and date the case was created.</span></span>
    
  - <span data-ttu-id="fefed-153">Wenn eine Groß-/Kleinschreibung geschlossen wird, die Person, die Sie geschlossen hat, und die Uhrzeit und das Datum, zu dem Sie geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fefed-153">If a case is closed, the person who closed it and the time and date it was closed.</span></span>
    
  - <span data-ttu-id="fefed-154">Die Speicherorte von Exchange-Postfächern und SharePoint-Websites.</span><span class="sxs-lookup"><span data-stu-id="fefed-154">The Exchange mailboxes and SharePoint sites locations that are on hold.</span></span>
    
  - <span data-ttu-id="fefed-155">Wenn der Haltebereich Abfrage basiert ist, wird die Abfragesyntax.</span><span class="sxs-lookup"><span data-stu-id="fefed-155">If the hold is query-based, the query syntax.</span></span>
    
  - <span data-ttu-id="fefed-156">Die Uhrzeit und das Datum, an dem die Aufbewahrungszeit erstellt wurde, und die Person, die Sie erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="fefed-156">The time and date the hold was created and the person who created it.</span></span>
    
  - <span data-ttu-id="fefed-157">Uhrzeit und Datum der letzten Änderung und die Person, die Sie geändert hat.</span><span class="sxs-lookup"><span data-stu-id="fefed-157">The time and date the hold was last changed and the person who changed it.</span></span>
