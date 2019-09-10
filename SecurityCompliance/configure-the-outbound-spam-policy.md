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
# <a name="configure-outbound-spam-policy-notifications-in-office-365"></a><span data-ttu-id="739c6-103">Konfigurieren von Benachrichtigungen über ausgehende Spam Richtlinien in Office 365</span><span class="sxs-lookup"><span data-stu-id="739c6-103">Configure outbound spam policy notifications in Office 365</span></span>

<span data-ttu-id="739c6-104">Die Filterung ausgehender Spamnachrichten ist immer aktiviert, wenn Sie den Dienst für das Senden ausgehender E-Mails verwenden und dadurch Organisationen, die den Dienst nutzen, und ihre jeweiligen Empfänger schützen.</span><span class="sxs-lookup"><span data-stu-id="739c6-104">Outbound spam filtering is always enabled if you use the service for sending outbound email, thereby protecting organizations using the service and their intended recipients.</span></span> <span data-ttu-id="739c6-105">Ebenso wie die Filterung eingehender Nachrichten besteht die Filterung ausgehender Nachrichten aus einer Verbindungsfilterung und einer Inhaltsfilterung, wobei die Einstellungen für den ausgehenden Filter nicht konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="739c6-105">Similar to inbound filtering, outbound spam filtering is comprised of connection filtering and content filtering, however the outbound filter settings are not configurable.</span></span> <span data-ttu-id="739c6-106">Wenn eine ausgehende Nachricht als Spam identifiziert wird, wird sie durch den Pool für besonders riskante Zustellungen geleitet, der die Wahrscheinlichkeit reduziert, dass der normale Pool für ausgehende IP-Adressen einer Sperrliste hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="739c6-106">If an outbound message is determined to be spam, it is routed through the higher risk delivery pool, which reduces the probability of the normal outbound-IP pool being added to a block list.</span></span> <span data-ttu-id="739c6-107">Falls ein Kunde auch weiterhin ausgehende Spamnachrichten über den Dienst sendet, wird er für das Senden von Nachrichten gesperrt.</span><span class="sxs-lookup"><span data-stu-id="739c6-107">If a customer continues to send outbound spam through the service, they will be blocked from sending messages.</span></span>

<span data-ttu-id="739c6-108">Sie können zwar keine ausgehende Spamfilterung deaktivieren oder ändern, aber Sie können die folgenden Einstellungen für ausgehende Spambenachrichtigungen konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="739c6-108">Although you can't disable or change outbound spam filtering, you can configure the following outbound spam notification settings:</span></span>

- <span data-ttu-id="739c6-109">**Kopien von verdächtigen Nachrichten senden**: diese Nachrichten werden als Spam gekennzeichnet (unabhängig von der SCL-Bewertung) und werden nicht vom Filter zurückgewiesen, sondern durch den höheren Risiko Zustellungs Pool weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="739c6-109">**Send copies of suspicious messages**: These messages are marked as spam (regardless of the SCL rating) and are not rejected by the filter, but are routed through the higher risk delivery pool.</span></span> <span data-ttu-id="739c6-110">Sie können die Exchange-Verwaltungskonsole (EAC) oder die \*\* \*-HostedOutboundSpamFilterPolicy-\*\* Cmdlets in Exchange Online PowerShell oder Exchange Online Protection PowerShell verwenden, um zusätzliche Empfänger für diese erkannten Nachrichten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="739c6-110">You can use the Exchange admin center (EAC) or the **\*-HostedOutboundSpamFilterPolicy** cmdlets in Exchange Online PowerShell or Exchange Online Protection PowerShell to specify addition recipients for these detected messages.</span></span> <span data-ttu-id="739c6-111">Beachten Sie, dass die Empfänger als **Bcc** -Empfänger hinzugefügt werden (die Felder **from** und **to** sind der ursprüngliche Absender und Empfänger).</span><span class="sxs-lookup"><span data-stu-id="739c6-111">Note that the recipients are added as **Bcc** recipients (the **From** and **To** fields are the original sender and recipient).</span></span>

