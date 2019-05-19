---
title: Nicht überprüfter Absender
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 04/25/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- M365-security-compliance
description: Um zu verhindern, dass Phishing-Nachrichten Ihr Postfach erreichen, überprüfen Outlook.com und Outlook im Internet, ob der Absender der Benutzer ist, der Sie sagen, und verdächtige Nachrichten als Junk-e-Mail markieren.
ms.openlocfilehash: ad94a2953b6fd53612b2fc15038a7157e97f3b39
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157987"
---
# <a name="unverified-sender"></a>Nicht überprüfter Absender

Um zu verhindern, dass Phishing-Nachrichten Ihr Postfach erreichen, überprüfen Outlook.com und Outlook im Internet, ob der Absender der Benutzer ist, der Sie sagen, und verdächtige Nachrichten als Junk-e-Mail markieren.

> [!IMPORTANT]
> Wenn eine Nachricht als Phishing-Betrug markiert ist, zeigen Outlook.com und Outlook im Internet eine Warnung oben auf der Seite an, aber alle Links in der Nachricht können weiterhin geöffnet werden.

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a>Wie kann ich eine verdächtige Nachricht im Posteingang identifizieren?

Outlook.com und Outlook im Internet zeigen Indikatoren an, wenn der Absender einer Nachricht entweder nicht identifiziert werden kann oder sich Ihre Identität von dem unterscheidet, was Sie in der von-Adresse sehen.

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a>Vorgehensweise Verwalten der Nachrichten, die nicht überprüfte Absender Behandlung erhalten 

Wenn Sie ein Office 365 Kunde sind, können Sie diese Funktion über das Security & Compliance Center verwalten. 

