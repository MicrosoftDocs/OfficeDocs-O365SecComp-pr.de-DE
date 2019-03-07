---
title: Nachrichtenablaufverfolgung im Security & Compliance Center
ms.author: chrisda
author: chrisda
manager: serdars
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 3e64f99d-ac33-4aba-91c5-9cb4ca476803
description: Administratoren können die Nachrichtenablaufverfolgung im Security & Compliance Center verwenden, um herauszufinden, was mit Nachrichten passiert ist.
ms.openlocfilehash: 9c427328972fb9c8d64a2847368f5be022974744
ms.sourcegitcommit: 6aa82374eef09d2c1921f93bda3eabeeb28aadeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2019
ms.locfileid: "30455347"
---
# <a name="message-trace-in-the-security--compliance-center"></a>Nachrichtenablaufverfolgung im Security & Compliance Center

Die Nachrichtenablaufverfolgung im Security & Compliance Center befolgt e-Mail-Nachrichten, während Sie über Ihre Exchange Online-Organisation Reisen. Sie können ermitteln, ob eine Nachricht empfangen, abgelehnt, zurückgestellt oder vom Dienst übermittelt wurde. Außerdem werden die Aktionen der Nachricht gezeigt, bevor diese ihren finalen Status erreicht hat.

Die Nachrichtenablaufverfolgung im Security & Compliance Center verbessert die Nachrichtenablaufverfolgung, die im Exchange Admin Center (EAC) verfügbar war. Sie können die Informationen aus der Nachrichtenablaufverfolgung verwenden, um Benutzer Fragen zu ihren Nachrichten zu beantworten, Probleme mit dem Nachrichtenfluss zu beheben und Richtlinienänderungen zu überprüfen.

## <a name="open-message-trace"></a>Nachrichtenablaufverfolgung öffnen

