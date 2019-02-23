---
title: Entscheidungen basierend auf den Ergebnissen in Office 365 Advanced eDiscovery
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
ms.assetid: aed65bcd-0a4f-43e9-b5e5-b98cc376bdf8
description: 'Erfahren Sie, wie die Registerkarte "entscheiden" in Office 365 Advanced eDiscovery Daten enthält, die Sie bei der Bestimmung der richtigen Größe der Fall Dateien unterstützen können. '
ms.openlocfilehash: c4767e703d03ef5dbdb808332e873d22094d7bca
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216105"
---
# <a name="decision-based-on-the-results-in-office-365-advanced-ediscovery"></a>Entscheidungen basierend auf den Ergebnissen in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
 In Advanced eDiscovery bietet die Registerkarte entscheiden zusätzliche Informationen zum Anzeigen und Verwenden von Entscheidungs Unterstützungs Statistiken, um die Größe der Fall Dateien zu überprüfen. 
  
## <a name="using-the-decide-tab"></a>Verwenden der Registerkarte "entscheiden"

![Relevanzentscheidung](media/f32fed89-f3b5-404a-90c7-ea25d2eb58a9.png)
  
Diese Registerkarte umfasst Folgendes:
  
- **Problem**: von hier aus können Sie das gewünschte Problem aus der Liste auswählen. 
    
- **Review-Recall Ratio**: Vergleich der erweiterten eDiscovery-Überprüfungen gemäß Relevanz-Bewertungen. Der Grenzpunkt im Diagramm gibt den Prozentsatz der zu überprüfenden Dateien an, die einem Relevanzwert zugeordnet sind. Dies wird in der Relevanz-Testphase und als Export Schwellenwert für das Culling verwendet. Der Standardgrenzwert für die Anzahl der zu überprüfenden Dateien ist der Punkt, an dem das Gleichgewichtzwischen Rückruf und Genauigkeit optimal ist. Der tatsächliche Grenzwert sollte vom Benutzer abhängig von den Zielsetzungen und dem Kostennachteil (% Review) und Risiko (% Recall) bestimmt werden. Mithilfe des Schiebereglers können Sie den Cutoff-Punkt anpassen und die Auswirkungen auf das Diagramm und die Parameter anzeigen, wenn Sie den Prozentsatz der relevanten Dateien, die abgerufen werden sollen, anpassen und bevor Sie eine Entscheidung überprüfen.
    
- **Parameter**: Review, Recall, Next relevant and Total Cost Parameters sind kumulative berechnete Statistiken, die sich auf den Übersichts Satz beziehen, der im Zusammenhang mit der Sammlung für den gesamten Fall gilt. Definitionen für diese Parameter:
    
    **Review**: Prozentsatz der zu überprüfenden Dateien basierend auf diesem Cutoff. 
    
    **Recall**: Prozentsatz der relevanten Dateien im Übersichts Satz. 
    
    **Als nächstes relevant**: Kosten zum Überprüfen und Identifizieren einer zusätzlichen relevanten Datei, die sich derzeit nicht im Übersichts Satz befindet. 
    
    **Gesamtkosten**: Kosten für die Überprüfung dieses Prozentsatzes der Fall Dateien. Einstellungen für Kosten Parameter können vom Fall-Manager festgelegt werden.
    
- **Verteilung nach Relevanz Bewertung**: Dateien in der dunkelgrauen Anzeige Links befinden sich unterhalb der Cutoff-Bewertung. Ein QuickInfo zeigt den Relevanzwert und den zugehörigen Prozentsatz der Dateien in der Übersichtsdatei im Verhältnis zu den Gesamtdateien an.
    
Im erweiterten Detailbereich werden zusätzliche Details angezeigt. Dateien in Sammlungs Abbildungen enthalten keine leeren oder nebligen Dateien. Bei Familiendateien handelt es sich um Dateien, die nicht in Relevanz geladen, aber noch als Teil der Familie gezählt werden.
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Bedeutung der Bewertung](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Tagging und Bewertung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Durchführen von Relevanz-Schulungen](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz-Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Testen der Relevanz-Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

