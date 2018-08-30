---
title: Verwalten von Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 09f6737e-f03f-4bc8-8281-e46d24ee2a74
description: Nachdem Sie die Einstellung von Office 365 Message Encryption (OME) abgeschlossen haben, können Sie die Konfiguration Ihrer Bereitstellung auf unterschiedliche Weise anpassen. Beispielsweise können Sie konfigurieren, ob aktivieren einmalige Kenncodes verlangt, schützen die Schaltfläche in Outlook auf den Web- und vieles mehr angezeigt. Die Aufgaben in diesem Artikel wird beschrieben, wie.
ms.openlocfilehash: ddc86bdf0d0ce5480587862a4ed438b6c138987f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529189"
---
# <a name="manage-office-365-message-encryption"></a><span data-ttu-id="d74f1-105">Verwalten von Office 365-Nachrichtenverschlüsselung</span><span class="sxs-lookup"><span data-stu-id="d74f1-105">Manage Office 365 Message Encryption</span></span>

<span data-ttu-id="d74f1-p102">Nachdem Sie die Einstellung von Office 365 Message Encryption (OME) abgeschlossen haben, können Sie die Konfiguration Ihrer Bereitstellung auf unterschiedliche Weise anpassen. Beispielsweise können Sie konfigurieren, ob aktivieren einmalige Kenncodes verlangt, **schützen** die Schaltfläche in Outlook auf den Web- und vieles mehr angezeigt. Die Aufgaben in diesem Artikel wird beschrieben, wie.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p102">Once you've finished setting up Office 365 Message Encryption (OME), you can customize the configuration of your deployment in a number of ways. For example, you can configure whether to enable one-time pass codes, display the **Protect** button in Outlook on the web, and more. The tasks in this article describe how.</span></span> 
  
||
|:-----|
|<span data-ttu-id="d74f1-p103">Dieser Artikel ist Teil einer größeren Reihe von Artikeln zur Office 365 Message Encryption. In diesem Artikel ist für Administratoren und IT-Spezialisten vorgesehen. Wenn Sie sich gerade befinden Suchen nach Informationen zu senden oder Empfangen einer verschlüsselten Nachricht, finden Sie in der Liste der Artikel in [Office 365 Message Encryption (OME)](ome.md) , und suchen Sie im Artikel, der am besten Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p103">This article is part of a larger series of articles about Office 365 Message Encryption. This article is intended for administrators and IT Pros. If you're just looking for information on sending or receiving an encrypted message, see the list of articles in [Office 365 Message Encryption (OME)](ome.md) and locate the article that best fits your needs.</span></span> |
   
## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="d74f1-112">Verwalten von, ob Google, Yahoo! und Microsoft Account Empfänger diese Konten, zur Anmeldung verwenden können bei Office 365 Message Encryption-portal</span><span class="sxs-lookup"><span data-stu-id="d74f1-112">Managing whether Google, Yahoo, and Microsoft Account recipients can use these accounts to sign in to the Office 365 Message Encryption portal</span></span>
<span data-ttu-id="d74f1-113"><a name="PermitSocialID"> </a></span><span class="sxs-lookup"><span data-stu-id="d74f1-113"></span></span>

<span data-ttu-id="d74f1-p104">Standardmäßig Wenn Sie die neuen Funktionen für Office 365 Message Encryption einrichten können Benutzer in Ihrer Organisation Nachrichten an Empfänger senden, die sich außerhalb Ihrer Office 365-Organisation befinden. Wenn der Empfänger eine *ID für soziale Netzwerke* wie Google-Konto, Yahoo-Konto oder Microsoft-Konto verwendet wird, kann der Empfänger OME-Portal mit der sozialen-ID. anmelden Wenn Sie möchten, können Sie auswählen, die nicht für soziale Netzwerke IDs verwenden Sie zur Anmeldung bei des OME-Portals-Empfänger zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p104">By default, when you set up the new Office 365 Message Encryption capabilities, users in your organization can send messages to recipients that are outside of your Office 365 organization. If the recipient uses a  *social ID*  such as a Google account, Yahoo account, or Microsoft account, the recipient can sign in to the OME portal using the social ID. If you want, you can choose not to allow recipients to use social IDs to sign in to the OME portal.</span></span> 
  
 <span data-ttu-id="d74f1-117">**Ob Sie Empfänger für soziale Netzwerke IDs OME-Portal Anmeldung verwenden darf verwalten**</span><span class="sxs-lookup"><span data-stu-id="d74f1-117">**To manage whether or not to allow recipients to use social IDs to sign in to the OME portal**</span></span>
  
