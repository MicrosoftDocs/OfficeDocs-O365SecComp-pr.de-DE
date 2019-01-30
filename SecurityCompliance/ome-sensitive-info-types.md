---
title: Neue Office 365 Message Encryption Richtlinie für vertrauliche Informationen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/16/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Automatisch angewendet, Richtlinie für Typen vertraulicher Informationen für alle Mandanten Einführung Office 365 Message Encryption.'
ms.openlocfilehash: f83bf0fe572586b3becf2dd53395e611bdaaea24
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614379"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a>Office 365 Message Encryption Richtlinie für vertrauliche Informationen

Für eine ausgewählte Gruppe von Mandanten, basierend auf ihrer Organisation Größe und Komplexität der e-Mail-Fluss sind eine langsame Einführung einer neuen automatische Richtlinie in Office 365-Mandanten wir, für die Office 365 Message Encryption-e-Mails gilt, die bestimmte Arten von Sensitive enthalten Informationen. Wir sind dies mit eine kleine Gruppe von Mandanten testen. Diese Richtlinie wird nicht werden eingeführt für alle Organisationen und Aspekte wie die Größe der Organisation und Komplexität der e-Mail-Fluss wird verwendet, um die Berechtigung für diese Einführung zu bestimmen. Wenn Ihre Organisation für diese Einführung ausgewählt ist, erhalten Sie eine Benachrichtigung in Office 365 Message Center aufgefordert werden, das Datum, auf dem diese Richtlinie automatisch erstellt werden, und erhalten Sie mindestens eine 30-Tage-Benachrichtigung und die Option zum Abmelden. Wenn Sie nicht warten für Microsoft diese Richtlinie erstellen möchten und dazu selbst können Sie diese mithilfe von Regeln Exchange Mail Flow automatische Richtlinie erstellen.

## <a name="when-to-expect-the-update-for-your-tenant"></a>Das Update für Ihre Mandanten voraussichtliche Verfügbarkeit

Ihre Organisation erhalten eine Benachrichtigung in Office 365 Message Center aufgefordert werden, das Datum, an dem diese Richtlinie automatische in Ihrem Mandanten erstellt wird. Erhalten Sie mindestens eine 30-Tage-Benachrichtigung, und Sie müssen auch die Option zum Abmelden. Ein Szenario, in dem Sie potenziell kündigen möchten, ist bei einer 3rd Party Data Loss Prevention-Lösung, die bereits für vertrauliche Typen überprüft. Weitere Informationen zur Teilnahme stehen weiter unten in diesem Artikel.

## <a name="sensitive-information-type-policy-details"></a>Details zum Richtlinie vertrauliche Informationen

Eine Exchange Mail Flow Regel erstellt werden in Ihrer Organisation, die sich außerhalb Ihrer Organisation mit unterschiedlich sein und sollte-e-Mails automatisch verschlüsselt wird die *Verschlüsseln nur* Richtlinie, wenn die e-Mails oder die Anlagen, die folgenden Arten von vertraulichen Informationen enthalten:

- ABA routing Anzahl
- Kreditkartennummer
- Anzahl von Drug Erzwingung Agency (DEA)
- US / Großbritannien Reisepassnummer
- US-Bankkontonummer
- US-Steueridentifikationsnummer (ITIN)
- US-Sozialversicherungsnummer

> [!Note]
> Die genauen vertraulichen Typen abweichen von Ihrer Organisation Gebietsschema und werden in der Benachrichtigung Nachrichtencenter kommuniziert werden.

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a>Was muss ich tun, um diese Änderung bei der Vorbereitung?

Sie haben keine vorhandenen Office 365-Konfigurationseinstellungen vor dieser neuen Änderung zu aktualisieren. Sie möchten jedoch alle anwendbaren Endbenutzerdokumentation und Schulungsunterlagen zum Vorbereiten von Personen in Ihrer Organisation, damit diese Änderung zu aktualisieren. Freigeben von diese Office 365 Message Encryption-Ressourcen für Ihre Benutzer nach Bedarf:

- [Senden Sie, zeigen Sie an und beantworten Sie verschlüsselter Nachrichten in Outlook für PC](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [Office 365 Essentials Video: Office-Nachrichtenverschlüsselung](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a>Wie wird diese Änderung im Überwachungsprotokoll werden dargestellt?

Diese Aktivität wird überwacht und ist für Kunden verfügbar.  Der Vorgang ist 'New-TransportRule', und einem Codeausschnitt ein Überwachungseintrag Beispiel aus der Audit Log-Suche in Security & Compliance Center unter wird:

|     |
| --- |
| *{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 1, "ResultStatus": "True", "UserKey": "Microsoft Operator"," UserType": 3,"Version": 1,"Arbeitslast":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":""," UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX () 15.20.1382.008)","Parameters": {"Name":"Organisation","Value":" 123456 221 d - 12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Verschlüsseln"}, {"Name":"Name","Value":"Verschlüsseln ausgehende e-Mails (im Feld Regel)"}, {"Name":" MessageContainsDataClassifications"usw..*
 |

## <a name="how-do-i-opt-out"></a>Wie sich ich melden Sie?

Wenn Sie diese Änderung zielorientierten möchten, gehen Sie folgendermaßen vor:

1. Verwenden ein Arbeit oder Schule Konto, die in Office 365-Organisation über globaler Administrator-Berechtigungen verfügt, eine Windows PowerShell-Sitzung zu starten und eine Verbindung mit Exchange Online. Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).
2. Führen Sie das Cmdlet Set-IRMConfiguration wie folgt aus:

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-or-customize-the-automatic-policy"></a>Wie ich deaktivieren oder Anpassen die automatische Richtlinie?

Wenn Sie nicht melden Sie sich von dieser Änderung und die Exchange Mail Flow Regel bereits erstellt wurde, können Sie [deaktivieren, oder bearbeiten Sie die Regel](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) auf **E-Mail-Fluss** > **Regeln** in der Exchange Admin center (EAC) und deaktivieren Sie die Regel "*Verschlüsseln Ausgehende e-Mails (im Feld Regel)*".
