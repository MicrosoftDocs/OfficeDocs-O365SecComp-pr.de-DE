---
title: Untersuchen von teilweise indizierten Elementen in Office 365 eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
description: Teilweise indizierte Elemente (auch Anruf nicht indizierter Elemente) werden Exchange-Postfachelemente und Dokumente in SharePoint und OneDrive, die von Websites für die aus irgendeinem Grund für die Inhaltssuche vollständig indiziert wurden nicht. In diesem Artikel erfahren Sie, warum Elemente können nicht für die Suche indiziert werden und werden als teilweise indizierte Elemente zurückgegeben, Search-Fehler für teilweise indizierte Elemente zu identifizieren und verwenden Sie ein PowerShell-Skript bestimmen Ihrer Organisation die Angriffsfläche teilweise indizierten e-Mail Elemente.
ms.openlocfilehash: 4e8e8c31e6c5450a9b84a1240c2ae8d891c1bd6f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529998"
---
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a><span data-ttu-id="0da43-104">Untersuchen von teilweise indizierten Elementen in Office 365 eDiscovery</span><span class="sxs-lookup"><span data-stu-id="0da43-104">Investigating partially indexed items in Office 365 eDiscovery</span></span>

<span data-ttu-id="0da43-p102">Content-Suche, die Sie über die Office 365-Sicherheit ausführen &amp; Compliance Center enthält teilweise indizierte Elemente automatisch in der geschätzten Suchergebnisse, wenn Sie eine Suche ausführen. Teilweise indizierte Elemente sind Exchange Postfachelemente und Dokumenten auf SharePoint und OneDrive for Business-Websites, die aus irgendeinem Grund für die Suche vollständig indiziert wurden nicht. Die meisten e-Mail-Nachrichten und Dokumente werden erfolgreich indiziert, da sie innerhalb der [Grenzwerte für die Indizierung für e-Mail-Nachrichten](limits-for-content-search.md#indexinglimits)liegen. Einige Elemente möglicherweise diese Indizierung Grenzwerte überschreiten und teilweise indiziert werden. Hier sind andere Gründe, warum Elemente können nicht für die Suche indiziert werden und werden als teilweise indizierte Elemente zurückgegeben, bei der Ausführung einer Inhaltssuche:</span><span class="sxs-lookup"><span data-stu-id="0da43-p102">A Content Search that you run from the Office 365 Security &amp; Compliance Center automatically includes partially indexed items in the estimated search results when you run a search. Partially indexed items are Exchange mailbox items and documents on SharePoint and OneDrive for Business sites that for some reason weren't completely indexed for search. Most email messages and site documents are successfully indexed because they fall within the [Indexing limits for email messages](limits-for-content-search.md#indexinglimits). However, some items may exceed these indexing limits, and will be partially indexed. Here are other reasons why items can't be indexed for search and are returned as partially indexed items when you run a Content Search:</span></span>
  
- <span data-ttu-id="0da43-110">E-Mail-Nachrichten müssen eine angefügte Datei einen Dateityp, die nicht indiziert werden kann. in den meisten Fällen wird der Dateityp [nicht erkannte oder für die Indizierung wird nicht unterstützt](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span><span class="sxs-lookup"><span data-stu-id="0da43-110">Email messages have an attached file of a file type that can't be indexed; in most cases, the file type is [unrecognized or unsupported for indexing](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search)</span></span>
    
- <span data-ttu-id="0da43-111">E-Mail-Nachrichten haben eine angefügte Datei ohne einen gültigen Handler, beispielsweise Bilddateien. Dies ist die häufigste Ursache teilweise indizierten e-Mail-Elemente</span><span class="sxs-lookup"><span data-stu-id="0da43-111">Email messages have an attached file without a valid handler, such as image files; this is the most common cause of partially indexed email items</span></span>
    
- <span data-ttu-id="0da43-112">Zu viele Dateien, die an eine e-Mail-Nachricht angehängt</span><span class="sxs-lookup"><span data-stu-id="0da43-112">Too many files attached to an email message</span></span>
    
- <span data-ttu-id="0da43-113">Eine Datei an eine e-Mail-Nachricht angehängt ist zu groß</span><span class="sxs-lookup"><span data-stu-id="0da43-113">A file attached to an email message is too large</span></span>
    
- <span data-ttu-id="0da43-114">Der Dateityp ist für die Indizierung unterstützt, aber für eine bestimmte Datei ist ein Indizierung Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="0da43-114">The file type is supported for indexing but an indexing error occurred for a specific file</span></span>
    
<span data-ttu-id="0da43-p103">Obwohl variiert, haben die meisten Kunden von Office 365-Organisationen kleiner als 1 % des Inhalts und weniger als 12 % des Inhalts nach Größe, die teilweise indiziert ist. Der Grund für die Differenz zwischen der Lautstärke im Vergleich zur Größe ist, dass größere Dateien steigt die Wahrscheinlichkeit eines mit Inhalten, die nicht vollständig indiziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0da43-p103">Although it varies, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed. The reason for the difference between the volume versus size is that larger files have a higher probability of containing content that can't be completely indexed.</span></span>
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a><span data-ttu-id="0da43-117">Warum wird die Anzahl der teilweise indizierte Elemente für eine Suche geändert?</span><span class="sxs-lookup"><span data-stu-id="0da43-117">Why does the partially indexed item count change for a search?</span></span>

<span data-ttu-id="0da43-p104">Nach dem Ausführen einer Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center, die gesamte Anzahl und Größe der teilweise indizierte Elemente in die Speicherorte, die durchsucht wurden aufgelisteten in das Ergebnis Suchstatistik, die in die ausführlichen Statistiken für angezeigt werden die Suche. Beachten Sie, dass diese *nicht indizierten Elemente* in die Suchstatistik aufgerufen werden. Hier sind einige Punkte, die die Anzahl der teilweise indizierte Elemente auswirken, die in den Suchergebnissen zurückgegeben werden:</span><span class="sxs-lookup"><span data-stu-id="0da43-p104">After you run a Content Search in the Office 365 Security &amp; Compliance Center, the total number and size of partially indexed items in the locations that were searched are listed in the search result statistics that are displayed in the detailed statistics for the search. Note these are called  *unindexed items*  in the search statistics. Here are a few things that will affect the number of partially indexed items that are returned in the search results:</span></span> 
  
- <span data-ttu-id="0da43-p105">Wenn ein Element teilweise indiziert wird und die Suchabfrage entspricht, ist es in der Anzahl von Elementen (und die Größe) der Suchergebnisse und teilweise indizierte Elemente enthalten. Wenn die Ergebnisse dieser Suche gleichen exportiert werden, ist das Element jedoch nur mit den Suchergebnissen enthalten. Es ist nicht als teilweise indizierte Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="0da43-p105">If an item is partially indexed and matches the search query, it's included in both the count (and size) of search result items and partially indexed items. However, when the results of that same search are exported, the item is included only with set of search results; it's not included as a partially indexed item.</span></span>
    
- <span data-ttu-id="0da43-p106">Wenn Sie einen Datumsbereich für eine Suchabfrage (einschließlich es in der Stichwortabfrage) oder mit einer Bedingung angeben, ist nicht in der Anzahl der teilweise indizierte Elemente aller teilweise indizierte Elemente, die nicht den Datumsbereich entspricht enthalten. Nur die teilweise indizierte Elemente, die im Datumsbereich liegen sind in der Anzahl der teilweise indizierte Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="0da43-p106">If you specify a date range for a search query (by including it in the keyword query or by using a condition), any partially indexed item that doesn't match the date range isn't included in the count of partially indexed items. Only the partially indexed items that fall within date range are included in the count of partially indexed items.</span></span>
    
 <span data-ttu-id="0da43-p107">**Hinweis:** Teilweise indizierte Elemente befindet sich im SharePoint und OneDrive Websites *sind nicht* enthalten, die in der Schätzung der teilweise indizierte Elemente, die in die ausführlichen Statistiken für die Suche angezeigt wird. Teilweise indizierte Elemente können jedoch exportiert werden, wenn Sie die Ergebnisse einer Inhaltssuche exportieren. Wenn Sie nur Websites in einer Inhaltssuche die geschätzte Anzahl teilweise gesucht werden beispielsweise indizierte Elemente NULL sein.</span><span class="sxs-lookup"><span data-stu-id="0da43-p107">**Note:** Partially indexed items located in SharePoint and OneDrive sites  *are not*  included in the estimate of partially indexed items that's displayed in the detailed statistics for the search. However, partially indexed items can be exported when you export the results of a Content Search. For example, if you only search sites in a Content Search, the estimated number partially indexed items will be zero.</span></span> 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a><span data-ttu-id="0da43-128">Er das Verhältnis von teilweise indizierte Elemente in Ihrer Organisation</span><span class="sxs-lookup"><span data-stu-id="0da43-128">Calculating the ratio of partially indexed items in your organization</span></span>

<span data-ttu-id="0da43-p108">Um Ihre Organisation die Angriffsfläche teilweise indizierte Elemente zu verstehen, können Sie eine Suche für den gesamten Inhalt in allen Postfächern (mithilfe einer schlüsselwortabfrage leere) ausführen. Im folgenden Beispiel werden 56,208 (4,830 MB) vollständig indizierte Elemente und 470 (316 MB) teilweise indizierte Elemente.</span><span class="sxs-lookup"><span data-stu-id="0da43-p108">To understand your organization's exposure to partially indexed items, you can run a search for all content in all mailboxes (by using a blank keyword query). In the following example below, there are 56,208 (4,830 MB) fully indexed items and 470 (316 MB) partially indexed items.</span></span>
  
![Beispiel für die Suche Statistiken anzeigen indizierte teilweise Elemente](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
<span data-ttu-id="0da43-132">Sie können den Prozentsatz der teilweise indizierte Elemente bestimmen, mithilfe der folgenden Berechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="0da43-132">You can determine the percentage of partially indexed items by using the following calculations.</span></span>
  
 <span data-ttu-id="0da43-133">**Um das Verhältnis von teilweise indizierte Elemente in Ihrer Organisation zu berechnen:**</span><span class="sxs-lookup"><span data-stu-id="0da43-133">**To calculate the ratio of partially indexed items in your organization:**</span></span>

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
<span data-ttu-id="0da43-134">Mit den Suchergebnissen aus dem vorherigen Beispiel,. 84 % aller Postfächer Elemente sind teilweise indiziert.</span><span class="sxs-lookup"><span data-stu-id="0da43-134">By using the search results from the previous example, .84% of all mailboxes items are partially indexed.</span></span>
  
 <span data-ttu-id="0da43-135">**Um den Prozentsatz der Größe des teilweise indizierte Elemente in Ihrer Organisation zu berechnen:**</span><span class="sxs-lookup"><span data-stu-id="0da43-135">**To calculate the percentage of the size of partially indexed items in your organization:**</span></span>

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

<span data-ttu-id="0da43-p109">Damit im vorherigen Beispiel 6.54 % der Gesamtgröße der Postfachelemente teilweise indizierte Elemente gelten. Wie bereits erwähnt, die meisten Office 365-Organisationen, die Kunden weniger als 1 % des Inhalts vom Datenträger und weniger als 12 % des Inhalts nach Größe haben, die teilweise indiziert ist.</span><span class="sxs-lookup"><span data-stu-id="0da43-p109">So in the previous example, 6.54% of the total size of mailbox items are from partially indexed items. As previously stated, most Office 365 organizations customers have less than 1% of content by volume and less than 12% of content by size that is partially indexed.</span></span>

## <a name="working-with-partially-indexed-items"></a><span data-ttu-id="0da43-138">Arbeiten mit teilweise indizierte Elemente</span><span class="sxs-lookup"><span data-stu-id="0da43-138">Working with partially indexed items</span></span>

<span data-ttu-id="0da43-p110">In Fällen, wenn Sie teilweise untersuchen Elemente, um zu überprüfen, dass sie nicht die relevanten Informationen enthalten, können Sie [einen Bericht Inhaltssuche exportieren](export-a-content-search-report.md) müssen enthält, Informationen zu teilweise indizierte Elemente. Wenn Sie einen Bericht Inhaltssuche exportieren, müssen Sie wählen eine der Exportoptionen, die teilweise indizierte Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="0da43-p110">In cases when you need to examine partially items to validate that they don't contain relevant information, you can [export a content search report](export-a-content-search-report.md) that contains information about partially indexed items. When you export a content search report, be sure to choose one of the export options that includes partially indexed items.</span></span> 
  
![Wählen Sie die Option zweite oder dritte teilweise indizierte Elemente exportieren](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
<span data-ttu-id="0da43-p111">Beim Exportieren von Suchergebnissen oder eines Inhaltssuche-Berichts mithilfe einer dieser Optionen enthält der Export ein Berichts mit dem Namen nicht indizierten Items.csv. Dieser Bericht enthält die meisten die gleichen Informationen wie die Datei ResultsLog.csv; die Datei nicht indizierten Items.csv enthält jedoch auch zwei Felder im Zusammenhang mit teilweise indizierte Elemente: **Fehler Tags** und **Fehler-Eigenschaften**. Diese Felder enthalten Informationen über die Indizierung Fehler für jedes teilweise indizierten Element. Mithilfe der Informationen in dieser beiden Felder kann Ihnen bestimmen, ob der Indizierung Fehler für einen bestimmten wirkt sich die Untersuchung auf. Wenn dies der Fall ist, können eine gezielte Inhaltssuche Sie und Abrufen und Ausführen Exportieren bestimmter e-Mail-Nachrichten und SharePoint oder OneDrive-Dokumente, sodass Sie überprüfen können, um zu bestimmen, wenn sie für Ihre Untersuchung relevant sind. Schrittweise Anweisungen finden Sie unter [Vorbereiten einer CSV-Datei für eine gezielte Inhaltssuche in Office 365](csv-file-for-an-id-list-content-search.md).</span><span class="sxs-lookup"><span data-stu-id="0da43-p111">When you export content search results or a content search report using one of these options, the export includes a report named Unindexed Items.csv. This report includes most of the same information as the ResultsLog.csv file; however, the Unindexed Items.csv file also includes two fields related to partially indexed items: **Error Tags** and **Error Properties**. These fields contain information about the indexing error for each partially indexed item. Using the information in these two fields can help you determine whether or not the indexing error for a particular impacts your investigation. If it does, you can perform a targeted content search and retrieve and export specific email messages and SharePoint or OneDrive documents so that you can examine them to determine if they're relevant to your investigation. For step-by-step instructions, see [Prepare a CSV file for a targeted Content Search in Office 365](csv-file-for-an-id-list-content-search.md).</span></span>
  
 <span data-ttu-id="0da43-p112">**Hinweis:** Die Datei nicht indizierten Items.csv enthält auch Felder mit dem Namen **Fehlertyp** und eine **Fehlermeldung**. Dies sind ältere Felder, die Informationen enthalten, die mit den Informationen in den Feldern **Fehler Tags** und **Eigenschaften Fehler** , aber mit weniger detaillierte Informationen ähnlich ist. Sie können diese Vorversion Felder ignorieren.</span><span class="sxs-lookup"><span data-stu-id="0da43-p112">**Note:** The Unindexed Items.csv file also contains fields named **Error Type** and **Error Message**. These are legacy fields that contain information that is similar to the information in the **Error Tags** and **Error Properties** fields, but with less detailed information. You can safely ignore these legacy fields.</span></span> 
  
## <a name="errors-related-to-partially-indexed-items"></a><span data-ttu-id="0da43-151">Fehler im Zusammenhang mit teilweise indizierte Elemente</span><span class="sxs-lookup"><span data-stu-id="0da43-151">Errors related to partially indexed items</span></span>

<span data-ttu-id="0da43-p113">Fehler Tags bestehen aus zwei Teilen Informationen, die Fehlernummer und den Dateityp. Beispielsweise in diesem Fehler/Filetype-Paar:</span><span class="sxs-lookup"><span data-stu-id="0da43-p113">Error tags are made up of two pieces of information, the error and the file type. For example, in this error/filetype pair:</span></span>

```
 parseroutputsize_xls
```

   
 <span data-ttu-id="0da43-p114">`parseroutputsize`ist der Fehler und `xls` ist der Dateityp, der der Fehler aufgetreten ist, klicken Sie auf Datei. Der Dateityp wurde nicht erkannt, oder der Dateityp wurde Fällen waren gilt nicht auf den Fehler, sehen Sie den Wert `noformat` anstelle des Dateityps.</span><span class="sxs-lookup"><span data-stu-id="0da43-p114">`parseroutputsize` is the error and  `xls` is the file type of the file the error occurred on. In cases were the file type wasn't recognized or the file type was doesn't apply to the error, you will see the value  `noformat` in place of the file type.</span></span> 
  
<span data-ttu-id="0da43-156">Es folgt eine Liste der Indizierung Fehler und eine Beschreibung für die Ursache des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="0da43-156">The following is a list of indexing errors and a description of the possible cause of the error.</span></span>
  
|<span data-ttu-id="0da43-157">**Fehlertag**</span><span class="sxs-lookup"><span data-stu-id="0da43-157">**Error tag**</span></span>|<span data-ttu-id="0da43-158">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0da43-158">**Description**</span></span>|
|:-----|:-----|
| `attachmentcount` <br/> |<span data-ttu-id="0da43-159">Eine e-Mail-Nachricht hat zu viele Anlagen, und einige dieser Anlagen werden nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0da43-159">An email message had too many attachments, and some of these attachments weren't processed.</span></span>  <br/> |
| `attachmentdepth` <br/> |<span data-ttu-id="0da43-p115">Der Inhalte Suchfunktion und Dokument-Parser gefunden zu viele Ebenen von Anlagen in anderen Anlagen geschachtelt. Einige dieser Anlagen wurden nicht verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0da43-p115">The content retriever and document parser found too many levels of attachments nested inside other attachments. Some of these attachments were not processed.</span></span>  <br/> |
| `attachmentrms` <br/> |<span data-ttu-id="0da43-162">Eine Anlage konnte nicht Decodierung, da es RMS-geschützten wurde.</span><span class="sxs-lookup"><span data-stu-id="0da43-162">An attachment failed decoding because it was RMS-protected.</span></span>  <br/> |
| `attachmentsize` <br/> |<span data-ttu-id="0da43-163">An eine e-Mail-Nachricht angefügte Datei war zu groß und nicht verarbeitet werden konnte.</span><span class="sxs-lookup"><span data-stu-id="0da43-163">A file attached to an email message was too large and couldn't be processed.</span></span>  <br/> |
| `indexingtruncated` <br/> |<span data-ttu-id="0da43-p116">Beim Schreiben der verarbeiteten e-Mail-Nachricht in den Index der indizierbaren Eigenschaften war zu groß und wurde abgeschnitten. Die abgeschnittenen Eigenschaften sind im Feld Fehlereigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0da43-p116">When writing the processed email message to the index, one of the indexable properties was too large and was truncated. The truncated properties are listed in Error Properties field.</span></span>  <br/> |
| `invalidunicode` <br/> |<span data-ttu-id="0da43-p117">Eine e-Mail-Nachricht enthält Text, der konnte nicht als gültige Unicode verarbeitet werden. Die Indizierung für dieses Element möglicherweise unvollständig.</span><span class="sxs-lookup"><span data-stu-id="0da43-p117">An email message contained text that couldn't be processed as valid Unicode. Indexing for this item may be incomplete.</span></span>  <br/> |
| `parserencrypted` <br/> |<span data-ttu-id="0da43-168">Der Inhalt der Anlage oder ein e-Mail-Nachricht wird verschlüsselt, und Office 365 konnte nicht Decodieren der Inhalte.</span><span class="sxs-lookup"><span data-stu-id="0da43-168">The content of attachment or email message is encrypted, and Office 365 couldn't decode the content.</span></span>  <br/> |
| `parsererror` <br/> |<span data-ttu-id="0da43-p118">Während der Analyse ist ein Unbekannter Fehler aufgetreten. Dies führt in der Regel aus einem Software-Fehler oder einem Dienst Absturz.</span><span class="sxs-lookup"><span data-stu-id="0da43-p118">An unknown error occurred during parsing. This typically results from a software bug or a service crash.</span></span>  <br/> |
| `parserinputsize` <br/> |<span data-ttu-id="0da43-171">Eine Anlage war zu groß für den Parser behandelt, und die Analyse von dieser Anlage nicht erfolgen oder wurde nicht abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0da43-171">An attachment was too large for the parser to handle, and the parsing of that attachment didn't happen or wasn't completed.</span></span>  <br/> |
| `parsermalformed` <br/> |<span data-ttu-id="0da43-p119">Eine Anlage war ungültig und konnte nicht vom Parser behandelt werden. Dieses Ergebnis aus alten Datei kann formatiert, vom inkompatible Software oder Viren vorgeben, etwas andere als angefordert sein erstellte Dateien.</span><span class="sxs-lookup"><span data-stu-id="0da43-p119">An attachment was malformed and couldn't be handled by the parser. This result from can old file formats, files created by incompatible software, or viruses pretending to be something other than claimed.</span></span>  <br/> |
| `parseroutputsize` <br/> |<span data-ttu-id="0da43-174">Die Ausgabe aus der Analyse eines Anlage war zu lang und mussten gekürzt werden.</span><span class="sxs-lookup"><span data-stu-id="0da43-174">The output from the parsing of an attachment was too large and had to be truncated.</span></span>  <br/> |
| `parserunknowntype` <br/> |<span data-ttu-id="0da43-175">Eine Anlage hat einen Dateityp, den Office 365 erkennen konnte nicht.</span><span class="sxs-lookup"><span data-stu-id="0da43-175">An attachment had a file type that Office 365 couldn't detect.</span></span>  <br/> |
| `parserunsupportedtype` <br/> |<span data-ttu-id="0da43-176">Eine Anlage hat einen Dateityp, den Office-365could erkennen, aber Analysieren von diesem Dateityp wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0da43-176">An attachment had a file type that Office 365could detect, but parsing that file type isn't supported.</span></span>  <br/> |
| `propertytoobig` <br/> |<span data-ttu-id="0da43-p120">Der Wert einer e-Mail-Eigenschaft im Exchange Store war zu groß abgerufen werden sollen, und die Nachricht konnte nicht verarbeitet werden. Dies geschieht in der Regel nur auf die Body-Eigenschaft einer e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0da43-p120">The value of an email property in Exchange Store was too large to be retrieved and the message couldn't be processed. This typically only happens to the body property of an email message.</span></span>  <br/> |
| `retrieverrms` <br/> |<span data-ttu-id="0da43-179">Die Suchfunktion Content zum Decodieren einer Nachricht RMS-geschützten ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="0da43-179">The content retriever failed to decode an RMS-protected message.</span></span>  <br/> |
| `wordbreakertruncated` <br/> |<span data-ttu-id="0da43-p121">Zu viele Wörter wurden während der Indizierung in das Dokument identifiziert. Verarbeitung der-Eigenschaft angehalten, wenn den Grenzwert erreicht und die Eigenschaft abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="0da43-p121">Too many words were identified in the document during indexing. Processing of the property stopped when reaching the limit, and the property is truncated.</span></span>  <br/> |
   
<span data-ttu-id="0da43-p122">Fehler Felder wird beschrieben, welche Felder von der im Feld Fehler Tags aufgeführte Verarbeitungsfehler betroffen sind. Wenn Sie eine Eigenschaft wie Suchen `subject` oder `participants`, Fehler im Textkörper der Nachricht wird nicht die Ergebnisse der Suche auswirkt. Dies kann hilfreich sein, wenn genau die teilweise indizierte Elemente bestimmen Sie möglicherweise weiter zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="0da43-p122">Error fields describe which fields are affected by the processing error listed in the Error Tags field. If you're searching a property such as  `subject` or  `participants`, errors in the body of the message won't impact the results of your search. This can be useful when determining exactly which partially indexed items you might need to further investigate.</span></span>
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a><span data-ttu-id="0da43-185">Verwenden eines PowerShell-Skripts zum Ermitteln Ihrer Organisation die Angriffsfläche teilweise indizierten e-Mail-Elemente</span><span class="sxs-lookup"><span data-stu-id="0da43-185">Using a PowerShell script to determine your organization's exposure to partially indexed email items</span></span>

<span data-ttu-id="0da43-p123">Die folgenden Schritten wird gezeigt, wie Sie ein PowerShell-Skript ausführen, sucht nach allen Elementen in alle Exchange-Postfächer, und klicken Sie dann generiert einen Bericht zu Ihrer Organisation Verhältnis teilweise indizierten e-Mail-Elemente (nach Anzahl und Größe) und zeigt die Anzahl der Elemente (und der Dateityp) für jeden Indizierung aufgetretenen. Verwenden Sie die Beschreibung der Fehler Tag im vorherigen Abschnitt, um die Indizierung Fehler zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0da43-p123">The following steps show you how to run a PowerShell script that searches for all items in all Exchange mailboxes, and then generates a report about your organization's ratio of partially indexed email items (by count and by size) and displays the number of items (and their file type) for each indexing error that occurs. Use the error tag descriptions in the previous section to identify the indexing error.</span></span>
  
1. <span data-ttu-id="0da43-188">Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei, mithilfe der Dateiname Suffix. ps1; beispielsweise `PartiallyIndexedItems.ps1`.</span><span class="sxs-lookup"><span data-stu-id="0da43-188">Save the following text to a Windows PowerShell script file by using a filename suffix of .ps1; for example, `PartiallyIndexedItems.ps1`.</span></span>

```
  write-host "**************************************************"
  write-host "     Office 365 Security &amp; Compliance Center      " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "   eDiscovery Partially Indexed Item Statistics   " -foregroundColor yellow -backgroundcolor darkgreen
  write-host "**************************************************"
  " " 
  # Create a search with Error Tags Refinders enabled
  Remove-ComplianceSearch "RefinerTest" -Confirm:$false -ErrorAction 'SilentlyContinue'
  New-ComplianceSearch -Name "RefinerTest" -ContentMatchQuery "size>0" -RefinerNames ErrorTags -ExchangeLocation ALL
  Start-ComplianceSearch "RefinerTest"
  # Loop while search is in progress
  do{
      Write-host "Waiting for search to complete..."
      Start-Sleep -s 5
      $complianceSearch = Get-ComplianceSearch "RefinerTest"
  }while ($complianceSearch.Status -ne 'Completed')
  $refiners = $complianceSearch.Refiners | ConvertFrom-Json
  $errorTagProperties = $refiners.Entries | Get-Member -MemberType NoteProperty
  $partiallyIndexedRatio = $complianceSearch.UnindexedItems / $complianceSearch.Items
  $partiallyIndexedSizeRatio = $complianceSearch.UnindexedSize / $complianceSearch.Size
  " "
  "===== Partially indexed items ====="
  "         Total          Ratio"
  "Count    {0:N0}{1:P2}" -f $complianceSearch.Items.ToString("N0").PadRight(15, " "), $partiallyIndexedRatio
  "Size(GB) {0:N2}{1:P2}" -f ($complianceSearch.Size / 1GB).ToString("N2").PadRight(15, " "), $partiallyIndexedSizeRatio
  " "
  Write-Host ===== Reasons for partially indexed items =====
  foreach($errorTagProperty in $errorTagProperties)
  {
      $name = $refiners.Entries.($errorTagProperty.Name).Name
      $count = $refiners.Entries.($errorTagProperty.Name).TotalCount
      $frag = $name.Split("{_}")
      $errorTag = $frag[0]
      $fileType = $frag[1]
      if ($errorTag -ne $lastErrorTag)
      {
          $errorTag
      }
      "    " + $fileType + " => " + $count
      $lastErrorTag = $errorTag
  }
  
```
   
2. <span data-ttu-id="0da43-189">[Verbinden mit Office 365-Sicherheit &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span><span class="sxs-lookup"><span data-stu-id="0da43-189">[Connect to Office 365 Security &amp; Compliance Center PowerShell](https://go.microsoft.com/fwlink/p/?linkid=627084).</span></span>
    
3. <span data-ttu-id="0da43-190">Sicherheit &amp; Compliance Center PowerShell, wechseln Sie zu dem Ordner, in dem Sie das Skript in Schritt 1 gespeichert, und führen Sie das Skript; Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0da43-190">In Security &amp; Compliance Center PowerShell, go to the folder where you saved the script in step 1, and then run the script; for example:</span></span>

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
<span data-ttu-id="0da43-191">Es folgt ein Beispiel fo die Ausgabe vom Skript zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0da43-191">Here's an example fo the output returned by the script.</span></span>
  
![Beispiel für Ausgabe von Skripts, das einen Bericht zu Ihrer Organisation die Angriffsfläche teilweise generiert indizierte e-Mail-Elemente](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
<span data-ttu-id="0da43-193">Beachten Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0da43-193">Note the following:</span></span>
  
1. <span data-ttu-id="0da43-194">Total Anzahl und Größe von e-Mail-Elementen und Ihrer Organisation Verhältnis teilweise indizierten e-Mail-Elemente (nach Anzahl und Größe)</span><span class="sxs-lookup"><span data-stu-id="0da43-194">The total number and size of email items, and your organization's ratio of partially indexed email items (by count and by size)</span></span>
    
2. <span data-ttu-id="0da43-195">Eine Liste Fehler-Tags und die entsprechenden Dateitypen, bei denen der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="0da43-195">A list error tags and the corresponding file types for which the error occurred.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0da43-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0da43-196">See also</span></span>

[<span data-ttu-id="0da43-197">Teilweise indizierte Elemente in der Inhaltssuche in Office 365</span><span class="sxs-lookup"><span data-stu-id="0da43-197">Partially indexed items in Content Search in Office 365</span></span>](partially-indexed-items-in-content-search.md)
