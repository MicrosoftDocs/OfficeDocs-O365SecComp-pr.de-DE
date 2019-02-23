---
title: Steuern ausgehender Spamnachrichten in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
description: Wenn Ihre Organisation eine große Anzahl von Massensendungen sendet, die als Spam gekennzeichnet sind, können Sie das Senden von e-Mails mit Office 365 blockieren. Lesen Sie diesen Artikel, um mehr darüber zu erfahren, warum dies geschieht und was Sie dagegen tun können.
ms.openlocfilehash: 1098d22dedf9fd2a40b6ad8320c61ecd86f66593
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218685"
---
# <a name="controlling-outbound-spam-in-office-365"></a>Steuern ausgehender Spamnachrichten in Office 365

Wir nehmen ausgehende Spam-Mails Ernst, da es sich um einen gemeinsamen Dienst handelt.  Es gibt viele Kunden hinter einem freigegebenen Ressourcenpool, bei dem ein Kunde, der ausgehende e-Mails sendet, die ausgehende IP-Reputation des Diensts beeinträchtigen und die erfolgreiche Zustellung von e-Mail für andere Kunden beeinträchtigen kann. Es ist unfair gegenüber Kunden A, wenn Kunden B Spams und verschiedene 3rd Party IP-blocklists die verwendete IP-Adresse auflisten.

## <a name="what-admins-can-do-to-control-outbound-spam"></a>Was Administratoren tun können, um ausgehende Spam zu steuern

- **Benachrichtigungen aktivieren, wenn ein Konto Spam sendet oder heruntergefahren wird**. Administratoren können Bcc abrufen, wenn eine Nachricht als ausgehender Spam markiert und über den Pool mit hohem Risiko gesendet wird. Durch die Überwachung dieses Postfachs kann ein Administrator feststellen, ob er über ein kompromittiertes Konto in seinem Netzwerk verfügt oder ob der Spamfilter fälschlicherweise seine e-Mails als Spam markiert.  Weitere Informationen zum Einrichten der ausgehenden Spam Richtlinie finden Sie [hier](configure-the-outbound-spam-policy.md).
 
