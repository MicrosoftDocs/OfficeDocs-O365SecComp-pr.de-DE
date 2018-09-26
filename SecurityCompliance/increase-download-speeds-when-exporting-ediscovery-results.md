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
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a>Die Download-Leistung zu steigern, beim Exportieren von eDiscovery-Suchergebnisse aus Office 365

Wenn Sie das Office 365 eDiscovery-Export-Tool verwenden, um Laden Sie die Ergebnisse einer Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center oder Download von Daten aus Office 365 erweiterte eDiscovery, das Tool startet eine bestimmte Anzahl von gleichzeitigen exportieren Vorgänge, die Daten auf den lokalen Computer herunterladen. Standardmäßig ist die Anzahl der gleichzeitigen Operationen auf 8 Mal die Anzahl der Prozessorkerne auf dem Computer festgelegt, den Sie verwenden, um die Daten herunterladen. Wenn Sie einen dual-Core-Computer (d. h. zwei Prozessoren auf einem Chip) verfügen, ist die Standardanzahl zulässiger gleichzeitige Exportvorgänge beispielsweise 16. Um die Daten Übertragungsdurchsatz und beschleunigen der Downloadvorgang erhöhen möchten, können Sie die Anzahl der gleichzeitigen Operationen erhöhen, durch eine Einstellung für die Windows-Registrierung konfigurieren, auf dem Computer, mit denen Sie die Suchergebnisse herunterladen. Um den Download-Vorgang beschleunigen wird empfohlen, dass Sie mit der Einstellung der 24 gleichzeitige Vorgänge beginnen.
  
Wenn Sie die Suchergebnisse über ein Netzwerk mit niedriger Bandbreite herunterladen, möglicherweise Erhöhung dieser Einstellung negativ auswirken. Alternativ können Sie möglicherweise auf die Einstellung für mehr als 24 gleichzeitige Transaktionen in einem Netzwerk mit hoher Bandbreite erhöhen (die maximale Anzahl der gleichzeitigen Operationen ist 512). Nachdem Sie diese Einstellung in der Registrierung konfiguriert haben, müssen Sie möglicherweise ändern, um die optimale Anzahl gleichzeitiger Vorgänge für Ihre Umgebung zu suchen.
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a>Erstellen einer Einstellung so ändern Sie die Anzahl der gleichzeitigen Operationen beim Exportieren von Daten in der Registrierungs

Führen Sie das folgende Verfahren auf dem Computer, mit denen Sie die Sicherheit der Suchergebnisse heruntergeladen werden &amp; Compliance Center oder die Daten aus der erweiterten eDiscovery.
  
1. Schließen Sie das Office 365 eDiscovery-Export-Tool aus, wenn es geöffnet ist. 
    
2. Speichern Sie den folgenden Text zu einer Registrierungsdatei Fenster mithilfe der Dateiname Suffix reg; beispielsweise ConcurrentOperations.reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    Wie vorherige erläutert, es wird empfohlen, dass Sie mit 24 gleichzeitige Vorgänge starten, und klicken Sie dann diese Einstellung nach Bedarf ändern.
    
3. Klicken Sie in Windows Explorer auf, oder doppelklicken Sie auf die REG-Datei, die Sie im vorherigen Schritt erstellt haben.
    
4. Klicken Sie auf **Ja,** um den Registrierungs-Editor die Änderung vornehmen zu lassen, klicken Sie im Fenster User Access Control. 
    
5. Wenn Sie aufgefordert werden, um den Vorgang fortzusetzen, klicken Sie auf **Ja**.
    
    Den Registrierungs-Editor zeigt eine Meldung, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.
    
6. Sie können wiederholen Sie die Schritte 2 bis 5 zum Ändern des Werts für die `DownloadConcurrency` Einstellung in der Registrierung. 
    
    > [!IMPORTANT]
    > Nachdem Sie erstellen oder Ändern der `DownloadConcurrency` Registrierung festlegen, müssen Sie unbedingt Erstellen eines neuen Auftrags Export oder neu starten einer vorhandenen Exportauftrag für die Suchergebnisse oder Daten, die Sie herunterladen möchten. Finden Sie [Weitere Informationen](increase-download-speeds-when-exporting-ediscovery-results.md#moreinfo) im Abschnitt Weitere Informationen. 
  
## <a name="more-information"></a>Weitere Informationen

- Ein neuen Registrierungsschlüssel wird beim ersten erstellt, wenn Sie die REG-Datei ausführen, die Sie in diesem Verfahren erstellt haben. Anschließend wird die `DownloadConcurrency` registrierungseinstellung bearbeitet wird bei jedem ändern, und führen Sie die REG-Datei bearbeiten erneut aus. 
    
- Das Office 365 eDiscovery-Export-Tool verwendet die [Azure AzCopy Dienstprogramm](https://go.microsoft.com/fwlink/?linkid=849949) zum Suchen von Daten aus der Sicherheit herunterladen &amp; Compliance Center oder von erweiterten eDiscovery. Konfigurieren der `DownloadConcurrency` registrierungseinstellung ist ähnlich wie die Verwendung **des/NC** -Parameters beim Ausführen des Dienstprogramms AzCopy. Damit die Einstellung der Registrierung des `"DownloadConcurrency=24"` müssten die gleiche Auswirkung wie die Verwendung des Werts des Parameters des `/NC:24` mit dem Dienstprogramm AzCopy. 
    
- Wenn Sie einen Export Download beenden, der ist derzeit in Arbeit und starten Sie ihn neu (mit dem Versuch, die Suchergebnisse erneut laden), versucht das Office 365 eDiscovery-Export-Tool den gleichen Download fortzusetzen. Ja, wenn Sie einen Download starten, beenden, und ändern Sie die `DownloadConcurrency` Registrierung festlegen, die heruntergeladene Datei wahrscheinlich fehl, wenn Sie ihn neu starten, (durch Klicken auf **Download exportiert Ergebnisse**). Dies ist, da das Exporttool versucht, das Fortsetzen des vorherigen Downloads von Einstellungen, die nicht gültig sind, da Sie die Einstellung der Registrierung geändert haben.
    
    Aus diesem Grund nach dem Ändern der `DownloadConcurrency` Registrierung festlegen, müssen Sie unbedingt den Exportauftrag neu starten (durch Klicken auf **Export starten**) in das Wertpapier &amp; Compliance Center. Anschließend können Sie die exportierten Ergebnisse herunterladen. Weitere Informationen zum Exportieren von Suchergebnissen und Daten finden Sie unter:
    
  - [Exportieren von Suchergebnissen aus der Office 365-Sicherheit &amp; Compliance Center](export-search-results.md)
    
  - [Exportieren von Ergebnissen in Office 365 Advanced eDiscovery](export-results-in-advanced-ediscovery.md)
    
