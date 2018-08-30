---
title: Erstellen einer Abfrage zum Auffinden auf Websites gespeicherter vertraulicher Daten
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 3019fbc5-7f15-4972-8d0e-dc182dc7f836
description: Mit Data Loss Prevention (DLP) in SharePoint Online erkennen Sie Dokumente, die in der gesamten Ihres Mandanten vertrauliche Daten enthalten. Nach dem Auffinden der Dokumente, können Sie mit den Besitzern Dokument zum Schutz der Daten arbeiten. Dieses Thema enthält Informationen eine Abfrage zu suchenden vertrauliche Daten bilden.
ms.openlocfilehash: 13954a856dd265e3b735d940c7d334d922713637
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013859"
---
# <a name="form-a-query-to-find-sensitive-data-stored-on-sites"></a>Erstellen einer Abfrage zum Auffinden auf Websites gespeicherter vertraulicher Daten

Benutzer häufig vertrauliche Daten wie Kreditkarte Zahlen, Sozialversicherungsnummern, speichern oder persönliche, klicken Sie auf ihre Websites und über einen Zeitraum Dies kann verfügbar machen einer Organisation erhebliche Risiko von Datenverlusten. Dokumente auf Websites – einschließlich OneDrive for Business-Websites – mit Personen außerhalb der Organisation, die Zugriff auf die Informationen haben, sollte nicht freigegeben werden konnte. Mit Data Loss Prevention (DLP) in SharePoint Online erkennen Sie Dokumente, die in der gesamten Ihres Mandanten vertrauliche Daten enthalten. Nach dem Auffinden der Dokumente, können Sie mit den Besitzern Dokument zum Schutz der Daten arbeiten. Dieses Thema enthält Informationen eine Abfrage zu suchenden vertrauliche Daten bilden.
  
