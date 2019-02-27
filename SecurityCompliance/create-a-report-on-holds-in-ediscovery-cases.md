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
description: Verwenden Sie das Skript in diesem Artikel, um einen Bericht zu generieren, der Informationen zu allen Haltebereichen enthält, die eDiscovery-Fällen im Office &amp; 365 Security Compliance Center zugeordnet sind.
ms.openlocfilehash: 95a960e8f76c672185e10d5b6be2a7ff2538a34b
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30296998"
---
# <a name="create-a-report-on-holds-in-ediscovery-cases-in-office-365"></a>Erstellen eines Berichts zu Haltebereichen in eDiscovery-Fällen in Office 365
  
Mit dem Skript in diesem Artikel können eDiscovery-Administratoren und eDiscovery-Manager einen Bericht generieren, der Informationen zu allen Haltebereichen enthält, die eDiscovery-Fällen im &amp; Office 365 Security Compliance Center zugeordnet sind. Der Bericht enthält Informationen wie den Namen des Falls, dem ein Haltebereich zugeordnet ist, die inhaltsspeicherorte, die in die Warteschleife gestellt werden, und ob die Aufbewahrung Abfrage basiert ist. Wenn es Fälle gibt, in denen keine haltebereiche vorhanden sind, erstellt das Skript einen zusätzlichen Bericht mit einer Liste von Fällen ohne Aufbewahrung.

