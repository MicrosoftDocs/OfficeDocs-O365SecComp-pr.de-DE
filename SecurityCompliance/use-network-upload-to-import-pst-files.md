---
title: Verwenden des Netzwerk Uploads zum Importieren Ihrer Organisations-PST-Dateien in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 103f940c-0468-4e1a-b527-cc8ad13a5ea6
description: 'Für Administratoren: Hier erfahren Sie, wie Sie mit dem Netzwerk Upload mehrere PST-Dateien in Benutzerpostfächer in Office 365 Massenimportieren.'
ms.openlocfilehash: fb64eecdbeac40aa597d17459f06525b8859fb1f
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156167"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>Verwenden des Netzwerk Uploads zum Importieren Ihrer Organisations-PST-Dateien in Office 365

> [!NOTE]
> Dieser Artikel richtet sich an Administratoren. Möchten Sie PST-Dateien in Ihr eigenes Postfach importieren? Siehe [Importieren von e-Mails, Kontakten und Kalendern aus einer Outlook. PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)
  
Hier finden Sie die Schritt-für-Schritt-Anleitungen, die für die Verwendung des Netzwerk Uploads zum Massenimport mehrerer PST-Dateien in Office 365 Postfächer erforderlich sind. Häufig gestellte Fragen zur Verwendung von Netzwerk Uploads zum Massenimport von PST-Dateien in Office 365 Postfächern finden Sie unter [FAQs für die Verwendung des Netzwerk Uploads zum Importieren von PST-Dateien](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files).
  
