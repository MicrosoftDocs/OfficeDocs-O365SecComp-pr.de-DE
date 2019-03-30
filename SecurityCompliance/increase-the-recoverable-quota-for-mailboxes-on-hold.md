---
title: Erhöhen des Kontingents für wiederherstellbare Elemente für aufzubewahrende Postfächer
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a8bdcbdd-9298-462f-b889-df26037a990c
description: 'Aktivieren Sie das Archivpostfach, und aktivieren Sie die automatische Erweiterung der Archivierung, um die Größe des Ordners "Wiederherstellbare Elemente" für ein Postfach in Office 365 zu erhöhen. '
ms.openlocfilehash: f419da5b1b42d52433e9fc288aa5b401a2123c1c
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "30998968"
---
# <a name="increase-the-recoverable-items-quota-for-mailboxes-on-hold"></a>Erhöhen des Kontingents für wiederherstellbare Elemente für aufzubewahrende Postfächer

Die standardmäßige Aufbewahrungsrichtlinie "Default MRM Policy", die automatisch auf neue Postfächer in Exchange Online angewendet wird, enthält ein Aufbewahrungs mit dem Namen "Wiederherstellbare Elemente 14 Tage in Archiv verschieben". Mit diesem Aufbewahrungs werden Elemente aus dem Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner "Wiederherstellbare Elemente" im Archivpostfach des Benutzers verschoben, nachdem die Aufbewahrungsdauer für ein Element von 14 Tagen abgelaufen ist. Damit dies geschieht, muss das Archivpostfach des Benutzers aktiviert sein. Wenn das Archivpostfach nicht aktiviert ist, wird keine Aktion ausgeführt, was bedeutet, dass Elemente im Ordner "Wiederherstellbare Elemente" für ein gespeichertes Postfach nicht nach Ablauf des Aufbewahrungszeitraums von 14 Tagen in das Archivpostfach verschoben werden. Da nichts aus einem Postfach gelöscht wird, ist es möglich, dass das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" überschritten wird, insbesondere, wenn das Archivpostfach des Benutzers nicht aktiviert ist. 
  
Um die Wahrscheinlichkeit zu verringern, dass dieser Grenzwert überschritten wird, wird das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" automatisch von 30 GB auf 100 GB erhöht, wenn ein Haltebereich für ein Postfach in Exchange Online gespeichert wird. Wenn das Archivpostfach aktiviert ist, wird das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" im Archivpostfach ebenfalls von 30 GB auf 100 GB erhöht. Wenn das Feature für die automatische Erweiterung der Archivierung in Exchange Online aktiviert ist, ist das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" im Archiv des Benutzers unbegrenzt.
  
 In der folgenden Tabelle wird das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" zusammengefasst. 
  
|**Speicherort des Ordners "Wiederherstellbare Elemente"**|**Postfächer nicht in der Warteschleife**|**Aufbewahrung von Postfächern**|
|:-----|:-----|:-----|
|Primäres Postfach  <br/> |30 GB  <br/> |100 GB  <br/> |
|Archivpostfach<sup>\*</sup> <br/> |Unbeschränkt  <br/> |Unbeschränkt  <br/> |
|**Gesamtspeicher Kontingent für den Ordner "Wiederherstellbare Elemente"** <br/> |Unbeschränkt  <br/> |Unbeschränkt  <br/> |
   
> [!NOTE]
> <sup>\*</sup>Das anfängliche Speicherkontingent für das Archivpostfach beträgt 100 GB für Benutzer mit einer Exchange Online-Lizenz (Plan 2). Wenn die automatische Erweiterung der Archivierung jedoch für Postfächer aktiviert ist, wird das Speicherkontingent für das Archivpostfach und den Ordner "Wiederherstellbare Elemente" auf 110 GB erhöht. Bei Bedarf wird zusätzlicher Archivspeicher Platz zur Verfügung gestellt, was eine unbegrenzte Menge an Archivspeicher zur Folge hat. Weitere Informationen zur automatischen Erweiterung der Archivierung finden Sie unter [Übersicht über die unbegrenzte Archivierung in Office 365](unlimited-archiving.md). 
  
