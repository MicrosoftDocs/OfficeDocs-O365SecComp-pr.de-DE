---
title: Verwenden des Relevance-Moduls zum Analysieren von Daten nach belegen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 3aa37a6778947934759eb652a9367559b9ef838b
ms.sourcegitcommit: 2c5834235c32b2616e1813ce24eeb3419a09629f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2019
ms.locfileid: "31030156"
---
# <a name="use-the-relevance-module-to-analyze-data-in-evidence"></a>Verwenden des Relevance-Moduls zum Analysieren von Daten nach belegen

In Daten Untersuchungen (Preview) enthält das Relevanz-Modul die Relevanz von Schulungen und die Überprüfung von Dateien im Zusammenhang mit einer Untersuchung. Der Relevanz-Workflow wird angezeigt und wie folgt beschrieben:
  
![Relevanz-Workflow](../media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- **Zyklen der Bewertung und Nachverfolgung**:
    
  - **Bewertung**: ermöglicht eine frühe Bewertung basierend auf einer Zufallsstichprobe von Dateien und verwendet diese Bewertung, um Entscheidungen zu treffen, um die Leistung des vorher sagenden Codierungsprozesses zu bestimmen. 
    
  - **Track**: berechnen und Anzeigen von Zwischenergebnissen der Bewertung, während die statistische Gültigkeit des Prozesses überwacht wird. 
    
- **Zyklen der Schulung und Nachverfolgung**
    
  - **Tag**: Daten Untersuchungen (Preview) erfahren Sie anhand der iterativen Überprüfung und des Taggings einzelner Dateien, welche Relevanz-Kriterien für jedes Problem gelten.
    
  - **Track**: berechnen und Anzeigen von zwischenErgebnissen der Relevanz-Schulung bei gleichzeitiger Überwachung der statistischen Gültigkeit des Prozesses. 
    
- **Batch Berechnung**: die akkumulierten und gelernten Relevanz-Kriterien werden auf die gesamte Dateisammlung angewendet, und für jede Datei wird ein relevanzwert generiert.
    
- **Entscheiden**: die Ergebnisse der Analyse, die auf den gesamten Fall angewendet werden, werden nach der Batch Berechnung angezeigt, und es werden Daten zum Überprüfen der Dokumentüberprüfung angezeigt.
    
- **Test**: Ergebnisse können getestet werden, um die Gültigkeit und Wirksamkeit der Daten Untersuchungen (Vorschau) zu überprüfen.

- **Suche**: Sobald der Relevanz-Workflow abgeschlossen ist, können Sie die Ausgabe wie zum Beispiel "Read Perzentil" eines Dokuments für Ihr Problem verwenden, wenn Sie eine Abfrage innerhalb des Arbeitssatzes ausführen.
    
## <a name="guidelines-for-relevance-training-and-review"></a>Richtlinien für Relevanz Schulungen und Überprüfungen

Es folgt eine Übersicht über die Richtlinien für die Relevanz von Schulungen und Überprüfungen:
  
- **Fehler und**Inkonsistenzen: Wenn während des Trainings Markierungsfehler auftreten, kehren Sie zu früheren Datei Beispielen zurück, um Sie zu korrigieren. Wenn zu viele Fehler zu korrigieren sind oder eine neue Perspektive für den Fall oder das Problem vorliegt, sollten die Relevanz-Kriterien vom Administrator neu definiert werden, und das Relevanz-Training wurde erneut gestartet.
    
- **Tagging und Schulung**: 
    
  - Dateien sollten nur auf der Grundlage von Inhalten gekennzeichnet werden. Berücksichtigen Sie keine Metadaten wie Depot, Datum oder Dateipfad. 
    
  - Beachten Sie beim Taggen von Dateien keine Datumsbereiche im Text.
    
  - Berücksichtigen Sie beim Taggen von Dateien keine eingebetteten Grafiken.
     
  - Text ignorieren, der auf Relevanz angewendet wird, wird in der angezeigten Dateiinhalt in der Textansicht relevant entfernt. Wenn die Werte für Ignore Text definiert wurden, nachdem Relevanz Training bereits gestartet wurde, wird der neue ignorierte Text auf Beispieldateien angewendet, die von dem Punkt erstellt wurden, an dem Sie definiert wurde. Das Feature Text ignorieren sollte vorsichtig verwendet werden, da die Verwendung die Leistung der Dateianalyse reduzieren kann.
    
  - Verwenden Sie die Option **Tagging überspringen** nur bei Bedarf. Daten Untersuchungen (Preview) werden nicht basierend auf übersprungenen Dateien trainiert. Wenn es schwierig ist, zu beurteilen, ob eine Datei relevant ist, sollten Sie bei der Bewertung, wann immer möglich, nicht über **springen**, sondern als relevant (R) oder nicht relevant (Nr) markieren. Wenn Daten Untersuchungen (Preview) das Training auswertet, kann dann gesehen werden, wie gut diese Dateitypen verarbeitet wurden.
    
  - Auch Dateien mit sehr kleinem extrahiertem Text sollten, wenn möglich, als R/NR als "Skip" markiert werden. 
    
  - Tagging kann sich auf die Klassifizierung auswirken, solange die Datei lesbar ist und als R/NR gekennzeichnet werden kann.
    
  - Die Dateisequenz Nummer in der Liste angezeigte Beispieldateien auf der Registerkarte **Tag** ermöglicht es dem Benutzer, zur ursprünglichen angezeigten Reihenfolge der Dateien zurückzukehren. 
    
  - Sie können zu einem beliebigen Beispiel zurückkehren und das Tagging der Assessment-und Trainingssatz Dateien ändern. Die Änderungen werden beim Erstellen des nächsten Beispiels angewendet.
    
  - Gescannte Excel-Dateien im PDF-Format sollten beim Taggen von Dateien genauso behandelt werden wie native Excel-Dateien.
    
  - Wenn Sie Zweifel bezüglich des Relevanz-Taggings einer Datei haben, konsultieren Sie einen Experten. Das falsche Tagging während der Relevanz-Schulung kann zu einem späteren Zeitpunkt im Prozess zu Zeitverlusten führen und sich auch negativ auf die Qualität der Gesamtergebnisse auswirken.
    
  - Schlüsselwörter, die in Stichwortlisten definiert wurden, werden in Farben angezeigt, damit der Benutzer relevante Dateien beim taggen identifiziert.
    
- **Batch Berechnung**: Dateien, die vom Experten als R/Nr markiert wurden, erhalten eine Bewertung von 0 oder 100. Dies gilt für das Tagging vor der Batch Berechnung. Wenn der Experte das Problem nach der Batch Berechnung in den Leerlauf umgeschaltet hat und dieses Problem weiterhin kennzeichnet, werden die neu markierten Ergebnisse nicht 100/0, sondern die ursprüngliche Partitur.
    
- **Probleme und Samplingmodus**: Probleme werden normalerweise deaktiviert, wenn die Arbeit an diesen abgeschlossen ist (Relevanz-Schulung wird stabilisiert und die Batch Berechnung durchgeführt), wenn die Probleme abgebrochen werden oder wenn ein anderer Benutzer an den Problemen arbeitet.
    
## <a name="steps-in-relevance-training"></a>Schritte in Relevanz Schulung

Auf der Registerkarte **Relevanz \> verfolgen** werden mit den folgenden Schritten Empfehlungen zur Verarbeitung von Daten untersucht. Die Implikationen werden im folgenden beschrieben, wenn jeder der folgenden Schritte im Relevanz-Schulungsprozess empfohlen wird. 
  
- Tagging/Continue Tagging: Dateiüberprüfung und Relevanz-Tagging, die von einem Experten für jede Datei und jedes Problem innerhalb eines Beispiels ausgeführt werden.
    
  - Implikation: ein vorhandenes Beispiel muss markiert werden.
    
- Bewertung/Fortsetzung der Bewertung: ermöglicht die vorzeitige Validierung der Relevanz der Groß-/Kleinschreibung und eine vorläufige Ansicht der Relevanz der für den aktuellen Fall importierten Datei Auffüllung.
    
  - Implikation: mehr Bewertung ist erforderlich oder empfohlen.
    
- Schulung/Fortbildung: Prozess, bei dem Daten Untersuchungen vom Experten erlernt werden, der die Dateibeispiele kennzeichnet und die Möglichkeit erhält, Relevanz-Kriterien zu identifizieren, die für jedes Problem im Kontext jedes Falls relevant sind.
    
  - Implikation: das Problem benötigt mehr Schulung; Das nächste Beispiel sollte erstellt und gekennzeichnet werden. 
    
- Batch Berechnung: Relevanzprozess, bei dem Daten Untersuchungen das während der Schulung erworbene Wissen übernehmen und auf die gesamte Datei Auffüllung anwenden. Alle Dateien in der entsprechenden Dateigruppe werden auf Relevanz ausgewertet und einem Relevanz-Wert zugewiesen.
    
  - Implikation: das Problem wurde stabilisiert, und die Batch Berechnung kann ausgeführt werden.
    
- Catch-up: Relevanz gibt an, wann ein Experte ein Beispiel von Dateien überprüft und markiert, die aus einer zusätzlichen Datei Auslastung während eines Szenarios für die parallele Auslastung ausgewählt wurden.
    
  - Implikation: Es wurde eine neue Ladung hinzugefügt, und der Nachholbedarf ist erforderlich, um weiter zu arbeiten.
    
- Tag Inkonsistenzen: Prozess identifiziert über einen Daten Ermittlungs Algorithmus Inkonsistenzen im Datei Kennzeichnungs Prozess, die sich negativ auf die Analyse auswirken können.
    
  - Implikation: im nächsten Beispiel werden Dateien enthalten, die in vorherigen Beispielen markiert wurden, und Ihr Tagging muss erneut ausgeführt werden.
    
- Klassifizierung aktualisieren: ermöglicht dem Benutzer das Anwenden von Markierungs-oder Seeding Änderungen.
    
  - Implikation: Tagging-und Seeding Änderungen können angewendet werden, ohne dass ein weiteres Beispiel für die Relevanz manuell ausgeführt werden muss.
    
- In der Warteschleife: der Relevanz-Schulungsprozess ist abgeschlossen.
    
  - Implikation: an dieser Stelle ist keine Relevanz-Schulung erforderlich.
    
Daten Untersuchungen führen Sie zwar durch den Prozess, mit empfohlenen nächsten Schritten in unterschiedlichen Phasen können Sie aber auch zwischen Registerkarten und Seiten navigieren und Entscheidungen treffen, um Situationen zu behandeln, die für Ihren Einzelfall, Ihr Problem oder Ihre Prozess zur Dokumentüberprüfung. 
  
Es ist möglich, Daten Untersuchungen zu akzeptieren oder zu überschreiben, die bei der Verarbeitung von Auswahlmöglichkeiten auftreten. Wenn Sie einen anderen als den empfohlenen nächsten Schritt ausführen möchten, klicken Sie auf den **nächsten Schritt** , der in der erweiterten Problemanzeige im Dialogfeld angezeigt wird, klicken Sie neben dem nächsten Schritt auf die Schaltfläche **ändern** , und wählen Sie eine andere Option für nächsten Schritt aus. 
  
> [!NOTE]
> Einige Optionen bleiben nach dem entriegeln möglicherweise deaktiviert, da Sie nicht für die Verwendung an diesem Punkt des Prozesses unterstützt werden. 
  
## <a name="more-information"></a>Weitere Informationen

[Bedeutung der Bewertung](../assessment-in-relevance-in-advanced-ediscovery.md)
  
[Tagging und Bewertung](../tagging-and-assessment-in-advanced-ediscovery.md)
  
[Tagging-und Relevanz-Schulung](../tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz-Analyse](../track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden basierend auf den Ergebnissen](../decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz-Analyse](../test-relevance-analysis-in-advanced-ediscovery.md)

[Abfragen der Daten nach belegen](evidence-query.md)
