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
search.appverid: MOE150
ms.assetid: cca08d26-6fbf-4b2c-b102-b226e4cd7381
description: Verwenden Sie das Skript einen Bericht mit Informationen über alle Haltestatus, die eDiscovery-Fälle in die Office 365-Sicherheit zugeordnet sind in diesem Artikel &amp; Compliance Center.
ms.openlocfilehash: b6cef2824002d7e45e4f500bc6c1e9bc880cbd41
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038208"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a>Erstellen eines Berichts in Archiven in eDiscovery-Fälle in Office 365
  
Das Skript in diesem Artikel kann Administratoren die eDiscovery und eDiscovery-Manager erstellen Sie einen Bericht mit Informationen über alle Haltestatus, die eDiscovery-Fälle in die Office 365-Sicherheit zugeordnet sind &amp; Compliance Center. Der Bericht enthält Informationen, wie der Name der Anfrage einem Haltebereich zugeordnet, die Speicherorte für Inhalte, die in der Warteschleife platziert werden und ob die Sperre abfragebasierter ist. Wenn Anfragen, die nicht über einen Haltestatus verfügen vorhanden sind, wird das Skript einen Bericht zusätzlichen mit einer Liste von Fällen ohne Haltestatus erstellen.

Finden Sie [Weitere Informationen](#more-information) im Abschnitt eine ausführliche Beschreibung der Informationen in den Bericht einbezogen. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Um einen Bericht über alle eDiscovery-Fälle in Ihrer Organisation generiert werden soll, müssen Sie eine eDiscovery-Administrator in Ihrer Organisation sein. Wenn Sie ein eDiscovery-Manager sind, wird der Bericht nur Informationen zu den Fällen berücksichtigen, die Sie zugreifen können. Weitere Informationen zu eDiscovery-Berechtigungen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](assign-ediscovery-permissions.md).
    
- Das Skript in diesem Artikel enthält minimale Fehlerbehandlung. Der primäre Zweck ist Bericht zu den Haltebereichen schnell zu erstellen, die eDiscovery-Fälle in Ihrer Organisation zugeordnet sind.
    
- Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.
    
## <a name="step-1-connect-to-the-security-amp-compliance-center-using-remote-powershell"></a>Schritt 1: Verbinden mit der Sicherheit &amp; Compliance Center mit Remote-PowerShell

Der erste Schritt besteht Verbindung von Windows PowerShell für die Sicherheit &amp; Compliance Center für Ihre Organisation.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `ConnectSCC.ps1`. 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben. 
    
3. Führen Sie das Skript; Zum Beispiel:

    ```
    .\ConnectSCC.ps1
    ```
   
4. Geben Sie nach Ihren Anmeldeinformationen gefragt Ihre e-Mail-Adresse und das Kennwort ein, und klicken Sie dann auf **OK**. 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a>Schritt 2: Ausführen enthält des Skripts in den Bericht eDiscovery-Fälle zugeordnet

Nachdem Sie die Sicherheit verbunden sind &amp; Compliance Center mit remote-PowerShell, im nächsten Schritt erstellen und Ausführen des Skripts, das Informationen über die eDiscovery-Fälle in Ihrer Organisation erfasst wird. 
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise CaseHoldsReport.ps1. 
    
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

2. In der Windows PowerShell-Sitzung, die in Schritt 1 geöffnet, wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben. 
    
3. Führen Sie das Skript; Zum Beispiel:

    ```
    .\CaseHoldsReport.ps1
    ```

    Das Skript fordert einen Zielordner aus, um den Bericht zu speichern. 
    
4. Geben Sie den vollständigen Pfadnamen des Ordners, in den Bericht zu speichern, und drücken Sie die **EINGABETASTE**.
    
    > [!TIP]
    > Um den Bericht im selben Ordner zu speichern, die in das Skript gespeichert ist, geben Sie einen Punkt (".") Wenn Sie einen Zielordner aufgefordert werden. Um den Bericht in einem Unterordner im Ordner zu speichern, in das Skript gespeichert ist, geben Sie einfach den Namen des Unterordners. 
  
    Das Skript startet das Erfassen von Informationen zu den eDiscovery-Fällen in Ihrer Organisation. Greifen Sie auf nicht Berichtsdatei während der Ausführung des Skripts. Nachdem das Skript abgeschlossen ist, wird eine Meldung zur Bestätigung in der Windows PowerShell-Sitzung angezeigt. Nachdem diese Meldung angezeigt wird, können Sie den Bericht im Ordner zugreifen, die Sie in Schritt 4 angegeben. Der Dateiname für den Bericht ist `CaseHoldsReport<DateTimeStamp>.csv`.

    Auch, erstellt das Skript auch einen Bericht mit einer Liste von Anfragen, die nicht über einen Haltestatus verfügen. Der Dateiname für diesen Bericht ist `CaseswithNoHolds<DateTimeStamp>.csv`.
    
    Es folgt ein Beispiel der Ausführung des Skripts CaseHoldsReport.ps1. 
    
    ![Die Ausgabe nach der Ausführung des Skripts CaseHoldsReport.ps1](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a>Weitere Informationen

Die Groß-/Kleinschreibung enthält Bericht, der beim Ausführen des Skripts in diesem Artikel erstellt wird, die folgende Informationen zu jedem Haltebereich enthält. Wie bereits erklärt müssen Sie eine eDiscovery-Administrator sein, um die Informationen für alle Haltestatus in Ihrer Organisation zurückgegeben werden. Weitere Informationen zu Fall enthält, finden Sie unter [eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](ediscovery-cases.md).
  
  - Der Name des Haltestatus und den Namen der eDiscovery-Fall, die der Haltebereich zugeordnet ist.
    
  - Unabhängig davon, ob die eDiscovery-Fall aktiv oder geschlossen ist.
    
  - Unabhängig davon, ob die Sperre aktiviert oder deaktiviert ist.
    
  - Die Mitglieder von eDiscovery-Fall, die der Haltebereich zugeordnet ist. Groß-/Kleinschreibung Mitglieder können anzeigen und verwalten eine Anfrage, abhängig von den eDiscovery-Berechtigungen, die sie zugewiesen wurde, haben.
    
  - Datum und die Uhrzeit der Erstellung die Groß-/Kleinschreibung.
    
  - Wenn eine Anfrage geschlossen ist, wurde die Person, die geschlossen wurde, und die Uhrzeit und Datum geschlossen.
    
  - Die Exchange-Postfächern und SharePoint-Websites Speicherorte, die in der Warteschleife sind.
    
  - Wenn die Sperre abfragebasierte, ist die Abfragesyntax.
    
  - Die Zeit und Datum, an dem Haltebereich erstellt wurde und die Person, die sie erstellt haben.
    
  - Die Zeit und Datum, an dem Haltebereich zuletzt geändert wurde und die Person, die sie geändert.
