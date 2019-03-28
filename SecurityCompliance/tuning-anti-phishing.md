---
title: Optimieren des Schutzes gegen Phishing in Office 365
ms.author: chrisda
author: chrisda
manager: serdars
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
description: Administratoren können erfahren, warum und wie Phishing-Nachrichten durchgemacht wurden und was Sie tun müssen, um künftig weitere Phishing-Nachrichten zu verhindern.
ms.openlocfilehash: efda9e16c23e4533b6951e43ac085b7640e84576
ms.sourcegitcommit: 8a65a29aa3bfe5dcad0ff152a7cd795e02877dd9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/28/2019
ms.locfileid: "30937822"
---
# <a name="tune-anti-phishing-protection-in-office-365"></a>Optimieren des Schutzes gegen Phishing in Office 365

Obwohl Office 365 mit einer Vielzahl von Antiphishingfunktionen geliefert wird, die standardmäßig aktiviert sind, ist es möglich, dass einige Phishing-Nachrichten zu ihren Postfächern weitergeleitet werden. In diesem Thema wird beschrieben, was Sie tun können, um zu ermitteln, warum eine Phishing-Nachricht eingegangen ist und was Sie tun können, um die Einstellungen zum Schutz vor Phishing in Ihrer Exchange Online-Organisation zu ändern, _ohne dass sich dies versehentlich verschlechtert_.

## <a name="first-things-first-deal-with-any-compromised-accounts-and-make-sure-you-block-any-more-phishing-messages-from-getting-through"></a>Die ersten Schritte: befassen Sie sich mit kompromittierten Konten, und stellen Sie sicher, dass Sie keine weiteren Phishing-Nachrichten mehr blockieren.

Wenn das Konto eines Empfängers aufgrund der Phishing-Nachricht kompromittiert wurde, befolgen Sie die Schritte unter [Antworten auf ein kompromittiertes e-Mail-Konto in Office 365](responding-to-a-compromised-email-account.md).

Wenn Ihr Abonnement Advanced Threat Protection (ATP) enthält, können Sie mithilfe von [Office 365 Threat Intelligence](office-365-ti.md) andere Benutzer identifizieren, die auch die Phishing-Nachricht erhalten haben. Sie haben zusätzliche Optionen zum Blockieren von Phishing-Nachrichten:

- [ATP-sichere Links](set-up-atp-safe-links-policies.md)

- [Sichere Anlagen in ATP](set-up-atp-safe-attachments-policies.md)

- [Anti-Phishing-Richtlinien für ATP](set-up-anti-phishing-policies.md). Beachten Sie, dass Sie die **erweiterten Phishing-Schwellenwerte** in der Richtlinie von **Standard** auf **aggressiv**, **** aggressiver oder aggressiver erweitern können. ****

Überprüfen Sie, ob diese ATP-Funktionen aktiviert sind.

## <a name="report-the-phishing-message-to-microsoft"></a>Melden der Phishing-Nachricht an Microsoft

Das Melden von Phishing-Nachrichten ist hilfreich beim Optimieren der Filter, die zum Schutz aller Kunden in Office 365 verwendet werden.

