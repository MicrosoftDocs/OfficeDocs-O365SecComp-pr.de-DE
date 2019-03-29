---
title: Verwenden des Netzwerk Uploads zum Importieren Ihrer Organisations-PST-Dateien in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.audience: Admin
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
description: 'Für Administratoren: erfahren Sie, wie Sie mithilfe des Netzwerk-Uploads mehrere PST-Dateien in Benutzerpostfächern in Office 365 Massenimportieren.'
ms.openlocfilehash: d7ef9d5f9f1d9fcf9ebdf31ffe42979482abc5e7
ms.sourcegitcommit: fb50bf2f2c9d780c911f245a2f78c6bb5e357f67
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2019
ms.locfileid: "30950452"
---
# <a name="use-network-upload-to-import-your-organization-pst-files-to-office-365"></a>Verwenden des Netzwerk Uploads zum Importieren Ihrer Organisations-PST-Dateien in Office 365

> [!NOTE]
> Dieser Artikel richtet sich an Administratoren. Möchten Sie PST-Dateien in Ihr eigenes Postfach importieren? Weitere Informationen finden Sie unter [Importieren von e-Mails, Kontakten und Kalendern aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)
  
Nachfolgend finden Sie die schrittweisen Anweisungen, die für die Verwendung des Netzwerk Uploads zum Massenimport mehrerer PST-Dateien in Office 365-Postfächer erforderlich sind. Häufig gestellte Fragen zur Verwendung des Netzwerk Uploads zum Massenimport von PST-Dateien in Office 365-Postfächern finden Sie unter [FAQs zur Verwendung des Netzwerk Uploads zum Importieren von PST-Dateien](faqimporting-pst-files-to-office-365.md#using-network-upload-to-import-pst-files).
  
[Schritt 1: Kopieren Sie die SAS-URL, und installieren Sie Azure AzCopy](#step-1-copy-the-sas-url-and-install-azure-azcopy)

[Schritt 2: Hochladen der PST-Dateien in Office 365](#step-2-upload-your-pst-files-to-office-365)

[Optional Schritt 3: Anzeigen einer Liste der PST-Dateien, die in Office 365 hochgeladen wurden](#optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Schritt 4: Erstellen der PST-Import Zuordnungsdatei](#step-4-create-the-pst-import-mapping-file)

[Schritt 5: Erstellen eines PST-Import Auftrags in Office 365](#step-5-create-a-pst-import-job-in-office-365)

[Schritt 6: Filtern von Daten und Starten des PST-Import Auftrags](#step-6-filter-data-and-start-the-pst-import-job)

Beachten Sie, dass Sie Schritt 1 nur einmal ausführen müssen, um PST-Dateien in Office 365-Postfächer zu importieren. Nachdem Sie diese Schritte ausgeführt haben, führen Sie Schritt 2 bis Schritt 6 jedes Mal aus, wenn Sie einen Batch von PST-Dateien hochladen und importieren möchten.

## <a name="before-you-begin"></a>Bevor Sie beginnen
  
- Sie müssen die Rolle "Postfachimport-export" in Exchange Online zuweisen, um PST-Dateien in Office 365-Postfächer zu importieren. Diese Rolle wird standardmäßig keiner Rollengruppe in Exchange Online zugewiesen. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" unter [Verwalten von Rollengruppen](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Darüber hinaus muss eine der folgenden Anforderungen erfüllt sein, um &amp; Importaufträge im Office 365 Security Compliance Center zu erstellen:
    
  - Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Oder
    
  - Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation sein.
    
  > [!TIP]
    > Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange Online, die speziell für den Import von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die erforderlichen Mindestberechtigungen zum Importieren von PST-Dateien die Rollen Mailbox Import Export und e-Mail-Empfänger der neuen Rollengruppe zu, und fügen Sie dann Mitglieder hinzu. 
  
- Die einzige unterstützte Methode zum Importieren von PST-Dateien in Office 365 ist die Verwendung des Azure AzCopy-Tools, wie in diesem Thema beschrieben. Sie können den Azure-Speicher-Explorer nicht verwenden, um PST-Dateien direkt in den Azure-Speicherbereich hochzuladen.
    
- Sie müssen die PST-Dateien, die Sie in Office 365 importieren möchten, auf einem Dateiserver oder einem freigegebenen Ordner in Ihrer Organisation speichern. In Schritt 2 führen Sie das Azure AzCopy-Tool aus, mit dem die PST-Dateien, die auf diesem Dateiserver oder freigegebenen Ordner gespeichert sind, in Office 365 hochgeladen werden.
    
- Bei diesem Verfahren wird eine Kopie einer URL mit einer Zugriffstaste kopiert und gespeichert. Diese Informationen werden in Schritt 2 zum Hochladen Ihrer PST-Dateien und in Schritt 3 verwendet, wenn Sie eine Liste der PST-Dateien anzeigen möchten, die in Office 365 hochgeladen wurden. Achten Sie darauf, Vorkehrungen zu treffen, um diese URL zu schützen, wie Sie Kennwörter oder andere sicherheitsrelevante Informationen schützen würden. Sie können Sie beispielsweise in einem kennwortgeschützten Microsoft Word-Dokument oder auf einem verschlüsselten USB-Laufwerk speichern. Im Abschnitt [Weitere Informationen](#more-information) finden Sie ein Beispiel für diese kombinierte URL und den kombinierten Schlüssel. 
    
- Sie können PST-Dateien in ein inaktives Postfach in Office 365 importieren. Hierzu geben Sie die GUID des inaktiven Postfachs im `Mailbox` Parameter in der PST-Import Zuordnungsdatei an. Weitere Informationen finden Sie in Schritt 4 auf der Registerkarte " **Anweisungen** " in diesem Thema. 
    
- In einer Exchange-hybridbereitstellung können Sie PST-Dateien in ein cloudbasierten Archivpostfach für einen Benutzer importieren, dessen primäres Postfach lokal ist. Führen Sie dazu die folgenden Schritte in der PST-Import Zuordnungsdatei aus:
    
  - Geben Sie die e-Mail-Adresse des lokalen Postfachs des Benutzers `Mailbox` im Parameter an. 
    
  - Geben Sie den Wert **true** im `IsArchive` Parameter an. 
    
    Weitere Informationen finden Sie in [Schritt 4](#step-4-create-the-pst-import-mapping-file) . 
    
- Nachdem PST-Dateien in ein Office 365-Postfach importiert wurden, wird die Aufbewahrungszeit für das Postfach für eine unbegrenzte Dauer aktiviert. Dies führt dazu, dass die dem Postfach zugewiesene Aufbewahrungsrichtlinie erst verarbeitet wird, wenn Sie die Aufbewahrungsdauer deaktivieren oder ein Datum festlegen, um den Haltestatus zu deaktivieren. Warum tun wir das? Wenn Nachrichten, die in ein Postfach importiert wurden, alt sind, werden Sie möglicherweise dauerhaft gelöscht (bereinigt), da ihre Aufbewahrungszeit auf Grundlage der für das Postfach konfigurierten Aufbewahrungseinstellungen abgelaufen ist. Wenn Sie die Aufbewahrungszeit für das Postfach aktivieren, wird der Postfachbesitzer zum Verwalten dieser neu importierten Nachrichten oder zum Ändern der Aufbewahrungseinstellungen für das Postfach Zeit. Auf der Registerkarte **Weitere Informationen** in diesem Thema finden Sie Vorschläge zum Verwalten der Aufbewahrungsdauer. 
    
- Standardmäßig beträgt die maximale Nachrichtengröße, die von einem Office 365-Postfach empfangen werden kann, 35 MB. Der Grund ist, dass der Standardwert für die *MaxReceiveSize* -Eigenschaft für ein postfach auf 35 MB festgelegt ist. Das Limit für die maximale Nachrichtenempfangs Größe in Office 365 beträgt jedoch 150 MB. Wenn Sie also eine PST-Datei importieren, die ein Element enthält, das größer als 35 MB ist, wird der Office 365-Import Dienst automatisch den Wert der *MaxReceiveSize* -Eigenschaft des zielpostfachs auf 150 MB ändern. Dadurch können Nachrichten bis zu 150 MB in Benutzerpostfächer importiert werden. 
    
    > [!TIP]
    > Um die Nachrichtenempfangs Größe für ein Postfach zu identifizieren, können Sie diesen Befehl in Exchange Online PowerShell: `Get-Mailbox <user mailbox> | FL MaxReceiveSize`ausführen. 

## <a name="step-1-copy-the-sas-url-and-install-azure-azcopy"></a>Schritt 1: Kopieren Sie die SAS-URL, und installieren Sie Azure AzCopy

Der erste Schritt besteht darin, das Azure AzCopy-Tool herunterzuladen und zu installieren, das das Tool ist, das Sie in Schritt 2 ausführen, um PST-Dateien in Office 365 hochzuladen. Außerdem kopieren Sie die SAS-URL für Ihre Organisation. Diese URL ist eine Kombination aus der Netzwerk-URL für den Azure-Speicherort in der Microsoft-Cloud für Ihre Organisation und einem SAS-Schlüssel (Shared Access Signature). Dieser Schlüssel enthält die erforderlichen Berechtigungen zum Hochladen von PST-Dateien an den Azure-Speicherort. Achten Sie darauf, Vorkehrungen zum Schutz der SAS-URL zu treffen. Sie ist eindeutig für Ihre Organisation und wird in Schritt 2 verwendet.

> [!IMPORTANT]
> Zum Importieren von PST-Dateien mithilfe der Network Upload-Methode wird empfohlen, die Version von Azure AzCopy zu verwenden, die in Schritt 6B im folgenden Verfahren heruntergeladen werden kann.
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in ihrer Office 365-Organisation an. 
    
2. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Data Governance** \> - **Import**.
    
    > [!NOTE]
    > Sie müssen über die entsprechenden Berechtigungen für den Zugriff auf die Seite " **importieren** " im &amp; Security Compliance Center verfügen. Weitere Informationen finden Sie im Abschnitt **bevor Sie beginnen** . 
    
3. Klicken Sie **** ![auf der Seite importieren auf Symbol](media/ITPro-EAC-AddIcon.gif) hinzufügen **neuer Importauftrag**.
    
    Der importauftrags-Assistent wird angezeigt.
    
4. Geben Sie einen Namen für den PST-Importauftrag ein, und klicken Sie dann auf **weiter**. Verwenden Sie Kleinbuchstaben, Zahlen, Bindestriche und Unterstriche. Sie können keine Großbuchstaben verwenden oder Leerzeichen im Namen einfügen.
    
5. Klicken Sie auf der Seite möchten **Sie uploaden oder Daten versenden** auf **Ihre Daten hochladen** , und klicken Sie dann auf **weiter**.
    
    ![Klicken Sie auf Ihre Daten hochladen, um einen Importauftrag für Netzwerk Uploads zu erstellen.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Führen Sie auf der Seite **Daten importieren** die folgenden beiden Aktionen aus: 
    
    ![Kopieren der SAS-URL und Herunterladen des Azure AzCopy-Tools auf der Seite "Daten importieren"](media/74411014-ec4b-4e25-9065-404c934cce17.png)
  
    a. Klicken Sie in Schritt 2 auf **Netzwerk-Upload-SAS-URL anzeigen**. Klicken Sie nach dem Anzeigen der SAS-URL auf **in die Zwischenablage kopieren** , und fügen Sie Sie dann in eine Datei ein, damit Sie Sie später aufrufen können.
    
    b. Klicken Sie in Schritt 3 auf **Azure AzCopy herunterladen** , um das Azure AzCopy-Tool herunterzuladen und zu installieren. Klicken Sie im Popupfenster auf **Ausführen** , um AzCopy zu installieren. 
    
> [!NOTE]
> Sie können die Seite **Daten importieren** geöffnet lassen (falls Sie die SAS-URL erneut kopieren müssen) oder auf **Abbrechen** klicken, um Sie zu schließen. 
 
## <a name="step-2-upload-your-pst-files-to-office-365"></a>Schritt 2: Hochladen der PST-Dateien in Office 365

Jetzt können Sie das AzCopy. exe-Tool verwenden, um PST-Dateien in Office 365 hochzuladen. Dieses Tool wird hochgeladen und an einem Azure-Speicherort in der Microsoft-Cloud gespeichert. Wie bereits erläutert, befindet sich der Azure-Speicherort, an den Sie Ihre PST-Dateien hochladen, im gleichen regionalen Microsoft-Datencenter, in dem sich Ihre Office 365-Organisation befindet. Damit Sie diesen Schritt ausführen können, müssen sich die PST-Dateien in einer Dateifreigabe oder auf einem Dateiserver in Ihrer Organisation befinden. Im folgenden Verfahren wird dies als das Quellverzeichnis bezeichnet. Jedes Mal, wenn Sie das AzCopy-Tool ausführen, können Sie ein anderes Quellverzeichnis angeben. 
  
1. Öffnen Sie eine Eingabeaufforderung auf dem lokalen Computer.
    
2. Wechseln Sie zu dem Verzeichnis, in dem Sie das Tool AzCopy. exe in Schritt 1 installiert haben. Wenn Sie das Tool am Standardspeicherort installiert haben, wechseln Sie `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy`zu.
    
3. Führen Sie den folgenden Befehl aus, um die PST-Dateien in Office 365 hochzuladen.

    ```
    AzCopy.exe /Source:<Location of PST files> /Dest:<SAS URL> /V:<Log file location> /Y
  
    ```
 
    In der folgenden Tabelle werden die Parameter und deren erforderliche Werte beschrieben. Beachten Sie, dass die Informationen, die Sie im vorherigen Schritt abgerufen haben, in den Werten für diese Parameter verwendet werden.
    
    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `/Source:` <br/> |Gibt das Quellverzeichnis in Ihrer Organisation an, das die PST-Dateien enthält, die in Office 365 hochgeladen werden.  <br/> Stellen Sie sicher, dass Sie den Wert dieses Parameters in doppelte Anführungszeichen ("") einschließen.  <br/> | `/Source:"\\FILESERVER01\PSTs"` <br/> |
    | `/Dest:` <br/> |Gibt die SAS-URL an, die Sie in Schritt 1 abgerufen haben.  <br/> Stellen Sie sicher, dass Sie den Wert dieses Parameters in doppelte Anführungszeichen ("") einschließen.  <br/> **Tipp:** Optional Sie können einen Unterordner im Azure-Speicher Speicherort angeben, in den die PST-Dateien hochgeladen werden sollen. Hierzu fügen Sie einen Unterordner Speicherort (nach "ingestiondata") in der SAS-URL hinzu. Im ersten Beispiel wird kein Unterordner angegeben; Das heißt, dass die PST in den Stamm (mit dem Namen *ingestiondata* ) des Azure-Speicherorts hochgeladen wird. Im zweiten Beispiel werden die PST-Dateien in einen Unterordner (mit dem Namen *PSTFiles* ) im stammVerzeichnis des Azure-Speicherorts hochgeladen.  <br/> | `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> Oder  <br/>  `/Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/PSTFiles?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/V:` <br/> |Gibt ausführliche Statusmeldungen in einer Protokolldatei aus. Standardmäßig heißt die ausführliche Protokolldatei AzCopyVerbose. Log in%LocalAppData%\Microsoft\Azure\AzCopy. Wenn Sie für diese Option einen vorhandenen Dateispeicherort angeben, wird das ausführliche Protokoll an die Datei angefügt.  <br/> Stellen Sie sicher, dass Sie den Wert dieses Parameters in doppelte Anführungszeichen ("") einschließen.  <br/> | `/V:"c:\Users\Admin\Desktop\Uploadlog.log"` <br/> |
    | `/S` <br/> |Diese optionale Option gibt den rekursiven Modus an, sodass das AzCopy-Tool PST-Dateien in Unterordnern im Quellverzeichnis, das durch den `/Source:` -Parameter angegeben ist, kopiert.  <br/> **Hinweis:** Wenn Sie diese Option verwenden, haben PST-Dateien in Unterordnern einen anderen Datei Pfad im Azure-Speicher Speicherort, nachdem Sie hochgeladen wurden. Sie müssen den genauen Dateipfadnamen in der CSV-Datei angeben, die Sie in Schritt 4 erstellen.  <br/> | `/S` <br/> |
    | `/Y` <br/> |Diese erforderliche Option ermöglicht die Verwendung von schreibgeschützten SAS-Token beim Hochladen der PST-Dateien an den Azure-Speicherort. Die SAS-URL, die Sie in Schritt 1 (und `/Dest:` in Parameter angegeben) abgerufen haben, ist eine schreibgeschützte SAS-URL, weshalb Sie diese Option verwenden müssen. Beachten Sie, dass eine schreibgeschützte SAS-URL nicht verhindert, dass Sie den Azure-Speicher-Explorer verwenden, um eine Liste der PST-Dateien anzuzeigen, die an den Azure-Speicherort hochgeladen wurden.  <br/> | `/Y` <br/> |
   
NachFolgend finden Sie ein Beispiel für die Syntax für das AzCopy. exe-Tool, das die tatsächlichen Werte für jeden Parameter verwendet:
    
```
  AzCopy.exe /Source:"\\FILESERVER1\PSTs" /Dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D" /V:"c:\Users\Admin\Desktop\AzCopy1.log" /Y
  
```

Nachdem Sie den Befehl ausgeführt haben, werden Statusmeldungen angezeigt, die den Fortschritt des Hochladens der PST-Dateien anzeigen. Eine endgültige Statusmeldung zeigt die Gesamtzahl der erfolgreich hochgeladenen Dateien an.

> [!TIP]
> Nachdem Sie den Befehl AzCopy. exe erfolgreich ausgeführt haben und sichergestellt haben, dass alle Parameter korrekt sind, speichern Sie eine Kopie der Befehlszeilensyntax in derselben (sicheren) Datei, in der Sie die in Schritt 1 abgerufenen Informationen kopiert haben. Sie können diesen Befehl dann jedes Mal in einer EingabeaufForderungen kopieren und einfügen, wenn Sie das AzCopy. exe-Tool ausführen möchten, um PST-Dateien in Office 365 hochzuladen. Der einzige Wert, den Sie möglicherweise ändern müssen, sind `/Source:` die für den-Parameter. Dies hängt vom Quellverzeichnis ab, in dem sich die PST-Dateien befinden.

## <a name="optional-step-3-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Optional Schritt 3: Anzeigen einer Liste der PST-Dateien, die in Office 365 hochgeladen wurden

Als optionaler Schritt können Sie den Microsoft Azure Storage Explorer (ein kostenloses Open Source-Tool) installieren und verwenden, um die Liste der PST-Dateien anzuzeigen, die Sie in das Azure-BLOB hochgeladen haben. Hierfür gibt es zwei gute Gründe:
  
- Stellen Sie sicher, dass PST-Dateien aus dem freigegebenen Ordner oder Dateiserver in Ihrer Organisation erfolgreich in das Azure-BLOB hochgeladen wurden.
    
- Überprüfen Sie den Dateinamen (und den Pfadnamen des Unterordners, wenn Sie einen enthalten) für jede PST-Datei, die in das Azure-BLOB hochgeladen wurde. Dies ist sehr hilfreich, wenn Sie die PST-Zuordnungsdatei im nächsten Schritt erstellen, da Sie sowohl den Ordner Pfadnamen als auch den Dateinamen für jede PST-Datei angeben müssen. Die Überprüfung dieser Namen kann dazu beitragen, potenzielle Fehler in Ihrer PST-Zuordnungsdatei zu reduzieren.
    
Der Microsoft Azure-Speicher-Explorer befindet sich in der Vorschau.
  
> [!IMPORTANT]
> Sie können den Azure-Speicher-Explorer nicht verwenden, um PST-Dateien hochzuladen oder zu ändern. Die einzige unterstützte Methode zum Importieren von PST-Dateien in Office 365 ist die Verwendung von AzCopy. Außerdem können Sie keine PST-Dateien löschen, die Sie in das Azure-BLOB hochgeladen haben. Wenn Sie versuchen, eine PST-Datei zu löschen, wird eine Fehlermeldung angezeigt, in der Sie darauf hingewiesen werden, dass Sie nicht über die erforderlichen Berechtigungen verfügen. Beachten Sie, dass alle PST-Dateien automatisch aus Ihrem Azure-Speicherbereich gelöscht werden. If there are no import jobs in progress, then all PST files in the **ingestiondata** container are deleted 30 days after the most recent import job was created.
  
So installieren Sie den Azure Storage Explorer und stellen eine Verbindung mit Ihrem Azure-Speicherbereich her:
  
1. Laden Sie das [Microsoft Azure Storage Explorer-Tool](https://go.microsoft.com/fwlink/p/?LinkId=544842)herunter, und installieren Sie es.
    
2. Starten Sie den Microsoft Azure Storage Explorer, klicken Sie im linken Bereich mit der rechten Maustaste auf **Speicherkonten** , und klicken Sie dann auf mit **Azure-Speicher verbinden**.
    
    ![Klicken Sie mit der rechten Maustaste auf Speicherkonten, und klicken Sie dann auf mit Azure-Speicher verbinden](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Klicken Sie auf **zugriffssignatur (Shared Access Signature, SAS)-URI oder Verbindungszeichenfolge verwenden** , und klicken Sie auf **weiter**.
    
4. Klicken Sie auf **SAS-URI verwenden**, fügen Sie die SAS-URL, die Sie in Schritt 1 abgerufen haben, in das Feld unter **URI**ein, und klicken Sie dann auf **weiter**.
    
5. Auf der Zusammenfassungsseite der **Verbindung** können Sie die Verbindungsinformationen überarbeiten und dann auf **verbinden**klicken.
    
    Der **ingestiondata** -Container wird geöffnet; Sie enthält die PST-Dateien, die Sie in Schritt 2 hochgeladen haben. Der **ingestiondata** -Container befindet sich unter **Speicherkonten** \> **(SAS-Attached Services)** \> - **BLOB-Container**. 
    
    ![Azure Storage Explorer zeigt eine Liste der PST-Dateien an, die Sie hochgeladen haben](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
6. Wenn Sie die Verwendung von Microsoft Azure Storage Explorer abgeschlossen haben, klicken Sie mit der rechten Maustaste auf **** **ingestiondata**, und klicken Sie dann auf trennen, um die Verbindung mit dem Azure-Speicherbereich zu trennen. Andernfalls erhalten Sie eine Fehlermeldung, wenn Sie das nächste Mal anfügen. 
    
    ![Klicken Sie mit der rechten Maustaste auf die Einnahme, und klicken Sie auf trennen, um die Verbindung mit Ihrem Azure-Speicherbereich](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-4-create-the-pst-import-mapping-file"></a>Schritt 4: Erstellen der PST-Import Zuordnungsdatei

Nachdem die PST-Dateien an den Azure-Speicherort für Ihre Office 365-Organisation hochgeladen wurden, besteht der nächste Schritt darin, eine CSV-Datei (Comma Separated Value) zu erstellen, die angibt, in welche Benutzerpostfächer die PST-Dateien importiert werden sollen. Sie werden diese CSV-Datei im nächsten Schritt übermitteln, wenn Sie einen PST-Import Auftrag erstellen.
  
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
    Die erste Zeile oder Kopfzeile der CSV-Datei enthält die Parameter, die vom PST-Importdienst verwendet werden, um die PST-Dateien in Benutzerpostfächer zu importieren. Die einzelnen Parameternamen werden jeweils durch ein Komma getrennt. Jede Zeile unter der Kopfzeile stellt die Parameterwerte für das Importieren einer PST-Datei in ein bestimmtes Postfach dar. Sie benötigen eine Zeile für jede PST-Datei, die Sie in ein Benutzerpostfach importieren möchten. Vergessen Sie nicht, die Platzhalterdaten in der Zuordnungsdatei durch die tatsächlichen Werte zu ersetzen.

   **Hinweis:** Ändern Sie nichts in der Kopfzeile, einschließlich der SharePoint-Parameter; Sie werden während des PST-Import Vorgangs ignoriert. 

 3. Verwenden Sie die Informationen in der folgenden Tabelle, um zu die CSV-Datei mit den erforderlichen Informationen zu füllen.


    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Gibt den Office 365-Dienst an, in den die Daten importiert werden. Verwenden `Exchange`Sie zum Importieren von PST-Dateien in Benutzerpostfächer.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Gibt den Speicherort des Ordners im Azure-Speicherort an, an den Sie die PST-Dateien in Schritt 2 hochgeladen haben.  <br/> Wenn Sie in der SAS-URL im `/Dest:` Parameter in Schritt 2 keinen optionalen Unterordnernamen angegeben haben, lassen Sie diesen Parameter in der CSV-Datei leer. Wenn Sie einen Unterordnernamen hinzugefügt haben, geben Sie ihn in diesem Parameter an (siehe zweites Beispiel). Bei dem Wert für diesen Parameter wird die Groß-/Kleinschreibung beachtet.  <br/> In beiden Fällen *müssen Sie nicht* "ingestiondata" in den Wert des `FilePath` Parameters aufnehmen.  <br/><br/> **Wichtig:** Die Groß-/Kleinschreibung für den Dateipfad muss mit dem Fall identisch sein, den Sie verwendet haben, wenn Sie einen optionalen Unterordnernamen in die SAS `/Dest:` -URL im Parameter in Schritt 2 aufgenommen haben. Wenn Sie beispielsweise für den `PSTFiles` Namen des Unterordners in Schritt 2 verwendet haben und `pstfiles` dann den `FilePath` Parameter in der CSV-Datei verwenden, schlägt der Import für die PST-Datei fehl. Stellen Sie sicher, dass Sie den gleichen Fall in beiden Instanzen verwenden.  <br/> |(leer lassen)  <br/> Oder  <br/>  `PSTFiles` <br/> |
    | `Name` <br/> |Gibt den Namen der PST-Datei an, die in das Benutzerpostfach importiert wird.  Bei dem Wert für diesen Parameter wird die Groß-/Kleinschreibung beachtet.  <br/> <br/>**Wichtig:** Der Fall für den PST-Dateinamen in der CSV-Datei muss mit der PST-Datei übereinstimmen, die in Schritt 2 in den Azure-Speicherort hochgeladen wurde. Wenn Sie beispielsweise den `annb.pst` `Name` Parameter in der CSV-Datei verwenden, aber der Name der tatsächlichen PST-Datei lautet `AnnB.pst`, schlägt der Import für diese PST-Datei fehl. Stellen Sie sicher, dass der Name der PST in der CSV-Datei den gleichen Fall wie die tatsächliche PST-Datei verwendet.  <br/> | `annb.pst` <br/> |
    | `Mailbox` <br/> |Gibt die E-Mail-Adresse des Postfachs an, in das die PST-Datei importiert werden soll.  Beachten Sie, dass Sie keinen öffentlichen Ordner angeben können, da der PST-Importdienst keine Unterstützung f+r das Importieren von PST-Dateien in öffentlichen Ordnern bietet.  <br/> Um eine PST-Datei in ein inaktives Postfach zu importieren, müssen Sie die Postfach-GUID für diesen Parameter angeben. Führen Sie den folgenden PowerShell-Befehl in Exchange Online aus, um diese GUID zu erhalten:`Get-Mailbox <identity of inactive mailbox> -InactiveMailboxOnly | FL Guid` <br/> <br/>**Hinweis:** In einigen Fällen verfügen Sie möglicherweise über mehrere Postfächer mit derselben e-Mail-Adresse, wobei ein Postfach ein aktives Postfach und das andere Postfach den Status "Soft-Deleted" (oder inaktiv) aufweist. In diesen Situationen müssen Sie die Postfach-GUID angeben, um das Postfach, in das die PST-Datei importiert werden soll, eindeutig zu identifizieren. Führen Sie den folgenden PowerShell-Befehl aus, um diese GUID für aktive `Get-Mailbox <identity of active mailbox> | FL Guid`Postfächer zu erhalten:. Führen Sie diesen Befehl `Get-Mailbox <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`aus, um die GUID für Soft-deleted (oder inactive)-Postfächer abzurufen.  <br/> | `annb@contoso.onmicrosoft.com` <br/> Oder  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Gibt an, ob die PST-Datei in das Archivpostfach des Benutzers importiert werden soll. Es gibt zwei Möglichkeiten:  <br/><br/>**False** -importiert die PST-Datei in das primäre Postfach des Benutzers.  <br/> **True** -importiert die PST-Datei in das Archivpostfach des Benutzers. This assumes that the [user's archive mailbox is enabled](enable-archive-mailboxes.md). <br/><br/>Wenn Sie diesen Parameter auf `TRUE` festlegen und das Archivpostfach des Benutzers nicht aktiviert ist, schlägt der Import für diesen Benutzer fehl. Beachten Sie, dass bei einem Importfehler für einen Benutzer (da das Archiv nicht aktiviert ist und diese Eigenschaft `TRUE`auf festgelegt ist) die anderen Benutzer im Importauftrag nicht betroffen sind.  <br/>  If you leave this parameter blank, the PST file is imported to the user's primary mailbox.  <br/> <br/>**Hinweis:** Wenn Sie eine PST-Datei in ein cloudbasierten Archivpostfach für einen Benutzer importieren möchten, dessen primäres Postfach lokal ist, geben `TRUE` Sie diesen Parameter an, und geben Sie die e-Mail-Adresse für das lokale Postfach `Mailbox` des Benutzers für den Parameter an.  <br/> | `FALSE` <br/> Oder  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Gibt den Postfachordner an, in den die PST-Datei importiert wird.  <br/>  Wenn Sie diesen Parameter leer lassen, wird die PST-Datei in einen neuen Ordner mit dem Namen " **importiert** " auf der Stammebene des Postfachs importiert (dieselbe Ebene wie der Posteingangsordner und die anderen Standard Postfachordner).  <br/>  Wenn Sie angeben `/`, werden die Elemente in der PST-Datei direkt in den Ordner Posteingang des Benutzers importiert.  <br/><br/>  Wenn Sie angeben `/<foldername>`, werden die Elemente in der PST-Datei in einen Ordner mit dem Namen * \<\> FolderName* importiert. Wenn Sie beispielsweise verwenden `/ImportedPst`, werden die Elemente in einen Ordner mit dem Namen **ImportedPst**importiert. Dieser Ordner befindet sich im Postfach des Benutzers auf derselben Ebene wie der Ordner Posteingang.  <br/><br/> **Tipp:** Erwägen Sie, einige Test Batches auszuführen, um mit diesem Parameter zu experimentieren, damit Sie den besten Ordnerspeicherort bestimmen können, in den PST-Dateien importiert werden sollen.  <br/> |(leer lassen)  <br/> Oder  <br/>  `/` <br/> Oder  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Dieser optionale Parameter gibt einen numerischen Wert für die Codepage an, die zum Importieren von PST-Dateien im ANSI-Dateiformat verwendet werden soll. Dieser Parameter wird zum Importieren von PST-Dateien aus Chinesisch, Japanisch und Koreanisch (CJK) verwendet, da in diesen Sprachen in der Regel ein Double-Byte-Zeichensatz (DBCS) für die Zeichencodierung verwendet wird. Wenn dieser Parameter nicht zum Importieren von PST-Dateien für Sprachen verwendet wird, die DBCS für Postfachordner Namen verwenden, werden die Ordnernamen oft verstümmelt, nachdem Sie importiert wurden.  <br/><br/> Eine Liste der unterstützten Werte für diesen Parameter finden Sie unter [Code Page Identifiers](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> <br/>**Hinweis:** Wie bereits erwähnt, handelt es sich um einen optionalen Parameter, den Sie nicht in die CSV-Datei aufnehmen müssen. Sie können Sie auch hinzufügen und den Wert für eine oder mehrere Zeilen leer lassen.  <br/> |(leer lassen)  <br/> Oder  <br/>  `932`(Dies ist die Codepage-ID für ANSI/OEM Japanisch)  <br/> |
    | `SPFileContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPManifestContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPSiteUrl` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |

## <a name="step-5-create-a-pst-import-job-in-office-365"></a>Schritt 5: Erstellen eines PST-Import Auftrags in Office 365

Im nächsten Schritt erstellen Sie den PST-Importauftrag im Import Dienst in Office 365. Wie bereits erläutert, übermitteln Sie die PST-Import Zuordnungsdatei, die Sie in Schritt 4 erstellt haben. Nachdem Sie den neuen Auftrag erstellt haben, analysiert Office 365 die Daten in den PST-Dateien und gibt Ihnen dann die Möglichkeit, die Daten zu filtern, die tatsächlich in die in der PST-Import Zuordnungsdatei angegebenen Postfächer importiert werden (siehe [Schritt 6](#step-6-filter-data-and-start-the-pst-import-job)).
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in ihrer Office 365-Organisation an. 
    
2. Klicken Sie im linken Bereich des Security &amp; Compliance Centers auf **Datenverwaltung** , und klicken Sie dann auf **importieren**.
    
3. Klicken Sie **** ![auf der Seite importieren auf Symbol](media/ITPro-EAC-AddIcon.gif) hinzufügen **neuer Importauftrag**.
    
    **Hinweis:** Sie müssen über die entsprechenden Berechtigungen für den Zugriff auf die Seite " **importieren** " im &amp; Security Compliance Center verfügen, um einen neuen Importauftrag zu erstellen. Weitere Informationen finden Sie im Abschnitt **bevor Sie beginnen** . 
    
4. Geben Sie einen Namen für den PST-Importauftrag ein, und klicken Sie dann auf **weiter**. Verwenden Sie Kleinbuchstaben, Zahlen, Bindestriche und Unterstriche. Sie können keine Großbuchstaben verwenden oder Leerzeichen im Namen einfügen.
    
5. Klicken Sie auf der Seite möchten **Sie uploaden oder Daten versenden** auf **Ihre Daten hochladen** , und klicken Sie dann auf **weiter**.
    
    ![Klicken Sie auf Ihre Daten hochladen, um einen Importauftrag für Netzwerk Uploads zu erstellen.](media/e59f9dc3-ccde-44ff-ac38-c4e39d76ae85.png)
  
6. Klicken Sie in Schritt 4 auf der Seite **Daten importieren** auf die Kontrollkästchen **Ich habe meine Dateien hochgeladen** , und **Ich habe Zugriff auf die Zuordnungsdatei** , und klicken Sie dann auf **weiter**.
    
    ![Klicken Sie in Schritt 4 auf die beiden Kontrollkästchen.](media/9f2427e8-3af2-4e27-95e6-a9f08430d3d8.png)
  
7. Klicken Sie auf der Seite **Zuordnungsdatei auswählen** auf **Zuordnungsdatei auswählen** , um die PST-Import Zuordnungsdatei zu übermitteln, die Sie in Schritt 4 erstellt haben. 
    
    ![Klicken Sie auf Zuordnungsdatei auswählen, um die CSV-Datei zu übermitteln, die Sie für den Importauftrag erstellt haben.](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
8. Wenn der Name der CSV-Datei unter **Zuordnungs Dateiname**angezeigt wird, klicken **** Sie auf überPRÜFEN, um die CSV-Datei auf Fehler zu überprüfen. 
    
    ![Klicken Sie auf Validate, um die CSV-Datei auf Fehler zu prüfen.](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    Die CSV-Datei muss erfolgreich validiert werden, um einen PST-Import Auftrag zu erstellen. Hinweis der Dateiname wird nach erfolgreicher Validierung in Grün geändert. Wenn die Überprüfung fehlschlägt, klicken Sie auf den Link **Protokoll anzeigen** . Es wird ein Validierungsfehler Bericht mit einer Fehlermeldung für jede Zeile in der Datei geöffnet, die fehlgeschlagen ist. 
    
9. Nachdem die PST-Zuordnungsdatei erfolgreich überprüft wurde, lesen Sie das Dokument mit den allgemeinen Geschäftsbedingungen, und klicken Sie dann auf das Kontrollkästchen.
    
10. Klicken Sie auf **Speichern** , um den Auftrag zu übermitteln, und klicken Sie dann auf **Schließen** , nachdem der Auftrag erfolgreich erstellt wurde. 
    
    Eine Status Flyout-Seite mit dem Status **Analyse wird ausgeführt** , und der neue Importauftrag wird in der Liste auf der Seite **importieren** angezeigt. 
    
11. Klicken Sie auf Aktualisierungs](media/O365-MDM-Policy-RefreshIcon.gif) Symbol aktualisieren, um die Statusinformationen zu aktualisieren, die in der Spalte **Status** angezeigt werden. **** ![ Wenn die Analyse abgeschlossen ist und die Daten importiert werden können, wird der Status in **Analyse abgeschlossen**geändert.
    
    Sie können auf den Importauftrag klicken, um die Seite Status-Flyout anzuzeigen, die detailliertere Informationen zum Importauftrag enthält, beispielsweise den Status der einzelnen PST-Dateien, die in der Zuordnungsdatei aufgeführt sind.
 
## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Schritt 6: Filtern von Daten und Starten des PST-Import Auftrags

Nachdem Sie den Importauftrag in Schritt 5 erstellt haben, analysiert Office 365 die Daten in den PST-Dateien (auf sichere und sichere Weise), indem das Alter der Elemente und die verschiedenen Nachrichtentypen in den PST-Dateien angegeben werden. Wenn die Analyse abgeschlossen ist und die Daten zum Importieren bereit sind, haben Sie die Möglichkeit, alle in den PST-Dateien enthaltenen Daten zu importieren, oder Sie können die importierten Daten trimmen, indem Sie Filter festlegen, die Steuern, welche Daten importiert werden.
  
1. Klicken Sie auf der Seite **importieren** im &amp; Security Compliance Center auf bereit, um den Importauftrag, den Sie in Schritt 5 erstellt haben, in **Office 365 zu importieren** . 
    
    ![Klicken Sie neben dem von Ihnen erstellten Importauftrag auf bereit, um nach Office 365 zu importieren.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Eine Fly-Out-Seite wird mit Informationen zu den PST-Dateien und weiteren Informationen zum Importauftrag angezeigt.
    
2. Klicken Sie auf der Seite Flyout auf **in Office 365 importieren**.
    
    Die Seite **Filter Ihre Daten** wird angezeigt. Sie enthält die Daten Einblicke, die aus der Analyse der PST-Dateien durch Office 365 resultieren, einschließlich Informationen zum Alter der Daten. Zu diesem Zeitpunkt haben Sie die Möglichkeit, die Daten zu filtern, die importiert werden, oder alle Daten zu importieren. 
    
    ![Sie können die Daten in den PST-Dateien kürzen oder importieren.](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
3. Führen Sie einen der folgenden Schritte aus:
    
    a. Klicken Sie zum Kürzen der importierten Daten auf **Ja, ich möchte Sie vor dem Importieren Filtern**.
    
    Detaillierte schrittweise Anweisungen zum Filtern der Daten in den PST-Dateien und zum anschließenden Starten des importauftrags finden Sie unter [Filtern von Daten beim Importieren von PST-Dateien in Office 365](filter-data-when-importing-pst-files.md).
    
    Oder
    
    b. Klicken Sie auf **Nein, ich möchte alles importieren,** und klicken Sie auf **weiter**, um alle Daten in den PST-Dateien zu importieren.
    
4. Wenn Sie alle Daten importiert haben, klicken Sie auf **Daten importieren** , um den Importauftrag zu starten. 
    
    Der Status des importauftrags wird auf der Seite **importieren** angezeigt. Klicken Sie auf ![aktualisieren, um die Statusinformationen zu aktualisieren, die in der Spalte **Status** angezeigt werden. **** ](media/O365-MDM-Policy-RefreshIcon.gif) Klicken Sie auf den Importauftrag, um die Seite Status Flyout anzuzeigen, in der Statusinformationen zu jeder importierten PST-Datei angezeigt werden. 

## <a name="how-the-import-process-works"></a>FunktionsWeise des Importvorgangs
  
Sie können die Option Netzwerk Upload und den Office 365-Import Dienst verwenden, um PST-Dateien in Benutzerpostfächer massenweise zu importieren. Der Netzwerk Upload bewirkt, dass Sie die PST-Dateien in einem temporären Speicherbereich in der Microsoft-Cloud hochladen. Anschließend kopiert der Office 365-Import Dienst die PST-Dateien aus dem Speicherbereich in die Postfächer des Zielbenutzers.
  
Hier sehen Sie eine Abbildung und Beschreibung des Netzwerk Upload-Prozesses zum Importieren von PST-Dateien in Postfächer in Office 365.
  
![Workflow des Netzwerk Uploads zum Importieren von PST-Dateien in Office 365](media/9e05a19e-1e7a-4f1f-82df-9118f51588c4.png)
  
1. **Herunterladen des PST-Importtools und des Schlüssels in den privaten Azure-Speicherort** – der erste Schritt besteht darin, das Azure AzCopy-Befehlszeilentool und eine Zugriffstaste zum Hochladen der PST-Dateien an einen Azure-Speicherort in der Microsoft-Cloud herunterzuladen. Sie erhalten diese auf der Seite " **importieren** " im Office 365 &amp; Security Compliance Center. Der Schlüssel (als SAS-Schlüssel bezeichnet) bietet Ihnen die erforderlichen Berechtigungen zum Hochladen von PST-Dateien an einen privaten und sicheren Azure-Speicherort. Diese Zugriffstaste ist eindeutig für Ihre Organisation und verhindert den unbefugten Zugriff auf Ihre PST-Dateien, nachdem Sie in die Microsoft-Cloud hochgeladen wurden. Beachten Sie, dass das Importieren von PST-Dateien in Office 365 für Ihre Organisation kein separates Azure-Abonnement erfordert. 
    
2. **Laden Sie die PST-Dateien an den Azure-Speicherort hoch** -im nächsten Schritt verwenden Sie das AzCopy. exe-Tool (heruntergeladen in Schritt 1) zum Hochladen und Speichern Ihrer PST-Dateien an einem Azure-Speicherort, der sich im selben regionalen Microsoft-Datencenter befindet, in dem ihr Office 365 Organisation befindet. Die PST-Dateien, die Sie in Office 365 importieren möchten, müssen sich in Ihrer Organisation auf einem Dateifreigabe-oder Dateiserver befinden.
    
    Beachten Sie, dass es einen optionalen Schritt gibt, den Sie ausführen können, um die Liste der PST-Dateien anzuzeigen, nachdem Sie an den Azure-Speicherort hochgeladen wurden.
    
3. **Erstellen einer PST-Import Zuordnungsdatei** -nachdem die PST-Dateien an den Azure-Speicherort hochgeladen wurden, besteht der nächste Schritt darin, eine CSV-Datei (Comma Separated Value) zu erstellen, die angibt, in welche Benutzerpostfächer die PST-Dateien importiert werden sollen, beachten Sie, dass eine PST-Datei  in das primäre Postfach eines Benutzers oder in sein Archivpostfach importiert. Der Office 365-Import Dienst verwendet die Informationen in der CSV-Datei, um die PST-Dateien zu importieren.
    
4. **Erstellen eines PST-importauftrags** – im nächsten Schritt erstellen Sie auf der Seite " **importieren** " im Security &amp; Compliance Center einen PST-Importauftrag und übermitteln die im vorherigen Schritt erstellte PST-Import Zuordnungsdatei. Nachdem Sie den Importauftrag erstellt haben, analysiert Office 365 die Daten in den PST-Dateien und bietet Ihnen dann die Möglichkeit, Filter festzulegen, die Steuern, welche Daten tatsächlich in die in der PST-Import Zuordnungsdatei angegebenen Postfächer importiert werden. 
    
5. **Filtern der PST-Daten, die in Postfächer importiert werden** -nachdem der Importauftrag erstellt und gestartet wurde, analysiert Office 365 die Daten in den PST-Dateien (sicher und sicher), indem das Alter der Elemente und die unterschiedlichen Nachrichtentypen in den PST-Dateien ermittelt werden. . Wenn die Analyse abgeschlossen ist und die Daten zum Importieren bereit sind, haben Sie die Möglichkeit, alle in den PST-Dateien enthaltenen Daten zu importieren, oder Sie können die importierten Daten trimmen, indem Sie Filter festlegen, die Steuern, welche Daten importiert werden.
    
6. **Starten des PST-importauftrags** – nachdem der Importauftrag gestartet wurde, verwendet Office 365 die Informationen in der PST-Import Zuordnungsdatei, um die PST-Dateien aus dem Azure-Speicher Speicherort in Benutzerpostfächer zu importieren. Status Informationen zum Importauftrag (einschließlich Informationen zu jeder importierten PST-Datei) werden auf der Seite " **importieren** " im Security &amp; Compliance Center angezeigt. Wenn der Importauftrag abgeschlossen ist, wird der Status für den Auftrag auf **abgeschlossen**festgelegt.
  
## <a name="more-information"></a>Weitere Informationen

- Gründe für das Importieren von PST-Dateien in Office 365
    
  - Es ist eine gute Möglichkeit, die Archivierungs Nachrichtendaten Ihrer Organisation in Office 365 zu importieren.
    
  - Die Daten sind für den Benutzer auf allen Geräten verfügbar, da Sie in der Cloud gespeichert sind.
    
  - Sie unterstützt die Einhaltung der Compliance-Anforderungen Ihrer Organisation, indem Sie Office 365-Kompatibilitätsfeatures auf die Daten aus den importierten PST-Dateien anwenden lassen. Dies umfasst Folgendes:
    
  - Aktivieren von [archivpostfächern](enable-archive-mailboxes.md) und [Automatisches Erweitern der Archivierung](enable-unlimited-archiving.md) , um Benutzern zusätzlichen Postfachspeicher Platz zum Speichern der importierten Daten zu geben. 
    
  - Platzieren von Postfächern in der [Beweis](https://go.microsoft.com/fwlink/?linkid=856286) Sicherung, um die importierten Daten beizubehalten. 
    
  - Verwenden von Microsoft [eDiscovery-Tools](search-for-content.md) zum Durchsuchen der importierten Daten. 
    
  - Verwenden von [Office 365-Aufbewahrungsrichtlinien](retention-policies.md) , um zu steuern, wie lange die importierten Daten aufbewahrt werden, und welche Aktion nach Ablauf des Aufbewahrungszeitraums durchgeführt werden soll. 
    
  - DurchSuchen des [Office 365-Überwachungsprotokolls](search-the-audit-log-in-security-and-compliance.md) für Post fachbezogene Ereignisse, die sich auf die importierten Daten auswirken. 
    
  - Importieren von Daten in inaktive [Postfächer](create-and-manage-inactive-mailboxes.md) zum Archivieren von Daten zu Compliance-Zwecken 
    
  - Verwenden von Richtlinien zur Verhinderung von [Datenverlust](data-loss-prevention-policies.md) , um zu verhindern, dass vertrauliche Daten außerhalb Ihrer Organisation verloren gehen. 
  
- NachFolgend finden Sie ein Beispiel für die SAS-URL (Shared Access Signature), die in Schritt 1 abgerufen wird. Dieses Beispiel enthält auch die Syntax für den Befehl, den Sie im Tool AzCopy. exe ausführen, um PST-Dateien in Office 365 hochzuladen. Achten Sie darauf, die SAS-URL genau so zu schützen, wie Sie Kennwörter oder andere sicherheitsrelevante Informationen schützen würden.

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
    
