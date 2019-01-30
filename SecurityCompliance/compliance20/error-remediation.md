---
title: Error Remediation beim Verarbeiten von Daten
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: ''
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 82e6d44ded64d586611f429f9b3eebe4f47e9898
ms.sourcegitcommit: ee28ee2b2bdfd049333c2f495d7f7780d13af4a6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29607832"
---
# <a name="error-remediation-when-processing-data"></a><span data-ttu-id="ffe3c-102">Error Remediation beim Verarbeiten von Daten</span><span class="sxs-lookup"><span data-stu-id="ffe3c-102">Error remediation when processing data</span></span>

<span data-ttu-id="ffe3c-p101">Error Remediation kann eDiscovery-Administratoren die Möglichkeit zum Beheben von Problemen mit der die verhindern, dass die erweiterte eDiscovery (Preview) ordnungsgemäß verarbeiten des Inhalts. Dateien, die ein Kennwort geschützt sind können beispielsweise verarbeitet werden, da die Dateien gesperrt oder verschlüsselt werden. Error Remediation verwenden, können eDiscovery-Administratoren Downloaddateien mit derartige Fehler, Entfernen des Kennwortschutzes und die für gewartete Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-p101">Error remediation allows eDiscovery administrators the ability to rectify data issues which prevent Advanced eDiscovery (Preview) from properly processing the content. For example, files that are password protected cannot be processed since the files are locked or encrypted. Using error remediation, eDiscovery administrators can download files with such errors, remove the password protection and upload the remediated files.</span></span>

<span data-ttu-id="ffe3c-106">Verwenden Sie den folgenden Workflow zum Warten von Dateien mit Fehlern in Fällen erweiterte eDiscovery (Preview).</span><span class="sxs-lookup"><span data-stu-id="ffe3c-106">Use the following workflow to remediate files with errors in Advanced eDiscovery (Preview) cases.</span></span>

## <a name="creating-an-error-remediation-session-to-remediate-files-with-processing-errors"></a><span data-ttu-id="ffe3c-107">Erstellen eine Error Remediation Sitzung zum Warten von Dateien mit der Verarbeitung von Fehlern</span><span class="sxs-lookup"><span data-stu-id="ffe3c-107">Creating an error remediation session to remediate files with processing errors</span></span>

>[!NOTE]
><span data-ttu-id="ffe3c-108">Wenn der der Fehler Remediation-Assistent geschlossen ist, können Sie jederzeit während des folgenden Verfahrens, können Sie zurückgeben der Error Remediation-Sitzung auf der Registerkarte **Verarbeitung** **Fehler Bereinigungsstatus** in das Dropdownmenü **Ansicht** auswählen.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-108">If the the error remediation wizard is closed at any time during the following procedure, you can return to the error remediation session from the **Processing** tab by selecting **Error remediations** in the **View** drop down menu.</span></span>

1. <span data-ttu-id="ffe3c-109">Wählen Sie auf der Registerkarte **Verarbeitung** in einem erweiterten eDiscovery (Preview)-Fall **Fehler** in das Dropdownmenü **Ansicht** aus.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-109">On the **Processing** tab in an Advanced eDiscovery (Preview) case, select **Errors** in the **View** drop down menu.</span></span>

2. <span data-ttu-id="ffe3c-p102">Wählen Sie die Fehler, den, die Sie durch Klicken auf das Optionsfeld neben den Fehlertyp oder der Dateityp warten möchten.  Im folgenden Beispiel haben wir eine kennwortgeschützte Datei Korrigieren von.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-p102">Select the errors you want to remediate by clicking the radio button next to either the error type or file type.  In the following example, we're remediating a password protected file.</span></span>

3. <span data-ttu-id="ffe3c-112">Klicken Sie auf **+ Neues Error Remediation**.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-112">Click **+ New error remediation**.</span></span>

    ![Error remediation](../media/8c2faf1a-834b-44fc-b418-6a18aed8b81a.png)

    <span data-ttu-id="ffe3c-114">Die Fehler Remediation-Sitzung wird gestartet, beginnend mit einer Vorbereitung Phase, in der das Dateifehler an einem sicheren Speicherort Azure verschoben heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-114">The error remediation session will begin, starting with a preparation stage where the files that errored are moved to a secure Azure location to be downloaded.</span></span>

    ![Vorbereiten der Error remediation](../media/390572ec-7012-47c4-a6b6-4cbb5649e8a8.png)

