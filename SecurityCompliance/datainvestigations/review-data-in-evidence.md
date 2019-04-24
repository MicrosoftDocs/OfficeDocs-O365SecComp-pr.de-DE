---
title: Überprüfen von Nachweisdaten
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
ms.openlocfilehash: e84f05fa1a7356952b62f2f4adc3b7d0f1ddc94e
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32258043"
---
# <a name="review-the-data-in-evidence"></a><span data-ttu-id="766cc-102">Überprüfen von Nachweisdaten</span><span class="sxs-lookup"><span data-stu-id="766cc-102">Review the data in evidence</span></span>

<span data-ttu-id="766cc-103">Bei den Daten in einem Evidence-Satz in einer Daten Untersuchung handelt es sich um eine Momentaufnahme der Suchergebnisse, die Sie gesammelt und dem Evidence-Satz hinzugefügt haben.</span><span class="sxs-lookup"><span data-stu-id="766cc-103">The data in an evidence set in a data investigation is a snapshot of the search results that you collected and added to the evidence set.</span></span> <span data-ttu-id="766cc-104">Wenn Sie Suchergebnisse zu beweisen hinzufügen, wird ein Prozess ausgelöst, um Dateien, Metadaten und Text aus den von der Suche zurückgegebenen Elementen zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="766cc-104">When you add search results to evidence, a process is triggered to extract files, metadata, and text from the items returned by the search.</span></span> <span data-ttu-id="766cc-105">Dann erstellt das Tool für Daten Untersuchungen (Vorschau) einen neuen Index (durch einen Prozess namens *Advanced Indexing*) aller Daten und fügt einen auf der Registerkarte **Evidence** festgelegten Nachweis hinzu.</span><span class="sxs-lookup"><span data-stu-id="766cc-105">Then the Data Investigations (Preview) tool then builds a new index (by a process called *Advanced indexing*) of all the data and adds to an evidence set on the **Evidence** tab.</span></span> 

<span data-ttu-id="766cc-106">Bei zeitabhängigen Untersuchungen können Sie dadurch schnell die Umgebung eindämmen, indem Sie die tatsächlich verschütteten oder bösartigen Daten, die sich in der ursprünglichen Datenquelle befinden, löschen und gleichzeitig den erneut erstellten Beweis in einem isolierte Umgebung, in diesem Fall werden die Daten in den Evidence-Satz kopiert.</span><span class="sxs-lookup"><span data-stu-id="766cc-106">For time-sensitive investigations, this allows you to quickly contain the environment by deleting the actual spilled or malicious data located in the at original data source, while at the same time allowing you to investigate the re-created evidence in a quarantined environment, which in this case is the data copied to the evidence set).</span></span> <span data-ttu-id="766cc-107">Nachdem der Beweis gesammelt und dem Evidence-Satz hinzugefügt wurde, können Sie einzelne Dokumente im nativen Format, im Text Format oder in einem nahezu systemeigenen Format überarbeiten, mit dem Sie Dokumente mit Anmerkungen versehen und redact können.</span><span class="sxs-lookup"><span data-stu-id="766cc-107">After the evidence is collected and added to the evidence set, you can review individual documents in their native format, text format, or a near-native format that you can use to annotate and redact documents.</span></span> <span data-ttu-id="766cc-108">Darüber hinaus können Sie Abfragen ausführen, um die Datensätze nach Zeitspanne, Dateitypen, Datenbesitzern und vielen anderen Eigenschaften und Suchbedingungen einzugrenzen.</span><span class="sxs-lookup"><span data-stu-id="766cc-108">Additionally, you can run queries to narrow the data set by time range, file types, data owners, and many other properties and search conditions.</span></span> <span data-ttu-id="766cc-109">Beispielsweise können Sie mithilfe der Bedingungen Autor, Absender oder Empfänger schnell erkennen, welche Personen an dem Vorfall beteiligt sind und ob Daten aus Ihrer Organisation für externe Benutzer freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="766cc-109">For example, by using the Author, Sender, or Recipient conditions, you can quickly identify the people are involved in the incident and if any data from your organization has been shared with external users.</span></span> <span data-ttu-id="766cc-110">Weitere Informationen zum Durchsuchen von Daten in einem Evidence-Satz finden Sie unter [Query the data in Evidence](evidence-query.md).</span><span class="sxs-lookup"><span data-stu-id="766cc-110">For more information about searching through data in an evidence set, see [Query the data in evidence](evidence-query.md).</span></span>

