---
title: Erstellen eines Schlüsselwörterbuchs
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Priority
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Um vertrauliche Informationen identifizieren zu können, muss manchmal nach Schlüsselwörtern gesucht werden, insbesondere, wenn allgemeine Inhalte (z. B. Kommunikation im Bereich Gesundheitswesen) oder unangemessene bzw. obszöne Sprache identifiziert werden. Sie können zwar Schlüsselwortlisten in vertraulichen Informationstypen erstellen, diese sind aber im Hinblick auf ihre Größe eingeschränkt und erfordern zum Erstellen oder Ändern eine Bearbeitung der XML-Daten. Schlüsselwörterbücher bieten eine einfachere Verwaltung von Schlüsselwörtern und sind für viel größere Inhalte geeignet; es werden bis zu 100.000 Begriffe pro Wörterbuch unterstützt.
ms.openlocfilehash: bd13b4d522b22773fe56f93e1975f1d4decfbfe5
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410730"
---
# <a name="create-a-keyword-dictionary"></a><span data-ttu-id="92686-105">Erstellen eines Schlüsselwörterbuchs</span><span class="sxs-lookup"><span data-stu-id="92686-105">Create a keyword dictionary</span></span>

<span data-ttu-id="92686-p102">Durch die Verhinderung von Datenverlusten (Data Loss Prevention, DLP) in Office 365 können vertrauliche Informationen identifiziert, überwacht und geschützt werden. Um vertrauliche Informationen identifizieren zu können, muss manchmal nach Schlüsselwörtern gesucht werden, insbesondere, wenn allgemeine Inhalte (z. B. Kommunikation im Bereich Gesundheitswesen) oder unangemessene bzw. obszöne Sprache identifiziert werden. Sie können zwar Schlüsselwortlisten in vertraulichen Informationstypen erstellen, diese sind aber im Hinblick auf ihre Größe eingeschränkt und erfordern zum Erstellen oder Ändern eine Bearbeitung der XML-Daten. Schlüsselwörterbücher bieten eine einfachere Verwaltung von Schlüsselwörtern und sind für viel größere Inhalte geeignet; es werden bis zu 100.000 Begriffe pro Wörterbuch unterstützt.</span><span class="sxs-lookup"><span data-stu-id="92686-p102">Data loss prevention (DLP) in Office 365 can identify, monitor, and protect your sensitive information. Identifying sensitive information sometimes requires looking for keywords, particularly when identifying generic content (such as healthcare-related communication) or inappropriate or explicit language. While you can create keyword lists in sensitive information types, keyword lists are limited in size and require modifying XML to create or edit them. Keyword dictionaries provide simpler management of keywords and at a much larger scale, supporting up to 100,000 terms per dictionary.</span></span>
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a><span data-ttu-id="92686-110">Grundlegende Schritte zum Erstellen eines Schlüsselwörterbuchs</span><span class="sxs-lookup"><span data-stu-id="92686-110">Basic steps to creating a keyword dictionary</span></span>

<span data-ttu-id="92686-p103">Die Schlüsselwörter für Ihr Wörterbuch können aus einer Vielzahl von Quellen stammen, meistens aber aus einer Datei (etwa einer CSV- oder TXT-Liste), aus einer Liste, die Sie direkt in das Cmdlet eingeben, oder aus einem vorhandenen Wörterbuch. Befolgen Sie beim Erstellen eines Schlüsselwörterbuchs die folgenden Kernschritte:</span><span class="sxs-lookup"><span data-stu-id="92686-p103">The keywords for your dictionary could come from a variety of sources, most commonly from a file (such as a .csv or .txt list), from a list you enter directly in the cmdlet, or from an existing dictionary. When you create a keyword dictionary, you follow the same core steps:</span></span>
  
