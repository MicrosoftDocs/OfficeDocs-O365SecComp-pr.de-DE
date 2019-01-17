---
title: Nachricht Trace in die & Security Compliance Center
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
description: Administratoren können nachrichtenablaufverfolgung in der & Security Compliance Center um herauszufinden, was mit Nachrichten geschehen ist.
ms.openlocfilehash: 9dfdab4adc5caba55664e93b49c8428791670ab3
ms.sourcegitcommit: 25fb33a1f8b2844fde15f6c03db2936c610824e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28685469"
---
# <a name="message-trace-in-the-security--compliance-center"></a>Nachricht Trace in die & Security Compliance Center

Nachricht Trace in die & Security Compliance Center folgt e-Mail-Nachrichten, wie sie über die Exchange Online-Organisation unterwegs sind. Sie können festlegen, ob eine Nachricht empfangen, abgelehnt, zurückgestellt oder vom Dienst übermittelt wurde. Außerdem wird gezeigt, welche Aktionen für die Nachricht ausgeführt wurden, bevor sie den letzten Status erreicht.

Nachricht Trace in die & Security Compliance Center verbessert nachrichtenablaufverfolgung, die in der Exchange-Verwaltungskonsole (EAC) verfügbar war. Die Informationen aus der nachrichtenablaufverfolgung können Sie effizient Benutzer Änderungen an ihre Nachrichten bei der Fragen beantworten, Mail Flow Probleme zu beheben und Richtlinie Änderungen überprüfen.

## <a name="open-message-trace"></a>Open nachrichtenablaufverfolgung

1. [Melden Sie sich bei Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) mit Ihrem Firmen- oder Schulkonto an.

2. Wählen Sie das Symbol für das App-Startfeld ![Symbol für Office 365-App-Startfeld](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) in der oberen linken Ecke und dann **Administrator** aus.

3. Erweitern Sie in der unteren linken Navigationsbereich **Zentriert Admin** - **Sicherheit & Compliance**.

4. Auf der Seite **Sicherheit & Compliance** , die geöffnet wird, erweitern Sie **E-Mail-Fluss**und wählen Sie **nachrichtenablaufverfolgung**.

## <a name="message-trace-page"></a>Nachricht Trace-Seite

Hier können Sie eine neue Standard Verfolgung, indem Sie auf die Schaltfläche **Starten Sie eine Verfolgung** starten. Dies wird für alle Nachrichten für alle Absender und Empfänger für den letzten zwei Tagen gesucht. Oder Sie können eine der gespeicherten Abfragen aus den Kategorien verfügbaren Abfrageregeln und führen Sie diese als- verwenden Sie diese als Ausgangspunkt für Ihre eigenen Abfragen:

- **Default Abfragen**: integrierte Abfragen von Office 365 bereitgestellt.

- **Benutzerdefinierte Abfragen**: Abfragen von Administratoren in Ihrer Organisation für die zukünftige Verwendung gespeichert.

- **Automatisch gespeicherte Abfragen**: die letzten zehn Abfragen die zuletzt ausgeführt. In dieser Liste können sie ganz einfach Stelle aufzunehmen.

Auf dieser Seite ist ein Abschnitt **zum Herunterladen von Berichten** für die von Ihnen übermittelten Anfragen als auch die Berichte selbst auch wenn zum Download zur Verfügung stehen.

## <a name="options-for-a-new-message-trace"></a>Optionen für eine neue nachrichtenablaufverfolgung

### <a name="filter-by-senders-and-recipients"></a>Filtern Sie nach Absender und Empfänger

Die Standardwerte sind **Alle Absender** und **alle Empfänger**, aber Sie können die folgenden Felder verwenden, um die Ergebnisse zu filtern:

- **Durch diese Personen**: Klicken Sie in dieses Feld, um eine oder mehrere Absender aus Ihrer Organisation auszuwählen. Sie können auch beginnen, geben Sie einen Namen und die Elemente in der Liste werden vom, viel Eingabe wie das Verhalten von einer Seite gefiltert werden.

- **Für diese Personen**: Klicken Sie in dieses Feld, um einen oder mehrere Empfänger in Ihrer Organisation auszuwählen.

Sie können auch die e-Mail-Adressen von externen Absendern und Empfängern eingeben. Es werden keine Platzhalter unterstützt (`*@contoso.com` oder `scot?@contoso.com`), jedoch nicht mehrere Einträge mit Platzhaltern gleichzeitig im gleichen Feld verwenden.

