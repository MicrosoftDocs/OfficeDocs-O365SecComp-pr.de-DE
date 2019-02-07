---
title: Aufsichtsrichtlinien in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Grundlegendes zu aufsichtsrichtlinien in Office 365
ms.openlocfilehash: c66ded719791c4a5ecaaa459f81d0a0d4a3db924
ms.sourcegitcommit: e4d56cab6bbb77404457d506d17f6a7577f302be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/06/2019
ms.locfileid: "29760077"
---
# <a name="supervision-policies-in-office-365"></a>Aufsichtsrichtlinien in Office 365

Aufsichtsrichtlinien in Office 365 ermöglichen die Kommunikation der Mitarbeiter zur Prüfung durch festgelegten Bearbeiter erfassen. Sie können bestimmte Richtlinien definieren, die interne und externe e-Mail, Microsoft-Teams oder 3rd Party Communications in Ihrer Organisation zu erfassen. Bearbeiter können dann überprüfen Sie die Nachrichten aus, um sicherzustellen, dass sie mit Ihrer Organisation Nachricht Standards kompatibel sind und beheben Sie diese mit Klassifizierungstyp. Diese Richtlinien können Sie viele moderne Compliance-Lösung, einschließlich einer steigenden Typen der Kommunikationskanäle, erhöhen die Lautstärke des Meldungsdaten und behördlichen Erzwingung & das Risiko von Bußgelder Überwachung dieses Problems auch helfen.

In einigen Organisationen möglicherweise eine Trennung von Aufgaben zwischen IT-Support und der Gruppe Compliance Management. Office 365 unterstützt die Trennung zwischen den Mandanten mit Aufsicht Richtlinienfeatures Support und die Konfiguration von Richtlinien konfigurieren und reagieren auf aufgezeichneten Communications. Die IT-Abteilung für eine Organisation möglicherweise beispielsweise verantwortlich für das Einrichten von Berechtigungen für Rollen und Gruppen aufsichtsrichtlinien unterstützen, die konfiguriert und von der Organisation Compliance-Team verwaltet werden.

## <a name="scenarios-for-supervision-policies"></a>Szenarien für aufsichtsrichtlinien

Aufsichtsrichtlinien können monitoring Communications in Ihrer Organisation in unterschiedlichen Bereichen unterstützen:

- **Unternehmensrichtlinien**

    Akzeptable verwenden, ethische Standards und andere Unternehmensrichtlinien in ihre geschäftliche Kommunikation müssen Mitarbeiter entsprechen. Aufsichtsrichtlinien können Verstöße erkennen und Ihnen bei der Maßnahmen zum Verringern dieser Arten von Vorfälle übernehmen. Beispielsweise könnten Sie Ihre Organisation für potenzielle Personalabteilung Verstöße wie Belästigung oder die Verwendung von ungeeignetes oder anstößige Sprache in Mitarbeiter Communications überwachen.

- **Risikomanagement**

    Organisationen sind zuständig, um die gesamte Kommunikation über ihre Infrastruktur und Systemen Unternehmensnetzwerk verteilt. Aufsichtsrichtlinien zum Identifizieren und verwalten potenzielle rechtliche Folgen und des Risikomanagements mit hilft bei Risiken minimieren, bevor Vorgänge im Unternehmen beschädigt werden kann. Beispielsweise könnten Sie Ihre Organisation für unbefugte Kommunikation für vertrauliche Projekte wie anstehende Übernahmen, Fusionen, Einnahmen Angaben, Reorganisationen oder führende Team Änderungen überwachen.

- **Einhaltung von Vorschriften**

    Die meisten Organisationen müssen einige Typ der Einhaltung von Vorschriften Standards im Rahmen ihrer normalen Betrieb Verfahren entsprechen. Diese Auflagen erfordern häufig Organisationen eine Art von generelle implementieren oder Aufsicht Prozess für messaging, die für ihre Branche geeignet ist. Die finanziellen Branche behördlichen Autorität (FINRA) Regel 3110 ist ein gutes Beispiel für eine Anforderung für Organisationen verfügen generelle Prozeduren direkt zum Überwachen der Aktivitäten der Mitarbeiter und die Typen von Unternehmen es abwickelt. Ein weiteres Beispiel möglicherweise Bedarf für Broker-Händler in Ihrer Organisation zum Schutz gegen mögliche Geldwäsche, bezüglich Insider, Absprache oder Bestechung Aktivitäten zu überwachen. Aufsichtsrichtlinien können Ihre Organisation diese Anforderungen erfüllen, durch die Bereitstellung eines Prozesses zum Überwachen und Unternehmenskommunikation-Bericht helfen.

