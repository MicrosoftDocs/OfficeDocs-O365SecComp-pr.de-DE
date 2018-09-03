---
title: Erhöhen des Kontingents für wiederherstellbare Elemente für im In-Situ-Speicher befindliche Postfächer
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/22/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: 'Aktivieren Sie das Archivpostfach, und schalten Sie automatisch erweitert, um die Größe des Ordners "wiederherstellbare Elemente" für ein Postfach in Office 365 erhöhen Archivierung. '
ms.openlocfilehash: cd2d07e6ef1637343798ccb71870c8d436f10574
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782092"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a>Erhöhen des Kontingents für wiederherstellbare Elemente für im In-Situ-Speicher befindliche Postfächer

Standardaufbewahrungsrichtlinie – mit dem Namen MRM-Standardrichtlinie – d. h. automatisch angewendet auf neue Postfächer in Exchange Online enthält ein aufbewahrungstag benannten wiederherstellbare Elemente, 14 Tage in Archiv verschieben. In diesem aufbewahrungstag Verschiebt Elemente aus dem Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner "wiederherstellbare Elemente" im Archivpostfach des Benutzers nach Ablauf die Aufbewahrungszeit 14 Tagen für ein Element. Für dazu muss Archivpostfach des Benutzers aktiviert sein. Wenn das Archivpostfach nicht aktiviert ist, wird keine Aktion ausgeführt, was bedeutet, dass Elemente im Ordner für ein Postfach auf halten wiederherstellbaren Elementen in das Archivpostfach verschoben werden nicht nach Ablauf die Aufbewahrungszeit 14 Tagen. Da nichts aus einem Postfach in der Warteschleife gelöscht wird, ist es möglich, dass das Speicherkontingent für den Ordner wiederherstellbare Elemente überschritten werden kann, insbesondere dann, wenn das Postfach des Benutzers Archiv nicht aktiviert ist. 
  
Um das Risiko Überschreitung dieses Grenzwerts reduzieren, ist das Speicherkontingent für den Ordner wiederherstellbare Elemente automatisch Erhöhung von 30 GB auf 100 GB bei ein Haltestatus für ein Postfach im Exchange Online platziert wird. Wenn das Archivpostfach aktiviert ist, wird das Speicherkontingent für den Ordner "wiederherstellbare Elemente" im Archivpostfach auch von 30 GB auf 100 GB erhöht. Wenn feature erweiterbares Archivierung in Exchange Online ist aktiviert, das Speicherkontingent für den Ordner "wiederherstellbare Elemente" in das benutzerarchiv unbegrenzt.
  
  In der folgenden Tabelle sind die Speicherkontingente für den Ordner „Wiederherstellbare Elemente“ zusammengefasst. 
  
|**Speicherort des Ordners „Wiederherstellbare Elemente“**|**Nicht aufzubewahrende Postfächer**|**Aufzubewahrende Postfächer**|
|:-----|:-----|:-----|
|Primäres Postfach  <br/> |30 GB  <br/> |100 GB  <br/> |
|Archivpostfach<sup>\*</sup> <br/> |Unbegrenzt  <br/> |Unbegrenzt  <br/> |
|**Gesamtspeicherkontingent für den Ordner „Wiederherstellbare Elemente“** <br/> |Unbegrenzt  <br/> |Unbegrenzt  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Das ursprüngliche Speicherkontingent für das Archivpostfach beträgt 100 GB für Benutzer mit einer Lizenz für Exchange Online (Plan 2). Jedoch wenn erweiterbares Archivierung aktiviert ist für Postfächer in der Warteschleife, das Speicherkontingent für beide das Archivpostfach und des Ordners wiederherstellbare Elemente auf 110 GB erhöht. Zusätzliche Archiv Speicherplatz wird bereitgestellt, bei Bedarf unbegrenzt Archivspeicher ergibt. Weitere Informationen zum Erweitern von automatischen Archivierung, finden Sie unter [Übersicht über die uneingeschränkte Archivierung in Office 365](unlimited-archiving.md). 
  