### <a name="time-range"></a>Zeitbereich

Der Standardwert ist **2 Tage**, aber Sie können die Bereiche für Datum/Uhrzeit bis zu 90 Tage angeben. Wenn Sie Datum/Uhrzeit Bereiche verwenden, sollten Sie auf Folgendes berücksichtigen:

- Standardmäßig wählen Sie den Zeitraum in **Schieberegler** Ansicht mit einer Zeitlinie. Sie können nur wählen Sie den Tag oder Zeiteinstellungen, die angezeigt werden. Versuch, wählen Sie einen Wert zwischen Start-/End Blase zum Ausrichten wird die nächste Einstellung angezeigt.

   ![Ein Schieberegler Zeitbereich in eine neue Nachricht Trace in die & Security Compliance Center](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   Aber Sie können auch **benutzerdefinierte** Ansicht, in dem Sie können das **Startdatum** und **Enddatum** Werte (einschließlich Zeiten) angeben, und Sie können auch die **Zeitzone** für den Bereich für Datum/Uhrzeit auswählen, wechseln. Beachten Sie, dass die Einstellung **Zeitzone** für Ihre Abfrage Eingaben und den Abfrageergebnissen gilt.

   ![Eine benutzerdefinierte Zeitbereich in eine neue Nachricht Trace in die & Security Compliance Center](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   Für 10 Tage oder weniger, die Ergebnisse werden sofort als **ein Zusammenfassungsbericht** zur Verfügung. Wenn Sie einen Zeitraum, der auch geringfügig größer als 10 Tage ist angeben, werden die Ergebnisse verzögert nur als einer herunterladbaren CSV-Datei ( **Enhanced Zusammenfassung** oder **Erweitert** Berichte) verfügbar sind.

   Weitere Informationen zu den verschiedenen Berichtstypen finden Sie [Berichtstyp auswählen](#choose-report-type) im Abschnitt in diesem Thema.

   **Hinweis**: Erweiterte Zusammenfassung und nicht erweiterten Berichte mithilfe von archivierten Daten der nachrichtenablaufverfolgung vorbereitet werden, und es kann bis zu mehrere Stunden, bevor Sie der Bericht zum Download zur Verfügung steht dauern. Je nachdem, wie viele andere Administratoren auch Anfragen etwa zur gleichen Zeit übermittelt haben bemerken Sie möglicherweise auch eine Verzögerung vor Beginn der Verarbeitung für Ihre Anforderung in der Warteschlange.

- Speichern einer Abfrage in der Ansicht **Schieberegler** speichert den relative Zeitbereich (beispielsweise 3 Tage ab heute). Speichern einer Abfrage in der **benutzerdefinierten** Ansicht speichert die absolute Datum-/Uhrzeitbereich (beispielsweise 2018-05-06 13:00 Uhr bis 2018-05-08 18:00).

### <a name="more-search-options"></a>Weitere Suchoptionen

#### <a name="delivery-status"></a>Zustellungsstatus

Lassen Sie den Standardwert **Alle** ausgewählt, oder wählen Sie eine der folgenden Werte, um die Ergebnisse zu filtern:

- **Übermittelte**: die Nachricht wurde erfolgreich an das vorgesehene Ziel übermittelt.

- **Ausstehend**: Zustellung der Nachricht wird versucht oder wird erneut versucht.

- **Erweitert**: Verteilung Gruppen als Empfänger vor der Zustellung an den einzelnen Mitgliedern der Gruppe erweitert wurde.

- **Fehler**: die Nachricht wurde nicht übermittelt.

- **Isoliert**: die Nachricht wurde unter Quarantäne gestellte e-Mails (als Spam, Massen- oder Phishing). Weitere Informationen finden Sie unter [Quarantäne e-Mail-Nachrichten in Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).

- **Gefilterte als Spam**: die Nachricht war Spam identifiziert und wurde abgelehnt oder blockiert (nicht in Quarantäne).

- **Erste Status:** Die Nachricht wurde vor kurzem von Office 365 empfangen, aber keine anderen Statusdaten ist noch verfügbar. Versuchen Sie es ein paar Minuten.

**Hinweis**: die Werte **offen,** **isoliert**und **Filter als Spam** sind nur verfügbar für die Suche weniger als 10 Tage. Darüber hinaus gibt es möglicherweise eine Verzögerung von 5 bis 10 Minuten zwischen dem tatsächlichen und gemeldete Zustellungsstatus.

#### <a name="message-id"></a>Nachrichten-ID

Dies ist die Internetnachrichten-ID (auch bekannt als die Client-ID), die im gefunden wird die **Nachrichten-ID:** Kopfzeilenfeld in der Kopfzeile der Nachricht. Benutzer können diesen Wert bestimmte Nachrichten untersuchen erteilen.

Dieser Wert ist für die Lebensdauer der Nachricht konstant. Für Nachrichten, die in Office 365 oder Exchange erstellt werden, ist der Wert im Format `<GUID@ServerFQDN>`, einschließlich der Spitze Klammern (\< \>). Beispielsweise `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Andere Messagingsysteme möglicherweise andere Syntax oder Werte verwenden. Dieser Wert sollte eindeutig sein, aber nicht von allen e-Mail-Systemen folgen streng dieser Anforderung. Wenn die **Nachrichten-ID:** Kopfzeilenfeld ist nicht vorhanden oder für eingehende Nachrichten von externen Quellen leer ist, wird ein beliebiger Wert zugewiesen.

Wenn Sie zum Filtern der Ergebnisse **Nachrichten-ID** verwenden, müssen Sie die vollständige Zeichenfolge, einschließlich alle spitzen Klammern eingeschlossen.

#### <a name="direction"></a>Direction

Lassen Sie den Standardwert **Alle** ausgewählt, oder Sie können auswählen, **eingehend** (Nachrichten an Empfänger in Ihrer Organisation gesendet) oder **ausgehend** (Nachrichten von Benutzern in Ihrer Organisation gesendet) zum Filtern der Ergebnisse.

#### <a name="original-client-ip-address"></a>Ursprüngliche Client-IP-Adresse

Sie können die Ergebnisse File-Server, indem Sie Client-IP-Adresse gehackten Computern untersuchen, die große Mengen von Spam oder Schadsoftware senden. Obwohl die Nachrichten anscheinend von mehreren Absendern stammt, ist es wahrscheinlich, dass auf der gleiche Computer aller Nachrichten generiert.

**Hinweis**: die Client-IP-Adressinformationen ist nur für 10 Tage zur Verfügung und ist nur verfügbar in den Berichten **Zusammenfassung erweiterter** oder **Erweitert** (herunterladbaren CSV-Dateien).

### <a name="choose-report-type"></a>Wählen Sie Berichtstyp

Die verfügbaren Berichtstypen sind:

- **Zusammenfassung**: verfügbar, wenn der Zeitbereich weniger als 10 Tage beträgt und keine zusätzlichen Filteroptionen erfordert. Die Ergebnisse sind verfügbar, fast sofort nach dem Sie **Suchen**klicken.

- **Erweiterte Zusammenfassung** oder **Erweitert**: Diese Berichte sind nur verfügbar als herunterladbare CSV-Dateien sowie eine oder mehrere der folgenden Filteroptionen unabhängig von den Zeitbereich erforderlich:, **indem Sie diese Personen** **an diese Personen**oder ** Nachrichten-ID**. Sie können Platzhalter für den Absender oder Empfänger verwenden (beispielsweise \*@contoso.com).

**Hinweise**:

- Erweiterte Zusammenfassung und nicht erweiterten Berichte mithilfe von archivierten Daten der nachrichtenablaufverfolgung vorbereitet werden, und es kann bis zu mehrere Stunden, bevor Sie der Bericht zum Herunterladen zur Verfügung steht dauern. Je nachdem, wie viele andere Administratoren auch Anfragen etwa zur gleichen Zeit übermittelt haben bemerken Sie möglicherweise auch eine Verzögerung vor Beginn der Ihre Anfrage in der Warteschlange verarbeitet werden.

- Während Sie auswählen können ein erweiterte Zusammenfassung oder erweiterte Bericht aus einem Datum-/Uhrzeitbereich, häufig die letzten vier Stunden von archivierten Daten werden nicht noch für diese zwei Arten von Berichten zur Verfügung.

Wenn Sie auf **Weiter**klicken, sind Sie können eine Zusammenfassungsseite, in der die Filteroptionen, die Sie ausgewählt haben aufgelistet, einen eindeutigen (bearbeitbar) Titel für den Bericht, und die e-Mail-Adresse, die die Benachrichtigung empfängt, wenn die nachrichtenablaufverfolgung (auch bearbeitet werden, abgeschlossen ist und in einer der akzeptierten Domänen Ihrer Organisation sein). Klicken Sie auf **Prepare-Bericht** , um die nachrichtenablaufverfolgung zu übermitteln. Klicken Sie im Hauptmenü **Message Trace** -Seite können Sie den Status des Berichts im Abschnitt **zum Herunterladen von Berichten** anzeigen.

Weitere Informationen zu den Informationen, der in den verschiedenen Berichtstypen zurückgegeben wird, finden Sie im nächsten Abschnitt.

## <a name="message-trace-results"></a>Ergebnisse der nachrichtenablaufverfolgung

Die verschiedenen Berichtstypen zurückgeben verschiedene Ebenen der Informationen. Die Informationen, die in den verschiedenen Berichten zur Verfügung steht, wird in den folgenden Abschnitten beschrieben.

### <a name="summary-report-output"></a>Zusammenfassungsbericht Ausgabe

Nach der Ausführung der nachrichtenablaufverfolgung, werden die Ergebnisse aufgeführt werden nach Datum/Uhrzeit (neueste zuerst) absteigend sortiert.

![Zusammenfassungsbericht Ergebnisse für die nachrichtenablaufverfolgung in der & Security Compliance Center](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

Der zusammenfassende Bericht enthält die folgende Informationen:

- **Datum**: Datum und Uhrzeit, an dem die Nachricht vom Dienst mithilfe der konfigurierten UTC-Zeitzone empfangen wurde.

- **Absender**: die e-Mail-Adresse des Absenders (*Alias*@*Domäne*).

- **Empfänger**: die e-Mail-Adresse des Empfängers oder Empfänger. Für eine Nachricht an mehrere Empfänger gesendet ist es eine Zeile pro Empfänger. Wenn der Empfänger eine Verteilergruppe, dynamische Verteilergruppe oder e-Mail-aktivierte Sicherheitsgruppe ist, die Gruppe den ersten Empfänger, und klicken Sie dann jedes Mitglied der Gruppe wird in einer separaten Zeile.

- **Betreff**: die ersten 256 Zeichen der Nachricht **Betreff:** dar.

- **Status**: Diese Werte werden im Abschnitt [Zustellungsstatus](#delivery-status) beschrieben.

Standardmäßig werden die ersten 250 Ergebnisse geladen und immer leicht zugänglich sind. Wenn Sie einen Bildlauf nach unten durchführen, wird eine kurzen Verzögerung, wie der nächste Batch von Ergebnissen geladen werden. Statt einen Bildlauf durchzuführen, können Sie **alle zu laden** , um alle Ergebnisse bis zu maximal 10.000 laden klicken.

Klicken Sie auf die Spaltenüberschriften zum Sortieren der Ergebnisse nach den Werten in dieser Spalte in aufsteigender oder absteigender Reihenfolge.

Sie können die **Ergebnisse der Filter** zum Filtern der Ergebnisse nach einer oder mehreren Spalten klicken.

Sie können die Ergebnisse exportieren, nachdem Sie eine oder mehrere Zeilen markiert haben, indem Sie auf **Ergebnisse exportieren** , und klicken Sie dann **alle Ergebnisse exportieren**, **Export Ergebnisse geladen**oder **Exportieren Sie ausgewählte**auswählen.

#### <a name="find-related-records-for-this-message"></a>Hier finden Sie verwandte Datensätze für diese Nachricht

Verwandte Nachrichtendatensätze werden Datensätze, die die gleiche Nachricht-ID gemeinsam genutzt Beachten Sie, dass auch eine einzelne Nachricht, die zwischen zwei Personen gesendet mehrere Datensätze generiert werden kann. Die Anzahl von Datensätzen erhöht, wenn die Nachricht durch die Erweiterung von Verteilergruppen, Weiterleitung, e-Mail-Flussregeln (auch als Transportregeln bezeichnet) betroffen ist.

Nachdem Sie eine Zeile Kontrollkästchen ausgewählt haben, finden Sie verwandte Datensätze für die Nachricht mit der Schaltfläche **Find beziehen** , die angezeigt wird oder indem Sie **Weitere Optionen** auswählen ![weitere](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **verknüpften Datensätze für diese Nachricht suchen**).

Weitere Informationen zu den Nachrichten-ID finden Sie im Abschnitt "Nachrichten-ID" weiter oben in diesem Thema.

#### <a name="message-trace-details"></a>Nachricht Trace-details

In der Ausgabe zusammenfassenden Bericht können Sie Details zu einer Nachricht anzeigen, mithilfe einer der folgenden Methoden:

- Wählen Sie die Zeile (klicken Sie auf eine beliebige Stelle in der Zeile außer dem Kontrollkästchen).

- Kontrollkästchen für die Zeile, und klicken Sie auf **Weitere Optionen** ![weitere](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Details der Nachricht anzeigen**.

   ![Details nach einem Doppelklick eine Zeile in der zusammenfassenden Bericht Nachricht Ablaufverfolgungsergebnisse in die & Security Compliance Center](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

Die Nachricht Trace Details enthalten die folgende zusätzliche Informationen, die in der zusammenfassenden Bericht nicht vorhanden ist:

- **Nachricht Ereignisse**: Dieser Abschnitt enthält Klassifikationen, mit deren Hilfe die Aktionen kategorisieren, die der Dienst für Nachrichten akzeptiert. Sind einige weitere interessante Ereignisse, die auftreten können:

   - **Empfangen**: die Nachricht wurde vom Dienst empfangen.

   - **Senden**: die Nachricht wurde vom Dienst gesendet.

   - **Fehler**: die Nachricht konnte nicht zugestellt werden.

   - **Übermitteln**: die Nachricht wurde an ein Postfach zugestellt.

   - **Erweitern**: die Nachricht wurde an eine Verteilergruppe, die erweitert wurde gesendet.

   - **Übertragen**: Empfänger wurden aufgrund von inhaltskonvertierung, empfängerbeschränkungen oder Agents in eine verzweigte Nachricht verschoben.

   - **Defer**: die Nachrichtenübermittlung wurde verschoben und möglicherweise werden erneut zu einem späteren Zeitpunkt.

   - **Gelöst**: die Nachricht wurde umgeleitet, um eine neue Adresse des Empfängers basierend auf einer Active Directory zu suchen. In diesem Fall wird die ursprüngliche Empfängeradresse in einer separaten Zeile in der Nachricht Trace zusammen mit den Status der Übermittlung der Nachricht aufgeführt.

   Beachten Sie, dass auch eine problemlosen an, die erfolgreich übermittelt werden **mehrere Einträge** in der nachrichtenablaufverfolgung generiert.

- **Weitere Informationen**: Dieser Abschnitt enthält die folgenden Details:

   - **Nachrichten-ID**: Dieser Wert wird in den [Nachrichten-ID](#message-id) -Abschnitt weiter oben in diesem Thema beschrieben. Beispielsweise `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

   - **Nachrichtengröße**

   - **Von IP-Adresse**: die IP-Adresse des Computers, der die Nachricht gesendet hat. Für ausgehende Nachrichten von Exchange Online beträgt dieser Wert leer.

   - **Um-IP**: die IP-Adressen, auf dem der Dienst hat versucht, die Nachricht übermitteln. Wenn eine Nachricht mehrere Empfänger enthält, werden diese angezeigt. Für eingehende Nachrichten zu Exchange Online gesendet beträgt dieser Wert leer.

### <a name="enhanced-summary-reports"></a>Erweiterte Zusammenfassungsberichte

Im Abschnitt **zum Herunterladen von Berichten** am Anfang Nachricht Trace sind verfügbar (abgeschlossenen) erweiterter Zusammenfassungsberichte verfügbar. Die folgende Informationen steht im Bericht zur Verfügung:

- **Origin_timestamp**<sup>*</sup>: Datum und Uhrzeit, wenn die Nachricht vom Dienst mithilfe der konfigurierten UTC-Zeitzone zunächst empfangen wurde.

- **Sender_address**: e-Mail-Adresse des Absenders (*Alias*@*Domäne*).

- **Recipient_status**: der Status der Zustellung der Nachricht an den Empfänger. Wenn die Nachricht an mehrere Empfänger gesendet wurde, es zeigt alle Empfänger und den entsprechenden Status für die einzelnen im Format: \< *e-Mail-Adresse*\>##\<*Status*\>. Zum Beispiel:

   - **Senden von ##Receive,** bedeutet, dass die Nachricht wurde vom Dienst empfangen und an das vorgesehene Ziel gesendet wurde.

   - **##Receive, ein Fehler auftritt** , bedeutet, dass die Nachricht durch den Dienst aber Zustellung an das vorgesehene Ziel konnte nicht empfangen wurde.

   - **Übermitteln von ##Receive,** bedeutet, dass die Nachricht wurde vom Dienst empfangen und an das Postfach des Empfängers übermittelt wurde.

- **Betreff der Nachricht**: die ersten 256 Zeichen der **Betreff der Nachricht** .

- **Total_bytes**: die Größe der Nachricht in Byte, einschließlich Anlagen.

- **Message_id**: Dieser Wert wird in den [Nachrichten-ID](#message-id) -Abschnitt weiter oben in diesem Thema beschrieben. Beispielsweise `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

- **Network_message_id**: eine eindeutige Nachrichten-ID-Wert, die über alle Kopien der Nachricht erhalten bleibt, die aufgrund der Erweiterung Verzweigung oder einer Verteilergruppe erstellt werden kann. Ein Beispielwert ist `1341ac7b13fb42ab4d4408cf7f55890f`.

- **Original_client_ip**: die IP-Adresse des Client des Absenders an.

- **richtungsabhängigkeit**: Gibt an, ob die Nachricht an (1) eingehend Ihrer Organisation gesendet wurde, oder ausgehende (2) von Ihrer Organisation gesendet wurde.

- **Connector_id**: der Name der Quell- oder Ziel-Verbindung. Weitere Informationen zu Connectors in Exchange Online finden Sie unter [Configure e-Mail-Fluss mithilfe von Connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).

- **delivery_priority zeigt**<sup>*</sup>: Gibt an, ob die Nachricht mit **hoher**, **niedriger**oder **normaler** Priorität gesendet wurde.

<sup>*</sup>Diese Eigenschaften sind nur verfügbar in erweiterter Zusammenfassungsberichte.

### <a name="extended-reports"></a>Erweiterte Berichte

Im Abschnitt **zum Herunterladen von Berichten** am Anfang des nachrichtenablaufverfolgung stehen zur Verfügung (abgeschlossenen) Extended Berichte. Nahezu alle Informationen aus einem erweiterter zusammenfassenden Bericht ist in einem Bericht Extended (mit Ausnahme von **Origin_timestamp** und **delivery_priority zeigt**) verfügbar. Die folgende zusätzliche Informationen steht nur in einem Bericht erweitert:

- **Client_ip**: die IP-Adresse des e-Mail-Servers oder der messaging-Client, der die Nachricht gesendet.

- **Client_hostname**: den Hostnamen oder FQDN des e-Mail-Server oder messaging-Client, der die Nachricht gesendet.

- **Server_ip**: die IP-Adresse des Servers Quell- oder Ziel.

- **Server_hostname**: den Hostnamen oder FQDN des Zielservers.

- **Source_context**: zusätzliche Informationen im Zusammenhang mit der **Datenquelle** dar. Zum Beispiel:

   - `Protocol Filter Agent`

   - `3489061114359050000`

- **Quelle**: der Exchange Online-Komponente, die für das Ereignis zuständig ist. Zum Beispiel:

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- **Event_id**: Diese entsprechen den **Message-Ereignis** -Werten, die im Abschnitt [Suchen verknüpften Datensätze für diese Nachricht](#find-related-records-for-this-message) erläutert werden.

- **Internal_message_id**: eine Nachricht-ID, die vom Exchange Online-Server zugewiesen ist, die gerade die Nachricht verarbeitet.

- **Recipient_Address**: die e-Mail-Adressen der Empfänger der Nachricht. Mehrere e-Mail-Adressen werden durch das Semikolon (;) voneinander getrennt.

- **Recipient_count**: die Gesamtzahl der Empfänger der Nachricht.

- **Related_recipient_address**: verwendet mit `EXPAND`, `REDIRECT`, und `RESOLVE` Ereignisse an anderen Empfänger e-Mail-Adressen, die der Meldung zugeordnet sind.

- **Referenz**: Dieses Feld enthält zusätzliche Informationen für bestimmte Arten von Ereignissen. Zum Beispiel:

   - **DSN**: enthält den Berichtshyperlink, der den Wert **Message_id** zugeordneten Übermittlungsstatus (auch bekannt als ein DSN, -non-Delivery Report, NDR oder Unzustellbarkeitsnachricht) ist ein DSN nach diesem Ereignis generiert wird. Ist dies eine DSN-Meldung, enthält dieses Feld den Wert **Message_id** der ursprünglichen Nachricht, der für der DSN generiert wurde.

   - **Erweitern**: enthält den **Related_recipient_address** -Wert, der die verwandten Nachrichten.

   - **Empfangen**: kann den Wert **Message_id** zugehörige Nachrichten enthalten, wenn die Nachricht durch andere Prozesse (beispielsweise Posteingangsregeln) generiert wurde.

   - **Senden**: enthält den Wert **Internal_message_id** alle DSN-Nachrichten.

   - **Übertragen**: enthält den **Internal_message_id** -Wert, der die Nachricht, die (beispielsweise durch inhaltskonvertierung, empfängerbeschränkungen oder Agents) verzweigt wird, ist.

   - **MAILBOXRULE**: enthält den **Internal_message_id** -Wert, der die eingehende Nachricht, die Posteingangsregel an, die ausgehende Nachricht generieren verursacht.

   Für andere Ereignistypen ist dieses Feld zumeist leer.

- **Return_path**: die Rückgabe e-Mail-Adresse angegeben, die vom Befehl **MAIL FROM** , die die Nachricht gesendet. Obwohl dieses Feld nicht leer ist, kann es der null-Absender Adresswert dargestellt als haben `<>`.

- **Message_info**: Weitere Informationen zur Nachricht. Zum Beispiel:

   - Nachricht Aufnahme Datum und Uhrzeit in UTC für `DELIVER` und `SEND` Ereignisse. Die Aufnahme Datum-Zeit ist die Zeit, wenn die Meldung auf die Exchange Online-Organisation eingegeben. Die UTC-Datum-Uhrzeit im ISO 8601-Datum-Uhrzeit-Format dargestellt ist: `yyyy-mm-ddThh:mm:ss.fffZ`, wobei `yyyy` = Jahr, `mm` = Monat, `dd` = Tag, `T` gibt den Anfang des die Zeitkomponente `hh` = Stunde, `mm` = Minute, `ss` = zweiter, `fff` Bruchteile einer Sekunde = und `Z` bedeutet `Zulu`, die eine andere Möglichkeit zum Kennzeichnen von UTC ist.

   - Authentifizierungsfehler. Beispielsweise können Sie den Wert finden Sie `11a` und die Art der Authentifizierung, die beim Auftreten des Authentifizierungsfehlers verwendet wurde.

- **Tenant_id**: ein GUID-Wert, die Exchange Online-Organisation darstellt (z. B. `39238e87-b5ab-4ef6-a559-af54c6b07b42`).

- **Original_server_ip**: die IP-Adresse des ursprünglichen Servers.

- **Custom_data**: Daten im Zusammenhang mit bestimmten Ereignistypen enthält. Weitere Informationen finden Sie unter den folgenden Abschnitten.

#### <a name="customdata-values"></a>Custom_data Werte

Das Feld **Custom_data** für eine `AGENTINFO` Ereignis wird von einer Vielzahl von Exchange Online-Agents verwendet, um die Verarbeitung von Nachrichten Details zu protokollieren. Einige weitere interessante Agents werden in den folgenden Abschnitten beschrieben.

#### <a name="spam-filter-agent"></a>Spam-Filter-agent

Ein **Custom_data** -Wert, der mit beginnt `S:SFA` hat ihren Ursprung der Spam-Filter-Agent. In der folgenden Tabelle werden die wichtigsten Informationen beschrieben:

|**Wert**|**Beschreibung**|
|:-----|:-----|
|`SFV=NSPM`|Die Nachricht wurde als "Nicht-Spam" markiert und an die vorgesehenen Empfänger gesendet.|
|`SFV=SPM`|Die Nachricht wurde vom Inhaltsfilter als Spam markiert.|
|`SFV=BLK`|Die Filterung wurde übergangen, und die Nachricht wurde gesperrt, da sie von einem gesperrten Absender stammt.|
|`SFV=SKS`|Die Nachricht wurde bereits als Spam markiert, noch bevor sie vom Inhaltsfilter verarbeitet wurde. Dies beinhaltet Nachrichten, bei denen die Nachricht einer Transportregel entsprach, die diese automatisch als Spam markiert und alle zusätzlichen Filterungen umgeht.|
|`SCL=<number>`|Weitere Informationen zu den verschiedenen SCL-Werten und deren Bedeutung finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](https://technet.microsoft.com/library/jj200686.aspx).|
|`PCL=<number>`|Der PCL-Wert (Phishing Confidence Level) der Nachricht. Diese Werte können auf die gleiche Weise interpretiert werden wie die in [SCL-Bewertungen (Spam Confidence Level)](https://technet.microsoft.com/library/jj200686.aspx) dokumentierten SCL-Werte.  |
|`DI=SB`|Der Absender der Nachricht wurde blockiert.|
|`DI=SQ`|Die Nachricht wurde unter Quarantäne gestellt.|
|`DI=SD`|Die Nachricht wurde gelöscht.|
|`DI=SJ`|Die Nachricht wurde an den Ordner "Junk-E-Mail" des Empfängers gesendet.|
|`DI=SN`|Die Nachricht wurde über den höheren Risk Delivery Pool weitergeleitet. Weitere Informationen finden Sie unter [hohem Delivery Pool für ausgehende Nachrichten](https://technet.microsoft.com/library/jj200746.aspx).|
|`DI=SO`|Die Nachricht wurde durch den normalen Pool für ausgehende Zustellungen geleitet.|
|' Angewendet = [a]|Angewendet [b] ='|Dies bedeutet, dass Übereinstimmungen mit den Spam-Regeln gefunden wurden.|
|`IPV=CAL`|Die Nachricht wurde durch die Spam-Filter gelassen, weil die IP-Adrese in einer IP-Zulassungsliste im Verbindungsfilter angegeben wurde.|
|`H=<EHLOstring>`|Die HELO- oder EHLO-Zeichenfolge des verbindenden e-Mail-Servers.|
|`PTR=<ReverseDNS>`|Der PTR-Eintrag der IP-Adresse des Absenders, auch bekannt als Reverse-DNS-Adresse.|

Ein Beispiel für **Custom_data** einen Wert für eine Nachricht, die als Spam wie folgt ausgefiltert wird:

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a>Malware Filter-agent

Ein **Custom_data** -Wert, der mit beginnt `S:AMA` hat ihren Ursprung der Malware Filter-Agent. In der folgenden Tabelle werden die wichtigsten Informationen beschrieben:

|**Wert**|**Beschreibung**|
|:-----|:-----|
|' AMA = SUMME|v=1|` or `AMA=EV|V = 1'|Die Nachricht wurde auf Schadsoftware ermittelt. `SUM` gibt an, die Malware konnte von einer beliebigen Anzahl von Modulen erkannt wurden haben. `EV` gibt an, von einem bestimmten Modul wurde die Schadsoftware erkannt. Wenn Malware von einem Modul erkannt wird, dass dies die nachfolgenden Aktionen ausgelöst wird.|
|`Action=r`|Die Nachricht wurde ersetzt.|
|`Action=p`|Die Nachricht wurde umgangen.|
|`Action=d`|Die Nachricht wurde zurückgestellt.|
|`Action=s`|Die Nachricht wurde gelöscht.|
|`Action=st`|Die Nachricht wurde umgangen.|
|`Action=sy`|Die Nachricht wurde umgangen.|
|`Action=ni`|Die Nachricht wurde abgelehnt.|
|`Action=ne`|Die Nachricht wurde abgelehnt.|
|`Action=b`|Die Nachricht wurde blockiert.|
|`Name=<malware>`|Der Name der Schadsoftware, die gefunden wurde.|
|`File=<filename>`|Der Name der Datei, welche die Schadsoftware enthielt.|

Ein Beispiel für **Custom_data** einen Wert für eine Nachricht, die Schadsoftware enthält sieht folgendermaßen aus:

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a>Transportregel-agent

Ein **Custom_data** -Wert, der mit beginnt`S:TRA` hat ihren Ursprung der Transportregel-Agent für e-Mail-Flussregeln (auch als Transportregeln bezeichnet). In der folgenden Tabelle werden die wichtigsten Informationen beschrieben:

|**Wert**|**Beschreibung**|
|:-----|:-----|
|"ETR|Regel-ID =<guid>`|Die ID der Regel, die abgeglichen wurde.|
|`St=<datetime>`|Datum und Uhrzeit in UTC, wenn dem Abgleich ist aufgetreten.|
|`Action=<ActionDefinition>`|Die Aktion, die angewendet wurde. Eine Liste der verfügbaren Aktionen finden Sie unter [E-Mail-Fluss Regelaktionen in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).|
|`Mode=<Mode>`|Der Modus der Regel. Gültige Werte sind:<br/>• **Erzwingen**: alle Aktionen für die Regel werden erzwungen. <br/>• **Test mit Richtlinientipps:**: alle richtlinientippaktionen werden gesendet, aber andere zu erzwingende Aktionen werden nicht ausgeführt. <br/>• **Test ohne Richtlinientipps**: Aktionen werden in einer Protokolldatei aufgelistet, aber Absender werden keinerlei nicht benachrichtigt und erzwingende Aktionen werden nicht ausgeführt.|

Ein Beispiel **Custom_data** Wert für eine Nachrichten, der die Bedingungen eine e-Mail-Flussregel erfüllt sieht folgendermaßen aus:

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`
