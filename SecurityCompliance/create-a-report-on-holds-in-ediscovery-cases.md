---
title: Erstellen eines Berichts in Archiven in eDiscovery-Fälle in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/11/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: Verwenden Sie das Skript einen Bericht mit Informationen über alle Haltestatus, die eDiscovery-Fälle in die Office 365-Sicherheit zugeordnet sind in diesem Artikel &amp; Compliance Center.
ms.openlocfilehash: 8bc1285f776e2b1aa0c0330c06ccffff8ce4585c
ms.sourcegitcommit: c166964fe14eec69139a2d3d9c10d2c40ab33f91
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2018
ms.locfileid: "23258643"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a><span data-ttu-id="658cc-103">Erstellen eines Berichts in Archiven in eDiscovery-Fälle in Office 365</span><span class="sxs-lookup"><span data-stu-id="658cc-103">Create a report on holds in eDiscovery cases in Office 365</span></span>
  
<span data-ttu-id="658cc-p101">Das Skript in diesem Artikel kann Administratoren die eDiscovery und eDiscovery-Manager erstellen Sie einen Bericht mit Informationen über alle Haltestatus, die eDiscovery-Fälle in die Office 365-Sicherheit zugeordnet sind &amp; Compliance Center. Der Bericht enthält Informationen, wie der Name der Anfrage einem Haltebereich zugeordnet, die Speicherorte für Inhalte, die in der Warteschleife platziert werden und ob die Sperre abfragebasierter ist. Wenn Anfragen, die nicht über einen Haltestatus verfügen vorhanden sind, wird das Skript einen Bericht zusätzlichen mit einer Liste von Fällen ohne Haltestatus erstellen.</span><span class="sxs-lookup"><span data-stu-id="658cc-p101">The script in this article lets eDiscovery administrators and eDiscovery managers generate a report that contains information about all holds that are associated with eDiscovery cases in the Office 365 Security &amp; Compliance Center. The report contains information such as the name of the case a hold is associated with, the content locations that are placed on hold, and whether the hold is query-based. If there are cases that don't have any holds, the script will create an additional report with a list of cases without holds.</span></span>

