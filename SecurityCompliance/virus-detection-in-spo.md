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
# <a name="virus-detection-in-sharepoint-online"></a>Virenerkennung in SharePoint Online

Office 365 kann Ihre Umgebung vor Schadsoftware schützen, indem Viren in Dateien ermittelt werden, die Benutzer in SharePoint Online hochladen. Dateien werden nach dem Hochladen auf Viren überprüft. Wenn eine Datei als infiziert festgestellt wird, wird eine Eigenschaft festgelegt, sodass Benutzer die Datei weder herunterladen noch synchronisieren können.
  
> [!IMPORTANT]
> Diese Antivirus-Funktionen in SharePoint Online sind eine Möglichkeit, Viren zu enthalten. Sie sind nicht als zentraler Schutz gegen Schadsoftware für Ihre Umgebung vorgesehen. Wir ermutigen alle Kunden, den Schutz vor Schadsoftware auf verschiedenen Ebenen zu bewerten und zu implementieren und bewährte Methoden zum Sichern Ihrer Unternehmensinfrastruktur anzuwenden. Weitere Informationen zu Strategien und bewährten Methoden finden Sie unter [bewährte Methoden für die Sicherheit von Office 365](security-best-practices.md). 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a>Was geschieht, wenn eine infizierte Datei in SharePoint Online hochgeladen wird?

Office 365 verwendet ein allgemeines Viruserkennungsmodul. Das Modul wird asynchron in SharePoint Online ausgeführt und scannt Dateien nach dem Hochladen. Wenn eine Datei einen Virus enthält, wird Sie so gekennzeichnet, dass Sie nicht erneut heruntergeladen werden kann. Im April 2018 haben wir den Grenzwert von 25 MB für gescannte Dateien entfernt.
  
Folgendes geschieht:
  
1. Ein Benutzer lädt eine Datei in SharePoint Online hoch.
    
2. Das Viruserkennungsmodul überprüft die Datei.
    
3. Wenn ein Virus gefunden wird, wird vom Viren Modul eine Eigenschaft für die Datei festgelegt, die darauf hinweist, dass Sie infiziert ist.
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a>Was geschieht, wenn ein Benutzer versucht, eine infizierte Datei mithilfe des Browsers herunterzuladen?

Wenn eine Datei mit einem Virus infiziert ist, können Benutzer die Datei nicht über den Browser aus SharePoint Online herunterladen.
  
Folgendes geschieht:
  
1. Ein Benutzer öffnet einen Webbrowser und versucht, eine infizierte Datei aus SharePoint Online herunterzuladen.
    
2. Der Benutzer erhält eine Warnung, dass ein Virus erkannt wurde. Der Benutzer erhält die Option, die Datei herunterzuladen und zu versuchen, Sie mit ihrer eigenen Viren Software zu säubern.

> [!NOTE]
> Sie können das Cmdlet Set-SPOTenant mit dem Parameter **DisallowInfectedFileDownload** verwenden, um Benutzern das Herunterladen einer erkannten Datei auch im Fenster mit der Virenschutz Warnung zu gestatten. Siehe [DisallowInfectedFileDownload] (https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant).
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a>Was geschieht, wenn der OneDrive-synchronisierungsclient versucht, eine infizierte Datei zu synchronisieren?

Ob Benutzer Dateien mit dem neuen OneDrive-synchronisierungsclient (OneDrive. exe) oder dem vorherigen OneDrive for Business-synchronisierungsclient (Groove. exe) synchronisieren, wenn eine Datei einen Virus enthält, wird Sie vom synchronisierungsclient nicht heruntergeladen. Der synchronisierungsclient zeigt eine Benachrichtigung an, dass die Datei nicht synchronisiert werden kann.
  

