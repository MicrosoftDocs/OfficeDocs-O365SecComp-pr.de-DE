---
title: Grenzwerte für die Inhaltssuche im Office 365 &amp; Security Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 78fe3147-1979-4c41-83bb-aeccf244368d
description: 'Informieren Sie sich über die Grenzwerte für die Inhaltssuche im Office 365 Security &amp; Compliance Center, wie beispielsweise die maximale Anzahl gleichzeitiger Suchvorgänge. '
ms.openlocfilehash: 0d114db30e9c5b61477789f8a2b91b88c936b253
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223114"
---
# <a name="limits-for-content-search-in-the-office-365-security-amp-compliance-center"></a>Grenzwerte für die Inhaltssuche im Office 365 &amp; Security Compliance Center

> [!NOTE]
> Die Grenzwerte in diesem Thema unterscheiden sich von den aktuellen Grenzwerten für in-Place-eDiscovery in Exchange Online und für das eDiscovery Center in SharePoint Online. 
  
Auf die Inhaltssuche im Office 365 Security &amp; Compliance Center werden verschiedene Grenzwerte angewendet. Hierzu gehören Suchvorgänge, die auf der Seite für die **Inhaltssuche** ausgeführt werden, und Suchvorgänge, die einem eDiscovery-Fall zugeordnet sind. Diese Grenzwerte tragen dazu bei, die Integrität und Qualität von Diensten für Office 365-Organisationen aufrechtzuerhalten. Außerdem gibt es Beschränkungen im Zusammenhang mit der Indizierung von e-Mail-Nachrichten in Exchange Online für die Suche. Sie können die Grenzwerte für die Inhaltssuche oder e-Mail-Indizierung nicht ändern, aber Sie sollten Sie beachten, damit Sie diese Einschränkungen bei der Planung, beim Ausführen und bei der Problembehandlung bei der Inhaltssuche berücksichtigen. 
  
## <a name="content-search-limits"></a>Grenzwerte für die Inhaltssuche

In der folgenden Tabelle sind die Such Grenzwerte im &amp; Security Compliance Center aufgeführt.
  
