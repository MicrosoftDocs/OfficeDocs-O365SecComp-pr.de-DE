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
# <a name="manage-office-365-message-encryption"></a>Verwalten von Office 365-Nachrichtenverschlüsselung

Nachdem Sie die Einstellung von Office 365 Message Encryption (OME) abgeschlossen haben, können Sie die Konfiguration Ihrer Bereitstellung auf unterschiedliche Weise anpassen. Beispielsweise können Sie konfigurieren, ob aktivieren einmalige Kenncodes verlangt, **schützen** die Schaltfläche in Outlook auf den Web- und vieles mehr angezeigt. Die Aufgaben in diesem Artikel wird beschrieben, wie. 
  
||
|:-----|
|Dieser Artikel ist Teil einer größeren Reihe von Artikeln zur Office 365 Message Encryption. In diesem Artikel ist für Administratoren und IT-Spezialisten vorgesehen. Wenn Sie sich gerade befinden Suchen nach Informationen zu senden oder Empfangen einer verschlüsselten Nachricht, finden Sie in der Liste der Artikel in [Office 365 Message Encryption (OME)](ome.md) , und suchen Sie im Artikel, der am besten Ihren Anforderungen entspricht. |
   
## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Verwalten von, ob Google, Yahoo! und Microsoft Account Empfänger diese Konten, zur Anmeldung verwenden können bei Office 365 Message Encryption-portal
<a name="PermitSocialID"> </a>

Standardmäßig Wenn Sie die neuen Funktionen für Office 365 Message Encryption einrichten können Benutzer in Ihrer Organisation Nachrichten an Empfänger senden, die sich außerhalb Ihrer Office 365-Organisation befinden. Wenn der Empfänger eine *ID für soziale Netzwerke* wie Google-Konto, Yahoo-Konto oder Microsoft-Konto verwendet wird, kann der Empfänger OME-Portal mit der sozialen-ID. anmelden Wenn Sie möchten, können Sie auswählen, die nicht für soziale Netzwerke IDs verwenden Sie zur Anmeldung bei des OME-Portals-Empfänger zuzulassen. 
  
 **Ob Sie Empfänger für soziale Netzwerke IDs OME-Portal Anmeldung verwenden darf verwalten**
  
