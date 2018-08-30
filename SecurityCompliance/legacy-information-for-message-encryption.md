---
title: Legacy-Informationen für Office 365-Nachrichtenverschlüsselung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 1/4/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
ms.assetid: 5986b9e1-c824-4f8f-9b7d-a2b0ae2a7fe9
description: Wenn Sie noch nicht Office 365-Organisation noch auf die neuen Funktionen OME verschoben, aber Sie OME bereits bereitgestellt haben, beziehen sich die Informationen in diesem Artikel zu Ihrer Organisation. Microsoft empfiehlt, stellen Sie einen Plan für die in der neuen OME-Funktionen zu verschieben, wie es für Ihre Organisation angemessen ist. Anweisungen finden Sie unter Set up neue Office 365 Message Encryption-Funktionen, die auf der Basis Azure Information Protection. Wenn Sie erfahren Sie mehr über die neuen Funktionen wie zuerst arbeiten möchten, finden Sie unter Office 365 Message Encryption. Der Rest dieses Artikels bezieht sich auf OME Verhalten vor der Veröffentlichung der neuen OME-Funktionen.
ms.openlocfilehash: d5b21cbe0004ca7bda38085bd5d8ef5f2a22b04e
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529537"
---
# <a name="legacy-information-for-office-365-message-encryption"></a>Legacy-Informationen für Office 365-Nachrichtenverschlüsselung

Wenn Sie noch nicht Office 365-Organisation noch auf die neuen Funktionen OME verschoben, aber Sie OME bereits bereitgestellt haben, beziehen sich die Informationen in diesem Artikel zu Ihrer Organisation. Microsoft empfiehlt, stellen Sie einen Plan für die in der neuen OME-Funktionen zu verschieben, wie es für Ihre Organisation angemessen ist. Anweisungen finden Sie unter [Einrichten von neuen Office 365 Message Encryption-Funktionen, die auf der Basis Azure Information Protection](set-up-new-message-encryption-capabilities.md). Wenn Sie erfahren Sie mehr über die neuen Funktionen wie zuerst arbeiten möchten, finden Sie unter [Office 365 Message Encryption](ome.md). Der Rest dieses Artikels bezieht sich auf OME Verhalten vor der Veröffentlichung der neuen OME-Funktionen.
  
Mit Office 365 Message Encryption kann Ihre Organisation senden und Empfangen von verschlüsselten e-Mail-Nachrichten zwischen Personen innerhalb und außerhalb Ihrer Organisation. Office 365 arbeitet Message Encryption mit Outlook.com, Yahoo, Google Mail und anderen e-Mail-Dienste. E-Mail-nachrichtenverschlüsselung können Sie sicherstellen, die lediglich Empfänger kann Nachrichteninhalt anzeigen.
  
Es folgen einige Beispiele:
  
- Ein Bankangestellter sendet kreditkartenabrechnungen an Kunden
    
- Eine Versicherungsgesellschaft Vertreter enthält Details zur Richtlinie für Kunden
    
- Ein Hypothekenrechner Broker fordert Finanzinformationen von einem Kunden für einen Darlehensantrag
    
- Ein gesundheitspflegeversorger sendet Gesundheitsinformationen an Patienten
    
- Ein Anwalt sendet vertrauliche Informationen zu einem Kunden oder einen anderen Anwalt
    
## <a name="how-office-365-message-encryption-works-without-the-new-capabilities"></a>Funktionsweise von Office 365 Message Encryption ohne die neuen Funktionen

Office 365-Nachrichtenverschlüsselung ist ein Onlinedienst, der auf Microsoft Azure-Rechteverwaltung (RMS Azure) basiert. Azure-RMS können Administratoren Mail Flow Regeln zum Bestimmen der Bedingungen für die Verschlüsselung definieren. Beispielsweise kann eine Regel die Verschlüsselung aller Nachrichten an einen bestimmten Empfänger adressiert ist erforderlich.
  
