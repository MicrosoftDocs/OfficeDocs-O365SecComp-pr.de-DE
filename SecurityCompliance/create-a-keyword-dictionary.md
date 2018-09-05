---
title: Erstellen eines Schlüsselwörterbuchs
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Priority
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: c8a95d1b-c3b6-4613-98ab-0331d1872cf3
description: Um vertrauliche Informationen identifizieren zu können, muss manchmal nach Schlüsselwörtern gesucht werden, insbesondere, wenn allgemeine Inhalte (z. B. Kommunikation im Bereich Gesundheitswesen) oder unangemessene bzw. obszöne Sprache identifiziert werden. Sie können zwar Schlüsselwortlisten in vertraulichen Informationstypen erstellen, diese sind aber im Hinblick auf ihre Größe eingeschränkt und erfordern zum Erstellen oder Ändern eine Bearbeitung der XML-Daten. Schlüsselwörterbücher bieten eine einfachere Verwaltung von Schlüsselwörtern und sind für viel größere Inhalte geeignet; es werden bis zu 100.000 Begriffe pro Wörterbuch unterstützt.
ms.openlocfilehash: 3a6557e14a3dd8bdc9e803915ea460c1fbda704b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013989"
---
# <a name="create-a-keyword-dictionary"></a>Erstellen eines Schlüsselwörterbuchs

Durch die Verhinderung von Datenverlusten (Data Loss Prevention, DLP) in Office 365 können vertrauliche Informationen identifiziert, überwacht und geschützt werden. Um vertrauliche Informationen identifizieren zu können, muss manchmal nach Schlüsselwörtern gesucht werden, insbesondere, wenn allgemeine Inhalte (z. B. Kommunikation im Bereich Gesundheitswesen) oder unangemessene bzw. obszöne Sprache identifiziert werden. Sie können zwar Schlüsselwortlisten in vertraulichen Informationstypen erstellen, diese sind aber im Hinblick auf ihre Größe eingeschränkt und erfordern zum Erstellen oder Ändern eine Bearbeitung der XML-Daten. Schlüsselwörterbücher bieten eine einfachere Verwaltung von Schlüsselwörtern und sind für viel größere Inhalte geeignet; es werden bis zu 100.000 Begriffe pro Wörterbuch unterstützt.
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a>Grundlegende Schritte zum Erstellen eines Schlüsselwörterbuchs

Die Schlüsselwörter für Ihr Wörterbuch können aus einer Vielzahl von Quellen stammen, meistens aber aus einer Datei (etwa einer CSV- oder TXT-Liste), aus einer Liste, die Sie direkt in das Cmdlet eingeben, oder aus einem vorhandenen Wörterbuch. Befolgen Sie beim Erstellen eines Schlüsselwörterbuchs die folgenden Kernschritte:
  
