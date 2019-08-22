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
ms.openlocfilehash: c9c2660929037430535c9b612218563c51b1f056
ms.sourcegitcommit: 3f3f3ecb28ef65d023f3573f9a4e09a0586d8f53
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2019
ms.locfileid: "36490792"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="50a1b-102">Beheben von Fehlern beim Verarbeiten von Daten</span><span class="sxs-lookup"><span data-stu-id="50a1b-102">Error remediation when processing data</span></span>

<span data-ttu-id="50a1b-103">Durch die Fehlerkorrektur können eDiscovery-Administratoren Daten Probleme beheben, die verhindern, dass Advanced eDiscovery die Inhalte ordnungsgemäß verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="50a1b-103">Error remediation allows eDiscovery administrators the ability to rectify data issues that prevent Advanced eDiscovery from properly processing the content.</span></span> <span data-ttu-id="50a1b-104">Beispielsweise können Dateien, die kennwortgeschützt sind, nicht verarbeitet werden, da die Dateien gesperrt oder verschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="50a1b-104">For example, files that are password protected can't be processed since the files are locked or encrypted.</span></span> <span data-ttu-id="50a1b-105">Mithilfe der Fehlerbehebung können eDiscovery-Administratoren Dateien mit solchen Fehlern herunterladen, den Kennwortschutz entfernen und dann die korrigierten Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="50a1b-105">Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection, and then upload the remediated files.</span></span>

<span data-ttu-id="50a1b-106">Verwenden Sie den folgenden Workflow, um Dateien mit Fehlern in erweiterten eDiscovery-Fällen zu beheben.</span><span class="sxs-lookup"><span data-stu-id="50a1b-106">Use the following workflow to remediate files with errors in Advanced eDiscovery cases.</span></span>

## <a name="create-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="50a1b-107">Erstellen einer Fehlerkorrektur Sitzung zum Beheben von Dateien mit Verarbeitungsfehlern</span><span class="sxs-lookup"><span data-stu-id="50a1b-107">Create an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="50a1b-108">Wenn der Fehlerkorrektur-Assistent während des folgenden Verfahrens zu einem beliebigen Zeitpunkt geschlossen wird, können Sie auf der Registerkarte **Verarbeitung** zur Fehlerbehebungssitzung zurückkehren, indem Sie im Dropdownmenü **Ansicht** die Option **Fehler** Korrekturen auswählen.</span><span class="sxs-lookup"><span data-stu-id="50a1b-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="50a1b-109">Wählen Sie auf der Registerkarte **Verarbeitung** in einem erweiterten eDiscovery-Fall im Dropdownmenü **Ansicht** die Option **Fehler** aus.</span><span class="sxs-lookup"><span data-stu-id="50a1b-109">On the **Processing** tab in an Advanced eDiscovery case, select **Errors** in the **View** drop-down menu.</span></span>

