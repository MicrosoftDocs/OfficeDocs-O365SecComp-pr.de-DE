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
# <a name="manage-office-365-message-encryption"></a>Verwalten der Office 365-Nachrichtenverschlüsselung

Nachdem Sie die Einrichtung von Office 365-Nachrichtenverschlüsselung (OM) abgeschlossen haben, können Sie die Konfiguration Ihrer Bereitstellung auf verschiedene Weise anpassen. Sie können beispielsweise konfigurieren, ob einmalige Code-Codes aktiviert werden sollen, die Schaltfläche **schützen** in Outlook im Web und vieles mehr angezeigt werden soll. In den Aufgaben in diesem Artikel wird beschrieben, wie.

## <a name="manage-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Verwalten, ob die Empfänger von Google, Yahoo und Microsoft-Konto diese Konten verwenden können, um sich beim Office 365-Nachrichten Verschlüsselungs Portal anzumelden

Wenn Sie die neuen Office 365-Nachrichten Verschlüsselungsfunktionen einrichten, können Benutzer in Ihrer Organisation Nachrichten an Empfänger senden, die sich außerhalb Ihrer Office 365-Organisation befinden. Wenn der Empfänger eine *soziale ID* wie ein Google-Konto, ein Yahoo-Konto oder ein Microsoft-Konto verwendet, kann sich der Empfänger mit einer sozialen ID beim OM-Portal anmelden. Wenn Sie möchten, können Sie festlegen, dass Empfänger keine sozialen IDs verwenden dürfen, um sich beim OM-Portal anzumelden.
  
### <a name="to-manage-whether-recipients-can-use-social-ids-to-sign-in-to-the-ome-portal"></a>So verwalten Sie, ob Empfänger soziale IDs verwenden können, um sich beim OM-Portal anzumelden
  
1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).

2. Führen Sie das Cmdlet Set-OMEConfiguration mit dem Parameter SocialIdSignIn wie folgt aus:

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter"> -SocialIdSignIn <$true|$false>
   ```

   Um beispielsweise soziale IDs zu deaktivieren:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   So aktivieren Sie soziale IDs:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="manage-the-use-of-one-time-pass-codes-for-the-office-365-message-encryption-portal"></a>Verwalten der Verwendung von einmaligen Durchlaufcodes für das Office 365-Nachrichten Verschlüsselungs Portal

Wenn der Empfänger einer Nachricht, die von OM verschlüsselt wird, nicht Outlook verwendet, unabhängig vom Konto, das der Empfänger verwendet, erhält der Empfänger einen Link zur zeitlich begrenzten Webansicht, über die er die Nachricht lesen kann. Dieser Link enthält einen einmaligen Code. Als Administrator können Sie entscheiden, ob sich Empfänger mit einmaligen Codes bei dem OM-Portal anmelden können.
  
### <a name="to-manage-whether-ome-generates-one-time-pass-codes"></a>So verwalten Sie, ob OM einmalige Durchlaufcodes generiert
  
1. Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet Set-OMEConfiguration mit dem Parameter OTPEnabled aus:

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -OTPEnabled <$true|$false>
   ```

   So können Sie beispielsweise einmalige Durchlaufcodes deaktivieren:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $false
   ```

   So aktivieren Sie einmalige Code-Codes:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -OTPEnabled $true
   ```

## <a name="manage-the-display-of-the-protect-button-in-outlook-on-the-web"></a>Verwalten der Anzeige der Schaltfläche "schützen" in Outlook im Web

Die Schaltfläche **schützen** in Outlook im Web ist deaktiviert, wenn Sie OM einrichten. Als Administrator können Sie verwalten, ob diese Schaltfläche Endbenutzern angezeigt werden soll.
  
### <a name="to-manage-whether-the-protect-button-appears-in-outlook-on-the-web"></a>So verwalten Sie, ob die Schaltfläche schützen in Outlook im Web angezeigt wird
  
1. Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet Set-IRMConfiguration mit dem-SimplifiedClientAccessEnabled-Parameter aus:

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled <$true|$false>
   ```

   Um beispielsweise die Schaltfläche **Protect** zu deaktivieren:

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

   So aktivieren Sie die Schaltfläche " **schützen** "

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $true
   ```

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>Aktivieren der dienstseitigen Entschlüsselung von e-Mail-Nachrichten für IOS-Mail-App-Benutzer

Die IOS-Mail-App kann nicht mit der Office 365-Nachrichtenverschlüsselung geschützte Nachrichten entschlüsseln. Als Office 365-Administrator können Sie die dienstseitige Entschlüsselung für Nachrichten anwenden, die an die IOS-Mail-App übermittelt werden. Wenn Sie sich für die Verwendung der dienstseitigen Entschlüsselung entscheiden, sendet der Dienst eine entschlüsselte Kopie der Nachricht an das IOS-Gerät. Auf dem Clientgerät wird eine entschlüsselte Kopie der Nachricht gespeichert. Die Nachricht behält auch Informationen zu Nutzungsrechten, obwohl die IOS-Mail-App keine clientseitigen Nutzungsrechte für den Benutzer anwendet. Der Benutzer kann die Nachricht auch dann kopieren oder drucken, wenn Sie nicht ursprünglich über die Rechte dazu verfügt hat. Wenn der Benutzer jedoch versucht, eine Aktion abzuschließen, die den Office 365-e-Mail-Server erfordert, wie beispielsweise das Weiterleiten der Nachricht, lässt der Server die Aktion nicht zu, wenn der Benutzer nicht ursprünglich über das Nutzungsrecht für diesen Vorgang verfügt. Endbenutzer können jedoch die Verwendungseinschränkung "nicht weiterleiten" umgehen, indem Sie die Nachricht von einem anderen Konto innerhalb der IOS-Mail-App weiterleiten. Unabhängig davon, ob Sie die dienstseitige Entschlüsselung von e-Mails einrichten, können Anlagen zu verschlüsselten und geschützten e-Mails nicht in der IOS-Mail-App angezeigt werden.
  
Wenn Sie nicht zulassen, dass entschlüsselte Nachrichten an IOS-Mail-App-Benutzer gesendet werden, erhalten Benutzer eine Meldung, die besagt, dass Sie nicht über die Berechtigung zum Anzeigen der Nachricht verfügen. Die dienstseitige Entschlüsselung von e-Mail-Nachrichten ist standardmäßig nicht aktiviert.
  
Weitere Informationen und eine Ansicht der Clientumgebung finden Sie unter Anzeigen von verschlüsselten [Nachrichten auf Ihrem iPhone oder iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).
  
### <a name="to-manage-whether-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a>So verwalten Sie, ob IOS-Mail-App-Benutzer Nachrichten anzeigen können, die von der Office 365-Nachrichtenverschlüsselung geschützt sind
  
1. Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet Set-ActiveSyncOrganizations mit dem Parameter AllowRMSSupportForUnenlightenedApps aus:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   So konfigurieren Sie beispielsweise den Dienst zum Entschlüsseln von Nachrichten, bevor Sie an unaufgeklärte apps wie die IOS-Mail-App gesendet werden:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   Oder, um den Dienst so zu konfigurieren, dass entschlüsselte Nachrichten nicht an unerleuchtete apps gesendet werden:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>Aktivieren der dienstseitigen Entschlüsselung von e-Mail-Anlagen für Webbrowser-e-Mail-Clients

Bei Verwendung der Nachrichtenverschlüsselung von Office 365 werden Anlagen in der Regel automatisch verschlüsselt. Als Office 365-Administrator können Sie die dienstseitige Entschlüsselung für e-Mail-Anhänge anwenden, die Benutzer über einen Webbrowser herunterladen.
  
