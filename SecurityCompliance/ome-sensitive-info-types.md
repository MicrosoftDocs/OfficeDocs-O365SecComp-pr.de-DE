---
title: Office 365-Nachrichten Verschlüsselungsrichtlinie für vertrauliche Informationen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/31/2019
ROBOTS: NOINDEX, NOFOLLOW
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Office 365-Nachrichten Verschlüsselungsrichtlinie für vertrauliche Informationstypen, die jetzt verfügbar sind.'
ms.openlocfilehash: e2a72ee85ca65a2fe8ae1543979b51915ff0a88f
ms.sourcegitcommit: 24659bdb09f49d0ffed180a4b80bbb7c45c2d301
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2019
ms.locfileid: "29696199"
---
# <a name="office-365-message-encryption-policy-for-sensitive-information"></a><span data-ttu-id="1a950-103">Office 365-Nachrichten Verschlüsselungsrichtlinie für vertrauliche Informationen</span><span class="sxs-lookup"><span data-stu-id="1a950-103">Office 365 Message Encryption policy for sensitive information</span></span>

<span data-ttu-id="1a950-p101">Update (1/30/19): im Oktober 2018 haben wir mit einer kleinen Auswahl an Kunden zusammengearbeitet, um zu verstehen, ob wir den Schutz vereinfachen können, indem Sie vertrauliche e-Mails auf der Grundlage bestimmter vertraulicher Informationstypen automatisch verschlüsseln. Basierend auf positiven Feedback aus diesem Beispiel haben wir uns entschieden, im Dezember 2018 zu einem vielfältigeren Profil von Mandanten zu expandieren. Nachdem wir die nächste Einführung zur Auswahl von Mandanten kommuniziert haben, haben wir uns Ihr Feedback angehört und festgestellt, dass Kunden mit komplexeren Umgebungen die Regeln vorsichtiger implementieren wollten, und wir passen unsere Pläne daher an.</span><span class="sxs-lookup"><span data-stu-id="1a950-p101">Update (1/30/19): In October 2018, we worked with a small sample of customers to understand if we can simplify protection by automatically encrypting sensitive emails based on certain sensitive information types. Based on positive feedback from this sample, we decided to expand to a more diverse profile of tenants in December 2018. After communicating the next roll-out to select tenants, we listened to your feedback and determined that customers with more complex environments wanted to implement the rules more cautiously, and we are therefore adjusting our plans.</span></span>

<span data-ttu-id="1a950-p102">Wenn Ihre Organisation für die Einführung ab dem 15. Januar 2019 ausgewählt wurde, wird die automatische Richtlinie nicht eingeführt. Stattdessen geben wir in diesem Artikel Anweisungen dazu, wie Sie die Einführung selbst abschließen können. Lesen Sie weiter, um herauszufinden, wie.</span><span class="sxs-lookup"><span data-stu-id="1a950-p102">If your organization was selected for the roll-out starting January 15, 2019, we will not roll out the automatic policy. Instead, we are providing instructions in this article on how you can complete the roll-out yourselves. Keep reading to find out how.</span></span>

||
|:-----|
|<span data-ttu-id="1a950-p103">Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="1a950-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and ITPros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="how-to-create-the-sensitive-information-type-policy-for-your-tenant"></a><span data-ttu-id="1a950-113">Erstellen der Richtlinie für vertrauliche Informationstypen für Ihren Mandanten</span><span class="sxs-lookup"><span data-stu-id="1a950-113">How to create the sensitive information type policy for your tenant</span></span>

