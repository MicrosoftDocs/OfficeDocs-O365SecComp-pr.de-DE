---
title: Virenschutz in SharePoint Online
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
description: Office 365 kann besser schützen Ihrer Umgebung von Malware Erkennen von Viren in Dateien, die Benutzer in SharePoint Online hoch. Dateien werden auf Viren überprüft, nachdem sie hochgeladen werden. Wenn eine Datei infiziert gefunden wird, wird eine Eigenschaft festgelegt, damit Benutzer nicht herunterladen oder synchronisieren Sie die Datei.
ms.openlocfilehash: 22e983d35283ff96e1469fdf913e25b8d1d1c485
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529707"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="987b2-105">Virenschutz in SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="987b2-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="987b2-p102">Office 365 kann besser schützen Ihrer Umgebung von Malware Erkennen von Viren in Dateien, die Benutzer in SharePoint Online hoch. Dateien werden auf Viren überprüft, nachdem sie hochgeladen werden. Wenn eine Datei infiziert gefunden wird, wird eine Eigenschaft festgelegt, damit Benutzer nicht herunterladen oder synchronisieren Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="987b2-p102">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online. Files are scanned for viruses after they are uploaded. If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="987b2-p103">Diese Antiviren-Funktionen in SharePoint Online bieten eine Möglichkeit, Viren enthalten. Sie werden nicht als eine zentrale Stelle Verteidigung gegen Malware für Ihre Umgebung vorgesehen. Wir empfehlen allen Benutzern zu bewerten und Implementieren von Modul-Schutz auf verschiedenen Ebenen anwenden bewährte Methoden zum Sichern Ihrer Enterprise-Infrastruktur. Weitere Informationen zu Strategien und best Practices finden Sie unter [bewährte Methoden für Office 365-Sicherheit](security-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="987b2-p103">These antivirus capabilities in SharePoint Online are a way to contain viruses. They aren't intended as a single point of defense against malware for your environment. We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure. For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="987b2-113">Was geschieht, wenn eine infizierte Datei in SharePoint Online hochgeladen wird?</span><span class="sxs-lookup"><span data-stu-id="987b2-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="987b2-p104">Office 365 wird eine allgemeine Virus Erkennung Engine verwendet. Das Modul wird innerhalb von SharePoint Online asynchron ausgeführt und scannt Dateien, nachdem sie hochgeladen haben. Wenn eine Datei einen Virus enthält gefunden wird, ist es markiert, damit es nicht erneut heruntergeladen werden kann. Im April 2018 entfernt wir den Grenzwert 25 MB für die überprüften Dateien.</span><span class="sxs-lookup"><span data-stu-id="987b2-p104">Office 365 uses a common virus detection engine. The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded. When a file is found to contain a virus, it's flagged so that it can't be downloaded again. In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="987b2-118">Hier geschieht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="987b2-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="987b2-119">Ein Benutzer lädt eine Datei in SharePoint Online hoch.</span><span class="sxs-lookup"><span data-stu-id="987b2-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="987b2-120">Die Virus Erkennung Engine überprüft die Datei.</span><span class="sxs-lookup"><span data-stu-id="987b2-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="987b2-121">Wenn ein Virus gefunden wird, wird die Virus Engine eine-Eigenschaft auf die Datei, die angibt, dass es infiziert ist.</span><span class="sxs-lookup"><span data-stu-id="987b2-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="987b2-122">Was geschieht, wenn ein Benutzer versucht, eine infizierte Datei mit dem Browser heruntergeladen?</span><span class="sxs-lookup"><span data-stu-id="987b2-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="987b2-123">Wenn eine Datei mit einem Virus infiziert ist, können nicht Benutzer die Datei mit dem Browser aus SharePoint Online herunterladen.</span><span class="sxs-lookup"><span data-stu-id="987b2-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="987b2-124">Hier geschieht Folgendes:</span><span class="sxs-lookup"><span data-stu-id="987b2-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="987b2-125">Ein Benutzer öffnet ein Webbrowser und versucht, eine infizierte Datei von SharePoint Online herunterladen.</span><span class="sxs-lookup"><span data-stu-id="987b2-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="987b2-126">Der Benutzer erhält eine Warnung, dass ein Virus erkannt wurde, und die Option zum Herunterladen der Datei erhält, und sie mit ihren eigenen Antivirussoftware bereinigen.</span><span class="sxs-lookup"><span data-stu-id="987b2-126">The user is given a warning that a virus has been detected, and is given the option to download the file and attempt to clean it using their own virus software.</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="987b2-127">Was geschieht, wenn der OneDrive Sync-Client versucht, eine infizierte Datei synchronisieren?</span><span class="sxs-lookup"><span data-stu-id="987b2-127">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="987b2-p105">Ob Benutzer Dateien mit der neuen OneDrive Sync-Client (OneDrive.exe) oder der vorherigen OneDrive for Business-Synchronisierungsclient (Groove.exe), synchronisieren, wenn eine Datei einen Virus enthält, wird nicht der Sync-Client es herunterladen. Der Sync-Client zeigt eine Benachrichtigung, dass die Datei kann nicht synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="987b2-p105">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it. The sync client will display a notification that the file can't be synced.</span></span>
  

