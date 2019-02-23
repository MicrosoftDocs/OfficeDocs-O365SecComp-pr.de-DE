---
title: Übersicht über das Sicherheits Dashboard
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/07/2019
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: fe0b9b8f-faa9-44ff-8095-4d1b2f507b74
ms.collection: M365-security-compliance
description: Verwenden Sie das neue Sicherheits Dashboard, um den Status der BedrohungsSchutz in Office 365 zu überprüfen und Sicherheitswarnungen anzuzeigen und zu bearbeiten.
ms.openlocfilehash: 7fcf570887e5ed720e2e62d627b442597b824e84
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215174"
---
# <a name="security-dashboard"></a>Sicherheits Dashboard

## <a name="overview"></a>Übersicht

Mit [dem &amp; Security Compliance Center](go-to-the-securitycompliance-center.md) kann Ihre Organisation Datenschutz und-Compliance verwalten. Unter der Voraussetzung, dass Sie über die erforderlichen Berechtigungen verfügen, können Sie mithilfe des Sicherheits Dashboards den Status des BedrohungsSchutzes überprüfen und Sicherheitswarnungen anzeigen und bearbeiten. 
  
Sehen Sie sich das Video an, um einen Überblick zu erhalten, und lesen Sie diesen Artikel, um mehr zu erfahren.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/3540b1f8-62d2-47fa-a07d-d7ad76f55b0f?autoplay=false]
  
Je nach dem, was das Office 365-Abonnement Ihrer Organisation enthält, enthält das Sicherheits Dashboard mehrere Widgets, wie etwa die Zusammenfassung der Bedrohungs Verwaltung, den Status des BedrohungsSchutzes, globale wöchentliche Bedrohungs Erkennungsmethoden, Schadsoftware und vieles mehr, wie im Abschnitte.
  
wechseln sie zum anzeigen des sicherheits dashboards im [Office 365 &amp; security Compliance Center](go-to-the-securitycompliance-center.md)zu **Threat management** \> **dashboard**.
  
> [!NOTE]
> Sie müssen ein globaler Office 365-Administrator, ein Sicherheitsadministrator oder ein Sicherheits-Lesegerät sein, um das Sicherheits Dashboard anzuzeigen. Einige Widgets erfordern zusätzliche Berechtigungen zum anzeigen. Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="threat-management-summary"></a>Zusammenfassung der Bedrohungs Verwaltung

Das zusammenfassende Widget "Threat Management" informiert Sie auf einen Blick, wie Ihre Organisation vor Bedrohungen in den letzten sieben (7) Tagen geschützt wurde.

![Sicherheits Dashboard-Widget "Zusammenfassung der Bedrohungs Verwaltung"](media/SecDash-ThreatMgmtSummary.png)

Die Informationen, die Sie in der Zusammenfassung der Bedrohungs Verwaltung sehen, hängen davon ab, was Ihr Abonnement enthält. In der folgenden Tabelle wird beschrieben, welche Informationen für Office 365 Enterprise E3 und Office 365 Enterprise E5 enthalten sind.


|Office 365 Enterprise E3  |Office 365 Enterprise E5  |
|---------|---------|
|Blockierte Schadsoftware<br/>Blockierte Phishing-Nachrichten<br>Von Benutzern gemeldete Nachrichten<br><br><br><br> |Blockierte Schadsoftware<br>Blockierte Phishing-Nachrichten<br>Von Benutzern gemeldete Nachrichten<br>Blockierte Zero-Day-Schadsoftware<br>Erweiterte Phishing-Nachrichten erkannt<br>Blockierte bösartige URLs |

