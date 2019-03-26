---
title: Verwenden des Bedrohungs-Explorers &amp; im Security Compliance Center
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
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Informationen zu Explorer (auch als Bedrohungs-Explorer bezeichnet) &amp; im Security Compliance Center.
ms.openlocfilehash: 202898873bb9611c747aed335d295c749c7cd0fa
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30732258"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a>Verwenden des Bedrohungs-Explorers &amp; im Security Compliance Center

Wenn Ihre Organisation [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md)enthält und Sie über die erforderlichen Berechtigungen verfügen, können Sie Threat Explorer verwenden, um Bedrohungen zu identifizieren und zu analysieren. Sie können beispielsweise infizierte e-Mails identifizieren und löschen, die übermittelt wurden, oder Malware, die von den Office 365-Sicherheitsfeatures abgefangen wurde. Threat Explorer (auch als Explorer bezeichnet) ist ein leistungsstarkes Near-Real-Time-Tool, mit dessen Hilfe Sicherheitsteams untersuchen und auf Bedrohungen &amp; im Security Compliance Center reagieren können.
  
![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
Um Explorer zu verwenden, wechseln Sie &amp; im Security Compliance Center zu **Threat Management** \> **Explorer**.

> [!IMPORTANT]
> Office 365 Threat Intelligence ist jetzt Office 365 Advanced Threat Protection Plan 2, zusammen mit zusätzlichen Funktionen zum Schutz vor Bedrohungen. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).
      
## <a name="explorer-overview"></a>Übersicht über den Explorer

Wenn Ihr Unternehmen über [Office 365 Bedrohungs Ermittlungs-und-Antwortfunktionen](office-365-ti.md) verfügt (Dies ist im ATP-Plan 2 enthalten), und Sie über die erforderlichen Berechtigungen verfügen, können Sie Threat Explorer (auch als Explorer bezeichnet) verwenden, um Bedrohungen zu identifizieren und zu analysieren. (Wechseln Sie im &amp; Security Compliance Center zu **Threat Management** \> **Explorer**.)

![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)

In diesem Artikel werden einige Dinge beschrieben, die Sie mit Explorer tun können (es gibt viel mehr Möglichkeiten):

