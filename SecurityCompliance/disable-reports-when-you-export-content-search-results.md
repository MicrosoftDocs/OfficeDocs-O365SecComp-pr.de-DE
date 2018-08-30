---
title: Deaktivieren von Berichten beim Exportieren von Suchergebnissen in die Office 365-Sicherheit &amp; Compliance Center
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 12/30/2016
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9b0ff0c-282b-4a44-b43f-cfc5b96557f9
description: Bearbeiten Sie die Windows-Registrierung auf dem lokalen Computer, um Berichte zu deaktivieren, wenn Sie die Ergebnisse einer Suche Content aus der Office 365-Sicherheit exportieren &amp; Comliance Center. Deaktivieren diese Berichte kann Download beschleunigen und Speicherplatz.
ms.openlocfilehash: 3c09e0563ddd4469f21950dc3a698ce08b0014df
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529977"
---
# <a name="disable-reports-when-you-export-content-search-results-in-the-office-365-security-amp-compliance-center"></a>Deaktivieren von Berichten beim Exportieren von Suchergebnissen in die Office 365-Sicherheit &amp; Compliance Center

Wenn Sie das Office 365 eDiscovery-Export-Tool verwenden, um exportieren Sie die Ergebnisse einer Suche Inhalte in das Wertpapier &amp; Compliance Center, das Tool automatisch erstellt und exportiert zwei Berichte, die zusätzliche Informationen über die exportierten Inhalte enthalten. Diese Berichte sind die Results.csv und die Datei Manifest.xml (Siehe den Abschnitt [häufig gestellte Fragen zum Deaktivieren von Exportieren von Berichten](#frequently-asked-questions-about-disabling-export-reports) in diesem Thema eine ausführliche Beschreibung dieser Berichte). Da diese Dateien sehr groß sein können, können Download beschleunigen und Speicherplatz sparen, indem Sie verhindern, dass diese Dateien exportiert wird. Hierzu können Sie der Windows-Registrierung auf dem Computer, mit denen Sie die Suchergebnisse exportieren ändern. Wenn Sie die Berichte zu einem späteren Zeitpunkt einschließen möchten, können Sie die registrierungseinstellung bearbeiten. 
  
## <a name="create-registry-settings-to-disable-the-export-reports"></a>Erstellen von Einstellungen in der Registrierung, um das Exportieren von Berichten zu deaktivieren.

Führen Sie das folgende Verfahren auf dem Computer, mit denen Sie die Ergebnisse einer Inhaltssuche exportiert werden.
  
1. Schließen Sie das Office 365 eDiscovery-Export-Tool aus, wenn es geöffnet ist.
    
2. Führen Sie eine oder beide der folgenden Schritte aus, je nach dem, die Bericht exportieren Sie deaktivieren möchten.
    
    - **Results.csv**
    
      Speichern Sie den folgenden Text zu einer Windows-Registrierungsdatei mithilfe der Dateiname Suffix reg; beispielsweise DisableResultsCsv.reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d False 
      ```

    - **"Manifest.xml"**
    
      Speichern Sie den folgenden Text zu einer Windows-Registrierungsdatei mithilfe der Dateiname Suffix reg; beispielsweise DisableManifestXml.reg.
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d False 
      ```

3. Klicken Sie in Windows Explorer auf, oder doppelklicken Sie auf die REG-Datei, die Sie in den vorherigen Schritten erstellt haben.
    
4. Klicken Sie auf **Ja,** um den Registrierungs-Editor die Änderung vornehmen zu lassen, klicken Sie im Fenster User Access Control. 
    
5. Wenn Sie aufgefordert werden, um den Vorgang fortzusetzen, klicken Sie auf **Ja**.
    
    Den Registrierungs-Editor zeigt eine Meldung, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.
  
## <a name="edit-registry-settings-to-re-enable-the-export-reports"></a>Bearbeiten der Einstellungen in der Registrierung können Sie die Export-Berichte wieder aktivieren

Wenn Sie die Berichte Results.csv und die Datei Manifest.xml deaktiviert haben, indem Sie die reg-Dateien in der vorherigen Prozedur erstellen, können Sie diese Dateien, um einen Bericht wieder zu aktivieren, damit sie mit den Suchergebnissen exportiert wird bearbeiten. Führen Sie das folgende Verfahren erneut aus, auf dem Computer, mit denen Sie die Ergebnisse einer Inhaltssuche exportiert werden.
  
1. Schließen Sie das Office 365 eDiscovery-Export-Tool aus, wenn es geöffnet ist.
    
2. Bearbeiten Sie eine oder beide der Bearbeiten reg-Dateien, die Sie im vorherigen Verfahren erstellt haben.
    
    - **Results.csv**
    
        Öffnen die Datei DisableResultsCsv.reg in Notepad ein, ändern Sie den Wert `False` , `True`, und speichern Sie die Datei. Angenommen, nachdem Sie die Datei bearbeiten, sieht es wie folgt:
    
        ```
        Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultCsvEnabled /t REG_SZ /d True
        ```

    - **"Manifest.xml"**
    
        Öffnen die Datei DisableManifestXml.reg in Notepad ein, ändern Sie den Wert `False` , `True`, und speichern Sie die Datei. Angenommen, nachdem Sie die Datei bearbeiten, sieht es wie folgt:
    
      ```
      Windows Registry Editor Version 5.00
      reg add HKLM\SOFTWARE\Microsoft\Exchange\Client\eDiscovery\ExportTool /v ResultEdrmEnabled /t REG_SZ /d True
      ```

3. Klicken Sie in Windows Explorer auf, oder doppelklicken Sie auf eine Registrierungsdatei, die Sie im vorherigen Schritt bearbeitet.
    
4. Klicken Sie auf **Ja,** um den Registrierungs-Editor die Änderung vornehmen zu lassen, klicken Sie im Fenster User Access Control. 
    
5. Wenn Sie aufgefordert werden, um den Vorgang fortzusetzen, klicken Sie auf **Ja**.
    
    Den Registrierungs-Editor zeigt eine Meldung, dass die Einstellung der Registrierung erfolgreich hinzugefügt wurde.
  
## <a name="frequently-asked-questions-about-disabling-export-reports"></a>Häufig gestellte Fragen zum Exportieren von Berichten deaktivieren
<a name="faqs"> </a>

 **Was sind die Results.csv und die Datei Manifest.xml Berichte?**
  
Die Results.csv und die Datei Manifest.xml-Dateien enthalten weitere Informationen über den Inhalt, der exportiert wurde.
  
- **Results.csv** eine Excel-Dokument, das Informationen über jedes Element enthält, die als Suchergebnis Download ist. Für e-Mails die, das Ergebnis-Protokoll enthält Informationen zu jeder Nachricht, einschließlich: 
    
  - Der Speicherort der Nachricht im Quellpostfach (einschließlich der Angabe, ob die Nachricht sich im primären oder im Archivpostfach befindet).
    
  - Das Datum, an dem die Nachricht gesendet oder empfangen wurde.
    
  - Die Betreffzeile der Nachricht.
    
  - Absender und Empfänger der Nachricht.
    
  - Gibt an, ob die Nachricht eine doppelte Nachricht ist, wenn Sie Deduplizierung aktiviert, wenn Sie die Suchergebnisse exportieren. Doppelte Nachrichten müssen einen Wert in der Spalte **Übergeordnete ItemId** , die die Nachricht als ein Duplikat identifiziert. Der Wert in der Spalte **Übergeordnete ItemId** ist identisch mit dem Wert in der Spalte **DocumentId Element** der Nachricht, die exportiert wurde. 
    
    Für Dokumente aus SharePoint und OneDrive for Business-Websites, das Ergebnis-Protokoll enthält Informationen zu den einzelnen Dokumenten, einschließlich:
    
  - Die URL für das Dokument.
    
  - Die URL für die Websitesammlung, in dem das Dokument gespeichert ist.
    
  - Das Datum, das das Dokument zuletzt geändert wurde.
    
  - Der Name des Dokuments (der in der Spalte Betreff im Protokoll Ergebnis befindet).
    
- **Manifest.XML** eine Manifestdatei (im XML-Format), die Informationen über jedes Element in den Suchergebnissen enthalten enthält. Die Informationen in diesem Bericht ist identisch mit dem Bericht Results.csv, aber er wird im Format angegeben durch den Verweis Modell EDRM (Electronic Discovery). Weitere Informationen zu EDRM, finden Sie unter [https://www.edrm.net](https://www.edrm.net).
    
 **Wann sollte ich Deaktivieren dieser Berichte exportieren?**
  
Es hängt Ihre Bedürfnisse. Viele Organisationen müssen keine zusätzlichen Informationen zu den Suchergebnissen, und diese Berichte ist nicht erforderlich.
  
 **Welche Computer müssen dazu auf werden?**
  
 Sie müssen die Einstellung in der Registrierung auf einem lokalen Computer zu ändern, die Sie für das Office 365 eDiscovery-Export-Tool ausführen. 
  
 **Nachdem ich diese Einstellung ändern, müssen ich einen Neustart des Computers?**
  
Nein, müssen Sie den Computer neu starten. Wenn das Office 365 eDiscovery-Export-Tool ausgeführt wird, das Ihnen jedoch zu schließen und dann neu starten, nachdem Sie die Einstellung der Registrierung ändern.
  
 **Bearbeitet ein bereits vorhandenen Registrierungsschlüssel abrufen, oder haben ein neues Schlüssels erstellt abrufen?**
  
Ein neuen Registrierungsschlüssel wird beim ersten erstellt, wenn Sie die REG-Datei ausführen, die Sie in den Verfahren in diesem Thema erstellt haben. Die Einstellung wird dann jedes Mal bearbeitet, Sie ändern, und führen Sie die REG-Datei bearbeiten erneut aus.
