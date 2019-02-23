---
title: Office 365-Nachrichten Verschlüsselungsrichtlinie für vertrauliche Informationen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Office 365-Nachrichten Verschlüsselungsrichtlinie für vertrauliche Informationstypen, die jetzt verfügbar sind.'
ms.openlocfilehash: 99cb7a9f94c9cf4036c11b74a5208ddf0e819ceb
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213979"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a>Office 365-Nachrichten Verschlüsselungsrichtlinie für vertrauliche Informationen

Update (1/30/19): im Oktober 2018 haben wir mit einer kleinen Auswahl an Kunden zusammengearbeitet, um zu verstehen, ob wir den Schutz vereinfachen können, indem Sie vertrauliche e-Mails auf der Grundlage bestimmter vertraulicher Informationstypen automatisch verschlüsseln. Basierend auf positiven Feedback aus diesem Beispiel haben wir uns entschieden, im Dezember 2018 zu einem vielfältigeren Profil von Mandanten zu expandieren. Nachdem wir die nächste Einführung zur Auswahl von Mandanten kommuniziert haben, haben wir uns Ihr Feedback angehört und festgestellt, dass Kunden mit komplexeren Umgebungen die Regeln vorsichtiger implementieren wollten, und wir passen unsere Pläne daher an.

Wenn Ihre Organisation für die Einführung ab dem 15. Januar 2019 ausgewählt wurde, wird die automatische Richtlinie nicht eingeführt. Stattdessen geben wir in diesem Artikel Anweisungen dazu, wie Sie die Einführung selbst abschließen können. Lesen Sie weiter, um herauszufinden, wie.

||
|:-----|
|Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a>Erstellen der Richtlinie für vertrauliche Informationstypen für Ihren Mandanten

Sie können entweder Exchange-Nachrichtenfluss Regeln oder Office 365 Data Loss Prevention (DLP) verwenden, um die Richtlinie für vertrauliche Informationstypen zu erstellen. Zum Erstellen einer Exchange-Nachrichtenfluss Regel können Sie entweder die Exchange-Verwaltungskonsole (EAC) oder PowerShell verwenden.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a>So erstellen Sie die Richtlinie mithilfe von Nachrichtenfluss Regeln in der Exchange-verwaltungsKONSOLE

Melden Sie sich bei der Exchange-Verwaltungskonsole an, und wechseln Sie zu **Nachrichtenfluss** > **Regeln**. Erstellen Sie dort eine Regel, die die Office 365-Nachrichtenverschlüsselung auf Grundlage von Bedingungen wie dem vorhanden sein bestimmter Schlüsselwörter oder vertraulicher Informationstypen in der Nachricht oder Anlage anwendet.

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a>So erstellen Sie die Richtlinie mithilfe von Nachrichtenfluss Regeln in PowerShell

Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell). Verwenden Sie die Cmdlets Set-IRMConfiguration und New-TransporRule, um die Richtlinie zu erstellen.

### <a name="example-mail-flow-rule-created-with-powershell"></a>Mit PowerShell erstellte Beispiel-e-Mail-Fluss Regel

Durch Ausführen der folgenden Befehle in PowerShell wird eine Exchange-Nachrichtenfluss Regel erstellt, mit der e-Mails, die sich außerhalb ** Ihrer Organisation befinden, automatisch mit der Verschlüsselungsrichtlinie verschlüsselt werden, wenn die e-Mails oder Ihre Anlagen die folgenden vertraulichen Informationstypen:

- ABA-Routingnummer
- Kreditkartennummer
- DEA-Nummer (Drug Enforcement Agency)
- U.S./UK-Passport-Nummer
- US-Bankkontonummer
- US-Steueridentifikationsnummer (ITIN)
- US-Sozialversicherungsnummer

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a>Wie Empfänger auf Anlagen zugreifen

Nachdem eine Nachricht verschlüsselt wurde, haben die Empfänger uneingeschränkten Zugriff auf Anlagen, nachdem Sie auf Ihre verschlüsselte e-Mail zugegriffen haben.

## <a name="to-prepare-for-this-change"></a>So bereiten Sie diese Änderung vor

Möglicherweise möchten Sie die entsprechenden Endbenutzer Dokumentationen und Schulungsmaterialien aktualisieren, um Personen in Ihrer Organisation auf diese Änderung vorzubereiten. Teilen Sie diese Office 365-Nachrichten Verschlüsselungs Ressourcen bei Bedarf Ihren Benutzern mit:

- [Senden, anzeigen und beantworten von verschlüsselten Nachrichten in Outlook für PC](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Office 365 Essentials Video: Office-Nachrichtenverschlüsselung](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a>Diese Änderungen im Überwachungsprotokoll anzeigen

Diese Aktivität wird überwacht und steht Office 365-Administratoren zur Verfügung. Der Vorgang ist "New-transportRule" und ein Auszug aus einem Beispiel Überwachungseintrag aus der Überwachungsprotokoll Suche im Security & Compliance Center befindet sich unten:

|     |
| --- |
| *{"Creation-Zeit": "2018-11-28T23:35:01", "ID": "A1b2C3d4-daa0-4c4f-A019-03a1234a1b0c", "Operation": "New-transportRule", "Organizational-ID": "123456-221d-12345", "RecordType": 1, "ResultStatus": "true", "UserKey": "Microsoft-Operator", " Usertype ": 3," Version ": 1," Workload ":" Exchange "," ClientIP ":" 123.456.147.68:17584 "," ObjectId ":" "," UserId ":" Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso. onmicrosoft. com "," OriginatingServer ":" CY4PR13MBXXXX ( 15.20.1382.008) "," Parameters ": {" Name ":" Organization "," Value ":" 123456-221d-12346 "{" Name ":" ApplyRightsProtectionTemplate "," Value ":" Encrypt "}, {" Name ":" Name "," Value ":" verSchlüsseln von ausgehenden vertraulichen e-Mails (Out of Box Rule) "}, {" Name " MessageContainsDataClassifications "... usw.* |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a>So deaktivieren oder ändern Sie die Richtlinie für vertrauliche Informationstypen

Nachdem Sie die Exchange-Nachrichtenfluss Regel erstellt haben, können Sie [die Regel deaktivieren oder bearbeiten](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) , indem Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** > **Regeln** wechseln und die Regel "*vertrauliche e-Mails verschlüsseln (außerhalb der Box-Regel)* " deaktivieren. ".
