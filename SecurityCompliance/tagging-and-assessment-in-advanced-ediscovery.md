---
title: Markieren und Beurteilung in Office 365 Advanced eDiscovery
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
ms.assetid: b5c82de7-ed2f-4cc6-becd-db403faf4d18
description: 'Überprüfen Sie die Schritte zur Durchführung von Assessment-Schulungen, einschließlich Taggingdateien, und überprüfen Sie die Ergebnisse der Bewertung in Office 365 Advanced eDiscovery. '
ms.openlocfilehash: 02dae23b6489b40243272beea1d79e871ca6a911
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217935"
---
# <a name="tagging-and-assessment-in-office-365-advanced-ediscovery"></a>Markieren und Beurteilung in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Abschnitt wird das Verfahren für das Modul Advanced eDiscovery Relevance Assessment beschrieben. 
  
## <a name="performing-assessment-training-and-analysis"></a>Durchführen von Assessment-Schulungen und-Analysen

1. Klicken Sie auf der Registerkarte ** \> Relevanz verfolgen** auf **Bewertung** , um die Fall Bewertung zu starten. 
    
    In diesem Verfahren wird beispielsweise ein Beispiel für eine Bewertung von 500-Dateien erstellt, und die Registerkarte **Tag** wird angezeigt, die das Markierungsfeld enthält, die Dateiinhalte und andere Tagging-Optionen angezeigt. 
    
    ![Registerkarte „Relevanztag“ für Bewertung](media/c8acf891-b1cd-4344-816c-eabb8cbbe742.png)
  
2. Überprüfen Sie jede Datei im Beispiel, bestimmen Sie die Relevanz der Datei für jeden Fall Problem, und markieren Sie die Datei mithilfe der Tasten Relevanz (R), nicht relevant (NR) und **** überspringen im Bereich des taggingbereichs. 
    
    > [!NOTE]
    >  Die Bewertung erfordert 500 gekennzeichnete Dateien. Wenn Dateien übersprungen werden, erhalten Sie weitere zu markierende Dateien. 
  
3. Nachdem Sie alle Dateien im Beispiel gekennzeichnet haben, klicken Sie auf **berechnen**. 
    
    Die aktuelle Fehlergrenze und der Umfang der Bewertung werden auf der Registerkarte **Relevanz verfolgen** mit erweiterten Details pro Problem berechnet und angezeigt (siehe unten). Weitere Informationen zu diesem Dialog werden im späteren Abschnitt "überPrüfen der Ergebnisse der Bewertung" beschrieben. 
    
    ![Relevanznachverfolgung – Bewertung](media/da911ba5-8678-40d6-9ad5-fd0b058355c1.png)
  
    > [!TIP]
    > Standardmäßig wird empfohlen, mit dem standardmäßigen nächsten Schritt fortzufahren, wenn die Anzeige des Bewertungs Fortschritts für das Problem abgeschlossen wurde, was darauf hinweist, dass das Bewertungs Beispiel überprüft wurde und ausreichende relevante Dateien markiert wurden. > andernfalls können Sie, wenn Sie die Ergebnisse der Registerkarte " **Spur** " anzeigen und die Fehlergrenze und den nächsten Schritt steuern möchten, auf neben dem **nächsten Schritt** **ändern** klicken, die Option **Bewertung fortsetzen**und dann auf **OK**klicken. 
  
1. Klicken Sie rechts neben dem Kontrollkästchen **Bewertung** auf **ändern** , um Bewertungsparameter pro Problem anzuzeigen und anzugeben. Ein Dialogfeld zur **Beurteilungs Stufe** für jedes Problem wird angezeigt, wie im folgenden Beispiel dargestellt: 
    
    ![Fallproblem mit Bewertungsebene](media/b7113fef-d125-4617-ae1b-c9eb0bf79aec.png)
  
    Die folgenden Parameter für das Problem werden im Dialogfeld Beurteilungs **Stufe** berechnet und angezeigt: 
    
    **Ziel Fehlermarge für Rückruf Schätzungen**: basierend auf diesem Wert wird die geschätzte Anzahl der zu überprüfenden zusätzlichen Dateien berechnet. Der für den Rückruf verwendete Margin-Wert ist größer als 75% und mit einem Konfidenzniveau von 95%. 
    
    **Weitere erforderliche Testdateien**: gibt an, wie viele Dateien erforderlich sind, wenn die Anforderungen des aktuellen Fehler Rands nicht erfüllt sind. 
    
