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
# <a name="check-your-content-search-query-for-errors"></a>Überprüfen Ihrer Inhaltssuche auf Fehler

Wenn Sie erstellen oder einer Inhaltssuche bearbeiten, haben Sie Office 365 überprüfen Sie Ihre Abfrage für nicht unterstützte Zeichen und boolesche Operatoren, die möglicherweise nicht groß geschrieben werden. Auf welche Weise? Klicken Sie einfach auf **Abfrage für Tippfehler überprüfen** auf der Abfrageseite eine Inhaltssuche. 
  
![Klicken Sie auf "Überprüfen Sie die Abfrage für Tippfehler" So überprüfen Sie die Suchabfrage für nicht unterstützte Zeichen](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
Es folgt eine Liste der nicht unterstützten Zeichen, denen wir für überprüfen. Nicht unterstützte Zeichen werden häufig ausgeblendet, und sie in der Regel verursacht einen Fehler beim Suchen oder unbeabsichtigte Ergebnisse zurückzugeben.
  
- **Typografische Anführungszeichen** - Smart einfachen und doppelte Anführungszeichen (auch als "typografische" bezeichnet) werden nicht unterstützt. Bei einer Suchabfrage kann nur gerader Anführungszeichen verwendet werden. 
    
- **Nicht druckbare und Steuerzeichen** - nicht druckbare und Steuerzeichen darstellen keine schriftliche Symbol, wie ein alphanumerische Zeichen. Beispiele für nicht druckbare und Steuerzeichen Zeichen, das Formatieren von Text oder separaten Textzeilen enthalten. 
    
- **Ein links-nach-rechts und rechts-nach-links** - Dies sind Steuerzeichen verwendet, um die Ausrichtung des Textes für Links-nach-rechts-Sprachen (wie Englisch und Spanisch) und rechts-nach-links-Sprachen (wie Arabisch und Hebräisch) anzugeben.
    
- **Kleinbuchstaben boolesche Operatoren** – Wenn Sie einen booleschen Operators wie **AND**, **OR**und **nicht** bei einer Suchabfrage verwenden, muss er in Großbuchstaben sein. Wenn wir eine Abfrage nach Tippfehler einchecken, wird die Abfragesyntax häufig hingewiesen, dass ein booleschen Operators verwendet wird, obwohl Kleinbuchstabe Operatoren verwendet werden können; beispielsweise `(WordA or WordB) and (WordC or WordD)`.
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a>Was passiert, wenn eine Abfrage ein nicht unterstütztes Zeichen hat?

Nicht unterstützte Zeichen in der Abfrage gefunden, wird eine Warnmeldung angezeigt, die nicht unterstützte Zeichen, die besagt, die gefunden wurden und eine Alternative vorschlägt. Klicken Sie dann haben Sie dann die Option lassen Sie die ursprüngliche Abfrage oder Ersetzen Sie ihn durch die vorgeschlagenen überarbeitete Abfrage. Hier ist ein Beispiel für die Warnung, die angezeigt wird, nachdem Sie für die Suchabfrage im vorherigen Screenshot **Abfrage für Tippfehler überprüfen** klicken. Beachten Sie, dass die ursprüngliche Abfrage typografische Anführungszeichen und Kleinbuchstaben boolesche Operatoren enthält. 
  
![Mit vorgeschlagenen Überarbeitung für Ihre Abfrage wird eine Warnmeldung angezeigt.](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a>Gewusst wie: verhindern, dass nicht unterstützte Zeichen in Suchabfragen

Nicht unterstützte Zeichen werden in der Regel zu einer Abfrage hinzugefügt, wenn Sie kopieren Sie das Query- oder Teile der Abfrage aus anderen Programmen (wie Microsoft Word oder Microsoft Excel), und kopieren Sie sie in das Feld Stichwort auf der Abfrageseite ein Inhaltssuche. Die beste Möglichkeit zum verhindern, dass nicht unterstützte Zeichen ist, geben die Abfrage in das Feld Stichwort. Alternativ können Sie eine Abfrage aus Word oder Excel kopieren und fügen Sie ihn an der Datei in einem nur-Text-Editor wie Microsoft Notepad. Klicken Sie dann speichern Sie die Datei, und wählen Sie in der Dropdownliste **Codierung** **ANSI** . Dadurch werden alle Formatierungen und nicht unterstützten Zeichen entfernt. Sie können dann kopieren und fügen die Abfrage aus der Textdatei Schlüsselwort Abfrage im Feld. 
