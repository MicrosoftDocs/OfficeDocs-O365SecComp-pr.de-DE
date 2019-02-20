---
title: Privilegierte Zugriffsverwaltung in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: In diesem Thema erfahren Sie mehr über die Verwaltung privilegierter Zugriffsrechte in Office 365
ms.openlocfilehash: 78107ceb497a546ef4d19ba33b8b72ec1406de1b
ms.sourcegitcommit: c94cb88a9ce5bcc2d3c558f0fcc648519cc264a2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2019
ms.locfileid: "30090797"
---
# <a name="privileged-access-management-in-office-365"></a>Privilegierte Zugriffsverwaltung in Office 365

> [!IMPORTANT]
> Dieses Thema enthält Informationen zur Bereitstellung und Konfiguration von Features, die derzeit nur in Office 365 E5 und Advanced Compliance-SKUs verfügbar sind.

Privileged Access Management ermöglicht eine granulare Zugriffssteuerung über privilegierte Verwaltungsaufgaben in Office 365. Es kann dazu beitragen, Ihre Organisation vor Verstößen zu schützen, die vorhandene privilegierte Administratorkonten mit ständigem Zugriff auf vertrauliche Daten oder Zugriff auf wichtige Konfigurationseinstellungen verwenden können. Nach der Aktivierung der privilegierten Zugriffsverwaltung müssen Benutzer Just-in-Time-Zugriff anfordern, um erweiterte und privilegierte Aufgaben durch einen Genehmigungsworkflow abzuschließen, der hochgradig und Zeit gebunden ist. Dadurch erhält der Benutzer gerade genug Zugriff, um die Aufgabe auszuführen, ohne dass vertrauliche Daten oder wichtige Konfigurationseinstellungen gefährdet werden müssen. Die Aktivierung der Verwaltung privilegierter Zugriffsrechte in Office 365 ermöglicht es Ihrer Organisation, mit NULL stehenden Berechtigungen zu arbeiten und eine Schutzebene gegen Sicherheitsrisiken zu schaffen, die aufgrund eines solchen ständigen Verwaltungszugriffs entstehen.

