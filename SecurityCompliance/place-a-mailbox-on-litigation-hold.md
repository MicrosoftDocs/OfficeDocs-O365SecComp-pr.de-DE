---
title: Aktivieren des Beweissicherungsverfahrens für ein Postfach
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Durch die Aktivierung des Beweissicherungsverfahrens für ein Postfach werden auch alle Postfachinhalte aufbewahrt, einschließlich gelöschter Elemente und Originalversionen geänderter Elemente. '
ms.openlocfilehash: 00f83d69d90f10659427986ffcb16f9e5358c054
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038038"
---
# <a name="place-a-mailbox-on-litigation-hold"></a>Aktivieren des Beweissicherungsverfahrens für ein Postfach
 
Durch die Aktivierung des Beweissicherungsverfahrens für ein Postfach werden auch alle Postfachinhalte aufbewahrt, einschließlich gelöschter Elemente und Originalversionen geänderter Elemente. Wenn Sie für das Postfach eines Benutzers das Beweissicherungsverfahren aktivieren, wird auch der Inhalt im Archivpostfach archiviert, wenn dieses aktiviert ist. Gelöschte und geänderte Elemente werden eine bestimmte Zeit lang aufbewahrt oder bis Sie das Beweissicherungsverfahren für das Postfach deaktivieren. Alle diese Postfachelemente werden bei einer [In-Place eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx)-Suche zurückgegeben. 
  
> [!IMPORTANT]
> Aufbewahrung für eventuelle Rechtsstreitigkeiten behält Elemente im Ordner "wiederherstellbare Elemente" im Postfach des Benutzers. Je nach Anzahl und Größe der Elemente gelöscht oder geändert erhöhen Sie die Größe des Ordners "wiederherstellbare Elemente" des Postfachs schnell. Ordner "wiederherstellbare Elemente" ist standardmäßig mit einer hohen Vorgabe konfiguriert. In Exchange Online wird dieses Kontingent automatisch erhöht, wenn Sie ein Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten platzieren. Server 2013 in Exchange wird empfohlen, dass Sie Postfächer überwachen, die in die Aufbewahrung für eventuelle Rechtsstreitigkeiten wöchentlich, stellen Sie sicher, dass sie die Grenzwerte für die Kontingente wiederherstellbare Elemente erreicht nicht platziert werden. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

- Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
    
- Es dauert bis zu 60 Minuten, bis die Einstellung für das Beweissicherungsverfahren in Kraft tritt.
    
- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter „In-Situ-Archiv" im Thema [Berechtigungen für Messagingrichtlinien und -kompatibilität](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx). 
    
- Um ein Exchange Online-Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten zu platzieren, müssen sie eine Lizenz Exchange Online (Plan 2) zugewiesen werden. Wenn ein Postfach mit eine Exchange Online (Plan 1)-Lizenz zugewiesen ist, müssten Sie weisen Sie ihr eine separate Lizenz der Exchange Online-Archivierung auf platziert halten.
    
- Wenn Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten für ein Benutzerpostfach einleiten, wird wie bereits erklärt auch Inhalt im Archivpostfach des Benutzers in der Warteschleife platziert. Wenn Sie eine Aufbewahrung für eventuelle Rechtsstreitigkeiten für eine lokale primären Postfach in einer Exchange-hybridbereitstellung setzen, wird das Cloud-basierten Archivpostfach (sofern aktiviert) auch in der Warteschleife platziert.
    
- In Exchange Online wird das Kontingent für "wiederherstellbare Elemente" auf 100 GB automatisch erhöht, wenn Sie ein Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten platzieren. Die Standardgröße dieses Ordners ist 30 GB.
    
