---
title: Suchen der Office 365-Überwachungsprotokoll für die Problembehandlung bei gängigen Szenarien
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
description: Office 365 Audit Log Such-Tool können zum Beheben häufig auftretender Probleme wie Untersuchen von einem kompromittierten Konto oder herausfinden, die e-Mail-Weiterleitung für ein Postfach einrichten.
ms.openlocfilehash: 930e311712e49214ca2a51e256c29e5f959deab8
ms.sourcegitcommit: c34f1a0d560117153fc9a7b8da8994bc6fc53791
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2018
ms.locfileid: "27123898"
---
# <a name="search-the-office-365-audit-log-to-troubleshoot-common-scenarios"></a>Suchen der Office 365-Überwachungsprotokoll für die Problembehandlung bei gängigen Szenarien

Dieser Artikel beschreibt, wie Sie mit der Suchfunktion von Office 365 Audit Log Standardszenarien Unterstützung bei der Problembehandlung unterstützen. Dazu gehört das Überwachungsprotokoll zu verwenden:

- Hier finden Sie die IP-Adresse des Computers verwendet, um einem kompromittierten Konto zugreifen
- Bestimmen Sie, die e-Mail-Weiterleitung für ein Postfach einrichten
- Bestimmen Sie, ob ein Benutzer e-Mail-Elemente in ihrem Postfach gelöscht.
- Bestimmen Sie, ob ein Benutzer eine Posteingangsregel erstellt.

## <a name="using-the-office-365-audit-log-search-tool"></a>Verwenden der Suchfunktion von Office 365 Audit log

Jedes der zur Problembehandlung in diesem Artikel beschriebenen Szenarien basieren auf mit Audit Log Such-Tool im Compliance Center & Sicherheit in Office 365. Dieser Abschnitt enthält die erforderlichen Berechtigungen für das Überwachungsprotokoll durchsuchen und beschreibt die Schritte zum zugreifen und überwachungsprotokollsuchvorgänge ausführen. Jeder Abschnitt Szenario enthält bestimmte Anleitungen zu und Konfigurieren eines Audit Log Suchabfrage und wie die detaillierte Informationen in das Überwachungsprotokoll Datensätze suchen, die den Suchkriterien entsprechen.

### <a name="permissions-required-to-use-the-audit-log-search-tool"></a>Erforderliche Berechtigungen zum Verwenden der Suchfunktion von Audit log

