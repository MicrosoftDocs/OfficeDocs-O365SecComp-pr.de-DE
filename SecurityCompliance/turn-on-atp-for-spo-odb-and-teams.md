---
title: Aktivieren von Office 365 ATP für SharePoint, OneDrive und Microsoft Teams
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 02/06/2019
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 07e76024-0c80-40dc-8c48-1dd0d0f863cb
ms.collection: M365-security-compliance
description: Hier erfahren Sie, wie Sie ATP für SharePoint, OneDrive und Teams aktivieren, einschließlich der Festlegung von Warnungen für erkannte Dateien.
ms.openlocfilehash: 8ba82a812881b53636f2fbc941ee04bc5dacdac1
ms.sourcegitcommit: 32cb896aef370764ec6e8f8278ebaf16f1c5ff37
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30123896"
---
# <a name="turn-on-office-365-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Aktivieren von Office 365 ATP für SharePoint, OneDrive und Microsoft Teams

[Office 365 ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md) schützt Ihre Organisation vor versehentlicher Freigabe schädlicher Dateien. Wenn eine bösartige Datei erkannt wird, wird diese Datei blockiert, sodass niemand Sie öffnen, kopieren, verschieben oder freigeben kann, bis weitere Aktionen des Sicherheitsteams der Organisation durchgeführt werden. Lesen Sie diesen Artikel, um ATP für SharePoint, OneDrive und Teams zu aktivieren, Warnungen für die Erkennung von Dateien einzurichten und die nächsten Schritte zu Unternehmen. 
  
Um ATP-Richtlinien zu definieren (oder zu bearbeiten), muss Ihnen eine entsprechende Rolle zugewiesen werden. Einige Beispiele werden in der folgenden Tabelle beschrieben:

|Rolle  |Wo/wie zugewiesen  |
|---------|---------|
|Office 365 globaler Administrator |Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator. (Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Sicherheitsadministrator |Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online-Organisationsverwaltung |Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
  
## <a name="turn-on-atp-for-sharepoint-onedrive-and-microsoft-teams"></a>Aktivieren von ATP für SharePoint, OneDrive und Microsoft Teams

**Bevor Sie mit diesem Verfahren beginnen, sollten Sie sicherstellen, dass die Überwachungsprotokollierung für Ihre Office 365-Umgebung bereits aktiviert ist**. Dies erfolgt in der Regel durch einen Benutzer, dem die Rolle "Überwachungsprotokolle" in Exchange Online zugewiesen wurde. Weitere Informationen finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com)zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an.
    
2. wählen sie im Office 365 &amp; Security Compliance Center im linken navigationsbereich unter bedrohungs **verwaltung**die option **richtlinie** \> für **sichere anlagen**aus. <br/>![Wählen Sie im &amp; Security Compliance Center die Option Threat \> Management Policy aus.](media/08849c91-f043-4cd1-a55e-d440c86442f2.png)
  
3. Wählen Sie **ATP für SharePoint, OneDrive und Microsoft Teams aktivieren**aus.<br/>![Aktivieren von Advanced Threat Protection für SharePoint Online, OneDrive for Business und Microsoft Teams](media/48cfaace-59cc-4e60-bf86-05ff6b99bdbf.png)
  
4. Klicken Sie auf **Speichern**.
    
5. Überarbeiten Sie die Richt [Linien zu sicheren Anlagen](set-up-atp-safe-attachments-policies.md) und Richtlinien für [sichere Links](set-up-atp-safe-links-policies.md)in Ihrer Organisation.
    
6. Empfohlen Führen Sie als globaler Administrator oder SharePoint Online-Administrator das Cmdlet **[Set-SPOTenant](https://docs.microsoft.com/powershell/module/sharepoint-online/Set-SPOTenant?view=sharepoint-ps)** aus, wobei der Parameter **DisallowInfectedFileDownload** auf *true*festgelegt ist. <br/>
      - Wenn der Parameter auf *true* festgelegt wird, werden alle Aktionen (außer DELETE) für erkannte Dateien blockiert. Personen können erkannte Dateien nicht öffnen, verschieben, kopieren oder freigeben.
      - Wenn der Parameter auf *false* festgelegt wird, werden alle Aktionen außer löschen und herunterladen blockiert. Personen können das Risiko annehmen und eine erkannte Datei herunterladen.  
   
7. Sie können bis zu 30 Minuten dauern, bis Ihre Änderungen auf alle Office 365-Rechenzentren verteilt sind.
    
8. Empfohlen Gehen Sie vor, um Warnungen für erkannte Dateien einzurichten.
    
Weitere Informationen zur Verwendung von PowerShell mit Office 365 finden Sie unter [Manage office 365 with PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/manage-office-365-with-office-365-powershell). 

Weitere Informationen zur Benutzererfahrung, wenn eine Datei als bösartig erkannt wurde, finden Sie unter [Vorgehensweise, wenn eine bösartige Datei in SharePoint Online, OneDrive oder Microsoft Teams gefunden wird](https://support.office.com/article/01e902ad-a903-4e0f-b093-1e1ac0c37ad2). 
  
## <a name="set-up-alerts-for-detected-files"></a>Einrichten von Warnungen für erkannte Dateien

Um eine Benachrichtigung zu erhalten, wenn eine Datei in SharePoint Online, OneDrive for Business oder Microsoft Teams als bösartig identifiziert wurde, können Sie eine Warnung einrichten.
  
1. wählen sie im [Office 365 &amp; Security Compliance Center](https://protection.office.com) **alerts** \> **Manage alerts**aus.
    
2. Wählen Sie **neue Warnungs Richtlinie**aus.
    
3. Geben Sie einen Namen für die Warnung an. Sie können beispielsweise schädliche Dateien in Bibliotheken eingeben.
    
4. Geben Sie eine Beschreibung für die Warnung ein. Beispielsweisekönnten Sie benachrichtigt Administratoren eingeben, wenn schädliche Dateien in SharePoint Online, OneDrive oder Microsoft Teams erkannt werden.
    
5. Führen Sie im Abschnitt **Diese Warnung senden, wenn...** die folgenden Schritte aus: 
    
    a. Wählen Sie in der Liste **Aktivitäten** die Option **erkannte Schadsoftware in der Datei**aus.
    
    b. lassen Sie das Feld **Benutzer** leer. 
    
6. Wählen Sie im Abschnitt **diese Benachrichtigung senden an** einen oder mehrere globale Administratoren, Sicherheitsadministratoren oder Sicherheits Leser aus, die Benachrichtigungen erhalten sollen, wenn eine bösartige Datei erkannt wird. 
    
7. Klicken Sie auf **Speichern**.
    
Weitere Informationen zu Warnungen finden Sie unter [Create Activity Alerts in the Office 365 &amp; Security Compliance Center](create-activity-alerts.md). 
  
## <a name="next-steps"></a>Nächste Schritte

1. [Anzeigen von Informationen zu schädlichen Dateien, die in SharePoint, OneDrive oder Microsoft Teams erkannt wurden](malicious-files-detected-in-spo-odb-or-teams.md)
    
2. [Verwalten von isolierten Nachrichten und Dateien als Administrator in Office 365](manage-quarantined-messages-and-files.md)
    

  

