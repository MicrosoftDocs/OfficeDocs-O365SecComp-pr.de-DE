---
title: Übersicht über Richtlinien zur Verhinderung von Datenverlust
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/29/2019
ms.audience: ITPro
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MET150
description: Mit einer DLP-Richtlinie (Data Loss Prevention, Datenverlust Verhinderung) im Office 365 Security &amp; Compliance Center können Sie vertrauliche Informationen in Office 365 identifizieren, überwachen und automatisch schützen.
ms.openlocfilehash: 4117a99afc804fd397deb45087c5058077f9ff60
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000018"
---
# <a name="overview-of-data-loss-prevention-policies"></a>Übersicht über Richtlinien zur Verhinderung von Datenverlust

Um Geschäftsstandards und branchenspezifische Vorschriften einzuhalten, müssen Organisationen vertrauliche Informationen schützen und verhindern, dass sie versehentlich offengelegt werden. Beispiele für vertrauliche Informationen, bei denen Sie verhindern möchten, dass sie Ihre Organisation verlassen, sind Finanzdaten oder personenbezogene Informationen (PII) wie Kreditkartennummern, Sozialversicherungsnummern oder Gesundheitsakten. Mit einer DLP-Richtlinie (Data Loss Prevention, Datenverlust Verhinderung) im Office 365 Security &amp; Compliance Center können Sie vertrauliche Informationen in Office 365 identifizieren, überwachen und automatisch schützen.
  
Mit einer DLP-Richtlinie haben Sie die folgenden Möglichkeiten:
  
- **Identifizieren Sie vertrauliche Informationen über viele Standorte hinweg, beispielsweise Exchange Online, SharePoint Online, OneDrive for Business und Microsoft Teams.**
    
    Sie können beispielsweise ein beliebiges Dokument mit einer Kreditkartennummer identifizieren, die in einer OneDrive for Business-Website gespeichert ist, oder Sie können nur die OneDrive-Websites bestimmter Personen überwachen.
    
- **Verhindern, dass vertrauliche Informationen unbeabsichtigt weitergegeben werden**. 
    
    Sie können beispielsweise alle Dokumente oder e-Mails identifizieren, die einen Integritätsdaten Satz enthalten, der für Personen außerhalb Ihrer Organisation freigegeben ist, und dann den Zugriff auf dieses Dokument automatisch blockieren oder verhindern, dass e-Mails gesendet werden.
    
- **Überwachen und schützen Sie vertrauliche Informationen in den Desktop Versionen von Excel, PowerPoint und Word.**
    
    Genau wie in Exchange Online, SharePoint Online und OneDrive for Business verfügen diese Office-Desktop Programme über dieselben Funktionen, um vertrauliche Informationen zu identifizieren und DLP-Richtlinien anzuwenden. DLP bietet eine kontinuierliche Überwachung, wenn Personen Inhalte in diesen Office-Programmen freigeben.
    
- **Helfen Sie den Benutzern dabei, zu erfahren, wie sie die Anforderungen erfüllen, ohne dabei ihren Arbeitsablauf unterbrechen zu müssen.**
    
    Sie können die Benutzer über DLP-Richtlinien informieren und sie dabei unterstützen, den Anforderungen gerecht zu werden, ohne dass dies ihre Arbeit beeinträchtigt. Wenn ein Benutzer z. B. versucht, ein Dokument mit vertraulichen Informationen freizugeben, kann eine DLP-Richtlinie eine E-Mail-Benachrichtigung senden und dem Benutzer einen Richtlinientipp im Kontext der Dokumentbibliothek anzeigen, welche ihm das Außerkraftsetzen erlaubt, wenn er über eine geschäftliche Rechtfertigung verfügt. Die gleichen Richtlinien Tipps werden auch in Outlook im Web, Outlook, Excel, PowerPoint und Word angezeigt.
    
- **Zeigen Sie DLP-Berichte mit Inhalten an, die mit den DLP-Richtlinien Ihrer Organisation übereinstimmen.**
    
    Um die Einhaltung einer DLP-Richtlinie in Ihrer Organisation zu beurteilen, können Sie ermitteln, wie viele Übereinstimmungen jede Richtlinie und Regel in einem Zeitraum aufweist. Wenn eine DLP-Richtlinie es Benutzern ermöglicht, einen richtlinientipp außer Kraft zu setzen und ein falsch positives Ergebnis zu melden, können Sie auch anzeigen, was Benutzer gemeldet haben.
    
Sie erstellen und verwalten DLP-Richtlinien auf der Seite zur Verhinderung von Daten &amp; Verlust im Office 365 Security Compliance Center.
  
![Seite zur Verhinderung von Datenverlust im &amp; Office 365 Security Compliance Center](media/943fd01c-d7aa-43a9-846d-0561321a405e.png)
  
## <a name="what-a-dlp-policy-contains"></a>Inhalt einer DLP-Richtlinie

Eine DLP-Richtlinie enthält einige grundlegende Punkte:
  
- Wo die Inhalts **Speicherorte** wie Exchange Online, SharePoint Online und OneDrive for Business-Websites sowie Microsoft Teams-Chats und-Kanäle geschützt werden sollen. 
    
- Wann und wie die Inhalte durch Durchsetzen von **Regeln** geschützt werden sollen, die Folgendes umfassen: 
    
  - **Bedingungen** , die der Inhalt erfüllen muss, bevor die Regel erzwungen wird-beispielsweise suchen Sie nur nach Inhalten, die Sozialversicherungsnummern enthalten, die für Personen außerhalb Ihrer Organisation freigegeben wurden. 
    
  - **Aktionen**, die von der Regel automatisch durchgeführt werden sollen, wenn diesen Bedingungen entsprechender Inhalt gefunden wird. Es kann dann zum Beispiel der Zugriff auf das Dokument gesperrt und sowohl an den Benutzer als auch den Compliance Officer eine entsprechende E-Mail-Benachrichtigung gesendet werden. 
    
Sie können eine Regel verwenden, um eine bestimmte Schutzanforderung zu erfüllen, und dann mithilfe einer DLP-Richtlinie gemeinsame Schutzanforderungen gruppieren, beispielsweise alle Regeln, die erforderlich sind, um eine bestimmte Verordnung einzuhalten.
  
Sie haben beispielsweise eine DLP-Richtlinie, die Ihnen hilft, das vorhanden sein von Informationen zu erfassen, die dem Krankenversicherungs-und Verantwortlichkeits-Act (HIPAA) unterliegen. Diese DLP-Richtlinie kann dazu beitragen, HIPAA-Daten (was) in allen SharePoint Online-Websites und allen OneDrive für Business-Websites zu schützen, indem ein Dokument mit diesen vertraulichen Informationen gefunden wird, das für Personen außerhalb Ihrer Organisation freigegeben ist (die Bedingungen) und dann den Zugriff auf das Dokument und das Senden einer Benachrichtigung (die Aktionen). Diese Anforderungen werden als einzelne Regeln gespeichert und als DLP-Richtlinie gruppiert, um die Verwaltung und Berichterstellung zu vereinfachen.
  
![Diagramm zeigt DLP-Richtlinie enthält Standorte und Regeln](media/c006860c-2d00-42cb-aaa4-5b5638d139f7.png)
  
### <a name="locations"></a>Speicherorte

