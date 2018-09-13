---
title: Löschen eines inaktiven Postfachs in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: f5caf497-5e8d-4b7a-bfff-d02942f38150
description: Wenn Sie nicht mehr den Inhalt eines inaktiven Postfachs für Office 365 beibehalten möchten, können Sie dauerhaft inaktive Postfach löschen, durch den Haltestatus entfernen. Nach dem Entfernen des Haltestatus, inaktive Postfach ist zum Löschen markiert und wird endgültig gelöscht werden, nachdem sie verarbeitet wird.
ms.openlocfilehash: a7284be650d7ec6c89a6fdc43d8614603d6f1e19
ms.sourcegitcommit: 82fd4c85b952819157fbb13175c7b2dbbdff510f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/13/2018
ms.locfileid: "23965252"
---
# <a name="delete-an-inactive-mailbox-in-office-365"></a>Löschen eines inaktiven Postfachs in Office 365

Ein inaktives Postfach wird verwendet, um die E-Mails eines ehemaligen Mitarbeiters aufzubewahren, nachdem dieser die Organisation verlassen hat. Wenn Sie die Inhalte eines inaktiven Postfachs nicht mehr aufbewahren müssen, können Sie das inaktive Postfach durch Entfernen des Haltebereichs endgültig löschen. Darüber hinaus ist es möglich, mehrere Haltebereiche für ein inaktives Postfach festzulegen. Beispielsweise kann für ein inaktives Postfach ein Beweissicherungsverfahren aktiviert oder das Postfach in einem oder mehreren In-Situ-Speichern abgelegt werden. Außerdem kann eine Office 365-Aufbewahrungsrichtlinie (erstellt in der Office 365 Security &amp; Compliance Center) auf ein inaktives Postfach angewendet werden. Sie müssen alle Haltebereiche und Office 365-Aufbewahrungsrichtlinien von einem inaktiven Postfach entfernen, um dieses löschen zu können. Nach dem Entfernen der Haltebereiche und Aufbewahrungsrichtlinien wird das inaktive Postfach zum Löschen markiert und endgültig gelöscht, nachdem es verarbeitet wurde.
  
> [!IMPORTANT]
> Wir haben den Stichtag (1. Juli 2017) zum Erstellen von neuem In-Situ-Speicher, um ein Postfach als inaktiv zu markieren, nach hinten verlegt. Ende dieses Jahres oder Anfang des nächsten Jahres können Sie keinen neuen In-Situ-Speicher in Exchange Online mehr erstellen. Es können dann nur noch das Beweissicherungsverfahren und Office 365-Aufbewahrungsrichtlinien zum Erstellen eines inaktiven Postfachs verwendet werden. Vorhandene inaktive Postfächer, die sich im In-Situ-Speicher befinden, werden jedoch weiterhin unterstützt, und Sie können weiterhin die In-Situ-Speicher für inaktive Postfächer verwalten. Dazu zählen das Ändern der Dauer eines In-Situ-Speichers sowie das dauerhafte Löschen eines inaktiven Postfachs durch Entfernen des In-Situ-Speichers. 
  
