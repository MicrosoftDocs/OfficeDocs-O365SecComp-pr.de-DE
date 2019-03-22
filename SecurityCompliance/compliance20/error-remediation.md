---
title: Beheben von Fehlern beim Verarbeiten von Daten
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
ms.openlocfilehash: f6db3c178e584c45cf282158c58fb5125dc41f3f
ms.sourcegitcommit: cf9d9b545a7c153d314aa9c08c7fb16fcd785b3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30737675"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="b38b4-102">Beheben von Fehlern beim Verarbeiten von Daten</span><span class="sxs-lookup"><span data-stu-id="b38b4-102">Error remediation when processing data</span></span>

<span data-ttu-id="b38b4-103">Fehlerkorrektur ermöglicht eDiscovery-Administratoren das Beheben von Datenproblemen, die verhindern, dass Advanced eDiscovery (Preview) die Inhalte ordnungsgemäß verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="b38b4-103">Error remediation allows eDiscovery administrators the ability to rectify data issues which prevent Advanced eDiscovery (Preview) from properly processing the content.</span></span> <span data-ttu-id="b38b4-104">Dateien, die kennwortgeschützt sind, können beispielsweise nicht verarbeitet werden, da die Dateien gesperrt oder verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="b38b4-104">For example, files that are password protected cannot be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="b38b4-105">Mithilfe von Fehlerkorrekturen können eDiscovery-Administratoren Dateien mit solchen Fehlern herunterladen, den Kennwortschutz entfernen und die korrigierten Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="b38b4-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="b38b4-106">Verwenden Sie den folgenden Workflow, um Dateien mit Fehlern in Advanced eDiscovery (Preview)-Fällen zu korrigieren.</span><span class="sxs-lookup"><span data-stu-id="b38b4-106">Use the following workflow to remediate files with errors in Advanced eDiscovery (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="b38b4-107">Erstellen einer Fehlerbehebungssitzung zum Beheben von Dateien mit Verarbeitungsfehlern</span><span class="sxs-lookup"><span data-stu-id="b38b4-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="b38b4-108">Wenn der Fehlerkorrektur-Assistent während des folgenden Verfahrens jederzeit geschlossen ist, können Sie auf der Registerkarte **Verarbeitung** zur Fehlerbehebungssitzung zurückkehren, indem Sie im Dropdownmenü **Ansicht** die Option **Fehler** Korrekturen auswählen.</span><span class="sxs-lookup"><span data-stu-id="b38b4-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="b38b4-109">Wählen Sie auf der Registerkarte **Verarbeitung** in einem Advanced EDiscovery (Preview)-Fall im Dropdownmenü **Ansicht** die Option **Fehler** aus.</span><span class="sxs-lookup"><span data-stu-id="b38b4-109">On the **Processing** tab in an Advanced eDiscovery (Preview) case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="b38b4-110">Wählen Sie die Fehler aus, die Sie korrigieren möchten, indem Sie auf das Optionsfeld neben dem Fehlertyp oder-Dateityp klicken.</span><span class="sxs-lookup"><span data-stu-id="b38b4-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="b38b4-111">Im folgenden Beispiel besprechen wir eine kennwortgeschützte Datei.</span><span class="sxs-lookup"><span data-stu-id="b38b4-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="b38b4-112">Klicken Sie auf **+ neue Fehlerkorrektur**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-112">Click **+ New error remediation**.</span></span>

    ![Fehlerkorrektur](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="b38b4-114">Die Fehlerbehebungssitzung beginnt mit einer Vorbereitungsphase, in der die fehlerhaften Dateien zu einem sicheren Azure-Speicherort verschoben und heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="b38b4-114">The error remediation session will begin, starting with a preparation stage where the files that errored are moved to a secure Azure location to be downloaded.</span></span>

    ![Vorbereiten der Fehlerkorrektur](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="b38b4-116">Klicken Sie nach Abschluss der Vorbereitung auf **Weiter: Dateien herunterladen** , um den Download fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="b38b4-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Dateien herunterladen](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="b38b4-118">Zum Herunterladen von Dateien geben Sie den **Zielpfad zum Herunterladen**an. Hierbei handelt es sich um einen Pfad auf dem lokalen Computer, auf dem die Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="b38b4-118">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.</span></span>  <span data-ttu-id="b38b4-119">Der Standardpfad,%USERPROFILE%\Downloads\errors, verweist auf den Downloadordner des angemeldeten Benutzers. Dies kann bei Bedarf geändert werden.</span><span class="sxs-lookup"><span data-stu-id="b38b4-119">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="b38b4-120">Es wird empfohlen, einen lokalen Dateipfad anstelle eines Remotenetzwerk Pfads für eine optimale Leistung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b38b4-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b38b4-121">Wenn Sie AzCopy nicht installiert haben, können Sie es von hier aus installieren:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="b38b4-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="b38b4-122">Kopieren Sie den vordefinierten Befehl **, indem Sie auf in Zwischenablage kopieren**klicken.</span><span class="sxs-lookup"><span data-stu-id="b38b4-122">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="b38b4-123">Starten Sie eine Windows-Eingabeaufforderungen, fügen Sie den Befehl ein, und drücken Sie dann die **Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="b38b4-123">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="b38b4-124">Die Dateien werden heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="b38b4-124">The files will be downloaded.</span></span>

    ![Vorbereiten der Fehlerkorrektur](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="b38b4-126">Wenn der angegebene AzCopy-Befehl fehlschlägt, finden Sie weitere Informationen unter [Problembehandlung bei AzCopy in Advanced eDiscovery (Preview)](troubleshooting-azcopy.md)</span><span class="sxs-lookup"><span data-stu-id="b38b4-126">If the supplied AzCopy command fails, see to [Troubleshoot AzCopy in Advanced eDiscovery (Preview)](troubleshooting-azcopy.md)</span></span>

7. <span data-ttu-id="b38b4-127">Nachdem Sie die Dateien heruntergeladen haben, können Sie Sie mit einem geeigneten Tool beheben.</span><span class="sxs-lookup"><span data-stu-id="b38b4-127">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="b38b4-128">Für kennwortgeschützte Dateien gibt es eine Reihe von Kenn Wort Knack Werkzeugen, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b38b4-128">For password protected files, there are a number of password cracking tools you can use.</span></span> <span data-ttu-id="b38b4-129">Wenn Sie die Kennwörter für die Dateien kennen, können Sie Sie öffnen und den Kennwortschutz entfernen.</span><span class="sxs-lookup"><span data-stu-id="b38b4-129">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="b38b4-130">Es ist wichtig, dass Sie die Verzeichnisstruktur und die Dateinamen der bereinigten Dateien im Takt behalten.</span><span class="sxs-lookup"><span data-stu-id="b38b4-130">IT is important that you retain the directory structure and file names of the remediated files in tact.</span></span>  <span data-ttu-id="b38b4-131">Alle in den heruntergeladenen Dateien und Ordnern verwendeten Benennungskonventionen ermöglichen es, die remdiated-Dateien dem Original zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="b38b4-131">All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="b38b4-132">Kehren Sie nun zu Advanced eDiscovery (Preview) zurück, und klicken Sie auf **Weiter: Dateien hochladen**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-132">Now, return to Advanced eDiscovery (Preview) and click **Next: Upload files**.</span></span>  <span data-ttu-id="b38b4-133">Dadurch gelangen Sie zum nächsten Schritt, in dem Sie jetzt die Dateien hochladen können.</span><span class="sxs-lookup"><span data-stu-id="b38b4-133">This will move to the next step where you can now upload the files.</span></span>

    ![Hochladen von Dateien](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="b38b4-135">Spezifizieren Sie den Speicherort der wiederherzustellenden Dateien im Textfeld **Pfad zum Speicherort der Dateien** , und klicken Sie dann auf **in clibpboard kopieren**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-135">Specifiy the location of the remediated files in the **Path to location of files** text box, then click **Copy to clibpboard**.</span></span>

10. <span data-ttu-id="b38b4-136">Fügen Sie den Befehl in eine Windows-EingabeaufForderungen ein, und drücken **Sie die Eingabe** Taste, um die Dateien hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="b38b4-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="b38b4-138">Kehren Sie schließlich zu Advanced eDiscovery (Preview) zurück, und klicken Sie auf **Weiter: Process files**.</span><span class="sxs-lookup"><span data-stu-id="b38b4-138">Finally, return to Advanced eDiscovery (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="b38b4-139">Nach Abschluss der Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="b38b4-139">When processing is complete.</span></span>  <span data-ttu-id="b38b4-140">Sie können zum Arbeitssatz zurückkehren und die korrigierte Datei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b38b4-140">You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="b38b4-141">Was geschieht, wenn Dateien korrigiert werden</span><span class="sxs-lookup"><span data-stu-id="b38b4-141">What happens when files are remediated</span></span>

<span data-ttu-id="b38b4-142">Bei hochgeladenen Dateien werden die ursprünglichen Metadaten mit Ausnahme der folgenden Felder beibehalten:</span><span class="sxs-lookup"><span data-stu-id="b38b4-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="b38b4-143">DocumentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="b38b4-143">DocumentExtractedUrl</span></span>
- <span data-ttu-id="b38b4-144">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="b38b4-144">ExtractedTextSize</span></span>
- <span data-ttu-id="b38b4-145">HasText</span><span class="sxs-lookup"><span data-stu-id="b38b4-145">HasText</span></span>
- <span data-ttu-id="b38b4-146">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="b38b4-146">IsErrorRemediate</span></span>
- <span data-ttu-id="b38b4-147">IsParentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="b38b4-147">IsParentExtractedUrl</span></span>
- <span data-ttu-id="b38b4-148">ItemExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="b38b4-148">ItemExtractedUrl</span></span>
- <span data-ttu-id="b38b4-149">Lade-Nr.</span><span class="sxs-lookup"><span data-stu-id="b38b4-149">LoadId</span></span>
- <span data-ttu-id="b38b4-150">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="b38b4-150">ProcessingErrorMessage</span></span>
- <span data-ttu-id="b38b4-151">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="b38b4-151">ProcessingStatus</span></span>
- <span data-ttu-id="b38b4-152">Text</span><span class="sxs-lookup"><span data-stu-id="b38b4-152">Text</span></span>
- <span data-ttu-id="b38b4-153">WordCount</span><span class="sxs-lookup"><span data-stu-id="b38b4-153">WordCount</span></span>
- <span data-ttu-id="b38b4-154">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="b38b4-154">WorkingsetId</span></span>

<span data-ttu-id="b38b4-155">Eine Definition aller Dokument Metadatenfelder in Advanced eDiscovery (Preview) finden Sie unter [Document Metadata fields](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="b38b4-155">For a definition of all document metadata fields in Advanced eDiscovery (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>