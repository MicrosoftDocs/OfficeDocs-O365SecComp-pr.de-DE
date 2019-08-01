---
title: Beheben von Fehlern beim Verarbeiten von Daten
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 5168196dcac8a2cb3809f43fabb470c0f64cd0f7
ms.sourcegitcommit: 73dcdafb15b462223d1a670c781db260eb73c2f5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "36048146"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="f06c1-102">Beheben von Fehlern beim Verarbeiten von Daten</span><span class="sxs-lookup"><span data-stu-id="f06c1-102">Error remediation when processing data</span></span>

<span data-ttu-id="f06c1-103">Durch die Fehlerkorrektur können eDiscovery-Administratoren Daten Probleme beheben, die verhindern, dass Advanced eDiscovery die Inhalte ordnungsgemäß verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f06c1-103">Error remediation allows eDiscovery administrators the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="f06c1-104">Beispielsweise können Dateien, die kennwortgeschützt sind, nicht verarbeitet werden, da die Dateien gesperrt oder verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="f06c1-104">For example, files that are password protected can't be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="f06c1-105">Mithilfe der Fehlerbehebung können eDiscovery-Administratoren Dateien mit solchen Fehlern herunterladen, den Kennwortschutz entfernen und dann die korrigierten Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection, and then upload the remediated files.</span></span>

<span data-ttu-id="f06c1-106">Verwenden Sie den folgenden Workflow, um Dateien mit Fehlern in erweiterten eDiscovery-Fällen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f06c1-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="f06c1-107">Erstellen einer Fehlerkorrektur Sitzung zum Beheben von Dateien mit Verarbeitungsfehlern</span><span class="sxs-lookup"><span data-stu-id="f06c1-107">Create an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="f06c1-108">Wenn der Fehlerkorrektur-Assistent während des folgenden Verfahrens zu einem beliebigen Zeitpunkt geschlossen wird, können Sie auf der Registerkarte **Verarbeitung** zur Fehlerbehebungssitzung zurückkehren, indem Sie im Dropdownmenü **Ansicht** die Option **Fehler** Korrekturen auswählen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="f06c1-109">Wählen Sie auf der Registerkarte **Verarbeitung** in einem erweiterten eDiscovery-Fall im Dropdownmenü **Ansicht** die Option **Fehler** aus.</span><span class="sxs-lookup"><span data-stu-id="f06c1-109">On the **Processing** tab in an Advanced eDiscovery case, select **Errors** in the **View** drop-down menu.</span></span>

