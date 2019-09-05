---
title: Automatisches untersuchen und reagieren auf Bedrohungen in Office 365
keywords: Luft, autoIR, ATP, automatisiert, Untersuchung, Antwort, Behebung, Bedrohungen, erweitert, Bedrohung, Schutz
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 09/04/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Erste Schritte mit automatisierten Ermittlungs-und Antwortfunktionen in Office 365 Advanced Threat Protection-Plan 2.
ms.openlocfilehash: 2c64ea936170524811839db7c593d67bfe11a928
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/05/2019
ms.locfileid: "36762023"
---
# <a name="automatically-investigate-and-respond-to-threats-in-office-365"></a>Automatisches untersuchen und reagieren auf Bedrohungen in Office 365

## <a name="overview"></a>Übersicht

[Office 365 Advanced Threat Protection](office-365-atp.md) Plan 2 enthält automatisierte Ermittlungs-und Antwortfunktionen (Air), mit denen Sie die Zeit und den Aufwand für Sicherheitsvorgänge im Umgang mit Warnungen und Bedrohungen speichern können. Lesen Sie diesen Artikel, um mit der Verwendung von Air-Funktionen in Office 365 zu beginnen. Weitere Informationen zur Funktionsweise von Air finden Sie unter [Automatische Untersuchung und Antwort (Air) mit Office 365](automated-investigation-response-office.md).

Wenn bestimmte Warnungen ausgelöst werden, werden ein oder mehrere Sicherheits-Textbuch initiiert, und die automatische Untersuchung beginnt. Während und nach einem automatisierten Ermittlungsprozess können Administratoren und Sicherheitsteams folgende Aufgaben ausführen:

