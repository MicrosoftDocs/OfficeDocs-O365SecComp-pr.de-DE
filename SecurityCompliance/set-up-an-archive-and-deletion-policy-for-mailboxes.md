---
title: Einrichten einer Archivierungs-und Löschrichtlinie für Postfächer in Ihrer Office 365-Organisation
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
- MED150
- MBS150
- BCS160
ms.assetid: ec3587e4-7b4a-40fb-8fb8-8aa05aeae2ce
description: Erstellen Sie eine Archivierungs-und Löschrichtlinie in Office 365, die Elemente automatisch in das Archivpostfach eines Benutzers verschiebt.
ms.openlocfilehash: 87e155869c6740dd839c09e3e31e0cb819dc5d37
ms.sourcegitcommit: 54a2cbe5d13f448e0c28655bdf88deb9e5434cac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2019
ms.locfileid: "30935270"
---
# <a name="set-up-an-archive-and-deletion-policy-for-mailboxes-in-your-office-365-organization"></a>Einrichten einer Archivierungs-und Löschrichtlinie für Postfächer in Ihrer Office 365-Organisation

 In Office 365 können Administratoren eine Archivierungs-und Löschrichtlinie erstellen, die Elemente automatisch in das Archivpostfach eines Benutzers verschiebt und automatisch Elemente aus dem Postfach löscht. Hierzu erstellt der Administrator eine Aufbewahrungsrichtlinie, die Postfächern zugewiesen ist, und verschiebt Elemente nach einem bestimmten Zeitraum in das Archivpostfach eines Benutzers und löscht außerdem Elemente aus dem Postfach, nachdem Sie eine bestimmte Altersgrenze erreicht haben. Die tatsächlichen Regeln, die bestimmen, welche Elemente verschoben oder gelöscht werden, und wenn dies der Fall ist, werden als Aufbewahrungstags bezeichnet. Aufbewahrungstags sind mit einer Aufbewahrungsrichtlinie verknüpft, die wiederum dem Postfach eines Benutzers zugewiesen wird. Ein Aufbewahrungs wendet Aufbewahrungseinstellungen auf einzelne Nachrichten und Ordner im Postfach eines Benutzers an. Es definiert, wie lange eine Nachricht im Postfach verbleibt und welche Aktion ausgeführt wird, wenn die Nachricht das angegebene Aufbewahrungs Alter erreicht. Wenn eine Nachricht das Aufbewahrungs Alter erreicht, wird Sie entweder in das Archivpostfach des Benutzers verschoben oder gelöscht. 
  
Mit den Schritten in diesem Artikel wird eine Archivierungs-und Aufbewahrungsrichtlinie für eine fiktive Organisation namens "Alpine House" eingerichtet. Das Einrichten dieser Richtlinie umfasst die folgenden Aufgaben:
  
- Aktivieren eines Archivpostfachs für jeden Benutzer in der Organisation. Dadurch erhält der Benutzer zusätzlichen Postfachspeicher und ist erforderlich, damit eine Aufbewahrungsrichtlinie Elemente in das Archivpostfach verschieben kann. Außerdem können benutzerarchiv Informationen speichern, indem Sie Elemente in Ihr Archivpostfach bewegen. 
    