<span data-ttu-id="1a950-p104">Sie können entweder Exchange-Nachrichtenfluss Regeln oder Office 365 Data Loss Prevention (DLP) verwenden, um die Richtlinie für vertrauliche Informationstypen zu erstellen. Zum Erstellen einer Exchange-Nachrichtenfluss Regel können Sie entweder die Exchange-Verwaltungskonsole (EAC) oder PowerShell verwenden.</span><span class="sxs-lookup"><span data-stu-id="1a950-p104">You can use either Exchange mail flow rules or Office 365 Data Loss Prevention (DLP) to create the sensitive information type policy. To create an Exchange mail flow rule you can use either the Exchange admin center (EAC) or PowerShell.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-the-eac"></a><span data-ttu-id="1a950-116">So erstellen Sie die Richtlinie mithilfe von Nachrichtenfluss Regeln in der Exchange-verwaltungsKONSOLE</span><span class="sxs-lookup"><span data-stu-id="1a950-116">To create the policy by using mail flow rules in the EAC</span></span>

<span data-ttu-id="1a950-p105">Melden Sie sich bei der Exchange-Verwaltungskonsole an, und wechseln Sie zu **Nachrichtenfluss** > **Regeln**. Erstellen Sie dort eine Regel, die die Office 365-Nachrichtenverschlüsselung auf Grundlage von Bedingungen wie dem vorhanden sein bestimmter Schlüsselwörter oder vertraulicher Informationstypen in der Nachricht oder Anlage anwendet.</span><span class="sxs-lookup"><span data-stu-id="1a950-p105">Sign-in to the Exchange admin center (EAC) and go to **Mail flow** > **Rules**. There, create a rule that applies Office 365 Message Encryption based on conditions such as the presence of certain keywords or sensitive information types in the message or attachment.</span></span>

### <a name="to-create-the-policy-by-using-mail-flow-rules-in-powershell"></a><span data-ttu-id="1a950-119">So erstellen Sie die Richtlinie mithilfe von Nachrichtenfluss Regeln in PowerShell</span><span class="sxs-lookup"><span data-stu-id="1a950-119">To create the policy by using mail flow rules in PowerShell</span></span>

<span data-ttu-id="1a950-p106">Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell). Verwenden Sie die Cmdlets Set-IRMConfiguration und New-TransporRule, um die Richtlinie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1a950-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell). Use the Set-IRMConfiguration and New-TransporRule cmdlets to create the policy.</span></span>

### <a name="example-mail-flow-rule-created-with-powershell"></a><span data-ttu-id="1a950-123">Mit PowerShell erstellte Beispiel-e-Mail-Fluss Regel</span><span class="sxs-lookup"><span data-stu-id="1a950-123">Example mail flow rule created with PowerShell</span></span>

<span data-ttu-id="1a950-124">Durch Ausführen der folgenden Befehle in PowerShell wird eine Exchange-Nachrichtenfluss Regel erstellt, mit der e-Mails, die sich außerhalb \*\* Ihrer Organisation befinden, automatisch mit der Verschlüsselungsrichtlinie verschlüsselt werden, wenn die e-Mails oder Ihre Anlagen die folgenden vertraulichen Informationstypen:</span><span class="sxs-lookup"><span data-stu-id="1a950-124">Running the following commands in PowerShell create an Exchange mail flow rule that automatically encrypts emails going outside your organization with the *Encrypt-Only* policy if the emails or their attachments contain the following sensitive information types:</span></span>

- <span data-ttu-id="1a950-125">ABA-Routingnummer</span><span class="sxs-lookup"><span data-stu-id="1a950-125">ABA routing number</span></span>
- <span data-ttu-id="1a950-126">Kreditkartennummer</span><span class="sxs-lookup"><span data-stu-id="1a950-126">Credit card Number</span></span>
- <span data-ttu-id="1a950-127">DEA-Nummer (Drug Enforcement Agency)</span><span class="sxs-lookup"><span data-stu-id="1a950-127">Drug Enforcement Agency (DEA) number</span></span>
- <span data-ttu-id="1a950-p107">U.S./UK-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="1a950-p107">U.S. / U.K. passport number</span></span>
- <span data-ttu-id="1a950-130">US-Bankkontonummer</span><span class="sxs-lookup"><span data-stu-id="1a950-130">U.S. bank account number</span></span>
- <span data-ttu-id="1a950-131">US-Steueridentifikationsnummer (ITIN)</span><span class="sxs-lookup"><span data-stu-id="1a950-131">U.S. Individual Taxpayer Identification Number (ITIN)</span></span>
- <span data-ttu-id="1a950-132">US-Sozialversicherungsnummer</span><span class="sxs-lookup"><span data-stu-id="1a950-132">U.S. Social Security Number (SSN)</span></span>

