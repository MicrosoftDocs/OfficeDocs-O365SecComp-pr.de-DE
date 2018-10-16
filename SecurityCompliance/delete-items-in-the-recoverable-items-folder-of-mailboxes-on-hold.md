---
title: Löschen von Elementen im Ordner "wiederherstellbare Elemente" des cloudbasierten Postfächer in der Warteschleife - Admin-Hilfe
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
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Für Administratoren: Löschen von Elementen in den Ordner eines Benutzers wiederherstellbare Elemente für ein Exchange Online-Postfach, auch wenn dieses Postfach rechtliche Aufbewahrungspflicht platziert wird. Dies ist eine effektive Möglichkeit zum Löschen von Daten, die in Office 365 versehentlich verschüttet ist.'
ms.openlocfilehash: 9174e953ebdd7f0032f411b99a814aeacd880a1e
ms.sourcegitcommit: dd58ed6fd424272e361bc3c109ecd6d63d673048
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/15/2018
ms.locfileid: "25566886"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a>Löschen von Elementen im Ordner "wiederherstellbare Elemente" des cloudbasierten Postfächer in der Warteschleife - Admin-Hilfe

"Wiederherstellbare Elemente" für ein Exchange Online-Postfach zum Schutz vor versehentlichen oder böswilligen Löschvorgängen vorhanden ist. Es wird auch verwendet zum Speichern von Elementen, die werden beibehalten und Office 365-Compliance-Features wie Haltestatus und eDiscovery-Suchvorgänge zugreifen. Jedoch möglicherweise Organisationen in manchen Fällen Daten haben, die versehentlich im Ordner "wiederherstellbare Elemente" beibehalten worden ist, die sie löschen müssen. Ein Benutzer kann beispielsweise unwissentlich senden oder Weiterleiten eine e-Mail-Nachricht, die enthält vertrauliche Informationen oder Informationen, die schwerwiegende Business Konsequenzen haben kann. Auch wenn die Nachricht dauerhaft gelöscht wird, kann es auf unbestimmte Zeit aufbewahrt werden, da eine rechtliche Aufbewahrungspflicht für das Postfach versetzt wurde. In diesem Szenario wird als Daten stellen bezeichnet, da Daten in Office 365 versehentlich verschüttet hat. In diesen Fällen können Sie Elemente in den Ordner eines Benutzers wiederherstellbare Elemente für ein Exchange Online-Postfach löschen, auch wenn dieses Postfach mit einer der anderen Warteschleife Features in Office 365 gehalten wird. Diese Arten von Haltestatus umfassen Rechtsstreitigkeiten enthält, Compliance-Archive, eDiscovery-Archive und Office 365-Aufbewahrungsrichtlinien erstellt in der Office 365-Sicherheit &amp; Compliance Center. 
  
 In diesem Artikel wird erläutert, wie Elemente aus dem Ordner wiederherstellbare Elemente für cloudbasierte Postfächer zu löschen, die in der Warteschleife sind. Bei diesem Verfahren werden deaktiviert den Zugriff auf das Postfach und Deaktivieren der Wiederherstellung einzelner Elemente, deaktivieren den Assistenten für verwaltete Ordner aus der Verarbeitung des Postfachs, vorübergehend den Haltestatus entfernen, Löschen von Elementen aus dem Ordner "wiederherstellbare Elemente" und anschließend wiederherstellen das Postfach auf die vorherige Konfiguration. Hier wird der Prozess: 
  