<span data-ttu-id="766cc-111">Um Dokumente zu gruppieren und weitere Unterstützung für Ihre Überprüfungen zu erhalten, wählen Sie auf der Registerkarte **Evidence** einen Evidence-Satz aus, und klicken Sie dann auf **Evidence verwalten**.</span><span class="sxs-lookup"><span data-stu-id="766cc-111">To group documents and get more assistance for your review, select an evidence set on the **Evidence** tab, and then click **Manage evidence**.</span></span> <span data-ttu-id="766cc-112">Klicken Sie in der **Analytics** -Kachel auf **Analyse für den gesamten Satz neu erstellen**.</span><span class="sxs-lookup"><span data-stu-id="766cc-112">In the **Analytics** tile, click **Rebuild analytics for the whole set**.</span></span> <span data-ttu-id="766cc-113">Dadurch werden erweiterte Analysen wie doppelte Erkennung, e-Mail-Threading und Design Analyse ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="766cc-113">This will run advanced analytics such as duplicate detection, email threading, and theme analysis.</span></span> <span data-ttu-id="766cc-114">Anschließend können Sie die allgemeinen Themen der Daten sehen und auch Dokumente per e-Mail-Threads, in der Nähe von Duplikaten und exakte Duplikate organisieren, um Ihre Untersuchung zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="766cc-114">Afterwards, you can see the general themes of the data and also organize documents by email threads, near duplicates, and exact duplicates to help your investigation.</span></span> <span data-ttu-id="766cc-115">Weitere Informationen finden Sie unter [Run Analytics to untersuchen schneller](run-analytics-to-investigate-faster.md).</span><span class="sxs-lookup"><span data-stu-id="766cc-115">For more information, see [Run analytics to investigate faster](run-analytics-to-investigate-faster.md).</span></span>

## <a name="view-documents-in-evidence"></a><span data-ttu-id="766cc-116">Dokumente als Beweis anzeigen</span><span class="sxs-lookup"><span data-stu-id="766cc-116">View documents in evidence</span></span>

<span data-ttu-id="766cc-117">Daten Untersuchungen (Preview) ermöglicht die Anzeige von Inhalten in mehreren verschiedenen Viewern, wobei jeder Betrachter einen anderen Zweck hat.</span><span class="sxs-lookup"><span data-stu-id="766cc-117">Data Investigations (Preview) allows you to display content in several different viewers, with each viewer having a different purpose.</span></span> <span data-ttu-id="766cc-118">Diese Zuschauer sind:</span><span class="sxs-lookup"><span data-stu-id="766cc-118">These viewers are:</span></span>

- <span data-ttu-id="766cc-119">Datei Metadaten</span><span class="sxs-lookup"><span data-stu-id="766cc-119">File metadata</span></span>
- <span data-ttu-id="766cc-120">Systemeigene Ansicht</span><span class="sxs-lookup"><span data-stu-id="766cc-120">Native view</span></span>
- <span data-ttu-id="766cc-121">Text Ansicht</span><span class="sxs-lookup"><span data-stu-id="766cc-121">Text view</span></span>
- <span data-ttu-id="766cc-122">Ansicht mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="766cc-122">Annotate view</span></span>

<span data-ttu-id="766cc-123">Wenn Sie auf einen dieser Viewer zugreifen möchten, wählen Sie ein Dokument in einem Evidence-Set aus.</span><span class="sxs-lookup"><span data-stu-id="766cc-123">To access any of these viewers, just select a document in an evidence set.</span></span>

## <a name="file-metadata"></a><span data-ttu-id="766cc-124">Datei Metadaten</span><span class="sxs-lookup"><span data-stu-id="766cc-124">File metadata</span></span>

<span data-ttu-id="766cc-125">In dieser Ansicht werden verschiedene Metadaten-Eigenschaften angezeigt, die dem ausgewählten Dokument zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="766cc-125">This view displays various metadata properties associated with the selected document.</span></span> <span data-ttu-id="766cc-126">Sie können diese Ansicht ein-und ausschalten, indem Sie auf **Datei Metadaten**klicken.</span><span class="sxs-lookup"><span data-stu-id="766cc-126">You can toggle this view on and off by clicking **File metadata**.</span></span> <span data-ttu-id="766cc-127">Beim Überprüfen eines Dokuments können Sie die Datei Metadaten anzeigen und trotzdem zwischen den verschiedenen Viewern wechseln.</span><span class="sxs-lookup"><span data-stu-id="766cc-127">When reviewing a document, you can view the file metadata and still change between the different viewers.</span></span>

<span data-ttu-id="766cc-128">Im folgenden finden Sie ein Beispiel für die Datei Metadaten für ein Dokument.</span><span class="sxs-lookup"><span data-stu-id="766cc-128">Here's an example of the file metadata for a document.</span></span> <span data-ttu-id="766cc-129">Weitere Informationen zu den Metadatenfeldern finden Sie unter [Document Metadata fields in Data Investigations (Preview)](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="766cc-129">For more information about the metadata fields, see [Document metadata fields in Data Investigations (Preview)](document-metadata-fields.md).</span></span>

