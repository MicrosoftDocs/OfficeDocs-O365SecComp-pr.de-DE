---
title: Ausführen des Prozessmoduls in Office 365 Advanced eDiscovery
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
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30216115"
---
# <a name="run-the-process-module-in-office-365-advanced-ediscovery"></a><span data-ttu-id="ab066-103">Ausführen des Prozessmoduls in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ab066-103">Run the Process module in Office 365 Advanced eDiscovery</span></span>

<span data-ttu-id="ab066-104">Fall Dateien werden während des **Prepare** \> - **Vorgangs**in die erweiterte eDiscovery geladen.</span><span class="sxs-lookup"><span data-stu-id="ab066-104">Case files are loaded into the Advanced eDiscovery during **Prepare** \> **Process**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ab066-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="ab066-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="guidelines-preparing-data-for-advanced-ediscovery"></a><span data-ttu-id="ab066-107">Richtlinien: Vorbereiten von Daten für Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ab066-107">Guidelines: Preparing data for Advanced eDiscovery</span></span>

- <span data-ttu-id="ab066-108">**Qualität**: identifizieren Sie eindeutig die für den Fall relevante Datei Auffüllung.</span><span class="sxs-lookup"><span data-stu-id="ab066-108">**Quality**: Clearly identify the case file population pertinent to the case.</span></span>
    
- <span data-ttu-id="ab066-109">**Lasten**: Laden Sie die Dateien an einen Speicherort, auf den Advanced eDiscovery zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ab066-109">**Loads**: Load the files into a location that is accessible to Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="ab066-p102">**Datei-ID**: ein eindeutiger Dateibezeichner in Advanced eDiscovery. Wenn kein Dateibezeichner importiert wird, generiert Advanced eDiscovery automatisch die ID. Wenn Sie die ID in einem nachfolgenden Prozess laden zuordnen und einen anderen Pfad als bei der anfänglichen Prozessauslastung zuordnen, wird der Pfad von Advanced eDiscovery ersetzt (statt einen neuen Dateieintrag hinzuzufügen). Die ID kann als Referenz im Export Prozess verwendet werden. Der ID-Wert sollte nicht "-1" lauten.</span><span class="sxs-lookup"><span data-stu-id="ab066-p102">**File ID**: A unique file identifier in Advanced eDiscovery. If no file identifier is imported, Advanced eDiscovery automatically generates the ID. If you map the ID in a subsequent Process load, and map a different path than in the initial Process load, Advanced eDiscovery will replace the path (rather than add a new file entry). The ID can be used as a reference in the Export process. The ID value should not be "-1".</span></span>
    
- <span data-ttu-id="ab066-p103">**MD5**: Diese Signatur wird verwendet, um zwischen Dateien zu unterscheiden (zwei Dateien werden nicht als exakte Duplikate betrachtet, es sei denn, Sie haben den gleichen MD5). Standardmäßig berechnet Advanced eDiscovery die MD5-Dateien. Wenn es sich bei den geladenen Dateien um Textdateien handelt, wird empfohlen, den ursprünglichen MD5-Wert zu laden und zu zuordnen, statt ihn in Advanced eDiscovery zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ab066-p103">**MD5**: This signature is used to differentiate between files (two files are not considered exact duplicates unless they have the same MD5). By default, Advanced eDiscovery calculates the MD5 of files. When the loaded files are text files, it is recommended to load and map the original MD5 value instead of calculating it in Advanced eDiscovery.</span></span>
    
- <span data-ttu-id="ab066-118">**Dateityp und Name**:</span><span class="sxs-lookup"><span data-stu-id="ab066-118">**File type and name**:</span></span>
    
  - <span data-ttu-id="ab066-p104">Advanced eDiscovery kann Dateien mit verschiedenen Formaten verarbeiten und geladene systemeigene Dateien in ein Standardformat wie \*. TXT, HTML oder. XML. processing von Textdateien ist schneller als systemeigene Dateien. Extrahierte Textdateien werden im Case-Ordner gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ab066-p104">Advanced eDiscovery can process files of various formats and extract loaded native files into a standard format, such as \*.TXT, HTML, or .XML. Processing of text files is faster than native files. Extracted text files are stored in the case folder.</span></span>
    
  - <span data-ttu-id="ab066-p105">Laden Sie keine Dateien, die nicht extrahiert werden können, wie Systemdateien oder Grafik Bilder nicht. Diese Dateien können die Verarbeitung verzögern.</span><span class="sxs-lookup"><span data-stu-id="ab066-p105">Do not load files that cannot be extracted, such as system files or graphic images. These files may delay processing.</span></span>
    
  - <span data-ttu-id="ab066-124">Stellen Sie sicher, dass die Dateinamen bedeutend benannt werden und die Pfade korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="ab066-124">Verify that file names are significantly named and paths are correct.</span></span>
    
