---
title: Verwenden des Netzwerk Uploads zum Importieren von RMS-verschlüsselten PST-Dateien in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 5/29/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MET150
ms.assetid: 84a595b8-cd77-4f66-ac52-57a33ddd4773
description: Erfahren Sie, wie Sie mithilfe des Netzwerk-Uploads RMS-verschlüsselte PST-Dateien in Benutzerpostfächer in Office 365 importieren.
ms.openlocfilehash: 69bbd0082f02bd60101f59c2870bc8adfdc95fda
ms.sourcegitcommit: fb50bf2f2c9d780c911f245a2f78c6bb5e357f67
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2019
ms.locfileid: "30950462"
---
# <a name="use-network-upload-to-import-rms-encrypted-pst-files-to-office-365"></a>Verwenden des Netzwerk Uploads zum Importieren von RMS-verschlüsselten PST-Dateien in Office 365

**Dieser Artikel richtet sich an Administratoren. Versuchen Sie, PST-Dateien in Ihr eigenes Postfach zu importieren? Weitere Informationen finden Sie unter [Importieren von e-Mails, Kontakten und Kalendern aus einer Outlook-PST-Datei](https://go.microsoft.com/fwlink/p/?LinkID=785075)**
   
Verwenden Sie die Option Netzwerk Upload und den Office 365-Import Dienst, um PST-Dateien in Benutzerpostfächer zu importieren. Der Netzwerk Upload bewirkt, dass Sie die PST-Dateien in einem temporären Speicherbereich in der Microsoft-Cloud hochladen. Anschließend kopiert der Office 365-Import Dienst die PST-Dateien aus dem Speicherbereich in die Postfächer des Zielbenutzers. Mit einer neuen Funktion des Import Diensts können Sie Ihre PST-Dateien verschlüsseln, bevor Sie hochgeladen und in der Microsoft-Cloud gespeichert werden. Diese Dateien werden nicht verschlüsselt, wenn Sie in Benutzerpostfächer importiert werden. 
  
Hier sind die Schritte, die zum Verschlüsseln und Importieren von PST-Dateien in Office 365-Postfächern erforderlich sind:
  
[Schritt 1: Einrichten der Azure-Rechteverwaltung für den PST-Import](#step-1-set-up-azure-rights-management-for-pst-import)

[Schritt 2: Generieren eines Verschlüsselungsschlüssels für den PST-Import](#step-2-generate-an-encryption-key-for-pst-import)

[Schritt 3: Abrufen der RMS-Mandanten-ID und der Lizenzierungs-URL](#step-3-obtain-rms-tenant-id-and-licensing-url)

[Schritt 4: Herunterladen der PST-Import Tools und Kopieren der SAS-URL](#step-4-download-the-pst-import-tools-and-copy-the-sas-url)

[Schritt 5: verSchlüsseln und Hochladen der PST-Dateien in Office 365](#step-5-encrypt-and-upload-your-pst-files-to-office-365)

[Optional Schritt 6: Anzeigen einer Liste der PST-Dateien, die in Office 365 hochgeladen wurden](#optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365)

[Schritt 7: Erstellen der PST-Import Zuordnungsdatei](#step-7-create-the-pst-import-mapping-file)

[Schritt 8: Erstellen eines PST-Import Auftrags in Office 365](#step-8-create-a-pst-import-job-in-office-365)
  
> [!IMPORTANT]
> Sie müssen Schritt 1 bis Schritt 4 nur einmal ausführen, um Ihre Organisation zum Verschlüsseln und Importieren von PST-Dateien in Office 365-Postfächern einzurichten und zu konfigurieren. Nachdem Sie diese Schritte ausgeführt haben, befolgen Sie Schritt 5 bis Schritt 8 jedes Mal, wenn Sie einen Batch von PST-Dateien verschlüsseln, hochladen und importieren möchten. 
  
Weitere Informationen zum Importieren von Daten in Office 365 finden Sie unter [Overview of Import your organization PST files to office 365](importing-pst-files-to-office-365.md).
  
## <a name="before-you-begin"></a>Bevor Sie beginnen

- Sie müssen die Rolle "Postfachimport-export" in Exchange Online zuweisen, um PST-Dateien in Office 365-Postfächer zu importieren. Diese Rolle wird standardmäßig keiner Rollengruppe in Exchange Online zugewiesen. You can add the Mailbox Import Export role to the Organization Management role group. Or you can create a new role group, assign the Mailbox Import Export role, and then add yourself as a member. Weitere Informationen finden Sie im Abschnitt "Hinzufügen einer Rolle zu einer Rollengruppe" oder "Erstellen einer Rollengruppe" unter [Verwalten von Rollengruppen](https://go.microsoft.com/fwlink/p/?LinkId=730688).
    
    Darüber hinaus muss eine der folgenden Anforderungen erfüllt sein, um &amp; Importaufträge im Office 365 Security Compliance Center zu erstellen:
    
  - Sie müssen der Rolle e-Mail-Empfänger in Exchange Online zugewiesen werden. By default, this role is assigned to the Organization Management and Recipient Management roles groups.
    
    Oder
    
  - Sie müssen ein globaler Administrator in Ihrer Office 365-Organisation sein.
    
  > [!TIP]
  > Erwägen Sie das Erstellen einer neuen Rollengruppe in Exchange Online, die speziell für den Import von PST-Dateien in Office 365 vorgesehen ist. Weisen Sie für die erforderlichen Mindestberechtigungen zum Importieren von PST-Dateien die Rollen Mailbox Import Export und e-Mail-Empfänger der neuen Rollengruppe zu, und fügen Sie dann Mitglieder hinzu. 
  
- Sie müssen die PST-Dateien, die Sie in Office 365 importieren möchten, auf einem Dateiserver oder einem freigegebenen Ordner in Ihrer Organisation speichern. In Schritt 5 führen Sie die Office 365-ImportTool aus, die die PST-Dateien, die auf diesem Dateiserver oder freigegebenen Ordner gespeichert sind, in Office 365 verschlüsseln und hochladen.
    
- Dieses Verfahren umfasst das Kopieren und Speichern einer Kopie eines Verschlüsselungsschlüssels, eines Speicher Schlüssels und einer Reihe von Identifizierungs Schlüsseln und URLs. Diese Informationen werden in Schritt 5 zum Verschlüsseln und Hochladen Ihrer PST-Dateien verwendet. Ergreifen Sie entsprechende Vorsichtsmaßnahmen, um diese so zu schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen schützen würden. Sie können Sie beispielsweise in einem kennwortgeschützten Microsoft Word-Dokument speichern oder auf einem verschlüsselten USB-Laufwerk speichern. Im Abschnitt [Weitere Informationen](#more-information) finden Sie ein Beispiel für diese Schlüssel, IDs und URLs. 
    
- Sie können PST-Dateien in ein inaktives Postfach in Office 365 importieren. Hierzu geben Sie die GUID des inaktiven Postfachs im `Mailbox` Parameter in der PST-Import Zuordnungsdatei an. Weitere Informationen finden Sie in [Schritt 7](#step-7-create-the-pst-import-mapping-file) . 
    
- In einer Exchange-hybridbereitstellung können Sie PST-Dateien in ein cloudbasierten Archivpostfach für einen Benutzer importieren, dessen primäres Postfach lokal ist. Führen Sie dazu die folgenden Schritte in der PST-Import Zuordnungsdatei aus:
    
  - Geben Sie die e-Mail-Adresse des lokalen Postfachs des Benutzers `Mailbox` im Parameter an. 
    
  - Geben Sie den Wert **true** im `IsArchive` Parameter an. 
    
    Weitere Informationen finden Sie in [Schritt 7](#step-7-create-the-pst-import-mapping-file) . 
    
- Nachdem PST-Dateien in ein Office 365-Postfach importiert wurden, wird die Aufbewahrungszeit für das Postfach für eine unbegrenzte Dauer aktiviert. Dies führt dazu, dass die dem Postfach zugewiesene Aufbewahrungsrichtlinie erst verarbeitet wird, wenn Sie die Aufbewahrungsdauer deaktivieren oder ein Datum festlegen, um den Haltestatus zu deaktivieren. Warum tun wir das? Wenn Nachrichten, die in ein Postfach importiert wurden, alt sind, werden Sie möglicherweise dauerhaft gelöscht (bereinigt), da ihre Aufbewahrungszeit auf Grundlage der für das Postfach konfigurierten Aufbewahrungseinstellungen abgelaufen ist. Wenn Sie die Aufbewahrungszeit für das Postfach aktivieren, wird der Postfachbesitzer zum Verwalten dieser neu importierten Nachrichten oder zum Ändern der Aufbewahrungseinstellungen für das Postfach Zeit. Im Abschnitt [Weitere Informationen](#more-information) finden Sie Vorschläge zum Verwalten der Aufbewahrungsdauer. 
    
- Wenn Sie Ihre PST-Dateien vor dem Hochladen in Office 365 nicht verschlüsseln müssen, finden Sie weitere Informationen unter [Verwenden des Netzwerk Uploads zum Importieren von PST-Dateien in office 365](use-network-upload-to-import-pst-files.md).
    
- Häufig gestellte Fragen zur Verwendung des Netzwerk Uploads zum Importieren von PST-Dateien in Office 365 finden Sie unter [FAQ zum Importieren von PST-Dateien in office 365](faqimporting-pst-files-to-office-365.md).
  
## <a name="step-1-set-up-azure-rights-management-for-pst-import"></a>Schritt 1: Einrichten der Azure-Rechteverwaltung für den PST-Import

Der PST-Import verwendet die Verschlüsselungsfunktionalität des Azure Rights Management (Azure RMS)-Diensts in Office 365. Auf diese Weise können Sie PST-Dateien verschlüsseln, bevor Sie Sie in Office 365 hochladen. 
  
Das Konfigurieren von Azure RMS für PST-Import besteht aus drei Schritten:
  
- [Aktivieren von Azure RMS](#activating-azure-rms)
    
- [Konfigurieren von RMS in Exchange Online](#configuring-rms-in-exchange-online)
    
- [Installieren des Active Directory RMS-Clients](#installing-the-active-directory-rms-client)
    
### <a name="activating-azure-rms"></a>Aktivieren von Azure RMS

Azure RMS ist standardmäßig deaktiviert, aber Sie oder ein anderer Administrator in Ihrer Organisation haben es möglicherweise aktiviert. Folgen Sie den Anweisungen zum [Aktivieren der Azure-Rechteverwaltung](https://docs.microsoft.com/azure/information-protection/deploy-use/activate-service) , um Azure DRM zu installieren und zu aktivieren.
  
### <a name="configuring-rms-in-exchange-online"></a>Konfigurieren von RMS in Exchange Online

Nachdem Sie den Rechteverwaltungsdienst aktiviert haben, besteht der nächste Schritt darin, die Verwaltung von Informationsrechten in Exchange Online für die Verwendung von Azure RMS einzurichten. Weitere Informationen finden Sie unter [Konfigurieren von IRM für die Verwendung der Azure-Rechteverwaltung](https://go.microsoft.com/fwlink/p/?LinkId=394816).
  
1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](https://go.microsoft.com/fwlink/p/?LinkId=396554 ).
    
2. Führen Sie den folgenden Befehl aus, um die RMS-Schlüssel Freigabe-URL festzulegen.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation <RMS key sharing location>
    ```

    Bestimmen Sie anhand der folgenden Tabelle den richtigen Speicherort für die RMS-Schlüssel Freigabe für den Standort Ihrer Organisation.
    
    |**Location**|**RMS-Key-Sharing-Location**|
    |:-----|:-----|
    |Nordamerika  <br/> | `https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Europäische Union  <br/> | `https://sp-rms.eu.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Asien  <br/> | `https://sp-rms.ap.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Südamerika  <br/> | `https://sp-rms.sa.aadrm.com/TenantManagement/ServicePartner.svc` <br/> |
    |Office 365 für Behörden (Community-Cloud der US-Regierung)  <br/> | `https://sp-rms.govus.aadrm.com/TenantManagement/ServicePartner.svc`<sup>1</sup> <br/> |
   
    > [!NOTE]
    > <sup>1</sup> nur Kunden, die Office 365 für Government SKUs (Government Community Cloud) erworben haben, sollten diesen RMS-Schlüssel Freigabespeicherort verwenden. 
  
    Mit diesem Befehl wird beispielsweise der Speicherort der RMS Online-Schlüssel Freigabe in Exchange Online für einen Kunden in Nordamerika konfiguriert.
    
    ```
    Set-IRMConfiguration -RMSOnlineKeySharingLocation "https://sp-rms.na.aadrm.com/TenantManagement/ServicePartner.svc"
    ```

3. Führen Sie den folgenden Befehl aus, um eine vertrauenswürdige VeröffentlichungsDomäne (TPD) aus RMS Online in Ihre Office 365-Organisation zu importieren. 
    
    ```
    Import-RMSTrustedPublishingDomain -RMSOnline -Name "RMS Online"
    ```

    Ein TPD enthält die für die Verwendung von RMS-Funktionen in Ihrer Organisation erforderlichen Einstellungen, einschließlich der Verschlüsselung von PST-Dateien. 
    
4. Führen Sie den folgenden Befehl aus, um IRM für Ihre Office 365-Organisation zu aktivieren.
    
    ```
    Set-IRMConfiguration -InternalLicensingEnabled $true
    ```

### <a name="installing-the-active-directory-rms-client"></a>Installieren des Active Directory RMS-Clients

Der letzte Schritt in diesem Abschnitt ist das Herunterladen des RMS-Clients 2,1 (Rights Management Services). Mit dieser Software wird der Zugriff auf Azure RMS geschützt, und es werden Informationen über Anwendungen geschützt, die Azure RMS verwenden. Installieren Sie den RMS-Client auf dem Computer, den Sie zum Verschlüsseln und Hochladen von PST-Dateien in Schritt 5 verwenden. 
  
1. Herunterladen des [Rights Management Service-clients 2,1](https://www.microsoft.com/en-us/download/details.aspx?id=38396).
    
2. Führen Sie den Assistenten für den Active Directory-RechteverwaltungsDienst-Client 2,1 aus, um den Client zu installieren.

## <a name="step-2-generate-an-encryption-key-for-pst-import"></a>Schritt 2: Generieren eines Verschlüsselungsschlüssels für den PST-Import

Nachdem Sie Azure RMS eingerichtet haben, besteht der nächste Schritt im Generieren eines Verschlüsselungsschlüssels (als symmetrischer Schlüssel bezeichnet), der zum Verschlüsseln der PST-Dateien verwendet wird, die Sie in Office 365 hochladen. Hierzu fügen Sie den PST-Import Dienst als Dienstprinzipal in Azure Active Directory hinzu. Wenn Sie diese Anwendung als Dienstprinzipal hinzufügen, kann der PST-Import Dienst sich direkt bei Azure Active Directory authentifizieren, wenn Sie die verschlüsselten PST-Dateien in Schritt 5 in den Azure-Speicherort hochladen.
  
1. Starten Sie das Azure Active Directory-Modul für Windows PowerShell.
    
2. Führen Sie den folgenden Befehl aus, um eine Verbindung mit dem Microsoft Online-Dienst herzustellen.
    
    ```
    Connect-MsolService
    ```

3. Geben Sie die Anmeldeinformationen für ein Administratorkonto in Ihrer Office 365-Organisation ein, und klicken Sie dann auf **OK**.
    
4. Führen Sie den folgenden Befehl aus, um einen Verschlüsselungsschlüssel zu generieren (einen symmetrischen Schlüssel aufrufen). Erstellen Sie dazu einen neuen PST-Verschlüsselungs Prinzipal.
    
    ```
    New-MsolServicePrincipal -DisplayName PstEncryptionPrincipal
    ```

    Das System zeigt den symmetrischen Schlüssel und die Eigenschaften des neuen PST-Verschlüsselungs Prinzipals an.
    
    ![Kopieren und Speichern des symmetrischen Schlüssels, der angezeigt wird](media/0003fdea-dace-41d2-b49d-f5c98c6230ca.png)
  
5. Kopieren Sie den symmetrischen Schlüssel in eine Text-oder Word-Datei. Wie bereits erwähnt, müssen Sie Vorkehrungen treffen, um diese Datei zu schützen. Da dies der einzige Zeitpunkt ist, an dem der symmetrische Schlüssel angezeigt wird, können Sie auch einen Screenshot dieses Fensters erstellen und ihn in derselben Datei speichern. 
    
    > [!IMPORTANT]
    > Nachdem Sie den PST-Verschlüsselungs Prinzipal erstellt haben, können Sie den symmetrischen Schlüssel nicht mithilfe des Cmdlets **Get-MsolServicePrincipal** abrufen. Deshalb ist es wichtig, den Schlüssel zu speichern. 
  
Lassen Sie das Azure Active Directory-Modul für Windows PowerShell geöffnet und mit dem Microsoft Online-Dienst verbunden. In diesem Fenster führen Sie im nächsten Schritt einen Befehl aus.

## <a name="step-3-obtain-rms-tenant-id-and-licensing-url"></a>Schritt 3: Abrufen der RMS-Mandanten-ID und der Lizenzierungs-URL

Der nächste Schritt besteht darin, die Mandanten-ID und den Lizenzierungs Speicherort für den Azure RMS-Dienst für Ihre Organisation abzurufen. Kopieren und speichern Sie diese Informationen in derselben Datei, die den symmetrischen Schlüssel aus Schritt 2 enthält. Die ID und die URL werden in Schritt 5 zum Verschlüsseln Ihrer PST-Dateien verwendet.
  
1. Führen Sie im Azure Active Directory-Modul für Windows PowerShell (das mit dem Microsoft Online-Dienst verbunden ist) den folgenden Befehl aus, um eine Verbindung mit dem Azure RMS-Dienst in Ihrer Office 365-Organisation herzustellen.
    
    ```
    Connect-AadrmService 
    ```

2. Geben Sie die Anmeldeinformationen für ein Administratorkonto in Ihrer Office 365-Organisation ein, und klicken Sie dann auf **OK**.
    
3. Führen Sie den folgenden Befehl aus, um die Mandanten-ID für den Azure RMS-Dienst in Ihrer Office 365-Organisation anzuzeigen.
    
    ```
    Get-AadrmConfiguration | FL BPOSId
    ```

    Kopieren und speichern Sie den Wert für `BPOSId` die Eigenschaft. 
    
4. Führen Sie den folgenden Befehl aus, um den Lizenzierungs Speicherort für Ihren Azure RMS-Dienst anzuzeigen.
    
    ```
    Get-AadrmConfiguration | FL LicensingIntranetDistributionPointUrl
    ```

    Kopieren und speichern Sie den Wert für `LicensingIntranetDistributionPointUrl` die Eigenschaft. 

## <a name="step-4-download-the-pst-import-tools-and-copy-the-sas-url"></a>Schritt 4: Herunterladen der PST-Import Tools und Kopieren der SAS-URL

Nachdem Sie Azure RMS konfiguriert und die zum Verschlüsseln von PST-Dateien erforderlichen IDs erhalten haben, müssen Sie im nächsten Schritt die Tools herunterladen und installieren, die Sie in Schritt 5 ausführen müssen, um PST-Dateien in Office 365 zu verschlüsseln und hochzuladen. Diese Tools sind das Azure-AzCopy-Tool und das Office 365-Daten Verschlüsselungstool. Außerdem kopieren Sie die SAS-URL für Ihre Organisation. Diese URL ist eine Kombination aus der Netzwerk-URL für den Azure-Speicherort in der Microsoft-Cloud für Ihre Organisation und einem SAS-Schlüssel (Shared Access Signature). Dieser Schlüssel enthält die erforderlichen Berechtigungen zum Hochladen von PST-Dateien an den Azure-Speicherort. Speichern Sie es in der Datei, in die Sie die anderen Informationen kopiert haben, in Schritt 2 und Schritt 3. Treffen Sie, wie bereits erwähnt, Vorkehrungen zum Schutz der SAS-URL. 
  
> [!IMPORTANT]
> Sie müssen die Azure AzCopy Version 5,0 verwenden, um PST-Dateien erfolgreich an den Azure-Speicherort hochzuladen. Neuere Versionen des AzCopy-Tools werden für den Import von PST-Dateien in Office 365 nicht unterstützt. Stellen Sie sicher, dass Sie das AzCopy-Tool über die Seite zum **Hochladen von Dateien über das Netzwerk** herunterladen, indem Sie die Verfahren in diesem Schritt ausführen. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit den Anmeldeinformationen für ein Administratorkonto in Ihrer Office 365-Organisation an.
    
3. Klicken Sie im linken Bereich auf **Datenverwaltung** , und klicken Sie dann auf **importieren**.
    
4. Klicken Sie auf der Seite **Import** auf **Zum Importdienst wechseln**.
    
5. klicken sie auf der seite **daten in Office 365 importieren** auf **neues auftrags** ![symbol](media/ITPro-EAC-AddIcon.gif), und klicken sie dann auf **e-mail-nachrichten hochladen (PST-dateien)**.
    
6. Klicken Sie auf der Seite **Dateien über das Netzwerk hochladen** in Schritt 2 auf **Netzwerk-Upload-SAS-URL anzeigen**.
    
7. Nachdem die URL angezeigt wurde, kopieren Sie Sie, und speichern Sie Sie in der Datei, in der Sie die anderen Schlüssel gespeichert haben. Kopieren Sie unbedingt die gesamte URL. 
    
8. Klicken Sie in Schritt 3 auf **Azure AzCopy Tool herunterladen** , um das Azure AzCopy-Tool herunterzuladen und zu installieren. 
    
9. Klicken Sie im Popupfenster auf **Ausführen** , um das Azure AzCopy-Tool zu installieren. 
    
    > [!IMPORTANT]
    > Stellen Sie sicher, dass Sie das Azure AzCopy-Tool am Standardspeicherort `%ProgramFiles(x86)%\Microsoft SDKs\Azure\AzCopy` auf einem computer mit 64-Bit-Windows installieren. Das liegt daran, dass beim Ausführen von "O365importtool. exe in Schritt 5 nach dem AzCopy-Tool an diesem Speicherort gesucht wird. 
  
10. Nachdem Sie das Azure AzCopy-Tool installiert haben, klicken Sie auf **Office 365-Datenverschlüsselung und-Import-Tool herunterladen**.
    
11. Klicken Sie **** \> **** im Popupfenster auf Speichern unter, um die Datei "o365importtool. zip in einem Ordner auf dem lokalen Computer zu speichern. 
    
12. Extrahieren Sie die Datei "O365importtool. zip.
    
13. Klicken Sie auf **Abbrechen** , um die **Uploaddateien über die Seite Netzwerk** zu schließen. 
 
## <a name="step-5-encrypt-and-upload-your-pst-files-to-office-365"></a>Schritt 5: verSchlüsseln und Hochladen der PST-Dateien in Office 365

Nachdem Sie Schritt 1 bis Schritt 4 abgeschlossen haben, können Sie das "O365importtool. exe-Tool verwenden, um PST-Dateien in Office 365 zu verschlüsseln und hochzuladen. Mit diesem Tool werden Ihre PST-Dateien verschlüsselt und dann hochgeladen und an einem Azure-Speicherort in der Microsoft-Cloud gespeichert. Damit Sie diesen Schritt ausführen können, müssen sich die PST-Dateien in einer Dateifreigabe oder auf einem Dateiserver in Ihrer Organisation befinden. Im folgenden Verfahren wird dies als das Quellverzeichnis bezeichnet. Jedes Mal, wenn Sie das "O365importtool. exe-Tool ausführen, können Sie ein anderes Quellverzeichnis angeben. 
  
1. Öffnen Sie eine Eingabeaufforderung auf dem lokalen Computer.
    
2. Wechseln Sie zu dem Verzeichnis, in dem Sie das Tool "O365importtool. exe in Schritt 4 installiert haben.
    
3. Führen Sie den folgenden Befehl aus, um PST-Dateien in Office 365 zu verschlüsseln und hochzuladen.
    
    ```
    O365ImportTool.exe /srcdir:<Location of PST files> /protect-rmsserver:<RMS licensing location> /protect-tenantid:<BPOSId> /protect-key:<Symmetric key> /transfer:upload /upload-dest:<Network upload URL> /upload-destSAS:<SAS key>
    ```

    In der folgenden Tabelle werden die Parameter und deren erforderliche Werte beschrieben. Beachten Sie, dass die Informationen, die Sie in den vorherigen Schritten abgerufen haben, in den Werten für diese Parameter verwendet werden.
    
    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `/srcdir:` <br/> |Gibt das Quellverzeichnis in Ihrer Organisation an, das die PST-Dateien enthält, die in Office 365 hochgeladen werden.  <br/> | `/srcdir:\\FILESERVER01\PSTs` <br/> |
    | `/protect-rmsserver:` <br/> |Gibt den Lizenzierungs Speicherort für Ihren Azure RMS-Dienst an. Verwenden Sie den Wert der `LicensingIntranetDistributionPointUrl` Eigenschaft, die Sie in Schritt 3 abgerufen haben. Stellen Sie sicher, dass Sie den Wert dieses Parameters mit doppelten Anführungszeichen ("") umgeben.  <br/> | `/protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing"` <br/> |
    | `/protect-tenantid:` <br/> |Gibt die Identität ihrer Azure RMS-Organisation an. Verwenden Sie den Wert der `BPOSId` Eigenschaft, die Sie in Schritt 3 abgerufen haben.  <br/> | `/protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b` <br/> |
    | `/protect-key:` <br/> |Gibt den symmetrischen Schlüssel an, den Sie in Schritt 2 abgerufen haben. Stellen Sie sicher, dass Sie den Wert dieses Parameters in doppelte Anführungszeichen ("") einschließen.  <br/> | `/protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867="` <br/> |
    | `/transfer:` <br/> |Gibt an, ob Sie PST-Dateien über das Netzwerk hochladen oder auf einer Festplatte versenden. Der Wert `upload` gibt an, dass Sie die Dateien über das Netzwerk hochladen. Der Wert `drive` gibt an, dass Sie die PST auf einer Festplatte Verschiffen.  <br/> | `/transfer:upload` <br/> |
    | `/upload-dest:` <br/> |Gibt das Ziel in Office 365 an, in das die PST-Dateien hochgeladen werden sollen. Dies ist der Azure-Speicherort für Ihre Organisation. Der Wert für diesen Parameter besteht aus der Netzwerk-Upload-URL aus der SAS-URL, die Sie in Schritt 4 kopiert haben. Stellen Sie sicher, dass Sie den Wert dieses Parameters in doppelte Anführungszeichen ("") einschließen.  <br/><br/> **Tipp:** Optional Sie können einen Unterordner im Azure-Speicherort angeben, in den die verschlüsselten PST-Dateien hochgeladen werden sollen. Hierzu fügen Sie einen Unterordner Speicherort (nach "ingestiondata") in der Netzwerk-Upload-URL hinzu. Im ersten Beispiel wird kein Unterordner angegeben; Das heißt, dass die PST in den Stamm (mit dem Namen *ingestiondata* ) des Azure-Speicherorts hochgeladen wird. Im zweiten Beispiel werden die PST-Dateien in einen Unterordner (mit dem Namen *EncryptedPSTs* ) im Azure-Speicherort hochgeladen.           | `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata"` <br/> Oder  <br/>  `/upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata/EncryptedPSTs"` <br/> |
    | `/upload-destSAS:` <br/> |Gibt den SAS-Schlüssel für Ihre Organisation an. Der Wert für diesen Parameter besteht aus dem SAS-Schlüssel aus der SAS-URL, die Sie in Schritt 4 kopiert haben. Beachten Sie, dass das erste Zeichen in der SAS-Taste ein Fragezeichen ("?") ist. Stellen Sie sicher, dass Sie den Wert dieses Parameters in doppelte Anführungszeichen ("") einschließen.  <br/> | `/upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"` <br/> |
    | `/recurse` <br/> |Diese optionale Option gibt den rekursiven Modus an, sodass das Tool "O365importtool. exe PST-Dateien in Unterordnern im Quellverzeichnis, das durch den `/srcdir:` -Parameter angegeben ist, kopiert.  <br/><br/> **Hinweis:** Wenn Sie diese Option verwenden, haben PST-Dateien in Unterordnern einen anderen Datei Pfad im Azure-Speicher Speicherort, nachdem Sie hochgeladen wurden. Sie müssen den genauen Dateipfadnamen in der CSV-Datei angeben, die Sie in Schritt 7 erstellen.           | `/recurse` <br/> |
   
    NachFolgend finden Sie ein Beispiel für die Syntax für das "O365importtool. exe-Tool, das die tatsächlichen Werte für jeden Parameter verwendet:
    
    ```
    O365ImportTool.exe /srcdir:\\FILESERVER01\PSTs /protect-rmsserver:"https://afcbd8ec-cb2b-4a1a-8246-0b4bc22d1978.rms.na.aadrm.com/_wmcs/licensing" /protect-tenantid:42745b33-2a5c-4726-8a2a-ca43caa0f74b  /protect-key:"l+R+Umc5RGmSBh1oW+DoyMxm/h5h2JJXFcNOFiNp867=" /transfer:upload /upload-dest:"https://3c3e5952a2764023ad14984.blob.core.windows.net/ingestiondata" /upload-destSAS:"?sv=2012-02-12&amp;se=9999-12-31T23%3A59%3A59Z&amp;sr=c&amp;si=IngestionSasForAzCopy201601121920498117&amp;sig=Vt5S4hVzlzMcBkuH8bH711atBffdrOS72TlV1mNdORg%3D"
    ```

    Nachdem Sie den Befehl ausgeführt haben, werden Statusmeldungen angezeigt, die den Fortschritt der Verschlüsselung und des Uploads der PST-Dateien anzeigen. Eine endgültige Statusmeldung zeigt die Gesamtanzahl der Dateien an, die erfolgreich verschlüsselt und hochgeladen wurden. 
    
    > [!TIP]
    > Nachdem Sie den Befehl "O365importtool. exe erfolgreich ausgeführt haben und sichergestellt haben, dass alle Parameter korrekt sind, speichern Sie eine Kopie der Befehlszeilensyntax in derselben (sicheren) Datei, in der Sie die in den vorherigen Schritten abgerufenen Informationen kopiert haben. Anschließend können Sie diesen Befehl in einer eingabeaufForderungen kopieren und jedes Mal einfügen, wenn Sie das "O365importtool. exe-Tool zum Verschlüsseln und Hochladen von PST-Dateien in Office 365 ausführen möchten. Die einzigen Werte, die Sie möglicherweise ändern müssen, sind `/srcdir:` die `/upload-dest:` für die Parameter und. 
  
## <a name="optional-step-6-view-a-list-of-the-pst-files-uploaded-to-office-365"></a>Optional Schritt 6: Anzeigen einer Liste der PST-Dateien, die in Office 365 hochgeladen wurden

Als optionaler Schritt können Sie den Microsoft Azure Storage Explorer (ein kostenloses Open Source-Tool) installieren und verwenden, um die Liste der PST-Dateien anzuzeigen, die Sie in das Azure-BLOB hochgeladen haben. Dafür gibt es drei gute Gründe:
  
- Stellen Sie sicher, dass PST-Dateien aus dem freigegebenen Ordner oder Dateiserver in Ihrer Organisation erfolgreich in das Azure-BLOB hochgeladen wurden.

- Stellen Sie sicher, dass die PST-Dateien verschlüsselt sind. VerSchlüsselte PST- `.pfile` Dateien haben eine Erweiterung an den PST-Dateinamen angefügt; Beispiel: `pilarp.pst.pfile`.
    
- Überprüfen Sie den Dateinamen (und den Pfadnamen des Unterordners, wenn Sie einen enthalten) für jede PST-Datei, die in das Azure-BLOB hochgeladen wurde. Dies ist sehr hilfreich, wenn Sie die PST-Zuordnungsdatei im nächsten Schritt erstellen, da Sie sowohl den Ordner Pfadnamen als auch den Dateinamen für jede PST-Datei angeben müssen. Die Überprüfung dieser Namen kann dazu beitragen, potenzielle Fehler in Ihrer PST-Zuordnungsdatei zu reduzieren.
    
Der Microsoft Azure-Speicher-Explorer befindet sich in der Vorschau. 
  
 > [!IMPORTANT]
>  Sie können den Azure-Speicher-Explorer nicht verwenden, um PST-Dateien hochzuladen oder zu ändern. Die einzige unterstützte Methode zum Importieren von PST-Dateien in Office 365 ist die Verwendung von AzCopy. Außerdem können Sie keine PST-Dateien löschen, die Sie in das Azure-BLOB hochgeladen haben. Wenn Sie versuchen, eine PST-Datei zu löschen, wird eine Fehlermeldung angezeigt, in der Sie darauf hingewiesen werden, dass Sie nicht über die erforderlichen Berechtigungen verfügen. Beachten Sie, dass alle PST-Dateien automatisch aus Ihrem Azure-Speicherbereich gelöscht werden. If there are no import jobs in progress, then all PST files in the **ingestiondata** container are deleted 30 days after the most recent import job was created. 
  
So installieren Sie den Azure Storage Explorer und stellen eine Verbindung mit Ihrem Azure-Speicherbereich her:
  
1. Laden Sie das [Microsoft Azure Storage Explorer-Tool](https://go.microsoft.com/fwlink/p/?LinkId=544842)herunter, und installieren Sie es.
    
2. Starten Sie den Microsoft Azure Storage Explorer, klicken Sie im linken Bereich mit der rechten Maustaste auf **Speicherkonten** , und klicken Sie dann auf mit **Azure-Speicher verbinden**. 
    
    ![Klicken Sie mit der rechten Maustaste auf Speicherkonten, und klicken Sie dann auf mit Azure-Speicher verbinden](media/75b80cc3-c336-4f96-ad32-54ac9b96a7af.png)
  
3. Fügen Sie in das Feld unter **mit Azure-Speicher verbinden**die in Schritt 4 abgerufene SAS-URL ein, und klicken Sie dann auf **weiter**. 
    
    ![Fügen Sie die SAS-URL in das Feld auf der Seite mit Azure-Speicher verbinden ein.](media/5d034128-e087-48e1-9ebc-4c9fa262d5b7.png)
  
4. Auf der Zusammenfassungsseite der **Verbindung** können Sie die Verbindungsinformationen überarbeiten und dann auf **verbinden**klicken. 
    
5. Erweitern Sie unter **Speicherkonten**den Knoten **(Dienst-SAS)** , und erweitern Sie dann den Knoten **BLOB-Container** . 
    
6. Klicken Sie mit der rechten Maustaste auf **ingestiondata**, und klicken Sie dann auf **BLOB-Container-Editor öffnen**.
    
    ![Klicken Sie mit der rechten Maustaste auf ingestiondata und dann auf BLOB-Container-Editor öffnen.](media/f50eee30-9202-4efc-904a-2895a0bc388d.png)
  
    Der Azure-Speicherbereich mit einer Liste der PST-Dateien, die Sie in Schritt 5 hochgeladen haben, wird angezeigt.
    
    ![Azure Storage Explorer zeigt eine Liste der PST-Dateien an, die Sie hochgeladen haben](media/a448ae43-e744-4153-8304-22b59e93883c.png)
  
7. Wenn Sie die Verwendung von Microsoft Azure Storage Explorer abgeschlossen haben, klicken Sie mit der rechten Maustaste auf **** **ingestiondata**, und klicken Sie dann auf trennen, um die Verbindung mit dem Azure-Speicherbereich zu trennen. Andernfalls erhalten Sie eine Fehlermeldung, wenn Sie das nächste Mal anfügen. 
    
    ![Klicken Sie mit der rechten Maustaste auf die Einnahme, und klicken Sie auf trennen, um die Verbindung mit Ihrem Azure-Speicherbereich](media/1e8e5e95-4215-4ce4-a13d-ab5f826a0510.png)
  
## <a name="step-7-create-the-pst-import-mapping-file"></a>Schritt 7: Erstellen der PST-Import Zuordnungsdatei

Nachdem die PST-Dateien verschlüsselt und an den Azure-Speicherort für Ihre Office 365-Organisation hochgeladen wurden, besteht der nächste Schritt darin, eine CSV-Datei (Comma Separated Value) zu erstellen, die angibt, in welche Benutzerpostfächer die PST-Dateien importiert werden sollen. Diese CSV-Datei wird im nächsten Schritt übermittelt, wenn Sie einen PST-Importauftrag erstellen.
  
1. [Laden Sie eine Kopie der PST-Import Zuordnungsdatei herunter](https://go.microsoft.com/fwlink/p/?LinkId=544717). 
    
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

    Die erste Zeile oder Kopfzeile der CSV-Datei enthält die Parameter, die vom PST-Importdienst verwendet werden, um die PST-Dateien in Benutzerpostfächer zu importieren. Die einzelnen Parameternamen werden jeweils durch ein Komma getrennt. Jede Zeile unter der Kopfzeile stellt die Parameterwerte für das Importieren einer PST-Datei in ein bestimmtes Postfach dar. Sie benötigen eine Zeile für jede PST-Datei, die Sie in ein Benutzerpostfach importieren möchten. Vergessen Sie nicht, die Platzhalterdaten in der Zuordnungsdatei durch die tatsächlichen Werte zu ersetzen.
    
    > [!NOTE]
    > Ändern Sie nichts in der Kopfzeile, einschließlich der SharePoint-Parameter; diese werden während des PST-Importvorgangs ignoriert. 
  
3. Verwenden Sie die Informationen in der folgenden Tabelle, um zu die CSV-Datei mit den erforderlichen Informationen zu füllen.
    
    |**Parameter**|**Beschreibung**|**Beispiel**|
    |:-----|:-----|:-----|
    | `Workload` <br/> |Gibt den Office 365-Dienst an, in den die Daten importiert werden. Verwenden `Exchange`Sie zum Importieren von PST-Dateien in Benutzerpostfächer.  <br/> | `Exchange` <br/> |
    | `FilePath` <br/> |Gibt den Speicherort des Ordners an dem Azure-Speicherort an, in den Sie die PST-Dateien in Schritt 5 hochgeladen haben.  <br/>  Wenn Sie in Schritt 5 keinen Namen für den optionalen Unterordner in die `/upload-dest:` Netzwerk-URL aufgenommen haben, lassen Sie diesen Parameter in der CSV-Datei leer. Wenn Sie einen Unterordnernamen hinzugefügt haben, geben Sie ihn in diesem Parameter an. Bei dem Wert für diesen Parameter wird die Groß-/Kleinschreibung beachtet. In beiden Fällen *müssen Sie nicht* "ingestiondata" in den Wert des `FilePath` Parameters aufnehmen.  <br/> <br/>**Wichtig:** Bei dem Dateipfadnamen muss es sich um den gleichen Fall handeln, den Sie verwendet haben, wenn Sie einen optionalen Unterordnernamen in die `/upload-dest:` SAS-URL im Parameter in Schritt 5 aufgenommen haben. Wenn Sie beispielsweise für den `EncryptedPSTs` Namen des Unterordners in Schritt 5 verwendet haben und `encryptedpsts` dann den `FilePath` Parameter in der CSV-Datei verwenden, tritt beim Import für die PST-Datei ein Fehler auf. Stellen Sie sicher, dass Sie den gleichen Fall in beiden Instanzen verwenden.           |(leer lassen)  <br/> Oder  <br/>  `EncryptedPSTs` <br/> |
    | `Name` <br/> |Gibt den Namen der PST-Datei an, die in das Benutzerpostfach importiert wird.  Bei dem Wert für diesen Parameter wird die Groß-/Kleinschreibung beachtet. Da die PST-Dateien, die in den Azure-Speicherort hochgeladen werden, `.pfile` verschlüsselt sind, wird dem PST-Dateinamen eine Erweiterung hinzugefügt. Sie müssen die `.pfile` Erweiterung dem Namen der PST-Dateien in der CSV-Datei hinzufügen.  <br/><br/> **Wichtig:** Der Fall für den PST-Dateinamen in der CSV-Datei muss mit der PST-Datei übereinstimmen, die in Schritt 5 in den Azure-Speicherort hochgeladen wurde. Wenn Sie beispielsweise den `annb.pst.pfile` `Name` Parameter in der CSV-Datei verwenden, aber der Name der tatsächlichen PST-Datei lautet `AnnB.pst`, schlägt der Import für diese PST-Datei fehl. Stellen Sie sicher, dass der Name der PST in der CSV-Datei den gleichen Fall wie die tatsächliche PST-Datei verwendet.           | `annb.pst.pfile` <br/> |
    | `Mailbox` <br/> |Gibt die E-Mail-Adresse des Postfachs an, in das die PST-Datei importiert werden soll.   <br/> Um eine PST-Datei in ein inaktives Postfach zu importieren, müssen Sie die Postfach-GUID für diesen Parameter angeben. Führen Sie den folgenden PowerShell-Befehl in Exchange Online aus, um diese GUID zu erhalten:`Get-Mailbox -InactiveMailboxOnly <identity of inactive mailbox> | FL Guid` <br/><br/> **Hinweis:** In einigen Fällen verfügen Sie möglicherweise über mehrere Postfächer mit derselben e-Mail-Adresse, wobei ein Postfach ein aktives Postfach und das andere Postfach den Status "Soft-Deleted" (oder inaktiv) aufweist. In diesen Fällen müssen Sie die Postfach-GUID angeben, um das Postfach, in das die PST-Datei importiert werden soll, eindeutig zu identifizieren. Führen Sie den folgenden PowerShell-Befehl aus, um diese GUID für aktive `Get-Mailbox - <identity of active mailbox> | FL Guid`Postfächer zu erhalten:. Führen Sie diesen Befehl aus, um die GUID für Soft-deleted (oder inactive)-Postfächer abzurufen.`Get-Mailbox - <identity of soft-deleted or inactive mailbox> -SoftDeletedMailbox | FL Guid`           | `annb@contoso.onmicrosoft.com` <br/> Oder  <br/>  `2d7a87fe-d6a2-40cc-8aff-1ebea80d4ae7` <br/> |
    | `IsArchive` <br/> | Gibt an, ob die PST-Datei in das Archivpostfach des Benutzers importiert werden soll. Es gibt zwei Möglichkeiten:  <br/> **False** Importiert die PST-Datei in das primäre Postfach des Benutzers.  <br/> **True** Importiert die PST-Datei in das Archivpostfach des Benutzers.  <br/>  If you leave this parameter blank, the PST file is imported to the user's primary mailbox.  <br/><br/> **Hinweis:** Wenn Sie eine PST-Datei in ein cloudbasierten Archivpostfach für einen Benutzer importieren möchten, dessen primäres Postfach lokal ist, geben Sie für diesen Parameter nur **true** an, und geben Sie die e-Mail-Adresse für das `Mailbox` lokale Postfach des Benutzers für den Parameter an.           | `FALSE` <br/> Oder  <br/>  `TRUE` <br/> |
    | `TargetRootFolder` <br/> | Gibt den Postfachordner an, in den die PST-Datei importiert wird.  <br/>  Wenn Sie diesen Parameter leer lassen, wird die PST-Datei in einen neuen Ordner mit dem Namen " **importiert** " auf der Stammebene des Postfachs importiert (dieselbe Ebene wie der Posteingangsordner und die anderen Standard Postfachordner).  <br/>  Wenn Sie angeben `/`, werden die Elemente in der PST-Datei direkt in den Ordner Posteingang des Benutzers importiert.  <br/>  Wenn Sie angeben `/<foldername>`, werden die Elemente in der PST-Datei in einen Unterordner mit dem Namen * \<\> FolderName* importiert. Wenn Sie beispielsweise verwendet `/ImportedPst`haben, werden die Elemente in einen Unterordner mit dem Namen **ImportedPst**importiert. Dieser Unterordner befindet sich im Ordner Posteingang des Benutzers.  <br/><br/> **Tipp:** Erwägen Sie, einige Test Batches auszuführen, um mit diesem Parameter zu experimentieren, damit Sie den besten Ordnerspeicherort bestimmen können, in den PST-Dateien importiert werden sollen.           |(leer lassen)  <br/> Oder  <br/>  `/` <br/> Oder  <br/>  `/ImportedPst` <br/> |
    | `ContentCodePage` <br/> |Dieser optionale Parameter gibt einen numerischen Wert für die Codepage an, die zum Importieren von PST-Dateien im ANSI-Dateiformat verwendet werden soll. Dieser Parameter wird zum Importieren von PST-Dateien aus Chinesisch, Japanisch und Koreanisch (CJK) verwendet, da in diesen Sprachen in der Regel ein Double-Byte-Zeichensatz (DBCS) für die Zeichencodierung verwendet wird. Wenn dieser Parameter nicht zum Importieren von PST-Dateien für Sprachen verwendet wird, die DBCS für Postfachordner Namen verwenden, werden die Ordnernamen oft verstümmelt, nachdem Sie importiert wurden. Eine Liste der unterstützten Werte für diesen Parameter finden Sie unter [Code Page Identifiers](https://go.microsoft.com/fwlink/p/?LinkId=328514).  <br/><br/> **Hinweis:** Wie bereits erwähnt, handelt es sich um einen optionalen Parameter, den Sie nicht in die CSV-Datei aufnehmen müssen. Sie können Sie auch hinzufügen und den Wert für eine oder mehrere Zeilen leer lassen.           |(leer lassen)  <br/> Oder  <br/>  `932`(Dies ist die Codepage-ID für ANSI/OEM Japanisch)  <br/> |
    | `SPFileContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPManifestContainer` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
    | `SPSiteUrl` <br/> |Lassen Sie diesen Parameter für den PST-Import leer.   <br/> |Nicht zutreffend  <br/> |
  
## <a name="step-8-create-a-pst-import-job-in-office-365"></a>Schritt 8: Erstellen eines PST-Import Auftrags in Office 365

Der letzte Schritt besteht darin, den PST-Importauftrag im Import Dienst in Office 365 zu erstellen. Wie bereits erläutert, übermitteln Sie die PST-Import Zuordnungsdatei, die Sie in Schritt 7 erstellt haben. Nach dem Erstellen des neuen Auftrags verwendet der Import Dienst die Informationen in der Zuordnungsdatei, um die PST-Dateien (die Sie in Schritt 5 in Office 365 hochgeladen haben) an das angegebene Benutzerpostfach zu verschlüsseln und zu importieren. 
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).
    
2. Melden Sie sich bei Office 365 mit den Anmeldeinformationen für ein Administratorkonto in Ihrer Office 365-Organisation an.
    
3. Klicken Sie im linken Bereich auf **Datenverwaltung** , und klicken Sie dann auf **importieren**.
    
4. Klicken Sie auf der Seite **Import** auf **Zum Importdienst wechseln**.
    
5. klicken sie auf der seite **daten in Office 365 importieren** auf **neues auftrags**![symbol](media/ITPro-EAC-AddIcon.gif), und klicken sie dann auf **e-mail-nachrichten hochladen (PST-dateien)**.
    
6. Klicken Sie auf der Seite **Dateien über das Netzwerk hochladen** auf die Kontrollkästchen **Ich habe meine Dateien hochgeladen** , und **Ich habe Zugriff auf die Zuordnungsdatei** , und klicken Sie dann auf **weiter**. 
    
7. Geben Sie einen Namen für den PST-Importauftrag an, und klicken Sie dann auf **Weiter**.
    
8. Klicken Sie auf hinzu](media/ITPro-EAC-AddIcon.gif) fügen, um die PST-Zuordnungsdatei auszuwählen, die Sie in Schritt 7 erstellt haben. **** ![ 
    
9. Nachdem der Name der CSV-Datei in der Liste angezeigt wurde, wählen Sie ihn aus **** , und klicken Sie dann auf überprüfen, um die CSV-Datei auf Fehler zu prüfen. 
    
    > [!NOTE]
    > Wie bereits erläutert, wird bei der Verschlüsselung der PST-Dateien `.pfile` eine Erweiterung an den PST-Dateinamen angehängt. Sie müssen die `.pfile` Erweiterung dem Namen der PST-Dateien in der CSV-Datei hinzufügen. Andernfalls schlägt die Überprüfung der CSV-Datei fehl. 
  
    Die CSV-Datei muss erfolgreich validiert werden, um einen PST-Import Auftrag zu erstellen. Wenn die Überprüfung fehlschlägt, klicken Sie in der Spalte **Status** auf den Link **ungültig** . Eine Kopie Ihrer PST-Import Zuordnungsdatei wird geöffnet, und es wird eine Fehlermeldung für jede Zeile in der Datei angezeigt, die fehlgeschlagen ist. 
    
10. Wenn die PST-Zuordnungsdatei erfolgreich überprüft wurde, lesen Sie das Dokument mit den allgemeinen Geschäftsbedingungen, und klicken Sie dann auf das Kontrollkästchen.
    
11. Klicken Sie auf **Fertig stellen** , um den Auftrag zu übermitteln. 
    
    Der Auftrag wird in der Liste der PST-Importaufträge auf der Seite **Daten in Office 365 importieren** angezeigt. 
    
12. Wählen Sie den Auftrag aus ****![, und klicken](media/O365-MDM-Policy-RefreshIcon.gif) Sie auf aktualisieren, um die Statusinformationen zu aktualisieren, die im Detailbereich angezeigt werden. 
    
13. Klicken Sie im Detailbereich auf **Details anzeigen** , um den aktuellen Status für den ausgewählten Auftrag abzurufen. 
 
## <a name="more-information"></a>Weitere Informationen

- Gründe für das Importieren von PST-Dateien in Office 365
    
  - Es ist eine gute Möglichkeit, die e-Mails Ihrer Organisation zu Office 365 zu migrieren.
    
  - Es hilft Ihnen dabei, die Compliance-Anforderungen Ihrer Organisation zu erfüllen, indem Sie:
    
  - Aktivieren der Archivierung von Postfächern, um Benutzern zusätzlichen Speicherplatz im Postfach bereitzustellen.
    
  - Aufbewahrung von Postfächern zur Aufbewahrung von Inhalten
    
  - Verwenden von Microsoft eDiscovery-Tools zum Suchen nach Inhalten in Postfächern
    
  - Verwenden von Aufbewahrungsrichtlinien, um zu steuern, wie lange Postfachinhalte aufbewahrt werden.
    
  - Durchsuchen Sie das Office 365-Überwachungsprotokoll nach Post fachbezogenen Ereignissen.
    
  - Sie schützt vor Datenverlust. PST-Dateien, die in Office 365-Postfächer importiert werden, erben die Hochverfügbarkeitsfeatures von Exchange Online, im Gegensatz zum Speichern der Daten auf dem Computer eines Benutzers.
    
  - Die Daten sind für den Benutzer auf allen Geräten verfügbar, da Sie in der Cloud gespeichert sind.
    
- Nachfolgend finden Sie ein Beispiel für die Schlüssel, IDs und URLs, die in den Schritten 2, 3 und 4 abgerufen werden. Dieses Beispiel enthält auch die Syntax für den Befehl, den Sie im Tool "O365importtool. exe ausführen, um PST-Dateien in Office 365 zu verschlüsseln und hochzuladen. Ergreifen Sie entsprechende Vorsichtsmaßnahmen, um diese so zu schützen, wie Sie Kennwörter oder andere Sicherheitsinformationen schützen würden.
    
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

- Wie bereits erläutert, aktiviert der Office 365-Import Dienst die Einstellung Aufbewahrungszeit (für unbestimmte Dauer), nachdem PST-Dateien in ein Postfach importiert wurden. Dies bedeutet, dass die *RentionHoldEnabled* -Eigenschaft `True` auf festgelegt ist, sodass die dem Postfach zugewiesene Aufbewahrungsrichtlinie nicht verarbeitet wird. Dadurch erhält der Postfachbesitzer Zeit zum Verwalten der neu importierten Nachrichten, indem verhindert wird, dass eine Lösch-oder Archivrichtlinie ältere Nachrichten löscht oder archiviert. Hier sind einige Schritte, die Sie zum Verwalten dieser Aufbewahrungsdauer ausführen können: 
    
  - Sie können die Aufbewahrungszeit nach einem bestimmten Zeitraum deaktivieren, indem Sie den `Set-Mailbox -RetentionHoldEnabled $false` Befehl ausführen. Weitere Informationen finden Sie unter [Platzieren einer aufbewahrungsZeit für ein Postfach](https://go.microsoft.com/fwlink/p/?LinkId=544749).
    
  - Sie können die Aufbewahrungsdauer so konfigurieren, dass Sie zu einem bestimmten Zeitpunkt in der Zukunft deaktiviert wird. Führen Sie dazu den `Set-Mailbox -EndDateForRetentionHold <date>` Befehl aus. Wenn Sie beispielsweise davon ausgehen, dass das heutige Datum 1. Juni 2016 ist und die Aufbewahrungszeit in 30 Tagen deaktiviert werden soll, führen Sie den `Set-Mailbox -EndDateForRetentionHold 7/1/2016`folgenden Befehl aus:. In diesem Szenario lassen Sie die *RentionHoldEnabled* -Eigenschaft auf `True`festgelegt. Weitere Informationen finden Sie unter [Set-Mailbox](https://go.microsoft.com/fwlink/p/?LinkId=150317).
    
  - Sie können die Einstellungen für die Aufbewahrungsrichtlinie ändern, die dem Postfach zugewiesen ist, sodass ältere importierte Elemente nicht sofort gelöscht oder in das Archivpostfach des Benutzers verschoben werden. Sie können beispielsweise das Aufbewahrungs Alter für eine Lösch-oder Archivrichtlinie verlängern, die dem Postfach zugewiesen ist. In diesem Szenario würden Sie die Aufbewahrungszeit für das Postfach deaktivieren, nachdem Sie die Einstellungen der Aufbewahrungsrichtlinie geändert haben. Weitere Informationen finden Sie unter [Einrichten einer Archiv-und Löschrichtlinie für Postfächer in Ihrer Office 365-Organisation](set-up-an-archive-and-deletion-policy-for-mailboxes.md).
