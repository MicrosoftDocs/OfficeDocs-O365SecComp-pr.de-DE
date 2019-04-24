---
title: Ausführen des Prozess Moduls und Laden von Daten in Office 365 Advanced eDiscovery
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
ms.assetid: c87bb0e5-301c-4d1d-958e-aabeb7990f44
description: 'Informationen zur Verwendung des Office 365 Security &amp; Compliance Center für den Zugriff auf Office 365 Advanced eDiscovery und zum Ausführen des Prozess Moduls für einen Fall.  '
ms.openlocfilehash: 95c73c034ed2ffa1c45f9aacd8463c497a842859
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261403"
---
# <a name="run-the-process-module-and-load-data-in-office-365-advanced-ediscovery"></a>Ausführen des Prozess Moduls und Laden von Daten in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Abschnitt wird die Funktionalität des erweiterten eDiscovery-Prozess Moduls beschrieben. 
  
Zusätzlich zu Dateidaten können Metadaten wie Dateityp, Erweiterung, Speicherort oder Pfad, Erstellungsdatum und-Uhrzeit, Autor, Depotbank und Betreff in Advanced eDiscovery geladen und für jeden Fall gespeichert werden. Einige Metadaten werden beispielsweise von Advanced eDiscovery berechnet, wenn systemeigene Dateien geladen werden. 
  
Erweiterte eDiscovery stellt System Metadatenwerte bereit, beispielsweise beinahe doppelt vorhandene Gruppierungen oder Relevanz-Ergebnisse. Andere Metadaten, wie etwa Datei Anmerkungen, können vom Administrator hinzugefügt werden. 
  
## <a name="running-process"></a>Ausgeführter Prozess

> [!NOTE]
> Batch Nummern werden während des Prozesses einer Datei zugewiesen, um die Nachverfolgung von Dateien zu ermöglichen. Die Chargennummer ermöglicht auch die Identifizierung von Prozess Batches für Wiederaufbereitungs Optionen. Für die Filterung nach Batch Nummern und Sitzungen stehen zusätzliche Filter zur Verfügung. 
  
Führen Sie die folgenden Schritte aus, um Process auszuführen.
  
1. [Öffnen Sie das Office 365 &amp; Security Compliance Center](go-to-the-securitycompliance-center.md) . 
    
2. Wechseln Sie **zur &amp; Such Untersuchung** \> **eDiscovery** , und klicken Sie dann auf **zur erweiterten eDiscovery**.
    
3. Wählen Sie in Erweiterte eDiscovery in der Seite angezeigte **Anfragen** den entsprechenden Fall aus, und klicken Sie auf **Gehe zu Groß-/Kleinschreibung**.
    
4. Wählen Sie unter **Prepare** \> **Process** \> **Setup**einen Container aus der Liste der verfügbaren Container aus.
    
    ![Klicken Sie auf Prozess, um die Suchergebnisse der Anfrage hinzuzufügen.](media/50bdc55c-d378-4881-b302-31ef785fa359.png)
  
5. Klicken Sie auf **Erweiterte Einstellungen...** , wenn Sie den Container als Seed-Dateien oder als vordefinierte Dateien hinzufügen möchten. 
    
    Verwenden Sie Seed-Dateien, um das Training bei Problemen mit geringem Reichtum (in der Regel 2% oder weniger) zu beschleunigen. Bei Seed-Dateien empfiehlt es sich, eine Vielzahl von deutlich relevanten Dateien auszuwählen und ungefähr 20-50 Samen pro Problem zu verarbeiten (zu viele seeddateien können Relevanz-Ergebnisse verzerren). Seed-Dateien sollten von derselben Person überprüft werden, die das Problem trainieren wird.
    
    Verwenden Sie vordefinierte Dateien, um die Relevanz-Schulung zu automatisieren. Sie sollten mindestens 1.500-Dateien markieren und den Anteil relevanter und nicht relevanter Dateien genauso wie in der Sammlung, die der Relevanz hinzugefügt wurde, beibehalten. Diese Dateien sollten manuell gekennzeichnet werden, und Sie sollten auf die Qualität der Markierung Vertrauen.
    
    ![Screenshot der Seite "Erweiterte Einstellungen" für die Verarbeitung von Batchdateien](media/3c25cb78-4484-41e5-bd34-3753c7ab6cf2.jpg)
  
  - Im Abschnitt **Seed** : 
    
    Wählen Sie **als Seed-Dateien markieren** aus, um den Container als Seed-Dateien zu kennzeichnen. Sie müssen Sie auch wählen, um Sie pro Problem aus der Dropdownliste **für Problem** zuzuweisen. Wählen Sie im Dropdown **** - **Tag** entweder **relevant** oder irrelevant aus. 
    
    > [!NOTE]
    > Nachdem Sie Dateien als Startwert festgelegt haben, können Sie Sie nicht als **Pre-Tagged**markieren. **** 
  
  - Im Abschnitt **Pre-Tagged files** : 
    
    Wählen Sie **als vordefinierte Dateien markieren** aus, um den Container als vorgetaggte Dateien zu markieren. Sie müssen Sie auch pro Problem aus der Dropdownliste **für Problem** zuweisen. Wählen Sie im Dropdown **** - **Tag** entweder **relevant** oder irrelevant aus. 
    
    > [!NOTE]
    > Nachdem Sie Dateien als vorDefinierte **Tags**festgelegt haben, können Sie **** Sie nicht als Startwert markieren. 
  
  - Im Abschnitt **e-Mail-Tagging** . Legen Sie fest, welcher Teil einer verarbeiteten e-Mail als Seed oder Pre-Tagged gekennzeichnet werden soll. 
    
6. Klicken Sie zunächst auf **Prozess**. Nach Abschluss des Vorgangs werden die Ergebnisse des Prozesses angezeigt.
    
7. Optional Wenn Sie einer bestimmten Depotbank Datenquellen zuweisen müssen, können Sie **** \> Depotnamen in Verwalter **Verwalten** und zuweisen, die Verwalter in **Verwalter** \> **zuweisen**. 
    
Wenn Sie den Fall hinzufügen, können Sie erneut verarbeiten.
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Anzeigen der Ergebnisse des Prozess Moduls](view-process-module-results-in-advanced-ediscovery.md)

