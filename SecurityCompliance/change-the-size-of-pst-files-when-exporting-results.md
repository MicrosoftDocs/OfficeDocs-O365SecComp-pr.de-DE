---
title: Ändern der Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnissen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Sie können die Standardgröße von PST-Dateien ändern, die beim Exportieren von eDiscovery-Suchergebnissen auf Ihren Computer heruntergeladen werden.
ms.openlocfilehash: 8a956091f29ec1b564d3194c7e3ca2680fdeb564
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214625"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a><span data-ttu-id="c84d8-103">Ändern der Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnissen</span><span class="sxs-lookup"><span data-stu-id="c84d8-103">Change the size of PST files when exporting eDiscovery search results</span></span>

<span data-ttu-id="c84d8-p101">Wenn Sie das Office 365 eDiscovery-Export Tool verwenden, um die e-Mail-Ergebnisse einer eDiscovery-Suche aus den verschiedenen Microsoft eDiscovery-Tools zu exportieren, beträgt die Standardgröße einer PST-Datei, die exportiert werden kann, 10 GB. Wenn Sie diese Standardgröße ändern möchten, können Sie die Windows-Registrierung auf dem Computer bearbeiten, den Sie zum Exportieren der Suchergebnisse verwenden. Ein Grund hierfür ist, dass eine PST-Datei auf Wechseldatenträger, eine DVD, eine CD oder ein USB-Laufwerk angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="c84d8-p101">When you use the Office 365 eDiscovery Export tool to export the email results of an eDiscovery search from the different Microsoft eDiscovery tools, the default size of a PST file that can be exported is 10 GB. If you want to change this default size, you can edit the Windows Registry on the computer that you use to export the search results. One reason to do this is so a PST file can fit on removable media, such a DVD, a compact disc, or a USB drive.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="c84d8-107">Das Office 365 eDiscovery-Export Tool wird verwendet, um die Suchergebnisse zu exportieren, wenn Sie die Inhaltssuche &amp; im Office 365 Security Compliance Center, in-Place eDiscovery in Exchange Online und im eDiscovery Center in SharePoint Online verwenden.</span><span class="sxs-lookup"><span data-stu-id="c84d8-107">The Office 365 eDiscovery Export tool is used to export the search results when using Content Search in the Office 365 Security &amp; Compliance Center, In-Place eDiscovery in Exchange Online, and the eDiscovery Center in SharePoint Online.</span></span> 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="c84d8-108">Erstellen einer Registrierungseinstellung zum Ändern der Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnissen</span><span class="sxs-lookup"><span data-stu-id="c84d8-108">Create a registry setting to change the size of PST files when you export eDiscovery search results</span></span>

<span data-ttu-id="c84d8-109">Führen Sie auf dem Computer, auf dem Sie die Ergebnisse einer eDiscovery-Suche exportieren möchten, das folgende Verfahren aus.</span><span class="sxs-lookup"><span data-stu-id="c84d8-109">Perform the following procedure on the computer that you'll use to export the results of an eDiscovery search.</span></span>
  
1. <span data-ttu-id="c84d8-110">Schließen Sie das Office 365 eDiscovery-Export Tool, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="c84d8-110">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="c84d8-111">Speichern Sie den folgenden Text in einer Fenster Registrierungsdatei mithilfe eines Dateinamen Suffixes von. reg; Beispiel: PstExportSize. reg.</span><span class="sxs-lookup"><span data-stu-id="c84d8-111">Save the following text to a Window registry file by using a filename suffix of .reg; for example, PstExportSize.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    <span data-ttu-id="c84d8-p102">Im obigen Beispiel ist der `PstSizeLimitInBytes` wert auf 1.073.741.824 Byte oder ungefähr 1 GB festgelegt. Im folgenden finden Sie einige andere Beispielwerte `PstSizeLimitInBytes` für die Einstellung.</span><span class="sxs-lookup"><span data-stu-id="c84d8-p102">In the example above, the  `PstSizeLimitInBytes` value is set to 1,073,741,824 bytes or approximately 1 GB. Here are some other sample values for the  `PstSizeLimitInBytes` setting.</span></span> 
    
    |<span data-ttu-id="c84d8-114">**Größe in GB (ca.)**</span><span class="sxs-lookup"><span data-stu-id="c84d8-114">**Size in GB (approx.)**</span></span>|<span data-ttu-id="c84d8-115">**Größe in Byte**</span><span class="sxs-lookup"><span data-stu-id="c84d8-115">**Size in bytes**</span></span>|
    |:-----|:-----|
    |<span data-ttu-id="c84d8-116">.7 GB (700 MB)</span><span class="sxs-lookup"><span data-stu-id="c84d8-116">.7 GB (700 MB)</span></span>  <br/> |<span data-ttu-id="c84d8-117">751619277</span><span class="sxs-lookup"><span data-stu-id="c84d8-117">751619277</span></span>  <br/> |
    |<span data-ttu-id="c84d8-118">2 GB</span><span class="sxs-lookup"><span data-stu-id="c84d8-118">2 GB</span></span>  <br/> |<span data-ttu-id="c84d8-119">2147483648</span><span class="sxs-lookup"><span data-stu-id="c84d8-119">2147483648</span></span>  <br/> |
    |<span data-ttu-id="c84d8-120">4 GB</span><span class="sxs-lookup"><span data-stu-id="c84d8-120">4 GB</span></span>  <br/> |<span data-ttu-id="c84d8-121">4294967296</span><span class="sxs-lookup"><span data-stu-id="c84d8-121">4294967296</span></span>  <br/> |
    |<span data-ttu-id="c84d8-122">8 GB</span><span class="sxs-lookup"><span data-stu-id="c84d8-122">8 GB</span></span>  <br/> |<span data-ttu-id="c84d8-123">8589934592</span><span class="sxs-lookup"><span data-stu-id="c84d8-123">8589934592</span></span>  <br/> |
   
