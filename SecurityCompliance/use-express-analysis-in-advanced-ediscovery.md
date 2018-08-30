---
title: Verwenden Sie Analyse Express in Office 365 erweiterte eDiscovery
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Erfahren Sie, wie den Modus Express Analyse der Office 365 erweiterte eDiscovery ausführen
ms.openlocfilehash: a71e6775b1116e805e455815dca53a727d887809
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529315"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a><span data-ttu-id="9b922-103">Verwenden Sie Analyse Express in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9b922-103">Use Express Analysis in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="9b922-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="9b922-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="9b922-106">Sie können **Express Analysis** Sie schnell eine Anfrage zu analysieren und Exportieren der Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="9b922-106">You can use **Express analysis** to quickly analyze a case and export the results.</span></span> 
  
<span data-ttu-id="9b922-p102">Express-Analyse können Sie in der Nähe Duplikate berechnen und e-Mail-Threads und Designs zu berechnen. Sie können auch bestimmte Parameter für Designs, Dokument Ähnlichkeit und das Exportieren von Dateien in den [erweiterten Einstellungen für die Analyse Express](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings)festlegen.</span><span class="sxs-lookup"><span data-stu-id="9b922-p102">You can use express analysis to calculate near-duplicates and email threads and calculate themes. You can also set certain parameters for themes, document similarity and the export files in the [Advanced settings for Express analysis](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings).</span></span>
  
## <a name="run-express-analysis"></a><span data-ttu-id="9b922-109">Führen Sie Express-Analyse</span><span class="sxs-lookup"><span data-stu-id="9b922-109">Run Express analysis</span></span>

