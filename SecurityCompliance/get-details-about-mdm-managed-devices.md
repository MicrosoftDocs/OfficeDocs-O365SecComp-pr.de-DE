---
title: Abrufen von Informationen zu verwalteten durch Mobile Device Management (MDM) für Office 365-Geräten
ms.author: brendonb
author: brendonb
manager: laurawi
ms.date: 6/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MBS150
- MET150
ms.assetid: 5602963c-a1f2-4c21-afb9-f66cd7dca1f0
description: Dieser Artikel beschreibt, wie Windows PowerShell verwenden, um Details zu den Geräten in Ihrer Organisation abzurufen, die Sie für die Verwaltung mobiler Geräte für Office 365 einrichten.
ms.openlocfilehash: 90ee59c5afed1cd260e13134299a7cb4f17dc5bc
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972317"
---
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a>Abrufen von Informationen zu verwalteten durch Mobile Device Management (MDM) für Office 365-Geräten

Dieser Artikel beschreibt, wie Windows PowerShell verwenden, um Details zu den Geräten in Ihrer Organisation abzurufen, die Sie für die Verwaltung mobiler Geräte für Office 365 einrichten. 
  
## <a name="what-device-details-can-i-get"></a>Welche Gerätedetails finde ich?

Es folgt eine Aufschlüsselung.
  
