---
title: Teilweise indizierte Elemente in der Inhaltssuche in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/11/2018
ms.audience: Admin
ms.topic: conceptual
f1_keywords:
- ms.o365.cc.UnindexedItemsLearnMore
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: d1691de4-ca0d-446f-a0d0-373a4fc8487b
description: 'Informationen zu nicht indizierten Elementen in Exchange und SharePoint, die Sie in eine Inhaltssuche einbeziehen können, die über das Security & Compliance Center ausgeführt wird. '
ms.openlocfilehash: 22eca4e56c21783db348f6569b73257a9cc53dab
ms.sourcegitcommit: 0baa79a6e6fb72be488556607bc8c441642981a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/02/2019
ms.locfileid: "33527653"
---
# <a name="partially-indexed-items-in-content-search-in-office-365"></a>Teilweise indizierte Elemente in der Inhaltssuche in Office 365

Eine Inhaltssuche, die Sie im Security & Compliance Center in Office 365 ausführen, enthält automatisch teilweise indizierte Elemente in den geschätzten Suchergebnissen, wenn Sie eine Suche ausführen. Teilweise indizierte Elemente sind Exchange-Postfachelemente und Dokumente auf SharePoint-und OneDrive für Business-Websites, die aus irgendeinem Grund nicht vollständig für die Suche indiziert wurden. In Exchange enthält ein teilweise indiziertes Element in der Regel eine Datei mit einem Dateityp, der nicht indiziert werden kann, die an eine e-Mail-Nachricht angefügt ist. Im folgenden finden Sie einige Gründe, warum Elemente nicht für die Suche indiziert werden können und beim Ausführen einer Suche als teilweise indizierte Elemente zurückgegeben werden: 
  
- Der Dateityp wird für die Indizierung nicht erkannt oder nicht unterstützt.
    
-  Nachrichten haben eine angefügte Datei ohne einen gültigen Handler, wie Bilddateien; Dies ist die häufigste Ursache für teilweise indizierte e-Mail-Elemente. 
    
- Der Dateityp wird für die Indizierung unterstützt, aber es ist ein Indizierungsfehler für eine bestimmte Datei aufgetreten.
    
- Die E-Mail enthält zu viele Dateien im Anhang.
    
- Die an die E-Mail angehängte Datei ist zu groß.
    
- Eine Datei wurde mit Technologien von anderen Anbietern als Microsoft verschlüsselt.
    
- Eine Datei ist kennwortgeschützt.
    
> [!NOTE]
> Die meisten Office 365-Organisationen weisen weniger als 1% der Inhalte nach Volumen und weniger als 12% nach Größe auf, die teilweise indiziert sind. Der Unterschied zwischen Volumen und Größe besteht darin, dass größere Dateien eine höhere Wahrscheinlichkeit haben, Inhalte zu enthalten, die nicht vollständig indiziert werden können. 
  
Bei rechtlichen Untersuchungen kann es erforderlich sein, dass Ihre Organisation teilweise indizierte Elemente überprüft. Sie können auch angeben, ob teilweise indizierte Elemente eingeschlossen werden sollen, wenn Sie Suchergebnisse auf einen lokalen Computer exportieren oder wenn Sie die Ergebnisse für die Analyse mit Office 365 Advanced eDiscovery vorbereiten. Weitere Informationen finden Sie unter [ermitteln teilweise indizierter Elemente in Office 365 eDiscovery](investigating-partially-indexed-items-in-ediscovery.md).
  
## <a name="file-types-not-indexed-for-search"></a>Für die Suche nicht indizierte Dateitypen

Bestimmte Dateitypen wie Bitmap- oder MP3-Dateien enthalten keinen zu indizierenden Inhalt. Daher führen die Such Indizierungsserver in Exchange und SharePoint keine Volltextindizierung für diese Dateitypen durch. Diese Dateitypen werden als nicht unterstützte Dateitypen betrachtet. Es gibt außerdem Dateitypen, für die die Volltextindizierung deaktiviert wurde (entweder standardmäßig oder durch den Administrator). Nicht unterstützte und deaktivierte Dateitypen werden als nicht indizierte Elemente in der Inhaltssuche bezeichnet. Wie bereits erwähnt, können teilweise indizierte Elemente in die Gruppe der Suchergebnisse eingeschlossen werden, wenn Sie eine Suche ausführen, die Suchergebnisse auf einen lokalen Computer exportieren oder Suchergebnisse für erweiterte eDiscovery vorbereiten. 
  
