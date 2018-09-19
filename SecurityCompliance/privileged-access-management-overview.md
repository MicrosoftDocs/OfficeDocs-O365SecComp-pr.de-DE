---
title: Berechtigungen zugreifen Management in Office 365
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Normal
search.appverid:
- MET150
ms.collection: Strat_O365_IP
ms.custom: Ent_Solutions
ms.assetid: ''
description: Verwenden Sie in diesem Thema erfahren Sie mehr über Berechtigungen Zugriff auf Management in Office 365
ms.openlocfilehash: 979587e68ea0cbcf255e087eaaeb38dca4fc7ca1
ms.sourcegitcommit: 0ce722533d72fa8dcc1d8a58d3c649cb345b938d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2018
ms.locfileid: "24016119"
---
# <a name="privileged-access-management-in-office-365"></a>Berechtigungen zugreifen Management in Office 365

> [!IMPORTANT]
> In diesem Thema werden die Hinweise zur Bereitstellung und Konfiguration für derzeit nur in Office 365 E5 und erweiterte Compliance-SKUs verfügbaren Features behandelt.

Access privilegierten Management ermöglicht die Differenzierte Sicherung Access Steuerung privilegierten Administratoraufgaben in Office 365.  Es kann Schützen Ihrer Organisation aus Verstöße, die vorhandenen privilegierten Administratorkonten stehende Zugriff auf vertrauliche Daten oder Zugriff auf wichtige Konfigurationseinstellungen verwenden können. Nach der Aktivierung der Verwaltung von Systemzugriff benötigen Benutzer anfordern Just-in-Time-Zugriff mit erhöhten Rechten und privilegierten über einen Genehmigungsworkflow Aufgaben, die hochgradig bezogenen und Zeit gebunden ist. Dadurch können Benutzer Just-in-ausreichend-zugreifen zum Ausführen der Aufgabe zur hand, ohne zu riskieren Belichtung vertrauliche Daten oder wichtige Konfigurationseinstellungen. Aktivieren der Systemzugriff Management in Office 365 aktivieren Ihrer Organisation mit 0 (null) stehende Berechtigungen Betrieb und stellen eine Ebene Verteidigung gegen Sicherheitslücken haftbar gemacht werden, aufgrund von solchen stehende Verwaltungszugriff bereit. 

## <a name="layers-of-protection"></a>Schutzebenen

Access privilegierten Management ergänzt, andere Daten und Access Feature Schutzmechanismen in die Sicherheitsarchitektur von Office 365. Durch die Aktivierung der Systemzugriff-Verwaltung im Rahmen des integrierten Konzepts für die Sicherheit und Schutz Ihrer Organisation, kann ein Bedeutung der mehrstufigen Sicherheitsmodell Schutz von vertraulichen Informationen und Office 365-Konfigurationseinstellungen optimieren verwendet werden. Wie in der folgenden aktivieren privilegierten dargestellt Access Management hilft basiert auf den Schutz mit systemeigenen Verschlüsselung von Office 365-Daten und der rollenbasierten Sicherheit Zugriffssteuerungsmodell von Office 365-Diensten ab. Bei Verwendung in Verbindung mit [Azure AD privilegierten Identitätsmanagement](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure)bieten diese beiden Funktionen Steuerung des Zugriffs Just-in-Time-Zugriff in anderen Bereichen.

![Bedeutung der mehrstufigen Schutz in Office 365](media/pam-layered-protection.jpg)

Access privilegierten Management in Office 365 bezogenen auf **Aufgabenebene,** während Schutz auf der Ebene der **Rolle** von Azure AD privilegierten Identitätsmanagement die Möglichkeit, mehrere Aufgaben ausführen angewendet wird und definiert werden kann.  Azure AD-Berechtigungen Identitätsmanagement in erster Linie ermöglicht die Verwaltung von Zugriffe für AD-Rollen und Rollengruppen, Berechtigungen zugreifen Management in Office 365 nur auf Aufgabenebene angewendet wird.

- **Aktivieren Berechtigungen Management in Office 365 beim bereits mit Azure AD privilegierten Identitätsmanagement zugreifen:** Hinzufügen von Systemzugriff Management in Office 365 bietet einer anderen differenzierte Schutz und Überwachung Funktionen für privilegierten Zugriff auf Office 365-Daten.

- **Aktivieren der Azure AD privilegierten Identitätsmanagement bei Verwendung von bereits privilegierten Access Management in Office 365:**  Hinzufügen von Azure AD privilegierten Identitätsmanagement zu Berechtigungen kann Access Management in Office 365 privilegierten Zugriff auf Daten außerhalb von Office 365 erweitern, die in erster Linie nach Rolle oder die Identität eines Benutzers definiert ist.  

