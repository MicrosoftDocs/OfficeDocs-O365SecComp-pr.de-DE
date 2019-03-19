---
title: Beispielskript für das Anwenden von EOP-Einstellungen für mehrere Mandanten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/17/2014
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: e87e84e1-7be0-44bf-a414-d91d60ed8817
description: Mit dem folgenden Beispielskript können Microsoft Exchange Online Protection (EOP)-Administratoren, die mehrere Mandanten (Unternehmen) verwalten, Konfigurationseinstellungen für ihre Mandanten mithilfe von Windows PowerShell anwenden.
ms.openlocfilehash: 787847721f46fc4b3caeec037e89306ef450141a
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670410"
---
# <a name="sample-script-for-applying-eop-settings-to-multiple-tenants"></a>Beispielskript für das Anwenden von EOP-Einstellungen für mehrere Mandanten

Mit dem folgenden Beispielskript können Microsoft Exchange Online Protection (EOP)-Administratoren, die mehrere Mandanten (Unternehmen) verwalten, Konfigurationseinstellungen für ihre Mandanten mithilfe von Windows PowerShell anwenden.
  
### <a name="to-run-a-script-or-cmdlet-on-multiple-tenants"></a>So führen Sie ein Skript oder Cmdlet auf mehreren Mandanten aus:

1. Erstellen Sie mithilfe einer Anwendung wie Excel eine CSV-Datei (zum Beispiel c:\scripts\inputfile.csv):
    
1. Geben Sie in der CSV-Datei zwei Spaltennamen an: UserName und Cmdlet.
    
2. Geben Sie für jede Zeile in der CSV-Datei den Administratornamen des Mandanten in die Spalte "UserName" und das für diesen Mandanten auszuführende Cmdlet in die Spalte "Cmdlet" ein. Verwenden Sie beispielsweise admin@contoso.com und Get-AcceptedDomain.
    
2. Kopieren Sie das Skript [RunCmdletOnMultipleTenants.ps1](sample-script-for-applying-eop-settings-to-multiple-tenants.md#RunCmdletOnMultipleTenants.ps1) in einen Editor wie Notepad, und speichern Sie die Datei dann an einem Speicherort (wie c:\scripts), an dem Sie PS1-Dateien leicht finden können. 
    
3. Führen Sie das Skript mit der folgenden Syntax aus:
    ```Powershell
     & "<file path>\RunCmdletOnMultipleTenants.ps1" "<file path>\inputfile.csv"
    ```
    
    Im Folgenden sehen Sie ein Beispiel. 
    
    ```Powershell
    & "c:\scripts\RunCmdletOnMultipleTenanats.ps1" "c:\scripts\inputfile.csv"
    ```

4. Jeder Mandant wird angemeldet, und das Cmdlet wird ausgeführt.
    
## <a name="runcmdletonmultipletenantsps1"></a>Skript runcmdletonmultipletenants. ps1
<a name="RunCmdletOnMultipleTenants.ps1"> </a>

```Powershell
# This script runs Windows PowerShell cmdlets on multiple tenants.
# Usage: RunCmdletOnMultipleTenants.ps1 inputfile.csv
#  
# .csv input file sample: 
# UserName,Cmdlet
# admin@contoso.com,Get-AcceptedDomain | ft Name
# URI for connecting to remote Windows PowerShell
$URI = "https://ps.protection.outlook.com/powershell-liveid/"
# Get the .csv file name as an argument to this script.
$FilePath = $args[0]
# Import the UserName and Cmdlet values from the .csv file.
$CompanyList = Import-CSV $FilePath
# Loop through each entry from the .csv file.
ForEach ($Company in $CompanyList) {
# Get the current entry's UserName.
$UserName = $Company.UserName
# Get the current entry's Cmdlet.
$Cmdlet = $Company.Cmdlet
# Create a PowerShell credential object by using the current entry's UserName. Prompt for the password.
$UserCredential = Get-Credential -username $UserName
# Log on to a new Windows PowerShell session.
$Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri $URI -Credential $UserCredential -Authentication Basic -AllowRedirection
Import-PSSession $Session
# Here's where the script to be run on the tenant goes.
# In this example, the cmdlet in the .csv file runs.
Invoke-Expression $Cmdlet
# End the current PowerShell session.
remove-pssession -session $Session
}

```