```powershell
Set-IRMConfiguration -DecryptAttachmentsForEncryptOnly $true
New-TransportRule -Name "Encrypt outbound sensitive emails (out of box rule)" -SentToScope  NotInOrganization  -ApplyRightsProtectionTemplate "Encrypt" -MessageContainsDataClassifications @(@{Name="ABA Routing Number"; minCount="1"},@{Name="Credit Card Number"; minCount="1"},@{Name="Drug Enforcement Agency (DEA) Number"; minCount="1"},@{Name="U.S. / U.K. Passport Number"; minCount="1"},@{Name="U.S. Bank Account Number"; minCount="1"},@{Name="U.S. Individual Taxpayer Identification Number (ITIN)"; minCount="1"},@{Name="U.S. Social Security Number (SSN)"; minCount="1"}) -SenderNotificationType "NotifyOnly"
```

## <a name="how-recipients-access-attachments"></a><span data-ttu-id="1a950-133">Wie Empfänger auf Anlagen zugreifen</span><span class="sxs-lookup"><span data-stu-id="1a950-133">How recipients access attachments</span></span>

<span data-ttu-id="1a950-134">Nachdem eine Nachricht verschlüsselt wurde, haben die Empfänger uneingeschränkten Zugriff auf Anlagen, nachdem Sie auf Ihre verschlüsselte e-Mail zugegriffen haben.</span><span class="sxs-lookup"><span data-stu-id="1a950-134">Once a message is encrypted, recipients will have unrestricted access to attachments once they access and open their encrypted email.</span></span>

## <a name="to-prepare-for-this-change"></a><span data-ttu-id="1a950-135">So bereiten Sie diese Änderung vor</span><span class="sxs-lookup"><span data-stu-id="1a950-135">To prepare for this change</span></span>

<span data-ttu-id="1a950-p108">Möglicherweise möchten Sie die entsprechenden Endbenutzer Dokumentationen und Schulungsmaterialien aktualisieren, um Personen in Ihrer Organisation auf diese Änderung vorzubereiten. Teilen Sie diese Office 365-Nachrichten Verschlüsselungs Ressourcen bei Bedarf Ihren Benutzern mit:</span><span class="sxs-lookup"><span data-stu-id="1a950-p108">You may want to update any applicable end-user documentation and training materials to prepare people in your organization for this change. Share these Office 365 Message Encryption resources with your users as appropriate:</span></span>

