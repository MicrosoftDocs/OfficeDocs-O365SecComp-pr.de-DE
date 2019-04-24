---
title: Durchsuchen des Office 365-Überwachungsprotokolls zur Behandlung allgemeiner Szenarien
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
- MET150
- MOE150
description: Sie können das Office 365-Überwachungsprotokoll-Such Tool verwenden, um häufige Probleme wie die Untersuchung eines kompromittierten Kontos zu beheben oder herauszufinden, wer die e-Mail-Weiterleitung für ein Postfach eingerichtet hat.
ms.openlocfilehash: bd0483f2b2e209dc0cbd2b03eda928fd8d44d7b0
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32250257"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a>Durchsuchen des Office 365-Überwachungsprotokolls zur Behandlung allgemeiner Szenarien

In diesem Artikel wird beschrieben, wie Sie das Office 365-Überwachungsprotokoll-Such Tool verwenden, um häufige Support Szenarien zu behandeln. Hierzu gehört die Verwendung des Überwachungsprotokolls für Folgendes:

- Ermitteln der IP-Adresse des Computers, der für den Zugriff auf ein kompromittiertes Konto verwendet wird
- Festlegen der e-Mail-Weiterleitung für ein Postfach
- Bestimmen, ob ein Benutzer e-Mail-Elemente in seinem Postfach gelöscht hat
- Bestimmen, ob ein Benutzer eine Posteingangsregel erstellt hat

## <a name="using-the-office-365-audit-log-search-tool"></a>Verwenden des Office 365-Überwachungsprotokoll-Such Tools

Alle in diesem Artikel beschriebenen Problembehandlungsszenarien basieren auf der Verwendung des Überwachungsprotokoll-Such Tools im Office 365 Security and Compliance Center. In diesem Abschnitt werden die Berechtigungen aufgelistet, die zum Durchsuchen des Überwachungsprotokolls erforderlich sind, und die Schritte zum Zugreifen auf und Ausführen von Überwachungsprotokoll suchen. Jeder szenariobereich enthält spezifische Anleitungen zum Konfigurieren einer Suchabfrage für das Überwachungsprotokoll und zu den zu suchenden Details in den Überwachungsdatensätzen, die den Suchkriterien entsprechen.

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a>Erforderliche Berechtigungen für die Verwendung des Überwachungsprotokoll-Such Tools

