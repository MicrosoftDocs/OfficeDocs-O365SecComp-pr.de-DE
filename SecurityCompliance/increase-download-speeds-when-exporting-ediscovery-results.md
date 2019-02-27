---
title: Höhere Downloadgeschwindigkeit beim Exportieren von eDiscovery-Suchergebnissen aus Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid: MOE150
ms.assetid: c4c8f689-9d52-4e80-ae4b-1411ee9efc43
description: Erfahren Sie, wie Sie die Windows-Registrierung konfigurieren, um den Datendurchsatz beim Herunterladen von Suchergebnissen und Such Daten &amp; aus dem Office 365 Security Compliance Center und Office 365 Advanced eDiscovery zu erhöhen.
ms.openlocfilehash: a23525ada1ef5f36bc7df4fc738c712e22243bc0
ms.sourcegitcommit: baf23be44f1ed5abbf84f140b5ffa64fce605478
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30295428"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a><span data-ttu-id="65019-103">Höhere Downloadgeschwindigkeit beim Exportieren von eDiscovery-Suchergebnissen aus Office 365</span><span class="sxs-lookup"><span data-stu-id="65019-103">Increase the download speed when exporting eDiscovery search results from Office 365</span></span>

<span data-ttu-id="65019-p101">Wenn Sie das Office 365 eDiscovery-Export Tool zum Herunterladen der Ergebnisse einer Inhaltssuche im Office 365 Security &amp; Compliance Center oder zum Herunterladen von Daten aus Office 365 Advanced eDiscovery verwenden, startet das Tool eine bestimmte Anzahl gleichzeitiger Export Vorgänge zum Herunterladen der Daten auf den lokalen Computer. Standardmäßig ist die Anzahl der gleichzeitigen Vorgänge auf die Anzahl der Kerne auf dem Computer festgelegt, den Sie zum Herunterladen der Daten verwenden. Wenn Sie beispielsweise einen Dual-Core-Computer (also zwei zentrale Verarbeitungseinheiten auf einem Chip) haben, ist die Standardanzahl gleichzeitiger Exportvorgänge 16. Um den Durchsatz bei der Datenübertragung zu erhöhen und den Downloadprozess zu beschleunigen, können Sie die Anzahl gleichzeitiger Vorgänge erhöhen, indem Sie auf dem Computer, auf dem Sie die Suchergebnisse herunterladen, eine Windows-Registrierungseinstellung konfigurieren. Um den Downloadprozess zu beschleunigen, empfehlen wir, dass Sie mit einer Einstellung von 24 gleichzeitigen Vorgängen beginnen.</span><span class="sxs-lookup"><span data-stu-id="65019-p101">When you use the Office 365 eDiscovery Export tool to download the results of a Content Search in the Office 365 Security &amp; Compliance Center or download data from Office 365 Advanced eDiscovery, the tool starts a certain number of concurrent export operations to download the data to your local computer. By default, the number of concurrent operations is set to 8 times the number of cores in the computer you're using to download the data. For example, if you have a dual core computer (meaning two central processing units on one chip), the default number of concurrent export operations is 16. To increase the data transfer throughput and speed-up the download process, you can increase the number of concurrent operations by configuring a Windows Registry setting on the computer that you use to download the search results. To speed-up the download process, we recommend that you start with a setting of 24 concurrent operations.</span></span>
  
<span data-ttu-id="65019-p102">Wenn Sie Suchergebnisse über ein Netzwerk mit niedriger Bandbreite herunterladen, kann sich die Erhöhung dieser Einstellung negativ auswirken. Alternativ können Sie die Einstellung möglicherweise auf mehr als 24 gleichzeitige Vorgänge in einem Netzwerk mit hoher Bandbreite (die maximale Anzahl gleichzeitiger Vorgänge beträgt 512). Nachdem Sie diese Registrierungseinstellung konfiguriert haben, müssen Sie Sie möglicherweise ändern, um die optimale Anzahl gleichzeitiger Vorgänge für Ihre Umgebung zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="65019-p102">If you download search results over a low-bandwidth network, increasing this setting might have a negative impact. Alternatively, you might be able to increase the setting to more than 24 concurrent operations in a high-bandwidth network (the maximum number of concurrent operations is 512). After you configure this registry setting, you might have to change it to find the optimal number of concurrent operations for your environment.</span></span>
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a><span data-ttu-id="65019-112">Erstellen einer Registrierungseinstellung zum Ändern der Anzahl gleichzeitiger Vorgänge beim Exportieren von Daten</span><span class="sxs-lookup"><span data-stu-id="65019-112">Create a registry setting to change the number of concurrent operations when exporting data</span></span>

