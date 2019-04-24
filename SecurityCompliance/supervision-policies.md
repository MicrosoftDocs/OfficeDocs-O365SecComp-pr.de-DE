---
title: Aufsichtsrichtlinien in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
f1_keywords:
- ms.o365.cc.SupervisoryReview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
ms.assetid: d14ae7c3-fcb0-4a03-967b-cbed861bb086
description: Grundlegendes zu Aufsichtsrichtlinien in Office 365
ms.openlocfilehash: 091f5b1f31fcf59162df6ded6a6b07fb501834c7
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260323"
---
# <a name="supervision-policies-in-office-365"></a>Aufsichtsrichtlinien in Office 365

Mit Aufsichtsrichtlinien in Office 365 können Sie Mitarbeiterkommunikation zur Prüfung durch bestimmte Prüfer erfassen. Sie können bestimmte Richtlinien definieren, die interne und externe e-Mails, Microsoft Teams oder 3rd-Party-Kommunikationen in Ihrer Organisation erfassen. Die Bearbeiter können die Nachrichten dann überprüfen, um sicherzustellen, dass Sie den Nachrichtenstandards Ihrer Organisation entsprechen und diese mit dem Klassifizierungs auflösen. Mit diesen Richtlinien können Sie auch viele moderne Compliance-Herausforderungen bewältigen, einschließlich der Überwachung zunehmender Arten von Kommunikationskanälen, erhöhen des Volumens von Nachrichtendaten und der behördlichen Durchsetzung & das Risiko von Geldbußen.

In einigen Organisationen gibt es möglicherweise eine Trennung der Aufgaben zwischen dem IT-Support und der Compliance-Verwaltungsgruppe. Office 365 unterstützt die Trennung zwischen der Konfiguration des Mandanten mit den Aufsichtsrichtlinien-Supportfunktionen und der Konfiguration von Richtlinien und der Reaktion auf aufgezeichnete Kommunikation. Die IT-Gruppe für eine Organisation kann beispielsweise für das Einrichten von Rollen Berechtigungen und Gruppen zuständig sein, um Aufsichtsrichtlinien zu unterstützen, die vom Compliance-Team der Organisation konfiguriert und verwaltet werden.

## <a name="scenarios-for-supervision-policies"></a>Szenarien für Aufsichtsrichtlinien

Aufsichtsrichtlinien können die Überwachung der Kommunikation in Ihrer Organisation in mehreren Bereichen unterstützen:

- **Unternehmensrichtlinien**

    Mitarbeiter müssen in allen unternehmensbezogenen Kommunikationen eine akzeptable Nutzung, ethische Standards und andere Unternehmensrichtlinien einhalten. Aufsichtsrichtlinien können Richtlinienverstöße ermitteln und Ihnen helfen, Korrekturmaßnahmen zu ergreifen, um diese Art von Vorfällen zu verringern. Beispielsweise können Sie Ihre Organisation auf potenzielle Verletzungen der Personalabteilung überwachen, beispielsweise Belästigung oder die Verwendung ungeeigneter oder anstößiger Sprachen in der Mitarbeiterkommunikation.

- **Risikomanagement**

    Organisationen sind für alle Kommunikationen verantwortlich, die über Ihre Infrastruktur und Unternehmensnetzwerk Systeme verteilt sind. Durch die Verwendung von Aufsichtsrichtlinien zur Identifizierung und Verwaltung potenzieller rechtlicher Risiken und Risiken kann das Risiko minimiert werden, bevor es zu Unternehmens Vorgängen kommen kann. Beispielsweise können Sie Ihre Organisation auf unbefugte Kommunikation für vertrauliche Projekte wie anstehende Akquisitionen, Zusammenschlüsse, ergebnisoffen Legungen, Umstrukturierungen oder Änderungen des Führungsteams überwachen.

- **Einhaltung gesetzlicher Vorschriften**

    Die meisten Organisationen müssen im Rahmen ihrer normalen Betriebsverfahren irgendeine Art von Compliance-Standards erfüllen. Diese Bestimmungen erfordern häufig eine Art Aufsichts-oder Überwachungsverfahren für Messaging, das für die jeweilige Branche geeignet ist. Die Regel 3110 der Finanzindustrie-Regulierungsbehörde (FINRA) ist ein gutes Beispiel dafür, dass Organisationen über Aufsichtsverfahren verfügen, um die Aktivitäten Ihrer Mitarbeiter zu überwachen und die Arten von Geschäften, in denen Sie tätig sind. Ein weiteres Beispiel ist die Überprüfung von Broker Händlern in Ihrer Organisation, um gegen mögliche Geldwäsche, Insiderhandel, Absprachen oder Bestechungsaktivitäten zu schützen. Aufsichtsrichtlinien können Ihre Organisation bei der Erfüllung dieser Anforderungen unterstützen, indem Sie einen Prozess zur Überwachung und Berichterstellung über die Unternehmenskommunikation bereitstellen.

