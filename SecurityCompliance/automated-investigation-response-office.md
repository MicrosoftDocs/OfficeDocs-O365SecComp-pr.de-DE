---
title: Automatisierte Untersuchung und Antwort (AIR) mit Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Erfahren Sie mehr über automatisierte Ermittlungs-und Antwortfunktionen in Office 365 Advanced Threat Protection.
ms.openlocfilehash: c2d5acd0bf26dc28b30f26488adf47de2c834fb6
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30736335"
---
# <a name="automated-investigation-and-response-air-with-office-365-threat-intelligence"></a>Automatisierte Untersuchung und Antwort (AIR) mit Office 365 Threat Intelligence

Automatisierte Untersuchung und Antwort (AIR) (demnächst in [Office 365 Threat Investigation and Response Capabilities](office-365-ti.md)) ermöglicht es Ihnen, automatisierte Untersuchungen und Korrekturen zu bekannten Bedrohungen durchzuführen, die es heute gibt. Lesen Sie diesen Artikel, um einen Überblick über die Luft zu erhalten und zu erfahren, wie Sie Ihr Unternehmen dabei unterstützen, Bedrohungen effektiver und effizienter zu verringern. Weitere Informationen dazu, wann AIR verfügbar ist, finden Sie im [Microsoft 365-Fahrplan](https://www.microsoft.com/microsoft-365/roadmap).

## <a name="alerts"></a>Warnungen

[Warnungen](alert-policies.md#viewing-alerts) stellen Auslöser für Sicherheitsoperationen-Team Workflows für Vorfalls Reaktionen dar. Das Priorisieren des richtigen Warnungs Satzes zur Untersuchung und sicherstellen, dass keine Bedrohungen unadressiert sind, ist eine Herausforderung. Wenn Untersuchungen zu Warnungen manuell durchgeführt werden, müssen Sicherheits Betriebsteams Entitäten (z. b. Inhalte, Geräte und Benutzer), die von Bedrohungen bedroht sind, aufspüren und korrelieren. Solche Aufgaben und Workflows sind sehr zeitaufwändig und beinhalten mehrere Tools und Systeme. Mit AIR werden Untersuchungen und Reaktionszeiten zu wichtigen Sicherheits-und Bedrohungs Verwaltungswarnungen automatisiert, die ihre Sicherheitsantwort-Manuskripte automatisch auslösen. 

zum anzeigen von benachrichtigungen wählen sie im Office 365 Security & Compliance Center **alerts** > **anzeigen**.

![Warnungen, die auf Untersuchungen verweisen](media/air-alerts-page-details.png) 

Wählen Sie eine Warnung aus, um die Details anzuzeigen, und verwenden Sie dann den Link **untersuchUng anzeigen** , um zur entsprechenden [Untersuchung](#investigation-graph)zu wechseln.

## <a name="security-playbooks"></a>Sicherheits Manuskripte

Sicherheits Manuskripte sind Back-End-Richtlinien, die im Mittelpunkt der Automatisierung in Microsoft Threat Protection stehen. Die in AIR bereitgestellten Sicherheits Manuskripte basieren auf allgemeinen Sicherheitsszenarien in der Praxis. Ein Sicherheits Textbuch wird automatisch gestartet, wenn in Ihrer Organisation eine Warnung ausgelöst wird. Sobald die Warnung ausgelöst wird, wird das zugehörige Textbuch automatisch ausgeführt. Das Textbuch führt eine Untersuchung durch, untersucht alle zugehörigen Metadaten (einschließlich e-Mail-Nachrichten, Benutzer, betreffs, Absender usw.), und empfiehlt anhand der Ergebnisse eine Reihe von Aktionen, die das Sicherheitsteam Ihrer Organisation ausführen kann, um die Bedrohung. 

Die Sicherheits Manuskripte, die Sie mit AIR erhalten, wurden entwickelt, um die häufigsten Bedrohungen zu bewältigen, denen Organisationen heute gegenüberstehen. Sie basieren auf Eingaben aus Sicherheits-und Vorfall Reaktions Teams, einschließlich derer, die bei der Verteidigung von Microsoft-Objekten helfen.

### <a name="security-playbooks-are-rolling-out-in-phases"></a>Sicherheits Manuskripte werden phasenweise ausgeführt

Als Teil von AIR werden Sicherheits Manuskripte phasenweise ausgeführt

- **Phase 1 (April 2019)**: Manuskripte bieten Empfehlungen, die Sicherheitsadministratoren überarbeiten und genehmigen. 

- **Phase 2 (juni 2019)**: Sicherheitsadministratoren haben die Möglichkeit, Sicherheits-Textbuch zu ermöglichen, automatisch Maßnahmen ohne administrative Interaktion zu ergreifen.

Phase 1 umfasst die folgenden Manuskripte:
- Vom Benutzer gemeldete Phishing-Nachricht
- URL Klick Urteil ändern und ATP Safe Links Block außer Kraft setzen
- Malware ZAP
- Phishing ZAP
- Manuelle Untersuchungen (mit Explorer)

Für Phase 2 sind mehrere Manuskripte geplant.

### <a name="playbooks-include-investigation-and-recommendations"></a>Manuskripte schließen Untersuchungen und Empfehlungen ein

Jedes Textbuch umfasst Folgendes: 
- eine Stamm Ermittlung, 
- Schritte zum Aufspüren anderer potenzieller Bedrohungen und 
- Empfohlene Bedrohungs Korrektur.

Jeder allgemeine Schritt enthält viele unter Schritte, die ausgeführt werden, um eine umfassende, detaillierte und umfassende Antwort auf Bedrohungen bereitzustellen.

## <a name="example-user-reported-phish-message"></a>Beispiel: vom Benutzer gemeldete Phishing-Nachricht

Wenn ein Benutzer in Ihrer Organisation eine e-Mail-Nachricht sendet und ihn über das [Add-in Berichtnachricht für Outlook oder Outlook Web Access](enable-the-report-message-add-in.md)an Microsoft meldet. Dies löst eine System basierte Informationswarnung aus, die das Ermittlungs Manuskript automatisch startet.

Während der Stamm Untersuchung werden verschiedene Aspekte der e-Mail ausgewertet. Zu diesen zählen:
- Eine Bestimmung darüber, welche Art von Bedrohung es sein könnte;
- Wer hat Sie gesendet?
- Absender der e-Mail (Sendeinfrastruktur)
- Ob andere Instanzen der e-Mail zugestellt oder blockiert wurden;
- Eine Bewertung durch unsere Analysten;
- Gibt an, ob die e-Mail bekannten Kampagnen zugeordnet ist;
- und vieles mehr.

Nach Abschluss der Stamm Ermittlung enthält das Textbuch eine Liste der empfohlenen Aktionen.
  
Als nächstes werden mehrere Jagd Schritte ausgeführt:

- Ähnliche e-Mails in anderen e-Mail-Clustern werden durchsucht.
- Das Signal wird für andere Plattformen wie [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection)freigegeben.
- Es wird festgelegt, ob Benutzer auf die verdächtige e-Mail-Nachricht geklickt haben.
- Eine Überprüfung erfolgt in Office 365 [EoP](eop/exchange-online-protection-eop.md) und [ATP](office-365-atp.md) , um festzustellen, ob andere ähnliche Nachrichten von Benutzern gemeldet werden.
- Es wird überprüft, ob ein Benutzer kompromittiert wurde. Diese Überprüfung nutzt Signale in [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) und [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), korreliert alle zugehörigen Ereignisse oder Warnungen. 

Während der Jagd Phase werden Risiken und Bedrohungen verschiedenen Jagd Stufen zugeordnet.  

Sanierung ist die letzte Phase des Manuskripts. Während dieser Phase werden Behebungsschritte auf der Grundlage von theinvestigation-und-Jagd Phasen ausgeführt.  

## <a name="getting-started"></a>Erste Schritte

Um auf ihre Untersuchungen zuzugreifen, wechseln Sie als globaler Office 365-Administrator oder Sicherheitsadministrator zum Office 365 Security &[https://protection.office.com](https://protection.office.com)Compliance Center (), und melden Sie sich an. Führen Sie dann einen der folgenden Schritte aus:

- Navigieren Sie im linken Navigationsbereich zu **Threat Management** > **Investigations**.

    oder

- Besuchen Sie das Threat Management Dashboard (im Security & Compliance Center, navigieren Sie zu **Threat Management** > **Dashboard**).

![AIR-Widgets](media/air-widgets.png)

Ihre AIR-Widgets werden am oberen Rand des [Sicherheits Dashboards](security-dashboard.md)angezeigt. Wählen Sie ein Widget aus, um loszulegen.

### <a name="automated-investigations"></a>Automatisierte Untersuchungen

Auf der Seite automatisierte Untersuchungen werden die Ermittlungen Ihrer Organisation und ihre aktuellen Status angezeigt.

![Haupt Untersuchungs Seite für Luft](media/air-maininvestigationpage.png) 
  
Sie können:
- Navigieren Sie direkt zu einer Untersuchung (Wählen Sie eine **ERMITTLUNGS-ID**aus).
- Anwenden von Filtern Wählen Sie **unter**Untersuchungs, **Zeitspanne**, **Status**oder eine Kombination aus.
- Exportieren Sie die Daten in eine CSV-Datei.

### <a name="investigation-graph"></a>Untersuchung Graph

Wenn Sie eine bestimmte Untersuchung öffnen, wird die Seite Untersuchungs Graph angezeigt. Auf dieser Seite werden alle Entitäten angezeigt: e-Mail-Nachrichten, Benutzer (und ihre Aktivitäten) und Geräte, die als Teil der ausgelösten Warnung automatisch untersuchtwurden.

![Seite "AIR Investigation Graph"](media/air-investigationgraphpage.png)

Sie können:
- Erhalten Sie einen visuellen Überblick über die aktuelle Untersuchung.
- Zeigen Sie eine Zusammenfassung der Untersuchungen an.
- Wählen Sie einen Knoten in der Visualisierung aus, um Details für diesen Knoten anzuzeigen.
- Wählen Sie oben eine Registerkarte aus, um Details für diese Registerkarte anzuzeigen.

### <a name="alert-investigation"></a>Warnungs Ermittlung

Auf der Registerkarte **Benachrichtigungen** für eine Untersuchung werden alle für die Untersuchung relevanten Warnungen angezeigt. Details sind die Warnung, die die Untersuchung ausgelöst hat, sowie andere Warnungen, wie beispielsweise riskante Anmeldungen, Massendownloads usw., die mit der Untersuchung in Beziehung stehen. Auf dieser Seite kann ein Sicherheitsanalytiker auch zusätzliche Details zu einzelnen Warnungen anzeigen.

![Seite "Luft Warnungen"](media/air-investigationalertspage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die aktuelle Auslöse Warnung und alle zugehörigen Warnungen.
- Wählen Sie in der Liste eine Warnung aus, um eine Fly-Out-Seite mit vollständigen Warnungsdetails zu öffnen.

### <a name="email-investigation"></a>E-Mail-Untersuchung

Auf der Registerkarte **e-Mail-Nachricht** für eine Untersuchung werden alle e-Mail-Cluster angezeigt, die im Rahmen der Untersuchung identifiziert wurden. 

Angesichts der schieren Menge an e-Mails, die Benutzer in einer Organisation senden und empfangen, wird der Prozess der 
- Gruppieren von e-Mail-Nachrichten basierend auf ähnlichen Attributen aus einem Nachrichtenkopf, einem Text, einer URL und einer Anlage 
- Trennen von böswilligen e-Mails von der guten e-Mail; und 
- Ausführen von Aktionen für böswillige e-Mail-Nachrichten 

kann viele Stunden in Anspruch nehmen. Mit AIR wird dieser Prozess automatisiert, und das Sicherheitsteam des Unternehmens spart Zeit und Aufwand. 

Betrachten Sie als Beispiel die folgende Abbildung. Der erste Cluster von drei e-Mail-Nachrichten wurde als Phishing eingestuft. Es wurde ein weiterer Cluster ähnlicher Nachrichten mit derselben IP-Adresse und einem anderen Betreff gefunden, der als bösartig eingestuft wurde, da einige von Ihnen bei der Ersterkennung als Phishing identifiziert wurden. 

![Seite zur Untersuchung der Luft e-Mail](media/air-investigationemailpage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die aktuellen Cluster Ergebnisse und Bedrohungen.
- Klicken Sie auf eine Cluster Entität oder eine Bedrohungsliste, um eine Fly-Out-Seite zu öffnen, auf der die vollständigen Warnungsdetails angezeigt werden.

![Untersuchung per e-Mail mit Flyout-Details](media/air-investigationemailpageflyoutdetails.png)

### <a name="user-investigation"></a>Benutzer Ermittlung

Auf der Registerkarte **Benutzer** werden alle Benutzer angezeigt, die im Rahmen der Untersuchung identifiziert wurden. 

In der folgenden Abbildung hat AIR beispielsweise Indikatoren für Kompromisse und Anomalien basierend auf einer neuen Posteingangsregel ermittelt, die erstellt wurde. Weitere Details (Evidence) der Untersuchung sind über detaillierte Ansichten auf dieser Registerkarte verfügbar.

![Seite "Luft Ermittlungs Benutzer"](media/air-investigationuserspage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die identifizierten Benutzer Ergebnisse und Risiken.
- Wählen Sie einen Benutzer aus, um eine Fly-Out-Seite mit den vollständigen Warnungsdetails zu öffnen.

### <a name="machine-investigation"></a>Computeruntersuchungen

Auf der Registerkarte **Computer** werden alle Computer angezeigt, die im Rahmen der Untersuchung identifiziert wurden. 

![Seite "Luft Untersuchungsgerät"](media/air-investigationmachinepage.png)

Im Rahmen der Untersuchung korreliert AIR e-Mail-Bedrohungen mit Geräten. Eine Untersuchung übergibt beispielsweise einen Dateihash an [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) , um zu untersuchen. Dies ermöglicht eine automatisierte Untersuchung der relevanten Computer für Ihre Benutzer und hilft dabei, sicherzustellen, dass Bedrohungen sowohl in der Cloud als auch über Ihre Geräte adressiert werden. 

Sie können:
- Erhalten Sie eine visuelle Übersicht über die aktuellen Computer und Bedrohungen.
- Wählen Sie einen Computer aus, um eine Ansicht zu öffnen, die in die zugehörigen [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection)-Untersuchungen eingeht.

### <a name="entity-investigation"></a>Entitäts Untersuchung

Auf der Registerkarte **Entitäten** werden alle Computer angezeigt, die im Rahmen der Untersuchung identifiziert wurden. 

Hier sehen Sie die untersuchten Entitäten. Sie können Details der Entitätstypen wie e-Mail-Nachrichten, Cluster, IP-Adressen, Benutzer und vieles mehr anzeigen. Sie können auch sehen, wie viele Entitäten analysiert wurden und welche Bedrohungen jeweils zugeordnet wurden. 

![Seite "AIR Investigation Entities"](media/air-investigationentitiespage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die gefundenen Ermittlungs Entitäten und-Bedrohungen.
- Wählen Sie eine Entität aus, um eine Fly-Out-Seite zu öffnen, die die Details der zugehörigen Entität anzeigt.

![Details zu AIR Investigation Entities](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a>Textbuch-Protokoll

Auf der Registerkarte **Protokoll** werden alle Schritte für das Textbuch angezeigt, die während der Untersuchung aufgetreten sind. Das Protokoll erfasst eine vollständige Bestandsaufnahme aller Aktionen, die von Office 365 Threat Intelligence-Funktionen als Teil von AIR ausgeführt wurden. Es bietet eine übersichtliche Ansicht aller Schritte, einschließlich der Aktion selbst, einer Beschreibung und der Dauer des aktuellen vom Anfang bis zum Ende. 

![Seite "AIR Investigation log"](media/air-investigationlogpage.png)

Sie können:
- Sehen Sie sich eine visuelle Übersicht über die Schritte des Manuskripts an.
- Exportieren Sie die Ergebnisse in eine CSV-Datei.
- Filtern Sie die Ansicht.

### <a name="recommended-actions"></a>Empfohlene Aktionen

Auf der Registerkarte **Aktionen** werden alle Text Handlung-Aktionen angezeigt, die nach Abschluss der Untersuchung zur Korrektur empfohlen werden. 

Aktionen erfassen eine vollständige Liste aller Schritte, die Microsoft am Ende einer Untersuchung empfiehlt. Sie können Korrekturaktionen durchführen, indem Sie eine oder mehrere Aktionen auswählen. Wenn **** Sie auf Genehmigen klicken, kann die Korrektur beginnen. (Möglicherweise sind entsprechende Berechtigungen erforderlich. Beispielsweise kann ein Sicherheits Lesegerät Aktionen anzeigen, aber nicht genehmigen.)  

![Seite "AIR Investigations Action"](media/air-investigationactionspage.png)

Sie können:
- Erhalten Sie eine visuelle Übersicht über die vom Textbuch empfohlenen Aktionen.
- Wählen Sie eine einzelne Aktion oder mehrere Aktionen aus.
- Genehmigen empfohlener Aktionen. (Diese werden sofort mit Kommentaren gestartet.)
- Exportieren Sie die Ergebnisse in eine CSV-Datei.
- Filtern Sie die Ansicht.

## <a name="how-to-get-air"></a>So erhalten Sie AIR

Derzeit ist AIR in der Vorschau. Bei der Veröffentlichung wird AIR in die folgenden Abonnements aufgenommen:

- Microsoft 365 Enterprise E5
- Office 365 Enterprise E5
- Microsoft Threat Protection
- Office 365 Advanced Threat Protection-Plan 2

Weitere Informationen zur Verfügbarkeit von Funktionen finden Sie in der [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap).
