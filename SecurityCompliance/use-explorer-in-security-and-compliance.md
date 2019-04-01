---
title: Verwenden des Bedrohungs-Explorers &amp; im Security Compliance Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/31/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Informationen zu Explorer (auch als Bedrohungs-Explorer bezeichnet) &amp; im Security Compliance Center.
ms.openlocfilehash: c782e5962164b7d35947befe526c20f7dc0943d5
ms.sourcegitcommit: 691370682825a7601bd4b77d0a8c4b51ed15682f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2019
ms.locfileid: "31014014"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a>Verwenden des Bedrohungs-Explorers &amp; im Security Compliance Center

Wenn Ihre Organisation [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md) (ATP) enthält und Sie über die erforderlichen Berechtigungen verfügen, können Sie Threat Explorer (auch als Explorer bezeichnet) verwenden, um Bedrohungen zu identifizieren und zu analysieren. (Um Explorer zu verwenden, wechseln Sie &amp; im Security Compliance Center zu **Threat Management** \> **Explorer**.)

![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

Explorer ist ein leistungsstarkes, nahezu Echtzeit-Tool, mit dessen Hilfe Sicherheitsteams untersuchen und auf Bedrohungen im Security &amp; Compliance Center reagieren können. Hier sind einige Dinge, die Sie tun können:
- [Siehe Schadsoftware, die von Office 365-Sicherheitsfeatures erkannt wurde](#see-malware-detected-in-email-by-technology)
- [Anzeigen von Daten zu Phishing-URLs und klicken auf "Urteil"](#view-data-about-phishing-urls-and-click-verdict)
- [Starten eines automatisierten unter Such-und Antwort Prozesses aus einer Ansicht im Explorer](#start-automated-investigation-and-response)
- ... [und vieles mehr](#more-ways-to-use-explorer)!

## <a name="see-malware-detected-in-email-by-technology"></a>Siehe in e-Mail erkannte Schadsoftware nach Technologie

Angenommen, Sie möchten Schadsoftware erkennen, die in e-Mails erkannt wurde, und die Technologie in Office 365. Zu diesem Zweck verwenden Sie die [e-Mail-_GT_ Malware-](threat-explorer-views.md#email--malware) Ansicht des Explorers.

1. Klicken Sie im Security & Compliance Center[https://protection.office.com](https://protection.office.com)() auf **Threat Management** > **Explorer**.
2. Wählen Sie im Menü **Ansicht** die Option **e-Mail-** > **Schadsoftware**aus.<br/>![Menü ' Ansicht ' für Explorer](media/ExplorerViewEmailMalwareMenu.png)<br/>
3. Klicken Sie auf **Absender**, und wählen Sie dann **grundlegende** > **Erkennungstechnologie**aus.<br/>Ihre Erkennungstechnologien sind jetzt als Filter für den Bericht verfügbar.<br/>![Malware Erkennungstechnologien](media/ExplorerEmailMalwareDetectionTech.png)<br/> 
4. Wählen Sie eine Option aus, und klicken Sie dann auf die Schaltfläche Aktualisieren, um diesen Filter anzuwenden.<br/>![Ausgewählte Erkennungstechnologie](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

Der Bericht wird aktualisiert, um die in e-Mails festgestellten Ergebnisse mithilfe der von Ihnen ausgewählten technologieoption anzuzeigen. Von hier aus können Sie eine weitere Analyse durchführen.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>Anzeigen von Daten zu Phishing-URLs und klicken auf "Urteil"

Angenommen, Sie möchten Phishing-Versuche über URLs in e-Mails anzeigen, einschließlich einer Liste von URLs, die zugelassen, blockiert und überschrieben wurden.  Die Identifizierung von URLs, auf die geklickt wurde, erfordert [ATP-sichere Links](atp-safe-links.md). (Stellen Sie sicher, dass Sie für Ihre Benutzer die [Richtlinien "ATP Safe Links](set-up-atp-safe-links-policies.md) " eingerichtet und angewendet haben, um den Click-Time-Schutz und die Protokollierung von Click-urteilen durch ATP-sichere Links zu ermöglichen.) Zum Überprüfen von Phishing-URLs in Nachrichten und klicken auf URLs in Phishing-Nachrichten verwenden Sie die [e-Mail-_GT_-Phishing-](threat-explorer-views.md#email--phish) Ansicht des Explorers.

1. Klicken Sie im Security & Compliance Center[https://protection.office.com](https://protection.office.com)() auf **Threat Management** > **Explorer**.
2. Wählen Sie im Menü **Ansicht** die Option **e-Mail-** > **Phishing**aus.<br/>![Menü ' Ansicht ' für Explorer](media/ExplorerViewEmailPhishMenu.png)<br/>
3. Klicken Sie auf **Absender**, und wählen Sie dann **URLs** > **Klicken Sie auf Urteil**.
4. Wählen Sie eine oder mehrere Optionen aus, beispielsweise **blockiert** und über **schrieben**, und klicken Sie dann auf die Schaltfläche **Aktualisieren** , um diesen Filter anzuwenden.<br/>![URLs und Klick Urteile](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

Der Bericht wird aktualisiert, um zwei verschiedene URL-Tabellen auf der Registerkarte URL unten anzuzeigen:
1. **Top-URLs** sind die URLs, die in den Nachrichten enthalten sind, auf die Sie nach unten gefiltert haben, und die e-Mail-Zuschlags Aktion gilt für jede URL. In der Phishing-e-Mail-Ansicht enthält diese Liste normalerweise legitime URLs. Angreifer bieten eine Kombination aus guten und schlechten URLs in ihren Nachrichten, um zu versuchen, Sie zuzustellen, aber Sie machen die böswilligen Links interessanter, wenn der Benutzer darauf klickt. Die Tabelle der URLs wird nach der Gesamtzahl der e-Mails sortiert (Hinweis: Diese Spalte wird nicht angezeigt, um die Ansicht zu vereinfachen).
2. Bei den **oberen Klicks** handelt es sich um sichere Links eingebundene URLs, auf die geklickt wurde, sortiert nach der Gesamtanzahl der Klick zahlen (diese Spalte wird auch nicht angezeigt, um die Ansicht zu vereinfachen). Gesamtanzahl nach Spalte: Klicken Sie auf die Anzahl der sicheren Links, auf die Sie für die einzelnen URLs geklickt haben. In der Phishing-e-Mail-Ansicht sind diese häufig verdächtige oder böswillige Links, aber auch saubere URLs, die in Phishing-Nachrichten vorkommen. URL-Klicks auf nicht umbrochene Links werden hier nicht angezeigt.

Die beiden URLs-Tabellen zeigen die häufigsten URLs in Phishing-e-Mails nach dem Zustellungsstatus und zeigen URL-Klicks, die blockiert (oder trotz einer Warnung besucht) wurden, damit Sie verstehen können, welche potenziellen fehlerhaften Links von Benutzern empfangen und von Benutzern interagiert wurden. Von hier aus können Sie eine weitere Analyse durchführen. Unter dem Diagramm können Sie beispielsweise die häufigsten URLs in e-Mails anzeigen, die in der Umgebung Ihrer Organisation blockiert wurden. 

![Blockierte Explorer-URLs](media/ExplorerPhishClickVerdictURLs.png) 

Wählen Sie eine URL aus, um detailliertere Informationen anzuzeigen. Beachten Sie, dass im Dialogfeld URL-Flyout die Filterung in e-Mails entfernt wird, um die vollständige Anzeige der Belichtung der URL in Ihrer Umgebung anzuzeigen. Auf diese Weise können Sie e-Mails im Explorer filtern, die Sie betreffen, nach bestimmten URLs suchen, die potenzielle Bedrohungen darstellen, und dann Ihr Verständnis für die URL-Exposition in Ihrer Umgebung erweitern (über das Dialogfeld URL-Details), ohne URL-Filter hinzufügen zu müssen. Explorer-Ansicht selbst.

## <a name="review-email-messages-reported-by-users"></a>Überprüfende e-Mail-Nachrichten von Benutzern

Angenommen, Sie möchten e-Mail-Nachrichten anzeigen, die Benutzer in Ihrer Organisation als Junk, nicht als Junk oder als Phishing gemeldet haben, indem Sie das [Add-in Berichtnachricht für Outlook und Outlook im Web](enable-the-report-message-add-in.md)verwenden. Verwenden Sie hierzu die vom [Benutzer angegebene e-Mail->](threat-explorer-views.md#email--user-reported) -Ansicht des Explorers.

1. Klicken Sie im Security & Compliance Center[https://protection.office.com](https://protection.office.com)() auf **Threat Management** > **Explorer**.
2. Wählen Sie im Menü **Ansicht** die Option **e-Mail** > **-Benutzer gemeldet**aus.<br/>![Menü ' Ansicht ' für Explorer](media/ExplorerViewMenuEmailUserReported.png)<br/>
3. Klicken Sie auf **Absender**, und wählen Sie dann **Basis** > **Berichtstyp**aus.
4. Wählen Sie eine Option wie **Phishing**aus, und klicken Sie dann auf die Schaltfläche **Aktualisieren** . <br/>![Vom Benutzer gemeldete Phishing-Nachweise](media/EmailUserReportedReportType.png)<br/> 

Der Bericht wird aktualisiert, um Daten zu e-Mail-Nachrichten anzuzeigen, die Personen in Ihrer Organisation als Phishing-Versuch gemeldet haben. Sie können diese Informationen verwenden, um eine weitere Analyse durchzuführen und gegebenenfalls Ihre [ATP-AntiPhishing-Richtlinien](set-up-anti-phishing-policies.md)anzupassen.

## <a name="start-automated-investigation-and-response"></a>Automatisierte Untersuchung und Antwort starten

(Neu!) [Automatisierte Untersuchungen und Antworten](automated-investigation-response-office.md), die kürzlich zum ATP-Plan 2 hinzugefügt wurden, können Ihre Sicherheitsteams sehr viel Zeit und Aufwand bei der Untersuchung und Milderung von Cyber-Angriffen sparen. Zusätzlich zum Konfigurieren von Warnungen, die ein Sicherheits Manuskript auslösen können, können Sie einen automatisierten unter Such-und Antwortprozess aus einer Ansicht im Explorer starten. 

Weitere Informationen hierzu finden Sie unter [Beispiel: ein Sicherheitsadministrator löst eine Untersuchung vom Threat Explorer aus](automated-investigation-response-office.md#example-a-security-administrator-triggers-an-investigation-from-threat-explorer).

## <a name="more-ways-to-use-explorer"></a>Weitere Möglichkeiten zum Verwenden des Explorers

Zusätzlich zu den in diesem Artikel beschriebenen Szenarien stehen im Explorer viele weitere Berichtsoptionen zur Verfügung. 
- [Suchen und Untersuchen von bösartigen E-Mails, die zugestellt wurden](investigate-malicious-email-that-was-delivered.md)
- [Anzeigen schädlicher Dateien, die in SharePoint Online, OneDrive und Microsoft Teams erkannt wurden](malicious-files-detected-in-spo-odb-or-teams.md)
- [Übersicht über die Ansichten im Bedrohungs-Explorer](threat-explorer-views.md)

## <a name="required-licenses-and-permissions"></a>Erforderliche Lizenzen und Berechtigungen

Der Explorer ist in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md)enthalten. 

Zum Anzeigen und Verwenden des Explorers benötigen Sie die entsprechenden Berechtigungen, beispielsweise solche, die einem Sicherheitsadministrator oder Sicherheits Leser erteilt werden. 

- Für das Security &amp; Compliance Center muss eine der folgenden Rollen zugewiesen sein:
    - Organisationsverwaltung
    - Sicherheits Administrator (kann im Azure Active Directory Admin Center[https://aad.portal.azure.com](https://aad.portal.azure.com)zugewiesen werden)
    - Sicherheits Leser

- Für Exchange Online müssen Sie über eine der folgenden Rollen verfügen, die entweder in der Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() oder mit PowerShell-Cmdlets zugewiesen sind (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Organisationsverwaltung
    - Organisationsverwaltung mit Leserechten
    - Rolle „Empfänger mit Leserechten“
    - Verwaltung der Richtlinientreue

Weitere Informationen zu Rollen und Berechtigungen finden Sie in den folgenden Ressourcen:

- [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Featureberechtigungen in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
