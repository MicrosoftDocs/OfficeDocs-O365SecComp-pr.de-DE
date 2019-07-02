---
title: Hinzufügen Ihrer Unternehmensmarke zu verschlüsselten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.date: 4/30/2019
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: Als Office 365 globaler Administrator können Sie das Branding Ihrer Organisation auf die verschlüsselten e-Mail-Nachrichten Ihrer Organisation und auf den Inhalt des Verschlüsselungs Portals anwenden.
ms.openlocfilehash: 19f227971c522f9d92aec343f1865ab7f23c13aa
ms.sourcegitcommit: b0ea2d66bc4c7f2fc0a8abab28d2ae652b1c4b73
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2019
ms.locfileid: "34721372"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Hinzufügen der Marke Ihres Unternehmens zu Ihren verschlüsselten Nachrichten

Als Exchange Online-oder Exchange Online Protection-Administrator können Sie Ihr Firmenbranding anwenden, um das Aussehen der e-Mail-Nachrichten der Office 365 Nachrichtenverschlüsselung Ihrer Organisation und den Inhalt des Verschlüsselungs Portals anzupassen. Mithilfe der Cmdlets "Get-OMEConfiguration" und "OMEConfiguration Windows PowerShell" können Sie die folgenden Aspekte der Anzeige Erfahrung für Empfänger von verschlüsselten e-Mail-Nachrichten anpassen:
  
- Einleitender Text der E-Mail, die die verschlüsselte Nachricht enthält

- Text des Haftungsausschlusses der E-Mail, die die verschlüsselte Nachricht enthält

- Text, der im OM-Portal angezeigt wird

- Logo, das in der e-Mail-Nachricht und im OM-Portal angezeigt wird

- Hintergrundfarbe in der e-Mail-Nachricht und im OM-Portal

Sie können auch jederzeit zum Standardaussehen und -verhalten zurückkehren.

 Wenn Sie mehr Kontrolle wünschen, können Sie Office 365 erweiterte Nachrichtenverschlüsselung verwenden und mehrere Vorlagen für verschlüsselte e-Mails erstellen, die von Ihrer Organisation stammen. Mithilfe dieser Vorlagen können Sie mehr als nur das Aussehen und Verhalten der e-Mail-Nachrichten steuern, aber auch Teile der Endbenutzeroberfläche steuern. Sie können beispielsweise angeben, ob Empfänger von e-Mails, auf die diese Vorlage angewendet wird, und wer Google, Yahoo und Microsoft-Konten verwendet, diese Konten zum Anmelden beim Office 365 Nachrichten Verschlüsselungs Portal verwenden können. Sie können Vorlagen verwenden, um mehrere Anwendungsfälle zu erfüllen, beispielsweise:

- Vorlagen für jede Abteilung, beispielsweise Finanzen, Vertrieb usw.

- Vorlagen für verschiedene Produkte

- Vorlagen für unterschiedliche geographische Regionen oder Länder

- Unabhängig davon, ob Sie das Widerrufen von e-Mails zulassen möchten

- Gibt an, ob e-Mail-Nachrichten, die an externe Empfänger gesendet werden, nach einer bestimmten Anzahl von Tagen ablaufen sollen.

Nachdem Sie die Vorlagen erstellt haben, können Sie Sie mithilfe von Exchange-Nachrichtenfluss Regeln auf verschlüsselte e-Mail-Nachrichten anwenden. Wenn Sie Office 365 erweiterte Nachrichtenverschlüsselung haben, können Sie jede e-Mail-Nachricht widerrufen, die Sie mit diesen Vorlagen gebrandmarkt haben.
  
||
|:-----|
|Dieser Artikel ist Teil einer größeren Reihe von Artikeln über Office 365 Nachrichtenverschlüsselung. Dieser Artikel richtet sich an Administratoren und ITPros. Wenn Sie nur auf der Suche nach Informationen zum Senden oder Empfangen einer verschlüsselten Nachricht sind, lesen Sie die Artikelliste in [Office 365 Nachrichtenverschlüsselung (OM)](ome.md) , und suchen Sie nach dem Artikel, der Ihren Anforderungen am besten entspricht.|
||

## <a name="create-branding-templates"></a>Erstellen von Branding-Vorlagen

