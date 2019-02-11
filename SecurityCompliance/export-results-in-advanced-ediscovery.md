---
title: Exportieren von Ergebnissen in Office 365 Advanced eDiscovery
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
ms.assetid: a9951a07-10b3-48cb-b37a-0ffaa24931ad
description: 'Hier erfahren Sie, wie Sie Optionen für den Export von Ergebnissen aus Office 365 erweiterte eDiscovery, einschließlich des Verfahrens zum Angeben der Parameter für einen Batch Export definieren. '
ms.openlocfilehash: 49dab9820735af3bf5c322fc531c78a6baab2f8e
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559048"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a>Exportieren von Ergebnissen in Office 365 Advanced eDiscovery

> [!NOTE]
> Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
In diesem Thema werden die erweiterten eDiscovery exportieren Setupoptionen.
  
 **Inhalt dieses Themas:**
  
- [Definieren von Export Batches und Sitzungen](export-results-in-advanced-ediscovery.md#BK_Define)
    
- [Inkrementelle und zusätzliche Exporte](export-results-in-advanced-ediscovery.md#BK_IncrementalReports)
    
- [Einrichten von Batch Export-Parameter](export-results-in-advanced-ediscovery.md#BK_SetUpExport)
    
- [Exportieren von Ausgabedateien Bericht](export-results-in-advanced-ediscovery.md#BK_ExportOutputFIles)
    
## <a name="defining-export-batches-and-sessions"></a>Definieren von Export Batches und Sitzungen
<a name="BK_Define"> </a>

Ein Export Batch ermöglicht Exportvorgang mithilfe einer Reihe von definierten Parameter. Erweiterte eDiscovery können Sie Batches zum Anpassen der einzelnen Export definieren.
  
Parameter werden pro Export Batch definiert. In der Standardeinstellung für den ersten Batch einer Anfrage wird ein Batches mit dem Namen "Exportieren Batch 01" erstellt. Sie können auch den Namen und die Beschreibung bearbeiten.
  
Eine Export-Sitzung ist Ausführung des erweiterten eDiscovery-Export innerhalb eines Batches exportieren.
  
## <a name="incremental-and-additional-exports"></a>Inkrementelle und zusätzliche Exporte
<a name="BK_IncrementalReports"> </a>

Sie können mehrere Export Sitzungen innerhalb eines Batches exportieren, um sicherzustellen, dass übereinstimmende Ergebnisse basierend auf dem gleichen Exportvorlage und Parameter ausführen. Für jede Sitzung in einem Batch können Sie Analytics exportieren, neu Groß-/Kleinschreibung Daten verarbeitet und Verarbeiten von jeweils "inkrementell".
  
Um mit anderen Parametern zu exportieren, müssen Sie zuerst einen neuen Batch zu erstellen. Die erste Sitzung in das neue Blatt erzeugt Ergebnisse für Dateien verarbeitet im Fall bisher, unabhängig davon, ob diese Dateien importiert und über eine oder mehrere Imports verarbeitet wurden. Jedem Batch wird die Pivot-Elemente, Ähnlichkeit, Inclusives neu berechnet. Sitzungen verwenden Sie die Parameter für den Batch definiert und nicht neu berechnet Pivot-Elemente, Ähnlichkeit, Inclusives usw. für jede Sitzung Ausführung.
  
Nehmen wir beispielsweise an eine Anfrage importiert wurde, und seine Daten analysiert. Um in der Nähe Duplikate und Threading-e-Mail-Ergebnisse für die inkrementellen Daten abzurufen, klicken Sie auf **Create Session exportieren** im selben Batch, der zuvor zum Exportieren von Daten verwendet wurde. 
  
## <a name="set-up-batch-export-parameters"></a>Einrichten von Batch Export-Parameter
<a name="BK_SetUpExport"> </a>

Die eDiscovery-Exporttool wird verwendet, um Suchergebnisse aus erweiterte eDiscovery auf Ihrem lokalen Computer zu exportieren. Um die Daten Übertragungsdurchsatz und beschleunigen der Exportvorgang erhöhen möchten, können Sie eine Einstellung für die Windows-Registrierung auf dem Computer konfigurieren, mit denen Sie die Suchergebnisse exportieren. Wenn Sie die Download-Geschwindigkeit erhöhen möchten, konfigurieren Sie die Einstellung der Registrierung, bevor Sie die Exportparameter einrichten. Weitere Informationen finden Sie unter [erhöhen die Geschwindigkeit Download beim Exportieren von eDiscovery-Suchergebnisse aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md).
  
1. Wählen Sie eine Anfrage im erweiterte eDiscovery, und klicken Sie auf **Exportieren** \> **Setup**.
    
    - Aus der Liste **Exportieren Batch** wählen den Blattnamen oder Exportieren von Ergebnissen in Export Batch 01 (Standard). 
    
    - Um Ergebnisse für neue Dateien zu exportieren, die Sie einer vorhandenen Anfrage hinzugefügt haben, fahren Sie mit Ihren aktuellen Stapel. Zum Erstellen einer Sitzung im Batch, wählen Sie die gleiche Anzahl von Batch aus, und klicken Sie auf **Create Session exportieren** können Sie diese Option verwenden, so exportieren Sie die gleichen Parameter als den vorherigen Batch eine inkrementelle Weise. 
    
    - Klicken Sie auf **Hinzufügen** , um einen neuen Batch zu exportieren, ![Symbol hinzufügen](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)und geben Sie einen neuen Namen in **Blattname** (oder übernehmen Sie den Standardwert) und eine Beschreibung im **Feld Beschreibung Batch**. Klicken Sie auf **OK**.
    
    - Um einen Namen oder die Beschreibung zu bearbeiten, wählen Sie den Namen im **Batch exportieren**, klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), und klicken Sie dann die Felder zu ändern.
    
      > [!NOTE]
      > Nach dem Ausführen Sitzungen für einen Batch Export können sie gelöscht werden. Darüber hinaus können nur einige Parameter bearbeitet werden, sobald die erste Sitzung ausgeführt wird. 
  
    - Wählen Sie zum Erstellen eines Batches für die doppelte Export **Duplikat Export Batch** ![doppelte Export Batch-Symbol erstellen](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) , und geben Sie einen Namen und eine Beschreibung für den doppelten Batch in der Systemsteuerung. 
    
    - Wählen Sie zum Löschen eines Batches Export **Löschen** ![löschen Symbolgröße Batch Export](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).
    
    - Wählen Sie zum Anzeigen des Verlaufs eines Batches **Batch Verlauf** ![Ansicht Verlauf Symbol](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).
    
2. Wählen Sie unter **Auffüllung** **Includedateien nur über Relevanz Grenzwert Score** und/oder **verfeinern Export Batch** , wenn Sie die Einstellungen für Ihren Export-Stapel optimieren möchten. 
    
3. Wenn Sie **nur Dateien über Relevanz Grenzwert Score einschließen**ausgewählt haben, ist das **Problem** aktiviert. Wenn die Datei Relevanz Score höher ist als die Bewertung Grenzwert für das ausgewählte Problem ist, wird die Datei exportiert werden, wenn es vom Filter "zur Prüfung" ausgeschlossen wird. 
  
    Bei Auswahl von **verfeinern Export Batch**, die **Deduplizierung** und Filter von 'Zur Überprüfung' Feld Optionsfelder aktiviert sind. Bei Auswahl von **Deduplizierung**, und klicken Sie dann duplizierte Dateien gemäß der Richtlinie definierten herausgefiltert [Case-Ebene (Standard): aus jeder Gruppe von duplizierten Dateien in der gesamten Groß-/Kleinschreibung, alle jedoch eine Datei Aufhebung der duped werden soll. Verwaltungsberechtigter Ebene: aus jeder Gruppe von duplizierten Dateien von der gleichen Verwaltungsberechtigte, werden alle jedoch eine Datei Aufhebung der duped werden.] Die Export-Ausgabe enthält einen Datensatz für alle duplizierten Dateien. Wenn Sie **von 'zur Prüfung"** Filterfeld auswählen, wählen Sie **ändern unter Metadaten** Geben Sie Ihre Einstellungen **'zur Prüfung"** dar. Wählen Sie **input Includedateien** Quelldateien im Paketinhalt enthalten. Deaktivieren Sie diese Einstellung, um den Exportvorgang zu beschleunigen. Beachten Sie, dass die systemeigenen Dateien in jedem Fall exportiert werden sollen. 
    
4. Wählen Sie unter **Metadaten**aus der folgenden Optionen in der Liste **Vorlage exportieren** (einmal pro Sitzung). 
    
    - **Standard**: grundlegende Satz von Datenelemente, Metadaten und Eigenschaften. Verwenden Sie diese Option aus, wenn Daten importieren bereits im erweiterten eDiscovery verarbeitet wurde und Exportieren von Daten an ein System, das bereits die Dateien enthält hochgeladen. Exportieren Sie standardmäßig Vorlage Spalten erstellt und aufgefüllt werden.
    
    - **Alle**: umfassende Auswahl an standard-Metadaten sowie alle Verarbeiten von Daten, analysieren und Relevanz Bewertungen. Diese Vorlage ist erforderlich, wenn erweiterte eDiscovery die Verarbeitung führt und Dateidaten werden zum ersten Mal mit einem externen System hochgeladen.
    
    - **Probleme**: Wählen Sie **Alle Probleme** oder ein bestimmtes Problem, das Sie erstellt haben. 
    
5. Klicken Sie unter **Ziel**:
    
    - **Laden Sie auf dem lokalen Computer**
    
    - **Export in Azure Blob benutzerdefinierte**: Wenn diese Option aktiviert ist, können Sie angeben, dass ein Container-URL und SAS-Token.
    
      > [!NOTE]
      > Sobald ein Exportpaket zu gespeichert wurde die benutzerdefinierten Azure Blob, die Daten werden nicht mehr verwaltet von erweiterten eDiscovery; Es wird von den Azure Blob verwaltet. Dies bedeutet, wenn Sie die Groß-/Kleinschreibung löschen, die exportierten Dateien weiterhin auf die Azure Blob verbleibt. 
  
    - **Token für zukünftige Export-Sitzung speichern SAS**: Wenn diese Einstellung aktiviert, wird das SAS-Token in der erweiterten eDiscovery interne Datenbank für die zukünftige Verwendung verschlüsselt werden.
    
      > [!NOTE]
      > Derzeit läuft ab das Token SAS nach Monat. Wenn Sie versuchen, die nach mehr als einem Monat herunterladen Sie die letzten Sitzung rückgängig zu machen müssen, exportieren Sie dann erneut. 
  
6. Klicken Sie auf **Ändern** , um die Feldeigenschaften "zur Prüfung" festgelegt. 
    
    ![Einrichten von für überprüfen Sie die Einstellungen für einen Batch Export dar](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
   - **Für Überarbeitung dar**in Szenario Pulldownmenü Liste **auswählen** , wählen Sie unter der Szenario und des Umfangs der Überprüfung. Die Einstellungen werden basierend auf Ihrer Auswahl angezeigt.
    
      - **Alle überprüfen** (Standard): alle e-Mails, Anlagen und Dokumente standardmäßig ausgewählt sind. 
    
      - **Überprüfen Sie alle eindeutigen Inhalte in einem Satz**: Inclusives eindeutige inklusive Kopien, eindeutige Anlagen in e-Mail eingestellt aus jeder Gruppe von genaue Duplikate repräsentative Ebene.
    
      - **Überprüfen Sie alle eindeutigen Inhalt in einem Satz - keine inklusiven Kopien**: Inclusives, legen Sie eindeutige Anlagen in e-Mail Ebene, repräsentative aus jeder Gruppe von genaue Duplikate.
    
      - **Überprüfen Sie alle eindeutige und die zugehörige Produktfamilie Dateien**: Inclusives eindeutige Anlagen in e-Mail-Ebene festlegen Vertreter jede Gruppe von genaue Duplikate zu erweitern, um Produktfamilie Dateien enthalten.
    
      - **Benutzerdefinierte** (können Sie die Optionen im Dialogfeld definieren): die Standardmethode ist auf die aktuelle Auswahl beibehalten und aktivieren alle Dialogfeld Optionen, um ihre Auswahl zu ermöglichen. Wenn Sie diese Option auswählen, können Sie dann die Einstellungen für e-Mails, Dokumente, Anlagen anpassen und sonstige.
    
    - Wählen Sie unter **-e-Mails**die e-Mails, die Sie exportieren möchten.
    
      - **Alle e-Mails**: (Standardeinstellung) alle e-Mails ausgewählt sind.
    
      - **Inclusives**: eine inklusive e-Mail ist eine letzte e-Mail von einem Thread, und alle e-Mails aus dem Thread enthält.
    
      - **Inclusives und eindeutige inklusive Kopien**: inklusive Kopien und Inclusives mit dem gleichen Betreff, Textkörper und Anlagen; eindeutige inklusive Kopien werden eindeutige Kopien der diese e-Mails.
    
    - Wählen Sie unter **Dokumente**die Dokumente, die Sie exportieren möchten. 
    
      - **Alle Dokumente**: (Standardeinstellung) alle Dokumente ausgewählt sind.
    
      - **Pivot-Elemente**: eine Datei als repräsentativ für die in der Nähe Duplikate festgelegt, die in der Regel als Grundlinie verwendet wird, wenn die Gruppe zu überprüfen.
    
      - **Repräsentative aus jeder Gruppe von genaue Duplikate**: eindeutige nahezu doppelte Dateien (einschließlich das Pivot).
    
    - Wählen Sie unter **Anlagen**die Anlagen, die Sie exportieren möchten. 
    
      - **Alle Anlagen**: (Standardeinstellung) alle Anlagen ausgewählt sind.
    
      - **Eindeutige Anlage in Groß-/Kleinschreibung Ebene**: eindeutige Anlagedateien innerhalb der angegebenen Groß-/Kleinschreibung.
    
      - **Legen Sie eindeutige Anlagen in e-Mail-Nachricht**: eindeutige Anlagedateien in die angegebene e-Mail-Groß-/Kleinschreibung.
    
   - Sie können unter**Micellaneous** **Anlagen als Dokumente behandelt**, **wie Dokumente-e-Mails behandelt**oder **erweitern, um Produktfamilie Includedateien**angeben. Bei der Auswahl **erweitern, um Produktfamilie Includedateien**, für jede Datei zur Prüfung gekennzeichnet ist, werden auch alle Dateien derselben Familie gekennzeichnet.
    
7. Wählen Sie **Speichern** , um die Einstellungen zu speichern. 
    
8. Nachdem Sie Exportparameter angeben, um Export-Batch starten klicken Sie auf **Create Session exportieren**.
    
    Während des Exportvorgangs wird der Status in **Aufgabenstatus**angezeigt. Die Ergebnisse werden in der **Zusammenfassung Export**angezeigt.
    
9. Klicken Sie auf **in die Zwischenablage kopieren** , um den Schlüssel exportieren kopieren, klicken Sie im Fenster **Downloaddateien** . 
    
    ![Herunterladen von Dateien](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
10. Klicken Sie auf **Schließen**. 
    
    Die eDiscovery-Exporttool wird gestartet.
    
    ![eDiscovery-Exporttool](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
11. In der **eDiscovery-Exporttool**:
    
    -  Fügen Sie in **Einfügen der Signatur Zugriff freigegeben, die zum Verbinden mit der Datenquelle verwendet wird**dem Schlüssel exportieren, Youcopied in die Zwischenablage in Schritt 7.
    
    - Klicken Sie auf **Durchsuchen** , um den Zielspeicherort zum Speichern der heruntergeladenen Exportdateien auf dem lokalen Computer auszuwählen. 
    
    - Klicken Sie auf **Start**. Die Exportdateien werden auf den lokalen Computer heruntergeladen. Wenn Sie in Schritt 4 **Export in Azure Blob Benutzerdefiniert** ausgewählt haben, wird die Sitzung an ein BLOB-Speicher-Ziel-URL Ihrer Wahl exportiert.
    
Eine vollständige Beschreibung der Felder in den Exportbericht finden Sie unter [Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md).
  
## <a name="export-report-output-files"></a>Exportieren von Ausgabedateien Bericht
<a name="BK_ExportOutputFIles"> </a>

Die folgende Tabelle enthält die Ausgabedateien, die beim Ausführen eines Batches Export generiert werden.
  
|**Dateiname**|**Dateityp**|**Beschreibung**|
|:-----|:-----|:-----|
|Zusammenfassung exportieren  <br/> |CSV  <br/> |Eine Protokolldatei generiert, indem die eDiscovery Exporttool.  <br/> |
|Spur  <br/> |txt  <br/> |Eine Protokolldatei generiert, indem die eDiscovery Exporttool.  <br/> |
|Extrahierten Textdateien  <br/> |Dateiordner  <br/> |Ordner, der die extrahierten Textdateien der exportierten Dateien enthält.  <br/> |
|Eingabe oder systemeigene Dateien  <br/> |Dateiordner  <br/> |Ordner, die systemeigenen und input-Dateien der exportierten Dateien enthält.  <br/> |
|Liste exportieren  <br/> |xlsx  <br/> |Metadaten der exportierten Dateien im Xlsx-Format dar. Felder in Dateien werden gemäß der Vorlage Benutzer wählt zu exportieren. Falls erforderlich, mehrere Dateien erstellt wurden, jeweils 100-150 KB Zeilen enthält. Wenn Sie ein bestimmten Wert enthält mehr Zeichen als eine Excel-Zelle enthalten kann (derzeit die Grenze liegt bei 32.767 Zeichen), und klicken Sie dann der Wert wird auf die maximal zulässige Länge gekürzt werden. Wenn Sie ein Wert abgeschnitten wird, ist Hintergrundfarbe der Zelle an, dass dies dem Benutzer Rot." E-Mail Teilnehmer"ist ein Beispiel für ein Feld, das die maximale Länge überschreiten kann, wenn die e-Mail-Nachricht an eine große Verteilergruppe gesendet wurde. Details zu den Ausgabefeldern finden Sie unter [Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md) .<br/> |
|Datei laden  <br/> |CSV  <br/> |Metadaten der exportierten Dateien im CSV-Format in einer anderen Anwendung geladen. Felder in Dateien werden gemäß der Vorlage Benutzer wählt zu exportieren.  <br/> |
|Symbol für Erfolg  <br/> |txt  <br/> |Nur erstellt beim Exportieren einer 3rd Azure Blob Partei. Wenn der Export erfolgreich ausgeführt werden, wird die Datei erstellt. Bei einem Ausfall oder den partiellen wird Erfolg die Datei nicht erstellt werden. Datei wird im Stammordner, ermöglicht die automatisierte Tracking auf verschiedenen Export Batches-Sitzungen Statusarten erstellt werden. Dies ist eine leere Datei. Ihr Name lautet: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.  <br/> |
   
## <a name="see-also"></a>Siehe auch

[Office 365 Advanced eDiscovery](office-365-advanced-ediscovery.md)
  
[Anzeigen des Verlaufs Batch und ältere Ergebnisse exportieren](view-batch-history-and-export-past-results.md)
  
[Schnelleinrichtung für Office 365 Advanced eDiscovery](quick-setup-for-advanced-ediscovery.md)

[Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md)
  
[Die Download-Leistung zu steigern, beim Exportieren von eDiscovery-Suchergebnisse aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md)

