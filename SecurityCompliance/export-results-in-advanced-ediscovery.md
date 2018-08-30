---
title: Exportieren von Ergebnissen in Office 365 erweiterte eDiscovery
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
ms.openlocfilehash: 92ee107ad096393fbccbc9a3dbe81d8e7dd28da9
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530043"
---
# <a name="export-results-in-office-365-advanced-ediscovery"></a>Exportieren von Ergebnissen in Office 365 erweiterte eDiscovery

> [!NOTE]
> Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279). 
  
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
    
  - Klicken Sie auf **Hinzufügen**, um einen neuen Batch zu exportieren,![Symbol hinzufügen](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png)und geben Sie einen neuen Namen in **Blattname** (oder übernehmen Sie den Standardwert) und eine Beschreibung im **Feld Beschreibung Batch**. Klicken Sie auf **OK**.
    
  - Um einen Namen oder die Beschreibung zu bearbeiten, wählen Sie den Namen im **Batch exportieren**, klicken Sie auf **Bearbeiten** ![Bearbeitungssymbol](media/3d613660-7602-4df2-bdb9-14e9ca2f9cf2.png), und klicken Sie dann die Felder zu ändern.
    
    > [!NOTE]
    > Nach dem Ausführen Sitzungen für einen Batch Export können sie gelöscht werden. Darüber hinaus können nur einige Parameter bearbeitet werden, sobald die erste Sitzung ausgeführt wird. 
  
  - Wählen Sie zum Erstellen eines Batches für die doppelte Export **Duplikat Export Batch**![doppelte Export Batch-Symbol erstellen](media/3f6d5f59-e842-4946-a493-473528af0119.jpg) , und geben Sie einen Namen und eine Beschreibung für den doppelten Batch in der Systemsteuerung. 
    
  - Wählen Sie zum Löschen eines Batches Export **Löschen**![löschen Symbolgröße Batch Export](media/92a9f8e0-d469-48da-addb-69365e7ffb6f.jpg).
    
  - Wählen Sie zum Anzeigen des Verlaufs eines Batches **Batch Verlauf**![Ansicht Verlauf Symbol](media/a80cc320-d96c-4d91-8884-75fe2cb147e2.jpg).
    
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
  
6. Klicken Sie auf **Ändern** , legen Sie die "zur Überprüfung ' Feld Einstellungen. 
    
> ![Einrichten von für die Überprüfung Feld Seetings für einen Batch export](media/39451aba-f6fe-4a01-8ed0-0be6a6ce889a.png)
  
    In **For review field settings** panel, in **Select scenario**, select the scenario and scope of the review. The settings are displayed based on your selection.
    
    **Review all** (default): All emails, attachments, and documents are selected by default. 
    
    **Review all unique content in a set**: Inclusives and unique inclusive copies, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content in a set - no inclusive copies**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates.
    
    **Review all unique content and related family files**: Inclusives, unique attachments in email set level, representative from every set of exact duplicates, expand to include family files.
    
    **Custom** (allows you to define the options in the dialog): The default is to keep current selections and enable all dialog options, to allow their selection. 
    
    If you select custom, you can then customize the settings for emails, documents, attachments and miscellaneous.
    
> Wählen Sie die e-Mails, die Sie exportieren möchten, im **-e-Mails** : 
    
    **All emails**: (default) All emails are selected.
    
    **Inclusives**: An inclusive email is a last email of a thread, and it contains all the other emails from the thread.
    
    **Inclusives and unique inclusive copies**: Inclusive copies and inclusives with the same subject, body and attachments; unique inclusive copies are unique copies of these emails .
    
> Wählen Sie in **Dokumenten** die Dokumente, die Sie exportieren möchten: 
    
    **All documents**: (default) All documents are selected.
    
    **Pivots**: A file chosen as representative of near-duplicates set, which is typically used as the baseline when reviewing the set.
    
    **Representative from every set of exact duplicates**: Unique near-duplicate files (including the pivot).
    
> Wählen Sie in **Anlagen** der Anlagen, die Sie exportieren möchten 
    
    **All attachments**: (default) All attachments are selected.
    
    **Unique attachment in case level**: Unique attachment files within the specified case.
    
    **Unique attachment in email set level**: Unique attachment files within the specified email case.
    
> Im **Micellaneous** können Sie **Anlagen als Dokumente behandelt**, **wie Dokumente-e-Mails behandelt**oder **erweitern, um Produktfamilie Includedateien**auswählen. Bei der Auswahl **erweitern, um Produktfamilie Includedateien**, für jede Datei zur Prüfung gekennzeichnet ist, werden auch alle Dateien derselben Familie gekennzeichnet.
    
    Choose **Save** to save the settings. 
    
7. Nachdem Sie Exportparameter angeben, um Export-Batch starten klicken Sie auf **Create Session exportieren**.
    
    Während des Exportvorgangs wird der Status in **Aufgabenstatus**angezeigt. Die Ergebnisse werden in der **Zusammenfassung Export**angezeigt.
    