[Schritt 1: Sammeln von Informationen über das Postfach](#step-1-collect-information-about-the-mailbox)

[Schritt 2: Vorbereiten des Postfachs](#step-2-prepare-the-mailbox)

[Schritt 3: Entfernen Sie alle Haltestatus aus dem Postfach](#step-3-remove-all-holds-from-the-mailbox)

[Schritt 4: Entfernen Sie den Haltestatus Verzögerung aus dem Postfach](#step-4-remove-the-delay-hold-from-the-mailbox)

[Schritt 5: Löschen von Elementen im Ordner "wiederherstellbare Elemente"](#step-5-delete-items-in-the-recoverable-items-folder)

[Schritt 6: Das Postfach in den vorherigen Zustand zurücksetzen](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> Die Verfahren in diesem Artikel beschriebenen führt Daten dauerhaft gelöscht (gelöscht) von einem Exchange Online-Postfach. Das bedeutet, dass Nachrichten, die Sie aus dem Ordner wiederherstellbare Elemente löschen können nicht wiederhergestellt werden nicht für die Offenlegungspflicht oder sonstige Zwecke Compliance verfügbar. Wenn Sie möchten, um Nachrichten aus einem Postfach zu löschen, die als Teil einer Aufbewahrung für eventuelle Rechtsstreitigkeiten, Compliance-Archiv, in die Warteschleife gestellt wird eDiscovery halten oder Office 365 Aufbewahrungsrichtlinie erstellt, in die Office 365-Sicherheit &amp; Compliance Center, erkundigen Sie sich bei der Verwaltung von Datensätzen und Legal Abteilungen, bevor Sie den Haltestatus entfernen. Ihre Organisation möglicherweise eine Richtlinie, die definiert, ob ein Postfach auf halten oder ein Daten stellen Vorfall Vorrang. 
  
## <a name="before-you-begin"></a>Vorbemerkung

- Sie müssen beide der folgenden Verwaltungsrollen in Exchange Online suchen und Löschen von Nachrichten aus dem Ordner "wiederherstellbare Elemente" in Schritt 5 zugewiesen werden.
    
  - **Postfachsuche** – diese Rolle können Sie Postfächer in Ihrer Organisation zu suchen. Exchange-Administratoren sind nicht dieser Rolle standardmäßig zugewiesen. Wenn sich diese Rolle zuweisen möchten, tragen Sie sich als Mitglied der Rollengruppe "Discoveryverwaltung" im Exchange Online. 
    
  - **Postfach Import/Export** - dieser Rolle können Sie Nachrichten aus dem Postfach eines Benutzers zu löschen. Standardmäßig ist nicht dieser Rolle alle Rollengruppe zugewiesen. Um Nachrichten aus den Postfächern der Benutzer zu löschen, können Sie die Rolle Postfach Import/Export der Rollengruppe "Organisationsverwaltung" im Exchange Online hinzufügen. 
    
- In diesem Artikel beschriebene Verfahren wird für inaktive Postfächer nicht unterstützt. Das, da Sie eine Warteschleife (oder Office 365 Aufbewahrungsrichtlinie) erneut anwenden können nicht zu eines inaktiven Postfachs ist, nachdem Sie ihn entfernen. Wenn Sie eines inaktiven Postfachs einen Haltestatus aufheben, wird in einem normalen vorläufig gelöschten Postfach geändert und werden unwiederbringlich aus Ihrer Organisation gelöscht werden, nachdem er vom Assistenten für verwaltete Ordner verarbeitet wird.
    
- Dieses Verfahren für ein Postfach nicht möglich, die ein Office 365-Aufbewahrungsrichtlinie zugewiesen wurde, die mit einer Sperre permanentes gesperrt ist. Dies liegt daran eine Beibehaltung der Sperre verhindert, dass Sie zu entfernen oder ohne das Postfach aus der Office 365-Aufbewahrungsrichtlinie und den Assistenten für verwaltete Ordner für das Postfach zu deaktivieren. Weitere Informationen zu Aufbewahrungsrichtlinien Sperren finden Sie unter [Sperren einer Aufbewahrungsrichtlinie](retention-policies.md#locking-a-retention-policy).
    
- Wenn ein Postfach wird nicht in die Warteschleife gestellt (oder verfügt nicht über Wiederherstellung einzelner Elemente aktiviert), können Sie einfach die Elemente aus dem Ordner wiederherstellbare Elemente löschen. Weitere Informationen hierzu finden Sie unter [Suchen und Löschen von Nachrichten ](https://go.microsoft.com/fwlink/?linkid=852453).
  
## <a name="step-1-collect-information-about-the-mailbox"></a>Schritt 1: Sammeln von Informationen über das Postfach

Dieser erste Schritt besteht darin ausgewählte Eigenschaften aus dem Zielpostfach sammeln, die für dieses Verfahren gelten. Achten Sie darauf, notieren Sie sich diese Einstellungen oder da Sie einige dieser Eigenschaften ändern, und klicken Sie dann auf die ursprünglichen Werte in Schritt 6, zurückgesetzt, nach dem Löschen von Elementen aus dem Ordner wiederherstellbare Elemente in einer Textdatei speichern. Es folgt eine Liste mit den Postfacheigenschaften benötigten sammeln.
  
-  *SingleItemRecoveryEnabled* und *RetainDeletedItemsFor* ; Falls erforderlich, Sie einzelne Wiederherstellung deaktivieren und erhöhen die Aufbewahrungszeit von gelöschten Elemente in Schritt 3. 
    
-  *LitigationHoldEnabled* und *InPlaceHolds* ; Sie müssen alle Haltestatus, die für das Postfach platziert werden, sodass Sie sie in Schritt 3 vorübergehend entfernen können. Finden Sie [Weitere Informationen](delete-items-in-the-recoverable-items-folder-of-mailboxes-on-hold.md#moreinfo) im Abschnitt Tipps dazu, wie Sie den Typ Haltestatus zu identifizieren, der für ein Postfach platziert werden kann. 
    
Darüber hinaus müssen Sie das Postfach Clientzugriffseinstellungen abrufen, damit Sie vorübergehend deaktivieren, damit der Besitzer (oder andere Benutzer) während dieses Vorgangs Zugriff auf das Postfach ist nicht möglich. Schließlich können Sie die aktuelle Größe und Anzahl der Elemente im Ordner "wiederherstellbare Elemente" abrufen. Nachdem Sie Elemente im Ordner "wiederherstellbare Elemente" in Schritt 5 zu löschen, verwenden Sie diese Informationen, um sicherzustellen, dass Elemente tatsächlich entfernt wurden.
  
1. [Herstellen einer Verbindung mit Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Achten Sie darauf, dass Sie einen Benutzernamen und ein Kennwort für ein Administratorkonto verwenden, das die entsprechenden Verwaltungsrollen in Exchange Online zugewiesen wurde. 
    
2. Führen Sie den folgenden Befehl zum Abrufen von Informationen zur Wiederherstellung einzelner Elemente und die Aufbewahrungszeit für gelöschte Elemente.

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   Wenn die Wiederherstellung einzelner Elemente aktiviert ist, müssen Sie in Schritt2 zu deaktivieren. Wenn die Aufbewahrungszeit für gelöschte 30 Tage lang nicht festgelegt (der maximale Wert in Exchange Online), und klicken Sie dann in Schritt2 zu erhöhen. 
    
3. Führen Sie den folgenden Befehl aus, um das Postfach Access-Einstellungen für das Postfach abzurufen. 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   Sie müssen alle diese Zugriffsmethoden in Schritt2 deaktivieren.
    
4. Führen Sie den folgenden Befehl zum Abrufen von Informationen zu den Haltestatus und Office 365-Aufbewahrungsrichtlinien an das Postfach angewendet.
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > Wenn in der Eigenschaft *InPlaceHolds* zu viele Werte vorhanden sind, und nicht alle angezeigt werden, können Sie Ausführen der `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` Befehl aus, um jeden Wert in einer separaten Zeile angezeigt. 
  
5. Führen Sie den folgenden Befehl zum Abrufen von Informationen über alle organisationsweiten Office 365-Aufbewahrungsrichtlinien. 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   Wenn Ihre Organisation eine beliebige organisationsweiten Office 365-Aufbewahrungsrichtlinien verfügt, müssen Sie das Postfach aus dieser Richtlinien in Schritt 3 ausschließen.

   > [!TIP]
    > Wenn in der Eigenschaft *InPlaceHolds* zu viele Werte vorhanden sind, und nicht alle angezeigt werden, können Sie Ausführen der `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` Befehl aus, um jeden Wert in einer separaten Zeile angezeigt. 
  
6. Führen Sie den folgenden Befehl aus, um die aktuelle Größe und die Gesamtanzahl der Elemente in Ordner und Unterordner im Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers abzurufen. 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Wenn das Postfach des Benutzers Archiv aktiviert ist, führen Sie den folgenden Befehl zum Abrufen der Größe und der Gesamtzahl der Elemente in Ordner und Unterordner im Ordner "wiederherstellbare Elemente" in ihrem Postfach archivieren. 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Wenn Sie in Schritt 5 Elemente löschen, können Sie auswählen, zu löschen oder Elemente im Ordner "wiederherstellbare Elemente" im primären Archivpostfach des Benutzers nicht löschen. Beachten Sie, dass bei erweiterbares Archivierung für das Postfach aktiviert ist, wird nicht Elemente in einem Hilfs-Archivpostfach gelöscht.
  
## <a name="step-2-prepare-the-mailbox"></a>Schritt 2: Vorbereiten des Postfachs

Nach dem Erfassen und Speichern von Informationen über das Postfach, werden im nächste Schritt das Postfach vorbereiten, indem Sie die folgenden Aufgaben ausführen: 
  
- **Clientzugriff auf das Postfach zu deaktivieren** , damit der Postfachbesitzer Zugriff auf ihre Postfächer und ändern Sie die Postfachdaten während dieses Vorgangs ist nicht möglich. 
    
- **Erhöhen Sie die Aufbewahrungszeit für gelöschte** auf 30 Tage (Höchstwert in Exchange Online), sodass Elemente aus dem Ordner wiederherstellbare Elemente gelöscht werden nicht, bevor Sie sie in Schritt 5 löschen können. 
    
- (Für die Dauer der Aufbewahrungszeit für gelöschte) werden nicht so Elementen, **Deaktivieren Sie die Wiederherstellung einzelnen Elemente** aufbewahrt werden, nach dem Löschen aus dem Ordner "wiederherstellbare Elemente" in Schritt 5. 
    
- **Assistenten für verwaltete Ordner zu deaktivieren** , damit das alles nicht das Postfach zu verarbeiten und die Elemente, die Sie in Schritt 5 löschen beibehalten. 
    
Führen Sie die folgenden Schritte aus, in Exchange Online PowerShell.
  
1. Führen Sie den folgenden Befehl aus, um alle Clientzugriff auf das Postfach zu deaktivieren. Die Befehlssyntax wird davon ausgegangen, dass alle Methoden für den Clientzugriff auf das Postfach aktiviert wurden.

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > Es kann so deaktivieren Sie alle Methoden für den Clientzugriff an das Postfach von bis zu 60 Minuten dauern. Beachten Sie, dass diese Zugriffsmethoden deaktivieren den Postfachbesitzer Trennen wird nicht, den sie bereits angemeldet sind. Wenn der Besitzer angemeldet ist nicht, werden nicht diese werden auf ihre Postfächer zugreifen, nachdem diese Zugriffsmethoden deaktiviert werden können. 
  
2. Führen Sie den folgenden Befehl aus, um die Aufbewahrungszeit für gelöschte maximal 30 Tage zu erhöhen. Dabei wird vorausgesetzt, dass die aktuelle Einstellung weniger als 30 Tage ist. 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. Führen Sie den folgenden Befehl zum Deaktivieren der Wiederherstellung einzelner Elemente.
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > Es kann bis zu 60 Minuten Wiederherstellung einzelner Elemente deaktivieren dauern. Löschen von Elementen im Ordner "wiederherstellbare Elemente" nicht erst nach Ablauf dieses Zeitraums. 
  
4. Führen Sie den folgenden Befehl zum Assistenten für verwaltete Ordner verhindern, dass das Postfach zu verarbeiten. Wie bereits erklärt können Sie den Assistenten für verwaltete Ordner deaktivieren nur, wenn eine Aufbewahrungsrichtlinie Office 365 mit einer Sperre permanentes nicht auf das Postfach angewendet wird. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a>Schritt 3: Entfernen Sie alle Haltestatus aus dem Postfach

Der letzte Schritt, bevor Sie Elemente aus dem Ordner wiederherstellbare Elemente löschen können ist, entfernen alle Haltestatus (, die Sie in Schritt 1 identifiziert) für das Postfach platziert. Alle Haltestatus müssen entfernt werden, sodass Elemente wird nicht beibehalten werden, nachdem Sie diese aus dem Ordner wiederherstellbare Elemente löschen. Die folgenden Abschnitte enthalten Informationen zum Entfernen von verschiedenen Typen von Haltestatus für ein Postfach. Finden Sie [Weitere Informationen](#more-information) im Abschnitt Tipps dazu, wie Sie den Typ Haltestatus zu identifizieren, der für ein Postfach platziert werden kann. Weitere Informationen finden Sie unter [So identifizieren Sie den Typ des platziert eines Exchange Online-Postfachs halten](identify-a-hold-on-an-exchange-online-mailbox.md).
  
> [!CAUTION]
> Wie bereits zuvor erwähnt überprüfen Sie mit der datensatzverwaltung oder der rechtlichen Abteilungen vor einen Haltestatus aus einem Postfach entfernen. 
  
 ### <a name="litigation-hold"></a>Beweissicherungsverfahren
  
Führen Sie den folgenden Befehl in Exchange Online PowerShell, um eine Aufbewahrung für eventuelle Rechtsstreitigkeiten aus dem Postfach entfernt.

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> Ähnlich wie die Methoden für den Clientzugriff und die Wiederherstellung einzelner Elemente deaktivieren, kann es zum Entfernen der Aufbewahrung für eventuelle Rechtsstreitigkeiten bis zu 60 Minuten dauern. Löschen von Elementen nicht aus dem Ordner wiederherstellbare Elemente, bis dieser Zeitraum abgelaufen ist. 
  
 ### <a name="in-place-hold"></a>Compliance-Archiv
  
Führen Sie den folgenden Befehl in Exchange Online PowerShell, um die Compliance-Archivs zu ermitteln, die für das Postfach befindet. Verwenden Sie die GUID für die Compliance-Archivs, die Sie in Schritt 1 identifiziert. 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
Nachdem Sie die In-Place Hold identifiziert haben, können Sie die Exchange-Verwaltungskonsole (EAC) oder Exchange Online PowerShell verwenden, an um das Postfach aus dem Haltestatus zu entfernen. Weitere Informationen finden Sie unter [Create or Remove an In-Place Hold](https://go.microsoft.com/fwlink/?linkid=852668).
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a>Office 365 Aufbewahrungsrichtlinien auf bestimmte Postfächer angewendet
  
Führen den folgenden Befehl [Sicherheit in Office 365 &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) , die Office 365-Aufbewahrungsrichtlinie zu identifizieren, die auf das Postfach angewendet wird. Verwenden Sie die GUID (einschließlich nicht die `mbx` oder `skp` Präfix) für die Aufbewahrungsrichtlinie, die Sie in Schritt 1 identifiziert. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
Nachdem Sie die Aufbewahrungsrichtlinie identifiziert haben, wechseln Sie zu dem **Datum Governance** \> **Aufbewahrung** Seite in das Wertpapier &amp; Compliance Center, bearbeiten Sie die Aufbewahrungsrichtlinie, die Sie im vorherigen Schritt identifiziert haben, und entfernen Sie das Postfach aus der Liste der Empfänger, die in der Aufbewahrungsrichtlinie enthalten sind. 
  
 ### <a name="organization-wide-office-365-retention-policies"></a>Office 365-Aufbewahrungsrichtlinien organisationsweiten
  
Organisationsweite und Exchange-Wide Office 365-Aufbewahrungsrichtlinien gelten für alle Postfächer in der Organisation. Sie werden auf Organisationsebene (nicht die Postfachebene) angewendet und werden zurückgegeben, wenn Sie das Cmdlet **Get-OrganizationConfig** in Schritt 1 ausführen. Führen den folgenden Befehl [Sicherheit &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) zum Identifizieren der gesamten Organisation Office 365-Aufbewahrungsrichtlinien. Verwenden Sie die GUID (einschließlich nicht die `mbx` Präfix) für die Organisation geltende Aufbewahrungsrichtlinien, die Sie in Schritt 1 identifiziert. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

Nachdem Sie die gesamte Organisation Office 365-Aufbewahrungsrichtlinien identifiziert haben, wechseln Sie zu dem **Datum Governance** \> **Aufbewahrung** Seite in das Wertpapier &amp; Compliance Center bearbeiten für jede Organisation geltende Aufbewahrungsrichtlinie, die Sie in identifiziert die vorherigen Schritt, und fügen Sie das Postfach in die Liste der ausgeschlossenen Empfänger. Hierdurch wird das Postfach des Benutzers aus der Aufbewahrungsrichtlinie entfernt. 

### <a name="office-365-retention-labels"></a>Office 365 Aufbewahrung Etiketten

Wenn ein Benutzer eine Bezeichnung, die beibehalten werden Inhalte gilt oder beibehalten, und klicken Sie dann Löschen von Inhalt eines beliebigen Ordners oder Elements in ihrem Postfach konfiguriert ist, wird die *ComplianceTagHoldApplied* Postfach-Eigenschaft auf **True**festgelegt. In diesem Fall gilt das Postfach werden abwarten, so als würde gebracht Aufbewahrung für eventuelle Rechtsstreitigkeiten oder eine Aufbewahrungsrichtlinie für Office 365 zugewiesen wurde.

Wenn den Wert der Eigenschaft *ComplianceTagHoldApplied* anzeigen möchten, führen Sie den folgenden Befehl in Exchange Online PowerShell:

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Nachdem Sie festgestellt haben, dass ein Postfach auf ist gesperrt, da eine Beschriftung für die Aufbewahrung auf einen Ordner oder das Element angewendet wird, Sie das Tool für die Inhaltssuche in das Wertpapier können & Compliance Center zu suchenden mit der Bezeichnung Elemente mithilfe der ComplianceTag Suchbedingung. Weitere Informationen finden Sie im Abschnitt "Suchen Conditions" in [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md#conditions-for-common-properties).

Weitere Informationen zu Etiketten finden Sie unter [Übersicht über Office 365 Beschriftungen](labels.md).

 ### <a name="ediscovery-case-holds"></a>eDiscovery-Fall enthält
  
Führen die folgenden Befehle [Sicherheit &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) identifiziert den Haltestatus Zusammenhang mit einem eDiscovery-Fall, die an das Postfach angewendet wird. Verwenden Sie die GUID (einschließlich nicht die `UniH` Präfix) für die eDiscovery halten, dass Sie in Schritt 1 identifiziert haben. Beachten Sie, dass der zweite Befehl den Namen der eDiscovery-Fall anzeigt, die der Haltebereich zugeordnet ist. Der dritte Befehl zeigt den Namen des Haltestatus. 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

Nachdem Sie den Namen des eDiscovery-Fall und den Haltestatus identifiziert haben, wechseln Sie zu der **Suche &amp; Untersuchung** \> **eDiscovery** -Seite in das Wertpapier &amp; Compliance Center, öffnen Sie die Groß-/Kleinschreibung, und das Postfach aus dem Haltestatus zu entfernen. Weitere Informationen finden Sie unter [Verwalten von eDiscovery-Fälle in die Office 365-Sicherheit &amp; Compliance Center](manage-ediscovery-cases.md).
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a>Schritt 4: Entfernen Sie den Haltestatus Verzögerung aus dem Postfach

Nach beliebigen Typs Haltestatus aus einem Postfach entfernt wird, wird der Wert der *DelayHoldApplied* Postfach-Eigenschaft auf **True**festgelegt. Dadurch wird aufgerufen, eine *Verzögerung halten* und bedeutet, dass das tatsächliche Entfernen des Haltestatus für 30 Tage, um zu verhindern, dass Daten endgültig gelöscht werden verzögert wird (gelöscht) aus dem Postfach.   Bei ein Haltestatus Verzögerung für das Postfach befindet, wird das Postfach weiterhin als werden in der Warteschleife für eine unbegrenzte Dauer, als wenn das Postfach beweissicherungsverfahrens wurde. (Der Zweck der Haltestatus Verzögerung ist Admins Gelegenheit zur Suche oder Wiederherstellen Postfachelemente, die gelöscht werden, nachdem eine Sperre entfernt wurde.) Noe, dass nach 30 Tagen, halten Sie die Verzögerung läuft ab und Office 365 versucht automatisch, den Verzögerung Haltestatus entfernen (durch Festlegen der *DelayHoldApplied* -Eigenschaft auf **false festgelegt**), damit die Sperre tatsächlich entfernt wird. 

Bevor Sie in Schritt 5 Elemente löschen können, müssen Sie den Haltestatus Verzögerung aus dem Postfach entfernt. Führen Sie den folgenden Befehl in Exchange Online PowerShell, um die Verzögerung Haltestatus zu entfernen: 
 
```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Beachten Sie, dass Sie die rechtlichen Aufbewahrungspflicht Rolle im Exchange Online zuweisen müssen, damit der *RemoveDelayHoldApplied* -Parameter verwendet werden.

Zum bestätigen, dass die Verzögerung Haltebereich entfernt wurde, führen Sie den folgenden Befehl aus.

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Der Wert von **"false"** für die *DelayHoldApplied* -Eigenschaft gibt an, dass die Verzögerung entfernt wurde.

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a>Schritt 5: Löschen von Elementen im Ordner "wiederherstellbare Elemente"

Sie können nun Elemente im Ordner "wiederherstellbare Elemente" tatsächlich zu löschen, indem Sie mit dem Cmdlet [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) in Exchange Online PowerShell. Ihnen stehen drei Optionen, wenn das **Search-Mailbox** -Cmdlet ausgeführt wird. 
  
- Kopieren Sie Elemente in einer Zielpostfach, bevor Sie diese löschen, damit Sie die Elemente bei Bedarf überprüfen können, bevor Sie gelöscht werden.
    
- Kopieren von Elementen in einem Zielpostfach und im gleichen Befehl zu löschen.
    
- Löschen Sie Elemente, ohne sie in einer Zielpostfach kopiert werden. 
    
Notiz, die Elemente im Ordner "wiederherstellbare Elemente" im primären Archivpostfach des Benutzers werden ebenfalls gelöscht werden, bei der Ausführung der ** Search-Mailbox ** Cmdlet. Um dies zu verhindern, können Sie die Option *DoNotIncludeArchive* einschließen. Wie bereits zuvor erwähnt, wenn erweiterbares Archivierung für das Postfach aktiviert ist, und die ** Search-Mailbox ** Cmdlet nicht Elemente in einem Hilfs-Archivpostfach gelöscht. Weitere Informationen zu automatisch erweitert archivieren, finden Sie unter [Übersicht über die uneingeschränkte Archivierung in Office 365](unlimited-archiving.md).
  
> [!NOTE]
> Wenn Sie eine Suchabfrage (durch Verwendung des Parameters  *SearchQuery*  ) einschließen, gibt das Cmdlet **Search-Mailbox** maximal 10.000 Elemente in den Suchergebnissen zurück. Wenn Sie also eine Suchabfrage einschließen, müssen Sie den Befehl **Search-Mailbox** möglicherweise mehrere Male ausführen, um mehr als 10.000 Elemente zu löschen. 
  
Die folgenden Beispiele zeigen die Befehlssyntax für jede dieser Optionen an. Diese Beispiele verwenden die `-SearchQuery size>0` Wert des Parameters, der alle Elemente in allen Unterordnern im Ordner "wiederherstellbare Elemente" gelöscht. Wenn Sie nur Elemente löschen, die bestimmte Bedingungen erfüllen müssen, können Sie auch den Parameter *SearchQuery* verwenden, Sonstiges wie den Betreff einer Nachricht oder einen Datumsbereich angeben. Finden Sie [Weitere Beispiele für die Verwendung des Parameters SearchQuery](#other-examples-of-using-the-searchquery-parameter) unten. 
  
### <a name="example-1"></a>Beispiel 1

In diesem Beispiel werden alle Elemente in den Ordner des Benutzers wiederherstellbare Elemente in einen Ordner in Ihrer Organisation Discoverysuchpostfach kopiert. Auf diese Weise können Sie die Elemente lesen, bevor Sie endgültig löschen.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

Im vorherigen Beispiel ist nicht erforderlich zum Kopieren von Elementen auf dem Discoverysuchpostfach. Sie können eine beliebige Zielpostfach Nachrichten kopieren. Wird jedoch empfohlen, um Zugriff auf sensible Postfachdaten zu verhindern, das Kopieren von Nachrichten an ein Postfach, Zugriff auf autorisierte Personen beschränkt ist. Standardmäßig wird auf den Standardwert Discoverysuchpostfach eingeschränkten Zugriff auf Mitglieder der Rollengruppe "Discoveryverwaltung" im Exchange Online. 
  
### <a name="example-2"></a>Beispiel 2

Dieses Beispiel kopiert alle Elemente in den Ordner des Benutzers wiederherstellbare Elemente in einen Ordner in Ihrer Organisation Discoverysuchpostfach und löscht dann die Elemente aus den Ordner des Benutzers wiederherstellbare Elemente.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a>Beispiel 3

Dieses Beispiel löscht alle Elemente in den Ordner des Benutzers wiederherstellbare Elemente, ohne sie in einer Zielpostfach kopiert werden. 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a>Andere Beispiele für die Verwendung des Parameters SearchQuery

Hier sind einige Beispiele für die Verwendung des Parameters *SearchQuery* bestimmte Nachrichten suchen. Wenn Sie den Parameter *SearchQuery* zum Suchen nach bestimmten Objekten verwenden, sollten Sie die Suchergebnisse in eine Zielpostfach kopieren, damit Sie die Suchergebnisse überprüfen und Überarbeiten die Abfrage bei Bedarf ein, bevor Sie die Ergebnisse einer Suche löschen können. 
  
Dieses Beispiel gibt die Nachrichten, die einen bestimmten Ausdruck in das Feld Betreff enthalten.
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

Dieses Beispiel gibt die Nachrichten, die innerhalb des angegebenen Datumsbereichs gesendet wurden.
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
Dieses Beispiel gibt die Nachrichten, die an die angegebene Person gesendet wurden.

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a>Stellen Sie sicher, dass Elemente gelöscht wurden

Zum bestätigen, dass Sie erfolgreich Elemente aus dem Ordner wiederherstellbare Elemente eines Postfachs gelöscht haben, verwenden Sie **Get-mailboxfolderstatistics abrufen** Cmdlet in Exchange Online PowerShell so überprüfen Sie die Größe und Anzahl der Elemente im Ordner "wiederherstellbare Elemente". Sie können diese Statistiken, mit denen vergleichen, die Sie in Schritt 1 gesammelt. 
  
Führen Sie den folgenden Befehl die aktuelle Größe und die Gesamtanzahl der Elemente im Ordner und Unterordner im Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers abgerufen. 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
Führen Sie den folgenden Befehl aus, um die Größe und die Gesamtanzahl der Elemente im Ordner und Unterordner im Ordner "wiederherstellbare Elemente" im Archivpostfach des Benutzers abzurufen. 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a>Schritt 6: Das Postfach in den vorherigen Zustand zurücksetzen

Der letzte Schritt ist das Postfach wieder auf die vorherige Konfiguration wiederherzustellen. Dies bedeutet, dass Zurücksetzen der Eigenschaften, die Sie in Schritt2 geändert und zum erneuten Anwenden der Haltestatus an, denen Sie in Schritt 3 entfernt. Dazu gehören:
  
- Ändern der Aufbewahrungszeit für gelöschte auf den vorherigen Wert zurück. Alternativ können Sie dies in Exchange auf 30 Tage, den Höchstwert festgelegt Online lassen.
    
- Erneutes Aktivieren Wiederherstellung einzelnen Elemente.
    
- Erneutes Aktivieren der Methods für den Clientzugriff, damit der Besitzer ihre Postfächer zugreifen kann.
    
- Erneutes Anwenden der Haltestatus und Office 365-Aufbewahrungsrichtlinien, die Sie entfernt.
    
- Erneutes Aktivieren der Assistenten für verwaltete Ordner das Postfach zu verarbeiten.
    
> [!IMPORTANT]
> Es wird empfohlen, dass Sie warten, 24 Stunden erneut anwenden einer Warteschleife oder die Office 365 Retention Policy (und sichergestellt haben, dass es vorhanden ist), bevor Sie erneut den Assistenten für verwaltete Ordner verarbeitet das Postfach aktivieren. 
  
Führen Sie die folgenden Schritte aus (in der angegebenen Reihenfolge) in Exchange Online PowerShell.
  
1. Führen Sie der folgende Befehl zum Ändern der Aufbewahrungszeit für gelöschte wieder in den ursprünglichen Wert. Dabei wird davon ausgegangen, dass die vorherige Einstellung weniger als 30 Tage ist; Beispiel: 14 Tage. 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. Führen Sie den folgenden Befehl zur Wiederherstellung einzelner Elemente wieder zu aktivieren.
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. Führen Sie den folgenden Befehl aus, um alle Methoden für den Clientzugriff an das Postfach wieder zu aktivieren.
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. Weisen Sie erneut den Haltestatus, die Sie in Schritt 3 entfernt. Je nach Typ des Haltestatus verwenden Sie eines der folgenden Verfahren.
    
    **Beweissicherungsverfahren**
    
    Führen Sie den folgenden Befehl aus, um eine Aufbewahrung für eventuelle Rechtsstreitigkeiten für das Postfach wieder zu aktivieren.
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    **In-Place Hold**
    
    Verwenden Sie die Exchange-Verwaltungskonsole (oder Exchange Online PowerShell), um das Postfach zurück, der In-Place Hold hinzuzufügen. 
    
    **Office 365 Aufbewahrungsrichtlinien auf bestimmte Postfächer angewendet**
    
    Verwenden Sie die Sicherheit &amp; Compliance Center das Postfach wieder in die Office 365-Aufbewahrungsrichtlinie hinzu. Wechseln Sie zu dem **Datum Governance** \> **Aufbewahrung** Seite in das Wertpapier &amp; Compliance Center, bearbeiten Sie die Aufbewahrungsrichtlinie, und fügen Sie das Postfach zurück zur Liste der Empfänger an, die auf die Aufbewahrungsrichtlinie angewendet wird. 
    
    **Office 365-Aufbewahrungsrichtlinien organisationsweiten**
    
    Wenn Sie einer Organisation geltende oder Exchange geltende Aufbewahrungsrichtlinie entfernt, indem Sie es aus der Richtlinie ausschließen, verwenden Sie die Sicherheit &amp; Compliance Center Entfernen des Postfachs aus der Liste der Benutzer ausgeschlossen. Wechseln Sie zu dem **Datum Governance** \> **Aufbewahrung** Seite in das Wertpapier &amp; Compliance Center bearbeiten die Organisation geltende Aufbewahrungsrichtlinie und das Postfach aus der Liste der ausgeschlossenen Empfänger zu entfernen. Auf diese Weise wird die Aufbewahrungsrichtlinie auf das Postfach des Benutzers erneut angewendet. 
    
    **eDiscovery-Fall enthält**
    
    Verwenden Sie die Sicherheit &amp; Compliance Center das Postfach hinzufügen sichern den Haltestatus, die einem eDiscovery-Fall zugeordnet ist. Wechseln Sie zu der **Suche &amp; Untersuchung** \> **eDiscovery** -Seite in das Wertpapier &amp; Compliance Center, öffnen Sie die Groß-/Kleinschreibung, und das Postfach wieder dem Haltestatus hinzufügen. 
    
5. Führen Sie den folgenden Befehl aus, um den Assistenten für verwaltete Ordner erneut verarbeitet das Postfach zuzulassen. Wie bereits erwähnt, es wird empfohlen, dass Sie warten, 24 Stunden erneut anwenden einer Warteschleife oder die Office 365 Retention Policy (und sichergestellt haben, dass es vorhanden ist), bevor Sie erneut den Assistenten für verwaltete Ordner aktivieren. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. Um sicherzustellen, dass das Postfach wieder auf die vorherige Konfiguration wiederhergestellt wurde, können folgende Befehle ausführen, und vergleichen Sie die Einstellungen auf diejenigen aus, denen Sie in Schritt 1 gesammelt.

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a>Weitere Informationen

Hier ist eine Tabelle, die beschreibt, wie verschiedene Arten von Haltestatus basierend auf den Werten in der *InPlaceHolds* -Eigenschaft, bei der Ausführung der Cmdlets **Get-Mailbox** oder **Get-OrganizationConfig** zu identifizieren. Ausführlichere Informationen finden Sie unter [So identifizieren Sie den Typ des Archiv platziert eines Exchange Online-Postfachs](identify-a-hold-on-an-exchange-online-mailbox.md).

Wie bereits erläutert, müssen Sie alle Haltestatus entfernen und Aufbewahrungsrichtlinien aus einem Postfach, bevor Sie Office 365 können erfolgreich Löschen von Elementen im Ordner "wiederherstellbare Elemente". 
  
|**Haltebereichstyp**|**Beispielwert**|**So identifizieren Sie den Haltestatus**|
|:-----|:-----|:-----|
|Beweissicherungsverfahren  <br/> | `True` <br/> |Die  *LitigationHoldEnabled*  -Eigenschaft wird festgelegt auf  `True`.  <br/> |
|Compliance-Archiv  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |Die *InPlaceHolds* -Eigenschaft enthält die GUID der der Compliance-Archivs, das für das Postfach befindet. Sie können erkennen, dass dies eine In-Place Hold ist, da die GUID nicht mit einem Präfix beginnt.<br/> Sie können den Befehl  `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL "Command in Exchange Online PowerShell Abrufen von Informationen zu den In-Place Hold für das Postfach.  <br/> |
| Office 365-Aufbewahrungsrichtlinien in das Wertpapier &amp; Compliance Center auf bestimmte Postfächer angewendet  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> oder  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |Wenn Sie das Cmdlet **Get-Mailbox** ausführen, enthält die *InPlaceHolds* -Eigenschaft auch GUIDs der Office 365-Aufbewahrungsrichtlinien an das Postfach angewendet. Sie können Aufbewahrungsrichtlinien identifizieren, weil die GUID mit beginnt die `mbx` Präfix. Beachten Sie, dass die GUID der Aufbewahrungsrichtlinie mit beginnt die `skp` Präfix, die das gibt an, dass die Aufbewahrungsrichtlinie auf Skype für Business Unterhaltungen angewendet wird.<br/> Identität der Office 365-Aufbewahrungsrichtlinie, die an das Postfach angewendet wird, führen Sie den folgenden Befehl in der Sicherheit &amp; Compliance Center PowerShell: <br/> <br/>"Get-RetentionCompliancePolicy<retention policy GUID without prefix> | FL Name`<br/><br/>Be sure to remove the  `Mbx` or  `Skp' Präfix, wenn Sie diesen Befehl ausführen.  <br/> |
|Organisationsweite Office 365-Aufbewahrungsrichtlinien in das Wertpapier &amp; Compliance Center  <br/> |Kein Wert  <br/> oder  <br/>  `-mbxe9b52bf7ab3b46a286308ecb29624696`(gibt an, dass das Postfach von eine unternehmensweite Richtlinie ausgeschlossen ist)  <br/> |Selbst wenn die *InPlaceHolds* -Eigenschaft leer ist, wenn Sie das **Get-Mailbox** -Cmdlet ausführen, weiterhin möglicherweise mindestens einen organisationsweiten Office 365 Aufbewahrungsrichtlinien auf das Postfach angewendet.  <br/> Um dies zu überprüfen, führen Sie das "Get-OrganizationConfig | FL InPlaceHolds` command in Exchange Online PowerShell to get a list of the GUIDs for organization-wide Office 365 retention policies. The GUID for organization-wide retention policies applied to Exchange mailboxes start with the  `Mbx` prefix; for example  `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> To identity the organization-wide Office 365 retention policy that's applied to the mailbox, run the following command in Security &amp; Compliance Center PowerShell: <br/><br/> `Get-RetentionCompliancePolicy<retention policy GUID without prefix> | FL Name`<br/><br/>Note that if a mailbox is excluded from an organization-wide Office 365 retention policy, the GUID for the retention policy is displayed in the  *InPlaceHolds*  property of the user's mailbox when you run the **Get-Mailbox** cmdlet; it's identified by the prefix  `Mbx -`; for example,  `-mbxe9b52bf7ab3b46a286308ecb29624696' <br/> |
|eDiscovery-Fall in der Security &amp; Compliance Center  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |Die *InPlaceHolds* -Eigenschaft enthält auch die GUID des eine Sperre einer eDiscovery-Fall in das Wertpapier zugeordnet &amp; Compliance Center, die für das Postfach verwendet werden kann. Sie können erkennen, dies ist ein eDiscovery Groß-/Kleinschreibung halten, da die GUID mit beginnt die `UniH` Präfix.<br/> Sie können die `Get-CaseHoldPolicy` -Cmdlet in Security &amp; Compliance Center PowerShell Abrufen von Informationen zu eDiscovery-Fall, die die Sperre für das Postfach zugeordnet ist. Beispielsweise können Sie den Befehl ausführen "Get-CaseHoldPolicy<hold GUID without prefix> | FL Name` to display the name of the case hold that's on the mailbox. Be sure to remove the  `UniH` prefix when you run this command.  <br/><br/> To identity the eDiscovery case that the hold on the mailbox is associated with, run the following commands:<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix> `<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name'


