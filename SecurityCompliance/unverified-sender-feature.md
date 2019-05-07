---
title: Identifizieren verdächtiger Nachrichten in Outlook.com und Outlook im Web
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Um zu verhindern, dass Phishing-Nachrichten zu Ihrem Postfach gelangen, überprüfen Outlook.com und Outlook im Web, ob der Absender der Empfänger ist und verdächtige Nachrichten als Junk-e-Mail kennzeichnet.
ms.openlocfilehash: edba30bb2ac0f9dc6ebc12db957a518de0c1b543
ms.sourcegitcommit: 9907bebc5f225032f681c4952de0b0be2df278ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2019
ms.locfileid: "33345900"
---
# <a name="identify-suspicious-messages-in-outlookcom-and-outlook-on-the-web"></a>Identifizieren verdächtiger Nachrichten in Outlook.com und Outlook im Web

Um zu verhindern, dass Phishing-Nachrichten zu Ihrem Postfach gelangen, überprüfen Outlook.com und Outlook im Web, ob der Absender der Empfänger ist und verdächtige Nachrichten als Junk-e-Mail kennzeichnet.

> [!IMPORTANT]
> Wenn eine Nachricht als Phishing-Betrug gekennzeichnet ist, wird Outlook.com und Outlook im Web eine Warnung am oberen Rand der Seite angezeigt, aber alle Links in der Nachricht können weiterhin geöffnet werden.

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a>Wie kann ich eine verdächtige Nachricht im Posteingang identifizieren?

Outlook.com und Outlook im Web zeigen Indikatoren an, wenn der Absender einer Nachricht nicht identifiziert werden kann, oder Ihre Identität unterscheidet sich von dem, was in der von-Adresse angezeigt wird.

### <a name="you-see-a--in-the-sender-image"></a>Sie sehen ein '? ' im Absender Bild

Wenn Outlook.com und Outlook im Web die Identität des Absenders nicht mithilfe von e-Mail-Authentifizierungstechniken überprüfen können, wird im Absender Foto ein "?" angezeigt.

![Nachricht wurde nicht erfolgreich überprüft](media/message-did-not-pass-verification.jpg)

Nicht jede Nachricht, die sich nicht authentifizieren kann, ist bösartig. Sie sollten jedoch bei der Interaktion mit Nachrichten, die sich nicht authentifizieren, vorsichtig sein, wenn Sie den Absender nicht erkennen. Oder, wenn Sie einen Absender erkennen, der normalerweise kein "?" im Absender Bild hat, aber Sie plötzlich beginnen, ihn zu sehen, könnte dies ein Zeichen sein, dass der Absender gefälscht wird.

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a>Die Adresse des Absenders unterscheidet sich von der Absenderadresse

Die e-Mail-Adresse, die in einer Nachricht angezeigt wird, unterscheidet sich häufig von dem, was Sie in der Absenderadresse sehen. Manchmal versuchen Phisher, Sie zu täuschen, dass der Absender eine andere Person als die ist, die Sie wirklich sind.

Wenn Outlook.com und Outlook im Web einen Unterschied zwischen der tatsächlichen Adresse des Absenders und der Adresse der Absenderadresse feststellen, wird der tatsächliche Absender mit dem Via-Tag angezeigt, das unterstrichen wird.

![nicht überprüfter Absender-Alternativtext](media/unverified-sender-feature1.png)

In diesem Beispiel wird die sendende `suspicious.com` Domäne authentifiziert, aber der Absender `unknown@contoso.com` in der von-Adresse.

Nicht jede Nachricht mit einem Via-Tag ist misstrauisch. Wenn Sie jedoch keine Nachricht mit einem Via-Tag erkennen, sollten Sie bei der Interaktion mit ihr vorsichtig sein.

In Outlook.com und im neuen Outlook im Web können Sie mit dem Mauszeiger auf den Namen oder die Adresse eines Absenders in der Nachrichtenliste zeigen, um die e-Mail-Adresse anzuzeigen, ohne die Nachricht öffnen zu müssen.

![Erste Schritte mit OneDrive](media/get-started-with-onedrive-message.png)

Woher wissen Sie, ob Sie das neue Outlook im Web verwenden? Sehen Sie sich die folgenden Beispiele an:

![Outlook vs Office 365](media/outlook-vs-outlook365.png)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a>Welche Kriterien werden von Outlook.com und Outlook im Web verwendet, um die Eigenschaften "?" und "Via" hinzuzufügen?

Für die "?" im Absender Bild: Outlook.com erfordert, dass die Nachricht entweder SPF-oder DKIM-Authentifizierung übergibt. Weitere Informationen finden Sie unter [Einrichten von SPF in office 365 zur](set-up-spf-in-office-365-to-help-prevent-spoofing.md) Verhinderung von Spoofing und [Verwenden von DKIM zum Überprüfen ausgehender e-Mails, die von Ihrer benutzerdefinierten domäne in Office 365 gesendet](use-dkim-to-validate-outbound-email.md)werden.

Für das via-Tag: Wenn sich die Domäne in der von-Adresse von der Domäne in der DKIM-Signatur oder von der SMTP-e-MAIL von unterscheidet, zeigt Outlook.com die Domäne in einem dieser beiden Felder an (bevorzugt die DKIM-Signatur).

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a>Können diese Eigenschaften mit IP-Zulässigkeit, Exchange-Transport Regel oder sicheren Absendern außer Kraft gesetzt werden?

Sie können diese Eigenschaften nicht außer Kraft setzen.

### <a name="how-do-i-remove-these-properties"></a>Wie entferne ich diese Eigenschaften?

Für das "?" im Absender Bild: als Absender sollten Sie Ihre Nachricht entweder mit SPF oder DKIM authentifizieren.

Für das via-Tag: als Absender sollten Sie sicherstellen, dass entweder die Domäne in der DKIM-Signatur oder die SMTP-e-MAIL-Nachricht mit der Domäne in der von-Adresse identisch oder eine Unterdomäne ist.

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a>Zeigt Outlook.com und Outlook im Web dies für jede Nachricht an, die die Authentifizierung nicht übergibt?

Nicht unbedingt. Outlook.com und Outlook im Web haben möglicherweise andere Eigenschaften in der Nachricht, um den Absender zu authentifizieren.

## <a name="related-topics"></a>Verwandte Themen

[Schützen Ihres Outlook.com-e-Mail-Kontos](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[Behandeln von Missbrauch, Phishing oder Spoofing in Outlook.com](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[Filtern von Junk-e-Mails und Spam in Outlook im Web](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)