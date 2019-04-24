---
title: Erstellen eines Schlüsselwörterbuchs
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 04/11/2019
localization_priority: Normal
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Um vertrauliche Informationen identifizieren zu können, muss manchmal nach Schlüsselwörtern gesucht werden, insbesondere, wenn allgemeine Inhalte (z. B. Kommunikation im Bereich Gesundheitswesen) oder unangemessene bzw. obszöne Sprache identifiziert werden. Sie können zwar Schlüsselwortlisten in vertraulichen Informationstypen erstellen, diese sind aber im Hinblick auf ihre Größe eingeschränkt und erfordern zum Erstellen oder Ändern eine Bearbeitung der XML-Daten. Schlüsselwörterbücher bieten eine einfachere Verwaltung von Schlüsselwörtern und sind für viel größere Inhalte geeignet; es werden bis zu 100.000 Begriffe pro Wörterbuch unterstützt.
ms.openlocfilehash: 142f471d80c7278cabd4c437f0ae0ee9af3ff219
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258163"
---
# <a name="create-a-keyword-dictionary"></a>Erstellen eines Schlüsselwörterbuchs

Data Loss Prevention (DLP) in Office 365 kann Ihre vertraulichen Informationen identifizieren, überwachen und schützen. Für die Identifizierung vertraulicher Informationen ist es manchmal erforderlich, nach Stichwörtern zu suchen, insbesondere bei der Identifizierung generischer Inhalte (beispielsweise Kommunikation im Zusammenhang mit dem Gesundheitswesen) oder anstößigen oder expliziten Sprachen Obwohl Sie Stichwortlisten in vertraulichen Informationstypen erstellen können, sind Keyword-Listen in der Größe begrenzt und erfordern das Ändern von XML, um Sie zu erstellen oder zu bearbeiten. Stichwort Wörterbücher bieten eine einfachere Verwaltung von Schlüsselwörtern und in einem wesentlich größeren Umfang und unterstützen bis zu 100.000 Ausdrücke pro Wörterbuch.
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a>Grundlegende Schritte zum Erstellen eines Schlüsselwörterbuchs

Die Schlüsselwörter für Ihr Wörterbuch können aus einer Vielzahl von Quellen stammen, meistens aber aus einer in den Dienst importierten Datei (etwa einer CSV- oder TXT-Liste), oder durch ein einem PowerShell-Cmdlet, aus einer Liste, die Sie direkt in das PowerShell-Cmdlet eingeben, oder aus einem vorhandenen Wörterbuch.Beim Erstellen eines Schlüsselwörterbuchs befolgen Sie die gleichen einfachen Schritte:
  
1. verwenden sie das **security & compliance center** ([https://protection.office.com](https://protection.office.com)), oder stellen sie eine verbindung mit **Office 365 security &amp; compliance center PowerShell**her.
    
2. **Definieren oder laden Sie Ihre Schlüsselwörter aus der beabsichtigten Quelle**. Sowohl der Assistent als auch das Cmdlet akzeptieren eine durch trennzeichengetrennte Liste von Schlüsselwörtern, um ein benutzerdefiniertes Stichwort Wörterbuch zu erstellen, sodass dieser Schritt je nachdem, woher Ihre Schlüsselwörter stammen, etwas variieren kann. Nach dem Laden werden diese codiert und in ein Bytearray konvertiert, bevor sie importiert werden.
    
3. **Erstellen Sie Ihr Wörterbuch**. Wählen Sie einen Namen und eine Beschreibung aus, und erstellen Sie Ihr Wörterbuch.

## <a name="create-a-keyword-dictionary-using-the-security--compliance-center"></a>Erstellen eines Stichwort Wörterbuchs mithilfe des Security & Compliance Center

Verwenden Sie die folgenden Schritte zum Erstellen und Importieren von Schlüsselwörtern für ein Benutzerwörterbuch:

1. Stellen Sie eine Verbindung mit dem Security &[https://protection.office.com](https://protection.office.com)Compliance Center her ().

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

Häufig müssen Sie ein umfangreiches Wörterbuch erstellen, indem Sie Stichwörter aus einer Datei oder aus einer Liste verwenden, die aus einer anderen Quelle exportiert wurde. In diesem Fall erstellen Sie ein Stichwort Wörterbuch, das eine Liste der anstößigen Sprache enthält, die in externen e-Mails angezeigt werden soll. Sie müssen zuerst [eine Verbindung mit Office 365 &amp; Security Compliance Center PowerShell herstellen](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).
  
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

Beispielsweise ändern wir einige Ausdrücke in PowerShell, speichern die Ausdrücke lokal, wo Sie Sie in einem Editor ändern können, und aktualisieren dann die vorherigen Ausdrücke direkt. 

Rufen Sie zuerst das Wörterbuchobjekt ab:
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

Beim `$dict` Drucken werden die verschiedenen Variablen angezeigt. Die Schlüsselwörter selbst werden in einem Objekt im Back-End gespeichert `$dict.KeywordDictionary` , Sie enthalten jedoch eine Zeichenfolgendarstellung, die Sie zum Ändern des Wörterbuchs verwenden. 

Bevor Sie das Wörterbuch ändern, müssen Sie die Zeichenfolge mithilfe der `.split(',')` -Methode wieder in ein Array umwandeln. Dann bereinigen Sie die unerwünschten Leerzeichen zwischen den Schlüsselwörtern `.trim()` mit der Methode, sodass nur die Schlüsselwörter für die Arbeit verwendet werden. 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

Jetzt entfernen Sie einige Ausdrücke aus dem Wörterbuch. Da das Beispielwörterbuch nur einige Schlüsselwörter enthält, können Sie diesen Schritt auch überspringen und mit dem Exportieren des Wörterbuchs und dem Bearbeiten im Editor fortfahren. Wörterbücher enthalten aber in der Regel eine große Textmenge, daher erfahren Sie zunächst, wie diese in PowerShell ganz einfach bearbeiten werden.
  
Im letzten Schritt haben Sie die Schlüsselwörter in einem Array gespeichert. Es gibt mehrere Möglichkeiten, um [Elemente aus einem Array zu entfernen](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)). Der Einfachheit halber erstellen Sie aber ein Array der Ausdrücke, die Sie aus dem Wörterbuch entfernen möchten, und kopieren dann nur die Wörterbuchbegriffe dort hinein, die sich nicht in der Liste der zu entfernenden Ausdrücke befinden.
  
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

Stichwort Wörterbücher können als Teil der Übereinstimmungs Anforderungen für einen benutzerdefinierten vertraulichen Informationstyp oder als vertraulicher Informationstyp verwendet werden. Beide müssen Sie einen [benutzerdefinierten vertraulichen Informationstyp](create-a-custom-sensitive-information-type-in-scc-powershell.md)erstellen. BeFolgen Sie die Anweisungen im verknüpften Artikel, um einen vertraulichen Informationstyp zu erstellen. Sobald Sie die XML-Datei haben, benötigen Sie die GUID-ID für das Wörterbuch, um Sie zu verwenden.
  
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