- [Erfahren Sie, welche Arten von Schadsoftware in e-Mails erkannt wurden](#see-malware-detected-in-email-by-technology), und mit der Bedrohungsschutz Technologie (Schutz vor Schadsoftware, sichere ATP-Anhänge usw.)

- [Anzeigen von Daten zu Phishing-Links (URLs)](#view-data-about-phishing-urls-and-click-verdict), und wie die Click-Urteile (URLs wurden blockiert, erlaubt oder besucht trotz Warnungen)

- [Überprüfen von e-Mail-Nachrichten, die als Junk-, nicht Junk-oder Phishing-Nachricht gemeldet wurden](#review-email-messages-reported-by-users), und Identifizieren von Trends (beispielsweise eine größere Anzahl von Nachrichten, die als Phishing gemeldet wurden) 

## <a name="see-malware-detected-in-email-by-technology"></a>Siehe in e-Mail erkannte Schadsoftware nach Technologie

Angenommen, Sie möchten Schadsoftware erkennen, die in e-Mails erkannt wurde, und die Technologie in Office 365. Zu diesem Zweck verwenden Sie die [e-Mail-_GT_ Malware-](threat-explorer-views.md#email--malware) Ansicht des Explorers.

1. wählen sie im Office 365 Security & Compliance Center[https://protection.office.com](https://protection.office.com)() die option **Threat management** > **Explorer**aus.
2. Wählen Sie im Menü **Ansicht** die Option **e-Mail-** > **Schadsoftware**aus.<br/>![Menü ' Ansicht ' für Explorer](media/ExplorerViewEmailMalwareMenu.png)<br/>
3. Klicken Sie auf **Absender**, und wählen Sie dann **grundlegende** > **Erkennungstechnologie**aus.<br/>Ihre Erkennungstechnologien sind jetzt als Filter für den Bericht verfügbar.<br/>![Malware Erkennungstechnologien](media/ExplorerEmailMalwareDetectionTech.png)<br/> 
4. Wählen Sie eine Option aus, und klicken Sie dann auf die Schaltfläche Aktualisieren, um diesen Filter anzuwenden.<br/>![Ausgewählte Erkennungstechnologie](media/ExplorerEmailMalwareDetectionTechATP.png)<br/> 

Der Bericht wird aktualisiert, um die in e-Mails festgestellten Ergebnisse mithilfe der von Ihnen ausgewählten technologieoption anzuzeigen. Von hier aus können Sie eine weitere Analyse durchführen.

## <a name="view-data-about-phishing-urls-and-click-verdict"></a>Anzeigen von Daten zu Phishing-URLs und klicken auf "Urteil"

Angenommen, Sie möchten Phishing-Versuche über URLs in e-Mails anzeigen, einschließlich einer Liste von URLs, die zugelassen, blockiert und überschrieben wurden. Zu diesem Zweck verwenden Sie die [e-Mail-_GT_ Phishing-](threat-explorer-views.md#email--phish) Ansicht des Explorers.

1. wählen sie im Office 365 Security & Compliance Center[https://protection.office.com](https://protection.office.com)() die option **Threat management** > **Explorer**aus.
2. Wählen Sie im Menü **Ansicht** die Option **e-Mail-** > **Phishing**aus.<br/>![Menü ' Ansicht ' für Explorer](media/ExplorerViewEmailPhishMenu.png)<br/>
3. Klicken Sie auf **Absender**, und wählen Sie dann **URLs** > **Klicken Sie auf Urteil**.
4. Wählen Sie eine oder mehrere Optionen aus, beispielsweise **blockiert** und über **schrieben**, und klicken Sie dann auf die Schaltfläche **Aktualisieren** , um diesen Filter anzuwenden.<br/>![URLs und Klick Urteile](media/ThreatExplorerEmailPhishClickVerdictOptions.png)<br/>

Der Bericht wird so aktualisiert, dass erkannte Phishing-URLs in e-Mails angezeigt werden, die blockiert (oder trotz einer Warnung besucht wurden) sowie e-Mail-Zustellungsstatus. Von hier aus können Sie eine weitere Analyse durchführen. Unter dem Diagramm können Sie beispielsweise die häufigsten URLs sehen, die in den e-Mails Ihrer Organisation blockiert wurden. 

![Blockierte Explorer-URLs](media/ExplorerPhishClickVerdictURLs.png) 

Wählen Sie eine URL aus, um detailliertere Informationen anzuzeigen.

## <a name="review-email-messages-reported-by-users"></a>Überprüfende e-Mail-Nachrichten von Benutzern

Angenommen, Sie möchten e-Mail-Nachrichten anzeigen, die Benutzer in Ihrer Organisation als Junk, nicht als Junk oder als Phishing gemeldet haben, indem Sie das [Add-in Berichtnachricht für Outlook und Outlook im Web](enable-the-report-message-add-in.md)verwenden. Verwenden Sie hierzu die vom [Benutzer angegebene e-Mail->](threat-explorer-views.md#email--user-reported) -Ansicht des Explorers.

1. wählen sie im Office 365 Security & Compliance Center[https://protection.office.com](https://protection.office.com)() die option **Threat management** > **Explorer**aus.
2. Wählen Sie im Menü **Ansicht** die Option **e-Mail** > **-Benutzer gemeldet**aus.<br/>![Menü ' Ansicht ' für Explorer](media/ExplorerViewMenuEmailUserReported.png)<br/>
3. Klicken Sie auf **Absender**, und wählen Sie dann **Basis** > **Berichtstyp**aus.
4. Wählen Sie eine Option wie **Phishing**aus, und klicken Sie dann auf die Schaltfläche **Aktualisieren** . <br/>![Vom Benutzer gemeldete Phishing-Nachweise](media/EmailUserReportedReportType.png)<br/> 

Der Bericht wird aktualisiert, um Daten zu e-Mail-Nachrichten anzuzeigen, die Personen in Ihrer Organisation als Phishing-Versuch gemeldet haben. Sie können diese Informationen verwenden, um eine weitere Analyse durchzuführen und gegebenenfalls Ihre [ATP-AntiPhishing-Richtlinien](set-up-anti-phishing-policies.md)anzupassen.

## <a name="theres-more"></a>Es gibt noch mehr!

Zusätzlich zu den drei in diesem Artikel beschriebenen Szenarien stehen im Explorer viele Berichterstellungsszenarien zur Verfügung. Hier einige weitere Beispiele:

- [Suchen und untersuchen von übermittelten Schad-e-Mails](investigate-malicious-email-that-was-delivered.md)

- [Anzeigen schädlicher Dateien, die in SharePoint Online, OneDrive und Microsoft Teams erkannt wurden](malicious-files-detected-in-spo-odb-or-teams.md)

- [Übersicht über die Ansichten im Bedrohungs-Explorer](threat-explorer-views.md)

## <a name="how-to-get-explorer"></a>Abrufen des Explorers

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

Weitere Informationen finden Sie in den folgenden Ressourcen:

- [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Featureberechtigungen in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
  
## <a name="related-topics"></a>Verwandte Themen

- [Automatisierte Untersuchung und Antwort (AIR)](automated-investigation-response-office.md)

- [Ansichten des Bedrohungs-Explorers](threat-explorer-views.md)

- [Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)