- <span data-ttu-id="739c6-112">**Senden von Benachrichtigungen, wenn ein Absender blockiert wird**: Wenn ein bestimmter Benutzer eine erhebliche Menge an Spam eingeht, ist der Benutzer für das Senden von e-Mail-Nachrichten deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="739c6-112">**Send notifications when a sender is blocked**: When a significant amount of spam is coming from a particular user, the user is disabled from sending email messages.</span></span> <span data-ttu-id="739c6-113">Administratoren werden standardmäßig benachrichtigt, aber Sie können den **Benutzer vom Senden von e-Mail-** [Warnungsrichtlinien](alert-policies.md) im Office 365 Security #a0 Compliance Center beschränken, um zusätzliche Benachrichtigungsempfänger zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="739c6-113">Admins are notified by default, but you can use the **User restricted from sending email** [alert policy](alert-policies.md) in the Office 365 Security & Compliance Center to configure additional notification recipients.</span></span>

  <span data-ttu-id="739c6-114">Ein Beispiel für diese Benachrichtigung finden Sie unter [Beispielbenachrichtigung, wenn ein Absender aufgrund des Versendens von ausgehendem Spam blockiert wird](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span><span class="sxs-lookup"><span data-stu-id="739c6-114">To see what this notification looks like, see [Sample notification when a sender is blocked sending outbound spam](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md).</span></span> <span data-ttu-id="739c6-115">Informationen zur erneuten Aktivierung finden Sie unter [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span><span class="sxs-lookup"><span data-stu-id="739c6-115">For information about getting re-enabled, see [Removing a user, domain, or IP address from a block list after sending spam email](http://technet.microsoft.com/library/712cfcc1-31e8-4e51-8561-b64258a8f1e5.aspx).</span></span>

## <a name="what-do-you-need-to-know-before-you-begin"></a><span data-ttu-id="739c6-116">Was sollten Sie wissen, bevor Sie beginnen?</span><span class="sxs-lookup"><span data-stu-id="739c6-116">What do you need to know before you begin?</span></span>

- <span data-ttu-id="739c6-117">Geschätzte Zeit bis zum Abschließen des Vorgangs: 5 Minuten</span><span class="sxs-lookup"><span data-stu-id="739c6-117">Estimated time to complete: 5 minutes</span></span>

- <span data-ttu-id="739c6-118">Informationen zum Öffnen des Security & Compliance Center finden Sie unter [Wechseln zum Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="739c6-118">To open the Security & Compliance Center, see [Go to the Office 365 Security & Compliance Center](go-to-the-securitycompliance-center.md).</span></span>

- <span data-ttu-id="739c6-119">Informationen zum Öffnen des EAC finden Sie unter [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) oder [Exchange Admin Center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span><span class="sxs-lookup"><span data-stu-id="739c6-119">To open the EAC, see [Exchange admin center in Exchange Online](https://docs.microsoft.com/Exchange/exchange-admin-center) or [Exchange admin center in Exchange Online Protection](exchange-admin-center-in-exchange-online-protection-eop.md).</span></span>

- <span data-ttu-id="739c6-120">Informationen zum Öffnen Exchange Online PowerShell finden Sie unter [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span><span class="sxs-lookup"><span data-stu-id="739c6-120">To open Exchange Online PowerShell, see [Connect to Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/connect-to-exchange-online-powershell/connect-to-exchange-online-powershell).</span></span> <span data-ttu-id="739c6-121">Informationen zum Öffnen von Exchange Online Protection PowerShell finden Sie unter [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).</span><span class="sxs-lookup"><span data-stu-id="739c6-121">To open Exchange Online Protection PowerShell, see [Connect to Exchange Online Protection PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-eop/exchange-online-protection-powershell).</span></span>

- <span data-ttu-id="739c6-122">Ihrem Konto müssen Berechtigungen zugewiesen werden, bevor Sie dieses Verfahren ausführen können.</span><span class="sxs-lookup"><span data-stu-id="739c6-122">Your account needs to be assigned permissions before you can perform this procedure.</span></span> <span data-ttu-id="739c6-123">Informationen zu den von Ihnen benötigten Berechtigungen finden Sie unter "Manage Alerts" Role entry in [Permissions in the Office 365 Security #a0 Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="739c6-123">To see what permissions you need, see the "Manage Alerts" role entry in [Permissions in the Office 365 Security & Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>

## <a name="use-the-eac-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="739c6-124">Konfigurieren zusätzlicher Empfänger für ausgehende Spamnachrichten mithilfe der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="739c6-124">Use the EAC to configure additional recipients for outbound spam messages</span></span>

1. <span data-ttu-id="739c6-125">Wechseln Sie in der Exchange-Verwaltungskonsole zu **Schutz** \> **ausgehenden Spam**.</span><span class="sxs-lookup"><span data-stu-id="739c6-125">In the EAC, go to **Protection** \> **Outbound spam**.</span></span>

2. <span data-ttu-id="739c6-126">Wählen Sie die Richtlinie **default**aus, und klicken Sie dann](media/ITPro-EAC-EditIcon.png)auf Bearbeitungssymbol **Bearbeiten** ![.</span><span class="sxs-lookup"><span data-stu-id="739c6-126">Select the policy named **Default**, and then click **Edit** ![Edit icon](media/ITPro-EAC-EditIcon.png).</span></span>

3. <span data-ttu-id="739c6-127">Überprüfen Sie auf der Seite Eigenschaften, die geöffnet wird, ob die Registerkarte **ausgehende Spameinstellungen** ausgewählt ist, und konfigurieren Sie dann die folgende Einstellung:</span><span class="sxs-lookup"><span data-stu-id="739c6-127">In the properties page that opens, verify that the **Outbound spam preferences** tab is selected, and then configure the following setting:</span></span>

   <span data-ttu-id="739c6-128">**Senden Sie eine Kopie aller Verdächtigen ausgehenden e-Mail-Nachrichten an die folgende e-Mail-Adresse oder**Adresse: Aktivieren Sie das Kontrollkästchen, und geben Sie die e-Mail-Adressen von einem oder mehreren Administratoren ein, die dem Feld **Bcc** für erkannte Nachrichten hinzugefügt werden sollen</span><span class="sxs-lookup"><span data-stu-id="739c6-128">**Send a copy of all suspicious outbound email messages to the following email address or addresses**: Select the check box and enter the email addresses of one or more administrators who should be added to the **Bcc** field of detected messages.</span></span> <span data-ttu-id="739c6-129">Trennen Sie mehrere e-Mail-Adressen durch ein Semikolon (;).</span><span class="sxs-lookup"><span data-stu-id="739c6-129">Separate multiple email addresses with a semicolon ( ; ).</span></span>

   <span data-ttu-id="739c6-130">Klicken Sie nach Abschluss des Vorgangs auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="739c6-130">When you're finished, click **Save**.</span></span>

### <a name="use-exchange-online-powershell-or-exchange-online-protection-powershell-to-configure-additional-recipients-for-outbound-spam-messages"></a><span data-ttu-id="739c6-131">Verwenden Sie Exchange Online PowerShell oder Exchange Online Protection PowerShell, um zusätzliche Empfänger für ausgehende Spamnachrichten zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="739c6-131">Use Exchange Online PowerShell or Exchange Online Protection PowerShell to configure additional recipients for outbound spam messages</span></span>

<span data-ttu-id="739c6-132">Verwenden Sie die folgende Syntax, um zusätzliche Empfänger für ausgehende Spamnachrichten zu aktivieren und zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="739c6-132">To enable and configure additional recipients for outbound spam messages, use the following syntax:</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients <recipients>
```

- <span data-ttu-id="739c6-133">Verwenden Sie die Syntax `emailaddress1,emailaddress2,...emailaddressN`, um Empfänger anzugeben, die alle vorhandenen Werte überschreiben.</span><span class="sxs-lookup"><span data-stu-id="739c6-133">To specify recipients that overwrite all existing values, use the syntax `emailaddress1,emailaddress2,...emailaddressN`.</span></span>

- <span data-ttu-id="739c6-134">Verwenden Sie die Syntax `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`, um Empfänger selektiv hinzuzufügen oder zu entfernen, ohne die anderen Einträge zu beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="739c6-134">To selectively add or remove recipients without affecting the other entries, use the syntax `@{Add="\<emailaddress1\>","\<emailaddress2\>"...; Remove="\<emailaddress1\>","\<emailaddress2\>"...}`.</span></span>

<span data-ttu-id="739c6-135">In diesem Beispiel werden Chris@contoso.com, Laura@contoso.com und Julia@contoso.com als Bcc-Empfänger für ausgehende Spamnachrichten aktiviert und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="739c6-135">This example enables and configures chris@contoso.com, laura@contoso.com and julia@contoso.com as Bcc recipients for outbound spam messages.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundMail $true -BccSuspiciousOutboundAdditionalRecipients chris@contoso.com,laura@contoso.com,julia@contoso.com
```

<span data-ttu-id="739c6-136">In diesem Beispiel wird Michelle@contoso.com als zusätzlicher Bcc-Empfänger hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="739c6-136">This example adds michelle@contoso.com as an additional Bcc recipient.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Add=michelle@contoso.com}
```

<span data-ttu-id="739c6-137">In diesem Beispiel werden Chris@contoso.com und Julia@contoso.com aus der Liste der Bcc-Empfänger entfernt.</span><span class="sxs-lookup"><span data-stu-id="739c6-137">This example removes chris@contoso.com and julia@contoso.com from the list of Bcc recipients.</span></span>

```PowerShell
Set-HostedOutboundSpamFilterPolicy -Identity Default -BccSuspiciousOutboundAdditionalRecipients @{Remove='chris@contoso.com','julia@contoso.com'}
```

<span data-ttu-id="739c6-138">Ausführliche Informationen zu Syntax und Parametern finden Sie unter [Sets-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span><span class="sxs-lookup"><span data-stu-id="739c6-138">For detailed syntax and parameter information, see [Set-HostedOutboundSpamFilterPolicy](https://docs.microsoft.com/powershell/module/exchange/antispam-antimalware/set-hostedoutboundspamfilterpolicy).</span></span>

<span data-ttu-id="739c6-139">**Hinweis**: führen Sie den `Get-HostedOutboundSpamFilterPolicy | Format-List` Befehl aus, um die aktuellen Werte der Eigenschaften *BccSuspiciousOutboundMail* und *BccSuspiciousOutboundAdditionalRecipients* anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="739c6-139">**Note**: Run the command `Get-HostedOutboundSpamFilterPolicy | Format-List` to see the current values of the *BccSuspiciousOutboundMail* and *BccSuspiciousOutboundAdditionalRecipients* properties.</span></span>

## <a name="use-the-security--compliance-center-to-configure-notifications-when-a-sender-is-blocked"></a><span data-ttu-id="739c6-140">Verwenden des Security #a0 Compliance Center zum Konfigurieren von Benachrichtigungen, wenn ein Absender blockiert wird</span><span class="sxs-lookup"><span data-stu-id="739c6-140">Use the Security & Compliance Center to configure notifications when a sender is blocked</span></span>

1. <span data-ttu-id="739c6-141">Wechseln Sie im Security #a0 Compliance Center **zu** \> Alerts **Alerts-Richtlinien**.</span><span class="sxs-lookup"><span data-stu-id="739c6-141">In the Security & Compliance Center, go to **Alerts** \> **Alert Policies**.</span></span>

2. <span data-ttu-id="739c6-142">Suchen und wählen Sie die Richtlinie mit dem Namen " **Benutzer eingeschränkt vom Senden von e-Mails" aus**.</span><span class="sxs-lookup"><span data-stu-id="739c6-142">Find and select the policy named **User restricted from sending email**.</span></span>

3. <span data-ttu-id="739c6-143">Klicken Sie im Dialogfeld ausfliegen, das geöffnet wird, auf **Richtlinie bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="739c6-143">In the fly out that opens, click **Edit policy**.</span></span>

4. <span data-ttu-id="739c6-144">Konfigurieren Sie auf der angezeigten Seite **Empfänger bearbeiten** die folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="739c6-144">In the **Edit recipients** page that appears, configure the following settings:</span></span>

   - <span data-ttu-id="739c6-145">**Senden von e-Mail-Benachrichtigungen**: Vergewissern Sie sich, dass **on** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="739c6-145">**Send email notifications**: Verify that **On** is selected.</span></span>

   - <span data-ttu-id="739c6-146">**E-Mail-Empfänger**: Standardmäßig ist **TenantAdmins** der einzige Wert hier.</span><span class="sxs-lookup"><span data-stu-id="739c6-146">**Email recipients**: By default **TenantAdmins** is the only value here.</span></span> <span data-ttu-id="739c6-147">Wenn Sie weitere Empfänger hinzufügen möchten, klicken Sie in diesem Feld auf eine leere Stelle, beginnen Sie mit der Eingabe des Empfängers, und wählen Sie den Empfänger aus, wenn der Name aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="739c6-147">To add additional recipients, click in an empty spot in this box, start typing the recipient, and select the recipient when their name resolves.</span></span> <span data-ttu-id="739c6-148">Klicken Sie zum Entfernen von Empfängern auf das **X** neben dem Namen.</span><span class="sxs-lookup"><span data-stu-id="739c6-148">To remove recipients, click on the **X** next to their names.</span></span>

   - <span data-ttu-id="739c6-149">**Grenzwert für tägliche Benachrichtigungen**: der Standardwert ist **No Limit**, aber Sie können verschiedene Grenzwerte von 1 bis 200 konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="739c6-149">**Daily notification limit**: The default value is **No limit**, but you can configure various limits from 1 to 200.</span></span>

   <span data-ttu-id="739c6-150">Klicken Sie nach Abschluss des Vorgangs auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="739c6-150">When you're finished, click **Save**.</span></span>

## <a name="for-more-information"></a><span data-ttu-id="739c6-151">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="739c6-151">For more information</span></span>

[<span data-ttu-id="739c6-152">Pool für besonders riskante Zustellungen für ausgehende Nachrichten</span><span class="sxs-lookup"><span data-stu-id="739c6-152">High-risk delivery pool for outbound messages</span></span>](high-risk-delivery-pool-for-outbound-messages.md)

[<span data-ttu-id="739c6-153">Häufig gestellte Fragen zum Anti-Spam-Schutz</span><span class="sxs-lookup"><span data-stu-id="739c6-153">Anti-spam protection FAQ</span></span>](anti-spam-protection-faq.md)
