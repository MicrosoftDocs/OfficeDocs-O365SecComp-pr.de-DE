---
title: Problembehandlung bei AzCopy in Advanced eDiscovery
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: o365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: eb8c84d696a05f86246a512f1867d8efc98881a0
ms.sourcegitcommit: 73dcdafb15b462223d1a670c781db260eb73c2f5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "36048091"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery"></a><span data-ttu-id="d5198-102">Problembehandlung bei AzCopy in Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="d5198-102">Troubleshoot AzCopy in Advanced eDiscovery</span></span>

<span data-ttu-id="d5198-103">Beim Laden von nicht Office 365 Daten oder Dokumenten zur Fehlerbehebung in Advanced eDiscovery stellt die Benutzeroberfläche einen Azure AzCopy-Befehl bereit, der Parameter mit dem Speicherort enthält, an dem die Dateien, die Sie hochladen möchten, gespeichert werden und der Azure-Speicher Speicherort, in den die Dateien hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="d5198-103">When loading non-Office 365 data or documents for error remediation in Advanced eDiscovery, the user interface supplies an Azure AzCopy command that contains parameters with the location of where the files that you want to upload are stored and the Azure storage location that the files will be uploaded to.</span></span> <span data-ttu-id="d5198-104">Zum Hochladen Ihrer Dokumente kopieren Sie diesen Befehl und führen ihn dann an einer Eingabeaufforderung auf dem lokalen Computer aus.</span><span class="sxs-lookup"><span data-stu-id="d5198-104">To upload your documents, you copy this command and then run it in a Command Prompt on your local computer.</span></span>  <span data-ttu-id="d5198-105">Das folgende Screenshot zeigt ein Beispiel für einen AzCopy-Befehl:</span><span class="sxs-lookup"><span data-stu-id="d5198-105">The follow screenshot shows an example of an AzCopy command:</span></span>

![Hochladen nicht Office 365er Dateien](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

<span data-ttu-id="d5198-107">Normalerweise funktioniert der Befehl, der bereitgestellt wird, wenn Sie ihn ausführen.</span><span class="sxs-lookup"><span data-stu-id="d5198-107">Usually the command that's provided works when you run it.</span></span> <span data-ttu-id="d5198-108">Es kann jedoch vorkommen, dass der angezeigte Befehl nicht erfolgreich ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d5198-108">However, there may be cases when the command that's displayed will not run successfully.</span></span> <span data-ttu-id="d5198-109">Es folgen einige mögliche Gründe.</span><span class="sxs-lookup"><span data-stu-id="d5198-109">Here's a few possible reasons.</span></span>

## <a name="the-supported-version-of-azcopy-isnt-installed-on-the-local-computer"></a><span data-ttu-id="d5198-110">Die unterstützte Version von AzCopy ist nicht auf dem lokalen Computer installiert.</span><span class="sxs-lookup"><span data-stu-id="d5198-110">The supported version of AzCopy isn't installed on the local computer</span></span>

<span data-ttu-id="d5198-111">Zu diesem Zeitpunkt müssen Sie AzCopy v 8.1 verwenden, um nicht Office 365 Daten in Advanced eDiscovery zu laden.</span><span class="sxs-lookup"><span data-stu-id="d5198-111">At this time, you must use AzCopy v8.1 to load non-Office 365 data in Advanced eDiscovery.</span></span> <span data-ttu-id="d5198-112">Der AzCopy-Befehl, der auf der im vorherigen Screenshot angezeigten Seite **Dateien hochladen** angezeigt wird, gibt einen Fehler zurück, wenn Sie nicht AzCopy v 8.1 verwenden.</span><span class="sxs-lookup"><span data-stu-id="d5198-112">The AzCopy command that's displayed on the **Upload files** page shown in the previous screenshot returns an error if you're not using AzCopy v8.1.</span></span> <span data-ttu-id="d5198-113">Informationen zum Installieren dieser Version finden Sie unter [übertragen von Daten mit der AzCopy v 8.1 unter Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="d5198-113">To install this version, see [Transfer data with the AzCopy v8.1 on Windows](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span>

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a><span data-ttu-id="d5198-114">AzCopy ist auf dem lokalen Computer nicht installiert oder wird nicht am Standardspeicherort installiert.</span><span class="sxs-lookup"><span data-stu-id="d5198-114">AzCopy isn't installed on the local computer or it's not installed in the default location</span></span>

<span data-ttu-id="d5198-115">Wenn AzCopy nicht installiert ist oder an einem anderen Speicherort als dem standardmäßigen Installationsspeicherort installiert ist ( `%ProgramFiles(x86)%`Dies ist), wird möglicherweise die folgende Fehlermeldung angezeigt, wenn Sie den AzCopy-Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="d5198-115">If AzCopy isn't installed or it's installed in a location other than the default install location (which is `%ProgramFiles(x86)%`), you may receive the following error when you run the AzCopy command:</span></span>

    The system cannot find the path specified.

<span data-ttu-id="d5198-116">Wenn AzCopy nicht auf dem lokalen Computer installiert ist, können Sie [hier](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy)installieren.</span><span class="sxs-lookup"><span data-stu-id="d5198-116">If AzCopy isn't installed on the local computer, you can install from [here](https://docs.microsoft.com/previous-versions/azure/storage/storage-use-azcopy).</span></span> <span data-ttu-id="d5198-117">Stellen Sie sicher, dass Sie Sie am Standardspeicherort installieren.</span><span class="sxs-lookup"><span data-stu-id="d5198-117">Be sure to install it in the default location.</span></span>

<span data-ttu-id="d5198-118">Wenn AzCopy installiert ist, aber an einem anderen Speicherort als dem Standardspeicherort installiert ist, können Sie den Befehl Kopieren, in eine Textdatei einfügen und dann den Pfad zu dem Speicherort ändern, an dem AzCopy installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d5198-118">If AzCopy is installed, but it's installed in a location different than the default location, you can copy the command, paste it to a text file, and then change the path to the location where AzCopy is installed.</span></span> <span data-ttu-id="d5198-119">Wenn sich beispielsweise Azcopy in `%ProgramFiles%`befindet, können Sie den ersten Teil des Befehls von `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` in in ändern. `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`</span><span class="sxs-lookup"><span data-stu-id="d5198-119">For example, if Azcopy is located in `%ProgramFiles%`, then you can change the first part of the command from `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` to `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy`.</span></span> <span data-ttu-id="d5198-120">Nachdem Sie diese Änderung vorgenommen haben, kopieren Sie Sie aus der Textdatei, und führen Sie dann eine Eingabeaufforderung aus.</span><span class="sxs-lookup"><span data-stu-id="d5198-120">After you make this change, copy it from the text file and then run it a Command Prompt.</span></span>

> [!TIP]
> <span data-ttu-id="d5198-121">Wenn AzCopy an einem anderen Speicherort als dem standardmäßigen Installationsspeicherort installiert ist, sollten Sie ihn deinstallieren und dann am Standardspeicherort erneut installieren.</span><span class="sxs-lookup"><span data-stu-id="d5198-121">If AzCopy is installed in a location other then the default install location, consider uninstalling it and then re-installing it in the default location.</span></span> <span data-ttu-id="d5198-122">Dies wird dazu beitragen, dieses Problem in Zukunft zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d5198-122">This will help prevent this issue in the future.</span></span>
