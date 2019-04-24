---
title: Privilegierte Zugriffsverwaltung in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
ms.custom: Ent_Solutions
ms.assetid: ''
description: In diesem Thema erfahren Sie mehr über die Verwaltung privilegierter Zugriffsrechte in Office 365
ms.openlocfilehash: e03b615971b90e8443f73c3ec8c4cd3febe90450
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32261826"
---
# <a name="privileged-access-management-in-office-365"></a>Privilegierte Zugriffsverwaltung in Office 365

> [!IMPORTANT]
> Dieses Thema enthält Informationen zur Bereitstellung und Konfiguration von Features, die derzeit nur in Office 365 E5 und Advanced Compliance-SKUs verfügbar sind.

Privileged Access Management ermöglicht eine granulare Zugriffssteuerung über privilegierte Verwaltungsaufgaben in Office 365. Es kann dazu beitragen, Ihre Organisation vor Verstößen zu schützen, die vorhandene privilegierte Administratorkonten mit ständigem Zugriff auf vertrauliche Daten oder Zugriff auf wichtige Konfigurationseinstellungen verwenden. Die Verwaltung privilegierter Zugriffsrechte erfordert, dass Benutzer Just-in-Time-Zugriff anfordern, um erweiterte und privilegierte Aufgaben über einen umfassenden und zeitbegrenzten Genehmigungsworkflow abzuschließen. Dadurch erhält der Benutzer gerade genug Zugriff, um die Aufgabe auszuführen, ohne dass vertrauliche Daten oder wichtige Konfigurationseinstellungen gefährdet werden müssen. Das Aktivieren der privilegierten Zugriffsverwaltung in Office 365 ermöglicht es Ihrer Organisation, mit NULL stehenden Berechtigungen zu arbeiten und eine Schutzebene gegen die anstehende Sicherheitsanfälligkeit für den administrativen Zugriff bereitzustellen.

