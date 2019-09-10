---
title: Konfigurieren von Benachrichtigungen über ausgehende Spam Richtlinien in Office 365
ms.author: tracyp
author: MSFTTracyP
manager: dansimp
ms.date: 11/10/2016
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: a44764e9-a5d2-4c67-8888-e7fb871c17c7
ms.collection:
- M365-security-compliance
description: Administratoren können erfahren, wie Sie die Benachrichtigungseinstellungen für ausgehende Spamerkennungen in Office 365 ändern.
ms.openlocfilehash: c48b6cd634417a00040fb5479313782b44f6aa8d
ms.sourcegitcommit: 81b3bff27bc60235a38004c5b0297ac454331b25
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2019
ms.locfileid: "36822515"
---
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a>Konfigurieren von Benachrichtigungen über ausgehende Spam Richtlinien in Office 365

Die Filterung ausgehender Spamnachrichten ist immer aktiviert, wenn Sie den Dienst für das Senden ausgehender E-Mails verwenden und dadurch Organisationen, die den Dienst nutzen, und ihre jeweiligen Empfänger schützen. Ebenso wie die Filterung eingehender Nachrichten besteht die Filterung ausgehender Nachrichten aus einer Verbindungsfilterung und einer Inhaltsfilterung, wobei die Einstellungen für den ausgehenden Filter nicht konfiguriert werden können. Wenn eine ausgehende Nachricht als Spam identifiziert wird, wird sie durch den Pool für besonders riskante Zustellungen geleitet, der die Wahrscheinlichkeit reduziert, dass der normale Pool für ausgehende IP-Adressen einer Sperrliste hinzugefügt wird. Falls ein Kunde auch weiterhin ausgehende Spamnachrichten über den Dienst sendet, wird er für das Senden von Nachrichten gesperrt.

Sie können zwar keine ausgehende Spamfilterung deaktivieren oder ändern, aber Sie können die folgenden Einstellungen für ausgehende Spambenachrichtigungen konfigurieren:

- **Kopien von verdächtigen Nachrichten senden**: diese Nachrichten werden als Spam gekennzeichnet (unabhängig von der SCL-Bewertung) und werden nicht vom Filter zurückgewiesen, sondern durch den höheren Risiko Zustellungs Pool weitergeleitet. Sie können die Exchange-Verwaltungskonsole (EAC) oder die ** \*-HostedOutboundSpamFilterPolicy-** Cmdlets in Exchange Online PowerShell oder Exchange Online Protection PowerShell verwenden, um zusätzliche Empfänger für diese erkannten Nachrichten anzugeben. Beachten Sie, dass die Empfänger als **Bcc** -Empfänger hinzugefügt werden (die Felder **from** und **to** sind der ursprüngliche Absender und Empfänger).

- **Senden von Benachrichtigungen, wenn ein Absender blockiert wird**: Wenn ein bestimmter Benutzer eine erhebliche Menge an Spam eingeht, ist der Benutzer für das Senden von e-Mail-Nachrichten deaktiviert. Administratoren werden standardmäßig benachrichtigt, aber Sie können den **Benutzer vom Senden von e-Mail-** [Warnungsrichtlinien](alert-policies.md) im Office 365 Security #a0 Compliance Center beschränken, um zusätzliche Benachrichtigungsempfänger zu konfigurieren.

  Ein Beispiel für diese Benachrichtigung finden Sie unter [Beispielbenachrichtigung, wenn ein Absender aufgrund des Versendens von ausgehendem Spam blockiert wird](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md). Informationen zur erneuten Aktivierung finden Sie unter [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).

## <a name="what-do-you-need-to-know-before-you-begin"></a>Was sollten Sie wissen, bevor Sie beginnen?

- Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten

- Informationen zum Öffnen des Security & Compliance Center finden Sie unter [Wechseln zum Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).

- Informationen zum Öffnen des EAC finden Sie unter [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) oder [Exchange Admin Center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).

- Informationen zum Öffnen Exchange Online PowerShell finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell). Informationen zum Öffnen von Exchange Online Protection PowerShell finden Sie unter [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).

- Ihrem Konto müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren ausführen können. Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Manage Alerts" Role entry in [Permissions in the Office 365 Security #a0 Compliance Center](permissions-in-the-security-and-compliance-center.md).

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a>Konfigurieren zusätzlicher Empfänger für ausgehende Spamnachrichten mithilfe der Exchange-Verwaltungskonsole

