---
title: Anzeigen von e-Mail-Sicherheits &amp; Berichten im Security Compliance Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3a137e28-1174-42d5-99af-f18868b43e86
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Sie e-Mail-Sicherheitsberichte für Ihre Organisation mit Office 365 Enterprise suchen und verwenden. E-Mail-Sicherheitsberichte sind im &amp; Security Compliance Center verfügbar.
ms.openlocfilehash: 833cb4e0b90375179a4ce2097cb986926a9856d0
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341446"
---
# <a name="view-email-security-reports-in-the-security-amp-compliance-center"></a>Anzeigen von e-Mail-Sicherheits &amp; Berichten im Security Compliance Center

Im [ &amp; Security Compliance Center](https://protection.office.com) stehen verschiedene Berichte zur Verfügung, mit denen Sie sehen können, wie e-Mail-Sicherheitsfunktionen wie Antispam-, Antischadsoftware-und Verschlüsselungsfunktionen in Office 365 Ihre Organisation schützen. Wenn Sie über die [erforderlichen Berechtigungen](#what-permissions-are-needed-to-view-these-reports)verfügen, können Sie diese Berichte &amp; im Security Compliance Center anzeigen, indem Sie zum **Dashboard**für **Berichte** \> wechseln.
  
![Dashboard, in dem Sie sehen, wie Advanced Threat Protection funktioniert](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
Zu Ihren e-Mail-Sicherheitsberichten gehört Folgendes:

- [Verschlüsselungs Bericht](#encryption-report) (Neu!)
  
- [Status Bericht zum BedrohungsSchutz](view-email-security-reports.md#tps) 
    
- [Bericht über Schadsoftware](view-email-security-reports.md#maldet)
    
- [Häufigster Schadsoftware-Bericht](#top-malware-report)
    
- [Bericht "häufigste Absender und Empfänger"](view-email-security-reports.md#topsenders)
    
- [Spoof-e-Mail-Bericht](#spoof-mail-report)
    
- [Bericht über Spam-Entdeckungen](#spam-detections-report)
    
- [Gesendete und empfangene e-Mail-Berichte](view-email-security-reports.md#sentreceivedemail)

- [Bericht über vom Benutzer gemeldete Nachrichten](view-email-security-reports.md#userreported)
    
## <a name="encryption-report"></a>Verschlüsselungs Bericht

(**Neu!**) Der **Verschlüsselungs Bericht** enthält Informationen zu e-Mail-Nachrichten, die über Richtlinien oder durch Endbenutzer Steuerelemente verschlüsselt wurden. Das Sicherheitsteam Ihrer Organisation kann anhand dieser Informationen Muster erkennen und proaktive Richtlinien für vertrauliche e-Mail-Nachrichten anwenden oder anpassen.

Um diesen Bericht anzuzeigen, wechseln Sie im Security & Compliance Center zu **Berichte** \> - **Dashboard** \> -Verschlüsselungs **Bericht**.

![Verschlüsselungs Bericht](media/encryptionreport-defaultview.png) 

Beim ersten Öffnen des Berichts werden Daten zu Verschlüsselungsmethoden für e-Mail-Nachrichten für die letzten sieben (7) Tage angezeigt. Sie können den Datumsbereich und die Details im Bericht ändern, indem Sie in der oberen rechten Ecke des Bildschirms auf Filter klicken.

![Filter für Verschlüsselungs Berichte](media/encryptionreport-filters.png)   

Sie können auch das Menü "nach unten nach" verwenden, um Daten nach Verschlüsselungs Vorlage (oder-Methode) anzuzeigen.

![Verschlüsselungsmethode oder-Vorlage](media/encryptionreport-breakdownby.png)

Sie können auch das Menü Daten anzeigen nach verwenden, um die Ansicht zu ändern, um die Anzahl der verschlüsselten Nachrichten in den fünf größten Empfängerdomänen anzuzeigen.

![Verschlüsselungs Bericht-Ansicht von Daten nach Menü](media/encryptionreport-viewdataby.png)

Mit der Flexibilität des neuen Verschlüsselungs Berichts können Sie Trends anzeigen und entsprechende Aktionen ausführen. Wenn beispielsweise eine hohe Anzahl von e-Mail-Nachrichten angezeigt wird, die von Benutzern verschlüsselt wurden, können Sie eine Verschlüsselungsrichtlinie hinzufügen, um die Verschlüsselung für bestimmte Anwendungsfälle zu automatisieren. Wenn Sie eine Reihe von Verschlüsselungs Vorlagen zur Verfügung haben, die Sie jedoch nicht verwenden, können Sie ermitteln, ob die Benutzerschulungen für diese Funktion benötigen. 

Mit diesem Bericht kann das Sicherheits-und Compliance-Team Ihrer Organisation überwachen, wie die Nachrichtenverschlüsselung verwendet wird und ob weitere Aktionen erforderlich sind.

## <a name="threat-protection-status-report"></a>Status Bericht zum BedrohungsSchutz

Der **bedrohungSschutz Status** Bericht ist ein intelligenter Bericht, der bösartige e-Mails anzeigt, die von Exchange Online Protection erkannt und blockiert wurden. Dieser Bericht enthält Informationen zu e-Mails, die als Schadsoftware oder als Phishing-Versuch identifiziert wurden. 

> [!NOTE]
> Ein Bericht über den BedrohungsSchutz steht Kunden zur Verfügung, die entweder [Office 365 ATP](office-365-atp.md) oder [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EoP) haben; die Informationen, die im Status Bericht zur Gefahrenabwehr für ATP-Kunden angezeigt werden, enthalten jedoch wahrscheinlich unterschiedliche Daten als die EOP-Kunden. EOP-Kunden können beispielsweise Informationen über in e-Mails erkannte Schadsoftware anzeigen, jedoch keine Informationen zu böswilligen Dateien, die [in SharePoint Online, OneDrive oder Microsoft Teams erkannt](atp-for-spo-odb-and-teams.md)wurden, eine ATP-spezifische Funktion. ([Erfahren Sie mehr über ATP-Berichte](view-reports-for-atp.md).)
  
Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zum Status des \> **Threat Protection**-Dashboards für **Berichte** \> **** .
  
![Status Bericht zum BedrohungsSchutz](media/0ff86e12-c2b2-4d89-92a5-cefb054dc070.png)
  
Wenn Sie den Status Bericht zum ersten Mal öffnen, zeigt der Bericht standardmäßig Daten für die letzten sieben Tage an; Sie können jedoch auf **Filter** klicken und den Datums Umfang für bis zu 90 Tage ändern. Dieser Bericht ist nützlich, um die Effektivität und die Auswirkungen der Exchange Online Protection-Features in Ihrer Organisation sowie für längerfristige Trends anzuzeigen. 
  
![Status Berichtsfilter für den BedrohungsSchutz](media/ab6b6b8d-e97a-4c3a-8fb1-c4940dcb7a07.png)
  
Sie können auch auswählen, ob Daten für als böswillig identifizierte e-Mails, als Phishing-Versuche identifizierte e-Mails oder als Schadsoftware identifizierte e-Mails angezeigt werden sollen.
  
![Status Berichts Ansichtsoptionen für den BedrohungsSchutz](media/d429ecd7-cb7a-4c99-8d27-79a2832cf467.png)
  
## <a name="malware-detections-report"></a>Bericht über Schadsoftware

Der **** Bericht über Schadsoftware zeigt, wie viele eingehende und ausgehende Nachrichten erkannt wurden, die Schadsoftware für Ihre Organisation enthalten. 
  
Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu " **Berichte** \> - **Dashboard** \> -Schadsoftware- **Entdeckungen**".
  
![Beispiel für Schadsoftware-Erkennungsberichte](media/a1ba61a3-565a-46d6-b0d5-6a6cff6b31d7.png)
  
Ähnlich wie bei anderen Berichten zeigt der Bericht standardmäßig Daten für die letzten sieben Tage an. Sie können jedoch auch **Filter** auswählen, um den Datums Umfang zu ändern. 
  
## <a name="top-malware-report"></a>Häufigster Schadsoftware-Bericht

Der **häufigste Malware** Bericht zeigt die verschiedenen Arten von Schadsoftware, die von Exchange Online erkannt wurden. 
  
Um **** \> diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu den **Top**-Schadsoftware- **Dashboards** \> .
  
![SCC-EOP – häufigste Schadsoftware](media/763330b3-f56e-4ba4-b0bb-051500ae950a.png)
  
Wenn Sie im Kreisdiagramm auf einen Keil zeigen, sehen Sie den Namen einer Art von Schadsoftware und die Anzahl der Nachrichten, die als Schadsoftware erkannt wurden.
  
Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.
  
![Dieser Bericht zeigt die häufigste Schadsoftware, die für Ihre Organisation erkannt wurde.](media/3fded224-fb31-4713-86f2-8afce5ce2991.png)
  
Unterhalb des Diagramms wird eine Liste der erkannten Schadsoftware und der Anzahl der Nachrichten angezeigt, die als Schadsoftware erkannt wurden.
  
## <a name="top-senders-and-recipients-report"></a>Bericht "häufigste Absender und Empfänger"

Der Bericht " **häufigste Absender und Empfänger** " ist ein Kreisdiagramm, in dem die wichtigsten e-Mail-Absender angezeigt werden. 
  
**** \> Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu den Top-Absendern **und Empfängern**des Dashboards. **** \>
  
![Um diesen Bericht anzuzeigen, wechseln Sie im &amp; Security Compliance Center zu den Top \> - \> Absendern und Empfängern des Berichte-Dashboards.](media/b5506b5c-2420-4a5a-9ea3-d654294ac838.png)
  
Wenn Sie den Mauszeiger über einen Keil im Kreisdiagramm bewegen, wird die Anzahl der gesendeten oder empfangenen Nachrichten angezeigt.
  
Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.
  
Verwenden Sie die Liste **Daten für anzeigen** , um auszuwählen, ob Daten für die wichtigsten Absender, Empfänger, Spamempfänger und Schadsoftware-Empfänger angezeigt werden sollen. Sie können auch sehen, wer Malware erhalten hat, die von Advanced Threat Protection erkannt wurde. 
  
![Verwenden der Liste "Daten für anzeigen" zum Anzeigen bestimmter Informationen](media/bd91449f-7d42-4749-8666-7b44044049b8.png)
  
Unter dem Diagramm sehen Sie, wer die häufigsten e-Mail-Absender oder Empfänger waren, zusammen mit der Anzahl der Nachrichten, die für den angegebenen Zeitraum gesendet oder empfangen wurden.
  
## <a name="spoof-detections-report"></a>Bericht über Spoof-Entdeckungen

Der Bericht über **Spoof** -Erkennungen zeigt, wie viele Spoof-e-Mails erkannt wurden, und von denen, die als "gut" galten (Spoof-e-Mails aus berechtigten geschäftlichen Gründen). 
  
Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu **Berichte** \> - **Dashboard** \> **-Spoof-e-Mail**.
  
![Wechseln Sie im &amp; Security Compliance Center zu Berichte \> -Dashboard \> -Spoof-e-Mail](media/0427e85c-9e40-4225-a0f0-e21a4e8b0e44.png)
  
Wenn Sie den Mauszeiger über einen Tag im Diagramm bewegen, sehen Sie, wie viele Spoof-e-Mail-Nachrichten durchlaufen haben.
  
Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.
  
## <a name="spam-detections-report"></a>Bericht über Spam-Entdeckungen

Der Bericht über **Spam Entdeckungen** enthält alle Spam-Inhalte, die von Exchange Online blockiert wurden. 
  
Um **** \> diesen Bericht anzuzeigen, gehen Sie [im &amp; Security Compliance Center](https://protection.office.com)zu **Spam Entdeckungen**im **Dashboard** \> .
  
![Um diesen Bericht anzuzeigen, wechseln Sie im &amp; Security Compliance Center zu den Berichten \> Dashboard \> EoP Spam Detections](media/028cff3c-79ce-4ec0-8f0f-ec32ac28243a.png)
  
Wenn Sie den Mauszeiger über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Elemente an diesem Tag blockiert wurden, und wie diese Elemente kategorisiert werden. Sie können beispielsweise sehen, wie viele Spamnachrichten gefiltert wurden und wie viele Elemente aus einer blockierten IP-Adresse (Internet Protocol) stammten.
  
Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.
  
![Der Bericht über Spam Entdeckungen gibt an, wie viele Spamnachrichten blockiert oder herausgefiltert wurden.](media/370ec67d-eb30-4863-bfcf-68a41be02295.png)
  
Unterhalb des Diagramms wird eine Liste der gefundenen Spam Elemente angezeigt. Wählen Sie ein Element aus, um zusätzliche Informationen anzuzeigen, beispielsweise ob es sich bei dem Spam Element um ein-oder ausgehend, um die Nachrichten-ID und den Empfänger handelt.
  
## <a name="sent-and-received-email-report"></a>Gesendete und empfangene e-Mail-Berichte

Der **gesendete und empfangene e-Mail-** Bericht ist ein intelligenter Bericht mit Informationen zu eingehenden und ausgehenden e-Mails, einschließlich Spamerkennungen, Schadsoftware und e-Mails, die als "gut" identifiziert wurden. 
  
Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zum **Berichte** \> - **Dashboard** \> **gesendet und empfangen per e-Mail**.
  
![Um diesen Bericht anzuzeigen, wechseln Sie im &amp; Security Compliance Center zum Berichte \> -Dashboard \> gesendet und empfangen per e-Mail.](media/0e710ed0-1b0e-4dac-8796-94a01a710f3a.png)
  
Wenn Sie den Mauszeiger über einen Tag im Diagramm bewegen, können Sie sehen, wie viele Nachrichten eingehen und wie diese Nachrichten kategorisiert werden. Sie können beispielsweise sehen, wie viele Nachrichten mit Schadsoftware erkannt wurden und wie viele als Spam identifiziert wurden.
  
Klicken Sie auf den Bericht (oder tippen Sie darauf), um ihn in einem neuen Browserfenster zu öffnen, in dem Sie eine detailliertere Ansicht des Berichts erhalten.
  
Mithilfe der Liste nach **unten** nach können Sie Informationen nach Typ oder nach Richtung (ein-und ausgehend) anzeigen. 
  
![Verwenden der aufSchlüsselung nach Liste zum Anzeigen von Informationen nach Typ oder Richtung](media/a5b30c94-d75f-4bfc-851a-cb155685b177.png)
  
Unterhalb des Diagramms sehen Sie eine Liste der e-Mail-Kategorien, wie **GoodMail**, **SpamContentFiltered**usw. Wählen Sie eine Kategorie aus, um zusätzliche Informationen anzuzeigen, beispielsweise Aktionen, die für Schadsoftware ergriffen wurden, und ob e-Mails ein-oder ausgehen.
  
![Dieser Bericht informiert Sie über Antischadsoftware, Antispam und andere Nachrichten Entdeckungen.](media/9ea4b606-f27a-46ee-97a7-be018e2b839c.png)
  
## <a name="user-reported-messages-report"></a>Bericht über vom Benutzer gemeldete Nachrichten

Der Bericht vom **Benutzer gemeldete Nachrichten** enthält Informationen zu e-Mail-Nachrichten, die von Benutzern als Junk-, Phishing-oder gute e-Mails mithilfe des [Add-Ins "Berichtnachricht](enable-the-report-message-add-in.md)" gemeldet wurden.
  
Für jede Nachricht stehen Details zur Verfügung, einschließlich des Liefer Grunds, einer Spam Richtlinienausnahme oder einer Nachrichtenfluss Regel, die für Ihre Organisation konfiguriert ist. Zum Anzeigen von Details wählen Sie ein Element in der Liste Benutzer Berichte aus, und zeigen Sie die Informationen auf den Registerkarten **Zusammenfassung** und **Details** an. 
  
![Der Bericht vom Benutzer gemeldete Nachrichten zeigt Benutzer, die als Junk-, nicht Junk-oder Phishing-Versuche gekennzeichnet sind.](media/ad5e9a3d-b833-419c-bcc9-3425d9604ead.png)
  
Führen Sie im [ &amp; Security Compliance Center](https://protection.office.com)einen der folgenden Schritte aus, um diesen Bericht anzuzeigen:
  
- Wechseln Sie zu vom **Benutzer gemeldeten Nachrichten**des **Threat Management** \> - **Dashboards** \> .
    
- Gehen Sie zu **Threat Management** \> **Review** \> vom **Benutzer gemeldete Nachrichten**.
    
![Wählen Sie im &amp; Security Compliance Center die Option \> Bedrohungs \> Verwaltung Überprüfung der gemeldeten Nachrichten aus.](media/e372c57c-1414-4616-957b-bc933b8c8711.png)
  
> [!IMPORTANT]
> Damit der Bericht vom Benutzer gemeldete Nachrichten ordnungsgemäß funktioniert, **muss die Überwachungsprotokollierung** für ihre Office 365-Umgebung aktiviert sein. Dies erfolgt in der Regel durch einen Benutzer, dem die Rolle "Überwachungsprotokolle" in Exchange Online zugewiesen wurde. Weitere Informationen finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md). 
  
## <a name="what-permissions-are-needed-to-view-these-reports"></a>Welche Berechtigungen sind erforderlich, um diese Berichte anzuzeigen?

Um die in diesem Artikel beschriebenen Berichte anzuzeigen und zu verwenden, **müssen Sie eine entsprechende Rolle sowohl für das Security &amp; Compliance Center als auch für das Exchange Admin Center zugewiesen haben**.

- Für das Security &amp; Compliance Center muss eine der folgenden Rollen zugewiesen sein:
    - Organisationsverwaltung
    - Sicherheits Administrator (Dies kann im Azure Active Directory Admin Center zugewiesen werden ([https://aad.portal.azure.com](https://aad.portal.azure.com))
    - Sicherheits Leser

- Für Exchange Online müssen Sie über eine der folgenden Rollen verfügen, die entweder in der Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() oder mit PowerShell-Cmdlets zugewiesen sind (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):
    - Organisationsverwaltung
    - Organisationsverwaltung mit Leserechten
    - Rolle „Empfänger mit Leserechten“
    - Verwaltung der Richtlinientreue

Weitere Informationen finden Sie in den folgenden Ressourcen:

- [Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)

- [Featureberechtigungen in Exchange Online](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
   
## <a name="what-if-the-reports-arent-showing-data"></a>Was geschieht, wenn die Berichte keine Daten anzeigen?

Wenn in ihren Berichten keine Daten angezeigt werden, überprüfen Sie, ob Ihre Richtlinien ordnungsgemäß eingerichtet sind. Weitere Informationen finden Sie unter [Antispam-und Antischadsoftware-Schutz in Office 365](anti-spam-and-anti-malware-protection.md).
  
## <a name="related-topics"></a>Verwandte Themen

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)
  
[Berichte und Einblicke im Office 365 &amp; Security Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Erstellen eines Zeitplans für einen Bericht im &amp; Security Compliance Center](create-a-schedule-for-a-report.md)
  
[Einrichten und Herunterladen eines benutzerdefinierten Berichts im Security &amp; Compliance Center](set-up-and-download-a-custom-report.md)
  

