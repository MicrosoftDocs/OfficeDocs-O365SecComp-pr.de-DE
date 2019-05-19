---
title: Aufsichtsrichtlinien in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
audience: Admin
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
description: Informationen zu Aufsichtsrichtlinien in Office 365
ms.openlocfilehash: 2948cc0440bf481e3f0e90e76a23392233d81cc8
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156477"
---
# <a name="supervision-policies-in-office-365"></a>Aufsichtsrichtlinien in Office 365

Aufsichtsrichtlinien in Office 365 ermöglichen es Ihnen, Mitarbeiter Kommunikationen zur Untersuchung durch designierte Bearbeiter zu erfassen. Sie können bestimmte Richtlinien definieren, die interne und externe e-Mails, Microsoft Teams oder Drittanbieter Kommunikationen in Ihrer Organisation erfassen. Bearbeiter können dann die Nachrichten überprüfen, um sicherzustellen, dass Sie mit den Nachrichtenstandards Ihrer Organisation übereinstimmen und diese mit dem Klassifizierungs lösen. 

Mithilfe dieser Richtlinien können Sie auch viele moderne Anforderungen an die Compliance bewältigen, darunter:

- Überwachen der zunehmenden Typen von Kommunikationskanälen
- Die zunehmende Menge an Nachrichtendaten
- Regulatorische Durchsetzung & das Risiko von Geldbußen

In einigen Organisationen besteht möglicherweise eine Trennung der Aufgaben zwischen der IT-Unterstützung und der Compliance-Verwaltungsgruppe. Office 365 unterstützt die Trennung zwischen der Konfiguration von Aufsichtsrichtlinien Features und der Konfiguration von Richtlinien für aufgezeichnete Kommunikationen. Beispielsweise kann die IT-Gruppe für eine Organisation für die Einrichtung von Rollen Berechtigungen und-Gruppen zuständig sein, um Aufsichtsrichtlinien zu unterstützen, die vom Compliance-Team der Organisation konfiguriert und verwaltet werden.

