---
title: Wie Office 365 die Absenderadresse überprüft, um Phishing zu verhindern
ms.author: krowley
author: kccross
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
description: 'Um Phishing zu verhindern, benötigen Office 365 und Outlook.com jetzt die RFC-Konformität für von: addresses.'
ms.openlocfilehash: df2f399e4044e9e96eab20e6789a8a53fad9015c
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217165"
---
# <a name="how-office-365-validates-the-from-address-to-prevent-phishing"></a><span data-ttu-id="dfb3a-103">Wie Office 365 die Absenderadresse überprüft, um Phishing zu verhindern</span><span class="sxs-lookup"><span data-stu-id="dfb3a-103">How Office 365 validates the From address to prevent phishing</span></span>

<span data-ttu-id="dfb3a-p101">Office 365-und Outlook.com-e-Mail-Konten erhalten eine immer größere Anzahl von Phishing-Angriffen. Eine Methode, die Phisher verwenden, ist das Senden von Nachrichten mit Werten für die Absenderadresse, die nicht mit [RFC 5322](https://tools.ietf.org/html/rfc5322)kompatibel sind. Die von:-Adresse wird auch als 5322. from-Adresse bezeichnet. Um diese Art von Phishing zu verhindern, benötigen Office 365 und Outlook.com Nachrichten, die vom Dienst empfangen wurden, um eine RFC-konforme from:-Adresse einzuschließen, wie in diesem Artikel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p101">Office 365 and Outlook.com email accounts receive an increasingly large number of phishing attacks. One technique phishers use is to send messages that have values for the From: address that are not compliant with [RFC 5322](https://tools.ietf.org/html/rfc5322). The From: address is also called the 5322.From address. To help prevent this type of phishing, Office 365 and Outlook.com require messages received by the service to include an RFC-compliant From: address as described in this article.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dfb3a-p102">Die Informationen in diesem Artikel erfordern grundlegende Kenntnisse des allgemeinen Formats von e-Mail-Adressen. Weitere Informationen finden Sie unter [rfc 5322](https://tools.ietf.org/html/rfc5322) (insbesondere Sections 3.2.3, 3,4 und 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321)sowie [RFC 3696](https://tools.ietf.org/html/rfc3696). Dieser Artikel befasst sich mit der Richtlinienerzwingung für die 5322. from-Adresse. In diesem Artikel geht es nicht um die 5321. mailFrom-Adresse.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p102">The information in this article requires you to have a basic understanding of the general format of email addresses. For more information, see [RFC 5322](https://tools.ietf.org/html/rfc5322) (particularly sections 3.2.3, 3.4, and 3.4.1), [RFC 5321](https://tools.ietf.org/html/rfc5321), as well as [RFC 3696](https://tools.ietf.org/html/rfc3696). This article is about policy enforcement for the 5322.From address. This article is not about the 5321.MailFrom address.</span></span> 
  
<span data-ttu-id="dfb3a-p103">Leider gibt es immer noch einige Legacy-e-Mail-Server im Internet, die weiterhin "legitime" e-Mail-Nachrichten senden, die eine fehlende oder fehlerhafte von:-Adresse aufweisen. Wenn Sie regelmäßig e-Mails von Organisationen empfangen, die diese Legacy Systeme verwenden, sollten Sie diese Organisationen ermutigen, Ihre e-Mail-Server zu aktualisieren, um die modernen Sicherheitsstandards einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p103">Unfortunately, there are still some legacy email servers on the Internet that continue to send "legitimate" email messages that have a missing or malformed From: address. If you regularly receive email from organizations that use these legacy systems, encourage those organizations to update their mail servers to comply with modern security standards.</span></span>
  
<span data-ttu-id="dfb3a-114">Microsoft startet die Durchsetzung der in diesem Artikel beschriebenen Richtlinien am 9. November 2017.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-114">Microsoft will start rolling out enforcement of the policies described in this article on November 9, 2017.</span></span>
  
## <a name="how-office-365-enforces-the-use-of-a-valid-from-address-to-prevent-phishing-attacks"></a><span data-ttu-id="dfb3a-115">Wie Office 365 die Verwendung einer gültigen from:-Adresse erzwingt, um Phishing-Angriffe zu verhindern</span><span class="sxs-lookup"><span data-stu-id="dfb3a-115">How Office 365 enforces the use of a valid From: address to prevent phishing attacks</span></span>

<span data-ttu-id="dfb3a-p104">In Office 365 werden Änderungen an der Art und Weise vorgenommen, wie die Verwendung der from:-Adresse in Nachrichten erzwungen wird, die Sie erhält, um Sie besser vor Phishing-Angriffen zu schützen. In diesem Artikel:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p104">Office 365 is making changes to the way it enforces the use of the From: address in messages it receives in order to better protect you from phishing attacks. In this article:</span></span>
  
- [<span data-ttu-id="dfb3a-118">Alle Nachrichten müssen eine gültige from:-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-118">All messages must include a valid From: address</span></span>](how-office-365-validates-the-from-address.md#MustIncludeFromAddress)
    
- [<span data-ttu-id="dfb3a-119">Format der from:-Adresse, wenn Sie keinen Anzeigenamen angeben</span><span class="sxs-lookup"><span data-stu-id="dfb3a-119">Format of the From: address if you don't include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatNoDisplayName)
    
- [<span data-ttu-id="dfb3a-120">Format der from:-Adresse, wenn Sie einen Anzeigenamen angeben</span><span class="sxs-lookup"><span data-stu-id="dfb3a-120">Format of the From: address if you include a display name</span></span>](how-office-365-validates-the-from-address.md#FormatDisplayName)
    
- [<span data-ttu-id="dfb3a-121">Weitere Beispiele für gültige und ungültige from:-Adressen</span><span class="sxs-lookup"><span data-stu-id="dfb3a-121">Additional examples of valid and invalid From: addresses</span></span>](how-office-365-validates-the-from-address.md#Examples)
    
- [<span data-ttu-id="dfb3a-122">Unterdrücken von automatischen Antworten auf Ihre benutzerdefinierte Domäne, ohne die von zu unterbrechen: Policy</span><span class="sxs-lookup"><span data-stu-id="dfb3a-122">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>](how-office-365-validates-the-from-address.md#SuppressAutoReply)
    
- [<span data-ttu-id="dfb3a-123">Überschreiben von Office 365 von: Adress Durchsetzungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="dfb3a-123">Overriding the Office 365 From: address enforcement policy</span></span>](how-office-365-validates-the-from-address.md#Override)
    
- [<span data-ttu-id="dfb3a-124">Weitere Möglichkeiten zum Schutz vor Internetkriminalität in Office 365</span><span class="sxs-lookup"><span data-stu-id="dfb3a-124">Other ways to prevent and protect against cybercrimes in Office 365</span></span>](how-office-365-validates-the-from-address.md#OtherProtection)
    
<span data-ttu-id="dfb3a-125">Das Senden im Auftrag eines anderen Benutzers ist von dieser Änderung nicht betroffen, weitere Informationen finden Sie unter Terry Zinks Blog "[Was verstehen wir, wenn wir auf den Absender einer e-Mail verweisen?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".</span><span class="sxs-lookup"><span data-stu-id="dfb3a-125">Sending on behalf of another user is not affected by this change, for more details, read Terry Zink's blog "[What do we mean when we refer to the 'sender' of an email?](https://blogs.msdn.microsoft.com/tzink/2017/06/22/what-do-we-mean-when-we-refer-to-the-sender-of-an-email/)".</span></span>
  
### <a name="all-messages-must-include-a-valid-from-address"></a><span data-ttu-id="dfb3a-126">Alle Nachrichten müssen eine gültige from:-Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-126">All messages must include a valid From: address</span></span>
<span data-ttu-id="dfb3a-127"><a name="MustIncludeFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="dfb3a-127"></span></span>

<span data-ttu-id="dfb3a-p105">Einige automatisierte Nachrichten schließen keine from:-Adresse ein, wenn Sie gesendet werden. Als Office 365 oder Outlook.com in der Vergangenheit eine Nachricht ohne from:-Adresse erhalten hat, hat der Dienst die folgende standardmäßige von:-Adresse zu der Nachricht hinzugefügt, damit Sie geliefert werden kann:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p105">Some automated messages don't include a From: address when they are sent. In the past, when Office 365 or Outlook.com received a message without a From: address, the service added the following default From: address to the message in order to make it deliverable:</span></span>
  
```
From: <>
```

<span data-ttu-id="dfb3a-p106">Ab November 2017 werden in Office 365 Änderungen an den Rechenzentren und e-Mail-Servern vorgenommen, die eine neue Regel erzwingen, bei der Nachrichten ohne Absenderadresse nicht mehr von Office 365 oder Outlook.com akzeptiert werden. Stattdessen müssen alle von Office 365 empfangenen Nachrichten bereits eine gültige from:-Adresse enthalten. Andernfalls wird die Nachricht an die Ordner "Junk-e-Mail" oder "Gelöschte Elemente" in Outlook.com und Office 365 gesendet.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p106">Starting November 9, 2017, Office 365 will be rolling out changes to its datacenters and mail servers which will enforce a new rule where messages without a From: address will no longer be accepted by Office 365 or Outlook.com. Instead, all messages received by Office 365 must already contain a valid From: address. Otherwise, the message will be sent to either the Junk Email or Deleted Items folders in Outlook.com and Office 365.</span></span> 
  
### <a name="syntax-overview-valid-format-for-the-from-address-for-office-365"></a><span data-ttu-id="dfb3a-133">Syntax Übersicht: gültiges Format für die from:-Adresse für Office 365</span><span class="sxs-lookup"><span data-stu-id="dfb3a-133">Syntax overview: Valid format for the From: address for Office 365</span></span>
<span data-ttu-id="dfb3a-134"><a name="SyntaxOverviewFromAddress"> </a></span><span class="sxs-lookup"><span data-stu-id="dfb3a-134"></span></span>

<span data-ttu-id="dfb3a-p107">Das Format für den Wert der from:-Adresse wird in mehreren RFCs ausführlich definiert. Es gibt viele Variationen bei der Adressierung und was als gültig oder ungültig angesehen werden kann. Um es einfach zu halten, empfiehlt Microsoft, dass Sie das folgende Format und die folgenden Definitionen verwenden:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p107">The format for the value of the From: address is defined in detail across several RFCs. There are many variations on addressing and what may be considered valid or invalid. To keep it simple, Microsoft recommends that you use the following format and definitions:</span></span>
  
```
From: "displayname " <emailaddress >
```

<span data-ttu-id="dfb3a-138">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-138">Where:</span></span>
  
- <span data-ttu-id="dfb3a-p108">Optional  *DisplayName* ist ein Ausdruck, der den Besitzer der e-Mail-Adresse beschreibt. Dies kann beispielsweise ein benutzerfreundlicher Name sein, um den Absender zu beschreiben, als der Name des Postfachs. Die Verwendung eines Anzeigenamens ist optional. Wenn Sie jedoch einen Anzeigenamen verwenden, empfiehlt Microsoft, dass Sie ihn immer in Anführungszeichen einschließen, wie in der Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p108">(Optional)  *displayname*  is a phrase that describes the owner of the email address. For example, this might be a more user-friendly name to describe the sender than the name of the mailbox. Using a display name is optional. However, if you choose to use a display name, Microsoft recommends that you always enclose it within quotation marks as shown.</span></span> 
    
- <span data-ttu-id="dfb3a-143">Erforderlich  \*\* die e-mailemail besteht aus:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-143">(Required)  *emailaddress*  is made up of:</span></span> 
    
  ```
  local-part @domain
  ```

    <span data-ttu-id="dfb3a-144">Wobei Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-144">Where:</span></span>
    
  - <span data-ttu-id="dfb3a-p109">Erforderlich  *local-Teil* ist eine Zeichenfolge, die das Postfach identifiziert, das der Adresse zugeordnet ist. Dies ist innerhalb der Domäne eindeutig. Häufig wird der Benutzername oder die GUID des Postfachbesitzers als Wert für den lokalen Webpart verwendet.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p109">(Required)  *local-part*  is a string that identifies the mailbox associated with the address. This is unique within the domain. Often, the mailbox owner's username or GUID is used as the value for the local-part.</span></span> 
    
  - <span data-ttu-id="dfb3a-148">Erforderlich  *Domäne* ist der vollqualifizierte Domänenname (FQDN) des e-Mail-Servers, der das Postfach hostet, das vom lokalen Teil der e-Mail-Adresse identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-148">(Required)  *domain*  is the fully-qualified domain name (FQDN) of the mail server that hosts the mailbox identified by the local-part of the email address.</span></span> 
    
### <a name="format-of-the-from-address-if-you-dont-include-a-display-name"></a><span data-ttu-id="dfb3a-149">Format der from:-Adresse, wenn Sie keinen Anzeigenamen angeben</span><span class="sxs-lookup"><span data-stu-id="dfb3a-149">Format of the From: address if you don't include a display name</span></span>
<span data-ttu-id="dfb3a-150"><a name="FormatNoDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="dfb3a-150"></span></span>

<span data-ttu-id="dfb3a-p110">Eine ordnungsgemäß formatierte from:-Adresse, die keinen Anzeigenamen enthält, beinhaltet nur eine einzelne e-Mail-Adresse mit oder ohne Spitze Klammern. Microsoft empfiehlt, die spitzen Klammern nicht mit Leerzeichen zu trennen. Fügen Sie darüber hinaus nichts nach der e-Mail-Adresse ein.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p110">A properly formatted From: address that does not include a display name includes only a single email address with or without angle brackets. Microsoft recommends that you do not separate the angle brackets with spaces. In addition, don't include anything after the email address.</span></span>
  
<span data-ttu-id="dfb3a-154">Die folgenden Beispiele sind gültig:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-154">The following examples are valid:</span></span>
  
```
From: sender@contoso.com
```

```
From: <sender@contoso.com>
```

<span data-ttu-id="dfb3a-155">Das folgende Beispiel ist gültig, aber nicht empfehlenswert, da es Leerzeichen zwischen den spitzen Klammern und der e-Mail-Adresse enthält:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-155">The following example is valid but not recommended because it contains spaces between the angle brackets and the email address:</span></span>
  
```
From: < sender@contoso.com >
```

<span data-ttu-id="dfb3a-156">Das folgende Beispiel ist ungültig, da es Text nach der e-Mail-Adresse enthält:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-156">The following example is invalid because it contains text after the email address:</span></span>
  
```
From: "Office 365" <sender@contoso.com> (Sent by a process)
```

### <a name="format-of-the-from-address-if-you-include-a-display-name"></a><span data-ttu-id="dfb3a-157">Format der from:-Adresse, wenn Sie einen Anzeigenamen angeben</span><span class="sxs-lookup"><span data-stu-id="dfb3a-157">Format of the From: address if you include a display name</span></span>
<span data-ttu-id="dfb3a-158"><a name="FormatDisplayName"> </a></span><span class="sxs-lookup"><span data-stu-id="dfb3a-158"></span></span>

<span data-ttu-id="dfb3a-159">Für from:-Adressen, die einen Wert für den Anzeigenamen aufweisen, gelten die folgenden Regeln:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-159">For From: addresses that include a value for the display name, the following rules apply:</span></span>
  
- <span data-ttu-id="dfb3a-p111">Wenn die Absenderadresse einen Anzeigenamen enthält und der Anzeigename ein Komma enthält, muss der Anzeigename in Anführungszeichen eingeschlossen werden. Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p111">If the sender address includes a display name, and the display name includes a comma, then the display name must be enclosed within quotation marks. For example:</span></span>
    
    <span data-ttu-id="dfb3a-162">Das folgende Beispiel ist gültig:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-162">The following example is valid:</span></span>
    
  ```
  From: "Sender, Example" <sender.example@contoso.com>
  ```

    <span data-ttu-id="dfb3a-163">Das folgende Beispiel ist ungültig:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-163">The following example is not valid:</span></span>
    
  ```
  From: Sender, Example <sender.example@contoso.com>
  ```

    <span data-ttu-id="dfb3a-164">Der Anzeigename wird nicht in Anführungszeichen gesetzt, wenn der Anzeigename ein Komma enthält, das gemäß RFC 5322 ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-164">Not enclosing the display name in quotation marks if that display name includes a comma is invalid according to RFC 5322.</span></span>
    
    <span data-ttu-id="dfb3a-165">Als bewährte Methode sollten Sie Anführungszeichen um den Anzeigenamen setzen, unabhängig davon, ob es ein Komma innerhalb des Anzeigenamens gibt oder nicht.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-165">As a best practice, put quote marks around the display name regardless of whether or not there is a comma within the display name.</span></span>
    
- <span data-ttu-id="dfb3a-166">Wenn die Absenderadresse einen Anzeigenamen enthält, muss die e-Mail-Adresse in eckige Klammern eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-166">If the sender address includes a display name, then the email address must be enclosed within angle brackets.</span></span>
    
    <span data-ttu-id="dfb3a-167">Als bewährte Methode empfiehlt Microsoft dringend, ein Leerzeichen zwischen dem Anzeigenamen und der e-Mail-Adresse einzufügen.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-167">As a best practice, Microsoft strongly recommends that you insert a space between the display name and the email address.</span></span>
    
### <a name="additional-examples-of-valid-and-invalid-from-addresses"></a><span data-ttu-id="dfb3a-168">Weitere Beispiele für gültige und ungültige from:-Adressen</span><span class="sxs-lookup"><span data-stu-id="dfb3a-168">Additional examples of valid and invalid From: addresses</span></span>
<span data-ttu-id="dfb3a-169"><a name="Examples"> </a></span><span class="sxs-lookup"><span data-stu-id="dfb3a-169"></span></span>

- <span data-ttu-id="dfb3a-170">Gültige</span><span class="sxs-lookup"><span data-stu-id="dfb3a-170">Valid:</span></span>
    
  ```
  From: "Office 365" <sender@contoso.com>
  ```

- <span data-ttu-id="dfb3a-p112">Ungültig. Die e-Mail-Adresse ist nicht in eckige Klammern eingeschlossen:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p112">Invalid. The email address is not enclosed with angle brackets:</span></span>
    
  ```
  From: Office 365 sender@contoso.com
  ```

- <span data-ttu-id="dfb3a-p113">Gültig, wird jedoch nicht empfohlen. Der Anzeigename ist nicht in Anführungszeichen gesetzt. Als bewährte Methode sollten Sie immer Anführungszeichen um den Anzeigenamen setzen:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p113">Valid, but not recommended. The display name is not in quotes. As a best practice, always put quotation marks around the display name:</span></span>
    
  ```
  From: Office 365 <sender@contoso.com>
  ```

- <span data-ttu-id="dfb3a-p114">Ungültig. Alles wird in Anführungszeichen eingeschlossen, nicht nur auf den Anzeigenamen:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p114">Invalid. Everything is enclosed within quotation marks, not just the display name:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>"
  ```

- <span data-ttu-id="dfb3a-p115">Ungültig. Die e-Mail-Adresse weist keine eckigen Klammern auf:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p115">Invalid. There are no angle brackets around the email address:</span></span>
    
  ```
  From: "Office 365 <sender@contoso.com>" sender@contoso.com
  ```

- <span data-ttu-id="dfb3a-p116">Ungültig. Zwischen dem Anzeigenamen und der linken Winkelklammer ist kein Leerzeichen:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p116">Invalid. There is no space between the display name and left angle bracket:</span></span>
    
  ```
  From: Office 365<sender@contoso.com>
  ```

- <span data-ttu-id="dfb3a-p117">Ungültig. Zwischen dem schließenden Anführungszeichen um den Anzeigenamen und der linken Spitze Klammer ist kein Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p117">Invalid. There is no space between the closing quotation mark around the display name and the left angle bracket.</span></span>
    
  ```
  From: "Office 365"<sender@contoso.com>
  ```

### <a name="suppress-auto-replies-to-your-custom-domain-without-breaking-the-from-policy"></a><span data-ttu-id="dfb3a-184">Unterdrücken von automatischen Antworten auf Ihre benutzerdefinierte Domäne, ohne die von zu unterbrechen: Policy</span><span class="sxs-lookup"><span data-stu-id="dfb3a-184">Suppress auto-replies to your custom domain without breaking the From: policy</span></span>
<span data-ttu-id="dfb3a-185"><a name="SuppressAutoReply"> </a></span><span class="sxs-lookup"><span data-stu-id="dfb3a-185"></span></span>

<span data-ttu-id="dfb3a-p118">Mit der neuen von: Policy Enforcement können Sie nicht mehr von: \< \> verwenden, um automatische Antworten zu unterdrücken. Stattdessen müssen Sie einen NULL-MX-Eintrag für Ihre benutzerdefinierte Domäne einrichten.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p118">With the new From: policy enforcement, you can no longer use From: \<\> to suppress auto-replies. Instead, you need to set up a null MX record for your custom domain.</span></span>
  
<span data-ttu-id="dfb3a-p119">Der MX-Eintrag (Mail Exchanger) ist ein Ressourceneintrag in DNS, der den e-Mail-Server identifiziert, der e-Mails für Ihre Domäne empfängt. Automatische Antworten (und alle Antworten) werden natürlich unterdrückt, da keine veröffentlichte Adresse vorhanden ist, an die der antwortende Server Nachrichten senden kann.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p119">The mail exchanger (MX) record is a resource record in DNS that identifies the mail server that receives mail for your domain. Auto-replies (and all replies) are naturally suppressed because there is no published address to which the responding server can send messages.</span></span>
  
<span data-ttu-id="dfb3a-190">Wenn Sie einen NULL-MX-Eintrag für Ihre benutzerdefinierte Domäne einrichten:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-190">When you set up a null MX record for your custom domain:</span></span>
  
- <span data-ttu-id="dfb3a-p120">Wählen Sie eine Domäne aus, von der Nachrichten gesendet werden, die keine (empfangen) e-Mails annehmen. Wenn Ihre primäre Domäne beispielsweise contoso.com ist, können Sie noreply.contoso.com auswählen.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p120">Choose a domain from which to send messages that doesn't accept (receive) email. For example, if your primary domain is contoso.com, you might choose noreply.contoso.com.</span></span>
    
- <span data-ttu-id="dfb3a-p121">Richten Sie den NULL-MX-Eintrag für Ihre Domäne ein. Ein NULL-MX-Eintrag besteht aus einem einzelnen Punkt, beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p121">Set up the null MX record for your domain. A null MX record consists of a single dot, for example:</span></span>
    
  ```
  noreply.contoso.com IN MX .
  ```

<span data-ttu-id="dfb3a-195">Weitere Informationen zum Veröffentlichen von NULL MX finden Sie unter [RFC 7505](https://tools.ietf.org/html/rfc7505).</span><span class="sxs-lookup"><span data-stu-id="dfb3a-195">For more information about publishing a null MX, see [RFC 7505](https://tools.ietf.org/html/rfc7505).</span></span>
  
### <a name="overriding-the-office-365-from-address-enforcement-policy"></a><span data-ttu-id="dfb3a-196">Überschreiben von Office 365 von: Adress Durchsetzungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="dfb3a-196">Overriding the Office 365 From: address enforcement policy</span></span>
<span data-ttu-id="dfb3a-197"><a name="Override"> </a></span><span class="sxs-lookup"><span data-stu-id="dfb3a-197"></span></span>

<span data-ttu-id="dfb3a-198">Nachdem Sie die neue Richtlinie abgeschlossen haben, können Sie diese Richtlinie für eingehende e-Mails, die Sie von Office 365 erhalten, nur umgehen, indem Sie eine der folgenden Methoden verwenden:</span><span class="sxs-lookup"><span data-stu-id="dfb3a-198">Once roll out of the new policy is complete, you can only bypass this policy for inbound mail you receive from Office 365 by using one of the following methods:</span></span> 
  
- <span data-ttu-id="dfb3a-199">IP-Zulassungslisten</span><span class="sxs-lookup"><span data-stu-id="dfb3a-199">IP allow lists</span></span>
    
- <span data-ttu-id="dfb3a-200">Exchange Online-Nachrichtenfluss Regeln</span><span class="sxs-lookup"><span data-stu-id="dfb3a-200">Exchange Online mail flow rules</span></span>
    
<span data-ttu-id="dfb3a-p122">Microsoft empfiehlt nachdrücklich, die Erzwingung der von:-Richtlinie zu überschreiben. Durch das Überschreiben dieser Richtlinie kann das Risiko Ihrer Organisation auf Spam, Phishing und andere Internetkriminalität erhöht werden.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p122">Microsoft strongly recommends against overriding the enforcement of the From: policy. Overriding this policy can increase your organization's risk of exposure to spam, phishing, and other cybercrimes.</span></span>
  
<span data-ttu-id="dfb3a-p123">Sie können diese Richtlinie für ausgehende e-Mails, die Sie in Office 365 senden, nicht außer Kraft setzen. Darüber hinaus wird Outlook.com keine Überschreibungen jeglicher Art zulassen, auch nicht über den Support.</span><span class="sxs-lookup"><span data-stu-id="dfb3a-p123">You cannot override this policy for outbound mail you send in Office 365. In addition, Outlook.com will not allow overrides of any kind, even through support.</span></span> 
  
### <a name="other-ways-to-prevent-and-protect-against-cybercrimes-in-office-365"></a><span data-ttu-id="dfb3a-205">Weitere Möglichkeiten zum Schutz vor Internetkriminalität in Office 365</span><span class="sxs-lookup"><span data-stu-id="dfb3a-205">Other ways to prevent and protect against cybercrimes in Office 365</span></span>
<span data-ttu-id="dfb3a-206"><a name="OtherProtection"> </a></span><span class="sxs-lookup"><span data-stu-id="dfb3a-206"></span></span>

<span data-ttu-id="dfb3a-207">Weitere Informationen dazu, wie Sie Ihre Organisation gegen Internetkriminalität wie Phishing, Spamming, Datenschutzverletzungen und andere Bedrohungen stärken können, finden Sie unter [Bewährte Sicherheitsmethoden für Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span><span class="sxs-lookup"><span data-stu-id="dfb3a-207">For more information on how you can strengthen your organization against cybercrimes like phishing, spamming, data breaches, and other threats, see [Security best practices for Office 365](https://support.office.com/article/9295e396-e53d-49b9-ae9b-0b5828cdedc3).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="dfb3a-208">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="dfb3a-208">Related Topics</span></span>

[<span data-ttu-id="dfb3a-209">Rückläufernachrichten und EOP</span><span class="sxs-lookup"><span data-stu-id="dfb3a-209">Backscatter messages and EOP</span></span>](https://technet.microsoft.com/en-us/library/dn499795%28v=exchg.150%29.aspx)
  

