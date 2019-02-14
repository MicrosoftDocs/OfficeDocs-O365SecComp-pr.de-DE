---
title: Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/07/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection: M365-security-compliance
description: Informationen Sie zum Suchen und Verwenden von e-Mail-Sicherheitsberichte für Ihre Organisation mit Office 365 Enterprise. E-Mail-Sicherheitsberichte stehen in der Sicherheit &amp; Compliance Center.
ms.openlocfilehash: 0c9b4c4c75f1e2996217bea600b9d36145b30339
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995296"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a>Anzeigen von e-Mail-Sicherheitsberichte in das Wertpapier &amp; Compliance Center

Eine Vielzahl von e-Mail-Sicherheitsberichte stehen in der [Sicherheit &amp; Compliance Center](https://security.microsoft.com) mit denen Sie die finden Sie unter wie Antispam- und Antischadsoftware-Features in Office 365 Ihrer Organisation geschützt sind. Wenn Sie die [erforderlichen Berechtigungen](#what-permissions-are-needed-to-view-these-reports)verfügen, können Sie diese Berichte anzeigen, in das Wertpapier &amp; Compliance Center auf **Berichte** zugreifen, indem \> **Dashboard**.
  
![Die Sicherheit &amp; Compliance Center-Dashboard kann Ihnen finden Sie unter, in dem erweiterte Schutz funktionsfähig ist](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
Ihre e-Mail-Sicherheitsberichte umfassen Folgendes:
  
- [Threat Protection Statusbericht](view-email-security-reports.md#tps) 
    
- [Erkannte Schadsoftware Bericht](view-email-security-reports.md#maldet)
    
- [Top-Schadsoftware-Bericht](#top-malware-report)
    
- [Obere Absendern und Empfängern Bericht](view-email-security-reports.md#topsenders)
    
- [Spoofing der e-Mail-Bericht](#spoof-mail-report)
    
- [Bericht Spamerkennungen](#spam-detections-report)
    
- [Gesendete und empfangene e-Mail-Bericht](view-email-security-reports.md#sentreceivedemail)
    
- [Benutzer gemeldete Nachrichten Bericht](view-email-security-reports.md#userreported) (neu!) 
    
## <a name="threat-protection-status-report"></a>Threat Protection Statusbericht

Der neue **Threat Protection** Statusbericht ist smart Bericht mit böswilligen Absichten e-Mail, die erkannt und von Exchange Online Protection blockiert wurde. In diesem Bericht werden Informationen zu e-Mails, die als Malware oder Phishing-Versuch identifiziert. 

> [!NOTE]
> Ein Bericht Bedrohung Schutzstatus steht Kunden mit [Office 365 ATP](office-365-atp.md) oder [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); Allerdings werden die Informationen, die im Bericht Schutzstatus Bedrohung für ATP-Kunden angezeigt wird wahrscheinlich andere Daten als was EOP-Kunden finden Sie unter möglicherweise enthalten. EOP-Kunden können beispielsweise Schadsoftware erkannt in e-Mails, die aber nicht Informationen zu [schädliche Dateien in SharePoint Online, OneDrive, oder Microsoft-Teams erkannt](atp-for-spo-odb-and-teams.md), eine Funktion ATP-spezifische Informationen anzeigen. ([Erfahren Sie mehr über Berichte ATP](view-reports-for-atp.md)).
  
Zum Anzeigen dieser Bericht in der [Sicherheit &amp; Compliance Center](https://protection.office.com), wechseln Sie zu **Berichte** \> **Dashboard** \> **Bedrohung Schutzstatus**.
  
![Threat Protection Statusbericht](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
Wenn Sie den Threat Protection Statusbericht zum ersten Mal öffnen, zeigt der Bericht Daten für die letzten sieben Tage standardmäßig; Sie können jedoch auf **Filter** und den Datumsbereich für bis zu 90 Tage Detailebene ändern. In diesem Bericht eignet sich für die Anzeige der Effizienz und der Auswirkung von Ihrer Organisation Exchange Online Protection Features und für längerfristige Trend. 
  
![Bedrohung Schutzstatus Berichtsfilter](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
Sie können auch auswählen, ob zum Anzeigen von Daten für e-Mails, die als böswillige e-Mail identifiziert, wie ein Phishing versucht, oder e-Mail identifiziert Schadsoftware enthält.
  
![Bedrohung Schutzstatus Bericht anzeigen von Optionen](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a>Erkannte Schadsoftware Bericht

Der **Erkannte Schadsoftware** Bericht zeigt, wie viele ein- und ausgehende Nachrichten als mit Malware für Ihre Organisation erkannt wurden. 
  
Zum Anzeigen dieser Bericht in der [Sicherheit &amp; Compliance Center](https://protection.office.com), wechseln Sie zu **Berichte** \> **Dashboard** \> **Schadsoftwareerkennungen**.
  
![Beispiel für Schadsoftware erkannte Bericht](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
Andere Berichte, wie ein Bericht Bedrohung Schutzstatus ähnelt der Bericht Daten für die letzten sieben Tage standardmäßig angezeigt. Sie können jedoch **Filter** , um den Datumsbereich zu ändern. 
  
## <a name="top-malware-report"></a>Top-Schadsoftware-Bericht

Der **Oben Malware** Bericht werden die verschiedenen Arten von Schadsoftware, die von Exchange Online gefunden wurde. 
  
Zum Anzeigen dieser Bericht in der [Sicherheit &amp; Compliance Center](https://protection.office.com), wechseln Sie zu **Berichte** \> **Dashboard** \> **Oben Malware**.
  
![SCC - EOP wichtigste Schadsoftware](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
Wenn Sie über eine Keil im Kreisdiagramm bewegen, sehen Sie den Namen von der Art der Malware und wie viele Nachrichten mit, dass Malware erkannt wurden.
  
Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).
  
![In diesem Bericht werden die wichtigste Schadsoftware erkannt für Ihre Organisation](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
Unter dem Diagramm sehen Sie eine Liste der erkannten Malware und wie viele Nachrichten mit, dass Malware erkannt wurden.
  
## <a name="top-senders-and-recipients-report"></a>Obere Absendern und Empfängern Bericht

Der **häufigste Absender und Empfänger** Bericht ist ein Kreisdiagramm Ihre oberen e-Mail-Absender angezeigt. 
  
Zum Anzeigen dieser Bericht in der [Sicherheit &amp; Compliance Center](https://protection.office.com), wechseln Sie zu **Berichte** \> **Dashboard** \> **häufigste Absender und Empfänger**.
  
![So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur Berichte \> Dashboard \> häufigste Absender und Empfänger](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
Wenn Sie über eine Keil im Kreisdiagramm bewegen, sehen Sie die Anzahl der Nachrichten gesendet oder empfangen wurden.
  
Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).
  
Verwenden Sie die Liste **Anzeigen von Daten für** , ob Sie Daten für häufigste Absender, Empfänger, Spamempfänger und schadsoftwareempfänger anzeigen möchten. Sie können auch sehen, wer Malware erhalten, die von der erweiterte Schutz erkannt wurde. 
  
![Mithilfe der Liste Anzeigen von Daten für spezifische Informationen anzuzeigen](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
Unterhalb des Diagramms angezeigt, die die oberen e-Mail-Absender oder Empfänger wurden, zusammen mit der Anzahl der Nachrichten gesendet oder empfangen wurden, für den angegebenen Zeitraum an.
  
## <a name="spoof-mail-report"></a>Spoofing der e-Mail-Bericht

Der **Spoofing Mail** Bericht zeigt, wie viele e-Mail-Nachrichten von Spoofing erkannt wurden, wurden, welche "gut" (Spoofing Mail legitimen geschäftlichen Gründen geschehen) betrachtet und. 
  
Zum Anzeigen dieser Bericht in der [Sicherheit &amp; Compliance Center](https://protection.office.com), wechseln Sie zu **Berichte** \> **Dashboard** \> **Spoofing Mail**.
  
![So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur Berichte \> Dashboard \> Spoofing Mail](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
Wenn Sie über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Spoofing e-Mail-Nachrichten über stammt.
  
Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).
  
## <a name="spam-detections-report"></a>Bericht Spamerkennungen

Der Bericht **Spamerkennungen** zeigt alle Spam-Inhalt von Exchange Online blockiert. 
  
Zum Anzeigen dieser Bericht in der [Sicherheit &amp; Compliance Center](https://protection.office.com), wechseln Sie zu **Berichte** \> **Dashboard** \> **Spamerkennungen**.
  
![So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur Berichte \> Dashboard \> EOP Spamerkennungen](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
Wenn Sie über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Elemente dieses Tages blockiert wurden, wie diese Elemente kategorisiert werden. Beispielsweise können Sie sehen, wie viele Spamnachrichten gefiltert wurden, und wie viele Elemente eine blockierte IP (Internet Protocol) Adresse stammt.
  
Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).
  
![Der Bericht Spamerkennungen erfahren Sie, wie viele Spamnachrichten herausgefiltert oder blockiert wurden](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
Unter dem Diagramm sehen Sie eine Liste der Spam-Objekte, die erkannt wurden. Wählen Sie ein Element aus, um zusätzliche Informationen wie gibt an, ob das Element Spam eingehend oder ausgehend war, die Nachrichten-ID und der Empfänger anzuzeigen.
  
## <a name="sent-and-received-email-report"></a>Gesendete und empfangene e-Mail-Bericht

Der Bericht **gesendete und empfangene e-Mail** ist smart Bericht mit Informationen zu eingehender und ausgehender e-Mails, einschließlich spamerkennungen, Malware und e-Mails, die als "gut". 
  
Zum Anzeigen dieser Bericht in der [Sicherheit &amp; Compliance Center](https://protection.office.com), wechseln Sie zu **Berichte** \> **Dashboard** \> **gesendete und empfangene e-Mail**.
  
![So zeigen Sie in diesem Bericht in das Wertpapier an &amp; Compliance Center, navigieren Sie zur Berichte \> Dashboard \> gesendete und empfangene e-Mail](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
Wenn Sie über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Nachrichten geliefert wurde und wie diese Nachrichten kategorisiert werden. Beispielsweise können Sie sehen, wie viele Nachrichten als mit Schadsoftware erkannt wurden, und wie viele als Spam identifiziert wurden.
  
Berichts, um sie in einem neuen Browserfenster zu öffnen, in dem Sie eine ausführlichere Ansicht des Berichts erhalten können klicken (oder tippen).
  
Die Liste **nach aufgliedern** können zum Anzeigen von Informationen nach Typ oder nach Richtung (eingehend und ausgehend). 
  
![Verwenden Sie die Liste unterbrechen nach unten durch, zum Anzeigen von Informationen vom Typ oder die Richtung](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
Unter dem Diagramm sehen Sie eine Liste von e-Mail-Kategorien, wie **GoodMail**, **SpamContentFiltered**und So weiter. Wählen Sie eine Kategorie anzeigen zusätzlicher Informationen, wie beispielsweise für Schadsoftware, durchgeführten Aktionen und gibt an, ob e-Mail-wurde eingehend oder ausgehend.
  
![In diesem Bericht erfahren Sie mehr über Schadsoftware, Anti-Spam- und andere erkannte Nachricht](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report-new"></a>Benutzer gemeldete Nachrichten Bericht (neu!)

Der **Benutzer gemeldete Nachrichten** -Bericht enthält Informationen zu e-Mail-Nachrichten, die Benutzer mit dem [Bericht-add-in](enable-the-report-message-add-in.md)als Junk, Phishing-Versuche oder unbedenkliche e-Mails gemeldet haben.
  
Details sind für jede Nachricht, einschließlich der Übermittlung Grund, einen solchen Spam-Richtlinie Ausnahme oder e-Mail-Flussregel für Ihre Organisation konfiguriert. Um Details anzuzeigen, wählen Sie ein Element in der Liste Benutzer-Berichte, und klicken Sie dann zeigen Sie die Informationen auf den Registerkarten **Zusammenfassung** und **Details an** . 
  
![Bericht User-Reported Nachrichten werden Nachrichten, die Benutzer mit der Bezeichnung als Junk, keine Junk-e- oder Phishing Versuche.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
Zum Anzeigen dieser Bericht in der [Sicherheit &amp; Compliance Center](https://protection.office.com), eine der folgenden Aktionen aus:
  
- Wechseln Sie zu **Threat Management** \> **Dashboard** \> **Nachrichten Benutzer gemeldet**.
    
- Wechseln Sie zu **Threat Management** \> **Überprüfung** \> **Nachrichten Benutzer gemeldet**.
    
![In das Wertpapier &amp; Compliance Center, wählen Sie Threat Management \> Überprüfung \> Benutzer gemeldete Nachrichten](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> In Reihenfolge für den Benutzer gemeldete Nachrichten Bericht ordnungsgemäß funktioniert für Ihre Office 365-Umgebung **muss die überwachungsprotokollierung aktiviert werden** . Dies erfolgt normalerweise von einem Benutzer, der Rolle für Überwachungsprotokolle im Exchange Online zugewiesen hat. Weitere Informationen finden Sie unter [Aktivieren von Office 365 Such-Protokoll aktiviert oder deaktiviert](turn-audit-log-search-on-or-off.md). 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a>Welche Berechtigungen sind erforderlich, damit diese Berichte anzeigen?

Anzeigen und verwenden die Berichte in diesem Artikel beschriebenen **benötigen Sie eine entsprechende Rolle zugewiesen sind beide Sicherheit &amp; Compliance Center und der Exchange-Verwaltungskonsole**.

- Für die Sicherheit &amp; Compliance Center, benötigen Sie eine der folgenden Rollen zugewiesen:
    - Organisationsverwaltung
    - Sicherheitsadministrator (Dies kann in der Verwaltungskonsole von Azure Active Directory zugewiesen werden ([https://aad.portal.azure.com](https://aad.portal.azure.com))
    - Sicherheit-Reader

- Für Exchange Online müssen Sie eine der folgenden Rollen in der Exchange-Verwaltungskonsole zugewiesen haben ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) oder mit PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Organisationsverwaltung
    - Organisationsverwaltung mit Leserechten
    - Rolle „Empfänger mit Leserechten“
    - Verwaltung der Richtlinientreue

Finden Sie weitere Informationen finden Sie unter den folgenden Ressourcen:

- [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Featureberechtigungen in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a>Was passiert, wenn nicht die Berichte Daten angezeigt?

Wenn Sie Daten in den Berichten nicht angezeigt werden, überprüfen Sie, dass Ihre Richtlinien ordnungsgemäß eingerichtet wurden. Weitere Informationen finden Sie unter [Anti-Spam and Anti-Malware Protection in Office 365](anti-spam-and-anti-malware-protection.md).
  
## <a name="related-topics"></a>Verwandte Themen

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)
  
[Berichte und Einblicke in die Office 365-Sicherheit &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Erstellen Sie einen Zeitplan für einen Bericht in das Wertpapier &amp; Compliance Center](create-a-schedule-for-a-report.md)
  
[Einrichten von, und Laden Sie einen benutzerdefinierten Bericht in das Wertpapier &amp; Compliance Center](set-up-and-download-a-custom-report.md)
  

