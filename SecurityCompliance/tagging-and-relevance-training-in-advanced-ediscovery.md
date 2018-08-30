---
title: Kategorien und Relevanz Schulung in Office 365 erweiterte eDiscovery
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
ms.assetid: 8576cc86-d51b-4285-b54b-67184714cc62
description: 'Informationen zu den Schritten in Tag, und klicken Sie dann mit einer Stichprobe Schulung von 40 Dateien während der Phase Relevanz Schulung für Office 365 erweiterte eDiscovery arbeiten.  '
ms.openlocfilehash: 90272452c8c1317957e542eba07bc43722f9c0e9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529486"
---
# <a name="tagging-and-relevance-training-in-office-365-advanced-ediscovery"></a>Kategorien und Relevanz Schulung in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Thema wird das Verfahren für die Arbeit mit der erweiterten eDiscovery Relevanz Schulungsmodul. 
  
Nach Bewertung in erweiterten eDiscovery abgeschlossen ist, und geben Sie die Relevanz Schulung Phase, ist ein Beispiel für die Schulung von 40 Dateien in die Registerkarte-Tag zum Markieren von eingebunden. 
  
## <a name="performing-relevance-training"></a>Ausführen der Relevanz-Schulung

1. In der **Relevanz \> Tag** Registerkarte im Bereich Kategorien von standardmäßig in der linken und dem Beispiel Dateien angezeigt werden, jeweils einmal für die Markierung angezeigt wird. 
    
    ![Relevanztagbereich](media/0cf19ab4-b427-4a7f-8749-0f4ed9afaf58.png)
  
    Anzeigename für die Datei wird in der Registerkarte **Tag** angezeigt. Der Pfad, e-Mail-Betreff, Titel oder benutzerdefinierter Name möglicherweise. Die ID, Dateipfad oder Textpfad kann mit der rechten Maustaste auf den Pfad der Datei kopiert werden. 
    
    Die Registerkarte **Tag** tagging Statistiken anzeigen, die Beispiel-Dateinummer (oben links), die Anzahl der aktuell angezeigten-Datei aus der Dateien insgesamt in der Stichprobe (unten rechts) und die Gesamtzahl der markierten Dateien in der Stichprobe (unterer Teil von t entspricht er links Bereich), wodurch geändert wird, wie Sie Dateien markieren. Dies gilt für alle Relevanz tagging durchgeführt, in Assessment, Schulungen, synchronisieren oder Test. 
    
    Symbole, die angibt, des Vorhandenseins von Kommentaren, Kategorien und Produktfamilie Dateien werden in der Dateiansicht in einer Leiste über die Datei angezeigt.
    
2. Bestimmen Sie die Datei Relevanz für die Groß-/Kleinschreibung Problem und markieren Sie die Datei mit dem Tag Optionsfelder Symbol oder Tastenkombinationen, wie in der folgenden Tabelle dargestellt:
    
| |
|**Markieren die option**|**Beschreibung**|**Tastenkombination**|**Massen Sie für mehrere Probleme --Tag Tastenkombination**|
|:-----|:-----|:-----|:-----|
|R  <br/> |Relevante  <br/> |Z  <br/> |Umschalttaste + Z  <br/> |
|NR.  <br/> |Nicht relevant  <br/> |X  <br/> |Umschalttaste + X  <br/> |
|Überspringen  <br/> |Überspringen  <br/> |C  <br/> |UMSCHALT + A  <br/> |
   
  - Wenn mehrere Probleme für eine Datei vorhanden sind, nach der Markierung ein Problem verschiebt die Markierung zum nächsten Problem (falls vorhanden). 
    
  - Schlüsselwörter, die durch den Administrator oder die Groß-/Kleinschreibung Manager definiert wurden, wenn Sie Schlüsselwörter hervorheben (Relevanz Setup \> Schlüsselwörter hervorgehoben), wird zur Identifizierung der relevante Dateien während tagging (im angegebenen Farben) angezeigt. Wenn ein Schlüsselwort doppelte unterstrichen ist, kann darauf geklickt werden, um eine QuickInfo mit dem Schlüsselwort Beschreibung anzuzeigen. 
    
    Klicken Sie optional auf der Registerkarte **Tag** auf **Einstellungen** , um die folgenden Optionen festlegen: 
    
    ![Relevanztageinstellungen](media/533e89fa-7eb4-409e-ab07-f5aab9296dd8.png)
  
  - **Massen-Tag**: mit dieser Option können Sie mehrere Probleme für eine Datei, indem Sie **Alle** das Tag für die ausgewählte Datei für alle Probleme (überschreibt bereits markierte Probleme) festlegen oder durch auswählen **der Rest** anzuwendende das Tag für die verbleibenden ohne Tags Probleme zuweisen. Die ausgewählte Option bleibt in Kraft für alle Fälle des Benutzers, bis die von diesem Benutzer geändert (Einstellung ist für alle Benutzer Fällen pro Benutzer). 
    
  - **Automatische Tag**: Aktivieren Sie dieses Kontrollkästchen, das andere Probleme für eine Datei als nicht festgelegt nach einer einzelnen relevanten tagging relevant.
    
  - **Automatische Advance**: Aktivieren Sie dieses Kontrollkästchen angezeigte Datei mit der nächsten Datei zu markieren, wenn die letzte oder nur ohne Tags Problem markieren. 
    
    Übersprungene Dateien werden nicht für die Relevanz Schulung und Punktzahl Relevanz berücksichtigt.
    
