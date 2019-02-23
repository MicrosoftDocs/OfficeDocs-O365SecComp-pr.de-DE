---
title: Erstellen einer Abfrage zum Auffinden auf Websites gespeicherter vertraulicher Daten
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 3019fbc5-7f15-4972-8d0e-dc182dc7f836
description: Mit Data Loss Prevention (DLP) in SharePoint Online können Sie Dokumente ermitteln, die vertrauliche Daten in Ihrem Mandanten enthalten. Nachdem Sie die Dokumente ermittelt haben, können Sie mit den Dokument Besitzern zusammenarbeiten, um die Daten zu schützen. In diesem Thema können Sie eine Abfrage für die Suche nach vertraulichen Daten unterstützen.
ms.openlocfilehash: 3dc1081d4627f1a26c50eed84f733c31a3f6c194
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217235"
---
# <a name="form-a-query-to-find-sensitive-data-stored-on-sites"></a>Erstellen einer Abfrage zum Auffinden auf Websites gespeicherter vertraulicher Daten

Benutzer speichern häufig vertrauliche Daten wie Kreditkartennummern, Sozialversicherungsnummern oder persönliche Informationen auf ihren Websites und können im Laufe der Zeit eine Organisation mit erheblichen Datenverlustrisiken aussetzen. Dokumente, die auf Websites gespeichert sind, einschließlich OneDrive für Unternehmens-Websites, konnten für Personen außerhalb der Organisation freigegeben werden, die keinen Zugriff auf die Informationen haben sollten. Mit Data Loss Prevention (DLP) in SharePoint Online können Sie Dokumente ermitteln, die vertrauliche Daten in Ihrem Mandanten enthalten. Nachdem Sie die Dokumente ermittelt haben, können Sie mit den Dokument Besitzern zusammenarbeiten, um die Daten zu schützen. In diesem Thema können Sie eine Abfrage für die Suche nach vertraulichen Daten unterstützen.
  
