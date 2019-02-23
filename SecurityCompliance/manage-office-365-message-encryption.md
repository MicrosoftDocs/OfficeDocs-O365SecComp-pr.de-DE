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
# <a name="manage-office-365-message-encryption"></a>Verwalten der Office 365-Nachrichtenverschlüsselung

Nachdem Sie die Einrichtung von Office 365-Nachrichtenverschlüsselung (OM) abgeschlossen haben, können Sie die Konfiguration Ihrer Bereitstellung auf verschiedene Arten anpassen. Sie können beispielsweise konfigurieren, ob einmalige Code-Codes aktiviert werden sollen, die Schaltfläche **schützen** in Outlook im Web und vieles mehr angezeigt werden soll. In den Aufgaben in diesem Artikel wird beschrieben, wie.
  
||
|:-----|
|Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht. |
||

## <a name="managing-whether-google-yahoo-and-microsoft-account-recipients-can-use-these-accounts-to-sign-in-to-the-office-365-message-encryption-portal"></a>Verwalten der Empfänger von Google-, Yahoo-und Microsoft-Konten zum Anmelden beim Office 365-Nachrichten Verschlüsselungs Portal

Wenn Sie die neuen Office 365-Nachrichten Verschlüsselungsfunktionen einrichten, können Benutzer in Ihrer Organisation standardmäßig Nachrichten an Empfänger senden, die sich außerhalb Ihrer Office 365-Organisation befinden. Wenn der Empfänger eine *soziale ID* wie ein Google-Konto, ein Yahoo-Konto oder ein Microsoft-Konto verwendet, kann der Empfänger sich über die soziale ID beim OM-Portal anmelden. Wenn Sie möchten, können Sie festlegen, dass Empfänger keine sozialen IDs verwenden dürfen, um sich beim OM-Portal anzumelden.
  
### <a name="to-manage-whether-or-not-to-allow-recipients-to-use-social-ids-to-sign-in-to-the-ome-portal"></a>So verwalten Sie, ob Empfängern die Verwendung sozialer IDs für die Anmeldung beim OM-Portal erlaubt ist
  
1. [Herstellen einer Verbindung mit Exchange Online mithilfe der Remote-PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).

