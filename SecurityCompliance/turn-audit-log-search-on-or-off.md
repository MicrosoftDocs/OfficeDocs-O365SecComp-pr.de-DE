---
title: Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Sie können die Suchfunktion des Überwachungsprotokolls im Security & Compliance Center aktivieren. Wenn Sie es ändern, können Sie jederzeit deaktivieren. Wenn die Überwachungsprotokoll Suche deaktiviert ist, können Administratoren das Office 365-Überwachungsprotokoll nicht nach Benutzer-und Administratoraktivitäten in Ihrer Organisation durchsuchen.
ms.openlocfilehash: 0619b19f9dc6e8bdc21e26275f02a81948b40bf4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265377"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a>Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche

Sie (oder ein anderer Administrator) muss die Überwachungsprotokollierung aktivieren, bevor Sie mit der Durchsuchung des Office 365-Überwachungsprotokolls beginnen können. Wenn die Überwachungsprotokoll Suche im Security & Compliance Center aktiviert ist, werden die Benutzer-und Administratoraktivitäten Ihrer Organisation im Überwachungsprotokoll aufgezeichnet und für 90 Tage aufbewahrt. Ihre Organisation möchte jedoch möglicherweise keine Überwachungsprotokolldaten aufzeichnen und aufbewahren. Oder Sie verwenden möglicherweise eine Drittanbieter-App für das Security Information and Event Management (SIEM), um auf Ihre Überwachungsdaten zuzugreifen. In diesen Fällen kann ein globaler Administrator die Suchprotokoll Suche in Office 365 deaktivieren.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen in Exchange Online über die Rolle "Überwachungsprotokolle" verfügen, um die Überwachungsprotokoll Suche in Ihrer Office 365-Organisation zu aktivieren oder zu deaktivieren. Diese Rolle wird standardmäßig der Rollengruppe "Compliance-Management" und "Organisationsverwaltung" auf der Seite " **Berechtigungen** " im Exchange Admin Center zugewiesen. Globale Administratoren in Office 365 sind Mitglieder der Rollengruppe "Organisationsverwaltung" in Exchange Online. 
    
    > [!IMPORTANT]
    > Benutzer müssen in Exchange Online über Berechtigungen verfügen, um die Überwachungsprotokoll Suche ein-oder auszuschalten. Wenn Sie Benutzern die Rolle "Überwachungsprotokolle" auf der Seite " **Berechtigungen** " im Security _AMP_ Compliance Center zuweisen, können Sie die Überwachungsprotokoll Suche nicht aktivieren oder deaktivieren. Dies liegt daran, dass das zugrunde liegende Cmdlet ein Exchange Online-Cmdlet ist. 
  
- Wenn Sie die Überwachungsprotokoll Suche in Office 365 deaktivieren, können Sie die Office 365-Verwaltungs Aktivitäts-API nicht verwenden, um auf Überwachungsdaten für Ihre Organisation zuzugreifen. Durch das Deaktivieren der Überwachungsprotokoll Suche mithilfe der Schritte in diesem Artikel werden keine Ergebnisse zurückgegeben, wenn Sie das Überwachungsprotokoll mithilfe des Security & Compliance Center durchsuchen oder wenn Sie das Cmdlet **Search-UnifiedAuditLog** in Exchange Online ausführen. PowerShell. Dies hat auch zur Folge, dass die Überwachungsprotokolle nicht über die Office 365-Verwaltungs Aktivitäts-API verfügbar sind.  
    
- Schrittweise Anleitungen zum Durchsuchen des Office 365-Überwachungsprotokolls finden Sie unter durch [Suchen des Überwachungsprotokolls im Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md).
    
## <a name="turn-on-audit-log-search"></a>Aktivieren der Überwachungsprotokoll Suche

Sie können das Security & Compliance Center oder PowerShell verwenden, um die Suche nach Überwachungsprotokollen in Office 365 zu aktivieren. Es kann mehrere Stunden dauern, bis Sie die Überwachungsprotokoll Suche aktiviert haben, bevor Sie beim Durchsuchen des Überwachungsprotokolls Ergebnisse zurückgeben können. Sie müssen in Exchange Online über die Rolle "Überwachungsprotokolle" verfügen, um die Suche nach Überwachungsprotokollen zu aktivieren.
  
### <a name="use-the-security--compliance-center-to-turn-on-audit-log-search"></a>Verwenden des Security & Compliance Center zum Aktivieren der Überwachungsprotokoll Suche

1. Wechseln Sie im Security & Compliance Center zur **** \> Such **Überwachungsprotokoll**Suche.
    
2. Klicken Sie auf **Aufzeichnung von Benutzer-und Administratoraktivitäten starten**.
    
    ![Klicken Sie auf Aufzeichnung von Benutzer-und Administratoraktivitäten starten, um die Überwachung zu aktivieren.](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    Es wird ein Dialogfeld mit der Meldung angezeigt, dass die Benutzer-und Administratoraktivitäten in Ihrer Organisation im Office 365-Überwachungsprotokoll aufgezeichnet werden und in einem Bericht angezeigt werden können. 
    
3. Klicken Sie auf **Aktivieren**.
    
    Es wird eine Meldung angezeigt, die besagt, dass das Überwachungsprotokoll vorbereitet wird, und dass Sie eine Suche nach Abschluss der Vorbereitung in wenigen Stunden ausführen können.
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a>Verwenden von PowerShell zum Aktivieren der Überwachungsprotokoll Suche

1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).
    
2. Führen Sie den folgenden PowerShell-Befehl aus, um die Suche in Office 365 zu aktivieren.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    Es wird eine Meldung angezeigt, dass es möglicherweise bis zu 60 Minuten dauert, bis die Änderung wirksam wird.
  
## <a name="turn-off-audit-log-search"></a>Deaktivieren der Überwachungsprotokoll Suche

Sie müssen die mit Ihrer Exchange Online-Organisation verbundene Remote-PowerShell verwenden, um die Überwachungsprotokoll Suche zu deaktivieren. Ähnlich wie beim Aktivieren der Überwachungsprotokoll Suche muss Ihnen die Rolle "Überwachungsprotokolle" in Exchange Online zugewiesen werden, um die Suche nach Überwachungsprotokollen zu deaktivieren.
  
1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).
    
2. Führen Sie den folgenden PowerShell-Befehl aus, um die Suche in Office 365 zu deaktivieren.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. Stellen Sie nach einer Weile sicher, dass die Überwachungsprotokoll Suche deaktiviert ist. Sie können auf zwei Arten vorgehen:
    
    - Führen Sie in PowerShell den folgenden Befehl aus:

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        Der Wert der `False` für die _UnifiedAuditLogIngestionEnabled_ -Eigenschaft gibt an, dass die Überwachungsprotokoll Suche deaktiviert ist. 
    
    - Navigieren Sie im Security & Compliance **** \> Center zur Such **Überwachungsprotokoll**Suche, und klicken Sie dann auf **Suchen**.
    
      Es wird eine Meldung angezeigt, die besagt, dass die Überwachungsprotokoll Suche nicht aktiviert ist. 
    
      ![Eine Meldung wird angezeigt, wenn die Überwachung deaktiviert ist.](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
