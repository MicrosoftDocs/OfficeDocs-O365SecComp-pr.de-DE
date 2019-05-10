---
title: Erstellen von Richtlinien für sensible Datentypen für Ihr Unternehmen mithilfe von Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 4/30/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
- Strat_O365_Enterprise
description: 'Zusammenfassung: Office 365-Nachrichten Verschlüsselungsrichtlinie für vertrauliche Informationstypen.'
ms.openlocfilehash: 44966303ec7c58fdd82f733e1922073de848cf73
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834834"
---
# <a name="create-a-sensitive-information-type-policy-for-your-organization-using-office-365-message-encryption"></a>Erstellen von Richtlinien für sensible Datentypen für Ihr Unternehmen mithilfe von Office 365-Nachrichtenverschlüsselung

Sie können entweder Exchange-Nachrichtenfluss Regeln oder Office 365 Data Loss Prevention (DLP) verwenden, um eine Richtlinie für vertrauliche Informationen mit der Office 365-Nachrichtenverschlüsselung zu erstellen. Zum Erstellen einer Exchange-Nachrichtenfluss Regel können Sie entweder die Exchange-Verwaltungskonsole (EAC) oder PowerShell verwenden.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a>So erstellen Sie die Richtlinie mithilfe von Nachrichtenfluss Regeln in der Exchange-Verwaltungskonsole

Melden Sie sich beim Exchange Admin Center (EAC) an, und wechseln Sie zu **Nachrichtenfluss** > **Regeln**. Erstellen Sie auf der Seite Regeln eine Regel, die die Office 365-Nachrichtenverschlüsselung anwendet. Sie können eine Regel erstellen, die auf Bedingungen wie dem vorhanden sein bestimmter Schlüsselwörter oder vertraulicher Informationstypen in der Nachricht oder Anlage basiert.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a>So erstellen Sie die Richtlinie mithilfe von Nachrichtenfluss Regeln in PowerShell

Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell). Verwenden Sie die Cmdlets Set-IRMConfiguration und New-TransportRule, um die Richtlinie zu erstellen.

### <a name="example-mail-flow-rule-created-with-powershell"></a>Mit PowerShell erstellte Beispiel-e-Mail-Fluss Regel

Führen Sie die folgenden Befehle in PowerShell aus, um eine Exchange-Nachrichtenfluss Regel zu erstellen, mit der e-Mails, die ** außerhalb Ihrer Organisation gesendet werden, automatisch mit der Verschlüsselungsrichtlinie verschlüsselt werden, wenn die e-Mails oder Ihre Anlagen die folgenden vertraulichen Informationen enthalten. Typen

- ABA-Routingnummer
- Kreditkartennummer
- DEA-Nummer (Drug Enforcement Agency)
- USA/U.K. passport number
- US-Bankkontonummer
- US-Steueridentifikationsnummer (ITIN)
- US-Sozialversicherungsnummer

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a>Wie Empfänger auf Anlagen zugreifen

Nachdem Office 365 eine Nachricht verschlüsselt hat, haben Empfänger uneingeschränkten Zugriff auf Anlagen, wenn Sie auf Ihre verschlüsselte e-Mail zugreifen und diese öffnen.

## <a name="to-prepare-for-this-change"></a>So bereiten Sie diese Änderung vor

Möglicherweise möchten Sie die entsprechenden Endbenutzer Dokumentationen und Schulungsmaterialien aktualisieren, um Personen in Ihrer Organisation auf diese Änderung vorzubereiten. Teilen Sie diese Office 365-Nachrichten Verschlüsselungs Ressourcen bei Bedarf Ihren Benutzern mit:

- [Senden, anzeigen und beantworten von verschlüsselten Nachrichten in Outlook für PC](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Office 365 Essentials Video: Office-Nachrichtenverschlüsselung](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a>Diese Änderungen im Überwachungsprotokoll anzeigen

Office 365 überwacht diese Aktivität und stellt Sie Office 365-Administratoren zur Verfügung. Der Vorgang ist "New-TransportRule" und ein Auszug aus einem Beispiel Überwachungseintrag aus der Überwachungsprotokoll Suche im Security & Compliance Center befindet sich unten:

```text
*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*
```

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a>So deaktivieren oder ändern Sie die Richtlinie für vertrauliche Informationstypen

Nachdem Sie die Exchange-Nachrichtenfluss Regel erstellt haben, können Sie [die Regel deaktivieren oder bearbeiten](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) , indem Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** > **Regeln** wechseln und die Regel "*vertrauliche e-Mails verschlüsseln (außerhalb der Box-Regel)* " deaktivieren. ".