8. Klicken Sie auf **in die Zwischenablage kopieren** , um den Schlüssel exportieren kopieren, klicken Sie im Fenster **Downloaddateien** . 
    
    ![Herunterladen von Dateien](media/99cf2c13-4954-479f-9741-80d7458c1a15.png)
  
9. Klicken Sie auf **Schließen**. 
    
    Die eDiscovery-Exporttool wird gestartet.
    
    ![eDiscovery-Exporttool](media/705756ca-ee97-4d24-b70f-8b23513f6d11.gif)
  
10. In der **eDiscovery-Exporttool**:
    
1. Fügen Sie in **Einfügen der Signatur Zugriff freigegeben, die zum Verbinden mit der Datenquelle verwendet wird**dem Schlüssel exportieren, Youcopied in die Zwischenablage in Schritt 7.
    
2. Klicken Sie auf **Durchsuchen** , um den Zielspeicherort zum Speichern der heruntergeladenen Exportdateien auf dem lokalen Computer auszuwählen. 
    
11. Klicken Sie auf **Start**. Die Exportdateien werden auf den lokalen Computer heruntergeladen. Wenn Sie in Schritt 4 **Export in Azure Blob Benutzerdefiniert** ausgewählt haben, wird die Sitzung an ein BLOB-Speicher-Ziel-URL Ihrer Wahl exportiert. 
    
Eine vollständige Beschreibung der Felder in den Exportbericht finden Sie unter [Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md).
  
## <a name="export-report-output-files"></a>Exportieren von Ausgabedateien Bericht
<a name="BK_ExportOutputFIles"> </a>

Die folgende Tabelle enthält die Ausgabedateien, die beim Ausführen eines Batches Export generiert werden.
  
|**Dateiname**|**Dateityp**|**Beschreibung**|
|:-----|:-----|:-----|
|Zusammenfassung exportieren  <br/> |CSV  <br/> |Eine Protokolldatei generiert, indem die eDiscovery Exporttool.  <br/> |
|Trace  <br/> |txt  <br/> |Eine Protokolldatei generiert, indem die eDiscovery Exporttool.  <br/> |
|Extrahierten Textdateien  <br/> |Dateiordner  <br/> |Ordner, der die extrahierten Textdateien der exportierten Dateien enthält.  <br/> |
|Eingabe oder systemeigene Dateien  <br/> |Dateiordner  <br/> |Ordner, die systemeigenen und input-Dateien der exportierten Dateien enthält.  <br/> |
|Liste exportieren  <br/> |xlsx  <br/> |Metadaten der exportierten Dateien im Xlsx-Format dar. Felder in Dateien werden gemäß der Vorlage Benutzer wählt zu exportieren. Falls erforderlich, mehrere Dateien erstellt wurden, jeweils 100-150 KB Zeilen enthält. Wenn Sie ein bestimmten Wert enthält mehr Zeichen als eine Excel-Zelle enthalten kann (derzeit die Grenze liegt bei 32.767 Zeichen), und klicken Sie dann der Wert wird auf die maximal zulässige Länge gekürzt werden. Wenn Sie ein Wert abgeschnitten wird, ist Hintergrundfarbe der Zelle an, dass dies dem Benutzer Rot." E-Mail Teilnehmer"ist ein Beispiel für ein Feld, das die maximale Länge überschreiten kann, wenn die e-Mail-Nachricht an eine große Verteilergruppe gesendet wurde. Details zu den Ausgabefeldern finden Sie unter [Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md) .<br/> |
|Datei laden  <br/> |CSV  <br/> |Metadaten der exportierten Dateien im CSV-Format in einer anderen Anwendung geladen. Felder in Dateien werden gemäß der Vorlage Benutzer wählt zu exportieren.  <br/> |
|Symbol für Erfolg  <br/> |txt  <br/> |Nur erstellt beim Exportieren einer 3rd Azure Blob Partei. Wenn der Export erfolgreich ausgeführt werden, wird die Datei erstellt. Bei einem Ausfall oder den partiellen wird Erfolg die Datei nicht erstellt werden. Datei wird im Stammordner, ermöglicht die automatisierte Tracking auf verschiedenen Export Batches-Sitzungen Statusarten erstellt werden. Dies ist eine leere Datei. Ihr Name lautet: TenantId_CaseId_ExternalCaseId_CaseName_ExportBatchId_SessionId_DateTime.txt.  <br/> |
   
## <a name="see-also"></a>Siehe auch
<a name="BK_ExportOutputFIles"> </a>

[Office 365 Erweiterte eDiscovery](office-365-advanced-ediscovery.md)
  
[Anzeigen des Verlaufs Batch und ältere Ergebnisse exportieren](view-batch-history-and-export-past-results.md)
  
[Schnelles Setup für Office 365 erweiterte eDiscovery](quick-setup-for-advanced-ediscovery.md)

[Exportieren von Berichtsfeldern](export-report-fields-in-advanced-ediscovery.md)
  
[Die Download-Leistung zu steigern, beim Exportieren von eDiscovery-Suchergebnisse aus Office 365](increase-download-speeds-when-exporting-ediscovery-results.md)

