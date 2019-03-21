---
title: Erstellen eines Schlüsselwörterbuchs
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Um vertrauliche Informationen identifizieren zu können, muss manchmal nach Schlüsselwörtern gesucht werden, insbesondere, wenn allgemeine Inhalte (z. B. Kommunikation im Bereich Gesundheitswesen) oder unangemessene bzw. obszöne Sprache identifiziert werden. Sie können zwar Schlüsselwortlisten in vertraulichen Informationstypen erstellen, diese sind aber im Hinblick auf ihre Größe eingeschränkt und erfordern zum Erstellen oder Ändern eine Bearbeitung der XML-Daten. Schlüsselwörterbücher bieten eine einfachere Verwaltung von Schlüsselwörtern und sind für viel größere Inhalte geeignet; es werden bis zu 100.000 Begriffe pro Wörterbuch unterstützt.
ms.openlocfilehash: 5561f8b11cf7bab8c726da332caca1484d455b35
ms.sourcegitcommit: 9a69ea604b415af4fef4964a19a09f3cead5a2ce
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30701310"
---
# <a name="create-a-keyword-dictionary"></a>Erstellen eines Schlüsselwörterbuchs

Durch die Verhinderung von Datenverlusten (Data Loss Prevention, DLP) in Office 365 können vertrauliche Informationen identifiziert, überwacht und geschützt werden. Um vertrauliche Informationen identifizieren zu können, muss manchmal nach Schlüsselwörtern gesucht werden, insbesondere, wenn allgemeine Inhalte (z. B. Kommunikation im Bereich Gesundheitswesen) oder unangemessene bzw. obszöne Sprache identifiziert werden. Sie können zwar Schlüsselwortlisten in vertraulichen Informationstypen erstellen, diese sind aber im Hinblick auf ihre Größe eingeschränkt und erfordern zum Erstellen oder Ändern eine Bearbeitung der XML-Daten. Schlüsselwörterbücher bieten eine einfachere Verwaltung von Schlüsselwörtern und sind für viel größere Inhalte geeignet; es werden bis zu 100.000 Begriffe pro Wörterbuch unterstützt.
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a>Grundlegende Schritte zum Erstellen eines Schlüsselwörterbuchs

Die Schlüsselwörter für Ihr Wörterbuch können aus einer Vielzahl von Quellen stammen, meistens aber aus einer in den Dienst importierten Datei (etwa einer CSV- oder TXT-Liste), oder durch ein einem PowerShell-Cmdlet, aus einer Liste, die Sie direkt in das PowerShell-Cmdlet eingeben, oder aus einem vorhandenen Wörterbuch.Beim Erstellen eines Schlüsselwörterbuchs befolgen Sie die gleichen einfachen Schritte:
  
1. Verwenden Sie das **Security & Compliance Center**, oder stellen Sie die Verbindung zu **Security &amp; Compliance Center PowerShell** her.
    
2. **Definieren oder Laden der Schlüsselwörter aus der gewünschten Quelle**: Der Assistent und das Cmdlet akzeptieren eine durch Trennzeichen getrennte Liste von Schlüsselwörtern zum Erstellen eines benutzerdefinierten Schlüsselwörterbuchs, dieser Schritt kann also in Abhängigkeit davon, woher Ihre Schlüsselwörter stammen, geringfügig anders sein. Nach dem Laden werden diese codiert und in ein Bytearray konvertiert, bevor sie importiert werden.
    
3. **Erstellen des Wörterbuchs**: Wählen Sie einen Namen und eine Beschreibung aus, und erstellen Sie das Wörterbuch.

## <a name="create-a-keyword-dictionary-using-the-security--compliance-center"></a>Erstellen eines Schlüsselwörterbuchs mit dem Security & Compliance Center

Verwenden Sie die folgenden Schritte zum Erstellen und Importieren von Schlüsselwörtern für ein Benutzerwörterbuch:

