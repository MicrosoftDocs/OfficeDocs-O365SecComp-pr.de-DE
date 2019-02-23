---
title: Aktivieren der Postfachüberwachung in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: In Office 365 können Sie die postfachüberwachungsprotokollierung aktivieren, um den Postfachzugriff durch Postfachbesitzer, Stellvertretungen und Administratoren zu protokollieren. Die postfachüberwachung in Office 365 ist standardmäßig nicht aktiviert. Nachdem Sie die postfachüberwachungsprotokollierung für ein Postfach aktiviert haben, können Sie im Office 365-Überwachungsprotokoll nach Aktivitäten suchen, die für das Postfach durchgeführt werden.
ms.openlocfilehash: bb110e95d27feb8ae82b62803d218a2b38528692
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214605"
---
# <a name="enable-mailbox-auditing-in-office-365"></a>Aktivieren der Postfachüberwachung in Office 365
  
In Office 365 können Sie die postfachüberwachungsprotokollierung aktivieren, um den Postfachzugriff durch Postfachbesitzer, Stellvertretungen und Administratoren zu protokollieren. Die postfachüberwachung in Office 365 ist standardmäßig nicht aktiviert. Dies führt dazu, dass Post Fach Überwachungsereignisse nicht in den Ergebnissen angezeigt werden, wenn Sie das Office 365-Überwachungsprotokoll für die Post Fach Aktivität durchsuchen. Nachdem Sie die postfachüberwachungsprotokollierung für ein Benutzerpostfach aktiviert haben, können Sie das Überwachungsprotokoll nach Postfachaktivitäten durchsuchen. Wenn die postfachüberwachungsprotokollierung aktiviert ist, werden außerdem einige Aktionen von Administratoren, Stellvertretungen und Besitzern standardmäßig protokolliert. Weitere Informationen finden Sie unter Schritt 3.

## <a name="before-you-begin"></a>Bevor Sie beginnen
  
- Sie müssen Exchange Online PowerShell verwenden, um die postfachüberwachungsprotokollierung zu aktivieren. Sie können das Office 365 Security &amp; Compliance Center oder das Exchange Admin Center nicht verwenden.
    
- Sie können die postfachüberwachungsprotokollierung für das Postfach, das einer Office 365-Gruppe oder einem Team in Microsoft Teams zugeordnet ist, nicht aktivieren.
    
- Ein Administrator, dem Vollzugriff für ein Benutzerpostfach gewährt wurde, gilt als Stellvertreter.
  
## <a name="step-1-connect-to-exchange-online-powershell"></a>Schritt 1: Herstellen einer Verbindung mit Exchange Online PowerShell

1. Öffnen Sie auf Ihrem lokalen Computer Windows PowerShell, und führen Sie dann den folgenden Befehl aus.
   
    ```
    $UserCredential = Get-Credential
    ```

2. Geben Sie im Dialogfeld **Bei Windows PowerShell anmelden** den Benutzernamen und das Kennwort des globalen Office 365-Administratorkontos ein, und klicken Sie dann auf **OK**.
    
3. Führen Sie den folgenden Befehl aus:
    
    ```
    $Session = New-PSSession -ConfigurationName Microsoft.Exchange -ConnectionUri https://outlook.office365.com/powershell-liveid/ -Credential $UserCredential -Authentication Basic -AllowRedirection
    ```

3. Führen Sie den folgenden Befehl aus.

    ```
    Import-PSSession $Session
    ```
   
4. Um zu prüfen, ob Sie mit Ihrer Exchange Online-Organisation verbunden sind, führen Sie den folgenden Befehl aus, um eine Liste aller Postfächer in Ihrer Organisation abzurufen.
    
    ```
    Get-Mailbox
    ```
  
Weitere Informationen oder Hinweise bei Problemen mit der Verbindung zu Ihrer Exchange Online-Organisation finden Sie unter [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283).
  
## <a name="step-2-enable-mailbox-audit-logging"></a>Schritt 2: Aktivieren der Postfachüberwachungsprotokollierung

Nachdem Sie eine Verbindung mit Ihrer Exchange Online-Organisation hergestellt haben, verwenden Sie PowerShell, um die postfachüberwachungsprotokollierung für ein Postfach zu aktivieren. Alternativ können Sie die postfachüberwachung für alle Postfächer in Ihrer Organisation aktivieren.
  
In diesem Beispiel wird die postfachüberwachungsprotokollierung für das Postfach von Pilar Pinilla aktiviert.
  
```
Set-Mailbox -Identity "Pilar Pinilla" -AuditEnabled $true
```

