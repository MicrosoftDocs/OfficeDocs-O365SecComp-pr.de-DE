---
title: Durchsuchen des Office 365 Überwachungsprotokolls zur Problembehandlung bei allgemeinen Szenarien
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
description: Sie können das Office 365 Überwachungsprotokoll-Such Tool verwenden, um Sie bei der Behandlung häufig auftretender Probleme zu unterstützen, beispielsweise beim Untersuchen eines kompromittierten Kontos oder beim ermitteln, wer die e-Mail-Weiterleitung für ein Postfach eingerichtet hat.
ms.openlocfilehash: e5c043668d73bdff30dfce962962a015a6748949
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155677"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a>Durchsuchen des Office 365 Überwachungsprotokolls zur Problembehandlung bei allgemeinen Szenarien

In diesem Artikel wird beschrieben, wie Sie mithilfe des Office 365 Überwachungsprotokoll-Such Tools häufige Support Szenarien beheben können. Dies umfasst die Verwendung des Überwachungsprotokolls für Folgendes:

- Suchen der IP-Adresse des Computers, der für den Zugriff auf ein kompromittiertes Konto verwendet wurde
- Bestimmen, wer die e-Mail-Weiterleitung für ein Postfach eingerichtet hat
- Ermitteln, ob ein Benutzer e-Mail-Elemente in seinem Postfach gelöscht hat
- Ermitteln, ob ein Benutzer eine Posteingangsregel erstellt hat

## <a name="using-the-office-365-audit-log-search-tool"></a>Verwenden des Office 365 Überwachungsprotokoll-Such Tools

Jedes der in diesem Artikel beschriebenen Problembehandlungsszenarien basiert auf der Verwendung des Überwachungsprotokoll-Such Tools im Office 365 Security and Compliance Center. In diesem Abschnitt werden die Berechtigungen aufgelistet, die zum Durchsuchen des Überwachungsprotokolls erforderlich sind, und es werden die Schritte zum Zugreifen auf und Ausführen von Überwachungsprotokoll suchen beschrieben. In jedem Szenario-Abschnitt finden Sie spezifische Hinweise dazu, wie Sie eine Überwachungsprotokoll-Suchabfrage konfigurieren und was Sie in den detaillierten Informationen in den Überwachungsdatensätzen suchen, die den Suchkriterien entsprechen.

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a>Erforderliche Berechtigungen für die Verwendung des Überwachungsprotokoll-Such Tools

Sie müssen in Exchange Online die Rolle "nur Ansichts Überwachungsprotokolle" oder "Überwachungsprotokolle" zugewiesen sein, um das Office 365 Überwachungsprotokoll durchsuchen zu können. Diese Rollen werden standardmäßig den Rollengruppen Compliance Management und Organisationsverwaltung auf der Seite **Berechtigungen** im Exchange Admin Center zugewiesen. Beachten Sie, dass globale Administratoren in Office 365 und Microsoft 365 automatisch als Mitglieder der Rollengruppe "Organisationsverwaltung" in Exchange Online hinzugefügt werden. Weitere Informationen finden Sie unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

### <a name="running-audit-log-searches"></a>Ausführung von Überwachungsprotokoll suchen

In diesem Abschnitt werden die Grundlagen für die Erstellung und Ausführung von Überwachungsprotokoll suchen beschrieben. Verwenden Sie diese Anweisungen als Ausgangspunkt für jedes Problembehandlungsszenario in diesem Artikel. Ausführlichere Schritt-für-Schritt-Anweisungen finden Sie unter durch [Suchen des Überwachungsprotokolls](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search).

