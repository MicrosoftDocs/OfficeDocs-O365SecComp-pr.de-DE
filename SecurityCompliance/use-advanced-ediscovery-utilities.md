---
title: Verwenden von Office 365 Advanced eDiscovery Utilities
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Erfahren Sie mehr über die Dienstprogramme in Office 365 Advanced eDiscovery, einschließlich Case Log, Clear Data, Process Errors, Modify Relevance und Transparency Analysis.  '
ms.openlocfilehash: bd100883804b300e77abcc8a2224cf1a59b53475
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265357"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a>Verwenden von Office 365 Advanced eDiscovery Utilities

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Die in Advanced eDiscovery angezeigten und verfügbaren Dienstprogramme hängen von Kontext-und Benutzerrollen ab.
  
## <a name="case-log"></a>Fallprotokoll

Das Fallprotokoll enthält eine detaillierte Liste der Anwendungs Verarbeitungsaktivitäten, die zum Nachverfolgen, zur Problembehandlung und zum Beheben von Fehlern und Warnungen verwendet werden können. Das Protokoll kann lokal auf dem Host oder Server generiert und gespeichert oder direkt an eine e-Mail-Adresse gesendet werden.
  
Die Protokolldatei kann auch auf den Clientcomputer heruntergeladen werden. Die Client Download Option kann gemäß der Konfiguration und der Benutzerrolle aktiviert oder deaktiviert werden.
  
1. Klicken Sie in der Menüleiste auf das **Zahnrad** Symbol. 
    
2. Wählen Sie auf der Registerkarte **Einstellungen und Dienstprogramme \> ** die Option ** \> Case Log Setup**aus.
    
3. Wählen Sie die **Protokollebene** wie folgt aus: 
    
  - **Standard**: enthält die grundlegenden Protokolldaten. Diese Option ist in der Regel für die Überwachung erforderlich und sollte verwendet werden, sofern nicht anders empfohlen.
    
  - **Minimal**: wird für sehr große Fälle verwendet und gibt nur die neuesten Daten zurück.
    
4. Klicken Sie auf **Fallprotokoll ausführen**. Das Protokoll wird generiert, und path wird angezeigt. Die Vorgangsfortschritts Informationen für den aktuellen und den letzten Vorgang werden im Bereich Vorgangsstatus angezeigt.
    
## <a name="clear-data"></a>Daten löschen

Wenn es erforderlich ist, Falldaten zu löschen oder neu zu initialisieren, muss die Datenbankinstanz initialisiert werden. Mit dem Dienstprogramm löschen werden alle angegebenen Einträge aus der falldatenbank, den Textdateien, dem Fallordner und den akkumulierten Ergebnissen gelöscht. Die Funktion kann nur von einem Administrator ausgeführt werden.
  
> [!IMPORTANT]
> Diese Aktion ist nicht umkehrbar und löscht alle Relevanz-Tagging und Analysen des Experten. Speichern Sie bei Bedarf eine Sicherung der Daten. Verwenden Sie diese Option mit äußerster Vorsicht. Das Löschen von gekennzeichneten und bewerteten Dateien kann sich auf die Relevanz auswirken. 
  
1. Klicken Sie in der Menüleiste auf das **Zahnrad** Symbol. 
    
2. Wählen Sie auf der Registerkarte **Einstellungen und Dienstprogramme \> ** die Option ** \> Daten Einrichtung löschen**aus.
    
3. Wählen Sie eine Option für die zu initialisierenden Informationen aus:
    
  - **Relevanz**: Löscht alle in Relevanz gemachten arbeiten, einschließlich der Definition von Lasten und der Zuordnung von Dateien zu Lasten. Es werden alle Beispiele und Markierungen gelöscht.
    
  - **Near-Duplikate und e-Mail-Threads**: Löscht alle Analyseinformationen von Near-Duplikaten und e-Mail-Threads.
    
  - **Designs**: löscht themenbezogene Daten.
    
  - **Export Verlauf**: Löscht Verlaufsinformationen zu Export Batches.
    