1. <span data-ttu-id="d74f1-118">[Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d74f1-118">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="d74f1-119">Führen Sie das Cmdlet "Set-OMEConfiguration" mit dem Parameter SocialIdSignIn wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d74f1-119">Run the Set-OMEConfiguration cmdlet with the SocialIdSignIn parameter as follows:</span></span>
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true |$false >
  ```

    <span data-ttu-id="d74f1-120">Geben Sie beispielsweise Folgendes ein, um die IDs für soziale Netzwerke deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="d74f1-120">For example, to disable social IDs:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
  ```

    <span data-ttu-id="d74f1-121">So aktivieren Sie IDs für soziale Netzwerke</span><span class="sxs-lookup"><span data-stu-id="d74f1-121">To enable social IDs:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
  ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a><span data-ttu-id="d74f1-122">Die Verwendung der einmaligen Kenncodes zum Anmelden bei Office 365 Message Encryption-Portal verwalten</span><span class="sxs-lookup"><span data-stu-id="d74f1-122">Managing the use of one-time pass codes for signing in to the Office 365 Message Encryption portal</span></span>
<span data-ttu-id="d74f1-123"><a name="GenerateOTPC"> </a></span><span class="sxs-lookup"><span data-stu-id="d74f1-123"></span></span>

<span data-ttu-id="d74f1-p105">Wenn der Empfänger einer Nachricht verschlüsselt, OME Outlook, unabhängig von der durch den Empfänger verwendete Konto nicht verwendet, erhält der Empfänger eine zeitlich beschränkte Webansicht Verknüpfung, die Sie die Nachricht lesen können. Dies umfasst eine einmalige Kennung. Als Administrator können Sie verwalten, ob Kenncodes einmalige Anmelden OME-Portal verwendet werden können oder nicht.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p105">By default, if the recipient of a message encrypted by OME doesn't use Outlook, regardless of the account used by the recipient, the recipient receives a limited-time web-view link that lets them read the message. This includes a one-time pass code. As an administrator, you can manage whether or not one-time pass codes can be used to sign-in to the OME portal.</span></span>
  
 <span data-ttu-id="d74f1-127">**Verwalten, unabhängig davon, ob eine einmalige Kenncodes für OME generiert werden**</span><span class="sxs-lookup"><span data-stu-id="d74f1-127">**To manage whether or not one-time pass codes are generated for OME**</span></span>
  
1. <span data-ttu-id="d74f1-128">[Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d74f1-128">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="d74f1-129">Führen Sie das Cmdlet "Set-OMEConfiguration" mit dem Parameter OTPEnabled wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d74f1-129">Run the Set-OMEConfiguration cmdlet with the OTPEnabled parameter as follows:</span></span>
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true |$false >
  ```

    <span data-ttu-id="d74f1-130">Geben Sie beispielsweise Folgendes ein, um die einmalige Kenncodes zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="d74f1-130">For example, to disable one-time pass codes:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
  ```

    <span data-ttu-id="d74f1-131">So aktivieren Sie das einmalige Kenncodes verlangt:</span><span class="sxs-lookup"><span data-stu-id="d74f1-131">To enable one-time pass codes:</span></span>
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
  ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a><span data-ttu-id="d74f1-132">Verwaltung der Anzeige der Schaltfläche Protect in Outlook im Web</span><span class="sxs-lookup"><span data-stu-id="d74f1-132">Managing the display of the Protect button in Outlook on the web</span></span>
<span data-ttu-id="d74f1-133"><a name="DisplayProtectButton"> </a></span><span class="sxs-lookup"><span data-stu-id="d74f1-133"></span></span>

<span data-ttu-id="d74f1-p106">Standardmäßig ist die Schaltfläche **Protect** in Outlook im Web nicht aktiviert, wenn Sie OME einrichten. Als Administrator können Sie, ob diese Schaltfläche für Endbenutzer angezeigt werden soll oder nicht verwalten.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p106">By default, the **Protect** button in Outlook on the web is not enabled when you set up OME. As an administrator, you can manage whether or not to display this button to end users.</span></span> 
  
 <span data-ttu-id="d74f1-136">**Zum Verwalten von wird angezeigt, unabhängig davon, ob die Schaltfläche Protect in Outlook im Web**</span><span class="sxs-lookup"><span data-stu-id="d74f1-136">**To manage whether or not the Protect button appears in Outlook on the web**</span></span>
  
1. <span data-ttu-id="d74f1-137">[Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d74f1-137">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="d74f1-138">Führen Sie das Cmdlet Set-IRMConfiguration mit dem Parameter - SimplifiedClientAccessEnabled wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d74f1-138">Run the Set-IRMConfiguration cmdlet with the -SimplifiedClientAccessEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true |$false >
  ```

    <span data-ttu-id="d74f1-139">Geben Sie beispielsweise Folgendes ein, um die Schaltfläche **Protect** zu deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="d74f1-139">For example, to disable the **Protect** button:</span></span> 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

    <span data-ttu-id="d74f1-140">So aktivieren Sie die Schaltfläche **schützen** :</span><span class="sxs-lookup"><span data-stu-id="d74f1-140">To enable the **Protect** button:</span></span> 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
  ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a><span data-ttu-id="d74f1-141">Aktivieren Sie dienstseitige Entschlüsselung von e-Mails für iOS Mail-app-Benutzer</span><span class="sxs-lookup"><span data-stu-id="d74f1-141">Enable service-side decryption of email messages for iOS mail app users</span></span>
<span data-ttu-id="d74f1-142"><a name="EnableServiceSideDecrypt"> </a></span><span class="sxs-lookup"><span data-stu-id="d74f1-142"></span></span>

<span data-ttu-id="d74f1-p107">Die Mail-app für iOS kann nicht mit Office 365 Message Encryption geschützten Nachrichten nicht entschlüsseln. Als Office 365-Administrator können Sie dienstseitige Entschlüsselung für Nachrichten an die Mail-app für iOS anwenden. Wenn Sie dazu entschließen, sendet der Dienst eine verschlüsselte Kopie der Nachricht an das Gerät iOS. Die Nachricht wird auf dem Clientgerät entschlüsselt gespeichert. Die Nachricht enthält auch Informationen zu Nutzungsrechte, auch wenn die Mail-app für iOS mithilfe der clientseitigen Nutzungsrechte für den Benutzer nicht zutrifft. Dies bedeutet, dass der Benutzer kann kopieren oder der Nachricht drucken, auch wenn sie ursprünglich nicht über die Rechte dazu verfügt. Jedoch, wenn der Benutzer versucht, eine Aktion ausführen, in der Office 365-Mailserver, z. B. das Weiterleiten der Nachricht erfordert wird der Server nicht die Aktion lassen, wenn der Benutzer nicht ursprünglich Usage dazu berechtigt. Endbenutzer können nicht weiterleiten verwendungseinschränkung durch Weiterleiten der Nachricht von einem anderen Konto in ihrer iOS-Mail-App unabhängig davon, ob Sie dienstseitige Entschlüsselung von e-Mail einrichten umgehen jedoch aller Anlagen verschlüsselt werden, und die Rechte geschützte Nachrichten kann nicht in der Mail-app für iOS angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p107">The iOS mail app can't decrypt messages protected with Office 365 Message Encryption. As an Office 365 administrator, you can apply service-side decryption for messages delivered to the iOS mail app. When you choose to do this, the service sends a decrypted copy of the message to the iOS device. The message is stored decrypted on the client device. The message also retains information about usage rights even though the iOS mail app doesn't apply client-side usage rights to the user. This means that the user can copy or print the message even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the message, the server will not permit the action if the user did not originally have the usage right to do so. However, end-users can work around Do Not Forward usage restriction by forwarding the message from a different account in their iOS mail app. Regardless of whether you set up service-side decryption of mail, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="d74f1-p108">Wenn Sie nicht entschlüsselte Nachrichten gesendet werden können iOS mail-app-Benutzer, Benutzer erhalten die Meldung, die besagt, dass sie nicht über die Rechte zum Anzeigen der Meldung verfügen. Standardmäßig ist die dienstseitige Entschlüsselung der e-Mail-Nachrichten nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p108">If you choose not to allow decrypted messages to be sent to iOS mail app users, users receive a message that states that they don't have the rights to view the message. By default, service-side decryption of email messages is not enabled.</span></span>
  
<span data-ttu-id="d74f1-154">Weitere Informationen und einen Überblick über die Clientumgebung finden Sie im Abschnitt, "[Anzeigen von verschlüsselten Nachrichten auf dem iPhone oder iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)" in [verschlüsselten Nachrichten auf dem iPhone oder iPad anzuzeigen](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span><span class="sxs-lookup"><span data-stu-id="d74f1-154">For more information, and for a view of the client experience, see the section, "[View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)" in [View encrypted messages on your iPhone or iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).</span></span>
  
 <span data-ttu-id="d74f1-155">**Zum Verwalten, unabhängig davon, ob e-Mail von iOS-app-Benutzer kann von Office 365 Message Encryption geschützte Nachrichten anzeigen.**</span><span class="sxs-lookup"><span data-stu-id="d74f1-155">**To manage whether or not iOS mail app users can view messages protected by Office 365 Message Encryption**</span></span>
  
1. <span data-ttu-id="d74f1-156">[Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d74f1-156">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="d74f1-157">Führen Sie das Cmdlet Set-ActiveSyncOrganizations mit dem Parameter AllowRMSSupportForUnenlightenedApps wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d74f1-157">Run the Set-ActiveSyncOrganizations cmdlet with the AllowRMSSupportForUnenlightenedApps parameter as follows:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true |$false >
  ```

    <span data-ttu-id="d74f1-158">Beispiel-mail-so konfigurieren Sie den Dienst, um Nachrichten zu entschlüsseln, bevor sie unenlightened Apps gesendet werden wie iOS app:</span><span class="sxs-lookup"><span data-stu-id="d74f1-158">For example, to configure the service to decrypt messages before they are sent to unenlightened apps such as the iOS mail app:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
  ```

    <span data-ttu-id="d74f1-159">Geben Sie beispielsweise Folgendes ein, um den Dienst nicht zum Senden von entschlüsselter Nachrichten an unenlightened apps zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="d74f1-159">For example, to configure the service not to send decrypted messages to unenlightened apps:</span></span>
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
  ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a><span data-ttu-id="d74f1-160">Aktivieren Sie dienstseitige Entschlüsselung der e-Mail-Anlagen für Webbrowser Mail-clients</span><span class="sxs-lookup"><span data-stu-id="d74f1-160">Enable service-side decryption of email attachments for web browser mail clients</span></span>
<span data-ttu-id="d74f1-161"><a name="EnableServiceSideDecrypt"> </a></span><span class="sxs-lookup"><span data-stu-id="d74f1-161"></span></span>

<span data-ttu-id="d74f1-p109">Wenn Sie Office 365-nachrichtenverschlüsselung verwenden, werden normalerweise automatisch Anlagen verschlüsselt. Als Office 365-Administrator können Sie dienstseitige Entschlüsselung für e-Mail-Anlagen anwenden, die Benutzer über einen Webbrowser herunterladen.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p109">Normally, when you use Office 365 message encryption, attachments are automatically encrypted. As an Office 365 administrator, you can apply service-side decryption for email attachments that users download from a web browser.</span></span> 
  
<span data-ttu-id="d74f1-p110">Wenn Sie dazu entschließen, sendet der Dienst eine verschlüsselte Kopie der Datei auf das Gerät. Die Nachricht wird weiterhin verschlüsselt. Die e-Mail-Anlage behält auch Informationen über die Nutzungsrechte, obwohl im Browser nicht mithilfe der clientseitigen Nutzungsrechte für den Benutzer angewendet werden kann. Dies bedeutet, dass der Benutzer kann kopieren oder die e-Mail-Anlage drucken, selbst wenn sie ursprünglich nicht über die Rechte dazu verfügt. Jedoch, wenn der Benutzer versucht, eine Aktion ausführen, in der Office 365-Mailserver, wie die Anlage weiterleiten erfordert der Server die Aktion lässt, wenn der Benutzer nicht ursprünglich Usage dazu berechtigt.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p110">When you choose to do this, the service sends a decrypted copy of the file to the device. The message is still encrypted. The email attachment also retains information about usage rights even though the browser does not apply client-side usage rights to the user. This means that the user can copy or print the email attachment even if they did not originally have the rights to do so. However, if the user attempts to complete an action that requires the Office 365 mail server, such as forwarding the attachment, the server will not permit the action if the user did not originally have the usage right to do so.</span></span>
  
<span data-ttu-id="d74f1-169">Unabhängig davon, ob Sie dienstseitige Entschlüsselung von Anlagen eingerichtet alle Anhänge verschlüsselt und Rechte geschützte e-Mail nicht in der Mail-app für iOS angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d74f1-169">Regardless of whether you set up service-side decryption of attachments, any attachments to encrypted and rights protected mail cannot be viewed in the iOS mail app.</span></span>
  
<span data-ttu-id="d74f1-p111">Wenn Sie nicht zulassen entschlüsselten e-Mail-Anlagen, die der Standardwert ist, erhalten Benutzer eine Meldung angezeigt, dass sie nicht über die Rechte zum Anzeigen der Anlage verfügen. \* \* \* Bild einfügen?</span><span class="sxs-lookup"><span data-stu-id="d74f1-p111">If you choose not to allow decrypted email attachments, which is the default, users receive a message that states that they don't have the rights to view the attachment. \*\*\* insert picture?</span></span>
  
<span data-ttu-id="d74f1-172">Weitere Informationen dazu, wie Office 365 für e-Mails und e-Mail-Anlagen mit der Option nur verschlüsseln Verschlüsselung implementiert wird, finden Sie unter [Verschlüsseln-Only Option-e-Mails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span><span class="sxs-lookup"><span data-stu-id="d74f1-172">For more information about how Office 365 implements encryption for emails and email attachments with the Encrypt-Only option, see [Encrypt-Only option for emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)</span></span>
  
 <span data-ttu-id="d74f1-173">**Zum Verwalten von werden unabhängig davon, ob e-Mail-Anlagen beim Download über einen Webbrowser entschlüsselt**</span><span class="sxs-lookup"><span data-stu-id="d74f1-173">**To manage whether or not email attachments are decrypted on download from a web browser**</span></span>
  
1. <span data-ttu-id="d74f1-174">[Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d74f1-174">[Connect to Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).</span></span>
    
2. <span data-ttu-id="d74f1-175">Führen Sie das Cmdlet Set-IRMConfiguration mit dem Parameter DecryptAttachmentFromPortal wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d74f1-175">Run the Set-IRMConfiguration cmdlet with the DecryptAttachmentFromPortal parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal <$true |$false >
  ```

    <span data-ttu-id="d74f1-176">Beispielsweise gedownloadet zum Konfigurieren des Dienstes zum Entschlüsseln von e-Mail-Anlagen, wenn ein Benutzer über einen Webbrowser:</span><span class="sxs-lookup"><span data-stu-id="d74f1-176">For example, to configure the service to decrypt email attachments when a user downloads them from a web browser:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $true
  ```

    <span data-ttu-id="d74f1-177">So konfigurieren Sie den Dienst, um verschlüsselte e-Mail-Anlagen lassen, wie sie beim Download sind:</span><span class="sxs-lookup"><span data-stu-id="d74f1-177">To configure the service to leave encrypted email attachments as they are upon download:</span></span>
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $false
  ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a><span data-ttu-id="d74f1-178">Anpassen der Darstellung von e-Mail-Nachrichten und das OME-portal</span><span class="sxs-lookup"><span data-stu-id="d74f1-178">Customizing the appearance of email messages and the OME portal</span></span>
<span data-ttu-id="d74f1-179"><a name="CustomizeAppearance"> </a></span><span class="sxs-lookup"><span data-stu-id="d74f1-179"></span></span>

<span data-ttu-id="d74f1-180">Ausführliche Informationen dazu, wie Sie OME für Ihre Organisation anpassen können finden Sie unter [Hinzufügen von Branding zu verschlüsselten Nachrichten Ihrer Organisation](add-your-organization-brand-to-encrypted-messages.md).</span><span class="sxs-lookup"><span data-stu-id="d74f1-180">For detailed information about how you can customize OME for your organization, see [Add your organization's brand to your encrypted messages](add-your-organization-brand-to-encrypted-messages.md).</span></span>
  
## <a name="disabling-the-new-capabilities-for-ome"></a><span data-ttu-id="d74f1-181">Deaktivieren die neuen Funktionen für OME</span><span class="sxs-lookup"><span data-stu-id="d74f1-181">Disabling the new capabilities for OME</span></span>
<span data-ttu-id="d74f1-182"><a name="CustomizeAppearance"> </a></span><span class="sxs-lookup"><span data-stu-id="d74f1-182"></span></span>

<span data-ttu-id="d74f1-p112">Hoffentlich sie kommen nicht, wenn Sie aber, deaktivieren die neuen Funktionen für OME sehr einfach ist. Zunächst müssen Sie alle e-Mail-Flussregeln, die von die Ihnen erstellten entfernen, die die neuen OME-Funktionen verwenden. Informationen zum Entfernen von e-Mail-Flussregeln finden Sie unter [Manage Mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Klicken Sie dann, führen Sie diese Schritte in Exchange Online PowerShell.</span><span class="sxs-lookup"><span data-stu-id="d74f1-p112">We hope it doesn't come to it, but if you need to, disabling the new capabilities for OME is very straightforward. First, you'll need to remove any mail flow rules you've created that use the new OME capabilities. For information about removing mail flow rules, see [Manage mail flow rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Then, complete these steps in Exchange Online PowerShell.</span></span>
  
 <span data-ttu-id="d74f1-187">**So deaktivieren Sie die neuen Funktionen für OME**</span><span class="sxs-lookup"><span data-stu-id="d74f1-187">**To disable the new capabilities for OME**</span></span>
  
1. <span data-ttu-id="d74f1-188">[Verbindung mit Exchange Online mit Remote-PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d74f1-188">[Connect to Exchange Online Using Remote PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).</span></span>
    
2. <span data-ttu-id="d74f1-189">Wenn Sie die Schaltfläche Protect in Outlook im Web aktiviert, deaktivieren sie das Set-IRMConfiguration-Cmdlet ausführen, mit dem Parameter SimplifiedClientAccessEnabled wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d74f1-189">If you enabled the Protect button in Outlook on the web, disable it by running the Set-IRMConfiguration cmdlet with the SimplifiedClientAccessEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

3. <span data-ttu-id="d74f1-190">Führen Sie das Cmdlet Set-IRMConfiguration mit dem Parameter AzureRMSLicensingEnabled wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d74f1-190">Run the Set-IRMConfiguration cmdlet with the AzureRMSLicensingEnabled parameter as follows:</span></span>
    
  ```
  Set-IRMConfiguration -AzureRMSLicensingEnabled $false
  ```


