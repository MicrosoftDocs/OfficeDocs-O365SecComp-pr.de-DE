---
title: Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/11/2019
audience: Admin
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
description: Zero-Hour Auto Purge (zap) ist eine e-Mail-Schutzfunktion, die Nachrichten mit Spam oder Schadsoftware erkennt, die bereits an die Posteingänge Ihrer Benutzer übermittelt wurden, und dann den schädlichen Inhalt harmlos macht. Wie zap Dies bewirkt, hängt vom Typ der erkannten schädlichen Inhalte ab.
ms.openlocfilehash: e6faef4c123ea2db38a27b49ff0ee49b237ec75c
ms.sourcegitcommit: 2b46fba650df8d252b1dd2b3c3f080a383183a06
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/23/2019
ms.locfileid: "34408350"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware

## <a name="overview"></a>Übersicht

Zero-Hour Auto Purge (zap) ist eine e-Mail-Schutzfunktion, die Nachrichten mit Phishing, Spam oder Schadsoftware erkennt, die bereits an die Posteingänge Ihrer Benutzer übermittelt wurden, und dann den schädlichen Inhalt harmlos macht. Wie zap Dies bewirkt, hängt vom Typ des erkannten schädlichen Inhalts ab. e-Mails können aufgrund von e-Mail-Inhalten, URLs oder Anlagen gezappt werden.
  
ZAP ist mit dem Standard Exchange Online Schutz verfügbar, der in jedem Office 365-Abonnement enthalten ist, das Exchange Online Postfächer enthält.

ZAP ist standardmäßig aktiviert, aber die folgenden Bedingungen müssen erfüllt sein:
  
- **Spam-Aktion** ist so eingestellt, dass die **Nachricht in den Junk-e-Mail-Ordner wechselt**. Sie können auch eine neue Spamfilter Richtlinie erstellen, die nur für eine Gruppe von Benutzern gilt, wenn Sie nicht möchten, dass alle Postfächer von zap abgeschirmt werden.

- Benutzer haben ihre Standardeinstellungen für Junk-e-Mail beibehalten und den Junk-e-Mail-Schutz nicht deaktiviert. (Weitere Informationen zu Benutzeroptionen in Outlook finden Sie unter [Ändern der Schutzebene im Junk-e-Mail-Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) .) 
  
## <a name="how-zap-works"></a>Funktionsweise von zap

Office 365 aktualisiert das Anti-Spam-Modul und die Malware Signaturen in Echtzeit auf täglicher Basis. Allerdings erhalten Ihre Benutzer möglicherweise weiterhin Schadsoftware-Nachrichten, die aus einer Vielzahl von Gründen an ihre Posteingänge gesendet werden, einschließlich, wenn der Inhalt nach der Zustellung an die Benutzer Waffen basiert. Zap behebt dies, indem Updates für die Office 365 Spam-und Malware Signaturen kontinuierlich überwacht werden. Zap kann zuvor zugestellte Nachrichten, die sich bereits in den Posteingängen von Benutzern befinden, suchen und entfernen.

- Bei e-Mails, die als Spam identifiziert werden, verschiebt zap ungelesene Nachrichten in den Junk-e-Mail-Ordner der Benutzer.

- Bei e-Mails, die als Phishing identifiziert werden, verschiebt zap Nachrichten in den Junk-e-Mail-Ordner der Benutzer, unabhängig davon, ob die e-Mail gelesen wurde.

- Für neu erkannte Schadsoftware entfernt zap Anlagen aus e-Mail-Nachrichten, unabhängig davon, ob die e-Mail gelesen wurde.
  
Die ZAP-Aktion ist nahtlos für den Postfachbenutzer; Sie werden nicht benachrichtigt, wenn eine e-Mail-Nachricht verschoben wird. Die Nachricht darf nicht älter als 2 Tage sein.
  
Zulassungslisten, [Nachrichtenfluss Regeln](https://go.microsoft.com/fwlink/p/?LinkId=722755)und Endbenutzer Regeln oder zusätzliche Filter haben Vorrang vor zap.
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a>So überprüfen oder konfigurieren Sie eine Spamfilter Richtlinie
  
1. Wechseln Sie [https://protection.office.com](https://protection.office.com) zu, und melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an.

2. Wählen Sie unter **Threat Management**die Option **Anti-Spam**aus.

3. Überprüfen Sie die Standardeinstellungen.

4. Wenn Sie Ihre Einstellungen anpassen möchten, wählen Sie die Registerkarte **Benutzerdefiniert** aus, und aktivieren Sie **benutzerdefinierte Einstellungen**. Bearbeiten Sie Ihre Einstellungen, und wählen Sie bei Bedarf die Option **+ Richtlinie erstellen** aus, um eine neue Richtlinie hinzuzufügen.

## <a name="to-see-if-zap-moved-your-message"></a>So prüfen Sie, ob zap Ihre Nachricht verschoben hat

Wenn Sie sehen möchten, ob zap Ihre Nachricht verschoben hat, können Sie entweder den [Threat Protection-Status Bericht](view-email-security-reports.md#threat-protection-status-report) oder den [Threat-Explorer (und Echt Zeit Erkennungen)](threat-explorer.md)verwenden.

## <a name="to-disable-zap"></a>So deaktivieren Sie zap
  
Wenn Sie ZAP für Ihren Office 365 Mandanten oder eine Gruppe von Benutzern deaktivieren möchten, verwenden Sie den **ZapEnabled** -Parameter von sethostedcontentfilterpolicy dient zum, ein EoP [-](https://go.microsoft.com/fwlink/p/?LinkId=722758)Cmdlet.

Im folgenden Beispiel ist zap für eine Inhaltsfilter Richtlinie mit dem Namen "Test" deaktiviert.

```Powershell
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a>Häufig gestellte Fragen

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a>Was passiert, wenn eine legitime Nachricht in den Junk-e-Mail-Ordner verschoben wird?
  
Sie sollten den normalen Berichtsprozess für [falsch positive](prevent-email-from-being-marked-as-spam.md)Vorgänge ausführen. Der einzige Grund, warum die Nachricht aus dem Posteingang in den Junk-e-Mail-Ordner verschoben würde, liegt daran, dass der Dienst festgestellt hat, dass die Nachricht als Spam oder böswillig eingestuft wurde.
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a>Was kann ich tun, wenn ich die Office 365 Quarantäne anstelle des Junk-e-Mail-Ordners verwende?
  
Zap verschiebt Nachrichten zu diesem Zeitpunkt nicht aus dem Posteingang in die Quarantäne.
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a>Was geschieht, wenn ich über eine benutzerdefinierte Nachrichtenfluss Regel (Block/Zulassungsregel) verfüge?
  
Von Administratoren erstellte Regeln (Nachrichtenfluss Regeln) oder Block-und Zulassungsregeln haben Vorrang. Solche Nachrichten werden von den Funktionskriterien ausgeschlossen, sodass die Nachrichtenübermittlung der Regelaktion (Block/Zulassungsregel) folgt.

### <a name="what-if-a-message-is-moved-to-another-folder-eg-inbox-rule"></a>Was passiert, wenn eine Nachricht in einen anderen Ordner verschoben wird (z.b. Posteingangsregel)?
Zap funktioniert in diesem Fall weiterhin, es sei denn, die Nachricht wurde gelöscht oder ist in Junk.

## <a name="related-topics"></a>Verwandte Themen

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](reduce-spam-email.md)