1. Wechseln Sie [https://protection.office.com/unifiedauditlog](https://protection.office.com/unifiedauditlog) zu, und melden Sie sich mit ihrem geschäftlichen oder Schulkonto an.
    
    Die Seite **Überwachungsprotokoll Suche** wird angezeigt. 
    
    ![Konfigurieren Sie Kriterien, und klicken Sie dann auf suchen, um die Suche auszuführen.](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. Sie können die folgenden Suchkriterien konfigurieren. Beachten Sie, dass bei jedem Problembehandlungsszenario in diesem Artikel spezielle Anleitungen zum Konfigurieren dieser Felder empfohlen werden.
    
    a. **Aktivitäten** – klicken Sie auf die Dropdownliste, um die Aktivitäten anzuzeigen, nach denen Sie suchen können. Nachdem Sie die Suche ausgeführt haben, werden nur die Überwachungseinträge für die ausgewählten Aktivitäten angezeigt. Wenn Sie **Ergebnisse für alle Aktivitäten anzeigen** auswählen, werden die Ergebnisse für alle Aktivitäten angezeigt, die den anderen Suchkriterien entsprechen. Außerdem müssen Sie dieses Feld in einigen der Problembehandlungsszenarien leer lassen.
    
    b. **Start Datum** und **Enddatum** – wählen Sie einen Datums-und Zeitbereich aus, um die Ereignisse anzuzeigen, die innerhalb dieses Zeitraums aufgetreten sind. Die letzten sieben Tage sind standardmäßig ausgewählt. Das Datum und die Uhrzeit werden im UTC-Format (Coordinated Universal Time) angezeigt. Der maximale Datumsbereich, den Sie angeben können, ist 90 Tage.

    c. **Benutzer** – klicken Sie in dieses Feld, und wählen Sie einen oder mehrere Benutzer aus, für die Suchergebnisse angezeigt werden sollen. Überwachungsdatensätze für die ausgewählte Aktivität, die von den Benutzern ausgeführt werden, die Sie in diesem Feld ausgewählt haben, werden in der Ergebnisliste angezeigt. Lassen Sie dieses Feld leer, um Einträge für alle Benutzer (und Dienstkonten) in Ihrer Organisation zurückzugeben.
    
    d. **Datei, Ordner oder Website** – geben Sie einen oder alle Datei-oder Ordnernamen ein, um nach Aktivitäten im Zusammenhang mit der Datei des Ordners zu suchen, die das angegebene Schlüsselwort enthält. Sie können auch eine URL einer Datei oder eines Ordners angeben. Wenn Sie eine URL verwenden, müssen Sie sicherstellen, dass Sie den vollständigen URL-Pfad eingeben oder nur einen Teil der URL eingeben, wobei keine Sonderzeichen oder Leerzeichen enthalten sind. Lassen Sie dieses Feld leer, um Einträge für alle Dateien und Ordner in Ihrer Organisation zurückzugeben. Beachten Sie, dass dieses Feld in allen Problembehandlungsszenarien in diesem Artikel leer bleibt.
    
5. Klicken Sie auf **Suchen** , um die Suche mit Ihren Suchkriterien auszuführen. 
    
    Die Suchergebnisse werden geladen, und nach ein paar Momenten werden Sie unter **Ergebnisse** auf der Seite **Überwachungsprotokoll Suche** angezeigt. In den folgenden Abschnitten finden Sie Anleitungen zu den Themen, die für das spezifische Problembehandlungsszenario zu suchen sind.

    Weitere Informationen zum Anzeigen, Filtern oder Exportieren von Überwachungsprotokoll-Suchergebnissen finden Sie unter:

    - [Anzeigen von Suchergebnissen](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [Filtern von Suchergebnissen](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [Exportieren der Suchergebnisse](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="finding-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a>Ermitteln der IP-Adresse des Computers, der für den Zugriff auf ein kompromittiertes Konto verwendet wurde

Die IP-Adresse, die einer von einem beliebigen Benutzer ausgeführten Aktivität entspricht, ist in den meisten Überwachungsdatensätzen enthalten. Informationen zum verwendeten Client sind ebenfalls im Überwachungsprotokoll enthalten.

Hier erfahren Sie, wie Sie eine Überwachungsprotokoll-Suchabfrage für dieses Szenario konfigurieren:

**Aktivitäten** – falls relevant für Ihren Fall – wählen Sie eine bestimmte Aktivität aus, nach der gesucht werden soll. Für die Problembehandlung in kompromittierten Konten sollten **Sie die Option Benutzer bei Post** Fach **Aktivitäten unter Exchange-Postfachaktivitäten**Anmelden auswählen. Dadurch werden Überwachungsdatensätze zurückgegeben, die die IP-Adresse anzeigen, die bei der Anmeldung beim Postfach verwendet wurde. Lassen Sie andernfalls dieses Feld leer, um Überwachungseinträge für alle Aktivitäten zurückzugeben. 

> [!TIP]
> Wenn Sie dieses Feld leer lassen, werden **UserLoggedIn** -Aktivitäten zurückgegeben, bei denen es sich um eine Azure-Active Directory Aktivität handelt, die angibt, dass sich jemand bei einem Office 365-Benutzerkonto angemeldet hat. Verwenden Sie die Filterung in den Suchergebnissen, um die **UserLoggedIn** -Überwachungseinträge anzuzeigen.

**Start Datum** und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung gilt.

**Benutzer** – Wenn Sie ein kompromittiertes Konto untersuchen, wählen Sie den Benutzer aus, dessen Konto kompromittiert wurde. Dadurch werden Überwachungsdatensätze für Aktivitäten zurückgegeben, die von diesem Benutzerkonto ausgeführt werden.

**Datei, Ordner oder Website** – lassen Sie dieses Feld leer.

Nachdem Sie die Suche ausgeführt haben, wird die IP-Adresse für jede Aktivität in der Spalte **IP-Adresse** in den Suchergebnissen angezeigt. Klicken Sie auf den Datensatz in den Suchergebnissen, um ausführlichere Informationen auf der Flyout-Seite anzuzeigen.

## <a name="determining-who-set-up-email-forwarding-for-a-mailbox"></a>Bestimmen der Personen, die die e-Mail-Weiterleitung für ein Postfach einrichten

Wenn die e-Mail-Weiterleitung für ein Postfach konfiguriert ist, werden e-Mail-Nachrichten, die an das Postfach gesendet werden, an ein anderes Postfach weitergeleitet. Nachrichten können an Benutzer innerhalb oder außerhalb Ihrer Organisation weitergeleitet werden. Wenn die e-Mail-Weiterleitung für ein Postfach eingerichtet wurde, ist das zugrunde liegende Exchange Online Cmdlet, das verwendet wird, " **festgelegt-Postfach**".

Hier erfahren Sie, wie Sie eine Überwachungsprotokoll-Suchabfrage für dieses Szenario konfigurieren:

**Aktivitäten** : lassen Sie dieses Feld leer, damit die Suche Überwachungsdatensätze für alle Aktivitäten zurückgibt. Dies ist erforderlich, um alle Überwachungseinträge im Zusammenhang mit dem Cmdlet " **Satz-Postfach** " zurückzugeben.

**Start Datum** und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung gilt.

**Benutzer** – lassen Sie dieses Feld leer, wenn Sie ein e-Mail-Weiterleitungs Problem für einen bestimmten Benutzer nicht untersuchen. Auf diese Weise können Sie ermitteln, ob die e-Mail-Weiterleitung für einen beliebigen Benutzer eingerichtet wurde.

**Datei, Ordner oder Website** – lassen Sie dieses Feld leer.

Nachdem Sie die Suche ausgeführt haben, klicken Sie auf der Suchergebnisseite auf **Filter Ergebnisse** . Geben Sie in das Feld unter **Aktivitäts** Spaltenkopf die **Option Satz-Postfach** ein, sodass nur Überwachungseinträge im Zusammenhang mit dem CmdletSet **-Mailbox** angezeigt werden.

![Filtern der Ergebnisse einer Überwachungsprotokoll Suche](media/emailforwarding1.png)

An dieser Stelle müssen Sie sich die Details jedes Überwachungsdatensatzes ansehen, um zu ermitteln, ob die Aktivität mit der e-Mail-Weiterleitung zusammenhängt. Klicken Sie auf den Überwachungseintrag, um die **Detail** Flyout-Seite anzuzeigen, und klicken Sie dann auf **Weitere Informationen**. Im folgenden Screenshot und den Beschreibungen werden die Informationen hervorgehoben, die angibt, dass die e-Mail-Weiterleitung für das Postfach festgelegt wurde

![Ausführliche Informationen aus dem Überwachungsprotokoll](media/emailforwarding2.png)

a. Im Feld **objectID** wird der Alias des Postfachs, auf dem die e-Mail-Weiterleitung festgelegt wurde, angezeigt. Dieses Postfach wird auch in der Spalte **Element** auf der Suchergebnisseite angezeigt.

b. Im Feld **Parameter** gibt der Wert *ForwardingSmtpAddress* an, dass e-Mail-Nachrichten für das Postfach festgelegt wurden. In diesem Beispiel wird e-Mail an die e-Mail-Adresse Mike@contoso.com weitergeleitet, die sich außerhalb der alpinehouse.onmicrosoft.com-Organisation befindet.

c. Der Wert *true* für den Parameter *DeliverToMailboxAndForward* gibt an, dass eine Kopie der an Sarad@alpinehouse.onmicrosoft.com ** zugestellten Nachricht an die von der ForwardingSmtpAddress angegebene e-Mail-Adresse weitergeleitet wird. * *-Parameter, der in diesem Beispiel Mike@contoso.com ist. Wenn der Wert für den *DeliverToMailboxAndForward* -Parameter auf *false*festgelegt ist, wird e-Mail nur an die durch den *ForwardingSmtpAddress* -Parameter angegebene Adresse weitergeleitet. Sie wird nicht an das im Feld **objectID** angegebene Postfach übermittelt.

d. Das **UserID** -Feld gibt den Benutzer an, der die e-Mail-Weiterleitung für das im Feld **objectID** angegebene Postfach festgelegt hat. Dieser Benutzer wird auch in der Spalte **Benutzer** auf der Suchergebnisseite angezeigt. In diesem Fall scheint es, dass der Besitzer des Postfachs die e-Mail-Weiterleitung für Ihr Postfach festgelegt hat.

Wenn Sie feststellen, dass die e-Mail-Weiterleitung nicht für das Postfach festgelegt werden sollte, können Sie Sie entfernen, indem Sie den folgenden Befehl in Exchange Online PowerShell ausführen:

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

Weitere Informationen zu den Parametern im Zusammenhang mit der e-Mail-Weiterleitung finden Sie im Artikel " [Satz-Postfach](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) ".

## <a name="determining-if-a-user-deleted-email-items"></a>Ermitteln, ob ein Benutzer e-Mail-Elemente gelöscht hat

Ab Januar 2019 wird Microsoft die postfachüberwachungsprotokollierung standardmäßig für alle Office 365 und Microsoft-Organisationen aktivieren. Dies bedeutet, dass bestimmte von Postfachbesitzern ausgeführte Aktionen automatisch protokolliert werden und dass die entsprechenden Post Fach Überwachungseinträge verfügbar sind, wenn Sie im postfachüberwachungsprotokoll nach diesen suchen. Bevor die postfachüberwachung standardmäßig aktiviert wurde, muss Sie für jedes Benutzerpostfach in Ihrer Organisation manuell aktiviert werden. 

Die standardmäßig protokollierten Postfachaktionen umfassen die SoftDelete-und HardDelete-Postfachaktionen, die von Postfachbesitzern ausgeführt werden. Dies bedeutet, dass Sie mit den folgenden Schritten können Sie das Überwachungsprotokoll nach Ereignissen durchsuchen, die mit gelöschten e-Mail-Elementen in Zusammenhangstehen. Weitere Informationen zur postfachüberwachung standardmäßig finden Sie unter [Manage Mailbox Auditing](enable-mailbox-auditing.md).

Hier erfahren Sie, wie Sie eine Überwachungsprotokoll-Suchabfrage für dieses Szenario konfigurieren:

**Aktivitäten** – wählen Sie unter **Exchange-Postfachaktivitäten**eine oder beide der folgenden Aktionen aus:

- **Gelöschte Nachrichten aus dem Ordner "Gelöschte Elemente"** -diese Aktivität entspricht der **SoftDelete** -Post Fach Überwachungsaktion. Diese Aktivität wird auch protokolliert, wenn ein Benutzer ein Element dauerhaft löscht, indem es ihn auswählt und **UMSCHALT + ENTF**drückt. Nachdem ein Element endgültig gelöscht wurde, kann es vom Benutzer wiederhergestellt werden, bis der Aufbewahrungszeitraum für gelöschte Elemente abläuft.

- **Bereinigte Nachrichten aus dem Postfach** – diese Aktivität entspricht der **HardDelete** -Post Fach Überwachungsaktion. Dies wird protokolliert, wenn ein Benutzer ein Element aus dem Ordner "refundable Items" löscht. Administratoren können das Inhalts Such Tool im Security and Compliance Center verwenden, um bereinigte Elemente zu suchen und wiederherzustellen, bis der Aufbewahrungszeitraum für gelöschte Elemente abläuft oder länger ist, wenn das Postfach des Benutzers in der Warteschleife steht.

**Start Datum** und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung gilt.

**Benutzer** – Wenn Sie einen Benutzer in diesem Feld auswählen, gibt das Überwachungsprotokoll-Such Tool Überwachungsdatensätze für gelöschte e-Mail-Elemente zurück, die von dem von Ihnen angegebenen Benutzer (SoftDeleted oder HardDeleted) gelöscht wurden. In einigen Fällen ist der Benutzer, der eine e-Mail löscht, möglicherweise nicht der Postfachbesitzer.

**Datei, Ordner oder Website** – lassen Sie dieses Feld leer.

Nachdem Sie die Suche ausgeführt haben, können Sie die Suchergebnisse filtern, um die Überwachungsdatensätze für vorläufig gelöschte Elemente oder für hart gelöschte Elemente anzuzeigen. Klicken Sie auf den Überwachungseintrag, um die **Detail** Flyout-Seite anzuzeigen, und klicken Sie dann auf **Weitere Informationen**. Zusätzliche Informationen zu dem gelöschten Element, beispielsweise die Betreffzeile und den Speicherort des Elements, wenn es gelöscht wurde, werden im Feld **AffectedItems** angezeigt. Die folgenden Screenshots zeigen ein Beispiel für das **AffectedItems** -Feld aus einem vorläufig gelöschten Element und einem hart gelöschten Element.

**Beispiel für ein AffectedItems-Feld für vorläufig gelöschtes Element**

![Überwachungseintrag für vorläufig gelöschtes Element](media/softdeleteditem.png)

**Beispiel für ein AffectedItems-Feld für das hart gelöschte Element**

![Überwachungseintrag für das hart gelöschte e-Mail-Element](media/harddeleteditem.png)

### <a name="recovering-deleted-email-items"></a>Rückgewinnung gelöschter e-Mail-Elemente

Benutzer können vorläufig gelöschte Elemente wiederherstellen, wenn der Aufbewahrungszeitraum für gelöschte Elemente nicht abgelaufen ist. In Exchange Online ist der Aufbewahrungszeitraum für gelöschte Elemente standardmäßig 14 Tage, Administratoren können diese Einstellung jedoch auf maximal 30 Tage vergrössern. Zeigen Sie die Benutzer auf die [Wiederherstellung gelöschter Elemente oder e-Mails in Outlook](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) im Artikel, um Anweisungen zur Wiederherstellung gelöschter Elemente zu erhalten.

Wie bereits erläutert, können Administratoren möglicherweise gelöschte Elemente wiederherstellen, wenn der Aufbewahrungszeitraum für gelöschte Elemente nicht abgelaufen ist oder wenn das Postfach gesperrt ist, wobei die Elemente bis zum Ablauf der Haltedauer beibehalten werden. Wenn Sie eine Inhaltssuche ausführen, werden im Ordner "Wiederherstellbare Elemente" vorläufig gelöschte und hart gelöschte Elemente in den Suchergebnissen zurückgegeben, wenn Sie mit der Suchabfrage übereinstimmen. Weitere Informationen zum Durchführen von Inhalts suchen finden Sie unter [Inhaltssuche in Office 365](content-search.md).

> [!TIP]
> Um nach gelöschten e-Mail-Elementen zu suchen, suchen Sie nach der Betreffzeile, die im **AffectedItems** -Feld des Überwachungsdatensatzes angezeigt wird, oder in einem Teil der Betreffzeile.

## <a name="determining-if-a-user-created-an-inbox-rule"></a>Ermitteln, ob ein Benutzer eine Posteingangsregel erstellt hat

Wenn Benutzer eine Posteingangsregel für Ihr Exchange Online Postfach erstellen, wird ein entsprechender Überwachungseintrag im Überwachungsprotokoll gespeichert. Weitere Informationen zu Posteingangsregeln finden Sie unter:

- [Verwenden von Posteingangsregeln in Outlook im Internet](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [Verwalten von e-Mail-Nachrichten in Outlook mithilfe von Regeln](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

Hier erfahren Sie, wie Sie eine Überwachungsprotokoll-Suchabfrage für dieses Szenario konfigurieren:

**Aktivitäten** – wählen Sie unter **Exchange-Postfachaktivitäten**die Option **neue-InboxRule Create/Modify/Enable/Disable Posteingangsregel**aus.

**Start Datum** und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung gilt.

**Benutzer** – Wenn Sie einen bestimmten Benutzer nicht untersuchen, lassen Sie dieses Feld leer. Auf diese Weise können Sie neue Posteingangsregeln ermitteln, die von jedem Benutzer eingerichtet wurden.

**Datei, Ordner oder Website** – lassen Sie dieses Feld leer.

Nachdem Sie die Suche ausgeführt haben, werden alle Überwachungseinträge für diese Aktivität in den Suchergebnissen angezeigt. Klicken Sie auf einen Überwachungseintrag, um die **Detail** Flyout-Seite anzuzeigen, und klicken Sie dann auf **Weitere Informationen**. Im Feld **Parameter** werden Informationen zu den Einstellungen für Posteingangsregeln angezeigt. Im folgenden Screenshot und in den Beschreibungen werden die Informationen zu Posteingangsregeln hervorgehoben.

![Überwachungseintrag für neue Posteingangsregel](media/NewInboxRuleRecord.png)

a. Im Feld **objectID** wird der vollständige Name der Posteingangsregel angezeigt. Dieser Name enthält den Alias des Postfachs des Benutzers (beispielsweise "Sarad") und den Namen der Posteingangsregel (beispielsweise "Nachrichten von Administrator verschieben").

b. Im Feld **Parameter** wird die Bedingung der Posteingangsregel angezeigt. In diesem Beispiel wird die Bedingung durch den *from* -Parameter angegeben. Der für den Parameter *from* definierte Wert gibt an, dass die Posteingangsregel auf von admin@alpinehouse.onmicrosoft.com gesendeten e-Mails agiert. Eine vollständige Liste der Parameter, die zum Definieren von Bedingungen für Posteingangsregeln verwendet werden können, finden Sie im Artikel [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) .

c. Der Parameter *MoveToFolder* gibt die Aktion für die Posteingangsregel an. in diesem Beispiel werden Nachrichten, die von admin@alpinehouse.onmicrosoft.com empfangen werden, in den Ordner " *AdminSearch*" verschoben. Eine vollständige Liste der Parameter, die zum Definieren der Aktion einer Posteingangsregel verwendet werden können, finden Sie auch im Artikel [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) .

d. Das **UserID** -Feld gibt den Benutzer an, der die im Feld **objectID** angegebene Posteingangsregel erstellt hat. Dieser Benutzer wird auch in der Spalte **Benutzer** auf der Suchergebnisseite angezeigt.