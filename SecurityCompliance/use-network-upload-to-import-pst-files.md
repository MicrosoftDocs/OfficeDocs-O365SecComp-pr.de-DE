---
title: Verwenden Sie Netzwerk hochladen, um Ihre Organisation PST-Dateien in Office 365 importieren
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: 'Für Administratoren: erfahren Sie, wie Netzwerk Upload verwenden, um mehrere PST-Dateien auf die Benutzerpostfächer in Office 365 Massenimport.'
ms.openlocfilehash: c5bcaed9075939d098ac4bf9fbf4d8a94007232c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529203"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>Verwenden Sie Netzwerk hochladen, um Ihre Organisation PST-Dateien in Office 365 importieren

> [!NOTE]
> Dieser Artikel ist für Administratoren. Versuchen Sie zum Importieren von PST-Dateien an Ihrem eigenen Postfach? Finden Sie unter [Import e-Mail, Kontakte und Kalender aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)
  
Hier erhalten Sie eine schrittweise Anleitung zum Netzwerk Upload verwenden, um mehrere PST-Dateien in Office 365-Postfächer Massenimport erforderlich sind. Häufig gestellte Fragen zur Verwendung von Netzwerk-Upload zum Massenimport PST-Dateien in Office 365-Postfächer finden Sie unter [häufig gestellte Fragen für die Verwendung von Netzwerk-hochladen, um die PST-Dateien zu importieren](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files).
  
