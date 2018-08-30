---
title: Erstellen von Aktivität Warnungen in die Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/7/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- BCS160
- MET150
ms.assetid: 72bbad69-035b-4d33-b8f4-549a2743e97d
description: Hinzufügen und Verwalten von Warnungen in das Wertpapier Aktivität &amp; Compliance Center, damit die Office 365 senden Sie e-Mail-Benachrichtigung, wenn Benutzer bestimmte Aktivitäten in Office 365 ausführen.
ms.openlocfilehash: 409c1ff4c7fdd0d2d071bdb2eab08ec49357ed8a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529844"
---
# <a name="create-activity-alerts-in-the-office-365-security-amp-compliance-center"></a>Erstellen von Aktivität Warnungen in die Office 365-Sicherheit &amp; Compliance Center

Sie können eine Benachrichtigung Aktivität erstellen, die Sie eine e-Mail-Benachrichtigung senden wird, wenn Benutzer bestimmte Aktivitäten in Office 365 ausführen. Aktivität Warnungen sind vergleichbar mit der Suche für Ereignisse im Überwachungsprotokoll Office 365, passiert, außer dass Sie eine e-Mail-Nachricht, wenn ein Ereignis für eine Aktivität gesendet werden, denen Sie eine Benachrichtigung erstellt haben. 
  
 **Gründe für die Verwendung Aktivität Benachrichtigungen anstelle des Überwachungsprotokolls suchen?** Möglicherweise gibt es bestimmte Arten von Aktivitäten oder Aktivitäten, die von bestimmten Benutzern, denen Sie wirklich bekannt sein. Aktivität Benachrichtigungen können Sie anstelle der Denken Sie daran, die das Überwachungsprotokoll für die Aktivitäten durchsuchen, haben Sie eine e-Mail-Nachricht senden, wenn Benutzer diese Aktivitäten ausführen Office 365. Beispielsweise können Sie eine Benachrichtigung Aktivität benachrichtigt werden, wenn ein Benutzer Dateien in SharePoint löscht oder Sie können eine Benachrichtigung, um Sie zu benachrichtigen, wenn ein Benutzer Nachrichten dauerhaft aus dem Postfach löscht erstellen erstellen. Die an Sie gesendete e-Mail-Benachrichtigung enthält Informationen über die Aktivität ausgeführt wurde und der Benutzer, der sie ausgeführt. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen die Organisationskonfiguration Rolle in das Wertpapier zugewiesen &amp; Compliance Center Aktivität Benachrichtigungen verwalten. Standardmäßig wird die Rollengruppen Compliance-Administrator und Organization Management dieser Rolle zugewiesen. Weitere Informationen zum Hinzufügen von Mitgliedern zu Rollengruppen finden Sie unter [Gewähren des Zugriffs auf die Office 365-Sicherheit &amp; Compliance Center](grant-access-to-the-security-and-compliance-center.md).
    
- Sie (oder ein anderes Admin) muss zuerst aktivieren überwachungsprotokollierung für Ihre Organisation bevor Sie Aktivität Warnungen verwenden können. Zu diesem Zweck klicken Sie einfach auf der Seite **Aktivität Warnungen** **Benutzer- und Admin Aktivität Aufzeichnung starten** . (Wenn Sie diese Verknüpfung nicht angezeigt wird, wurde die Überwachung bereits für Ihre Organisation aktiviert.) Sie können auch auf der Seite **Audit Log Suche** in das Wertpapier Überwachung aktivieren &amp; Compliance Center (Wechseln Sie zu **Suche &amp; Untersuchung** \> **Audit Log Suche**). Sie müssen nur führen Sie diesen Schritt einmal für Ihre Organisation.
    
- Sie können die Seite **Warnungen** in das Wertpapier &amp; Compliance Center zum Erstellen von Benachrichtigungen nur für die Aktivitäten von Benutzern, die im Adressbuch Ihrer Organisation aufgeführt sind. Auf dieser Seite können Sie Benachrichtigungen für Aktivitäten durch externe Benutzer erstellen. 
    
