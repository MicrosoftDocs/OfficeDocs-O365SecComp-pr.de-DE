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
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="07ef1-103">Führen Sie das Modul Prozess in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="07ef1-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="07ef1-104">Groß-/Kleinschreibung Dateien werden in der erweiterten eDiscovery geladen, während der **Vorbereitung** \> **Prozess**.</span><span class="sxs-lookup"><span data-stu-id="07ef1-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="07ef1-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="07ef1-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="07ef1-107">Richtlinien: Vorbereiten von Daten für erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="07ef1-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="07ef1-108">**Qualität**: eindeutig identifizieren die Groß-/Kleinschreibung Datei Auffüllung für die Groß-/Kleinschreibung relevant sind.</span><span class="sxs-lookup"><span data-stu-id="07ef1-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="07ef1-109">**Lädt**: Laden Sie die Dateien in einem Speicherort, der für erweiterte eDiscovery zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="07ef1-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="07ef1-p102">**Datei-ID**: einen eindeutigen Bezeichner in erweiterten eDiscovery. Wenn kein Dateibezeichner importiert ist, generiert erweiterte eDiscovery automatisch die-ID. Wenn Sie die nachfolgende Ladevorgänge Prozess-ID zugeordnet, und ordnen einen anderen Pfad als in der ersten Prozess laden, wird erweiterte eDiscovery ersetzen Sie den Pfad (anstatt einen neuen Dateieintrag hinzufügen). Die ID kann als Referenz in den Exportvorgang verwendet werden. Der ID-Wert darf nicht "-1" sein.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p102">**File ID**: A unique file identifier in Advanced eDiscovery. If no file identifier is imported, Advanced eDiscovery automatically generates the ID. If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry). The ID can be used as a reference in the Export process. The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="07ef1-p103">**MD5**: Diese Signatur wird verwendet, um zwischen Dateien zu unterscheiden (zwei Dateien gelten nicht als genaue Duplikate, wenn sie die gleiche MD5 haben). Standardmäßig berechnet erweiterte eDiscovery MD5-Dateien. Wenn die geladenen Dateien Textdateien sind, empfiehlt es sich zum Laden und zum Zuordnen des Originalwert MD5, anstatt es in erweiterten eDiscovery berechnen.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p103">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5). By default, Advanced eDiscovery calculates the MD5 of files. When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="07ef1-118">**Typ und Name der**:</span><span class="sxs-lookup"><span data-stu-id="07ef1-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="07ef1-p104">Erweiterte eDiscovery kann verarbeitet Dateien in verschiedenen Formaten und extrahieren geladene systemeigene Dateien in ein Standardformat wie \*. TXT, HTML oder. XML-. Verarbeitung von Textdateien ist schneller als systemeigene Dateien. Extrahierten Textdateien werden im Ordner "Case" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p104">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML. Processing of text files is faster than native files. Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="07ef1-p105">Geladen Sie Dateien, die extrahiert werden können, wie Systemdateien oder Grafiken, werden nicht werden. Diese Dateien können eine Verzögerung Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p105">Do not load files that cannot be extracted, such as system files or graphic images. These files may delay processing.</span></span>
    
  - <span data-ttu-id="07ef1-124">Stellen Sie sicher, dass erheblich Dateinamen heißen und Pfade richtig sind.</span><span class="sxs-lookup"><span data-stu-id="07ef1-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="07ef1-125">**Pfad**: Erweiterte eDiscovery kann Dateien mit Länge des Pfads bis 400 Zeichen zu laden.</span><span class="sxs-lookup"><span data-stu-id="07ef1-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="07ef1-p106">**Extraktion von Text**: beim Extrahieren von Text aus Originaldateien, zusätzlich zu den normalen Text werden auch die folgenden extrahiert: ausgeblendeter Text (Excel und doc) ausgeblendet Spalten (Excel), Nachverfolgen von Änderungen (.doc) und Lautsprecher Notizen (PPT), eingebettete Objekte (z. b Excel-Objekte in einer PPT). Diese können im Text-Editor angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p106">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt). These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="07ef1-p107">**Text zu ignorieren**: dieses Feature optionale wird definiert, nachdem der Prozess ausgeführt wird und vor der Analyse. Ignorieren Text sollte mit Bedacht verwendet werden, da deren Verwendung die Leistung von Dateianalyse verringern kann.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p107">**Ignore Text**: This optional feature is defined after Process is run and before Analyze. Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="07ef1-130">**Mehrsprachiger Text**: Erweiterte eDiscovery nicht aktuell mehrsprachige Namen für Tags, Verwaltungsberechtigter und Probleme behandelt.</span><span class="sxs-lookup"><span data-stu-id="07ef1-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="07ef1-p108">**Metadaten**: ermitteln, ob Metadaten, die in der Groß-/Kleinschreibung Datenbank für die zukünftige wie Datumsbereich, Dateigröße, Dateityp, Verwaltungsberechtigter, speichern und subject werden soll. Metadaten kann geladen werden, nachdem die Dateien ohne erneutes Ausführen der Inventar oder erneute Verarbeitung führt zu mehr Verarbeitungsaufwand hinzufügen bereits geladen wurden.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p108">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject. Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="07ef1-p109">Wenn die Dateien vom Pfad ursprünglich geladen wurden, ordnen Sie die Pfad-Spalte beim Importieren der Metadaten weiter unten. Es ist möglich, verweisen auf die Datei nach ID und einen anderen Pfad zuzuordnen. Dies ist ein Szenario hilfreich, wenn die Dateipfade ändern.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p109">If the files were originally loaded by path, map the path column when later importing metadata. It is possible to refer to the file by ID and to map a different path. This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="07ef1-p110">Wenn die Dateien ursprünglich nach ID-Datei geladen wurden, ordnen Sie die ID-Spalte beim Laden der Metadaten. Verweisen auf die Datei durch Pfad (anstelle der ID) verursacht Dateien mit einer anderen ID erneut geladen werden Erweiterte eDiscovery erstellt Kopien der Dateien vielmehr, Laden von Metadaten der vorhandenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p110">If the files were originally loaded by File ID, map the ID column when loading metadata. Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID. Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="07ef1-139">**Familien**: Es ist nicht möglich, eine Familie ohne seines übergeordneten (Head-Produktfamilie) zu laden.</span><span class="sxs-lookup"><span data-stu-id="07ef1-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="07ef1-p111">**Dateigröße**: Es gibt keine Einschränkung auf die Größe der Dateien in erweiterten eDiscovery geladen. Für die Analyse (analysieren, Relevanz usw.) ist die Grenze 5.242.880 extrahierten Textzeichen. Größere Dateien werden ignoriert (beispielsweise in Relevanz, Dateien der Relevanz Schulung Prozess nicht teilnehmen und erhalten Sie eine Bewertung Relevanz nicht nach Batch Berechnung).</span><span class="sxs-lookup"><span data-stu-id="07ef1-p111">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery. For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text. Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="07ef1-p112">**Datei Menge**: Es gibt keine empfohlene Höchstgrenze für die Anzahl der Dateien, die in einer einzelnen Fall behandelt werden kann. Leistung hängt von den Ressourcen des Systems.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p112">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case. Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="07ef1-145">Filtern von Dateien</span><span class="sxs-lookup"><span data-stu-id="07ef1-145">Filtering files</span></span>

<span data-ttu-id="07ef1-p113">Eine benutzerdefinierte Bezeichnung kann eine Reihe von Dateien, deren Prozess oder andere Aufgaben auszuschließende zugeordnet werden. Jede Sitzung Prozess ist eine Batch-ID zugeordnet Obwohl die Batch-ID nicht an den Experten in Relevanz angezeigt wird, kann dies mit einer Suchfunktion durch einen Filter für den aktuellen Batch hinzufügen, und markieren alle entsprechende Dateien mit einer benutzerdefinierten Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="07ef1-p113">A user-defined label can be associated with a set of files to exclude them from Process or other tasks. Each Process session is associated with a batch ID. Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07ef1-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07ef1-149">See also</span></span>

[<span data-ttu-id="07ef1-150">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="07ef1-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="07ef1-151">Das Prozess-Modul ausgeführt, und Laden von Daten</span><span class="sxs-lookup"><span data-stu-id="07ef1-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="07ef1-152">Anzeigen von Ergebnissen der Prozess Modul</span><span class="sxs-lookup"><span data-stu-id="07ef1-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

