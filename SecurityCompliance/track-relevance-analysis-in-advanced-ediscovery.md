---
title: Nachverfolgen von Relevanz Analyse in Office 365 erweiterte eDiscovery
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
ms.assetid: 3ab1e2c3-28cf-4bf5-b0a8-c0222f32bdf5
description: 'Informationen Sie zum Anzeigen und Interpretieren der Relevanz Schulung Status und das Ergebnis für Groß-/Kleinschreibung Probleme in Office 365 erweiterte eDiscovery.  '
ms.openlocfilehash: a19f7eaabf5dc15eefaa7209ded8261020d0d557
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530106"
---
# <a name="track-relevance-analysis-in-office-365-advanced-ediscovery"></a>Nachverfolgen von Relevanz Analyse in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Im erweiterten eDiscovery die Relevanz nachverfolgen-Registerkarte zeigt die berechnete Gültigkeit der Relevanz Schulung in die Registerkarte Tag ausgeführt und gibt an, der nächste Schritt im Prozess iterative Schulung in Relevanz zu übernehmen. 
  
## <a name="tracking-relevance-training-status"></a>Verlaufstatus Relevanz-Schulung

1. Anzeigen die folgenden Details in Relevanz Nachverfolgen für die Groß-/Kleinschreibung Probleme, wie im folgenden Beispiel wird ein Dialogfeld " **Problem Name** " gezeigt. 
    
  - **Assessment**: Diese Statusanzeige zeigt, in welchem Ausmaß die Relevanz Schulung bisher ausgeführten das Ziel der Bewertung im Hinblick auf Fehlermarge von erreicht hat. Auch wird vom Umfang der Relevanz Schulung Ergebnisse angezeigt. 
    
  - **Schulung**: dieser farbcodierten Fortschrittsanzeige Indikator- und QuickInfo gibt an, die Relevanz Schulung erzeugt Stabilität und eine numerische Skala mit der Anzahl der Relevanz Schulungsbeispiele für jedes Problem markiert. Der Experte überwacht den Status des Schulungsprozesses iterative Relevanz. 
    
  - **Batch-Berechnung**: Diese Statusanzeige enthält Informationen über den Abschluss der Batch Berechnung.
    
  - **Als Nächstes**: Zeigt die Empfehlung für den nächsten Schritt ausgeführt werden. 
    
    Im Beispiel wird eine erfolgreich abgeschlossene Bewertung für ein Problem angezeigt, durch die Statusanzeige abgeschlossenen Farbe und das Häkchen gekennzeichnet. Markieren aktiviert ist, aber die Groß-/Kleinschreibung wird weiterhin als instabil betrachtet (Stabilität Status auch in einer QuickInfo angezeigt). Die nächste Schritt Empfehlung ist "Training". 
    
    ![Schulung für Relevanznachverfolgung: Schritt 1](media/a00fe607-680a-48eb-9d61-4565319f7ab6.png)
  
    Die erweiterten zeigt zusätzliche Informationen und Optionen. Angezeigten aktuellen Fehler Rand wird der Fehler Rand der Rückruf in den aktuellen Status der Bewertung, die vorhandenen Dateien (bereits markierte) Assessment angegeben.
    
    > [!NOTE]
    >  Die Phase Assessment kann durch Deaktivieren des Kontrollkästchens **Assessment** pro Problem, und klicken Sie dann für "alle Probleme" umgangen werden. Dementsprechend, werden es jedoch keine Statistiken für dieses Problem. > Deaktivieren des Kontrollkästchens **Assessment** kann nur ausgeführt werden, bevor Assessment ausgeführt wird. In dem Fall mehrere Probleme vorhanden sind, wird zur Bewertung umgangen nur, wenn das Kontrollkästchen für jedes Problem deaktiviert ist 
  
    Wenn Assessment mit nicht abgeschlossen wird im erste Beispiel von Dateien festgelegt ist, zur Bewertung möglicherweise im nächsten Schritt zum Markieren von Weitere Dateien. 
    
    In der **Relevanz** \> **Nachverfolgen**, die Statusanzeige für Schulung und QuickInfo Geben Sie an, die geschätzte Anzahl der Weitere Beispiele erforderlich, um die Stabilität zu erreichen. Bei dieser Schätzung bietet eine Richtlinie für die zusätzliche Schulungen erforderlich.
    
    ![Schulung für Relevanznachverfolgung](media/98dbc3f5-5238-4d73-9f88-1aa4d77ea729.png)
  
2. Wenn Sie sind fertig Kategorien und Schulung fortsetzen möchten, klicken Sie auf **Schulung**. Reihe von Dateien in einer anderen Beispieldaten wird aus der geladene Datei legen Sie für zusätzliche Schulungen generiert. Sie kehren klicken Sie dann auf die Registerkarte-Tag zum Markieren und weitere Dateien Schulen.
    
### <a name="reaching-stable-training-levels"></a>Erreichen von stabil Schulung Ebenen

