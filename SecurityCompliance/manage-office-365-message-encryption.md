---
title: Verwalten der Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
description: Nachdem Sie die Einrichtung von Office 365-Nachrichtenverschlüsselung (OM) abgeschlossen haben, können Sie die Konfiguration Ihrer Bereitstellung auf verschiedene Arten anpassen. Sie können beispielsweise konfigurieren, ob einmalige Code-Codes aktiviert werden sollen, die Schaltfläche schützen in Outlook im Web und vieles mehr angezeigt werden soll. In den Aufgaben in diesem Artikel wird beschrieben, wie.
ms.openlocfilehash: 8b044898efb1ef86790773cd3f8e8061523b0ec0
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213755"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="6f1d2-105">Verwalten der Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="6f1d2-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="6f1d2-p102">Nachdem Sie die Einrichtung von Office 365-Nachrichtenverschlüsselung (OM) abgeschlossen haben, können Sie die Konfiguration Ihrer Bereitstellung auf verschiedene Arten anpassen. Sie können beispielsweise konfigurieren, ob einmalige Code-Codes aktiviert werden sollen, die Schaltfläche **schützen** in Outlook im Web und vieles mehr angezeigt werden soll. In den Aufgaben in diesem Artikel wird beschrieben, wie.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p102">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways. For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more. The tasks in this article describe how.</span></span>
  
||
|:-----|
|<span data-ttu-id="6f1d2-p103">Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and ITPros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
||

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="6f1d2-112">Verwalten der Empfänger von Google-, Yahoo-und Microsoft-Konten zum Anmelden beim Office 365-Nachrichten Verschlüsselungs Portal</span><span class="sxs-lookup"><span data-stu-id="6f1d2-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="6f1d2-p104">Wenn Sie die neuen Office 365-Nachrichten Verschlüsselungsfunktionen einrichten, können Benutzer in Ihrer Organisation standardmäßig Nachrichten an Empfänger senden, die sich außerhalb Ihrer Office 365-Organisation befinden. Wenn der Empfänger eine *soziale ID* wie ein Google-Konto, ein Yahoo-Konto oder ein Microsoft-Konto verwendet, kann der Empfänger sich über die soziale ID beim OM-Portal anmelden. Wenn Sie möchten, können Sie festlegen, dass Empfänger keine sozialen IDs verwenden dürfen, um sich beim OM-Portal anzumelden.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p104">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization. If the recipient uses a *social ID* such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID. If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a><span data-ttu-id="6f1d2-116">So verwalten Sie, ob Empfängern die Verwendung sozialer IDs für die Anmeldung beim OM-Portal erlaubt ist</span><span class="sxs-lookup"><span data-stu-id="6f1d2-116">To manage whether or not to allow recipients to use social IDs to sign in to the OME portal</span></span>
  
