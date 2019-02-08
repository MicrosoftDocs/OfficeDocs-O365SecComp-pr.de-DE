---
title: Übersicht über die Sicherheit-dashboard
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/07/2019
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: fe0b9b8f-faa9-44ff-8095-4d1b2f507b74
description: Verwenden Sie das neue Dashboard Sicherheit, um Office 365 Threat Protection Status überprüfen und anzeigen und Bearbeiten von Sicherheitswarnungen.
ms.openlocfilehash: c393513d08762785eab44102fa83680531a49b53
ms.sourcegitcommit: c2ec9a4b0279a248b85c2e4a4e91458214b5b31c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/08/2019
ms.locfileid: "29770800"
---
# <a name="security-dashboard"></a>Sicherheits-Dashboard

## <a name="overview"></a>Übersicht

Die [Sicherheit &amp; Compliance Center](go-to-the-securitycompliance-center.md) ermöglicht Ihrem Unternehmen zum Verwalten von Datenschutz und Compliance. Vorausgesetzt, dass Sie die erforderlichen Berechtigungen verfügen, können das Dashboard Sicherheit Sie Ihren Schutzstatus Bedrohung überprüfen als auch anzeigen und Bearbeiten von Sicherheitswarnungen. 
  
Video ansehen, wenn Sie eine Übersicht über erhalten möchten, und Lesen Sie diesen Artikel, um mehr zu erfahren.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/3540b1f8-62d2-47fa-a07d-d7ad76f55b0f?autoplay=false]
  
Je nachdem, welche Ihrer Organisation-Office 365-Abonnement umfasst, enthält das Dashboard Sicherheit mehrere Widgets, wie etwa Threat Management Zusammenfassung, Bedrohung Schutzstatus, globale wöchentliche Bedrohung erkannte, Malware und mehr, wie beschrieben in der folgenden Abschnitten.
  
Zum Anzeigen des Dashboards Sicherheit in der [Sicherheit in Office 365 &amp; Compliance Center](go-to-the-securitycompliance-center.md), wechseln Sie zu **Verwaltung der Bedrohung** \> **Dashboard**.
  
> [!NOTE]
> Sie müssen ein globaler Office 365-Administrator, einen Sicherheitsadministrator oder ein Sicherheit Reader zum Anzeigen des Dashboards Sicherheit sein. Einige Widgets erfordern zusätzliche Berechtigungen zum Anzeigen. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md). 
  
## <a name="threat-management-summary"></a>Threat Management Zusammenfassung

Das Widget Threat Management Zusammenfassung erfahren Sie auf einen Blick wie Ihre Organisation in den letzten sieben (7) Tagen vor Angriffen geschützt wurde.

![Sicherheits-Dashboard - Widget Threat Management Zusammenfassung](media/SecDash-ThreatMgmtSummary.png)

Die Informationen, die Sie in der Zusammenfassung der Threat Management sehen werden, hängt davon ab, was Sie-Abonnement umfasst. In der folgenden Tabelle wird beschrieben, welche Informationen für Office 365 Enterprise E3 und Office 365 Enterprise E5 enthalten sind.


|Office 365 Enterprise E3  |Office 365 Enterprise E5  |
|---------|---------|
|Malware Nachrichten blockiert<br/>Blockiert Phishing-Nachrichten<br>Nachrichten, die vom Benutzer gemeldet wurde<br><br><br><br> |Malware Nachrichten blockiert<br>Blockiert Phishing-Nachrichten<br>Nachrichten, die vom Benutzer gemeldet wurde<br>Zero-Day-Schadsoftware blockiert<br>Erweiterte Phishingnachrichten erkannt<br>Schädliche URLs blockiert |