<span data-ttu-id="65019-113">Führen Sie das folgende Verfahren auf dem Computer aus, auf dem Sie Suchergebnisse aus dem Security &amp; Compliance Center oder Daten aus Advanced eDiscovery herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="65019-113">Perform the following procedure on the computer that you'll use to download search results from the Security &amp; Compliance Center or data from Advanced eDiscovery.</span></span>
  
1. <span data-ttu-id="65019-114">Schließen Sie das Office 365 eDiscovery-Export Tool, wenn es geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="65019-114">Close the Office 365 eDiscovery Export tool if it's open.</span></span> 
    
2. <span data-ttu-id="65019-115">Speichern Sie den folgenden Text in einer Fenster Registrierungsdatei mithilfe eines Dateinamen Suffixes von. reg; Beispiel: ConcurrentOperations. reg.</span><span class="sxs-lookup"><span data-stu-id="65019-115">Save the following text to a Window registry file by using a filename suffix of .reg; for example, ConcurrentOperations.reg.</span></span> 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    <span data-ttu-id="65019-116">Wie bereits erläutert, empfiehlt es sich, mit 24 gleichzeitigen Vorgängen zu beginnen und diese Einstellung gegebenenfalls zu ändern.</span><span class="sxs-lookup"><span data-stu-id="65019-116">As previous explained, we recommend that you start with 24 concurrent operations, and then change this setting as appropriate.</span></span>
    
3. <span data-ttu-id="65019-117">Klicken oder Doppelklicken Sie in Windows Explorer auf die. reg-Datei, die Sie im vorherigen Schritt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="65019-117">In Windows Explorer, click or double-click the .reg file that you created in the previous step.</span></span>
    
4. <span data-ttu-id="65019-118">Klicken Sie im Fenster Benutzerzugriffssteuerung auf **Ja** , um die Änderung des Registrierungs-Editors zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="65019-118">In the User Access Control window, click **Yes** to let the Registry Editor make the change.</span></span> 
    
5. <span data-ttu-id="65019-119">Wenn Sie zum Fortfahren aufgefordert werden, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="65019-119">When prompted to continue, click **Yes**.</span></span>
    
    <span data-ttu-id="65019-120">Der Registrierungs-Editor zeigt eine Meldung an, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="65019-120">The Registry Editor displays a message saying that the setting was successfully added to the registry.</span></span>
    
6. <span data-ttu-id="65019-121">Sie können die Schritte 2-5 wiederholen, um den Wert `DownloadConcurrency` für die Registrierungseinstellung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="65019-121">You can repeat steps 2 - 5 to change the value for the  `DownloadConcurrency` registry setting.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="65019-p103">Nachdem Sie die `DownloadConcurrency` Registrierungseinstellung erstellt oder geändert haben, müssen Sie einen neuen Exportauftrag erstellen oder einen vorhandenen Exportauftrag für die Suchergebnisse oder Daten, die Sie herunterladen möchten, neu starten. Weitere Informationen finden Sie im Abschnitt [More Information](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) .</span><span class="sxs-lookup"><span data-stu-id="65019-p103">After you create or change the  `DownloadConcurrency` registry setting, be sure to create a new export job or restart an existing export job for the search results or data that you want to download. See the [More information](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) section for more details.</span></span> 
  
## <a name="more-information"></a><span data-ttu-id="65019-124">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="65019-124">More information</span></span>