|**Beschreibung der Beschränkung**|**Grenzwert**|
|:-----|:-----|
|Die maximale Anzahl von Postfächern oder Websites, die in einer einzelnen Inhaltssuche durchsucht werden können  <br/> |Keine Begrenzung  <br/> |
|Die maximale Anzahl von Inhalts suchVorgängen, die in Ihrer Organisation gleichzeitig ausgeführt werden können.  <br/> |Keine Begrenzung  <br/> |
|Die maximale Anzahl von Inhalts suchVorgängen, die ein einzelner Benutzer gleichzeitig starten kann. Beachten Sie, dass dieser Grenzwert höchstwahrscheinlich betroffen ist, wenn der Benutzer versucht, mehrere Suchen mithilfe des Befehls **get \| -ComplianceSearch Start-ComplianceSearch** in Security & Compliance Center PowerShell zu starten.<br/> |10   <br/> |
|Die maximale Anzahl von Elementen pro Benutzerpostfach, die auf der Vorschauseite angezeigt werden, wenn Sie die Anzeige der Inhalts Suchergebnisse anzeigen.  <br/> |100  <br/> |
|Die maximale Anzahl von Elementen, die in allen Benutzerpostfächern gefunden werden, die auf der Vorschauseite angezeigt werden, wenn Sie die Anzeige der Inhalts Suchergebnisse anzeigen. Die neuesten Elemente werden angezeigt.  <br/> |1,000  <br/> |
|Die maximale Anzahl von Benutzerpostfächern, die für Suchergebnisse in der Vorschau angezeigt werden können. Wenn es mehr als 1000 Postfächer gibt, die Inhalte enthalten, die mit der Suchabfrage übereinstimmen, stehen nur die oberen 1000-Postfächer mit den meisten Suchergebnissen für die Vorschau zur Verfügung.  <br/> |1,000  <br/> |
|Die maximale Anzahl von Elementen, die in SharePoint-und OneDrive für Business-Websites gefunden werden, die auf der Vorschauseite angezeigt werden, wenn Sie die Anzeige der Inhalts Suchergebnisse anzeigen. Die neuesten Elemente werden angezeigt.  <br/> |200  <br/> |
|Die maximale Anzahl von Websites (in SharePoint und OneDrive for Business), die für Suchergebnisse in der Vorschau angezeigt werden können. Wenn es mehr als 200 gesamt Websites mit Inhalten gibt, die mit der Suchabfrage übereinstimmen, stehen nur die Top 200-Websites mit den meisten Suchergebnissen für die Vorschau zur Verfügung.  <br/> |200  <br/> |
|Die maximale Anzahl von Elementen pro Postfach für Öffentliche Ordner, die auf der Vorschauseite angezeigt werden, wenn Sie die Anzeige der Inhalts Suchergebnisse anzeigen.  <br/> |100  <br/> |
|Die maximale Anzahl von Elementen, die in allen Postfächern für Öffentliche Ordner gefunden werden, die auf der Vorschauseite angezeigt werden, wenn Sie die Inhalts Suchergebnisse anzeigen.  <br/> |200  <br/> |
|Die maximale Anzahl von öffentlichen Postfächern, die für Suchergebnisse in der Vorschau angezeigt werden können. Wenn mehr als 500 Postfächer für Öffentliche Ordner vorhanden sind, die Inhalte enthalten, die mit der Suchabfrage übereinstimmen, stehen nur die oberen 500-Postfächer für Öffentliche Ordner mit den meisten Suchergebnissen für die Vorschau zur Verfügung.  <br/> |500  <br/> |
|Die maximale Anzahl von Zeichen für die Suchabfrage (einschließlich Operatoren und Bedingungen) für eine Inhaltssuche.  <br/><br/> **Hinweis:** Diese Grenze wird wirksam, nachdem die Abfrage erweitert wurde, was bedeutet, dass die Abfrage für jedes Schlüsselwort erweitert wird. Wenn beispielsweise eine Suchabfrage 15 Schlüsselwörter und zusätzliche Parameter und Bedingungen enthält, wird die Abfrage 15 Mal erweitert, wobei sich die anderen Parameter und Bedingungen in der Abfrage befinden. Auch wenn die Anzahl der Zeichen in der Suchabfrage möglicherweise unter dem Grenzwert liegt, ist es die Erweiterte Abfrage, die dazu beitragen kann, diesen Grenzwert zu überschreiten.<br/> |**Postfächer:** 10.000  <br/> **Websites:** 4.000 beim Durchsuchen aller websites oder 2.000 bei der Suche von bis zu 20 Websites <sup>1</sup> <br/> |
|Maximale Anzahl von Varianten, die zurückgegeben werden, wenn ein Präfix Platzhalter verwendet wird, um nach einem exakten Ausdruck in einer Suchabfrage oder bei Verwendung eines Präfix Platzhalters und des booleschen Operators **near** oder **ONEAR** zu suchen.  <br/> |10.000 <sup>2</sup> <br/> |
|Die Mindestanzahl von Alphazeichen für Präfix Platzhalter; Beispiel `time*` `one*`:, oder `set*`.  <br/> |3  <br/> |
|Die maximale Anzahl von Postfächern in einer Inhaltssuche, in der Sie Elemente löschen können, indem Sie eine Aktion "suchen und löschen" ausführen (mithilfe des Befehls **New-ComplianceSearchAction-Purge** ). Wenn die Inhaltssuche, für die Sie eine Aktion zum Löschen ausführen, mehr Quellpostfächer als diesen Grenzwert hat, schlägt die Löschaktion fehl. Weitere Informationen zu Suche und Säuberung finden Sie unter [Suchen nach und Löschen von e-Mail-Nachrichten in Ihrer Office 365-Organisation](search-for-and-delete-messages-in-your-organization.md).<br/> |50.000  <br/> |
   
