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
# <a name="create-a-keyword-dictionary"></a><span data-ttu-id="ac5e4-105">Erstellen eines Schlüsselwörterbuchs</span><span class="sxs-lookup"><span data-stu-id="ac5e4-105">Create a keyword dictionary</span></span>

<span data-ttu-id="ac5e4-106">Data Loss Prevention (DLP) in Office 365 kann Ihre vertraulichen Informationen identifizieren, überwachen und schützen.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-106">Data loss prevention (DLP) in Office 365 can identify, monitor, and protect your sensitive information.</span></span> <span data-ttu-id="ac5e4-107">Für die Identifizierung vertraulicher Informationen ist es manchmal erforderlich, nach Stichwörtern zu suchen, insbesondere bei der Identifizierung generischer Inhalte (beispielsweise Kommunikation im Zusammenhang mit dem Gesundheitswesen) oder anstößigen oder expliziten Sprachen</span><span class="sxs-lookup"><span data-stu-id="ac5e4-107">Identifying sensitive information sometimes requires looking for keywords, particularly when identifying generic content (such as healthcare-related communication), or inappropriate or explicit language.</span></span> <span data-ttu-id="ac5e4-108">Obwohl Sie Stichwortlisten in vertraulichen Informationstypen erstellen können, sind Keyword-Listen in der Größe begrenzt und erfordern das Ändern von XML, um Sie zu erstellen oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-108">Although you can create keyword lists in sensitive information types, keyword lists are limited in size and require modifying XML to create or edit them.</span></span> <span data-ttu-id="ac5e4-109">Stichwort Wörterbücher bieten eine einfachere Verwaltung von Schlüsselwörtern und in einem wesentlich größeren Umfang und unterstützen bis zu 100.000 Ausdrücke pro Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-109">Keyword dictionaries provide simpler management of keywords and at a much larger scale, supporting up to 100,000 terms per dictionary.</span></span>
  
## <a name="basic-steps-to-creating-a-keyword-dictionary"></a><span data-ttu-id="ac5e4-110">Grundlegende Schritte zum Erstellen eines Schlüsselwörterbuchs</span><span class="sxs-lookup"><span data-stu-id="ac5e4-110">Basic steps to creating a keyword dictionary</span></span>

<span data-ttu-id="ac5e4-p103">Die Schlüsselwörter für Ihr Wörterbuch können aus einer Vielzahl von Quellen stammen, meistens aber aus einer in den Dienst importierten Datei (etwa einer CSV- oder TXT-Liste), oder durch ein einem PowerShell-Cmdlet, aus einer Liste, die Sie direkt in das PowerShell-Cmdlet eingeben, oder aus einem vorhandenen Wörterbuch.Beim Erstellen eines Schlüsselwörterbuchs befolgen Sie die gleichen einfachen Schritte:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p103">The keywords for your dictionary could come from a variety of sources, most commonly from a file (such as a .csv or .txt list) imported in the service or by PowerShell cmdlet, from a list you enter directly in the PowerShell cmdlet, or from an existing dictionary. When you create a keyword dictionary, you follow the same core steps:</span></span>
  
