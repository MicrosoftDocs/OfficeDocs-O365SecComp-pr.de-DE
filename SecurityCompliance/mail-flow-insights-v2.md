---
title: Nachrichtenübermittlung und Einblicke im Security & Compliance Center
ms.author: chrisda
author: chrisda
manager: serdars
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: beb6acaa-6016-4d54-ba7e-3d6d035e2b46
description: Administratoren können sich über das Nachrichtenfluss-Dashboard im Security & Compliance Center informieren.
ms.openlocfilehash: c7c1a6a16c908f42098500c1015b3c3994175818
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155877"
---
# <a name="mail-flow-insights-in-the-security--compliance-center"></a>Nachrichtenübermittlung und Einblicke im Security & Compliance Center

Administratoren können das Nachrichtenfluss-Dashboard im Security & Compliance Center verwenden, um Trends, Einblicke zu ermitteln und Aktionen zum Beheben von Problemen im Zusammenhang mit dem Nachrichtenfluss in Ihrer Office 365 Organisation durchführen.

Die im e-Mail-Fluss-Dashboard verfügbaren Einblicke, Berichte und Widgets sind:

- [Nachrichtenfluss-Zuordnungsbericht](mfi-mail-flow-map-report.md)

- [Einblick in den Domänen Nachrichtenflussstatus](mfi-domain-mail-flow-status-insight.md)

- [SMTP-Authentifizierungsclients (Bericht)](mfi-smtp-auth-clients-report.md)

- [Absenderdomänen Einblicke](mfi-sender-domain-insight.md)

- [Unzustellbarkeitsbericht](mfi-non-delivery-report.md)

- [Bericht über nicht akzeptierte Domänen](mfi-non-accepted-domain-report.md)

- [Fluss eingehenden und ausgehender E-Mails](mfi-outbound-and-inbound-mail-flow.md)

- [Warteschlangenwarnungen und Warteschlangen](mfi-queue-alerts-and-queues.md)

- [Bericht über automatisch weitergeleitete Nachrichten](mfi-auto-forwarded-messages-report.md)

- [Einblick für E-Mail-Schleife](mfi-mail-loop-insight.md)

- [Einblick für langsame Nachrichtenflussregeln](mfi-slow-mail-flow-rules-insight.md)

## <a name="permissions-required-to-view-the-mail-flow-dashboard"></a>Erforderliche Berechtigungen zum Anzeigen des Nachrichtenfluss-Dashboards

Das Nachrichtenfluss-Dashboard steht für Folgendes zur Verfügung:

- Mitglieder der **globalen Administratorrolle Office 365** .

- Mitglieder Office 365 Rolle " **Exchange-Administrator** ".

- Mitglieder der **Rolle "Nachrichtenfluss-Administrator** " im Security & Compliance Center. Wenn diese Rolle explizit einem Benutzer zugewiesen ist, der kein Mitglied der globalen Administrator-oder Exchange-Administratorrolle ist:

  - Der Benutzer muss sich direkt bei [https://protection.office.com](https://protection.office.com)dem Security & Compliance Center anmelden.

  - Der Benutzer verfügt nur über eine schreibgeschützte Berechtigung für das Nachrichtenfluss-Dashboard.

  - Der Benutzer hat keinen Zugriff auf das Office 365-Verwaltungsportal.

Weitere Informationen zur Rolle Office 365 globalen Administrators finden Sie unter [Informationen zu Office 365 Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles).

Informationen zum Zuweisen von Sicherheits & Compliance Center-Rollen zu Benutzern finden Sie unter [Gewähren von Benutzern Zugriff auf das Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/grant-access-to-the-security-and-compliance-center).

## <a name="where-to-find-the-mail-flow-dashboard"></a>So finden Sie das Nachrichtenfluss-Dashboard

1. Wechseln Sie zum Security & Compliance Center unter [https://protection.office.com](https://protection.office.com).

2. Erweitern Sie **Nachrichtenfluss** , und wählen Sie dann **Dashboard**aus.

   ![Das Nachrichtenfluss-Dashboard im Office 365 Security & Compliance Center](media/mail-flow-dashboard-v2.png)