- <span data-ttu-id="ab066-125">\*\*\*\* Dateipfad: Advanced eDiscovery kann Dateien mit Pfad Längen von bis zu 400 Zeichen laden.</span><span class="sxs-lookup"><span data-stu-id="ab066-125">**File path**: Advanced eDiscovery can load files with path lengths up to 400 characters.</span></span>
    
- <span data-ttu-id="ab066-p106">**Textextraktion**: beim Extrahieren von Text aus systemeigenen Dateien werden zusätzlich zu normalem Text auch folgende Elemente extrahiert: ausgeblendeter Text (Excel und doc), ausgeblendete Spalten (Excel), Nachverfolgen von Änderungen (. doc), Vortragsnotizen (PPT), eingebettete Objekte (beispielsweise Excel-Objekte in a. ppt). Diese können im Text-Editor angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ab066-p106">**Text extraction**: When extracting text from native files, in addition to normal text, the following are also extracted: hidden text (Excel and .doc), hidden columns (Excel), track changes (.doc), speaker notes (.ppt), embedded objects (for example, Excel objects in a .ppt). These can be viewed in the Text editor.</span></span>
    
- <span data-ttu-id="ab066-p107">**Text ignorieren**: dieses optionale Feature wird definiert, nachdem der Prozess ausgeführt und analysiert wurde. Ignore Text sollte mit Bedacht verwendet werden, da seine Verwendung die Leistung der Dateianalyse reduzieren kann.</span><span class="sxs-lookup"><span data-stu-id="ab066-p107">**Ignore Text**: This optional feature is defined after Process is run and before Analyze. Ignore text should be used with caution because its use may reduce the performance of file analysis.</span></span>
    
- <span data-ttu-id="ab066-130">**Mehrsprachiger Text**: Erweiterte eDiscovery verwendet derzeit keine mehrsprachigen Namen für Tags, Verwalter und Probleme.</span><span class="sxs-lookup"><span data-stu-id="ab066-130">**Multilingual text**: Advanced eDiscovery does not currently handle multilingual names for tags, custodian, and issues.</span></span>
    
- <span data-ttu-id="ab066-p108">**Metadaten**: bestimmen Sie, ob es sich bei Metadaten, die Sie in der falldatenbank speichern möchten, um zukünftige Referenzen wie Datumsbereich, Dateigröße, Dateityp, Depotbank und Betreff gibt. Metadaten können geladen werden, nachdem Dateien bereits geladen wurden, ohne das Inventar erneut auszuführen oder den Aufwand für die erneute Verarbeitung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ab066-p108">**Metadata**: Determine if there is metadata that you want to save in the case database for future reference, such as date range, file size, file type, custodian, and subject. Metadata can be loaded after files were already loaded without rerunning the inventory or adding reprocessing overhead.</span></span> 
    
  - <span data-ttu-id="ab066-p109">Wenn die Dateien ursprünglich über den Pfad geladen wurden, ordnen Sie die Spalte path beim späteren Importieren von Metadaten zu. Sie können auf die Datei anhand der ID verweisen und einen anderen Pfad zuordnen. Dies ist ein nützliches Szenario, wenn sich die Dateipfade ändern.</span><span class="sxs-lookup"><span data-stu-id="ab066-p109">If the files were originally loaded by path, map the path column when later importing metadata. It is possible to refer to the file by ID and to map a different path. This is a useful scenario when the file paths change.</span></span>
    
  - <span data-ttu-id="ab066-p110">Wenn die Dateien ursprünglich mit der Datei-ID geladen wurden, ordnen Sie die ID-Spalte beim Laden von Metadaten zu. Wenn Sie auf die Datei nach Pfad (anstelle von ID) verweisen, werden Dateien mit einer anderen ID erneut geladen. Erweiterte eDiscovery erstellt Kopien der Dateien, statt die Metadaten der vorhandenen Dateien zu laden.</span><span class="sxs-lookup"><span data-stu-id="ab066-p110">If the files were originally loaded by File ID, map the ID column when loading metadata. Referring to the file by path (instead of ID) will cause files to be re-loaded with a different ID. Advanced eDiscovery creates copies of the files rather that loading metadata of the existing files.</span></span>
    
