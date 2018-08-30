---
title: Office 365 e-Mail-Anti-Spam-Schutz
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 6/29/2018
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 6a601501-a6a8-4559-b2e7-56b59c96a586
description: Lernen Sie die Anti-Spam-Einstellungen und Filter, die helfen, dass Sie verhindern, dass Spam in Exchange Online und Office 365. Abrufen von zu viel Spam in Office 365? Sie können Ihre Spam-Filter und Anti-Spam-Richtlinieneinstellungen anpassen.
ms.openlocfilehash: 5547904633a0be9ad57fa7431aeddf1267871662
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529484"
---
# <a name="office-365-email-anti-spam-protection"></a>Office 365 e-Mail-Anti-Spam-Schutz

Sind Sie zu viel Spam in Office 365 Bedenken? Wir haben mehrere Spam-Filter in Ihrem Office 365 oder Exchange Online Protection (EOP)-Dienst integriert, sodass Ihre e-Mail-Adresse ab dem Zeitpunkt geschützt ist Sie Ihre erste Meldung. Um Spam in Office 365 zu verhindern, möchten Sie möglicherweise eine Protection-Einstellung für den Umgang mit einem bestimmten Problem in Ihrer Organisation ändern – sagen Sie sind sehr viel Spam beispielsweise von einem bestimmten Absender, empfangen – oder einfach fein einstellen Ihre Einstellungen, damit sie sind auf bewährte Erfüllung die Anforderungen Ihrer Organisation zugeschnitten. Zu diesem Zweck können Sie ändern, Anti-Spam-Einstellungen in der Office 365-Sicherheit &amp; Compliance Center.
  
