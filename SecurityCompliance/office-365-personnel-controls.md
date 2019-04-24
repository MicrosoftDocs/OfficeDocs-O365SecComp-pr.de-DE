---
title: Personalsteuerungen in Office 365
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
description: 'Zusammenfassung: eine Übersicht über die Vorgehensweisen von Microsoft für Office 365.'
ms.openlocfilehash: b69c219ef6b405734035d74ce10195ea8cddf401
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262417"
---
# <a name="office-365-personnel-controls"></a>Personalsteuerungen in Office 365 

Das Personal Screening, das den Prozess der Überprüfung und Validierung des Verhaltens und Status einer Person in der Vergangenheit darstellt, ist eine wichtige Minderungs Kontrolle, um die Office 365-Dienst Kompromittierung zu verhindern. Während das Verhalten der Vergangenheit nicht die perfekte Voraussage für das zukünftige Verhalten einer Person ist, hilft Sie bei der Identifizierung potenzieller schlechter Darsteller. Der Personal Screening-Standard von Microsoft gilt für alle Microsoft-Mitarbeiter, Praktikanten und Kontingent Mitarbeiter, die an der Entwicklung, dem Betrieb oder der Bereitstellung von Onlinediensten für Regierungs-oder kommerzielle Cloud-Kunden beteiligt sind. Screening-Standards für nationale Cloud-Umgebungen, die nicht von Microsoft betrieben werden, werden von den Mitarbeitern des Betriebs Partners für jede spezifische Umgebung definiert.

## <a name="microsofts-personnel-screening-standard"></a>Microsoft-Personal Screening-Standard

Die Personal Screening-Methoden von Microsoft für Office 365 werden an die Unternehmensstandards von Microsoft und an die National Institute of Standards and Technology (NIST)-Steuerelemente für das Personal Screening angepasst. Microsoft-Mitarbeiter, die Zugriff auf Folgendes benötigen, unterliegen dem Microsoft-Screening-Standard:
- Physischer Zugriff auf Datencenter, Standorte, gesicherte Räume, Käfige, Server Racks oder Edge-Websites, die die Infrastruktur bereitstellen, die Onlinedienste für Kunden von Regierungs-oder kommerziellen Clouds unterstützt.
- Logischer Zugriff auf Kundendaten der Regierung oder der kommerziellen Cloud, die über bestimmte verwaltete Umgebungen bereitgestellt werden.
    - Netzwerkverwaltung der Zugriff auf Geräte und Dienste, die öffentliche oder geschäftliche Cloud-Kundendaten transportieren oder speichern.

Zu den spezifischen personellen Ereignissen, die Screening-Anforderungen auslösen, gehört Folgendes:
- Neue Microsoft-Mitarbeiter in Rollen, bei denen die Überprüfung eine definierte Anforderung ist.
- Interne Microsoft-Mitarbeiter übertragen oder wechseln zu einer vorhandenen Rolle, die derzeit eine Überprüfung als definierte Anforderung umfasst.
- Vorhandene Rollen, die den Bereich ändern, um das Screening als definierte Anforderung einzubeziehen.

## <a name="screening-enforcement-criteria"></a>Screening-Durchsetzungs Kriterien

Um sicherzustellen, dass nur autorisierte Mitarbeiter Zugriff auf Kundendaten oder Umgebungen haben, die eine Überprüfung erfordern, gelten die folgenden Durchsetzungs Kriterien:

**Nur in den USA Cloud-Umgebungen**:
- Der Zugriff auf Kundendaten oder-Umgebungen, die eine Überprüfung erfordern, muss nur zulässig sein, nachdem das Urteil abgeschlossen ist und die Screening-Anforderungen erfüllt sind.
- Microsoft-Mitarbeiter, die keinen Zugriff mehr auf Kundendaten oder Verwandte Umgebungen benötigen, müssen beim Verlassen von Microsoft oder wechseln zu einer neuen Rolle entfernt werden.
- Microsoft-Mitarbeiter müssen geschirmte Umgebungs Smartcards mit der Verwaltung verlassen, bevor Sie die USA verlassen.

**Nationale Cloud-Umgebungen**:
- Mitarbeiter des Drittanbieters oder des Datenempfängers sind für die Verwaltung und Durchsetzung des Zugriffs für nationale Cloud-Umgebungen verantwortlich.

In den Cloud-Dienstumgebungen von Microsoft ist der Zugriff auf die Rolle einer Person und die Art der betroffenen Daten beschränkt, wie in der folgenden Tabelle beschrieben. Qualifizierte oder nicht qualifizierte Mitarbeiter, die sich physisch außerhalb der USA befinden, dürfen keinen Zugriff auf Kundendaten in einer United States Cloud haben. Der Zugriff auf die nationalen Cloud-Umgebungen ist eingeschränkt, sodass Microsoft-Mitarbeiter keinen technischen Zugriff auf Kundendaten oder Systeme mit Kundendaten ohne Genehmigung durch den Drittanbieter-oder Datenverwalter haben.