- Erstellen von drei benutzerdefinierten Aufbewahrungstags, die folgende Aufgaben ausführen: 
    
  - Verschiebt Elemente, die 3 Jahre alt sind, automatisch in das Archivpostfach des Benutzers. Das Verschieben von Elementen in das Archivpostfach gibt Speicherplatz im primären Postfach eines Benutzers frei.
    
  - Löscht Elemente, die 5 Jahre alt sind, automatisch aus dem Ordner "Gelöschte Elemente". Dadurch wird auch Speicherplatz im primären Postfach des Benutzers freigegeben. Die Benutzer haben die Möglichkeit, diese Elemente bei Bedarf wiederherzustellen. Weitere Informationen finden Sie in der Fußnote im Abschnitt [Weitere Informationen](#more-information) . 
    
  - Löscht Elemente, die 7 Jahre alt sind, automatisch (und dauerhaft) aus dem primären und dem Archivpostfach. Aufgrund von Compliance-Vorschriften müssen einige Organisationen e-Mails für einen bestimmten Zeitraum aufbewahren. Nach Ablauf dieses Zeitraums kann eine Organisation diese Elemente für Benutzerpostfächer dauerhaft entfernen. 
    
- Erstellen einer neuen Aufbewahrungsrichtlinie und Hinzufügen der neuen benutzerdefinierten Aufbewahrungstags. Darüber hinaus fügen Sie der neuen Aufbewahrungsrichtlinie auch integrierte Aufbewahrungstags hinzu. Dies umfasst persönliche Tags, die Benutzer Elementen in Ihrem Postfach zuweisen können. Außerdem fügen Sie ein Aufbewahrungs hinzu, mit dem Elemente aus dem Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner "Wiederherstellbare Elemente" im Archivpostfach verschoben werden. Dadurch wird der Speicherplatz im Ordner "Wiederherstellbare Elemente" eines Benutzers freigegeben.
    
Sie können einige oder alle Schritte in diesem Artikel ausführen, um eine Archiv-und Löschrichtlinie für Postfächer in ihrer eigenen Organisation einzurichten. Es wird empfohlen, diesen Prozess für einige Postfächer zu testen, bevor Sie ihn für alle Postfächer in Ihrer Organisation implementieren.
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation sein, um die Schritte in diesem Thema ausführen zu können. 
    
-  Wenn Sie in Office 365 ein neues Benutzerkonto erstellen und dem Benutzer eine Exchange Online-Lizenz zuweisen, wird automatisch ein Postfach für den Benutzer erstellt. Wenn das Postfach erstellt wird, wird ihm automatisch eine standardmäßige Aufbewahrungsrichtlinie namens "Default MRM Policy" zugewiesen. In diesem Artikel erstellen Sie eine neue Aufbewahrungsrichtlinie und weisen Sie dann den Benutzerpostfächern zu, wobei Sie die Standard-MRM-Richtlinie ersetzen. Einem Postfach kann jeweils nur eine Aufbewahrungsrichtlinie zugewiesen sein.
    
- Weitere Informationen zu Aufbewahrungstags und-Richtlinien in Exchange Online finden Sie unter [Aufbewahrungstags und](https://go.microsoft.com/fwlink/p/?LinkId=404424)Aufbewahrungsrichtlinien.
    
## <a name="step-1-enable-archive-mailboxes-for-users"></a>Schritt 1: Aktivieren von archivpostfächern für Benutzer

Der erste Schritt besteht darin, das Archivpostfach für jeden Benutzer in Ihrer Organisation zu aktivieren. Das Archivpostfach eines Benutzers muss aktiviert sein, damit ein Aufbewahrungs mit einer Aufbewahrungsaktion "in Archiv verschieben" das Element nach Ablauf des Aufbewahrungszeitraums verschieben kann. 
  
> [!NOTE]
> Sie können Archivpostfächer jederzeit während dieses Vorgangs aktivieren, solange Sie zu einem bestimmten Zeitpunkt aktiviert sind, bevor Sie den Vorgang abschließen. Wenn ein Archivpostfach nicht aktiviert ist, wird für Elemente, denen eine Archivrichtlinie zugewiesen ist, keine Aktion ausgeführt. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Sign in to Office 365 using your global administrator account.
    
    
3. Wechseln Sie im &amp; Security Compliance Center zu **Data Governance** \> **Archive**.
    
    Eine Liste der Postfächer in Ihrer Organisation wird angezeigt und ob das entsprechende Archivpostfach aktiviert oder deaktiviert ist. 
    
4. Wählen Sie alle Postfächer aus, indem Sie auf den ersten Eintrag in der Liste klicken, die **UMSCHALT** Taste gedrückt halten und dann auf den letzten Eintrag in der Liste klicken. 
    
    > [!TIP]
    > Bei diesem Schritt wird davon ausgegangen, dass keine Archivpostfächer aktiviert sind. Wenn Sie Postfächer mit aktiviertem Archiv haben, halten Sie die **STRG** -Taste gedrückt, und klicken Sie auf jedes Postfach, das ein deaktiviertes Archivpostfach aufweist. Sie können auch auf die Spaltenüberschrift **Archivpostfach** klicken, um die Zeilen abhängig davon zu sortieren, ob das Archivpostfach aktiviert oder deaktiviert ist, um die Auswahl von Postfächern zu erleichtern. 
  
5. Klicken Sie im Detailbereich unter **Massenbearbeitung**auf **aktivieren**.
    
    Es wird eine Warnung angezeigt, die besagt, dass Elemente, die älter als zwei Jahre sind, in das neue Archivpostfach verschoben werden. Der Grund ist, dass die standardmäßige Aufbewahrungsrichtlinie, der ein neues Benutzerpostfach zugewiesen wird, wenn es erstellt wird, ein Standardrichtlinientag für Archive mit einem Aufbewahrungszeitraum von 2 Jahren aufweist. Das Standardrichtlinientag für das benutzerdefinierte Archiv, das Sie in Schritt 2 erstellen, hat ein Aufbewahrungs Alter von 3 Jahren. Daher werden Elemente, die 3 Jahre oder älter sind, in das Archivpostfach verschoben.
    
6. Klicken Sie auf **Ja** , um die Warnmeldung zu beenden und den Prozess zu starten, um das Archivpostfach für jedes ausgewählte Postfach zu aktivieren. 
    
7. Klicken Sie **** ![nach Abschluss des Vorgangs auf Aktualisieren aktualisieren](media/165fb3ad-38a8-4dd9-9e76-296aefd96334.png) , um die Liste auf der Seite **Archiv** zu aktualisieren. 
    
    Das Archivpostfach ist für alle Benutzer in Ihrer Organisation aktiviert.
    
    ![Die Liste der Postfächer, für die das Archivpostfach aktiviert ist](media/61a7cb97-1bed-4808-aa5f-b6b761cfa8de.png)
  
8. Lassen Sie das &amp; Security Compliance Center geöffnet. Sie werden es im nächsten Schritt verwenden.
    
## <a name="step-2-create-new-retention-tags-for-the-archive-and-deletion-policies"></a>Schritt 2: Erstellen neuer Aufbewahrungstags für die Archivierungs-und Löschrichtlinien

In diesem Schritt erstellen Sie die drei zuvor beschriebenen benutzerdefinierten Aufbewahrungstags.
  
- Alpine House 3 Jahre Umzug in Archiv (benutzerdefinierte Archivrichtlinie)
    
- Alpine House 7 Jahr dauerhaft löschen (benutzerdefinierte Löschrichtlinie)
    
- Alpine House gelöschte Elemente 5 Jahre löschen und Wiederherstellung zulassen (benutzerdefiniertes Tag für den Ordner "Gelöschte Elemente")
    
Zum Erstellen neuer Aufbewahrungstags verwenden Sie die Exchange-Verwaltungskonsole in Ihrer Exchange Online-Organisation.
  
1. Klicken Sie im &amp; Security Compliance Center in der oberen linken Ecke auf das App-Startfeld, und klicken Sie dann auf die Kachel **Admin** . 
    
2. Klicken Sie im linken Navigationsbereich des Office 365 Admin Center auf **Admin**Center, und klicken Sie dann auf **Exchange**.
    
    ![Screenshot shows the Office 365 admin center with the Admin centers option expanded and Exchange selected.](media/47399df2-0bc4-42e2-b183-07750a46bc68.png)
  
3. Navigieren Sie in der Exchange- **Verwaltungs** \> Konsole zu **Aufbewahrungstags** für die Compliance-Verwaltung.
    
    Eine Liste der Aufbewahrungstags für Ihre Organisation wird angezeigt.
    
### <a name="create-a-custom-archive-default-policy-tag"></a>Erstellen eines benutzerdefinierten Archiv-Standardrichtlinientags
  
Zuerst erstellen Sie ein benutzerdefiniertes Standardrichtlinientag für das Archiv, mit dem Elemente nach 3 Jahren in das Archivpostfach verschoben werden. 
  
1. Klicken Sie auf der Seite **Aufbewahrungstags** auf **Neues Tag**![-Symbol](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), und wählen Sie dann **automatisch auf gesamtes Postfach angewendet (Standard)** aus. 
    
2. Füllen Sie auf der Seite **Neues Tag automatisch auf gesamtes Postfach angewendet (Standard)** die folgenden Felder aus: 
    
    ![Einstellungen zum Erstellen eines neuen Standardrichtlinientags für Archive](media/41c0a43c-9c72-44e0-8947-da0831896432.png)
  
1. **Name** Geben Sie einen Namen für das neue Aufbewahrungs ein. 
    
2. **Aufbewahrungsaktion** Wählen Sie **in Archiv verschieben** aus, um Elemente nach Ablauf des Aufbewahrungszeitraums in das Archivpostfach zu verschieben. 
    
3. **Aufbewahrungszeitraum** Wählen Sie aus, **wann das Element das folgende Alter (in Tagen) erreicht**, und geben Sie dann die Dauer des Aufbewahrungszeitraums ein. In diesem Szenario werden Elemente nach 1095 Tagen (3 Jahre) in das Archivpostfach verschoben.
    
4. **Kommentar** Optional Geben Sie einen Kommentar ein, der den Zweck des benutzerdefinierten Aufbewahrungstags erläutert. 
    
3. Klicken Sie auf **Speichern** , um die benutzerdefinierte Archiv-Standardrichtlinien zu erstellen. 
    
    Der neue Archiv-Standardrichtlinientag wird in der Liste der Aufbewahrungstags angezeigt.
    
### <a name="create-a-custom-deletion-default-policy-tag"></a>Erstellen eines Standardrichtlinientags für das Löschen von benutzerdefinierten Löschungen
  
Als Nächstes erstellen Sie einen weiteren benutzerdefinierten Standardrichtlinientag, aber hierbei handelt es sich um eine Löschrichtlinie, die Elemente dauerhaft nach 7 Jahren löscht.
  
1. Klicken Sie auf der Seite **Aufbewahrungstags** auf **Neues Tag**![-Symbol](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), und wählen Sie dann **automatisch auf gesamtes Postfach angewendet (Standard)** aus. 
    
2. Füllen Sie auf der Seite **Neues Tag automatisch auf gesamtes Postfach angewendet (Standard)** die folgenden Felder aus: 
    
    ![Einstellungen zum Erstellen eines neuen Standardrichtlinientags für das Löschen](media/f1f0ff62-eec9-4824-8e7c-d93dcfb09a79.png)
  
1. **Name** Geben Sie einen Namen für das neue Aufbewahrungs ein. 
    
2. **Aufbewahrungsaktion** Wählen Sie **endgültig löschen** aus, um Elemente aus dem Postfach zu entfernen, wenn der Aufbewahrungszeitraum abgelaufen ist. 
    
3. **Aufbewahrungszeitraum** Wählen Sie aus, **wann das Element das folgende Alter (in Tagen) erreicht**, und geben Sie dann die Dauer des Aufbewahrungszeitraums ein. In diesem Szenario werden Elemente nach 2555 Tagen (7 Jahre) gelöscht.
    
4. **Kommentar** Optional Geben Sie einen Kommentar ein, der den Zweck des benutzerdefinierten Aufbewahrungstags erläutert. 
    
3. Klicken Sie auf **Speichern** , um die benutzerdefinierte Löschungsrichtlinien Erstellung zu erstellen. 
    
    Der neue Lösch richtlinientag wird in der Liste der Aufbewahrungstags angezeigt.
    
### <a name="create-a-custom-retention-policy-tag-for-the-deleted-items-folder"></a>Erstellen eines benutzerdefinierten Aufbewahrungsrichtlinientags für den Ordner "Gelöschte Elemente"
  
Das letzte Aufbewahrungs, das Sie erstellen, ist ein benutzerdefiniertes Aufbewahrungsrichtlinientag (rpt) für den Ordner "Gelöschte Elemente". Mit diesem Tag werden Elemente im Ordner Gelöschte Elemente nach 5 Jahren gelöscht, und es wird ein Wiederherstellungszeitraum bereitgestellt, wenn Benutzer das Tool gelöschte Elemente wiederherstellen verwenden können, um ein Element wiederherzustellen.
  
1. Klicken Sie auf der Seite **Aufbewahrungstags** auf **Neues Tag** ![-Symbol](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif), und wählen Sie dann **automatisch auf einen Standardordner angewendet**aus. 
    
2. Füllen Sie für das **neue Tag, das automatisch auf eine Standardordner Seite angewendet** wird, die folgenden Felder aus: 
    
    ![Einstellungen zum Erstellen eines neuen Aufbewahrungsrichtlinientags für den Ordner "Gelöschte Elemente"](media/6f3104bd-5edb-48ac-884d-5fe13d81dd1d.png)
  
1. **Name** Geben Sie einen Namen für das neue Aufbewahrungs ein. 
    
2. **Anwenden dieses Tags auf den folgenden Standardordner** Wählen Sie in der Dropdownliste **Gelöschte Elemente**aus.
    
3. **Aufbewahrungsaktion** Wählen Sie **Löschen und Wiederherstellung zulassen** aus, um Elemente zu löschen, wenn der Aufbewahrungszeitraum abgelaufen ist, aber Benutzern das Wiederherstellen eines gelöschten Elements innerhalb des Aufbewahrungszeitraums für gelöschte Elemente (standardmäßig 14 Tage) gestatten. 
    
4. **Aufbewahrungszeitraum** Wählen Sie aus, **wann das Element das folgende Alter (in Tagen) erreicht**, und geben Sie dann die Dauer des Aufbewahrungszeitraums ein. In diesem Szenario werden Elemente nach 1825 Tagen (5 Jahre) gelöscht.
    
5. **Kommentar** Optional Geben Sie einen Kommentar ein, der den Zweck des benutzerdefinierten Aufbewahrungstags erläutert. 
    
3. Klicken Sie auf **Speichern** , um die benutzerdefinierte RPT für den Ordner Gelöschte Elemente zu erstellen. 
    
    Die neue RPT wird in der Liste der Aufbewahrungstags angezeigt.

## <a name="step-3-create-a-new-retention-policy"></a>Schritt 3: Erstellen einer neuen Aufbewahrungsrichtlinie

Nachdem Sie die benutzerdefinierten Aufbewahrungstags erstellt haben, besteht der nächste Schritt darin, eine neue Aufbewahrungsrichtlinie zu erstellen und die Aufbewahrungstags hinzuzufügen. Sie fügen die drei benutzerdefinierten Aufbewahrungstags hinzu, die Sie in Schritt 2 erstellt haben, und die integrierten Tags, die im ersten Abschnitt erwähnt wurden. In Schritt 4 weisen Sie diese neue Aufbewahrungsrichtlinie den Benutzerpostfächern zu.
  
1. Wechseln Sie in der Exchange- **Verwaltungs** \> Konsole zu **Aufbewahrungsrichtlinien**für Compliance-Verwaltung.
    
2. Klicken Sie auf der Seite Aufbewahrungs **** ![ **Richtlinien** auf neues](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)Symbol.
    
3. Geben Sie im Feld **Name** einen Namen für die neue Aufbewahrungsrichtlinie ein. Beispiel: **Alpine House Archiv-und Löschrichtlinie**. 
    
4. Klicken Sie unter **Aufbewahrungstags**auf neues](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif)Symbol **Hinzufügen** ![.
    
    Eine Liste der Aufbewahrungstags in Ihrer Organisation wird angezeigt. Hinweis die benutzerdefinierten Tags, die Sie in Schritt 2 erstellt haben, werden angezeigt.
    
5. Fügen Sie die 9 Aufbewahrungstags hinzu, die im folgenden Screenshot hervorgehoben werden (diese Tags werden im Abschnitt [Weitere Informationen](#more-information) ausführlicher beschrieben). Zum Hinzufügen eines Aufbewahrungstags wählen Sie es aus, und klicken Sie dann auf **Hinzufügen**. 
    
    ![Hinzufügen von Aufbewahrungstags zur neuen Aufbewahrungsrichtlinie](media/d8e87176-0716-4238-9e6a-7c4af35541dc.png)
  
    > [!TIP]
    > Sie können mehrere Aufbewahrungstags auswählen, indem Sie die **STRG** -Taste gedrückt halten und dann auf die einzelnen Tags klicken. 
  
6. Nachdem Sie die Aufbewahrungstags hinzugefügt haben, klicken Sie auf **OK**.
    
7. Klicken Sie auf der Seite **neue Aufbewahrungsrichtlinie** auf **Speichern** , um die neue Richtlinie zu erstellen. 
    
    Die neue Aufbewahrungsrichtlinie wird in der Liste angezeigt. Wählen Sie diese Option aus, um die mit ihr verknüpften Aufbewahrungstags im Detailbereich anzuzeigen.
    
    ![Die neue Aufbewahrungsrichtlinie und die Liste der verknüpften Aufbewahrungstags](media/63bc45e6-110b-4dc9-a85f-8eb1961a8258.png)
  
## <a name="step-4-assign-the-new-retention-policy-to-user-mailboxes"></a>Schritt 4: Zuweisen der neuen Aufbewahrungsrichtlinie zu Benutzerpostfächern

Wenn ein neues Postfach erstellt wird, wird standardmäßig eine Aufbewahrungsrichtlinie namens "Default MRM Policy" zugewiesen. In diesem Schritt ersetzen Sie diese Aufbewahrungsrichtlinie (da einem Postfach nur eine Aufbewahrungsrichtlinie zugewiesen werden kann), indem Sie die neue Aufbewahrungsrichtlinie, die Sie in Schritt 3 erstellt haben, den Benutzerpostfächern in Ihrer Organisation zuweisen. Bei diesem Schritt wird davon ausgegangen, dass Sie die neue Richtlinie allen Postfächern in Ihrer Organisation zuweisen.
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Empfänger** \> **Postfächer**.
    
    Eine Liste aller Benutzerpostfächer in Ihrer Organisation wird angezeigt. 
    
2. Wählen Sie alle Postfächer aus, indem Sie auf den ersten Eintrag in der Liste klicken, die **UMSCHALT** Taste gedrückt halten und dann auf den letzten Eintrag in der Liste klicken. 
    
3. Klicken Sie im Detailbereich auf der rechten Seite der Exchange-verwaltungsKONSOLE unter **Massenbearbeitung**auf **Weitere Optionen**.
    
4. Klicken Sie unter **Aufbewahrungsrichtlinie** auf **Aktualisieren**.
    
5. Wählen Sie auf der Seite **massenzuweisung** für Aufbewahrungsrichtlinie in der Dropdownliste **Aufbewahrungsrichtlinie auswählen** die Aufbewahrungsrichtlinie aus, die Sie in Schritt 3 erstellt haben. Beispiel: **Alpine House Archive and Retention Policy**.
    
6. Klicken Sie auf **Speichern** , um die neue Aufbewahrungsrichtlinien Zuweisung zu speichern. 
    
7. Gehen Sie wie folgt vor, um zu überprüfen, ob die neue Aufbewahrungsrichtlinie Postfächern zugewiesen wurde: Wählen Sie auf der Seite Postfächer ein Postfach aus, und klicken Sie dann auf Bearbeiten. 
    
1. Wählen Sie auf der Seite **Postfächer** ein Postfach aus, **** ![und klicken](media/d7dc7e5f-17a1-4eb9-b42d-487db59e2e21.png)Sie dann auf bearbeiten bearbeiten. 
    
2. Klicken Sie auf der Eigenschaftenseite des Postfachs für den ausgewählten Benutzer auf **Postfachfunktionen**.
    
    Der Name der neuen Richtlinie, die dem Postfach zugewiesen wurde, wird in der Dropdownliste **Aufbewahrungsrichtlinie** angezeigt. 

## <a name="optional-step-5-run-the-managed-folder-assistant-to-apply-the-new-settings"></a>Optional Schritt 5: Ausführen des Assistenten für verwaltete Ordner zum Anwenden der neuen Einstellungen

Nachdem Sie die neue Aufbewahrungsrichtlinie in Schritt 4 auf Postfächer angewendet haben, kann es bis zu 7 Tage dauern, bis die neuen Aufbewahrungseinstellungen auf die Postfächer angewendet werden. Der Grund ist, dass ein Prozess, der als Assistent für verwaltete Ordner bezeichnet wird, Postfächer alle 7 Tage verarbeitet. Anstatt zu warten, bis der Assistent für verwaltete Ordner ausgeführt wird, können Sie dies erzwingen, indem Sie das Cmdlet **Start-ManagedFolderAssistant** in Exchange Online PowerShell ausführen. 
  
 **Was geschieht, wenn Sie den Assistenten für verwaltete Ordner ausführen?** Die Einstellungen werden in der Aufbewahrungsrichtlinie angewendet, indem Elemente im Postfach überprüft werden und festgestellt wird, ob Sie aufbewahrt werden. Anschließend werden Elemente, die der Aufbewahrung unterliegen, mit dem entsprechenden Aufbewahrungs gestempelt, und anschließend wird die angegebene Aufbewahrungsaktion für Elemente nach Ihrem Aufbewahrungszeitraum ausgeführt. 
  
Im folgenden finden Sie die Schritte zum Herstellen einer Verbindung mit Exchange Online PowerShell und zum Ausführen des Assistenten für verwaltete Ordner für jedes Postfach in Ihrer Organisation.
  
1. Öffnen Sie auf Ihrem lokalen Computer Windows PowerShell, und führen Sie dann den folgenden Befehl aus.
    
    ```
    $UserCredential = Get-Credential
    ```

    Geben Sie im Dialogfeld **Windows PowerShell-Anmeldeinformationen anfordern** den Benutzernamen und das Kennwort für Ihr globales Administratorkonto von Office 365 ein, und klicken Sie dann auf **OK**.
    
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
    > Weitere Informationen oder Probleme beim Herstellen einer Verbindung mit Ihrer Exchange Online-Organisation finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283). 
  
5. Führen Sie die folgenden beiden Befehle aus, um den Assistenten für verwaltete Ordner für alle Benutzerpostfächer in Ihrer Organisation zu starten.
    
    ```
    $Mailboxes = Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"}
    ```

    ```
    $Mailboxes.Identity | Start-ManagedFolderAssistant
    ```

Das ist alles. Sie haben eine Archiv-und Löschrichtlinie für die Alpine House-Organisation eingerichtet.
  
## <a name="optional-step-6-make-the-new-retention-policy-the-default-for-your-organization"></a>Optional Schritt 6: Festlegen der standardmäßigen Aufbewahrungsrichtlinie für Ihre Organisation

In Schritt 4 müssen Sie die neue Aufbewahrungsrichtlinie vorhandenen Postfächern zuweisen. Sie können Exchange Online jedoch so konfigurieren, dass die neue Aufbewahrungsrichtlinie neuen Postfächern zugewiesen wird, die in der Zukunft erstellt werden. Hierzu können Sie Exchange Online PowerShell verwenden, um den Standard Postfachplan Ihrer Organisation zu aktualisieren. Ein *Postfachplan* ist eine Vorlage, mit der Eigenschaften für neue Postfächer automatisch konfiguriert werden.  In diesem optionalen Schritt können Sie die aktuelle Aufbewahrungsrichtlinie ersetzen, die dem Postfachplan (standardmäßig der MRM-Standardrichtlinie) mit der in Schritt 3 erstellten Aufbewahrungsrichtlinie zugewiesen ist. Nachdem Sie den Postfachplan aktualisiert haben, wird die neue Aufbewahrungsrichtlinie neuen Postfächern zugewiesen.

1. Stellen Sie [eine Verbindung mit Exchange Online PowerShell her,](https://go.microsoft.com/fwlink/p/?LinkId=517283) oder lesen Sie Schritt 5.

2. Führen Sie den folgenden Befehl aus, um Informationen zu den Postfachplänen in Ihrer Organisation anzuzeigen.

    ```
    Get-MailboxPlan | Format-Table DisplayName,RetentionPolicy,IsDefault
    ```
    Beachten Sie den Postfachplan, der als Standard festgelegt ist.

3. Führen Sie den folgenden Befehl aus, um die neue Aufbewahrungsrichtlinie, die Sie in Schritt 3 (beispielsweise **Alpine House Archive and Retention Policy**) erstellt haben, dem Standard Postfachplan zuzuweisen. In diesem Beispiel wird davon ausgegangen, dass der Name des Standard Postfachplans **exchangeonlineenterprise zurückgegeben**ist.

    ```
    Set-MailboxPlan "ExchangeOnlineEnterprise" -RetentionPolicy "Alpine House Archive and Retention Policy"
    ```
4. Sie können den Befehl in Schritt 2 erneut ausführen, um zu überprüfen, ob die dem Standard Postfachplan zugewiesene Aufbewahrungsrichtlinie geändert wurde.

## <a name="more-information"></a>Weitere Informationen

- Wie wird das Aufbewahrungszeitraum berechnet? Das Aufbewahrungs Alter von Postfachelementen wird ab dem Lieferdatum oder dem Erstellungsdatum für Elemente wie Entwurfsnachrichten berechnet, die nicht gesendet, sondern vom Benutzer erstellt werden. Wenn der Assistent für verwaltete Ordner Elemente in einem Postfach verarbeitet, werden alle Elemente, die Aufbewahrungstags mit der Aufbewahrungsaktion Löschen und Wiederherstellung zulassen oder Endgültig löschen aufweisen, mit einem Start- und einem Ablaufdatum gestempelt. Elemente mit einem Archiv-Tag werden mit einem Verschiebungsdatum gestempelt. 
    
- Die folgende Tabelle enthält weitere Informationen zu den einzelnen Aufbewahrungstags, die der benutzerdefinierten Aufbewahrungsrichtlinie hinzugefügt werden, die mit den Schritten in diesem Thema erstellt wurde.
    
    |**Aufbewahrungs**|**Was dieses Tag bewirkt**|**Integriert oder Benutzerdefiniert?**|**Type**|
    |:-----|:-----|:-----|:-----|
    |Alpine House 3 Jahre in Archiv verschieben  <br/> |Verschiebt Elemente, die 1095 Tage (3 Jahre) alt sind, in das Archivpostfach.  <br/> |Benutzerdefiniert (siehe [Schritt 2: Erstellen neuer Aufbewahrungstags für die Archivierungs-und Löschrichtlinien](#step-2-create-new-retention-tags-for-the-archive-and-deletion-policies))  <br/> |Standardrichtlinientag (Archiv); Dieses Tag wird automatisch auf das gesamte Postfach angewendet.  <br/> |
    |Alpine House 7 Jahr endgültig löschen  <br/> |Löscht Elemente im primären Postfach oder im Archivpostfach endgültig, wenn Sie 7 Jahre alt sind.  <br/> |Benutzerdefiniert (siehe [Schritt 2: Erstellen neuer Aufbewahrungstags für die Archivierungs-und Löschrichtlinien](#step-2-create-new-retention-tags-for-the-archive-and-deletion-policies))  <br/> |Standardrichtlinientag (Löschen); Dieses Tag wird automatisch auf das gesamte Postfach angewendet.  <br/> |
    |Alpine House gelöschte Elemente 5 Jahre löschen und Wiederherstellung zulassen  <br/> |Löscht Elemente aus dem Ordner Gelöschte Elemente, die 5 Jahre alt sind. Benutzer können diese Elemente bis zu 14 Tage nach dem Löschen wiederherstellen.<sup>\*</sup> <br/> |Benutzerdefiniert (siehe [Schritt 2: Erstellen neuer Aufbewahrungstags für die Archivierungs-und Löschrichtlinien](#step-2-create-new-retention-tags-for-the-archive-and-deletion-policies))  <br/> |AufbewahrungsRichtlinientag (Gelöschte Elemente); Dieses Tag wird automatisch auf Elemente im Ordner "Gelöschte Elemente" angewendet.  <br/> |
    |Wiederherstellbare Elemente, 14 Tage, in Archiv verschieben  <br/> |Verschiebt Elemente, die sich im Ordner "Wiederherstellbare Elemente" befinden, 14 Tage lang in den Ordner "Wiederherstellbare Elemente" im Archivpostfach.  <br/> |Integriert  <br/> |AufbewahrungsRichtlinientag (Wiederherstellbare Elemente); Dieses Tag wird automatisch auf Elemente im Ordner "Wiederherstellbare Elemente" angewendet.  <br/> |
    |Junk-E-Mail  <br/> |Löscht Elemente, die sich im Junk-e-Mail-Ordner befinden, endgültig 30 Tage lang. Benutzer können diese Elemente bis zu 14 Tage nach dem Löschen wiederherstellen.<sup>\*</sup> <br/> |Integriert  <br/> |AufbewahrungsRichtlinientag (Junk-e-Mail); Dieses Tag wird automatisch auf Elemente im Junk-e-Mail-Ordner angewendet.  <br/> |
    |1 Monat, löschen  <br/> |Löscht Elemente, die 30 Tage alt sind, endgültig. Benutzer können diese Elemente bis zu 14 Tage nach dem Löschen wiederherstellen.<sup>\*</sup> <br/> |Integriert  <br/> |Persönliche Dieses Tag kann von Benutzern angewendet werden.  <br/> |
    |1 Jahr, löschen  <br/> |Löscht Elemente, die 365 Tage alt sind, endgültig. Benutzer können diese Elemente bis zu 14 Tage nach dem Löschen wiederherstellen.<sup>\*</sup> <br/> |Integriert  <br/> |Persönliche Dieses Tag kann von Benutzern angewendet werden.  <br/> |
    |Nie löschen  <br/> |Dieses Tag verhindert, dass Elemente durch eine Aufbewahrungsrichtlinie gelöscht werden.  <br/> |Integriert  <br/> |Persönliche Dieses Tag kann von Benutzern angewendet werden.  <br/> |
    |Persönlich, 1 Jahre, in Archiv verschieben  <br/> |Verschiebt Elemente nach einem Jahr in das Archivpostfach.  <br/> |Integriert  <br/> |Persönliche Dieses Tag kann von Benutzern angewendet werden.  <br/> |
   
    > <sup>\*</sup>Benutzer können das Tool gelöschte Elemente wiederherstellen in Outlook und Outlook im Web (früher als Outlook Web App bezeichnet) verwenden, um ein gelöschtes Element innerhalb des Aufbewahrungszeitraums für gelöschte Elemente wiederherzustellen, der standardmäßig 14 Tage in Exchange Online ist. Ein Administrator kann Windows PowerShell verwenden, um die Aufbewahrungsdauer für gelöschte Elemente auf maximal 30 Tage zu verlängern. Weitere Informationen finden Sie unter: [Wiederherstellen von gelöschten Elementen in Outlook für Windows](https://support.office.com/article/49e81f3c-c8f4-4426-a0b9-c0fd751d48ce) und [Ändern des Aufbewahrungszeitraums für gelöschte Elemente für ein Postfach in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940)
  
- Die Verwendung des Recoverable **Items 14 Days Move to Archive** Retention Tag trägt dazu bei, Speicherplatz im Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers freizugeben. Dies ist hilfreich, wenn das Postfach eines Benutzers in den Wartebereich gestellt wird, was bedeutet, dass das Postfach des Benutzers nie dauerhaft gelöscht wird. Ohne Elemente in das Archivpostfach zu bewegen, ist es möglich, dass das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" im primären Postfach erreicht wird. Weitere Informationen zu diesem Thema und dazu, wie Sie es vermeiden können, finden Sie unter [increase the recoverAble Items Quota for Mailboxes on Hold](https://go.microsoft.com/fwlink/p/?LinkId=786479).