![Datei-Metadatenbereich](../media/Reviewimage2.png)

## <a name="native-view"></a><span data-ttu-id="766cc-131">Systemeigene Ansicht</span><span class="sxs-lookup"><span data-stu-id="766cc-131">Native view</span></span>

<span data-ttu-id="766cc-132">Der systemeigene Viewer zeigt die genaueste Ansicht eines Dokuments im systemeigenen Format an.</span><span class="sxs-lookup"><span data-stu-id="766cc-132">The Native viewer displays the most accurate view of a document in it's native format.</span></span> <span data-ttu-id="766cc-133">Die systemeigene Ansicht wird für Hunderte von Dateitypen unterstützt und soll Dokumente in der größtmöglichen nativen Umgebung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="766cc-133">Native view is supported for hundreds of file types and is meant to display documents in the truest native experience possible.</span></span> <span data-ttu-id="766cc-134">Für Microsoft Office-Dateien verwendet der systemeigene Viewer Office Online.</span><span class="sxs-lookup"><span data-stu-id="766cc-134">For Microsoft Office files, the Native viewer uses Office Online.</span></span> <span data-ttu-id="766cc-135">Auf diese Weise können Sie Inhalte wie Kommentare in verschiedenen Office-Dokumenten, Formeln und ausgeblendeten Zeilen/Spalten in Excel und die Notizenansicht in PowerPoint anzeigen.</span><span class="sxs-lookup"><span data-stu-id="766cc-135">This allows you to view content such as comments in different Office documents, formulas and hidden rows/columns in Excel, and the Notes view in PowerPoint.</span></span>

![<span data-ttu-id="766cc-136">Systemeigene Ansicht</span><span class="sxs-lookup"><span data-stu-id="766cc-136">Native view</span></span>
](../media/Reviewimage3.png)

## <a name="text-view"></a><span data-ttu-id="766cc-137">Text Ansicht</span><span class="sxs-lookup"><span data-stu-id="766cc-137">Text view</span></span>

<span data-ttu-id="766cc-138">Der Text Betrachter bietet eine Ansicht des extrahierten Texts einer Datei.</span><span class="sxs-lookup"><span data-stu-id="766cc-138">The Text viewer provides a view of the extracted text of a file.</span></span> <span data-ttu-id="766cc-139">Eingebettete Bilder und Formatierungen werden ignoriert, aber diese Ansicht ist sehr nützlich, wenn Sie versuchen, die Inhalte in einem Dokument schnell zu überprüfen und zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="766cc-139">It ignores any embedded images and formatting, but this view is very useful if you're trying to quickly review and understand the content in a document.</span></span> <span data-ttu-id="766cc-140">Die Text Ansicht umfasst auch die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="766cc-140">Text view also includes these features:</span></span>

  - <span data-ttu-id="766cc-141">Ein Linien Zähler, der das referenzieren bestimmter Teile eines Dokuments erleichtert.</span><span class="sxs-lookup"><span data-stu-id="766cc-141">A line counter, which makes it easier to reference specific portions of a document.</span></span>

  - <span data-ttu-id="766cc-142">Hervorheben von Suchtreffern, die Ausdrücke im Dokument sowie auf der Bildlaufleiste hervorheben</span><span class="sxs-lookup"><span data-stu-id="766cc-142">Search hit highlighting that highlight terms in the document as well as on the scrollbar</span></span>

  - <span data-ttu-id="766cc-143">Eine diff-Ansicht bietet eine Vergleichsansicht, in der die Textunterschiede beim Anzeigen von Dokumenten mit dem Panel **near Duplicates** hervorgehoben werden.</span><span class="sxs-lookup"><span data-stu-id="766cc-143">A diff view provides a comparison view that highlights the text differences when viewing documents using the **Near duplicates** panel.</span></span>

<span data-ttu-id="766cc-144">**Beispiel für Linien Zähler und Suchtreffer Hervorhebung in Text und ScrollBar**</span><span class="sxs-lookup"><span data-stu-id="766cc-144">**Example of line counter and search hit highlighting in text and scrollbar**</span></span>

![<span data-ttu-id="766cc-145">Text Ansicht</span><span class="sxs-lookup"><span data-stu-id="766cc-145">Text view</span></span>
](../media/Reviewimage4.png)

<span data-ttu-id="766cc-146">**Beispiel für die diff-Ansicht**</span><span class="sxs-lookup"><span data-stu-id="766cc-146">**Example of the diff view**</span></span>

