---
title: Grenzwerte für die Inhaltssuche in Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 78fe3147-1979-4c41-83bb-aeccf244368d
description: 'Erfahren Sie mehr über die Grenzwerte für die Inhaltssuche-Funktion in die Office 365-Sicherheit &amp; Compliance Center, wie beispielsweise die maximale Anzahl von gleichzeitigen Suchvorgänge. '
ms.openlocfilehash: 79142edf2e80378bf6f22474fca55c54fe5cc776
ms.sourcegitcommit: ea625737c4be14927f69aa71d4fbd7d7d94d9334
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/04/2019
ms.locfileid: "27544106"
---
# <a name="limits-for-content-search-in-the-office-365-security-amp-compliance-center"></a>Grenzwerte für die Inhaltssuche in Office 365-Sicherheit &amp; Compliance Center

> [!NOTE]
> Die Grenzwerte für die in diesem Thema unterscheiden sich von der aktuellen Grenzwerte für Compliance-eDiscovery in Exchange Online und für das eDiscovery Center in SharePoint Online. 
  
Verschiedene Grenzwerte gelten für das Inhaltssuche-Feature in die Office 365-Sicherheit &amp; Compliance Center. Führen Sie diese Include-suchen auf der Seite **Inhaltssuche** und Suchvorgänge an, die einem eDiscovery-Fall zugeordnet sind. Diese Grenzwerte helfen, die Integrität und die Qualität der Office 365-Organisationen bereitgestellten Dienste verwalten. Es gibt auch Grenzwerte, die im Zusammenhang mit der Indizierung von e-Mail-Nachrichten in Exchange Online für die Suche. Die Inhaltssuche oder e-Mail-Grenzwerte für die Indizierung können nicht geändert werden, aber Sie sollten bekannt sein, sodass diese Grenzwerte bei der Planung, Ausführung und Problembehandlung Content-Suche berücksichtigt werden können. 
  
## <a name="content-search-limits"></a>Grenzwerte für Inhaltssuche

Die folgende Tabelle enthält die Grenzwerte für die Suche in das Wertpapier &amp; Compliance Center.
  
|**Beschreibung der Beschränkung**|**Grenzwert**|
|:-----|:-----|
|Die maximale Anzahl von Postfächern oder Websites, die in einer einzelnen Content-Suche durchsucht werden können  <br/> |Keine Begrenzung  <br/> |
|Die maximale Anzahl der Content-Suche, die in Ihrer Organisation gleichzeitig ausgeführt werden können.  <br/> |Keine Begrenzung  <br/> |
|Die maximale Anzahl der Content-Suche, die ein einzelner Benutzer zur selben Zeit starten können. Beachten Sie, dass dieser Grenzwert wahrscheinlich erreicht wird, wenn der Benutzer versucht, starten Sie mehrere Suchvorgänge mithilfe der **Get-ComplianceSearch \| Start ComplianceSearch** in Sicherheit und Compliance Center PowerShell Command.<br/> |10   <br/> |
|Die maximale Anzahl der Elemente pro Postfach des Benutzers, die beim Anzeigen der Vorschau der Suchergebnisse auf der Vorschauseite angezeigt werden.  <br/> |100  <br/> |
|Die maximale Anzahl der Elemente in allen Benutzerpostfächern, die auf der Vorschauseite angezeigt werden, bei der Vorschau der Suchergebnisse gefunden. Die neuesten Elemente werden angezeigt.  <br/> |1,000  <br/> |
|Die maximale Anzahl von Benutzerpostfächern, die in der Vorschau für Suchergebnisse angezeigt werden können. Wenn mehr als 1000 Postfächer, die Inhalte enthalten, die die Suchabfrage entspricht vorhanden sind, werden nur die oberste 1000 Postfächer mit den meisten Suchergebnissen für die Vorschau.  <br/> |1,000  <br/> |
|Die maximale Anzahl von Elementen in SharePoint und OneDrive for Business-Websites, die auf der Vorschauseite angezeigt werden, bei der Vorschau der Suchergebnisse gefunden. Die neuesten Elemente werden angezeigt.  <br/> |200  <br/> |
|Die maximale Anzahl von Websites (in SharePoint und OneDrive für Unternehmen), die in der Vorschau für Suchergebnisse angezeigt werden können. Wenn mehr als 200 insgesamt Websites, die Inhalte enthalten, die die Suchabfrage entspricht vorhanden sind, werden nur die 200 Websites auf oberster Ebene mit den meisten Suchergebnissen für die Vorschau.  <br/> |200  <br/> |
|Die maximale Anzahl der Elemente pro Postfach für Öffentliche Ordner, die beim Anzeigen der Vorschau der Suchergebnisse auf der Vorschauseite angezeigt werden.  <br/> |100  <br/> |
|Die maximale Anzahl von Elementen, die gefunden in alle Postfächer für Öffentliche Ordner, die beim Anzeigen der Vorschau der Suchergebnisse auf der Vorschauseite angezeigt werden.  <br/> |200  <br/> |
|Die maximale Anzahl der öffentlichen Postfächer, die in der Vorschau für Suchergebnisse angezeigt werden können. Wenn mehr als 500 Postfächer für Öffentliche Ordner, die Inhalte enthalten, die die Suchabfrage entspricht vorhanden sind, werden nur die oberen 500 Postfächer für Öffentliche Ordner mit den meisten Suchergebnissen für die Vorschau.  <br/> |500  <br/> |
|Die maximale Anzahl von Zeichen für die Suchabfrage für ein Inhaltssuche (einschließlich Operatoren und Bedingungen).  <br/><br/> **Hinweis:** Dieser Grenzwert wird erst wirksam, nachdem die Abfrage erweitert wird, was bedeutet, dass die Abfrage für jedes Schlüsselwort erweitert abgerufen wird. Beispielsweise wenn Ruft eine Suchabfrage 15 Schlüsselwörter und zusätzliche Parameter und Bedingungen verfügt, die Abfrage 15 Mal jeweils mit den anderen Parametern und Bedingungen in der Abfrage erweitert. Obwohl die Anzahl der Zeichen in der Suchabfrage unter den Grenzwert möglicherweise, also es die erweiterten Abfrage, die Überschreitung dieses Grenzwerts dazu beitragen kann.<br/> |**Postfächer:** 10.000  <br/> **Websites:** 4.000 bei der Suche alle Websites oder 2.000, bei der Suche von bis zu 20 Websites <sup>1</sup> <br/> |
|Maximale Anzahl von Varianten beim Präfix Platzhalter verwenden, suchen Sie nach einem exakten Wortlaut in einer Suchabfrage oder bei Verwendung von Platzhalterzeichen Präfix und der boolesche Operator **NEAR** oder **ONEAR** zurückgegeben wird.  <br/> |10.000 <sup>2</sup> <br/> |
|Die minimale Anzahl von alpha-Zeichen für Präfix Platzhalter; beispielsweise `time*`, `one*`, oder `set*`.  <br/> |3  <br/> |
|Die maximale Anzahl von Postfächern in einer Content-Suche, die Sie löschen können Elemente, indem Sie eine Aktion "Suchen und löschen" (mithilfe der **New-ComplianceSearchAction-bereinigen** Befehl). Besitzt die Content-Suche, die Sie für eine Aktion durchführen Weitere Quellpostfächer als dieser Grenzwert, wird bei der Aktion fehl. Weitere Informationen zu suchen und löschen können finden Sie unter [Suchen und Löschen von e-Mail-Nachrichten in Office 365-Organisation](search-for-and-delete-messages-in-your-organization.md).<br/> |50.000  <br/> |
   
