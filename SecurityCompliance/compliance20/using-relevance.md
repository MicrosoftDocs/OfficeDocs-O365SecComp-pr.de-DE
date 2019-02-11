---
title: Verwenden Sie das Modul Relevanz zum Analysieren von Daten in erweiterten eDiscovery (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 56e83a1f8a951fd6e14172122a5e86447c6f2ccf
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29695171"
---
# <a name="use-the-relevance-module-to-analyze-data-in-advanced-ediscovery-preview"></a>Verwenden Sie das Modul Relevanz zum Analysieren von Daten in erweiterten eDiscovery (Preview)

Erweiterte eDiscovery (Preview) enthält das Modul Relevanz der Relevanz Schulung und Überprüfung von Dateien im Zusammenhang mit der Fall. Der Relevanz Workflow wird angezeigt und wie folgt beschrieben:
  
![Relevanzworkflow](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- **Zyklen der Bewertung und Nachverfolgen von Änderungen**:
    
  - **Assessment**: ermöglicht frühe Assessment basierend auf einer Stichprobe von Dateien an und verwendet diese Bewertung Entscheidungen, die Leistung der vorhersehbare Codierung bestimmen anwenden. 
    
  - **Titel**: berechnen und Anzeigen der Zwischenergebnisse der Bewertung bei der Überwachung statistische Gültigkeit des Prozesses. 
    
- **Zyklen Schulung und Überwachung**
    
  - **Tag**: Erweiterte eDiscovery (Preview) lernen Relevanz Kriterien speziell für jedes Problem basierend auf der Experte iterative überprüfen und Kategorien der einzelnen Dateien.
    
  - **Titel**: berechnen und Anzeigen der Zwischenergebnisse der Schulung Relevanz bei der Überwachung statistische Gültigkeit des Prozesses. 
    
- **Batch-Berechnung**: die kumulierte und gelernten Relevanz Kriterien auf die gesamte Dateisammlung angewendet wird und eine Bewertung Relevanz für jede Datei generiert wird.
    
- **Decide**: die Ergebnisse der Analyse auf die gesamte Groß-/Kleinschreibung angewendet wird nach der Berechnung Batch angezeigt, und Daten zur Dokument überprüfen Entscheidungen treffen werden angezeigt.
    
- **Test**: Ergebnisse können getestet werden, um die Gültigkeit und Effektivität der Verarbeitung erweiterte eDiscovery (Preview) überprüfen.

- **Suche**: Sobald der Relevanz Workflow abgeschlossen ist, können die Ausgabe wie Lese Quantil eines Dokuments für Ihr Problem bei der Ausführung einer Abfrage in das Workingset.
    
## <a name="guidelines-for-relevance-training-and-review"></a>Richtlinien für die Relevanz Schulung und überprüfen

Es folgt eine Übersicht über Richtlinien für die Relevanz Schulung und überprüfen:
  
- **Fehler und Inkonsistenzen**: Kategorien Fehler während des Trainings vorgenommen wurde, kehren Sie zur vorherigen Datei herunter, die zu korrigieren. Wenn aufgrund zu vieler Fehler an den richtigen vorhanden sind, oder es eine neue Perspektive der Groß-/Kleinschreibung oder Problem ist, die Relevanz Kriterien sollten vom Administrator neu definiert werden, und die Relevanz Schulung neu gestartet.
    
- **Tag und Schulung**: 
    
  - Dateien sollten basierend auf dem Inhalt nur markiert werden. Metadaten wie der Verwaltungsberechtigte, Datum oder Dateipfad nicht berücksichtigt. 
    
  - Berücksichtigen Sie den Datum nicht Bereich Angaben im Text beim Markieren von Dateien.
    
  - Berücksichtigt beim Markieren von Dateien keine eingebettete Grafiken.
     
  - Ignorieren auf Relevanz angewendetem Text wird in der angezeigten Datei in der Textansicht in Relevanz entfernt. Wenn die Werte für Text ignorieren nach Relevanz Schulung bereits Schritte definiert wurden, wird der neue Text ignorierte auf Beispieldateien aus den Punkt in dem er definiert wurde erstellt angewendet werden. Das Feature Text ignorieren sollte mit Bedacht, verwendet werden, da die Verwendung die Leistung von Dateianalyse verringern kann
    
  - Verwenden Sie die **Überspringen tagging** Option nur bei Bedarf. Erweiterte eDiscovery (Preview) werden nicht basierend Übersprungene Dateien Schulen. Bewertung, wenn es schwierig ist, sagen, ob eine Datei relevant ist ist es besser, Tag als Relevant (R) oder nicht relevant (Nr.) nach Möglichkeit statt **Überspringen**auswählen. Wenn erweiterte eDiscovery (Preview) Training ausgewertet wird, kann diese klicken Sie dann wie gut diese Dateitypen verarbeitet wurden angezeigt werden.
    
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
  
## <a name="more-information"></a>Weitere Informationen

[Grundlegendes zur Bewertung in Relevanz](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[Kategorien und Bewertung](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[Kategorien und Relevanz-Schulung](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz Analyse](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden je nach den Ergebnissen](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz Analyse](../test-relevance-analysis-in-advanced-ediscovery.md)

[Fragen in Arbeitssatz ab](working-set-search.md)
