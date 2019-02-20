---
title: Berichtsfeatures in Office 365
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
ms.collection:
- Strat_O365_IP
- M365-analytics
description: Eine Erläuterung der Berichterstellungsfeatures in Office 365.
ms.openlocfilehash: f750ac6647199ef14bd6605535797e00c1cab961
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090897"
---
# <a name="office-365-reporting-features"></a>Berichtsfeatures in Office 365 

## <a name="introduction"></a>Einführung
Das Berichtsfeature in Office 365 bietet eine Vielzahl von Überwachungsberichten für Azure Active Directory (AD), Exchange Online, Device Management, Supervisory Review und Data Loss Prevention (DLP). Diese unterscheiden sich von den Office 365-Aktivitätsberichten.

## <a name="office-365-reports-dashboard"></a>Office 365-Dashboard "Berichte"
Im Dashboard "Berichte" in der Office 365 Admin Center-Vorschau wird die Verwendungs Aktivität in Office 365 angezeigt. Office 365 globale Administratoren oder ein Exchange Online-, SharePoint Online-oder Skype for Business-Administrator können detaillierte Einblicke in die Nutzung dieses Diensts erhalten. Berichte bieten Einblicke wie die Anzahl der Benutzer, die einen bestimmten Office 365-Dienst verwenden, die Anzahl der Benutzer, die Office Professional Plus aktiviert haben, und wie viele e-Mails über die Organisation fließen. Berichte sind für die letzten 7, 30, 90 und 180 Tage verfügbar.

