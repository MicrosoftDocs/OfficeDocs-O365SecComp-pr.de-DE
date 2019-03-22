---
title: Problembehandlung bei AzCopy in Advanced eDiscovery (Preview)
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: o365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 9711bee4ec9a61510b47568df37dfd3135e1e00c
ms.sourcegitcommit: cf9d9b545a7c153d314aa9c08c7fb16fcd785b3e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30742503"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery-preview"></a><span data-ttu-id="6fb1f-102">Problembehandlung bei AzCopy in Advanced eDiscovery (Preview)</span><span class="sxs-lookup"><span data-stu-id="6fb1f-102">Troubleshoot AzCopy in Advanced eDiscovery (Preview)</span></span>

<span data-ttu-id="6fb1f-103">Beim Laden von nicht-Office 365-Daten oder-Dokumenten zur Fehlerkorrektur in Advanced eDiscovery (Preview) stellt die Benutzeroberfläche einen Azure-AzCopy-Befehl bereit, der Parameter mit dem Speicherort enthält, an dem die Dateien, die Sie hochladen möchten, gespeichert sind und die Azure Speicherort, in den die Dateien hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-103">When loading non-Office 365 data or documents for error remediation in Advanced eDiscovery (Preview), the user interface supplies an Azure AzCopy command that contains parameters with the location of where the files that you want to upload are stored and the Azure storage location that the files will be uploaded to.</span></span> <span data-ttu-id="6fb1f-104">Um Ihre Dokumente hochzuladen, kopieren Sie diesen Befehl, und führen Sie ihn dann an einer EingabeaufForderungen auf Ihrem lokalen Computer aus.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-104">To upload your documents, you copy this command and then run it in a Command Prompt on your local computer.</span></span>  <span data-ttu-id="6fb1f-105">Der folgende Screenshot zeigt ein Beispiel für einen AzCopy-Befehl:</span><span class="sxs-lookup"><span data-stu-id="6fb1f-105">The follow screenshot shows an example of an AzCopy command:</span></span>

![Hochladen nicht-Office 365-Dateien](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

<span data-ttu-id="6fb1f-107">In den meisten Fällen funktioniert der Befehl, der bereitgestellt wird, wenn Sie ihn ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-107">In most cases, the command that's provided will work when you run it.</span></span> <span data-ttu-id="6fb1f-108">Es kann jedoch vorkommen, dass der angezeigte Befehl nicht erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-108">However, there may be cases when the command that's displayed will not run successfully.</span></span> <span data-ttu-id="6fb1f-109">Hier einige mögliche Gründe.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-109">Here's a few possible reasons.</span></span>

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a><span data-ttu-id="6fb1f-110">AzCopy wird nicht auf dem lokalen Computer installiert, oder es ist nicht am Standardspeicherort installiert</span><span class="sxs-lookup"><span data-stu-id="6fb1f-110">AzCopy isn't installed on the local computer or it's not installed in the default location</span></span>

<span data-ttu-id="6fb1f-111">Wenn AzCopy nicht installiert ist oder an einem anderen Speicherort als dem Standard Installationsspeicherort installiert ist, wird `%ProgramFiles(x86)%`möglicherweise die folgende Fehlermeldung angezeigt, wenn Sie den AzCopy-Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="6fb1f-111">If AzCopy isn't installed or it's installed in a location other than the default install location (which is `%ProgramFiles(x86)%`), you may receive the following error when you run the AzCopy command:</span></span>

    The system cannot find the path specified.

<span data-ttu-id="6fb1f-112">Wenn AzCopy nicht auf dem lokalen Computer installiert werden kann, können Sie von hier aus installieren (Sie müssen es unbedingt am Standardspeicherort installieren [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy)):.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-112">If AzCopy isn't install on the local computer, you can install from here (being sure to install it in the default location): [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy).</span></span>


<span data-ttu-id="6fb1f-113">Wenn AzCopy installiert ist, aber an einem anderen Speicherort als dem Standardspeicherort installiert ist, können Sie den Befehl Kopieren, ihn in eine Textdatei einfügen und dann den Pfad zu dem Speicherort ändern, an dem AzCopy tatsächlich installiert ist.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-113">If AzCopy is installed, but it's installed in a location different than the default location, you can copy the command, paste it to a text file, and then change the path to the location where AzCopy is actually installed.</span></span> <span data-ttu-id="6fb1f-114">Wenn sich beispielsweise Azcopy in `%ProgramFiles%`befindet, können Sie den ersten Teil des Befehls von `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` in ändern. `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`</span><span class="sxs-lookup"><span data-stu-id="6fb1f-114">For example, if Azcopy is located in `%ProgramFiles%`, then you can change the first part of the command from `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` to `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`.</span></span> <span data-ttu-id="6fb1f-115">Nachdem Sie diese Änderung vorgenommen haben, kopieren Sie Sie aus der Textdatei, und führen Sie Sie an einer EingabeaufForderungen aus.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-115">After you make this change, copy it from the text file and then run it a Command Prompt.</span></span>

> [!TIP]
> <span data-ttu-id="6fb1f-116">Wenn AzCopy an einem anderen Speicherort als dem Standard Installationsspeicherort installiert ist, sollten Sie ihn deinstallieren und dann erneut am Standardspeicherort installieren.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-116">If AzCopy is installed in a location other then the default install location, consider uninstalling it and then re-installing it in the default location.</span></span> <span data-ttu-id="6fb1f-117">Dadurch wird dieses Problem künftig verhindert.</span><span class="sxs-lookup"><span data-stu-id="6fb1f-117">This will help prevent this issue in the future.</span></span>