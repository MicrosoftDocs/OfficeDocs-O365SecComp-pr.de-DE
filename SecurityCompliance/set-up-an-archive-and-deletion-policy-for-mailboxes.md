---
title: Richten Sie ein Archiv und Löschung Richtlinie für Postfächer in Ihrer Organisation Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/9/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MBS150
- BCS160
ms.assetid: ec3587e4-7b4a-40fb-8fb8-8aa05aeae2ce
description: Erstellen Sie eine Richtlinie Archivierung und Löschung in Office 365, die automatisch Elemente zum Archivpostfach des Benutzers verschoben wird.
ms.openlocfilehash: 740164ee840a32aff20f5c2dc1b1ae433d95cfe5
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522296"
---
# <a name="set-up-an-archive-and-deletion-policy-for-mailboxes-in-your-office-365-organization"></a>Richten Sie ein Archiv und Löschung Richtlinie für Postfächer in Ihrer Organisation Office 365

 **Dieser Artikel ist für Administratoren. Archiv-und Aufbewahrungsrichtlinien Elemente in Ihrem Postfach hinzufügen möchten? Finden Sie unter [zuweisen Aufbewahrungsrichtlinie für e-Mail-Nachrichten](https://support.office.com/article/3e5fd2dc-633f-4a38-b313-b31b81f7cf7a) | [Aufbewahrungs- und Archivierungsrichtlinien in Outlook im Web für Unternehmen](https://support.office.com/article/465372e4-e16b-47db-bee0-aba44799085e)**
  
In Office 365 können Sie eine Richtlinie Archivierung und Löschung erstellen, die automatisch Verschiebt Elemente in Archivpostfach des Benutzers und werden automatisch Elemente aus dem Postfach gelöscht. Hierzu können Sie eine Aufbewahrungsrichtlinie zu erstellen, die "s zugewiesen Postfächer und Elemente zum Archivpostfach des Benutzers wechselt, nachdem eine bestimmte Zeitspanne und, auch löscht Elemente aus dem Postfach, nachdem sie eine bestimmte Verfallszeit erreichen. Die tatsächlichen Regeln, die bestimmen, welche Elemente verschoben oder gelöscht werden und in diesem Fall aufgerufene aufbewahrungstags werden. Aufbewahrungstags werden einer Aufbewahrungsrichtlinie verknüpft, die wiederum dem Postfach eines Benutzers zugewiesen wird. Ein aufbewahrungstag gilt beibehaltungseinstellungen für einzelne Nachrichten und Ordnern im Postfach des Benutzers an. Es definiert, wie lange eine Nachricht im Postfach verbleibt und welche Aktion ausgeführt wird, wenn die Meldung die angegebenen Aufbewahrungszeitraum erreicht. Wenn eine Nachricht den Aufbewahrungszeitraum erreicht, entweder auf das Postfach des Benutzers Archiv verschoben wird, oder wird gelöscht. 
  
Die Schritte in diesem Thema werden eine Richtlinie Archivierung und Aufbewahrung für einen fiktiven Organisation mit dem Namen Alpine House eingerichtet. Einrichten von dieser Richtlinie umfasst die folgenden Aufgaben:
  
- Aktivieren eines archivpostfachs für jeden Benutzer in der Organisation. Dies ermöglicht es den Benutzern Postfachspeicher hinzufügen, und ist erforderlich, damit eine Aufbewahrungsrichtlinie Elemente in das Archivpostfach verschoben werden kann. Es Elemente wir auch eine Archivierung Store Benutzerinformationen durch Verschieben in ihre Archivpostfach. 
    
- Erstellen von drei benutzerdefinierte Retention Tags, die die folgenden Aktionen aus: 
    
  - Automatisch Verschiebt Elemente, die 3 Jahre Archivpostfach des Benutzers sind. Verschieben von Elementen in das Archivpostfach Freigabe von Speicherplatz im primären Postfach eines Benutzers.
    
  - Auf Elemente mit fünf Jahren aus dem Ordner Gelöschte Elemente werden automatisch gelöscht. Dies setzt auch Speicherplatz im primären Postfach des Benutzers. Des Benutzers wird die Möglichkeit, diese Elemente bei Bedarf wiederhergestellt haben. Siehe die Fußnote im Abschnitt [Weitere Informationen](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) für weitere Details. 
    
  - Automatisch (und dauerhaft) werden die Elemente, die aus der primären 7 Jahre und Archivpostfach sind gelöscht. Einige Unternehmen müssen aufgrund von Vorschriften e-Mail für einen bestimmten Zeitraum beibehalten. Nach Ablauf dieses Zeitraums möglicherweise eine Organisation diese Benutzerpostfächer Elemente dauerhaft entfernen möchten. 
    
- Erstellen einer neuen Aufbewahrungsrichtlinie, und die neue benutzerdefinierte aufbewahrungstags hinzugefügt. Darüber hinaus fügen Sie integrierte aufbewahrungstags auch auf die neue Aufbewahrungsrichtlinie. Dazu gehören persönliche Tags, die Benutzer Elemente in ihrem Postfach zuweisen können. Sie können auch ein aufbewahrungstag hinzufügen, die Elemente aus dem Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner wiederherstellbare Elemente in ihrem Archivpostfach verschoben. Auf diese Weise können Geben Sie Speicherplatz in den Ordner eines Benutzers wiederherstellbare Elemente, wenn ihr Postfach in der Warteschleife platziert wird.
    
Führen Sie einige oder alle Schritte in diesem Artikel können Sie ein Archiv und Löschung Richtlinie für Postfächer in Ihrer Organisation einrichten. Es wird empfohlen, diesen Vorgang für einige Postfächer testen, bevor es für alle Postfächer in Ihrer Organisation zu implementieren.
  
## <a name="before-you-begin"></a>Vorbemerkung

- Sie müssen ein globaler Administrator in Office 365-Organisation zum Ausführen der Schritte in diesem Thema werden. 
    
-  Wenn Sie ein neues Benutzerkonto in Office 365 erstellen und weisen Sie dem Benutzer eine Lizenz Exchange Online, wird automatisch ein Postfach für den Benutzer erstellt. Wenn das Postfach erstellt wird, hat diese eine Standardaufbewahrungsrichtlinie, mit dem Namen MRM-Standardrichtlinie automatisch zugewiesen. In diesem Artikel erstellen eine neuen Aufbewahrungsrichtlinie und weisen Sie es dann auf die Benutzerpostfächer, ersetzen die Standard-MRM-Richtlinie. Ein Postfach kann nur eine Aufbewahrungsrichtlinie jeweils zugewiesen haben.
    
- Finden Sie weitere Informationen zu aufbewahrungstags und Aufbewahrungsrichtlinien in Exchange Online finden Sie unter [aufbewahrungstags und Aufbewahrungsrichtlinien](https://go.microsoft.com/fwlink/p/?LinkId=404424).
    
## <a name="step-1-enable-archive-mailboxes-for-users"></a>Schritt 1: Aktivieren von archivpostfächern für Benutzer

Der erste Schritt ist das Archivpostfach für jeden Benutzer in Ihrer Organisation zu aktivieren. Archivpostfach des Benutzers muss aktiviert sein, damit ein aufbewahrungstag mit einem "verschieben" Retention ins Archiv das Element verschoben werden kann, nachdem der Aufbewahrungszeitraum abgelaufen ist. 
  
> [!NOTE]
> Archivpostfächer können jederzeit während dieses Vorgangs Sie einfach, solange sie zu einem bestimmten Zeitpunkt aktiviert sind, bevor Sie den Vorgang abzuschließen. Wenn ein Archivpostfach nicht aktiviert ist, wird keine Aktion auf alle Elemente ausgeführt, die ein Archivrichtlinie zugewiesen haben. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit Ihrer globalen Administratorkonto an.
    
    
3. In das Wertpapier &amp; Compliance Center, navigieren Sie zur **Steuerung der Daten** \> **Archiv**.
    
    Eine Liste der Postfächer in Ihrer Organisation wird angezeigt und gibt an, ob das entsprechende Archivpostfach aktiviert oder deaktiviert ist. 
    
4. Wählen Sie alle Postfächer auf dem ersten in der Liste die **UMSCHALTTASTE** gedrückt, und klicken Sie dann auf das letzte Element in der Liste aus. 
    
    > [!TIP]
    > In diesem Schritt wird davon ausgegangen, dass keine archivpostfächer aktiviert sind. Wenn Sie alle Postfächer mit dem Archiv aktiviert haben, halten Sie die **STRG** -Taste gedrückt, und klicken Sie auf jedem Postfach, für ein Archivpostfach deaktiviert ist. Oder Sie können auf die Spaltenüberschrift **Archivpostfach** zum Sortieren der Zeilen basierend auf gibt an, ob das Archivpostfach aktiviert oder deaktiviert, um Postfächer auszuwählen erleichtern. 
  
5. Klicken Sie im Detailbereich unter **Massenbearbeitung**auf **Aktivieren**.
    
    Eine Warnung wird angezeigt, die besagt, dass Elemente, die älter als zwei Jahre sind in das neue Archivpostfach verschoben werden sollen. Dies ist, da die Standardrichtlinie für die Aufbewahrung, die ein neues Benutzerpostfach zugewiesen hat, bei der Erstellung ein Archiv Richtlinie Standardtag verfügt, die ein Aufbewahrungszeitraum 2 Jahre hat. Das Archiv der benutzerdefinierten Richtlinie Standardtag, das Sie in Schritt2 erstellen, verfügt über eine Aufbewahrungszeitraum von 3 Jahren. Das bedeutet, dass Elemente, die 3 Jahren sind oder älter wird in das Archivpostfach verschoben werden.
    
6. Klicken Sie auf **Ja** , um die Warnmeldung zu schließen, und starten Sie den Vorgang, um das Archivpostfach für jedes ausgewählten Postfach zu aktivieren. 
    
7. Klicken Sie auf **Aktualisieren** , wenn der Vorgang abgeschlossen ist, ![aktualisieren](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) zum Aktualisieren der Liste auf der Seite **Archiv** . 
    
    Das Archivpostfach ist für alle Benutzer in Ihrer Organisation aktiviert.
    
    ![Die Liste der Postfächer mit das Archivpostfach aktiviert](media/61a7cb97-1bed-4808-aa5f-b6b761cfa8de.png)
  
8. Lassen Sie die Sicherheit &amp; Compliance Center öffnen. Im nächsten Schritt verwenden Sie es.
    
## <a name="step-2-create-new-retention-tags-for-the-archive-and-deletion-policies"></a>Schritt 2: Erstellen von neuen aufbewahrungstags für die Archivierung und Löschung Richtlinien

In diesem Schritt erstellen Sie die drei benutzerdefinierte aufbewahrungstags, die weiter oben beschrieben wurden.
  
- Alpine House 3 Jahr in Archiv verschieben (benutzerdefinierte Archivrichtlinie)
    
- Alpine House 7 Jahr endgültig löschen (benutzerdefinierte Löschung Policy)
    
- Alpine House gelöschte Elemente, 5 Jahre löschen und Wiederherstellung zulassen (benutzerdefinierte Tags für den Ordner Gelöschte Objekte)
    
Um neue aufbewahrungstags zu erstellen, verwenden Sie die Exchange-Verwaltungskonsole (EAC) in Ihrer Exchange Online-Organisation.
  
1. In das Wertpapier &amp; Compliance Center, klicken Sie auf der app in der oberen linken Ecke, und klicken Sie dann auf die Kachel " **Admin** ". 
    
2. Klicken Sie auf **Admin zentriert**im linken Navigationsbereich des Office 365 Administrationscenter, und klicken Sie dann auf **Exchange**.
    
    ![Screenshot shows the Office 365 admin center with the Admin centers option expanded and Exchange selected.](media/47399df2-0bc4-42e2-b183-07750a46bc68.png)
  
3. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Verwaltung der Richtlinientreue** \> **aufbewahrungstags**
    
    Es wird eine Liste der Retention Tags für Ihre Organisation angezeigt.
    
### <a name="create-a-custom-archive-default-policy-tag"></a>Erstellen einer benutzerdefinierten Archiv Richtlinie Standardtag
  
Zuerst erstellen Sie ein benutzerdefiniertes Archiv Standard-Richtlinie Tag (DPT), die Elemente nach 3 Jahren in das Archivpostfach verschoben werden. 
  
1. Klicken Sie auf der Seite **aufbewahrungstags** auf **Neues Tag**![New Icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), und wählen Sie dann **auf gesamte Postfach (Standard) automatisch angewendet**. 
    
2. Füllen Sie auf der Seite **Neues Tag automatisch auf die gesamte Postfach (Standard) angewendet** die folgenden Felder aus: 
    
    ![Einstellungen zum Erstellen einer neuen Archiv Richtlinie Standardtag](media/41c0a43c-9c72-44e0-8947-da0831896432.png)
  
1. **Name** Geben Sie einen Namen für die neue aufbewahrungstag. 
    
2. **Aufbewahrungsaktion** Wählen Sie aus, **in Archiv verschieben** , Elemente in das Archivpostfach verschieben, wenn der Aufbewahrungszeitraum abgelaufen ist. 
    
3. **Aufbewahrungszeitraum** Wählen Sie aus, **Wenn das Element das folgende Alter (in Tagen) erreicht**, und geben Sie die Dauer des Aufbewahrungszeitraums. In diesem Szenario werden Elemente nach 1095 Tagen (in 3 Jahren) in das Archivpostfach verschoben.
    
4. **Kommentar** (Optional) Geben Sie einen Kommentar, der den Zweck des benutzerdefinierten Retention Tags erläutert. 
    
3. Klicken Sie auf **Speichern** , um das Archiv der benutzerdefinierten DPT erstellen. 
    
    Die neue Archiv DPT wird in der Liste der aufbewahrungstags angezeigt.
    
### <a name="create-a-custom-deletion-default-policy-tag"></a>Erstellen einer benutzerdefinierten Löschung Richtlinie Standardtag
  
Im nächsten Schritt erstellen Sie eine andere benutzerdefinierte DPT, aber diese wird eine Löschung-Richtlinie, die Elemente nach 7 Jahren dauerhaft gelöscht werden.
  
1. Klicken Sie auf der Seite **aufbewahrungstags** auf **Neues Tag**![New Icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), und wählen Sie dann **auf gesamte Postfach (Standard) automatisch angewendet**. 
    
2. Füllen Sie auf der Seite **Neues Tag automatisch auf die gesamte Postfach (Standard) angewendet** die folgenden Felder aus: 
    
    ![Einstellungen zum Erstellen einer neuen Standardtag Richtlinie löschen](media/f1f0ff62-eec9-4824-8e7c-d93dcfb09a79.png)
  
1. **Name** Geben Sie einen Namen für die neue aufbewahrungstag. 
    
2. **Aufbewahrungsaktion** Wählen Sie **Endgültig löschen** , um Elemente aus dem Postfach löschen, wenn der Aufbewahrungszeitraum abgelaufen ist. 
    
3. **Aufbewahrungszeitraum** Wählen Sie aus, **Wenn das Element das folgende Alter (in Tagen) erreicht**, und geben Sie die Dauer des Aufbewahrungszeitraums. In diesem Szenario werden nach 2555 Tagen (7 Jahre) Elemente gelöscht werden.
    
4. **Kommentar** (Optional) Geben Sie einen Kommentar, der den Zweck des benutzerdefinierten Retention Tags erläutert. 
    
3. Klicken Sie auf **Speichern** , um den benutzerdefinierten Löschvorgang DPT erstellen. 
    
    Die neue Löschung DPT wird in der Liste der aufbewahrungstags angezeigt.
    
### <a name="create-a-custom-retention-policy-tag-for-the-deleted-items-folder"></a>Erstellen einer benutzerdefinierten Aufbewahrungsrichtlinien-Tag für den Ordner Gelöschte Elemente
  
Das letzte aufbewahrungstag, das Sie erstellen, ist eine benutzerdefinierte Aufbewahrungsrichtlinien-Tag (außer) für den Ordner Gelöschte Objekte. Dieses Tag Löschen von Elementen im Ordner "Gelöschte Elemente" wird nach fünf Jahren und bietet einen Zeitraum für die Wiederherstellung Wenn Benutzer das gelöschte Elemente wiederherstellen-Tool zum Wiederherstellen eines Elements verwenden können.
  
1. Klicken Sie auf der Seite **aufbewahrungstags** auf **Neues Tag** ![New Icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), und wählen Sie dann **auf einen Standardordner automatisch angewendet**. 
    
2. Füllen Sie auf der Seite **Neues Tag automatisch auf einen Standardordner angewendet** die folgenden Felder aus: 
    
    ![Einstellungen zum Erstellen eines neuen Aufbewahrungsrichtlinien-Tags für den Ordner Gelöschte Elemente](media/6f3104bd-5edb-48ac-884d-5fe13d81dd1d.png)
  
1. **Name** Geben Sie einen Namen für die neue aufbewahrungstag. 
    
2. **Dieses Tag in den folgenden Standardordner übernehmen** Wählen Sie in der Dropdown-Liste **Gelöschte Elemente**.
    
3. **Aufbewahrungsaktion** Wählen Sie **Löschen und Wiederherstellung zulassen** Elemente löschen, wenn der Aufbewahrungszeitraum abgelaufen ist, aber zulassen, Benutzer ein gelöschtes Element innerhalb der Aufbewahrungszeit für gelöschte Elemente wiederherstellen dass (die standardmäßig 14 Tage ist). 
    
4. **Aufbewahrungszeitraum** Wählen Sie aus, **Wenn das Element das folgende Alter (in Tagen) erreicht**, und geben Sie die Dauer des Aufbewahrungszeitraums. In diesem Szenario werden Elemente nach 1825 Tagen (5 Jahre) gelöscht.
    
5. **Kommentar** (Optional) Geben Sie einen Kommentar, der den Zweck des benutzerdefinierten Retention Tags erläutert. 
    
3. Klicken Sie auf **Speichern** , um die benutzerdefinierten Aufbewahrungsrichtlinientag für den Ordner Gelöschte Objekte zu erstellen. 
    
    Die neue Berichtskopf wird in der Liste der aufbewahrungstags angezeigt.

## <a name="step-3-create-a-new-retention-policy"></a>Schritt 3: Erstellen einer neuen Aufbewahrungsrichtlinie

Nachdem die benutzerdefinierte aufbewahrungstags erstellt wurde, besteht der nächste Schritt zum Erstellen einer neuen Aufbewahrungsrichtlinie und die aufbewahrungstags hinzufügen. Sie fügen die drei benutzerdefinierte aufbewahrungstags, die Sie in Schritt2 erstellt haben, und die integrierten Tags, die im ersten Abschnitt erwähnt wurden. In Schritt 4 werden Sie diese neue Aufbewahrungsrichtlinie auf Benutzerpostfächer zuweisen.
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Verwaltung der Richtlinientreue** \> **Aufbewahrungsrichtlinien**.
    
2. Klicken Sie auf der Seite **Aufbewahrungsrichtlinien** auf **neu** ![New Icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif).
    
3. Geben Sie im Feld **Name** einen Namen für die neue Aufbewahrungsrichtlinie; beispielsweise **Alpine House-Archivierung und Löschung**. 
    
4. Klicken Sie auf **Hinzufügen** , klicken Sie unter **Retention Tags**, ![New Icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif).
    
    Es wird eine Liste der Retention Tags in Ihrer Organisation angezeigt. Beachten Sie, dass der benutzerdefinierte Tags, die Sie in Schritt2 erstellt haben, angezeigt werden.
    
5. Fügen Sie die 9 Retention Tags, die hervorgehoben sind im folgenden Screenshot (diese Tags werden ausführlich im Abschnitt [Weitere Informationen](set-up-an-archive-and-deletion-policy-for-mailboxes.md#moreinfo) beschrieben). Um ein aufbewahrungstag hinzuzufügen, wählen Sie sie aus, und klicken Sie dann auf **Hinzufügen**. 
    
    ![Die neue Aufbewahrungsrichtlinie Retention Tags hinzufügen](media/d8e87176-0716-4238-9e6a-7c4af35541dc.png)
  
    > [!TIP]
    > Sie können mehrere aufbewahrungstags auswählen, indem Sie die **STRG** -Taste gedrückt halten und dann auf jedes Tag. 
  
6. Nachdem Sie die aufbewahrungstags hinzugefügt haben, klicken Sie auf **OK**.
    
7. Klicken Sie auf der Seite **Neue Aufbewahrungsrichtlinie** auf **Speichern** , um die neue Richtlinie erstellen. 
    
    Die neue Aufbewahrungsrichtlinie wird in der Liste angezeigt. Wählen Sie aus, um die aufbewahrungstags verknüpften im Detailbereich anzuzeigen.
    
    ![Die neue Aufbewahrungsrichtlinie und die Liste der verknüpfte aufbewahrungstags](media/63bc45e6-110b-4dc9-a85f-8eb1961a8258.png)
  
## <a name="step-4-assign-the-new-retention-policy-to-user-mailboxes"></a>Schritt 4: Zuweisen von Benutzerpostfächern in die neue Aufbewahrungsrichtlinie

Wenn ein neues Postfach erstellt wird, wird eine Aufbewahrungsrichtlinie mit dem Namen Standard-MRM-Standardrichtlinie es standardmäßig zugewiesen. In diesem Schritt werden Sie diese Aufbewahrungsrichtlinie ersetzen (, da ein Postfach nur eine Aufbewahrungsrichtlinie zugewiesen werden kann) durch die neue Aufbewahrungsrichtlinie, die Sie in Schritt 3 auf die Benutzerpostfächer in Ihrer Organisation erstellt zuweisen. In diesem Schritt wird davon ausgegangen, dass die neue Richtlinie auf alle Postfächer in Ihrer Organisation zugewiesen werden.
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Empfänger** \> **Postfächer**.
    
    Es wird eine Liste aller Postfächer für Benutzer in Ihrer Organisation angezeigt. 
    
2. Wählen Sie alle Postfächer auf dem ersten in der Liste die **UMSCHALTTASTE** gedrückt, und klicken Sie dann auf das letzte Element in der Liste aus. 
    
3. Klicken Sie im Detailbereich auf der rechten Seite von der Exchange-Verwaltungskonsole unter **Massenbearbeitung**auf **Weitere Optionen**.
    
4. Klicken Sie unter **Aufbewahrungsrichtlinie** auf **Aktualisieren**.
    
5. Wählen Sie auf der Seite **Bulk zuweisen Aufbewahrungsrichtlinie** in der Dropdownliste **Wählen Sie die Aufbewahrungsrichtlinie** die Aufbewahrungsrichtlinie, die Sie in Schritt 3 erstellt; beispielsweise **Alpine House Archive und Aufbewahrungsrichtlinien**.
    
6. Klicken Sie auf **Speichern** , um die neue Retention Policy Zuweisung zu speichern. 
    
7. Um sicherzustellen, dass die neue Aufbewahrungsrichtlinie auf Postfächer zugewiesen wurde, können Sie die folgenden Aktionen ausführen: Wählen Sie ein Postfach auf der Seite Postfächer aus, und klicken Sie dann auf Bearbeiten. 
    
1. Wählen Sie ein Postfach auf der Seite **Postfächer** aus, und klicken Sie dann auf **Bearbeiten** ![bearbeiten](media/d7dc7e5f-17a1-4eb9-b42d-487db59e2e21.png). 
    
2. Klicken Sie auf der Eigenschaftenseite des Postfachs für den ausgewählten Benutzer die auf **Postfachfunktionen**.
    
    Der Name der neuen Richtlinie zugewiesen an das Postfach wird in der **Aufbewahrungsrichtlinie** Dropdown-Liste angezeigt. 
    

  
## <a name="optional-step-5-run-the-managed-folder-assistant-to-apply-the-new-settings"></a>(Optional) Schritt 5: Führen Sie den Assistenten für verwaltete Ordner, um die neuen Einstellungen anzuwenden
<a name="step3"> </a>

Nachdem Sie die neue Aufbewahrungsrichtlinie auf Postfächer in Schritt 4 anwenden, kann es bis zu sieben Tage in Exchange Online für die neue Einstellungen für die Aufbewahrung auf die Postfächer angewendet werden soll dauern. Dies ist, da ein Prozess der Assistenten für verwaltete Ordner Prozesse Postfächer einmal alle 7 Tage aufgerufen. Anstelle von Warten auf Assistenten für verwaltete Ordner ausführen, können Sie dies durch Ausführen des **Start-ManagedFolderAssistant-** Cmdlets in Exchange Online PowerShell erzwingen. 
  
 **Was geschieht, wenn Sie den Assistenten für verwaltete Ordner ausführen?** Es gilt die Einstellungen in der Aufbewahrungsrichtlinie, indem Prüfen von Elementen im Postfach und bestimmen, ob sie unterliegen Aufbewahrung sind. Es versieht klicken Sie dann mit der entsprechenden aufbewahrungstag Artikeln, für die Aufbewahrung und nimmt dann die angegebenen Aufbewahrungsaktion für Elemente nach deren Aufbewahrungszeitraum. 
  
Hier sind die Schritte zum Verbinden mit Exchange Online PowerShell, und führen Sie den Assistenten für verwaltete Ordner auf alle Postfächer in Ihrer Organisation.
  
1. Öffnen Sie auf Ihrem lokalen Computer Windows PowerShell, und führen Sie dann den folgenden Befehl aus.
    
    ```
    $UserCredential = Get-Credential
    ```

    Klicken Sie im Dialogfeld **Windows PowerShell anmelden** Geben Sie den Benutzernamen und das Kennwort für Ihr Office 365 globaler Administrator-Konto ein, und klicken Sie dann auf **OK**.
    
2. Führen Sie den folgenden Befehl aus.
    
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

    > [!NOTE]
    > Weitere Informationen oder Hinweise bei Problemen mit der Verbindung zu Ihrer Exchange Online-Organisation finden Sie unter [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283). 
  
5. Führen Sie die folgenden zwei Befehle aus, um den Assistenten für verwaltete Ordner für alle Benutzerpostfächer in Ihrer Organisation zu starten.
    
    ```
    $Mailboxes = Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"}
    ```

    ```
    $Mailboxes.Identity | Start-ManagedFolderAssistant
    ```

Das wars! Sie haben ein Archiv und Löschung Richtlinie für die Organisation Alpine House einrichten.
  
## <a name="more-information"></a>Weitere Informationen
<a name="moreinfo"> </a>

- Wie wird der Aufbewahrungszeitraum berechnet? Der Aufbewahrungszeitraum Postfachelemente aus dem Datum der Lieferung oder das Erstellungsdatum für Elemente wie Entwurf-Nachrichten, die gesendet werden nicht berechnet wird, aber vom Benutzer erstellt werden. Wenn die Assistenten für verwaltete Ordner Elemente in einem Postfach verarbeitet, stempelt sie ein Startdatum und ein Ablaufdatum für alle Elemente, die mit der Aufbewahrungsaktion löschen und Wiederherstellung zulassen oder endgültig löschen aufbewahrungstags aufweisen. Auf Elemente mit einem Tag Archiv werden mit einem Datum der Verschiebung versehen. 
    
- Die folgende Tabelle enthält weitere Informationen zu den einzelnen Retention Tags, die die benutzerdefinierten Aufbewahrungsrichtlinie hinzugefügt wird, die mithilfe der Schritte in diesem Thema erstellt wurde.
    
    |**Aufbewahrungstag**|**Funktionsweise dieses tag**|**Integrierte oder benutzerdefinierte?**|**Type**|
    |:-----|:-----|:-----|:-----|
    |3 Jahre, Alpine House in Archiv verschieben  <br/> |Verschiebt Elemente, die in das Archivpostfach alte 1095 Tage (in 3 Jahren) sind.  <br/> |Benutzerdefinierte (finden Sie unter [Schritt2: Erstellen von neuen aufbewahrungstags für die Archivierung und Löschung Richtlinien](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )  <br/> |Richtlinie Standardtag (Archiv); Dieses Tag wird automatisch auf das gesamte Postfach angewendet.  <br/> |
    |Alpine House 7 Jahr endgültig löschen  <br/> |Löscht Elemente in das primäre Postfach oder das Archivpostfach dauerhaft, wenn sie 7 Jahre alt sind.  <br/> |Benutzerdefinierte (finden Sie unter [Schritt2: Erstellen von neuen aufbewahrungstags für die Archivierung und Löschung Richtlinien](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )  <br/> |Richtlinie Standardtag (löschen); Dieses Tag wird automatisch auf das gesamte Postfach angewendet.  <br/> |
    |Alpine House gelöschte Elemente 5 Jahre löschen und Wiederherstellung zulassen  <br/> |Löscht Elemente aus dem Ordner Gelöschte Objekte, die 5 Jahre alt sind. Benutzer können diese Elemente für von 14 Tagen, nachdem sie gelöscht sind wiederherstellen.<sup>\*</sup> <br/> |Benutzerdefinierte (finden Sie unter [Schritt2: Erstellen von neuen aufbewahrungstags für die Archivierung und Löschung Richtlinien](set-up-an-archive-and-deletion-policy-for-mailboxes.md#step3) )  <br/> |Aufbewahrungsrichtlinien-Tag (Gelöschte Objekte); Dieses Tag wird automatisch auf Elemente im Ordner "Gelöschte Elemente" angewendet.  <br/> |
    |Wiederherstellbare Elemente, 14 Tage verschieben in Archiv  <br/> |Verschiebt Elemente, die im Ordner "wiederherstellbare Elemente" in den Ordner wiederherstellbare Elemente im Archivpostfach 14 Tagen wurden.  <br/> |Integriert  <br/> |Aufbewahrungsrichtlinien-Tag (wiederherstellbare Elemente); Dieses Tag wird automatisch auf Elemente im Ordner "wiederherstellbare Elemente" angewendet.  <br/> |
    |Junk-e-Mail  <br/> |Löscht dauerhaft Elemente, die in den Junk-e-Mail-Ordner für 30 Tage wurden. Benutzer können diese Elemente für von 14 Tagen, nachdem sie gelöscht sind wiederherstellen.<sup>\*</sup> <br/> |Integriert  <br/> |Aufbewahrungsrichtlinien-Tag (Junk-e); Dieses Tag wird automatisch auf Elemente in den Junk-e-Mail-Ordner angewendet.  <br/> |
    |1 Monat, löschen  <br/> |Löscht dauerhaft Elemente, die 30 Tage alt sind. Benutzer können diese Elemente für von 14 Tagen, nachdem sie gelöscht sind wiederherstellen.<sup>\*</sup> <br/> |Integriert  <br/> |Persönliche; Dieses Tag kann von Benutzern angewendet werden.  <br/> |
    |1 Jahr, löschen  <br/> |Löscht dauerhaft Elemente, die 365 Tage alt sind. Benutzer können diese Elemente für von 14 Tagen, nachdem sie gelöscht sind wiederherstellen.<sup>\*</sup> <br/> |Integriert  <br/> |Persönliche; Dieses Tag kann von Benutzern angewendet werden.  <br/> |
    |Nie löschen  <br/> |Dieses Tag verhindern, dass Elemente durch eine Aufbewahrungsrichtlinie gelöscht.  <br/> |Integriert  <br/> |Persönliche; Dieses Tag kann von Benutzern angewendet werden.  <br/> |
    |Persönlich, 1 Jahre, in Archiv verschieben  <br/> |Verschiebt Elemente in das Archivpostfach nach einem Jahr an.  <br/> |Integriert  <br/> |Persönliche; Dieses Tag kann von Benutzern angewendet werden.  <br/> |
   
    > <sup>\*</sup>Benutzer können das Tool gelöschte Elemente wiederherstellen in Outlook und Outlook Web App verwenden, um ein gelöschtes Element in die Aufbewahrungszeit für gelöschte Elemente wiederherstellen, die standardmäßig 14 Tage in Exchange Online ist. Ein Administrator kann Windows PowerShell verwenden, um die Aufbewahrungszeit auf ein Maximum von 30 Tagen zu erhöhen. Weitere Informationen finden Sie unter: [Wiederherstellen gelöschter Elemente in Outlook für Windows](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce) und [Änderung der Aufbewahrungszeit für ein Postfach in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940)
  
- Verwendet werden, die **wiederherstellbare Elemente, 14 Tage, in Archiv verschieben** Retention Tags wird freien Speicherplatz im Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers. Dies ist nützlich, wenn dem Postfach eines Benutzers in der Warteschleife, platziert wird, d. h., nothing jemals dauerhaft ist, das Postfach des Benutzers gelöscht. Ohne Elemente in das Archivpostfach verschieben, ist es möglich, das Speicherkontingent für den Ordner wiederherstellbare Elemente im Postfach primären erreicht wird. Weitere Informationen hierzu und wie Sie dies vermeiden finden Sie unter [Erhöhen der wiederherstellbare Elemente Kontingent für Postfächer auf halten](https://go.microsoft.com/fwlink/p/?LinkId=786479).
