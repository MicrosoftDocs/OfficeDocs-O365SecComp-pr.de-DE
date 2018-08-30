---
title: Office 365 Reporting Features
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: Eine Erläuterung der Berichterstellungsfeatures in Office 365.
ms.openlocfilehash: 5a448089de5d517b81551269416c4a6f91599725
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530038"
---
# <a name="office-365-reporting-features"></a>Office 365 Reporting Features 

## <a name="introduction"></a>Einführung
Das Berichtsfeature in Office 365 bietet eine Vielzahl von Überwachungsberichten für Azure Active Directory (AD), Exchange Online Gerätemanagement generelle überprüfen und Verhinderung von Datenverlust (DLP). Dies sind verschiedene und die Office 365 Berichte trennen.

## <a name="office-365-reports-dashboard"></a>Office 365-Berichte (engl.)
Das Dashboard Berichte in der Office 365 Admin Center Vorschau zeigt zur Nutzung über Office 365. Globale Office 365-Administratoren oder ein Exchange Online, SharePoint Online oder Skype für Business-Administrator kann differenzierte Einblick in die Verwendung dieses Diensts abrufen. Berichte können Insights wie die Anzahl von Benutzern Verarbeiten von einem bestimmten Office 365-Dienst die Anzahl der Benutzer, die aktiviert haben, Office Professional Plus und wie viele e-Mail-Nachrichten über die Organisation fließt bereitstellen. Berichte sind für die letzten 7, 30, 90 und 180 Tage verfügbar.