Wenn sich das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" im primären Postfach eines Postfachs in der Warteschleife in der Nähe des Grenzwerts befindet, können Sie die folgenden Schritte ausführen:
  
- **Aktivieren Sie das Archivpostfach, und** aktivieren Sie die automatische Erweiterung der Archivierung-Sie können eine unbegrenzte Speicherkapazität für den Ordner "Wiederherstellbare Elemente" aktivieren, indem Sie einfach das Archivpostfach aktivieren und dann das Feature für die automatische Erweiterung der Archivierung in Exchange Online. Dies führt zu 110 GB für den Ordner "Wiederherstellbare Elemente" im primären Postfach und eine unbegrenzte Speicherkapazität für den Ordner "Wiederherstellbare Elemente" im Archiv des Benutzers. Weitere Informationen finden Sie unter Vorgehensweise: [Aktivieren von archivpostfächern im Security _AMP_ Compliance Center](enable-archive-mailboxes.md) und Aktivieren der unlimitierten [archivierung in Office 365](enable-unlimited-archiving.md).
    
    > [!NOTE]
    > Nachdem Sie das Archiv für ein Postfach aktiviert haben, das das Speicherkontingent für den Ordner "Wiederherstellbare Elemente" nicht überschreitet, können Sie den Assistenten für verwaltete Ordner ausführen, um den Assistenten für die Verarbeitung des Postfachs manuell auszulösen, sodass abgelaufene Elemente verschoben werden. Ordner "Wiederherstellbare Elemente" im Archivpostfach. Weitere Informationen finden Sie unter [Schritt 4](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings) . Beachten Sie, dass andere Elemente im Postfach des Benutzers möglicherweise in das neue Archivpostfach verschoben werden. Sie sollten dem Benutzer mitteilen, dass dies nach der Aktivierung des Archivpostfachs möglicherweise geschieht. 
  
- **Erstellen einer benutzerdefinierten Aufbewahrungsrichtlinie für Postfächer in der Warteschleife** – zusätzlich zur Aktivierung des Archivpostfachs und der automatischen Erweiterung der Archivierung von Postfächern im Rechtsstreit oder in-situ-Speicherung möchten Sie möglicherweise auch eine benutzerdefinierte Aufbewahrungsrichtlinie für Postfächer erstellen. situ. Auf diese Weise können Sie eine Aufbewahrungsrichtlinie auf Postfächer anwenden, die sich von der standardmäßigen MRM-Richtlinie unterscheidet, die auf Postfächer angewendet wird, die nicht in der Warteschleife gespeichert sind. Auf diese Weise können Sie Aufbewahrungstags anwenden, die speziell für Postfächer vorgesehen sind. Dazu gehört das Erstellen eines neuen Aufbewahrungstags für den Ordner "Wiederherstellbare Elemente". 
    
Im weiteren Verlauf dieses Themas werden die schrittweisen Verfahren zum Erstellen einer benutzerdefinierten Aufbewahrungsrichtlinie für Postfächer beschrieben.
  