2. <span data-ttu-id="f06c1-110">Wählen Sie die Fehler aus, die Sie korrigieren möchten, indem Sie auf das Optionsfeld neben dem Fehlertyp oder-Dateityp klicken.</span><span class="sxs-lookup"><span data-stu-id="f06c1-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="f06c1-111">Im folgenden Beispiel werden wir eine kennwortgeschützte Datei remediationieren.</span><span class="sxs-lookup"><span data-stu-id="f06c1-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="f06c1-112">Klicken Sie auf **neue Fehlerkorrektur**.</span><span class="sxs-lookup"><span data-stu-id="f06c1-112">Click **New error remediation**.</span></span>

    ![Fehlerbehebung](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="f06c1-114">Die Fehlerkorrektur-Sitzung beginnt mit einer Vorbereitungsphase, in der die Dateien mit Fehlern in einen von Microsoft bereitgestellten Azure-Speicherort kopiert werden, damit Sie Sie auf den lokalen Computer herunterladen können, um Sie zu beheben.</span><span class="sxs-lookup"><span data-stu-id="f06c1-114">The error remediation session starts with a preparation stage where the files with errors are copied to a Microsoft-provided Azure Storage location so that you can download them to your local computer to remediate.</span></span>

    ![Vorbereiten der Fehlerbehebung](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="f06c1-116">Nachdem die Vorbereitung abgeschlossen ist, klicken Sie auf **Weiter: Dateien herunterladen** , um den Download fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Herunterladen von Dateien](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="f06c1-118">Geben Sie zum Herunterladen von Dateien den **Ziel Pfad für den Download**an.</span><span class="sxs-lookup"><span data-stu-id="f06c1-118">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="f06c1-119">Dies ist ein Pfad auf dem lokalen Computer, auf dem die Datei heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="f06c1-119">This is a path on your local computer where the file will be downloaded.</span></span>  <span data-ttu-id="f06c1-120">Der Standardpfad,%USERPROFILE%\Downloads\errors, verweist auf den Ordner "Downloads" des angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="f06c1-120">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder.</span></span> <span data-ttu-id="f06c1-121">Sie können diesen Pfad bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="f06c1-121">You can change this path if necessary.</span></span> <span data-ttu-id="f06c1-122">Wenn Sie dies ändern, wird empfohlen, einen lokalen Dateipfad anstelle eines Remotenetzwerk Pfads zu verwenden, um eine optimale Leistung zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-122">If you do change it, we recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

6. <span data-ttu-id="f06c1-123">Kopieren Sie den vordefinierten Befehl **, indem Sie auf in Zwischenablage kopieren**klicken.</span><span class="sxs-lookup"><span data-stu-id="f06c1-123">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="f06c1-124">Starten Sie eine Windows-Eingabeaufforderung, fügen Sie den Befehl ein, und drücken Sie dann die **Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="f06c1-124">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="f06c1-125">Die Dateien werden heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-125">The files are downloaded.</span></span>

    ![Vorbereiten der Fehlerbehebung](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="f06c1-127">Sie müssen AzCopy v 8.1 verwenden, um den Befehl erfolgreich zu verwenden, der auf der Seite zum **Herunterladen von Dateien** bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f06c1-127">You must use AzCopy v8.1 to successfully use the command that's provided on the **Download files** page.</span></span> <span data-ttu-id="f06c1-128">Sie müssen auch AzCopy v 8.1 verwenden, um die Dateien in Schritt 10 unten hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-128">You also must use AzCopy v8.1 to upload the files in step 10 below.</span></span> <span data-ttu-id="f06c1-129">Informationen zum Installieren dieser Version von AzCopy finden Sie unter [übertragen von Daten mit der AzCopy v 8.1 unter Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="f06c1-129">To install this version of AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="f06c1-130">Wenn der angegebene AzCopy-Befehl fehlschlägt, finden Sie weitere Informationen unter [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="f06c1-130">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="f06c1-131">Nachdem Sie die Dateien heruntergeladen haben, können Sie Sie mit einem geeigneten Tool korrigieren.</span><span class="sxs-lookup"><span data-stu-id="f06c1-131">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="f06c1-132">Für kennwortgeschützte Dateien gibt es mehrere Kenn Wort Knack Tools, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f06c1-132">For password-protected files, there several password cracking tools you can use.</span></span> <span data-ttu-id="f06c1-133">Wenn Sie die Kennwörter für die Dateien kennen, können Sie Sie öffnen und den Kennwortschutz entfernen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-133">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="f06c1-134">Es ist wichtig, dass Sie die Verzeichnisstruktur und die Dateinamen der korrigierten Dateien in Takt halten.</span><span class="sxs-lookup"><span data-stu-id="f06c1-134">IT is important that you retain the directory structure and file names of the remediated files in tact.</span></span>  <span data-ttu-id="f06c1-135">Alle in den heruntergeladenen Dateien und Ordnern verwendeten Benennungskonventionen ermöglichen es, die remdiated-Dateien wieder dem Original zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-135">All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="f06c1-136">Kehren Sie nun zu Advanced eDiscovery zurück, und klicken Sie auf **Weiter: Dateien hochladen**.</span><span class="sxs-lookup"><span data-stu-id="f06c1-136">Now, return to Advanced eDiscovery and click **Next: Upload files**.</span></span>  <span data-ttu-id="f06c1-137">Dadurch gelangen Sie zum nächsten Schritt, in dem Sie die Dateien jetzt hochladen können.</span><span class="sxs-lookup"><span data-stu-id="f06c1-137">This will move to the next step where you can now upload the files.</span></span>

    ![Hochladen von Dateien](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="f06c1-139">Geben Sie den Speicherort der korrigierten Dateien in das Textfeld **Pfad zum Speicherort der Dateien** ein, und klicken Sie dann auf **in Zwischenablage kopieren**.</span><span class="sxs-lookup"><span data-stu-id="f06c1-139">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="f06c1-140">Fügen Sie den Befehl in eine Windows-Eingabeaufforderung ein, und drücken **Sie die EINGABETASTE** , um die Dateien hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-140">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="f06c1-142">Kehren Sie zu Advanced eDiscovery zurück, und klicken Sie auf **Weiter: Process files**.</span><span class="sxs-lookup"><span data-stu-id="f06c1-142">Return to Advanced eDiscovery and click **Next: Process files**.</span></span>

12. <span data-ttu-id="f06c1-143">Nach Abschluss der Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="f06c1-143">When processing is complete.</span></span>  <span data-ttu-id="f06c1-144">Sie können zur Überprüfungsgruppe zurückkehren und die korrigierte Datei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f06c1-144">You can return to the review set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="f06c1-145">Was geschieht, wenn Dateien behoben werden</span><span class="sxs-lookup"><span data-stu-id="f06c1-145">What happens when files are remediated</span></span>

<span data-ttu-id="f06c1-146">Bei hochzuladenden Dateien werden die ursprünglichen Metadaten mit Ausnahme der folgenden Felder beibehalten:</span><span class="sxs-lookup"><span data-stu-id="f06c1-146">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="f06c1-147">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="f06c1-147">ExtractedTextSize</span></span>
- <span data-ttu-id="f06c1-148">HasText</span><span class="sxs-lookup"><span data-stu-id="f06c1-148">HasText</span></span>
- <span data-ttu-id="f06c1-149">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="f06c1-149">IsErrorRemediate</span></span>
- <span data-ttu-id="f06c1-150">Lade-Nr</span><span class="sxs-lookup"><span data-stu-id="f06c1-150">LoadId</span></span>
- <span data-ttu-id="f06c1-151">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="f06c1-151">ProcessingErrorMessage</span></span>
- <span data-ttu-id="f06c1-152">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="f06c1-152">ProcessingStatus</span></span>
- <span data-ttu-id="f06c1-153">Text</span><span class="sxs-lookup"><span data-stu-id="f06c1-153">Text</span></span>
- <span data-ttu-id="f06c1-154">WordCount</span><span class="sxs-lookup"><span data-stu-id="f06c1-154">WordCount</span></span>
- <span data-ttu-id="f06c1-155">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="f06c1-155">WorkingsetId</span></span>

<span data-ttu-id="f06c1-156">Eine Definition aller Dokumentmetadaten-Felder in Advanced eDiscovery finden Sie unter [Document Metadata fields](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="f06c1-156">For a definition of all document metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