1. Stellen Sie die Verbindung zum [Security & Compliance Center](https://protection.office.com) her.
2. Navigieren Sie zu **Klassifizierungen > Typen vertraulicher Informationen**.
3. Wählen Sie **Erstellen** aus, geben Sie einen **Namen** und eine **Beschreibung** für Ihren vertraulichen Infotyp ein, und wählen Sie dann **Weiter** aus.
4. Wählen Sie **Element hinzufügen** und dann **Wörterbuch (große Schlüsselwörter)** in der Dropdownliste **Inhalt erkennen, der Folgendes enthält** aus.
5. Wählen Sie **Wörterbuch hinzufügen** aus.
6. Wählen Sie unter dem Steuerelement "Suche" die Option **Hier können Sie neue Schlüsselwörterbücher erstellen** aus.
7. Geben Sie einen **Namen** für Ihr Benutzerwörterbuch ein.
8. Klicken Sie auf **Importieren**, und wählen Sie dann entweder **Aus Text** oder **Aus CSV** aus, je nach Typ der Schlüsselwortdatei.
9. Wählen Sie im Dialogfeld "Datei" die Schlüsselwortdatei auf Ihrem lokalen PC oder aus der Netzwerkfreigabe aus, und klicken Sie dann auf **Öffnen**.
10. Klicken Sie auf **Speichern**, und wählen Sie dann Ihr Benutzerwörterbuch aus der Liste **Schlüsselwörterbücher** aus.
11. Wählen Sie **Hinzufügen** aus, und klicken Sie dann auf **Weiter**.
12. Überprüfen und vervollständigen Sie den ausgewählten Typ vertraulicher Informationen, und wählen Sie dann **Fertig stellen** aus.
    
## <a name="create-a-keyword-dictionary-from-a-file-using-powershell"></a>Erstellen eines Schlüsselwörterbuchs aus einer Datei mit PowerShell

Wenn Sie ein großes Wörterbuch erstellen müssen, werden dafür häufig Schlüsselwörter aus einer Datei oder aus einer Liste verwendet, die aus einer anderen Quelle exportiert wurde. In diesem Fall erstellen Sie ein Schlüsselwörterbuch mit einer Liste unangemessener Begriffe, nach denen in externen E-Mails gesucht werden soll. Zunächst müssen Sie [eine Verbindung zu Office 365 Security &amp; Compliance Center PowerShell herstellen](https://docs.microsoft.com/de-DE/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
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

Möglicherweise müssen Sie einmal Schlüsselwörter in einem Ihrer Schlüsselwörterbücher oder in einem der integrierten Wörterbücher ändern. Derzeit können Sie mit PowerShell nur ein benutzerdefiniertes Schlüsselwörterbuch aktualisieren. 

In diesem Beispiel ändern wir einige Ausdrücke in PowerShell, speichern die Ausdrücke lokal, wo Sie sie in einem Editor bearbeiten können, und aktualisieren anschließend die vorherigen Ausdrücke an Ort und Stelle. Rufen Sie zuerst das Wörterbuchobjekt ab:
  
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

Schlüsselwörterbücher können als Bestandteil der Übereinstimmungsanforderungen für einen benutzerdefinierten vertraulichen Informationstyp verwendet werden oder direkt als vertraulicher Informationstyp. Für beides muss [ein benutzerdefinierter vertraulicher Informationstyp in Office 365 Security & Compliance Center PowerShell erstellt werden](create-a-custom-sensitive-information-type-in-scc-powershell.md). Folgen Sie den Anweisungen im verknüpften Artikel, um einen vertraulichen Informationstyp zu erstellen. Wenn Sie die XML haben, benötigen Sie die GUID-ID für das Wörterbuch, um dieses zu verwenden.
  
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

Fügen Sie die Identität in den XML-Code Ihres benutzerdefinierten Typs vertraulicher Informationen ein, und laden Sie ihn hoch. Jetzt wird das Wörterbuch in Ihrer Liste der Typen vertraulicher Informationen angezeigt, und Sie können es direkt in Ihrer Richtlinie verwenden und festlegen, bei wie vielen Schlüsselwörtern eine Übereinstimmung festgestellt werden muss.
  
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


