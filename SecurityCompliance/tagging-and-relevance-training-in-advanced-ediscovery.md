---
title: Tagging-und Relevanz-Schulung in Office 365 Advanced eDiscovery
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
ms.assetid: 8576cc86-d51b-4285-b54b-67184714cc62
description: 'Hier finden Sie Informationen zu den Schritten zur Kennzeichnung und zum Arbeiten mit einem Schulungs Beispiel von 40-Dateien während der Relevanz-Schulungsstufe von Office 365 Advanced eDiscovery.  '
ms.openlocfilehash: e8c9c02d72a756565f6fe59011a6788f592463eb
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260408"
---
# <a name="tagging-and-relevance-training-in-office-365-advanced-ediscovery"></a>Tagging-und Relevanz-Schulung in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Thema wird die Vorgehensweise für das Arbeiten mit dem Advanced eDiscovery Relevance Training-Modul beschrieben. 
  
Nachdem die Bewertung in Advanced eDiscovery abgeschlossen ist und Sie die Relevanz-Schulungsstufe eingeben, wird ein Übungsbeispiel von 40-Dateien in die Tag-Registerkarte zum Taggen gebracht. 
  
## <a name="performing-relevance-training"></a>Durchführen von Relevanz-Schulungen

1. Auf der Registerkarte ** \> relevanztag** wird der Bereich Tagging standardmäßig im linken Bereich angezeigt, und die Beispieldateien werden nacheinander für Tagging angezeigt. 
    
    ![Bereich "Relevanztag"](media/0cf19ab4-b427-4a7f-8749-0f4ed9afaf58.png)
  
    Auf der Registerkarte **Tag** wird der Anzeigename der Datei angezeigt. Dabei kann es sich um den Pfad, den e-Mail-Betreff, den Titel oder den benutzerdefinierten Namen handeln. Die ID, der Dateipfad oder der Textpfad können kopiert werden, indem Sie mit der rechten Maustaste auf den Pfad der Datei klicken. 
    
    Die Tagging-Statistik des **Tag-Tags** zeigt die Datei Beispiel Nummer (oben im linken Bereich), die Anzahl der aktuell angezeigten Datei aus den Gesamtdateien im Beispiel (unten im rechten Bereich) und die aktuelle Gesamtanzahl der markierten Dateien im Beispiel (unten in t er Linker Bereich), der sich während der Tag-Dateien ändert. Dies gilt für alle relevanten Taggings, sei es bei der Bewertung, Schulung, catch-up oder Test. 
    
    Symbole, die das vorhanden sein von Kommentaren, Tags und Familiendateien angeben, werden in der Datei Ansicht in einer Leiste oberhalb der Datei angezeigt.
    
2. Bestimmen Sie die Relevanz der Datei für das Fall Problem, und markieren Sie die Datei mithilfe der Symbolschaltflächen oder Tastenkombinationen für die Tagging-Option, wie in der folgenden Tabelle dargestellt:
    
| |
|**Tagging-Option**|**Beschreibung**|**Tastenkombination**|**Für mehrere Probleme-Tastenkombination für Massen Tags**|
|:-----|:-----|:-----|:-----|
|R  <br/> |Relevanten  <br/> |Z  <br/> |UMSCHALT + Z  <br/> |
|NR  <br/> |Nicht relevant  <br/> |X  <br/> |UMSCHALT + X  <br/> |
|Überspringen  <br/> |Überspringen  <br/> |C  <br/> |UMSCHALT + A  <br/> |
   
  - Wenn mehrere Probleme für eine Datei vorhanden sind, wird nach dem Markieren eines Problems die Auswahl zum nächsten Problem verschoben (falls verfügbar). 
    
  - Schlüsselwörter, die vom Administrator oder Case Manager beim Hervorheben von Stichwörtern (Relevanz \> Setup hervorgehobene Schlüsselwörter) definiert wurden, werden angezeigt (in bestimmten Farben), um relevante Dateien beim taggen zu identifizieren. Wenn ein Schlüsselwort eine doppelte Unterstreichung aufweist, können Sie darauf klicken, um einen Tooltip mit der Beschreibung des Schlüsselwortes anzuzeigen. 
    
    Klicken Sie optional auf der Registerkarte **Tag** auf **Tag-Einstellungen** , um die folgenden Optionen festzulegen: 
    
    ![Relevanz-Tag-Einstellungen](media/533e89fa-7eb4-409e-ab07-f5aab9296dd8.png)
  
  - **Massentag**: Verwenden Sie diese Option, um mehrere Probleme für eine Datei zuzuweisen, indem Sie **alle** auswählen, um das Tag für die ausgewählte Datei für alle Probleme festzulegen (Überschreibt bereits markierte Probleme) oder indem Sie **den Rest** auswählen, um das Tag auf die verbleibenden nicht markierten Probleme anzuwenden. Die ausgewählte Option bleibt für alle Fälle dieses Benutzers gültig, bis Sie von diesem Benutzer geändert wurde (Einstellung ist pro Benutzer für alle Fälle des Benutzers). 
    
  - **Auto-Tag**: Aktivieren Sie dieses Kontrollkästchen, um andere Probleme für eine Datei nach einem einzelnen relevanten Tagging als nicht relevant festzulegen.
    
  - **Auto Advance**: Aktivieren Sie dieses Kontrollkästchen, um die angezeigte Dateiauswahl in die nächste Datei zu verschieben, wenn Sie das letzte oder nur nicht gekennzeichnete Problem kennzeichnen. 
    
    ÜberSprungene Dateien werden nicht für Relevanz Schulungen und Relevanz Scoring Zwecke berücksichtigt.
    
