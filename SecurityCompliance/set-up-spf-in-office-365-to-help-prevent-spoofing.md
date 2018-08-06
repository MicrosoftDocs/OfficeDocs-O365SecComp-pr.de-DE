---
title: Einrichten von SPF in Office 365 zum Verhindern von Spoofing
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 2/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: 71373291-83d2-466f-86ea-fc61493743a6
description: 'Zusammenfassung: Dieser Artikel enthält Informationen zum Aktualisieren des DNS-Eintrags (Domain Name Service) für die Verwendung von SPF (Sender Policy Framework) mit Ihrer benutzerdefinierten Domäne in Office 365. SPF hilft bei der Überprüfung ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne gesendet werden.'
ms.openlocfilehash: 1670e646d4eb847c72159e0b8b730ae08ea285a8
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22026362"
---
# <a name="set-up-spf-in-office-365-to-help-prevent-spoofing"></a>Einrichten von SPF in Office 365 zum Verhindern von Spoofing

 **Zusammenfassung:** Dieser Artikel enthält Informationen zum Aktualisieren des DNS-Eintrags (Domain Name Service) für die Verwendung von SPF (Sender Policy Framework) mit Ihrer benutzerdefinierten Domäne in Office 365. SPF hilft bei der Überprüfung ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne gesendet werden. 
  
Für die Verwendung einer benutzerdefinierten Domäne erfordert Office 365, einen SPF (Sender Policy Framework) TXT-Eintrag Ihrem DNS-Eintrag hinzuzufügen, um Spoofing zu verhindern. SPF identifiziert, welche E-Mail-Server zum Senden von E-Mails in Ihrem Auftrag berechtigt sind. Im Grunde trägt SPF zusammen mit DKIM, DMARC und anderen Technologien von Office 365 dazu bei, Spoofing und Phishing zu verhindern. SPF wird als TXT-Eintrag hinzugefügt, der von DNS verwendet wird, um zu identifizieren, welche E-Mail-Server E-Mails im Auftrag Ihrer benutzerdefinierten Domäne senden können. Empfänger können auf den SPF TXT-Eintrag zugreifen, um festzustellen, ob eine Nachricht von Ihrer benutzerdefinierten Domäne über einen autorisierten Messagingserver kommt.
  
Nehmen wir beispielsweise an, dass Ihre benutzerdefinierte Domäne „contoso.com“ Office 365 verwendet. Sie fügen einen SPF TXT-Eintrag hinzu, der die Office 365-Messagingserver als berechtigte E-Mail-Server für Ihre Domäne auflistet. Wenn der empfangende Messagingserver eine Nachricht von „joe@contoso.com“ erhält, sucht der Server im SPF TXT-Eintrag nach „contoso.com“ und findet heraus, ob die Nachricht gültig ist. Wenn der empfangende Server herausfindet, dass die Nachricht von einem anderen Server als den Office 365-Messagingservern kommt, die im SPF-Eintrag aufgelistet sind, kann der empfangende E-Mail-Server die Nachricht als Spam ablehnen.
  
Wenn Ihre benutzerdefinierte Domäne keinen SPF TXT-Eintrag aufweist, können einige empfangende Server die Nachricht auch sofort ablehnen. Das liegt daran, dass der empfangende Server nicht überprüfen kann, ob die Nachricht von einem autorisierten Messagingserver stammt.
  
Wenn Sie bereits E-Mail für Office 365 eingerichtet haben, haben Sie bereits die Messagingserver von Microsoft in DNS als SPF TXT-Eintrag hinzugefügt. Es gibt jedoch einige Fälle, in denen Sie Ihren SPF TXT-Eintrag in DNS möglicherweise aktualisieren müssen. Beispiel:
  
- In früheren Versionen mussten Sie Ihrer benutzerdefinierten Domäne einen anderen SPF TXT-Eintrag hinzufügen, wenn Sie SharePoint Online verwendet haben. Dies ist nicht mehr erforderlich. Diese Änderung sollte das Risiko reduzieren, dass SharePoint Online-Benachrichtigungsnachrichten im Junk-E-Mail-Ordner landen. Aktualisieren Sie Ihren SPF TXT-Eintrag, wenn Sie die Beschränkung von 10 Lookups erreichen und Fehlermeldungen erhalten wie z. B. „Suchlimit überschritten“ und „Zu viele Hops“.
    
- Wenn Sie eine Hybridumgebung mit Office 365 und Exchange (lokal) haben.
    
- Sie möchten DKIM und DMARC einrichten (empfohlen).
    
## <a name="updating-your-spf-txt-record-for-office-365"></a>Aktualisieren Ihres SPF TXT-Eintrags für Office 365
<a name="sectionSection0"> </a>