- Aufbewahrung für eventuelle Rechtsstreitigkeiten behält gelöschte Elemente und behält auch ursprüngliche Versionen geänderter Objekte, bis die Sperre entfernt wurde. Sie können optional eine Dauer halten angeben, die ein Postfach-Element für die angegebene Dauer Periode behält. Wenn Sie einen Haltestatus Dauer angeben, wird ab dem Datum berechnet eine Nachricht empfangen oder ein Postfach-Element erstellt wird. Verwenden Sie Elemente, die den angegebenen Kriterien übereinstimmen, eine In-Place Hold zum Erstellen eines Haltestatus abfragebasierter. Weitere Informationen hierzu finden Sie unter [Erstellen oder Entfernen einer In-Place Hold](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx).
    
- Wenn Sie die Shell verwenden um ein Exchange Online-Postfachs in die Warteschleife zu stellen, müssen Sie Exchange Online PowerShell verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).
    
- Das Festlegen eines Beweissicherungsverfahrens für ein Postfach für öffentliche Ordner wird nicht unterstützt. Sie müssen einen In-Situ-Speicher verwenden, um eine Speicherung für öffentliche Ordner festzulegen.
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a>Verwenden von EAC zum Aktivieren des Beweissicherungsverfahrens für ein Postfach
<a name="sectionSection1"> </a>

1. Navigieren Sie zu **Empfänger** \> **Postfächer**.
    
2. In der Liste der Benutzerpostfächer, klicken Sie auf das Postfach, das Sie für die Aufbewahrung für eventuelle Rechtsstreitigkeiten platzieren möchten, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/ITPro-EAC-EditIcon.gif).
    
3. Klicken Sie auf der Eigenschaftenseite des Postfachs auf **Postfachfunktionen.**
    
4. Klicken Sie unter **Beweissicherungsverfahren: Deaktiviert** auf **Aktivieren**, um für das Postfach das Beweissicherungsverfahren zu aktivieren. 
    
5. Geben Sie auf der Seite **Beweissicherungsverfahren** die folgenden optionalen Informationen ein: 
    
  - **Dauer des Beweissicherungsverfahrens (Tage)** Verwenden Sie dieses Feld zum Angeben, wie lange Postfachelemente aufbewahrt werden, wenn für das Postfach das Beweissicherungsverfahren aktiviert wird. Der Zeitraum beginnt mit dem Datum, an dem das Postfachelement empfangen oder erstellt wurde. Wenn Sie dieses Feld leer lassen, werden Elemente unbegrenzt aufbewahrt oder bis die Aufbewahrung entfernt wird. Geben Sie die Dauer in Tagen an. 
    
  - **Hinweis** Können Sie in diesem Feld um den Benutzer zu informieren, die, den Ihr Postfach auf Aufbewahrung für eventuelle Rechtsstreitigkeiten ist. Die Notiz wird im Postfach des Benutzers angezeigt, wenn sie Outlook 2010 oder höher verwenden. 
    
  - **URL** Verwenden Sie dieses Feld, um den Benutzer zu einer Website Weitere Informationen zur Aufbewahrung für eventuelle Rechtsstreitigkeiten zu leiten. Diese URL wird im Postfach des Benutzers angezeigt, wenn sie Outlook 2010 oder höher verwenden. 
    
6. Klicken Sie auf **Speichern** auf der Seite **Beweissicherungsverfahren**, und klicken Sie dann auf der Postfacheigenschaftsseite auf **Speichern**. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a>Verwenden der Shell zum Aktivieren des unbegrenzten Beweissicherungsverfahrens für ein Postfach
<a name="sectionSection2"> </a>

In diesem Beispiel wird das Beweissicherungsverfahren für das Postfach "bsuneja@contoso.com" aktiviert. Elemente im Postfach werden unbegrenzt aufbewahrt oder bis die Aufbewahrung entfernt wird.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> Wenn Sie für ein Postfach das unbegrenzte Beweissicherungsverfahren aktivieren (indem Sie keine Dauer angeben), wird der Wert für die  _LitigationHoldDuration_-Eigenschaft des Postfachs auf  `Unlimited` festgelegt. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a>Verwenden der Shell zum Aktivieren eines Postfachs für das Beweissicherungsverfahren und Beibehalten von Elementen für eine bestimmte Dauer
<a name="sectionSection3"> </a>