4. <span data-ttu-id="ffe3c-116">Nachdem die Vorbereitung abgeschlossen ist, klicken Sie auf **Weiter: Downloaddateien** Download fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-116">After the preparation is completed, click **Next: Download files** to proceed with download.</span></span>

    ![Herunterladen von Dateien](../media/6ac04b09-8e13-414a-9e24-7c75ba586363.png)

5. <span data-ttu-id="ffe3c-p103">Informationen zum Herunterladen von Dateien anzugeben Sie den **Zielpfad für den Download**. Hierbei handelt es sich um einen Pfad auf dem lokalen Computer, auf dem die Datei heruntergeladen werden soll.  Der Standardpfad % USERPROFILE%\Downloads\errors, verweist auf des angemeldeten Benutzers Downloads Ordner; Dies kann bei Bedarf geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-p103">To download files, specify the **Destination path for download**; this is a path on your local computer where the file should be downloaded.  The default path, %USERPROFILE%\Downloads\errors, points to the logged-in user's downloads folder; this can be changed as needed.</span></span>

    >[!NOTE]
    ><span data-ttu-id="ffe3c-120">Es wird empfohlen, dass Sie einen lokalen Pfad anstelle einer remote Netzwerkpfad für eine optimale Leistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-120">We recommend that you use a local file path instead of a remote network path for optimal performance.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ffe3c-121">Wenn Sie AzCopy nicht installiert haben, können Sie es dort installieren:https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span><span class="sxs-lookup"><span data-stu-id="ffe3c-121">If you haven't installed AzCopy, you can install it from here: https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy</span></span>

6. <span data-ttu-id="ffe3c-p104">Kopieren Sie den vordefinierten Befehl durch Klicken auf **in die Zwischenablage kopieren**. Starten einer Windows-Eingabeaufforderung, fügen Sie den Befehl ein, und drücken Sie die **EINGABETASTE**.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-p104">Copy the predefined command by clicking **Copy to clipboard**. Start a windows command prompt, paste the command, and then press **Enter**.</span></span>  

    <span data-ttu-id="ffe3c-124">Die Dateien werden heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-124">The files will be downloaded.</span></span>

    ![Vorbereiten der Error remediation](../media/f364ab4d-31c5-4375-b69f-650f694a2f69.png)

     > [!NOTE]
     > <span data-ttu-id="ffe3c-126">Wenn Sie Probleme mit diesem Befehl ausgeführt haben, finden Sie unter https://go.microsoft.com/fwlink/?linkid=2038117 Tipps zur Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-126">If you have issues running this command, see https://go.microsoft.com/fwlink/?linkid=2038117 for troubleshooting tips.</span></span>

7. <span data-ttu-id="ffe3c-p105">Nach dem Herunterladen der Dateien, können Sie diese mit einem geeigneten Tool warten. Für kennwortgeschützte Dateien schützen stehen Ihnen eine Reihe von Kennwörtern Tools, die Sie verwenden können. Wenn Sie die Kennwörter für die Dateien kennen, können Sie öffnen und den Kennwortschutz entfernen.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-p105">After downloading the files, you can remediate them with an appropriate tool. For password protected files, there are a number of password cracking tools you can use. If you know the passwords for the files, you can open them and remove the password protection.</span></span>
    > [!NOTE]
    > <span data-ttu-id="ffe3c-p106">IT ist wichtig, dass Sie die Directory-Struktur und den Dateinamen der Dateien für gewartete intakt beibehalten.  Alle Namenskonventionen verwendet wird, in den heruntergeladenen Dateien und Ordner ermöglichen, ordnen Sie die Dateien Remdiated wieder in den ursprünglichen.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-p106">IT is important that you retain the directory structure and file names of the remediated files in tact.  All naming conventions used in the downloaded files and folders make it possible to associate the remdiated files back to the original.</span></span>

8. <span data-ttu-id="ffe3c-p107">Nun, erweiterte eDiscovery (Preview) zurück, und klicken Sie auf **Weiter: Hochladen von Dateien**.  Dies wird mit dem nächsten Schritt verschieben, können Sie jetzt die Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-p107">Now, return to Advanced eDiscovery (Preview) and click **Next: Upload files**.  This will move to the next step where you can now upload the files.</span></span>

    ![Hochladen von Dateien](../media/af3d8617-1bab-4ecd-8de0-22e53acba240.png)

