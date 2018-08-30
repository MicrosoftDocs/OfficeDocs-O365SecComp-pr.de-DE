---
title: Hinzufügen von Ihrer Organisation Marke auf verschlüsselten Nachrichten
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 11/2/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 7a29260d-2959-42aa-8916-feceff6ee51d
description: 'Als Exchange-Administrator können Sie Ihrer Organisation branding zu verschlüsselten e-Mail-Nachrichten von Ihrer Organisation und den Inhalt des Portals Verschlüsselung anwenden. '
ms.openlocfilehash: 2f34b5cea3155f587fd7787f1f69270d1373400b
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529469"
---
# <a name="add-your-organizations-brand-to-your-encrypted-messages"></a>Hinzufügen von Marke Ihres Unternehmens zu Ihrer verschlüsselten Nachrichten

Als Exchange Online oder Exchange Online Protection-Administrator können Sie Ihr Unternehmen zum Anpassen der Darstellung von Office 365 Message Encryption-e-Mails für Ihre Organisation und den Inhalt des Portals Verschlüsselung branding anwenden. Get-OMEConfiguration und Set-OMEConfiguration Windows PowerShell-Cmdlets können Sie die folgenden Aspekte des die Anzeigequalität für Empfänger von verschlüsselten e-Mail-Nachrichten anpassen:
  
- Einleitender Text der E-Mail, die die verschlüsselte Nachricht enthält
    
- Text des Haftungsausschlusses der E-Mail, die die verschlüsselte Nachricht enthält
    
- Text, der im OME-Portal angezeigt.
    
- Logo, die in der e-Mail-Nachricht und die OME-Portal angezeigt wird
    
- Hintergrundfarbe in der e-Mail-Nachricht und die OME-portal
    
Sie können auch jederzeit zum Standardaussehen und -verhalten zurückkehren.
  
||
|:-----|
|Dieser Artikel ist Teil einer größeren Reihe von Artikeln zur Office 365 Message Encryption. In diesem Artikel ist für Administratoren und IT-Fachleute vorgesehen. Wenn Sie sich gerade befinden Suchen nach Informationen zu senden oder Empfangen einer verschlüsselten Nachricht, finden Sie in der Liste der Artikel in [Office 365 Message Encryption (OME)](ome.md) , und suchen Sie im Artikel, der am besten Ihren Anforderungen entspricht. |
||
   
**Zum Anpassen der Darstellung der OME Portal und e-Mail-Nachrichten von OME mit Ihrer Organisation Marke verschlüsselt**
  
1. Verbindung mit Exchange Online mithilfe von Remote-PowerShell, wie beschrieben in [Verbindung mit Exchange Online Using Remote PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).
    
2. Verwenden Sie das Cmdlet Set-OMEConfiguration, wie beschrieben in [Set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) oder anhand der folgenden Tabelle Hinweise. 
    
**Anpassungsoptionen für Verschlüsselung**

|**So passen Sie dieses Verschlüsselungsfeature an**|**Verwenden Sie diese Befehle**|
|:-----|:-----|
|Standardtext, der verschlüsselten e-Mail-Nachrichten beigefügt ist. Der Standardtext wird über den Anweisungen zum Betrachten von verschlüsselten Nachrichten angezeigt.  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<String up to 1024 characters>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system."`|
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -DisclaimerText "<Disclaimer statement. String of up to 1024 characters.>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only."` <br/> |
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt<br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<Text for your portal. String of up to 128 characters.>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal."` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Unterstützte Dateiformate: .png, .jpg, .bmp oder .tiff  <br/> Optimale Größe der Logodatei: kleiner als 40 KB  <br/> Optimale Abmessungen des Logobilds: 170 x 70 Pixel  <br/> |
|Hintergrundfarbe  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor "<Hexadecimal color code>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -BackgroundColor "#ffffff"` <br/> |
   
**So entfernen Sie Marke Anpassungen aus der OME Portal und e-Mail-Nachrichten von OME verschlüsselt**
  
1. Verbindung mit Exchange Online mithilfe von Remote-PowerShell, wie beschrieben in [Verbindung mit Exchange Online Using Remote PowerShell](http://technet.microsoft.com/library/jj984289%28v=exchg.150%29.aspx).
    
2. Verwenden Sie das Cmdlet Set-OMEConfiguration, wie in [Set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b)beschrieben. Ihrer Organisation Entfernen der Anpassungen aus der DisclaimerText emailText fest, Branding und PortalText Werte, legen Sie den Wert auf eine leere Zeichenfolge, `""`. Für alle Werte wie Logo, Abbild legen Sie den Wert auf `"$null"`.
    
**Anpassungsoptionen für Verschlüsselung**

**Dieses Feature der Verschlüsselungserfahrung zu Standardtext und -bild zurücksetzen**|**Verwenden Sie diese Befehle**|
|:-----|:-----|
|Standardtext, der verschlüsselten E-Mail-Nachrichten beigefügt ist  <br/> Der Standardtext wird über den Anweisungen zum Betrachten von verschlüsselten Nachrichten angezeigt  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Beispiel:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Beispiel wechseln auf den Standardwert:** <br/>  `Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Beispiel wechseln auf den Standardwert:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
|Hintergrundfarbe  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -BackgroundColor <"$null">` <br/> **Beispiel wechseln auf den Standardwert:** <br/>  `Set-OMEConfiguration -Identity "OME configuration" -BackgroundColor $null` <br/> |
   