3. Freitext-, einer Datei zugeordneten Kommentare können angezeigt und über die Option **Kommentar** in der linken Dropdownliste bearbeitet werden. (optional) 
    
4. Richtlinien für die Markierung können durch Auswählen der Option **Markieren von Richtlinien** in den linken Bereich Dropdown-Liste angezeigt werden. 
    
5. Nachdem Sie alle Dateien in der Liste Kategorien Fertig stellen und zum Berechnen der Ergebnisse bereit sind, klicken Sie auf **berechnen**. Die Registerkarte **Nachverfolgen** wird angezeigt. 
    
## <a name="working-with-the-sample-files-list"></a>Arbeiten mit der Liste der Beispiel-Dateien

Die Beispielliste Dateien können Sie zum Anzeigen einer Liste der Dateien in einer Stichprobe Schulung und verschiedene Aktionen für eine oder mehrere Dateien ausführen. In der **Relevanz** \> **Tag** Registerkarte **Beispieldateien** linke Bereich zeigt eine Liste der Beispieldateien für die Verarbeitung von Geschäftsprozessen mit Assessment, Schulungen, synchronisieren und Inkonsistenzen. 
  
1. In der **Relevanz \> Tag** Registerkarte, wählen Sie die Beispieldateien in den linken Bereich Dropdown-Liste aus. Klicken Sie im linken Bereich sind die Beispieldateien aufgeführt. 
    
    ![Relevanztag: Liste mit Beispieldateien](media/fd058bdd-645a-4af1-a1eb-bff08581cb18.png)
  
2. Wählen Sie eine bestimmte Anzahl von Beispieldaten oder Datei durch eingeben oder auswählen die Nummer in den Feldern **Beispiel** oder eine **Datei** aus. 
    
  -   - Eine Sequenznummer Datei wird in der linken Spalte der Liste angezeigte Datei auf der Registerkarte " **Tag** " aufgeführt. Durch Klicken auf die Kopfzeile, gibt die ursprüngliche angezeigte Reihenfolge der Dateien zurück, mit der ursprünglichen Reihenfolge. 
    
  - Durch Klicken auf eine Zeile Datei zeigt seinen Inhalt im rechten Bereich.
    
  - Navigieren Sie zwischen Dateien im aktuellen Beispiel mithilfe der unteren Optionen der Menüleiste. Darüber hinaus stehen Navigation Tastenkombinationen zur Verfügung:
    
    Um die erste Datei in der Stichprobe zu navigieren: UMSCHALT + STRG +\<
    
    Navigieren Sie auf die vorherige Datei im Beispiel: UMSCHALT +\<
    
    Navigieren Sie in der nächsten Datei in der Stichprobe: UMSCHALT +\>
    
    Um auf die letzte Datei in der Stichprobe zu navigieren: UMSCHALT + STRG +\>
    
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Bewertung in Relevanz](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Kategorien und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden je nach den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

