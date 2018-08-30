---
title: Archivieren von Drittanbieter-Daten in Office 365
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: 9/5/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MOE150
- MET150
ms.assetid: 0ce338d5-3666-4a18-86ab-c6910ff408cc
description: Administratoren können Drittanbieter-Daten aus soziale Medien Plattformen, instant messaging-Plattformen und Dokument für die Zusammenarbeit Plattformen auf Postfächer in Office 365-Organisation importieren. Auf diese Weise können Sie Daten aus Facebook, Twitter und Datenquellen in Office 365 zu archivieren. Anschließend können Sie Appply Office 365 Compliance-Features (wie rechtliche Aufbewahrungspflicht, Inhaltssuche und Aufbewahrungsrichtlinien) auf Drittanbieter-Daten.
ms.openlocfilehash: 3d51d9f5cb546b33fa636fab0ca319e4d24b1ad4
ms.sourcegitcommit: edf5db9357c0d34573f8cc406314525ef10d1eb9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/28/2018
ms.locfileid: "23230037"
---
# <a name="archiving-third-party-data-in-office-365"></a>Archivieren von Drittanbieter-Daten in Office 365

Office 365 ermöglicht Administratoren importieren und Archivieren von Drittanbieter-Daten von Plattformen soziale Medien, instant messaging-Plattformen und Collaboration-Plattformen Dokument auf Postfächer in Office 365-Organisation. Die folgenden: Beispiele für Drittanbieter-Datenquellen, die Sie in Office 365 importieren können 
  
- **Social** - Twitter, Facebook, LinkedIn und Yammer 
    
- **Instant messaging** - Yahoo Messenger, GoogleTalk und Cisco Jabber 
    
- **Zusammenarbeit an Dokumenten** - Feld und Ablage 
    
- **Vertikale Branchen** - Customer Relationship Management (beispielsweise Vertriebs Anwendungsstörgeräusche) und Finanzen (wie Thomson Reuters und Bloomberg) 
    
- **SMS-Text messaging** - BlackBerry 
    
Nach dem Import Drittanbieter-Daten können Sie Office 365 Compliance-Features anwenden – beispielsweise Aufbewahrung für eventuelle Rechtsstreitigkeiten, Inhaltssuche, Compliance-Archivierung, Überwachung und Office 365 Aufbewahrungsrichtlinien – auf diese Daten. Wenn ein Postfach in der Aufbewahrung für eventuelle Rechtsstreitigkeiten eingefügt wird, werden angenommen, Drittanbieter-Daten beibehalten. Sie können Drittanbieter-Daten mithilfe von Inhaltssuche suchen. Oder Sie können anwenden, Archivierung und Aufbewahrungsrichtlinien auf Drittanbieter-Daten wie für Microsoft Data. Kurz gesagt, helfen Archivierung von Drittanbieter-Daten in Office 365 Ihrer Organisation, die Einhaltung der behördlichen und behördlichen Richtlinien bleiben.
  
Hier ist eine Übersicht über den Prozess und die Schritte zum Importieren von Drittanbieter-Daten zu Office 365 erforderlich.

