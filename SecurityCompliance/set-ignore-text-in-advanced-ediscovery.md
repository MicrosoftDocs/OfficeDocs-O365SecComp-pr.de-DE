---
title: Legen Sie Text ignorieren-Option für die Analyse in Office 365 erweiterte eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Erfahren Sie, wie die Regel, um bestimmten Text ignoriert wird, wenn mit den Modulen analysieren und Prozess in Office 365 erweiterte eDiscovery definieren.  '
ms.openlocfilehash: eb7e7052979087b7dba98aac3b0c9ab75ec0d02a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529494"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a>Legen Sie Text ignorieren-Option für die Analyse in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Das Feature ignorieren Text angewendet werden soll, auf alle oder auf die folgenden erweiterten eDiscovery-Module: Analysieren (in der Nähe Duplikate, E-Mail-Threads Designs) und Relevanz. Ignorierte Text wird nicht angezeigt, in der Dateien werden in Relevanz angezeigt, und die Analysis-Berechnungen verwirft des ignorierten Texts.
  
Wenn das Feature Text ignorieren für Module zuvor definiert wurde, die bereits ausgeführt haben, wird die Einstellung Text ignorieren geändert wird, wird nun geschützt werden. Das Feature ignorieren Text für das Modul Relevanz kann jedoch weiterhin jederzeit geändert werden.
  
## <a name="how-ignore-text-filters-are-applied"></a>Anwenden von Filtern für Text ignorieren

Mehrere Text ignorieren Filter werden in der Reihenfolge angewendet, dass sie eingegeben wurden. Zum Ändern der Reihenfolge, in der sie angewendet werden, müssen sie gelöscht und in der gewünschten Reihenfolge erneut eingegeben werden.
  
Beispiel: bei der Textinhalt ist: "DAVE BOB ALICE CAROL EVE", die im folgenden sind Beispiele für ignorieren Texteinträge und die Ergebnisse:
  
||||
|:-----|:-----|:-----|
|**Texteinträge ignorieren** <br/> |**==\>** <br/> |**Ergebnisse** <br/> |
|"ALICE", "BOB CAROL"  <br/> |==\>  <br/> |"DAVE EVE"  <br/> |
|"ALICE", "BOB ALICE CAROL"  <br/> |==\>  <br/> |"DAVE BOB CAROL EVE"  <br/> |
   
Die zweite ignorieren Texteingabe ist nicht implementiert, da die Zeichenfolge als solche nicht gefunden wird, nachdem der erste ignorieren Text angewendet wurde.
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a>Verwenden Sie reguläre Ausdrücke beim Definieren der Text ignorieren

Reguläre Ausdrücke werden für die Verwendung unterstützt, wenn Text ignorieren definieren. Es folgen Beispiele für die Syntax für reguläre Ausdrücke und Verwendung:
  
- So entfernen Sie (ignorieren) Text vom Anfang bis zum Ende einer Zeile:
    
     `Begin(.*)$`
    
    Dabei ist "Begin" das erste Auftreten des diese Zeichenfolge in der Zeile.
    
    Zum Beispiel für den folgenden Text:
    
    **"Dies ist ersten Satz und die erste Zeile**
    
    **Dies ist die zweite Satz und zweiten Zeile"**
    
    der reguläre Ausdruck first(.\*) $ führt zu:
    
    **"Dies ist**
    
    **Dies ist die zweite Satz und zweiten Zeile"**
    
- So entfernen Sie Haftungsausschluss und rechtliche Anweisungen automatisch am Ende des e-Mail-Threads eingefügt:
    
     `Begin(.|\s)*End`
    
    wobei "Begin" und "End" eindeutige Zeichenfolgen am Anfang und Ende eines Absatzes umbrochenen Text sind. 
    
    Im folgende reguläre Ausdruck entfernt beispielsweise Haftungsausschluss und rechtliche Anweisungen, die in der e-Mail-Thread zwischen den Zeichenfolgen Begin- und End wurden:
    
    **Diese Nachricht enthält vertrauliche Informationen (. | \s)\*, wenn die Überprüfung erforderlich ist, fordern Sie eine harte Kopie-Version**
    
- So entfernen Sie einen Haftungsausschluss (einschließlich Sonderzeichen) 
    
    Zum Beispiel für den folgenden Text (mit der Haftungsausschluss hier dargestellt durch x): 
    
    **/\*\ Diese Nachricht enthält vertrauliche Informationen. Xxxx-xxxx**
    
    **Xxxx Xxxx Xxxx Xxxx Xxxx-Xxxx-xxxx**
    
    **Xxxx-Xxxx, wenn die Überprüfung erforderlich ist, fordern Sie eine harte Kopie Version. /\*\**
    
    der reguläre Ausdruck, den oben genannten Haftungsausschluss entfernen sollte sein: 
    
    **\/\\*\\Diese Nachricht enthält vertrauliche Informationen\.(. | \s)\* , wenn die Überprüfung erforderlich ist, fordern Sie eine harte Kopie Version\.\/\\*\\**
    
- Regeln für den regulären Ausdruck:
    
  - Alle Zeichen, die nicht Teil des Alphabets mit Ausnahme aufhören, "_" sind und "-" muss vorangestellt werden "\".
    
  - Feld reguläre eExpression kann unbegrenzte Länge sein.
    
> [!TIP]
> Eine Erläuterung und Informationen zur Syntax von regulären Ausdrücken finden Sie unter: [Regulären Ausdruck Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx). 
  
## <a name="define-ignore-text-rule"></a>Definieren der Regel Text ignorieren

1. In der **verwalten \> Analyze \> analysieren Optionen** Registerkarte im Abschnitt **Text ignoriert wird** , klicken Sie auf die **+** Symbol, um eine Regel hinzuzufügen. 
    
2. Geben Sie im Dialogfeld **Ignorieren Text hinzufügen** im Feld **Name** einen Namen für die Regel Text ignoriert wird. 
    
    ![Ignorierten Text hinzufügen](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. Geben Sie in das **Textfeld** den Text ignoriert werden soll. Das Textfeld ermöglicht eine unbegrenzte Anzahl von Zeichen. 
    
    > [!TIP]
    > Wie im obigen Fenster angezeigt wird, klicken Sie auf **Glühbirne** um allgemeine Syntax Richtlinien für die Regel ignorieren Text anzuzeigen. 
  
4. Wählen Sie bei Bedarf das Kontrollkästchen **Groß-/Kleinschreibung beachten** . 
    
5. Wählen Sie in der Liste **Übernehmen für** die erweiterte eDiscovery-Module in der Definition die angewendet. 
    
6. Wenn Sie einen Testlauf auf Beispieltext möchten, geben Sie in das Textfeld **Eingabe** Beispieltext ein, und klicken Sie auf **Testen**. Die Ergebnisse werden in das Textfeld **Ausgabe** angezeigt. 
    
7. Klicken Sie auf **OK** , um die Regel ignorieren Text zu speichern. Die definierte Text ignorieren Regel wird angezeigt. 
    
    ![Set hat Textname ignoriert](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zu Dokument Ähnlichkeit](understand-document-similarity-in-advanced-ediscovery.md)
  
[Festlegen von Optionen für Analyse](set-analyze-options-in-advanced-ediscovery.md)
  
[Analysieren der Einstellung Erweiterte Einstellungen](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Anzeigen von Ergebnissen der Analyse](view-analyze-results-in-advanced-ediscovery.md)

