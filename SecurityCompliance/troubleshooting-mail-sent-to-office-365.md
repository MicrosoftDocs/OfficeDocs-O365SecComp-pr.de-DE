---
title: Problembehandlung für E-Mail-Nachrichten, die an Office 365 gesendet werden
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 5/2/2016
ms.audience: ITPro
ms.topic: troubleshooting
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: f4caa4e1-e414-4b21-8822-31c08064c059
ms.collection:
- M365-security-compliance
description: Dieser Artikel enthält Informationen zur Problembehandlung für Absender, die Probleme haben, E-Mails an Postfächer in Office 365 zu senden, und bewährte Methoden für Massenmailings an Office 365-Kunden.
ms.openlocfilehash: ac465e7ef42b9cfeb2587481202fab1b5adb5f75
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265907"
---
# <a name="troubleshooting-mail-sent-to-office-365"></a>Problembehandlung für E-Mail-Nachrichten, die an Office 365 gesendet werden

Dieser Artikel enthält Informationen zur Problembehandlung für Absender, die Probleme haben, E-Mails an Postfächer in Office 365 zu senden, und bewährte Methoden für Massenmailings an Office 365-Kunden.
  
## <a name="troubleshooting-common-problems-with-mail-delivery-to-office-365"></a>Problembehandlung bei häufig auftretenden Probleme mit E-Mail-Übermittlung an Office 365

Wählen Sie aus den folgenden häufig auftretenden Problemen.
  
