---
title: Erstellen benutzerdefinierter vertraulicher Informationstypen mit genauer Datenübereinstimmung
ms.author: chrfox
author: chrfox
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
ms.date: 05/15/2019
localization_priority: Priority
ms.collection:
- M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Erstellen Sie benutzerdefinierte vertrauliche Informationstypen mit genauer Datenübereinstimmungsklassifizierung.
ms.openlocfilehash: be86f22ec20d36aaf12ae253028d0896f885267e
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230839"
---
# <a name="create-custom-sensitive-information-types-with-exact-data-match-based-classification-preview"></a>Erstellen benutzerdefinierter vertraulicher Informationstypen mit genauer Datenübereinstimmungsklassifizierung (Vorschau)

## <a name="overview"></a>Übersicht

[Benutzerdefinierte vertrauliche Informationstypen](custom-sensitive-info-types.md) werden verwendet, um zu verhindern, dass vertrauliche Informationen versehentlich oder unangemessen weitergegeben werden. Als Administrator können Sie das [Security & Compliance Center](create-a-custom-sensitive-information-type.md) oder [PowerShell](create-a-custom-sensitive-information-type-in-scc-powershell.md) verwenden, um einen benutzerdefinierten vertraulichen Informationstyp basierend auf Mustern, Nachweisen (Stichwörtern wie *Mitarbeiter*, *Abzeichen*, *ID* usw.), Zeichenabstand (wie nahe Nachweise sich an Zeichen in einem bestimmten Muster befinden) und Vertrauensstufen zu definieren. Solche benutzerdefinierten vertraulichen Informationstypen erfüllen die geschäftlichen Anforderungen vieler Organisationen.

Was aber, wenn Sie einen benutzerdefinierten vertraulichen Informationstyp verwenden möchten, der genaue Datenwerte anstelle von Mustern und Näherungswerten verwendet? Mit einer EDM-basierten Klassifizierung (genaue Datenübereinstimmung) können Sie einen benutzerdefinierten Informationstyp mit den folgenden Merkmalen erstellen:
- dynamisch und aktualisierbar;
- höhere Skalierbarkeit;
- weniger falsch positive Ergebnisse;
- Arbeiten mit strukturierten vertraulichen Daten;
- vertrauliche Informationen sicherer behandeln; 
- Verwendbarkeit mit mehreren Microsoft Cloud Services.

![EDM-basierte Klassifikation](media/EDMClassification.png)