Wenn Sie die dienstseitige Entschlüsselung verwenden, sendet der Dienst eine entschlüsselte Kopie der Datei an das Gerät. Die Nachricht ist weiterhin verschlüsselt. Die e-Mail-Anlage speichert auch Informationen zu Nutzungsrechten, obwohl der Browserclient seitige Nutzungsrechte nicht auf den Benutzer angewendet hat. Der Benutzer kann die e-Mail-Anlage auch dann kopieren oder ausdrucken, wenn Sie nicht ursprünglich über die Rechte dazu verfügt hat. Wenn der Benutzer jedoch versucht, eine Aktion abzuschließen, die den Office 365-e-Mail-Server erfordert, wie beispielsweise das Weiterleiten der Anlage, lässt der Server die Aktion nicht zu, wenn der Benutzer ursprünglich nicht über das Nutzungsrecht verfügt hat.
  
Unabhängig davon, ob Sie die dienstseitige Entschlüsselung von Anlagen einrichten, können Benutzer keine Anlagen zu verschlüsselten und geschützten e-Mails in der IOS-Mail-App anzeigen.
  
Wenn Sie nicht die standardmäßige verschlüsselte e-Mail-Anlagen zulassen, erhalten Benutzer eine Meldung, die besagt, dass Sie nicht über die Berechtigung zum Anzeigen der Anlage verfügen.
  
Weitere Informationen dazu, wie Office 365 die Verschlüsselung von e-Mails und e-Mail-Anlagen mit der Option nur-Verschlüsselung implementiert, finden Sie unter [Encrypt-only Option for Emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)
  
### <a name="to-manage-whether-email-attachments-are-decrypted-on-download-from-a-web-browser"></a>So verwalten Sie, ob e-Mail-Anhänge beim Herunterladen aus einem Webbrowser entschlüsselt werden
  
1. Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet Set-IRMConfiguration mit dem Parameter DecryptAttachmentFromPortal aus:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal <$true|$false>
   ```

   Beispielsweise können Sie den Dienst so konfigurieren, dass e-Mail-Anlagen entschlüsselt werden, wenn ein Benutzer Sie von einem Webbrowser herunterlädt:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $true
   ```

   So konfigurieren Sie den Dienst so, dass verschlüsselte e-Mail-Anlagen beim Herunterladen hinterlassen werden:

   ```powershell
   Set-IRMConfiguration -DecryptAttachmentFromPortal $false
   ```

## <a name="ensure-all-external-recipients-use-the-ome-portal-to-read-encrypted-mail--office-365-advanced-message-encryption-only"></a>Sicherstellen, dass alle externen Empfänger das OM-Portal verwenden, um verschlüsselte e-Mails zu lesen – nur Office 365 erweiterte Nachrichtenverschlüsselung

Wenn Sie über die erweiterte Nachrichtenverschlüsselung von Office 365 verfügen, können Sie mit benutzerdefinierten Branding-Vorlagen erzwingen, dass Empfänger eine Wrapper-e-Mail erhalten, die Sie zum Lesen verschlüsselter e-Mails im OM-Portal anstelle von Outlook oder Outlook im Web anweist. Möglicherweise möchten Sie dies tun, wenn Sie mehr Kontrolle darüber haben möchten, wie Empfänger die empfangene e-Mail verwenden. Wenn externe Empfänger beispielsweise e-Mails im Webportal anzeigen, können Sie ein Ablaufdatum für die e-Mail festlegen und die e-Mail widerrufen. Diese Funktionen werden nur über das OM-Portal unterstützt. Sie können die Option Verschlüsseln und die Option nicht weiterleiten beim Erstellen der Nachrichtenfluss Regeln verwenden.

### <a name="create-a-custom-template-to-force-all-external-recipients-to-use-the-ome-portal-and-for-encrypted-email-to-be-revocable-and-expire-in-7-days"></a>Erstellen Sie eine benutzerdefinierte Vorlage, um zu erzwingen, dass alle externen Empfänger das OM-Portal verwenden und dass verschlüsselte e-Mails widerruflich und innerhalb von 7 Tagen ablaufen.

