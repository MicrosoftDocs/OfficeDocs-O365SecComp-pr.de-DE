---
title: Verwenden Sie Analyse Express in Office 365 erweiterte eDiscovery
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
ms.assetid: 50580099-3dc0-44a1-a9b6-5ca6d396316b
description: Erfahren Sie, wie den Modus Express Analyse der Office 365 erweiterte eDiscovery ausführen
ms.openlocfilehash: a71e6775b1116e805e455815dca53a727d887809
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529315"
---
# <a name="use-express-analysis-in-office-365-advanced-ediscovery"></a>Verwenden Sie Analyse Express in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
Sie können **Express Analysis** Sie schnell eine Anfrage zu analysieren und Exportieren der Ergebnisse. 
  
Express-Analyse können Sie in der Nähe Duplikate berechnen und e-Mail-Threads und Designs zu berechnen. Sie können auch bestimmte Parameter für Designs, Dokument Ähnlichkeit und das Exportieren von Dateien in den [erweiterten Einstellungen für die Analyse Express](use-express-analysis-in-advanced-ediscovery.md#BK_AdvancedSettings)festlegen.
  
## <a name="run-express-analysis"></a>Führen Sie Express-Analyse

1. In der Registerkarte **Analyse Express** (1) Wählen Sie einen Container Aktivieren der ** Express Analysis ** (2), und Schaltflächen **Erweiterte Einstellungen** . 
    
    ![Screenshot der Seite Analysis Express](media/60009974-5d1f-4971-8ebe-e5ec74e7fd2a.jpg)
  
2. Klicken Sie unter **Parameter analysieren**:
    
  - Überprüfen Sie **in Ihrer Nähe Duplikate zu berechnen und e-Mail-Threads** , wenn Sie die Analyse ausführen möchten. Es ist standardmäßig aktiviert. 
    
  - Überprüfen Sie **Berechnen Designs** zur Verarbeitung aller Dateien und Designs zuweisen. Es ist standardmäßig aktiviert. 
    
3. Klicken Sie unter **Ziel für das Exportieren**:
    
  - Überprüfen Sie **auf dem lokalen Computer herunterladen** , auf dem lokalen Computer herunterzuladen. 
    
  - Wenn Sie den **Export in Azure Blob benutzerdefinierte** aktivieren können Sie auch ein Container-URL und SAS-Token angeben. 
    
    > [!NOTE]
    > Sobald ein Exportpaket zu gespeichert wurde die benutzerdefinierten Azure Blob, die Daten nicht mehr vom erweiterte eDiscovery verwaltet werden. Es wird von den Azure Blob verwaltet. Dies bedeutet, wenn Sie die Groß-/Kleinschreibung löschen, die exportierten Dateien weiterhin auf die Azure Blob verbleibt. 
  
  - **Token für zukünftige Export-Sitzung speichern SAS**: Wenn diese Einstellung aktiviert, wird das SAS-Token in der erweiterten eDiscovery interne Datenbank für die zukünftige Verwendung verschlüsselt werden.
    
    > [!NOTE]
    > Derzeit läuft ab das Token SAS nach Monat. Wenn Sie versuchen, die nach mehr als einem Monat herunterladen Sie die letzten Sitzung rückgängig zu machen müssen, exportieren Sie dann erneut. 
  
4. Die express Analyse mit Default starten zu Einstellungen, wählen Sie **Express Analyse**und die Seite **Aufgabenstatus** wird angezeigt. 
    
    Klicken Sie auf der Seite **Aufgabenstatus** können Sie die **Prozess**, **Analysieren** und **Exportieren von** Registerkarten zum Anzeigen von Details zu den express ausführen erweitern. 
    
    ![Screenshot der erweiterte eDiscovery Express Analysis Aufgabe Statusseite](media/bf30ab02-9828-4a6d-a485-0babc2c49ae5.jpg)
  
5. Wählen Sie die Seite **Zusammenfassung Analysis Express** detaillierte Informationen über die Ausführung aufgelistet. 
    
    Am unteren Rand der Seite **Zusammenfassung Analysis Express** wählen Sie in der **letzten Sitzung herunterladen** , dem Analyse Dateien Tp Ihrem lokalen Computer herunterladen. Sie müssen zuerst herunterladen eDiscovery-Export-Tool, und fügen Sie die Export-Taste, um das eDiscovery-Export-Tool. 
    
## <a name="advanced-settings-for-express-analysis"></a>Erweiterte Einstellungen für die Analyse Express
<a name="BK_AdvancedSettings"> </a>

Sie können **Erweiterte Einstellungen** , so ändern Sie die Express-Analyse Standardparametern optional festlegen. 
  
1. Im Abschnitt **Analysieren** : 
    
  - Geben Sie in der **in der Nähe von Duplikaten und e-Mail-Threads**den Wert **Dokument Ähnlichkeit** oder übernehmen Sie den Standardwert von 65 %. 
    
  - Die **maximale Anzahl von Designs** Geben Sie, oder wählen Sie einen Wert für die Anzahl der Designs zu erstellen. Der Standardwert ist 200. 
    
    > [!NOTE]
    > Erhöhung der Anzahl der Designs wirkt sich auf Leistung als auch die Möglichkeit eines Designs, verallgemeinern. Je höher die Anzahl der Designs, die eine genauere sind. Beispielsweise, wenn eine Reihe von 50 Designs ein Design wie "Basketball, beleben, geschoren Lakers" enthalten 300 Designs separate Designs enthalten können: "Beleben", "Geschoren", "Lakers". Wenn Sie keine zur Förderung des Bekanntheitsgrads des Designs "Basketball" hatte und verwenden Sie diese Funktion für ECA, konnte das Design anzeigen "Basketball" nützlich sein. Wenn die Verarbeitung zu viele Designs hatten, Sie jedoch möglicherweise noch nie das Wort "Basketball" angezeigt und können nicht kennen, beleben und geschoren gute Basketball Designs sind, um zu prüfen, anstatt Elemente, die auf startet und für haarstrich verwendet. 
  
  - Wählen Sie in der **vorgeschlagene Designs** **Ändern** zum Vorschlagen des Designs Wörter zum Steuern der Verarbeitung Designs aus. Erweiterte eDiscovery wird den Schwerpunkt auf folgenden vorgeschlagenen Wörter und versuchen, eine oder mehrere relevante Designs, basierend auf der Einstellung "Maximale Anzahl der Designs" zu erstellen. 
    
    Beispielsweise wird das vorgeschlagene Wort "Computer", und Sie als die "maximale Anzahl der Designs" "2" angegeben, erweiterte eDiscovery versuchen, zwei Designs zu generieren, die sich auf das Wort "Computer" beziehen. Zwei Designs können beispielsweise "Computersoftware" und "Computerhardware" sein.
    
    ![Vorgeschlagenes Design hinzufügen](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
  - **Modus** Wählen Sie aus der Dropdownliste ein **Designs** -Option aus: 
    
  - **Erstellen und Anwenden von Modell**: berechnet Designs von Modellen aus einem Segment der Dateien und dann verteilt zwischen diesen Dateien.
    
  - **Create-Modell**: ein Designs-Modell aus einem Segment der Dateien berechnet. Der übernehmen Prozess der Division von Dateien ist separat zu einem späteren Zeitpunkt ausgeführt.
    
  - **Apply-Modell**: Diese Option wird nur angezeigt, wenn ein Modell wurde bereits zuvor erstellt und noch nicht angewendet. Dadurch werden die Dateien basierend auf der Designs dividiert.
    
2. Im Abschnitt **Exportieren** : 
    
1. In den **Batch wählen Sie exportieren**:
    
  - Aus der Liste **Exportieren Batch** wählen den Blattnamen oder Exportieren von Ergebnissen in Export Batch 01 (Standard). 
    
  - Um Ergebnisse für neue Dateien zu exportieren, die Sie einer vorhandenen Anfrage hinzugefügt haben, fahren Sie mit Ihren aktuellen Stapel. Zum Erstellen einer Sitzung im Batch, wählen Sie die gleiche Anzahl von Batch aus, und klicken Sie auf **Create Session exportieren** können Sie diese Option verwenden, so exportieren Sie die gleichen Parameter als den vorherigen Batch eine inkrementelle Weise. 
    
  - Klicken Sie auf **Hinzufügen**, um einen neuen Batch zu exportieren,![Symbol hinzufügen](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) und geben Sie einen neuen Namen in **Blattname** (oder übernehmen Sie den Standardwert) und eine Beschreibung im **Feld Beschreibung Batch**. Klicken Sie auf **OK**.
    
  - Um einen Namen oder die Beschreibung zu bearbeiten, wählen Sie den Namen im **Batch exportieren**, klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), und klicken Sie dann die Felder zu ändern.
    
    > [!NOTE]
    > Nach dem Ausführen Sitzungen für einen Batch Export können sie gelöscht werden. Darüber hinaus können nur einige Parameter bearbeitet werden, sobald die erste Sitzung ausgeführt wird. 
  
  - Wählen Sie zum Erstellen eines Batches für die doppelte Export **Duplikat Export Batch**![doppelte Export Batch-Symbol erstellen](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) , und geben Sie einen Namen und eine Beschreibung für den doppelten Batch in der Systemsteuerung. 
    
  - Wählen Sie zum Löschen eines Batches Export **Löschen**![löschen Symbolgröße Batch Export](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).
    
  - Wählen Sie zum Anzeigen des Verlaufs eines Batches **Batch Verlauf**![Ansicht Verlauf Symbol](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).
    
2. Klicken Sie unter Define p **Opulation:** **Includedateien nur über Relevanz Grenzwert Score** und/oder **verfeinern Export Batch** wählen, wenn Sie die Einstellungen für Ihren Export-Stapel optimieren möchten. Wenn Sie **nur Dateien über Relevanz Grenzwert Score einschließen**ausgewählt haben, klicken Sie dann das **Problem** ist aktiviert, und wenn die Datei Relevanz Score höher ist als die Bewertung Grenzwert für das ausgewählte Problem ist, klicken Sie dann die Datei wird exportiert. Die Datei exportiert werden, es sei denn, es von ausgeschlossen ist die ' **zur Prüfung** Filter. Bei Auswahl von **verfeinern Export Batch**, und klicken Sie dann die **Deduplizierung** und **Filter von 'Zur Überprüfung' Feld** Optionsfelder aktiviert sind. Falls gewünscht **Deduplizierung**, und klicken Sie dann Duplikate Dateien gefiltert gemäß der Richtlinie definierten skalierten werden werden: [Case-Ebene (Standard): aus jeder Gruppe von duplizierten Dateien in der gesamten Groß-/Kleinschreibung, alle jedoch eine Datei Aufhebung der duped werden soll. Verwaltungsberechtigter Ebene: aus jeder Gruppe von duplizierten Dateien von der gleichen Verwaltungsberechtigte, alle jedoch eine Datei Aufhebung der duped werden soll. Eine Aufzeichnung aller duplizierten Dateien ist Export Ausgabe verfügbar. Wenn Sie **von 'zur Prüfung"** Filterfeld auswählen, wählen Sie **ändern unter Metadaten** Geben Sie Ihre Einstellungen **'zur Prüfung"** dar. Wählen Sie **input Includedateien**Quelldateien im Paketinhalt enthalten. Deaktivieren Sie diese Option, um den Exportvorgang zu beschleunigen. Beachten Sie, dass die systemeigenen Dateien in jedem Fall exportiert werden sollen.
    
3. Wählen Sie unter **Define Metadaten**aus den folgenden Optionen in der Liste **Vorlage exportieren** (einmal pro Sitzung). 
    
  - **Standard**: grundlegende Satz von Datenelemente, Metadaten und Eigenschaften. Verwenden Sie diese Option aus, wenn Daten importieren bereits im erweiterten eDiscovery verarbeitet wurde und Exportieren von Daten an ein System, das bereits die Dateien enthält hochgeladen. Exportieren Sie standardmäßig Vorlage Spalten erstellt und aufgefüllt werden.
    
  - **Alle**: umfassende Auswahl an standard-Metadaten sowie alle Verarbeiten von Daten, analysieren und Relevanz Bewertungen. Diese Vorlage ist erforderlich, wenn erweiterte eDiscovery die Verarbeitung führt und Dateidaten werden zum ersten Mal mit einem externen System hochgeladen.
    
  - **Probleme**: Wählen Sie **Alle Probleme** oder ein bestimmtes Problem, das Sie erstellt haben. 
    
Wählen Sie **OK**um die erweiterten Einstellungen zu speichern, verwenden Sie die Standardwerte **Wiederherstellen** oder **Abbrechen** , um den erweiterten Einstellungen festlegen Abbrechen. 
  
## <a name="see-also"></a>Siehe auch
<a name="BK_AdvancedSettings"> </a>

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)