> [!NOTE]
> <sup>1</sup> beim durchSuchen von SharePoint-und OneDrive für Business-Standorte werden die Zeichen in den URLs der Websites, die durchsucht werden, mit diesem Grenzwert gezählt.<br/> <sup>2</sup> für nicht-Phrase-Abfragen (ein Schlüsselwortwert, der keine doppelten Anführungszeichen verwendet) verwenden wir einen speziellen Präfix Index. Dies weist darauf hin, dass ein Wort in einem Dokument vorkommt, aber nicht, wo es im Dokument vorkommt. Wenn Sie eine Ausdrucks Abfrage (einen Stichwort Wert mit doppelten Anführungszeichen) ausführen möchten, müssen wir die Position im Dokument mit den Wörtern im Ausdruck vergleichen. Dies führt dazu, dass der Präfix Index für Ausdrucks Abfragen nicht verwendet werden kann. In diesem Fall erweitern wir die Abfrage intern mit allen möglichen Wörtern, auf die das Präfix erweitert wird. beispielsweise `"time*"` kann zu `"time OR timer OR times OR timex OR timeboxed OR …"`erweitern. 10.000 ist die maximale Anzahl von Varianten, auf die das Wort erweitert werden kann, und nicht die Anzahl der Dokumente, die mit der Abfrage übereinstimmen. Es gibt keine Obergrenze für nicht-Phrasen Ausdrücke. 
  
## <a name="indexing-limits-for-email-messages"></a>Indizierungs Grenzwerte für e-Mail-Nachrichten

In der folgenden Tabelle werden die Indizierungs Grenzwerte beschrieben, die dazu führen können, dass eine e-Mail-Nachricht als nicht indiziertes Element oder als Teil indizierten Element in den Ergebnissen einer Inhaltssuche zurückgegeben wird.
  
