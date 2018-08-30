---
title: Kategorien und Bewertung in Office 365 erweiterte eDiscovery
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
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: 'Überprüfen Sie die Schritte zum Ausführen der Bewertung Training, einschließlich Markieren von Dateien und zur der Bewertungsergebnisse im Office 365 erweiterte eDiscovery überprüfen. '
ms.openlocfilehash: 0f67dd4780a29536888231f556c18fe887f230ba
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529320"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a>Kategorien und Bewertung in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Abschnitt wird das Verfahren für die erweiterte eDiscovery Relevanz Assessment Modul. 
  
## <a name="performing-assessment-training-and-analysis"></a>Schulung zur Bewertung und Analysen durchführen

1. In der **Relevanz \> nachverfolgen** auf **Assessment** um Groß-/Kleinschreibung Bewertung zu starten. 
    
    Beispielsweise Zwecke in diesem Verfahren, eine Reihe von 500 Dateien Beispieldaten-Bewertung wird erstellt, und die Registerkarte **Tag** wird angezeigt, die den Bereich Kategorien, angezeigte Dateiinhalte und andere Kategorien Optionen enthält. 
    
    ![Registerkarte „Relevanztag“ für Bewertung](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. Überprüfen Sie jede Datei in der Stichprobe, Bestimmen der Relevanz für jedes Groß-/Kleinschreibung Problem der Datei, und markieren Sie die Datei mithilfe der Relevance (R) nicht relevant (Nr.) und überspringen Schaltflächen im Bereich **Kategorien Systemsteuerung** . 
    
    > [!NOTE]
    >  Assessment erfordert 500 markierte Dateien. Wenn Dateien "übersprungen" sind, erhalten Sie weitere Dateien zu markieren. 
  
3. Klicken Sie nachdem Sie alle Dateien in der Stichprobe tagging auf **berechnen**. 
    
    Die Bewertung aktuellen Fehler Rand und wie umfangreich berechnet und in der Registerkarte **Relevanz nachverfolgen** mit erweiterten Details pro Problem, angezeigt wird, wie unten dargestellt. Weitere Informationen zu diesem Dialogfeld werden später im Abschnitt "Überarbeiten Bewertung Ergebnisse" beschrieben. 
    
    ![Relevanznachverfolgung – Bewertung](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > Standardmäßig wird empfohlen, dass Sie mit dem nächsten Schritt Standard vornehmen, wenn die Statusanzeige zur Bewertung für das Problem abgeschlossen wurde, gibt an, dass das Bewertung Beispiel überprüft wurde und ausreichend relevante Dateien markiert wurden. > Andernfalls, wenn Sie die **Nachverfolgen** Registerkarte Ergebnisse und die Kontrolle der Rand von Fehler- und im nächsten Schritt anzeigen möchten, klicken Sie auf **Ändern** neben der **Nächste Schritt darin**, wählen Sie **Weiter zur Bewertung**und klicken Sie dann auf **OK**. 
  
1. Klicken Sie auf **Ändern** rechts neben das Kontrollkästchen **Assessment** zum Anzeigen und Bewertung Parameter pro Problem angeben. Ein Dialogfeld **Assessment Ebene** für jedes Problem wird angezeigt, wie im folgenden Beispiel dargestellt: 
    
    ![Fallproblem mit Bewertungsebene](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    Die folgenden Parameter für das Problem werden berechnet und im Dialogfeld **Assessment Ebene** angezeigt: 
    
    **Ziel Fehler Seitenrand für den Wiederaufruf schätzt**: basierend auf diesen Wert, wird die geschätzte Anzahl der zusätzliche Dateien erforderlich, um zu prüfen berechnet. Der Seitenrand für den Rückruf verwendet ist mehr als 75 % und mit einer 95 % Confidence Level. 
    
    **Zusätzliche Assessment Dateien erforderlich**: Gibt an, wie viele weitere Dateien sind erforderlich, wenn der aktuelle Fehler Seitenrand Anforderungen nicht erfüllt sind. 
    
2. So passen Sie den aktuellen Fehler Rand und finden Sie unter den Effekt der anderen Fehler Ränder (pro Problem):
    
1. Wählen Sie in der Liste **Wählen Sie Problem** ein Problem. 
    
2. Geben Sie im **Ziel Fehler Seitenrand für den Wiederaufruf schätzt**einen neuen Wert ein.
    
3. Klicken Sie auf **Werte aktualisieren** , um die Auswirkungen der die Korrekturen finden Sie unter. 
    
3. Klicken Sie auf **Erweitert** im Dialogfeld **Assessment Ebene** , auf die folgenden zusätzlichen Parameter und ausführliche Informationen finden Sie unter: 
    
    ![Bewertungsebene: erweiterte Ansicht für Fallproblem](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    **Geschätzte Funktionsvielfalt**: geschätzte Funktionsvielfalt gemäß den aktuellen Bewertungsergebnisse zur
    
    **Für den Rückruf angenommenen**: standardmäßig am Rand der Ziel-Fehler angewendet wird, um mehr als 75 % zurückzurufen. Klicken Sie auf **Bearbeiten** , wenn Sie möchten, ändern Sie diesen Parameter und Steuern des Rands von Fehler auf einem anderen Wertebereich Rückruf. 
    
    **Vertrauensebene**: Standardmäßig ist die empfohlene Fehler Seitenrands Confidence 95 %. Wenn Sie diesen Parameter ändern möchten, klicken Sie auf **Bearbeiten** . 
    
    **Erwartete Funktionsvielfalt Fehler Rand**: anhand der aktualisierten Werte, dies ist der erwartete Rand von Fehler wie umfangreich die, nachdem alle zusätzlichen Assessment-Dateien überprüft werden.
    
    **Zusätzliche Assessment Dateien erforderlich**: anhand der aktualisierten Werte, die Anzahl der zusätzlichen Assessment Dateien, die zum Erreichen der des Ziels des Vorgangs überprüft werden müssen.
    
    **Insgesamt Assessment Dateien erforderlich**: anhand der aktualisierten Werte, für die Überprüfung erforderliche Assessment Dateien insgesamt.
    
    **Erwartete Anzahl der relevanten Dateien in Assessment**: anhand der aktualisierten Werte, die erwartete Anzahl von relevanten Dateien in der gesamten Bewertung, nachdem alle zusätzlichen Assessment-Dateien überprüft werden.
    
4. Klicken Sie auf die **Werte neu zu berechnen**, wenn Parameter geändert werden. Wenn Sie fertig sind, wenn ein Problem vorliegt, klicken Sie auf **OK** , um die Änderungen (oder **Weiter** , wenn es sind mehrere Probleme überprüfen oder ändern und dann auf **Fertig stellen**) zu speichern. 
    
    Wenn mehrere Probleme vorhanden sind, nachdem alle Probleme überprüft oder korrigiert, wurden eine **Assessment Ebene: Zusammenfassung** Dialogfeld wird angezeigt, wie im folgenden Beispiel dargestellt. 
    
    ![Zusammenfassung der Bewertungsebene](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    Fahren Sie nach dem erfolgreichen Abschluss der Bewertung in die nächste Phase Relevanz Schulung fort.
    
## <a name="reviewing-assessment-results"></a>Überprüfen der Bewertungsergebnisse

Nachdem ein Beispiel zur Bewertung markiert ist, werden die Bewertungsergebnisse zur berechnet und auf der Registerkarte Relevanz nachverfolgen angezeigt.
  
Die folgenden Ergebnisse angezeigt werden im erweiterten Track-Anzeige: 
  
- Schätzt die aktuellen Fehler Seitenrand für den Wiederaufruf Bewertung
    
- Geschätzte Funktionsvielfalt
    
- Zusätzliche Assessment-Dateien (zur Überarbeitung) erforderlich
    
Assessment aktuelle Fehler Rand wird der Fehler Rand von erweiterten eDiscovery empfohlen. Dieser Empfehlung entspricht die Anzahl für "zusätzliche Assessment erforderlichen Dateien" angezeigt.
  
Die Bewertung-Statusanzeige wird der Fertigstellung der Bewertung, erhält den aktuellen Fehler Rand. Wenn der Bewertung aktiviert wird, wird der Benutzer ein weiteres Beispiel für Assessment markieren.
  
Wenn die Statusanzeige Assessment Assessment als abgeschlossen angezeigt wird, bedeutet, dass die Bewertung Beispiel abgeschlossen wurde und ausreichend relevante Dateien markiert wurden. 
  
Erweiterte Track-Anzeige sind empfohlene Nächstes, die Statistiken zur Bewertung und Zugriff auf ausführliche Ergebnisse.
  
Wenn Umfang sehr gering ist, ist die Anzahl der zusätzlichen Assessment Dateien erforderlich, um eine minimale Anzahl von relevanten Dateien nützliche Statistiken zu erreichen sehr hoch. Erweiterte eDiscovery wird dann empfehlen zur Schulung übergeht. Die Statusanzeige Assessment wird grau schattiert dargestellt werden, und keine Statistiken zur Verfügung gestellt. 
  
Keine der Stabilisierung statistisch basiert werden Ergebnisse mit einen geringeren Genauigkeit und Confidence Level. Allerdings können diese Ergebnisse, relevante Dateien zu finden, wenn Sie nicht wissen, den Prozentsatz der relevanten gefundenen Dateitypen müssen verwendet werden. In ähnlicher Weise kann dieser Status verwendet werden zu schulen Probleme mit geringer Funktionsvielfalt, in dem können Relevanz Bewertungen Zugriff auf Dateien an einem bestimmten Problem relevant zu beschleunigen.
  
> [!TIP]
> In der **Relevanz \> nachverfolgen** Registerkarte Erweiterte Problem anzeigen, stehen die folgenden Optionen zum Anzeigen: > den empfohlene nächsten Schritt, z. B. **nächsten Schritt: Tagging** können (pro Problem) umgangen werden, indem Sie auf die Schaltfläche **Ändern** , um dessen rechts, und klicken Sie dann im **nächsten Schritt**Auswählen eines anderen Schritts. Wenn Sie die Statusanzeige Assessment nicht abgeschlossen wurde, müssen zur Bewertung die empfohlene Option zum Markieren von weitere Assessment-Dateien und Statistiken Genauigkeit erhöhen. > Sie können den Rand Fehler ändern und seine Auswirkung bewerten, indem Sie auf **Ändern**, und **Bewertung Ebene Dialogfeld**, das **Ziel Fehler Seitenrand für den Wiederaufruf schätzt**, ändern und auf **Update Werte**. In diesem Dialogfeld können Sie darüber hinaus erweiterte Optionen anzeigen, indem Sie auf **Erweitert**. > Sie können zusätzliche Assessment Ebene Verwendungsstatistiken und deren Einfluss anzeigen, indem Sie auf **Ansicht**. Die angezeigten Ergebnisse Dialogfeld mit den Details stehen in Statistiken pro Problem, wenn mindestens 500 markierte Assessment-Dateien vorhanden sind und mindestens 18 Dateien als Relevant für das Problem markiert sind. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Bewertung in Relevanz](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Kategorien und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden je nach den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