Nachdem die Dateien zur Bewertung eine stabile Ebene der Schulung erreicht haben, ist erweiterte eDiscovery für Batch Berechnung bereit.
  
> [!NOTE]
> Nach drei Schulungsbeispiele stabil, besteht der nächste Schritt in der Regel "Batch Berechnung". Möglicherweise gibt es Ausnahmen, beispielsweise bei Änderungen an der Kategorien von Dateien aus früheren Beispiele oder wann Seed Dateien hinzugefügt wurden. 
  
### <a name="performing-batch-calculation"></a>Batch-Berechnung ausführen

Batch-Berechnung wird im nächsten Schritt ausgeführt, nachdem Schulung erfolgreich abgeschlossen wurde (bei einer stabilen Schulung der Statusanzeige, einer Markierung und stabilen Status in der QuickInfo angezeigt wird.) Batch Berechnung gilt, die während der Relevanz Schulungen für die gesamte Datei Auffüllung, der Dateien Relevanz bewerten und Zuweisen von Relevanz Bewertungen erworbene Kenntnisse.
  
Wenn mehr als ein Problem vorliegt, erfolgt Batch Berechnung pro Problem. Während der Berechnung Batch wird Fortschritt überwacht, während der Verarbeitung aller Dateien. 
  
Hier ist die empfohlene Nächstes "None", die angibt, dass keine weiteren iterative Relevanz Schulung zu diesem Zeitpunkt erforderlich ist. Die nächste Phase ist die **Relevanz \> Decide** Registerkarte. 
  
Wenn Sie neue Dateien nach Batch Berechnung importieren möchten, kann der Administrator ein neues laden die importierten Dateien hinzufügen.
  
> [!NOTE]
> Wenn Sie während der Berechnung Batch auf **Abbrechen** klicken, speichert der Prozess an, welche bereits ausgeführt wurde. Wenn Sie Batch Berechnung erneut ausführen, wird der Prozess der letzte Punkt ausgeführten fortgeführt werden. 
  
### <a name="assessing-tagging-consistency"></a>Bewerten der Konsistenz von Kategorien

Wenn Inkonsistenzen in Datei tagging vorhanden sind, können sie die Analyse beeinflussen. Die erweiterte eDiscovery tagging-Konsistenz Prozess kann verwendet werden, wenn Ergebnisse nicht optimal sind oder Konsistenz nicht sicher sind ist. Eine Liste der möglichen inkonsistent markierte Dateien zurückgegeben wird, und überprüft und erneut markiert, nach Bedarf werden können.
  
> [!NOTE]
> Nach dem folgenden Assessment, markieren die Konsistenz in **Relevanz** angezeigt werden kann sieben oder mehr Schulungen rundet \> **Nachverfolgen** \> **Problem** \> **ausführliche Ergebnisse** \> **Status der Erfassung**. Diese Überprüfung wird zu einem Zeitpunkt für ein Problem durchgeführt. 
  
1. In **Relevanz \> nachverfolgen**, ein Problem Zeile erweitern.
    
2. Rechts neben der **nächste Schritt darin**klicken Sie auf **Ändern**.
    
3. Wählen Sie **Tag Inkonsistenzen** als **nächsten Schritt** Option, nach sieben Schulungsbeispiele, und klicken Sie auf **OK**.
    
4. Wählen Sie **Tag Inkonsistenzen**aus. Die Registerkarte **Tag** wird geöffnet, und eine Übersicht über die Inkonsistenzen bei Bedarf erneut markieren. 
    
5. Klicken Sie auf **berechnen** , um die Änderungen zu übermitteln. Der nächste Schritt nach dem Markieren von Inkonsistenzen ist "Training". 
    
## <a name="viewing-and-using-relevance-results"></a>Anzeigen und Verwenden der Relevanz von Suchergebnissen

In der **Relevanz \> nachverfolgen** Registerkarte, erweitern Sie ein Problem Zeile und neben **ausführliche Ergebnisse**, klicken Sie auf **Ansicht**. Die ausführliche Ergebnisbereiche werden angezeigt, wie dargestellt und unten beschrieben.
  
![Detaillierte Ergebnisse der Relevanzschulung](media/495c04a9-ed1e-4355-8cab-c14270ca2bbb.png)
  
### <a name="tagging-summary"></a>Zusammenfassung markieren

 Im nachfolgenden Beispiel zeigt die **Zusammenfassung Tagging** Summen für die einzelnen Assessment, Schulung und tagging Prozesse hervorgehobene Datei. 
  
![Taggingzusammenfassung der Relevanznachverfolgung](media/0ec906fc-bc84-4245-a964-fb3ca37891db.png)
  
### <a name="keywords"></a>Keywords

Ein Schlüsselwort ist eine eindeutige Zeichenfolge, Word, Ausdruck oder Sequenz von Wörtern in einer Datei identifizierten erweiterte eDiscovery als eine erhebliche Indikator gibt an, ob eine Datei relevant ist. Die Spalten "Include" auflisten Schlüsselwort und Weights in Dateien als Relevant markiert und die Spalten "Ausschließen" aufgeführt sind, Schlüsselwörter und Weights in Dateien, die als nicht markierte relevant.
  
