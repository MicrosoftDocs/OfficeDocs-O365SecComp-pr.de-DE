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
# <a name="create-a-sensitive-information-type-policy-for-your-organization-using-office-365-message-encryption"></a><span data-ttu-id="6c54e-103">Erstellen von Richtlinien für sensible Datentypen für Ihr Unternehmen mithilfe von Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6c54e-103">Create a sensitive information type policy for your organization using Office 365 Message Encryption</span></span>

<span data-ttu-id="6c54e-104">Sie können entweder Exchange-Nachrichtenfluss Regeln oder Office 365 Data Loss Prevention (DLP) verwenden, um eine Richtlinie für vertrauliche Informationen mit der Office 365-Nachrichtenverschlüsselung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6c54e-104">You can use either Exchange mail flow rules or Office 365 Data Loss Prevention (DLP) to create a sensitive information type policy with Office 365 Message Encryption.</span></span> <span data-ttu-id="6c54e-105">Zum Erstellen einer Exchange-Nachrichtenfluss Regel können Sie entweder die Exchange-Verwaltungskonsole (EAC) oder PowerShell verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c54e-105">To create an Exchange mail flow rule, you can use either the Exchange admin center (EAC) or PowerShell.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a><span data-ttu-id="6c54e-106">So erstellen Sie die Richtlinie mithilfe von Nachrichtenfluss Regeln in der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="6c54e-106">To create the policy by using mail flow rules in the EAC</span></span>

<span data-ttu-id="6c54e-107">Melden Sie sich beim Exchange Admin Center (EAC) an, und wechseln Sie zu **Nachrichtenfluss** > **Regeln**.</span><span class="sxs-lookup"><span data-stu-id="6c54e-107">Sign in to the Exchange admin center (EAC) and go to **Mail flow** > **Rules**.</span></span> <span data-ttu-id="6c54e-108">Erstellen Sie auf der Seite Regeln eine Regel, die die Office 365-Nachrichtenverschlüsselung anwendet.</span><span class="sxs-lookup"><span data-stu-id="6c54e-108">On the Rules page, create a rule that applies Office 365 Message Encryption.</span></span> <span data-ttu-id="6c54e-109">Sie können eine Regel erstellen, die auf Bedingungen wie dem vorhanden sein bestimmter Schlüsselwörter oder vertraulicher Informationstypen in der Nachricht oder Anlage basiert.</span><span class="sxs-lookup"><span data-stu-id="6c54e-109">You can create a rule based on conditions such as the presence of certain keywords or sensitive information types in the message or attachment.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a><span data-ttu-id="6c54e-110">So erstellen Sie die Richtlinie mithilfe von Nachrichtenfluss Regeln in PowerShell</span><span class="sxs-lookup"><span data-stu-id="6c54e-110">To create the policy by using mail flow rules in PowerShell</span></span>

<span data-ttu-id="6c54e-111">Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her.</span><span class="sxs-lookup"><span data-stu-id="6c54e-111">Use a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="6c54e-112">Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="6c54e-112">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span> <span data-ttu-id="6c54e-113">Verwenden Sie die Cmdlets Set-IRMConfiguration und New-TransportRule, um die Richtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6c54e-113">Use the Set-IRMConfiguration and New-TransportRule cmdlets to create the policy.</span></span>

### <a name="example-mail-flow-rule-created-with-powershell"></a><span data-ttu-id="6c54e-114">Mit PowerShell erstellte Beispiel-e-Mail-Fluss Regel</span><span class="sxs-lookup"><span data-stu-id="6c54e-114">Example mail flow rule created with PowerShell</span></span>

