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
# <a name="new-office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="4c073-103">Neue Office 365 Message Encryption Richtlinie für vertrauliche Informationen</span><span class="sxs-lookup"><span data-stu-id="4c073-103">New Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="4c073-p101">Es wird eine neue Richtlinie für die automatische in Office 365-Mandanten erstellen, die gelten Office 365 Message Encryption auf alle e-Mails, die vertraulichen Informationen enthalten und, sind außerhalb Ihrer Organisation gesendet werden. Dieser neuen Exchange Mail Flow Regel wird automatisch in Ihrem Office 365-Mandanten erstellt werden, damit Ihre Organisation standardmäßig geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="4c073-p101">We will be creating a new automatic policy in Office 365 tenants that will apply Office 365 Message Encryption to all emails that contain sensitive information and that are being sent outside your organization. This new Exchange mail flow rule will be automatically created in your Office 365 tenant so that your organization will be protected by default.</span></span>

## <a name="how-will-this-work"></a><span data-ttu-id="4c073-106">Wie diese Arbeit wird?</span><span class="sxs-lookup"><span data-stu-id="4c073-106">How will this work?</span></span>

<span data-ttu-id="4c073-p102">Ihre Organisation erhalten eine Benachrichtigung in Office 365 Message Center aufgefordert werden, das Datum, an dem diese Richtlinie automatische in Ihrem Mandanten erstellt wird. Erhalten Sie mindestens eine 30-Tage-Benachrichtigung, und Sie müssen auch die Option zum Abmelden. Ein Szenario, in dem Sie potenziell kündigen möchten, ist bei einer 3rd Party Data Loss Prevention-Lösung, die bereits für vertrauliche Typen überprüft.</span><span class="sxs-lookup"><span data-stu-id="4c073-p102">Your organization will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created in your tenant. You will be given at least a 30-day notice and you will also have the option to opt-out. A scenario in which you may want to potentially opt out is if you have a 3rd-party Data Loss Prevention solution that already scans for sensitive types.</span></span>

## <a name="new-policy-details"></a><span data-ttu-id="4c073-109">Details zur neuen Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4c073-109">New policy details</span></span>

<span data-ttu-id="4c073-110">In Ihrer Organisation, die sich außerhalb Ihrer Organisation mit unterschiedlich sein und sollte-e-Mails automatisch verschlüsselt wird eine neue e-Mail-Flussregel Exchange erstellt werden die *Reinen verschlüsseln* Richtlinie, wenn sie die folgenden Arten von vertraulichen Informationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="4c073-110">A new Exchange mail flow rule will be created in your organization that will automatically encrypt emails going outside your organization with the *Encrypt-Only* policy if they contain the following sensitive information types:</span></span>

- <span data-ttu-id="4c073-111">ABA routing Anzahl</span><span class="sxs-lookup"><span data-stu-id="4c073-111">ABA routing number</span></span>
- <span data-ttu-id="4c073-112">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="4c073-112">Credit card Number</span></span>
- <span data-ttu-id="4c073-113">Anzahl von Drug Erzwingung Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="4c073-113">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="4c073-p103">US / Großbritannien Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="4c073-p103">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="4c073-116">US-Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="4c073-116">U.S. bank account number</span></span>
- <span data-ttu-id="4c073-117">US-Steueridentifikationsnummer (ITIN)</span><span class="sxs-lookup"><span data-stu-id="4c073-117">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="4c073-118">US-Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="4c073-118">U.S. Social Security Number (SSN)</span></span>

> [!Note]
> <span data-ttu-id="4c073-119">Die genauen vertraulichen Typen abweichen von Ihrer Organisation Gebietsschema und werden in der Benachrichtigung Nachrichtencenter kommuniziert werden.</span><span class="sxs-lookup"><span data-stu-id="4c073-119">The exact sensitive types may differ by your organization’s locale and will be communicated in the Message Center notification.</span></span>

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="4c073-120">Was muss ich tun, um diese Änderung bei der Vorbereitung?</span><span class="sxs-lookup"><span data-stu-id="4c073-120">What do I need to do to prepare for this change?</span></span>

