---
title: Festlegen von Analyseoptionen in Office 365 Advanced eDiscovery
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Lesen Sie die Schritte zum Einrichten von Optionen für den Analyseprozess in Office 365 Advanced eDiscovery, einschließlich near-Duplicates, e-Mail-Threads und Designs.  '
ms.openlocfilehash: 4689638f5cebe2ef17fcea5a13ff06edc29e5930
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260893"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a>Festlegen von Analyseoptionen in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Legen Sie in Advanced eDiscovery die Analyseoptionen vor dem Durchführen von ANALYZE fest.
  
## <a name="set-analyze-options"></a>Festlegen von Analyseoptionen

Öffnen **Sie \> Prepare analyze** \> **Setup**. Das folgende Fenster wird angezeigt.
  
![Festlegen von Analyseoptionen](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 **Near-Duplikate und e-Mail-Threads** Aktivieren Sie dieses Kontrollkästchen, wenn Sie die Analyse ausführen möchten. Sie ist standardmäßig ausgewählt. 
  
 **Dokument Ähnlichkeit** Geben Sie den Schwellenwert für Near-Duplicates ein, oder übernehmen Sie den Standard von 65%. 
  
 **Designs** Aktivieren Sie dieses Kontrollkästchen, um alle Dateien zu verarbeiten und Ihnen Designs zuzuweisen. Dieses Kontrollkästchen ist standardmäßig nicht aktiviert. Geben Sie die folgenden Optionen ein, wenn Sie die Bearbeitung von Designs durchführen möchten.
  
- **Maximale Anzahl von Designs** Geben Sie einen Wert für die Anzahl der zu erstellende Designs ein, oder wählen Sie ihn aus. Der Standardwert ist 200. 
    
    > [!NOTE]
    > Das Erhöhen der Anzahl von Designs wirkt sich auf die Leistung und die Möglichkeit, ein Design zu verallgemeinern. Je höher die Anzahl der Designs ist, desto detaillierter sind Sie. Wenn beispielsweise ein Satz von 50 Designs ein Design wie "Basketball, Spurs, Clippers, Lakers" enthält, 300 Designs können separate Designs aufweisen: "Spurs", "Clippers", "Lakers". Wenn Sie kein Bewusstsein für das Thema "Basketball" hatten und dieses Feature für ECA verwenden, könnte das Thema "Basketball" nützlich sein. Aber wenn die Verarbeitung zu viele Designs hatte, werden Sie möglicherweise nie das Wort "Basketball" sehen und wissen möglicherweise nicht, dass Spurs und Clippers gute Basketball Designs sind, anstatt Elemente, die auf Stiefel gehen und für Haare verwendet werden. 
  
- **Vorgeschlagene Designs** Sie können Design Wörter vorschlagen, um die Verarbeitung von Designs zu steuern. Advanced eDiscovery konzentriert sich auf diese vorgeschlagenen Wörter und versucht, ein oder mehrere relevante Designs basierend auf den Einstellungen für "maximale Anzahl von Designs" zu erstellen. 
    
    Wenn das vorgeschlagene Wort beispielsweise "Computer" lautet und Sie "2" als "maximale Anzahl von Designs" angegeben haben, versucht Advanced eDiscovery, zwei Designs zu generieren, die sich auf das Wort "Computer" beziehen. Die beiden Designs können beispielsweise "Computer Software" und "Computer Hardware" sein. 
    
    ![Vorgeschlagenes Design hinzufügen](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. Klicken Sie auf **ändern**, um vorgeschlagene Designs anzuzeigen, hinzuzufügen oder zu bearbeiten.
    
2. Klicken Sie im Bereich **vorgeschlagene Designs** auf das **** ![Symbol hinzufügen](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) Symbol hinzufügen, um ein Design hinzuzufügen. Fügen Sie im Bereich **vorgeschlagene Design hinzufügen** die Wörter durch Kommata getrennt hinzu. 
    
3. Wählen Sie unter **Anzahl der Designs**einen Wert aus, um die Anzahl der Designs zu ermitteln, die die erweiterte eDiscovery für diese Wörter generieren soll (standardmäßig 1 Design).
    
4. Klicken Sie auf **Speichern** , und schließen Sie dann den Dialog. 
    
    > [!NOTE]
    > Die Gesamtzahl der Designs enthält vorgeschlagene Designs. Die insgesamt vorgeschlagenen Designs dürfen die Gesamtdesigns nicht überschreiten. Wenn es viele vorgeschlagene Designs im Verhältnis zu den Gesamtdesigns gibt, werden nur einige "Roman"-Designs vom System erkannt, da die meisten der Designs für vorgeschlagene Designs vorgesehen sind. 
  
- **Modus** Wählen Sie in der Dropdownliste eine **Designs** -Option aus: 
    
  - **Modell erstellen und anwenden**: berechnet Designs anhand von Modellen aus einem Segment der Dateien und verteilt dann Dateien darunter.
    
  - **Modell erstellen**: berechnet ein Design Modell aus einem Segment der Dateien. Der Prozess der Aufteilung von Dateien erfolgt separat zu einem anderen Zeitpunkt.
    
  - **Modell anwenden**: diese Option wird nur angezeigt, wenn ein Modell zuvor erstellt und noch nicht angewendet wurde. Dadurch werden die Dateien basierend auf den Designs unterteilt.
    
Sie können auch [Text ignorieren festlegen](set-ignore-text-in-advanced-ediscovery.md) und [Erweiterte Einstellungen](set-analyze-advanced-settings-in-advanced-ediscovery.md) für analyze analysieren festlegen. 
  
Nachdem Sie diese Optionen festgelegt haben, klicken Sie auf **analyze** to Run. Die [Ansicht Analyseergebnisse](view-analyze-results-in-advanced-ediscovery.md) werden angezeigt. 
  
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Grundlegendes zur Dokument Ähnlichkeit](understand-document-similarity-in-advanced-ediscovery.md)
  
[Text ignorieren festlegen](set-ignore-text-in-advanced-ediscovery.md)
  
[Erweiterte Einstellungen für ANALYZE festlegen](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[Ergebnisse analysieren](view-analyze-results-in-advanced-ediscovery.md)

