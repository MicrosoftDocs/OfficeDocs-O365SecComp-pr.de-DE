---
title: Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/05/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MED150
- MBS150
- MET150
ms.assetid: 96deb75f-64e8-4c10-b570-84c99c674e15
description: Null-Stunden automatisch löschen (ZAP) ist eine e-Mail-Schutz-Funktion, die Nachrichten mit Spam oder Schadsoftware erkannt, die bereits an die Posteingänge der Benutzer gesendet wurden, und klicken Sie dann den schädlichem Inhalt unschädlichen rendert. Wie ZAP dies funktioniert, hängt von den Typ des schädlichem Inhalt erkannt.
ms.openlocfilehash: 1e90e69018b7640bb36011287abd5bcd77d43358
ms.sourcegitcommit: 30faa3ba91cab4c36e3d8d8ed5858d5269ea8a56
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2019
ms.locfileid: "27749319"
---
# <a name="zero-hour-auto-purge---protection-against-spam-and-malware"></a>Automatische Bereinigung zur Nullstunde – Schutz vor Spam und Schadsoftware

## <a name="overview"></a>Übersicht

Null-Stunden automatisch löschen (ZAP) ist eine e-Mail-Schutz-Funktion, die Nachrichten mit Phishing, Spam oder Schadsoftware erkannt, die bereits an die Posteingänge der Benutzer gesendet wurden, und klicken Sie dann rendert schädlichem Inhalt unschädlichen. Wie ZAP dies funktioniert, hängt von den Typ des schädlichem Inhalt erkannt. e-Mail-Nachrichten kann von e-Mail-Inhalten, URLs oder Anlagen zapped werden.
  
ZAP ist mit Exchange Online Protection, die mit einem beliebigen Office 365-Abonnement enthalten ist, die Exchange Online-Postfächer enthält standardmäßig verfügbar.

ZAP ist standardmäßig aktiviert, jedoch müssen die folgenden Bedingungen erfüllt sein:
  
- **Spam-Aktion** ist eine **Nachricht in Junk-e-Mail-Ordner verschieben**festlegen. <br/>Sie können auch eine neue Richtlinie des Spam-Filter erstellen, die nur für eine Gruppe von Benutzern angewendet wird, wenn Sie nicht möchten, dass alle Postfächer von ZAP überwachten sein.