3. <span data-ttu-id="c84d8-124">Ändern Sie `PstSizeLimitInBytes` den Wert in die gewünschte maximale Größe einer PST-Datei, wenn Sie die Suchergebnisse exportieren, und speichern Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="c84d8-124">Change the `PstSizeLimitInBytes` value to the desired maximum size of a PST file when you export search results, and then save the file.</span></span> 
    
4. <span data-ttu-id="c84d8-125">Klicken oder Doppelklicken Sie in Windows Explorer auf die. reg-Datei, die Sie in den vorherigen Schritten erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c84d8-125">In Windows Explorer, click or double-click the .reg file that you created in the previous steps.</span></span>
    
5. <span data-ttu-id="c84d8-126">Klicken Sie im Fenster Benutzerzugriffssteuerung auf **Ja** , um die Änderung des Registrierungs-Editors zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c84d8-126">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
6. <span data-ttu-id="c84d8-127">Wenn Sie zum Fortfahren aufgefordert werden, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c84d8-127">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="c84d8-128">Der Registrierungs-Editor zeigt eine Meldung an, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c84d8-128">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
7. <span data-ttu-id="c84d8-129">Sie können die Schritte 3-6 wiederholen, um den Wert `PstSizeLimitInBytes` für die Registrierungseinstellung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c84d8-129">You can repeat steps 3 - 6 to change the value for the  `PstSizeLimitInBytes` registry setting.</span></span> 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a><span data-ttu-id="c84d8-130">Häufig gestellte Fragen zum Ändern der Standardgröße von PST-Dateien beim Exportieren von eDiscovery-Suchergebnissen</span><span class="sxs-lookup"><span data-stu-id="c84d8-130">Frequently asked questions about changing the default size of PST files when you export eDiscovery search results</span></span>

 <span data-ttu-id="c84d8-131">**Warum ist die Standardgröße 10 GB?**</span><span class="sxs-lookup"><span data-stu-id="c84d8-131">**Why is the default size 10 GB?**</span></span>
  
<span data-ttu-id="c84d8-132">Die Standardgröße von 10 GB basierte auf Kundenfeedback; 10 GB stellt eine gute Balance zwischen der optimalen Menge an Inhalten in einer einzelnen PST-Datei und einer minimalen Wahrscheinlichkeit für eine Beschädigung von Dateien dar.</span><span class="sxs-lookup"><span data-stu-id="c84d8-132">The default size of 10 GB was based on customer feedback; 10 GB is a good balance between the optimal amount of content in a single PST and with a minimum chance of file corruption.</span></span>
  
 <span data-ttu-id="c84d8-133">**Sollte ich die Standardgröße von PST-Dateien vergrößern oder verkleinern?**</span><span class="sxs-lookup"><span data-stu-id="c84d8-133">**Should I increase or decrease the default size of PST files?**</span></span>
  
<span data-ttu-id="c84d8-p103">Kunden neigen dazu, die Größenbeschränkung zu verringern, sodass die Suchergebnisse auf Wechseldatenträger angepasst werden, die Sie physisch an andere Standorte in Ihrer Organisation senden können. Es wird nicht empfohlen, dass Sie die Standardgröße vergrößern, da PST-Dateien, die größer als 10 GB sind, möglicherweise beschädigte Probleme aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c84d8-p103">Customers tend to decrease the size limit so that the search results will fit on removable media that they can physically ship other locations in their organization. We don't recommend that you increase the default size because PST files larger than 10 GB might have corruption issues.</span></span>
  
 <span data-ttu-id="c84d8-136">**Auf welchem Computer muss ich vorgehen?**</span><span class="sxs-lookup"><span data-stu-id="c84d8-136">**What computer do I have to do this on?**</span></span>
  
<span data-ttu-id="c84d8-137">Sie müssen die Registrierungseinstellung auf jedem lokalen Computer ändern, auf dem Sie das Office 365 eDiscovery-Export Tool ausführen.</span><span class="sxs-lookup"><span data-stu-id="c84d8-137">You need to change the registry setting on any local computer that you run the Office 365 eDiscovery Export tool on.</span></span>
  
 <span data-ttu-id="c84d8-138">**Muss ich den Computer neu starten, nachdem ich diese Einstellung geändert habe?**</span><span class="sxs-lookup"><span data-stu-id="c84d8-138">**After I change this setting, do I have to reboot the computer?**</span></span>
  
<span data-ttu-id="c84d8-p104">Nein, Sie müssen den Computer nicht neu starten. Wenn jedoch das Office 365 eDiscovery-Export Tool läuft, müssen Sie es beenden und es nach dem Ändern dieser Einstellung neu starten.</span><span class="sxs-lookup"><span data-stu-id="c84d8-p104">No, you don't have to reboot the computer. But, if the Office 365 eDiscovery Export tool is running, you'll have to close it and the restart it after you change this setting.</span></span>
  
 <span data-ttu-id="c84d8-141">**Wird ein vorhandener Registrierungsschlüssel bearbeitet oder wird ein neuer Schlüssel erstellt?**</span><span class="sxs-lookup"><span data-stu-id="c84d8-141">**Does an existing registry key get edited or does a new key get created?**</span></span>
  
<span data-ttu-id="c84d8-p105">Bei der ersten Ausführung der reg-Datei, die Sie in diesem Verfahren erstellt haben, wird ein neuer Registrierungsschlüssel erstellt. Dann wird die Einstellung jedes Mal bearbeitet, wenn Sie die reg-Bearbeitungs Datei ändern und erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="c84d8-p105">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the setting is edited each time you change and re-run the .reg edit file.</span></span>