1. <span data-ttu-id="ac5e4-113">verwenden sie das **security & compliance center** ([https://protection.office.com](https://protection.office.com)), oder stellen sie eine verbindung mit **Office 365 security &amp; compliance center PowerShell**her.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-113">Use the **Security & Compliance Center** ([https://protection.office.com](https://protection.office.com)) or connect to  **Office 365 Security &amp; Compliance Center PowerShell**.</span></span>
    
2. <span data-ttu-id="ac5e4-114">**Definieren oder laden Sie Ihre Schlüsselwörter aus der beabsichtigten Quelle**.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-114">**Define or load your keywords from your intended source**.</span></span> <span data-ttu-id="ac5e4-115">Sowohl der Assistent als auch das Cmdlet akzeptieren eine durch trennzeichengetrennte Liste von Schlüsselwörtern, um ein benutzerdefiniertes Stichwort Wörterbuch zu erstellen, sodass dieser Schritt je nachdem, woher Ihre Schlüsselwörter stammen, etwas variieren kann.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-115">The wizard and the cmdlet both accept a comma-separated list of keywords to create a custom keyword dictionary, so this step will vary slightly depending on where your keywords come from.</span></span> <span data-ttu-id="ac5e4-116">Nach dem Laden werden diese codiert und in ein Bytearray konvertiert, bevor sie importiert werden.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-116">Once loaded, they're encoded and converted to a byte array before they're imported.</span></span>
    
3. <span data-ttu-id="ac5e4-117">**Erstellen Sie Ihr Wörterbuch**.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-117">**Create your dictionary**.</span></span> <span data-ttu-id="ac5e4-118">Wählen Sie einen Namen und eine Beschreibung aus, und erstellen Sie Ihr Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-118">Choose a name and description and create your dictionary.</span></span>

## <a name="create-a-keyword-dictionary-using-the-security--compliance-center"></a><span data-ttu-id="ac5e4-119">Erstellen eines Stichwort Wörterbuchs mithilfe des Security & Compliance Center</span><span class="sxs-lookup"><span data-stu-id="ac5e4-119">Create a keyword dictionary using the Security & Compliance Center</span></span>

<span data-ttu-id="ac5e4-120">Verwenden Sie die folgenden Schritte zum Erstellen und Importieren von Schlüsselwörtern für ein Benutzerwörterbuch:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-120">Use the following steps to create and import keywords for a custom dictionary:</span></span>

1. <span data-ttu-id="ac5e4-121">Stellen Sie eine Verbindung mit dem Security &[https://protection.office.com](https://protection.office.com)Compliance Center her ().</span><span class="sxs-lookup"><span data-stu-id="ac5e4-121">Connect to the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)).</span></span>

2. <span data-ttu-id="ac5e4-122">Navigieren Sie zu **Klassifizierungen > Typen vertraulicher Informationen**.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-122">Navigate to **Classifications > Sensitive info types**.</span></span>

3. <span data-ttu-id="ac5e4-123">Wählen Sie **Erstellen** aus, geben Sie einen **Namen** und eine **Beschreibung** für Ihren vertraulichen Infotyp ein, und wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-123">Select **Create** and enter a **Name** and **Description** for your sensitive info type, then select **Next**</span></span>

4. <span data-ttu-id="ac5e4-124">Wählen Sie **Element hinzufügen** und dann **Wörterbuch (große Schlüsselwörter)** in der Dropdownliste **Inhalt erkennen, der Folgendes enthält** aus.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-124">Select **Add an element**, then select **Dictionary (Large keywords)** in the **Detect content containing** drop-down list.</span></span>

5. <span data-ttu-id="ac5e4-125">Wählen Sie **Wörterbuch hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-125">Select **Add a dictionary**</span></span>

6. <span data-ttu-id="ac5e4-126">Wählen Sie unter dem Steuerelement "Suche" die Option **Hier können Sie neue Schlüsselwörterbücher erstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-126">Under the Search control, select **You can create new keyword dictionaries here**.</span></span>

7. <span data-ttu-id="ac5e4-127">Geben Sie einen **Namen** für Ihr Benutzerwörterbuch ein.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-127">Enter a **Name** for your custom dictionary.</span></span>

8. <span data-ttu-id="ac5e4-128">Klicken Sie auf **Importieren**, und wählen Sie dann entweder **Aus Text** oder **Aus CSV** aus, je nach Typ der Schlüsselwortdatei.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-128">Select **Import**, and select either **From text** or **From csv** depending on your keyword file type.</span></span>

9. <span data-ttu-id="ac5e4-129">Wählen Sie im Dialogfeld "Datei" die Schlüsselwortdatei auf Ihrem lokalen PC oder aus der Netzwerkfreigabe aus, und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-129">In the file dialog, select the keyword file from your local PC or network file share, then select **Open**.</span></span>

10. <span data-ttu-id="ac5e4-130">Klicken Sie auf **Speichern**, und wählen Sie dann Ihr Benutzerwörterbuch aus der Liste **Schlüsselwörterbücher** aus.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-130">Select **Save**, then select your custom dictionary from the **Keyword dictionaries** list.</span></span>

11. <span data-ttu-id="ac5e4-131">Wählen Sie **Hinzufügen** aus, und klicken Sie dann auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-131">Select **Add**, then select **Next**.</span></span>

12. <span data-ttu-id="ac5e4-132">Überprüfen und vervollständigen Sie den ausgewählten Typ vertraulicher Informationen, und wählen Sie dann **Fertig stellen** aus.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-132">Review and finalize your sensitive info type selections, then select **Finish**.</span></span>
    
## <a name="create-a-keyword-dictionary-from-a-file-using-powershell"></a><span data-ttu-id="ac5e4-133">Erstellen eines Schlüsselwörterbuchs aus einer Datei mit PowerShell</span><span class="sxs-lookup"><span data-stu-id="ac5e4-133">Create a keyword dictionary from a file using PowerShell</span></span>

<span data-ttu-id="ac5e4-134">Häufig müssen Sie ein umfangreiches Wörterbuch erstellen, indem Sie Stichwörter aus einer Datei oder aus einer Liste verwenden, die aus einer anderen Quelle exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-134">Often when you need to create a large dictionary, it's to use keywords from a file or a list exported from some other source.</span></span> <span data-ttu-id="ac5e4-135">In diesem Fall erstellen Sie ein Stichwort Wörterbuch, das eine Liste der anstößigen Sprache enthält, die in externen e-Mails angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-135">In this case, you'll create a keyword dictionary containing a list of inappropriate language to screen in external email.</span></span> <span data-ttu-id="ac5e4-136">Sie müssen zuerst [eine Verbindung mit Office 365 &amp; Security Compliance Center PowerShell herstellen](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span><span class="sxs-lookup"><span data-stu-id="ac5e4-136">You must first [connect to Office 365 Security &amp; Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell).</span></span>
  
1. <span data-ttu-id="ac5e4-137">Kopieren Sie die Schlüsselwörter in eine Textdatei, und stellen Sie sicher, dass sich jedes Schlüsselwort in einer separaten Zeile befindet.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-137">Copy the keywords into a text file and make sure that each keyword is on a separate line.</span></span>
    
2. <span data-ttu-id="ac5e4-p107">Speichern Sie die Textdatei in Unicode-Codierung: Im Editor \> **Speichern als** \> **Codierung** \> **Unicode**.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p107">Save the text file with Unicode encoding. In Notepad \> **Save As** \> **Encoding** \> **Unicode**.</span></span>
    
3. <span data-ttu-id="ac5e4-140">Lesen Sie die Datei in eine Variable, indem Sie das folgende Cmdlet ausführen:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-140">Read the file into a variable by running this cmdlet:</span></span>
    
    ```
    $fileData = Get-Content <filename> -Encoding Byte -ReadCount 0
    ```

4. <span data-ttu-id="ac5e4-141">Erstellen Sie das Wörterbuch, indem Sie das folgende Cmdlet ausführen:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-141">Create the dictionary by running this cmdlet:</span></span>
    
    ```
    New-DlpKeywordDictionary -Name <name> -Description <description> -FileData $fileData
    ```

## <a name="modifying-an-existing-keyword-dictionary"></a><span data-ttu-id="ac5e4-142">Ändern eines vorhandenen Schlüsselwörterbuchs</span><span class="sxs-lookup"><span data-stu-id="ac5e4-142">Modifying an existing keyword dictionary</span></span>

<span data-ttu-id="ac5e4-143">Möglicherweise müssen Sie einmal Schlüsselwörter in einem Ihrer Schlüsselwörterbücher oder in einem der integrierten Wörterbücher ändern.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-143">You might need to modify keywords in one of your keyword dictionaries, or modify one of the built-in dictionaries.</span></span> <span data-ttu-id="ac5e4-144">Derzeit können Sie mit PowerShell nur ein benutzerdefiniertes Schlüsselwörterbuch aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-144">Currently, your can only update a custom keyword dictionary using PowerShell.</span></span> 

<span data-ttu-id="ac5e4-145">Beispielsweise ändern wir einige Ausdrücke in PowerShell, speichern die Ausdrücke lokal, wo Sie Sie in einem Editor ändern können, und aktualisieren dann die vorherigen Ausdrücke direkt.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-145">For example, we'll modify some terms in PowerShell, save the terms locally where you can modify them in an editor, and then update the previous terms in place.</span></span> 

<span data-ttu-id="ac5e4-146">Rufen Sie zuerst das Wörterbuchobjekt ab:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-146">First, retrieve the dictionary object:</span></span>
  
```
$dict = Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="ac5e4-147">Beim `$dict` Drucken werden die verschiedenen Variablen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-147">Printing  `$dict` will show the various variables.</span></span> <span data-ttu-id="ac5e4-148">Die Schlüsselwörter selbst werden in einem Objekt im Back-End gespeichert `$dict.KeywordDictionary` , Sie enthalten jedoch eine Zeichenfolgendarstellung, die Sie zum Ändern des Wörterbuchs verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-148">The keywords themselves are stored in an object on the backend, but  `$dict.KeywordDictionary` contains a string representation of them, which you'll use to modify the dictionary.</span></span> 

<span data-ttu-id="ac5e4-149">Bevor Sie das Wörterbuch ändern, müssen Sie die Zeichenfolge mithilfe der `.split(',')` -Methode wieder in ein Array umwandeln.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-149">Before you modify the dictionary, you need to turn the string of terms back into an array using the  `.split(',')` method.</span></span> <span data-ttu-id="ac5e4-150">Dann bereinigen Sie die unerwünschten Leerzeichen zwischen den Schlüsselwörtern `.trim()` mit der Methode, sodass nur die Schlüsselwörter für die Arbeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-150">Then you'll clean up the unwanted spaces between the keywords with the  `.trim()` method, leaving just the keywords to work with.</span></span> 
  
```
$terms = $dict.KeywordDictionary.split(',').trim()
```

<span data-ttu-id="ac5e4-p111">Jetzt entfernen Sie einige Ausdrücke aus dem Wörterbuch. Da das Beispielwörterbuch nur einige Schlüsselwörter enthält, können Sie diesen Schritt auch überspringen und mit dem Exportieren des Wörterbuchs und dem Bearbeiten im Editor fortfahren. Wörterbücher enthalten aber in der Regel eine große Textmenge, daher erfahren Sie zunächst, wie diese in PowerShell ganz einfach bearbeiten werden.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p111">Now you'll remove some terms from the dictionary. Because the example dictionary has only a few keywords, you could just as easily skip to exporting the dictionary and editing it in Notepad, but dictionaries generally contain a large amount of text, so you'll first learn this way to edit them easily in PowerShell.</span></span>
  
<span data-ttu-id="ac5e4-p112">Im letzten Schritt haben Sie die Schlüsselwörter in einem Array gespeichert. Es gibt mehrere Möglichkeiten, um [Elemente aus einem Array zu entfernen](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)). Der Einfachheit halber erstellen Sie aber ein Array der Ausdrücke, die Sie aus dem Wörterbuch entfernen möchten, und kopieren dann nur die Wörterbuchbegriffe dort hinein, die sich nicht in der Liste der zu entfernenden Ausdrücke befinden.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p112">In the last step, you saved the keywords to an array. There are several ways to [remove items from an array](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-powershell-1.0/ee692802(v=technet.10)), but as a straightforward approach, you'll create an array of the terms you want to remove from the dictionary, and then copy only the dictionary terms to it that aren't in the list of terms to remove.</span></span>
  
<span data-ttu-id="ac5e4-p113">Führen Sie den Befehl  `$terms` aus, um die aktuelle Liste von Ausdrücken anzuzeigen. Die Ausgabe des Befehls sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p113">Run the command  `$terms` to show the current list of terms. The output of the command looks like this:</span></span> 
  
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

<span data-ttu-id="ac5e4-157">Führen Sie diesen Befehl aus, um die Ausdrücke anzugeben, die Sie entfernen möchten:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-157">Run this command to specify the terms that you want to remove:</span></span>
  
```
$termsToRemove = @('abandonment', 'ablatio')
```

<span data-ttu-id="ac5e4-158">Führen Sie diesen Befehl, um die Ausdrücke tatsächlich aus der Liste zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-158">Run this command to actually remove the terms from the list:</span></span>
  
```
$updatedTerms = $terms | Where-Object{ $_ -notin $termsToRemove }
```

<span data-ttu-id="ac5e4-p114">Führen Sie den Befehl  `$updatedTerms` aus, um die aktualisierte Liste von Ausdrücken anzuzeigen. Die Ausgabe des Befehls sieht wie folgt aus (die angegebenen Ausdrücke wurden entfernt):</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p114">Run the command  `$updatedTerms` to show the updated list of terms. The output of the command looks like this (the specified terms have been removed):</span></span> 
  
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

<span data-ttu-id="ac5e4-p115">Speichern Sie das Wörterbuch jetzt lokal, und fügen Sie ein paar mehr Ausdrücke hinzu. Sie können Ausdrücke direkt in PowerShell hinzufügen, müssen aber die Datei dennoch lokal exportieren, um sicherzustellen, dass sie mit Unicode-Codierung gespeichert wird und die BOM enthält.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p115">Now save the dictionary locally and add a few more terms. You could add the terms right here in PowerShell, but you'll still need to export the file locally to ensure it's saved with Unicode encoding and contains the BOM.</span></span>
  
<span data-ttu-id="ac5e4-163">Speichern Sie das Wörterbuch lokal, indem Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-163">Save the dictionary locally by running the following:</span></span>
  
```
Set-Content $updatedTerms -Path "C:\myPath\terms.txt"
```

<span data-ttu-id="ac5e4-p116">Öffnen Sie jetzt einfach die Datei, fügen Sie Ihre zusätzlichen Ausdrücke hinzu, und speichern Sie die Datei mit Unicode-Codierung (UTF-16). Nun laden Sie die aktualisierten Ausdrücke hoch und aktualisieren das vorhandene Wörterbuch.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p116">Now simply open the file, add your additional terms, and save with Unicode encoding (UTF-16). Now you'll upload the updated terms and update the dictionary in place.</span></span>
  
```
PS> Set-DlpKeywordDictionary -Identity "Diseases" -FileData (Get-Content -Path "C:myPath\terms.txt" -Encoding Byte -ReadCount 0)
```

<span data-ttu-id="ac5e4-p117">Das vorhandene Wörterbuch wurde nun aktualisiert. Beachten Sie, dass das Feld `Identity` den Namen des Wörterbuchs erhält. Wenn Sie auch den Namen Ihres Wörterbuchs mit dem `set-`-Cmdlet ändern möchten, müssten Sie oben einfach den `-Name`-Parameter mit dem neuen Wörterbuchnamen hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p117">Now the dictionary has been updated in place. Note that the  `Identity` field takes the name of the dictionary. If you wanted to also change the name of your dictionary using the  `set-` cmdlet, you would just need to add the  `-Name` parameter to what's above with your new dictionary name.</span></span> 
  
## <a name="using-keyword-dictionaries-in-custom-sensitive-information-types-and-dlp-policies"></a><span data-ttu-id="ac5e4-169">Verwenden von Schlüsselwörterbüchern in benutzerdefinierten vertraulichen Informationstypen und DLP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="ac5e4-169">Using keyword dictionaries in custom sensitive information types and DLP policies</span></span>

<span data-ttu-id="ac5e4-170">Stichwort Wörterbücher können als Teil der Übereinstimmungs Anforderungen für einen benutzerdefinierten vertraulichen Informationstyp oder als vertraulicher Informationstyp verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-170">Keyword dictionaries can be used as part of the match requirements for a custom sensitive information type, or as a sensitive information type themselves.</span></span> <span data-ttu-id="ac5e4-171">Beide müssen Sie einen [benutzerdefinierten vertraulichen Informationstyp](create-a-custom-sensitive-information-type-in-scc-powershell.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-171">Both require you to create a [custom sensitive information type](create-a-custom-sensitive-information-type-in-scc-powershell.md).</span></span> <span data-ttu-id="ac5e4-172">BeFolgen Sie die Anweisungen im verknüpften Artikel, um einen vertraulichen Informationstyp zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-172">Follow the instructions in the linked article to create a sensitive information type.</span></span> <span data-ttu-id="ac5e4-173">Sobald Sie die XML-Datei haben, benötigen Sie die GUID-ID für das Wörterbuch, um Sie zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-173">Once you have the XML, you'll need the GUID identifier for the dictionary to use it.</span></span>
  
```
<Entity id="9e5382d0-1b6a-42fd-820e-44e0d3b15b6e" patternsProximity="300" recommendedConfidence="75">
    <Pattern confidenceLevel="75">
        <IdMatch idRef=". . ."/>
    </Pattern>
</Entity>
```

<span data-ttu-id="ac5e4-174">Um die Identität des Wörterbuchs zu erhalten, führen Sie den folgenden Befehl aus, und kopieren Sie den **Identity**-Eigenschaftswert:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-174">To get the identity of your dictionary, run this command and copy the **Identity** property value:</span></span> 
  
```
Get-DlpKeywordDictionary -Name "Diseases"
```

<span data-ttu-id="ac5e4-175">Die Ausgabe des Befehls sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="ac5e4-175">The output of the command looks like this:</span></span>
  
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

<span data-ttu-id="ac5e4-p119">Fügen Sie die Identität in den XML-Code Ihres benutzerdefinierten Typs vertraulicher Informationen ein, und laden Sie ihn hoch. Jetzt wird das Wörterbuch in Ihrer Liste der Typen vertraulicher Informationen angezeigt, und Sie können es direkt in Ihrer Richtlinie verwenden und festlegen, bei wie vielen Schlüsselwörtern eine Übereinstimmung festgestellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ac5e4-p119">Paste the identity into your custom sensitive information type's XML and upload it. Now your dictionary will appear in your list of sensitive information types and you can use it right in your policy, specifying how many keywords are required to match.</span></span>
  
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


