---
title: Festlegen von Optionen für die Analyse in Office 365 erweiterte eDiscovery
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Überprüfen Sie die Schritte zum Einrichten von Optionen für die Analyse-Prozess in Office 365 erweiterte eDiscovery, einschließlich in Ihrer Nähe Duplikate, e-Mail-Threads und Designs.  '
ms.openlocfilehash: a0ebbadb180321a3094cb1056ed8e0e6500ee66a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529442"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a>Festlegen von Optionen für die Analyse in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Erweiterte eDiscovery legen Sie die Optionen Analyse vor dem Ausführen der Analyse.
  
## <a name="set-analyze-options"></a>Festlegen von Optionen für die Analyse

Open **Vorbereiten \> analysieren** \> **Setup**. Das folgende Fenster wird angezeigt.
  
![Analyseoptionen festlegen](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 **In Ihrer Nähe Duplikate und e-Mail-Threads** Aktivieren Kontrollkästchen Sie dieses, wenn Sie die Analyse ausführen möchten. Es ist standardmäßig aktiviert. 
  
 **Dokument Ähnlichkeit** Geben Sie den Schwellenwert Near-Duplikate, oder übernehmen Sie den Standardwert von 65 %. 
  
 **Designs** Kontrollkästchen Sie dieses, um alle Dateien zu verarbeiten und Designs zuweisen. Standardmäßig ist dieses Kontrollkästchen nicht aktiviert. Geben Sie die folgenden Optionen aus, wenn Sie Designs Verarbeitung ausführen möchten.
  
- **Maximale Anzahl von Designs** Geben Sie ein, oder wählen Sie einen Wert für die Anzahl der Designs zu erstellen. Der Standardwert ist 200. 
    
    > [!NOTE]
    > Erhöhung der Anzahl der Designs wirkt sich auf Leistung als auch die Möglichkeit eines Designs, verallgemeinern. Je höher die Anzahl der Designs, die eine genauere sind. Beispielsweise, wenn eine Reihe von 50 Designs ein Design wie "Basketball, beleben, geschoren Lakers" enthalten 300 Designs separate Designs enthalten können: "Beleben", "Geschoren", "Lakers". Wenn Sie keine zur Förderung des Bekanntheitsgrads des Designs "Basketball" hatte und verwenden Sie diese Funktion für ECA, konnte das Design anzeigen "Basketball" nützlich sein. Wenn die Verarbeitung zu viele Designs hatten, Sie jedoch möglicherweise noch nie das Wort "Basketball" angezeigt und können nicht kennen, beleben und geschoren gute Basketball Designs sind, um zu prüfen, anstatt Elemente, die auf startet und für haarstrich verwendet. 
  
- **Vorgeschlagene Designs** Sie können Designs Wörter zum Steuern der Verarbeitung Designs vorschlagen. Erweiterte eDiscovery wird den Schwerpunkt auf folgenden vorgeschlagenen Wörter und versuchen, eine oder mehrere relevante Designs, basierend auf der Einstellung "Maximale Anzahl der Designs" zu erstellen. 
    
    Beispielsweise wird das vorgeschlagene Wort "Computer", und Sie als die "maximale Anzahl der Designs" "2" angegeben, erweiterte eDiscovery versuchen, zwei Designs zu generieren, die sich auf das Wort "Computer" beziehen. Zwei Designs können beispielsweise "Computersoftware" und "Computerhardware" sein. 
    
    ![Vorgeschlagenes Design hinzufügen](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. Zum Anzeigen, hinzufügen oder Bearbeiten der vorgeschlagenen Designs, klicken Sie auf **Ändern**.
    
2. Klicken Sie auf **Hinzufügen**, in der Systemsteuerung **vorgeschlagene Designs** ![Symbol hinzufügen](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) Symbol, um ein Design hinzuzufügen. Fügen Sie in der Systemsteuerung **Hinzufügen vorgeschlagenen Design** Wörter durch Kommas getrennt. 
    
3. **Anzahl der Designs**wählen Sie einen Wert für die Anzahl der Designs zu bestimmen, die erweiterte eDiscovery versucht, diese Wörter generieren (der Standardwert ist 1 Design).
    
4. Klicken Sie auf **Speichern** , und schließen Sie das Dialogfeld. 
    
    > [!NOTE]
    > Die Gesamtzahl der Designs enthält vorgeschlagene Designs. Die gesamte vorgeschlagene Designs darf die gesamten Designs nicht überschreiten. Wenn viele vorgeschlagene Designs relativ zur Erstellung der gesamten Designs vorhanden sind, werden nur ein Paar "Roman" Designs, da die meisten der Designs vorgeschlagene Designs zugewiesen wird, werden vom System erkannt. 
  
- **Modus** Wählen Sie aus der Dropdownliste ein **Designs** -Option aus: 
    
  - **Erstellen und Anwenden von Modell**: berechnet Designs von Modellen aus einem Segment der Dateien und dann verteilt zwischen diesen Dateien.
    
  - **Create-Modell**: ein Designs-Modell aus einem Segment der Dateien berechnet. Der übernehmen Prozess der Division von Dateien ist separat zu einem späteren Zeitpunkt ausgeführt.
    
  - **Apply-Modell**: Diese Option wird nur angezeigt, wenn ein Modell wurde bereits zuvor erstellt und noch nicht angewendet. Dadurch werden die Dateien basierend auf der Designs dividiert.
    
Sie können auch [Set Text ignorieren](set-ignore-text-in-advanced-ediscovery.md) , und [Legen Sie Analyze Erweiterte Einstellungen](set-analyze-advanced-settings-in-advanced-ediscovery.md) für die Analyse. 
  
Nachdem Sie diese Optionen festgelegt haben, klicken Sie auf **Analyze** ausführen. [Analysieren der Ansicht Ergebnisse](view-analyze-results-in-advanced-ediscovery.md) werden angezeigt. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zu Dokument Ähnlichkeit](understand-document-similarity-in-advanced-ediscovery.md)
  
[Legen Sie Text ignorieren](set-ignore-text-in-advanced-ediscovery.md)
  
[Analysieren erweiterter Einstellungen festlegen](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Anzeigen von Ergebnisse der Analyse](view-analyze-results-in-advanced-ediscovery.md)

