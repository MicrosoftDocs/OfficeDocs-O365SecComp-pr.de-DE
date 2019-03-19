---
title: Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
ms.collection:
- M365-security-compliance
description: Zero-Hour Auto Purge (ZAP) ist eine e-Mail-Schutzfunktion, die Nachrichten mit Spam oder Schadsoftware erkennt, die bereits an die Posteingänge Ihrer Benutzer übermittelt wurden, und dann den schädlichen Inhalt harmlos macht. Wie ZAP Dies bewirkt, hängt vom Typ der erkannten bösartigen Inhalte ab.
ms.openlocfilehash: b49f7e3b5effec7b67daf6ab8acbf049705a4841
ms.sourcegitcommit: b688d67935edb036658bb5aa1671328498d5ddd3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/19/2019
ms.locfileid: "30670580"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware

## <a name="overview"></a>Übersicht

Zero-Hour Auto Purge (ZAP) ist eine e-Mail-Schutzfunktion, die Nachrichten mit Phishing, Spam oder Schadsoftware erkennt, die bereits an die Posteingänge Ihrer Benutzer übermittelt wurden, und dann den schädlichen Inhalt harmlos macht. Wie ZAP Dies bewirkt, hängt vom Typ der erkannten bösartigen Inhalte ab. e-Mails können aufgrund von e-Mail-Inhalten, URLs oder Anlagen gezappt werden.
  
ZAP ist mit dem Exchange Online Protection-Standard verfügbar, der in jedem Office 365-Abonnement enthalten ist, das Exchange Online-Postfächer enthält.

ZAP ist standardmäßig aktiviert, aber die folgenden Bedingungen müssen erfüllt sein:
  
- **Spam Aktion** ist so eingestellt, dass die **Nachricht in den Junk-e-Mail-Ordner verschoben**wird. <br/>Sie können auch eine neue Spamfilter Richtlinie erstellen, die nur für eine Gruppe von Benutzern gilt, wenn Sie nicht möchten, dass alle Postfächer durch ZAP angezeigt werden.

- Benutzer haben Ihre standardmäßigen Junk-e-Mail-Einstellungen beibehalten und den Junk-e-Mail-Schutz nicht deaktiviert. (Weitere Informationen zu Benutzeroptionen in Outlook finden Sie unter [Ändern des schutzgrads im Junk-e-Mail-Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) .) 
  
## <a name="how-does-zap-work"></a>Wie funktioniert ZAP?

Office 365 aktualisiert Anti-Spam-Modul und Schadsoftware-Signaturen in Echtzeit täglich. Ihre Benutzer erhalten jedoch möglicherweise weiterhin bösartige Nachrichten an ihre Posteingänge aus einer Vielzahl von Gründen, einschließlich, wenn der Inhalt nach der Zustellung an Benutzer Waffen bereitgestellt wird. ZAP behebt dies, indem Aktualisierungen der Office 365-Spam-und Schadsoftware-Signaturen ständig überwacht werden. ZAP kann zuvor übermittelte Nachrichten finden und entfernen, die sich bereits in den Posteingängen der Benutzer befinden. 

- Bei e-Mails, die als Spam identifiziert werden, verschiebt ZAP ungelesene Nachrichten in den Junk-e-Mail-Ordner der Benutzer. 

- Bei e-Mails, die als Phishing identifiziert werden, verschiebt ZAP Nachrichten in den Junk-e-Mail-Ordner der Benutzer, unabhängig davon, ob die e-Mail gelesen wurde.

- Bei neu erkannter Schadsoftware entfernt ZAP Anhänge von e-Mail-Nachrichten, unabhängig davon, ob die e-Mail gelesen wurde. 
  
Die ZAP-Aktion ist für den Postfachbenutzer nahtlos. Sie werden nicht benachrichtigt, wenn eine e-Mail-Nachricht verschoben wird.
  
Zulassungslisten, [Nachrichtenfluss Regeln](https://go.microsoft.com/fwlink/p/?LinkId=722755)und Endbenutzer Regeln oder zusätzliche Filter haben Vorrang vor zap.
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a>So überarbeiten Sie eine Spamfilter Richtlinie
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu und melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an.

2. Wählen Sie unter **Bedrohungs Verwaltung**die Option **Antispam**aus.

3. Überarbeiten Sie die Standardeinstellungen. 

4. Wenn Sie Ihre Einstellungen anpassen möchten, wählen Sie die Registerkarte **Benutzerdefiniert** aus, und aktivieren Sie **benutzerdefinierte Einstellungen**. Bearbeiten Sie Ihre Einstellungen, und wählen Sie dann **eine Richtlinie erstellen** , um eine neue Richtlinie hinzuzufügen. 
    
## <a name="to-see-if-zap-moved-your-message"></a>So überprüfen Sie, ob ZAP Ihre Nachricht verschoben hat

Wenn Sie sehen möchten, ob ZAP Ihre Nachricht verschoben hat, können Sie entweder den [Status Bericht](view-email-security-reports.md#threat-protection-status-report) für den Bedrohungsschutz (oder den Bedrohungs- [Explorer](use-explorer-in-security-and-compliance.md)) verwenden.
    
## <a name="to-disable-zap"></a>So deaktivieren Sie ZAP
  
Wenn Sie ZAP für Ihren Office 365-Mandanten oder eine Gruppe von Benutzern deaktivieren möchten, verwenden Sie den **ZapEnabled** -Parameter von [Set-HOSTEDCONTENTFILTERPOLICY dient zum](https://go.microsoft.com/fwlink/p/?LinkId=722758), einem EoP-Cmdlet.
    
Im folgenden Beispiel ist ZAP für eine Inhaltsfilter Richtlinie mit dem Namen "Test" deaktiviert.
    
```Powershell
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a>Häufig gestellte Fragen

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a>Was geschieht, wenn eine legitime Nachricht in den Junk-e-Mail-Ordner verschoben wird?
  
Sie sollten den normalen Berichtsprozess für [falsch positive Ergebnisse](prevent-email-from-being-marked-as-spam.md)befolgen. Der einzige Grund, warum die Nachricht aus dem Posteingang in den Junk-e-Mail-Ordner verschoben würde, liegt darin, dass der Dienst festgestellt hat, dass es sich um Spam oder bösartige Nachricht handelt.
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a>Was geschieht, wenn ich die Office 365-Quarantäne anstelle des Junk-e-Mail-Ordners verwende?
  
ZAP verschiebt Nachrichten zu diesem Zeitpunkt nicht aus dem Posteingang in die Quarantäne.
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a>Was geschieht, wenn ich über eine benutzerdefinierte e-Mail-Fluss Regel (Block/Allow Rule) verfüge?
  
Von Administratoren erstellte Regeln (Nachrichtenfluss Regeln) oder Sperr-und Zulassungsregeln haben Vorrang. Solche Nachrichten werden von den Feature-Kriterien ausgeschlossen, sodass der Nachrichtenfluss der Regelaktion (Block/Allow Rule) folgt.
  
## <a name="related-topics"></a>Verwandte Themen

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](reduce-spam-email.md)
  