Wenn das Speicherkontingent für den Ordner „Wiederherstellbare Elemente“ im primären Postfach eines aufzubewahrenden Postfachs seinen Grenzwert bald erreicht, können Sie Folgendes ausführen:
  
- **Aktivieren Sie das Archivpostfach und Aktivieren von erweiterbares Archivierung** – können Sie einen unbegrenzte Speicherkapazität für "wiederherstellbare Elemente" einfach durch das Archivpostfach aktivieren und dann das automatisch erweitert, Archivierung Feature in Exchange Online. Dies führt 110 GB für den Ordner "wiederherstellbare Elemente" in das primäre Postfach und eine unbegrenzte Zeitspanne Speicherkapazität für den Ordner wiederherstellbare Elemente im Archiv des Benutzers. Finden Sie unter wie: [Aktivieren von archivpostfächern in die Office 365-Sicherheit &amp; Compliance Center](enable-archive-mailboxes.md) und [unbegrenzte Archivierung in Office 365 zu aktivieren](enable-unlimited-archiving.md).
    
    > [!NOTE]
    > Nachdem Sie das Archiv für ein Postfach aktiviert haben, die fast für "wiederherstellbare Elemente" das Speicherkontingent überschritten ist, Sie möglicherweise ausführen möchten, der Assistent für verwaltete Ordner manuell Auslösen der Assistent, um das Postfach verarbeitet werden, damit abgelaufene Elemente verschoben werden, um die Ordner wiederherstellbare Elemente im Archivpostfach. Weitere Informationen finden Sie in [Schritt 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) . Beachten Sie, dass andere Elemente im Postfach des Benutzers in das neue Archivpostfach verschoben werden können. Berücksichtigen Sie den Anwender darüber, dass dies geschehen kann, nachdem Sie das Archivpostfach aktivieren. 
  
- **Erstellen eine benutzerdefinierten Aufbewahrungsrichtlinie für Postfächer auf halten** - zusätzlich zu aktivieren das Archivpostfach und erweiterbares Archivierung für Postfächer Beweissicherungsverfahren oder Compliance-Archiv, auch sollten Sie zum Erstellen einer benutzerdefinierten Aufbewahrungsrichtlinie für Postfächer auf halten. Dies wenden wir Sie eine Aufbewahrungsrichtlinie auf Postfächer in der Warteschleife, die von der MRM-Standardrichtlinie abweicht, die auf Postfächer angewendet wird, die nicht in der Warteschleife sind. Auf diese Weise können Sie um aufbewahrungstags anzuwenden, die speziell für Postfächer in der Warteschleife entwickelt wurden. Dazu gehört das Erstellen eines neuen aufbewahrungstags für "wiederherstellbare Elemente". 
    
Im restlichen Thema werden die schrittweisen Anweisungen zum Erstellen einer benutzerdefinierten Aufbewahrungsrichtlinie für aufzubewahrende Postfächer erläutert.
  