9. <span data-ttu-id="ffe3c-135">Geben Sie den Speicherort der Dateien in das Textfeld **Pfad zum Speicherort der Dateien** für gewartete klicken Sie dann auf **in Clibpboard kopieren**.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-135">Specifiy the location of the remediated files in the **Path to location of files** text box, then click **Copy to clibpboard**.</span></span>

10. <span data-ttu-id="ffe3c-136">Fügen Sie den Befehl in einer Windows-Eingabeaufforderung, und drücken Sie die **EINGABETASTE** , um die Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-136">Paste the command into a Windows Command Prompt and press **Enter** to upload the files.</span></span>

    ![ff2ff691-629f-4065-9b37-5333f937daf6.png](../media/ff2ff691-629f-4065-9b37-5333f937daf6.png)

11. <span data-ttu-id="ffe3c-138">Schließlich erweiterte eDiscovery (Preview) zurück, und klicken Sie auf **Weiter: Dateien verarbeiten**.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-138">Finally, return to Advanced eDiscovery (Preview) and click **Next: Process files**.</span></span>

12. <span data-ttu-id="ffe3c-p108">Wenn die Verarbeitung abgeschlossen ist.  Sie können die Arbeitsseiten zurück, und finden Sie in der Datei für gewartete.</span><span class="sxs-lookup"><span data-stu-id="ffe3c-p108">When processing is complete.  You can return to the working set and see the remediated file.</span></span>

## <a name="what-happens-when-files-are-remediated"></a><span data-ttu-id="ffe3c-141">Was geschieht, wenn Dateien behoben wurden</span><span class="sxs-lookup"><span data-stu-id="ffe3c-141">What happens when files are remediated</span></span>

<span data-ttu-id="ffe3c-142">Wenn für gewartete Dateien hochgeladen werden, wird die ursprüngliche Metadaten mit Ausnahme der folgenden Felder beibehalten:</span><span class="sxs-lookup"><span data-stu-id="ffe3c-142">When remediated files are uploaded, the original metadata is preserved with the exception of the following fields:</span></span> 

- <span data-ttu-id="ffe3c-143">DocumentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="ffe3c-143">DocumentExtractedUrl</span></span>
- <span data-ttu-id="ffe3c-144">ExtractedTextSize</span><span class="sxs-lookup"><span data-stu-id="ffe3c-144">ExtractedTextSize</span></span>
- <span data-ttu-id="ffe3c-145">HasText</span><span class="sxs-lookup"><span data-stu-id="ffe3c-145">HasText</span></span>
- <span data-ttu-id="ffe3c-146">IsErrorRemediate</span><span class="sxs-lookup"><span data-stu-id="ffe3c-146">IsErrorRemediate</span></span>
- <span data-ttu-id="ffe3c-147">IsParentExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="ffe3c-147">IsParentExtractedUrl</span></span>
- <span data-ttu-id="ffe3c-148">ItemExtractedUrl</span><span class="sxs-lookup"><span data-stu-id="ffe3c-148">ItemExtractedUrl</span></span>
- <span data-ttu-id="ffe3c-149">LoadId</span><span class="sxs-lookup"><span data-stu-id="ffe3c-149">LoadId</span></span>
- <span data-ttu-id="ffe3c-150">ProcessingErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ffe3c-150">ProcessingErrorMessage</span></span>
- <span data-ttu-id="ffe3c-151">Verarbeitungsstatusname</span><span class="sxs-lookup"><span data-stu-id="ffe3c-151">ProcessingStatus</span></span>
- <span data-ttu-id="ffe3c-152">Text</span><span class="sxs-lookup"><span data-stu-id="ffe3c-152">Text</span></span>
- <span data-ttu-id="ffe3c-153">WordCount</span><span class="sxs-lookup"><span data-stu-id="ffe3c-153">WordCount</span></span>
- <span data-ttu-id="ffe3c-154">WorkingsetId</span><span class="sxs-lookup"><span data-stu-id="ffe3c-154">WorkingsetId</span></span>

<span data-ttu-id="ffe3c-155">Eine Definition aller Dokument Metadaten-Felder in erweiterten eDiscovery (Preview) finden Sie unter [Metadatenfelder Dokument](document-metadata-fields.md).</span><span class="sxs-lookup"><span data-stu-id="ffe3c-155">For a definition of all document metadata fields in Advanced eDiscovery (Preview), see [Document metadata fields](document-metadata-fields.md).</span></span>