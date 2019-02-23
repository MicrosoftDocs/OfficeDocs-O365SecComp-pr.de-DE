---
title: Hinzufügen Ihrer Unternehmensmarke zu ihren verschlüsselten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
ms.collection:
- M365-security-compliance
description: Als Exchange-Administrator können Sie das Branding Ihrer Organisation auf verschlüsselte e-Mail-Nachrichten Ihrer Organisation und auf die Inhalte des Verschlüsselungs Portals anwenden.
ms.openlocfilehash: 237824890d2b519e36cf5205a1f5c3dcc0fe830a
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213335"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Hinzufügen der Marke Ihres Unternehmens zu Ihren verschlüsselten Nachrichten

Als Exchange Online-oder Exchange Online Protection-Administrator können Sie Ihr Unternehmensbranding anwenden, um das Aussehen der Office 365-e-Mail-Nachrichten in Ihrer Organisation und die Inhalte des Verschlüsselungs Portals anzupassen. Mithilfe der Windows PowerShell-Cmdlets Get-OMEConfiguration und Set-OMEConfiguration können Sie die folgenden Aspekte der Anzeige Erfahrung für Empfänger von verschlüsselten e-Mail-Nachrichten anpassen:
  
- Einleitender Text der E-Mail, die die verschlüsselte Nachricht enthält
- Text des Haftungsausschlusses der E-Mail, die die verschlüsselte Nachricht enthält
- Text, der im OM-Portal angezeigt wird
- Logo, das in der e-Mail-Nachricht und im Portal angezeigt wird
- Hintergrundfarbe in der e-Mail-Nachricht und im Portal

Sie können auch jederzeit zum Standardaussehen und -verhalten zurückkehren.

Wenn Sie mehr Kontrolle wünschen, können Sie mehrere Vorlagen für verschlüsselte e-Mails aus Ihrer Organisation erstellen. Mithilfe dieser Vorlagen können Sie mehr als nur das Aussehen und Verhalten der e-Mail-Nachrichten steuern, aber auch Teile der Endbenutzeroberfläche steuern. Sie können beispielsweise angeben, ob Empfänger von e-Mails, auf die diese Vorlage angewendet wurde und die Google, Yahoo und Microsoft-Konten verwenden, diese Konten verwenden können, um sich beim Office 365-Nachrichten Verschlüsselungs Portal anzumelden. Sie können Vorlagen verwenden, um mehrere Anwendungsfälle zu erfüllen, wie zum Beispiel:

- Vorlagen für jede Abteilung, wie Finanzen, Vertrieb usw.
- Vorlagen für verschiedene Produkte
- Vorlagen für verschiedene geographische Regionen oder Länder

Nachdem Sie die Vorlagen erstellt haben, können Sie Sie mithilfe von Exchange-Nachrichtenfluss Regeln auf verschlüsselte e-Mails anwenden. Alle e-Mails, die mit diesen Vorlagen gebrandmarkt werden, können widerrufen werden.
  