In diesem kurzen Video, finden Sie unter Funktionsweise von Office 365 Message Encryption ohne die neuen Funktionen.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/c55540e7-f7f0-42f5-b254-4b2d2fbb1d63?autoplay=false]
  
Wenn Ihnen jemand eine e-Mail-Nachricht im Exchange Online sendet, die eine Verschlüsselungsregel übereinstimmt, wird die Nachricht mit einer HTML-Anlage gesendet. Der Empfänger öffnet den HTML-Anhang und folgt Anweisungen, um die verschlüsselte Nachricht auf dem Office 365 Message Encryption Portal anzeigen. Der Empfänger kann auswählen, um die Nachricht durch ein Microsoft-Konto oder eine Arbeit oder Schule zugeordnet Office 365 anmelden oder mithilfe einer einmaligen Kennung anzuzeigen. Beide Optionen können Sie sicherstellen, dass nur der beabsichtigte Empfänger die verschlüsselte Nachricht anzeigen kann. Dieser Prozess unterscheidet sich für die neuen OME-Funktionen.
  
Im folgenden Diagramm wird die Weitergabe einer E-Mail-Nachricht durch den Verschlüsselungs- und Entschlüsselungsvorgang zusammengefasst.
  
![Diagramm mit dem Pfad einer verschlüsselten E-Mail](media/O365-Office365MessageEncryption-Concept.png)
  