Sie müssen die Rolle des Kontaktobjekts überwachen Protokolle oder Protokolle überwachen im Exchange Online um das Office 365-Überwachungsprotokoll durchsuchen zugewiesen werden. Standardmäßig werden die Verwaltung der Richtlinientreue und Organization Management Rollengruppen auf der Seite **Berechtigungen** in der Exchange-Verwaltungskonsole dieser Rollen zugewiesen. Weitere Informationen finden Sie unter [Manage Role Gruppen in Exchange Online](https://go.microsoft.com/fwlink/p/?LinkID=730688).

### <a name="running-audit-log-searches"></a>Ausgeführte überwachungsprotokollsuchvorgänge

In diesem Abschnitt werden die Grundlagen zum Erstellen und Ausführen von überwachungsprotokollsuchvorgänge beschrieben. Verwenden Sie diese Anweisungen als Ausgangspunkt für jedes Szenario für die Problembehandlung in diesem Artikel. Weitere detaillierte schrittweise Anleitung finden Sie unter [Suchen der Überwachungsprotokolle melden Sie sich bei der Office 365-Sicherheit und Compliance Center ](search-the-audit-log-in-security-and-compliance.md#step-1-run-an-audit-log-search).

1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
  
2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.

3. Klicken Sie im linken Bereich der Sicherheit und Compliance Center auf **Suche & Untersuchung** > **Audit Log suchen**.
    
    **Audit Log** Suchseite wird angezeigt. 
    
    ![Konfigurieren von Kriterien, und klicken Sie auf Suchen, die zum Ausführen der Suche](media/8639d09c-2843-44e4-8b4b-9f45974ff7f1.png)
  
4. Sie können die folgenden Suchkriterien konfigurieren. Beachten Sie, dass bestimmte Anleitungen zum Konfigurieren dieser Felder wird jedes Szenario für die Problembehandlung in diesem Artikel empfohlen wird.
    
    a. **Aktivitäten** - klicken Sie auf die Dropdown-Liste die Aktivitäten angezeigt werden sollen, denen Sie für suchen können. Nachdem die Suche ausgeführt wurde, werden nur die Audit-Datensätze für die ausgewählten Aktivitäten angezeigt. Auswählen der **Ergebnisse für alle Aktivitäten anzeigen** zeigt Ergebnisse für alle Aktivitäten, die die anderen Suchkriterien erfüllen. Sie müssen auch das Feld in einigen Szenarien zur Problembehandlung leer lassen.
    
    b. **Startdatum** und **Enddatum** - wählen Sie einen Bereich für Datum und Uhrzeit der Ereignisse angezeigt, die innerhalb dieses Zeitraums aufgetreten sind. Die letzten sieben Tagen sind standardmäßig aktiviert. Datum und Uhrzeit werden in koordinierter Weltzeit (UTC) Format angezeigt. Der maximale Zeitraum, den Sie angeben können, ist 90 Tage.

    c. **Benutzer** : Klicken Sie in dieses Feld ein und wählen Sie einen oder mehrere Benutzer, um die Suche angezeigt werden Ergebnisse für die. Audit-Einträge für die ausgewählten Aktivitäten, die von den Benutzern, die Sie in dieses Feld auswählen, werden in der Liste der Ergebnisse angezeigt. Lassen Sie dieses Feld leer, Zurückgeben von Einträgen für alle Benutzer (und Dienstkonten) in Ihrer Organisation.
    
    d. **Dateien, Ordner, oder Website** – Geben Sie einige oder alle ein File- oder Folder Name für die Suche nach Aktivitäten im Zusammenhang mit der Datei des Ordners, der das angegebene Schlüsselwort enthält. Sie können auch eine URL einer Datei oder eines Ordners angeben. Enthalten Sie Wenn Sie eine URL verwenden, sicherzustellen, dass der Typ der vollständige URL-Pfad sein oder wenn Sie nur einen Teil der URL eingeben nicht keine Sonderzeichen oder Leerzeichen. Lassen Sie dieses Feld leer, Zurückgeben von Einträgen für alle Dateien und Ordner in Ihrer Organisation. Beachten Sie, dass dieses Feld in der Problembehandlungsszenarien in diesem Artikel leer ist.
    
5. Klicken Sie auf **Suche** zum Ausführen der Suche mit den Suchkriterien. 
    
    Die Suchergebnisse werden geladen, und werden sie nach einigen Augenblicken unter **Ergebnisse** angezeigt, auf der Seite **Audit Log** . Jede in den folgenden Abschnitten wird Anleitungen zur Aspekte, die für das spezifische Szenario zur Problembehandlung bieten.

    Weitere Informationen anzeigen, filtern oder Audit Log Suchergebnisse exportieren finden Sie unter:

    - [Anzeigen der Suchergebnisse](search-the-audit-log-in-security-and-compliance.md#step-2-view-the-search-results)
    - [Suchergebnisse filtern](search-the-audit-log-in-security-and-compliance.md#step-3-filter-the-search-results)
    - [Exportieren der Suchergebnisse](search-the-audit-log-in-security-and-compliance.md#step-4-export-the-search-results-to-a-file)

## <a name="finding-the-ip-address-of-the-computer-used-to-access-a-compromised-account"></a>Suchen die IP-Adresse des Computers verwendet, um einem kompromittierten Konto zugreifen

Die IP-Adresse für eine Aktivität von jedem Benutzer ist in den meisten Überwachungseinträge enthalten. Informationen über den Client verwendet, ist auch im Audit Datensatz enthalten.

Hier ist ein Audit Log Suchabfrage für dieses Szenario zu konfigurieren:

**Aktivitäten** - Fall wählen Sie eine bestimmte Aktivität zu suchen. Zur Problembehandlung betroffenen Konten erwägen Sie auswählen die **Benutzer angemeldet Postfach** -Aktivität unter dem **Exchange-Postfach-Aktivitäten**. Überwachung Datensätze, die die IP-Adresse, die verwendet wurde, bei der Anmeldung an das Postfach anzeigen, wird zurückgegeben. Andernfalls lassen Sie dieses Feld leer, um die Überwachungseinträge für alle Aktivitäten zurückzugeben. 

> [!TIP]
> Dieses Feld leer lassen wird **UserLoggedIn** Aktivitäten, zurückgegeben, die ist eine Azure Active Directory-Aktivität, die angibt, dass eine Person zu einem Office 365-Benutzerkonto angemeldet hat. Verwenden Sie in den Suchergebnissen filtern, um die Überwachungseinträge **UserLoggedIn** anzuzeigen.

**Startdatum** und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung anwendbar ist.

**Benutzer** : Wenn Sie einem kompromittierten Konto untersuchen sind, wählen Sie den Benutzer, dessen Konto wurde gefährdet. Dadurch wird die Überwachungseinträge für Aktivitäten von mit dem Benutzerkonto zurückgegeben.

**Dateien, Ordner, oder Site** – lassen Sie dieses Feld leer.

Nachdem Sie die Suche ausführen wird die IP-Adresse für jede Aktivität in der Spalte **IP-Adresse** in den Suchergebnissen angezeigt. Klicken Sie auf den Datensatz in den Suchergebnissen auf Ausführlichere Informationen auf der Seite flyoutmenü anzeigen.

## <a name="determining-who-set-up-email-forwarding-for-a-mailbox"></a>Bestimmen, die e-Mail-Weiterleitung für ein Postfach einrichten

Wenn e-Mail-Weiterleitung für ein Postfach konfiguriert ist, werden e-Mail-Nachrichten, die an das Postfach gesendet werden an ein anderes Postfach weitergeleitet. Nachrichten können an Benutzer innerhalb und außerhalb Ihrer Organisation weitergeleitet werden. Wenn e-Mail-Weiterleitung für ein Postfach festgelegt wird, ist das zugrunde liegende Exchange Online-Cmdlet, das verwendet wird, **Set-Mailbox**.

Hier ist ein Audit Log Suchabfrage für dieses Szenario zu konfigurieren:

**Aktivitäten** - lassen Sie dieses Feld leer, damit die Suche Überwachungseinträge für alle Aktivitäten zurückgibt. Dies ist erforderlich, um eine zurückgeben audit-Datensätze im Zusammenhang mit dem Cmdlet **Set-Mailbox** .

**Startdatum** und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung anwendbar ist.

**Benutzer** :, wenn Sie eine e-Mail-Weiterleitung Problem für einen bestimmten Benutzer untersuchen sind, lassen Sie dieses Feld leer. Dadurch können Sie erkennen, ob e-Mail-Weiterleitung für jeden Benutzer eingerichtet wurde.

**Dateien, Ordner, oder Site** – lassen Sie dieses Feld leer.

Klicken Sie nach dem Ausführen die Suche auf der Suchergebnisseite auf **Ergebnisse filtern** . Geben Sie im Feld unter **Aktivität** Spaltenüberschrift **Set-Mailbox** , sodass nur im Zusammenhang mit dem Cmdlet **Set-Mailbox** Audit Datensätze angezeigt werden.

![Filtern der Ergebnisse einer Audit Log-Suche](media/emailforwarding1.png)

Zu diesem Zeitpunkt müssen Sie die Details der einzelnen Audit Datensätze zu ermitteln, ob die Aktivität e-Mail-Weiterleitung zusammenhängt. Klicken Sie auf die Audit-Datensatzes, um die Seite **Details** flyoutmenü anzuzeigen, und klicken Sie dann auf **Weitere Informationen**. Der folgende Screenshot und Beschreibungen Highlights, die die Informationen, die e-Mail-Weiterleitung gibt an, für das Postfach festgelegt wurde.

![Ausführliche Informationen aus dem Audit-Datensatz](media/emailforwarding2.png)

a. Klicken Sie in das Feld **ObjectId** der Alias des Postfachs an, die e-Mail-Weiterleitung festgelegt wurde auf wird angezeigt. Dieses Postfach wird auch in der Spalte **Element** auf der Suchergebnisseite angezeigt.

b in das Feld **Parameter** gibt den Wert *ForwardingSmtpAddress* auf, ob e-Mail weiterleiten für das Postfach festgelegt wurde. In diesem Beispiel wird e-Mail an die e-Mail-Adresse mike@contoso.com weitergeleitet wird, die außerhalb der Organisation alpinehouse.onmicrosoft.com werden.

c. der Wert *True* für den Parameter *DeliverToMailboxAndForward* gibt an, dass eine Kopie der Nachricht an sarad@alpinehouse.onmicrosoft.com *und* übermittelt, die durch die *ForwardingSmtpAddress angegebenen e-Mail-Adresse weitergeleitet wird *-Parameter, der in diesem Beispiel wird der mike@contoso.com. Wenn der Wert für den Parameter *DeliverToMailboxAndForward* auf *False*festgelegt ist, wird e-Mail nur an die durch den Parameter *ForwardingSmtpAddress* angegebene Adresse weitergeleitet. Es wird nicht im Feld **ObjectId** angegebenen Postfach übermittelt.

d. das **UserId** -Feld gibt an, der Benutzer, der e-Mail-Weiterleitung für das Postfach in das Feld **ObjectId** angegebenen festgelegt. Dieser Benutzer ist auch in der Spalte **Benutzer** auf der Suchergebnisseite angezeigt. In diesem Fall scheint es, dass der Besitzer des Postfachs e-Mail-Weiterleitung für ihr Postfach festgelegt.

Wenn Sie feststellen, dass e-Mail-Weiterleitung sollte nicht für das Postfach festgelegt werden, können Sie ihn mithilfe des folgenden Befehls in Exchange Online PowerShell entfernen:

```
Set-Mailbox <mailbox alias> -ForwardingSmtpAddress $null 
```

Finden Sie unter [Set-Mailbox](https://docs.microsoft.com/powershell/module/exchange/mailboxes/set-mailbox) Artikel für Weitere Informationen zu den Parametern im Zusammenhang mit e-Mail-Weiterleitung.

## <a name="determining-if-a-user-deleted-email-items"></a>Feststellen, ob ein Benutzer e-Mail-Elemente gelöscht.

Vor dem Löschen Überwachungsprotokolldatensätze zu e-Mail-Elemente in das Überwachungsprotokoll Office 365 gespeichert sind, Überwachung von Postfächern muss für jedes Benutzerpostfach in Ihrer Organisation aktiviert sein. Darüber hinaus müssen die SoftDelete und HardDelete Postfach Aktionen für die Überwachung aktiviert werden. Anweisungen finden Sie unter [Überwachung in Office 365 Postfach zu aktivieren](enable-mailbox-auditing.md). Wenn die Überwachung von Postfächern für Benutzer bereits aktiviert ist, gehen Sie folgendermaßen vor, um das Überwachungsprotokoll für Ereignisse im Zusammenhang mit der gelöschten e-Mail-Elemente durchsuchen.

Hier ist ein Audit Log Suchabfrage für dieses Szenario zu konfigurieren:

**Aktivitäten** - unter dem **Exchange-Postfach Aktivitäten**, wählen Sie eine oder beide der folgenden Aktivitäten:

- **Gelöschte Nachrichten aus dem Ordner Gelöschte Elemente** – diese Aktivität entspricht der **SoftDelete** postfachüberwachung-Aktion. Diese Aktivität wird auch protokolliert, wenn ein Benutzer ein Element dauerhaft löscht, indem Sie es markieren, und drücken **UMSCHALT + ENTF**. Nachdem ein Element dauerhaft gelöscht wird, kann der Benutzer wiederhergestellt werden, bis die Aufbewahrungszeit für gelöschte läuft ab.

- **Gelöschte Nachrichten aus dem Postfach von** – diese Aktivität entspricht der **HardDelete** postfachüberwachung-Aktion. Dies wird protokolliert, wenn ein Benutzer ein Element aus dem Ordner wiederherstellbare Elemente löscht. Administratoren können das Tool Inhaltssuche im Compliance Center & Sicherheit in Office 365 um zu suchenden und Recover gelöscht Elemente, bis die Aufbewahrungszeit für gelöschte läuft ab oder länger, wenn das Postfach des Benutzers ist gesperrt.

**Startdatum** und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung anwendbar ist.

**Benutzer** : Wenn Sie einen Benutzer in diesem Feld auswählen, gibt Audit Log Such-Tool Überwachungseinträge für e-Mail-Elemente zurück, die vom Benutzer die von die Ihnen angegebenen gelöschten (SoftDeleted oder HardDeleted) waren. In einigen Fällen möglicherweise der Benutzer, der eine e-Mail-Nachricht löscht den Besitzer des Postfachs nicht.

**Dateien, Ordner, oder Site** – lassen Sie dieses Feld leer.

Nachdem die Suche ausgeführt wurde, können Sie um Audit Datensätze für vorläufig gelöschten Elemente oder Festplatte gelöschte Elemente anzuzeigen, die Suchergebnisse filtern. Klicken Sie auf die Audit-Datensatzes, um die Seite **Details** flyoutmenü anzuzeigen, und klicken Sie dann auf **Weitere Informationen**. Weitere Informationen zu den gelöschte Elemente, wie die Betreffzeile und den Speicherort des Elements, wenn es gelöscht wurde, wird im Feld **AffectedItems** angezeigt. Die folgenden Screenshots zeigen ein Beispiel für das Feld **AffectedItems** aus einem vorläufig gelöschten Element und ein Element Festplatte gelöscht.

**Beispiel für AffectedItems Feld für vorläufig gelöschten Element**

![Audit-Datensatz für vorläufig gelöschten Element](media/softdeleteditem.png)

**Beispiel für AffectedItems Feld für Element Festplatte gelöscht**

![Audit-Datensatz für harte gelöschten e-Mail-Element](media/harddeleteditem.png)

### <a name="recovering-deleted-email-items"></a>Wiederherstellen von gelöschten e-Mail-Elementen

Benutzer können vorläufig gelöschte Elemente wiederherstellen, wenn die Aufbewahrungszeit für gelöschte Elemente nicht abgelaufen ist. In Exchange Online die gelöschte Elemente Beibehaltungsdauer beträgt standardmäßig 14 Tage, jedoch können Administratoren diese Einstellung auf ein Maximum von 30 Tagen erhöhen. Punkt Benutzer [Wiederherstellen gelöschter Elemente oder e-Mail in Outlook Web App](https://support.office.com/article/Recover-deleted-items-or-email-in-Outlook-Web-App-C3D8FC15-EEEF-4F1C-81DF-E27964B7EDD4) Artikel eine Anleitung zum Wiederherstellen von gelöschten Objekten.

Wie bereits erklärt Administratoren möglicherweise schwer gelöschte Elemente wiederherstellen, wenn die Aufbewahrungszeit für gelöschte nicht abgelaufen ist oder wenn das Postfach befindet sich auf halten, Elemente werden in diesem Fall beibehalten, bis die Warteschleife Dauer abläuft. Beim Ausführen einer Inhaltssuche werden vorläufig gelöschten und schwer gelöschte Elemente im Ordner "wiederherstellbare Elemente" in den Suchergebnissen zurückgegeben, wenn sie die Search-Abfrage übereinstimmen. Weitere Informationen zum Ausführen von Content-Suche finden Sie unter [Inhalte suchen in Office 365](content-search.md).

> [!TIP]
> Suchen Sie zum Suchen nach gelöschten e-Mail-Elemente für alle oder einen Teil der Betreffzeile, die im Feld **AffectedItems** im Audit Datensatz angezeigt wird.

## <a name="determining-if-a-user-created-an-inbox-rule"></a>Feststellen, ob ein Benutzer eine Posteingangsregel erstellt.

Wenn Benutzer eine Posteingangsregel für Exchange Online-Postfach erstellen, wird ein entsprechende Audit Datensatz in das Überwachungsprotokoll gespeichert. Weitere Informationen zu Posteingangsregeln finden Sie unter:

- [Verwenden von Posteingangsregeln in Outlook im Web](https://support.office.com/article/use-inbox-rules-in-outlook-on-the-web-8400435c-f14e-4272-9004-1548bb1848f2)
- [Verwalten von e-Mail-Nachrichten in Outlook mithilfe von Regeln](https://support.office.com/article/Manage-email-messages-by-using-rules-C24F5DEA-9465-4DF4-AD17-A50704D66C59)

Hier ist ein Audit Log Suchabfrage für dieses Szenario zu konfigurieren:

**Aktivitäten** - unter dem **Exchange-Postfach Aktivitäten**, wählen Sie **New-InboxRule erstellen/ändern/Aktivieren/Deaktivieren der Posteingangsregel**.

**Startdatum** und **Enddatum** – wählen Sie einen Datumsbereich aus, der für Ihre Untersuchung anwendbar ist.

**Benutzer** :, wenn Sie einen bestimmten Benutzer untersuchen sind, lassen Sie dieses Feld leer. Dies hilft Ihnen neue Posteingangsregeln Einrichten von jedem Benutzer zu identifizieren.

**Dateien, Ordner, oder Site** – lassen Sie dieses Feld leer.

Nach dem Ausführen der Suche werden keine Audit-Datensätze für diese Aktivität in den Suchergebnissen angezeigt. Klicken Sie auf einen Audit-Eintrag, um die Seite **Details** flyoutmenü anzuzeigen, und klicken Sie dann auf **Weitere Informationen**. Informationen zu den Posteingang regeleinstellungen im Feld **Parameter** angezeigt werden. Die folgenden Screenshot und Beschreibungen werden die Informationen zu Posteingangsregeln behandelt.

![Audit-Eintrag für neue Posteingangsregel](media/NewInboxRuleRecord.png)

a. Klicken Sie in das Feld **ObjectId** wird der vollständige Namen der Posteingangsregel angezeigt. Dieser Name enthält den Alias des Postfach des Benutzers (z. B. SaraD) und den Namen der Posteingangsregel an (beispielsweise "Verschieben von Nachrichten aus Admin").

b. Klicken Sie im Feld **Parameter** wird die Bedingung der Posteingangsregel angezeigt. In diesem Beispiel wird die Bedingung durch den Parameter *aus* angegeben. Der Wert für den Parameter *aus* definiert gibt an, dass die Posteingangsregel admin@alpinehouse.onmicrosoft.com gesendeten e-Mail fungiert. Eine vollständige Liste der Parameter, die zum Definieren der App Posteingangsregeln verwendet werden können, finden Sie unter [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) Artikel.

c. der *MoveToFolder* -Parameter gibt die Aktion für die Posteingangsregel an. In diesem Beispiel werden Nachrichten von admin@alpinehouse.onmicrosoft.com in den Ordner mit dem Namen *AdminSearch*verschoben. Außerdem finden Sie unter [New-InboxRule](https://docs.microsoft.com/powershell/module/exchange/mailboxes/new-inboxrule) Artikel für eine vollständige Liste der Parameter, mit denen die Aktion der Posteingangsregel an definieren können.

d. das **Benutzer-ID** das Feld an der Benutzer, der die Posteingangsregel an im Feld **ObjectId** angegebenen erstellt hat. Dieser Benutzer ist auch in der Spalte **Benutzer** auf der Suchergebnisseite angezeigt.