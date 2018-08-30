---
title: Überwachung und Berichte in Office 365
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
description: Eine Übersicht über die Überwachung und Berichterstellungsfeatures in Office 365 sowie Service Assurance.
ms.openlocfilehash: 055a24523260bf14220d5436dcdd010f31f5d8cd
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529729"
---
# <a name="auditing-and-reporting-in-office-365"></a>Überwachung und Berichte in Office 365

## <a name="introduction"></a>Einführung
Microsoft Cloud Services umfasst mehrere Überwachung und Berichtsfunktionen, mit denen Kunden können Benutzer und administrative Aktivitäten innerhalb ihrer Mandanten, wie Änderungen an ihre Exchange Online und SharePoint Online-Mandanten Konfigurationseinstellungen verfolgen, und Änderungen durch Benutzer Dokumente und andere Elemente. Kunden können die Überwachungsinformationen und Berichte in unsere Clouddienste verwenden, effektiver verwalten die Benutzeroberfläche, Risiken und Auflagen erfüllen.

## <a name="office-365-security--compliance-center"></a>Office 365 Security & Compliance Center
[Office 365-Sicherheit und Compliance Center](https://support.office.com/article/Go-to-the-Office-365-Security-Compliance-Center-7e696a40-b86b-4a20-afcc-559218b7b1b8) ist ein zentraler Portal zum Schutz von Daten in Office 365 und viele Überwachung und Berichterstellungsfeatures enthält. Es ist eine Weiterentwicklung von Office 365 Compliance Center. Die Sicherheit und Compliance Center eignet sich für Organisationen, in denen Daten Protection oder kompatibilitätsanforderungen oder, Benutzer und Administrator-Aktivität überwachen möchten. Die Sicherheit und Compliance Center können Sie um Compliance für alle Office 365-Daten der Organisation zu verwalten. Sie können die Sicherheit und Compliance Center unter zugreifen [http://protection.office.com](http://protection.office.com/) mit Ihrem Office 365-Admin-Konto.

Die Sicherheit und Compliance Center umfasst Navigation Bereiche, in denen Sie Zugriff auf verschiedene Funktionen bereitstellen:
- **Alerts** - können Sie Benachrichtigungen verwalten, sicherheitsbezogene Warnungen anzeigen und Verwalten von erweiterten Benachrichtigungen mit [Erweiterten Sicherheitsmanagement](https://support.office.com/article/overview-of-office-365-cloud-app-security-81f0ee9a-9645-45ab-ba56-de9cbccab475). 
- **Berechtigungen** - ermöglicht das [Zuweisen von Berechtigungen](https://support.office.com/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76) wie Administrator Compliance, eDiscovery-Manager und andere Personen in Ihrer Organisation, damit diese Aufgaben im Compliance Center & Sicherheit durchführen können. Zuweisen von Berechtigungen für die meisten Funktionen im Compliance Center & Sicherheit, aber andere Berechtigungen müssen mit der Exchange-Verwaltungskonsole und der SharePoint-Verwaltungskonsole konfiguriert werden.
- **Threat Management** – ermöglicht Ihnen das Erstellen und anwenden Gerät Informationsverwaltungsrichtlinien, die Verwendung der [Verwaltung von Office 365 mobiler Geräte](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a), zum Einrichten von Richtlinien für Ihre Organisation, zum Konfigurieren von e-Mail-Filterung [Data Loss Prevention](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e) (DLP), Anti-Malware, DomainKeys Identified Mail (DKIM), sichere Anlagen, sicheren Links und app-Berechtigungen.
- **Daten Governance** - ermöglicht das [Importieren von e-Mails oder SharePoint-Daten aus anderen Systemen in Office 365](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84), [archivpostfächer konfigurieren](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce), und Festlegen von [Aufbewahrungsrichtlinien](https://support.office.com/article/Retention-in-the-Office-365-Security-Compliance-Center-2a0fc432-f18c-45aa-a539-30ab035c608c) für e-Mails und andere Inhalte in Ihrer Organisation.
- **Suche & Untersuchung** - [Inhalte zu suchen](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), [Überwachungsprotokoll](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), Quarantäne und [eDiscovery-Fall-Verwaltung](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) Tools Aktivität schnell über Exchange Online-Postfächern, Gruppen und Öffentliche Ordner, SharePoint analysieren bereit Online und OneDrive für Unternehmen.
- **Berichte** - können Sie schnell [Berichte](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) für SharePoint Online, OneDrive für Unternehmen, Exchange Online und Azure Active Directory zugreifen.
- **Service Assurance** - enthält Informationen darüber, wie Microsoft Sicherheit, Datenschutz und Übereinstimmung mit den globalen Standards für Office 365, Azure, Microsoft Dynamics CRM Online, Microsoft Intune und andere Cloud-Dienste verwaltet. Enthält außerdem Zugriff auf Drittanbieter-ISO, SOC, und andere Überwachungsberichte sowie überwacht-Steuerelemente, die Details über die verschiedenen Steuerelemente enthält, die von Drittanbieter-Auditoren von Office 365 überprüft und getestet wurden.

## <a name="service-assurance"></a>Service-Bereitstellung
Viele unserer Kunden in regulierten Branchen wird umfassende Compliance-Bestimmungen unterliegen. Kunden benötigen, um ihre eigenen risikoauswertungen durchführen, häufig detaillierte Informationen darüber, wie Office 365 die Sicherheit und Datenschutz ihrer Daten verwaltet. Microsoft ist bestrebt, um die Sicherheit und Datenschutz von Kundendaten in die Clouddienste und Sie Kunden durch die Bereitstellung einer transparenten Ansicht der Vorgänge und einfachen Zugriff auf unabhängige Compliance-Berichte und Analysen erwerben.

Service Assurance bietet Transparenz der Vorgänge und Informationen darüber, wie Microsoft die Sicherheit, Datenschutz und Kompatibilität von Kundendaten in Office 365 verwaltet. Sie umfasst Drittanbieter-Überwachungsberichte zusammen mit einer Bibliothek, Whitepapers, häufig gestellte Fragen und anderen Materialien, die auf Office 365-Themen wie datenverschlüsselung, datenflexibilität, Sicherheit Incident Management und vieles mehr. Diese Informationen können Kunden ihre eigenen behördlichen risikoauswertungen ausführen. Compliance Officer können die Rolle "Service Assurance Benutzer" erhalten Benutzer Zugriff auf Dienst Assurance zuweisen. Der mandantenadministrator kann auch externe Benutzer, wie unabhängige Auditoren mit Zugriff auf Informationen im Dashboard Service Assurance über das [Microsoft Cloud Service vertrauen Portal](http://aka.ms/STP) (STP) bereitstellen. Weitere Informationen zum Zugriff auf das STP finden Sie auf [Erste Schritte mit der Service vertrauen Portal für Office 365 für Unternehmen, Azure und Dynamics CRM Online Abonnements](http://aka.ms/STPHelp).

## <a name="onedrive-for-business-admin-center"></a>OneDrive for Business-Verwaltungskonsole
Das neue Microsoft OneDrive Administrationscenter können Sie schnell und problemlos verwalten Ihrer Organisation OneDrive for Business-Einstellungen an einem Ort. Um der OneDrive-Verwaltungskonsole zu verwenden, müssen Sie den Zugriff auf onedrive.com zulassen. Außerdem müssen Sie ein globaler Administrator für Ihre Organisation oder einer benutzerdefinierten Admin mit der SharePoint-Administrator-Rolle sein. Zugriff auf die OneDrive for Business Admin Center Preview unter [https://admin.onedrive.com](https://admin.onedrive.com/).

Wichtige Merkmale einen Compliance-Bereich, der Administratoren mit Links zu Office 365-Sicherheit und Compliance Center für wichtige Szenarien wie das Überwachungsprotokoll suchen, arbeiten mit DLP, Aufbewahrung, eDiscovery und Warnungen bereitstellt.

## <a name="related-links"></a>Verwandte Links
- [eDiscovery und Features für die Suche](office-365-ediscovery-and-search-features.md)
- [Office 365 Reporting Features](office-365-reporting-features.md)
- [Office 365-API-Management-Aktivität](office-365-management-activity-api.md)
- [Office 365-Postfachmigration](office-365-mailbox-migrations.md)
- [Interne Protokollierung für Office 365-Entwicklung](office-365-internal-logging.md)