|**Indizierungs Grenzwert**|**Maximalwert**|**Beschreibung**|
|:-----|:-----|:-----|
|Maximale Anlagengröße (ohne Excel-Dateien)  <br/> |150 MB  <br/> |Die maximale Größe einer e-Mail-Anlage, die für die Indizierung analysiert wird. Anlagen, die größer als dieser Grenzwert sind, werden nicht für die Indizierung analysiert, und die Nachricht mit der Anlage wird als teilweise indiziert markiert.<br/> <br/>**Hinweis:** Bei der Analyse handelt es sich um den Prozess, bei dem der Indexdienst Text aus der Anlage extrahiert, unnötige Zeichen wie Interpunktion und Leerräume entfernt und dann den Text in Wörter (in einem Prozess namens "Tokenisierung") unterteilt, die dann im Index gespeichert werden.           |
|Maximale Größe von Excel-Dateien  <br/> |4 MB  <br/> |Die maximale Größe einer Excel-Datei, die sich auf einer Website befindet oder an eine e-Mail-Nachricht angefügt ist, die zum Indizieren analysiert wird. Alle Excel-Dateien, die größer als dieser Grenzwert sind, werden nicht analysiert, und die Datei oder die e-Mail-Nachricht mit der Dateianlage wird als nicht indiziert markiert.  <br/> |
|Maximale Anzahl von Anlagen  <br/> |250  <br/> |Die maximale Anzahl von Dateien, die an eine e-Mail-Nachricht angehängt werden, die für die Indizierung analysiert wird. Wenn eine Nachricht mehr als 250 Anlagen enthält, werden die ersten 250-Anlagen analysiert und indiziert, und die Nachricht wird als teilweise indiziert markiert, da Sie zusätzliche Anlagen hatte, die nicht analysiert wurden.  <br/> |
|Maximale Anlagen Tiefe  <br/> |30  <br/> |Die maximale Anzahl von geschachtelten Anlagen, die analysiert werden. Wenn beispielsweise eine e-Mail-Nachricht mit einer anderen Nachricht verbunden ist und die angefügte Nachricht ein angefügtes Word-Dokument enthält, werden das Word-Dokument und die angefügte Nachricht indiziert. Dieses Verhalten wird für bis zu 30 verschachtelte Anlagen fortgesetzt.  <br/> |
|Maximale Anzahl der angefügten Bilder  <br/> |0  <br/> |Ein Bild, das an eine e-Mail-Nachricht angefügt ist, wird vom Parser übersprungen und nicht indiziert.  <br/> |
|Maximale Zeit für die Analyse eines Elements  <br/> |30 Sekunden  <br/> |Es werden maximal 30 Sekunden für die Analyse eines Elements für die Indizierung verwendet. Wenn die Analysezeit 30 Sekunden überschreitet, wird das Element als teilweise indiziert markiert.  <br/> |
|Maximale Ausgabe des Parsers  <br/> |2 Millionen Zeichen  <br/> |Die maximale Menge an Text, die vom Parser indiziert wird. Wenn der Parser beispielsweise 8 Millionen Zeichen aus einem Dokument extrahiert hat, werden nur die ersten 2 Millionen Zeichen indiziert.  <br/> |
|Maximale Anmerkungs Token  <br/> |2 Millionen  <br/> |Wenn eine e-Mail-Nachricht indiziert wird, wird jedes Wort mit verschiedenen Verarbeitungsanweisungen versehen, die angeben, wie dieses Wort indiziert werden soll. Jeder Satz von Verarbeitungsanweisungen wird als Anmerkungs Token bezeichnet. Um die Dienstqualität in Office 365 zu erhalten, gibt es eine Grenze von 2 Millionen-Anmerkungs Token für eine e-Mail-Nachricht.  <br/> |
|Maximale Größe des Texts im Index  <br/> |67 Millionen Zeichen  <br/> |Die Gesamtzahl der Zeichen im Textkörper einer e-Mail-Nachricht und aller Anlagen. Wenn eine e-Mail-Nachricht indiziert wird, wird der gesamte Text im Nachrichtentext und in allen Anlagen in einer einzelnen Zeichenfolge verkettet. Die maximale Größe dieser Zeichenfolge, die indiziert wird, ist 67 Millionen Zeichen.  <br/> |
|Maximale Anzahl eindeutiger Token im Textkörper  <br/> |1 Mio.  <br/> |Wie bereits erläutert, sind Token das Ergebnis der Extraktion von Text aus Inhalten, das Entfernen von Interpunktion und Leerzeichen und das anschließende Teilen in Wörter (als Token bezeichnet), die im Index gespeichert sind. Der Ausdruck `"cat, mouse, bird, dog, dog"` enthält beispielsweise 5 Token. Aber nur 4 davon sind eindeutige Token. Es gibt eine Grenze von 1 Million eindeutigen Token pro e-Mail-Nachricht, wodurch verhindert wird, dass der Index mit zufälligen Token zu lang wird.<br/> |
  
## <a name="more-information"></a>Weitere Informationen

Es gibt zusätzliche Beschränkungen im Zusammenhang mit verschiedenen Aspekten der Inhaltssuche, beispielsweise beim Exportieren von Suchergebnissen und der Inhaltsindizierung. Eine Beschreibung dieser Grenzwerte finden Sie in den folgenden Themen:
  
- [Exportieren von Inhaltssuchergebnissen ](export-search-results.md#export-limits)
    
- [Teilweise indizierte Elemente in der Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md)
    
- [Untersuchen von teilweise indizierten Elementen in Office 365 eDiscovery](investigating-partially-indexed-items-in-ediscovery.md)
    
- [Such Grenzwerte für SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f)
    
Informationen zu Inhalts suchen finden Sie unter:
  
- [Inhaltssuche in Office 365](content-search.md)
    
- [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