4. Klicken Sie auf **Daten löschen**. Die Falldaten werden gelöscht. Die Vorgangsfortschritts Informationen für den aktuellen und den letzten Vorgang werden im Bereich **Vorgangsstatus** angezeigt. 
    
## <a name="modify-relevance"></a>Relevanz ändern

In diesem Abschnitt wird beschrieben, wie Sie ein Relevanz-Beispiel überspringen oder zurücksetzen.
  
1. Klicken Sie in der Menüleiste auf das **Zahnrad** Symbol. 
    
2. Wählen Sie auf der Registerkarte **Einstellungen und Dienstprogramme \> ** die Option **Relevanz ändern**aus.
    
3. Wählen Sie eine der folgenden Optionen aus: 
    
  - **Aktuelle Beispiel überspringen-für aktuellen Benutzer**: Dieses Tag, als **Skip**, alle untagged-Dateien im Open Case-Beispiel des Benutzers, der das Hilfsprogramm ausführt. Die Relevanz-Verarbeitung wird nicht für Dateien ausgeführt, die als **Skip**gekennzeichnet sind.
    
  - **Aktuelle Sample-alle geöffneten Samples überspringen**: Dieses Tag, als **Skip**, alle nicht markierten Dateien in allen geöffneten Beispielen für alle Benutzer. Diese Option wird nicht empfohlen, wenn Benutzer derzeit Beispiele markieren.
    
  - **Letztes Beispiel zurück**setzen: das Beispiel für die letzte abgeschlossene Relevanz wird zurückgesetzt, unabhängig davon, ob es vor oder nach dem Prozess "berechnen" vorliegt. Das Rollback eines catch-up-Beispiels ist nicht zulässig.
    
4. Klicken **** Sie auf Ausführen, um auszuführen. 
    
## <a name="transparency-analysis"></a>Transparenz Analyse

Das Dienstprogramm für die Transparenz Analyse ermöglicht eine detaillierte Ansicht der Dateien und ihre zugewiesene Relevanz. Der Bericht kann als Plausibilitätsprüfung oder zum Vergleichen der Relevanz einer von einem menschlichen Prüfer definierten Datei im Vergleich zu der Relevanz verwendet werden, die von Advanced eDiscovery zugewiesen wurde. 
  
Zusätzlich zu den Relevanz-Bewertungen berechnet und weist Advanced eDiscovery Schlüsselwort Gewichte auf, die den Stichwort Kontext berücksichtigen. Das gleiche Wort in einer Datei kann je nach Kontext und Speicherort mit unterschiedlichen gewichten versehen werden. Jedes Schlüsselwort wird mit einer zunehmenden Farbintensität von gelb bis dunkel Orange und unterschiedlichen Grautönen gekennzeichnet. Die Farbcodierung wird verwendet, um den relativen positiven oder negativen Beitrag des Wortes zum Relevanzwert visuell anzuzeigen. 
  
In einem Szenario mit mehreren Problemen kann für jedes Problem ein Bericht zur Transparenz Analyse generiert werden.
  
1. Klicken Sie in der Menüleiste auf das **Zahnrad** Symbol. 
    
2. Wählen Sie auf der Registerkarte **Einstellungen und Dienstprogramme \> ** die Option ** \> Transparenz analyseeinrichtung**aus.
    
3. Geben Sie in * * Datei-ID * * die Datei-ID der zu verarbeitenden Datei ein.
    
4. Wählen Sie in der Liste **Problem** das entsprechende Problem aus. 
    
5. Klicken Sie auf **Transparenz Analyse**. Nach Abschluss des Vorgangs wird der Bericht zur Transparenz Analyse für die Datei angezeigt, der zeigt, wie die markierten Schlüsselwortfarben mit dem Gesamtergebnis der Relevanz korrelieren.
    
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Definieren von Fall-und Mandanten Einstellungen](define-case-and-tenant-settings-in-advanced-ediscovery.md)