Dieses Beispiel aktiviert die Überwachungsprotokollierung für alle Postfächer in Ihrer Organisation.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditEnabled $true
```
  
## <a name="step-3-specify-owner-actions-to-audit"></a>Schritt 3: Festlegen der zu überwachenden Aktionen des Postfachbesitzers

Wenn Sie die Überwachung für ein Postfach aktivieren, werden einige vom Postfachbesitzer ausgeführte Aktionen standardmäßig überwacht. Sie müssen andere zu überwachende Besitzer Aktionen angeben. Eine Liste und Beschreibung der Besitzer Aktionen, die standardmäßig protokolliert werden, sowie die anderen Aktionen, die überwacht werden können, finden Sie in der Tabelle im Abschnitt über die [Post Fach Überwachungsaktionen](#mailbox-auditing-actions) . 
  
In diesem Beispiel werden die **Mailbox Login:** -und **HardDelete** -Besitzer Aktionen der postfachüberwachung für das Postfach von Pilar Pinilla hinzugefügt. In diesem Beispiel wird davon ausgegangen, dass die postfachüberwachung für dieses Postfach bereits aktiviert wurde. 

```
Set-Mailbox "Pilar Pinilla" -AuditOwner @{Add="MailboxLogin","HardDelete"}
```

In diesem Beispiel wird die postfachüberwachungsprotokollierung für das Postfach von Don Hall aktiviert, und es wird angegeben, dass nur die vom Postfachbesitzer ausgeführte **Mailbox Login:** -Aktion protokolliert wird. Beachten Sie, dass in diesem Beispiel die UpdateFolderPermissions-Standardaktion überschrieben wird. 
  
```
Set-Mailbox "Don Hall" -AuditEnabled $true -AuditOwner MailboxLogin
```
   
In diesem Beispiel werden die **Mailbox Login:**-, **HardDelete**-und **SoftDelete** -Besitzer Aktionen allen Postfächern in der Organisation hinzugefügt. In diesem Beispiel wird davon ausgegangen, dass die postfachüberwachung für alle Postfächer bereits aktiviert wurde. 
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditOwner @{Add="MailboxLogin","HardDelete","SoftDelete"}
```
  
## <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?

Um zu überprüfen, ob Sie die Überwachungsprotokollierung für ein Postfach erfolgreich aktiviert haben, verwenden Sie das **Get-Mailbox**-Cmdlet zum Abrufen der Überwachungseinstellungen für dieses Postfach. 
  
In diesem Beispiel werden die Überwachungseinstellungen für Pilar Pinilla abgerufen.

```
Get-Mailbox "Pilar Pinilla"| FL Audit*
```
   
Dieses Beispiel ruft die Überwachungseinstellungen für alle Benutzerpostfächer in Ihrer Organisation ab.

```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,Audit*
```
   
Der Wert **true** für die **AuditEnabled** -Eigenschaft überprüft, ob die postfachüberwachungsprotokollierung aktiviert ist. 
    
## <a name="mailbox-auditing-actions"></a>Aktionen für die postfachüberwachung
  
In der folgenden Tabelle sind die Aktionen aufgeführt, die von der postfachüberwachungsprotokollierung protokolliert werden können. Die Tabelle enthält die Aktion, die für die verschiedenen Benutzeranmelde Typen protokolliert werden kann. In der Tabelle gibt ein **Nein** an, dass für diesen Anmeldetyp keine Aktion protokolliert werden kann. Ein Sternchen ( **\*** ) gibt an, dass die Aktion standardmäßig protokolliert wird, wenn die postfachüberwachungsprotokollierung für das Postfach aktiviert ist. 
  
