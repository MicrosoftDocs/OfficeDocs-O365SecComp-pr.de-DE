---
title: Ändern Sie die Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Sie können die Standardgröße von PST-Dateien ändern, die beim Exportieren von eDiscovery-Suchergebnisse auf den Computer heruntergeladen werden.
ms.openlocfilehash: c01f05a02fd94941eb2eb7a05b4c84ffecec9b39
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522246"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a><span data-ttu-id="28d65-103">Ändern Sie die Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="28d65-103">Change the size of PST files when exporting eDiscovery search results</span></span>

<span data-ttu-id="28d65-p101">Wenn Sie das Office 365 eDiscovery-Export-Tool verwenden, um die e-Mail-Ergebnisse einer eDiscovery-Suche aus der verschiedenen Microsoft eDiscovery-Tools zu exportieren, wird die Standardgröße des eine PST-Datei, die exportiert werden kann 10 GB. Wenn Sie diese Standardgröße ändern möchten, können Sie die Windows-Registrierung auf dem Computer bearbeiten, mit denen Sie die Suchergebnisse exportieren. Ein Grund hierfür ist, sodass eine PST-Datei auf das Wechselmedium, solche einer DVD, einer CD oder ein USB-Laufwerk passen.</span><span class="sxs-lookup"><span data-stu-id="28d65-p101">When you use the Office 365 eDiscovery Export tool to export the email results of an eDiscovery search from the different Microsoft eDiscovery tools, the default size of a PST file that can be exported is 10 GB. If you want to change this default size, you can edit the Windows Registry on the computer that you use to export the search results. One reason to do this is so a PST file can fit on removable media, such a DVD, a compact disc, or a USB drive.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="28d65-107">Das Office 365 eDiscovery-Export-Tool wird verwendet, um die Suchergebnisse zu exportieren, bei der Verwendung von Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center, Compliance-eDiscovery in Exchange Online und das eDiscovery Center in SharePoint Online.</span><span class="sxs-lookup"><span data-stu-id="28d65-107">The Office 365 eDiscovery Export tool is used to export the search results when using Content Search in the Office 365 Security &amp; Compliance Center, In-Place eDiscovery in Exchange Online, and the eDiscovery Center in SharePoint Online.</span></span> 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="28d65-108">Erstellen Sie einen Registrierungseintrag so ändern Sie die Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="28d65-108">Create a registry setting to change the size of PST files when you export eDiscovery search results</span></span>

<span data-ttu-id="28d65-109">Führen Sie das folgende Verfahren auf dem Computer, mit denen Sie die Ergebnisse einer eDiscovery-Suche exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="28d65-109">Perform the following procedure on the computer that you'll use to export the results of an eDiscovery search.</span></span>
  
1. <span data-ttu-id="28d65-110">Schließen Sie das Office 365 eDiscovery-Export-Tool aus, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="28d65-110">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="28d65-111">Speichern Sie den folgenden Text zu einer Registrierungsdatei Fenster mithilfe der Dateiname Suffix reg; beispielsweise PstExportSize.reg.</span><span class="sxs-lookup"><span data-stu-id="28d65-111">Save the following text to a Window registry file by using a filename suffix of .reg; for example, PstExportSize.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    <span data-ttu-id="28d65-p102">Im obigen Beispiel die `PstSizeLimitInBytes` Wert auf 1.073.741.824 Bytes oder ungefähr 1 GB festgelegt ist. Hier sind einige andere Beispielwerte für die `PstSizeLimitInBytes` Einstellung.</span><span class="sxs-lookup"><span data-stu-id="28d65-p102">In the example above, the  `PstSizeLimitInBytes` value is set to 1,073,741,824 bytes or approximately 1 GB. Here are some other sample values for the  `PstSizeLimitInBytes` setting.</span></span> 
    
    |<span data-ttu-id="28d65-114">**Größe in GB (etwa)**</span><span class="sxs-lookup"><span data-stu-id="28d65-114">**Size in GB (approx.)**</span></span>|<span data-ttu-id="28d65-115">**Größe in bytes**</span><span class="sxs-lookup"><span data-stu-id="28d65-115">**Size in bytes**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="28d65-116">.7 GB (700 MB)</span><span class="sxs-lookup"><span data-stu-id="28d65-116">.7 GB (700 MB)</span></span>  <br/> |<span data-ttu-id="28d65-117">751619277</span><span class="sxs-lookup"><span data-stu-id="28d65-117">751619277</span></span>  <br/> |
    |<span data-ttu-id="28d65-118">2 GB</span><span class="sxs-lookup"><span data-stu-id="28d65-118">2 GB</span></span>  <br/> |<span data-ttu-id="28d65-119">2147483648</span><span class="sxs-lookup"><span data-stu-id="28d65-119">2147483648</span></span>  <br/> |
    |<span data-ttu-id="28d65-120">4 GB</span><span class="sxs-lookup"><span data-stu-id="28d65-120">4 GB</span></span>  <br/> |<span data-ttu-id="28d65-121">4294967296</span><span class="sxs-lookup"><span data-stu-id="28d65-121">4294967296</span></span>  <br/> |
    |<span data-ttu-id="28d65-122">8 GB</span><span class="sxs-lookup"><span data-stu-id="28d65-122">8 GB</span></span>  <br/> |<span data-ttu-id="28d65-123">8589934592</span><span class="sxs-lookup"><span data-stu-id="28d65-123">8589934592</span></span>  <br/> |
   