- [Verwalten Sie die Sendezuverlässigkeit Ihrer IP-Adresse und Ihrer Domäne?](troubleshooting-mail-sent-to-office-365.md#ManageRep)
    
- [Senden Sie E-Mails von neuen IP-Adressen?](troubleshooting-mail-sent-to-office-365.md#NewIPs)
    
- [Bestätigen, dass Ihr DNS ordnungsgemäß eingerichtet ist](troubleshooting-mail-sent-to-office-365.md#ConfirmDNSsetup)
    
- [Stellen Sie sicher, dass Sie sich selbst nicht als nicht routbare IP-Adresse bewerben.](troubleshooting-mail-sent-to-office-365.md#NoReverseDNS)
    
- [Sie haben einen Unzustellbarkeitsbericht (NDR) beim Senden von E-Mails an einen Benutzer in Office 365 erhalten.](troubleshooting-mail-sent-to-office-365.md#NDRInbound)
    
- [Meine E-Mails sind im Junk-Ordner des Empfängers in EOP gelandet.](troubleshooting-mail-sent-to-office-365.md#JunkMailBox)
    
- [Datenverkehr von meiner IP-Adresse wird durch EOP beschränkt.](troubleshooting-mail-sent-to-office-365.md#AllowEOPIPs)
    
### <a name="are-you-managing-your-ip-and-domains-sending-reputation"></a>Verwalten Sie die Sendezuverlässigkeit Ihrer IP-Adresse und Ihrer Domäne?
<a name="ManageRep"> </a>

EOP-Filtertechnologien sollen Anti-Spam-Schutz für Microsoft Office 365 sowie andere Microsoft-Produkte wie Exchange Server, Microsoft Office Outlook und Windows Live Mail bereitstellen. Wir nutzen auch SPF, DKIM und DMARC; E-Mail-Authentifizierungstechnologien, mit denen das Problem des Spoofings und Phishings durch Überprüfen, ob die Domäne, die die E-Mail sendet, dazu berechtigt ist, gelöst werden kann. EOP-Filter werden von einer Reihe von Faktoren der sendenden IP-Adresse, Domäne, Authentifizierung, Listengenauigkeit, Beschwerdehäufigkeit, Inhalte und mehr beeinflusst. Einer der wichtigsten Faktoren ist das Reduzieren der Absenderzuverlässigkeit und der Möglichkeit der E-Mail-Zustellung durch die Junk-E-Mail-Beschwerdehäufigkeit. 
  
### <a name="are-you-sending-email-from-new-ip-addresses"></a>Senden Sie E-Mails von neuen IP-Adressen?
<a name="NewIPs"> </a>

IP-Adressen, die bisher nicht verwendet wurden, um E-Mails zu senden, verfügen in der Regel in unseren Systemen über keinerlei Zuverlässigkeitswertung. Dementsprechend gibt es bei E-Mails von neuen IP-Adressen eher Übermittlungsprobleme. Nachdem die IP-Adresse eine gewisse Zuverlässigkeit aufgebaut hat, da kein Spam gesendet wurde, lässt EOP in der Regel eine bessere E-Mail-Übermittlung zu.
  
Neue IP-Adressen, die für Domänen hinzugefügt werden, die unter den vorhandenen SPF-Einträgen authentifiziert werden, haben in der Regel den Vorteil, einen Teil der Sendezuverlässigkeit der Domäne zu erben. Hat Ihre Domäne eine gute Sendezuverlässigkeit, wird er Vorgang bei neuen IP-Adressen möglicherweise beschleunigt. Eine neue IP-Adresse kann innerhalb von zwei Wochen oder früher – je nach Volumen, Listengenauigkeit und Junk-E-Mail-Beschwerdehäufigkeit – als zuverlässig anerkannt werden.
  
### <a name="confirm-that-your-dns-is-set-up-correctly"></a>Bestätigen, dass Ihr DNS ordnungsgemäß eingerichtet ist
<a name="ConfirmDNSsetup"> </a>

Anweisungen zum Erstellen und Verwalten von DNS-Einträgen, einschließlich des MX-Eintrags für E-Mail-Weiterleitung, erhalten Sie von Ihrem DNS-Hostinganbieter.
  
### <a name="ensure-that-you-do-not-advertise-yourself-as-a-non-routable-ip"></a>Stellen Sie sicher, dass Sie sich selbst nicht als nicht routbare IP-Adresse bewerben.
<a name="NoReverseDNS"> </a>

Wir akzeptieren möglicherweise keine E-Mail-Nachrichten von Absendern, für die eine Reverse-DNS-Suche fehlschlägt. In einigen Fällen bewerben sich seriöse Absender fälschlicherweise als nicht routbare IP-Adresse bei dem Versuch, eine Verbindung zu EOP zu öffnen. IP-Adressen, die für private (nicht routbare) Netzwerke reserviert sind, enthalten:
  
- 192.168.0.0/16 (oder 192.168.0.0 - 192.168.255.255)
    
- 10.0.0.0/8 (oder 10.0.0.0 - 10.255.255.255)
    
- 172.16.0.0/11 (oder 172.16.0.0 - 172.31.255.255)
    
### <a name="you-received-a-non-delivery-report-ndr-when-sending-email-to-a-user-in-office-365"></a>Sie haben einen Unzustellbarkeitsbericht (NDR) beim Senden von E-Mails an einen Benutzer in Office 365 erhalten.
<a name="NDRInbound"> </a>

Einige Probleme bei der Übermittlung sind das Ergebnis der IP-Adresse des Absenders, die von Microsoft blockiert wird, oder weil das Benutzerkonto als gesperrter Absender aufgrund von vorherigen Spam-Aktivitäten identifiziert wird. Wenn Sie glauben, dass Sie den NDR irrtümlich erhalten haben, führen Sie zunächst alle Anweisungen in der NDR-Nachricht aus, um das Problem zu beheben. 
  
Weitere Informationen zu dem Fehler, den Sie erhalten haben, finden Sie in der vollständigen Liste der SMTP-Fehlercodes in [DSNs and NDRs in On-Premises Exchange 2013 and Office 365](http://technet.microsoft.com/library/8e91de84-76fa-49b2-898c-c5eface76560.aspx).
  
 Wenn Sie z. B. den folgenden Unzustellbarkeitsbericht erhalten haben, wurde die IP-Adresse des Absenders wahrscheinlich durch Microsoft blockiert. 
  
 `550 5.7.606-649 Access denied, banned sending IP [x.x.x.x]; To request removal from this list please visit https://sender.office.com/ and follow the directions.`
  
Um die Entfernung aus dieser Liste anzufordern, können Sie wie folgt vorgehen: [Verwenden des Listenentfernungsportals, um sich selbst aus der Liste der blockierten Absender von Office 365 zu entfernen](use-the-delist-portal-to-remove-yourself-from-the-office-365-blocked-senders-lis.md).
  
### <a name="my-email-landed-in-the-recipients-junk-folder-in-eop"></a>Meine E-Mails sind im Junk-Ordner des Empfängers in EOP gelandet.
<a name="JunkMailBox"> </a>

Falls eine Nachricht fälschlicherweise von EOP als Spam identifiziert wurde, können Sie diese falsch positive Nachricht zusammen mit dem Empfänger an das Microsoft-Spamanalyseteam weiterleiten, das die Nachricht bewertet und untersucht. Abhängig vom Ergebnis der Analyse werden die Filterregeln für Spaminhalte des Diensts angepasst, damit die Nachricht zugestellt werden kann. Sie können Nachrichten, die nicht als Spam klassifiziert werden sollen, per E-Mail an Microsoft weiterleiten. Gehen Sie dabei wie folgt vor.
  
### <a name="to-use-email-to-submit-false-positive-messages-to-the-microsoft-spam-analysis-team"></a>So verwenden Sie eine E-Mail, um falsch positive Nachrichten an das Microsoft-Spamanalyseteam zu senden

1. Speichern Sie die an Microsoft zu sendende Nachricht als Nicht-Spamnachricht.
    
2. Erstellen Sie eine neue, leere Nachricht und hängen die Nichtspamnachricht an.
    
    Sie können bei Bedarf mehrere Nicht-Spamnachrichten anhängen.
    
3. Kopieren Sie den Betreff der ursprünglichen Nachricht, und fügen Sie ihn in den Betreff der neuen Nachricht ein.
    
    > [!IMPORTANT]
    > Lassen Sie den Nachrichtentext leer. 
  
4. Senden Sie Ihre neue Nachricht an [not_junk@office365.microsoft.com](mailto:not_junk@office365.microsoft.com).
    
### <a name="traffic-from-my-ip-address-is-throttled-by-eop"></a>Datenverkehr von meiner IP-Adresse wird durch EOP beschränkt.
<a name="AllowEOPIPs"> </a>

Wenn Sie einen Unzustellbarkeitsbericht von EOP erhalten, der angibt, dass Ihre IP-Adresse von EOP beschränkt wird, z. B.:
  
 `host xxxx.outlook.com [x.x.x.x]: 451 4.7.550 Access denied, please try again later`
  
Sie haben einen NDR erhalten, da an der betreffenden IP-Adresse eine verdächtige Aktivität erfasst. Die IP-Adresse wurde vorübergehend beschränkt, solange sie weiter ausgewertet wird. Wenn der Verdacht durch Bewertung aufgelöst wird, wird diese Einschränkung in Kürze aufgehoben.
  
### <a name="i-cant-receive-email-from-senders-in-office-365"></a>Ich kann keine E-Mails von Absendern in Office 365 erhalten.
<a name="AllowEOPIPs"> </a>

 Damit Sie Nachrichten von unseren Benutzern empfangen können, muss Ihr Netzwerk Verbindungen von den IP-Adressen zulassen, die EOP in unseren Rechenzentren verwendet. Weitere Informationen finden Sie unter [Exchange Online Protection-IP-Adressen](eop/exchange-online-protection-ip-addresses.md). 
  
## <a name="best-practices-for-bulk-emailing-to-office-365-users"></a>Bewährte Methoden für Massen-E-Mails an Office 365-Benutzer
<a name="BulkMailer"> </a>

Wenn Sie häufig Massen-E-Mail-Kampagnen für Benutzer von Office 365 durchführen und sicherstellen möchten, dass Ihre E-Mails sicher und zeitnah eintreffen, folgen Sie den Tipps in diesem Abschnitt.
  
### <a name="ensure-that-the-from-name-reflects-who-is-sending-the-message"></a>Stellen Sie sicher, dass der Name unter „Von:“ angibt, wer die Nachricht sendet.

Der Betreff sollte eine kurze Zusammenfassung der Nachricht darstellen, und der Nachrichtentext sollte klar und eindeutig angeben, um was es beim Angebot, Dienst oder Produkt geht. Beispiel:
  
Richtig
  
 ` From: marketing@shoppershandbag.com `
  
 `Subject: Updated catalog for the Christmas season!`
  
Falsch
  
 `From: someone@outlook.com`
  
 `Subject: Catalogs`
  
Je einfacher Sie es den Benutzern machen, ihre Identität und Absichten zu erkennen, desto weniger Probleme haben Sie bei der Zustellung durch die meisten Spamfilter.
  
### <a name="always-include-an-unsubscribe-option-in-campaign-emails"></a>Schließen Sie in Kampagnen-E-Mails immer eine Option zum Abbestellen ein.

Marketing-E-Mails, insbesondere Newsletter, sollten immer eine Möglichkeit enthalten, zukünftige E-Mails abzubestellen. Beispiel:
  
 `This email was sent to example@contoso.com by sender@fabrikam.com.`
  
 `Update Profile/Email Address | Instant removal with SafeUnsubscribe™ | Privacy Policy`
  
Einige Absender fügen diese Option hinzu, indem Empfänger eine E-Mail-Nachricht an einen bestimmten Alias mit „Unsubscribe" im Betreff senden müssen. Das oben genannte Ein-Klick-Beispiel ist aber vorzuziehen. Wenn Sie sich dafür entscheiden, dass Empfänger eine E-Mail senden müssen, stellen Sie sicher, dass alle erforderlichen Felder bereits ausgefüllt sind, wenn sie auf den Link klicken.
  
### <a name="use-the-double-opt-in-option-for-marketing-email-or-newsletter-registration"></a>Verwenden der doppelten Anmeldeoption für die Registrierung für Marketing-E-Mails oder Newsletter

Die bewährte Methode der Branche wird empfohlen, wenn Ihr Unternehmen möchte, dass Benutzer ihre Kontaktinformationen registrieren, um auf das Produkt oder den Dienst zuzugreifen. In einigen Unternehmen werden Benutzer automatisch während der Registrierung für Marketing-E-Mails oder Newsletter angemeldet, was aber als fragliche Marketingmethode in der Welt der E-Mail-Filterung angesehen wird.
  
Wenn während der Registrierung Kontrollkästchen wie „Ja, Newsletter senden" oder „Ja, Sonderangebote senden" standardmäßig aktiviert sind, können sich Benutzer, die nicht darauf achten, versehentlich für Marketing-E-Mails oder Newsletter anmelden, die sie nicht erhalten möchten.
  
 Es empfiehlt sich stattdessen die doppelte Anmeldeoption, was bedeutet, dass das Kontrollkästchen für Marketing-E-Mails oder Newsletter standardmäßig deaktiviert ist. Nachdem das Registrierungsformular gesendet wurde, wird zudem eine Überprüfungs-E-Mail mit einer URL an den Benutzer gesendet, die es ihm ermöglicht, seine Entscheidung für Marketing-E-Mails zu bestätigen. 
  
 Dadurch wird sichergestellt, dass nur Benutzer, die Marketing-E-Mails erhalten möchten, für die E-Mail-Nachrichten angemeldet werden, und das sendende Unternehmen setzt keine fraglichen E-Mail-Marketingmethoden ein. 
  
### <a name="ensure-that-email-message-content-is-transparent-and-traceable"></a>Sicherstellen, dass E-Mail-Nachrichteninhalte transparent und nachverfolgbar sind

Der Inhalt von E-Mails ist genauso wichtig wie die Sendemethode. Beim Erstellen von E-Mail-Inhalt verwenden Sie die folgenden bewährten Methoden, um sicherzustellen, dass die E-Mails nicht durch E-Mail-Filterdienste gekennzeichnet werden:
  
- Wenn die E-Mail Empfänger dazu auffordert, den Absender zum Adressbuch hinzuzufügen, sollte deutlich darauf hingewiesen werden, dass dies keine Übermittlungsgarantie darstellt.
    
- Weiterleitungen im Textkörper der Nachricht sollten ähnlich und konsistent sein, nicht zahlreich und unterschiedlich. Eine Weiterleitung ist in diesem Kontext etwas, das von der Nachricht wegführt, z. B. Links und Dokumente. Wenn Sie viele Werbe- oder Abbestellungslinks haben oder die Profillinks aktualisieren, sollten sie alle auf dieselbe Domäne verweisen. Beispiel:
    
    Richtig
    
     `unsubscribe.bulkmailer.com`
    
     `profile.bulkmailer.com`
    
     `options.bulkmailer.com`
    
    Falsch
    
     `unsubscribe.bulkmailer.com`
    
     `profiles.excite.com`
    
     `options.yahoo.com`
    
- Senden Sie keine Inhalte mit großen Bilder oder Anlagen und keine Nachrichten, die nur aus einem Bild bestehen.
    
- Ihre öffentlichen Datenschutz- oder P3P-Einstellungen sollten deutlich angeben, dass Sie Nachverfolgungspixel (Web-Bugs oder Beacons) verwenden.
    
### <a name="remove-incorrect-email-aliases-from-your-databases"></a>Entfernen falscher E-Mail-Aliasnamen aus den Datenbanken

Jeder E-Mail-Alias in der Datenbank, die eine Rücksendung auslöst, ist unnötig und kann dazu führen, dass Ihre ausgehenden E-Mails für weitere Analysen durch E-Mail-Filterdienste herangezogen werden. Stellen Sie sicher, dass Ihre E-Mail-Datenbank auf dem neuesten Stand ist.
  

