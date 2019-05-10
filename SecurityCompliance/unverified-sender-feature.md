---
title: Nicht überprüfter Absender
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
ms.openlocfilehash: 5d4315afb33964e7c466384366b7315287cf6298
ms.sourcegitcommit: d24f50347c671cf5d2d8afec2f80d37d18af8b5d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/10/2019
ms.locfileid: "33867843"
---
# <a name="unverified-sender"></a>Nicht überprüfter Absender

Um zu verhindern, dass Phishing-Nachrichten zu Ihrem Postfach gelangen, überprüfen Outlook.com und Outlook im Web, ob der Absender der Empfänger ist und verdächtige Nachrichten als Junk-e-Mail kennzeichnet.

> [!IMPORTANT]
> Wenn eine Nachricht als Phishing-Betrug gekennzeichnet ist, wird Outlook.com und Outlook im Web eine Warnung am oberen Rand der Seite angezeigt, aber alle Links in der Nachricht können weiterhin geöffnet werden.

## <a name="how-can-i-identify-a-suspicious-message-in-my-inbox"></a>Wie kann ich eine verdächtige Nachricht im Posteingang identifizieren?

Outlook.com und Outlook im Web zeigen Indikatoren an, wenn der Absender einer Nachricht nicht identifiziert werden kann, oder Ihre Identität unterscheidet sich von dem, was in der von-Adresse angezeigt wird.

## <a name="how-to-manage-which-messages-receive-the-unverified-sender-treatment"></a>Verwalten der Nachrichten, die die nicht verifizierte Absender Behandlung erhalten 

Wenn Sie ein Office 365-Kunde sind, können Sie diese Funktion über das Security & Compliance Center verwalten. 

- Im Office 365 Security & Compliance Center können mandantenadministratoren die Funktion durch den Schutz vor Spoofing unter der Anti-Phishing-Richtlinie ein-oder ausschalten. Darüber hinaus kann es über das Cmdlet Set-AntiPhishPolicy verwaltet werden. Weitere Informationen finden Sie unter Schutz vor Phishing in Office 365 und Set-AntiPhishPolicy.

    ![Bearbeiten nicht authentifizierter Absender in der grafischen Benutzeroberfläche.](media/unverified-sender-article-editing-unauthenticated-senders.jpg)

- Wenn ein Administrator ein falsch positives Ergebnis ermittelt hat und ein Absender nicht die nicht verifizierte Absender Behandlung erhalten soll, können Sie eine der folgenden Aktionen ausführen, um den Absender der Spoof Intelligence-Zulassungsliste für Vortäuschungen hinzuzufügen:
        
    - Fügen Sie das Domänenpaar über Spoof Intelligence Insight hinzu. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise: Spoof Intelligence Insight
                
    - Fügen Sie das Domänenpaar über das PhishFilterPolicy-Cmdlet hinzu. Weitere Informationen finden Sie unter Set-PhishFilterPolicy und Schutz vor Spoofing in Office 365

Darüber hinaus wenden wir die nicht verifizierte Absender Behandlung nicht an, wenn Sie über eine Zulassungsliste für Administratoren an den Posteingang übermittelt wurde, einschließlich e-Mail-Transport Regeln (ETRs), sichere Domänenliste (Anti-Spam-Richtlinie), Liste sicherer Absender oder Benutzer hat diesen Benutzer als "sicheren Absender" in seinem Inbox.

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

Für die "?" im Absender Bild: Outlook.com erfordert, dass die Nachricht entweder SPF-oder DKIM-Authentifizierung übergibt. Weitere Informationen finden Sie unter [Einrichten von SPF in Office 365 zur](set-up-spf-in-office-365-to-help-prevent-spoofing.md) Verhinderung von Spoofing und [Verwenden von DKIM zum Überprüfen ausgehender e-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet](use-dkim-to-validate-outbound-email.md)werden.

Für das via-Tag: Wenn sich die Domäne in der von-Adresse von der Domäne in der DKIM-Signatur oder von der SMTP-e-Mail von unterscheidet, zeigt Outlook.com die Domäne in einem dieser beiden Felder an (bevorzugt die DKIM-Signatur).

### <a name="can-i-override-these-properties-with-ip-allows-exchange-transport-rule-allows-or-safe-senders"></a>Können diese Eigenschaften mit IP-Zulässigkeit, Exchange-Transport Regel oder sicheren Absendern außer Kraft gesetzt werden?

Sie können diese Eigenschaften nicht außer Kraft setzen.

### <a name="how-do-i-remove-these-properties"></a>Wie entferne ich diese Eigenschaften?

Für das "?" im Absender Bild: als Absender sollten Sie Ihre Nachricht entweder mit SPF oder DKIM authentifizieren.

Für das via-Tag: als Absender sollten Sie sicherstellen, dass entweder die Domäne in der DKIM-Signatur oder die SMTP-e-Mail-Nachricht mit der Domäne in der von-Adresse identisch oder eine Unterdomäne ist.

### <a name="does-outlookcom-and-outlook-on-the-web-show-this-for-every-message-that-doesnt-pass-authentication"></a>Zeigt Outlook.com und Outlook im Web dies für jede Nachricht an, die die Authentifizierung nicht übergibt?

Nicht unbedingt. Outlook.com und Outlook im Web haben möglicherweise andere Eigenschaften in der Nachricht, um den Absender zu authentifizieren.

## <a name="related-topics"></a>Verwandte Themen

[Schützen Ihres Outlook.com-e-Mail-Kontos](https://support.office.com/article/a4f20fc5-4307-4ece-8231-6d4d4bd8a9ba)

[Behandeln von Missbrauch, Phishing oder Spoofing in Outlook.com](https://support.office.com/article/0d882ea5-eedc-4bed-aebc-079ffa1105a3)

[Filtern von Junk-e-Mails und Spam in Outlook im Web](https://support.office.com/article/db786e79-54e2-40cc-904f-d89d57b7f41d)
