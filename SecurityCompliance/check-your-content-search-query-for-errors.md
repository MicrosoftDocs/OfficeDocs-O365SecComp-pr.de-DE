---
title: Überprüfen Ihrer Inhaltssuche auf Fehler
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
description: Überprüfen Sie die Schlüsselwort-Abfrage für die Inhaltssuche für Fehler und Tippfehler, wie beispielsweise nicht unterstützte Zeichen und Kleinbuchstaben Sie boolesche Operatoren, vor dem Ausführen der Suche. Wenn einen Fehler gefunden, wird eine überarbeitete Abfrage empfohlen.
ms.openlocfilehash: 6ae14edc29bb7f8bab5dd2306282a69443872633
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038288"
---
# <a name="check-your-content-search-query-for-errors"></a><span data-ttu-id="68bc2-104">Überprüfen Ihrer Inhaltssuche auf Fehler</span><span class="sxs-lookup"><span data-stu-id="68bc2-104">Check your Content Search query for errors</span></span>

<span data-ttu-id="68bc2-p102">Wenn Sie erstellen oder einer Inhaltssuche bearbeiten, haben Sie Office 365 überprüfen Sie Ihre Abfrage für nicht unterstützte Zeichen und boolesche Operatoren, die möglicherweise nicht groß geschrieben werden. Auf welche Weise? Klicken Sie einfach auf **Abfrage für Tippfehler überprüfen** auf der Abfrageseite eine Inhaltssuche.</span><span class="sxs-lookup"><span data-stu-id="68bc2-p102">When you create or edit a Content Search, you can have Office 365 check your query for unsupported characters and Boolean operators that might not be capitalized. How? Just click **Check query for typos** on the query page of a Content Search.</span></span> 
  
![Klicken Sie auf "Überprüfen Sie die Abfrage für Tippfehler" So überprüfen Sie die Suchabfrage für nicht unterstützte Zeichen](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
<span data-ttu-id="68bc2-p103">Es folgt eine Liste der nicht unterstützten Zeichen, denen wir für überprüfen. Nicht unterstützte Zeichen werden häufig ausgeblendet, und sie in der Regel verursacht einen Fehler beim Suchen oder unbeabsichtigte Ergebnisse zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="68bc2-p103">Here's a list of the unsupported characters that we check for. Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="68bc2-p104">**Typografische Anführungszeichen** - Smart einfachen und doppelte Anführungszeichen (auch als "typografische" bezeichnet) werden nicht unterstützt. Bei einer Suchabfrage kann nur gerader Anführungszeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68bc2-p104">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported. Only straight quotation marks can be used in a search query.</span></span> 
    
- <span data-ttu-id="68bc2-p105">**Nicht druckbare und Steuerzeichen** - nicht druckbare und Steuerzeichen darstellen keine schriftliche Symbol, wie ein alphanumerische Zeichen. Beispiele für nicht druckbare und Steuerzeichen Zeichen, das Formatieren von Text oder separaten Textzeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="68bc2-p105">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as a alpha-numeric character. Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 
    
- <span data-ttu-id="68bc2-115">**Ein links-nach-rechts und rechts-nach-links** - Dies sind Steuerzeichen verwendet, um die Ausrichtung des Textes für Links-nach-rechts-Sprachen (wie Englisch und Spanisch) und rechts-nach-links-Sprachen (wie Arabisch und Hebräisch) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="68bc2-115">**Left-to-right and right-to-left marks** - These are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>
    
- <span data-ttu-id="68bc2-p106">**Kleinbuchstaben boolesche Operatoren** – Wenn Sie einen booleschen Operators wie **AND**, **OR**und **nicht** bei einer Suchabfrage verwenden, muss er in Großbuchstaben sein. Wenn wir eine Abfrage nach Tippfehler einchecken, wird die Abfragesyntax häufig hingewiesen, dass ein booleschen Operators verwendet wird, obwohl Kleinbuchstabe Operatoren verwendet werden können; beispielsweise `(WordA or WordB) and (WordC or WordD)`.</span><span class="sxs-lookup"><span data-stu-id="68bc2-p106">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase. When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="68bc2-118">Was passiert, wenn eine Abfrage ein nicht unterstütztes Zeichen hat?</span><span class="sxs-lookup"><span data-stu-id="68bc2-118">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="68bc2-p107">Nicht unterstützte Zeichen in der Abfrage gefunden, wird eine Warnmeldung angezeigt, die nicht unterstützte Zeichen, die besagt, die gefunden wurden und eine Alternative vorschlägt. Klicken Sie dann haben Sie dann die Option lassen Sie die ursprüngliche Abfrage oder Ersetzen Sie ihn durch die vorgeschlagenen überarbeitete Abfrage. Hier ist ein Beispiel für die Warnung, die angezeigt wird, nachdem Sie für die Suchabfrage im vorherigen Screenshot **Abfrage für Tippfehler überprüfen** klicken. Beachten Sie, dass die ursprüngliche Abfrage typografische Anführungszeichen und Kleinbuchstaben boolesche Operatoren enthält.</span><span class="sxs-lookup"><span data-stu-id="68bc2-p107">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters that were found and a suggests an alternative. Then you then have the option keep the original query or replace it with the suggested revised query. Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot. Notice that the original query contains smart quotes and lowercase Boolean operators.</span></span> 
  
![Mit vorgeschlagenen Überarbeitung für Ihre Abfrage wird eine Warnmeldung angezeigt.](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="68bc2-124">Gewusst wie: verhindern, dass nicht unterstützte Zeichen in Suchabfragen</span><span class="sxs-lookup"><span data-stu-id="68bc2-124">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="68bc2-p108">Nicht unterstützte Zeichen werden in der Regel zu einer Abfrage hinzugefügt, wenn Sie kopieren Sie das Query- oder Teile der Abfrage aus anderen Programmen (wie Microsoft Word oder Microsoft Excel), und kopieren Sie sie in das Feld Stichwort auf der Abfrageseite ein Inhaltssuche. Die beste Möglichkeit zum verhindern, dass nicht unterstützte Zeichen ist, geben die Abfrage in das Feld Stichwort. Alternativ können Sie eine Abfrage aus Word oder Excel kopieren und fügen Sie ihn an der Datei in einem nur-Text-Editor wie Microsoft Notepad. Klicken Sie dann speichern Sie die Datei, und wählen Sie in der Dropdownliste **Codierung** **ANSI** . Dadurch werden alle Formatierungen und nicht unterstützten Zeichen entfernt. Sie können dann kopieren und fügen die Abfrage aus der Textdatei Schlüsselwort Abfrage im Feld.</span><span class="sxs-lookup"><span data-stu-id="68bc2-p108">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and copy them to the keyword box on the query page of a Content Search. The best way to prevent unsupported characters is to just type the query in the keyword box. Alternatively, you can copy a query from Word or Excel and then paste it to file in a plain text editor, such as Microsoft Notepad. Then save the text file and select **ANSI** in the **Encoding** drop-down list. This will remove any formatting and unsupported characters. Then you can copy and paste the query from the text file to the keyword query box.</span></span> 