1. <span data-ttu-id="9b922-110">In der Registerkarte **Analyse Express** (1) Wählen Sie einen Container Aktivieren der ** Express Analysis ** (2), und Schaltflächen **Erweiterte Einstellungen** .</span><span class="sxs-lookup"><span data-stu-id="9b922-110">In the **Express analysis** (1) tab, select a container to enable the ** Express analysis ** (2), and **Advanced settings** buttons.</span></span> 
    
    ![Screenshot der Seite Analysis Express](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. <span data-ttu-id="9b922-112">Klicken Sie unter **Parameter analysieren**:</span><span class="sxs-lookup"><span data-stu-id="9b922-112">Under **Analyze parameters**:</span></span>
    
  - <span data-ttu-id="9b922-p103">Überprüfen Sie **in Ihrer Nähe Duplikate zu berechnen und e-Mail-Threads** , wenn Sie die Analyse ausführen möchten. Es ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9b922-p103">Check **Calculate near-duplicates and email threads** if you want to run the analysis. It is selected by default.</span></span> 
    
  - <span data-ttu-id="9b922-p104">Überprüfen Sie **Berechnen Designs** zur Verarbeitung aller Dateien und Designs zuweisen. Es ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9b922-p104">Check **Calculate Themes** to process all files and assign themes to them. It is selected by default.</span></span> 
    
3. <span data-ttu-id="9b922-117">Klicken Sie unter **Ziel für das Exportieren**:</span><span class="sxs-lookup"><span data-stu-id="9b922-117">Under **Export destination**:</span></span>
    
  - <span data-ttu-id="9b922-118">Überprüfen Sie **auf dem lokalen Computer herunterladen** , auf dem lokalen Computer herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="9b922-118">Check **Download to local machine** to download to your local computer.</span></span> 
    
  - <span data-ttu-id="9b922-119">Wenn Sie den **Export in Azure Blob benutzerdefinierte** aktivieren können Sie auch ein Container-URL und SAS-Token angeben.</span><span class="sxs-lookup"><span data-stu-id="9b922-119">If you check **Export to user-defined Azure blob** then you can also specify a container URL and SAS token.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="9b922-p105">Sobald ein Exportpaket zu gespeichert wurde die benutzerdefinierten Azure Blob, die Daten nicht mehr vom erweiterte eDiscovery verwaltet werden. Es wird von den Azure Blob verwaltet. Dies bedeutet, wenn Sie die Groß-/Kleinschreibung löschen, die exportierten Dateien weiterhin auf die Azure Blob verbleibt.</span><span class="sxs-lookup"><span data-stu-id="9b922-p105">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery. it is managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="9b922-123">**Token für zukünftige Export-Sitzung speichern SAS**: Wenn diese Einstellung aktiviert, wird das SAS-Token in der erweiterten eDiscovery interne Datenbank für die zukünftige Verwendung verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="9b922-123">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9b922-p106">Derzeit läuft ab das Token SAS nach Monat. Wenn Sie versuchen, die nach mehr als einem Monat herunterladen Sie die letzten Sitzung rückgängig zu machen müssen, exportieren Sie dann erneut.</span><span class="sxs-lookup"><span data-stu-id="9b922-p106">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
4. <span data-ttu-id="9b922-126">Die express Analyse mit Default starten zu Einstellungen, wählen Sie **Express Analyse**und die Seite **Aufgabenstatus** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9b922-126">To start the express analysis with default settings, choose **Express analysis**, and the **Task status** page will display</span></span> 
    
    <span data-ttu-id="9b922-127">Klicken Sie auf der Seite **Aufgabenstatus** können Sie die **Prozess**, **Analysieren** und **Exportieren von** Registerkarten zum Anzeigen von Details zu den express ausführen erweitern.</span><span class="sxs-lookup"><span data-stu-id="9b922-127">On the **Task status** page you can expand the **Process**, **Analyze** and **Export** tabs to display details about the express run.</span></span> 
    
    ![Screenshot der erweiterte eDiscovery Express Analysis Aufgabe Statusseite](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. <span data-ttu-id="9b922-129">Wählen Sie die Seite **Zusammenfassung Analysis Express** detaillierte Informationen über die Ausführung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="9b922-129">Choose the **Express analysis summary** page to list detailed information about the run.</span></span> 
    
    <span data-ttu-id="9b922-p107">Am unteren Rand der Seite **Zusammenfassung Analysis Express** wählen Sie in der **letzten Sitzung herunterladen** , dem Analyse Dateien Tp Ihrem lokalen Computer herunterladen. Sie müssen zuerst herunterladen eDiscovery-Export-Tool, und fügen Sie die Export-Taste, um das eDiscovery-Export-Tool.</span><span class="sxs-lookup"><span data-stu-id="9b922-p107">On the bottom of the **Express analysis summary** page, choose **Download last session** to download the analysis files tp your local computer. You will first have to download eDiscovery Export tool and paste the Export key to the eDiscovery Export tool.</span></span> 
    
## <a name="advanced-settings-for-express-analysis"></a><span data-ttu-id="9b922-132">Erweiterte Einstellungen für die Analyse Express</span><span class="sxs-lookup"><span data-stu-id="9b922-132">Advanced settings for Express analysis</span></span>
<span data-ttu-id="9b922-133"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="9b922-133"></span></span>

<span data-ttu-id="9b922-134">Sie können **Erweiterte Einstellungen** , so ändern Sie die Express-Analyse Standardparametern optional festlegen.</span><span class="sxs-lookup"><span data-stu-id="9b922-134">You can optionally set **Advanced settings** to change the default Express analysis parameters.</span></span> 
  
1. <span data-ttu-id="9b922-135">Im Abschnitt **Analysieren** :</span><span class="sxs-lookup"><span data-stu-id="9b922-135">In the **Analyze** section:</span></span> 
    
  - <span data-ttu-id="9b922-136">Geben Sie in der **in der Nähe von Duplikaten und e-Mail-Threads**den Wert **Dokument Ähnlichkeit** oder übernehmen Sie den Standardwert von 65 %.</span><span class="sxs-lookup"><span data-stu-id="9b922-136">In the **Near duplicates and email threads**, enter the **Document similarity** value, or accept the default of 65%.</span></span> 
    
  - <span data-ttu-id="9b922-p108">Die **maximale Anzahl von Designs** Geben Sie, oder wählen Sie einen Wert für die Anzahl der Designs zu erstellen. Der Standardwert ist 200.</span><span class="sxs-lookup"><span data-stu-id="9b922-p108">In the **Max number of themes** enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="9b922-p109">Erhöhung der Anzahl der Designs wirkt sich auf Leistung als auch die Möglichkeit eines Designs, verallgemeinern. Je höher die Anzahl der Designs, die eine genauere sind. Beispielsweise, wenn eine Reihe von 50 Designs ein Design wie "Basketball, beleben, geschoren Lakers" enthalten 300 Designs separate Designs enthalten können: "Beleben", "Geschoren", "Lakers". Wenn Sie keine zur Förderung des Bekanntheitsgrads des Designs "Basketball" hatte und verwenden Sie diese Funktion für ECA, konnte das Design anzeigen "Basketball" nützlich sein. Wenn die Verarbeitung zu viele Designs hatten, Sie jedoch möglicherweise noch nie das Wort "Basketball" angezeigt und können nicht kennen, beleben und geschoren gute Basketball Designs sind, um zu prüfen, anstatt Elemente, die auf startet und für haarstrich verwendet.</span><span class="sxs-lookup"><span data-stu-id="9b922-p109">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
  - <span data-ttu-id="9b922-p110">Wählen Sie in der **vorgeschlagene Designs** **Ändern** zum Vorschlagen des Designs Wörter zum Steuern der Verarbeitung Designs aus. Erweiterte eDiscovery wird den Schwerpunkt auf folgenden vorgeschlagenen Wörter und versuchen, eine oder mehrere relevante Designs, basierend auf der Einstellung "Maximale Anzahl der Designs" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9b922-p110">In the **Suggested themes** choose **Modify** to suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="9b922-p111">Beispielsweise wird das vorgeschlagene Wort "Computer", und Sie als die "maximale Anzahl der Designs" "2" angegeben, erweiterte eDiscovery versuchen, zwei Designs zu generieren, die sich auf das Wort "Computer" beziehen. Zwei Designs können beispielsweise "Computersoftware" und "Computerhardware" sein.</span><span class="sxs-lookup"><span data-stu-id="9b922-p111">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span>
    
    ![Vorgeschlagenes Design hinzufügen](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - <span data-ttu-id="9b922-149">**Modus** Wählen Sie aus der Dropdownliste ein **Designs** -Option aus:</span><span class="sxs-lookup"><span data-stu-id="9b922-149">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="9b922-150">**Erstellen und Anwenden von Modell**: berechnet Designs von Modellen aus einem Segment der Dateien und dann verteilt zwischen diesen Dateien.</span><span class="sxs-lookup"><span data-stu-id="9b922-150">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="9b922-p112">**Create-Modell**: ein Designs-Modell aus einem Segment der Dateien berechnet. Der übernehmen Prozess der Division von Dateien ist separat zu einem späteren Zeitpunkt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9b922-p112">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="9b922-p113">**Apply-Modell**: Diese Option wird nur angezeigt, wenn ein Modell wurde bereits zuvor erstellt und noch nicht angewendet. Dadurch werden die Dateien basierend auf der Designs dividiert.</span><span class="sxs-lookup"><span data-stu-id="9b922-p113">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
2. <span data-ttu-id="9b922-155">Im Abschnitt **Exportieren** :</span><span class="sxs-lookup"><span data-stu-id="9b922-155">In the **Export** section:</span></span> 
    
1. <span data-ttu-id="9b922-156">In den **Batch wählen Sie exportieren**:</span><span class="sxs-lookup"><span data-stu-id="9b922-156">In the **Select export batch**:</span></span>
    
  - <span data-ttu-id="9b922-157">Aus der Liste **Exportieren Batch** wählen den Blattnamen oder Exportieren von Ergebnissen in Export Batch 01 (Standard).</span><span class="sxs-lookup"><span data-stu-id="9b922-157">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="9b922-p114">Um Ergebnisse für neue Dateien zu exportieren, die Sie einer vorhandenen Anfrage hinzugefügt haben, fahren Sie mit Ihren aktuellen Stapel. Zum Erstellen einer Sitzung im Batch, wählen Sie die gleiche Anzahl von Batch aus, und klicken Sie auf **Create Session exportieren** können Sie diese Option verwenden, so exportieren Sie die gleichen Parameter als den vorherigen Batch eine inkrementelle Weise.</span><span class="sxs-lookup"><span data-stu-id="9b922-p114">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="9b922-p115">Klicken Sie auf **Hinzufügen**, um einen neuen Batch zu exportieren,![Symbol hinzufügen](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) und geben Sie einen neuen Namen in **Blattname** (oder übernehmen Sie den Standardwert) und eine Beschreibung im **Feld Beschreibung Batch**. Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9b922-p115">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="9b922-162">Um einen Namen oder die Beschreibung zu bearbeiten, wählen Sie den Namen im **Batch exportieren**, klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), und klicken Sie dann die Felder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9b922-162">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9b922-p116">Nach dem Ausführen Sitzungen für einen Batch Export können sie gelöscht werden. Darüber hinaus können nur einige Parameter bearbeitet werden, sobald die erste Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9b922-p116">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="9b922-165">Wählen Sie zum Erstellen eines Batches für die doppelte Export **Duplikat Export Batch**![doppelte Export Batch-Symbol erstellen](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) , und geben Sie einen Namen und eine Beschreibung für den doppelten Batch in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="9b922-165">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="9b922-166">Wählen Sie zum Löschen eines Batches Export **Löschen**![löschen Symbolgröße Batch Export](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span><span class="sxs-lookup"><span data-stu-id="9b922-166">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="9b922-167">Wählen Sie zum Anzeigen des Verlaufs eines Batches **Batch Verlauf**![Ansicht Verlauf Symbol](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span><span class="sxs-lookup"><span data-stu-id="9b922-167">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="9b922-p117">Klicken Sie unter Define p **Opulation:** **Includedateien nur über Relevanz Grenzwert Score** und/oder **verfeinern Export Batch** wählen, wenn Sie die Einstellungen für Ihren Export-Stapel optimieren möchten. Wenn Sie **nur Dateien über Relevanz Grenzwert Score einschließen**ausgewählt haben, klicken Sie dann das **Problem** ist aktiviert, und wenn die Datei Relevanz Score höher ist als die Bewertung Grenzwert für das ausgewählte Problem ist, klicken Sie dann die Datei wird exportiert. Die Datei exportiert werden, es sei denn, es von ausgeschlossen ist die ' **zur Prüfung** Filter. Bei Auswahl von **verfeinern Export Batch**, und klicken Sie dann die **Deduplizierung** und **Filter von 'Zur Überprüfung' Feld** Optionsfelder aktiviert sind. Falls gewünscht **Deduplizierung**, und klicken Sie dann Duplikate Dateien gefiltert gemäß der Richtlinie definierten skalierten werden werden: [Case-Ebene (Standard): aus jeder Gruppe von duplizierten Dateien in der gesamten Groß-/Kleinschreibung, alle jedoch eine Datei Aufhebung der duped werden soll. Verwaltungsberechtigter Ebene: aus jeder Gruppe von duplizierten Dateien von der gleichen Verwaltungsberechtigte, alle jedoch eine Datei Aufhebung der duped werden soll. Eine Aufzeichnung aller duplizierten Dateien ist Export Ausgabe verfügbar. Wenn Sie **von 'zur Prüfung"** Filterfeld auswählen, wählen Sie **ändern unter Metadaten** Geben Sie Ihre Einstellungen **'zur Prüfung"** dar. Wählen Sie **input Includedateien**Quelldateien im Paketinhalt enthalten. Deaktivieren Sie diese Option, um den Exportvorgang zu beschleunigen. Beachten Sie, dass die systemeigenen Dateien in jedem Fall exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b922-p117">Under Define p **opulation:** Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch. If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled, and if the file's relevance score is higher than the cut-off score for the selected issue, then the file is exported. The file will be exported unless it's excluded by the ' **For review** filter. If you select **Refine export batch**, then the **De-dupe** and **Filter by 'For review' field** radio buttons are enabled. If you choose **De-dupe**, then duplicates files will be filtered-out according to the policy defined: [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped. A record of all duplicate files is available in export output. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files**to include source files in the package content. You can clear this option to speed up the export process. Note that the Native files will be exported in any case.</span></span>
    
3. <span data-ttu-id="9b922-179">Wählen Sie unter **Define Metadaten**aus den folgenden Optionen in der Liste **Vorlage exportieren** (einmal pro Sitzung).</span><span class="sxs-lookup"><span data-stu-id="9b922-179">Under **Define metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="9b922-p118">**Standard**: grundlegende Satz von Datenelemente, Metadaten und Eigenschaften. Verwenden Sie diese Option aus, wenn Daten importieren bereits im erweiterten eDiscovery verarbeitet wurde und Exportieren von Daten an ein System, das bereits die Dateien enthält hochgeladen. Exportieren Sie standardmäßig Vorlage Spalten erstellt und aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="9b922-p118">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="9b922-p119">**Alle**: umfassende Auswahl an standard-Metadaten sowie alle Verarbeiten von Daten, analysieren und Relevanz Bewertungen. Diese Vorlage ist erforderlich, wenn erweiterte eDiscovery die Verarbeitung führt und Dateidaten werden zum ersten Mal mit einem externen System hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="9b922-p119">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="9b922-185">**Probleme**: Wählen Sie **Alle Probleme** oder ein bestimmtes Problem, das Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="9b922-185">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
<span data-ttu-id="9b922-186">Wählen Sie **OK**um die erweiterten Einstellungen zu speichern, verwenden Sie die Standardwerte **Wiederherstellen** oder **Abbrechen** , um den erweiterten Einstellungen festlegen Abbrechen.</span><span class="sxs-lookup"><span data-stu-id="9b922-186">Choose **OK**to save the advanced settings, **Restore defaults** to use default values, or **Cancel** to cancel setting the advanced settings.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9b922-187">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9b922-187">See also</span></span>
<span data-ttu-id="9b922-188"><a name="BK_AdvancedSettings"> </a></span><span class="sxs-lookup"><span data-stu-id="9b922-188"></span></span>

[<span data-ttu-id="9b922-189">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9b922-189">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)

