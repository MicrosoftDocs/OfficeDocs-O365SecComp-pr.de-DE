---
title: Anzeigen von Prozessmodulergebnissen in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c6f016cb-409f-4ae9-911c-1395cf0c86ea
description: 'Erfahren Sie, wie Sie die Ergebnisse eines Process-Moduls in Office 365 Advanced eDiscovery finden, einschließlich Vorgangsstatus und Prozesszusammenfassung.  '
ms.openlocfilehash: 0393cde78e559036d92b9ac48245afafc974a8b2
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218055"
---
# <a name="view-process-module-results-in-office-365-advanced-ediscovery"></a>Anzeigen von Prozessmodulergebnissen in Office 365 Advanced eDiscovery

Nachdem der **Vorbereitungs** \> **Prozess** eingeleitet wurde, können Sie den Fortschritt und die Ergebnisse anzeigen. 
  
> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
## <a name="process-task-status"></a>Prozess Vorgangsstatus

In **Prepare** \> **Process** \> **results**zeigt die Seite den aktuellen Status (falls Prozess derzeit ausgeführt wird) oder den Status Task der letzten Prozessstatus an, wie im folgenden Beispiel gezeigt.
  
![Prozessmodul-Aufgabenstatus](media/9430f9e7-a4dd-47c7-ac2e-2c6a60fc948b.png)
  
Die angezeigten Aufgaben können abhängig von den ausgewählten Prozessoptionen variieren. 
  
- **Inventory**: Advanced eDiscovery durchläuft alle für Process ausgewählten Dateien und führt grundlegende Datensammlung aus.
    
- **Signaturen berechnen**: berechnet die digitalen MD5-Signaturen.
    
- **Compounds Extraction**: extrahiert innere oder enthaltene Dateien rekursiv aus Verbunddateien (beispielsweise PST, ZIP, msg). Extrahierte Dateien werden im Case-Ordner des Falls gespeichert.
    
- **Synchronisieren der Datenbank**: interner Datenbankprozess.
    
- **Dateikopie**: kopiert Prozessdateien. Diese Aufgabe wird immer angezeigt, auch wenn die Option Erweiterte Kopiendateien ausgewählt ist.
    
- **Textextraktion**: Wenn systemeigene Dateien vorhanden sind, extrahiert Advanced eDiscovery Text aus diesen Dateien mithilfe von DTSearch. Der extrahierte Text dieser Dateien wird als Textdateien im Case-Ordner gespeichert.
    
- **Aktualisieren von Metadaten**: verarbeitet die geladenen Metadaten. 
    
- **Finalisieren**: interne Verarbeitung, die die Daten der geladenen Fall Dateien finalisiert (beispielsweise identifizieren von Fehler-und Erfolgs Dateien). 
    
Vorgangsstatus: wird nach Abschluss der Aufgabe angezeigt. Während Vorgänge ausgeführt werden, wird die Ausführungsdauer angezeigt.
  
> [!NOTE]
> Abgeschlossene Aufgaben können auch Gesamtsummen für Dateien sein, die die Verarbeitung abgeschlossen haben, oder Dateien mit Fehlern. 
  
> [!TIP]
> "Cancel" bietet eine Rollbackoption zum Beenden der Prozessausführung und zum erneuten Ausführen eines Rollbacks zur vorherigen Datenauffüllung oder zum Speichern der verarbeiteten Daten. Rollback löscht alle verarbeiteten Daten. Wenn Sie nicht möchten, dass die verarbeiteten Daten verloren gehen (beispielsweise möchten Sie diese Dateien erneut laden), wählen Sie die Option "Abbrechen" in diesem Fenster aus, um ein Rollback zu wählen. 
  
## <a name="process-summary"></a>Prozesszusammenfassung

In Prepare \> Process \> results \> Process Summary wird eine Aufteilung der Ergebnisse der geladenen Dateien entsprechend den Ergebnissen der erfolgreichen Dateiverarbeitung und des Fehlers angezeigt.
  
Die Bereiche enthalten eine grafische Darstellung der importierten Dateistatistiken wie folgt:
  
- **Process Summary akkumulieren**d: alle Dateien im Fall.
    
- **Prozesszusammenfassung**: Dateien, die aus der letzten Sitzung oder Aktion geladen wurden. 
    
- **Familien Last**: Family Information in dem Fall (falls vorhanden).
    
- Wenn **seeddateien** hinzugefügt wurden, wird die Anzahl der Seed-Dateien pro Problem aufgeführt, das für die Dateien definiert wurde. 
    
    Wenn die Markierung von **Seed** -Dateien fehlgeschlagen ist, wird ebenfalls darauf hingewiesen. 
    
- Wenn **** vordefinierte Dateien hinzugefügt wurden, wird die Anzahl der vorgetaggten Dateien pro Problem aufgeführt, das für die Dateien definiert wurde. 
    
    Wenn die Markierung von **** Dateien mit Vorzeichen fehlgeschlagen ist, wird ebenfalls darauf hingewiesen. 
    
![Zusammenfassung des Prozessmoduls](media/2086a691-9e3d-4117-beb2-a5c3a9a4cc94.png)
  
## <a name="process-summary-accumulated-and-last-charts"></a>Zusammenfassung Kumulierter und letzter Diagramme

Die linke Leiste enthält Quell-und extrahierte Dateien: alle gefundenen Dateien. 
  
Der Rechte Balken, verarbeitet, umfasst:
  
- Dateien mit Ladefehlern
    
- Erfolgreich geladene Dateien, die Folgendes aufweisen können: 
    
  - **Vorhanden**: Dateien, die zuvor geladen wurden und erneut geladen werden (einschließlich Duplikate).
    
  - **Text**: eindeutige Dateien mit Text.
    
  - **Nicht-Text**: leere Textdateien, leere systemeigene Textdateien, systemeigene nicht-Textdateien. 
    
  - **Duplikat**s: doppelte Dateien mit Text.
    
## <a name="last-process-errors"></a>Letzte Prozessfehler

In Prepare \> Process \> results \> werden beim letzten Prozessfehler Details zu den Fehlern in der letzten ausgeführten Sitzung oder Aktion angezeigt.
  
![Prozessmodulfehler](media/4771d0f4-4217-445a-9ba4-8b6541c5ad09.png)
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Prozessmodul wird ausgeführt und Daten geladen](run-the-process-module-and-load-data-in-advanced-ediscovery.md)

