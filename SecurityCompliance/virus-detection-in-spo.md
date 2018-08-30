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
# <a name="virus-detection-in-sharepoint-online"></a>Virenschutz in SharePoint Online

Office 365 kann besser schützen Ihrer Umgebung von Malware Erkennen von Viren in Dateien, die Benutzer in SharePoint Online hoch. Dateien werden auf Viren überprüft, nachdem sie hochgeladen werden. Wenn eine Datei infiziert gefunden wird, wird eine Eigenschaft festgelegt, damit Benutzer nicht herunterladen oder synchronisieren Sie die Datei.
  
> [!IMPORTANT]
> Diese Antiviren-Funktionen in SharePoint Online bieten eine Möglichkeit, Viren enthalten. Sie werden nicht als eine zentrale Stelle Verteidigung gegen Malware für Ihre Umgebung vorgesehen. Wir empfehlen allen Benutzern zu bewerten und Implementieren von Modul-Schutz auf verschiedenen Ebenen anwenden bewährte Methoden zum Sichern Ihrer Enterprise-Infrastruktur. Weitere Informationen zu Strategien und best Practices finden Sie unter [bewährte Methoden für Office 365-Sicherheit](security-best-practices.md). 
  
## <a name="what-happens-when-an-infected-file-is-uploaded-to-sharepoint-online"></a>Was geschieht, wenn eine infizierte Datei in SharePoint Online hochgeladen wird?

Office 365 wird eine allgemeine Virus Erkennung Engine verwendet. Das Modul wird innerhalb von SharePoint Online asynchron ausgeführt und scannt Dateien, nachdem sie hochgeladen haben. Wenn eine Datei einen Virus enthält gefunden wird, ist es markiert, damit es nicht erneut heruntergeladen werden kann. Im April 2018 entfernt wir den Grenzwert 25 MB für die überprüften Dateien.
  
Hier geschieht Folgendes:
  
1. Ein Benutzer lädt eine Datei in SharePoint Online hoch.
    
2. Die Virus Erkennung Engine überprüft die Datei.
    
3. Wenn ein Virus gefunden wird, wird die Virus Engine eine-Eigenschaft auf die Datei, die angibt, dass es infiziert ist.
    
## <a name="what-happens-when-a-user-tries-to-download-an-infected-file-by-using-the-browser"></a>Was geschieht, wenn ein Benutzer versucht, eine infizierte Datei mit dem Browser heruntergeladen?

Wenn eine Datei mit einem Virus infiziert ist, können nicht Benutzer die Datei mit dem Browser aus SharePoint Online herunterladen.
  
Hier geschieht Folgendes:
  
1. Ein Benutzer öffnet ein Webbrowser und versucht, eine infizierte Datei von SharePoint Online herunterladen.
    
2. Der Benutzer erhält eine Warnung, dass ein Virus erkannt wurde, und die Option zum Herunterladen der Datei erhält, und sie mit ihren eigenen Antivirussoftware bereinigen.
    
## <a name="what-happens-when-the-onedrive-sync-client-tries-to-sync-an-infected-file"></a>Was geschieht, wenn der OneDrive Sync-Client versucht, eine infizierte Datei synchronisieren?

Ob Benutzer Dateien mit der neuen OneDrive Sync-Client (OneDrive.exe) oder der vorherigen OneDrive for Business-Synchronisierungsclient (Groove.exe), synchronisieren, wenn eine Datei einen Virus enthält, wird nicht der Sync-Client es herunterladen. Der Sync-Client zeigt eine Benachrichtigung, dass die Datei kann nicht synchronisiert werden.
  

