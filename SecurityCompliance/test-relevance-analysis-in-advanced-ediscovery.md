---
title: Testen von Relevanz Analyse in Office 365 erweiterte eDiscovery
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Erfahren Sie, wie auf die Registerkarte Test nach Batch Berechnung in Office 365 erweiterte eDiscovery verwenden, um zu testen, vergleichen und überprüfen die allgemeine Qualität der Verarbeitung.  '
ms.openlocfilehash: 782859fe3b6bb3d00945c477928131cd1154446d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529470"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a>Testen von Relevanz Analyse in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Die Registerkarte Test in erweiterten eDiscovery können Sie testen, vergleichen und überprüfen die allgemeine Qualität der Verarbeitung. Diese Tests werden nach Batch Berechnung ausgeführt. Durch die Kennzeichnung der Dateien in der Auflistung, wird ein Experte für die abschließende Entscheidung darüber, ob jede markierte Datei tatsächlich für die Groß-/Kleinschreibung relevant ist. 
  
In einzelnen und mehreren Problem Szenarien sind Tests pro Problem in der Regel ausgeführt. Ergebnisse nach jedem Test angezeigt werden können, und Testergebnisse mit angegebenen Test-Beispieldateien überarbeitet werden können.
  
## <a name="testing-the-rest"></a>Testen die restlichen

Der Test "Testen von Rest" wird verwendet, beispielsweise Cullingverfahren Entscheidungen zu überprüfen, um nur Dateien über eine bestimmte Relevanz trennwert Score basierend auf die endgültige erweiterte eDiscovery-Ergebnisse zu überprüfen. Der Experte prüft ein Beispiel für Dateien, die einen ausgewählten trennwert Faktor für die Anzahl der relevanten Dateien innerhalb dieser Gruppe ausgewertet werden soll.
  
Bei diesem Test enthält Statistiken und einen Vergleich zwischen den Satz überprüfen und das Testen die Rest-Auffüllung. Die Ergebnisse der Überprüfung Menge gelten als nach Relevanz während des Trainings berechnet. Die Ergebnisse enthalten Berechnungen, basierend auf Einstellungen und Eingabeparameter, wie beispielsweise:
  
- Testen Sie Beispiel-Statistik der Anzahl von Dateien in einer Beispielcode und identifizierten relevanten Dateien. 
    
- Tabellarische Vergleich der Auffüllung Parameter für die Überprüfung und die restlichen, beispielsweise die Anzahl der Dateien, geschätzte Anzahl der relevanten Dateien, geschätzte Umfang und die durchschnittlichen Kosten eine zusätzliche relevante Datei suchen. Einstellungen für die Kosten-Parameter können vom Administrator festgelegt werden.
    
1. Öffnen der **Relevanz \> Test** Registerkarte. 
    
2. Klicken Sie in der Registerkarte **Testen** auf **neu zu testen**. Klicken Sie im Dialogfeld **Erstellen testen** wird angezeigt, wie im folgenden Beispiel dargestellt. 
    
    ![Relevanztest der REST-Ergebnisse](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. Geben Sie im **Test-Name**und **Beschreibung**den Namen und eine Beschreibung ein.
    
4. Wählen Sie in der Liste **Testtyp** **Test den Rest**
    
5. In der **Problem / Kategorie** , wählen Sie den Namen des Problems. 
    
6. Aktivieren Sie in der Liste **Laden** laden. 
    
7. Akzeptieren Sie in **% Lesen**den Standardwert, oder wählen Sie einen Wert für die trennwert Relevanz Bewertung. 
    
8. In der **Größe festgelegt**oder übernehmen Sie den Standardwert. Beachten Sie, dass die Symbole wiederherstellen die Standardwerte wiederhergestellt werden sollen.
    
9. Klicken Sie auf **Start, markieren**. Ein Beispiel für Test wird generiert.
    
10. Überprüfen Sie, und markieren Sie die Dateien in die **Relevanz \> Tag** Registerkarte, und klicken Sie dann auf **berechnen**.
    
11. In der Registerkarte Test können Sie die **Ergebnisse anzeigen** , um die Testergebnisse finden Sie unter klicken. Ein Beispiel ist in der folgenden Abbildung dargestellt. 
    
    ![REST-Ergebnisse testen](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
In der obigen Abbildung enthält im Abschnitt **Beispiel-Parameter** der Tabelle Details über die Anzahl der Dateien in der Stichprobe mithilfe der Experte markiert und die Anzahl der relevanten Dateien in diesem Beispiel gefunden. 
  
Im Abschnitt **Parameter Auffüllen** der Tabelle enthält die Testergebnisse, einschließlich der Überprüfung Set Auffüllung mit einem Faktor unterhalb der ausgewählten größere Dateien und Auffüllen von Dateien mit einer Bewertung oberhalb der ausgewählten größere "The Rest". Für jede Auffüllung werden die folgenden Ergebnisse angezeigt: 
  
- Enthält die Dateien mit Lesen % - erwähnt Grenzwert
    
- Die Gesamtzahl der Dateien 
    
- Die geschätzte Anzahl der relevanten Dateien 
    
- Die geschätzte Vielfalt 
    
- Die durchschnittliche überprüfen Kosten der Suche nach einem anderen relevanten Datei
    
## <a name="testing-the-slice"></a>Testen das Segment

"Testen des Segments" Test ähnelt dem "Testen der Rest" Testen führt testen, jedoch in der Datei ein Segment festlegen, gemäß Relevanz lesen %.
  
1. Öffnen der **Relevanz \> Test** Registerkarte. 
    
2. Klicken Sie in der Registerkarte **Testen** auf **neu zu testen**. Klicken Sie im Dialogfeld **Erstellen testen** wird angezeigt. 
    
3. Geben Sie im **Test-Name** und **Beschreibung**die Informationen aus.
    
4. Wählen Sie in der Liste **Testtyp** **Test Segments**.
    
5. Wählen Sie in der Liste **Problem** den Problem Namen ein. 
    
6. Aktivieren Sie in der Liste **Laden** laden. 
    
7. **Zwischen % Lesen**akzeptieren Sie die Standardwerte für die unteren und oberen Bereich oder wählen Sie Werte für den trennwert Relevanz Bewertungen. 
    
8. **Festlegen der Größe**wählen Sie einen Wert oder übernehmen Sie den Standardwert.
    
    Den Standardwert werden die Wiederherstellung Symbole wiederhergestellt werden.
    
9. Klicken Sie auf **Start, markieren**. Ein Beispiel für Test wird generiert.
    
10. Überprüfen Sie, und markieren Sie die Dateien in die **Relevanz \> Tag** Registerkarte, und klicken Sie dann auf **berechnen**. 
    
11. In der Registerkarte Test können Sie die **Ergebnisse anzeigen** , um die Testergebnisse finden Sie unter klicken. 
    
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Bewertung in Relevanz](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Kategorien und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Kategorien und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden je nach den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)