<span data-ttu-id="658cc-107">Finden Sie [Weitere Informationen](#more-information) im Abschnitt eine ausführliche Beschreibung der Informationen in den Bericht einbezogen.</span><span class="sxs-lookup"><span data-stu-id="658cc-107">See the [More information](#more-information) section for a detailed description of the information included in the report.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="658cc-108">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="658cc-108">Before you begin</span></span>

- <span data-ttu-id="658cc-p102">Um einen Bericht über alle eDiscovery-Fälle in Ihrer Organisation generiert werden soll, müssen Sie eine eDiscovery-Administrator in Ihrer Organisation sein. Wenn Sie ein eDiscovery-Manager sind, wird der Bericht nur Informationen zu den Fällen berücksichtigen, die Sie zugreifen können. Weitere Informationen zu eDiscovery-Berechtigungen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="658cc-p102">To generate a report on all eDiscovery cases in your organization, you have to be an eDiscovery Administrator in your organization. If you are an eDiscovery Manager, the report will only include information about the cases that you can access. For more information about eDiscovery permissions, see [Assign eDiscovery permissions in the Office‍ 365 Security &amp; Compliance Center](assign-ediscovery-permissions.md).</span></span>
    
- <span data-ttu-id="658cc-p103">Das Skript in diesem Artikel enthält minimale Fehlerbehandlung. Der primäre Zweck ist Bericht zu den Haltebereichen schnell zu erstellen, die eDiscovery-Fälle in Ihrer Organisation zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="658cc-p103">The script in this article has minimal error handling. The primary purpose is to quickly create report about the holds that are associated with the eDiscovery cases in your organization.</span></span>
    
- <span data-ttu-id="658cc-p104">In diesem Thema bereitgestellten Beispielskripts werden unter keinem standard Support-Programm von Microsoft oder der Dienst nicht unterstützt. Die Beispielskripts werden wie besehen ohne jede Gewährleistung bereitgestellt. Microsoft schließt alle konkludente Garantien einschließlich, aber nicht beschränkt auf konkludente Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck. Das gesamte Risiko aus der Verwendung oder der Leistung der Beispielskripts und der Dokumentation liegt bei Ihnen. In keinem Fall muss Microsoft, seine Autoren oder ein Benutzer die Erstellung, Produktion oder Übermittlung der Skripts else beteiligt für Schäden jeglicher Art (einschließlich, aber nicht beschränkt auf Schäden für den Verlust von Gewinn Business, Business Unterbrechung, Verlust von Unternehmensinformationen, Folge- oder) aus der Verwendung des oder der Fehler beim Verwenden der Beispielskripts oder der Dokumentation, haftbar gemacht werden, auch wenn Microsoft die Möglichkeit solcher Schäden hingewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="658cc-p104">The sample scripts provided in this topic aren't supported under any Microsoft standard support program or service. The sample scripts are provided AS IS without warranty of any kind. Microsoft further disclaims all implied warranties including, without limitation, any implied warranties of merchantability or of fitness for a particular purpose. The entire risk arising out of the use or performance of the sample scripts and documentation remains with you. In no event shall Microsoft, its authors, or anyone else involved in the creation, production, or delivery of the scripts be liable for any damages whatsoever (including, without limitation, damages for loss of business profits, business interruption, loss of business information, or other pecuniary loss) arising out of the use of or inability to use the sample scripts or documentation, even if Microsoft has been advised of the possibility of such damages.</span></span>
    
## <a name="step-1-connect-to-the-security-amp-compliance-center-using-remote-powershell"></a><span data-ttu-id="658cc-119">Schritt 1: Verbinden mit der Sicherheit &amp; Compliance Center mit Remote-PowerShell</span><span class="sxs-lookup"><span data-stu-id="658cc-119">Step 1: Connect to the Security &amp; Compliance Center using Remote PowerShell</span></span>

<span data-ttu-id="658cc-120">Der erste Schritt besteht Verbindung von Windows PowerShell für die Sicherheit &amp; Compliance Center für Ihre Organisation.</span><span class="sxs-lookup"><span data-stu-id="658cc-120">The first step is to connect Windows PowerShell to the Security &amp; Compliance Center for your organization.</span></span>
  
1. <span data-ttu-id="658cc-121">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `ConnectSCC.ps1`.</span><span class="sxs-lookup"><span data-stu-id="658cc-121">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `ConnectSCC.ps1`.</span></span> 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. <span data-ttu-id="658cc-122">Öffnen Sie auf dem lokalen Computer Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="658cc-122">On your local computer, open Windows PowerShell and go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="658cc-123">Führen Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="658cc-123">Run the script; for example:</span></span>

    ```
    .\ConnectSCC.ps1
    ```
   
4. <span data-ttu-id="658cc-124">Geben Sie nach Ihren Anmeldeinformationen gefragt Ihre e-Mail-Adresse und das Kennwort ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="658cc-124">When prompted for your credentials, enter your email address and password, and then click **OK**.</span></span> 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a><span data-ttu-id="658cc-125">Schritt 2: Ausführen enthält des Skripts in den Bericht eDiscovery-Fälle zugeordnet</span><span class="sxs-lookup"><span data-stu-id="658cc-125">Step 2: Run the script to report on holds associated with eDiscovery cases</span></span>

<span data-ttu-id="658cc-126">Nachdem Sie die Sicherheit verbunden sind &amp; Compliance Center mit remote-PowerShell, im nächsten Schritt erstellen und Ausführen des Skripts, das Informationen über die eDiscovery-Fälle in Ihrer Organisation erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="658cc-126">After you've connected to the Security &amp; Compliance Center with remote PowerShell, the next step is to create and run the script that collects information about the eDiscovery cases in your organization.</span></span> 
  
1. <span data-ttu-id="658cc-127">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise CaseHoldsReport.ps1.</span><span class="sxs-lookup"><span data-stu-id="658cc-127">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, CaseHoldsReport.ps1.</span></span> 
    
  ```
#script begin
" " 
write-host "***********************************************"
write-host "   Office 365 Security & Compliance Center   " -foregroundColor yellow -backgroundcolor darkgreen
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

2. <span data-ttu-id="658cc-128">In der Windows PowerShell-Sitzung, die in Schritt 1 geöffnet, wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="658cc-128">In the Windows PowerShell session that opened in Step 1, go to the folder where you saved the script.</span></span> 
    
3. <span data-ttu-id="658cc-129">Führen Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="658cc-129">Run the script; for example:</span></span>

    ```
    .\CaseHoldsReport.ps1
    ```

    <span data-ttu-id="658cc-130">Das Skript fordert einen Zielordner aus, um den Bericht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="658cc-130">The script will prompt for a target folder to save the report to.</span></span> 
    
4. <span data-ttu-id="658cc-131">Geben Sie den vollständigen Pfadnamen des Ordners, in den Bericht zu speichern, und drücken Sie die **EINGABETASTE**.</span><span class="sxs-lookup"><span data-stu-id="658cc-131">Type the full path name of the folder to save the report to, and then press **Enter**.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="658cc-p105">Um den Bericht im selben Ordner zu speichern, die in das Skript gespeichert ist, geben Sie einen Punkt (".") Wenn Sie einen Zielordner aufgefordert werden. Um den Bericht in einem Unterordner im Ordner zu speichern, in das Skript gespeichert ist, geben Sie einfach den Namen des Unterordners.</span><span class="sxs-lookup"><span data-stu-id="658cc-p105">To save the report in the same folder that the script is located in, type a period (".") when prompted for a target folder. To save the report in a subfolder in the folder where the script is located, just type the name of the subfolder.</span></span> 
  
    <span data-ttu-id="658cc-p106">Das Skript startet das Erfassen von Informationen zu den eDiscovery-Fällen in Ihrer Organisation. Greifen Sie auf nicht Berichtsdatei während der Ausführung des Skripts. Nachdem das Skript abgeschlossen ist, wird eine Meldung zur Bestätigung in der Windows PowerShell-Sitzung angezeigt. Nachdem diese Meldung angezeigt wird, können Sie den Bericht im Ordner zugreifen, die Sie in Schritt 4 angegeben. Der Dateiname für den Bericht ist `CaseHoldsReport<DateTimeStamp>.csv`.</span><span class="sxs-lookup"><span data-stu-id="658cc-p106">The script starts to collect information about all the eDiscovery cases in your organization. Don't access the report file while the script is running. After the script is complete, a confirmation message is displayed in the Windows PowerShell session. After this message is displayed, you can access the report in the folder that you specified in Step 4. The file name for the report is `CaseHoldsReport<DateTimeStamp>.csv`.</span></span>

    <span data-ttu-id="658cc-p107">Auch, erstellt das Skript auch einen Bericht mit einer Liste von Anfragen, die nicht über einen Haltestatus verfügen. Der Dateiname für diesen Bericht ist `CaseswithNoHolds<DateTimeStamp>.csv`.</span><span class="sxs-lookup"><span data-stu-id="658cc-p107">Addtionally, the script also creates a report with a list of cases that don't have any holds. The file name for this report is `CaseswithNoHolds<DateTimeStamp>.csv`.</span></span>
    
    <span data-ttu-id="658cc-141">Es folgt ein Beispiel der Ausführung des Skripts CaseHoldsReport.ps1.</span><span class="sxs-lookup"><span data-stu-id="658cc-141">Here's an example of running the CaseHoldsReport.ps1 script.</span></span> 
    
    ![Die Ausgabe nach der Ausführung des Skripts CaseHoldsReport.ps1](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a><span data-ttu-id="658cc-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="658cc-143">More information</span></span>

<span data-ttu-id="658cc-p108">Die Groß-/Kleinschreibung enthält Bericht, der beim Ausführen des Skripts in diesem Artikel erstellt wird, die folgende Informationen zu jedem Haltebereich enthält. Wie bereits erklärt müssen Sie eine eDiscovery-Administrator sein, um die Informationen für alle Haltestatus in Ihrer Organisation zurückgegeben werden. Weitere Informationen zu Fall enthält, finden Sie unter [eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](ediscovery-cases.md).</span><span class="sxs-lookup"><span data-stu-id="658cc-p108">The case holds report that's created when you run the script in this article contains the following information about each hold. As previously explained, you have to be an eDiscovery Administrator to return information for all holds in your organization. For more information about case holds, see [eDiscovery cases in the Office 365 Security &amp; Compliance Center](ediscovery-cases.md).</span></span>
  
  - <span data-ttu-id="658cc-147">Der Name des Haltestatus und den Namen der eDiscovery-Fall, die der Haltebereich zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="658cc-147">The name of the hold and the name of the eDiscovery case that the hold is associated with.</span></span>
    
  - <span data-ttu-id="658cc-148">Unabhängig davon, ob die eDiscovery-Fall aktiv oder geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="658cc-148">Whether or not the eDiscovery case is active or closed.</span></span>
    
  - <span data-ttu-id="658cc-149">Unabhängig davon, ob die Sperre aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="658cc-149">Whether or not the hold is enabled or disabled.</span></span>
    
  - <span data-ttu-id="658cc-p109">Die Mitglieder von eDiscovery-Fall, die der Haltebereich zugeordnet ist. Groß-/Kleinschreibung Mitglieder können anzeigen und verwalten eine Anfrage, abhängig von den eDiscovery-Berechtigungen, die sie zugewiesen wurde, haben.</span><span class="sxs-lookup"><span data-stu-id="658cc-p109">The members of the eDiscovery case that the hold is associated with. Case members can view or manage a case, depending on the eDiscovery permissions they've been assigned.</span></span>
    
  - <span data-ttu-id="658cc-152">Datum und die Uhrzeit der Erstellung die Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="658cc-152">The time and date the case was created.</span></span>
    
  - <span data-ttu-id="658cc-153">Wenn eine Anfrage geschlossen ist, wurde die Person, die geschlossen wurde, und die Uhrzeit und Datum geschlossen.</span><span class="sxs-lookup"><span data-stu-id="658cc-153">If a case is closed, the person who closed it and the time and date it was closed.</span></span>
    
  - <span data-ttu-id="658cc-154">Die Exchange-Postfächern und SharePoint-Websites Speicherorte, die in der Warteschleife sind.</span><span class="sxs-lookup"><span data-stu-id="658cc-154">The Exchange mailboxes and SharePoint sites locations that are on hold.</span></span>
    
  - <span data-ttu-id="658cc-155">Wenn die Sperre abfragebasierte, ist die Abfragesyntax.</span><span class="sxs-lookup"><span data-stu-id="658cc-155">If the hold is query-based, the query syntax.</span></span>
    
  - <span data-ttu-id="658cc-156">Die Zeit und Datum, an dem Haltebereich erstellt wurde und die Person, die sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="658cc-156">The time and date the hold was created and the person who created it.</span></span>
    
  - <span data-ttu-id="658cc-157">Die Zeit und Datum, an dem Haltebereich zuletzt geändert wurde und die Person, die sie geändert.</span><span class="sxs-lookup"><span data-stu-id="658cc-157">The time and date the hold was last changed and the person who changed it.</span></span>
