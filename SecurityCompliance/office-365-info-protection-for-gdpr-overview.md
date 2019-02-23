---
title: Übersicht über Office 365 Information Protection für die DSGVO
ms.author: bcarter
author: brendacarter
manager: laurawi
ms.date: 2/7/2018
ms.audience: ITPro
ms.topic: overview
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
- GDPR
ms.service: O365-seccomp
localization_priority: Priority
search.appverid:
- MET150
description: Hier erhalten Sie eine Übersicht über Office 365 Information Protection für die DSGVO. Erfahren Sie, wie Sie personenbezogene Daten ermitteln, klassifizieren, schützen und überwachen können.
ms.openlocfilehash: 7070f719698f92acf7ad885340e59c496559063a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30212705"
---
# <a name="overview-of-office-365-information-protection-for-gdpr"></a>Übersicht über Office 365 Information Protection für die DSGVO

Diese Lösung veranschaulicht, wie vertrauliche Daten, die in Office 365-Diensten gespeichert sind, geschützt werden können. Sie bietet Empfehlungen zum Ermitteln, Klassifizieren, Schützen und Überwachen von persönlichen Daten. Dabei wird die Datenschutz-Grundverordnung (DSGVO) als Beispiel verwendet, Sie können das Verfahren jedoch auch für die Einhaltung vieler anderer Bestimmungen nutzen.

Die DSGVO regelt die Erfassung, Speicherung, Verarbeitung und Freigabe von personenbezogenen Daten. Personenbezogene Daten sind unter der DSGVO allgemein als Daten definiert, die sich auf eine identifizierte oder identifizierbare natürliche Person beziehen, die Einwohner der Europäischen Union (EU) ist.

Artikel 4: Definitionen

> Als „personenbezogene Daten“ gelten alle Informationen über eine identifizierte oder identifizierbare natürliche Person („betroffene Person“). Eine identifizierbare natürliche Person ist eine Person, die direkt oder indirekt, insbesondere durch Zuordnung zu einer Kennung wie einem Namen, zu einer Kennnummer, zu Standortdaten, zu einer Online-Kennung oder zu einem oder mehreren besonderen Merkmalen identifiziert werden kann, die Ausdruck der physischen, physiologischen, genetischen, psychischen, wirtschaftlichen, kulturellen oder sozialen Identität dieser natürlichen Person sind.

Diese Lösung soll Organisationen beim Erkennen und Schützen der personenbezogenen Daten in Office 365 helfen, die möglicherweise der DSGVO unterliegen. Sie wird nicht als Nachweis für DSGVO-Compliance angeboten. Organisationen sind für die Einhaltung ihrer DSGVO selbst verantwortlich und werden angewiesen, ihre Rechts- und Compliance-Teams heranzuziehen oder Rat und Hilfe bei auf Compliance spezialisierten Drittanbietern zu suchen.