|**Aktion**|**Beschreibung**|**Administrator**|**Stellvertretung\*\*\***|**Besitzer**|
|:-----|:-----|:-----|:-----|:-----|
|**Kopieren** <br/> |Eine Nachricht wurde in einen anderen Ordner kopiert.  <br/> |Ja  <br/> |Nein   <br/> |Nein  <br/> |
|**Erstellen** <br/> |Ein Element wird im Ordner Kalender, Kontakte, Notizen oder Aufgaben im Postfach erstellt. Beispielsweise wird eine neue Besprechungsanfrage erstellt. Beachten Sie, dass das Erstellen, senden oder Empfangen einer Nachricht nicht überwacht wird. Außerdem wird das Erstellen eines Postfachordners nicht überwacht.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**FolderBind** <br/> |Auf einen Postfachordner wurde zugegriffen. Diese Aktion wird auch protokolliert, wenn der Administrator oder der delegierte Benutzer das Postfach öffnet.  <br/> |Ja  <br/> |Ja\*\*  <br/> |Nr.  <br/> |
|**HardDelete** <br/> |Eine Nachricht wurde endgültig aus dem Ordner "Wiederherstellbare Elemente" gelöscht.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**Mailbox Login:** <br/> |Der Benutzer hat sich bei seinem Postfach angemeldet.  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|**MessageBind** <br/> |Eine Nachricht wurde im Vorschaufenster angezeigt oder geöffnet.  <br/> |Ja  <br/> |Nein   <br/> |Nein  <br/> |
|**Verschieben** <br/> |Eine Nachricht wurde in einen anderen Ordner verschoben.  <br/> |Ja  <br/> |Ja   <br/> |Ja   <br/> |
|**MoveToDeletedItems** <br/> |Eine Nachricht wurde gelöscht und in den Ordner „Gelöschte Objekte“ verschoben.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**SendAs** <br/> |Eine Nachricht wurde mithilfe der SendAs-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht so gesendet hat, dass sie vom Postfachbesitzer zu kommen scheint.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Nein  <br/> |
|**SendOnBehalf** <br/> |Eine Nachricht wurde mithilfe der SendOnBehalf-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht im Namen des Postfachbesitzers gesendet hat. Für den Empfänger ist in der Nachricht angegeben, in wessen Namen die Nachricht gesendet wurde und wer die Nachricht tatsächlich gesendet hat.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Nein  <br/> |
|**SoftDelete** <br/> |Eine Nachricht wurde dauerhaft gelöscht oder aus dem Ordner „Gelöschte Objekte“ gelöscht. Vorübergehend gelöschte Elemente werden in den Ordner „Wiederherstellbare Elemente“ verschoben.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**Aktualisieren** <br/> |Eine Nachricht oder deren Eigenschaften wurden geändert.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**UpdateCalendarDelegation** <br/> |Einem Postfach wurde eine Kalender Delegierung zugewiesen. Die Kalender Delegierung erteilt anderen Benutzern in derselben Organisation Berechtigungen zum Verwalten des Kalenders des Postfachbesitzers.  <br/> |Ja\*  <br/> |Nein  <br/> |Ja\*  <br/> |
|**UpdateFolderPermissions** <br/> |Eine Ordnerberechtigung wurde geändert. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Ordner in einem Postfach und die Nachrichten zugreifen können, die sich in diesen Ordnern befinden.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
|**UpdateInboxRules** <br/> |Eine Posteingangsregel wurde hinzugefügt, entfernt oder geändert. PostEingangsregeln werden verwendet, um Nachrichten im Posteingang des Benutzers basierend auf den angegebenen Bedingungen zu verarbeiten und Aktionen auszuführen, wenn die Bedingungen einer Regel erfüllt sind, beispielsweise das Verschieben einer Nachricht in einen bestimmten Ordner oder das Löschen einer Nachricht.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Wird standardmäßig überwacht, wenn die Überwachung für ein Postfach aktiviert ist.<br/><br/>  <sup>\*\*</sup>Einträge für Ordner Bindungs Aktionen, die von Stellvertretern ausgeführt werden, werden konsolidiert. Ein Protokolleintrag wird für den Zugriff einzelner Ordner innerhalb von 24 Stunden generiert.<br/><br/><sup>\*\*\*</sup>Ein Administrator, dem die Berechtigung Vollzugriff für das Postfach eines Benutzers zugewiesen wurde, wird als Stellvertreter-Benutzer betrachtet. 
  