Bevor Sie den TXT-Eintrag im DNS aktualisieren, müssen Sie einige Informationen sammeln und das Format des Eintrags bestimmen. Auf diese Weise können Sie DNS-Fehler vermeiden. Erweiterte Beispiele, eine ausführlichere Erläuterung zur unterstützten SPF-Syntax finden Sie unter [Funktionsweise von SPF zur Verhinderung von Spoofing und Phishing in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).
  
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
|2  <br/> |Exchange Online  <br/> |Standard  <br/> |include: SPF.Protection.Outlook.com  <br/> |
|3  <br/> |Nur dediziert für Exchange Online  <br/> |Kein Standard  <br/> |IP4:23.103.224.0/19 ip4:206.191.224.0/19 ip4:40.103.0.0/16 include: SPF.Protection.Outlook.com  <br/> |
|4   <br/> |Office 365 Deutschland, nur Microsoft Cloud Deutschland  <br/> |Kein Standard  <br/> |include:SPF.Protection.Outlook.de  <br/> |
|5  <br/> |Drittanbieter-E-Mail-System  <br/> |Kein Standard  <br/> |include:\<Domänenname\>  <br/> Wobei „Domänenname" dem Domänennamen des Drittanbieter-E-Mail-Systems entspricht.  <br/> |
|6  <br/> |Lokales E-Mail-System Zum Beispiel Exchange Online Protection und ein anderes E-Mail-System  <br/> |Kein Standard  <br/> | Verwenden Sie einen der folgenden Einträge für jedes zusätzliche E-Mail-System:  <br/>  ip4:\<  _IP address_\>  <br/>  ip6:\<  _IP address_\>  <br/>  include:\<  _domain name_\>  <br/>  Dabei steht der Wert von \<  _IP address_\> für die IP-Adresse des anderen E-Mail-Systems und \< _domain name_\> für den Domänennamen des anderen E-Mail-Systems, das E-Mails im Auftrag Ihrer Domäne sendet.  <br/> |
|7   <br/> |Beliebiges E-Mail-System (erforderlich)  <br/> |Standard. Alle SPF TXT-Einträge enden mit diesem Wert  <br/> |\< _enforcement rule_\>  <br/> Kann einer von mehreren Werten sein. Es wird empfohlen, **-all** zu verwenden.  <br/> |
   
1.1 beispielsweise müssen, wenn Sie in Office 365 vollständig gehostet sind, d. h., Sie keine lokale e-Mail-Servern Ihrer SPF TXT Datensatz zählen Zeilen 1, 2 und 7 und würde wie folgt aussehen:
    
  ```
   v=spf1 include:spf.protection.outlook.com -all
  ```

1.2 Dies ist die am häufigsten verwendeten Office 365 SPF TXT-Eintrag. Dieser Eintrag eignet sich für fast alle, unabhängig davon, ob Ihr Office 365-Datencenter in den USA oder in Europa (einschließlich Deutschland) oder an einem anderen Standort befindet.
    
1.3 Wenn Sie Office 365 Deutschland, Teil des Microsoft-Cloud-Deutschland erworben haben sollten Sie die Include-Anweisung von Zeile 4 jedoch anstelle von Zeile 2 verwenden. Beispielsweise müssen, wenn Sie in Office 365 Deutschland vollständig gehostet sind, d. h., Sie keine lokalen e-Mail-Servern Ihrer SPF TXT Datensatz zählen Zeilen 1, 4 und 7 und würde wie folgt aussehen:
    
  ```
   v=spf1 include:spf.protection.outlook.de -all
  ```

1.4, wenn Sie bereits in Office 365 bereitgestellt werden und Ihre TXT SPF-Datensätze, die für Ihre benutzerdefinierte Domäne eingerichtet haben, und Sie nach Office 365 Deutschland migrieren, müssen Sie Ihre SPF TXT-Eintrag aktualisieren. Ändern Sie hierzu **include: SPF.Protection.Outlook.com** in **include.spf.protection.outlook.de**.
    
2. Nachdem Sie Ihren SPF TXT-Eintrag erstellt haben, müssen Sie den Eintrag in DNS aktualisieren. Sie dürfen nur einen SPF TXT-Eintrag für eine Domäne haben. Statt einen neuen Eintrag hinzuzufügen, müssen Sie, falls ein SPF TXT-Eintrag vorhanden ist, den vorhandenen Eintrag aktualisieren. Wechseln Sie zu [Erstellen von DNS-Einträgen für Office 365](https://support.office.microsoft.com/article/b0f3fdca-8a80-4e8e-9ef3-61e8a2a9ab23), und klicken Sie dann auf den Link für Ihren DNS-Host. (Wenn Ihr DNS-Host auf der Seite keinen Link aufweist, können Sie [den allgemeinen Anweisungen folgen](https://support.office.microsoft.com/article/7b7b075d-79f9-4e37-8a9e-fb60c1d95166), um Einträge hinzuzufügen. Wenden Sie sich andernfalls an den DNS-Host, um Hilfe zu erhalten.) 
    
3. Testen Sie Ihre SPF TXT-Eintrag.
    
## <a name="more-information-about-spf"></a>Weitere Informationen zu SPF
<a name="sectionSection1"> </a>

Erweiterte Beispiele, eine ausführlichere Erläuterung zur unterstützten SPF-Syntax, zu Spoofing, zur Problembehandlung und zur Unterstützung von SPF durch Office 365 finden Sie unter [Funktionsweise von SPF zur Verhinderung von Spoofing und Phishing in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#HowSPFWorks).
  
## <a name="next-steps-after-you-set-up-spf-for-office-365"></a>Nächste Schritte: Nach dem Einrichten von SPF für Office 365
<a name="sectionSection2"> </a>

Gibt es Probleme mit Ihrem SPF TXT-Eintrag? Lesen Sie [Problembehandlung: Bewährte Methoden für SPF in Office 365](how-office-365-uses-spf-to-prevent-spoofing.md#SPFTroubleshoot).
  
 Obwohl SPF Spoofing verhindern soll, gibt es Spoofingtechniken, gegen die SPF nicht schützen kann. Zum Einrichten eines entsprechenden Schutzes sollten Sie nach dem Einrichten von SPF auch DKIM und DMARC für Office 365 konfigurieren. Die ersten Schritte finden Sie unter [Verwenden von DKIM zum Überprüfen ausgehender E-Mails, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet werden](use-dkim-to-validate-outbound-email.md). Lesen Sie anschließend [Verwenden von DMARC zum Überprüfen von E-Mails in Office 365](use-dmarc-to-validate-email.md).
  

