---
title: Aktivieren der Postfachüberwachung in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: In Office 365 können Sie Protokollierung zum Protokollieren von Postfachzugriff durch Postfachbesitzer, Stellvertretungen und Administratoren Postfach aktivieren. Standardmäßig ist nicht Überwachung von Postfächern in Office 365 aktiviert. Nachdem Sie die postfachüberwachungsprotokollierung für ein Postfach aktiviert haben, können Sie das Office 365-Überwachungsprotokoll für Aktivitäten, die ausgeführt werden, für das Postfach suchen.
ms.openlocfilehash: 6d3de226e7c0e03be824b14e1b16fadaae3f040e
ms.sourcegitcommit: 8294182d4dd124f035a221de0b90159ef7eec4ae
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/19/2018
ms.locfileid: "25639664"
---
# <a name="enable-mailbox-auditing-in-office-365"></a>Aktivieren der Postfachüberwachung in Office 365
  
In Office 365 können Sie Protokollierung zum Protokollieren von Postfachzugriff durch Postfachbesitzer, Stellvertretungen und Administratoren Postfach aktivieren. Standardmäßig ist nicht Überwachung von Postfächern in Office 365 aktiviert. Dies bedeutet, dass die Überwachungsereignisse Postfach nicht in den Ergebnissen angezeigt, wenn Sie das Office 365-Überwachungsprotokoll für Mailbox-Aktivität durchsuchen. Aber wenn postfachüberwachungsprotokollierung für ein Benutzerpostfach aktiviert ist, können Sie das Überwachungsprotokoll Postfach Aktivität suchen. Darüber hinaus bei der Überwachung Postfach Protokollierung aktiviert ist, einige Aktionen, die von Administratoren, Stellvertretungen, und Besitzer werden standardmäßig protokolliert. Melden Sie sich (und suchen Sie nach) Weitere Aktionen finden Sie unter Schritt 3.

## <a name="before-you-begin"></a>Vorbemerkung
  
- Sie müssen Exchange Online PowerShell verwenden, um Postfach zu aktivieren postfachüberwachungsprotokollierung. Sie können die Office 365-Sicherheit nicht verwenden &amp; Compliance Center oder die Exchange-Verwaltungskonsole.
    
- Sie können nicht aktiviert werden postfachüberwachungsprotokollierung für das Postfach, das ein Office 365-Gruppe oder ein Team in Microsoft-Teams zugeordnet ist.
    
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

Nachdem Sie sich mit Ihrer Exchange Online-Organisation verbunden, mithilfe von PowerShell um postfachüberwachungsprotokollierung für ein Postfach zu aktivieren. Alternativ können Sie die Überwachung von Postfächern für alle Postfächer in Ihrer Organisation.
  
Dieses Beispiel aktiviert die postfachüberwachungsprotokollierung für Pilar Pinilla Postfach.
  
```
Set-Mailbox -Identity "Pilar Pinilla" -AuditEnabled $true
```

