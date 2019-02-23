---
title: Antispam-Nachrichtenkopfzeilen
ms.author: krowley
author: kccross
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 2e3fcfc5-5604-4b88-ac0a-c5c45c03f1db
ms.collection:
- M365-security-compliance
description: Wenn Exchange Online Protection eingehende E-Mail-Nachrichten prüft, wird jeder Nachricht die Kopfzeile **X-Forefront-Antispam-Report** hinzugefügt.
ms.openlocfilehash: 4851c05f4db8d120eb54b9c22025fe2972e1e515
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30223584"
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
|PCL|Der PCL-Wert (Phishing Confidence Level) der Nachricht. |
|SRV:BULK|Die Nachricht wurde als Massen-E-Mail identifiziert. Ist die erweiterte Spamfilteroption **Alle Massen-E-Mail-Nachrichten sperren** aktiviert, wird sie als Spam markiert. Ist die nicht aktiviert, wird sie nur dann als Spam markiert, wenn der Rest der Filterungsregeln festlegt, dass es sich bei der Nachricht um Spam handelt.  |
|SFV:SFE|Filterung wurde übersprungen, und die Nachricht wurde durchgelassen, da sie von einem Absender aus der Liste mit sicheren Absendern stammt.|
|SFV:BLK|Filterung wurde übersprungen, und die Nachricht wurde blockiert, da sie von einem Absender aus der Liste mit blockierten Absendern stammt.  <br/> **Tipp**: Weitere Informationen dazu, wie Endbenutzer sichere und blockierte Absenderlisten erstellen können, finden Sie unter [blockieren oder zulassen (Junk-e-Mail-Einstellungen)](https://go.microsoft.com/fwlink/p/?LinkId=294862) (Outlook im Web) und [Übersicht über den Junk-e-Mail-Filter](https://go.microsoft.com/fwlink/p/?LinkId=270065) (Outlook).|
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
|SFTY|Die Nachricht wurde als Phishing identifiziert und wird mit einem der folgenden Werte gekennzeichnet: <br/>• 9,1: Standardwert. Die Nachricht enthält eine Phishing-URL, kann andere Phishing-Inhalte enthalten oder wurde möglicherweise durch einen anderen e-Mail-Filter wie eine lokale Version von Exchange Server als Phishing gekennzeichnet, bevor die Nachricht an Office 365 weitergeleitet wird. <br/>• 9,11: Fehler bei der Antispoofing-Überprüfung, wenn die sendende Domäne in der from:-Kopfzeile identisch mit oder an der gleichen Organisation wie die empfangende Domäne ausgerichtet ist oder mit dieser übereinstimmt. Dies deutet darauf hin, dass der Nachricht ein organisationsinterner Spoofing-Sicherheitstipp hinzugefügt wird. <br/>• 9,19: Nachrichten Fehler bei der Domänen Identitätswechsel Überprüfung, wenn die sendende Domäne versucht, eine Identität für eine Domäne des Empfängers oder eine durch die Anti-Phishing-Richtlinie geschützte benutzerdefinierte Domäne zu imitieren. Dies weist darauf hin, dass der Nachricht ein Identitätswechsel-Sicherheitstipp hinzugefügt wird, wenn diese über die Anti-Phishig-Richtlinie aktiviert ist. <br/>• 9,20: Nachrichten Fehler beim Benutzeridentitätswechsel überprüft, ob der sendende Benutzer versucht, die Identität eines Benutzers in der Empfängerorganisation oder ein benutzerdefinierter Benutzer zu imitieren, der durch die Anti-Phishing-Richtlinie geschützt ist. Dies weist darauf hin, dass der Nachricht ein Identitätswechsel-Sicherheitstipp hinzugefügt wird, wenn diese über die Anti-Phishig-Richtlinie aktiviert ist. <br/>• 9,21: fehlgeschlagene Antispoofing-Prüfungen der Nachricht und die sendende Domäne im from:-Header authentifiziert sich nicht und stammt von einer externen Domäne. Wird in Kombination mit CompAuth verwendet (siehe Authentication-results). <br/>• 9,22: identisch mit 9,21, außer dass der Benutzer über einen sicheren Absender verfügt, der überschrieben wurde. <br/>• 9,23: identisch mit 9,22, außer dass die Organisation über einen zulässigen Absender oder eine Domäne verfügt, die überschrieben wurde. <br/>• 9,24: identisch mit 9,23, außer dass der Benutzer über eine Exchange-Nachrichtenfluss Regel verfügt, die außer Kraft gesetzt wurde.|
|X-CustomSpam: [ASFOption]|Die Nachricht entsprach einer erweiterten Spamfilter Option. Beispielsweise zeigt **X-CustomSpam: Bild Links zu Remotestandorten** , dass die ASF-Option **Bild Links zu Remotestandorten** verglichen wurde. Informationen dazu, welcher X-Header-Text für jede einzelne ASF-Option hinzugefügt wird, finden Sie unter [Advanced Spam Filtering Options](advanced-spam-filtering-asf-options.md).|
   
## <a name="x-microsoft-antispam-message-header-fields"></a>Felder der Nachrichtenkopfzeile X-Microsoft-Antispam
<a name="sectionSection1"> </a>

In der folgenden Tabelle werden die hilfreiche Felder der Nachrichtenkopfzeile **X-Microsoft-Antispam** beschrieben: Andere Felder in dieser Kopfzeile werden ausschließlich vom Microsoft-Antispamteam zu Diagnosezwecken verwendet.
  
|**Kopfzeilenfeld**|**Beschreibung**|
|:-----|:-----|
|BCL|Die BCL-Wert (Bulk Complaint Level) der Nachricht. Weitere Informationen finden Sie unter [BCL-Werte (Bulk Complaint Level)](bulk-complaint-level-values.md).  |
|PCL|Die Phishing Confidence Level (PCL) der Nachricht, die angibt, ob es sich um eine Phishing-Nachricht handelt. Dieser Status kann als einer der folgenden numerischen Werte zurückgegeben werden:<br/>• **0-3**: der Inhalt der Nachricht ist wahrscheinlich kein Phishing. <br/>• **4-8**: der Inhalt der Nachricht ist wahrscheinlich Phishing. <br/>• **-9990**: (nur Exchange Online Protection) der Inhalt der Nachricht ist wahrscheinlich Phishing.  <br/>  Anhand der Werte wird bestimmt, welche Aktion Ihr e-Mail-Client auf Nachrichten annimmt. Outlook verwendet beispielsweise den PCL-Stempel, um den Inhalt verdächtiger Nachrichten zu blockieren. Weitere Informationen zu Phishing und zur Verarbeitung von Phishing-Nachrichten in Outlook finden Sie unter [Aktivieren oder Deaktivieren von Links in e-Mail-Nachrichten](https://support.office.com/article/2D79B907-93B6-4774-82E6-1F0385CF20F8).|
   
## <a name="authentication-results-message-header"></a>Nachrichtenkopfzeile „Authentication-results"
<a name="sectionSection2"> </a>

Die Ergebnisse der SPF-, DKIM- und DMARC-Überprüfungen werden aufgezeichnet, oder in der Nachrichtenkopfzeile **Authentication-results** von Office 365 markiert, wenn unsere E-Mail-Server eine E-Mail erhalten.
  
### <a name="check-stamp-syntax-and-examples"></a>Überprüfen der Stempelsyntax und Beispiele
<a name="referenceSPFstamp"> </a>

Die folgenden Syntax Beispiele zeigen einen Teil des Texts "Stamp" an, für den Office 365 für jede e-Mail gilt, die einer e-Mail-Authentifizierungsüberprüfung unterzogen wird, wenn Sie von unseren e-Mail-Servern empfangen wird. Der Stempel wird dem **Authentication-results-** Header hinzugefügt.
  
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
|SPF|Beschreibt die Ergebnisse der SPF-Prüfung für die Nachricht. Mögliche Werte sind:  <br/>• **Pass (IP-Adresse)**: gibt die SPF-Überprüfung für die übergebene Nachricht an und enthält die IP-Adresse des Absenders. Der Client ist berechtigt, e-Mails im Namen der Domäne des Absenders zu senden oder weiterzuleiten.<br/>• **Fail (IP-Adresse)**: gibt an, dass die SPF-Überprüfung für die Nachricht fehlgeschlagen ist und die IP-Adresse des Absenders enthält. Dies wird manchmal als _harter Fehler_bezeichnet.<br/>• **SoftFail (reason)**: gibt an, dass der SPF-Eintrag festgelegt hat, dass der Host nicht gesendet werden darf, sondern sich im Übergang befindet. <br/>• **neutral**: gibt an, dass der SPF-Eintrag explizit angegeben hat, dass nicht bestätigt wird, ob die IP-Adresse autorisiert ist. <br/>• **None**: gibt an, dass die Domäne nicht über einen SPF-Eintrag verfügt oder dass der SPF-Eintrag nicht zu einem Ergebnis ausgewertet wird. <br/>• **TempError**: gibt an, dass ein Fehler aufgetreten ist, der möglicherweise vorübergehend ist, beispielsweise ein DNS-Fehler. Der spätere Versuch kann ohne Administratoraktion erfolgreich ausgeführt werden.<br/>• **PermError**: gibt an, dass ein dauerhafter Fehler aufgetreten ist. Dies ist beispielsweise der Fall, wenn die Domäne einen schlecht formatierten SPF-Eintrag aufweist.|
|SMTP. MailFrom|Enthält die Quelldomäne, von der die Nachricht gesendet wurde. Alle Fehler zu dieser E-Mail-Nachricht werden an den Postmaster oder an die Entität gesendet, der bzw. die für die Domäne verantwortlich ist. Diese Adresse wird im Nachrichtenumschlag manchmal als 5321.MailFrom Adresse oder als reverse-path-Adresse bezeichnet.|
|dkim|Beschreibt die Ergebnisse der DKIM-Prüfung für die Nachricht. Mögliche Werte sind:  <br/>• **Pass**: gibt die DKIM-Überprüfung für die übergebene Nachricht an. <br/>• **Fail (reason)**: gibt an, dass die DKIM-Prüfung für die Nachricht fehlgeschlagen ist und warum. Wenn die Nachricht beispielsweise nicht signiert wurde oder die Signatur nicht überprüft wurde.<br/>• **None**: gibt an, dass die Nachricht nicht signiert wurde. Dies kann oder kann nicht darauf hinweisen, dass die Domäne einen DKIM-Eintrag aufweist oder dass der DKIM-Eintrag nicht zu einem Ergebnis ausgewertet wird, sondern nur, dass diese Nachricht nicht signiert wurde.|
|Header. d|Die in der DKIM-Signatur identifizierte Domäne, sofern vorhanden. Dies ist die Domäne, die für den öffentlichen Schlüssel abgefragt wird.|
|dmarc|Beschreibt die Ergebnisse der DMARC-Prüfung für die Nachricht. Mögliche Werte sind:  <br/>• **Pass**: gibt die DMARC-Überprüfung für die übergebene Nachricht an. <br/>• **Fail**: gibt an, dass die DMARC-Überprüfung für die Nachricht fehlgeschlagen ist. <br/>• **bestguesspass**: gibt an, dass kein DMARC TXT-Eintrag für die Domäne vorhanden ist, aber wenn eine vorhanden war, würde die DMARC-Überprüfung für die Nachricht übergeben haben. Der Grund dafür ist, dass die Domäne in der 5321. mailFrom-Adresse mit der Domäne in der 5322. from-Adresse übereinstimmt.<br/>• **None**: gibt an, dass kein DKIM-TXT-Eintrag für die sendende Domäne in DNS vorhanden ist.|
|action|Gibt die Aktion an, die vom Spamfilter basierend auf den Ergebnissen der DMARC-Prüfung ausgeführt wird. Beispiel:  <br/>• **PermError**: während der DMARC-Bewertung ist ein dauerhafter Fehler aufgetreten, beispielsweise ein falsch FORMATIERTER DMARC TXT-Eintrag in DNS. Der Versuch, diese Nachricht erneut zu senden, wird wahrscheinlich nicht mit einem anderen Ergebnis enden. Stattdessen müssen Sie sich möglicherweise an den Besitzer der Domäne wenden, um das Problem zu beheben.<br/>• **TempError**: während der DMARC-Auswertung ist ein temporärer Fehler aufgetreten. Möglicherweise können Sie anfordern, dass der Absender die Nachricht später erneut sendet, um die e-Mail ordnungsgemäß zu verarbeiten.<br/>• **oreject** oder **o. Reject**: steht für override Reject. In diesem Fall verwendet Office 365 diese Aktion, wenn Sie eine Nachricht erhält, bei der die DMARC-Prüfung aus einer Domäne, deren DMARC TXT-Eintrag eine Richtlinie von p = Reject aufweist, fehlschlägt. Anstatt die Nachricht zu löschen oder abzulehnen, markiert Office 365 die Nachricht als Spam. Weitere Informationen dazu, warum Office 365 auf diese Weise konfiguriert ist, finden Sie unter [How office 365 verarbeitet eingehende e-Mails, die DMARC fehlschlägt](use-dmarc-to-validate-email.md#inbounddmarcfail).<br/>• **PCT. Quarantine**: gibt an, dass ein Prozentsatz von weniger als 100% der Nachrichten, die DMARC nicht bestehen, trotzdem zugestellt wird. Dies hat zur Folge, dass die Nachricht nicht erfolgreich DMARC und die Richtlinie auf "Quarantine" festgelegt wurde, aber das PCT-Feld wurde nicht auf 100% festgelegt, und das System hat nach dem Zufallsprinzip ermittelt, dass die DMARC-Aktion gemäß der Richtlinie der angegebenen Domäne nicht angewendet werden soll.<br/>• **PCT. Reject**: gibt an, dass ein Prozentsatz von weniger als 100% der Nachrichten, die DMARC nicht bestehen, trotzdem zugestellt wird. Dies hat zur Folge, dass die Nachricht nicht erfolgreich DMARC und die Richtlinie auf ablehnen festgelegt wurde, aber das PCT-Feld wurde nicht auf 100% festgelegt, und das System hat nach dem Zufallsprinzip ermittelt, dass die DMARC-Aktion gemäß der Richtlinie der angegebenen Domäne nicht angewendet werden soll.|
|Kopfzeile. from|Die Domäne der Absenderadresse im e-Mail-Nachrichtenkopf. Dies wird manchmal auch als _5322. from_ -Adresse bezeichnet.|
|compauth|Ergebnis der Verbundauthentifizierung. Wird von Office 365 verwendet, um mehrere Authentifizierungstypen wie SPF, DKIM, DMARC oder einen beliebigen anderen Teil der Nachricht zu kombinieren, um zu bestimmen, ob die Nachricht authentifiziert wird. Verwendet die from:-Domäne als Basis für die Auswertung.|
|Grund|Der Grund, warum die Verbundauthentifizierung erfolgreich war oder fehlgeschlagen ist. Der Wert für den Grund besteht aus drei Ziffern:<br/>• **000**: die Authentifizierung der Nachricht wurde explizit fehlgeschlagen. Die Nachricht hat beispielsweise ein DMARC-Fehler mit einer Aktion der Quarantäne oder Ablehnung erhalten.<br/>• **001**: die Authentifizierung mit implizit fehlgeschlagen, und die sendende Domäne hat keine Authentifizierungsrichtlinien veröffentlicht. Beispiel: eine DMARC-Richtlinie von p = None.<br/>• **1xx**: die Nachricht hat die Authentifizierung übergeben. Die zweiten beiden Ziffern sind interne Codes, die von Office 365 verwendet werden.<br/>• **2xx**: die Meldung "Soft-passed Authentication". Die zweiten beiden Ziffern sind interne Codes, die von Office 365 verwendet werden.<br/>• **3xx**: die Nachricht wurde nicht auf die Verbundauthentifizierung überprüft. <br/>• **4xx**: die Nachricht hat die Verbundauthentifizierung umgangen. Die zweiten beiden Ziffern sind interne Codes, die von Office 365 verwendet werden.|
