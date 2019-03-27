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
ms.openlocfilehash: ddeb247be6981dbfdb874e270a123e4465914d86
ms.sourcegitcommit: c0d4fe3e43e22353f30034567ade28330266bcf7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2019
ms.locfileid: "30899924"
---
# <a name="increase-the-download-speed-when-exporting-ediscovery-search-results-from-office-365"></a>Höhere Downloadgeschwindigkeit beim Exportieren von eDiscovery-Suchergebnissen aus Office 365

Wenn Sie das Office 365 eDiscovery-Export Tool zum Herunterladen der Ergebnisse einer Inhaltssuche im Office 365 Security &amp; Compliance Center oder zum Herunterladen von Daten aus Office 365 Advanced eDiscovery verwenden, startet das Tool eine bestimmte Anzahl gleichzeitiger Export Vorgänge zum Herunterladen der Daten auf den lokalen Computer. Standardmäßig ist die Anzahl der gleichzeitigen Vorgänge auf die Anzahl der Kerne auf dem Computer festgelegt, den Sie zum Herunterladen der Daten verwenden. Wenn Sie beispielsweise einen Dual-Core-Computer (also zwei zentrale Verarbeitungseinheiten auf einem Chip) haben, ist die Standardanzahl gleichzeitiger Exportvorgänge 16. Um den Durchsatz bei der Datenübertragung zu erhöhen und den Downloadprozess zu beschleunigen, können Sie die Anzahl gleichzeitiger Vorgänge erhöhen, indem Sie auf dem Computer, auf dem Sie die Suchergebnisse herunterladen, eine Windows-Registrierungseinstellung konfigurieren. Um den Downloadprozess zu beschleunigen, empfehlen wir, dass Sie mit einer Einstellung von 24 gleichzeitigen Vorgängen beginnen.
  
Wenn Sie Suchergebnisse über ein Netzwerk mit niedriger Bandbreite herunterladen, kann sich die Erhöhung dieser Einstellung negativ auswirken. Alternativ können Sie die Einstellung möglicherweise auf mehr als 24 gleichzeitige Vorgänge in einem Netzwerk mit hoher Bandbreite (die maximale Anzahl gleichzeitiger Vorgänge beträgt 512). Nachdem Sie diese Registrierungseinstellung konfiguriert haben, müssen Sie Sie möglicherweise ändern, um die optimale Anzahl gleichzeitiger Vorgänge für Ihre Umgebung zu ermitteln.
  
## <a name="create-a-registry-setting-to-change-the-number-of-concurrent-operations-when-exporting-data"></a>Erstellen einer Registrierungseinstellung zum Ändern der Anzahl gleichzeitiger Vorgänge beim Exportieren von Daten

Führen Sie das folgende Verfahren auf dem Computer aus, auf dem Sie Suchergebnisse aus dem Security &amp; Compliance Center oder Daten aus Advanced eDiscovery herunterladen möchten.
  
1. Schließen Sie das Office 365 eDiscovery-Export Tool, wenn es geöffnet ist. 
    
2. Speichern Sie den folgenden Text in einer Fenster Registrierungsdatei mithilfe eines Dateinamen Suffixes von. reg; Beispiel: ConcurrentOperations. reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "DownloadConcurrency"="24"
    ```

    Wie bereits erläutert, empfiehlt es sich, mit 24 gleichzeitigen Vorgängen zu beginnen und diese Einstellung gegebenenfalls zu ändern.
    
3. Klicken oder Doppelklicken Sie in Windows Explorer auf die. reg-Datei, die Sie im vorherigen Schritt erstellt haben.
    
4. Klicken Sie im Fenster Benutzerzugriffssteuerung auf **Ja** , um die Änderung des Registrierungs-Editors zu ermöglichen. 
    
5. Wenn Sie zum Fortfahren aufgefordert werden, klicken Sie auf **Ja**.
    
    Der Registrierungs-Editor zeigt eine Meldung an, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.
    
6. Sie können die Schritte 2-5 wiederholen, um den Wert `DownloadConcurrency` für die Registrierungseinstellung zu ändern. 
    
    > [!IMPORTANT]
    > Nachdem Sie die `DownloadConcurrency` Registrierungseinstellung erstellt oder geändert haben, müssen Sie einen neuen Exportauftrag erstellen oder einen vorhandenen Exportauftrag für die Suchergebnisse oder Daten, die Sie herunterladen möchten, neu starten. Weitere Informationen finden Sie im Abschnitt [More Information](#more-information) . 
  
## <a name="more-information"></a>Weitere Informationen

- Bei der ersten Ausführung der reg-Datei, die Sie in diesem Verfahren erstellt haben, wird ein neuer Registrierungsschlüssel erstellt. Dann wird `DownloadConcurrency` die Registrierungseinstellung jedes Mal bearbeitet, wenn Sie die reg-Bearbeitungs Datei ändern und erneut ausführen. 
    
- Das Office 365 eDiscovery-Export Tool verwendet das [Azure AzCopy-Dienstprogramm](https://go.microsoft.com/fwlink/?linkid=849949) zum Herunterladen von &amp; Such Daten aus dem Security Compliance Center oder von Advanced eDiscovery. Das konfigurieren `DownloadConcurrency` der Registrierungseinstellung ähnelt der Verwendung des **/NC** -Parameters beim Starten des AzCopy-Dienstprogramms. Daher hätte die Registrierungseinstellung `"DownloadConcurrency=24"` von den gleichen Effekt wie die Verwendung des Parameterwerts von `/NC:24` mit dem AzCopy-Dienstprogramm. 
    
- Wenn Sie einen Export Download beenden, der derzeit ausgeführt wird, und diesen dann erneut starten (indem Sie versuchen, die Suchergebnisse erneut herunterzuladen), versucht das Office 365 eDiscovery-Export Tool, den gleichen Download wieder aufzunehmen. Wenn Sie also einen Download starten, ihn beenden und dann die `DownloadConcurrency` Registrierungseinstellung ändern, wird der Download wahrscheinlich fehlschlagen, wenn Sie ihn neu starten (indem Sie auf exportierte **Ergebnisse herunterladen**klicken). Dies liegt daran, dass das Export Tool versucht, den vorherigen Download mithilfe von Einstellungen fortzusetzen, die nicht gültig sind, da Sie die Registrierungseinstellung geändert haben.
    
    Nachdem Sie die `DownloadConcurrency` Registrierungseinstellung geändert haben, müssen Sie daher den Exportauftrag (durch Klicken auf **Neustart exportieren**) im Security &amp; Compliance Center neu starten. Dann können Sie die exportierten Ergebnisse herunterladen. Weitere Informationen zum Exportieren von Suchergebnissen und Daten finden Sie unter:
    
  - [Exportieren von Inhalts Suchergebnissen aus dem Office 365 &amp; Security Compliance Center](export-search-results.md)
    
  - [Exportieren von Ergebnissen in Office 365 Advanced eDiscovery](export-results-in-advanced-ediscovery.md)
    
