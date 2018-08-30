---
title: Verwenden Sie das Modul Relevanz in Office 365 erweiterte eDiscovery
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: 'Lernen Sie das Modul Relevanz in Office 365 erweiterte eDiscovery, einschließlich eines Workflows und Richtlinien und Schritte zur Schulung und Datei überprüfen.  '
ms.openlocfilehash: 2cf75ef95291c5393367ce01fb0cd660f9b99145
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529212"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a>Verwenden Sie das Modul Relevanz in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Erweiterte eDiscovery enthält das Modul Relevanz der Relevanz Schulung und Überprüfung von Dateien im Zusammenhang mit der Fall. Der Relevanz Workflow wird angezeigt und wie folgt beschrieben:
  
![Relevanzworkflow](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- **Zyklen der Bewertung und Nachverfolgen von Änderungen**:
    
  - **Assessment**: Erweiterte eDiscovery ermöglicht frühe Assessment basierend auf einer Stichprobe von Dateien und wird mit dieser Bewertung Entscheidungen, die Leistung der vorhersehbare Codierung bestimmen angewendet. 
    
  - **Titel**: Erweiterte eDiscovery berechnet und anzeigt Zwischenergebnisse der Bewertung bei der Überwachung statistische Gültigkeit des Prozesses. 
    
- **Zyklen Schulung und Nachverfolgen von Änderungen**:
    
  - **Tag**: Erweiterte eDiscovery lernen Relevanz Kriterien speziell für jedes Problem basierend auf der Experte iterative überprüfen und Kategorien der einzelnen Dateien.
    
  - **Titel**: Erweiterte eDiscovery berechnet und anzeigt Zwischenergebnisse der Schulung Relevanz bei der Überwachung statistische Gültigkeit des Prozesses. 
    
- **Batch-Berechnung**: Erweiterte eDiscovery übernimmt die kumulierte und gelernten Relevanz Kriterien, betrifft die gesamte Dateisammlung und Relevanz der Ergebnisse für jede Datei generiert.
    
- **Decide**: Erweiterte eDiscovery zeigt die Ergebnisse der Analyse auf die gesamte Groß-/Kleinschreibung nach Batch Berechnung angewendet, und zeigt die Daten für das Dokument überprüfen Entscheidung.
    
- **Test**: Erweiterte eDiscovery-Suchergebnissen zum Überprüfen der Gültigkeit und Effektivität der eDiscovery-erweiterte Verarbeitung getestet werden können.
    
## <a name="guidelines-for-relevance-training-and-review"></a>Richtlinien für die Relevanz Schulung und überprüfen

Es folgt eine Übersicht über Richtlinien für die Relevanz Schulung und überprüfen:
  
- **Fehler und Inkonsistenzen**: Kategorien Fehler während des Trainings vorgenommen wurde, kehren Sie zur vorherigen Datei herunter, die zu korrigieren. Wenn aufgrund zu vieler Fehler an den richtigen vorhanden sind, oder es eine neue Perspektive der Groß-/Kleinschreibung oder Problem ist, die Relevanz Kriterien sollten vom Administrator neu definiert werden, und die Relevanz Schulung neu gestartet.
    
- **Tag und Schulung**: 
    
  - Dateien sollten basierend auf dem Inhalt nur markiert werden. Metadaten wie der Verwaltungsberechtigte, Datum oder Dateipfad nicht berücksichtigt. 
    
  - Berücksichtigen Sie den Datum nicht Bereich Angaben im Text beim Markieren von Dateien.
    
  - Berücksichtigt beim Markieren von Dateien keine eingebettete Grafiken.
    
  - Wenn eine Datei in das Symbol **formatierten Textansicht** beim tagging anzeigen, die Formatierung von Text nicht berücksichtigt. Beispielsweise wird ein Wort durchgestrichen (eine horizontale Linie durch seine Mitte, der angibt, löschen) nach Relevanz als Teil der analysierten Text weiterhin betrachtet. 
    
  - Ignorieren angewendetem zur Relevanz (gemäß Festlegung von der Groß-/Kleinschreibung Manager oder Administrator) Text wird in der Relevanz in der angezeigten Datei in der Textansicht entfernt. Wenn die Werte für Text ignorieren nach Relevanz Schulung bereits Schritte definiert wurden, wird der neue Text ignorierte auf Beispieldateien aus den Punkt in dem er definiert wurde erstellt angewendet werden. Das Feature Text ignorieren sollte mit Bedacht, verwendet werden, da die Verwendung die Leistung von Dateianalyse verringern kann
    
  - Verwenden Sie die **Überspringen tagging** Option nur bei Bedarf. Erweiterte eDiscovery wird nicht basierend auf Übersprungene Dateien Schulen. Bewertung, wenn es schwierig ist, sagen, ob eine Datei relevant ist ist es besser, Tag als Relevant (R) oder nicht relevant (Nr.) nach Möglichkeit statt **Überspringen**auswählen. Wenn erweiterte eDiscovery Training ausgewertet wird, kann diese klicken Sie dann wie gut diese Dateitypen verarbeitet wurden angezeigt werden.
    
  - Selbst Dateien, die mit einer sehr geringen extrahierte Text sollte in Schulung nicht als "Überspringen", wenn möglich, sondern als R/Nr. markiert werden. 
    
  - Kategorien, kann die Klassifizierung auswirken, solange die Datei gelesen werden kann und als R/Nr. markiert werden kann.
    
  - Die Datei Sequenznummer in der angezeigten Liste der Beispiel-Dateien auf der Registerkarte **Tag** ermöglicht es dem Benutzer wieder an die ursprüngliche Reihenfolge der Dateien angezeigt. 
    
  - Können Sie zurück zur Beispiele, und ändern Sie die Kennzeichnung der Bewertung und Schulung Dateien festgelegt. Beim Erstellen von im nächsten Beispiels werden die Änderungen angewendet.
    
  - Überprüften Excel, die Dateien im PDF-Format müssen behandelt als systemeigene Excel-Dateien beim Markieren von Dateien.
    
  - Wenden Sie im unsicheren bezüglich der Relevanz Markieren einer Datei sich an einen Experten. Falsche Kategorien während der Relevanz Schulung kann dazu führen, dass später im Vorgang Verlust von Zeit und möglicherweise auch eine negative Auswirkung auf die Qualität der Gesamtergebnisse.
    
  - Schlüsselwörter, die definiert wurden in-Schlüsselwort werden in Farben, um die relevante Dateien während tagging identifizieren Benutzerhilfe Listen angezeigt werden.
    
- **Batch-Berechnung**: Dateien, die markiert wurden, erhalten diese R/Nr. mithilfe der Experte eine integritätsbewertung von 0 und 100. Dies gilt für tagging vor dem Batch Berechnung vorgenommen. Wenn der Experte das Problem im Leerlauf nach Batch Berechnung gewechselt und Fortsetzung dieses Problem markieren, werden die neu markierten Faktoren nicht 100/0, sondern vielmehr die ursprüngliche Bewertung.
    
- **Probleme und sampling Modus**: Probleme werden in der Regel deaktiviert, wenn Arbeit abgeschlossen ist (Relevanz Schulung ist konstant und Batch Berechnung ausgeführt wurde), wenn die Probleme abgebrochen werden, oder wenn ein anderer Benutzer die Fragen funktionsfähig ist.
    
## <a name="steps-in-relevance-training"></a>Schritte im Relevanz-Schulung

In der **Relevanz \> nachverfolgen** Registerkarte Erweiterte eDiscovery Leitfaden zur Vorgehensweise bei der Verarbeitung, mit den folgenden Schritten weiter. Bei jeder der folgenden Schritte im Prozess Schulung Relevanz empfohlen wird, werden die Auswirkungen nachfolgend beschrieben. 
  
- Markieren / Continue-tagging: Datei überprüfen und die Relevanz tagging durchgeführte Experte für jede Datei und Problem innerhalb einer Stichprobe.
    
  - Implikation: Vorhandenen Beispiels markiert werden muss.
    
- Bewertung / Continue-Bewertung: ermöglicht frühe Validierung von Groß-/Kleinschreibung Problem Relevanz und eine vorläufige Ansicht der Relevanz von der Datei Auffüllung für die aktuelle Groß-/Kleinschreibung importiert.
    
  - Implikation: Weitere Bewertung erforderlich oder empfohlen.
    
- Schulung / Continue-Training: Prozess während der erweitert eDiscovery vom Experten, die die Datei tagging ist lernen Beispiele und erhält die Möglichkeit zum Identifizieren der Relevanz Kriterien für jedes Problem im Kontext des Einzelfall relevant sind.
    
  - Implikation: Das Problem Bedarf weitere Schulungen. Im nächste Beispiel sollte erstellt und markiert werden. 
    
- Batch-Berechnung: Relevanz Prozess in welche erweitert eDiscovery nimmt die während der Phase der Schulung erworbene Kenntnisse und die gesamte Datei Auffüllung betrifft. Alle Dateien in der Dateigruppe relevanten sind für Relevanz bewertet und einen Faktor Relevanz zugewiesen.
    
  - Implikation: Das Problem hat konstant und Batch Berechnung ausgeführt werden kann.
    
- Synchronisieren: Relevanz gibt an, wann ein Experte überprüft und tags eine Stichprobe Dateien aus Laden einer zusätzlichen Datei ausgewählt, während ein Szenario lädt Gang (engl.).
    
  - Implikation: Eine neue Last wurde hinzugefügt, und synchronisieren weiterzuarbeiten erforderlich ist.
    
- Markieren von Inkonsistenzen: Prozess identifiziert, über eine erweiterte eDiscovery-Algorithmus Inkonsistenzen in der Datei tagging-Prozess, die sich negativ auf die Analyse auswirken können.
    
  - Implikation: Im nächste Beispiel enthält Dateien, die markiert wurden in den vorherigen Beispielen und deren tagging muss wiederhergestellt werden.
    
- Aktualisieren der Klassifizierung: ermöglicht dem Benutzer das tagging oder seeding Änderungen anwenden.
    
  - Implikation: Kategorien und seeding Änderungen können angewendet werden ohne ein weiteres Beispiel der Relevanz manuell ausführen.
    
- In der Warteschleife: die Relevanz Training abgeschlossen ist.
    
  - Implikation: Keine Relevanz Schulung ist erforderlich, zu diesem Zeitpunkt.
    
Obwohl erweiterte eDiscovery Sie durch den Prozess mit weitere Schritte in verschiedenen Phasen empfohlen führt, außerdem können Sie zwischen den Seiten und Registerkarten navigieren und Auswahlmöglichkeiten für Situationen vornehmen, die für Ihre Einzelfall Problem relevant sind möglicherweise oder Überprüfung des Dokuments. 
  
Es ist möglich, übernehmen oder erweiterte eDiscovery Nächstes Verarbeitung Auswahlmöglichkeiten überschreiben. Wenn Sie möchten, führen Sie einen Schritt als Nächstes empfohlen, klicken Sie auf der **nächste Schritt** in der erweiterten Problem Anzeige im Dialogfeld aufgeführt, klicken Sie auf die Schaltfläche **Ändern** neben im nächsten Schritt, und wählen Sie eine andere Option für nächsten Schritt. 
  
> [!NOTE]
> Einige Optionen bleiben deaktivierte nach entsperren, wie sie für die Verwendung im Prozess zu diesem Zeitpunkt nicht unterstützt werden. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Bewertung in Relevanz](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Kategorien und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Kategorien und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden je nach den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

