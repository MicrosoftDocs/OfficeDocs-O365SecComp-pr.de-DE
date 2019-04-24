---
title: Verwenden des Relevance-Moduls in Office 365 Advanced eDiscovery
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
ms.assetid: 5d671821-d188-42da-a9ce-9cfe92beedfd
description: 'Erfahren Sie mehr über das Relevanz-Modul in Office 365 Advanced eDiscovery, einschließlich eines Workflows und Richtlinien und Schritte für Schulung und Dateiüberprüfung.  '
ms.openlocfilehash: ad44066c8b00bccacf1f4fe2088aa84096c4db84
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32263787"
---
# <a name="use-the-relevance-module-in-office-365-advanced-ediscovery"></a>Verwenden des Relevance-Moduls in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In Advanced eDiscovery umfasst das Relevance-Modul die Relevanz von Schulungen und Überprüfungen von Dateien im Zusammenhang mit einem Fall. Der Relevanz-Workflow wird angezeigt und wie folgt beschrieben:
  
![Relevanz-Workflow](media/44c67dd2-7a20-40a9-b0ed-784364845c77.gif)
  
- **Zyklen der Bewertung und Nachverfolgung**:
    
  - **Bewertung**: Advanced eDiscovery ermöglicht eine frühe Bewertung basierend auf einer Zufallsstichprobe von Dateien und verwendet diese Bewertung, um Entscheidungen zu treffen, um die Leistung des vorher sagenden Codierungsprozesses zu bestimmen. 
    
  - **Track**: Erweiterte eDiscovery berechnet und zeigt Zwischenergebnisse der Bewertung an, während die statistische Gültigkeit des Prozesses überwacht wird. 
    
- **Schulungs-und Überwachungs Zyklen**:
    
  - **Tag**: Advanced eDiscovery lernt anhand der iterativen Überprüfungen und Markierungen von einzelnen Dateien, welche Relevanz-Kriterien für jedes Problem gelten.
    
  - **Track**: Erweiterte eDiscovery berechnet und zeigt zwischenErgebnisse der Relevanz-Schulung, während die statistische Gültigkeit des Prozesses überwacht wird. 
    
- **Batch Berechnung**: die erweiterte eDiscovery verwendet die akkumulierten und erlernten Relevanz-Kriterien, wendet Sie auf die gesamte Dateisammlung an und generiert Relevanzwerte für jede Datei.
    
- **Entscheiden**: Advanced eDiscovery zeigt die Ergebnisse der Analyse an, die nach der Batch Berechnung auf den gesamten Fall angewendet werden, und zeigt Daten zum Durchführen von Dokument Überprüfungs Entscheidungen an.
    
- **Test**: Erweiterte eDiscovery-Ergebnisse können getestet werden, um die Gültigkeit und Wirksamkeit der erweiterten eDiscovery-Verarbeitung zu überprüfen.
    
## <a name="guidelines-for-relevance-training-and-review"></a>Richtlinien für Relevanz Schulungen und Überprüfungen

Es folgt eine Übersicht über die Richtlinien für die Relevanz von Schulungen und Überprüfungen:
  
- **Fehler und**Inkonsistenzen: Wenn während des Trainings Markierungsfehler auftreten, kehren Sie zu früheren Datei Beispielen zurück, um Sie zu korrigieren. Wenn zu viele Fehler zu korrigieren sind oder eine neue Perspektive für den Fall oder das Problem vorliegt, sollten die Relevanz-Kriterien vom Administrator neu definiert werden, und das Relevanz-Training wurde erneut gestartet.
    
- **Tagging und Schulung**: 
    
  - Dateien sollten nur auf der Grundlage von Inhalten gekennzeichnet werden. Berücksichtigen Sie keine Metadaten wie Depot, Datum oder Dateipfad. 
    
  - Beachten Sie beim Taggen von Dateien keine Datumsbereiche im Text.
    
  - Berücksichtigen Sie beim Taggen von Dateien keine eingebetteten Grafiken.
    
  - Wenn Sie eine Datei mit dem Symbol für die **formatierte Textansicht** beim Markieren anzeigen, sollten Sie die Formatierung von Text nicht berücksichtigen. Beispielsweise wird ein Wort, das durchgestrichen angezeigt wird (eine horizontale Linie durch sein Zentrum, die den Löschvorgang angibt) weiterhin als Teil des analysierten Texts als relevant betrachtet. 
    
  - Text ignorieren, der auf Relevanz angewendet wird (wie vom Fall-Manager oder Administrator festgelegt) wird in der angezeigten Dateiinhalt in der Textansicht relevant entfernt. Wenn die Werte für Ignore Text definiert wurden, nachdem Relevanz Training bereits gestartet wurde, wird der neue ignorierte Text auf Beispieldateien angewendet, die von dem Punkt erstellt wurden, an dem Sie definiert wurde. Das Feature Text ignorieren sollte vorsichtig verwendet werden, da die Verwendung die Leistung der Dateianalyse reduzieren kann.
    
  - Verwenden Sie die Option **Tagging überspringen** nur bei Bedarf. Erweiterte eDiscovery wird nicht basierend auf übersprungenen Dateien trainiert. Wenn es schwierig ist, zu beurteilen, ob eine Datei relevant ist, sollten Sie bei der Bewertung, wann immer möglich, nicht über **springen**, sondern als relevant (R) oder nicht relevant (Nr) markieren. Wenn Advanced eDiscovery das Training auswertet, kann dann gesehen werden, wie gut diese Dateitypen verarbeitet wurden.
    
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