In diesem Beispiel wird das Beweissicherungsverfahren für das Postfach "mailbox bsuneja@contoso.com" aktiviert, und Elemente werden für 2.555 Tage (etwa 7 Jahre) beibehalten. 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a>Verwenden der Shell zum Aktivieren des Beweissicherungsverfahrens für alle Postfächer für eine bestimmte Dauer
<a name="sectionSection4"> </a>

In Ihrer Organisation ist es möglicherweise erforderlich, dass alle Postfachdaten für einen bestimmten Zeitraum beibehalten werden. Bedenken Sie Folgendes, bevor Sie für alle Postfächer in einer Organisation das Beweissicherungsverfahren aktivieren:
  
In diesem Beispiel wird für alle Benutzerpostfächer in der Organisation für ein Jahr (365 Tage) das Beweissicherungsverfahren aktiviert.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

Im Beispiel wird das Cmdlet [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) verwendet, um alle Postfächer in der Organisation abzurufen. Es wird ein Empfängerfilter angegeben, um alle Benutzerpostfächer einzubeziehen. Anschließend wird die Liste der Postfächer an das [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx)-Cmdlet umgeleitet, um das Beweissicherungsverfahren und die Aufbewahrungsdauer zu aktivieren. 
  
Führen Sie den vorherigen Befehl ohne den Parameter  _LitigationHoldDuration_ aus, um alle Benutzerpostfächer unbegrenzt aufzubewahren. 
  
