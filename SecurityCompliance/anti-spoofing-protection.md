---
title: Anti-spoofing Schutz in Office 365
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 7/2/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: d24bb387-c65d-486e-93e7-06a4f1a436c0
description: In diesem Artikel wird beschrieben, wie Office 365 gegen Phishing-Angriffe gemindert, dass Verwendungsmöglichkeiten Absenderdomänen, d. h., Domänen gefälscht, die manipuliert werden. Sie erreicht dies durch die Analyse der Nachrichten und Neithe mithilfe der standard-e-Mail-Authentifizierungsmethoden noch andere Sender Reputation Techniken authentifiziert Blockierung diejenigen aus, die werden können. Diese Änderung wird implementiert wird, um die Anzahl der Phishingangriffe zu reduzieren, die Organisationen in Office 365 verfügbar gemacht werden.
ms.openlocfilehash: bbcfbcdf32c87e070f10c9478a7c5978e909f009
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22559220"
---
# <a name="anti-spoofing-protection-in-office-365"></a>Anti-spoofing Schutz in Office 365

In diesem Artikel wird beschrieben, wie Office 365 gegen Phishing-Angriffe gemindert, dass Verwendungsmöglichkeiten Absenderdomänen, d. h., Domänen gefälscht, die manipuliert werden. Sie erreicht dies, indem Sie die Nachrichten analysieren und sperrende Korrelation diejenigen aus, die mithilfe der standard-e-Mail-Authentifizierungsmethoden noch andere Sender Reputation Techniken nicht authentifiziert werden können. Diese Änderung wird implementiert wird, um die Anzahl der Phishingangriffe zu reduzieren, die Kunden verfügbar gemacht werden.
  
In diesem Artikel wird erläutert, warum diese Änderung vorgenommen wird, wie Kunden, damit diese Änderung vorbereiten können, wie Nachrichten anzeigen, die betroffen sind, wie Nachrichten melden, wie falsch positive Ergebnisse zu mindern sowie wie Absender an Microsoft für dieses vorbereiten sollte ändern.
  
Microsoft Anti-spoofing-Technologie wird zunächst auf die Office 365 erweiterte Threat Protection (ATP) und E5 Kunden bereitgestellt. Allerdings können aufgrund der Art, die alle seine Filter voneinander lernen, nicht ATP-Kunden und sogar Outlook.com Benutzer auch beeinträchtigt werden.
  
## <a name="how-spoofing-is-used-in-phishing-attacks"></a>Wie spoofing in Phishingangriffe verwendet wird

Wenn es darum geht, ihren Benutzern schützen, hat Microsoft die Bedrohung Phishing ernsthaft. Eines der Verfahren, mit denen Spammer und Phishing häufig ist spoofing, d. h., wann der Absender gefälscht ist und eine Meldung wird angezeigt, die von einer Person oder zumindest als die aktuelle Quelle stammen. Dieses Verfahren wird häufig in Phishing-Kampagnen entwickelt, um das Abrufen von Benutzeranmeldeinformationen verwendet. Microsoft Anti-Spoofing Technologie untersucht speziell Forgery von der ' aus: Kopfzeile ' ist diejenige, die in ein e-Mail-Client wie Outlook wird angezeigt. Wenn Microsoft vertrauenswürdige hat, die von: Kopfzeile manipuliert wurde, wird die Nachricht als ein Spoofing identifiziert.
  
Spoofing Nachrichten haben zwei negative Auswirkungen für Benutzer der Praxis:
  
### <a name="1-spoofed-messages-deceive-users"></a>1. gefälschte Nachrichten Benutzer dazu verleiten.
  
Erstens kann eine gefälschte Nachricht bringen, einen Benutzer auf den Link und ihre Anmeldeinformationen aufgegeben, Malware herunterladen oder Antworten auf eine Nachricht mit vertrauliche Inhalte (von denen letzterer als Business E-Mail Kompromiss bezeichnet). Folgendes wird beispielsweise eine Phishingnachricht mit einer gefälschten Absender der msoutlook94@service.outlook.com:
  
![Identitätswechsel bei service.outlook.com Phishing-Nachricht](media/1a441f21-8ef7-41c7-90c0-847272dc5350.jpg)
  
Die oben genannten stammt nicht tatsächlich von service.outlook.com, aber stattdessen manipuliert wurde, durch die leitet, sieht dies der Fall war. Es wird versucht, einen Benutzer auf den Link in der Nachricht bringen.
  
Im nächste Beispiel wird "contoso.com" spoofing:
  
![Phishingnachricht - Gefährdung der Business-e-Mail](media/da15adaa-708b-4e73-8165-482fc9182090.jpg)
  
Die Nachricht sieht legitime, aber tatsächlich ist eine Spoofing. Diese Meldung Phishing ist ein Business E-Mail Kompromiss ist eine Unterkategorie Phishing.
    
### <a name="2-users-confuse-real-messages-for-fake-ones"></a>2. Benutzer verwirren echte Nachrichten für gefälschten Regeln
  
Zweitens gefälschte Nachrichten erstellen Unsicherheit für Benutzer, die Phishing-Nachrichten kennen, aber den Unterschied zwischen einer realen Nachricht und gefälschten können nicht feststellen. Beispielsweise ist der folgenden ein Beispiel für einen tatsächlichen Kennwort zurücksetzen aus der Microsoft Security-Konto e-Mail-Adresse:
  
![Microsoft legitime Kennwort zurücksetzen](media/58a3154f-e83d-4f86-bcfe-ae9e8c87bd37.jpg)
  
Die oben angegebene Meldung stammt von Microsoft, aber gleichzeitig, sind Benutzer, um erste Phishing-Nachrichten, die möglicherweise bringen, einen Benutzer auf den Link und ihre Anmeldeinformationen aufgegeben, Malware herunterladen oder Antworten auf eine Nachricht mit vertrauliche Inhalte. Da es schwierig ist, den Unterschied zwischen einer realen Kennwörter zurückzusetzen und eine Fälschung 1, erkennen viele Benutzer diese Nachrichten ignorieren, meldet sie als Spam oder unnötig Ergebnisse die Nachrichten an Microsoft als verpassten Phishingangriffen.
    