- [<span data-ttu-id="1a950-138">Senden, anzeigen und beantworten von verschlüsselten Nachrichten in Outlook für PC</span><span class="sxs-lookup"><span data-stu-id="1a950-138">Send, view, and reply to encrypted messages in Outlook for PC</span></span>](https://support.office.com/article/send-view-and-reply-to-encrypted-messages-in-outlook-for-pc-eaa43495-9bbb-4fca-922a-df90dee51980)
- [<span data-ttu-id="1a950-139">Office 365 Essentials Video: Office-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="1a950-139">Office 365 Essentials Video: Office Message Encryption</span></span>](https://youtu.be/CQR0cG_iEUc)

## <a name="view-these-changes-in-the-audit-log"></a><span data-ttu-id="1a950-140">Diese Änderungen im Überwachungsprotokoll anzeigen</span><span class="sxs-lookup"><span data-stu-id="1a950-140">View these changes in the Audit log</span></span>

<span data-ttu-id="1a950-p109">Diese Aktivität wird überwacht und steht Office 365-Administratoren zur Verfügung. Der Vorgang ist "New-transportRule" und ein Auszug aus einem Beispiel Überwachungseintrag aus der Überwachungsprotokoll Suche im Security & Compliance Center befindet sich unten:</span><span class="sxs-lookup"><span data-stu-id="1a950-p109">This activity is audited and is available to Office 365 administrators. The operation is ‘New-TransportRule’ and a snippet of a sample audit entry from the Audit Log Search in Security & Compliance Center is below:</span></span>

|     |
| --- |
| <span data-ttu-id="1a950-143">*{"Creation-Zeit": "2018-11-28T23:35:01", "ID": "A1b2C3d4-daa0-4c4f-A019-03a1234a1b0c", "Operation": "New-transportRule", "Organizational-ID": "123456-221d-12345", "RecordType": 1, "ResultStatus": "true", "UserKey": "Microsoft-Operator", " Usertype ": 3," Version ": 1," Workload ":" Exchange "," ClientIP ":" 123.456.147.68:17584 "," ObjectId ":" "," UserId ":" Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso. onmicrosoft. com "," OriginatingServer ":" CY4PR13MBXXXX ( 15.20.1382.008) "," Parameters ": {" Name ":" Organization "," Value ":" 123456-221d-12346 "{" Name ":" ApplyRightsProtectionTemplate "," Value ":" Encrypt "}, {" Name ":" Name "," Value ":" verSchlüsseln von ausgehenden vertraulichen e-Mails (Out of Box Rule) "}, {" Name " MessageContainsDataClassifications "... usw.*</span><span class="sxs-lookup"><span data-stu-id="1a950-143">*{"CreationTime":"2018-11-28T23:35:01","Id":"a1b2c3d4-daa0-4c4f-a019-03a1234a1b0c","Operation":"New-TransportRule","OrganizationId":"123456-221d-12345 ","RecordType":1,"ResultStatus":"True","UserKey":"Microsoft Operator","UserType":3,"Version":1,"Workload":"Exchange","ClientIP":"123.456.147.68:17584","ObjectId":"","UserId":"Microsoft Operator","ExternalAccess":true,"OrganizationName":"contoso.onmicrosoft.com","OriginatingServer":"CY4PR13MBXXXX (15.20.1382.008)","Parameters": {"Name":"Organization","Value":"123456-221d-12346"{"Name":"ApplyRightsProtectionTemplate","Value":"Encrypt"},{"Name":"Name","Value":"Encrypt outbound sensitive emails (out of box rule)"},{"Name":"MessageContainsDataClassifications”…etc.*</span></span> |
| |

## <a name="to-disable-or-customize-the-sensitive-information-types-policy"></a><span data-ttu-id="1a950-144">So deaktivieren oder ändern Sie die Richtlinie für vertrauliche Informationstypen</span><span class="sxs-lookup"><span data-stu-id="1a950-144">To disable or customize the sensitive information types policy</span></span>

<span data-ttu-id="1a950-145">Nachdem Sie die Exchange-Nachrichtenfluss Regel erstellt haben, können Sie [die Regel deaktivieren oder bearbeiten](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) , indem Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** > **Regeln** wechseln und die Regel "*vertrauliche e-Mails verschlüsseln (außerhalb der Box-Regel)* " deaktivieren. ".</span><span class="sxs-lookup"><span data-stu-id="1a950-145">Once you've created the Exchange mail flow rule, you can [disable or edit the rule](https://docs.microsoft.com/exchange/security-and-compliance/mail-flow-rules/manage-mail-flow-rules#enable-or-disable-a-mail-flow-rule) by going to **Mail flow** > **Rules** in the Exchange admin center (EAC) and disable the rule “*Encrypt outbound sensitive emails (out of box rule)*”.</span></span>