![<span data-ttu-id="766cc-147">Ansicht "diff"</span><span class="sxs-lookup"><span data-stu-id="766cc-147">Diff view</span></span>
](../media/Reviewimage5.png)

## <a name="annotate-view"></a><span data-ttu-id="766cc-148">Ansicht mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="766cc-148">Annotate view</span></span>

<span data-ttu-id="766cc-149">In der Ansicht mit Anmerkungen werden Features bereitgestellt, mit denen Sie während des überarbeits Vorgangs Markups für ein Dokument anwenden können. Hierzu gehören die folgenden Tools:</span><span class="sxs-lookup"><span data-stu-id="766cc-149">The Annotate view provides features that allow you to apply markup on a document during the review process; this  includes these tools:</span></span>

  - <span data-ttu-id="766cc-150">**Flächen-Aktionen** – Sie können ein deckendes Feld im Dokument zeichnen, das vertrauliche Inhalte ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="766cc-150">**Area redactions** – You can draw an opaque box on the document that hides sensitive content.</span></span>

  - <span data-ttu-id="766cc-151">**Bleistift** – Sie können ein Dokument Freihandzeichnen, um auf bestimmte Teile des Inhalts zu achten.</span><span class="sxs-lookup"><span data-stu-id="766cc-151">**Pencil** – You can free-hand draw on a document to bring attention to certain portions of the content</span></span>

  - <span data-ttu-id="766cc-152">**Anmerkungen auswählen** – Sie können Anmerkungen in einem Dokument auswählen und löschen.</span><span class="sxs-lookup"><span data-stu-id="766cc-152">**Select annotations** - You can select and delete annotations in a document.</span></span>

  - <span data-ttu-id="766cc-153">**Anmerkungs Transparenz umschalten** – Sie können die Transparenz von Anmerkungen (zwischen deckend und halbtransparent) so umschalten, dass der Inhalt hinter der Anmerkung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="766cc-153">**Toggle annotation transparency** – You can toggle the transparency of annotations (between opaque and semi-transparent)so you can view the content behind the annotation.</span></span> <span data-ttu-id="766cc-154">Dazu gehört das Umschalten der Transparenz von Bleistift Anmerkungen und-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="766cc-154">This includes toggling the transparency of pencil annotations and redactions.</span></span>

<span data-ttu-id="766cc-155">Die Ansicht mit Anmerkungen stellt auch die folgenden Navigationsfunktionen bereit:</span><span class="sxs-lookup"><span data-stu-id="766cc-155">The Annotate view also provides the following navigation functionality:</span></span>

  - <span data-ttu-id="766cc-156">**Vorherige Seite**, **Nächste Seite**, und **Navigieren Sie zu** Steuerelementen für die Seiten Navigation für mehrseitige Dokumente.</span><span class="sxs-lookup"><span data-stu-id="766cc-156">**Previous page**, **Next page**, and **Go to page** - Navigation controls to use for multi-page documents.</span></span>

  - <span data-ttu-id="766cc-157">**Zoom** – erhöht oder verkleinert die Größe von Dokumenten in der Ansicht mit Anmerkungen.</span><span class="sxs-lookup"><span data-stu-id="766cc-157">**Zoom** – Increases or decreases the size of documents in Annotate view.</span></span>

  - <span data-ttu-id="766cc-158">**Rotate** – Dokumente im Uhrzeigersinn drehen.</span><span class="sxs-lookup"><span data-stu-id="766cc-158">**Rotate** – Rotate documents clockwise.</span></span>

  - <span data-ttu-id="766cc-159">**Suche** – suchen Sie nach Schlüsselwörtern in einem Dokument, und verwenden Sie dann die vorherigen und nächsten Steuerelemente, um die Treffer (die hervorgehoben werden) innerhalb des Dokuments anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="766cc-159">**Search** – Search for keywords in a document, and then use Previous and Next controls to view the hits (which are highlighted) within the document.</span></span>

<span data-ttu-id="766cc-160">**Beispiel für eine Ansicht mit Anmerkungen**</span><span class="sxs-lookup"><span data-stu-id="766cc-160">**Example of Annotate view**</span></span>

![Ansicht mit Anmerkungen](../media/Reviewimage1.png)

> [!NOTE]
> <span data-ttu-id="766cc-162">Anmerkungen werden auf eine Kopie des Dokuments angewendet, das dem Evidence-Satz hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="766cc-162">Annotations are applied to a copy of the document that was added to the evidence set.</span></span> <span data-ttu-id="766cc-163">Die Originaldokumente im Live-Dienst werden nicht mit Anmerkungen versehen.</span><span class="sxs-lookup"><span data-stu-id="766cc-163">The original documents in the live service aren't annotated.</span></span>