Weitere Informationen finden Sie unter [Serviceinformationen für die Vorversion Office 365 Message Encryption vor der Veröffentlichung der neuen OME-Funktionen](legacy-information-for-message-encryption.md#LegacyServiceInfo).
  
## <a name="defining-mail-flow-rules-for-office-365-message-encryption-that-dont-use-the-new-ome-capabilities"></a>Definieren von e-Mail-Flussregeln für Office 365 Message Encryption, die die neuen OME-Funktionen nicht verwenden

Um Office 365 Message Encryption ohne die neuen Funktionen zu aktivieren, definieren Sie Exchange Online und Exchange Online Protection-Administratoren Exchange Mail Flow Regeln. Diese Regeln bestimmen, unter welchen Bedingungen e-Mail-Nachrichten verschlüsselt werden soll, sowie die Bedingungen zum Entfernen der nachrichtenverschlüsselung. Wenn eine Verschlüsselung-Aktion für eine Regel festgelegt ist, werden alle Nachrichten, die die regelbedingungen entsprechen vor dem Senden sind verschlüsselt.
  
E-Mail-Flussregeln sind flexibel, sodass Bedingungen kombiniert werden, damit Sie bestimmte sicherheitsanforderungen in einer einzelnen Regel erfüllen können. Beispielsweise können Sie eine Regel, um alle Nachrichten verschlüsseln, die angegebenen Schlüsselwörter enthalten und werden an externe Empfänger adressiert erstellen. Office 365-Nachrichtenverschlüsselung verschlüsselt außerdem Antworten von verschlüsselten e-Mail-Empfänger, und Sie können eine Regel, die die Antworten Komfort für Ihre e-Mail-Benutzer entschlüsselt erstellen. Auf diese Weise keine Benutzer in Ihrer Organisation zur Anmeldung bei des Verschlüsselung Portals Antworten anzeigen.
  
Weitere Informationen dazu, wie Sie die Exchange-Mail Flow Regeln erstellen finden Sie unter [Definieren von Regeln für Office 365 Message Encryption](define-mail-flow-rules-to-encrypt-email.md).
  
## <a name="sending-viewing-and-replying-to-encrypted-email-messages"></a>Senden, Anzeigen und Beantworten von verschlüsselten E-Mail-Nachrichten

Mit Office 365 Message Encryption werden e-Mail-Nachrichten automatisch verschlüsselt basierend auf vom Administrator definierten Regeln. Eine e-Mail-Nachricht, die eine verschlüsselte Nachricht trägt Eingang im Posteingang des Empfängers mit einer verbundenen HTML-Datei.
  
Empfänger der Anleitung in der Nachricht zum Öffnen des Anhangs und authentifizieren mithilfe von Microsoft-Konto oder eine Arbeit "oder" Schule mit Office 365 verknüpft ist. Wenn der Empfänger nicht über ein Konto verfügen, sind sie angewiesen, erstellen eine Microsoft Konto, mit denen sie anmelden, um die verschlüsselte Nachricht anzuzeigen. Alternativ können Empfänger erhalten eine einmalige Kennung, um die Nachricht anzuzeigen. Empfänger können nach dem Anmelden bei, oder verwenden eine einmalige Kennung, die entschlüsselte Nachricht anzuzeigen und senden eine verschlüsselte Antwort.
  
## <a name="customize-encrypted-messages-with-office-365-message-encryption"></a>Anpassen von verschlüsselten Nachrichten mit Office 365-Nachrichtenverschlüsselung

Als Exchange Online und Exchange Online Protection-Administrator können Sie verschlüsselten Nachrichten anpassen. Sie können beispielsweise hinzufügen Ihres Unternehmens Marke Logo, geben Sie eine Einführung in und Hinzufügen von Text des Haftungsausschlusses in verschlüsselten Nachrichten und im Portal, in dem Empfänger Ihre verschlüsselten Nachrichten anzeigen. Windows PowerShell-Cmdlets können Sie die folgenden Aspekte des die Anzeigequalität für Empfänger von verschlüsselten e-Mail-Nachrichten anpassen:
  
- Einleitender Text der E-Mail, die die verschlüsselte Nachricht enthält
    
- Text des Haftungsausschlusses der E-Mail, die die verschlüsselte Nachricht enthält
    
- Portaltext, der im Meldungsanzeigeportal angezeigt wird
    
- Logo, das in der E-Mail-Nachricht und im Anzeigeportal erscheint
    
Sie können auch jederzeit zum Standardaussehen und -verhalten zurückkehren.
  
Im folgenden Beispiel wird ein benutzerdefiniertes ContosoPharma-Logo im E-Mail-Anhang gezeigt:
  
![Beispiel für die Seite mit Anzeige einer verschlüsselten Nachricht](media/TA-OME-3attachment2.jpg)
  
 **Anpassen von Verschlüsselung von e-Mail-Nachrichten und das verschlüsselungsportal an Ihrer Organisation Marke**
  
1. Verbindung mit Exchange Online mithilfe von Remote-PowerShell, wie beschrieben in [Verbindung mit Exchange Online Using Remote PowerShell](https://docs.microsoft.com/office365/enterprise/powershell/connect-to-exchange-online-tenants-with-remote-windows-powershell-for-delegated).
    
2. Verwenden Sie das Cmdlet "Set-OMEConfiguration gemäß" hier: [Set-OMEConfiguration](http://technet.microsoft.com/en-us/3ef0aec0-ce28-411d-abe8-7236f082af1b) , oder verwenden Sie die folgende Tabelle als Leitfaden. 
    
   **Anpassungsoptionen für Verschlüsselung**

|**So passen Sie dieses Verschlüsselungsfeature an**|**Verwenden Sie diese Befehle von Windows PowerShell**|
|:-----|:-----|
|Standardtext, der verschlüsselten E-Mail-Nachrichten beigefügt ist  <br/> Der Standardtext wird über den Anweisungen zum Betrachten von verschlüsselten Nachrichten angezeigt  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<string of up to 1024 characters>"` <br/> **Beispiel:**`Set-OMEConfiguration -Identity "OME Configuration" -EmailText "Encrypted message from ContosoPharma secure messaging system"` <br/> |
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<your disclaimer statement, string of up to 1024 characters>"` <br/> **Beispiel:**`Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText "This message is confidential for the use of the addressee only"` <br/> |
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<text for your portal, string of up to 128 characters>"` <br/> **Beispiel:**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText "ContosoPharma secure email portal"` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <Byte[]>` <br/> **Beispiel:**`Set-OMEConfiguration -Identity "OME configuration" -Image (Get-Content "C:\Temp\contosologo.png" -Encoding byte)` <br/> Unterstützte Dateiformate: .png, .jpg, .bmp oder .tiff  <br/> Optimale Größe der Logodatei: kleiner als 40 KB  <br/> Optimale Abmessungen des Logobilds: 170 x 70 Pixel  <br/> |
   
 **So entfernen Sie Marke Anpassungen aus Verschlüsselung von e-Mail-Nachrichten und das verschlüsselungsportal**
  
1. Verbindung mit Exchange Online mithilfe von Remote-PowerShell, wie beschrieben in [Verbindung mit Exchange Online Using Remote PowerShell](http://technet.microsoft.com/en-us/library/jj984289%28v=exchg.150%29.aspx).
    
2. Verwenden Sie das Cmdlet "Set-OMEConfiguration gemäß" hier: [Set-OMEConfiguration](http://technet.microsoft.com/3ef0aec0-ce28-411d-abe8-7236f082af1b). Ihrer Organisation Entfernen der Anpassungen aus der DisclaimerText emailText fest, Branding und PortalText Werte, legen Sie den Wert auf eine leere Zeichenfolge, `""`. Für alle Werte wie Logo, Abbild legen Sie den Wert auf `"$null"`.
    
   **Anpassungsoptionen für Verschlüsselung**

|**Dieses Feature der Verschlüsselungserfahrung zu Standardtext und -bild zurücksetzen**|**Verwenden Sie diese Befehle von Windows PowerShell**|
|:-----|:-----|
|Standardtext, der verschlüsselten E-Mail-Nachrichten beigefügt ist  <br/> Der Standardtext wird über den Anweisungen zum Betrachten von verschlüsselten Nachrichten angezeigt  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -EmailText "<empty string>"` <br/> **Beispiel:**`Set-OMEConfiguration -Identity "OME Configuration" -EmailText ""` <br/> |
|Haftungsausschluss in der E-Mail, die die verschlüsselte Nachricht enthält  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> DisclaimerText "<empty string>"` <br/> **Beispiel:**`Set-OMEConfiguration -Identity "OME Configuration" -DisclaimerText ""` <br/> |
|Der Text wird oben im Anzeigeportal für verschlüsselte E-Mails angezeigt  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -PortalText "<empty string>"` <br/> **Beispiel zurücksetzen auf Standard:**`Set-OMEConfiguration -Identity "OME Configuration" -PortalText ""` <br/> |
|Logo  <br/> | `Set-OMEConfiguration -Identity <OMEConfigurationIdParameter> -Image <"$null">` <br/> **Beispiel zurücksetzen auf Standard:**`Set-OMEConfiguration -Identity "OME configuration" -Image $null` <br/> |
   
## <a name="service-information-for-legacy-office-365-message-encryption-prior-to-the-release-of-the-new-ome-capabilities"></a>Serviceinformationen für die Vorversion Office 365 Message Encryption vor der Veröffentlichung der neuen OME-Funktionen
<a name="LegacyServiceInfo"> </a>

Die folgende Tabelle enthält technische Details für den Dienst Office 365 Message Encryption vor der Veröffentlichung der neuen OME-Funktionen.
  
|**Service-Informationen**|**Beschreibung**|
|:-----|:-----|
|Anforderungen an die Client-Geräte  <br/> |Verschlüsselte Nachrichten können auf einem Client-Gerät angezeigt werden, solange der HTML-Anhang in einem modernen Browser geöffnet werden kann, der Form Post unterstützt.  <br/> |
|Verschlüsselungsalgorithmus und Compliance Federal Information Processing Standards (FIPS)  <br/> |Office 365 Message Encryption verwendet die gleichen Verschlüsselungsschlüssel als Windows Azure Information Rights Management (IRM) und kryptografischen Modus 2 (2K für RSA) und 256 Bits Schlüssel SHA-1-Systemen unterstützt. Weitere Informationen zu den zugrunde liegenden kryptografische IRM-Modi finden Sie unter [AD RMS kryptografische Modi](http://technet.microsoft.com/library/hh867439%28WS.10%29.aspx).<br/> |
|Unterstützte Nachrichtentypen  <br/> |Office 365 Message Encryption wird nur für Elemente unterstützt, die eine Nachricht Klassen-ID des **IPM aufweisen. Hinweis**. Weitere Informationen finden Sie unter [Elementtypen und Nachrichtenklassen](https://msdn.microsoft.com/library/office/ff861573.aspx).<br/> |
|Beschränkungen der Nachrichtengröße  <br/> |Office 365 Message Encryption können Nachrichten von bis zu 25 MB verschlüsseln. Weitere Informationen zu größenbeschränkungen für Nachrichten finden Sie unter [Exchange Online-Begrenzungen](http://technet.microsoft.com/library/exchange-online-limits.aspx).<br/> |
|Exchange Online-e-Aufbewahrungsrichtlinien  <br/> |Exchange Online nicht verschlüsselten Nachrichten gespeichert.  <br/> |
|Die Sprachunterstützung für Office 365 Nachrichtenverschlüsselung  <br/> | Office 365 Nachrichtenverschlüsselung unterstützt Office 365-Sprachen wie folgt:  <br/>  Eingehende e-Mail-Nachrichten und angehängte HTML-Dateien werden basierend auf den spracheinstellungen des Absenders lokalisiert.  <br/>  Das Anzeigeportal wird basierend auf den Browsereinstellungen des Empfängers lokalisiert.  <br/>  Der Nachrichtentext (Inhalt) der verschlüsselten Nachricht ist nicht lokalisiert.  <br/> |
|Datenschutzinformationen für OME-Portal und OME-Viewer-App  <br/> |Die [Office 365 Messaging Encryption Portal privacy statement](protected-message-viewer-portal-privacy-statement.md) enthalten ausführliche Informationen darüber, wofür Microsoft Ihre vertraulichen Informationen verwendet.  <br/> |
   
## <a name="frequently-asked-questions-about-legacy-ome"></a>Häufig gestellte Fragen zu älteren OME
<a name="LegacyServiceInfo"> </a>

Haben Sie Fragen zu Office 365 Message Encryption? Hier finden Sie Antworten. Wenn Sie nicht finden, was Sie benötigen, überprüfen Sie die Office 365-Community-Foren auf [Office 365-Community](http://community.office365.com/en-us/forums/default.aspx).
  
 **F: Meine Benutzer Senden verschlüsselter Nachrichten an Empfänger außerhalb unserer Organisation. Gibt es etwas, das externe Empfänger zu tun, um das Lesen und Beantworten von e-Mail-Nachrichten, die verschlüsselt werden mit Office 365 Message Encryption haben?**
  
Empfänger außerhalb Ihrer Organisation, die verschlüsselte Office 365-Nachrichten erhalten, können diese auf eine von zwei Weisen anzeigen:
  
- Durch ein Microsoft-Konto oder Office 365 zugeordnete Arbeit oder Schule Konto anmelden.
    
- Mithilfe einer einmaligen Kennung.
    
 **F. Werden mit Office 365 verschlüsselte Nachrichten in der Cloud oder auf Microsoft-Servern gespeichert?**
  
Nein, die verschlüsselten Nachrichten auf e-Mail-System des Empfängers gespeichert sind, und wenn der Empfänger die Nachricht öffnet, wird es vorübergehend gebucht für die Anzeige auf Office 365-Servern. Die Nachrichten werden es nicht gespeichert.
  
 **F. Kann ich meine Marke in verschlüsselte E-Mail-Nachrichten einbinden?**
  
Ja. Sie können Windows PowerShell-Cmdlets verwenden, um den Standardtext, der oben in verschlüsselten E-Mail-Nachrichten angezeigt wird, sowie den Haftungsausschlusstext und das Logo, das Sie für E-Mail-Nachrichten und das Verschlüsselungsportal verwenden möchten, anpassen. Weitere Informationen finden Sie unter [Add branding to encrypted messages](add-your-organization-brand-to-encrypted-messages.md).
  
 **F. Ist für den Dienst eine Lizenz für jeden Benutzer in meiner Organisation erforderlich?**
  
Jeder Benutzer in der Organisation benötigt eine Lizenz, der verschlüsselte E-Mails versendet.
  
 **Q. Benötigen externe Empfänger Abonnements?**
  
Nein, externe Empfänger benötigen kein Abonnement zum Lesen oder Beantworten verschlüsselter Nachrichten. 
  
 **Frage: wie ist Office 365 Message Encryption unterschiedliche aus der Windows-Verwaltungsinstrumentation (Rights Management Services, RMS)?**
  
RMS bietet Informationen Rechteschutz Funktionen für interne e-Mails von einer Organisation durch integrierten Vorlagen, z. B.: kein weiterleiten und Firma (vertraulich). Office 365 Message Encryption unterstützt e-Mail-nachrichtenverschlüsselung für Nachrichten, die an externe Empfänger als auch interne Empfänger gesendet werden.
  
 **Frage: wie ist Office 365 Message Encryption, die sich von S/MIME?**
  
S/MIME ist im Grunde eine clientseitige Verschlüsselungstechnologie, für die eine komplizierte Zertifikatverwaltung und Veröffentlichungsinfrastruktur erforderlich ist. Die Office 365-Nachrichtenverschlüsselung verwendet Transportregeln und hängt nicht von der Veröffentlichung von Zertifikaten ab.
  
 **F. Kann ich über mobile Geräte verschlüsselten Nachrichten lesen?**
  
Ja, können Sie Nachrichten auf mobilen Android- und iOS anzeigen, die OME-Viewer-apps von der [Google wiedergeben speichern](http://go.microsoft.com/fwlink/?LinkID=525995&amp;clcid=0x409) und die [Apple App speichern](http://go.microsoft.com/fwlink/?LinkID=525996&amp;clcid=0x409)herunterladen. Öffnen Sie die HTML-Anhang in der OME-Viewer-app, und befolgen Sie die Anweisungen, um die verschlüsselte Nachricht zu öffnen. Für andere mobile Geräte können Sie die HTML-Anhang öffnen, solange der Mailclient Form Post unterstützt.
  
 **F. Sind Antworten und weitergeleitete Nachrichten verschlüsselt?**
  
Ja. Antworten werden während des gesamten Nachrichtenverlaufs weiterhin verschlüsselt.
  
 **F. Bietet die Office 365-Nachrichtenverschlüsselung eine Lokalisierung?**
  
Eingehende E-Mails und HTML-Inhalte werden basierend auf den E-Maileinstellungen des Absenders lokalisiert. Das Anzeigeportal wird basierend auf den Browsereinstellungen des Empfängers lokalisiert. Allerdings wird der eigentliche Text (Inhalt) der verschlüsselten Nachricht nicht lokalisiert.
  
 **F. Welche Verschlüsselungsmethode wird für die Office 365-Nachrichtenverschlüsselung verwendet?**
  
Die Office 365-Nachrichtenverschlüsselung verwendet die Rechteverwaltungsdienste (RMS) als Verschlüsselungsinfrastruktur. Die verwendete Verschlüsselungsmethode hängt davon ab, woher Sie die RMS-Schlüssel zum Verschlüsseln und Entschlüsseln von Nachrichten erhalten.
  
- Wenn Sie Microsoft Azure RMS verwenden, um die Schlüssel zu erhalten, wird die kryptografische Modus 2 verwendet. Kryptografische Modus 2 ist eine aktualisierte und verbesserte, kryptografische AD RMS-Implementierung. Es unterstützt RSA 2048 für die Signatur und Verschlüsselung, und SHA-256 für Signatur.
    
- Wenn Sie Active Directory (AD) RMS verwenden, um die Schlüssel abzurufen, wird entweder Kryptografiemodus 1 oder 2 verwendet. Die verwendete Methode hängt von Ihrer lokalen AD RMS-Bereitstellung ab. Kryptografiemodus 1 ist die ursprüngliche Kryptografieimplementierung für AD RMS. Er bietet Unterstützung für RSA 1024 für Signatur und Verschlüsselung sowie Unterstützung für SHA-1 für die Signatur. Dieser Modus wird durch alle aktuellen Versionen von RMS weiter unterstützt.
    
Weitere Informationen finden Sie unter [AD RMS kryptografische Modi](http://go.microsoft.com/fwlink/p/?LinkId=398616).
  
 **F: Warum wird bei einigen verschlüsselten Nachrichten angegeben, dass diese von Office365@messaging.microsoft.com stammen?**
  
Wenn eine verschlüsselte Antwort aus dem Verschlüsselungsportal oder über die OME Viewer-App gesendet wird, wird die Absender-E-Mail-Adresse auf Office365@messaging.microsoft.com festgelegt, da die verschlüsselte Nachricht über einen Microsoft-Endpunkt gesendet wird. Dadurch wird verhindert, dass verschlüsselte Nachrichten als Spam markiert werden. Der angezeigte Name in der E-Mail und die Adresse im Verschlüsselungsportal werden durch diese Bezeichnung nicht geändert. Außerdem gilt diese Bezeichnung nur für über das Portal gesendete Nachrichten und nicht für Nachrichten, die über einen anderen E-Mail-Client gesendet werden.
  
 **F: Ich bin Abonnent von Exchange Hosted Encryption (EHE). Wo kann ich mehr über das Upgrade auf Office 365 Message Encryption erfahren?**
  
Alle Kunden, die EHE wurden aktualisiert, um Office 365 Message Encryption. Weitere Informationen finden Sie im [Exchange gehostete Verschlüsselung Upgrade-Center](http://go.microsoft.com/fwlink/p/?LinkID=511077).
  
 **F: müssen ich alle URLs, die IP-Adressen öffnen oder Ports in der Firewall der Organisation zur Unterstützung von Office 365 Message Encryption?**
  
Ja. Sie müssen URLs für Exchange Online zur Liste „Zulassen“ für Ihre Organisation hinzufügen, damit Nachrichten, die mit der Office 365-Nachrichtenverschlüsselung verschlüsselt wurden, authentifiziert werden können. Eine Liste von Exchange Online-URLs finden Sie unter [Office 365 URLs and IP Address Ranges](https://support.office.com/article/f57e35b7-0a45-42f0-855e-11aa5e7f13fd.aspx).
  
 **F: Wie vielen Empfängern kann ich eine verschlüsselte Office 365-Nachricht senden?**
  
Die Empfängerzahl für eine verschlüsselte Nachricht basiert auf der Anzahl der Zeichen im Feld für die Nachricht **an** . In Kombination (nach Verteilerlistenerweiterung) sollte Empfängeradressen im Feld **an** 11,980 Zeichen nicht überschreiten. Da e-Mail-Adressen in Zeichenlänge variiert, keine standardmäßige Empfängergrenzwert für eine verschlüsselte Nachricht. 
  
 **F: Ist es möglich, eine Nachricht an einen bestimmten Empfänger zu sperren?**
  
Nein. Eine Nachricht an eine bestimmte Person nicht widerrufen werden, nachdem sie gesendet wird.
  
 **F: Kann ich einen Bericht über verschlüsselte Nachrichten anzeigen, die empfangen und gelesen wurden?**
  
Es ist kein Bericht, der anzeigt, wenn eine verschlüsselte Nachricht angesehen, aber es sind Office 365-Berichte zur Verfügung, die Sie zum Bestimmen der Anzahl von Nachrichten, die eine bestimmte Transportregel, beispielsweise abgeglichen nutzen können.
  
 **F. Wofür verwendet Microsoft die von mir über das OME-Portal und die OME-Viewer-App eingegebenen Informationen?**
  
Die [Datenschutzrichtlinie für Office 365-Verschlüsselungsportal Messaging](protected-message-viewer-portal-privacy-statement.md) bietet detaillierte Informationen zu den Microsoft wird und nicht mit Ihrem privaten Informationen. 
  

