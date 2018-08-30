---
title: Führen Sie das Modul Prozess und Laden von Daten in Office 365 erweiterte eDiscovery
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Hier erfahren Sie, wie Sie die Office 365-Sicherheit &amp; Compliance Center zu Office 365 erweiterte eDiscovery zugreifen, und führen Sie das Prozess-Modul für eine Anfrage.  '
ms.openlocfilehash: 32052bccc37d20c8707a1efb0592f7c93daf3590
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529462"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a>Führen Sie das Modul Prozess und Laden von Daten in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Abschnitt wird die Funktionalität des Moduls Prozess erweiterte eDiscovery. 
  
Zusätzlich zur Dateidaten kann in Metadaten wie Dateityp, Erweiterung, Standort oder Pfad, Erstellungsdatum und Uhrzeit, Autor, Verwaltungsberechtigter und Betreff, geladen werden erweiterte eDiscovery und für jeden Fall gespeichert. Einigen Metadaten, die wird beispielsweise von erweiterten eDiscovery berechnet, wenn systemeigene Dateien geladen werden. 
  
Erweiterte eDiscovery bietet System Metadatenwerte wie nahezu doppelte Gruppen oder Relevanz Bewertungen. Andere Metadaten wie der Datei Anmerkungen, kann vom Administrator hinzugefügt werden. 
  
## <a name="running-process"></a>Laufenden Prozess

> [!NOTE]
> Batch-Nummern werden in eine Datei während der Prozess zugewiesen, um die Überwachung der Dateien zu ermöglichen. Die Anzahl der Batch kann auch die Identifikation des Prozesses Batches für Anwendereingabe Optionen. Zusätzliche Filter stehen zum Filtern nach Batch Anzahl und Sitzungen zur Verfügung. 
  
Führen Sie die folgenden Schritte aus, um den Prozess ausgeführt werden.
  
1. [Öffnen Sie die Office 365-Sicherheit &amp; Compliance Center](go-to-the-securitycompliance-center.md) . 
    
2. Wechseln Sie zu **Suche &amp; Untersuchung** \> **eDiscovery** , und klicken Sie dann auf **Gehe zu erweiterten eDiscovery**.
    
3. Erweiterte eDiscovery wählen Sie die entsprechende Anfrage in der angezeigten Seite **Fällen** und dann auf **Gehe zu Fall**.
    
4. Unter **Prepare** \> **Prozess** \> **Setup**, wählen Sie eine Container aus der Liste der verfügbaren Container aus.
    
    ![Klicken Sie auf fortsetzen, um die Suchergebnisse die Groß-/Kleinschreibung hinzuzufügen](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. Klicken Sie auf **Erweiterte Einstellungen...** , wenn Sie den Container als Ausgangswert Dateien oder als vor dem markierten Dateien hinzufügen möchten. 
    
    Seed Dateien die Schulung für Probleme mit geringer Funktionsvielfalt beschleunigen verwenden (in der Regel 2 % oder weniger). Seed-Dateien, wird empfohlen, dass Sie wählen Sie eine Vielzahl von Messagingsysteme relevanten Dateien und zu verarbeiten 20 – 50 Basis pro Problem (zu viele Seed-Dateien können Relevanz Ergebnisse verzerren). Durch die gleiche Person, die das Problem Schulen wird, sollte SEED Dateien überprüft werden.
    
    Verwenden Sie vor dem markierte Dateien Relevanz Schulungen zu automatisieren. Sie sollten mindestens 1.500 Dateien, und beibehalten dem Anteil der-relevanten Dateien für die Überprüfung relevante genauso wie in der Auflistung, Relevanz hinzugefügt wurde. Diese Dateien manuell markiert werden soll, und Sie sollten sich die Qualität von Kategorien sicher sein.
    
    ![Screenshot der erweiterte Einstellungsseite für die Verarbeitung von Batchdateien](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - Im Abschnitt **Seed** : 
    
    Wählen Sie **als Ausgangswert Dateien markieren** markieren Sie den Container als Ausgangswert-Dateien. Sie müssen auch das **Problem** Dropdown-pro Problem zuweisen auswählen. Wählen Sie aus der Dropdownliste **Tag** **Relevant** oder **nicht relevant** . 
    
    > [!NOTE]
    > Nachdem Sie die Dateien als **Ausgangswert**festlegen, können nicht Sie sie als **vorab markierte**markieren. 
  
  - Im Abschnitt **vor dem markierten Dateien** : 
    
    Wählen Sie **als vorab markierte Dateien markieren** markieren Sie den Container als vor dem markierten Dateien. Sie müssen auch diese pro Problem in der **für Problem** Dropdown-Liste zuordnen. Wählen Sie aus der Dropdownliste **Tag** **Relevant** oder **nicht relevant** . 
    
    > [!NOTE]
    > Nachdem Sie Dateien als **markierte vor dem**festlegen, können nicht Sie sie als **Ausgangswert**markieren. 
  
  - Im Abschnitt **E-Mail zu markieren** . festlegen, welcher Teil einer verarbeiteten e-Mail sind, als Seed oder vor dem markierten markiert werden soll. 
    
6. Klicken Sie zunächst auf **Prozess**. Wenn abgeschlossen ist, werden die Prozess-Ergebnisse angezeigt.
    
7. (Optional) Wenn Sie ein bestimmtes Verwaltungsberechtigter Datenquellen zuweisen müssen, können Sie hinzufügen und bearbeiten Sie Verwaltungsberechtigter Namen in der **Verwalter** \> **Verwalten** und zuweisen Verwalter in **Verwalter** \> **zuweisen**. 
    
Wenn Sie die Groß-/Kleinschreibung hinzugefügt haben, können Sie dann erneut verarbeitet werden.
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Anzeigen von Ergebnissen der Prozess Modul](view-process-module-results-in-advanced-ediscovery.md)