> [!NOTE]
> <sup>1</sup> bei der Suche SharePoint- und OneDrive for Business-Standorte werden die Zeichen in den URLs der Websites, der durchsucht wird mit dem Grenzwert gezählt.<br/> <sup>2</sup> für nicht-Satz Abfragen (ein Schlüsselwortwert, der keine Anführungszeichen verwendet) verwenden wir einen spezielle Präfix Index. Hier erfahren wir, dass ein Wort in einem Dokument, jedoch nicht im Dokument Auftretens auftritt. Klicken Sie dazu eine Abfrage Phrase (ein Schlüsselwortwert in doppelte Anführungszeichen) müssen wir die Position innerhalb des Dokuments für die Wörter im Ausdruck verglichen werden soll. Dies bedeutet, dass wir den Präfix Index für Phrase Abfragen verwendet werden können. In diesem Fall erweitert wir intern die Abfrage mit alle möglichen Wörter, denen das Präfix auf Erweitert. beispielsweise `"time*"` können erweitern bis `"time OR timer OR times OR timex OR timeboxed OR …"`. 10.000 ist die maximale Anzahl von Varianten, die das Wort, nicht die Anzahl der Dokumente, die mit der Abfrage übereinstimmen erweitert werden kann. Es ist keine Obergrenze für nicht-Satz Begriffe. 
  
## <a name="indexing-limits-for-email-messages"></a>Grenzwerte für die Indizierung für e-Mail-Nachrichten

Die folgende Tabelle beschreibt die Grenzwerte für die Indizierung, die in einer e-Mail-Nachricht als ein nicht-indizierten Element oder eine teilweise indizierten Element in den Ergebnissen einer Inhaltssuche zurückgegeben wird, führen können.
  
