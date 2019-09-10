---
title: Verwalten von isolierten Nachrichten und Dateien als Administrator in Office 365
ms.author: tracyp
author: MSFTTracyp
manager: dansimp
ms.date: 09/05/2018
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 065cc2cf-2f3a-47fd-a434-2a20b8f51d0c
ms.collection:
- M365-security-compliance
description: 'Administratoren erfahren, wie Sie isolierte Nachrichten im Office 365 Security #a0 Compliance Center anzeigen und verwalten können.'
ms.openlocfilehash: 0b67abe3dbf21650925b53d2882bc40096d6a646
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822525"
---
# <a name="manage-quarantined-messages-and-files-as-an-admin-in-office-365"></a>Verwalten von isolierten Nachrichten und Dateien als Administrator in Office 365

Als Administrator können Sie in Office 365 unter Quarantäne gestellte Nachrichten anzeigen, freigeben und löschen sowie falsch positive Nachrichten in Quarantäne melden. Sie können auch isolierte Dateien anzeigen, herunterladen und löschen, die von Advance Threat Protection (ATP) für SharePoint Online, OneDrive für Unternehmen und Microsoft Teams erfasst werden. Sie können Richtlinien so einrichten, dass Nachrichten von Office 365 gefiltert und aus mehreren Gründen an die Quarantäne gesendet werden: weil Sie als Spam, Massen-e-Mails, Phishing-e-Mails, Schadsoftware oder aufgrund einer e-Mail-Fluss Regel identifiziert wurden.

Standardmäßig sendet Office 365 Phishingnachrichten und Nachrichten mit Schadsoftware direkt in Quarantäne. Andere gefilterte Nachrichten werden an den Junk-e-Mail-Ordner der Benutzer gesendet, es sei denn, Sie richten eine Richtlinie zum Senden an den Quarantänebereich ein.

Zum Anzeigen und Ausführen von Aktionen für isolierte Nachrichten im Security #a0 Compliance Center benötigt Ihr Konto eine der folgenden Berechtigungen:

**Rolle "View-Only Recipients**": zeigt die Liste der in Quarantäne befindlichen Nachrichten an.

**Rolle des Sicherheits Lesers**: zeigt die Liste der isolierten Nachrichten und deren Nachrichtenkopfzeilen an.

**Rolle des Sicherheitsadministrators**: zeigt die Liste der isolierten Nachrichten und deren Nachrichtenkopfzeilen an; Vorschau, Freigabe, Löschung und Download von isolierten Nachrichten.

Standardmäßig ist für die Sicherheitsadministrator-und Organisations Verwaltungsrollengruppen im Security #a0 Compliance Center die Sicherheitsadministrator Rolle zugewiesen (die Mitgliedschaft in einer dieser Rollengruppen erteilt Ihnen die Berechtigungen). Weitere Informationen finden Sie unter [Berechtigungen im Office 365 Security #a0 Compliance Center](permissions-in-the-security-and-compliance-center.md).

> [!IMPORTANT]
> Standardmäßig werden Spam, Massen-und Phishing-Nachrichten 30 Tage lang in Quarantäne aufbewahrt. Nachrichten, die unter Quarantäne gestellt werden, weil Sie einer Nachrichtenfluss Regel entsprechen, werden für 7 Tage in Quarantäne aufbewahrt. Schadsoftware-Nachrichten werden 15 Tage lang in Quarantäne aufbewahrt. Sie können die Spamquarantäne Zeit in den Antispam-Einstellungen im Security #a0 Compliance Center anpassen. Wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht zurück bekommen. Wenn Sie möchten, können Sie den Aufbewahrungszeitraum für isolierte Nachrichten in ihren Anti-Spam-Filterrichtlinien ändern. Weitere Informationen finden Sie im Abschnitt [Festlegen des Aufbewahrungszeitraums für Quarantäne](#set-the-quarantine-retention-period) in diesem Thema.

## <a name="view-your-organizations-quarantined-messages"></a>Anzeigen der isolierten Nachrichten Ihrer Organisation

