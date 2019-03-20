---
title: Aktivieren des Beweissicherungsverfahrens für ein Postfach
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/18/2016
ms.audience: End User
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid: ''
ms.assetid: adee4621-3626-4aec-aa53-00b35ff0d0b0
description: 'Durch die Aktivierung des Beweissicherungsverfahrens für ein Postfach werden auch alle Postfachinhalte aufbewahrt, einschließlich gelöschter Elemente und Originalversionen geänderter Elemente. '
ms.openlocfilehash: a4d0939ffed32a8442b4b705bd15804b9f3eb7ea
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693124"
---
# <a name="place-a-mailbox-on-litigation-hold"></a>Aktivieren des Beweissicherungsverfahrens für ein Postfach
 
Durch die Aktivierung des Beweissicherungsverfahrens für ein Postfach werden auch alle Postfachinhalte aufbewahrt, einschließlich gelöschter Elemente und Originalversionen geänderter Elemente. Wenn Sie ein Benutzerpostfach für die Beweissicherung platzieren, werden Inhalte im Archivpostfach des Benutzers (falls aktiviert) ebenfalls in der Warteschleife platziert. Gelöschte und geänderte Elemente werden für einen bestimmten Zeitraum aufbewahrt, oder Sie entfernen das Postfach aus der Beweissicherung. Alle diese Postfachelemente werden bei einer [Compliance-eDiscovery](http://technet.microsoft.com/library/6377cb7a-3416-4e15-8571-c45d2160fc6f.aspx)-Suche zurückgegeben. 
  
> [!IMPORTANT]
> Das Beweissicherungsverfahren behält Elemente im Ordner „Wiederherstellbare Elemente" im Postfach des Benutzers bei. In Abhängigkeit der Anzahl und Größe der gelöschten oder geänderten Elemente steigt die Größe des Ordners „Wiederherstellbare Elemente" des Postfachs möglicherweise rasant. Der Ordner „Wiederherstellbare Elemente" wird standardmäßig mit einem hohen Kontingent konfiguriert. In Exchange Online wird dieses Kontingent automatisch erhöht, wenn Sie ein Postfach für ein Beweissicherungsverfahren festlegen. In Exchange Server 2013 wird empfohlen, die Postfächer zu überwachen, die in der wöchentlichen Aufbewahrungszeit gespeichert werden, um sicherzustellen, dass Sie nicht die Grenzen der Kontingente für wiederherstellbare Elemente erreichen. 
  
## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?
<a name="sectionSection0"> </a>

- Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten
    
- Es dauert bis zu 60 Minuten, bis die Einstellung für das Beweissicherungsverfahren in Kraft tritt.
    
- Bevor Sie diese Verfahren ausführen können, müssen Ihnen die entsprechenden Berechtigungen zugewiesen werden. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter „In-Situ-Archiv" im Thema [Berechtigungen für Messagingrichtlinien und -kompatibilität](http://technet.microsoft.com/library/ec4d3b9f-b85a-4cb9-95f5-6fc149c3899b.aspx). 
    
- Um ein Exchange Online-Postfach für die Aufbewahrung zu aktivieren, muss ihm eine Exchange Online-Lizenz (Plan 2) zugewiesen werden. Wenn einem Postfach eine Exchange Online-Lizenz (Tarif 1) zugewiesen ist, müssen Sie ihm eine separate Exchange Online-Archivierungslizenz zuweisen, um es anzuhalten.
    
- Wie bereits erläutert, wird der Inhalt im Archivpostfach des Benutzers auch dann in der Warteschleife platziert, wenn Sie für das Postfach eines Benutzers eine Beweissicherung platzieren. Wenn Sie für ein lokales primäres Postfach in einer Exchange-hybridbereitstellung eine Beweissicherung durchzuführen, wird das Cloud-basierte Archivpostfach (sofern aktiviert) ebenfalls in der Warteschleife platziert.
    
- In Exchange Online wird das Kontingent für den Ordner "Wiederherstellbare Elemente" automatisch auf 100 GB erhöht, wenn Sie für ein Postfach ein AufbewahrungsVerfahren festlegen. Die Standardgröße dieses Ordners beträgt 30 GB.
    
- Das Beweissicherungsverfahren behält gelöschte Elemente und die ursprünglichen Versionen der geänderten Elemente bei, bis die Aufbewahrung entfernt wird. Sie können optional eine Aufbewahrungsdauer angeben, in der ein Postfachelement für eine angegebene Zeitdauer beibehalten wird. Wenn Sie eine Aufbewahrungsdauer angeben, wird sie vom Datum an berechnet, an dem eine Nachricht empfangen oder ein Postfachelement erstellt wurde. Um Elemente beizubehalten, die ihren angegebenen Kriterien entsprechen, verwenden Sie einen in-situ-Speicher, um eine abfragebasierte Aufbewahrung zu erstellen. Weitere Informationen finden Sie unter [erstellen oder Entfernen eines in-situ-](http://technet.microsoft.com/library/9d5d8d37-a053-4830-9cb1-6e1ede25e963.aspx)Speichers.
    
- Um die Shell zum Speichern eines Exchange Online-Postfachs zu verwenden, müssen Sie Exchange Online PowerShell verwenden. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](http://technet.microsoft.com/library/c8bea338-6c1a-4bdf-8de0-7895d427ee5b.aspx).
    
- Es wird nicht unterstützt, ein Gerichtsverfahren für ein Postfach für Öffentliche Ordner zu aktivieren. Sie müssen einen in-situ-Speicher verwenden, um öffentliche Ordner zu speichern.
    
## <a name="use-the-eac-to-place-a-mailbox-on-litigation-hold"></a>Verwenden von EAC zum Aktivieren des Beweissicherungsverfahrens für ein Postfach
<a name="sectionSection1"> </a>

1. Navigieren Sie zu **Empfänger** \> **Postfächer**.
    
2. Klicken Sie in der Liste der Benutzerpostfächer auf das Postfach, das Sie für die Aufbewahrung von Rechtsstreitigkeiten aktivieren möchten **** ![, und klicken](media/ITPro-EAC-EditIcon.gif)Sie dann auf Bearbeitungssymbol bearbeiten.
    
3. Klicken Sie auf der Eigenschaftenseite des Postfachs auf **Postfachfunktionen.**
    
4. Klicken Sie unter **Beweissicherungsverfahren: Deaktiviert** auf **Aktivieren**, um für das Postfach das Beweissicherungsverfahren zu aktivieren. 
    
5. Geben Sie auf der Seite **Beweissicherungsverfahren** die folgenden optionalen Informationen ein: 
    
  - **Dauer des Beweissicherungsverfahrens (Tage)** Verwenden Sie dieses Feld zum Angeben, wie lange Postfachelemente aufbewahrt werden, wenn für das Postfach das Beweissicherungsverfahren aktiviert wird. Der Zeitraum beginnt mit dem Datum, an dem das Postfachelement empfangen oder erstellt wurde. Wenn Sie dieses Feld leer lassen, werden Elemente unbegrenzt aufbewahrt oder bis die Aufbewahrung entfernt wird. Geben Sie die Dauer in Tagen an. 
    
  - **Hinweis** Verwenden Sie dieses Feld, um Benutzer darüber zu informieren, dass für ihr Postfach das Beweissicherungsverfahren aktiv ist. Die Notiz wird im Postfach des Benutzers angezeigt, wenn Sie Outlook 2010 oder höher verwenden. 
    
  - **URL** Verwenden Sie dieses Feld, um den Benutzer an eine Website weiterzuleiten, auf der er weitere Informationen über das Beweissicherungsverfahren erhält. Diese URL wird im Postfach des Benutzers angezeigt, wenn Sie Outlook 2010 oder höher verwenden. 
    
6. Klicken Sie auf **Speichern** auf der Seite **Beweissicherungsverfahren**, und klicken Sie dann auf der Postfacheigenschaftsseite auf **Speichern**. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-indefinitely"></a>Verwenden der Shell, um ein Postfach auf unbestimmte Zeit zu halten
<a name="sectionSection2"> </a>

In diesem Beispiel wird das Beweissicherungsverfahren für das Postfach "bsuneja@contoso.com" aktiviert. Elemente im Postfach werden unbegrenzt aufbewahrt oder bis die Aufbewahrung entfernt wird.
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true
```

> [!NOTE]
> Wenn Sie für ein Postfach das unbegrenzte Beweissicherungsverfahren aktivieren (indem Sie keine Dauer angeben), wird der Wert für die  _LitigationHoldDuration_-Eigenschaft des Postfachs auf  `Unlimited` festgelegt. 
  
## <a name="use-the-shell-to-place-a-mailbox-on-litigation-hold-and-preserve-items-for-a-specified-duration"></a>Verwenden der Shell zum Platzieren eines Postfachs für die Aufbewahrung und Aufbewahrung von Elementen für eine bestimmte Dauer
<a name="sectionSection3"> </a>

In diesem Beispiel wird das Beweissicherungsverfahren für das Postfach "mailbox bsuneja@contoso.com" aktiviert, und Elemente werden für 2.555 Tage (etwa 7 Jahre) beibehalten. 
  
```
Set-Mailbox bsuneja@contoso.com -LitigationHoldEnabled $true -LitigationHoldDuration 2555
```

## <a name="use-the-shell-to-place-all-mailboxes-on-litigation-hold-for-a-specified-duration"></a>Verwenden der Shell zum Speichern aller Postfächer für eine bestimmte Dauer
<a name="sectionSection4"> </a>

Ihre Organisation erfordert möglicherweise, dass alle Postfachdaten für einen bestimmten Zeitraum aufbewahrt werden. Berücksichtigen Sie Folgendes, bevor Sie alle Postfächer in einer Organisation in einem Unternehmen platzieren:
  
In diesem Beispiel werden alle Benutzerpostfächer in der Organisation für ein Jahr (365 Tage) als Beweissicherung platziert.
  
```
Get-Mailbox -ResultSize Unlimited -Filter {RecipientTypeDetails -eq "UserMailbox"} | Set-Mailbox -LitigationHoldEnabled $true -LitigationHoldDuration 365
```

Im Beispiel wird das Cmdlet [Get-Mailbox](http://technet.microsoft.com/library/8a5a6eb9-4a75-47f9-ae3b-a3ba251cf9a8.aspx) verwendet, um alle Postfächer in der Organisation abzurufen, gibt einen Empfängerfilter an, der alle Benutzerpostfächer enthält, und leitet dann die Liste der Postfächer an das Cmdlet [Set-Mailbox](http://technet.microsoft.com/library/a0d413b9-d949-4df6-ba96-ac0906dedae2.aspx) um, um die Beweissicherung zu aktivieren und Dauer halten. 
  
Führen Sie den vorherigen Befehl ohne den Parameter  _LitigationHoldDuration_ aus, um alle Benutzerpostfächer unbegrenzt aufzubewahren. 
  
Im Abschnitt [Weitere Informationen](#moreinfo.md) finden Sie Beispiele für die Verwendung von anderen Empfängereigenschaften in einem Filter zum Einbeziehen oder Ausschließen von mindestens einem Postfach. 
  
## <a name="use-the-shell-to-remove-a-mailbox-from-litigation-hold"></a>Verwenden der Shell zum Entfernen eines Postfachs
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
    
2. Klicken Sie in der Liste der Benutzerpostfächer auf das Postfach, für das Sie die Einstellungen für die Beweis Aufbewahrung überprüfen **** ![möchten, und](media/ITPro-EAC-EditIcon.gif)klicken Sie dann auf Bearbeitungssymbol bearbeiten.
    
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
    
  - Die Aktivierung des Beweissicherungsverfahrens für alle Postfächer kann sich erheblich auf die Postfachgrößen auswirken. Planen Sie in einer Exchange Server 2013-Organisation eine adäquate Speicherung, um die Aufbewahrungsanforderungen Ihrer Organisation zu erfüllen.
    
  - Für den Ordner „Wiederherstellbare Elemente" gilt eine eigene Speicherbegrenzung, sodass Elemente in diesem Ordner nicht zur Speicherbegrenzung des Postfachs zählen. Wie bereits erläutert, nimmt die Datenmenge im Postfach und Archiv eines Benutzers im Ordner „Wiederherstellbare Elemente" zu, wenn Sie Postfachdaten über einen langen Zeitraum aufbewahren. Um diese Zunahme in Exchange Online zu bewältigen, wird das Kontingent für den Ordner "Wiederherstellbare Elemente" automatisch von 30 GB auf 100 GB erhöht, wenn Sie ein Postfach für ein Verfahren halten. 
    
    In Exchange Server 2013 beträgt der Standardspeichergrenzwert für den Ordner "Wiederherstellbare Elemente" auch 30 GB. Wir empfehlen, die Größe des Ordners regelmäßig zu überprüfen, um sicherzustellen, dass die Grenze nicht erreicht wird. Weitere Informationen finden Sie unter [Ordner "Wiederherstellbare Elemente"](http://technet.microsoft.com/library/efc48fb4-2ed8-4d05-93af-f3505fbc389d.aspx).
    
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
    