2. <span data-ttu-id="50a1b-110">Wählen Sie die Fehler aus, die Sie korrigieren möchten, indem Sie auf das Optionsfeld neben dem Fehlertyp oder-Dateityp klicken.</span><span class="sxs-lookup"><span data-stu-id="50a1b-110">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.</span></span>  <span data-ttu-id="50a1b-111">Im folgenden Beispiel werden wir eine kennwortgeschützte Datei remediationieren.</span><span class="sxs-lookup"><span data-stu-id="50a1b-111">In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="50a1b-112">Klicken Sie auf **neue Fehlerkorrektur**.</span><span class="sxs-lookup"><span data-stu-id="50a1b-112">Click **New error remediation**.</span></span>

    ![Fehlerbehebung](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="50a1b-114">Die Fehlerkorrektur-Sitzung beginnt mit einer Vorbereitungsphase, in der die Dateien mit Fehlern in einen von Microsoft bereitgestellten Azure-Speicherort kopiert werden, damit Sie Sie auf den lokalen Computer herunterladen können, um Sie zu beheben.</span><span class="sxs-lookup"><span data-stu-id="50a1b-114">The error remediation session starts with a preparation stage where the files with errors are copied to a Microsoft-provided Azure Storage location so that you can download them to your local computer to remediate.</span></span>

    ![Vorbereiten der Fehlerbehebung](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="50a1b-116">Nachdem die Vorbereitung abgeschlossen ist, klicken Sie auf **Weiter: Dateien herunterladen** , um den Download fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="50a1b-116">After the preparation is complete, click **Next: Download files** to proceed with download.</span></span>

    ![Herunterladen von Dateien](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="50a1b-118">Geben Sie zum Herunterladen von Dateien den **Ziel Pfad für den Download**an.</span><span class="sxs-lookup"><span data-stu-id="50a1b-118">To download files, specify the **Destination path for download**.</span></span> <span data-ttu-id="50a1b-119">Dies ist ein Pfad auf dem lokalen Computer, auf dem die Datei heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="50a1b-119">This is a path on your local computer where the file is downloaded.</span></span>  <span data-ttu-id="50a1b-120">Der Standardpfad,%USERPROFILE%\Downloads\errors, verweist auf den Ordner "Downloads" des angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="50a1b-120">The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder.</span></span> <span data-ttu-id="50a1b-121">Sie können diesen Pfad bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="50a1b-121">You can change this path if necessary.</span></span> <span data-ttu-id="50a1b-122">Wenn Sie es ändern, wird empfohlen, einen lokalen Dateipfad für die beste Leistung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="50a1b-122">If you do change it, we recommend that you use a local file path for the best performance.</span></span> <span data-ttu-id="50a1b-123">Verwenden Sie keinen Remotenetzwerk Pfad.</span><span class="sxs-lookup"><span data-stu-id="50a1b-123">Don't use a remote network path.</span></span>

6. <span data-ttu-id="50a1b-124">Kopieren Sie den vordefinierten Befehl **, indem Sie auf in Zwischenablage kopieren**klicken.</span><span class="sxs-lookup"><span data-stu-id="50a1b-124">Copy the predefined command by clicking **Copy to clipboard**.</span></span> <span data-ttu-id="50a1b-125">Starten Sie eine Windows-Eingabeaufforderung, fügen Sie den Befehl ein, und drücken Sie dann die **Eingabe**Taste.</span><span class="sxs-lookup"><span data-stu-id="50a1b-125">Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="50a1b-126">Die Dateien werden heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="50a1b-126">The files are downloaded.</span></span>

    ![Vorbereiten der Fehlerbehebung](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

    > [!NOTE]
    > <span data-ttu-id="50a1b-128">Sie müssen AzCopy v 8.1 verwenden, um den Befehl erfolgreich zu verwenden, der auf der Seite zum **Herunterladen von Dateien** bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="50a1b-128">You must use AzCopy v8.1 to successfully use the command that's provided on the **Download files** page.</span></span> <span data-ttu-id="50a1b-129">Sie müssen auch AzCopy v 8.1 verwenden, um die Dateien in Schritt 10 unten hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="50a1b-129">You also must use AzCopy v8.1 to upload the files in step 10 below.</span></span> <span data-ttu-id="50a1b-130">Informationen zum Installieren dieser Version von AzCopy finden Sie unter [übertragen von Daten mit der AzCopy v 8.1 unter Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="50a1b-130">To install this version of AzCopy, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="50a1b-131">Wenn der angegebene AzCopy-Befehl fehlschlägt, finden Sie weitere Informationen unter [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span><span class="sxs-lookup"><span data-stu-id="50a1b-131">If the supplied AzCopy command fails, please see [Troubleshoot AzCopy in Advanced eDiscovery](troubleshooting-azcopy.md).</span></span>

7. <span data-ttu-id="50a1b-132">Nachdem Sie die Dateien heruntergeladen haben, können Sie Sie mit einem geeigneten Tool korrigieren.</span><span class="sxs-lookup"><span data-stu-id="50a1b-132">After downloading the files, you can remediate them with an appropriate tool.</span></span> <span data-ttu-id="50a1b-133">Für kennwortgeschützte Dateien gibt es mehrere Kenn Wort Knack Tools, die Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="50a1b-133">For password-protected files, there several password cracking tools you can use.</span></span> <span data-ttu-id="50a1b-134">Wenn Sie die Kennwörter für die Dateien kennen, können Sie Sie öffnen und den Kennwortschutz entfernen.</span><span class="sxs-lookup"><span data-stu-id="50a1b-134">If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="50a1b-135">Es ist wichtig, dass Sie die Verzeichnisstruktur und die Dateinamen der korrigierten Dateien beibehalten.</span><span class="sxs-lookup"><span data-stu-id="50a1b-135">It's important that you retain the directory structure and file names of the remediated files.</span></span> <span data-ttu-id="50a1b-136">Die Pfadnamen der heruntergeladenen Dateien und Ordner ermöglichen das Zuordnen der korrigierten Dateien zu den Originaldateien.</span><span class="sxs-lookup"><span data-stu-id="50a1b-136">The path names of the downloaded files and folders make it possible to associate the remediated files with the original files.</span></span>  <span data-ttu-id="50a1b-137">Wenn die Verzeichnisstruktur oder die Dateinamen geändert werden, erhalten Sie den folgenden Fehler: `Cannot apply Error Remediation to the current Workingset`.</span><span class="sxs-lookup"><span data-stu-id="50a1b-137">If the directory structure or file names are changed, you'll receive the following error: `Cannot apply Error Remediation to the current Workingset`.</span></span>

8. <span data-ttu-id="50a1b-138">Kehren Sie nun zu Advanced eDiscovery zurück, und klicken Sie auf **Weiter: Dateien hochladen**.</span><span class="sxs-lookup"><span data-stu-id="50a1b-138">Now, return to Advanced eDiscovery and click **Next: Upload files**.</span></span>  <span data-ttu-id="50a1b-139">Dadurch gelangen Sie zum nächsten Schritt, in dem Sie die Dateien jetzt hochladen können.</span><span class="sxs-lookup"><span data-stu-id="50a1b-139">This will move to the next step where you can now upload the files.</span></span>

    ![Hochladen von Dateien](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="50a1b-141">Geben Sie den Speicherort der korrigierten Dateien in das Textfeld **Pfad zum Speicherort der Dateien** ein, und klicken Sie dann auf **in Zwischenablage kopieren**.</span><span class="sxs-lookup"><span data-stu-id="50a1b-141">Specify the location of the remediated files in the **Path to location of files** text box, then click **Copy to clipboard**.</span></span>

10. <span data-ttu-id="50a1b-142">Fügen Sie den Befehl in eine Windows-Eingabeaufforderung ein, und drücken **Sie die EINGABETASTE** , um die Dateien hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="50a1b-142">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6. png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="50a1b-144">Kehren Sie zu Advanced eDiscovery zurück, und klicken Sie auf **Weiter: Process files**.</span><span class="sxs-lookup"><span data-stu-id="50a1b-144">Return to Advanced eDiscovery and click **Next: Process files**.</span></span>

12. <span data-ttu-id="50a1b-145">Nach Abschluss der Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="50a1b-145">When processing is complete.</span></span> <span data-ttu-id="50a1b-146">Sie können zur Überprüfungsgruppe zurückkehren und die korrigierte Datei anzeigen.</span><span class="sxs-lookup"><span data-stu-id="50a1b-146">You can return to the review set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="50a1b-147">Was geschieht, wenn Dateien behoben werden</span><span class="sxs-lookup"><span data-stu-id="50a1b-147">What happens when files are remediated</span></span>

<span data-ttu-id="50a1b-148">Bei hochzuladenden Dateien werden die ursprünglichen Metadaten mit Ausnahme der folgenden Felder beibehalten:</span><span class="sxs-lookup"><span data-stu-id="50a1b-148">When remediated files are uploaded, the original metadata is preserved except for the following fields:</span></span> 

- <span data-ttu-id="50a1b-149">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="50a1b-149">ExtractedTextSize</span></span>
- <span data-ttu-id="50a1b-150">HasText</span><span class="sxs-lookup"><span data-stu-id="50a1b-150">HasText</span></span>
- <span data-ttu-id="50a1b-151">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="50a1b-151">IsErrorRemediate</span></span>
- <span data-ttu-id="50a1b-152">Lade-Nr</span><span class="sxs-lookup"><span data-stu-id="50a1b-152">LoadId</span></span>
- <span data-ttu-id="50a1b-153">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="50a1b-153">ProcessingErrorMessage</span></span>
- <span data-ttu-id="50a1b-154">ProcessingStatus</span><span class="sxs-lookup"><span data-stu-id="50a1b-154">ProcessingStatus</span></span>
- <span data-ttu-id="50a1b-155">Text</span><span class="sxs-lookup"><span data-stu-id="50a1b-155">Text</span></span>
- <span data-ttu-id="50a1b-156">WordCount</span><span class="sxs-lookup"><span data-stu-id="50a1b-156">WordCount</span></span>
- <span data-ttu-id="50a1b-157">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="50a1b-157">WorkingsetId</span></span>

<span data-ttu-id="50a1b-158">Eine Definition aller Metadatenfelder in Advanced eDiscovery finden Sie unter [Document Metadata fields](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="50a1b-158">For a definition of all metadata fields in Advanced eDiscovery, see [Document metadata fields](document-metadata-fields.md).</span></span>
