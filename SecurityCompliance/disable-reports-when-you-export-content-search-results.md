---
title: Deaktivieren von Berichten beim Exportieren von Inhalts Suchergebnissen im Office 365 Security &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Bearbeiten Sie die Windows-Registrierung auf dem lokalen Computer, um Berichte zu deaktivieren, wenn Sie die Ergebnisse einer Inhaltssuche aus dem &amp; Office 365 Security Comliance Center exportieren. Durch das Deaktivieren dieser Berichte kann die Downloadzeit beschleunigt und Speicherplatz gespart werden.
ms.openlocfilehash: 0be2be18eaccb618a49e1b58a5c0e53d0a339d1e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213475"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="44ffa-104">Deaktivieren von Berichten beim Exportieren von Inhalts Suchergebnissen im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="44ffa-104">Disable reports when you export Content Search results in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="44ffa-p102">Wenn Sie das Office 365 eDiscovery-Export Tool verwenden, um die Ergebnisse einer Inhaltssuche im Security &amp; Compliance Center zu exportieren, erstellt und exportiert das Tool automatisch zwei Berichte, die zusätzliche Informationen zu den exportierten Inhalten enthalten. Diese Berichte sind die Datei results. CSV und die Datei Manifest. XML (Lesen Sie den Abschnitt [häufig gestellte Fragen zum Deaktivieren von Export Berichten](#frequently-asked-questions-about-disabling-export-reports) in diesem Thema für detaillierte Beschreibungen dieser Berichte). Da diese Dateien sehr umfangreich sein können, können Sie die Downloadzeit beschleunigen und Speicherplatz sparen, indem Sie verhindern, dass diese Dateien exportiert werden. Ändern Sie dazu die Windows-Registrierung auf dem Computer, den Sie zum Exportieren der Suchergebnisse verwenden. Wenn Sie die Berichte zu einem späteren Zeitpunkt hinzufügen möchten, können Sie die Registrierungseinstellung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="44ffa-p102">When you use the Office 365 eDiscovery Export tool to export the results of a Content Search in the Security &amp; Compliance Center, the tool automatically creates and exports two reports that contain additional information about the exported content. These reports are the Results.csv file and the Manifest.xml file (see the [Frequently asked questions about disabling export reports](#frequently-asked-questions-about-disabling-export-reports) section in this topic for detailed descriptions of these reports). Because these files can be very large, you can speed up the download time and save disk space by preventing these files from being exported. You can do this by changing the Windows Registry on the computer that you use to export the search results. If you want to include the reports at a later time, you can edit the registry setting.</span></span> 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a><span data-ttu-id="44ffa-110">Erstellen von Registrierungseinstellungen zum Deaktivieren der Export Berichte</span><span class="sxs-lookup"><span data-stu-id="44ffa-110">Create registry settings to disable the export reports</span></span>

<span data-ttu-id="44ffa-111">Führen Sie auf dem Computer, auf dem Sie die Ergebnisse einer Inhaltssuche exportieren möchten, das folgende Verfahren aus.</span><span class="sxs-lookup"><span data-stu-id="44ffa-111">Perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="44ffa-112">Schließen Sie das Office 365 eDiscovery-Export Tool, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="44ffa-112">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="44ffa-113">Führen Sie einen oder beide der folgenden Schritte aus, je nachdem, welchen Exportbericht Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="44ffa-113">Perform one or both of the following steps, depending on which export report you want to disable.</span></span>
    
    - <span data-ttu-id="44ffa-114">**Results. CSV**</span><span class="sxs-lookup"><span data-stu-id="44ffa-114">**Results.csv**</span></span>
    
      <span data-ttu-id="44ffa-115">Speichern Sie den folgenden Text in einer Windows-Registrierungsdatei mithilfe eines filename-Suffixes von. reg; Beispiel: DisableResultsCsv. reg.</span><span class="sxs-lookup"><span data-stu-id="44ffa-115">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableResultsCsv.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - <span data-ttu-id="44ffa-116">**Manifest. XML**</span><span class="sxs-lookup"><span data-stu-id="44ffa-116">**Manifest.xml**</span></span>
    
      <span data-ttu-id="44ffa-117">Speichern Sie den folgenden Text in einer Windows-Registrierungsdatei mithilfe eines filename-Suffixes von. reg; Beispiel: DisableManifestXml. reg.</span><span class="sxs-lookup"><span data-stu-id="44ffa-117">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableManifestXml.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. <span data-ttu-id="44ffa-118">Klicken oder Doppelklicken Sie in Windows Explorer auf die. reg-Datei, die Sie in den vorherigen Schritten erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="44ffa-118">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
4. <span data-ttu-id="44ffa-119">Klicken Sie im Fenster Benutzerzugriffssteuerung auf **Ja** , um die Änderung des Registrierungs-Editors zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="44ffa-119">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="44ffa-120">Wenn Sie zum Fortfahren aufgefordert werden, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="44ffa-120">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="44ffa-121">Der Registrierungs-Editor zeigt eine Meldung an, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="44ffa-121">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a><span data-ttu-id="44ffa-122">Bearbeiten von Registrierungseinstellungen zum erneuten Aktivieren der Export Berichte</span><span class="sxs-lookup"><span data-stu-id="44ffa-122">Edit registry settings to re-enable the export reports</span></span>

