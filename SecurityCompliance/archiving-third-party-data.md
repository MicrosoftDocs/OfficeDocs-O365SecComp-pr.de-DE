---
title: Archivieren von Drittanbieter-Daten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid: MOE150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Administratoren können drittanbieterdaten aus sozialen Medienplattformen, Instant Messaging-Plattformen und Dokument Zusammenarbeits Plattformen in Postfächer in Ihrer Office 365-Organisation importieren. Auf diese Weise können Sie Daten aus Facebook, Twitter und Datenquellen in Office 365 archivieren. Anschließend können Sie Office 365-Kompatibilitätsfeatures (wie rechtliche Aufbewahrung, Inhaltssuche und Aufbewahrungsrichtlinien) an drittanbieterdaten appply.
ms.openlocfilehash: 37811fdbee52cf956c6371deea53a242c2a3c550
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218495"
---
# <a name="archiving-third-party-data-in-office-365"></a>Archivieren von Drittanbieter-Daten in Office 365

Office 365 ermöglicht Administratoren das Importieren und Archivieren von drittanbieterdaten von sozialen Medienplattformen, Instant Messaging-Plattformen und Dokument Zusammenarbeits Plattformen zu Postfächern in Ihrer Office 365-Organisation. Beispiele für Drittanbieter-Datenquellen, die Sie in Office 365 importieren können, sind folgende: 
  
- **Social** -Twitter, Facebook, jammern und LinkedIn 
    
- **Instant Messaging** -Yahoo Messenger, GoogleTalk und Cisco Jabber 
    
- **Dokument Zusammenarbeit** und Dropbox 
    
- **Vertikale Branchen** – Customer Relationship Management (wie Salesforce Chatter) und Financials (wie Thomson Reuters und Bloomberg) 
    
- **SMS/Textnachrichten** -BlackBerry 
    
Nachdem drittanbieterdaten importiert wurden, können Sie die Office 365-Compliance-Funktionen wie das Aufheben von Rechtsstreitigkeiten, Inhaltssuche, in-situ-Archivierung,-Überwachung und Office 365-Aufbewahrungsrichtlinien auf diese Daten anwenden. Wenn beispielsweise ein Postfach in den Rechtsstreit versetzt wird, werden Daten von Drittanbietern beibehalten. Mithilfe der Inhaltssuche können Sie drittanbieterdaten durchsuchen. Sie können auch Archivierungs-und Aufbewahrungsrichtlinien auf drittanbieterdaten anwenden, genau wie für Microsoft-Daten. Kurz gesagt, die Archivierung von drittanbieterdaten in Office 365 kann dazu beitragen, dass Ihre Organisation mit behördlichen und behördlichen Richtlinien kompatibel bleibt.
  
Im folgenden finden Sie eine Übersicht über den Prozess und die erforderlichen Schritte zum Importieren von drittanbieterdaten in Office 365.

