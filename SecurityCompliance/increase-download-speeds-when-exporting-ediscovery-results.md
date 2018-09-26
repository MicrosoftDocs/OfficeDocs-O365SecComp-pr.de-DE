---
title: Die Download-Leistung zu steigern, beim Exportieren von eDiscovery-Suchergebnisse aus Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Informationen zum Konfigurieren der Windows-Registrierung, um den Datendurchsatz beim Herunterladen der Suchergebnisse zu erhöhen und Suchen von Daten aus der Office 365-Sicherheit &amp; Compliance Center und Office 365 erweiterte eDiscovery.
ms.openlocfilehash: a05c2b786d1d1de7ff5014d12c708484345f908b
ms.sourcegitcommit: 7956955cd919f6e00b64e4506605a743c5872549
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/26/2018
ms.locfileid: "25038118"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a><span data-ttu-id="b043a-103">Die Download-Leistung zu steigern, beim Exportieren von eDiscovery-Suchergebnisse aus Office 365</span><span class="sxs-lookup"><span data-stu-id="b043a-103">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>

<span data-ttu-id="b043a-p101">Wenn Sie das Office 365 eDiscovery-Export-Tool verwenden, um Laden Sie die Ergebnisse einer Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center oder Download von Daten aus Office 365 erweiterte eDiscovery, das Tool startet eine bestimmte Anzahl von gleichzeitigen exportieren Vorgänge, die Daten auf den lokalen Computer herunterladen. Standardmäßig ist die Anzahl der gleichzeitigen Operationen auf 8 Mal die Anzahl der Prozessorkerne auf dem Computer festgelegt, den Sie verwenden, um die Daten herunterladen. Wenn Sie einen dual-Core-Computer (d. h. zwei Prozessoren auf einem Chip) verfügen, ist die Standardanzahl zulässiger gleichzeitige Exportvorgänge beispielsweise 16. Um die Daten Übertragungsdurchsatz und beschleunigen der Downloadvorgang erhöhen möchten, können Sie die Anzahl der gleichzeitigen Operationen erhöhen, durch eine Einstellung für die Windows-Registrierung konfigurieren, auf dem Computer, mit denen Sie die Suchergebnisse herunterladen. Um den Download-Vorgang beschleunigen wird empfohlen, dass Sie mit der Einstellung der 24 gleichzeitige Vorgänge beginnen.</span><span class="sxs-lookup"><span data-stu-id="b043a-p101">When you use the Office 365 eDiscovery Export tool to download the results of a Content Search in the Office 365 Security &amp; Compliance Center or download data from Office 365 Advanced eDiscovery, the tool starts a certain number of concurrent export operations to download the data to your local computer. By default, the number of concurrent operations is set to 8 times the number of cores in the computer you're using to download the data. For example, if you have a dual core computer (meaning two central processing units on one chip), the default number of concurrent export operations is 16. To increase the data transfer throughput and speed-up the download process, you can increase the number of concurrent operations by configuring a Windows Registry setting on the computer that you use to download the search results. To speed-up the download process, we recommend that you start with a setting of 24 concurrent operations.</span></span>
  
<span data-ttu-id="b043a-p102">Wenn Sie die Suchergebnisse über ein Netzwerk mit niedriger Bandbreite herunterladen, möglicherweise Erhöhung dieser Einstellung negativ auswirken. Alternativ können Sie möglicherweise auf die Einstellung für mehr als 24 gleichzeitige Transaktionen in einem Netzwerk mit hoher Bandbreite erhöhen (die maximale Anzahl der gleichzeitigen Operationen ist 512). Nachdem Sie diese Einstellung in der Registrierung konfiguriert haben, müssen Sie möglicherweise ändern, um die optimale Anzahl gleichzeitiger Vorgänge für Ihre Umgebung zu suchen.</span><span class="sxs-lookup"><span data-stu-id="b043a-p102">If you download search results over a low-bandwidth network, increasing this setting might have a negative impact. Alternatively, you might be able to increase the setting to more than 24 concurrent operations in a high-bandwidth network (the maximum number of concurrent operations is 512). After you configure this registry setting, you might have to change it to find the optimal number of concurrent operations for your environment.</span></span>
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a><span data-ttu-id="b043a-112">Erstellen einer Einstellung so ändern Sie die Anzahl der gleichzeitigen Operationen beim Exportieren von Daten in der Registrierungs</span><span class="sxs-lookup"><span data-stu-id="b043a-112">Create a registry setting to change the number of concurrent operations when exporting data</span></span>