- <span data-ttu-id="65019-p104">Bei der ersten Ausführung der reg-Datei, die Sie in diesem Verfahren erstellt haben, wird ein neuer Registrierungsschlüssel erstellt. Dann wird `DownloadConcurrency` die Registrierungseinstellung jedes Mal bearbeitet, wenn Sie die reg-Bearbeitungs Datei ändern und erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="65019-p104">A new registry key is created the first time you run the .reg file that you created in this procedure. Then the  `DownloadConcurrency` registry setting is edited each time you change and re-run the .reg edit file.</span></span> 
    
- <span data-ttu-id="65019-p105">Das Office 365 eDiscovery-Export Tool verwendet das [Azure AzCopy-Dienstprogramm](https://go.microsoft.com/fwlink/?linkid=849949) zum Herunterladen von &amp; Such Daten aus dem Security Compliance Center oder von Advanced eDiscovery. Das konfigurieren `DownloadConcurrency` der Registrierungseinstellung ähnelt der Verwendung des **/NC** -Parameters beim Starten des AzCopy-Dienstprogramms. Daher hätte die Registrierungseinstellung `"DownloadConcurrency=24"` von den gleichen Effekt wie die Verwendung des Parameterwerts von `/NC:24` mit dem AzCopy-Dienstprogramm.</span><span class="sxs-lookup"><span data-stu-id="65019-p105">The Office 365 eDiscovery Export tool uses the [Azure AzCopy utility](https://go.microsoft.com/fwlink/?linkid=849949) to download search data from the Security &amp; Compliance Center or from Advanced eDiscovery. Configuring the  `DownloadConcurrency` registry setting is similar to using the **/NC** parameter when running the AzCopy utility. So the registry setting of  `"DownloadConcurrency=24"` would have the same effect as using the parameter value of  `/NC:24` with the AzCopy utility.</span></span> 
    
- <span data-ttu-id="65019-p106">Wenn Sie einen Export Download beenden, der derzeit ausgeführt wird, und diesen dann erneut starten (indem Sie versuchen, die Suchergebnisse erneut herunterzuladen), versucht das Office 365 eDiscovery-Export Tool, den gleichen Download wieder aufzunehmen. Wenn Sie also einen Download starten, ihn beenden und dann die `DownloadConcurrency` Registrierungseinstellung ändern, wird der Download wahrscheinlich fehlschlagen, wenn Sie ihn neu starten (indem Sie auf exportierte **Ergebnisse herunterladen**klicken). Dies liegt daran, dass das Export Tool versucht, den vorherigen Download mithilfe von Einstellungen fortzusetzen, die nicht gültig sind, da Sie die Registrierungseinstellung geändert haben.</span><span class="sxs-lookup"><span data-stu-id="65019-p106">If you stop an export download that's currently in progress and then restart it (by trying to download the search results again), the Office 365 eDiscovery Export tool will attempt to resume the same download. So, if you start a download, stop it, and then change the  `DownloadConcurrency` registry setting, the download will probably fail if you restart it (by clicking **Download exported results**). This is because the export tool will attempt to resume the previous download using settings that aren't valid because you changed the registry setting.</span></span>
    
    <span data-ttu-id="65019-p107">Nachdem Sie die `DownloadConcurrency` Registrierungseinstellung geändert haben, müssen Sie daher den Exportauftrag (durch Klicken auf **Neustart exportieren**) im Security &amp; Compliance Center neu starten. Dann können Sie die exportierten Ergebnisse herunterladen. Weitere Informationen zum Exportieren von Suchergebnissen und Daten finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="65019-p107">Therefore, after you change the  `DownloadConcurrency` registry setting, be sure to restart the export job (by clicking **Restart export**) in the Security &amp; Compliance Center. Then you can download the exported results. For more information about exporting search results and data, see:</span></span>
    
  - [<span data-ttu-id="65019-136">Exportieren von Inhalts Suchergebnissen aus dem Office 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="65019-136">Export Content Search results from the Office 365 Security &amp; Compliance Center</span></span>](export-search-results.md)
    
  - [<span data-ttu-id="65019-137">Exportieren von Ergebnissen in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="65019-137">Export results in Office 365 Advanced eDiscovery</span></span>](export-results-in-advanced-ediscovery.md)
    