[Schritt 1: Kopieren der SAS-URL und Installieren von Azure AzCopy](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[Schritt 2: Hochladen der PST-Dateien in Office 365](#step-2-upload-your-pst-files-to-office-365)

[Optional Schritt 3: Anzeigen einer Liste der PST-Dateien, die in Office 365 hochgeladen wurden](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Schritt 4: Erstellen der PST-Import Zuordnungsdatei](#step-4-create-the-pst-import-mapping-file)

[Schritt 5: Erstellen eines PST-Import Auftrags in Office 365](#step-5-create-a-pst-import-job-in-office-365)

[Schritt 6: Filtern von Daten und Starten des PST-Import Auftrags](#step-6-filter-data-and-start-the-pst-import-job)

Beachten Sie, dass Sie Schritt 1 nur einmal ausführen müssen, um PST-Dateien in Office 365 Postfächer zu importieren. Nachdem Sie diese Schritte ausgeführt haben, befolgen Sie Schritt 2 bis Schritt 6 jedes Mal, wenn Sie einen Batch von PST-Dateien hochladen und importieren möchten.

## <a name="before-you-begin"></a>Bevor Sie beginnen
  
- Sie müssen in Exchange Online über die Rolle "Postfachimport export" verfügen, um PST-Dateien in Office 365 Postfächer zu importieren. Diese Rolle ist in Exchange Online standardmäßig keiner Rollengruppe zugewiesen. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" oder unter "Erstellen einer Rollengruppe" in [Verwalten von Rollengruppen](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Um außerdem Importaufträge im Security & Compliance Center zu erstellen, muss eine der folgenden Anforderungen erfüllt sein:
    
  - Sie müssen in Exchange Online die Rolle "e-Mail-Empfänger" zugewiesen haben. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Oder
    
  - Sie müssen ein globaler Administrator in Ihrer Office 365 Organisation sein.
    
  > [!TIP]
    > Sie sollten in Exchange Online eine neue Rollengruppe erstellen, die speziell für den Import von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie die Rollen "Postfachimport" und "e-Mail-Empfänger" für die für den Import von PST-Dateien erforderliche Mindeststufe von Berechtigungen der neuen Rollengruppe zu, und fügen Sie dann Mitglieder hinzu. 
  
- Die einzige unterstützte Methode zum Importieren von PST-Dateien in Office 365 besteht darin, das Azure AzCopy-Tool zu verwenden, wie in diesem Thema beschrieben. Sie können den Azure-Speicher-Explorer nicht verwenden, um PST-Dateien direkt in den Azure-Speicherbereich hochzuladen.
    
- Sie müssen die PST-Dateien, die Sie importieren möchten, in Office 365 auf einem Dateiserver oder einem freigegebenen Ordner in Ihrer Organisation speichern. In Schritt 2 führen Sie das Azure AzCopy-Tool aus, mit dem die PST-Dateien, die auf diesem Dateiserver oder freigegebenen Ordner gespeichert sind, in Office 365 hochgeladen werden.
    
- Bei diesem Verfahren wird eine Kopie einer URL kopiert und gespeichert, die eine Zugriffstaste enthält. Diese Informationen werden in Schritt 2 verwendet, um Ihre PST-Dateien hochzuladen, und in Schritt 3, wenn Sie eine Liste der PST-Dateien anzeigen möchten, die in Office 365 hochgeladen wurden. Achten Sie darauf, Vorkehrungen zu treffen, um diese URL wie Kennwörter oder andere sicherheitsrelevante Informationen zu schützen. Beispielsweise können Sie es in einem kennwortgeschützten Microsoft Word Dokument oder auf einem verschlüsselten USB-Laufwerk speichern. Ein Beispiel für diese kombinierte URL und den Schlüssel finden Sie im Abschnitt [Weitere Informationen](#more-information) . 
    
- Sie können PST-Dateien in ein inaktives Postfach in Office 365 importieren. Geben Sie dazu die GUID des inaktiven Postfachs im `Mailbox` Parameter in der PST-Import Zuordnungsdatei an. Weitere Informationen finden Sie in Schritt 4 auf der Registerkarte " **Anweisungen** " in diesem Thema. 
    
- In einer Exchange-hybridbereitstellung können Sie PST-Dateien in ein Cloud-basiertes Archivpostfach für einen Benutzer importieren, dessen primäres Postfach lokal ist. Führen Sie dazu in der PST-Import Zuordnungsdatei folgende Schritte aus:
    
  - Geben Sie die e-Mail-Adresse für das lokale Postfach des Benutzers `Mailbox` im Parameter an. 
    
  - Geben Sie den Wert **true** im `IsArchive` Parameter an. 
    
    Weitere Informationen finden Sie in [Schritt 4](#step-4-create-the-pst-import-mapping-file) . 
    
- Nachdem PST-Dateien in ein Office 365 Postfach importiert wurden, ist die Aufbewahrungsdauer für das Postfach auf unbestimmte Zeit aktiviert. Dies bedeutet, dass die dem Postfach zugewiesene Aufbewahrungsrichtlinie erst dann verarbeitet wird, wenn Sie die Aufbewahrungszeit deaktivieren oder ein Datum zum Deaktivieren des Haltestatus festlegen. Warum tun wir das? Wenn Nachrichten, die in ein Postfach importiert werden, alt sind, werden Sie möglicherweise endgültig gelöscht (bereinigt), da ihre Aufbewahrungsdauer auf der Grundlage der für das Postfach konfigurierten Aufbewahrungseinstellungen abgelaufen ist. Wenn Sie das Postfach in die Aufbewahrungszeit aufnehmen, erhält der Postfachbesitzer Zeit, diese neu importierten Nachrichten zu verwalten, oder Sie erhalten Zeit, um die Aufbewahrungseinstellungen für das Postfach zu ändern. Auf der Registerkarte **Weitere Informationen** in diesem Thema finden Sie Vorschläge zum Verwalten des Aufbewahrungs Speichers. 
    
- Standardmäßig beträgt die maximale Nachrichtengröße, die von einem Office 365 Postfach empfangen werden kann, 35 MB. Das liegt daran, dass der Standardwert für die *MaxReceiveSize* -Eigenschaft für ein Postfach auf 35 MB festgelegt ist. Der Grenzwert für die maximale Nachrichtenempfangs Größe in Office 365 beträgt jedoch 150 MB. Wenn Sie also eine PST-Datei importieren, die ein Element größer als 35 MB enthält Office 365, wird der Wert der MaxReceiveSize-Eigenschaft des Zielpostfachs automatisch in 150 MB geändert. Auf diese Weise können Nachrichten bis zu 150 MB in Benutzerpostfächer importiert werden. 
    
    > [!TIP]
    > Um die Nachrichtenempfangs Größe für ein Postfach zu identifizieren, können Sie diesen Befehl in Exchange Online PowerShell: `Get-Mailbox <user mailbox> | FL MaxReceiveSize`ausführen. 

## <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>Schritt 1: Kopieren der SAS-URL und Installieren von Azure AzCopy

Der erste Schritt besteht darin, das Azure AzCopy-Tool herunterzuladen und zu installieren, das das Tool ist, das Sie in Schritt 2 ausführen müssen, um PST-Dateien in Office 365 hochzuladen. Außerdem kopieren Sie die SAS-URL für Ihre Organisation. Diese URL ist eine Kombination aus der Netzwerk-URL für den Azure-Speicherort in der Microsoft-Cloud für Ihre Organisation und einem SAS-Schlüssel (Shared Access Signature). Dieser Schlüssel bietet Ihnen die erforderlichen Berechtigungen zum Hochladen von PST-Dateien an Ihren Azure-Speicherort. Achten Sie darauf, Vorkehrungen zu treffen, um die SAS-URL zu schützen. Sie ist für Ihre Organisation eindeutig und wird in Schritt 2 verwendet.

> [!IMPORTANT]
> Zum Importieren von PST-Dateien mithilfe der Network Upload-Methode wird empfohlen, dass Sie die Version von Azure AzCopy verwenden, die in Schritt 6B im folgenden Verfahren heruntergeladen werden kann.
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Ihrer Office 365 Organisation an. 
    
2. Klicken Sie im linken Bereich des Security & Compliance Center auf **Data Governance** \> **Import**.
    
    > [!NOTE]
    > Ihnen müssen die entsprechenden Berechtigungen für den Zugriff auf die **Import** Seite im Security & Compliance Center zugewiesen werden. Weitere Informationen finden Sie im Abschnitt **bevor Sie beginnen** . 
    
3. Klicken Sie **** ![auf der Seite importieren auf Symbol](media/ITPro-EAC-AddIcon.gif) **neuer Importauftrag**hinzufügen.
    
    Der Assistent zum Importieren von Aufträgen wird angezeigt.
    
4. Geben Sie einen Namen für den PST-Importauftrag ein, und klicken Sie dann auf **weiter**. Verwenden Sie Kleinbuchstaben, Zahlen, Bindestriche und Unterstriche. Sie können keine Großbuchstaben verwenden oder Leerzeichen im Namen einschließen.
    
5. Klicken Sie auf der Seite möchten **Sie Daten hochladen oder versenden?** auf **Daten hochladen** , und klicken Sie dann auf **weiter**.
    
    ![Klicken Sie auf Daten hochladen, um einen Importauftrag für Netzwerk Uploads zu erstellen.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Führen Sie auf der Seite **Daten importieren** die folgenden zwei Schritte aus: 
    
    ![Kopieren Sie die SAS-URL, und laden Sie das Azure AzCopy-Tool auf der Seite Daten importieren herunter.](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    a. Klicken Sie in Schritt 2 auf **Netzwerk-Upload-SAS-URL anzeigen**. Nachdem die SAS-URL angezeigt wurde, klicken Sie auf **in die Zwischenablage kopieren** und anschließend in eine Datei einfügen und speichern, damit Sie später darauf zugreifen können.
    
    b. Klicken Sie in Schritt 3 auf **Azure AzCopy herunterladen** , um das Azure AzCopy-Tool herunterzuladen und zu installieren. Klicken Sie im Popupfenster auf **Ausführen** , um AzCopy zu installieren. 
    
> [!NOTE]
> Sie können die Seite **Daten importieren** geöffnet lassen (falls Sie die SAS-URL erneut kopieren müssen) oder auf **Abbrechen** klicken, um Sie zu schließen. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>Schritt 2: Hochladen der PST-Dateien in Office 365

Jetzt können Sie das AzCopy. exe-Tool verwenden, um PST-Dateien in Office 365 hochzuladen. Dieses Tool lädt und speichert Sie an einem Azure-Speicherort in der Microsoft-Cloud. Wie bereits erläutert, befindet sich der Azure-Speicherort, an den Sie Ihre PST-Dateien hochgeladen haben, in demselben regionalen Microsoft-Rechenzentrum, in dem sich Ihre Office 365 Organisation befindet. Damit Sie diesen Schritt ausführen können, müssen sich die PST-Dateien in einer Dateifreigabe oder auf einem Dateiserver in Ihrer Organisation befinden. Im folgenden Verfahren wird dies als das Quellverzeichnis bezeichnet. Jedes Mal, wenn Sie das AzCopy-Tool ausführen, können Sie ein anderes Quellverzeichnis angeben. 
  
1. Öffnen Sie eine Eingabeaufforderung auf dem lokalen Computer.
    
2. Wechseln Sie zu dem Verzeichnis, in dem Sie das Tool AzCopy. exe in Schritt 1 installiert haben. Wenn Sie das Tool am Standardspeicherort installiert haben, wechseln Sie `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`zu.
    
3. Führen Sie den folgenden Befehl aus, um die PST-Dateien in Office 365 hochzuladen.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    > [!IMPORTANT] 
    > Sie müssen im vorherigen Befehl ein Verzeichnis als Quellspeicherort angeben. Sie können keine individuelle PST-Datei angeben. Alle PST-Dateien im Quellverzeichnis werden hochgeladen.
 
    In der folgenden Tabelle werden die Parameter AzCopy. exe und die erforderlichen Werte beschrieben. Die Informationen, die Sie im vorherigen Schritt erhalten haben, werden in den Werten für diese Parameter verwendet.
    
    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Gibt das Quellverzeichnis in Ihrer Organisation an, das die PST-Dateien enthält, die in Office 365 hochgeladen werden.  <br/> Stellen Sie sicher, dass Sie den Wert dieses Parameters mit doppelten Anführungszeichen ("") umgeben.  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |Gibt die SAS-URL an, die Sie in Schritt 1 erhalten haben.  <br/> Stellen Sie sicher, dass Sie den Wert dieses Parameters mit doppelten Anführungszeichen ("") umgeben.  <br/> **Tipp:** Optional Sie können einen Unterordner im Azure-Speicher Speicherort angeben, in den die PST-Dateien hochgeladen werden sollen. Hierzu fügen Sie in der SAS-URL einen Speicherort des Unterordners (nach "ingestiondata") hinzu. Im ersten Beispiel wird kein Unterordner angegeben. Das bedeutet, dass das PST in den Stamm (namens *ingestiondata* ) des Azure-Speicherorts hochgeladen wird. Das zweite Beispiel lädt die PST-Dateien in einen Unterordner (mit dem Namen *PSTFiles* ) im Stammverzeichnis des Azure-Speicherorts hoch.  <br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> Oder  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |Gibt ausführliche Statusmeldungen in eine Protokolldatei aus. Standardmäßig wird die ausführliche Protokolldatei mit dem Namen AzCopyVerbose. Log in%LocalAppData%\Microsoft\Azure\AzCopy. Wenn Sie einen vorhandenen Dateispeicherort für diese Option angeben, wird das ausführliche Protokoll an diese Datei angefügt.  <br/> Stellen Sie sicher, dass Sie den Wert dieses Parameters mit doppelten Anführungszeichen ("") umgeben.  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |Diese optionale Option gibt den rekursiven Modus an, sodass das AzCopy-Tool PST-Dateien kopiert, die sich in Unterordnern im Quellverzeichnis befinden, das durch den `/Source:` -Parameter angegeben wird.  <br/> **Hinweis:** Wenn Sie diesen Switch verwenden, werden PST-Dateien in Unterordnern nach dem Hochladen einen anderen Dateipfadname am Azure-Speicherort haben. Sie müssen den genauen Dateipfadname in der CSV-Datei angeben, die Sie in Schritt 4 erstellen.  <br/> | `/S` <br/> |
    | `/Y` <br/> |Diese erforderliche Option ermöglicht die Verwendung von schreibgeschützten SAS-Token, wenn Sie die PST-Dateien an den Azure-Speicherort hochladen. Die SAS-URL, die Sie in Schritt 1 (und `/Dest:` in Parameter angegeben) erhalten haben, ist eine schreibgeschützte SAS-URL, weshalb Sie diese Option einbeziehen müssen. Beachten Sie, dass eine schreibgeschützte SAS-URL nicht verhindert, dass Sie den Azure-Speicher-Explorer verwenden, um eine Liste der PST-Dateien anzuzeigen, die in den Azure-Speicherort hochgeladen werden.  <br/> | `/Y` <br/> |
   
Im folgenden finden Sie ein Beispiel für die Syntax für das Tool AzCopy. exe unter Verwendung der tatsächlichen Werte für die einzelnen Parameter:
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

Nachdem Sie den Befehl ausgeführt haben, werden Statusmeldungen angezeigt, die den Fortschritt des Uploads der PST-Dateien anzeigen. Eine abschließende Statusmeldung zeigt die Gesamtzahl der Dateien an, die erfolgreich hochgeladen wurden.

> [!TIP]
> Nachdem Sie den Befehl AzCopy. exe erfolgreich ausgeführt und sichergestellt haben, dass alle Parameter korrekt sind, speichern Sie eine Kopie der Befehlszeilensyntax in derselben (gesicherten) Datei, in der Sie die Informationen kopiert haben, die Sie in Schritt 1 erhalten haben. Anschließend können Sie diesen Befehl jedes Mal kopieren und in eine Eingabeaufforderung einfügen, wenn Sie das Tool AzCopy. exe ausführen möchten, um PST-Dateien in Office 365 hochzuladen. Der einzige Wert, den Sie möglicherweise ändern müssen, sind `/Source:` diejenigen für den Parameter. Dies hängt vom Quellverzeichnis ab, in dem sich die PST-Dateien befinden.

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Optional Schritt 3: Anzeigen einer Liste der PST-Dateien, die in Office 365 hochgeladen wurden

Als optionalen Schritt können Sie den Microsoft Azure Speicher-Explorer (ein kostenloses Open-Source-Tool) installieren und verwenden, um die Liste der PST-Dateien anzuzeigen, die Sie in das Azure-BLOB hochgeladen haben. Hierfür gibt es zwei gute Gründe:
  
- Stellen Sie sicher, dass PST-Dateien aus dem freigegebenen Ordner oder Dateiserver in Ihrer Organisation erfolgreich in das Azure-BLOB hochgeladen wurden.
    
- Überprüfen Sie für jede PST-Datei, die in das Azure-BLOB hochgeladen wurde, den Dateinamen (und den Unterordner Pfadnamen, wenn Sie einen enthalten). Dies ist wirklich hilfreich, wenn Sie die PST-Zuordnungsdatei im nächsten Schritt erstellen, da Sie sowohl den Ordner Pfadnamen als auch den Dateinamen für jede PST-Datei angeben müssen. Die Überprüfung dieser Namen kann dazu beitragen, mögliche Fehler in Ihrer PST-Zuordnungsdatei zu verringern.
    
Der Microsoft Azure Speicher-Explorer befindet sich in der Vorschau.
  
> [!IMPORTANT]
> Sie können den Azure-Speicher-Explorer nicht zum Hochladen oder Ändern von PST-Dateien verwenden. Die einzige unterstützte Methode zum Importieren von PST-Dateien in Office 365 ist die Verwendung von AzCopy. Außerdem können Sie keine PST-Dateien löschen, die Sie in das Azure-BLOB hochgeladen haben. Wenn Sie versuchen, eine PST-Datei zu löschen, wird eine Fehlermeldung angezeigt, in der Sie darauf hingewiesen werden, dass Sie nicht über die erforderlichen Berechtigungen verfügen. Beachten Sie, dass alle PST-Dateien automatisch aus Ihrem Azure-Speicherbereich gelöscht werden. If there are no import jobs in progress, then all PST files in the **ingestiondata** container are deleted 30 days after the most recent import job was created.
  
So installieren Sie den Azure Storage-Explorer und stellen eine Verbindung mit Ihrem Azure-Speicherbereich her:
  
1. Laden Sie das [Tool Microsoft Azure Storage Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842)herunter, und installieren Sie es.
    
2. Starten Sie den Microsoft Azure Speicher-Explorer, klicken Sie im linken Bereich mit der rechten Maustaste auf **Speicherkonten** , und klicken Sie dann auf mit **Azure-Speicher verbinden**.
    
    ![Klicken Sie mit der rechten Maustaste auf Speicherkonten, und klicken Sie dann auf mit Azure Storage verbinden](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Klicken Sie auf **einen SAS-URI (Shared Access Signature) oder eine Verbindungszeichenfolge verwenden** , und klicken Sie auf **weiter**.
    
4. Klicken Sie auf **SAS-URI verwenden**, fügen Sie die in Schritt 1 abgerufene SAS-URL in das Feld unter **URI**ein, und klicken Sie dann auf **weiter**.
    
5. Auf der Seite zusammen **Fassung der Verbindung** können Sie die Verbindungsinformationen überprüfen und dann auf **verbinden**klicken.
    
    Der **ingestiondata** -Container wird geöffnet; Sie enthält die PST-Dateien, die Sie in Schritt 2 hochgeladen haben. Der **ingestiondata** -Container befindet sich unter **Speicherkonten** \> **(SAS-Attached Services)** \> **BLOB-Container**. 
    
    ![Azure Storage Explorer zeigt eine Liste der PST-Dateien an, die Sie hochgeladen haben.](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Wenn Sie mit dem Microsoft Azure Speicher-Explorer fertig sind, klicken Sie mit der rechten Maustaste auf **ingestiondata**, und klicken Sie dann auf **trennen** , um die Verbindung mit dem Azure-Speicherbereich zu trennen. Andernfalls erhalten Sie eine Fehlermeldung, wenn Sie das nächste Mal versuchen anzufügen. 
    
    ![Klicken Sie mit der rechten Maustaste auf die Einnahme, und klicken Sie auf trennen, um die Verbindung mit Ihrem Azure-Speicherbereich](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>Schritt 4: Erstellen der PST-Import Zuordnungsdatei

Nachdem die PST-Dateien in den Azure-Speicherort für Ihre Office 365 Organisation hochgeladen wurden, besteht der nächste Schritt darin, eine CSV-Datei (Comma Separated Value) zu erstellen, in der die Benutzerpostfächer angegeben werden, in die die PST-Dateien importiert werden. Sie werden diese CSV-Datei im nächsten Schritt übermitteln, wenn Sie einen PST-Import Auftrag erstellen.
  
1. [Laden Sie eine Kopie der PST-Import Zuordnungsdatei herunter](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
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
    Die erste Zeile oder Kopfzeile der CSV-Datei enthält die Parameter, die vom PST-Importdienst verwendet werden, um die PST-Dateien in Benutzerpostfächer zu importieren. Die einzelnen Parameternamen werden jeweils durch ein Komma getrennt. Jede Zeile unter der Kopfzeile stellt die Parameterwerte für das Importieren einer PST-Datei in ein bestimmtes Postfach dar. Sie benötigen eine Zeile für jede PST-Datei, die in ein Benutzerpostfach importiert werden soll. Vergessen Sie nicht, die Platzhalterdaten in der Zuordnungsdatei durch die tatsächlichen Werte zu ersetzen.

   **Hinweis:** Ändern Sie nichts in der Kopfzeile, einschließlich der SharePoint-Parameter; Sie werden während des PST-Import Vorgangs ignoriert. 

 3. Verwenden Sie die Informationen in der folgenden Tabelle, um zu die CSV-Datei mit den erforderlichen Informationen zu füllen.


    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Gibt den Office 365 Dienst an, in den Daten importiert werden. Um PST-Dateien in Benutzerpostfächer zu importieren `Exchange`, verwenden Sie.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Gibt den Speicherort des Ordners am Azure-Speicherort an, an den Sie die PST-Dateien in Schritt 2 hochgeladen haben.  <br/> Wenn Sie keinen optionalen Unterordnernamen in die SAS-URL des `/Dest:` Parameters in Schritt 2 aufgenommen haben, lassen Sie diesen Parameter in der CSV-Datei leer. Wenn Sie einen Unterordnernamen angegeben haben, geben Sie ihn in diesem Parameter an (siehe zweites Beispiel). Bei dem Wert für diesen Parameter wird die Groß-/Kleinschreibung beachtet.  <br/> Verwenden Sie in beiden Fällen *nicht* "ingestiondata" in den Wert des `FilePath` Parameters.  <br/><br/> **Wichtig:** Der Fall des Datei Pfadnamens muss mit dem Fall identisch sein, den Sie verwendet haben, wenn Sie einen optionalen Unterordnernamen in die SAS- `/Dest:` URL im Parameter in Schritt 2 aufgenommen haben. Wenn Sie beispielsweise den Namen `PSTFiles` des Unterordners in Schritt 2 verwendet haben und dann `pstfiles` im Parameter `FilePath` in der CSV-Datei verwenden, tritt beim Import für die PST-Datei ein Fehler auf. Achten Sie darauf, dass Sie in beiden Fällen denselben Fall verwenden.  <br/> |(leer lassen)  <br/> Oder  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |Gibt den Namen der PST-Datei an, die in das Benutzerpostfach importiert wird.  Bei dem Wert für diesen Parameter wird die Groß-/Kleinschreibung beachtet.  <br/> <br/>**Wichtig:** Der Fall für den Namen der PST-Datei in der CSV-Datei muss mit der PST-Datei identisch sein, die in Schritt 2 in den Azure-Speicherort hochgeladen wurde. Wenn Sie beispielsweise im- `annb.pst` `Name` Parameter in der CSV-Datei verwenden, aber der Name der tatsächlichen PST-Datei lautet `AnnB.pst`, tritt beim Import für diese PST-Datei ein Fehler auf. Stellen Sie sicher, dass der Name der PST-Datei in der CSV-Datei den gleichen Fall wie die tatsächliche PST-Datei verwendet.  <br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |Gibt die E-Mail-Adresse des Postfachs an, in das die PST-Datei importiert werden soll.  Beachten Sie, dass Sie keinen öffentlichen Ordner angeben können, da der PST-Importdienst keine Unterstützung f+r das Importieren von PST-Dateien in öffentlichen Ordnern bietet.  <br/> Um eine PST-Datei in ein inaktives Postfach zu importieren, müssen Sie die Postfach-GUID für diesen Parameter angeben. Um diese GUID zu erhalten, führen Sie den folgenden PowerShell-Befehl in Exchange Online aus:`Get-Mailbox <identity of inactive mailbox> -InactiveMailboxOnly | FL Guid` <br/> <br/>**Hinweis:** In einigen Fällen verfügen Sie möglicherweise über mehrere Postfächer mit derselben e-Mail-Adresse, wobei ein Postfach ein aktives Postfach ist und sich das andere Postfach in einem weichen-gelöschten (oder inaktiven) Status befindet. In diesen Situationen müssen Sie die Postfach-GUID angeben, um das Postfach, in das die PST-Datei importiert werden soll, eindeutig zu identifizieren. Führen Sie den folgenden PowerShell-Befehl aus, um diese GUID für aktive `Get-Mailbox <identity of active mailbox> | FL Guid`Postfächer zu erhalten:. Um die GUID für vorläufig gelöschte (oder inaktive) Postfächer zu erhalten, `Get-Mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`führen Sie diesen Befehl aus.  <br/> | `annb@contoso.onmicrosoft.com` <br/> Oder  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Gibt an, ob die PST-Datei in das Archivpostfach des Benutzers importiert werden soll. Es gibt zwei Möglichkeiten:  <br/><br/>**False** – importiert die PST-Datei in das primäre Postfach des Benutzers.  <br/> **True** : importiert die PST-Datei in das Archivpostfach des Benutzers. This assumes that the [user's archive mailbox is enabled](enable-archive-mailboxes.md). <br/><br/>Wenn Sie diesen Parameter auf `TRUE` festlegen und das Archivpostfach des Benutzers nicht aktiviert ist, tritt beim Import für diesen Benutzer ein Fehler auf. Beachten Sie, dass beim Fehlschlagen eines Imports für einen Benutzer (da das Archiv nicht aktiviert ist `TRUE`und diese Eigenschaft auf festgelegt ist) die anderen Benutzer im Importauftrag nicht betroffen sind.  <br/>  If you leave this parameter blank, the PST file is imported to the user's primary mailbox.  <br/> <br/>**Hinweis:** Wenn Sie eine PST-Datei in ein Cloud-basiertes Archivpostfach für einen Benutzer importieren möchten, dessen primäres Postfach lokal `TRUE` ist, geben Sie für diesen Parameter einfach an, und geben Sie die e-Mail- `Mailbox` Adresse für das lokale Postfach des Benutzers für den Parameter an.  <br/> | `FALSE` <br/> Oder  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Gibt den Postfachordner an, in den die PST-Datei importiert wird.  <br/>  Wenn Sie diesen Parameter leer lassen, wird die PST-Datei in einen neuen Ordner mit **** dem Namen "imported" importiert, der sich auf der Stammebene des Postfachs befindet (die gleiche Ebene wie der Posteingangsordner und die anderen standardmäßigen Postfachordner).  <br/>  Wenn Sie angeben `/`, werden Elemente in der PST-Datei direkt in den Posteingangsordner des Benutzers importiert.  <br/><br/>  Wenn Sie angeben `/<foldername>`, werden Elemente in der PST-Datei in einen Ordner mit dem Namen * \<\> FolderName* importiert. Wenn Sie beispielsweise verwenden `/ImportedPst`, werden Elemente in einen Ordner mit dem Namen **ImportedPst**importiert. Dieser Ordner befindet sich im Postfach des Benutzers auf derselben Ebene wie der Posteingangsordner.  <br/><br/> **Tipp:** Sie sollten einige Test Batches durchführen, um mit diesem Parameter zu experimentieren, damit Sie den Speicherort für den besten Ordner zum Importieren von PST-Dateien ermitteln können.  <br/> |(leer lassen)  <br/> Oder  <br/>  `/` <br/> Oder  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Dieser optionale Parameter gibt einen numerischen Wert für die Codepage an, die zum Importieren von PST-Dateien im ANSI-Dateiformat verwendet werden soll. Dieser Parameter wird zum Importieren von PST-Dateien aus chinesischen, japanischen und koreanischen Organisationen (CJK) verwendet, da diese Sprachen in der Regel einen Doppelbyte-Zeichensatz (DBCS) für die Zeichencodierung verwenden. Wenn dieser Parameter nicht zum Importieren von PST-Dateien für Sprachen verwendet wird, die DBCS für Postfachordner Namen verwenden, werden die Ordnernamen nach dem Import häufig verstümmelt.  <br/><br/> Eine Liste der unterstützten Werte, die für diesen Parameter verwendet werden sollen, finden Sie unter [Code Page Identifiers](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> <br/>**Hinweis:** Wie bereits erwähnt, ist dies ein optionaler Parameter, den Sie nicht in die CSV-Datei einschließen müssen. Oder Sie können ihn einschließen und den Wert für eine oder mehrere Zeilen leer lassen.  <br/> |(leer lassen)  <br/> Oder  <br/>  `932`(Dies ist der Codepagebezeichner für ANSI/OEM Japanisch)  <br/> |
    | `SPFileContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPManifestContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPSiteUrl` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>Schritt 5: Erstellen eines PST-Import Auftrags in Office 365

Im nächsten Schritt erstellen Sie den PST-Importauftrag im Import Dienst in Office 365. Wie bereits erläutert, übermitteln Sie die PST-Import Zuordnungsdatei, die Sie in Schritt 4 erstellt haben. Nachdem Sie den neuen Auftrag erstellt haben, analysiert Office 365 die Daten in den PST-Dateien und gibt Ihnen dann die Möglichkeit, die Daten zu filtern, die tatsächlich in die in der PST-Import Zuordnungsdatei angegebenen Postfächer importiert werden (siehe [Schritt 6](#step-6-filter-data-and-start-the-pst-import-job)).
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Ihrer Office 365 Organisation an. 
    
2. Klicken Sie im linken Bereich des Security & Compliance Center auf **Data Governance** , und klicken Sie dann auf **importieren**.
    
3. Klicken Sie **** ![auf der Seite importieren auf Symbol](media/ITPro-EAC-AddIcon.gif) **neuer Importauftrag**hinzufügen.
    
    **Hinweis:** Sie müssen die entsprechenden Berechtigungen für den Zugriff auf die **Import** Seite im Security & Compliance Center erhalten, um einen neuen Importauftrag zu erstellen. Weitere Informationen finden Sie im Abschnitt **bevor Sie beginnen** . 
    
4. Geben Sie einen Namen für den PST-Importauftrag ein, und klicken Sie dann auf **weiter**. Verwenden Sie Kleinbuchstaben, Zahlen, Bindestriche und Unterstriche. Sie können keine Großbuchstaben verwenden oder Leerzeichen im Namen einschließen.
    
5. Klicken Sie auf der Seite möchten **Sie Daten hochladen oder versenden?** auf **Daten hochladen** , und klicken Sie dann auf **weiter**.
    
    ![Klicken Sie auf Daten hochladen, um einen Importauftrag für Netzwerk Uploads zu erstellen.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Klicken Sie in Schritt 4 auf der Seite **Daten importieren** auf die Kontrollkästchen **Ich bin fertig, meine Dateien hochzuladen** , und **Ich habe Zugriff auf die Zuordnungsdatei** , und klicken Sie dann auf **weiter**.
    
    ![Aktivieren Sie die beiden Kontrollkästchen in Schritt 4.](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. Klicken Sie auf der Seite **Zuordnungsdatei auswählen** auf **Zuordnungsdatei auswählen** , um die in Schritt 4 erstellte PST-Import Zuordnungsdatei zu übermitteln. 
    
    ![Klicken Sie auf Zuordnungsdatei auswählen, um die CSV-Datei zu übermitteln, die Sie für den Importauftrag erstellt haben.](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. Nachdem der Name der CSV-Datei unter **Name der Zuordnungsdatei**angezeigt wird **** , klicken Sie auf überprüfen, um die CSV-Datei auf Fehler zu überprüfen. 
    
    ![Klicken Sie auf überprüfen, um die CSV-Datei auf Fehler zu überprüfen](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    Die CSV-Datei muss erfolgreich überprüft werden, um einen PST-Import Auftrag zu erstellen. Hinweis der Dateiname wird nach der erfolgreichen Validierung in Grün geändert. Wenn die Überprüfung fehlschlägt, klicken Sie auf den Link **Protokoll anzeigen** . Es wird ein Validierungsfehler Bericht mit einer Fehlermeldung für jede Zeile in der Datei geöffnet, die fehlgeschlagen ist. 
    
9. Nachdem die PST-Zuordnungsdatei erfolgreich überprüft wurde, lesen Sie das Dokument mit den allgemeinen Geschäftsbedingungen, und klicken Sie dann auf das Kontrollkästchen.
    
10. Klicken Sie auf **Speichern** , um den Auftrag zu übermitteln, und klicken Sie dann auf **Schließen** , nachdem der Auftrag erfolgreich erstellt wurde. 
    
    Eine Status Flyout-Seite wird angezeigt, wobei der Status der **Analyse in Bearbeitung** ist und der neue Importauftrag in der Liste auf der Seite **importieren** angezeigt wird. 
    
11. Klicken Sie auf Aktualisierungs](media/O365-MDM-Policy-RefreshIcon.gif) Symbol aktualisieren, um die Statusinformationen zu aktualisieren, die in der Spalte **Status** angezeigt werden. **** ![ Wenn die Analyse abgeschlossen ist und die Daten importiert werden können, wird der Status in **Analyse abgeschlossen**geändert.
    
    Sie können auf den Importauftrag klicken, um die Status-Flyout-Seite anzuzeigen, die ausführlichere Informationen zum Importauftrag enthält, beispielsweise den Status jeder PST-Datei, die in der Zuordnungsdatei aufgeführt ist.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Schritt 6: Filtern von Daten und Starten des PST-Import Auftrags

Nachdem Sie den Importauftrag in Schritt 5 erstellt haben, analysiert Office 365 die Daten in den PST-Dateien (auf sichere und sichere Weise), indem das Alter der Elemente und die unterschiedlichen Nachrichtentypen, die in den PST-Dateien enthalten sind, identifiziert werden. Wenn die Analyse abgeschlossen ist und die Daten importiert werden können, haben Sie die Möglichkeit, alle in den PST-Dateien enthaltenen Daten zu importieren oder die importierten Daten zu trimmen, indem Sie Filter festlegen, mit denen gesteuert wird, welche Daten importiert werden.
  
1. Klicken Sie auf der Seite **importieren** im Security & Compliance Center auf **Ready to Import to Office 365** für den Importauftrag, den Sie in Schritt 5 erstellt haben. 
    
    ![Klicken Sie auf Ready to Import to Office 365 neben dem von Ihnen erstellten Importauftrag.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Eine Ausklappseite wird mit Informationen über die PST-Dateien und andere Informationen zum Importauftrag angezeigt.
    
2. Klicken Sie auf der Seite Flyout auf **Importieren in Office 365**.
    
    Die Seite **Daten filtern** wird angezeigt. Sie enthält die Daten Insights, die sich aus der Analyse ergeben, die für die PST-Dateien von Office 365 durchgeführt wurde, einschließlich Informationen zum Alter der Daten. Zu diesem Zeitpunkt haben Sie die Möglichkeit, die Daten zu filtern, die importiert werden, oder alle Daten zu importieren. 
    
    ![Sie können die Daten in den PST-Dateien kürzen oder alles importieren.](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. Führen Sie einen der folgenden Schritte aus:
    
    a. Um die importierten Daten zu trimmen, klicken Sie auf **Ja, ich möchte Sie vor dem Importieren Filtern**.
    
    Ausführliche Schritt-für-Schritt-Anweisungen zum Filtern der Daten in den PST-Dateien und zum Starten des importauftrags finden Sie unter [Filtern von Daten beim Importieren von PST-Dateien in Office 365](filter-data-when-importing-pst-files.md).
    
    Oder
    
    b. Wenn Sie alle Daten in den PST-Dateien importieren möchten, klicken Sie auf **Nein, ich möchte alles importieren,** und klicken Sie dann auf **weiter**.
    
4. Wenn Sie alle Daten importiert haben, klicken Sie auf **Daten importieren** , um den Importauftrag zu starten. 
    
    Der Status des importauftrags wird auf der Seite " **importieren** " angezeigt. Klicken ![Sie auf](media/O365-MDM-Policy-RefreshIcon.gif) Aktualisierungssymbol **Aktualisieren** , um die Statusinformationen zu aktualisieren, die in der Spalte **Status** angezeigt werden. Klicken Sie auf den Importauftrag, um die Status-Flyout-Seite anzuzeigen, in der Statusinformationen zu den importierten PST-Dateien angezeigt werden. 

## <a name="how-the-import-process-works"></a>Funktionsweise des Importvorgangs
  
Sie können die Option "Netzwerk Upload" und den Office 365 Import-Dienst verwenden, um PST-Dateien in Benutzerpostfächer zu Massenimportieren. Netzwerk Upload bedeutet, dass Sie die PST-Dateien in einen temporären Speicherbereich in der Microsoft-Cloud hochladen. Anschließend kopiert der Office 365-Import Dienst die PST-Dateien aus dem Speicherbereich in die Zielbenutzer Postfächer.
  
Im folgenden finden Sie eine Abbildung und eine Beschreibung des Netzwerk Upload-Prozesses zum Importieren von PST-Dateien in Postfächer in Office 365.
  
![Workflow des Netzwerk-Upload-Prozesses zum Importieren von PST-Dateien in Office 365](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **Laden Sie das PST-Import Tool und den Schlüssel zum privaten Azure-Speicherplatz herunter** – der erste Schritt besteht darin, das Azure AzCopy-Befehlszeilentool und eine Zugriffstaste herunterzuladen, die zum Hochladen der PST-Dateien an einen Azure-Speicherort in der Microsoft-Cloud verwendet wird. Sie erhalten diese auf der Seite **importieren** im Security & Compliance Center. Der Schlüssel (als SAS-Schlüssel bezeichnet) bietet Ihnen die erforderlichen Berechtigungen zum Hochladen von PST-Dateien an einen privaten und sicheren Azure-Speicherort. Dieser Zugriffsschlüssel ist für Ihre Organisation eindeutig und verhindert, dass nicht autorisierter Zugriff auf Ihre PST-Dateien nach dem Hochladen in die Microsoft-Cloud erfolgt. Beachten Sie, dass das Importieren von PST-Dateien in Office 365 nicht erforderlich ist, dass Ihre Organisation über ein separates Azure-Abonnement verfügt. 
    
2. **Laden Sie die PST-Dateien in den Azure-Speicherort hoch** – im nächsten Schritt verwenden Sie das AzCopy. exe-Tool (in Schritt 1 heruntergeladen) zum Hochladen und Speichern Ihrer PST-Dateien an einem Azure-Speicherort, der sich im selben regionalen Microsoft-Rechenzentrum befindet, in dem Ihre Office 365 Organisation befindet. Zum Hochladen der PST-Dateien, die Sie in Office 365 importieren möchten, müssen Sie sich in einer Dateifreigabe oder einem Dateiserver in Ihrer Organisation befinden.
    
    Beachten Sie, dass Sie einen optionalen Schritt ausführen können, um die Liste der PST-Dateien anzuzeigen, nachdem diese in den Azure-Speicherort hochgeladen wurden.
    
3. **Erstellen einer PST-Import Zuordnungsdatei** – nachdem die PST-Dateien in den Azure-Speicherort hochgeladen wurden, besteht der nächste Schritt darin, eine CSV-Datei (Comma Separated Value) zu erstellen, die angibt, in welche Benutzerpostfächer die PST-Dateien importiert werden, beachten Sie, dass eine PST-Datei  in das primäre Postfach eines Benutzers oder sein Archivpostfach importiert. Der Office 365-Import Dienst verwendet die Informationen in der CSV-Datei, um die PST-Dateien zu importieren.
    
4. **Create a PST Import Job** -der nächste Schritt besteht darin, einen PST-Importauftrag auf der Seite " **importieren** " im Security & Compliance Center zu erstellen und die PST-Import Zuordnungsdatei zu übermitteln, die im vorherigen Schritt erstellt wurde. Nachdem Sie den Importauftrag erstellt haben, analysiert Office 365 die Daten in den PST-Dateien und gibt Ihnen dann die Möglichkeit, Filter festzulegen, mit denen gesteuert wird, welche Daten tatsächlich in die in der PST-Import Zuordnungsdatei angegebenen Postfächer importiert werden. 
    
5. **Filtern der PST-Daten, die in Postfächer importiert** werden – nachdem der Importauftrag erstellt und gestartet wurde, analysiert Office 365 die Daten in den PST-Dateien (sicher und sicher), indem das Alter der Elemente und die unterschiedlichen Nachrichtentypen identifiziert werden, die in den PST-Dateien enthalten sind. . Wenn die Analyse abgeschlossen ist und die Daten importiert werden können, haben Sie die Möglichkeit, alle in den PST-Dateien enthaltenen Daten zu importieren oder die importierten Daten zu trimmen, indem Sie Filter festlegen, mit denen gesteuert wird, welche Daten importiert werden.
    
6. **Starten des PST-importauftrags** – nachdem der Importauftrag gestartet wurde, verwendet Office 365 die Informationen in der PST-Import Zuordnungsdatei, um die PST-Dateien vom he Azure-Speicherort in Benutzerpostfächer zu importieren. Status Informationen zum Importauftrag (einschließlich Informationen zu den einzelnen importierten PST-Dateien) werden auf der Seite " **importieren** " im Security & Compliance Center angezeigt. Wenn der Importauftrag abgeschlossen ist, wird der Status für den Auftrag auf " **abgeschlossen**" festgelegt.
  
## <a name="more-information"></a>Weitere Informationen

- Gründe für das Importieren von PST-Dateien in Office 365
    
  - Es ist eine gute Möglichkeit, die Archiv Nachrichtendaten Ihrer Organisation in Office 365 zu importieren.
    
  - Die Daten sind für den Benutzer auf allen Geräten verfügbar, da Sie in der Cloud gespeichert sind.
    
  - Es hilft, die Compliance-Anforderungen Ihrer Organisation zu erfüllen, indem Sie Office 365 Compliance-Features auf die Daten aus den importierten PST-Dateien anwenden können. Dies umfasst Folgendes:
    
  - Durch Aktivieren von [archivpostfächern](enable-archive-mailboxes.md) und [automatisch erweiterter Archivierung](enable-unlimited-archiving.md) können Benutzer zusätzlichen Postfachspeicher Platz zum Speichern der importierten Daten erhalten. 
    
  - Platzieren von Postfächern in einem [Beweissicherungsverfahren](https://go.microsoft.com/fwlink/?linkid=856286) , um die importierten Daten beizubehalten. 
    
  - Verwenden von Microsoft [eDiscovery-Tools](search-for-content.md) zum Durchsuchen der importierten Daten. 
    
  - Verwenden [Office 365 Aufbewahrungsrichtlinien](retention-policies.md) , um zu steuern, wie lange die Daten, die Sie importiert haben, aufbewahrt werden, und welche Aktionen nach Ablauf des Aufbewahrungszeitraums durchgeführt werden sollen. 
    
  - Durchsuchen des [Office 365 Überwachungsprotokolls](search-the-audit-log-in-security-and-compliance.md) nach Post fachbezogenen Ereignissen, die sich auf die importierten Daten auswirken. 
    
  - Importieren von Daten in inaktive [Postfächer](create-and-manage-inactive-mailboxes.md) zum Archivieren von Daten zu Kompatibilitätszwecken. 
    
  - Verwenden von Richtlinien zur Verhinderung von [Datenverlust](data-loss-prevention-policies.md) , um zu verhindern, dass vertrauliche Daten außerhalb Ihrer Organisation verloren gehen. 
  
- Hier ist ein Beispiel für die SAS-URL (Shared Access Signature), die in Schritt 1 abgerufen wird. Dieses Beispiel enthält auch die Syntax für den Befehl, den Sie im Tool AzCopy. exe ausführen, um PST-Dateien in Office 365 hochzuladen. Achten Sie darauf, dass Sie Vorkehrungen treffen, um die SAS-URL zu schützen, genauso wie Sie Kennwörter oder andere sicherheitsrelevante Informationen schützen würden.

    ```
    SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D

    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y

    EXAMPLES

    This example uploads PST files to the root of the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
    
    This example uploads PST files to a subfolder named PSTFiles  in the Azure storage location:

    AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
``

- As previously explained, the Office 365 Import service turns on the retention hold setting (for an indefinite duration) after PST files are imported to a mailbox. This means the  *RetentionHoldEnabled*  property is set to  **True** so that the retention policy assigned to the mailbox won't be processed. This gives the mailbox owner time to manage the newly-imported messages by preventing a deletion or archive policy from deleting or archiving older messages. Here are some steps you can take to manage this retention hold: 
    
    - After a certain period of time, you can turn off the retention hold by running the **Set-Mailbox -RetentionHoldEnabled $false** command. For instructions, see [Place a mailbox on retention hold](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
   - You can configure the retention hold so that it's turned off on some date in the future. You do this by running the **Set-Mailbox -EndDateForRetentionHold *date*** command. For example, assuming that today's date is June 1, 2016 and you want the retention hold turned off in 30 days, you would run the following command:  **Set-Mailbox -EndDateForRetentionHold 7/1/2016**. In this scenario, you would leave the  **RetentionHoldEnabled**  property set to  *True*. For more information, see [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
   - You can change the settings for the retention policy that's assigned to the mailbox so that older items that were imported won't be immediately deleted or moved to the user's archive mailbox. For example, you could lengthen the retention age for a deletion or archive policy that's assigned to the mailbox. In this scenario, you would turn off the retention hold on the mailbox after you changed the settings of the retention policy. For more information, see [Set up an archive and deletion policy for mailboxes in your Office 365 organization](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    