1. [Melden Sie sich bei Office 365](https://support.office.com/article/e9eb7d51-5430-4929-91ab-6157c5a050b4) mit Ihrem Firmen- oder Schulkonto an.

2. Wählen Sie das Symbol für das App-Startfeld ![Symbol für Office 365-App-Startfeld](media/0aaa6945-f9a4-4b13-bf5f-d5c5dbe978fb.png) in der oberen linken Ecke und dann **Administrator** aus.

3. Erweitern Sie in der unteren linken Navigationsleiste **Admin Center** , und wählen Sie **Security & Compliance**aus.

4. Erweitern Sie auf der Seite **Sicherheit &-Konformität** , die geöffnet wird, die Option Nachrichten **Fluss**, und wählen Sie dann **Meldungsablauf Verfolgung**aus.

## <a name="message-trace-page"></a>Seite "Nachrichtenablaufverfolgung"

Von hier aus können Sie eine neue Standardablaufverfolgung starten, indem Sie auf die Schaltfläche **Trace starten** klicken. Dadurch werden alle Nachrichten für alle Absender und Empfänger für die letzten zwei Tage gesucht. Sie können auch eine der gespeicherten Abfragen aus den verfügbaren Abfrage Kategorien verwenden und diese entweder wie folgt ausführen oder als Ausgangspunkt für eigene Abfragen verwenden:

- **Standardabfragen**: integrierte Abfragen, die von Office 365 bereitgestellt werden.

- **Benutzerdefinierte Abfragen**: von Administratoren in Ihrer Organisation gespeicherte Abfragen zur späteren Verwendung.

- **Autosaved Queries**: die letzten zehn zuletzt ausgeführten Abfragen. Diese Liste erleichtert die Abholung, wo Sie aufgehört haben.

Auch auf dieser Seite finden Sie einen Abschnitt zum **Herunterladen von Berichten** für die von Ihnen übermittelten Anforderungen sowie die Berichte selbst, wenn der Download verfügbar ist.

## <a name="options-for-a-new-message-trace"></a>Optionen für eine neue Nachrichtenablaufverfolgung

### <a name="filter-by-senders-and-recipients"></a>Filtern nach Absender und Empfänger

Die Standardwerte sind **alle Absender** und **alle Empfänger**, aber Sie können die folgenden Felder zum Filtern der Ergebnisse verwenden:

- **Von diesen Personen**: Klicken Sie in dieses Feld, um einen oder mehrere Absender aus Ihrer Organisation auszuwählen. Sie können auch beginnen, einen Namen einzugeben, und die Elemente in der Liste werden nach Ihren Eingaben gefiltert, ähnlich wie bei einer Such Seite.

- **Für diese Personen**: Klicken Sie in dieses Feld, um einen oder mehrere Empfänger in Ihrer Organisation auszuwählen.

Sie können auch die e-Mail-Adressen von externen Absendern und Empfängern eingeben. Platzhalter werden unterstützt`*@contoso.com` ( `scot?@contoso.com`oder), aber Sie können nicht gleichzeitig mehrere Platzhaltereinträge im gleichen Feld verwenden.

### <a name="time-range"></a>Zeitspanne

Der Standardwert beträgt **2 Tage**, Sie können jedoch Datums-und Zeitbereiche von bis zu 90 Tagen angeben. Berücksichtigen Sie bei der Verwendung von Datums-und Zeitbereichen folgende Probleme:

- Standardmäßig wählen Sie den Zeitintervall in der **Schiebe** Ansicht mit einer Zeitlinie aus. Sie können nur die angezeigten Tages-oder Uhrzeiteinstellungen auswählen. Wenn Sie versuchen, einen dazwischen liegenden Wert auszuwählen, wird die Start/End-Blase an die nächste angezeigte Einstellung ausgerichtet.

   ![Ein Slider-Zeitbereich in einer neuen Nachrichtenablaufverfolgung im Security & Compliance Center](media/55a9e9c1-f7d5-4047-b217-824e8b976bcb.png)

   Sie können jedoch auch zur **benutzerdefinierten** Ansicht wechseln, in der Sie die Werte für **Start Datum** und Enddatum (einschließlich Zeiten) angeben können, und Sie können **** auch die Zeitzone für den Datums-und Uhrzeitbereich auswählen. **** Beachten Sie, dass die **Zeit Zonen** Einstellung sowohl für die Abfrage Eingaben als auch für die Abfrageergebnisse gilt.

   ![Ein benutzerdefinierter Zeitbereich in einer neuen Nachrichtenablaufverfolgung im Security & Compliance Center](media/ed4c8d50-9ea5-4694-93f9-ee3ab6660b4f.png)

   Für maximal 10 Tage stehen die Ergebnisse sofort als Zusammenfassungsbericht zur **** Verfügung. Wenn Sie einen Zeitabstand angeben, der sogar etwas größer als 10 Tage ist, werden die Ergebnisse verzögert, da Sie nur als herunterladbare CSV-Datei ( **Erweiterte Zusammenfassung** oder **Erweiterte** Berichte) verfügbar sind.

   Weitere Informationen zu den verschiedenen Berichtstypen finden Sie im Abschnitt [berichtsTyp auswählen](#choose-report-type) in diesem Thema.

   **Hinweis**: erweiterte Zusammenfassung und erweiterte Berichte werden mit archivierten Nachrichtenablauf Verfolgungsdaten erstellt, und es kann bis zu mehreren Stunden dauern, bis der Bericht zum Download verfügbar ist. Je nachdem, wie viele andere Administratoren auch Berichtsanforderungen gleichzeitig übermittelt haben, wird möglicherweise auch eine Verzögerung festgestellt, bevor die Verarbeitung für die Warteschlangen Anforderung gestartet wird.

- Beim Speichern einer Abfrage **** in der Schiebe Ansicht wird der relative Zeitintervall (beispielsweise 3 Tage von heute) gespeichert. Beim Speichern einer Abfrage in einer **benutzerdefinierten** Ansicht wird der absolute Datum/Uhrzeit-Zeitraum (beispielsweise 2018-05-06 13:00 bis 2018-05-08 18:00) gespeichert.

### <a name="more-search-options"></a>Weitere Suchoptionen

#### <a name="delivery-status"></a>Zustellungsstatus

Sie können den Standardwert **alle** ausgewählt lassen, oder Sie können einen der folgenden Werte auswählen, um die Ergebnisse zu filtern:

- **Zustellung**: die Nachricht wurde erfolgreich an das vorgesehene Ziel übermittelt.

- **Pending**: die Übermittlung der Nachricht wird versucht oder erneut versucht.

- **Expanded**: ein Verteilergruppenempfänger wurde vor der Übergabe an die einzelnen Mitglieder der Gruppe erweitert.

- **Fehler**: die Nachricht wurde nicht zugestellt.

- **Isoliert**: die Nachricht wurde isoliert (als Spam, Massenmail oder Phishing). Weitere Informationen finden Sie unter [Isolieren von e-Mail-Nachrichten in Office 365](https://support.office.com/article/4c234874-015e-4768-8495-98fcccfc639b.aspx).

- **Gefiltert als Spam**: die Nachricht wurde als Spam identifiziert und wurde zurückgewiesen oder blockiert (nicht isoliert).

- **Status:** Die Nachricht wurde kürzlich von Office 365 empfangen, aber es sind noch keine anderen Statusdaten verfügbar. Checken Sie in wenigen Minuten.

**Hinweis**: die Werte **Ausstehend,** **isoliert**und **Filter als Spam** sind nur für Suchvorgänge kleiner als 10 Tage verfügbar. Außerdem kann es eine Verzögerung von 5 bis 10 Minuten zwischen dem tatsächlichen und dem gemeldeten Zustellungsstatus geben.

#### <a name="message-id"></a>Nachrichten-ID

Hierbei handelt es sich um die Internet Nachrichten-ID (auch als Client-ID bezeichnet), die im Nachrichtenkopf im Message **-ID:-** Kopfzeilenfeld gefunden wird. Benutzer können diesen Wert zur Untersuchung bestimmter Nachrichten angeben.

Dieser Wert ist für die Lebensdauer der Nachricht konstant. Bei Nachrichten, die in Office 365 oder Exchange erstellt wurden, hat der `<GUID@ServerFQDN>`Wert das Format, einschließlich der\< \>spitzen Klammern (). Beispiel: `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`. Andere Messagingsysteme verwenden möglicherweise unterschiedliche Syntax oder Werte. Dieser Wert soll eindeutig sein, aber nicht alle e-Mail-Systeme folgen genau dieser Anforderung. Wenn das **Message-ID:-** Kopfzeilenfeld für eingehende Nachrichten aus externen Quellen nicht vorhanden oder leer ist, wird ein beliebiger Wert zugewiesen.

Wenn Sie die nach **richten-ID** zum Filtern der Ergebnisse verwenden, achten Sie darauf, dass Sie die vollständige Zeichenfolge einschließlich aller eckigen Klammern einschließen.

#### <a name="direction"></a>Direction

Sie können den Standardwert **alle** ausgewählt lassen, oder Sie können **eingehende** (an Empfänger in Ihrer Organisation gesendete Nachrichten) oder **ausgehende** (Nachrichten, die von Benutzern in Ihrer Organisation gesendet werden) zum Filtern der Ergebnisse auswählen.

#### <a name="original-client-ip-address"></a>Ursprüngliche Client-IP-Adresse

Sie können die Ergebnisse nach Client-IP-Adresse einreichen, um gehackte Computer zu untersuchen, die große Mengen an Spam oder Schadsoftware senden. Obwohl die Nachrichten scheinbar von mehreren Absendern stammen, ist es wahrscheinlich, dass der gleiche Computer alle Nachrichten generiert.

**Hinweis**: die Client-IP-Adressinformationen sind nur 10 Tage lang verfügbar und stehen nur in den **erweiterten Zusammenfassungen** oder **erweiterten** Berichten (herunterladbare CSV-Dateien) zur Verfügung.

### <a name="choose-report-type"></a>Berichtstyp auswählen

Die verfügbaren Berichtstypen sind:

- **Zusammenfassung**: verfügbar, wenn der Zeitintervall kürzer als 10 Tage ist und keine zusätzlichen Filteroptionen erforderlich sind. Die Ergebnisse sind fast unmittelbar nach dem Klicken auf **Suche**verfügbar.

- **Erweiterte Zusammenfassung** oder **erweitert**: Diese Berichte sind nur als herunterladbare CSV-Dateien verfügbar und erfordern eine oder mehrere der folgenden Filteroptionen unabhängig vom Zeitintervall: **von diesen Personen** **zu diesen Personen**oder ** NachRichten-ID**. Sie können Platzhalter für Absender oder Empfänger verwenden (beispielsweise \*@contoso. com).

**Hinweise**:

- Erweiterte Zusammenfassung und erweiterte Berichte werden mit archivierten Nachrichtenablauf Verfolgungsdaten erstellt, und es kann bis zu mehreren Stunden dauern, bis der Bericht zum Herunterladen verfügbar ist. Je nachdem, wie viele andere Administratoren auch Berichtsanforderungen gleichzeitig übermittelt haben, wird möglicherweise auch eine Verzögerung festgestellt, bevor die Verarbeitung der Warteschlangen Anforderung beginnt.

- Während Sie eine erweiterte Zusammenfassung oder einen erweiterten Bericht für einen beliebigen Datum/Uhrzeit-Zeitraum auswählen können, sind die letzten vier Stunden archivierter Daten für diese beiden Berichtstypen noch nicht verfügbar.

Wenn Sie auf **weiter**klicken, wird eine Zusammenfassungsseite mit den ausgewählten Filteroptionen, einem eindeutigen (bearbeitbaren) Titel für den Bericht und der e-Mail-Adresse angezeigt, die die Benachrichtigung erhält, wenn die Nachrichtenablaufverfolgung abgeschlossen ist (auch bearbeitbar, und muss sich in einer der akzeptierten Domänen Ihrer Organisation befinden). Klicken Sie auf **Bericht vorbereiten** , um die Nachrichtenablaufverfolgung zu übermitteln. Auf der Hauptseite der **Nachrichtenablaufverfolgung** wird der Status des Berichts im Abschnitt **zum Herunterladen von Berichten** angezeigt.

Weitere Informationen zu den Informationen, die in den verschiedenen Berichtstypen zurückgegeben werden, finden Sie im nächsten Abschnitt.

## <a name="message-trace-results"></a>Ergebnisse der Nachrichtenablaufverfolgung

Die verschiedenen Berichtstypen geben unterschiedliche Informationsebenen zurück. Die in den verschiedenen Berichten verfügbaren Informationen werden in den folgenden Abschnitten beschrieben.

### <a name="summary-report-output"></a>Zusammenfassungsbericht Ausgabe

Nach dem Ausführen der Nachrichtenablaufverfolgung werden die Ergebnisse aufgelistet, sortiert nach absteigenden Datum/Uhrzeit (zuletzt zuerst).

![Zusammenfassungsbericht Ergebnisse für die Nachrichtenablaufverfolgung im Security & Compliance Center](media/0664bafe-0b03-477b-b571-0b046ac8c977.png)

Der Zusammenfassungsbericht enthält die folgenden Informationen:

- **Date**: das Datum und die Uhrzeit, zu der die Nachricht vom Dienst empfangen wurde, unter Verwendung der KONFIGURIERTen UTC-Zeitzone.

- **Absender**: die e-Mail-Adresse des Absenders (*Alias*@*Domäne*).

- **Empfänger**: die e-Mail-Adresse des Empfängers oder Empfängers. Für eine Nachricht, die an mehrere Empfänger gesendet wird, gibt es eine Leitung pro Empfänger. Wenn es sich bei dem Empfänger um eine Verteilergruppe, eine dynamische Verteilergruppe oder eine e-Mail-aktivierte Sicherheitsgruppe handelt, ist die Gruppe der erste Empfänger, und dann befindet sich jedes Mitglied der Gruppe in einer separaten Leitung.

- **Betreff**: die ersten 256 Zeichen des **Subject** -Felds der Nachricht.

- **Status**: diese Werte werden im Abschnitt Zustellungs [Status](#delivery-status) beschrieben.

Standardmäßig werden die ersten 250-Ergebnisse geladen und stehen sofort zur Verfügung. Wenn Sie nach unten scrollen, gibt es eine leichte Pause, wenn der nächste Ergebnis Batch geladen wird. Anstatt einen Bildlauf durchzuführen, können Sie auf **alle laden** klicken, um alle Ergebnisse auf maximal 10.000 zu laden.

Sie können auf die Spaltenüberschriften klicken, um die Ergebnisse nach den Werten in dieser Spalte in aufsteigender oder absteigender Reihenfolge zu sortieren.

Sie können auf **Ergebnisse filtern** klicken, um die Ergebnisse nach einer oder mehreren Spalten zu filtern.

Sie können die Ergebnisse exportieren, nachdem Sie eine oder mehrere Zeilen ausgewählt haben, indem Sie auf **Ergebnisse exportieren** und dann **alle Ergebnisse**exportieren, geladene **Ergebnisse exportieren**oder **ausgewählte**exportieren auswählen.

#### <a name="find-related-records-for-this-message"></a>Suchen nach verwandten Datensätzen für diese Nachricht

Verknüpfte Nachrichtendatensätze sind Datensätze, die dieselbe nachRichten-ID gemeinsam verwendet haben. Denken Sie daran, dass auch eine einzelne Nachricht, die zwischen zwei Personen gesendet wurde, mehrere Datensätze generieren kann. Die Anzahl der Datensätze wird erhöht, wenn die Nachricht von Verteilergruppenerweiterungen, Weiterleitung, Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) usw. beeinflusst wird.

Nachdem Sie das Kontrollkästchen einer Zeile ausgewählt haben, finden Sie verknüpfte Datensätze für die Nachricht, indem Sie auf die Schaltfläche **Verwandte Suchen** klicken, die angezeigt wird, oder indem Sie **Weitere Optionen** ![weitere](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Suche in Verbindung stehende Datensätze für diese Nachricht**auswählen.

Weitere Informationen zur nachRichten-ID finden Sie im Abschnitt nachRichten-ID weiter oben in diesem Thema.

#### <a name="message-trace-details"></a>Details der Nachrichtenablaufverfolgung

In der Ausgabe des Zusammenfassungsberichts können Sie Details zu einer Nachricht mit einer der folgenden Methoden anzeigen:

- Wählen Sie die Zeile aus (Klicken Sie an eine beliebige Stelle in der Zeile mit Ausnahme des Kontrollkästchens).

- Aktivieren Sie das Kontrollkästchen der Zeile, und klicken Sie auf **Weitere Optionen** ![mehr](media/1ea52bbf-9d00-48ce-9362-307f7f6fb7fe.png) \> **Ansichts Nachrichtendetails**.

   ![Details nach dem Doppelklicken auf eine Zeile in der Zusammenfassungsbericht-Nachrichtenablaufverfolgung Ergebnisse im Security & Compliance Center](media/e50ee7cd-810a-4c06-8b58-e56ffd7028d1.png)

Die Details der Nachrichtenablaufverfolgung enthalten die folgenden zusätzlichen Informationen, die im Zusammenfassungsbericht nicht vorhanden sind:

- **Nachrichten Ereignisse**: Dieser Abschnitt enthält Klassifikationen, mit denen die Aktionen kategorisiert werden, die der Dienst für Nachrichten ausführt. Einige der interessantesten Ereignisse, die auftreten können, sind:

   - **Receive**: die Nachricht wurde vom Dienst empfangen.

   - **Send**: die Nachricht wurde vom Dienst gesendet.

   - **Fehler**: die Nachricht konnte nicht zugestellt werden.

   - **Deliver**: die Nachricht wurde an ein Postfach zugestellt.

   - **Expand**: die Nachricht wurde an eine erweiterte Verteilergruppe gesendet.

   - **Übertragung**: Empfänger wurden aufgrund von Inhaltskonvertierung, Grenzwerten für Nachrichtenempfänger oder Agents zu einer gegabelten Nachricht verschoben.

   - **** Zurückstellen: die Nachrichtenübermittlung wurde verschoben und kann später erneut versucht werden.

   - **Behoben**: die Nachricht wurde an eine neue Empfängeradresse umgeleitet, die auf einer Active Directory-Suche basiert. Wenn dies geschieht, wird die ursprüngliche Empfängeradresse zusammen mit dem abschließenden Zustellungsstatus in der Nachrichtenablaufverfolgung einer separaten Zeile aufgeführt.

   Beachten Sie, dass auch eine ereignislose Nachricht, die erfolgreich übermittelt wird, mehrere **Ereignis** Einträge in der Nachrichtenablaufverfolgung generiert.

- **Weitere Informationen**: Dieser Abschnitt enthält die folgenden Details:

   - Nach **richten-ID**: dieser Wert wird im Abschnitt nach [richten-ID](#message-id) weiter oben in diesem Thema beschrieben. Beispiel: `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

   - **Nachrichtengröße**

   - **Von IP**: die IP-Adresse des Computers, von dem die Nachricht gesendet wurde. Für ausgehende Nachrichten, die von Exchange Online gesendet wurden, wird kein Wert angegeben.

   - **Zu IP**: die IP-Adresse oder die Adressen, an denen der Dienst versucht hat, die Nachricht zuzustellen. Wenn die Nachricht mehrere Empfänger hat, werden diese angezeigt. Für eingehende Nachrichten, die an Exchange Online gesendet wurden, wird kein Wert angegeben.

### <a name="enhanced-summary-reports"></a>Erweiterte Zusammenfassungsberichte

Verfügbare (abgeschlossene) erweiterte Zusammenfassungsberichte stehen im Abschnitt zum **Herunterladen von Berichten** am Anfang der Nachrichtenablaufverfolgung zur Verfügung. Die folgenden Informationen sind im Bericht verfügbar:

- **origin_timestamp**<sup>*</sup>: das Datum und die Uhrzeit, zu der die Nachricht anfänglich vom Dienst empfangen wurde, unter Verwendung der konfigurierten UTC-Zeitzone.

- **sender_address**: die e-Mail-Adresse des Absenders (*Alias*@*Domäne*).

- **Recipient_status**: der Status der Übermittlung der Nachricht an den Empfänger. Wenn die Nachricht an mehrere Empfänger gesendet wurde, werden alle Empfänger und der entsprechende Status für jeden im Format: \< *e-Mail-Adress*\>##\<*Status*\>angezeigt. Beispiel:

   - **# #Receive, Send,** dass die Nachricht vom Dienst empfangen und an das vorgesehene Ziel gesendet wurde.

   - **# #Receive, Fail,** dass die Nachricht vom Dienst empfangen wurde, aber die Zustellung an das vorgesehene Ziel fehlgeschlagen ist.

   - **# #Receive, Deliver** : die Nachricht wurde vom Dienst empfangen und an das Postfach des Empfängers übermittelt.

- **message_subject**: die ersten 256 Zeichen des **Betreff** -Felds der Nachricht.

- **total_bytes**: die Größe der Nachricht in Byte, einschließlich Anlagen.

- **message_id**: dieser Wert wird im Abschnitt nach [richten-ID](#message-id) weiter oben in diesem Thema beschrieben. Beispiel: `<d9683b4c-127b-413a-ae2e-fa7dfb32c69d@DM3NAM06BG401.Eop-nam06.prod.protection.outlook.com>`.

- **network_message_id**: ein eindeutiger Wert für die Nachrichten-ID, der für alle Kopien der Nachricht beibehalten wird, die aufgrund von Verzweigungs-oder Verteilergruppenerweiterungen erstellt werden können. Ein Beispielwert ist `1341ac7b13fb42ab4d4408cf7f55890f`.

- **original_client_ip**: die IP-Adresse des Absenders.

- **Direktionalität**: gibt an, ob die Nachricht eingehend (1) an Ihre Organisation gesendet wurde oder ob Sie ausgehend (2) von Ihrer Organisation gesendet wurde.

- **connector_id**: der Name des Quell-oder Ziel-Konnektors. Weitere Informationen zu Connectors in Exchange Online finden Sie unter [Configure Mail Flow using Connectors in Office 365](https://docs.microsoft.com/Exchange/mail-flow-best-practices/use-connectors-to-configure-mail-flow/use-connectors-to-configure-mail-flow).

- **delivery_priority**<sup>*</sup>: gibt an, ob die Nachricht mit **hoher**, **niedriger**oder **normaler** Priorität gesendet wurde.

<sup>*</sup>Diese Eigenschaften sind nur in erweiterten Zusammenfassungsberichten verfügbar.

### <a name="extended-reports"></a>Erweiterte Berichte

Verfügbare (abgeschlossene) Erweiterte Berichte stehen am Anfang der Nachrichtenablaufverfolgung im Abschnitt zum **Herunterladen von Berichten** zur Verfügung. Praktisch alle Informationen aus einem erweiterten Zusammenfassungsbericht stehen in einem erweiterten Bericht (mit Ausnahme von **origin_timestamp** und **delivery_priority**) zur Verfügung. Die folgenden zusätzlichen Informationen stehen nur in einem erweiterten Bericht zur Verfügung:

- **client_ip**: die IP-Adresse des e-Mail-Servers oder Messaging-Clients, der die Nachricht übermittelt hat.

- **client_hostname**: der Hostname oder FQDN des e-Mail-Servers oder des Messagingclients, der die Nachricht übermittelt hat.

- **server_ip**: die IP-Adresse des Quell-oder Zielservers.

- **server_hostname**: der Hostname oder FQDN des Zielservers.

- **source_context**: zusätzliche Informationen, die dem **Quellfeld** zugeordnet sind. Beispiel:

   - `Protocol Filter Agent`

   - `3489061114359050000`

- **Quelle**: die Exchange Online-Komponente, die für das Ereignis zuständig ist. Beispiel:

   - `AGENT`

   - `MAILBOXRULE`

   - `SMTP`

- **event_id**: Diese entsprechen den **Nachrichtenereignis** Werten, die im Abschnitt [verwandte Datensätze für diese Nachricht suchen](#find-related-records-for-this-message) erläutert werden.

- **internal_message_id**: eine Nachrichten-ID, die vom Exchange Online-Server zugewiesen wird, der die Nachricht derzeit verarbeitet.

- **recipient_address**: die e-Mail-Adressen der Empfänger der Nachricht. Mehrere E-Mail-Adressen sind durch ein Semikolon (;) getrennt.

- **recipient_count**: die Gesamtzahl der Empfänger in der Nachricht.

- **related_recipient_address**: wird mit `EXPAND`, `REDIRECT`und `RESOLVE` Ereignissen verwendet, um andere Empfänger-e-Mail-Adressen anzuzeigen, die der Nachricht zugeordnet sind.

- **Referenz**: Dieses Feld enthält zusätzliche Informationen für bestimmte Ereignistypen. Beispiel:

   - **DSN**: enthält den Bericht Link, bei dem es sich um den **message_id** -Wert der zugehörigen Benachrichtigung über den Zustellungsstatus (auch als DSN, Unzustellbarkeitsbericht, NDR oder Bounce-Nachricht bezeichnet) handelt, wenn nach diesem Ereignis ein DSN generiert wird. Wenn es sich um eine DSN-Nachricht handelt, enthält dieses Feld den **message_id** -Wert der ursprünglichen Nachricht, für die der DSN generiert wurde.

   - **Expand**: enthält den **related_recipient_address** -Wert der zugehörigen Nachrichten.

   - **Receive**: kann den **message_id** -Wert der zugehörigen Nachricht enthalten, wenn die Nachricht von anderen Prozessen generiert wurde (beispielsweise Posteingangsregeln).

   - **Send**: enthält den **internal_message_id** -Wert aller DSN-Nachrichten.

   - **Transfer**: enthält den **internal_message_id** -Wert der Nachricht, die verzweigt wird (beispielsweisedurch Inhaltskonvertierung, Limits für Nachrichtenempfänger oder Agents).

   - **MAILBOXRULE**: enthält den **internal_message_id** -Wert der eingehenden Nachricht, die dazu geführt hat, dass die Posteingangsregel die ausgehende Nachricht generiert hat.

   Für andere Ereignistypen ist dieses Feld zumeist leer.

- **return_path**: die Absender-e-Mail-Adresse, die vom Befehl **Mail from** angegeben wurde, der die Nachricht gesendet hat. Obwohl dieses Feld nie leer ist, kann es den Wert der NULL-Absenderadresse haben `<>`, der als angegeben wird.

- **message_info**: zusätzliche Informationen zur Nachricht. Beispiel:

   - Die Datum-Uhrzeit der Nachrichtenerstellung in UTC für `DELIVER` und `SEND` Ereignisse. Die Datum-Uhrzeit der Entstehung ist der Zeitpunkt, zu dem die Nachricht zuerst in die Exchange Online-Organisation eingegeben wurde. Die UTC-Datums-und-Uhrzeit wird im ISO 8601 Date-Time- `yyyy-mm-ddThh:mm:ss.fffZ`Format dargestellt `yyyy` :, where `mm` = Year, `dd` = month, `T` = Day, gibt den Anfang der Zeit `hh` Komponente an, `mm` = Stunde, `ss` = Minute, `fff` = Sekunde, = Brüche einer Sekunde und `Z` gibt an `Zulu`, was eine andere Möglichkeit zum bezeichnen der UTC ist.

   - Authentifizierungsfehler. Möglicherweise wird der Wert `11a` und der Authentifizierungstyp angezeigt, der beim Auftreten des Authentifizierungsfehlers verwendet wurde.

- **tenant_id**: ein GUID-Wert, der die Exchange Online-Organisation darstellt ( `39238e87-b5ab-4ef6-a559-af54c6b07b42`beispielsweise).

- **original_server_ip**: die IP-Adresse des ursprünglichen Servers.

- **custom_data**: enthält Daten zu bestimmten Ereignistypen. Weitere Informationen finden Sie in den folgenden Abschnitten.

#### <a name="customdata-values"></a>custom_data-Werte

Das **Custom_data** -Feld für `AGENTINFO` ein Ereignis wird von einer Vielzahl von Exchange Online-Agents verwendet, um Details zur Nachrichtenverarbeitung zu protokollieren. Einige der interessantesten Agents werden in den folgenden Abschnitten beschrieben.

#### <a name="spam-filter-agent"></a>Spam Filter-Agent

Ein **custom_data** -Wert, der `S:SFA` mit beginnt, stammt vom Spamfilter-Agent. Die wichtigsten Details werden in der folgenden Tabelle beschrieben:

|**Wert**|**Beschreibung**|
|:-----|:-----|
|`SFV=NSPM`|Die Nachricht wurde als "Nicht-Spam" markiert und an die vorgesehenen Empfänger gesendet.|
|`SFV=SPM`|Die Nachricht wurde vom Inhaltsfilter als Spam markiert.|
|`SFV=BLK`|Die Filterung wurde übergangen, und die Nachricht wurde gesperrt, da sie von einem gesperrten Absender stammt.|
|`SFV=SKS`|Die Nachricht wurde bereits als Spam markiert, noch bevor sie vom Inhaltsfilter verarbeitet wurde Dies beinhaltet Nachrichten, bei denen die Nachricht einer Transportregel entsprach, die diese automatisch als Spam markiert und alle zusätzlichen Filterungen umgeht.|
|`SCL=<number>`|Weitere Informationen zu den verschiedenen SCL-Werten und deren Bedeutung finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](https://technet.microsoft.com/library/jj200686.aspx).|
|`PCL=<number>`|Der PCL-Wert (Phishing Confidence Level) der Nachricht. Diese Werte können auf die gleiche Weise interpretiert werden wie die in [SCL-Bewertungen (Spam Confidence Level)](https://technet.microsoft.com/library/jj200686.aspx) dokumentierten SCL-Werte.  |
|`DI=SB`|Der Absender der Nachricht wurde blockiert.|
|`DI=SQ`|Die Nachricht wurde unter Quarantäne gestellt.|
|`DI=SD`|Die Nachricht wurde gelöscht.|
|`DI=SJ`|Die Nachricht wurde an den Ordner "Junk-E-Mail" des Empfängers gesendet.|
|`DI=SN`|Die Nachricht wurde durch den Pool für besonders riskante Zustellungen geleitet. Weitere Informationen finden Sie unter [High-Risk-Übermittlungs Pool für ausgehende Nachrichten](https://technet.microsoft.com/library/jj200746.aspx).|
|`DI=SO`|Die Nachricht wurde durch den normalen Pool für ausgehende Zustellungen geleitet.|
|' SFS = [a]|SFS = [b] '|Dies bedeutet, dass Übereinstimmungen mit den Spam-Regeln gefunden wurden.|
|`IPV=CAL`|Die Nachricht wurde durch die Spam-Filter gelassen weil die IP-Adrese in einer IP-Zulassungsliste im Verbindungsfilter angegeben wurde.|
|`H=<EHLOstring>`|Die HELO-oder EHLO-Zeichenfolge des verbundenen e-Mail-Servers.|
|`PTR=<ReverseDNS>`|Der PTR-Eintrag der IP-Adresse des Absenders, auch bekannt als Reverse-DNS-Adresse.|

Ein Beispiel für einen **custom_data** -Wert für eine Nachricht, die wie folgt gefiltert wird:

`S:SFA=SUM|SFV=SPM|IPV=CAL|SRV=BULK|SFS=470454002|SFS=349001|SCL=9|SCORE=-1|LIST=0|DI=SN|RD=ftmail.inc.com|H=ftmail.inc.com|CIP=98.129.140.74|SFP=1501|ASF=1|CTRY=US|CLTCTRY=|LANG=en|LAT=287|LAT=260|LAT=18;`

#### <a name="malware-filter-agent"></a>Malware Filter-Agent

Ein **custom_data** -Wert, der `S:AMA` mit beginnt, stammt vom Malware Filter-Agent. Die wichtigsten Details werden in der folgenden Tabelle beschrieben:

|**Wert**|**Beschreibung**|
|:-----|:-----|
|' AMA = Summe|v=1|` or `AMA=EV|v = 1 '|Die Nachricht enthält Schadsoftware. `SUM`Gibt an, dass die Schadsoftware von einer beliebigen Anzahl von Modulen erkannt wurde. `EV`Gibt an, dass die Schadsoftware von einem bestimmten Modul erkannt wurde. Wenn von einem Modul Schadsoftware erkannt wird, werden dadurch die nachfolgenden Aktionen ausgelöst.|
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

Ein Beispiel für einen **custom_data** -Wert für eine Nachricht mit Schadsoftware sieht wie folgt aus:

`S:AMA=SUM|v=1|action=b|error=|atch=1;S:AMA=EV|engine=M|v=1|sig=1.155.974.0|name=DOS/Test_File|file=filename;S:AMA=EV|engine=A|v=1|sig=201707282038|name=Test_File|file=filename`

#### <a name="transport-rule-agent"></a>Transport Regel-Agent

Ein **custom_data** -Wert, der`S:TRA` mit beginnt, stammt aus dem Transportregel-Agent für Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet). Die wichtigsten Details werden in der folgenden Tabelle beschrieben:

|**Wert**|**Beschreibung**|
|:-----|:-----|
|' ETR|Regel-Nr. =<guid>`|Die ID der Regel, die abgeglichen wurde.|
|`St=<datetime>`|Das Datum und die Uhrzeit in UTC, als die Regelübereinstimmung aufgetreten ist.|
|`Action=<ActionDefinition>`|Die Aktion, die angewendet wurde. Eine Liste der verfügbaren Aktionen finden Sie unter [Aktionen für Nachrichtenfluss Regeln in Exchange Online](https://technet.microsoft.com/library/jj919237.aspx).|
|`Mode=<Mode>`|Der Modus der Regel. UserMailbox <br/>• **Erzwingen**: alle Aktionen für die Regel werden erzwungen. <br/>• **Test mit Richtlinien Tipps:**: alle richtlinientipp Aktionen werden gesendet, aber andere Durchsetzungs Aktionen werden nicht ausgeführt. <br/>• **Test ohne Richtlinien Tipps**: Aktionen werden in einer Protokolldatei aufgelistet, aber die Absender werden nicht benachrichtigt, und es werden keine Durchsetzungs Aktionen ausgeführt.|

Ein Beispiel für einen **custom_data** -Wert für eine Nachricht, die den Bedingungen einer Nachrichtenfluss Regel entspricht, sieht wie folgt aus:

`S:TRA=ETR|ruleId=19a25eb2-3e43-4896-ad9e-47b6c359779d|st=7/17/2017 12:31:25 AM|action=ApplyHtmlDisclaimer|sev=1|mode=Enforce`
