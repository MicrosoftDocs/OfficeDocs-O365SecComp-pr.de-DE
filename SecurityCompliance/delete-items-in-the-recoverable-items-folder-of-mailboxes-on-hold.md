---
title: Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von Cloud-basierten Postfächern in Hold-Admin-Hilfe
ms.author: markjjo
author: markjjo
manager: laurawi
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
ms.assetid: a85e1c87-a48e-4715-bfa9-d5275cde67b0
description: 'Für Administratoren: Löschen Sie Elemente im Ordner "Wiederherstellbare Elemente" eines Benutzers für ein Exchange Online-Postfach, auch wenn das Postfach in der gesetzlichen Aufbewahrungspflicht steht. Dies ist eine effektive Möglichkeit zum Löschen von Daten, die versehentlich in Office 365 verschüttet wurden.'
ms.openlocfilehash: a1abfd73d96db6d67e1e1fe13d5487ac55c40344
ms.sourcegitcommit: c0d4fe3e43e22353f30034567ade28330266bcf7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2019
ms.locfileid: "30900114"
---
# <a name="delete-items-in-the-recoverable-items-folder-of-cloud-based-mailboxes-on-hold---admin-help"></a>Löschen von Elementen im Ordner "Wiederherstellbare Elemente" von Cloud-basierten Postfächern in Hold-Admin-Hilfe

Der Ordner "Wiederherstellbare Elemente" für ein Exchange Online-Postfach ist vorhanden, um vor versehentlichen oder böswilligen Löschungen zu schützen. Es wird auch verwendet, um Elemente zu speichern, die von den Office 365-Kompatibilitätsfeatures, wie zum Beispiel Aufbewahrungs-und eDiscovery-suchen, gespeichert werden. In einigen Situationen können Organisationen jedoch Daten enthalten, die versehentlich im Ordner "Wiederherstellbare Elemente" aufbewahrt wurden, die Sie löschen müssen. Beispielsweise kann ein Benutzer unwissentlich eine e-Mail-Nachricht mit vertraulichen Informationen oder Informationen, die schwerwiegende geschäftliche Konsequenzen haben können, senden oder weiterleiten. Auch wenn die Nachricht dauerhaft gelöscht wird, wird Sie möglicherweise unbegrenzt aufbewahrt, da für das Postfach eine rechtliche Aufbewahrungspflicht festgestellt wurde. Dieses Szenario wird als Datenüberlauf bezeichnet, da Daten versehentlich in Office 365 verschüttet wurden. In diesen Situationen können Sie Elemente im Ordner "Wiederherstellbare Elemente" eines Benutzers für ein Exchange Online-Postfach löschen, auch wenn das Postfach mit einer der verschiedenen halte Features in Office 365 in der Warteschleife gespeichert wird. Zu diesen Aufbewahrungsarten gehört das Rechtsschutzverfahren, in-situ-Speicher, eDiscovery-Haltestatus und Office 365-Archivierungsrichtlinien &amp; , die im Office 365 Security Compliance Center erstellt wurden. 
  
 In diesem Artikel wird erläutert, wie Sie Elemente aus dem Ordner "Wiederherstellbare Elemente" für in der Warteschleife aktivierte Cloud-basierte Postfächer löschen. Dieses Verfahren beinhaltet das Deaktivieren des Zugriffs auf das Postfach und das Deaktivieren der Wiederherstellung einzelner Elemente, das Deaktivieren des Assistenten für verwaltete Ordner von der Verarbeitung des Postfachs, das vorübergehende Entfernen des haltebereichs, das Löschen von Elementen aus dem Ordner "Wiederherstellbare Elemente" und das anschließende Wiederherstellen die vorherige Konfiguration des Postfachs. Hier ist der Prozess: 
  
