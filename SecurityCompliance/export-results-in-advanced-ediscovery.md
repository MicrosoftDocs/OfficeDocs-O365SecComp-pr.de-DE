---
title: Exportieren von Ergebnissen in Office 365 Advanced eDiscovery
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
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Erfahren Sie, wie Sie Optionen zum Exportieren von Ergebnissen aus Office 365 Advanced eDiscovery definieren, einschließlich des Verfahrens zum Angeben von Parametern für einen Export Batch. '
ms.openlocfilehash: 02314b0848d8e7bb37a7cb96fa4a721cf2622712
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218095"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a>Exportieren von Ergebnissen in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Thema werden die erweiterten eDiscovery-Export-Setup Optionen beschrieben.
  
 **Inhalt dieses Themas:**
  
- [Definieren von Export Batches und-Sitzungen](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [Inkrementelle und zusätzliche Exporte](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [Einrichten von Batch Exportparametern](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [Exportieren von Berichtsausgabe Dateien](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a>Definieren von Export Batches und-Sitzungen
<a name="BK_Define"> </a>

Ein Export Batch ermöglicht die Export Verarbeitung mithilfe einer Reihe von definierten Parametern. Mit Advanced eDiscovery können Sie Batches definieren, um die einzelnen Exporte anzupassen.
  
Parameter werden pro Export Batch definiert. Ein Batch mit dem Namen "Export Batch 01" wird standardmäßig für den ersten Batch eines Falls erstellt. Sie können auch den Namen und die Beschreibung des Batches bearbeiten.
  
Bei einer Export Sitzung handelt es sich um eine Ausführung des erweiterten eDiscovery-Exports innerhalb eines Export Batches.
  
## <a name="incremental-and-additional-exports"></a>Inkrementelle und zusätzliche Exporte
<a name="BK_IncrementalReports"> </a>

Sie können mehrere Export Sitzungen innerhalb eines Export Batches ausführen, um konsistente Ergebnisse auf der Grundlage derselben Exportvorlage und Parameter sicherzustellen. Für jede Sitzung innerhalb eines Batches können Sie Analysen für neu verarbeitete Falldaten exportieren und diese inkrementell verarbeiten.
  
Wenn Sie einen anderen Satz von Parametern exportieren möchten, müssen Sie zunächst einen neuen Batch erstellen. Die erste Sitzung im neuen Batch erzeugt Ergebnisse für im Fall verarbeitete Dateien, unabhängig davon, ob diese Dateien importiert und über einen oder mehrere imPorte verarbeitet wurden. Jeder Batch berechnet Pivots, Similarity, inclusive, etc. Sitzungen verwenden die für den Batch definierten Parameter und berechnen Pivots, Similarity, inclusives, etc. für jede Sitzungs Ausführung nicht neu.
  
Nehmen wir beispielsweise an, ein Fall wurde importiert, und die Daten wurden analysiert. Um Near-Duplicates-und e-Mail-Threading-Ergebnisse für die inkrementellen Daten abzurufen, klicken Sie auf **Export Sitzung** in demselben Batch erstellen, der zuvor zum Exportieren von Daten verwendet wurde. 
  
## <a name="set-up-batch-export-parameters"></a>Einrichten von Batch Exportparametern
<a name="BK_SetUpExport"> </a>

Das eDiscovery-Export Tool wird verwendet, um Suchergebnisse aus Advanced eDiscovery auf Ihren lokalen Computer zu exportieren. Um den Durchsatz bei der Datenübertragung zu erhöhen und den Exportvorgang zu beschleunigen, können Sie eine Windows-Registrierungseinstellung auf dem Computer konfigurieren, den Sie zum Exportieren der Suchergebnisse verwenden. Wenn Sie die Downloadgeschwindigkeit verlängern möchten, konfigurieren Sie die Registrierungseinstellung, bevor Sie die Exportparameter einrichten. Weitere Informationen finden Sie unter [höhere Downloadgeschwindigkeit beim Exportieren von eDiscovery-Suchergebnissen aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. Wählen Sie unter Erweiterte eDiscovery eine Groß-/Kleinschreibung aus, und klicken Sie auf **Setup** **exportieren** \> .
    
    - Wählen Sie in der Liste **Export Batch** den Namen des Batches aus, oder exportieren Sie die Ergebnisse, um den Batch 01 zu exportieren (Standard Batch). 
    
    - Wenn Sie Ergebnisse für neue Dateien exportieren möchten, die Sie einem vorhandenen Fall hinzugefügt haben, fahren Sie mit dem aktuellen Batch fort. Um eine Sitzung im Batch zu erstellen, wählen Sie dieselbe Batchnummer aus, und klicken Sie auf **Export Sitzung erstellen** mit dieser Option können Sie die gleichen Parameter wie im vorherigen Batch inkrementell exportieren. 
    
    - Um in einen neuen Batch zu exportieren, klicken Sie auf](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)hinzufügen Symbol **Hinzufügen** ![, und geben Sie einen neuen Namen in den **batchnamen** ein (oder übernehmen Sie den Standardwert) und eine Beschreibung in der **Batch Beschreibung**. Klicken Sie auf **OK**.
    
    - Wenn Sie einen batchnamen oder eine Beschreibung bearbeiten möchten, wählen Sie den Namen unter **Export Batch**aus](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), klicken Sie auf Bearbeitungssymbol **Bearbeiten** ![, und ändern Sie dann die Felder.
    
      > [!NOTE]
      > Nachdem Sie Sitzungen für einen Export Batch ausgeführt haben, können diese nicht gelöscht werden. Darüber hinaus können nur einige Parameter bearbeitet werden, nachdem die erste Sitzung ausgeführt wurde. 
  
    - Wenn Sie einen doppelten Export Batch erstellen möchten, wählen Sie **Duplicate** ![Export Batch Create a Duplicate](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) Export Batch Icon aus, und geben Sie im Bereich einen Namen und eine Beschreibung für den doppelten Batch ein. 
    
    - Wenn Sie einen Export Batch löschen möchten **** ![, klicken Sie auf Löschen eines](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg)Export Batch-Symbols.
    
    - Um den Verlauf eines Batches anzuzeigen, wählen **** ![Sie Verlaufs Symbol](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg)für den Stapelverarbeitungs Verlauf.
    
2. Wählen Sie unter **Auffüllung**die Option **nur Dateien über Relevanz Cut-Off Score** und/oder **Export Batch verfeinern** aus, wenn Sie die Einstellungen für Ihren Export Batch optimieren möchten. 
    
3. Wenn Sie **nur Dateien über Relevanz Cut-Off-Score einbeziehen**aktivieren, wird das **Problem** aktiviert. Wenn der relevanzwert der Datei höher ist als der Wert für das ausgewählte Problem, wird die Datei exportiert, es sei denn, Sie wird durch den Filter ' for Review ' ausgeschlossen. 
  
    Wenn Sie **Export Batch verfeinern**auswählen, werden die Optionsfelder **de-dupe** und Filter by Review aktiviert. Wenn Sie Deduplizierung auswählen, werden doppelte Dateien entsprechend der definierten Richtlinie gefiltert [Case Level (Standard): aus jedem Satz doppelter Dateien im gesamten Fall werden nur eine Datei debetrogen. **** Depot Ebene: aus jeder Gruppe von doppelten Dateien desselben Depotbank wird nur eine Datei debetrogen.] Die Ausgabe des Exports enthält einen Datensatz aller doppelten Dateien. Wenn Sie **Filtern nach ' zur Überarbeitung '** wählen, wählen Sie **unter Metadaten ändern** , um die Feld Einstellungen **für die Überprüfungen** einzugeben. Wählen Sie **Eingabedateien einfügen** aus, um Quelldateien in den Paketinhalt einzubeziehen. Sie können diese Einstellung deaktivieren, um den Exportvorgang zu beschleunigen. Beachten Sie, dass die systemeigenen Dateien in jedem Fall exportiert werden. 
    
4. Wählen Sie unter **Metadaten**aus den folgenden Optionen in der Liste **Export Vorlage** (einmal pro Sitzung) aus. 
    
    - **Standard**: grundlegende Gruppe von Datenelementen, Metadaten und Eigenschaften. Verwenden Sie diese Option, wenn Importdaten bereits in Advanced eDiscovery verarbeitet wurden und Exportdaten in ein System hochgeladen werden, in dem die Dateien bereits enthalten sind. Standardmäßig werden Spalten für das Exportieren von Vorlagen erstellt und ausgefüllt.
    
    - **All**: vollständiger Satz von Standardmetadaten einschließlich aller verarbeitungsDaten sowie Analyse-und Relevanzwerte. Diese Vorlage ist erforderlich, wenn Advanced eDiscovery die Verarbeitung ausführt und Dateidaten zum ersten Mal auf ein externes System hochgeladen werden.
    
    - **Probleme**: Wählen Sie **alle Probleme** aus, oder wählen Sie ein bestimmtes Problem aus, das Sie erstellt haben. 
    
5. Unter **Ziel**:
    
    - **Auf lokalen Computer herunterladen**
    
    - **In benutzerdefinierten Azure-BLOB exportieren**: Wenn diese Option aktiviert ist, können Sie eine Container-URL und ein SAS-Token angeben.
    
      > [!NOTE]
      > Nachdem ein Exportpaket im benutzerdefinierten Azure-BLOB gespeichert wurde, werden die Daten nicht mehr von Advanced eDiscovery verwaltet. Sie wird vom Azure-BLOB verwaltet. Wenn Sie also den Fall löschen, verbleiben die exportierten Dateien weiterhin im Azure-BLOB. 
  
    - **SAS-Token für zukünftige Export Sitzung speichern**: Wenn diese Option aktiviert ist, wird das SAS-Token in der internen Datenbank von Advanced eDiscovery für zukünftige Verwendung verschlüsselt.
    
      > [!NOTE]
      > Derzeit läuft das SAS-Token nach einem Monat ab. Wenn Sie versuchen, nach mehr als einem Monat herunterzuladen, müssen Sie die letzte Sitzung rückgängig machen und dann erneut exportieren. 
  
6. Klicken Sie auf **ändern** , um die Feld Einstellungen für Überprüfungen festzulegen. 
    
    ![Einrichten von Feld Einstellungen für Überprüfungen für einen Export Batch](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
   - Wählen Sie unter **für Überprüfungen von Feld Einstellungen**in Dropdownliste **Szenario auswählen** das Szenario und den Umfang der Überprüfungen aus. Die Einstellungen werden basierend auf Ihrer Auswahl angezeigt.
    
      - **Alle überarbeiten** (Standard): alle e-Mails, Anlagen und Dokumente sind standardmäßig ausgewählt. 
    
      - **Überarbeiten Sie alle eindeutigen Inhalte in einem Satz**: inclusives und Unique inclusive copies, Unique Attachments in e-Mail-Set-Ebene, repräsentativ aus jedem Satz von exakten Duplikaten.
    
      - **Überarbeiten Sie alle eindeutigen Inhalte in einem Set-No inclusive-Kopien**: inclusives, Unique Attachments in e-Mail-Set-Ebene, repräsentativ aus jedem Satz von exakten Duplikaten.
    
      - **Überarbeiten Sie alle eindeutigen Inhalte und verwandten Familiendateien**: inclusives, Unique Attachments in e-Mail-Set-Ebene, repräsentativ aus jedem Satz von exakten Duplikaten, erweitern Sie, um Familiendateien einzubeziehen.
    
      - **Benutzerdefiniert** (ermöglicht es Ihnen, die Optionen im Dialogfeld zu definieren): die Standardeinstellung ist, aktuelle Auswahl beizubehalten und alle Dialog Optionen zu aktivieren, um die Auswahl zu ermöglichen. Wenn Sie diese Option auswählen, können Sie die Einstellungen für e-Mails, Dokumente, Anlagen und Verschiedenes anpassen.
    
    - Wählen Sie unter **e-Mails**die e-Mails aus, die Sie exportieren möchten.
    
      - **Alle e-Mails**: (Standard) alle e-Mails sind ausgewählt.
    
      - **Inclusives**: eine umfassende e-Mail ist eine letzte e-Mail eines Threads und enthält alle anderen e-Mails aus dem Thread.
    
      - Inclusive **-und Unique inclusive-Kopien**: inklusive Kopien und Inklusivleistungen mit demselben Betreff, Körper und Anlagen; eindeutige inklusive Kopien sind eindeutige Kopien dieser e-Mails.
    
    - Wählen Sie unter **Dokumente**die Dokumente aus, die Sie exportieren möchten. 
    
      - **Alle Dokumente**: (Standard) alle Dokumente sind ausgewählt.
    
      - **Pivots**: eine Datei, die als Vertreter des Satzes für nahezu Duplikate ausgewählt wurde, der normalerweise beim Überprüfen des Satzes als Baseline verwendet wird.
    
      - **Repräsentativ aus jeder Gruppe von exakten Duplikaten**: einzigartige near-Duplicate-Dateien (einschließlich Pivot).
    
    - Wählen Sie unter **Anlagen**die zu exportierenden Anlagen aus. 
    
      - **Alle Anlagen**: (Standard) alle Anlagen sind ausgewählt.
    
      - **Eindeutige Anlage im Fallebene**: eindeutige Anlagendateien innerhalb des angegebenen Falls.
    
      - **Eindeutige Anlage im e-Mail-Set-Level**: eindeutige Anlagendateien innerhalb des angegebenen e-Mail-Falls.
    
   - Unter**Micellaneous**können Sie **Anhänge als Dokumente behandeln**, **e-Mails als Dokumente behandeln**oder **Familiendateien hinzufügen**. Wenn Sie erweitern auswählen, **um Familiendateien einzubeziehen**, werden für jede zur Überarbeitung gekennzeichnete Datei alle Dateien derselben Familie ebenfalls gekennzeichnet.
    
7. Klicken Sie auf **Speichern** , um die Einstellungen zu speichern. 
    
8. Nachdem Sie Exportparameter angegeben haben, klicken Sie auf **Export Sitzung erstellen**, um den Export Batch zu starten.
    
    Während des Exports wird der Status im **Vorgangsstatus**angezeigt. Die Ergebnisse werden in der **Export Zusammenfassung**angezeigt.
    
9. Klicken Sie im Fenster **Dateien herunterladen** auf in **Zwischenablage kopieren** , um den Export Schlüssel zu kopieren. 
    
    ![Dateien herunterladen](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
10. Klicken Sie auf **Schließen**. 
    
    Das eDiscovery-Export Tool wurde gestartet.
    
    ![eDiscovery-Exporttool](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
11. Im **eDiscovery-Export Tool**:
    
    -  Fügen Sie in **Einfügen der gemeinsamen Zugriffssignatur, die zum Herstellen einer Verbindung mit der Quelle verwendet wird**, in Schritt 7 den Export Schlüssel ein, der youcopied in die Zwischenablage kopiert.
    
    - Klicken Sie auf **Durchsuchen** , um den Zielspeicherort für die heruntergeladenen Exportdateien auf dem lokalen Computer auszuwählen. 
    
    - Klicken Sie auf **starten**. Die Exportdateien werden auf den lokalen Computer heruntergeladen. Wenn Sie in Schritt 4 die Option **zum Exportieren in benutzerdefiniertEs Azure-BLOB** ausgewählt haben, wird die Sitzung in ein BLOB-Speicher-URL-Ziel Ihrer Wahl exportiert.
    
Eine vollständige Beschreibung der Felder im Exportbericht finden Sie unter [Export Report Fields](export-report-fields-in-advanced-ediscovery.md).
  
## <a name="export-report-output-files"></a>Exportieren von Berichtsausgabe Dateien
<a name="BK_ExportOutputFIles"> </a>

In der folgenden Tabelle sind die Ausgabedateien aufgeführt, die beim Ausführen eines Export Batches generiert werden.
  
|**Dateiname**|**Dateityp**|**Beschreibung**|
|:-----|:-----|:-----|
|Zusammenfassung exportieren  <br/> |CSV  <br/> |Eine vom eDiscovery-Export Tool generierte Protokolldatei.  <br/> |
|Ablaufverfolgung  <br/> |txt  <br/> |Eine vom eDiscovery-Export Tool generierte Protokolldatei.  <br/> |
|Extrahierte Textdateien  <br/> |Datei Ordner  <br/> |Ordner, der die extrahierten Textdateien der exportierten Dateien enthält.  <br/> |
|Eingabe-oder systemeigene Dateien  <br/> |Datei Ordner  <br/> |Ordner, der die systemeigenen und Eingabedateien der exportierten Dateien enthält.  <br/> |
|Liste exportieren  <br/> |xlsx  <br/> |Exportierte Metadaten im XLSX-Format. Die Felder in den Dateien entsprechen der Auswahl des Vorlagen Benutzers für den Export. Bei Bedarf werden mehrere Dateien erstellt, die jeweils 100 150K Zeilen enthalten. Wenn ein bestimmter Wert mehr Zeichen enthält, als eine Excel-Zelle enthalten kann (derzeit ist der Grenzwert 32.767 Zeichen), wird der Wert auf die zulässige maximale Länge gekürzt. Wenn ein Wert gekürzt wird, ist die Hintergrundfarbe der Zelle rot, um dies dem Benutzer anzuzeigen. " E-Mail-Teilnehmer "ist ein Beispiel für ein Feld, das den Längen Grenzwert überschreiten kann, wenn die e-Mail an eine umfangreiche Verteilung gesendet wurde. Details zu den Ausgabefeldern finden Sie unter [Export Report Fields](export-report-fields-in-advanced-ediscovery.md) .<br/> |
|Datei laden  <br/> |CSV  <br/> |Exportierte Metadaten im CSV-Format zum Laden in eine andere Anwendung. Die Felder in den Dateien entsprechen der Auswahl des Vorlagen Benutzers für den Export.  <br/> |
|Erfolgsindikator  <br/> |txt  <br/> |Wird nur beim Exportieren in ein Azure-BLOB von einem Drittanbieter erstellt. Wenn der Export vollständig erfolgreich verläuft, wird die Datei erstellt. Bei einem Fehler oder teilweiser Erfolg wird die Datei nicht erstellt. Die Datei wird im Stammordner erstellt und ermöglicht die automatische Nachverfolgung in verschiedenen Export Batches/-Sitzungsstatus. Dies ist eine leere Datei. Der Name lautet: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime. txt.  <br/> |
   
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Anzeigen des Batch Verlaufs und exportieren vergangener Ergebnisse](view-batch-history-and-export-past-results.md)
  
[Schnelleinrichtung für Office 365 Advanced eDiscovery](quick-setup-for-advanced-ediscovery.md)

[Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md)
  
[Höhere Downloadgeschwindigkeit beim Exportieren von eDiscovery-Suchergebnissen aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md)