Sie erstellen Branding-Vorlagen für Ihre Organisation in Windows PowerShell mit dem New-OMEConfiguration-Cmdlet. Nachdem Sie die Vorlage erstellt haben, definieren Sie die Teile der Vorlage mithilfe des Cmdlets "OMEConfiguration". Sie können mehrere Vorlagen erstellen.

![Anpassbare e-Mail-Teile](media/ome-template-breakout.png)
  
1. Verwenden Sie ein Arbeits-oder Schulkonto, das über globale Administratorberechtigungen in Ihrer Office 365 Organisation verfügt, starten Sie eine Windows PowerShell Sitzung, und stellen Sie eine Verbindung mit Exchange Online her. Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Verwenden Sie das Cmdlet New-OMEConfiguration, um eine neue Vorlage zu erstellen.

   ```powershell
   New-OMEConfiguration -Identity <OMEConfigurationIdParameter>
   ```

   For example,

   ```powershell
   New-OMEConfiguration -Identity "Branding template 1"
   ```

3. Definieren Sie die Anpassungen für die soeben definierte Vorlage mithilfe des Cmdlets "OMEConfiguration" wie unter " [festlegen-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration) " beschrieben, oder verwenden Sie die folgende Tabelle, um Anleitungen zu erstellen.

|**So passen Sie dieses Verschlüsselungsfeature an**|**Verwenden Sie diese Befehle**|
|:-----|:-----|
|Hintergrundfarbe|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -BackgroundColor "#ffffff"`|
|Logo|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Unterstützte Dateiformate: .png, .jpg, .bmp oder .tiff  <br/> Optimale Größe der Logodatei: kleiner als 40 KB  <br/> Optimale Abmessungen des Logobilds: 170 x 70 Pixel|
|Text neben dem Namen und der e-Mail-Adresse des Absenders|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -IntroductionText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -IntroductionText "has sent you a secure message."`|
|Text, der auf der Schaltfläche "Nachricht lesen" angezeigt wird|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -ReadButtonText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -ReadButtonText "Read Secure Message."`|
|Text, der oberhalb der Schaltfläche "Nachricht lesen" angezeigt wird|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -DisclaimerText "This message is confidential for the use of the addressee only."`|
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."`|
|So aktivieren oder deaktivieren Sie die Authentifizierung mithilfe eines einmaligen Pass Codes für diese benutzerdefinierte Vorlage|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -OTPEnabled <$true|$false>` <br/> **Beispiele:** <br/>So aktivieren Sie einmalige Kennwörter für diese benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $true` <br/> So deaktivieren Sie einmalige Kennwörter für diese benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $false`|
|So aktivieren oder deaktivieren Sie die Authentifizierung mit Microsoft-, Google-oder Yahoo-Identitäten für diese benutzerdefinierte Vorlage|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -SocialIdSignIn <$true|$false>` <br/> **Beispiele:** <br/>So aktivieren Sie soziale IDs für diese benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $true` <br/> So deaktivieren Sie soziale IDs für diese benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $false`|

## <a name="to-remove-brand-customizations-from-the-ome-portal-and-email-messages-encrypted-by-ome"></a>So entfernen Sie Marken Anpassungen aus dem OM-Portal und von OM verschlüsselte e-Mail-Nachrichten
  
