---
title: Verstehen von Relevanz in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: Hier erhalten Sie einen Überblick über die Bewertungsstufe und ihre Rolle bei der Ermittlung der reichhaltigen Probleme beim Relevanz-Training in Office 365 Advanced eDiscovery.
ms.openlocfilehash: 1ddaa7ef37f762d7b63bb6c0c51193ff382b8d6b
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32250202"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a>Verstehen von Relevanz in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Advanced eDiscovery ermöglicht eine frühe Bewertung, beispielsweise für die definierten Probleme und die für einen Fall importierten Daten. Advanced eDiscovery ermöglicht es dem Experten, Entscheidungen über eine angenommene Vorgehensweise zu treffen und diese auf das Dokument Übersichts Projekt anzuwenden.
  
## <a name="understanding-assessment"></a>Grundlegendes zur Bewertung

In der Bewertung prüft der Experte eine zufällige Gruppe von mindestens 500-Dateien, die verwendet werden, um die Reichhaltigkeit der Probleme zu bestimmen und um Statistiken zu erstellen, die die Trainingsergebnisse widerspiegeln. Die Bewertung ist erfolgreich, wenn genügend relevante Dateien gefunden werden, um einen statistischen Grad zu erreichen, der die FortgeSchrittene eDiscovery-Relevanz für genaue Statistiken und zur effektiven Bestimmung des Stabilisierungs Punkts im Schulungsprozess unterstützt. 
  
Je höher die Anzahl der relevanten Dateien in der Bewertung ist, desto genauer sind die Statistiken und die Effektivität des Stabilitäts Algorithmus. Die Anzahl der relevanten Dateien in den Evaluierungs Dateien hängt vom Umfang des Problems ab. Reichtum ist der geschätzte Prozentsatz der relevanten Dateien in der Gruppe, die für ein Problem relevant ist. Probleme mit höherer Reichweite erreichen eine höhere Anzahl von relevanten Dateien schneller als Probleme mit geringem Umfang. Probleme mit extrem geringem Reichtum (beispielsweise 2% oder weniger) erfordern eine sehr umfangreiche Bewertung, um eine beträchtliche Anzahl von relevanten Dateien zu erreichen.
  
Die Statistiken, die während des Trainings und nach der Batch Berechnung auf den Registerkarten "Titel" und "Entscheidung" angezeigt werden, enthalten Schätzungen des Rückrufs für verschiedene Übersichts Sätze. In Statistiken sind Schätzungen, die auf einer Beispiel Gruppe basieren (in diesem Fall die Bewertungsdateien), die Fehlertoleranz und die Zuverlässigkeitsstufe dieses fehlerbereichs. Beispielsweise kann der geschätzte Rückruf von 80% einen Fehlerwert von Plus oder minus 5% mit einer Konfidenz Stufe von 95% aufweisen. Dies bedeutet, dass der geschätzte Rückruf tatsächlich 75%-85% ist und diese Schätzung 95% vertrauenswürdig ist. Je größer der Bewertungs Satz ist, desto geringer ist der Fehlerspielraum, und die Statistiken sind genauer. 
  
Nachdem der Experte einen anfänglichen Bewertungs Satz von 500-Dateien überprüft hat, kann die Relevanz den aktuellen Fehler Rand der Rückruf Werte bestimmen. Relevanz wird auch einen standardmäßigen Fehler Rand festlegen, der zur Optimierung des Bewertungs Satzes empfohlen wird. Es folgen einige Beispiele:
  
- Wenn für den assessmentsatz bereits eine Fehlergrenze von Plus oder minus 10% vorliegt, wird empfohlen, zur Schulung zu wechseln (es ist keine zusätzliche Bewertung erforderlich). 
    
- Wenn der Beurteilungs Satz eine Fehlergrenze von Plus oder minus 13% ergab, kann die Relevanz die Überprüfung eines anderen Satzes von Bewertungsdateien empfehlen, um einen geringeren Seitenrand zu erreichen. 
    
- Wenn der Umfang äußerst gering ist, empfiehlt es sich möglicherweise, die Bewertung zu beenden, obwohl die Fehlergrenze hoch ist (Statistiken sind nicht praktikabel), da die zum Erreichen einer nützlichen Fehlergrenze erforderliche Bewertung zu umfangreich ist.
    
Jedes Problem hat seinen eigenen Umfang, den aktuellen Fehlerspielraum und als Ergebnis die geschätzte Anzahl zusätzlicher Evaluierungs Dateien. Der nächste Bewertungs Satz wird entsprechend der maximalen Anzahl von Dateien (bis zu 1.000 in einem einzelnen Satz) erstellt.
  
Sie können die Relevanz-Empfehlungen akzeptieren oder den aktuellen Fehlerspielraum gemäß Ihren Anforderungen anpassen. Der standardmäßige aktuelle Fehler ist für den Rückruf bei gleich oder über 75% bestimmt.
  
> [!NOTE]
> Die Bewertungsstufe kann auf der Registerkarte ** \> Relevanz verfolgen** in der erweiterten Ansicht für ein Problem umgangen werden, indem das Kontrollkästchen **Bewertung** pro Problem und dann für alle Probleme deaktiviert wird. Daher gibt es für dieses Problem keine Statistiken. > das Kontrollkästchen **Bewertung** kann nur ausgeführt werden, bevor die Bewertung durchgeführt wird. Wenn in einem Fall mehrere Probleme vorhanden sind, wird die Bewertung nur umgangen, wenn das Kontrollkästchen für jedes Problem deaktiviert ist. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Tagging und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Tagging-und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz-Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden basierend auf den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz-Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

