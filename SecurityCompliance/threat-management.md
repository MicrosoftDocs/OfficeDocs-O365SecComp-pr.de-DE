---
title: Threat management in the Office 365 Security &amp; Compliance Center
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 9/24/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 0a73d5fa-b2c8-43e7-9ed4-61f0552b1c98
description: Verwenden von Threat Management kontrollieren und Verwalten von mobilen Gerätezugriff auf die Daten des Unternehmen, Ihre Organisation vor Datenverlust schützen, und eingehende und ausgehende Nachrichten vor Schadsoftware und Spam schützen. Sie können auch Bedrohung, dass Management zum Schutz Ihrer Domäne und um zu bestimmen, ob Absender in böswilliger Absicht spoofing sind oder nicht von Ihrer Domäne Konten verwenden.
ms.openlocfilehash: fc7d0a3fd73c03e6eec6cfd265edbf3c47ce1803
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29652250"
---
# <a name="threat-management-in-the-office-365-security-amp-compliance-center"></a>Threat management in the Office 365 Security &amp; Compliance Center

Verwenden von Threat Management kontrollieren und Verwalten von mobilen Gerätezugriff auf die Daten des Unternehmen, Ihre Organisation vor Datenverlust schützen, und eingehende und ausgehende Nachrichten vor Schadsoftware und Spam schützen. Sie können auch Bedrohung, dass Management zum Schutz Ihrer Domäne und um zu bestimmen, ob Absender in böswilliger Absicht spoofing sind oder nicht von Ihrer Domäne Konten verwenden.
  
## <a name="how-to-view-and-use-threat-management-in-the-security-amp-compliance-center"></a>Zum Anzeigen und Verwenden von Threat Management in das Wertpapier &amp; Compliance Center

Verwenden Sie die Sicherheit in Office 365, &amp; Compliance Center Bedrohungen in Ihrer Organisation zu verwalten.
  
 **So rufen direkt auf die Sicherheit &amp; Compliance Center:**
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com).

2. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.

3. Wählen Sie im linken Bereich **Threat Management**.

    ![Office 365-Sicherheit &amp; Compliance Center Threat Management-Menü](media/dca29ff2-ad6d-4c27-becb-b5947268d55a.png)
  
 **So rufen die Sicherheit &amp; Compliance Center mit Office 365-app-Start:**
  
1. Melden Sie sich bei Office 365 mit Ihrem Geschäfts-, Schul- oder Unikonto an.

2. Wählen Sie dieses Startprogramm app ![das app-Start-Symbol in Office 365](media/7502f4ec-3c9a-435d-a7b4-b9cda85189a7.png) in der oberen rechten Ecke, und wählen Sie dann die **Sicherheit &amp; Compliance** Kachel. 

3. Wählen Sie im linken Bereich **Threat Management**.

## <a name="about-threat-management-in-office-365"></a>Informationen zur Verwaltung von Bedrohung in Office 365

Diese Optionen sind verfügbar unter **Threat Management** in das Wertpapier &amp; Compliance Center.
  
Wir sind noch Rollout Threat Management für die Sicherheit &amp; Compliance Center, damit Sie möglicherweise nicht finden Sie alle diese noch oder Sie möglicherweise mehr als die Optionen hier aufgeführt. Während der Einführung verbleiben einige dieser, beispielsweise Anti-Malware Dkim und andere, über das Exchange Admin Center (EAC) für kurze Zeit zur Verfügung.

In einigen Fällen sind Unterschiede bestehen zwischen der Exchange-Verwaltungskonsole und die Sicherheit &amp; Compliance Center Implementierungen. Beispielsweise sind die unterstützte Zeichen für Spam-Filter zwischen den beiden Plattformen unterschiedlich. Artikel stehen zur Verfügung, die enthalten weitere Informationen zu bestimmten Unterschiede, wenn sie anfallen.
  