|**Indizierung Grenzwert**|**Maximalwert**|**Beschreibung**|
|:-----|:-----|:-----|
|Maximale Anlagengröße (außer Excel-Dateien)  <br/> |150 MB  <br/> |Die maximale Größe einer e-Mail-Anlage, die für die Indizierung analysiert werden. Mindestens eine Anlage, die größer als dieser Grenzwert ist für die Indizierung wird nicht analysiert werden kann, und die Nachricht mit der Anlage wird als teilweise indiziert gekennzeichnet.<br/> <br/>**Hinweis:** Die Analyse ist der Prozess, in dem der Indexdienst extrahiert den Text aus der Anlage, unnötige Zeichen wie Punkte und Leerzeichen entfernt und dividiert den Text in Wörter (in einem Prozess Tokenvorgang bezeichnet), die dann in den Index gespeichert werden.           |
|Maximale Größe des Excel-Dateien  <br/> |4 MB  <br/> |Die maximale Größe einer Excel-Datei befindet sich auf einer Website oder einer e-Mail-Nachricht, die für die Indizierung zu analysierende zugeordnet. Eine Excel-Datei, die größer als dieser Grenzwert wird nicht analysiert werden kann, und die Datei oder der e-Mail, die, der die Nachricht mit der Dateianlage als gekennzeichnet wird, nicht indizierten ist.  <br/> |
|Maximale Anzahl von Anlagen  <br/> |250  <br/> |Die maximale Anzahl von Dateien als Anlage einer e-Mail-Nachricht, die für die Indizierung analysiert werden soll. Wenn eine Nachricht mehr als 250 Anlagen enthält, die ersten 250 Anlagen analysiert und indiziert werden, und die Nachricht wird als teilweise indiziert werden, da sie zusätzliche Anlagen hatte, die analysiert waren nicht gekennzeichnet.  <br/> |
|Maximale Anlage Tiefe  <br/> |30  <br/> |Die maximale Anzahl von geschachtelten Anlagen, die analysiert werden. Beispielsweise werden, wenn eine e-Mail-Nachricht eine andere Nachricht als Anlage und die Anlage eine angefügte Word-Dokument hat, das Word-Dokument und die Nachricht angefügte indiziert. Dieses Verhalten weiterhin für bis zu 30 geschachtelten Anlagen.  <br/> |
|Maximale Anzahl von angefügte Bilder  <br/> |0  <br/> |Ein Bild, das an eine e-Mail-Nachricht angefügt wird vom Parser übersprungen, und ist nicht indiziert.  <br/> |
|Maximale Zeitaufwand für die Analyse eines Elements  <br/> |30 Sekunden  <br/> |Maximal 30 Sekunden ist für die Analyse eines Elements für die Indizierung aufgewendet wurde. Wenn die Analyse Zeit 30 Sekunden überschreitet, wird das Element als teilweise indiziert gekennzeichnet.  <br/> |
|Maximale Parser-Ausgabe  <br/> |2 Millionen Zeichen  <br/> |Die maximale Größe der Textausgabe aus der Parser, der indiziert ist. Beispielsweise werden der Parser 8 Millionen Zeichen aus einem Dokument extrahiert haben, nur die ersten 2 Millionen Zeichen indiziert.  <br/> |
|Maximale Annotation Token  <br/> |2 Millionen  <br/> |Wenn eine e-Mail-Nachricht indiziert ist, wird jedes Wort mit verschiedenen verarbeitungsanweisungen gekennzeichnet, die angeben, wie das Wort indiziert werden soll. Jede Gruppe von verarbeitungsanweisungen ist ein Token Annotation aufgerufen. Um die Qualität des Diensts in Office 365 verwalten, besteht es ein Grenzwert von 2 Millionen Annotation Token für eine e-Mail-Nachricht.  <br/> |
|Maximale Größe des Hauptteils im index  <br/> |67 Millionen Zeichen  <br/> |Die Gesamtzahl der Zeichen in den Textkörper einer e-Mail-Nachricht und alle zugehörigen Anlagen. Bei eine e-Mail-Nachricht indiziert ist, wird die gesamte Text im Textkörper der Nachricht und alle Anlagen in einer einzelnen Zeichenfolge verkettet. Diese Zeichenfolge, die indiziert ist die maximale Größe beträgt 67 Millionen Zeichen.  <br/> |
|Maximale eindeutige Token im Textkörper  <br/> |1 Mio.  <br/> |Wie bereits erläutert, Token sind das Ergebnis der Extrahieren von Text aus dem Inhalt, Interpunktionszeichen und Leerzeichen entfernt, und klicken Sie dann Inhaltsmengen in Wörter (als Token bezeichnet), die im Index gespeichert sind. Beispielsweise den Ausdruck `"cat, mouse, bird, dog, dog"` 5 Token enthält. Aber nur 4 dieser Token eindeutig sind. Es besteht ein Grenzwert von 1 Million eindeutige Token pro e-Mail-Nachricht, die verhindert, dass den Index zu groß mit zufälligen Token abrufen.<br/> |
  
## <a name="more-information"></a>Weitere Informationen

Es sind zusätzliche Einschränkungen im Zusammenhang mit verschiedenen Aspekte der Inhalte Suche, wie das Exportieren von Suchergebnissen und Indizieren von Inhalt. Eine Beschreibung der mit diesen Grenzwerten finden Sie unter den folgenden Themen:
  
- [Exportieren von Inhaltssuchergebnissen ](export-search-results.md#export-limits)
    
- [Teilweise indizierte Elemente in der Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md)
    
- [Untersuchen von teilweise indizierten Elementen in Office 365 eDiscovery](investigating-partially-indexed-items-in-ediscovery.md)
    
- [Suchbeschränkungen für SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f)
    
Informationen zum Content-Suche finden Sie unter:
  
- [Content-Suche in Office 365](content-search.md)
    
- [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
