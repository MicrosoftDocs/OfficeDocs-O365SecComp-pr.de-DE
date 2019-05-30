---
title: Threat Explorer (und Echtzeiterkennung)
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 05/22/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Erfahren Sie mehr über Explorer (und Echtzeiterkennung) im Security &amp; Compliance Center.
ms.openlocfilehash: 030f866c5e86daa3dc543bddae7152e19f377d3b
ms.sourcegitcommit: 6c0fcb82178a4ac26375545f328389a6852a81be
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2019
ms.locfileid: "34490531"
---
# <a name="threat-explorer-and-real-time-detections"></a>Threat Explorer (und Echtzeiterkennung)

Wenn Ihre Organisation [Office 365 Advanced Threat Protection](office-365-atp.md) (Office 365 ATP) verfügt und Sie über die [erforderlichen Berechtigungen](#required-licenses-and-permissions)verfügen, haben Sie entweder **Explorer** -oder **Echtzeiterkennung** (früher *Echtzeitberichte* ), [Siehe ](#new-features-in-real-time-detections)Neuigkeiten!). Wechseln Sie im Security & Compliance Center zu **Threat Management**, und wählen Sie dann **Explorer** oder **Real-Time Detections**aus. 

|Mit ATP-Plan 2 sehen Sie Folgendes:  |Mit ATP-Plan 1 sehen Sie Folgendes:  |
|---------|---------|
|![Bedrohungs-Explorer](media/threatmgmt-explorer.png)      |![Echt Zeit Erkennungen](media/threatmgmt-realtimedetections.png)         |

Mit Explorer (oder Echtzeiterkennung) haben Sie einen leistungsfähigen Bericht, mit dem Ihr Sicherheits Betriebsteam Bedrohungen effektiv und effizient untersuchen und darauf reagieren kann, und es ähnelt dem folgenden Bild: 

![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

Mit diesem Bericht haben Sie folgende Möglichkeiten:
- [Siehe von Office 365 Sicherheitsfeatures erkannte Schadsoftware](#see-malware-detected-in-email-by-technology)
- [Anzeigen von Daten zu Phishing-URLs und klicken auf Urteil](#view-data-about-phishing-urls-and-click-verdict)
- [Starten eines automatisierten unter Such-und Antwort Prozesses in einer Ansicht im Explorer](#start-automated-investigation-and-response) (Nur ATP-Plan 2)
- ... [Untersuchung schädlicher e-Mails und vieles mehr](#more-ways-to-use-explorer-or-real-time-detections)!

## <a name="new-features-in-real-time-detections"></a>Neue Features in Echt Zeit Erkennungen

Für Office 365 ATP-Plan 1-Kunden wurde der Bericht über *Echt Zeit Erkennungen* zuvor als *Echtzeitberichte*bezeichnet. Zusätzlich zur Namensänderung werden mehrere neue Features und Verbesserungen bereitstellen:

- In der Phishing-Ansicht finden Sie weitere Details zu erkannten URLs über [ATP-sichere Links](atp-safe-links.md). Zu den neuen Details und Funktionen gehören:
  - URLs in e-Mail-Nachrichten
  - Filtern basierend auf URL-Informationen
  - In datendiagrammen angezeigte URL-Informationen
  - Time-of-Click-Daten zu Klicks in Nachrichten

- Wenn es eine Änderung in einer URL auf Urteilsspruch gibt, wird eine Warnung angezeigt. URL-Klick-Urteile können sich ändern, wenn sich die Reputation einer URL nach der Detonation ändert oder wenn ein Benutzer, der durch ATP-sichere Links geschützt ist, eine [Warnung über ATP-sichere Links](atp-safe-links-warning-pages.md)überschreibt.  
 
Diese Verbesserungen ermöglichen es den Sicherheitsadministratoren Ihrer Organisation, mehr Details anzuzeigen als zuvor. Sicherheitsadministratoren können Informationen zu URL-Domänen, verpassten URLs, Klick Urteilen und mehr anzeigen und dann Office 365 ATP-Richtlinien entsprechend anpassen.

> [!NOTE]
> Während sich diese Features in der Vorschau befinden, stehen URL-Daten für eine beschränkte Anzahl von Tagen zur Verfügung. 

## <a name="see-malware-detected-in-email-by-technology"></a>Siehe in e-Mail erkannte Malware nach Technologie

Angenommen, Sie möchten die in e-Mail-nach Office 365-Technologie erkannte Malware sehen. Verwenden Sie dazu die [e-Mail->-Malware](threat-explorer-views.md#email--malware) Ansicht des Explorers (oder Echtzeiterkennung).

1. Wählen Sie im Security & Compliance Center[https://protection.office.com](https://protection.office.com)() **Threat Management** > **Explorer** (oder **Echtzeiterkennung**) aus. (In diesem Beispiel wird der Explorer verwendet.)

2. Wählen Sie im Menü **Ansicht** die Option **e-Mail-** > **Schadsoftware**aus.<br/>![Menü "Ansicht" für Explorer](media/ExplorerViewEmailMalwareMenu.png)<br/>

3. Klicken Sie auf **Absender**, und wählen Sie dann **Basis** > **Erkennungstechnologie**aus.<br/>Ihre Erkennungstechnologien stehen nun als Filter für den Bericht zur Verfügung.<br/>![Technologien zur Erkennung von Malware](media/ExplorerEmailMalwareDetectionTech.png)<br/> 

4. Wählen Sie eine Option aus, und klicken Sie dann auf die Schaltfläche **Aktualisieren** , um diesen Filter anzuwenden.<br/>![Ausgewählte Erkennungstechnologie](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

Der Bericht wird aktualisiert, um die in e-Mail-Nachweise erkannten Ergebnisse mithilfe der ausgewählten Technologie-Option anzuzeigen. Von hier aus können Sie weitere Analysen durchführen.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>Anzeigen von Daten zu Phishing-URLs und klicken auf Urteil

Angenommen, Sie möchten Phishing-Versuche über URLs in e-Mails sehen, einschließlich einer Liste von URLs, die zugelassen, blockiert und außer Kraft gesetzt wurden. Zum Identifizieren von URLs, auf die geklickt wurde, müssen [ATP-sichere Links](atp-safe-links.md) konfiguriert werden. Stellen Sie sicher, dass Sie [Richtlinien für ATP-sichere Links](set-up-atp-safe-links-policies.md) zum Zeitpunkt des Klick Schutzes und zur Protokollierung von Klick urteilen durch ATP-sichere Links eingerichtet haben. 

Um Phishing-URLs in Nachrichten und Klicks auf URLs in Phishing-Nachrichten zu überprüfen, verwenden Sie die [e-Mail-> Phishing-](threat-explorer-views.md#email--phish) Ansicht des Explorers (oder Echtzeiterkennung).

1. Wählen Sie im Security & Compliance Center[https://protection.office.com](https://protection.office.com)() **Threat Management** > **Explorer** (oder **Echtzeiterkennung**) aus. (In diesem Beispiel wird der Explorer verwendet.)

2. Wählen Sie im Menü **Ansicht** die Option**Phishing** **per e-Mail** > aus.<br/>![Menü "Ansicht" für Explorer](media/ExplorerViewEmailPhishMenu.png)<br/>

3. Klicken Sie auf **Absender**, und wählen Sie dann **URLs** > **Klicken Sie auf Urteil**.

4. Wählen Sie eine oder mehrere Optionen aus, beispielsweise " **blockiert** " und "über **schrieben**", und klicken Sie dann auf die Schaltfläche **Aktualisieren** , die sich in derselben Reihe befindet wie die Optionen zum Anwenden des Filters. (Aktualisieren Sie Ihr Browserfenster nicht.)<br/>![URLs und Klick Urteile](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

    Der Bericht wird aktualisiert, um zwei unterschiedliche URL-Tabellen auf der Registerkarte URL unter dem Bericht anzuzeigen:

   1. **Top-URLs** sind die URLs, die in den Nachrichten enthalten sind, nach denen Sie nach unten gefiltert haben, und die e-Mail-Zustellungs Aktion zählt für jede URL. In der Phishing-e-Mail-Ansicht enthält diese Liste normalerweise legitime URLs. Angreifer enthalten eine Mischung aus guten und ungültigen URLs in ihren Nachrichten, um Sie zu übermitteln, aber Sie machen die bösartigen Links für den Benutzer interessanter, auf Sie zuwerden. Die Tabelle der URLs wird nach der Gesamtzahl der e-Mails sortiert (Hinweis: Diese Spalte wird nicht angezeigt, um die Ansicht zu vereinfachen).

   2. Zu den **wichtigsten Klicks** gehören die eingebundenen URLs, auf die geklickt wurde, sortiert nach der Gesamtanzahl der Klick Zähler (diese Spalte wird auch nicht angezeigt, um die Ansicht zu vereinfachen). Gesamtanzahl Zählungen nach Spalte geben Sie die sichere Links klicken Sie auf Urteils Zählung für jede URL, auf die geklickt wurde. In der Phishing-e-Mail-Ansicht sind dies häufiger verdächtige oder böswillige URLs, aber Sie können auch saubere URLs in Phishing-Nachrichten enthalten. URL Klicks auf unverpackte Links werden hier nicht angezeigt.
   
   Die beiden URLs Tabellen zeigen Top-URLs in Phishing-e-Mails nach Zustellung Aktion und Ort, und Sie zeigen URL Klicks, die blockiert wurden (oder besucht, obwohl eine Warnung), damit Sie verstehen, welche potenziellen schlechten Links wurden von Benutzern empfangen und mit den Benutzern interagieren. Von hier aus können Sie weitere Analysen durchführen. Beispielsweise können Sie unter dem Diagramm die häufigsten URLs in e-Mails sehen, die in der Umgebung Ihrer Organisation blockiert wurden.
   
   ![Blockierte Explorer-URLs](media/ExplorerPhishClickVerdictURLs.png)
   
   Wählen Sie eine URL aus, um ausführlichere Informationen anzuzeigen. Beachten Sie, dass im Dialogfeld URL-Flyout die Filterung von e-Mails entfernt wird, um Ihnen die vollständige Ansicht der URL-Exposition in Ihrer Umgebung anzuzeigen. Auf diese Weise können Sie e-Mails im Explorer nach bestimmten URLs filtern, die potenzielle Bedrohungen darstellen, und dann Ihr Verständnis der URL-Exposition in Ihrer Umgebung erweitern (über das Dialogfeld "URL-Details"), ohne dass Sie der URL-Filter hinzufügen müssen. Explorer-Ansicht selbst.

## <a name="review-email-messages-reported-by-users"></a>Überprüfen von von Benutzern gemeldeten e-Mail-Nachrichten

Angenommen, Sie möchten e-Mail-Nachrichten anzeigen, die Benutzer in Ihrer Organisation als Junk-, kein Junk-oder als Phishing gemeldet haben, indem Sie das [Berichtsnachrichten-Add-in für Outlook und Outlook im Internet](enable-the-report-message-add-in.md)verwenden. Verwenden Sie dazu die [benutzerbezogene](threat-explorer-views.md#email--user-reported) Ansicht "e-Mail->" des Explorers (oder Echt Zeit Erkennungen).

1. Wählen Sie im Security & Compliance Center[https://protection.office.com](https://protection.office.com)() **Threat Management** > **Explorer** (oder **Echtzeiterkennung**) aus. (In diesem Beispiel wird der Explorer verwendet.)

2. Wählen Sie im Menü **Ansicht** die Option **e-Mail** > **-Benutzerbericht**aus.<br/>![Menü "Ansicht" für Explorer](media/ExplorerViewMenuEmailUserReported.png)<br/>

3. Klicken Sie auf **Absender**, und wählen Sie **Standard** > **Berichtstyp**aus.

4. Wählen Sie eine Option wie **Phishing**aus, und klicken Sie dann auf die Schaltfläche **Aktualisieren** . <br/>![Vom Benutzer gemeldetes Phishing](media/EmailUserReportedReportType.png)<br/> 

Der Bericht wird aktualisiert, um Daten über e-Mail-Nachrichten anzuzeigen, die Personen in Ihrer Organisation als Phishing-Versuch gemeldet haben. Sie können diese Informationen verwenden, um weitere Analysen durchzuführen und bei Bedarf Ihre [ATP-Anti-Phishing-Richtlinien](set-up-anti-phishing-policies.md)anzupassen.

## <a name="start-automated-investigation-and-response"></a>Starten der automatischen Untersuchung und Antwort

> [!NOTE]
> In **Office 365 ATP-Plan 2** und **Office 365 E5**stehen automatisierte Ermittlungs-und Antwortfunktionen zur Verfügung.

(Neu!) Durch [Automatische Untersuchung und Antwort](automated-investigation-response-office.md) können Sie Ihr Sicherheits Betriebsteam viel Zeit und Mühe bei der Untersuchung und Abwehr von Cyber-Angriffen speichern. Zusätzlich zum Konfigurieren von Warnungen, die ein Sicherheits Textbuch auslösen können, können Sie einen automatisierten Ermittlungs-und Antwortprozess aus einer Ansicht im Explorer starten. 

Ausführliche Informationen hierzu finden Sie unter [Beispiel: ein Sicherheitsadministrator löst eine Untersuchung im Explorer aus](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer).

## <a name="more-ways-to-use-explorer-or-real-time-detections"></a>Weitere Möglichkeiten zum Verwenden von Explorer (oder Echtzeiterkennung)

Zusätzlich zu den in diesem Artikel beschriebenen Szenarien stehen Ihnen viele weitere Berichtsoptionen mit Explorer (oder Echtzeiterkennung) zur Verfügung. 
- [Suchen und Untersuchen von bösartigen E-Mails, die zugestellt wurden](investigate-malicious-email-that-was-delivered.md)
- [Anzeigen schädlicher Dateien, die in SharePoint Online, OneDrive und Microsoft Teams erkannt wurden](malicious-files-detected-in-spo-odb-or-teams.md)
- [Erhalten einer Übersicht über die Ansichten in Threat Explorer (und Echtzeiterkennung)](threat-explorer-views.md)

## <a name="required-licenses-and-permissions"></a>Erforderliche Lizenzen und Berechtigungen

Sie benötigen [Office 365 ATP](office-365-atp.md) , um den Explorer oder Echt Zeit Erkennungen zu erhalten.
- Der Explorer ist in Office 365 ATP-Plan 2 enthalten. 
- Der Bericht über Echt Zeit Erkennungen ist in Office 365 ATP-Plan 1 enthalten.

Zum Anzeigen und Verwenden von Explorer-oder Echt Zeit Erkennungen müssen Sie über die entsprechenden Berechtigungen verfügen, beispielsweise solche, die einem Sicherheitsadministrator oder Sicherheits Leser erteilt werden. 

- Für das Security &amp; Compliance Center müssen Sie eine der folgenden Rollen zugewiesen haben:
    - Organisationsverwaltung
    - Sicherheits Administrator (Dies kann im Azure Active Directory Admin Center zugewiesen werden ([https://aad.portal.azure.com](https://aad.portal.azure.com)))
    - Sicherheits Leser

- Für Exchange Online müssen Sie eine der folgenden Rollen entweder in der Exchange-Verwaltungskonsole ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) oder mit PowerShell-Cmdlets zugewiesen haben (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Organisationsverwaltung
    - Organisationsverwaltung mit Leserechten
    - Rolle „Empfänger mit Leserechten“
    - Verwaltung der Richtlinientreue

Weitere Informationen zu Rollen und Berechtigungen finden Sie in den folgenden Ressourcen:

- [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
- [Featureberechtigungen in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
