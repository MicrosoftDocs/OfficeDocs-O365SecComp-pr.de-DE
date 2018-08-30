---
title: Office 365 ATP für SharePoint, OneDrive und Microsoft-Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 6/18/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
description: Erweitern Sie Office 365 erweiterte Schutz, um Dateien in SharePoint Online, OneDrive für Unternehmen und Microsoft-Teams, um sicherer Zusammenarbeit für Ihre Organisation zu aktivieren.
ms.openlocfilehash: ea1c77273be70ce27f60bfaeae3544d605553a32
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529874"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Office 365 ATP für SharePoint, OneDrive und Microsoft-Teams

Personen, für die regelmäßig Dateien freigeben und Zusammenarbeit per SharePoint, OneDrive und Microsoft-Teams. Mit [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP) kann Ihre Organisation auf sichere Weise zusammenarbeiten. ATP hilft beim Erkennen und blockieren Dateien, die in Dokumentbibliotheken und Teamwebsites wie böswilligen identifiziert werden. Lesen Sie diesen Artikel, wenn Sie eine Übersicht über ATP für SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams erhalten möchten, und schalten Sie die nächsten Schritte aus. 
  
> [!TIP]
> Um die in diesem Artikel beschriebenen Aufgaben durchführen zu können, müssen Sie ein globaler Office 365-Administrator oder ein Sicherheitsadministrator sein. Finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="how-it-works"></a>Funktionsweise

Wenn Sie eine Datei in SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams, wie böswillige identifiziert wurden, ATP integriert direkt mit den Dateispeicher, diese Datei zu sperren. Die folgende Abbildung zeigt ein Beispiel für eine solche Datei in einer Bibliothek erkannt.
  
[![Screenshot der Dateien in OneDrive für Unternehmen mit einem als böswilligen entdeckt](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Zwar weiterhin Gesperrte Dateitypen in der Dokumentbibliothek und Web, Mobil oder desktop Applications aufgeführt ist kann nicht die blockierte Datei geöffnet, kopiert, verschoben oder shared. Personen können, jedoch eine blockierte Datei löschen. Hier ist ein Beispiel für das auf dem mobilen Gerät eines Benutzers aussieht:
  
[![Screenshot des Löschens einer blockierten Datei aus OneDrive for Business aus der mobilen OneDrive-app](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Je nach Konfiguration der Office 365 Personen möglicherweise oder möglicherweise nicht die Möglichkeit, eine blockierte Datei herunterladen. Sieht aus wie eine blockierte Datei herunterladen auf mobilen Gerät eines Benutzers aussieht:
  
[![Screenshot des Herunterladens eine gesperrte Dateitypen in OneDrive für Unternehmen](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Finden Sie weitere Informationen finden Sie unter [Office 365 ATP für SharePoint, OneDrive, und Microsoft-Teams aktivieren](turn-on-atp-for-spo-odb-and-teams.md).
  
### <a name="keep-the-following-points-in-mind"></a>Beachten Sie die folgenden Punkte

- ATP überprüft nicht jede einzelne Datei in SharePoint Online, OneDrive for Business oder Microsoft-Teams. Dies ist entwurfsbedingt. Dateien werden asynchron durch einen Prozess überprüft, die Dateifreigabe und Gast Aktivitätsereignisse zusammen mit smart Heuristik und Bedrohung Signale verwendet, um bösartige Dateien zu identifizieren.
    
- Dateien, die als böswillige in SharePoint Online gekennzeichnet sind, werden OneDrive for Business oder Microsoft-Teams, in [Berichten für Office 365 erweiterte Threat Protection](view-reports-for-atp.md) und Threat Explorer (Teil von [Office 365 Bedrohungsanalyse](office-365-ti.md)) angezeigt.
    
- ATP ist Teil Ihrer Organisation insgesamt Threat Protection-Strategie Antispam- und Anti-Malware Protection, als auch sichere Links und sichere Anlagen. Weitere Informationen finden Sie unter [Schutz vor Bedrohungen in Office 365](protect-against-threats.md).
    
- SharePoint Online-Administrator kann bestimmen, ob Benutzer auf Dateien herunterladen, die als böswilligen entdeckt werden. Dies erfolgt durch Ausführen des Set-SPOTenant-PowerShell-Cmdlets, die mit einem DisallowInfectedFileDownload-Parameter (finden Sie unter [Aktivieren der Office 365 ATP für SharePoint, OneDrive, und Microsoft-Teams](turn-on-atp-for-spo-odb-and-teams.md)).
    
## <a name="new-quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a>(Neu!) Quarantäne in ATP für SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams

 ** Ab Ende Mai 2018, [Quarantäne](quarantine-email-messages.md) -Funktionen in das Wertpapier &amp; Compliance Center sind erweiternden, ATP für SharePoint Online, OneDrive für Unternehmen und die Microsoft-Teams. **
  
Wenn Sie eine Datei in SharePoint Online, OneDrive for Business oder Microsoft-Teams, böswilligen, zusätzlich zur ATP blockieren die Datei geöffnet oder gemeinsam genutzt werden angezeigt, diese Datei in eine Liste der in Quarantäne verschobenen Elemente enthalten ist. (In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Bedrohung Management** \> **Überprüfung** \> **Quarantäne** und Filter für Inhalt.) 
  
Wenn Sie Teil von Office 365-Security-Team Ihrer Organisation und die erforderlichen haben [in die Office 365-Sicherheit zugewiesenen Berechtigungen &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md), Sie herunterladen, freigeben, Berichten und Löschen von Dateien, die durch ATP wie böswilligen entdeckt werden aus der Quarantäne.
  
- **Freigeben und melden** einer Datei entfernt den ATP-Block auf die Datei in den jeweiligen Team Website oder Dokumentbibliothek für SharePoint, OneDrive oder Microsoft-Teams. Benutzer können klicken Sie dann auf Öffnen, freigeben, und Laden Sie die Datei. Und wenn die Option **Bericht an Microsoft senden** ausgewählt ist, wird die Datei als falsch positiv an Microsoft gemeldet. 
    
- **Löschen einer Datei** wird die Datei aus der Quarantäne entfernt. die Datei wird jedoch weiterhin werden blockiert, geöffnet oder freigegeben. Die Datei muss ebenfalls in der jeweiligen Bibliothek oder einer Team-Website (SharePoint Online, OneDrive for Business oder Microsoft-Teams) gelöscht. 
    
- **Herunterladen einer Datei** können Sie herunterladen und Analysieren der Datei für alle falsch positive Ergebnisse. 
    
## <a name="next-steps"></a>Nächste Schritte

- [Aktivieren Sie Office 365 ATP für SharePoint, OneDrive und Microsoft-Teams](turn-on-atp-for-spo-odb-and-teams.md)
    
- [Anzeigen von Informationen über schädliche Dateien in SharePoint, OneDrive oder Microsoft-Teams erkannt](malicious-files-detected-in-spo-odb-or-teams.md)
    
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Anzeigen der Berichte für Office 365 erweiterte Threat Protection](view-reports-for-atp.md)
  
[Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
  

