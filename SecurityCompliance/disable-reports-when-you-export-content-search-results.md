---
title: Deaktivieren von Berichten beim Exportieren von Inhalts Suchergebnissen im Office 365 Security &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: MOE150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Bearbeiten Sie die Windows-Registrierung auf dem lokalen Computer, um Berichte zu deaktivieren, wenn Sie die Ergebnisse einer Inhaltssuche aus dem &amp; Office 365 Security Comliance Center exportieren. Durch das Deaktivieren dieser Berichte kann die Downloadzeit beschleunigt und Speicherplatz gespart werden.
ms.openlocfilehash: 0be2be18eaccb618a49e1b58a5c0e53d0a339d1e
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213475"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a>Deaktivieren von Berichten beim Exportieren von Inhalts Suchergebnissen im Office 365 Security &amp; Compliance Center

Wenn Sie das Office 365 eDiscovery-Export Tool verwenden, um die Ergebnisse einer Inhaltssuche im Security &amp; Compliance Center zu exportieren, erstellt und exportiert das Tool automatisch zwei Berichte, die zusätzliche Informationen zu den exportierten Inhalten enthalten. Diese Berichte sind die Datei results. CSV und die Datei Manifest. XML (Lesen Sie den Abschnitt [häufig gestellte Fragen zum Deaktivieren von Export Berichten](#frequently-asked-questions-about-disabling-export-reports) in diesem Thema für detaillierte Beschreibungen dieser Berichte). Da diese Dateien sehr umfangreich sein können, können Sie die Downloadzeit beschleunigen und Speicherplatz sparen, indem Sie verhindern, dass diese Dateien exportiert werden. Ändern Sie dazu die Windows-Registrierung auf dem Computer, den Sie zum Exportieren der Suchergebnisse verwenden. Wenn Sie die Berichte zu einem späteren Zeitpunkt hinzufügen möchten, können Sie die Registrierungseinstellung bearbeiten. 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a>Erstellen von Registrierungseinstellungen zum Deaktivieren der Export Berichte

Führen Sie auf dem Computer, auf dem Sie die Ergebnisse einer Inhaltssuche exportieren möchten, das folgende Verfahren aus.
  
1. Schließen Sie das Office 365 eDiscovery-Export Tool, wenn es geöffnet ist.
    
2. Führen Sie einen oder beide der folgenden Schritte aus, je nachdem, welchen Exportbericht Sie deaktivieren möchten.
    
    - **Results. CSV**
    
      Speichern Sie den folgenden Text in einer Windows-Registrierungsdatei mithilfe eines filename-Suffixes von. reg; Beispiel: DisableResultsCsv. reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - **Manifest. XML**
    
      Speichern Sie den folgenden Text in einer Windows-Registrierungsdatei mithilfe eines filename-Suffixes von. reg; Beispiel: DisableManifestXml. reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. Klicken oder Doppelklicken Sie in Windows Explorer auf die. reg-Datei, die Sie in den vorherigen Schritten erstellt haben.
    
4. Klicken Sie im Fenster Benutzerzugriffssteuerung auf **Ja** , um die Änderung des Registrierungs-Editors zu ermöglichen. 
    
5. Wenn Sie zum Fortfahren aufgefordert werden, klicken Sie auf **Ja**.
    
    Der Registrierungs-Editor zeigt eine Meldung an, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a>Bearbeiten von Registrierungseinstellungen zum erneuten Aktivieren der Export Berichte

Wenn Sie die Berichte "results. csv" und "Manifest. xml" deaktiviert haben, indem Sie die. reg-Dateien im vorherigen Verfahren erstellt haben, können Sie diese Dateien bearbeiten, um einen Bericht erneut zu aktivieren, sodass er mit den Suchergebnissen exportiert wird. Führen Sie erneut das folgende Verfahren auf dem Computer aus, auf dem Sie die Ergebnisse einer Inhaltssuche exportieren.
  
1. Schließen Sie das Office 365 eDiscovery-Export Tool, wenn es geöffnet ist.
    
2. Bearbeiten Sie eine oder beide der reg-Bearbeitungs Dateien, die Sie im vorherigen Verfahren erstellt haben.
    
    - **Results. CSV**
    
        Öffnen Sie die Datei DisableResultsCsv. reg im Editor, ändern Sie `False` den `True`Wert in, und speichern Sie die Datei. Nach dem Bearbeiten der Datei sieht es beispielsweise wie folgt aus:
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - **Manifest. XML**
    
        Öffnen Sie die Datei DisableManifestXml. reg im Editor, ändern Sie `False` den `True`Wert in, und speichern Sie die Datei. Nach dem Bearbeiten der Datei sieht es beispielsweise wie folgt aus:
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. Klicken oder Doppelklicken Sie in Windows Explorer auf eine REG-Datei, die Sie im vorherigen Schritt bearbeitet haben.
    
4. Klicken Sie im Fenster Benutzerzugriffssteuerung auf **Ja** , um die Änderung des Registrierungs-Editors zu ermöglichen. 
    
5. Wenn Sie zum Fortfahren aufgefordert werden, klicken Sie auf **Ja**.
    
    Der Registrierungs-Editor zeigt eine Meldung an, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a>Häufig gestellte Fragen zum Deaktivieren von Export Berichten
<a name="faqs"> </a>

 **Was sind die Berichte "results. csv" und "Manifest. xml"?**
  
Die Dateien results. CSV und Manifest. XML enthalten zusätzliche Informationen zu den exportierten Inhalten.
  
- **Results. CSV** ein Excel-Dokument, das Informationen zu jedem Element enthält, das als Suchergebnis heruntergeladen wird. Für e-Mails enthält das Ergebnisprotokoll Informationen zu den einzelnen Nachrichten, einschließlich: 
    
  - Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).
    
  - Das Datum, an dem die Nachricht gesendet oder empfangen wurde.
    
  - Die Betreffzeile der Nachricht.
    
  - Absender und Empfänger der Nachricht.
    
  - Gibt an, ob es sich bei der Nachricht um eine doppelte Nachricht handelt, wenn Sie beim Exportieren der Suchergebnisse Deduplizierung aktiviert haben. Doppelte Nachrichten haben einen Wert in der **ÜbergeordnetEn Itemid** -Spalte, die die Nachricht als Duplikat identifiziert. Der Wert in der **ÜbergeordnetEn Itemid** -Spalte ist identisch mit dem Wert in der Spalte **Element-Dokument-Nr** der Nachricht, die exportiert wurde. 
    
    Für Dokumente aus SharePoint und OneDrive for Business-Websites enthält das Ergebnisprotokoll Informationen zu jedem Dokument, einschließlich:
    
  - Die URL für das Dokument.
    
  - Die URL für die Websitesammlung, in der sich das Dokument befindet.
    
  - Das Datum, an dem das Dokument zuletzt geändert wurde.
    
  - Der Name des Dokuments (das sich in der Spalte Betreff im Ergebnisprotokoll befindet).
    
- **Manifest. XML** eine Manifestdatei (im XML-Format), die Informationen zu jedem in den Suchergebnissen enthaltenen Element enthält. Die Informationen in diesem Bericht sind identisch mit dem Bericht "results. csv", aber es ist in dem Format, das im Electronic Discovery Reference Model (EDRM) angegeben ist. Weitere Informationen zu EDRM finden Sie unter [https://www.edrm.net](https://www.edrm.net).
    
 **Wann sollte ich den Export dieser Berichte deaktivieren?**
  
Es hängt von ihren spezifischen Anforderungen ab. Viele Organisationen benötigen keine zusätzlichen Informationen zu Suchergebnissen und benötigen diese Berichte nicht.
  
 **Auf welchem Computer muss ich vorgehen?**
  
 Sie müssen die Registrierungseinstellung auf jedem lokalen Computer ändern, auf dem Sie das Office 365 eDiscovery-Export Tool ausführen. 
  
 **Muss ich den Computer neu starten, nachdem ich diese Einstellung geändert habe?**
  
Nein, Sie müssen den Computer nicht neu starten. Wenn jedoch das Office 365 eDiscovery-Export Tool läuft, müssen Sie es schließen und neu starten, nachdem Sie die Registrierungseinstellung geändert haben.
  
 **Wird ein vorhandener Registrierungsschlüssel bearbeitet oder wird ein neuer Schlüssel erstellt?**
  
Bei der ersten Ausführung der reg-Datei, die Sie im Verfahren in diesem Thema erstellt haben, wird ein neuer Registrierungsschlüssel erstellt. Dann wird die Einstellung jedes Mal bearbeitet, wenn Sie die reg-Bearbeitungs Datei ändern und erneut ausführen.