1. [Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Führen Sie das Cmdlet "Set-OMEConfiguration" mit dem Parameter SocialIdSignIn wie folgt aus:
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true |$false >
  ```

    Geben Sie beispielsweise Folgendes ein, um die IDs für soziale Netzwerke deaktivieren:
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
  ```

    So aktivieren Sie IDs für soziale Netzwerke
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
  ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a>Die Verwendung der einmaligen Kenncodes zum Anmelden bei Office 365 Message Encryption-Portal verwalten
<a name="GenerateOTPC"> </a>

Wenn der Empfänger einer Nachricht verschlüsselt, OME Outlook, unabhängig von der durch den Empfänger verwendete Konto nicht verwendet, erhält der Empfänger eine zeitlich beschränkte Webansicht Verknüpfung, die Sie die Nachricht lesen können. Dies umfasst eine einmalige Kennung. Als Administrator können Sie verwalten, ob Kenncodes einmalige Anmelden OME-Portal verwendet werden können oder nicht.
  
 **Verwalten, unabhängig davon, ob eine einmalige Kenncodes für OME generiert werden**
  
1. [Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Führen Sie das Cmdlet "Set-OMEConfiguration" mit dem Parameter OTPEnabled wie folgt aus:
    
  ```
  Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true |$false >
  ```

    Geben Sie beispielsweise Folgendes ein, um die einmalige Kenncodes zu deaktivieren:
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
  ```

    So aktivieren Sie das einmalige Kenncodes verlangt:
    
  ```
  Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
  ```

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a>Verwaltung der Anzeige der Schaltfläche Protect in Outlook im Web
<a name="DisplayProtectButton"> </a>

Standardmäßig ist die Schaltfläche **Protect** in Outlook im Web nicht aktiviert, wenn Sie OME einrichten. Als Administrator können Sie, ob diese Schaltfläche für Endbenutzer angezeigt werden soll oder nicht verwalten. 
  
 **Zum Verwalten von wird angezeigt, unabhängig davon, ob die Schaltfläche Protect in Outlook im Web**
  
1. [Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Führen Sie das Cmdlet Set-IRMConfiguration mit dem Parameter - SimplifiedClientAccessEnabled wie folgt aus:
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true |$false >
  ```

    Geben Sie beispielsweise Folgendes ein, um die Schaltfläche **Protect** zu deaktivieren: 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

    So aktivieren Sie die Schaltfläche **schützen** : 
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
  ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>Aktivieren Sie dienstseitige Entschlüsselung von e-Mails für iOS Mail-app-Benutzer
<a name="EnableServiceSideDecrypt"> </a>

Die Mail-app für iOS kann nicht mit Office 365 Message Encryption geschützten Nachrichten nicht entschlüsseln. Als Office 365-Administrator können Sie dienstseitige Entschlüsselung für Nachrichten an die Mail-app für iOS anwenden. Wenn Sie dazu entschließen, sendet der Dienst eine verschlüsselte Kopie der Nachricht an das Gerät iOS. Die Nachricht wird auf dem Clientgerät entschlüsselt gespeichert. Die Nachricht enthält auch Informationen zu Nutzungsrechte, auch wenn die Mail-app für iOS mithilfe der clientseitigen Nutzungsrechte für den Benutzer nicht zutrifft. Dies bedeutet, dass der Benutzer kann kopieren oder der Nachricht drucken, auch wenn sie ursprünglich nicht über die Rechte dazu verfügt. Jedoch, wenn der Benutzer versucht, eine Aktion ausführen, in der Office 365-Mailserver, z. B. das Weiterleiten der Nachricht erfordert wird der Server nicht die Aktion lassen, wenn der Benutzer nicht ursprünglich Usage dazu berechtigt. Endbenutzer können nicht weiterleiten verwendungseinschränkung durch Weiterleiten der Nachricht von einem anderen Konto in ihrer iOS-Mail-App unabhängig davon, ob Sie dienstseitige Entschlüsselung von e-Mail einrichten umgehen jedoch aller Anlagen verschlüsselt werden, und die Rechte geschützte Nachrichten kann nicht in der Mail-app für iOS angezeigt werden.
  
Wenn Sie nicht entschlüsselte Nachrichten gesendet werden können iOS mail-app-Benutzer, Benutzer erhalten die Meldung, die besagt, dass sie nicht über die Rechte zum Anzeigen der Meldung verfügen. Standardmäßig ist die dienstseitige Entschlüsselung der e-Mail-Nachrichten nicht aktiviert.
  
Weitere Informationen und einen Überblick über die Clientumgebung finden Sie im Abschnitt, "[Anzeigen von verschlüsselten Nachrichten auf dem iPhone oder iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf#iOSEncryptedMail)" in [verschlüsselten Nachrichten auf dem iPhone oder iPad anzuzeigen](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).
  
 **Zum Verwalten, unabhängig davon, ob e-Mail von iOS-app-Benutzer kann von Office 365 Message Encryption geschützte Nachrichten anzeigen.**
  
1. [Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Führen Sie das Cmdlet Set-ActiveSyncOrganizations mit dem Parameter AllowRMSSupportForUnenlightenedApps wie folgt aus:
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true |$false >
  ```

    Beispiel-mail-so konfigurieren Sie den Dienst, um Nachrichten zu entschlüsseln, bevor sie unenlightened Apps gesendet werden wie iOS app:
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
  ```

    Geben Sie beispielsweise Folgendes ein, um den Dienst nicht zum Senden von entschlüsselter Nachrichten an unenlightened apps zu konfigurieren:
    
  ```
  Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
  ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>Aktivieren Sie dienstseitige Entschlüsselung der e-Mail-Anlagen für Webbrowser Mail-clients
<a name="EnableServiceSideDecrypt"> </a>

Wenn Sie Office 365-nachrichtenverschlüsselung verwenden, werden normalerweise automatisch Anlagen verschlüsselt. Als Office 365-Administrator können Sie dienstseitige Entschlüsselung für e-Mail-Anlagen anwenden, die Benutzer über einen Webbrowser herunterladen. 
  
Wenn Sie dazu entschließen, sendet der Dienst eine verschlüsselte Kopie der Datei auf das Gerät. Die Nachricht wird weiterhin verschlüsselt. Die e-Mail-Anlage behält auch Informationen über die Nutzungsrechte, obwohl im Browser nicht mithilfe der clientseitigen Nutzungsrechte für den Benutzer angewendet werden kann. Dies bedeutet, dass der Benutzer kann kopieren oder die e-Mail-Anlage drucken, selbst wenn sie ursprünglich nicht über die Rechte dazu verfügt. Jedoch, wenn der Benutzer versucht, eine Aktion ausführen, in der Office 365-Mailserver, wie die Anlage weiterleiten erfordert der Server die Aktion lässt, wenn der Benutzer nicht ursprünglich Usage dazu berechtigt.
  
Unabhängig davon, ob Sie dienstseitige Entschlüsselung von Anlagen eingerichtet alle Anhänge verschlüsselt und Rechte geschützte e-Mail nicht in der Mail-app für iOS angezeigt werden.
  
Wenn Sie nicht zulassen entschlüsselten e-Mail-Anlagen, die der Standardwert ist, erhalten Benutzer eine Meldung angezeigt, dass sie nicht über die Rechte zum Anzeigen der Anlage verfügen. \* \* \* Bild einfügen?
  
Weitere Informationen dazu, wie Office 365 für e-Mails und e-Mail-Anlagen mit der Option nur verschlüsseln Verschlüsselung implementiert wird, finden Sie unter [Verschlüsseln-Only Option-e-Mails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)
  
 **Zum Verwalten von werden unabhängig davon, ob e-Mail-Anlagen beim Download über einen Webbrowser entschlüsselt**
  
1. [Verbindung mit Exchange Online mit Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Führen Sie das Cmdlet Set-IRMConfiguration mit dem Parameter DecryptAttachmentFromPortal wie folgt aus:
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal <$true |$false >
  ```

    Beispielsweise gedownloadet zum Konfigurieren des Dienstes zum Entschlüsseln von e-Mail-Anlagen, wenn ein Benutzer über einen Webbrowser:
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $true
  ```

    So konfigurieren Sie den Dienst, um verschlüsselte e-Mail-Anlagen lassen, wie sie beim Download sind:
    
  ```
  Set-IRMConfiguration -DecryptAttachmentFromPortal $false
  ```

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a>Anpassen der Darstellung von e-Mail-Nachrichten und das OME-portal
<a name="CustomizeAppearance"> </a>

Ausführliche Informationen dazu, wie Sie OME für Ihre Organisation anpassen können finden Sie unter [Hinzufügen von Branding zu verschlüsselten Nachrichten Ihrer Organisation](add-your-organization-brand-to-encrypted-messages.md).
  
## <a name="disabling-the-new-capabilities-for-ome"></a>Deaktivieren die neuen Funktionen für OME
<a name="CustomizeAppearance"> </a>

Hoffentlich sie kommen nicht, wenn Sie aber, deaktivieren die neuen Funktionen für OME sehr einfach ist. Zunächst müssen Sie alle e-Mail-Flussregeln, die von die Ihnen erstellten entfernen, die die neuen OME-Funktionen verwenden. Informationen zum Entfernen von e-Mail-Flussregeln finden Sie unter [Manage Mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Klicken Sie dann, führen Sie diese Schritte in Exchange Online PowerShell.
  
 **So deaktivieren Sie die neuen Funktionen für OME**
  
1. [Verbindung mit Exchange Online mit Remote-PowerShell](https://technet.microsoft.com/library/jj984289%28v=exchg.160%29.aspx).
    
2. Wenn Sie die Schaltfläche Protect in Outlook im Web aktiviert, deaktivieren sie das Set-IRMConfiguration-Cmdlet ausführen, mit dem Parameter SimplifiedClientAccessEnabled wie folgt:
    
  ```
  Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
  ```

3. Führen Sie das Cmdlet Set-IRMConfiguration mit dem Parameter AzureRMSLicensingEnabled wie folgt aus:
    
  ```
  Set-IRMConfiguration -AzureRMSLicensingEnabled $false
  ```


