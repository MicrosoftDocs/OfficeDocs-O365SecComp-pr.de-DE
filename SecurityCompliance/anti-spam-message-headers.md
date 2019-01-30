---
title: Antispam-Nachrichtenkopfzeilen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
description: Wenn Exchange Online Protection eingehende E-Mail-Nachrichten prüft, wird jeder Nachricht die Kopfzeile **X-Forefront-Antispam-Report** hinzugefügt.
ms.openlocfilehash: d887fea94bac6177dde69fac9586d7d562ef50de
ms.sourcegitcommit: 03b9221d9885bcde1cdb5df2c2dc5d835802d299
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2019
ms.locfileid: "29614459"
---
# <a name="anti-spam-message-headers"></a>Antispam-Nachrichtenkopfzeilen

Wenn Exchange Online Protection eingehende E-Mail-Nachrichten prüft, wird jeder Nachricht die Kopfzeile **X-Forefront-Antispam-Report** hinzugefügt. Mit den Feldern in dieser Kopfzeile können Administratoren Information zur Nachricht und deren Verarbeitung bereitgestellt werden. Die Felder in der Kopfzeile **X-Microsoft-Antispam** liefern zusätzliche Informationen über Massensendungen und Phishing. Zusätzlich zu diesen beiden Kopfzeilen fügt Exchange Online Protection auch E-Mail-Authentifizierungsergebnisse für jede verarbeitete Nachricht in die Kopfzeile **Authentication-results** ein.
  
