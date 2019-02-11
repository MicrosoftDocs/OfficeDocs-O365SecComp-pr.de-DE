---
title: Hinzufügen von Ihrer Organisation Marke auf verschlüsselten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: Als Exchange-Administrator können Sie Ihrer Organisation branding zu verschlüsselten e-Mail-Nachrichten von Ihrer Organisation und den Inhalt des Portals Verschlüsselung anwenden.
ms.openlocfilehash: 4b22b72a8b77c2978a7cf25166978759119c272c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29696219"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Hinzufügen der Marke Ihres Unternehmens zu Ihren verschlüsselten Nachrichten

Als Exchange Online oder Exchange Online Protection-Administrator können Sie Ihr Unternehmen zum Anpassen der Darstellung von Office 365 Message Encryption-e-Mails für Ihre Organisation und den Inhalt des Portals Verschlüsselung branding anwenden. Get-OMEConfiguration und Set-OMEConfiguration Windows PowerShell-Cmdlets können Sie die folgenden Aspekte des die Anzeigequalität für Empfänger von verschlüsselten e-Mail-Nachrichten anpassen:
  
- Einleitender Text der E-Mail, die die verschlüsselte Nachricht enthält
- Text des Haftungsausschlusses der E-Mail, die die verschlüsselte Nachricht enthält
- Text, der im OME-Portal angezeigt.
- Logo, die in der e-Mail-Nachricht und die OME-Portal angezeigt wird
- Hintergrundfarbe in der e-Mail-Nachricht und die OME-portal

Sie können auch jederzeit zum Standardaussehen und -verhalten zurückkehren.

Wenn Sie mehr Kontrolle erhalten möchten, können Sie mehrere Vorlagen für verschlüsselte e-Mails, die aus Ihrer Organisation stammen erstellen. Mithilfe von Vorlagen, können Sie mehr als nur das Aussehen und Verhalten von e-Mail-Nachrichten steuern, sondern auch Steuerelement Teile der durch den Endbenutzer. Beispielsweise können Sie angeben, ob die Empfänger der e-Mail-Nachrichten, die diese Vorlage angewendet haben, und wer Google, Yahoo! und Microsoft Accounts verwenden, diese Konten verwenden können, zur Anmeldung bei Office 365 Message Encryption-Portal oder nicht. Vorlagen können Sie verschiedene Anwendungsfälle, z. B. erfüllen:

- Vorlagen für jede Abteilung, z. B. Finance, Sales.
- Vorlagen für verschiedene Produkte
- Vorlagen für verschiedene geographische Regionen oder Ländern

Nach dem Erstellen der Vorlagen können Sie diese mithilfe von Exchange e-Mail-Flussregeln auf verschlüsselte e-Mails anwenden. Alle e-Mails, die mithilfe dieser Vorlagen Branding sind können gesperrt werden.
  
||
|:-----|
|Dieser Artikel ist Teil einer größeren Reihe von Artikeln zur Office 365 Message Encryption. In diesem Artikel ist für Administratoren und IT-Fachleute vorgesehen. Wenn Sie sich gerade befinden Suchen nach Informationen zu senden oder Empfangen einer verschlüsselten Nachricht, finden Sie in der Liste der Artikel in [Office 365 Message Encryption (OME)](ome.md) , und suchen Sie im Artikel, der am besten Ihren Anforderungen entspricht. |
||

## <a name="create-branding-templates"></a>Branding Vorlagen erstellen

Sie erstellen branding Vorlagen für Ihre Organisation in Windows PowerShell mit dem Cmdlet New-OMEConfiguration. Nachdem Sie die Vorlage erstellt haben, definieren Sie die Teile der Vorlage mithilfe des Cmdlets Set-OMEConfiguration. Sie können mehrere Vorlagen erstellen.

![Anpassbare e-Mail-Webparts](media/ome-template-breakout.png)
  