<span data-ttu-id="44ffa-p103">Wenn Sie die Berichte "results. csv" und "Manifest. xml" deaktiviert haben, indem Sie die. reg-Dateien im vorherigen Verfahren erstellt haben, können Sie diese Dateien bearbeiten, um einen Bericht erneut zu aktivieren, sodass er mit den Suchergebnissen exportiert wird. Führen Sie erneut das folgende Verfahren auf dem Computer aus, auf dem Sie die Ergebnisse einer Inhaltssuche exportieren.</span><span class="sxs-lookup"><span data-stu-id="44ffa-p103">If you disabled the Results.csv and Manifest.xml reports by creating the .reg files in the previous procedure, you can edit those files to re-enable a report so that it's exported with the search results. Again, perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="44ffa-125">Schließen Sie das Office 365 eDiscovery-Export Tool, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="44ffa-125">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="44ffa-126">Bearbeiten Sie eine oder beide der reg-Bearbeitungs Dateien, die Sie im vorherigen Verfahren erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="44ffa-126">Edit one or both of the .reg edit files that you created in the previous procedure.</span></span>
    
    - <span data-ttu-id="44ffa-127">**Results. CSV**</span><span class="sxs-lookup"><span data-stu-id="44ffa-127">**Results.csv**</span></span>
    
        <span data-ttu-id="44ffa-p104">Öffnen Sie die Datei DisableResultsCsv. reg im Editor, ändern Sie `False` den `True`Wert in, und speichern Sie die Datei. Nach dem Bearbeiten der Datei sieht es beispielsweise wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="44ffa-p104">Open the DisableResultsCsv.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - <span data-ttu-id="44ffa-130">**Manifest. XML**</span><span class="sxs-lookup"><span data-stu-id="44ffa-130">**Manifest.xml**</span></span>
    
        <span data-ttu-id="44ffa-p105">Öffnen Sie die Datei DisableManifestXml. reg im Editor, ändern Sie `False` den `True`Wert in, und speichern Sie die Datei. Nach dem Bearbeiten der Datei sieht es beispielsweise wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="44ffa-p105">Open the DisableManifestXml.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. <span data-ttu-id="44ffa-133">Klicken oder Doppelklicken Sie in Windows Explorer auf eine REG-Datei, die Sie im vorherigen Schritt bearbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="44ffa-133">In Windows Explorer, click or double-click a .reg file that you edited in the previous step.</span></span>
    
4. <span data-ttu-id="44ffa-134">Klicken Sie im Fenster Benutzerzugriffssteuerung auf **Ja** , um die Änderung des Registrierungs-Editors zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="44ffa-134">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="44ffa-135">Wenn Sie zum Fortfahren aufgefordert werden, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="44ffa-135">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="44ffa-136">Der Registrierungs-Editor zeigt eine Meldung an, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="44ffa-136">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a><span data-ttu-id="44ffa-137">Häufig gestellte Fragen zum Deaktivieren von Export Berichten</span><span class="sxs-lookup"><span data-stu-id="44ffa-137">Frequently asked questions about disabling export reports</span></span>
<span data-ttu-id="44ffa-138"><a name="faqs"> </a></span><span class="sxs-lookup"><span data-stu-id="44ffa-138"></span></span>

 <span data-ttu-id="44ffa-139">**Was sind die Berichte "results. csv" und "Manifest. xml"?**</span><span class="sxs-lookup"><span data-stu-id="44ffa-139">**What are the Results.csv and Manifest.xml reports?**</span></span>
  
<span data-ttu-id="44ffa-140">Die Dateien results. CSV und Manifest. XML enthalten zusätzliche Informationen zu den exportierten Inhalten.</span><span class="sxs-lookup"><span data-stu-id="44ffa-140">The Results.csv and Manifest.xml files contain additional information about the content that was exported.</span></span>
  