| Rolle | Zugriff auf Kundendaten | Zugriff auf System Daten |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|---------------------------------|
| Qualifiziertes Personal, das sich physisch in den USA befindet | Erlaubt | Erlaubt |
| Qualifiziertes Personal außerhalb der USA | Nicht zulässig | Erlaubt |
| Internationaler Ausnahme Zugriff für Microsoft-Mitarbeiter – ermöglicht den logischen Zugriff für Microsoft-Mitarbeiter, die sich nicht in dem Land befinden, in dem die Behörden-oder Geschäftskunden Daten ruhen. | Nicht zulässig | Erlaubt |
| Nicht qualifiziertes Personal (ungeschirmtes Personal, das eine Eskorte durch qualifiziertes Personal erfordert) | Mit Autorisierung zulässig | Zulässig mit Escort-Aufsicht |


## <a name="microsoft-pre-employment-screening"></a>Microsoft Pre-Employment-Screening

In den Bereichen, in denen das lokale Recht dies zulässt, führt die globale Sicherheitsabteilung von Microsoft eine Vorprüfung durch. Dies ist eine formale Hintergrund Untersuchung, die die folgenden Kriterien umfasst:
- Eine Prüfung (z. b. für Vollständigkeit und Richtigkeit) des Lebenslaufs des Bewerbers
- Bestätigung von akademischen und beruflichen Qualifikationen
- Untersuchung eines Verlusts an beruflichen Anmeldeinformationen
- Überprüfung der letzten drei Arbeitgeber
- Eine Überprüfung der polizeilichen Aufzeichnungen wegen Kapitalverbrechen
- Bestätigung der Identität aus einer vom Staat herausgegebenen Identifizierung
- Gegebenenfalls Bonitätsprüfung

Für bestimmte Verwaltungs-, Sicherheits-oder andere Rollen, einschließlich, aber nicht beschränkt auf in der USA ansässigen Mitarbeitern in Rollen, die Zugriff auf Kundendaten benötigen, sind möglicherweise regelmäßige rescreenings und/oder zusätzliche Hintergrundprüfungen erforderlich.
Für Kontingent Mitarbeiter gibt der Vertrag mit dem Drittanbieter die Anforderungen von Microsoft für die Überprüfung an, die von dem Drittanbieter durchgeführt werden müssen. Bei Hintergrundprüfungen ist das drittanbieterunternehmen dafür verantwortlich, Microsoft zu überprüfen, ob eine Hintergrundüberprüfung durchgeführt wurde. Die Ergebnisse der Hintergrundüberprüfung werden in der Regel per e-Mail von der Personalabteilung des Drittanbieters empfangen. Internationale Mitarbeiter von Vertragsbedienstete können aufgrund von Gesetzen in Ländern, die Hintergrundprüfungen verbieten, vom Hintergrund Screening ausgeschlossen werden.

## <a name="microsoft-employment-screening"></a>Microsoft Employment Screening
Seit 2004 hat Microsoft Personen aufgefordert, einen siebenjährigen Strafregister Bildschirm für Kapitalverbrechen und Vergehen zu verabschieden, und ihre Bildungs-und Beschäftigungshistorie im Rahmen der vorarbeits Überprüfung in den USA für Mitarbeiter und Praktikanten zu überprüfen.

Vor dem Zuweisen von Microsoft-Mitarbeitern oder einem von Microsoft zugewiesenen Subunternehmer zur Bereitstellung von Office 365-bezogenen Diensten in den Vereinigten Staaten führt Microsoft die unter Auftragnehmerin durch, um eine Hintergrundprüfung durchzuführen, die aus einem sozialVersicherungs- Nummern Ablaufverfolgung und Überprüfung der Vorstrafen. Die Daten aus dieser Hintergrundüberprüfung werden als Faktor bei der Einstellungsentscheidung verwendet. Die Strafregister Überprüfung umfasst eine siebenjährige Straftat und Vergehen kriminelle Aufzeichnungen Überprüfung der Bundes-, Bundes-und County Records (soweit zutreffend).

Als Beschäftigungsbedingung müssen alle Microsoft-Mitarbeiter zum Zeitpunkt der Vermietung Vertraulichkeits-und Geheimhaltungsvereinbarungen unterzeichnen und sich vergewissern, dass Sie das Microsoft-Mitarbeiterhandbuch überprüft haben.

