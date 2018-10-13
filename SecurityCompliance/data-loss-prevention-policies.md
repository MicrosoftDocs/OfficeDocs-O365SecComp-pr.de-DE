---
title: Übersicht über Richtlinien zur Verhinderung von Datenverlust
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.DLPLandingPage
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 1966b2a7-d1e2-4d92-ab61-42efbb137f5e
description: Mit einer Data Loss Prevention (DLP) Richtlinie in der Office 365-Sicherheit &amp; Compliance Center, können Sie ermitteln, überwachen und schützen Sie sensible Informationen automatisch über Office 365.
ms.openlocfilehash: c33fe53797f86208e7cd033029949737a5c84d2f
ms.sourcegitcommit: 397a5fe594e4cf4bb64c0c6f233d310ef3cbd922
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "25540421"
---
# <a name="overview-of-data-loss-prevention-policies"></a>Übersicht über Richtlinien zur Verhinderung von Datenverlust

Um Business Normen und aus dem Gesundheitswesen Vorschriften zu erfüllen, müssen Organisationen schützen Sie sensible Informationen und zu verhindern, dass die unbeabsichtigte Weitergabe. Beispiele für vertrauliche Informationen, den Sie möglicherweise verhindern, dass Eindruck außerhalb Ihrer Organisation sind Finanzdaten oder personenbezogene Informationen (PII) wie Kreditkarte Zahlen, Sozialversicherungsnummern oder Health Datensätze. Mit einer Data Loss Prevention (DLP) Richtlinie in der Office 365-Sicherheit &amp; Compliance Center, können Sie ermitteln, überwachen und schützen Sie sensible Informationen automatisch über Office 365.
  
Mit einer DLP-Richtlinie haben Sie die folgenden Möglichkeiten:
  
- **Identifizieren Sie vertraulichen Informationen über viele Standorte, wie Exchange Online, SharePoint Online und OneDrive für Unternehmen.**
    
    Beispielsweise können Sie identifizieren aller Dokumente mit einer Kreditkartennummer an, die in jeder OneDrive for Business-Website gespeichert ist, oder können Sie nur die OneDrive-Websites von bestimmten Personen überwachen.
    
- **Verhindern, dass vertrauliche Informationen unbeabsichtigt weitergegeben werden**. 
    
    Sie können beispielsweise identifizieren beliebiges Dokument oder eine e-Mail mit Unterlagen Integrität mit Personen außerhalb Ihrer Organisation freigegeben werden und dann Zugriff auf das Dokument automatisch blockieren oder blockieren e-Mail gesendet werden.
    
- **Überwachen und Schützen von vertraulichen Informationen in den Desktopversionen von Excel 2016, PowerPoint 2016 und Word 2016.**
    
    Genau wie in Exchange Online, SharePoint Online und OneDrive für Unternehmen, enthalten diese desktop 2016 Office-Programme dieselben Funktionen zum Identifizieren von vertraulichen Informationen und Anwenden von DLP-Richtlinien zur Verfügung. DLP bietet kontinuierliche Überwachung, wenn Personen Inhalte in dieser Office 2016 Programme freigeben.
    
- **Benutzern dabei helfen, zu erfahren, wie sie die Anforderungen erfüllen, ohne dabei ihren Arbeitsablauf unterbrechen zu müssen**
    
    Können Sie Schulen Sie Ihre Benutzer DLP-Richtlinien und können diese kompatible verbleiben, ohne dass ihre Arbeit zu blockieren. Angenommen, wenn ein Benutzer versucht, ein Dokument mit vertraulichen Informationen freigeben, kann eine DLP-Richtlinie beide senden Sie ihnen eine e-Mail-Benachrichtigung und einen richtlinientipp im Kontext der Dokumentbibliothek, die ermöglicht es ihnen, die Richtlinie außer Kraft, wenn sie ein Unternehmen besitzen anzeigen Begründung. Die gleichen richtlinientipps werden auch in Outlook auf dem Web, Outlook 2013 und höher, Excel 2016, 2016 PowerPoint und Word 2016 angezeigt.
    
- **Ansicht DLP-Berichte mit Inhalten, die DLP-Richtlinien Ihrer Organisation entspricht.**
    
    Informationen zum Bewerten, wie Ihre Organisation eine DLP-Richtlinie einhalten ist, können Sie sehen, wie viele jede Richtlinie entspricht und Regel verfügt über einen Zeitraum. Wenn eine DLP-Richtlinie Benutzern ermöglicht, einen richtlinientipp überschreiben und ein falsch positives Ergebnis angeben, können Sie auch anzeigen, welche Benutzer gemeldet haben.
    
Sie erstellen und Verwalten von DLP-Richtlinien auf der Seite Daten Loss Prevention, in die Office 365-Sicherheit &amp; Compliance Center.
  
![Data Loss Prevention Seite in die Office 365-Sicherheit &amp; Compliance Center](media/943fd01c-d7aa-43a9-846d-0561321a405e.png)
  
## <a name="what-a-dlp-policy-contains"></a>Inhalt einer DLP-Richtlinie

Eine DLP-Richtlinie enthält einige grundlegende Punkte:
  
- Wo die Inhalte - **Speicherorte** wie Exchange Online, SharePoint Online und OneDrive for Business-Websites schützen. 
    
- Wann und wie die Inhalte durch Durchsetzen von **Regeln** geschützt werden sollen, die Folgendes umfassen: 
    
  - **Bedingungen** , die der Inhalt übereinstimmen muss, bevor die Regel erzwungen wird – Beispiel aussehen nur nach Inhalten, Sozialversicherungsnummern enthält, der mit Personen außerhalb Ihrer Organisation freigegeben wurde. 
    
  - **Aktionen**, die von der Regel automatisch durchgeführt werden sollen, wenn diesen Bedingungen entsprechender Inhalt gefunden wird. Es kann dann zum Beispiel der Zugriff auf das Dokument gesperrt und sowohl an den Benutzer als auch den Compliance Officer eine entsprechende E-Mail-Benachrichtigung gesendet werden. 
    
Sie können verwenden eine Regel, um eine bestimmte Protection Anforderung erfüllen und klicken Sie dann eine DLP-Richtlinie zum Gruppieren von allgemeinen Schutz Anforderungen, wie alle Regeln erforderlich, um eine bestimmte Vorschriften einhalten verwenden.
  
Sie möglicherweise beispielsweise eine DLP-Richtlinie, die Ihnen das Vorhandensein von Informationen unterliegen den Health Insurance Portability and Accountability Act (HIPAA) erkennt helfen. In diesem DLP-Richtlinie konnte Daten zu schützen HIPAA (was) für alle SharePoint Online-Websites und alle OneDrive for Business-Websites (wo) mithilfe ein Dokuments mit dieser vertraulichen Informationen, die gemeinsam mit Personen außerhalb Ihrer Organisation (die von Entwicklern Conditions) und Sperren des Zugriffs auf das Dokument und Senden einer Benachrichtigung (Aktionen). Diese Anforderungen als einzelne Regeln gespeichert und als eine DLP-Richtlinie zur Vereinfachung der Verwaltung und reporting gruppiert.
  