- [Weitere Informationen](#more-information) finden Sie im Abschnitt für eine Liste der gängigen Szenarien (und der bestimmten Aktivität zum Überwachen), dass Sie Warnungen für erstellen können. 
    
- Sie können Warnungen für die gleichen Aktivitäten erstellen, die Sie in das Überwachungsprotokoll Office 365 suchen können. 
    
## <a name="create-an-activity-alert"></a>Erstellen einer Warnung Aktivität

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365.
    
3. Klicken Sie im linken Bereich auf **Benachrichtigungen**, und klicken Sie dann auf **Benachrichtigungen verwalten**.
    
4. Klicken Sie auf der Seite **Aktivität Benachrichtigungen** auf **Hinzufügen eine Benachrichtigung**.
    
    ![Hinzufügen einer Benachrichtigung für eine Aktivität](media/53888bd5-9fa2-4398-8ccc-1a9dc72517ac.png)
  
5. Füllen Sie die folgenden Felder zum Erstellen einer Warnung:
    
    a. **Name** – Geben Sie einen Namen für die Benachrichtigung. Warnungsnamen müssen innerhalb Ihrer Organisation eindeutig sein.
    
    B. **Beschreibung** (Optional) – beschreibt die Warnung, wie die Aktivitäten und nachverfolgt, Benutzer und an die Benutzer, die e-Mail-Benachrichtigungen gesendet werden. Beschreibungen bieten eine schnelle und einfache Möglichkeit, den Zweck der Benachrichtigung, um andere Administratoren zu beschreiben.
    
    c. **senden, die diese Warnung bei** - klicken Sie auf **Diese Warnung bei senden** und konfigurieren Sie anschließend diese beiden Felder:
    
    - **Aktivitäten** - klicken Sie auf die Dropdown-Liste die Aktivitäten angezeigt werden sollen, denen Sie für eine Benachrichtigung erstellen können. Dies ist die gleiche Aktivitätenliste, die angezeigt wird, wenn Sie das Office 365-Überwachungsprotokoll durchsuchen. Sie können eine oder mehrere bestimmte Aktivitäten auswählen, oder auf den Gruppennamen Aktivität, um alle Aktivitäten in der Gruppe auszuwählen. Eine Beschreibung dieser Aktivitäten finden Sie im Abschnitt "Überwacht Aktivitäten" bei der [Suche der Überwachungsprotokolle melden Sie sich bei der Office 365-Sicherheit und Compliance Center](search-the-audit-log-in-security-and-compliance.md#audited-activities). Wenn ein Benutzer Aktivitäten, die Sie an der Warnung hinzugefügt haben ausführt, wird eine e-Mail-Benachrichtigung gesendet. 
    
     - **Benutzer** : Klicken Sie auf dieses Feld, und wählen Sie dann einen oder mehrere Benutzer aus. Wenn die Benutzer in dieses Feld die Aktivitäten, die Sie in das Feld **Aktivitäten** hinzugefügt haben ausführen, wird eine Benachrichtigung gesendet werden. Lassen Sie das Feld **Benutzer** leer, um eine Benachrichtigung zu senden, wenn jeder Benutzer in Ihrer Organisation die Aktivitäten von der Benachrichtigung für die angegebene ausführt. 
    
    **dieser Warnung senden** - d auf **Diese Warnung senden**, und klicken Sie im Feld **Empfänger** und geben Sie einen Namen, einen Benutzer hinzuzufügen, eine e-Mail-Benachrichtigung erhält, wenn ein Benutzer (in das Feld **Benutzer** angegeben) eine Aktivität ausführt (angegebenen in der **Aktivitäten** im Feld). Beachten Sie, dass Sie die Liste der Empfänger standardmäßig hinzugefügt. Sie können Ihren Namen aus dieser Liste entfernen.
    
6. Klicken Sie auf **Speichern** , um die Benachrichtigung zu erstellen. 
    
    Die neue Warnung wird in der Liste auf der Seite **Aktivität Warnungen** angezeigt. 
    
    ![Eine Liste der Benachrichtigungen wird angezeigt, auf der Seite Aktivität Warnungen in das Wertpapier &amp; Compliance Center](media/02b774f2-1719-41de-bbc9-5e5b7576f335.png)
  
    Der Status der Warnung wird auf **aktiviert**festgelegt. Beachten Sie, dass die Empfänger eine e-Mail-Benachrichtigung empfangen wird, wenn eine Benachrichtigung gesendet wird ebenfalls aufgelistet sind. 
  
## <a name="turn-off-an-activity-alert"></a>Eine Aktivität Benachrichtigung deaktivieren

Sie können eine Aktivität Benachrichtigung deaktivieren, damit eine e-Mail-Benachrichtigung gesendet. Nachdem Sie die Aktivität Warnung deaktivieren, es wird weiterhin in der Liste der Aktivität Benachrichtigungen für Ihre Organisation angezeigt, und Sie können immer noch seine Eigenschaften anzeigen.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich mit Ihrem Konto arbeiten oder Schule Office 365.
    
3. Klicken Sie im linken Bereich auf **Benachrichtigungen**, und klicken Sie dann auf **die Aktivität Benachrichtigungen verwalten**.
    
4. Klicken Sie in der Liste der Benachrichtigungen für Ihre Organisation auf die Benachrichtigung, die Sie deaktivieren möchten.
    
5. Klicken Sie auf der Seite **Warnung bearbeiten** klicken Sie auf die Umschaltfläche **auf** zum Ändern des Status auf **deaktiviert**, und klicken Sie dann auf **Speichern**.
    
    Der Status der Warnung auf den Seiten der Aktivität Benachrichtigungen wird auf **deaktiviert**festgelegt. 
    
Wenn Sie um eine Benachrichtigung Aktivität wieder zu aktivieren, wiederholen Sie diese Schritte, und klicken Sie auf die Umschaltfläche **deaktiviert** zum Ändern des Status auf **aktiviert**.
  
## <a name="more-information"></a>Weitere Informationen

- Es folgt ein Beispiel für die e-Mail-Benachrichtigung, die an die Benutzer gesendet wird, die in der diesem Feld (und unter aufgeführten **Empfänger** auf der Seite **Aktivität Warnungen** ) in das Wertpapier Warnung gesendete angegeben sind &amp; Compliance Center. 
    
    ![Beispiel für eine e-Mail-Notification für eine Aktivität-Warnung gesendet](media/a5f91611-fae6-4fe9-82f5-58521a2e2541.png)
  
- Hier sind einige gängige Dokument- und e-Mail-Aktivitäten, Sie können eine Aktivität für Warnungen. In den Tabellen beschreibt die Aktivität, den Namen der Aktivität auf eine Benachrichtigung erstellen und den Namen der Aktivitätsgruppe, die die Aktivität in der Dropdown-Liste von **Aktivitäten** unter aufgeführt wird. Um eine vollständige Liste der Aktivitäten anzuzeigen, die Sie Warnungen für Aktivität erstellen können, finden Sie unter im Abschnitt "Überwacht Aktivitäten" bei der [Suche der Überwachungsprotokolle melden Sie sich bei der Office 365-Sicherheit und Compliance Center](search-the-audit-log-in-security-and-compliance.md#audited-activities).
    
    > [!TIP]
    > Sie möchten möglicherweise eine Aktivität Benachrichtigung nur eine Aktivität erstellen, die von jedem Benutzer ausgeführt wird. Oder Sie möchten möglicherweise eine Aktivität-Benachrichtigung, die mehrere Aktivitäten von mindestens einer der u. a. nachverfolgen erstellen Benutzer. 
  
    Die folgende Tabelle enthält einige gängige dokumentbezogene Aktivitäten in SharePoint oder OneDrive für Unternehmen.
    
    |**Wenn ein Benutzer...**|**Erstellen einer Warnung für diese Aktivität**|**Aktivitätsgruppe**|
    |:-----|:-----|:-----|
    |Ansichten ein Dokuments auf einer Website.  <br/> |Geöffneten Datei  <br/> |Datei- und Aktivitäten  <br/> |
    |Bearbeitet oder ein Dokument geändert.  <br/> |Geänderte Datei  <br/> |Datei- und Aktivitäten  <br/> |
    |Teilt ein Dokument mit einem Benutzer außerhalb Ihrer Organisation.  <br/> |Freigeben von Dateien, Ordner oder Website  <br/> Und  <br/> Einladung zur Freigabe erstellt  <br/> Weitere Informationen finden Sie unter [Überwachung in das Überwachungsprotokoll Office 365 Freigabe verwenden](use-sharing-auditing.md).  <br/> |Freigabe und Access Anforderung Aktivitäten  <br/> |
    |Hoch- oder ein Dokument heruntergeladen.  <br/> |Hochgeladene Datei  <br/> Und/oder  <br/> Heruntergeladene Datei  <br/> |Datei- und Aktivitäten  <br/> |
    |Ändert die Zugriffsberechtigungen auf einer Website.  <br/> |Geänderte Projektwebsite-Berechtigungen  <br/> |Site-Verwaltungsaktivitäten  <br/> |

    Die folgende Tabelle enthält einige gängige e-Mail-bezogenen Aktivitäten in Exchange Online.

    |**Wenn ein Benutzer...**|**Erstellen einer Warnung für diese Aktivität**|**Aktivitätsgruppe**|
    |:-----|:-----|:-----|
    |Dauerhaft gelöscht (entfernt) eine e-Mail-Nachrichten aus dem Postfach.  <br/> |Gelöschten Nachrichten aus dem Postfach von  <br/> | Exchange-Postfach-Aktivitäten  <br/> |
    |Sendet eine e-Mail-Nachricht von einem freigegebenen Postfach an.  <br/> |Gesendete Nachricht mit der Berechtigung Senden als  <br/> Und  <br/> Nachricht gesendet Senden im Auftrag von Berechtigungen  <br/> | Exchange-Postfach-Aktivitäten  <br/> |
   
- Sie können auch die Cmdlets **New-ActivityAlert** und **Set-ActivityAlert** -Sicherheit &amp; Compliance Center PowerShell zum Erstellen und Bearbeiten von Warnungen Aktivität. Behalten Sie Folgendes im Hinterkopf, wenn Sie diese Cmdlets zum Erstellen oder Bearbeiten von Warnungen Aktivität verwenden: 
    
  - Wenn Sie ein Cmdlet verwenden, um eine Aktivität auf die Warnung hinzuzufügen, die in der Dropdown-Liste von **Aktivitäten** nicht aufgeführt ist, wird eine Meldung in angezeigt auf der Eigenschaftenseite für die Warnung, die besagt, "Diese Warnung hat benutzerdefinierte Vorgänge, die nicht im Auswahltool aufgeführt." 
    
  - Verwenden Sie die Cmdlets zum Erstellen oder bearbeiten eine Benachrichtigung Aktivität ein wichtiger Grund ist das Senden von e-Mail-Benachrichtigungen an eine Person außerhalb Ihrer Organisation. Diese externe Benutzer wird in der Liste der Empfänger für die Benachrichtigung aufgeführt. Aber wenn Sie diese externen Benutzer aus der Benachrichtigung entfernen möchten, dass der Benutzer kann nicht erneut hinzugefügt an der Warnung mithilfe der Seite **Warnung bearbeiten** in das Wertpapier &amp; Compliance Center. Sie müssen den externen Benutzer mit dem Cmdlet **Set-ActivityAlert** erneut hinzufügen, oder verwenden Sie das Cmdlet **New-ActivityAlert** so eine neue Benachrichtigung der externe Benutzer denselben (oder anderen) hinzu. 
    
  