Die EDM-basierte Klassifikation ermöglicht es Ihnen, benutzerdefinierte vertrauliche Informationstypen zu erstellen, die sich auf genaue Werte in einer Datenbank mit vertraulichen Informationen beziehen. Die Datenbank kann täglich oder wöchentlich aktualisiert werden und bis zu 10 Millionen Datenzeilen enthalten. Mitarbeiter, Patienten oder Kunden kommen und gehen und Datensätze ändern sich, aber Ihre benutzerdefinierten vertraulichen Informationstypen bleiben aktuell und anwendbar. Darüber hinaus können Sie EDM-basierte Klassifikation mit Richtlinien verwenden, z. B. [Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md) (Data Loss Prevention, DLP) oder [Microsoft Cloud App Security-Dateirichtlinien](https://docs.microsoft.com/cloud-app-security/data-protection-policies).

## <a name="required-licenses-and-permissions"></a>Erforderliche Lizenzen und Berechtigungen

- Sie müssen ein globaler, Compliance- oder Exchange Online-Administrator sein, um die in diesem Artikel beschriebenen Aufgaben ausführen zu können. Weitere Informationen über DLP-Berechtigungen finden Sie unter [Berechtigungen](data-loss-prevention-policies.md#permissions).

- Nach allgemeiner Verfügbarkeit werden die EDM-basierten Klassifikation in den folgenden Abonnements berücksichtigt:
    - Office 365 E5
    - Microsoft 365 E5
    - Microsoft 365 Informationsschutz und Compliance
    - Erweiterte Compliance in Office 365

> [!NOTE]
> **Die EDM-basierte Klassifikation ist derzeit in der Vorschau** für [DLP in Office 365](data-loss-prevention-policies.md) (mit Exchange Online und Microsoft Teams) und [Cloud App Security](https://docs.microsoft.com/cloud-app-security). Wenn in Ihrer Organisation [DLP-Funktionen](https://docs.microsoft.com/office365/servicedescriptions/exchange-online-protection-service-description/messaging-policy-and-compliance-servicedesc#data-loss-prevention-dlp) zur Verfügung stehen, können Sie die EDM-basierte Klassifikation ausprobieren. Wenn Sie noch nicht an der Vorschau teilnehmen, wenden Sie sich an [Microsoft](https://resources.office.com/us-landing-spe-contactus.html?LCID=EN-US), um einzusteigen. 

## <a name="the-work-flow-at-a-glance"></a>Der Workflow auf einen Blick

|Phase  |Anforderungen  |
|---------|---------|
|[Teil 1: Einrichten der EDM-basierten Klassifizierung](#part-1-set-up-edm-based-classification)<br/><br/>(je nach Bedarf)<br/>- [Bearbeiten des Datenbankschemas](#editing-the-schema-for-edm-based-classification) <br/>- [Entfernen des Schemas](#removing-the-schema-for-edm-based-classification) |– Lesezugriff auf vertrauliche Daten<br/>– Datenbankschema im XML-Format (Beispiel)<br/>– Regelpaket im XML-Format (Beispiel)<br/>– Administratorberechtigungen für das Security & Compliance Center (mithilfe von PowerShell) |
|[Teil 2: Indizieren und Hochladen vertraulicher Daten](#part-2-index-and-upload-the-sensitive-data)<br/><br/>(je nach Bedarf)<br/>[Aktualisieren der Daten](#refreshing-your-sensitive-information-database) |– Benutzerdefinierte Sicherheitsgruppe und Benutzerkonto<br/>– Lokaler Administratorzugriff auf den Computer mit dem EDM-Upload-Agent<br/>– Lesezugriff auf vertrauliche Daten<br/>– Prozess und Zeitplan für die Datenaktualisierung|
|[Teil 3: Verwenden der EDM-basierten Klassifizierung mit Ihren Microsoft Cloud Services](#part-3-use-edm-based-classification-with-your-microsoft-cloud-services) |– Office 365-Abonnement mit DLP<br/>– EDM-basiertes Klassifizierungsfeature aktiviert (in Vorschau) |

## <a name="part-1-set-up-edm-based-classification"></a>Teil 1: Einrichten der EDM-basierten Klassifizierung

Beim Einrichten und Konfigurieren der EDM-basierten Klassifizierung werden vertrauliche Daten im CSV-Format gespeichert, ein Schema für Ihre Datenbank mit vertraulichen Informationen definiert und ein Regelpaket erstellt. Anschließend werden das Schema und das Regelpaket hochgeladen.

### <a name="define-the-schema-for-your-database-of-sensitive-information"></a>Definieren des Schemas für Ihre Datenbank mit vertraulichen Informationen

1. Identifizieren Sie die vertraulichen Informationen, die Sie verwenden möchten. Exportieren Sie die Daten in eine App, wie z. B. Microsoft Excel, und speichern Sie die Datei im CSV-Format. Die Datendatei kann Folgendes umfassen:

    - Bis zu 10 Millionen Zeilen vertraulicher Daten
    - Bis zu 32 Spalten (Felder) pro Datenquelle

2. Strukturieren Sie die vertraulichen Daten in der CSV-Datei so, dass die erste Zeile die Namen der für die EDM-basierte Klassifizierung verwendeten Felder enthält. Möglicherweise gibt es in Ihrer CSV-Datei Feldnamen, wie z. B. "SSN", "Geburtsdatum", "Vorname", "Nachname" usw. Im Beispiel nennen wir unsere CSV-Datei *PatientRecords.csv*, und die Spalten beinhalten *PatientID*, *MRN*, *lastname*, *FirstName*, *SSN* und mehr.

3. Definieren Sie das Schema für die Datenbank mit vertraulichen Informationen im XML-Format (ähnlich wie in unserem Beispiel unten). Nennen Sie diese Schemadatei `edm.xml` und konfigurieren Sie sie so, dass für jede Spalte in der Datenbank eine Zeile mit der Syntax `<Field name="" unique="" searchable=""/>` verwendet wird. 

    - Verwenden Sie Spaltennamen für *Field name*-Werte.
    - Verwenden Sie *unique="true* für die Felder mit eindeutigen Werten (Sozialversicherungsnummern, Identifikationsnummern usw.), verwenden Sie andernfalls *unique = "false*".
    - Verwenden Sie *searchable = "true* für die Felder, die durchsuchbar sein sollen. Geben Sie nicht mehr als fünf Felder pro Datenbank an, die durchsuchbar sein sollen. Für alle übrigen sollte gelten: *searchable="false"*.  

    Im folgenden Beispiel definiert die XML-Datei das Schema für eine Datenbank mit Patientendatensätzen, wobei fünf Felder als durchsuchbar angegeben werden: *PatientID*, *MRN*, *SSN*, *Phone* und *DOB*. 
    
    (Sie können das Beispiel kopieren, ändern und verwenden.)
    
    ```<?xml version="1.0" encoding="utf-8"?>
    <EdmSchema xmlns="http://schemas.microsoft.com/office/2018/edm">
        <DataStore name="PatientRecords" description="Schema for patient records" version="1">
            <Field name="PatientID" unique="false" searchable="true" />
            <Field name="MRN" unique="false" searchable="true" />
            <Field name="FirstName" unique="false" searchable="false" />
            <Field name="LastName" unique="false" searchable="false" />
            <Field name="SSN" unique="false" searchable="true" />
            <Field name="Phone" unique="false" searchable="true" />
            <Field name="DOB" unique="false" searchable="true" />
            <Field name="Gender" unique="false" searchable="false" />
            <Field name="Address" unique="false" searchable="false" />
        </DataStore>
    </EdmSchema>
    ```

4. [Stellen Sie eine Verbindung mit Office 365 Security & Compliance Center PowerShell her](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

5. Führen Sie die folgenden Cmdlets nacheinander aus, um das Datenbankschema hochzuladen:

    `$edmSchemaXml=Get-Content .\edm.xml -Encoding Byte -ReadCount 0`

    `New-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true`

    Sie werden zu folgenden Bestätigungen aufgefordert:

       Confirm
       Are you sure you want to perform this action?
       New EDM Schema for the data store 'patientrecords' will be imported.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):

    > [!TIP]
    > Wenn Sie möchten, dass Ihre Änderungen ohne Bestätigung durchgeführt werden, verwenden Sie in Schritt 5 stattdessen das folgende Cmdlet: `New-DlpEdmSchema -FileData $edmSchemaXml`
    
Nachdem das Schema für Ihre Datenbank mit vertraulichen Informationen definiert wurde, besteht der nächste Schritt darin, ein Regelpaket einzurichten. Fahren Sie mit dem Abschnitt [Einrichten eines Regelpakets](#set-up-a-rule-package) fort.

#### <a name="editing-the-schema-for-edm-based-classification"></a>Bearbeiten des Schemas für die EDM-basierte Klassifikation 

(Nach Bedarf) Wenn Sie Änderungen an ihrer edm.xml-Datei vornehmen möchten, wenn Sie z. B. ändern möchten, welche Felder für die EDM-basierte Klassifikation verwendet werden, führen Sie die folgenden Schritte aus:

1. Bearbeiten Sie Ihre edm.mxl-Datei. (Dies ist die Datei, die im Abschnitt [Definieren des Schemas](#define-the-schema-for-your-database-of-sensitive-information) in diesem Artikel behandelt wird).

2. [Stellen Sie eine Verbindung mit Office 365 Security & Compliance Center PowerShell her](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

3. Führen Sie die folgenden Cmdlets nacheinander aus, um Ihr Datenbankschema zu aktualisieren:

    `$edmSchemaXml=Get-Content .\edm.xml -Encoding Byte -ReadCount 0`

    `Set-DlpEdmSchema -FileData $edmSchemaXml -Confirm:$true`

    Sie werden zu folgenden Bestätigungen aufgefordert:

       Confirm
       Are you sure you want to perform this action?
       EDM Schema for the data store 'patientrecords' will be updated.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):

    > [!TIP]
    > Wenn Sie möchten, dass Ihre Änderungen ohne Bestätigung durchgeführt werden, verwenden Sie in Schritt 3 stattdessen das folgende Cmdlet: `Set-DlpEdmSchema -FileData $edmSchemaXml`

#### <a name="removing-the-schema-for-edm-based-classification"></a>Entfernen des Schemas für die EDM-basierte Klassifikation

(Nach Bedarf) Wenn Sie das Schema entfernen möchten, das Sie für die EDM-basierte Klassifizierung verwenden, gehen Sie folgendermaßen vor:

1. [Stellen Sie eine Verbindung mit Office 365 Security & Compliance Center PowerShell her](https://docs.microsoft.com/powershell/exchange/office-365-scc/connect-to-scc-powershell/connect-to-scc-powershell?view=exchange-ps).

2. Führen Sie das folgende PowerShell-Cmdlet aus, und ersetzen Sie dabei den Datenspeicherortnamen "patientrecords" durch den Namen, den Sie entfernen möchten:

    `Remove-DlpEdmSchema -Identity patientrecords`

     Sie werden zu folgenden Bestätigungen aufgefordert:
    
       Confirm
       Are you sure you want to perform this action?
       EDM Schema for the data store 'patientrecords' will be removed.
       [Y] Yes  [A] Yes to All  [N] No  [L] No to All  [?] Help (default is "Y"):
    
    > [!TIP]
    > Wenn Sie möchten, dass Ihre Änderungen ohne Bestätigung durchgeführt werden, verwenden Sie in Schritt 2 stattdessen das folgende Cmdlet: `Remove-DlpEdmSchema -Identity patientrecords -Confirm:$false`

### <a name="set-up-a-rule-package"></a>Einrichten eines Regelpakets

1. Erstellen Sie ein Regelpaket im XML-Format (mit Unicode-Codierung), ähnlich wie im folgenden Beispiel. (Sie können das Beispiel kopieren, ändern und verwenden.) 

   Wie Sie im vorherigen Verfahren erfahren haben, wurden im PatientRecords-Schema fünf Felder als durchsuchbar definiert: *PatientID*, *MRN*, *SSN*, *Phone* und *DOB*. In unserem Beispiel für ein Regelpaket sind diese Felder enthalten, und es wird auf die Datenbankschemadatei (edm.xml) verwiesen, wobei ein *ExactMatch*-Element pro durchsuchbarem Feld vorhanden ist. Sehen Sie sich das folgende ExactMatch-Element an:

   ```
    <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
      <Pattern confidenceLevel="65">
        <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
      </Pattern>
    </ExactMatch>
   ```

    Notieren Sie in diesem Beispiel Folgendes:

    - Der dataStore-Name verweist auf die zuvor erstellte CSV-Datei: **dataStore = "PatientRecords"**.
    - Der idMatch-Wert verweist auf ein durchsuchbares Feld, das in der Datenbankschema-Datei aufgelistet ist: **idMatch matches = "SSN"**.
    - Der classification-Wert verweist auf einen vorhandenen oder benutzerdefinierten vertraulichen Informationstyp: **classification = "US-Sozialversicherungsnummer (SSN)"**. (In diesem Fall wird der vorhandene vertrauliche Informationstyp "US-Sozialversicherungsnummer (SSN)" verwendet.)

    Vergewissern Sie sich beim Einrichten des Regelpakets, dass Sie die CSV-Datei und die Datei "edm.xml" korrekt referenzieren. (Sie können das Beispiel kopieren, ändern und verwenden.) 

    ```<?xml version="1.0" encoding="utf-8"?>
    <RulePackage xmlns="http://schemas.microsoft.com/office/2018/edm">
      <RulePack id="fd098e03-1796-41a5-8ab6-198c93c62b11">
        <Version build="0" major="2" minor="0" revision="0" />
        <Publisher id="eb553734-8306-44b4-9ad5-c388ad970528" />
        <Details defaultLangCode="en-us">
          <LocalizedDetails langcode="en-us">
            <PublisherName>IP DLP</PublisherName>
            <Name>Health Care EDM Rulepack</Name>
            <Description>This rule package contains the EDM sensitive type for health care sensitive types.</Description>
          </LocalizedDetails>
        </Details>
      </RulePack>
      <Rules>
        <ExactMatch id = "E1CC861E-3FE9-4A58-82DF-4BD259EAB371" patternsProximity = "300" dataStore ="PatientRecords" recommendedConfidence = "65" >
          <Pattern confidenceLevel="65">
            <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
          </Pattern>
          <Pattern confidenceLevel="75">
            <idMatch matches = "SSN" classification = "U.S. Social Security Number (SSN)" />
            <Any minMatches ="3" maxMatches ="100">
              <match matches="PatientID" />
              <match matches="MRN"/>
              <match matches="FirstName"/>
              <match matches="LastName"/>
              <match matches="Phone"/>
              <match matches="DOB"/>
            </Any>
          </Pattern>
        </ExactMatch>
        <LocalizedStrings>
          <Resource idRef="E1CC861E-3FE9-4A58-82DF-4BD259EAB371">
            <Name default="true" langcode="en-us">Patient SSN Exact Match.</Name>
            <Description default="true" langcode="en-us">EDM Sensitive type for detecting Patient SSN.</Description>
          </Resource>
        </LocalizedStrings>
      </Rules>
    </RulePackage>
    ```
    
2. Laden Sie das Regelpaket herunter, indem Sie nacheinander die folgenden PowerShell-Cmdlets ausführen:

    `$rulepack=Get-Content .\rulepack.xml -Encoding Byte -ReadCount 0`

    `New-DlpSensitiveInformationTypeRulePackage -FileData $rulepack`

Sie haben die EDM-basierte Klassifizierung nun eingerichtet. Im nächsten Schritt werden die vertraulichen Daten indiziert und dann die indizierten Daten hochgeladen. 

## <a name="part-2-index-and-upload-the-sensitive-data"></a>Teil 2: Indizieren und Hochladen vertraulicher Daten

In dieser Phase richten Sie eine benutzerdefinierte Sicherheitsgruppe, ein Benutzerkonto und das Tool EDM-Upload-Agent ein. Dann verwenden Sie das Tool, um die vertraulichen Daten zu indizieren und die indizierten Daten hochzuladen.

### <a name="set-up-the-security-group-and-user-account"></a>Einrichten der Sicherheitsgruppe und des Benutzerkontos

1. Wechseln Sie als globaler Administrator zum Admin Center ([https://admin.microsoft.com](https://admin.microsoft.com)) und [erstellen Sie eine Sicherheitsgruppe](https://docs.microsoft.com/office365/admin/email/create-edit-or-delete-a-security-group?view=o365-worldwide) namens `EDM_DataUploaders`. 

2. Fügen Sie einen oder mehrere Benutzer zu der *EDM_DataUploaders*-Sicherheitsgruppe hinzu. (Diese Benutzer verwalten die Datenbank mit vertraulichen Informationen.)

3. Stellen Sie sicher, dass jeder Benutzer, der die vertraulichen Daten verwaltet, ein lokaler Administrator auf dem Computer ist, der für den EDM-Upload-Agent verwendet wird.

### <a name="set-up-the-edm-upload-agent"></a>Einrichten des EDM-Upload-Agenten

> [!NOTE]
> Bevor Sie mit diesem Verfahren beginnen, stellen Sie sicher, dass Sie ein Mitglied der Sicherheitsgruppe *EDM_DataUploaders* und ein lokaler Administrator auf Ihrem Computer sind.

1. Laden Sie den EDM-Upload-Agent unter [https://go.microsoft.com/fwlink/?linkid=2088639](https://go.microsoft.com/fwlink/?linkid=2088639) herunter und installieren Sie ihn. Standardmäßig lautet der Installationsspeicherort `C:\Program Files\Microsoft\EdmUploadAgent`. 

2. Wenn Sie den EDM-Upload-Agent autorisieren möchten, öffnen Sie die Windows-Eingabeaufforderung (als Administrator), und führen Sie dann den folgenden Befehl aus:

    `EdmUploadAgent.exe /Authorize`

3. Melden Sie sich mit Ihrem Office 365-Geschäfts-, Schul- oder Unikonto an.

Im nächsten Schritt verwenden Sie den EDM-Upload-Agent, um die vertraulichen Daten zu indizieren und dann die indizierten Daten hochzuladen.

### <a name="index-and-upload-the-sensitive-data"></a>Indizieren und Hochladen vertraulicher Daten

1. Speichern Sie die Datei mit den vertraulichen Daten (unser Beispiel ist *PatientRecords.csv*) auf dem lokalen Laufwerk Ihres Computers. (Wir haben unser Beispiel *PatientRecords.csv* auf `C:\Edm\Data` gespeichert.)

2. Um die vertraulichen Daten zu indizieren, führen Sie den folgenden Befehl in der Windows-Eingabeaufforderung aus:

    `EdmUploadAgent.exe /CreateHash /DataStoreName <DataStoreName> /DataFile <DataFilePath> /HashLocation <HashedFileLocation>`

    Beispiel: **EdmUploadAgent.exe /CreateHash /DataStoreName PatientRecords /DataFile C:\Edm\Data\PatientRecords.csv /HashLocation C:\Edm\Hash** 

3. Um die vertraulichen Daten hochzuladen, führen Sie den folgenden Befehl in der Windows-Eingabeaufforderung aus:

    `EdmUploadAgent.exe /UploadHash /DataStoreName <DataStoreName> /HashFile <HashedSourceFilePath>`

    Beispiel: **EdmUploadAgent.exe /UploadHash /DataStoreName PatientRecords /HashFile C:\Edm\Hash\PatientRecords.EdmHash** 

4. Um zu überprüfen, ob Ihre vertraulichen Daten hochgeladen wurden, führen Sie den folgenden Befehl in der Windows-Eingabeaufforderung aus:

    `EdmUploadAgent.exe /GetDataStore`

    Sie sehen eine Liste der Datenspeicher mit dem Zeitpunkt der letzten Aktualisierung, die der folgenden Liste ähnelt: <br/>![Beispiel für das GetDataStore-Cmdlet und die Ergebnisse](media/EDM-GetDataStore-example.png)

5. Fahren Sie mit dem Einrichten des Prozesses und des Zeitplans für [Aktualisieren der Datenbank für vertrauliche Informationen](#refreshing-your-sensitive-information-database) fort.

Sie können nun die EDM-basierte Klassifikation mit Ihren Microsoft Cloud Services verwenden. Sie können beispielsweise [eine DLP-Richtlinie mithilfe der EDM-basierten Klassifizierung](#to-create-a-dlp-policy-with-edm) einrichten. 

### <a name="refreshing-your-sensitive-information-database"></a>Aktualisieren der Datenbank für vertrauliche Informationen

Sie können Ihre Datenbank für vertrauliche Informationen täglich oder wöchentlich aktualisieren, und das EDM-Upload-Tool kann die vertraulichen Daten neu indizieren und dann die indizierten Daten erneut hochladen. 

1. Ermitteln Sie den Vorgang und die Häufigkeit (täglich oder wöchentlich) zum Aktualisieren der Datenbank mit vertraulichen Informationen.

2. Exportieren Sie die vertraulichen Daten erneut in eine App, wie z. B. Microsoft Excel, und speichern Sie die Datei im CSV-Format. Behalten Sie den Dateinamen und den Speicherort bei, den Sie beim Ausführen der unter [Indizieren und Hochladen vertraulicher Daten](#index-and-upload-the-sensitive-data) beschriebenen Schritte verwendet haben.

    > [!NOTE]
    > Wenn es keine Änderungen an der Struktur (Feldnamen) der CSV-Datei gibt, müssen Sie keine Änderungen an der Datenbankschemadatei vornehmen, wenn Sie die Daten aktualisieren. Wenn Sie jedoch Änderungen vornehmen müssen, stellen Sie sicher, dass Sie das [Datenbankschema](#editing-the-schema-for-edm-based-classification) und Ihr [Regelpaket](#set-up-a-rule-package) entsprechend bearbeiten.        

3. Verwenden Sie die [Aufgabenplanung](https://docs.microsoft.com/windows/desktop/TaskSchd/task-scheduler-start-page), um die Schritte 2 und 3 im Verfahren [Indexieren und Hochladen vertraulicher Daten](#index-and-upload-the-sensitive-data) zu automatisieren. Sie können Aufgaben mithilfe verschiedener Methoden planen:
    
    |Methode  |Vorgehensweise  |
    |---------|---------|
    |Windows PowerShell     |Siehe Dokumentation [Aufgabenplanung](https://docs.microsoft.com/powershell/module/scheduledtasks/?view=win10-ps) und [Beispiel PowerShell-Skript](#example-powershell-script-for-task-scheduler) in diesem Artikel|
    |Aufgabenplaner-API |Siehe Dokumentation [Aufgabenplaner](https://docs.microsoft.com/windows/desktop/TaskSchd/using-the-task-scheduler) |
    |Windows-Benutzeroberfläche     |Klicken Sie in Windows auf **Start** und geben Sie `Task Scheduler` ein. Klicken Sie dann in der Ergebnisliste mit der rechten Maustaste auf **Aufgabenplaner** und wählen Sie **Als Administrator ausführen**.          |

#### <a name="example-powershell-script-for-task-scheduler"></a>Beispiel: PowerShell-Skript für den Aufgabenplaner

Dieser Abschnitt enthält ein Beispiel für ein PowerShell-Skript, das Sie verwenden können, um Ihre Aufgaben zum Indizieren von Daten und Hochladen der indizierten Daten zu planen:

```powershell
param([string]$dataStoreName,[string]$fileLocation)
# Assuming current user is also the user context to run the task
$user = "$env:USERDOMAIN\$env:USERNAME"
$edminstallpath = 'C:\Program Files\Microsoft\EdmUploadAgent\'
$edmuploader = $edminstallpath + 'EdmUploadAgent.exe'
$csvext = '.csv'
$edmext = '.EdmHash'
# Assuming CSV file name is same as data store name
$dataFile = "$fileLocation\$dataStoreName$csvext"
$hashFile = "$fileLocation\$dataStoreName$edmext"
# Assuming location to store hash file is same as the location of csv file
$hashLocation = $fileLocation
$createHashArgs = '/CreateHash /DataStoreName ' + $dataStoreName + ' /DataFile ' + $dataFile + ' /HashLocation ' + $hashLocation
$uploadHashArgs = '/UploadHash /DataStoreName ' + $dataStoreName + ' /HashFile ' + $hashFile
# Set up actions associated with the task
$actions = @()
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $createHashArgs -WorkingDirectory $edminstallpath
$actions += New-ScheduledTaskAction -Execute $edmuploader -Argument $uploadHashArgs -WorkingDirectory $edminstallpath
# Set up trigger for the task
$trigger = New-ScheduledTaskTrigger -Weekly -DaysOfWeek Sunday -At 2am
# Set up task settings
$principal = New-ScheduledTaskPrincipal -UserId $user -LogonType S4U -RunLevel Highest
$settings = New-ScheduledTaskSettingsSet -RunOnlyIfNetworkAvailable -StartWhenAvailable -WakeToRun
# Create the scheduled task
$scheduledTask = New-ScheduledTask -Action $actions -Principal $principal -Trigger $trigger -Settings $settings
# Get credentials to run the task
$creds = Get-Credential -UserName $user -Message "Enter credentials to run the task"
$password=[Runtime.InteropServices.Marshal]::PtrToStringAuto([Runtime.InteropServices.Marshal]::SecureStringToBSTR($creds.Password))
# Register the scheduled task
$taskName = 'EDMUpload_' + $dataStoreName
Register-ScheduledTask -TaskName $taskName -InputObject $scheduledTask -User $user -Password $password
```
## <a name="part-3-use-edm-based-classification-with-your-microsoft-cloud-services"></a>Teil 3: Verwenden der EDM-basierten Klassifizierung mit Ihren Microsoft Cloud Services

Sie können die EDM-basierte Klassifikation mit Informationsschutzfunktionen verwenden, wie z. B. [Office 365 DLP-Richtlinien](data-loss-prevention-policies.md) und [Microsoft Cloud App Security-Dateirichtlinien](https://docs.microsoft.com/cloud-app-security/data-protection-policies). Das folgende Verfahren beschreibt, wie EDM mit einer DLP-Richtlinie verwendet wird, die im Office 365 Security & Compliance Center erstellt wird.

### <a name="to-create-a-dlp-policy-with-edm"></a>Erstellen einer DLP-Richtlinie mit EDM

1. Wechseln Sie zum Security & Compliance Center ([https://protection.office.com](https://protection.office.com)).

2. Klicken Sie auf die **Verhinderung von Datenverlust-** > **Richtlinie**.

3. Wählen Sie **Richtlinie erstellen** > **Benutzerdefiniert** > **Weiter**.

4. Geben Sie auf der Registerkarte **Richtlinie benennen** einen Namen und eine Beschreibung ein und wählen Sie dann **Weiter**.

5. Wählen Sie auf der Registerkarte **Speicherorte auswählen** **Bestimmte Speicherorte auswählen** und wählen Sie dann **Weiter**.<br/>![Option Speicherorte auswählen](media/DLP-EDM-newpolicy-chooselocations.png)<br/>

6. Wählen Sie in der Spalte **Status** **Nur Exchange-E-Mail** und wählen Sie dann **Weiter**. <br/>![EDM-Richtlinie nur mit Exchange](media/EDM-DLPpolicy-ExchangeOnly.png)<br/>

7. Wählen Sie auf der Registerkarte **Richtlinieneinstellungen** **Erweiterte Einstellungen verwenden** und dann **Weiter**.<br/>![Erweiterte Einstellungen verwenden](media/edm-dlp-policy-advancedsettings.png)<br/>

8. Wählen Sie **+ Neue Regel** aus.<br/>![Erstellen einer Regel](media/edm-dlp-newrule.png)<br/>

9. Geben Sie im Abschnitt **Name** einen Namen und eine Beschreibung für die Regel ein.<br/>![Neue Regel-Felder](media/edm-dlp-newruleform.png)<br/>

10. Wählen Sie im Abschnitt **Bedingungen** in der Liste **+ Bedingung hinzufügen** **Inhalt enthält vertraulichen Typ**.<br/>![Inhalt enthält vertrauliche Informationstypen](media/edm-dlp-newrule-conditions.png)<br/>

11. Suchen Sie den vertraulichen Informationstyp, den Sie beim Einrichten Ihres Regelpakets erstellt haben, und wählen Sie dann **+ Hinzufügen**.<br/>![Vertraulichen Informationstyp finden](media/edm-dlp-newrulefindsensitiverulepack.png)<br/>Wählen Sie dann **Fertig**.

12. Wählen Sie Optionen für die Regel aus, wie z. B. **Benutzerbenachrichtigungen**, **Benutzeraußerkraftsetzungen**, **Schadensberichte** usw., und wählen Sie dann **Speichern**.

13. Überprüfen Sie auf der Registerkarte die **Richtlinieneinstellungen**, überprüfen Sie Ihre Regeln und wählen Sie dann **Weiter**.

14. Geben Sie an, ob Sie die Richtlinie sofort aktivieren, sie testen oder deaktivieren möchten. Wählen Sie dann **Weiter** aus.

15. Überprüfen Sie auf der Registerkarte **Überprüfen Sie Ihre Einstellungen** Ihre Richtlinie. Nehmen Sie alle erforderlichen Änderungen vor. Wenn Sie fertig sind, wählen Sie **Erstellen** aus.

    > [!NOTE]
    > Es kann ungefähr eine Stunde dauern, bis Ihre neue DLP-Richtlinie im Rechenzentrum erscheint.

## <a name="related-articles"></a>Verwandte Artikel

[Integrierte vertrauliche Informationstypen und wonach diese suchen](what-the-sensitive-information-types-look-for.md)

[Benutzerdefinierte vertrauliche Informationstypen](custom-sensitive-info-types.md)

[Überblick über DLP-Richtlinien](data-loss-prevention-policies.md)

[Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security)
