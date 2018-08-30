---
title: Führen Sie das Modul Prozess in Office 365 erweiterte eDiscovery
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Informationen Sie zu Richtlinien für die Vorbereitung Groß-/Kleinschreibung von Dateien von Office 365-Daten für die Analyse mit Office 365 erweiterte eDiscovery.  '
ms.openlocfilehash: 52b1dce9fb778c6628d90c39135f0c93f08134d7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530002"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a>Führen Sie das Modul Prozess in Office 365 erweiterte eDiscovery

Groß-/Kleinschreibung Dateien werden in der erweiterten eDiscovery geladen, während der **Vorbereitung** \> **Prozess**. 
  
> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a>Richtlinien: Vorbereiten von Daten für erweiterte eDiscovery

- **Qualität**: eindeutig identifizieren die Groß-/Kleinschreibung Datei Auffüllung für die Groß-/Kleinschreibung relevant sind.
    
- **Lädt**: Laden Sie die Dateien in einem Speicherort, der für erweiterte eDiscovery zugänglich ist.
    
- **Datei-ID**: einen eindeutigen Bezeichner in erweiterten eDiscovery. Wenn kein Dateibezeichner importiert ist, generiert erweiterte eDiscovery automatisch die-ID. Wenn Sie die nachfolgende Ladevorgänge Prozess-ID zugeordnet, und ordnen einen anderen Pfad als in der ersten Prozess laden, wird erweiterte eDiscovery ersetzen Sie den Pfad (anstatt einen neuen Dateieintrag hinzufügen). Die ID kann als Referenz in den Exportvorgang verwendet werden. Der ID-Wert darf nicht "-1" sein.
    
- **MD5**: Diese Signatur wird verwendet, um zwischen Dateien zu unterscheiden (zwei Dateien gelten nicht als genaue Duplikate, wenn sie die gleiche MD5 haben). Standardmäßig berechnet erweiterte eDiscovery MD5-Dateien. Wenn die geladenen Dateien Textdateien sind, empfiehlt es sich zum Laden und zum Zuordnen des Originalwert MD5, anstatt es in erweiterten eDiscovery berechnen.
    
- **Typ und Name der**:
    
  - Erweiterte eDiscovery kann verarbeitet Dateien in verschiedenen Formaten und extrahieren geladene systemeigene Dateien in ein Standardformat wie \*. TXT, HTML oder. XML-. Verarbeitung von Textdateien ist schneller als systemeigene Dateien. Extrahierten Textdateien werden im Ordner "Case" gespeichert.
    
  - Geladen Sie Dateien, die extrahiert werden können, wie Systemdateien oder Grafiken, werden nicht werden. Diese Dateien können eine Verzögerung Verarbeitung.
    
  - Stellen Sie sicher, dass erheblich Dateinamen heißen und Pfade richtig sind.
    
- **Pfad**: Erweiterte eDiscovery kann Dateien mit Länge des Pfads bis 400 Zeichen zu laden.
    
- **Extraktion von Text**: beim Extrahieren von Text aus Originaldateien, zusätzlich zu den normalen Text werden auch die folgenden extrahiert: ausgeblendeter Text (Excel und doc) ausgeblendet Spalten (Excel), Nachverfolgen von Änderungen (.doc) und Lautsprecher Notizen (PPT), eingebettete Objekte (z. b Excel-Objekte in einer PPT). Diese können im Text-Editor angezeigt werden.
    
- **Text zu ignorieren**: dieses Feature optionale wird definiert, nachdem der Prozess ausgeführt wird und vor der Analyse. Ignorieren Text sollte mit Bedacht verwendet werden, da deren Verwendung die Leistung von Dateianalyse verringern kann.
    
- **Mehrsprachiger Text**: Erweiterte eDiscovery nicht aktuell mehrsprachige Namen für Tags, Verwaltungsberechtigter und Probleme behandelt.
    
- **Metadaten**: ermitteln, ob Metadaten, die in der Groß-/Kleinschreibung Datenbank für die zukünftige wie Datumsbereich, Dateigröße, Dateityp, Verwaltungsberechtigter, speichern und subject werden soll. Metadaten kann geladen werden, nachdem die Dateien ohne erneutes Ausführen der Inventar oder erneute Verarbeitung führt zu mehr Verarbeitungsaufwand hinzufügen bereits geladen wurden. 
    
  - Wenn die Dateien vom Pfad ursprünglich geladen wurden, ordnen Sie die Pfad-Spalte beim Importieren der Metadaten weiter unten. Es ist möglich, verweisen auf die Datei nach ID und einen anderen Pfad zuzuordnen. Dies ist ein Szenario hilfreich, wenn die Dateipfade ändern.
    
  - Wenn die Dateien ursprünglich nach ID-Datei geladen wurden, ordnen Sie die ID-Spalte beim Laden der Metadaten. Verweisen auf die Datei durch Pfad (anstelle der ID) verursacht Dateien mit einer anderen ID erneut geladen werden Erweiterte eDiscovery erstellt Kopien der Dateien vielmehr, Laden von Metadaten der vorhandenen Dateien.
    
- **Familien**: Es ist nicht möglich, eine Familie ohne seines übergeordneten (Head-Produktfamilie) zu laden. 
    
- **Dateigröße**: Es gibt keine Einschränkung auf die Größe der Dateien in erweiterten eDiscovery geladen. Für die Analyse (analysieren, Relevanz usw.) ist die Grenze 5.242.880 extrahierten Textzeichen. Größere Dateien werden ignoriert (beispielsweise in Relevanz, Dateien der Relevanz Schulung Prozess nicht teilnehmen und erhalten Sie eine Bewertung Relevanz nicht nach Batch Berechnung).
    
- **Datei Menge**: Es gibt keine empfohlene Höchstgrenze für die Anzahl der Dateien, die in einer einzelnen Fall behandelt werden kann. Leistung hängt von den Ressourcen des Systems. 
    
## <a name="filtering-files"></a>Filtern von Dateien

Eine benutzerdefinierte Bezeichnung kann eine Reihe von Dateien, deren Prozess oder andere Aufgaben auszuschließende zugeordnet werden. Jede Sitzung Prozess ist eine Batch-ID zugeordnet Obwohl die Batch-ID nicht an den Experten in Relevanz angezeigt wird, kann dies mit einer Suchfunktion durch einen Filter für den aktuellen Batch hinzufügen, und markieren alle entsprechende Dateien mit einer benutzerdefinierten Bezeichnung. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Das Prozess-Modul ausgeführt, und Laden von Daten](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[Anzeigen von Ergebnissen der Prozess Modul](view-process-module-results-in-advanced-ediscovery.md)