> [!NOTE]
> Die elektronische Erkennung oder eDiscovery und DLP sind Premium-Features, die [SharePoint Online-Plan 2](https://go.microsoft.com/fwlink/?LinkId=510080)erfordern. 
  
## <a name="forming-a-basic-dlp-query"></a>Erstellen einer einfachen DLP-Abfrage

Es gibt drei Teile, aus denen eine grundlegende DLP-Abfrage besteht: Sensitivetype, count Range und Confidence Range. Wie in der folgenden Grafik dargestellt, ist **sensitivetype:\<"\>Type"** erforderlich, und sowohl**|\<count Range\> ** **|\<als auch Konfidenz\> Range** sind optional. 
  
![Beispielabfrage, aufgeteilt in "Erforderlich" und "Optional"](media/DLP-query-example-text.png)
  
### <a name="sensitive-type---required"></a>Typ vertraulicher Informationen - erforderlich

Was ist also jeder Anteil? SharePoint DLP-Abfragen beginnen in der `SensitiveType:"` Regel mit der Eigenschaft und dem Namen eines Informationstyps aus dem Inventar der vertraulichen `"` [Informationstypen](https://go.microsoft.com/fwlink/?LinkID=509999)und enden mit a. Sie können auch den Namen eines [benutzerdefinierten Typs für vertrauliche Informationen](create-a-custom-sensitive-information-type.md) verwenden, den Sie für Ihre Organisation erstellt haben. Sie suchen beispielsweise nach Dokumenten, die Kreditkartennummern enthalten. In einer solchen Instanz würden Sie das folgende Format verwenden: `SensitiveType:"Credit Card Number"`. Da Sie nicht count Range oder Confidence Range eingeschlossen haben, gibt die Abfrage jedes Dokument zurück, in dem eine Kreditkartennummer erkannt wird. Dies ist die einfachste Abfrage, die Sie ausführen können, und es werden die meisten Ergebnisse zurückgegeben. Beachten Sie, dass die Rechtschreibung und der Abstand des vertraulichen Typs wichtig sind. 
  
### <a name="ranges---optional"></a>Bereiche - optional

Beide der nächsten beiden Teile sind Bereiche, lassen Sie uns also schnell untersuchen, wie ein Bereich aussieht. In SharePoint DLP-Abfragen wird ein grundlegender Wert durch zwei durch zwei Punkte getrennte Zahlen dargestellt, die wie `[number]..[number]`folgt aussehen:. Wenn `10..20` beispielsweise verwendet wird, erfasst dieser Zeitraum Zahlen von 10 bis 20. Es gibt viele verschiedene Kombinations Bereiche, die in diesem Thema behandelt werden. 
  
Fügen wir der Abfrage einen count-Range hinzu. Sie können count Range verwenden, um die Anzahl der Vorkommen von vertraulichen Informationen zu definieren, die ein Dokument enthalten muss, bevor es in den Abfrageergebnissen enthalten ist. Wenn Sie beispielsweise möchten, dass Ihre Abfrage nur Dokumente zurückgibt, die genau fünf Kreditkartennummern enthalten, verwenden `SensitiveType:"Credit Card Number|5"`Sie Folgendes:. Count Range kann auch bei der Identifizierung von Dokumenten helfen, die einen hohen Risikograd aufweisen. Beispielsweise kann Ihre Organisation Dokumente mit mindestens fünf Kreditkartennummern als hohes Risiko betrachten. Zum Suchen nach Dokumenten, die dieses Kriterium erfüllen, verwenden Sie diese `SensitiveType:"Credit Card Number|5.."`Abfrage:. Alternativ können Sie Dokumente mit mindestens fünf Kreditkartennummern mithilfe dieser Abfrage suchen: `SensitiveType:"Credit Card Number|..5"`. 
  
#### <a name="confidence-range"></a>Konfidenzbereich

Schließlich ist der Vertrauensbereich die Vertrauensebene, bei der der erkannte vertrauliche Typ tatsächlich eine Übereinstimmung darstellt. Die Werte für den Konfidenzbereich funktionieren ähnlich wie bei count Range. Sie können eine Abfrage ohne einen count-Range bilden. Wenn Sie beispielsweise nach Dokumenten mit einer beliebigen Anzahl von Kreditkartennummern suchen möchten, solange der Konfidenz Wert 85 Prozent oder höher ist, verwenden Sie diese Abfrage: `SensitiveType:"Credit Card Number|*|85.."`. 
  
> [!IMPORTANT]
> Das Sternchen ( `*`) ist ein Platzhalterzeichen, das bedeutet, dass ein beliebiger Wert funktioniert. Sie können das Platzhalterzeichen ( `*`) entweder im count-oder im Konfidenzbereich verwenden, jedoch nicht in einem vertraulichen Typ. 
  
### <a name="additional-query-properties-and-search-operators-available-in-the-ediscovery-center"></a>Im eDiscovery Center stehen weitere Abfrageeigenschaften und Suchoperatoren zur Verfügung.

DLP in SharePoint bietet außerdem eine Einführung in die LastSensitiveContentScan-Eigenschaft, die Sie bei der Suche nach Dateien unterstützenkann, die innerhalb eines bestimmten Zeitrahmens gescannt werden. Abfragebeispiele mit der `LastSensitiveContentScan` -Eigenschaft finden Sie in den Beispielen für [komplexe Abfragen](form-a-query-to-find-sensitive-data-stored-on-sites.md#BKMK_ExamplesOfComplexQueries) im nächsten Abschnitt. 
  
Sie können nicht nur DLP-spezifische Eigenschaften verwenden, um eine Abfrage zu erstellen, sondern auch standardmäßige SharePoint `Author` eDiscovery `FileExtension`-Sucheigenschaften wie oder. Sie können Operatoren verwenden, um komplexe Abfragen zu erstellen. Eine Liste der verfügbaren Eigenschaften und Operatoren finden Sie unter [using Search Properties and Operators with eDiscovery](https://go.microsoft.com/fwlink/?LinkId=510093) Blog Post. 
  
## <a name="examples-of-complex-queries"></a>Beispiele

In den folgenden Beispielen werden verschiedene vertrauliche Typen, Eigenschaften und Operatoren verwendet, um zu veranschaulichen, wie Sie Ihre Abfragen verfeinern können, um genau zu finden, wonach Sie suchen.
  
|**Abfrage**|**Erläuterung**|
|:-----|:-----|
| `SensitiveType:"International Banking Account Number (IBAN)"` <br/> |Der Name mag seltsam erscheinen, weil er so lang ist, aber er ist der richtige Name für diesen vertraulichen Typ. Stellen Sie sicher, dass Sie genaue Namen aus den [Typen der vertraulichen Informationen](https://go.microsoft.com/fwlink/?LinkID=509999)verwenden. Sie können auch den Namen eines [benutzerdefinierten Typs für vertrauliche Informationen](create-a-custom-sensitive-information-type.md) verwenden, den Sie für Ihre Organisation erstellt haben.<br/> |
| `SensitiveType:"Credit Card Number|1..4294967295|1..100"` <br/> |Dadurch werden Dokumente mit mindestens einer Übereinstimmung mit dem vertraulichen Typ "Kreditkartennummer" zurückgegeben. Die Werte für die einzelnen Bereiche sind die jeweiligen minimal-und Maximalwerte. Eine einfachere Möglichkeit zum Schreiben dieser Abfrage ist `SensitiveType:"Credit Card Number"`, aber wo ist der Spaß daran?<br/> |
| `SensitiveType:"Credit Card Number| 5..25" AND LastSensitiveContentScan:"8/11/2018..8/13/2018"` <br/> |Dadurch werden Dokumente mit 5-25 Kreditkartennummern zurückgegeben, die vom 11. August 2018 bis 13. August 2018 gescannt wurden.  <br/> |
| `SensitiveType:"Credit Card Number| 5..25" AND LastSensitiveContentScan:"8/11/2018..8/13/2018" NOT FileExtension:XLSX` <br/> |Dadurch werden Dokumente mit 5-25 Kreditkartennummern zurückgegeben, die vom 11. August 2018 bis 13. August 2018 gescannt wurden. Dateien mit einer XLSX-Erweiterung sind nicht in den Abfrageergebnissen enthalten.  `FileExtension` ist eine von vielen Eigenschaften, die Sie in eine Abfrage aufnehmen können. Weitere Informationen finden Sie unter [Verwenden von Sucheigenschaften und Operatoren mit eDiscovery](https://go.microsoft.com/fwlink/?LinkId=510093).<br/> |
| `SensitiveType:"Credit Card Number" OR SensitiveType:"U.S. Social Security Number (SSN)"` <br/> |Diese Abfrage gibt Dokumente zurück, die entweder eine Kreditkartennummer oder US-Sozialversicherungsnummer enthalten.  <br/> |
   
## <a name="examples-of-queries-to-avoid"></a>Beispiele

Nicht alle Abfragen werden gleich erstellt. In der folgenden Tabelle finden Sie Beispiele für Abfragen, die nicht mit DLP in SharePoint funktionieren und warum.
  
|**Nicht unterstützte Abfrage**|**Reason**|
|:-----|:-----|
| `SensitiveType:"Credit Card Number|.."` <br/> |Sie müssen mindestens eine Zahl hinzufügen.  <br/> |
| `SensitiveType:"NotARule"` <br/> |"NotARule" ist kein gültiger vertraulicher Typname. Nur Namen in den [Typen vertraulicher Informationen](https://go.microsoft.com/fwlink/?LinkID=509999) werden in DLP-Abfragen verwendet.<br/> |
| `SensitiveType:"Credit Card Number|0"` <br/> |NULL ist weder als Minimalwert noch als Maximalwert in einem Range-Objekt gültig.  <br/> |
| `SensitiveType:"Credit Card Number"` <br/> |Es ist möglicherweise schwierig zu erkennen, aber es gibt zusätzlichen Leerraum zwischen "Guthaben" und "Karte", der die Abfrage ungültig macht. Verwenden Sie genaue vertrauliche Typnamen aus dem [Inventar der vertraulichen Informationstypen](https://go.microsoft.com/fwlink/?LinkID=509999).<br/> |
| `SensitiveType:"Credit Card Number|1. .3"` <br/> |Die zwei-Perioden-Teil sollte nicht durch ein Leerzeichengetrennt werden.  <br/> |
| `SensitiveType:"Credit Card Number| |1..|80.."` <br/> |Es gibt zu viele Pipe-Trennzeichen (|). Folgen Sie stattdessen diesem Format:`SensitiveType: "Credit Card Number|1..|80.."` <br/> |
| `SensitiveType:"Credit Card Number|1..|80..101"` <br/> |Da Zuverlässigkeitswerte einen Prozentsatz darstellen, dürfen Sie 100 nicht überschreiten. Wählen Sie stattdessen eine Zahl zwischen 1 und 100 aus.  <br/> |
   
## <a name="for-more-information"></a>Weitere Informationen

[Wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md)
  
[Ausführen einer Inhaltssuche im Office 365 Security &amp; Compliance Center](run-a-content-search-in-the-security-and-compliance-center.md)
  
[Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
  

