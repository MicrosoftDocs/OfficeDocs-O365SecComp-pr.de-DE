---
title: Überwachung und Berichterstellung in Microsoft Cloud Services
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- M365-analytics
description: Eine Übersicht über Überwachungs-und Berichterstellungsfeatures in Office 365, Microsoft 365 und Service Assurance.
ms.openlocfilehash: 8e8c8612294058572dc671188ae8299bdd73b373
ms.sourcegitcommit: c7989a8ead235aaebb2503abbde598f2c26c0056
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2019
ms.locfileid: "33979461"
---
# <a name="auditing-and-reporting-in-microsoft-cloud-services"></a>Überwachung und Berichterstellung in Microsoft Cloud Services

## <a name="introduction"></a>Einführung

Microsoft Cloud Services beinhaltet verschiedene Überwachungs-und Berichtsfunktionen, die Sie zum Nachverfolgen von Benutzer-und Verwaltungsaktivitäten innerhalb des Mandanten verwenden können, Beispiele sind Änderungen an den Konfigurationseinstellungen von Exchange Online und SharePoint Online-Mandanten sowie Änderungen, die von Benutzern an Dokumenten und anderen Elementen vorgenommen wurden. Sie können Überwachungsinformationen und Berichte verwenden, die in Microsoft Cloud Services zur Verfügung stehen, um die Benutzerfreundlichkeit besser zu verwalten, Risiken zu minimieren und Compliance-Verpflichtungen zu erfüllen.

## <a name="security--compliance-centers"></a>Security & Compliance Center