1. [Öffnen Sie das Security #a0 Compliance Center](go-to-the-securitycompliance-center.md) , und wechseln Sie zu **Threat Management** \> **Review** \> **Quarantine**.

   > [!TIP]
   > Wenn Sie direkt zur **Quarantäne** Seite wechseln möchten, verwenden Sie die folgende [https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)URL:.

   Standardmäßig zeigt das Security #a0 Compliance Center alle e-Mail-Nachrichten an, die als Spam isoliert wurden. Die Nachrichten werden basierend auf dem **Datum** , an dem die Nachricht empfangen wurde, von der neuesten bis zur ältesten sortiert. **Absender**, **Betreff**und das Ablaufdatum (unter **Expires**) werden ebenfalls für jede Nachricht angezeigt. Sie können nach einem Feld sortieren, indem Sie auf die entsprechende Spaltenüberschrift klicken; Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge umzukehren.

2. Sie können eine Liste aller in Quarantäne gestellten Nachrichten anzeigen oder das Resultset durch Filterung reduzieren. Sie können nur Massenvorgänge für bis zu 100 Elemente ausführen, sodass das Filtern auch dazu beitragen kann, Ihr Resultset zu reduzieren, wenn Sie mehr als das haben. Sie können Nachrichten schnell nach einem einzelnen Quarantäne Grund filtern, indem Sie eine Option aus dem Filter oben auf der Seite auswählen. Zu den Optionen gehören:

   - Als Spam identifizierte e-Mails

   - E-Mail-Quarantäne, da Sie mit einer Richtlinie übereinstimmt, die von einer Nachrichtenfluss Regel festgelegt wurde (auch als Transportregel bezeichnet)

   - Als Massen-e-Mail bezeichnete e-Mail

   - Als Phishing-e-Mails identifizierte e-Mails

   - E-Mail-Quarantäne, weil Sie Schadsoftware enthält

Als Administrator können Sie auch auswählen, dass alle Nachrichten für Ihre Organisation oder nur an Sie gesendete Nachrichten gefiltert werden. Endbenutzer können Nachrichten, die an Sie gesendet wurden, nur anzeigen und mit Ihnen arbeiten.

Sie können Ihre Ergebnisse auch filtern, um nach bestimmten Nachrichten zu suchen. Tipps finden Sie in diesem Thema im Abschnitt [Filtern der Ergebnisse nach isolierten Nachrichten und Dateien finden](#filter-the-results-to-find-quarantined-messages-and-files) Sie unter.

Nachdem Sie eine bestimmte isolierte Nachricht gefunden haben, klicken Sie auf die Nachricht, um Details dazu anzuzeigen und Aktionen durchführen zu können, wie das Freigeben der Nachricht an das Postfach eines anderen Benutzers.

## <a name="view-your-organizations-quarantined-files"></a>Anzeigen der isolierten Dateien in Ihrer Organisation

1. [Öffnen Sie das Security #a0 Compliance Center](go-to-the-securitycompliance-center.md) , und wechseln Sie zu **Threat Management** \> **Review** \> **Quarantine**.

   > [!TIP]
   > Wenn Sie direkt zur **Quarantäne** Seite im Security #a0 Compliance Center wechseln möchten, verwenden Sie die folgende URL: #a1[https://protection.office.com/?hash=/quarantine](https://protection.office.com/?hash=/quarantine)

   Standardmäßig werden in der Seite isolierte e-Mail-Nachrichten angezeigt. Zum Anzeigen von isolierten Dateien legen Sie die Filter oben auf der Seite so fest, dass **Dateien**angezeigt werden, die aufgrund **Schadsoftware**isoliert wurden.

   Die Dateien werden basierend auf dem Datum, an dem die Datei isoliert wurde, von der neuesten bis zur ältesten sortiert. Der **Benutzer** , der die Datei zuletzt geändert hat, der **Dienst** , auf den die Datei geschrieben wurde, der **Dateiname**, der **Speicherort**, die **Dateigröße**und das Ablaufdatum ( **Expires**) werden ebenfalls für jede Datei aufgelistet. Sie können nach einem Feld sortieren, indem Sie auf eine Kopfzeile klicken; Klicken Sie ein zweites Mal auf eine Spaltenüberschrift, um die Sortierreihenfolge umzukehren.

2. Sie können eine Liste aller in Quarantäne befindlichen Dateien anzeigen, oder Sie können nach bestimmten Dateien suchen, indem Sie filtern. Genau wie Nachrichten können Sie nur Massenvorgänge für bis zu 100 Elemente ausführen. Derzeit können Sie mit dem Security #a0 Compliance Center Dateien anzeigen und verwalten, die sich in Quarantäne befinden, da Sie als Schadsoftware erkannt wurden. Tipps finden Sie im nächsten Abschnitt.

## <a name="filter-the-results-to-find-quarantined-messages-and-files"></a>Filtern der Ergebnisse zum Suchen nach Nachrichten und Dateien in Quarantäne

Je nach Ihren Einstellungen gibt es möglicherweise viele isolierte Nachrichten und Dateien. Zum Auffinden einer bestimmten Nachricht oder Datei oder eines Satzes von Nachrichten oder Dateien können Sie unter Quarantäne gestellte Elemente basierend auf einer Vielzahl zusätzlicher Informationen filtern.

1. Stellen Sie auf der Seite " **Quarantäne** " sicher, dass die oberste Reihe von Filtern so festgelegt ist, dass Nachrichten oder Dateien entsprechend angezeigt werden:

   - Zum Suchen nach Dateien legen Sie die Filter so fest, dass **Dateien** angezeigt werden, die aufgrund von **Schadsoftware**isoliert wurden.

     Bei isolierten Dateien werden auf der Seite alle isolierten Dateien angezeigt, nicht nur Ihre eigenen, unabhängig davon, was Sie anzeigen möchten.

   - Zum Suchen nach isolierten Nachrichten legen Sie Filter so fest, dass **alle** oder **nur meine** **e-Mails**angezeigt werden. Für den letzten Filter wählen Sie den Typ der isolierten Nachricht aus, nach der gesucht werden soll. Sie können nach Nachrichten suchen, die als **Spam**identifiziert wurden, für Nachrichten, die einer e-Mail-Fluss Regel (**Transportregel**), **Massen** Nachrichten, **Phishing** -e-Mails oder e-Mails mit **Schadsoftware**entsprachen.

2. Wählen Sie unter **Ergebnisse sortieren nach**die Filter oder Filter aus, die Sie für die Suche in den Dropdownlisten verwenden möchten. Die Optionen variieren je nachdem, ob Sie nach Dateien oder Nachrichten suchen. Platzhalter werden zu diesem Zeitpunkt in Suchfeldern nicht unterstützt.

   Für Dateien und Nachrichten können Sie festlegen, dass nach dem Datum gefiltert wird, an dem die Nachricht oder Datei an die Quarantäne gesendet wurde. Sie können das Datum oder einen Datumsbereich angeben, einschließlich der Uhrzeit. Sie können Ihre Suchergebnisse auch nach dem Ablaufdatum filtern, an dem die Datei oder Nachricht aus der Quarantäne gelöscht wird, oder Sie können eine Kombination von Filtern verwenden. Um nach Ablaufdatum zu suchen, wählen Sie **Erweiterter Filter**aus. Unter **Expires**können Sie Nachrichten auswählen, die innerhalb der nächsten 24 Stunden ( **heute**) aus der Quarantäne gelöscht werden, innerhalb der nächsten 48 Stunden ( **nächsten 2 Tage**), innerhalb der nächsten Woche ( **Nächste 7 Tage**), oder Sie können ein benutzerdefiniertes Zeitintervall auswählen.

   Für Nachrichten haben Sie die folgenden zusätzlichen Optionen:

   - Nach **richten-ID**: Verwenden Sie diese, um eine bestimmte Nachricht zu identifizieren, wenn Sie die Nachrichten-ID kennen.

     Wenn beispielsweise eine bestimmte Nachricht von einem Benutzer in Ihrer Organisation gesendet oder dafür vorgesehen wird, aber nie sein Ziel erreicht hat, können Sie mithilfe einer [Nachrichtenablaufverfolgung](message-trace-scc.md)nach der Nachricht suchen. Wenn Sie feststellen, dass die Nachricht an die Quarantäne gesendet wurde, weil Sie möglicherweise mit einer Nachrichtenfluss Regel übereinstimmt oder als Spam identifiziert wurde, können Sie diese Nachricht dann leicht in der Quarantäne finden, indem Sie die zugehörige Nachrichten-ID angeben. Achten Sie darauf, die vollständige Nachricht-ID-Zeichenfolge einzubeziehen. Dies kann auch spitzen Klammern (\<\>) umfassen, beispielsweise `<79239079-d95a-483a-aacf-e954f592a0f6@XYZPR00BM0200.contoso.com>`:.

   - **Absender-e-Mail-Adresse**: Wählen Sie filtern nach einer einzelnen Absender-e-Mail-Adresse.

   - **Empfänger-e-Mail-Adresse**: Wählen Sie, um nach einer einzelnen Empfänger-e-Mail-Adresse zu filtern

   - **Betreff**. Geben Sie den Betreff einer e-Mail-Adresse ein, die Sie suchen möchten. Da die Suche nach Platzhalter nicht unterstützt wird, müssen Sie den gesamten Betreff der Nachricht verwenden, damit die Nachricht in den Ergebnissen zurückgegeben wird. Bei der Suche wird die Groß-/Kleinschreibung nicht beachtet.

## <a name="view-details-about-quarantined-messages-and-files"></a>Anzeigen von Details zu isolierten Nachrichten und Dateien

Wenn Sie ein in der Quarantäneliste angezeigtes Element auswählen, wird im **Detail** Bereich auf der rechten Seite des Security #a0 Compliance Center eine Zusammenfassung der Eigenschaften angezeigt.

### <a name="details-displayed-for-quarantined-messages"></a>Für isolierte Nachrichten angezeigte Details

- Nach **richten-ID**: der eindeutige Bezeichner für die Nachricht.

- **Absenderadresse**: Wer die Nachricht gesendet hat.

- **Received**: das Datum und die Uhrzeit, zu der die Nachricht empfangen wurde.

- **Subject**: der Text der Betreffzeile der Nachricht.

- **Typ**: zeigt an, ob eine Nachricht als **Spam**, **Massen**, **Phishing**, Übereinstimmung mit einer Nachrichtenfluss Regel (**Transport Regel**) identifiziert wurde oder als enthaltender **Schadsoftware**erkannt wurde.

- **Expires**: das Datum und die Uhrzeit, zu der die Nachricht automatisch aus der Quarantäne gelöscht wird.

- **Veröffentlicht für**: alle e-Mail-Adressen (falls vorhanden), für die die Nachricht freigegeben wurde.

- **Noch nicht freigegeben an**: alle e-Mail-Adressen (falls vorhanden), für die die Nachricht noch nicht freigegeben wurde.

### <a name="details-displayed-for-quarantined-files"></a>Für isolierte Dateien angezeigte Details

- **Dateiname**: der Name der Datei in Quarantäne.

- **Websitepfad**: URL, die den Speicherort der Datei in Office 365 definiert.

- **Erkannte Datum/Uhrzeit**: das Datum und die Uhrzeit, zu der die Datei isoliert wurde.

- **Expires**: das Datum, an dem die Nachricht aus der Quarantäne gelöscht wird.

- **Erkannt von**: die Methode, mit der die Schadsoftware in der Datei erkannt wird. Dies kann entweder ATP (Advanced Threat Protection) oder das Anti-Malware-Modul von Microsoft sein.

- **Veröffentlicht**: Beschreibt, ob die Datei freigegeben wurde oder nicht.

- **Name der Malware**: Familie und Name der in der Datei gefundenen Schadsoftware.

- **Dokument-ID**: ein eindeutiger Bezeichner für das Dokument.

- **Dateigröße**: die Größe der Datei in KB.

- **Organisation**: die eindeutige ID Ihrer Organisation in Office 365.

- **Geändert von**: das Arbeits-oder Schulkonto des Benutzers, der die Datei zuletzt geändert hat.

- **Dateigröße**: die Größe der Datei in KB.

- **SHA256-Hash**: der Hash der Datei. Sie können dies verwenden, um nach anderen Reputation Stores zu suchen, die Sie möglicherweise haben, oder um herauszufinden, wo sich die Datei sonst in Ihrer Umgebung befinden könnte.

## <a name="manage-messages-and-files-in-quarantine"></a>Verwalten von Nachrichten und Dateien in der Quarantäne

Nachdem Sie eine Nachricht oder eine Gruppe von Nachrichten in der Quarantäne ausgewählt haben, haben Sie mehrere Möglichkeiten, mit den Nachrichten zu tun:

- Nichts tun: Wenn Sie nichts tun, wird die Nachricht nach Ablauf von Office 365 automatisch gelöscht. Standardmäßig werden Spam, Massen, Schadsoftware, Phishing und Nachrichten, die mit einer e-Mail-Fluss Regel übereinstimmen, in Quarantäne für 30 Tage aufbewahrt. Wenn Office 365 eine Nachricht aus der Quarantäne löscht, können Sie Sie nicht zurück bekommen. Wenn Sie möchten, können Sie den Aufbewahrungszeitraum für isolierte Nachrichten ändern, indem Sie die Einstellung **Spam für (Tage)** in ihren Anti-Spam-Richtlinien konfigurieren. Weitere Informationen finden Sie im Abschnitt [Festlegen des Aufbewahrungszeitraums für Quarantäne](#set-the-quarantine-retention-period) in diesem Thema.

- **Nachrichtenkopfzeile anzeigen**: Wählen Sie diesen Link aus, um den Text der Nachrichtenkopfzeile anzuzeigen. Um die Kopfzeile eingehend zu analysieren, kopieren Sie den Text der Nachrichtenkopfzeile in die Zwischenablage, und wählen Sie dann **Microsoft Message Header Analyzer** aus, um zur Remote Verbindungs Untersuchung zu wechseln (Klicken Sie mit der rechten Maustaste, und wählen Sie **in einer neuen Registerkarte öffnen** aus, wenn Sie Office nicht verlassen möchten. 365, um diese Aufgabe abzuschließen). Fügen Sie die Kopfzeile der Nachricht auf der Seite im Abschnitt Nachrichtenkopf Analyse ein, und wählen Sie **Kopfzeilen analysieren**aus.

- **Vorschau Nachricht**: ermöglicht das Anzeigen von Rohdaten-oder HTML-Versionen des Nachrichtentext Texts. In der HTML-Ansicht sind Links deaktiviert.

- **Download Nachricht** oder **Downloaddatei**: Wählen Sie diese Option aus, um eine Kopie der Nachricht oder Datei auf Ihr lokales Gerät herunterzuladen. Sie müssen sich vergewissern, dass Sie die Risiken im Zusammenhang mit dem Herunterladen von Elementen aus der Quarantäne kennen, bevor Sie dies tun können. Nachrichten werden im eml-Format in einem von Ihnen angegebenen Ordner gespeichert. In Quarantäne befindliche Dateien werden im ursprünglichen Format gespeichert.

- **Delete**: Wenn Sie möchten, können Sie sofort ein isoliertes Element (oder eine Gruppe von Elementen) löschen, anstatt auf das vom Office 365 festgelegte Ablaufdatum zu warten. Zum Löschen einer Nachricht oder Datei wählen Sie in der Quarantäneliste das Element aus, und klicken Sie dann auf **Löschen**. Wenn Sie mehrere Elemente gleichzeitig löschen möchten, aktivieren Sie das Kontrollkästchen links neben den Elementen in der Quarantäneliste, und wählen Sie dann auf der angezeigten Seite **Massenaktionen** die Option **ausgewählte Nachrichten löschen** oder **ausgewählte Dateien löschen**aus.

- **Release**: Freigeben eines isolierten Elements (oder einer Gruppe von Elementen) und melden der Elemente als falsch isoliert (falsch positive Ergebnisse) an Microsoft.

  Wenn Sie eine einzelne Nachricht oder Datei freigeben und melden möchten, wählen Sie in der Quarantäneliste das Element aus, und wählen Sie **Datei freigeben** oder **Nachricht freigeben**aus. Stellen Sie auf der nächsten Seite sicher, dass **Berichtsmeldungen an Microsoft für Analyse** -oder **Berichtsdateien an Microsoft für Analyse** ausgewählt ist.

  Wenn Sie mehrere Elemente gleichzeitig freigeben möchten, aktivieren Sie das Kontrollkästchen links neben den Elementen in der Quarantäneliste, und wählen Sie dann auf der angezeigten Seite **Massenaktionen** die Option **Dateien freigeben** oder **Nachrichten**freigeben aus. Stellen Sie auf der nächsten Seite sicher, dass **Berichtsmeldungen an Microsoft für Analyse** -oder **Berichtsdateien an Microsoft für Analyse** ausgewählt ist.

Beachten Sie beim Freigeben von Nachrichten Folgendes:

- Wenn Sie eine Massen Veröffentlichung mehrerer Nachrichten gleichzeitig ausführen, werden die Nachrichten für alle ursprünglich identifizierten Empfänger freigegeben. Wenn Sie nur Nachrichten nur für bestimmte Empfänger freigeben möchten, müssen Sie die Nachrichten nacheinander freigeben und die Empfänger einzeln identifizieren.

- Eine Nachricht kann nicht mehrmals an denselben Empfänger freigegeben werden.

- Wenn Sie eine Nachricht an mehrere Empfänger freigeben, werden nur Empfänger, die die Nachricht zuvor nicht erhalten haben, in der Liste der potenziellen Empfänger angezeigt.

- Wenn Sie sich entscheiden, falsch positive Ergebnisse zu melden, werden die Nachrichten, die Sie freigegeben haben, als Spam, Massen, Phishing oder als enthaltender Schadsoftware isoliert, dann wird die Nachricht auch an das Microsoft-Spam Analyse Team gemeldet. Das Team bewertet und analysiert die Nachricht, und je nach den Ergebnissen der Analyse können die Filterregeln für den Dienst weiten Spam Inhalt so angepasst werden, dass die Nachricht durchlassen wird.

## <a name="set-the-quarantine-retention-period"></a>Festlegen des Aufbewahrungszeitraums für Quarantäne

Sie können konfigurieren, wie lange Nachrichten und Dateien in der Quarantäne verbleiben, bevor Sie ablaufen. Standardmäßig werden isolierte Elemente 30 Tage lang aufbewahrt. Sie konfigurieren diese Einstellung für jede Richtlinie, die Sie erstellen. Sie können den Wert für die Standardrichtlinie auch wie in diesem Artikel beschrieben ändern.

### <a name="modify-the-quarantine-retention-period-for-the-default-spam-filter-policy-in-the-security--compliance-center"></a>Ändern des Aufbewahrungszeitraums für die Quarantäne für die standardmäßige Spamfilter Richtlinie im Security #a0 Compliance Center

1. [Öffnen Sie das Security #a0 Compliance Center](go-to-the-securitycompliance-center.md) , und wechseln Sie zu **Threat Management** \> **Policy** \> **Anti-Spam**.

   > [!TIP]
   > Wenn Sie direkt zur **Antispam-** Seite wechseln möchten, verwenden Sie die folgende URL:[https://protection.office.com/?hash=/antispam](https://protection.office.com/?hash=/antispam)

2. Wählen Sie **Benutzerdefiniert** aus, um die Registerkarte **benutzerdefinierte Einstellungen** anzuzeigen.

3. Erweitern Sie die Zeile **Standard-Spamfilter Richtlinie (Always on)** .

4. Wählen Sie **Richtlinie bearbeiten**aus. Die Einstellungen für die standardmäßige Spamfilter Richtlinie werden auf einer neuen Seite angezeigt.

5. Erweitern Sie **Spam-und Massenaktionen**.

6. Geben Sie unter **Quarantäne**im Textfeld **Spam für (Tage) beibehalten** den Zeitraum ein, in dem Office 365 Nachrichten und Dateien in der Quarantäne aufbewahrt werden sollen. Der Standardwert beträgt 30 Tage. Dies ist auch die maximale.

7. Wählen Sie **Speichern** aus.