- Benutzer haben ihre standardmäßige Junk-e-Mail-Einstellungen gespeichert und junk-e-Mail-Schutz nicht deaktiviert haben. (Informationen zu den Benutzeroptionen in Outlook finden Sie unter [Ändern der Schutz in den Junk-e-Mail-Filter](https://support.office.com/article/change-the-level-of-protection-in-the-junk-email-filter-e89c12d8-9d61-4320-8c57-d982c8d52f6b) .) 
  
## <a name="how-does-zap-work"></a>Wie funktioniert ZAP?

Office 365 aktualisiert Anti-Spam-Modul- und Malware-Signaturen in Echtzeit auf täglicher Basis. Jedoch könnte die Benutzer weiterhin bösartige Nachrichten an ihre Posteingänge für eine Vielzahl von Gründen, einschließlich, wenn Inhalte nach der Übermittlung an Benutzer weaponized ist erhalten. Entfernen Sie Adressen dies durch die Überwachung ständig mit Office 365 Spam und Malware Signaturen aktualisiert. ZAP kann suchen und Entfernen zuvor zugestellte Nachrichten, die bereits im Posteingang Benutzer sind. 

- Für e-Mail-Nachrichten, die als Spam gekennzeichnet ist, verschiebt ZAP ungelesene Nachrichten an Benutzer Junk-e-Mail-Ordner. 

- Für e-Mail-Nachrichten, die als Spam gekennzeichnet ist, verschiebt ZAP Nachrichten an Benutzer Junk-e-Mail-Ordner, unabhängig davon, ob die e-Mail-Nachricht gelesen wurde.

- Für neu erkannte Schadsoftware entfernt ZAP Anlagen in e-Mail-Nachrichten, unabhängig davon, ob die e-Mail-Nachricht gelesen wurde. 
  
Die ZAP-Aktion ist für den Postfachbenutzer nahtlos. Sie werden nicht benachrichtigt, wenn eine e-Mail-Nachricht verschoben wird.
  
Listen, [e-Mail-Flussregeln](https://go.microsoft.com/fwlink/p/?LinkId=722755)und Endbenutzer Regeln zulassen oder zusätzliche Filter haben Vorrang vor ZAP.
  
## <a name="to-review-or-set-up-a-spam-filter-policy"></a>Um zu überprüfen, oder richten Sie eine Spam-Filter-Richtlinie
  
1. Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365.

2. Wählen Sie unter **Threat Management** **Anti-Spam**aus.

3. Überprüfen Sie die Standardeinstellungen. 

4. Wenn Sie Ihre Einstellungen anpassen möchten, wählen Sie die Registerkarte **Benutzerdefiniert** aus, und aktivieren Sie **Benutzerdefinierte Einstellungen**. Bearbeiten Sie Ihre Einstellungen, und wenn Sie möchten, wählen Sie **+ Erstellen einer Richtlinie** um eine neue Richtlinie hinzuzufügen. 
    
## <a name="to-see-if-zap-moved-your-message"></a>Um festzustellen, ob ZAP Ihrer Nachricht verschoben.

Wenn um festzustellen, ob ZAP Ihre Nachricht verschoben werden soll, können Sie entweder die [Threat Protection Statusbericht](view-email-security-reports.md#threat-protection-status-report) (oder [Threat Explorer](use-explorer-in-security-and-compliance.md)).
    
## <a name="to-disable-zap"></a>So deaktivieren Sie ZAP
  
Wenn Sie deaktivieren möchten für Ihre Office 365-Mandanten entfernen, oder eine Gruppe von Benutzern, verwenden Sie den **ZapEnabled** -Parameter des [Set-HostedContentFilterPolicy](https://go.microsoft.com/fwlink/p/?LinkId=722758), ein EOP-Cmdlet.
    
Im folgenden Beispiel wird ZAP für eine inhaltsfilterrichtlinie namens "Test" deaktiviert.
    
```
  Set-HostedContentFilterPolicy -Identity Test -ZapEnabled $false
```

## <a name="faq"></a>Häufig gestellte Fragen (FAQ)

### <a name="what-happens-if-a-legitimate-message-is-moved-to-the-junk-mail-folder"></a>Was passiert, wenn eine legitime Nachricht in den Junk-e-Mailordner verschoben wird?
  
Befolgen Sie den normalen reporting-Prozess für falsch positive ein. Der einzige Grund für die Nachricht aus dem Posteingang in den Junk-e-Mailordner verschoben werden wird, da der Dienst festgestellt hat, dass die Nachricht Spam war wäre oder böswilliges.
  
### <a name="what-if-i-use-the-office-365-quarantine-instead-of-the-junk-mail-folder"></a>Was geschieht, wenn ich Office 365 Quarantäne anstelle der Junk-e-Mailordner verwenden?
  
ZAP nicht Sie Nachrichten in Quarantäne aus dem Posteingang zu diesem Zeitpunkt verschieben.
  
### <a name="what-if-i-have-a-custom-mail-flow-rule-block-allow-rule"></a>Was geschieht, wenn ich eine benutzerdefinierte e-Mail-Flussregel haben (blockieren / Regel zulassen)?
  
Regelanzahl durch Administratoren (e-Mail-Flussregeln) oder blockieren und zulassen Regeln haben Vorrang vor. Solche Nachrichten werden von der Funktion Kriterien ausgeschlossen.
  
## <a name="related-topics"></a>Verwandte Themen

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)
  
[Blockieren von E-Mail-Spam mit dem Office 365-Spamfilter zur Vermeidung von falsch negativen Einträgen](block-email-spam-to-prevent-false-negatives.md)
  