[Schritt 1: Sammeln von Informationen über das Postfach](#step-1-collect-information-about-the-mailbox)

[Schritt 2: Vorbereiten des Postfachs](#step-2-prepare-the-mailbox)

[Schritt 3: Entfernen aller haltebereiche aus dem Postfach](#step-3-remove-all-holds-from-the-mailbox)

[Schritt 4: Entfernen des Verzögerungs Speichers aus dem Postfach](#step-4-remove-the-delay-hold-from-the-mailbox)

[Schritt 5: Löschen von Elementen im Ordner "Wiederherstellbare Elemente"](#step-5-delete-items-in-the-recoverable-items-folder)

[Schritt 6: Zurücksetzen des Postfachs in den vorherigen Zustand](#step-6-revert-the-mailbox-to-its-previous-state)
  
> [!CAUTION]
> Die in diesem Artikel beschriebenen Verfahren führen dazu, dass Daten dauerhaft aus einem Exchange Online-Postfach gelöscht werden. Das heißt, dass Nachrichten, die Sie aus dem Ordner "Wiederherstellbare Elemente" löschen, nicht wiederhergestellt werden können und nicht für rechtliche Ermittlungen oder andere Compliance-Zwecke zur Verfügung stehen. Wenn Sie Nachrichten aus einem Postfach löschen möchten, das im Rahmen eines Rechtsstreits, eines in-situ-Speichers, einer eDiscovery-Speicherung oder einer im Office 365 Security &amp; Compliance Center erstellten Office 365-Aufbewahrungsrichtlinie aufbewahrt wird, erkundigen Sie sich bei ihrer Datensatzverwaltung oder den gesetzlichen Bestimmungen. Abteilungen vor dem Entfernen des haltebereichs. Ihre Organisation verfügt möglicherweise über eine Richtlinie, die definiert, ob ein Postfach in der Warteschleife oder ein Vorfall mit Daten ausschütten Vorrang hat. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen beide der folgenden Verwaltungsrollen in Exchange Online zugewiesen sein, um nach Nachrichten aus dem Ordner "Wiederherstellbare Elemente" in Schritt 5 zu suchen und zu löschen.
    
  - **Postfachsuche** – mit dieser Rolle können Sie Postfächer in Ihrer Organisation durchsuchen. Exchange-Administratoren werden standardmäßig nicht dieser Rolle zugewiesen. Wenn Sie diese Rolle zuweisen möchten, fügen Sie sich selbst als Mitglied der Rollengruppe "Discoveryverwaltung" in Exchange Online hinzu. 
    
  - **Post Fach Import** – mit dieser Rolle können Sie Nachrichten aus dem Postfach eines Benutzers löschen. Diese Rolle ist standardmäßig keiner Rollengruppe zugewiesen. Zum Löschen von Nachrichten aus Benutzerpostfächern können Sie die Rolle "Post Fach Import-Export" zur Rollengruppe "Organisationsverwaltung" in Exchange Online hinzufügen. 
    
- Das in diesem Artikel beschriebene Verfahren wird für inaktive Postfächer nicht unterstützt. Das liegt daran, dass Sie nach dem Entfernen eine Aufbewahrungsrichtlinie (oder eine Office-365-Richtlinie) nicht mehr auf ein inaktives Postfach anwenden können. Wenn Sie einen Haltebereich aus einem inaktiven Postfach entfernen, wird er in ein normales gelöschtes Postfach geändert und dauerhaft aus Ihrer Organisation gelöscht, nachdem es vom Assistenten für verwaltete Ordner verarbeitet wurde.
    
- Sie können dieses Verfahren nicht für ein Postfach ausführen, das einer Office 365-Aufbewahrungsrichtlinie zugewiesen wurde, die mit einer Aufbewahrungs Sperre gesperrt wurde. Das liegt daran, dass Sie durch eine Aufbewahrungs Sperre das Entfernen oder ausschließen des Postfachs aus der Office 365-Aufbewahrungsrichtlinie und das Deaktivieren des Assistenten für verwaltete Ordner für das Postfach verhindern. Weitere Informationen zum Sperren von Aufbewahrungsrichtlinien finden Sie unter [Sperren einer Aufbewahrungsrichtlinie](retention-policies.md#locking-a-retention-policy).
    
- Wenn ein Postfach nicht gehalten wird (oder die Wiederherstellung einzelner Elemente nicht aktiviert ist), können Sie die Elemente einfach aus dem Ordner "Wiederherstellbare Elemente" löschen. Weitere Informationen dazu finden Sie unter [Suchen nach und Löschen von Nachrichten ](https://go.microsoft.com/fwlink/?linkid=852453).
  
## <a name="step-1-collect-information-about-the-mailbox"></a>Schritt 1: Sammeln von Informationen über das Postfach

Dieser erste Schritt besteht darin, ausgewählte Eigenschaften aus dem Zielpostfach zu sammeln, die sich auf diese Prozedur auswirken. Notieren Sie sich diese Einstellungen, oder speichern Sie Sie in einer Textdatei, da Sie einige dieser Eigenschaften ändern und dann auf die ursprünglichen Werte in Schritt 6 zurücksetzen, nachdem Sie Elemente aus dem Ordner "Wiederherstellbare Elemente" gelöscht haben. Hier finden Sie eine Liste der Postfacheigenschaften, die Sie sammeln müssen.
  
-  *SingleItemRecoveryEnabled* und *Parameter RetainDeletedItemsFor* ; Falls erforderlich, deaktivieren Sie einzelne Wiederherstellung, und erweitern Sie den Aufbewahrungszeitraum für gelöschte Elemente in Schritt 3. 
    
-  *LitigationHoldEnabled* und *InPlaceHolds* ; Sie müssen alle für das Postfach festgelegten haltebereiche identifizieren, damit Sie Sie vorübergehend in Schritt 3 entfernen können. Im Abschnitt [Weitere Informationen](#more-information) finden Sie Tipps dazu, wie Sie den Typ Hold identifizieren, der möglicherweise in einem Postfach gespeichert wird. 
    
Darüber hinaus müssen Sie die Einstellungen für den Post Fach Clientzugriff abrufen, damit Sie Sie vorübergehend deaktivieren können, damit der Besitzer (oder andere Benutzer) während dieses Verfahrens nicht auf das Postfach zugreifen kann. Schließlich können Sie die aktuelle Größe und Anzahl der Elemente im Ordner "Wiederherstellbare Elemente" abrufen. Nachdem Sie Elemente im Ordner "Wiederherstellbare Elemente" in Schritt 5 gelöscht haben, verwenden Sie diese Informationen, um zu überprüfen, ob die Elemente tatsächlich entfernt wurden.
  
1. [Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://go.microsoft.com/fwlink/?linkid=396554). Achten Sie darauf, einen Benutzernamen und ein Kennwort für ein Administratorkonto zu verwenden, dem die entsprechenden Verwaltungsrollen in Exchange Online zugewiesen wurden. 
    
2. Führen Sie den folgenden Befehl aus, um Informationen zur Wiederherstellung einzelner Elemente und zur Aufbewahrungsdauer für gelöschte Elemente abzurufen.

    ```
    Get-Mailbox <username> | FL SingleItemRecoveryEnabled,RetainDeletedItemsFor
    ```

   Wenn die Wiederherstellung einzelner Elemente aktiviert ist, müssen Sie Sie in Schritt 2 deaktivieren. Wenn der Aufbewahrungszeitraum für gelöschte Elemente für 30 Tage (der Höchstwert in Exchange Online) nicht festgelegt ist, können Sie ihn in Schritt 2 erweitern. 
    
3. Führen Sie den folgenden Befehl aus, um die Einstellungen für den Postfachzugriff für das Postfach abzurufen. 
    
    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```

   In Schritt 2 werden alle diese Zugriffsmethoden deaktiviert.
    
4. Führen Sie den folgenden Befehl aus, um Informationen zu den Haltebereichen und Office 365-Aufbewahrungsrichtlinien für das Postfach abzurufen.
    
    ```
    Get-Mailbox <username> | FL LitigationHoldEnabled,InPlaceHolds
    ```


   > [!TIP]
    > Wenn die *InPlaceHolds* -Eigenschaft zu viele Werte enthält und nicht alle angezeigt werden, können Sie den `Get-Mailbox <username> | Select-Object -ExpandProperty InPlaceHolds` Befehl ausführen, um jeden Wert in einer separaten Zeile anzuzeigen. 
  
5. Führen Sie den folgenden Befehl aus, um Informationen zu organisationsweiten Office 365-Aufbewahrungsrichtlinien abzurufen. 

    ```
    Get-OrganizationConfig | FL InPlaceHolds
    ```
   Wenn Ihre Organisation über organisationsweite Office 365-Aufbewahrungsrichtlinien verfügt, müssen Sie das Postfach in Schritt 3 aus diesen Richtlinien ausschließen.

   > [!TIP]
    > Wenn die *InPlaceHolds* -Eigenschaft zu viele Werte enthält und nicht alle angezeigt werden, können Sie den `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` Befehl ausführen, um jeden Wert in einer separaten Zeile anzuzeigen. 
  
6. Führen Sie den folgenden Befehl aus, um die aktuelle Größe und Gesamtanzahl von Elementen in Ordnern und Unterordnern im Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers abzurufen. 

    ```
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Wenn das Archivpostfach des Benutzers aktiviert ist, führen Sie den folgenden Befehl aus, um die Größe und Gesamtanzahl von Elementen in Ordnern und Unterordnern im Ordner "Wiederherstellbare Elemente" in Ihrem Archivpostfach abzurufen. 

    ```s
    Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
    ```

   Wenn Sie Elemente in Schritt 5 löschen, können Sie auswählen, ob Elemente im Ordner "Wiederherstellbare Elemente" im primären Archivpostfach des Benutzers gelöscht oder nicht gelöscht werden sollen. Beachten Sie, dass Elemente in einem zusätzlichen Archivpostfach nicht gelöscht werden, wenn die automatische Erweiterung der Archivierung für das Postfach aktiviert ist.
  
## <a name="step-2-prepare-the-mailbox"></a>Schritt 2: Vorbereiten des Postfachs

Nachdem Sie Informationen zum Postfach gesammelt und gespeichert haben, besteht der nächste Schritt im Vorbereiten des Postfachs, indem Sie die folgenden Aufgaben ausführen: 
  
- **Deaktivieren Sie den Clientzugriff auf das Postfach** , sodass der Postfachbesitzer während dieses Verfahrens nicht auf sein Postfach zugreifen und Änderungen an den Postfachdaten vornehmen kann. 
    
- **Verlängern Sie die Aufbewahrungsdauer für gelöschte** Elemente auf 30 Tage (den Höchstwert in Exchange Online), sodass Elemente nicht aus dem Ordner "Wiederherstellbare Elemente" gelöscht werden, bevor Sie Sie in Schritt 5 löschen können. 
    
- **Deaktivieren Sie die Wiederherstellung einzelner** Elemente, damit Elemente (für die Dauer des Aufbewahrungszeitraums für gelöschte Elemente) nicht aufbewahrt werden, nachdem Sie Sie aus dem Ordner "Wiederherstellbare Elemente" in Schritt 5 gelöscht haben. 
    
- **Deaktivieren Sie den Assistenten für verwaltete Ordner** , sodass er das Postfach nicht verarbeitet und die Elemente, die Sie in Schritt 5 löschen, nicht aufbewahren. 
    
Führen Sie die folgenden Schritte in Exchange Online PowerShell aus.
  
1. Führen Sie den folgenden Befehl aus, um den gesamten Clientzugriff auf das Postfach zu deaktivieren. Bei der Befehlssyntax wird davon ausgegangen, dass alle Clientzugriffsmethoden für das Postfach aktiviert wurden.

    ```   
    Set-CASMailbox <username> -EwsEnabled $false -ActiveSyncEnabled $false -MAPIEnabled $false -OWAEnabled $false -ImapEnabled $false -PopEnabled $false
    ```
   
   > [!NOTE]
    > Es kann bis zu 60 Minuten dauern, bis alle Clientzugriffsmethoden für das Postfach deaktiviert wurden. Beachten Sie, dass durch das Deaktivieren dieser Zugriffsmethoden der Postfachbesitzer, den Sie derzeit angemeldet haben, nicht getrennt wird. Wenn der Besitzer nicht angemeldet ist, kann er nicht mehr auf sein Postfach zugreifen, nachdem diese Zugriffsmethoden deaktiviert wurden. 
  
2. Führen Sie den folgenden Befehl aus, um die Aufbewahrungsdauer für gelöschte Elemente um maximal 30 Tage zu verlängern. Dabei wird davon ausgegangen, dass die aktuelle Einstellung weniger als 30 Tage beträgt. 

    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 30
    ```

3. Führen Sie den folgenden Befehl aus, um die Wiederherstellung einzelner Elemente zu deaktivieren.
    
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $false
    ```

   > [!NOTE]
    > Es kann bis zu 60 Minuten dauern, bis die Wiederherstellung einzelner Elemente deaktiviert ist. Löschen Sie keine Elemente im Ordner "Wiederherstellbare Elemente", bis dieser Zeitraum abgelaufen ist. 
  
4. Führen Sie den folgenden Befehl aus, um zu verhindern, dass der Assistent für verwaltete Ordner das Postfach verarbeitet. Wie bereits erläutert, können Sie den Assistenten für verwaltete Ordner nur deaktivieren, wenn keine Office 365-Aufbewahrungsrichtlinie mit einer erHaltungs Sperre auf das Postfach angewendet wird. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $true
    ```

## <a name="step-3-remove-all-holds-from-the-mailbox"></a>Schritt 3: Entfernen aller haltebereiche aus dem Postfach

Der letzte Schritt, bevor Sie Elemente aus dem Ordner "Wiederherstellbare Elemente" löschen können, besteht darin, alle haltebereiche (die Sie in Schritt 1 identifiziert haben) für das Postfach zu entfernen. Alle haltebereiche müssen entfernt werden, damit Elemente nicht aufbewahrt werden, nachdem Sie Sie aus dem Ordner "Wiederherstellbare Elemente" gelöscht haben. Die folgenden Abschnitte enthalten Informationen zum Entfernen unterschiedlicher Aufbewahrungs Typen für ein Postfach. Im Abschnitt [Weitere Informationen](#more-information) finden Sie Tipps dazu, wie Sie den Typ Hold identifizieren, der möglicherweise in einem Postfach gespeichert wird. Weitere Informationen finden Sie unter [Vorgehensweise beim Identifizieren des Aufbewahrungs Typs für ein Exchange Online-Postfach](identify-a-hold-on-an-exchange-online-mailbox.md).
  
> [!CAUTION]
> Wie bereits erwähnt, erkundigen Sie sich bei ihrer Datensatzverwaltung oder Rechtsabteilung vor dem Entfernen eines haltebereichs aus einem Postfach. 
  
 ### <a name="litigation-hold"></a>Aufbewahrung für eventuelle Rechtsstreitigkeiten
  
Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um eine Beweissicherung aus dem Postfach zu entfernen.

```
Set-Mailbox <username> -LitigationHoldEnabled $false
```

   
> [!NOTE]
> Ähnlich wie bei der Deaktivierung der Clientzugriffsmethoden und der Wiederherstellung einzelner Elemente kann es bis zu 60 Minuten dauern, bis die Beweissicherung entfernt wurde. Löschen Sie keine Elemente aus dem Ordner "Wiederherstellbare Elemente", bis dieser Zeitraum abgelaufen ist. 
  
 ### <a name="in-place-hold"></a>Compliance-Archiv
  
Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den in-situ-Speicher für das Postfach zu identifizieren. Verwenden Sie die GUID für den in-situ-Speicher, den Sie in Schritt 1 identifiziert haben. 

```
Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL Name
```
   
Nachdem Sie den in-situ-Speicher identifiziert haben, können Sie die Exchange-Verwaltungskonsole (EAC) oder Exchange Online PowerShell verwenden, um das Postfach aus dem Haltebereich zu entfernen. Weitere Informationen finden Sie unter [Erstellen oder Entfernen eines Compliance-Archivs](https://go.microsoft.com/fwlink/?linkid=852668).
  
 ### <a name="office-365-retention-policies-applied-to-specific-mailboxes"></a>Office 365-Aufbewahrungsrichtlinien, die auf bestimmte Postfächer angewendet werden
  
Führen Sie den folgenden Befehl in [office 365 &amp; Security Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) aus, um die auf das postfach angewendete Office 365-Aufbewahrungsrichtlinie zu identifizieren. Verwenden Sie die GUID (ohne das `mbx` Präfix `skp` oder) für die Aufbewahrungsrichtlinie, die Sie in Schritt 1 identifiziert haben. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```
   
Nachdem Sie die Aufbewahrungsrichtlinie identifiziert haben, wechseln Sie zur Seite Aufbewahrungszeit für &amp; die **Datenverwaltung** \> **** im Security Compliance Center, bearbeiten Sie die Aufbewahrungsrichtlinie, die Sie im vorherigen Schritt identifiziert haben, und entfernen Sie das Postfach aus der Liste der Empfänger, die in der Aufbewahrungsrichtlinie enthalten sind. 
  
 ### <a name="organization-wide-office-365-retention-policies"></a>Organisationsweite Office 365-Aufbewahrungsrichtlinien
  
Organisationsweite und Exchange-weite Office 365-Aufbewahrungsrichtlinien werden auf jedes Postfach in der Organisation angewendet. Sie werden auf Organisationsebene (nicht auf die Postfachebene) angewendet und werden zurückgegeben, wenn Sie das Cmdlet **Get-OrganizationConfig** in Schritt 1 ausführen. Führen Sie den folgenden Befehl [in &amp; Security Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) aus, um die organisationsweiten Office 365-Aufbewahrungsrichtlinien zu identifizieren. Verwenden Sie die GUID (ohne `mbx` Präfix) für die organisationsweiten Aufbewahrungsrichtlinien, die Sie in Schritt 1 identifiziert haben. 

```
Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name
```

nachdem sie die organisationsweiten Office 365-aufbewahrungsrichtlinien identifiziert haben, navigieren sie im &amp; Security Compliance Center zur seite zur **aufbewahrung** der **datenverwaltung** \> , und bearbeiten sie jede organisationsweite aufbewahrungsrichtlinie, die sie im vorherigen Schritt, und fügen Sie das Postfach zur Liste der ausgeschlossenen Empfänger hinzu. Dadurch wird das Postfach des Benutzers aus der Aufbewahrungsrichtlinie entfernt. 

### <a name="office-365-retention-labels"></a>Office 365-Aufbewahrungs Bezeichnungen

Wenn ein Benutzer eine Bezeichnung anwendet, die so konfiguriert ist, dass Inhalte aufbewahrt oder aufbewahrt und dann Inhalte in einem beliebigen Ordner oder Element in Ihrem Postfach gelöscht werden, wird die *ComplianceTagHoldApplied* -Postfacheigenschaft auf **true**festgelegt. Wenn dies der Fall ist, wird das Postfach als in der Warteschleife gehalten, so als ob es in einem Rechtsstreit gehalten oder einer Office 365-Aufbewahrungsrichtlinie zugewiesen wurde.

Führen Sie den folgenden Befehl in Exchange Online PowerShell aus, um den Wert der *ComplianceTagHoldApplied* -Eigenschaft anzuzeigen:

```
Get-Mailbox <username> |FL ComplianceTagHoldApplied
```

Nachdem Sie festgestellt haben, dass ein Postfach in der Warteschleife ist, weil eine Aufbewahrungs Bezeichnung auf einen Ordner oder ein Element angewendet wird, können Sie das Inhaltssuche-Tool im Security & Compliance Center verwenden, um mithilfe der ComplianceTag-Suchbedingung nach beschrifteten Elementen zu suchen. Weitere Informationen finden Sie im Abschnitt "Suchbedingungen" in [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md#conditions-for-common-properties).

Weitere Informationen zu Bezeichnungen finden Sie unter [Overview of Office 365 Labels](labels.md).

 ### <a name="ediscovery-case-holds"></a>eDiscovery-Fall enthält
  
Führen Sie die folgenden Befehle [in &amp; Security Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=627084) aus, um den Haltebereich zu identifizieren, der einem eDiscovery-Fall zugeordnet ist, der auf das Postfach angewendet wird. Verwenden Sie die GUID (ohne `UniH` Präfix) für den eDiscovery-Speicher, den Sie in Schritt 1 identifiziert haben. Beachten Sie, dass mit dem zweiten Befehl der Name des eDiscovery-falls angezeigt wird, dem der Haltebereich zugeordnet ist. der dritte Befehl zeigt den Namen des Haltestatus an. 
  
```
$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>
```

```
Get-ComplianceCase $CaseHold.CaseId | FL Name
```

```
$CaseHold.Name
```

Nachdem Sie den Namen des eDiscovery-Falls und den Haltestatus ermittelt haben, wechseln Sie im &amp; Security Compliance Center zur \> **eDiscovery** -Seite für die **Suche &amp; ** , öffnen Sie den Fall, und entfernen Sie das Postfach aus dem Haltebereich. Weitere Informationen finden Sie unter [Verwalten von eDiscovery-Fällen im Office 365 &amp; Security Compliance Center](manage-ediscovery-cases.md).
  
## <a name="step-4-remove-the-delay-hold-from-the-mailbox"></a>Schritt 4: Entfernen des Verzögerungs Speichers aus dem Postfach

Nachdem ein Aufbewahrungs aus einem Postfach entfernt wurde, wird der Wert der *DelayHoldApplied* -Postfacheigenschaft auf **true**festgelegt. Dies tritt auf, wenn der Assistent für verwaltete Ordner das nächste Mal das Postfach verarbeitet und erkennt, dass ein Haltebereich entfernt wurde. Dies wird als *Verzögerungs Sperre* bezeichnet und bedeutet, dass das tatsächliche Entfernen des Haltestatus für 30 Tage verzögert wird, um zu verhindern, dass Daten dauerhaft aus dem Postfach gelöscht werden. (Der Zweck einer Verzögerungs Sperre besteht darin, Administratoren die Möglichkeit zu geben, Postfachelemente zu suchen oder wiederherzustellen, die nach dem Entfernen eines Haltestatus gelöscht werden.)  Wenn ein Verzögerungs Speicher für das Postfach gespeichert wird, wird das Postfach für eine unbegrenzte Dauer nach wie vor als für das Postfach aktiviert gehalten. Nach 30 Tagen wird die Verzögerungsdauer abgelaufen, und Office 365 versucht automatisch, die Verzögerungsdauer zu entfernen (indem Sie die *DelayHoldApplied* -Eigenschaft auf **false**festlegen), sodass der Haltebereich tatsächlich entfernt wird. 

Bevor Sie Elemente in Schritt 5 löschen können, müssen Sie die Verzögerungsdauer aus dem Postfach entfernen. Bestimmen Sie zunächst, ob die Verzögerungs Sperre auf das Postfach angewendet wird, indem Sie den folgenden Befehl in Exchange Online PowerShell ausführen:

```
Get-Mailbox <username> | FL DelayHoldApplied
```

Wenn der Wert der *DelayHoldApplied* -Eigenschaft auf **false**festgelegt ist, wurde keine Verzögerungsdauer für das Postfach gespeichert. Sie können zu Schritt 5 wechseln und Elemente im Ordner "Wiederherstellbare Elemente" löschen.

Wenn der Wert der *DelayHoldApplied* -Eigenschaft auf **true**festgelegt ist, führen Sie den folgenden Befehl aus, um die Verzögerungsdauer zu entfernen:

```
Set-Mailbox <username> -RemoveDelayHoldApplied
```
Beachten Sie, dass Sie in Exchange Online zur Verwendung des *RemoveDelayHoldApplied* -Parameters die rechtliche Aufbewahrungspflicht zugewiesen werden müssen.

## <a name="step-5-delete-items-in-the-recoverable-items-folder"></a>Schritt 5: Löschen von Elementen im Ordner "Wiederherstellbare Elemente"

Jetzt können Sie Elemente im Ordner "Wiederherstellbare Elemente" tatsächlich löschen, indem Sie das Cmdlet [Search-Mailbox](https://go.microsoft.com/fwlink/?linkid=852595) in Exchange Online PowerShell verwenden. Beim Ausführen des Cmdlets **Search-Mailbox** haben Sie drei Optionen. 
  
- Kopieren Sie die Elemente vor dem Löschen in ein Zielpostfach, damit Sie die Elemente ggf. überarbeiten können, bevor Sie Sie löschen.
    
- Kopieren Sie Elemente in ein Zielpostfach, und löschen Sie Sie im gleichen Befehl.
    
- Elemente löschen, ohne Sie in ein Zielpostfach zu kopieren. 
    
Beachten Sie, dass Elemente im Ordner "Wiederherstellbare Elemente" im primären Archivpostfach des Benutzers auch gelöscht werden, wenn Sie das Cmdlet " **Search-Mailbox** " ausführen. Um dies zu verhindern, können Sie die Option  *DoNotIncludeArchive*  einschließen. Und wie bereits erwähnt, wenn die automatische Erweiterung der Archivierung für das Postfach aktiviert ist, löscht das * * Search-Mailbox * *-Cmdlet keine Elemente in einem zusätzlichen Archivpostfach. Weitere Informationen zum automatisch expandierenden Archiv finden Sie unter [Übersicht über die unbegrenzte Archivierung in Office 365](unlimited-archiving.md).
  
> [!NOTE]
> Wenn Sie eine Suchabfrage (durch Verwendung des Parameters  *SearchQuery*  ) einschließen, gibt das Cmdlet **Search-Mailbox** maximal 10.000 Elemente in den Suchergebnissen zurück. Wenn Sie also eine Suchabfrage einschließen, müssen Sie den Befehl **Search-Mailbox** möglicherweise mehrere Male ausführen, um mehr als 10.000 Elemente zu löschen. 
  
Die folgenden Beispiele zeigen die Befehlssyntax für jede dieser Optionen. In diesen Beispielen wird `-SearchQuery size>0` der Parameterwert verwendet, mit dem alle Elemente aus allen Unterordnern im Ordner "Wiederherstellbare Elemente" gelöscht werden. Wenn Sie nur Elemente löschen müssen, die bestimmten Bedingungen entsprechen, können Sie auch den *SearchQuery* -Parameter verwenden, um andere Bedingungen anzugeben, beispielsweise den Betreff einer Nachricht oder einen Datumsbereich. [Weitere Beispiele zur Verwendung des SearchQuery-Parameters](#other-examples-of-using-the-searchquery-parameter) finden Sie weiter unten. 
  
### <a name="example-1"></a>Beispiel 1

In diesem Beispiel werden alle Elemente im Ordner "Wiederherstellbare Elemente" des Benutzers in einen Ordner im Discovery-Such Postfach Ihrer Organisation kopiert. Auf diese Weise können Sie die Elemente überarbeiten, bevor Sie sie endgültig löschen.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>"
```

Im vorherigen Beispiel ist es nicht erforderlich, Elemente in das Such Postfach für die Suche zu kopieren. Sie können Nachrichten in ein beliebiges Zielpostfach kopieren. Um den Zugriff auf potenziell vertrauliche Postfachdaten zu verhindern, wird jedoch empfohlen, Nachrichten in ein Postfach zu kopieren, das Zugriff auf autorisiertes Personal hat. Standardmäßig ist der Zugriff auf das standardmäßige Discovery-Such Postfach auf Mitglieder der Rollengruppe "Discoveryverwaltung" in Exchange Online beschränkt. 
  
### <a name="example-2"></a>Beispiel 2

In diesem Beispiel werden alle Elemente im Ordner "Wiederherstellbare Elemente" des Benutzers in einen Ordner im Discovery-Such Postfach Ihrer Organisation kopiert und dann die Elemente aus dem Ordner "Wiederherstellbare Elemente" des Benutzers gelöscht.

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -TargetMailbox "Discovery Search Mailbox" -TargetFolder "<foldername>" -DeleteContent
```
 
### <a name="example-3"></a>Beispiel 3

In diesem Beispiel werden alle Elemente im Ordner "Wiederherstellbare Elemente" des Benutzers gelöscht, ohne Sie in ein Zielpostfach zu kopieren. 

```
Search-Mailbox <username> -SearchQuery size>0 -SearchDumpsterOnly -DeleteContent
```

### <a name="other-examples-of-using-the-searchquery-parameter"></a>Weitere Beispiele für die Verwendung des SearchQuery-Parameters

Hier einige Beispiele für die Verwendung des *SearchQuery* -Parameters zum Suchen bestimmter Nachrichten. Wenn Sie den Parameter *SearchQuery* verwenden, um nach bestimmten Elementen zu suchen, können Sie die Suchergebnisse in ein Zielpostfach kopieren, um die Suchergebnisse zu überprüfen und dann die Abfrage zu überarbeiten, bevor Sie die Ergebnisse einer Suche löschen. 
  
In diesem Beispiel werden Nachrichten zurückgegeben, die einen bestimmten Ausdruck im Feld Subject enthalten.
  
```
SearchQuery 'subject:"MAIL_BOX VALIDATION/UPGRADE!!!"' 
```

In diesem Beispiel werden Nachrichten zurückgegeben, die innerhalb des angegebenen Datumsbereich gesendet wurden.
  
```
SearchQuery 'sent>=06/01/2016 AND sent<=09/01/2016'
```
 
In diesem Beispiel werden Nachrichten zurückgegeben, die an die angegebene Person gesendet wurden.

```
SearchQuery 'to:garthf@alpinehouse.com'
```
   
### <a name="verify-that-items-were-deleted"></a>Überprüfen, ob Elemente gelöscht wurden

Um zu überprüfen, ob Sie Elemente erfolgreich aus dem Ordner "Wiederherstellbare Elemente" eines Postfachs gelöscht haben, verwenden Sie das Cmdlet **Get-MailboxFolderStatistics** in Exchange Online PowerShell, um die Größe und Anzahl der Elemente im Ordner "Wiederherstellbare Elemente" zu überprüfen. Sie können diese Statistiken mit den in Schritt 1 gesammelten vergleichen. 
  
Führen Sie den folgenden Befehl in aus, um die aktuelle Größe und Gesamtanzahl von Elementen in Ordnern und Unterordnern im Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers abzurufen. 
  
```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
   
Führen Sie den folgenden Befehl aus, um die Größe und die Gesamtanzahl von Elementen in Ordnern und Unterordnern im Ordner "Wiederherstellbare Elemente" im Archivpostfach des Benutzers abzurufen. 

```
Get-MailboxFolderStatistics <username> -FolderScope RecoverableItems -Archive | FL Name,FolderAndSubfolderSize,ItemsInFolderAndSubfolders
```
  
## <a name="step-6-revert-the-mailbox-to-its-previous-state"></a>Schritt 6: Zurücksetzen des Postfachs in den vorherigen Zustand

Der letzte Schritt besteht darin, das Postfach wieder auf die vorherige Konfiguration zurückzusetzen. Dies ist das Zurücksetzen der Eigenschaften, die Sie in Schritt 2 geändert haben, und erneutes Anwenden der haltebereiche, die Sie in Schritt 3 entfernt haben. Dies umfasst Folgendes:
  
- Ändern des Aufbewahrungszeitraums für gelöschte Elemente wieder auf den vorherigen Wert. Alternativ können Sie diese Einstellung nur auf 30 Tage festlegen, den Maximalwert in Exchange Online.
    
- Wieder aktivieren der Wiederherstellung einzelner Elemente.
    
- Erneutes Aktivieren der Clientzugriffsmethoden, damit der Besitzer auf sein Postfach zugreifen kann.
    
- Erneutes Anwenden der Speicher-und Office 365-Aufbewahrungsrichtlinien, die Sie entfernt haben.
    
- Erneutes Aktivieren des Assistenten für verwaltete Ordner zur Verarbeitung des Postfachs.
    
> [!IMPORTANT]
> Es wird empfohlen, dass Sie 24 Stunden nach der erneuten Anwendung einer Aufbewahrungs-oder Office 365-Speicherrichtlinie warten, bevor Sie den Assistenten für verwaltete Ordner erneut aktivieren, um das Postfach zu verarbeiten. 
  
Führen Sie die folgenden Schritte (in der angegebenen Reihenfolge) in Exchange Online PowerShell aus.
  
1. Führen Sie den folgenden Befehl aus, um den Aufbewahrungszeitraum für gelöschte Elemente wieder auf den ursprünglichen Wert zu ändern. Dabei wird davon ausgegangen, dass die vorherige Einstellung weniger als 30 Tage beträgt; Beispiel: 14 Tage. 
    
    ```
    Set-Mailbox <username> -RetainDeletedItemsFor 14
    ```
   
2. Führen Sie den folgenden Befehl aus, um die Wiederherstellung einzelner Elemente wieder zu aktivieren.
   
    ```
    Set-Mailbox <username> -SingleItemRecoveryEnabled $true
    ```

3. Führen Sie den folgenden Befehl aus, um alle Clientzugriffsmethoden für das Postfach erneut zu aktivieren.
    
    ```
    Set-CASMailbox <username> -EwsEnabled $true -ActiveSyncEnabled $true -MAPIEnabled $true -OWAEnabled $true -ImapEnabled $true -PopEnabled $true
    ```
   
4. Wenden Sie die in Schritt 3 entfernten haltebereiche erneut an. Verwenden Sie je nach Aufbewahrungs eines der folgenden Verfahren.
    
    **Aufbewahrung für eventuelle Rechtsstreitigkeiten**
    
    Führen Sie den folgenden Befehl aus, um die Beweissicherung für das Postfach erneut zu aktivieren.
    
    ```
    Set-Mailbox <username> -LitigationHoldEnabled $true
    ```

    **In-Place Hold**
    
    Verwenden Sie die EAC (oder Exchange Online PowerShell), um das Postfach wieder dem in-situ-Speicher hinzuzufügen. 
    
    **Office 365-Aufbewahrungsrichtlinien, die auf bestimmte Postfächer angewendet werden**
    
    Verwenden Sie das &amp; Security Compliance Center, um das Postfach der Office 365-Aufbewahrungsrichtlinie wieder hinzuzufügen. Wechseln Sie zur Seite Aufbewahrungs **Zeit der Datenverwaltung** \> **** im Security &amp; Compliance Center, bearbeiten Sie die Aufbewahrungsrichtlinie, und fügen Sie das Postfach zurück zur Liste der Empfänger, auf die die Aufbewahrungsrichtlinie angewendet wird. 
    
    **Organisationsweite Office 365-Aufbewahrungsrichtlinien**
    
    Wenn Sie eine organisationsweite oder Exchange-weite Aufbewahrungsrichtlinie entfernt haben, indem Sie Sie aus der Richtlinie ausschließen, &amp; verwenden Sie das Security Compliance Center, um das Postfach aus der Liste der ausgeschlossenen Benutzer zu entfernen. Wechseln Sie im &amp; Security Compliance Center zur Seite Aufbewahrungszeit der **Datenverwaltung** \> **** , bearbeiten Sie die organisationsweite Aufbewahrungsrichtlinie, und entfernen Sie das Postfach aus der Liste der ausgeschlossenen Empfänger. Auf diese Weise wird die Aufbewahrungsrichtlinie erneut auf das Postfach des Benutzers angewendet. 
    
    **eDiscovery-Fall enthält**
    
    Verwenden Sie das &amp; Security Compliance Center, um das Postfach mit einem eDiscovery-Fall zu versehen. Wechseln Sie im &amp; Security Compliance Center zur **eDiscovery** -Seite für die ** &amp; Such Untersuchung** \> , öffnen Sie den Fall, und fügen Sie das Postfach wieder in den Haltebereich ein. 
    
5. Führen Sie den folgenden Befehl aus, damit der Assistent für verwaltete Ordner das Postfach erneut verarbeiten kann. Wie bereits erwähnt, empfiehlt es sich, dass Sie 24 Stunden nach der erneuten Anwendung eines haltebereichs oder einer Office 365-Aufbewahrungsrichtlinie warten, bevor Sie den Assistenten für verwaltete Ordner erneut aktivieren. 

    ```
    Set-Mailbox <username> -ElcProcessingDisabled $false
    ```
   
6. Um zu überprüfen, ob das Postfach wieder auf die vorherige Konfiguration zurückgesetzt wurde, können Sie die folgenden Befehle ausführen und die Einstellungen dann mit denjenigen vergleichen, die Sie in Schritt 1 gesammelt haben.

    ```
    Get-Mailbox <username> | FL ElcProcessingDisabled,InPlaceHolds,LitigationHoldEnabled,RetainDeletedItemsFor,SingleItemRecoveryEnabled
    ```

    ```
    Get-CASMailbox <username> | FL EwsEnabled,ActiveSyncEnabled,MAPIEnabled,OWAEnabled,ImapEnabled,PopEnabled
    ```
  
## <a name="more-information"></a>Weitere Informationen

Im folgenden finden Sie eine Tabelle, in der beschrieben wird, wie unterschiedliche Aufbewahrungs Typen basierend auf den Werten in der *InPlaceHolds* -Eigenschaft identifiziert werden, wenn Sie die Cmdlets **Get-Mailbox** oder **Get-OrganizationConfig** ausführen. Ausführlichere Informationen finden Sie unter [Vorgehensweise beim Identifizieren des Aufbewahrungs Typs für ein Exchange Online-Postfach](identify-a-hold-on-an-exchange-online-mailbox.md).

Wie bereits erläutert, müssen Sie alle Haltestatus-und Office 365-Aufbewahrungsrichtlinien aus einem Postfach entfernen, bevor Sie Elemente im Ordner "Wiederherstellbare Elemente" erfolgreich löschen können. 
  
|**Haltebereichstyp**|**Beispielwert**|**So identifizieren Sie den Haltestatus**|
|:-----|:-----|:-----|
|Beweissicherungsverfahren  <br/> | `True` <br/> |Die  *LitigationHoldEnabled*  -Eigenschaft wird festgelegt auf  `True`.  <br/> |
|Compliance-Archiv  <br/> | `c0ba3ce811b6432a8751430937152491` <br/> |Die *InPlaceHolds* -Eigenschaft enthält die GUID des in-situ-Speichers, der für das Postfach platziert wird. Sie können feststellen, dass dies ein in-situ-Speicher ist, da die GUID nicht mit einem Präfix beginnt.  <br/> Sie können den `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` Befehl in Exchange Online PowerShell verwenden, um Informationen zum in-situ-Speicher für das Postfach abzurufen.  <br/> |
| Office 365-Aufbewahrungsrichtlinien im &amp; Security Compliance Center, die auf bestimmte Postfächer angewendet werden  <br/> | `mbxcdbbb86ce60342489bff371876e7f224` <br/> oder  <br/>  `skp127d7cf1076947929bf136b7a2a8c36f` <br/> |Wenn Sie das Cmdlet **Get-Mailbox** ausführen, enthält die *InPlaceHolds* -Eigenschaft auch guids von Office 365-Aufbewahrungsrichtlinien, die auf das Postfach angewendet werden. Sie können Aufbewahrungsrichtlinien identifizieren, da die GUID mit `mbx` dem Präfix beginnt. Wenn die GUID der Aufbewahrungsrichtlinie mit dem `skp` Präfix beginnt, bedeutet dies, dass die Aufbewahrungsrichtlinie auf Skype for Business-Unterhaltungen angewendet wird.  <br/> Führen Sie den folgenden Befehl in Security &amp; Compliance Center PowerShell aus, um die Office 365-Aufbewahrungsrichtlinie zu identifizieren, die auf das Postfach angewendet wird: <br/> <br/>`Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>Entfernen Sie die Präfix  `mbx` oder  `skp`, wenn Sie diesen Befehl ausführen.  <br/> |
|Organisationsweite Office 365-Aufbewahrungsrichtlinien im Security &amp; Compliance Center  <br/> |Kein Wert  <br/> oder  <br/>  `-mbxe9b52bf7ab3b46a286308ecb29624696`(gibt an, dass das Postfach von einer organisationsweiten Richtlinie ausgeschlossen ist)  <br/> |Auch wenn die *InPlaceHolds* -Eigenschaft beim Ausführen des Cmdlets **Get-Mailbox** leer ist, gibt es möglicherweise noch eine oder mehrere organisationsweite Office 365-Aufbewahrungsrichtlinien, die auf das Postfach angewendet werden.  <br/> Um dies zu überprüfen, können Sie `Get-OrganizationConfig | FL InPlaceHolds` den Befehl in Exchange Online PowerShell ausführen, um eine Liste der GUIDs für organisationsweite Office 365-Aufbewahrungsrichtlinien abzurufen. Die GUID für organisationsweite Aufbewahrungsrichtlinien, die auf Exchange-Postfächer `mbx` angewendet werden, beginnen mit dem Präfix; Beispiel `mbxa3056bb15562480fadb46ce523ff7b02`.  <br/> Führen Sie den folgenden Befehl in Security &amp; Compliance Center PowerShell aus, um die organisationsweite Office 365-Aufbewahrungsrichtlinie zu identifizieren, die auf das Postfach angewendet wird: <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>Beachten Sie, dass, wenn ein Postfach von einer organisationsweiten Office 365-Aufbewahrungsrichtlinie ausgeschlossen wird, die GUID für die Aufbewahrungsrichtlinie in der *InPlaceHolds* -Eigenschaft des Postfachs des Benutzers angezeigt wird, wenn Sie das Cmdlet **Get-Mailbox** ausführen. Es wird durch das Präfix `-mbx`identifiziert; Zum Beispiel`-mbxe9b52bf7ab3b46a286308ecb29624696` <br/> |
|eDiscovery-Fall in der Security &amp; Compliance Center  <br/> | `UniH7d895d48-7e23-4a8d-8346-533c3beac15d` <br/> |Die *InPlaceHolds* -Eigenschaft enthält auch die GUID aller Haltestatus, der einem eDiscovery-Fall im &amp; Security Compliance Center zugeordnet ist, der möglicherweise im Postfach gespeichert wird. Sie können erkennen, dass es sich hierbei um einen eDiscovery-Fall handelt, da die GUID mit dem Präfix  `UniH` beginnt.  <br/> Sie können das `Get-CaseHoldPolicy` Cmdlet im Security &amp; Compliance Center PowerShell verwenden, um Informationen über den eDiscovery-Fall abzurufen, dem das Postfach zugeordnet ist. Beispielsweise können Sie den Befehl `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` ausführen, um den Namen der Groß-/Kleinschreibung im Postfach anzuzeigen. Be sure to remove the  `UniH`, wenn Sie diesen Befehl ausführen.  <br/><br/> Führen Sie die folgenden Befehle aus, um den eDiscovery-Fall zu identifizieren, dem das Postfach zugeordnet ist:<br/><br/>`$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/>`Get-ComplianceCase $CaseHold.CaseId | FL Name`