1. **Herstellen einer Verbindung mit Security &amp; Compliance Center PowerShell**: Weitere Informationen finden Sie in [diesem Thema](https://go.microsoft.com/fwlink/p/?linkid=799771).
    
2. **Definieren oder Laden der Schlüsselwörter aus der gewünschten Quelle**: Das Cmdlet zum Erstellen eines Schlüsselwörterbuchs akzeptiert eine durch Trennzeichen getrennte Liste von Schlüsselwörtern, dieser Schritt kann also in Abhängigkeit davon, woher Ihre Schlüsselwörter stammen, geringfügig anders sein. 
    
3. **Codieren der Schlüsselwörter**: Nach dem Laden werden diese in ein Bytearray konvertiert, bevor sie importiert werden. 
    
4. **Erstellen des Wörterbuchs**: Wählen Sie einen Namen und eine Beschreibung aus, und erstellen Sie das Wörterbuch. 
    
## <a name="create-a-keyword-dictionary-from-a-file"></a>Erstellen eines Schlüsselwörterbuchs aus einer Datei

Wenn Sie ein großes Wörterbuch erstellen müssen, werden dafür häufig Schlüsselwörter aus einer Datei oder aus einer Liste verwendet, die von einer anderen Quelle exportiert wurde. In diesem Fall erstellen Sie ein Schlüsselwörterbuch mit einer Liste unangemessener Begriffe, die in externen E-Mails gefunden werden sollen. Zunächst müssen Sie [eine Verbindung zu Security &amp; Compliance Center PowerShell herstellen](https://go.microsoft.com/fwlink/p/?linkid=799771).
  
1. Kopieren Sie die Schlüsselwörter in eine Textdatei, und stellen Sie sicher, dass sich jedes Schlüsselwort in einer separaten Zeile befindet.
    
2. Speichern Sie die Textdatei in Unicode-Codierung: Im Editor \> **Speichern als** \> **Codierung** \> **Unicode**.
    
3. Lesen Sie die Datei in eine Variable, indem Sie das folgende Cmdlet ausführen:
    
  ```
  $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
  ```

4. Erstellen Sie das Wörterbuch, indem Sie das folgende Cmdlet ausführen:
    
  ```
  New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
  ```

## <a name="modifying-an-existing-keyword-dictionary"></a>Ändern eines vorhandenen Schlüsselwörterbuchs

Vielleicht müssen Sie Schlüsselwörter in einem Ihrer Schlüsselwörterbucher ändern oder eines der integrierten Wörterbücher ändern. In diesem Beispiel ändern wir einige Ausdrücke in PowerShell, speichern die Ausdrücke lokal, wo Sie sie in einem Editor bearbeiten können, und aktualisieren dann die vorhandenen, früheren Ausdrücke. Rufen Sie zunächst das Wörterbuchobjekt ab:
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

Durch Drucken von `$dict` werden die verschiedenen Variablen angezeigt. Die eigentlichen Schlüsselwörter werden in einem Objekt am Back-End gespeichert, `$dict.KeywordDictionary` enthält aber eine Zeichenfolgendarstellung von diesen, die Sie zum Ändern des Wörterbuchs verwenden. Bevor Sie das Wörterbuch ändern, müssen Sie die Begriffe mit der `.split(',')`-Methode wieder in ein Array konvertieren. Danach entfernen Sie die ungewünschten Leerzeichen zwischen den Schlüsselwörtern mithilfe der `.trim()`-Methode, sodass nur die Schlüsselwörter übrig bleiben, mit denen Sie arbeiten möchten. 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

Jetzt entfernen Sie einige Ausdrücke aus dem Wörterbuch. Da das Beispielwörterbuch nur einige Schlüsselwörter enthält, können Sie diesen Schritt auch überspringen und mit dem Exportieren des Wörterbuchs und dem Bearbeiten im Editor fortfahren. Wörterbücher enthalten aber in der Regel eine große Textmenge, daher erfahren Sie zunächst, wie diese in PowerShell ganz einfach bearbeiten werden.
  
Im letzten Schritt haben Sie die Schlüsselwörter in einem Array gespeichert. Es gibt mehrere Möglichkeiten, um [Elemente aus einem Array zu entfernen](https://go.microsoft.com/fwlink/p/?linkid=852620). Der Einfachheit halber erstellen Sie aber ein Array der Ausdrücke, die Sie aus dem Wörterbuch entfernen möchten, und kopieren dann nur die Wörterbuchbegriffe dort hinein, die sich nicht in der Liste der zu entfernenden Ausdrücke befinden.
  
Führen Sie den Befehl  `$terms` aus, um die aktuelle Liste von Ausdrücken anzuzeigen. Die Ausgabe des Befehls sieht wie folgt aus: 
  
```
aarskog's syndrome
abandonment
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipoproteinemia
abiotrophy
ablatio
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

Führen Sie diesen Befehl aus, um die Ausdrücke anzugeben, die Sie entfernen möchten:
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

Führen Sie diesen Befehl, um die Ausdrücke tatsächlich aus der Liste zu entfernen:
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

Führen Sie den Befehl  `$updatedTerms` aus, um die aktualisierte Liste von Ausdrücken anzuzeigen. Die Ausgabe des Befehls sieht wie folgt aus (die angegebenen Ausdrücke wurden entfernt): 
  
```
aarskog's syndrome
abasia
abderhalden-kaufmann-lignac
abdominalgia
abduction contracture
abetalipo proteinemia
abiotrophy
ablation
ablepharia
abocclusion
abolition
aborter
abortion
abortus
aboulomania
abrami's disease
```

Speichern Sie das Wörterbuch jetzt lokal, und fügen Sie ein paar mehr Ausdrücke hinzu. Sie können Ausdrücke direkt in PowerShell hinzufügen, müssen aber die Datei dennoch lokal exportieren, um sicherzustellen, dass sie mit Unicode-Codierung gespeichert wird und die BOM enthält.
  
Speichern Sie das Wörterbuch lokal, indem Sie Folgendes ausführen:
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

Öffnen Sie jetzt einfach die Datei, fügen Sie Ihre zusätzlichen Ausdrücke hinzu, und speichern Sie die Datei mit Unicode-Codierung (UTF-16). Nun laden Sie die aktualisierten Ausdrücke hoch und aktualisieren das vorhandene Wörterbuch.
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

Das vorhandene Wörterbuch wurde nun aktualisiert. Beachten Sie, dass das Feld `Identity` den Namen des Wörterbuchs erhält. Wenn Sie auch den Namen Ihres Wörterbuchs mit dem `set-`-Cmdlet ändern möchten, müssten Sie oben einfach den `-Name`-Parameter mit dem neuen Wörterbuchnamen hinzufügen. 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a>Verwenden von Schlüsselwörterbüchern in benutzerdefinierten vertraulichen Informationstypen und DLP-Richtlinien

Schlüsselwörterbücher können als Bestandteil der Übereinstimmungsanforderungen für einen benutzerdefinierten vertraulichen Informationstyp verwendet werden oder direkt als vertraulicher Informationstyp. Für beides muss [ein benutzerdefinierter vertraulicher Informationstyp erstellt werden](create-a-custom-sensitive-information-type.md). Folgen Sie den Anweisungen im verknüpften Artikel, um einen vertraulichen Informationstyp zu erstellen. Wenn Sie die XML haben, benötigen Sie die GUID-ID für das Wörterbuch, um dieses zu verwenden.
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

Um die Identität des Wörterbuchs zu erhalten, führen Sie den folgenden Befehl aus, und kopieren Sie den **Identity**-Eigenschaftswert: 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

Die Ausgabe des Befehls sieht wie folgt aus:
  
```
RunspaceId        : 138e55e7-ea1e-4f7a-b824-79f2c4252255
Identity          : 8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f
Name              : Diseases
Description       : Names of diseases and injuries from ICD-10-CM lexicon
KeywordDictionary : aarskog's syndrome, abandonment, abasia, abderhalden-kaufmann-lignac, abdominalgia, abduction contracture, abetalipo
                    proteinemia, abiotrophy, ablatio, ablation, ablepharia, abocclusion, abolition, aborter, abortion, abortus, aboulomania,
                    abrami's disease, abramo
IsValid           : True
ObjectState       : Unchanged
```

Fügen Sie die Identität in den XML-Code Ihres benutzerdefinierten vertraulichen Informationstyps ein, und laden Sie sie hoch. Das Wörterbuch wird jetzt in der Liste vertraulicher Informationstypen angezeigt, und Sie können es direkt in Ihrer Richtlinie verwenden. Geben Sie dabei an, wie viele Schlüsselwörter übereinstimmen müssen.
  
```
<Entity id="d333c6c2-5f4c-4131-9433-db3ef72a89e8" patternsProximity="300" recommendedConfidence="85">
      <Pattern confidenceLevel="85">
        <IdMatch idRef="8d2d44b0-91f4-41f2-94e0-21c1c5b5fc9f" />
      </Pattern>
    </Entity>
    <LocalizedStrings>
      <Resource idRef="d333c6c2-5f4c-4131-9433-db3ef72a89e8">
        <Name default="true" langcode="en-us">Diseases</Name>
        <Description default="true" langcode="en-us">Detects various diseases</Description>
      </Resource>
    </LocalizedStrings>
```