Die folgenden Berichte sind verfügbar:
- [E-Mail-Aktivitätsbericht](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Email-activity-1cbe2c00-ca65-4fb9-9663-1bbfa58ebe44)
- [Microsoft Office-Aktivierungsbericht](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--Microsoft-Office-activations-87c24ae2-82e0-4d1e-be01-c3bcc3f18c60)
- [SharePoint Online-Websiteverwendungsbericht](https://support.office.com/article/Office-365-Reports-in-the-admin-center-preview--SharePoint-site-usage-4ecfb843-e5d5-464d-8bf6-7ed512a9b213)
- [OneDrive for Business-Verwendungsbericht](https://support.office.com/article/Office-365-Reports-in-the-Admin-Center-Preview--OneDrive-for-Business-usage-0de3b312-c4e8-4e4b-a02d-32b2f726a680)
- [Yammer-Aktivitätsberichte](https://support.office.com/article/View-the-Yammer-Activity-report-in-the-Office-365-admin-center-preview-c7c9f938-5b8e-4d52-b1a2-c7c32cb2312a)
- [Skype for Business-Aktivitätsbericht](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/activity-report)
- [Bericht über Skype for Business-Peer-to-Peer-Aktivität](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/peer-to-peer-activity-report)
- [Bericht zu Skype for Business-Konferenzorganisator](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-organizer-activity-report)
- [Bericht über Skype for Business-Konferenzteilnehmer](https://docs.microsoft.com/SkypeForBusiness/skype-for-business-online-reporting/conference-participant-activity-report)

Weitere Informationen finden Sie unter [Aktivitätsberichte im Office 365 Admin Center](https://support.office.com/article/activity-reports-in-the-office-365-admin-center-0d6dfb17-8582-4172-a9a9-aed798150263).


## <a name="azure-active-directory-reports"></a>Azure Active Directory-Berichte
Office 365 verwendet Azure AD für die Authentifizierung und Identitätsverwaltung. Office 365-Administratoren können die von Azure generierten Berichte verwenden, um nach ungewöhnlichen Aktivitäten und nicht autorisiertem Zugriff auf Ihre Daten zu suchen. Sie können die Zugriffs-und Verwendungsberichte in Azure AD verwenden, um die Integrität und Sicherheit des Verzeichnisses Ihrer Organisation zu erhalten. Anhand dieser Informationen kann ein Administrator besser feststellen, wo mögliche Sicherheitsrisiken auftreten können, damit Sie angemessen planen können, diese Risiken einzudämmen.

Azure AD-Berichte können in Microsoft Excel exportiert und mit anderen Daten aus Office 365, wie beispielsweise den Ergebnissen einer Überwachungsprotokoll Suche, korreliert werden, um Einblicke in den Zugriff, die Authentifizierung und Aktivitäten auf Anwendungsebene zu ermöglichen. Erweiterte Anomalien und Ressourcen Nutzungsberichte sind verfügbar, wenn Azure AD Premium aktiviert ist. Diese erweiterten Berichte helfen, die Sicherheitsposition einer Organisation zu verbessern und Organisationen bei der Reaktion auf potenzielle Bedrohungen zu unterstützen, indem Sie Analysen zum Geräte Zugriff und zur Anwendungsnutzung nutzen. Weitere Informationen finden Sie unter [Azure Active Directory Reporting](https://docs.microsoft.com/azure/active-directory/reports-monitoring/overview-reports/).

## <a name="exchange-online-audit-reports"></a>Exchange Online-Überwachungsberichte
Exchange Online-Überwachungsberichte schließen Details über den Postfachzugriff und Änderungen durch Administratoren an den Exchange Online-Mandanten einer Organisation ein. Nachdem die postfachüberwachung aktiviert wurde, können Sie die Aufgaben in der folgenden Tabelle verwenden, um Berichte auszuführen und Exchange Online-Überwachungsprotokolle zu exportieren.

>**Hinweis**: Sie müssen die postfachüberwachungsprotokollierung für jedes Postfach aktivieren, damit überwachte Ereignisse im Überwachungsprotokoll für dieses Postfach gespeichert werden. Wenn die postfachüberwachungsprotokollierung für ein Postfach nicht aktiviert ist, werden Ereignisse für dieses Postfach nicht im Überwachungsprotokoll gespeichert und nicht in Post Fach Überwachungsberichten angezeigt. Weitere Informationen finden Sie unter [Aktivieren der postfachüberwachung](https://support.office.com/article/Enable-mailbox-auditing-in-Office-365-aaca8987-5b62-458b-9882-c28476a66918).

| Aufgabe | Beschreibung |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Ausführen eines Berichts zum Postfachzugriff durch Nicht-Besitzer](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/non-owner-mailbox-access-report) | Zeigt die Liste der Postfächer an, auf die von anderen Benutzern als dem Besitzer des Postfachs zugegriffen wurde. Der Bericht enthält Informationen darüber, wer auf das Postfach zugegriffen hat, welche Aktionen Sie im Postfach durchgeführt haben und ob die Aktionen erfolgreich waren. |
| [Exportieren von Postfachüberwachungsprotokollen](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/export-mailbox-audit-logs) | Postfachüberwachungsprotokolle enthalten Informationen zum Zugriff und zu Aktionen in einem Postfach, die von einem anderen Benutzer als dem Postfachbesitzer übernommen wurden. Administratoren können Postfächer zusammen mit einem Datumsintervall angeben, um Berichte zu generieren. Die Protokolle werden in XML exportiert, einer Nachricht angefügt und an bestimmte Benutzer gesendet, wie vom Administrator festgelegt. |
| [Ausführen eines Berichts für Administratorrollengruppen](https://docs.microsoft.com/Office365/SecurityCompliance/eop/run-an-administrator-role-group-report-in-eop-eop) | Die Administratorrollengruppe wird verwendet, um Benutzern Administratorrechte zuzuweisen. Mit diesen Berechtigungen können Benutzer Verwaltungsaufgaben wie Kennwörter zurücksetzen, Postfächer erstellen oder ändern und anderen Benutzern Administratorrechte zuweisen. Der Administratorrollengruppen Bericht enthält Änderungen an Rollengruppen, einschließlich des Hinzufügens oder Entfernens von Mitgliedern. |
| [Anzeigen des administratorüberwachungsprotokolls](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-administrator-audit-log) | Der Administrator-Überwachungsprotokollbericht listet alle CREATE-, Update-und DELETE-Funktionen auf, die von Administratoren in Exchange Online ausgeführt werden. Protokolleinträge enthalten Informationen dazu, welches Cmdlet ausgeführt wurde, welche Parameter verwendet wurden, wer das Cmdlet ausgeführt hat und welche Objekte betroffen waren. |
| [Suche und Aufbewahrung von Postfachinhalten](https://docs.microsoft.com/exchange/security-and-compliance/in-place-ediscovery/in-place-ediscovery) | Enthält Details zu Änderungen an in-situ-eDiscovery-oder in-Place-Speichereinstellungen für Postfächer. |
| [Exportieren des administratorüberwachungsprotokolls](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/search-role-group-changes) | Das Administrator-Überwachungsprotokoll zeichnet bestimmte Verwaltungsaktionen wie erstellen, aktualisieren und löschen in Exchange Online auf. Die Ergebnisse aus dem Protokoll werden in XML exportiert, und Administratoren können dieses Protokoll an eine Gruppe von Benutzern senden. |
| [Ausführen eines Berichts zu Beweissicherungsverfahren pro Postfach](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/per-mailbox-litigation-hold-report) | Enthält Details zu Änderungen der Einstellungen für die Aufbewahrung von Rechtsstreitigkeiten in Postfächern. |
| [Anzeige und Export des externen Administratorüberwachungsprotokolls](https://docs.microsoft.com/exchange/security-and-compliance/exchange-auditing-reports/view-external-admin-audit-log) | Enthält Details zu Aktionen, die von externen Administratoren ausgeführt wurden. Die Einträge enthalten Informationen dazu, welches Cmdlet ausgeführt wurde, welche Parameter verwendet wurden, sowie Aktionen, mit denen Objekte in Exchange Online erstellt, geändert oder gelöscht werden. |

## <a name="device-compliance-reports"></a>Geräte Kompatibilitätsberichte
Sie können mobile Geräte verwalten und sichern, wenn Sie über die Office 365 Mobile Device Management (MDM) mit Ihrer Office 365-Organisation verbunden sind. Mobile Geräte wie Smartphones und Tablets, die für den Zugriff auf geschäftliche e-Mails, Kalender, Kontakte und Dokumente verwendet werden, spielen eine wichtige Rolle bei der sicherstellen, dass Mitarbeiter jederzeit und von überall aus arbeiten können. Daher ist es wichtig, dass Sie die Informationen Ihrer Organisation schützen. Sie können Office 365 MDM verwenden, um Gerätesicherheitsrichtlinien und Zugriffsregeln festzulegen und mobile Geräte zu löschen, wenn Sie verloren gehen oder gestohlen werden.

MDM-Kompatibilitätsberichte bieten eine Übersicht über Richtlinien, die von einer Organisation zur Sicherung mobiler Geräte eingerichtet wurden, die auf Office 365-Daten zugreifen. Der Bericht ermöglicht das Filtern von Geräten nach Kompatibilitätsstatus, gemeldeten Verstößen, blockierten Geräten und der Anzahl von Geräten, die als Folge von Sicherheitsrichtlinien gelöscht wurden. Weitere Informationen finden Sie unter [Übersicht über die Verwaltung mobiler Geräte für Office 365](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a).

## <a name="data-loss-prevention"></a>Verhinderung von Datenverlust
DLP-Richtlinien helfen bei der Verwaltung der Sicherheit und des Informationsflusses in einer Organisation. Sie können Richtlinien einrichten, um den Zugriff auf Inhalte zu blockieren, Daten zu verschlüsseln oder Benutzer von Richtlinien-und Richtlinienverstößen mithilfe von in-Application-DLP-Richtlinien Tipps zu benachrichtigen. DLP-Berichte bieten Einblicke in die Anzahl der Richtlinien und Regel Übereinstimmungen, Außerkraftsetzungen und falsch positive Ergebnisse.

Sie können das Office 365 Admin Center verwenden, um Informationen zur Anzahl der Nachrichten anzuzeigen, die von ihren DLP-Richtlinien im grafischen Diagramm-oder Tabellenformat erkannt werden. Die DLP-Richtlinie entspricht insbesondere für gesendete und empfangene e-Mails sowie für DLP-Regel Übereinstimmungen für gesendete und empfangene e-Mails. Sie können die Anzahl der Übereinstimmungen, Überschreibungen und falsch positiver Ergebnisse für jede Richtlinie innerhalb der letzten 24 Stunden auch mithilfe des Exchange Admin Centers anzeigen. Diese Daten sind jedoch nicht als Diagramm verfügbar. Wenn Sie einen Bericht zur Verwendung in Excel herunterladen, können Sie sogar noch mehr Details anzeigen, beispielsweise wer welche Nachricht an welchem Tag gesendet hat und welche Richtlinien Übereinstimmungen ausgelöst wurden. Weitere Informationen finden Sie unter [Anzeigen von Berichten zu DLP-Richtlinien Ermittlungen](https://technet.microsoft.com/en-us/library/jj889415(v=exchg.150).aspx).

## <a name="auditing-in-yammer-enterprise"></a>Überwachung in jammern Enterprise
Jammern Enterprise bietet Administratoren die Möglichkeit, Benutzeraktivitätsdaten aus Ihrem Jammer Netzwerk (e) über die [jammern-Datenexport-API](https://support.office.com/article/export-data-from-yammer-enterprise-b303d8f3-007d-4ad4-81f8-54fb1ecfb3f2)oder manuell über die jammern-Netzwerk Verwaltungsseite zu exportieren. Die Möglichkeit zum Exportieren von Protokollen ist auf Netzwerkadministratoren in jammern beschränkt. (Alle Office 365-globalen Administratoren sind Jammer Netzwerkadministratoren.)

Die folgenden Daten können exportiert werden:

| Filename | Description |
|----------------------------|-------------------------------------------------------------------------|
| Users. CSV | Alle neuen, ausstehenden und angehalten Benutzer im Netzwerk |
| Messages. CSV | Alle Nachrichten im Netzwerk |
| Files. CSV (Metadaten) | Metadaten wie filename, Datei-API-URL, Uploader-ID, hochgeladen bei, etc. |
| Files. CSV (Original Dateien) | ZIP-Datei der ursprünglichen Dateien, die von Benutzern in jammern hochgeladen wurden |
| Topics. CSV | Im Netzwerk erstellte Themen |
| Pages. CSV | Von Benutzern im Netzwerk erstellte Seiten (Notizen) |
| Admins. CSV | Alle überprüften Administratoren im Netzwerk |
| Networks. CSV | Alle jammern-externe Netzwerke |

*Tabelle 3-jammern Netzwerk Datendateien für den Export durch Kunden verfügbar*

Jammern Enterprise-Daten sind auch über die Office 365-Aktivitätsberichte verfügbar. Darüber hinaus arbeitet jammern aktiv an der Offenlegung zusätzlicher Protokollierung über die Office 365-Verwaltungs Aktivitäts-API und an der Möglichkeit, Daten mithilfe von Power BI zu belegen. Weitere Informationen zu diesen Features finden Sie in der [Office-Roadmap](https://fasttrack.microsoft.com/roadmap?filters=yammer) .
