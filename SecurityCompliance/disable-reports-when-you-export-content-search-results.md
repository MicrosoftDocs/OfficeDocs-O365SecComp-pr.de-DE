---
title: Deaktivieren von Berichten beim Exportieren von Suchergebnissen in die Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Bearbeiten Sie die Windows-Registrierung auf dem lokalen Computer, um Berichte zu deaktivieren, wenn Sie die Ergebnisse einer Suche Content aus der Office 365-Sicherheit exportieren &amp; Comliance Center. Deaktivieren diese Berichte kann Download beschleunigen und Speicherplatz.
ms.openlocfilehash: 3c09e0563ddd4469f21950dc3a698ce08b0014df
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529977"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a><span data-ttu-id="928c7-104">Deaktivieren von Berichten beim Exportieren von Suchergebnissen in die Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="928c7-104">Disable reports when you export Content Search results in the Office 365 Security &amp; Compliance Center</span></span>

<span data-ttu-id="928c7-p102">Wenn Sie das Office 365 eDiscovery-Export-Tool verwenden, um exportieren Sie die Ergebnisse einer Suche Inhalte in das Wertpapier &amp; Compliance Center, das Tool automatisch erstellt und exportiert zwei Berichte, die zusätzliche Informationen über die exportierten Inhalte enthalten. Diese Berichte sind die Results.csv und die Datei Manifest.xml (Siehe den Abschnitt [häufig gestellte Fragen zum Deaktivieren von Exportieren von Berichten](#frequently-asked-questions-about-disabling-export-reports) in diesem Thema eine ausführliche Beschreibung dieser Berichte). Da diese Dateien sehr groß sein können, können Download beschleunigen und Speicherplatz sparen, indem Sie verhindern, dass diese Dateien exportiert wird. Hierzu können Sie der Windows-Registrierung auf dem Computer, mit denen Sie die Suchergebnisse exportieren ändern. Wenn Sie die Berichte zu einem späteren Zeitpunkt einschließen möchten, können Sie die registrierungseinstellung bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="928c7-p102">When you use the Office 365 eDiscovery Export tool to export the results of a Content Search in the Security &amp; Compliance Center, the tool automatically creates and exports two reports that contain additional information about the exported content. These reports are the Results.csv file and the Manifest.xml file (see the [Frequently asked questions about disabling export reports](#frequently-asked-questions-about-disabling-export-reports) section in this topic for detailed descriptions of these reports). Because these files can be very large, you can speed up the download time and save disk space by preventing these files from being exported. You can do this by changing the Windows Registry on the computer that you use to export the search results. If you want to include the reports at a later time, you can edit the registry setting.</span></span> 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a><span data-ttu-id="928c7-110">Erstellen von Einstellungen in der Registrierung, um das Exportieren von Berichten zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="928c7-110">Create registry settings to disable the export reports</span></span>

<span data-ttu-id="928c7-111">Führen Sie das folgende Verfahren auf dem Computer, mit denen Sie die Ergebnisse einer Inhaltssuche exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="928c7-111">Perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="928c7-112">Schließen Sie das Office 365 eDiscovery-Export-Tool aus, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="928c7-112">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="928c7-113">Führen Sie eine oder beide der folgenden Schritte aus, je nach dem, die Bericht exportieren Sie deaktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="928c7-113">Perform one or both of the following steps, depending on which export report you want to disable.</span></span>
    
    - <span data-ttu-id="928c7-114">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="928c7-114">**Results.csv**</span></span>
    
      <span data-ttu-id="928c7-115">Speichern Sie den folgenden Text zu einer Windows-Registrierungsdatei mithilfe der Dateiname Suffix reg; beispielsweise DisableResultsCsv.reg.</span><span class="sxs-lookup"><span data-stu-id="928c7-115">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableResultsCsv.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - <span data-ttu-id="928c7-116">**"Manifest.xml"**</span><span class="sxs-lookup"><span data-stu-id="928c7-116">**Manifest.xml**</span></span>
    
      <span data-ttu-id="928c7-117">Speichern Sie den folgenden Text zu einer Windows-Registrierungsdatei mithilfe der Dateiname Suffix reg; beispielsweise DisableManifestXml.reg.</span><span class="sxs-lookup"><span data-stu-id="928c7-117">Save the following text to a Windows registry file by using a filename suffix of .reg; for example, DisableManifestXml.reg.</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. <span data-ttu-id="928c7-118">Klicken Sie in Windows Explorer auf, oder doppelklicken Sie auf die REG-Datei, die Sie in den vorherigen Schritten erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="928c7-118">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
4. <span data-ttu-id="928c7-119">Klicken Sie auf **Ja,** um den Registrierungs-Editor die Änderung vornehmen zu lassen, klicken Sie im Fenster User Access Control.</span><span class="sxs-lookup"><span data-stu-id="928c7-119">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="928c7-120">Wenn Sie aufgefordert werden, um den Vorgang fortzusetzen, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="928c7-120">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="928c7-121">Den Registrierungs-Editor zeigt eine Meldung, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="928c7-121">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a><span data-ttu-id="928c7-122">Bearbeiten der Einstellungen in der Registrierung können Sie die Export-Berichte wieder aktivieren</span><span class="sxs-lookup"><span data-stu-id="928c7-122">Edit registry settings to re-enable the export reports</span></span>

<span data-ttu-id="928c7-p103">Wenn Sie die Berichte Results.csv und die Datei Manifest.xml deaktiviert haben, indem Sie die reg-Dateien in der vorherigen Prozedur erstellen, können Sie diese Dateien, um einen Bericht wieder zu aktivieren, damit sie mit den Suchergebnissen exportiert wird bearbeiten. Führen Sie das folgende Verfahren erneut aus, auf dem Computer, mit denen Sie die Ergebnisse einer Inhaltssuche exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="928c7-p103">If you disabled the Results.csv and Manifest.xml reports by creating the .reg files in the previous procedure, you can edit those files to re-enable a report so that it's exported with the search results. Again, perform the following procedure on the computer that you'll use to export the results a content search.</span></span>
  
1. <span data-ttu-id="928c7-125">Schließen Sie das Office 365 eDiscovery-Export-Tool aus, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="928c7-125">Close the Office 365 eDiscovery Export tool if it's open.</span></span>
    
2. <span data-ttu-id="928c7-126">Bearbeiten Sie eine oder beide der Bearbeiten reg-Dateien, die Sie im vorherigen Verfahren erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="928c7-126">Edit one or both of the .reg edit files that you created in the previous procedure.</span></span>
    
    - <span data-ttu-id="928c7-127">**Results.csv**</span><span class="sxs-lookup"><span data-stu-id="928c7-127">**Results.csv**</span></span>
    
        <span data-ttu-id="928c7-p104">Öffnen die Datei DisableResultsCsv.reg in Notepad ein, ändern Sie den Wert `False` , `True`, und speichern Sie die Datei. Angenommen, nachdem Sie die Datei bearbeiten, sieht es wie folgt:</span><span class="sxs-lookup"><span data-stu-id="928c7-p104">Open the DisableResultsCsv.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - <span data-ttu-id="928c7-130">**"Manifest.xml"**</span><span class="sxs-lookup"><span data-stu-id="928c7-130">**Manifest.xml**</span></span>
    
        <span data-ttu-id="928c7-p105">Öffnen die Datei DisableManifestXml.reg in Notepad ein, ändern Sie den Wert `False` , `True`, und speichern Sie die Datei. Angenommen, nachdem Sie die Datei bearbeiten, sieht es wie folgt:</span><span class="sxs-lookup"><span data-stu-id="928c7-p105">Open the DisableManifestXml.reg file in Notepad, change the value  `False` to  `True`, and then save the file. For example, after you edit the file, it looks like this:</span></span>
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. <span data-ttu-id="928c7-133">Klicken Sie in Windows Explorer auf, oder doppelklicken Sie auf eine Registrierungsdatei, die Sie im vorherigen Schritt bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="928c7-133">In Windows Explorer, click or double-click a .reg file that you edited in the previous step.</span></span>
    
4. <span data-ttu-id="928c7-134">Klicken Sie auf **Ja,** um den Registrierungs-Editor die Änderung vornehmen zu lassen, klicken Sie im Fenster User Access Control.</span><span class="sxs-lookup"><span data-stu-id="928c7-134">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="928c7-135">Wenn Sie aufgefordert werden, um den Vorgang fortzusetzen, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="928c7-135">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="928c7-136">Den Registrierungs-Editor zeigt eine Meldung, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="928c7-136">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a><span data-ttu-id="928c7-137">Häufig gestellte Fragen zum Exportieren von Berichten deaktivieren</span><span class="sxs-lookup"><span data-stu-id="928c7-137">Frequently asked questions about disabling export reports</span></span>
<span data-ttu-id="928c7-138"><a name="faqs"> </a></span><span class="sxs-lookup"><span data-stu-id="928c7-138"></span></span>

 <span data-ttu-id="928c7-139">**Was sind die Results.csv und die Datei Manifest.xml Berichte?**</span><span class="sxs-lookup"><span data-stu-id="928c7-139">**What are the Results.csv and Manifest.xml reports?**</span></span>
  
<span data-ttu-id="928c7-140">Die Results.csv und die Datei Manifest.xml-Dateien enthalten weitere Informationen über den Inhalt, der exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="928c7-140">The Results.csv and Manifest.xml files contain additional information about the content that was exported.</span></span>
  
- <span data-ttu-id="928c7-p106">**Results.csv** eine Excel-Dokument, das Informationen über jedes Element enthält, die als Suchergebnis Download ist. Für e-Mails die, das Ergebnis-Protokoll enthält Informationen zu jeder Nachricht, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="928c7-p106">**Results.csv** An Excel document that contains information about each item that is download as a search result. For email, the result log contains information about each message, including:</span></span> 
    
  - <span data-ttu-id="928c7-143">Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).</span><span class="sxs-lookup"><span data-stu-id="928c7-143">The location of the message in the source mailbox (including whether the message is in the primary or archive mailbox).</span></span>
    
  - <span data-ttu-id="928c7-144">Das Datum, an dem die Nachricht gesendet oder empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="928c7-144">The date the message was sent or received.</span></span>
    
  - <span data-ttu-id="928c7-145">Die Betreffzeile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="928c7-145">The Subject line from the message.</span></span>
    
  - <span data-ttu-id="928c7-146">Absender und Empfänger der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="928c7-146">The sender and recipients of the message.</span></span>
    
  - <span data-ttu-id="928c7-p107">Gibt an, ob die Nachricht eine doppelte Nachricht ist, wenn Sie Deduplizierung aktiviert, wenn Sie die Suchergebnisse exportieren. Doppelte Nachrichten müssen einen Wert in der Spalte **Übergeordnete ItemId** , die die Nachricht als ein Duplikat identifiziert. Der Wert in der Spalte **Übergeordnete ItemId** ist identisch mit dem Wert in der Spalte **DocumentId Element** der Nachricht, die exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="928c7-p107">Whether the message is a duplicate message if you enabled de-duplication when exporting the search results. Duplicate messages will have a value in the **Parent ItemId** column that identifies the message as a duplicate. The value in the **Parent ItemId** column is the same as the value in the **Item DocumentId** column of the message that was exported.</span></span> 
    
    <span data-ttu-id="928c7-150">Für Dokumente aus SharePoint und OneDrive for Business-Websites, das Ergebnis-Protokoll enthält Informationen zu den einzelnen Dokumenten, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="928c7-150">For documents from SharePoint and OneDrive for Business sites, the result log contains information about each document, including:</span></span>
    
  - <span data-ttu-id="928c7-151">Die URL für das Dokument.</span><span class="sxs-lookup"><span data-stu-id="928c7-151">The URL for the document.</span></span>
    
  - <span data-ttu-id="928c7-152">Die URL für die Websitesammlung, in dem das Dokument gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="928c7-152">The URL for the site collection where the document is located.</span></span>
    
  - <span data-ttu-id="928c7-153">Das Datum, das das Dokument zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="928c7-153">The date that the document was last modified.</span></span>
    
  - <span data-ttu-id="928c7-154">Der Name des Dokuments (der in der Spalte Betreff im Protokoll Ergebnis befindet).</span><span class="sxs-lookup"><span data-stu-id="928c7-154">The name of the document (which is located in the Subject column in the result log).</span></span>
    
- <span data-ttu-id="928c7-p108">**Manifest.XML** eine Manifestdatei (im XML-Format), die Informationen über jedes Element in den Suchergebnissen enthalten enthält. Die Informationen in diesem Bericht ist identisch mit dem Bericht Results.csv, aber er wird im Format angegeben durch den Verweis Modell EDRM (Electronic Discovery). Weitere Informationen zu EDRM, finden Sie unter [https://www.edrm.net](https://www.edrm.net).</span><span class="sxs-lookup"><span data-stu-id="928c7-p108">**Manifest.xml** A manifest file (in XML format) that contains information about each item included in the search results. The information in this report is the same as the Results.csv report, but it's in the format specified by the Electronic Discovery Reference Model (EDRM). For more information about EDRM, go to [https://www.edrm.net](https://www.edrm.net).</span></span>
    
 <span data-ttu-id="928c7-158">**Wann sollte ich Deaktivieren dieser Berichte exportieren?**</span><span class="sxs-lookup"><span data-stu-id="928c7-158">**When should I disable exporting these reports?**</span></span>
  
<span data-ttu-id="928c7-p109">Es hängt Ihre Bedürfnisse. Viele Organisationen müssen keine zusätzlichen Informationen zu den Suchergebnissen, und diese Berichte ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="928c7-p109">It depends on your specific needs. Many organizations don't require additional information about search results, and don't need these reports.</span></span>
  
 <span data-ttu-id="928c7-161">**Welche Computer müssen dazu auf werden?**</span><span class="sxs-lookup"><span data-stu-id="928c7-161">**What computer do I have to do this on?**</span></span>
  
 <span data-ttu-id="928c7-162">Sie müssen die Einstellung in der Registrierung auf einem lokalen Computer zu ändern, die Sie für das Office 365 eDiscovery-Export-Tool ausführen.</span><span class="sxs-lookup"><span data-stu-id="928c7-162">You have to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span> 
  
 <span data-ttu-id="928c7-163">**Nachdem ich diese Einstellung ändern, müssen ich einen Neustart des Computers?**</span><span class="sxs-lookup"><span data-stu-id="928c7-163">**After I change this setting, do I have to restart the computer?**</span></span>
  
<span data-ttu-id="928c7-p110">Nein, müssen Sie den Computer neu starten. Wenn das Office 365 eDiscovery-Export-Tool ausgeführt wird, das Ihnen jedoch zu schließen und dann neu starten, nachdem Sie die Einstellung der Registrierung ändern.</span><span class="sxs-lookup"><span data-stu-id="928c7-p110">No, you don't have to restart the computer. But if the Office 365 eDiscovery Export tool is running, you have to close it and then restart it after you change the registry setting.</span></span>
  
 <span data-ttu-id="928c7-166">**Bearbeitet ein bereits vorhandenen Registrierungsschlüssel abrufen, oder haben ein neues Schlüssels erstellt abrufen?**</span><span class="sxs-lookup"><span data-stu-id="928c7-166">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="928c7-p111">Ein neuen Registrierungsschlüssel wird beim ersten erstellt, wenn Sie die REG-Datei ausführen, die Sie in den Verfahren in diesem Thema erstellt haben. Die Einstellung wird dann jedes Mal bearbeitet, Sie ändern, und führen Sie die REG-Datei bearbeiten erneut aus.</span><span class="sxs-lookup"><span data-stu-id="928c7-p111">A new registry key is created the first time you run the .reg file that you created in the procedure in this topic. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