3. Freitextkommentare, die einer Datei zugeordnet sind, können über die **Kommentar** Option in der Dropdownliste im linken Bereich angezeigt und bearbeitet werden. (optional) 
    
4. Die Richtlinien für das Tagging können angezeigt werden, indem Sie die Option **Tagging Guidelines** in der linken Dropdownliste auswählen. 
    
5. Nachdem Sie alle Dateien in der Liste gekennzeichnet haben und bereit sind, die Ergebnisse zu berechnen, klicken Sie auf **berechnen**. Die Registerkarte **Spur** wird angezeigt. 
    
## <a name="working-with-the-sample-files-list"></a>Arbeiten mit der Liste "Beispieldateien"

In der Liste Beispieldateien können Sie eine Liste der Dateien in einem Schulungs Beispiel anzeigen und verschiedene Aktionen für eine oder mehrere Dateien ausführen. Auf der Registerkarte **relevanztag** \> **** wird im linken Bereich **Beispieldateien** eine Liste der Beispieldateien für die Verarbeitung mit den Prozessen Bewertung, Schulung, catch-up und Inkonsistenzen angezeigt. 
  
1. Wählen Sie **auf \> ** der Registerkarte relevanztag die Beispieldateien in der Dropdownliste im linken Bereich aus. Die Beispieldateien werden im linken Bereich aufgelistet. 
    
    ![Liste der Beispieldateien für das Relevance-Tag](media/fd058bdd-645a-4af1-a1eb-bff08581cb18.png)
  
2. Wählen Sie eine bestimmte Beispiel-oder Dateinummer aus, indem Sie die Nummer in den Feldern **Sample** oder **File** eingeben oder auswählen. 
    
  -   - Eine Dateisequenz Nummer wird in der linken Spalte der angezeigten Dateiliste auf der Registerkarte **Tag** aufgelistet. Durch Klicken auf die Kopfzeile wird die ursprüngliche Reihenfolge der Dateien zurückgegeben. 
    
  - Durch Klicken auf eine Datei Zeile wird der zugehörige Inhalt im rechten Bereich angezeigt.
    
  - Navigieren Sie zwischen Dateien im aktuellen Beispiel, indem Sie die Optionen Untermenüleiste verwenden. Darüber hinaus stehen Navigationstasten Kombinationen zur Verfügung:
    
    So navigieren Sie zu der ersten Datei im Beispiel: UMSCHALT + STRG +\<
    
    So navigieren Sie zur vorherigen Datei im Beispiel: UMSCHALT +\<
    
    So navigieren Sie zur nächsten Datei im Beispiel: UMSCHALT +\>
    
    So navigieren Sie zur letzten Datei im Beispiel: UMSCHALT + STRG +\>
    
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Bedeutung der Bewertung](assessment-in-relevance-in-advanced-ediscovery.md)
  
[Tagging und Bewertung](tagging-and-assessment-in-advanced-ediscovery.md)
  
[Nachverfolgen der Relevanz-Analyse](track-relevance-analysis-in-advanced-ediscovery.md)
  
[Entscheiden basierend auf den Ergebnissen](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[Testen der Relevanz-Analyse](test-relevance-analysis-in-advanced-ediscovery.md)