1. [Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://aka.ms/exopowershell).

2. Verwenden Sie das Cmdlet " **OMEConfiguration** " wie unter " [festlegen-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration)" beschrieben. Wenn Sie die Marken Anpassungen ihrer Organisation aus den DisclaimerText-, EmailText-und Portal Text-Werten entfernen möchten, legen Sie den Wert auf eine `""`leere Zeichenfolge fest. Legen Sie für alle Bild Werte wie Logo den Wert auf `"$null"`fest.

**Anpassungsoptionen für Verschlüsselung**

**Dieses Feature der Verschlüsselungserfahrung zu Standardtext und -bild zurücksetzen**|**Verwenden Sie diese Befehle**|
|:-----|:-----|
|Standardtext, der verschlüsselten E-Mail-Nachrichten beigefügt ist  <br/> Der Standardtext wird über den Anweisungen zum Betrachten von verschlüsselten Nachrichten angezeigt|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""`|
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""`|
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Beispiel Zurücksetzen auf Standard:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""`|
|Logo|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Beispiel Zurücksetzen auf Standard:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null`|
|Hintergrundfarbe|`Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Beispiel Zurücksetzen auf Standard:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null`|

## <a name="create-an-exchange-mail-flow-rule-that-applies-custom-branding-to-encrypted-emails"></a>Erstellen einer Exchange-Nachrichtenfluss Regel, die benutzerdefiniertes Branding auf verschlüsselte e-Mails anwendet

Nachdem Sie eine Branding-Vorlage erstellt haben, können Sie Exchange-Nachrichtenfluss Regeln erstellen, um das benutzerdefinierte Branding auf der Grundlage bestimmter Bedingungen anzuwenden. In den folgenden Szenarien wird eine solche Regel benutzerdefiniertes Branding anwenden:

- Wenn die e-Mail manuell vom Endbenutzer aus dem Outlook oder Outlook im Internet (früher als Outlook Web App bezeichnet)-Clients verschlüsselt wurde

- Wenn die e-Mail-Nachricht automatisch von einer Exchange-Nachrichtenfluss Regel oder Office 365 Richtlinie zur Verhinderung von Datenverlusten verschlüsselt wurde

Informationen zum Erstellen einer Exchange-Nachrichtenfluss Regel, die Verschlüsselung zutrifft, finden Sie unter [define Mail Flow Rules to encrypt Email Messages in Office 365](define-mail-flow-rules-to-encrypt-email.md).

1. Melden Sie sich in einem Webbrowser mit einem Arbeits-oder Schulkonto, dem globale Administratorberechtigungen erteilt wurden, bei [Office 365 an](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser).

2. Wählen Sie die Kachel **Admin** aus.

3. Wählen Sie im Office 365 Admin Center die Option **Admin** \> Center **Exchange**aus.

4. Wechseln Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln** , und](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> wählen Sie **Neues** ![neues Symbol neue **Regel erstellen**aus. Weitere Informationen zur Verwendung der Exchange-Verwaltungskonsole finden Sie unter [Exchange Admin Center in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Geben Sie unter **Name**einen Namen für die Regel ein, beispielsweise Branding für die Vertriebsabteilung.

6. Wählen Sie unter **diese Regel anwenden, wenn** eine Bedingung auswählen die Bedingung aus, in der sich **der Absender innerhalb der Organisation befindet** , sowie in der Liste der verfügbaren Bedingungen weitere Bedingungen. Beispielsweise können Sie eine bestimmte Branding-Vorlage auf Folgendes anwenden:

     - Alle verschlüsselten e-Mails, die von Mitgliedern der Finanzabteilung gesendet wurden
     - Verschlüsselte e-Mails, die mit einem bestimmten Schlüsselwort wie "extern" oder "Partner" gesendet werden
     - Verschlüsselte e-Mails, die an eine bestimmte Domäne gesendet werden

7. Wählen Sie unter **gehen Sie wie folgt**vor die Option **Nachrichtensicherheit** > **anwenden benutzerdefiniertes Branding auf OM-Nachrichten**ändern aus. Wählen Sie dann in der Dropdownliste eine Branding-Vorlage aus denen aus, die Sie erstellt haben.

8. Optional Wenn die e-Mail-Fluss Regel zusätzlich zum benutzerdefinierten Branding auch die Verschlüsselung anwenden soll, **** wählen Sie die Option **Nachrichtensicherheit ändern** aus, und wählen Sie dann **Office 365 Nachrichtenverschlüsselung und Rechte Schutz anwenden**aus. Wählen Sie in der Liste eine RMS-Vorlage aus, wählen Sie **Speichern**aus, und klicken Sie dann auf **OK**.
  
     Die Liste der Vorlagen enthält alle Standardvorlagen und-Optionen sowie benutzerdefinierte Vorlagen, die Sie zur Verwendung durch Office 365 erstellt haben. Wenn die Liste leer ist, stellen Sie sicher, dass Sie Office 365 Nachrichtenverschlüsselung mit den neuen Funktionen eingerichtet haben, wie unter [Einrichten neuer Office 365 Nachrichten Verschlüsselungsfunktionen](set-up-new-message-encryption-capabilities.md)beschrieben. Informationen zu den Standardvorlagen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Informationen zur Option " **nicht weiterleiten** " finden Sie unter [do not Forward Option for Emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Informationen zur Option **nur** verschlüsseln finden Sie unter Verschlüsseln [nur Option for Emails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

     Sie können die Option **Aktion hinzufügen** auswählen, wenn Sie eine andere Aktion angeben möchten.