Eine DLP-Richtlinie kann vertrauliche Informationen in Office 365 finden und schützen, unabhängig davon, ob sich diese Informationen in Exchange Online, SharePoint Online, OneDrive for Business oder Microsoft Teams befinden. Sie können Inhalte in Exchange-e-Mails, Microsoft Teams-Chats und-Kanälen sowie alle SharePoint-oder OneDrive-Bibliotheken schützen oder bestimmte Speicherorte für eine Richtlinie auswählen.
  
![Optionen für Speicherorte, an denen eine DLP-Richtlinie angewendet werden kann](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
Beachten Sie, dass eine DLP-Richtlinie nicht mehr als 100 solche Einschlüsse und Ausschlüsse enthalten kann, wenn Sie bestimmte SharePoint-Websites oder OneDrive-Konten einschließen oder ausschließen. Obwohl dieser Grenzwert vorliegt, können Sie diesen Grenzwert überschreiten, indem Sie entweder eine organisationsweite Richtlinie oder eine Richtlinie anwenden, die für gesamte Standorte gilt.
  
### <a name="rules"></a>Regeln

Durch Regeln werden Ihre geschäftlichen Anforderungen an den Inhalt Ihrer Organisation durchgesetzt. Eine Richtlinie enthält eine oder mehrere Regeln, und jede Regel besteht aus Bedingungen und Aktionen. Wenn die Bedingungen der einzelnen Regeln erfüllt sind, werden automatisch die entsprechenden Aktionen ausgeführt. Regeln werden sequenziell ausgeführt, beginnend mit der Regel mit der höchsten Priorität in jeder Richtlinie.
  
Eine Regel bietet auch Optionen zum Benachrichtigen von Benutzern (mit Richtlinien Tipps und e-Mail-Benachrichtigungen) und Administratoren (bei e-Mail-Vorfall Berichten), denen der Inhalt der Regel entspricht.
  
Hier sind die Komponenten einer Regel, die jeweils unten erläutert werden.
  
![Abschnitte des DLP-Regel-Editors](media/1859d504-b9c2-45ed-961b-a0092251acc2.png)
  
#### <a name="conditions"></a>Bedingungen

Bedingungen sind wichtig, da Sie festlegen, welche Arten von Informationen Sie suchen und wann eine Aktion ausgeführt werden soll. Sie können beispielsweise festlegen, dass Inhalte mit Passport-Nummern ignoriert werden, es sei denn, der Inhalt enthält mehr als zehn solcher Nummern und wird für Personen außerhalb Ihrer Organisation freigegeben.
  
Die Bedingungen konzentrieren sich auf den **Inhalt**, beispielsweise auf die Art der vertraulichen Informationen, die Sie suchen, und auch auf den **Kontext**, wie zum Beispiel, mit wem das Dokument geteilt wird. Sie können Bedingungen verwenden, um verschiedenen Risikostufen verschiedene Aktionen zuzuweisen – beispielsweise sind vertrauliche Inhalte, die intern freigegeben werden, möglicherweise geringeres Risiko und erfordern weniger Aktionen als vertrauliche Inhalte, die für Personen außerhalb der Organisation freigegeben werden. 
  
![Liste mit verfügbaren DLP-Bedingungen](media/0fa43f90-d007-4506-ae93-43e8424fe103.png)
  
Mit den derzeit verfügbaren Bedingungen können Sie ermitteln, ob:
  
- Inhalt enthält eine Art vertraulicher Informationen.
    
- Inhalt enthält eine Bezeichnung. Weitere Informationen finden Sie im folgenden Abschnitt [Verwenden einer Bezeichnung als Bedingung in einer DLP-Richtlinie](#using-a-label-as-a-condition-in-a-dlp-policy).
    
- Inhalte für Personen außerhalb oder innerhalb der Organisation freigegeben werden.
    
#### <a name="types-of-sensitive-information"></a>Arten von vertraulichen Informationen

Eine DLP-Richtlinie kann dazu beitragen, vertrauliche Informationen zu schützen ****, die als vertraulicher Informationstyp definiert sind. Office 365 enthält Definitionen für viele allgemeine vertrauliche Informationstypen in vielen verschiedenen Regionen, die Sie verwenden können, beispielsweise eine Kreditkartennummer, Kontonummern, nationale ID-Nummern und Passport-Nummern. 
  
![Liste der verfügbaren Typen für vertrauliche Informationen](media/3eaa9911-bc94-44be-902f-363dbf3b07fe.png)
  
Wenn eine DLP-Richtlinie nach einem vertraulichen Informationstyp wie einer Kreditkartennummer sucht, sucht er nicht einfach nach einer 16-stelligen Nummer. Jede Art vertraulicher Informationen wird durch eine Kombination der folgenden Elemente definiert und anhand dieser ermittelt:
  
- Schlüsselwörter
    
- Interne Funktionen zur Überprüfung der Prüfsummen oder Zusammensetzung
    
- Auswertung regulärer Ausdrücke zum Suchen von Musterübereinstimmungen
    
- Andere Inhaltsuntersuchungsmethoden
    
Dies hilft bei der DLP-Erkennung bei gleichzeitiger Reduzierung der Anzahl falsch positiver Ergebnisse, die die Arbeit von Völkern unterbrechen können.
  
#### <a name="actions"></a>Aktionen

Wenn der Inhalt einer Bedingung in einer Regel entspricht, können Sie Aktionen anwenden, um den Inhalt automatisch zu schützen.
  
![Liste der verfügbaren DLP-Aktionen](media/8aef17fc-1e99-4ac7-adfc-0f2c9c1a0697.png)
  
Mit den jetzt verfügbaren Aktionen können Sie Folgendes tun:
  
- **Einschränken des Zugriffs auf Inhalte** Für Websiteinhalte bedeuten dies, dass Berechtigungen für das Dokument für alle Benutzer eingeschränkt sind, mit Ausnahme des primären Websitesammlungsadministrators, des Dokumentbesitzers und der Person, die das Dokument zuletzt geändert hat. Diese Personen können die vertraulichen Informationen aus dem Dokument entfernen oder eine andere Aktion ausführen. Wenn das Dokument den Anforderungen entspricht, werden die ursprünglichen Berechtigungen automatisch wiederhergestellt. Wenn der Zugriff auf ein Dokument gesperrt ist, wird das Dokument in der Bibliothek auf der Website mit einem speziellen Richtlinientipp-Symbol angezeigt. 
    
    ![Richtlinientipp mit Zugriff auf Dokument blockiert](media/b6cefed3-d212-43d7-8534-4b92b26ebd50.png)
  
    Bei e-Mail-Inhalten wird durch diese Aktion verhindert, dass die Nachricht gesendet wird. Je nach Konfiguration der DLP-Regel wird dem Absender ein NDR angezeigt oder (wenn die Regel eine Benachrichtigung verwendet) ein richtlinientipp und/oder eine e-Mail-Benachrichtigung.
    
    ![Warnung, dass nicht autorisierte Empfänger aus der Nachricht entfernt werden müssen](media/302f9994-912d-41e7-861f-8a4539b3c285.png)
  
#### <a name="user-notifications-and-user-overrides"></a>Benutzer Benachrichtigungen und Benutzerüberschreibungen

Sie können Benachrichtigungen und Außerkraftsetzungen verwenden, um Ihre Benutzer über DLP-Richtlinien zu informieren und Sie dabei zu unterstützen, ohne Ihre Arbeit zu blockieren. Wenn ein Benutzer z. B. versucht, ein Dokument mit vertraulichen Informationen freizugeben, kann eine DLP-Richtlinie eine E-Mail-Benachrichtigung senden und dem Benutzer einen Richtlinientipp im Kontext der Dokumentbibliothek anzeigen, welche ihm das Außerkraftsetzen erlaubt, wenn er über eine geschäftliche Rechtfertigung verfügt.
  
![Benutzer Benachrichtigungen und Benutzerüberschreibungen Abschnitte des DLP-Regel-Editors](media/37b560d4-6e4e-489e-9134-d4b9daf60296.png)
  
Die e-Mail kann die Person Benachrichtigen, die den Inhalt gesendet, freigegeben oder zuletzt geändert hat, und für Websiteinhalte der primäre Websitesammlungsadministrator und der Dokumentbesitzer. Außerdem können Sie beliebige Absender hinzufügen oder entfernen, die Sie aus der e-Mail-Benachrichtigung auswählen.
  
Zusätzlich zum Senden einer e-Mail-Benachrichtigung wird in einer Benutzerbenachrichtigung ein richtlinientipp angezeigt:
  
- In Outlook und Outlook im Web.
    
- Für das Dokument auf einer SharePoint Online-oder OneDrive for Business-Website.
    
- In Excel, PowerPoint und Word, wenn das Dokument auf einer Website gespeichert ist, die in einer DLP-Richtlinie enthalten ist.
    
Der e-Mail-Benachrichtigungs-und richtlinientipp erläutert, warum Inhalte mit einer DLP-Richtlinie in Konflikt stehen. Wenn Sie möchten, können die E-Mail-Benachrichtigung und der Richtlinientipp Benutzern das Außerkraftsetzen einer Regel erlauben, indem sie ein falsch positives Ergebnis melden oder eine geschäftliche Begründung angeben. Dadurch können Sie Benutzer über Ihre DLP-Richtlinien informieren und diese umsetzen, ohne dass Benutzer bei der Arbeit behindert werden. Informationen zu Außerkraftsetzungen und falsch positiven Ergebnissen werden auch für Berichte (siehe Hinweise unten zu den DLP-Berichten) protokolliert und in die Schadensberichte (im nächsten Abschnitt) aufgenommen, sodass der Compliance-Beauftragte diese Informationen regelmäßig prüfen kann.
  
So sieht ein richtlinientipp in einem OneDrive for Business-Konto aus.
  
![Richtlinientipp für ein Dokument in einem OneDrive-Konto](media/f9834d35-94f0-4511-8555-0fe69855ce6d.png)
  
#### <a name="incident-reports"></a>Schadensberichte

Wenn eine Regel abgeglichen wird, können Sie einen Vorfall Bericht an Ihren Compliance Officer (oder an alle Personen, die Sie auswählen) mit Details des Ereignisses senden. Dieser Bericht enthält Informationen zu dem Element, das abgeglichen wurde, den tatsächlichen Inhalt, der mit der Regel übereinstimmt, und den Namen der Person, die den Inhalt zuletzt geändert hat. Für e-Mail-Nachrichten enthält der Bericht auch als Anlage die ursprüngliche Nachricht, die einer DLP-Richtlinie entspricht.
  
![Seite zum Konfigurieren von Vorfall Berichten](media/31c6da0e-981c-415e-91bf-d94ca391a893.png)
  
## <a name="grouping-and-logical-operators"></a>Gruppierungs-und logische Operatoren

Häufig muss ihre DLP-Richtlinie eine einfache Anforderung haben, um den gesamten Inhalt zu identifizieren, der eine US-sozialVersicherungsNummer enthält. In anderen Szenarien muss ihre DLP-Richtlinie jedoch möglicherweise mehr lose definierte Daten identifizieren.
  
Um beispielsweise Inhalte zu identifizieren, die dem US-KrankenversicherungsGesetz (HIPAA) unterliegen, müssen Sie Folgendes suchen:
  
- Inhalte, die bestimmte Typen von vertraulichen Informationen enthalten, beispielsweise eine US-sozialVersicherungsNummer oder eine DEA-Nummer.
    
    UND
    
- Schwer zu identifizierende Inhalte, beispielsweise Kommunikation über die Pflege eines Patienten oder Beschreibungen der bereitgestellten medizinischen Dienste. Für die Identifizierung dieses Inhalts sind Schlüsselwörter aus sehr großen Keyword-Listen wie der internationalen Klassifikation von Krankheiten (ICD-9-CM oder ICD-10-CM) erforderlich.
    
Sie können diese lose definierten Daten mithilfe von Gruppierungs-und logischen Operatoren (und, oder) leicht identifizieren. Wenn Sie eine DLP-Richtlinie erstellen, können Sie Folgendes tun:
  
- Gruppieren von vertraulichen Informationstypen.
    
- Wählen Sie den logischen Operator zwischen den Typen vertraulicher Informationen innerhalb einer Gruppe und zwischen den Gruppen selbst aus.
    
### <a name="choosing-the-operator-within-a-group"></a>Auswählen des Operators innerhalb einer Gruppe

Innerhalb einer Gruppe können Sie auswählen, ob eine oder alle der Bedingungen in dieser Gruppe erfüllt sein müssen, damit der Inhalt mit der Regel übereinstimmt.
  
![Gruppe mit den Operatoren innerhalb der Gruppe](media/6a12f1e8-112d-48ee-9a73-82b3dd0542e7.png)
  
### <a name="adding-a-group"></a>Hinzufügen einer Gruppe

Sie können schnell eine Gruppe hinzufügen, die über eigene Bedingungen und Operatoren innerhalb dieser Gruppe verfügen kann.
  
![Schaltfläche "Gruppe hinzufügen"](media/5f72f292-d1f3-4f11-a911-a9f71e10abf6.png)
  
### <a name="choosing-the-operator-between-groups"></a>Auswählen des Operators zwischen Gruppen

Zwischen Gruppen können Sie auswählen, ob die Bedingungen in einer Gruppe oder in allen Gruppen erfüllt sein müssen, damit der Inhalt mit der Regel übereinstimmt.
  
Beispielsweise verfügt die integrierte **U.S. HIPAA** -Richtlinie über eine Regel, die einen **and-** Operator zwischen den Gruppen verwendet, damit Inhalte identifiziert werden, die Folgendes enthalten: 
  
- aus der Gruppe **PII-IDs** (mindestens eine SSN-Nummer **oder** eine DEA-Nummer) 
    
    **AND**
    
- aus der Gruppe **medizinische Ausdrücke** (mindestens ein ICD-9-cm-Schlüsselwort **oder** ein ICD-10-cm-Schlüsselwort) 
    
![Gruppen, die den Operator zwischen Gruppen anzeigen](media/354aa77f-569c-4847-9dfe-605ee2bb28d1.png)
  
## <a name="the-priority-by-which-rules-are-processed"></a>Die Priorität, nach der Regeln verarbeitet werden.

Wenn Sie Regeln in einer Richtlinie erstellen, erhält jede Regel eine Priorität in der Reihenfolge, in der Sie erstellt wurde – Bedeutung, die Regel, die zuerst erstellt wurde, hat die erste Priorität, die Regel, die erstellt wird, zweite Priorität usw. Nachdem Sie eine Regel erstellt haben, kann die Priorität nicht geändert werden, es sei denn, Sie wird gelöscht und neu erstellt.
  
![Regeln in der Prioritätsreihenfolge](media/f7dc06bf-bc6f-485c-bcdb-606edbcf6565.png)
  
Wenn Inhalte anhand von Regeln ausgewertet werden, werden die Regeln in der Reihenfolge der Priorität verarbeitet. Wenn Inhalte mit mehreren Regeln übereinstimmen, werden die Regeln in der Reihenfolge der Priorität verarbeitet, und die restriktivste Aktion wird erzwungen. Wenn der Inhalt beispielsweise mit allen der folgenden Regeln übereinstimmt, wird Regel 3 erzwungen, da es sich um die höchste Priorität, die restriktivste Regel, handelt:
  
- Regel 1: nur benachrichtigt Benutzer
    
- Regel 2: benachrichtigt Benutzer, schränkt den Zugriff ein und ermöglicht Benutzerüberschreibungen
    
- Regel 3: benachrichtigt Benutzer, schränkt den Zugriff ein und lässt keine Benutzerüberschreibungen zu
    
- Regel 4: nur Benachrichtigen von Benutzern
    
- Regel 5: schränkt den Zugriff ein
    
- Regel 6: benachrichtigt Benutzer, schränkt den Zugriff ein und lässt keine Benutzerüberschreibungen zu
    
Beachten Sie in diesem Beispiel, dass Übereinstimmungen für alle Regeln in den Überwachungsprotokollen aufgezeichnet und in den DLP-Berichten angezeigt werden, obwohl nur die restriktivste Regel erzwungen wird.
  
Beachten Sie im Hinblick auf Richtlinien Tipps Folgendes:
  
- Nur der richtlinientipp mit der höchsten Priorität wird angezeigt. Beispielsweise wird ein richtlinientipp aus einer Regel, die den Zugriff auf Inhalte blockiert, über einen richtlinientipp aus einer Regel angezeigt, die einfach eine Benachrichtigung sendet. Dadurch wird verhindert, dass Personen eine Kaskade von Richtlinien Tipps sehen.
    
- Wenn die Richtlinien Tipps in der restriktivsten Regel es Benutzern ermöglichen, die Regel außer Kraft zu setzen, überschreibt diese Regel auch alle anderen Regeln, die mit dem Inhalt übereinstimmten.
    
## <a name="tuning-rules-to-make-them-easier-or-harder-to-match"></a>Optimierungsregeln, damit diese leichter oder schwieriger übereinstimmen können

Nachdem Benutzer ihre DLP-Richtlinien erstellt und aktiviert haben, werden diese Probleme manchmal ausgeführt:
  
- Zu viele Inhalte, bei denen **es sich nicht um** vertrauliche Informationen handelt, entsprechen den Regeln – mit anderen Worten zu viel falsch positiver Ergebnisse. 
    
- Zu wenig Inhalte, die vertrauliche Informationen **sind** , entsprechen den Regeln – anders ausgedrückt, werden die Schutzaktionen nicht für die vertraulichen Informationen erzwungen. 
    
Um diese Probleme zu beheben, können Sie Ihre Regeln optimieren, indem Sie die Anzahl der Instanzen anpassen und die Genauigkeit anpassen, um die Übereinstimmung mit den Regeln für Inhalte zu erschweren. Jeder vertrauliche Informationstyp, der in einer Regel verwendet wird, weist sowohl eine instanzenanzahl als auch eine Übereinstimmungs Genauigkeit auf.
  
### <a name="instance-count"></a>Anzahl der Instanzen

Instanzenanzahl: gibt an, wie viele Vorkommen eines bestimmten Typs vertraulicher Informationen vorhanden sein müssen, damit der Inhalt mit der Regel übereinstimmt. Beispielsweise stimmt der Inhalt mit der unten gezeigten Regel überein, wenn zwischen 1 und 9 Unique U.S. oder U.K. Passport-Nummern werden identifiziert.
  
Beachten Sie, dass die Anzahl der Instanzen nur **eindeutige** Übereinstimmungen für vertrauliche Informationstypen und Schlüsselwörter enthält. Wenn beispielsweise eine e-Mail 10 vorkommen mit derselben Kreditkartennummer enthält, zählen diese 10 vorkommen als eine einzelne Instanz einer Kreditkartennummer. 
  
Um die instanzenanzahl zum Optimieren von Regeln zu verwenden, ist die Vorgehensweise einfach:
  
- Um die Übereinstimmung der Regel zu vereinfachen, verringern **** Sie die Mindestanzahl und/oder die **Maximale** Anzahl. Sie können auch **Max** auf **any** festlegen, indem Sie den numerischen Wert löschen. 
    
- Um die Übereinstimmung der Regel zu vereinfachen, sollten Sie die **Min** -Anzahl verlängern. 
    
NormalerWeise verwenden Sie weniger restriktive Aktionen wie das Senden von Benutzer Benachrichtigungen in einer Regel mit einer niedrigeren Anzahl von Instanzen (beispielsweise 1-9). Und Sie verwenden restriktivere Aktionen wie das Einschränken des Zugriffs auf Inhalte, ohne dass Benutzerüberschreibungen in einer Regel mit einer höheren instanzenanzahl (beispielsweise 10-any) möglich sind.
  
![Instanzenanzahl im Regel-Editor](media/e7ea3c12-72c5-4bb3-9590-c924c665e84d.png)
  
### <a name="match-accuracy"></a>Übereinstimmungs Genauigkeit

Wie oben beschrieben, wird ein vertraulicher Informationstyp mithilfe einer Kombination unterschiedlicher Beweistypen definiert und erkannt. Im Allgemeinen wird ein vertraulicher Informationstyp durch mehrere solcher Kombinationen, die als Muster bezeichnet werden, definiert. Ein Muster, das weniger Beweise erfordert, hat eine niedrigere Übereinstimmungs Genauigkeit (oder Zuverlässigkeitsstufe), während ein Muster, das mehr Nachweise erfordert, eine höhere Übereinstimmungs Genauigkeit (oder Zuverlässigkeitsstufe) aufweist. Weitere Informationen zu den tatsächlichen Mustern und Konfidenz Stufen, die von jedem vertraulichen Informationstyp verwendet werden, finden Sie unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).
  
Der vertrauliche Informationstyp mit dem Namen Kreditkartennummer wird beispielsweisedurch zwei Muster definiert:
  
- Ein Muster mit einer Zuverlässigkeit von 65%, die Folgendes erfordert:
    
  - Eine Zahl im Format einer Kreditkartennummer.
    
  - Eine Zahl, die die Prüfsumme übergibt.
    
- Ein Muster mit einer Zuverlässigkeit von 85%, die Folgendes erfordert:
    
  - Eine Zahl im Format einer Kreditkartennummer.
    
  - Eine Zahl, die die Prüfsumme übergibt.
    
  - Ein Schlüsselwort oder ein Ablaufdatum im richtigen Format.
    
Sie können diese Zuverlässigkeits Stufen (oder Genauigkeit) in ihren Regeln verwenden. NormalerWeise verwenden Sie weniger restriktive Aktionen wie das Senden von Benutzer Benachrichtigungen in einer Regel mit niedrigerer Übereinstimmungs Genauigkeit. Und Sie verwenden restriktivere Aktionen wie das Einschränken des Zugriffs auf Inhalte, ohne Benutzerüberschreibungen zuzulassen, in einer Regel mit höherer Übereinstimmungs Genauigkeit.
  
Beachten Sie, dass bei der Identifizierung eines bestimmten Typs vertraulicher Informationen, wie etwa einer Kreditkartennummer, nur eine einzige Zuverlässigkeitsstufe zurückgegeben wird:
  
- Wenn alle Übereinstimmungen für ein einzelnes Muster gelten, wird die Zuverlässigkeitsstufe für dieses Muster zurückgegeben.
    
- Wenn es für mehrere Muster Übereinstimmungen gibt (d. h., es gibt Übereinstimmungen mit zwei verschiedenen Konfidenz Stufen), wird eine höhere Zuverlässigkeitsstufe als die einzelnen Muster zurückgegeben. Dies ist der heikle Abschnitt. Wenn beispielsweise für eine Kreditkarte sowohl die 65%-als auch die 85%-Muster übereinstimmen, ist die für diesen vertraulichen Informationstyp zurückgegebene Zuverlässigkeitsstufe größer als 90%, da mehr Sicherheit mehr Vertrauen bedeutet.
    
Wenn Sie also zwei sich gegenseitig ausschließende Regeln für Kreditkarten erstellen möchten, eine für die 65%-Übereinstimmung und eine für die Genauigkeit von 85%, würden die Bereiche für die Übereinstimmungs Genauigkeit wie folgt aussehen. Die erste Regel nimmt nur Übereinstimmungen des 65%-Musters auf. Die zweite Regel nimmt Übereinstimmungen mit mindestens einer Übereinstimmung von 85% auf und **kann potenziell** andere Ergebnisse mit geringerer Vertrauens **Ebene** aufweisen. 
  
![Zwei Regeln mit unterschiedlichen Bereichen für die Übereinstimmungs Genauigkeit](media/21bdfe36-7a91-4347-8098-11809a92f9a4.png)
  
Aus diesen Gründen ist die Richtlinie zum Erstellen von Regeln mit unterschiedlichen Übereinstimmungs Genauigkeiten:
  
- Die niedrigste Zuverlässigkeitsstufe verwendet in der Regel den gleichen Wert für **Min** und **Max** (kein Bereich). 
    
- Die höchste Zuverlässigkeitsstufe ist in der Regel ein Bereich von direkt oberhalb der niedrigeren Zuverlässigkeitsstufe bis 100.
    
- Jede zwischen Zuverlässigkeitsstufe reicht in der Regel von direkt über dem niedrigeren Konfidenzniveau auf direkt unter der höheren Zuverlässigkeitsstufe.
    
## <a name="using-a-label-as-a-condition-in-a-dlp-policy"></a>Verwenden einer Bezeichnung als Bedingung in einer DLP-Richtlinie

Sie können eine Bezeichnung erstellen und dann:
  
- **Veröffentlichen** Sie diese, sodass Endbenutzer die Bezeichnung auf Inhalte sehen und manuell anwenden können. 
    
- **Automatisches Anwenden** des Inhalts auf Inhalte, die den ausgewählten Bedingungen entsprechen. 
    
Weitere Informationen zu Bezeichnungen finden Sie unter [Übersicht über Aufbewahrungs Beschriftungen](labels.md).
  
Nachdem Sie eine Bezeichnung erstellt haben, können Sie diese Bezeichnung als Bedingung in ihren DLP-Richtlinien verwenden. Sie können dies beispielsweise tun, weil:
  
- Sie haben eine Bezeichnung namens " **vertraulich**" veröffentlicht, damit Personen in Ihrer Organisation die Bezeichnung manuell auf vertrauliche e-Mails und Dokumente anwenden können. Wenn Sie diese Bezeichnung als Bedingung in ihrer DLP-Richtlinie verwenden, können Sie die **Vertraulichkeit** von vertraulichen Inhalten für Personen außerhalb Ihrer Organisation einschränken. 
    
- Sie haben eine Bezeichnung namens " **Alpine House** " für ein Projekt mit diesem Namen erstellt und diese Bezeichnung dann automatisch auf Inhalte angewendet, die die Schlüsselwörter "Alpine House" enthalten. Wenn Sie diese Bezeichnung als Bedingung in der DLP-Richtlinie verwenden, können Sie den Endbenutzern einen richtlinientipp zeigen, wenn Sie diese Inhalte für eine andere Person außerhalb Ihrer Organisation freigeben möchten. 
    
- Sie haben eine Bezeichnung mit dem Namen **Tax Record**veröffentlicht, damit Ihr Records Manager die Bezeichnung manuell auf Inhalte anwenden kann, die als Datensatz klassifiziert werden müssen. Wenn Sie diese Bezeichnung als Bedingung in der DLP-Richtlinie verwenden, können Sie in Verbindung mit anderen Typen vertraulicher Informationen wie ITINs oder SSNs nach Inhalten mit dieser Bezeichnung suchen. Anwenden von Schutzaktionen auf Inhalte mit dem Namen " **Tax Record**" und erhalten Sie detaillierte Aktivitätsberichte über die DLP-Richtlinie aus den DLP-Berichten und Überwachungsprotokolldaten. 
    
- Sie haben ein Label mit dem Namen **Executive Leadership Team** für die Exchange-Postfächer und OneDrive-Konten einer Gruppe von Führungskräften veröffentlicht. Durch die Verwendung dieser Bezeichnung als Bedingung in der DLP-Richtlinie können Sie sowohl Aufbewahrungs-als auch Schutzaktionen für dieselbe Teilmenge von Inhalten und Benutzern erzwingen. 
    
Mithilfe von Bezeichnungen als Bedingung in ihren DLP-Regeln können Sie SELEKTIVSCHUTZ Aktionen für bestimmte Inhalte, Speicherorte oder Benutzer erzwingen.
  
![Bezeichnungen als Bedingung](media/5b1752b4-a129-4a88-b010-8dcf8a38bb09.png)

### <a name="support-for-sensitivity-labels-is-coming"></a>Unterstützung für Sensitivitäts Beschriftungen kommt

Beachten Sie, dass Sie derzeit nur eine Aufbewahrungs Bezeichnung als Bedingung und keine [Vertraulichkeits Bezeichnung](sensitivity-labels.md)verwenden können. Wir arbeiten derzeit an der Unterstützung für die Verwendung einer Vertraulichkeits Bezeichnung in dieser Bedingung.
  
### <a name="how-this-feature-relates-to-other-features"></a>Beziehung zwischen diesem Feature und anderen Features

Auf Inhalte mit vertraulichen Informationen können mehrere Features angewendet werden:
  
- Eine [Aufbewahrungs Bezeichnung](labels.md#applying-a-retention-label-automatically-based-on-conditions) und eine [Aufbewahrungsrichtlinie](retention-policies.md) können sowohl **Aufbewahrungs** Aktionen für diesen Inhalt erzwingen. 
    
- Eine DLP-Richtlinie kann **Schutz** Aktionen für diesen Inhalt erzwingen. Vor dem Erzwingen dieser Aktionen kann eine DLP-Richtlinie zusätzlich zu den Inhalten, die eine Bezeichnung enthalten, weitere Bedingungen erfordern. 
    
![Diagramm der Features, die auf vertrauliche Informationen angewendet werden können](media/dd410f97-a3a3-455c-a1e9-7ed8ae6893d6.png)
  
Beachten Sie, dass eine DLP-Richtlinie eine umfassendere Erkennungsfunktion aufweist als eine Bezeichnung oder Aufbewahrungsrichtlinie, die auf vertrauliche Informationen angewendet wird. Eine DLP-Richtlinie kann Schutzmaßnahmen für Inhalte erzwingen, die vertrauliche Informationen enthalten, und wenn die vertraulichen Informationen aus dem Inhalt entfernt werden, werden diese Schutzaktionen beim nächsten Scannen des Inhalts rückgängig gemacht. Wenn jedoch eine Aufbewahrungsrichtlinie oder Bezeichnung auf Inhalte angewendet wird, die vertrauliche Informationen enthalten, handelt es sich um eine einmalige Aktion, die auch dann nicht rückgängig gemacht wird, wenn die vertraulichen Informationen entfernt werden.
  
Durch die Verwendung einer Bezeichnung als Bedingung in einer DLP-Richtlinie können Sie sowohl Aufbewahrungs-als auch Schutzaktionen für Inhalte mit dieser Bezeichnung erzwingen. Sie können sich den Inhalt vorstellen, der eine Bezeichnung genau wie Inhalte enthält, die vertrauliche Informationen enthalten – sowohl eine Bezeichnung als auch ein Typ für vertrauliche Informationen sind Eigenschaften, die zum Klassifizieren von Inhalten verwendet werden, damit Sie Aktionen für diese Inhalte erzwingen können.
  
![Diagramm der DLP-Richtlinie mit Bezeichnung als Bedingung](media/4538fd8f-fb74-4743-bc22-a5de33adfebb.png)
  
## <a name="simple-settings-vs-advanced-settings"></a>Einfache Einstellungen im Vergleich zu erweiterten Einstellungen

Wenn Sie eine DLP-Richtlinie erstellen, können Sie zwischen einfachen oder erweiterten Einstellungen wählen:
  
- **Einfache Einstellungen** erleichtern das Erstellen des gängigsten DLP-Richtlinientyps, ohne den Regel-Editor zum Erstellen oder Ändern von Regeln zu verwenden. 
    
- **Erweiterte Einstellungen** verwenden Sie den Regel-Editor, um die vollständige Kontrolle über jede Einstellung für ihre DLP-Richtlinie zu geben. 
    
Machen Sie sich keine Sorgen, im Rahmen der Abdeckungen funktionieren einfache Einstellungen und erweiterte Einstellungen genauso, indem Sie Regeln, die aus Bedingungen und Aktionen bestehen, nur mit einfachen Einstellungen erzwingen. Es ist eine schnelle Möglichkeit zum Erstellen einer DLP-Richtlinie.
  
### <a name="simple-settings"></a>Einfache Einstellungen

Bei weitem ist das am häufigsten verwendete DLP-Szenario das Erstellen einer Richtlinie zum Schutz von Inhalten, die vertrauliche Informationen enthalten, für Personen außerhalb Ihrer Organisation und automatische Abhilfemaßnahmen wie die Einschränkung, wer auf den Inhalt zugreifen kann. Senden von Endbenutzer-oder Administratorbenachrichtigungen und Überwachen des Ereignisses zur späteren Untersuchung. Personen verwenden DLP, um zu verhindern, dass vertrauliche Informationen versehentlich offen gelegt werden.
  
Um dieses Ziel zu erreichen, können Sie beim Erstellen einer DLP-Richtlinie die Option **einfache Einstellungen verwenden**auswählen. Diese Einstellungen bieten alles, was Sie zum Implementieren der gängigsten DLP-Richtlinien benötigen, ohne dass Sie den Regel-Editor verwenden müssen.
  
![DLP-Optionen für einfache und erweiterte Einstellungen](media/33c93824-ead5-43b6-9c3e-fd1630c92a7d.png)
  
### <a name="advanced-settings"></a>Erweiterte Einstellungen

Wenn Sie mehr angepasste DLP-Richtlinien erstellen müssen, können Sie **Erweiterte Einstellungen verwenden**auswählen.
  
In den erweiterten Einstellungen wird der Regel-Editor angezeigt, in dem Sie die vollständige Kontrolle über jede mögliche Option haben, einschließlich der Anzahl der Instanzen und der Genauigkeit (Zuverlässigkeitsstufe) für jede Regel.
  
Wenn Sie schnell zu einem Abschnitt wechseln möchten, klicken Sie auf ein Element in der oberen Navigationsleiste des Regel-Editors, um zu diesem Abschnitt zu gelangen.
  
![Oberes Navigationsmenü des DLP-Regel-Editors](media/c527b97f-ca53-4c79-ad19-1a63be8a8ecc.png)
  
## <a name="dlp-policy-templates"></a>DLP-Richtlinienvorlagen

Der erste Schritt beim Erstellen einer DLP-Richtlinie ist die Auswahl der zu schützenden Informationen. Wenn Sie mit einer DLP-Vorlage beginnen, können Sie die Arbeit des Erstellens einer neuen Regel von Grund auf neu speichern und herausfinden, welche Arten von Informationen standardmäßig enthalten sein sollen. Sie können diese Anforderungen dann hinzufügen oder ändern, um die Regel entsprechend den speziellen Anforderungen Ihrer Organisation zu optimieren.
  
Eine vorkonfigurierte DLP-Richtlinienvorlage kann Ihnen dabei helfen, bestimmte Arten vertraulicher Informationen wie HIPAA-Daten, PCI-DSS-Daten, Gramm-Leach-Bliley Act-Daten oder sogar gebietsschemaspezifische personenbezogene Informationen zu erkennen. Um Ihnen das Auffinden und Schützen gängiger Typen von vertraulichen Informationen zu erleichtern, enthalten die Vorlagen in Office 365 bereits die am häufigsten verwendeten vertraulichen Informationstypen, die Sie zum Einstieg benötigen.
  
![Liste der Vorlagen für Richtlinien zur Verhinderung von Datenverlust mit Fokus auf Vorlage für US-Patriot Act](media/791b2403-430b-4987-8643-cc20abbd8148.png)
  
Ihre Organisation kann auch eigene spezifische Anforderungen erfüllen, in diesem Fall können Sie eine DLP-Richtlinie von Grund auf neu erstellen, indem Sie die Option **benutzerdefinierte Richtlinie** auswählen. Eine benutzerdefinierte Richtlinie ist leer und enthält keine vordefinierten Regeln. 
  
## <a name="roll-out-dlp-policies-gradually-with-test-mode"></a>Allmähliches Bereitstellen von DLP-Richtlinien im Testmodus

Wenn Sie DLP-Richtlinien erstellen, sollten Sie sie erst einmal nach und nach bereitstellen, um die Auswirkungen beurteilen und ihre Effektivität testen zu können, bevor Sie sie vollständig durchsetzen. Sie möchten beispielsweise nicht, dass eine neue DLP-Richtlinie versehentlich den Zugriff auf Tausende Dokumente blockiert, auf die die Benutzer Zugriff haben, um Ihre Arbeit zu erledigen.
  
Wenn Sie DLP-Richtlinien mit einer hohen potenziellen Auswirkung erstellen, empfehlen wir die folgenden Schritte:
  
1. **Starten Sie im Testmodus ohne Richtlinien Tipps** , und verwenden Sie dann die DLP-Berichte und alle vorfallberichte, um die Auswirkungen zu bewerten. In den DLP-Berichten werden die Anzahl von Richtlinienübereinstimmungen, der Ort des Vorkommens, der Typ und der Schweregrad aufgeführt. Auf Grundlage der Ergebnisse können Sie die Regeln nach Bedarf genauer anpassen. Im Testmodus haben DLP-Richtlinien keinen Einfluss auf die Produktivität der Mitarbeiter in Ihrer Organisation. 
    
2. **Fahren Sie im Testmodus mit Benachrichtigungen und Richtlinientipps fort**, sodass Sie die Benutzer über die Einhaltungsrichtlinien in Kenntnis setzen und auf die Anwendung der Regeln vorbereiten können. In dieser Phase können Sie die Benutzer auch bitte, Sie über falsche Positivmeldungen zu benachrichtigen, damit Sie die Regeln noch besser abstimmen können. 
    
3. **Starten Sie die vollständige Erzwingung der Richtlinien** , damit die Aktionen in den Regeln angewendet werden und der Inhalt geschützt ist. Überwachen Sie weiterhin die DLP-Berichte und alle Schadensberichte oder Benachrichtigungen, um sicherzustellen, dass die von Ihnen gewünschten Ergebnisse erzielt werden. 
    
![Optionen für die Verwendung des Testmodus und Aktivieren der Richtlinie](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
Sie können eine DLP-Richtlinie jederzeit deaktivieren, was alle Regeln in der Richtlinie betrifft. Jede Regel kann jedoch auch einzeln deaktiviert werden, indem Sie Ihren Status im Regel-Editor umschalten.
  
![Optionen zum Deaktivieren einer Regel in einer Richtlinie](media/f7b258ff-1b8b-4127-b580-83c6492f2bef.png)
  
## <a name="dlp-reports"></a>DLP-Berichte

Nachdem Sie Ihre DLP-Richtlinien erstellt und aktiviert haben, sollten Sie sicherstellen, dass Sie wie gewünscht funktionieren und Ihnen helfen, die Kompatibilität zu behalten. Mit DLP-Berichten können Sie schnell die Anzahl der Übereinstimmungen mit DLP-Richtlinien und Regeln in einem Zeitraum sowie die Anzahl von falsch positiven Ergebnissen und Außerkraftsetzungen anzeigen. Bei jedem Bericht können Sie diese Übereinstimmungen nach Speicherort und Zeitraum filtern und sogar auf eine bestimmte Richtlinie, Regel oder Aktion einschränken.
  
Mit den DLP-Berichten können Sie geschäftliche Einblicke erhalten und von folgenden Vorteilen profitieren:
  
- Sie können sich auf bestimmte Zeiträume konzentrieren und so mehr über die Gründe für Spitzen und Trends erfahren.
    
- Entdecken Sie Geschäftsprozesse, die die Konformitätsrichtlinien Ihrer Organisation verletzen.
    
- Sie können die geschäftlichen Auswirkungen der DLP-Richtlinien besser nachvollziehen.
    
Darüber hinaus können Sie die DLP-Berichte verwenden, um Ihre DLP-Richtlinien optimieren, wenn sie ausgeführt werden.
  
![Dashboard "Berichte" im Security and Compliance Center](media/6d741252-a0ce-4429-95ba-6c857ecc9a7e.png)
  
## <a name="how-dlp-policies-work"></a>Funktionsweise von DLP-Richtlinien

DLP erkennt vertrauliche Informationen mithilfe einer eingehenden Inhaltsanalyse (nicht nur einer einfachen Textprüfung). Bei dieser eingehenden Inhaltsanalyse werden Schlüsselwortübereinstimmung, Wörterbuchübereinstimmungen, die Auswertung regulärer Ausdrücke, interne Funktionen sowie weitere Inhaltsuntersuchungsmethoden herangezogen, um Inhalte zu erkennen, welche die DLP-Richtlinien erfüllen. Möglicherweise gilt nur ein kleiner Prozentsatz Ihrer Daten als vertraulich. Eine DLP-Richtlinie kann nur diese Daten bestimmen, überwachen und automatisch schützen, ohne Personen zu behindern, die mit den restlichen Inhalten arbeiten.
  
### <a name="policies-are-synced"></a>Richtlinien werden synchronisiert

Nachdem Sie im Security &amp; Compliance Center eine DLP-Richtlinie erstellt haben, wird Sie in einem zentralen Richtlinienspeicher gespeichert und dann mit den verschiedenen Inhaltsquellen synchronisiert, einschließlich:
  
- Exchange Online und von dort zu Outlook im Web und Outlook
    
- OneDrive for Business-Websites
    
- SharePoint Online-Websites
    
- Office-Desktop Programme (Excel, PowerPoint und Word)

- Microsoft Teams-Kanäle und -Chats.
    
Nachdem die Richtlinie mit den richtigen Speicherorten synchronisiert wurde, werden Inhalte ausgewertet und Aktionen erzwungen.
  
### <a name="policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites"></a>Richtlinienauswertung in OneDrive for Business- und SharePoint Online-Websites

In allen SharePoint Online-Websites und OneDrive für Business-Websites werden Dokumente ständig geändert – Sie werden ständig erstellt, bearbeitet, freigegeben und so weiter. Dies bedeutet, dass Dokumente zu jedem Zeitpunkt gegen eine DLP-Richtlinie verstoßen können oder im Gegensatz dazu die DLP-Richtlinie erfüllen können. So kann es zum Beispiel sein, dass eine Person ein Dokument auf die Teamwebsite hochlädt, das keine vertraulichen Informationen enthält, zu einem späteren Zeitpunkt eine andere Person dasselbe Dokument jedoch bearbeitet und vertrauliche Informationen einfügt.
  
Aus diesem Grund überprüfen DLP-Richtlinien Dokumente häufig im Hintergrund auf Richtlinienübereinstimmungen. Sie können sich dies als asynchrone Richtlinienauswertung vorstellen.
  
#### <a name="how-it-works"></a>Funktionsweise
 
Wenn Benutzer Dokumente auf ihren Websites hinzufügen oder ändern, überprüft die Suchmaschine den Inhalt, sodass Sie später danach suchen können. Während dieses Vorgangs wird der Inhalt auch auf vertrauliche Informationen überprüft und überprüft, ob er freigegeben wurde. Alle vertraulichen Informationen, die gefunden werden, werden sicher im Suchindex gespeichert, sodass nur das Compliance-Team darauf zugreifen kann, jedoch keine typischen Benutzer. Jede DLP-Richtlinie, die Sie aktiviert haben, wird im Hintergrund ausgeführt (asynchron), die Suche wird häufig nach Inhalten überprüft, die einer Richtlinie entsprechen, und durch Anwenden von Aktionen, um Sie vor versehentlichen Lecks zu schützen.
  
![Diagramm, das zeigt, wie DLP-Richtlinien Inhalt asynchron auswerten](media/bdf73099-039a-4909-ae89-ac12c41992ba.png)
  
Dokumente können jedoch nicht nur mit einer DLP-Richtlinie in Konflikt stehen, sondern es können auch Änderungen vorgenommen werden, die dazu führen, dass sie nun einer DLP-Richtlinie entsprechen. Wenn eine Person zum Beispiel einem Dokument Kreditkartennummern hinzufügt, kann dies dazu führen, dass die DLP-Richtlinie den Zugriff auf das Dokument automatisch sperrt. Wenn die Person jedoch später die vertraulichen Informationen entfernt, wird die Aktion (in diesem Fall die Sperre) automatisch entfernt, wenn das Dokument das nächste Mal anhand der Richtlinie ausgewertet wird.
  
DLP bewertet alle Inhalte, die indiziert werden können. Weitere Informationen dazu, welche Dateitypen standardmäßig gecrawlt werden, finden Sie unter [standardmäßig durchforstete Dateinamenerweiterungen und analysierte Dateitypen in SharePoint Server](https://docs.microsoft.com/SharePoint/technical-reference/default-crawled-file-name-extensions-and-parsed-file-types).
  
### <a name="policy-evaluation-in-exchange-online-outlook-and-outlook-on-the-web"></a>Richtlinienauswertung in Exchange Online, Outlook und Outlook im Web

Wenn Sie eine DLP-Richtlinie mit Exchange Online als Standort erstellen, wird die Richtlinie vom Office 365 Security &amp; Compliance Center zu Exchange Online und dann von Exchange Online zu Outlook im Web und Outlook synchronisiert.
  
Wenn eine Nachricht in Outlook verfasst wird, kann der Benutzerrichtlinien Tipps anzeigen, während der erstellte Inhalt anhand von DLP-Richtlinien ausgewertet wird. Und nachdem eine Nachricht gesendet wurde, wird Sie anhand von DLP-Richtlinien als normaler Teil des Nachrichtenflusses zusammen mit Exchange-Nachrichtenfluss Regeln (auch bekannt als Transportregeln) und DLP-Richtlinien ausgewertet, die im Exchange Admin Center erstellt werden. DLP-Richtlinien überprüfen sowohl die Nachricht als auch alle Anhänge.
  
### <a name="policy-evaluation-in-the-office-desktop-programs"></a>Richtlinienauswertung in Office-Desktop Programmen

Excel, PowerPoint und Word verfügen über die gleichen Möglichkeiten, vertrauliche Informationen zu identifizieren und DLP-Richtlinien als SharePoint Online und OneDrive for Business anzuwenden. Diese Office-Programme synchronisieren ihre DLP-Richtlinien direkt aus dem zentralen Richtlinienspeicher und bewerten dann kontinuierlich den Inhalt anhand der DLP-Richtlinien, wenn Personen mit Dokumenten arbeiten, die von einer in einer DLP-Richtlinie enthaltenen Website geöffnet werden.
  
Die DLP-Richtlinienevaluierung in Office hat keine Auswirkungen auf die Leistung der Programme oder die Produktivität von Personen, die an Inhalten arbeiten. Wenn Sie an einem umfangreichen Dokument arbeiten oder der Computer des Benutzers ausgelastet ist, kann es einige Sekunden dauern, bis ein richtlinientipp angezeigt wird.

### <a name="policy-evaluation-in-microsoft-teams"></a>Richtlinienauswertung in Microsoft Teams
 
Wenn Sie eine DLP-Richtlinie erstellen, die Microsoft Teams als Standort enthält, wird die Richtlinie vom Office 365 Security &amp; Compliance Center auf Benutzerkonten und Microsoft Teams-Kanäle und-Chats synchronisiert. Je nachdem, wie DLP-Richtlinien konfiguriert werden, kann die Nachricht blockiert oder gesperrt werden, wenn jemand versucht, vertrauliche Informationen in einem Microsoft Teams-Chat oder-Kanal freizugeben. Und Dokumente mit vertraulichen Informationen, die für Gäste (externe Benutzer) freigegeben werden, werden für diese Benutzer nicht geöffnet.

Nehmen wir beispielsweise an, dass jemand versucht, vertrauliche Informationen in einem Teams-Chat oder-Kanal mit externen Benutzern zu teilen. Angenommen, es ist eine DLP-Richtlinie definiert, um dies zu verhindern. Mit geschütztem Schutz werden Nachrichten mit vertraulichen Informationen, die an externe Benutzer gesendet werden, gelöscht. Dies geschieht innerhalb von Sekunden, und es geschieht automatisch, je nachdem, wie die DLP-Richtlinie konfiguriert ist.

Richtlinien Tipps Benachrichtigen Absender darüber, warum Ihre Nachrichten blockiert oder gesperrt wurden. Beispielsweise kann einem Absender mitgeteilt werden, dass seine Nachricht personenbezogene Informationen enthält, die nicht für andere Personen freigegeben werden dürfen, oder dass ein Dokument, das PII enthält, nicht für Benutzer außerhalb Ihrer Organisation freigegeben werden kann. Der Absender kann dann seine Nachricht so bearbeiten, dass Sie mit DLP-Richtlinien kompatibel ist.
 
## <a name="permissions"></a>Berechtigungen

Mitglieder des Compliance-Teams, die DLP-Richtlinien erstellen, benötigen Berechtigungen &amp; für das Security Compliance Center. Standardmäßig hat ihr mandantenadministrator Zugriff auf diesen Standort und kann Compliance-Verantwortlichen und anderen Benutzern Zugriff auf das Security &amp; Compliance Center gewähren, ohne Ihnen alle Berechtigungen eines Mandanten Administrators zu erteilen. Zu diesem Zweck wird Folgendes empfohlen:
  
1. Erstellen Sie eine Gruppe in Office 365, und fügen Sie ihr Compliance Officers hinzu.
    
2. Erstellen Sie auf der Seite **Berechtigungen** des Security &amp; Compliance Center eine Rollengruppe. 
    
3. Fügen Sie die Office 365-Gruppe der Rollengruppe hinzu.
    
Weitere Informationen finden Sie unter [Give users access to the Office 365 Compliance Center](grant-access-to-the-security-and-compliance-center.md).
  
Diese Berechtigungen sind nur erforderlich, um eine DLP-Richtlinie zu erstellen und anzuwenden. Für die Durchsetzung von Richtlinien ist kein Zugriff auf Inhalte erforderlich.
  
## <a name="find-the-dlp-cmdlets"></a>Suchen der DLP-Cmdlets

Um die meisten Cmdlets für das Security &amp; Compliance Center zu verwenden, müssen Sie Folgendes tun:
  
1. [Eine Verbindung zum Office 365 Security &amp; Compliance Center mithilfe von Remote-PowerShell herstellen](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps)
    
2. Verwenden Sie eines der folgenden Cmdlets für [Richtlinien-und Kompatibilitäts-DLP](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/export-dlppolicycollection?view=exchange-ps)
    
DLP-Berichte benötigen jedoch Pull-Daten von über Office 365, einschließlich Exchange Online. Aus diesem Grund stehen **die Cmdlets für die DLP-Berichte in Exchange Online PowerShell zur Verfügung – nicht im &amp; Security Compliance Center PowerShell**. Um die Cmdlets für die DLP-Berichte zu verwenden, müssen Sie daher Folgendes tun:
  
1. [Connect to Exchange Online using remote PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell?view=exchange-ps)
    
2. Verwenden Sie eines dieser Cmdlets für die DLP-Berichte:
    
  - [Get-DlpDetectionsReport](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpDetectionsReport?view=exchange-ps)
    
  - [Get-DlpDetailReport](https://docs.microsoft.com/powershell/module/exchange/policy-and-compliance-dlp/Get-DlpDetailReport?view=exchange-ps)
    
## <a name="more-information"></a>Weitere Informationen

- [Erstellen einer DLP-Richtlinie aus einer Vorlage](create-a-dlp-policy-from-a-template.md)
    
- [Senden von Benachrichtigungen und Anzeigen von Richtlinientipps für DLP-Richtlinien](use-notifications-and-policy-tips.md)
    
- [Erstellen einer DLP-Richtlinie zum Schützen von Dokumenten mit FCI oder anderen Eigenschaften](protect-documents-that-have-fci-or-other-properties.md)
    
- [Inhalt der DLP-Richtlinienvorlagen](what-the-dlp-policy-templates-include.md)
    
- [Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)
    
- [Wonach die DLP-Funktionen suchen](what-the-dlp-functions-look-for.md)
    
- [Erstellen eines benutzerdefinierten vertraulichen Informationstyps](create-a-custom-sensitive-information-type.md)
    

