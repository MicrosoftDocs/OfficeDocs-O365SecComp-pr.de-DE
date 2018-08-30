---
title: Grundlegendes zu Assessment in Relevanz in Office 365 erweiterte eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 1d33d4fb-91ed-41c0-b72e-5a26eca3a2a7
description: 'Rufen Sie eine Übersicht über die Bewertungsphase und seiner Rolle bei der Bestimmung der Umfang der Probleme während der Relevanz Schulung in Office 365 erweiterte eDiscovery.  '
ms.openlocfilehash: a54a4134609b16568586f3cb6b60ebdeba860bac
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529461"
---
# <a name="understand-assessment-in-relevance-in-office-365-advanced-ediscovery"></a>Grundlegendes zu Assessment in Relevanz in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Erweiterte eDiscovery ermöglicht frühe Bewertung, beispielsweise für die definierten Probleme und die Daten für eine Anfrage importiert. Erweiterte eDiscovery ermöglicht den Experten für einen angenommene Ansatz Entscheidungen treffen Sie auf Überprüfung Dokumentprojekt anwenden.
  
## <a name="understanding-assessment"></a>Grundlegendes zur Bewertung

Bewertung überprüft der Experte einen zufällig ausgewählten Satz von mindestens 500-Dateien, die verwendet werden, um den Umfang der Probleme zu ermitteln und Statistiken zu erstellen, die die Schulung Ergebnisse widerspiegeln. Assessment ist erfolgreich, wenn genügend relevanten Dateien gefunden werden, ein statistische Niveau erreicht, die erweiterte eDiscovery Relevanz genaue Statistiken bereitstellen und tatsächlich die Stabilisierung Stelle der Schulung bestimmen helfen. 
  
Je höher die Anzahl der relevanten in die Bewertung festgelegt sind, desto genauer die Statistiken und die Effektivität des Algorithmus Stabilität Dateien. Die Anzahl der relevanten Dateien innerhalb der Bewertung Dateien hängt vom Umfang des Problems. Wie umfangreich ist der geschätzte Prozentsatz der entsprechenden Dateien in der Gruppe für ein Problem relevant. Probleme mit einer höheren Funktionsvielfalt werden eine größere Anzahl von relevanten Dateien schneller als Probleme mit niedrigeren Funktionsvielfalt erreichen. Probleme mit sehr niedrige Funktionsvielfalt (beispielsweise 2 % oder weniger) erfordern eine sehr große Bewertung gesetzt, um eine beträchtliche Anzahl von relevanten Dateien zu.
  
Die Statistiken, die in den Registerkarten nachverfolgen und Decide während der Schulung und nach der Batch Berechnung vorgelegt werden, umfassen Abschätzung der Rückruf für verschiedene Überprüfung festgelegt. Innerhalb der Statistik, Einschätzung, die auf einer Stichprobe basieren festgelegt (in diesem Fall die Assessment-Dateien) enthalten, dem der Fehler und die Vertrauensstufe der jeweilige Fehler Rand. Beispielsweise möglicherweise geschätzte Rückruf 80 % Rand Fehler von Plus oder minus 5 % mit einer Vertrauensstufe von 95 %. Dies bedeutet, dass der geschätzte Rückruf ist tatsächlich 75-85 % dieser Schätzung 95 % Confidence hat. Je größer der Bewertung festgelegt, wird des Rands des Fehlers kleiner und die Statistiken verständlich sind. 
  
Nachdem der Experte eine erste Einschätzung Menge von 500 Dateien überprüft, kann Relevanz den aktuellen Rand von Fehler der Rückruf Werte zu bestimmen. Relevanz wird auch einen standardmäßigen Rand des Fehlers festgelegt, die es empfiehlt erreichen, um die Bewertung zu optimieren. Es folgen einige Beispiele:
  
- Wenn die Bewertung bereits einen Rand des Fehlers von Plus oder minus 10 % bereitgestellt wurde, wird Relevanz wird empfohlen, zu Schulungen verschieben, klicken Sie auf (keine zusätzliche Bewertung ist erforderlich). 
    
- Wenn der Bewertung Satz einen Rand des Fehlers von Plus oder minus 13 % brachte, möglicherweise Relevanz wird die Überprüfung von einem anderen Satz von Assessment Dateien in einen kleineren Rand erreichen empfohlen. 
    
- Wenn Funktionsvielfalt sehr gering ist, wird Relevanz möglicherweise empfehlen Assessment stoppen, obwohl der Rand des Fehlers (wobei Statistiken nicht praktikabel) groß ist, da festgelegten Assessment benötigt, um eine nützliche Rand von Fehler zu erreichen ist zu groß.
    
Jedes Problem verfügt über eine eigene Funktionsvielfalt, aktuellen Rand von Fehler, und daher geschätzte Anzahl der zusätzliche Assessment-Dateien. Der nächste Satz Assessment wird entsprechend die maximale Anzahl von Dateien (bis zu 1.000 in einem einzigen Satz) erstellt.
  
Können Sie die Relevanz Empfehlungen akzeptieren oder den aktuellen Rand von Fehler entsprechend Ihren Anforderungen anpassen. Der aktuellen standardmäßigen Rand des Fehlers wird für den Wiederaufruf gleich mindestens 75 % bestimmt.
  
> [!NOTE]
> Die Phase Assessment kann umgangen werden, in der **Relevanz \> nachverfolgen** Registerkarte in der erweiterten Ansicht für ein Problem, indem Sie das Kontrollkästchen **Assessment** pro Problem, und klicken Sie dann für "alle Probleme" deaktivieren. Dementsprechend, werden es jedoch keine Statistiken für dieses Problem. > Deaktivieren des Kontrollkästchens **Assessment** kann nur ausgeführt werden, bevor Assessment ausgeführt wird. In dem Fall mehrere Probleme vorhanden sind, wird zur Bewertung umgangen nur, wenn das Kontrollkästchen für jedes Problem deaktiviert ist 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Kategorien und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Kategorien und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden je nach den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