![Diagramm zeigt, dass DLP-Richtlinie Speicherorte und Regeln enthält](media/c006860c-2d00-42cb-aaa4-5b5638d139f7.png)
  
### <a name="locations"></a>Speicherorte

Eine DLP-Richtlinie finden und schützen Sie sensible Informationen über Office 365, ob diese Informationen in Exchange Online, SharePoint Online oder OneDrive für Unternehmen befindet. Sie können auf einfache Weise auswählen, um alle SharePoint-Websites oder OneDrive-Konten zu schützen nur für bestimmte Standorte oder Konten oder alle Postfächer. Beachten Sie, dass es noch nicht möglich, nur die Postfächer bestimmter Benutzer ausgewählt ist.
  
![Optionen für Speicherorte, an denen eine DLP-Richtlinie angewendet werden kann](media/ee50a61a-e867-4571-a150-3eec8d83650f.png)
  
Beachten Sie, dass bei Auswahl von ein-oder Ausschließen von bestimmten SharePoint-Websites oder OneDrive Konten eine DLP-Richtlinie nicht mehr als 100 enthalten kann diese Inklusionen und Ausschlüsse. Obwohl diese Grenze vorhanden ist, erkennen Sie, dass Sie diesen Grenzwert überschreiten können, durch das Anwenden einer Richtlinie für den gesamten Org oder eine Richtlinie, die für die gesamte Speicherorte gilt.
  
### <a name="rules"></a>Regeln

Regeln sind, was Ihrer geschäftlichen Anforderungen auf der Inhalt Ihrer Organisation zu erzwingen. Eine Richtlinie enthält eine oder mehrere Regeln, und jede Regel besteht aus Bedingungen und Aktionen. Wenn die Bedingungen erfüllt sind, werden die Aktionen für jede Regel automatisch ausgeführt. Regeln werden nacheinander ausgeführt, beginnend mit der höchsten Priorität Regel in den einzelnen Richtlinien.
  
Eine Regel enthält auch Optionen zum Benachrichtigen Sie Benutzer (mit richtlinientipps und e-Mail-Benachrichtigungen) und Administratoren (mit e-Mail-Vorfall Berichte) Inhalt wurde die Regel abgeglichen.
  
Hier sind die Komponenten einer Regel, erläutert jede unten.
  
![Abschnitte des DLP-Regel-Editors](media/1859d504-b9c2-45ed-961b-a0092251acc2.png)
  
#### <a name="conditions"></a>Bedingungen

Bedingungen sind wichtig, da sie bestimmen, welche Arten von Informationen, die Sie benötigen, und wenn eine Aktion. Sie können beispielsweise Content enthaltenden Ausweisnummern ignorieren, es sei denn, der Inhalt mehr als zehn solche Rufnummern enthält und Personen außerhalb Ihrer Organisation freigegeben.
  
Bedingungen konzentrieren Sie sich auf die **Inhalte**, beispielsweise welche Arten von vertraulichen Informationen, Suche nach und auch auf dem **Kontext**, z. B., die das Dokument mit gemeinsam genutzt wird. Können Bedingungen verschiedene Risikoebenen unterschiedliche Aktionen zuweisen – beispielsweise vertrauliche Inhalte intern shared möglicherweise geringeres Risiko und benötigen weniger Aktionen als vertrauliche Inhalte, die gemeinsam mit Personen außerhalb der Organisation. 
  
![Liste mit verfügbaren DLP-Bedingungen](media/0fa43f90-d007-4506-ae93-43e8424fe103.png)
  
Mit den derzeit verfügbaren Bedingungen können Sie ermitteln, ob:
  
- Inhalt enthält einen Typ von vertraulichen Informationen.
    