[Schritt 1: Kopieren Sie die SAS-URL und installieren Azure AzCopy](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[Schritt 2: Hochladen Sie PST-Dateien in Office 365](#step-2-upload-your-pst-files-to-office-365)

[(Optional) Schritt 3: Hochgeladen Ansicht eine Liste der PST-Dateien nach Office 365](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Schritt 4: Erstellen Sie die Datei zur Zuordnung von PST-Import](#step-4-create-the-pst-import-mapping-file)

[Schritt 5: Erstellen eines PST-Importauftrags in Office 365](#step-5-create-a-pst-import-job-in-office-365)

[Schritt 6: Filtern von Daten, und starten Sie den Importauftrag PST-Datei](#step-6-filter-data-and-start-the-pst-import-job)

Beachten Sie, dass Sie Schritt 1 nur einmal ausführen, um PST-Dateien in Office 365-Postfächer zu importieren. Nachdem Sie diese Schritte ausgeführt haben, führen Sie Schritt2 bis 6, die jedes Mal, wenn Sie hochgeladen wird und für einen Batch von PST-Dateien importieren möchten.

## <a name="before-you-begin"></a>Bevor Sie beginnen
  
- Sie müssen die Rolle Postfach importieren exportieren in Exchange Online zum Importieren von PST-Dateien in Office 365-Postfächer zugewiesen werden. Standardmäßig ist nicht dieser Rolle alle Rollengruppe in Exchange Online zugewiesen. Sie können die Rollengruppe "Organisationsverwaltung" Postfach Import/Export-Rolle hinzufügen. Oder erstellen eine neuen Rollengruppe, weisen Sie die Rolle Postfach Import/Export und fügen Sie sich als Mitglied hinzu. Weitere Informationen finden Sie unter "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" Abschnitte auf [Rollengruppen verwalten](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Darüber hinaus Import erstellen Aufträge in der Office 365-Sicherheit &amp; Compliance Center, eine der folgenden muss true sein:
    
  - Sie müssen die Rolle des E-Mail-Empfänger in Exchange Online zugewiesen werden. Standardmäßig wird diese Rolle der Organization Management und Recipient Management Rollen Gruppen zugewiesen.
    
    oder -
    
  - Sie müssen ein globaler Administrator in Office 365-Organisation sein.
    
  > [!TIP]
    > Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange-Online, die speziell für das Importieren von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die Mindestebene von Berechtigungen, die zum Importieren von PST-Dateien erforderlich sind der neuen Rollengruppe die Rollen Postfach importieren exportieren und E-Mail-Empfänger, und fügen Sie Mitglieder. 
  
- Die einzige unterstützte Methode für das Importieren von PST-Dateien in Office 365 ist das Tool Azure AzCopy verwenden, wie in diesem Thema beschrieben. Azure-Speicher-Explorer können Sie direkt in den Bereich der Azure-Speicher PST-Dateien hochladen.
    
- Sie müssen die PST-Dateien zu speichern, die Sie auf einem Dateiserver oder freigegebenen Ordner in Ihrer Organisation zu Office 365 importieren möchten. In Schritt2 werden Azure AzCopy Ausführen des Tools, die die PST-Dateien geladen wird, die auf diesem Dateiserver gespeichert sind oder freigegebenen Ordner zu Office 365.
    
- Dieses Verfahren umfasst das Kopieren und Speichern einer Kopie einer URL, die eine Zugriffstaste enthält. Diese Informationen werden in Schritt2, um Ihre PST-Dateien hochladen und in Schritt 3 verwendet werden, wenn Sie eine Liste der PST-Dateien in Office 365 hochgeladen anzeigen möchten. Achten Sie darauf, müssen Sie Vorsichtsmaßnahmen gegen diese URL zu schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen zu schützen. Beispielsweise können Sie es auf kennwortgeschützte Microsoft Word-Dokument oder auf ein verschlüsseltes USB-Laufwerk speichern. Finden Sie im Abschnitt [Weitere Informationen](#more-information) für ein Beispiel dafür URL und Schlüssel kombiniert. 
    
- Sie können PST-Dateien in eines inaktiven Postfachs in Office 365 importieren. Zu diesem Zweck Angabe der GUID des inaktiven Postfachs in die `Mailbox` Parameter in der Zuordnungsdatei PST-Datei importieren. Finden Sie unter Schritt 4 auf der Registerkarte **Anweisungen** in diesem Thema Informationen. 
    
- In einer Exchange-hybridbereitstellung können Sie PST-Dateien in einer Cloud-basierten Archivpostfach für einen Benutzer importieren, deren Hauptpostfach lokal wurde. Dabei wird in der Zuordnungsdatei Import von PST-Datei wie folgt:
    
  - Geben Sie die e-Mail-Adresse für das Postfach des Benutzers: lokal in der `Mailbox` Parameter. 
    
  - Geben Sie den Wert **"true"** in der `IsArchive` Parameter. 
    
    Weitere Informationen finden Sie unter [Schritt 4](#step-4-create-the-pst-import-mapping-file) . 
    
- Nachdem PST-Dateien in ein Office 365-Postfach importiert wurden, ist die Einstellung für das Postfach Anhalten der Aufbewahrungszeit für unbefristete aktiviert. Dies bedeutet, dass die Aufbewahrungsrichtlinie an das Postfach zugewiesen, bis Sie das Anhalten der Aufbewahrungszeit deaktivieren oder ein Datums festlegen So deaktivieren Sie den Haltestatus verarbeitet wird. Warum tun wir das? Wenn Sie Nachrichten in einem Postfach importiert alt sind, sie möglicherweise werden endgültig gelöscht (gelöscht), da der Aufbewahrungszeitraum abgelaufen ist basierend auf der aufbewahrungseinstellungen für das Postfach konfiguriert. Platzieren das Postfach auf Anhalten der Aufbewahrungszeit erhalten die Postfach Besitzer Zeit zum Verwalten dieser Nachrichten neu importiert oder geben Sie Zeit, um die Einstellungen für die Aufbewahrung für das Postfach zu ändern. Finden Sie unter der Registerkarte **Weitere Informationen** in diesem Thema für Vorschläge zum Verwalten von das Anhalten der Aufbewahrungszeit. 
    
- Standardmäßig ist die maximale Größe von Nachrichten, die von Office 365-Postfach empfangen werden kann 35 MB. Das liegt, da der Standardwert für die *MaxReceiveSize* -Eigenschaft für ein Postfach auf 35 MB festgelegt ist. Für die maximale Meldung Größe in Office 365 ist die Grenze jedoch 150 MB. Wenn Sie eine PST-Datei importieren, enthält ein Element größer als 35 MB, die wir ändert automatisch den Wert der *MaxReceiveSize* -Eigenschaft für das Zielpostfach auf 150 MB Importieren von Office 365-Dienst. Auf diese Weise können Nachrichten bis zu 150 MB für Benutzerpostfächer importiert werden. 
    
    > [!TIP]
    > Identifiziert die Meldung Größe für ein Postfach, können Sie diesen Befehl ausführen, in Exchange Online PowerShell: `Get-Mailbox <user mailbox> | FL MaxReceiveSize`. 

### <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>Schritt 1: Kopieren Sie die SAS-URL und installieren Azure AzCopy

Der erste Schritt besteht herunterladen und installieren Sie das Tool Azure AzCopy, das das Tool ist, das Sie in Schritt2 zum Hochladen von PST-Dateien in Office 365 ausgeführt werden. Sie können auch die SAS-URL für Ihre Organisation kopieren. Diese URL ist eine Kombination aus der Netzwerk-URL für den Speicherort der Azure-Speicher in der Microsoft-Cloud für Ihre Organisation und einer gemeinsamen Zugriff Signatur (SAS)-Taste. Dieser Schlüssel enthält die erforderlichen Berechtigungen zum Hochladen von PST-Dateien zu dem Speicherort der Azure-Speicher. Müssen Sie Vorsichtsmaßnahmen zum Schutz der SAS-URL. Es ist nur in Ihrer Organisation und in Schritt2 verwendet werden.
  
 **Wichtig:** Es wird empfohlen, Azure AzCopy Version, dass 7.1.0 zum Importieren von PST-Dateien mithilfe des Netzwerks Methode hochladen zu verwenden. In Schritt 6 b in der folgenden Prozedur wird die Version 7.1.0 heruntergeladen. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Governance** \> **Importieren**.
    
    **Hinweis:** Sie haben Zugriff auf die Seite **Importieren** in das Wertpapier die entsprechenden Berechtigungen zugewiesen werden &amp; Compliance Center. Finden Sie weitere Informationen im Abschnitt **bevor Sie beginnen** . 
    
3. Klicken Sie auf der Seite **Importieren** auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Importauftrag neu**.
    
    Der Importassistent Auftrag wird angezeigt.
    
4. Geben Sie einen Namen für den Auftrag für Import von PST-Datei, und klicken Sie dann auf **Weiter**. Verwenden Sie Kleinbuchstaben, Zahlen, Bindestriche und Unterstriche. In Großbuchstabe können nicht oder Leerzeichen im Namen enthalten.
    
5. Klicken Sie auf die **möchten Sie hochladen oder Daten liefern?** Seite, klicken Sie auf **Hochladen die Daten** , und klicken Sie dann auf **Weiter**.
    
    ![Klicken Sie auf Hochladen, die Ihre Daten zum Erstellen eines Netzwerk-Uploads Auftrag importieren](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Führen Sie auf der Seite **Daten importieren** die folgenden beiden Schritte aus: 
    
    ![Kopieren Sie die SAS-URL, und Laden Sie das Tool Azure AzCopy auf der Seite Daten importieren](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    a. Klicken Sie in Schritt 2 Klicken Sie auf **Netzwerk Upload SAS-URL anzeigen**. Nachdem die SAS-URL angezeigt wird, auf **in die Zwischenablage kopieren** und fügen Sie ihn und in einer Datei speichern Sie, damit Sie später zugreifen können.
    
    b klicken Sie in Schritt 3 auf **Azure AzCopy herunterladen** herunterladen und installieren Sie das Tool Azure AzCopy. Wie bereits erwähnt, Version 7.1.0 wird heruntergeladen werden. Klicken Sie im Popupfenster auf **Ausführen** , um AzCopy zu installieren. 
    
  **Hinweis:** Sie können die Seite **Daten importieren** geöffnet lassen, (für den Fall, dass Sie die URL SAS erneut zu kopieren müssen), oder klicken Sie auf **Abbrechen** , um es zu schließen. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>Schritt 2: Hochladen Sie PST-Dateien in Office 365

Sie können nun das Tool AzCopy.exe verwenden, um die PST-Dateien in Office 365 hoch. Dieses Tool hochgeladen und speichert diese in ein Azure Speicherort in der Microsoft-Cloud. Wie bereits erklärt befindet sich im selben regionale Microsoft Rechenzentrum, in Office 365-Organisation gespeichert ist, der Azure Speicherort, dem Sie Ihrer PST-Dateien zum Hochladen. Wenn Sie diesen Schritt abgeschlossen haben, müssen die PST-Dateien in einer Dateifreigabe oder Dateiserver in Ihrer Organisation befinden. Dies wird als Quellverzeichnis in der folgenden Prozedur bezeichnet. Jedes Mal, wenn Sie das Tool AzCopy ausführen, können Sie einen anderen Quellverzeichnis angeben. 
  
1. Öffnen Sie eine Eingabeaufforderung auf dem lokalen Computer.
    
2. Wechseln Sie zu dem Verzeichnis, in dem Sie das Tool AzCopy.exe in Schritt 1 installiert. Wenn Sie das Tool im Standardverzeichnis installiert haben, fahren Sie mit `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`.
    
3. Führen Sie den folgenden Befehl zum Hochladen von PST-Dateien zu Office 365.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    Die folgende Tabelle beschreibt die Parameter und deren Werte erforderlich. Beachten Sie, dass die Informationen, die Sie im vorherigen Schritt abgerufen haben in die Werte für diese Parameter verwendet wird.
    
    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Gibt das Quellverzeichnis in Ihrer Organisation, die die PST-Dateien enthält, die zu Office 365 hochgeladen werden soll.  <br/> Beachten Sie, den Wert dieses Parameters in doppelte Anführungszeichen (" ") einzuschließen .  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |Gibt die SAS-URL, die Sie erhalten in Schritt 1 an.  <br/> Beachten Sie, den Wert dieses Parameters in doppelte Anführungszeichen (" ") einzuschließen .  <br/> **Tipp:** (Optional) Sie können einen Unterordner in Azure Speicherort die PST-Dateien zum Hochladen angeben. Zu diesem Zweck hinzufügen einen Unterordner Speicherort (nach "Ingestiondata") in der SAS-URL. Im ersten Beispiel wird keinen Unterordner angeben. Dies bedeutet, dass die PST-Dateien in das Stammverzeichnis (mit dem Namen *Ingestiondata* ) von Azure Speicherort hochgeladen werden soll. Im zweite Beispiel werden die PST-Dateien in einem Unterordner ( *PSTFiles* ) im Stamm des Azure Speicherort hochgeladen.<br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> oder -  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |Gibt ausführliche Statusmeldungen in einer Protokolldatei aus. Die ausführliche Protokolldatei trägt standardmäßig den Namen „AzCopyVerbose.log“ in %LocalAppData%\Microsoft\Azure\AzCopy. Wenn Sie einen vorhandenen Dateispeicherort für diese Option angeben, wird das ausführliche Protokoll an diese Datei angehängt.  <br/> Beachten Sie, den Wert dieses Parameters in doppelte Anführungszeichen (" ") einzuschließen .  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |Diese optionale Befehlszeilenoption gibt den rekursiven Modus, damit das Tool AzCopy PST-Dateien kopiert werden, die in Unterordnern im Quellverzeichnis befinden, die durch angegeben ist die `/Source:` Parameter.  <br/> **Hinweis:** Wenn Sie diese Option verwenden, müssen das PST-Dateien in Unterordnern einer anderen Datei Pathname Azure Speicherort an, nachdem sie hochgeladen haben. Sie müssen den genauen Dateipfadnamen in der CSV-Datei angeben, die Sie in Schritt 4 erstellen.<br/> | `/S` <br/> |
    | `/Y` <br/> |Dieser erforderliche Option ermöglicht die Verwendung von lesegeschützte SAS Token beim Hochladen der PST-Dateien auf den Speicherort der Azure-Speicher. Die SAS-URL, die Sie in Schritt 1 abgerufene (und im angegebenen `/Dest:` Parameter) ist eine lesegeschützte SAS-URL, weshalb Sie diese Befehlszeilenoption umfassen müssen. Beachten Sie, dass eine lesegeschützte SAS-URL nicht verhindern mit dem Azure-Speicher-Explorer zum Anzeigen einer Liste der PST-Dateien in der Azure Speicherort hochgeladen.<br/> | `/Y` <br/> |
   
Nachfolgend sehen Sie ein Beispiel der Syntax für das Tool „AzCopy.exe“, in dem die tatsächlichen Werte für jeden Parameter verwendet werden:
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

Nachdem Sie den Befehl ausgeführt haben, werden Statusmeldungen angezeigt, die den Fortschritt des Hochladens der PST-Dateien anzeigen. Eine endgültige Statusmeldung zeigt die Gesamtzahl der Dateien an, die erfolgreich hochgeladen wurden. 
    
**Tipp:** Nachdem Sie erfolgreich führen den Befehl AzCopy.exe aus, und stellen Sie sicher, dass alle Parameter richtig sind, Speichern einer Kopie der die Befehlszeilensyntax auf die gleiche (gesicherten)-Datei, in dem Sie die Informationen kopiert haben, erhaltenen Sie in Schritt 1. Sie können dann kopieren und fügen diesen Befehl in einem Eingabeaufforderungsfenster jedes Mal, dem Sie das Tool AzCopy.exe zum Hochladen von PST-Dateien zu Office 365 ausführen möchten. Möglicherweise müssen Sie ändern nur ein Wert entsprechen denen für die `/Source:` Parameter. Dies hängt das Quellverzeichnis, wo sich die PST-Dateien befinden. 

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(Optional) Schritt 3: Hochgeladen Ansicht eine Liste der PST-Dateien nach Office 365

Als optionalen Schritt können Sie installieren und Verwenden der Microsoft Azure-Speicher-Explorer (Dies ist eine kostenlose open Source-Tool) zum Anzeigen der Liste der PST-Dateien, die Sie für die Azure Blob hochgeladen haben. Es gibt zwei gute Gründe dazu:
  
- Stellen Sie sicher, dass die PST-Dateien aus dem freigegebenen Ordner oder Dateiserver in Ihrer Organisation erfolgreich für die Azure Blob hochgeladen wurden.
    
- Überprüfen Sie den Dateinamen (und den Unterordner Pfadnamen, wenn Sie eine eingeschlossen) für jede PST-Datei in den Azure Blob hochgeladen. Dies ist sehr nützlich, wenn Sie die Zuordnungsdatei im nächsten Schritt müssen Sie den Ordner Pathname und den Dateinamen für jede PST-Datei anzugeben PST-Datei erstellen. Überprüfen der Managementsystems hilft bei Senkung der potenzielle Fehler in der PST-Datei zur Zuordnung.
    
Microsoft Azure-Speicher-Explorer ist in der Vorschau.
  
 **Wichtig:** Sie können der Azure-Speicher-Explorer zum Hochladen oder Ändern von PST-Dateien verwenden. Die einzige unterstützte Methode für das Importieren von PST-Dateien in Office 365 ist die Verwendung von AzCopy. Darüber hinaus können Sie nicht PST-Dateien löschen, die Sie für die Azure Blob hochgeladen haben. Wenn Sie versuchen, eine PST-Datei zu löschen, erhalten Sie einen Fehler über nicht zu den erforderlichen Berechtigungen. Beachten Sie, dass alle PST-Dateien aus Ihrer Region Azure-Speicher automatisch gelöscht werden. Wenn es keine Importaufträge in Arbeit, und klicken Sie dann auf alle PST-Dateien in sind die ** Ingestiondata ** Container werden 30 Tage nach der neueste Importauftrag erstellt wurde gelöscht. 
  
So installieren die Azure-Speicher-Explorer, und eine Verbindung mit Ihrer Region Azure-Speicher:
  
1. Herunterladen Sie und installieren Sie das [Tool von Microsoft Azure-Speicher-Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Starten Sie Microsoft Azure-Speicher-Explorer, mit der rechten Maustaste **Speicherkonten** im linken Bereich, und klicken Sie dann auf **Verbinden mit Azure-Speicher**.
    
    ![Mit der rechten Maustaste Speicherkonten und klicken Sie dann auf Verbindung mit Azure-Speicher](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Klicken Sie auf **einen freigegebenen Signatur (SAS)-URI oder Verbindung Zugriffszeichenfolge verwenden** , und klicken Sie auf **Weiter**.
    
4. Klicken Sie auf **einen URI SAS verwenden**, fügen Sie die SAS-URL, die Sie erhalten in Schritt 1 in das Feld unter **URI**, und klicken Sie dann auf **Weiter**.
    
5. Auf der Seite **Zusammenfassung Verbindung** können Sie überprüfen Sie die Verbindungsinformationen, und klicken Sie auf **Verbinden**.
    
    Der Container **Ingestiondata** wird geöffnet. Sie enthält die PST-Dateien, die Sie in Schritt2 hochgeladen. Der Container **Ingestiondata** befindet sich unter **Storage Konten** \> **(SAS-Attached Services)** \> **BLOB-Container**. 
    
    ![Im Azure-Speicher-Explorer wird eine Liste der PST-Dateien angezeigt, die Sie hochgeladen haben.](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Wenn Sie mit dem Microsoft Azure Storage Explorer fertig sind, mit der rechten Maustaste **Ingestiondata**, und klicken Sie dann auf **Trennen** , um von Ihrer Region Azure-Speicher zu trennen. Andernfalls erhalten einen Fehler beim nächsten Sie, den Sie versuchen, anfügen. 
    
    ![Klicken Sie mit der rechten Maustaste auf „ingestion“, und klicken Sie dann auf „Trennen“, um die Verbindung von Ihrem Azure-Speicherbereich zu trennen.](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>Schritt 4: Erstellen Sie die Datei zur Zuordnung von PST-Import

Nachdem die PST-Dateien auf den Azure Speicherort für Ihre Office 365-Organisation hochgeladen wurden, wird im nächste Schritt erstellen Sie ein Komma getrennt Werten (CSV)-Datei, die die Benutzerpostfächer gibt die PST-Dateien zu importiert werden sollen. Sie können diese CSV-Datei im nächsten Schritt beim Erstellen einer PST-Importauftrag senden.
  
1. [Laden Sie eine Kopie der Zuordnungsdatei PST -Datei importieren](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
2. Öffnen oder speichern Sie die CSV-Datei auf Ihrem lokalen Computer. Das folgende Beispiel zeigt eine abgeschlossene PST-Importzuordnungsdatei (in Editor geöffnet). Es ist wesentlich einfacher, Microsoft Excel zum Bearbeiten der CSV-Datei zu verwenden.


    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,,annb.pst,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,annb_archive.pst,annb@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,,donh.pst,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,donh_archive.pst,donh@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,PSTFiles,pilarp.pst,pilarp@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,PSTFiles,pilarp_archive.pst,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,PSTFiles,tonyk.pst,tonyk@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,PSTFiles,tonyk_archive.pst,tonyk@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,PSTFiles,zrinkam.pst,zrinkam@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,PSTFiles,zrinkam_archive.pst,zrinkam@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    ```
    Die erste Zeile oder Kopfzeile der CSV-Datei enthält die Parameter, die vom Dienst PST-Datei importieren zum Importieren der PST-Dateien auf die Benutzerpostfächer verwendet werden. Jeder Parametername wird durch ein Komma getrennt. Jede Zeile unter der Überschrift stellt die Parameterwerte zum Importieren einer PST-Datei in ein bestimmtes Postfach. Sie benötigen eine Zeile für jeden PST-Datei, die Sie zu einem Benutzerpostfach importieren möchten. Achten Sie darauf, dass Sie die Platzhalterdaten in die Datei zur Zuordnung durch den tatsächlichen Daten ersetzen.

   **Hinweis:** Ändern Sie nichts die Kopfzeile, einschließlich der SharePoint-Parameter; Sie werden während des Importvorgangs PST ignoriert werden. 

 3. Verwenden Sie die Informationen in der folgenden Tabelle, um zu die CSV-Datei mit den erforderlichen Informationen zu füllen.


    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Gibt den Office 365-Dienst, dem Daten importiert werden. Verwenden Sie zum Importieren von PST-Dateien auf die Benutzerpostfächer `Exchange`.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Gibt den Speicherort des Ordners in den Azure Speicherort, dass Sie die PST-Dateien in Schritt2 auf hochgeladen.  <br/> Wenn Sie einen Unterordnernamen für die optionalen der SAS-URL im einschließen nicht die `/Dest:` Parameter in Schritt2, lassen Sie diesen Parameter leer in der CSV-Datei. Wenn Sie einen Unterordnernamen eingeschlossen, in diesem Parameter angeben (Siehe zweites Beispiel). Der Wert für diesen Parameter ist Groß-/Kleinschreibung beachtet.<br/> *In beiden Fällen nehmen "Ingestiondata" in den Wert für* die `FilePath` Parameter.  <br/><br/> **Wichtig:** Die Groß-/Kleinschreibung für den Namen der Pfad muss die gleiche wie die Groß-/Kleinschreibung Sie verwendet werden, wenn Sie einen Unterordnernamen für die optionalen in der SAS-URL in enthalten die `/Dest:` Parameter in Schritt2. Beispielsweise, wenn Sie verwendet `PSTFiles` für den Unterordner Namen Sie in Schritt2, und klicken Sie dann verwenden `pstfiles` in der `FilePath` schlägt fehl, Parameter in der CSV-Datei, die für die PST-Datei importieren. Achten Sie darauf, dass die Groß-/Kleinschreibung in beiden Fällen verwenden.<br/> |(leer lassen)  <br/> Oder  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |Gibt den Namen der PST-Datei, die für das Postfach des Benutzers importiert werden. Der Wert für diesen Parameter ist Groß-/Kleinschreibung beachtet.<br/> <br/>**Wichtig:** Die Groß-/Kleinschreibung für den Namen des PST-Datei in der CSV-Datei muss die gleiche wie die PST-Datei, die in der Azure Speicherort in Schritt2 hochgeladen wurde. Angenommen, Sie verwenden `annb.pst` in der `Name` Parameter in der CSV-Datei, aber der Name der PST-Datei ist `AnnB.pst`, schlägt der Import für die PST-Datei fehl. Stellen Sie sicher, dass der Name der PST-Datei in der CSV-Datei die gleiche Groß-/Kleinschreibung als die eigentliche PST-Datei verwendet wird.<br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |Gibt die e-Mail-Adresse des Postfachs an, das die PST-Datei importiert werden. Beachten Sie, dass Sie einen öffentlichen Ordner angeben ist nicht möglich, da der PST-Import-Dienst unterstützt Import von PST-Dateien auf Öffentliche Ordner.<br/> Um eine PST-Datei in eines inaktiven Postfachs zu importieren, müssen Sie die Postfach-GUID für diesen Parameter angeben. Um diese GUID zu erhalten, führen Sie den folgenden PowerShell-Befehl in Exchange Online: "Get-Mailbox <identity of inactive mailbox> - InactiveMailboxOnly | FL Guid` <br/> <br/>**Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox<identity of active mailbox> | FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-Mailbox <identity of soft-deleted or inactive mailbox> - SoftDeletedMailbox | FL Guid ".  <br/> | `annb@contoso.onmicrosoft.com` <br/> oder -  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Gibt an, ob die PST-Datei in das Archivpostfach des Benutzers importiert werden soll. Es gibt zwei Möglichkeiten:<br/><br/>**FALSE** - importiert die PST-Datei in primären Postfach des Benutzers.  <br/> **TRUE** - importiert die PST-Datei in das Postfach des Benutzers archivieren. Dies setzt voraus, dass das [Archivpostfach des Benutzers ist aktiviert](enable-archive-mailboxes.md).<br/><br/>Wenn Sie diesen Parameter auf setzen `TRUE` und Archivpostfach des Benutzers ist nicht aktiviert, schlägt der Import für diesen Benutzer fehl. Beachten Sie, dass, wenn ein Import für einen Benutzer ein Fehler auftritt (, da ihre Archiv ist nicht aktiviert, und diese Eigenschaft, um festgelegt wird `TRUE`), die andere Benutzer in den Importauftrag wird nicht beeinflusst werden.<br/>  Wenn Sie diesen Parameter leer lassen, wird die PST-Datei in der primären Postfach des Benutzers importiert.  <br/> <br/>**Hinweis:** Geben Sie einfach eine PST-Datei in einer Cloud-basierten Archivpostfach für einen Benutzer Sie zum Importieren, deren primäre Postfach der lokale ist `TRUE` für diesen Parameter, und geben Sie die e-Mail-Adresse für das Postfach des Benutzers: lokal für die `Mailbox` Parameter.  <br/> | `FALSE` <br/> oder -  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Gibt den Postfachordner, dem in die PST-Datei importiert wird.  <br/>  Wenn dieser Parameter leer lassen, wird die PST-Datei in einen neuen Ordner importiert werden benannten **importierte** auf der Stammebene des Postfachs (der gleichen Ebene wie der Ordner Posteingang und anderen standardmäßigen Postfachordner) befinden.  <br/>  Wenn Sie angeben `/`, Elemente in der PST-Datei importiert werden direkt im Ordner Posteingang des Benutzers.  <br/><br/>  Wenn Sie angeben `/<foldername>`, Elemente in der PST-Datei in einen Ordner namens importiert werden * \<Foldername\> * . Wenn Sie verwenden, beispielsweise `/ImportedPst`, würde Elemente in einen Ordner namens **ImportedPst**importiert werden. Dieser Ordner wird im Postfach des Benutzers auf derselben Ebene wie der Ordner Posteingang befinden.<br/><br/> **Tipp:** Berücksichtigen Sie mit ein paar Test Batches mit diesem Parameter experimentieren, damit Sie ermitteln können, die am besten geeigneten Speicherorte Ordner PST-Dateien zu importieren.  <br/> |(leer lassen)  <br/> Oder  <br/>  `/` <br/> oder -  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Dieser optionale Parameter gibt einen numerischen Wert für die Codepage für den Import von PST-Dateien im ANSI-Format verwenden. Dieser Parameter wird verwendet, für den Import von PST-Dateien von Organisationen Chinesisch, Japanisch und Koreanisch (CJK), da diese Sprachen in der Regel einen double-Byte-Zeichensatz (DBCS) für die zeichencodierung von verwenden. Wenn dieser Parameter wird nicht zum Importieren von PST-Dateien für Sprachen, die DBCS für Ordnernamen Postfach verwenden verwendet, werden die Namen der Ordner häufig verzerrt, nach dem Importieren.<br/><br/> Eine Liste der unterstützten Werte für diesen Parameter verwenden finden Sie unter [Code Seite Bezeichner](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> <br/>**Hinweis:** Wie bereits erwähnt, dies ist ein optionaler Parameter, und Sie keinen zum Einschließen in die CSV-Datei. Oder Sie können einschließen und den Wert für eine oder mehrere Zeilen leer lassen.<br/> |(leer lassen)  <br/> Oder  <br/>  `932`(Dies ist der Bezeichner für Japanisch ANSI/OEM-Seite)  <br/> |
    | `SPFileContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPManifestContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPSiteUrl` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>Schritt 5: Erstellen eines PST-Importauftrags in Office 365

Der nächste Schritt besteht darin den Importauftrag PST-Datei im Dienst Import in Office 365 erstellen. Wie bereits erklärt senden Sie die PST-Import-Zuordnung-Datei, die Sie in Schritt 4 erstellt haben. Nach der Erstellung neuen Auftrags Office 365 analysiert die Daten in die PST-Dateien, und klicken Sie dann bietet Ihnen eine Möglichkeit zum Filtern der Daten, die tatsächlich auf die Postfächer in die Datei zur Zuordnung von PST-Datei importieren angegebenen importiert dient zum Abrufen (siehe [Schritt 6](#step-6-filter-data-and-start-the-pst-import-job)).
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Steuerung** , und klicken Sie dann auf **Importieren**.
    
3. Klicken Sie auf der Seite **Importieren** auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Importauftrag neu**.
    
    **Hinweis:** Sie haben Zugriff auf die Seite **Importieren** in das Wertpapier die entsprechenden Berechtigungen zugewiesen werden &amp; Compliance Center, um einen neuen Importauftrag erstellen. Finden Sie weitere Informationen im Abschnitt **bevor Sie beginnen** . 
    
4. Geben Sie einen Namen für den Auftrag für Import von PST-Datei, und klicken Sie dann auf **Weiter**. Verwenden Sie Kleinbuchstaben, Zahlen, Bindestriche und Unterstriche. In Großbuchstabe können nicht oder Leerzeichen im Namen enthalten.
    
5. Klicken Sie auf die **möchten Sie hochladen oder Daten liefern?** Seite, klicken Sie auf **Hochladen die Daten** , und klicken Sie dann auf **Weiter**.
    
    ![Klicken Sie auf Hochladen, die Ihre Daten zum Erstellen eines Netzwerk-Uploads Auftrag importieren](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Klicken Sie in Schritt 4 auf der Seite **Daten importieren** auf die **habe ich meine Dateien hochladen** und **ich haben Zugriff auf die Datei zur Zuordnung** , Kontrollkästchen, und klicken Sie dann auf **Weiter**.
    
    ![Klicken Sie auf die zwei Kontrollkästchen in Schritt 4](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. Klicken Sie auf der Seite **Wählen Sie die Datei zur Zuordnung** auf **Zuordnungsdatei auswählen** , um die Datei zur Zuordnung von PST-Import zu senden, die Sie in Schritt 4 erstellt haben. 
    
    ![Klicken Sie auf Select Zuordnungsdatei, um die CSV-Datei, die Sie erstellt haben, für den Importauftrag übermitteln](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. Nach dem Namen des im CSV-Format Datei unter **Mapping-Dateiname**angezeigt wird, klicken Sie auf **Überprüfen** , um die CSV-Datei auf Fehler zu überprüfen. 
    
    ![Klicken Sie auf überprüfen, um die CSV-Datei für Fehler sicherzustellen.](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    Die CSV-Datei muss erfolgreich überprüft werden, um einen Auftrag für Import von PST-Datei zu erstellen. Beachten Sie, dass der Dateiname auf Grün geändert wird, nachdem es erfolgreich überprüft wird. Wenn die Überprüfung fehlschlägt, klicken Sie auf den Link **Protokoll anzeigen** . Eine Überprüfung Fehlerbericht wird mit einer Fehlermeldung für jede Zeile in der Datei geöffnet, die nicht erfolgreich. 
    
9. Nachdem die PST-Datei zur Zuordnung erfolgreich validiert wurde, lesen Sie die Geschäftsbedingungen, und klicken Sie dann auf das Kontrollkästchen.
    
10. Klicken Sie auf **Speichern** , um den Auftrag zu übermitteln, und klicken Sie dann auf **Schließen** , nachdem der Auftrag erfolgreich erstellt wurde. 
    
    Eine flyoutmenü Statusseite wird angezeigt, mit dem Status der **Analyse in Arbeit** und der neuen Importauftrag wird angezeigt, in der Liste auf der Seite **Importieren** . 
    
11. Klicken Sie auf **Aktualisieren**![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) , die Statusinformationen zu aktualisieren, die in der Spalte **Status** angezeigt wird. Wenn die Analyse abgeschlossen ist, und die Daten importiert werden können, wird der Status in der **Analyse abgeschlossen**geändert.
    
    Klicken Sie auf den Importauftrag zum Anzeigen der Seite Status flyoutmenü die enthält ausführlichere Informationen zu den Importauftrag wie beispielsweise der Status der einzelnen PST-Datei in der Zuordnungsdatei aufgeführt.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Schritt 6: Filtern von Daten, und starten Sie den Importauftrag PST-Datei

Nachdem Sie den Importauftrag in Schritt 5 erstellt haben, zur Analyse von Office 365 der Datenteils in die PST-Dateien (auf sichere Weise), identifiziert das Alter der Elemente und die verschiedenen Nachrichtentypen in PST-Dateien enthalten. Wenn die Analyse abgeschlossen ist, und die Daten zum Importieren bereit sind, Sie haben die Möglichkeit, alle Daten in die PST-Dateien importieren oder können Sie die Daten, die importiert wird durch Festlegen von Filtern, die steuern, welche Daten importierten ruft zuschneiden.
  
1. Auf der Seite **Importieren** in das Wertpapier &amp; Compliance Center, klicken Sie auf **bereit sind, zu Office 365 importieren** , für den Importauftrag, den Sie in Schritt 5 erstellt haben. 
    
    ![Klicken Sie auf kann jetzt zu Office 365 neben den Importauftrag importieren, die Sie erstellt haben.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Ausfliegen Seite wird mit Informationen zu den PST-Dateien und andere Informationen zu den Importauftrag angezeigt.
    
2. Klicken Sie auf der Seite flyoutmenü auf **Import zu Office 365**.
    
    Die Seite **Filtern die Daten** wird angezeigt. Sie enthält die Daten Einblicke in die resultierende aus der Analyse von Office 365, einschließlich Informationen über das Alter der Daten für die PST-Dateien ausgeführt. Zu diesem Zeitpunkt müssen Sie die Option zum Filtern der Daten, die importiert werden, oder importieren Sie die Daten unverändert. 
    
    ![Sie können erhöhen, die Daten in die PST-Dateien oder importieren Sie alle davon](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. Führen Sie einen der folgenden Schritte aus:
    
    a. zu erhöhen, die Daten, die Sie importieren möchten, klicken Sie auf **Ja, ich möchte vor dem Importieren von Filtern**.
    
    Ausführliche Anleitung zum Filtern der Daten in die PST-Dateien, und starten Sie den Importauftrag finden Sie unter [Filtern von Daten beim Import von PST-Dateien zu Office 365](filter-data-when-importing-pst-files.md).
    
    oder -
    
    b, um alle Daten in die PST-Dateien zu importieren, klicken Sie auf **Nein, ich möchte alles, importieren** , und klicken Sie auf **Weiter**.
    
4. Wenn Sie alle Daten importieren möchten, klicken Sie auf **Daten importieren** , um den Auftrag für Import starten. 
    
    Der Status des Importauftrags ist auf der Seite **Importieren** anzeigen. Klicken Sie auf ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) **Aktualisieren** , um die Statusinformationen zu aktualisieren, die in der Spalte **Status** angezeigt wird. Klicken Sie auf den Importauftrag zum Anzeigen der Seite Status flyoutmenü, die Statusinformationen für jedes zu importierenden PST-Datei angezeigt. 

## <a name="how-the-import-process-works"></a>Funktionsweise der Importvorgang
  
Die Option Netzwerk hochladen und den Dienst Office 365 importieren können Sie Massenimport-PST-Dateien für Benutzerpostfächer. Netzwerk-Upload bedeutet, dass Sie den PST-Dateien einen temporäre Speicherung Bereich in der Microsoft-Cloud hochladen. Klicken Sie dann kopiert der Import von Office 365-Dienst die PST-Dateien aus dem Speicherbereich an die Ziel-Benutzerpostfächer.
  
Nachfolgend finden Sie eine Abbildung und eine Beschreibung des Hochladens Netzwerk PST-Dateien auf Postfächer in Office 365 importieren.
  
![Workflow des Netzwerks hochladen Prozess zum Importieren von PST-Dateien nach Office 365](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **Download der PST-Datei importieren, Tools und auf private Schlüssel Azure Speicherort** - der erste Schritt besteht darin, laden Sie das Befehlszeilentool Azure AzCopy sowie eine Zugriffstaste verwendet, um die PST-Dateien an einem Speicherort Azure-Speicher in der Microsoft-Cloud hochladen. Sie erhalten diese auf der Seite **Importieren** , in die Office 365-Sicherheit &amp; Compliance Center. Der Schlüssel (einen sicheren Zugriff Signaturschlüssel (SAS) aufgerufen, bietet Ihnen die erforderlichen Berechtigungen zum Hochladen von PST-Dateien an einem privaten und Azure Speicherort sichern. Diese Tastenkombination ist in Ihrer Organisation eindeutig und verhindert nicht autorisierten Zugriff auf Ihre PST-Dateien nach dem Upload in die Microsoft-Cloud. Beachten Sie, dass das Importieren von PST-Dateien in Office 365 nicht Ihrer Organisation zu ein separates Azure-Abonnement verfügen muss. 
    
2. **Hochladen die PST-Dateien auf den Speicherort des Azure** - im nächsten Schritt besteht darin, die Verwendung des AzCopy.exe (in Schritt 1 heruntergeladen haben) hochladen und Speichern von PST-Dateien in ein Azure Speicherort, der sich im selben regionale Microsoft-Rechenzentrum befindet, in dem von Office 365 Organisation befindet. Wenn sie hochladen möchten, müssen die PST-Dateien, die Sie zu Office 365 importieren möchten in einer Dateifreigabe oder Dateiserver in Ihrer Organisation befinden.
    
    Beachten Sie, dass es ein optionaler Schritt, den Sie ausführen können ist, um die Liste der PST-Dateien nach dem Upload an den Speicherort der Azure-Speicher anzuzeigen.
    
3. **Erstellen eine PST-Datei importieren Zuordnungsdatei** - nach die PST-Dateien auf den Azure Speicherort hochgeladen wurden, besteht der nächste Schritt zum Erstellen einer Datei mit durch Kommas getrennten Werten (CSV), die angibt, welche Benutzerpostfächer PST-Dateien werden importiert werden, beachten Sie, dass eine PST-Datei werden kann  in der primären Postfach eines Benutzers oder ihrer Archivpostfach importiert. Importieren von Office 365-Dienst wird die Informationen in der CSV-Datei verwenden, um die PST-Dateien zu importieren.
    
4. **Erstellen einer PST-Datei importieren Job** - der nächste Schritt besteht darin, erstellen Sie einen Auftrag für Import von PST-Datei auf der Seite **Importieren** in das Wertpapier &amp; Compliance Center, und übermitteln Sie die PST-Datei importieren Zuordnungsdatei im vorherigen Schritt erstellt haben. Nachdem Sie den Importauftrag erstellt haben, ist Office 365 analysiert die Daten in die PST-Dateien und dann haben Sie Gelegenheit Filter festlegen, die steuern, welche Daten, auf die Postfächer in die Datei zur Zuordnung von PST-Datei importieren angegebenen importierten Ruft ab. 
    
5. **Filtern die PST-Daten, die auf Postfächer importiert werden sollen** – nach der Importauftrag erstellt und gestartet ist, analysiert Office 365 die Daten in die PST-Dateien (sicher und sichere) durch das Identifizieren von des Alters der Elemente und die verschiedenen Nachrichtentypen in PST-Dateien enthalten . Wenn die Analyse abgeschlossen ist, und die Daten zum Importieren bereit sind, Sie haben die Möglichkeit, alle Daten in die PST-Dateien importieren oder können Sie die Daten, die importiert wird durch Festlegen von Filtern, die steuern, welche Daten importierten ruft zuschneiden.
    
6. **Starten Sie den Auftrag für Import von PST** - nach der Importauftrag gestartet wird, verwendet Office 365 die Informationen in die Datei zur Zuordnung von PST-Datei importieren zum Importieren der PST-Dateien aus dem Azure IE-Speicherort für Benutzerpostfächer. Statusinformationen über den Importauftrag (einschließlich Informationen zu jeder zu importierenden PST-Datei) wird angezeigt, auf der Seite **Importieren** in das Wertpapier &amp; Compliance Center. Wenn der Auftrag für Import abgeschlossen ist, wird der Status für den Auftrag auf **Complete**festgelegt.
  
## <a name="more-information"></a>Weitere Informationen

- Warum Importieren von PST-Dateien in Office 365?
    
  - Es ist eine gute Möglichkeit, Archivdaten Ihrer Organisation in Office 365 zu importieren.
    
  - Die Daten sind für den Benutzer auf allen Geräten verfügbar, da sie in der Cloud gespeichert sind.
    
  - Adresse kompatibilitätsanforderungen Ihrer Organisation nützlich, um mit deren Hilfe Sie Office 365 Compliance-Features auf die Daten aus den PST-Dateien angewendet, die Sie importiert. Dazu gehören:
    
  - Aktivieren von [archivpostfächern](enable-archive-mailboxes.md) und [Archivierung automatisch erweitert](enable-unlimited-archiving.md) , um Benutzern erteilen zusätzliche Postfach Speicherplatz zum Speichern der Daten, die Sie importiert. 
    
  - Platzieren Postfächer, die Daten zu behalten, die Sie importiert [Aufbewahrung für eventuelle Rechtsstreitigkeiten](https://go.microsoft.com/fwlink/?linkid=856286) . 
    
  - Mithilfe von Microsoft [eDiscovery-Tools](search-for-content.md) um die Daten zu suchen, die Sie importiert haben. 
    
  - Verwenden von [Aufbewahrungsrichtlinien für Office 365](retention-policies.md) zu steuern, wie lange die Daten, die Sie importiert aufbewahrt werden sollen und welche Aktion erfolgen soll, nachdem der Aufbewahrungszeitraum abgelaufen ist. 
    
  - Suchen der [Office 365-Überwachungsprotokoll](search-the-audit-log-in-security-and-compliance.md) für Mailbox-bezogenen Ereignisse, die Einfluss auf die Daten, die Sie importiert. 
    
  - Importieren von Daten in [inaktiver Postfächer](create-and-manage-inactive-mailboxes.md) Daten aus Gründen der Einhaltung von Bestimmungen archiviert. 
    
  - Verwenden [Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md) , um zu verhindern, dass vertrauliche Daten außerhalb Ihrer Organisation verloren gehen. 
  
- Hier ist ein Beispiel für die gemeinsamen Zugriff Signatur (SAS)-URL, die in Schritt 1 ermittelt wird. Dieses Beispiel enthält auch die Syntax für den Befehl, den Sie zum Hochladen von PST-Dateien in Office 365 im Tool AzCopy.exe ausführen. Achten Sie darauf, müssen Sie Vorsichtsmaßnahmen gegen die SAS-URL zu schützen, genau wie Sie Kennwörter oder andere Sicherheitsinformationen zu schützen.

    ```
    SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D

    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y

    EXAMPLES

    This example uploads PST files to the root of the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
    
    This example uploads PST files to a subfolder named PSTFiles  in the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
``

- As previously explained, the Office 365 Import service turns on the retention hold setting (for an indefinite duration) after PST files are imported to a mailbox. This means the  *RetentionHoldEnabled*  property is set to  `True` so that the retention policy assigned to the mailbox won't be processed. This gives the mailbox owner time to manage the newly-imported messages by preventing a deletion or archive policy from deleting or archiving older messages. Here are some steps you can take to manage this retention hold: 
    
    - After a certain period of time, you can turn off the retention hold by running the  `Set-Mailbox -RetentionHoldEnabled $false` command. For instructions, see [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
   - You can configure the retention hold so that it's turned off on some date in the future. You do this by running the  `Set-Mailbox -EndDateForRetentionHold <date>` command. For example, assuming that today's date is July 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. In this scenario, you would leave the  *RetentionHoldEnabled*  property set to  *True*  . For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
   - You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    
