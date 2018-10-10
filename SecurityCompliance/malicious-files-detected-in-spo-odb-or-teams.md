---
title: Anzeigen von Informationen über schädliche Dateien in SharePoint, OneDrive oder Microsoft-Teams erkannt
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5ed8abf1-c0e9-4e5b-a5b7-2059cea50b61
description: Erfahren Sie, wo Sie zum Anzeigen von Informationen zu schädliche Dateien in SharePoint, OneDrive oder Teams erkannt und wie Sie auf diese Dateien ergreifen.
ms.openlocfilehash: 370e5e3d4d7fd5f35caa8ef993f6245d15ee9999
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454272"
---
# <a name="view-information-about-malicious-files-detected-in-sharepoint-onedrive-or-microsoft-teams"></a>Anzeigen von Informationen über schädliche Dateien in SharePoint, OneDrive oder Microsoft-Teams erkannt

[Office 365 ATP für SharePoint, OneDrive, und Microsoft-Teams](atp-for-spo-odb-and-teams.md) schützt Ihre Organisation vor schädliche Dateien in Dokumentbibliotheken und Teamwebsites. Wenn eine solche Datei erkannt wird, wird diese Datei blockiert, damit niemand öffnen, kopieren, verschieben oder freigeben, bis der Organisation Security Team Weitere Aktionen ausgeführt werden. Lesen Sie diesen Artikel, um Hier erfahren, wie Sie Informationen zu erkannten Dateien anzeigen und welche Aktionen vorgenommen werden sollen. 

Um die in diesem Artikel beschriebenen Aufgaben durchführen zu können, benötigen Sie die erforderlichen [in die Office 365-Sicherheit zugewiesenen Berechtigungen &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="view-reports-with-information-about-detected-files"></a>Anzeigen von Berichten mit Informationen zu erkannten Dateien

Zum Anzeigen von Status und detaillierte Informationen zu Dateien, die von Office 365 ATP erkannt wurden, können Sie den Threat Protection Statusbericht verwenden.
  
1. In der Office 365-Sicherheit &amp; Compliance Center, wählen Sie **Berichte** \> **Dashboard** \> **Bedrohung Schutzstatus**.
    
2. Wählen Sie in der oberen rechten Ecke des Berichts **Ansicht Detailtabelle**aus.
    
3. Anzeigen der Liste der Dateien, die im Bericht erkannt wurden.
    
4. Wählen Sie ein Element in der Liste, um ausführliche Informationen, einschließlich der Aktionen, den Dateinamen, den Dateipfad und anzeigen.
    
5. Wählen Sie die Registerkarte **Erweiterte Analyse** Informationen wie beobachteten Verhalten und Analysen Details anzeigen. 
  
## <a name="view-and-take-action-on-files-in-quarantine"></a>Dient zum zeigen Sie an und führen Sie einer Aktion auf Dateien in Quarantäne aus

1. In der Office 365-Sicherheit &amp; Compliance Center, wählen Sie **Threat Management** \> **Überprüfung** \> **Quarantine**.
    
2. Ändern Sie in der oberen linken Ecke des Filters von **E-Mail** auf **Inhalt**.
    
3. Wählen Sie ein Element in der Liste aus, um ausführliche Informationen, einschließlich der URL der Datei anzuzeigen.
    
4. Auswählen einer verfügbaren Aktion an.
    
  - Wählen Sie **Release &amp; Bericht** für die Datei aufheben. 
    
    Wählen Sie auf die Datei als falsch positiv an Microsoft gemeldet **Bericht an Microsoft senden** . 
    
  - Wählen Sie die **Datei herunterladen** , untersuchen Sie die Datei noch. 
    
  - Wählen Sie auf **Löschen** , um die Datei aus der Liste der in Quarantäne verschobenen Elemente zu entfernen. Wenn Sie diese Option auswählen, müssen Sie auch die Datei aus der entsprechenden Dokumentbibliothek in SharePoint Online, OneDrive for Business oder Microsoft-Teams löschen. Diese Option ist eine Datei verhindern oder freigegebenen geöffnete nicht Blockierung aufheben. 
    
5. Wählen Sie auf **Schließen** , um die Details für ein ausgewähltes Element zu schließen. 
  
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Anzeigen der Berichte für Office 365 erweiterte Threat Protection](view-reports-for-atp.md)
  
[Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

[Verwalten von in Quarantäne verschobenen Nachrichten und Dateien als Administrator in Office 365](manage-quarantined-messages-and-files.md)
  

