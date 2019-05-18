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
ms.openlocfilehash: 2c8378cf7b9bd21f901b1babbebdcb0b69a8ed73
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34151517"
---
# <a name="troubleshoot-azcopy-in-advanced-ediscovery"></a>Problembehandlung bei AzCopy in Advanced eDiscovery

Beim Laden von nicht Office 365 Daten oder Dokumenten zur Fehlerbehebung in Advanced eDiscovery stellt die Benutzeroberfläche einen Azure AzCopy-Befehl bereit, der Parameter mit dem Speicherort enthält, an dem die Dateien, die Sie hochladen möchten, gespeichert werden und der Azure-Speicher Speicherort, in den die Dateien hochgeladen werden. Zum Hochladen Ihrer Dokumente kopieren Sie diesen Befehl und führen ihn dann an einer Eingabeaufforderung auf dem lokalen Computer aus.  Das folgende Screenshot zeigt ein Beispiel für einen AzCopy-Befehl:

![Hochladen nicht Office 365er Dateien](../media/46ba68f6-af11-4e70-bb91-5fc7973516e3.png)

In den meisten Fällen funktioniert der Befehl, der bereitgestellt wird, wenn Sie ihn ausführen. Es kann jedoch vorkommen, dass der angezeigte Befehl nicht erfolgreich ausgeführt wird. Es folgen einige mögliche Gründe.

## <a name="azcopy-isnt-installed-on-the-local-computer-or-its-not-installed-in-the-default-location"></a>AzCopy ist auf dem lokalen Computer nicht installiert oder wird nicht am Standardspeicherort installiert.

Wenn AzCopy nicht installiert ist oder an einem anderen Speicherort als dem standardmäßigen Installationsspeicherort installiert ist ( `%ProgramFiles(x86)%`Dies ist), wird möglicherweise die folgende Fehlermeldung angezeigt, wenn Sie den AzCopy-Befehl ausführen:

    The system cannot find the path specified.

Wenn AzCopy nicht auf dem lokalen Computer installiert ist, können Sie von hier aus installieren (wobei sichergestellt wird, dass es am Standard [https://docs.microsoft.com/azure/storage/common/storage-use-azcopy](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy)Speicherort installiert wird):.


Wenn AzCopy installiert ist, aber an einem anderen Speicherort als dem Standardspeicherort installiert ist, können Sie den Befehl Kopieren, in eine Textdatei einfügen und dann den Pfad zu dem Speicherort ändern, an dem AzCopy tatsächlich installiert ist. Wenn sich beispielsweise Azcopy in `%ProgramFiles%`befindet, können Sie den ersten Teil des Befehls von `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy.exe` in in ändern. `%ProgramFiles%\Microsoft SDKs\Azure\AzCopy` Nachdem Sie diese Änderung vorgenommen haben, kopieren Sie Sie aus der Textdatei, und führen Sie dann eine Eingabeaufforderung aus.

> [!TIP]
> Wenn AzCopy an einem anderen Speicherort als dem standardmäßigen Installationsspeicherort installiert ist, sollten Sie ihn deinstallieren und dann am Standardspeicherort erneut installieren. Dies wird dazu beitragen, dieses Problem in Zukunft zu vermeiden.