Die folgenden Berichte sind verfügbar:
- [Bericht über Benutzeraktivität von e-Mail](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office-Aktivierungen Bericht](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Online Websiteverwendungsbericht](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive for Business-Verwendungsbericht](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Bericht über Benutzeraktivität Yammer](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype für Business Aktivitätsbericht](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Skype für Business Peer-zu-Peer-Aktivitätsbericht](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Skype für Business Konferenzorganisator Bericht](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Skype für Konferenzteilnehmer Business Aktivitätsbericht](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Weitere Informationen finden Sie unter [Berichte im Office 365 Admin Center](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263).


## <a name="azure-active-directory-reports"></a>Azure Active Directory-Berichte
Office 365 verwendet Azure AD-Authentifizierung und Identitätsmanagement. Office 365-Administratoren können die Berichte von Azure generierte ungewöhnliche Aktivitäten und nicht autorisiertem Zugriff auf ihre Daten gesucht. Die Berichte Zugriff und die Verwendung können in Azure AD Sie um Einblicke in die Integrität und Sicherheit der Verzeichnis Ihrer Organisation zu erhalten. Mit diesen Informationen kann ein Administrator besser ermitteln, in möglichen Sicherheitsrisiken möglicherweise nicht so, dass sie ausreichend, diese Risiken planen können.

Azure AD-Berichte können in Microsoft Excel exportiert und korreliert mit anderen Daten aus Office 365, wie die Ergebnisse einer Audit Log-Suche, um einen Einblick in Access, Authentifizierung und Anwendungsebene Aktivitäten bereitzustellen. Erweiterte Anomalie- und Ressource Verwendungsberichte sind verfügbar, wenn Azure AD Premium aktiviert ist. Diese erweiterte meldet Hilfe zur Verbesserung der Organisation Sicherheit Posture und Hilfe Organisationen durch die Nutzung von Analytics zur Verwendung des Geräts Access und Anwendung auf potenzielle Bedrohungen zu reagieren. Weitere Informationen finden Sie unter [reporting Azure Active Directory](https://docs.microsoft.com/azure/active-directory/reports-monitoring/overview-reports/).

## <a name="exchange-online-audit-reports"></a>Exchange Online-Überwachungsberichte
Exchange Online-Überwachungsberichte enthalten Details zu Postfachzugriff und Änderungen durch Administratoren zu einer Organisation Exchange Online-Mandanten. Nachdem die Überwachung von Postfächern aktiviert ist, können Sie die Aufgaben in der folgenden Tabelle zum Ausführen von Berichten und Exchange Online Überwachungsprotokolle exportieren.

>**Hinweis**: Sie müssen aktivieren Postfach Audit logging für jedes Postfach, sodass überwachten Ereignisse im Überwachungsprotokoll für dieses Postfach gespeichert werden. Wenn postfachüberwachungsprotokollierung für ein Postfach nicht Protokollierung aktiviert, Ereignisse für dieses Postfach wird nicht in das Überwachungsprotokoll gespeichert werden und in Überwachungsberichte Postfach nicht angezeigt. Weitere Informationen finden Sie unter [Aktivieren der Überwachung von Postfächern](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918).

| Task | Beschreibung |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ausführen eines Berichts zum Postfachzugriff durch Nicht-Besitzer](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Zeigt die Liste der Postfächer, die von einem anderen als den Besitzer des Postfachs zugegriffen wurde. Der Bericht enthält Informationen, die das Postfach zugegriffen, die Aktionen, die sie in das Postfach hat und ob die Aktionen erfolgreich waren. |
| [Exportieren von Postfachüberwachungsprotokollen](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Postfachüberwachungsprotokolle enthalten Informationen zu Access und Aktionen in einem Postfach durch einen Benutzer als Besitzer des Postfachs geschaltet. Administratoren können Postfächer sowie einen Datumsbereich zum Generieren von Berichten angeben. Die Protokolle sind in XML-Datei exportiert, an eine Nachricht angefügt und auf bestimmte Benutzer gemäß den Administrator gesendet. |
| [Ausführen eines Berichts für Administratorrollengruppen](https://docs.microsoft.com/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | Die Administrator Rollengruppe wird verwendet, um Benutzern Administratorrechte zuweisen. Diese Berechtigungen zulassen, dass Benutzer administrative Aufgaben wie das Zurücksetzen von Kennwörtern, erstellen oder Ändern von Postfächern und anderen Benutzern Administratorrechte zuweisen. Der Administrator-rollengruppenbericht zeigt Änderungen Rollengruppen, einschließlich das Hinzufügen oder Entfernen von Mitgliedern. |
| [Anzeigen des administratorüberwachungsprotokolls](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | Admin Audit Log Berichtslisten, die alle erstellen, aktualisieren und Löschen von Funktionen, die von Administratoren in Exchange Online ausgeführt. Protokolleinträge enthalten Informationen über welche Cmdlet ausgeführt wurde, welche Parameter verwendet wurden, die das Cmdlet ausgeführt wurde und welche Objekte betroffen waren. |
| [Inhaltssuche Postfach und Archiv](https://docs.microsoft.com/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Enthält Details zu Änderungen an In-Place eDiscovery oder Compliance-Archiv-Einstellungen für Postfächer. |
| [Exportieren des administratorüberwachungsprotokolls](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | Admin Überwachungsprotokolldatensätze, wie bestimmte Verwaltungsvorgänge erstellen, aktualisieren und Löschen in Exchange Online. Die Ergebnisse aus dem Protokoll sind in XML exportiert, und Administratoren können verhindern, dass dieses Protokoll an eine Gruppe von Benutzern zu senden. |
| [Ausführen eines Berichts zu Beweissicherungsverfahren pro Postfach](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Enthält Details zu den Änderungen Rechtsstreitigkeiten Einstellungen für Postfächer halten. |
| [Anzeige und Export des externen Administratorüberwachungsprotokolls](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Enthält ausführliche Informationen zu Aktionen, die von externen Administratoren durchgeführt. Die Einträge enthalten Informationen, welche Cmdlet wurde ausführen, welche Parameter verwendet wurden und alle Aktionen, die erstellen, ändern oder Löschen von Objekten in Exchange Online. |

## <a name="device-compliance-reports"></a>Gerät Compliance-Berichte
Sie können verwalten und mobile Geräten secure, wenn sie mit Office 365-Organisation verbunden sind, mithilfe von Office 365 Mobile Device Management (MDM). Mobile Geräte wie Smartphones und Tablets, mit denen Arbeit e-Mail, Kalender, Kontakte zugreifen und Dokumente spielen eine wichtige Rolle, die dafür sorgen, dass Mitarbeiter jederzeit und überall arbeiten können, und unabhängig vom Standort. Daher ist es wichtig, dass Sie die Informationen Ihres Unternehmens schützen. Sie können die Office 365 MDM verwenden, um gerätesicherheit Richtlinien und Zugriffsregeln festzulegen und mobile Geräte zu löschen, wenn sie verlorenen oder gestohlenen.

MDM Compliance-Berichte enthalten eine Übersicht über Richtlinien, die von einem Unternehmen eingerichtet wurde, den Schutz von mobilen Geräten, die auf Office 365-Daten zugreifen. Der Bericht ermöglicht das Filtern von Geräten von Compliance-Status, gemeldete Verstöße, blockierte Geräte und wie viele Geräte aufgrund von Sicherheitsrichtlinien Kennworteingaben gelöscht wurden. Weitere Informationen finden Sie unter [Overview of Mobile Gerätemanagement für Office 365](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a).

## <a name="data-loss-prevention"></a>Verhinderung von Datenverlust
DLP-Richtlinien tragen die Sicherheits- und Informationsfluss in einer Organisation verwalten. Sie können Richtlinien zum Blockieren Sie den Zugriff auf Inhalte, Verschlüsseln von Daten oder benachrichtigen Sie Benutzer der Richtlinie und Verstöße gegen mit DLP-Richtlinientipps in der Anwendung einrichten. DLP-Berichte Einblicke in die Anzahl der Richtlinie und Regel übereinstimmt, Außerkraftsetzungen und falsch positive Ergebnisse.

Sie können das Office 365 Administrationscenter verwenden, zum Anzeigen von Informationen über die Anzahl der Nachrichten, die von Ihrer DLP-Richtlinien in Diagramms oder Tabellenformat erkannt werden. DLP-Richtlinie Übereinstimmungen für gesendet und Empfangen von e-Mail, insbesondere DLP-regelübereinstimmungen für gesendete und empfangene Nachrichten. Sie können auch die Anzahl von Übereinstimmungen, Außerkraftsetzungen und falsch positive Ergebnisse für jede Richtlinie in den vergangenen 24 Stunden mithilfe der Exchange-Verwaltungskonsole anzeigen. Jedoch ist diese Daten nicht als Grafik zur Verfügung. Wenn Sie einen Bericht zur Verwendung in Excel heruntergeladen haben, können Sie auch weitere Details, wie etwa der Absender der Nachricht, an welchem Tag anzeigen und welche richtlinienübereinstimmungen ausgelöst wurden. Weitere Informationen finden Sie unter [Anzeigen von Berichten zu DLP-Richtlinie erkannte](https://technet.microsoft.com/en-us/library/jj889415(v=exchg.150).aspx).

## <a name="auditing-in-yammer-enterprise"></a>Überwachung in Yammer Enterprise
Yammer Enterprise Administratoren die Möglichkeit zum Exportieren von Benutzerdaten Aktivität aus ihren Yammer-Netzwerke über das [Exportieren von Daten-API Yammer](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)oder manuell über den der Yammer-Netzwerk-Admin-Seite enthält. Die Möglichkeit zum Exportieren von Protokollen ist auf Netzwerkadministratoren in Yammer beschränkt. (Alle globale Office 365-Administratoren sind Netzwerkadministratoren Yammer.)

Die folgenden Daten können exportiert werden:

| Filename | Beschreibung |
|----------------------------|-------------------------------------------------------------------------|
| Users.csv | Alle neu, Ausstehend und angehaltenen Benutzer im Netzwerk |
| Messages.csv | Alle Nachrichten im Netzwerk |
| Files.csv (Metadaten) | Metadaten wie Dateiname, Datei-API-URL, Ladeprogramm ID, usw. hochgeladenen an. |
| Files.csv (Originaldateien) | ZIP-Datei der ursprünglichen Dateien, die von Benutzern in Yammer hochgeladen wurden |
| Topics.csv | Themen im Netzwerk erstellt |
| Pages.csv | Seiten (Notes) von Benutzern im Netzwerk erstellt |
| Admins.csv | Alle überprüft Administratoren im Netzwerk |
| Networks.csv | Alle Yammer externe Netzwerke |

*Tabelle 3: Yammer-Netzwerk Datendateien verfügbar für den Export von Kunden*

Yammer Enterprise-Daten ist auch über die Office 365 Berichte verfügbar. Darüber hinaus Yammer arbeiten aktiv über Daten zum Verfügbarmachen zusätzliche Protokollierung über die Office 365 Management Aktivität-API, und klicken Sie auf die Möglichkeit zum Grund Power BI verwendet wird. Finden Sie unter der [Wegweiser für Office](https://fasttrack.microsoft.com/roadmap?filters=yammer) für Weitere Informationen zu diesen Funktionen.
