---
title: Untersuchen von teilweise indizierten Elementen in Office 365 eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 1/26/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: 4e8ff113-6361-41e2-915a-6338a7e2a1ed
description: Teilweise indizierte Elemente (auch Aufruf von nicht indizierten Elementen) sind Exchange-Postfachelemente und Dokumente auf SharePoint-und OneDrive-Websites, die aus irgendeinem Grund nicht vollständig für die Inhaltssuche indiziert wurden. In diesem Artikel erfahren Sie, warum Elemente nicht für die Suche indiziert werden können und als teilweise indizierte Elemente zurückgegeben werden, Suchfehler für teilweise indizierte Elemente identifizieren und ein PowerShell-Skript verwenden, um die Exposition ihrer Organisation gegenüber teilweise indizierten e-Mails zu ermitteln. Elemente.
ms.openlocfilehash: d6b1326498780a5d40e49ff22aa1ac7d16bee8e4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254128"
---
# <a name="investigating-partially-indexed-items-in-office-365-ediscovery"></a>Untersuchen von teilweise indizierten Elementen in Office 365 eDiscovery

Eine Inhaltssuche, die Sie im Security & Compliance Center ausführen, enthält automatisch teilweise indizierte Elemente in den geschätzten Suchergebnissen, wenn Sie eine Suche ausführen. Teilweise indizierte Elemente sind Exchange-Postfachelemente und Dokumente auf SharePoint-und OneDrive für Business-Websites, die aus irgendeinem Grund nicht vollständig für die Suche indiziert wurden. Die meisten e-Mail-Nachrichten und Website Dokumente werden erfolgreich indiziert, da Sie in die [Indizierungs Grenzen für e-Mail-Nachrichten](limits-for-content-search.md#indexing-limits-for-email-messages)fallen. Einige Elemente können jedoch diese Indizierungs Grenzwerte überschreiten und teilweise indiziert werden. Im folgenden finden Sie weitere Gründe, warum Elemente nicht für die Suche indiziert werden können und beim Ausführen einer Inhaltssuche als teilweise indizierte Elemente zurückgegeben werden:
  
- E-Mail-Nachrichten verfügen über eine angefügte Datei mit einem Dateityp, der nicht indiziert werden kann. in den meisten Fällen wird der Dateityp nicht [erkannt oder für die Indizierung nicht unterstützt](partially-indexed-items-in-content-search.md#file-types-not-indexed-for-search) .
    
- E-Mail-Nachrichten haben eine angefügte Datei ohne einen gültigen Handler, wie Bilddateien; Dies ist die häufigste Ursache für teilweise indizierte e-Mail-Elemente
    
- Zu viele an eine e-Mail-Nachricht angefügte Dateien
    
- Eine an eine e-Mail-Nachricht angefügte Datei ist zu umfangreich
    
- Der Dateityp wird für die Indizierung unterstützt, aber für eine bestimmte Datei ist ein Indizierungsfehler aufgetreten.
    
Obwohl es unterschiedlich ist, haben die meisten Office 365-Organisationen Kunden weniger als 1% der Inhalte nach Volumen und weniger als 12% der Inhalte nach Größe, die teilweise indiziert sind. Der Unterschied zwischen dem Volume und der Größe besteht darin, dass größere Dateien eine höhere Wahrscheinlichkeit haben, Inhalte zu enthalten, die nicht vollständig indiziert werden können.
  
## <a name="why-does-the-partially-indexed-item-count-change-for-a-search"></a>Warum ändert sich die Anzahl der teilweise indizierten Elemente für eine Suche?

Nachdem Sie eine Inhaltssuche im Security & Compliance Center ausgeführt haben, werden die Gesamtanzahl und Größe der teilweise indizierten Elemente an den durchsuchten Speicherorten in den Suchergebnis Statistiken aufgeführt, die in der detaillierten Statistik für die Suche angezeigt werden. Hinweis Diese werden als nicht *indizierte Elemente* in der Suchstatistik bezeichnet. Es folgen einige Aspekte, die sich auf die Anzahl der teilweise indizierten Elemente auswirken, die in den Suchergebnissen zurückgegeben werden: 
  
- Wenn ein Element teilweise indiziert ist und mit der Suchabfrage übereinstimmt, ist es sowohl in der Anzahl (als auch in der Größe) von Suchergebnis Elementen und teilweise indizierten Elementen enthalten. Wenn jedoch die Ergebnisse derselben Suche exportiert werden, wird das Element nur mit der Gruppe der Suchergebnisse eingeschlossen. Sie ist nicht als teilweise indiziertes Element enthalten.
    
- Wenn Sie einen Datumsbereichs für eine Suchabfrage angeben (indem Sie ihn in die Stichwortabfrage einschließen oder eine Bedingung verwenden), wird ein teilweise indiziertes Element, das nicht mit dem Datumsbereichs übereinstimmt, nicht in die Anzahl der teilweise indizierten Elemente eingeschlossen. Nur die teilweise indizierten Elemente, die innerhalb des Datumsbereichs liegen, sind in der Anzahl der teilweise indizierten Elemente enthalten.
    
 **Hinweis:** Teilweise indizierte Elemente in SharePoint-und OneDrive-Websites *sind nicht* in der Schätzung der teilweise indizierten Elemente enthalten, die in der detaillierten Statistik für die Suche angezeigt werden. Teilweise indizierte Elemente können jedoch exportiert werden, wenn Sie die Ergebnisse einer Inhaltssuche exportieren. Wenn Sie beispielsweise nur Websites in einer Inhaltssuche durchsuchen, ist die geschätzte Anzahl teilweise indizierter Elemente NULL. 
  
## <a name="calculating-the-ratio-of-partially-indexed-items-in-your-organization"></a>Berechnen des Verhältnisses von teilweise indizierten Elementen in Ihrer Organisation

Um die Exposition ihrer Organisation gegenüber teilweise indizierten Elementen zu verstehen, können Sie eine Suche nach allen Inhalten in allen Postfächern ausführen (mithilfe einer leeren Stichwortabfrage). Im folgenden Beispiel unten gibt es 56.208 (4.830 MB) vollständig indizierte Elemente und 470 (316 MB) teilweise indizierte Elemente.
  
![Beispiel für Suchstatistiken mit teilweise indizierten Elementen](media/0f6a5cf7-4c98-44a0-a0dd-5aed67124641.png)
  
Sie können den Prozentsatz der teilweise indizierten Elemente mithilfe der folgenden Berechnungen ermitteln.
  
 **So berechnen Sie das Verhältnis von teilweise indizierten Elementen in Ihrer Organisation:**

`(Total number of partially indexed items/Total number of items) x 100`


`(470/56,208) x 100 = 0.84%`
 
Mithilfe der Suchergebnisse aus dem vorherigen Beispiel werden. 84% aller Postfächer-Elemente teilweise indiziert.
  
 **So berechnen Sie den prozentualen Anteil der Teil indizierten Elemente in Ihrer Organisation:**

`(Size of all partially indexed items/Size of all items) x 100`

`(316 MB/4830 MB) x 100 = 6.54%`

Im vorherigen Beispiel sind 6,54% der Gesamtgröße von Postfachelementen aus teilweise indizierten Elementen. Wie bereits erwähnt, haben die meisten Kunden von Office 365-Organisationen weniger als 1% der Inhalte nach Volumen und weniger als 12% der Inhalte nach Größe, die teilweise indiziert sind.

## <a name="working-with-partially-indexed-items"></a>Arbeiten mit teilweise indizierten Elementen

In Fällen, in denen Sie Teilelemente überprüfen müssen, um zu überprüfen, ob Sie keine relevanten Informationen enthalten, können Sie [einen Inhalts Suchbericht exportieren](export-a-content-search-report.md) , der Informationen zu teilweise indizierten Elementen enthält. Wenn Sie einen Inhalts Suchbericht exportieren, achten Sie darauf, eine der Exportoptionen zu wählen, die teilweise indizierte Elemente enthalten. 
  
![Auswählen der zweiten oder dritten Option zum Exportieren teilweise indizierter Elemente](media/624a62b4-78f7-4329-ab5d-e62e3b369885.png)
  
Wenn Sie Inhalts Suchergebnisse oder einen Inhalts Suchbericht mithilfe einer dieser Optionen exportieren, enthält der Export einen Bericht mit dem Namen "unindizierte Elemente. csv". Dieser Bericht enthält die meisten der gleichen Informationen wie die ResultsLog. CSV-Datei; die unindizierte Items. CSV-Datei enthält jedoch auch zwei Felder im Zusammenhang mit teilweise indizierten Elementen: **Fehler Tags** und **Fehlereigenschaften**. Diese Felder enthalten Informationen zum Indizierungsfehler für jedes teilweise indizierte Element. Mithilfe der Informationen in diesen beiden Feldern können Sie ermitteln, ob sich der Indizierungsfehler für eine bestimmte Auswirkung auf ihre Untersuchung auswirkt. Wenn dies der Fall ist, können Sie eine gezielte Inhaltssuche durchführen und bestimmte e-Mail-Nachrichten und SharePoint-oder OneDrive-Dokumente abrufen und exportieren, damit Sie Sie überprüfen können, um festzustellen, ob Sie für Ihre Untersuchung relevant sind. Schrittweise Anleitungen finden Sie unter [Vorbereiten einer CSV-Datei für eine gezielte Inhaltssuche in Office 365](csv-file-for-an-id-list-content-search.md).
  
 **Hinweis:** Die Datei unindizierte Items. csv enthält auch Felder mit dem Namen **Error Type** und **Fehlermeldung**. Hierbei handelt es sich um Legacy Felder, die Informationen enthalten, die den Informationen in den Feldern **Error Tags** and **Error Properties** ähneln, jedoch mit wenig detaillierten Informationen. Sie können diese Legacy Felder bedenkenlos ignorieren. 
  
## <a name="errors-related-to-partially-indexed-items"></a>Fehler im Zusammenhang mit teilweise indizierten Elementen

Fehler Tags bestehen aus zwei Informationen, dem Fehler und dem Dateityp. Beispielsweise in diesem Fehler/filetype-paar:

```
 parseroutputsize_xls
```

   
 `parseroutputsize`ist der Fehler und `xls` ist der Dateityp der Datei, in der der Fehler aufgetreten ist. In Fällen, in denen der Dateityp nicht erkannt wurde oder der Dateityp nicht auf den Fehler angewendet wurde, wird der Wert `noformat` anstelle des Dateityps angezeigt. 
  
Es folgt eine Liste der Indizierungsfehler und eine Beschreibung der möglichen Ursache für den Fehler.
  
|**Fehlertag**|**Beschreibung**|
|:-----|:-----|
| `attachmentcount` <br/> |Eine e-Mail-Nachricht hatte zu viele Anlagen, und einige dieser Anlagen wurden nicht verarbeitet.  <br/> |
| `attachmentdepth` <br/> |Der Inhalts-Retriever und der Dokumentparser haben zu viele Stufen von Anlagen gefunden, die in anderen Anlagen geschachtelt sind. Einige dieser Anlagen wurden nicht verarbeitet.  <br/> |
| `attachmentrms` <br/> |Fehler bei der Decodierung einer Anlage, da Sie RMS-geschützt war.  <br/> |
| `attachmentsize` <br/> |Eine an eine e-Mail-Nachricht angefügte Datei war zu umfangreich und konnte nicht verarbeitet werden.  <br/> |
| `indexingtruncated` <br/> |Beim Schreiben der verarbeiteten e-Mail-Nachricht in den Index war eine der Indexable-Eigenschaften zu umfangreich und wurde abgeschnitten. Die abgeschnittenen Eigenschaften werden im Feld Fehlereigenschaften aufgelistet.  <br/> |
| `invalidunicode` <br/> |Eine e-Mail-Nachricht enthielt Text, der nicht als gültige Unicode-Verarbeitung verarbeitet werden konnte. Die Indizierung für dieses Element ist möglicherweise unvollständig.  <br/> |
| `parserencrypted` <br/> |Der Inhalt der Anlage oder e-Mail-Nachricht ist verschlüsselt, und Office 365 konnte den Inhalt nicht decodieren.  <br/> |
| `parsererror` <br/> |Während der Analyse ist ein unbekannter Fehler aufgetreten. Dies resultiert in der Regel aus einem Softwarefehler oder einem Dienst Absturz.  <br/> |
| `parserinputsize` <br/> |Eine Anlage war für den Parser zu umfangreich, und die Analyse der Anlage wurde nicht ausgeführt oder wurde nicht abgeschlossen.  <br/> |
| `parsermalformed` <br/> |Eine Anlage war fehlerhaft und konnte vom Parser nicht verarbeitet werden. Dieses Ergebnis kann aus alten Dateiformaten, Dateien, die von inkompatibler Software erstellt wurden, oder Viren, die vorgeben, etwas anderes als behauptet zu werden.  <br/> |
| `parseroutputsize` <br/> |Die Ausgabe der Analyse einer Anlage war zu umfangreich und musste abgeschnitten werden.  <br/> |
| `parserunknowntype` <br/> |Eine Anlage hatte einen Dateityp, der von Office 365 nicht gefunden werden konnte.  <br/> |
| `parserunsupportedtype` <br/> |Eine Anlage hatte einen Dateityp, den Office 365could erkannte, aber die Analyse dieses Dateityps wird nicht unterstützt.  <br/> |
| `propertytoobig` <br/> |Der Wert einer e-Mail-Eigenschaft im Exchange-Speicher war zu umfangreich, um abgerufen werden zu können, und die Nachricht konnte nicht verarbeitet werden. Dies geschieht in der Regel nur für die Body-Eigenschaft einer e-Mail-Nachricht.  <br/> |
| `retrieverrms` <br/> |Der Inhaltsabruf Fehler beim Decodieren einer RMS-geschützten Nachricht.  <br/> |
| `wordbreakertruncated` <br/> |Zu viele Wörter wurden im Dokument während der Indizierung identifiziert. Die Verarbeitung der Eigenschaft wurde beendet, wenn die Grenze erreicht wurde, und die Eigenschaft wurde abgeschnitten.  <br/> |
   
Fehler Felder beschreiben, welche Felder von dem im Feld Fehler Tags aufgeführten Verarbeitungsfehler betroffen sind. Wenn Sie eine Eigenschaft wie `subject` oder `participants`durchsuchen, wirken sich Fehler im Textkörper der Nachricht nicht auf die Ergebnisse Ihrer Suche aus. Dies kann hilfreich sein, wenn Sie genau ermitteln möchten, welche teilweise indizierten Elemente Sie möglicherweise weiter untersuchen müssen.
  
## <a name="using-a-powershell-script-to-determine-your-organizations-exposure-to-partially-indexed-email-items"></a>Verwenden eines PowerShell-Skripts, um die Exposition ihrer Organisation gegenüber teilweise indizierten e-Mail-Elementen zu ermitteln

In den folgenden Schritten wird gezeigt, wie Sie ein PowerShell-Skript ausführen, das nach allen Elementen in allen Exchange-Postfächern sucht, und dann einen Bericht über das Verhältnis ihrer Organisation zu teilweise indizierten e-Mail-Elementen (nach Anzahl und Größe) generiert und die Anzahl der Elemente anzeigt (und Ihren Dateityp) für jeden auftretenden Indizierungsfehler. Verwenden Sie die Beschreibungen des Fehler Tags im vorherigen Abschnitt, um den Indizierungsfehler zu identifizieren.
  
1. Speichern Sie den folgenden Text in einer Windows PowerShell-Skriptdatei mithilfe des Dateinamen Suffixes ". ps1". Beispiel: `PartiallyIndexedItems.ps1`.

```
  write-host "**************************************************"
  write-host "     Security & Compliance Center      " -foregroundColor yellow -backgroundcolor darkgreen
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
   
2. Stellen [Sie eine Verbindung mit Security _AMP_ Compliance Center PowerShell her](https://go.microsoft.com/fwlink/p/?linkid=627084).
    
3. Wechseln Sie im Security & Compliance Center PowerShell zu dem Ordner, in dem Sie das Skript in Schritt 1 gespeichert haben, und führen Sie das Skript aus; Zum Beispiel:

    ```
    .\PartiallyIndexedItems.ps1
    ```
   
Nachfolgend finden Sie ein Beispiel für die vom Skript zurückgegebene Ausgabe.
  
![Beispiel für die Ausgabe eines Skripts, das einen Bericht über die Exposition ihrer Organisation bei teilweise indizierten e-Mail-Elementen generiert.](media/aeab5943-c15d-431a-bdb2-82f135abc2f3.png)
  
Beachten Sie Folgendes:
  
1. Die Gesamtanzahl und Größe von e-Mail-Elementen und das Verhältnis ihrer Organisation zu teilweise indizierten e-Mail-Elementen (nach Anzahl und Größe)
    
2. Eine Liste der Fehler Tags und die entsprechenden Dateitypen, für die der Fehler aufgetreten ist.
  
## <a name="see-also"></a>Siehe auch

[Teilweise indizierte Elemente in der Inhaltssuche in Office 365](partially-indexed-items-in-content-search.md)
