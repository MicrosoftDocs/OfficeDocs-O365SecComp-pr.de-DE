---
title: Verwenden Sie Laufwerk des Protokollversands, um Ihre Organisation PST-Dateien in Office 365 zu importieren
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 6/14/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 40829b57-793c-4d41-b171-e9270129173d
description: 'Für Administratoren: erfahren Sie, wie PST-Dateien in Office 365-Postfächer Ihrer Organisation Massenimport von PST-Dateien auf einer Festplatte kopiert, und klicken Sie dann auf Microsoft Lieferung. '
ms.openlocfilehash: ebe88918b6c25e18562db7817d22fbf71f05e4c7
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529366"
---
# <a name="use-drive-shipping-to-import-your-organization-pst-files-to-office-365"></a>Verwenden Sie Laufwerk des Protokollversands, um Ihre Organisation PST-Dateien in Office 365 zu importieren

**Dieser Artikel ist für Administratoren. Versuchen Sie zum Importieren von PST-Dateien an Ihrem eigenen Postfach? Finden Sie unter [Import e-Mail, Kontakte und Kalender aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)**
   
Importieren von Office 365-Dienst und PST-Dateien auf die Benutzerpostfächer Massenimport Protokollversand Laufwerk verwenden. Laufwerk des Protokollversands bedeutet, dass Sie kopieren Sie die PST-Dateien auf einer Festplatte, und klicken Sie dann das Laufwerk an Microsoft physisch liefern. Wenn Microsoft Festplatte empfängt, werden Mitarbeitern des Rechenzentrums die Daten von der Festplatte auf einen Speicherbereich in der Microsoft-Cloud kopiert. Klicken Sie dann haben Sie die Möglichkeit zu erhöhen, die PST-Daten, die tatsächlich an die Ziel-Postfächer importiert wird durch Festlegen von Filtern, die steuern, welche Daten importierten abruft. Nachdem Sie den Importauftrag gestartet haben, importiert der Import-Dienst die PST-Daten aus Bereich für die Speicherung auf Benutzerpostfächer an. Laufwerk des Protokollversands zum Importieren von PST-Dateien auf die Benutzerpostfächer mit ist eine Möglichkeit zum Migrieren von e-Mail von Ihrer Organisation zu Office 365.
  
Hier sind die erforderlichen Schritte zum Importieren von PST-Dateien in Office 365-Postfächer verwenden Laufwerk ausgeliefert:
  
