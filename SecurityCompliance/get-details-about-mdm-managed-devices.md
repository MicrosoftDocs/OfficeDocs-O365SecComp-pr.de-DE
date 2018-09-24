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
# <a name="get-details-about-devices-managed-by-mobile-device-management-mdm-for-office-365"></a><span data-ttu-id="157fc-103">Abrufen von Informationen zu verwalteten durch Mobile Device Management (MDM) für Office 365-Geräten</span><span class="sxs-lookup"><span data-stu-id="157fc-103">Get details about devices managed by Mobile Device Management (MDM) for Office 365</span></span>

<span data-ttu-id="157fc-104">Dieser Artikel beschreibt, wie Windows PowerShell verwenden, um Details zu den Geräten in Ihrer Organisation abzurufen, die Sie für die Verwaltung mobiler Geräte für Office 365 einrichten.</span><span class="sxs-lookup"><span data-stu-id="157fc-104">This article shows you how to use Windows PowerShell to get details about the devices in your organization that you set up for Mobile Device Management for Office 365.</span></span> 
  
## <a name="what-device-details-can-i-get"></a><span data-ttu-id="157fc-105">Welche Gerätedetails finde ich?</span><span class="sxs-lookup"><span data-stu-id="157fc-105">What device details can I get?</span></span>

<span data-ttu-id="157fc-106">Es folgt eine Aufschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="157fc-106">Here's a breakdown.</span></span>
  