## <a name="components"></a>Komponenten

### <a name="supervision-policy"></a>Aufsichtsrichtlinie

Sie erstellen Aufsichtsrichtlinien im Compliance Center. Diese Richtlinien legen fest, welche Kommunikationen und Benutzer in Ihrer Organisation überprüft werden sollen, definieren benutzerdefinierte Bedingungen, die die Kommunikation erfüllen muss, und gibt an, wer Bewertungen durchführen soll. Benutzer, die in der Rollengruppe Aufsichtsüberprüfung enthalten sind, können Richtlinien einrichten, und alle Personen, denen diese Rolle zugewiesen wurde, können auf die Seite "Überwachung" im Compliance Center zugreifen.

### <a name="supervised-users"></a>ÜberWachte Benutzer

Bevor Sie mit der Überwachung beginnen, müssen Sie bestimmen, wer Ihre Kommunikation überprüfen muss. In der Richtlinie identifizieren Benutzer-e-Mail-Adressen Personen oder Gruppen von Personen, die überwacht werden sollen. Beispiele für diese Gruppen sind Office 365-Gruppen, Exchange-basierte Verteilerlisten und Microsoft Teams-Kanäle. Sie können auch bestimmte Benutzer oder Gruppen von der Aufsicht mit einer überwachten Gruppe oder einer Liste von Gruppen ausschließen.