## <a name="feature-components"></a>Featurekomponenten

### <a name="supervision-policy"></a>Aufsichtsrichtlinie

Aufsichtsrichtlinien erstellen Sie in der & Security Compliance Center. Diese Richtlinien definieren, welche Communications und Benutzer in Ihrer Organisation überprüft werden, definieren Sie benutzerdefinierte Bedingung, dass die Kommunikation erfüllen müssen, und gibt an, die überprüft werden soll. Benutzer in die generelle Überprüfung Rollengruppe einrichten kann Richtlinien und jeder Benutzer, der diese Rolle zugewiesen wurde, können die Seite Überwachung unter Steuerung der Daten in der Office 365-Sicherheit & Compliance Center zugreifen.

### <a name="supervised-users"></a>Überwachten Benutzer

Bevor Sie beginnen, Überwachung verwenden, müssen Sie bestimmen, wer ihre Kommunikation überprüft haben. Verwenden Sie die e-Mail-Adressen in der Richtlinie zum Identifizieren von Personen oder Gruppen von Personen zu überwachen. Einige Beispiele für diese Gruppen sind Gruppen von Office 365, Exchange-basierten Verteilerlisten und Microsoft-Teams, Kanäle. Sie können auch bestimmte Benutzer oder Gruppen ausschließen, Überwachung, die innerhalb einer überwachten Gruppe oder eine Liste von Gruppen enthalten sind.

> [!IMPORTANT]
> Alle Benutzer von aufsichtsrichtlinien überwacht werden, müssen eine Office 365 Enterprise E3 Lizenz mit dem Add-on erweiterte Compliance oder in einem Office 365 Enterprise E5-Abonnement enthalten sein. Wenn Sie keinen vorhandenen Enterprise-E5 Plan haben und Überwachung ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).

### <a name="reviewers"></a>Bearbeiter

Wenn Sie eine Richtlinie für Überwachung erstellen, ermitteln Sie auch, wem die Überprüfung der Nachrichten der überwachten Benutzer ausgeführt werden soll. In der Richtlinie verwenden Sie die e-Mail-Adressen zum Identifizieren von Personen oder Gruppen von Personen zu einer überwachten durchstellung Communications überprüfen.

### <a name="groups-for-supervised-users-and-reviewers"></a>Gruppen für überwachten Benutzer und Bearbeiter

Um das Setup zu vereinfachen, Erstellen von Gruppen für Personen, die ihre Kommunikation überprüft haben, werden und Gruppen für Personen, die diese Kommunikation überprüft werden. Wenn Sie Gruppen verwenden, benötigen Sie möglicherweise mehrere. Angenommen, wenn Sie die Kommunikation zwischen zwei unterschiedlichen Gruppen von Personen überwachen möchten, oder wenn Sie möchten, um eine Gruppe anzugeben, die überwacht werden und sollte nicht zur Verfügung.

### <a name="supported-communication-types"></a>Unterstützte Kommunikationstypen

Mit aufsichtsrichtlinien können Sie Nachrichten in einem oder mehreren der folgenden Kommunikation Plattformen überwachen:

