---
title: Anzeigen von Informationen zu schädlichen Dateien, die in SharePoint, OneDrive oder Microsoft Teams erkannt wurden
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
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
ms.openlocfilehash: f5304f78ddec884748dd7d1090e2a7895044d045
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259833"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>Anzeigen von Informationen zu schädlichen Dateien, die in SharePoint, OneDrive oder Microsoft Teams erkannt wurden

[Office 365 ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md) schützt Ihre Organisation vor schädlichen Dateien in Dokumentbibliotheken und Teamwebsites. Wenn eine bösartige Datei erkannt wird, wird diese Datei blockiert, sodass niemand Sie öffnen, kopieren, verschieben oder freigeben kann, bis weitere Aktionen des Sicherheitsteams der Organisation durchgeführt werden. In diesem Artikel erfahren Sie, wie Sie Informationen zu erkannten Dateien und zu ergreifenden Aktionen anzeigen können. 

Zum Ausführen der in diesem Artikel beschriebenen Aufgaben benötigen Sie die erforderlichen [Berechtigungen für das Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="view-reports-with-information-about-detected-files"></a>Anzeigen von Berichten mit Informationen zu erkannten Dateien

Zum Anzeigen des Status und detaillierter Informationen zu Dateien, die von Office 365 ATP erkannt wurden, können Sie den Statusbericht über den BedrohungsSchutz verwenden.
  
1. wählen sie im [Office 365 &amp; Security Compliance Center](https://protection.office.com)die option **berichte** \> - **Dashboard** \> **Threat Protection Status**aus.
    
2. Klicken Sie in der oberen rechten Ecke des Berichts auf **Details anzeigen**.
    
3. Dient zum Anzeigen der Liste der Dateien, die im Bericht erkannt wurden.
    
4. Wählen Sie ein Element in der Liste aus, um detaillierte Informationen anzuzeigen, einschließlich der ausgeführten Aktionen, des Datei namens, des Dateipfads und vieles mehr.
    
5. Klicken Sie auf die Registerkarte **Erweiterte Analyse** , um Informationen wie beobachtete Verhaltens-und Analysedetails anzuzeigen. 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>Anzeigen und Ausführen von Aktionen für Dateien in Quarantäne

1. wählen sie im Office 365 &amp; Security Compliance Center die option **Threat management** \> **Review** \> **quarantine**aus.
    
2. Ändern Sie in der oberen linken Ecke den Filter von **e-Mail** in **Inhalt**.
    
3. Wählen Sie ein Element in der Liste aus, um detaillierte Informationen, einschließlich der Datei-URL, anzuzeigen.
    
4. Wählen Sie eine verfügbare Aktion aus.
    
  - Wählen **Sie &amp; Freigabe Bericht** aus, um die Datei aufzuheben. 
    
    Wählen Sie **Bericht an Microsoft senden** aus, um die Datei als falsch positives Ergebnis an Microsoft zu melden. 
    
  - Wählen Sie **Datei herunterladen** , um die Datei weiter zu untersuchen. 
    
  - Wählen Sie **Löschen** aus, um die Datei aus der Liste der isolierten Elemente zu entfernen. Wenn Sie diese Option auswählen, müssen Sie die Datei auch aus der entsprechenden Bibliothek in SharePoint Online, OneDrive for Business oder Microsoft Teams löschen. Mit dieser Option wird das Öffnen oder Freigeben einer Datei nicht aufgehoben. 
    
5. Klicken Sie auf **Schließen** , um die Details für ein ausgewähltes Element zu schließen. 
  
  

