---
title: Verwalten der Postfächern
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: aaca8987-5b62-458b-9882-c28476a66918
description: Die postfachüberwachungsprotokollierung ist standardmäßig in Microsoft 365 (auch als standardmäßige postfachüberwachung oder postfachüberwachung aktiviert) aktiviert. Dies führt dazu, dass bestimmte Aktionen, die von Postfachbesitzern, Stellvertretungen und Administratoren ausgeführt werden, automatisch in einem postfachüberwachungsprotokoll protokolliert werden, in dem Sie nach Aktivitäten suchen können, die für das Postfach ausgeführt werden.
ms.openlocfilehash: 38632798aedfa34ee7568a7038d5ff906888619c
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256983"
---
# <a name="manage-mailbox-auditing"></a>Verwalten der Postfächern
  
Ab Januar 2019 aktiviert Microsoft die postfachüberwachungsprotokollierung standardmäßig für alle Microsoft 365-Organisationen. Dies führt dazu, dass bestimmte Aktionen, die von Postfachbesitzern, Stellvertretern und Administratoren ausgeführt werden, automatisch protokolliert werden, und die entsprechenden Post Fach Überwachungseinträge stehen zur Verfügung, wenn Sie im postfachüberwachungsprotokoll nach diesen suchen. Bevor die postfachüberwachung standardmäßig aktiviert wurde, muss Sie für jedes Benutzerpostfach in Ihrer Organisation manuell aktiviert werden. 

Hier sind einige Vorteile der postfachüberwachung standardmäßig aktiviert:

- Die Überwachung wird standardmäßig aktiviert, wenn Sie ein neues Postfach erstellen. Sie müssen Sie nicht manuell für neue Benutzer aktivieren. 

- Sie können die überwachten Postfachaktionen nicht verwalten. Ein definierter Satz von Postfachaktionen wird standardmäßig für jeden Anmeldetyp überwacht. Diese [Anmeldetypen](#mailbox-actions-logged-by-default) sind Besitzer, Stellvertreter und Administrator.

- Neue von Microsoft freigegebene Postfachaktionen werden standardmäßig überwacht. Wenn Microsoft eine neue Post Fach Aktion veröffentlicht (insbesondere solche, die zum Schutz Ihrer Organisation und zur Hilfe bei forensischen Untersuchungen beitragen), wird Sie automatisch der Liste der standardmäßig überwachten Postfachaktionen hinzugefügt. Dies führt dazu, dass Sie der Liste der Postfachaktionen, die von Besitzern, Stellvertretern oder Administratoren ausgeführt werden, keine neuen Aktionen hinzufügen müssen. 

- Stellen Sie sicher, dass Sie die gleichen Aktionen für alle Postfächerüber wachen, damit Sie über eine konsistente Post Fach Überwachungsrichtlinie für Ihre Organisation verfügen.

> [!TIP]
> Beachten Sie, dass Sie bei der Freigabe der postfachüberwachung standardmäßig keine weiteren Schritte zur Verwaltung der postfachüberwachung ausführen müssen. Wenn Sie jedoch weitere Informationen wünschen, ändern Sie das Verhalten von den Standardeinstellungen, oder deaktivieren Sie es insgesamt, dieser Artikel kann Ihnen dabei helfen.

## <a name="verify-mailbox-auditing-on-by-default-is-turned-on"></a>ÜberPrüfen, ob die postfachüberwachung standardmäßig aktiviert ist

Führen Sie in [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell)den folgenden Befehl aus, um zu überprüfen, ob die postfachüberwachung standardmäßig für Ihre Organisation aktiviert ist:

```
Get-OrganizationConfig | FL AuditDisabled
``` 

Der Wert **false** gibt an, dass die postfachüberwachung standardmäßig für Ihre Organisation aktiviert ist. 

Wenn die postfachüberwachung standardmäßig aktiviert ist (wenn die *AuditDisabled* -Eigenschaft auf **false**festgelegt ist), überschreibt die Einstellung für die Organisation die Einstellung für die postfachüberwachung für ein bestimmtes Postfach. Wenn beispielsweise die *AuditEnabled* -Eigenschaft für ein Postfach auf **false**festgelegt ist, die postfachüberwachung aber standardmäßig für Ihre Organisation aktiviert ist, werden die standardmäßigen Postfachaktionen für dieses Postfach überwacht. Wenn die postfachüberwachung für ein bestimmtes Postfach explizit deaktiviert wurde und Sie dennoch deaktiviert werden soll, können Sie die postfachüberwachung für den Postfachbesitzer und andere Benutzer, denen der Zugriff auf das Postfach delegiert wurde, einrichten. Weitere Informationen finden Sie im Abschnitt [umgehen der postfachüberwachungsprotokollierung](#bypass-mailbox-audit-logging) in diesem Artikel.

> [!NOTE]
> Wenn die postfachüberwachung standardmäßig aktiviert ist, wird die *AuditEnabled* -Eigenschaft für ein Postfach nicht in **true** geändert, wenn Sie aktuell auf **false**festgelegt wurde. Anders ausgedrückt, wird die *AuditEnabled* -Eigenschaft für ein Postfach von der postfachüberwachung standardmäßig ignoriert.

## <a name="supported-mailbox-types"></a>Unterstützte Postfachtypen

In der folgenden Tabelle sind die Postfachtypen aufgeführt, die von der postfachüberwachung derzeit standardmäßig unterstützt werden:

|Postfachtyp|Unterstützt|Nicht unterstützt|
|:---------|:---------:|:---------:|
|Benutzerpostfächer    |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)       |         |
|Freigegebene Postfächer    |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)        |       |
|Office 365-Gruppen Postfächer    |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)         |         |
|Ressourcenpostfächer    |      |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)        |
|Postfächer für öffentliche Ordner    |       |![Häkchen](media/f3b4c351-17d9-42d9-8540-e48e01779b31.png)  |
||||

