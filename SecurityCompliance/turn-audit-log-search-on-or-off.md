---
title: Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: e893b19a-660c-41f2-9074-d3631c95a014
description: Sie können die Audit Log-Suchfunktion in die Office 365-Sicherheit aktivieren &amp; Compliance Center. Wenn Sie Sie überlegen, können Sie aktivieren If deaktiviert zu einem beliebigen Zeitpunkt. Wenn Audit Log Suche deaktiviert ist, können nicht Administratoren das Office 365-Überwachungsprotokoll für Benutzer- und Admin-Aktivität in Ihrer Organisation suchen.
ms.openlocfilehash: 4fa6ac095222addce578294813cbd22dfc50a2ab
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529466"
---
# <a name="turn-office-365-audit-log-search-on-or-off"></a>Aktivieren oder Deaktivieren der Office 365-Überwachungsprotokollsuche

Protokollierung, bevor Sie beginnen können, suchen das Office 365-Überwachungsprotokoll müssen Sie (oder ein anderes Admin) aktivieren. Wenn audit Log-Suche in der Office 365-Sicherheit &amp; Compliance Center aktiviert ist, Benutzer und Admin-Aktivität aus Ihrer Organisation ist im Überwachungsprotokoll aufgezeichnet und 90 Tage lang aufbewahrt. Allerdings sollten Ihrer Organisation nicht zum Aufzeichnen und Aufbewahren von Audit Log-Daten. Oder möglicherweise verwenden Sie eine Anwendung Drittanbieter-Sicherheit und Ereignissen Management (SIEM) auf die Überwachung von Daten zugreifen. In diesen Fällen kann ein globaler Administrator Audit Log Suche in Office 365 deaktivieren.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen die Rolle des überwachen Protokolle im Exchange Online zu Audit Log Suche aktivieren oder deaktivieren Sie in Office 365-Organisation zugewiesen werden. Standardmäßig wird die Verwaltung der Richtlinientreue und Organization Management Rollengruppen auf der Seite **Berechtigungen** in der Exchange-Verwaltungskonsole dieser Rolle zugewiesen. Globale Administratoren in Office 365 gehören die Rollengruppe "Organisationsverwaltung" im Exchange Online. 
    
    > [!IMPORTANT]
    > Benutzer müssen Berechtigungen in Exchange Online um zu aktivieren oder deaktivieren Sie Audit Log Suche zugewiesen werden. Wenn Sie Benutzern die Rolle überwachen Protokolle auf der Seite **Berechtigungen** in das Wertpapier zuweisen &amp; Compliance Center, sie nicht möglich Audit Log Suche aktivieren oder deaktivieren. Dies ist, da das zugrunde liegende Cmdlet Exchange Online-Cmdlet ist. 
  
- Wenn Sie den Audit Log Suche in Office 365 deaktivieren, können Sie weiterhin die Office 365-Verwaltungs-Aktivität-API verwenden, Überwachung von Daten für Ihre Organisation Zugriff auf. Deaktivieren von Audit Log Suche mithilfe der Schritte in diesem Artikel bedeutet, dass keine Ergebnisse zurückgegeben werden, wenn Sie das Überwachungsprotokoll mithilfe der Sicherheits suchen &amp; Compliance Center oder bei der Ausführung des Cmdlets **Search-UnifiedAuditLog** in Exchange Online PowerShell. Wenn Sie jeder Anwendung zur Überwachung Ihrer Organisation von Daten über die Office 365-Verwaltungs-Aktivität API Zugriff erteilt haben, werden jedoch Anwendungsbereiche fortgesetzt, funktioniert. 
    
- Eine schrittweise Anleitung zum Suchen der Office 365 in das Überwachungsprotokoll, finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).
    
## <a name="turn-on-audit-log-search"></a>Schalten Sie Audit Log-Suche

Sie können die Sicherheit &amp; Compliance Center oder PowerShell, um Audit Log Suche in Office 365 zu aktivieren. Es kann einige Stunden, nachdem Sie Audit Log Suche aktivieren, bevor Sie Ergebnisse zurückgeben können, wenn Sie das Überwachungsprotokoll durchsuchen dauern. Sie müssen die Protokolle überwachen Rolle im Exchange Online zugewiesen werden um Audit Log Suche zu aktivieren.
  
### <a name="use-the-security-amp-compliance-center-to-turn-on-audit-log-search"></a>Verwenden Sie die Sicherheit &amp; Compliance Center Audit Log Suche aktivieren

1. In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Audit Log suchen**.
    
2. Klicken Sie auf **Benutzer und Admin Aktivitäten Aufzeichnung starten**.
    
    ![Klicken Sie auf „Aufzeichnung von Benutzer- und Administratoraktivitäten beginnen“, um die Überwachung zu aktivieren.](media/39a9d35f-88d0-4bbe-a962-0be2f838e2bf.png)
  
    Ein Dialogfeld wird angezeigt, dass Benutzer und die Admin-Aktivitäten in Ihrer Organisation in das Office 365-Überwachungsprotokoll aufgezeichneten und zum Anzeigen von in einem Bericht verfügbar sein werden. 
    
3. Klicken Sie auf **Aktivieren**.
    
    Eine Meldung wird angezeigt, die besagt, das Überwachungsprotokoll vorbereitet wird und dass Sie eine Suche, in ein paar Stunden ausführen können nach Abschluss die Vorbereitung.
    
### <a name="use-powershell-to-turn-on-audit-log-search"></a>Verwenden von PowerShell, Audit Log Suche aktivieren

1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).
    
2. Führen Sie den folgenden PowerShell-Befehl, um Audit Log Suche in Office 365 zu aktivieren.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $true
    ```

    Eine Meldung wird angezeigt, die besagt, dass dauert bis zu 60 Minuten, damit die Änderung wirksam wird.
  
## <a name="turn-off-audit-log-search"></a>Audit Log Suche deaktivieren

Sie müssen remote-PowerShell mit Ihrer Exchange Online-Organisation verbunden zu Audit Log deaktivieren verwenden. Ähnliche Audit Log Suche aktivieren, müssen Sie die Protokolle überwachen Rolle in Exchange Online zu Audit Log deaktivieren zugewiesen werden.
  
1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkID=396554).
    
2. Führen Sie den folgenden PowerShell-Befehl zu Audit Log in Office 365 deaktivieren.
    
    ```
    Set-AdminAuditLogConfig -UnifiedAuditLogIngestionEnabled $false
    ```

3. Nach einer gewissen stellen Sie sicher, dass die Audit Log Suche deaktiviert (Disabled) aktiviert ist. Es gibt zwei Methoden, um diese Schritte durchführen:
    
    - Führen Sie in PowerShell den folgenden Befehl ein:

        ```
        Get-AdminAuditLogConfig | FL UnifiedAuditLogIngestionEnabled
        ```

        Der Wert der `False` für die _UnifiedAuditLogIngestionEnabled_ -Eigenschaft gibt an, dass die Audit Log Suche ist deaktiviert. 
    
    - In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Suche &amp; Untersuchung** \> **Audit Log suchen**, und klicken Sie auf **Suchen**.
    
      Eine Meldung wird angezeigt, die besagt, dass Audit Log die Suche nicht aktiviert ist. 
    
      ![Eine Nachricht ist Dispayed, wenn die Überwachung deaktiviert ist](media/dca53da6-1cbe-4fa3-9860-f0d674de9538.png)