> [!IMPORTANT]
> Benutzer, die von Aufsichtsrichtlinien überwacht werden, müssen über eine Microsoft 365 E5-Konformitäts Lizenz, eine Office 365 Enterprise E3-Lizenz mit dem Advanced Compliance-Add-on verfügen oder in ein Office 365 Enterprise E5-Abonnement aufgenommen werden.
Wenn Sie keinen Enterprise E5-Plan haben und die Überwachung testen möchten, können Sie [sich für eine Testversion von Office 365 Enterprise E5 registrieren](https://go.microsoft.com/fwlink/p/?LinkID=698279).

### <a name="reviewers"></a>Prüfer

Wenn Sie eine Aufsichtsrichtlinie erstellen, müssen Sie bestimmen, wer die Überprüfungen der Nachrichten der überwachten Benutzer ausführen soll. In der Richtlinie identifizieren Benutzer-e-Mail-Adressen Personen oder Gruppen von Personen, die überwachte Kommunikationen überprüfen. Alle Prüfer müssen über Postfächer verfügen, die in Exchange Online gehostet werden.

### <a name="groups-for-supervised-users-and-reviewers"></a>Gruppen für überwachte Benutzer und Prüfer

Um das Setup zu vereinfachen, erstellen Sie Gruppen für Personen, die Ihre Kommunikation benötigen, und Gruppen für Personen, die diese Kommunikationen überprüfen. Wenn Sie Gruppen verwenden, benötigen Sie möglicherweise mehrere. Wenn Sie beispielsweise die Kommunikation zwischen zwei unterschiedlichen Personengruppen überwachen möchten, oder wenn Sie eine Gruppe angeben möchten, die nicht überwacht wird.

### <a name="supported-communication-types"></a>Unterstützte Kommunikationstypen

Mit Aufsichtsrichtlinien können Sie Nachrichten auf einer oder mehreren der folgenden Kommunikationsplattformen überwachen:

- **Exchange-e-Mail:** Postfächer, die in Exchange Online als Teil Ihres Office 365-Abonnements gehostet werden, sind alle für die Nachrichten Aufsicht berechtigt. E-Mails und Anhänge passender Aufsichtsrichtlinien Bedingungen stehen sofort für die Überwachung und in Aufsichtsberichten zur Verfügung. Unterstützte Anlagentypen für die Überwachung sind identisch mit den [Dateitypen, die für Exchange-Nachrichtenfluss Regel-Inhalts Prüfungen unterstützt](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection)werden.
- **Microsoft Teams:** Chatnachrichten und zugehörige Anlagen in öffentlichen und privaten Microsoft Teams-Kanälen und einzelnen Chats können überwacht werden. Teams-Chats, die Aufsichtsrichtlinien Bedingungen entsprechen, werden alle 24 Stunden verarbeitet und stehen dann für die Überwachung und in Aufsichtsberichten zur Verfügung. Verwenden Sie die folgenden Gruppen Verwaltungs Konfigurationen, um einzelne Benutzer Chats und die Kanal Kommunikation in Teams zu überwachen:

    - **Für die Team Chat Aufsicht:** Weisen Sie einzelne Benutzer zu, oder weisen Sie der Aufsichtsrichtlinie eine [Verteilergruppe](https://support.office.com/article/Distribution-groups-E8BA58A8-FAB2-4AAF-8AA1-2A304052D2DE) zu. Dies ist für 1-zu-1-oder 1-zu-n-Benutzer/Chat-Beziehungen.
    - **Für Teams-Kanal Kommunikation:** Weisen Sie jeder Microsoft Team Channel-oder Office 365-Gruppe, die Sie überwachen möchten, einen bestimmten Benutzer zur Aufsichtsrichtlinie zu. Wenn Sie den gleichen Benutzer anderen Microsoft Teams-Kanälen oder Office 365-Gruppen hinzufügen, müssen Sie diese neuen Kanäle und Gruppen auch der Aufsichtsrichtlinie hinzufügen.

- **Drittanbieterquellen:** Sie können die Kommunikation von Drittanbieterquellen (wie Facebook oder DropBox) für Daten überwachen, die in Office 365-Postfächern in Ihrer Organisation importiert werden. [Informationen zum Importieren von drittanbieterdaten in Office 365](https://docs.microsoft.com/office365/securitycompliance/archiving-third-party-data).

### <a name="policy-settings"></a>Richtlinieneinstellungen

#### <a name="direction"></a>Richtung

Standardmäßig wird die **Richtung** Bedingung angezeigt und kann nicht entfernt werden. Die Kommunikations Richtungseinstellungen in einer Richtlinie werden einzeln oder zusammen ausgewählt:

- **Eingehend**– Sie können " **eingehend** " auswählen, um die Kommunikation zu überwachen **, die an** die Personen gesendet werden, die Sie **von** Personen, die nicht in der Richtlinie enthalten sind, über
- **** Ausgehend: Sie können **ausgehende** Nachrichten überwachen, die von den Personen gesendet werden, **** die Sie für die Überwachung **von** Personen ausgewählt haben, die nicht in der Richtlinie enthalten sind.
- **Intern** -Sie können die Kommunikation **zwischen** den Personen, die Sie in der Richtlinie identifiziert haben, **intern** auswählen.

#### <a name="sensitive-information-types"></a>Typen vertraulicher Informationen

Sie haben die Möglichkeit, vertrauliche Informationstypen als Teil ihrer Aufsichtsrichtlinie einzubinden. Vertrauliche Informationstypen sind entweder vordefinierte oder benutzerdefinierte Datentypen, die dazu beitragen können, Kreditkartennummern, Bank Kontonummern, Passport-Nummern und vieles mehr zu identifizieren und zu schützen. Als Teil von Office 365 [Data Loss Prevention (DLP)](data-loss-prevention-policies.md)kann die Konfiguration vertraulicher Informationen Muster, Zeichen Nähe, Zuverlässigkeits Stufen und sogar benutzerdefinierte DatentypenVerwenden, um Inhalte zu identifizieren und zu kennzeichnen, die möglicherweise vertraulich sind. Die Standardtypen für vertrauliche Informationen sind:

- Finanzen
- Medizin und Gesundheit
- Datenschutz
- Benutzerdefinierter Informationstyp

Weitere Informationen zu vertraulichen Informationen und den in den Standardtypen enthaltenen Mustern finden Sie unter [welche Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).

#### <a name="custom-keyword-dictionaries"></a>Benutzerdefinierte Keyword-Wörterbücher

Das Konfigurieren von benutzerdefinierten Keyword-Wörterbüchern (oder Lexika) ermöglicht die einfache Verwaltung von Schlüsselwörtern für Ihre Organisation oder Branche und kann bis zu 100.000 Ausdrücke pro Wörterbuch unterstützen. Bei Bedarf können Sie mehrere benutzerdefinierte Keyword-Wörterbücher auf eine einzelne Richtlinie anwenden oder über ein einzelnes Stichwort Wörterbuch pro Richtlinie verfügen. Diese Wörterbücher werden in einer Aufsichtsrichtlinie zugewiesen und können aus einer Datei (wie eine CSV-oder txt-Liste) oder aus einer Liste, [die Sie im Compliance Center importieren](create-a-keyword-dictionary.md)können, bezogen werden.

#### <a name="conditional-settings"></a>Bedingte Einstellungen

Die Bedingungen, die Sie für die Richtlinie wählen, gelten für die Kommunikation von e-Mails und Drittanbieterquellen in Ihrer Organisation (wie bei Facebook oder DropBox).

In der folgenden Tabelle werden weitere Informationen zu den einzelnen Bedingungen erläutert.
  
|**Bedingung**|**Verwendung**|
|:-----|:-----|
| Die Nachricht wird von einer dieser Domänen empfangen.  <br><br> Nachricht wird von keiner dieser Domänen empfangen | Wenn Sie die Richtlinie anwenden möchten, wenn bestimmte Domänen in eine empfangene Nachricht eingeschlossen oder ausgeschlossen werden, geben Sie jede Domäne ein, und trennen Sie mehrere Domänen durch ein Komma. Jede von Ihnen eingegebene Domäne wird separat angewendet (nur eine dieser Domänen muss gelten, damit die Richtlinie auf die Nachricht angewendet wird). |
| Die Nachricht wird an eine dieser Domänen gesendet.  <br><br> Nachricht wird an keine dieser Domänen gesendet | Wenn Sie die Richtlinie anwenden möchten, wenn bestimmte Domänen in eine gesendete Nachricht eingeschlossen oder ausgeschlossen werden, geben Sie jede Domäne ein, und trennen Sie mehrere Domänen durch ein Komma. Jede von Ihnen eingegebene Domäne wird separat angewendet (nur eine dieser Domänen muss gelten, damit die Richtlinie auf die Nachricht angewendet wird). |
| Die Nachricht wird mit einer dieser Bezeichnungen klassifiziert.  <br><br> Die Nachricht ist nicht mit einer dieser Bezeichnungen klassifiziert | Anwenden der Richtlinie, wenn bestimmte Aufbewahrungs Bezeichnungen in eine Nachricht eingeschlossen oder ausgeschlossen werden. Aufbewahrungs Bezeichnungen müssen separat konfiguriert werden, und konfigurierte Bezeichnungen werden als Teil dieser Bedingung ausgewählt. Jede ausgewählte Bezeichnung wird separat angewendet (nur eine dieser Bezeichnungen muss für die Richtlinie gelten, die auf die Nachricht angewendet werden soll). Weitere Informationen zum Konfigurieren von Aufbewahrungs Bezeichnungen finden Sie unter [Übersicht über Aufbewahrungs Beschriftungen](https://docs.microsoft.com/office365/securitycompliance/labels).|
| Nachricht enthält eines dieser Wörter  <br><br> Nachricht enthält keines dieser Wörter | Wenn Sie die Richtlinie anwenden möchten, wenn bestimmte Wörter oder Ausdrücke in eine Nachricht eingeschlossen oder ausgeschlossen werden, geben Sie jedes Wort oder jeden Ausdruck in einer separaten Linie ein. Jede eingegebene Zeile wird separat angewendet (nur eine dieser Zeilen muss angewendet werden, damit die Richtlinie auf die Nachricht angewendet wird). Weitere Informationen zum Eingeben von Wörtern oder Ausdrücken finden Sie im nächsten Abschnitt [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
| Anlage enthält eines dieser Wörter  <br><br> Anlage enthält keines dieser Wörter | Wenn Sie die Richtlinie anwenden möchten, wenn bestimmte Wörter oder Ausdrücke in eine Nachrichtenanlage eingeschlossen oder ausgeschlossen werden (beispielsweise ein Word-Dokument), geben Sie jedes Wort oder jeden Ausdruck in einer separaten Linie ein. Jede eingegebene wortlinie wird separat angewendet (nur eine einzige Linie muss für die Richtlinie gelten, die auf die Anlage angewendet werden soll). Weitere Informationen zum Eingeben von Wörtern oder Ausdrücken finden Sie im nächsten Abschnitt [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
| Attachment ist einer dieser Dateitypen  <br><br> Attachment ist keiner dieser Dateitypen | Um die Kommunikation zu überwachen, in der bestimmte Typen von Anlagen eingeschlossen oder ausgeschlossen werden, geben Sie die Dateierweiterungen ein (wie. exe oder. pdf). Wenn Sie mehrere Dateierweiterungen einschließen oder ausschließen möchten, geben Sie diese in separaten Zeilen ein. Damit die Richtlinie angewendet wird, muss nur eine Anlagenerweiterung übereinstimmen.|
| Nachricht ist größer als  <br><br> Die Nachrichtengröße ist nicht größer als | Um Nachrichten anhand einer bestimmten Größe zu überarbeiten, verwenden Sie diese Bedingungen, um die maximale oder minimale Größe einer Nachricht anzugeben, bevor Sie überprüft werden kann. wenn sie beispielsweise die **nachrichtengröße größer als** \> **1,0 mb**angeben, werden alle nachrichten, die 1,01 mb groß sind, überprüft. Sie können Byte, Kilobyte, Megabyte oder Gigabyte für diese Bedingung auswählen.|
| Die Anlage ist größer als  <br><br> Die Anlage ist nicht größer als | Um Nachrichten anhand der Größe Ihrer Anlagen zu überarbeiten, geben Sie die maximale oder minimale Größe an, die eine Anlage aufweisen kann, bevor die Nachricht und ihre Anlagen überprüft werden können. wenn sie beispielsweise attachment angeben, **ist größer als** \> **2,0 mb**, können alle nachrichten mit anlagen 2,01 mb und mehr überprüft werden. Sie können Byte, Kilobyte, Megabyte oder Gigabyte für diese Bedingung auswählen.|
   
##### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Übereinstimmende Wörter und Ausdrücke in E-Mails oder Anlagen
<a name="Matchwords"></a> Jede eingegebene wortlinie wird separat angewendet (nur eine einzige Linie muss für die Richtlinienbedingung gelten, die auf die e-Mail oder Anlage angewendet werden soll). Verwenden wir beispielsweise die Bedingung, **Nachricht enthält eines dieser Wörter**mit den Stichwörtern "Banker" und "Insider Trading" in separaten Zeilen. Die Richtlinie gilt für alle Nachrichten, die das Wort "Banker" oder "Insider Trading" enthalten. Nur eins der Wörter oder einer der Ausdrücke muss vorkommen, damit die Richtlinienbedingung zutrifft. Wörter in der Nachricht oder Anlage müssen genau mit Ihren Angaben übereinstimmen.
  
##### <a name="enter-multiple-conditions"></a>Mehrere Bedingungen eingeben

Wenn Sie mehrere Bedingungen eingeben, verwendet Office 365 alle Bedingungen, um zu bestimmen, wann die Richtlinie auf Kommunikationselemente angewendet werden soll. Wenn Sie mehrere Bedingungen einrichten, müssen alle erfüllt sein, damit die Richtlinie angewendet wird, außer wenn Sie eine Ausnahme eingeben. Sie müssen beispielsweise eine Richtlinie erstellen, die angewendet werden sollte, wenn eine Nachricht das Wort "Trade" enthält und größer als 2 MB ist. Wenn die Nachricht jedoch auch die Wörter "Approved by Contoso Financial" enthält, sollte die Richtlinie nicht angewendet werden. In diesem Fall würden die drei Bedingungen wie folgt aussehen:
  
- Die **Nachricht enthält eines dieser Wörter**mit den Schlüsselwörtern "Trade".

- Die **Nachrichtengröße ist größer als**, mit dem Wert 2 MB

- Die **Nachricht enthält keines dieser Wörter**, mit den Stichwörtern "von Contoso Financial Team genehmigt".

#### <a name="review-percentage"></a>Prozentsatz der Überprüfungen

Wenn Sie die Menge der zu überprüfenden Inhalte reduzieren möchten, können Sie einen Prozentsatz der gesamten Kommunikation angeben, die von einer Aufsichtsrichtlinie gesteuert wird. Eine zufällig ausgewählte Menge an Inhalten wird aus dem Gesamtprozentsatz ausgewählt, der den von Ihnen ausgewählten Bedingungen entspricht. Wenn Sie möchten, dass die Bearbeiter alle Elemente überwachen, können Sie **100%** in eine Aufsichtsrichtlinie eingeben.

## <a name="monitor--manage"></a>Überwachen von & Manage

Die Überwachung der Ergebnisse ihrer Aufsichtsrichtlinien und die Anwendung eines Lösungs Tags ist einfach und bequem. Sie können den Status von überprüfte Elemente, die Benutzer und Gruppen unter Aufsicht und die Benutzer und Gruppen, die als Prüfer festgelegt sind, schnell anzeigen.

### <a name="supervision-policy-dashboard"></a>Überwachungsrichtlinien-Dashboard

Am einfachsten können Sie die Ergebnisse der Aufsichtsrichtlinien verwalten und ausstehende Elemente lösen, indem Sie das Dashboard für Aufsichtsrichtlinien verwenden. Mit diesem Dashboard können Prüfer Elemente anzeigen, die überprüft werden müssen, Aktionen für ein Element ergreifen und die Ergebnisse zuvor überprüfter und aufgelöster Elemente für jede Aufsichtsrichtlinie überprüfen. Sie können auf das Dashboard Aufsichtsrichtlinien im Compliance Center unter **beaufsichtigen** > Sie*Ihre benutzerdefinierte Richtlinie* > **Öffnen**zugreifen.

#### <a name="dashboard-home"></a>Dashboard-Startseite

Die Dashboard- **Start** Seite verfügt über mehrere Abschnitte, die Ihnen helfen, schnell Maßnahmen für Ihre Aufsichtsrichtlinien durchführen zu können. Hier können Sie folgende Schritte durchgehen:

- Schnelles überarbeiten der ausstehenden und aufgelösten Highlights der Woche
- Anzeigen einer Liste der überwachten Benutzer und überwachten Gruppen für die ausgewählte Richtlinie
- Anzeigen einer Liste der Prüfer und Überprüfen von Teams für die ausgewählte Richtlinie
- Sehen Sie, welche Kommunikationsplattformen Inhalte unter Überwachung für die Richtlinie enthalten.

#### <a name="review-tab"></a>Registerkarte "überarbeiten"

Auf der Registerkarte **Überarbeiten** können Prüfer Aktionen ausführen und von der ausgewählten Richtlinie identifizierte Elemente auflösen. Hier können Sie folgende Schritte durchgehen:

- Filtern nach ausstehenden, kompatiblen, nicht kompatiblen und fragwürdigen Elementen
- Kennzeichnen eines einzelnen Elements als kompatibel, nicht kompatibel oder fragwürdig. Sie können auch einen Kommentar mit dem Element aufzeichnen, um die getroffene Markierungs Aktion zu veranschaulichen.
- Massen Kennzeichnung mehrerer Elemente als kompatibel, nicht kompatibel oder fragwürdig. Sie können auch einen Kommentar mit mehreren Elementen aufzeichnen, um die getroffene Markierungs Aktion zu veranschaulichen.
- Anzeigen des Verlaufs des Taggings für ein einzelnes Element. Dazu gehören die Person, die das Element aufgelöst hat, das Datum und die Uhrzeit der Aktion, das Lösungstag und alle enthaltenen Kommentare.
- Neu klassifizieren Sie zuvor überprüfte Elemente als kompatibel, nicht konform oder fragwürdig. Sie können auch einen Kommentar mit einzelnen oder mehreren Elementen aufzeichnen, um die umklassifizierungs Aktion zu veranschaulichen.

#### <a name="resolved-items-tab"></a>Registerkarte "aufgelöste Elemente"

Auf der Registerkarte **aufgelöste Elemente** können Prüfer alle zuvor aufgelöste Elemente für die ausgewählte Richtlinie anzeigen. Hier können Sie folgende Schritte durchgehen:

- Schnelles anzeigen und Sortieren des Betreffs, des Absenders und des Datums der aufgelösten Elemente.
- Anzeigen des Klassifizierungs-und Kommentar Verlaufs eines ausgewählten Elements

### <a name="other-ways-to-review-items"></a>Weitere Möglichkeiten zum Überarbeiten von Elementen

Wenn die Bearbeiter das Aufsichts Dashboard in Office 365 nicht verwenden möchten, haben Sie auch weitere Optionen zum überarbeiten und Verwalten von Elementen, die von Aufsichtsrichtlinien erfasst werden.

#### <a name="outlook-on-the-web"></a>Outlook im Web

Benutzer, die in einer Aufsichtsrichtlinie als Prüfer festgelegt sind, können mithilfe von Outlook im Web Aufsichts Elemente überwachen und lösen. Das Überwachungs-Add-in wird automatisch in Outlook im Web für alle in der Richtlinie angegebenen Prüfer installiert. Es ist keine zusätzliche Konfiguration erforderlich, damit freigegebene Ordner der Aufsichtsrichtlinie für konfigurierte Prüfer zur Verfügung stehen.

Mit Outlook im Web können Prüfer:

- Anzeigen gefilterter Elemente nach dem Status "kompatibel", "nicht kompatibel", "fragwürdig" und "aufgelöst"
- Kennzeichnen eines einzelnen Elements als kompatibel, nicht kompatibel, fraglich oder aufgelöst. Sie können auch einen Kommentar mit dem Element aufzeichnen, um die getroffene Markierungs Aktion zu veranschaulichen.
- Anzeigen des Verlaufs des Taggings für ein einzelnes Element, einschließlich der Person, die das Element aufgelöst hat, des Datums und der Uhrzeit der Aktion, des Lösungs Tags und der enthaltenen Kommentare.
- Neu klassifizieren Sie zuvor überprüfte Elemente als kompatibel, nicht konform oder fragwürdig. Sie können auch einen Kommentar mit einzelnen Elementen aufzeichnen, um die umklassifizierungs Aktion zu veranschaulichen.

#### <a name="microsoft-outlook"></a>Microsoft Outlook

Zur Überprüfung der durch eine Aufsichtsrichtlinie identifizierten Kommunikation können Prüfer auch das Aufsichts-Add-in für Microsoft Outlook verwenden. Die Prüfer müssen jedoch einige Schritte ausführen, um Sie in der Desktop Version von Outlook zu installieren. Ausführliche Anleitungen zum Aufsichts-Add-in für Outlook finden Sie unter [Konfigurieren von Aufsichtsrichtlinien](configure-supervision-policies.md).

Mit Outlook können Prüfer:

- Anzeigen gefilterter Elemente nach dem Status "kompatibel", "nicht kompatibel", "fragwürdig" und "aufgelöst"
- Kennzeichnen eines einzelnen Elements als kompatibel, nicht kompatibel, fraglich oder aufgelöst. Sie können auch einen Kommentar mit dem Element aufzeichnen, um die getroffene Markierungs Aktion zu veranschaulichen.
- Anzeigen des Verlaufs des Taggings für ein einzelnes Element, einschließlich der Person, die das Element aufgelöst hat, des Datums und der Uhrzeit der Aktion, des Lösungs Tags und der enthaltenen Kommentare.
- Neu klassifizieren Sie zuvor überprüfte Elemente als kompatibel, nicht konform oder fragwürdig. Sie können auch einen Kommentar mit einzelnen Elementen aufzeichnen, um die umklassifizierungs Aktion zu veranschaulichen.

## <a name="reports"></a>Berichte

Verwenden Sie die Überwachungsberichte, um die Überprüfungsaktivität auf Richtlinie und Prüfer Ebene anzuzeigen. Für jede Richtlinie können Sie auch Live Statistiken zum aktuellen Status der Überprüfungen anzeigen. Sie können die Überwachungsberichte für folgende Zwecke verwenden:
  
- Stellen Sie sicher, dass Ihre Richtlinien wie gewünscht funktionieren.
- Erfahren Sie, wie viele Kommunikationen zur Überprüfungen identifiziert werden.
- Erfahren Sie, wie viele Kommunikationen nicht kompatibel sind und welche Überprüfungen durchgeführt werden. Anhand dieser Informationen können Sie entscheiden, ob Sie Ihre Richtlinien optimieren oder die Anzahl der Bearbeiter ändern möchten.

### <a name="view-the-supervision-report"></a>Anzeigen des Aufsichts Berichts

1. Melden Sie sich im [Compliance Center](https://compliance.microsoft.com) mit den Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an, das über Berechtigungen zum Anzeigen von Überwachungsberichten verfügt.
2. Wechseln Sie zu **Berichte** \> **Dashboard** oder **Überwachung**. Es wird ein Widget "Aufsichtsbericht" mit einer Zusammenfassung der aktuellen Aufsichtsrichtlinien Aktivität angezeigt.
3. Wählen Sie das **Überwachungs** -widget aus, um die Seite detaillierte Berichte zu öffnen.

> [!NOTE]
> Wenn Sie nicht auf die Seite " **Berichte** " zugreifen können, stellen Sie sicher, dass Sie Mitglied der rollenGruppe "Supervisory Review" sind, wie unter [machen der Aufsicht in Ihrer Organisation](configure-supervision-policies.md)beschrieben. Wenn Sie in diese Rollengruppe eingeschlossen werden, können Sie Aufsichtsrichtlinien erstellen und verwalten und den Bericht ausführen.
  
### <a name="how-to-use-the-report"></a>Verwenden des Berichts

Wenn eine Überwachungsrichtlinie eine Kommunikations Nachricht zur Überprüfung identifiziert, wird die e-Mail an den Aufsichts Ordner der Prüfer in Outlook und Outlook im Web (früher als Outlook Web App bezeichnet) übermittelt. In diesem Bericht werden die einzelnen Richtlinien und die Anzahl der Kommunikationen in jeder Phase des überarbeits Vorgangs aufgelistet.
  
Verwenden Sie den Bericht für Folgendes:
  
- Anzeigen von Daten für alle oder bestimmte Richtlinien.
- Anzeigen von Daten gruppiert nach Tag-Typ, Prüfer oder Nachrichtentyp.
- Exportieren von Daten in eine CSV-Datei basierend auf dem Aktivitätsdatum, der Richtlinie und der Prüfer Aktivität.
- Filtern von Daten basierend auf dem Aktivitätsdatum, dem Tag-Typ, dem Prüfer und dem Nachrichtentyp.

Nachfolgend finden Sie eine Aufstellung der Werte, die in der **** Spalte Transpondertyp angezeigt werden können.
  
|**Tagtyp**|**Bedeutung**|
|:-----|:-----|
| Nicht überprüft | Die Anzahl von e-Mails, die noch nicht überprüft wurden. Diese e-Mails warten auf die Überprüfung im Office 365-überwachungsdashboard oder im Ordner "Aufsicht" des Rezensenten in Outlook oder Outlook im Web.
| Kompatible | Die Anzahl der überprüften und als kompatibel markierten e-Mails. Diese Nachrichten benötigen noch eine Lösung. |
| Fragwürdig | Die Anzahl der überprüften und markierten e-Mails. Dies dient als Kennzeichnung für andere Prüfer, um zu überprüfen, ob eine e-Mail-Konformitätsprüfung erforderlich ist. Diese Nachrichten benötigen noch eine Lösung. |
| Nicht konform (aktiv) | Die Anzahl der nicht kompatiblen e-Mails, die von den Prüfern derzeit untersucht werden. |
| Nicht kompatibel (aufgelöst) | Die Anzahl der nicht kompatiblen e-Mails, die von den Bearbeitern untersucht und aufgelöst wurden. |
| Treffer Richtlinie | Die Gesamtzahl (täglich) von Nachrichten von Exchange-, Teams-und Drittanbieter-Datenquellen, die mit einem oder mehreren Bedingungen übereinstimmten, die in einer Aufsichtsrichtlinie definiert sind. |
| Im Zuständigkeitsbereich | Die Gesamtzahl (täglich) von Nachrichten von Exchange-, Teams-und Drittanbieter-Datenquellen, die von einer Aufsichtsrichtlinie überprüft wurden. |
| Gelöst | Die Gesamtanzahl von Nachrichten von Exchange, Teams und Drittanbieter-Datenquellen, die als **aufgelöst** klassifiziert wurden.|

> [!NOTE]
> Aufsichtsrichtlinien müssen zuerst eingerichtet werden, bevor Sie in diesem Bericht angezeigt werden. Wenn Richtlinien gelöscht werden, werden außerdem Verlaufsdaten angezeigt. Sie werden jedoch als "nicht vorhandene Richtlinie" angezeigt, und die **Export** Funktion ist nicht verfügbar.

## <a name="audit"></a>Audit

In einigen Fällen müssen Sie den Zulassungs Prüfern Informationen zur Verfügung stellen, um die Überwachung der Aktivitäten und der Kommunikation von Mitarbeitern nachzuweisen. Dabei kann es sich um eine Zusammenfassung aller Aufsichtsaktivitäten handeln, die mit einer definierten Richtlinie oder zu jeder Zeit geändert oder aktualisiert werden. Aufsichtsrichtlinien verfügen über integrierte Überwachungspfade für die vollständige Bereitschaft für interne oder externe Überprüfungen. Der Nachweis der Aufsichtsverfahren wird mit einem detaillierten Überwachungsverlauf jeder von ihren Aufsichtsrichtlinien überwachten Aktion demonstriert.

Die folgenden Aufsichtsrichtlinien Aktivitäten werden in den Unified Office 365-Überwachungsprotokollen überwacht und zur Verfügung gestellt:

|**Aktivität**|**Zugeordnete Befehle**|
|:-----|:-----|
| Erstellen einer Richtlinie | [New-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2) <br> [New-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule) |
| Bearbeiten einer Richtlinie | [Set-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2) <br> [Set-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule) |
| Löschen einer Richtlinie| [Remove-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2) |
| Anzeigen einer Richtlinie | [Get-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2) |

Anzeigen von Überwachungsaktivitäten im vereinheitlichten Überwachungsprotokoll oder mit dem PowerShell-Cmdlet " [Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) ".

Das folgende Beispiel gibt beispielsweise die Aktivitäten für alle Aufsichts Überprüfungen (Richtlinien und Regeln) zurück und listet detaillierte Informationen zu jedem:

```
Search-UnifiedAuditLog -StartDate 3/1/2019 -EndDate ([System.DateTime]::Now) -RecordType DataGovernance -ResultSize 5000 | Where-Object {$_.Operations -like "*SupervisoryReview*"}  | fl CreationDate,Operations,UserIds,AuditData
```

Zusätzlich zu den in den Überwachungsberichten und-Protokollen bereitgestellten Informationen können Sie auch das PowerShell [-Cmdlet Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity?view=exchange-ps) verwenden, um eine vollständige detaillierte Auflistung aller Aufsichtsrichtlinien Aktivitäten zurückzugeben.

## <a name="ready-to-get-started"></a>Sind Sie bereit zu beginnen?

Informationen zum Konfigurieren von Aufsichtsrichtlinien für Ihre Organisation finden Sie unter [Konfigurieren von Aufsichtsrichtlinien](configure-supervision-policies.md).