||
|:-----|
|Dieser Artikel ist Teil einer größeren Artikelreihe zur Nachrichtenverschlüsselung von Office 365. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht suchen, lesen Sie die Artikelliste in [Office 365 Message Encryption (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht.|
||

## <a name="create-branding-templates"></a>Erstellen von Branding-Vorlagen

Sie erstellen Branding-Vorlagen für Ihre Organisation in Windows PowerShell mit dem New-OMEConfiguration-Cmdlet. Nachdem Sie die Vorlage erstellt haben, definieren Sie die Teile der Vorlage mithilfe des Cmdlets Set-OMEConfiguration. Sie können mehrere Vorlagen erstellen.

![Anpassbare e-Mail-Teile](media/ome-template-breakout.png)
  
1. Starten Sie eine Windows PowerShell-Sitzung, und stellen Sie eine Verbindung mit Exchange Online her, wenn Sie ein Arbeits-oder Schulkonto mit globalen Administratorberechtigungen in Ihrer Office 365-Organisation verwenden. Weitere Informationen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Verwenden Sie das New-OMEConfiguration-Cmdlet, um eine neue Vorlage zu erstellen.

   ```powershell
   New-OMEConfiguration -Identity <OMEConfigurationIdParameter>
   ```
   Beispiel:

   ```powershell
   New-OMEConfiguration -Identity <Branding template 1>
   ```
3. Definieren Sie die Anpassungen für die Vorlage, die Sie gerade definiert haben, indem Sie das Cmdlet Set-OMEConfiguration verwenden, wie in [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration) beschrieben, oder verwenden Sie die folgende Tabelle.

|**So passen Sie dieses Verschlüsselungsfeature an**|**Verwenden Sie diese Befehle**|
|:-----|:-----|
|Hintergrundfarbe|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -BackgroundColor "#ffffff"`|
|Logo|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Unterstützte Dateiformate: .png, .jpg, .bmp oder .tiff  <br/> Optimale Größe der Logodatei: kleiner als 40 KB  <br/> Optimale Abmessungen des Logobilds: 170 x 70 Pixel|
|Text neben dem Namen des Absenders und der e-Mail-Adresse|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -IntroductionText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -IntroductionText "has sent you a secure message."`|
|Text, der auf der Schaltfläche "Nachricht lesen" angezeigt wird|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -ReadButtonText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -ReadButtonText "Read Secure Message."`|
|Text, der oberhalb der Schaltfläche "Nachricht lesen" angezeigt wird|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -DisclaimerText "This message is confidential for the use of the addressee only."`|
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."`|
|So aktivieren oder deaktivieren Sie die Authentifizierung mit einem einmaligen Code für diese benutzerdefinierte Vorlage|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -OTPEnabled <$true|$false>` <br/> **Beispiele:** <br/>So aktivieren Sie einmalige Kennungen für diese benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $true` <br/> So deaktivieren Sie einmalige Kennungen für diese benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $false`|
|So aktivieren oder deaktivieren Sie die Authentifizierung mit Microsoft-, Google-oder Yahoo-Identitäten für diese benutzerdefinierte Vorlage|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -SocialIdSignIn <$true|$false>` <br/> **Beispiele:** <br/>So aktivieren Sie soziale IDs für diese benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $true` <br/> So deaktivieren Sie soziale IDs für diese benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $false`|

## <a name="to-remove-brand-customizations-from-the-ome-portal-and-email-messages-encrypted-by-ome"></a>So entfernen Sie Marken Anpassungen aus dem OM-Portal und e-Mail-Nachrichten, die von OM verschlüsselt werden
  
1. [Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://aka.ms/exopowershell).

2. Verwenden Sie das Cmdlet **Set-OMEConfiguration** , wie in [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration)beschrieben. Wenn Sie die Branding-Anpassungen ihrer Organisation aus den DisclaimerText-, EmailText-und Portal Text-Werten entfernen möchten, legen Sie den Wert auf `""`eine leere Zeichenfolge fest. Legen Sie für alle Bildwerte, wie beispielsweise Logo, den `"$null"`Wert auf fest.

**Anpassungsoptionen für Verschlüsselung**

**Dieses Feature der Verschlüsselungserfahrung zu Standardtext und -bild zurücksetzen**|**Verwenden Sie diese Befehle**|
|:-----|:-----|
|Standardtext, der verschlüsselten E-Mail-Nachrichten beigefügt ist  <br/> Der Standardtext wird über den Anweisungen zum Betrachten von verschlüsselten Nachrichten angezeigt|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""`|
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""`|
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Beispiel Zurücksetzen auf Standard:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""`|
|Logo|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Beispiel Zurücksetzen auf Standard:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null`|
|Hintergrundfarbe|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Beispiel Zurücksetzen auf Standard:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null`|

## <a name="create-an-exchange-mail-flow-rule-that-applies-custom-branding-to-encrypted-emails"></a>Erstellen einer Exchange-Nachrichtenfluss Regel, die das benutzerdefinierte Branding auf verschlüsselte e-Mails anwendet

Nachdem Sie eine Branding-Vorlage erstellt haben, können Sie Exchange-Nachrichtenfluss Regeln erstellen, die das benutzerdefinierte Branding basierend auf bestimmten Bedingungen anwenden. Eine solche Regel wendet in den folgenden Szenarien ein benutzerdefiniertes Branding an:

- Wenn die e-Mail vom Endbenutzer manuell aus dem Outlook-oder Outlook im Web (früher als Outlook Web App bezeichnet)-Clients verschlüsselt wurde
- Wenn die e-Mail automatisch durch eine Exchange-Nachrichtenfluss Regel oder eine Office 365-Richtlinie zur verHinderung von Datenverlust verschlüsselt wurde

Informationen zum Erstellen einer Exchange-Nachrichtenfluss Regel, die die Verschlüsselung anwendet, finden Sie unter [Definieren von Nachrichtenfluss Regeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).

1. Melden Sie sich in einem Webbrowser bei einem Arbeits-oder Schulkonto, dem globale Administratorberechtigungen erteilt wurden, bei [Office 365 an](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Wählen Sie die Kachel **Admin** aus.

3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.

4. Wechseln Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln** , und wählen Sie **Neues** ![neues Symbol](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **Erstellen**aus. Weitere Informationen zur Verwendung der EAC finden Sie unter [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Geben Sie unter **Name**einen Namen für die Regel ein, beispielsweise Branding für die Vertriebsabteilung.

6. Wählen Sie unter **diese Regel anwenden, wenn** wählen Sie eine Bedingung aus die Bedingung aus, **die der Absender in der Organisation** und andere Bedingungen aus der Liste der verfügbaren Bedingungen befindet. Sie können beispielsweise eine bestimmte Branding-Vorlage auf Folgendes anwenden:

     - Alle verschlüsselten e-Mails, die von Mitgliedern der Finanzabteilung gesendet wurden
     - VerSchlüsselte e-Mails, die mit einem bestimmten Stichwort gesendet werden, beispielsweise "extern" oder "Partner"
     - VerSchlüsselte e-Mails, die an eine bestimmte Domäne gesendet werden

7. Wählen Sie unter **folgende Aktion** **die Option Nachrichtensicherheit** > **anwenden auf benutzerdefiniertes Branding auf OM-Nachrichten**aus. Wählen Sie als nächstes aus der Dropdownliste eine Branding-Vorlage aus den von Ihnen erstellten aus.
8. Optional Wenn Sie möchten, dass die Nachrichtenfluss Regel zusätzlich zu dem benutzerdefinierten Branding auch die Verschlüsselung angewendet **** wird, wählen Sie die Option **Nachrichtensicherheit ändern** aus, und wählen Sie dann **Office 365 Nachrichtenverschlüsselung und Rechte Schutz anwenden**aus. Wählen Sie in der Liste eine RMS-Vorlage aus, klicken Sie auf **Speichern**und dann auf **OK**.
  
     Die Liste der Vorlagen enthält alle Standardvorlagen und-Optionen sowie alle benutzerdefinierten Vorlagen, die Sie für Office 365 erstellt haben. Wenn die Liste leer ist, stellen Sie sicher, dass Sie die Office 365-Nachrichtenverschlüsselung mit den neuen Funktionen eingerichtet haben, wie unter [Einrichten der neuen Office 365-Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md)beschrieben. Informationen zu den Standardvorlagen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Informationen zur Option " **nicht weiterleiten** " finden Sie unter [do not Forward Option for Emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Informationen zur Option **nur** verschlüsseln finden Sie unter [Encrypt only Option for Emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

     Wenn Sie eine andere Aktion angeben möchten, können Sie **Aktion hinzufügen** auswählen.
