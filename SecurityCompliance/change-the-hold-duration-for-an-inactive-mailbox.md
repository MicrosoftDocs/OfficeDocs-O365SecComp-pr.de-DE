---
title: Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 8/29/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: bdee24ed-b8cf-4dd0-92ae-b86ec4661e6b
description: Nach der Deaktivierung eines Office 365-Postfachs können Sie die Dauer des Haltestatus oder die der dem inaktiven Postfach zugewiesene Aufbewahrungsrichtlinie für Office 365 ändern. Die Aufbewahrungsdauer definiert, wie lange Elemente im Ordner "Wiederherstellbare Elemente" aufbewahrt werden.
ms.openlocfilehash: 3f92d51505ba8a9a9f4b8e78d0fb79036b6db489
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220615"
---
# <a name="change-the-hold-duration-for-an-inactive-mailbox-in-office-365"></a>Ändern der Aufbewahrungsdauer für ein inaktives Postfach in Office 365

Ein inaktives Postfach wird verwendet, um die E-Mails eines ehemaligen Mitarbeiters aufzubewahren, nachdem dieser die Organisation verlassen hat. Ein Postfach wird inaktiv, wenn das Postfach in einem Beweissicherungsverfahren, in einem In-Situ-Speicher, in einer Office 365-Aufbewahrungsrichtlinie oder in einem Haltebereich platziert, der mit einem eDiscovery-Fall verknüpft ist, und das entsprechende Office 365-Benutzerkonto gelöscht wird. Die Inhalte eines inaktiven Postfachs werden für die Dauer der Archivierung beibehalten, die für das Postfach aktiviert wurde, bevor es inaktiv gemacht wurde. Die Aufbewahrungsdauer definiert die Aufbewahrungsdauer von Elementen im Ordner „Wiederherstellbare Elemente". Wenn die Aufbewahrungsdauer für ein Element im Ordner „Wiederherstellbare Elemente" abläuft, wird das Element dauerhaft aus dem inaktiven Postfach gelöscht. Nachdem ein Postfach als inaktiv markiert wurde, können Sie die Aufbewahrungsdauer oder die Office 365-Aufbewahrungsrichtlinie für das inaktive Postfach ändern.
  
> [!IMPORTANT]
> Wir haben den Stichtag (1. Juli 2017) zum Erstellen von neuem In-Situ-Speicher, um ein Postfach als inaktiv zu markieren, nach hinten verlegt. Ende dieses Jahres oder Anfang des nächsten Jahres können Sie keinen neuen In-Situ-Speicher in Exchange Online mehr erstellen. Es können dann nur noch das Beweissicherungsverfahren und Office 365-Aufbewahrungsrichtlinien zum Erstellen eines inaktiven Postfachs verwendet werden. Vorhandene inaktive Postfächer, die sich im In-Situ-Speicher befinden, werden jedoch weiterhin unterstützt, und Sie können weiterhin die In-Situ-Speicher für inaktive Postfächer verwalten. Dazu zählen das Ändern der Dauer eines In-Situ-Speichers sowie das dauerhafte Löschen eines inaktiven Postfachs durch Entfernen des In-Situ-Speichers. 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Zum Ändern der Aufbewahrungsdauer für ein Beweissicherungsverfahren für ein aktives Postfach müssen Sie die Exchange Online PowerShell verwenden. Sie können nicht die Exchange-Verwaltungskonsole (EAC) verwenden. Sie können Exchange Online PowerShell oder die Exchange-Verwaltungskonsole jedoch verwenden, um die Aufbewahrungsdauer für einen In-Situ-Speicher zu ändern. Sie können die Office 365 Security &amp; Compliance Center oder die Security &amp; Compliance Center PowerShell zum Ändern der Aufbewahrungsdauer für eine Office 365-Aufbewahrungsrichtlinie verwenden.
    
- Informationen zum Herstellen einer Verbindung mit Exchange Online PowerShell oder Security &amp; Compliance Center PowerShell finden Sie in den folgenden Themen:
    
  - [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?linkid=396554).
    
  - [Herstellen einer Verbindung mit Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/?linkid=799771)
    
- Beachten Sie, dass Haltebereiche, die eDiscovery-Fällen zugeordnet sind, unendliche Haltebereiche sind, was bedeutet, dass es keine Dauer gibt, die geändert werden kann. Elemente werden dauerhaft aufbewahrt oder bis der Haltebereich entfernt wird und das inaktive Postfach gelöscht wird.
    