[Schritt 1: Laden Sie den Schlüssel sicherer Speicher und PST-Importtool](#step-1-download-the-secure-storage-key-and-pst-import-tool)

[Schritt 2: Kopieren Sie die PST-Dateien auf der Festplatte](#step-2-copy-the-pst-files-to-the-hard-drive)

[Schritt 3: Erstellen Sie die Datei zur Zuordnung von PST-Import](#step-3-create-the-pst-import-mapping-file)

[Schritt 4: Erstellen eines PST-Importauftrags in Office 365](#step-4-create-a-pst-import-job-in-office-365)

[Schritt 5: Versenden der Festplatte an Microsoft](#step-5-ship-the-hard-drive-to-microsoft)

[Schritt 6: Filtern von Daten, und starten Sie den Importauftrag PST-Datei](#step-6-filter-data-and-start-the-pst-import-job)
  
> [!IMPORTANT]
> Sie müssen Schritt 1 einmal ausführen, um den Schlüssel sicherer Speicher und die Importtools laden herunter. Nachdem Sie diese Schritte ausgeführt haben, führen Sie Schritt2 bis 6, die jedes Mal zu eine Festplatte an Microsoft zu liefern. 
  
Für die häufig Fragen zur Verwendung von Laufwerk ausgeliefert zum Importieren von PST-Dateien in Office 365 finden Sie unter [häufig gestellte Fragen für die Verwendung von Laufwerk ausgeliefert zum Importieren von PST-Dateien](faqimporting-pst-files-to-office-365.md#using-drive-shipping-to-import-pst-files). 
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen die Rolle Postfach importieren exportieren in Exchange Online zum Importieren von PST-Dateien in Office 365-Postfächer zugewiesen werden. Standardmäßig ist nicht dieser Rolle alle Rollengruppe in Exchange Online zugewiesen. Sie können die Rollengruppe "Organisationsverwaltung" Postfach Import/Export-Rolle hinzufügen. Oder erstellen eine neuen Rollengruppe, weisen Sie die Rolle Postfach Import/Export und fügen Sie sich als Mitglied hinzu. Weitere Informationen finden Sie unter "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" Abschnitte auf [Rollengruppen verwalten](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Darüber hinaus Import erstellen Aufträge in der Office 365-Sicherheit &amp; Compliance Center, eine der folgenden muss true sein:
    
  - Sie müssen die Rolle des E-Mail-Empfänger in Exchange Online zugewiesen werden. Standardmäßig wird diese Rolle der Organization Management und Recipient Management Rollen Gruppen zugewiesen.
    
    oder -
    
  - Sie müssen ein globaler Administrator in Office 365-Organisation sein.
    
    > [!TIP]
    > Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange-Online, die speziell für das Importieren von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die Mindestebene von Berechtigungen, die zum Importieren von PST-Dateien erforderlich sind der neuen Rollengruppe die Rollen Postfach importieren exportieren und E-Mail-Empfänger, und fügen Sie Mitglieder. 
  
- Sie müssen die PST-Dateien zu speichern, die Sie auf einer Festplatte auf einem Dateiserver oder freigegebenen Ordner in Ihrer Organisation zu kopieren möchten. In Schritt2 ausführen Sie des Azure Import/Export (WAImportExport.exe), die die PST-Dateien, die auf diesem Dateiserver gespeichert sind oder freigegebenen Ordner auf der Festplatte Daten kopiert werden.
    
- Nur 2,5 Zoll Solid-State-Laufwerke (SSDs) oder 2.5 oder 3,5 Zoll SATA II/III interne Festplatten für die Verwendung mit dem Import von Office 365-Dienst unterstützt werden. Festplatten können bis zu 10 TB. Für Projekte importieren wird nur die erste Datenvolumen auf der Festplatte verarbeitet werden. Das Datenvolume muss mit NTFS formatiert werden. Beim Kopieren von Daten auf einer Festplatte, verknüpfen Sie ihn direkt mit einem 2,5 Zoll SSD 2.5 oder 3.5 Zoll SATA II/III Connector oder können Sie es extern mit externen 2,5 Zoll SSD oder 2.5 oder 3,5 Zoll SATA II/III USB-Adapter anfügen.
    
    > [!IMPORTANT]
    > Externe Festplatten, die mit einer integrierten USB-Adapter geliefert werden vom Office 365-Import-Dienst nicht unterstützt. Darüber hinaus kann nicht innerhalb der Groß-/Kleinschreibung von einer externen Festplatte Datenträger verwendet werden. Bitte versenden Sie nicht externe Festplatten. 
  
- Die Festplatte, der Sie die PST-Dateien zu kopieren, muss mit BitLocker verschlüsselt werden. Das WAImportExport.exe-Tool, das Sie in Schritt2 ausführen helfen Ihnen die BitLocker einrichten. Generiert wird, auch einem Verschlüsselungsschlüssel BitLocker, dass Microsoft Mitarbeiter im Rechenzentrum verwendet werden, um Zugriff auf das Laufwerk die PST-Dateien in den Bereich der Azure-Speicher in der Microsoft-Cloud hochladen.
    
- Laufwerk des Protokollversands ist über Microsoft Enterprise Agreement (EA) verfügbar. Laufwerk des Protokollversands nicht über eine Microsoft Products and Services Vereinbarung (MPSA) zur Verfügung.
    
- Die Kosten für die PST-Dateien in Office 365-Postfächer, die mithilfe des Protokollversands Laufwerk importieren ist 2 US-Dollar pro GB Daten. Wenn Sie eine Festplatte, die 1.000 GB (1 TB) PST-Dateien enthält liefern, ist die Kosten beispielsweise 2.000 US-Dollar. Sie können mit einem Partner die Import-Gebühr Zahlen arbeiten. Informationen zum Suchen nach einem Partner finden Sie unter [finden Ihrer Office 365-Partner oder Händler](https://go.microsoft.com/fwlink/p/?LinkId=785197).
    
- Sie bzw. Ihre Organisation müssen über ein Konto bei FedEx oder DHL verfügen. 
    
  - Organisationen in den USA, Brasilien und Europa müssen FedEx Konten verfügen.
    
  - Organisationen in Ostasien, Südost Asien, Japan, Republik Korea und Australien müssen DHL Konten verfügen.
    
    Microsoft verwendet (und belastet) dieses Konto, um die Festplatte an Sie zurückzusenden. 
    
- Beim Versand der Festplatte an Microsoft werden möglicherweise internationale Grenzen überschritten. Wenn dies der Fall ist, sind Sie dafür verantwortlich, dass die Festplatte und die darauf befindlichen Daten in Übereinstimmung mit dem jeweils geltenden Recht importiert bzw. exportiert werden. Erkundigen Sie sich vor dem Versenden der Festplatte bei dem entsprechenden Berater, ob die Festplatte und die Daten legal an das angegebene Microsoft-Rechenzentrum versandt werden können. Dadurch wird sichergestellt, dass die Festplatte Microsoft termingerecht erreicht.
    
- Bei diesem Verfahren werden kopieren und Speichern einer sicherer Speicher und ein BitLocker-Verschlüsselungsschlüssel. Achten Sie darauf, müssen Sie Vorsichtsmaßnahmen gegen diese Schlüssel schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen zu schützen. Beispielsweise können Sie auf kennwortgeschützte Microsoft Word-Dokument speichern oder in ein verschlüsseltes USB-Laufwerk speichern. Finden Sie [Weitere Informationen](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) im Abschnitt ein Beispiel für diese Schlüssel. 
    
- Nachdem PST-Dateien in ein Office 365-Postfach importiert wurden, ist die Einstellung für das Postfach Anhalten der Aufbewahrungszeit für unbefristete aktiviert. Dies bedeutet, dass die Aufbewahrungsrichtlinie an das Postfach zugewiesen, bis Sie das Anhalten der Aufbewahrungszeit deaktivieren oder ein Datums festlegen So deaktivieren Sie den Haltestatus verarbeitet wird. Warum tun wir das? Wenn Sie Nachrichten in einem Postfach importiert alt sind, sie möglicherweise werden endgültig gelöscht (gelöscht), da der Aufbewahrungszeitraum abgelaufen ist basierend auf der aufbewahrungseinstellungen für das Postfach konfiguriert. Platzieren das Postfach auf Anhalten der Aufbewahrungszeit erhalten die Postfach Besitzer Zeit zum Verwalten dieser Nachrichten neu importiert oder geben Sie Zeit, um die Einstellungen für die Aufbewahrung für das Postfach zu ändern. Finden Sie im Abschnitt [Weitere Informationen](use-drive-shipping-to-import-pst-files-to-office-365.md#moreinfo) zum Verwalten von das Anhalten der Aufbewahrungszeit Vorschläge. 
    
- Standardmäßig ist die maximale Größe von Nachrichten, die von Office 365-Postfach empfangen werden kann 35 MB. Das liegt, da der Standardwert für die *MaxReceiveSize* -Eigenschaft für ein Postfach auf 35 MB festgelegt ist. Für die maximale Meldung Größe in Office 365 ist die Grenze jedoch 150 MB. Wenn Sie eine PST-Datei importieren, enthält ein Element größer als 35 MB, die wir ändert automatisch den Wert der *MaxReceiveSize* -Eigenschaft für das Zielpostfach auf 150 MB Importieren von Office 365-Dienst. Auf diese Weise können Nachrichten bis zu 150 MB für Benutzerpostfächer importiert werden. 
    
    > [!TIP]
    > Identifiziert die Meldung Größe für ein Postfach, können Sie diesen Befehl ausführen, in Exchange Online PowerShell: `Get-Mailbox <user mailbox> | FL MaxReceiveSize`. 
  
- Sie können PST-Dateien in eines inaktiven Postfachs in Office 365 importieren. Zu diesem Zweck Angabe der GUID des inaktiven Postfachs in die `Mailbox` Parameter in der Zuordnungsdatei PST-Datei importieren. Finden Sie unter [Schritt 3: Erstellen Sie die Datei zur Zuordnung von PST-Import](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) Weitere Informationen. 
    
- In einer Exchange-hybridbereitstellung können Sie PST-Dateien in einer Cloud-basierten Archivpostfach für einen Benutzer importieren, deren Hauptpostfach lokal wurde. Dabei wird in der Zuordnungsdatei Import von PST-Datei wie folgt:
    
  - Geben Sie die e-Mail-Adresse für das Postfach des Benutzers: lokal in der `Mailbox` Parameter. 
    
  - Geben Sie den Wert **"true"** in der `IsArchive` Parameter. 
    
    Finden Sie unter [Schritt 3: Erstellen Sie die Datei zur Zuordnung von PST-Import](use-drive-shipping-to-import-pst-files-to-office-365.md#step3) Weitere Informationen. 

## <a name="step-1-download-the-secure-storage-key-and-pst-import-tool"></a>Schritt 1: Laden Sie den Schlüssel sicherer Speicher und PST-Importtool

Der erste Schritt besteht, laden Sie den Schlüssel sicherer Speicher und das Tool, und Sie werden in Schritt2 verwenden, um Kopie von PST-Dateien auf der Festplatte.
  
> [!IMPORTANT]
> Sie müssen Azure Import/Export Tool Version 1 (WAimportExportV1) verwenden, um erfolgreich importieren PST-Dateien mithilfe der Protokollversand Laufwerk-Methode. 2-Version des Azure Import/Export-Tools nicht unterstützt wird und dessen Verwendung, bewirken nicht ordnungsgemäß für den Importauftrag Vorbereiten der Festplatte. Achten Sie darauf, dass Sie die Sicherheit das Azure-Import/Export-Tool heruntergeladen werden &amp; Compliance Center mit den Verfahren in diesem Schritt. 
  
1. Wechseln Sie zu [https://protection.office.com/](https://protection.office.com/) und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Governance** \> **Importieren**.
    
    > [!NOTE]
    > Wie bereits erwähnt, müssen Sie die entsprechenden Berechtigungen Zugriff auf die Seite **Importieren** in das Wertpapier zugewiesen werden &amp; Compliance Center. 
  
3. Klicken Sie auf der Seite **Importieren** auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Importauftrag neu**.
    
4. Der Auftrag Zertifikatimport-Assistenten geben Sie einen Namen für den Auftrag für Import von PST-Datei ein, und klicken Sie dann auf **Weiter**. Verwenden Sie Kleinbuchstaben, Zahlen, Bindestriche und Unterstriche. In Großbuchstabe können nicht oder Leerzeichen im Namen enthalten.
    
5. Klicken Sie auf der Seite **Choose importieren Auftragstyp** auf **liefern-Festplatten auf eine der unsere physische Standorte** , und klicken Sie dann auf **Weiter**.
    
    ![Klicken Sie auf liefern Festplatten auf eine der unsere physische Standorte Erstellen eines Laufwerks shipping Auftrag für import](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. Führen Sie auf der Seite **Daten importieren** die folgenden beiden Schritte aus: 
    
    ![Kopieren Sie den Schlüssel sicherer Speicher und Laden Sie das Tool Azure Import/Export auf der Seite Daten importieren](media/e22e0b48-e5ce-48e0-95bc-0490a2b3b983.png)
  
    a. Klicken Sie in Schritt 2 Klicken Sie auf **Kopieren Sie den Schlüssel sicherer Speicher**. Nachdem der Speicherschlüssel angezeigt wird, auf **in die Zwischenablage kopieren** und fügen Sie ihn und in einer Datei speichern Sie, damit Sie später zugreifen können.
    
    b. in Schritt 3, herunterladen und installieren Sie das Tool Azure Import/Export (Version 1) **Herunterladen des Azure Import/Export-Tools** .
    
    - Klicken Sie auf **Speichern** , klicken Sie im Popupfenster \> zum Speichern der WaImportExportV1.zip-Datei in einen Ordner auf Ihrem lokalen Computer **Speichern** . 
    
    - Extrahieren Sie die Datei WaImportExportV1.zip.
    
7. Klicken Sie auf **Abbrechen** , um den Assistenten zu schließen. 
    
    Sie können später auf der Seite **Importieren** in das Wertpapier &amp; Compliance Center, wenn Sie in Schritt 4 den Importauftrag erstellen. 

## <a name="step-2-copy-the-pst-files-to-the-hard-drive"></a>Schritt 2: Kopieren Sie die PST-Dateien auf der Festplatte

Im nächste Schritt wird mit dem WAImportExport.exe Tool zum Kopieren von PST-Dateien auf der Festplatte. Dieses Tool die Festplatte mit BitLocker verschlüsselt, die PST-Dateien auf der Festplatte kopiert und erstellt eine Journaldatei, die Informationen zu den Kopiervorgang gespeichert. Wenn Sie diesen Schritt abgeschlossen haben, müssen die PST-Dateien in einer Dateifreigabe oder Dateiserver in Ihrer Organisation befinden. Dies wird als Quellverzeichnis in der folgenden Prozedur bezeichnet. 
  
> [!IMPORTANT]
> Nach des WAImportExport.exe beim ersten für eine Festplatte ausführen müssen Sie verwenden eine andere Syntax jedes Mal nach. Mit dieser Syntax wird in Schritt 4 dieses Verfahrens zum Kopieren von PST-Dateien auf der Festplatte erläutert. 
  
1. Öffnen Sie eine Eingabeaufforderung auf dem lokalen Computer.
    
    > [!TIP]
    > Wenn Sie die Eingabeaufforderung als Administrator ausführen (durch Auswahl von „Als Administrator ausführen“ beim Öffnen), werden im Fenster der Eingabeaufforderung Fehlermeldungen angezeigt. Dies kann Ihnen bei der Behandlung von Problemen beim Ausführen des Tools „WAImportExport.exe“ helfen. 
  
2. Wechseln Sie zu dem Verzeichnis, in dem Sie das Tool „WAImportExport.exe“ in Schritt 1 installiert haben.
    
3. Wenn Sie „WAImportExport.exe“ zum ersten Mal verwenden, um die PST-Dateien auf eine Festplatte zu kopieren, führen Sie den folgenden Befehl aus.

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /t:<Drive letter> /id:<Name of session> /srcdir:<Location of PST files> /dstdir:<PST file path> /sk:<Storage account key> /encrypt /logdir:<Log file location>
    ```

    In der folgenden Tabelle werden die Parameter und deren erforderliche Werte beschrieben.
    
    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `/j:` <br/> |Gibt den Namen der Journaldatei an. Diese Datei wird im selben Ordner gespeichert, in dem sich das Tool „WAImportExport.exe“ befindet. Jede Festplatte, die Sie an Microsoft senden, muss eine Journaldatei enthalten. Jedes Mal, wenn Sie „WAImportTool.exe“ zum Kopieren von PST-Dateien auf eine Festplatte ausführen, werden Informationen zur Journaldatei dieser Festplatte hinzugefügt. 
  <br/> Mitarbeiter im Rechenzentrum Microsoft anhand der Informationen in die Journal-Datei an, die Festplatte den Importauftrag zugeordnet, die Sie in Schritt 4 erstellen und die PST-Dateien in den Bereich der Azure-Speicher in der Microsoft-Cloud hochladen.  <br/> | `/j:PSTHDD1.jrn` <br/> |
    | `/t:` <br/> |Gibt den Buchstaben des Laufwerks an, wenn die Festplatte an Ihren lokalen Computer angeschlossen ist.  <br/> | `/t:h` <br/> |
    | `/id:` <br/> |Gibt den Namen der Kopiersitzung an. Eine Sitzung ist definiert als jeder einzelne Vorgang, in dem Sie das Tool „WAImportExport.exe“ ausführen und Dateien auf die Festplatte kopieren. Die PST-Dateien werden in einen Ordner mit dem Namen der Sitzung kopiert, der durch diesen Parameter angegeben wird.   <br/> | `/id:driveship1` <br/> |
    | `/srcdir:` <br/> |Gibt das Quellverzeichnis in Ihrer Organisation, die die PST-Dateien enthält, die während der Sitzung kopiert werden. Achten Sie darauf, um den Wert dieses Parameters mit doppelte Anführungszeichen umgeben ("").  <br/> | `/srcdir:"\\FILESERVER01\PSTs"` <br/> |
    | `/dstdir:` <br/> |Gibt das Zielverzeichnis im Bereich Azure-Speicher in der Microsoft-Cloud, in die PST-Dateien hochgeladen werden soll. Sie müssen den Wert verwenden `ingestiondata/`. Achten Sie darauf, um den Wert dieses Parameters mit doppelte Anführungszeichen umgeben ("").<br/> Optional können Sie auch einen zusätzliche Pfad auf den Wert dieses Parameters hinzufügen. Sie können beispielsweise den Dateipfad der Source-Verzeichnis auf der Festplatte (konvertiert in ein URL-Format), die in angegeben ist die `/srcdir:` Parameter. Beispielsweise `\\FILESERVER01\PSTs` wird geändert in `FILESERVER01/PSTs`. In diesem Fall weiterhin muss enthalten `ingestiondata` in den Dateipfad. In diesem Fall in diesem Beispiel wird der Wert für die `/dstdir:` Parameter wäre `"ingestiondata/FILESERVER01/PSTs"`.<br/> Ein Grund für das Hinzufügen des zusätzliche Pfads ist, wenn Sie PST-Dateien mit dem gleichen Dateinamen vorhanden sind.  <br/> > [!NOTE]> Wenn Sie die optionale Pathname enthalten, muss der Namespace für eine PST-Datei, nachdem er auf den Bereich der Azure-Speicher hochgeladen wird der Pfad und der Name der PST-Datei enthalten; beispielsweise `FILESERVER01/PSTs/annb.pst`. Wenn Sie einen Pfadnamen angeben, ist der Namespace nur der Dateiname PST; beispielsweise `annb.pst`.           | `/dstdir:"ingestiondata/"` <br/> oder -  <br/>  `/dstdir:"ingestiondata/FILESERVER01/PSTs"` <br/> |
    | `/sk:` <br/> |Gibt den Speicher Konto Schlüssel, den Sie erhalten in Schritt 1 an. Achten Sie darauf, um den Wert dieses Parameters mit doppelte Anführungszeichen umgeben ("").  <br/> | `"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ=="` <br/> |
    | `/encrypt` <br/> |Diese Option aktiviert BitLocker für die Festplatte. Dieser Parameter ist beim erstmaligen Ausführen des Tools „WAImportExport.exe“ erforderlich.  <br/> Der BitLocker-Verschlüsselungsschlüssel kopiert die Journal-Datei und die Protokolldatei, die erstellt wird, wenn Sie verwenden die `/logfile:` Parameter. Wie bereits erklärt wird die Journal-Datei im gleichen Ordner gespeichert, in das Tool WAImportExport.exe gespeichert ist.<br/> | `/encrypt` <br/> |
    | `/logdir:` <br/> |Dieser optionale Parameter gibt einen Ordner, um Protokolldateien zu speichern. Wenn nicht angegeben, werden die Protokolldateien speichern im gleichen Ordner, in das Tool WAImportExport.exe gespeichert ist. Achten Sie darauf, um den Wert dieses Parameters mit doppelte Anführungszeichen umgeben ("").  <br/> | `/logdir:"c:\users\admin\desktop\PstImportLogs"` <br/> |
   
    Nachfolgend sehen Sie ein Beispiel der Syntax für das Tool „WAImportExport.exe“, in dem die tatsächlichen Werte für jeden Parameter verwendet werden:
    
    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /t:f /id:driveship1 /srcdir:"\\FILESERVER01\PSTs" /dstdir:"ingestiondata/" /sk:"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==" /encrypt /logdir:"c:\users\admin\desktop\PstImportLogs"
    ```

    Nachdem Sie den Befehl ausgeführt haben, werden Statusmeldungen angezeigt, die den Fortschritt des Kopierens der PST-Dateien auf die Festplatte anzeigen. Eine endgültige Statusmeldung zeigt die Gesamtzahl der Dateien an, die erfolgreich kopiert wurden. 
    
4. Führen Sie diesen Befehl jedes Mal aus, wenn Sie das Tool „WAImportExport.exe“ zum Kopieren der PST-Dateien auf dieselbe Festplatte ausführen.

    ```
    WAImportExport.exe PrepImport /j:<Name of journal file> /id:<Name of new session> /srcdir:<Location of PST files> /dstdir:<PST file path> 
    ```

    Im Folgenden sehen Sie ein Beispiel der Syntax für die Ausführung weiterer Sitzungen zum Kopieren von PST-Dateien auf dieselbe Festplatte.  

    ```
    WAImportExport.exe PrepImport /j:PSTHDD1.jrn /id:driveship2 /srcdir:"\\FILESERVER01\PSTs\SecondBatch" /dstdir:"ingestiondata/"
    ```

## <a name="step-3-create-the-pst-import-mapping-file"></a>Schritt 3: Erstellen Sie die Datei zur Zuordnung von PST-Import

Nach dem Hochladen der PST-Dateien von der Festplatte zu dem Azure-Speicherbereich Microsoft Mitarbeiter im Rechenzentrum wird der Import-Dienst die Informationen in der Zuordnungsdatei PST-Import verwenden die ist eine durch Kommas getrennten Werten (CSV)-Datei, die angibt, welche Benutzerpostfächer der PST-Datei Dateien werden in importiert werden. Sie senden diese CSV-Datei im nächsten Schritt beim Erstellen eines Auftrags PST-Datei importieren.
  
1. [Laden Sie eine Kopie der Zuordnungsdatei PST -Datei importieren](https://go.microsoft.com/fwlink/p/?LinkId=544717).
    
2. Öffnen oder speichern Sie die CSV-Datei auf Ihrem lokalen Computer. Das folgende Beispiel zeigt eine abgeschlossene PST-Importzuordnungsdatei (in Editor geöffnet). Es ist wesentlich einfacher, Microsoft Excel zum Bearbeiten der CSV-Datei zu verwenden.

    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,FILESERVER01/PSTs,annb.pst,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,annb_archive.pst,annb@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,FILESERVER01/PSTs,donh.pst,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,donh_archive.pst,donh@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,FILESERVER01/PSTs,pilarp.pst,pilarp@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,FILESERVER01/PSTs,pilarp_archive.pst,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,,tonyk.pst,tonyk@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,tonyk_archive.pst,tonyk@contoso.onmicrosoft.com,TRUE,,,,,
    Exchange,,zrinkam.pst,zrinkam@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,zrinkam_archive.pst,zrinkam@contoso.onmicrosoft.com,TRUE,,,,,
    ```

    Die erste Zeile oder Kopfzeile der CSV-Datei enthält die Parameter, die vom Dienst PST-Datei importieren zum Importieren der PST-Dateien auf die Benutzerpostfächer verwendet werden. Jeder Parametername wird durch ein Komma getrennt. Jede Zeile unter der Überschrift stellt die Parameterwerte zum Importieren einer PST-Datei in ein bestimmtes Postfach. Sie benötigen eine Zeile für jeden PST-Datei, die auf der Festplatte kopiert wurde. Achten Sie darauf, dass Sie die Platzhalterdaten in die Datei zur Zuordnung durch den tatsächlichen Daten ersetzen.

    > [!NOTE]
    > Ändern Sie nichts in der Kopfzeile, einschließlich der SharePoint-Parameter; diese werden während des PST-Importvorgangs ignoriert. 
  
3. Verwenden Sie die Informationen in der folgenden Tabelle, um zu die CSV-Datei mit den erforderlichen Informationen zu füllen.
    
    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Gibt den Office 365-Dienst, dem Daten importiert werden. Verwenden Sie zum Importieren von PST-Dateien auf die Benutzerpostfächer `Exchange`.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> | Gibt den Speicherort des Ordners im Bereich, dem PST-Dateien, kopiert werden, wenn die Festplatte geliefert wird an Microsoft Azure-Speicher an.  <br/>  Was Sie in dieser Spalte in der CSV-Datei hinzufügen, was Sie für in angegeben hängt die `/dstdir:` Parameter im vorherigen Schritt.  <br/>  Wenn Sie verwendet `/dstdir:"ingestiondata/"`, klicken Sie dann dieser Parameter leer lassen in der CSV-Datei.  <br/>  Wenn Sie einen optionalen Pfadname für den Wert des enthalten die `/dstdir:` Parameter (beispielsweise `/dstdir:"ingestiondata/FILESERVER01/PSTs"`, klicken Sie dann diese Pathname (nicht einschließlich "Ingestiondata") für diesen Parameter in der CSV-Datei verwenden. Der Wert für diesen Parameter ist Groß-/Kleinschreibung beachtet.<br/>  *In beiden Fällen nehmen "Ingestiondata" in den Wert für* die `FilePath` Parameter. Lassen Sie dieser Parameter leer, oder geben Sie nur den optionalen Pfadname.<br/> > [!IMPORTANT]> Die Groß-/Kleinschreibung für den Namen der Pfad muss die Groß-/Kleinschreibung, die Sie in der `/dstdir:` Parameter im vorherigen Schritt. Beispielsweise, wenn Sie verwendet `"ingestiondata/FILESERVER01/PSTs"` für den Namen des Unterordners im vorherigen Schritt, klicken Sie dann verwendet, aber `fileserver01/psts` in der `FilePath` schlägt fehl, Parameter in der CSV-Datei, die für die PST-Datei importieren. Achten Sie darauf, dass die Groß-/Kleinschreibung in beiden Fällen verwenden.           |(leer lassen)  <br/> Oder  <br/>  `FILESERVER01/PSTs` <br/> |
    | `Name` <br/> |Gibt den Namen der PST-Datei, die für das Postfach des Benutzers importiert werden. Der Wert für diesen Parameter ist Groß-/Kleinschreibung beachtet.<br/> > [!IMPORTANT]> Die Groß-/Kleinschreibung für den Namen des PST-Datei in der CSV-Datei muss die gleiche wie die PST-Datei, die in der Azure Speicherort in Schritt2 hochgeladen wurde. Angenommen, Sie verwenden `annb.pst` in der `Name` Parameter in der CSV-Datei, aber der Name der PST-Datei ist `AnnB.pst`, schlägt der Import für die PST-Datei fehl. Stellen Sie sicher, dass der Name der PST-Datei in der CSV-Datei die gleiche Groß-/Kleinschreibung als die eigentliche PST-Datei verwendet wird.           | `annb.pst` <br/> |
    | `Mailbox` <br/> |Gibt die e-Mail-Adresse des Postfachs an, das die PST-Datei importiert werden. Beachten Sie, dass Sie einen öffentlichen Ordner angeben ist nicht möglich, da der PST-Import-Dienst unterstützt Import von PST-Dateien auf Öffentliche Ordner.<br/> Um eine PST-Datei in eines inaktiven Postfachs zu importieren, müssen Sie die Postfach-GUID für diesen Parameter angeben. Um diese GUID zu erhalten, führen Sie den folgenden PowerShell-Befehl in Exchange Online: "Get-Mailbox <identity of inactive mailbox> - InactiveMailboxOnly | FL Guid` <br/> > [!NOTE]> In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have to specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox<identity of active mailbox> | FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command:  `Get-Mailbox <identity of soft-deleted or inactive mailbox> - SoftDeletedMailbox | FL Guid ".           | `annb@contoso.onmicrosoft.com` <br/> oder -  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Gibt an, ob die PST-Datei in das Archivpostfach des Benutzers importiert werden soll. Es gibt zwei Möglichkeiten:<br/> **"False"** Importiert die PST-Datei zum primären Postfach des Benutzers.  <br/> **"True"** Importiert die PST-Datei in Archivpostfach des Benutzers an. Dies setzt voraus, dass das [Archivpostfach des Benutzers ist aktiviert](enable-archive-mailboxes.md). Wenn Sie diesen Parameter auf setzen `TRUE` und Archivpostfach des Benutzers ist nicht aktiviert, schlägt der Import für diesen Benutzer fehl. Beachten Sie, dass, wenn ein Import für einen Benutzer ein Fehler auftritt (, da ihre Archiv ist nicht aktiviert, und diese Eigenschaft, um festgelegt wird `TRUE`), die andere Benutzer in den Importauftrag wird nicht beeinflusst werden.<br/>  Wenn Sie diesen Parameter leer lassen, wird die PST-Datei in der primären Postfach des Benutzers importiert.  <br/> **Hinweis:** Geben Sie einfach eine PST-Datei in einer Cloud-basierten Archivpostfach für einen Benutzer Sie zum Importieren, deren primäre Postfach der lokale ist `TRUE` für diesen Parameter, und geben Sie die e-Mail-Adresse für das Postfach des Benutzers: lokal für die `Mailbox` Parameter.  <br/> | `FALSE` <br/> oder -  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Gibt den Postfachordner, dem in die PST-Datei importiert wird.  <br/>  Wenn dieser Parameter leer lassen, wird die PST-Datei in einen neuen Ordner importiert werden benannten **importierte** auf der Stammebene des Postfachs (der gleichen Ebene wie der Ordner Posteingang und anderen standardmäßigen Postfachordner) befinden.  <br/>  Wenn Sie angeben `/`, Elemente in der PST-Datei importiert werden direkt im Ordner Posteingang des Benutzers.  <br/>  Wenn Sie angeben `/<foldername>`, Elemente in der PST-Datei in einen Ordner namens importiert werden * \<Foldername\> * . Wenn Sie verwenden, beispielsweise `/ImportedPst`, würde Elemente in einen Ordner namens **ImportedPst**importiert werden. Dieser Ordner wird im Postfach des Benutzers auf derselben Ebene wie der Ordner Posteingang befinden.<br/> |(leer lassen)  <br/> Oder  <br/>  `/` <br/> oder -  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Dieser optionale Parameter gibt einen numerischen Wert für die Codepage für den Import von PST-Dateien im ANSI-Format verwenden. Dieser Parameter wird verwendet, für den Import von PST-Dateien von Organisationen Chinesisch, Japanisch und Koreanisch (CJK), da diese Sprachen in der Regel einen double-Byte-Zeichensatz (DBCS) für die zeichencodierung von verwenden. Wenn dieser Parameter wird nicht zum Importieren von PST-Dateien für Sprachen, die DBCS für Ordnernamen Postfach verwenden verwendet, werden die Namen der Ordner häufig verzerrt, nach dem Importieren.<br/> Eine Liste der unterstützten Werte für diesen Parameter verwenden finden Sie unter [Code Seite Bezeichner](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/> > [!NOTE]> Wie zuvor erwähnt, dies ist ein optionaler Parameter, und Sie keinen zum Einschließen in die CSV-Datei. Oder Sie können einschließen und den Wert für eine oder mehrere Zeilen leer lassen.           |(leer lassen)  <br/> Oder  <br/>  `932`(Dies ist der Bezeichner für Japanisch ANSI/OEM-Seite)  <br/> |
    | `SPFileContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPManifestContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPSiteUrl` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |

## <a name="step-4-create-a-pst-import-job-in-office-365"></a>Schritt 4: Erstellen eines PST-Importauftrags in Office 365

Der nächste Schritt besteht darin den Importauftrag PST-Datei im Dienst Import in Office 365 erstellen. Wie bereits erklärt senden Sie die PST-Import-Zuordnung-Datei, die Sie in Schritt 3 erstellt haben. Nachdem das neue Projekt erstellt wurde, wird der Import-Dienst anhand der Informationen in die Datei zur Zuordnung zum Importieren der PST-Dateien in das angegebene Postfach nach die PST-Dateien von der Festplatte zu dem Bereich der Azure-Speicher kopiert werden und erstellen und starten Sie den Importauftrag.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Steuerung** , und klicken Sie dann auf **Importieren**.
    
3. Klicken Sie auf der Seite **Importieren** auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Importauftrag neu**.
    
    > [!NOTE]
    > Wie bereits erwähnt, müssen Sie die entsprechenden Berechtigungen Zugriff auf die Seite **Importieren** in das Wertpapier zugewiesen werden &amp; Compliance Center. 
  
4. Geben Sie einen Namen für den Auftrag für Import von PST-Datei, und klicken Sie dann auf **Weiter**. Verwenden Sie Kleinbuchstaben, Zahlen, Bindestriche und Unterstriche. In Großbuchstabe können nicht oder Leerzeichen im Namen enthalten.
    
5. Klicken Sie auf der Seite **Choose importieren Auftragstyp** auf **liefern-Festplatten auf eine der unsere physische Standorte** , und klicken Sie dann auf **Weiter**.
    
    ![Klicken Sie auf liefern Festplatten auf eine der unsere physische Standorte Erstellen eines Laufwerks shipping Auftrag für import](media/1584fdc5-cd4c-4e47-932e-db6c8e07f5f8.png)
  
6. Klicken Sie in Schritt 6 Klicken Sie auf das Kontrollkästchen **ich meine Festplatten vorbereitet haben, und haben Zugriff auf Dateien der erforderlichen Journal** und **ich haben Zugriff auf die Datei zur Zuordnung** , und klicken Sie dann auf **Weiter**.
    
    ![Klicken Sie auf die zwei Kontrollkästchen in Schritt 6](media/fad43078-ea68-4acd-b2ed-75a800183262.png)
  
7. Klicken Sie auf der Seite **Wählen Sie die Datei Laufwerk** klicken Sie auf **Laufwerk Datei auswählen**, und wechseln Sie im gleichen Ordner, in dem das Tool WAImportExport.exe befindet. Die Journal-Datei, die in Schritt2 erstellt wurde, wurde in diesen Ordner kopiert.
    
    ![Klicken Sie auf Laufwerk-Datei, um die Journal-Datei zu übermitteln, die erstellt wurde, wenn Sie das Tool WAImportExport.exe ausgeführt wurde](media/1ea35c04-bd88-4d7e-b7d9-dc390149d94f.png)
  
8. Wählen Sie die Journal-Datei. beispielsweise `PSTHDD1.jrn`.
    
    > [!TIP]
    > Wenn Sie das Tool WAImportExport.exe in Schritt2 ausgeführt haben, wurde durch der Namen der Journaldatei angegeben die `/j:` Parameter. 
  
9. Nachdem Sie der Namen der Datei Laufwerk unter **Laufwerk Dateiname**angezeigt wird, klicken Sie auf **Überprüfen** , um Ihre Datei Laufwerk auf Fehler prüfen. 
    
    ![Klicken Sie auf überprüfen, um die Datei Laufwerk prüfen, die Sie ausgewählt haben](media/4b707f5a-152a-4e74-b9f5-449c88d1fec4.png)
  
    Die Datei Laufwerk muss erfolgreich überprüft werden, um einen Auftrag für Import von PST-Datei zu erstellen. Beachten Sie, dass der Dateiname auf Grün geändert wird, nachdem es erfolgreich überprüft wird. Wenn die Überprüfung fehlschlägt, klicken Sie auf den Link **Protokoll anzeigen** . Eine Überprüfung Fehlerbericht wird mit einer Fehlermeldung mit Informationen, warum die Datei konnte nicht geöffnet. 
    
    > [!NOTE]
    > Fügen Sie den, und überprüfen eine Journaldatei für jede Festplatte, die Sie an Microsoft zu liefern. 
  
10. Nach dem Hinzufügen und Validieren einer Journaldatei für jede Festplatte, die liefern Ihnen an Microsoft, klicken Sie auf **Weiter**.
    
11. Klicken Sie auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Zuordnungsdatei auswählen** , um die Datei zur Zuordnung von PST-Import zu senden, die Sie in Schritt 3 erstellt haben. 
    
    ![Klicken Sie auf Select Zuordnungsdatei, um die CSV-Datei, die Sie erstellt haben, für den Importauftrag übermitteln](media/d30b1d73-80bb-491e-a642-a21673d06889.png)
  
12. Nach dem Namen des im CSV-Format Datei unter **Mapping-Dateiname**angezeigt wird, klicken Sie auf **Überprüfen** , um die CSV-Datei auf Fehler zu überprüfen. 
    
    ![Klicken Sie auf überprüfen, um die CSV-Datei für Fehler sicherzustellen.](media/4680999d-5538-4059-b878-2736a5445037.png)
  
    Die CSV-Datei muss erfolgreich überprüft werden, um einen Auftrag für Import von PST-Datei zu erstellen. Beachten Sie, dass der Dateiname auf Grün geändert wird, nachdem es erfolgreich überprüft wird. Wenn die Überprüfung fehlschlägt, klicken Sie auf den Link **Protokoll anzeigen** . Eine Überprüfung Fehlerbericht wird mit einer Fehlermeldung für jede Zeile in der Datei geöffnet, die nicht erfolgreich. 
    
13. Nachdem die PST-Datei zur Zuordnung erfolgreich validiert wurde, klicken Sie auf **Weiter**.
    
14. Geben Sie auf der Seite **Provide Kontaktinformationen** Ihre Kontaktinformationen in die entsprechenden Felder ein. 
    
    Beachten Sie, dass die Adresse für den Microsoft-Speicherort, dem Sie Ihre Festplatten auf ausgeliefert wird angezeigt wird. Diese Adresse wird basierend auf Ihrer Office 365 Center Datenspeicherort automatisch generiert. Kopieren Sie diese Adresse in eine Datei oder einen Screenshot.
    
15. Lesen Sie die Geschäftsbedingungen, aktivieren Sie das Kontrollkästchen, und klicken Sie dann auf **Speichern** , um den Importvorgang zu senden. 
    
    Wenn der Auftrag für Import erfolgreich erstellt wurde, wird eine Statusseite angezeigt, die die nächsten Schritte des Laufwerks shipping Prozess erklärt.
    
16. Klicken Sie auf der Seite **Importieren** auf ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) **Aktualisieren** , um das neue Laufwerk ausgeliefert Importauftrag in der Liste der Importaufträge angezeigt. Beachten Sie, dass der Status zum **Warten auf laufende Nummer**festgelegt ist. Sie können auch den Importauftrag zum Anzeigen der Seite Status flyoutmenü die ausführlichere Informationen zu den Importauftrag enthält klicken.
 
## <a name="step-5-ship-the-hard-drive-to-microsoft"></a>Schritt 5: Versenden der Festplatte an Microsoft

Im nächste Schritt wird liefern die Festplatte an Microsoft, und geben Sie dann die laufende Nummer für die Lieferung und Zurückgeben von Informationen für den Versand Laufwerk Auftrag Lieferung. Nachdem das Laufwerk von Microsoft empfangen wurde, dauert zwischen 7 bis 10 Arbeitstagen für Daten Personal des Rechenzentrums PST-Dateien in den Bereich der Azure-Speicher für Ihre Organisation hoch es.
  
> [!NOTE]
> Wenn Sie die laufende Nummer und Lieferinformationen innerhalb von 14 Tagen erstellen Sie den Importauftrag nicht angeben, wird der Auftrag für Import abgelaufen. In diesem Fall müssen Sie zum Erstellen eines neuen Laufwerks shipping Importauftrag (finden Sie unter [Schritt 4: Erstellen einer PST-Importauftrag in Office 365](use-drive-shipping-to-import-pst-files-to-office-365.md#step4)), und übermitteln Sie erneut die Datei Laufwerk und die Datei zur Zuordnung von PST-Datei importieren. 
  
### <a name="ship-the-hard-drive"></a>Versenden der Festplatte

Beachten Sie die folgenden Punkte, wenn Sie Festplatten an Microsoft senden:
  
- Versenden Sie nicht den SATA-zu-USB-Adapter; Sie müssen nur die Festplatte zu liefern.
    
- Verpacken Sie die Laufwerke ordnungsgemäß; verwenden Sie z. B. antistatische Verpackung oder Luftpolsterfolie.
    
- Senden Sie die Festplatte mit einem Spediteur Ihrer Wahl an Microsoft.
    
- Liefern von der Festplatte auf die Adresse für den Microsoft-Speicherort, der angezeigt wurde, wenn Sie den Importauftrag in Schritt 4 erstellt haben. Achten Sie darauf, dass "Office 365 Import Dienst" in der Adresse enthalten.
    
- Nachdem Sie die Festplatte versendet haben, notieren Sie sich den Namen des Spediteurs und die Nachverfolgungsnummer. Diese müssen Sie im nächsten Schritt angeben.
    
### <a name="enter-the-tracking-number-and-other-shipping-information"></a>Eingabe der Nachverfolgungsnummer und anderer Versandinformationen

Nachdem Sie die Festplatte an Microsoft gesendet haben, führen Sie auf der Seite des Importdiensts die folgenden Schritte aus.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. Klicken Sie im linken Bereich auf **Daten Steuerung** , und klicken Sie dann auf **Importieren**.
    
3. Klicken Sie auf der Seite **Importieren** auf den Auftrag für die Laufwerk Lieferung, der Sie für die laufende Nummer eingeben möchten. 
    
4. Klicken Sie auf der Seite Status flyoutmenü auf **EINGABETASTE Anzahl nachverfolgen**.
    
5. Geben Sie die folgenden Versandinformationen an:
    
1. **Übermittlung Netzbetreiber** Geben Sie den Namen des Netzbetreibers Übermittlung, mit der Sie die Festplatte an Microsoft zu liefern. 
    
2. **Nachverfolgen der Anzahl** Geben Sie die laufende Nummer für die Lieferung Festplatte. 
    
3. **Zurückgeben des Netzbetreibers Account-Nummer** Geben Sie Ihrer Organisation Account-Nummer des Netzbetreibers, die unter **Netzbetreiber zurückgeben**aufgelistet. Microsoft verwendet (dieses Konto die Festplatte für Sie den Versand und aufgeladen). Beachten Sie, dass Organisationen in den USA und in Europa, müssen über ein Konto mit FedEx verfügen. Organisationen in Asien und den Rest der Welt, müssen über ein Konto mit DHL verfügen.
    
6. Klicken Sie auf **Speichern**, um diese Informationen für den Importauftrag zu speichern. 
    
    Klicken Sie auf der Seite **Importieren** auf ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) so aktualisieren Sie die Informationen für Ihre Festplatte ausgeliefert Importauftrag **Aktualisieren** . Beachten Sie, dass Status jetzt auf **Laufwerke während der Übertragung**festgelegt ist.

## <a name="step-6-filter-data-and-start-the-pst-import-job"></a>Schritt 6: Filtern von Daten, und starten Sie den Importauftrag PST-Datei

Nach Ihrer Festplatte bei Microsoft eingeht, wird der Status für den Importauftrag auf der Seite **Importieren** in **empfangenen Laufwerke**geändert. Mitarbeiter im Rechenzentrum werden die Informationen in die Journal-Datei zum Hochladen von PST-Dateien in den Bereich der Azure-Speicher für Ihre Organisation verwenden. Zu diesem Zeitpunkt ändert sich der Status in **in Arbeit importieren**. Wie bereits zuvor erwähnt dauert es zwischen 7 bis 10 Business Tage nach Erhalt der Festplatte auf die PST-Dateien hochladen.
  
Nach der PST-Dateien in Azure hochgeladen werden, wird der Status in **Analysis in Bearbeitung**geändert. Dies gibt an, dass Office 365 die Daten in die PST-Dateien (auf sichere Weise) analysieren, um die Elemente und die verschiedenen Nachrichtentypen in PST-Dateien enthalten das Alter zu identifizieren. Wenn die Analyse abgeschlossen ist, und die Daten zum Importieren bereit ist, wird der Status für den Importauftrag **Analyse**abgeschlossen geändert. Zu diesem Zeitpunkt Sie haben die Möglichkeit, alle Daten in die PST-Dateien importieren oder Sie können die Daten, die importiert wird durch Festlegen von Filtern, die steuern, welche Daten importierten ruft zuschneiden.
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. Klicken Sie im linken Bereich auf **Daten Governance** > **Importieren**.
    
3. Klicken Sie auf **bereit sind, zu Office 365 importieren** für den Importauftrag, den Sie in Schritt 4 erstellt haben, klicken Sie auf der Seite **Importieren** . 
    
    ![Klicken Sie auf kann jetzt zu Office 365 neben den Importauftrag importieren, die Sie erstellt haben.](media/5760aac3-300b-4e31-b894-253c42a4b82b.png)
  
    Ausfliegen Seite wird mit Informationen zu den PST-Dateien und andere Informationen zu den Importauftrag angezeigt.
    
4. Klicken Sie auf **Import zu Office 365**.
    
5. Die Seite **Filtern die Daten** wird angezeigt. Sie enthält die Daten Einblicke in die resultierende aus der Analyse von Office 365, einschließlich Informationen über das Alter der Daten für die PST-Dateien ausgeführt. Zu diesem Zeitpunkt müssen Sie die Option zum Filtern der Daten, die importiert werden, oder importieren Sie die Daten unverändert. 
    
    ![Sie können erhöhen, die Daten in die PST-Dateien oder importieren Sie alle davon](media/287fc030-99e9-417b-ace7-f64617ea5d4e.png)
  
6. Führen Sie einen der folgenden Schritte aus:
    
    a. zu erhöhen, die Daten, die Sie importieren möchten, klicken Sie auf **Ja, ich möchte vor dem Importieren von Filtern**.
    
    Ausführliche Anleitung zum Filtern der Daten in die PST-Dateien, und starten Sie den Importauftrag finden Sie unter [Filtern von Daten beim Import von PST-Dateien zu Office 365](filter-data-when-importing-pst-files.md).
    
    oder -
    
    b, um alle Daten in die PST-Dateien zu importieren, klicken Sie auf **Nein, ich möchte alles, importieren** , und klicken Sie auf **Weiter**.
    
7. Wenn Sie alle Daten importieren möchten, klicken Sie auf **Daten importieren** , um den Auftrag für Import starten. 
    
    Der Status des Importauftrags wird auf der Seite **Importieren** angezeigt. Klicken Sie auf ![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) **Aktualisieren** , um die Statusinformationen zu aktualisieren, die in der Spalte **Status** angezeigt wird. Klicken Sie auf den Importauftrag zum Anzeigen der Seite Status flyoutmenü, die Statusinformationen für jedes zu importierenden PST-Datei angezeigt. Wenn der Importvorgang abgeschlossen ist und PST-Dateien auf die Benutzerpostfächer importiert wurden, wird der Status in **abgeschlossen**geändert werden.

## <a name="view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Anzeigen einer Liste von PST-Dateien, die in Office 365 hochgeladen

Sie können installieren und Verwenden der Microsoft Azure-Speicher-Explorer (Dies ist eine kostenlose open Source-Tool) zum Anzeigen der Liste der PST-Dateien, dass wir in den Bereich der Azure-Speicher für Ihre Organisation (von Mitarbeitern des Microsoft Rechenzentrums) hochgeladen werden. Sie können Sie tun, um sicherzustellen, dass die PST-Dateien von den Festplatten, die Sie an Microsoft gesendet, erfolgreich in den Bereich der Azure-Speicher hochgeladen wurden.
  
Microsoft Azure-Speicher-Explorer ist in der Vorschau.
  
 **Wichtig:** Sie können der Azure-Speicher-Explorer zum Hochladen oder Ändern von PST-Dateien verwenden. Die einzige unterstützte Methode für das Importieren von PST-Dateien in Office 365 ist die Verwendung von AzCopy. Darüber hinaus können Sie nicht PST-Dateien löschen, die Sie für die Azure Blob hochgeladen haben. Wenn Sie versuchen, eine PST-Datei zu löschen, erhalten Sie einen Fehler über nicht zu den erforderlichen Berechtigungen. Beachten Sie, dass alle PST-Dateien aus Ihrer Region Azure-Speicher automatisch gelöscht werden. Wenn es keine Importaufträge in Arbeit, und klicken Sie dann auf alle PST-Dateien in sind die ** Ingestiondata ** Container werden 30 Tage nach der neueste Importauftrag erstellt wurde gelöscht. 
  
So installieren die Azure-Speicher-Explorer, und eine Verbindung mit Ihrer Region Azure-Speicher:
  
1. Führen Sie die folgenden Schritte aus, um die gemeinsamen Zugriff Signatur (SAS)-URL für Ihre Organisation abzurufen. Diese URL ist eine Kombination aus der Netzwerk-URL für den Speicherort der Azure-Speicher in der Microsoft-Cloud für Ihre Organisation und eine SAS-Taste. Dieser Schlüssel enthält die erforderlichen Berechtigungen zum Zugriff auf Azure Speicherort Ihrer Organisation.
    
1. Wechseln Sie zu [https://protection.office.com/](https://protection.office.com/) und melden Sie sich mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation. 
    
2. Im linken Bereich der Sicherheit &amp; Compliance Center, klicken Sie auf **Daten Governance** \> **Importieren**.
    
3. Klicken Sie auf der Seite **Importieren** auf ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) **Importauftrag neu**.
    
4. Der Auftrag Zertifikatimport-Assistenten geben Sie einen Namen für den Auftrag für Import von PST-Datei ein, und klicken Sie dann auf **Weiter**. Verwenden Sie Kleinbuchstaben, Zahlen, Bindestriche und Unterstriche. In Großbuchstabe können nicht oder Leerzeichen im Namen enthalten.
    
5. Klicken Sie auf der Seite **Choose Auftragstyp importieren** klicken Sie auf **Hochladen die Daten** , und klicken Sie dann auf **Weiter**.
    
6. Klicken Sie in Schritt 2 auf **Netzwerk Upload SAS-URL anzeigen**.
    
7. Nachdem Sie die URL angezeigt wird, kopieren Sie die Datei, und speichern Sie sie in eine Datei. Achten Sie darauf, dass Sie den gesamten URL kopieren.
    
    > [!IMPORTANT]
    > Müssen Sie Vorsichtsmaßnahmen zum Schutz der SAS-URL. Dies kann durch jeden Benutzer Zugriff auf den Bereich der Azure-Speicher für Ihre Organisation verwendet werden. 
  
8. Klicken Sie auf **Abbrechen** , um den Import-Projekt-Assistenten zu schließen. 
    
2. Herunterladen Sie und installieren Sie das [Tool von Microsoft Azure-Speicher-Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
3. Starten Sie Microsoft Azure-Speicher-Explorer, mit der rechten Maustaste **Speicherkonten** im linken Bereich, und klicken Sie dann auf **Verbinden mit Azure-Speicher**.
    
    ![Mit der rechten Maustaste Speicherkonten und klicken Sie dann auf Verbindung mit Azure-Speicher](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
4. Klicken Sie auf **einen freigegebenen Signatur (SAS)-URI oder Verbindung Zugriffszeichenfolge verwenden** , und klicken Sie auf **Weiter**.
    
5. Klicken Sie auf **einen URI SAS verwenden**, fügen Sie die SAS-URL, die Sie erhalten in Schritt 1 in unter **URI**im Feld, und klicken Sie dann auf **Weiter**.
    
6. Auf der Seite **Zusammenfassung Verbindung** können Sie überprüfen Sie die Verbindungsinformationen, und klicken Sie auf **Verbinden**.
    
    Der Container **Ingestiondata** wird geöffnet. Sie enthält die PST-Dateien von der Festplatte. Der Container **Ingestiondata** befindet sich unter **Storage Konten** \> **(SAS-Attached Services)** \> **BLOB-Container**.
    
    ![Im Azure-Speicher-Explorer wird eine Liste der PST-Dateien angezeigt, die Sie hochgeladen haben.](media/12376fed-13a5-4a09-8fe6-e819e011b334.png)
  
7. Wenn Sie mit dem Microsoft Azure Storage Explorer fertig sind, mit der rechten Maustaste **Ingestiondata**, und klicken Sie dann auf **Trennen** , um von Ihrer Region Azure-Speicher zu trennen. Andernfalls erhalten einen Fehler beim nächsten Sie, den Sie versuchen, anfügen. 
    
    ![Klicken Sie mit der rechten Maustaste auf „ingestion“, und klicken Sie dann auf „Trennen“, um die Verbindung von Ihrem Azure-Speicherbereich zu trennen.](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  

  
## <a name="troubleshooting-tips"></a>Tipps zur Problembehandlung
<a name="troubleshootingtips"> </a>

- **Was passiert, wenn Sie der Importauftrag aufgrund von Fehlern in die PST-Datei importieren CSV-Datei zur Zuordnung ein Fehler auftritt?** Wenn ein Auftrag für Import aufgrund von Fehlern in der Zuordnungsdatei fehlschlägt, müssen Sie die Festplatte an Microsoft liefern erneut, um einen neuen Importauftrag erstellen. Dies liegt daran PST-Dateien von der Festplatte, die Sie übermittelt für den Importauftrag der Laufwerk des Protokollversands in den Bereich der Azure-Speicher für Ihre Organisation bereits hochgeladen wurden. In diesem Fall müssen Sie lediglich Beheben der Fehler in die PST-Datei importieren CSV-Datei zur Zuordnung, und klicken Sie dann Erstellen eines neuen "Netzwerk hochladen" Import-Auftrags und senden die überarbeitete CSV-Datei zur Zuordnung. Zum Erstellen und Starten eines neuen Auftrags für Netzwerk Upload importieren, finden Sie unter [Schritt 5: Erstellen einer PST-Importauftrag in Office 365](use-network-upload-to-import-pst-files.md#step-5-create-a-pst-import-job-in-office-365) und [Schritt 6: Filtern von Daten, und starten Sie den Importauftrag PST](use-network-upload-to-import-pst-files.md#step-6-filter-data-and-start-the-pst-import-job) im Thema "Verwendung Netzwerk Upload zum Importieren von PST-Dateien zu Office 365" 
    
    > [!NOTE]
    > Um Ihnen bei der Problembehandlung für der PST-Datei importieren CSV-Datei zur Zuordnung, verwenden Sie das Tool [Azure-Speicher-Explorer](#view-a-list-of-the-pst-files-uploaded-to-office-365) zum Anzeigen der Ordnerstruktur in den **Ingestiondata** Container für die PST-Dateien von der Festplatte, die in den Bereich der Azure-Speicher hochgeladen wurden. Zuordnung werden Datei in der Regel durch einen falschen Wert im Parameter FilePath verursacht. Dieser Parameter gibt den Speicherort einer PST-Datei in den Bereich der Azure-Speicher. Finden Sie in der Beschreibung des Parameters FilePath in der Tabelle in [Schritt 3](#step-3-create-the-pst-import-mapping-file). Wie bereits erklärt der Speicherort der PST-Dateien in den Bereich der Azure-Speicher durch angegeben wurde die `/dstdir:` Parameter, wenn Sie das Tool WAImportExport.exe in [Schritt2](#step-2-copy-the-pst-files-to-the-hard-drive)ausgeführt haben. 
  

  
## <a name="more-information"></a>Weitere Informationen

- Laufwerk des Protokollversands ist eine effektive Möglichkeit zum Importieren von großer Datenmengen Archivierung messaging in Office 365-Compliance-Funktionen nutzen, die für Ihre Organisation verfügbar sind. Nach dem Import Archivdaten für Benutzerpostfächer ermöglichen Folgendes:
    
  - Aktivieren Sie [archivpostfächer](enable-archive-mailboxes.md) und [Archivierung automatisch erweitert](enable-unlimited-archiving.md) , um Benutzern zusätzliche Postfach freier Speicherplatz für die Daten zu erteilen. 
    
  - Platzieren Sie Postfächer [Aufbewahrung für eventuelle Rechtsstreitigkeiten](https://go.microsoft.com/fwlink/?linkid=856286) , die Daten zu behalten. 
    
  - Verwenden Sie Microsoft [eDiscovery-Tools](search-for-content.md) , um die Daten zu suchen. 
    
  - Anwenden von [Aufbewahrungsrichtlinien für Office 365](retention-policies.md) , um zu steuern, wie lange die Daten aufbewahrt werden sollen und welche Aktionen an, die nach der Aufbewahrungszeitraum abgelaufen ist. 
    
  - Suchen der [Office 365-Überwachungsprotokoll](search-the-audit-log-in-security-and-compliance.md) für Ereignisse im Zusammenhang mit dieser Daten. 
    
  - Importieren von Daten in [inaktiver Postfächer](create-and-manage-inactive-mailboxes.md) Daten aus Gründen der Einhaltung von Bestimmungen archiviert. 
    
  - Ihre Organisation vor [Datenverlust](data-loss-prevention-policies.md) vertrauliche Informationen zu schützen. 
    
- Im Folgenden sehen Sie ein Beispiel für einen sicheren Speicherkontoschlüssel und einen BitLocker-Verschlüsselungsschlüssel. Dieses Beispiel enthält auch die Syntax für den Befehl „WAImportExport.exe“, den Sie zum Kopieren der PST-Dateien auf die Festplatte ausführen. Ergreifen Sie entsprechende Vorsichtsmaßnahmen, um diese so zu schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen schützen würden.
    

    ```
    Secure storage account key: 

    yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==

    BitLocker encryption key:

    397386-221353-718905-535249-156728-127017-683716-083391

  COMMAND SYNTAX

  First time:

  WAImportExport.exe PrepImport /j:<Name of journal file> /t:<Drive letter> /id:<Name of session> /srcdir:<Location of PST files> /dstdir:<PST file path> /sk:<Storage account key> /encrypt /logdir:<Log file location>

  Subsequent times:

  WAImportExport.exe PrepImport /j:<Name of journal file> /id:<Name of new session> /srcdir:<Location of PST files> /dstdir:<PST file path> 

  EXAMPLES

  First time:

  WAImportExport.exe PrepImport /j:PSTHDD1.jrn /t:f /id:driveship1 /srcdir:"\\FILESERVER1\PSTs" /dstdir:"ingestiondata/" /sk:"yaNIIs9Uy5g25Yoak+LlSHfqVBGOeNwjqtBEBGqRMoidq6/e5k/VPkjOXdDIXJHxHvNoNoFH5NcVUJXHwu9ZxQ==" /encrypt /logdir:"c:\users\admin\desktop\PstImportLogs"

  Subsequent times:

  WAImportExport.exe PrepImport /j:PSTHDD1.jrn /id:driveship2 /srcdir:"\\FILESERVER1\PSTs\SecondBatch" /dstdir:"ingestiondata/"
    ```
   
- Wie bereits erklärt aktiviert der Import von Office 365-Dienst das Anhalten der Aufbewahrungszeit (für unbefristete) festlegen, nach der PST-Dateien mit einem Postfach importiert werden. Dies bedeutet, dass die *RentionHoldEnabled* -Eigenschaft wird festgelegt, um `True` , damit die Aufbewahrungsrichtlinie Postfach zugeordnet werden nicht verarbeitet werden. Dadurch werden Postfach Besitzer Zeit, die neu importierte Nachrichten verwalten, indem Sie verhindern, dass eine Löschung oder Archivrichtlinie löschen oder Archivieren von Nachrichten, die älter sind. Es folgen einige Schritte, mit denen Sie diese Anhalten der Aufbewahrungszeit verwalten: 
    
  - Nach einem bestimmten Zeitraum, können Sie deaktivieren das Anhalten der Aufbewahrungszeit durch Ausführen der `Set-Mailbox -RetentionHoldEnabled $false` Befehl. Anweisungen finden Sie unter [einem Postfach zur Aufbewahrung von Compliance-Archivs](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
  - Sie können das Anhalten der Aufbewahrungszeit konfigurieren, sodass es auf einige Datum in der Zukunft deaktiviert ist. Führen Sie dies durch Ausführen der `Set-Mailbox -EndDateForRetentionHold <date>` Befehl. Beispielsweise unter der Annahme, dass heutigen Datum 1 Juli 2016 und das Anhalten der Aufbewahrungszeit in 30 Tagen deaktiviert werden soll, Sie führen den folgenden Befehl: `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. In diesem Szenario würden Sie die *RentionHoldEnabled* -Eigenschaft auf *True* festgelegt lassen. Weitere Informationen finden Sie unter [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
  - Sie können die Einstellungen für die Aufbewahrungsrichtlinie ändern, die an das Postfach zugewiesen ist, sodass ältere Elemente, die importiert wurden wird nicht sofort gelöscht oder zum Archivpostfach des Benutzers verschoben. Sie könnten beispielsweise der Aufbewahrungszeitraum für eine Richtlinie löschen oder Archivieren verlängern, die das dem Postfach zugeordnet ist. In diesem Szenario würden Sie deaktivieren Sie das Anhalten der Aufbewahrungszeit für das Postfach, nachdem Sie die Einstellungen der Aufbewahrungsrichtlinie geändert haben. Weitere Informationen finden Sie unter [Einrichten einer Richtlinie Archiv und Löschung für Postfächer in Office 365-Organisation](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
    

  

