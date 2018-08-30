---
title: Verwenden des Netzwerkuploads zum Importieren RMS-verschlüsselter PST-Dateien in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/29/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 84a595b8-cd77-4f66-ac52-57a33ddd4773
description: Erfahren Sie, wie Netzwerk Upload zum Importieren von RMS-verschlüsselten PST-Dateien in Benutzerpostfächer in Office 365 verwenden.
ms.openlocfilehash: 6460512e2d6085df684841248dc286d39dbd9d87
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530067"
---
# <a name="use-network-upload-to-import-rms-encrypted-pst-files-to-office-365"></a>Verwenden des Netzwerkuploads zum Importieren RMS-verschlüsselter PST-Dateien in Office 365

**Dieser Artikel ist für Administratoren. Versuchen Sie zum Importieren von PST-Dateien an Ihrem eigenen Postfach? Finden Sie unter [Import e-Mail, Kontakte und Kalender aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)**
   
Verwenden des Netzwerks hochladen Option und den Dienst Office 365 importieren zum Importieren von PST-Dateien für Benutzerpostfächer. Netzwerk-Upload bedeutet, dass Sie den PST-Dateien einen temporäre Speicherung Bereich in der Microsoft-Cloud hochladen. Klicken Sie dann kopiert der Import von Office 365-Dienst die PST-Dateien aus dem Speicherbereich an die Ziel-Benutzerpostfächer. Ein neues Feature des Diensts importieren können Sie die PST-Dateien zu verschlüsseln, bevor sie hochgeladen und auf der Microsoft-Cloud gespeichert sind. Diese Dateien werden nicht verschlüsselte werden beim Import für Benutzerpostfächer. 
  
Hier sind die erforderlichen Schritte zum Verschlüsseln und Importieren von PST-Dateien in Office 365-Postfächer:
  