1. <span data-ttu-id="6f1d2-117">[Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="6f1d2-117">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>

2. <span data-ttu-id="6f1d2-118">Führen Sie das Cmdlet Set-OMEConfiguration mit dem Parameter SocialIdSignIn wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-118">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
   ```

   <span data-ttu-id="6f1d2-119">Um beispielsweise soziale IDs zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-119">For example, to disable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   <span data-ttu-id="6f1d2-120">So aktivieren Sie soziale IDs:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-120">To enable social IDs:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="6f1d2-121">Verwalten der Verwendung von einmaligen Passthrough-Codes für die Anmeldung beim Office 365-Nachrichten Verschlüsselungs Portal</span><span class="sxs-lookup"><span data-stu-id="6f1d2-121">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>

<span data-ttu-id="6f1d2-p105">Wenn der Empfänger einer Nachricht, die von OM verschlüsselt wird, nicht Outlook verwendet, erhält der Empfänger in der Standardeinstellung einen Link zur zeitlich begrenzten Webansicht, über die er die Nachricht lesen kann. Hierzu gehört ein einmaliger Code. Als Administrator können Sie verwalten, ob einmalige Durchlaufcodes zum Anmelden am OM-Portal verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p105">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message. This includes a one-time pass code. As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a><span data-ttu-id="6f1d2-125">So verwalten Sie, ob einmalige Durchlaufcodes für OM generiert werden</span><span class="sxs-lookup"><span data-stu-id="6f1d2-125">To manage whether or not one-time pass codes are generated for OME</span></span>
  
1. <span data-ttu-id="6f1d2-p106">Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p106">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="6f1d2-128">Führen Sie das Cmdlet Set-OMEConfiguration mit dem Parameter OTPEnabled aus:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-128">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   <span data-ttu-id="6f1d2-129">So können Sie beispielsweise einmalige Durchlaufcodes deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-129">For example, to disable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   <span data-ttu-id="6f1d2-130">So aktivieren Sie einmalige Code-Codes:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-130">To enable one-time pass codes:</span></span>

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="6f1d2-131">Verwalten der Anzeige der Schaltfläche "schützen" in Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="6f1d2-131">Managing the display of the Protect button in Outlook on the web</span></span>

<span data-ttu-id="6f1d2-p107">Standardmäßig ist die Schaltfläche **schützen** in Outlook im Web nicht aktiviert, wenn Sie OM einrichten. Als Administrator können Sie verwalten, ob diese Schaltfläche Endbenutzern angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p107">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME. As an administrator, you can manage whether or not to display this button to end users.</span></span>
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a><span data-ttu-id="6f1d2-134">So verwalten Sie, ob die Schaltfläche schützen in Outlook im Web angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="6f1d2-134">To manage whether or not the Protect button appears in Outlook on the web</span></span>
  
1. <span data-ttu-id="6f1d2-p108">Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p108">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="6f1d2-137">Führen Sie das Cmdlet Set-IRMConfiguration mit dem-SimplifiedClientAccessEnabled-Parameter aus:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-137">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   <span data-ttu-id="6f1d2-138">Um beispielsweise die Schaltfläche **Protect** zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-138">For example, to disable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   <span data-ttu-id="6f1d2-139">So aktivieren Sie die Schaltfläche " **schützen** "</span><span class="sxs-lookup"><span data-stu-id="6f1d2-139">To enable the **Protect** button:</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="6f1d2-140">Aktivieren der dienstseitigen Entschlüsselung von e-Mail-Nachrichten für iOS-Mail-App-Benutzer</span><span class="sxs-lookup"><span data-stu-id="6f1d2-140">Enable service-side decryption of email messages for iOS mail app users</span></span>

<span data-ttu-id="6f1d2-p109">Die iOS-Mail-App kann nicht mit der Office 365-Nachrichtenverschlüsselung geschützte Nachrichten entschlüsseln. Als Office 365-Administrator können Sie die dienstseitige Entschlüsselung für Nachrichten anwenden, die an die iOS-Mail-App übermittelt werden. Wenn Sie dies tun, sendet der Dienst eine entschlüsselte Kopie der Nachricht an das iOS-Gerät. Die Nachricht wird auf dem Clientgerät entschlüsselt gespeichert. Die Nachricht behält auch Informationen zu Nutzungsrechten, obwohl die iOS-Mail-App keine clientseitigen Nutzungsrechte für den Benutzer anwendet. Dies führt dazu, dass der Benutzer die Nachricht kopieren oder drucken kann, auch wenn Sie nicht ursprünglich über die Rechte dazu verfügt hat. Wenn der Benutzer jedoch versucht, eine Aktion abzuschließen, die den Office 365-e-Mail-Server erfordert, wie beispielsweise die Weiterleitung der Nachricht, lässt der Server die Aktion nicht zu, wenn der Benutzer ursprünglich nicht über das Nutzungsrecht für diesen Vorgang verfügt. Endbenutzer können jedoch keine Nutzungseinschränkung weiterleiten, indem Sie die Nachricht von einem anderen Konto in ihrer iOS-Mail-App weiterleiten. unabhängig davon, ob Sie die dienstseitige Entschlüsselung von e-Mails, Anhänge zu verschlüsselten und geschützten e-Mails kann nicht in der iOS-Mail-App angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p109">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption. As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app. When you choose to do this, the service sends a decrypted copy of the message to the iOS device. The message is stored decrypted on the client device. The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user. This means that the user can copy or print the message even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so. However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app. Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="6f1d2-p110">Wenn Sie nicht zulassen, dass entschlüsselte Nachrichten an iOS-Mail-App-Benutzer gesendet werden, erhalten Benutzer eine Meldung, die besagt, dass Sie nicht über die Berechtigung zum Anzeigen der Nachricht verfügen. Die dienstseitige Entschlüsselung von e-Mail-Nachrichten ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p110">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message. By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="6f1d2-152">Weitere Informationen und eine Ansicht der Clientumgebung finden Sie unter Anzeigen von verschlüsselten [Nachrichten auf Ihrem iPhone oder iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="6f1d2-152">For more information, and for a view of the client experience, see [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a><span data-ttu-id="6f1d2-153">So verwalten Sie, ob iOS-Mail-App-Benutzer Nachrichten anzeigen können, die von der Office 365-Nachrichtenverschlüsselung geschützt sind</span><span class="sxs-lookup"><span data-stu-id="6f1d2-153">To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption</span></span>
  
1. <span data-ttu-id="6f1d2-p111">Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p111">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="6f1d2-156">Führen Sie das Cmdlet Set-ActiveSyncOrganizations mit dem Parameter AllowRMSSupportForUnenlightenedApps aus:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-156">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   <span data-ttu-id="6f1d2-157">So konfigurieren Sie beispielsweise den Dienst zum Entschlüsseln von Nachrichten, bevor Sie an unaufgeklärte apps wie die iOS-Mail-App gesendet werden:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-157">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   <span data-ttu-id="6f1d2-158">Oder, um den Dienst so zu konfigurieren, dass entschlüsselte Nachrichten nicht an unerleuchtete apps gesendet werden:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-158">Or, to configure the service not to send decrypted messages to unenlightened apps:</span></span>

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="6f1d2-159">Aktivieren der dienstseitigen Entschlüsselung von e-Mail-Anlagen für Webbrowser-e-Mail-Clients</span><span class="sxs-lookup"><span data-stu-id="6f1d2-159">Enable service-side decryption of email attachments for web browser mail clients</span></span>

<span data-ttu-id="6f1d2-p112">Bei Verwendung der Nachrichtenverschlüsselung von Office 365 werden Anlagen in der Regel automatisch verschlüsselt. Als Office 365-Administrator können Sie die dienstseitige Entschlüsselung für e-Mail-Anhänge anwenden, die Benutzer über einen Webbrowser herunterladen.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p112">Normally, when you use Office 365 message encryption, attachments are automatically encrypted. As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span>
  
<span data-ttu-id="6f1d2-p113">Wenn Sie dies tun, sendet der Dienst eine entschlüsselte Kopie der Datei an das Gerät. Die Nachricht ist weiterhin verschlüsselt. Die e-Mail-Anlage behält auch Informationen zu Nutzungsrechten, obwohl der Browserclient seitigen Nutzungsrechten für den Benutzer nicht zutrifft. Dies führt dazu, dass der Benutzer die e-Mail-Anlage auch dann kopieren oder ausdrucken kann, wenn er ursprünglich nicht über die Rechte dazu verfügt. Wenn der Benutzer jedoch versucht, eine Aktion abzuschließen, die den Office 365-e-Mail-Server erfordert, wie beispielsweise das Weiterleiten der Anlage, lässt der Server die Aktion nicht zu, wenn der Benutzer ursprünglich nicht über das Nutzungsrecht für diesen Vorgang verfügt.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p113">When you choose to do this, the service sends a decrypted copy of the file to the device. The message is still encrypted. The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user. This means that the user can copy or print the email attachment even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="6f1d2-167">Unabhängig davon, ob Sie die dienstseitige Entschlüsselung von Anlagen einrichten, können Anhänge zu verschlüsselten und geschützten e-Mails nicht in der iOS-Mail-App angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-167">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="6f1d2-168">Wenn Sie nicht die standardmäßige verschlüsselte e-Mail-Anlagen zulassen, erhalten Benutzer eine Meldung, die besagt, dass Sie nicht über die Berechtigung zum Anzeigen der Anlage verfügen.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-168">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment.</span></span>
  
<span data-ttu-id="6f1d2-169">Weitere Informationen dazu, wie Office 365 die Verschlüsselung von e-Mails und e-Mail-Anlagen mit der Option nur-Verschlüsselung implementiert, finden Sie unter [Encrypt-only Option for Emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="6f1d2-169">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a><span data-ttu-id="6f1d2-170">So verwalten Sie, ob e-Mail-Anhänge beim Herunterladen aus einem Webbrowser entschlüsselt werden</span><span class="sxs-lookup"><span data-stu-id="6f1d2-170">To manage whether or not email attachments are decrypted on download from a web browser</span></span>
  
1. <span data-ttu-id="6f1d2-p114">Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p114">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="6f1d2-173">Führen Sie das Cmdlet Set-IRMConfiguration mit dem Parameter DecryptAttachmentFromPortal aus:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-173">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   <span data-ttu-id="6f1d2-174">Beispielsweise können Sie den Dienst so konfigurieren, dass e-Mail-Anlagen entschlüsselt werden, wenn ein Benutzer Sie von einem Webbrowser herunterlädt:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-174">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   <span data-ttu-id="6f1d2-175">So konfigurieren Sie den Dienst so, dass verschlüsselte e-Mail-Anlagen beim Herunterladen hinterlassen werden:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-175">To configure the service to leave encrypted email attachments as they are upon download:</span></span>

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="6f1d2-176">Anpassen der Darstellung von e-Mail-Nachrichten und des OM-Portals</span><span class="sxs-lookup"><span data-stu-id="6f1d2-176">Customizing the appearance of email messages and the OME portal</span></span>

<span data-ttu-id="6f1d2-177">Ausführliche Informationen dazu, wie Sie OM für Ihre Organisation anpassen können, finden Sie unter [Hinzufügen der Marke Ihrer Organisation zu ihren verschlüsselten Nachrichten](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="6f1d2-177">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="6f1d2-178">Deaktivieren der neuen Funktionen für OM</span><span class="sxs-lookup"><span data-stu-id="6f1d2-178">Disabling the new capabilities for OME</span></span>

<span data-ttu-id="6f1d2-p115">Wir hoffen, dass dies nicht der Fall ist, aber wenn Sie es benötigen, ist es sehr einfach, die neuen Funktionen für OM zu deaktivieren. Zunächst müssen Sie alle von Ihnen erstellten Nachrichtenfluss Regeln entfernen, die die neuen OM-Funktionen verwenden. Informationen zum Entfernen von Nachrichtenfluss Regeln finden Sie unter [Manage Mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Führen Sie diese Schritte dann in Exchange Online PowerShell aus.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p115">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward. First, you'll need to remove any mail flow rules you've created that use the new OME capabilities. For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Then, complete these steps in Exchange Online PowerShell.</span></span>
  
### <a name="to-disable-the-new-capabilities-for-ome"></a><span data-ttu-id="6f1d2-183">So deaktivieren Sie die neuen Funktionen für OM</span><span class="sxs-lookup"><span data-stu-id="6f1d2-183">To disable the new capabilities for OME</span></span>
  
1. <span data-ttu-id="6f1d2-p116">Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p116">Using a work or school account that has global administrator permissions in your Office 365 organization, start a Windows PowerShell session and connect to Exchange Online. For instructions, see [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).</span></span>

2. <span data-ttu-id="6f1d2-p117">Wenn Sie die Schaltfläche **schützen** in Outlook im Web aktiviert haben, deaktivieren Sie Sie, indem Sie das Cmdlet Set-IRMConfiguration mit dem Parameter SimplifiedClientAccessEnabled ausführen. Überspringen Sie andernfalls diesen Schritt.</span><span class="sxs-lookup"><span data-stu-id="6f1d2-p117">If you enabled the **Protect** button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter. Otherwise, skip this step.</span></span>

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. <span data-ttu-id="6f1d2-188">Deaktivieren Sie die neuen Funktionen für OM, indem Sie das Cmdlet Set-IRMConfiguration ausführen, wobei der Parameter AzureRMSLicensingEnabled auf false festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="6f1d2-188">Disable the new capabilities for OME by running the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter set to false:</span></span>

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