In diesem Artikel ist für Office 365-Administratoren vorgesehen. Wenn Sie nicht Administrator, aber Sie Office 365-Benutzer sind und Sie erfahren, wie für den Umgang mit Spam, die Sie erhalten möchten, nicht im Artikel, die, den Sie benötigen. Stattdessen, wenn Sie Outlook für PC oder Outlook für Mac verwenden, beginnen Sie mit [Übersicht über den Junk-e-Mail-Filter](https://support.office.com/article/5ae3ea8e-cf41-4fa0-b02a-3b96e21de089). Wenn Sie Outlook im Web verwenden, beginnen Sie mit [Informationen zu junk-e-Mail- und Phishing](https://support.office.com/article/86c1d76f-4d5a-4967-9647-35665dc17c31).
  
## <a name="these-options-help-you-prevent-spam-in-office-365"></a>Mit diesen Optionen können Sie verhindern, dass Spam in Office 365

 **Verbindungsfilter.** Wenn Sie Verbindungsfilter verwenden, wird Office 365 vor dem eine Nachricht holen Sie sich über die Reputation des Absenders überprüft. Sie können eine Liste zugelassener oder Liste mit sicheren Absendern, um sicherzustellen, dass Sie alle von einer bestimmten IP-Adresse oder die IP-Adressbereich an Sie gesendeten Nachrichten erhalten erstellen. Sie können auch eine Liste der IP-Adressen aus dem Blockieren von Nachrichten, so genannte eine Sperrliste erstellen. Weitere Informationen finden Sie unter [Configure the Connection Filter Policy](https://technet.microsoft.com/library/jj200718%28v=exchg.150%29.aspx). Wenn Sie Spam in Office 365 besorgt sind, verwenden Sie die verbindungsfilterung so verhindern von Spam.
  
Für Kunden, die über Office 365 Enterprise E5 oder erweiterte Threat Protection (ATP) Lizenzen erworben haben, Verbindungsfilter wird durch Spoofing Intelligence erstellen zulassen oder Blockieren von Listen der Absender, die Ihre Domäne spoofing sind. Weitere Informationen finden Sie unter [erfahren Sie mehr über Spoofing Intelligence](https://go.microsoft.com/fwlink/?LinkID=735009).
  
 **Spamfilterung.** Office 365 überprüft Nachrichtenmerkmalen Spam mithilfe von Filtern von Spam. Sie können ändern, welche Aktionen für Nachrichten, die als Spam identifiziert übernehmen und auswählen, ob Filtern von Nachrichten in bestimmten Sprachen geschrieben oder von bestimmten Ländern oder Regionen gesendet. Sie können auch aktivieren, klicken Sie auf Erweiterte spamfilterungsoptionen Wenn Sie einen aggressiven Ansatz zum Filtern von Spam-verfolgen möchten. Darüber hinaus können Sie spambenachrichtigungen, um Benutzer zu benachrichtigen, wenn für sie bestimmte Nachrichten unter Quarantäne gestellt wurden stattdessen konfigurieren. (Senden von Nachrichten in Quarantäne ist eine der konfigurierbaren Aktionen.) Diese Benachrichtigungen können Endbenutzer falsch positive Ergebnisse freigeben und zur Analyse an Microsoft gemeldet. Weitere Informationen finden Sie unter [Konfigurieren von Richtlinien Ihrer Spam-Filter](https://go.microsoft.com/fwlink/p/?LinkId=617147). Um Hilfe zu verhindern, dass Spam in Office 365, Filtern von Spam verwenden, wenn Sie zu viele unerwünschte e-Mails in Office 365 besorgt sind, verwenden Sie Verbindungsfilter um Spam zu verhindern.
  
> [!NOTE]
> Für Kunden, die eigenständige EOP: standardmäßig die EOP-Spam-Filter als Spam erkannten Nachrichten an jeden Empfänger Junk-e-Mail-Ordner senden. Um sicherzustellen, dass die **Nachricht in Junk-e-Mail-Ordner verschieben** -Aktion mit lokalen Postfächern funktioniert, müssen Sie jedoch zwei Exchange-Transportregeln auf Ihren lokalen Servern zum Erkennen von Spam-Headern von EOP hinzugefügte konfigurieren. Weitere Informationen hierzu finden Sie unter [sicherstellen, dass Spam an die Junk-e-Mail-Ordner des Benutzers weitergeleitet wird](https://technet.microsoft.com/library/jj837173%28v=exchg.150%29.aspx). 
  
## <a name="extra-information-if-you-receive-too-much-spam-in-office-365"></a>Wenn Sie in Office 365 zu viel Spam erhalten zusätzliche Informationen

Das folgende Video bietet eine Übersicht über das Konfigurieren von Spamfilterung in EOP.
  
> [!VIDEO https://www.microsoft.com/videoplayer/embed/608be94c-d763-4c47-af94-99e7cb277713?autoplay=false]
  
Weitere Informationen finden Sie unter das Thema [Configure Spam-Filterrichtlinien](https://go.microsoft.com/fwlink/p/?LinkId=617147) . 
  
## <a name="check-your-outgoing-messages-to-prevent-spam-in-office-365"></a>Überprüfen Sie Ihren ausgehenden Nachrichten zur Verhinderung von Spam in Office 365

 **Ausgehende Filterung.** Office 365 überprüft auch dafür sorgen, dass Ihre Benutzer keine Spamnachrichten senden. Beispielsweise erhalten möchten dem Computer eines Benutzers mit Malware infiziert, die zum Senden von Spamnachrichten, damit wir zum Erstellen von Schutz vor, die *ausgehende Filterung* aufgerufen wird. Sie können nicht die ausgehende Filterung deaktivieren, aber Sie können die Einstellungen unter [Konfigurieren der Richtlinie für ausgehende Spamnachrichten](https://technet.microsoft.com/library/jj200737%28v=exchg.150%29.aspx)beschrieben konfigurieren. Wenn Sie zu viele unerwünschte e-Mails in Office 365 besorgt sind, verwenden Sie ausgehende Filterung, um zu verhindern, dass Spam in Exchange Online.
  
## <a name="beyond-the-basics-more-ways-to-prevent-spam-in-office-365"></a>Weiterführendes: Weitere Möglichkeiten zur Verhinderung von Spam in Office 365
<a name="BeyondBasics"> </a>

 **E-Mail-Flussregeln.** Wenn Sie integrierte Spamfilterung hinausgehen und Erstellen von benutzerdefinierten Regeln, die basieren auf Ihren Geschäftsrichtlinien *[e-Mail-Flussregeln](https://technet.microsoft.com/library/jj919238%28v=exchg.150%29.aspx)* , auch als *Transportregeln* bezeichnet werden, sind möchten einen weiteren Filter, mit denen Sie verhindern, dass Spam in Office 365. Beispielsweise können Sie e-Mail-Flussregeln verwenden, um Spam Confidence Level (SCL) Wert für Nachrichten, die bestimmte Suchkriterien übereinstimmen festzulegen, wie unter [Verwenden von e-Mail-Flussregeln, um die Spam Confidence Level (SCL) in Nachrichten festzulegen](https://technet.microsoft.com/library/dn798345%28v=exchg.150%29.aspx). 
  
 **E-Mail-Authentifizierung.** Techniken, die das Domain Name System (DNS) verwenden, um e-Mail-Nachrichten über den Absender einer e-Mail-Nachricht überprüfbaren Informationen, die hinzugefügt werden e-Mail-Authentifizierung bezeichnet. Erweiterte Office 365, die Administratoren vornehmen können Verwenden dieser e-Mail-Authentifizierungsmethoden Sie Folgendes: 
  
- **Sender Policy Framework (SPF).** SPF überprüft Ursprung des e-Mail-Nachrichten mithilfe die IP-Adresse des Absenders gegen den möglichen Besitzer der sendenden Domäne überprüfen. Eine kurze Einführung in SPF und erhalten sie schnell konfiguriert finden Sie unter [Einrichten von SPF in Office 365, um spoofing zu verhindern](https://technet.microsoft.com/library/dn789058%28v=exchg.150%29.aspx). Ausführlichere Informationen zu der Verwendung von Office 365 SPF oder zur Problembehandlung oder nicht standardmäßigen Bereitstellungen wie hybridbereitstellungen beginnen Sie mit [wie Office 365 verwendet Sender Policy Framework (SPF), um spoofing zu verhindern](https://technet.microsoft.com/library/mt712724%28v=exchg.150%29.aspx).
    
- **DomainKeys Mail (DKIM) identifiziert.** DKIM kann fügen Sie eine digitale Signatur an e-Mail-Nachrichten in der Kopfzeile der e-Mail-Nachrichten senden. E-Mail-Systemen, die e-Mail von Ihrer Domäne empfangen verwenden diese digitale Signatur um zu ermitteln, ob eingehender e-Mail, den sie erhalten legitime ist. Informationen zu DKIM und Office 365 finden Sie unter [DKIM verwenden, um von Ihrer Domäne in Office 365 gesendete e-Mails zu überprüfen](https://technet.microsoft.com/library/mt695945%28v=exchg.150%29.aspx).
    
- **Domänenbasierte Nachrichtenauthentifizierung, Reporting und Konformität (DMARC).** Empfangen von e-Mail-Systemen DMARC hilft bestimmen, was mit Nachrichten zu tun, die ausfallen SPF oder DKIM Überprüfungen oder einer anderen Vertrauensstellung für die e-Mail-Partner bietet. Informationen zum Einrichten von DMARC finden Sie unter [Verwendung von DMARC zum Überprüfen von e-Mail in Office 365](https://technet.microsoft.com/library/mt734386%28v=exchg.150%29.aspx).
    
Wenn Sie die betreffenden Informationen zu Spam, Phishing und spoofing in Office 365 sind, verwenden Sie SPF, DKIM und DMARC zusammen um Spam und unerwünschte spoofing zu verhindern.
  
 **Endbenutzer Einstellungen für verwaltete.** Wenn der gesuchte Informationen wie Endbenutzer ihre eigenen Spameinstellungen verwalten können, checken Sie [Übersicht über den Junk-e-Mail-Filter](https://go.microsoft.com/fwlink/?LinkId=270065) (für Microsoft Outlook-Benutzer) oder [Informationen zu Junk-e-Mail- und Phishing](https://go.microsoft.com/fwlink/?LinkId=270068) (für Outlook auf dem Web-Benutzer aus). Wenn Sie EOP zum Schutz von lokalen Postfächern verwenden, müssen Sie verzeichnissynchronisierung verwenden, um sicherzustellen, dass diese Einstellungen mit dem Dienst synchronisiert werden. Weitere Informationen zum Einrichten von verzeichnissynchronisierung finden Sie unter "verzeichnissynchronisierung zum Verwalten von e-Mail-Benutzer" in [Manage Mail Users in EOP](https://technet.microsoft.com/library/dn636911%28v=exchg.150%29.aspx).
  
## <a name="for-more-information"></a>Weitere Informationen
<a name="BeyondBasics"> </a>

[Blog: Warum erhält Spam und Phishing über Office 365?](https://go.microsoft.com/fwlink/?LinkId=528179 )
  
[Häufig gestellte Fragen zum Antispamschutz](https://technet.microsoft.com/library/jj937231%28v=exchg.150%29.aspx)
  
[Verwenden von sicheren Listen oder anderen Techniken, um zu verhindern, dass falsch positive E-Mails als Spam markiert werden](prevent-email-from-being-marked-as-spam-0.md)
  
[Zum Einrichten von Office 365 Spamfilterung, mit denen Junk-e-Blockieren von Nachrichten](block-email-spam-to-prevent-false-negatives.md)
  
[Was ist der Unterschied zwischen Junk Email and Bulk Email?](https://technet.microsoft.com/library/dn720441%28v=exchg.150%29.aspx)
  
[Antispam-Nachrichtenkopfzeilen](https://technet.microsoft.com/library/dn205071%28v=exchg.150%29.aspx)
  
[Rückläufernachrichten und EOP](https://technet.microsoft.com/library/dn499795%28v=exchg.150%29.aspx)
  
## <a name="still-need-help"></a>Benötigen Sie weitere Hilfe?
<a name="BeyondBasics"> </a>

[![Erhalten von Hilfe in den Communityforen von Office 365](media/12a746cc-184b-4288-908c-f718ce9c4ba5.png)](https://go.microsoft.com/fwlink/p/?LinkId=518605)
  
[![Administratoren: Anmelden und Serviceanfrage erstellen](media/10862798-181d-47a5-ae4f-3f8d5a2874d4.png)]( https://go.microsoft.com/fwlink/p/?LinkId=519124)
  
[![Administratoren: Support kontaktieren](media/9f262e67-e8c9-4fc0-85c2-b3f4cfbc064e.png)](https://go.microsoft.com/fwlink/p/?LinkID=518322)
  

