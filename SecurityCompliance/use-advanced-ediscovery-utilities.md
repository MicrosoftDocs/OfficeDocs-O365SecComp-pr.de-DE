---
title: Verwenden Sie Office 365 erweiterte eDiscovery Hilfsprogramme
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Erfahren Sie mehr über die Dienstprogramme in Office 365 erweiterte eDiscovery, einschließlich Groß-/Kleinschreibung Anmeldung, Daten löschen, Fehler verarbeiten, Relevanz und Transparenz Analysis ändern.  '
ms.openlocfilehash: a68c98dd353971fcaa13fdc6b8e12bcf00c2faf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528934"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a>Verwenden Sie Office 365 erweiterte eDiscovery Hilfsprogramme

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Die Dienstprogramme, die angezeigt und in erweiterten eDiscovery verfügbar sind, hängt von Rollen Kontext und Benutzer.
  
## <a name="case-log"></a>Groß-/Kleinschreibung Protokoll

Groß-/Kleinschreibung Protokoll enthält eine ausführliche Liste der Anwendung Verarbeitungsaktivitäten, die für die Überwachung, Problembehandlung und zum Umgang mit Fehlern und Warnungen verwendet werden kann. Das Protokoll kann generiert und lokal auf dem Host oder Server gespeichert werden, oder direkt an eine e-Mail-Adresse gesendet.
  
Die Protokolldatei kann auch auf dem Clientcomputer heruntergeladen werden. Die Option zum Herunterladen Client kann aktiviert oder deaktiviert entsprechend der Konfiguration und der Rolle werden.
  
1. Klicken Sie in der Menüleiste auf das Symbol **Cogwheel** . 
    
2. In der **Einstellungen und Dienstprogramme \> Dienstprogramme** Registerkarte **Groß-/Kleinschreibung Log \> Setup**.
    
3. Wählen Sie die **Protokollebene** wie folgt: 
    
  - **Standard**: enthält die grundlegenden Protokolldaten. Diese Option ist in der Regel erforderlich für die Überwachung und sollte verwendet werden, es sei denn, andernfalls empfohlen.
    
  - **Minimale**: sehr große Umstände verwendet und gibt nur die neuesten Daten zurück.
    
4. Klicken Sie auf **Protokoll Fall ausführen**. Das Protokoll wird generiert und Pfad wird angezeigt. Die Aufgabe Fortschrittsinformationen für den aktuellen und dem letzten Vorgang wird im Aufgabenbereich Status angezeigt.
    
## <a name="clear-data"></a>Daten löschen

Wenn es erforderlich ist, löschen oder erneuten Initialisieren der Groß-/Kleinschreibung Daten, muss die Datenbankinstanz initialisiert werden. Das Dienstprogramm Daten löschen Löscht alle angegebenen Einträge aus der Datenbank der Groß-/Kleinschreibung, Textdateien, Groß-/Kleinschreibung Ordner und kumulierten Ergebnisse. Die Funktion kann nur von einem Administrator ausgeführt werden.
  
> [!IMPORTANT]
> Diese Aktion kann nicht rückgängig gemacht und löscht alle Kategorien Relevanz und Analysen, die von der Experte durchgeführt. Speichern Sie eine Sicherung der Daten, falls erforderlich. Verwenden Sie diese Option mit größter Vorsicht. Löschen von Dateien mit Tags und Rangfolge kann die Ergebnisse der Relevanz beeinträchtigen. 
  
1. Klicken Sie in der Menüleiste auf das Symbol **Cogwheel** . 
    
2. In der **Einstellungen und Dienstprogramme \> Dienstprogramme** Registerkarte **Daten löschen \> Setup**.
    
3. Wählen Sie eine Option für die Informationen nicht initialisiert werden:
    
  - **Relevanz**: Löscht alle Arbeit in Relevanz, einschließlich Definition Lasten und Zuordnung von Dateien und lädt. Es löscht alle Beispiele und Kategorien.
    
  - **In Ihrer Nähe Duplikate und e-Mail-Threads**: Löscht alle Analyseinformationen in Ihrer Nähe Duplikate und e-Mail-Threads.
    
  - **Designs**: Löscht Daten im Zusammenhang mit Designs.
    
  - **Historie exportieren**: Verlaufsinformationen der Export Batches löscht.
    