2. So passen Sie den aktuellen Fehler Rand an und sehen die Auswirkungen unterschiedlicher Fehler Ränder (pro Problem):
    
1. Wählen Sie in der Liste **Problem auswählen** ein Problem aus. 
    
2. Geben Sie unter **Ziel Fehlermarge für Rückruf Schätzungen**einen neuen Wert ein.
    
3. Klicken Sie auf **Werte aktualisieren** , um die Auswirkungen der Anpassungen anzuzeigen. 
    
3. Klicken Sie im Dialogfeld **Bewertung** auf **erweitert** , um die folgenden zusätzlichen Parameter und Details anzuzeigen: 
    
    ![Bewertungsebene: erweiterte Ansicht für Fallproblem](media/577d7e0e-95df-48c2-9dec-bdeab5e801d8.png)
  
    **Geschätzte Reichhaltigkeit**: geschätzte Reichhaltigkeit gemäß den aktuellen Bewertungsergebnissen
    
    **Für angenommene Rückrufaktion**: Standardmäßig gilt die Ziel Fehlermarge für den rückruf über 75%. Klicken Sie auf **Bearbeiten** , wenn Sie diesen Parameter ändern und die Fehlergrenze für einen anderen Bereich von Rückruf Werten steuern möchten. 
    
    **Zuverlässigkeitsstufe**: Standardmäßig ist der empfohlene Fehlerbereich für das Vertrauen 95%. Klicken Sie auf **Bearbeiten** , wenn Sie diesen Parameter ändern möchten. 
    
    Erwartete reichhaltige **Fehlermarge**: Angesichts der aktualisierten Werte ist dies der erwartete Fehlerspielraum des Reichtums, nachdem alle zusätzlichen Bewertungsdateien überprüft wurden.
    
    **Erforderliche zusätzliche Analysedateien**: Angesichts der aktualisierten Werte muss die Anzahl zusätzlicher Evaluierungs Dateien, die überprüft werden müssen, um das Ziel zu erreichen.
    
    **Erforderliche Gesamt Beurteilungs Dateien**: Angesichts der aktualisierten Werte sind die Gesamtbewertung für die Überprüfung erforderlichen Dateien erforderlich.
    
    **Erwartete Anzahl der relevanten Dateien in der Bewertung**: Angesichts der aktualisierten Werte wird die erwartete Anzahl von relevanten Dateien in der gesamten Bewertung nachgeprüft, nachdem alle zusätzlichen Bewertungsdateien überprüft wurden.
    
4. Klicken Sie auf **Werte neu berechnen**, wenn Parameter geändert werden. Wenn Sie fertig sind, klicken Sie bei einem Problem auf **OK** , um die Änderungen zu speichern (oder als **nächstes** , wenn mehrere Probleme zu überprüfende oder **** zu ändern sind, und schließen Sie dann). 
    
    Wenn es mehrere Probleme gibt, wird, nachdem alle Probleme überprüft oder angepasst wurden, **** ein Zusammenfassungs Dialogfeld angezeigt, wie im folgenden Beispiel gezeigt. 
    
    ![Zusammenfassung der Bewertungsebene](media/4997b46d-10a5-4abc-b3b2-7b75a370eb9e.png)
  
    Gehen Sie nach erfolgreichem Abschluss der Bewertung zur nächsten Stufe in Relevanz Training.
    
## <a name="reviewing-assessment-results"></a>ÜberPrüfen der Bewertungsergebnisse

Nachdem ein Bewertungs Beispiel markiert wurde, werden die Bewertungsergebnisse berechnet und auf der Registerkarte Relevanz verfolgen angezeigt.
  