- **Exchange-e-Mail:** Postfächer, die als Teil Ihres Office 365-Abonnements auf Exchange Online gehostet werden sind alle für die Nachricht Überwachung. -E-Mails und Anlagen Drahtloszugriff Aufsicht sind für die Überwachung und Berichte Aufsicht sofort verfügbar. Anlagen in unterstützten Typen für Überwachung stimmen die [Dateitypen für Exchange Mail Flow Regel Content Kontrollen unterstützt](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection).
- **Microsoft-Teams:** Chat Communications und der zugeordneten Anlagen in öffentlichen und privaten Microsoft-Teams, Kanäle und einzelne Chats können überwacht werden. Teams Chats Aufsicht Drahtloszugriff Übereinstimmung einmal alle 24 Stunden verarbeitet werden und klicken Sie dann stehen für die Überwachung und in Berichten Überwachung.
- **Drittanbieter-Quellen:** Sie können Communications von Drittanbieter-Quellen (wie von Facebook oder Ablage) überwacht, wenn Sie diese Daten in Office 365-Postfächer in Ihrer Organisation importiert haben. [Informationen zum Importieren von Daten in Office 365 3rd Party](https://docs.microsoft.com/office365/securitycompliance/archiving-third-party-data).

### <a name="policy-settings"></a>Richtlinieneinstellungen

#### <a name="direction"></a>Direction

Standardmäßig wird die Bedingung **Richtung ist** wird angezeigt und kann nicht entfernt werden. Richtung für die Netzwerkkommunikation in einer Richtlinie können einzeln oder zusammen ausgewählt werden:

- **Eingehend** - Sie können **eingehende** Kommunikation zu überprüfen, die **an** gesendet werden die Personen, die Sie ausgewählt, zur Überwachung **von** Personen haben in der Richtlinie nicht enthalten.
- **Ausgehend** - **ausgehend** u. wenn Communications zu überprüfen, die die Personen, die Sie ausgewählt haben, **um** Personen über innehaben nicht, in der Richtlinie enthalten **aus** gesendet werden soll.
- **Internal** - u. **intern** , um zu prüfen, die gesendet werden, **zwischen** identifizierten Personen in der Richtlinie.

#### <a name="sensitive-information-types"></a>Typen vertraulicher Informationen

Sie haben die Möglichkeit, einschließlich der Typen vertraulicher Informationen als Teil Ihrer aufsichtsrichtlinie. Typen vertraulicher Informationen sind entweder vordefinierten oder benutzerdefinierten Datentypen, die identifizieren und schützen Sie Kreditkarte Zahlen, Bankkonto Zahlen, Ausweisnummern und helfen kann. Als Bestandteil von Office 365 [Verhinderung von Datenverlust (DLP)](data-loss-prevention-policies.md)kann die Konfiguration von vertraulichen Informationen Muster, Character Nähe, Confidence Levels und sogar benutzerdefinierte Datentypen zum Identifizieren und kennzeichnen, die möglicherweise vertrauliche Inhalte nutzen. Die Standardtypen vertrauliche Informationen sind:

- Finanzielle
- Medizinische und Integritätsdatenerfassung
- Datenschutz
- Benutzerdefinierte Informationen-Typ

Weitere Informationen zu vertrauliche Informationen und die Muster in die Standardtypen enthalten finden, finden Sie unter [welche Arten von vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).

#### <a name="custom-keyword-dictionaries"></a>Schlüsselwort für benutzerdefinierte Wörterbücher

Konfigurieren benutzerdefinierte Schlüsselwortsuche Wörterbücher (oder Lexika) können einfache Verwaltung von Schlüsselwörtern, die speziell für Ihre Organisation oder aus dem Gesundheitswesen enthalten und kann bis zu 100.000 Begriffe pro Wörterbuch unterstützen. Bei Bedarf können Sie mehrere benutzerdefinierte Schlüsselwortsuche Wörterbücher auf eine einzelne Richtlinie anwenden oder ein einzelnes Schlüsselwort Wörterbuch pro Richtlinie haben. Diese Wörterbücher sind in einer Richtlinie für Überwachung zugewiesen und können als Quelle stammen aus einer Datei (beispielsweise eine Liste CSV- oder TXT) oder aus einer Liste können Sie [direkt in einem PowerShell-Cmdlet eingeben](create-a-keyword-dictionary.md).

#### <a name="conditional-settings"></a>Bedingte Einstellungen

Die Bedingungen für die Richtlinie gewählte werden für die Kommunikation von e-Mails und 3rd Party Quellen in Ihrer Organisation (wie von Facebook oder Ablage) gelten.

Die folgende Tabelle erläutert mehr zu jeder Bedingung.
  
|**Bedingung**|**Verwendung**|
|:-----|:-----|
|Nachricht ist von diesen Domänen empfangen.  <br><br> Nachricht wird aus diesen Domänen nicht empfangen. | Um die Richtlinie anwenden, wenn bestimmte Domänen oder ausgeschlossen werden in einer empfangenen Nachricht, geben Sie jede Domäne, und trennen Sie mehrere Domänen durch ein Komma. Jede Domäne, die Sie eingeben, werden separat angewendet (nur eine dieser Domänen muss für die Richtlinie angewendet, die der Nachricht angewendet). |
|Nachricht wird an diesen Domänen gesendet.  <br><br> Nachricht wird an diesen Domänen nicht gesendet. | Um die Richtlinie anwenden, wenn bestimmte Domänen oder ausgeschlossen werden in eine gesendete Nachricht, geben Sie jede Domäne, und trennen Sie mehrere Domänen durch ein Komma. Jede Domäne, die Sie eingeben, werden separat angewendet (nur eine dieser Domänen muss für die Richtlinie angewendet, die der Nachricht angewendet). |
|Nachricht ist mit einem der folgenden Bezeichnungen klassifiziert.  <br><br> Nachricht wird nicht mit einem der folgenden Bezeichnungen klassifiziert. | Die Richtlinie anwenden, wenn bestimmte Aufbewahrung Etiketten ein- oder ausgeschlossen werden in einer Nachricht. Aufbewahrung Etiketten müssen separat konfiguriert werden und konfigurierte Etiketten im Rahmen dieser Bedingung ausgewählt werden können. Jede Etiketten separat angewendet werden (nur eine der folgenden Bezeichnungen muss für die Richtlinie angewendet, die der Nachricht anwenden). Weitere Informationen zum Konfigurieren von Beschriftungen Aufbewahrung finden Sie unter [Übersicht über die Aufbewahrung Beschriftungen](https://docs.microsoft.com/office365/securitycompliance/labels).|
|Nachricht enthält eines dieser Wörter  <br><br> Nachricht enthält keine der folgenden Wörter | Geben Sie zum Anwenden der Richtlinie, wenn bestimmte Wörter oder Ausdrücke ein- oder ausgeschlossen werden in einer Nachricht, einzelnen Wörter oder Ausdrücke in einer separaten Zeile ein. Jede Zeile der eingegebenen Wörter separat angewendet werden (nur eine der folgenden Zeilen muss für die Richtlinie angewendet, die der Nachricht angewendet). Weitere Informationen zum Eingeben von Wörtern oder Begriffen finden Sie im nächsten Abschnitt [übereinstimmende Wörter und Ausdrücke zum-e-Mails oder Anhänge](supervision-policies.md#Matchwords).|
|Anlage enthält eines dieser Wörter  <br><br> Anlage enthält keine der folgenden Wörter | Um die Richtlinie anwenden, wenn bestimmte Wörter oder Ausdrücke ein- oder ausgeschlossen werden in e-Mail-Anlagen (beispielsweise ein Word-Dokument), geben Sie jedes Wort oder Ausdruck in einer separaten Zeile ein. Jede Zeile der eingegebenen Wörter separat angewendet werden (nur eine Zeile gilt für die Richtlinie auf die Anlage angewendet). Weitere Informationen zum Eingeben von Wörtern oder Begriffen finden Sie im nächsten Abschnitt [übereinstimmende Wörter und Ausdrücke zum-e-Mails oder Anhänge](supervision-policies.md#Matchwords).|
|Anlage ist eine der folgenden Dateitypen  <br><br> Anlage ist keiner dieser Dateitypen | Um eine Kommunikation überwachen, die ein- oder ausschließen bestimmte Typen von Anlagen an, geben Sie die Dateierweiterungen (wie .exe oder PDF). Wenn Sie ein- oder Ausschließen von mehreren Dateierweiterungen möchten, geben Sie diese in separaten Zeilen. Nur eine Anlage-Erweiterung muss für die Richtlinie angewendet übereinstimmen.|
|Nachricht ist größer als  <br><br> Nachrichtengröße ist nicht größer als | Verwenden Sie diese Bedingungen-Mails basierend auf eine bestimmte Größe um zu überprüfen, um die maximale oder minimale Größe anzugeben, die eine Nachricht werden kann, bevor es überprüft wird. Beispielsweise, wenn Sie die **Nachrichtengröße ist größer als** angeben \> **1.0 MB**, alle Nachrichten, die 1.01 MB und größere wird sind hin überprüft werden. Sie können Bytes, KB, MB oder GB für diese Bedingung auswählen.|
|Anlage ist größer als  <br><br> Anlage ist nicht größer als | Um Nachrichten basierend auf deren Anlagengröße zu überprüfen, geben Sie die maximale oder minimale Größe einer Anlage kann sein, bevor Sie die Nachricht und ihre Anhänge unterliegen überprüfen. Wenn Sie die **Anlage ist größer als** angeben beispielsweise \> **2.0 MB**, alle Nachrichten mit Anlagen 2.01 MB und Failover wird überprüft. Sie können Bytes, KB, MB oder GB für diese Bedingung auswählen.|
   
##### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Übereinstimmende Wörter und Ausdrücke in E-Mails oder Anlagen
<a name="Matchwords"> </a>

Jede Zeile der eingegebenen Wörter separat angewendet werden (nur eine Zeile muss für die Richtlinie Bedingung auf das e-Mail- oder Anlage anwenden anwenden). Verwenden Sie die Bedingung, die **Nachricht enthält eines dieser Wörter**, mit den Schlüsselwörtern "Banker" und "Insider-Geschäften" beispielsweise fangen wir an in separaten Zeilen. Die Richtlinie gilt für alle Nachrichten, die das Wort "Banker" oder der Ausdruck "Insider-Geschäften" enthält. Nur eine der folgenden Wörter oder Ausdrücke muss für diese Richtlinie Bedingung anwenden auftreten. Wörter in die Nachricht oder Anlage müssen exakt übereinstimmen, was Sie eingeben.
  
##### <a name="entering-multiple-conditions"></a>Eingeben mehrerer Bedingungen

Wenn Sie mehrere Bedingungen eingeben, verwendet Office 365 aller Bedingungen um zu bestimmen, wann die Richtlinie auf Kommunikationselemente anwenden zusammen. Wenn Sie mehrere Bedingungen eingerichtet haben, müssen sie alle für die Richtlinie angewendet wurde, erfüllt sein, wenn Sie eine Ausnahme eingeben. Nehmen wir beispielsweise an, dass Sie eine Richtlinie erstellen, die angewendet werden soll, wenn eine Nachricht das Wort "Handel enthält" und größer als 2 MB ist müssen. Wenn die Nachricht auch die Wörter "Von Contoso finanzielle genehmigt enthält" sollten jedoch die Richtlinie nicht angewendet. In diesem Fall würde die drei Bedingungen folglich wie folgt lauten:
  
- **Nachricht enthält eines dieser Wörter**, mit den Schlüsselwörtern "Handel"

- **Nachrichtengröße ist größer als**, mit dem Wert von 2 MB

- **Nachricht enthält keine der folgenden Wörter**, mit den Schlüsselwörtern "Contoso finanzielle Teams genehmigt".

#### <a name="review-percentage"></a>Überprüfen der Prozentsatz

Sie können einen Prozentsatz der gesamten Kommunikation, die durch eine Richtlinie für Überwachung gesteuert wird, wenn Sie die Menge des Inhalts, um zu prüfen reduzieren möchten, angeben. Wir werden nach dem Zufallsprinzip, Umfang des Inhalts aus der Gesamtprozentsatz auswählen, die die Bedingungen entspricht, den, die Sie ausgewählt haben. Wenn Sie Bearbeiter alle Elemente überprüfen möchten, können Sie in einer Richtlinie für Überwachung **100 %** eingeben.

## <a name="monitoring--managing"></a>Verwalten von & Monitoring

Überwachung der Ergebnisse Ihrer Richtlinien für die Überwachung und Anwenden von einem Tag Lösung ist einfach und bequem. Sie können den Status der überprüften Elemente, die Benutzer und Gruppen unter Überwachung, und die Benutzer und Gruppen, die als Bearbeiter schnell sehen.

### <a name="supervision-policy-dashboard"></a>Überwachung Richtlinie dashboard

Die einfachste Möglichkeit zum Verwalten der Überwachung Gruppenrichtlinienergebnissen und zum Auflösen der ausstehenden Elemente ist die Verwendung das Überwachung Richtlinie Dashboard. Das Dashboard ermöglicht Bearbeiter schnell finden Artikel, die überprüft werden, Ausführen einer Aktion für ein Element, und überprüfen Sie die Ergebnisse von zuvor überprüft und Elemente für jede aufsichtsrichtlinie aufgelöst. Sie können das Überwachung Richtlinie Dashboard in der Office 365-Sicherheit & Compliance Center unter **Überwachung**zugreifen > *Your benutzerdefinierte Richtlinie* > **Öffnen**.

#### <a name="dashboard-home"></a>Dashboard-Startseite

Die **Startseite** Dashboardseite hat mehrere Abschnitte, die Sie schnell auf Ihre aufsichtsrichtlinien ergreifen unterstützen. Hier können Sie:

- Kurz die ausstehenden und aufgelöst Highlights für die Woche
- Anzeigen einer Liste der überwachten Benutzer und überwachten Gruppen für die ausgewählte Richtlinie
- Finden Sie eine Liste der Bearbeiter und überprüfen Teams für die ausgewählte Richtlinie
- Erfahren Sie, welche Plattformen Kommunikation Inhalte unter Überwachung für die Richtlinie ein.

#### <a name="supervise-tab"></a>Registerkarte Überwachung

Die Registerkarte **Supervise** wird, in dem Bearbeiter Ausführen einer Aktion und Elemente auflösen können durch die ausgewählte Richtlinie identifiziert. Hier können Sie:

- Ausstehende kompatible, nicht kompatible und fragwürdige Elemente filtern, indem Sie
- Markieren Sie ein einzelnes Element als kompatible, nicht kompatible oder fragwürdige. Sie können auch einen Kommentar mit dem Element, um zu verdeutlichen, dass die Kategorien ausgeführte Aktion aufzeichnen.
- Massen Markieren mehrerer Elemente als kompatible, nicht kompatible oder fragwürdige. Sie können auch einen Kommentar mit mehreren Elementen, um zu verdeutlichen, dass die Kategorien ausgeführte Aktion aufzeichnen.
- Anzeigen des Verlaufs von der Kategorien für ein einzelnes Element, einschließlich, die das Element, das Datum und Uhrzeit der die Aktion, die Lösung Tag und Kommentare enthalten aufgelöst.
- Klassifizieren Sie zuvor überprüfte Elemente als kompatible, nicht kompatible oder fragwürdige. Sie können auch einen Kommentar mit einzelne oder mehrere Elemente aus, um zu verdeutlichen, dass die erneute Klassifizierung Aktion aufzeichnen.

#### <a name="resolved-items-tab"></a>Registerkarte Elemente aufgelöst

Die Registerkarte **Elemente aufgelöst** wird, auf alle zuvor aufgelöst Elemente für die ausgewählte Richtlinie Bearbeiter angezeigt werden. Hier können Sie:

- Schnelles Anzeigen und den Betreff, Absender und Datum behoben Elemente sortieren.
- Anzeigen des Verlaufs Klassifizierung und Kommentar eines beliebigen ausgewählten Elements

### <a name="other-ways-to-review-items"></a>Weitere Methoden zum Lesen von Elementen

Wenn Bearbeiter nicht das Dashboard Überwachung in Office 365 verwenden möchten, müssen sie auch andere Optionen, um zu prüfen und Verwalten von aufsichtsrichtlinien erfassten Elemente.

#### <a name="outlook-on-the-web"></a>Outlook im Web

Benutzer, die als Bearbeiter in einer aufsichtsrichtlinie für Outlook im Web verwenden können, um zu prüfen und Überwachung Elementen behoben. Die Add-in-Überwachung wird automatisch in Outlook im Web für alle Bearbeiter installiert, die Sie in der Richtlinie angegeben. Ihre Organisation für die Überwachung Richtlinie freigegebene Ordner für konfigurierten Bearbeiter verfügbar sein soll ist keine zusätzliche Konfiguration erforderlich.

Verwenden von Outlook im Web, können Bearbeiter:

- Zeigen Sie gefilterte Elemente an, indem Sie kompatible, nicht kompatible, fragwürdige und aufgelöst status
- Markieren Sie ein einzelnes Element als kompatible, nicht kompatible, fragwürdige oder aufgelöst. Sie können auch einen Kommentar mit dem Element, um zu verdeutlichen, dass die Kategorien ausgeführte Aktion aufzeichnen.
- Anzeigen des Verlaufs von der Kategorien für ein einzelnes Element, einschließlich, die das Element, das Datum und Uhrzeit der die Aktion, die Lösung Tag und Kommentare enthalten aufgelöst.
- Klassifizieren Sie zuvor überprüfte Elemente als kompatible, nicht kompatible oder fragwürdige. Sie können auch einen Kommentar mit einzelner Elemente, um zu verdeutlichen, dass die erneute Klassifizierung Aktion aufzeichnen.

#### <a name="microsoft-outlook"></a>Microsoft Outlook

Um Communications identifiziert durch eine Richtlinie für die Überwachung zu überprüfen, können Bearbeiter auch des Aufsicht-add-Ins für Microsoft Outlook verwenden. Bearbeiter müssen jedoch über einige Schritte zur Installation in der Desktopversion von Outlook ausführen. Ausführliche Hilfestellungen zur Überwachung-add-in für Outlook installieren finden Sie unter [Configure aufsichtsrichtlinien](configure-supervision-policies.md).

Mit Outlook können Bearbeiter:

- Zeigen Sie gefilterte Elemente an, indem Sie kompatible, nicht kompatible, fragwürdige und aufgelöst status
- Markieren Sie ein einzelnes Element als kompatible, nicht kompatible, fragwürdige oder aufgelöst. Sie können auch einen Kommentar mit dem Element, um zu verdeutlichen, dass die Kategorien ausgeführte Aktion aufzeichnen.
- Anzeigen des Verlaufs von der Kategorien für ein einzelnes Element, einschließlich, die das Element, das Datum und Uhrzeit der die Aktion, die Lösung Tag und Kommentare enthalten aufgelöst.
- Klassifizieren Sie zuvor überprüfte Elemente als kompatible, nicht kompatible oder fragwürdige. Sie können auch einen Kommentar mit einzelner Elemente, um zu verdeutlichen, dass die erneute Klassifizierung Aktion aufzeichnen.

## <a name="reporting"></a>Berichte

Verwenden Sie die Überwachung Berichte, um die Überprüfung Aktivität Ebene der Richtlinie und Bearbeiter finden Sie unter. Für jede Richtlinie können Sie auch live Statistiken auf den aktuellen Status der Überprüfung Aktivität anzeigen. Sie können die Überwachung Berichte verwenden:
  
- Stellen Sie sicher, dass Ihre Richtlinien wie gewünscht funktionieren.
- Hier erfahren Sie, wie viele Communications zur Prüfung erkannt werden.
- Erfahren Sie, wie viele Communications nicht kompatibel sind und welche übergeben werden überprüfen. Diese Informationen helfen Ihnen die Entscheidung für Optimieren Ihrer Richtlinien oder Ändern der Anzahl der Bearbeiter.

### <a name="view-the-supervision-report"></a>Anzeigen des Berichts zu Überwachung

1. Melden Sie sich bei der [Sicherheit & Compliance Center](https://protection.office.com/) mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation, die über Berechtigungen zum Anzeigen von Berichten Aufsicht verfügt.
2. Wechseln Sie zu **Berichte** \> **Dashboard** oder **Überwachung**. Sehen Sie eine Überwachung reporting Widget mit einer Zusammenfassung der aktuellen Aufsicht Policy-Aktivität ein.
3. Wählen Sie das Widget **Überwachung** , um die Seite detaillierten Bericht öffnen.

> [!NOTE]
> Wenn Sie auf die Seite **Berichte** zugreifen nicht, überprüfen Sie, ob Sie ein Mitglied der Rollengruppe generelle Überprüfung sind wie unter [Überwachung in Ihrer Organisation zur Verfügung stellen](configure-supervision-policies.md). In dieser Rolle Gruppe können Sie erstellen und Verwalten der Überwachung eingeschlossen werden Richtlinien, und führen Sie den Bericht.
  
### <a name="how-to-use-the-report"></a>So verwenden Sie den Bericht

Wenn eine Richtlinie für Überwachung Kommunikation-Nachricht zum Überarbeiten erkannt wird, wird die e-Mail in der Prüfer Aufsicht Ordner in Outlook und Outlook übermittelt Web app. Dieser Bericht listet die Namen der einzelnen Richtlinien und die Anzahl der Kommunikation in den einzelnen Phasen des Prozesses überprüfen.
  
Verwenden Sie den Bericht an:
  
- Anzeigen von Daten für alle oder bestimmte Richtlinien.
- Anzeigen von Daten, die gruppiert nach Tag Typs (beispielsweise konform, Questionable usw.), Bearbeiter oder Nachrichtentyp.
- Exportieren von Daten in eine CSV-Datei basierend auf das Aktivitätsdatum, Richtlinie, und durch Reviewer-Aktivität.
- Filtern von Daten basierend auf das Aktivitätsdatum, Tagtyp, Reviewer und Nachrichtentyp.

Es folgt eine Aufschlüsselung der Werte, die möglicherweise in der Spalte **Typ Tag** angezeigt.
  
|**Tagtyp**|**Was bedeutet, dass**|
|:-----|:-----|
| Nicht überprüft. | Die Anzahl der e-Mails, die noch nicht überprüft. Diese e-Mails werden zur Überprüfung im Office 365 Aufsicht Dashboard oder in der Prüfer Aufsicht Ordner in Outlook-/Outlook Web App erwartet.|
| Kompatible | Die Anzahl der e-Mails überprüft und als kompatibel markiert. Diese Nachrichten müssen noch aufgelöst werden. |
| Fragwürdige | Die Anzahl der e-Mails überprüft und fragwürdige gekennzeichnet. Dies fungiert als Flag. andere Bearbeiter helfen überprüfen, ob eine e-Mail-Nachricht für die Einhaltung der Untersuchung benötigt. Diese Nachrichten müssen noch aufgelöst werden. |
| Nicht kompatible (aktiv) | Die Anzahl der nicht konforme e-Mails, die derzeit Bearbeiter untersuchen. |
| Nicht-kompatible (aufgelöst) | Die Anzahl der nicht konforme e-Mails, die Bearbeiter untersucht und aufgelöst. |
| Drücken Sie die Richtlinie | Die Gesamtzahl (täglich) von Nachrichten von Exchange, Teams und Drittanbieter-Datenquellen, die eine oder mehrere der in einer Richtlinie für Überwachung festgelegten Bedingungen entsprechen. |
| Im Geltungsbereich | Die Gesamtzahl (täglich) von Nachrichten von Exchange, Teams und Drittanbieter-Datenquellen, die durch eine Richtlinie für Überwachung überprüft |
| Aufgelöst | Die Gesamtzahl der Nachrichten von Exchange, Teams und Drittanbieter-Datenquellen, die als **gelöst** klassifiziert wurden|

> [!NOTE]
> Aufsichtsrichtlinien müssen zuerst bereitgestellt werden, bevor sie in diesem Bericht angezeigt werden. Wenn Richtlinien gelöscht werden, werden darüber hinaus noch Verlaufsdaten angezeigt. Allerdings sie "nicht vorhandene Richtlinie" gekennzeichnet sind, und die **Export** -Funktion ist nicht verfügbar.

## <a name="auditing"></a>Überwachung

In einigen Fällen müssen Sie Informationen zur Einhaltung behördlicher bereitstellen oder Compliance-Auditoren Überwachung der Mitarbeiteraktivitäten und Communications nachzuweisen. Dies ist möglicherweise eine Zusammenfassung der alle generelle Aktivitäten im Zusammenhang mit einer definierten Richtlinie oder, jedes Mal, wenn eine Richtlinie für Überwachung geändert oder aktualisiert wurde. Aufsichtsrichtlinien haben integrierten Prüflisten für vollständige Bereitschaft für interne oder externe Überwachungen. Nachweis der generelle Verfahren kann mit einen detaillierten Audit Verlauf aller Aktionen, die von Ihrer aufsichtsrichtlinien überwacht nachgewiesen werden.

Die folgenden Aufsicht Richtlinie Aktivitäten überwacht werden sollen, und können mithilfe der unified Office 365-Überwachungsprotokolle angezeigt werden:

|**Aktivität**|**Zugeordnete Befehle**|
|:-----|:-----|
| Erstellen einer Richtlinie | Neue SupervisoryReviewPolicy <br> Neue SupervisoryReviewRule |
| Bearbeiten einer Richtlinie | Set-SupervisoryReviewPolicy <br> Set-SupervisoryReviewRule |
| Löschen einer Richtlinie| Remove-SupervisoryReviewPolicy |

Die Überwachungen können abgerufen werden, mit der Suchfunktion von einheitlichen Audit Log oder mithilfe des [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) -PowerShell-Cmdlets.

Beispielsweise das folgende Beispiel gibt die Aktivitäten für die alle generelle Überprüfung Aktivitäten (Richtlinien und Regeln) und enthält detaillierte Informationen für die einzelnen:

```
Search-UnifiedAuditLog -StartDate $startDate -EndDate $endDate -RecordType DataGovernance -ResultSize 5000 | Where-Object {$_.Operations -like "*SupervisoryReview*"} | fl CreationDate,Operations,UserIds,AuditData 
```

Zusätzlich zu den Informationen in die Überwachung von Berichten und Protokollen können Sie auch das PowerShell-Cmdlet [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewactivity?view=exchange-ps) verwenden, um eine vollständige Liste aller Aufsicht detaillierte Richtlinie Aktivitäten zurückzugeben.

## <a name="ready-to-get-started"></a>Sind Sie bereit für die ersten Schritte?

Zum Konfigurieren der Überwachung Richtlinien für Ihre Organisation zu starten, finden Sie unter [Configure aufsichtsrichtlinien](configure-supervision-policies.md).