- **Überprüfende Spam Reklamationen von Drittanbieter-e-Mail-Anbietern**. Viele Drittanbieter-e-Mail-Dienste wie Outlook.com, Yahoo und AOL bieten eine Feedback Schleife, wenn ein Benutzer in seinem Dienst eine e-Mail von unserem Dienst als Spam markiert, wird die Nachricht verpackt und zur Überprüfungen an uns zurückgesendet. Weitere Informationen zur Sender Unterstützung für Outlook.com finden Sie [hier](https://sendersupport.olc.protection.outlook.com/pm/services.aspx).

## <a name="what-eop-does-to-control-outbound-spam"></a>Was EOP tut, um ausgehende Spam zu steuern 

1. **Segregation des ausgehenden Datenverkehrs in separate Pools von IPS**. Jede Nachricht, die Kunden über den Dienst senden, wird auf Spam überprüft. Wenn es sich bei der Nachricht um Spam handelt, wird Sie über den Pool mit hohem risikobereit gestellt. Dieser IP-Pool enthält nichtzustellbare Statusbenachrichtigungen und Spam. Die Lieferung an den beabsichtigten Empfänger wird nicht sichergestellt, da viele Drittparteien keine e-Mails akzeptieren, da die Qualität der gesendeten e-Mail.

Durch das Aufteilen des Datenverkehrs auf diese Weise wird sichergestellt, dass die niedrigere Qualität von e-Mails (Spam, Backscatter-Unzustellbarkeitsberichte) die Reputation der regulären ausgehenden e-Mail-Pools nicht nach unten zieht. Der Pool mit hohem Risiko hat in der Regel einen niedrigen Ruf bei vielen Empfängern im Internet, obwohl dies nicht universell ist. 

2. **Überwachung der IP-Reputation**. Office 365 fragt verschiedene IP-blocklists von Drittanbietern ab und generiert Warnungen, wenn eine unserer ausgehenden IPs darauf aufgeführt ist. Dies ermöglicht es uns, schnell zu reagieren, wenn Spam unseren Ruf verschlechtert hat. Wenn eine Warnung generiert wird, verfügen wir über eine interne Dokumentation, die die erforderlichen Schritte für die delistung vornimmt. 

3. **Deaktivieren von verletzenden Konten, wenn Sie zu viele e-Mails senden, die als Spam markiert sind**. Auch wenn wir unsere Spam-und nicht-Spam-e-Mails in zwei getrennte ausgehende IP-Pools einteilen, können diese nicht auf unbestimmte Zeit Spam senden. Wir überwachen, welche Konten Spam senden, und wenn es eine nicht genannte Grenze überschreitet, wird das Senden von Spam auf das Konto blockiert.

Eine einzelne Nachricht, die als Spam gekennzeichnet ist, kann eine Fehlklassifizierung des Spam Moduls und auch als falsch positives Ergebnis bezeichnet werden. Wir senden es über den Pool mit hohem Risiko, um ihm eine Chance zu geben; eine hohe Anzahl von Nachrichten in einem kurzen Zeitrahmen ist jedoch ein Anzeichen für ein Problem, und wenn dies der Fall ist, wird verhindert, dass das Konto mehr e-Mails sendet. Es gibt unterschiedliche Schwellenwerte für einzelne e-Mail-Konten sowie für den gesamten Mandanten.

4. **Deaktivieren von verletzenden Konten, wenn Sie zu viel e-Mails in einem zu kurzen Zeitrahmen senden**. Zusätzlich zu den Grenzwerten oben, die nach Nachrichten suchen, die als Spam markiert sind, gibt es auch Einschränkungen, die Konten blockieren, wenn Sie eine allgemeine Grenze erreichen, unabhängig davon, ob die Nachrichten als Spam markiert sind. Der Grund dieses Limits liegt darin, dass ein kompromittiertes Konto Spam Zero-Day senden kann, der vom Spamfilter verpasst wurde. Da es schwierig, wenn nicht gar unmöglich ist, den Unterschied zwischen einer legitimen Massen-Mailingkampagne und einer massiven Spam Kampagne zu erkennen, werden diese Grenzwerte aktiviert, um mögliche Schäden zu begrenzen.

> [!NOTE]
> Für #3 und #4 werden die genauen Grenzwerte nicht angepriesen.  Dadurch wird verhindert, dass Spammer das System spielen und sicherstellen, dass wir die Begrenzungen bei Bedarf ändern können. Die Grenzwertesind so hoch, dass ein durchschnittlicher geschäftlicher Benutzer Sie nie trifft und so niedrig ist, dass er den größten Teil des Schadens enthält, den ein Spammer ausführen kann. 

## <a name="recommended-workarounds-for-customers-who-want-to-send-outbound-a-lot-of-email-through-eop"></a>Empfohlene Problemumgehungen für Kunden, die ausgehende e-Mails über EOP senden möchten

Es ist schwierig, eine Balance zwischen Kunden zu finden, die eine große Menge an e-Mails senden möchten, im Vergleich zum Schutz des Diensts vor kompromittierten Konten und Massen-e-Mailern mit schlechten Listen Akquisitions Praktiken. Auch hier ist die Kosten für eine ausgehende IP-Landung auf einem 3rd-Party-blocklist höher als das Blockieren eines Kunden am Senden ausgehender e-Mails. Wie in der [Exchange Online-Dienstbeschreibung](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx#Receiving and sending limits)beschrieben, ist die Verwendung von EoP zum Senden von Massen-e-Mails keine unterstützte Verwendung des Diensts und ist nur auf "Best-Effort"-Basis zulässig. Für Kunden, die Massen-e-Mails senden möchten, wird Folgendes empfohlen:

a. **Senden Sie die Massen-e-Mails über ihre eigenen lokalen e-Mail-Server**. Dies führt dazu, dass der Kunde eine eigene e-Mail-Infrastruktur für diesen e-Mail-Typ verwalten muss.

b. **verwenden Sie einen Drittanbieter-Massen-e-Mailer zum Senden der Massenkommunikation**. Es gibt mehrere Drittanbieter-Massen-e-Mails, deren einziges Unternehmen es ist, Massen-e-Mails zu senden. Sie können mit Kunden zusammenarbeiten, um sicherzustellen, dass Sie über bewährte Methoden für die e-Mail-Anwendung verfügen und Ressourcen für deren Durchsetzung bereitstellen. 

Die Messaging-, Mobile-, Schadsoftware-Arbeitsgruppe "Anti-Abuse" (MAAWG) veröffentlicht ihre Mitgliedschaftsliste [hier](http://www.maawg.org/about/roster). Mehrere Bulk-e-Mail-Anbieter befinden sich in der Liste und sind als verantwortliche Internet Bürger bekannt. 
  
## <a name="for-more-information"></a>Weitere Informationen

[Beispielbenachrichtigung, wenn ein Absender aufgrund des Versendens von ausgehendem Spam blockiert wird](sample-notification-when-a-sender-is-blocked-sending-outbound-spam.md)

[Antispamschutz für Office 365-E-Mails](anti-spam-protection.md)

[Antispoofingschutz in Office 365](anti-spoofing-protection.md)

[SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md)
