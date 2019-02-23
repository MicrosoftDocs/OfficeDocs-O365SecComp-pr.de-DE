---
title: Überprüfen Ihrer Inhaltssuche auf Fehler
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 11/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 88898874-e262-4c5c-b6d2-4e697497fc74
description: Überprüfen Sie Ihre Stichwortabfrage auf die Inhaltssuche nach Fehlern und Tippfehler, wie nicht unterstützte Zeichen und klein geschriebene boolesche Operatoren, bevor Sie die Suche ausführen. Wenn ein Fehler auftritt, wird eine überarbeitete Abfrage vorgeschlagen.
ms.openlocfilehash: 00612116f345e2a01471d5c83df77f4bc8db9ce5
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215935"
---
# <a name="check-your-content-search-query-for-errors"></a><span data-ttu-id="85ee4-104">Überprüfen Ihrer Inhaltssuche auf Fehler</span><span class="sxs-lookup"><span data-stu-id="85ee4-104">Check your Content Search query for errors</span></span>

<span data-ttu-id="85ee4-p102">Wenn Sie eine Inhaltssuche erstellen oder bearbeiten, können Sie in Office 365 die Abfrage auf nicht unterstützte Zeichen und boolesche Operatoren überprüfen, die möglicherweise nicht groß geschrieben werden. , Wie? Klicken Sie auf der Seite Abfrage einer Inhaltssuche einfach auf **Abfrage für Tippfehler überprüfen** .</span><span class="sxs-lookup"><span data-stu-id="85ee4-p102">When you create or edit a Content Search, you can have Office 365 check your query for unsupported characters and Boolean operators that might not be capitalized. How? Just click **Check query for typos** on the query page of a Content Search.</span></span> 
  