<span data-ttu-id="b043a-113">Führen Sie das folgende Verfahren auf dem Computer, mit denen Sie die Sicherheit der Suchergebnisse heruntergeladen werden &amp; Compliance Center oder die Daten aus der erweiterten eDiscovery.</span><span class="sxs-lookup"><span data-stu-id="b043a-113">Perform the following procedure on the computer that you'll use to download search results from the Security &amp; Compliance Center or data from Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="b043a-114">Schließen Sie das Office 365 eDiscovery-Export-Tool aus, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="b043a-114">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="b043a-115">Speichern Sie den folgenden Text zu einer Registrierungsdatei Fenster mithilfe der Dateiname Suffix reg; beispielsweise ConcurrentOperations.reg.</span><span class="sxs-lookup"><span data-stu-id="b043a-115">Save the following text to a Window registry file by using a filename suffix of .reg; for example, ConcurrentOperations.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    <span data-ttu-id="b043a-116">Wie vorherige erläutert, es wird empfohlen, dass Sie mit 24 gleichzeitige Vorgänge starten, und klicken Sie dann diese Einstellung nach Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="b043a-116">As previous explained, we recommend that you start with 24 concurrent operations, and then change this setting as appropriate.</span></span>
    
3. <span data-ttu-id="b043a-117">Klicken Sie in Windows Explorer auf, oder doppelklicken Sie auf die REG-Datei, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="b043a-117">In Windows Explorer, click or double-click the .reg file that you created in the previous step.</span></span>
    
4. <span data-ttu-id="b043a-118">Klicken Sie auf **Ja,** um den Registrierungs-Editor die Änderung vornehmen zu lassen, klicken Sie im Fenster User Access Control.</span><span class="sxs-lookup"><span data-stu-id="b043a-118">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="b043a-119">Wenn Sie aufgefordert werden, um den Vorgang fortzusetzen, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b043a-119">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="b043a-120">Den Registrierungs-Editor zeigt eine Meldung, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b043a-120">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
6. <span data-ttu-id="b043a-121">Sie können wiederholen Sie die Schritte 2 bis 5 zum Ändern des Werts für die `DownloadConcurrency` Einstellung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="b043a-121">You can repeat steps 2 - 5 to change the value for the  `DownloadConcurrency` registry setting.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="b043a-p103">Nachdem Sie erstellen oder Ändern der `DownloadConcurrency` Registrierung festlegen, müssen Sie unbedingt Erstellen eines neuen Auftrags Export oder neu starten einer vorhandenen Exportauftrag für die Suchergebnisse oder Daten, die Sie herunterladen möchten. Finden Sie [Weitere Informationen](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) im Abschnitt Weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="b043a-p103">After you create or change the  `DownloadConcurrency` registry setting, be sure to create a new export job or restart an existing export job for the search results or data that you want to download. See the [More information](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) section for more details.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="b043a-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b043a-124">More information</span></span>

- <span data-ttu-id="b043a-p104">Ein neuen Registrierungsschlüssel wird beim ersten erstellt, wenn Sie die REG-Datei ausführen, die Sie in diesem Verfahren erstellt haben. Anschließend wird die `DownloadConcurrency` registrierungseinstellung bearbeitet wird bei jedem ändern, und führen Sie die REG-Datei bearbeiten erneut aus.</span><span class="sxs-lookup"><span data-stu-id="b043a-p104">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the  `DownloadConcurrency` registry setting is edited each time you change and re-run the .reg edit file.</span></span> 
    
