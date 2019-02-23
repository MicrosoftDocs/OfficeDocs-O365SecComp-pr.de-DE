---
title: Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/20/2019
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection umfasst sichere Anlagen, sichere Links, erweiterte Anti-Phishing-Tools, Reporting-Tools und Threat Intelligence-Funktionen.
ms.openlocfilehash: 33a98781c29a6ab8a44a69922afd976ce044c09d
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220005"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

> [!IMPORTANT]
> Dieser Artikel richtet sich an Office 365 Enterprise-Kunden. Wenn Sie Outlook.com, Office 365 Home oder Office 365 Personal verwenden und weitere Informationen zu sicheren Links in Outlook benötigen, lesen Sie den Thema [erweiterte Outlook.com-Sicherheit](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

## <a name="overview"></a>Übersicht

Office 365 Advanced Threat Protection (ATP) schützt Ihre Organisation vor böswilligen Bedrohungen durch e-Mail-Nachrichten, Links (URLs) und Tools für die Zusammenarbeit. ATP umfasst:

- [Bedrohungsschutz Richtlinien](#configure-atp-policies): definieren Sie Richtlinien zum Schutz vor Bedrohungen, um die entsprechende Schutzebene für Ihre Organisation festzulegen. 

- [Berichte](#view-atp-reports): Anzeigen von Echtzeitberichten zum Überwachen der ATP-Leistung in Ihrer Organisation. 

- [Threat Intelligence-Funktionen](#utilize-threat-intelligence-capabilities): Verwenden Sie führende Tools, um Bedrohungen zu untersuchen, zu verstehen, zu simulieren und zu verhindern. 
 

## <a name="configure-atp-policies"></a>Konfigurieren von ATP-Richtlinien

Office 365 ATP bietet zahlreiche Tools, mit denen Sie einen angemessenen Schutzgrad für Ihre Organisation festlegen können. 

Das Sicherheitsteam Ihrer Organisation muss Richtlinien für jedes ATP-Tool im Office 365 Security & Compliance Center definieren. Wechseln Sie zur**Richtlinie** zur **Gefahren Verwaltung** > , um auf Richtlinienoptionen zuzugreifen. 

Die für Ihre Organisation definierten Richtlinien bestimmen das Verhalten und die Schutzebene für vordefinierte Bedrohungen. Die Richtlinienoptionen sind äußerst flexibel. Beispielsweise kann das Sicherheitsteam Ihrer Organisation einen abgestimmten Bedrohungsschutz auf Benutzer-, Organisations-, Empfänger-und Domänenebene festlegen. Es ist wichtig, Ihre Richtlinien regelmäßig zu überwachen, da neue Bedrohungen und Herausforderungen täglich entstehen.  

- [ATP Safe Attachments](atp-safe-attachments.md): bietet Zero-Day-Schutz, um Ihr Messagingsystem zu schützen, indem Sie e-Mail-Anhänge auf böswillige Inhalte überprüfen. Alle Nachrichten und Anlagen, die über keine Virus-/Malware-Signatur verfügen, werden an eine spezielle Umgebung weitergeleitet, und anschließend werden mithilfe der Computer Lern-und Analysetechniken böswillige Absichten ermittelt. Wenn keine verdächtige Aktivität gefunden wird, wird die Nachricht an das Postfach weitergeleitet. Weitere Informationen finden Sie unter [Einrichten von Office 365 ATP Safe Attachments Policies](set-up-atp-safe-attachments-policies.md).

- [ATP-sichere Links](atp-safe-links.md): ermöglicht die Überprüfung von URLs in e-Mail-Nachrichten und Office-Dateien per Mausklick. Der Schutz wird fortgesetzt und gilt für Ihre Messaging-und Office-Umgebung. Links werden für jeden Klick überprüft: sichere Links bleiben zugänglich und böswillige Links werden dynamisch blockiert. Weitere Informationen finden Sie unter [Einrichten von Office 365 ATP-Richtlinien für sichere Links](https://docs.microsoft.com/en-us/office365/securitycompliance/set-up-atp-safe-links-policies). 

- [ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md): schützt Ihre Organisation, wenn Benutzer zusammenarbeiten und Dateien freigeben, indem Sie schädliche Dateien in Teamwebsites und Dokumentbibliotheken identifizieren und blockieren. Weitere Informationen finden Sie unter [Turn on Office 365 ATP for SharePoint, OneDrive und Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md). 

- [ATP-Schutz vor Phishing](atp-anti-phishing.md): erkennt Versuche, die Identität der Benutzer und benutzerdefinierter Domänen zu imitieren. Es wendet Computer Lernmodelle und erweiterte Identitätswechsel Erkennungsalgorithmen an, um Phishing-Angriffe zu verhindern. Weitere Informationen finden Sie unter [Einrichten von Office 365-ATP-Antiphishing-und-Phishing-Richtlinien](set-up-anti-phishing-policies.md).

## <a name="view-atp-reports"></a>ATP-Berichte anzeigen

Office 365 ATP enthält ein erweitertes [Reporting-Dashboard](view-reports-for-atp.md) , um Ihre ATP-Leistung zu überwachen. Sie können auf diese unter **Berichte _GT_ Dashboard** im Security _AMP_ Compliance Center zugreifen. 

Berichte werden in Echtzeit aktualisiert, sodass Sie die neuesten Einblicke erhalten. Diese Berichte enthalten auch Empfehlungen und warnen Sie bei drohenden Bedrohungen. Zu den vorDefinierten Berichten gehören der [bedrohungSschutz Status Bericht](view-reports-for-atp.md#threat-protection-status-report), [ATP-Dateitypen](view-reports-for-atp.md#atp-file-types-report), [ATP-Nachrichten Disposition](view-reports-for-atp.md#atp-message-disposition-report) und vieles mehr. 

## <a name="utilize-threat-intelligence-capabilities"></a>Verwenden von Threat Intelligence-Funktionen

Office 365 ATP enthält Best-of-Class- [Threat Intelligence-Tools](office-365-ti.md) , mit denen das Sicherheitsteam Ihrer Organisation Vorwegnahme, verstehen und verhindern kann. 

- [Threat Tracker](threat-trackers.md) bieten die neuesten Informationen zu vorherrschenden Cyber-Problemen. Sie können beispielsweise Informationen über die neueste Schadsoftware anzeigen und Gegenmaßnahmen ergreifen, bevor Sie zu einer tatsächlichen Bedrohung für Ihre Organisation wird. Zu den verfügbaren Tracker gehört [bemerkenswerte Tracker](threat-trackers.md#noteworthy-trackers), [Trend Verfolgungs](threat-trackers.md#trending-trackers)-und Überwachungs [Abfragen](threat-trackers.md#tracked-queries)sowie [gespeicherte Abfragen](threat-trackers.md#saved-queries).

- [Explorer](use-explorer-in-security-and-compliance.md) (auch als Bedrohungs-Explorer bezeichnet) ist ein Echtzeitbericht, der es Ihnen ermöglicht, aktuelle Bedrohungen zu identifizieren und zu analysieren. Sie können Explorer so konfigurieren, dass Daten für benutzerdefinierte Zeiträume angezeigt werden.

- Mit dem anGriffs [Simulator](attack-simulator.md) können Sie realistische Angriffsszenarien in Ihrer Organisation ausführen, um Sicherheitsrisiken zu identifizieren. Es stehen Simulationen der aktuellen Angriffstypen zur Verfügung, darunter ein [Anzeigename Speer-Phishing-Angriff](attack-simulator.md#display-name-spear-phishing-attack), ein [Kenn Wort Sprüh Angriff](attack-simulator.md#password-spray-attack), ein [Brute-Force-Kennwortangriff](attack-simulator.md#brute-force-password-attack)und vieles mehr.
    
## <a name="permissions-required-to-use-atp-features"></a>Erforderliche Berechtigungen für die Verwendung von ATP-Features

Für den Zugriff auf ATP-Funktionen im Security & Compliance Center müssen Sie eine entsprechende Rolle zugewiesen sein. Die folgende Tabelle enthält einige Beispiele:

|Rolle oder Rollengruppe  |Ressourcen für weitere Informationen  |
|---------|---------|
|Office 365 globaler Administrator |[Informationen zu Administratorrollen von Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|Sicherheitsadministrator |[Berechtigungen für Administrator Rollen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Exchange Online-Organisationsverwaltung |[Berechtigungen in Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>und<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

Siehe auch:
- [Berechtigungen im Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) 

- [Gewähren von Benutzern Zugriff auf das Office 365 Security & Compliance Center](grant-access-to-the-security-and-compliance-center.md)

## <a name="get-office-365-atp"></a>Office 365 ATP abrufen

Office 365 ATP ist in Office 365 Enterprise E5, Office 365 Education a5 und Microsoft 365 Business enthalten. Wenn Ihr Abonnement nicht Office 365 ATP enthält, können Sie möglicherweise ATP als Add-on erwerben. Weitere Informationen finden Sie in den folgenden Ressourcen:

- Eine Liste der Abonnements mit ATP-Plänen finden Sie unter [Office 365 Advanced Threat Protection (ATP)](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#office-365-advanced-threat-protection-atp-availability) .

- Eine Liste der in Plan 1 und 2 enthaltenen Features finden Sie unter [Feature Availability Across Advanced Threat Protection (ATP) Pläne](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans) .

- Weitere Informationen finden Sie unter [Abrufen der richtigen office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content) zum Vergleichen von Plänen und erwerben von Office 365 ATP.

## <a name="new-features-in-office-365-atp"></a>Neue Features in Office 365 ATP

Neue Features werden Office 365 ATP kontinuierlich hinzugefügt. Weitere Informationen finden Sie in den folgenden Ressourcen:

- Die [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection) enthält eine Liste der neuen Features in der Entwicklung und Einführung.

- Die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) Beschreibt Features und Verfügbarkeit in den ATP-Plänen.
