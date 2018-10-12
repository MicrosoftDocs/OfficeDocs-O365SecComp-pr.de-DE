---
title: Ändern Sie die Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Sie können die Standardgröße von PST-Dateien ändern, die beim Exportieren von eDiscovery-Suchergebnisse auf den Computer heruntergeladen werden.
ms.openlocfilehash: c01f05a02fd94941eb2eb7a05b4c84ffecec9b39
ms.sourcegitcommit: 448c5897e44448adfc82e3eaffb774c770c04815
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2018
ms.locfileid: "25522246"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a>Ändern Sie die Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse

Wenn Sie das Office 365 eDiscovery-Export-Tool verwenden, um die e-Mail-Ergebnisse einer eDiscovery-Suche aus der verschiedenen Microsoft eDiscovery-Tools zu exportieren, wird die Standardgröße des eine PST-Datei, die exportiert werden kann 10 GB. Wenn Sie diese Standardgröße ändern möchten, können Sie die Windows-Registrierung auf dem Computer bearbeiten, mit denen Sie die Suchergebnisse exportieren. Ein Grund hierfür ist, sodass eine PST-Datei auf das Wechselmedium, solche einer DVD, einer CD oder ein USB-Laufwerk passen. 
  
> [!NOTE]
>  Das Office 365 eDiscovery-Export-Tool wird verwendet, um die Suchergebnisse zu exportieren, bei der Verwendung von Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center, Compliance-eDiscovery in Exchange Online und das eDiscovery Center in SharePoint Online. 
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a>Erstellen Sie einen Registrierungseintrag so ändern Sie die Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse

Führen Sie das folgende Verfahren auf dem Computer, mit denen Sie die Ergebnisse einer eDiscovery-Suche exportiert werden.
  
1. Schließen Sie das Office 365 eDiscovery-Export-Tool aus, wenn es geöffnet ist. 
    
2. Speichern Sie den folgenden Text zu einer Registrierungsdatei Fenster mithilfe der Dateiname Suffix reg; beispielsweise PstExportSize.reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    Im obigen Beispiel die `PstSizeLimitInBytes` Wert auf 1.073.741.824 Bytes oder ungefähr 1 GB festgelegt ist. Hier sind einige andere Beispielwerte für die `PstSizeLimitInBytes` Einstellung. 
    
    |**Größe in GB (etwa)**|**Größe in bytes**|
    |:-----|:-----|
    |.7 GB (700 MB)  <br/> |751619277  <br/> |
    |2 GB  <br/> |2147483648  <br/> |
    |4 GB  <br/> |4294967296  <br/> |
    |8 GB  <br/> |8589934592  <br/> |
   
3. Ändern der `PstSizeLimitInBytes` Wert auf die gewünschte maximale Größe einer PST-Datei bei der Suchergebnisse exportieren und speichern Sie die Datei. 
    
4. Klicken Sie in Windows Explorer auf, oder doppelklicken Sie auf die REG-Datei, die Sie in den vorherigen Schritten erstellt haben.
    
5. Klicken Sie auf **Ja,** um den Registrierungs-Editor die Änderung vornehmen zu lassen, klicken Sie im Fenster User Access Control. 
    
6. Wenn Sie aufgefordert werden, um den Vorgang fortzusetzen, klicken Sie auf **Ja**.
    
    Den Registrierungs-Editor zeigt eine Meldung, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.
    
7. Sie können wiederholen Sie die Schritte 3 bis 6 zum Ändern des Werts für die `PstSizeLimitInBytes` Einstellung in der Registrierung. 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a>Häufig gestellte Fragen zum Ändern der Standardgröße von PST-Dateien beim Exportieren von eDiscovery-Suchergebnisse

 **Warum ist der Standardwert 10 GB Größe?**
  
Die Standardgröße von 10 GB wurde basierend auf Feedback von Kunden; 10 GB lautet ein guter Kompromiss zwischen den optimalen Umfang des Inhalts in einer einzelnen PST-Datei und eine minimale Möglichkeit der Beschädigung der Datei.
  
 **Ich habe erhöhen oder verringern Sie die Standardgröße von PST-Dateien?**
  
Kunden in der Regel die maximale Größe reduzieren, sodass die Suchergebnisse auf Wechselmedium passt, dass sie andere Standorte in ihrer Organisation physisch versenden können. Es wird nicht empfohlen, dass Sie die Standardgröße erhöhen, da PST-größer Dateien als 10 GB Beschädigung Probleme auftreten.
  
 **Welche Computer müssen dazu auf werden?**
  
Sie müssen die Einstellung in der Registrierung auf einem lokalen Computer zu ändern, die Sie für das Office 365 eDiscovery-Export-Tool ausführen.
  
 **Nachdem ich diese Einstellung ändern, müssen ich den Computer neu starten?**
  
Nein, müssen Sie den Computer neu starten. Jedoch nicht, wenn das Office 365 eDiscovery-Export-Tool ausgeführt wird, müssen Sie es und dem Neustart zu schließen, nachdem Sie diese Einstellung ändern.
  
 **Bearbeitet ein bereits vorhandenen Registrierungsschlüssel abrufen, oder haben ein neues Schlüssels erstellt abrufen?**
  
Ein neuen Registrierungsschlüssel wird beim ersten erstellt, wenn Sie die REG-Datei ausführen, die Sie in diesem Verfahren erstellt haben. Die Einstellung wird dann jedes Mal bearbeitet, Sie ändern, und führen Sie die REG-Datei bearbeiten erneut aus.
