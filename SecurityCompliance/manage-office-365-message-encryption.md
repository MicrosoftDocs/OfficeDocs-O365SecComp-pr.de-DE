---
title: Verwalten der Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 5/8/2019
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Nachdem Sie die Einrichtung von Office 365-Nachrichtenverschlüsselung (OM) abgeschlossen haben, können Sie die Konfiguration Ihrer Bereitstellung auf verschiedene Weise anpassen. Sie können beispielsweise konfigurieren, ob einmalige Code-Codes aktiviert werden sollen, die Schaltfläche schützen in Outlook im Web und vieles mehr angezeigt werden soll. In den Aufgaben in diesem Artikel wird beschrieben, wie.
ms.openlocfilehash: 1afaaea3cd744878630598acd3f02dc7dc70e9cb
ms.sourcegitcommit: 865b3dc071150b20bf3967e1263fc54e75898284
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/09/2019
ms.locfileid: "33834924"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="d14ff-105">Verwalten der Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d14ff-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="d14ff-106">Nachdem Sie die Einrichtung von Office 365-Nachrichtenverschlüsselung (OM) abgeschlossen haben, können Sie die Konfiguration Ihrer Bereitstellung auf verschiedene Weise anpassen.</span><span class="sxs-lookup"><span data-stu-id="d14ff-106">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in several ways.</span></span> <span data-ttu-id="d14ff-107">Sie können beispielsweise konfigurieren, ob einmalige Code-Codes aktiviert werden sollen, die Schaltfläche **schützen** in Outlook im Web und vieles mehr angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d14ff-107">For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more.</span></span> <span data-ttu-id="d14ff-108">In den Aufgaben in diesem Artikel wird beschrieben, wie.</span><span class="sxs-lookup"><span data-stu-id="d14ff-108">The tasks in this article describe how.</span></span>

