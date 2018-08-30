---
title: Entscheidung basierend auf den Ergebnissen in Office 365 erweiterte eDiscovery
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
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Hier erfahren Sie, wie die Registerkarte Decide in Office 365 erweiterte eDiscovery, dass Daten, die Ihnen dabei helfen, die richtige Größe der Menge der Groß-/Kleinschreibung Dateien überprüfen bestimmen. '
ms.openlocfilehash: 58a181e00ad5843ccbbde4dcb47050eccf199225
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529166"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a>Entscheidung basierend auf den Ergebnissen in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
 In erweiterten eDiscovery bietet die Registerkarte Decide zusätzliche Informationen zum Anzeigen und Verwenden von Decision Support-Statistiken zum Bestimmen der Größe der Menge der Groß-/Kleinschreibung Dateien überprüfen. 
  
## <a name="using-the-decide-tab"></a>Mithilfe der Registerkarte Decide

![Relevanzentscheidung](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
Auf dieser Registerkarte umfasst Folgendes:
  
- **Problem**: Hier können Sie das Problem von Interesse aus der Liste auswählen. 
    
- **Überprüfung-Rückruf Verhältnis**: Erweiterte Vergleich von eDiscovery-Überprüfung nach Relevanz Bewertungen. Der Grenzwert Punkt im Diagramm stellt den Prozentsatz der Dateien, um zu prüfen, einen Faktor Relevanz zugeordnet. Dies ist die Relevanz Testphase und als ein Export Schwellenwert für culling verwendet. Der standardmäßige trennwert Punkt für die Anzahl der Dateien, um zu prüfen wird an der Stelle, in dem das Gleichgewicht zwischen Rückruf und Precision optimal ist. Der tatsächliche trennwert Punkt sollte vom Benutzer je nach Zielen und die Kosten Kompromiss (% Überarbeitung) und das Risiko (% Rückruf) bestimmt werden. Verwenden den Schieberegler, können Sie den trennwert Punkt anpassen und finden Sie unter Auswirkungen auf das Diagramm und die Parameter, wenn Sie den Prozentsatz der relevanten Dateien abgerufen werden sollen, und vor dem Überprüfen einer Entscheidung anpassen.
    
- **Parameter**: Lesen, denken Sie daran, nächste relevant und Gesamtkosten-Parameter sind kumulative berechnete Statistiken für die Überprüfung in Bezug auf die Auflistung für die gesamte Groß-/Kleinschreibung festgelegt. Definitionen für diese Parameter sind wie folgt:
    
    **Überprüfen**: Prozentsatz der Dateien überprüfen basierend auf dieser Grenzwert. 
    
    **Denken Sie daran**: Prozentsatz der entsprechenden Dateien in der Gruppe überprüfen. 
    
    **Nächsten relevanten**: Kosten, um zu prüfen, und identifizieren eine zusätzliche relevante Datei, die bei der Überprüfung zurzeit nicht festgelegt ist. 
    
    **Gesamtkosten**: Kosten für die Überprüfung dieser Prozentsatz der Groß-/Kleinschreibung-Dateien. Von der Groß-/Kleinschreibung Manager können Einstellungen für die Kosten Parameter festgelegt werden.
    
- **Verteilung relevanzbewertung**: Dateien in die dunklen Grau Anzeige auf der linken Seite unterhalb der trennwert Score sind. Eine QuickInfo zeigt die Relevanz Bewertung und der zugehörigen Prozentsatz der Dateien in die Überprüfungsdatei in Bezug auf die Gesamtzahl der Dateien festgelegt.
    
Erweiterte Detailbereich werden weitere Details angezeigt. Dateien in der Auflistung Zahlen enthalten nicht leere ist oder unspezifisch Dateien. Produktfamilie Dateien Zahlen darstellen, Dateien, die nicht im Relevanz geladen, aber weiterhin im Rahmen der Produktfamilie gezählt.
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Bewertung in Relevanz](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Kategorien und Bewertung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Ausführen der Relevanz-Schulung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Testen der Relevanz Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