- <span data-ttu-id="b043a-p105">Das Office 365 eDiscovery-Export-Tool verwendet die [Azure AzCopy Dienstprogramm](https://go.microsoft.com/fwlink/?linkid=849949) zum Suchen von Daten aus der Sicherheit herunterladen &amp; Compliance Center oder von erweiterten eDiscovery. Konfigurieren der `DownloadConcurrency` registrierungseinstellung ist ähnlich wie die Verwendung **des/NC** -Parameters beim Ausführen des Dienstprogramms AzCopy. Damit die Einstellung der Registrierung des `"DownloadConcurrency=24"` müssten die gleiche Auswirkung wie die Verwendung des Werts des Parameters des `/NC:24` mit dem Dienstprogramm AzCopy.</span><span class="sxs-lookup"><span data-stu-id="b043a-p105">The Office 365 eDiscovery Export tool uses the [Azure AzCopy utility](https://go.microsoft.com/fwlink/?linkid=849949) to download search data from the Security &amp; Compliance Center or from Advanced eDiscovery. Configuring the  `DownloadConcurrency` registry setting is similar to using the **/NC** parameter when running the AzCopy utility. So the registry setting of  `"DownloadConcurrency=24"` would have the same effect as using the parameter value of  `/NC:24` with the AzCopy utility.</span></span> 
    
- <span data-ttu-id="b043a-p106">Wenn Sie einen Export Download beenden, der ist derzeit in Arbeit und starten Sie ihn neu (mit dem Versuch, die Suchergebnisse erneut laden), versucht das Office 365 eDiscovery-Export-Tool den gleichen Download fortzusetzen. Ja, wenn Sie einen Download starten, beenden, und ändern Sie die `DownloadConcurrency` Registrierung festlegen, die heruntergeladene Datei wahrscheinlich fehl, wenn Sie ihn neu starten, (durch Klicken auf **Download exportiert Ergebnisse**). Dies ist, da das Exporttool versucht, das Fortsetzen des vorherigen Downloads von Einstellungen, die nicht gültig sind, da Sie die Einstellung der Registrierung geändert haben.</span><span class="sxs-lookup"><span data-stu-id="b043a-p106">If you stop an export download that's currently in progress and then restart it (by trying to download the search results again), the Office 365 eDiscovery Export tool will attempt to resume the same download. So, if you start a download, stop it, and then change the  `DownloadConcurrency` registry setting, the download will probably fail if you restart it (by clicking **Download exported results**). This is because the export tool will attempt to resume the previous download using settings that aren't valid because you changed the registry setting.</span></span>
    
    <span data-ttu-id="b043a-p107">Aus diesem Grund nach dem Ändern der `DownloadConcurrency` Registrierung festlegen, müssen Sie unbedingt den Exportauftrag neu starten (durch Klicken auf **Export starten**) in das Wertpapier &amp; Compliance Center. Anschließend können Sie die exportierten Ergebnisse herunterladen. Weitere Informationen zum Exportieren von Suchergebnissen und Daten finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="b043a-p107">Therefore, after you change the  `DownloadConcurrency` registry setting, be sure to restart the export job (by clicking **Restart export**) in the Security &amp; Compliance Center. Then you can download the exported results. For more information about exporting search results and data, see:</span></span>
    
  - [<span data-ttu-id="b043a-136">Exportieren von Suchergebnissen aus der Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="b043a-136">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
  - [<span data-ttu-id="b043a-137">Exportieren von Ergebnissen in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="b043a-137">Export results in Office 365 Advanced eDiscovery</span></span>](export-results-in-advanced-ediscovery.md)
    