[Schritt 1: Partner für Drittanbieterdaten suchen](#step-1-find-a-third-party-data-partner)

[Schritt 2: Drittanbieter-Postfach in Office 365 erstellen und konfigurieren](#step-2-create-and-configure-a-third-party-data-mailbox-in-office-365)

[Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren](#step-3-configure-user-mailboxes-for-third-party-data)

[Schritt 4: Bereitstellen von Informationen für Ihren Partner](#step-4-provide-your-partner-with-information)

## <a name="how-the-third-party-data-import-process-works"></a>Funktioniert wie die Daten von Drittanbieter-Prozess Importieren >

Die folgende Abbildung und die Beschreibung erläutern, wie der Prozess zum Importieren von Drittanbieterdaten funktioniert.
  
![So funktioniert der Prozess zum Importieren von Drittanbieterdaten](media/5d4cf8e9-b4cc-4547-90c8-d12d04a9f0e7.png)
  
1. Kunden arbeitet mit Partner Wahl eine Verbindung konfigurieren, die Elemente aus der Drittanbieter-Datenquelle extrahiert und dann diese Elemente zu Office 365 importieren.
    
2. Der Partner-Connector Drittanbieter-Datenquellen über einen Drittanbieter-API (auf Basis geplant oder als konfiguriert) her und extrahiert Elemente aus der Datenquelle. Der Partner Connector konvertiert den Inhalt eines Elements in einer e-Mail-Format. Finden Sie [Weitere Informationen](#more-information) im Abschnitt für eine Beschreibung des Message-Format-Schemas. 
    
3. Partner-Connector stellt eine Verbindung mit dem Azure-Dienst in Office 365 mithilfe von Dienst (Exchange Web Services, EWS) über eine bekannte Endpunkt aus.
    
4. Elemente werden in das Postfach eines bestimmten Benutzers oder in ein spezielles Postfach zur Aufnahme aller Drittanbieterdaten importiert. Ob ein Element in das Postfach eines bestimmten Benutzers oder in das Postfach für Drittanbieterdaten importiert wird, basiert auf den folgenden Kriterien:
    
    a **Elemente verfügen, die eine Benutzer-ID, die ein Benutzerkonto für Office 365 entspricht** -Wenn Sie der Connector Partner die Benutzer-ID des Elements in der Drittanbieter-Datenquelle für einen bestimmten Benutzer zugeordnet werden kann, die in den Ordner **Löscht ein** , in des Benutzers-ID in Office 365, das Element kopiert werden. Ordner "wiederherstellbare Elemente". Benutzer können keine Elemente im Ordner Benutzerkontenverwaltung zugreifen. EDiscovery-Tools für Office 365 können Sie jedoch um für Elemente im Ordner Benutzerkontenverwaltung zu suchen.
    
    b. **Elemente, die eine Benutzer-ID besitzen, die ein Office 365-Benutzerkonto entspricht** – Falls der Partner-Connector die Benutzer-ID eines Elements zu einem bestimmten Benutzer zuordnen kann nicht-ID in Office 365, das Element in den Ordner **Posteingang** des Postfachs Drittanbieter-Daten kopiert werden. Importieren von Elementen in den Posteingang können Sie oder eine Person in Ihrer Organisation So melden Sie sich an das Postfach von Drittanbietern zum Anzeigen und Verwalten von dieser Elemente sowie überprüfen, ob alle Korrekturen in der Connectorkonfiguration Partner getroffen werden müssen.
 
## <a name="step-1-find-a-third-party-data-partner"></a>Schritt 1: Partner für Drittanbieterdaten suchen

Eine wichtige Komponente für die Archivierung von Drittanbieter-Daten in Office 365 ist Suchen von und Arbeiten mit einem Microsoft-Partner, die sich auf in Sammeln von Daten aus einer Drittanbieter-Datenquelle und importieren es in Office 365. Nachdem die Daten importiert werden, es kann archiviert und beibehalten zusammen mit Ihrer Organisation des anderen Microsoft-Daten, wie beispielsweise e-Mail-Nachrichten von Exchange und Dokumente aus SharePoint und OneDrive für Unternehmen. Ein Partner erstellt einen Connector, der Daten aus Ihrer Organisation Drittanbieter-Datenquellen (beispielsweise BlackBerry, Facebook, Google +, Thomson Reuters, Twitter und YouTube) extrahiert und übergibt diese Daten an eine Office 365-API, die Elemente in Exchange-Postfächern als importiert e-Mail-Nachrichten. 
  
In den folgenden Abschnitten aufgelistet, die Microsoft-Partner – und Drittanbieter-Datenquellen, die sie unterstützen –, die die Anwendung für die Archivierung von Drittanbieter-Daten in Office 365 beteiligt sind.

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
    
- LivePerson
    
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

[Actiance](https://www.actiance.com) unterstützt die folgenden Drittanbieter-Datenquellen: 
  
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

    
- Cisco Sofortnachrichten &amp; Anwesenheitsserver (v9.0.1, 9.1, v9.1.1 SU1, v10 v10.5.1 SU1)
    
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
    
- YouTube (engl.)
    
  
### <a name="archivesocial"></a>ArchiveSocial

[ArchiveSocial](https://www.archivesocial.com) unterstützt die folgenden Drittanbieter-Datenquellen: 
  
- Facebook
    
- Flickr

    
- Instagram

    
- LinkedIn
    
- Pinterest
    
- Twitter
    
- YouTube (engl.)
    
- Vimeo
  
### <a name="globanet"></a>Globanet

[Globanet](https://www.globanet.com) unterstützt die folgenden Drittanbieter-Datenquellen: 
  
- AOL mit Pivot-Client
 
    
- BlackBerry-Anrufprotokolle (v5, v10, v12)

    
- BlackBerry Messenger (v5, v10, v12)
    
- BlackBerry PIN (v5, v10, v12)
    
- BlackBerry SMS (v5, v10, v12)
    
- Bloomberg Chat

    
- Bloomberg Mail

    
- Box

    
- CipherCloud for Salesforce Chatter
    
- Cisco Sofortnachrichten &amp; Anwesenheitsserver (V11. v10 v10.5.1 SU1, 0, "v11.5 SU2")

- Cisco Webex Teams

- Citrix Workspace &amp; ShareFile

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

    
- YouTube (engl.)
  
### <a name="opentext"></a>OpenText

[OpenText](https://www.opentext.com/what-we-do/products/opentext-product-offerings-catalog/rebranded-products/daegis) unterstützt die folgenden Drittanbieter-Datenquellen: 
  
- Axs Encrypted
    
- Axs Exchange
    
- Axs Local Archive
    
- Axs PlaceHolder
    
- Axs Signed
    
- Bloomberg
    
- Thomson Reuters
  
### <a name="verba"></a>Verba

[Verba](https://www.verba.com) unterstützt die folgenden Drittanbieter-Datenquellen: 
  
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
    
- Cisco UCCX/UCCE VoIP
    
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

Hier sind die Schritte zum Erstellen und Konfigurieren eines Postfachs Drittanbieter-Daten für das Importieren von Daten in Office 365. Wie vorherige erläutert, Elemente auf dieses Postfach importiert werden, wenn der Partner-Connector die Benutzer-ID des Elements ein Benutzerkonto für Office 365 zugeordnet ist nicht möglich.
  
 **Führen Sie diese Aufgaben in Office 365 Administrationscenter**
  
1. Erstellen eines neuen Benutzerkontos in Office 365, und weisen Sie es mit einer Lizenzvertrags für Exchange Online – Plan 2; finden Sie unter [Hinzufügen von Benutzern zu Office 365](https://go.microsoft.com/fwlink/p/?LinkId=692098). So platzieren das Postfach in die Aufbewahrung für eventuelle Rechtsstreitigkeiten oder Aktivieren eines archivpostfachs, das eine unbegrenzte Speicherkontingent hat, ist eine Plan 2-Lizenz erforderlich.
    
2. Fügen Sie das Benutzerkonto für das Postfach von Drittanbieter-Daten für die **Exchange-Administrator** -Admin-Rolle in Office 365; finden Sie unter [Zuweisen von Administratorrollen in Office 365](https://go.microsoft.com/fwlink/p/?LinkId=532393).
    
    > [!TIP]
    > Notieren Sie die Anmeldeinformationen für dieses Benutzerkonto. Sie müssen diese für Ihren Partner bereitstellen, wie in Schritt 4 beschrieben. 
  
 **Führen Sie diese Aufgaben in der Exchange-Verwaltungskonsole**
  
1. Ausblenden des Postfachs Drittanbieter-Daten aus dem Adressbuch und andere Adresslisten in Ihrer Organisation; finden Sie unter [Verwalten von Benutzerpostfächern](https://go.microsoft.com/fwlink/p/?LinkId=616058). Alternativ können Sie den folgenden PowerShell-Befehl ausführen:
    
    ```
    Set-Mailbox -Identity <identity of third-party data mailbox> -HiddenFromAddressListsEnabled $true
    ```

2. Weisen Sie die Berechtigung **FullAccess** das Postfach von Drittanbieter-Daten, damit Administratoren oder Compliance Officer das Postfach von Drittanbietern Daten im Outlook-Desktopclient geöffnet werden können; finden Sie unter [Verwalten von Berechtigungen für Empfänger](https://go.microsoft.com/fwlink/p/?LinkId=692104).
    
3. Aktivieren Sie die folgenden Compliance-bezogene Office 365-Features für das Postfach von Drittanbieter-Daten:
    
    - Aktivieren Sie das Archivpostfach; finden Sie unter [archivpostfächern in die Office 365-Sicherheit aktivieren &amp; Compliance Center](enable-archive-mailboxes.md) und [unbegrenzte Archivierung in Office 365 zu aktivieren](enable-unlimited-archiving.md). Auf diese Weise können Sie frei bis Speicherplatz in das primäre Postfach durch Einrichten einer Archivrichtlinie, die Elemente von Drittanbieter-Daten in das Archivpostfach verschoben. Dies stellt Sie unbegrenzte Speicher für Drittanbieter-Daten bereit.
    
    - Platzieren Sie das Postfach von Drittanbieter-Daten in die Aufbewahrung für eventuelle Rechtsstreitigkeiten. Sie können auch anwenden eine Aufbewahrungsrichtlinie Office 365 in die Office 365-Sicherheit &amp; Compliance Center. Platzieren dieses Postfach in der Warteschleife wird aufbewahren von von Drittanbieter-Datenelementen (auf unbestimmte Zeit oder für eine angegebene Dauer) und zu verhindern, aus dem Postfach gelöscht werden. Finden Sie in den folgenden Themen:
    
      - [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
      - [Übersicht über Aufbewahrungsrichtlinien in Office 365](retention-policies.md)
    
       
    
    - Aktivieren Sie die postfachüberwachungsprotokollierung für den Besitzer, Delegaten und Admin-Zugriff auf das Postfach von Drittanbietern Daten; finden Sie unter [Überwachung in Office 365 Postfach zu aktivieren](enable-mailbox-auditing.md). Dadurch können Sie alle Aktivitäten, die von jedem Benutzer mit Zugriff auf das Postfach von Drittanbietern Daten überwachen.

## <a name="step-3-configure-user-mailboxes-for-third-party-data"></a>Schritt 3: Benutzerpostfächer für Drittanbieterdaten konfigurieren

Der nächste Schritt besteht darin Benutzerpostfächer zur Unterstützung von Drittanbieter-Daten konfigurieren. Führen Sie diese Aufgaben mithilfe der Exchange-Verwaltungskonsole oder mithilfe der entsprechenden Windows PowerShell-Cmdlets.
  
1. Aktivieren Sie das Archivpostfach für jeden Benutzer. finden Sie unter [archivpostfächern in die Office 365-Sicherheit aktivieren &amp; Compliance Center](enable-archive-mailboxes.md) und [unbegrenzte Archivierung in Office 365 zu aktivieren](enable-unlimited-archiving.md).
    
2. Platzieren von Benutzerpostfächern in Aufbewahrung für eventuelle Rechtsstreitigkeiten oder Anwenden einer Aufbewahrungsrichtlinie für Office 365. finden Sie in den folgenden Themen: 
    
    - [Place a mailbox on Litigation Hold](https://go.microsoft.com/fwlink/p/?LinkId=404420)
    
    - [Übersicht über Aufbewahrungsrichtlinien in Office 365](retention-policies.md)
    
    Wie bereits weiter oben erwähnt, können Sie beim Aktivieren des Beweissicherungsverfahrens für Postfächer festlegen, wie lange Elemente aus einer Drittanbieter-Datenquelle aufbewahrt werden sollen. Sie können auch festlegen, dass sie dauerhaft aufbewahrt werden sollen.

## <a name="step-4-provide-your-partner-with-information"></a>Schritt 4: Bereitstellen von Informationen für Ihren Partner

Im letzten Schritt müssen Sie dem Partner die folgenden Informationen bereitstellen, damit er den Connector für die Verbindung mit Office 365-Organisation konfigurieren kann, um Daten in Benutzerpostfächer und das Drittanbieterdaten-Postfach zu importieren. 
  
- Der Endpunkt für die Verbindung mit dem Azure-Dienst in Office 365 verwendet:

    ```
    https://office365ingestionsvc.gble1.protection.outlook.com/service/ThirdPartyIngestionService.svc
    ```

- Die Anmeldung Anmeldeinformationen (Office 365-Benutzer-ID und Kennwort) für das Postfach von Drittanbieter-Daten, das Sie in Schritt2 erstellt haben. Diese Anmeldeinformationen sind erforderlich, damit der Partner-Connector zugreifen und Elemente für Benutzerpostfächer und an das Postfach von Drittanbietern Daten importieren kann.
    

  
## <a name="more-information"></a>Weitere Informationen

- Wie vorherige erläutert, Elemente von Drittanbieter-Daten, die in Exchange-Postfächern als e-Mail-Nachrichten Quellen importiert werden. Der Partner-Connector importiert das Element mit einem Schema, das von der Office 365-API erforderlich. In der folgenden Tabelle werden die Eigenschaften eines Elements aus einer Drittanbieter-Datenquelle beschrieben, nach dem Import auf einem Exchange-Postfach als e-Mail-Nachricht ist. Die Tabelle zeigt auch an, ob die Message-Eigenschaft zwingend erforderlich ist. Erforderliche Eigenschaften müssen aufgefüllt werden. Wenn ein Element eine erforderliche Eigenschaft nicht angezeigt wird, werden nicht es zu Office 365 importiert werden. Der Importvorgang wird eine Fehlermeldung angezeigt, die erklärt, warum ein Element wurde nicht importiert und welche Eigenschaft fehlt zurückgegeben.
    
    |**Nachrichteneigenschaft**|**Zwingend erforderlich?**|**Beschreibung**|**Beispielwert**|
    |:-----|:-----|:-----|:-----|
    |**FROM** <br/> |Ja  <br/> |Der Benutzer, die ursprünglich erstellt oder das Element in der Drittanbieter-Datenquelle gesendet. Der Partner-Verbindung versucht, die Benutzer-ID aus dem Quellelement (beispielsweise ein Handle Twitter) ein Benutzerkonto für Office 365 für alle Teilnehmer (Benutzer in die Felder FROM und TO) zuordnen. Eine Kopie der Nachricht wird an das Postfach von jedem Teilnehmer importiert werden. Wenn keines der Teilnehmer aus dem Element zu einem Office 365-Benutzerkonto zugeordnet werden kann, wird das Element auf das Postfach der Drittanbieter-Archivierung in Office 365 importiert werden.<br/> <br/> Der Teilnehmer, der als Absender des Elements identifiziert wird benötigen kein active-Postfach in der Office 365-Organisation, die auf das Element importiert wird. Wenn der Absender eine aktive Postfach besitzt, wird die folgende Fehlermeldung zurückgegeben:<br/><br/>  `One or more messages in the Request failed to be delivered to either From or Sender email address. You will need to resend your entire Request. Error: The request failed. The remote server returned an error: (401) Unauthorized.`  | `bob@contoso.com` <br/> |
    |**TO** <br/> |Ja  <br/> |Der Benutzer, der ein Element erhalten hat (wenn für ein Element in der Datenquelle zutreffend).  <br/> | `bob@contoso.com` <br/> |
    |**SUBJECT** <br/> |Nein  <br/> |Der Betreff des Quellelements.  <br/> | `"Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/> |
    |**DATUM** <br/> |Ja  <br/> |Das Datum, an dem das Element ursprünglich erstellt oder in der Kundendatenquelle veröffentlicht wurde. Beispiel: Das Datum, an dem eine Twitter-Nachricht getweetet wurde.  <br/> | `01 NOV 2015` <br/> |
    |**BODY** <br/> |Nein  <br/> |Der Inhalt der Nachricht oder des Beitrags. Für einige Datenquellen können den Inhalt dieser Eigenschaft des Inhalts für die **SUBJECT** -Eigenschaft identisch sein. Während des Importvorgangs versucht der Partner Connector originalgetreue aus der Inhaltsquelle wie möglich beizubehalten. Wenn möglich ist in dieser Eigenschaft Dateien, Grafiken oder andere Inhalte aus dem Textkörper des Quellelements enthalten. Andernfalls ist in der **Anlage** -Eigenschaft Inhalte aus dem Quellelement enthalten. Der Inhalt dieser Eigenschaft werden für den Connector Partner und für die Funktionalität der Source-Plattform abhängig sind.<br/> | `Author: bob@contoso.com` <br/>  `Date: 10 DEC 2014` <br/>  `Tweet: "Mega deals with Contoso coming your way! #ContosoHolidayDeals"` <br/>  `Date: 01 NOV 2015` <br/> |
    |**ATTACHMENT** <br/> |Nein  <br/> |Wenn ein Element in der Datenquelle (beispielsweise einen Tweet in Twitter oder einer Unterhaltung über Sofortnachrichten) hat eine angefügte Datei oder fügen Sie Bilder, Verbinden des Partners wird ersten Versuch zum Einschließen von Anlagen in die **BODY** -Eigenschaft. Wenn das ist nicht möglich, wird diese hinzugefügt der ** Anlage ** Eigenschaft. Weitere Beispiele für Anlagen sind "gefällt mir" in Facebook Metadaten aus der Inhaltsquelle und Antworten auf eine Nachricht oder ein Beitrag.<br/> | `image.gif` <br/> |
    |**MESSAGECLASS** <br/> |Ja  <br/> | Dies ist eine mehrwertige-Eigenschaft, die erstellt und durch Partner Connector aufgefüllt wird. Das Format dieser Eigenschaft ist `IPM.NOTE.Source.Event`. (Diese Eigenschaft muss zunächst `IPM.NOTE`; dieses Format ist vergleichbar mit der für die `IPM.NOTE.X` Nachrichtenklasse.) Diese Eigenschaft enthält die folgenden Informationen:<br/><br/>`Source`-Gibt die Drittanbieter-Datenquelle an. beispielsweise Twitter, Facebook oder BlackBerry.  <br/> <br/>  `Event`-Gibt den Typ der Aktivität, die in der Drittanbieter-Datenquelle ausgeführt wurde, die die Elemente erzeugt an. beispielsweise einen Tweet in Twitter oder ein Beitrag in Facebook. Ereignisse sind für die Datenquelle spezifisch.<br/> <br/>  Ein Zweck von dieser Eigenschaft wird zum Filtern von bestimmter Elementen basierend auf die Datenquelle, an dem ein Element stammt oder basierend auf den Typ des Ereignisses. Beispielsweise können in einer eDiscovery-Suche Sie erstellen eine Suchabfrage aus, um alle Tweets zu suchen, die von einem bestimmten Benutzer veröffentlicht wurden.<br/> | `IPM.NOTE.Twitter.Tweet` <br/> |
   
- Wenn Elemente auf Postfächer in Office 365 erfolgreich importiert wurden, wird eine eindeutige ID wieder an den Aufrufer als Teil der HTTP-Antwort zurückgegeben. Dieser Bezeichner – aufgerufen `x-IngestionCorrelationID`– aus Gründen nachfolgende zur Problembehandlung von Partnern für eine End-to-End-Überwachung von Elementen verwendet werden kann. Es wird empfohlen, dass Partner diese Informationen erfassen und melden Sie es entsprechend geleitet. Es folgt ein Beispiel für eine HTTP-Antwort, die mit diesem Bezeichner:

    ```
    HTTP/1.1 200 OK
    Content-Type: text/xml; charset=utf-8
    Server: Microsoft-IIS/8.5
    x-IngestionCorrelationID: 1ec7667d-f097-47fe-a9a2-bc7ab0a7552b
    X-AspNet-Version: 4.0.30319
    X-Powered-By: ASP.NET
    Date: Tue, 02 Feb 2016 22:55:33 GMT 
    ```
 
- Sie können das Tool für die Inhaltssuche in die Office 365-Sicherheit &amp; Compliance Center, um die Suche nach Elementen, die auf Postfächer in Office 365 aus einer Drittanbieter-Datenquelle importiert wurden. Um speziell für diese importierte Elemente zu suchen, können Sie die folgende Meldung-Wert-Paare im Schlüsselwort für ein Inhaltssuche verwenden. . 
    
  - **`kind:externaldata`**-Verwenden Sie diese Eigenschaft-Wert-Paar, um alle Arten von Drittanbietern suchen. Verwenden Sie beispielsweise, um die Suche nach Elementen, die aus einer Drittanbieter-Datenquelle importiert wurden und das Wort "Contoso" in die Subject-Eigenschaft des importierten Elements enthalten die Stichwortabfrage `kind:externaldata AND subject:contoso`.
    
  - **`itemclass:ipm.externaldata.<third-party data type>`**-Verwenden Sie dieses-Eigenschaft-Wert-Paar nur Suche eines Datentyps Drittanbieter-angeben. Um nur Facebook Daten zu suchen, die das Wort "Contoso" in die Subject-Eigenschaft enthält, verwenden Sie beispielsweise die Stichwortabfrage `itemclass:ipm.externaldata.Facebook* AND subject:contoso`. 

  Eine vollständige Liste der Werte für Drittanbieter-Datentypen für die `itemclass` -Eigenschaft, finden Sie unter [Inhaltssuche verwenden, um Daten von Dritten zu suchen, die in Office 365 importiert wurde,](use-content-search-to-search-third-party-data-that-was-imported.md)
    
   Weitere Informationen zur Verwendung der Inhaltssuche und zum Erstellen von Stichwortsuchabfragen finden Sie unter:
    
  - [Content-Suche in Office 365](content-search.md)
    
  - [Stichwortabfragen und Suchbedingungen für die Inhaltssuche](keyword-queries-and-search-conditions.md)
 
