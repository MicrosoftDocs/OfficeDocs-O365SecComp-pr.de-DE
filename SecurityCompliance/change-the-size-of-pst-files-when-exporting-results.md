---
title: Ändern der Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnissen
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 10/12/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: 04e9de2d-765b-457b-a98a-d0f60bfb13f2
description: Sie können die Standardgröße von PST-Dateien ändern, die beim Exportieren von eDiscovery-Suchergebnissen auf Ihren Computer heruntergeladen werden.
ms.openlocfilehash: 98b543b6e34cb9cb075a765671def91742aee6c1
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999718"
---
# <a name="change-the-size-of-pst-files-when-exporting-ediscovery-search-results"></a>Ändern der Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnissen

Wenn Sie das Office 365 eDiscovery-Export Tool verwenden, um die e-Mail-Ergebnisse einer eDiscovery-Suche aus den verschiedenen Microsoft eDiscovery-Tools zu exportieren, beträgt die Standardgröße einer PST-Datei, die exportiert werden kann, 10 GB. Wenn Sie diese Standardgröße ändern möchten, können Sie die Windows-Registrierung auf dem Computer bearbeiten, den Sie zum Exportieren der Suchergebnisse verwenden. Ein Grund hierfür ist, dass eine PST-Datei auf Wechseldatenträger, eine DVD, eine CD oder ein USB-Laufwerk angepasst werden kann. 
  
> [!NOTE]
>  Das Office 365 eDiscovery-Export Tool wird verwendet, um die Suchergebnisse zu exportieren, wenn Sie das Tool für die Inhaltssuche im Security and Compliance Center, in-Place eDiscovery in Exchange Online und im eDiscovery Center in SharePoint Online verwenden.
  
## <a name="create-a-registry-setting-to-change-the-size-of-pst-files-when-you-export-ediscovery-search-results"></a>Erstellen einer Registrierungseinstellung zum Ändern der Größe von PST-Dateien beim Exportieren von eDiscovery-Suchergebnissen

Führen Sie auf dem Computer, auf dem Sie die Ergebnisse einer eDiscovery-Suche exportieren möchten, das folgende Verfahren aus.
  
1. Schließen Sie das Office 365 eDiscovery-Export Tool, wenn es geöffnet ist. 
    
2. Speichern Sie den folgenden Text in einer Fenster Registrierungsdatei mithilfe eines Dateinamen Suffixes von. reg; Beispiel: PstExportSize. reg. 
    
    ```
    Windows Registry Editor Version 5.00
    [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool]
    "PstSizeLimitInBytes"="1073741824"
    ```

    Im obigen Beispiel ist der `PstSizeLimitInBytes` wert auf 1.073.741.824 Byte oder ungefähr 1 GB festgelegt. Im folgenden finden Sie einige andere Beispielwerte `PstSizeLimitInBytes` für die Einstellung. 
    
    |**Größe in GB (ca.)**|**Größe in Byte**|
    |:-----|:-----|
    |.7 GB (700 MB)  <br/> |751619277  <br/> |
    |2 GB  <br/> |2147483648  <br/> |
    |4 GB  <br/> |4294967296  <br/> |
    |8 GB  <br/> |8589934592  <br/> |
   
3. Ändern Sie `PstSizeLimitInBytes` den Wert in die gewünschte maximale Größe einer PST-Datei, wenn Sie die Suchergebnisse exportieren, und speichern Sie die Datei. 
    
4. Klicken oder Doppelklicken Sie in Windows Explorer auf die. reg-Datei, die Sie in den vorherigen Schritten erstellt haben.
    
5. Klicken Sie im Fenster Benutzerzugriffssteuerung auf **Ja** , um die Änderung des Registrierungs-Editors zu ermöglichen. 
    
6. Wenn Sie zum Fortfahren aufgefordert werden, klicken Sie auf **Ja**.
    
    Der Registrierungs-Editor zeigt eine Meldung an, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.
    
7. Sie können die Schritte 3-6 wiederholen, um den Wert `PstSizeLimitInBytes` für die Registrierungseinstellung zu ändern. 
  
## <a name="frequently-asked-questions-about-changing-the-default-size-of-pst-files-when-you-export-ediscovery-search-results"></a>Häufig gestellte Fragen zum Ändern der Standardgröße von PST-Dateien beim Exportieren von eDiscovery-Suchergebnissen

 **Warum ist die Standardgröße 10 GB?**
  
Die Standardgröße von 10 GB basierte auf Kundenfeedback; 10 GB stellt eine gute Balance zwischen der optimalen Menge an Inhalten in einer einzelnen PST-Datei und einer minimalen Wahrscheinlichkeit für eine Beschädigung von Dateien dar.
  
 **Sollte ich die Standardgröße von PST-Dateien vergrößern oder verkleinern?**
  
Kunden neigen dazu, die Größenbeschränkung zu verringern, sodass die Suchergebnisse auf Wechseldatenträger angepasst werden, die Sie physisch an andere Standorte in Ihrer Organisation senden können. Es wird nicht empfohlen, dass Sie die Standardgröße vergrößern, da PST-Dateien, die größer als 10 GB sind, möglicherweise beschädigte Probleme aufweisen.
  
 **Auf welchem Computer muss ich vorgehen?**
  
Sie müssen die Registrierungseinstellung auf jedem lokalen Computer ändern, auf dem Sie das Office 365 eDiscovery-Export Tool ausführen.
  
 **Muss ich den Computer neu starten, nachdem ich diese Einstellung geändert habe?**
  
Nein, Sie müssen den Computer nicht neu starten. Wenn jedoch das Office 365 eDiscovery-Export Tool läuft, müssen Sie es beenden und es nach dem Ändern dieser Einstellung neu starten.
  
 **Wird ein vorhandener Registrierungsschlüssel bearbeitet oder wird ein neuer Schlüssel erstellt?**
  
Bei der ersten Ausführung der reg-Datei, die Sie in diesem Verfahren erstellt haben, wird ein neuer Registrierungsschlüssel erstellt. Dann wird die Einstellung jedes Mal bearbeitet, wenn Sie die reg-Bearbeitungs Datei ändern und erneut ausführen.