|**Detail**|**Wonach Sie suchen in PowerShell**|
|:-----|:-----|
|Gerät ist [in MDM für Office 365 registriert](enroll-your-mobile-device.md) <br/> |Der Wert des Parameters *IsManaged* ist:  <br/> **True** = Gerät registriert ist.  <br/> **False** = Gerät ist nicht registriert.  <br/> |
|Gerät ist kompatibel mit Ihrer [Sicherheitsrichtlinien für Geräte](https://go.microsoft.com/fwlink/?linkid=615144) <br/> |Der Wert des Parameters *IsCompliant* ist:  <br/> **True** = Gerät mit Richtlinien kompatibel ist.  <br/> **False** = Gerät ist nicht kompatibel mit Richtlinien.  <br/> |
   
![Fluss AAD Shell Param Werte für gibt an, ob Geräte registriert sind und kompatibles anzeigen](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> Die Befehle und Skripts in diesem Artikel werden ebenfalls Details über alle Geräte zurückgegeben, die von [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune)verwaltet werden. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

Es gibt einige Dinge, denen Sie benötigen bis zum Festlegen der Befehle und Skripts beschrieben in diesem Artikel ausführen.
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a>Schritt 1: Herunterladen Sie und installieren Sie der Azure Active Directory-Modul für Windows PowerShell

Weitere Informationen zu diesen Schritten finden Sie unter [Connect to Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).
  
1. Wechseln Sie zum [Microsoft Online Services-Anmeldeassistent für IT-Experten RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) , und klicken Sie auf **Download** für Microsoft Online Services-Anmeldeassistenten. 
    
2. Installieren Sie die Microsoft Azure Active Directory-Modul für Windows PowerShell mit der folgenden Schritte aus:
    
    1. Öffnen Sie eine PowerShell-Eingabeaufforderung auf Administratorebene.
        
    2. Führen Sie die `Install-Module MSOnline` Befehl.
        
    3. Wenn Sie aufgefordert, den NuGet-Anbieter installieren, geben Sie `Y` , und drücken Sie die EINGABETASTE.
        
    4. Wenn Sie aufgefordert werden, installieren Sie das Modul aus PSGallery, geben Sie `Y` , und drücken Sie die EINGABETASTE.
        
    5. Schließen Sie nach der Installation das PowerShell-Befehlsfenster.
    
### <a name="step-2-connect-to-your-office-365-subscription"></a>Schritt 2: Verbinden Sie mit Office 365-Abonnements

1. Führen Sie in der Windows Azure Active Directory-Modul für Windows PowerShell den folgenden Befehl ein.<br/>  
  `$UserCredential = Get-Credential`

2. Klicken Sie im Dialogfeld **Windows PowerShell anmelden** Geben Sie den Benutzernamen und das Kennwort für Ihr Office 365 globaler Administrator-Konto ein, und klicken Sie dann auf **OK**.
    
3. Führen Sie den folgenden Befehl aus.<br/>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a>Schritt 3: Stellen Sie sicher, dass Sie PowerShell-Skripts ausführen können.

> [!NOTE]
> Sie können diesen Schritt überspringen, wenn Sie bereits zum Ausführen des PowerShell-Skripts eingerichtet sind. 
  
Um das **Get-MsolUserDeviceComplianceStatus.ps1** -Skript ausführen, müssen Sie die Ausführung von PowerShell-Skripts aktivieren. 
  
1. Aus dem Windows-Desktop auf **Start**, und geben Sie dann auf Windows PowerShell. Klicken Sie mit der rechten Maustaste auf **Windows PowerShell**, und klicken Sie dann auf **als Administrator ausführen**.
    
2. Führen Sie den folgenden Befehl aus.<br/>
  `Set-ExecutionPolicy RemoteSigned`

3. Geben Sie bei entsprechender Aufforderung `Y` und drücken Sie dann die EINGABETASTE. 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a>Führen Sie das Cmdlet Get-MsolDevice zum Anzeigen von Details für alle Geräte in Ihrer Organisation

1. Öffnen Sie das Microsoft Azure Active Directory-Modul für Windows PowerShell.
    
2. Führen Sie den folgenden Befehl aus.<br/>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

Weitere Beispiele finden Sie unter [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).
  
## <a name="run-a-script-to-get-device-details"></a>Führen Sie ein Skript zum Abrufen von Gerätedetails

### <a name="first-save-the-script-to-your-computer"></a>Speichern Sie zuerst das Skript auf Ihrem computer

1. Kopieren Sie und fügen Sie den folgenden Text in Notepad ein.<br/> 
  ```
  param (
      [PSObject[]]$users = @(),
      [Switch]$export,
      [String]$exportFileName = "UserDeviceComplianceStatus_" + (Get-Date -Format "yyMMdd_HHMMss") + ".csv",
      [String]$exportPath = [Environment]::GetFolderPath("Desktop")
   )
  [System.Collections.IDictionary]$script:schema = @{
      
      DeviceId = ''
      DeviceOSType = ''
      DeviceOSVersion = ''
      DeviceTrustLevel = ''
      DisplayName = ''
      IsCompliant = ''
      IsManaged = ''
      ApproximateLastLogonTimestamp = ''
      DeviceObjectId = ''    
      RegisteredOwnerUpn = ''
      RegisteredOwnerObjectId = ''
      RegisteredOwnerDisplayName = ''
  }
  function createResultObject
  {
      [PSObject]$resultObject = New-Object -TypeName PSObject -Property $script:schema
      return $resultObject
  }
  If ($users.Count -eq 0)
  {
      $users = Get-MsolUser
  }
  [PSObject[]]$result = foreach ($u in $users)
  {
      
      [PSObject]$devices = get-msoldevice -RegisteredOwnerUpn $u.UserPrincipalName
      foreach ($d in $devices)
      {
          [PSObject]$deviceResult = createResultObject
          $deviceResult.DeviceId = $d.DeviceId 
          $deviceResult.DeviceOSType = $d.DeviceOSType 
          $deviceResult.DeviceOSVersion = $d.DeviceOSVersion 
          $deviceResult.DeviceTrustLevel = $d.DeviceTrustLevel
          $deviceResult.DisplayName = $d.DisplayName
          $deviceResult.IsCompliant = $d.GraphDeviceObject.IsCompliant
          $deviceResult.IsManaged = $d.GraphDeviceObject.IsManaged
          $deviceResult.DeviceObjectId = $d.ObjectId
          $deviceResult.RegisteredOwnerUpn = $u.UserPrincipalName
          $deviceResult.RegisteredOwnerObjectId = $u.ObjectId
          $deviceResult.RegisteredOwnerDisplayName = $u.DisplayName
          $deviceResult.ApproximateLastLogonTimestamp = $d.ApproximateLastLogonTimestamp
          $deviceResult
      }
  }
  If ($export)
  {
      $result | Export-Csv -path ($exportPath + "\" + $exportFileName) -NoTypeInformation
  }
  Else
  {
      $result
  }
  
  ```

2. Speichern Sie sie als eine Windows PowerShell-Skriptdatei mithilfe der Dateierweiterung **. ps1**. <br/>Beispiel:<br/> `Get-MsolUserDeviceComplianceStatus.ps1`.
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a>Führen Sie das Skript zum Abrufen von Geräteinformationen für ein einzelnes Benutzerkonto

1. Öffnen Sie das Microsoft Azure Active Directory-Modul für Windows PowerShell.
    
2. Navigieren Sie zu dem Ordner, in dem Sie das Skript gespeichert haben. Wenn Sie es in der C:\PS-Scripts gespeichert, würden Sie beispielsweise den folgenden Befehl ausführen.<br/>
    `cd C:\PS-Scripts`

3. Führen Sie den folgenden Befehl zum Identifizieren des Benutzers, dass Sie Gerätedetails für abrufen möchten. Dieses Beispiel ruft die Details für bar@example.com.<br/>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. Führen Sie den folgenden Befehl aus, um das Skript zu initiieren.<br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

Die Informationen werden zum Windows-Desktop als CSV-Datei exportiert. Zusätzliche Parameter können Sie den Dateinamen und Pfad der CSV angeben.
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a>Führen Sie das Skript zum Abrufen von Geräteinformationen für eine Gruppe von Benutzern

1. Öffnen Sie das Microsoft Azure Active Directory-Modul für Windows PowerShell.
    
2. Navigieren Sie zu dem Ordner, in dem Sie das Skript gespeichert haben. Wenn Sie es in der C:\PS-Scripts gespeichert, würden Sie beispielsweise den folgenden Befehl ausführen.<br/>
  `cd C:\PS-Scripts`

3. Führen Sie den folgenden Befehl zum Identifizieren der Gruppe, dass Sie Gerätedetails für abrufen möchten. Dieses Beispiel ruft die Details für Benutzer in der Gruppe FinanceStaff.<br/>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. Führen Sie den folgenden Befehl aus, um das Skript zu initiieren.<br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

Die Informationen werden zum Windows-Desktop als CSV-Datei exportiert. Zusätzliche Parameter können Sie den Dateinamen und Pfad der CSV angeben.
  
## <a name="more-info"></a>Weitere Informationen

[Übersicht über MDM für Office 365](overview-of-mdm.md)
  
[Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721)
  

