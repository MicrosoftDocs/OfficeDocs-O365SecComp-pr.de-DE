---
title: Neue Office 365 Message Encryption Richtlinie für vertrauliche Informationen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/9/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Automatisch angewendet, Richtlinie für Typen vertraulicher Informationen für alle Mandanten Einführung Office 365 Message Encryption.'
ms.openlocfilehash: a8cd132af2b1429698ea92779a3c54559e2b13e2
ms.sourcegitcommit: b936a2fd4b7f7a7099b96cc29580ed55bdb8bf2b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/10/2019
ms.locfileid: "27789453"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="c0de9-103">Office 365 Message Encryption Richtlinie für vertrauliche Informationen</span><span class="sxs-lookup"><span data-stu-id="c0de9-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="c0de9-p101">Es wird eine neue Richtlinie für die automatische in Office 365-Mandanten erstellen, die gelten Office 365 Message Encryption auf alle e-Mails, die vertraulichen Informationen enthalten und, sind außerhalb Ihrer Organisation gesendet werden. Dieser neuen Exchange Mail Flow Regel wird automatisch in Ihrem Office 365-Mandanten erstellt werden, damit Ihre Organisation standardmäßig geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="c0de9-p101">We will be creating a new automatic policy in Office 365 tenants that will apply Office 365 Message Encryption to all emails that contain sensitive information and that are being sent outside your organization. This new Exchange mail flow rule will be automatically created in your Office 365 tenant so that your organization will be protected by default.</span></span>

## <a name="when-to-expect-the-update-for-your-tenant"></a><span data-ttu-id="c0de9-106">Das Update für Ihre Mandanten voraussichtliche Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="c0de9-106">When to expect the update for your tenant</span></span>

<span data-ttu-id="c0de9-p102">Ihre Organisation erhalten eine Benachrichtigung in Office 365 Message Center aufgefordert werden, das Datum, an dem diese Richtlinie automatische in Ihrem Mandanten erstellt wird. Erhalten Sie mindestens eine 30-Tage-Benachrichtigung, und Sie müssen auch die Option zum Abmelden. Ein Szenario, in dem Sie potenziell kündigen möchten, ist bei einer 3rd Party Data Loss Prevention-Lösung, die bereits für vertrauliche Typen überprüft. Weitere Informationen zur Teilnahme stehen weiter unten in diesem Artikel.</span><span class="sxs-lookup"><span data-stu-id="c0de9-p102">Your organization will receive a notification in the Office 365 Message Center notifying you the date on which this automatic policy will be created in your tenant. You will be given at least a 30-day notice and you will also have the option to opt-out. A scenario in which you may want to potentially opt out is if you have a 3rd-party Data Loss Prevention solution that already scans for sensitive types. More details on how to opt-out are available later in this article.</span></span>

## <a name="sensitive-information-type-policy-details"></a><span data-ttu-id="c0de9-110">Details zum Richtlinie vertrauliche Informationen</span><span class="sxs-lookup"><span data-stu-id="c0de9-110">Sensitive information type policy details</span></span>

<span data-ttu-id="c0de9-111">Eine Exchange Mail Flow Regel erstellt werden in Ihrer Organisation, die sich außerhalb Ihrer Organisation mit unterschiedlich sein und sollte-e-Mails automatisch verschlüsselt wird die *Verschlüsseln nur* Richtlinie, wenn die e-Mails oder die Anlagen, die folgenden Arten von vertraulichen Informationen enthalten:</span><span class="sxs-lookup"><span data-stu-id="c0de9-111">An Exchange mail flow rule will be created in your organization that will automatically encrypt emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="c0de9-112">ABA routing Anzahl</span><span class="sxs-lookup"><span data-stu-id="c0de9-112">ABA routing number</span></span>
- <span data-ttu-id="c0de9-113">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="c0de9-113">Credit card Number</span></span>
- <span data-ttu-id="c0de9-114">Anzahl von Drug Erzwingung Agency (DEA)</span><span class="sxs-lookup"><span data-stu-id="c0de9-114">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="c0de9-p103">US / Großbritannien Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="c0de9-p103">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="c0de9-117">US-Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="c0de9-117">U.S. bank account number</span></span>
- <span data-ttu-id="c0de9-118">US-Steueridentifikationsnummer (ITIN)</span><span class="sxs-lookup"><span data-stu-id="c0de9-118">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="c0de9-119">US-Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="c0de9-119">U.S. Social Security Number (SSN)</span></span>

> [!Note]
> <span data-ttu-id="c0de9-120">Die genauen vertraulichen Typen abweichen von Ihrer Organisation Gebietsschema und werden in der Benachrichtigung Nachrichtencenter kommuniziert werden.</span><span class="sxs-lookup"><span data-stu-id="c0de9-120">The exact sensitive types may differ by your organization’s locale and will be communicated in the Message Center notification.</span></span>