1. Wechseln Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **ausgehenden Spam**.

2. Wählen Sie die Richtlinie **default**aus, und klicken Sie dann](media/ITPro-EAC-EditIcon.png)auf Bearbeitungssymbol **Bearbeiten** ![.

3. Überprüfen Sie auf der Seite Eigenschaften, die geöffnet wird, ob die Registerkarte **ausgehende Spameinstellungen** ausgewählt ist, und konfigurieren Sie dann die folgende Einstellung:

   **Senden Sie eine Kopie aller Verdächtigen ausgehenden e-Mail-Nachrichten an die folgende e-Mail-Adresse oder**Adresse: Aktivieren Sie das Kontrollkästchen, und geben Sie die e-Mail-Adressen von einem oder mehreren Administratoren ein, die dem Feld **Bcc** für erkannte Nachrichten hinzugefügt werden sollen Trennen Sie mehrere e-Mail-Adressen durch ein Semikolon (;).

   Klicken Sie nach Abschluss des Vorgangs auf **Speichern**.

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a>Verwenden Sie Exchange Online PowerShell oder Exchange Online Protection PowerShell, um zusätzliche Empfänger für ausgehende Spamnachrichten zu konfigurieren.

Verwenden Sie die folgende Syntax, um zusätzliche Empfänger für ausgehende Spamnachrichten zu aktivieren und zu konfigurieren:

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- Verwenden Sie die Syntax `emailaddress1,emailaddress2,...emailaddressN`, um Empfänger anzugeben, die alle vorhandenen Werte überschreiben.

- Verwenden Sie die Syntax `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`, um Empfänger selektiv hinzuzufügen oder zu entfernen, ohne die anderen Einträge zu beeinträchtigen.

In diesem Beispiel werden Chris@contoso.com, Laura@contoso.com und Julia@contoso.com als Bcc-Empfänger für ausgehende Spamnachrichten aktiviert und konfiguriert.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

In diesem Beispiel wird Michelle@contoso.com als zusätzlicher Bcc-Empfänger hinzugefügt.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

In diesem Beispiel werden Chris@contoso.com und Julia@contoso.com aus der Liste der Bcc-Empfänger entfernt.

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Sets-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).

**Hinweis**: führen Sie den `Get-HostedOutboundSpamFilterPolicy | Format-List` Befehl aus, um die aktuellen Werte der Eigenschaften *BccSuspiciousOutboundMail* und *BccSuspiciousOutboundAdditionalRecipients* anzuzeigen.

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a>Verwenden des Security #a0 Compliance Center zum Konfigurieren von Benachrichtigungen, wenn ein Absender blockiert wird

1. Wechseln Sie im Security #a0 Compliance Center **zu** \> Alerts **Alerts-Richtlinien**.

2. Suchen und wählen Sie die Richtlinie mit dem Namen " **Benutzer eingeschränkt vom Senden von e-Mails" aus**.

3. Klicken Sie im Dialogfeld ausfliegen, das geöffnet wird, auf **Richtlinie bearbeiten**.

4. Konfigurieren Sie auf der angezeigten Seite **Empfänger bearbeiten** die folgenden Einstellungen:

   - **Senden von e-Mail-Benachrichtigungen**: Vergewissern Sie sich, dass **on** ausgewählt ist.

   - **E-Mail-Empfänger**: Standardmäßig ist **TenantAdmins** der einzige Wert hier. Wenn Sie weitere Empfänger hinzufügen möchten, klicken Sie in diesem Feld auf eine leere Stelle, beginnen Sie mit der Eingabe des Empfängers, und wählen Sie den Empfänger aus, wenn der Name aufgelöst wird. Klicken Sie zum Entfernen von Empfängern auf das **X** neben dem Namen.

   - **Grenzwert für tägliche Benachrichtigungen**: der Standardwert ist **No Limit**, aber Sie können verschiedene Grenzwerte von 1 bis 200 konfigurieren.

   Klicken Sie nach Abschluss des Vorgangs auf **Speichern**.

## <a name="for-more-information"></a>Weitere Informationen

[Pool für besonders riskante Zustellungen für ausgehende Nachrichten](high-risk-delivery-pool-for-outbound-messages.md)

[Häufig gestellte Fragen zum Anti-Spam-Schutz](anti-spam-protection-faq.md)