[Schritt 1: Partner für Drittanbieterdaten suchen](#step-1-find-a-third-party-data-partner)

[Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren](#step-3-configure-user-mailboxes-for-third-party-data)

[Schritt 4: Bereitstellen von Informationen für Ihren Partner](#step-4-provide-your-partner-with-information)

[Schritt 5: Registrieren des Drittanbieter-Daten-Konnektors in Azure Active Directory](#step-5-register-the-third-party-data-connector-in-azure-active-directory)

## <a name="how-the-third-party-data-import-process-works"></a>Works> des Drittanbieters für den Datenimport

Die folgende Abbildung und die Beschreibung erläutern, wie der Prozess zum Importieren von Drittanbieterdaten funktioniert.
  
![So funktioniert der Prozess zum Importieren von Drittanbieterdaten](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. Der Kunde arbeitet mit seinem bevorzugten Partner zusammen, um einen Connector zu konfigurieren, der Elemente aus der Drittanbieter-Datenquelle extrahiert und diese Elemente dann in Office 365 importiert.
    
2. Der Partner-Connector stellt über eine Drittanbieter-API (auf einer festgelegten oder konfigurierten Basis) eine Verbindung zu drittanbieterdaten Quellen her und extrahiert Elemente aus der Datenquelle. Der Partner-Konnektor wandelt den Inhalt eines Elements in ein e-Mail-Nachrichtenformat um. Im Abschnitt [Weitere Informationen](#more-information) finden Sie eine Beschreibung des Nachrichtenformat Schemas. 
    
3. Der Partner-Connector stellt mithilfe des Exchange-webDiensts (EWS) über einen bekannten Endpunkt eine Verbindung mit dem Azure-Dienst in Office 365 her.
    
4. Elemente werden in das Postfach eines bestimmten Benutzers oder in ein spezielles Postfach zur Aufnahme aller Drittanbieterdaten importiert. Ob ein Element in das Postfach eines bestimmten Benutzers oder in das Postfach für Drittanbieterdaten importiert wird, basiert auf den folgenden Kriterien:
    
    a. **Elemente mit einer Benutzer-ID, die einem office 365-Benutzerkonto entspricht** – wenn der Partner-Konnektor die Benutzer-ID des Elements in der Drittanbieter-Datenquelle einer bestimmten Benutzer-ID in Office 365 zuordnen kann, wird das Element in **** den Ordner "purges" des Benutzers Ordner "Wiederherstellbare Elemente". Benutzer können nicht auf Elemente im Ordner "Purge" zugreifen. Sie können jedoch Office 365 eDiscovery-Tools verwenden, um im Ordner "Purges" nach Elementen zu suchen.
    
    b. **Elemente, die nicht über eine Benutzer-ID verfügen, die einem office 365-Benutzerkonto entspricht** – wenn der Partner-Konnektor die Benutzer-ID eines Elements nicht einer bestimmten Benutzer-ID in Office 365 zuordnen kann, wird das Element in den Ordner " **Posteingang** " des Drittanbieter-Daten Postfachs kopiert. Durch das Importieren von Elementen in den Posteingang können Sie oder eine Person in Ihrer Organisation sich beim Drittanbieter Postfach anmelden, um diese Elemente anzuzeigen und zu verwalten, und feststellen, ob Anpassungen in der Konfiguration des Partner-Connectors vorgenommen werden müssen.
 
## <a name="step-1-find-a-third-party-data-partner"></a>Schritt 1: Partner für Drittanbieterdaten suchen

Eine wichtige Komponente für die Archivierung von drittanbieterdaten in Office 365 ist die Suche und Zusammenarbeit mit einem Microsoft-Partner, der sich auf die Erfassung von Daten aus einer Drittanbieter-Datenquelle und deren Import in Office 365 spezialisiert hat. Nachdem die Daten importiert wurden, können Sie zusammen mit den anderen Microsoft-Daten Ihrer Organisation archiviert und aufbewahrt werden, wie beispielsweise e-Mails von Exchange und Dokumenten aus SharePoint und OneDrive for Business. Ein Partner erstellt einen Connector, der Daten aus drittanbieterdaten Quellen Ihrer Organisation extrahiert (beispielsweise BlackBerry, Facebook, Google +, Thomson Reuters, Twitter und YouTube) und übergibt diese Daten an eine Office 365-API, die Elemente in Exchange-Postfächer als e-Mail-Nachrichten. 
  
In den folgenden Abschnitten werden die Microsoft-Partner und die von Ihnen unterstützten Drittanbieter-Datenquellen aufgeführt, die am Programm zur Archivierung von drittanbieterdaten in Office 365 teilnehmen.

[17a-4 LLC](#17a-4-llc)
  
[Actiance](#actiance)
  
[ArchiveSocial](#archivesocial)
  
[Globanet](#globanet)
  
[OpenText](#opentext)
  
[Verba](#verba)
  
### <a name="17a-4-llc"></a>17a-4 LLC

17a-4 LLC unterstützt die folgenden Drittanbieter-Datenquellen:
  
- BlackBerry
    
- Bloomberg Data Streams
    
- Cisco Jabber
    
- FactSet
    
- HipChat
    
- InvestEdge
    
- Schwätzchen
    
- 
MessageLabs Data Streams

    
- OpenText
    
- Live-Hilfe für Oracle/ATG 'click-to-call'

    
- Pivot IMTRADER

    
- Microsoft SharePoint
    
- MindAlign
    
- Sitrion One (Newsgator)
    
- 
Skype for Business (Lync/OCS)
    
- 
Skype for Business Online (Lync Online)

    
- SQL-Datenbanken
    
- 
Squawker

    
- Thomson Reuters Eikon Messenger

  
### <a name="actiance"></a>Actiance

[Actiance](https://www.actiance.com) unterstützt die folgenden drittanbieterdaten Quellen: 
  
- AIM
    
- American Idol
    
- Apple Juice
    
- 
AOL mit Pivot-Client

    
- Ares
    
- Bazaar Voice
    
- Bear Share
    
- Bit Torrent
    
- BlackBerry-Anrufprotokolle (v5, v10, v12)

    
- BlackBerry Messenger (v5, v10, v12)
    
- BlackBerry PIN (v5, v10, v12)
    
- BlackBerry SMS (v5, v10, v12)
    
- Bloomberg Mail

    
- CellTrust
    
- Chat Import

    
- Echtzeitprotokollierung und -richtinie für Chat

    
- Chatter

    
- Cisco IM &amp; Presence Server (v 9.0.1, v 9.1, v 9.1.1 SU1, V10, v 10.5.1 SU1)
    
- Cisco Unified Presence Server (v8.6.3, v8.6.4, v8.6.5)

    
- Collaboration Import

    
- Echtzeitprotokollierung für Zusammenarbeit

    
- Direct Connect
    
- Facebook
    
- FactSet
    
- FastTrack
    
- Gnutella
    
- Google+

    
- GoToMyPC
    
- Hopster
    
- HubConnex
    
- IBM Connections (v3.0.1, v4.0, v4.5, v4.5 CR3, v5)

    
- IBM Connections Chat Cloud

    
- IBM Connections Social Cloud

    
- IBM SameTime Advanced 8.5.2 IFR1

    
- IBM SameTime Communicate 9.0

    
- IBM SameTime Community (v8.0.2, v8.5.1 IFR2, v8.5.2 IFR1, v9.1)

    
- IBM SameTime Complete 9.0

    
- IBM SameTime Conference 9.0

    
- IBM SameTime Meeting 8.5.2 IFR1

    
- ICE/YellowJacket
    
- Chat-Import

    
- Echtzeitprotokollierung und -richtinie für Chat

    
- Indii Messenger

    
- Instant Bloomberg

    
- IRC
    
- Jive

    
- Jive 6 Real Time Logging (v6, v7)

    
- Jive Import
    
- JXTA
    
- LinkedIn
    
- 
Microsoft Lync (2010, 2013)

    
- MFTP
    
- Microsoft Lync 2013 Voice

    
- Microsoft SharePoint (2010, 2013)

    
- Microsoft SharePoint Online
    
- Microsoft UC (Unified Communications)
    
- MindAlign
    
- Mobile Guard
    
- MSN
    
- My Space
    
- NEONetwork
    
- Office 365 Lync Dedicated

    
- Office 365 Shared IM

    
- Pinterest
    
- Pivot
    
- QQ
    
- Skype for Business 2015
    
- SoftEther
    
- Symphony

    
- Thomson Reuters Eikon

    
- Thomson Reuters Messenger

    
- Tor
    
- TTT
    
- Twitter
    
- WinMX
    
- Winny
    
- Yahoo

    
- Yammer
    
- YouTube
    
  
### <a name="archivesocial"></a>ArchiveSocial

[ArchiveSocial](https://www.archivesocial.com) unterstützt die folgenden drittanbieterdaten Quellen: 
  
- Facebook
    
- Flickr

    
- Instagram

    
- LinkedIn
    
- Pinterest
    
- Twitter
    
- YouTube
    
- Vimeo
  
### <a name="globanet"></a>Globanet

[Globanet](https://www.globanet.com) unterstützt die folgenden drittanbieterdaten Quellen: 
  
- AOL mit Pivot-Client
 
    
- BlackBerry-Anrufprotokolle (v5, v10, v12)

    
- BlackBerry Messenger (v5, v10, v12)
    
- BlackBerry PIN (v5, v10, v12)
    
- BlackBerry SMS (v5, v10, v12)
    
- Bloomberg Chat

    
- Bloomberg Mail

    
- Box
    
- CipherCloud for Salesforce Chatter
    
- Cisco IM &amp; Presence Server (v10, v 10.5.1 SU1, v 11.0, v 11.5 SU2)

- Cisco WebEx-Teams

- Freigabe für &amp; Citrix Arbeitsbereich

- CrowdCompass

- Durch Trennzeichen getrennte, benutzerdefinierte Textdateien

    
- Benutzerdefinierte XML-Dateien

    
- Facebook (Seiten)
    
- Factset

    
- FXConnect
    
- ICE Chat/YellowJacket
    
- Jive

    
- Macgregor XIP


- Microsoft Exchange Server
    
- Microsoft OneDrive for Business

- Microsoft Teams
       
- Microsoft Yammer

    
- Mobile Guard
    
- Pivot
    
- Salesforce Chatter

- Skype for Business Online
    
- Skype for Business, Versionen 2007 R2 - 2016 (lokal)

    
- Slack Enterprise Grid
    
- Symphony

    
- Thomson Reuters Eikon

    
- Thomson Reuters Messenger

    
- Thomson Reuters Dealings 3000 / FX Trading

    
- Twitter
    
- UBS Chat

    
- YouTube
  
### <a name="opentext"></a>OpenText

[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) unterstützt die folgenden drittanbieterdaten Quellen: 
  
- Axs Encrypted
    
- Axs Exchange
    
- Axs Local Archive
    
- Axs PlaceHolder
    
- Axs Signed
    
- Bloomberg
    
- Thomson Reuters
  
### <a name="verba"></a>Verba

[Verba](https://www.verba.com) unterstützt die folgenden drittanbieterdaten Quellen: 
  
- Avaya Aura Video

    
- Avaya Aura Voice

    
- Avtec Radio

    
- Bosch/Telex Radio

    
- BroadSoft Video

    
- BroadSoft Voice

    
- Centile Voice

    
- Chatnachricht in Cisco Jabber
    
- Cisco UC Video

    
- Cisco UC Voice

    
- Cisco UCCX/UCCE Video
    
- Cisco UCCX/UCCE Voice
    
- ESChat Radio
    
- Geoman Contact Expert
    
- IP Trade Voice

    
- Luware LUCS Contact Center
    
- Microsoft UC (Unified Communications)
    
- Mitel MiContact Center for Lync (prairieFyre) 

    
- Oracle/Acme Packet Session Border Controller Video  

    
- Oracle/Acme Packet Session Border Controller Voice

    
- Singtel Mobile Voice

    
- SIPREC Video
    
-  SIPREC Voice 
    
- Chatnachricht in Skype for Business/Lync

    
- Skype for Business/Lync Video

    
- Skype for Business/Lync Voice

    
- Speakerbus Voice

    
- Standard SIP/H.323 Video 

    
- Standard SIP/H.323 Voice 

    
- Truphone Voice

    
- TwistedPair Radio

    
- Windows Desktop-Computerbildschirm 

  
## <a name="step-2-create-and-configure-a-third-party-data-mailbox-in-office-365"></a>Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren

Hier finden Sie die Schritte zum Erstellen und Konfigurieren eines Drittanbieter-Daten Postfachs zum Importieren von Daten in Office 365. Wie bereits erläutert, werden Elemente in dieses Postfach importiert, wenn der Partner-Konnektor die Benutzer-ID des Elements nicht einem Office 365-Benutzerkonto zuordnen kann.
  
 **Führen Sie diese Aufgaben im Office 365 Admin Center aus.**
  
1. Erstellen Sie ein neues Benutzerkonto in Office 365, und weisen Sie ihm eine Exchange Online-Plan 2-Lizenz zu. Weitere Informationen finden Sie unter [Hinzufügen von Benutzern zu Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). Eine Plan 2-Lizenz ist erforderlich, um für das Postfach ein aufbewahrungsVerfahren durchzuführen oder ein Archivpostfach mit einem unbegrenzten Speicherkontingent zu aktivieren.
    
2. Fügen Sie das Benutzerkonto für das Drittanbieter-Daten Postfach der **Exchange-Administrator** Rolle in Office 365 hinzu. Weitere Informationen finden Sie unter [Zuweisen von Administratorrollen in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).
    
    > [!TIP]
    > Notieren Sie die Anmeldeinformationen für dieses Benutzerkonto. Sie müssen diese für Ihren Partner bereitstellen, wie in Schritt 4 beschrieben. 
  
 **Ausführen dieser Aufgaben im Exchange Admin Center**
  
1. Ausblenden des Drittanbieter-Daten Postfachs aus dem Adressbuch und anderen Adresslisten in Ihrer Organisation; Weitere Informationen finden Sie unter [Verwalten von Benutzerpostfächern](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternativ können Sie den folgenden PowerShell-Befehl ausführen:
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. Weisen Sie dem Drittanbieter-Daten Postfach die Berechtigung **FullAccess** zu, damit Administratoren oder Compliance Officers das Drittanbieter-Daten Postfach im Outlook-Desktop Client öffnen können. Weitere Informationen finden Sie unter [Manage Permissions for Recipients](https://go.microsoft.com/fwlink/p/?LinkId=692104).
    
3. Aktivieren Sie die folgenden kompatibilitätsbezogenen Office 365-Features für das Drittanbieter-Daten Postfach:
    
    - Aktivieren Sie das Archivpostfach. Weitere Informationen finden Sie unter [Aktivieren von archivpostfächern im office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) und Aktivieren der unlimitierten [Archivierung in Office 365](enable-unlimited-archiving.md). Auf diese Weise können Sie Speicherplatz im primären Postfach freigeben, indem Sie eine Archivrichtlinie einrichten, mit der Drittanbieter-Datenelemente in das Archivpostfach verschoben werden. Dadurch erhalten Sie unbegrenzten Speicherplatz für drittanbieterdaten.
    
    - Platzieren Sie das Drittanbieter-Daten Postfach in einem Rechtsstreit. Sie können auch eine Office 365-Aufbewahrungsrichtlinie im Office 365 Security &amp; Compliance Center anwenden. Wenn Sie dieses Postfach anhalten, werden Datenelemente von Drittanbietern (auf unbestimmte Zeit oder für eine bestimmte Dauer) aufbewahrt und verhindert, dass Sie aus dem Postfach gelöscht werden. Lesen Sie eines der folgenden Themen:
    
      - [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [Übersicht über Aufbewahrungsrichtlinien in Office 365](retention-policies.md)
    
       
    
    - Aktivieren der postfachüberwachungsprotokollierung für Besitzer-, Stellvertreter-und Administratorzugriff auf das Drittanbieter-Daten Postfach Weitere Informationen finden Sie unter [Aktivieren der postfachüberwachung in Office 365](enable-mailbox-auditing.md). Auf diese Weise können Sie alle Aktivitäten überwachen, die von jedem Benutzer ausgeführt werden, der Zugriff auf das Drittanbieter-Daten Postfach hat.

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a>Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren

Im nächsten Schritt werden Benutzerpostfächer für die Unterstützung von drittanbieterdaten konfiguriert. Führen Sie diese Aufgaben mithilfe der Exchange-Verwaltungskonsole oder mithilfe der entsprechenden Windows PowerShell-Cmdlets aus.
  
1. Aktivieren Sie das Archivpostfach für jeden Benutzer; Weitere Informationen finden Sie unter [Aktivieren von archivpostfächern im office 365 Security &amp; Compliance Center](enable-archive-mailboxes.md) und Aktivieren der unlimitierten [Archivierung in Office 365](enable-unlimited-archiving.md).
    
2. Platzieren von Benutzerpostfächern für die Aufbewahrung von Rechtsstreitigkeiten oder Anwenden einer Office 365-Archivierungsrichtlinie Lesen Sie eines der folgenden Themen: 
    
    - [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [Übersicht über Aufbewahrungsrichtlinien in Office 365](retention-policies.md)
    
    Wie bereits weiter oben erwähnt, können Sie beim Aktivieren des Beweissicherungsverfahrens für Postfächer festlegen, wie lange Elemente aus einer Drittanbieter-Datenquelle aufbewahrt werden sollen. Sie können auch festlegen, dass sie dauerhaft aufbewahrt werden sollen.

## <a name="step-4-provide-your-partner-with-information"></a>Schritt 4: Bereitstellen von Informationen für Ihren Partner

Im letzten Schritt müssen Sie dem Partner die folgenden Informationen bereitstellen, damit er den Connector für die Verbindung mit Office 365-Organisation konfigurieren kann, um Daten in Benutzerpostfächer und das Drittanbieterdaten-Postfach zu importieren. 
  
- Der Endpunkt, der zum Herstellen einer Verbindung mit dem Azure-Dienst in Office 365 verwendet wird:

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- Die Anmeldeinformationen (Office 365-Benutzer-ID und Kennwort) des Drittanbieter-Daten Postfachs, das Sie in Schritt 2 erstellt haben. Diese Anmeldeinformationen sind erforderlich, damit der Partner-Connector auf Elemente zugreifen und diese in Benutzerpostfächer und das Drittanbieter-Daten Postfach importieren kann.
 
## <a name="step-5-register-the-third-party-data-connector-in-azure-active-directory"></a>Schritt 5: Registrieren des Drittanbieter-Daten-Konnektors in Azure Active Directory

Ab dem 30. September 2018 beginnt der Azure-Dienst in Office 365 mit der Verwendung der modernen Authentifizierung in Exchange Online, um Drittanbieter-Datenkonnektoren zu authentifizieren, die versuchen, eine Verbindung mit Ihrer Office 365-Organisation herzustellen, um Daten zu importieren. Der Grund für diese Änderung besteht darin, dass die moderne Authentifizierung mehr Sicherheit bietet als die aktuelle Methode, die auf dem Whitelisting von Drittanbieter-Connectors basiert, die den zuvor beschriebenen Endpunkt zum Herstellen einer Verbindung mit dem Azure-Dienst verwenden.

Damit ein Drittanbieter-Datenkonnektor mit der neuen modernen Authentifizierungsmethode eine Verbindung mit Office 365 herstellen kann, muss ein Administrator in Ihrer Office 365-Organisation mit der Registrierung des Connectors als vertrauenswürdige Dienstanwendung in Azure Active Directory einverstanden sein. Hierzu wird eine Berechtigungsanforderung akzeptiert, damit der Connector auf die Daten Ihrer Organisation in Azure Active Directory zugreifen kann. Nachdem Sie diese Anforderung angenommen haben, wird der Drittanbieter-Datenkonnektor als Unternehmensanwendung zu Azure Active Directory hinzugefügt und als Dienstprinzipal dargestellt. Weitere Informationen zum Zustimmungsprozess finden Sie unter [mandantEnadministrator-Einwilligung](https://docs.microsoft.com/en-us/skype-sdk/trusted-application-api/docs/tenantadminconsent).

Hier sind die Schritte zum Zugreifen auf und akzeptieren der Anforderung zur Registrierung des Connectors:

1. Wechseln Sie zu [dieser Seite](https://login.microsoftonline.com/common/oauth2/authorize?client_id=8dfbc50b-2111-4d03-9b4d-dd0d00aae7a2&response_type=code&redirect_uri=https://portal.azure.com/&nonce=1234&prompt=admin_consent) , und melden Sie sich mit den Anmeldeinformationen eines globalen Office 365-Administrators an.<br/><br/>Das folgende Dialogfeld wird angezeigt. Sie können die "Carets" erweitern, um die Berechtigungen zu überarbeiten, die dem Connector zugewiesen werden.<br/><br/>![Das Dialogfeld Berechtigungsanforderung wird angezeigt.](media/O365_ThirdPartyDataConnector_OptIn1.png)
2. Klicken Sie auf **annehmen**.

Nachdem Sie die Anforderung akzeptiert haben, wird das [Azure-Portal](https://portal.azure.com) angezeigt. Klicken Sie auf **Azure Active Directory** > -**Unternehmensanwendungen**, um die Liste der Anwendungen für Ihre Organisation anzuzeigen. Der Office 365-Drittanbieter-Daten-Konnektor ist auf dem Blade **Enterprise-Anwendungen** aufgeführt.

> [!IMPORTANT]
> Nach dem 30. September 2018 werden drittanbieterdaten nicht mehr in Postfächer in Ihrer Organisation importiert, wenn Sie keinen Drittanbieter-Daten-Konnektor in Azure Active Directory registrieren. Hinweis vorhandene Drittanbieter-Datenkonnektoren (die vor dem 30. September 2018 erstellt wurden) müssen auch in Azure Active Directory registriert werden, indem Sie das Verfahren in Schritt 5 befolgen.

### <a name="revoking-consent-for-a-third-party-data-connector"></a>Widerrufen der Zustimmung für einen Drittanbieter-Daten-Konnektor

Nachdem Ihre Organisation der Berechtigungsanforderung zur Registrierung eines Drittanbieter-Daten-Konnektors in Azure Active Directory zugestimmt hat, kann Ihre Organisation diese Einwilligung jederzeit widerrufen. Das Widerrufen der Zustimmung für einen Connector bedeutet jedoch, dass Daten aus der Drittanbieter-Datenquelle nicht mehr in Office 365 importiert werden.

Um die Einwilligung für einen Drittanbieter-Datenkonnektor zu widerrufen, können Sie die Anwendung (durch Löschen des entsprechenden Dienst Prinzipals) aus Azure Active Directory mithilfe des Blades " **Enterprise-Anwendungen** " im Azure-Portal oder mithilfe der [ Remove-MsolServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/msonline/remove-msolserviceprincipal) in Office 365 PowerShell. Sie können auch das Cmdlet [Remove-AzureADServicePrincipal](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadserviceprincipal) in Azure Active Directory PowerShell verwenden.
  
## <a name="more-information"></a>Weitere Informationen

- Wie bereits erläutert, werden Elemente aus drittanbieterdaten Quellen als e-Mail-Nachrichten in Exchange-Postfächer importiert. Der Partner-Konnektor importiert das Element mithilfe eines für die Office 365-API erforderlichen Schemas. In der folgenden Tabelle werden die Nachrichteneigenschaften eines Elements aus einer Drittanbieter-Datenquelle beschrieben, nachdem es in ein Exchange-Postfach als e-Mail-Nachricht importiert wurde. Die Tabelle gibt auch an, ob die Message-Eigenschaft obligatorisch ist. Obligatorische Eigenschaften müssen aufgefüllt werden. Wenn für ein Element eine obligatorische Eigenschaft fehlt, wird es nicht in Office 365 importiert. Der Importprozess gibt eine Fehlermeldung zurück, die erklärt, warum ein Element nicht importiert wurde und welche Eigenschaft fehlt.
    
    |**Nachrichteneigenschaft**|**Obligatorisch?**|**Beschreibung**|**Beispielwert**|
    |:-----|:-----|:-----|:-----|
    |**FROM** <br/> |Ja  <br/> |Der Benutzer, der das Element ursprünglich erstellt oder in der Drittanbieter-Datenquelle gesendet hat. Der Partner-Konnektor versucht, die Benutzer-ID aus dem Quellelement (beispielsweise einem Twitter-handle) einem Office 365-Benutzerkonto für alle Teilnehmer (Benutzer in den Feldern von und bis) zuzuordnen. Eine Kopie der Nachricht wird in das Postfach jedes Teilnehmers importiert. Wenn keiner der Teilnehmer des Elements einem Office 365-Benutzerkonto zugeordnet werden kann, wird das Element in das Archivierungs Postfach eines Drittanbieters in Office 365 importiert.<br/> <br/> Der Teilnehmer, der als Absender des Elements identifiziert wird, muss über ein aktives Postfach in der Office 365-Organisation verfügen, in das das Element importiert wird. Wenn der Absender nicht über ein aktives Postfach verfügt, wird der folgende Fehler zurückgegeben:<br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |**TO** <br/> |Ja  <br/> |Der Benutzer, der ein Element erhalten hat (wenn für ein Element in der Datenquelle zutreffend).  <br/> | `bob@contoso.com` <br/> |
    |**SUBJECT** <br/> |Nein  <br/> |Der Betreff des Quellelements.  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |**Datum** <br/> |Ja  <br/> |Das Datum, an dem das Element ursprünglich erstellt oder in der Kundendatenquelle veröffentlicht wurde. Beispiel: Das Datum, an dem eine Twitter-Nachricht getweetet wurde.  <br/> | `01 NOV 2015` <br/> |
    |**BODY** <br/> |Nein  <br/> |Der Inhalt der Nachricht oder des Beitrags. Bei einigen Datenquellen kann der Inhalt dieser Eigenschaft mit dem Inhalt der **Subject** -Eigenschaft identisch sein. Während des Importvorgangs versucht der Partner-Konnektor, die vollständige Originaltreue aus der Inhaltsquelle zu erhalten. Wenn möglich, Dateien, Grafiken oder andere Inhalte aus dem Text des Quellelements in dieser Eigenschaft enthalten sind. Andernfalls wird der Inhalt des Quellelements in die **Attachment** -Eigenschaft eingeschlossen. Der Inhalt dieser Eigenschaft hängt vom Partner-Konnektor und von der Funktion der QuellPlattform ab.<br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |**ATTACHMENT** <br/> |Nein  <br/> |Wenn ein Element in der Datenquelle (beispielsweise ein tweet in Twitter oder eine Sofortnachrichtenunterhaltung) über eine angefügte Datei verfügt oder Bilder enthält, versucht der Partner Connect zunächst, Anlagen in die **Body** -Eigenschaft einzuschließen. Wenn dies nicht möglich ist, wird Sie der * * ATTACHMENT * *-Eigenschaft hinzugefügt. Weitere Beispiele für Anlagen sind likes in Facebook, Metadaten aus der Inhaltsquelle und Antworten auf eine Nachricht oder einen Beitrag.<br/> | `image.gif` <br/> |
    |**MESSAGECLASS** <br/> |Ja  <br/> | Hierbei handelt es sich um eine mehrwertige Eigenschaft, die vom Partner-Konnektor erstellt und aufgefüllt wird. Das Format dieser Eigenschaft ist `IPM.NOTE.Source.Event`. (Diese Eigenschaft muss mit `IPM.NOTE`beginnen; dieses Format ähnelt der für die `IPM.NOTE.X` Nachrichtenklasse.) Diese Eigenschaft enthält die folgenden Informationen:<br/><br/>`Source`-Gibt die Datenquelle eines Drittanbieters an. beispielsweise Twitter, Facebook oder BlackBerry.  <br/> <br/>  `Event`-Gibt die Art der Aktivität an, die in der Drittanbieter-Datenquelle ausgeführt wurde, die die Elemente erstellt hat; zum Beispiel ein tweet in Twitter oder ein Beitrag in Facebook. Ereignisse sind spezifisch für die Datenquelle.<br/> <br/>  Ein Zweck dieser Eigenschaft besteht darin, bestimmte Elemente basierend auf der Datenquelle zu filtern, von der ein Element stammt oder auf dem Typ des Ereignisses basiert. In einer eDiscovery-Suche können Sie beispielsweise eine Suchabfrage erstellen, um alle Tweets zu finden, die von einem bestimmten Benutzer gepostet wurden.<br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- Wenn Elemente erfolgreich in Postfächer in Office 365 importiert werden, wird ein eindeutiger Bezeichner als Teil der HTTP-Antwort an den Aufrufer zurückgegeben. Dieser Bezeichner – genannt `x-IngestionCorrelationID`– kann für nachfolgende Problembehandlungszwecke von Partnern für die End-to-End-Nachverfolgung von Elementen verwendet werden. Es wird empfohlen, dass Partner diese Informationen erfassen und am Ende entsprechend protokollieren. Nachfolgend finden Sie ein Beispiel für eine HTTP-Antwort mit diesem Bezeichner:

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- Sie können das Inhaltssuche-Tool im Office 365 Security &amp; Compliance Center verwenden, um nach Elementen zu suchen, die in Postfächern in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Wenn Sie speziell nach diesen importierten Elementen suchen möchten, können Sie die folgenden Nachrichten Eigenschaftswert-Paare im Stichwortfeld für eine Inhaltssuche verwenden. . 
    
  - **`kind:externaldata`**-Verwenden Sie dieses Eigenschaft-Wert-Paar zum Durchsuchen aller Drittanbieter-Datentypen. Wenn Sie beispielsweise nach Elementen suchen möchten, die aus einer Drittanbieter-Datenquelle importiert wurden und das Wort "Contoso" in der Subject-Eigenschaft des importierten Elements enthalten haben, würden Sie `kind:externaldata AND subject:contoso`die Stichwortabfrage verwenden.
    
  - **`itemclass:ipm.externaldata.<third-party data type>`**-Verwenden Sie dieses Eigenschaft-Wert-Paar nur, um einen angegebenen Typ von drittanbieterdaten zu durchsuchen. Wenn Sie beispielsweise nur Facebook-Daten durchsuchen möchten, die das Wort "Contoso" in der Subject-Eigenschaft enthalten, würden `itemclass:ipm.externaldata.Facebook* AND subject:contoso`Sie die Stichwortabfrage verwenden. 

  Eine vollständige Liste der Werte für Drittanbieter-Datentypen für die `itemclass` Eigenschaft finden Sie unter Verwenden der [Inhaltssuche zum Durchsuchen von drittanbieterdaten, die in Office 365 importiert wurden](use-content-search-to-search-third-party-data-that-was-imported.md) .
    
   Weitere Informationen zur Verwendung der Inhaltssuche und zum Erstellen von Stichwortsuchabfragen finden Sie unter:
    
  - [Inhaltssuche in Office 365](content-search.md)
    
  - [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
 