## <a name="privileged-access-management-architecture-and-process-flow"></a>Systemzugriff Management-Architektur und dem Prozessfluss

Jeder der folgenden Prozess Datenflüsse beschreiben die Architektur von Priveleged Access und wie sie mit der Office 365-Gate, Überwachung von Office 365 und Exchange Management-Runspace interagiert.

### <a name="step-1-configuring-a-privileged-access-policy"></a>Schritt 1: Konfigurieren einer Richtlinie Systemzugriff

Beim Konfigurieren einer Richtlinie für privilegierten Zugriff über die Office 365 Admin Center oder Exchange Management PowerShell Sie erstellen und definieren Sie die Richtlinie und das Feature Systemzugriff verarbeitet die Attribute einer Richtlinie in die Office 365-Gate und die Protokolle der Aktivitäten in Office 365-Sicherheit und Compliance Center. Die Richtlinie ist nun aktiviert und bereit um zur Genehmigung eingehenden Anforderungen zu behandeln.

![Schritt 1: Erstellen von Richtlinien](media/pam-step1-policy-creation.jpg)

### <a name="step-2-access-request"></a>Schritt 2: Access Anforderung

Verwenden Sie die Office 365 Admin Center oder Exchange Management PowerShell, können Benutzer den Zugriff auf Aufgaben mit erhöhten Rechten oder Berechtigungen anfordern. Das Feature Systemzugriff sendet die Anforderung an den Office 365-Gate für die Verarbeitung der Richtlinie für den konfigurierten Berechtigungen Zugriff und zeichnet die Sctivity in die Office 365-Sicherheit und Compliance Center protokolliert.

![Schritt 2: Access-Anforderung](media/pam-step2-access-request.jpg)

### <a name="step-3-access-approval"></a>Schritt 3: Zugriffsgenehmigung

Eine Aufforderung zur Genehmigung wird generiert und die Genehmigungsgruppe per e-Mail der ausstehende Anforderung benachrichtigt wird. Wenn Genehmigung erteilt wurde, wird die Anforderung Systemzugriff als eine Genehmigung verarbeitet, und der Vorgang ist fertig gestellt werden. Wenn die Anforderung verweigert wird, Aufgabe blockieren und keinen Zugriff auf die Reqeustor erteilt wird.

![Schritt 3: zugriffsgenehmigung](media/pam-step3-access-approval.jpg)

### <a name="step-4-access-processing"></a>Schritt 4: Access-Verarbeitung

Die Aufgabe ist durch die Exchange-Verwaltung Runspace für genehmigte Anforderungen verarbeitet. Die Genehmigung ist die Richtlinie Systemzugriff abgeglichen und von der Office 365-Gate verarbeitet. Alle Aktivitäten für den Vorgang ist im Office 365-Sicherheit und Compliance Center angemeldet.

![Schritt 4: Access-Verarbeitung](media/pam-step4-access-processing.jpg)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="what-skus-do-i-need-to-use-privileged-access-in-office-365"></a>Welche SKUs Systemzugriff in Office 365 verwenden, müssen?
Access privilegierten Management in Office 365 ist derzeit nur für Kunden mit E5 und erweiterte Compliance-SKUs verfügbar.

### <a name="when-will-privileged-access-be-available-for-office-365-workloads-beyond-exchange"></a>Wann wird Systemzugriff für Office 365-Arbeitslasten außerhalb Exchange verfügbar sein?
Wir möchten dieses Feature in anderen Office 365-Arbeitslasten bald anbieten. Wenn wir zur Freigabe einer Zeitskala bereit sind, wird sie der Übersicht über die Office 365 verfügbar sein.

### <a name="do-i-need-to-be-a-global-admin-to-manage-privileged-access-in-office-365"></a>Müssen ein globaler Administrator Systemzugriff in Office 365 verwalten werden?
Müssen Sie globaler Administrator-Berechtigung zum Systemzugriff in Office 365 verwalten können. Benutzer, die in einer genehmigenden Personen Gruppe enthaltenen müssen ein globaler Administrator überprüfen und Genehmigen von Anfragen werden. 

### <a name="how-is-privileged-access-management-in-office-365-related-to-customer-lockbox"></a>Wie wird Systemzugriff Management in Office 365 im Zusammenhang mit Kunden Lockbox?
[Kunden-Lockbox](https://support.office.com/article/Office-365-Customer-Lockbox-Requests-36f9cdd1-e64c-421b-a7e4-4a54d16440a2) ermöglicht ein Maß an Steuerung des Zugriffs für Organisationen, die für den Zugriff auf Daten von ihrem Dienstanbieter, d. h. Microsoft. Access privilegierten Management in Office 365 differenzierte Zugriffssteuerung innerhalb einer Organisation für alle Office 365 privilegierten Vorgänge ermöglicht.