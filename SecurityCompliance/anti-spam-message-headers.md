---
title: Antispam-Nachrichtenkopfzeilen
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 2/9/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
description: Wenn Exchange Online Protection eingehende E-Mail-Nachrichten prüft, wird jeder Nachricht die Kopfzeile **X-Forefront-Antispam-Report** hinzugefügt.
ms.openlocfilehash: 7baa15f4d687c809d45461a135f64f0d18f49a7f
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026502"
---
# <a name="anti-spam-message-headers"></a>Antispam-Nachrichtenkopfzeilen

Wenn Exchange Online Protection eingehende E-Mail-Nachrichten prüft, wird jeder Nachricht die Kopfzeile **X-Forefront-Antispam-Report** hinzugefügt. Mit den Feldern in dieser Kopfzeile können Administratoren Information zur Nachricht und deren Verarbeitung bereitgestellt werden. Die Felder in der Kopfzeile **X-Microsoft-Antispam** liefern zusätzliche Informationen über Massensendungen und Phishing. Zusätzlich zu diesen beiden Kopfzeilen fügt Exchange Online Protection auch E-Mail-Authentifizierungsergebnisse für jede verarbeitete Nachricht in die Kopfzeile **Authentication-results** ein. 
  
> [!TIP]
> Informationen dazu, wie Sie einen E-Mail-Nachrichtenkopf in verschiedenen E-Mail-Clients anzeigen, finden Sie unter [Message Header Analyzer](https://go.microsoft.com/fwlink/p/?LinkId=306583). Sie können den Inhalt der Nachrichtenkopfzeile kopieren und in der [Nachrichtenkopfanalyse](https://testconnectivity.microsoft.com/?tabid=mha) einfügen. Wenn Sie im Exchange Admin Center eine Nachricht in Quarantäne auswählen, können Sie über den Link **Nachrichtenkopfzeile anzeigen** ganz einfach den Text der Nachrichtenkopfzeile kopieren und im Tool einfügen. Klicken Sie im Nachrichtenkopfanalyse-Tool auf **Kopfzeilen analysieren**, um Informationen zur Kopfzeile abzurufen. 
  
## <a name="x-forefront-antispam-report-message-header-fields"></a>Felder der Nachrichtenkopfzeile X-Forefront-Antispam-Report
<a name="sectionSection0"> </a>

Suchen Sie nach dem Zugriff auf die Nachrichtenkopfzeileninformationen nach **X-Forefront-Antispam-Report**, und suchen Sie nach den folgenden Feldern: Andere Felder in dieser Kopfzeile werden ausschließlich vom Microsoft-Antispamteam zu Diagnosezwecken verwendet. 
  
|||
|:-----|:-----|
|**Kopfzeilenfeld** <br/> |**Beschreibung** <br/> |
|CIP: [IP-Adresse]  <br/> |Die IP-Verbindungsadresse. Sie sollten diese IP-Adresse angeben, wenn Sie im Verbindungsfilter eine IP-Zulassungsliste oder eine Liste für geblockte IP-Adressen erstellen. Weitere Informationen finden Sie unter [Konfigurieren der Verbindungsfilterrichtlinie](configure-the-connection-filter-policy.md).  <br/> |
|CTRY  <br/> |Das Land, aus dem die Nachricht mit dem Dienst verbunden wurde. Es wird anhand der Verbindungs-IP-Adresse ermittelt, die nicht notwendigerweise mit der ursprünglichen Sende-IP-Adresse übereinstimmen muss.  <br/> |
|LANG  <br/> |Die Sprache, in der die Nachricht verfasst wurde, wie im Ländercode angegeben (z. B. ru_RU für Russisch).  <br/> |
|SCL  <br/> |Die SCL-Bewertung (Spam Confidence Level) einer Nachricht. Weitere Informationen zur Interpretation dieser Werte finden Sie unter [SCL-Bewertungen (Spam Confidence Level)](spam-confidence-levels.md).  <br/> |
|PCL  <br/> |Der PCL-Wert (Phishing Confidence Level) der Nachricht. Unter [PCL](anti-spam-message-headers.md#PCL) erhalten Sie weitere Informationen über PCL-Werte.  <br/> |
|SRV:BULK  <br/> |Die Nachricht wurde als Massen-E-Mail identifiziert. Ist die erweiterte Spamfilteroption **Alle Massen-E-Mail-Nachrichten sperren** aktiviert, wird sie als Spam markiert. Ist die nicht aktiviert, wird sie nur dann als Spam markiert, wenn der Rest der Filterungsregeln festlegt, dass es sich bei der Nachricht um Spam handelt.  <br/> |
|SFV:SFE  <br/> |Filterung wurde übersprungen, und die Nachricht wurde durchgelassen, da sie von einem Absender aus der Liste mit sicheren Absendern stammt.  <br/> |
|SFV:BLK  <br/> |Filterung wurde übersprungen, und die Nachricht wurde blockiert, da sie von einem Absender aus der Liste mit blockierten Absendern stammt.  <br/> **Tipp:** Weitere Informationen zum Erstellen von Listen mit sicheren oder blockierten Absendern finden Sie unter [Sperren oder Zulassen (Junk-E-Mail-Einstellungen)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (OWA) und [Übersicht über den Junk-E-Mail-Filter](https://go.microsoft.com/fwlink/p/?LinkId=270065) (Outlook).  <br/> |
|IPV:CAL  <br/> |Die Nachricht wurde durch die Spam-Filter gelassen, weil die IP-Adrese in einer IP-Zulassungsliste im Verbindungsfilter angegeben wurde.  <br/> |
|IPV:NLI  <br/> |Die IP-Adresse war nicht in einer IP-Zuverlässigkeitsliste aufgeführt.  <br/> |
|SFV:SPM  <br/> |Die Nachricht wurde vom Inhaltsfilter als Spam markiert.  <br/> |
|SFV:SKS  <br/> |Die Nachricht wurde bereits als Spam markiert, noch bevor sie vom Inhaltsfilter verarbeitet wurde. Dies beinhaltet Nachrichten, bei denen die Nachricht einer Transportregel entsprach, die diese automatisch als Spam markiert und alle zusätzlichen Filterungen umgeht.  <br/> |
|SFV:SKA  <br/> |Die Nachricht hat das Filtern übersprungen und wurde im Posteingang zugestellt, da sie einer Zulassenliste in der Richtlinie für den Spamfilter entsprach, wie z. B. die Liste **Absender zulassen**.    <br/> |
|SFV:SKB  <br/> |Die Nachricht wurde als Spam markiert, da sie einer Sperrliste in der Richtlinie für den Spamfilter entsprach, wie z. B. die Liste **Absender blockieren**.    <br/> |
|SFV:SKN  <br/> |Die Nachricht wurde bereits als Nicht-Spam markiert, noch bevor sie vom Inhaltsfilter verarbeitet wurde. Dies beinhaltet Nachrichten, bei denen die Nachricht einer Transportregel entsprach, die diese automatisch als Nicht-Spam markiert und alle zusätzlichen Filterungen umgeht.  <br/> |
|SFV:SKI  <br/> |Ähnlich wie SFV:SKN, die Filterung der Nachricht wurde aus einem anderen Grund übersprungen, wie eine unternehmensinterne E-Mail innerhalb einer Mandantenstruktur.  <br/> |
|SFV:SKQ  <br/> |Die Nachricht wurde aus der Quarantäne freigegeben und an die vorgesehenen Empfänger gesendet.  <br/> |
|SFV:NSPM  <br/> |Die Nachricht wurde als "Nicht-Spam" markiert und an die vorgesehenen Empfänger gesendet.  <br/> |
|H: [helostring]  <br/> |Die Zeichenfolge HELO oder EHLO des verbundenen E-Mail-Servers.  <br/> |
|PTR: [ReverseDNS]  <br/> |Der PTR-Eintrag (bzw. der Zeigereintrag) der Absender-IP-Adresse, auch als Reverse-DNS-Adresse bezeichnet.  <br/> |
|SFTY  <br/> | Die Nachricht wurde als Phishing identifiziert und auch mit einem der folgenden Werte markiert werden:  <br/>  9.1 - Standardwert. Die Nachricht enthält eine URL Phishing, möglicherweise andere Phishing Inhalte enthalten oder kann als gekennzeichnet wurden Phishing durch einen anderen e-Mail-Filter wie eine lokale Version von Exchange Server vor der Weiterleitung der Nachricht zu Office 365.  <br/>  9.11 - Nachricht nicht erfolgreich überprüft Anti-spoofing, in dem die sendende Domäne in der From: Kopfzeile ist identisch, ausgerichtet oder Teil derselben Organisation wie die empfangende Domäne ist.  <br/>  9.21 - Nachricht nicht erfolgreich, Anti-spoofing Prüfungen und die sendende Domäne in der From: Kopfzeile keine Authentifizierung. In Kombination mit CompAuth verwendet (Siehe das Ergebnis-Authentifizierung).  <br/>  9.22 - identisch mit 9.21, mit der Ausnahme, dass der Benutzer einen sicheren Absender verfügt, die überschrieben wurde.  <br/>  9.23 - identisch mit 9.22, außer dass die Organisation hat eine zulässige Absender oder die Domäne, die überschrieben wurde.  <br/>  9,24 - identisch 9.23, mit der Ausnahme, dass der Benutzer eine Regel, die Exchange-Nachrichtenübermittlung wurde außer Kraft gesetzt.  <br/> |
|X-CustomSpam: [ASFOption]  <br/> |Die Nachricht entsprach einer erweiterten spamfilterungsoptionen. Beispielsweise **X-CustomSpam: Links zu Remotestandorten Image** gibt an, dass die Option **Bildlinks zu Remotestandorten** ASF Übereinstimmung gefunden wurde. Um herauszufinden, welche X-Headertext für jede bestimmte ASF Option hinzugefügt wird, finden Sie unter [Erweiterte Spamfilterung Optionen](advanced-spam-filtering-asf-options.md).<br/> |
   
## <a name="x-microsoft-antispam-message-header-fields"></a>Felder der Nachrichtenkopfzeile X-Microsoft-Antispam
<a name="sectionSection1"> </a>

In der folgenden Tabelle werden die hilfreiche Felder der Nachrichtenkopfzeile **X-Microsoft-Antispam** beschrieben: Andere Felder in dieser Kopfzeile werden ausschließlich vom Microsoft-Antispamteam zu Diagnosezwecken verwendet. 
  
|||
|:-----|:-----|
|**Kopfzeilenfeld** <br/> |**Beschreibung** <br/> |
|BCL  <br/> |Die BCL-Wert (Bulk Complaint Level) der Nachricht. Weitere Informationen finden Sie unter [BCL-Werte (Bulk Complaint Level)](bulk-complaint-level-values.md).  <br/> |
|PCL  <br/> | Der PCL-Wert (Phishing Confidence Level) der Nachricht, der anzeigt, ob es sich um eine Phishing-Nachricht handelt.  <br/>  Dieser Status kann als einer der folgenden numerischen Werte zurückgegeben werden:  <br/> **0-3** Der Inhalt der Nachricht wird wahrscheinlich nicht zum Phishing genutzt.  <br/> **4-8** Der Inhalt der Nachricht wird wahrscheinlich zum Phishing genutzt.  <br/> **-9990** (nur Exchange Online Protection) Der Inhalt der Nachricht wird wahrscheinlich als Phishing eingestuft.  <br/>  Anhand dieser Werte wird ermittelt, welche Aktion Ihr E-Mail-Client für die Nachrichten ausführt. Outlook verwendet z. B. den PCL-Stempel, um den Inhalt verdächtiger Nachrichten zu blockieren. Weitere Informationen über Phishing und darüber, wie Outlook Phishing-Nachrichten verarbeitet, erhalten Sie unter [Aktivieren und Deaktivieren von Links in E-Mail-Nachrichten](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8).  <br/> |
   
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
|SPF  <br/> | Beschreibt die Ergebnisse der SPF-Prüfung für die Nachricht. Mögliche Werte sind:  <br/> **pass (IP-Adresse)** gibt an, dass die SPF-Überprüfung für die Nachricht bestanden wurde, und enthält die IP-Adresse des Absenders. Der Client kann E-Mails im Auftrag der Absenderdomäne senden oder weiterleiten.  <br/> **fail (IP-Adresse)** gibt an, dass die SPF-Überprüfung für die Nachricht fehlgeschlagen ist, und enthält die IP-Adresse des Absenders. Dies wird häufig als „Schwerer Fehler" bezeichnet.  <br/> **SoftFail (Ursache)** gibt an, dass der SPF-Eintrag bestimmt hat, dass der Host nicht die Erlaubnis zum Senden hat, sich jedoch im Übergang befindet.  <br/> **neutral** gibt an, dass der SPF-Eintrag explizit angegeben hat, dass nicht angegeben wird, ob die IP-Adresse autorisiert ist.  <br/> **none** gibt an, dass die Domäne nicht über einen SPF-Eintrag verfügt oder dass der SPF-Eintrag nicht zu einem Ergebnis ausgewertet wird.  <br/> **temperror** gibt an, dass ein Fehler aufgetreten ist, der möglicherweise vorübergehend ist, zum Beispiel ein DNS-Fehler. Wenn Sie es später erneut versuchen, kann der Vorgang möglicherweise ohne Eingreifen von Seiten eines Administrators erfolgreich ausgeführt werden.  <br/> **permerror** gibt an, dass ein dauerhafter Fehler aufgetreten ist. Dies geschieht, wenn die Domäne beispielsweise einen falsch formatierten SPF-Eintrag aufweist.  <br/> |
|SMTP.MailFrom  <br/> |Enthält die Quelldomäne, von der die Nachricht gesendet wurde. Alle Fehler zu dieser E-Mail-Nachricht werden an den Postmaster oder an die Entität gesendet, der bzw. die für die Domäne verantwortlich ist. Diese Adresse wird im Nachrichtenumschlag manchmal als 5321.MailFrom Adresse oder als reverse-path-Adresse bezeichnet.  <br/> |
|dkim  <br/> | Beschreibt die Ergebnisse der DKIM-Prüfung für die Nachricht. Mögliche Werte sind:  <br/> **pass** gibt an, dass die Nachricht die DKIM-Prüfung bestanden hat.  <br/> **fail (Ursache)** gibt an, dass die Nachricht die DKIM-Prüfung nicht bestanden hat und warum. Wenn die Nachricht beispielsweise nicht signiert war oder die Signatur nicht überprüft werden konnte.  <br/> **none** gibt an, dass die Nachricht nicht signiert war. Dies kann darauf hinweisen, dass die Domäne über einen DKIM-Eintrag verfügt oder dass der DKIM-Eintrag nicht zu einem Ergebnis ausgewertet wird. Dieser Wert gibt nur an, dass die Nachricht nicht signiert war.  <br/> |
|Header.d  <br/> |Die in der DKIM-Signatur identifizierte Domäne, sofern vorhanden. Dies ist die Domäne, die für den öffentlichen Schlüssel abgefragt wird.  <br/> |
|dmarc  <br/> | Beschreibt die Ergebnisse der DMARC-Prüfung für die Nachricht. Mögliche Werte sind:  <br/> **pass** gibt an, dass die Nachricht die DMARC-Prüfung bestanden hat.  <br/> **fail** gibt an, dass die Nachricht die DMARC-Prüfung nicht bestanden hat.  <br/> **bestguesspass** gibt an, dass kein DMARC-TXT-Eintrag für die Domäne vorhanden ist. Wenn jedoch ein Eintrag vorhanden gewesen wäre, hätte die Nachricht die DMARC-Prüfung bestanden. Dies kommt daher, dass die Domäne in der Adresse „5321.MailFrom" der Domäne in der Adresse „5322.From" entspricht.  <br/> **none** gibt an, dass kein DKIM-TXT-Eintrag für die sendende Domäne in DNS vorhanden ist.  <br/> |
|action  <br/> | Gibt die Aktion an, die vom Spamfilter basierend auf den Ergebnissen der DMARC-Prüfung ausgeführt wird. Beispiel:  <br/> **permerror** Bei der DMARC-Prüfung ist ein dauerhafter Fehler aufgetreten, wie z. B. ein falsch formatierter DMARC-TXT-Eintrag in DNS. Der Versuch, die Nachricht erneut zu senden, wird höchstwahrscheinlich kein anderes Ergebnis liefern. Stattdessen müssen Sie sich möglicherweise an den Domänenbesitzer wenden, um das Problem zu beheben.  <br/> **temperror** Bei der DMARC-Prüfung ist ein temporärer Fehler aufgetreten. Sie können den Absender der Nachricht möglicherweise bitten, die Nachricht später noch einmal erneut zu senden, damit sie dann ordnungsgemäß verarbeitet werden kann.  <br/> **oreject** oder **o.reject** Dies bedeutet „override reject". Office 365 wendet diese Aktion an, wenn es Nachrichten empfängt, die die DMARC-Prüfung nicht bestehen und die von Domänen stammen, für deren DMARC-TXT-Eintrag die Richtlinie „p=reject" festgelegt ist. Anstatt die Nachricht abzulehnen oder zu löschen, kennzeichnet Office 365 die Nachricht als Spam. Weitere Informationen darüber, warum Office 365 auf diese Weise konfiguriert ist, finden Sie unter [So behandelt Office 365 eingehende E-Mail-Nachrichten, die DMARC-Prüfungen nicht bestehen](use-dmarc-to-validate-email.md#inbounddmarcfail).  <br/> **pct.quarantine** gibt an, dass ein Prozentsatz von weniger als 100 % der Nachrichten, die die DMARC-Prüfung nicht bestehen, trotzdem übermittelt wird. Dies bedeutet, dass die Nachricht die DMARC-Prüfung nicht bestanden hat und die Richtlinie auf „Quarantäne" festgelegt wurde. Dass PCT-Feld wurde jedoch nicht auf 100 % festgelegt, und das System hat gemäß der Richtlinie der angegebenen Domäne zufällig bestimmt, dass die DMARC-Aktion nicht angewendet werden soll.  <br/> **pct.reject** gibt an, dass ein Prozentsatz von weniger als 100 % der Nachrichten, die die DMARC-Prüfung nicht bestehen, trotzdem übermittelt wird. Dies bedeutet, dass die Nachricht die DMARC-Prüfung nicht bestanden hat und die Richtlinie auf „Ablehnen" festgelegt wurde. Dass PCT-Feld wurde jedoch nicht auf 100% festgelegt, und das System hat gemäß der Richtlinie der angegebenen Domäne zufällig bestimmt, dass die DMARC-Aktion nicht angewendet werden soll.  <br/> |
|Header.From  <br/> |Die Domäne der „Von"-Adresse in der Kopfzeile der E-Mail-Nachricht. Dies wird manchmal auch als 5322.From-Adresse bezeichnet.  <br/> |
|compauth  <br/> |Ergebnis der zusammengesetzten Authentifizierung. Von Office 365 verwendet zum Kombinieren mehrerer Authentifizierungstypen der wie SPF, DKIM, DMARC oder andere Teile der Nachricht um zu bestimmen, ob die Nachricht authentifiziert ist oder nicht. Verwendet von: Domäne als Grundlage für die Bewertung.  <br/> |
|Grund  <br/> | Der Grund dafür die zusammengesetzte Authentifizierung erfolgreich oder fehlgeschlagen ist. Der Wert für den Grund besteht aus drei Ziffern:  <br/>  000 - Fehler die Nachricht explizit Authentifizierung. Beispielsweise erhalten die Meldung DMARC Fail mit einer Aktion Quarantäne oder ablehnen.  <br/>  001 - die Nachricht konnte implizit Authentifizierung und die sendende Domäne veröffentlicht Authentifizierungsrichtlinien nicht. Beispielsweise eine DMARC Richtlinie von p = none.  <br/>  1xx - Nachricht übergeben Authentifizierung. Die nächsten zwei Ziffern handelt es sich um interne Codes, die von Office 365 verwendet.  <br/>  2xx - die Authentifizierung von Nachrichten vorläufig übergeben. Die nächsten zwei Ziffern handelt es sich um interne Codes, die von Office 365 verwendet.  <br/>  3xx - die Nachricht wurde nicht auf zusammengesetzte Authentifizierung überprüft.  <br/>  4xx - Nachricht umgangen zusammengesetzte Authentifizierung. Die nächsten zwei Ziffern handelt es sich um interne Codes, die von Office 365 verwendet.  <br/> |
  