[DSGVO-Bewertung](https://assessment.microsoft.com/gdpr-compliance) ist ein kostenloses, schnelles Online-Selbstauswertungstool, mit dem Ihre Organisation ihre allgemeine Stufe der Bereitschaft zur Einhaltung der DSGVO überprüfen kann (<http://aka.ms/gdprassessment>).

## <a name="assess-and-manage-your-compliance-risk"></a>Bewerten und Verwalten Ihres Compliance-Risikos

Der erste Schritt in Richtung DSGVO-Compliance ist, zu beurteilen, ob die DSGVO für Ihre Organisation zutrifft, und wenn ja, in welchem Umfang. Bei dieser Analyse wird untersucht, welche Daten in Ihrer Organisation verarbeitet und wo sie gespeichert werden.

### <a name="step-1--use-compliance-manager-to-view-the-regulation-requirements-and-track-your-progress"></a>Schritt 1 – Verwenden des Compliance-Managers zum Anzeigen der gesetzlichen Anforderungen und zum Nachverfolgen Ihres Fortschritts

Der Compliance-Manager bietet Tools zum Nachverfolgen, Implementieren und Verwalten der Überwachungssteuerelemente, mit denen Ihre Organisation die Einhaltung verschiedener Standards, auch der DSGVO, leichter erreichen kann.

![Verwenden des Compliance-Managers zum Anzeigen von Anforderungen und zum Nachverfolgen des Fortschritts](Media/Overview-image1.png)

Weitere Informationen finden Sie unter [Verwenden des Compliance-Managers im Service Trust Portal](https://support.office.com/de-DE/article/Use-Compliance-Manager-in-the-Service-Trust-Portal-Preview-5756d342-5af9-4496-82e8-4dd50fa39942). 

### <a name="step-2--use-content-search-and-sensitive-information-types-to-find-personal-data"></a>Schritt 2 – Verwenden der Inhaltssuche und vertraulicher Informationstypen für die Suche nach personenbezogenen Daten 

Entdecken Sie personenbezogene Daten in Ihrer Umgebung, die der DSGVO unterliegen. Verwenden Sie die Inhaltssuche zusammen mit vertraulichen Informationstypen zu folgenden Zwecken:

-   Suchen und Melden des Speicherorts von personenbezogenen Daten

-   Optimieren vertraulicher Datentypen und anderer Abfragen, um alle personenbezogenen Daten in Ihrer Umgebung zu finden.

![Verwenden der Inhaltssuche und vertraulicher Informationstypen zum Suchen nach personenbezogenen Daten](Media/Overview-image2.png)

Vertrauliche Informationstypen definieren, wie bestimmte Informationstypen, z. B. Kreditkartennummern, vom automatisierten Prozess erkannt werden. Dieser Artikel enthält einen Basissatz, den Sie als Ausgangspunkt verwenden können. Weitere vertrauliche Informationstypen werden in Kürze für personenbezogene Daten in EU-Ländern verfügbar sein.

Weitere Informationen finden Sie unter [Suchen und Finden personenbezogener Daten](search-for-and-find-personal-data.md). 

## <a name="classify-protect-and-monitor-personal-data-in-office-365-and-other-saas-apps"></a>Klassifizieren, Schützen und Überwachen von personenbezogenen Daten in Office 365 und anderen SaaS-Apps

Einige der Funktionen zum Schutz von Informationen in Office 365 können auch zum Schutz vertraulicher Daten in anderen SaaS-Anwendungen verwendet werden.

![Klassifizieren, Schützen und Überwachen von personenbezogenen Daten](Media/Overview-image3.png)

Diese Abbildung wird im restlichen Abschnitt beschrieben (Schritte 3 bis 5).

### <a name="step-3--decide-if-you-want-to-use-labels-in-addition-to-sensitive-information-types"></a>Schritt 3 – Entscheiden, ob Sie zusätzlich zu vertraulichen Informationstypen Beschriftungen verwenden möchten

Vertrauliche Informationstypen sind eine Form der Klassifizierung. Unter [Erstellen eines Klassifizierungsschemas für personenbezogene Daten](architect-a-classification-schema-for-personal-data.md) finden Sie Hinweise zu der Entscheidung, ob Sie auch Beschriftungen implementieren möchten. Weitere Informationen zum Anwenden von Beschriftungen finden Sie unter [Anwenden von Beschriftungen auf personenbezogene Daten in Office 365](apply-labels-to-personal-data-in-office-365.md).

In der Abbildung gelten vertrauliche Informationstypen und Beschriftungen allgemein in Office 365. In Kürze können Sie diese mit Cloud App Security verwenden, um vertrauliche Daten in anderen SaaS-Apps wie Box und Salesforce zu finden.

### <a name="step-4--protect-personal-data-in-office-365"></a>Schritt 4 – Schützen personenbezogener Daten in Office 365 

Der Schutz personenbezogener Daten beginnt mit der Verhinderung von Datenverlust in Office 365. Es gibt mehrere andere empfohlene Funktionen für den Schutz des Zugriffs auf persönliche Daten, z. B. die Office 365-Nachrichtenverschlüsselung für E-Mail.

Diese Schutzfunktionen können auf bestimmte Datasets ausgelegt werden:

-   Berechtigungen auf Website- und Bibliotheksebene

-   Richtlinien für externe Freigabe auf Websiteebene

-   Gerätezugriffsrichtlinien auf Websiteebene

Der Schutz für den Zugriff auf Office 365 und andere Clouddienste umfasst Folgendes:

-   Identitäts- und Gerätezugriffsschutz in Enterprise Mobility + Security (EMS)

-   Privileged Access Management

-   Windows 10-Sicherheitsfunktionen

Weitere Informationen über das Anwenden von Schutzfunktionen finden Sie unter [Anwenden von Schutz auf personenbezogene Daten in Office 365](apply-protection-to-personal-data-in-office-365.md).

### <a name="step-5--monitor-for-leaks-of-personal-data"></a>Schritt 5 – Überwachen auf Lecks für personenbezogene Daten

Berichte zur Verhinderung von Datenverlust in Office 365 bieten die größtmögliche Detailebene für die Überwachung vertraulicher Daten. Sie können automatisierte Warnungen einrichten und Verletzungen mithilfe des Office 365-Überwachungsprotokolls untersuchen. Durch Cloud App Security wird die Möglichkeit zum Suchen und Überwachen vertraulicher Daten auf andere SaaS-Anbieter erweitert. Weitere Informationen zu diesen Tools finden Sie unter [Überwachen auf Verletzungen personenbezogener Daten](monitor-for-leaks-of-personal-data.md).
