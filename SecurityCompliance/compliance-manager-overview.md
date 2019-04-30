---
title: Übersicht über den Microsoft Compliance-Manager
ms.author: robmazz
author: robmazz
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
description: Microsoft Compliance Manager ist ein kostenloses Workflow basiertes Risiko Bewertungstool im Microsoft Service Trust-Portal. Mit Compliance-Manager können Sie behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services nachverfolgen, zuweisen und überprüfen.
ms.openlocfilehash: a2f59eac63f8bbef98da09c2149e49ec32e56b77
ms.sourcegitcommit: 696c1ed6b270be3f9da7395b49a7d8fec98e6db0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/29/2019
ms.locfileid: "33473102"
---
# <a name="microsoft-compliance-manager-preview"></a>Microsoft Compliance-Manager (Vorschau)

> [!IMPORTANT]
> Der Compliance-Manager ist nicht in Office 365, betrieben von 21Vianet, Office 365 Deutschland, Office 365 US Government Community High (GCC) High oder Office 365 Department of Defense verfügbar.

[Microsoft Compliance Manager (Preview)](https://servicetrust.microsoft.com/ComplianceManager) ist ein kostenloses Workflow basiertes Risiko Bewertungstool, mit dem Sie behördliche Compliance-Aktivitäten im Zusammenhang mit Microsoft Cloud Services verfolgen, zuweisen und überprüfen können. Als Teil Ihres Microsoft 365-, Office 365-oder Azure Active Directory-Abonnements unterstützt Compliance Manager Sie bei der Verwaltung der Compliance im Rahmen des gemeinsamen Verantwortungs Modells für Microsoft Cloud Services. Compliance-Manager bietet ein zentrales Dashboard zum Anzeigen von Standards, Vorschriften und zur Steuerung der Implementierungsdetails und Testergebnisse für Microsoft-Dienst Bewertungen. Sie enthält außerdem Tools, mit denen Sie benutzerdefinierte Steuerelement Implementierungen und Compliance-Tracking für Ihre Organisation verwalten können.

Mit Compliance-Manager kann Ihre Organisation:
  
- Kombinieren Sie detaillierte Compliance-Informationen, die von Microsoft für Auditoren und Aufsichtsbehörden zu ihren Cloud-Diensten bereitgestellt werden, mit Ihrer Compliance-Self-Assessment für die für Ihre Organisation geltenden Standards und Vorschriften. Hierzu gehört auch die von der internationalen Organisation für Normung (ISO), dem National Institute of Standards and Technology (NIST), dem Krankenversicherungs-und Verantwortlichkeits Gesetz (HIPAA), den allgemeinen Daten Schutzverordnung (DSGVO) und viele andere.
- Sie können Compliance-und bewertungsbezogene Aktivitäten zuweisen, nachverfolgen und aufzeichnen, die Ihrer Organisation helfen, über Team Barrieren zu verfügen, um Ihre Compliance-Ziele zu erreichen.
- Stellen Sie einen Kompatibilitäts Faktor zur verFügung, mit dem Sie Ihren Fortschritt nachverfolgen und Überwachungssteuerelemente priorisieren können, die die Risikoanfälligkeit Ihrer Organisation verringern.
- Bereitstellen eines sicheren Repositorys zum Hochladen und Verwalten von nachweisen und anderen Artefakten im Zusammenhang mit ihren Compliance-Aktivitäten.
- Erstellen Sie detaillierte Microsoft Excel-Berichte, die Compliance-Aktivitäten von Microsoft und Ihrer Organisation für Auditoren, Regulierer und andere Compliance-Prüfer dokumentieren.

> [!NOTE]
> Die im Compliance-Manager bereitgestellten Kundenaktionen sind Empfehlungen; Es ist Ihre Organisation, die Wirksamkeit dieser Empfehlungen in ihrem jeweiligen regulatorischen Umfeld vor der Implementierung zu bewerten. Empfehlungen im Compliance-Manager sollten nicht als Garantie für die Compliance interpretiert werden.

## <a name="compliance-manager-relationships"></a>Compliance-Manager-Beziehungen

Der Compliance-Manager verwendet mehrere Komponenten, die Ihnen bei Ihrer Compliance-Verwaltung helfen. Diese Komponenten arbeiten zusammen, um einen vollständigen Verwaltungsablauf und problemlose Compliance-Berichte für Auditoren bereitzustellen.

Das Diagramm zeigt die Beziehungen zwischen den primären Komponenten von Compliance-Manager:

![Beziehungen im Compliance-Manager Version 3](media/compliance-manager-relationships.png)

## <a name="groups"></a>Gruppen

[Gruppen](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#groups) sind Container, mit denen Sie Bewertungen organisieren und allgemeine Informationen und Workflowaufgaben Zwischenbewertungen mit den gleichen oder verwandten vom Kunden verwalteten Steuerelementen freigeben können. Wenn zwei verschiedene Bewertungen in derselben Gruppe ein vom Kunden verwaltetes Steuerelement verwenden, wird der Abschluss der Implementierungsdetails, Tests und Status für das Steuerelement automatisch mit demselben Steuerelement in jeder anderen Bewertung in der Gruppe synchronisiert. Dadurch werden die zugewiesenen Aktionselemente für jedes Steuerelement in der gesamten Gruppe zusammengeführt und die Duplizierungs Arbeit reduziert. Sie können auch Gruppen zum Organisieren verwenden. Bewertungen nach Jahr, Bereich, Kompatibilitätsstandard oder anderen Gruppierungen zur Unterstützung der Organisation Ihrer Compliance-Arbeit.

## <a name="assessments"></a>Bewertungen

[Bewertungen](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#assessments) sind Container, mit denen Sie Steuerelemente basierend auf Zuständigkeiten von Microsoft und Ihrer Organisation für die Bewertung von Cloud Service-Sicherheits-und Compliance-Risiken organisieren können. Bewertungen unterstützen Sie bei der Implementierung von Datenschutzgarantien, die durch einen Compliance-Standard und entsprechende Datenschutzstandards,-Vorschriften oder-Gesetze festgelegt sind. Sie unterstützen Sie dabei, Ihre Datenschutz-und Compliance-Haltung gegenüber dem ausgewählten Branchenstandard für den ausgewählten Microsoft-clouddienst zu erkennen. Bewertungen werden durch die Implementierung von Steuerelementen in der Bewertung abgeschlossen, die einem Zertifizierungsstandard zugeordnet ist.

Standardmäßig erstellt Compliance-Manager die folgenden Bewertungen für Ihre Organisation:

- Office 365 ISO 27001
- Office 365 NIST 800-53
- Office 365 DSGVO

Bewertungen sind mehrere Komponenten:
  
- **In-Scope Services**: jede Bewertung gilt für eine bestimmte Gruppe von Microsoft-Diensten.
- Von **Microsoft verwaltete Steuerelemente**: für jeden clouddienst implementiert und verwaltet Microsoft eine Reihe von Konformitätskontrollen für entsprechende Standards und Vorschriften.
- Vom **Kunden verwaltete Steuerelemente**: Dies ist die Sammlung von Steuerelementen, die von Ihrer Organisation implementiert werden, wenn Sie Aktionen für jedes Steuerelement ausführen.
- **Bewertungsergebnis**: der Prozentsatz der Gesamtpunktzahl für vom Kunden verwaltete Steuerelemente in der Bewertung. Auf diese Weise können Sie die Implementierung der jedem Steuerelement zugewiesenen Aktionen nachverfolgen.

## <a name="controls"></a>Steuerelemente

[Steuerelemente](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#controls-and-actions) sind Compliance-Prozesscontainer im Compliance-Manager, die definieren, wie Sie Compliance-Aktivitäten verwalten. Diese Steuerelemente sind in Steuerelementfamilien gegliedert, die mit der Bewertungsstruktur für entsprechende Zertifizierungen oder Vorschriften übereinstimmen.

- **Steuerelement-ID**: der Name des ausgewählten Steuerelements aus der entsprechenden Zertifizierung oder Verordnung.
- **Steuerelement Titel**: der Titel für die Steuerelement-ID aus der entsprechenden Zertifizierung oder Verordnung.
- **Artikel-ID**: Dieses Feld ist nur für dsgvo-Bewertungen und gibt die entsprechende dsgvo-Artikelnummer an.
- **Beschreibung**: Text der Kontrolle aus der entsprechenden Zertifizierung oder Verordnung. Aufgrund von Copyright-Einschränkungen ist ein Link zu relevanten Informationen für ISO-Standards aufgeführt.

![Steuerelemente in Compliance-Manager Version 3](media/compliance-manager-controls.png)

Es gibt drei Arten von Steuerelementen in Compliance-Manager, von **Microsoft verwaltete Steuer**Elemente, vom **Kunden verwaltete**steuerElemente und **freigegebene Verwaltungs Steuer** Elemente.

### <a name="microsoft-managed-controls"></a>Von Microsoft verwaltete Steuerelemente

Für jeden Cloud-Dienst implementiert und verwaltet Microsoft eine Reihe von Steuerelementen im Rahmen der Einhaltung verschiedener Standards und Vorschriften durch Microsoft. Jedes Steuerelement enthält Details dazu, wie Microsoft das Steuerelement implementiert hat und wie und wann diese Implementierung von Microsoft und/oder von einem unabhängigen Drittanbieter-Prüfer getestet und validiert wurde.

### <a name="customer-managed-controls"></a>Vom Kunden verwaltete Steuerelemente

Dies ist die Sammlung von Steuerelementen, die von Ihrer Organisation verwaltet werden. Ihre Organisation ist für die Implementierung von Kunden verwalteten Steuerelementen im Rahmen ihres Compliance-Prozesses für einen bestimmten Standard oder eine bestimmte Regelung verantwortlich. Vom Kunden verwaltete Steuerelemente werden in Steuerelementfamilien für die entsprechende Zertifizierung oder Regulierung organisiert. Verwenden Sie die vom Kunden verwalteten Steuerelemente, um die empfohlenen Aktionen zu implementieren, die von Microsoft im Rahmen ihrer Compliance-Aktivitäten vorgeschlagen wurden. Ihre Organisation kann in jedem vom Kunden verwalteten Steuerelement die Anleitungen und empfohlenen Kundenaktionen verwenden, um den Implementierungs-und Bewertungsprozess für dieses Steuerelement zu verwalten.

Von Kunden verwaltete Steuerelemente in Bewertungen verfügen außerdem über integrierte Workflow Verwaltungsfunktionen, mit denen Sie Ihre Fortschritte bei der Bewertung abschließen können. Mit dieser Workflow-Funktionalität können Sie Folgendes tun:

- Zuweisen von Aktionselementen für jedes Steuerelement
- NachVerfolgen von zugewiesenen Aktionselementen
- Hochladen von nachweisen der Implementierung des Steuerelements
- Dokumentieren des Tests und der Validierung des Steuerelements
- Kennzeichnen der Aktionselemente als implementiert und getestet

Beispielsweise weist ein Compliance Officer in Ihrer Organisation einem IT-Administrator ein Aktionselement mit der Verantwortung und den erforderlichen Berechtigungen zum Ausführen der empfohlenen Aktion zu. Der IT-Administrator lädt den Nachweis der Implementierungsaufgaben hoch (Screenshots der Konfigurations-oder Richtlinieneinstellungen) und weist das Aktionselement nach Abschluss des Compliance-Verantwortlichen zurück. Der Compliance Officer wertet den gesammelten Nachweis aus, testet die Implementierung des Steuerelements und zeichnet das Implementierungsdatum und die Testergebnisse im Compliance-Manager auf.

### <a name="shared-management-controls"></a>FreigeGebene Verwaltungssteuerelemente

Ein freigegebenes Steuerelement bezieht sich auf alle Steuerelemente, bei denen sowohl Microsoft als auch Kunden Verantwortlichkeiten zur Implementierung teilen. Beispielsweise erfordern Steuerelemente im Zusammenhang mit Personal Screening, Konto-und Kennwortverwaltung und Verschlüsselung Aktionen sowohl von Microsoft als auch von Kunden.

## <a name="action-items"></a>Aktionselemente

[Aktionselemente](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#controls-and-actions) sind in vom Kunden verwaltete Steuerelemente als Teil der integrierten Workflow Verwaltungsfunktionalität enthalten, mit deren Hilfe Sie Ihre Fortschritte bei der Bewertung abschließen können.

Personen in Ihrer Organisation können Compliance-Manager verwenden, um die vom Kunden verwalteten Steuerelemente aus allen Bewertungen zu überarbeiten, denen Sie zugeordnet sind. Wenn sich ein Benutzer beim Compliance-Manager anmeldet und das Dashboard " **Aktionselemente** " öffnet, wird eine Liste der Ihnen zugewiesenen Aktionselemente angezeigt. Je nach der dem Benutzer zugewiesenen Compliance-Manager-Rolle können Sie Implementierungs-oder Testdetails bereitstellen, den Status aktualisieren oder Aktionselemente zuweisen.

Zertifizierungs Kontrollen werden in der Regel von einer Person implementiert und von einem anderen getestet. Wenn beispielsweise Aktionselemente, die einer Person zunächst für die Implementierung zugewiesen wurden, abgeschlossen sind, werden der nächsten Person Aktionselemente zum Testen und Hochladen von beweisen zugewiesen. Jeder Benutzer mit ausreichenden Berechtigungen für Steuer Zuweisungen kann Aktionselemente zuweisen und erneut zuweisen. Dies ermöglicht die zentrale Verwaltung von Steuerungs Zuweisungen und das dezentrale Routing von Aktionselementen zwischen Implementierern und Testern.

## <a name="permissions"></a>Berechtigungen

Der Compliance-Manager verwendet ein [Berechtigungsmodell](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#permissions)für die rollenbasierte Zugriffssteuerung. Standardmäßig verfügt jeder in Ihrer Organisation mit Azure Active Directory (Azure AD) über Vollzugriff und kann beliebige Aktionen im Compliance-Manager ausführen. Sobald die rollenbasierte Zugriffssteuerung von Ihrer Organisation implementiert wurde, wird jedem Benutzer, der keiner definierten Compliance-Manager-Rolle zugewiesen ist, der Gastzugriff zugewiesen. Microsoft-Dienstmitarbeiter haben keinen ständigen Zugriff auf Daten, die Sie eingeben oder hochladen.

Um die Standardberechtigungen zu ändern und ein vollständig rollenbasiertes Zugriffssteuerungsmodell zu implementieren, muss jeder Compliance-Manager-Rolle mindestens ein Benutzer hinzugefügt werden. Nachdem ein Benutzer einer Rolle hinzugefügt wurde, werden die Berechtigungen zum Ausführen der dieser Rolle zugewiesenen Aktionen aus dem Standardsatz von Berechtigungen entfernt, die allen Benutzern zur Verfügung stehen. Nur Benutzer, die mit der Rolle bereitgestellt werden, können auf den Compliance-Manager zugreifen und die von dieser Rolle zugelassenen Aktionen ausführen.

Wenn Sie beispielsweise der Rolle einen Benutzer hinzufügen, um Bewertungen zu verwalten, können nur Mitglieder dieser Rolle Bewertungen verwalten. Wenn Sie der Rolle keinen Benutzer hinzufügen, der Benutzern das Lesen der Daten in Bewertungen ermöglicht, können alle Benutzer in Ihrer Organisation auf Compliance-Manager zugreifen und bei jeder Bewertung Daten lesen.
  
## <a name="manage-evidence"></a>Beweise verwalten

Compliance-Manager kann Beweise für Ihre Implementierungsaufgaben zum Durchführen von Tests und Validierungen von vom Kunden verwalteten Steuerelementen speichern. Der Nachweis umfasst Dokumente, Tabellenkalkulationen, Screenshots, Bilder, Skripts, Skriptausgabe Dateien und andere Dateien. Compliance-Manager erhält auch automatisch Telemetrie und erstellt einen Evidence Record für Aktionselemente, die mit Secure Score integriert sind. Alle Daten, die als Beweismittel in Compliance Manager hochgeladen werden, werden in den Vereinigten Staaten auf Microsoft Cloud-Speicher Standorten gespeichert. Diese Daten werden über Azure-Regionen in Südostasien und Westeuropa repliziert.

## <a name="templates"></a>Vorlagen

Compliance-Manager stellt vorkonfigurierte [Vorlagen](https://docs.microsoft.com/office365/securitycompliance/working-with-compliance-manager#templates) für Bewertungen bereit und ermöglicht Ihnen das Erstellen benutzerdefinierter Vorlagen für vom Kunden verwaltete Steuerelemente für Ihre Compliance-Anforderungen. Neue Vorlagen werden erstellt, indem Steuerelementinformationen aus einer Excel-Datei importiert werden, oder Sie können eine Vorlage aus einer Kopie einer vorhandenen Vorlage erstellen.

Die im Compliance-Manager enthaltenen vorkonfigurierten Vorlagen sind:
 
- [ISO 27001:2013](https://www.iso.org/obp/ui/#iso:std:iso-iec:27001:ed-2:v1:en)
- [ISO 27018:2019](https://www.iso.org/obp/ui/#iso:std:iso-iec:27018:ed-2:v1:en)
- [NIST 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-4/final)
- [NIST 800-171](https://csrc.nist.gov/publications/detail/sp/800-171/rev-1/final)
- [NIST Cyber Framework (CSF)](https://www.nist.gov/cyberframework)
- [Cloud Security Alliance (CSA) Cloud Control Matrix (CCM) 3.0.1](https://cloudsecurityalliance.org/working-groups/cloud-controls-matrix/#_overview)
- [Informations Sicherheitsbroschüre des Federal Financial Institutions Examination Council (FFIEC)](https://ithandbook.ffiec.gov/it-booklets/information-security.aspx) 
- [HIPAA](https://www.hhs.gov/hipaa/for-professionals/index.html) / -[HITECH](https://www.hhs.gov/hipaa/for-professionals/special-topics/hitech-act-enforcement-interim-final-rule/index.html)
- [FedRAMP moderate](https://www.fedramp.gov/documents/)
- [Europäische Union DSGVO](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=CELEX:32016R0679&from=EN)

## <a name="compliance-score"></a>KonformitätsBewertung

Die [Konformitätsbewertung](compliance-score-methodology.md) ist eine Kernkomponente des Compliance-Managers, die Ihrem Unternehmen hilft, die Compliance zu verstehen und zu verwalten. Wie bei [Microsoft Secure Score](microsoft-secure-score.md)ist die Konformitätsbewertung ein verhaltensbasiertes Bewertungssystem für Aktivitäten im Zusammenhang mit Datenschutz, Privatsphäre und Sicherheit in Ihrer Organisation. Die Konformitätsbewertung für eine Beurteilung ist Ausdruck der Einhaltung einer bestimmten Norm oder Regelung. Je höher der numerische Wert ist, desto besser ist die Konformitäts Position für die Bewertung. Grundlegendes zur Konformitäts Bewertungsmethodik ist entscheidend für die Priorisierung erforderlicher von Kunden verwalteter Steuerungsaktionen.
  
> [!IMPORTANT]
> Die Compliance-Bewertung drückt kein absolutes Maß für die Einhaltung eines bestimmten Standards oder einer bestimmten Vorschrift in der Organisation aus. Sie drückt vielmehr den Umfang aus, in dem Sie Steuerelemente einsetzen, durch die die Risiken für persönliche Daten und den Datenschutz reduziert werden können. Kein Dienst kann garantieren, dass Sie einen Standard oder eine Vorschrift einhalten. Die Compliance-Bewertung sollte in keinster Weise als eine Garantie verstanden werden.

## <a name="secure-score-integration"></a>Secure Score-Integration

Compliance-Manager ist in [Microsoft Secure Score](microsoft-secure-score.md) integriert, um die Konformitätsbewertung für synchronisierte Aktionselemente automatisch mit einem Secure Score-Guthaben zu versehen. Dies ist für einzelne Aktionselemente konfigurierbar und bietet eine kontinuierliche Aktualisierung zwischen den Elementen.

Sie haben beispielsweise eine sicherheitsbezogene Anforderung zum Aktivieren der Azure-Rechteverwaltung in Ihrer Organisation, die auch für ein Compliance-relevantes Aktionselement gilt. Wenn die Azure-Rechteverwaltung von Secure Score aktiviert und verarbeitet wird, erhält der Compliance-Manager eine Benachrichtigung über das Update, und die Punktzahl für das Aktionselement wird automatisch mit dem Fertigstellungs Guthaben aktualisiert.

## <a name="ready-to-get-started"></a>Sind Sie bereit zu beginnen?

Beginnen Sie [mit der Zusammenarbeit mit Compliance-Manager](working-with-compliance-manager.md) , um die Compliance-Aktivitäten Ihrer Organisation zu verwalten.

## <a name="resources"></a>Ressourcen

- [InterAktiver Leitfaden: bewerten und erweitern ihrer Datenschutz-Steuerelemente mit Compliance-Manager](https://content.cloudguides.com/guides/Compliance%20Manager)
- [Technische Community für Microsoft-Sicherheit, Datenschutz und Compliance](https://techcommunity.microsoft.com/t5/Security-Privacy-Compliance/ct-p/SecurityPrivacyCompliance)
