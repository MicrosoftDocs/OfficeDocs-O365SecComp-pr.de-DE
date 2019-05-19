---
title: Einrichten von SPF in Office 365 zum Verhindern von Spoofing
ms.author: tracyp
author: MSFTTracyP
manager: laurawi
ms.date: 2/19/2018
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 71373291-83d2-466f-86ea-fc61493743a6
ms.collection:
- M365-security-compliance
description: 'Zusammenfassung: Dieser Artikel enthält Informationen zum Aktualisieren des DNS-Eintrags (Domain Name Service) für die Verwendung von SPF (Sender Policy Framework) mit Ihrer benutzerdefinierten Domäne in Office 365. SPF hilft bei der Überprüfung ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne gesendet werden.'
ms.openlocfilehash: 5194a9a8a8b694bc2dbac0eaf9b50517e46a9064
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34158197"
---
# <a name="set-up-spf-in-office-365-to-help-prevent-spoofing"></a>Einrichten von SPF in Office 365 zum Verhindern von Spoofing

 **Zusammenfassung:** Dieser Artikel enthält Informationen zum Aktualisieren des DNS-Eintrags (Domain Name Service) für die Verwendung von SPF (Sender Policy Framework) mit Ihrer benutzerdefinierten Domäne in Office 365. SPF hilft bei der Überprüfung ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne gesendet werden. 
  
Für die Verwendung einer benutzerdefinierten Domäne erfordert Office 365, einen SPF (Sender Policy Framework) TXT-Eintrag Ihrem DNS-Eintrag hinzuzufügen, um Spoofing zu verhindern. SPF identifiziert, welche E-Mail-Server zum Senden von E-Mails in Ihrem Auftrag berechtigt sind. Im Grunde trägt SPF zusammen mit DKIM, DMARC und anderen Technologien von Office 365 dazu bei, Spoofing und Phishing zu verhindern. SPF wird als TXT-Eintrag hinzugefügt, der von DNS verwendet wird, um zu identifizieren, welche E-Mail-Server E-Mails im Auftrag Ihrer benutzerdefinierten Domäne senden können. Empfänger können auf den SPF TXT-Eintrag zugreifen, um festzustellen, ob eine Nachricht von Ihrer benutzerdefinierten Domäne über einen autorisierten Messagingserver kommt.
  
Nehmen wir beispielsweise an, dass Ihre benutzerdefinierte Domäne „contoso.com" Office 365 verwendet. Sie fügen einen SPF TXT-Eintrag hinzu, der die Office 365-Messagingserver als berechtigte E-Mail-Server für Ihre Domäne auflistet. Wenn der empfangende Messagingserver eine Nachricht von „joe@contoso.com" erhält, sucht der Server im SPF TXT-Eintrag nach „contoso.com" und findet heraus, ob die Nachricht gültig ist. Wenn der empfangende Server herausfindet, dass die Nachricht von einem anderen Server als den Office 365-Messagingservern kommt, die im SPF-Eintrag aufgelistet sind, kann der empfangende E-Mail-Server die Nachricht als Spam ablehnen.
  
Wenn Ihre benutzerdefinierte Domäne keinen SPF TXT-Eintrag aufweist, können einige empfangende Server die Nachricht auch sofort ablehnen. Das liegt daran, dass der empfangende Server nicht überprüfen kann, ob die Nachricht von einem autorisierten Messagingserver stammt.
  
Wenn Sie bereits E-Mail für Office 365 eingerichtet haben, haben Sie bereits die Messagingserver von Microsoft in DNS als SPF TXT-Eintrag hinzugefügt. Es gibt jedoch einige Fälle, in denen Sie Ihren SPF TXT-Eintrag in DNS möglicherweise aktualisieren müssen. Beispiel:
  
- In früheren Versionen mussten Sie Ihrer benutzerdefinierten Domäne einen anderen SPF TXT-Eintrag hinzufügen, wenn Sie SharePoint Online verwendet haben. Dies ist nicht mehr erforderlich. Diese Änderung sollte das Risiko reduzieren, dass SharePoint Online-Benachrichtigungsnachrichten im Junk-E-Mail-Ordner landen. Aktualisieren Sie Ihren SPF TXT-Eintrag, wenn Sie die Beschränkung von 10 Lookups erreichen und Fehlermeldungen erhalten wie z. B. „Suchlimit überschritten" und „Zu viele Hops".
    