[Schritt 1: Einrichten von Azure Rights Management für den PST-Import ](#step-1-set-up-azure-rights-management-for-pst-import)

[Schritt 2: Generieren eines Verschlüsselungsschlüssels für den PST-Import](#step-2-generate-an-encryption-key-for-pst-import)

[Schritt 3: Abrufen von RMS-Mandanten-ID und Lizenzierung URL](#step-3-obtain-rms-tenant-id-and-licensing-url)

[Schritt 4: Laden Sie die PST-Importtools, und kopieren Sie die SAS-URL](#step-4-download-the-pst-import-tools-and-copy-the-sas-url)

[Schritt 5: Verschlüsseln und Hochladen von PST-Dateien in Office 365](#step-5-encrypt-and-upload-your-pst-files-to-office-365)

[(Optional) Schritt 6: Hochgeladen Ansicht eine Liste der PST-Dateien nach Office 365](#optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Schritt 7: Erstellen Sie die Datei zur Zuordnung von PST-Import](#step-7-create-the-pst-import-mapping-file)

[Schritt 8: Erstellen eines PST-Importauftrags in Office 365](#step-8-create-a-pst-import-job-in-office-365)
  
> [!IMPORTANT]
> Sie haben, führen Sie Schritt 1 bis Schritt 4 nur einmal zum Einrichten und Konfigurieren von Ihrer Organisation zum Ver- und Importieren von PST-Dateien in Office 365-Postfächer. Nachdem Sie diese Schritte ausgeführt haben, führen Sie Schritt 5 bis 8 für Schritt die jedes Mal zu verschlüsseln, hochladen und importieren ein Batches von PST-Dateien. 
  
Weitere Informationen zum Importieren von Daten in Office 365 finden Sie unter [Übersicht über das Importieren von Ihrer Organisation PST-Dateien zu Office 365](importing-pst-files-to-office-365.md).
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen die Rolle Postfach importieren exportieren in Exchange Online zum Importieren von PST-Dateien in Office 365-Postfächer zugewiesen werden. Standardmäßig ist nicht dieser Rolle alle Rollengruppe in Exchange Online zugewiesen. Sie können die Rollengruppe "Organisationsverwaltung" Postfach Import/Export-Rolle hinzufügen. Oder erstellen eine neuen Rollengruppe, weisen Sie die Rolle Postfach Import/Export und fügen Sie sich als Mitglied hinzu. Weitere Informationen finden Sie unter "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" Abschnitte auf [Rollengruppen verwalten](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Darüber hinaus Import erstellen Aufträge in der Office 365-Sicherheit &amp; Compliance Center, eine der folgenden muss true sein:
    
  - Sie müssen die Rolle des E-Mail-Empfänger in Exchange Online zugewiesen werden. Standardmäßig wird diese Rolle der Organization Management und Recipient Management Rollen Gruppen zugewiesen.
    
    oder -
    
  - Sie müssen ein globaler Administrator in Office 365-Organisation sein.
    
  > [!TIP]
  > Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange-Online, die speziell für das Importieren von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die Mindestebene von Berechtigungen, die zum Importieren von PST-Dateien erforderlich sind der neuen Rollengruppe die Rollen Postfach importieren exportieren und E-Mail-Empfänger, und fügen Sie Mitglieder. 
  
- Sie müssen die PST-Dateien zu speichern, die Sie auf einem Dateiserver oder freigegebenen Ordner in Ihrer Organisation zu Office 365 importieren möchten. In Schritt 5 müssen Sie die Office 365-ImportTool ausführen Ver-und Hochladen von PST-Dateien, die auf diesem Dateiserver gespeichert sind oder freigegebenen Ordner zu Office 365 wird.
    
- Dieses Verfahren umfasst das Kopieren und Speichern einer Kopie der eines Verschlüsselungsschlüssels, einen Speicherschlüssel und eine Reihe von Identification Schlüssel und URLs. Diese Informationen werden zum Verschlüsseln und Hochladen von PST-Dateien in Schritt 5 verwendet werden. Achten Sie darauf, müssen Sie Vorsichtsmaßnahmen gegen diese nur schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen zu schützen. Beispielsweise können Sie auf kennwortgeschützte Microsoft Word-Dokument speichern oder in ein verschlüsseltes USB-Laufwerk speichern. Finden Sie [Weitere Informationen](#more-information) im Abschnitt ein Beispiel für diese Schlüssel, -IDs und URLs. 
    
- Sie können PST-Dateien in eines inaktiven Postfachs in Office 365 importieren. Zu diesem Zweck Angabe der GUID des inaktiven Postfachs in die `Mailbox` Parameter in der Zuordnungsdatei PST-Datei importieren. Weitere Informationen finden Sie unter [Schritt 7](#step-7-create-the-pst-import-mapping-file) . 
    
- In einer Exchange-hybridbereitstellung können Sie PST-Dateien in einer Cloud-basierten Archivpostfach für einen Benutzer importieren, deren Hauptpostfach lokal wurde. Dabei wird in der Zuordnungsdatei Import von PST-Datei wie folgt:
    
  - Geben Sie die e-Mail-Adresse für das Postfach des Benutzers: lokal in der `Mailbox` Parameter. 
    
  - Geben Sie den Wert **"true"** in der `IsArchive` Parameter. 
    
    Weitere Informationen finden Sie unter [Schritt 7](#step-7-create-the-pst-import-mapping-file) . 
    
- Nachdem PST-Dateien in ein Office 365-Postfach importiert wurden, ist die Einstellung für das Postfach Anhalten der Aufbewahrungszeit für unbefristete aktiviert. Dies bedeutet, dass die Aufbewahrungsrichtlinie an das Postfach zugewiesen, bis Sie das Anhalten der Aufbewahrungszeit deaktivieren oder ein Datums festlegen So deaktivieren Sie den Haltestatus verarbeitet wird. Warum tun wir das? Wenn Sie Nachrichten in einem Postfach importiert alt sind, sie möglicherweise werden endgültig gelöscht (gelöscht), da der Aufbewahrungszeitraum abgelaufen ist basierend auf der aufbewahrungseinstellungen für das Postfach konfiguriert. Platzieren das Postfach auf Anhalten der Aufbewahrungszeit erhalten die Postfach Besitzer Zeit zum Verwalten dieser Nachrichten neu importiert oder geben Sie Zeit, um die Einstellungen für die Aufbewahrung für das Postfach zu ändern. Finden Sie im Abschnitt [Weitere Informationen](#more-information) zum Verwalten von das Anhalten der Aufbewahrungszeit Vorschläge. 
    
- Wenn Sie nicht die PST-Dateien zu verschlüsseln, bevor Sie sie in Office 365 hochladen müssen, finden Sie unter [Verwendung Netzwerk zum Importieren von PST-Dateien zu Office 365 hochladen](use-network-upload-to-import-pst-files.md).
    
- Häufig gestellte Fragen zur Verwendung von Netzwerk-Upload zum Importieren von PST-Dateien zu Office 365 finden Sie unter [häufig gestellte Fragen zum Importieren von PST-Dateien zu Office 365](faqimporting-pst-files-to-office-365.md).
  
## <a name="step-1-set-up-azure-rights-management-for-pst-import"></a>Schritt 1: Einrichten von Azure Rights Management für den PST-Import 

PST-Import verwendet die vom Dienst Azure Rights Management (Azure, RMS) in Office 365 bereitgestellte Verschlüsselungsfunktionalität. Auf diese Weise können Sie um PST-Dateien zu verschlüsseln, bevor Sie sie in Office 365 hochladen. 
  
Konfigurieren von Azure RMS für den Import von PST besteht aus drei Schritten:
  
- [Aktivieren von Azure RMS](#activate-azure-rms)
    
- [Konfigurieren der RMS in Exchange Online](#configure-rms-in-exchange-online)
    
- [Installieren von Active Directory RMS-Client](#install-the-active-directory-rms-client)
    
### <a name="activating-azure-rms"></a>Aktivieren von Azure RMS

Azure RMS ist standardmäßig deaktiviert, aber von einem Administrator in Ihrer Organisation möglicherweise aktiviert haben. Befolgen Sie die Anweisungen auf [Aktivieren von Azure Rights Management](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service) zum Installieren und Aktivieren von Azure DRM.
  
### <a name="configuring-rms-in-exchange-online"></a>Konfigurieren der RMS in Exchange Online

Nachdem Sie den Dienst für die Verwaltung von Informationsrechten aktiviert haben, besteht der nächste Schritt zum Einrichten von Information Rights Management (IRM) in Exchange Online mit Azure RMS festgelegt. Weitere Informationen finden Sie unter [Konfigurieren von IRM Azure Rights Management verwenden](https://go.microsoft.com/fwlink/p/?LinkId=394816).
  
1. [Verbindung mit Exchange Online mithilfe von Remote-PowerShell herstellen](https://go.microsoft.com/fwlink/p/?LinkId=396554 ).
    
2. Führen Sie zum Einrichten der RMS-Key-Sharing-URL den folgenden Befehl aus.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation <RMS key sharing location>
    ```

    Verwenden Sie die folgende Tabelle, um die richtige RMS-Key-Sharing-Location für Ihre Organisation zu ermitteln.
    
    |**Standort**|**RMS-Key-Sharing-Location**|
    |:-----|:-----|
    |Nordamerika  <br/> | `https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Europäische Union  <br/> | `https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Asien  <br/> | `https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Südamerika  <br/> | `https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Office 365 für Behörden (Community-Cloud der US-Regierung)  <br/> | `https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc`<sup>1</sup> <br/> |
   
    > [!NOTE]
    > <sup>1</sup> : nur Kunden, die Office 365 für Behörden SKUs (Community-Cloud der US-Regierung) erworben haben, sollten diese RMS-Key-sharing-Location verwenden. 
  
    Mit diesem Befehl wird beispielsweise die Key-sharing-Location in Exchange Online für einen Kunden in Nordamerika befindet sich RMS Online konfiguriert.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
    ```

3. Führen Sie den folgenden Befehl an einer Trusted Publishing Domain (TPD) aus RMS Online in Office 365-Organisation zu importieren. 
    
    ```
    Import-RMSTrustedPublishingDomain -RMSOnline -Name "RMS Online"
    ```

    Eine TPD enthält die erforderlichen Einstellungen für die Verwendung von RMS-Features in der Organisation, einschließlich der Verschlüsselung von PST-Dateien.  
    
4. Führen Sie den folgenden Befehl zur Aktivierung von IRM für Office 365-Organisation.
    
    ```
    Set-IRMConfiguration -InternalLicensingEnabled $true
    ```

### <a name="installing-the-active-directory-rms-client"></a>Installieren von Active Directory RMS-Client

Der letzte Schritt in diesem Abschnitt wird den Client (Rights Management Services, RMS) 2.1 herunterladen. Diese Software schützt Zugriff auf Azure RMS und schützt übertragenen Webanwendungen von der Azure RMS Installieren des RMS-Clients auf dem Computer, den Sie zum Verschlüsseln und Hochladen von PST-Dateien in Schritt 5 verwenden. 
  
1. Laden Sie [Service Rechteverwaltungsclient 2.1](https://www.microsoft.com/en-us/download/details.aspx?id=38396).
    
2. Führen Sie den Assistenten für den Active Directory Rights Management Service Client 2.1 aus, um den Client zu installieren.

## <a name="step-2-generate-an-encryption-key-for-pst-import"></a>Schritt 2: Generieren eines Verschlüsselungsschlüssels für den PST-Import

Nachdem Sie die Azure RMS eingerichtet haben, besteht der nächste Schritt zum Generieren eines Verschlüsselungsschlüssels (als einen symmetrischen Schlüssel bezeichnet), die zum Verschlüsseln von PST-Dateien, die Sie zu Office 365 hochladen verwendet werden. Hierzu können Sie den Import von PST-Dienst als principal in Azure Active Directory-Dienst hinzufügen. Hinzufügen von dieser Anwendung ein Dienstprinzipal den Import von PST-Dienst direkt mit Azure Active Directory authentifiziert werden, wenn Sie hochladen können verschlüsselt die PST-Dateien auf den Azure Speicherort in Schritt 5.
  
1. Starten des Azure Active Directory-Moduls für Windows PowerShell.
    
2. Führen Sie den folgenden Befehl aus, um eine Verbindung mit dem Microsoft Online-Dienst herzustellen.
    
    ```
    Connect-MsolService
    ```

3. Geben Sie die Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation, und klicken Sie dann auf **OK**.
    
4. Führen Sie den folgenden Befehl aus, um einen Verschlüsselungsschlüssel (als symmetrischer Schlüssel bezeichnet) zu generieren. Hierfür wird ein neuer PST-Verschlüsselungsprinzipal erstellt.
    
    ```
    New-MsolServicePrincipal -DisplayName PstEncryptionPrincipal
    ```

    Das System zeigt den symmetrischen Schlüssel und die Eigenschaften für den neuen PST-Verschlüsselungsprinzipal an.
    
    ![Kopieren und Speichern des symmetrischen Schlüssels, der angezeigt wird](media/0003fdea-dace-41d2-b49d-f5c98c6230ca.png)
  
5. Kopieren Sie den symmetrischen Schlüssel in eine Text- oder Word-Datei. Wie bereits erwähnt, müssen Sie entsprechende Sicherheitsmaßnahmen ergreifen, um diese Datei zu schützen. Da dies das einzige Mal ist, dass der symmetrische Schlüssel angezeigt wird, sollten Sie einen Screenshot dieses Fensters erstellen und diesen in derselben Datei speichern.  
    
    > [!IMPORTANT]
    > Nachdem Sie den PST-Verschlüsselnsprinzipal erstellt haben, können Sie den symmetrischen Schlüssel nicht mehr mithilfe des Cmdlets **Get-MsolServicePrincipal** abrufen. Deshalb ist es wichtig, den Schlüssel zu speichern. 
  
Behalten Sie die Azure Active Directory-Modul für Windows PowerShell öffnen und eine Verbindung mit dem Microsoft Online-Dienst. In diesem Fenster im nächsten Schritt fügen Sie einen Befehl ausführen.

## <a name="step-3-obtain-rms-tenant-id-and-licensing-url"></a>Schritt 3: Abrufen von RMS-Mandanten-ID und Lizenzierung URL

Im nächste Schritt werden die Mandanten-ID und Lizenzierung URL des Speicherorts für den Azure RMS-Dienst für Ihre Organisation abzurufen. Kopieren Sie und speichern Sie diese Informationen auf dieselbe Datei, die den symmetrischen Schlüssel aus Schritt2 enthält. Die ID und die URL wird in Schritt 5 zum Verschlüsseln von PST-Dateien verwendet werden.
  
1. In der Azure Active Directory-Modul für Windows PowerShell (die mit dem Microsoft Online-Dienst verbunden ist), führen Sie den folgenden Befehl zum Herstellen einer Verbindung des Azure RMS-Diensts in Office 365-Organisation.
    
    ```
    Connect-AadrmService 
    ```

2. Geben Sie die Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation, und klicken Sie dann auf **OK**.
    
3. Führen Sie den folgenden Befehl aus, um die Mandanten-ID für den Azure RMS-Dienst in Office 365-Organisation anzuzeigen.
    
    ```
    Get-AadrmConfiguration | FL BPOSId
    ```

    Kopieren und speichern Sie den Wert für die `BPOSId` Eigenschaft. 
    
4. Führen Sie den folgenden Befehl zum Anzeigen des Speicherorts des Lizenzierung für Ihren Azure RMS-Dienst.
    
    ```
    Get-AadrmConfiguration | FL LicensingIntranetDistributionPointUrl
    ```

    Kopieren und speichern Sie den Wert für die `LicensingIntranetDistributionPointUrl` Eigenschaft. 

## <a name="step-4-download-the-pst-import-tools-and-copy-the-sas-url"></a>Schritt 4: Laden Sie die PST-Importtools, und kopieren Sie die SAS-URL

Nun, dass Sie Azure RMS konfiguriert und die IDs, die erforderlich sind, um die PST-Dateien zu verschlüsseln abgerufen haben, besteht der nächste Schritt herunterladen und installieren Sie die Tools, die Sie in Schritt 5 zum Verschlüsseln von ausgeführt werden und Hochladen PST-Dateien zu Office 365. Diese Tools sind die Azure AzCopy-Tool und das Office 365 Data Encryption-Tool. Sie können auch die SAS-URL für Ihre Organisation kopieren. Diese URL ist eine Kombination aus der Netzwerk-URL für den Speicherort der Azure-Speicher in der Microsoft-Cloud für Ihre Organisation und einer gemeinsamen Zugriff Signatur (SAS)-Taste. Dieser Schlüssel enthält die erforderlichen Berechtigungen zum Hochladen von PST-Dateien zu dem Speicherort der Azure-Speicher. Speichern sie in der Datei, dass Sie andere Informationen, die in Schritt2 und Schritt 3 kopiert haben. Wie bereits erwähnt müssen Sie Vorsichtsmaßnahmen gegen die SAS-URL zu schützen. 
  
> [!IMPORTANT]
> Sie müssen Azure AzCopy Version 5.0 zu verwenden, um erfolgreich hochzuladen, PST-Dateien auf den Speicherort der Azure-Speicher. Sobald neuere Versionen des Tools AzCopy werden für den Import von PST-Dateien zu Office 365 nicht unterstützt. Achten Sie auf der Seite **Hochladen von Dateien über das Netzwerk** mit den Verfahren in diesem Schritt das Tool AzCopy heruntergeladen. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation.
    
3. Klicken Sie im linken Bereich auf **Daten Steuerung** , und klicken Sie dann auf **Importieren**.
    
4. Klicken Sie auf der Seite **Import** auf **Zum Importdienst wechseln**.
    
5. Klicken Sie auf der Seite **Daten importieren auf Office 365** auf **Neuer Auftrag** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif), und klicken Sie dann auf **Hochladen von e-Mail-Nachrichten (PST-Dateien)**.
    
6. Klicken Sie auf der Seite **Hochladen von Dateien über das Netzwerk** in Schritt 2 auf **Netzwerk Upload SAS-URL anzeigen**.
    
7. Nachdem die URL angezeigt wird, kopieren Sie die Datei, und speichern Sie es in der Datei, in dem Sie die anderen Schlüssel gespeichert. Achten Sie darauf, dass Sie den gesamten URL kopieren. 
    
8. Klicken Sie in Schritt 3 auf herunterladen und installieren Sie das Tool Azure AzCopy **Herunterladen des Azure AzCopy Tools** . 
    
9. Klicken Sie im Popupfenster auf **Ausführen**, um das Azure AzCopy-Tool zu installieren. 
    
    > [!IMPORTANT]
    > Achten Sie darauf, dass Sie das Tool Azure AzCopy am Standardspeicherort zu installieren, ist `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy` , die 64-Bit-Windows auf einem Computer ausführen. Dies liegt daran beim Ausführen der O365ImportTool.exe in Schritt 5 sieht für das Tool AzCopy an diesem Speicherort. 
  
10. Nachdem Sie das Tool Azure AzCopy installiert haben, klicken Sie auf **Herunterladen der Office 365-Verschlüsselung und -Importtool**.
    
11. Klicken Sie auf **Speichern** , klicken Sie im Popupfenster \> zum Speichern der O365ImportTool.zip-Datei in einen Ordner auf Ihrem lokalen Computer **Speichern** . 
    
12. Extrahieren Sie die Datei „O365ImportTool.zip“.
    
13. Klicken Sie auf **Abbrechen** , um die Seite zum **Hochladen von Dateien über das Netzwerk** zu schließen. 
 
## <a name="step-5-encrypt-and-upload-your-pst-files-to-office-365"></a>Schritt 5: Verschlüsseln und Hochladen von PST-Dateien in Office 365

Nachdem Sie Schritt 1 bis Schritt 4 abgeschlossen haben, können Sie mithilfe des Tools O365ImportTool.exe ver- und Hochladen von PST-Dateien in Office 365. Dieses Tool PST-Dateien verschlüsselt und dann hochgeladen und speichert diese in ein Azure Speicherort in der Microsoft-Cloud. Wenn Sie diesen Schritt abgeschlossen haben, müssen die PST-Dateien in einer Dateifreigabe oder Dateiserver in Ihrer Organisation befinden. Dies wird als Quellverzeichnis in der folgenden Prozedur bezeichnet. Jedes Mal, wenn Sie das Tool O365ImportTool.exe ausführen benötigen Sie einen anderen Quellverzeichnis angeben können. 
  
1. Öffnen Sie eine Eingabeaufforderung auf dem lokalen Computer.
    
2. Wechseln Sie zu dem Verzeichnis, in dem Sie das Tool „O365ImportTool.exe“ in Schritt 4 installiert haben.
    
3. Führen Sie den folgenden Befehl zum Verschlüsseln und Hochladen von PST-Dateien in Office 365.
    
    ```
    O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL> /upload-destSAS:<SAS key>
    ```

    In der folgenden Tabelle werden die Parameter und deren erforderliche Werte beschrieben. Beachten Sie, dass die Informationen, die Sie in den vorherigen Schritten abgerufen haben, in den Werten für dieses Parameter verwendet werden.
    
    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `/srcdir:` <br/> |Gibt das Quellverzeichnis in Ihrer Organisation, die die PST-Dateien enthält, die zu Office 365 hochgeladen werden soll.  <br/> | `/srcdir:\\FILESERVER01\PSTs` <br/> |
    | `/protect-rmsserver:` <br/> |Gibt den Speicherort Lizenzierung für Ihren Azure RMS-Dienst. Verwenden Sie den Wert der `LicensingIntranetDistributionPointUrl` -Eigenschaft, die Sie unter Schritt 3 notiert haben. Achten Sie darauf, um den Wert dieses Parameters mit doppelte Anführungszeichen umgeben ("")<br/> | `/protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing"` <br/> |
    | `/protect-tenantid:` <br/> |Gibt die Identität des Unternehmens Azure RMS. Verwenden Sie den Wert der `BPOSId` -Eigenschaft, die Sie unter Schritt 3 notiert haben.<br/> | `/protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b` <br/> |
    | `/protect-key:` <br/> |Gibt den symmetrischen Schlüssel, den Sie erhalten in Schritt2 an. Achten Sie darauf, um den Wert dieses Parameters mit doppelte Anführungszeichen umgeben ("").  <br/> | `/protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867="` <br/> |
    | `/transfer:` <br/> |Gibt an, ob Sie PST-Dateien über das Netzwerk hochladen oder auf einer Festplatte werden versendet. Der Wert `upload` gibt an, dass Sie über das Netzwerk die Dateien hochladen. Der Wert `drive` gibt an, dass Sie die PST-Dateien auf einer Festplatte ausgeliefert werden.<br/> | `/transfer:upload` <br/> |
    | `/upload-dest:` <br/> |Gibt das Ziel in Office 365, in dem die PST-Dateien zu hochgeladen werden soll. Dies ist der Speicherort der Azure-Speicher für Ihre Organisation. Der Wert für diesen Parameter besteht aus der Netzwerk-Upload-URL aus der SAS-URL, die Sie in Schritt 4 kopiert haben. Achten Sie darauf, um den Wert dieses Parameters mit doppelte Anführungszeichen umgeben ("").<br/><br/> **Tipp:** (Optional) Sie können einen Unterordner in Azure Speicherort verschlüsselten PST-Dateien zum Hochladen angeben. Zu diesem Zweck hinzufügen einen Unterordner Speicherort (nach "Ingestiondata") in der Netzwerk-Upload-URL. Im ersten Beispiel wird keinen Unterordner angeben. Dies bedeutet, dass die PST-Dateien in das Stammverzeichnis (mit dem Namen *Ingestiondata* ) von Azure Speicherort hochgeladen werden soll. Im zweite Beispiel werden die PST-Dateien in einem Unterordner ( *EncryptedPSTs* ) in Azure Speicherort hochgeladen.           | `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata"` <br/> oder -  <br/>  `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs"` <br/> |
    | `/upload-destSAS:` <br/> |Gibt den SAS-Schlüssel für Ihre Organisation. Der Wert für diesen Parameter besteht aus dem SAS-Schlüssel aus der SAS-URL, die Sie in Schritt 4 kopiert haben. Beachten Sie, dass das erste Zeichen im Schlüssel SAS ein Fragezeichen ist ("?"). Achten Sie darauf, um den Wert dieses Parameters mit doppelte Anführungszeichen umgeben ("").  <br/> | `/upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/recurse` <br/> |Diese optionale Befehlszeilenoption gibt den rekursiven Modus, damit das Tool O365ImportTool.exe PST-Dateien kopiert werden, die in Unterordnern im Quellverzeichnis befinden, die durch angegeben ist die `/srcdir:` Parameter.  <br/><br/> **Hinweis:** Wenn Sie diese Option verwenden, müssen das PST-Dateien in Unterordnern einer anderen Datei Pathname Azure Speicherort an, nachdem sie hochgeladen haben. Sie müssen den genauen Dateipfadnamen in der CSV-Datei angeben, die Sie in Schritt 7 erstellen.           | `/recurse` <br/> |
   
    Nachfolgend sehen Sie ein Beispiel der Syntax für das Tool „O365ImportTool.exe“, in dem die tatsächlichen Werte für jeden Parameter verwendet werden:
    
    ```
    O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b  /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
    ```

    Nachdem Sie den Befehl ausgeführt haben, werden Statusmeldungen angezeigt, die den Fortschritt des Verschlüsselns und Hochladens der PST-Dateien anzeigen. Eine endgültige Statusmeldung zeigt die Gesamtzahl der Dateien an, die erfolgreich verschlüsselt und hochgeladen wurden.  
    
    > [!TIP]
    > Nachdem Sie erfolgreich führen den Befehl O365ImportTool.exe aus, und stellen Sie sicher, dass alle Parameter richtig sind, abgerufen Speichern einer Kopie der die Befehlszeilensyntax auf die gleiche (gesicherten)-Datei, in dem Sie die Informationen kopiert, Sie in den vorherigen Schritten. Sie können dann kopieren und fügen mit diesem Befehl in einem Eingabeaufforderungsfenster bei jedem Ausführen des Tools O365ImportTool.exe zum Ver- und Hochladen von PST-Dateien in Office 365 werden soll. Möglicherweise Sie ändern müssen nur die Werte sind die Methoden für die `/srcdir:` und `/upload-dest:` Parameter. 
  
## <a name="optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>(Optional) Schritt 6: Hochgeladen Ansicht eine Liste der PST-Dateien nach Office 365

Als optionalen Schritt können Sie installieren und Verwenden der Microsoft Azure-Speicher-Explorer (Dies ist eine kostenlose open Source-Tool) zum Anzeigen der Liste der PST-Dateien, die Sie für die Azure Blob hochgeladen haben. Es gibt drei gute Gründe dazu:
  
- Stellen Sie sicher, dass die PST-Dateien aus dem freigegebenen Ordner oder Dateiserver in Ihrer Organisation erfolgreich für die Azure Blob hochgeladen wurden.

- Stellen Sie sicher, dass die PST-Dateien verschlüsselt werden. Verschlüsselte PST-Dateien haben eine `.pfile` Extension, angefügt an die PST-Filename; beispielsweise `pilarp.pst.pfile`.
    
- Überprüfen Sie den Dateinamen (und den Unterordner Pfadnamen, wenn Sie eine eingeschlossen) für jede PST-Datei in den Azure Blob hochgeladen. Dies ist sehr nützlich, wenn Sie die Zuordnungsdatei im nächsten Schritt müssen Sie den Ordner Pathname und den Dateinamen für jede PST-Datei anzugeben PST-Datei erstellen. Überprüfen der Managementsystems hilft bei Senkung der potenzielle Fehler in der PST-Datei zur Zuordnung.
    
Microsoft Azure-Speicher-Explorer ist in der Vorschau. 
  
 > [!IMPORTANT]
>  Sie können der Azure-Speicher-Explorer zum Hochladen oder Ändern von PST-Dateien verwenden. Die einzige unterstützte Methode für das Importieren von PST-Dateien in Office 365 ist die Verwendung von AzCopy. Darüber hinaus können Sie nicht PST-Dateien löschen, die Sie für die Azure Blob hochgeladen haben. Wenn Sie versuchen, eine PST-Datei zu löschen, erhalten Sie einen Fehler über nicht zu den erforderlichen Berechtigungen. Beachten Sie, dass alle PST-Dateien aus Ihrer Region Azure-Speicher automatisch gelöscht werden. Wenn es sind keine Importaufträge in Arbeit, klicken Sie dann alle PST-Dateien im Container **Ingestiondata** gelöscht 30 Tage nach der neueste Importauftrag erstellt wurde. 
  
So installieren die Azure-Speicher-Explorer, und eine Verbindung mit Ihrer Region Azure-Speicher:
  
1. Herunterladen Sie und installieren Sie das [Tool von Microsoft Azure-Speicher-Explorer](https://go.microsoft.com/fwlink/p/?LinkId=544842).
    
2. Starten Sie Microsoft Azure-Speicher-Explorer, mit der rechten Maustaste **Speicherkonten** im linken Bereich, und klicken Sie dann auf **Verbinden mit Azure-Speicher**. 
    
    ![Mit der rechten Maustaste Speicherkonten und klicken Sie dann auf Verbindung mit Azure-Speicher](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Klicken Sie im Feld unter **Verbinden mit Azure-Speicher**fügen Sie in Schritt 4 SAS-URL, die Sie erhalten haben, und klicken Sie dann auf **Weiter**. 
    
    ![Fügen Sie die SAS-URL in das Feld auf der Seite Connect to Azure-Speicher](media/5d034128-e087-48e1-9ebc-4c9fa262d5b7.png)
  
4. Auf der Seite **Zusammenfassung Verbindung** können Sie überprüfen Sie die Verbindungsinformationen, und klicken Sie auf **Verbinden**. 
    
5. Klicken Sie unter **Storage Konten**erweitern Sie den Knoten **(Service SAS)** und dann den Knoten **BLOB-Container** . 
    
6. Mit der rechten Maustaste **Ingestiondata**, und klicken Sie dann auf **Open Blob-Container-Editor**.
    
    ![Klicken Sie mit der rechten Maustaste auf „ingestiondata“, und anschließend auf „ BLOB-Container-Editor öffnen“.](media/f50eee30-9202-4efc-904a-2895a0bc388d.png)
  
    Der Bereich Azure-Speicher mit einer Liste von PST-Dateien, die Sie in Schritt 5 hochgeladen wird angezeigt.
    
    ![Im Azure-Speicher-Explorer wird eine Liste der PST-Dateien angezeigt, die Sie hochgeladen haben.](media/a448ae43-e744-4153-8304-22b59e93883c.png)
  
7. Wenn Sie mit dem Microsoft Azure Storage Explorer fertig sind, mit der rechten Maustaste **Ingestiondata**, und klicken Sie dann auf **Trennen** , um von Ihrer Region Azure-Speicher zu trennen. Andernfalls erhalten einen Fehler beim nächsten Sie, den Sie versuchen, anfügen. 
    
    ![Klicken Sie mit der rechten Maustaste auf „ingestion“, und klicken Sie dann auf „Trennen“, um die Verbindung von Ihrem Azure-Speicherbereich zu trennen.](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-7-create-the-pst-import-mapping-file"></a>Schritt 7: Erstellen Sie die Datei zur Zuordnung von PST-Import

Nachdem die PST-Dateien verschlüsselt und in Azure Speicherort für Ihre Office 365-Organisation hochgeladen haben, besteht der nächste Schritt erstellen Sie ein Komma getrennt Werten (CSV)-Datei, die die Benutzerpostfächer gibt die PST-Dateien zu importiert werden sollen. Sie senden diese CSV-Datei im nächsten Schritt beim Erstellen eines Auftrags PST-Datei importieren.
  
1. [Laden Sie eine Kopie der Zuordnungsdatei PST -Datei importieren](https://go.microsoft.com/fwlink/p/?LinkId=544717). 
    
2. Öffnen oder speichern Sie die CSV-Datei auf Ihrem lokalen Computer. Das folgende Beispiel zeigt eine abgeschlossene PST-Importzuordnungsdatei (in Editor geöffnet). Es ist wesentlich einfacher, Microsoft Excel zum Bearbeiten der CSV-Datei zu verwenden.
    
    ```
    Workload,FilePath,Name,Mailbox,IsArchive,TargetRootFolder,ContentCodePage,SPFileContainer,SPManifestContainer,SPSiteUrl
    Exchange,,annb.pst.pfile,annb@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,annb_archive.pst.pfile,annb@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,,donh.pst.pfile,donh@contoso.onmicrosoft.com,FALSE,/,,,,
    Exchange,,donh_archive.pst.pfile,donh@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,pilarp.pst.pfile,pilarp@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,pilarp_archive.pst.pfile,pilarp@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,tonyk.pst.pfile,tonyk@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,tonyk_archive.pst.pfile,tonyk@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    Exchange,EncryptedPSTs,zrinkam.pst.pfile,zrinkam@contoso.onmicrosoft.com,FALSE,,,,,
    Exchange,EncryptedPSTs,zrinkam_archive.pst.pfile,zrinkam@contoso.onmicrosoft.com,TRUE,/ImportedPst,,,,
    ```

    Die erste Zeile oder Kopfzeile der CSV-Datei enthält die Parameter, die vom Dienst PST-Datei importieren zum Importieren der PST-Dateien auf die Benutzerpostfächer verwendet werden. Jeder Parametername wird durch ein Komma getrennt. Jede Zeile unter der Überschrift stellt die Parameterwerte zum Importieren einer PST-Datei in ein bestimmtes Postfach. Sie benötigen eine Zeile für jeden PST-Datei, die Sie zu einem Benutzerpostfach importieren möchten. Achten Sie darauf, dass Sie die Platzhalterdaten in die Datei zur Zuordnung durch den tatsächlichen Daten ersetzen.
    
    > [!NOTE]
    > Ändern Sie nichts in der Kopfzeile, einschließlich der SharePoint-Parameter; diese werden während des PST-Importvorgangs ignoriert. 
  
3. Verwenden Sie die Informationen in der folgenden Tabelle, um zu die CSV-Datei mit den erforderlichen Informationen zu füllen.
    
    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Gibt den Office 365-Dienst, dem Daten importiert werden. Verwenden Sie zum Importieren von PST-Dateien auf die Benutzerpostfächer `Exchange`.<br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Gibt den Speicherort des Ordners in der Azure Speicherort, dass Sie die PST-Dateien in Schritt 5 auf hochgeladen.  <br/>  Wenn Sie einen Unterordnernamen für die optionalen der Netzwerk-URL im einschließen nicht die `/upload-dest:` Parameter in Schritt 5 dieser Parameter leer lassen in der CSV-Datei. Wenn Sie einen Unterordnernamen eingeschlossen, geben Sie es in diesen Parameter an. Der Wert für diesen Parameter ist Groß-/Kleinschreibung beachtet. *In beiden Fällen nehmen "Ingestiondata" in den Wert für* die `FilePath` Parameter.<br/> <br/>**Wichtig:** Die Groß-/Kleinschreibung für den Namen der Pfad muss die Groß-/Kleinschreibung, die Sie verwendet, wenn Sie in der SAS-URL in einen optionalen Unterordnernamen enthalten die `/upload-dest:` Parameter in Schritt 5. Beispielsweise, wenn Sie verwendet `EncryptedPSTs` für den Unterordner Namen Sie in Schritt 5, und klicken Sie dann verwenden `encryptedpsts` in der `FilePath` schlägt fehl, Parameter in der CSV-Datei, die für die PST-Datei importieren. Achten Sie darauf, dass die Groß-/Kleinschreibung in beiden Fällen verwenden.           |(leer lassen)  <br/> Oder  <br/>  `EncryptedPSTs` <br/> |
    | `Name` <br/> |Gibt den Namen der PST-Datei, die für das Postfach des Benutzers importiert werden. Der Wert für diesen Parameter ist Groß-/Kleinschreibung beachtet. Da die PST-Dateien, die auf den Azure Speicherort hochgeladen werden verschlüsselt sind, eine `.pfile` Erweiterung wird auf den Dateinamen der PST-Datei hinzugefügt. Sie müssen hinzufügen, die `.pfile` Erweiterung auf den Namen des der PST-Dateien in der CSV-Datei.<br/><br/> **Wichtig:** Die Groß-/Kleinschreibung für den Namen des PST-Datei in der CSV-Datei muss die gleiche wie die PST-Datei, die in der Azure Speicherort in Schritt 5 hochgeladen wurde. Angenommen, Sie verwenden `annb.pst.pfile` in der `Name` Parameter in der CSV-Datei, aber der Name der PST-Datei ist `AnnB.pst`, schlägt der Import für die PST-Datei fehl. Stellen Sie sicher, dass der Name der PST-Datei in der CSV-Datei die gleiche Groß-/Kleinschreibung als die eigentliche PST-Datei verwendet wird.           | `annb.pst.pfile` <br/> |
    | `Mailbox` <br/> |Gibt die E-Mail-Adresse des Postfachs an, in das die PST-Datei importiert werden soll.   <br/> Um eine PST-Datei in eines inaktiven Postfachs zu importieren, müssen Sie die Postfach-GUID für diesen Parameter angeben. Um diese GUID zu erhalten, führen Sie den folgenden PowerShell-Befehl in Exchange Online: "Get-Mailbox - InactiveMailboxOnly<identity of inactive mailbox> | FL Guid` <br/><br/> **Note:** In some cases, you might have multiple mailboxes with the same email address, where one mailbox is an active mailbox and the other mailbox is in a soft-deleted (or inactive) state. In these situations, you have specify the mailbox GUID to uniquely identify the mailbox to import the PST file to. To obtain this GUID for active mailboxes, run the following PowerShell command:  `Get-Mailbox -<identity of active mailbox> | FL Guid`. To obtain the GUID for soft-deleted (or inactive) mailboxes, run this command  `Get-Mailbox - <identity of soft-deleted or inactive mailbox> - SoftDeletedMailbox | FL Guid'           | `annb@contoso.onmicrosoft.com` <br/> oder -  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Gibt an, ob die PST-Datei in das Archivpostfach des Benutzers importiert werden soll. Es gibt zwei Möglichkeiten:<br/> **"False"** Importiert die PST-Datei zum primären Postfach des Benutzers.  <br/> **"True"** Importiert die PST-Datei in Archivpostfach des Benutzers an.  <br/>  Wenn Sie diesen Parameter leer lassen, wird die PST-Datei in der primären Postfach des Benutzers importiert.  <br/><br/> **Hinweis:** Um eine PST-Datei in einer Cloud-basierten Archivpostfach für einen Benutzer zu importieren, deren primäre Postfach der lokale ist, nur **TRUE** für diesen Parameter angeben und geben Sie die e-Mail-Adresse für das Postfach des Benutzers: lokal für die `Mailbox` Parameter.           | `FALSE` <br/> oder -  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Gibt den Postfachordner, dem in die PST-Datei importiert wird.  <br/>  Wenn dieser Parameter leer lassen, wird die PST-Datei in einen neuen Ordner importiert werden benannten **importierte** auf der Stammebene des Postfachs (der gleichen Ebene wie der Ordner Posteingang und anderen standardmäßigen Postfachordner) befinden.  <br/>  Wenn Sie angeben `/`, Elemente in der PST-Datei importiert werden direkt im Ordner Posteingang des Benutzers.  <br/>  Wenn Sie angeben `/<foldername>`, Elemente in der PST-Datei importiert werden in einem Unterordner mit dem Namen * \<Foldername\> * . Wenn Sie verwendet, beispielsweise `/ImportedPst`, würde Elemente in einem Unterordner mit dem Namen **ImportedPst**importiert werden. Dieser Unterordner wird im Ordner Posteingang des Benutzers befinden.<br/><br/> **Tipp:** Berücksichtigen Sie mit ein paar Test Batches mit diesem Parameter experimentieren, damit Sie ermitteln können, die am besten geeigneten Speicherorte Ordner PST-Dateien zu importieren.           |(leer lassen)  <br/> Oder  <br/>  `/` <br/> oder -  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Dieser optionale Parameter gibt einen numerischen Wert für die Codepage für den Import von PST-Dateien im ANSI-Format verwenden. Dieser Parameter wird verwendet, für den Import von PST-Dateien von Organisationen Chinesisch, Japanisch und Koreanisch (CJK), da diese Sprachen in der Regel einen double-Byte-Zeichensatz (DBCS) für die zeichencodierung von verwenden. Wenn dieser Parameter wird nicht zum Importieren von PST-Dateien für Sprachen, die DBCS für Ordnernamen Postfach verwenden verwendet, werden die Namen der Ordner häufig verzerrt, nach dem Importieren. Eine Liste der unterstützten Werte für diesen Parameter verwenden finden Sie unter [Code Seite Bezeichner](https://go.microsoft.com/fwlink/p/?LinkId=328514).<br/><br/> **Hinweis:** Wie bereits erwähnt, dies ist ein optionaler Parameter, und Sie keinen zum Einschließen in die CSV-Datei. Oder Sie können einschließen und den Wert für eine oder mehrere Zeilen leer lassen.           |(leer lassen)  <br/> Oder  <br/>  `932`(Dies ist der Bezeichner für Japanisch ANSI/OEM-Seite)  <br/> |
    | `SPFileContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPManifestContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPSiteUrl` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
  
## <a name="step-8-create-a-pst-import-job-in-office-365"></a>Schritt 8: Erstellen eines PST-Importauftrags in Office 365

Der letzte Schritt besteht darin den Importauftrag PST-Datei in den Import-Dienst in Office 365 erstellen. Wie bereits erklärt senden Sie die PST-Import-Zuordnung-Datei, die Sie in Schritt 7 erstellt haben. Nach der Erstellung neuen Auftrags mithilfe des Import-Diensts der Informationen in die Datei zur Zuordnung zum Aufheben der Markierung-Ver- und Importieren von PST-Dateien (, die Sie in Office 365 in Schritt 5 hochgeladen) in das angegebene Benutzerpostfach. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit den Anmeldeinformationen für ein Administratorkonto in Office 365-Organisation.
    
3. Klicken Sie im linken Bereich auf **Daten Steuerung** , und klicken Sie dann auf **Importieren**.
    
4. Klicken Sie auf der Seite **Import** auf **Zum Importdienst wechseln**.
    
5. Klicken Sie auf der Seite **Daten importieren auf Office 365** auf **Neuer Auftrag**![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif), und klicken Sie dann auf **Hochladen von e-Mail-Nachrichten (PST-Dateien)**.
    
6. Klicken Sie auf der Seite **Hochladen von Dateien über das Netzwerk** auf die **habe ich meine Dateien hochladen** und **ich haben Zugriff auf die Datei zur Zuordnung** , Kontrollkästchen, und klicken Sie dann auf **Weiter**. 
    
7. Geben Sie einen Namen für den PST-Importauftrag an, und klicken Sie dann auf **Weiter**.
    
8. Klicken Sie auf **Hinzufügen** ![Symbol hinzufügen](media/ITPro-EAC-AddIcon.gif) Zuordnen von PST-Datei aus, den Sie in Schritt 7 erstellt haben. 
    
9. Wenn der Name der CSV-Datei in der Liste angezeigt wird, wählen Sie ihn aus, und klicken Sie dann auf **Überprüfen**, um die CSV-Datei auf Fehler zu überprüfen.  
    
    > [!NOTE]
    > Wie vorherige erläutert, wann die PST-Dateien verschlüsselt werden, eine `.pfile` Erweiterung an den Dateinamen der PST-Datei angehängt ist. Sie müssen hinzufügen, die `.pfile` Erweiterung auf den Namen des der PST-Dateien in der CSV-Datei. Die Validierung der CSV-Datei schlägt fehl, wenn dies nicht der Fall. 
  
    Die CSV-Datei muss erfolgreich überprüft werden, um einen PST-Importauftrag zu erstellen. Wenn die Überprüfung fehlschlägt, klicken Sie auf den Link**Ungültig** in der Spalte **Status**. Eine Kopie der PST-Importzuordnungsdatei wird geöffnet, und es wird eine Fehlermeldung für jede Zeile in der Datei angezeigt, in der ein Fehler aufgetreten ist. 
    
10. Wenn die PST-Zuordnungsdatei erfolgreich überprüft wurde, lesen Sie das Dokument mit den allgemeinen Geschäftsbedingungen, und aktivieren Sie dann das Kontrollkästchen.
    
11. Klicken Sie auf **Fertig stellen**, um den Auftrag zu übermitteln. 
    
    Der Auftrag wird in der Liste der Aufträge PST-Datei importieren, klicken Sie auf der Seite **Daten importieren auf Office 365** angezeigt. 
    
12. Wählen Sie den Auftrag aus, und klicken Sie auf **Aktualisieren**![aktualisieren (Symbol)](media/O365-MDM-Policy-RefreshIcon.gif) , die Statusinformationen zu aktualisieren, die im Detailbereich angezeigt wird. 
    
13. Klicken Sie im Detailbereich auf **Details anzeigen**, um den aktuellen Status für den ausgewählten Auftrag abzurufen. 
 
## <a name="more-information"></a>Weitere Informationen

- Warum Importieren von PST-Dateien in Office 365?
    
  - Es ist eine gute Möglichkeit zum Migrieren von e-Mail von Ihrer Organisation zu Office 365.
    
  - Das Importieren hilft Ihnen beim Erfüllen der Complianceanforderungen Ihrer Organisation. Es ermöglicht Ihnen Folgendes:
    
  - Aktivieren der Archivierung von Postfächern, um Benutzern zusätzlichen Speicherplatz im Postfach bereitzustellen.
    
  - Aufbewahren von Postfächern, um Inhalte beizubehalten.
    
  - Verwenden von Microsoft eDiscovery-Tools, um in Postfächern nach Inhalten zu suchen.
    
  - Verwenden von Aufbewahrungsrichtlinien, um zu steuern, wie lange Postfachinhalte beibehalten werden.
    
  - Suchen Sie das Office 365-Überwachungsprotokoll für Ereignisse im Zusammenhang mit dem Postfach.
    
  - Es bietet Schutz vor Datenverlust. PST-Dateien, die in Office 365-Postfächer importiert werden erben die Funktionen für hohe Verfügbarkeit von Exchange Online, im Gegensatz zum Speichern der Daten auf dem Computer eines Benutzers.
    
  - Die Daten sind für den Benutzer auf allen Geräten verfügbar, da sie in der Cloud gespeichert sind.
    
- Es folgt ein Beispiel der Schlüssel, -IDs und URLs, die in den Schritten 2, 3 und 4 ermittelt werden. Dieses Beispiel enthält auch die Syntax für den Befehl an, dem Sie in das O365ImportTool.exe-Tool zum Verschlüsseln von ausgeführt und Hochladen PST-Dateien in Office 365. Achten Sie darauf, müssen Sie Vorsichtsmaßnahmen gegen diese nur schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen zu schützen.
    
  ```
  Symmetric key: l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=

  BPOSId: 42745b33-2a5c-4726-8a2a-ca43caa0f74b

  LicensingIntranetDistributionPointUrl (RMS licensing location): https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing
  
  SAS URL: https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D
  
  O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL from the SAS URL> /upload-destSAS:<SAS key from the SAS URL>
  
  EXAMPLES
  
  This example uploads PST files to the root of the Azure storage location:

  O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b /protect-ownerid:45beb445-4d06-47df-8e61-6ca1a88a080e /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
  
  This example uploads PST files to a subfolder named EncryptedPSTs  in the Azure storage location:
  
  O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b /protect-ownerid:45beb445-4d06-47df-8e61-6ca1a88a080e /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
  ```

- Wie bereits erklärt aktiviert der Import von Office 365-Dienst das Anhalten der Aufbewahrungszeit (für unbefristete) festlegen, nach der PST-Dateien mit einem Postfach importiert werden. Dies bedeutet, dass die *RentionHoldEnabled* -Eigenschaft wird festgelegt, um `True` , damit die Aufbewahrungsrichtlinie Postfach zugeordnet werden nicht verarbeitet werden. Dadurch werden Postfach Besitzer Zeit, die neu importierte Nachrichten verwalten, indem Sie verhindern, dass eine Löschung oder Archivrichtlinie löschen oder Archivieren von Nachrichten, die älter sind. Es folgen einige Schritte, mit denen Sie diese Anhalten der Aufbewahrungszeit verwalten: 
    
  - Nach einem bestimmten Zeitraum, können Sie deaktivieren das Anhalten der Aufbewahrungszeit durch Ausführen der `Set-Mailbox -RetentionHoldEnabled $false` Befehl. Anweisungen finden Sie unter [einem Postfach zur Aufbewahrung von Compliance-Archivs](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
  - Sie können das Anhalten der Aufbewahrungszeit konfigurieren, sodass es auf einige Datum in der Zukunft deaktiviert ist. Führen Sie dies durch Ausführen der `Set-Mailbox -EndDateForRetentionHold <date>` Befehl. Beispielsweise unter der Annahme, dass heutigen Datum 1 Juli 2016 und das Anhalten der Aufbewahrungszeit in 30 Tagen deaktiviert werden soll, Sie führen den folgenden Befehl: `Set-Mailbox -EndDateForRetentionHold 8/1/2016`. In diesem Szenario würden Sie die *RentionHoldEnabled* -Eigenschaft auf festgelegt lassen `True`. Weitere Informationen finden Sie unter [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
  - Sie können die Einstellungen für die Aufbewahrungsrichtlinie ändern, die an das Postfach zugewiesen ist, sodass ältere Elemente, die importiert wurden wird nicht sofort gelöscht oder zum Archivpostfach des Benutzers verschoben. Sie könnten beispielsweise der Aufbewahrungszeitraum für eine Richtlinie löschen oder Archivieren verlängern, die das dem Postfach zugeordnet ist. In diesem Szenario würden Sie deaktivieren Sie das Anhalten der Aufbewahrungszeit für das Postfach, nachdem Sie die Einstellungen der Aufbewahrungsrichtlinie geändert haben. Weitere Informationen finden Sie unter [Einrichten einer Richtlinie Archiv und Löschung für Postfächer in Office 365-Organisation](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