- <span data-ttu-id="ab066-139">**Familien**: Es ist nicht möglich, eine Familie ohne das übergeordnete Element (Familienoberhaupt) zu laden.</span><span class="sxs-lookup"><span data-stu-id="ab066-139">**Families**: It is not possible to load a family without its parent (head of family).</span></span> 
    
- <span data-ttu-id="ab066-p111">**Dateigröße**: Es gibt keine Beschränkung für die Größe der Dateien, die in Advanced eDiscovery geladen wurden. Für Analysen (analysieren, Relevanz usw.) beträgt die Grenze 5.242.880 Zeichen des extrahierten Texts. Größere Dateien werden ignoriert (beispielsweise in Relevanz, Dateien nehmen nicht am Relevanz-Schulungsprozess Teil und erhalten nach der Batch Berechnung kein Relevanz-Ergebnis).</span><span class="sxs-lookup"><span data-stu-id="ab066-p111">**File size**: There is no limitation on the size of files loaded to Advanced eDiscovery. For analysis (Analyze, Relevance, etc.), the limit is 5,242,880 characters of extracted text. Larger files are ignored (for example, in Relevance, files do not participate in the Relevance training process and do not receive a Relevance score after batch calculation).</span></span>
    
- <span data-ttu-id="ab066-p112">**Datei Menge**: Es wird kein Grenzwert für die Anzahl der Dateien empfohlen, die in einem einzelnen Fall verarbeitet werden können. Die Leistung hängt von den Ressourcen Ihres Systems ab.</span><span class="sxs-lookup"><span data-stu-id="ab066-p112">**File quantity**: There is no recommended limit on the number of files that can be handled in a single case. Performance depends on the resources of your system.</span></span> 
    
## <a name="filtering-files"></a><span data-ttu-id="ab066-145">Filtern von Dateien</span><span class="sxs-lookup"><span data-stu-id="ab066-145">Filtering files</span></span>

<span data-ttu-id="ab066-p113">Eine benutzerdefinierte Bezeichnung kann mit einer Reihe von Dateien verknüpft werden, um Sie von Prozess-oder anderen Aufgaben auszuschließen. Jeder Prozess Sitzung ist eine Batch-ID zugeordnet. Obwohl die Batch-ID für den Experten nicht relevant ist, kann dies mithilfe eines Such Dienstprogramms erfolgen, indem ein Filter für den aktuellen Batch hinzugefügt wird und alle entsprechenden Dateien mit einer benutzerdefinierten Bezeichnung gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ab066-p113">A user-defined label can be associated with a set of files to exclude them from Process or other tasks. Each Process session is associated with a batch ID. Although the batch ID is not visible to the expert in Relevance, this can be done using a search utility, by adding a filter for the current batch and tagging all appropriate files with a user-defined label.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ab066-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab066-149">See also</span></span>

[<span data-ttu-id="ab066-150">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="ab066-150">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="ab066-151">Prozessmodul wird ausgeführt und Daten geladen</span><span class="sxs-lookup"><span data-stu-id="ab066-151">Running the Process module and loading data</span></span>](run-the-process-module-and-load-data-in-advanced-ediscovery.md)
  
[<span data-ttu-id="ab066-152">Anzeigen der Ergebnisse des Prozess Moduls</span><span class="sxs-lookup"><span data-stu-id="ab066-152">Viewing Process module results</span></span>](view-process-module-results-in-advanced-ediscovery.md)

