---
title: Überprüfen der Inhaltssuchabfrage auf Fehler
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
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32243660"
---
# <a name="check-your-content-search-query-for-errors"></a>Überprüfen der Inhaltssuchabfrage auf Fehler

Wenn Sie eine Inhaltssuche erstellen oder bearbeiten, können Sie in Office 365 die Abfrage auf nicht unterstützte Zeichen und boolesche Operatoren überprüfen, die möglicherweise nicht groß geschrieben werden. Wie? Klicken Sie auf der Seite Abfrage einer Inhaltssuche einfach auf **Abfrage für Tippfehler überprüfen** . 
  
![Klicken Sie auf "Abfrage für Rechtschreibfehler überprüfen", um die Suchabfrage nach nicht unterstützten Zeichen zu überprüfen.](media/e5314306-cfb2-481d-9b5c-13ce658156e7.png)
  
Hier finden Sie eine Liste der nicht unterstützten Zeichen, die wir prüfen. Nicht unterstützte Zeichen werden oft ausgeblendet, und Sie verursachen in der Regel einen Suchfehler oder geben unbeabsichtigte Ergebnisse zurück.
  
- **Intelligente** Anführungszeichen: intelligente einfache und doppelte Anführungszeichen (auch als geschweifte Anführungszeichen bezeichnet) werden nicht unterstützt. Nur gerade Anführungszeichen können in einer Suchabfrage verwendet werden. 
    
- Nicht **druckbare und Steuerzeichen** -nicht druckbare und Steuerzeichen stellen kein schriftliches Symbol dar, wie beispielsweise ein alphanumerisches Zeichen. Beispiele für nicht druckbare Zeichen und Steuerzeichen sind Zeichen, die Text formatieren oder Textzeilen trennen. 
    
- **Links-nach-rechts-und rechts-nach-links** -Markierungen-Dies sind Steuerzeichen, die verwendet werden, um die Textrichtung für Links-nach-rechts-Sprachen (wie Englisch und Spanisch) und rechts-nach-links-Sprachen (wie Arabisch und Hebräisch) anzugeben.
    
- **Kleinbuchstaben-boolesche Operatoren** – Wenn Sie einen booleschen Operator verwenden, beispielsweise **and**, **or**und **nicht** in einer Suchabfrage, muss es sich um einen Großbuchstaben handeln. Wenn Sie eine Abfrage auf Tippfehler überprüfen, gibt die Abfragesyntax oft an, dass ein boolescher Operator verwendet wird, obwohl Kleinbuchstaben-Operatoren verwendet werden können. Beispiel: `(WordA or WordB) and (WordC or WordD)`.
    
## <a name="what-happens-if-a-query-has-an-unsupported-character"></a>Was geschieht, wenn eine Abfrage ein nicht unterstütztes Zeichen enthält?

Wenn in der Abfrage nicht unterstützte Zeichen gefunden werden, wird eine Warnmeldung angezeigt, die besagt, dass nicht unterstützte Zeichen gefunden wurden und eine Alternative vorgeschlagen wird. Dann haben Sie die Option, die ursprüngliche Abfrage beizubehalten, oder ersetzen Sie Sie durch die vorgeschlagene überarbeitete Abfrage. Nachfolgend sehen Sie ein Beispiel der Warnmeldung, die angezeigt wird, wenn Sie im vorherigen Screenshot auf **Abfrage für Tippfehler** für die Suchabfrage suchen klicken. Beachten Sie, dass die ursprüngliche Abfrage typografische Anführungszeichen und Kleinbuchstaben-boolesche Operatoren enthält. 
  
![Eine Warnmeldung wird mit einer vorgeschlagenen Überarbeitung für Ihre Abfrage angezeigt](media/23214b30-8e52-412c-bd80-63fb1b3ed52d.png)
  
## <a name="how-to-prevent-unsupported-characters-in-your-search-queries"></a>VorGehensWeise verhindern, dass nicht unterstützte Zeichen in Suchabfragen

Nicht unterstützte Zeichen werden normalerweise zu einer Abfrage hinzugefügt, wenn Sie die Abfrage oder Teile der Abfrage aus anderen Anwendungen (wie Microsoft Word oder Microsoft Excel) kopieren und Sie in das Feld Stichwort auf der Seite Abfrage einer Inhaltssuche kopieren. Die beste Möglichkeit zur Verhinderung nicht unterstützter Zeichen besteht darin, die Abfrage direkt in das Schlüsselwortfeld einzugeben. Alternativ können Sie eine Abfrage aus Word oder Excel kopieren und in einem Nur-Text-Editor, z. B. Microsoft Editor, in eine Datei einfügen. Speichern Sie dann die Textdatei, und wählen Sie **ANSI** in der Dropdownliste **Codierung** aus. Dadurch werden alle Formatierungen und nicht unterstützten Zeichen entfernt. Anschließend können Sie die Abfrage aus der Textdatei kopieren und im Schlüsselwort-Abfragefeld einfügen. 