## <a name="manage-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="d14ff-109">Verwalten, ob die Empfänger von Google, Yahoo und Microsoft-Konto diese Konten verwenden können, um sich beim Office 365-Nachrichten Verschlüsselungs Portal anzumelden</span><span class="sxs-lookup"><span data-stu-id="d14ff-109">Manage whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="d14ff-110">Wenn Sie die neuen Office 365-Nachrichten Verschlüsselungsfunktionen einrichten, können Benutzer in Ihrer Organisation Nachrichten an Empfänger senden, die sich außerhalb Ihrer Office 365-Organisation befinden.</span><span class="sxs-lookup"><span data-stu-id="d14ff-110">When you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization.</span></span> <span data-ttu-id="d14ff-111">Wenn der Empfänger eine *soziale ID* wie ein Google-Konto, ein Yahoo-Konto oder ein Microsoft-Konto verwendet, kann sich der Empfänger mit einer sozialen ID beim OM-Portal anmelden.</span><span class="sxs-lookup"><span data-stu-id="d14ff-111">If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal with a social ID.</span></span> <span data-ttu-id="d14ff-112">Wenn Sie möchten, können Sie festlegen, dass Empfänger keine sozialen IDs verwenden dürfen, um sich beim OM-Portal anzumelden.</span><span class="sxs-lookup"><span data-stu-id="d14ff-112">If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-recipients-can-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="d14ff-113">So verwalten Sie, ob Empfänger soziale IDs verwenden können, um sich beim OM-Portal anzumelden</span><span class="sxs-lookup"><span data-stu-id="d14ff-113">To manage whether recipients can use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="d14ff-114">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d14ff-114">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="d14ff-115">Führen Sie das Cmdlet Set-OMEConfiguration mit dem Parameter SocialIdSignIn wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d14ff-115">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter"> -SocialIdSignIn <$true|$false>
   ```

   <span data-ttu-id="d14ff-116">Um beispielsweise soziale IDs zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="d14ff-116">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="d14ff-117">So aktivieren Sie soziale IDs:</span><span class="sxs-lookup"><span data-stu-id="d14ff-117">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="manage-the-use-of-one-time-pass-codes-for-the-office-365-message-encryption-portal"></a><span data-ttu-id="d14ff-118">Verwalten der Verwendung von einmaligen Durchlaufcodes für das Office 365-Nachrichten Verschlüsselungs Portal</span><span class="sxs-lookup"><span data-stu-id="d14ff-118">Manage the use of one-time pass codes for the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="d14ff-119">Wenn der Empfänger einer Nachricht, die von OM verschlüsselt wird, nicht Outlook verwendet, unabhängig vom Konto, das der Empfänger verwendet, erhält der Empfänger einen Link zur zeitlich begrenzten Webansicht, über die er die Nachricht lesen kann.</span><span class="sxs-lookup"><span data-stu-id="d14ff-119">If the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message.</span></span> <span data-ttu-id="d14ff-120">Dieser Link enthält einen einmaligen Code.</span><span class="sxs-lookup"><span data-stu-id="d14ff-120">This link includes a one-time pass code.</span></span> <span data-ttu-id="d14ff-121">Als Administrator können Sie entscheiden, ob sich Empfänger mit einmaligen Codes bei dem OM-Portal anmelden können.</span><span class="sxs-lookup"><span data-stu-id="d14ff-121">As an administrator, you can decide if recipients can use one-time pass codes to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-ome-generates-one-time-pass-codes"></a><span data-ttu-id="d14ff-122">So verwalten Sie, ob OM einmalige Durchlaufcodes generiert</span><span class="sxs-lookup"><span data-stu-id="d14ff-122">To manage whether OME generates one-time pass codes</span></span>
  
1. <span data-ttu-id="d14ff-123">Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her.</span><span class="sxs-lookup"><span data-stu-id="d14ff-123">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="d14ff-124">Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="d14ff-124">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="d14ff-125">Führen Sie das Cmdlet Set-OMEConfiguration mit dem Parameter OTPEnabled aus:</span><span class="sxs-lookup"><span data-stu-id="d14ff-125">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="d14ff-126">So können Sie beispielsweise einmalige Durchlaufcodes deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="d14ff-126">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="d14ff-127">So aktivieren Sie einmalige Code-Codes:</span><span class="sxs-lookup"><span data-stu-id="d14ff-127">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="manage-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="d14ff-128">Verwalten der Anzeige der Schaltfläche "schützen" in Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="d14ff-128">Manage the display of the Protect button in Outlook on the web</span></span>

<span data-ttu-id="d14ff-129">Die Schaltfläche **schützen** in Outlook im Web ist deaktiviert, wenn Sie OM einrichten.</span><span class="sxs-lookup"><span data-stu-id="d14ff-129">The **Protect** button in Outlook on the web is disabled when you set up OME.</span></span> <span data-ttu-id="d14ff-130">Als Administrator können Sie verwalten, ob diese Schaltfläche Endbenutzern angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d14ff-130">As an administrator, you can manage whether to display this button to end users.</span></span>
  
### <a name="to-manage-whether-the-protect-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="d14ff-131">So verwalten Sie, ob die Schaltfläche schützen in Outlook im Web angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="d14ff-131">To manage whether the Protect button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="d14ff-132">Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her.</span><span class="sxs-lookup"><span data-stu-id="d14ff-132">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="d14ff-133">Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="d14ff-133">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="d14ff-134">Führen Sie das Cmdlet Set-IRMConfiguration mit dem-SimplifiedClientAccessEnabled-Parameter aus:</span><span class="sxs-lookup"><span data-stu-id="d14ff-134">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="d14ff-135">Um beispielsweise die Schaltfläche **Protect** zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="d14ff-135">For example, to disable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="d14ff-136">So aktivieren Sie die Schaltfläche " **schützen** "</span><span class="sxs-lookup"><span data-stu-id="d14ff-136">To enable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="d14ff-137">Aktivieren der dienstseitigen Entschlüsselung von e-Mail-Nachrichten für IOS-Mail-App-Benutzer</span><span class="sxs-lookup"><span data-stu-id="d14ff-137">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="d14ff-138">Die IOS-Mail-App kann nicht mit der Office 365-Nachrichtenverschlüsselung geschützte Nachrichten entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="d14ff-138">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption.</span></span> <span data-ttu-id="d14ff-139">Als Office 365-Administrator können Sie die dienstseitige Entschlüsselung für Nachrichten anwenden, die an die IOS-Mail-App übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="d14ff-139">As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app.</span></span> <span data-ttu-id="d14ff-140">Wenn Sie sich für die Verwendung der dienstseitigen Entschlüsselung entscheiden, sendet der Dienst eine entschlüsselte Kopie der Nachricht an das IOS-Gerät.</span><span class="sxs-lookup"><span data-stu-id="d14ff-140">When you choose to do use service-side decryption, the service sends a decrypted copy of the message to the iOS device.</span></span> <span data-ttu-id="d14ff-141">Auf dem Clientgerät wird eine entschlüsselte Kopie der Nachricht gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d14ff-141">The client device stores a decrypted copy of the message.</span></span> <span data-ttu-id="d14ff-142">Die Nachricht behält auch Informationen zu Nutzungsrechten, obwohl die IOS-Mail-App keine clientseitigen Nutzungsrechte für den Benutzer anwendet.</span><span class="sxs-lookup"><span data-stu-id="d14ff-142">The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="d14ff-143">Der Benutzer kann die Nachricht auch dann kopieren oder drucken, wenn Sie nicht ursprünglich über die Rechte dazu verfügt hat.</span><span class="sxs-lookup"><span data-stu-id="d14ff-143">The user can copy or print the message even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="d14ff-144">Wenn der Benutzer jedoch versucht, eine Aktion abzuschließen, die den Office 365-e-Mail-Server erfordert, wie beispielsweise das Weiterleiten der Nachricht, lässt der Server die Aktion nicht zu, wenn der Benutzer nicht ursprünglich über das Nutzungsrecht für diesen Vorgang verfügt.</span><span class="sxs-lookup"><span data-stu-id="d14ff-144">However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span> <span data-ttu-id="d14ff-145">Endbenutzer können jedoch die Verwendungseinschränkung "nicht weiterleiten" umgehen, indem Sie die Nachricht von einem anderen Konto innerhalb der IOS-Mail-App weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="d14ff-145">However, end users can work around "Do Not Forward" usage restriction by forwarding the message from a different account within the iOS mail app.</span></span> <span data-ttu-id="d14ff-146">Unabhängig davon, ob Sie die dienstseitige Entschlüsselung von e-Mails einrichten, können Anlagen zu verschlüsselten und geschützten e-Mails nicht in der IOS-Mail-App angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d14ff-146">Regardless of whether you set up service-side decryption of mail, attachments to encrypted and rights protected mail can't be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="d14ff-147">Wenn Sie nicht zulassen, dass entschlüsselte Nachrichten an IOS-Mail-App-Benutzer gesendet werden, erhalten Benutzer eine Meldung, die besagt, dass Sie nicht über die Berechtigung zum Anzeigen der Nachricht verfügen.</span><span class="sxs-lookup"><span data-stu-id="d14ff-147">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message.</span></span> <span data-ttu-id="d14ff-148">Die dienstseitige Entschlüsselung von e-Mail-Nachrichten ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d14ff-148">By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="d14ff-149">Weitere Informationen und eine Ansicht der Clientumgebung finden Sie unter Anzeigen von verschlüsselten [Nachrichten auf Ihrem iPhone oder iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="d14ff-149">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="d14ff-150">So verwalten Sie, ob IOS-Mail-App-Benutzer Nachrichten anzeigen können, die von der Office 365-Nachrichtenverschlüsselung geschützt sind</span><span class="sxs-lookup"><span data-stu-id="d14ff-150">To manage whether iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="d14ff-151">Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her.</span><span class="sxs-lookup"><span data-stu-id="d14ff-151">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="d14ff-152">Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="d14ff-152">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="d14ff-153">Führen Sie das Cmdlet Set-ActiveSyncOrganizations mit dem Parameter AllowRMSSupportForUnenlightenedApps aus:</span><span class="sxs-lookup"><span data-stu-id="d14ff-153">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="d14ff-154">So konfigurieren Sie beispielsweise den Dienst zum Entschlüsseln von Nachrichten, bevor Sie an unaufgeklärte apps wie die IOS-Mail-App gesendet werden:</span><span class="sxs-lookup"><span data-stu-id="d14ff-154">For example, to configure the service to decrypt messages before they're sent to unenlightened apps like the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="d14ff-155">Oder, um den Dienst so zu konfigurieren, dass entschlüsselte Nachrichten nicht an unerleuchtete apps gesendet werden:</span><span class="sxs-lookup"><span data-stu-id="d14ff-155">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="d14ff-156">Aktivieren der dienstseitigen Entschlüsselung von e-Mail-Anlagen für Webbrowser-e-Mail-Clients</span><span class="sxs-lookup"><span data-stu-id="d14ff-156">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="d14ff-157">Bei Verwendung der Nachrichtenverschlüsselung von Office 365 werden Anlagen in der Regel automatisch verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="d14ff-157">Normally, when you use Office 365 message encryption, attachments are automatically encrypted.</span></span> <span data-ttu-id="d14ff-158">Als Office 365-Administrator können Sie die dienstseitige Entschlüsselung für e-Mail-Anhänge anwenden, die Benutzer über einen Webbrowser herunterladen.</span><span class="sxs-lookup"><span data-stu-id="d14ff-158">As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="d14ff-159">Wenn Sie die dienstseitige Entschlüsselung verwenden, sendet der Dienst eine entschlüsselte Kopie der Datei an das Gerät.</span><span class="sxs-lookup"><span data-stu-id="d14ff-159">When you use service-side decryption, the service sends a decrypted copy of the file to the device.</span></span> <span data-ttu-id="d14ff-160">Die Nachricht ist weiterhin verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="d14ff-160">The message is still encrypted.</span></span> <span data-ttu-id="d14ff-161">Die e-Mail-Anlage speichert auch Informationen zu Nutzungsrechten, obwohl der Browserclient seitige Nutzungsrechte nicht auf den Benutzer angewendet hat.</span><span class="sxs-lookup"><span data-stu-id="d14ff-161">The email attachment also keeps information about usage rights even though the browser doesn't apply client-side usage rights to the user.</span></span> <span data-ttu-id="d14ff-162">Der Benutzer kann die e-Mail-Anlage auch dann kopieren oder ausdrucken, wenn Sie nicht ursprünglich über die Rechte dazu verfügt hat.</span><span class="sxs-lookup"><span data-stu-id="d14ff-162">The user can copy or print the email attachment even if they didn't originally have the rights to do so.</span></span> <span data-ttu-id="d14ff-163">Wenn der Benutzer jedoch versucht, eine Aktion abzuschließen, die den Office 365-e-Mail-Server erfordert, wie beispielsweise das Weiterleiten der Anlage, lässt der Server die Aktion nicht zu, wenn der Benutzer ursprünglich nicht über das Nutzungsrecht verfügt hat.</span><span class="sxs-lookup"><span data-stu-id="d14ff-163">However, if the user tries to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server won't permit the action if the user didn't originally have the usage right to do so.</span></span>
  
<span data-ttu-id="d14ff-164">Unabhängig davon, ob Sie die dienstseitige Entschlüsselung von Anlagen einrichten, können Benutzer keine Anlagen zu verschlüsselten und geschützten e-Mails in der IOS-Mail-App anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d14ff-164">Regardless of whether you set up service-side decryption of attachments, users can't view any attachments to encrypted and rights protected mail in the iOS mail app.</span></span>
  
<span data-ttu-id="d14ff-165">Wenn Sie nicht die standardmäßige verschlüsselte e-Mail-Anlagen zulassen, erhalten Benutzer eine Meldung, die besagt, dass Sie nicht über die Berechtigung zum Anzeigen der Anlage verfügen.</span><span class="sxs-lookup"><span data-stu-id="d14ff-165">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="d14ff-166">Weitere Informationen dazu, wie Office 365 die Verschlüsselung von e-Mails und e-Mail-Anlagen mit der Option nur-Verschlüsselung implementiert, finden Sie unter [Encrypt-only Option for Emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="d14ff-166">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="d14ff-167">So verwalten Sie, ob e-Mail-Anhänge beim Herunterladen aus einem Webbrowser entschlüsselt werden</span><span class="sxs-lookup"><span data-stu-id="d14ff-167">To manage whether email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="d14ff-168">Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her.</span><span class="sxs-lookup"><span data-stu-id="d14ff-168">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="d14ff-169">Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="d14ff-169">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="d14ff-170">Führen Sie das Cmdlet Set-IRMConfiguration mit dem Parameter DecryptAttachmentFromPortal aus:</span><span class="sxs-lookup"><span data-stu-id="d14ff-170">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   <span data-ttu-id="d14ff-171">Beispielsweise können Sie den Dienst so konfigurieren, dass e-Mail-Anlagen entschlüsselt werden, wenn ein Benutzer Sie von einem Webbrowser herunterlädt:</span><span class="sxs-lookup"><span data-stu-id="d14ff-171">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   <span data-ttu-id="d14ff-172">So konfigurieren Sie den Dienst so, dass verschlüsselte e-Mail-Anlagen beim Herunterladen hinterlassen werden:</span><span class="sxs-lookup"><span data-stu-id="d14ff-172">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="ensure-all-external-recipients-use-the-ome-portal-to-read-encrypted-mail--office-365-advanced-message-encryption-only"></a><span data-ttu-id="d14ff-173">Sicherstellen, dass alle externen Empfänger das OM-Portal verwenden, um verschlüsselte e-Mails zu lesen – nur Office 365 erweiterte Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d14ff-173">Ensure all external recipients use the OME Portal to read encrypted mail — Office 365 Advanced Message Encryption only</span></span>

<span data-ttu-id="d14ff-174">Wenn Sie über die erweiterte Nachrichtenverschlüsselung von Office 365 verfügen, können Sie mit benutzerdefinierten Branding-Vorlagen erzwingen, dass Empfänger eine Wrapper-e-Mail erhalten, die Sie zum Lesen verschlüsselter e-Mails im OM-Portal anstelle von Outlook oder Outlook im Web anweist.</span><span class="sxs-lookup"><span data-stu-id="d14ff-174">If you have Office 365 Advanced Message Encryption, you can use custom branding templates to force recipients to receive a wrapper mail that directs them to read encrypted email in the OME Portal instead of using Outlook or Outlook on the web.</span></span> <span data-ttu-id="d14ff-175">Möglicherweise möchten Sie dies tun, wenn Sie mehr Kontrolle darüber haben möchten, wie Empfänger die empfangene e-Mail verwenden.</span><span class="sxs-lookup"><span data-stu-id="d14ff-175">You might want to do this if you use want greater control over how recipients use the mail they receive.</span></span> <span data-ttu-id="d14ff-176">Wenn externe Empfänger beispielsweise e-Mails im Webportal anzeigen, können Sie ein Ablaufdatum für die e-Mail festlegen und die e-Mail widerrufen.</span><span class="sxs-lookup"><span data-stu-id="d14ff-176">For example, if external recipients view email in the web portal, you can set an expiration date for the email, and you can revoke the email.</span></span> <span data-ttu-id="d14ff-177">Diese Funktionen werden nur über das OM-Portal unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d14ff-177">These features are only supported through the OME Portal.</span></span> <span data-ttu-id="d14ff-178">Sie können die Option Verschlüsseln und die Option nicht weiterleiten beim Erstellen der Nachrichtenfluss Regeln verwenden.</span><span class="sxs-lookup"><span data-stu-id="d14ff-178">You can use the Encrypt option and the Do Not Forward option when creating the mail flow rules.</span></span>

### <a name="create-a-custom-template-to-force-all-external-recipients-to-use-the-ome-portal-and-for-encrypted-email-to-be-revocable-and-expire-in-7-days"></a><span data-ttu-id="d14ff-179">Erstellen Sie eine benutzerdefinierte Vorlage, um zu erzwingen, dass alle externen Empfänger das OM-Portal verwenden und dass verschlüsselte e-Mails widerruflich und innerhalb von 7 Tagen ablaufen.</span><span class="sxs-lookup"><span data-stu-id="d14ff-179">Create a custom template to force all external recipients to use the OME Portal and for encrypted email to be revocable and expire in 7 days</span></span>

1. <span data-ttu-id="d14ff-180">Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her.</span><span class="sxs-lookup"><span data-stu-id="d14ff-180">Use a work or school account that has global administrator permissions in your Office 365 organization and start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="d14ff-181">Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="d14ff-181">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="d14ff-182">Führen Sie das Cmdlet New-OMEConfiguration aus:</span><span class="sxs-lookup"><span data-stu-id="d14ff-182">Run the New-OMEConfiguration cmdlet:</span></span>

   ```powershell
   New-OMEConfiguration -Identity "<template name>" -ExternalMailExpiryInDays 7
   ```

   <span data-ttu-id="d14ff-183">Hierbei `template name` ist der Name, den Sie für die benutzerdefinierte Branding-Vorlage Office 365 Message Encryption verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="d14ff-183">where `template name` is the name you want to use for the Office 365 Message Encryption custom branding template.</span></span> <span data-ttu-id="d14ff-184">For example,</span><span class="sxs-lookup"><span data-stu-id="d14ff-184">For example,</span></span>

   ```powershell
   New-OMEConfiguration -Identity "<One week expiration>" -ExternalMailExpiryInDays 7
   ```

3. <span data-ttu-id="d14ff-185">Führen Sie das Cmdlet New-TransportRule aus:</span><span class="sxs-lookup"><span data-stu-id="d14ff-185">Run the New-TransportRule cmdlet:</span></span>

   ```powershell
   New-TransportRule -name "<mail flow rule name>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "<option name>" -ApplyRightsProtectionCustomizationTemplate "<template name>"
   ```

    <span data-ttu-id="d14ff-186">Dabei gilt:</span><span class="sxs-lookup"><span data-stu-id="d14ff-186">where:</span></span>

   - <span data-ttu-id="d14ff-187">`mail flow rule name`ist der Name, der für die neue Nachrichtenfluss Regel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d14ff-187">`mail flow rule name` is the name you want to use for the new mail flow rule.</span></span>

   - <span data-ttu-id="d14ff-188">`option name`ist entweder `Encrypt` oder `Do Not Forward`.</span><span class="sxs-lookup"><span data-stu-id="d14ff-188">`option name` is either `Encrypt` or `Do Not Forward`.</span></span>

   - <span data-ttu-id="d14ff-189">`template name`ist der Name, den Sie zum Beispiel `One week expiration`der benutzerdefinierten Branding-Vorlage erteilt haben.</span><span class="sxs-lookup"><span data-stu-id="d14ff-189">`template name` is the name you gave the custom branding template, for example `One week expiration`.</span></span>

   <span data-ttu-id="d14ff-190">Zum Verschlüsseln aller externen e-Mails mit der Vorlage "One Week Ablauf" und Anwenden der nur-Verschlüsselung-Option:</span><span class="sxs-lookup"><span data-stu-id="d14ff-190">To encrypt all external email with the "One week expiration" template and apply the Encrypt-Only option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Encrypt" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

   <span data-ttu-id="d14ff-191">So verschlüsseln Sie alle externen e-Mails mit der Vorlage "ein Wochenablauf" und wenden die Option "nicht weiterleiten" an:</span><span class="sxs-lookup"><span data-stu-id="d14ff-191">To encrypt all external email with the "One week expiration" template and apply the Do Not Forward option:</span></span>

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Do Not Forward" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

## <a name="customize-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="d14ff-192">Anpassen der Darstellung von e-Mail-Nachrichten und des OM-Portals</span><span class="sxs-lookup"><span data-stu-id="d14ff-192">Customize the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="d14ff-193">Ausführliche Informationen dazu, wie Sie OM für Ihre Organisation anpassen können, finden Sie unter [Hinzufügen der Marke Ihrer Organisation zu ihren verschlüsselten Nachrichten](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="d14ff-193">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disable-the-new-capabilities-for-ome"></a><span data-ttu-id="d14ff-194">Deaktivieren der neuen Funktionen für OM</span><span class="sxs-lookup"><span data-stu-id="d14ff-194">Disable the new capabilities for OME</span></span>

<span data-ttu-id="d14ff-195">Wir hoffen, dass dies nicht der Fall ist, aber wenn Sie es benötigen, ist es sehr einfach, die neuen Funktionen für OM zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d14ff-195">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward.</span></span> <span data-ttu-id="d14ff-196">Zunächst müssen Sie alle von Ihnen erstellten Nachrichtenfluss Regeln entfernen, die die neuen OM-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="d14ff-196">First, you'll need to remove any mail flow rules you've created that use the new OME capabilities.</span></span> <span data-ttu-id="d14ff-197">Informationen zum Entfernen von Nachrichtenfluss Regeln finden Sie unter [Manage Mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d14ff-197">For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx).</span></span> <span data-ttu-id="d14ff-198">Führen Sie diese Schritte dann in Exchange Online PowerShell aus.</span><span class="sxs-lookup"><span data-stu-id="d14ff-198">Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="d14ff-199">So deaktivieren Sie die neuen Funktionen für OM</span><span class="sxs-lookup"><span data-stu-id="d14ff-199">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="d14ff-200">Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden.</span><span class="sxs-lookup"><span data-stu-id="d14ff-200">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online.</span></span> <span data-ttu-id="d14ff-201">Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="d14ff-201">For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="d14ff-202">Wenn Sie die Schaltfläche **schützen** in Outlook im Web aktiviert haben, deaktivieren Sie Sie, indem Sie das Cmdlet Set-IRMConfiguration mit dem Parameter SimplifiedClientAccessEnabled ausführen.</span><span class="sxs-lookup"><span data-stu-id="d14ff-202">If you enabled the **Protect** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter.</span></span> <span data-ttu-id="d14ff-203">Überspringen Sie andernfalls diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="d14ff-203">Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="d14ff-204">Deaktivieren Sie die neuen Funktionen für OM, indem Sie das Cmdlet Set-IRMConfiguration ausführen, wobei der Parameter AzureRMSLicensingEnabled auf false festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="d14ff-204">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