Eine Beschreibung dessen, was geschieht, wenn Haltebereiche von einem inaktiven Postfach entfernt werden, finden Sie im Abschnitt [Weitere Informationen](delete-an-inactive-mailbox.md#moreinfo). 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen Exchange Online PowerShell verwenden, um eine Aufbewahrung für eventuelle Rechtsstreitigkeiten aus eines inaktiven Postfachs zu entfernen. Sie können nicht im Exchange Administrationscenter (EAC) verwenden. Schrittweise Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://go.microsoft.com/fwlink/?linkid=396554). Exchange Online PowerShell oder der Exchange-Verwaltungskonsole können Sie um eine In-Place Hold aus eines inaktiven Postfachs zu entfernen. 
    
- Sie können den Inhalt eines inaktiven Postfachs an ein anderes Postfach kopieren, bevor Sie den Haltestatus entfernen und eines inaktiven Postfachs löschen. Weitere Informationen hierzu finden Sie unter [Wiederherstellen ein inaktives Postfachs in Office 365](restore-an-inactive-mailbox.md).
    
- Wenn Sie die Warteschleife oder Office 365 Aufbewahrungsrichtlinie aus eines inaktiven Postfachs entfernen und die Aufbewahrungsdauer vorläufig gelöschte Postfach für das Postfach abgelaufen, wird das Postfach endgültig gelöscht werden. Nachdem sie gelöscht wurde, kann es nicht wiederhergestellt werden. Bevor Sie den Haltestatus entfernen, achten Sie darauf, dass Sie den Inhalt im Postfach nicht mehr benötigen. Erneutes Aktivieren ein inaktives Postfachs werden soll, können Sie sie wiederherstellen. Weitere Informationen hierzu finden Sie unter [Wiederherstellen ein inaktives Postfachs in Office 365](recover-an-inactive-mailbox.md).
    
- Weitere Informationen zu inaktiver Postfächer finden Sie unter [inaktiver Postfächer in Office 365](inactive-mailboxes-in-office-365.md).
    
## <a name="step-1-identify-the-holds-on-an-inactive-mailbox"></a>Schritt 1: Identifizieren der Haltebereiche für ein inaktives Postfach

Wie bereits erwähnt, kann ein Beweissicherungsverfahren, ein In-Situ-Speicher oder eine Office 365-Aufbewahrungsrichtlinie für ein inaktives Postfach aktiviert werden. Der erste Schritt besteht darin, die Haltebereiche für ein inaktives Postfach zu identifizieren.
  
Führen Sie den folgenden Befehl aus, um die Informationen zu Haltebereichen für alle inaktiven Postfächer in Ihrer Organisation anzuzeigen.
  
```
Get-Mailbox -InactiveMailboxOnly | FL DisplayName,Name,IsInactiveMailbox,LitigationHoldEnabled,InPlaceHolds
```

Der Wert **True** für die Eigenschaft **LitigationHoldEnabled** gibt an, dass für das inaktive Postfach ein Beweissicherungsverfahren aktiviert ist. Wenn ein In-Situ-Speicher für ein inaktives Postfach aktiviert ist, wird die GUID für den Haltebereich als Wert für die Eigenschaft **InPlaceHolds** angezeigt. Die folgenden Ergebnisse für zwei inaktive Postfächer zeigen beispielsweise, dass für Ann Beebe ein Beweissicherungsverfahren und für Pilar Pinilla zwei In-Situ-Speicher aktiviert wurden. 
  
```
DisplayName           : Ann Beebe
Name                  : annb
IsInactiveMailbox     : True
LitigationHoldEnabled : True
InPlaceHolds          : {}
...
DisplayName           : Pilar Pinilla
Name                  : pilarp
IsInactiveMailbox     : True
LitigationHoldEnabled : False
InPlaceHolds          : {c0ba3ce811b6432a8751430937152491, ba6f4ba25b62490aaaa253eea27426ab}
```

> [!TIP]
> Wenn ein Großteil der Compliance-Archive eines inaktiven Postfachs platziert werden, wird die Compliance-Archiv-GUIDs nicht alle angezeigt. Führen Sie den folgenden Befehl aus, um alle Compliance-Archiv GUIDs anzuzeigen:`Get-Mailbox -InactiveMailboxOnly -Identity <identity of inactive mailbox> | Select-Object -ExpandProperty InPlaceHolds`
  
## <a name="step-2-remove-a-hold-from-an-inactive-mailbox"></a>Schritt 2: Entfernen eines Haltebereichs von einem inaktiven Postfach

Nachdem Sie ermittelt haben, welche Art von Haltebereich für das inaktive Postfach aktiviert ist (und ob es mehrere Haltebereiche gibt), werden im nächsten Schritt die Haltebereiche für das Postfach entfernt. Wie bereits erwähnt, müssen Sie alle Haltebereiche entfernen, um ein inaktives Postfach endgültig zu entfernen. 
  
### <a name="remove-a-litigation-hold"></a>Entfernen eines Beweissicherungsverfahrens

Wie bereits erwähnt, müssen Sie Windows PowerShell verwenden, um ein Beweissicherungsverfahren von einem inaktiven Postfach zu entfernen. Sie können nicht die EAC verwenden. Führen Sie den folgenden Befehl aus, um ein Beweissicherungsverfahren zu entfernen.
  
```
Set-Mailbox -InactiveMailbox -Identity <identity of inactive mailbox> -LitigationHoldEnabled $false
```

> [!TIP]
> Die beste Methode zum Identifizieren eines inaktiven Postfachs ist die Verwendung des Distinguished Name oder des Exchange-GUID-Werts. Durch Verwenden eines dieser Werte können Sie verhindern, versehentlich das falsche Postfach anzugeben. 
  
### <a name="remove-in-place-holds"></a>Entfernen von In-Situ-Speichern

 Es gibt zwei Möglichkeiten, um einen In-Situ-Speicher von einem inaktiven Postfach zu entfernen: 
  
- **Löschen Sie das Objekt In-Place Hold** Wenn das inaktive Postfach, das Sie dauerhaft löschen möchten das einzige Quellpostfach für eine In-Place Hold ist, können Sie einfach das In-Place Hold-Objekt löschen. 
    
    > [!NOTE]
    > Sie müssen den Haltebereich deaktivieren, bevor Sie ein In-Situ-Speicherobjekt löschen können. Wenn Sie versuchen, ein In-Situ-Speicherobjekt zu löschen, dessen Haltebereich aktiviert ist, wird eine Fehlermeldung angezeigt. 
  
- **Entfernen des inaktiven Postfachs als Quellpostfach für einen In-Situ-Speicher** Wenn Sie andere Quellpostfächer für einen In-Situ-Speicher beibehalten möchten, können Sie das inaktive Postfach aus der Liste der Quellpostfächer entfernen und das In-Situ-Speicherobjekt beibehalten. 
    
#### <a name="use-the-eac-to-delete-an-in-place-hold"></a>Verwenden der EAC zum Löschen eines In-Situ-Speichers

1. Wenn Sie den Namen des zu löschenden In-Situ-Speichers kennen, können Sie mit dem nächsten Schritt fortfahren. Andernfalls führen Sie den folgenden Befehl aus, um den Namen des In-Situ-Speichers abzurufen, der für das endgültig zu löschende inaktive Postfach aktiviert ist. Verwenden Sie die In-Situ-Speicher-GUID, die Sie in [Schritt 1: Identifizieren der Haltebereiche für ein inaktives Postfach](delete-an-inactive-mailbox.md#step1) abgerufen haben.
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.
    
3. Wählen Sie die In-Place Hold, die Sie löschen möchten, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
4. Klicken Sie auf der **Compliance-eDiscovery &amp; halten** Eigenschaften Seite auf **Compliance-Archiv**, deaktivieren Sie das Kontrollkästchen **die Suchabfrage im ausgewählten Postfächer auf übereinstimmende Place Inhalte enthalten** , und klicken Sie dann auf **Speichern**.
    
5. Klicken Sie auf der **Compliance-eDiscovery &amp; halten** Seite, aktivieren Sie das Compliance-Archivs wieder, und klicken Sie dann auf **Löschen**![Löschsymbol](media/87565fbb-5147-4f22-9ed7-1c18ce664392.png).
    
6. Klicken Sie in der Warnung auf **Ja**, um den In-Situ-Speicher zu löschen. 
    
#### <a name="use-exchange-online-powershell-to-delete-an-in-place-hold"></a>Verwenden von Exchange Online PowerShell zum Löschen eines In-Situ-Speichers

1. Erstellen Sie eine Variable, die die Eigenschaften des zu löschenden In-Situ-Speichers enthält. Verwenden Sie die In-Situ-Speicher-GUID, die Sie in [Schritt 1: Identifizieren der Haltebereiche für ein inaktives Postfach](delete-an-inactive-mailbox.md#step1) abgerufen haben.
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. Deaktivieren Sie den Haltebereich für den In-Situ-Speicher.
    
```
  Set-MailboxSearch $InPlaceHold.Name -InPlaceHoldEnabled $false
```

3. Löschen Sie den In-Situ-Speicher.
    
```
  Remove-MailboxSearch $InPlaceHold.Name
```

#### <a name="use-the-eac-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>Verwenden der EAC zum Entfernen eines inaktiven Postfachs aus einem In-Situ-Speicher

1. Wenn Sie den Namen des In-Situ-Speichers kennen, der dem inaktiven Postfach zugeordnet ist, können Sie mit dem nächsten Schritt fortfahren. Führen Sie andernfalls den folgenden Befehl aus, um den Namen des In-Situ-Speichers abzurufen, der dem Postfach zugeordnet ist. Verwenden Sie die In-Situ-Speicher-GUID, die Sie in [Schritt 1: Identifizieren der Haltebereiche für ein inaktives Postfach](delete-an-inactive-mailbox.md#step1) abgerufen haben.
    
```
  Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID> | FL Name
```

2. Navigieren Sie in EAC zu **Verwaltung der Richtlinientreue** \> **In-Situ-eDiscovery &amp; Haltebereich**.
    
3. Wählen Sie die In-Place Hold, die für das inaktive Postfach befindet, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/ebd260e4-3556-4fb0-b0bb-cc489773042c.gif).
    
4. Klicken Sie auf der **Compliance-eDiscovery &amp; halten** Eigenschaften auf **Inhaltsquellen**.
    
5. Klicken Sie in der Liste der Quellpostfächer auf den Namen des inaktiven Postfachs, das Sie entfernen möchten, und dann auf **Entfernen**![Entfernen (Symbol)](media/adf01106-cc79-475c-8673-065371c1897b.gif).
    
6. Klicken Sie zum Speichern der Änderung auf **Speichern**. Eine Meldung wird angezeigt, dass der Vorgang erfolgreich abgeschlossen wurde. 
    
7. Wiederholen Sie die Schritte 1 bis 6, um andere In-Situ-Speicher zu entfernen, die dem inaktiven Postfach zugeordnet sind.
    
#### <a name="use-exchange-online-powershell-to-remove-an-inactive-mailbox-from-an-in-place-hold"></a>Verwenden der Exchange Online PowerShell zum Entfernen eines inaktiven Postfachs aus einem In-Situ-Speicher

Wenn der In-Situ-Speicher eine große Anzahl von Postfächern enthält, ist das inaktive Postfach möglicherweise nicht auf der Seite **Quellen** in der Exchange-Verwaltungskonsole aufgelistet. Bis zu 3.000 Postfächer werden auf der Seite **Quellen** angezeigt, wenn Sie einen In-Situ-Speicher bearbeiten. Wenn ein inaktives Postfach nicht auf der Seite **Quellen** aufgelistet ist, können Sie Exchange Online PowerShell verwenden, um es aus dem In-Situ-Speicher zu entfernen. 
  
1. Erstellen Sie eine Variable, die die Eigenschaften des In-Situ-Speichers enthält, der dem inaktiven Postfach zugeordnet ist. Verwenden Sie die In-Situ-Speicher-GUID, die Sie in [Schritt 1: Identifizieren der Haltebereiche für ein inaktives Postfach](delete-an-inactive-mailbox.md#step1) abgerufen haben.
    
```
  $InPlaceHold = Get-MailboxSearch -InPlaceHoldIdentity <In-Place Hold GUID>
```

2. Stellen Sie sicher, dass das inaktive Postfach als ein Quellpostfach für den In-Situ-Speicher aufgelistet ist. 
    
```
  $InPlaceHold.Sources
```

   **Hinweis:** Die *Quellen* -Eigenschaft der In-Place Hold identifiziert die Quellpostfächer durch ihre *LegacyExchangeDN* -Eigenschaften. Da diese Eigenschaft inaktiver Postfächer eindeutig identifiziert wird, kann mithilfe der *Quellen* -Eigenschaft aus der In-Place Hold zu verhindern, dass das falsche Postfach entfernen. Dadurch wird auch um Probleme zu vermeiden, wenn zwei Postfächer die gleichen Alias oder die SMTP-Adresse verfügen. 
   
3. Entfernen Sie das inaktive Postfach aus der Liste der Quellpostfächer in der Variablen. Achten Sie darauf, die Eigenschaft **LegacyExchangeDN** des inaktiven Postfachs zu verwenden, die von dem Befehl im vorherigen Schritt zurückgegeben wurde. 
    
```
  $InPlaceHold.Sources.Remove("<LegacyExchangeDN of the inactive mailbox>")
```

    For example, the following command removes the inactive mailbox for Pilar Pinilla.
    
  ```
  $InPlaceHold.Sources.Remove("/o=contoso/ou=Exchange Administrative Group (FYDIBOHF23SPDLT)/cn=Recipients/cn=9c8dfff651ec4908950f5df60cbbda06-pilarp")
  ```

4. Stellen Sie sicher, dass das inaktive Postfach aus der Liste der Quellpostfächer in der Variable entfernt wird.
    
```
  $InPlaceHold.Sources
```

5. Ändern Sie den In-Situ-Speicher mit der aktualisierten Liste der Quellpostfächer, die das inaktive Postfach nicht enthält.
    
```
  Set-MailboxSearch $InPlaceHold.Name -SourceMailboxes $InPlaceHold.Sources
```

6. Stellen Sie sicher, dass das inaktive Postfach aus der Liste der Quellpostfächer für den In-Situ-Speicher entfernt wird.
    
```
  Get-MailboxSearch $InPlaceHold.Name | FL Sources
```

## <a name="more-information"></a>Weitere Informationen

- **Ein inaktives Postfach ist ein Typ des vorläufig gelöschten Postfachs.** In Exchange Online ist ein vorläufig gelöschtes Postfach, das zwar gelöscht wurde, aber innerhalb einer bestimmten Beibehaltungsdauer wiederhergestellt werden kann. Die Aufbewahrungsdauer für vorläufig gelöschte Postfächer beträgt in Exchange Online 30 Tage. Das bedeutet, dass das Postfach innerhalb von 30 Tagen nach dem vorläufigen Löschen wiederhergestellt werden kann. Nach 30 Tagen wird ein vorläufig gelöschtes Postfach zum dauerhaften Löschen markiert und kann nicht wiederhergestellt werden. 
    
- **Was geschieht, nachdem Sie den Haltebereich für ein inaktives Postfach entfernt haben?** Das Postfach wird wie andere vorläufig gelöschte Postfächer behandelt und wird für die dauerhafte Löschung markiert, nachdem die 30-tägige Beibehaltungsdauer für das vorläufig gelöschte Postfach abgelaufen ist. Dieser Aufbewahrungszeitraum beginnt an dem Datum, an dem das Postfach erstmals inaktiv gemacht wurde. Dieses Datum wird als Datum für das vorläufige Löschen bezeichnet und ist das Datum, an dem das entsprechende Office 365-Benutzerkonto oder an dem das Exchange Online-Postfach mit dem Cmdlet **Remove-Mailbox** gelöscht wurde. Das Datum für das vorläufige Löschen ist nicht das Datum, an dem Sie den Haltebereich entfernt haben. 
    
- **Wird ein inaktives Postfach sofort nach dem Entfernen des Haltebereichs dauerhaft gelöscht?** Wenn das Datum für vorläufig gelöschte Elemente für ein inaktives Postfach mehr als 30 Tage zurückliegt, wird das Postfach nicht sofort dauerhaft gelöscht, sobald Sie den Haltebereich entfernen. Das Postfach wird zum endgültigen Löschen markiert und bei der nächsten Verarbeitung gelöscht. 
    
- **Wie wirkt sich die Aufbewahrungszeit für vorläufig gelöschten Postfächer auf inaktiver Postfächer?** Wenn das vorläufig gelöschte Datum für eines inaktiven Postfachs mehr als 30 Tage vor dem Datum, die die Sperre entfernt wurde ist, wird das Postfach für endgültig gekennzeichnet. Aber wenn ein inaktives Postfachs ein vorläufig gelöschten Datum in den letzten 30 Tagen hat und Sie den Haltestatus entfernen, können Sie das Postfach wiederherstellen, nach oben, bis der vorläufig gelöschten Postfach Aufbewahrungszeitraum abgelaufen ist. Weitere Informationen hierzu finden Sie unter [Löschen oder Wiederherstellen von Benutzerpostfächern in Exchange Online](https://go.microsoft.com/fwlink/?linkid=856835). Nachdem der vorläufig gelöschten Postfach Aufbewahrungszeitraum abgelaufen ist, Sie haben führen Sie die Verfahren zum Wiederherstellen eines inaktiven Postfachs. Weitere Informationen hierzu finden Sie unter [Wiederherstellen ein inaktives Postfachs in Office 365](recover-an-inactive-mailbox.md).
    
- **Wie können Sie Anzeigen eines inaktiven Postfachs Informationen nach der Haltebereich entfernt wird?** Nach ein Haltebereich entfernt und inaktive Postfach wieder auf einem vorläufig gelöschten Postfach wiederhergestellt wird, wird es nicht zurückgegeben mithilfe des *InactiveMailboxOnly* -Parameters mit dem Cmdlet **Get-Mailbox** . Jedoch können Sie Informationen über das Postfach mit dem Befehl **Get-Mailbox-SoftDeletedMailbox** anzeigen. Zum Beispiel: 
    
```
  Get-Mailbox -SoftDeletedMailbox -Identity pilarp | FL Name,Identity,LitigationHoldEnabled,In
  Placeholds,WhenSoftDeleted,IsInactiveMailbox
  Name                   : pilarp
  Identity               : Soft Deleted Objects\pilarp
  LitigationHoldEnabled  : False
  InPlaceHolds           : {}
  WhenSoftDeleted        : 10/30/2014 1:19:04 AM
  IsInactiveMailbox      : False
```
  
Im Beispiel oben bezeichnet die *WhenSoftDeleted* -Eigenschaft das vorläufig gelöschte Datum, das in diesem Beispiel wird der 30 Oktober 2014. Wenn dieses vorläufig gelöschten Postfach eines inaktiven Postfachs für das die Sperre entfernt wurde zuvor, werden endgültig gelöschte 30 Tage nach dem Wert der Eigenschaft *WhenSoftDeleted* . In diesem Fall wird das Postfach nach 30 November 2014 dauerhaft gelöscht.

