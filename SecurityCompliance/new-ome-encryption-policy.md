---
title: Neue Office 365 Message Encryption Richtlinie für vertrauliche Informationen
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 12/13/2018
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Neue Office 365 Message Encryption Richtlinie für vertrauliche Informationen.'
ms.openlocfilehash: 180050d1bf9303f6d29bc126e66ac53211c2fb34
ms.sourcegitcommit: 3aae959ea1ac5ef61a9942c681d334831e6b6038
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/14/2018
ms.locfileid: "27271091"
---
# <a name="new-office-365-message-encryption-policy-for-sensitive-information"></a>Neue Office 365 Message Encryption Richtlinie für vertrauliche Informationen

Es wird eine neue Richtlinie für die automatische in Office 365-Mandanten erstellen, die gelten Office 365 Message Encryption auf alle e-Mails, die vertraulichen Informationen enthalten und, sind außerhalb Ihrer Organisation gesendet werden. Dieser neuen Exchange Mail Flow Regel wird automatisch in Ihrem Office 365-Mandanten erstellt werden, damit Ihre Organisation standardmäßig geschützt werden.

## <a name="how-will-this-work"></a>Wie diese Arbeit wird?

Ihre Organisation erhalten eine Benachrichtigung in Office 365 Message Center aufgefordert werden, das Datum, an dem diese Richtlinie automatische in Ihrem Mandanten erstellt wird. Erhalten Sie mindestens eine 30-Tage-Benachrichtigung, und Sie müssen auch die Option zum Abmelden. Ein Szenario, in dem Sie potenziell kündigen möchten, ist bei einer 3rd Party Data Loss Prevention-Lösung, die bereits für vertrauliche Typen überprüft.

## <a name="new-policy-details"></a>Details zur neuen Richtlinie

In Ihrer Organisation, die sich außerhalb Ihrer Organisation mit unterschiedlich sein und sollte-e-Mails automatisch verschlüsselt wird eine neue e-Mail-Flussregel Exchange erstellt werden die *Reinen verschlüsseln* Richtlinie, wenn sie die folgenden Arten von vertraulichen Informationen enthalten:

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

Sie haben keine vorhandenen Office 365-Konfigurationseinstellungen vor dieser neuen Änderung zu aktualisieren. Sie möchten jedoch alle anwendbaren Endbenutzerdokumentation und Schulungsunterlagen zum Vorbereiten von Personen in Ihrer Organisation, damit diese Änderung zu aktualisieren.

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a>Wie wird diese Änderung im Überwachungsprotokoll werden dargestellt?

Diese Aktivität wird überwacht und ist für Kunden verfügbar.  Der Vorgang ist 'New-TransportRule', und einem Codeausschnitt ein Überwachungseintrag Beispiel aus der Audit Log-Suche in Sicherheit und Compliance Center unter wird:

|     |
| --- |
| *{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 1, "ResultStatus": "True", "UserKey": "Microsoft Operator"," UserType": 3,"Version": 1,"Arbeitslast":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":""," UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX () 15.20.1382.008)","Parameters": {"Name":"Organisation","Value":" 123456 221 d - 12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Verschlüsseln"}, {"Name":"Name","Value":"Verschlüsseln ausgehende e-Mails (im Feld Regel)"}, {"Name":" MessageContainsDataClassifications"usw..*
 |

## <a name="how-do-i-opt-out"></a>Wie sich ich melden Sie?

Wenn Sie diese Änderung zielorientierten möchten, gehen Sie folgendermaßen vor:

1. Verbinden Sie mit [Exchange Online PowerShell](https://aka.ms/exopowershell) als Benutzer mit der globalen Administratorrolle sein.
2.  Führen Sie den folgenden Code nach der Authentifizierung:

    ```
    Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
    ```

## <a name="how-do-i-disable-the-automatic-policy"></a>Wie deaktiviere ich die automatische Richtlinie?

Wenn Sie nicht melden Sie sich von dieser Änderung und die Exchange-Mail-Regel bereits erstellt wurde, können Sie [die Regel deaktiviert werden](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) durch das Aufrufen der **E-Mail-Fluss** > **Regeln** in der Exchange Admin center (EAC) und deaktivieren Sie die Regel "*verschlüsseln ausgehende vertrauliche-e-Mails (im Feld Regel)*".