3. <span data-ttu-id="28d65-124">Ändern der `PstSizeLimitInBytes` Wert auf die gewünschte maximale Größe einer PST-Datei bei der Suchergebnisse exportieren und speichern Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="28d65-124">Change the `PstSizeLimitInBytes` value to the desired maximum size of a PST file when you export search results, and then save the file.</span></span> 
    
4. <span data-ttu-id="28d65-125">Klicken Sie in Windows Explorer auf, oder doppelklicken Sie auf die REG-Datei, die Sie in den vorherigen Schritten erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="28d65-125">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
5. <span data-ttu-id="28d65-126">Klicken Sie auf **Ja,** um den Registrierungs-Editor die Änderung vornehmen zu lassen, klicken Sie im Fenster User Access Control.</span><span class="sxs-lookup"><span data-stu-id="28d65-126">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
6. <span data-ttu-id="28d65-127">Wenn Sie aufgefordert werden, um den Vorgang fortzusetzen, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="28d65-127">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="28d65-128">Den Registrierungs-Editor zeigt eine Meldung, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="28d65-128">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
7. <span data-ttu-id="28d65-129">Sie können wiederholen Sie die Schritte 3 bis 6 zum Ändern des Werts für die `PstSizeLimitInBytes` Einstellung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="28d65-129">You can repeat steps 3 - 6 to change the value for the  `PstSizeLimitInBytes` registry setting.</span></span> 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="28d65-130">Häufig gestellte Fragen zum Ändern der Standardgröße von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="28d65-130">Frequently asked questions about changing the default size of PST files when you export eDiscovery search results</span></span>

 <span data-ttu-id="28d65-131">**Warum ist der Standardwert 10 GB Größe?**</span><span class="sxs-lookup"><span data-stu-id="28d65-131">**Why is the default size 10 GB?**</span></span>
  
<span data-ttu-id="28d65-132">Die Standardgröße von 10 GB wurde basierend auf Feedback von Kunden; 10 GB lautet ein guter Kompromiss zwischen den optimalen Umfang des Inhalts in einer einzelnen PST-Datei und eine minimale Möglichkeit der Beschädigung der Datei.</span><span class="sxs-lookup"><span data-stu-id="28d65-132">The default size of 10 GB was based on customer feedback; 10 GB is a good balance between the optimal amount of content in a single PST and with a minimum chance of file corruption.</span></span>
  
 <span data-ttu-id="28d65-133">**Ich habe erhöhen oder verringern Sie die Standardgröße von PST-Dateien?**</span><span class="sxs-lookup"><span data-stu-id="28d65-133">**Should I increase or decrease the default size of PST files?**</span></span>
  
<span data-ttu-id="28d65-p103">Kunden in der Regel die maximale Größe reduzieren, sodass die Suchergebnisse auf Wechselmedium passt, dass sie andere Standorte in ihrer Organisation physisch versenden können. Es wird nicht empfohlen, dass Sie die Standardgröße erhöhen, da PST-größer Dateien als 10 GB Beschädigung Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="28d65-p103">Customers tend to decrease the size limit so that the search results will fit on removable media that they can physically ship other locations in their organization. We don't recommend that you increase the default size because PST files larger than 10 GB might have corruption issues.</span></span>
  
 <span data-ttu-id="28d65-136">**Welche Computer müssen dazu auf werden?**</span><span class="sxs-lookup"><span data-stu-id="28d65-136">**What computer do I have to do this on?**</span></span>
  
<span data-ttu-id="28d65-137">Sie müssen die Einstellung in der Registrierung auf einem lokalen Computer zu ändern, die Sie für das Office 365 eDiscovery-Export-Tool ausführen.</span><span class="sxs-lookup"><span data-stu-id="28d65-137">You need to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span>
  
 <span data-ttu-id="28d65-138">**Nachdem ich diese Einstellung ändern, müssen ich den Computer neu starten?**</span><span class="sxs-lookup"><span data-stu-id="28d65-138">**After I change this setting, do I have to reboot the computer?**</span></span>
  
<span data-ttu-id="28d65-p104">Nein, müssen Sie den Computer neu starten. Jedoch nicht, wenn das Office 365 eDiscovery-Export-Tool ausgeführt wird, müssen Sie es und dem Neustart zu schließen, nachdem Sie diese Einstellung ändern.</span><span class="sxs-lookup"><span data-stu-id="28d65-p104">No, you don't have to reboot the computer. But, if the Office 365 eDiscovery Export tool is running, you'll have to close it and the restart it after you change this setting.</span></span>
  
 <span data-ttu-id="28d65-141">**Bearbeitet ein bereits vorhandenen Registrierungsschlüssel abrufen, oder haben ein neues Schlüssels erstellt abrufen?**</span><span class="sxs-lookup"><span data-stu-id="28d65-141">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="28d65-p105">Ein neuen Registrierungsschlüssel wird beim ersten erstellt, wenn Sie die REG-Datei ausführen, die Sie in diesem Verfahren erstellt haben. Die Einstellung wird dann jedes Mal bearbeitet, Sie ändern, und führen Sie die REG-Datei bearbeiten erneut aus.</span><span class="sxs-lookup"><span data-stu-id="28d65-p105">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