Zum Anzeigen oder zugreifen auf das zusammenfassende Widget für die Bedrohungs Verwaltung benötigen Sie Berechtigungen zum Anzeigen von Advanced Threat Protection-Berichten. Weitere Informationen finden Sie unter [welche Berechtigungen sind erforderlich, um die ATP-Berichte anzuzeigen](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="threat-protection-status"></a>Status des BedrohungsSchutzes

Das Widget Threat Protection Status zeigt die Effektivität des Schutz vor Bedrohungen mit einer Trend-und Detailansicht von Phishing und Schadsoftware. 

![Widget "Threat Protection Status"](media/tpswidget.png)

Die Details hängen davon ab, ob Ihr Office 365 [-Abonnement Exchange Online Protection](eop/exchange-online-protection-eop.md) (EoP) mit oder ohne [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) enthält.


|Wenn Ihr Abonnement enthält... |Diese Details werden angezeigt. |
|---------|---------|
|EOP, jedoch nicht Office 365 ATP     |Bösartige e-Mails, die von EOP erkannt und blockiert wurden<br> Siehe [Threat Protection Status Report (EoP)](view-email-security-reports.md#threat-protection-status-report).| |
|Office 365 ATP |Bösartige Inhalte und bösartige e-Mails, die von EOP und Office 365 ATP erkannt und blockiert wurden<br>Aggregierte Anzahl von eindeutigen e-Mail-Nachrichten mit bösartigen Inhalten, die vom Antischadsoftware-Modul blockiert wurden, [Zero-Hour-automatische Bereinigung](zero-hour-auto-purge.md)und ATP-Funktionen (einschließlich [sicherer Links](atp-safe-links.md), [sicherer Anlagen](atp-safe-attachments.md)und [ATP-Phishing](atp-anti-phishing.md)).<br>Siehe [Threat Protection Status Report (ATP)](view-reports-for-atp.md#threat-protection-status-report). | 

Zum Anzeigen oder zugreifen auf das Widget Threat Protection Status benötigen Sie Berechtigungen zum Anzeigen von Advanced Threat Protection-Berichten. Weitere Informationen finden Sie unter [welche Berechtigungen sind erforderlich, um die ATP-Berichte anzuzeigen](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="global-weekly-threat-detections"></a>Globale wöchentliche BedrohungsEntdeckungen
 
Das Widget "globale wöchentliche BedrohungsErkennungen" zeigt, wie viele Bedrohungen in e-Mail-Nachrichten in den letzten sieben (7) Tagen erkannt wurden.

![Widget "globale wöchentliche Bedrohungs Ermittlungen"](media/globalweeklythreatdetections.png)

Die Metriken werden wie in der folgenden Tabelle beschrieben berechnet:

|Metrik  |Berechnung  |
|---------|---------|
|Gescannte Nachrichten |Anzahl der gescannten e-Mail-Nachrichten multipliziert mit der Anzahl der Empfänger |
|Bedrohungen gestoppt  |Anzahl der e-Mail-Nachrichten, die mit der Anzahl von Empfängern mit Schadsoftware multipliziert wurden |
|Gesperrt von [ATP](office-365-atp.md) |Anzahl der von ATP blockierten e-Mail-Nachrichten multipliziert mit der Anzahl der Empfänger |
|Nach der Lieferung entfernt |Anzahl der Nachrichten, die von der [automatischen Bereinigung von Null Stunden](zero-hour-auto-purge.md) entfernt wurden, multipliziert mit der Anzahl der Empfänger |

## <a name="malware"></a>Schadsoftware

Malware-Widgets zeigen in den letzten sieben (7) Tagen Details zu Malware Trends und Schadsoftware-Familientypen.

![Malware Trends und Familientypen](media/malwarewidgetatpe5.png)
 
## <a name="insights"></a>Einblicke

EinBlicke nicht nur die wichtigsten Probleme, die Sie überprüfen sollten, Sie auch Empfehlungen und Maßnahmen zu berücksichtigen. 

![Intelligente Einblicke](media/smartinsights.png)

So können Sie beispielsweise feststellen, dass Phishing-e-Mails übermittelt werden, da einige Benutzer Ihre Junk-e-Mail-Optionen deaktiviert haben. Weitere Informationen zur Funktionsweise von Einblicken finden Sie unter [Berichte und Einblicke &amp; im Office 365 Security Compliance Center](reports-and-insights-in-security-and-compliance.md).
  
## <a name="threat-intelligence"></a>Bedrohungs Intelligenz

Wenn das Abonnement Ihrer Organisation [Bedrohungen Intelligence-Funktionen](office-365-ti.md)enthält, weist Ihr Sicherheits Dashboard einen Abschnitt " **Threat Intelligence** " auf, der erweiterte Tools enthält. Das Sicherheitsteam Ihrer Organisation kann die Informationen in diesem Abschnitt verwenden, um sich mit neuen Kampagnen vertraut zu machen, Bedrohungen zu untersuchen und Vorfälle zu verwalten. 
  
![Threat Intelligence hilft Ihnen bei der Veranschaulichung von Angriffen in Ihrer Organisation](media/threatintelwidget.png)
  
  
## <a name="trends"></a>Trends

Am unteren Rand des Sicherheits Dashboards befindet sich ein Abschnitt **Trends** , in dem die Trends für den e-Mail-Fluss für Ihre Organisation zusammengefasst werden. Berichte bieten Informationen zu e-Mails, die als Spam, Schadsoftware, Phishing-Versuche und gute e-Mails kategorisiert werden. Klicken Sie auf eine Kachel, um detailliertere Informationen im Bericht anzuzeigen. 
  
![Im Abschnitt Trends werden die Trends für den e-Mail-Fluss für die Organisation zusammengefasst.](media/trends.png)
  
Und wenn das Office 365-Abonnement Ihrer Organisation [Threat Intelligence-Funktionen](office-365-ti.md)enthält, haben Sie auch einen **aktuellen Bericht über Warnmeldungen zur Gefahren Verwaltung** in diesem Abschnitt, der Ihrem Sicherheitsteam das Anzeigen und Ausführen von Aktionen ermöglicht. Sicherheitswarnungen mit hoher Priorität. 

Zum Anzeigen oder zugreifen auf das gesendete und empfangene e-Mail-widget benötigen Sie Berechtigungen zum Anzeigen von Advanced Threat Protection-Berichten. Weitere Informationen finden Sie unter [welche Berechtigungen sind erforderlich, um die ATP-Berichte anzuzeigen](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

Zum Anzeigen oder zugreifen auf das kürzlich veröffentlichte Widget "Threat Management Alerts" benötigen Sie Berechtigungen zum Anzeigen von Warnungen. Weitere Informationen finden Sie unter [RBAC Permissions Required to View Alerts](alert-policies.md#rbac-permissions-required-to-view-alerts).
  
## <a name="related-topics"></a>Verwandte Themen

[Anzeigen von e-Mail-Sicherheits &amp; Berichten im Security Compliance Center](view-email-security-reports.md)
  
[Anzeigen von Berichten für Office 365 Advanced Threat Protection](view-reports-for-atp.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Informationen zu Bedrohungen in Office 365](office-365-ti.md)
  