Das [Office 365 Security & Compliance Center](https://protection.office.com), das [Microsoft 365-Sicherheitscenter](https://security.microsoft.com)und das [Microsoft 365 Compliance Center](https://compliance.microsoft.com) sind One-Stop-Portale zum Schutz von Daten in Ihrer Organisation, und Sie schließen viele Überwachung und Berichterstellung ein. Funktionen. Diese Center helfen Ihnen bei Ihren Datenschutz-oder Compliance-Anforderungen und überwachen Benutzer-und Administratoraktivitäten. Sie können über Ihr Abonnement Administratorkonto auf diese Center zugreifen.

Diese Center bieten Navigationsbereiche für den Zugriff auf verschiedene Funktionen:

- **Warnungen:** Ermöglicht das Verwalten von Benachrichtigungen, Anzeigen von sicherheitsbezogenen Warnungen und verwalten erweiterter Warnungen mithilfe von [Office 365 Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security).
- **Berechtigungen:** Ermöglicht Ihnen das [Zuweisen von Berechtigungen](https://support.office.com/article/Give-users-access-to-the-Office-365-Security-Compliance-Center-2cfce2c8-20c5-47f9-afc4-24b059c1bd76) wie Compliance-Administrator, eDiscovery-Manager und anderen Personen in Ihrer Organisation, damit diese Aufgaben in diesen Zentren ausführen können. Sie weisen in jedem Center Berechtigungen für die meisten Features zu, andere Berechtigungen müssen jedoch über das Exchange-Verwaltungskonsole und das SharePoint Admin Center konfiguriert werden.
- **Bedrohungs Verwaltung:** Ermöglicht Ihnen das Erstellen und Anwenden von Geräteverwaltungsrichtlinien mithilfe der [mobilen Geräteverwaltung in Office 365](https://support.office.com/article/Overview-of-Mobile-Device-Management-for-Office-365-faa7d8e5-645d-4d59-839c-c8d4c1869e4a), um DLP-Richtlinien ( [Data Loss Prevention](https://support.office.com/article/Overview-of-data-loss-prevention-policies-1966b2a7-d1e2-4d92-ab61-42efbb137f5e) ) für Ihre Organisation einzurichten, um e-Mail-Filterung, Antischadsoftware und DomainKeys zu konfigurieren. Mail (DKIM), Safe Attachments, Safe Links und OAuth apps.
- **Datenverwaltung:** Ermöglicht Ihnen, [e-Mail-oder SharePoint-Daten aus anderen Systemen in Office 365 zu importieren](https://support.office.com/article/Import-PST-files-or-SharePoint-data-to-Office-365-ba688e0a-0fcb-4bd7-8e57-2b669564ea84), [Archivpostfächer zu konfigurieren](https://support.office.com/article/Enable-archive-mailboxes-in-the-Office-365-Security-Compliance-Center-268a109e-7843-405b-bb3d-b9393b2342ce)und [Aufbewahrungsrichtlinien](https://support.office.com/article/Retention-in-the-Office-365-Security-Compliance-Center-2a0fc432-f18c-45aa-a539-30ab035c608c) für e-Mails und andere Inhalte in Ihrer Organisation festzulegen.
- **Such &-Untersuchung:** Stellt [Inhaltssuche](https://support.office.com/article/Run-a-Content-Search-in-the-Office-365-Security-Compliance-Center-61852fd9-fe8a-4880-a339-cb19ed3bff4a), [Überwachungsprotokoll](https://support.office.com/article/Search-the-audit-log-in-the-Office-365-Security-Compliance-Center-0d4d0f35-390b-4518-800e-0c7ec95e946c), Quarantäne und eDiscovery- [Fall Verwaltungs](https://support.office.com/article/Manage-eDiscovery-cases-in-the-Office-365-Security-Compliance-Center-edea80d6-20a7-40fb-b8c4-5e8c8395f6da) Tools bereit, um schnell Aktivitäten in Exchange Online-Postfächern,-Gruppen und-öffentlichen Ordnern, in SharePoint Online und OneDrive für Unternehmen durchzusetzen.
- **Berichte:** Ermöglicht den schnellen Zugriff auf [Berichte](https://support.office.com/article/Reports-in-the-Office-365-Security-Compliance-Center-7acd33ce-1ec8-49fb-b625-43bac7b58c5a) für SharePoint Online, OneDrive for Business, Exchange Online und Azure AD.
- **Dienstsicherheit:** Enthält Informationen dazu, wie Microsoft Sicherheit, Datenschutz und die Einhaltung globaler Standards für Office 365, Azure, Microsoft Dynamics CRM Online, Microsoft InTune und andere Cloud-Dienste beibehält. Enthält außerdem Zugriff auf Drittanbieter-ISO-, SOC-und andere Überwachungsberichte sowie überwachte Steuerelemente, die Details zu den verschiedenen Steuerelementen enthält, die von Drittanbieter-Auditoren von Office 365 getestet und überprüft wurden.

## <a name="service-assurance"></a>Dienstsicherheit

Viele Organisationen in regulierten Branchen unterliegen umfassenden Compliance-Anforderungen. Um eigene Risikobewertungen durchzuführen, benötigen Kunden häufig ausführliche Informationen dazu, wie Office 365 die Sicherheit und den Datenschutz Ihrer Daten beibehält. Microsoft engagiert sich für die Sicherheit und den Datenschutz von Kundendaten in seinen Cloud-Diensten und für die Erzielung von Kunden Vertrauen, indem eine transparente Ansicht seiner Vorgänge bereitgestellt wird und ein einfacher Zugriff auf unabhängige Compliance-Berichte und-Bewertungen ermöglicht wird.

Service Assurance bietet Transparenz bei Vorgängen und Informationen dazu, wie Microsoft die Sicherheit, den Datenschutz und die Konformität von Kundendaten in Office 365 beibehält. Sie umfasst Überwachungsberichte von Drittanbietern sowie eine Bibliothek mit Whitepapers, FAQs und anderen Materialien zu Office 365-Themen wie Datenverschlüsselung, Datenausfall Sicherheit, Sicherheitsvorfall Verwaltung und vieles mehr. Kunden können diese Informationen verwenden, um eigene regulatorische Risikobewertungen durchzuführen. Compliance Officers können die Rolle "Service Assurance-Benutzer" zuweisen, um Benutzern Zugriff auf die Dienstsicherheit zu gewähren. Der mandantenadministrator kann externen Benutzern wie unabhängigen Auditoren auch den Zugriff auf Informationen im Service Assurance-Dashboard über das [Microsoft Cloud Service Trust Portal](http://aka.ms/STP) (STP) bereitstellen. Ausführliche Informationen zum Zugriff auf STP finden Sie unter [Erste Schritte mit dem Service Trust Portal für Office 365 for Business, Azure und Dynamics CRM Online-Abonnements](http://aka.ms/STPHelp).

## <a name="onedrive-for-business-admin-center"></a>OneDrive for Business Admin Center

Das Microsoft OneDrive Admin Center unterstützt Sie bei der schnellen und einfachen Verwaltung der OneDrive für Business-Einstellungen Ihrer Organisation an einem zentralen Ort. Um das OneDrive Admin Center zu verwenden, ist der Zugriff auf onedrive.com erforderlich. Sie müssen auch ein globaler Administrator für Ihre Organisation oder ein benutzerdefinierter Administrator mit der SharePoint-Administratorrolle sein. Zugriff auf das OneDrive for Business Admin Center [https://admin.onedrive.com](https://admin.onedrive.com/)unter.

Zu den wichtigsten Features gehören ein Kompatibilitätsbereich, der Administratoren Links zum entsprechenden Verwaltungscenter für wichtige Szenarien wie das Durchsuchen des Überwachungsprotokolls, das Arbeiten mit DLP, Aufbewahrung, eDiscovery und Warnungen bereitstellt.

## <a name="related-links"></a>Links zu verwandten Themen

- [eDiscovery und Suchfunktionen](office-365-ediscovery-and-search-features.md)
- [Berichtsfeatures in Office 365](office-365-reporting-features.md)
- [Office 365-Verwaltungsaktivitäts-API](office-365-management-activity-api.md)
- [Office 365-Postfachmigrationen](office-365-mailbox-migrations.md)
- [Interne Protokollierung für Office 365 Engineering](office-365-internal-logging.md)