## <a name="what-do-i-need-to-do-to-prepare-for-this-change"></a><span data-ttu-id="c0de9-121">Was muss ich tun, um diese Änderung bei der Vorbereitung?</span><span class="sxs-lookup"><span data-stu-id="c0de9-121">What do I need to do to prepare for this change?</span></span>

<span data-ttu-id="c0de9-p104">Sie haben keine vorhandenen Office 365-Konfigurationseinstellungen vor dieser neuen Änderung zu aktualisieren. Sie möchten jedoch alle anwendbaren Endbenutzerdokumentation und Schulungsunterlagen zum Vorbereiten von Personen in Ihrer Organisation, damit diese Änderung zu aktualisieren. Freigeben von diese Office 365 Message Encryption-Ressourcen für Ihre Benutzer nach Bedarf:</span><span class="sxs-lookup"><span data-stu-id="c0de9-p104">You do not have to update or modify any existing Office 365 configuration settings prior to this new change. However, you may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change. Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="c0de9-125">Senden Sie, zeigen Sie an und beantworten Sie verschlüsselter Nachrichten in Outlook für PC</span><span class="sxs-lookup"><span data-stu-id="c0de9-125">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="c0de9-126">Office 365 Essentials Video: Office-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="c0de9-126">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="how-will-this-change-be-represented-in-the-audit-log"></a><span data-ttu-id="c0de9-127">Wie wird diese Änderung im Überwachungsprotokoll werden dargestellt?</span><span class="sxs-lookup"><span data-stu-id="c0de9-127">How will this change be represented in the Audit log?</span></span>

<span data-ttu-id="c0de9-p105">Diese Aktivität wird überwacht und ist für Kunden verfügbar.  Der Vorgang ist 'New-TransportRule', und einem Codeausschnitt ein Überwachungseintrag Beispiel aus der Audit Log-Suche in Sicherheit und Compliance Center unter wird:</span><span class="sxs-lookup"><span data-stu-id="c0de9-p105">This activity is audited and is available to customers.  The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="c0de9-130">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345", "RecordType": 1, "ResultStatus": "True", "UserKey": "Microsoft Operator"," UserType": 3,"Version": 1,"Arbeitslast":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":""," UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX () 15.20.1382.008)","Parameters": {"Name":"Organisation","Value":" 123456 221 d - 12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Verschlüsseln"}, {"Name":"Name","Value":"Verschlüsseln ausgehende e-Mails (im Feld Regel)"}, {"Name":" MessageContainsDataClassifications"usw..*</span><span class="sxs-lookup"><span data-stu-id="c0de9-130">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span>
 |

## <a name="how-do-i-opt-out"></a><span data-ttu-id="c0de9-131">Wie sich ich melden Sie?</span><span class="sxs-lookup"><span data-stu-id="c0de9-131">How do I opt-out?</span></span>

<span data-ttu-id="c0de9-132">Wenn Sie diese Änderung zielorientierten möchten, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="c0de9-132">If you would like to opt-out of this change, please follow these steps:</span></span>

1. <span data-ttu-id="c0de9-p106">Verwenden ein Arbeit oder Schule Konto, die in Office 365-Organisation über globaler Administrator-Berechtigungen verfügt, eine Windows PowerShell-Sitzung zu starten und eine Verbindung mit Exchange Online. Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="c0de9-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>
2. <span data-ttu-id="c0de9-135">Führen Sie das Cmdlet Set-IRMConfiguration wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="c0de9-135">Run the Set-IRMConfiguration cmdlet as follows:</span></span>

   ```
   Set-IRMConfiguration -AutomaticServiceUpdateEnabled $false
   ```

## <a name="how-do-i-disable-or-customize-the-automatic-policy"></a><span data-ttu-id="c0de9-136">Wie ich deaktivieren oder Anpassen die automatische Richtlinie?</span><span class="sxs-lookup"><span data-stu-id="c0de9-136">How do I disable or customize the automatic policy?</span></span>

<span data-ttu-id="c0de9-137">Wenn Sie nicht melden Sie sich von dieser Änderung und die Exchange Mail Flow Regel bereits erstellt wurde, können Sie [deaktivieren, oder bearbeiten Sie die Regel](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) auf **E-Mail-Fluss** > **Regeln** in der Exchange Admin center (EAC) und deaktivieren Sie die Regel "*Verschlüsseln Ausgehende e-Mails (im Feld Regel)*".</span><span class="sxs-lookup"><span data-stu-id="c0de9-137">If you didn’t opt-out of this change and the Exchange mail flow rule has already been created, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
