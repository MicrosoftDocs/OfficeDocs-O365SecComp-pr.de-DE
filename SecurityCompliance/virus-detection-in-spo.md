---
title: Virenerkennung in SharePoint Online
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 01/14/2019
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: e3c6df61-8513-499d-ad8e-8a91770bff63
ms.collection:
- M365-security-compliance
description: Office 365 kann Ihre Umgebung vor Schadsoftware schützen, indem Viren in Dateien ermittelt werden, die Benutzer in SharePoint Online hochladen. Dateien werden nach dem Hochladen auf Viren überprüft. Wenn eine Datei als infiziert festgestellt wird, wird eine Eigenschaft festgelegt, sodass Benutzer die Datei weder herunterladen noch synchronisieren können.
ms.openlocfilehash: d4f18c84935d9c6e1d3f135bbda6c40737956ae7
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32266823"
---
# <a name="virus-detection-in-sharepoint-online"></a><span data-ttu-id="32dd1-105">Virenerkennung in SharePoint Online</span><span class="sxs-lookup"><span data-stu-id="32dd1-105">Virus detection in SharePoint Online</span></span>

<span data-ttu-id="32dd1-106">Office 365 kann Ihre Umgebung vor Schadsoftware schützen, indem Viren in Dateien ermittelt werden, die Benutzer in SharePoint Online hochladen.</span><span class="sxs-lookup"><span data-stu-id="32dd1-106">Office 365 can help protect your environment from malware by detecting viruses in files that users upload to SharePoint Online.</span></span> <span data-ttu-id="32dd1-107">Dateien werden nach dem Hochladen auf Viren überprüft.</span><span class="sxs-lookup"><span data-stu-id="32dd1-107">Files are scanned for viruses after they are uploaded.</span></span> <span data-ttu-id="32dd1-108">Wenn eine Datei als infiziert festgestellt wird, wird eine Eigenschaft festgelegt, sodass Benutzer die Datei weder herunterladen noch synchronisieren können.</span><span class="sxs-lookup"><span data-stu-id="32dd1-108">If a file is found to be infected, a property is set so that users can't download or sync the file.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="32dd1-109">Diese Antivirus-Funktionen in SharePoint Online sind eine Möglichkeit, Viren zu enthalten.</span><span class="sxs-lookup"><span data-stu-id="32dd1-109">These antivirus capabilities in SharePoint Online are a way to contain viruses.</span></span> <span data-ttu-id="32dd1-110">Sie sind nicht als zentraler Schutz gegen Schadsoftware für Ihre Umgebung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="32dd1-110">They aren't intended as a single point of defense against malware for your environment.</span></span> <span data-ttu-id="32dd1-111">Wir ermutigen alle Kunden, den Schutz vor Schadsoftware auf verschiedenen Ebenen zu bewerten und zu implementieren und bewährte Methoden zum Sichern Ihrer Unternehmensinfrastruktur anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="32dd1-111">We encourage all customers to assess and implement antimalware protection at various layers and apply best practices for securing your enterprise infrastructure.</span></span> <span data-ttu-id="32dd1-112">Weitere Informationen zu Strategien und bewährten Methoden finden Sie unter [bewährte Methoden für die Sicherheit von Office 365](security-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="32dd1-112">For more information about strategies and best practices, see [Security best practices for Office 365](security-best-practices.md).</span></span> 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a><span data-ttu-id="32dd1-113">Was geschieht, wenn eine infizierte Datei in SharePoint Online hochgeladen wird?</span><span class="sxs-lookup"><span data-stu-id="32dd1-113">What happens when an infected file is uploaded to SharePoint Online?</span></span>

<span data-ttu-id="32dd1-114">Office 365 verwendet ein allgemeines Viruserkennungsmodul.</span><span class="sxs-lookup"><span data-stu-id="32dd1-114">Office 365 uses a common virus detection engine.</span></span> <span data-ttu-id="32dd1-115">Das Modul wird asynchron in SharePoint Online ausgeführt und scannt Dateien nach dem Hochladen.</span><span class="sxs-lookup"><span data-stu-id="32dd1-115">The engine runs asynchronously within SharePoint Online, and scans files after they're uploaded.</span></span> <span data-ttu-id="32dd1-116">Wenn eine Datei einen Virus enthält, wird Sie so gekennzeichnet, dass Sie nicht erneut heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="32dd1-116">When a file is found to contain a virus, it's flagged so that it can't be downloaded again.</span></span> <span data-ttu-id="32dd1-117">Im April 2018 haben wir den Grenzwert von 25 MB für gescannte Dateien entfernt.</span><span class="sxs-lookup"><span data-stu-id="32dd1-117">In April 2018, we removed the 25 MB limit for scanned files.</span></span>
  
<span data-ttu-id="32dd1-118">Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="32dd1-118">Here's what happens:</span></span>
  
1. <span data-ttu-id="32dd1-119">Ein Benutzer lädt eine Datei in SharePoint Online hoch.</span><span class="sxs-lookup"><span data-stu-id="32dd1-119">A user uploads a file to SharePoint Online.</span></span>
    
2. <span data-ttu-id="32dd1-120">Das Viruserkennungsmodul überprüft die Datei.</span><span class="sxs-lookup"><span data-stu-id="32dd1-120">The virus detection engine scans the file.</span></span>
    
3. <span data-ttu-id="32dd1-121">Wenn ein Virus gefunden wird, wird vom Viren Modul eine Eigenschaft für die Datei festgelegt, die darauf hinweist, dass Sie infiziert ist.</span><span class="sxs-lookup"><span data-stu-id="32dd1-121">If a virus is found, the virus engine sets a property on the file indicating that it is infected.</span></span>
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a><span data-ttu-id="32dd1-122">Was geschieht, wenn ein Benutzer versucht, eine infizierte Datei mithilfe des Browsers herunterzuladen?</span><span class="sxs-lookup"><span data-stu-id="32dd1-122">What happens when a user tries to download an infected file by using the browser?</span></span>

<span data-ttu-id="32dd1-123">Wenn eine Datei mit einem Virus infiziert ist, können Benutzer die Datei nicht über den Browser aus SharePoint Online herunterladen.</span><span class="sxs-lookup"><span data-stu-id="32dd1-123">If a file is infected with a virus, users can't download the file from SharePoint Online by using the browser.</span></span>
  
<span data-ttu-id="32dd1-124">Folgendes geschieht:</span><span class="sxs-lookup"><span data-stu-id="32dd1-124">Here's what happens:</span></span>
  
1. <span data-ttu-id="32dd1-125">Ein Benutzer öffnet einen Webbrowser und versucht, eine infizierte Datei aus SharePoint Online herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="32dd1-125">A user opens a web browser and tries to download an infected file from SharePoint Online.</span></span>
    
2. <span data-ttu-id="32dd1-126">Der Benutzer erhält eine Warnung, dass ein Virus erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="32dd1-126">The user is given a warning that a virus has been detected.</span></span> <span data-ttu-id="32dd1-127">Der Benutzer erhält die Option, die Datei herunterzuladen und zu versuchen, Sie mit ihrer eigenen Viren Software zu säubern.</span><span class="sxs-lookup"><span data-stu-id="32dd1-127">The user is given the option to download the file and attempt to clean it using their own virus software.</span></span>

> [!NOTE]
> <span data-ttu-id="32dd1-128">Sie können das Cmdlet Set-SPOTenant mit dem Parameter **DisallowInfectedFileDownload** verwenden, um Benutzern das Herunterladen einer erkannten Datei auch im Fenster mit der Virenschutz Warnung zu gestatten.</span><span class="sxs-lookup"><span data-stu-id="32dd1-128">You can use the Set-SPOTenant cmdlet with the **DisallowInfectedFileDownload** parameter to not allow users to download a detected file, even in the anti-virus warning window.</span></span> <span data-ttu-id="32dd1-129">Siehe [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span><span class="sxs-lookup"><span data-stu-id="32dd1-129">See [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).</span></span>
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a><span data-ttu-id="32dd1-130">Was geschieht, wenn der OneDrive-synchronisierungsclient versucht, eine infizierte Datei zu synchronisieren?</span><span class="sxs-lookup"><span data-stu-id="32dd1-130">What happens when the OneDrive sync client tries to sync an infected file?</span></span>

<span data-ttu-id="32dd1-131">Ob Benutzer Dateien mit dem neuen OneDrive-synchronisierungsclient (OneDrive. exe) oder dem vorherigen OneDrive for Business-synchronisierungsclient (Groove. exe) synchronisieren, wenn eine Datei einen Virus enthält, wird Sie vom synchronisierungsclient nicht heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="32dd1-131">Whether users sync files with the new OneDrive sync client (OneDrive.exe) or the previous OneDrive for Business sync client (Groove.exe), if a file contains a virus, the sync client won't download it.</span></span> <span data-ttu-id="32dd1-132">Der synchronisierungsclient zeigt eine Benachrichtigung an, dass die Datei nicht synchronisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="32dd1-132">The sync client will display a notification that the file can't be synced.</span></span>
  