1. Verwenden Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation, und starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet New-OMEConfiguration aus:

   ```powershell
   New-OMEConfiguration -Identity "<template name>" -ExternalMailExpiryInDays 7
   ```

   Hierbei `template name` ist der Name, den Sie für die benutzerdefinierte Branding-Vorlage Office 365 Message Encryption verwenden möchten. For example,

   ```powershell
   New-OMEConfiguration -Identity "<One week expiration>" -ExternalMailExpiryInDays 7
   ```

3. Führen Sie das Cmdlet New-TransportRule aus:

   ```powershell
   New-TransportRule -name "<mail flow rule name>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "<option name>" -ApplyRightsProtectionCustomizationTemplate "<template name>"
   ```

    Dabei gilt:

   - `mail flow rule name`ist der Name, der für die neue Nachrichtenfluss Regel verwendet werden soll.

   - `option name`ist entweder `Encrypt` oder `Do Not Forward`.

   - `template name`ist der Name, den Sie zum Beispiel `One week expiration`der benutzerdefinierten Branding-Vorlage erteilt haben.

   Zum Verschlüsseln aller externen e-Mails mit der Vorlage "One Week Ablauf" und Anwenden der nur-Verschlüsselung-Option:

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Encrypt" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

   So verschlüsseln Sie alle externen e-Mails mit der Vorlage "ein Wochenablauf" und wenden die Option "nicht weiterleiten" an:

   ```powershell
   New-TransportRule -name "<All outgoing mail>" -FromScope "InOrganization" -ApplyRightsProtectionTemplate "Do Not Forward" -ApplyRightsProtectionCustomizationTemplate "<One week expiration>"
   ```

## <a name="customize-the-appearance-of-email-messages-and-the-ome-portal"></a>Anpassen der Darstellung von e-Mail-Nachrichten und des OM-Portals

Ausführliche Informationen dazu, wie Sie OM für Ihre Organisation anpassen können, finden Sie unter [Hinzufügen der Marke Ihrer Organisation zu ihren verschlüsselten Nachrichten](add-your-organization-brand-to-encrypted-messages.md).
  
## <a name="disable-the-new-capabilities-for-ome"></a>Deaktivieren der neuen Funktionen für OM

Wir hoffen, dass dies nicht der Fall ist, aber wenn Sie es benötigen, ist es sehr einfach, die neuen Funktionen für OM zu deaktivieren. Zunächst müssen Sie alle von Ihnen erstellten Nachrichtenfluss Regeln entfernen, die die neuen OM-Funktionen verwenden. Informationen zum Entfernen von Nachrichtenfluss Regeln finden Sie unter [Manage Mail Flow Rules](https://technet.microsoft.com/library/jj657505%28v=exchg.150%29.aspx). Führen Sie diese Schritte dann in Exchange Online PowerShell aus.
  
### <a name="to-disable-the-new-capabilities-for-ome"></a>So deaktivieren Sie die neuen Funktionen für OM
  
1. Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Wenn Sie die Schaltfläche **schützen** in Outlook im Web aktiviert haben, deaktivieren Sie Sie, indem Sie das Cmdlet Set-IRMConfiguration mit dem Parameter SimplifiedClientAccessEnabled ausführen. Überspringen Sie andernfalls diesen Schritt.

   ```powershell
   Set-IRMConfiguration -SimplifiedClientAccessEnabled $false
   ```

3. Deaktivieren Sie die neuen Funktionen für OM, indem Sie das Cmdlet Set-IRMConfiguration ausführen, wobei der Parameter AzureRMSLicensingEnabled auf false festgelegt ist:

   ```powershell
   Set-IRMConfiguration -AzureRMSLicensingEnabled $false
   ```