Die folgenden Ergebnisse werden in der erweiterten Spuranzeige angezeigt: 
  
- Bewertung aktueller Fehlermarge für Rückruf Schätzungen
    
- Geschätzter Umfang
    
- Erforderliche zusätzliche Evaluierungs Dateien (zur Überprüfung)
    
Die Bewertung Current Error Margin ist der von Advanced eDiscovery Empfohlene Fehler Rand. Die für die "zusätzlichen Assessment-Dateien erforderlich" angezeigte Nummer entspricht dieser Empfehlung.
  
Die Anzeige des Bewertungs Fortschritts zeigt den Grad des Abschlusses der Bewertung bei der aktuellen Fehlergrenze an. Wenn die Bewertung durchgeführt wird, wird ein weiteres Bewertungs Beispiel gekennzeichnet.
  
Wenn die Beurteilungs Fortschrittsanzeige die Bewertung als abgeschlossen anzeigt, ist die Bewertung der Test Beispiel Überprüfung abgeschlossen und ausreichende relevante Dateien wurden markiert. 
  
Die erweiterte Spuranzeige zeigt den empfohlenen nächsten Schritt, die Bewertungsstatistiken und den Zugriff auf detaillierte Ergebnisse.
  
Wenn der Umfang sehr gering ist, ist die Anzahl der zusätzlichen Bewertungsdateien, die erforderlich sind, um eine minimale Anzahl von relevanten Dateien zu erreichen, um nützliche Statistiken zu erstellen, sehr hoch. Advanced eDiscovery empfiehlt dann die Weiterbildung. Die Anzeige für den Fortschrittsstatus wird schattiert angezeigt, und es sind keine Statistiken verfügbar. 
  
Fehlt eine statistisch basierte Stabilisierung, gibt es Ergebnisse mit einer niedrigeren Genauigkeitsstufe und Zuverlässigkeitsstufe. Diese Ergebnisse können jedoch verwendet werden, um relevante Dateien zu finden, wenn Sie den Prozentsatz der gefundenen relevanten Dateien nicht kennen müssen. Auf ähnliche Weise kann dieser Status verwendet werden, um Probleme mit geringem Umfang zu trainieren, bei denen die Relevanz-Ergebnisse den Zugriff auf Dateien beschleunigen können, die für ein bestimmtes Problem relevant sind.
  
> [!TIP]
> Auf der Registerkarte ** \> Relevanz verfolgen** , erweiterte Problemanzeige, sind die folgenden Anzeigeoptionen verfügbar: > der Empfohlene nächste Schritt, wie **Nächster Schritt: Tagging** kann umgangen werden (pro Problem), indem Sie auf die Schaltfläche **ändern** , um die , und wählen Sie dann einen anderen Schritt im **nächsten Schritt**aus. Wenn die Anzeige für den Beurteilungs Fortschritt nicht abgeschlossen ist, ist die Bewertung die nächste empfohlene Option, um mehr Bewertungsdateien zu kennzeichnen und die Genauigkeit der Statistiken zu verbessern. > Sie können den Fehler Rand ändern und seine Auswirkungen bewerten, indem Sie auf **ändern**klicken und im **Dialogfeld Beurteilungs Stufe**den **Ziel Fehlerbereich für Rückruf Schätzungen**ändern und auf **Werte aktualisieren**klicken. Außerdem können Sie in diesem Dialogfeld Erweiterte Optionen anzeigen, indem Sie auf **erweitert**klicken. > Sie können zusätzliche Statistiken zum Bewertungs Level und deren Auswirkungen anzeigen, indem Sie auf **Ansicht**klicken. Im Dialogfeld Detail Ergebnisse angezeigt werden Statistiken pro Problem zur Verfügung gestellt, wenn mindestens 500 markierte Bewertungsdateien vorhanden sind und mindestens 18 Dateien für das Problem relevant sind. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Bedeutung der Bewertung](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Tagging-und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz-Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden basierend auf den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz-Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

