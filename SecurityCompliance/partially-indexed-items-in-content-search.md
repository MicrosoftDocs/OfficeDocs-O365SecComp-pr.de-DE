---
title: Teilweise indizierte Elemente in der Inhaltssuche in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/11/2018
ms.audience: Admin
ms.topic: overview
f1_keywords:
- ms.o365.cc.UnindexedItemsLearnMore
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- SPO160
- MOE150
- MET150
ms.assetid: d1691de4-ca0d-446f-a0d0-373a4fc8487b
description: 'Erfahren Sie mehr über nicht indizierten Elementen in Exchange und SharePoint, die Sie in eine Inhaltssuche führen Sie über die Office 365-Sicherheit hinzufügen können &amp; Compliance Center. '
ms.openlocfilehash: 4624985a9c80313d0222470e6cfb2c56495f2142
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528979"
---
# <a name="partially-indexed-items-in-content-search-in-office-365"></a>Teilweise indizierte Elemente in der Inhaltssuche in Office 365

Content-Suche, die Sie über die Office 365-Sicherheit ausführen &amp; Compliance Center enthält teilweise indizierte Elemente automatisch in der geschätzten Suchergebnisse, wenn Sie eine Suche ausführen. Teilweise indizierte Elemente sind Exchange Postfachelemente und Dokumenten auf SharePoint und OneDrive for Business-Websites, die aus irgendeinem Grund für die Suche vollständig indiziert wurden nicht. In Exchange enthält eine teilweise indizierten Element in der Regel eine Datei – einen Dateityp, die nicht indiziert werden –, das eine e-Mail-Nachricht angefügt wird. Hier sind einige andere Gründe Warum Elemente können nicht für die Suche indiziert werden und werden als teilweise indizierte Elemente zurückgegeben, wenn Sie eine Suche ausführen: 
  
- Der Dateityp ist unbekannt oder nicht für die Indizierung unterstützt.
    
-  Nachrichten haben eine angefügte Datei ohne einen gültigen Handler, beispielsweise Bilddateien; Dies ist die häufigste Ursache teilweise indizierten e-Mail-Elemente. 
    
- Der Dateityp wird für die Indizierung unterstützt, aber es ist ein Indizierungsfehler für eine bestimmte Datei aufgetreten.
    
- Die E-Mail enthält zu viele Dateien im Anhang.
    
- Die an die E-Mail angehängte Datei ist zu groß.
    
- Eine Datei wurde mit Technologien von anderen Anbietern als Microsoft verschlüsselt.
    
- Eine Datei ist kennwortgeschützt.
    
> [!NOTE]
> Die meisten Office 365-Organisationen haben weniger als 1 % des Inhalts vom Datenträger und weniger als 12 % nach Größe, die teilweise indiziert ist. Der Grund für die Differenz zwischen Volumes und Größe ist, dass größere Dateien steigt die Wahrscheinlichkeit eines mit Inhalten, die nicht vollständig indiziert werden kann. 
  
Für legal Untersuchungen möglicherweise erforderlich teilweise indizierte Elemente Überprüfen Ihrer Organisation. Sie können auch angeben, ob teilweise indizierte Elemente beim Exportieren von Suchergebnissen auf einen lokalen Computer oder beim Vorbereiten der Ergebnisse für die Analyse mit Office 365 erweiterte eDiscovery einbezogen werden sollen. Weitere Informationen finden Sie unter [Investigating teilweise Elemente in Office 365 eDiscovery indiziert](investigating-partially-indexed-items-in-ediscovery.md).
  
## <a name="file-types-not-indexed-for-search"></a>Für die Suche nicht indizierte Dateitypen

Bestimmte Typen von Dateien, beispielsweise Bitmap oder MP3-Dateien enthalten keine Inhalte, die indiziert werden kann. Daher führen nicht die Indizierung von Servern in Exchange-Suche und SharePoint Volltext-Indizierung für diese Typen von Dateien. Die folgenden Dateitypen gelten als nicht unterstützte Dateitypen. Es gibt auch Dateitypen für die Volltext-Indizierung, standardmäßig oder von einem Administrator deaktiviert wurde. Nicht unterstützte und deaktiviert Dateitypen werden als nicht-indizierten Elementen in Content-Suche gekennzeichnet. Wie bereits zuvor erwähnt, teilweise indizierte Elemente können in den Suchergebnissen enthalten sein wenn Sie eine Suche ausführen, exportieren Sie die Suchergebnisse auf einen lokalen Computer oder vorbereiten Sie Suchergebnisse für erweiterte eDiscovery. 
  