- Weitere Informationen zu inaktiven Postfächern finden Sie unter inAktive [Postfächer in Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>Schritt 1: Identifizieren der Haltebereiche für ein inaktives Postfach

Da unterschiedliche Haltebereiche oder eine oder mehrere Office 365-Aufbewahrungsrichtlinien für ein inaktives Postfach aktiviert werden können, besteht der erste Schritt darin, die Haltebereiche für ein inaktives Postfach zu identifizieren.
  
Führen Sie in Exchange Online PowerShell den folgenden Befehl aus, um die Informationen zu Haltebereichen für alle inaktiven Postfächer in Ihrer Organisation anzuzeigen.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,LitigationHoldDuration,InPlaceHolds
```
   
Der Wert von **true** für die **LitigationHoldEnabled** -Eigenschaft gibt an, dass das inaktive Postfach in einem Rechtsstreit gehalten wird. Wenn ein in-situ-Speicher, eine eDiscovery-Speicherung oder eine Office 365-Aufbewahrungsrichtlinie in einem inaktiven Postfach platziert wird, wird als Wert für die **InPlaceHolds** -Eigenschaft eine GUID für die halte-oder Aufbewahrungsrichtlinie angezeigt. Das folgende Beispiel zeigt die Ergebnisse für 5 inaktive Postfächer. 
  
||
|:-----|
|
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
LitigationHoldDuration: 365.00:00:00
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491}
...
DisplayName           : Mario Necaise
Name                  : marion
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {}
...
DisplayName           : Carol Olson
Name                  : carolo
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {mbxcdbbb86ce60342489bff371876e7f224}
...
DisplayName           : Abraham McMahon
Name                  : abrahamm
IsInactiveMailbox     : True
LitigationHoldEnabled : False
LitigationHoldDuration: Unlimited
InPlaceHolds          : {UniH7d895d48-7e23-4a8d-8346-533c3beac15d}
```
   
In der folgenden Tabelle sind fünf unterschiedliche Haltebereichstypen aufgeführt, die verwendet wurden, um die einzelnen Postfächer als inaktiv zu markieren.
  
|**Inaktives Postfach**|**Haltebereichstyp**|**Wie Sie den Haltebereich für das inaktive Postfach erkennen**|
|:-----|:-----|:-----|
|Ann Beebe  <br/> |Beweissicherungsverfahren  <br/> |Die  *LitigationHoldEnabled*  -Eigenschaft wird festgelegt auf  `True`.  <br/> |
|Pilar Pinilla  <br/> |Compliance-Archiv  <br/> |Die  *InPlaceHolds*  -Eigenschaft enthält die GUID des In-Situ-Speichers, in dem das inaktive Postfach platziert wird. Sie können erkennen, dass es sich hierbei um einen In-Situ-Speichern handelt, da die ID nicht mit einem Präfix beginnt.  <br/> Sie können den `Get-MailboxSearch -InPlaceHoldIdentity <hold GUID> | FL` Befehl in Exchange Online PowerShell verwenden, um Informationen zum in-situ-Speicher für das inaktive Postfach zu erhalten.  <br/> |
|Mario Necaise  <br/> |Organisationsweite Office 365-Aufbewahrungsrichtlinie in der Security &amp; Compliance Center  <br/> |Die *InPlaceHolds* -Eigenschaft ist leer. Dies weist darauf hin, dass eine oder mehrere organisationsweite oder (Exchange-weite) Office 365-Aufbewahrungsrichtlinien auf das inaktive Postfach angewendet werden. In diesem Fall können Sie den `Get-OrganizationConfig | Select-Object -ExpandProperty InPlaceHolds` Befehl in Exchange Online PowerShell ausführen, um eine Liste der GUIDs für organisationsweite Office 365-Aufbewahrungsrichtlinien abzurufen. Die GUID für organisationsweite Aufbewahrungsrichtlinien, die auf Exchange-Postfächer angewendet werden `mbx` , beginnen mit dem Präfix; Beispiel `mbxa3056bb15562480fadb46ce523ff7b02`.<br/> <br/>Führen Sie den folgenden Befehl in Security &amp; Compliance Center PowerShell aus, um die Office 365-Aufbewahrungsrichtlinie zu ermitteln, die auf das inaktive Postfach angewendet wird.  <br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name`<br/><br/>
|Carol Olson  <br/> |Office 365-Aufbewahrungsrichtlinie in Security &amp; Compliance Center angewendet auf bestimmte Postfächer  <br/> |Die  *InPlaceHolds*  -Eigenschaft enthält die GUID der Office 365-Aufbewahrungsrichtlinie, die auf das inaktive Postfach angewendet wird. Sie können erkennen, dass es sich hierbei um eine Aufbewahrungsrichtlinie handelt, die auf bestimmte Postfächer angewendet wurde, da die GUID mit dem Präfix  `mbx` beginnt. Wenn die GUID der Aufbewahrungsrichtlinie, die auf das inaktive Postfach angewendet wird, mit dem Präfix  `skp` beginnt, würde dies darauf hindeuten, dass die Aufbewahrungsrichtlinie auf Skype for Business-Unterhaltungen angewendet wird.  <br/><br/> Führen Sie den folgenden Befehl in Security &amp; Compliance Center PowerShell aus, um die Office 365-Aufbewahrungsrichtlinie zu ermitteln, die auf das inaktive Postfach angewendet wird.<br/><br/> `Get-RetentionCompliancePolicy <retention policy GUID without prefix> | FL Name` <br/><br/>Entfernen Sie unbedingt das `mbx` Präfix oder `skp` , wenn Sie diesen Befehl ausführen.  <br/> |
|Abraham McMahon  <br/> |eDiscovery-Fall in der Security &amp; Compliance Center  <br/> |Die  *InPlaceHolds*  -Eigenschaft enthält die GUID des eDiscovery-Falls, in dem das inaktive Postfach platziert wird. Sie können erkennen, dass es sich hierbei um einen eDiscovery-Fall handelt, da die GUID mit dem Präfix  `UniH` beginnt.  <br/> Sie können das `Get-CaseHoldPolicy` Cmdlet im Security &amp; Compliance Center PowerShell verwenden, um Informationen über den eDiscovery-Fall abzurufen, dem der Haltebereich für das inaktive Postfach zugeordnet ist. Sie können beispielsweise den Befehl `Get-CaseHoldPolicy <hold GUID without prefix> | FL Name` ausführen, um den Namen der Groß-/Kleinschreibung für das inaktive Postfach anzuzeigen. Achten Sie darauf, das `UniH` Präfix zu entfernen, wenn Sie diesen Befehl ausführen.<br/><br/> Führen Sie die folgenden Befehle aus, um den eDiscovery-Fall zu identifizieren, mit dem der Haltebereich für das inaktive Postfach verknüpft ist.  <br/><br/> `$CaseHold = Get-CaseHoldPolicy <hold GUID without prefix>`<br/><br/> `Get-ComplianceCase $CaseHold.CaseId | FL Name`<br/><br/><br/> **Hinweis:** Es wird nicht empfohlen, eDiscovery-Speicher für inaktive Postfächer zu verwenden. Das liegt daran, dass eDiscovery-Fälle für bestimmte, zeitlich gebundene Fälle im Zusammenhang mit einem rechtlichen Problem vorgesehen sind. Zu einem bestimmten Zeitpunkt wird möglicherweise ein Rechtsstreit beendet, und die dem Fall zugeordneten haltebereiche werden entfernt, und der eDiscovery-Fall wird geschlossen (oder gelöscht). Wenn ein Haltebereich in einem inaktiven Postfach einem eDiscovery-Fall zugeordnet ist und der Haltestatus freigegeben oder der eDiscovery-Fall geschlossen oder gelöscht wird, wird das inaktive Postfach dauerhaft gelöscht. 

Weitere Informationen zu Office 365-Aufbewahrungsrichtlinien finden Sie unter [Übersicht über Aufbewahrungsrichtlinien](retention-policies.md).
  
## <a name="step-2-change-the-hold-duration-for-an-inactive-mailbox"></a>Schritt 2: Ändern der Aufbewahrungsdauer für ein inaktives Postfach

Nachdem Sie ermittelt haben, welche Art von Haltebereich für das inaktive Postfach aktiviert ist (und ob es mehrere Haltebereiche gibt), wird im nächsten Schritt die Dauer des Haltebereichs geändert. 
  
### <a name="change-the-duration-for-a-litigation-hold"></a>Ändern der Dauer für ein Beweissicherungsverfahren

Im Folgenden erfahren Sie, wie Sie die Exchange Online PowerShell zum Ändern der Aufbewahrungsdauer für ein Beweissicherungsverfahren verwenden, das auf einem inaktiven Postfach platziert wird. Sie können nicht die EAC verwenden. Führen Sie zum Ändern der Aufbewahrungsdauer den folgenden Befehl aus. In diesem Beispiel wird die Aufbewahrungsdauer auf unbegrenzt festgelegt.
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldDuration unlimited
```

Dadurch werden die Elemente im inaktiven Postfach unbegrenzt beibehalten oder bis der Haltebereich entfernt oder die Aufbewahrungsdauer in einen anderen Wert geändert wird.
  
> [!TIP]
> Die beste Methode zum Identifizieren eines inaktiven Postfachs ist die Verwendung des **Distinguished Name** oder des **Exchange GUID** -Werts. Durch Verwenden eines dieser Werte können Sie verhindern, versehentlich das falsche Postfach anzugeben. 
  
### <a name="change-the-duration-for-an-in-place-hold"></a>Ändern der Dauer für einen In-Situ-Speicher

 Sie können die Exchange-Verwaltungskonsole oder Exchange Online PowerShell zum Ändern der Aufbewahrungsdauer für einen In-Situ-Speicher verwenden. 
  
#### <a name="use-the-eac-to-change-the-hold-duration"></a>Verwenden von EAC zum Ändern der Aufbewahrungsdauer

1. Wenn Sie den Namen des in-situ-Speichers kennen, den Sie ändern möchten, fahren Sie mit dem nächsten Schritt fort. Führen Sie andernfalls den folgenden Befehl aus, um den Namen des in-situ-Speichers abzurufen, der im inaktiven Postfach platziert wird. Verwenden Sie die in-situ-Aufbewahrungs-GUID, die Sie in [Schritt 1](#step-1-identify-the-holds-on-an-inactive-mailbox)abgerufen haben.

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.
    
3. Wählen Sie den in-situ-Speicher aus, den Sie ändern möchten **** ![, und klicken](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif)Sie dann auf Bearbeitungssymbol bearbeiten.
    
4. Klicken Sie auf der Eigenschaftenseite für den **in-situ-eDiscovery &amp; ** -Speicher auf **in-situ-Aufbewahrung**. 
    
5. Nehmen Sie auf Grundlage der aktuellen Aufbewahrungsdauer eine der folgenden Aktionen vor:
    
1. Klicken Sie auf **Dauerhaft aufbewahren**, um Elemente für einen unbegrenzten Zeitraum aufzubewahren. 
    
2. Klicken Sie auf **Anzahl von Tagen angeben, die Elemente in Bezug auf Ihr Empfangsdatum enthalten** sollen, um Elemente für einen bestimmten Zeitraum aufzubewahren. Geben Sie die Anzahl der Tage ein, für die Sie Elemente speichern möchten. 
    
    ![Screenshot: Ändern der Dauer für einen In-Situ-Speicher](media/cfcfd92a-9d65-40c0-90ef-ab72697b0166.png)
  
6. Klicken Sie auf **Speichern**.
    
#### <a name="use-exchange-online-powershell-to-change-the-hold-duration"></a>Verwenden von Exchange Online PowerShell zum Ändern der Aufbewahrungsdauer

1. Wenn Sie den Namen des in-situ-Speichers kennen, den Sie ändern möchten, fahren Sie mit dem nächsten Schritt fort. Führen Sie andernfalls den folgenden Befehl aus, um den Namen des in-situ-Speichers abzurufen, der im inaktiven Postfach platziert wird. Verwenden Sie die in-situ-Aufbewahrungs-GUID, die Sie in [Schritt 1](#step-1-identify-the-holds-on-an-inactive-mailbox)abgerufen haben.

    ```
    Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
    ```

2. Führen Sie zum Ändern der Aufbewahrungsdauer den folgenden Befehl aus. In diesem Beispiel wird die Aufbewahrungsdauer in 2.555 Tage (etwa 7 Jahre) geändert. 
    
    ```
    Set-MailboxSearch <identity of In-Place Hold> -ItemHoldPeriod 2555
    ```

     Verwenden Sie  _-ItemHoldPeriod unlimited_, um die Aufbewahrungsdauer in einen unbegrenzten Zeitraum zu ändern.
  
## <a name="more-information"></a>Weitere Informationen

- **Wie wird die Aufbewahrungsdauer für ein Element in einem inaktiven Postfach berechnet?** Die Dauer wird anhand des ursprünglichen Datums berechnet, an dem ein Postfach empfangen oder erstellt wurde. 
    
- **Was geschieht, wenn die Aufbewahrungsdauer abläuft?** Wenn die Aufbewahrungsdauer für ein Postfachelement im Ordner „Wiederherstellbare Elemente" abläuft, wird das Element dauerhaft aus dem inaktiven Postfach gelöscht. Wenn für den auf dem inaktiven Postfach platzierten Haltebereich keine Dauer angegeben ist, werden Elemente im Ordner „Wiederherstellbare Elemente" niemals gelöscht (es sei denn, die Aufbewahrungsdauer für das inaktive Postfach wird geändert). 
    
- **Wird eine Exchange-Aufbewahrungsrichtlinie für inaktive Postfächer weiterhin verarbeitet?** Wenn eine Exchange-Aufbewahrungsrichtlinie (Messaging-Datensatzverwaltung, MRM-Funktion inExchange Online) auf ein Postfach angewendet wurde, als es als inaktiv markiert wurde, werden die Löschrichtlinien (hierbei handelt es sich um Aufbewahrungstags mit der Aufbewahrungsaktion **Delete** ) weiterhin auf das inaktive Postfach angewendet. Mit einer Löschrichtlinie markierte Elemente werden demnach in den Ordner „Wiederherstellbare Elemente" verschoben, wenn die Aufbewahrungsrichtlinie abläuft. Diese Elemente werden dann aus dem inaktiven Postfach gelöscht, wenn die Aufbewahrungsdauer für ein Element abläuft. 
    
    Umgekehrt werden einem inaktiven Postfach zugewiesene Archivrichtlinien (mit der Aufbewahrungsaktion **MoveToArchive** konfigurierte Aufbewahrungstags) ignoriert, die in der Aufbewahrungsrichtlinie enthalten sind. Elemente in einem inaktiven Postfach, die mit einer Archivrichtlinie markiert sind, verbleiben demnach im primären Postfach, wenn die Aufbewahrungsdauer abläuft. Sie werden nicht in das Archivpostfach oder in den Ordner „Wiederherstellbare Elemente" im Archivpostfach verschoben. Da sich ein Benutzer nicht an einem inaktiven Postfach anmelden kann, gibt es keinen Grund, Rechenzentrumsressourcen für das Verarbeiten von Archivrichtlinien zu verwenden. 
    
- **Führen Sie einen der folgenden Befehle aus, um die neue Aufbewahrungsdauer zu überprüfen.** Der erste Befehl ist für das Beweissicherungsverfahren, der zweite für den In-Situ-Speicher. 

    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | FL LitigationHoldDuration
    ```

    ```
    Get-MailboxSearch <identity of In-Place Hold> | FL ItemHoldPeriod
    ```

- **Wie bei regulären Postfächern verarbeitet der Assistent für verwaltete Ordner auch inaktive Postfächer.** In Exchange Online verarbeitet der Assistent für verwaltete Ordner Postfächer einmal alle sieben Tage. Nachdem Sie die Aufbewahrungsdauer für ein inaktives Postfach geändert haben, können Sie das Cmdlet **Start-ManagedFolderAssistant** verwenden, um die Verarbeitung der neuen Aufbewahrungsdauer für das inaktive Postfach sofort zu starten. Führen Sie den folgenden Befehl aus. 

    ```
    Start-ManagedFolderAssistant -InactiveMailbox <identity of inactive mailbox>
    ```
   
- **Wenn viele Haltebereiche für ein inaktives Postfach aktiviert werden, werden nicht alle Haltebereich-GUIDs angezeigt.** Sie können den folgenden Befehl ausführen, um die GUIDs für alle Haltebereiche (mit Ausnahme von Beweissicherungsverfahren) für ein inaktives Postfach anzuzeigen. 
    
    ```
    Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds
    ```
