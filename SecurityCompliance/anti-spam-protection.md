---
title: Office 365-Antispamschutz für E-Mails
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
ms.collection:
- M365-security-compliance
description: Informationen zu den Antispam-Einstellungen und-Filtern, die Ihnen helfen, Spam in Exchange Online und Office 365 zu verhindern. Zu viel Spam in Office 365? Sie können Ihre Spamfilter und Anti-Spam-Richtlinieneinstellungen anpassen.
ms.openlocfilehash: 253ef10ac98b10377252a7a43fa306dd5a0ea90a
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32242513"
---
# <a name="office-365-email-anti-spam-protection"></a>Office 365-Antispamschutz für E-Mails

Machen Sie sich Gedanken über zu viel Spam in Office 365? Wir haben mehrere Spamfilter in Ihren Office 365-oder Exchange Online Protection (EOP)-Dienst integriert, sodass Ihre e-Mails ab dem Moment geschützt werden, an dem Sie Ihre erste Nachricht erhalten. Um Spam in Office 365 zu verhindern, möchten Sie möglicherweise eine Schutzeinstellung ändern, um ein bestimmtes Problem in Ihrer Organisation zu behandeln – angenommen, Sie erhalten beispielsweise viel Spam von einem bestimmten Absender – oder Sie können Ihre Einstellungen einfach so anpassen, dass Sie zugeschnitten auf die Anforderungen Ihrer Organisation. Zu diesem Zweck können Sie Antispam-Einstellungen im Office 365 Security &amp; Compliance Center ändern.
  