Um anzuzeigen, oder das Widget Threat Management Zusammenfassung zuzugreifen, müssen Sie die Berechtigung zum Anzeigen der erweiterte Schutz-Berichte verfügen. Weitere Informationen finden Sie unter [Welche Berechtigungen erforderlich sind, um die ATP-Berichte anzeigen?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="threat-protection-status"></a>Bedrohung Schutzstatus

Das Widget Bedrohung Schutzstatus zeigt Threat Protection Effektivität eine Trend und detaillierte Ansicht der Phishing und Malware. 

![Threat Protection Status widget](media/tpswidget.png)

Die Details hängen davon ab, ob Ihr Office 365-Abonnement [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP) mit oder ohne [Office 365 erweiterte Threat Protection](office-365-atp.md) (ATP) enthält.


|Wenn Ihr Abonnement enthält... |Sehen Sie diese details |
|---------|---------|
|EOP jedoch nicht Office 365 ATP     |Böswillige e-Mail, die wurde erkannt und blockiert von EOP gefiltert werden<br> Finden Sie unter [Threat Protection Statusbericht (EOP)](view-email-security-reports.md#threat-protection-status-report).| |
|Office 365 ATP |Bösartige Webinhalte und Schadsoftware e-Mails erkannt und von EOP und Office 365 ATP blockiert<br>Aggregierte Anzahl eindeutiger e-Mail-Nachrichten mit schädlichem Inhalt vom antischadsoftwaremodul, [0 (null)-Stunden automatisch löschen](zero-hour-auto-purge.md)und ATP-Funktionen (einschließlich [Sicherer Links](atp-safe-links.md), [Sichere Anlagen](atp-safe-attachments.md)und [ATP Phishing](atp-anti-phishing.md)) blockiert.<br>Finden Sie unter [Threat Protection Statusbericht (ATP)](view-reports-for-atp.md#threat-protection-status-report). | 

Um anzuzeigen, oder das Widget Bedrohung Schutzstatus zuzugreifen, müssen Sie die Berechtigung zum Anzeigen der erweiterte Schutz-Berichte verfügen. Weitere Informationen finden Sie unter [Welche Berechtigungen erforderlich sind, um die ATP-Berichte anzeigen?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

## <a name="global-weekly-threat-detections"></a>Globale wöchentliche Bedrohung erkannte
 
Das Widget globale wöchentliche Bedrohung erkannte zeigt, wie viele Bedrohungen in e-Mail-Nachrichten in den letzten sieben (7) Tagen erkannt wurden.

![Globale wöchentliche Bedrohung erkannte widget](media/globalweeklythreatdetections.png)

Die Metriken werden berechnet, wie in der folgenden Tabelle beschrieben:

|Metrik  |Wie berechnet  |
|---------|---------|
|Nachrichten, die gescannt |Anzahl der e-Mail-Nachrichten überprüft und der Anzahl von Empfängern |
|Bedrohungen beendet  |Anzahl der e-Mail-Nachrichten, die als mit Malware und der Anzahl von Empfängern |
|Von [ATP](office-365-atp.md) blockiert |Anzahl der e-Mail-Nachrichten, die durch die Anzahl von Empfängern multipliziert ATP blockiert |
|Nach der Übermittlung entfernt |Anzahl der Nachrichten, die durch [null-Stunden automatisch löschen](zero-hour-auto-purge.md) und der Anzahl von Empfängern entfernt |

## <a name="malware"></a>Schadsoftware

Malware Widgets zeigt Details zu Malwaretrends und Malware-Produktfamilie Typen in den letzten sieben (7) Tagen.

![Malwaretrends und Typen der Familien](media/malwarewidgetatpe5.png)
 
## <a name="insights"></a>Einblicke

Einblicke in die Oberfläche nicht nur wichtige Punkte, die Sie überprüfen sollten, dazu gehören auch Empfehlungen und Aktionen zu berücksichtigen sind. 

![Intelligente insights](media/smartinsights.png)

Beispielsweise können Sie sehen, dass Phishing-e-Mail-Nachrichten gesendet werden, da einige Benutzer ihre Junk-e-Mail-Optionen deaktiviert haben. Erfahren Sie mehr über die Funktionsweise von Insights, finden Sie unter [Berichte und Einblicke in die Office 365-Sicherheit &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md).
  
## <a name="threat-intelligence"></a>Bedrohungsanalyse

Wenn Abonnement Ihrer Organisation [Threat Intelligence-Funktionen](office-365-ti.md)enthält, hat Ihr Dashboard Sicherheit einen **Bedrohungsanalyse** Abschnitt, erweiterte Tools. Security-Team Ihrer Organisation können die Informationen in diesem Abschnitt neue Kampagnen verstehen, untersuchen Bedrohungen und Verwalten von Vorfälle. 
  
![Bedrohungsanalyse hilft Ihnen das Verständnis von Ihrer Organisation in der Übergangsphase Angriffe](media/threatintelwidget.png)
  
  
## <a name="trends"></a>Trends

Am unteren Rand des Dashboards Sicherheit ist ein Abschnitt **Trends** , der e-Mail-Fluss Trends für Ihre Organisation zusammenfasst. Berichte enthalten Informationen zu e-Mail als Spam, Malware, Phishing-Versuche und eine gute e-Mail kategorisiert. Klicken Sie auf eine Kachel, um ausführlichere Informationen im Bericht anzuzeigen. 
  
![Im Abschnitt Trends Überblick über die e-Mail-Fluss Trends für die Organisation](media/trends.png)
  
Und wenn Ihre Organisation Office 365-Abonnements [Threat Intelligence-Funktionen](office-365-ti.md)enthält, haben Sie einen Bericht **letzten Threat Management** in diesem Abschnitt, die zum Anzeigen und Ausführen einer Aktion auf Security Team ermöglicht Sicherheitshinweise mit hoher Priorität. 

Um anzuzeigen, oder das Widget gesendete und empfangene E-Mails zugreifen, müssen Sie die Berechtigung zum Anzeigen der erweiterte Schutz-Berichte verfügen. Weitere Informationen finden Sie unter [Welche Berechtigungen erforderlich sind, um die ATP-Berichte anzeigen?](view-reports-for-atp.md#what-permissions-are-needed-to-view-the-atp-reports). 

Um anzuzeigen, oder das Widget Threat Management letzten zugreifen, benötigen Sie Berechtigungen zum Anzeigen von Warnungen. Finden Sie weitere Informationen finden Sie unter [RBAC-Berechtigungen erforderlich, um Warnungen anzuzeigen](alert-policies.md#rbac-permissions-required-to-view-alerts).
  
## <a name="related-topics"></a>Verwandte Themen

[Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center](view-email-security-reports.md)
  
[Anzeigen von Berichten für Office 365 erweiterte Threat Protection](view-reports-for-atp.md)
  
[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Informationen zu Bedrohungen in Office 365](office-365-ti.md)
  

