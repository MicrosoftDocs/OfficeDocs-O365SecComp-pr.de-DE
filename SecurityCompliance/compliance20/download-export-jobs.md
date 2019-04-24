---
title: Herunterladen von Exportaufträgen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 904bc5f8a6d6cef937d55336e8f383957713769a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32251903"
---
# <a name="download-export-jobs"></a><span data-ttu-id="d8e81-102">Herunterladen von Exportaufträgen</span><span class="sxs-lookup"><span data-stu-id="d8e81-102">Download export jobs</span></span>

<span data-ttu-id="d8e81-103">Alle exportierten Daten werden zu einem Microsoft Azure-BLOB hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d8e81-103">All exported data is added to a Microsoft Azure blob.</span></span> <span data-ttu-id="d8e81-104">Dies bietet mehrere Optionen für die Verarbeitung der Daten Downstream.</span><span class="sxs-lookup"><span data-stu-id="d8e81-104">This provides multiple options to handle the data downstream.</span></span> <span data-ttu-id="d8e81-105">Es gibt mehrere Möglichkeiten, auf ein Azure-BLOB zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d8e81-105">There are several ways to access an Azure blob.</span></span> <span data-ttu-id="d8e81-106">Eine Methode ist die Verwendung von Azure Storage Explorer.</span><span class="sxs-lookup"><span data-stu-id="d8e81-106">One method is to use Azure Storage Explorer.</span></span> <span data-ttu-id="d8e81-107">Diese Methode unterstützt einfache Verbindung, durchsuchen und herunterladen.</span><span class="sxs-lookup"><span data-stu-id="d8e81-107">This method supports simple connection, browsing and downloading.</span></span> <span data-ttu-id="d8e81-108">Weitere Informationen finden Sie unter<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span><span class="sxs-lookup"><span data-stu-id="d8e81-108">For more information, visit <https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer></span></span>

1.  <span data-ttu-id="d8e81-109">Zum Herunterladen von Inhalten nach Abschluss eines Exportauftrags wechseln Sie zur Registerkarte Exporte, und wählen Sie einen Exportauftrag aus.</span><span class="sxs-lookup"><span data-stu-id="d8e81-109">To download content after an export job is complete, go to the Exports tab and select an export job.</span></span>

2.  <span data-ttu-id="d8e81-110">Kopieren Sie den Text im Abschnitt "Standorte" des Flyouts.</span><span class="sxs-lookup"><span data-stu-id="d8e81-110">Copy the text in the “Locations” section of the flyout.</span></span>

![](../media/eDiscoExportJob.png)

3.  <span data-ttu-id="d8e81-111">Öffnen Sie Azure Storage Explorer, und klicken Sie auf die Schaltfläche "verbinden"</span><span class="sxs-lookup"><span data-stu-id="d8e81-111">Open Azure Storage Explorer and click the “Connect” button</span></span>

![](../media/AzureStorageConnect.png)

4.  <span data-ttu-id="d8e81-112">Wählen Sie "Use a Shared Access Signature URI" aus, und klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="d8e81-112">Select “Use a shared access signature URI” and click next</span></span>

![](../media/AzureStorageConnect2.png)

5.  <span data-ttu-id="d8e81-113">Fügen Sie den Speicherort Text in das Textfeld URI ein, und klicken Sie auf Weiter.</span><span class="sxs-lookup"><span data-stu-id="d8e81-113">Paste the Location text in the URI text box and click next</span></span>

![](../media/AzureStorageConnect3.png)

6.  <span data-ttu-id="d8e81-114">Klicken Sie auf Verbinden</span><span class="sxs-lookup"><span data-stu-id="d8e81-114">Click Connect</span></span>

![](../media/AzureStorageConnect4.png)

<span data-ttu-id="d8e81-115">Dadurch wird der Export als Objekt in Speicherkonten/SAS-Attached Services/BLOB Containers hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d8e81-115">This will add the export as an object in Storage Accounts/SAS-Attached Services/Blob Containers.</span></span> <span data-ttu-id="d8e81-116">Sie können den Export erkunden und alle Teile des Exports herunterladen.</span><span class="sxs-lookup"><span data-stu-id="d8e81-116">You will be able to explore the export and download all or portions of the export.</span></span>

![](../media/AzureStorageConnect5.png)