Eine Liste von unterstützten und deaktivierten Dateiformaten finden Sie in den folgenden Themen:
  
- **** - [Von der Exchange-Suche indizierte Exchange-Dateiformate](https://go.microsoft.com/fwlink/p/?LinkID=386618)
    
- **Exchange** - [-Get-SearchDocumentFormat](https://go.microsoft.com/fwlink/p/?LinkID=724037)
    
- **** Standardmäßig[durchforstete Dateinamenerweiterungen und analysierte Dateitypen in](https://go.microsoft.com/fwlink/p/?LinkID=404033) SharePoint - 
    

  
## <a name="messages-and-documents-with-partially-indexed-file-types-can-be-returned-in-search-results"></a>Nachrichten und Dokumente mit teilweise indizierten Dateitypen können in Suchergebnissen zurückgegeben werden

Nicht jede e-Mail-Nachricht mit einer teilweise indizierten Dateianlage oder jedem teilweise indizierten SharePoint-Dokument wird automatisch als teilweise indiziertes Element zurückgegeben. Das liegt daran, dass andere Nachrichten-oder Dokumenteigenschaften wie die **Subject** -Eigenschaft in e-Mail-Nachrichten und die Eigenschaften **Title** oder **Author** für Dokumente indiziert und zur Durchsuchung verfügbar sind. Beispielsweise gibt eine Stichwortsuche nach "Financial" Elemente mit einer teilweise indizierten Dateianlage zurück, wenn dieses Schlüsselwort im Betreff einer e-Mail-Nachricht oder im Dateinamen oder Titel eines Dokuments angezeigt wird. Wenn das Schlüsselwort jedoch nur im Text der Datei angezeigt wird, wird die Nachricht oder das Dokument als teilweise indiziertes Element zurückgegeben. 
  
Auf ähnliche Weise werden Nachrichten mit teilweise indizierten Dateianlagen und Dokumenten eines teilweise indizierten Dateityps in Suchergebnisse eingeschlossen, wenn andere Nachrichten-oder Dokumenteigenschaften, die indiziert und durchsuchbar sind, den Suchkriterien entsprechen. Zu den Nachrichteneigenschaften, die für die Suche indiziert werden, gehören Sende- und Empfangsdatum, Absender und Empfänger, Dateiname von Anhängen sowie der Nachrichtentext. Zu den für die Suche indizierten Dokumenteigenschaften gehören erstellte und geänderte Daten. Obwohl es sich bei einer Nachrichtenanlage möglicherweise um ein teilweise indiziertes Element handelt, wird die Nachricht in die regulären Suchergebnisse eingeschlossen, wenn der Wert anderer Nachrichten-oder Dokumenteigenschaften mit den Suchkriterien übereinstimmt.
  
Eine Liste der e-Mail-und Dokumenteigenschaften, nach denen Sie mithilfe der Suchfunktion im Security & Compliance Center suchen können, finden Sie unter [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md).
  
## <a name="partially-indexed-items-included-in-the-search-results"></a>Teilweise indizierte Elemente in den Suchergebnissen

Möglicherweise muss Ihre Organisation zusätzliche Analysen für teilweise indizierte Elemente identifizieren und ausführen, um zu bestimmen, was Sie sind, was Sie enthalten, und ob Sie für eine bestimmte Untersuchung relevant sind. Wie bereits erläutert, werden die teilweise indizierten Elemente in den durchsuchten Inhaltsspeicherorten automatisch in die geschätzten Suchergebnisse eingeschlossen. Sie haben die Möglichkeit, diese teilweise indizierten Elemente einzuschließen, wenn Sie Suchergebnisse exportieren oder die Suchergebnisse für erweiterte eDiscovery vorbereiten.
  
Beachten Sie bei Teil indizierten Elementen Folgendes:
  
- Wenn Sie eine Inhaltssuche ausführen, werden die Gesamtanzahl und Größe von teilweise indizierten Exchange-Elementen (von der Suchabfrage zurückgegeben) in Suchstatistiken im Detailbereich angezeigt und als **indizierte Elemente**bezeichnet. Beachten Sie, dass Statistiken zu teilweise indizierten Elementen, die im Detailbereich angezeigt werden, nicht teilweise indizierte Elemente in SharePoint oder OneDrive sind.
    
- Wenn die Suche, aus der Sie Ergebnisse exportieren, eine Suche nach bestimmten Inhaltsspeicherorten oder allen Inhaltsspeicherorten in Ihrer Organisation war, werden nur die nicht indizierten Elemente aus Inhaltsspeicherorten exportiert, die Elemente enthalten, die den Suchkriterien entsprechen. In other words, if no search results are found in a mailbox or site, then any unindexed items in that mailbox or site won't be exported. Der Grund dafür ist, dass das Exportieren teilweise indizierter Elemente aus vielen Standorten in der Organisation möglicherweise die Wahrscheinlichkeit von Exportfehlern erhöht und die Zeitdauer erhöht, die zum Exportieren und Herunterladen der Suchergebnisse benötigt wird.
    
    Wenn Sie teilweise indizierte Elemente aus allen Inhaltsspeicherorten für eine Suche exportieren möchten, konfigurieren Sie die Suche so, dass alle Elemente (durch Entfernen von Schlüsselwörtern aus der Suchabfrage) zurückgegeben werden, und exportieren Sie dann nur teilweise indizierte Elemente, wenn Sie die Suchergebnisse exportieren (nur durch Klicken auf ** Elemente, die ein unbekanntes Format aufweisen, verschlüsselt sind oder aus anderen Gründen** unter **Ausgabeoptionen**nicht indiziert wurden).
    
- Wenn Sie alle Postfachelemente in die Suchergebnisse aufnehmen möchten oder wenn eine Suchabfrage keine Stichwörter oder nur einen Datumsbereichs angibt, werden teilweise indizierte Elemente möglicherweise nicht in die PST-Datei kopiert, die die teilweise indizierten Elemente enthält. Der Grund dafür ist, dass alle Elemente, einschließlich aller teilweise indizierten Elemente, automatisch in die regulären Suchergebnisse eingeschlossen werden.
    
- Teilweise indizierte Elemente können nicht in der Vorschau angezeigt werden. Sie müssen die Suchergebnisse exportieren, um teilweise indizierte Elemente anzuzeigen, die von der Suche zurückgegeben werden.

Wenn Sie außerdem Suchergebnisse exportieren und teilweise indizierte Elemente in den Export einbeziehen, werden teilweise indizierte Elemente aus SharePoint-Elementen in einen Ordner mit **** dem Namen "uncrawlable" exportiert. Wenn Sie teilweise indizierte Exchange-Elemente exportieren, werden Sie unterschiedlich exportiert, je nachdem, ob die teilweise indizierten Elemente mit der Suchabfrage übereinstimmen, und die Konfiguration der Exporteinstellungen. 

In der folgenden Tabelle wird das Export Verhalten von indizierten und teilweise indizierten Elementen und die Angabe angegeben, ob jeder für die verschiedenen Export Konfigurationseinstellungen enthalten ist.

|**Export Konfiguration**|**Indizierte Elemente, die einer Suchabfrage entsprechen**|**Teilweise indizierte Elemente, die einer Suchabfrage entsprechen**|**Teilweise indizierte Elemente, die nicht mit der Suchabfrage übereinstimmen**|
|:-----|:-----|:-----|:-----|
|Nur indizierte Elemente exportieren  <br/> |Exportiert<br/> |Exportiert (enthalten in den indizierten Elementen, die exportiert werden)<br/>  |Nicht exportiert <br/>|
|Nur teilweise indizierte Elemente exportieren  <br/> |Nicht exportiert  <br/> |Exportiert (als teilweise indizierte Elemente)<br/> |Exportiert (als teilweise indizierte Elemente)|
|Exportieren von indizierten und teilweise indizierten Elementen  <br/> |Exportiert<br/> |Exportiert (enthalten in den indizierten Elementen, die exportiert werden)<br/>  |Exportiert (als teilweise indizierte Elemente)<br/>|
||||

## <a name="partially-indexed-items-excluded-from-the-search-results"></a>Teilweise indizierte Elemente, die aus den Suchergebnissen ausgeschlossen sind

Wenn ein Element teilweise indiziert ist, aber nicht den Suchabfrage Kriterien entspricht, wird es nicht als teilweise indiziertes Element in den Suchergebnissen eingeschlossen. In anderen Worten wird das Element von den Suchergebnissen ausgeschlossen. Als Beispiel: Sie führen eine Suche ohne Schlüsselwörter oder Eigenschaften aus, weil Sie alle Inhalte einschließen möchten. Sie schließen jedoch einen Zeitraum für die Abfrage ein. Wenn ein teilweise indiziertes Element außerhalb dieses Datumsbereichs liegt, wird es nicht als teilweise indiziertes Element eingeschlossen. Datumsbereiche sind eine effektive Möglichkeit, teilweise indizierte Elemente aus den Suchergebnissen auszuschließen.
  
Wenn Sie beim Exportieren der Ergebnisse einer Suche teilweise indizierte Elemente einbeziehen möchten, werden teilweise indizierte Elemente, die aus den Suchergebnissen ausgeschlossen wurden, nicht exportiert.
  
Eine Ausnahme zu dieser Regel ist, wenn Sie eine abfragebasierte Aufbewahrung erstellen, die einem eDiscovery-Fall zugeordnet ist. Wenn Sie eine abfragebasierte Aufbewahrung erstellen, werden alle teilweise indizierten Elemente in der Warteschleife gehalten. Hierzu gehören teilweise indizierte Elemente, die nicht mit den Suchabfrage Kriterien übereinstimmen, und teilweise indizierte Elemente, die möglicherweise außerhalb einer Datumsbereichs Bedingung liegen. Weitere Informationen zum Erstellen von abfragebasierten Haltebereichen finden Sie in Schritt 4 in [eDiscovery-Fällen](ediscovery-cases.md#step-4-place-content-locations-on-hold).
  
## <a name="indexing-limits-for-messages-in-content-search"></a>Indizierungs Grenzwerte für Nachrichten in der Inhaltssuche

In der folgenden Tabelle werden die Indizierungs Grenzwerte beschrieben, die dazu führen können, dass eine e-Mail-Nachricht als teilweise indiziertes Element in einer Inhaltssuche in Office 365 zurückgegeben wird.
  
Eine Liste der Indizierungs Grenzwerte für SharePoint-Dokumente finden Sie unter [Search Limits for SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f).
  
|**Indizierungs Grenzwert**|**Maximalwert**|**Beschreibung**|
|:-----|:-----|:-----|
|Maximale Anlagengröße (ohne Excel-Dateien)  <br/> |150 MB  <br/> |Die maximale Größe einer e-Mail-Anlage, die für die Indizierung analysiert wird. Anlagen, die größer als dieser Grenzwert sind, werden nicht für die Indizierung analysiert, und die Nachricht mit der Anlage wird als teilweise indiziert markiert.  <br/><br/> **Hinweis:** Bei der Analyse handelt es sich um den Prozess, bei dem der Indexdienst Text aus der Anlage extrahiert, unnötige Zeichen wie Interpunktion und Leerräume entfernt und dann den Text in Wörter (in einem Prozess namens "Tokenisierung") unterteilt, die dann im Index gespeichert werden.           |
|Maximale Größe von Excel-Dateien  <br/> |4 MB  <br/> |Die maximale Größe einer Excel-Datei, die sich auf einer Website befindet oder an eine e-Mail-Nachricht angefügt ist, die zum Indizieren analysiert wird. Alle Excel-Dateien, die größer als dieser Grenzwert sind, werden nicht analysiert, und die Datei oder die e-Mail-Nachricht mit der Dateianlage wird als nicht indiziert markiert.  <br/> |
|Maximale Anzahl von Anlagen  <br/> |250  <br/> |Die maximale Anzahl von Dateien, die an eine e-Mail-Nachricht angehängt werden, die für die Indizierung analysiert wird. Wenn eine Nachricht mehr als 250 Anlagen enthält, werden die ersten 250-Anlagen analysiert und indiziert, und die Nachricht wird als teilweise indiziert markiert, da Sie zusätzliche Anlagen hatte, die nicht analysiert wurden.  <br/> |
|Maximale Anlagen Tiefe  <br/> |30  <br/> |Die maximale Anzahl von geschachtelten Anlagen, die analysiert werden. Wenn beispielsweise eine e-Mail-Nachricht mit einer anderen Nachricht verbunden ist und die angefügte Nachricht ein angefügtes Word-Dokument enthält, werden das Word-Dokument und die angefügte Nachricht indiziert. Dieses Verhalten wird für bis zu 30 verschachtelte Anlagen fortgesetzt.  <br/> |
|Maximale Anzahl der angefügten Bilder  <br/> |0  <br/> |Ein Bild, das an eine e-Mail-Nachricht angefügt ist, wird vom Parser übersprungen und nicht indiziert.  <br/> |
|Maximale Zeit für die Analyse eines Elements  <br/> |30 Sekunden  <br/> |Es werden maximal 30 Sekunden für die Analyse eines Elements für die Indizierung verwendet. Wenn die Analysezeit 30 Sekunden überschreitet, wird das Element als teilweise indiziert markiert.  <br/> |
|Maximale Ausgabe des Parsers  <br/> |2 Millionen Zeichen  <br/> |Die maximale Menge an Text, die vom Parser indiziert wird. Wenn der Parser beispielsweise 8 Millionen Zeichen aus einem Dokument extrahiert hat, werden nur die ersten 2 Millionen Zeichen indiziert.  <br/> |
|Maximale Anmerkungs Token  <br/> |2 Millionen  <br/> |Wenn eine e-Mail-Nachricht indiziert wird, wird jedes Wort mit verschiedenen Verarbeitungsanweisungen versehen, die angeben, wie dieses Wort indiziert werden soll. Jeder Satz von Verarbeitungsanweisungen wird als Anmerkungs Token bezeichnet. Um die Dienstqualität in Office 365 zu erhalten, gibt es eine Grenze von 2 Millionen-Anmerkungs Token für eine e-Mail-Nachricht.  <br/> |
|Maximale Größe des Texts im Index  <br/> |67 Millionen Zeichen  <br/> |Die Gesamtzahl der Zeichen im Textkörper einer e-Mail-Nachricht und aller Anlagen. Wenn eine e-Mail-Nachricht indiziert wird, wird der gesamte Text im Nachrichtentext und in allen Anlagen in einer einzelnen Zeichenfolge verkettet. Die maximale Größe dieser Zeichenfolge, die indiziert wird, ist 67 Millionen Zeichen.  <br/> |
|Maximale Anzahl eindeutiger Token im Textkörper  <br/> |1 Million  <br/> |Wie bereits erläutert, sind Token das Ergebnis der Extraktion von Text aus Inhalten, das Entfernen von Interpunktion und Leerzeichen und das anschließende Teilen in Wörter (als Token bezeichnet), die im Index gespeichert sind. Der Ausdruck `"cat, mouse, bird, dog, dog"` enthält beispielsweise 5 Token. Aber nur 4 davon sind eindeutige Token. Es gibt eine Grenze von 1 Million eindeutigen Token pro e-Mail-Nachricht, wodurch verhindert wird, dass der Index mit zufälligen Token zu lang wird.  <br/> |
   

  
## <a name="more-information-about-partially-indexed-items"></a>Weitere Informationen zu teilweise indizierten Elementen

- Wie bereits erwähnt, werden durch eine Stichwortsuche möglicherweise Ergebnisse zurückgegeben, wenn das Schlüsselwort in den indizierten Metadaten angezeigt wird, da Nachrichten-und Dokumenteigenschaften und deren Metadaten indiziert werden. Dieselbe Keyword-Suche gibt jedoch nicht dasselbe Element zurück, wenn das Schlüsselwort nur im Inhalt eines Elements mit einem nicht unterstützten Dateityp angezeigt wird. In diesem Fall würde das Element als teilweise indiziertes Element zurückgegeben.
    
- Wenn ein teilweise indiziertes Element in den Suchergebnissen enthalten ist, da es die Suchabfrage Kriterien erfüllt (und nicht ausgeschlossen wurde), wird es in der geschätzten Suchstatistik nicht als teilweise indiziertes Element eingeschlossen. Außerdem wird er beim Exportieren von Suchergebnissen nicht in teilweise indizierte Elemente eingeschlossen.
    
- Obwohl ein Dateityp für die Indizierung unterstützt wird und indiziert ist, können Indizierungs-oder Suchfehler auftreten, die dazu führen, dass eine Datei als teilweise indiziertes Element zurückgegeben wird. Beispielsweise kann das Durchsuchen einer sehr großen Excel-Datei teilweise erfolgreich sein (da die ersten 4 MB indiziert sind), aber dann schlägt fehl, da die Dateigrößenbeschränkung überschritten wird. In diesem Fall ist es möglich, dass dieselbe Datei mit den Suchergebnissen und als teilweise indiziertes Element zurückgegeben wird.
    
- Mit Microsoft-Technologien verschlüsselte Dateianlagen werden indiziert und können durchsucht werden. Mit nicht-Microsoft-Technologien verschlüsselte Dateien sind teilweise indiziert.
    
- Mit S/MIME verschlüsselte e-Mail-Nachrichten sind teilweise indiziert. Dazu gehören verschlüsselte Nachrichten mit oder ohne Dateianlagen.
    
- Durch die Verwaltung von Informationsrechten (Information Rights Management, IRM) geschützte Nachrichten werden indiziert und daher in die Suchergebnisse eingeschlossen, wenn sie der Suchabfrage entsprechen.

## <a name="see-also"></a>Siehe auch

[Untersuchen von teilweise indizierten Elementen in Office 365 eDiscovery](investigating-partially-indexed-items-in-ediscovery.md)