[Schritt 1: Erstellen eines benutzerdefinierten Aufbewahrungstags für den Ordner „Wiederherstellbare Elemente“](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

[[Schritt2: erstellen eine neuen Aufbewahrungsrichtlinie für Postfächer in der Warteschleife](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)

[Schritt 3: Anwenden der neuen Aufbewahrungsrichtlinie auf aufzubewahrende Postfächer](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[(Optional) Schritt 4: Ausführen des Assistenten für verwaltete Ordner zum Anwenden der neuen Aufbewahrungseinstellungen](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a>Schritt 1: Erstellen eines benutzerdefinierten Aufbewahrungstags für den Ordner „Wiederherstellbare Elemente“

Der erste Schritt ist zum Erstellen eines benutzerdefinierten aufbewahrungstags (Aufbewahrungsrichtlinien-Tag oder Berichtskopf genannt) für den Ordner "wiederherstellbare Elemente". Wie bereits erklärt verschiebt diese außer Elemente aus dem Ordner "wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner "wiederherstellbare Elemente" im Archivpostfach des Benutzers. Sie müssen PowerShell verwenden, um ein Aufbewahrungsrichtlinientag für "wiederherstellbare Elemente" zu erstellen. Sie können nicht im Exchange Administrationscenter (EAC) verwenden. 
  
1. [Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. Führen Sie den folgenden Befehl zum Erstellen eines Aufbewahrungstags für den Ordner „Wiederherstellbare Elemente“ aus:  
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    Durch den folgenden Befehl wird beispielsweise ein Aufbewahrungstag für den Ordner „Wiederherstellbare Elemente“ mit dem Namen „Wiederherstellbare Elemente, 30 Tage, für aufzubewahrende Postfächer“ mit einem Aufbewahrungszeitraum von 30 Tagen erstellt. Dies bedeutet, dass ein Element, nachdem es 30 Tage lang im Ordner „Wiederherstellbare Elemente“ gespeichert war, in den Ordner „Wiederherstellbare Elemente“ im Archivpostfach des Benutzers verschoben wird.
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > Es wird empfohlen, dass der Aufbewahrungszeitraum für die wiederherstellbare Elemente außer (definiert durch den Parameter _' AgeLimitForRetention '_ ) ist, als die Aufbewahrungszeit für Postfächer, die auf der Berichtskopf angewendet wird. Dadurch kann der Benutzer die gesamte Aufbewahrungszeit Wiederherstellen gelöschter Objekte, bevor sie in das Archivpostfach verschoben werden. Im vorherigen Beispiel wurde die Aufbewahrungsdauer auf 30 Tage basierend auf der Annahme, die die Aufbewahrungszeit für Postfächer auch 30 Tage ist festgelegt. Exchange Online-Postfachs ist für gelöschte Elemente 14 Tage lang aufbewahrt werden standardmäßig konfiguriert. Sie können jedoch ändern diese Einstellung auf ein Maximum von 30 Tagen. Weitere Informationen finden Sie unter [Ändern der Aufbewahrungszeit für ein Postfach im Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940). 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a>Schritt 2: Erstellen einer neuen Aufbewahrungsrichtlinie für aufzubewahrende Postfächer

Der nächste Schritt besteht darin, eine neue Aufbewahrungsrichtlinie zu erstellen und dieser Aufbewahrungstags hinzuzufügen, einschließlich der Aufbewahrungstags für wiederherstellbare Elemente, die Sie in Schritt 1 erstellt haben. Diese neue Richtlinie wird im nächsten Schritt auf aufzubewahrende Postfächer angewendet.  
  
Bevor Sie die neue Aufbewahrungsrichtlinie erstellen, ermitteln Sie die zusätzlichen Aufbewahrungstags, die Sie hinzufügen möchten. Eine Liste der Aufbewahrungstags, die der Standard-MRM-Richtlinie hinzugefügt werden, sowie Informationen zum Erstellen neuer Aufbewahrungstags finden Sie unter:
  
- [Default Aufbewahrungsrichtlinien in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [Standardordner, die Aufbewahrungsrichtlinientags unterstützen](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- Abschnitt "erstellen Sie ein aufbewahrungstag" im Thema [Create a Retention Policy](https://go.microsoft.com/fwlink/p/?LinkId=404422) .
    
Der Exchange-Verwaltungskonsole oder die Exchange Online PowerShell können Sie um eine Aufbewahrungsrichtlinie zu erstellen.
  
### <a name="use-the-eac-to-create-a-retention-policy"></a>Erstellen einer Aufbewahrungsrichtlinie mithilfe der Exchange-Verwaltungskonsole
  
1. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Verwaltung der Richtlinientreue** \> **Aufbewahrungsrichtlinien**, und klicken Sie dann auf **Hinzufügen** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif).
    
2. Geben Sie auf der Seite **Neue Aufbewahrungsrichtlinie** unter **Name** einen Namen ein, der den Zweck der Aufbewahrungsrichtlinie beschreibt, z. B. **MRM Policy for Mailboxes on Hold**.  
    
3. Klicken Sie auf **Hinzufügen** , klicken Sie unter **Retention Tags**, ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif).
    
4. Wählen Sie in der Liste mit Aufbewahrungstags das Aufbewahrungstag für wiederherstellbare Elemente aus, das Sie in Schritt 1 erstellt haben, und klicken Sie dann auf **Hinzufügen**.
    
    ![Wählen Sie das benutzerdefinierte Aufbewahrungstag „Wiederherstellbare Elemente“ aus.](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. Wählen Sie zusätzliche Aufbewahrungstags aus, die der Aufbewahrungsrichtlinie hinzugefügt werden sollen. Sie können beispielsweise dieselben Tags hinzufügen, die in der Standard-MRM-Richtlinie enthalten sind.
    
6. Klicken Sie auf **OK**, wenn Sie mit dem Hinzufügen von Aufbewahrungstags fertig sind.
    
7. Klicken Sie auf **Speichern**, um die neue Aufbewahrungsrichtlinie zu erstellen. 
    
    Im Detailbereich werden Aufbewahrungstags verknüpft mit der Aufbewahrungsrichtlinie angezeigt.
    
    ![Im Detailbereich werden Aufbewahrungstags verknüpft mit der Aufbewahrungsrichtlinie angezeigt.](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a>Verwenden Sie Exchange Online PowerShell, um eine Aufbewahrungsrichtlinie zu erstellen.
  
Führen Sie zum Erstellen einer neuen Aufbewahrungsrichtlinie für aufzubewahrende Postfächer den folgenden Befehl aus:  
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

Durch den folgenden Befehl wird beispielsweise die Aufbewahrungsrichtlinie erstellt und mit Aufbewahrungstags verknüpft, die in der vorherigen Abbildung dargestellt sind.
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a>Schritt 3: Anwenden der neuen Aufbewahrungsrichtlinie auf aufzubewahrende Postfächer

Der letzte Schritt ist die neue Aufbewahrungsrichtlinie angewendet, die Sie in Schritt2 auf Postfächer in der Warteschleife in Ihrer Organisation erstellt. Der Exchange-Verwaltungskonsole oder die Exchange Online PowerShell können Sie die Aufbewahrungsrichtlinie auf ein einzelnes Postfach oder auf mehrere Postfächer anzuwenden. 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a>Anwenden der neuen Aufbewahrungsrichtlinie mithilfe der Exchange-Verwaltungskonsole
  
1. Navigieren Sie zu **Empfänger** \> **Postfächer**.
    
2. In der Listenansicht, wählen Sie das Postfach, das Sie die Aufbewahrungsrichtlinie auf anwenden möchten, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
3. Klicken Sie auf der Seite **Benutzerpostfach** auf **Postfachfunktionen**.
    
4. Wählen Sie unter **Aufbewahrungsrichtlinie** die Aufbewahrungsrichtlinie aus, die Sie in Schritt 2 erstellt haben, und klicken Sie dann auf **Speichern**.
    
Sie können auch die Exchange-Verwaltungskonsole verwenden, um die Aufbewahrungsrichtlinie auf mehrere Postfächer anzuwenden.
  
1. Navigieren Sie zu **Empfänger** \> **Postfächer**.
    
2. Verwenden Sie in der Listenansicht die UMSCHALT- oder die STRG-TASTE, um mehrere Postfächer auszuwählen.
    
3. Klicken Sie im Detailbereich auf **Weitere Optionen**.
    
4. Klicken Sie unter **Aufbewahrungsrichtlinie** auf **Aktualisieren**.
    
5. Wählen Sie auf der Seite**Massenzuweisung von Aufbewahrungsrichtlinie** die Aufbewahrungsrichtlinie aus, die Sie in Schritt 2 erstellt haben, und klicken Sie dann auf **Speichern**.  
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a>Verwenden Sie Exchange Online PowerShell, um die neue Aufbewahrungsrichtlinie
  
Exchange Online PowerShell können Sie eine neue Aufbewahrungsrichtlinie auf ein einzelnes Postfach anwenden. Aber die wirkliche Stärke von PowerShell besteht darin, dass Sie schnell alle identifizieren, die die Postfächer in Ihrer Organisation, die entweder Beweissicherungsverfahren oder Compliance-Archiv, und wenden Sie die neue Aufbewahrungsrichtlinie auf alle Postfächer auf einem einzelnen Befehl enthalten können. Hier sind einige Beispiele für die Verwendung von Exchange PowerShell anwenden eine Aufbewahrungsrichtlinie auf eine oder mehrere Postfächer. Alle Beispiele gelten die Aufbewahrungsrichtlinie, die in Schritt2 erstellt wurde.
  
In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf das Postfach von Pilar Pinilla angewendet.
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf alle Postfächer im Beweissicherungsverfahren angewendet.
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf alle Postfächer in der Organisation angewendet, die sich im In-Situ-Speicher befinden.
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

Sie können das Cmdlet **Get-Mailbox** verwenden, um zu überprüfen, dass die neue Aufbewahrungsrichtlinie angewendet wurde. 
  
Nachfolgend finden Sie einige Beispiele, mit denen Sie überprüfen können, dass über die Befehle in den vorherigen Beispielen die Aufbewahrungsrichtlinie „MRM-Richtlinie für Postfächer im In-Situ-Speicher“ auf Postfächer im Beweissicherungsverfahren und auf Postfächer im In-Situ-Speicher angewendet wurde.
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a>(Optional) Schritt 4: Ausführen des Assistenten für verwaltete Ordner zum Anwenden der neuen Aufbewahrungseinstellungen

Nachdem Sie die neue Aufbewahrungsrichtlinie auf Postfächer in der Warteschleife anwenden, kann es bis zu sieben Tage in Exchange Online für den Assistenten für verwaltete Ordner diese Postfächer mithilfe der Einstellungen in die neue Aufbewahrungsrichtlinie verarbeitet dauern. Das Cmdlet **Start-ManagedFolderAssistant** können Sie anstelle der Assistent für verwaltete Ordner ausgeführt werden muss, manuell Auslösen der Assistent zum Verarbeiten der Postfächer, denen Sie auf die neue Aufbewahrungsrichtlinie angewendet. 
  
Führen Sie den folgenden Befehl aus, um den Assistenten für verwaltete Ordner für das Postfach von Pilar Pinilla zu starten.
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

Führen Sie die folgenden Befehle aus, um den Assistenten für verwaltete Ordner für alle aufzubewahrenden Postfächer zu starten:
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a>Weitere Informationen

- Nachdem Sie Archivpostfach des Benutzers aktiviert haben, sollten Sie den Anwender darüber, dass andere Elemente in ihrem Postfach (nicht nur Elemente im Ordner "wiederherstellbare Elemente") in das Archivpostfach verschoben werden können. Dies ist, da der MRM-Standardrichtlinie, die Exchange Online-Postfächern zugewiesen ist, ein aufbewahrungstag (benannte Standard 2 Jahre, in Archiv verschieben), die Elemente in das Archivpostfach zwei Jahre nach dem Datum verschiebt das Element an das Postfach übermittelt wurde oder enthält von erstellt die Benutzer. Weitere Informationen finden Sie unter [Default Retention Policy in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- Nachdem Sie Archivpostfach des Benutzers aktiviert haben, erfahren Sie möglicherweise auch, dass der Benutzer, den sie wiederherstellen können, Elemente im Ordner "wiederherstellbare Elemente" in ihrem Archivpostfach gelöscht. Sie können in Outlook dazu auswählen den Ordner **Gelöschte Elemente** in das Archivpostfach, und klicken auf der Registerkarte **Start** **Vom Server gelöschte Elemente wiederherstellen** . Weitere Informationen zum Wiederherstellen von gelöschten Elementen finden Sie unter [Gelöschte Elemente in Outlook für Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829). 