<span data-ttu-id="6c54e-115">Führen Sie die folgenden Befehle in PowerShell aus, um eine Exchange-Nachrichtenfluss Regel zu erstellen, mit der e-Mails, die \*\* außerhalb Ihrer Organisation gesendet werden, automatisch mit der Verschlüsselungsrichtlinie verschlüsselt werden, wenn die e-Mails oder Ihre Anlagen die folgenden vertraulichen Informationen enthalten. Typen</span><span class="sxs-lookup"><span data-stu-id="6c54e-115">Run the following commands in PowerShell to create an Exchange mail flow rule that automatically encrypts emails sent outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="6c54e-116">ABA-Routingnummer</span><span class="sxs-lookup"><span data-stu-id="6c54e-116">ABA routing number</span></span>
- <span data-ttu-id="6c54e-117">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="6c54e-117">Credit card Number</span></span>
- <span data-ttu-id="6c54e-118">DEA-Nummer (Drug Enforcement Agency)</span><span class="sxs-lookup"><span data-stu-id="6c54e-118">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="6c54e-119">USA/U.K.</span><span class="sxs-lookup"><span data-stu-id="6c54e-119">U.S. / U.K.</span></span> <span data-ttu-id="6c54e-120">passport number</span><span class="sxs-lookup"><span data-stu-id="6c54e-120">passport number</span></span>
- <span data-ttu-id="6c54e-121">US-Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="6c54e-121">U.S. bank account number</span></span>
- <span data-ttu-id="6c54e-122">US-Steueridentifikationsnummer (ITIN)</span><span class="sxs-lookup"><span data-stu-id="6c54e-122">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="6c54e-123">US-Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="6c54e-123">U.S. Social Security Number (SSN)</span></span>

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a><span data-ttu-id="6c54e-124">Wie Empfänger auf Anlagen zugreifen</span><span class="sxs-lookup"><span data-stu-id="6c54e-124">How recipients access attachments</span></span>

<span data-ttu-id="6c54e-125">Nachdem Office 365 eine Nachricht verschlüsselt hat, haben Empfänger uneingeschränkten Zugriff auf Anlagen, wenn Sie auf Ihre verschlüsselte e-Mail zugreifen und diese öffnen.</span><span class="sxs-lookup"><span data-stu-id="6c54e-125">After Office 365 encrypts a message, recipients have unrestricted access to attachments when they access and open their encrypted email.</span></span>

## <a name="to-prepare-for-this-change"></a><span data-ttu-id="6c54e-126">So bereiten Sie diese Änderung vor</span><span class="sxs-lookup"><span data-stu-id="6c54e-126">To prepare for this change</span></span>

<span data-ttu-id="6c54e-127">Möglicherweise möchten Sie die entsprechenden Endbenutzer Dokumentationen und Schulungsmaterialien aktualisieren, um Personen in Ihrer Organisation auf diese Änderung vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="6c54e-127">You may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change.</span></span> <span data-ttu-id="6c54e-128">Teilen Sie diese Office 365-Nachrichten Verschlüsselungs Ressourcen bei Bedarf Ihren Benutzern mit:</span><span class="sxs-lookup"><span data-stu-id="6c54e-128">Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="6c54e-129">Senden, anzeigen und beantworten von verschlüsselten Nachrichten in Outlook für PC</span><span class="sxs-lookup"><span data-stu-id="6c54e-129">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="6c54e-130">Office 365 Essentials Video: Office-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6c54e-130">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a><span data-ttu-id="6c54e-131">Diese Änderungen im Überwachungsprotokoll anzeigen</span><span class="sxs-lookup"><span data-stu-id="6c54e-131">View these changes in the Audit log</span></span>

<span data-ttu-id="6c54e-132">Office 365 überwacht diese Aktivität und stellt Sie Office 365-Administratoren zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="6c54e-132">Office 365 audits this activity and makes it available to Office 365 administrators.</span></span> <span data-ttu-id="6c54e-133">Der Vorgang ist "New-TransportRule" und ein Auszug aus einem Beispiel Überwachungseintrag aus der Überwachungsprotokoll Suche im Security & Compliance Center befindet sich unten:</span><span class="sxs-lookup"><span data-stu-id="6c54e-133">The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

```text
*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*
```

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a><span data-ttu-id="6c54e-134">So deaktivieren oder ändern Sie die Richtlinie für vertrauliche Informationstypen</span><span class="sxs-lookup"><span data-stu-id="6c54e-134">To disable or customize the sensitive information types policy</span></span>

<span data-ttu-id="6c54e-135">Nachdem Sie die Exchange-Nachrichtenfluss Regel erstellt haben, können Sie [die Regel deaktivieren oder bearbeiten](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) , indem Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** > **Regeln** wechseln und die Regel "*vertrauliche e-Mails verschlüsseln (außerhalb der Box-Regel)* " deaktivieren. ".</span><span class="sxs-lookup"><span data-stu-id="6c54e-135">Once you've created the Exchange mail flow rule, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