Dieses Beispiel aktiviert die Überwachungsprotokollierung für alle Postfächer in Ihrer Organisation.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -AuditEnabled $true
```
  
## <a name="step-3-specify-owner-actions-to-audit"></a>Schritt 3: Festlegen der zu überwachenden Aktionen des Postfachbesitzers

Wenn Sie die Überwachung für ein Postfach aktivieren, werden einige der Postfachbesitzer durchgeführten Aktionen standardmäßig überwacht. Sie müssen andere Aktionen von zu überwachenden angeben. Finden Sie in der Tabelle im Abschnitt [Überwachung Postfach-Aktionen](#mailbox-auditing-actions) für eine Liste und eine Beschreibung der Aktionen, die standardmäßig angemeldet sind und den anderen Aktionen, die überwacht werden können. 
  
In diesem Beispiel wird die postfachüberwachung für das Postfach von Pilar Pinilla die Aktionen von **MailboxLogin** und **HardDelete** hinzugefügt. In diesem Beispiel wird davon ausgegangen, dass die Überwachung von Postfächern bereits für dieses Postfach aktiviert wurde. 

```
Set-Mailbox "Pilar Pinilla" -AuditOwner @{Add="MailboxLogin","HardDelete"}
```

Dieses Beispiel aktiviert die postfachüberwachungsprotokollierung für das Postfach von Don Hall sowie gibt an, dass nur die von der Postfachbesitzer ausgeführte **MailboxLogin** Aktion protokolliert werden. Beachten Sie, dass in diesem Beispiel wird die Standardaktion UpdateFolderPermissions überschreibt. 
  
```
Set-Mailbox "Don Hall" -AuditEnabled $true -AuditOwner MailboxLogin
```
   
In diesem Beispiel werden alle Postfächer in der Organisation die Aktionen von **MailboxLogin**, **HardDelete**und **SoftDelete** hinzugefügt. In diesem Beispiel wird davon ausgegangen, dass die Überwachung von Postfächern für alle Postfächer bereits aktiviert wurde. 
  
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
   
Der Wert **True** für die Eigenschaft **AuditEnabled** überprüft, ob dieses Postfach Audit-Protokollierung ist aktiviert. 
    
## <a name="mailbox-auditing-actions"></a>Postfach auditing Aktionen
  
In der folgenden Tabelle sind die Aktionen aufgelistet, die vom Postfach protokolliert werden können postfachüberwachungsprotokollierung. Die Tabelle enthält, welche Aktion für die anderen Benutzer Anmeldetypen protokolliert werden kann. In der Tabelle gibt **No** , dass eine Aktion kann nicht für diese Anmeldetyp protokolliert werden. Ein Sternchen ( **\*** ) gibt an, dass die Aktion standardmäßig protokolliert wird, wenn die postfachüberwachungsprotokollierung für das Postfach aktiviert ist. 
  
|**Aktion**|**Beschreibung**|**Administrator**|**Stellvertretung\*\*\***|**Besitzer**|
|:-----|:-----|:-----|:-----|:-----|
|**Kopieren** <br/> |Eine Nachricht wurde in einen anderen Ordner kopiert.  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|**Erstellen** <br/> |Ein Element wird in den Ordner Kalender, Kontakte, Notizen oder Aufgaben im Postfach erstellt. Beispielsweise wird eine neue Besprechungsanfrage erstellt. Beachten Sie, dass das Erstellen, senden oder Empfangen einer Nachricht wird nicht überwacht. Erstellen einen Postfachordner wird auch nicht überwacht.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**"Folderbind"** <br/> |Auf einen Postfachordner wurde zugegriffen. Diese Aktion wird auch protokolliert, wenn der Administrator oder der delegierte Benutzer das Postfach öffnet.  <br/> |Ja  <br/> |Ja\*\*  <br/> |Nr.  <br/> |
|**HardDelete** <br/> |Eine Nachricht wurde endgültig aus dem Ordner "Wiederherstellbare Elemente" gelöscht.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**MailboxLogin** <br/> |Der Benutzer hat sich bei seinem Postfach angemeldet.  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|**"Messagebind"** <br/> |Eine Nachricht wurde im Vorschaufenster angezeigt oder geöffnet.  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|**Verschieben** <br/> |Eine Nachricht wurde in einen anderen Ordner verschoben.  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|**MoveToDeletedItems** <br/> |Eine Nachricht wurde gelöscht und in den Ordner „Gelöschte Objekte“ verschoben.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**"SendAs"** <br/> |Eine Nachricht wurde mithilfe der SendAs-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht so gesendet hat, dass sie vom Postfachbesitzer zu kommen scheint.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Nein  <br/> |
|**Sendonbehalf werden standardmäßig** <br/> |Eine Nachricht wurde mithilfe der SendOnBehalf-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht im Namen des Postfachbesitzers gesendet hat. Für den Empfänger ist in der Nachricht angegeben, in wessen Namen die Nachricht gesendet wurde und wer die Nachricht tatsächlich gesendet hat.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Nein  <br/> |
|**SoftDelete** <br/> |Eine Nachricht wurde dauerhaft gelöscht oder aus dem Ordner „Gelöschte Objekte“ gelöscht. Vorübergehend gelöschte Elemente werden in den Ordner „Wiederherstellbare Elemente“ verschoben.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**Aktualisieren** <br/> |Eine Nachricht oder deren Eigenschaften wurden geändert.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**UpdateCalendarDelegation** <br/> |Eine kalenderdelegierung wurde eines Postfachs zugewiesen. Kalenderdelegierung ermöglicht eine andere Person in der gleichen Organisationsberechtigungen zum Verwalten des Postfachbesitzers Kalenders.  <br/> |Ja\*  <br/> |Nein  <br/> |Ja\*  <br/> |
|**UpdateFolderPermissions** <br/> |Eine Ordnerberechtigung wurde geändert. Ordner Berechtigungen-steuern, welche Benutzer in Ihrer Organisation Ordner in einem Postfach und die Nachrichten befindet sich in den Ordnern zugreifen können.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
|**UpdateInboxRules** <br/> |Eine Posteingangsregel wurde hinzugefügt, entfernt oder geändert. Posteingangsregeln dienen zum Verarbeiten von Nachrichten im Posteingang des Benutzers basierend auf den angegebenen Bedingungen und Aktionen, wenn die Bedingung einer Regel erfüllt sind, wie eine Nachricht in einen bestimmten Ordner verschieben oder Löschen einer Nachricht.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Wird standardmäßig überwacht, wenn die Überwachung für ein Postfach aktiviert ist.<br/><br/>  <sup>\*\*</sup>Einträge für Ordner binden Aktionen, die von Stellvertretern werden konsolidiert. Für den Zugriff auf einzelne Ordner innerhalb des Zeitraums von 24 Stunden wird ein Protokolleintrag generiert.<br/><br/><sup>\*\*\*</sup>Ein Administrator die Berechtigung "Vollzugriff" des Postfachs eines Benutzers zugewiesen wurde, wird ein Stellvertreter betrachtet. 
  
Wenn Sie bestimmte Arten von zu überwachenden Postfach Aktionen nicht mehr benötigen, sollten Sie das Postfach Protokollierung Überwachungskonfiguration, um diese Aktionen deaktivieren ändern. Vorhandene Protokolleinträge werden nicht gelöscht, bis das Aufbewahrungslimit nach Überwachungsprotokolleinträgen erreicht wird. Weitere Informationen zu den Aufbewahrungszeitraum für Überwachungsprotokolleinträge finden Sie im Abschnitt "bevor Sie beginnen", bei der [Suche der Überwachungsprotokolle melden Sie sich bei der Office 365-Sicherheit und Compliance Center](search-the-audit-log-in-security-and-compliance.md#before-you-begin).
  
## <a name="more-infotab"></a>[Weitere Informationen](#tab/)
  
- Verwenden Sie das Überwachungsprotokoll für Office 365 für die Suche nach Postfach-Aktivität, die protokolliert wurden. Sie können für die Aktivität für das Postfach von einem bestimmten Benutzer suchen. Der folgende Screenshot zeigt eine Liste der Postfach-Aktivitäten, die Sie in das Überwachungsprotokoll Office 365 suchen können. Beachten Sie, dass diese Aktivitäten dieselben Aktionen, die im Abschnitt "Überwachung von Postfächern Aktionen" in diesem Thema beschrieben werden.
    
    ![Sie können das Office 365-Überwachungsprotokoll für Mailbox Audit Aktionen suchen, indem Sie in der Dropdownliste der Aktivitäten auswählen "Exchange-Postfach Aktivitäten"](media/fadc34f8-9de2-4688-8b1a-bc5540e69a23.png)
  
    In der folgenden Tabelle wird jede Aktivität Postfach, dass nach suchen und zeigt die entsprechende Aktion postfachüberwachung beschrieben.
    
    |**Aktivitäten im Überwachungsprotokoll**|**Postfach-Überwachung-Aktion**|
    |:-----|:-----|
    |Erstellte Postfach-Element  <br/> |Erstellen  <br/> |
    |Die kopierten Nachrichten in einen anderen Ordner  <br/> |Kopieren  <br/> |
    |Benutzer, die im Postfach angemeldet  <br/> |MailboxLogin  <br/> |
    |Nachricht gesendet Senden im Auftrag von Berechtigungen  <br/> |Sendonbehalf werden standardmäßig  <br/> |
    |Gelöschten Nachrichten aus dem Postfach  <br/> |HardDelete  <br/> |
    |Nachrichten in Ordner Gelöschte Elemente verschoben  <br/> |MoveToDeletedItems  <br/> |
    |Nachrichten in einen anderen Ordner verschoben  <br/> |Verschieben  <br/> |
    |Gesendete Nachricht mit der Berechtigung Senden als  <br/> |"SendAs"  <br/> |
    |Aktualisierte Nachricht  <br/> |Aktualisieren  <br/> |
    |Gelöschte Nachrichten aus dem Ordner Gelöschte Elemente  <br/> |SoftDelete  <br/> |
    |Zusätzliche Berechtigungen für Ordner  <br/> |UpdateFolderPermissions  <br/> |
    |Geänderte Berechtigungen des Ordners  <br/> |UpdateFolderPermissions  <br/> |
    |Entfernte Berechtigungen aus Ordner  <br/> |UpdateFolderPermissions  <br/> |
    |Hinzugefügt oder entfernt wurden Benutzer mit Delegieren des Zugriffs auf Kalenderordner  <br/> |UpdateCalendarDelegation  <br/> |
   
    Beachten Sie, dass die **Hinzufügung Stellvertretungsberechtigungen Postfach** und **entfernt Stellvertretungsberechtigungen Postfach** Aktivitäten, die dem vorherigen Screenshot mit postfachüberwachung Aktionen verknüpft sind. Sie geben an, ob ein Administrator zugewiesen oder die Berechtigung FullAccess Postfach entfernt. 
    
    Informationen über das Office 365-Überwachungsprotokoll finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).
    
- Nur in den folgenden Szenarien wird ein Postfachzugriff als Administratorzugriff erachtet:
    
  - Compliance-eDiscovery in Exchange Online oder Inhaltssuche in Office 365 wird zum Durchsuchen eines Postfachs verwendet.
    
  - [Microsoft Exchange Server MAPI Editor](https://go.microsoft.com/fwlink/p/?linkId=204086) wird für den Zugriff auf das Postfach verwendet. 
    
- Wenn Sie die Überwachungsprotokollierung für ein Postfach aktivieren, können Sie auch angeben, welche Benutzeraktionen (beispielsweise Zugriff auf eine Nachricht, Verschieben oder Löschen einer Nachricht) für einen Anmeldetyp (Administrator, Stellvertreter oder Besitzer) protokolliert werden. 
    
- Verwenden Sie den folgenden Befehl, um die Postfachüberwachungsprotokollierung zu deaktivieren:

  ```
  Set-Mailbox -Identity <identity of mailbox> -AuditEnabled $false
   ```

- Die Aktionen, die für jeden Typ von Benutzer überwacht werden werden nicht angezeigt, wenn Sie das **Get-Mailbox** -Cmdlet ausführen. Jedoch können Sie die folgenden Befehle zum Anzeigen der überwachten Aktionen für einen bestimmten Benutzer anmelden aus. 

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditAdmin
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditDelegate
    ```

    ```
    Get-Mailbox <identity of mailbox> | Select-Object -ExpandProperty AuditOwner
    ```

- Außerdem können Sie exportieren ein postfachüberwachungsprotokolls und geben Sie die Einträge für einen oder mehrere Benutzer einschließen. Jeder Eintrag in den Bericht und das Überwachungsprotokoll enthält Informationen, die die Aktion ausgeführt, und wenn die Aktion ausgeführt und, ob die Aktion erfolgreich war. Weitere Informationen finden Sie unter [postfachüberwachungsprotokolle exportieren](https://go.microsoft.com/fwlink/p/?LinkID=404104).