> [!TIP]
> Informationen dazu, wie Sie einen E-Mail-Nachrichtenkopf in verschiedenen E-Mail-Clients anzeigen, finden Sie unter [Message Header Analyzer](https://go.microsoft.com/fwlink/p/?LinkId=306583). Sie können den Inhalt der Nachrichtenkopfzeile kopieren und in der [Nachrichtenkopfanalyse](https://testconnectivity.microsoft.com/?tabid=mha) einfügen. Wenn Sie im Exchange Admin Center eine Nachricht in Quarantäne auswählen, können Sie über den Link **Nachrichtenkopfzeile anzeigen** ganz einfach den Text der Nachrichtenkopfzeile kopieren und im Tool einfügen. Klicken Sie im Nachrichtenkopfanalyse-Tool auf **Kopfzeilen analysieren**, um Informationen zur Kopfzeile abzurufen.
  
## <a name="x-forefront-antispam-report-message-header-fields"></a>Felder der Nachrichtenkopfzeile X-Forefront-Antispam-Report
<a name="sectionSection0"> </a>

Suchen Sie nach dem Zugriff auf die Nachrichtenkopfzeileninformationen nach **X-Forefront-Antispam-Report**, und suchen Sie nach den folgenden Feldern: Andere Felder in dieser Kopfzeile werden ausschließlich vom Microsoft-Antispamteam zu Diagnosezwecken verwendet.

|**Kopfzeilenfeld**|**Beschreibung**|
|:-----|:-----|
|CIP: [IP-Adresse]|Die IP-Verbindungsadresse. Sie sollten diese IP-Adresse angeben, wenn Sie im Verbindungsfilter eine IP-Zulassungsliste oder eine Liste für geblockte IP-Adressen erstellen. Weitere Informationen finden Sie unter [Konfigurieren der Verbindungsfilterrichtlinie](configure-the-connection-filter-policy.md).  |
|CTRY|Das Land, aus dem die Nachricht mit dem Dienst verbunden wurde. Es wird anhand der Verbindungs-IP-Adresse ermittelt, die nicht notwendigerweise mit der ursprünglichen Sende-IP-Adresse übereinstimmen muss.|
|LANG|Die Sprache, in der die Nachricht verfasst wurde, wie im Ländercode angegeben (z. B. ru_RU für Russisch).|
|SCL|Die SCL-Bewertung (Spam Confidence Level) einer Nachricht. Weitere Informationen zur Interpretation dieser Werte finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).  |
|PCL|Der PCL-Wert (Phishing Confidence Level) der Nachricht. Unter [PCL](anti-spam-message-headers.md#PCL) erhalten Sie weitere Informationen über PCL-Werte.  |
|SRV:BULK|Die Nachricht wurde als Massen-E-Mail identifiziert. Ist die erweiterte Spamfilteroption **Alle Massen-E-Mail-Nachrichten sperren** aktiviert, wird sie als Spam markiert. Ist die nicht aktiviert, wird sie nur dann als Spam markiert, wenn der Rest der Filterungsregeln festlegt, dass es sich bei der Nachricht um Spam handelt.  |
|SFV:SFE|Filterung wurde übersprungen, und die Nachricht wurde durchgelassen, da sie von einem Absender aus der Liste mit sicheren Absendern stammt.|
|SFV:BLK|Filterung wurde übersprungen, und die Nachricht wurde blockiert, da sie von einem Absender aus der Liste mit blockierten Absendern stammt.  <br/> **Tipp**: Weitere Informationen, wie Endbenutzer Listen sicherer und blockierter Absender erstellen können, finden Sie unter [Blockieren oder zulassen (junk-e-Mail-Einstellungen)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (Outlook im Web) und [Übersicht über den Junk-e-Mail-Filter](https://go.microsoft.com/fwlink/p/?LinkId=270065) (Outlook).|
|IPV:CAL|Die Nachricht wurde durch die Spam-Filter gelassen, weil die IP-Adrese in einer IP-Zulassungsliste im Verbindungsfilter angegeben wurde.|
|IPV:NLI|Die IP-Adresse war nicht in einer IP-Zuverlässigkeitsliste aufgeführt.|
|SFV:SPM|Die Nachricht wurde vom Inhaltsfilter als Spam markiert.|
|SFV:SKS|Die Nachricht wurde bereits als Spam markiert, noch bevor sie vom Inhaltsfilter verarbeitet wurde. Dies beinhaltet Nachrichten, bei denen die Nachricht einer Transportregel entsprach, die diese automatisch als Spam markiert und alle zusätzlichen Filterungen umgeht.|
|SFV:SKA|Die Nachricht hat das Filtern übersprungen und wurde im Posteingang zugestellt, da sie einer Zulassenliste in der Richtlinie für den Spamfilter entsprach, wie z. B. die Liste **Absender zulassen**.  |
|SFV:SKB|Die Nachricht wurde als Spam markiert, da sie einer Sperrliste in der Richtlinie für den Spamfilter entsprach, wie z. B. die Liste **Absender blockieren**.  |
|SFV:SKN|Die Nachricht wurde bereits als Nicht-Spam markiert, noch bevor sie vom Inhaltsfilter verarbeitet wurde. Dies beinhaltet Nachrichten, bei denen die Nachricht einer Transportregel entsprach, die diese automatisch als Nicht-Spam markiert und alle zusätzlichen Filterungen umgeht.|
|SFV:SKI|Ähnlich wie SFV:SKN, die Filterung der Nachricht wurde aus einem anderen Grund übersprungen, wie eine unternehmensinterne E-Mail innerhalb einer Mandantenstruktur.|
|SFV:SKQ|Die Nachricht wurde aus der Quarantäne freigegeben und an die vorgesehenen Empfänger gesendet.|
|SFV:NSPM|Die Nachricht wurde als "Nicht-Spam" markiert und an die vorgesehenen Empfänger gesendet.|
|H: [helostring]|Die Zeichenfolge HELO oder EHLO des verbundenen E-Mail-Servers.|
|PTR: [ReverseDNS]|Der PTR-Eintrag (bzw. der Zeigereintrag) der Absender-IP-Adresse, auch als Reverse-DNS-Adresse bezeichnet.|
|SFTY|Die Nachricht wurde als Phishing identifiziert und auch mit einem der folgenden Werte markiert werden: <br/>• 9.1: Standardwert. Die Nachricht enthält eine URL Phishing, möglicherweise andere Phishing Inhalte enthalten oder kann als gekennzeichnet wurden Phishing durch einen anderen e-Mail-Filter wie eine lokale Version von Exchange Server vor der Weiterleitung der Nachricht zu Office 365. <br/>• 9.11: Anti-spoofing überprüft die Nachricht nicht, in dem die sendende Domäne in der From: Kopfzeile ist identisch, ausgerichtet oder Teil derselben Organisation wie die empfangende Domäne ist. Dies gibt an, dass die Nachricht eine unternehmensinterne spoofing Safety Info hinzugefügt werden soll. <br/>• 9.19: Nachricht nicht erfolgreich Domäne Identitätswechsel Überprüfungen, in dem die sendende Domäne versucht, Identitätswechsel für eine Domäne, die im Besitz des Empfängers oder einer benutzerdefinierten Domäne, die durch die Richtlinie Anti-Phishing geschützt. Dies gibt an, dass ein Identitätswechsel Safety Tipp der Nachricht hinzugefügt werden soll, wenn über die Gruppenrichtlinie Anti-Phishig aktiviert. <br/>• 9,20: Benutzer Identitätswechsel Überprüfungen, an dem der sendende Benutzer versucht, einen Benutzer innerhalb der Organisation Ereignisempfänger imitieren oder einen benutzerdefinierten geschützte durch die Anti-Phishing-Richtlinie, die Nachricht nicht. Dies gibt an, dass ein Identitätswechsel Safety Tipp der Nachricht hinzugefügt werden soll, wenn über die Gruppenrichtlinie Anti-Phishig aktiviert. <br/>• 9.21: Nachricht nicht erfolgreich Anti-spoofing Prüfungen und die sendende Domäne in der From: Kopfzeile keine Authentifizierung und von einer externen Domäne ist. In Kombination mit CompAuth verwendet (Siehe das Ergebnis-Authentifizierung). <br/>• 9.22: identisch mit 9.21, mit der Ausnahme, dass der Benutzer einen sicheren Absender verfügt, die überschrieben wurde. <br/>• 9.23: identisch mit 9.22, außer dass die Organisation hat eine zulässige Absender oder die Domäne, die überschrieben wurde. <br/>• 9,24: identisch mit 9.23, mit der Ausnahme, dass der Benutzer eine Exchange Mail Flow Regel verfügt, die überschrieben wurde.|
|X-CustomSpam: [ASFOption]|Die Nachricht entsprach einer erweiterten spamfilterungsoptionen. Beispielsweise **X-CustomSpam: Links zu Remotestandorten Image** gibt an, dass die Option **Bildlinks zu Remotestandorten** ASF Übereinstimmung gefunden wurde. Um herauszufinden, welche X-Headertext für jede bestimmte ASF Option hinzugefügt wird, finden Sie unter [Erweiterte Spamfilterung Optionen](advanced-spam-filtering-asf-options.md).|
   
## <a name="x-microsoft-antispam-message-header-fields"></a>Felder der Nachrichtenkopfzeile X-Microsoft-Antispam
<a name="sectionSection1"> </a>

In der folgenden Tabelle werden die hilfreiche Felder der Nachrichtenkopfzeile **X-Microsoft-Antispam** beschrieben: Andere Felder in dieser Kopfzeile werden ausschließlich vom Microsoft-Antispamteam zu Diagnosezwecken verwendet.
  
|**Kopfzeilenfeld**|**Beschreibung**|
|:-----|:-----|
|BCL|Die BCL-Wert (Bulk Complaint Level) der Nachricht. Weitere Informationen finden Sie unter [BCL-Werte (Bulk Complaint Level)](bulk-complaint-level-values.md).  |
|PCL|Die Phishing Confidence Level (PCL) der Nachricht, die angibt, ob es eine Phishingnachricht darstellt. Dieser Status kann als eine der folgenden numerischen Werte zurückgegeben werden:<br/>• **0-3**: Inhalt der Nachricht ist wahrscheinlich Phishing werden nicht. <br/>• **4 bis 8**: die Nachricht Inhalt ist wahrscheinlich Phishing werden. <br/>• **-9990**: (Exchange Online Protection nur) die Meldung Inhalt ist wahrscheinlich Phishing werden.  <br/>  Die Werte werden bestimmt, welche Aktion Ihr e-Mail-Client für Nachrichten ausgeführt verwendet. Beispielsweise verwendet Outlook PCL Stempels den Inhalt von verdächtigen Nachrichten blockiert. Weitere Informationen zu Phishing und wie Outlook Phishing-Nachrichten verarbeitet finden Sie unter [Aktivieren oder Deaktivieren von Links in e-Mail-Nachrichten](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8).|
   
## <a name="authentication-results-message-header"></a>Nachrichtenkopfzeile „Authentication-results"
<a name="sectionSection2"> </a>

Die Ergebnisse der SPF-, DKIM- und DMARC-Überprüfungen werden aufgezeichnet, oder in der Nachrichtenkopfzeile **Authentication-results** von Office 365 markiert, wenn unsere E-Mail-Server eine E-Mail erhalten.
  
### <a name="check-stamp-syntax-and-examples"></a>Überprüfen der Stempelsyntax und Beispiele
<a name="referenceSPFstamp"> </a>

Die folgende Syntaxbeispiele zeigen einen Teil des Texts "Stempel", die Office 365 auf der für jede e-Mail-Nachrichtenkopf angewendet wird, die eine e-Mail-Authentifizierung Überprüfung unterzogen beim Empfang von unseren e-Mail-Servern wird. Der Zeitstempel wird die Kopfzeile **Ergebnis Authentifizierung** hinzugefügt.
  
 **Syntax: SPF-Prüfstempel**
  
Für SPF gilt die folgende Syntax.
  
```
spf=<pass (IP address)|fail (IP address)|softfail (reason)|neutral|none|temperror|permerror> smtp.mailfrom=<domain>
```

 **Beispiele: SPF-Prüfstempel**
  
```
spf=pass (sender IP is 192.168.0.1) smtp.mailfrom=contoso.com
spf=fail (sender IP is 127.0.0.1) smtp.mailfrom=contoso.com
```

 **Syntax: DKIM-Prüfstempel**
  
Für DKIM gilt die folgende Syntax.
  
```
dkim=<pass|fail (reason)|none> header.d=<domain>
```

 **Beispiele: DKIM-Prüfstempel**
  
```
dkim=pass (signature was verified) header.d=contoso.com
dkim=fail (body hash did not verify) header.d=contoso.com
```

 **Syntax: DMARC-Prüfstempel**
  
Für DMARC gilt die folgende Syntax.
  
```
dmarc=<pass|fail|bestguesspass|none> action=<permerror|temperror|oreject|pct.quarantine|pct.reject> header.from=<domain>
```

 **Beispiele: DMARC-Prüfstempel**
  
```
dmarc=pass action=none header.from=contoso.com
dmarc=bestguesspass action=none header.from=contoso.com
dmarc=fail action=none header.from=contoso.com
dmarc=fail action=oreject header.from=contoso.com
```

### <a name="authentication-results-message-header-fields-used-by-office-365-email-authentication"></a>Kopfzeilenfelder mit Authentifizierungsergebnissen, die von der Office 365-E-Mail-Authentifizierung verwendet werden
<a name="referenceSPFstamp"> </a>

In dieser Tabelle werden die Felder und die möglichen Werte für jede E-Mail-Authentifizierungsprüfung beschrieben.
  
|**Kopfzeilenfeld**|**Beschreibung**|
|:-----|:-----|
|SPF|Beschreibt die Ergebnisse der SPF-Prüfung für die Nachricht. Mögliche Werte sind:  <br/>• **übergeben (IP-Adresse)**: Zeigt die SPF-Prüfung für die Nachricht übergeben und umfasst die IP-Adresse des Absenders. Der Client ist autorisiert senden oder Weiterleiten von e-Mails im Namen der Domäne des Absenders.<br/>• **ein Fehler auftritt (IP-Adresse)**: Zeigt die SPF-Prüfung für die Nachricht konnte nicht an und umfasst die IP-Adresse des Absenders. Dies wird manchmal als _schwerer Fehler_bezeichnet.<br/>• **Softfail (Grund)**: Gibt an, dass der SPF-Datensatz wurde den Host als nicht berechtigt, senden eingerichtet, aber befindet sich im Übergang. <br/>• **neutral**: Gibt an, dass der SPF-Datensatz explizit angegeben wurde, dass davon, ob die IP-Adresse darf nicht auszugehen ist. <br/>• **none**: Gibt an, dass die Domäne hat keines SPF-Datensatzes oder der SPF-Eintrag wird nicht in ein Ergebnis ausgewertet. <br/>• **Temperror**: Gibt an, dass ein Fehler, die aufgetreten ist temporärer Natur, beispielsweise ein DNS-Fehler werden. Versucht möglicherweise später erneut ohne Administratoraktion erfolgreich ausgeführt werden.<br/>• **Permerror**: Gibt an, dass ein permanenter Fehler aufgetreten ist. Dies geschieht, wenn beispielsweise die Domäne falsch formatierte SPF-Eintrag hat.|
|SMTP.MailFrom|Enthält die Quelldomäne, von der die Nachricht gesendet wurde. Alle Fehler zu dieser E-Mail-Nachricht werden an den Postmaster oder an die Entität gesendet, der bzw. die für die Domäne verantwortlich ist. Diese Adresse wird im Nachrichtenumschlag manchmal als 5321.MailFrom Adresse oder als reverse-path-Adresse bezeichnet.|
|dkim|Beschreibt die Ergebnisse der DKIM-Prüfung für die Nachricht. Mögliche Werte sind:  <br/>• **übergeben**: Gibt an, das Kontrollkästchen DKIM für die Nachricht übergeben. <br/>• **ein Fehler auftritt (Grund)**: Gibt das Kontrollkästchen DKIM für die Nachricht konnte nicht an und warum. Wenn beispielsweise die Nachricht nicht signiert wurde, oder die Signatur wurde nicht überprüft.<br/>• **none**: Gibt an, dass die Nachricht nicht signiert wurde. Dies kann oder möglicherweise nicht, dass die Domäne verfügt über einen Datensatz DKIM oder DKIM-Eintrag wird nicht ausgewertet, um ein Ergebnis, nur, dass diese Nachricht nicht signiert wurde.|
|Header.d|Die in der DKIM-Signatur identifizierte Domäne, sofern vorhanden. Dies ist die Domäne, die für den öffentlichen Schlüssel abgefragt wird.|
|dmarc|Beschreibt die Ergebnisse der DMARC-Prüfung für die Nachricht. Mögliche Werte sind:  <br/>• **übergeben**: Gibt an, das Kontrollkästchen DMARC für die Nachricht übergeben. <br/>• **fehl**: Gibt das Kontrollkästchen DMARC für die Nachricht konnte nicht an. <br/>• **Bestguesspass**: Gibt an, dass keine DMARC TXT-Eintrag für die Domäne vorhanden ist, aber falls eines vorhanden war, hatte, das Kontrollkästchen DMARC für die Nachricht übergeben haben würde. Dies ist, da die Domäne in der Adresse 5321.MailFrom der Domäne in der Adresse 5322.From entspricht.<br/>• **none**: Gibt an, dass keine DKIM TXT-Eintrag für die sendende Domäne im DNS vorhanden ist.|
|action|Gibt die Aktion an, die vom Spamfilter basierend auf den Ergebnissen der DMARC-Prüfung ausgeführt wird. Beispiel:  <br/>• **Permerror**: ein permanenter Fehler aufgetreten DMARC zu Evaluierungszwecken wie Auftreten eines falsch formatiert DMARC TXT tragen in DNS. Versuchen, diese Nachricht erneut zu senden, ist nicht mit einem anderen Ergebnis enden wahrscheinlich. Stattdessen müssen Sie die Domäne Besitzer wenden, um dieses Problem zu beheben.<br/>• **Temperror**: ein zeitweiliger Fehler aufgetreten DMARC Bewertung. Möglicherweise um anzufordern, dass der Absender die Nachricht später, um die e-Mail-Nachricht ordnungsgemäß verarbeiten erneut senden können.<br/>• **Oreject** oder **o.reject**: steht für überschreiben ablehnen. In diesem Fall Office 365 wird verwendet, die diese Aktion beim Empfang einer Meldung, die die DMARC fehlschlägt Überprüfen von einer Domäne, deren DMARC TXT-Eintrag eine Richtlinie von p hat = ablehnen. Anstelle von löschen oder Ablehnen der Nachricht, kennzeichnet Office 365 die Nachricht als Spam. Weitere Informationen dazu, warum Office 365 auf diese Weise konfiguriert ist finden Sie unter [wie Office 365-Handles e-Mail-Eingang, die DMARC fällt aus](use-dmarc-to-validate-email.md#inbounddmarcfail).<br/>• **pct.quarantine**: Gibt an, dass ein Prozentsatz weniger als 100 % der Nachrichten, die keine DMARC übergeben trotzdem zugestellt werden. Dies bedeutet, dass die Nachricht konnte nicht DMARC und die Richtlinie in Quarantäne festgelegt wurde, aber Pct-Feld nicht auf 100 % festgelegt wurde und das System nach dem Zufallsprinzip bestimmt wird, nicht für die Aktion DMARC gemäß den Anweisungen in der angegebenen Domäne Richtlinie angewendet werden.<br/>• **pct.reject**: Gibt an, dass ein Prozentsatz weniger als 100 % der Nachrichten, die keine DMARC übergeben trotzdem zugestellt werden. Dies bedeutet, dass die Nachricht konnte nicht DMARC und die Richtlinie wurde auf ablehnen, aber Pct-Feld nicht auf 100 % festgelegt wurde und das System nach dem Zufallsprinzip bestimmt wird, nicht für die Aktion DMARC gemäß den Anweisungen in der angegebenen Domäne Richtlinie angewendet werden.|
|Header.From|Die Domäne der Absenderadresse in der Kopfzeile der e-Mail-Nachricht. Dies ist die Adresse _5322.From_ bezeichnet.|
|compauth|Ergebnis der zusammengesetzten Authentifizierung. Von Office 365 verwendet zum Kombinieren mehrerer Authentifizierungstypen der wie SPF, DKIM, DMARC oder andere Teile der Nachricht um zu bestimmen, ob die Nachricht authentifiziert ist oder nicht. Verwendet von: Domäne als Grundlage für die Bewertung.|
|Grund|Der Grund dafür die zusammengesetzte Authentifizierung erfolgreich oder fehlgeschlagen ist. Der Wert für den Grund besteht aus drei Ziffern:<br/>• **000**: die Nachricht konnte explizit Authentifizierung nicht. Beispielsweise erhalten die Meldung DMARC Fail mit einer Aktion Quarantäne oder ablehnen.<br/>• **001**: die Nachricht konnte implizit nicht Authentifizierung und die sendende Domäne veröffentlicht Authentifizierungsrichtlinien nicht. Beispielsweise eine DMARC Richtlinie von p = none.<br/>• **1xx**: die Nachricht Authentifizierung übergeben. Die nächsten zwei Ziffern handelt es sich um interne Codes, die von Office 365 verwendet.<br/>• **2xx**: die Nachricht vorläufig übergeben Authentifizierung. Die nächsten zwei Ziffern handelt es sich um interne Codes, die von Office 365 verwendet.<br/>• **3xx**: die Nachricht wurde nicht auf zusammengesetzte Authentifizierung überprüft. <br/>• **4xx**: die Nachricht zusammengesetzte Authentifizierung umgangen. Die nächsten zwei Ziffern handelt es sich um interne Codes, die von Office 365 verwendet.|
