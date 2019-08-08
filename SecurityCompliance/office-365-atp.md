---
title: Office 365 Advanced Threat Protection
ms.author: tracyp
author: msfttracyp
manager: dansimp
ms.date: 03/28/2019
audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
- MOE150
ms.assetid: e100fe7c-f2a1-4b7d-9e08-622330b83653
ms.collection:
- M365-security-compliance
description: Office 365 Advanced Threat Protection umfasst sichere Anlagen, sichere Links, erweiterte Anti-Phishing-Tools, Reporting-Tools und Funktionen für die Threat Intelligence.
ms.openlocfilehash: ca948fdd99ca04830ecb7685ed8930a71345299f
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2019
ms.locfileid: "36231089"
---
# <a name="office-365-advanced-threat-protection"></a>Office 365 Advanced Threat Protection

> [!IMPORTANT]
> Dieser Artikel richtet sich an Geschäftskunden, die [Office 365 Advanced Threat Protection](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description)haben. Wenn Sie Outlook.com, Office 365 Home oder Office 365 Personal verwenden und nach Informationen zu sicheren Links in Outlook suchen, finden Sie weitere Informationen unter [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

## <a name="overview"></a>Übersicht

Office 365 Advanced Threat Protection (ATP) schützt Ihre Organisation vor böswilligen Bedrohungen durch e-Mail-Nachrichten, Links (URLs) und Tools für die Zusammenarbeit. ATP umfasst Folgendes:

- [Richtlinien](#configure-atp-policies)für den Schutz von Bedrohungen: definieren Sie Richtlinien zum Schutz vor Bedrohungen, um das geeignete Schutzniveau für Ihre Organisation festzulegen. 

- [Berichte](#view-atp-reports): Anzeigen von Echtzeitberichten zum Überwachen der ATP-Leistung in Ihrer Organisation. 

- [Funktionen für die Untersuchung und Reaktion](#use-threat-investigation-and-response-capabilities)auf Bedrohungen: Verwenden Sie führende Tools, um Bedrohungen zu untersuchen, zu verstehen, zu simulieren und zu verhindern. 

- [Automatisierte Ermittlungs-und Antwortfunktionen](#save-time-with-automated-investigation-and-response): sparen Sie Zeit und Aufwand bei der Untersuchung und Abwehr von Bedrohungen.

## <a name="office-365-atp-plan-1-and-plan-2"></a>Office 365 ATP-Plan 1 und Plan 2

ATP ist in Office 365 E5 enthalten; ATP-Plan 1 und ATP-Plan 2 sind jedoch jeweils als Add-on für bestimmte Abonnements verfügbar. Weitere Informationen finden Sie unter [Feature Availability Across ATP Plans](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans).

## <a name="configure-atp-policies"></a>Konfigurieren von ATP-Richtlinien

Office 365 ATP bietet zahlreiche Tools, um ein angemessenes Maß an Schutz für Ihre Organisation festzulegen. 

Das Sicherheitsteam Ihrer Organisation muss Richtlinien für jedes ATP-Tool im Office 365 Security #a0 Compliance Center definieren. Wechseln Sie zur **Bedrohungs Verwaltungs** > **Richtlinie** , um auf Richtlinienoptionen zuzugreifen. (Weitere Informationen dazu finden Sie unter [schnell Start Handbuch: Einrichten Office 365 Advanced Threat Protection](checklist-atp-setup.md).)

Die für Ihre Organisation definierten Richtlinien bestimmen das Verhalten und die Schutzebene für vordefinierte Bedrohungen. Richtlinienoptionen sind äußerst flexibel. Beispielsweise kann das Sicherheitsteam Ihrer Organisation einen abgestimmten Bedrohungsschutz auf Benutzer-, Organisations-, Empfänger-und Domänenebene festlegen. Es ist wichtig, Ihre Richtlinien regelmäßig zu überprüfen, da täglich neue Bedrohungen und Herausforderungen auftreten.  

- [ATP-sichere Anlagen](atp-safe-attachments.md): bietet einen Zero-Day-Schutz zum Schutz Ihres Messagingsystems durch Überprüfen von e-Mail-Anlagen auf böswillige Inhalte. Alle Nachrichten und Anlagen, die nicht über eine Virus/Malware-Signatur verfügen, werden an eine spezielle Umgebung weitergeleitet, und anschließend werden maschinelle Lern-und Analysetechniken zum erkennen böswilliger Absichtserklärungen verwendet. Wenn keine verdächtigen Aktivitäten gefunden werden, wird die Nachricht an das Postfach weitergeleitet. Weitere Informationen finden Sie unter [Einrichten Office 365 ATP-Richtlinien für sichere Anlagen](set-up-atp-safe-attachments-policies.md).

- [ATP-sichere Links](atp-safe-links.md): bietet eine Zeit-zu-Klick-Überprüfung von URLs, beispielsweise in e-Mails und Office-Dateien. Der Schutz wird fortgesetzt und gilt für Ihre Messaging-und Office-Umgebung. Für jeden Klick werden Links gescannt: sichere Links bleiben verfügbar und böswillige Links werden dynamisch blockiert. Weitere Informationen finden Sie unter [Einrichten Office 365 Richtlinien für ATP-sichere Links](https://docs.microsoft.com/en-us/office365/securitycompliance/set-up-atp-safe-links-policies). 

- [ATP für SharePoint, OneDrive und Microsoft Teams](atp-for-spo-odb-and-teams.md): schützt Ihre Organisation, wenn Benutzer zusammenarbeiten und Dateien freigeben, indem Sie bösartige Dateien in Teamwebsites und Dokumentbibliotheken erkennen und blockieren. Weitere Informationen finden Sie unter [Aktivieren von Office 365 ATP für SharePoint, OneDrive und Microsoft Teams](turn-on-atp-for-spo-odb-and-teams.md). 

- [ATP-Schutz vor Phishing](atp-anti-phishing.md): erkennt Versuche, die Identität von Benutzern und benutzerdefinierten Domänen zu imitieren. Sie wendet Computer Lernmodelle und erweiterte Erkennungsalgorithmen für Identitätswechsel an, um Phishing-Angriffe zu verhindern. Weitere Informationen finden Sie unter [Einrichten Office 365 ATP-Anti-Phishing-und Anti-Phishing-Richtlinien](set-up-anti-phishing-policies.md).

## <a name="view-atp-reports"></a>Anzeigen der ATP-Berichte

Office 365 ATP enthält ein erweitertes [Berichts Dashboard](view-reports-for-atp.md) zum Überwachen Ihrer ATP-Leistung. Sie können auf den **Bericht unter Reports #a0 Dashboard** im Security #a1 Compliance Center zugreifen. 

Berichte werden in Echtzeit aktualisiert und bieten Ihnen die neuesten Einblicke. Diese Berichte enthalten auch Empfehlungen und warnen vor drohenden Bedrohungen. Zu den vordefinierten Berichten zählen folgende: 

- [Threat Explorer (oder Echtzeiterkennung)](threat-explorer.md)

- [Status Bericht über den Bedrohungsschutz](view-reports-for-atp.md#threat-protection-status-report)

- [Bericht "ATP-Dateitypen"](view-reports-for-atp.md#atp-file-types-report)

- [Bericht zur ATP-Nachrichten Disposition](view-reports-for-atp.md#atp-message-disposition-report)

- ... und vieles mehr. 

## <a name="use-threat-investigation-and-response-capabilities"></a>Verwenden von Ermittlungs-und Antwortfunktionen für Bedrohungen

Office 365 ATP-Plan 2 enthält erstklassige Tools für die [Untersuchung und Reaktion auf Bedrohungen](office-365-ti.md) , mit denen das Sicherheitsteam Ihrer Organisation böswillige Angriffe antizipieren, verstehen und verhindern kann. 

- [Threat Tracker](threat-trackers.md) bieten die neuesten Informationen zu vorherrschenden Cyber-Problemen. Beispielsweise können Sie Informationen zu den neuesten Schadsoftware anzeigen und Gegenmaßnahmen ergreifen, bevor Sie eine tatsächliche Bedrohung für Ihre Organisation darstellen. Zu den verfügbaren Trackern gehören [bemerkenswerte Tracker](threat-trackers.md#noteworthy-trackers), [Trend Tracker](threat-trackers.md#trending-trackers), nachverfolgte [Abfragen](threat-trackers.md#tracked-queries)und [gespeicherte Abfragen](threat-trackers.md#saved-queries).

- [Threat Explorer (oder Echtzeiterkennung)](threat-explorer.md) (auch als Explorer bezeichnet) ist ein Echtzeitbericht, mit dem Sie die aktuellen Bedrohungen identifizieren und analysieren können. Sie können Explorer so konfigurieren, dass Daten für benutzerdefinierte Zeiträume angezeigt werden.

- Mit dem Angriffs [Simulator](attack-simulator.md) können Sie realistische Angriffsszenarien in Ihrer Organisation ausführen, um Sicherheitsrisiken zu identifizieren. Simulationen von aktuellen Arten von Angriffen sind verfügbar, einschließlich eines [Anzeigenamens Spear-Phishing-](attack-simulator.md#display-name-spear-phishing-attack)Angriffs, eines [Kenn Wort Sprüh](attack-simulator.md#password-spray-attack)Angriffs, eines [Brute-Force-Kenn Wort](attack-simulator.md#brute-force-password-attack)Angriffs und vieles mehr.
    
## <a name="save-time-with-automated-investigation-and-response"></a>Sparen Sie Zeit mit automatischer Untersuchung und Antwort

(**Neu!**) Wenn Sie einen potenziellen Cyber-Angriff untersuchen, ist die Zeit im Wesentlichen. Je schneller Sie Bedrohungen erkennen und mindern können, desto besser ist Ihre Organisation. Office 365 ATP-Plan 2 umfasst nun die Funktionen für die [Automatische Untersuchung und Reaktion (Air)](automated-investigation-response-office.md) . (Wenn Sie diese Funktionen noch nicht haben, werden Sie Sie bald mit ATP-Plan 2 haben.)

Air enthält eine Reihe von Sicherheits-Textbuch, die automatisch gestartet werden können, beispielsweise wenn eine Warnung ausgelöst wird, oder manuell, beispielsweise aus einer Ansicht im Explorer. Mit Air können Sie die Zeit und den Aufwand für Sicherheitsvorgänge bei der effektiven und effizienten Abwehr von Bedrohungen sparen. Weitere Informationen finden Sie unter [Automatische Untersuchung und Antwort (Air) mit Office 365](automated-investigation-response-office.md).

## <a name="permissions-required-to-use-atp-features"></a>Erforderliche Berechtigungen für die Verwendung von ATP-Features

Für den Zugriff auf ATP-Funktionen im Security #a0 Compliance Center müssen Sie eine entsprechende Rolle zugewiesen haben. Die folgende Tabelle enthält einige Beispiele:

|Rolle oder Rollengruppe  |Ressourcen für weitere Informationen  |
|---------|---------|
|Office 365 globaler Administrator |[Informationen zu Administratorrollen von Office 365](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles)|
|Sicherheitsadministrator |[Berechtigungen für Administrator Rollen in Azure Active Directory](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-assign-admin-roles)|
|Exchange Online Organisationsverwaltung |[Berechtigungen in Exchange Online](https://docs.microsoft.com/en-us/exchange/permissions-exo/permissions-exo) <br>und<br> [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)|

Weitere Informationen finden Sie unter:

- [Berechtigungen im Security & Compliance Center](permissions-in-the-security-and-compliance-center.md) 

- [Freigeben des Benutzerzugriffs auf das Security & Compliance Center](grant-access-to-the-security-and-compliance-center.md)

## <a name="get-office-365-atp"></a>Office 365 ATP erhalten

Office 365 ATP-Plan 2 ist in Office 365 Enterprise E5, Office 365 Education a5 und Microsoft 365 Business enthalten. Wenn Ihr Abonnement Office 365 ATP nicht umfasst, können Sie ATP-Plan 1 oder ATP-Plan 2 als Add-on für bestimmte Abonnements erwerben. Weitere Informationen finden Sie in den folgenden Ressourcen:

- Eine Liste der Abonnements, die ATP-Pläne enthalten, finden Sie unter [Office 365 Advanced Threat Protection (ATP)-Verfügbarkeit](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#office-365-advanced-threat-protection-atp-availability) .

- Eine Liste der in Plan 1 und 2 enthaltenen Features finden Sie unter [Feature Availability Across Advanced Threat Protection (ATP) Pläne](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#feature-availability-across-advanced-threat-protection-atp-plans) .

- Weitere Informationen finden Sie unter [Abrufen der richtigen Office 365 Advanced Threat Protection](https://products.office.com/exchange/advance-threat-protection#pmg-allup-content) zum Vergleichen von Plänen und zum Erwerb Office 365 ATP.

## <a name="new-features-in-office-365-atp"></a>Neue Features in Office 365 ATP

Office 365 ATP werden laufend neue Features hinzugefügt. Weitere Informationen finden Sie in den folgenden Ressourcen:

- Die [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap?filters=&searchterms=advanced%2Cthreat%2Cprotection) enthält eine Liste der neuen Features in Entwicklung und Rollout.

- Die [Office 365 Beschreibung des Advanced Threat Protection-Diensts](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp) Beschreibt Features und Verfügbarkeit in ATP-Plänen.