- Wenn Sie eine Hybridumgebung mit Office 365 und Exchange (lokal) haben.
    
- Sie möchten DKIM und DMARC einrichten (empfohlen).
    
## <a name="updating-your-spf-txt-record-for-office-365"></a>Aktualisieren Ihres SPF TXT-Eintrags für Office 365

Bevor Sie den TXT-Eintrag im DNS aktualisieren, müssen Sie einige Informationen sammeln und das Format des Eintrags bestimmen. Auf diese Weise können Sie DNS-Fehler vermeiden. Erweiterte Beispiele, eine ausführlichere Erläuterung zur unterstützten SPF-Syntax finden Sie unter [How SPF works to prevent spoofing and phishing in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).
  
Sammeln Sie folgende Informationen:
  
- Den aktuellen SPF TXT-Eintrag für Ihre benutzerdefinierte Domäne. Anweisungen finden Sie unter [Sammeln der zum Erstellen von Office 365-DNS-Einträgen erforderlichen Informationen](https://support.office.microsoft.com/en-us/article/Gather-the-information-you-need-to-create-Office-365-DNS-records-77f90d4a-dc7f-4f09-8972-c1b03ea85a67).
    
- IP-Adressen von allen lokalen Messagingservern. Zum Beispiel **192.168.0.1**.
    
- Domänennamen für alle Domänen von Drittanbietern, die Sie in Ihren SPF TXT-Eintrag einschließen müssen. Einige Massen-E-Mail-Anbieter haben Unterdomänen für ihre Kunden eingerichtet. Das Unternehmen MailChimp hat beispielsweise **servers.mcsv.net** eingerichtet.
    
- Bestimmen Sie, welche Erzwingungsregel Sie für Ihren SPF TXT-Eintrag verwenden möchten. Wir empfehlen **-all**. Weitere Informationen zu anderen Syntaxoptionen finden Sie unter [Syntax des SPF TXT-Eintrags für Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFSyntaxO365).
    
### <a name="to-add-or-update-your-spf-txt-record"></a>So aktualisieren Sie den SPF TXT-Eintrag oder fügen ihn hinzu

1. Erstellen Sie Ihren SPF TXT-Eintrag, falls noch nicht geschehen, indem Sie die Syntax aus der folgenden Tabelle verwenden:
    
||**Wenn Sie Folgendes verwenden ...**|**Standard für Office 365-Kunden?**|**Fügen Sie Folgendes hinzu ...**|
|:-----|:-----|:-----|:-----|
|1  <br/> |Beliebiges E-Mail-System (erforderlich)  <br/> |Standard. Alle SPF TXT-Einträge beginnen mit dem folgenden Wert  <br/> |v=spf1  <br/> |
|2  <br/> |Exchange Online  <br/> |Standard  <br/> |include:spf.protection.outlook.com  <br/> |
|3  <br/> |Nur dediziert für Exchange Online  <br/> |Kein Standard  <br/> |IP4:23.103.224.0/19 IP4:206.191.224.0/19 IP4:40.103.0.0/16 include:SPF. Protection. Outlook. com  <br/> |
|4  <br/> |Office 365 Deutschland, nur Microsoft Cloud Deutschland  <br/> |Kein Standard  <br/> |einschließen von:SPF. Protection. Outlook. de  <br/> |
|5  <br/> |Drittanbieter-E-Mail-System  <br/> |Kein Standard  <br/> |include:\<Domänenname\>  <br/> Wobei „Domänenname" dem Domänennamen des Drittanbieter-E-Mail-Systems entspricht.  <br/> |
|6  <br/> |Lokales E-Mail-System Zum Beispiel Exchange Online Protection und ein anderes E-Mail-System  <br/> |Kein Standard  <br/> | Verwenden Sie einen der folgenden Einträge für jedes zusätzliche E-Mail-System:  <br/>  ip4:\<  _IP address_\>  <br/>  ip6:\<  _IP address_\>  <br/>  include:\<  _domain name_\>  <br/>  Dabei steht der Wert von \<  _IP address_\> für die IP-Adresse des anderen E-Mail-Systems und \< _domain name_\> für den Domänennamen des anderen E-Mail-Systems, das E-Mails im Auftrag Ihrer Domäne sendet.  <br/> |
|7  <br/> |Beliebiges E-Mail-System (erforderlich)  <br/> |Standard. Alle SPF TXT-Einträge enden mit diesem Wert  <br/> |\< _enforcement rule_\>  <br/> Kann einer von mehreren Werten sein. Es wird empfohlen, **-all** zu verwenden.  <br/> |
   
1,1 Wenn Sie beispielsweise vollständig in Office 365 gehostet werden, also keine lokalen e-Mail-Server haben, würde Ihr SPF TXT-Eintrag die Zeilen 1, 2 und 7 enthalten und würde wie folgt aussehen:
    
  ```
   v=spf1 include:spf.protection.outlook.com -all
  ```

1,2 Dies ist der häufigste Office 365 SPF TXT-Eintrag. Dieser Datensatz funktioniert für fast alle, unabhängig davon, ob sich Ihr Office 365 Rechenzentrum in den Vereinigten Staaten oder in Europa (einschließlich Deutschland) oder an einem anderen Standort befindet.
    
1,3 Wenn Sie jedoch Office 365 Deutschland, einen Teil von Microsoft Cloud Deutschland, erworben haben, sollten Sie die include-Anweisung aus der Reihe 4 anstelle von "2" verwenden. Wenn Sie vollständig in Office 365 Deutschland gehostet werden (Sie haben also keine lokalen E-Mail-Server), sieht Ihr SPF TXT-Eintrag wie folgt aus und enthält Zeilen 1, 4 und 7:
    
  ```
   v=spf1 include:spf.protection.outlook.de -all
  ```

1,4 Wenn Sie bereits in Office 365 bereitgestellt sind und ihre SPF TXT-Einträge für Ihre benutzerdefinierte Domäne eingerichtet haben und Sie nach Office 365 Deutschland migrieren, müssen Sie Ihren SPF TXT-Eintrag aktualisieren. Ändern Sie dazu include **:SPF. Protection. Outlook. com** in **include:SPF. Protection. Outlook. de**.
    
2. Nachdem Sie den SPF TXT-Eintrag gebildet haben, müssen Sie den Eintrag in DNS aktualisieren. Sie können nur einen SPF TXT-Eintrag für eine Domäne haben. Wenn ein SPF TXT-Eintrag vorhanden ist, müssen Sie den vorhandenen Datensatz aktualisieren, anstatt einen neuen Datensatz hinzuzufügen. Wechseln Sie zu [Erstellen von DNS-Einträgen für Office 365](https://docs.microsoft.com/office365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider?view=o365-worldwide), und klicken Sie dann auf den Link für Ihren DNS-Host. 
    
3. Testen Sie den SPF TXT-Eintrag.
    
## <a name="more-information-about-spf"></a>Weitere Informationen zu SPF

Erweiterte Beispiele, eine ausführlichere Erläuterung zur unterstützten SPF-Syntax, zu Spoofing, zur Problembehandlung und zur Unterstützung von SPF durch Office 365 finden Sie unter [How SPF works to prevent spoofing and phishing in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).
  
## <a name="next-steps-after-you-set-up-spf-for-office-365"></a>Nächste Schritte: Nach dem Einrichten von SPF für Office 365

Gibt es Probleme mit Ihrem SPF TXT-Eintrag? Lesen Sie [Problembehandlung: Bewährte Methoden für SPF in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).
  
 Obwohl SPF Spoofing verhindern soll, gibt es Spoofingtechniken, gegen die SPF nicht schützen kann. Zum Einrichten eines entsprechenden Schutzes sollten Sie nach dem Einrichten von SPF auch DKIM und DMARC für Office 365 konfigurieren. Die ersten Schritte finden Sie unter [Verwenden von DKIM zum Überprüfen ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet werden](use-dkim-to-validate-outbound-email.md). Lesen Sie anschließend [Verwenden von DMARC zum Überprüfen von E-Mails in Office 365](use-dmarc-to-validate-email.md).
  