- [Anzeigen der Details einer Untersuchung](#view-details-of-an-investigation)

- [Überprüfen und Genehmigen von Aktionen als Ergebnis einer Untersuchung](#review-and-approve-actions) 

- [Anzeigen von Details zu einer Warnung im Zusammenhang mit einer Untersuchung](#view-details-about-an-alert-related-to-an-investigation)

> [!NOTE]
> Sie müssen ein globaler Administrator, Sicherheitsadministrator, Sicherheits Operator oder Sicherheits Leser sein, um die in diesem Artikel beschriebenen Aufgaben ausführen zu können. Weitere Informationen finden Sie unter [Microsoft 365 Security Center: Roles and Permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).

## <a name="view-details-of-an-investigation"></a>Anzeigen von Details einer Untersuchung

1. Wechseln Sie als Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser zu und melden [https://protection.office.com](https://protection.office.com) Sie sich an. Sie gelangen auf das Sicherheits #a0 Compliance Center.

2. Führen Sie einen der folgenden Schritte aus:

    - Wechseln Sie zu **Threat Management** > **Dashboard**. Dadurch gelangen Sie zum [Sicherheits Dashboard](security-dashboard.md). Die Air-Widgets werden am oberen Rand des [Sicherheits Dashboards](security-dashboard.md)angezeigt. Wählen Sie ein Widget aus, beispielsweise **Zusammenfassung der Untersuchungen**.

    - Wechseln Sie zu **Threat Management** > **Investigations**. 

    Mit beiden Methoden gelangen Sie zu einer Liste von Untersuchungen.

    ![Haupt Untersuchungs Seite für Air](media/air-maininvestigationpage.png) 

3. Wählen Sie in der Liste der Untersuchungen ein Element in der Spalte **ID** aus. Dadurch wird die Seite Ermittlungs Details geöffnet, beginnend mit dem unter Such Diagramm.

    ![Seite "Luft Untersuchungs Diagramm"](media/air-investigationgraphpage.png)

4. Verwenden Sie die verschiedenen Registerkarten, um mehr über die Untersuchung zu erfahren.

## <a name="review-and-approve-actions"></a>Überprüfen und Genehmigen von Aktionen

In Office 365 führen automatisierte Untersuchungen normalerweise zu einer oder mehreren empfohlenen Aktionen. Es werden jedoch keine Aktionen ausgeführt, bis Sie vom Sicherheits Betriebsteam genehmigt wurden. Verwenden Sie das folgende Verfahren, um Aktionen zu überprüfen und zu genehmigen.

1. Wechseln Sie als Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser zu und melden [https://protection.office.com](https://protection.office.com) Sie sich an. 

2. Wechseln Sie zu **Threat Management** > **Investigations**.

3. Wählen Sie in der Liste der Untersuchungen ein Element in der Spalte **ID** aus. 

3. Wählen Sie in der Ansicht Ermittlungs Details die Registerkarte **Aktionen** aus. Alle Aktionen, für die eine Genehmigung aussteht, werden hier aufgelistet.

4. W?hlen Sie ein Element in der Liste aus.

5. Wählen Sie **genehmigen** aus, um die empfohlene Aktion zu ergreifen (oder **ablehnen** , um die Untersuchung ohne Aktion zu schließen).

## <a name="view-details-about-an-alert-related-to-an-investigation"></a>Anzeigen von Details zu einer Warnung im Zusammenhang mit einer Untersuchung

Bestimmte Arten von Warnungen lösen eine automatische Untersuchung in Office 365 aus. Weitere Informationen finden Sie unter [Alerts](automated-investigation-response-office.md#alerts). Verwenden Sie das folgende Verfahren, um Details zu einer Warnung anzuzeigen, die einer automatisierten Untersuchung zugeordnet ist.

1. Wechseln Sie als Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser zu und melden [https://protection.office.com](https://protection.office.com) Sie sich an. Sie gelangen auf das Sicherheits #a0 Compliance Center.

2. Wechseln Sie zu **Threat Management** > **Investigations**.

3. Wählen Sie in der Liste der Untersuchungen ein Element in der Spalte **ID** aus. 

4. Wenn Details zu einer Untersuchung geöffnet sind, wählen Sie die Registerkarte **Benachrichtigungen** aus. Alle Warnungen, die die Untersuchung ausgelöst haben, werden hier aufgelistet.

5. W?hlen Sie ein Element in der Liste aus. Ein Flyout mit Details zur Warnung und Links zu zusätzlichen Informationen und Aktionen wird geöffnet.

6. Überprüfen Sie die Informationen im Flyout, und nehmen Sie abhängig von der jeweiligen Warnung eine Aktion vor, beispielsweise zum **Auflösen**, unter **drücken**oder **Benachrichtigen von Benutzern**. 

## <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a>Verwenden der API für die Office 365-Verwaltungsaktivität für benutzerdefinierte oder Drittanbieter-Berichtslösungen

Wenn Ihre Organisation eine benutzerdefinierte Berichtslösung oder eine Drittanbieter-Berichtslösung verwendet, können Sie Informationen zu automatisierten Untersuchungen in dieser Lösung mithilfe der API für die Office 365-Verwaltungsaktivität anzeigen.

Verwenden Sie die folgenden Ressourcen, um dies einzurichten:

|Ressource  |Beschreibung  |
|---------|---------|
|[Übersicht über die Office 365-Verwaltungs-APIs](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview).     |Die Office 365-Verwaltungsaktivitäts-API bietet Informationen über verschiedene Benutzer-, Verwaltungs-, System- und Richtlinienaktionen und -ereignisse aus Office 365 und Azure Active Directory-Aktivitätsprotokollen.         |
|[Erste Schritte mit den Office 365-Verwaltungs-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |Die Office 365-Verwaltungs-API verwendet Azure AD, um Authentifizierungsdienste für Ihre Anwendung bereitzustellen, um auf Office 365 Daten zuzugreifen. Führen Sie die Schritte in diesem Artikel aus, um dies einzurichten.          |
|[Office 365-Verwaltungsaktivitäts-API – Referenz](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |Sie können die Office 365-Verwaltungs Aktivitäts-API verwenden, um Informationen zu Benutzer-, Verwaltungs-, System-und Richtlinienaktionen und-Ereignissen aus Office 365-und Azure AD-Aktivitätsprotokollen abzurufen. Lesen Sie diesen Artikel, um mehr über die Funktionsweise zu erfahren.        |
|[Office 365-Verwaltungsaktivitäts-API –Schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |Erhalten Sie einen Überblick über das [allgemeine Schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) und das [Office 365 ATP-und Threat-Ermittlungs-und-Antwortschema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) , um sich über bestimmte Arten von Daten zu informieren, die über die API für die Office 365-Verwaltungsaktivität verfügbar sind.         |

## <a name="next-steps"></a>Nächste Schritte

[Weitere Informationen zu Warnungen](alert-policies.md)

[Manuelles Suchen und untersuchen schädlicher e-Mails, die in Office 365 bereitgestellt wurden](investigate-malicious-email-that-was-delivered.md)

[Informationen zu Air in Microsoft Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

[Besuchen Sie die Microsoft 365-Roadmap, um zu sehen, was bald kommt und wie Sie Rollen](https://www.microsoft.com/microsoft-365/roadmap?filters=)