1. Verwenden ein Arbeit oder Schule Konto, die in Office 365-Organisation über globaler Administrator-Berechtigungen verfügt, eine Windows PowerShell-Sitzung zu starten und eine Verbindung mit Exchange Online. Anweisungen finden Sie unter [Connect to Exchange Online PowerShell](https://aka.ms/exopowershell).

2. Verwenden Sie das Cmdlet "New-OMEConfiguration", um eine neue Vorlage zu erstellen.
     ```powershell
     New-OMEConfiguration -Identity <OMEConfigurationIdParameter>
     ```
     Beispiel:
     ```powershell
     New-OMEConfiguration -Identity <Branding template 1>
     ```
3. Definieren Sie die Anpassungen für die Vorlage, die Sie soeben definiert haben, mithilfe des Cmdlets Set-OMEConfiguration, wie beschrieben in [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration) oder anhand der folgenden Tabelle Hinweise.

|**So passen Sie dieses Verschlüsselungsfeature an**|**Verwenden Sie diese Befehle**|
|:-----|:-----|
|Hintergrundfarbe  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -BackgroundColor "#ffffff"` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Unterstützte Dateiformate: .png, .jpg, .bmp oder .tiff  <br/> Optimale Größe der Logodatei: kleiner als 40 KB  <br/> Optimale Abmessungen des Logobilds: 170 x 70 Pixel  <br/> |
|Text neben Name und e-Mail-Adresse des Absenders| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -IntroductionText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -IntroductionText "has sent you a secure message."`|
|Text, der auf die Schaltfläche "Nachricht lesen" angezeigt wird| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -ReadButtonText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -ReadButtonText "Read Secure Message."`|
|Text, der über unterhalb der Schaltfläche "Nachricht lesen" angezeigt wird.| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -DisclaimerText "This message is confidential for the use of the addressee only."`|
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|So aktivieren oder Deaktivieren der Authentifizierung mit eine einmalige Kennung für diese benutzerdefinierte Vorlage| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -OTPEnabled <$true|$false>` <br/> **Beispiele:** <br/>So aktivieren Sie einmalige teilnehmerkennungen für dieses benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $true` <br/> So deaktivieren Sie einmalige teilnehmerkennungen für dieses benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -OTPEnabled $false`|
|Aktivieren oder Deaktivieren der Authentifizierung mit Microsoft, Google und Yahoo Identitäten für dieses benutzerdefinierte Vorlage| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -SocialIdSignIn <$true|$false>` <br/> **Beispiele:** <br/>So aktivieren Sie für soziale Netzwerke-IDs für dieses benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $true` <br/> So deaktivieren Sie soziale-IDs für dieses benutzerdefinierte Vorlage <br/>  `Set-OMEConfiguration -Identity "Branding Template 1" -SocialIdSignIn $false`|

## <a name="to-remove-brand-customizations-from-the-ome-portal-and-email-messages-encrypted-by-ome"></a>So entfernen Sie Marke Anpassungen aus der OME Portal und e-Mail-Nachrichten von OME verschlüsselt
  
1. [Stellen Sie eine Verbindung mit Exchange Online PowerShell her](https://aka.ms/exopowershell).

2. Verwenden Sie das Cmdlet Set-OMEConfiguration, wie in [Set-OMEConfiguration](https://docs.microsoft.com/powershell/module/exchange/encryption-and-certificates/Set-OMEConfiguration)beschrieben. Ihrer Organisation Entfernen der Anpassungen aus der DisclaimerText emailText fest, Branding und PortalText Werte, legen Sie den Wert auf eine leere Zeichenfolge, `""`. Für alle Werte wie Logo, Abbild legen Sie den Wert auf `"$null"`.

**Anpassungsoptionen für Verschlüsselung**

**Dieses Feature der Verschlüsselungserfahrung zu Standardtext und -bild zurücksetzen**|**Verwenden Sie diese Befehle**|
|:-----|:-----|
|Standardtext, der verschlüsselten E-Mail-Nachrichten beigefügt ist  <br/> Der Standardtext wird über den Anweisungen zum Betrachten von verschlüsselten Nachrichten angezeigt| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""`|
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""`|
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Beispiel wechseln auf den Standardwert:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logo| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Beispiel wechseln auf den Standardwert:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null`|
|Hintergrundfarbe| `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Beispiel wechseln auf den Standardwert:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null`|

## <a name="create-an-exchange-mail-flow-rule-that-applies-custom-branding-to-encrypted-emails"></a>Erstellen einer Exchange Mail Flow-Regel, die gilt benutzerdefiniertem branding auf verschlüsselte e-Mails

Nachdem Sie eine-branding-Vorlage erstellt haben, können Sie Exchange Mail Flow Regeln gelten, benutzerdefiniertes branding erstellen basierend auf bestimmten Umständen. Eine solche Regel wird Anwenden von benutzerdefiniertem branding in den folgenden Szenarien:

- Wenn die e-Mail-Nachricht manuell durch den Endbenutzer von Outlook oder OWA-Clients verschlüsselt wurde
- Wenn die e-Mail von einem Exchange Mail Flow Regel oder Office 365 Data Loss Prevention Richtlinie automatisch verschlüsselt wurde

Informationen zum Erstellen einer Exchange Mail Flow-Regel, die Verschlüsselung angewendet wird, finden Sie unter [Definieren von e-Mail-Flussregeln zum Verschlüsseln von e-Mail-Nachrichten in Office 365](define-mail-flow-rules-to-encrypt-email.md).

1. In einem Webbrowser unter Verwendung eines Kontos arbeiten oder Schule, die [Anmeldung an Office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426#ID0EAABAAA=Web_browser)globaler Administrator-Berechtigungen erteilt wurden.

2. Wählen Sie die Kachel " **Admin** ".

3. Wählen Sie im Office 365 Admin Center die Optionen **Admin** \> **Exchange**.

4. Navigieren Sie in der Exchange-Verwaltungskonsole zu **Nachrichtenfluss** \> **Regeln** , und wählen Sie **New** ![New Icon](media/457cd93f-22c2-4571-9f83-1b129bcfb58e.gif) \> **neue Regel erstellen**. Weitere Informationen zum Verwenden der Exchange-Verwaltungskonsole finden Sie unter [Exchange-Verwaltungskonsole in Exchange Online](https://docs.microsoft.com/exchange/exchange-admin-center).

5. Geben Sie im Feld **Name**einen Namen für die Regel ein, beispielsweise Branding für Ihre IT-Abteilung.

6. Wählen Sie in **diese Regel anwenden, wenn** eine Bedingung aus, wählen Sie aus der Liste verfügbarer Bedingungen die Bedingung **der Absender befindet sich innerhalb der Organisation** sowie weitere gewünschte Optionen aus. Angenommen, möchten Sie eine bestimmte branding-Vorlage zum anwenden:

     - Alle verschlüsselten in Elemente von der Finanzabteilung gesendete e-Mails
     - Verschlüsselte e-Mails mit einem bestimmten Schlüsselwort wie "External" oder "Partner"
     - Verschlüsselte e-Mails an eine bestimmte Domäne gesendet

7. Wählen Sie **die folgenden Schritte aus**, **nachrichtensicherheit ändern** > **Anwenden von benutzerdefiniertem branding auf OME Nachrichten**. Wählen Sie dann aus der Dropdownliste eine-branding-Vorlage aus, die Sie erstellt haben.
8. (Optional) Wenn Sie die e-Mail-Flussregel auch Verschlüsselung zusätzlich zu den benutzerdefinierten anwenden möchten branding, **Gehen Sie folgendermaßen vor**, wählen Sie **nachrichtensicherheit ändern** und dann **Office 365-Nachrichtenverschlüsselung anwenden und Schutzrechte**. Wählen Sie eine RMS-Vorlage aus der Liste aus, wählen Sie **Speichern**, und wählen Sie dann auf **OK**.
  
     Die Liste der Vorlagen enthält alle Standardvorlagen und Optionen sowie die von denen Ihnen für erstellten benutzerdefinierten Vorlagen von Office 365 verwenden. Wenn die Liste leer ist, stellen Sie sicher, dass Sie Office 365 Message Encryption mit den neuen Funktionen eingerichtet haben wie unter [Set up neuen Funktionen von Office 365 Message Encryption](set-up-new-message-encryption-capabilities.md)beschrieben. Informationen zu den standardmäßigen Vorlagen finden Sie unter [Konfigurieren und Verwalten von Vorlagen für Azure Information Protection](https://docs.microsoft.com/information-protection/deploy-use/configure-policy-templates). Informationen über die Option **Nicht weiterleiten** finden Sie unter [nicht weiterleiten Option-e-Mails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#do-not-forward-option-for-emails). Informationen über die Option **nur zu verschlüsseln** finden Sie unter [Verschlüsseln nur die Option-e-Mails](https://docs.microsoft.com/information-protection/deploy-use/configure-usage-rights#encrypt-only-option-for-emails).

     Sie können **Aktion hinzufügen** auswählen, wenn Sie eine andere Aktion angeben möchten.