2. Führen Sie das Cmdlet Set-OMEConfiguration mit dem Parameter SocialIdSignIn wie folgt aus:

   ```powershell
   Set-OMEConfiguration -Identity <"OMEConfigurationIdParameter "> -SocialIdSignIn <$true | $false>
   ```

   Um beispielsweise soziale IDs zu deaktivieren:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $false
   ```

   So aktivieren Sie soziale IDs:

   ```powershell
   Set-OMEConfiguration -Identity "OME Configuration" -SocialIdSignIn $true
   ```

## <a name="managing-the-use-of-one-time-pass-codes-for-signing-in-to-the-office-365-message-encryption-portal"></a>Verwalten der Verwendung von einmaligen Passthrough-Codes für die Anmeldung beim Office 365-Nachrichten Verschlüsselungs Portal

Wenn der Empfänger einer Nachricht, die von OM verschlüsselt wird, nicht Outlook verwendet, erhält der Empfänger in der Standardeinstellung einen Link zur zeitlich begrenzten Webansicht, über die er die Nachricht lesen kann. Hierzu gehört ein einmaliger Code. Als Administrator können Sie verwalten, ob einmalige Durchlaufcodes zum Anmelden am OM-Portal verwendet werden können.
  
### <a name="to-manage-whether-or-not-one-time-pass-codes-are-generated-for-ome"></a>So verwalten Sie, ob einmalige Durchlaufcodes für OM generiert werden
  
1. Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

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

## <a name="managing-the-display-of-the-protect-button-in-outlook-on-the-web"></a>Verwalten der Anzeige der Schaltfläche "schützen" in Outlook im Web

Standardmäßig ist die Schaltfläche **schützen** in Outlook im Web nicht aktiviert, wenn Sie OM einrichten. Als Administrator können Sie verwalten, ob diese Schaltfläche Endbenutzern angezeigt werden soll.
  
### <a name="to-manage-whether-or-not-the-protect-button-appears-in-outlook-on-the-web"></a>So verwalten Sie, ob die Schaltfläche schützen in Outlook im Web angezeigt wird
  
1. Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

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

## <a name="enable-service-side-decryption-of-email-messages-for-ios-mail-app-users"></a>Aktivieren der dienstseitigen Entschlüsselung von e-Mail-Nachrichten für iOS-Mail-App-Benutzer

Die iOS-Mail-App kann nicht mit der Office 365-Nachrichtenverschlüsselung geschützte Nachrichten entschlüsseln. Als Office 365-Administrator können Sie die dienstseitige Entschlüsselung für Nachrichten anwenden, die an die iOS-Mail-App übermittelt werden. Wenn Sie dies tun, sendet der Dienst eine entschlüsselte Kopie der Nachricht an das iOS-Gerät. Die Nachricht wird auf dem Clientgerät entschlüsselt gespeichert. Die Nachricht behält auch Informationen zu Nutzungsrechten, obwohl die iOS-Mail-App keine clientseitigen Nutzungsrechte für den Benutzer anwendet. Dies führt dazu, dass der Benutzer die Nachricht kopieren oder drucken kann, auch wenn Sie nicht ursprünglich über die Rechte dazu verfügt hat. Wenn der Benutzer jedoch versucht, eine Aktion abzuschließen, die den Office 365-e-Mail-Server erfordert, wie beispielsweise die Weiterleitung der Nachricht, lässt der Server die Aktion nicht zu, wenn der Benutzer ursprünglich nicht über das Nutzungsrecht für diesen Vorgang verfügt. Endbenutzer können jedoch keine Nutzungseinschränkung weiterleiten, indem Sie die Nachricht von einem anderen Konto in ihrer iOS-Mail-App weiterleiten. unabhängig davon, ob Sie die dienstseitige Entschlüsselung von e-Mails, Anhänge zu verschlüsselten und geschützten e-Mails kann nicht in der iOS-Mail-App angezeigt werden.
  
Wenn Sie nicht zulassen, dass entschlüsselte Nachrichten an iOS-Mail-App-Benutzer gesendet werden, erhalten Benutzer eine Meldung, die besagt, dass Sie nicht über die Berechtigung zum Anzeigen der Nachricht verfügen. Die dienstseitige Entschlüsselung von e-Mail-Nachrichten ist standardmäßig nicht aktiviert.
  
Weitere Informationen und eine Ansicht der Clientumgebung finden Sie unter Anzeigen von verschlüsselten [Nachrichten auf Ihrem iPhone oder iPad](https://support.office.com/article/4d631321-0d26-4bcc-a483-d294dd0b1caf).
  
### <a name="to-manage-whether-or-not-ios-mail-app-users-can-view-messages-protected-by-office-365-message-encryption"></a>So verwalten Sie, ob iOS-Mail-App-Benutzer Nachrichten anzeigen können, die von der Office 365-Nachrichtenverschlüsselung geschützt sind
  
1. Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Führen Sie das Cmdlet Set-ActiveSyncOrganizations mit dem Parameter AllowRMSSupportForUnenlightenedApps aus:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps <$true|$false>
   ```

   So konfigurieren Sie beispielsweise den Dienst zum Entschlüsseln von Nachrichten, bevor Sie an unaufgeklärte apps wie die iOS-Mail-App gesendet werden:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $true
   ```

   Oder, um den Dienst so zu konfigurieren, dass entschlüsselte Nachrichten nicht an unerleuchtete apps gesendet werden:

   ```powershell
   Set-ActiveSyncOrganizationSettings -AllowRMSSupportForUnenlightenedApps $false
   ```

## <a name="enable-service-side-decryption-of-email-attachments-for-web-browser-mail-clients"></a>Aktivieren der dienstseitigen Entschlüsselung von e-Mail-Anlagen für Webbrowser-e-Mail-Clients

Bei Verwendung der Nachrichtenverschlüsselung von Office 365 werden Anlagen in der Regel automatisch verschlüsselt. Als Office 365-Administrator können Sie die dienstseitige Entschlüsselung für e-Mail-Anhänge anwenden, die Benutzer über einen Webbrowser herunterladen.
  
Wenn Sie dies tun, sendet der Dienst eine entschlüsselte Kopie der Datei an das Gerät. Die Nachricht ist weiterhin verschlüsselt. Die e-Mail-Anlage behält auch Informationen zu Nutzungsrechten, obwohl der Browserclient seitigen Nutzungsrechten für den Benutzer nicht zutrifft. Dies führt dazu, dass der Benutzer die e-Mail-Anlage auch dann kopieren oder ausdrucken kann, wenn er ursprünglich nicht über die Rechte dazu verfügt. Wenn der Benutzer jedoch versucht, eine Aktion abzuschließen, die den Office 365-e-Mail-Server erfordert, wie beispielsweise das Weiterleiten der Anlage, lässt der Server die Aktion nicht zu, wenn der Benutzer ursprünglich nicht über das Nutzungsrecht für diesen Vorgang verfügt.
  
Unabhängig davon, ob Sie die dienstseitige Entschlüsselung von Anlagen einrichten, können Anhänge zu verschlüsselten und geschützten e-Mails nicht in der iOS-Mail-App angezeigt werden.
  
Wenn Sie nicht die standardmäßige verschlüsselte e-Mail-Anlagen zulassen, erhalten Benutzer eine Meldung, die besagt, dass Sie nicht über die Berechtigung zum Anzeigen der Anlage verfügen.
  
Weitere Informationen dazu, wie Office 365 die Verschlüsselung von e-Mails und e-Mail-Anlagen mit der Option nur-Verschlüsselung implementiert, finden Sie unter [Encrypt-only Option for Emails.](https://docs.microsoft.com/azure/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails)
  
### <a name="to-manage-whether-or-not-email-attachments-are-decrypted-on-download-from-a-web-browser"></a>So verwalten Sie, ob e-Mail-Anhänge beim Herunterladen aus einem Webbrowser entschlüsselt werden
  
1. Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

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

## <a name="customizing-the-appearance-of-email-messages-and-the-ome-portal"></a>Anpassen der Darstellung von e-Mail-Nachrichten und des OM-Portals

Ausführliche Informationen dazu, wie Sie OM für Ihre Organisation anpassen können, finden Sie unter [Hinzufügen der Marke Ihrer Organisation zu ihren verschlüsselten Nachrichten](add-your-organization-brand-to-encrypted-messages.md).
  
## <a name="disabling-the-new-capabilities-for-ome"></a>Deaktivieren der neuen Funktionen für OM

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
