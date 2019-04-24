---
title: Ausführen des Prozess Moduls in Office 365 Advanced eDiscovery
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
ms.assetid: dbc1e251-0596-443b-ac9b-f398ba955b73
description: 'Informationen zu den Richtlinien für die Vorbereitung von Fall Dateien von Office 365-Daten für die Analyse mit Office 365 Advanced eDiscovery.  '
ms.openlocfilehash: 19d50bda21f752ec7c22fe52b6fa7272592de128
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261033"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a>Ausführen des Prozess Moduls in Office 365 Advanced eDiscovery

Fall Dateien werden während des **Prepare** \> - **Vorgangs**in die erweiterte eDiscovery geladen. 
  
> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a>Richtlinien: Vorbereiten von Daten für Advanced eDiscovery

- **Qualität**: identifizieren Sie eindeutig die für den Fall relevante Datei Auffüllung.
    
- **Lasten**: Laden Sie die Dateien an einen Speicherort, auf den Advanced eDiscovery zugegriffen werden kann.
    
- **Datei-ID**: ein eindeutiger Dateibezeichner in Advanced eDiscovery. Wenn kein Dateibezeichner importiert wird, generiert Advanced eDiscovery automatisch die ID. Wenn Sie die ID in einem nachfolgenden Prozess laden zuordnen und einen anderen Pfad als bei der anfänglichen Prozessauslastung zuordnen, wird der Pfad von Advanced eDiscovery ersetzt (statt einen neuen Dateieintrag hinzuzufügen). Die ID kann als Referenz im Export Prozess verwendet werden. Der ID-Wert sollte nicht "-1" lauten.
    
- **MD5**: Diese Signatur wird verwendet, um zwischen Dateien zu unterscheiden (zwei Dateien werden nicht als exakte Duplikate betrachtet, es sei denn, Sie haben den gleichen MD5). Standardmäßig berechnet Advanced eDiscovery die MD5-Dateien. Wenn es sich bei den geladenen Dateien um Textdateien handelt, wird empfohlen, den ursprünglichen MD5-Wert zu laden und zu zuordnen, statt ihn in Advanced eDiscovery zu berechnen.
    
- **Dateityp und Name**:
    
  - Advanced eDiscovery kann Dateien mit verschiedenen Formaten verarbeiten und geladene systemeigene Dateien in ein Standardformat wie \*. TXT, HTML oder. XML. Die Verarbeitung von Textdateien ist schneller als systemeigene Dateien. Extrahierte Textdateien werden im Case-Ordner gespeichert.
    
  - Laden Sie keine Dateien, die nicht extrahiert werden können, wie Systemdateien oder Grafik Bilder nicht. Diese Dateien können die Verarbeitung verzögern.
    
  - Stellen Sie sicher, dass die Dateinamen bedeutend benannt werden und die Pfade korrekt sind.
    
- **** Dateipfad: Advanced eDiscovery kann Dateien mit Pfad Längen von bis zu 400 Zeichen laden.
    
- **Textextraktion**: beim Extrahieren von Text aus systemeigenen Dateien werden zusätzlich zu normalem Text auch folgende Elemente extrahiert: ausgeblendeter Text (Excel und doc), ausgeblendete Spalten (Excel), Nachverfolgen von Änderungen (. doc), Vortragsnotizen (PPT), eingebettete Objekte (beispielsweise Excel-Objekte in a. ppt). Diese können im Text-Editor angezeigt werden.
    
- **Text ignorieren**: dieses optionale Feature wird definiert, nachdem der Prozess ausgeführt und analysiert wurde. Ignore Text sollte mit Bedacht verwendet werden, da seine Verwendung die Leistung der Dateianalyse reduzieren kann.
    
- **Mehrsprachiger Text**: Erweiterte eDiscovery verwendet derzeit keine mehrsprachigen Namen für Tags, Verwalter und Probleme.
    
- **Metadaten**: bestimmen Sie, ob es sich bei Metadaten, die Sie in der falldatenbank speichern möchten, um zukünftige Referenzen wie Datumsbereich, Dateigröße, Dateityp, Depotbank und Betreff gibt. Metadaten können geladen werden, nachdem Dateien bereits geladen wurden, ohne das Inventar erneut auszuführen oder den Aufwand für die erneute Verarbeitung hinzugefügt. 
    
  - Wenn die Dateien ursprünglich über den Pfad geladen wurden, ordnen Sie die Spalte path beim späteren Importieren von Metadaten zu. Sie können auf die Datei anhand der ID verweisen und einen anderen Pfad zuordnen. Dies ist ein nützliches Szenario, wenn sich die Dateipfade ändern.
    
  - Wenn die Dateien ursprünglich mit der Datei-ID geladen wurden, ordnen Sie die ID-Spalte beim Laden von Metadaten zu. Wenn Sie auf die Datei nach Pfad (anstelle von ID) verweisen, werden Dateien mit einer anderen ID erneut geladen. Erweiterte eDiscovery erstellt Kopien der Dateien, statt die Metadaten der vorhandenen Dateien zu laden.
    
- **Familien**: Es ist nicht möglich, eine Familie ohne das übergeordnete Element (Familienoberhaupt) zu laden. 
    
- **Dateigröße**: Es gibt keine Beschränkung für die Größe der Dateien, die in Advanced eDiscovery geladen wurden. Für Analysen (analysieren, Relevanz usw.) beträgt die Grenze 5.242.880 Zeichen des extrahierten Texts. Größere Dateien werden ignoriert (beispielsweise in Relevanz, Dateien nehmen nicht am Relevanz-Schulungsprozess Teil und erhalten nach der Batch Berechnung kein Relevanz-Ergebnis).
    
- **Datei Menge**: Es wird kein Grenzwert für die Anzahl der Dateien empfohlen, die in einem einzelnen Fall verarbeitet werden können. Die Leistung hängt von den Ressourcen Ihres Systems ab. 
    
## <a name="filtering-files"></a>Filtern von Dateien

Eine benutzerdefinierte Bezeichnung kann mit einer Reihe von Dateien verknüpft werden, um Sie von Prozess-oder anderen Aufgaben auszuschließen. Jeder Prozess Sitzung ist eine Batch-ID zugeordnet. Obwohl die Batch-ID für den Experten nicht relevant ist, kann dies mithilfe eines Such Dienstprogramms erfolgen, indem ein Filter für den aktuellen Batch hinzugefügt wird und alle entsprechenden Dateien mit einer benutzerdefinierten Bezeichnung gekennzeichnet werden. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Prozessmodul wird ausgeführt und Daten geladen](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[Anzeigen der Ergebnisse des Prozess Moduls](view-process-module-results-in-advanced-ediscovery.md)