## <a name="mailbox-actions-logged-by-default"></a>Standardmäßig protokollierte Postfachaktionen

Für jeden der folgenden Anmeldetypen werden standardmäßig eine Reihe von Postfachaktionen protokolliert:  

   - **Owner** – der Postfachbesitzer. 
   
   - **Delegate** – ein anderer Benutzer, dem die Berechtigung "Sends", "SendOnBehalf" oder "FullAccess" für das Postfach einer Person zugewiesen wurde. Beachten Sie, dass ein Administrator, dem die FullAccess-Berechtigung für das Postfach eines Benutzers zugewiesen wurde, auch als Stellvertreter-Benutzer betrachtet wird.
   
    - Auf **Administrator** Postfächer wird nur in den folgenden Szenarien von einem Administrator Anmeldetyp zugegriffen:
    
       - Wenn ein Postfach mit einem der folgenden Microsoft eDiscovery-Tools durchsucht wird: 

         - Inhaltssuche im Compliance Center.
       
         -  eDiscovery oder Advanced eDiscovery im Compliance Center.
       
         - In-Place eDiscovery in Exchange Online.
       - Wenn der [Microsoft Exchange Server-MAPI-Editor](https://go.microsoft.com/fwlink/p/?linkId=204086) für den Zugriff auf das Postfach verwendet wird.     

In der folgenden Tabelle sind die Postfachaktionen aufgeführt, die derzeit standardmäßig für jeden Anmeldetyp protokolliert werden.

|Administratoraktionen|Stellvertretungs Aktionen|Besitzer Aktionen|
|:---------|:---------|:---------|
|Erstellen    |Erstellen       | HardDelete        |
|HardDelete    |HardDelete        |MoveToDeletedItems       |
|MoveToDeletedItems    |MoveToDeletedItems         |SoftDelete         |
|SendAs    |SendAs      |    Aktualisieren     |
|SendOnBehalf    |SendOnBehalf       |UpdateCalendarDelegation        |
|SoftDelete     |SoftDelete      | UpdateFolderPermissions        |
|Aktualisieren    |Aktualisieren       |UpdateInboxRules         |
|UpdateCalendarDelegation    | UpdateFolderPermissions        |         |
|UpdateFolderPermissions     | UpdateInboxRules        |         |
|UpdateInboxRules     |         |         |
||||

Hier finden Sie Beschreibungen dieser Postfachaktionen. 

|Postfach-Aktion|Beschreibung|
|:---------|:---------|
|**Create** <br/> |Ein Element wurde im Ordner Kalender, Kontakte, Notizen oder Aufgaben im Postfach erstellt. Beispielsweise wird eine neue Besprechungsanfrage erstellt. Beachten Sie, dass das Erstellen, senden oder Empfangen einer Nachricht nicht überwacht wird. Außerdem wird das Erstellen eines Postfachordners nicht überwacht.  <br/> |
|**HardDelete** <br/> |Eine Nachricht wurde endgültig aus dem Ordner "Wiederherstellbare Elemente" gelöscht.  <br/> |
|**MoveToDeletedItems** <br/> |Eine Nachricht wurde gelöscht und in den Ordner „Gelöschte Objekte“ verschoben.  <br/> |
|**SendAs** <br/> |Eine Nachricht wurde mithilfe der SendAs-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht so gesendet hat, dass sie vom Postfachbesitzer zu kommen scheint.  <br/> |
|**SendOnBehalf** <br/> |Eine Nachricht wurde mithilfe der SendOnBehalf-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht im Namen des Postfachbesitzers gesendet hat. Für den Empfänger ist in der Nachricht angegeben, in wessen Namen die Nachricht gesendet wurde und wer die Nachricht tatsächlich gesendet hat.  <br/> |
|**SoftDelete** <br/> |Eine Nachricht wurde dauerhaft gelöscht oder aus dem Ordner „Gelöschte Objekte“ gelöscht. Vorübergehend gelöschte Elemente werden in den Ordner „Wiederherstellbare Elemente“ verschoben.  <br/> |
|**Update** <br/> |Eine Nachricht oder deren Eigenschaften wurden geändert.  <br/> |
|**UpdateCalendarDelegation** <br/> |Einem Postfach wurde eine Kalender Delegierung zugewiesen. Die Kalender Delegierung erteilt anderen Benutzern in derselben Organisation Berechtigungen zum Verwalten des Kalenders des Postfachbesitzers.  <br/> |
|**UpdateFolderPermissions** <br/> |Eine Ordnerberechtigung wurde geändert. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Ordner in einem Postfach und die Nachrichten zugreifen können, die sich in diesen Ordnern befinden.  <br/> |
|**UpdateInboxRules** <br/> |Eine Posteingangsregel wurde hinzugefügt, entfernt oder geändert. PostEingangsregeln werden verwendet, um Nachrichten im Posteingang des Benutzers basierend auf den angegebenen Bedingungen zu verarbeiten und Aktionen auszuführen, wenn die Bedingungen einer Regel erfüllt sind, beispielsweise das Verschieben einer Nachricht in einen bestimmten Ordner oder das Löschen einer Nachricht.  <br/> |
|||

Eine vollständige Liste der Postfachaktionen, einschließlich der verfügbaren Aktionen, die jedoch nicht in den Standardaktionen enthalten sind, finden Sie im Abschnitt [Mailbox Auditing Actions](#mailbox-auditing-actions) in diesem Artikel.

> [!IMPORTANT]
> Wenn Sie die Postfachaktionen für einen beliebigen Anmeldetyp vor der postfachüberwachung standardmäßig für die Organisation aktiviert haben, wird die vorhandene Konfiguration für das Postfach Vorrang haben und vom Standardpostfach nicht überschrieben. in diesem Abschnitt beschriebenen Aktionen. Wenn Sie jederzeit zu den standardmäßigen Postfachaktionen zurückkehren möchten, können Sie den Befehl **Set-Mailbox-DefaultAuditSet** ausführen. Weitere Informationen hierzu finden Sie im Abschnitt [Wiederherstellen der standardmäßigen Postfachaktionen](#restore-the-default-mailbox-actions) in diesem Artikel.

### <a name="verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type"></a>Überprüfen, ob für jeden Anmeldetyp standardmäßige Postfachaktionen protokolliert werden

Bei der standardmäßigen Freigabe der postfachüberwachung wird eine neue Postfacheigenschaft mit dem Namen *DefaultAuditSet* hinzugefügt. Diese Eigenschaft gibt an, ob die standardmäßigen Postfachaktionen (von Microsoft verwaltet) für jeden Anmeldetyp für ein angegebenes Postfach überwacht werden. Sie können den folgenden Befehl ausführen, um die Werte dieser Eigenschaft anzuzeigen:

```
Get-Mailbox <username> | FL DefaultAuditSet
```

Ein Wert von `Admin, Delegate, Owner` gibt an, dass die standardmäßigen Postfachaktionen für alle drei Anmeldetypen überwacht werden und dass ein Administrator in Ihrer Organisation die Aktionen für einen beliebigen Anmeldetyp *nicht geändert hat* . Hinweis Dies ist der Standardzustand, nachdem die postfachüberwachung standardmäßig zunächst in Ihrer Organisation aktiviert wurde. 

Wenn ein Administrator in Ihrer Organisation die Postfachaktionen geändert hat, die für einen Anmeldetyp überwacht wurden (indem Sie das Cmdlet **Set-Mailbox** mit den Parametern *AuditAdmin*, *AuditDelegate*oder *AuditOwner* verwenden), wird der Wert für die *DefaultAuditSet* -Eigenschaft unterscheidet sich von dem Standardwert. Ein Wert von `Owner` gibt beispielsweise an, dass nur die standardmäßigen Postfachaktionen für den Postfachbesitzer überwacht werden und dass die Aktionen `Delegate` für `Admin` und geändert wurden. Wenn für die *DefaultAuditSet* -Eigenschaft keine Werte angezeigt werden (auch als *null* -Wert bezeichnet), wurden die Postfachaktionen für alle drei Anmeldetypen geändert.

Weitere Informationen zum Ändern der überwachten Postfachaktionen finden Sie unter [ändern oder Wiederherstellen von Postfachaktionen, die standardmäßig protokolliert](#change-or-restore-mailbox-actions-logged-by-default) wurden.

### <a name="display-a-list-of-mailbox-actions-logged-by-default"></a>Anzeigen einer Liste von Postfachaktionen, die standardmäßig protokolliert werden

Sie können die folgenden Befehle in Exchange Online PowerShell ausführen, um die Liste der Postfachaktionen anzuzeigen, die derzeit für ein Postfach für jeden Anmeldetyp gelten:

**Besitzer Aktionen**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditOwner
```

**Stellvertretungs Aktionen**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditDelegate
```

**Administratoraktionen**

```
Get-Mailbox <username> | Select-Object -ExpandProperty AuditAdmin
```

## <a name="change-or-restore-mailbox-actions-logged-by-default"></a>Standardmäßig protokollierte Postfachaktionen ändern oder wiederherstellen

Wie bereits erläutert, ist einer der Hauptvorteile der postfachüberwachung standardmäßig, dass Sie die überwachten Postfächer nicht verwalten müssen. Microsoft verwendet dies für Sie und fügt automatisch neue Postfachaktionen hinzu, die standardmäßig überwacht werden, wenn Sie freigegeben werden. Ihre Organisation kann jedoch Gründe haben, eine Reihe von Postfachaktionen zu überwachen, die sich von den Standardeinstellungen unterscheiden. In diesem Abschnitt wird gezeigt, wie Sie die für jeden Anmeldetyp überwachten Postfachaktionen ändern und wie Sie die Standardaktionen von Microsoft zurücksetzen.

> [!IMPORTANT]
> Wenn Sie Änderungen an den Postfachaktionen für einen Benutzer vornehmen, die standardmäßig protokolliert werden (wie im nächsten Abschnitt beschrieben), werden alle von Microsoft veröffentlichten neuen Postfachaktionen für diese Postfächer nicht überwacht. Sie müssen der Liste der Aktionen, die für einen Anmeldetyp überwacht werden, explizit eine neue Post Fach Aktion hinzufügen.

### <a name="change-the-mailbox-actions-to-audit"></a>Ändern der Postfachaktionen in "Überwachung"

Sie können das Cmdlet **Set-Mailbox** mit den Parametern *AuditAdmin*, *AuditDelegate*oder *AuditOwner* verwenden, um die überwachten Postfachaktionen je nach Anmeldetyp zu ändern. Da diese überwachungsbezogenen Parameter mehrwertige Parameter sind (d. h., Sie können mehr als einen Wert haben), gibt es zwei verschiedene Möglichkeiten, diese zu ändern.

- Mithilfe der folgenden Syntax können Sie mehrere Postfachaktionen angeben, die die vorhandenen Aktionen über `action1,action2,...actionN`schreiben:.

- Sie können eine oder mehrere Postfachaktionen hinzufügen oder entfernen, ohne vorhandene Datensätze zu beeinträchtigen, indem Sie `@{Add="action1","value2"}` die `@{Remove="action1","action2"}`folgende Syntax verwenden: oder.

Unabhängig davon, welche Methode Sie verwenden, um die überwachten Postfachaktionen zu ändern, werden die standardmäßig überwachten Postfachaktionen (für den geänderten Anmeldetyp) nicht mehr von Microsoft verwaltet. Darüber hinaus wird der Wert des Anmeldetyps, den Sie geändert haben, nicht im *DefaultAuditSet* -Post Fach Parameter angezeigt, der [zuvor beschrieben](#verify-that-default-mailbox-actions-are-being-logged-for-each-logon-type)wurde.

Im folgenden finden Sie einige Beispiele für die Verwendung einer der folgenden Methoden zum Ändern der Postfachaktionen, die für jeden der verschiedenen Anmeldetypen überwacht werden sollen. 

In diesem Beispiel werden die Aktionen des Admin-Postfachs durch Überschreiben der Standardaktionen mit SoftDelete und HardDelete geändert. 

```
Set-Mailbox <username> -AuditAdmin HardDelete,SoftDelete
```

In diesem Beispiel wird die Mailbox Login:-Besitzer Aktion hinzugefügt. 

```
Set-Mailbox <username> -AuditOwner @{Add="MailboxLogin"}
```

In diesem Beispiel wird die MoveToDeletedItems-Stellvertretungs Aktion entfernt.

```
Set-Mailbox <username> -AuditDelegate @{Remove="MoveToDeletedItems"}
```

#### <a name="checking-the-defaultauditset-property"></a>Überprüfen der DefaultAuditSet-Eigenschaft

Nachdem Sie die standardmäßigen Postfachaktionen für einen Anmeldetyp geändert haben, wird die *DefaultAuditSet* -Eigenschaft des Postfachs automatisch aktualisiert, um diese Änderung widerzuspiegeln. Wenn Sie beispielsweise nach dem `Get-Mailbox <username> | FL DefaultAuditSet` ersten Mal, wenn Sie eine Postfachbesitzer Aktion hinzufügen oder entfernen, ausführen, gibt der Befehl nur `Admin, Delegate`den Wert von zurück. Dies weist darauf hin, dass die standardmäßigen Postfachaktionen für den Besitzer geändert wurden, was bedeutet, dass alle von Microsoft veröffentlichten Aktionen für den Postfachbesitzer nicht automatisch zu diesem Postfach hinzugefügt werden. Dies gilt auch für das Ändern der Postfachaktionen für den Anmeldetyp "admin" oder "Delegate".

### <a name="restore-the-default-mailbox-actions"></a>Wiederherstellen der standardmäßigen Postfachaktionen

Wenn Sie Änderungen an den Postfachaktionen vorgenommen haben, die für einen Anmeldetyp überwacht wurden, können Sie die überwachten Standard Postfachaktionen wiederherstellen `Set-Mailbox -DefaultAuditSet` , indem Sie den Befehl ausführen. Wenn Sie dies tun, geschieht Folgendes:

- Die aktuelle Liste der Postfachaktionen wird durch die standardmäßigen Postfachaktionen für den entsprechenden Anmeldetyp ersetzt.
 
- Alle neuen Postfachaktionen, die von Microsoft veröffentlicht werden, werden automatisch der Liste für den entsprechenden Anmeldetyp hinzugefügt.

- Die [DefaultAuditSet-Postfacheigenschaft](#checking-the-defaultauditset-property) wird so aktualisiert, dass Sie den entsprechenden Anmeldetyp enthält.

Führen Sie den folgenden Befehl aus, um die standardmäßigen Postfachaktionen für alle Anmeldetypen wiederherzustellen:

```
Set-Mailbox <username> -DefaultAuditSet Admin,Delegate,Owner
```

Mit diesem Befehl können Sie die standardmäßigen Postfachaktionen für alle Anmeldetypen (mithilfe der Werte **Admin**, **Delegate**oder **Owner** für den Parameter *DefaultAuditSet* ) wiederherstellen.

## <a name="turn-off-mailbox-auditing-on-by-default-for-your-organization"></a>Deaktivieren Sie die postfachüberwachung standardmäßig für Ihre Organisation.

Wenn Ihre Organisation aus irgendeinem Grund entscheidet, dass Sie Postfachaktionen nicht überwachen soll, können Sie die postfachüberwachung standardmäßig für Ihre gesamte Organisation deaktivieren, indem Sie den folgenden Befehl in Exchange Online PowerShell ausführen:

```
Set-OrganizationConfig -AuditDisabled $true
```

Wenn die postfachüberwachung standardmäßig deaktiviert ist (die *AuditDisabled* -Eigenschaft ist auf **true**festgelegt), werden die folgenden Schritte ausgeführt:

- Die postfachüberwachung ist für Ihre Organisation deaktiviert.

- Es werden keine Postfachaktionen überwacht (ab dem Zeitpunkt, zu dem die Überwachung für die Organisation deaktiviert ist), auch wenn die *AuditEnabled* -Eigenschaft für ein Postfach auf **true**festgelegt ist.

- Die postfachüberwachung wird für neue Postfächer nicht aktiviert, und die *AuditEnabled* -Eigenschaft eines neuen (oder vorhandenen) Postfachs wird auf **true** festgelegt.

- Alle Einstellungen für die Zuordnung von Post Fach Überwachungs Umgehungen (konfiguriert mithilfe des Cmdlets **Set-MailboxAuditBypassAssociation** ) werden ignoriert.

- Vorhandene Post Fach Überwachungseinträge werden beibehalten, bis die Altersgrenze für das Überwachungsprotokoll für den Datensatz abgelaufen ist.

### <a name="turn-on-mailbox-auditing-on-by-default"></a>Aktivieren der postfachüberwachung standardmäßig

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um die postfachüberwachung wieder für Ihre Organisation zu aktivieren:

```
Set-OrganizationConfig -AuditDisabled $false
```

## <a name="bypass-mailbox-audit-logging"></a>Umgehen der postfachüberwachungsprotokollierung

Derzeit ist es nicht möglich, die postfachüberwachung für bestimmte Postfächer zu deaktivieren, wenn die postfachüberwachung standardmäßig in Ihrer Organisation aktiviert ist. Beispielsweise wird das Festlegen der *AuditEnabled* -Postfacheigenschaft auf **false** ignoriert.  Sie können jedoch das Cmdlet **Set-MailboxAuditBypassAssociation** in Exchange Online PowerShell verwenden, um zu verhindern, dass Postfachaktionen, die von bestimmten Benutzern ausgeführt werden, protokolliert werden. Wenn Sie die postfachüberwachung umgehen, werden die von einem bestimmten Benutzer ausgeführten Postfachaktionen nicht überwacht, unabhängig davon, in welchem Postfach diese Aktionen ausgeführt werden. Wenn Sie die postfachüberwachung für einen bestimmten Benutzer umgehen, werden die von diesem Benutzer durchgeführten Aktionen des Postfachbesitzers nicht protokolliert. Und wenn diesem Benutzerberechtigungen für das Postfach eines anderen Benutzers (oder ein freigegebenes Postfach) zugewiesen sind, werden auch die vom ersten Benutzer ausgeführten Stellvertretungs Aktionen nicht protokolliert.

Führen Sie den folgenden Befehl aus, um die postfachüberwachungsprotokollierung für einen bestimmten Benutzer zu umgehen:

```
Set-MailboxAuditBypassAssociation -Identity <username> -AuditByPassEnabled $true
```

Führen Sie den folgenden Befehl aus, um zu überprüfen, ob die Überwachung für den angegebenen Benutzer umgangen wird:

```
Get-MailboxAuditBypassAssociation -Identity <username> | FL AuditByPassEnabled
```

Der Wert **true** gibt an, dass die postfachüberwachungsprotokollierung für diesen Benutzer umgangen wird.

## <a name="mailbox-auditing-actions"></a>Aktionen für die postfachüberwachung
  
In der folgenden Tabelle werden die für die einzelnen Benutzeranmelde Typen überwachten Aktionen zusammengefasst. In der Tabelle gibt ein Sternchen ( **\*** ) an, dass die Aktion standardmäßig protokolliert wird. Ein **Nein** gibt an, dass für diesen Anmeldetyp keine Aktion protokolliert werden kann. Beachten Sie, dass ein Administrator, dem Vollzugriff für ein Benutzerpostfach gewährt wurde, als Stellvertreter gilt. 
  
|**Aktion**|**Beschreibung**|**Administrator**|**Stellvertretung**|**Besitzer**|
|:-----|:-----|:-----|:-----|:-----|
|**Kopieren** <br/> |Eine Nachricht wurde in einen anderen Ordner kopiert.  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|**Create** <br/> |Ein Element wird im Ordner Kalender, Kontakte, Notizen oder Aufgaben im Postfach erstellt. Beispielsweise wird eine neue Besprechungsanfrage erstellt. Beachten Sie, dass das Erstellen, senden oder Empfangen einer Nachricht nicht überwacht wird. Außerdem wird das Erstellen eines Postfachordners nicht überwacht.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja  <br/> |
|**FolderBind**\** <br/> |Auf einen Postfachordner wurde zugegriffen. Diese Aktion wird auch protokolliert, wenn der Administrator oder der delegierte Benutzer das Postfach öffnet.  <br/> |Ja  <br/> |Ja  <br/> |Nein  <br/> |
|**HardDelete** <br/> |Eine Nachricht wurde endgültig aus dem Ordner "Wiederherstellbare Elemente" gelöscht.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
|**Mailbox Login:** <br/> |Der Benutzer hat sich bei seinem Postfach angemeldet.  <br/> |Nein  <br/> |Nein  <br/> |Ja  <br/> |
|**MessageBind**\*** <br/> |Eine Nachricht wurde im Vorschaufenster angezeigt oder geöffnet.  <br/> |Ja  <br/> |Nein  <br/> |Nein  <br/> |
|**Verschieben** <br/> |Eine Nachricht wurde in einen anderen Ordner verschoben.  <br/> |Ja  <br/> |Ja  <br/> |Ja  <br/> |
|**MoveToDeletedItems** <br/> |Eine Nachricht wurde gelöscht und in den Ordner „Gelöschte Objekte“ verschoben.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
|**SendAs** <br/> |Eine Nachricht wurde mithilfe der SendAs-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht so gesendet hat, dass sie vom Postfachbesitzer zu kommen scheint.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Nein  <br/> |
|**SendOnBehalf** <br/> |Eine Nachricht wurde mithilfe der SendOnBehalf-Berechtigung gesendet. Das bedeutet, dass ein anderer Benutzer die Nachricht im Namen des Postfachbesitzers gesendet hat. Für den Empfänger ist in der Nachricht angegeben, in wessen Namen die Nachricht gesendet wurde und wer die Nachricht tatsächlich gesendet hat.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Nein  <br/> |
|**SoftDelete** <br/> |Eine Nachricht wurde dauerhaft gelöscht oder aus dem Ordner „Gelöschte Objekte“ gelöscht. Vorübergehend gelöschte Elemente werden in den Ordner „Wiederherstellbare Elemente“ verschoben.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
|**Update** <br/> |Eine Nachricht oder deren Eigenschaften wurden geändert.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
|**UpdateCalendarDelegation** <br/> |Einem Postfach wurde eine Kalender Delegierung zugewiesen. Die Kalender Delegierung erteilt anderen Benutzern in der Organisation die Berechtigung zum Verwalten des Kalenders des Postfachbesitzers.  <br/> |Ja\*  <br/> |Nein  <br/> |Ja\*  <br/> |
|**UpdateFolderPermissions** <br/> |Eine Ordnerberechtigung wurde geändert. Ordnerberechtigungen steuern, welche Benutzer in Ihrer Organisation auf Ordner in einem Postfach und die Nachrichten zugreifen können, die sich in diesen Ordnern befinden.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
|**UpdateInboxRules** <br/> |Eine Posteingangsregel wurde hinzugefügt, entfernt oder geändert. PostEingangsregeln werden verwendet, um Nachrichten im Posteingang des Benutzers basierend auf den angegebenen Bedingungen zu verarbeiten und Aktionen auszuführen, wenn die Bedingungen einer Regel erfüllt sind, beispielsweise das Verschieben einer Nachricht in einen bestimmten Ordner oder das Löschen einer Nachricht.  <br/> |Ja\*  <br/> |Ja\*  <br/> |Ja\*  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Wird standardmäßig überwacht, wenn die standardmäßige postfachüberwachung für den Anmeldetyp aktiviert ist. <br/><br/>  <sup>\*\*</sup>Überwachungsdatensätze für Ordner Bindungs Aktionen, die von Stellvertretern ausgeführt werden, werden konsolidiert. Ein Überwachungsdatensatz wird für den Zugriff einzelner Ordner innerhalb von 24 Stunden generiert. <br/><br/> Die MessageBind-Aktion ist in Exchange Online veraltet und kann nicht mehr zur Liste der Postfachaktionen für den Administrator Anmeldetyp hinzugefügt werden. <sup> \* \* \* </sup> 

## <a name="more-information"></a>Weitere Informationen

- Die postfachüberwachungsprotokoll Einträge werden standardmäßig für 90 Tage aufbewahrt und dann gelöscht. Sie können die Verfallszeit für Überwachungsprotokolldatensätze ändern, indem Sie den Befehl **Set-Mailbox-AuditLogAgeLimit** in Exchange Online PowerShell verwenden. Beachten Sie, dass die Erhöhung der standardmäßigen Verfallszeit für Post Fach Überwachungseinträge sich nicht auf die 90-Tage-Altersgrenze für postfachüberwachungsprotokoll Datensätze im Microsoft 365-Überwachungsprotokoll auswirkt. Wenn Sie beispielsweise die Verfallszeit für postfachüberwachungsprotokoll Datensätze auf 365 Tage verlängern, ist ein Post Fach Überwachungseintrag im Microsoft 365-Überwachungsprotokoll nur für 90 Tage nach dem entsprechenden Ereignis durchsuchbar. In diesem Fall müssen Sie das postfachüberwachungsprotokoll des Benutzers nach Datensätzen durchsuchen, die älter als 90 Tage sind. Weitere Informationen zum Durchsuchen von postfachüberwachungsprotokollen finden Sie unter [Search-Mailbox auditlog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-mailboxauditlog).

- Wenn Sie die *AuditLogAgeLimit* -Eigenschaft für ein Postfach geändert haben, bevor die postfachüberwachung standardmäßig für die Organisation aktiviert wird, wird der vorhandene Grenzwert für das Überwachungsprotokoll für dieses Postfach nicht geändert. in anderen Worten: die postfachüberwachung für die Post Fach Überwachungseinträge wird in der standardmäßigen Altersgrenze nicht aktiviert.

- Postfachüberwachungsprotokoll-Einträge werden in einem Unterordner **(mit dem Namen Audits) im Ordner "Wiederherstellbare Elemente" im Postfach der einzelnen Benutzer gespeichert. Beachten Sie die folgenden Aspekte in Bezug auf Post Fach Überwachungseinträge und den Ordner "Wiederherstellbare Elemente".
   
    - Post Fach Überwachungsdatensätze gelten für das Speicherkontingent des Ordners "Wiederherstellbare Elemente", der standardmäßig 30 GB lautet (das Kontingent für die Warnung beträgt 20 GBYTE). Beachten Sie, dass das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" automatisch von auf 100 GB (90 MB) erhöht wird, wenn ein Haltebereich für ein Postfach oder das Postfach einer Aufbewahrungsrichtlinie im Compliance Center zugewiesen ist.

    - Post Fach Überwachungsdatensätze gelten auch [für den Ordner Grenzwert für den Ordner "Wiederherstellbare Elemente](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-service-description/exchange-online-limits#mailbox-folder-limits)". Die maximale Anzahl von Elementen (in diesem Fall Überwachungsdatensätze), die im Unterordner "Überwachungen" gespeichert werden können, ist 3 Millionen Elemente. 

      > [!NOTE]
      > Es ist unwahrscheinlich, dass sich die postfachüberwachung standardmäßig auf das Speicherkontingent oder den Ordner Grenzwert für den Ordner "Wiederherstellbare Elemente" auswirkt. 

    - Sie können den folgenden Befehl in Exchange Online PowerShell ausführen, um die Größe und Anzahl der Elemente im Unterordner "Überwachungen" im Ordner "Wiederherstellbare Elemente" anzuzeigen: 
       ```
       Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | Where-Object {$_.Name -eq 'Audits'} | FL FolderPath,FolderSize,ItemsInFolder
       ```

     - Sie können nicht direkt auf einen Überwachungsprotokolleintrag im Ordner "Wiederherstellbare Elemente" zugreifen; Stattdessen verwenden Sie das Cmdlet **Search-Mailbox auditlog** oder durchsuchen das Überwachungsprotokoll von Microsoft 365, um Post Fach Überwachungseinträge zu finden und anzuzeigen.

- Wenn ein Postfach im Compliance Center gehalten oder einer Aufbewahrungsrichtlinie zugewiesen wird, werden Überwachungsprotokolleinträge weiterhin für die Dauer beibehalten, die von der *AuditLogAgeLimit* -Eigenschaft für das Postfach definiert wurde (standardmäßig auf 90 Tage festgelegt). Sie müssen den Aufbewahrungszeitraum verlängern, indem Sie den Wert für die *AuditLogAgeLimit* -Eigenschaft erhöhen, um die Überwachungsprotokolleinträge für die Warteschleife länger aufzubewahren.