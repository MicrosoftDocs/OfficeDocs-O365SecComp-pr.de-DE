---
title: Verwenden der Express-Analyse in Office 365 Advanced eDiscovery
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Informationen zum Ausführen des Express Analysemodus von Office 365 Advanced eDiscovery
ms.openlocfilehash: d8457587c9c1a1237ddc076ce803a46382a04ed8
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "31000958"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a>Verwenden der Express-Analyse in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Sie können die **Express Analyse** verwenden, um einen Fall schnell zu analysieren und die Ergebnisse zu exportieren. 
  
Sie können die Expressanalyse verwenden, um beinahe-Duplikate und e-Mail-Threads zu berechnen und Designs zu berechnen. Sie können auch bestimmte Parameter für Designs, die Dokument Ähnlichkeit und die Exportdateien in den [erweiterten Einstellungen für die Express Analyse](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings)festlegen.
  
## <a name="run-express-analysis"></a>Ausführen der Express Analyse

1. Wählen Sie auf der Registerkarte **Express Analyse** (1) einen Container aus, um die Schaltflächen * * Expressanalyse * * (2) und **Erweiterte Einstellungen** zu aktivieren. 
    
    ![Screenshot der Seite für die Express Analyse](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. Unter **analyze Parameters**:
    
  - Aktivieren Sie die Option **near-Duplikate und e-Mail-Threads berechnen** , wenn Sie die Analyse ausführen möchten. Sie ist standardmäßig ausgewählt. 
    
  - Aktivieren Sie die Option **Designs berechnen** , um alle Dateien zu verarbeiten, und weisen Sie Ihnen Designs zu. Sie ist standardmäßig ausgewählt. 
    
3. Unter **Export Ziel**:
    
  - Aktivieren Sie das Kontrollkästchen auf **lokalen Computer herunter** laden, um es auf Ihren lokalen Computern herunterzuladen. 
    
  - Wenn Sie **den Export in ein benutzerdefiniertEs Azure-BLOB aktivieren,** können Sie auch eine Container-URL und ein SAS-Token angeben. 
    
    > [!NOTE]
    > Nachdem ein Exportpaket im benutzerdefinierten Azure-BLOB gespeichert wurde, werden die Daten nicht mehr von Advanced eDiscovery verwaltet. Sie wird vom Azure-BLOB verwaltet. Wenn Sie also den Fall löschen, verbleiben die exportierten Dateien weiterhin im Azure-BLOB. 
  
  - **SAS-Token für zukünftige Export Sitzung speichern**: Wenn diese Option aktiviert ist, wird das SAS-Token in der internen Datenbank von Advanced eDiscovery für zukünftige Verwendung verschlüsselt.
    
    > [!NOTE]
    > Derzeit läuft das SAS-Token nach einem Monat ab. Wenn Sie versuchen, nach mehr als einem Monat herunterzuladen, müssen Sie die letzte Sitzung rückgängig machen und dann erneut exportieren. 
  
4. Um die Expressanalyse mit den Standardeinstellungen zu starten, wählen Sie **Expressanalyse**und die Seite **Vorgangsstatus** wird angezeigt. 
    
    Auf der Seite **Vorgangsstatus** können Sie die Registerkarten **Prozess**, **Analyse** und **Export** erweitern, um Details zum Express-Durchlauf anzuzeigen. 
    
    ![Screenshot der erweiterten eDiscovery Express Analysis-Aufgabenstatus Seite](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. Wählen Sie die Zusammenfassungsseite für **Express Analysen** aus, um detaillierte Informationen zur Ausführung aufzulisten. 
    
    Klicken Sie unten auf der Zusammenfassungsseite der **Express Analyse** auf **letzte Sitzung herunterladen** , um die Analysedateien auf dem lokalen Computer herunterzuladen. Sie müssen zunächst das eDiscovery-Export Tool herunterladen und den Exportschlüssel in das eDiscovery-Export Tool einfügen. 
    
## <a name="advanced-settings-for-express-analysis"></a>Erweiterte Einstellungen für die Express Analyse
<a name="BK_AdvancedSettings"> </a>

Optional können Sie **Erweiterte Einstellungen** festlegen, um die standardmäßigen Express Analyseparameter zu ändern. 
  
1. Im Abschnitt **analysieren** : 
    
  - Geben Sie im Feld **near Duplicates and Email**den Wert für die **Dokument Ähnlichkeit** ein, oder übernehmen Sie die Standardeinstellung von 65%. 
    
  - Geben Sie in die **Maximale Anzahl von Designs** ein, oder wählen Sie einen Wert für die Anzahl der zu erstellende Designs aus. Der Standardwert ist 200. 
    
    > [!NOTE]
    > Das Erhöhen der Anzahl von Designs wirkt sich auf die Leistung und die Möglichkeit, ein Design zu verallgemeinern. Je höher die Anzahl der Designs ist, desto detaillierter sind Sie. Wenn beispielsweise ein Satz von 50 Designs ein Design wie "Basketball, Spurs, Clippers, Lakers" enthält, 300 Designs können separate Designs aufweisen: "Spurs", "Clippers", "Lakers". Wenn Sie kein Bewusstsein für das Thema "Basketball" hatten und dieses Feature für ECA verwenden, könnte das Thema "Basketball" nützlich sein. Aber wenn die Verarbeitung zu viele Designs hatte, werden Sie möglicherweise nie das Wort "Basketball" sehen und wissen möglicherweise nicht, dass Spurs und Clippers gute Basketball Designs sind, anstatt Elemente, die auf Stiefel gehen und für Haare verwendet werden. 
  
  - Wählen Sie in den **vorgeschlagenen Designs** **ändern** , um Design Wörter zur Steuerung der Verarbeitung von Designs zu vorschlagen. Advanced eDiscovery konzentriert sich auf diese vorgeschlagenen Wörter und versucht, ein oder mehrere relevante Designs basierend auf den Einstellungen für "maximale Anzahl von Designs" zu erstellen. 
    
    Wenn das vorgeschlagene Wort beispielsweise "Computer" lautet und Sie "2" als "maximale Anzahl von Designs" angegeben haben, versucht Advanced eDiscovery, zwei Designs zu generieren, die sich auf das Wort "Computer" beziehen. Die beiden Designs können beispielsweise "Computer Software" und "Computer Hardware" sein.
    
    ![Vorgeschlagenes Design hinzufügen](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - **Modus** Wählen Sie in der Dropdownliste eine **Designs** -Option aus: 
    
  - **Modell erstellen und anwenden**: berechnet Designs anhand von Modellen aus einem Segment der Dateien und verteilt dann Dateien darunter.
    
  - **Modell erstellen**: berechnet ein Design Modell aus einem Segment der Dateien. Der Prozess der Aufteilung von Dateien erfolgt separat zu einem anderen Zeitpunkt.
    
  - **Modell anwenden**: diese Option wird nur angezeigt, wenn ein Modell zuvor erstellt und noch nicht angewendet wurde. Dadurch werden die Dateien basierend auf den Designs unterteilt.
    
2. Im Abschnitt **exportieren** : 
    
1. **Wählen Sie im Export Batch auswählen**:
    
  - Wählen Sie in der Liste **Export Batch** den Namen des Batches aus, oder exportieren Sie die Ergebnisse, um den Batch 01 zu exportieren (Standard Batch). 
    
  - Wenn Sie Ergebnisse für neue Dateien exportieren möchten, die Sie einem vorhandenen Fall hinzugefügt haben, fahren Sie mit dem aktuellen Batch fort. Um eine Sitzung im Batch zu erstellen, wählen Sie dieselbe Batchnummer aus, und klicken Sie auf **Export Sitzung erstellen** mit dieser Option können Sie die gleichen Parameter wie im vorherigen Batch inkrementell exportieren. 
    
  - Um in einen neuen Batch zu exportieren, klicken Sie auf](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) hinzufügen Symbol **Hinzufügen** ![, und geben Sie einen neuen Namen in den **batchnamen** ein (oder übernehmen Sie den Standardwert) und eine Beschreibung in der **Batch Beschreibung**. Klicken Sie auf **OK**.
    
  - Wenn Sie einen batchnamen oder eine Beschreibung bearbeiten möchten, wählen Sie den Namen unter **Export Batch**aus](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), klicken Sie auf Bearbeitungssymbol **Bearbeiten** ![, und ändern Sie dann die Felder.
    
    > [!NOTE]
    > Nachdem Sie Sitzungen für einen Export Batch ausgeführt haben, können diese nicht gelöscht werden. Darüber hinaus können nur einige Parameter bearbeitet werden, nachdem die erste Sitzung ausgeführt wurde. 
  
  - Wenn Sie einen doppelten Export Batch erstellen möchten, wählen Sie **Duplicate** ![Export Batch Create a Duplicate](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) Export Batch Icon aus, und geben Sie im Bereich einen Namen und eine Beschreibung für den doppelten Batch ein. 
    
  - Wenn Sie einen Export Batch löschen möchten **** ![, klicken Sie auf Löschen eines](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)Export Batch-Symbols.
    
  - Um den Verlauf eines Batches anzuzeigen, wählen **** ![Sie Verlaufs Symbol](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)für den Stapelverarbeitungs Verlauf.
    
2. Klicken Sie unter define p **Bevölkerung:** wählen Sie **nur Dateien über Relevanz Cut-Off** und/oder **Export Batch verfeinern** , wenn Sie die Einstellungen für Ihren Export Batch optimieren möchten. Wenn Sie **nur Dateien über Relevanz Cut-Off-Wert einbeziehen**auswählen, wird das **Problem** aktiviert, und wenn die Relevanz der Datei höher ist als die Cut-Off-Bewertung für das ausgewählte Problem, wird die Datei exportiert. Die Datei wird exportiert, es sei denn, Sie wird durch den Filter ' **for Review** ' ausgeschlossen. Wenn Sie **Export Batch verfeinern**auswählen, werden die Optionsfelder **de-dupe** und **Filter by Review** aktiviert. Wenn Sie die **** Deduplizierung auswählen, werden die Duplikatdateien entsprechend der definierten Richtlinie gefiltert: [Case Level (Standard): aus allen doppelten Dateien im gesamten Fall werden nur eine Datei debetrogen. Depot Ebene: aus jeder Gruppe von doppelten Dateien desselben Depotbank wird eine Datei mit bis zu einer Deduplizierung entfernt. Ein Datensatz aller doppelten Dateien ist in der Exportausgabe verfügbar. Wenn Sie **Filtern nach ' zur Überarbeitung '** wählen, wählen Sie **unter Metadaten ändern** , um die Feld Einstellungen **für die Überprüfungen**einzugeben. Wählen Sie **Eingabedateien einfügen**aus, um Quelldateien in den Paketinhalt einzubeziehen. Sie können diese Option deaktivieren, um den Exportvorgang zu beschleunigen. Beachten Sie, dass die systemeigenen Dateien in jedem Fall exportiert werden.
    
3. Wählen Sie unter **Metadaten definieren**aus den folgenden Optionen in der Liste **Export Vorlage** (einmal pro Sitzung) aus. 
    
  - **Standard**: grundlegende Gruppe von Datenelementen, Metadaten und Eigenschaften. Verwenden Sie diese Option, wenn Importdaten bereits in Advanced eDiscovery verarbeitet wurden und Exportdaten in ein System hochgeladen werden, in dem die Dateien bereits enthalten sind. Standardmäßig werden Spalten für das Exportieren von Vorlagen erstellt und ausgefüllt.
    
  - **All**: vollständiger Satz von Standardmetadaten einschließlich aller verarbeitungsDaten sowie Analyse-und Relevanzwerte. Diese Vorlage ist erforderlich, wenn Advanced eDiscovery die Verarbeitung ausführt und Dateidaten zum ersten Mal auf ein externes System hochgeladen werden.
    
  - **Probleme**: Wählen Sie **alle Probleme** aus, oder wählen Sie ein bestimmtes Problem aus, das Sie erstellt haben. 
    
Klicken Sie auf **OK**, um die erweiterten Einstellungen zu speichern, die Standardwerte **wiederherzustellen** , oder **Abbrechen** , um die Einstellung der erweiterten Einstellungen abzubrechen. 
  
## <a name="see-also"></a>Siehe auch
<a name="BK_AdvancedSettings"> </a>

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)

