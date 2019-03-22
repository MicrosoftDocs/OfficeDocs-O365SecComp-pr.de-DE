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
# <a name="troubleshoot-azcopy-in-advanced-ediscovery-preview"></a>Problembehandlung bei AzCopy in Advanced eDiscovery (Preview)

Beim Laden von nicht-Office 365-Daten oder-Dokumenten zur Fehlerkorrektur in Advanced eDiscovery (Preview) stellt die Benutzeroberfläche einen Azure-AzCopy-Befehl bereit, der Parameter mit dem Speicherort enthält, an dem die Dateien, die Sie hochladen möchten, gespeichert sind und die Azure Speicherort, in den die Dateien hochgeladen werden. Um Ihre Dokumente hochzuladen, kopieren Sie diesen Befehl, und führen Sie ihn dann an einer EingabeaufForderungen auf Ihrem lokalen Computer aus.  Der folgende Screenshot zeigt ein Beispiel für einen AzCopy-Befehl:

![Hochladen nicht-Office 365-Dateien](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

In den meisten Fällen funktioniert der Befehl, der bereitgestellt wird, wenn Sie ihn ausführen. Es kann jedoch vorkommen, dass der angezeigte Befehl nicht erfolgreich ausgeführt wird. Hier einige mögliche Gründe.

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a>AzCopy wird nicht auf dem lokalen Computer installiert, oder es ist nicht am Standardspeicherort installiert

Wenn AzCopy nicht installiert ist oder an einem anderen Speicherort als dem Standard Installationsspeicherort installiert ist, wird `%ProgramFiles(x86)%`möglicherweise die folgende Fehlermeldung angezeigt, wenn Sie den AzCopy-Befehl ausführen:

    The system cannot find the path specified.

Wenn AzCopy nicht auf dem lokalen Computer installiert werden kann, können Sie von hier aus installieren (Sie müssen es unbedingt am Standardspeicherort installieren [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy)):.


Wenn AzCopy installiert ist, aber an einem anderen Speicherort als dem Standardspeicherort installiert ist, können Sie den Befehl Kopieren, ihn in eine Textdatei einfügen und dann den Pfad zu dem Speicherort ändern, an dem AzCopy tatsächlich installiert ist. Wenn sich beispielsweise Azcopy in `%ProgramFiles%`befindet, können Sie den ersten Teil des Befehls von `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` in ändern. `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy` Nachdem Sie diese Änderung vorgenommen haben, kopieren Sie Sie aus der Textdatei, und führen Sie Sie an einer EingabeaufForderungen aus.

> [!TIP]
> Wenn AzCopy an einem anderen Speicherort als dem Standard Installationsspeicherort installiert ist, sollten Sie ihn deinstallieren und dann erneut am Standardspeicherort installieren. Dadurch wird dieses Problem künftig verhindert.