Sie müssen in Exchange Online über die Rolle "Überwachungsprotokolle" oder "Überwachungsprotokolle" verfügen, um das Office 365-Überwachungsprotokoll durchsuchen zu können. Diese Rollen werden standardmäßig den Rollengruppen "Compliance-Verwaltung" und "Organisationsverwaltung" auf der Seite " **Berechtigungen** " im Exchange Admin Center zugewiesen. Beachten Sie, dass globale Administratoren in Office 365 und Microsoft 365 automatisch als Mitglieder der Rollengruppe "Organisationsverwaltung" in Exchange Online hinzugefügt werden. Weitere Informationen finden Sie unter [Verwalten von Rollengruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

### <a name="running-audit-log-searches"></a>Durchführen von Überwachungsprotokoll suchen

In diesem Abschnitt werden die Grundlagen zum Erstellen und Durchführen von Überwachungsprotokoll suchen beschrieben. Verwenden Sie diese Anweisungen als Ausgangspunkt für jedes Problembehandlungsszenario in diesem Artikel. Ausführlichere schrittweise Anleitungen finden Sie unter durch [Suchen des Überwachungsprotokolls](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search).

1. Wechseln Sie [https://protection.office.com/unifiedauditlog](https://protection.office.com/unifiedauditlog) zu, und melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an.
    
    Die Seite **Überwachungsprotokoll Suche** wird angezeigt. 
    
    ![Konfigurieren Sie Kriterien, und klicken Sie dann auf suchen, um die Suche auszuführen](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. Sie können die folgenden Suchkriterien konfigurieren. Beachten Sie, dass für jedes Problembehandlungsszenario in diesem Artikel spezifische Anleitungen zum Konfigurieren dieser Felder empfohlen werden.
    
    a. **Aktivitäten** -klicken Sie auf die Dropdownliste, um die Aktivitäten anzuzeigen, nach denen Sie suchen können. Nachdem Sie die Suche ausgeführt haben, werden nur die Überwachungsdatensätze für die ausgewählten Aktivitäten angezeigt. Wenn Sie **Ergebnisse für alle Aktivitäten anzeigen** auswählen, werden Ergebnisse für alle Aktivitäten angezeigt, die den anderen Suchkriterien entsprechen. Außerdem müssen Sie dieses Feld in einigen der Problembehandlungsszenarien leer lassen.
    
    b. **Start** -und **Enddatum** – wählen Sie einen Datums-und Uhrzeitbereich aus, um die Ereignisse anzuzeigen, die innerhalb dieses Zeitraums aufgetreten sind. Die letzten sieben Tage sind standardmäßig ausgewählt. Datum und Uhrzeit werden im UTC-Format (Coordinated Universal Time) angezeigt. Der maximale Zeitraum, den Sie angeben können, beträgt 90 Tage.

    c. **Benutzer** – klicken Sie in dieses Feld, und wählen Sie dann einen oder mehrere Benutzer aus, für die Suchergebnisse angezeigt werden sollen. Überwachungsdatensätze für die ausgewählte Aktivität, die von den Benutzern, die Sie in diesem Feld ausgewählt haben, ausgeführt werden, werden in der Ergebnisliste angezeigt. Lassen Sie dieses Feld leer, um Einträge für alle Benutzer (und Dienstkonten) in Ihrer Organisation zurückzugeben.
    
    d. **Datei, Ordner oder Website** -geben Sie einen oder alle Datei-oder Ordnernamen ein, um nach Aktivitäten im Zusammenhang mit der Ordner Datei zu suchen, die das angegebene Schlüsselwort enthält. Sie können auch eine URL einer Datei oder eines Ordners angeben. Wenn Sie eine URL verwenden, stellen Sie sicher, dass Sie den vollständigen URL-Pfad eingeben, oder geben Sie nur einen Teil der URL ein, und schließen Sie keine Sonderzeichen oder Leerzeichen ein. Lassen Sie dieses Feld leer, um Einträge für alle Dateien und Ordner in Ihrer Organisation zurückzugeben. Beachten Sie, dass dieses Feld in allen Problembehandlungsszenarien in diesem Artikel leer gelassen wird.
    
5. Klicken Sie auf **Suchen** , um die Suche mit Ihren Suchkriterien auszuführen. 
    
    Die Suchergebnisse werden geladen, und nach ein paar Augenblicken werden Sie unter **Ergebnisse** auf der Such Seite des **Überwachungsprotokolls** angezeigt. In den folgenden Abschnitten finden Sie Anleitungen zur Suche nach dem spezifischen Problembehandlungsszenario.

    Weitere Informationen zum Anzeigen, Filtern oder Exportieren von Überwachungsprotokoll-Suchergebnissen finden Sie unter:

    - [Suchergebnisse anzeigen](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [Suchergebnisse filtern](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [Exportieren der Suchergebnisse](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="finding-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a>Ermitteln der IP-Adresse des Computers, der für den Zugriff auf ein kompromittiertes Konto verwendet wird

Die IP-Adresse, die einer von einem beliebigen Benutzer ausgeführten Aktivität entspricht, ist in den meisten Überwachungsaufzeichnungen enthalten. Informationen zum verwendeten Client sind auch im Überwachungsdatensatz enthalten.

Hier erfahren Sie, wie Sie eine Überwachungsprotokoll-Suchabfrage für dieses Szenario konfigurieren:

**Aktivitäten** -wenn relevant für Ihren Fall, wählen Sie eine bestimmte Aktivität für die Suche aus. Bei der Problembehandlung für kompromittierte Konten empfiehlt es sich, den **Benutzer,** der bei der Post Fach Aktivität angemeldet ist, unter **Exchange-Postfachaktivitäten**auszuwählen. Dadurch werden Überwachungsdatensätze zurückgegeben, die die bei der Anmeldung am Postfach verwendete IP-Adresse enthalten. Andernfalls lassen Sie dieses Feld leer, um Überwachungsdatensätze für alle Aktivitäten zurückzugeben. 

> [!TIP]
> Wenn Sie dieses Feld leer lassen, werden **UserLoggedIn** -Aktivitäten zurückgegeben, bei denen es sich um eine Azure Active Directory-Aktivität handelt, die angibt, dass sich jemand bei einem Office 365-Benutzerkonto angemeldet hat. Verwenden Sie die Filterung in den Suchergebnissen, um die **UserLoggedIn** -Überwachungsdatensätze anzuzeigen.

**Start** -und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung gilt.

**Benutzer** – Wenn Sie ein kompromittiertes Konto untersuchen, wählen Sie den Benutzer aus, dessen Konto kompromittiert wurde. Dadurch werden Überwachungsdatensätze für Aktivitäten zurückgegeben, die von diesem Benutzerkonto ausgeführt werden.

**Datei, Ordner oder Website** – lassen Sie dieses Feld leer.

Nachdem Sie die Suche ausgeführt haben, wird die IP-Adresse für jede Aktivität in der Spalte **IP-Adresse** in den Suchergebnissen angezeigt. Klicken Sie in den Suchergebnissen auf den Datensatz, um detailliertere Informationen auf der Flyout-Seite anzuzeigen.

## <a name="determining-who-set-up-email-forwarding-for-a-mailbox"></a>Bestimmen, wer die e-Mail-Weiterleitung für ein Postfach eingerichtet hat

Wenn die e-Mail-Weiterleitung für ein Postfach konfiguriert ist, werden e-Mail-Nachrichten, die an das Postfach gesendet werden, an ein anderes Postfach weitergeleitet. Nachrichten können an Benutzer innerhalb oder außerhalb Ihrer Organisation weitergeleitet werden. Wenn die e-Mail-Weiterleitung für ein Postfach eingerichtet ist, wird das zugrunde liegende Exchange Online-Cmdlet **Set-Mailbox**verwendet.

Hier erfahren Sie, wie Sie eine Überwachungsprotokoll-Suchabfrage für dieses Szenario konfigurieren:

**Aktivitäten** – lassen Sie dieses Feld leer, damit die Suche Überwachungsdatensätze für alle Aktivitäten zurückgibt. Dies ist erforderlich, um alle Überwachungsdatensätze zurückzugeben, die sich auf das Cmdlet **Set-Mailbox** beziehen.

**Start** -und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung gilt.

**Benutzer** – Wenn Sie ein Problem bei der e-Mail-Weiterleitung für einen bestimmten Benutzer nicht untersuchen, lassen Sie dieses Feld leer. Dadurch können Sie ermitteln, ob die e-Mail-Weiterleitung für einen beliebigen Benutzer eingerichtet wurde.

**Datei, Ordner oder Website** – lassen Sie dieses Feld leer.

Nachdem Sie die Suche ausgeführt haben, klicken Sie auf der Suchergebnisseite auf **Ergebnisse filtern** . Geben Sie im Feld unter **Aktivitäts** Spaltenüberschrift **Set-Mailbox** ein, sodass nur Überwachungsdatensätze angezeigt werden, die sich auf das Cmdlet **Set-Mailbox** beziehen.

![Filtern der Ergebnisse einer Überwachungsprotokoll Suche](media/emailforwarding1.png)

An dieser Stelle müssen Sie sich die Details der einzelnen Überwachungsdatensätze ansehen, um festzustellen, ob die Aktivität mit der e-Mail-Weiterleitung verbunden ist. Klicken Sie auf den Überwachungsdatensatz, um die **Detail** Flyout-Seite anzuzeigen, und klicken Sie dann auf **Weitere Informationen**. Im folgenden Screenshot werden die Informationen hervorgehoben, die angeben, dass die e-Mail-Weiterleitung für das Postfach festgelegt wurde.

![Detaillierte Informationen aus dem Überwachungsdatensatz](media/emailforwarding2.png)

a. Im Feld **objectID** wird der Alias des Postfachs, für das die e-Mail-Weiterleitung aktiviert wurde, angezeigt. Dieses Postfach wird auch in der Spalte **Element** auf der Suchergebnisseite angezeigt.

b. Im Feld **Parameter** gibt der Wert *ForwardingSmtpAddress* an, dass für das Postfach eine e-Mail-Weiterleitung festgelegt wurde. In diesem Beispiel wird die e-Mail an die e-Mail-Adresse mike@contoso.com weitergeleitet, die sich außerhalb der alpinehouse.onmicrosoft.com-Organisation befindet.

c. Der *true* -Wert für den *DeliverToMailboxAndForward* -Parameter gibt an, dass eine kopie der Nachricht an Sarad@alpinehouse.onmicrosoft.com übermittelt *und* an die e-Mail-Adresse weitergeleitet wird, die von der *ForwardingSmtpAddress *der Parameter, der in diesem Beispiel Mike@contoso.com ist. Wenn der Wert für den *DeliverToMailboxAndForward* -Parameter auf *false*festgelegt ist, wird e-Mail nur an die durch den *ForwardingSmtpAddress* -Parameter angegebene Adresse weitergeleitet. Sie wird nicht an das Postfach zugestellt, das im **objectID** -Feld angegeben ist.

d. Das Feld **UserID** gibt den Benutzer an, der die e-Mail-Weiterleitung für das im Feld **objectID** -Feld angegebene Postfach festgelegt hat. Dieser Benutzer wird auch in der Spalte **Benutzer** auf der Suchergebnisseite angezeigt. In diesem Fall scheint es, dass der Besitzer des Postfachs e-Mail-Weiterleitung für Ihr Postfach festgelegt hat.

Wenn Sie feststellen, dass die e-Mail-Weiterleitung nicht für das Postfach festgelegt werden soll, können Sie Sie entfernen, indem Sie den folgenden Befehl in Exchange Online PowerShell ausführen:

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

Weitere Informationen zu den Parametern für die e-Mail-Weiterleitung finden Sie im Artikel [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) .

## <a name="determining-if-a-user-deleted-email-items"></a>Ermitteln, ob ein Benutzer e-Mail-Elemente gelöscht hat

Ab Januar 2019 aktiviert Microsoft die postfachüberwachungsprotokollierung standardmäßig für alle Office 365 und Microsoft-Organisationen. Dies führt dazu, dass bestimmte Aktionen, die von Postfachbesitzern ausgeführt werden, automatisch protokolliert werden, und die entsprechenden Post Fach Überwachungseinträge stehen zur Verfügung, wenn Sie im postfachüberwachungsprotokoll nach diesen suchen. Bevor die postfachüberwachung standardmäßig aktiviert wurde, muss Sie für jedes Benutzerpostfach in Ihrer Organisation manuell aktiviert werden. 

Die standardmäßig protokollierten Postfachaktionen schließen die Postfachaktionen SoftDelete und HardDelete ein, die von Postfachbesitzern ausgeführt werden. Dies führt dazu, dass Sie die folgenden Schritte ausführen können, um das Überwachungsprotokoll nach Ereignissen im Zusammenhang mit gelöschten e-Mail-Elementen zu durchsuchen. Weitere Informationen zur postfachüberwachung in der Standardeinstellung finden Sie unter [Verwalten der postfachüberwachung](enable-mailbox-auditing.md).

Hier erfahren Sie, wie Sie eine Überwachungsprotokoll-Suchabfrage für dieses Szenario konfigurieren:

**Aktivitäten** – wählen Sie unter **Exchange-Postfachaktivitäten**eine oder beide der folgenden Aktivitäten aus:

- **Gelöschte Nachrichten aus Ordner "Gelöschte Elemente"** – diese Aktivität entspricht der **SoftDelete** -Post Fach Überwachungsaktion. Diese Aktivität wird auch protokolliert, wenn ein Benutzer ein Element dauerhaft löscht, indem er es auswählt und **UMSCHALT + ENTF**drückt. Nachdem ein Element dauerhaft gelöscht wurde, kann der Benutzer es wiederherstellen, bis der Aufbewahrungszeitraum für gelöschte Elemente abgelaufen ist.

- **Gelöschte Nachrichten aus dem Postfach** : diese Aktivität entspricht der **HardDelete** -Post Fach Überwachungsaktion. Diese wird protokolliert, wenn ein Benutzer ein Element aus dem Ordner "Wiederherstellbare Elemente" löscht. Administratoren können das Inhaltssuche-Tool im Security and Compliance Center verwenden, um gelöschte Elemente zu suchen und wiederherzustellen, bis der Aufbewahrungszeitraum des gelöschten Elements abgelaufen ist oder länger ist, wenn das Postfach des Benutzers in der Warteschleife steht.

**Start** -und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung gilt.

**Benutzer** : Wenn Sie einen Benutzer in diesem Feld auswählen, gibt das Such Tool des Überwachungsprotokolls Überwachungsdatensätze für e-Mail-Elemente zurück, die vom angegebenen Benutzer (SoftDeleted oder HardDeleted) gelöscht wurden. In einigen Fällen ist der Benutzer, der eine e-Mail löscht, möglicherweise nicht der Postfachbesitzer.

**Datei, Ordner oder Website** – lassen Sie dieses Feld leer.

Nachdem Sie die Suche ausgeführt haben, können Sie die Suchergebnisse filtern, um die Überwachungseinträge für Elemente mit weichen Elementen oder für fest gelöschte Elemente anzuzeigen. Klicken Sie auf den Überwachungsdatensatz, um die **Detail** Flyout-Seite anzuzeigen, und klicken Sie dann auf **Weitere Informationen**. Zusätzliche Informationen zum gelöschten Element, wie beispielsweise der Betreffzeile und dem Speicherort des Elements, wenn es gelöscht wurde, werden im Feld **AffectedItems** angezeigt. Die folgenden Screenshots zeigen ein Beispiel für das **AffectedItems** -Feld aus einem Element mit weichen Elementen und einem fest gelöschten Element.

**Beispiel für AffectedItems-Feld für Soft-Deleted Item**

![Überwachungsdatensatz für Soft-Deleted Item](media/softdeleteditem.png)

**Beispiel für das AffectedItems-Feld für das fest gelöschte Element**

![Überwachungsdatensatz für e-Mail-Element mit fester Löschung](media/harddeleteditem.png)

### <a name="recovering-deleted-email-items"></a>Wiederherstellen gelöschter e-Mail-Elemente

Wenn der Aufbewahrungszeitraum für gelöschte Elemente nicht abgelaufen ist, können Benutzer Soft-gelöschte Elemente wiederherstellen. In Exchange Online ist der Aufbewahrungszeitraum für gelöschte Elemente standardmäßig 14 Tage, Administratoren können diese Einstellung jedoch auf maximal 30 Tage verlängern. Verweisen Sie die Benutzer auf die [Wiederherstellung gelöschter Elemente oder e-Mails in Outlook im Web](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) -Artikel, um Anweisungen zur Wiederherstellung gelöschter Elemente zu erhalten.

Wie bereits erläutert, können Administratoren möglicherweise fest gelöschte Elemente wiederherstellen, wenn der Aufbewahrungszeitraum für gelöschte Elemente nicht abgelaufen ist oder wenn das Postfach in der Warteschleife ist, in diesem Fall werden die Elemente beibehalten, bis die Haltedauer abgelaufen ist. Wenn Sie eine Inhaltssuche ausführen, werden die Elemente im Ordner "Wiederherstellbare Elemente" in den Suchergebnissen zurückgegeben, wenn Sie mit der Suchabfrage übereinstimmen. Weitere Informationen zum Durchführen von Inhalts suchen finden Sie unter [Inhaltssuche in Office 365](content-search.md).

> [!TIP]
> Um nach gelöschten e-Mail-Elementen zu suchen, suchen Sie den gesamten oder einen Teil der Betreffzeile, die im Überwachungsdatensatz im Feld **AffectedItems** angezeigt wird.

## <a name="determining-if-a-user-created-an-inbox-rule"></a>Bestimmen, ob ein Benutzer eine Posteingangsregel erstellt hat

Wenn Benutzer eine Posteingangsregel für Ihr Exchange Online-Postfach erstellen, wird ein entsprechender Überwachungsdatensatz im Überwachungsprotokoll gespeichert. Weitere Informationen zu Posteingangsregeln finden Sie unter:

- [Verwenden von Posteingangsregeln in Outlook im Web](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [Verwalten von e-Mail-Nachrichten in Outlook mithilfe von Regeln](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

Hier erfahren Sie, wie Sie eine Überwachungsprotokoll-Suchabfrage für dieses Szenario konfigurieren:

**Aktivitäten** – wählen Sie unter **Exchange-Postfachaktivitäten**die Option **New-InboxRule Create/Modify/Enable/Disable Posteingang Rule**aus.

**Start** -und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung gilt.

**Benutzer** – Wenn Sie einen bestimmten Benutzer nicht untersuchen, lassen Sie dieses Feld leer. Dadurch können Sie neue Posteingangsregeln identifizieren, die von jedem Benutzer eingerichtet wurden.

**Datei, Ordner oder Website** – lassen Sie dieses Feld leer.

Nachdem Sie die Suche ausgeführt haben, werden alle Überwachungsdatensätze für diese Aktivität in den Suchergebnissen angezeigt. Klicken Sie auf einen Überwachungsdatensatz, um die **Detail** Flyout-Seite anzuzeigen, und klicken Sie dann auf **Weitere Informationen**. Informationen zu den Einstellungen der Posteingangsregel werden im Feld **Parameter** angezeigt. Im folgenden Screenshot werden die Informationen zu Posteingangsregeln hervorgehoben.

![Überwachungsdatensatz für neue Posteingangsregel](media/NewInboxRuleRecord.png)

a. Im Feld **objectID** wird der vollständige Name der Posteingangsregel angezeigt. Dieser Name enthält den Alias des Postfachs des Benutzers (beispielsweise Sarad) und den Namen der Posteingangsregel (beispielsweise "Nachrichten vom Administrator verschieben").

b. Im Feld **Parameter** wird die Bedingung der Posteingangsregel angezeigt. In diesem Beispiel wird die Bedingung durch den *from* -Parameter angegeben. Der für den *from* -Parameter definierte Wert gibt an, dass die Posteingangsregel auf e-Mails reagiert, die von admin@alpinehouse.onmicrosoft.com gesendet werden. Eine vollständige Liste der Parameter, die zum Definieren von Bedingungen für Posteingangsregeln verwendet werden können, finden Sie im Artikel [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) .

c. Der Parameter *MoveToFolder* gibt die Aktion für die Posteingangsregel an. in diesem Beispiel werden Nachrichten aus admin@alpinehouse.onmicrosoft.com in den Ordner mit dem Namen *AdminSearch*verschoben. Im Artikel [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) finden Sie eine vollständige Liste der Parameter, die zum Definieren der Aktion einer Posteingangsregel verwendet werden können.

d. Das Feld **UserID** gibt den Benutzer an, der die im **objectID** -Feld angegebene Posteingangsregel erstellt hat. Dieser Benutzer wird auch in der Spalte **Benutzer** auf der Suchergebnisseite angezeigt.