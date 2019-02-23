---
title: Festlegen der Option zum Ignorieren von Text für die Analyse in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Erfahren Sie, wie Sie die Regel definieren, um bestimmten Text zu ignorieren, wenn Sie die Module analyze und Process in Office 365 Advanced eDiscovery verwenden.  '
ms.openlocfilehash: 3a4c1d17a9a56d3018509a8dcfd6b49abb951676
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214245"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a>Festlegen der Option zum Ignorieren von Text für die Analyse in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Das Feature Text ignorieren kann auf alle oder eines der folgenden erweiterten eDiscovery-Module angewendet werden: analysieren (Near-Duplikate, e-Mail-Threads, Designs) und Relevanz. Ignorierter Text wird nicht in der Relevanz angezeigt, und die Analyse/Berechnungen verwirft den ignorierten Text.
  
Wenn das Feature Text ignorieren zuvor für Module definiert wurde, die bereits ausgeführt wurden, wird die Einstellung Text ignorieren jetzt vor der Änderung geschützt. Das Feature Text ignorieren für das Relevance-Modul kann jedoch jederzeit geändert werden.
  
## <a name="how-ignore-text-filters-are-applied"></a>Anwenden von Ignore-Text filtern

Mehrere Ignore-Text Filter werden in der Reihenfolge angewendet, in der Sie eingegeben wurden. Um die Reihenfolge zu ändern, in der Sie angewendet werden, müssen Sie gelöscht und in der gewünschten Reihenfolge erneut eingegeben werden.
  
Wenn der Textinhalt beispielsweise "DAVE BOB ALICE CAROL EVE" lautet, sind die folgenden Beispiele für Ignore-Texteinträge und die Ergebnisse:
  
||||
|:-----|:-----|:-----|
|**Text Einträge ignorieren** <br/> |**==\>** <br/> |**Ergebnisse** <br/> |
|"ALICE", "BOB CAROL"  <br/> |==\>  <br/> |"DAVE EVE"  <br/> |
|"ALICE", "BOB ALICE CAROL"  <br/> |==\>  <br/> |"DAVE BOB CAROL EVE"  <br/> |
   
Der zweite Ignore-Texteintrag wird nicht implementiert, da die Zeichenfolge nicht als solches gefunden wird, nachdem der erste Text ignoriert wurde.
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a>Verwenden regulärer Ausdrücke beim Definieren von Text ignorieren

Reguläre Ausdrücke werden für die Verwendung beim Definieren von Text ignorieren unterstützt. Im folgenden finden Sie Beispiele für Syntax und Verwendung regulärer Ausdrücke:
  
- So entfernen (ignorieren) Sie Text von Anfang bis zum Ende einer Zeile:
    
     `Begin(.*)$`
    
    Dabei ist "BEGIN" das erste Vorkommen dieser Zeichenfolge in der Linie.
    
    Beispiel für den folgenden Text:
    
    **"Dies ist der erste Satz und die erste Reihe**
    
    **Dies ist der zweite Satz und die zweite Reihe.**
    
    der reguläre Ausdruck zuerst (.\*) $ führt zu:
    
    **"Dies ist**
    
    **Dies ist der zweite Satz und die zweite Reihe.**
    
- So entfernen Sie Haftungsausschlüsse und-Anweisungen, die am Ende der e-Mail-Threads automatisch eingefügt werden:
    
     `Begin(.|\s)*End`
    
    wobei "BEGIN" und "End" eindeutige Zeichenfolgen am Anfang und am Ende eines umgebrochenen Textabsatzes sind. 
    
    Der folgende reguläre Ausdruck entfernt beispielsweise Haftungsausschlüsse und rechtliche Anweisungen, die sich im e-Mail-Thread zwischen der BEGIN-und der End-Zeichenfolge befanden:
    
    **Diese Nachricht enthält vertrauliche Informationen (. | \s)\*wenn eine Überprüfung erforderlich ist, fordern Sie eine Hardcopy-Version an.**
    
- So entfernen Sie einen Haftungsausschluss (einschließlich Sonderzeichen): 
    
    Beispielsweise für den folgenden Text (mit dem hier durch x dargestellten Haftungsausschluss): 
    
    **/\*\ Diese Nachricht enthält vertrauliche Informationen. xxxx xxxx**
    
    **xxxx xxxx xxxx xxxx xxxx xxxx xxxx**
    
    **xxxx xxxx wenn eine Überprüfung erforderlich ist, fordern Sie eine Version an. /\*\**
    
    der reguläre Ausdruck zum Entfernen des obigen Haftungsausschlusses sollte: 
    
    **\/\\*\\Diese Nachricht enthält vertrauliche\.Informationen (. | \s)\* wenn eine Überprüfung erforderlich ist, fordern Sie eine Hardcopy\. -Version an.\/\\*\\**
    
- Regeln für reguläre Ausdrücke:
    
  - Alle Zeichen, die nicht Teil des Alphabets sind, mit Ausnahme von Space (s), "_" und "-" müssen vorangestellt\"werden. "
    
  - Das reguläre eExpression-Feld kann unbegrenzte Länge aufweisen.
    
> [!TIP]
> Eine Erläuterung und ausführliche Syntax regulärer Ausdrücke finden Sie unter: [Regular Expression Language-Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx). 
  
## <a name="define-ignore-text-rule"></a>Ignore-Text Regel definieren

1. Klicken Sie auf der Registerkarte **Analyse \> \> Optionen verwalten** im Abschnitt **Text ignorieren** auf das **+** Symbol, um eine Regel hinzuzufügen. 
    
2. Geben Sie im Dialogfeld **ignorieren-Text hinzufügen** unter **Name** einen Namen für die Regel zum Ignorieren von Text ein. 
    
    ![Ignorierten Text hinzufügen](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. Geben Sie **** in das Textfeld den zu ignorierenden Text ein. Das Textfeld erlaubt eine unbegrenzte Anzahl von Zeichen. 
    
    > [!TIP]
    > Wie im obigen Fenster angezeigt, klicken Sie **** auf Glühbirne, um allgemeine Syntax Richtlinien für die Ignore-Textregel anzuzeigen. 
  
4. Aktivieren Sie bei Bedarf das Kontrollkästchen **groß** -/Kleinschreibung beachten. 
    
5. Wählen Sie in der Liste **übernehmen für** die erweiterten eDiscovery-Module aus, auf die die Definition angewendet werden soll. 
    
6. Wenn Sie einen Testlauf im Beispieltext ausführen möchten, geben Sie Beispieltext in das Textfeld **Eingabe** ein, und klicken Sie auf **Testen**. Die Ergebnisse werden im Textfeld **Ausgabe** angezeigt. 
    
7. Klicken Sie auf **OK** , um die ignoriertext-Regel zu speichern. Die definierte Ignore-Textregel wird angezeigt. 
    
    ![Set hat Textname ignoriert](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Dokument Ähnlichkeit](understand-document-similarity-in-advanced-ediscovery.md)
  
[Festlegen von Analyseoptionen](set-analyze-options-in-advanced-ediscovery.md)
  
[Einstellung "Erweiterte Einstellungen analysieren"](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Anzeigen von Analyseergebnissen](view-analyze-results-in-advanced-ediscovery.md)

