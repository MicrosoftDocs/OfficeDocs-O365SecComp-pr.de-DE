---
title: Anzeigen von Informationen zu schädlichen Dateien, die in SharePoint, OneDrive oder Microsoft Teams erkannt wurden
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wo Sie Informationen zu böswilligen Dateien anzeigen können, die in SharePoint, OneDrive oder Teams erkannt werden, und wie Sie Maßnahmen für diese Dateien ergreifen.
ms.openlocfilehash: 070640d9aa1d28cc1a49a9d8b88e5bf5780d3622
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077581"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>Anzeigen von Informationen zu schädlichen Dateien, die in SharePoint, OneDrive oder Microsoft Teams erkannt wurden

[Office 365 ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md) schützt Ihre Organisation vor schädlichen Dateien in Dokumentbibliotheken und Teamwebsites. Wenn eine bösartige Datei erkannt wird, wird diese Datei blockiert, sodass niemand Sie öffnen, kopieren, verschieben oder freigeben kann, bis weitere Aktionen des Sicherheitsteams der Organisation durchgeführt werden. In diesem Artikel erfahren Sie, wie Sie Informationen zu erkannten Dateien und zu ergreifenden Aktionen anzeigen können. 

Zum Ausführen der in diesem Artikel beschriebenen Aufgaben benötigen Sie die erforderlichen [Berechtigungen für das Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="view-reports-with-information-about-detected-files"></a>Anzeigen von Berichten mit Informationen zu erkannten Dateien

Zum Anzeigen des Status und detaillierter Informationen zu Dateien, die von Office 365 ATP erkannt wurden, können Sie den Statusbericht über den Bedrohungsschutz verwenden.
  
1. Wählen Sie im [Office 365 &amp; Security Compliance Center](https://protection.office.com)die Option **Berichte** \> - **Dashboard** \> **Threat Protection Status**aus.
    
2. Klicken Sie in der oberen rechten Ecke des Berichts auf **Details anzeigen**.
    
3. Dient zum Anzeigen der Liste der Dateien, die im Bericht erkannt wurden.
    
4. Wählen Sie ein Element in der Liste aus, um detaillierte Informationen anzuzeigen, einschließlich der ausgeführten Aktionen, des Datei namens, des Dateipfads und vieles mehr.
    
5. Klicken Sie auf die Registerkarte **Erweiterte Analyse** , um Informationen wie beobachtete Verhaltens-und Analysedetails anzuzeigen. 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>Anzeigen und Ausführen von Aktionen für Dateien in Quarantäne

1. Wählen Sie im Office 365 &amp; Security Compliance Center die Option **Threat Management** \> **Review** \> **Quarantine**aus.
    
2. Ändern Sie in der oberen linken Ecke den Filter von **e-Mail** in **Inhalt**.
    
3. Wählen Sie ein Element in der Liste aus, um detaillierte Informationen, einschließlich der Datei-URL, anzuzeigen.
    
4. Wählen Sie eine verfügbare Aktion aus.
    
  - Wählen **Sie &amp; Freigabe Bericht** aus, um die Datei aufzuheben. 
    
    Wählen Sie **Bericht an Microsoft senden** aus, um die Datei als falsch positives Ergebnis an Microsoft zu melden. 
    
  - Wählen Sie **Datei herunterladen** , um die Datei weiter zu untersuchen. 
    
  - Wählen Sie **Löschen** aus, um die Datei aus der Liste der isolierten Elemente zu entfernen. Wenn Sie diese Option auswählen, müssen Sie die Datei auch aus der entsprechenden Bibliothek in SharePoint Online, OneDrive for Business oder Microsoft Teams löschen. Mit dieser Option wird das Öffnen oder Freigeben einer Datei nicht aufgehoben. 
    
5. Klicken Sie auf **Schließen** , um die Details für ein ausgewähltes Element zu schließen. 
  
  