4. Klicken Sie auf **Daten löschen**. Die Groß-/Kleinschreibung Daten ist deaktiviert. Die Aufgabe Fortschrittsinformationen für den aktuellen und dem letzten Vorgang wird im Bereich **Aufgabenstatus** angezeigt. 
    
## <a name="modify-relevance"></a>Ändern der Relevanz

In diesem Abschnitt wird beschrieben, wie übersprungen oder Zurücksetzen einer Stichprobe Relevanz.
  
1. Klicken Sie in der Menüleiste auf das Symbol **Cogwheel** . 
    
2. In der **Einstellungen und Dienstprogramme \> Dienstprogramme** Registerkarte, wählen Sie **Relevanz ändern**.
    
3. Wählen Sie die Optionen aus: 
    
  - **Aktuelle Skip-Beispiel – für aktuellen Benutzer**: Dies wird markieren, als **Überspringen**, alle Dateien ohne Tags im open Groß-/Kleinschreibung Beispiel des Benutzers, der das Dienstprogramm. Verarbeitung der Relevanz wird nicht auf Dateien als **Überspringen**markierte ausgeführt werden.
    
  - **Für die aktuelle Skip - alle geöffneten Beispiele**: Dies wird markieren, als **Überspringen**, alle Dateien ohne Tags in allen geöffneten Beispiele für alle Benutzer. Diese Option wird nicht empfohlen, wenn der Benutzer derzeit Beispiele für Kategorien sind.
    
  - **Rollback der letzten Beispiel**: das letzte Relevanz Training-Beispiel ein Rollback wird, unabhängig davon, ob sie vor oder nach der "Berechnen" Prozess ist abgeschlossen. Rollback der hervorgehobene Beispiel ist nicht zulässig.
    
4. Klicken Sie auf **Execute** ausführen. 
    
## <a name="transparency-analysis"></a>Transparenz Analyse

Das Transparenz Analysis-Dienstprogramm ermöglicht eine detaillierte Ansicht der Dateien und dem zugeordneten Relevanz Faktor. Der Bericht kann als Überprüfung oder zum Vergleichen von eigenständigen der Relevanz einer Datei, die durch ein Prüfer im Vergleich zu der Relevanz von erweiterten eDiscovery zugewiesenen definiert verwendet werden. 
  
Zusätzlich zur Relevanz Faktoren erweiterte eDiscovery berechnet und weist Schlüsselwort Weights, die den Kontext Schlüsselwort berücksichtigen. Dasselbe Wort in einer Datei kann unterschiedliche Breiten, je nach Kontext und den Speicherort zugewiesen werden. Jedes Schlüsselwort ist eine zunehmende Skalierung der Farbintensität von Gelb bis hin zu dunkelorange und varying Graustufen mit gekennzeichnet. Farbe codieren wird verwendet, um visuell anzugeben, das Wort's relative positiven oder negativen Beitrag zum Ergebnis Relevanz. 
  
In einem Szenario mit mehreren Problem Groß-/Kleinschreibung kann ein Analysebericht Transparenz für jedes Problem generiert werden.
  
1. Klicken Sie in der Menüleiste auf das Symbol **Cogwheel** . 
    
2. In der **Einstellungen und Dienstprogramme \> Dienstprogramme** Registerkarte **Transparenz Analysis \> Setup**.
    
3. In ** Datei ID **, geben Sie die Datei-ID der Datei zu verarbeiten.
    
4. Wählen Sie in der Liste **Problem** das Problem relevant sind. 
    
5. Klicken Sie auf **Transparenz Analyse**. Nach Abschluss des Vorgangs wird die zeigt, wie die Schlüsselwortfarben im markierten die allgemeine Relevanz Bewertung entsprechen der Analysebericht Transparenz für die Datei angezeigt.
    
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Definieren von Groß-/Kleinschreibung und Mandanten-Einstellungen](define-case-and-tenant-settings-in-advanced-ediscovery.md)