|**Tool**|**Beschreibung**|
|:-----|:-----|
|**Dashboard, Threat Explorer und Vorfälle** <br/> |Nach der Aktivierung möglich dieser Bereiche Sie zum Verwalten von Office 365 Analytics und Threat Intelligence. Weitere Informationen finden Sie unter [Übersicht über die Office 365-Bedrohungsanalyse](office-365-ti.md).<br/> |
|**Mail-Filterung** <br/> |Optimieren Sie und überwachen Sie die Einstellungen, die verhindern, dass Spam in Office 365. Erstellen Sie zulassen und bestimmen, wer Ihre Domäne spoofing ist, blockierte Kontakte und Gründe, und konfigurieren, und zeigen Sie Richtlinien für Spam-Filter. Weitere Informationen finden Sie unter [Office 365 e-Mail-Anti-Spam-Schutz](anti-spam-protection.md).<br/> Sie können auch eine Richtlinie festlegen, um zu überprüfen, dass Ihre Benutzer Spam senden sind nicht. Dies kann beispielsweise auftreten, wenn der Computer des Benutzers mit Malware infiziert Ruft ab, die zum Senden von e-Mail-Nachrichten programmiert ist. Um Hier erfahren Sie, wie Sie ausgehenden Spamnachrichten verhindern können, finden Sie unter [Konfigurieren der Richtlinie für ausgehende Spamnachrichten](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx).<br/> Wenn Sie derzeit ein Problem mit Spam auftritt, können Sie den [Spam und Malware-Problembehandlung](https://configure.office.com/Scenario.aspx?sid=73).           |
|**Antischadsoftware** <br/> |Schützt vor Viren und Spyware auf Reisen oder von Ihrer Organisation in Office 365. Viren sind bösartige Software-Programme, die bei der Ausführung, sich selbst replizieren und anderen Programmen und Daten auf dem Computer zu ändern. Viren verteilt auf Ihrem Computer Programme infiziert gesucht und auch von einem Computer zu einem anderen häufig durch e-Mail freigegeben. Spyware sammelt Ihrer persönlichen Informationen, wie etwa-Anmeldung Informationen und sendet sie an den Autor zurück. Wenn Sie die ersten Schritte beim Konfigurieren der Antischadsoftware-Richtlinien, finden Sie unter [Configure Anti-Malware Policies](https://technet.microsoft.com/library/jj200745%28v=exchg.150%29.aspx).<br/> Wenn Sie derzeit ein Problem mit Malware auftritt, können Sie den [Spam und Malware-Problembehandlung](https://configure.office.com/Scenario.aspx?sid=73).           |
|**DKIM** <br/> |DomainKeys Identified Mail (DKIM), für die direkte Verwendung für erweiterte Office 365-Administratoren, aber für alle Office 365-Kunden verfügbar, wird sichergestellt, dass andere e-Mail-Systemen Nachrichten vertrauen, die Sie von Office 365 senden. DKIM geschieht durch Hinzufügen einer eindeutigen digitalen Signatur für e-Mail-Nachrichten, die Sie von Ihrer Organisation zu senden. E-Mail-Systemen, die von Ihnen e-Mail empfangen können diese digitale Signatur zu ermitteln, ob die e-Mail legitime ist.<br/> Kein Problem, wenn die Details der Funktionsweise kompliziert erscheinen, da die Standardeinstellung, die in Office 365 für Sie eingerichtet ist für die meisten Organisationen arbeiten darf. Wenn Sie nicht von mit DKIM selbst festlegen, verwendet Office 365 die Standardrichtlinie und Schlüssel, die erstellt wird, um DKIM für Ihre Domäne zu aktivieren. Wenn Sie DKIM Signieren deaktivieren, nach einer gewissen Zeitraum ermöglicht Office 365 außerdem automatisch die Office 365-Standardrichtlinie für Ihre Domäne.<br/> Wenn Sie möchten, können Sie diese Seite anzeigen, in das Wertpapier &amp; Compliance Center und finden Sie unter unabhängig davon, ob DKIM Signaturen für Ihre Domäne, und Sie derzeit aktiviert sind, können das letzte Mal die Verschlüsselungsschlüssel von Office 365 verwendete gedreht wurden anzeigen. Sie können auch manuell selbst die Schlüssel drehen.<br/> **Wichtig!** DKIM ist nur eine e-Mail-Authentifizierungstechnik von Office 365 verwendet. Um möglichst effizient zu können, wird mit DKIM zusammen mit anderen unterstützten Techniken wie Sender Policy Framework (SPF) und domänenbasierte Nachrichtenauthentifizierung, Berichte und Konformität (DMARC) verwendet. Gemeinsam helfen diese Technologien domänenbasierte Authentifizierung Spam und unerwünschte spoofing zu verhindern.<br/>  Vor dem Ändern der Sicherheit mit DKIM &amp; Compliance Center, vertraut werden mit der Technologie und deren Funktionsweise. Zum Einstieg finden Sie unter [weiterführendes: Weitere Möglichkeiten zur Verhinderung von Spam in Office 365](anti-spam-protection.md#beyond-the-basics-more-ways-to-prevent-spam-in-office-365).           |
|**Sichere Anlagen**<br/>|[Sichere Anlagen](atp-safe-attachments.md) ist Teil der erweiterte Schutz. Wenn aktiviert, werden e-Mail-Anlagen in einer speziellen, isolierte Umgebung geöffnet, die nicht Bestandteil von Office 365, bevor sie an die Posteingänge Empfänger gesendet werden. Sichere Anlagen ist darauf ausgelegt, bösartige Anlagen erkennen, bevor Antiviren-Signaturen zur Verfügung stehen. Weitere Informationen finden Sie unter [Sichere Anlagen in Office 365](atp-safe-attachments.md).<br/> |
|**Sichere Links** <br/> |[Sichere Links](atp-safe-links.md) ist Teil der erweiterte Schutz. Sichere Links können verhindern, dass Benutzer in der folgenden URLs in e-Mail-Nachricht oder in Office-Dokumenten, die auf Websites zu verweisen, die als böswillige erkannt werden. Finden Sie weitere Informationen finden Sie unter [Sichere Links in Office 365](atp-safe-links.md).<br/> |
|**Quarantäne**<br/>|Einrichten von [Quarantäne](http://go.microsoft.com/fwlink/p/?LinkID=809005) für eingehende e-Mail-Nachrichten in Office 365 Massen-Nachrichten, die als Spam gefiltert wurden, in dem, Phishing und Malware Mail kann für die spätere Verwendung gespeichert werden. Nachrichten in Quarantäne können Benutzer und-Administratoren entwickelt. Benutzer können nur eigene gefilterten Nachrichten in Quarantäne entwickelt. Administratoren können Suchen und Verwalten von Nachrichten in Quarantäne für alle Benutzer.<br/> |
|**Erweiterte Bedrohungen** <br/> |Anzeigen des [Threat Protection Statusbericht](https://support.office.com/article/View-the-reports-for-Advanced-Threat-Protection-E47E838C-D99E-4C0B-B9AA-E66C4FAE902F#advancedthreats) um finden Informationen über die bösartige Inhalte gefunden haben, und von Exchange Online Protection und erweiterte Schutz blockiert.  <br/> |
