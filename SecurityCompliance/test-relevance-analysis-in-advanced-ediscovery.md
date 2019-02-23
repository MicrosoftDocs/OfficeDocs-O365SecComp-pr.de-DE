---
title: Testen der Relevanzanalyse in Office 365 Advanced eDiscovery
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
ms.assetid: 1b092f7c-ea55-44f5-b419-63f3458fd7e0
description: 'Erfahren Sie, wie Sie die Registerkarte Test nach der Batch Berechnung in Office 365 Advanced eDiscovery verwenden, um die allgemeine Verarbeitungsqualität zu testen, zu vergleichen und zu validieren.  '
ms.openlocfilehash: 735a6d8088b4696e2ebc348db435a11914bd0b10
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215835"
---
# <a name="test-relevance-analysis-in-office-365-advanced-ediscovery"></a>Testen der Relevanzanalyse in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Auf der Registerkarte Test in Advanced eDiscovery können Sie die allgemeine Verarbeitungsqualität testen, vergleichen und überprüfen. Diese Tests werden nach der Batch Berechnung durchgeführt. Durch das Taggen der Dateien in der Auflistung trifft ein Experte das abschließende Urteil darüber, ob jede markierte Datei tatsächlich für den Fall relevant ist. 
  
In Szenarios mit mehreren Problemen werden in der Regel Tests pro Problem durchgeführt. Ergebnisse können nach jedem Test angezeigt werden, und Testergebnisse können mit angegebenen Beispiel Testdateien überarbeitet werden.
  
## <a name="testing-the-rest"></a>Testen des Rests

Der Test "Test the Rest" dient zum Überprüfen von Entscheidungen zum Abschneiden, beispielsweise zur Überprüfung von Dateien, die auf den letzten erweiterten eDiscovery-Ergebnissen basieren. Der Experte prüft ein Beispiel von Dateien unter einer ausgewählten Cutoff-Bewertung, um die Anzahl der relevanten Dateien innerhalb dieser Gruppe zu bewerten.
  
Dieser Test bietet Statistiken und einen Vergleich zwischen dem überPrüfungs Satz und dem Test der Rest-Auffüllung. Die Ergebnisse des Übersichts Satzes werden anhand der Relevanz während des Trainings berechnet. Die Ergebnisse sind Berechnungen, basierend auf Einstellungen und Eingabeparametern, wie zum Beispiel:
  
- Testen Sie die Beispiel Statistiken zur Anzahl der Dateien in einem Beispiel, und ermitteln Sie die relevanten Dateien. 
    
- Tabellarischer Vergleich der Populations Parameter des Übersichts Satzes und des Rests, beispielsweise der Anzahl von Dateien, der geschätzten Anzahl der relevanten Dateien, des geschätzten Umfangs und der durchschnittlichen Kosten für die Suche nach einer zusätzlichen relevanten Datei. Einstellungen für Kosten Parameter können vom Administrator festgelegt werden.
    
1. Öffnen Sie die Registerkarte **Relevanz \> testen** . 
    
2. Klicken Sie auf der Registerkarte **Test** auf **neuer Test**. Das Dialogfeld **Test erstellen** wird angezeigt, wie im folgenden Beispiel gezeigt. 
    
    ![Relevanztest der REST-Ergebnisse](media/46e6898a-f929-4fd0-88d9-6f91d04b6ce2.png)
  
3. Geben **** Sie unter Testname und **Beschreibung**den Namen und die Beschreibung ein.
    
4. Wählen Sie **** in der Liste Testtyp **die Option Rest testen** aus.
    
5. Wählen Sie in der Liste **Problem/Kategorie** den Problem Namen aus. 
    
6. Wählen Sie in der Liste **Laden** die Option Laden aus. 
    
7. Übernehmen Sie in **% Lesen**den Standardwert, oder wählen Sie einen Wert für das Cutoff-Relevanz-Ergebnis aus. 
    
8. , **** Oder übernehmen Sie den Standardwert. Beachten Sie, dass die Wiederherstellungs Symbole die Standardwerte wiederherstellen.
    
9. Klicken Sie auf **Tagging starten**. Ein Test Beispiel wird generiert.
    
10. Überarbeiten und markieren Sie die einzelnen Dateien auf der Registerkarte ** \> relevanztag** , und klicken Sie anschließend auf **berechnen**.
    
11. Auf der Registerkarte Test können Sie auf **Ergebnisse anzeigen** klicken, um die Testergebnisse anzuzeigen. Ein Beispiel ist in der folgenden Abbildung dargestellt. 
    
    ![REST-Ergebnisse testen](media/b95744a9-047d-4c29-992d-04fa7e58e58a.png)
  
In der obigen Abbildung enthält der Abschnitt **Beispiel Parameter** der Tabelle Details zur Anzahl der Dateien im Beispiel, die vom Experten gekennzeichnet wurden, und die Anzahl der relevanten Dateien, die in diesem Beispiel gefunden wurden. 
  
Der Abschnitt " **Population Parameters** " der Tabelle enthält die Testergebnisse, einschließlich der Überprüfung festgelegten Anzahl von Dateien mit einer Punktzahl unter dem ausgewählten Grenzwert und der "Rest"-Auffüllung von Dateien mit einer Bewertung über dem ausgewählten Grenzwert. Für jede Auffüllung werden die folgenden Ergebnisse angezeigt: 
  
- Enthält Dateien mit dem Read%-Grenzwert
    
- Die Gesamtzahl der Dateien 
    
- Die geschätzte Anzahl der relevanten Dateien 
    
- Die geschätzte Reichhaltigkeit 
    
- Die durchschnittlichen Überprüfungen der Suche nach einer anderen relevanten Datei
    
## <a name="testing-the-slice"></a>Testen des Segments

Der Test "Slice testen" führt Tests ähnlich dem Test "Test the Rest" durch, jedoch auf ein Segment der Dateigruppe gemäß der Relevanz Read%.
  
1. Öffnen Sie die Registerkarte **Relevanz \> testen** . 
    
2. Klicken Sie auf der Registerkarte **Test** auf **neuer Test**. Das Dialogfeld **Test erstellen** wird angezeigt. 
    
3. Geben **** Sie im Feld Testname und- **Beschreibung**die Informationen ein.
    
4. Wählen Sie **** in der Liste Testtyp **die Option Slice testen**aus.
    
5. Wählen Sie in der Liste **Problem** den Problem Namen aus. 
    
6. Wählen Sie in der Liste **Laden** die Option Laden aus. 
    
7. Übernehmen **Sie in% zwischen gelesen**die Standardwerte niedrig und hoch, oder wählen Sie Werte für die Ergebnisse der Cutoff-Relevanz aus. 
    
8. Wählen Sie unter **festGelegte Größe**einen Wert aus, oder übernehmen Sie den Standardwert.
    
    Die Wiederherstellungs Symbole stellen den Standardwert wieder her.
    
9. Klicken Sie auf **Tagging starten**. Ein Test Beispiel wird generiert.
    
10. Überarbeiten und markieren Sie die einzelnen Dateien auf der Registerkarte ** \> relevanztag** , und klicken Sie anschließend auf **berechnen**. 
    
11. Auf der Registerkarte Test können Sie auf **Ergebnisse anzeigen** klicken, um die Testergebnisse anzuzeigen. 
    
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Bedeutung der Bewertung](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Tagging und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Tagging-und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz-Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden basierend auf den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)

