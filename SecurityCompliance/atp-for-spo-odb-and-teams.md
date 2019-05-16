---
title: Office 365 ATP für SharePoint, OneDrive und Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
audience: Admin
ms.date: 03/19/2019
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 26261670-db33-4c53-b125-af0662c34607
ms.collection:
- M365-security-compliance
description: Erweitern Sie Office 365 Advanced Threat Protection auf Dateien in SharePoint Online, OneDrive for Business und Microsoft Teams, um eine sicherere Zusammenarbeit für Ihr Unternehmen zu ermöglichen.
ms.openlocfilehash: 9a1c4d3f7eca335b1668f8fc0947387cc9d496f3
ms.sourcegitcommit: 0d5a863f48914eeaaf29f7d2a2022618de186247
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "34077611"
---
# <a name="office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Office 365 ATP für SharePoint, OneDrive und Microsoft Teams

## <a name="overview-of-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Übersicht über Office 365 ATP für SharePoint, OneDrive und Microsoft Teams

Personen tauschen regelmäßig Dateien aus und arbeiten mit SharePoint, OneDrive und Microsoft Teams zusammen. Mit [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) kann Ihre Organisation sicher zusammenarbeiten. ATP hilft bei der Erkennung und Blockierung von Dateien, die in Teamwebsites und Dokumentbibliotheken als bösartig identifiziert werden.  
  
## <a name="how-it-works"></a>Funktionsweise

Wenn eine Datei in SharePoint Online, OneDrive for Business und Microsoft Teams als bösartig identifiziert wurde, wird ATP direkt in die Dateispeicher integriert, um diese Datei zu sperren. Die folgende Abbildung zeigt ein Beispiel für eine bösartige Datei, die in einer Bibliothek erkannt wurde.
  
[![Dateien in OneDrive for Business mit einer als bösartig erkannt](media/2bba71cc-7ad1-4799-8b9d-d56f923db3a7.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Obwohl die blockierte Datei weiterhin in der Dokumentbibliothek und den Web-, Mobil-oder Desktopanwendungen aufgeführt wird, kann die blockierte Datei nicht geöffnet, kopiert, verschoben oder freigegeben werden. Die Benutzer können jedoch eine blockierte Datei löschen. Hier sehen Sie ein Beispiel dafür, wie das auf dem mobilen Gerät eines Benutzers aussieht:
  
[![Löschen einer blockierten Datei aus OneDrive for Business aus der mobilen OneDrive-App](media/cb1c1705-fd0a-45b8-9a26-c22503011d54.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Je nach Konfiguration von Office 365 haben Benutzer möglicherweise die Möglichkeit, eine blockierte Datei herunterzuladen. So sieht das Herunterladen einer blockierten Datei auf dem mobilen Gerät eines Benutzers aus:
  
[![Herunterladen einer blockierten Datei in OneDrive for Business](media/be288a82-bdd8-4371-93d8-1783db3b61bc.png)](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2)
  
Weitere Informationen finden Sie unter [Turn on Office 365 ATP for SharePoint, OneDrive und Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md).
  
## <a name="keep-these-points-in-mind"></a>Bedenken Sie diese Punkte

- ATP prüft nicht jede einzelne Datei in SharePoint Online, OneDrive for Business oder Microsoft Teams. Dies ist so beabsichtigt. Dateien werden asynchron durch einen Prozess übertragen, der Freigabe-und Gast Aktivitätsereignisse sowie intelligente Heuristiken und Bedrohungs Signale zur Identifizierung schädlicher Dateien verwendet.

- Stellen Sie sicher, dass Ihre SharePoint-Websites so konfiguriert sind, dass Sie die [moderne Umgebung](https://docs.microsoft.com/sharepoint/guide-to-sharepoint-modern-experience)verwenden. Wenn eine Datei als bösartig und blockiert identifiziert wird, können die Benutzer erkennen, dass dies in der modernen Benutzeroberfläche stattgefunden hat, aber nicht in der klassischen Ansicht. ATP Protection gilt unabhängig davon, ob die moderne Erfahrung oder die klassische Ansicht verwendet wird; visuelle Indikatoren, die eine Datei blockiert, sind jedoch nur in der modernen Umgebung vorhanden.
    
- Dateien, die in SharePoint Online, OneDrive for Business oder Microsoft Teams als schädlich identifiziert werden, werden in [Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md) und im Threat Explorer (Teil von [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md) ) angezeigt. ).
    
- ATP ist Teil der allgemeinen Bedrohungsschutz Strategie Ihrer Organisation, die Schutz vor Spam und Schadsoftware sowie sichere Links und sichere Anlagen umfasst. Weitere Informationen finden Sie unter [schützen vor Bedrohungen in Office 365](protect-against-threats.md).
    
- Ein SharePoint Online-Administrator kann festlegen, ob Benutzer Dateien herunterladen können, die als bösartig erkannt werden. Führen Sie dazu das PowerShell-Cmdlet Set-SPOTenant mithilfe eines DisallowInfectedFileDownload-Parameters aus (siehe [Turn on Office 365 ATP for SharePoint, OneDrive und Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md)).
    
## <a name="quarantine-in-atp-for-sharepoint-online-onedrive-for-business-and-microsoft-teams"></a>Quarantäne in ATP für SharePoint Online, OneDrive for Business und Microsoft Teams

 Ab Ende Mai 2018 werden die [Quarantäne](quarantine-email-messages.md) Funktionen im Security &amp; Compliance Center auf ATP für SharePoint Online, OneDrive for Business und Microsoft Teams ausgedehnt.
  
Wenn eine Datei in SharePoint Online, OneDrive for Business oder Microsoft Teams als bösartig identifiziert wird, wird die Datei zusätzlich zu den ATP-Blockierungen, die geöffnet oder freigegeben werden sollen, in eine Liste von isolierten Elementen aufgenommen. (Wechseln Sie im &amp; Security Compliance Center zu **Threat Management** \> **Review** \> **Quarantine** , und Filtern Sie nach **Inhalten**.) 
  
Wenn Sie Teil des Office 365-Sicherheitsteams Ihrer Organisation sind und über die erforderlichen [Berechtigungen im Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md)verfügen, können Sie Dateien herunterladen, freigeben, melden und löschen, die von ATP als bösartig erkannt werden. aus der Quarantäne.
  
- Durch das **Freigeben und melden** einer Datei wird der ATP-Block für die Datei in der entsprechenden Teamwebsite oder Dokumentbibliothek für SharePoint, OneDrive oder Microsoft Teams entfernt. Benutzer können die Datei dann öffnen, freigeben und herunterladen. Und wenn die Option **Bericht an Microsoft senden** ausgewählt ist, wird die Datei als falsch positives Ergebnis an Microsoft gemeldet. 
    
- Durch das **Löschen einer Datei** wird die Datei aus der Quarantäne entfernt; die Datei kann jedoch noch nicht geöffnet oder freigegeben werden. Die Datei muss auch in der jeweiligen Dokumentbibliothek oder Teamwebsite (SharePoint Online, OneDrive for Business oder Microsoft Teams) gelöscht werden. 
    
- Beim **Herunterladen einer Datei** können Sie die Datei herunterladen und für alle falsch positive Ergebnisse analysieren. 
    
## <a name="next-steps"></a>Nächste Schritte

1. [Aktivieren von Office 365 ATP für SharePoint, OneDrive und Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md)
    
2. [Anzeigen von Informationen zu schädlichen Dateien, die in SharePoint, OneDrive oder Microsoft Teams erkannt wurden](malicious-files-detected-in-spo-odb-or-teams.md)
    