Wenn bestimmte Arten von Postfachaktionen nicht mehr überwacht werden müssen, sollten Sie die Überwachungs Protokollierungskonfiguration des Postfachs ändern, um diese Aktionen zu deaktivieren. Vorhandene Protokolleinträge werden erst gelöscht, wenn die Aufbewahrungszeit für Überwachungsprotokolleinträge erreicht ist. Weitere Informationen zum Aufbewahrungszeitraum für Überwachungsprotokolleinträge finden Sie im Abschnitt "Before You Begin" unter [Durchsuchen des Überwachungsprotokolls im Office 365 Security _AMP_ Compliance Center](search-the-audit-log-in-security-and-compliance.md#before-you-begin).
  
## <a name="more-infotab"></a>[Weitere Informationen](#tab/)
  
- Verwenden Sie das Office 365-Überwachungsprotokoll, um nach protokollierten Postfachaktivitäten zu suchen. Sie können nach Aktivitäten für ein bestimmtes Benutzerpostfach suchen. Der folgende Screenshot zeigt eine Liste der Postfachaktivitäten, nach denen Sie im Office 365-Überwachungsprotokoll suchen können. Beachten Sie, dass diese Aktivitäten die gleichen Aktionen sind, die im Abschnitt "Post Fach Überwachungsaktionen" in diesem Thema beschrieben werden.
    
    ![Sie können das Office 365-Überwachungsprotokoll für Post Fach Überwachungsaktionen durchsuchen, indem Sie in der Dropdownliste Aktivitäten die Option "Exchange-Postfachaktivitäten" auswählen.](media/fadc34f8-9de2-4688-8b1a-bc5540e69a23.png)
  
    In der folgenden Tabelle werden die einzelnen Postfachaktivitäten beschrieben, nach denen Sie suchen können, und die entsprechende Aktion für die postfachüberwachung.
    
    |**Aktivität im Überwachungsprotokoll**|**Aktion zum Überwachen von Postfächern**|
    |:-----|:-----|
    |Erstelltes Postfachelement  <br/> |Erstellen  <br/> |
    |Nachrichten in einen anderen Ordner kopiert  <br/> |Kopieren  <br/> |
    |Benutzer bei Postfach angemeldet  <br/> |Mailbox Login:  <br/> |
    |Gesendete Nachricht mithilfe von "Senden im Auftrag von"-Berechtigungen  <br/> |SendOnBehalf  <br/> |
    |Gelöschte Nachrichten aus dem Postfach  <br/> |HardDelete  <br/> |
    |Nachrichten in Ordner "Gelöschte Elemente" verschoben  <br/> |MoveToDeletedItems  <br/> |
    |Nachrichten in einen anderen Ordner verschoben  <br/> |Verschieben  <br/> |
    |Gesendete Nachricht unter Verwendung der Berechtigung "Senden als"  <br/> |SendAs  <br/> |
    |Aktualisierte Nachricht  <br/> |Aktualisieren  <br/> |
    |Gelöschte Nachrichten aus Ordner "Gelöschte Elemente"  <br/> |SoftDelete  <br/> |
    |Berechtigungen für Ordner HinzugeFügt  <br/> |UpdateFolderPermissions  <br/> |
    |Geänderte Ordnerberechtigungen  <br/> |UpdateFolderPermissions  <br/> |
    |Berechtigungen aus Ordner entfernt  <br/> |UpdateFolderPermissions  <br/> |
    |Benutzer mit Stellvertreterzugriff auf Kalenderordner HinzugeFügt oder entfernt  <br/> |UpdateCalendarDelegation  <br/> |
   
    Beachten Sie, **** dass die im vorherigen Screenshot gezeigten Aktivitäten für Stellvertretungs-Postfachberechtigungen und **entfernte Stell Vertretungs Berechtigungen** nicht im Zusammenhang mit Post Fach Überwachungsaktionen stehen. Sie geben an, ob ein Administrator die FullAccess-Post Fach Berechtigung zugewiesen oder entfernt hat. 
    
    Informationen zum Office 365-Überwachungsprotokoll finden Sie unter [Durchsuchen des Überwachungsprotokolls im office 365 Security &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).
    
- Nur in den folgenden Szenarien wird ein Postfachzugriff als Administratorzugriff erachtet:
    
  - In-Place eDiscovery in Exchange Online oder Inhaltssuche in Office 365 wird zum Durchsuchen eines Postfachs verwendet.
    
  - [Microsoft Exchange Server MAPI Editor](https://go.microsoft.com/fwlink/p/?linkId=204086) wird für den Zugriff auf das Postfach verwendet. 
    
- Wenn Sie die Überwachungsprotokollierung für ein Postfach aktivieren, können Sie auch angeben, welche Benutzeraktionen (beispielsweise Zugriff auf eine Nachricht, Verschieben oder Löschen einer Nachricht) für einen Anmeldetyp (Administrator, Stellvertreter oder Besitzer) protokolliert werden. 
    
- Verwenden Sie den folgenden Befehl, um die Postfachüberwachungsprotokollierung zu deaktivieren:

  ```
  Set-Mailbox -Identity <identity of mailbox> -AuditEnabled $false
   ```

- Die für jeden Benutzertyp überwachten Aktionen werden nicht angezeigt, wenn Sie das Cmdlet **Get-Mailbox** ausführen. Sie können jedoch die folgenden Befehle ausführen, um alle überwachten Aktionen für einen bestimmten Benutzer Anmeldetyp anzuzeigen. 

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditAdmin
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditDelegate
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditOwner
    ```

- Sie können auch ein postfachüberwachungsprotokoll exportieren und die Einträge angeben, die für einen oder mehrere Benutzer eingeschlossen werden sollen. Jeder Eintrag im Bericht und das Überwachungsprotokoll enthalten Informationen dazu, wer die Aktion ausgeführt hat und wann, welche Aktion ausgeführt wurde und ob die Aktion erfolgreich war. Weitere Informationen finden Sie unter [Exportieren von postfachüberwachungsprotokollen](https://go.microsoft.com/fwlink/p/?LinkID=404104).