Im Abschnitt [Weitere Informationen](#moreinfo.md) finden Sie Beispiele für die Verwendung von anderen Empfängereigenschaften in einem Filter zum Einbeziehen oder Ausschließen von mindestens einem Postfach. 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a>Verwenden der Shell zum Aufheben des Beweissicherungsverfahrens für ein Postfach
<a name="sectionSection5"> </a>

In diesem Beispiel wird das Beweissicherungsverfahren für das Postfach "bsuneja@contoso.com" aufgehoben.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $false
```

P
## <a name="how-do-you-know-this-worked"></a>Woher wissen Sie, dass dieses Verfahren erfolgreich war?
<a name="sectionSection6"> </a>

Führen Sie eine der folgenden Aktionen aus, um sicherzustellen, dass Sie das Beweissicherungsverfahren für ein Postfach erfolgreich aktiviert haben:
  
- In der Exchange-Verwaltungskonsole:
    
1. Navigieren Sie zu **Empfänger** \> **Postfächer**.
    
2. In der Liste der Benutzerpostfächer, klicken Sie auf das Postfach, das Sie Einstellungen für die Aufbewahrung für eventuelle Rechtsstreitigkeiten überprüfen möchten, und klicken Sie dann auf **Bearbeiten** ![Bearbeitungssymbol](media/ITPro-EAC-EditIcon.gif).
    
3. Klicken Sie auf der Eigenschaftenseite des Postfachs auf **Postfachfunktionen.**
    
4. Stellen Sie unter **Beweissicherungsverfahren** sicher, dass die Aufbewahrung aktiviert ist.
    
5. Klicken Sie auf **Details anzeigen**, um zu prüfen, wann und durch wen das Beweissicherungsverfahren für das Postfach aktiviert wurde. Sie können die Werte in den optionalen Feldern **Dauer des Beweissicherungsverfahrens (Tage)**, **Hinweis** und **URL** auch prüfen oder ändern. 
    
- Führen Sie in der Shell einen der folgenden Befehle aus:
    
  ```
  Get-Mailbox <name of mailbox> | FL LitigationHold*
  ```

    oder
    
  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | FL Name,LitigationHold*
  ```

    Wenn das unbegrenzte Beweissicherungsverfahren für ein Postfach aktiviert ist, ist der Wert für die Eigenschaft  _LitigationHoldDuration_ des Postfachs auf  `Unlimited` festgelegt.
    
## <a name="more-information"></a>Weitere Informationen
<a name="moreinfo"> </a>

- Wenn Ihre Organisation verlangt, dass alle Postfachdaten für einen bestimmten Zeitraum beibehalten werden müssen, ziehen Sie Folgendes in Betracht, bevor Sie das Beweissicherungsverfahren für alle Postfächer in einer Organisation aktivieren.
    
  - Wenn Sie den vorherigen Befehl verwenden, um eine Aufbewahrung für alle Postfächer in einer Organisation (oder eine Teilmenge an Postfächern, die mit einem angegebenen Empfängerfilter übereinstimmen) zu aktivieren, wird die Aufbewahrung nur für die Postfächer aktiviert, die zum Zeitpunkt der Befehlsausführung vorhanden sind. Wenn Sie später neue Postfächer erstellen, müssen Sie den Befehl erneut ausführen, um die neuen Postfächer aufzubewahren. Wenn Sie oft neue Postfächer erstellen, können Sie den Befehl als geplante Aufgabe so oft wie erforderlich ausführen.
    
  - Platzieren aller Postfächer auf Aufbewahrung für eventuelle Rechtsstreitigkeiten kann Postfachgrößen erheblich beeinträchtigen. Planen Sie in einer Exchange Server 2013-Organisation genügend Speicher verwendet, um die Beibehaltung der Anforderungen Ihrer Organisation zu erfüllen.
    
  - Ordner "wiederherstellbare Elemente" hat einen eigenen Speichergrenzwert damit Elemente im Ordner nicht zu den Speichergrenzwert Postfach zählen. Wie bereits erklärt Postfachdaten für einen längeren Zeitraum beibehalten Wachstum des Ordners wiederherstellbare Elemente im Postfach des Benutzers gelöscht und archivieren. Um für die höhere Beanspruchung in Exchange Online zu unterstützen, wird das Kontingent für "wiederherstellbare Elemente" automatisch Erhöhung von 30 GB auf 100 GB beim Platzieren eines Postfachs auf Aufbewahrung für eventuelle Rechtsstreitigkeiten. 
    
    In Exchange ist Server 2013, standardmäßig den maximalen Speicherplatz für den Ordner "wiederherstellbare Elemente" auch 30 GB. Es wird empfohlen, dass Sie die Größe dieses Ordners, um sicherzustellen, dass den Grenzwert erreicht werden nicht in regelmäßigen Abständen überwachen. Weitere Informationen finden Sie unter [Recoverable Items Folder](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).
    
- Der vorherige Befehl zum Platzieren aller Postfächer im Archiv verwendet einen Empfängerfilter, der alle Benutzerpostfächer zurückgibt. Sie können andere Empfängereigenschaften zum Zurückgeben einer Liste von bestimmten Postfächern verwenden, die Sie an das Cmdlet **Set-Mailbox** umleiten können, um für diese Postfächer ein Beweissicherungsverfahren zu aktivieren. 
    
    Hier sind einige Beispiele dafür, wie mit den Cmdlets **Get-Mailbox** und **Get-Recipient** eine Teilmenge an Postfächern basierend auf allgemeinen Benutzer- oder Postfacheigenschaften zurückgegeben wird. In diesen Beispielen wird davon ausgegangen, dass entsprechende Postfacheigenschaften (wie  _CustomAttributeN_ oder  _Department_) aufgefüllt wurden.
    
  ```
  Get-Mailbox -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'CustomAttribute15 -eq "OneYearLitigationHold"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'Department -eq "HR"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'PostalCode -eq "98052"'
  ```

  ```
  Get-Recipient -RecipientTypeDetails UserMailbox -ResultSize unlimited -Filter 'StateOrProvince -eq "WA"'
  ```

  ```
  Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -ne "DiscoveryMailbox"}
  ```

    Sie können andere Benutzerpostfacheigenschaften in einem Filter verwenden, um Postfächer einzubeziehen bzw. auszuschließen. Weitere Informationen finden Sie unter [Filterable Properties for the -Filter Parameter](http://technet.microsoft.com/library/b02b0005-2fb6-4bc2-8815-305259fa5432.aspx).
    