- Im Office 365 Security & Compliance Center können mandantenadministratoren das Feature über den Schutz vor Spoofing unter der Anti-Phishing-Richtlinie aktivieren oder deaktivieren. Darüber hinaus kann es über das Cmdlet "AntiPhishPolicy" verwaltet werden. Weitere Informationen finden Sie unter Anti-Phishing Protection in Office 365 und AntiPhishPolicy.

    ![Bearbeiten von nicht authentifizierten Absendern in der grafischen Benutzeroberfläche.](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- Wenn ein Administrator ein falsch positives Ergebnis erkannt hat und ein Absender nicht überprüfte Absender Behandlung erhalten soll, können Sie eine der folgenden Aktionen ausführen, um den Absender zur Spoof-Zulassungsliste "Spoof Intelligence" hinzuzufügen:
        
    - Fügen Sie das Domänenpaar über die Spoof Intelligence-Einblicke hinzu. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise: Spoof Intelligence Insight
                
    - Fügen Sie das Domänenpaar über das PhishFilterPolicy-Cmdlet hinzu. Weitere Informationen finden Sie unter Festlegen-PhishFilterPolicy und Schutz vor Spoofing in Office 365

Darüber hinaus wenden wir die nicht überprüfte Absender Behandlung nicht an, wenn Sie über eine Liste der zugelassenen Administratoren an den Posteingang übermittelt wurde, einschließlich e-Mail-Transport Regeln (ETRs), Liste sicherer Domänen (Anti-Spam-Richtlinie), Liste sicherer Absender oder ein Benutzer hat diesen Benutzer als "sicheren Absender" in ihrer festgelegt Inbox.

### <a name="you-see-a--in-the-sender-image"></a>Im Absender Bild wird ein "?" angezeigt.

Wenn Outlook.com und Outlook im Internet die Identität des Absenders nicht mithilfe von e-Mail-Authentifizierungstechniken überprüfen können, wird im Absender Foto ein "?" angezeigt. 

![Nachricht hat die Überprüfung nicht übergeben](media/message-did-not-pass-verification.jpg)

Nicht jede Nachricht, die nicht authentifiziert werden kann, ist bösartig. Sie sollten jedoch mit der Interaktion mit Nachrichten vorsichtig sein, die nicht authentifiziert werden, wenn Sie den Absender nicht erkennen. Oder wenn Sie einen Absender erkennen, der normalerweise nicht über ein "?" im Absender Bild verfügt, aber Sie ihn plötzlich sehen, könnte dies ein Zeichen sein, bei dem der Absender gefälscht wird.

### <a name="the-senders-address-is-different-than-what-appears-in-the-from-address"></a>Die Adresse des Absenders unterscheidet sich von dem, was in der Absenderadresse angezeigt wird.

Die e-Mail-Adresse, die in einer Nachricht angezeigt wird, unterscheidet sich häufig von dem, was Sie in der Absenderadresse sehen. Manchmal versuchen Phisher, zu denken, dass der Absender jemand anderes ist als der, den Sie wirklich sind.

Wenn Outlook.com und Outlook im Internet einen Unterschied zwischen der tatsächlichen Adresse des Absenders und der Adresse in der Absenderadresse erkennen, wird der tatsächliche Absender mit dem Via-Tag angezeigt, das unterstrichen wird.

![nicht überprüfter Absender-Alternativtext](media/unverified-sender-feature1.png)

In diesem Beispiel wird die sendende `suspicious.com` Domäne authentifiziert, der Absender wird jedoch `unknown@contoso.com` in die von-Adresse eingefügt.

Nicht jede Nachricht mit einem Via-Tag ist verdächtig. Wenn Sie jedoch keine Nachricht mit einem Via-Tag erkennen, sollten Sie bei der Interaktion mit ihr vorsichtig sein.

In Outlook.com und dem neuen Outlook im Internet können Sie den Mauszeiger über den Namen oder die Adresse eines Absenders in der Nachrichtenliste bewegen, um die e-Mail-Adresse anzuzeigen, ohne die Nachricht öffnen zu müssen.

![Erste Schritte mit OneDrive](media/get-started-with-onedrive-message.png)

Woher wissen Sie, ob Sie das neue Outlook im Internet verwenden? Sehen Sie sich die folgenden Beispiele an:

![Outlook vs Office 365](media/outlook-vs-outlook365.png)

## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="what-criteria-does-outlookcom-and-outlook-on-the-web-use-to-add-the--and-the-via-properties"></a>Welche Kriterien werden von Outlook.com und Outlook im Internet verwendet, um die Eigenschaften "?" und "Via" hinzuzufügen?

Für das "?" im Absender Bild: Outlook.com erfordert, dass die Nachricht entweder die SPF-oder die DKIM-Authentifizierung übergibt. Weitere Informationen finden Sie unter [Einrichten von SPF in Office 365 zum verhindern](set-up-spf-in-office-365-to-help-prevent-spoofing.md) von Spoofing und [Verwenden von DKIM zum Überprüfen von ausgehenden e-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet wurden](use-dkim-to-validate-outbound-email.md).

Für das via-Tag: Wenn sich die Domäne in der von-Adresse von der Domäne in der DKIM-Signatur oder von der SMTP-e-Mail-Nachricht unterscheidet, zeigt Outlook.com die Domäne in einem dieser beiden Felder an (es wird die DKIM-Signatur bevorzugt).

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a>Kann ich diese Eigenschaften mit IP-zulässt, Exchange-Transport Regel zulässt oder sichere Absender außer Kraft setzen?

Sie können diese Eigenschaften nicht außer Kraft setzen.

### <a name="how-do-i-remove-these-properties"></a>Wie entferne ich diese Eigenschaften?

Für das "?" im Absender Bild: als Absender sollten Sie die Nachricht entweder mit SPF oder DKIM authentifizieren.

Für das via-Tag: als Absender sollten Sie sicherstellen, dass entweder die Domäne in der DKIM-Signatur oder die SMTP-e-Mail von dieselbe oder eine Unterdomäne der Domäne in der von-Adresse ist.

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a>Zeigt Outlook.com und Outlook im Internet dies für jede Nachricht, die die Authentifizierung nicht übergibt?

Nicht unbedingt. Outlook.com und Outlook im Internet haben möglicherweise andere Eigenschaften in der Nachricht zur Authentifizierung des Absenders.

## <a name="related-topics"></a>Verwandte Themen

[Schützen Ihres Outlook.com-e-Mail-Kontos](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[Umgang mit Missbrauch, Phishing oder Spoofing in Outlook.com](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[Filtern von Junk-e-Mails und Spam in Outlook im Internet](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