1. <span data-ttu-id="92686-113">**Herstellen einer Verbindung mit Security &amp; Compliance Center PowerShell**: Weitere Informationen finden Sie in [diesem Thema](https://docs.microsoft.com/de-DE/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="92686-113">**Connect to Security &amp; Compliance Center PowerShell** - see [this topic](https://docs.microsoft.com/de-DE/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
    
2. <span data-ttu-id="92686-114">**Definieren oder Laden der Schlüsselwörter aus der gewünschten Quelle**: Das Cmdlet zum Erstellen eines Schlüsselwörterbuchs akzeptiert eine durch Trennzeichen getrennte Liste von Schlüsselwörtern, dieser Schritt kann also in Abhängigkeit davon, woher Ihre Schlüsselwörter stammen, geringfügig anders sein.</span><span class="sxs-lookup"><span data-stu-id="92686-114">**Define or load your keywords from your intended source** - the cmdlet to create a keyword dictionary accepts a comma-separated list of keywords, so this step will vary slightly depending on where your keywords come from.</span></span> 
    
3. <span data-ttu-id="92686-115">**Codieren der Schlüsselwörter**: Nach dem Laden werden diese in ein Bytearray konvertiert, bevor sie importiert werden.</span><span class="sxs-lookup"><span data-stu-id="92686-115">**Encode your keywords** - once loaded, they're converted to a byte array before they're imported.</span></span> 
    
4. <span data-ttu-id="92686-116">**Erstellen des Wörterbuchs**: Wählen Sie einen Namen und eine Beschreibung aus, und erstellen Sie das Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="92686-116">**Create your dictionary** - choose a name and description and create your dictionary.</span></span> 
    
## <a name="create-a-keyword-dictionary-from-a-file"></a><span data-ttu-id="92686-117">Erstellen eines Schlüsselwörterbuchs aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="92686-117">Create a keyword dictionary from a file</span></span>

<span data-ttu-id="92686-p104">Wenn Sie ein großes Wörterbuch erstellen müssen, werden dafür häufig Schlüsselwörter aus einer Datei oder aus einer Liste verwendet, die aus einer anderen Quelle exportiert wurde. In diesem Fall erstellen Sie ein Schlüsselwörterbuch mit einer Liste unangemessener Begriffe, nach denen in externen E-Mails gesucht werden soll. Zunächst müssen Sie [eine Verbindung zu Office 365 Security &amp; Compliance Center PowerShell herstellen](https://docs.microsoft.com/de-DE/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="92686-p104">Often when you need to create a large dictionary, it's to use keywords from a file or a list exported from some other source. In this case, you'll create a keyword dictionary containing a list of inappropriate language to screen in external email. You need to first [Connect to Office 365 Security &amp; Compliance Center PowerShell](https://docs.microsoft.com/de-DE/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
  
1. <span data-ttu-id="92686-121">Kopieren Sie die Schlüsselwörter in eine Textdatei, und stellen Sie sicher, dass sich jedes Schlüsselwort in einer separaten Zeile befindet.</span><span class="sxs-lookup"><span data-stu-id="92686-121">Copy the keywords into a text file and make sure that each keyword is on a separate line.</span></span>
    
2. <span data-ttu-id="92686-p105">Speichern Sie die Textdatei in Unicode-Codierung: Im Editor \> **Speichern als** \> **Codierung** \> **Unicode**.</span><span class="sxs-lookup"><span data-stu-id="92686-p105">Save the text file with Unicode encoding. In Notepad \> **Save As** \> **Encoding** \> **Unicode**.</span></span>
    
3. <span data-ttu-id="92686-124">Lesen Sie die Datei in eine Variable, indem Sie das folgende Cmdlet ausführen:</span><span class="sxs-lookup"><span data-stu-id="92686-124">Read the file into a variable by running this cmdlet:</span></span>
    
  ```
  $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
  ```

4. <span data-ttu-id="92686-125">Erstellen Sie das Wörterbuch, indem Sie das folgende Cmdlet ausführen:</span><span class="sxs-lookup"><span data-stu-id="92686-125">Create the dictionary by running this cmdlet:</span></span>
    
  ```
  New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
  ```

## <a name="modifying-an-existing-keyword-dictionary"></a><span data-ttu-id="92686-126">Ändern eines vorhandenen Schlüsselwörterbuchs</span><span class="sxs-lookup"><span data-stu-id="92686-126">Modifying an existing keyword dictionary</span></span>

<span data-ttu-id="92686-p106">Vielleicht müssen Sie Schlüsselwörter in einem Ihrer Schlüsselwörterbucher ändern oder eines der integrierten Wörterbücher ändern. In diesem Beispiel ändern wir einige Ausdrücke in PowerShell, speichern die Ausdrücke lokal, wo Sie sie in einem Editor bearbeiten können, und aktualisieren dann die vorhandenen, früheren Ausdrücke. Rufen Sie zunächst das Wörterbuchobjekt ab:</span><span class="sxs-lookup"><span data-stu-id="92686-p106">You might need to modify keywords in one of your keyword dictionaries, or modify one of the built-in dictionaries. In this example, we'll modify some terms in PowerShell, save the terms locally where you can modify them in an editor, and then update the previous terms in place. First, retrieve the dictionary object:</span></span>
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="92686-p107">Durch Drucken von `$dict` werden die verschiedenen Variablen angezeigt. Die eigentlichen Schlüsselwörter werden in einem Objekt am Back-End gespeichert, `$dict.KeywordDictionary` enthält aber eine Zeichenfolgendarstellung von diesen, die Sie zum Ändern des Wörterbuchs verwenden. Bevor Sie das Wörterbuch ändern, müssen Sie die Begriffe mit der `.split(',')`-Methode wieder in ein Array konvertieren. Danach entfernen Sie die ungewünschten Leerzeichen zwischen den Schlüsselwörtern mithilfe der `.trim()`-Methode, sodass nur die Schlüsselwörter übrig bleiben, mit denen Sie arbeiten möchten.</span><span class="sxs-lookup"><span data-stu-id="92686-p107">Printing  `$dict` will show the various variables. The keywords themselves are stored in an object on the backend, but  `$dict.KeywordDictionary` contains a string representation of them, which you'll use to modify the dictionary. Before you modify the dictionary, you need to turn the string of terms back into an array using the  `.split(',')` method. Then you'll clean up the unwanted spaces between the keywords with the  `.trim()` method, leaving just the keywords to work with.</span></span> 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

<span data-ttu-id="92686-p108">Jetzt entfernen Sie einige Ausdrücke aus dem Wörterbuch. Da das Beispielwörterbuch nur einige Schlüsselwörter enthält, können Sie diesen Schritt auch überspringen und mit dem Exportieren des Wörterbuchs und dem Bearbeiten im Editor fortfahren. Wörterbücher enthalten aber in der Regel eine große Textmenge, daher erfahren Sie zunächst, wie diese in PowerShell ganz einfach bearbeiten werden.</span><span class="sxs-lookup"><span data-stu-id="92686-p108">Now you'll remove some terms from the dictionary. Because the example dictionary has only a few keywords, you could just as easily skip to exporting the dictionary and editing it in Notepad, but dictionaries generally contain a large amount of text, so you'll first learn this way to edit them easily in PowerShell.</span></span>
  
<span data-ttu-id="92686-p109">Im letzten Schritt haben Sie die Schlüsselwörter in einem Array gespeichert. Es gibt mehrere Möglichkeiten, um [Elemente aus einem Array zu entfernen](https://go.microsoft.com/fwlink/p/?linkid=852620). Der Einfachheit halber erstellen Sie aber ein Array der Ausdrücke, die Sie aus dem Wörterbuch entfernen möchten, und kopieren dann nur die Wörterbuchbegriffe dort hinein, die sich nicht in der Liste der zu entfernenden Ausdrücke befinden.</span><span class="sxs-lookup"><span data-stu-id="92686-p109">In the last step, you saved the keywords to an array. There are several ways to [remove items from an array](https://go.microsoft.com/fwlink/p/?linkid=852620), but as a straightforward approach, you'll create an array of the terms you want to remove from the dictionary, and then copy only the dictionary terms to it that aren't in the list of terms to remove.</span></span>
  
<span data-ttu-id="92686-p110">Führen Sie den Befehl  `$terms` aus, um die aktuelle Liste von Ausdrücken anzuzeigen. Die Ausgabe des Befehls sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="92686-p110">Run the command  `$terms` to show the current list of terms. The output of the command looks like this:</span></span> 
  
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

<span data-ttu-id="92686-140">Führen Sie diesen Befehl aus, um die Ausdrücke anzugeben, die Sie entfernen möchten:</span><span class="sxs-lookup"><span data-stu-id="92686-140">Run this command to specify the terms that you want to remove:</span></span>
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

<span data-ttu-id="92686-141">Führen Sie diesen Befehl, um die Ausdrücke tatsächlich aus der Liste zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="92686-141">Run this command to actually remove the terms from the list:</span></span>
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

<span data-ttu-id="92686-p111">Führen Sie den Befehl  `$updatedTerms` aus, um die aktualisierte Liste von Ausdrücken anzuzeigen. Die Ausgabe des Befehls sieht wie folgt aus (die angegebenen Ausdrücke wurden entfernt):</span><span class="sxs-lookup"><span data-stu-id="92686-p111">Run the command  `$updatedTerms` to show the updated list of terms. The output of the command looks like this (the specified terms have been removed):</span></span> 
  
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

<span data-ttu-id="92686-p112">Speichern Sie das Wörterbuch jetzt lokal, und fügen Sie ein paar mehr Ausdrücke hinzu. Sie können Ausdrücke direkt in PowerShell hinzufügen, müssen aber die Datei dennoch lokal exportieren, um sicherzustellen, dass sie mit Unicode-Codierung gespeichert wird und die BOM enthält.</span><span class="sxs-lookup"><span data-stu-id="92686-p112">Now save the dictionary locally and add a few more terms. You could add the terms right here in PowerShell, but you'll still need to export the file locally to ensure it's saved with Unicode encoding and contains the BOM.</span></span>
  
<span data-ttu-id="92686-146">Speichern Sie das Wörterbuch lokal, indem Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="92686-146">Save the dictionary locally by running the following:</span></span>
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

<span data-ttu-id="92686-p113">Öffnen Sie jetzt einfach die Datei, fügen Sie Ihre zusätzlichen Ausdrücke hinzu, und speichern Sie die Datei mit Unicode-Codierung (UTF-16). Nun laden Sie die aktualisierten Ausdrücke hoch und aktualisieren das vorhandene Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="92686-p113">Now simply open the file, add your additional terms, and save with Unicode encoding (UTF-16). Now you'll upload the updated terms and update the dictionary in place.</span></span>
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

<span data-ttu-id="92686-p114">Das vorhandene Wörterbuch wurde nun aktualisiert. Beachten Sie, dass das Feld `Identity` den Namen des Wörterbuchs erhält. Wenn Sie auch den Namen Ihres Wörterbuchs mit dem `set-`-Cmdlet ändern möchten, müssten Sie oben einfach den `-Name`-Parameter mit dem neuen Wörterbuchnamen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="92686-p114">Now the dictionary has been updated in place. Note that the  `Identity` field takes the name of the dictionary. If you wanted to also change the name of your dictionary using the  `set-` cmdlet, you would just need to add the  `-Name` parameter to what's above with your new dictionary name.</span></span> 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a><span data-ttu-id="92686-152">Verwenden von Schlüsselwörterbüchern in benutzerdefinierten vertraulichen Informationstypen und DLP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="92686-152">Using keyword dictionaries in custom sensitive information types and DLP policies</span></span>

<span data-ttu-id="92686-p115">Schlüsselwörterbücher können als Bestandteil der Übereinstimmungsanforderungen für einen benutzerdefinierten vertraulichen Informationstyp verwendet werden oder direkt als vertraulicher Informationstyp. Für beides muss [ein benutzerdefinierter vertraulicher Informationstyp in Office 365 Security & Compliance Center PowerShell erstellt werden](create-a-custom-sensitive-information-type-in-scc-powershell.md). Folgen Sie den Anweisungen im verknüpften Artikel, um einen vertraulichen Informationstyp zu erstellen. Wenn Sie die XML haben, benötigen Sie die GUID-ID für das Wörterbuch, um dieses zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="92686-p115">Keyword dictionaries can be used as part of the match requirements for a custom sensitive information type, or as a sensitive information type themselves. Both require [Create a custom sensitive information type in Office 365 Security & Compliance Center PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md). Follow the instructions in the linked article to create a sensitive information type. Once you have the XML, you'll need the GUID identifier for the dictionary to use it.</span></span>
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

<span data-ttu-id="92686-157">Um die Identität des Wörterbuchs zu erhalten, führen Sie den folgenden Befehl aus, und kopieren Sie den **Identity**-Eigenschaftswert:</span><span class="sxs-lookup"><span data-stu-id="92686-157">To get the identity of your dictionary, run this command and copy the **Identity** property value:</span></span> 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="92686-158">Die Ausgabe des Befehls sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="92686-158">The output of the command looks like this:</span></span>
  
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

<span data-ttu-id="92686-p116">Fügen Sie die Identität in den XML-Code Ihres benutzerdefinierten vertraulichen Informationstyps ein, und laden Sie sie hoch. Das Wörterbuch wird jetzt in der Liste vertraulicher Informationstypen angezeigt, und Sie können es direkt in Ihrer Richtlinie verwenden. Geben Sie dabei an, wie viele Schlüsselwörter übereinstimmen müssen.</span><span class="sxs-lookup"><span data-stu-id="92686-p116">Paste the identity into your custom sensitive information type's XML and upload it. Now your dictionary will appear in your list of sensitive information types and you can use it right in your policy, specifying how many keywords are required to match.</span></span>
  
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