Eine Liste von unterstützten und deaktivierten Dateiformaten finden Sie in den folgenden Themen:
  
- **Exchange** - [von Exchange-Suche indizierte Dateiformate](https://go.microsoft.com/fwlink/p/?LinkID=386618)
    
- **Exchange** - [Get-SearchDocumentFormat](https://go.microsoft.com/fwlink/p/?LinkID=724037)
    
- **SharePoint** - [standardmäßig durchforstete Dateinamenerweiterungen und analysierte Dateitypen in SharePoint](https://go.microsoft.com/fwlink/p/?LinkID=404033)
    

  
## <a name="messages-and-documents-with-partially-indexed-file-types-can-be-returned-in-search-results"></a>Nachrichten und Dokumente mit indiziert teilweise Datei-Typen in den Suchergebnissen zurückgegeben werden können

Nicht jede e-Mail-Nachricht mit Dateianlage teilweise indizierten oder jedes teilweise indizierten SharePoint-Dokument wird automatisch als teilweise indizierte Element zurückgegeben. Dies liegt daran anderen Nachricht oder Dokumenteigenschaften, wie die **Subject** -Eigenschaft in e-Mail-Nachrichten und den **Titel** oder den **Autor** Eigenschaften für Dokumente indizierten und durchsucht werden zur Verfügung stehen. Beispielsweise wird eine Suche nach dem Begriff "finanzielle" Elemente mit einer teilweise indizierten Dateianlage zurück, wenn das Stichwort in den Betreff einer e-Mail-Nachricht oder der Name oder der Titel eines Dokuments angezeigt wird. Jedoch, wenn das Schlüsselwort nur im Textkörper der Datei angezeigt wird, werden die Nachrichten oder Dokumente als teilweise indizierte Element zurückgegeben. 
  
In ähnlicher Weise sind andere Eigenschaften Nachrichten oder Dokumente, die indiziert und durchsuchbar sind, die den Suchkriterien entsprechen Nachrichten mit teilweise indizierten Dateianlagen und Dokumenten eines Typs teilweise indizierten Datei in den Suchergebnissen bei enthalten. Nachrichteneigenschaften, die für die Suche indiziert werden enthalten gesendete und empfangene Datumsangaben, Absender und Empfänger, den Dateinamen einer Anlage und Text im Textkörper Nachricht. Dokumenteigenschaften, die für die Suche indiziert sind Datumsangaben erstellte und bearbeitet wurde. Also, obwohl e-Mail-Anlagen eines teilweise indizierten Elements werden kann, wird die Nachricht in den Suchergebnissen regulären aufgenommen, wenn der Wert der anderen Nachricht oder ein Dokument Eigenschaften den Suchkriterien entspricht.
  
Eine Liste der e-Mail- und Dokument-Eigenschaften, die Sie mithilfe der Suchfunktion in das Wertpapier suchen können &amp; Compliance Center, finden Sie unter [Stichwortabfragen und Suchkriterien für die Inhaltssuche](keyword-queries-and-search-conditions.md).
  

  
## <a name="partially-indexed-items-included-in-the-search-results"></a>Teilweise indizierte Elemente in den Suchergebnissen enthalten
<a name="unindexeditemsresults"> </a>

Ihre Organisation möglicherweise erforderlich zu identifizieren, und führen zusätzliche Analyse auf teilweise indizierte Elemente, um zu ermitteln, was sind, was sie enthalten und, ob sie für eine bestimmte Untersuchung relevant sind. Wie bereits erklärt sind die teilweise indizierte Elemente in der Speicherorte für Inhalte, die durchsucht werden automatisch in der geschätzten Suchergebnisse enthalten. Sie können diese teilweise indizierte Elemente beim Exportieren von Suchergebnissen oder die Suchergebnisse für erweiterte eDiscovery vorbereiten einbezogen werden sollen. Teilweise indizierte Elemente aufnehmen möchten, wenn Sie Suchergebnisse exportieren oder erweiterte eDiscovery Vorbereitung, wählen Sie eine der Optionen, Elemente enthalten, die ein unbekanntes Format haben, werden verschlüsselt oder aus anderen Gründen indiziert wurden nicht.
  
Behalten Sie Folgendes in Bezug auf teilweise indizierte Elemente:
  
- Wenn Sie eine Inhaltssuche ausführen, werden die gesamte Anzahl und Größe teilweise indizierter Elemente (von der die Suchabfrage zurückgegeben) in Suchstatistik im Detailbereich angezeigt als "nicht-indizierten Elemente" mit der Bezeichnung.
    
- Wenn Sie Exportieren von Suchergebnissen und teilweise indizierte Elemente einschließen, werden teilweise indizierte Elemente von Exchange exportiert in eine separate PST-Datei für jedes Postfach, in denen sie gespeichert sind, oder als einzelne Nachrichten bei Auswahl der Option zum Herunterladen von Exchange-Elementen als Nachrichten. teilweise indizierten SharePoint-Elemente werden in einen Ordner namens **Uncrawlable**exportiert.
    
- Wenn die Suche, der Sie exportieren Ergebnisse aus einer Suche nach bestimmten Speicherorte für Inhalte oder alle Speicherorte für Inhalte in Ihrer Organisation war, werden nur die nicht-indizierten Elemente Speicherorte für Inhalte, die Elemente enthält, die den Suchkriterien entsprechen, exportiert. Anders ausgedrückt, wenn keine Suchergebnisse in einem Postfach oder Website gefunden werden, wird nicht klicken Sie dann alle nicht-indizierten Elemente in diesem Postfach oder Website exportiert werden. Der Grund dafür ist, dass die Wahrscheinlichkeit der Export Fehler erhöhen und die lange es, die dauert erhöhen zu exportieren, und Laden Sie die Suchergebnisse, möglicherweise exportieren teilweise indizierte Elemente aus vielen Standorten in der Organisation.
    
    Zum Exportieren teilweise indizierte Elemente aus allen Speicherorte für Inhalte für die Suche, Konfigurieren der Suche zum Zurückgeben von allen Elementen (durch Entfernen von Schlüsselwörter vom Search-Abfrage), und klicken Sie dann exportieren nur teilweise indizierte Elemente, wenn Sie die Suchergebnisse (durch Klicken auf **nur exportieren auf Elemente mit einem unbekannten Format, verschlüsselt werden, oder aus anderen Gründen indiziert wurden nicht** unter **Ausgabeoptionen**).
    
- Wenn Sie angeben, dass alle Postfachelemente in den Suchergebnissen enthalten, oder wenn eine Suchabfrage nicht, sodass alle Schlüsselwörter angegeben oder nur einen Datumsbereich gibt, teilweise indizierte Elemente möglicherweise nicht werden in die PST-Datei, die die teilweise indizierte Elemente enthält kopiert. Dies ist, da alle Elemente, einschließlich teilweise indizierte Elemente, automatisch in die reguläre Suchergebnisse eingeschlossen werden sollen.
    
- Teilweise indizierte Elemente sind nicht verfügbar in der Vorschau angezeigt werden. Müssen Sie die Ergebnisse der Suche zurückgegebenen teilweise indizierte Elemente anzeigen zu exportieren.

## <a name="partially-indexed-items-excluded-from-the-search-results"></a>Teilweise indizierte Elemente aus den Suchergebnissen ausgeschlossen

Wenn ein Element wird teilweise indiziert, aber es nicht die Abfrage Suchkriterien erfüllen, werden nicht als teilweise indizierte Element in den Suchergebnissen enthalten sein. Anders ausgedrückt, wird das Element aus den Suchergebnissen ausgeschlossen werden. Nehmen wir beispielsweise an Sie eine Suche ausführen, und fügen Sie keine Schlüsselwörter oder Eigenschaften, da Sie alle Inhalte einschließen möchten. Aber eine Datum Bereich Bedingung für die Abfrage. Wenn eine teilweise indizierten Element außerhalb dieses Datumsbereichs liegt, wird nicht er als teilweise indizierte Element einbezogen werden. Datumsbereiche sind effektiv teilweise indizierte Elemente aus den Suchergebnissen ausgeschlossen werden sollen.
  
In ähnlicher Weise teilweise indizierte Elemente einschließen aus, wenn Sie die Ergebnisse einer Suche exportiert werden soll, wird nicht teilweise indizierte Elemente, die aus den Suchergebnissen ausgeschlossen wurden exportiert werden.
  
Eine Ausnahme zu dieser Regel ist, wenn Sie eine abfragebasierte Aufbewahrung erstellen, die einem eDiscovery-Fall zugeordnet ist. Wenn Sie eine abfragebasierte Aufbewahrung erstellen, werden alle teilweise indizierte Elemente in der Warteschleife platziert. Dazu gehören teilweise indizierte Elemente, die die Suchkriterien für die Abfrage nicht entsprechen und teilweise indizierte Elemente, die außerhalb von Bereich Bedingung Datum liegen möglicherweise. Weitere Informationen zum Erstellen abfragebasierter enthält, finden Sie unter Schritt 4 in [eDiscovery-Fälle, in der Office 365-Sicherheit und Compliance Center](ediscovery-cases.md#step-4-place-content-locations-on-hold).
  
## <a name="indexing-limits-for-messages-in-content-search"></a>Grenzwerte für Nachrichten in Inhaltssuche Indizierung

Die folgende Tabelle beschreibt die Grenzwerte für die Indizierung, die in einer e-Mail-Nachricht zurückgegeben wird, als teilweise indizierte Element in einer Inhaltssuche in Office 365 führen können.
  
Eine Liste der Indizierung Grenzwerte für SharePoint-Dokumente finden Sie unter [suchbeschränkungen für SharePoint Online](https://support.office.com/article/7c06e9ed-98b6-4304-a900-14773a8fa32f).
  
|**Indizierung Grenzwert**|**Maximalwert**|**Beschreibung**|
|:-----|:-----|:-----|
|Maximale Anlagengröße (außer Excel-Dateien)  <br/> |150 MB  <br/> |Die maximale Größe einer e-Mail-Anlage, die für die Indizierung analysiert werden. Mindestens eine Anlage, die größer als dieser Grenzwert ist für die Indizierung wird nicht analysiert werden kann, und die Nachricht mit der Anlage wird als teilweise indiziert gekennzeichnet.<br/><br/> **Hinweis:** Die Analyse ist der Prozess, in dem der Indexdienst extrahiert den Text aus der Anlage, unnötige Zeichen wie Punkte und Leerzeichen entfernt und dividiert den Text in Wörter (in einem Prozess Tokenvorgang bezeichnet), die dann in den Index gespeichert werden.           |
|Maximale Größe des Excel-Dateien  <br/> |4 MB  <br/> |Die maximale Größe einer Excel-Datei befindet sich auf einer Website oder einer e-Mail-Nachricht, die für die Indizierung zu analysierende zugeordnet. Eine Excel-Datei, die größer als dieser Grenzwert wird nicht analysiert werden kann, und die Datei oder der e-Mail, die, der die Nachricht mit der Dateianlage als gekennzeichnet wird, nicht indizierten ist.  <br/> |
|Maximale Anzahl von Anlagen  <br/> |250  <br/> |Die maximale Anzahl von Dateien als Anlage einer e-Mail-Nachricht, die für die Indizierung analysiert werden soll. Wenn eine Nachricht mehr als 250 Anlagen enthält, die ersten 250 Anlagen analysiert und indiziert werden, und die Nachricht wird als teilweise indiziert werden, da sie zusätzliche Anlagen hatte, die analysiert waren nicht gekennzeichnet.  <br/> |
|Maximale Anlage Tiefe  <br/> |30  <br/> |Die maximale Anzahl von geschachtelten Anlagen, die analysiert werden. Beispielsweise werden, wenn eine e-Mail-Nachricht eine andere Nachricht als Anlage und die Anlage eine angefügte Word-Dokument hat, das Word-Dokument und die Nachricht angefügte indiziert. Dieses Verhalten weiterhin für bis zu 30 geschachtelten Anlagen.  <br/> |
|Maximale Anzahl von angefügte Bilder  <br/> |0  <br/> |Ein Bild, das an eine e-Mail-Nachricht angefügt wird vom Parser übersprungen, und ist nicht indiziert.  <br/> |
|Maximale Zeitaufwand für die Analyse eines Elements  <br/> |30 Sekunden  <br/> |Maximal 30 Sekunden ist für die Analyse eines Elements für die Indizierung aufgewendet wurde. Wenn die Analyse Zeit 30 Sekunden überschreitet, wird das Element als teilweise indiziert gekennzeichnet.  <br/> |
|Maximale Parser-Ausgabe  <br/> |2 Millionen Zeichen  <br/> |Die maximale Größe der Textausgabe aus der Parser, der indiziert ist. Beispielsweise werden der Parser 8 Millionen Zeichen aus einem Dokument extrahiert haben, nur die ersten 2 Millionen Zeichen indiziert.  <br/> |
|Maximale Annotation Token  <br/> |2 Millionen  <br/> |Wenn eine e-Mail-Nachricht indiziert ist, wird jedes Wort mit verschiedenen verarbeitungsanweisungen gekennzeichnet, die angeben, wie das Wort indiziert werden soll. Jede Gruppe von verarbeitungsanweisungen ist ein Token Annotation aufgerufen. Um die Qualität des Diensts in Office 365 verwalten, besteht es ein Grenzwert von 2 Millionen Annotation Token für eine e-Mail-Nachricht.  <br/> |
|Maximale Größe des Hauptteils im index  <br/> |67 Millionen Zeichen  <br/> |Die Gesamtzahl der Zeichen in den Textkörper einer e-Mail-Nachricht und alle zugehörigen Anlagen. Bei eine e-Mail-Nachricht indiziert ist, wird die gesamte Text im Textkörper der Nachricht und alle Anlagen in einer einzelnen Zeichenfolge verkettet. Diese Zeichenfolge, die indiziert ist die maximale Größe beträgt 67 Millionen Zeichen.  <br/> |
|Maximale eindeutige Token im Textkörper  <br/> |1 Mio.  <br/> |Wie bereits erläutert, Token sind das Ergebnis der Extrahieren von Text aus dem Inhalt, Interpunktionszeichen und Leerzeichen entfernt, und klicken Sie dann Inhaltsmengen in Wörter (als Token bezeichnet), die im Index gespeichert sind. Beispielsweise den Ausdruck `"cat, mouse, bird, dog, dog"` 5 Token enthält. Aber nur 4 dieser Token eindeutig sind. Es besteht ein Grenzwert von 1 Million eindeutige Token pro e-Mail-Nachricht, die verhindert, dass den Index zu groß mit zufälligen Token abrufen.<br/> |
   

  
## <a name="more-information-about-partially-indexed-items"></a>Weitere Informationen zu teilweise indizierte Elemente
<a name="moreinfo"> </a>

- Wie bereits zuvor erwähnt, da die Nachricht und Dokumenteigenschaften und ihre Metadaten indiziert sind, möglicherweise eine Schlüsselwortsuche Ergebnisse zurück, wenn das Stichwort in den indizierten Metadaten wird angezeigt. Jedoch möglicherweise, dass dieselbe die Schlüsselwortsuche nicht dasselbe Element zurück, wenn das Schlüsselwort nur in den Inhalt eines Elements mit einen nicht unterstützten Dateityp angezeigt wird. In diesem Fall würde das Element als teilweise indizierte Element zurückgegeben werden soll.
    
- Wenn eine teilweise indizierten Element in den Suchergebnissen enthalten ist, da es die Suchkriterien für die Abfrage erfüllt (und wurde nicht ausgeschlossen) werden nicht als teilweise indizierte Element in der geschätzten Suchstatistik enthalten sein. Darüber hinaus wird nicht es enthalten sein mit teilweise indizierte Elemente beim Exportieren von Suchergebnissen.
    
- Zwar ein Dateityp für die Indizierung unterstützt wird und wird indiziert, es können jedoch Indizierung oder Fehler, führen eine Datei als teilweise indizierte Element zurückgegeben werden soll. Beispielsweise eine sehr umfangreiche Excel-Datei suchen möglicherweise teilweise erfolgreich (die erste 4 MB sind indiziert), aber schlägt fehl, da die maximale Dateigröße überschritten wird. In diesem Fall ist es möglich, dass dieselbe Datei mit den Suchergebnissen und als teilweise indizierte Element zurückgegeben wird.
    
- Anlagen, die in Microsoft-Technologien verschlüsselt sind indiziert und durchsucht werden können. Dateien mit nicht-Microsoft-Technologien verschlüsselt sind teilweise indiziert.
    
- E-Mail-Nachrichten, die mit S/MIME verschlüsselt sind teilweise indiziert. Dazu gehören verschlüsselte Nachrichten mit oder ohne Anlagen.
    
- Durch die Verwaltung von Informationsrechten (Information Rights Management, IRM) geschützte Nachrichten werden indiziert und daher in die Suchergebnisse eingeschlossen, wenn sie der Suchabfrage entsprechen.

## <a name="see-also"></a>Siehe auch

[Untersuchen von teilweise indizierten Elementen in Office 365 eDiscovery](investigating-partially-indexed-items-in-ediscovery.md)