Um spoofing zu beenden, hat die e-Mail-Filterung Branche e-Mail-Authentifizierungsprotokolle wie [SPF](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx), [DKIM](https://technet.microsoft.com/en-us/library/mt695945%28v=exchg.150%29.aspx)und [DMARC](https://technet.microsoft.com/en-us/library/mt734386%28v=exchg.150%29.aspx)entwickelt. DMARC verhindert, dass spoofing Untersuchen des Absenders einer Nachricht - diejenige, die dem Benutzer in ihrem e-Mail-Client angezeigt wird (in den obigen Beispielen ist dies service.outlook.com, outlook.com und accountprotection.microsoft.com) - mit der Domäne, die SPF oder DKIM übergeben. Die Domäne, die der Benutzer erhält, d. h., wurde authentifiziert und daher nicht manipuliert. Eine ausführlichere Erläuterung, finden Sie im Abschnitt " *verstehen, warum e-Mail-Authentifizierung ist nicht immer ausreichen spoofing beenden"* später in diesem Dokument. 
  
Das Problem ist jedoch die e-Mail-Authentifizierung, die Datensätze optional, nicht erforderlich sind. Aus diesem Grund während wie Domänen mit strenge Authentifizierungsrichtlinien sind microsoft.com und skype.com geschützt spoofing, Domänen, die schwächere Authentifizierungsrichtlinien für die oder keine Richtlinie überhaupt veröffentlichen, sind die Ziele für Spoofing. Ab März 2018 veröffentlichen Sie nur 9 % der Domänen von Unternehmen in den Fortune 500 sichere e-Mail-Authentifizierungsrichtlinien. Die verbleibende 91 % möglicherweise durch eine leitet manipuliert werden, und es sei denn, erkennt der e-Mail-Filter mit einer anderen Richtlinie kann an Endbenutzer gesendet werden und täuschen sie:
  
![DMARC Richtlinien von Fortune 500-Unternehmen](media/84e77d34-2073-4a8e-9f39-f109b32d06df.jpg)
  
Der Anteil der kleinen bis mittleren Größe Unternehmen, die sind ist nicht in die Fortune 500, die sichere e-Mail-Authentifizierungsrichtlinien veröffentlichen, kleiner und kleinere weiterhin für Domänen, die außerhalb von Nordamerika und Europa Western sind.
  
Dies ist ein großes Problem, da während Unternehmen möglicherweise nicht bekannt Funktionsweise der e-Mail-Authentifizierung, Phishing verstehen und nutzen Sie die mangelnde.
  
Informationen zum Einrichten von SPF, DKIM und DMARC, finden Sie im Abschnitt " *Kunden von Office 365"* weiter unten in diesem Dokument. 
  
## <a name="stopping-spoofing-with-implicit-email-authentication"></a>Beenden spoofing mit impliziten e-Mail-Authentifizierung

Da Phishing und Spear Phishing ein Problem aufgetreten ist, und aufgrund der begrenzten Annahme von Richtlinien für sichere e-Mail-Authentifizierung, weiterhin Microsoft in Funktionen zum Schutz seiner Kunden investieren. Aus diesem Grund Microsoft wird hingegen mit *Authentifizierung implizite e-Mail* - verschoben, wenn eine Domäne nicht zu authentifizieren, wird Microsoft behandeln, als sei es e-Mail-Authentifizierung Datensätze veröffentlicht wurde und er entsprechend behandelt, wenn es nicht übergeben. 
  
Zu diesem Zweck hat Microsoft zahlreiche Erweiterungen für reguläre e-Mail-Authentifizierung einschließlich Absenderzuverlässigkeits, Absender/Empfänger-Verlauf, Verhalten Analyse und andere erweiterten Techniken erstellt. Eine Nachricht von einer Domäne, die e-Mail-Authentifizierung veröffentlichen nicht gesendet wird als Spoofing, wenn sie andere enthält signalisiert, um anzugeben, dass es legitime ist markiert.
  
Auf diese Weise, End, die Benutzer können vertrauen, dass eine e-Mail an sie gesendet wurde nicht manipuliert wurde, können Absender sicher sein, dass niemand ihrer Domäne imitiert und Kunden von Office 365 noch besseren Schutz beispielsweise Identitätswechsel Schutz bieten können.
  
Microsofts allgemeine Ankündigung finden Sie unter [eine gefährliche von Phishing Teil 2 - Enhanced Anti-spoofing in Office 365](https://techcommunity.microsoft.com/t5/Security-Privacy-and-Compliance/Schooling-A-Sea-of-Phish-Part-2-Enhanced-Anti-spoofing/ba-p/176209).
  
## <a name="identifying-that-a-message-is-classified-as-spoofed"></a>Identifizieren, dass eine Nachricht als manipuliert klassifiziert wird

### <a name="composite-authentication"></a>Zusammengesetzte Authentifizierung

SPF, DKIM und DMARC selbst hilfreich sind, kommunizieren nicht sie genügend Authentifizierungsstatus, im Ereignisprotokoll eine Nachricht keine explizite Authentifizierung Datensätze enthalten sind. Microsoft hat daher einen Algorithmus entwickelt, der mehrere Signale in einen single-Wert für Short zusammengesetzte Authentifizierung oder Compauth aufgerufen kombiniert. Kunden in Office 365 sind Compauth die Werte in der Kopfzeile *Authentifizierung Ergebnisse* in den Kopfzeilen versehen. 
  
```
Authentication-Results:
  compauth=<fail|pass|softpass|none> reason=<yyy>

```

|**CompAuth Ergebnis**|**Beschreibung**|
|:-----|:-----|
|ein Fehler auftritt|Nachricht konnte nicht explizite Authentifizierung (sendende Domäne veröffentlicht Datensätze explizit im DNS) oder implizite Authentifizierung (senden) Domäne nicht veröffentlichen Datensätze in DNS, damit Office 365 das Ergebnis interpoliert, als wäre es Einträge veröffentlicht wurde.|
|übergeben Sie|Meldung übergeben explizite Authentifizierung (Nachricht übergeben DMARC oder [Bewährte erraten übergeben DMARC](https://blogs.msdn.microsoft.com/tzink/2015/05/06/what-is-dmarc-bestguesspass-in-office-365)) oder implizite Authentifizierung mit vertrauenswürdige (Senden von e-Mail-Authentifizierung Datensätze werden von der Domäne nicht veröffentlicht, aber Office 365 hat starken Back-End-Signale zu Geben Sie an die Nachricht ist wahrscheinlich legitime).|
|softpass|Nachricht implizite Authentifizierung mit wenig bis mittleren Confidence übergeben (Domäne werden e-Mail-Authentifizierung nicht veröffentlicht, aber Office 365 hat die Back-End-Signale an, dass die Nachricht ist zulässig, aber die Stärke des Signals ist schwächere senden).|
|n/z|Nachricht nicht authentifiziert (oder hat sich authentifiziert, aber keine Ausrichtung), aber zusammengesetzte Authentifizierung aufgrund Absenderzuverlässigkeits oder anderen Faktoren nicht angewendet.|
   
|||
|:-----|:-----|
|**Reason**|**Beschreibung**|
|0XX|Nachricht zusammengesetzte Authentifizierung ist fehlgeschlagen.<br/>**000** bedeutet, dass die Nachricht mit einer Aktion ablehnen oder Quarantäne DMARC konnte nicht.                    -001 bedeutet, dass die Nachricht implizite-e-Mail-Authentifizierung ist fehlgeschlagen. Dies bedeutet, dass die sendende Domäne verfügte nicht über die Authentifizierung von e-Mail-Datensätzen veröffentlicht, oder wenn dies der Fall war, mussten eine Richtlinie für schwächere Fehler (SPF-soft-Fehler oder Neutral, DMARC Richtlinie von p = none).<br/>**002** bedeutet, dass die Organisation über eine Richtlinie für den Absender-Domäne Paar verfügt, das Senden von e-Mails mit Spoofing stammen explizit verboten wird, ist diese Einstellung manuell vom Administrator festgelegt.  <br/>**010** bedeutet, dass die Nachricht konnte nicht mit einer Aktion ablehnen oder Quarantäne DMARC und die sendende Domäne eine der akzeptierten Domänen mit Ihrer Organisation (Dies ist Teil der Self-Self- oder organisationsintern, spoofing).  <br/>**011** bedeutet, dass die Nachricht konnte nicht implizite e-Mail-Authentifizierung und die sendende Domäne eine der akzeptierten Domänen Ihrer Organisation (Dies ist Teil der Self-Self- oder organisationsintern, spoofing).|
|Alle anderen Codes (1xx, 2xx, 3xx, 4xx, 5xx)|Verschiedene interne Codes entspricht warum eine Meldung übergeben implizite Authentifizierung oder hatte keine Authentifizierung, aber keine Aktion angewendet wurde.|
   
Verfolgen Sie die Kopfzeilen der Nachricht, kann ein Administrator oder sogar eines Endbenutzers bestimmen wie Office 365 nach Abschluss eingeht, dass der Absender manipuliert werden kann.
  
### <a name="differentiating-between-different-types-of-spoofing"></a>Unterscheidung zwischen verschiedenen Arten von spoofing

Microsoft unterscheidet zwischen zwei verschiedene Arten von spoofing Nachrichten:
  
 **Unternehmensinterne spoofing**
  
Auch bekannt als Self-Self-spoofing, Dies tritt auf, wenn die Domäne in der From: Adresse identisch ist, oder ausgerichtet, die Domäne des Empfängers (wenn die Domäne des Empfängers eines Ihrer Organisation [Akzeptierte Domänen](https://technet.microsoft.com/en-us/library/jj945194%28v=exchg.150%29.aspx)ist); oder, wenn die Domäne in der From: Adresse ist Teil derselben Organisation.
  
Beispielsweise bietet die folgenden Absender und Empfänger aus der gleichen Domäne (contoso.com). Leerzeichen sind in der e-Mail-Adresse, um zu verhindern, Spambots Harvest auf dieser Seite eingefügt):
  
Aus: der Absender @ contoso.com
  
An: Empfänger @ contoso.com
  
Die folgenden besteht aus die Absender und Empfänger Domänen mit der organisatorischen Domäne (fabrikam.com) ausrichten:
  
Aus: der Absender @ foo.fabrikam.com
  
An: Empfänger @ bar.fabrikam.com
  
Die folgenden Absender und Empfänger Domänen unterschiedlich sind (microsoft.com und bing.com), jedoch zu derselben Organisation gehören (d. h., beide sind Teil der Organisation akzeptierte Domänen):
  
Aus: der Absender @ Microsoft.com (engl.)
  
An: Empfänger @ bing.com
  
Nachrichten, die nicht organisationsintern spoofing enthalten die folgenden Werte in den Kopfzeilen:
  
X-Forefront-Antispam-Report:... CAT:SPM/HSPM/PHSH;... SFTY:9.11
  
Die Katze ist die Kategorie der Nachricht, und es wird normalerweise als SPM (Spam) versehen, aber gelegentlich HSPM (vertrauenswürdige Spam) werden oder Phishing (Phishing) abhängig davon, welche anderen Arten von Mustern auftreten in der Nachricht.
  
Die SFTY ist die Sicherheitsstufe der Nachricht, die erste Ziffer (9) bedeutet die Meldung ist Phishing, und zweiter Satz von Ziffern nach der Punkt (11) bedeutet, dass beträgt organisationsintern spoofing.
  
Es gibt keinen bestimmten Grund-Code für zusammengesetzte Authentifizierung für unternehmensinterne spoofing, die weiter unten in 2018 (Zeitachse noch nicht definiert) versehen werden soll.
  
 **Cross-Domain-spoofing**
  
Dies tritt auf, wenn die sendende Domäne in der From: Adresse ist eine externe Domäne der empfangenden-Organisation. Nachrichten, die aufgrund von Cross-Domain-spoofing zusammengesetzte-Authentifizierung fehl enthalten die folgenden Werte in den Kopfzeilen:
  
Ergebnis-Authentifizierung:... Compauth = Fail Grund = 000/001
  
X-Forefront-Antispam-Report:... CAT:SPOOF;... SFTY:9.22
  
In beiden Fällen wird die folgenden Rot Safety Spitze versehen, in der Nachricht oder Entsprechung, die auf dem Empfängerpostfach Sprache angepasst ist:
  
![Rote Safety Tipp - Betrug Erkennung](media/a366156a-14e8-4c14-bfe5-2031b21936f8.jpg)
  
Es ist nur anhand von: beheben und zu wissen, was Ihre Empfänger e-Mail-Adresse ist oder Überprüfen von e-Mail-Headern, die Sie zwischen organisationsintern und Cross-Domain-spoofing unterscheiden können.
  
## <a name="how-customers-of-office-365-can-prepare-themselves-for-the-new-anti-spoofing-protection"></a>Wie können Kunden von Office 365 selbst für die neue Anti-spoofing Protection vorbereiten

### <a name="information-for-administrators"></a>Informationen für Administratoren

Als Administrator einer Organisation in Office 365 stehen mehrere wichtigsten Informationen, die Sie berücksichtigen müssen.
  
### <a name="understanding-why-email-authentication-is-not-always-enough-to-stop-spoofing"></a>Grundlegendes zu Warum e-Mail-Authentifizierung ist nicht immer ausreichen spoofing beenden

Die neue Anti-spoofing Protection nutzt die e-Mail-Authentifizierung (SPF, DKIM und DMARC) eine Nachricht als spoofing nicht markiert. Ein allgemeines Beispiel ist, wenn eine sendende Domäne nie SPF-Datensätze veröffentlicht hat. Wenn keine SPF-Datensätze vorhanden sind, oder sie nicht ordnungsgemäß eingerichtet sind, werden als manipuliert, es sei denn, Microsoft Back-End Intelligence verfügt, die besagt, dass die Nachricht legitime ist eine gesendete Nachricht markiert.
  
Beispielsweise vor dem Anti-spoofing bereitgestellt wird, kann eine Meldung wie folgt mit keine SPF-Datensatzes, kein Datensatz DKIM und kein Datensatz DMARC sahen: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```
Nach Anti-spoofing, wenn Sie eine erweiterte Threat Protection oder E5 "Kunde", sind der Compauth Wert wird versehen (nicht ATP und nicht E5 Benutzer sind nicht betroffen):
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=none
  action=none header.from=example.com; compauth=fail reason=001
From: sender @ example.com
To: receiver @ contoso.com

```

Wenn dies von example.com durch Einrichten eines SPF-Datensatzes, aber keinen Datensatz DKIM behoben werden, würde dies zusammengesetzte Authentifizierung übergeben, da die Domäne, die SPF übergeben an die Domäne in der From ausgerichtet: Adresse: 
  
```
Authentication-Results: spf=pass (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=none
  (message not signed) header.d=none; contoso.com; dmarc=bestguesspass
  action=none header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Oder, wenn sie einen Datensatz DKIM, aber keines SPF-Datensatzes eingerichtet, dies auch übergeben zusammengesetzte Authentifizierung, da die Domäne in der DKIM-Signatur, die übergeben an die Domäne in der From ausgerichtet: Adresse: 
  
```
Authentication-Results: spf=none (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; contoso.com; dkim=pass
  (signature was verified) header.d=outbound.example.com;
  contoso.com; dmarc=bestguesspass action=none
  header.from=example.com; compauth=pass reason=109
From: sender @ example.com
To: receiver @ contoso.com
```

Eine leitet möglicherweise auch SPF und DKIM einrichten und melden die Nachricht mit der eigenen Domäne jedoch, geben Sie im Feld von einer anderen Domäne: Adresse. SPF weder DKIM erfordert die Domäne der Domäne in der From ausgerichtet: beheben, damit es sei denn, example.com DMARC Datensätze veröffentlicht, dies nicht als ein Spoofing von DMARC markiert werden würde: 
  
```
Authentication-Results: spf=pass (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=example.com;
From: sender @ example.com
To: receiver @ contoso.com
```

In der e-Mail-Client (Outlook, Outlook im Web oder einen anderen e-Mail-Client), nur von: Domäne angezeigt wird, nicht die Domäne in der SPF oder DKIM und, kann dazu zu verleiten Benutzer zu denken die Nachricht stammt example.com, aber tatsächlich maliciousDomain.com stammt .
  
![Authentifizierte Nachricht jedoch aus: keine Ausrichtung Domäne mit was SPF oder DKIM übergeben](media/a9b5ab2a-dfd3-47c6-8ee8-e3dab2fae528.jpg)
  
Aus diesem Grund Office 365 erfordert, dass die Domäne in der From: Adresse richtet mit der Domäne in der SPF oder DKIM-Signatur, und wenn es nicht der Fall, enthält einige interne Signale, die angibt, wird die Nachricht legitime. Andernfalls würde die Nachricht Compauth Fail sein. 
  
```
Authentication-Results: spf=none (sender IP is 5.6.7.8)
  smtp.mailfrom=maliciousDomain.com; contoso.com; dkim=pass
  (signature was verified) header.d=maliciousDomain.com;
  contoso.com; dmarc=none action=none header.from=contoso.com;
  compauth=fail reason=001
From: sender@contoso.com
To: someone@example.com
```

Office 365 Anti-spoofing folglich Schutz gegen Domänen ohne Authentifizierung und gegen Domänen, die Authentifizierung, aber für die Domäne in der From-Konflikt eingerichtet: Adresse wie, die das, dass der Benutzer sieht und geht davon aus, wird der Absender der Nachricht. Dies gilt sowohl von Domänen außerhalb Ihrer Organisation sowie Domänen innerhalb Ihrer Organisation.
  
Wenn Sie schon einmal eine Meldung, die Fehler bei zusammengesetzten Authentifizierung und wird angezeigt als manipuliert, gekennzeichnet werden, obwohl die Nachricht SPF und DKIM übergeben, es ist daher, da die Domäne, die SPF und DKIM übergeben werden nicht mit der Domäne in der From ausgerichtet: Adresse.
  
### <a name="understanding-changes-in-how-spoofed-emails-are-treated"></a>Grundlegendes zu Änderungen in wie gefälschten-e-Mails behandelt werden

Derzeit für alle Organisationen in Office 365 - ATP und nicht-ATP - Nachrichten, Fail DMARC mit einer Richtlinie ablehnen oder Quarantäne werden als spam, und führen Sie in der Regel die Spamaktion bei hoher oder in einigen Fällen die regulären Spam-Aktion markiert (je nachdem, ob andere Spam Regeln identifizieren Sie zuerst es als Spam). Unternehmensinterne Spoofing erkannte Aktion regulären Spam. Dieses Verhalten muss nicht aktiviert werden soll, noch kann es deaktiviert.
  
Jedoch für Cross-Domain-spoofing Nachrichten vor der Änderung sie würde regulären Spam, Phishing und Malware Überprüfungen durchlaufen und wenn andere Teile des Filters als verdächtigen, identifiziert würde kennzeichnen Sie sie als Spam, Phishing oder Schadsoftware jeweils. Mit dem neuen spoofing Cross-Domain-Schutz, jede Nachricht, die nicht authentifiziert werden kann, wird standardmäßig dauert die Aktion, die in der Anti-Phishing definierten \> Anti-spoofing Richtlinie. Sofern nicht definiert ist, wird es zu einem Benutzer Junk-e-Mail-Ordner verschoben werden. In einigen Fällen müssen mehr verdächtige Nachrichten auch die rote Safety Spitze zur Nachricht hinzugefügt.
  
Dies kann einige Nachrichten führen, die zuvor als spam als spam jedoch eine rote Safety Info nun auch weisen weiterhin markiert erste gekennzeichnet wurden. in anderen Fällen hinzugefügt Nachrichten, die zuvor als nicht-Spam markiert gestartet wird, als Spam (CAT:SPOOF) als Tipp Rot Sicherheit markiert wurden. In wieder anderen Fällen Kunden, die alle Spam und Phishing in Quarantäne verschoben wurden nun sieht diese steigenden in den Junk-e-Mail-Ordner (dieses Verhalten kann geändert werden, finden Sie unter [Ändern Ihrer Einstellungen Anti-spoofing](#changing-your-anti-spoofing-settings)).
  
Es gibt mehrere verschiedene Arten, die eine Nachricht manipuliert werden kann (finden Sie weiter oben in diesem Artikel unter [differenzierte zwischen verschiedenen Typen von spoofing](#differentiating-between-different-types-of-spoofing) ) ab März 2018 wie Office 365 diese Nachrichten behandelt wurde nicht noch vereinheitlicht. In der folgenden Tabelle ist eine schnelle Zusammenfassung, mit Cross-Domain-spoofing-Schutz werden neue Verhalten: 
  
|**Typ des Spoofing**|**Kategorie**|**Sicherheit Tipp hinzugefügt?**|**Gilt für**|
|:-----|:-----|:-----|:-----|
|DMARC Fail (Quarantäne oder ablehnen)  <br/> |HSPM (Standard), möglicherweise auch SPM oder PHSH  <br/> |Nein (noch nicht)  <br/> |Alle Office 365-Kunden, Outlook.com  <br/> |
|Self-Self-  <br/> |SPM  <br/> |Ja  <br/> |Alle Office 365-Organisationen, Outlook.com  <br/> |
|Cross-domain  <br/> |SPOOFING  <br/> |Ja  <br/> |Office 365 erweiterte Threat Protection und E5-Kunden  <br/> |
   
### <a name="changing-your-anti-spoofing-settings"></a>Ändern Ihre Einstellungen Anti-spoofing

Zum Erstellen oder Aktualisieren der Anti-spoofing für Ihr (Cross-Domain), navigieren Sie zu der Anti-Phishing \> Anti-spoofing Einstellungen unter der Threat Management \> Registerkarte Richtlinie in das Wertpapier &amp; Compliance Center. Wenn Sie noch nie eine beliebige Einstellung Anti-Phishing erstellt haben, müssen Sie einen erstellen:
  
![Anti-Phishing-- eine neue Richtlinie erstellen](media/9337ec91-270e-4fa7-9dfa-a51a2d1eb95e.jpg)
  
Wenn Sie bereits eine erstellt haben, können Sie es zum Bearbeiten auswählen:
  
![Anti-Phishing-- vorhandene Richtlinie zu ändern](media/75457a7c-882e-4984-80d1-21a12b42c53a.jpg)
  
Wählen Sie die Richtlinie, die Sie gerade erstellt haben und die Schritte durchlaufen, gemäß der Beschreibung auf [erfahren Sie mehr über Spoofing Intelligence.](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf)
  
![Aktivieren oder Deaktivieren von antispoofing](media/c49e2147-c954-443c-9144-1cbd139e1166.jpg)
  
![Aktivieren oder Deaktivieren der Antispoofing Sicherheitstipps](media/eec7c407-31fc-4f73-8325-307d82d1fb53.jpg)
  
So erstellen Sie eine neue Richtlinie über PowerShell: 
  
```
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: The name should not exclude 64 characters, including spaces.
# If it does, you will need to pick a smaller name.
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy $name -RecipientDomainIs $domains
```

Sie können dann die Anti-Phishing Richtlinienparameter von PowerShell, befolgen die Dokumentation unter [Set-AntiphishPolicy](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/Set-AntiPhishPolicy?view=exchange-ps)ändern. Sie können die $name als Parameter angeben:
  
```
Set-AntiphishPolicy -Identity $name <fill in rest of parameters>
```

Weiter unten in 2018, sondern Sie erstellen eine Standardrichtlinie, eine erstellt werden, der an alle Empfänger in Ihrer Organisation ausgelegt ist, sodass Sie nicht manuell angeben (die folgenden Screenshots sind können vor die final-Implementierung).
  
![Standardrichtlinie für Anti-Phishing-](media/1f27a0bf-e202-4e12-bbac-24baf013c8f9.jpg)
  
Im Gegensatz zu einer Richtlinie, die Sie erstellen, kann nicht die Standardrichtlinie zu löschen, ändern die Priorität oder auswählen, welche Benutzer, Domänen oder Gruppen, um den Bereich.
  
![Details zur Anti-Phishing-Standard-Richtlinie](media/30c21ceb-df52-4c93-aa65-f44a55dc1009.jpg)
  
Später in 2018 So richten Sie Ihre Standard--Schutz über PowerShell ein:
  
```
$defaultAntiphishPolicy = Get-AntiphishingPolicy -IsDefault $true
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement <$true|$false>
```

Sie sollten nur Anti-spoofing Schutz deaktivieren, wenn Sie einen anderen e-Mail-Server oder Server vor Office 365 haben (Siehe legitime Szenarien Anti-spoofing für weitere Details deaktivieren). 
  
```
$defaultAntiphishPolicy = Get-AntiphishingPolicy -IsDefault $true
Set-AntiphishPolicy -Identity $defaultAntiphishPolicy.Name -EnableAntispoofEnforcement $false 

```
> [!IMPORTANT]
> Wenn der erste Nächster Hop in Ihrem e-Mail-Pfad Office 365 ist, und Sie zu viele legitimen e-Mails, die als Spoofing markiert erhalten, sollten Sie zunächst Einrichten Ihrer Absender, die mit Spoofing stammen Senden von e-Mails an Ihre Domäne zulässig sind (siehe Abschnitt "Verwalten von legitimen Absender, von u senden * Nauthenticated e-Mail"* ). Wenn Sie noch zu viele falsch positive Ergebnisse abrufen (z. B. legitime Nachrichten als Spoofing gekennzeichnet), es wird nicht empfohlen, Anti-spoofing Protection vollständig deaktivieren. Stattdessen wird empfohlen, Basic anstelle von hoher Schutz auswählen.                    Es empfiehlt sich, falsch positive Ergebnisse als auf verfügbar machen, Ihre Organisation gefälschten e-Mail die zur Einführung erheblich höherer Kosten langfristig landen konnte durcharbeiten.

### <a name="managing-legitimate-senders-who-are-sending-unauthenticated-email"></a>Verwalten von legitimen Absender, die nicht authentifizierte e-Mail senden

Office 365 werden von nachverfolgt, die für Ihre Organisation nicht authentifizierte e-Mail gesendet hat. Wenn der Dienst geht davon aus, dass der Absender nicht legitime ist, wird es dann als ein Fehler *Compauth* gekennzeichnet. Dies wird als SPOOFING klassifiziert werden, obwohl sie Ihre Richtlinie Anti-spoofing abhängig, die auf die Nachricht angewendet wurde. 
  
Jedoch können als Administrator, Sie angeben die Absender zulässig sind zum Senden von e-Mails, die mit Spoofing stammen Überschreiben des Office 365-Entscheidung.
  
**Methode 1: Wenn Ihre Organisation die Domäne besitzt Einrichten der e-Mail-Authentifizierung**
  
Diese Methode kann zum Auflösen organisationsintern spoofing und Cross-Domain-spoofing in Fällen, in denen Sie besitzen oder interagieren, mit mehreren Mandanten verwendet werden. Darüber hinaus werden Auflösen von Cross-Domain-spoofing, in dem Sie mit anderen Kunden in Office 365 senden, und auch Drittanbieter, die in anderen Anbieter gehostet werden.
  
Weitere Informationen finden Sie unter [Kunden von Office 365](#customers-of-office-365). 
 
**Methode 2 - Verwendung Spoofing Intelligence Zugelassene Absender nicht authentifizierte e-Mail konfigurieren**
  
[Spoofing Intelligence](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) können auch Absender zum Übertragen von nicht authentifizierter Nachrichten für Ihre Organisation zuzulassen. 
  
Für externe Domänen der gefälschte Benutzer ist die Domäne in die von-Adresse, während die sendende Infrastruktur der sendenden IP-Adresse ist (unterteilt/24 bis / CIDR-Bereichen), oder der organisatorischen Domäne der PTR-Eintrag (im folgenden Screenshot der sendende IP zu können werden 131.107.18.4, deren PTR-Eintrag outbound.mail.protection.outlook.com ist, und dies als outlook.com für die sendende Infrastruktur angezeigt würden).
  
Ändern Sie zum Zulassen von diesem Absender nicht authentifizierte e-Mail senden **No** auf **Ja**.
  
![Einrichten von Antispoofing zulässige Absender](media/d4334921-d820-4334-8217-788279701e94.jpg)
  
PowerShell können auch bestimmte Absender Ihrer Domäne Spoofing können: 
  
```
$file = "C:\My Documents\Summary Spoofed Internal Domains and Senders.csv"
```

```
Get-PhishFilterPolicy -Detailed -SpoofAllowBlockList -SpoofType External | Export-CSV $file
```

![Erste gefälschten Absender über die Powershell](media/0e27ffcf-a5db-4c43-a19b-fa62326d5118.jpg)
  
In der vorherigen Abbildung wurden zusätzliche Zeilenumbrüche hinzugefügt, damit dieser Screenshot wird angepasst, aber tatsächlich würden alle Werte in einer separaten Zeile angezeigt werden.
  
Bearbeiten Sie die Datei und suchen Sie nach der Zeile, die outlook.com und bing.com entspricht, und ändern Sie den Eintrag AllowedToSpoof von Nein auf Ja:
  
![Einstellung Spoofing zulassen auf Ja, über die Powershell](media/62340452-62d3-4958-9ce9-afe5275a870d.jpg)
  
Speichern Sie die Datei, und führen Sie dann aus: 
  
```
$UpdateSpoofedSenders = Get-Content -Raw "C:\My Documents\Spoofed Senders.csv"
Set-PhishFilterPolicy -Identity Default -SpoofAllowBlockList $UpdateSpoofedSenders
```

Dadurch können jetzt bing.com zum Senden von e-Mail von nicht authentifizierten \*. outlook.com.

**Methode 3: Erstellen Sie einen Eintrag "zulassen" für den Absender/Empfänger-Paar**
  
Sie können auch alle Spamfilterung nach einem bestimmten Absender umgehen. Weitere Informationen finden Sie unter [Gewusst wie: Sichere Absender mit einer Zulassungsliste "in Office 365 hinzufügen](https://blogs.msdn.microsoft.com/tzink/2017/11/29/how-to-securely-add-a-sender-to-an-allow-list-in-office-365/).
  
Wenn Sie diese Methode verwenden, überspringt die Spam und einige die Filterung Phishing, aber nicht schadsoftwarefilterung.
  
**4 - Methode wenden Sie sich an den Absender, und bitten Sie sie zum Einrichten von e-Mail-Authentifizierung**
  
Aufgrund des Problems, Spam und Phishing empfiehlt es sich alle Absender e-Mail-Authentifizierung eingerichtet haben. Wenn Sie ein Administrator der sendenden Domäne kennen, wenden Sie sich an sie und die Anforderung, die sie e-Mail-Authentifizierung Datensätze einrichten, damit keine Außerkraftsetzungen hinzufügen. Weitere Informationen finden Sie unter [Administratoren von Domänen, die nicht Office 365-Kunden sind](#administrators-of-domains-that-are-not-office-365-customers)"weiter unten in diesem Artikel. 
  
Zwar es schwierig unter zuerst auf die Domänen authentifizieren senden möchten, im Laufe der Zeit als mehr e-Mail-Filter starten junking oder sogar ihren e-Mail ablehnen, verursacht diese So richten die richtigen Einträge für eine bessere Bereitstellung sicherzustellen.
  
### <a name="viewing-reports-of-how-many-messages-were-marked-as-spoofed"></a>Anzeigen von Berichten über wie viele Nachrichten gekennzeichnet wurden, als manipuliert

Nachdem Ihre Anti-spoofing-Richtlinie aktiviert ist, können Sie Bedrohungsanalyse, mit Zahlen wie viele Nachrichten als Phishing gekennzeichnet sind. Wechseln Sie zu diesem Zweck in die Sicherheit &amp; Compliance Center (SCC) unter Threat Management \> -Explorer legen Sie die Ansicht auf Phishing und Gruppe nach Domäne des Absenders oder Schutzstatus:
  
![Anzeigen, wie viele Nachrichten als Phishing gekennzeichnet sind](media/de25009a-44d4-4c5f-94ba-9c75cd9c64b3.jpg)
  
Sie können interagieren mit den verschiedenen Berichten angezeigt, wie viele als Phishing, einschließlich als SPOOFING markierte Nachrichten gekennzeichnet wurden. Weitere Informationen finden Sie unter [Erste Schritte mit Office 365 Bedrohungsanalyse](https://support.office.com/article/get-started-with-office-365-threat-intelligence-38e9b67f-d188-490f-bc91-a1ae4b270441).
  
Sie können nicht noch aufgeteilt, die welche Nachrichten gekennzeichnet wurden aufgrund von spoofing im Vergleich zu anderen Arten von Phishing (Allgemeine Phishing, Domänen oder Benutzer Identitätswechsel usw.). Weiter unten in 2018, Sie werden jedoch möglich, über die Sicherheit &amp; Compliance Center. Wenn Sie dies tun, können Sie diesen Bericht als Ausgangspunkt um sendende Domänen zu identifizieren, die möglicherweise legitime, die als Spoofing aufgrund von Fehler bei der Authentifizierung gekennzeichnet sind.
  
Im folgende Screenshot ist ein Vorschlag für wie diese Daten sehen, jedoch möglicherweise ändern, wenn veröffentlicht:
  
![Anzeigen von Berichten nach Erkennungstyp phishing](media/dd25d63f-152c-4c55-a07b-184ecda2de81.jpg)
  
Für nicht-ATP und E5 Kunden diese Berichte werden weiter unten in 2018 unter der Berichte Threat Protection Status (TPS) zur Verfügung stehen, jedoch werden von mindestens 24 Stunden verzögert. Diese Seite wird aktualisiert, wie sie die Sicherheit integriert sind &amp; Compliance Center.
  
### <a name="predicting-how-many-messages-will-be-marked-as-spoof"></a>Wie viele Nachrichten als Spoofing gekennzeichnet werden Vorhersage

Weiter unten in 2018 einmal aktualisiert Office 365 seiner Einstellungen für die Erzwingung der Anti-spoofing ausschalten können, oder auf mit Basic oder hoch Erzwingung erhalten Sie die Möglichkeit, finden Sie unter wie Disposition der Nachricht an die verschiedenen Einstellungen geändert wird. D. h., wenn Anti-spoofing deaktiviert ist, können Sie sehen, wie viele Nachrichten als Spoofing erkannt werden, wenn Sie zu Basic aktivieren; oder, wenn es Basic ist, Sie sehen, wie viele weitere Nachrichten als Spoofing erkannt werden, wenn Sie es auf hoch aktivieren.
  
Dieses Feature ist derzeit in der Entwicklung. Weitere Details definiert sind, wird auf dieser Seite mit der Sicherheit und Compliance Center Screenshots und mit PowerShell Beispielen aktualisiert.
  
!["Was geschieht, wenn" Bericht zum Aktivieren der antispoofing](media/fdd085ae-02c1-4327-a063-bfe9a32ff1eb.jpg)
  
![Mögliche UX für gefälschten Absender zulassen](media/53f9f73e-fb01-47f3-9a6d-850c1aef5efe.jpg)
  
### <a name="understanding-how-spam-phishing-and-advanced-phishing-detections-are-combined"></a>Grundlegendes zu wie spam, Phishing und erweiterte Phishing erkannte kombiniert werden

Exchange Online-Kunden - ATP und nicht ATP - können, geben Sie die Aktionen an, wenn der Dienst Nachrichten als Schadsoftware, Spam, vertrauenswürdige Spam, Phishing und Massen identifiziert wird. Allerdings mit der Einführung neuer Anti-Phishing-Richtlinien für ATP-Kunden und die Tatsache, dass eine Nachricht mehrere Arten der Erkennung (z. B. Malware, Phishing und Benutzeridentitätswechsel) erreicht werden kann, möglicherweise einige Verwirrung, welche Richtlinie angewendet wird. 
  
Im Allgemeinen wird die Richtlinie angewendet auf eine Nachricht in der Kopfzeile X-Forefront-Antispam-Report in der Eigenschaft Katze (Kategorie) identifiziert. 
  
|**Priority**|**Richtlinie**|**Kategorie**|**Wobei verwaltet?**|**Gilt für**|
|:-----|:-----|:-----|:-----|:-----|
|1  <br/> |Schadsoftware  <br/> |MALW  <br/> |[Malware-Richtlinie](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |Alle Kunden  <br/> |
|2  <br/> |Phishing  <br/> |PHSH  <br/> |[Gehostete inhaltsfilterrichtlinie](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Alle Kunden  <br/> |
|3  <br/> |Spam mit hoher Vertrauenswürdigkeit  <br/> |HSPM  <br/> |[Gehostete inhaltsfilterrichtlinie](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Alle Kunden  <br/> |
|4   <br/> |Spoofing  <br/> |SPOOFING  <br/> |[Anti-Phishing-Richtlinie](https://go.microsoft.com/fwlink/?linkid=864553), [Spoofing intelligence](https://support.office.com/article/Learn-more-about-spoof-intelligence-978c3173-3578-4286-aaf4-8a10951978bf) <br/> |Nur ATP  <br/> |
|5  <br/> |Spam  <br/> |SPM  <br/> |[Gehostete inhaltsfilterrichtlinie](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Alle Kunden  <br/> |
|6  <br/> |Massen  <br/> |MASSEN  <br/> |[Gehostete inhaltsfilterrichtlinie](https://technet.microsoft.com/library/jj200684%28v=exchg.150%29.aspx) <br/> |Alle Kunden  <br/> |
|7   <br/> |Domäne des Identitätswechsels  <br/> |DIMP  <br/> |[Anti-Phishing-Richtlinie](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |Nur ATP  <br/> |
|8   <br/> |Benutzeridentitätswechsel  <br/> |UIMP  <br/> |[Anti-Phishing-Richtlinie](https://go.microsoft.com/fwlink/?linkid=864553) <br/> |Nur ATP  <br/> |
   
Wenn Sie mehrere verschiedene Anti-Phishing-Richtlinien haben, wird die jeweils die höchste Priorität angewendet. Angenommen Sie, Sie haben zwei Richtlinien:
  
|**Richtlinie**|**Priority**|**Benutzer-Domäne Identitätswechsel**|**Anti-spoofing**|
|:-----|:-----|:-----|:-----|
|A  <br/> |1  <br/> |On  <br/> |Off  <br/> |
|B  <br/> |2  <br/> |Off  <br/> |Ein  <br/> |
   
Wenn eine Nachricht stammen und wird als Spoofing- und Benutzer Identitätswechsel identifiziert und Richtlinie A und B der Richtlinie, ist die gleiche Gruppe von Benutzern zugeordnet und klicken Sie dann die Nachricht wird als ein Spoofing behandelt, aber keine Aktion, da angewandt Anti-spoofing ist deaktiviert. , und SPOOFING führt eine höhere Priorität (4) als Benutzeridentitätswechsel (8).
  
So tätigen andere Arten von Phishing Richtlinie anzuwenden, benötigen Sie zum Anpassen der Einstellungen, die auf die verschiedenen Richtlinien angewendet werden.
  
### <a name="legitimate-scenarios-to-disable-anti-spoofing"></a>So deaktivieren Sie Anti-spoofing legitime Szenarien

Anti-spoofing besser Kunden vor Phishing-Angriffen geschützt, und daher deaktivieren Anti-spoofing-Schutz wird nicht empfohlen. Durch deaktivieren, können Sie einige kurzfristige falsch positive Ergebnisse, aber langfristig beheben, den, die Sie für weitere Risiko verfügbar gemacht werden soll. Die Kosten für das Einrichten der Authentifizierung auf der Seite Absender oder Anpassungen in der Phishing-Richtlinien sind in der Regel einmalige Ereignisse oder erfordern nur minimale, regelmäßige Wartung. Wurden die Kosten für die Wiederherstellung eines Phishing-Angriffs, in dem Daten offen gelegt wurde, oder Objekte ist jedoch gefährdet wesentlich höher.
  
Aus diesem Grund ist es besser über Anti-spoofing falsch positive Ergebnisse als zum Deaktivieren von Anti-Spoofing-Schutz verwendet werden.
  
Es ist jedoch ein gültigen Szenarios, in dem Anti-spoofing deaktiviert werden sollen, und, wenn vorhanden sind zusätzliche Mail-Filterung ist, Produkte in das routing von Nachrichten und Office 365 ist nicht der ersten Nächster Hop in der e-Mail-Pfad:
  
![Kunden-MX-Eintrag verweist nicht auf Office 365](media/62127c16-cfb8-4880-9cad-3c12d827c67e.jpg)
  
Der andere Server möglicherweise auf Standortbasierte Mail Exchange-Server eine Mail-Filterung Gerät wie Ironport, oder eine andere Cloud gehosteter Dienst.
  
Wenn Sie der MX-Eintrag, der die Domäne des Empfängers nicht zu Office 365 verweist, ist nicht erforderlich Anti-spoofing deaktivieren, da Office 365 die empfangende Domäne MX-Eintrag schlägt und Anti-spoofing, unterdrückt Wenn es auf einem anderen Dienst verweist. Wenn Sie nicht wissen Wenn Ihre Domäne im Vordergrund einen anderen Server enthält, können Sie eine Website wie MX-Toolbox, den MX-Eintrag nachschlagen. Sagen sie etwa folgendermaßen:
  
![MX-Eintrag gibt an, dass die Domäne zu Office 365 nicht verweist](media/d868bb9f-3462-49aa-baea-9447a3ce4877.jpg)
  
Diese Domäne hat einen MX-Eintrag, der nicht zu Office 365, verweist, damit Office 365 nicht Anti-spoofing Erzwingung angewendet wird.
  
Jedoch wenn des MX-Eintrags, der die Domäne des Empfängers *ist* , obwohl es ein anderer Dienst vor Office 365 ist zu Office 365, zeigen, sollten Sie Anti-spoofing deaktivieren. Das am häufigsten verwendete Beispiel ist die Verwendung von einem Empfänger zum Umschreiben von Adressen: 
  
![Routing-Diagramm für Empfänger zum Umschreiben von Adressen](media/070d90d1-50a0-42e4-9fd3-920bc99a7cad.jpg)
  
MX-Eintrag für die Domäne "contoso.com" verweist auf den lokalen Server während der Domäne @office365.contoso .net MX-Eintrag zu Office 365 verweist, da es enthält \*. protection.outlook.com, oder \*. eo.outlook.com des MX-Eintrags:
  
![MX-Eintrag zeigt zu Office 365, daher wahrscheinlich Empfänger umschreiben](media/4101ad51-ef92-4907-b466-b41d14d344ca.jpg)
  
Achten Sie darauf, dass Sie unterscheiden, wenn ein Empfänger Domäne MX-Eintrag nicht auf Office 365 verweist und es einen Empfänger zum Umschreiben von Adressen unterzogen wurde. Es ist wichtig, den Unterschied zwischen diesen beiden Fällen erkennen.
  
Wenn Sie nicht sicher sind, unabhängig davon, ob Ihre Domäne empfangende ein Empfänger-zum Umschreiben von Adressen unterzogen wurde, kann in einigen Fällen Ihnen sagen die Nachrichtenkopfzeilen verfolgen.
  
eine) zuerst, sehen Sie sich die Kopfzeilen der Nachricht für die Domäne des Empfängers in der Kopfzeile Authentifizierung Ergebnisse: 
  
```
Authentication-Results: spf=fail (sender IP is 1.2.3.4)
  smtp.mailfrom=example.com; office365.contoso.net; dkim=fail
  (body hash did not verify) header.d=simple.example.com;
  office365.contoso.net; dmarc=none action=none
  header.from=example.com; compauth=fail reason=001
```

Die Domäne des Empfängers befindet sich im roten Text oben in dieser Groß-/Kleinschreibung office365.contoso.net fett. Dies kann unterschiedlich sein, die den Empfänger im Feld an: Kopfzeile:
  
An: Beispiel Empfänger \<@ contoso.com Empfänger\>
  
Führen Sie einen MX-Eintrag Nachschlagen von der aktuellen Domäne des Empfängers. Wenn es enthält \*. protection.outlook.com, mail.messaging.microsoft.com, \*. eo.outlook.com oder mail.global.frontbridge.com, die bedeutet, dass die MX auf Office 365 verweist.
  
Wenn sie nicht über diese Werte enthält, bedeutet dies, dass die MX nicht zu Office 365 zeigt. Ein Tool, den, das Sie verwenden können, um dies zu überprüfen, ist MX-Toolbox.
  
In diesem Beispiel bestimmten folgender Meldung contoso.com, die Domäne, die den Empfänger aussieht, da so war: Kopfzeile, MX-Datensatz verweist auf einen Server auf Prem hat:
  
![MX-Eintrag verweist auf auf Prem server](media/2444144a-9a90-4319-96b2-d115041f669f.jpg)
  
Der eigentliche Empfänger ist jedoch office365.contoso.net, deren MX-Eintrag zu Office 365 verweist:
  
![MX zeigt auf Office 365, muss Empfänger zum Umschreiben von Adressen](media/10cf3245-9b50-475a-b655-d8a51f99d812.jpg)
  
Diese Meldung hat daher wahrscheinlich ein Empfänger-zum Umschreiben von Adressen unterzogen.
  
b) Zweitens müssen Sie allgemeine Anwendungsfälle des Empfängers umschreibt unterscheiden. Wenn Sie beabsichtigen, um die Domäne des Empfängers umzuschreiben \*. onmicrosoft.com, stattdessen umschreiben, um \*. mail.onmicrosoft.com.
  
Sobald Sie die Domäne des endgültige Empfängers, die hinter einem anderen Server geleitet werden identifiziert und der Empfänger Domäne MX-Eintrag tatsächlich auf Office 365 haben zeigt (wie in die DNS-Einträge veröffentlicht), können Sie fortfahren, Anti-spoofing deaktivieren.
  
Beachten Sie, dass Sie nicht möchten, Anti-spoofing deaktivieren, wenn die Domäne ersten Hop in der Routingpfad Office 365, nur beim hinter ein oder mehrere Dienste angezeigt wird.
  
### <a name="how-to-disable-anti-spoofing"></a>Zum Deaktivieren des Anti-spoofing

Wenn Sie bereits eine Anti-Phishing-Richtlinie erstellt haben, wird den EnableAntispoofEnforcement-Parameter auf $false festgelegt: 
  
```
$name = "<name of policy>"
Set-AntiphishPolicy -Identity $name -EnableAntiSpoofEnforcement $false 

```

Wenn Sie den Namen der Richtlinie (oder Richtlinien) deaktivieren nicht kennen, können Sie diese anzeigen: 
  
```
Get-AntiphishPolicy | fl Name
```

Wenn Sie nicht über die vorhandenen Anti-Phishing-Richtlinien verfügen, können Sie erstellen Sie eine und deaktivieren Sie es dann (selbst wenn Sie verfügen nicht über eine Richtlinie, Anti-spoofing weiterhin angewendete; klicken Sie auf Weiter unten in 2018 ist, eine Standardrichtlinie für Sie erstellt werden, und Sie dann deaktivieren können, anstatt eine) . Sie müssen diese Schritte auf mehrere Schritte durchführen: 
  
```
$org = Get-OrganizationConfig
$name = "My first anti-phishing policy for " + $org.Name
# Note: If the name is more than 64 characters, you will need to choose a smaller one
```

```
# Next, create a new anti-phishing policy with the default values
New-AntiphishPolicy -Name $Name
# Select the domains to scope it to
# Multiple domains are specified in a comma-separated list
$domains = "domain1.com, domain2.com, domain3.com"
# Next, create the anti-phishing rule, scope it to the anti-phishing rule
New-AntiphishRule -Name $name -AntiphishPolicy -RecipientDomainIs $domains
# Finally, scope the antiphishing policy to the domains
Set-AntiphishPolicy -Identity $name -EnableAntispoofEnforcement $false 

```

Deaktivieren von Anti-spoofing ist nur verfügbar über Cmdlet (weiter unten in Q2 2018 wird es in das Wertpapier verfügbar sein &amp; Compliance Center). Wenn Sie keinen Zugriff auf PowerShell erstellen Sie eine Support-Ticket.
  
Beachten Sie, dass dies auf Domänen nur angewendet werden soll, die indirekte routing, wenn zu Office 365 gesendet werden. Widerstehen nicht um Anti-spoofing aufgrund einige falsch positive Ergebnisse zu deaktivieren, ist es besser langfristig, die über diese verwendet werden.
  
### <a name="information-for-individual-users"></a>Informationen für einzelne Benutzer

Einzelne Benutzer werden in der Anti-spoofing Safety Spitze Umgang mit können begrenzt. Es gibt jedoch einige Dinge, die Sie tun können, um häufige Szenarien zu beheben.
  
### <a name="common-scenario-1---mailbox-forwarding"></a>Häufiges Szenario #1 - Postfach-Weiterleitung

Wenn Sie einen anderen e-Mail-Dienst verwenden und Ihre e-Mails an Office 365 oder Outlook.com weiterleiten, Ihre e-Mail-Adresse als spoofing gekennzeichnet werden kann und erhalten eine rote Safety Info. Office 365 und Outlook.com Planen dieses Problems automatisch, wenn die Weiterleitung kann eine der Outlook.com, Office 365, Google Mail oder keinen anderen Dienst, der die [Bogen-Protokoll](https://arc-spec.org)verwendet. Jedoch bis zur Bereitstellung dieser Fix sollten Benutzer das Feature für verbundene Konten verwenden ihre Nachrichten direkt, und nicht mit der Weiterleitungsoption importieren.
  
Um verbundene Konten in Office 365 einzurichten, wählen Sie das Zahnradsymbol in der oberen rechten Ecke der Office 365-Webbenutzeroberfläche \> Mail \> Mail \> Konten \> verbundene Konten.
  
![Option für Office 365 - verbundene Konten](media/e8e841ca-8861-4d83-8506-2a0858c51010.jpg)
  
Der Vorgang ist in Outlook.com, das Zahnradsymbol \> Optionen \> Mail \> Konten \> verbundene Konten.
  
### <a name="common-scenario-2---discussion-lists"></a>Häufiges Szenario #2 – listet Diskussion

Diskussionsforen, und ändern dessen Inhalt noch beibehalten werden das Original aus über Probleme mit Anti-spoofing daran sie Weiterleiten der Nachricht bekannt sind: Adresse.
  
Nehmen wir beispielsweise bei Ihrer e-Mail-Adresse ist Benutzer @ contoso.com und Vogel beobachten interessiert sind und teilnehmen an der Diskussion Liste Birdwatchers @ example.com. Wenn Sie eine Nachricht an die Diskussionsliste senden, können Sie auf diese Weise senden:
  
**Aus:** John Doe \<Benutzer @ contoso.com\> 
  
**An:** Diskussionsliste des Birdwatcher \<Birdwatchers @ example.com\> 
  
**Betreff:** Erstklassige Darstellung Blau Jays im oberen Bereich des MT. Rainer diese Woche 
  
Die Anzeige auschecken möchte diese Woche vom MT. Rainer?
  
Wenn die Liste der e-Mail-Nachricht empfängt, sie formatieren die Nachricht, dessen Inhalt zu ändern, und für den Rest der Elemente in der Diskussionsliste die Teilnehmer von den viele andere e-Mail-Empfängern besteht wiedergegeben.
  
**Aus:** John Doe \<Benutzer @ contoso.com\> 
  
**An:** Diskussionsliste des Birdwatcher \<Birdwatchers @ example.com\> 
  
**Betreff:** [BIRDWATCHERS] Erstklassige Darstellung Blau Jays im oberen Bereich des MT. Rainer diese Woche 
  
Die Anzeige auschecken möchte diese Woche vom MT. Rainer?
  
---
  
Diese Nachricht wurde an die Diskussionsliste Birdwatchers gesendet. Sie können jederzeit kündigen.
  
In den oben genannten wiedergegeben Nachricht enthält die gleichen aus: Adresse (Benutzer @ contoso.com), aber die ursprüngliche Nachricht durch Hinzufügen einer Kategorie auf die Zeile Betreff und eine Fußzeile am unteren Rand der Nachricht geändert wurde. Diese Art der Änderung der Nachricht ist häufig in Verteilerlisten und falsch positive Ergebnisse bewirken kann.
  
Wenn Sie oder eine Person in Ihrer Organisation ist ein Administrator der Adressenliste, Anti-spoofing Prüfung erfolgreich konfigurieren möglicherweise.
  
- Überprüfen Sie die häufig gestellten Fragen unter DMARC.org: [ich Mailingliste betreiben und ich möchte mit DMARC zusammenarbeiten, was soll ich tun?](https://dmarc.org/wiki/FAQ#I_operate_a_mailing_list_and_I_want_to_interoperate_with_DMARC.2C_what_should_I_do.3F)
    
- Lesen Sie die Anweisungen in diesem Blogbeitrag: [ein Tipp, Adressenliste Operatoren für die Zusammenarbeit mit DMARC um Fehler zu vermeiden.](https://blogs.msdn.microsoft.com/tzink/2017/03/22/a-tip-for-mailing-list-operators-to-interoperate-with-dmarc-to-avoid-failures/)
    
- Berücksichtigen Sie Installieren von Updates auf Ihrem Server Adressenliste Bogen unterstützen, finden Sie unter[https://arc-spec.org](https://arc-spec.org/)
    
Wenn Sie nicht den Besitz der Adressenliste verfügen:
  
- Sie können die Maintainer der Mailingliste eine der oben aufgeführten Optionen implementieren (sie sollten ebenfalls über e-Mail-Authentifizierung für die Domäne, der aus der Mailingliste Weiterleitung wird eingerichtet) anfordern
    
- Sie können in Ihrem e-Mail-Client zum Verschieben von Nachrichten in den Posteingang Postfachregeln erstellen. Sie können auch den Administratoren Ihrer Organisation zum Einrichten von Regeln zulassen oder im Abschnitt Verwalten von legitimen Absender, die nicht authentifizierte e-Mail senden erläutert Außerkraftsetzungen als anfordern
    
- Sie können ein Ticket Unterstützung mit Office 365 zum Erstellen einer Außerkraftsetzung für die Mailingliste als legitime behandelt erstellen.
    
### <a name="other-scenarios"></a>Andere Szenarien

1. Wenn keine der oben genannten häufigen Szenarien entsprechend Ihrer Situation an, melden Sie die Nachricht als falsch positive Wiederherstellung Microsoft. Weitere Informationen finden Sie im Abschnitt [wie kann ich Spam oder nicht-Spam-Nachrichten melden wieder an Microsoft?](#how-can-i-report-spam-or-non-spam-messages-back-to-microsoft) weiter unten in diesem Artikel. 
    
2. Sie können auch Ihr e-Mail-Administrator kontaktieren, der als eine mit Microsoft-Support-Ticket ausgelöst werden können. Die Microsoft-Entwicklungsteams untersucht, warum die Nachricht als ein Spoofing markiert wurde.
    
3. Wenn Sie, wer der Absender ist und sicher sind, dass sie nicht in böswilliger Absicht manipuliert wird sind wissen, können Sie darüber hinaus zurück an den Absender zurück, der angibt, dass sie Nachrichten von einem e-Mail-Server sendet, die nicht authentifiziert Antworten. Dies führt Manchmal den ursprünglichen Absender, wenden Sie sich an ihren IT-Administrator, die die Datensätze der erforderlichen e-Mail-Authentifizierung eingerichtet wird.
  
Wenn genügend Absender zurück Domänenbesitzer beantworten sollten sie die Authentifizierung von e-Mail-Datensätzen einrichten, spurs es ihnen in Aktion. Microsoft arbeitet außerdem mit Domänenbesitzer die erforderlichen Datensätze veröffentlichen, ist es hilfreich, noch mehr, wenn sie einzelne Benutzer anfordern.
    
4. Optional können Sie den Absender zur Liste sicherer Absender hinzufügen. Beachten Sie jedoch, dass wenn eine leitet dieses Kontos Spoofing, es an Ihr Postfach zugestellt werden. Diese Option sollte daher nur selten verwendet werden.
    
## <a name="how-senders-to-microsoft-should-prepare-for-anti-spoofing-protection"></a>Wie sollten Absender an Microsoft Anti-spoofing Schutz vorbereiten

Wenn Sie ein Administrator sind, die derzeit Nachrichten an Microsoft sendet Office 365 oder Outlook.com, sollten Sie sicherstellen, dass Ihre e-Mail-Adresse ordnungsgemäß authentifiziert ist anders als Spam oder Phishing gekennzeichnet werden kann. 
  
### <a name="customers-of-office-365"></a>Kunden von Office 365

Wenn Sie ein Office 365-Kunde sind, und Verwenden von Office 365 zum Senden von ausgehenden e-Mails:
  
- Für Ihre Domänen, die [in Office 365 zum Verhindern von spoofing SPF einrichten](https://technet.microsoft.com/en-us/library/dn789058%28v=exchg.150%29.aspx)
    
- Für Ihre primären Domänen, [Verwendung DKIM überprüfen Sie ausgehende e-Mail-Nachrichten, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet](https://technet.microsoft.com/en-us/library/mt695945%28v=exchg.150%29.aspx)
    
- [Verwenden Sie nach Möglichkeit DMARC Datensätze](https://technet.microsoft.com/en-us/library/mt734386%28v=exchg.150%29.aspx) für Ihre Domäne ermitteln, wer Ihre legitimen Absender sind 
    
Microsoft bietet keine ausführliche Implementierungsrichtlinien für die einzelnen SPF, DKIM und DMARC. Es ist jedoch viel online veröffentlichten Informationen. Es gibt auch 3. Unternehmen dedizierten zum Schutz Ihrer Organisation, die Authentifizierung von e-Mail-Datensätzen einrichten.
  
### <a name="administrators-of-domains-that-are-not-office-365-customers"></a>Administratoren von Domänen, die Office 365-Kunden nicht sind

Wenn Sie ein Domänenadministrator sind jedoch keiner Office 365-Kunden:
  
- Sie sollten einrichten SPF zum Veröffentlichen Ihrer Domäne sendenden IP-Adressen und richten Sie außerdem DKIM (sofern verfügbar) zum digitalen Signieren von Nachrichten. Sie sollten auch DMARC Datensätze einrichten.
    
- Wenn Sie Bulk Absender, die Übertragung von e-Mails in Ihrem Namen haben, sollten Sie mit diesen zum Senden von e-Mail in einer Weise arbeiten, dass die sendende Domäne in der From: Adresse (falls es Ihnen gehört) mit der Domäne, die SPF oder DMARC übergibt ausgerichtet.
    
- Wenn Sie über lokale e-Mail-Servern oder von einem Anbieter Software als Dienst oder aus einem Cloud-hosting-Dienst wie Microsoft Azure, GoDaddy, Racks mit 4U, Amazon-Webdienste senden oder ähnlich, Sie, dass sicherstellen sollten werden SPF-Eintrag hinzugefügt werden.
    
- Wenn Sie eine kleine Domäne, die vom Internetdienstanbieter gehostet wird sind, sollten Sie Ihre SPF-Datensatzes gemäß den Anweisungen einrichten, die Sie von Ihrem Internetdienstanbieter bereitgestellt wird. Die meisten Internetdienstanbieter bieten diese Arten von Anweisungen und auf Seiten der Unterstützung des Unternehmens befinden.
    
- Selbst wenn Sie mussten für die Authentifizierung von e-Mail-Datensätzen vor dem Veröffentlichen, und es einwandfrei funktioniert, müssen Sie dennoch Authentifizierung von e-Mail-Datensätzen an Microsoft senden veröffentlichen. Auf diese Weise werden Sie in der bekämpfen vor Phishing helfen, und reduzieren die Möglichkeit, dass Sie, oder Organisationen, die, denen Sie an, senden, Phished relevanten Informationen erhalten.
    
### <a name="what-if-you-dont-know-who-sends-email-as-your-domain"></a>Was geschieht, wenn Sie nicht wissen, wer e-Mail wie Ihre Domäne sendet?

Viele Domänen veröffentlichen nicht SPF-Datensätze, da sie nicht kennen, die alle Absender sind. Kein Problem, Sie müssen nicht wissen, wer alle werden. Sie sollten stattdessen gestartet erhalten möchten, durch das Veröffentlichen eines SPF-Datensatzes für diejenigen kennen, insbesondere, in Ihrem Unternehmen Datenverkehr gespeichert ist, und veröffentlichen eine neutrale SPF-Richtlinie? alle:
  
example.com IN TXT "V = spf1 include:spf.example.com? alle"
  
Die neutrale SPF-Richtlinie bedeutet, dass e-Mails, die nicht genügend Infrastruktur Ihres Unternehmens kommt e-Mail-Authentifizierung in allen anderen e-Mail-Empfänger übergibt. E-Mail, die von Absendern stammen, die Sie nicht wissen wird auf Neutral, zurückgreifen, die nahezu identisch mit kein SPF-Datensatz überhaupt Veröffentlichung ist.
  
Beim Senden von Office 365 wird e-Mail, die von Ihrem Unternehmen Datenverkehr stammt als authentifiziert gekennzeichnet werden, aber die e-Mail, die aus Quellen stammen, die Sie nicht wissen, die als Spoofing (in Abhängigkeit davon, ob Office 365 implizit noch authentifiziert er können) dennoch markiert. Dies ist jedoch weiterhin eine Verbesserung von alle e-Mails, die Sie als Spoofing von Office 365 markiert wird.
  
Mit eines SPF-Datensatzes mit einer fallback-Richtlinie von angefangen gelangt? all, können Sie schrittweise mehr senden Infrastruktur integrieren und veröffentlichen Sie eine strengere Richtlinie. 
  
### <a name="what-if-you-are-the-owner-of-a-mailing-list"></a>Was geschieht, wenn Sie den Besitzer der Mailingliste sind?

Finden Sie im Abschnitt [häufiges Szenario #2 – Diskussion enthält](#common-scenario-2---discussion-lists). 
  
### <a name="what-if-you-are-an-infrastructure-provider-such-as-an-internet-service-provider-isp-email-service-provider-esp-or-cloud-hosting-service"></a>Was geschieht, wenn Sie einen Anbieter Infrastruktur wie ein Internetdienstanbieter (ISP), e-Mail-Service Provider (ESP) oder Hostingdienst Cloud sind?

Wenn Sie eine Domäne e-Mail hosten und es e-Mail sendet, oder geben Sie hosting-Infrastruktur, die e-Mails senden kann, sollten Sie Folgendes:
  
- Stellen Sie sicher, dass Ihre Kunden was Sie veröffentlichen in ihre SPF-Datensätze in der Dokumentation
    
- Berücksichtigen Sie ausgehende e-Mail-Nachrichten, auch wenn der Kunde es (Signieren mit der Standarddomäne) explizit eingerichtet nicht DKIM-Signaturen anmelden. Sie können sogar Double Anmelden die e-Mails mit DKIM Signaturen (einmal mit Domäne des Kunden, wenn sie es eingerichtet haben, und ein zweites Mal mit Ihrem Unternehmen DKIM-Signatur)
    
Lässt an Microsoft erhebt keinen Anspruch, auch wenn Sie e-Mails, die aus Ihrer Plattform stammen authentifizieren, aber mindestens stellt sicher, dass Microsoft Ihre e-Mail-Adresse kein junk, da es nicht authentifiziert wird. Weitere Informationen zum lizenzübergang wie Outlook.com e-Mail-Filter finden Sie unter der [Outlook.com Postmaster-Seite](https://postmaster.live.com/pm/postmaster.aspx).
  
Weitere Informationen zu bewährten Methoden für Service Provider finden Sie unter [M3AAWG Mobile Messaging bewährte Methoden für den Dienstanbieter](https://www.m3aawg.org/sites/default/files/M3AAWG-Mobile-Messaging-Best-Practices-Service-Providers-2015-08.pdf).
  
## <a name="frequently-asked-questions"></a>Häufig gestellte Fragen

### <a name="why-is-microsoft-making-this-change"></a>Warum ist Microsoft diese Änderung vornehmen?

Da die Auswirkungen der Phishing-Angriffen und Microsoft, da der e-Mail-Authentifizierung um 15 Jahren wurde, davon ausgeht, dass das Risiko von weiterhin nicht authentifizierte e-Mail zulassen ist größer als das Risiko von legitimen e-Mails, dass verloren gehen.
  
### <a name="will-this-change-cause-legitimate-email-to-be-marked-as-spam"></a>Verursacht diese Änderung legitime e-Mail als Spam gekennzeichnet werden?

Zunächst werden einige Nachrichten, die als Spam gekennzeichnet sind. Jedoch wird im Laufe der Zeit Absender werden angepasst, und klicken Sie dann die Anzahl der Nachrichten, die als gefälschten falsches für die meisten e-Mail-Pfade unerheblich.
  
Microsoft selbst eingeführt diese Funktion zuerst bei Wochen vor der Bereitstellung für den Rest seiner Kunden. Während die Unterbrechung am ersten, es schrittweise abgelehnt ist aufgetreten.
  
### <a name="will-microsoft-bring-this-feature-to-outlookcom-and-non-advanced-threat-protection-customers-of-office-365"></a>Bringt Microsoft dieses Feature Outlook.com und nicht - erweiterte Threat Protection Kunden von Office 365?

Anti-spoofing Protection wird werden zunächst eingeführt ATP/E5 Kunden und in der Zukunft an die andere Benutzer freigegeben werden kann. Jedoch ist dies der Fall ist, möglicherweise einige Funktionen, die nicht wie reporting angewendet werden und benutzerdefinierte außer Kraft gesetzt.
  
### <a name="how-can-i-report-spam-or-non-spam-messages-back-to-microsoft"></a>Wie kann ich Spam oder nicht-Spam-Nachrichten an Microsoft gemeldet?

Sie können Sie im [Bericht-Add-in für Outlook](https://support.office.com/article/use-the-report-message-add-in-b5caa9f1-cdf3-4443-af8c-ff724ea719d2)verwenden, oder wenn die Datei darf nicht installiert, [Submit Spam, nicht-Spam und Phishing-Betrug Nachrichten an Microsoft zur Analyse](https://technet.microsoft.com/en-us/library/jj200769%28v=exchg.150%29.aspx).
  
### <a name="im-a-domain-administrator-who-doesnt-know-who-all-my-senders-are"></a>Ich bin ein Domänenadministrator, der wissen, wer sind alle meine Absender nicht!

Weitere Informationen finden Sie [Administratoren von Domänen, die nicht Office 365-Kunden sind](#administrators-of-domains-that-are-not-office-365-customers).
  
### <a name="what-happens-if-i-disable-anti-spoofing-protection-for-my-organization-even-though-office-365-is-my-primary-filter"></a>Was geschieht, wenn ich Anti-spoofing Schutz für meine Organisation deaktivieren, auch wenn Office 365 Meine primäre Filter ist?

Nicht empfohlen dies, da Sie mehr verpassten Phishing und Spamnachrichten verfügbar gemacht werden. Nicht alle Phishing spoofing ist, und nicht alle Spoofing ausgelassen werden. Jedoch kann das Risiko eines Kunden größer werden, Anti-spoofing ermöglicht.
  
### <a name="does-enabling-anti-spoofing-protection-mean-i-will-be-protected-from-all-phishing"></a>Bedeutet Aktivieren der Schutz Anti-spoofing, dass ich aus allen Phishing geschützt werden?

Leider, da Phishing anpassen, um andere Techniken verwenden wie gefährdet Nein, Konten oder Konten der kostenlosen Dienste einrichten. Phishing-Schutz funktioniert jedoch viel besser diese anderen Arten von Phishing-Methoden gefunden werden, da der Office 365-Schutz mit Ebenen sind Arbeit zusammen entwickelt und übereinander erstellen.
  
### <a name="do-other-large-email-receivers-block-unauthenticated-email"></a>Werden andere große e-Mail-Empfänger werden nicht authentifizierte e-Mail blockiert?

Nahezu alle große e-Mail-Empfänger implementieren herkömmlichen SPF, DKIM und DMARC. Einige Empfänger haben andere Prüfungen, die mehr strict als nur die Standards, aber nur wenige Gehe soweit Office 365 blockieren nicht authentifiziert werden e-Mail- und als eine behandelt werden. Jedoch die meisten der Branche ist immer mehr strict zu diesem bestimmten Typ der e-Mails, die besonders aufgrund des Problems, Phishing.
  
### <a name="do-i-still-need-the-advanced-spam-filtering-option-enabled-for-spf-hard-fail-if-i-enable-anti-spoofing"></a>Weiterhin benötige ich die Option Advanced Spam Filtering für "SPF schwerer Fehler" aktiviert, wenn ich Anti-spoofing aktivieren?

Nein, ist diese Option nicht mehr erforderlich, da das Feature Anti-spoofing nicht nur SPF Festplatte fehlschlägt, aber ein breiter Satz von Kriterien berücksichtigt. Wenn Sie Anti-spoofing aktiviert haben und die SPF schwerer Fehler Option aktiviert ist, Sie wahrscheinlich mehr falsch positive Ergebnisse erhalten. Es wird empfohlen, dieses Feature deaktivieren, wie es würde fast keine weiteren Catch Spam oder Phishing bieten und stattdessen hauptsächlich falsch positive Ergebnisse zu generieren.
  
### <a name="does-sender-rewriting-scheme-srs-help-fix-forwarded-email"></a>Hilft Absender Umschreiben von Adressen Schema (SRS) die weitergeleitete e-Mails beheben?

SRS behoben nur teilweise von weitergeleiteten e-Mails. Durch die SMTP-MAIL FROM umzuschreiben, können SRS sicherstellen, dass die weitergeleitete Nachricht übergibt SPF am nächsten Ziel. Allerdings, da Anti-spoofing von basiert: Adresse in Kombination mit der MAIL FROM oder DKIM Signieren Domäne (oder andere Signale), es ist nicht ausreichend, um zu verhindern, dass weitergeleitete e-Mails als manipuliert markiert werden.
  