- <span data-ttu-id="44ffa-p106">**Results. CSV** ein Excel-Dokument, das Informationen zu jedem Element enthält, das als Suchergebnis heruntergeladen wird. Für e-Mails enthält das Ergebnisprotokoll Informationen zu den einzelnen Nachrichten, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="44ffa-p106">**Results.csv** An Excel document that contains information about each item that is download as a search result. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="44ffa-143">Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).</span><span class="sxs-lookup"><span data-stu-id="44ffa-143">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="44ffa-144">Das Datum, an dem die Nachricht gesendet oder empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="44ffa-144">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="44ffa-145">Die Betreffzeile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="44ffa-145">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="44ffa-146">Absender und Empfänger der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="44ffa-146">The sender and recipients of the message.</span></span>
    
  - <span data-ttu-id="44ffa-p107">Gibt an, ob es sich bei der Nachricht um eine doppelte Nachricht handelt, wenn Sie beim Exportieren der Suchergebnisse Deduplizierung aktiviert haben. Doppelte Nachrichten haben einen Wert in der **ÜbergeordnetEn Itemid** -Spalte, die die Nachricht als Duplikat identifiziert. Der Wert in der **ÜbergeordnetEn Itemid** -Spalte ist identisch mit dem Wert in der Spalte **Element-Dokument-Nr** der Nachricht, die exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="44ffa-p107">Whether the message is a duplicate message if you enabled de-duplication when exporting the search results. Duplicate messages will have a value in the **Parent ItemId** column that identifies the message as a duplicate. The value in the **Parent ItemId** column is the same as the value in the **Item DocumentId** column of the message that was exported.</span></span> 
    
    <span data-ttu-id="44ffa-150">Für Dokumente aus SharePoint und OneDrive for Business-Websites enthält das Ergebnisprotokoll Informationen zu jedem Dokument, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="44ffa-150">For documents from SharePoint and OneDrive for Business sites, the result log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="44ffa-151">Die URL für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="44ffa-151">The URL for the document.</span></span>
    
  - <span data-ttu-id="44ffa-152">Die URL für die Websitesammlung, in der sich das Dokument befindet.</span><span class="sxs-lookup"><span data-stu-id="44ffa-152">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="44ffa-153">Das Datum, an dem das Dokument zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="44ffa-153">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="44ffa-154">Der Name des Dokuments (das sich in der Spalte Betreff im Ergebnisprotokoll befindet).</span><span class="sxs-lookup"><span data-stu-id="44ffa-154">The name of the document (which is located in the Subject column in the result log).</span></span>
    
- <span data-ttu-id="44ffa-p108">**Manifest. XML** eine Manifestdatei (im XML-Format), die Informationen zu jedem in den Suchergebnissen enthaltenen Element enthält. Die Informationen in diesem Bericht sind identisch mit dem Bericht "results. csv", aber es ist in dem Format, das im Electronic Discovery Reference Model (EDRM) angegeben ist. Weitere Informationen zu EDRM finden Sie unter [https://www.edrm.net](https://www.edrm.net).</span><span class="sxs-lookup"><span data-stu-id="44ffa-p108">**Manifest.xml** A manifest file (in XML format) that contains information about each item included in the search results. The information in this report is the same as the Results.csv report, but it's in the format specified by the Electronic Discovery Reference Model (EDRM). For more information about EDRM, go to [https://www.edrm.net](https://www.edrm.net).</span></span>
    
 <span data-ttu-id="44ffa-158">**Wann sollte ich den Export dieser Berichte deaktivieren?**</span><span class="sxs-lookup"><span data-stu-id="44ffa-158">**When should I disable exporting these reports?**</span></span>
  
<span data-ttu-id="44ffa-p109">Es hängt von ihren spezifischen Anforderungen ab. Viele Organisationen benötigen keine zusätzlichen Informationen zu Suchergebnissen und benötigen diese Berichte nicht.</span><span class="sxs-lookup"><span data-stu-id="44ffa-p109">It depends on your specific needs. Many organizations don't require additional information about search results, and don't need these reports.</span></span>
  
 <span data-ttu-id="44ffa-161">**Auf welchem Computer muss ich vorgehen?**</span><span class="sxs-lookup"><span data-stu-id="44ffa-161">**What computer do I have to do this on?**</span></span>
  
 <span data-ttu-id="44ffa-162">Sie müssen die Registrierungseinstellung auf jedem lokalen Computer ändern, auf dem Sie das Office 365 eDiscovery-Export Tool ausführen.</span><span class="sxs-lookup"><span data-stu-id="44ffa-162">You have to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span> 
  
 <span data-ttu-id="44ffa-163">**Muss ich den Computer neu starten, nachdem ich diese Einstellung geändert habe?**</span><span class="sxs-lookup"><span data-stu-id="44ffa-163">**After I change this setting, do I have to restart the computer?**</span></span>
  
<span data-ttu-id="44ffa-p110">Nein, Sie müssen den Computer nicht neu starten. Wenn jedoch das Office 365 eDiscovery-Export Tool läuft, müssen Sie es schließen und neu starten, nachdem Sie die Registrierungseinstellung geändert haben.</span><span class="sxs-lookup"><span data-stu-id="44ffa-p110">No, you don't have to restart the computer. But if the Office 365 eDiscovery Export tool is running, you have to close it and then restart it after you change the registry setting.</span></span>
  
 <span data-ttu-id="44ffa-166">**Wird ein vorhandener Registrierungsschlüssel bearbeitet oder wird ein neuer Schlüssel erstellt?**</span><span class="sxs-lookup"><span data-stu-id="44ffa-166">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="44ffa-p111">Bei der ersten Ausführung der reg-Datei, die Sie im Verfahren in diesem Thema erstellt haben, wird ein neuer Registrierungsschlüssel erstellt. Dann wird die Einstellung jedes Mal bearbeitet, wenn Sie die reg-Bearbeitungs Datei ändern und erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="44ffa-p111">A new registry key is created the first time you run the .reg file that you created in the procedure in this topic. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