[Schritt 1: Erstellen eines benutzerdefinierten Aufbewahrungstags für den Ordner "Wiederherstellbare Elemente"](#step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder)

[[Schritt 2: Erstellen einer neuen Aufbewahrungsrichtlinie für Postfächer in der Warteschleife](#step-2-create-a-new-retention-policy-for-mailboxes-on-hold)

[Schritt 3: Anwenden der neuen Aufbewahrungsrichtlinie auf Postfächer in der Warteschleife](#step-3-apply-the-new-retention-policy-to-mailboxes-on-hold)

[Optional Schritt 4: Ausführen des Assistenten für verwaltete Ordner zum Anwenden der neuen Aufbewahrungseinstellungen](#optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings)
  
## <a name="step-1-create-a-custom-retention-tag-for-the-recoverable-items-folder"></a>Schritt 1: Erstellen eines benutzerdefinierten Aufbewahrungstags für den Ordner "Wiederherstellbare Elemente"

Der erste Schritt besteht darin, ein benutzerdefiniertes Aufbewahrungs (als Aufbewahrungsrichtlinientag oder RPT bezeichnet) für den Ordner "Wiederherstellbare Elemente" zu erstellen. Wie bereits erläutert, verschiebt dieser RPT Elemente aus dem Ordner "Wiederherstellbare Elemente" im primären Postfach des Benutzers in den Ordner "Wiederherstellbare Elemente" im Archivpostfach des Benutzers. Sie müssen PowerShell verwenden, um eine RPT für den Ordner "Wiederherstellbare Elemente" zu erstellen. Sie können nicht die Exchange-Verwaltungskonsole (EAC) verwenden. 
  
1. [Connect to Exchange Online using remote PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=517283)
    
2. Führen Sie den folgenden Befehl aus, um eine neue RPT für den Ordner "Wiederherstellbare Elemente" zu erstellen: 
    
    ```
    New-RetentionPolicyTag -Name <Name of RPT> -Type RecoverableItems -AgeLimitForRetention <Number of days> -RetentionAction MoveToArchive
    ```

    Mit dem folgenden Befehl wird beispielsweise ein RPT für den Ordner "Wiederherstellbare Elemente" mit dem Namen "Wiederherstellbare Elemente 30 Tage für Aufbewahrungszeit von Postfächern" erstellt, der eine Beibehaltungsdauer von 30 Tagen hat. Dies hat zur Folge, dass ein Element im Ordner "Wiederherstellbare Elemente" seit 30 Tagen in den Ordner "Wiederherstellbare Elemente" im Archivpostfach des Benutzers verschoben wird.
    
    ```
    New-RetentionPolicyTag -Name "Recoverable Items 30 days for mailboxes on hold" -Type RecoverableItems -AgeLimitForRetention 30 -RetentionAction MoveToArchive
    ```

    > [!TIP]
    > Es wird empfohlen, dass der Aufbewahrungszeitraum (definiert durch den _AgeLimitForRetention_ -Parameter) für die zurückzuGebenden Elemente RPT mit dem Aufbewahrungszeitraum für gelöschte Elemente für die Postfächer identisch ist, auf die die RPT angewendet wird. Dadurch kann ein Benutzer den gesamten Aufbewahrungszeitraum für gelöschte Elemente wiederherstellen, bevor er in das Archivpostfach verschoben wird. Im vorherigen Beispiel wurde der Aufbewahrungszeitraum auf 30 Tage festgelegt, basierend auf der Annahme, dass der Aufbewahrungszeitraum für gelöschte Elemente auch 30 Tage beträgt. Ein Exchange Online-Postfach ist so konfiguriert, dass gelöschte Elemente standardmäßig 14 Tage aufbewahrt werden. Sie können diese Einstellung jedoch auf maximal 30 Tage ändern. Weitere Informationen finden Sie unter [Ändern des Aufbewahrungszeitraums für gelöschte Elemente für ein Postfach in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=286940). 
  
## <a name="step-2-create-a-new-retention-policy-for-mailboxes-on-hold"></a>Schritt 2: Erstellen einer neuen Aufbewahrungsrichtlinie für Postfächer in der Warteschleife

Der nächste Schritt besteht darin, eine neue Aufbewahrungsrichtlinie zu erstellen und Ihr Aufbewahrungstags hinzuzufügen, einschließlich der in Schritt 1 erstellten "Wiederherstellbare Elemente". Diese neue Richtlinie wird auf Postfächer angewendet, die im nächsten Schritt gehalten werden. 
  
Bevor Sie die neue Aufbewahrungsrichtlinie erstellen, bestimmen Sie die zusätzlichen Aufbewahrungstags, die Sie hinzufügen möchten. Eine Liste der Aufbewahrungstags, die der Standard-MRM-Richtlinie hinzugefügt werden, und Informationen zum Erstellen neuer Aufbewahrungstags finden Sie in den folgenden Themen:
  
- [Standardmäßige AufbewahrungsRichtlinie in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- [Standardordner, die Aufbewahrungsrichtlinientags unterstützen](https://go.microsoft.com/fwlink/p/?LinkId=746957)
    
- Der Abschnitt "Erstellen eines Aufbewahrungstags" im Thema [Erstellen einer Aufbewahrungsrichtlinie](https://go.microsoft.com/fwlink/p/?LinkId=404422) .
    
Sie können die EAC oder Exchange Online PowerShell verwenden, um eine Aufbewahrungsrichtlinie zu erstellen.
  
### <a name="use-the-eac-to-create-a-retention-policy"></a>Erstellen einer Aufbewahrungsrichtlinie mithilfe der Exchange-Verwaltungskonsole
  
1. Wechseln Sie in der Exchange- **Verwaltungs** \> Konsole zu **Aufbewahrungsrichtlinien**für Compliance **** ![-Verwaltung,](media/ITPro-EAC-AddIcon.gif)und klicken Sie dann auf hinzufügen.
    
2. Geben Sie auf der Seite **neue Aufbewahrungsrichtlinie** unter **Name**einen Namen ein, der den Zweck der Aufbewahrungsrichtlinie beschreibt. beispielsweise **MRM-Richtlinie für Postfächer in der Warteschleife**. 
    
3. Klicken Sie unter **Aufbewahrungstags**auf Add](media/ITPro-EAC-AddIcon.gif)-Symbol **Hinzufügen** ![.
    
4. Wählen Sie in der Liste der Aufbewahrungstags die in Schritt 1 erstellten "Wiederherstellbare Elemente" aus, und klicken Sie dann auf **Hinzufügen**.
    
    ![Auswählen des benutzerdefinierten Aufbewahrungstags für wiederherstellbare Elemente](media/eb49866b-bdef-4fcd-a6d9-01607c01249b.png)
  
5. Wählen Sie zusätzliche Aufbewahrungstags aus, die der Aufbewahrungsrichtlinie hinzugefügt werden sollen. Sie können beispielsweise die gleichen Tags hinzufügen, die in der standardmäßigen MRM-Richtlinie enthalten sind.
    
6. Wenn Sie mit dem Hinzufügen von Aufbewahrungstags fertig sind, klicken Sie auf **OK**.
    
7. Klicken Sie auf **Speichern** , um die neue Aufbewahrungsrichtlinie zu erstellen. 
    
    Beachten Sie, dass die Aufbewahrungstags, die mit der Aufbewahrungsrichtlinie verknüpft sind, im Detailbereich angezeigt werden.
    
    ![Aufbewahrungstags, die mit der Aufbewahrungsrichtlinie verknüpft sind, werden im Detailbereich angezeigt.](media/dad1c8f4-9928-4d6d-991a-6f6c5194eceb.png)
  
### <a name="use-exchange-online-powershell-to-create-a-retention-policy"></a>Verwenden von Exchange Online PowerShell zum Erstellen einer Aufbewahrungsrichtlinie
  
Führen Sie den folgenden Befehl aus, um eine neue Aufbewahrungsrichtlinie für Postfächer zu erstellen. 
  
```
New-RetentionPolicy <Name of retention policy>  -RetentionPolicyTagLinks <list of retention tags>

```

Mit dem folgenden Befehl wird beispielsweise die Aufbewahrungsrichtlinie und die verknüpften Aufbewahrungstags erstellt, die in der vorherigen Abbildung angezeigt werden.
  
```
New-RetentionPolicy "MRM Policy for Mailboxes on Hold"  -RetentionPolicyTagLinks "Recoverable Items 30 days for mailboxes on hold","1 Month Delete","1 Week Delete","1 Year Delete","5 Year Delete","6 Month Delete","Default 2 year move to archive","Junk Email","Never Delete","Personal 1 year move to archive","Personal 5 year move to archive"
```
  
## <a name="step-3-apply-the-new-retention-policy-to-mailboxes-on-hold"></a>Schritt 3: Anwenden der neuen Aufbewahrungsrichtlinie auf Postfächer in der Warteschleife

Der letzte Schritt besteht darin, die neue Aufbewahrungsrichtlinie, die Sie in Schritt 2 erstellt haben, auf Postfächer in Ihrer Organisation anzuwenden. Sie können die EAC oder Exchange Online PowerShell verwenden, um die Aufbewahrungsrichtlinie auf ein einzelnes Postfach oder auf mehrere Postfächer anzuwenden. 
  
### <a name="use-the-eac-to-apply-the-new-retention-policy"></a>Anwenden der neuen Aufbewahrungsrichtlinie mithilfe der Exchange-verwaltungsKONSOLE
  
1. Navigieren Sie zu **Empfänger** \> **Postfächer**.
    
2. Wählen Sie in der Listenansicht das Postfach aus, auf das Sie die Aufbewahrungsrichtlinie anwenden möchten, **** ![und klicken Sie](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)dann auf Bearbeitungssymbol bearbeiten.
    
3. Klicken Sie auf der Seite **Benutzerpostfach** auf **Postfachfunktionen**.
    
4. Wählen Sie unter **Aufbewahrungsrichtlinie**die Aufbewahrungsrichtlinie aus, die Sie in Schritt 2 erstellt haben, und klicken Sie dann auf **Speichern**.
    
Sie können auch die Exchange-verwaltungsKONSOLE verwenden, um die Aufbewahrungsrichtlinie auf mehrere Postfächer anzuwenden.
  
1. Navigieren Sie zu **Empfänger** \> **Postfächer**.
    
2. Verwenden Sie in der Listenansicht die UMSCHALT- oder die STRG-TASTE, um mehrere Postfächer auszuwählen.
    
3. Klicken Sie im Detailbereich auf **Weitere Optionen**.
    
4. Klicken Sie unter **Aufbewahrungsrichtlinie** auf **Aktualisieren**.
    
5. Wählen Sie auf der Seite **massenzuweisung von Aufbewahrungsrichtlinie** die Aufbewahrungsrichtlinie aus, die Sie in Schritt 2 erstellt haben, und klicken Sie dann auf **Speichern**. 
    
### <a name="use-exchange-online-powershell-to-apply-the-new-retention-policy"></a>Verwenden von Exchange Online PowerShell zum Anwenden der neuen Aufbewahrungsrichtlinie
  
Sie können Exchange Online PowerShell verwenden, um eine neue Aufbewahrungsrichtlinie auf ein einzelnes Postfach anzuwenden. Die wirkliche Leistungsfähigkeit von PowerShell besteht darin, dass Sie Sie verwenden können, um schnell alle Postfächer in Ihrer Organisation zu identifizieren, die in einem Rechtsstreit halten oder in der Lage sind, und dann die neue Aufbewahrungsrichtlinie auf alle Postfächer anwenden, die in einem einzigen Befehl aufbewahrt werden. Im folgenden finden Sie einige Beispiele für die Verwendung von Exchange PowerShell zum Anwenden einer Aufbewahrungsrichtlinie auf ein oder mehrere Postfächer. In allen Beispielen wird die in Schritt 2 erstellte Aufbewahrungsrichtlinie angewendet.
  
In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf das Postfach von Pilar Pinilla angewendet.
  
```
Set-Mailbox "Pilar Pinilla" -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf alle Postfächer in der Organisation angewendet, die in einem Rechtsstreit stehen.
  
```
$LitigationHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'}
```

```
$LitigationHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

In diesem Beispiel wird die neue Aufbewahrungsrichtlinie auf alle Postfächer in der Organisation angewendet, die sich in der Lage befinden.
  
```
$InPlaceHolds = Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null}
```

```
$InPlaceHolds.DistinguishedName | Set-Mailbox -RetentionPolicy "MRM Policy for Mailboxes on Hold"
```

Sie können das Cmdlet **Get-Mailbox** verwenden, um zu überprüfen, ob die neue Aufbewahrungsrichtlinie angewendet wurde. 
  
Im folgenden finden Sie einige Beispiele, um zu überprüfen, ob die Befehle in den vorherigen Beispielen die Aufbewahrungsrichtlinie "MRM-Richtlinie für Postfächer in der Warteschleife" auf Postfächer für die Rechtsstreitigkeit und die Postfächer in der Warteschleife angewendet haben.
  
```
Get-Mailbox "Pilar Pinilla" | Select RetentionPolicy
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.LitigationHoldEnabled -eq 'True'} | FT DisplayName,RetentionPolicy -Auto
```

```
Get-Mailbox -ResultSize unlimited | Where-Object {$_.InPlaceHolds -ne $null} | FT DisplayName,RetentionPolicy -Auto
```
  
## <a name="optional-step-4-run-the-managed-folder-assistant-to-apply-the-new-retention-settings"></a>Optional Schritt 4: Ausführen des Assistenten für verwaltete Ordner zum Anwenden der neuen Aufbewahrungseinstellungen

Nachdem Sie die neue Aufbewahrungsrichtlinie auf Postfächer angewendet haben, kann es bis zu 7 Tage dauern, bis der Assistent für verwaltete Ordner diese Postfächer mithilfe der Einstellungen in der neuen Aufbewahrungsrichtlinie verarbeitet. Anstatt auf die Ausführung des Assistenten für verwaltete Ordner zu warten, können Sie das Cmdlet **Start-ManagedFolderAssistant** verwenden, um den Assistenten manuell auszulösen, um die Postfächer zu verarbeiten, auf die Sie die neue Aufbewahrungsrichtlinie angewendet haben. 
  
Führen Sie den folgenden Befehl aus, um den Assistenten für verwaltete Ordner für das Postfach von Pilar Pinilla zu starten.
  
```
Start-ManagedFolderAssistant "Pilar Pinilla"
```

Führen Sie die folgenden Befehle aus, um den Assistenten für verwaltete Ordner für alle warte Schleifer zu starten.
  
```
$MailboxesOnHold = Get-Mailbox -ResultSize unlimited | Where-Object {($_.InPlaceHolds -ne $null) -or ($_.LitigationHoldEnabled -eq "True")}
```

```
$MailboxesOnHold.DistinguishedName | Start-ManagedFolderAssistant
```

## <a name="more-information"></a>Weitere Informationen

- Nachdem Sie das Archivpostfach eines Benutzers aktiviert haben, sollten Sie dem Benutzer mitteilen, dass andere Elemente in Ihrem Postfach (nicht nur Elemente im Ordner "Wiederherstellbare Elemente") möglicherweise in das Archivpostfach verschoben werden. Der Grund ist, dass die standardmäßige MRM-Richtlinie, die Exchange Online-Postfächern zugewiesen ist, ein Aufbewahrungs (Standard 2 Jahre in Archiv verschieben) enthält, das zwei Jahre nach dem Datum, an dem das Element an das Postfach zugestellt oder vom Benutzer. Weitere Informationen finden Sie unter [standardmäßige Aufbewahrungsrichtlinie in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkId=746954)
    
- Nachdem Sie das Archivpostfach eines Benutzers aktiviert haben, können Sie auch dem Benutzer mitteilen, dass er gelöschte Elemente im Ordner "Wiederherstellbare Elemente" im Archivpostfach zurücksetzen kann. Sie können dies in Outlook tun, indem Sie den Ordner " **Gelöschte Elemente** " im Archivpostfach auswählen und dann auf der Registerkarte **Start** auf **Gelöschte Elemente vom Server wiederherstellen** klicken. Weitere Informationen zum Wiederherstellen gelöschter Elemente finden Sie unter [Recover Deleted Items in Outlook for Windows](https://go.microsoft.com/fwlink/p/?LinkId=624829). 