![Klicken Sie auf "Abfrage für Rechtschreibfehler überprüfen", um die Suchabfrage nach nicht unterstützten Zeichen zu überprüfen.](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
<span data-ttu-id="85ee4-p103">Hier finden Sie eine Liste der nicht unterstützten Zeichen, die wir prüfen. Nicht unterstützte Zeichen werden oft ausgeblendet, und Sie verursachen in der Regel einen Suchfehler oder geben unbeabsichtigte Ergebnisse zurück.</span><span class="sxs-lookup"><span data-stu-id="85ee4-p103">Here's a list of the unsupported characters that we check for. Unsupported characters are often hidden, and they typically cause a search error or return unintended results.</span></span>
  
- <span data-ttu-id="85ee4-p104">**Intelligente** Anführungszeichen: intelligente einfache und doppelte Anführungszeichen (auch als geschweifte Anführungszeichen bezeichnet) werden nicht unterstützt. In einer Suchabfrage können nur einfache Anführungszeichen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85ee4-p104">**Smart quotation marks** - Smart single and double quotation marks (also called curly quotes) aren't supported. Only straight quotation marks can be used in a search query.</span></span> 
    
- <span data-ttu-id="85ee4-p105">Nicht **druckbare und Steuerzeichen** -nicht druckbare und Steuerzeichen stellen kein schriftliches Symbol dar, wie beispielsweise ein alphanumerisches Zeichen. Beispiele für nicht druckbare und Steuerzeichen sind Zeichen, die Text oder separate Textzeilen formatieren.</span><span class="sxs-lookup"><span data-stu-id="85ee4-p105">**Non-printable and control characters** - Non-printable and control characters don't represent a written symbol, such as a alpha-numeric character. Examples of non-printable and control characters include characters that format text or separate lines of text.</span></span> 
    
- <span data-ttu-id="85ee4-115">**Links-nach-rechts-und rechts-nach-links** -Markierungen-Dies sind Steuerzeichen, die verwendet werden, um die Textrichtung für Links-nach-rechts-Sprachen (wie Englisch und Spanisch) und rechts-nach-links-Sprachen (wie Arabisch und Hebräisch) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="85ee4-115">**Left-to-right and right-to-left marks** - These are control characters used to indicate text direction for left-to-right languages (such as English and Spanish) and right-to-left languages (such as Arabic and Hebrew).</span></span>
    
- <span data-ttu-id="85ee4-p106">**Kleinbuchstaben-boolesche Operatoren** – Wenn Sie einen booleschen Operator verwenden, beispielsweise **and**, **or**und **nicht** in einer Suchabfrage, muss es sich um einen Großbuchstaben handeln. Wenn Sie eine Abfrage auf Tippfehler überprüfen, gibt die Abfragesyntax oft an, dass ein boolescher Operator verwendet wird, obwohl Kleinbuchstaben-Operatoren verwendet werden können. Beispiel: `(WordA or WordB) and (WordC or WordD)`.</span><span class="sxs-lookup"><span data-stu-id="85ee4-p106">**Lowercase Boolean operators** - If you use a Boolean operator, such as **AND**, **OR**, and **NOT** in a search query, it must be uppercase. When we check a query for typos, the query syntax will often indicate that a Boolean operator is being used even though lowercase operators might be used; for example,  `(WordA or WordB) and (WordC or WordD)`.</span></span>
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a><span data-ttu-id="85ee4-118">Was geschieht, wenn eine Abfrage ein nicht unterstütztes Zeichen enthält?</span><span class="sxs-lookup"><span data-stu-id="85ee4-118">What happens if a query has an unsupported character?</span></span>

<span data-ttu-id="85ee4-p107">Wenn in der Abfrage nicht unterstützte Zeichen gefunden werden, wird eine Warnmeldung angezeigt, die besagt, dass nicht unterstützte Zeichen gefunden wurden und eine Alternative vorgeschlagen wird. Dann haben Sie die Option, die ursprüngliche Abfrage beizubehalten, oder ersetzen Sie Sie durch die vorgeschlagene überarbeitete Abfrage. Nachfolgend sehen Sie ein Beispiel der Warnmeldung, die angezeigt wird, wenn Sie im vorherigen Screenshot auf **Abfrage für Tippfehler** für die Suchabfrage suchen klicken. Beachten Sie, dass die ursprüngliche Abfrage typografische Anführungszeichen und Kleinbuchstaben-boolesche Operatoren enthält.</span><span class="sxs-lookup"><span data-stu-id="85ee4-p107">If unsupported characters are found in your query, a warning message is displayed that says unsupported characters that were found and a suggests an alternative. Then you then have the option keep the original query or replace it with the suggested revised query. Here's an example of the warning message that's displayed after you click **Check query for typos** for the search query in the previous screenshot. Notice that the original query contains smart quotes and lowercase Boolean operators.</span></span> 
  
![Eine Warnmeldung wird mit einer vorgeschlagenen Überarbeitung für Ihre Abfrage angezeigt](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a><span data-ttu-id="85ee4-124">VorGehensWeise verhindern, dass nicht unterstützte Zeichen in Suchabfragen</span><span class="sxs-lookup"><span data-stu-id="85ee4-124">How to prevent unsupported characters in your search queries</span></span>

<span data-ttu-id="85ee4-p108">Nicht unterstützte Zeichen werden normalerweise zu einer Abfrage hinzugefügt, wenn Sie die Abfrage oder Teile der Abfrage aus anderen Anwendungen (wie Microsoft Word oder Microsoft Excel) kopieren und Sie in das Feld Stichwort auf der Seite Abfrage einer Inhaltssuche kopieren. Die beste Möglichkeit, nicht unterstützte Zeichen zu verhindern, ist das Eingeben der Abfrage in das Feld Stichwort. Alternativ können Sie eine Abfrage aus Word oder Excel kopieren und dann in einem nur-Text-Editor wie Microsoft Notepad in eine Datei einfügen. Speichern Sie dann die Textdatei, und wählen Sie in der Dropdownliste **Codierung** die Option **ANSI** aus. Dadurch werden alle Formatierungen und nicht unterstützten Zeichen entfernt. Anschließend können Sie die Abfrage kopieren und aus der Textdatei in das Feld Stichwortabfrage einfügen.</span><span class="sxs-lookup"><span data-stu-id="85ee4-p108">Unsupported characters are typically added to a query when you copy the query or parts of the query from other applications (such as Microsoft Word or Microsoft Excel) and copy them to the keyword box on the query page of a Content Search. The best way to prevent unsupported characters is to just type the query in the keyword box. Alternatively, you can copy a query from Word or Excel and then paste it to file in a plain text editor, such as Microsoft Notepad. Then save the text file and select **ANSI** in the **Encoding** drop-down list. This will remove any formatting and unsupported characters. Then you can copy and paste the query from the text file to the keyword query box.</span></span> 
