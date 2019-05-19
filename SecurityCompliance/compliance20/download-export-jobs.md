---
title: Herunterladen von Exportaufträgen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 56ed8eac259974b43ca0cd26b2bd0c339a5fc05b
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155147"
---
# <a name="download-export-jobs"></a>Herunterladen von Exportaufträgen

Alle exportierten Daten werden einem Microsoft Azure-BLOB hinzugefügt. Dies bietet mehrere Optionen zum Verarbeiten der Daten Downstream. Es gibt mehrere Möglichkeiten, auf ein Azure-BLOB zuzugreifen. Eine Methode ist die Verwendung des Azure Storage Explorers. Diese Methode unterstützt einfache Verbindung, durchsuchen und herunterladen. Weitere Informationen finden Sie unter<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer>

1.  Wenn Sie nach Abschluss eines Exportauftrags Inhalte herunterladen möchten, wechseln Sie zur Registerkarte Exports, und wählen Sie einen Exportauftrag aus.

2.  Kopieren Sie den Text im Flyout-Abschnitt "Locations".

![](../media/eDiscoExportJob.png)

3.  Öffnen Sie Azure Storage Explorer, und klicken Sie auf die Schaltfläche "verbinden"

![](../media/AzureStorageConnect.png)

4.  Wählen Sie "Use a Shared Access Signature URI" aus, und klicken Sie auf Next

![](../media/AzureStorageConnect2.png)

5.  Fügen Sie den Speicherort Text in das Textfeld URI ein, und klicken Sie auf Weiter.

![](../media/AzureStorageConnect3.png)

6.  Klicken Sie auf Verbinden

![](../media/AzureStorageConnect4.png)

Dadurch wird der Export als Objekt in Speicherkonten/SAS-Attached Services/BLOB-Containern hinzugefügt. Sie können den Export durchsuchen und alle oder Teile des Exports herunterladen.

![](../media/AzureStorageConnect5.png)