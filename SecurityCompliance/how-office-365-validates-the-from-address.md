---
title: Wie Office 365 die Absenderadresse überprüft, um Phishing zu verhindern
ms.author: tracyp
author: MSFTTracyp
manager: laurawi
ms.date: 10/11/2017
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- OWC150
- MET150
ms.assetid: eef8408b-54d3-4d7d-9cf7-ad2af10b2e0e
ms.collection:
- M365-security-compliance
description: 'Um Phishing zu verhindern, benötigen Office 365 und Outlook.com jetzt die RFC-Konformität für von: addresses.'
ms.openlocfilehash: e540e56a7a40d13a92719865fccefefa61de47c2
ms.sourcegitcommit: 686bc9a8f7a7b6810a096f07d36751d10d334409
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/26/2019
ms.locfileid: "30276145"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a>Wie Office 365 die Absenderadresse überprüft, um Phishing zu verhindern

Office 365-und Outlook.com-e-Mail-Konten erhalten eine immer größere Anzahl von Phishing-Angriffen. Eine Methode, die Phisher verwenden, ist das Senden von Nachrichten mit Werten für die Absenderadresse, die nicht mit [RFC 5322](https://tools.ietf.org/html/rfc5322)kompatibel sind. Die von:-Adresse wird auch als 5322. from-Adresse bezeichnet. Um diese Art von Phishing zu verhindern, benötigen Office 365 und Outlook.com Nachrichten, die vom Dienst empfangen wurden, um eine RFC-konforme from:-Adresse einzuschließen, wie in diesem Artikel beschrieben.
  
> [!NOTE]
> Die Informationen in diesem Artikel erfordern grundlegende Kenntnisse des allgemeinen Formats von e-Mail-Adressen. Weitere Informationen finden Sie unter [rfc 5322](https://tools.ietf.org/html/rfc5322) (insbesondere Sections 3.2.3, 3,4 und 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321)sowie [RFC 3696](https://tools.ietf.org/html/rfc3696). Dieser Artikel befasst sich mit der Richtlinienerzwingung für die 5322. from-Adresse. In diesem Artikel geht es nicht um die 5321. mailFrom-Adresse. 
  
Leider gibt es immer noch einige Legacy-e-Mail-Server im Internet, die weiterhin "legitime" e-Mail-Nachrichten senden, die eine fehlende oder fehlerhafte von:-Adresse aufweisen. Wenn Sie regelmäßig e-Mails von Organisationen empfangen, die diese Legacy Systeme verwenden, sollten Sie diese Organisationen ermutigen, Ihre e-Mail-Server zu aktualisieren, um die modernen Sicherheitsstandards einzuhalten.
  
Microsoft startet die Durchsetzung der in diesem Artikel beschriebenen Richtlinien am 9. November 2017.
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a>Wie Office 365 die Verwendung einer gültigen from:-Adresse erzwingt, um Phishing-Angriffe zu verhindern

In Office 365 werden Änderungen an der Art und Weise vorgenommen, wie die Verwendung der from:-Adresse in Nachrichten erzwungen wird, die Sie erhält, um Sie besser vor Phishing-Angriffen zu schützen. In diesem Artikel:
  
- [Alle Nachrichten müssen eine gültige from:-Adresse aufweisen.](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [Format der from:-Adresse, wenn Sie keinen Anzeigenamen angeben](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [Format der from:-Adresse, wenn Sie einen Anzeigenamen angeben](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [Weitere Beispiele für gültige und ungültige from:-Adressen](how-office-365-validates-the-from-address.md#Examples)
    
- [Unterdrücken von automatischen Antworten auf Ihre benutzerdefinierte Domäne, ohne die von zu unterbrechen: Policy](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [Überschreiben von Office 365 von: Adress Durchsetzungsrichtlinie](how-office-365-validates-the-from-address.md#Override)
    
- [Weitere Möglichkeiten zum Schutz vor Internetkriminalität in Office 365](how-office-365-validates-the-from-address.md#OtherProtection)
    
Das Senden im Auftrag eines anderen Benutzers ist von dieser Änderung nicht betroffen, weitere Informationen finden Sie unter Terry Zinks Blog "[Was verstehen wir, wenn wir auf den Absender einer e-Mail verweisen?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".
  
### <a name="all-messages-must-include-a-valid-from-address"></a>Alle Nachrichten müssen eine gültige from:-Adresse aufweisen.
<a name="MustIncludeFromAddress"> </a>

Einige automatisierte Nachrichten schließen keine from:-Adresse ein, wenn Sie gesendet werden. Als Office 365 oder Outlook.com in der Vergangenheit eine Nachricht ohne from:-Adresse erhalten hat, hat der Dienst die folgende standardmäßige von:-Adresse zu der Nachricht hinzugefügt, damit Sie geliefert werden kann:
  
```
From: <>
```

Ab November 2017 werden in Office 365 Änderungen an den Rechenzentren und e-Mail-Servern vorgenommen, die eine neue Regel erzwingen, bei der Nachrichten ohne Absenderadresse nicht mehr von Office 365 oder Outlook.com akzeptiert werden. Stattdessen müssen alle von Office 365 empfangenen Nachrichten bereits eine gültige from:-Adresse enthalten. Andernfalls wird die Nachricht an die Ordner "Junk-e-Mail" oder "Gelöschte Elemente" in Outlook.com und Office 365 gesendet. 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a>Syntax Übersicht: gültiges Format für die from:-Adresse für Office 365
<a name="SyntaxOverviewFromAddress"> </a>

Das Format für den Wert der from:-Adresse wird in mehreren RFCs ausführlich definiert. Es gibt viele Variationen bei der Adressierung und was als gültig oder ungültig angesehen werden kann. Um es einfach zu halten, empfiehlt Microsoft, dass Sie das folgende Format und die folgenden Definitionen verwenden:
  
```
From: "displayname " <emailaddress >
```

Wobei Folgendes gilt:
  
- Optional  *DisplayName* ist ein Ausdruck, der den Besitzer der e-Mail-Adresse beschreibt. Dies kann beispielsweise ein benutzerfreundlicher Name sein, um den Absender zu beschreiben, als der Name des Postfachs. Die Verwendung eines Anzeigenamens ist optional. Wenn Sie jedoch einen Anzeigenamen verwenden, empfiehlt Microsoft, dass Sie ihn immer in Anführungszeichen einschließen, wie in der Abbildung dargestellt. 
    
- Erforderlich  ** die e-mailemail besteht aus: 
    
  ```
  local-part @domain
  ```

    Wobei Folgendes gilt:
    
  - Erforderlich  *local-Teil* ist eine Zeichenfolge, die das Postfach identifiziert, das der Adresse zugeordnet ist. Dies ist innerhalb der Domäne eindeutig. Häufig wird der Benutzername oder die GUID des Postfachbesitzers als Wert für den lokalen Webpart verwendet. 
    
  - Erforderlich  *Domäne* ist der vollqualifizierte Domänenname (FQDN) des e-Mail-Servers, der das Postfach hostet, das vom lokalen Teil der e-Mail-Adresse identifiziert wird. 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a>Format der from:-Adresse, wenn Sie keinen Anzeigenamen angeben
<a name="FormatNoDisplayName"> </a>

Eine ordnungsgemäß formatierte from:-Adresse, die keinen Anzeigenamen enthält, beinhaltet nur eine einzelne e-Mail-Adresse mit oder ohne Spitze Klammern. Microsoft empfiehlt, die spitzen Klammern nicht mit Leerzeichen zu trennen. Fügen Sie darüber hinaus nichts nach der e-Mail-Adresse ein.
  
Die folgenden Beispiele sind gültig:
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

Das folgende Beispiel ist gültig, aber nicht empfehlenswert, da es Leerzeichen zwischen den spitzen Klammern und der e-Mail-Adresse enthält:
  
```
From: < sender@contoso.com >
```

Das folgende Beispiel ist ungültig, da es Text nach der e-Mail-Adresse enthält:
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a>Format der from:-Adresse, wenn Sie einen Anzeigenamen angeben
<a name="FormatDisplayName"> </a>

Für from:-Adressen, die einen Wert für den Anzeigenamen aufweisen, gelten die folgenden Regeln:
  
- Wenn die Absenderadresse einen Anzeigenamen enthält und der Anzeigename ein Komma enthält, muss der Anzeigename in Anführungszeichen eingeschlossen werden. Zum Beispiel:
    
    Das folgende Beispiel ist gültig:
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    Das folgende Beispiel ist ungültig:
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    Der Anzeigename wird nicht in Anführungszeichen gesetzt, wenn der Anzeigename ein Komma enthält, das gemäß RFC 5322 ungültig ist.
    
    Als bewährte Methode sollten Sie Anführungszeichen um den Anzeigenamen setzen, unabhängig davon, ob es ein Komma innerhalb des Anzeigenamens gibt oder nicht.
    
- Wenn die Absenderadresse einen Anzeigenamen enthält, muss die e-Mail-Adresse in eckige Klammern eingeschlossen werden.
    
    Als bewährte Methode empfiehlt Microsoft dringend, ein Leerzeichen zwischen dem Anzeigenamen und der e-Mail-Adresse einzufügen.
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a>Weitere Beispiele für gültige und ungültige from:-Adressen
<a name="Examples"> </a>

- Gültige
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- Ungültig. Die e-Mail-Adresse ist nicht in eckige Klammern eingeschlossen:
    
  ```
  From: Office 365 sender@contoso.com
  ```

- Gültig, wird jedoch nicht empfohlen. Der Anzeigename ist nicht in Anführungszeichen gesetzt. Als bewährte Methode sollten Sie immer Anführungszeichen um den Anzeigenamen setzen:
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- Ungültig. Alles wird in Anführungszeichen eingeschlossen, nicht nur auf den Anzeigenamen:
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- Ungültig. Die e-Mail-Adresse weist keine eckigen Klammern auf:
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- Ungültig. Zwischen dem Anzeigenamen und der linken Winkelklammer ist kein Leerzeichen:
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- Ungültig. Zwischen dem schließenden Anführungszeichen um den Anzeigenamen und der linken Spitze Klammer ist kein Leerzeichen.
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a>Unterdrücken von automatischen Antworten auf Ihre benutzerdefinierte Domäne, ohne die von zu unterbrechen: Policy
<a name="SuppressAutoReply"> </a>

Mit der neuen von: Policy Enforcement können Sie nicht mehr von: \< \> verwenden, um automatische Antworten zu unterdrücken. Stattdessen müssen Sie einen NULL-MX-Eintrag für Ihre benutzerdefinierte Domäne einrichten.
  
Der MX-Eintrag (Mail Exchanger) ist ein Ressourceneintrag in DNS, der den e-Mail-Server identifiziert, der e-Mails für Ihre Domäne empfängt. Automatische Antworten (und alle Antworten) werden natürlich unterdrückt, da keine veröffentlichte Adresse vorhanden ist, an die der antwortende Server Nachrichten senden kann.
  
Wenn Sie einen NULL-MX-Eintrag für Ihre benutzerdefinierte Domäne einrichten:
  
- Wählen Sie eine Domäne aus, von der Nachrichten gesendet werden, die keine (empfangen) e-Mails annehmen. Wenn Ihre primäre Domäne beispielsweise contoso.com ist, können Sie noreply.contoso.com auswählen.
    
- Richten Sie den NULL-MX-Eintrag für Ihre Domäne ein. Ein NULL-MX-Eintrag besteht aus einem einzelnen Punkt, beispielsweise:
    
  ```
  noreply.contoso.com IN MX .
  ```

Weitere Informationen zum Veröffentlichen von NULL MX finden Sie unter [RFC 7505](https://tools.ietf.org/html/rfc7505).
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a>Überschreiben von Office 365 von: Adress Durchsetzungsrichtlinie
<a name="Override"> </a>

Nachdem Sie die neue Richtlinie abgeschlossen haben, können Sie diese Richtlinie für eingehende e-Mails, die Sie von Office 365 erhalten, nur umgehen, indem Sie eine der folgenden Methoden verwenden: 
  
- IP-Zulassungslisten
    
- Exchange Online-Nachrichtenfluss Regeln
    
Microsoft empfiehlt nachdrücklich, die Erzwingung der von:-Richtlinie zu überschreiben. Durch das Überschreiben dieser Richtlinie kann das Risiko Ihrer Organisation auf Spam, Phishing und andere Internetkriminalität erhöht werden.
  
Sie können diese Richtlinie für ausgehende e-Mails, die Sie in Office 365 senden, nicht außer Kraft setzen. Darüber hinaus wird Outlook.com keine Überschreibungen jeglicher Art zulassen, auch nicht über den Support. 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a>Weitere Möglichkeiten zum Schutz vor Internetkriminalität in Office 365
<a name="OtherProtection"> </a>

Weitere Informationen dazu, wie Sie Ihre Organisation gegen Internetkriminalität wie Phishing, Spamming, Datenschutzverletzungen und andere Bedrohungen stärken können, finden Sie unter [Bewährte Sicherheitsmethoden für Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).
  
## <a name="related-topics"></a>Verwandte Themen

[Rückläufernachrichten und EOP](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