## <a name="microsoft-cloud-background-check"></a>Microsoft-Cloud-Hintergrundüberprüfung
Eine Microsoft-Cloud-Hintergrundüberprüfung ist erforderlich, damit Kandidaten als Mitarbeiter mit Office 365-bezogenen Diensten in den USA gemietet werden können. Microsoft-Mitarbeiter in den USA mit Zugriff auf Kundendaten müssen dem Microsoft Cloud Background Check-Prozess folgen, der von allen Office 365-Diensten benötigt wird. Außerhalb der USA variiert der Prozess. Beispielsweise verwendet die Microsoft-Cloud für Deutschland ein Daten Vertrauensnehmer-Genehmigungsmodell, mit dem sichergestellt werden soll, dass der Datenverwalter (ein deutsches Unternehmen) und nicht Microsoft die Kontrolle über den Zugriff auf Kundendaten hat. Die Microsoft-Cloud in Deutschland wird aus Rechenzentren in Deutschland geliefert, und die Operations Center (OC), die die technischen Mitarbeiter des Data Trustee enthalten, befinden sich ebenfalls in Deutschland. Sowohl das Rechenzentrum als auch die OC-Einrichtungen werden vom Datenverwalter betrieben, gewartet und gesteuert.

In der folgenden Tabelle sind die Prüfungen aufgeführt, die im Rahmen der Microsoft-Cloud-Hintergrundüberprüfung durchgeführt werden.

| Prüfung | Beschreibung |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| Suche nach sozialVersicherungsNummern | Überprüft, ob die angegebene sozialVersicherungsnummer gültig ist. |
| Überprüfen des Vorstrafenregisters | Die siebenjährigen kriminellen Datensätze überprüfen auf Schwerverbrechen und Vergehen Vergehen auf Bundes-, Landes-und Ortsebene sowie gegebenenfalls auf föderaler Ebene. |
| Office of Foreign Assets-Steuerelementliste | Department of Treasury Liste der Einzelpersonen und Organisationen, mit denen US-Bürger und dauerhafte Bewohner sind nicht berechtigt, Geschäfte zu tätigen. |
| Liste "Bureau of Industry and Security" | Department of Commerce Liste der Personen und Entitäten, die von der Teilnahme an Exportaktivitäten ausgeschlossen sind. |
| Office of Defense Trade Controls Liste der gesperrten Personen (*hinzugefügt am 2010*) | Department of State Liste der Einzelpersonen und Entitäten, die von der Teilnahme an Exportaktivitäten im Zusammenhang mit der Rüstungsindustrie ausgeschlossen sind. |


Die Ergebnisse aus der Microsoft-Cloud-Hintergrundüberprüfung werden in unserer Mitarbeiterdatenbank gespeichert, die mit unseren Datencenter-Zugriffs Steuerungssystemen verbunden ist. Wenn die Microsoft-Cloud-Hintergrundüberprüfung abläuft und der Mitarbeiter Sie nicht erneuert, wird der Zugriff auf Office 365-Dienste widerrufen und ist erst dann verfügbar, wenn die Microsoft-Cloud-Hintergrundüberprüfung erneut abgeschlossen ist. Wenn das Arbeitsverhältnis zu Microsoft beendet wird, wird ein vorhandener Datencenter Zugriff sofort widerrufen.

Die US-Staatsbürgerschaft wird für alle Mitarbeiter mit physischem oder logischem Zugriff auf die Office 365 United States Government Services verifiziert. Um die Staatsbürgerschaft zu überprüfen, treffen sich Mitarbeiter und/oder neue Kandidaten mit einem US-Staats Bürgerschafts Delegierten, der zur Überprüfung der US-amerikanischen Staatsbürgerschaft geschult ist. Mitarbeiter oder neue Bewerber müssen die erforderliche Dokumentation mitbringen und ein Bescheinigungsformular bei einer Besprechung mit der Citizenship-Stellvertretung für Ihre Region signieren. Die Besprechung muss persönlich durchgeführt werden. Sobald die Person mit der Citizenship-Stellvertretung zusammen gekommen ist und die erforderlichen Unterlagen und Signaturen bereitgestellt hat, leitet der Citizenship-Delegat eine Kopie der Dokumente an Microsoft-Mitarbeiter weiter, die die Kopie zur Aufzeichnung einreichen.

Mitarbeiter mit logischem Zugriff auf die US-amerikanische Behörden-Community-Cloud oder logischen oder physischen Zugriff auf die Azure-Angebote der US-Regierung sind erforderlich, um die Anforderungen der Bundesregierung an die [Informationen zum Strafrecht des FBI zu erfüllen. Dienste](https://www.fbi.gov/services/cjis) (CJIS), einschließlich Personal Screening. CJIS-Screening zur Unterstützung des Office 365 US Government Service umfasst eine Fingerabdruck basierte kriminelle Hintergrundprüfung, die von der CJIS-System Agentur als Juror in Staaten, die sich in Microsoft Online [registriert haben,](https://blogs.office.com/2013/10/23/california-and-microsoft-sign-cjis-security-policy-agreement/) entschieden wird. Support Programm für Dienste CJIS.