<span data-ttu-id="4c073-p104">Sie haben keine vorhandenen Office 365-Konfigurationseinstellungen vor dieser neuen Änderung zu aktualisieren. Sie möchten jedoch alle anwendbaren Endbenutzerdokumentation und Schulungsunterlagen zum Vorbereiten von Personen in Ihrer Organisation, damit diese Änderung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="4c073-p104">You do not have to update or modify any existing Office 365 configuration settings prior to this new change. However, you may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change.</span></span>

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a><span data-ttu-id="4c073-123">Wie wird diese Änderung im Überwachungsprotokoll werden dargestellt?</span><span class="sxs-lookup"><span data-stu-id="4c073-123">How will this change be represented in the Audit log?</span></span>

<span data-ttu-id="4c073-p105">Diese Aktivität wird überwacht und ist für Kunden verfügbar.  Der Vorgang ist 'New-TransportRule', und einem Codeausschnitt ein Überwachungseintrag Beispiel aus der Audit Log-Suche in Sicherheit und Compliance Center unter wird:</span><span class="sxs-lookup"><span data-stu-id="4c073-p105">This activity is audited and is available to customers.  The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="4c073-126">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 1, "ResultStatus": "True", "UserKey": "Microsoft Operator"," UserType": 3,"Version": 1,"Arbeitslast":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":""," UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX () 15.20.1382.008)","Parameters": {"Name":"Organisation","Value":" 123456 221 d - 12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Verschlüsseln"}, {"Name":"Name","Value":"Verschlüsseln ausgehende e-Mails (im Feld Regel)"}, {"Name":" MessageContainsDataClassifications"usw..*</span><span class="sxs-lookup"><span data-stu-id="4c073-126">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span>
 |

## <a name="how-do-i-opt-out"></a><span data-ttu-id="4c073-127">Wie sich ich melden Sie?</span><span class="sxs-lookup"><span data-stu-id="4c073-127">How do I opt-out?</span></span>

<span data-ttu-id="4c073-128">Wenn Sie diese Änderung zielorientierten möchten, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="4c073-128">If you would like to opt-out of this change, please follow these steps:</span></span>

1. <span data-ttu-id="4c073-129">Verbinden Sie mit [Exchange Online PowerShell](https://aka.ms/exopowershell) als Benutzer mit der globalen Administratorrolle sein.</span><span class="sxs-lookup"><span data-stu-id="4c073-129">Connect to [Exchange Online PowerShell](https://aka.ms/exopowershell) as a user with the global administrator role.</span></span>
2.  <span data-ttu-id="4c073-130">Führen Sie den folgenden Code nach der Authentifizierung:</span><span class="sxs-lookup"><span data-stu-id="4c073-130">Run the following code after authenticating:</span></span>

    ```
    Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
    ```

## <a name="how-do-i-disable-the-automatic-policy"></a><span data-ttu-id="4c073-131">Wie deaktiviere ich die automatische Richtlinie?</span><span class="sxs-lookup"><span data-stu-id="4c073-131">How do I disable the automatic policy?</span></span>

<span data-ttu-id="4c073-132">Wenn Sie nicht melden Sie sich von dieser Änderung und die Exchange-Mail-Regel bereits erstellt wurde, können Sie [die Regel deaktiviert werden](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) durch das Aufrufen der **E-Mail-Fluss** > **Regeln** in der Exchange Admin center (EAC) und deaktivieren Sie die Regel "*verschlüsseln ausgehende vertrauliche-e-Mails (im Feld Regel)*".</span><span class="sxs-lookup"><span data-stu-id="4c073-132">If you didn’t opt-out of this change and the Exchange mail rule has already been created, you can [disable the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