> [!NOTE]
> Elektronische Ermittlung oder eDiscovery und DLP sind Premium-Features, die [SharePoint Online – Plan 2](https://go.microsoft.com/fwlink/?LinkId=510080)erfordern. 
  
## <a name="forming-a-basic-dlp-query"></a>Erstellen einer einfachen DLP-Abfrage

Es gibt drei Teile, die eine grundlegende DLP-Abfrage bilden: SensitiveType, zählen Bereichs und Confidence Bereichs. Wie in der folgenden Abbildung dargestellt **SensitiveType: "\<Typ\>"** ist erforderlich, und beide**|\<zählen Bereich\> ** und**|\<Confidence Bereich\> ** sind optional. 
  
![Beispielabfrage, aufgeteilt in "Erforderlich" und "Optional"](media/DLP-query-example-text.png)
  
### <a name="sensitive-type---required"></a>Typ vertraulicher Informationen - erforderlich

Was ist jeder Teil? SharePoint DLP-Abfragen in der Regel beginnen Sie mit der Eigenschaft `SensitiveType:"` und einen Informationstyp aus der [vertraulicher Informationen eingibt Inventar](https://go.microsoft.com/fwlink/?LinkID=509999)nennen, und beenden Sie mit einem `"`. Sie können auch den Namen eines [benutzerdefinierten vertrauliche Informationstyp](create-a-custom-sensitive-information-type.md) verwenden, die Sie für Ihre Organisation erstellt haben. Angenommen, suchen Sie möglicherweise für Dokumente, die Kreditkarte Zahlen enthalten. In einer Instanz, verwenden Sie das folgende Format: `SensitiveType:"Credit Card Number"`. Da Sie Count Bereich oder Confidence Bereich einschließen, gibt die Abfrage jedes Dokument, in dem eine Kreditkartennummer erkannt wird. Dies ist die einfachste Abfrage, die Sie ausführen können, und es gibt die meisten Ergebnisse zurück. Beachten Sie, was zählt die Rechtschreibung und Abstände des Typs vertrauliche, beibehalten. 
  
### <a name="ranges---optional"></a>Bereiche - optional

Beide die nächsten beiden Webparts sind Bereiche, wir schnell überprüfen ein Bereichs aussieht. In SharePoint DLP-Abfragen, ein grundlegender Bereich wird durch dargestellt zweier Zahlen getrennt durch zwei Punkte dieses sieht wie folgt: `[number]..[number]`. Beispielsweise wenn `10..20` wird verwendet, würden diesen Bereich Zahlen von 10 bis 20 erfassen. Es gibt viele Kombinationen von anderen Bereich und mehrere werden in diesem Thema behandelt. 
  
Fügen Sie einen Bereich für die Anzahl der Abfrage. Count-Bereich können Sie um die Anzahl der Vorkommen von vertraulichen Informationen zu definieren, die ein Dokument muss enthalten, bevor es in den Abfrageergebnissen enthalten ist. Angenommen, wenn die Abfrage nur Dokumente zurückgegeben, die genau fünf Kreditkarte Zahlen enthalten soll, verwenden Sie diese: `SensitiveType:"Credit Card Number|5"`. Count-Bereich ist auch beim Identifizieren von Dokumenten, die hohe Grad Risiko darstellen. Beispielsweise könnte Ihrer Organisation Dokumente mit fünf oder mehr Kreditkarte Zahlen Risiken berücksichtigen. Suche nach Dokumenten dieses Kriterium Zeilenbreite, verwenden Sie diese Abfrage: `SensitiveType:"Credit Card Number|5.."`. Alternativ können Sie Suchen von Dokumenten mit fünf oder weniger Kreditkarte Zahlen Karte mithilfe dieser Abfrage: `SensitiveType:"Credit Card Number|..5"`. 
  
#### <a name="confidence-range"></a>Konfidenzbereich

Confidence-Bereich wird schließlich die Ebene der vertrauen, dass der erkannte vertrauliche Typ tatsächlich eine Übereinstimmung. Die Werte für Confidence Bereich funktionieren ähnlich wie um Bereich zu zählen. Sie können eine Abfrage ohne einschließlich eines Bereichs Count bilden. Suchen von Dokumenten mit einer beliebigen Anzahl von Kreditkarte Zahlen beispielsweise – wie lange die Confidence reichen 85 % oder höher – verwenden Sie diese Abfrage: `SensitiveType:"Credit Card Number|*|85.."`. 
  
> [!IMPORTANT]
> Das Sternchen ( `*`) ist ein Platzhalterzeichen, das alle Works Wert bedeutet. Sie können das Platzhalterzeichen verwenden ( `*`) entweder im Bereich Count oder im Bereich vertrauen, jedoch nicht in einem vertrauliche Typ. 
  
### <a name="additional-query-properties-and-search-operators-available-in-the-ediscovery-center"></a>Im eDiscovery Center stehen weitere Abfrageeigenschaften und Suchoperatoren zur Verfügung.

DLP in SharePoint wird auch die LastSensitiveContentScan-Eigenschaft, die Ihnen helfen kann für einen bestimmten Zeitrahmen überprüfte Dateien zu suchen. Beispiele für die Abfrage mit der `LastSensitiveContentScan` -Eigenschaft, siehe die [Beispiele für komplexe Abfragen](form-a-query-to-find-sensitive-data-stored-on-sites.md#BKMK_ExamplesOfComplexQueries) im nächsten Abschnitt. 
  
Sie können nicht nur DLP-spezifische Eigenschaften zum Erstellen einer Abfrage, sondern auch standardmäßige SharePoint eDiscovery-Suche Eigenschaften wie `Author` oder `FileExtension`. Operatoren können Sie komplexe Abfragen erstellen. Die Liste der verfügbaren Eigenschaften und Operatoren finden Sie im Blogbeitrag [Sucheigenschaften verwenden und Operatoren mit eDiscovery](https://go.microsoft.com/fwlink/?LinkId=510093) . 
  
## <a name="examples-of-complex-queries"></a>Beispiele

Die folgenden Beispiele verwenden unterschiedliche vertrauliche, Eigenschaften und Operatoren um zu veranschaulichen, wie Sie die Abfragen so finden, wonach Sie suchen optimieren können.
  
|**Abfrage**|**Erläuterung**|
|:-----|:-----|
| `SensitiveType:"International Banking Account Number (IBAN)"` <br/> |Der Name mag seltsam, da es so lange ist, aber es der richtige Name für diesen vertrauliche ist. Stellen Sie sicher, dass Sie den genaue Namen aus dem [vertrauliche Informationen Typen Inventar](https://go.microsoft.com/fwlink/?LinkID=509999)verwenden. Sie können auch den Namen eines [benutzerdefinierten vertrauliche Informationstyp](create-a-custom-sensitive-information-type.md) verwenden, die Sie für Ihre Organisation erstellt haben.<br/> |
| "SensitiveType:"Kreditkartennummer|1..4294967295|1.. 100"' <br/> |Dies gibt Dokumente mit mindestens eine Übereinstimmung, die vertrauliche Typ "Kreditkartennummer". Die Werte für den jeweiligen Bereich sind die jeweiligen Mindest- und Höchstwerte. Eine einfachere Möglichkeit zum Schreiben dieser Abfrage ist `SensitiveType:"Credit Card Number"`, aber wo befindet sich der Spaß?<br/> |
| "SensitiveType:"Kreditkartennummer| 5..25" und LastSensitiveContentScan:"8/11/2018..8/13/2018 "' <br/> |Dies gibt Dokumente mit 5-25 Kreditkarte Zahlen, die gescannt wurden aus 11 August 2018 bis 13 August 2018 zurück.  <br/> |
| "SensitiveType:"Kreditkartennummer| 5..25" und LastSensitiveContentScan:"8/11/2018..8/13/2018 "nicht FileExtension:XLSX" <br/> |Dies gibt Dokumente mit 5-25 Kreditkarte Zahlen, die gescannt wurden aus 11 August 2018 bis 13 August 2018 zurück. Dateien mit der Erweiterung XLSX sind nicht in den Abfrageergebnissen enthalten.  `FileExtension` ist eine viele Eigenschaften, die in einer Abfrage enthalten sein können. Weitere Informationen finden Sie unter [Verwenden von Sucheigenschaften und Operatoren mit eDiscovery](https://go.microsoft.com/fwlink/?LinkId=510093).<br/> |
| `SensitiveType:"Credit Card Number" OR SensitiveType:"U.S. Social Security Number (SSN)"` <br/> |Diese Abfrage gibt Dokumente zurück, die entweder eine Kreditkartennummer oder US-Sozialversicherungsnummer enthalten.  <br/> |
   
## <a name="examples-of-queries-to-avoid"></a>Beispiele

Nicht alle Abfragen werden gleich erstellt. Die folgende Tabelle enthält Beispiele für Abfragen, die nicht mit DLP in SharePoint funktionieren und beschreibt, warum.
  
|**Nicht unterstützte Abfrage**|**Reason**|
|:-----|:-----|
| "SensitiveType:"Kreditkartennummer|.." ` <br/> |Sie müssen mindestens eine Zahl hinzufügen.  <br/> |
| `SensitiveType:"NotARule"` <br/> |"NotARule" ist eine gültige vertrauliche Typnamen nicht. Nur Namen innerhalb der [vertraulichen Informationen Typen Inventar](https://go.microsoft.com/fwlink/?LinkID=509999) Arbeit in DLP-Abfragen.<br/> |
| "SensitiveType:"Kreditkartennummer|0"' <br/> |0 (null) ist nicht gültig, als der Mindestwert oder den Höchstwert in einem Bereich.  <br/> |
| `SensitiveType:"Credit Card Number"` <br/> |Es ist möglicherweise schwierig, finden Sie unter, aber es gibt zusätzlicher Leerraum zwischen "Kredit" und "Card", die die Abfrage ungültig macht. Verwenden Sie die genauen vertrauliche Typnamen aus dem [vertrauliche Informationen Typen Inventar](https://go.microsoft.com/fwlink/?LinkID=509999).<br/> |
| "SensitiveType:"Kreditkartennummer|1.. 3"" <br/> |Der Teil zwei Zeiträume sollte nicht durch ein Leerzeichen voneinander getrennt werden.  <br/> |
| "SensitiveType:"Kreditkartennummer| |1.|80.."" <br/> |Es sind zu viele Pipe Trennzeichen (|). Führen Sie stattdessen die in diesem Format: "SensitiveType:"Kreditkartennummer|1.|80.."" <br/> |
| "SensitiveType:"Kreditkartennummer|1.|80..101"' <br/> |Da Confidence Werte Prozentsatz darstellen, darf sie 100 nicht überschreiten. Wählen Sie stattdessen eine Zahl zwischen 1 und 100 ein.  <br/> |
   
## <a name="for-more-information"></a>Weitere Informationen

[Suchen von vertraulichen Daten, die in SharePoint Online-Websites gespeichert sind](https://support.office.com/article/ef788d8f-9748-4025-bfe4-40541ca4cfb2)
  
[Verfügbare Arten von vertraulichen Informationen](https://go.microsoft.com/fwlink/?LinkID=509999)
  
[Führen Sie eine Inhaltssuche in Office 365-Sicherheit &amp; Compliance Center](run-a-content-search-in-the-security-and-compliance-center.md)
  
[Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
  