Einen schnellen Überblick über die integrierte Kunden-Lockbox und den Workflow für die Verwaltung privilegierter Zugriffsrechte finden Sie [in diesem Kunden-Lockbox-und privileged Access Management in Office 365 Video](https://go.microsoft.com/fwlink/?linkid=2066800).

## <a name="layers-of-protection"></a>Schutzebenen

Die privilegierte Zugriffsverwaltung ergänzt andere Daten-und Zugriffsschutzfunktionen in der Office 365-Sicherheitsarchitektur. Einschließlich der privilegierten Zugriffsverwaltung als Teil eines integrierten und mehrstufigen Sicherheitskonzepts, bietet ein Sicherheitsmodell, das den Schutz von vertraulichen Informationen und Office 365-Konfigurationseinstellungen maximiert. Wie im Diagramm dargestellt, basiert die Verwaltung privilegierter Zugriffsrechte auf dem Schutz der systemeigenen Verschlüsselung von Office 365-Daten und dem Sicherheitsmodell für die rollenbasierte Zugriffssteuerung von Office 365-Diensten. Bei Verwendung mit einer [Azure AD-privilegierten Identitätsverwaltung](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)bieten diese beiden Features Zugriffssteuerung mit Just-in-Time-Zugriff in unterschiedlichen Bereichen.

![MehrStufiger Schutz in Office 365](media/pam-layered-protection.png)

Die Verwaltung privilegierter Zugriffsrechte in Office 365 ist auf **Aufgaben** Ebene definiert und umfasst, während die Azure AD-privilegierte Identitätsverwaltung auf **Rollen** Ebene Schutz anwendet und mehrere Aufgaben ausführen kann. Azure AD Privileged Identity Management ermöglicht in erster Linie das Verwalten von Zugriffen für AD-Rollen und Rollengruppen, während die privilegierte Zugriffsverwaltung in Office 365 nur auf Aufgabenebene gilt.

- **Aktivieren der privilegierten Zugriffsverwaltung in Office 365, während bereits Azure AD privilegEd Identity Management verwendet wird:** Das Hinzufügen von privileged Access Management in Office 365 bietet eine weitere granulare Schicht von Schutz-und Überwachungsfunktionen für privilegierten Zugriff auf Office 365-Daten.

- **Aktivieren von Azure AD privilegEd Identity Management bei Verwendung der privilegierten Zugriffsverwaltung in Office 365:**  Durch das Hinzufügen von Azure AD Privileged Identity Management zur privilegierten Zugriffsverwaltung in Office 365 kann privilegierter Zugriff auf Daten außerhalb von Office 365, die in erster Linie durch Benutzerrollen oder Identität definiert werden, erweitert werden.  

## <a name="privileged-access-management-architecture-and-process-flow"></a>Privilegierte Zugriffs Verwaltungsarchitektur und Prozessfluss

Jeder der folgenden Prozessabläufe skizziert die Architektur des privilegierten Zugriffs und deren Interaktion mit dem Office 365-Substrat, der Office 365-Überwachung und der Exchange-Runspace.

### <a name="step-1-configure-a-privileged-access-policy"></a>Schritt 1: Konfigurieren einer privilegierten Zugriffsrichtlinie

Wenn Sie eine Richtlinie für den privilegierten Zugriff mit dem [Microsoft 365 Admin Center](https://admin.microsoft.com) oder der Exchange-Verwaltungsshell konfigurieren, definieren Sie die Richtlinie und die Berechtigungen für den privilegierten Zugriff und die Richtlinien Attribute im Office 365-Substrat. Die Aktivitäten werden im Office 365 Security and Compliance Center protokolliert. Die Richtlinie ist jetzt aktiviert und kann eingehende Anforderungen für Genehmigungen verarbeiten.

![Schritt 1: Erstellen von Richtlinien](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a>Schritt 2: Zugriffsanforderung

Im [Microsoft 365 Admin Center](https://admin.microsoft.com) oder in der Exchange-Verwaltungs-PowerShell können Benutzer Zugriff auf erhöhte oder privilegierte Aufgaben anfordern. Die privilegierte Zugriffsfunktion sendet die Anforderung an das Office 365-Substrat zur Verarbeitung anhand der konfigurierten Zugriffsrichtlinie für Berechtigungen und zeichnet die Aktivität in den Office 365 Security and Compliance Center-Protokollen auf.

![Schritt 2: Zugriffsanforderung](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a>Schritt 3: Zugriffsgenehmigung

Eine Genehmigungsanforderung wird generiert, und die ausstehende Anforderungs Benachrichtigung wird an die genehmigende Person per e-Mail gesendet. Wenn diese Berechtigung genehmigt wurde, wird die privilegierte Zugriffsanforderung als Genehmigung verarbeitet, und die Aufgabe kann abgeschlossen werden. Wenn die Aufgabe verweigert wurde, wird Sie blockiert, und dem Requestor wird kein Zugriff erteilt. Der Anforderer wird über eine e-Mail-Nachricht über die Genehmigung oder Ablehnung der Anforderung benachrichtigt.

![Schritt 3: Zugriffsgenehmigung](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a>Schritt 4: Zugriffs Verarbeitung

Für eine genehmigte Anforderung wird die Aufgabe vom Exchange-Runspace verarbeitet. Die Genehmigung wird anhand der Richtlinie über den privilegierten Zugriff überprüft und vom Office 365-Substrat verarbeitet. Alle Aktivitäten für den Vorgang werden im Office 365 Security and Compliance Center protokolliert.

![Schritt 4: Zugriffs Verarbeitung](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="what-skus-can-use-privileged-access-in-office-365"></a>Welche SKUs können privilegierten Zugriff in Office 365 verwenden?
Privilegierte Zugriffsverwaltung ist für Kunden mit Office 365 E5 und Advanced Compliance-SKUs verfügbar.

### <a name="when-will-privileged-access-support-office-365-workloads-beyond-exchange"></a>Wann wird der privilegierte Zugriff Office 365-Arbeitsauslastungen über Exchange hinaus unterstützen?
Die Verwaltung privilegierter Zugriffsrechte wird in Kürze in anderen Office 365-Arbeitsauslastungen verfügbar sein. Weitere Informationen finden Sie in der [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap) .

### <a name="my-organization-needs-more-than-30-privileged-access-policies-will-this-limit-be-increased"></a>Meine Organisation benötigt mehr als 30 privilegierte Zugriffsrichtlinien, wird diese Grenze erhöht?
Ja, die aktuelle Grenze von 30 privilegierten Zugriffsrichtlinien pro Office 365-Organisation zu erhöhen, liegt im Feature Roadmap.

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a>Muss ich ein globaler Administrator sein, um den privilegierten Zugriff in Office 365 zu verwalten?
Nein, Sie benötigen die Exchange-Rollenverwaltungsrolle für Konten, die den privilegierten Zugriff in Office 365 verwalten. Wenn Sie die Rollenverwaltungsrolle nicht als eigenständige Konto Berechtigung konfigurieren möchten, enthält die globale Administrator Rolle standardmäßig diese Rolle und kann den privilegierten Zugriff verwalten. Benutzer, die in der Gruppe der genehmigenden Personen enthalten sind, müssen kein globaler Administrator sein oder die Rolle "Rollenverwaltung" zugewiesen haben, um Anforderungen zu überarbeiten und zu genehmigen.

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a>Wie ist die privilegierte Zugriffsverwaltung in Office 365 im Zusammenhang mit der Kunden-Lockbox?
[Kunden](https://docs.microsoft.com/office365/admin/manage/customer-lockbox-requests) -Lockbox ermöglicht eine Zugriffssteuerung für Organisationen, wenn Microsoft auf Daten zugreift. Die privilegierte Zugriffsverwaltung in Office 365 ermöglicht eine granulare Zugriffssteuerung innerhalb einer Organisation für alle privilegierten Office 365-Aufgaben.

## <a name="ready-to-get-started"></a>Sind Sie bereit zu beginnen?

Starten [Sie die Konfiguration Ihrer Organisation für die Verwaltung privilegierter Zugriffsrechte](privileged-access-management-configuration.md).

## <a name="learn-more"></a>Weitere Informationen

[InterAktiver Leitfaden: überwachen und Steuern von Administratoraufgaben mit privilegierter Zugriffsverwaltung](https://content.cloudguides.com/en-us/guides/Privileged%20Access%20Management)