Im Abschnitt [Weitere Informationen](#more-information) finden Sie eine ausführliche Beschreibung der im Bericht enthaltenen Informationen. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Wenn Sie einen Bericht zu allen eDiscovery-Fällen in Ihrer Organisation generieren möchten, müssen Sie ein eDiscovery-Administrator in Ihrer Organisation sein. Wenn Sie ein eDiscovery-Manager sind, enthält der Bericht nur Informationen zu den Fällen, auf die Sie zugreifen können. Weitere Informationen zu eDiscovery-Berechtigungen finden Sie unter [Zuweisen von eDiscovery-Berechtigungen im Office &amp; 365 Security Compliance Center](assign-ediscovery-permissions.md).
    
- Das Skript in diesem Artikel hat eine minimale Fehlerbehandlung. Der Hauptzweck besteht darin, Schnellbericht zu den Haltebereichen zu erstellen, die den eDiscovery-Fällen in Ihrer Organisation zugeordnet sind.
    
- Die in diesem Thema bereitgestellten Beispielskripts werden in den Microsoft-Standardsupportprogrammen oder -diensten nicht unterstützt. Die Beispielskripts werden wie besehen ohne Garantie jeglicher Art bereitgestellt. Microsoft schließt weiterhin konkludent, einschließlich, aber nicht beschränkt auf implizite Garantien der Handelsüblichkeit oder Eignung für einen bestimmten Zweck aus. Alle Risiken, die aus der Nutzung oder Ausführung der Beispielskripts und Dokumentation entstehen, liegen bei Ihnen. Microsoft, seine Autoren oder an der Erstellung, Produktion oder Bereitstellung der Skripts beteiligte Personen sind in keinem Fall haftbar für entstandene Schäden (darunter entgangene Gewinne, Geschäftsunterbrechungen, Verluste von Geschäftsinformationen oder sonstige finanzielle Verluste), die aus der Nutzung oder der Nutzungsunfähigkeit der Bespielskripts oder Dokumentation entstanden sind, selbst dann nicht, wenn Microsoft über eventuelle Folgen informiert wurde.
    
## <a name="step-1-connect-to-the-security-amp-compliance-center-using-remote-powershell"></a>Schritt 1: Herstellen einer Verbindung mit &amp; dem Security Compliance Center mithilfe von Remote-PowerShell

Der erste Schritt besteht darin, Windows PowerShell mit dem Security &amp; Compliance Center für Ihre Organisation zu verbinden.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `ConnectSCC.ps1`. 
    
      ```
      # Get login credentials 
      $UserCredential = Get-Credential 
      $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://ps.compliance.protection.outlook.com/powershell-liveid -Credential $UserCredential -Authentication Basic -AllowRedirection 
      Import-PSSession $Session -AllowClobber -DisableNameChecking 
      $Host.UI.RawUI.WindowTitle = $UserCredential.UserName + " (Office 365 Security &amp; Compliance Center)" 
    ```

2. Öffnen Sie auf dem lokalen Computer Windows PowerShell, und wechseln Sie zu dem Ordner, in dem Sie das Skript gespeichert haben. 
    
3. Führen Sie das Skript aus; Zum Beispiel:

    ```
    .\ConnectSCC.ps1
    ```
   
4. Wenn Sie zur Eingabe Ihrer Anmeldeinformationen aufgefordert werden, geben Sie Ihre e-Mail-Adresse und Ihr Kennwort ein, und klicken Sie auf **OK**. 
  
## <a name="step-2-run-the-script-to-report-on-holds-associated-with-ediscovery-cases"></a>Schritt 2: Ausführen des Skripts zum Melden von Haltebereichen im Zusammenhang mit eDiscovery-Fällen

Nachdem Sie mit der Remote-PowerShell &amp; eine Verbindung mit dem Security Compliance Center hergestellt haben, besteht der nächste Schritt im erstellen und Ausführen des Skripts, das Informationen zu den eDiscovery-Fällen in Ihrer Organisation sammelt. 
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: CaseHoldsReport. ps1. 
    
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

2. Wechseln Sie in der Windows PowerShell-Sitzung, die in Schritt 1 geöffnet wurde, zu dem Ordner, in dem Sie das Skript gespeichert haben. 
    
3. Führen Sie das Skript aus; Zum Beispiel:

    ```
    .\CaseHoldsReport.ps1
    ```

    Das Skript fordert einen Zielordner an, in dem der Bericht gespeichert werden soll. 
    
4. Geben Sie den vollständigen Pfadnamen des Ordners ein, in dem der Bericht gespeichert werden soll, und drücken Sie dann die **Eingabe**Taste.
    
    > [!TIP]
    > Zum Speichern des Berichts in demselben Ordner, in dem sich das Skript befindet, geben Sie einen Punkt (".") ein, wenn Sie für einen Zielordner aufgefordert werden. Zum Speichern des Berichts in einem Unterordner in dem Ordner, in dem sich das Skript befindet, geben Sie einfach den Namen des Unterordners ein. 
  
    Das Skript fängt an, Informationen zu allen eDiscovery-Fällen in Ihrer Organisation zu sammeln. Greifen Sie während des Skripts nicht auf die Berichtsdatei zu. Nach Abschluss des Skripts wird in der Windows PowerShell-Sitzung eine Bestätigungsmeldung angezeigt. Nachdem diese Meldung angezeigt wurde, können Sie auf den Bericht in dem Ordner zugreifen, den Sie in Schritt 4 angegeben haben. Der Dateiname für den Bericht lautet `CaseHoldsReport<DateTimeStamp>.csv`.

    Außerdem erstellt das Skript einen Bericht mit einer Liste von Fällen, die keine haltebereiche enthalten. Der Dateiname für diesen Bericht lautet `CaseswithNoHolds<DateTimeStamp>.csv`.
    
    Nachfolgend finden Sie ein Beispiel für die Verwendung des CaseHoldsReport. ps1-Skripts. 
    
    ![Die Ausgabe nach dem Ausführen des CaseHoldsReport. ps1-Skripts](media/7d312ed5-505e-4ec5-8f06-3571e3524a1a.png)
  
## <a name="more-information"></a>Weitere Informationen

Der Fall enthält Bericht, der erstellt wird, wenn Sie das Skript in diesem Artikel ausführen enthält die folgenden Informationen zu den einzelnen Haltebereichen. Wie bereits erläutert, müssen Sie ein eDiscovery-Administrator sein, um Informationen für alle haltebereiche in Ihrer Organisation zurückzugeben. Weitere Informationen zu Fall Haltebereichen finden Sie unter [eDiscovery Cases im Office 365 &amp; Security Compliance Center](ediscovery-cases.md).
  
  - Der Name des haltebereichs und der Name des eDiscovery-Falls, dem der Haltebereich zugeordnet ist.
    
  - Gibt an, ob der eDiscovery-Fall aktiv oder geschlossen ist.
    
  - Gibt an, ob der Haltestatus aktiviert oder deaktiviert ist.
    
  - Die Mitglieder des eDiscovery-Falls, dem der Haltebereich zugeordnet ist. Fall Mitglieder können eine Groß-/Kleinschreibung abhängig von den Ihnen zugewiesenen eDiscovery-Berechtigungen anzeigen oder verwalten.
    
  - Die Uhrzeit und das Datum, an dem die Anfrage erstellt wurde.
    
  - Wenn eine Groß-/Kleinschreibung geschlossen wird, die Person, die Sie geschlossen hat, und die Uhrzeit und das Datum, zu dem Sie geschlossen wurde.
    
  - Die Speicherorte von Exchange-Postfächern und SharePoint-Websites.
    
  - Wenn der Haltebereich Abfrage basiert ist, wird die Abfragesyntax.
    
  - Die Uhrzeit und das Datum, an dem die Aufbewahrungszeit erstellt wurde, und die Person, die Sie erstellt hat.
    
  - Uhrzeit und Datum der letzten Änderung und die Person, die Sie geändert hat.
