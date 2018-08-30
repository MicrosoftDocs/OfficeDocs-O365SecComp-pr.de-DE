---
title: Exportieren von Ergebnissen in Office 365 erweiterte eDiscovery
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
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Hier erfahren Sie, wie Sie Optionen für den Export von Ergebnissen aus Office 365 erweiterte eDiscovery, einschließlich des Verfahrens zum Angeben der Parameter für einen Batch Export definieren. '
ms.openlocfilehash: 92ee107ad096393fbccbc9a3dbe81d8e7dd28da9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530043"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a><span data-ttu-id="9deb5-103">Exportieren von Ergebnissen in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9deb5-103">Export results in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="9deb5-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="9deb5-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="9deb5-106">In diesem Thema werden die erweiterten eDiscovery exportieren Setupoptionen.</span><span class="sxs-lookup"><span data-stu-id="9deb5-106">This topic describes the Advanced eDiscovery Export Setup options.</span></span>
  
 <span data-ttu-id="9deb5-107">**Inhalt dieses Themas:**</span><span class="sxs-lookup"><span data-stu-id="9deb5-107">**In this topic:**</span></span>
  
- [<span data-ttu-id="9deb5-108">Definieren von Export Batches und Sitzungen</span><span class="sxs-lookup"><span data-stu-id="9deb5-108">Defining export batches and sessions</span></span>](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [<span data-ttu-id="9deb5-109">Inkrementelle und zusätzliche Exporte</span><span class="sxs-lookup"><span data-stu-id="9deb5-109">Incremental and additional exports</span></span>](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [<span data-ttu-id="9deb5-110">Einrichten von Batch Export-Parameter</span><span class="sxs-lookup"><span data-stu-id="9deb5-110">Set up batch export parameters</span></span>](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [<span data-ttu-id="9deb5-111">Exportieren von Ausgabedateien Bericht</span><span class="sxs-lookup"><span data-stu-id="9deb5-111">Export report output files</span></span>](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a><span data-ttu-id="9deb5-112">Definieren von Export Batches und Sitzungen</span><span class="sxs-lookup"><span data-stu-id="9deb5-112">Defining export batches and sessions</span></span>
<span data-ttu-id="9deb5-113"><a name="BK_Define"> </a></span><span class="sxs-lookup"><span data-stu-id="9deb5-113"></span></span>

<span data-ttu-id="9deb5-p102">Ein Export Batch ermöglicht Exportvorgang mithilfe einer Reihe von definierten Parameter. Erweiterte eDiscovery können Sie Batches zum Anpassen der einzelnen Export definieren.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p102">An export batch allows export processing using a set of defined parameters. Advanced eDiscovery enables you to define batches to customize each export.</span></span>
  
<span data-ttu-id="9deb5-p103">Parameter werden pro Export Batch definiert. In der Standardeinstellung für den ersten Batch einer Anfrage wird ein Batches mit dem Namen "Exportieren Batch 01" erstellt. Sie können auch den Namen und die Beschreibung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p103">Parameters are defined per export batch. A batch named "Export batch 01" is created by default for the first batch of a case. You can also edit the batch name and description.</span></span>
  
<span data-ttu-id="9deb5-119">Eine Export-Sitzung ist Ausführung des erweiterten eDiscovery-Export innerhalb eines Batches exportieren.</span><span class="sxs-lookup"><span data-stu-id="9deb5-119">An export session is an execution of Advanced eDiscovery Export within an export batch.</span></span>
  
## <a name="incremental-and-additional-exports"></a><span data-ttu-id="9deb5-120">Inkrementelle und zusätzliche Exporte</span><span class="sxs-lookup"><span data-stu-id="9deb5-120">Incremental and additional exports</span></span>
<span data-ttu-id="9deb5-121"><a name="BK_IncrementalReports"> </a></span><span class="sxs-lookup"><span data-stu-id="9deb5-121"></span></span>

<span data-ttu-id="9deb5-p104">Sie können mehrere Export Sitzungen innerhalb eines Batches exportieren, um sicherzustellen, dass übereinstimmende Ergebnisse basierend auf dem gleichen Exportvorlage und Parameter ausführen. Für jede Sitzung in einem Batch können Sie Analytics exportieren, neu Groß-/Kleinschreibung Daten verarbeitet und Verarbeiten von jeweils "inkrementell".</span><span class="sxs-lookup"><span data-stu-id="9deb5-p104">You can run multiple export sessions within an export batch, to ensure consistent results based on the same export template and parameters. For each session within a batch, you can export analytics for newly processed case data and process each "incrementally."</span></span>
  
<span data-ttu-id="9deb5-p105">Um mit anderen Parametern zu exportieren, müssen Sie zuerst einen neuen Batch zu erstellen. Die erste Sitzung in das neue Blatt erzeugt Ergebnisse für Dateien verarbeitet im Fall bisher, unabhängig davon, ob diese Dateien importiert und über eine oder mehrere Imports verarbeitet wurden. Jedem Batch wird die Pivot-Elemente, Ähnlichkeit, Inclusives neu berechnet. Sitzungen verwenden Sie die Parameter für den Batch definiert und nicht neu berechnet Pivot-Elemente, Ähnlichkeit, Inclusives usw. für jede Sitzung Ausführung.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p105">In order to export using a different set of parameters, you first need to create a new batch. The first session in the new batch will produce results for files processed in the case so far, whether or not these files were imported and processed over one or multiple Imports. Each batch recalculates pivots, similarity, inclusives, etc. Sessions use the parameters defined for the batch and do not recalculate pivots, similarity, inclusives, etc. for each session execution.</span></span>
  
<span data-ttu-id="9deb5-p106">Nehmen wir beispielsweise an eine Anfrage importiert wurde, und seine Daten analysiert. Um in der Nähe Duplikate und Threading-e-Mail-Ergebnisse für die inkrementellen Daten abzurufen, klicken Sie auf **Create Session exportieren** im selben Batch, der zuvor zum Exportieren von Daten verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p106">For example, assume a case was imported and its data analyzed. In order to retrieve Near-duplicates and Email Threading results for the incremental data, click **Create export session** in the same batch that was previously used to export data.</span></span> 
  
## <a name="set-up-batch-export-parameters"></a><span data-ttu-id="9deb5-129">Einrichten von Batch Export-Parameter</span><span class="sxs-lookup"><span data-stu-id="9deb5-129">Set up batch export parameters</span></span>
<span data-ttu-id="9deb5-130"><a name="BK_SetUpExport"> </a></span><span class="sxs-lookup"><span data-stu-id="9deb5-130"></span></span>

<span data-ttu-id="9deb5-p107">Die eDiscovery-Exporttool wird verwendet, um Suchergebnisse aus erweiterte eDiscovery auf Ihrem lokalen Computer zu exportieren. Um die Daten Übertragungsdurchsatz und beschleunigen der Exportvorgang erhöhen möchten, können Sie eine Einstellung für die Windows-Registrierung auf dem Computer konfigurieren, mit denen Sie die Suchergebnisse exportieren. Wenn Sie die Download-Geschwindigkeit erhöhen möchten, konfigurieren Sie die Einstellung der Registrierung, bevor Sie die Exportparameter einrichten. Weitere Informationen finden Sie unter [erhöhen die Geschwindigkeit Download beim Exportieren von eDiscovery-Suchergebnisse aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span><span class="sxs-lookup"><span data-stu-id="9deb5-p107">The eDiscovery Export Tool is used to export search results from Advanced eDiscovery to your local computer. To increase the data transfer throughput and speed-up the export process, you can configure a Windows Registry setting on the computer that you use to export the search results. If you'd like to increase the download speed, configure the registry setting before you set up the export parameters. For more information, see [Increase the download speed when exporting eDiscovery search results from Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).</span></span>
  
1. <span data-ttu-id="9deb5-135">Wählen Sie eine Anfrage im erweiterte eDiscovery, und klicken Sie auf **Exportieren** \> **Setup**.</span><span class="sxs-lookup"><span data-stu-id="9deb5-135">In Advanced eDiscovery, select a Case and click **Export** \> **Setup**.</span></span>
    
  - <span data-ttu-id="9deb5-136">Aus der Liste **Exportieren Batch** wählen den Blattnamen oder Exportieren von Ergebnissen in Export Batch 01 (Standard).</span><span class="sxs-lookup"><span data-stu-id="9deb5-136">From the **Export batch** list, select the batch name or export results to Export batch 01, (the default batch).</span></span> 
    
  - <span data-ttu-id="9deb5-p108">Um Ergebnisse für neue Dateien zu exportieren, die Sie einer vorhandenen Anfrage hinzugefügt haben, fahren Sie mit Ihren aktuellen Stapel. Zum Erstellen einer Sitzung im Batch, wählen Sie die gleiche Anzahl von Batch aus, und klicken Sie auf **Create Session exportieren** können Sie diese Option verwenden, so exportieren Sie die gleichen Parameter als den vorherigen Batch eine inkrementelle Weise.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p108">To export results for new files that you added to an existing case, continue with your current batch. To create a session in the batch, select the same batch number and click **Create export session** You can use this option to export the same parameters as the previous batch, in an incremental manner.</span></span> 
    
  - <span data-ttu-id="9deb5-p109">Klicken Sie auf **Hinzufügen**, um einen neuen Batch zu exportieren,![Symbol hinzufügen](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)und geben Sie einen neuen Namen in **Blattname** (oder übernehmen Sie den Standardwert) und eine Beschreibung im **Feld Beschreibung Batch**. Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p109">To export to a new batch, click **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)and enter a new name in **Batch name** (or accept the default) and a description in **Batch description**. Click **OK**.</span></span>
    
  - <span data-ttu-id="9deb5-141">Um einen Namen oder die Beschreibung zu bearbeiten, wählen Sie den Namen im **Batch exportieren**, klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), und klicken Sie dann die Felder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9deb5-141">To edit a batch name or description, select the name in **Export batch**, click **Edit** ![Edit icon](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), and then modify the fields.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9deb5-p110">Nach dem Ausführen Sitzungen für einen Batch Export können sie gelöscht werden. Darüber hinaus können nur einige Parameter bearbeitet werden, sobald die erste Sitzung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p110">After you've run sessions for an export batch, they cannot be deleted. In addition, only some parameters can be edited once the first session is run.</span></span> 
  
  - <span data-ttu-id="9deb5-144">Wählen Sie zum Erstellen eines Batches für die doppelte Export **Duplikat Export Batch**![doppelte Export Batch-Symbol erstellen](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) , und geben Sie einen Namen und eine Beschreibung für den doppelten Batch in der Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="9deb5-144">To create a duplicate export batch, choose **Duplicate export batch**![Create a duplicate export batch icon](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) and enter a name and a description for the duplicate batch in the panel.</span></span> 
    
  - <span data-ttu-id="9deb5-145">Wählen Sie zum Löschen eines Batches Export **Löschen**![löschen Symbolgröße Batch Export](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span><span class="sxs-lookup"><span data-stu-id="9deb5-145">To delete an export batch, choose **Delete**![Delete an export batch icon](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).</span></span>
    
  - <span data-ttu-id="9deb5-146">Wählen Sie zum Anzeigen des Verlaufs eines Batches **Batch Verlauf**![Ansicht Verlauf Symbol](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span><span class="sxs-lookup"><span data-stu-id="9deb5-146">To view the history of a batch, choose **Batch history**![View history icon](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).</span></span>
    
2. <span data-ttu-id="9deb5-147">Wählen Sie unter **Auffüllung** **Includedateien nur über Relevanz Grenzwert Score** und/oder **verfeinern Export Batch** , wenn Sie die Einstellungen für Ihren Export-Stapel optimieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9deb5-147">Under **Population**,Select **Include only files above Relevance cut-off score** and/or **Refine export batch** if you want to fine-tune the settings for your export batch.</span></span> 
    
3. <span data-ttu-id="9deb5-p111">Wenn Sie **nur Dateien über Relevanz Grenzwert Score einschließen**ausgewählt haben, ist das **Problem** aktiviert. Wenn die Datei Relevanz Score höher ist als die Bewertung Grenzwert für das ausgewählte Problem ist, wird die Datei exportiert werden, wenn es vom Filter "zur Prüfung" ausgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p111">If you select **Include only files above Relevance cut-off score**, then the **Issue** is enabled. If the file's relevance score is higher than the cut-off score for the selected issue, the file will be exported unless it's excluded by the 'For review' filter.</span></span> 
  
<span data-ttu-id="9deb5-p112">Bei Auswahl von **verfeinern Export Batch**, die **Deduplizierung** und Filter von 'Zur Überprüfung' Feld Optionsfelder aktiviert sind. Bei Auswahl von **Deduplizierung**, und klicken Sie dann duplizierte Dateien gemäß der Richtlinie definierten herausgefiltert [Case-Ebene (Standard): aus jeder Gruppe von duplizierten Dateien in der gesamten Groß-/Kleinschreibung, alle jedoch eine Datei Aufhebung der duped werden soll. Verwaltungsberechtigter Ebene: aus jeder Gruppe von duplizierten Dateien von der gleichen Verwaltungsberechtigte, werden alle jedoch eine Datei Aufhebung der duped werden.] Die Export-Ausgabe enthält einen Datensatz für alle duplizierten Dateien. Wenn Sie **von 'zur Prüfung"** Filterfeld auswählen, wählen Sie **ändern unter Metadaten** Geben Sie Ihre Einstellungen **'zur Prüfung"** dar. Wählen Sie **input Includedateien** Quelldateien im Paketinhalt enthalten. Deaktivieren Sie diese Einstellung, um den Exportvorgang zu beschleunigen. Beachten Sie, dass die systemeigenen Dateien in jedem Fall exportiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p112">If you select **Refine export batch**, the **De-dupe** and Filter by 'For review' field radio buttons are enabled. If you choose **De-dupe**, then duplicate files will be filtered out according to the policy defined [Case level (default): from every set of duplicate files in the entire case, all but one file will be de-duped. Custodian level: from every set of duplicate files of the same custodian, all but one file will be de-duped.] The export output contains a record of all duplicate files. If you choose **Filter by 'For review'** field, select **Modify under Metadata** to enter your **'For review'** field settings. Select **Include input files** to include source files in the package content. You can clear this setting to speed up the export process. Note that the Native files will be exported in any case.</span></span> 
    
4. <span data-ttu-id="9deb5-157">Wählen Sie unter **Metadaten**aus der folgenden Optionen in der Liste **Vorlage exportieren** (einmal pro Sitzung).</span><span class="sxs-lookup"><span data-stu-id="9deb5-157">Under **Metadata**, select from the following options in the **Export template** list (once per session).</span></span> 
    
  - <span data-ttu-id="9deb5-p113">**Standard**: grundlegende Satz von Datenelemente, Metadaten und Eigenschaften. Verwenden Sie diese Option aus, wenn Daten importieren bereits im erweiterten eDiscovery verarbeitet wurde und Exportieren von Daten an ein System, das bereits die Dateien enthält hochgeladen. Exportieren Sie standardmäßig Vorlage Spalten erstellt und aufgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p113">**Standard**: Basic set of data items, metadata, and properties. Use this option when import data was already processed in Advanced eDiscovery and export data is uploaded to a system that already contains the files. By default, export template columns are created and filled.</span></span>
    
  - <span data-ttu-id="9deb5-p114">**Alle**: umfassende Auswahl an standard-Metadaten sowie alle Verarbeiten von Daten, analysieren und Relevanz Bewertungen. Diese Vorlage ist erforderlich, wenn erweiterte eDiscovery die Verarbeitung führt und Dateidaten werden zum ersten Mal mit einem externen System hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p114">**All**: Full set of standard metadata including all processing data, as well as Analyze and Relevance scores. This template is required when Advanced eDiscovery performs the processing and file data is uploaded to an external system for the first time.</span></span>
    
  - <span data-ttu-id="9deb5-163">**Probleme**: Wählen Sie **Alle Probleme** oder ein bestimmtes Problem, das Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="9deb5-163">**Issues**: Select **All Issues** or select a particular issue you have created.</span></span> 
    
5. <span data-ttu-id="9deb5-164">Klicken Sie unter **Ziel**:</span><span class="sxs-lookup"><span data-stu-id="9deb5-164">Under **Destination**:</span></span>
    
  - <span data-ttu-id="9deb5-165">**Laden Sie auf dem lokalen Computer**</span><span class="sxs-lookup"><span data-stu-id="9deb5-165">**Download to local machine**</span></span>
    
  - <span data-ttu-id="9deb5-166">**Export in Azure Blob benutzerdefinierte**: Wenn diese Option aktiviert ist, können Sie angeben, dass ein Container-URL und SAS-Token.</span><span class="sxs-lookup"><span data-stu-id="9deb5-166">**Export to user-defined Azure blob**: If this is checked, you can specify a container URL and SAS token.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9deb5-p115">Sobald ein Exportpaket zu gespeichert wurde die benutzerdefinierten Azure Blob, die Daten werden nicht mehr verwaltet von erweiterten eDiscovery; Es wird von den Azure Blob verwaltet. Dies bedeutet, wenn Sie die Groß-/Kleinschreibung löschen, die exportierten Dateien weiterhin auf die Azure Blob verbleibt.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p115">Once an export package is stored to the user defined Azure blob, the data is no longer managed by Advanced eDiscovery; it's managed by the Azure blob. This means if you delete the case, the exported files will still remain on the Azure blob.</span></span> 
  
  - <span data-ttu-id="9deb5-169">**Token für zukünftige Export-Sitzung speichern SAS**: Wenn diese Einstellung aktiviert, wird das SAS-Token in der erweiterten eDiscovery interne Datenbank für die zukünftige Verwendung verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="9deb5-169">**Save SAS token for future export session**: If checked, the SAS token will be encrypted in the Advanced eDiscovery's internal database for future use.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="9deb5-p116">Derzeit läuft ab das Token SAS nach Monat. Wenn Sie versuchen, die nach mehr als einem Monat herunterladen Sie die letzten Sitzung rückgängig zu machen müssen, exportieren Sie dann erneut.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p116">Currently the SAS token expires after a month. If you try to download after more than a month you have to undo last session, then export again.</span></span> 
  
6. <span data-ttu-id="9deb5-172">Klicken Sie auf **Ändern** , legen Sie die "zur Überprüfung ' Feld Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="9deb5-172">Click **Modify** to set the "for review' field settings.</span></span> 
    
> ![Einrichten von für die Überprüfung Feld Seetings für einen Batch export](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
    In **For review field settings** panel, in **Select scenario**, select the scenario and scope of the review. The settings are displayed based on your selection.
    
    **Review all** (default): All emails, attachments, and documents are selected by default. 
    
    **Review all unique content in a set**: Inclusives and unique inclusive copies, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content in a set - no inclusive copies**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content and related family files**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates, expand to include family files.
    
    **Custom** (allows you to define the options in the dialog): The default is to keep current selections and enable all dialog options, to allow their selection. 
    
    If you select custom, you can then customize the settings for emails, documents, attachments and miscellaneous.
    
> <span data-ttu-id="9deb5-174">Wählen Sie die e-Mails, die Sie exportieren möchten, im **-e-Mails** :</span><span class="sxs-lookup"><span data-stu-id="9deb5-174">In **Emails** select the emails you want to export:</span></span> 
    
    **All emails**: (default) All emails are selected.
    
    **Inclusives**: An inclusive email is a last email of a thread, and it contains all the other emails from the thread.
    
    **Inclusives and unique inclusive copies**: Inclusive copies and inclusives with the same subject, body and attachments; unique inclusive copies are unique copies of these emails .
    
> <span data-ttu-id="9deb5-175">Wählen Sie in **Dokumenten** die Dokumente, die Sie exportieren möchten:</span><span class="sxs-lookup"><span data-stu-id="9deb5-175">In **Documents** select the documents you want to export:</span></span> 
    
    **All documents**: (default) All documents are selected.
    
    **Pivots**: A file chosen as representative of near-duplicates set, which is typically used as the baseline when reviewing the set.
    
    **Representative from every set of exact duplicates**: Unique near-duplicate files (including the pivot).
    
> <span data-ttu-id="9deb5-176">Wählen Sie in **Anlagen** der Anlagen, die Sie exportieren möchten</span><span class="sxs-lookup"><span data-stu-id="9deb5-176">In **Attachments** select the attachments you want to export</span></span> 
    
    **All attachments**: (default) All attachments are selected.
    
    **Unique attachment in case level**: Unique attachment files within the specified case.
    
    **Unique attachment in email set level**: Unique attachment files within the specified email case.
    
> <span data-ttu-id="9deb5-p117">Im **Micellaneous** können Sie **Anlagen als Dokumente behandelt**, **wie Dokumente-e-Mails behandelt**oder **erweitern, um Produktfamilie Includedateien**auswählen. Bei der Auswahl **erweitern, um Produktfamilie Includedateien**, für jede Datei zur Prüfung gekennzeichnet ist, werden auch alle Dateien derselben Familie gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p117">In **Micellaneous** you can choose to **Treat attachments as documents**, **Treat emails as documents**, or **Expand to include family files**. When you choose **Expand to include family files**, for each file that is flagged for review, all files of the same family will also be flagged.</span></span>
    
    Choose **Save** to save the settings. 
    
7. <span data-ttu-id="9deb5-179">Nachdem Sie Exportparameter angeben, um Export-Batch starten klicken Sie auf **Create Session exportieren**.</span><span class="sxs-lookup"><span data-stu-id="9deb5-179">After you specify export parameters, to start export batch, click **Create export session**.</span></span>
    
    <span data-ttu-id="9deb5-p118">Während des Exportvorgangs wird der Status in **Aufgabenstatus**angezeigt. Die Ergebnisse werden in der **Zusammenfassung Export**angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p118">During export, the status is displayed in **Task status**. The results are displayed in **Export summary**.</span></span>
    
8. <span data-ttu-id="9deb5-182">Klicken Sie auf **in die Zwischenablage kopieren** , um den Schlüssel exportieren kopieren, klicken Sie im Fenster **Downloaddateien** .</span><span class="sxs-lookup"><span data-stu-id="9deb5-182">In the **Download files** window, click **Copy to clipboard** to copy the Export key.</span></span> 
    
    ![Herunterladen von Dateien](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
9. <span data-ttu-id="9deb5-184">Klicken Sie auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="9deb5-184">Click **Close**.</span></span> 
    
    <span data-ttu-id="9deb5-185">Die eDiscovery-Exporttool wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="9deb5-185">The eDiscovery Export Tool is started.</span></span>
    
    ![eDiscovery-Exporttool](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
10. <span data-ttu-id="9deb5-187">In der **eDiscovery-Exporttool**:</span><span class="sxs-lookup"><span data-stu-id="9deb5-187">In the **eDiscovery Export Tool**:</span></span>
    
1. <span data-ttu-id="9deb5-188">Fügen Sie in **Einfügen der Signatur Zugriff freigegeben, die zum Verbinden mit der Datenquelle verwendet wird**dem Schlüssel exportieren, Youcopied in die Zwischenablage in Schritt 7.</span><span class="sxs-lookup"><span data-stu-id="9deb5-188">In **Paste the Shared Access Signature that will be used to connect to the source**, paste the Export key that youcopied to the clipboard in step 7.</span></span>
    
2. <span data-ttu-id="9deb5-189">Klicken Sie auf **Durchsuchen** , um den Zielspeicherort zum Speichern der heruntergeladenen Exportdateien auf dem lokalen Computer auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9deb5-189">Click **Browse** to select the target location for storing the downloaded export files on the local machine.</span></span> 
    
11. <span data-ttu-id="9deb5-p119">Klicken Sie auf **Start**. Die Exportdateien werden auf den lokalen Computer heruntergeladen. Wenn Sie in Schritt 4 **Export in Azure Blob Benutzerdefiniert** ausgewählt haben, wird die Sitzung an ein BLOB-Speicher-Ziel-URL Ihrer Wahl exportiert.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p119">Click **Start**.The export files are downloaded to the local machine. If you chose **Export to user-defined Azure blob** in step 4, the session is exported to a Blob storage URL destination of your choosing.</span></span> 
    
<span data-ttu-id="9deb5-192">Eine vollständige Beschreibung der Felder in den Exportbericht finden Sie unter [Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md).</span><span class="sxs-lookup"><span data-stu-id="9deb5-192">For a full description of the fields in the export report, see [Export report fields](export-report-fields-in-advanced-ediscovery.md).</span></span>
  
## <a name="export-report-output-files"></a><span data-ttu-id="9deb5-193">Exportieren von Ausgabedateien Bericht</span><span class="sxs-lookup"><span data-stu-id="9deb5-193">Export report output files</span></span>
<span data-ttu-id="9deb5-194"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="9deb5-194"></span></span>

<span data-ttu-id="9deb5-195">Die folgende Tabelle enthält die Ausgabedateien, die beim Ausführen eines Batches Export generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9deb5-195">The following table lists the output files that are generated when you run an Export batch.</span></span>
  
|<span data-ttu-id="9deb5-196">**Dateiname**</span><span class="sxs-lookup"><span data-stu-id="9deb5-196">**File name**</span></span>|<span data-ttu-id="9deb5-197">**Dateityp**</span><span class="sxs-lookup"><span data-stu-id="9deb5-197">**File type**</span></span>|<span data-ttu-id="9deb5-198">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9deb5-198">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9deb5-199">Zusammenfassung exportieren</span><span class="sxs-lookup"><span data-stu-id="9deb5-199">Export summary</span></span>  <br/> |<span data-ttu-id="9deb5-200">CSV</span><span class="sxs-lookup"><span data-stu-id="9deb5-200">csv</span></span>  <br/> |<span data-ttu-id="9deb5-201">Eine Protokolldatei generiert, indem die eDiscovery Exporttool.</span><span class="sxs-lookup"><span data-stu-id="9deb5-201">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="9deb5-202">Trace</span><span class="sxs-lookup"><span data-stu-id="9deb5-202">Trace</span></span>  <br/> |<span data-ttu-id="9deb5-203">txt</span><span class="sxs-lookup"><span data-stu-id="9deb5-203">txt</span></span>  <br/> |<span data-ttu-id="9deb5-204">Eine Protokolldatei generiert, indem die eDiscovery Exporttool.</span><span class="sxs-lookup"><span data-stu-id="9deb5-204">A log file generated by the eDiscovery Export Tool.</span></span>  <br/> |
|<span data-ttu-id="9deb5-205">Extrahierten Textdateien</span><span class="sxs-lookup"><span data-stu-id="9deb5-205">Extracted text files</span></span>  <br/> |<span data-ttu-id="9deb5-206">Dateiordner</span><span class="sxs-lookup"><span data-stu-id="9deb5-206">File folder</span></span>  <br/> |<span data-ttu-id="9deb5-207">Ordner, der die extrahierten Textdateien der exportierten Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="9deb5-207">Folder that contains the extracted text files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="9deb5-208">Eingabe oder systemeigene Dateien</span><span class="sxs-lookup"><span data-stu-id="9deb5-208">Input or native files</span></span>  <br/> |<span data-ttu-id="9deb5-209">Dateiordner</span><span class="sxs-lookup"><span data-stu-id="9deb5-209">File folder</span></span>  <br/> |<span data-ttu-id="9deb5-210">Ordner, die systemeigenen und input-Dateien der exportierten Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="9deb5-210">Folder that contains the native and input files of the exported files.</span></span>  <br/> |
|<span data-ttu-id="9deb5-211">Liste exportieren</span><span class="sxs-lookup"><span data-stu-id="9deb5-211">Export list</span></span>  <br/> |<span data-ttu-id="9deb5-212">xlsx</span><span class="sxs-lookup"><span data-stu-id="9deb5-212">xlsx</span></span>  <br/> |<span data-ttu-id="9deb5-p120">Metadaten der exportierten Dateien im Xlsx-Format dar. Felder in Dateien werden gemäß der Vorlage Benutzer wählt zu exportieren. Falls erforderlich, mehrere Dateien erstellt wurden, jeweils 100-150 KB Zeilen enthält. Wenn Sie ein bestimmten Wert enthält mehr Zeichen als eine Excel-Zelle enthalten kann (derzeit die Grenze liegt bei 32.767 Zeichen), und klicken Sie dann der Wert wird auf die maximal zulässige Länge gekürzt werden. Wenn Sie ein Wert abgeschnitten wird, ist Hintergrundfarbe der Zelle an, dass dies dem Benutzer Rot." E-Mail Teilnehmer"ist ein Beispiel für ein Feld, das die maximale Länge überschreiten kann, wenn die e-Mail-Nachricht an eine große Verteilergruppe gesendet wurde. Details zu den Ausgabefeldern finden Sie unter [Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md) .</span><span class="sxs-lookup"><span data-stu-id="9deb5-p120">Exported files metadata in xlsx format. Fields in files are according to template user selects to export. If needed, several files are created, each contains 100-150K rows. If a certain value contains more characters than an Excel cell can contain (currently the limit is 32,767 characters), then the value will be trimmed to the maximum length allowed. If a value is trimmed, the cell's background color is red to indicate this to the user."Email participants" is an example of a field that can exceed the length limit, if the email was sent to a large distribution. See [Export report fields](export-report-fields-in-advanced-ediscovery.md) for details about the output fields.  </span></span><br/> |
|<span data-ttu-id="9deb5-219">Datei laden</span><span class="sxs-lookup"><span data-stu-id="9deb5-219">Load file</span></span>  <br/> |<span data-ttu-id="9deb5-220">CSV</span><span class="sxs-lookup"><span data-stu-id="9deb5-220">csv</span></span>  <br/> |<span data-ttu-id="9deb5-p121">Metadaten der exportierten Dateien im CSV-Format in einer anderen Anwendung geladen. Felder in Dateien werden gemäß der Vorlage Benutzer wählt zu exportieren.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p121">Exported files metadata in csv format for loading into a different application. Fields in files are according to template user selects to export.</span></span>  <br/> |
|<span data-ttu-id="9deb5-223">Symbol für Erfolg</span><span class="sxs-lookup"><span data-stu-id="9deb5-223">Success indicator</span></span>  <br/> |<span data-ttu-id="9deb5-224">txt</span><span class="sxs-lookup"><span data-stu-id="9deb5-224">txt</span></span>  <br/> |<span data-ttu-id="9deb5-p122">Nur erstellt beim Exportieren einer 3rd Azure Blob Partei. Wenn der Export erfolgreich ausgeführt werden, wird die Datei erstellt. Bei einem Ausfall oder den partiellen wird Erfolg die Datei nicht erstellt werden. Datei wird im Stammordner, ermöglicht die automatisierte Tracking auf verschiedenen Export Batches-Sitzungen Statusarten erstellt werden. Dies ist eine leere Datei. Ihr Name lautet: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span><span class="sxs-lookup"><span data-stu-id="9deb5-p122">Only created when exporting to a 3rd party Azure blob. If export succeed completely, the file will be created. In case of failure, or partial success the file will not be created. File will be created in the root folder, allowing automated tracking on different Export batches/sessions statuses. This is an empty file. Its name is: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9deb5-231">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9deb5-231">See also</span></span>
<span data-ttu-id="9deb5-232"><a name="BK_ExportOutputFIles"> </a></span><span class="sxs-lookup"><span data-stu-id="9deb5-232"></span></span>

[<span data-ttu-id="9deb5-233">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9deb5-233">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="9deb5-234">Anzeigen des Verlaufs Batch und ältere Ergebnisse exportieren</span><span class="sxs-lookup"><span data-stu-id="9deb5-234">Viewing batch history and exporting past results</span></span>](view-batch-history-and-export-past-results.md)
  
[<span data-ttu-id="9deb5-235">Schnelles Setup für Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9deb5-235">Quick setup for Office 365 Advanced eDiscovery</span></span>](quick-setup-for-advanced-ediscovery.md)

[<span data-ttu-id="9deb5-236">Exportieren von Berichtsfeldern</span><span class="sxs-lookup"><span data-stu-id="9deb5-236">Export report fields</span></span>](export-report-fields-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9deb5-237">Die Download-Leistung zu steigern, beim Exportieren von eDiscovery-Suchergebnisse aus Office 365</span><span class="sxs-lookup"><span data-stu-id="9deb5-237">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>](increase-download-speeds-when-exporting-ediscovery-results.md)