Erweiterte eDiscovery weist positiven oder negativen Schlüsselwort die Weight-Werte. Je höher die Gewichtung, je höher ist die Wahrscheinlichkeit, dass eine Datei, in der das Schlüsselwort angezeigt wird, während der Berechnung Batch eine höhere Relevanz Punktzahl zugewiesen ist. 
  
Die erweiterte eDiscovery-Liste der Schlüsselwörter kann verwendet werden, um eine Liste erstellt nach einem Experten oder als eine indirekte plausibilitätsprüfung ergänzen Überprüfungsprozess an einer beliebigen Stelle in der Datei.
  
### <a name="training-progress"></a>Status der Erfassung

Die **Schulung des Fortschritts** enthält eine Schulung Diagramm und die Qualität Indikator Fortschrittsanzeige, wie im folgenden Beispiel dargestellt. 
  
![Schulungsstatus für Relevanznachverfolgung](media/8a5089f5-a162-4246-ae09-bc1921859860.png)
  
 **Schulung Qualität Indikator**: Zeigt die Bewertung für die Kategorien Konsistenz wie folgt:
  
- **Eine gute**: Dateien konsistent markiert sind. (Grünes Licht angezeigt)
    
- **Mittel**: einige Dateien möglicherweise inkonsistent markiert werden. (Gelbes Licht angezeigt)
    
- **Warnung**: viele Dateien möglicherweise inkonsistent markiert werden. (Rot hell angezeigt)
    
 **Schulung des Fortschritts Diagramm**: Zeigt den Grad der Relevanz Schulung Stabilität nach einer Anzahl von Relevanz Schulung Zyklen im Vergleich zu F-Messwert. Wie wir von links nach rechts bewegen des Fokus auf das Diagramm, das Konfidenzintervall eingegrenzt und verwendet wird, zusammen mit der F-Measure, indem erweiterte eDiscovery Relevanz Stabilität bestimmen die Relevanz Schulung Wenn als Ergebnis sind optimiert.
  
> [!NOTE]
> Relevanz verwendet F2, eine F-Measure Metrik, in denen Rückruf doppelt so viel Gewichtung als Genauigkeit erhält. Für Fälle mit hoher Funktionsvielfalt (über 25 %) Relevanz verwendet F1 (Verhältnis 1:1). Das Verhältnis von F-Measure kann konfiguriert werden, während des Setups von **Relevanz** \> **Erweiterte Einstellungen**. 
  
### <a name="batch-calculation-results"></a>Ergebnisse der Batch

Im **Batch Berechnung Ergebnisbereich** enthält die Anzahl der Dateien, die für Relevanz,, wie folgt bewertet wurden: 
  
- **Success**
    
- **Leere**: enthält keinen Text, beispielsweise nur Leerzeichen/Registerkarten
    
- **Fehler**: aufgrund von übermäßig viele Größe oder konnte nicht gelesen werden
    
- **Ignoriert**: übermäßig viele nach Größe
    
- **Nebulous**: enthält Text ohne Bedeutung oder keine Features für das Problem relevant
    
> [!NOTE]
> Leer ist, Fehler, ignoriert oder Nebulous einen Faktor Relevanz von-1 erhält. 
  
### <a name="training-statistics"></a>Schulung-Statistik

Bereich **Training Statistik** werden Statistiken und Diagramme auf der Grundlage von erweiterten eDiscovery Relevanz Training Ergebnisse angezeigt. 
  
![Schulungsstatistiken für Relevanznachverfolgung](media/9a07740e-20d3-49fb-b9b9-84265e0a1836.png)
  
In dieser Ansicht werden die folgenden:
  
- **Überprüfung-Rückruf Verhältnis**: Vergleich der Ergebnisse nach Relevanz in einer wollte linear Überprüfung bewertet. Rückruf wird geschätzt bei Überprüfung Set Größe einer Gruppe.
    
- **Parameter**: kumulative berechnet Statistiken für die Überprüfung in Bezug auf die Datei Auffüllung für die gesamte Groß-/Kleinschreibung festgelegt.
    
- **Überprüfen**: Prozentsatz der Dateien überprüfen basierend auf dieser Grenzwert.
    
- **Denken Sie daran**: Prozentsatz der Relevant Dateien in der Sammlung überprüfen. 
    
- **Verteilung relevanzbewertung**: Dateien in die dunklen Grau Anzeige auf der linken Seite unterhalb der trennwert Score sind. Eine QuickInfo zeigt die Relevanz Bewertung und der zugehörigen Prozentsatz der Dateien in die Überprüfungsdatei in Bezug auf die Gesamtzahl der Dateien festgelegt.
    
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Bewertung in Relevanz](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Ausführen und Überprüfen von Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Ausführen der Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Entscheidung basierend auf den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