Dieser Artikel richtet sich an Office 365-Administratoren. Wenn Sie kein Administrator sind, aber Sie ein Office 365-Benutzer sind und Sie erfahren möchten, wie Sie mit Spam umgehen, die Sie erhalten, ist dies nicht der Artikel, den Sie suchen. Wenn Sie Outlook für PC oder Outlook für Mac verwenden, beginnen Sie stattdessen mit [Übersicht über den Junk-e-Mail-Filter](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089). Wenn Sie Outlook im Web verwenden, beginnen Sie mit [Informationen zu Junk-e-Mails und Phishing](https://support.office.com/article/86c1d76f-4d5a-4967-9647-35665dc17c31).
  
## <a name="these-options-help-you-prevent-spam-in-office-365"></a>Diese Optionen helfen Ihnen, Spam in Office 365 zu verhindern.

 **Verbindungsfilterung**: Wenn Sie die Verbindungsfilterung verwenden, überprüft Office 365 die Reputation des Absenders, bevor Sie eine Nachricht erhalten. Sie können eine Zulassungsliste oder eine Liste sicherer Absender erstellen, um sicherzustellen, dass Sie jede Nachricht erhalten, die Ihnen über eine bestimmte IP-Adresse oder einen IP-Adress Kreis gesendet wird. Sie können auch eine Liste mit IP-Adressen erstellen, von denen Nachrichten blockiert werden, die als Sperrliste bezeichnet werden. Weitere Informationen finden Sie unter [Configure the Connection Filter Policy](https://technet.microsoft.com/library/jj200718%28v=exchg.150%29.aspx). Wenn Sie sich Sorgen über Spam in Office 365 machen, verwenden Sie die Verbindungsfilterung, um Spam zu verhindern.
  
Für Kunden, die Office 365 Enterprise E5 haben oder Advanced Threat Protection (ATP)-Lizenzen erworben haben, wird die Verbindungsfilterung von Spoof Intelligence verwendet, um Zulassungs-und Sperrlisten von Absendern zu erstellen, die Ihre Domäne spoofen. Weitere Informationen finden Sie unter [erfahren Sie mehr über Spoof Intelligence](https://go.microsoft.com/fwlink/?LinkID=735009).
  
 **Spamfilterung**: Office 365 überprüft mithilfe der Spamfilterung, ob Nachrichten Merkmale mit Spam konsistent sind. Sie können ändern, welche Aktionen für Nachrichten als Spam identifiziert werden sollen, und auswählen, ob Nachrichten, die in bestimmten Sprachen geschrieben wurden, gefiltert oder aus bestimmten Ländern oder Regionen gesendet werden sollen. Sie können auch erweiterte Spam Filterungsoptionen aktivieren, wenn Sie einen aggressiven Ansatz für die Spamfilterung verfolgen möchten. Darüber hinaus können Sie Spambenachrichtigungen für Endbenutzer konfigurieren, um Benutzer zu informieren, wenn für Sie vorgesehene Nachrichten an die Quarantäne gesendet wurden. (Das Senden von Nachrichten an die Quarantäne ist eine der konfigurierbaren Aktionen.) Anhand dieser Benachrichtigungen können Endbenutzer falsch positive Ergebnisse veröffentlichen und Microsoft zur Analyse melden. Weitere Informationen finden Sie unter [Konfigurieren von Spamfilterrichtlinien](https://go.microsoft.com/fwlink/p/?LinkId=617147). Um Spam in Office 365 zu verhindern, verwenden Sie die Spamfilterung, wenn Sie zu viel Spam in Office 365 befürchten, verwenden Sie die Verbindungsfilterung, um Spam zu verhindern.
  
> [!NOTE]
> Für eigenständige EOP-Kunden: Standardmäßig senden die EOP-Spamfilter Spam erkannte Nachrichten an den Junk-e-Mail-Ordner der Empfänger. Um jedoch sicherzustellen, dass die Aktion **Nachricht in Junk-e-Mail-Ordner verschieben** mit lokalen Postfächern funktioniert, müssen Sie zwei Exchange-Nachrichtenfluss Regeln (auch bekannt als Transportregeln) auf Ihren lokalen Servern konfigurieren, um die von EoP. Weitere Informationen finden Sie unter [Sicherstellen, dass Spam an die Junk-E-Mail-Ordner der einzelnen Benutzer geleitet wird](https://technet.microsoft.com/library/jj837173%28v=exchg.150%29.aspx). 
  
## <a name="extra-information-if-you-receive-too-much-spam-in-office-365"></a>Zusätzliche Informationen, wenn Sie zu viel Spam in Office 365 erhalten

Das folgende Video bietet eine Übersicht über die Konfiguration der Spamfilterung in EOP.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/608be94c-d763-4c47-af94-99e7cb277713?autoplay=false]
  
Weitere Informationen finden Sie im Thema [configure Spamfilter Policies](https://go.microsoft.com/fwlink/p/?LinkId=617147) .
  
## <a name="check-your-outgoing-messages-to-prevent-spam-in-office-365"></a>Überprüfen der ausgehenden Nachrichten zur Verhinderung von Spam in Office 365

 **Ausgehende Filterung**: Office 365 überprüft auch, ob Ihre Benutzer keine Spamnachrichten senden. Beispielsweise kann der Computer eines Benutzers mit Schadsoftware infiziert werden, die dazu führt, dass Spamnachrichten gesendet werden. ** Die ausgehende Filterung kann nicht deaktiviert werden, aber Sie können die unter [configure the Outbound Spam Policy](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx)beschriebenen Einstellungen konfigurieren. Wenn Sie zu viel Spam in Office 365 Bedenken, verwenden Sie ausgehende Filterung, um Spam in Exchange Online zu verhindern.
  
## <a name="beyond-the-basics-more-ways-to-prevent-spam-in-office-365"></a>Jenseits der Grundlagen: Weitere Möglichkeiten zum Verhindern von Spam in Office 365

 **Nachrichtenfluss Regeln**: Wenn Sie über die integrierte Spamfilterung hinausgehen und benutzerdefinierte Regeln erstellen möchten, die auf Ihren Geschäftsrichtlinien basieren, sind _[Nachrichtenfluss Regeln](https://technet.microsoft.com/library/jj919238%28v=exchg.150%29.aspx)_ (auch als _Transportregeln_bezeichnet) ein weiterer Filter, der Ihnen hilft, Spam in Office zu verhindern. 365. Sie können beispielsweise Nachrichtenfluss Regeln verwenden, um den SCL-Wert (Spam Confidence Level) für Nachrichten festzulegen, die bestimmten Bedingungen entsprechen, wie in [Verwenden von Nachrichtenfluss Regeln zum Festlegen der SCL-Bewertung (Spam Confidence Level) in Nachrichten](use-mail-flow-rules-to-set-the-spam-confidence-level-scl-in-messages.md)beschrieben.
  
 **E-Mail-Authentifizierung**: Techniken, die das Domain Name System (DNS) zum Hinzufügen überprüfbarer Informationen zu e-Mail-Nachrichten zum Absender einer e-Mail-Nachricht verwenden, werden als e-Mail-Authentifizierung bezeichnet Fortgeschrittenere Office 365-Administratoren können diese e-Mail-Authentifizierungsmethoden verwenden:
  
- **Sender Policy Framework (SPF)**: SPF überprüft den Ursprung von e-Mail-Nachrichten, indem die IP-Adresse des Absenders anhand des mutmaßlichen Besitzers der sendenden Domäne überprüft wird. Eine kurze Einführung in SPF und die schnelle Konfiguration finden Sie unter [Set up SPF in Office 365 to help prevent spoofing](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx). Ausführlichere Informationen zur Verwendung von SPF durch Office 365 oder zur Problembehandlung oder zu nicht standardmäßigen Bereitstellungen, z. B. Hybridbereitstellungen, finden Sie unter [How Office 365 uses Sender Policy Framework (SPF) to prevent spoofing](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx).

- **DomainKeys Identified Mail (DKIM)**: DKIM ermöglicht das Anfügen einer digitalen Signatur an e-Mail-Nachrichten im Nachrichtenkopf von e-Mails, die Sie senden. E-Mail-Systeme, die e-Mails von Ihrer Domäne empfangen, verwenden diese digitale Signatur, um zu ermitteln, ob eingehende e-Mails, die Sie erhalten, legitim sind. Informationen zu DKIM und Office 365 finden Sie unter [Verwenden von DKIM zum Überprüfen ausgehender e-Mails, die von Ihrer Domäne in office 365 gesendet werden](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx).

- **Domänenbasierte Nachrichtenauthentifizierung,-Berichterstellung und-Konformität (DMARC)**: DMARC hilft beim Empfang von e-Mail-Systemen, zu bestimmen, was mit Nachrichten zu tun hat, die SPF-oder DKIM-Prüfungen durchführen, und eine weitere Vertrauensebene für Ihre e-Mail-Partner Informationen zum Einrichten von DMARC finden Sie unter [Verwenden von DMARC zum Überprüfen von e-Mails in Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).

Wenn Sie sich Sorgen über Spam, Phishing und Spoofing in Office 365 machen, verwenden Sie SPF-, DKIM-und DMARC zusammen, um Spam und unerwünschte Spoofing zu verhindern.
  
 **Verwaltete Einstellungen**für Endbenutzer: Informationen dazu, wie Endbenutzer ihre eigenen Spameinstellungen verwalten können, finden Sie unter [Übersicht über den Junk-e-Mail-Filter](https://go.microsoft.com/fwlink/?LinkId=270065) (für Microsoft Outlook-Benutzer) oder [erfahren Sie mehr über Junk-e-Mails und Phishing](https://go.microsoft.com/fwlink/?LinkId=270068) (für Outlook im Web-Benutzer). Wenn Sie EOP verwenden, um lokale Postfächer zu schützen, müssen Sie die Verzeichnissynchronisierung verwenden, um sicherzustellen, dass diese Einstellungen mit dem Dienst synchronisiert werden. Weitere Informationen zum Einrichten der Verzeichnissynchronisierung finden Sie unter "Verwalten von E-Mail-Benutzern durch Verzeichnissynchronisierung" in [Verwalten von E-Mail-Benutzern in EOP](https://technet.microsoft.com/library/dn636911%28v=exchg.150%29.aspx).
  
## <a name="for-more-information"></a>Weitere Informationen

[Blog: Warum werden Spam und Phishing über Office 365?](https://go.microsoft.com/fwlink/?LinkId=528179 )
  
[Häufig gestellte Fragen zum Antispamschutz](https://technet.microsoft.com/library/jj937231%28v=exchg.150%29.aspx)
  
[Verwenden einer Liste sicherer IP-Adressen oder anderer Techniken, um zu verhindern, dass falsch positive E-Mails als Spam markiert werden](prevent-email-from-being-marked-as-spam-0.md)
  
[Einrichten von Office 365-Spamfilterung zur Unterstützung der Blockierung von Junk-e-Mails](reduce-spam-email.md)
  
[Was ist der Unterschied zwischen Junk-e-Mails und Massen-e-Mails?](https://technet.microsoft.com/library/dn720441%28v=exchg.150%29.aspx)
  
[Antispam-Nachrichtenkopfzeilen](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)
  
[Rückläufer Nachrichten und EOP](https://technet.microsoft.com/library/dn499795%28v=exchg.150%29.aspx)

## <a name="more-resources"></a>Weitere Ressourcen

[Abrufen von Hilfe bei den Office 365-Community-Foren](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[Administratoren: Melden Sie sich an, und erstellen Sie eine Serviceanfrage](https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[Administratoren: Rufen Sie den Support an](https://go.microsoft.com/fwlink/p/?LinkID=518322)