Einen schnellen Überblick über den End-to-End-Workflow für die integrierte Kunden-Lockbox und die Verwaltung von privilegiertem Zugriff finden Sie [in diesem Kunden-Lockbox-und privilegierten Zugriffsmanagement in Office 365 Video](https://go.microsoft.com/fwlink/?linkid=2066800).

## <a name="layers-of-protection"></a>Schutzebenen

Die privilegierte Zugriffsverwaltung ergänzt andere Daten-und Zugriffsschutzfunktionen in der Office 365-Sicherheitsarchitektur. Durch die Aktivierung einer privilegierten Zugriffsverwaltung als Teil eines integrierten Ansatzes für Sicherheit und Schutz Ihrer Organisation kann ein mehrstufiges Sicherheitsmodell zum Maximieren des Schutzes vertraulicher Informationen und der Office 365-Konfigurationseinstellungen verwendet werden. Wie im folgenden Diagramm dargestellt, unterstützt die Aktivierung der Verwaltung privilegierter Zugriffsrechte den Schutz, der mit der systemeigenen Verschlüsselung von Office 365-Daten und dem Sicherheitsmodell für die rollenbasierte Zugriffssteuerung von Office 365-Diensten bereitgestellt wird. Bei Verwendung in Verbindung mit der [privilegierten Identitätsverwaltung von Azure AD](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)bieten diese beiden Features Zugriffssteuerung mit Just-in-Time-Zugriff in unterschiedlichen Bereichen.

![MehrStufiger Schutz in Office 365](media/pam-layered-protection.png)

Die Verwaltung privilegierter Zugriffsrechte in Office 365 kann auf **Aufgaben** Ebene definiert werden, während die Azure AD-privilegierte Identitätsverwaltung den Schutz auf **Rollen** Ebene mit der Möglichkeit, mehrere Aufgaben auszuführen, anwendet.  Azure AD Privileged Identity Management ermöglicht in erster Linie das Verwalten von Zugriffen für AD-Rollen und Rollengruppen, während die privilegierte Zugriffsverwaltung in Office 365 nur auf Aufgabenebene angewendet wird.

- **Aktivieren der privilegierten Zugriffsverwaltung in Office 365, während bereits Azure AD privilegEd Identity Management verwendet wird:** Das Hinzufügen von privileged Access Management in Office 365 bietet eine weitere granulare Schicht von Schutz-und Überwachungsfunktionen für privilegierten Zugriff auf Office 365-Daten.

- **Aktivieren von Azure AD privilegEd Identity Management bei Verwendung der privilegierten Zugriffsverwaltung in Office 365:**  Das Hinzufügen von Azure AD Privileged Identity Management zur privilegierten Zugriffsverwaltung in Office 365 kann den privilegierten Zugriff auf Daten außerhalb von Office 365 verlängern, die in erster Linie durch die Rolle oder Identität eines Benutzers definiert sind.  

## <a name="privileged-access-management-architecture-and-process-flow"></a>Privilegierte Zugriffs Verwaltungsarchitektur und Prozessfluss

Jeder der folgenden Prozessabläufe skizziert die Architektur des privilegiert-Zugriffs und die Interaktion mit dem Office 365-Substrat, der Office 365-Überwachung und der Exchange-Verwaltungs Runspace.

### <a name="step-1-configuring-a-privileged-access-policy"></a>Schritt 1: Konfigurieren einer privilegierten Zugriffsrichtlinie

Beim Konfigurieren einer Richtlinie für privilegierten Zugriff mit dem Office 365 Admin Center oder der Exchange Management PowerShell erstellen und definieren Sie die Richtlinie, und die privilegierte Zugriffsfunktion verarbeitet die Richtlinien Attribute im Office 365-Substrat und protokolliert die Aktivität im Office 365 Security and Compliance Center. Die Richtlinie ist jetzt aktiviert und kann eingehende Anforderungen für Genehmigungen verarbeiten.

![Schritt 1: Erstellen von Richtlinien](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a>Schritt 2: Zugriffsanforderung

Über das Office 365 Admin Center oder die Exchange-Verwaltungs-PowerShell können Benutzer Zugriff auf erhöhte oder privilegierte Aufgaben anfordern. Die privilegierte Zugriffsfunktion sendet die Anforderung an das Office 365-Substrat zur Verarbeitung anhand der konfigurierten Zugriffsrichtlinie für Berechtigungen und zeichnet die sctivity in den Office 365 Security and Compliance Center-Protokollen auf.

![Schritt 2-Zugriffsanforderung](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a>Schritt 3: Zugriffsgenehmigung

Eine Genehmigungsanforderung wird generiert, und die Genehmigungsgruppe wird per e-Mail der ausstehenden Anforderung benachrichtigt. Wenn die Genehmigung erteilt wird, wird die privilegierte Zugriffsanforderung als Genehmigung verarbeitet, und die Aufgabe kann abgeschlossen werden. Wenn die Anforderung abgelehnt wurde, wird die Aufgabe blockiert, und dem reqeustor wird kein Zugriff erteilt. Der Anforderer wird über eine e-Mail-Nachricht über die Genehmigung oder Ablehnung der Anforderung benachrichtigt.

![Schritt 3: Zugriffsgenehmigung](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a>Schritt 4: Zugriffs Verarbeitung

Für genehmigte Anforderungen wird die Aufgabe vom Exchange-Runspace verarbeitet. Die Genehmigung wird anhand der Richtlinie über den privilegierten Zugriff überprüft und vom Office 365-Substrat verarbeitet. Alle Aktivitäten für den Vorgang werden im Office 365 Security and Compliance Center protokolliert.

![Schritt 4: Zugriffs Verarbeitung](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="what-skus-do-i-need-to-use-privileged-access-in-office-365"></a>Welche SKUs benötige ich für den privilegierten Zugriff in Office 365?
Die Verwaltung privilegierter Zugriffsrechte ist derzeit nur für Kunden mit Office 365 E5 und Advanced Compliance-SKUs verfügbar.

### <a name="when-will-privileged-access-be-available-for-office-365-workloads-beyond-exchange"></a>Wann wird der privilegierte Zugriff für Office 365-Arbeitsauslastungen über Exchange hinaus verfügbar sein?
Diese Funktion wird in Kürze in anderen Office 365-Arbeitsauslastungen angeboten. Wenn wir bereit sind, eine Zeitachse freizugeben, steht Sie über die [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap)zur Verfügung.

### <a name="my-organization-needs-more-than-30-privileged-access-polices-will-this-limit-be-increased"></a>Meine Organisation benötigt mehr als 30 privilegierte Zugriffsrichtlinien, wird diese Grenze erhöht?

Wir planen, die aktuelle Grenze von 30 privilegierten Zugriffsrichtlinien pro Office 365-Organisation bald zu verlängern.

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a>Muss ich ein globaler Administrator sein, um den privilegierten Zugriff in Office 365 zu verwalten?
Nein, Sie müssen den Konten, die den privilegierten Zugriff in Office 365 verwalten, die Exchange-Rollenverwaltungsrolle zugewiesen haben. Die globale Administrator Rolle enthält jedoch standardmäßig diese Rolle und kann zum Verwalten des privilegierten Zugriffs verwendet werden, wenn Sie die Rollenverwaltungsrolle nicht als eigenständige Konto Berechtigung konfigurieren möchten. Benutzer, die in der Gruppe der genehmigenden Personen enthalten sind, müssen kein globaler Administrator sein oder die Rolle "Rollenverwaltung" zugewiesen haben, um Anforderungen zu überarbeiten und zu genehmigen. 

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a>Wie ist die privilegierte Zugriffsverwaltung in Office 365 im Zusammenhang mit der Kunden-Lockbox?
[Kunden](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) -Lockbox ermöglicht eine Zugriffssteuerung für Organisationen für den Zugriff auf Daten durch Ihren Dienstanbieter, also Microsoft. Die privilegierte Zugriffsverwaltung in Office 365 ermöglicht eine granulare Zugriffssteuerung innerhalb einer Organisation für alle privilegierten Office 365-Aufgaben.