Eine kurze Übersicht über Aufsichtsrichtlinien finden Sie im [Video zur Aufsichtsrichtlinie](https://youtu.be/C3Y8WZ7o_dI) im [Microsoft Mechanics-Kanal](https://www.youtube.com/user/OfficeGarageSeries).

Weitere Informationen zu Verbesserungen und Verfügbarkeit der Überwachungsfunktionen finden Sie in der [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap).

## <a name="scenarios-for-supervision-policies"></a>Szenarien für Aufsichtsrichtlinien

Aufsichtsrichtlinien können die Überwachung der Kommunikation in Ihrer Organisation in mehreren Bereichen unterstützen:

- **Unternehmensrichtlinien**

    Mitarbeiter müssen in ihrer geschäftsbezogenen Kommunikation angemessene Verwendung, ethische Standards und andere Unternehmensrichtlinien einhalten. Aufsichtsrichtlinien können Richtlinienverstöße erkennen und Sie bei der Durchführung von Korrekturmaßnahmen unterstützen, um diese Art von Vorfällen zu verringern. Beispielsweise können Sie Ihre Organisation auf mögliche Verletzungen von Humanressourcen wie Belästigung oder die Verwendung ungeeigneter oder anstößiger Sprachen in der Mitarbeiterkommunikation überwachen.

- **Risikomanagement**

    Organisationen sind für die gesamte Kommunikation verantwortlich, die über Ihre Infrastruktur und Unternehmensnetzwerk Systeme verteilt ist. Durch die Verwendung von Aufsichtsrichtlinien zur Ermittlung und Verwaltung potenzieller rechtlicher Risiken und Risiken können Risiken minimiert werden, bevor Sie Unternehmensvorgänge beschädigen können. Beispielsweise können Sie Ihre Organisation auf unbefugte Kommunikation für vertrauliche Projekte wie bevorstehende Akquisitionen, Fusionen, Gewinn Offenlegungen, Neuorganisationen oder Änderungen des Führungsteams überwachen.

- **Einhaltung von Vorschriften**

    Die meisten Organisationen müssen im Rahmen ihrer normalen Betriebsverfahren einige Arten von Standards für die Einhaltung gesetzlicher Vorschriften einhalten. In diesen Vorschriften wird häufig gefordert, dass Organisationen einen Aufsichts-oder Überwachungsprozess für Messaging implementieren, der für Ihre Branche geeignet ist. Die Regel 3110 der Financial Industry Regulatory Authority (FINRA) ist ein gutes Beispiel für eine Anforderung an Organisationen, Aufsichtsverfahren für die Überwachung der Aktivitäten Ihrer Mitarbeiter und der Unternehmenstypen, in denen Sie tätig ist, zu überwachen. Ein weiteres Beispiel ist möglicherweise die Notwendigkeit, Broker Händler in Ihrer Organisation zu überwachen, um gegen potenzielle Geldwäsche, Insidergeschäfte, Absprachen oder Bestechungsaktivitäten zu schützen. Aufsichtsrichtlinien können Ihre Organisation bei der Erfüllung dieser Anforderungen unterstützen, indem Sie einen Prozess für die Überwachung und den Bericht über die Unternehmenskommunikation bereitstellen.

## <a name="components"></a>Komponenten

### <a name="supervision-policy"></a>Aufsichtsrichtlinie

Sie erstellen Aufsichtsrichtlinien im Compliance Center. Diese Richtlinien definieren, welche Kommunikation und welche Benutzer in Ihrer Organisation überprüft werden sollen, definieren benutzerdefinierte Bedingungen, denen die Kommunikation entsprechen muss, und geben an, wer Überprüfungen durchführen soll. Benutzer, die in der Rollengruppe "aufsichtsüberprüfung" enthalten sind, können Richtlinien einrichten, und jeder, dem diese Rolle zugewiesen ist, kann im Compliance Center auf die Seite "Beaufsichtigung" zugreifen.

### <a name="supervised-users"></a>Beaufsichtigte Benutzer

Bevor Sie mit der Überwachung beginnen, müssen Sie ermitteln, wer Ihre Kommunikationen überprüfen muss. In der Richtlinie identifizieren Benutzer-e-Mail-Adressen einzelne Personen oder Gruppen von Personen, die überwacht werden sollen. Einige Beispiele für diese Gruppen sind Office 365 Gruppen, Exchange-basierte Verteilerlisten und Microsoft Teams-Kanäle. Sie können auch bestimmte Benutzer oder Gruppen von der Beaufsichtigung mit einer beaufsichtigten Gruppe oder einer Liste von Gruppen ausschließen.

> [!IMPORTANT]
> Benutzer, die von Aufsichtsrichtlinien überwacht werden, müssen über eine Microsoft 365 E5-Konformitäts Lizenz, eine Office 365 Enterprise E3-Lizenz mit dem Add-on für die erweiterte Kompatibilität verfügen oder in einem Office 365 Enterprise E5-Abonnement enthalten sein.
Wenn Sie über keinen vorhandenen Enterprise E5-Plan verfügen und die Überwachung testen möchten, können Sie [sich für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).

### <a name="reviewers"></a>Prüfer

Wenn Sie eine Aufsichtsrichtlinie erstellen, müssen Sie festlegen, wer die Überprüfungen der Nachrichten der überwachten Benutzer durchführen soll. In der Richtlinie identifizieren Benutzer e-Mail-Adressen einzelne Personen oder Gruppen von Personen, um die beaufsichtigte Kommunikation zu überprüfen. Alle Bearbeiter müssen über Postfächer verfügen, die auf Exchange Online gehostet werden.

### <a name="groups-for-supervised-users-and-reviewers"></a>Gruppen für beaufsichtigte Benutzer und Bearbeiter

Um Ihr Setup zu vereinfachen, erstellen Sie Gruppen für Personen, die Ihre Kommunikation überprüfen müssen, sowie Gruppen für Personen, die diese Kommunikationen überprüfen. Wenn Sie Gruppen verwenden, benötigen Sie möglicherweise mehrere. Wenn Sie beispielsweise die Kommunikation zwischen zwei unterschiedlichen Personengruppen überwachen möchten oder wenn Sie eine Gruppe angeben möchten, die nicht überwacht wird.

### <a name="supported-communication-types"></a>Unterstützte Kommunikationstypen

Mit Aufsichtsrichtlinien können Sie festlegen, dass Nachrichten in einer oder mehreren der folgenden Kommunikationsplattformen überwacht werden:

- **Exchange-e-Mail:** Postfächer, die auf Exchange Online als Teil Ihres Office 365 Abonnements gehostet werden, sind für die Nachrichtenüberwachung geeignet. E-Mails und Anhänge, die Aufsichtsrichtlinien Bedingungen entsprechen, stehen sofort für die Überwachung und in Aufsichtsberichten zur Verfügung. Unterstützte Anlagentypen für die Überwachung sind identisch mit den [Dateitypen, die für Exchange-Nachrichtenfluss Regelinhalts Inspektionen unterstützt](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/inspect-message-attachments#supported-file-types-for-mail-flow-rule-content-inspection)werden.
- **Microsoft Teams:** Chatnachrichten und zugehörige Anlagen sowohl in öffentlichen als auch privaten Microsoft Teams-Kanälen und einzelnen Chats können überwacht werden. Microsoft Teams-Chats entsprechende Aufsichtsrichtlinien Bedingungen werden einmal alle 24 Stunden verarbeitet und stehen dann für die Überwachung und in Aufsichtsberichten zur Verfügung. Verwenden Sie die folgenden Gruppen Verwaltungs Konfigurationen, um einzelne Benutzer Chats und Kanal Kommunikationen in Microsoft Teams zu überwachen:

    - **Für Teams-Chat Überwachung:** Zuweisen einzelner Benutzer oder Zuweisen einer [Verteilergruppe](https://support.office.com/article/Distribution-groups-E8BA58A8-FAB2-4AAF-8AA1-2A304052D2DE) zur Aufsichtsrichtlinie Dies gilt für 1-zu-1-oder 1: n-Benutzer/Chat-Beziehungen.
    - **Für Teams-Kanal Kommunikation:** Weisen Sie alle Microsoft Team-Kanal oder Office 365 Gruppe, die Sie überwachen möchten, die einen bestimmten Benutzer für die Aufsichtsrichtlinie enthält. Wenn Sie denselben Benutzer anderen Microsoft Teams-Kanälen oder Office 365 Gruppen hinzufügen, müssen Sie diese neuen Kanäle und Gruppen auch der Aufsichtsrichtlinie hinzufügen.

- **Drittanbieterquellen:** Sie können die Kommunikation von Drittanbieter-Quellen (wie Facebook oder Dropbox) für Daten überwachen, die in Office 365 Postfächer in Ihrer Organisation importiert werden. [Hier erfahren Sie, wie Sie drittanbieterdaten in Office 365 importieren](https://docs.microsoft.com/office365/securitycompliance/archiving-third-party-data).

Auf diesen Plattformen erfasste Kommunikationen werden für jede Richtlinie standardmäßig sieben Jahre lang aufbewahrt, selbst wenn Benutzer Ihre Organisation verlassen und Ihr Postfach gelöscht wird.

### <a name="policy-settings"></a>Richtlinieneinstellungen

#### <a name="direction"></a>Direction

Standardmäßig wird die Bedingung " **Direction** " angezeigt und kann nicht entfernt werden. Die Einstellungen für die Kommunikationsrichtung in einer Richtlinie werden einzeln oder gemeinsam ausgewählt:

- **Eingehend**: Sie können " **eingehend** " auswählen, um die Kommunikation zu überprüfen, die **an** die Personen gesendet wird, die Sie überwachen möchten, **von** Personen, die nicht in die Richtlinie
- **** Ausgehend: Sie **** können ausgehend wählen, wenn Sie die Kommunikation überprüfen möchten, die **von** den Personen gesendet wurde, die Sie für die Überwachung ausgewählt haben, die nicht in der Richtlinie enthalten sind. ****
- **Intern**: Sie können **interne** auswählen, um die Kommunikation zu überprüfen, die **zwischen** den Personen gesendet wird, die Sie in der Richtlinie angegeben haben.

#### <a name="sensitive-information-types"></a>Typen vertraulicher Informationen

Sie haben die Möglichkeit, vertrauliche Informationstypen als Teil ihrer Aufsichtsrichtlinie einzubinden. Vertrauliche Informationstypen sind entweder vordefinierte oder benutzerdefinierte Datentypen, die helfen, Kreditkartennummern, Bank Kontonummern, Passport-Nummern und vieles mehr zu identifizieren und zu schützen. Im Rahmen Office 365 Verhinderung von [Datenverlust (DLP)](data-loss-prevention-policies.md)können mit der Konfiguration vertraulicher Informationen Muster, Zeichen Nähe, Konfidenz Stufen und sogar benutzerdefinierte Datentypen verwendet werden, um Inhalte zu identifizieren und zu kennzeichnen, die möglicherweise vertraulich sind. Die Standardtypen für vertrauliche Informationen sind:

- Finanzen
- Medizin und Gesundheit
- Datenschutz
- Benutzerdefinierter Informationstyp

Weitere Informationen zu Details zu vertraulichen Informationen und zu den Mustern, die in den Standardtypen enthalten sind, finden Sie unter [welche Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).

#### <a name="custom-keyword-dictionaries"></a>Benutzerdefinierte Schlüsselwörter Wörterbücher

Konfigurieren Sie benutzerdefinierte Keyword-Wörterbücher (oder Lexika), um eine einfache Verwaltung von Schlüsselwörtern für Ihre Organisation oder Industrie bereitzustellen. Stichwort Wörterbücher unterstützen bis zu 100.000 Begriffe pro Wörterbuch. Bei Bedarf können Sie mehrere benutzerdefinierte Schlüsselwörter Wörterbücher auf eine einzelne Richtlinie anwenden oder über ein einzelnes Schlüssel Wörterbuch pro Richtlinie verfügen. Diese Wörterbücher werden in einer Aufsichtsrichtlinie zugewiesen und können aus einer Datei (wie einer CSV-oder txt-Liste) oder aus einer Liste, [die Sie im Compliance Center importieren](create-a-keyword-dictionary.md)können, bezogen werden.

#### <a name="offensive-language"></a>Anstößige Sprache

Überwachen von gesendeten oder empfangenen e-Mail-Nachrichten in Ihrer Organisation für anstößige Sprachen Das Modell verwendet eine Kombination aus maschinellem lernen, künstlicher Intelligenz und Stichwörtern, um ungeeignete e-Mail-Nachrichten im Rahmen von Überwachungsanforderungen für Belästigung und Cyber-Mobbing zu identifizieren. Um anstößige Sprachen für andere Kommunikationen in Ihrer Organisation zu verhindern oder zu blockieren, erstellen Sie eine [Richtlinie](create-test-tune-dlp-policy.md) zur Verhinderung von Datenverlust, die ein [benutzerdefiniertes Stichwort Wörterbuch](create-a-keyword-dictionary.md) mit anstößigen Begriffen verwendet

Das Offensive Sprachmodell unterstützt derzeit englische Stichwörter und überwacht den Textkörper von e-Mail-Nachrichten. Das Offensive Sprachmodell überwacht e-Mails nach dem Sentiment, das den folgenden Sprachtypen zugeordnet ist:

|**Typ**|**Beschreibung**|
|:-----|:-----|
| **Weltlichkeiten** | Ausdrücke, die für die meisten Benutzer ungeeignet und peinlich sind. |
| **Bögen** | Ausdrücke, die Kulturen und Ethnien angreifen. |
| **Sticheleien** | Ausdrücke, die verhöhnen, verurteilen und lächerlich machen. |
| **Verweise auf Handicaps** | Ausdrücke, die auf physische oder psychische Nachteile abzielen. |
| **Schmutzige Sprache** | Ausdrücke, die auf sexuelle Interessen und den physikalischen Zustand der Reinheit abzielen. |
| **Phobie** | Ausdrücke, die auf sexuelle Präferenzen abzielen. |
| **Rassismus** | Ausdrücke, die auf Rasse und Ethnizität abzielen. |
| **Extremismus** | Ausdrücke, die auf Religion und politische Ideologien Zielen. |
| **Verschleiern** | Ausdrücke, für die die Bedeutung oder Aussprache identisch mit einem anderen beleidigenden Begriff ist. |
| **Provokative Sprache** | Ausdrücke, die möglicherweise Ärger oder Gewalt verursachen. |
| **Tabu** | Ausdrücke, die in einer höflichen gesellschaftlichen Kommunikation generell nicht geeignet sind. |
| **Nicht verfeinerte Sprache** | Ausdrücke, die keine höflichen Umgangsformen aufweisen und möglicherweise hart und unhöflich sind. |

#### <a name="conditional-settings"></a>Bedingte Einstellungen

Die Bedingungen, die Sie für die Richtlinie wählen, gelten für die Kommunikation sowohl von e-Mails als auch von Drittanbieterquellen in Ihrer Organisation (wie Facebook oder Dropbox).

In der folgenden Tabelle werden die einzelnen Bedingungen näher erläutert.
  
|**Bedingung**|**Verwendung**|
|:-----|:-----|
| **Nachricht wird von einer dieser Domänen empfangen**  <br><br> **Nachricht wird von keiner dieser Domänen empfangen** | Wenn Sie die Richtlinie anwenden möchten, wenn bestimmte Domänen in einer empfangenen Nachricht enthalten oder ausgeschlossen werden, geben Sie die einzelnen Domänen ein, und trennen Sie mehrere Domänen durch ein Komma. Jede Domäne, die Sie eingeben, wird separat angewendet (nur eine dieser Domänen muss für die Richtlinie gelten, die auf die Nachricht angewendet wird). |
| **Nachricht wird an eine dieser Domänen gesendet.**  <br><br> **Nachricht wird nicht an eine dieser Domänen gesendet** | Wenn Sie die Richtlinie anwenden möchten, wenn bestimmte Domänen in einer gesendeten Nachricht enthalten oder ausgeschlossen werden, geben Sie die einzelnen Domänen ein, und trennen Sie mehrere Domänen durch ein Komma. Jede Domäne, die Sie eingeben, wird separat angewendet (nur eine dieser Domänen muss für die Richtlinie gelten, die auf die Nachricht angewendet wird). |
| **Nachricht wird mit einer dieser Bezeichnungen klassifiziert.**  <br><br> **Nachricht ist nicht mit einer dieser Bezeichnungen klassifiziert** | So wenden Sie die Richtlinie an, wenn bestimmte Aufbewahrungs Bezeichnungen in einer Nachricht enthalten oder ausgeschlossen werden. Aufbewahrungs Bezeichnungen müssen separat konfiguriert werden, und die konfigurierten Beschriftungen werden als Teil dieser Bedingung ausgewählt. Jede ausgewählte Bezeichnung wird separat angewendet (nur eine dieser Bezeichnungen muss für die Richtlinie gelten, die auf die Nachricht angewendet wird). Weitere Informationen zum Konfigurieren von Aufbewahrungs Bezeichnungen finden Sie unter [Overview of Retention Labels](https://docs.microsoft.com/office365/securitycompliance/labels).|
| **Nachricht enthält eines dieser Wörter**  <br><br> **Nachricht enthält keines dieser Wörter** | Um die Richtlinie anzuwenden, wenn bestimmte Wörter oder Ausdrücke in einer Nachricht enthalten oder ausgeschlossen werden, geben Sie jedes Wort oder jede Phrase in einer separaten Linie ein. Jede Zeile von Wörtern, die Sie eingeben, werden separat angewendet (nur eine dieser Zeilen muss für die Richtlinie gelten, die auf die Nachricht angewendet wird). Weitere Informationen zum Eingeben von Wörtern oder Ausdrücken finden Sie im nächsten Abschnitt [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
| **Attachment enthält eines dieser Wörter**  <br><br> **Attachment enthält keines dieser Wörter** | Wenn Sie die Richtlinie anwenden möchten, wenn bestimmte Wörter oder Ausdrücke in einer Nachrichtenanlage eingeschlossen oder ausgeschlossen werden (beispielsweise in einem Word-Dokument), geben Sie jedes Wort oder jede Phrase in einer separaten Linie ein. Jede wortlinie, die Sie eingeben, wird separat angewendet (es muss nur eine Linie angewendet werden, damit die Richtlinie auf die Anlage angewendet wird). Weitere Informationen zum Eingeben von Wörtern oder Ausdrücken finden Sie im nächsten Abschnitt [Matching words and phrases to emails or attachments](supervision-policies.md#Matchwords).|
| **Attachment ist einer der folgenden Dateitypen**  <br><br> **Attachment ist keiner dieser Dateitypen** | Geben Sie die Dateierweiterungen ein (beispielsweise. exe oder. pdf), um die Kommunikation zu überwachen, die bestimmte Anlagentypen einschließen oder ausschließen. Wenn Sie mehrere Dateierweiterungen einschließen oder ausschließen möchten, geben Sie diese in separaten Zeilen ein. Damit die Richtlinie angewendet wird, muss nur eine Anlagenerweiterung übereinstimmen.|
| **Nachricht ist größer als**  <br><br> **Die Nachrichtengröße ist nicht größer als** | Zum Überprüfen von Nachrichten, die auf einer bestimmten Größe basieren, verwenden Sie diese Bedingungen, um die maximale oder minimale Größe einer Nachricht anzugeben, bevor Sie überprüft werden kann. Wenn Sie beispielsweise angeben, dass die **Nachrichtengröße größer als** \> **1,0 MB**ist, werden alle Nachrichten mit einer Größe von 1,01 MB überprüft. Sie können Byte, Kilobyte, Megabyte oder Gigabyte für diese Bedingung auswählen.|
| **Anlage ist größer als**  <br><br> **Die Anlage ist nicht größer als** | Um Nachrichten anhand der Größe Ihrer Anlagen zu überprüfen, geben Sie die maximale oder minimale Größe an, die eine Anlage sein kann, bevor die Nachricht und ihre Anlagen überprüft werden können. Wenn Sie beispielsweise **Attachment größer als** \> **2,0 MB**angeben, werden alle Nachrichten mit Anlagen von 2,01 MB und mehr überprüft. Sie können Byte, Kilobyte, Megabyte oder Gigabyte für diese Bedingung auswählen.|
   
##### <a name="matching-words-and-phrases-to-emails-or-attachments"></a>Übereinstimmende Wörter und Ausdrücke in E-Mails oder Anlagen
<a name="Matchwords"></a> Jede wortlinie, die Sie eingeben, wird separat angewendet (es muss nur eine Linie angewendet werden, damit die Richtlinienbedingung auf die e-Mail oder Anlage angewendet wird). Verwenden wir beispielsweise die Bedingung, **Nachricht enthält eines dieser Wörter**mit den Schlüsselwörtern "Banker" und "Insiderhandel" in separaten Zeilen. Die Richtlinie gilt für alle Nachrichten, die das Wort "Banker" oder den Ausdruck "Insiderhandel" enthalten. Nur eins der Wörter oder einer der Ausdrücke muss vorkommen, damit die Richtlinienbedingung zutrifft. Wörter in der Nachricht oder Anlage müssen genau übereinstimmen, die Sie eingeben.
  
##### <a name="enter-multiple-conditions"></a>Eingeben mehrerer Bedingungen

Wenn Sie mehrere Bedingungen eingeben, verwendet Office 365 alle Bedingungen zusammen, um zu bestimmen, wann die Richtlinie auf Kommunikationselemente angewendet werden soll. Wenn Sie mehrere Bedingungen einrichten, müssen alle erfüllt sein, damit die Richtlinie angewendet wird, außer wenn Sie eine Ausnahme eingeben. Sie müssen beispielsweise eine Richtlinie erstellen, die gilt, wenn eine Nachricht das Wort "Trade" enthält und größer als 2 MB ist. Wenn die Nachricht jedoch auch die Wörter "von Contoso Financial genehmigt" enthält, sollte die Richtlinie nicht angewendet werden. In diesem Fall wären also die folgenden drei Bedingungen erfüllt:
  
- **Nachricht enthält eines dieser Wörter**mit den Schlüsselwörtern "Trade"

- Die **Nachrichtengröße ist größer als**, mit dem Wert 2 MB

- **Nachricht enthält keines dieser Wörter**, mit den Schlüsselwörtern "genehmigt von Contoso Financial Team"

#### <a name="review-percentage"></a>Überprüfen des Prozentsatzes

Wenn Sie die zu überprüfende Menge an Inhalten reduzieren möchten, können Sie einen Prozentsatz der gesamten Kommunikation angeben, die einer Aufsichtsrichtlinie unterliegt. Aus dem Gesamtprozentsatz des Inhalts, der den ausgewählten Richtlinienbedingungen entspricht, wird ein Zufalls Beispiel für eine echt Zeitauswahl ausgewählt. Wenn Bearbeiter alle Elemente überprüfen möchten, können Sie in einer Aufsichtsrichtlinie **100%** eingeben.

## <a name="monitor--manage"></a>Überwachen der & verwalten

Es ist einfach, die Ergebnisse ihrer Aufsichtsrichtlinien zu überwachen und ein Auflösungs-Tag anzuwenden. Sie können den Status überprüfter Elemente, der Benutzer und Gruppen unter Aufsicht und der als Bearbeiter festgelegten Benutzer und Gruppen schnell anzeigen.

### <a name="supervision-policy-dashboard"></a>Aufsichtsrichtlinien-Dashboard

Verwenden Sie das Dashboard für Aufsichtsrichtlinien, um Aufsichtsrichtlinien Ergebnisse zu verwalten und ausstehende Elemente aufzulösen. In diesem Dashboard können Bearbeiter Elemente anzeigen, die überprüft werden müssen, Aktionen für ein Element durchführen und die Ergebnisse der zuvor geprüften und aufgelösten Elemente für jede Aufsichtsrichtlinie überprüfen. Sie können auf das Dashboard für Aufsichtsrichtlinien im Compliance Center unter **beaufsichtigen** > *der benutzerdefinierten Richt* > Linie**Öffnen**zugreifen.

#### <a name="dashboard-home"></a>Dashboard-Startseite

Die Dashboard- **Start** Seite verfügt über mehrere Abschnitte, die Ihnen helfen, schnell Maßnahmen für Ihre Aufsichtsrichtlinien durchführen zu können. Hier haben Sie folgende Möglichkeiten:

- Schnelles Überprüfen der ausstehenden und aufgelösten Highlights für die Woche
- Anzeigen einer Liste der überwachten Benutzer und der überwachten Gruppen für die ausgewählte Richtlinie
- Anzeigen einer Liste der Bearbeiter und Überprüfungsteams für die ausgewählte Richtlinie
- Anzeigen der Kommunikationsplattformen für die Richtlinie unter Aufsicht über Inhalte

#### <a name="review-tab"></a>Registerkarte "überprüfen"

Auf der Registerkarte " **überprüfen** " werden die von der ausgewählten Richtlinie identifizierten Elemente klassifiziert und aufgelöst. Hier haben Sie folgende Möglichkeiten:

- Filtern nach ausstehenden, kompatiblen, nicht kompatiblen und fragwürdigen Elementen.
- Kennzeichnen eines einzelnen Elements als konform, nicht kompatibel oder fragwürdig. Sie können auch einen Kommentar mit dem Element aufzeichnen, um die getroffene Markierungs Aktion zu verdeutlichen.
- Massen Markierung mehrerer Elemente als konform, nicht kompatibel oder fragwürdig. Sie können auch einen Kommentar mit mehreren Elementen aufzeichnen, um eine Erläuterung der ausgeführten Markierungs Aktion zu ermöglichen.
- Zeigt den Verlauf der Kennzeichnung für ein einzelnes Element an. Dazu gehören die, die das Element, das Datum und die Uhrzeit der Aktion, das Auflösungs und alle eingeschlossenen Kommentare aufgelöst haben.
- Erneutes Klassifizieren zuvor geprüfter Elemente als konform, nicht kompatibel oder fragwürdig. Sie können auch einen Kommentar mit einem oder mehreren Elementen aufzeichnen, um die vorgenommene umklassifizierungs Aktion zu verdeutlichen.

#### <a name="resolved-items-tab"></a>Registerkarte "aufgelöste Elemente"

Auf der Registerkarte **aufgelöste Elemente** können Bearbeiter alle zuvor aufgelösten Elemente für die ausgewählte Richtlinie anzeigen. Hier haben Sie folgende Möglichkeiten:

- Schnelles anzeigen und Sortieren des Betreffs, des Absenders und des Datums von aufgelösten Elementen
- Anzeigen der Klassifizierung und des Kommentar Verlaufs eines beliebigen ausgewählten Elements

## <a name="reports"></a>Berichte

Verwenden Sie die Überwachungsberichte, um die Überprüfungsaktivität auf der Ebene Richtlinie und Prüfer anzuzeigen. Für jede Richtlinie können Sie auch Live Statistiken zum aktuellen Status der Überprüfungsaktivität anzeigen. Sie können die Überwachungsberichte für folgende Zwecke verwenden:
  
- Stellen Sie sicher, dass Ihre Richtlinien ordnungsgemäß funktionieren.
- Erfahren Sie, wie viele Kommunikationsanforderungen überprüft werden müssen.
- Finden Sie heraus, wie viele Kommunikationen nicht konform sind und welche die Überprüfung übergeben. Anhand dieser Informationen können Sie entscheiden, ob Sie Ihre Richtlinien optimieren oder die Anzahl der Bearbeiter ändern möchten.

### <a name="view-the-supervision-report"></a>Anzeigen des Aufsichts Berichts

1. Melden Sie sich im [Compliance Center](https://compliance.microsoft.com) mit den Anmeldeinformationen für ein Administratorkonto in Ihrer Organisation an, das über Berechtigungen zum Anzeigen von Überwachungsberichten verfügt.
2. Wechseln Sie zu **** \> **Dashboard** "Berichte **** " oder "Beaufsichtigung", um das Widget für Aufsichtsberichte mit einer Zusammenfassung der aktuellen Aufsichtsrichtlinien Aktivität anzuzeigen.
3. Wählen Sie das **Aufsichts** widget aus, um die Seite detaillierter Bericht zu öffnen.

> [!NOTE]
> Wenn Sie nicht auf die Seite **Berichte** zugreifen können, überprüfen Sie, dass Sie ein Mitglied der Rollengruppe aufsichtsüberprüfung sind, wie unter [machen Sie die Überwachung in Ihrer Organisation verfügbar](configure-supervision-policies.md)beschrieben. Mit der Aufnahme in diese Rollengruppe können Sie Aufsichtsrichtlinien erstellen und verwalten und den Bericht ausführen.
  
### <a name="how-to-use-the-report"></a>Verwenden des Berichts

In diesem Bericht werden die einzelnen Richtlinien und die Anzahl der Kommunikationen in jeder Phase des Überprüfungsprozesses aufgelistet. Verwenden Sie den Bericht, um Folgendes zu tun:
  
- Anzeigen von Daten für alle oder bestimmte Richtlinien.
- Anzeigen von Daten, die nach Tag-Typ, Prüfer oder Nachrichtentyp gruppiert sind.
- Exportieren Sie Daten basierend auf dem Aktivitätsdatum, der Richtlinie und den Prüfer Aktivitäten in eine CSV-Datei.
- Filtern von Daten basierend auf dem Aktivitätsdatum, dem Tag-Typ, dem Prüfer und dem Nachrichtentyp.

Im folgenden finden Sie eine Aufschlüsselung der Werte, die in der Spalte **Tag Type** angezeigt werden.
  
|**Tagtyp**|**Was das bedeutet**|
|:-----|:-----|
| **Nicht überprüft** | Die Anzahl der e-Mails, die noch nicht überprüft wurden. Diese e-Mails warten auf die Überprüfung im Dashboard für die Office 365 Aufsicht.
| **Compliant** | Die Anzahl der überprüften und als konform gekennzeichneten e-Mails. Diese Nachrichten benötigen noch eine Lösung. |
| **Fragwürdig** | Die Anzahl der überprüften und fragwürdig markierten e-Mails. Dies dient als Kennzeichnung anderer Bearbeiter, um zu überprüfen, ob eine e-Mail-Konformität untersucht werden muss. Diese Nachrichten benötigen noch eine Lösung. |
| **Nicht kompatibel (aktiv)** | Die Anzahl der nicht kompatiblen e-Mails, die von den Prüfern derzeit untersucht werden. |
| **Nicht kompatibel (aufgelöst)** | Die Anzahl der nicht kompatiblen e-Mails, die von den Prüfern untersucht und aufgelöst wurden. |
| **Treffer Richtlinie** | Die Gesamtzahl (täglich) von Nachrichten von Exchange, Microsoft Teams und Drittanbieter-Datenquellen, die einer oder mehreren in einer Aufsichtsrichtlinie definierten Bedingungen entsprechen. |
| **In Zuständigkeitsbereich** | Die Gesamtzahl (täglich) von Nachrichten von Exchange, von Teams und von Drittanbieter-Datenquellen, die von einer Aufsichtsrichtlinie überprüft wurden. |
| **Resolved** | Die Gesamtzahl der Nachrichten von Exchange, Microsoft Teams und Drittanbieter-Datenquellen, die als **aufgelöst** klassifiziert wurden.|

> [!NOTE]
> Aufsichtsrichtlinien müssen zuerst eingerichtet werden, bevor Sie in diesem Bericht angezeigt werden. Außerdem werden, wenn Richtlinien gelöscht werden, Verlaufsdaten weiterhin angezeigt. Sie werden jedoch als "nicht vorhandene Richtlinie" angezeigt, und die **Export** Funktion ist nicht verfügbar.

## <a name="audit"></a>Überwachungs

In einigen Fällen müssen Sie Aufsichtsbehörden oder Compliance-Prüfern Informationen bereitstellen, um die Überwachung der Aktivitäten und der Kommunikation von Mitarbeitern nachzuweisen. Dies kann eine Zusammenfassung aller Aufsichtsaktivitäten sein, die einer definierten Richtlinie zugeordnet sind, oder wenn sich eine Aufsichtsrichtlinie ändert. Aufsichtsrichtlinien verfügen über integrierte Überwachungspfade für die vollständige Bereitstellung interner oder externer Überprüfungen. Detaillierte Überwachungs Verläufe jeder durch ihre Aufsichtsrichtlinien überwachten Aktion bieten einen Nachweis über Aufsichtsverfahren.

Die folgenden Überwachungsrichtlinien Aktivitäten werden überwacht und in den einheitlichen Office 365 Überwachungsprotokollen zur Verfügung gestellt:

|**Aktivität**|**Zugeordnete Befehle**|
|:-----|:-----|
| **Erstellen einer Richtlinie** | [New-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewpolicyv2) <br> [New-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/new-supervisoryreviewrule) |
| **Bearbeiten einer Richtlinie** | [Gruppe-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewpolicyv2) <br> [Gruppe-SupervisoryReviewRule](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/set-supervisoryreviewrule) |
| **Löschen einer Richtlinie** | [Remove-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/remove-supervisoryreviewpolicyv2) |
| **Anzeigen einer Richtlinie** | [Get-SupervisoryReviewPolicyV2](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance/get-supervisoryreviewpolicyv2) |

Zeigen Sie Überwachungsaktivitäten im einheitlichen Überwachungsprotokoll oder mit dem PowerShell [-Cmdlet Search-UnifiedAuditLog](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-audit/search-unifiedauditlog) an.

Im folgenden Beispiel werden die Aktivitäten für alle Aufsichts Überprüfungsaktivitäten (Richtlinien und Regeln) zurückgegeben, und es werden detaillierte Informationen zu den einzelnen Vorgängen aufgelistet:

```
Search-UnifiedAuditLog -StartDate 3/1/2019 -EndDate ([System.DateTime]::Now) -RecordType DataGovernance -ResultSize 5000 | Where-Object {$_.Operations -like "*SupervisoryReview*"}  | fl CreationDate,Operations,UserIds,AuditData
```

Zusätzlich zu den in den Überwachungsberichten und-Protokollen bereitgestellten Informationen können Sie auch das Cmdlet [Get-SupervisoryReviewActivity](https://docs.microsoft.com/powershell/module/exchange/reporting/get-supervisoryreviewactivity?view=exchange-ps) PowerShell verwenden, um eine vollständige detaillierte Auflistung aller Aufsichtsrichtlinien Aktivitäten zurückzugeben.

## <a name="ready-to-get-started"></a>Sind Sie bereit zu beginnen?

Informationen zum Starten der Konfiguration von Aufsichtsrichtlinien für Ihre Organisation finden Sie unter [configure upvision Policies](configure-supervision-policies.md).