- Inhalt enthält eine Beschriftung. Weitere Informationen finden Sie unter der weiter unten im Abschnitt [eine Beschriftung als Bedingung in einer DLP-Richtlinie verwenden](data-loss-prevention-policies.md#label).
    
- Inhalte für Personen außerhalb oder innerhalb der Organisation freigegeben werden.
    
#### <a name="types-of-sensitive-information"></a>Arten von vertraulichen Informationen

Eine DLP-Richtlinie schützen vertraulichen Informationen, die als **Typ vertraulicher Informationen**definiert ist. Office 365 enthält Definitionen für viele häufig vertrauliche Informationen über viele verschiedenen Regionen, die Sie, wie eine Kreditkartennummer, Bankkonto Zahlen, national ID-Nummern und Ausweisnummern verwendet werden. 
  
![Liste der verfügbaren Typen vertraulicher Daten.](media/3eaa9911-bc94-44be-902f-363dbf3b07fe.png)
  
Wenn eine DLP-Richtlinie für einen vertrauliche Informationen wie eine Kreditkartennummer aussieht, sieht nicht einfach für eine 16-stellige Zahl aus. Jede Art von vertraulichen Informationen definiert und mit einer Kombination von erkannt:
  
- Schlüsselwörter
    
- Interne Funktionen zur Überprüfung der Prüfsummen oder Zusammensetzung
    
- Auswertung regulärer Ausdrücke zum Suchen von Musterübereinstimmungen
    
- Andere Inhaltsuntersuchungsmethoden
    
Dadurch wird die DLP-Erkennung ein hohes Maß an Genauigkeit beim Reduzieren der Anzahl der falsch positive Ergebnisse, die Personen Arbeit unterbrechen kann zu erzielen.
  
#### <a name="actions"></a>Aktionen

Wenn der Inhalt einer Bedingung in einer Regel übereinstimmt, können Sie Aktionen aus, um den Inhalt automatisch schützen anwenden.
  
![Liste der verfügbaren DLP-Aktionen](media/8aef17fc-1e99-4ac7-adfc-0f2c9c1a0697.png)
  
Die jetzt verfügbaren Aktionen ermöglichen Folgendes:
  
- **Einschränken des Zugriffs auf den Inhalt** Für Websiteinhalte bedeutet dies, dass die Berechtigungen für das Dokument sind für alle Benutzer mit Ausnahme der primärer Administrator der Websitesammlung, der Besitzer des Dokuments und der Person, die das Dokument zuletzt geändert. Diese Personen können vertraulichen Informationen aus dem Dokument entfernen oder eine andere Vertragsstrafen und Aktion ausführen. Wenn das Dokument im Compliance befindet, werden die ursprünglichen Berechtigungen automatisch wiederhergestellt werden. Beim Zugriff auf ein Dokument gesperrt ist, wird das Dokument mit einem speziellen Richtlinie Tipp Symbol in der Bibliothek auf der Website angezeigt. 
    
    ![Richtlinientipp, der zeigt, dass der Zugriff auf das Dokument gesperrt ist.](media/b6cefed3-d212-43d7-8534-4b92b26ebd50.png)
  
    Für e-Mail-Inhalte blockiert diese Aktion die Nachricht gesendet werden. Abhängig, wie die DLP-Regel konfiguriert ist, wird der Absender einen Unzustellbarkeitsbericht angezeigt oder (wenn die Regel eine Benachrichtigung verwendet) eine Richtlinie Tipp und/oder e-Mail-Benachrichtigung.
    
    ![Warnung, dass nicht autorisierte Empfänger aus der Nachricht entfernt werden muss](media/302f9994-912d-41e7-861f-8a4539b3c285.png)
  
#### <a name="user-notifications-and-user-overrides"></a>Benachrichtigungen für Benutzer und Benutzer überschreibt

Sie können die Benachrichtigungen und zum Informieren der Benutzer über die DLP-Richtlinien und können diese kompatible verbleiben, ohne dass ihre Arbeit Blockierung überschreibt. Angenommen, wenn ein Benutzer versucht, ein Dokument mit vertraulichen Informationen freigeben, kann eine DLP-Richtlinie beide senden Sie ihnen eine e-Mail-Benachrichtigung und einen richtlinientipp im Kontext der Dokumentbibliothek, die ermöglicht es ihnen, die Richtlinie außer Kraft, wenn sie ein Unternehmen besitzen anzeigen Begründung.
  
![Benutzer-Benachrichtigungen und Benutzer überschreibt Abschnitte des DLP-Regel-Editors](media/37b560d4-6e4e-489e-9134-d4b9daf60296.png)
  
E-Mail kann diese Person benachrichtigen, die gesendet, freigegebene oder letzten Änderung der Inhalts- und, für Websiteinhalte, der primärer Administrator der Websitesammlung und der Besitzer des Dokuments. Darüber hinaus können Sie hinzufügen oder Entfernen von jedem Benutzer wählen Sie die e-Mail-Benachrichtigung.
  
Zusätzlich zum Senden einer e-Mail-benachrichtigungs, wird eine Benachrichtigung der Benutzer einen richtlinientipp angezeigt:
  
- In Outlook 2013 und höher und Outlook im Web.
    
- Für das Dokument auf einer SharePoint Online oder OneDrive for Business-Site.
    
- In einer DLP-Richtlinie enthalten 2016 PowerPoint und Word 2016, wenn das Dokument auf einer Website gespeichert ist, im Excel-2016.
    
Die e-Mail-Benachrichtigung und richtlinientipp wird erläutert, warum Inhalte mit einer DLP-Richtlinie in Konflikt steht. Wenn Sie auswählen, kann die e-Mail-Benachrichtigung und Richtlinie Spitze Benutzern eine Regel außer Kraft gesetzt, falsch positives Ergebnis melden oder Bereitstellen als Rechtfertigung von ermöglichen. Dies hilft Ihnen informieren Sie Benutzer über DLP-Richtlinien und ohne verhindert, dass Personen ihre Arbeit zu erzwingen. Informationen zu Außerkraftsetzungen und falsch positive Ergebnisse ist auch für die berichterstellung (siehe unten über die DLP-Berichte) angemeldet und in der Vorfall enthalten meldet (nächsten Abschnitt), damit diese Informationen von der Compliance-beauftragte regelmäßig überprüfen kann.
  
Nachfolgend finden Sie ein richtlinientipp in einer OneDrive for Business-Konto aussehen.
  
![Richtlinientipp für ein Dokument in einem OneDrive-Konto](media/f9834d35-94f0-4511-8555-0fe69855ce6d.png)
  
#### <a name="incident-reports"></a>Schadensberichte

Wenn eine Regel erfüllt werden, können Sie einen schadensbericht an Ihre Compliance Officer (oder eine beliebige Personen gewählte) senden, mit Details des Ereignisses. Dieser Bericht enthält Informationen zu den Elementen, die abgeglichen wurde, die tatsächlichen Inhalte, die die Regel und den Namen der Person ein, die den Inhalt der letzten Änderung abgeglichen. Für e-Mail-Nachrichten enthält der Bericht auch als Anlage die ursprüngliche Nachricht, die mit eine DLP-Richtlinie übereinstimmt.
  
![Seite zum Konfigurieren von Vorfallberichten](media/31c6da0e-981c-415e-91bf-d94ca391a893.png)
  
## <a name="grouping-and-logical-operators"></a>Gruppieren und logischen Operatoren

DLP-Richtlinie hat häufig Voraussetzung recht einfach ist, z. B., alle Inhalte zu identifizieren, die eine US-Sozialversicherungsnummer enthält. Jedoch in anderen Szenarien DLP-Richtlinie müssen möglicherweise mehr lose definierte Daten zu identifizieren.
  
Um Inhalte können US Health Insurance Act (HIPAA) zu ermitteln, müssen Sie beispielsweise gesucht:
  
- Inhalte, die bestimmte Arten von vertraulichen Informationen, wie eine US-Sozialversicherungsnummer oder Drug Erzwingung Agency (DEA) Zahl enthält.
    
    AND
    
- Der Inhalt, die schwieriger zu erkennen, wie Communications zu eines Patienten Behandlung oder eine Beschreibung der medizinischen bereitgestellten Dienste ist. Identifizieren von dieser Inhalt erfordert passenden Schlüsselwörter aus dem sehr große Schlüsselwortlisten, z. B. International Klassifizierung der Krankheiten (ICD-9-CM oder ICD-10-CM).
    
Sie können solche lose definierten Daten auf einfache Weise ermitteln Sie mithilfe von Gruppierungs- und logischen Operatoren (AND, OR). Wenn Sie eine DLP-Richtlinie erstellen, können Sie folgende Schritte ausführen:
  
- Typen vertraulicher Informationen zu gruppieren.
    
- Wählen Sie den logischen Operator zwischen den Arten der vertraulichen Informationen innerhalb einer Gruppe und die Gruppen selbst.
    
### <a name="choosing-the-operator-within-a-group"></a>Auswählen des Operators innerhalb einer Gruppe

Innerhalb einer Gruppe können Sie auswählen, ob einige oder alle Aktionen in dieser Gruppe für den Inhalt entsprechend die Regel erfüllt werden müssen.
  
![Gruppe mit den Operatoren in der Gruppe](media/6a12f1e8-112d-48ee-9a73-82b3dd0542e7.png)
  
### <a name="adding-a-group"></a>Hinzufügen einer Gruppe

Sie können schnell eine Gruppe hinzufügen, die was eine eigene Bedingungen und Operator innerhalb der Gruppe haben kann.
  
![Schaltfläche "Gruppe" hinzufügen](media/5f72f292-d1f3-4f11-a911-a9f71e10abf6.png)
  
### <a name="choosing-the-operator-between-groups"></a>Auswählen des Operators zwischen Gruppen

Zwischen Gruppen können Sie auswählen, ob die Bedingungen in nur einer Gruppe oder alle Gruppen für den Inhalt entsprechend die Regel erfüllt werden müssen.
  
Die integrierte **US HIPAA** -Richtlinie verfügt beispielsweise über eine Regel, die einen **AND** -Operator zwischen den Gruppen verwendet, sodass sie Inhalte mit identifiziert: 
  
- aus der Gruppe **PII-IDs** (mindestens eine SSN Rufnummer **oder** DEA) 
    
    **UND**
    
- aus der Gruppe **Medizinischen Begriffen** (mindestens eine ICD-9-CM **oder** ICD-10-CM Schlüsselwort) 
    
![Gruppen mit den Operator zwischen Gruppen](media/354aa77f-569c-4847-9dfe-605ee2bb28d1.png)
  
## <a name="the-priority-by-which-rules-are-processed"></a>Die Priorität von der Regeln verarbeitet werden

Wenn Sie Regeln in einer Richtlinie erstellen, jede Regel wird eine Priorität in der Reihenfolge, in der es d. h. erstellt wird, die Regel erstellt zuerst höchste Priorität hat - zugewiesen, die Regel erstellt Zweitens hat Priorität zweite usw.. Nachdem Sie eine Regel erstellen, die Priorität kann nicht geändert werden, es sei denn, löschen und neu zu erstellen.
  
![Regeln nach Priorität sortiert](media/f7dc06bf-bc6f-485c-bcdb-606edbcf6565.png)
  
Wenn Inhalte Regeln ausgewertet wird, werden die Regeln nach Priorität sortiert verarbeitet. Wenn Inhalte mehrerer Regeln entspricht, werden die Regeln nach Priorität sortiert verarbeitet, und die restriktivste Aktion wird erzwungen. Beispielsweise wenn Inhalte alle folgenden Regeln entspricht, wird Regel 3 erzwungen, da es die höchste Priorität, die am stärksten einschränkende Regel ist:
  
- Regel 1: nur Benutzer benachrichtigt
    
- Regel 2: Benutzer benachrichtigt, schränkt den Zugriff und Außerkraftsetzung für Benutzer
    
- Regel 3: Benutzer benachrichtigt, schränkt den Zugriff und lässt sich nicht auf Benutzer Außerkraftsetzungen
    
- Regel 4: nur Benutzer benachrichtigt
    
- Regel 5: schränkt den Zugriff
    
- Regel 6: Benutzer benachrichtigt, schränkt den Zugriff und lässt sich nicht auf Benutzer Außerkraftsetzungen
    
Beachten Sie in diesem Beispiel, dass Übereinstimmungen für alle Regeln in den Überwachungsprotokollen aufgezeichnet und in der DLP-Berichten angezeigt werden, obwohl nur die restriktivste Regel erzwungen wird.
  
In Bezug auf Tipps zu Richtlinien beachten Sie Folgendes:
  
- Restriktivsten Regel wird nur die richtlinientipp aus der höchsten Priorität, angezeigt. Beispielsweise einen richtlinientipp aus einer Regel, die blockiert den Zugriff auf Inhalt über einen richtlinientipp aus einer Regel angezeigt werden, die einfach eine Benachrichtigung sendet. Dadurch wird verhindert, dass Personen eine Hierarchie von richtlinientipps anzeigen.
    
- Wenn die Richtlinientipps in der restriktivsten Regel Benutzern erlauben, die Regel außer Kraft zu setzen, dann werden durch das Außerkraftsetzen dieser Regel auch alle weiteren Regeln außer Kraft gesetzt, welche mit dem Inhalt übereinstimmten.
    
## <a name="tuning-rules-to-make-them-easier-or-harder-to-match"></a>Optimieren von Regeln zu machen einfacher oder schwieriger zu übereinstimmen

Nach dem Personen erstellen und deren DLP-Richtlinien aktivieren, führen sie in einigen Fällen diese Probleme auftreten:
  
- Zu viel Inhalt, dass vertrauliche Informationen **nicht ist** die Regeln - mit anderen Worten, zu viele falsch positive Ergebnisse übereinstimmt. 
    
- Zu wenig Inhalt, dass vertrauliche Informationen **wird** , die Regeln ermittelt – also die Schutzvorrichtungen Aktionen nicht auf den vertraulichen Informationen erzwungen wird. 
    
Um diese Probleme zu beheben, können Sie optimieren Sie Ihre Regeln durch die Anzahl der Instanzen anpassen und um es schwieriger oder entsprechen die Regeln der Inhalt einfacher Genauigkeit übereinstimmen. Jeder vertrauliche Informationen in einer Regel verwendet hat sowohl eine Instanz zählen und Genauigkeit übereinstimmen.
  
### <a name="instance-count"></a>Anzahl der Instanzen

Anzahl der Instanzen bedeutet ganz einfach an, wie viele Vorkommen eines bestimmten Typs vertrauliche Informationen für Inhalte, auf die Regel übereinstimmen vorhanden sein müssen. Inhalt wird beispielsweise die Regel, wenn zwischen 1 und 9 eindeutige USA oder Großbritannien Ausweisnummern identifiziert werden nachfolgend aufgeführten überein.
  
Beachten Sie, dass die Anzahl der Instanzen nur **eindeutige** Übereinstimmungen für Schlüsselwörter und Typen vertraulicher Informationen enthält. Wenn eine e-Mail 10 Vorkommen des gleichen Kreditkartennummer enthält, zählen diese 10 Vorkommen beispielsweise als eine einzelne Instanz eine Kreditkartennummer. 
  
Um die Anzahl der Instanzen verwenden, um die Regeln zu optimieren, ist die Anleitung unkompliziert:
  
- Um die Regel übereinstimmen vereinfachen, verringern Sie die Anzahl der **min** und/oder erhöhen Sie die **maximale** Anzahl. Sie können auch **max** auf **eine beliebige** festlegen durch Löschen der numerische Wert. 
    
- Um die Regel übereinstimmen, erhöhen die Anzahl der **min** erschweren. 
    
In der Regel verwenden Sie weniger restriktive Aktionen, beispielsweise das Senden von Benachrichtigungen für Benutzer, in einer Regel mit einem niedrigeren Anzahl der Instanzen (beispielsweise 1 bis 9). Und restriktivere Aktionen wie Einschränken des Zugriffs auf Inhalte, ohne dass Benutzer überschreibt, in einer Regel mit einer höheren Anzahl der Instanzen (beispielsweise 10 any) verwenden.
  
![Anzahl der Instanz in der Regeleditor](media/e7ea3c12-72c5-4bb3-9590-c924c665e84d.png)
  
### <a name="match-accuracy"></a>Genauigkeit übereinstimmen

Wie oben beschrieben, ein anderes vertrauliche Informationen definiert und mit einer Kombination von unterschiedlichen Elementtypen Nachweis erkannt. Im Allgemeinen ist ein anderes vertrauliche Informationen durch mehrere Kombinationen, Muster aufgerufen definiert. Ein Muster, die weniger Nachweis benötigt hat einen niedrigeren Übereinstimmung Genauigkeit (Confidence Level), während ein Muster an, die erforderlich, dass weitere Nachweise verfügt sind, eine höhere Genauigkeit von Übereinstimmung (oder Confidence Level). Weitere Informationen zu den tatsächlichen Muster und Confidence Levels verwendet, die für jede Art von vertraulichen Informationen finden Sie unter [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).
  
Beispielsweise ist der Typ vertraulicher Informationen mit dem Namen Kreditkartennummer durch zwei Muster definiert:
  
- Ein Muster mit 65 % vertrauen, die erforderlich sind:
    
  - Eine Zahl im Format einer Kreditkartennummer an.
    
  - Eine Zahl, die die Prüfsumme übergibt.
    
- Ein Muster mit 85 % vertrauen, die erforderlich sind:
    
  - Eine Zahl im Format einer Kreditkartennummer an.
    
  - Eine Zahl, die die Prüfsumme übergibt.
    
  - Ein Schlüsselwort oder ein Ablaufdatum im richtigen Format.
    
Sie können mithilfe dieser Confidence Levels (oder Übereinstimmung Genauigkeit) in Ihren Regeln. In der Regel verwenden Sie weniger restriktive Aktionen, beispielsweise das Senden von Benachrichtigungen für Benutzer, in einer Regel mit niedriger Übereinstimmung Genauigkeit. Und restriktivere Aktionen wie Einschränken des Zugriffs auf Inhalte, ohne dass Benutzer überschreibt, in einer Regel mit einer höheren Übereinstimmung Genauigkeit verwenden.
  
Es ist wichtig zu verstehen, dass, wenn im Inhalt ein bestimmtes Typs von vertraulichen Informationen, wie eine Kreditkartennummer identifiziert wird, nur einen einzigen Vertrauensstufe zurückgegeben wird:
  
- Wenn alle der Übereinstimmungen für ein einzelnes Muster sind, wird die Vertrauensebene für diese Muster zurückgegeben.
    
- Wenn es Übereinstimmungen für mehr als ein Muster gibt (d. h., es sind Übereinstimmungen mit zwei verschiedenen Confidence Level), eine Confidence Level höher ist als mindestens eines der einzelnen Muster allein wird zurückgegeben. Dies ist die Schwierigkeit. Beispielsweise wenn sowohl die 65 % und 85 % Muster übereinstimmen, zurückgegeben für eine Kreditkarte die Vertrauensstufe für, dass vertrauliche Informationstyp, da weitere Nachweise mehr vertrauen bedeutet, dass mehr als 90 % ist.
    
Wenn Sie zwei sich gegenseitig ausschließende Regeln für Kreditkarte, eine für die Übereinstimmung 65 % Genauigkeit und eine für die Genauigkeit 85 % Übereinstimmung erstellen möchten würde die Bereiche für die Übereinstimmung Genauigkeit wie folgt aussehen. Die erste Regel nimmt nur Übereinstimmungen des Musters 65 %. Die zweite Regel aufnimmt entspricht mit **mindestens** 85 % abgleichen und **potenziell haben können** andere Zeiteinheiten Confidence entspricht. 
  
![Zwei Regeln mit unterschiedlichen Bereichen für die Übereinstimmung Genauigkeit](media/21bdfe36-7a91-4347-8098-11809a92f9a4.png)
  
Aus diesen Gründen wird die Anleitung zum Erstellen von Regeln mit unterschiedlichen Übereinstimmung Genauigkeitsgraden:
  
- Die niedrigste Vertrauensstufe verwendet den gleichen Wert in der Regel für die **Funktionen min** und **max** (nicht auf einen Bereich). 
    
- Die höchste Vertrauensstufe ist in der Regel ein Bereich von direkt über die unteren Vertrauensstufe bis 100.
    
- Alle dazwischen liegenden Confidence Levels im Bereich in der Regel von direkt über die unteren Vertrauensstufe unterhalb der höheren Vertrauensstufe einfach.
    
## <a name="using-a-label-as-a-condition-in-a-dlp-policy"></a>Verwenden einer Bezeichnung als Bedingung in einer DLP-Richtlinie

Sie können eine Beschriftung erstellen und dann:
  
- **Veröffentlichen** , sodass Endbenutzer finden Sie unter und die Bezeichnung manuell auf Inhalte anwenden können. 
    
- **Automatisch übernehmen** ermittelt, um Inhalte, die die Bedingungen, die Sie auswählen. 
    
Weitere Informationen über Bezeichnungen finden Sie unter [Übersicht über Bezeichnungen](labels.md).
  
Nachdem eine Bezeichnung erstellt wurde, können Sie in Ihrer DLP-Richtlinien klicken Sie dann der Beschriftung als Bedingung verwenden. Sie möchten z. B., da hierfür:
  
- Sie veröffentlicht eine Beschriftung mit dem Namen **vertraulich**, so dass Personen in Ihrer Organisation die Bezeichnung manuell auf vertrauliche e-Mails und Dokumente anwenden können. Mithilfe dieser Beschriftung als Bedingung in DLP-Richtlinie können Sie Inhalte mit der Bezeichnung **vertraulich** genutzt wird mit Personen außerhalb Ihrer Organisation einschränken. 
    
- Sie ein Label mit dem Namen **Alpine House** für ein Projekt mit diesem Namen erstellt und dann der Beschriftung automatisch auf Inhalte, die mit den Schlüsselwörtern "Alpine Hütte" angewendet. Mithilfe dieser Beschriftung als Bedingung in DLP-Richtlinie können Sie einen richtlinientipp für Endbenutzer anzeigen, wenn sie diese Inhalte mit einer anderen Person außerhalb Ihrer Organisation freigeben möchten. 
    
- Ein Label namens **Steuerdatensatz**, wird veröffentlicht, damit Ihre Datensatzverwalter manuell die Bezeichnung auf Inhalte anwenden können, die als Datensätze klassifiziert werden soll. Mithilfe dieser Beschriftung als Bedingung in DLP-Richtlinie können Sie Inhalte mit dieser Beschriftung in Verbindung mit anderen Arten von vertraulichen Informationen wie ITINs oder Führerschein-erhalten; gelten Sie Protection-Aktionen für Inhalte, die mit der Bezeichnung **Steuerdatensatz**. sowie zum rufen Sie detaillierter Berichte über die DLP-Richtlinie aus der DLP-Berichte ab und überwachen Sie Protokolldaten. 
    
- Sie haben ein Label namens " **Executive führende Team - Sensitive** " auf die Exchange-Postfächern und OneDrive-Konten von einer Gruppe von Führungskräften veröffentlicht. Mithilfe dieser Beschriftung als Bedingung in DLP-Richtlinie können Sie die Archivierung und den Schutz Aktionen auf die gleiche Teilmenge der Inhalte und Benutzer erzwingen. 
    
Etiketten als Bedingung in DLP-Regeln verwenden, können Sie selektiv Protection Aktionen auf einem bestimmten Satz von Inhalten, Standorte oder Benutzer erzwingen.
  
![Etiketten als Bedingung](media/5b1752b4-a129-4a88-b010-8dcf8a38bb09.png)
  
### <a name="how-this-feature-relates-to-other-features"></a>Bezieht sich diese Funktion wie anderen Funktionen

Verschiedene Features können auf Inhalte, die mit vertraulichen Informationen angewendet werden:
  
- Eine [Aufbewahrungsrichtlinie Label](labels.md#applying-a-retention-label-automatically-based-on-conditions)[Anwenden einer Bezeichnung, automatisch basierend auf Bedingungen] und einer [Aufbewahrungsrichtlinie](retention-policies.md) können beide **aufbewahrungsaktionen für diesen Inhalt** erzwingen. 
    
- Eine DLP-Richtlinie kann **Schutz** Aktionen für diesen Inhalt durchsetzen. Und bevor diese Aktionen erzwungen, eine DLP-Richtlinie kann andere Bedingungen, die zusätzlich zu den Inhalt mit einer Bezeichnung erfüllt werden, erfordern. 
    
![Diagramm der Features, die auf vertrauliche Informationen anwenden können](media/dd410f97-a3a3-455c-a1e9-7ed8ae6893d6.png)
  
Beachten Sie, dass eine DLP-Richtlinie eine umfangreichere Erkennung-Funktion als eine Beschriftung oder Aufbewahrung Richtlinie vertrauliche Informationen angewendet wurde. Eine DLP-Richtlinie Schutzvorrichtungen Aktionen auf Inhalte, die mit vertraulichen Informationen erzwingen kann, und wenn vertrauliche Informationen aus dem Inhalt entfernt wird, diese Schutzvorrichtungen Aktionen rückgängig gemacht beim nächsten Start von der Inhalt überprüft. Aber wenn eine Aufbewahrungsrichtlinie oder Beschriftung Inhalte mit vertraulichen Informationen angewendet wird, das ist eine einmalige Aktion, die wird nicht rückgängig gemacht werden, auch wenn der vertraulichen Informations entfernt.
  
Eine Beschriftung als Bedingung in einer DLP-Richtlinie verwenden, können Sie die Archivierung und den Schutz von Aktionen auf Inhalt mit der Beschriftung erzwingen. Sie können Inhalte mit einer Bezeichnung genau wie Inhalt mit vertraulichen Informationen vorstellen – eine Beschriftung und einen Typ vertrauliche Informationen werden Eigenschaften, die zum Inhalt, klassifizieren, damit Sie Aktionen auf diesen Inhalt erzwingen können.
  
![Diagramm der DLP-Richtlinie mit Label-Steuerelement als Bedingung](media/4538fd8f-fb74-4743-bc22-a5de33adfebb.png)
  
## <a name="simple-settings-vs-advanced-settings"></a>Einfache Einstellungen im Vergleich zu Erweiterte Einstellungen

Bei der Erstellung einer DLP-Richtlinie fügen Sie zwischen einfache oder erweiterte Einstellungen auswählen:
  
- **Einfache Einstellungen** erleichtern den am häufigsten verwendeten Typ des DLP-Richtlinie ohne Verwendung des Regel-Editors zum Erstellen oder ändern Regeln erstellen. 
    
- **Erweiterte Einstellungen** verwenden den Skript-Editor, um Sie vollständige Kontrolle über jede Einstellung für die DLP-Richtlinie zu ermöglichen. 
    
Keine Sorge, im Hintergrund einfache Einstellungen und erweiterte Einstellungen arbeiten, genau, indem bestehend aus Bedingungen und Aktionen – nur mit einfachen Einstellungen Regeln durchsetzen, den Skript-Editor nicht angezeigt. Es ist eine schnelle Möglichkeit zum Erstellen einer DLP-Richtlinie.
  
### <a name="simple-settings"></a>Einfache Einstellungen

Das häufigste DLP-Szenario erstellen weitem, ist eine Richtlinie zum Schutz von Inhalt mit vertraulichen Informationen genutzt wird mit Personen außerhalb Ihrer Organisation und einer Aktion automatische Vertragsstrafen und wie durch die Beschränkung auf, die den Inhalt zugreifen können, Endbenutzer oder Administrator Benachrichtigungen senden, und das Ereignis zur späteren Untersuchung Überwachung. Personen verwenden DLP, um zu verhindern, dass die unbeabsichtigte Offenlegung von vertraulichen Informationen.
  
Um dieses Ziel zu erreichen, bei der Erstellung einer DLP-Richtlinie zu vereinfachen, können Sie **einfache Einstellungen verwenden**auswählen. Geben Sie diese Einstellungen konsultieren, um die am häufigsten verwendeten DLP-Richtlinie implementieren, ohne in der Regeleditor wechseln zu müssen.
  
![DLP-Optionen für einfache oder erweiterte Einstellungen](media/33c93824-ead5-43b6-9c3e-fd1630c92a7d.png)
  
### <a name="advanced-settings"></a>Erweiterte Einstellungen

Wenn Sie weitere benutzerdefinierte DLP-Richtlinien erstellen müssen, können Sie die **Verwendung der erweiterten Einstellungen**auswählen.
  
Erweiterten Einstellungen erhalten Sie die Regeleditor, in dem Sie verfügen über Vollzugriff auf alle möglichen Optionen, einschließlich der Anzahl der Instanzen und Genauigkeit (Confidence Level) für jede Regel übereinstimmen.
  
Um zu einem Abschnitt schnell zu wechseln, klicken Sie auf ein Element in der oberen Navigationsleiste des Editors Regel fahren Sie mit diesem Abschnitt unten.
  
![Der oberen Navigationsleiste im Menü des DLP-Regel-Editors](media/c527b97f-ca53-4c79-ad19-1a63be8a8ecc.png)
  
## <a name="dlp-policy-templates"></a>DLP-Richtlinienvorlagen

Der erste Schritt beim Erstellen einer DLP-Richtlinie ist welche Informationen zum Schutz auswählen. Beginnen Sie mit einer DLP-Vorlage, speichern Sie die Arbeit erstellen einen neuen Satz von Regeln von Grund auf neu, und herauszufinden, welche Arten von Informationen in der Standardeinstellung enthalten sein sollen. Sie können dann zum Hinzufügen oder ändern diesen Anforderungen an die Regel, um bestimmte Anforderungen Ihrer Organisation erfüllen Feinabstimmung.
  
Eine vorkonfigurierte DLP-Richtlinienvorlage helfen Ihnen die bestimmte Arten von vertraulichen Informationen, wie etwa HIPAA Daten, PCI DSS-Daten, Gramm-Leach-Bliley Act-Daten oder sogar standortspezifisch personenbezogene Informationen (P.I.) zu erkennen. Erleichterung für Suchen und häufige Arten von vertraulichen Informationen zu schützen, enthalten die Richtlinienvorlagen in Office 365 bereits am häufigsten verwendeten Arten der vertraulichen Informationen für Sie die ersten Schritte beim erforderlich.
  
![Liste der Vorlagen für Richtlinien zur Verhinderung von Datenverlust, wobei die Vorlage für die USA hervorgehoben ist Patriot Act](media/791b2403-430b-4987-8643-cc20abbd8148.png)
  
Ihrer Organisation möglicherweise auch einen eigenen spezifischen Anforderungen, die in diesem Fall können Sie eine DLP-Richtlinie von Grund auf erstellen, indem Sie die Option **benutzerdefinierte Richtlinie** auswählen. Eine benutzerdefinierte Richtlinie ist leer und enthält keine vorgefertigten Regeln. 
  
## <a name="roll-out-dlp-policies-gradually-with-test-mode"></a>Allmähliches Bereitstellen von DLP-Richtlinien im Testmodus

Wenn Sie die DLP-Richtlinien erstellen, sollten Sie erwägen, Bereitstellung der Schulungsunterlagen schrittweise deren Einfluss bewerten und Testen ihre Effektivität vor deren vollständiger Erzwingung. Sie möchten beispielsweise keine neue DLP-Richtlinie zum versehentlich Blockieren des Zugriffs auf Tausenden von Dokumenten, die Personen Zugriff auf ihre Arbeit benötigen.
  
Wenn Sie möglicherweise eine große Auswirkung DLP-Richtlinien erstellen, sollten in den folgenden Schritten folgen:
  
1. **Im Testmodus ohne Richtlinientipps starten** und verwenden Sie dann die DLP-Berichte und Vorfälle bewerten die Auswirkungen von Berichten. DLP-Berichte können Sie die Nummer, Speicherort, Typ und Schweregrad der Richtlinie Übereinstimmungen anzeigen. Basierend auf den Ergebnissen, können Sie die Regeln Feinabstimmung nach Bedarf. Im Testmodus wirkt sich DLP-Richtlinien nicht die Produktivität der Mitarbeiter in Ihrer Organisation arbeiten. 
    
2. **Fahren Sie im Testmodus mit Benachrichtigungen und Richtlinientipps fort**, sodass Sie die Benutzer über die Einhaltungsrichtlinien in Kenntnis setzen und auf die Anwendung der Regeln vorbereiten können. In dieser Phase können Sie die Benutzer auch bitte, Sie über falsche Positivmeldungen zu benachrichtigen, damit Sie die Regeln noch besser abstimmen können. 
    
3. **Vollständiger Erzwingung für die Richtlinien zu starten** , damit die Aktivitäten in den Regeln werden angewendet, und der Inhalt der geschützte. Überwachen der DLP-Berichte und Vorfall Berichte oder Benachrichtigungen, um sicherzustellen, dass die Ergebnisse sind, was Sie beabsichtigen weiterhin. 
    
![Optionen für die Verwendung des Testmodus und das Einschalten der Richtlinie](media/49fafaac-c6cb-41de-99c4-c43c3e380c3a.png)
  
Sie können eine DLP-Richtlinie zu einem beliebigen Zeitpunkt deaktivieren die alle Regeln in der Richtlinie beeinflusst. Allerdings kann jede Regel auch einzeln deaktiviert werden durch den Status in der Regeleditor umschalten.
  
![Optionen für das Deaktivieren einer Regel in einer Richtlinie](media/f7b258ff-1b8b-4127-b580-83c6492f2bef.png)
  
## <a name="dlp-reports"></a>DLP-Berichte

Nachdem Sie erstellen und Aktivieren der DLP-Richtlinien, sollten Sie überprüfen, ob sie arbeiten, wie Sie vorgesehen und hilft Ihnen, bleiben kompatibel sind. DLP-Berichte können Sie schnell die Anzahl der DLP-Richtlinie anzeigen und eine Regel gleicht über Zeit und die Anzahl der falsch positive Ergebnisse und überschreibt. Für jeden Bericht können Sie diese Übereinstimmungen, hängt vom Speicherort Zeitrahmen, Filtern und es auch nach unten zu einer bestimmten Richtlinie, Regel oder Aktion werden können.
  
Mit den DLP-Berichten können Sie geschäftliche Einblicke erhalten und von folgenden Vorteilen profitieren:
  
- Sie können sich auf bestimmte Zeiträume konzentrieren und so mehr über die Gründe für Spitzen und Trends erfahren.
    
- Entdecken von Geschäftsprozessen, die Ihre Organisation Kompatibilitätsrichtlinien verletzen.
    
- Sie können die geschäftlichen Auswirkungen der DLP-Richtlinien besser nachvollziehen.
    
Darüber hinaus können Sie die DLP-Berichte verwenden, um Ihre DLP-Richtlinien optimieren, wenn sie ausgeführt werden.
  
![Dashboard in Sicherheit und Compliance Center Berichte](media/6d741252-a0ce-4429-95ba-6c857ecc9a7e.png)
  
## <a name="how-dlp-policies-work"></a>Funktionsweise von DLP-Richtlinien

DLP erkennt vertrauliche Informationen mithilfe einer eingehenden Inhaltsanalyse (nicht nur einer einfachen Textprüfung). Bei dieser eingehenden Inhaltsanalyse werden Schlüsselwortübereinstimmung, Wörterbuchübereinstimmungen, die Auswertung regulärer Ausdrücke, interne Funktionen sowie weitere Inhaltsuntersuchungsmethoden herangezogen, um Inhalte zu erkennen, welche die DLP-Richtlinien erfüllen. Möglicherweise gilt nur ein kleiner Prozentsatz Ihrer Daten als vertraulich. Eine DLP-Richtlinie kann nur diese Daten bestimmen, überwachen und automatisch schützen, ohne Personen zu behindern, die mit den restlichen Inhalten arbeiten.
  
### <a name="policies-are-synced"></a>Richtlinien werden synchronisiert

Nach der Erstellung einer DLP-Richtlinie in das Wertpapier &amp; Compliance Center, in einem zentralen Speicher gespeichert und klicken Sie dann auf verschiedene Inhaltsquellen, einschließlich synchronisiert:
  
- Exchange Online, und von dort an Outlook im Web und Outlook 2013 und höher
    
- OneDrive for Business-Websites
    
- SharePoint Online-Websites
    
- Office 2016-Desktopprogramme (Excel 2016, PowerPoint 2016 und Word 2016)
    
Nachdem die Richtlinie mit den richtigen Speicherorten synchronisiert zugrunde, startet zum Bewerten von Inhalten und Erzwingen von Aktionen.
  
### <a name="policy-evaluation-in-onedrive-for-business-and-sharepoint-online-sites"></a>Richtlinienauswertung in OneDrive for Business- und SharePoint Online-Websites

In allen Ihrer SharePoint Online-Websites und OneDrive for Business-Websites, Dokumenten ständig ändern – ständig wird der Erstellung, bearbeiteten, freigegebenen und so weiter. Dies bedeutet Dokumente können in Konflikt oder jederzeit mit einer DLP-Richtlinie kompatibel sind. Beispielsweise eine Person kann Hochladen eines Dokuments, das keine vertraulichen Informationen für ihre Teamwebsite enthält, aber später, eine andere Person dasselbe Dokument bearbeiten kann, und fügen Sie vertraulichen Informationen hinzu.
  
Aus diesem Grund überprüfen DLP-Richtlinien Dokumente häufig im Hintergrund auf Richtlinienübereinstimmungen. Sie können sich dies als asynchrone Richtlinienauswertung vorstellen.
  
Hier wird die Funktionsweise. Als Personen hinzufügen oder Ändern von Dokumenten in ihre Websites, durchsucht das Suchmodul die Inhalte, damit Sie sie später suchen können. Während dies der Fall ist, überprüft des Inhalts auch für vertrauliche Informationen und überprüft, ob es gemeinsam genutzt wird. Vertraulicher Informationen, der gefunden wird ist sicher in den Suchindex gespeichert, sodass nur das Compliance-Team, aber nicht die meisten Benutzer zugreifen kann. Jede DLP-Richtlinie, die Sie aktiviert haben, klicken Sie auf führt im Hintergrund (asynchron) Überprüfung Suche häufig für alle Inhalte, die mit eine Richtlinie übereinstimmt, und Anwenden von Aktionen aus, um vor unbeabsichtigten Speicherverluste zu schützen.
  
![Diagramm zum Programmkompatibilitäts-DLP-Richtlinie Inhalt asynchron auswerten](media/bdf73099-039a-4909-ae89-ac12c41992ba.png)
  
Dokumente können jedoch nicht nur mit einer DLP-Richtlinie in Konflikt stehen, sondern es können auch Änderungen vorgenommen werden, die dazu führen, dass sie nun einer DLP-Richtlinie entsprechen. Wenn eine Person zum Beispiel einem Dokument Kreditkartennummern hinzufügt, kann dies dazu führen, dass die DLP-Richtlinie den Zugriff auf das Dokument automatisch sperrt. Wenn die Person jedoch später die vertraulichen Informationen entfernt, wird die Aktion (in diesem Fall die Sperre) automatisch entfernt, wenn das Dokument das nächste Mal anhand der Richtlinie ausgewertet wird.
  
DLP wertet alle Inhalte, die indiziert werden kann. Weitere Informationen dazu, welche Dateitypen standardmäßig durchsucht werden finden Sie unter [standardmäßig durchforstete Dateinamenerweiterungen und analysierte Dateitypen in SharePoint Server 2013](https://go.microsoft.com/fwlink/p/?LinkID=627430).
  
### <a name="policy-evaluation-in-exchange-online-outlook-2013-and-later-and-outlook-on-the-web"></a>Auswertung von Richtlinien in Exchange Online, Outlook 2013 und höher und Outlook im Web

Bei der Erstellung einer DLP-Richtlinie, die Exchange Online als Speicherort enthält, die die Richtlinie aus der Office 365-Sicherheit synchronisierter &amp; Compliance Center zu Exchange Online, und klicken Sie dann von Exchange Online zu Outlook im Web und Outlook 2013 und höher.
  
Beim Verfassen einer Nachricht in Outlook kann der Benutzer richtlinientipps finden Sie unter wie die Inhalte zu erstellenden DLP-Richtlinien ausgewertet wird. Und nachdem eine Nachricht gesendet wurde, wird ausgewertet gegen DLP-Richtlinien als normaler Bestandteil der Nachrichtenübermittlung, zusammen mit Exchange-Transportregeln und DLP-Richtlinien in der Exchange-Verwaltungskonsole erstellt (Siehe für Weitere Informationen im nächsten Abschnitt). DLP-Richtlinien überprüft die Nachricht und alle Anlagen.
  
### <a name="policy-evaluation-in-the-office-2016-desktop-programs"></a>Richtlinienbewertung in den Office 2016-Desktopprogrammen

Excel 2016, 2016 PowerPoint und Word 2016 bestehen dieselbe Funktion zum Identifizieren von vertraulichen Informationen und Anwenden von DLP-Richtlinien als SharePoint Online und OneDrive für Unternehmen. Diese Programme Office 2016 Synchronisieren ihrer DLP-Richtlinien direkt aus dem zentralen Richtlinienspeicher, und klicken Sie dann den Inhalt für die DLP-Richtlinien kontinuierlich bewerten, wenn Benutzer arbeiten mit Dokumenten aus einer Website, die in einer DLP-Richtlinie enthalten ist.
  
Auswertung von DLP-Richtlinien in Office 2016 soll keine Auswirkung auf die Leistung der Programme oder die Produktivität der Mitarbeiter an Inhalten arbeiten. Wenn sie in einem großen Dokument arbeiten oder dem Computer des Benutzers ausgelastet ist, kann es einige Sekunden für einen richtlinientipp angezeigt werden dauern.
  
## <a name="permissions"></a>Berechtigungen

Mitglieder Ihres Teams Compliance, die DLP-Richtlinien erstellen werden benötigen Berechtigungen, um die Sicherheit &amp; Compliance Center. Standardmäßig Ihr Administrator haben Zugriff auf diesen Speicherort, und weisen Sie können Compliance Officer und anderen Personen Zugriff auf die Sicherheit &amp; Compliance Center, ohne dass sie alle erforderlichen Berechtigungen von einem Mandanten Admin. Zu diesem Zweck, es wird empfohlen, die Sie:
  
1. Erstellen Sie eine Gruppe in Office 365, und fügen Sie ihr Compliance Officers hinzu.
    
2. Erstellen Sie auf der Seite **Berechtigungen** der Sicherheit eine Rollengruppe &amp; Compliance Center. 
    
3. Fügen Sie die Office 365-Gruppe der Rollengruppe hinzu.
    
Weitere Informationen finden Sie unter [Give users access to the Office 365 Compliance Center](grant-access-to-the-security-and-compliance-center.md).
  
Diese Berechtigungen sind nur erforderlich, um eine DLP-Richtlinie zu erstellen und anzuwenden. Für die Durchsetzung von Richtlinien ist kein Zugriff auf Inhalte erforderlich.
  
## <a name="find-the-dlp-cmdlets"></a>Suchen Sie nach der DLP-cmdlets

Die meisten der Cmdlets für die Sicherheit zu verwendenden &amp; Compliance Center, müssen Sie:
  
1. [Eine Verbindung zum Office 365 Security &amp; Compliance Center mithilfe von Remote-PowerShell herstellen](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. Verwenden Sie eine der folgenden [Sicherheit in Office 365 &amp; Compliance Center Cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)
    
DLP-Berichte müssen jedoch Daten aus über Office 365, einschließlich Exchange Online ziehen. Aus diesem Grund stehen die Cmdlets für die DLP-Berichte in Exchange Online Powershell – nicht in Security &amp; Compliance Center Powershell. Aus diesem Grund müssen für die Verwendung von Cmdlets für die DLP-Berichte:
  
1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. Verwenden Sie eine dieser Cmdlets für die DLP-Berichte:
    
  - [Get-DlpDetectionsReport](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
  - [Get-DlpDetailReport](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    
## <a name="more-information"></a>Weitere Informationen

- [Erstellen einer DLP-Richtlinie aus einer Vorlage](create-a-dlp-policy-from-a-template.md)
    
- [Senden von Benachrichtigungen und Anzeigen von Richtlinientipps für DLP-Richtlinien](use-notifications-and-policy-tips.md)
    
- [Erstellen einer DLP-Richtlinie zum Schützen von Dokumenten mit FCI oder anderen Eigenschaften](protect-documents-that-have-fci-or-other-properties.md)
    
- [Inhalt der DLP-Richtlinienvorlagen](what-the-dlp-policy-templates-include.md)
    
- [Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)
    
- [Wonach die DLP-Funktionen suchen](what-the-dlp-functions-look-for.md)
    
- [Erstellen eines benutzerdefinierten vertraulichen Informationstyps](create-a-custom-sensitive-information-type.md)
    