Senden Sie die Phishing-Nachricht _als Anlage_ in einer neuen, ansonsten leeren nachricht an **Phish@office365.microsoft.com**. Die ursprüngliche Nachricht nicht nur weiterleiten; Andernfalls können die ursprünglichen Nachrichtenkopfzeilen nicht untersucht werden. Sie können auch das [Berichtnachrichten](https://docs.microsoft.com/office365/securitycompliance/enable-the-report-message-add-in) -Add-in in Outlook oder Outlook im Web (früher als Outlook Web App bezeichnet) verwenden.

Weitere Informationen finden Sie unter [Übermitteln von Spam-, Nicht-Spamnachrichten und Nachrichten, die als betrügerische Phishing-Angriffe angesehen werden, an Microsoft zur Analyse](submit-spam-non-spam-and-phishing-scam-messages-to-microsoft-for-analysis.md).

## <a name="inspect-the-message-headers"></a>ÜberPrüfen der Nachrichtenkopfzeilen

Sie können die Kopfzeilen der Phishing-Nachricht überprüfen, um festzustellen, ob es etwas gibt, was Sie selbst tun können, um zu verhindern, dass mehr Phishing-Nachrichten durchkommen. Mit anderen Worten: die Untersuchung der Kopfzeilen von Nachrichten kann Ihnen dabei helfen, Einstellungen in Ihrer Organisation zu identifizieren, die für das Zulassen der Phishing-Nachrichten verantwortlich waren.

Insbesondere sollten Sie das **X-Forefront-Antispam-Report-** Kopfzeilenfeld in den Nachrichtenkopfzeilen auf Hinweise zu übersprungenen Spam-oder Phishing-Filtern im SFV-Wert (Spamfilter Urteil) überprüfen. Nachrichten, die die Filterung überspringen, `SCL:-1`haben einen Eintrag von, was besagt, dass eine Ihrer Einstellungen diese Nachricht durch Überschreiben der Spam-oder Phishing-Urteile erlaubt, die vom Dienst bestimmt wurden. Weitere Informationen zum Abrufen von Nachrichtenkopfzeilen und eine vollständige Liste aller verfügbaren Antispam-und Antiphishing-Nachrichtenkopfzeilen finden Sie unter [Antispam-Nachrichtenkopfzeilen](https://docs.microsoft.com/office365/SecurityCompliance/anti-spam-message-headers).

## <a name="best-practices-to-stay-protected"></a>Bewährte Methoden zum Schutz vor

- Führen Sie auf monatlicher Basis [office 365 Secure Score](office-365-secure-score.md) aus, um die Sicherheitseinstellungen ihrer Office 365-Organisation zu bewerten.

- Überarbeiten Sie regelmäßig den [Spoof Intelligence-Bericht](learn-about-spoof-intelligence.md) , und aktivieren Sie den [Schutz vor Spoofing in der Anti-Phishing-Richtlinie](learn-about-spoof-intelligence.md#configuring-the-anti-spoofing-policy) , um verdächtige Nachrichten zu **isolieren** , anstatt Sie an den Junk-e-Mail-Ordner des Benutzers zu übermitteln.

- Überarbeiten Sie den [Status Bericht über Bedrohungen](view-reports-for-atp.md#threat-protection-status-report).

- Einige Kunden lassen versehentlich Phishing-Nachrichten durch, indem Sie Ihre eigenen Domänen in der Liste Absender oder zugelassene Domäne in Anti-Spam-Richtlinien platzieren. Wenn Sie dies tun, müssen Sie äußerste Vorsicht walten lassen. Diese Konfiguration erlaubt zwar einige legitime Nachrichten, aber auch schädliche Nachrichten, die normalerweise durch die Office 365-Spam-und/oder Phishing-Filter blockiert würden.

  Die beste Möglichkeit für den Umgang mit legitimen Nachrichten, die von Office 365 (falsch positive) blockiert werden und Absender in Ihrer Domäne betreffen, besteht darin, die SPF-, DKIM-und DMARC-Einträge in DNS für _alle_ e-Mail-Domänen in Office 365 vollständig und vollständig zu konfigurieren:

  - Stellen Sie sicher, dass Ihr SPF-Eintrag _alle_ e-Mail-Quellen für Absender in Ihrer Domäne identifiziert (Drittanbieterdienste nicht vergessen!).

  - Verwenden Sie Hard Fail\-(), um sicherzustellen, dass unbefugte Absender von e-Mail-Systemen, die so konfiguriert sind, abgelehnt werden. Sie können [Spoof Intelligence](https://docs.microsoft.com/office365/securitycompliance/learn-about-spoof-intelligence) verwenden, um Absender zu identifizieren, die Ihre Domäne verwenden, damit Sie autorisierte Drittanbieter Absender in ihren SPF-Eintrag aufnehmen können.

  Konfigurationsanweisungen finden Sie unter:
  
  - [Einrichten von SPF in Office 365 zum Verhindern von Spoofing](set-up-spf-in-office-365-to-help-prevent-spoofing.md)

  - [Verwenden von DKIM zum Überprüfen ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet werden](use-dkim-to-validate-outbound-email.md)

  - [Verwenden von DMARC zum Überprüfen von e-Mails in Office 365](use-dmarc-to-validate-email.md)

- Es wird empfohlen, nach Möglichkeit e-Mails für Ihre Domäne direkt an Office 365 zu senden. Zeigen Sie mit anderen Worten den MX-Eintrag Ihrer Office 365-Domäne auf Office 365. Exchange Online Protection (EOP) ist in der Lage, den bestmöglichen Schutz für Ihre Cloud-Benutzer bereitzustellen, wenn Ihre e-Mails direkt an Office 365 zugestellt werden. Wenn Sie ein Drittanbieter-e-Mail-Hygienesystem vor EOP verwenden müssen, stellen Sie sicher, dass Sie die Anweisungen [hier](https://docs.microsoft.com/exchange/mail-flow-best-practices/manage-mail-flow-using-third-party-cloud)befolgt haben.

- Die Multi-Factor-Authentifizierung (MFA) ist eine wirklich gute Möglichkeit, um kompromittierte Konten zu verhindern. Sie sollten unbedingt die Aktivierung von MFA für alle Ihre Benutzer erwägen. Beginnen Sie bei einem phasenweisen Ansatz, indem Sie MFA für die sensibelsten Benutzer (Administratoren, Führungskräfte usw.) aktivieren, bevor Sie MFA für alle aktivieren. Weitere Informationen finden Sie unter [Einrichten der mehr](https://docs.microsoft.com/office365/admin/security-and-compliance/set-up-multi-factor-authentication)stufigen Authentifizierung.

- WeiterLeitungsregeln an externe Empfänger werden häufig von Angreifern zum Extrahieren von Daten verwendet. Verwenden Sie die Informationen zum Überwachen von **Post Fach Weiterleitungsregeln** in [Office 365 Secure Score](office-365-secure-score.md) , um Weiterleitungsregeln an externe Empfänger zu finden und sogar zu verhindern. Weitere Informationen finden Sie unter [mildernde Client External forwardIng Rules with Secure Score](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/).