|<span data-ttu-id="157fc-107">**Detail**</span><span class="sxs-lookup"><span data-stu-id="157fc-107">**Detail**</span></span>|<span data-ttu-id="157fc-108">**Wonach Sie suchen in PowerShell**</span><span class="sxs-lookup"><span data-stu-id="157fc-108">**What to look for in PowerShell**</span></span>|
|:-----|:-----|
|<span data-ttu-id="157fc-109">Gerät ist [in MDM für Office 365 registriert](enroll-your-mobile-device.md)</span><span class="sxs-lookup"><span data-stu-id="157fc-109">Device is [enrolled in MDM for Office 365](enroll-your-mobile-device.md)</span></span> <br/> |<span data-ttu-id="157fc-110">Der Wert des Parameters *IsManaged* ist:</span><span class="sxs-lookup"><span data-stu-id="157fc-110">The value of the  *isManaged*  parameter is:</span></span>  <br/> <span data-ttu-id="157fc-111">**True** = Gerät registriert ist.</span><span class="sxs-lookup"><span data-stu-id="157fc-111">**True** = device is enrolled.</span></span>  <br/> <span data-ttu-id="157fc-112">**False** = Gerät ist nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="157fc-112">**False** = device is not enrolled.</span></span>  <br/> |
|<span data-ttu-id="157fc-113">Gerät ist kompatibel mit Ihrer [Sicherheitsrichtlinien für Geräte](https://go.microsoft.com/fwlink/?linkid=615144)</span><span class="sxs-lookup"><span data-stu-id="157fc-113">Device is compliant with your [device security policies](https://go.microsoft.com/fwlink/?linkid=615144)</span></span> <br/> |<span data-ttu-id="157fc-114">Der Wert des Parameters *IsCompliant* ist:</span><span class="sxs-lookup"><span data-stu-id="157fc-114">The value of the  *isCompliant*  parameter is:</span></span>  <br/> <span data-ttu-id="157fc-115">**True** = Gerät mit Richtlinien kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="157fc-115">**True** = device is compliant with policies.</span></span>  <br/> <span data-ttu-id="157fc-116">**False** = Gerät ist nicht kompatibel mit Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="157fc-116">**False** = device is not compliant with policies.</span></span>  <br/> |
   
![Fluss AAD Shell Param Werte für gibt an, ob Geräte registriert sind und kompatibles anzeigen](media/647b70f4-f886-41ef-8bff-04773a1da278.png)
  
> [!NOTE]
> <span data-ttu-id="157fc-118">Die Befehle und Skripts in diesem Artikel werden ebenfalls Details über alle Geräte zurückgegeben, die von [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune)verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="157fc-118">The commands and scripts in this article will also return details about any devices that are managed by [Microsoft Intune](https://www.microsoft.com/en-us/cloud-platform/microsoft-intune).</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="157fc-119">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="157fc-119">Before you begin</span></span>

<span data-ttu-id="157fc-120">Es gibt einige Dinge, denen Sie benötigen bis zum Festlegen der Befehle und Skripts beschrieben in diesem Artikel ausführen.</span><span class="sxs-lookup"><span data-stu-id="157fc-120">There are a few things you'll need to set up to run the commands and scripts described in this article.</span></span>
  
### <a name="step-1-download-and-install-the-azure-active-directory-module-for-windows-powershell"></a><span data-ttu-id="157fc-121">Schritt 1: Herunterladen Sie und installieren Sie der Azure Active Directory-Modul für Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="157fc-121">Step 1: Download and install the Azure Active Directory Module for Windows PowerShell</span></span>

<span data-ttu-id="157fc-122">Weitere Informationen zu diesen Schritten finden Sie unter [Connect to Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).</span><span class="sxs-lookup"><span data-stu-id="157fc-122">For more info on these steps, see [Connect to Office 365 PowerShell](https://docs.microsoft.com/Office365/enterprise/powershell/connect-to-office-365-powershell).</span></span>
  
1. <span data-ttu-id="157fc-123">Wechseln Sie zum [Microsoft Online Services-Anmeldeassistent für IT-Experten RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) , und klicken Sie auf **Download** für Microsoft Online Services-Anmeldeassistenten.</span><span class="sxs-lookup"><span data-stu-id="157fc-123">Go to [Microsoft Online Services Sign-In Assistant for IT Professionals RTWl](https://www.microsoft.com/en-us/download/details.aspx?id=41950) and click **Download** for Microsoft Online Services Sign-in Assistant.</span></span> 
    
2. <span data-ttu-id="157fc-124">Installieren Sie die Microsoft Azure Active Directory-Modul für Windows PowerShell mit der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="157fc-124">Install the Microsoft Azure Active Directory Module for Windows PowerShell with these steps:</span></span>
    
    1. <span data-ttu-id="157fc-125">Öffnen Sie eine PowerShell-Eingabeaufforderung auf Administratorebene.</span><span class="sxs-lookup"><span data-stu-id="157fc-125">Open an administrator-level PowerShell command prompt.</span></span>
        
    2. <span data-ttu-id="157fc-126">Führen Sie die `Install-Module MSOnline` Befehl.</span><span class="sxs-lookup"><span data-stu-id="157fc-126">Run the `Install-Module MSOnline` command.</span></span>
        
    3. <span data-ttu-id="157fc-127">Wenn Sie aufgefordert, den NuGet-Anbieter installieren, geben Sie `Y` , und drücken Sie die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="157fc-127">If prompted to install the NuGet provider, type `Y` and press ENTER.</span></span>
        
    4. <span data-ttu-id="157fc-128">Wenn Sie aufgefordert werden, installieren Sie das Modul aus PSGallery, geben Sie `Y` , und drücken Sie die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="157fc-128">If prompted to install the module from PSGallery, type `Y` and press ENTER.</span></span>
        
    5. <span data-ttu-id="157fc-129">Schließen Sie nach der Installation das PowerShell-Befehlsfenster.</span><span class="sxs-lookup"><span data-stu-id="157fc-129">After installation, close the PowerShell command window.</span></span>
    
### <a name="step-2-connect-to-your-office-365-subscription"></a><span data-ttu-id="157fc-130">Schritt 2: Verbinden Sie mit Office 365-Abonnements</span><span class="sxs-lookup"><span data-stu-id="157fc-130">Step 2: Connect to your Office 365 subscription</span></span>

1. <span data-ttu-id="157fc-131">Führen Sie in der Windows Azure Active Directory-Modul für Windows PowerShell den folgenden Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="157fc-131">In the Windows Azure Active Directory Module for Windows PowerShell, run the following command.</span></span><br/>  
  `$UserCredential = Get-Credential`

2. <span data-ttu-id="157fc-132">Klicken Sie im Dialogfeld **Windows PowerShell anmelden** Geben Sie den Benutzernamen und das Kennwort für Ihr Office 365 globaler Administrator-Konto ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="157fc-132">In the **Windows PowerShell Credential Request** dialog box, type the user name and password for your Office 365 global admin account, and then click **OK**.</span></span>
    
3. <span data-ttu-id="157fc-133">Führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="157fc-133">Run the following command.</span></span><br/>
    `
  Connect-MsolService -Credential $UserCredential
  `

### <a name="step-3-make-sure-youre-able-to-run-powershell-scripts"></a><span data-ttu-id="157fc-134">Schritt 3: Stellen Sie sicher, dass Sie PowerShell-Skripts ausführen können.</span><span class="sxs-lookup"><span data-stu-id="157fc-134">Step 3: Make sure you're able to run PowerShell scripts</span></span>

> [!NOTE]
> <span data-ttu-id="157fc-135">Sie können diesen Schritt überspringen, wenn Sie bereits zum Ausführen des PowerShell-Skripts eingerichtet sind.</span><span class="sxs-lookup"><span data-stu-id="157fc-135">You can skip this step if you're already set up to run PowerShell scripts.</span></span> 
  
<span data-ttu-id="157fc-136">Um das **Get-MsolUserDeviceComplianceStatus.ps1** -Skript ausführen, müssen Sie die Ausführung von PowerShell-Skripts aktivieren.</span><span class="sxs-lookup"><span data-stu-id="157fc-136">To run the **Get-MsolUserDeviceComplianceStatus.ps1** script, you need to enable the running of PowerShell scripts.</span></span> 
  
1. <span data-ttu-id="157fc-p101">Aus dem Windows-Desktop auf **Start**, und geben Sie dann auf Windows PowerShell. Klicken Sie mit der rechten Maustaste auf **Windows PowerShell**, und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="157fc-p101">From your Windows Desktop, click **Start**, and then type Windows PowerShell. Right click **Windows PowerShell**, and then click **Run as administrator**.</span></span>
    
2. <span data-ttu-id="157fc-139">Führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="157fc-139">Run the following command.</span></span><br/>
  `Set-ExecutionPolicy RemoteSigned`

3. <span data-ttu-id="157fc-140">Geben Sie bei entsprechender Aufforderung `Y` und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="157fc-140">When prompted, type `Y` and then press Enter.</span></span> 
    
## <a name="run-the-get-msoldevice-cmdlet-to-display-details-for-all-devices-in-your-organization"></a><span data-ttu-id="157fc-141">Führen Sie das Cmdlet Get-MsolDevice zum Anzeigen von Details für alle Geräte in Ihrer Organisation</span><span class="sxs-lookup"><span data-stu-id="157fc-141">Run the Get-MsolDevice cmdlet to display details for all devices in your organization</span></span>

1. <span data-ttu-id="157fc-142">Öffnen Sie das Microsoft Azure Active Directory-Modul für Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="157fc-142">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="157fc-143">Führen Sie den folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="157fc-143">Run the following command.</span></span><br/>
  ```
  Get-MsolDevice -All -ReturnRegisteredOwners | Where-Object {$_.RegisteredOwners.Count -gt 0}
  ```

<span data-ttu-id="157fc-144">Weitere Beispiele finden Sie unter [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).</span><span class="sxs-lookup"><span data-stu-id="157fc-144">For more examples, see [Get-MsolDevice](https://go.microsoft.com/fwlink/?linkid=841721).</span></span>
  
## <a name="run-a-script-to-get-device-details"></a><span data-ttu-id="157fc-145">Führen Sie ein Skript zum Abrufen von Gerätedetails</span><span class="sxs-lookup"><span data-stu-id="157fc-145">Run a script to get device details</span></span>

### <a name="first-save-the-script-to-your-computer"></a><span data-ttu-id="157fc-146">Speichern Sie zuerst das Skript auf Ihrem computer</span><span class="sxs-lookup"><span data-stu-id="157fc-146">First, save the script to your computer</span></span>

1. <span data-ttu-id="157fc-147">Kopieren Sie und fügen Sie den folgenden Text in Notepad ein.</span><span class="sxs-lookup"><span data-stu-id="157fc-147">Copy and paste the following text into Notepad.</span></span><br/> 
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

2. <span data-ttu-id="157fc-148">Speichern Sie sie als eine Windows PowerShell-Skriptdatei mithilfe der Dateierweiterung **. ps1**.</span><span class="sxs-lookup"><span data-stu-id="157fc-148">Save it as a Windows PowerShell script file by using the file extension **.ps1**.</span></span> <br/><span data-ttu-id="157fc-149">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="157fc-149">Example:</span></span><br/> <span data-ttu-id="157fc-150">`Get-MsolUserDeviceComplianceStatus.ps1`.</span><span class="sxs-lookup"><span data-stu-id="157fc-150"></span></span>
    
### <a name="run-the-script-to-get-device-information-for-a-single-user-account"></a><span data-ttu-id="157fc-151">Führen Sie das Skript zum Abrufen von Geräteinformationen für ein einzelnes Benutzerkonto</span><span class="sxs-lookup"><span data-stu-id="157fc-151">Run the script to get device information for a single user account</span></span>

1. <span data-ttu-id="157fc-152">Öffnen Sie das Microsoft Azure Active Directory-Modul für Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="157fc-152">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="157fc-p102">Navigieren Sie zu dem Ordner, in dem Sie das Skript gespeichert haben. Wenn Sie es in der C:\PS-Scripts gespeichert, würden Sie beispielsweise den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="157fc-p102">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span><br/>
    `cd C:\PS-Scripts`

3. <span data-ttu-id="157fc-p103">Führen Sie den folgenden Befehl zum Identifizieren des Benutzers, dass Sie Gerätedetails für abrufen möchten. Dieses Beispiel ruft die Details für bar@example.com.</span><span class="sxs-lookup"><span data-stu-id="157fc-p103">Run the following command to identify the user you want to get device details for. This example gets details for bar@example.com.</span></span><br/>
  ```
  $u = Get-MsolUser -UserPrincipalName bar@example.com
  ```

4. <span data-ttu-id="157fc-157">Führen Sie den folgenden Befehl aus, um das Skript zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="157fc-157">Run the following command to initiate the script.</span></span><br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="157fc-p104">Die Informationen werden zum Windows-Desktop als CSV-Datei exportiert. Zusätzliche Parameter können Sie den Dateinamen und Pfad der CSV angeben.</span><span class="sxs-lookup"><span data-stu-id="157fc-p104">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
### <a name="run-the-script-to-get-device-information-for-a-group-of-users"></a><span data-ttu-id="157fc-160">Führen Sie das Skript zum Abrufen von Geräteinformationen für eine Gruppe von Benutzern</span><span class="sxs-lookup"><span data-stu-id="157fc-160">Run the script to get device information for a group of users</span></span>

1. <span data-ttu-id="157fc-161">Öffnen Sie das Microsoft Azure Active Directory-Modul für Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="157fc-161">Open the Microsoft Azure Active Directory Module for Windows PowerShell.</span></span>
    
2. <span data-ttu-id="157fc-p105">Navigieren Sie zu dem Ordner, in dem Sie das Skript gespeichert haben. Wenn Sie es in der C:\PS-Scripts gespeichert, würden Sie beispielsweise den folgenden Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="157fc-p105">Navigate to the folder where you saved the script. For example, if you saved it to C:\PS-Scripts, you'd run the following command.</span></span><br/>
  `cd C:\PS-Scripts`

3. <span data-ttu-id="157fc-p106">Führen Sie den folgenden Befehl zum Identifizieren der Gruppe, dass Sie Gerätedetails für abrufen möchten. Dieses Beispiel ruft die Details für Benutzer in der Gruppe FinanceStaff.</span><span class="sxs-lookup"><span data-stu-id="157fc-p106">Run the following command to identify the group you want to get device details for. This example gets details for users in the FinanceStaff group.</span></span><br/>
  ```
  $u = Get-MsolGroupMember -SearchString "FinanceStaff" | % { Get-MsolUser -ObjectId $_.ObjectId }
  ```

4. <span data-ttu-id="157fc-166">Führen Sie den folgenden Befehl aus, um das Skript zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="157fc-166">Run the following command to initiate the script.</span></span><br/>
  ```
  .\Get-MsolUserDeviceComplianceStatus.ps1 -User $u -Export
  ```

<span data-ttu-id="157fc-p107">Die Informationen werden zum Windows-Desktop als CSV-Datei exportiert. Zusätzliche Parameter können Sie den Dateinamen und Pfad der CSV angeben.</span><span class="sxs-lookup"><span data-stu-id="157fc-p107">The information is exported to your Windows Desktop as a CSV file. You can use additional parameters to specify the file name and path of the CSV.</span></span>
  
## <a name="more-info"></a><span data-ttu-id="157fc-169">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="157fc-169">More info</span></span>

[<span data-ttu-id="157fc-170">Übersicht über MDM für Office 365</span><span class="sxs-lookup"><span data-stu-id="157fc-170">Overview of MDM for Office 365</span></span>](overview-of-mdm.md)
  
[<span data-ttu-id="157fc-171">Get-MsolDevice</span><span class="sxs-lookup"><span data-stu-id="157fc-171">Get-MsolDevice</span></span>](https://go.microsoft.com/fwlink/?linkid=841721)
  

