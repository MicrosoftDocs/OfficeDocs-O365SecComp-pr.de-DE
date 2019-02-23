---
title: Überwachung und Berichterstellung in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 12/03/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- M365-analytics
description: Eine Übersicht über Überwachungs-und Berichterstellungsfeatures in Office 365 sowie Dienstsicherheit.
ms.openlocfilehash: e2fd596279743ad72a3632ba09ec28142e9322f4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30221015"
---
# <a name="auditing-and-reporting-in-office-365"></a>Überwachung und Berichterstellung in Office 365

## <a name="introduction"></a>Einführung
Microsoft Cloud Services umfasst mehrere Überwachungs-und Berichterstattungsfeatures, mit denen Kunden Benutzer-und Verwaltungsaktivitäten innerhalb des Mandanten nachverfolgen können, beispielsweise Änderungen an den Konfigurationseinstellungen für Exchange Online und SharePoint Online-Mandanten. und Änderungen, die von Benutzern an Dokumenten und anderen Elementen vorgenommen wurden. Kunden können die in unseren Cloud-Diensten verfügbaren Überwachungsinformationen und Berichte verwenden, um die Benutzererfahrung effektiver zu managen, Risiken zu minimieren und Compliance-Verpflichtungen zu erfüllen.

## <a name="office-365-security--compliance-center"></a>Office 365 Security & Compliance Center
Das [office 365 Security _AMP_ Compliance Center](https://support.office.com/article/Go-to-the-Office-365-Security-Compliance-Center-7e696a40-b86b-4a20-afcc-559218b7b1b8) ist ein One-Stop-Portal zum Schutz Ihrer Daten in Office 365 und enthält zahlreiche Überwachungs-und Berichterstellungsfeatures. Es handelt sich um eine Weiterentwicklung des Office 365 Compliance Center. Das Security & Compliance Center wurde für Organisationen entwickelt, die Datenschutz-oder Compliance-Anforderungen erfüllen oder Benutzer-und Administratoraktivitäten überwachen möchten. Sie können das Security & Compliance Center verwenden, um die Compliance für alle Office 365-Daten Ihrer Organisation zu verwalten. Sie können auf [http://protection.office.com](http://protection.office.com/) das Security _AMP_ Compliance Center unter Verwendung ihres Office 365-Administratorkontos zugreifen.

Das Security & Compliance Center umfasst Navigationsbereiche, die Ihnen den Zugriff auf verschiedene Funktionen ermöglichen:
- **Alerts** – ermöglicht Ihnen, Warnungen zu verwalten, sicherheitsbezogene Warnungen anzuzeigen und erweiterte Warnungen mithilfe von [Office 365 Cloud App Security](https://docs.microsoft.com/en-us/Office365/SecurityCompliance/office-365-cas-overview)zu verwalten. 
- **Berechtigungen** – ermöglicht Ihnen das [Zuweisen von Berechtigungen](https://support.office.com/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76) wie Compliance-Administrator, eDiscovery-Manager und anderen Personen in Ihrer Organisation, damit diese Aufgaben im Security & Compliance Center ausführen können. Sie können Berechtigungen für die meisten Features im Security & Compliance Center zuweisen, andere Berechtigungen müssen jedoch über das Exchange Admin Center und das SharePoint Admin Center konfiguriert werden.
- **Threat Management** -ermöglicht Ihnen das Erstellen und Anwenden von Geräteverwaltungsrichtlinien mithilfe der [mobilen Geräteverwaltung in Office 365](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a), um Richtlinien zur Verhinderung von [Datenverlust](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e) (DLP) für Ihre Organisation einzurichten, um die e-Mail-Filterung zu konfigurieren. Antischadsoftware, DomainKeys Identified Mail (DKIM), Safe Attachments, Safe Links und OAuth apps.
- **Data Governance** – ermöglicht das [Importieren von E-Mails oder SharePoint-Daten aus anderen systemen in Office 365](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84), das [Konfigurieren von archivpostfächern](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)und das Festlegen von Aufbewahrungs [Richtlinien](https://support.office.com/article/Retention-in-the-Office-365-Security-Compliance-Center-2a0fc432-f18c-45aa-a539-30ab035c608c) für e-Mails und andere Inhalte in Ihrer Organisation.
- **Such &-Untersuchung** -bietet [Inhaltssuche](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), [Überwachungsprotokoll](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), Quarantäne und [eDiscovery-Fall Verwaltungs](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) Tools, um schnell Aktivitäten in Exchange Online-Postfächern,-Gruppen und-öffentlichen Ordnern, SharePoint Online und OneDrive for Business.
- **Berichte** – ermöglicht Ihnen den schnellen Zugriff auf [Berichte](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) für SharePoint Online, OneDrive for Business, Exchange Online und Azure AD.
- **Service Assurance** – bietet Informationen dazu, wie Microsoft Sicherheit, Datenschutz und die Einhaltung globaler Standards für Office 365, Azure, Microsoft Dynamics CRM Online, Microsoft InTune und andere Cloud-Dienste beibehält. Enthält außerdem Zugriff auf Drittanbieter-ISO-, SOC-und andere Überwachungsberichte sowie überwachte Steuerelemente, die Details zu den verschiedenen Steuerelementen enthält, die von Drittanbieter-Auditoren von Office 365 getestet und überprüft wurden.

## <a name="service-assurance"></a>Dienstsicherheit
Viele unserer Kunden in regulierten Branchen unterliegen umfassenden Compliance-Anforderungen. Um eigene Risikobewertungen durchzuführen, benötigen Kunden häufig ausführliche Informationen dazu, wie Office 365 die Sicherheit und den Datenschutz Ihrer Daten beibehält. Microsoft engagiert sich für die Sicherheit und den Datenschutz von Kundendaten in seinen Cloud-Diensten und für die Erzielung von Kunden Vertrauen, indem eine transparente Ansicht seiner Vorgänge bereitgestellt wird und ein einfacher Zugriff auf unabhängige Compliance-Berichte und-Bewertungen ermöglicht wird.

Service Assurance bietet Transparenz bei Vorgängen und Informationen dazu, wie Microsoft die Sicherheit, den Datenschutz und die Konformität von Kundendaten in Office 365 beibehält. Sie umfasst Überwachungsberichte von Drittanbietern sowie eine Bibliothek mit Whitepapers, FAQs und anderen Materialien zu Office 365-Themen wie Datenverschlüsselung, Datenausfall Sicherheit, Sicherheitsvorfall Verwaltung und vieles mehr. Kunden können diese Informationen verwenden, um eigene regulatorische Risikobewertungen durchzuführen. Compliance Officers können die Rolle "Service Assurance-Benutzer" zuweisen, um Benutzern Zugriff auf die Dienstsicherheit zu gewähren. Der mandantenadministrator kann externen Benutzern wie unabhängigen Auditoren auch den Zugriff auf Informationen im Service Assurance-Dashboard über das [Microsoft Cloud Service Trust Portal](http://aka.ms/STP) (STP) bereitstellen. Ausführliche Informationen zum Zugriff auf STP finden Sie unter [Erste Schritte mit dem Service Trust Portal für Office 365 for Business, Azure und Dynamics CRM Online-Abonnements](http://aka.ms/STPHelp).

## <a name="onedrive-for-business-admin-center"></a>OneDrive for Business Admin Center
Das neue Microsoft OneDrive Admin Center hilft Ihnen bei der schnellen und einfachen Verwaltung der OneDrive für Unternehmens-Einstellungen. Um das OneDrive Admin Center zu verwenden, müssen Sie den Zugriff auf onedrive.com zulassen. Sie müssen auch ein globaler Administrator für Ihre Organisation oder ein benutzerdefinierter Administrator mit der SharePoint-Administratorrolle sein. Zugriff auf die OneDrive for Business Admin Center Preview [https://admin.onedrive.com](https://admin.onedrive.com/)unter.

Zu den wichtigsten Features gehören ein Kompatibilitätsbereich, der Administratoren Links zum Office 365 Security and Compliance Center für wichtige Szenarien wie das Durchsuchen des Überwachungsprotokolls, das Arbeiten mit DLP, Aufbewahrung, eDiscovery und Warnungen bietet.

## <a name="related-links"></a>Verwandte Links
- [eDiscovery und Suchfunktionen](office-365-ediscovery-and-search-features.md)
- [Berichtsfeatures in Office 365](office-365-reporting-features.md)
- [Office 365-Verwaltungsaktivitäts-API](office-365-management-activity-api.md)
- [Office 365-Postfachmigrationen](office-365-mailbox-migrations.md)
- [Interne Protokollierung für Office 365 Engineering](office-365-internal-logging.md)