Auf der Registerkarte **Relevanz \> verfolgen** bietet Advanced eDiscovery Empfehlungen für die Fortsetzung der Verarbeitung mit den folgenden Schritten. Die Implikationen werden im folgenden beschrieben, wenn jeder der folgenden Schritte im Relevanz-Schulungsprozess empfohlen wird. 
  
- Tagging/Continue Tagging: Dateiüberprüfung und Relevanz-Tagging, die von einem Experten für jede Datei und jedes Problem innerhalb eines Beispiels ausgeführt werden.
    
  - Implikation: ein vorhandenes Beispiel muss markiert werden.
    
- Bewertung/Fortsetzung der Bewertung: ermöglicht die vorzeitige Validierung der Relevanz der Groß-/Kleinschreibung und eine vorläufige Ansicht der Relevanz der für den aktuellen Fall importierten Datei Auffüllung.
    
  - Implikation: mehr Bewertung ist erforderlich oder empfohlen.
    
- Schulung/Fortbildung: Prozess, bei dem Advanced eDiscovery vom Experten, der die Dateibeispiele kennzeichnet, erlernt und die Möglichkeit erhält, Relevanz-Kriterien für jedes Problem im Kontext jedes Falls zu identifizieren.
    
  - Implikation: das Problem benötigt mehr Schulung; Das nächste Beispiel sollte erstellt und gekennzeichnet werden. 
    
- Batch Berechnung: Relevanzprozess, bei dem Advanced eDiscovery das während der Schulung erworbene Wissen einnimmt und es auf die gesamte Datei Auffüllung anwenden kann. Alle Dateien in der entsprechenden Dateigruppe werden auf Relevanz ausgewertet und einem Relevanz-Wert zugewiesen.
    
  - Implikation: das Problem wurde stabilisiert, und die Batch Berechnung kann ausgeführt werden.
    
- Catch-up: Relevanz gibt an, wann ein Experte ein Beispiel von Dateien überprüft und markiert, die aus einer zusätzlichen Datei Auslastung während eines Szenarios für die parallele Auslastung ausgewählt wurden.
    
  - Implikation: Es wurde eine neue Ladung hinzugefügt, und der Nachholbedarf ist erforderlich, um weiter zu arbeiten.
    
- Tag Inkonsistenzen: Prozess identifiziert über einen erweiterten eDiscovery-Algorithmus Inkonsistenzen im Datei Kennzeichnungs Prozess, die sich negativ auf die Analyse auswirken können.
    
  - Implikation: im nächsten Beispiel werden Dateien enthalten, die in vorherigen Beispielen markiert wurden, und Ihr Tagging muss erneut ausgeführt werden.
    
- Klassifizierung aktualisieren: ermöglicht dem Benutzer das Anwenden von Markierungs-oder Seeding Änderungen.
    
  - Implikation: Tagging-und Seeding Änderungen können angewendet werden, ohne dass ein weiteres Beispiel für die Relevanz manuell ausgeführt werden muss.
    
- In der Warteschleife: der Relevanz-Schulungsprozess ist abgeschlossen.
    
  - Implikation: an dieser Stelle ist keine Relevanz-Schulung erforderlich.
    
Obwohl Advanced eDiscovery Sie durch den Prozess führt, mit empfohlenen nächsten Schritten in unterschiedlichen Phasen, können Sie auch zwischen Registerkarten und Seiten navigieren und Entscheidungen treffen, um Situationen zu beheben, die für Ihren Einzelfall, Ihr Problem oder Ihre Prozess zur Dokumentüberprüfung. 
  
Es ist möglich, erweiterte eDiscovery-Verarbeitungsoptionen für die nächste Schritt Verarbeitung zu akzeptieren oder zu überschreiben. Wenn Sie einen anderen als den empfohlenen nächsten Schritt ausführen möchten, klicken Sie auf den **nächsten Schritt** , der in der erweiterten Problemanzeige im Dialogfeld angezeigt wird, klicken Sie neben dem nächsten Schritt auf die Schaltfläche **ändern** , und wählen Sie eine andere Option für nächsten Schritt aus. 
  
> [!NOTE]
> Einige Optionen bleiben nach dem entriegeln möglicherweise deaktiviert, da Sie nicht für die Verwendung an diesem Punkt des Prozesses unterstützt werden. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Bedeutung der Bewertung](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Tagging und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Tagging-und Relevanz-Schulung](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz-Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden basierend auf den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz-Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

