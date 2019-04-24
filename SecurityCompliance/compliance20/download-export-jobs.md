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
# <a name="download-export-jobs"></a>Herunterladen von Exportaufträgen

Alle exportierten Daten werden zu einem Microsoft Azure-BLOB hinzugefügt. Dies bietet mehrere Optionen für die Verarbeitung der Daten Downstream. Es gibt mehrere Möglichkeiten, auf ein Azure-BLOB zuzugreifen. Eine Methode ist die Verwendung von Azure Storage Explorer. Diese Methode unterstützt einfache Verbindung, durchsuchen und herunterladen. Weitere Informationen finden Sie unter<https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-storage-explorer>

1.  Zum Herunterladen von Inhalten nach Abschluss eines Exportauftrags wechseln Sie zur Registerkarte Exporte, und wählen Sie einen Exportauftrag aus.

2.  Kopieren Sie den Text im Abschnitt "Standorte" des Flyouts.

![](../media/eDiscoExportJob.png)

3.  Öffnen Sie Azure Storage Explorer, und klicken Sie auf die Schaltfläche "verbinden"

![](../media/AzureStorageConnect.png)

4.  Wählen Sie "Use a Shared Access Signature URI" aus, und klicken Sie auf Weiter.

![](../media/AzureStorageConnect2.png)

5.  Fügen Sie den Speicherort Text in das Textfeld URI ein, und klicken Sie auf Weiter.

![](../media/AzureStorageConnect3.png)

6.  Klicken Sie auf Verbinden

![](../media/AzureStorageConnect4.png)

Dadurch wird der Export als Objekt in Speicherkonten/SAS-Attached Services/BLOB Containers hinzugefügt. Sie können den Export erkunden und alle Teile des Exports herunterladen.

![](../media/AzureStorageConnect5.png)