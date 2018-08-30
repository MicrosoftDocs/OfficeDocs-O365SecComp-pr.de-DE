---
title: Anzeigen von Ergebnisse der Prozess-Modul in Office 365 erweiterte eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'Informationen Sie zu Updates für die Ergebnisse eines Moduls Prozess in Office 365 erweiterte eDiscovery, einschließlich Vorgangsstatus und zusammenfassende Prozess ausgeführt.  '
ms.openlocfilehash: 01093b0230aaf78ab7ccf1235f0874a0b69aa1bd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528866"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a>Anzeigen von Ergebnisse der Prozess-Modul in Office 365 erweiterte eDiscovery

Nach dem **Vorbereiten** \> **Prozess** wird initiiert, können Sie Status und die Ergebnisse anzeigen. 
  
> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="process-task-status"></a>Process Vorgangsstatus

Unter **Prepare** \> **Prozess** \> **Ergebnisse**, die auf der Seite wird der aktuelle Status (Wenn Prozess derzeit ausgeführt wird) oder den letzten Prozess Status Aufgabenstatus wie im folgenden Beispiel dargestellt.
  
![Prozessmodul-Aufgabenstatus](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
Die angezeigten Aufgaben variieren je nach den ausgewählten Optionen Prozess. 
  
- **Inventar**: Erweiterte eDiscovery durchlaufen und alle Dateien, die für den Vorgang ausgewählt und führt die grundlegenden Datensammlung.
    
- **Calculate-Signaturen**: die digitalen Signaturen MD5 berechnet.
    
- **Verbindung Extraction**: extrahiert innere oder enthaltenen Dateien rekursiv aus zusammengesetzter-Dateien (beispielsweise PST ZIP, MSG). Extrahierte Dateien werden im Ordner "Case" von der Groß-/Kleinschreibung gespeichert.
    
- **Synchronisieren von Datenbank**: interne Datenbank Prozess.
    
- **Kopieren von Dateien**: Kopien von Dateien. Für diese Aufgabe wird immer angezeigt, auch wenn die Option Dateien erweiterte Kopie ausgewählt ist.
    
- **Extraktion von Text**: systemeigene Dateien vorhanden sind, extrahiert erweiterte eDiscovery Text aus diesen Dateien DTSearch verwenden. Der extrahierte Text, der diese Dateien als Textdateien im Ordner "Case" gespeichert.
    
- **Aktualisieren von Metadaten**: die geladene Metadaten verarbeitet. 
    
- **Abschluss**: Interner, die Daten der schließt geladen Groß-/Kleinschreibung Dateien (beispielsweise identifizieren Fehler- und Erfolgsmeldungen-Dateien). 
    
Taskstatus: nach Abschluss des Tasks angezeigt. Während der Ausführung der Aufgaben, wird zur Dauer angezeigt.
  
> [!NOTE]
> Abgeschlossene Aufgaben umfassen möglicherweise auch Summen für Dateien, die Verarbeitung abgeschlossen oder Dateien mit Fehlern. 
  
> [!TIP]
> "Abbrechen" bietet die Rollbackoption halten Sie die Ausführung der Prozess und klicken Sie dann auf den vorherigen Data Populator Rollback oder verarbeitete Daten gespeichert. Rollback löscht alle verarbeitete Daten. Wenn Sie nicht möchten, dass die verarbeiteten Daten an (beispielsweise planen, diese Dateien erneut zu laden), wählen Sie die "Abbrechen" Option in diesem Fenster zu wählen, führen Sie ein Rollback nicht verloren gehen. 
  
## <a name="process-summary"></a>Prozesszusammenfassung

Unter Prepare \> Prozess \> Ergebnisse \> Process Zusammenfassung, wird eine Aufschlüsselung der geladene Dateiergebnisse entsprechend erfolgreiche Verarbeitung und Fehler Ergebnisse angezeigt.
  
Die Bereiche präsentieren grafisch dargestellt der importierten Dateistatistiken, wie folgt:
  
- **Zusammenfassung Prozess angesammelt**d: alle Dateien in die Groß-/Kleinschreibung.
    
- **Zusammenfassung zuletzt verarbeitet**: Dateien aus dem letzten Sitzung oder Aktion geladen. 
    
- **Letzte Familien**: Familie Informationen in die Groß-/Kleinschreibung (falls vorhanden).
    
- Wenn **Seed** Dateien hinzugefügt wurden, wird die Anzahl der Startwert Dateien pro Problem aufgeführt, die für die Dateien definiert wurde. 
    
    Wenn die Markierung von **Seed** Dateien ausgefallen ist, wird, die auch hingewiesen. 
    
- Wenn **vor dem markierte** Dateien hinzugefügt wurden, wird die Anzahl der Überprüfung vor dem markierten Dateien pro Problem aufgeführt, die für die Dateien definiert wurde. 
    
    Wenn das Markieren von Dateien **vor dem tagged** ausgefallen ist, ist, die auch darauf hingewiesen. 
    
![Zusammenfassung des Prozessmoduls](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a>Prozesszusammenfassung gesammelt und die letzte Diagramme

Die linke Balken umfasst, Quelle + extrahierten Dateien: also alle Dateien gefunden. 
  
Das Recht, verarbeitet, umfasst:
  
- Dateien mit Ladefehler
    
- Erfolgreich geladenen Dateien, unter anderem der folgenden: 
    
  - **Vorhandene**: Dateien, die geladen wurden, bevor und werden jetzt (einschließlich Duplikate) erneut geladen.
    
  - **Text**: eindeutige Dateien mit Text.
    
  - **Nicht-Text**: Textdateien, leere systemeigene Textdateien, nicht-Text-Dateien zu leeren. 
    
  - **Doppelte**s: Duplicate-Dateien mit Text.
    
## <a name="last-process-errors"></a>Letzte Prozess-Fehler

Unter Prepare \> Prozess \> Ergebnisse \> letzten Prozess Fehler, Details der Fehler in der letzten Sitzung oder ausgeführte Aktion angezeigt werden.
  
![Prozessmodulfehler](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Das Prozess-Modul ausgeführt, und Laden von Daten](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

