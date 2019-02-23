---
title: ATP-sichere Links in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.date: 02/11/2019
ms.topic: overview
f1_keywords:
- "197503"
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
- MOE150
- ZVO160
- ZXL160
- ZPP160
- ZWD160
ms.assetid: dd6a1fef-ec4a-4cf4-a25a-bb591c5811e3
description: Mit der Funktion "sichere Links" können Sie Hyperlinks in Office-Dokumenten und e-Mail-Nachrichten per Mausklick überprüfen. Verwenden Sie sichere Links, um Ihre Organisation vor Phishing-und anderen Angriffen zu schützen.
ms.openlocfilehash: 3de79ec42a0d9534f93711741cb8427a0cde9fb1
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30214055"
---
# <a name="office-365-atp-safe-links"></a>ATP-sichere Links in Office 365

## <a name="overview-of-office-365-atp-safe-links"></a>Übersicht über Office 365 ATP-sichere Links

> [!IMPORTANT]
> Dieser Artikel richtet sich an Geschäftskunden. Wenn Sie ein Benutzer sind, der nach Informationen zu sicheren Links in Outlook sucht, lesen Sie den Thema [Advanced Outlook.com Security](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Office 365 ATP-sichere Links (Teil von [Advanced Threat Protection](office-365-atp.md)) können Ihre Organisation schützen, indem Sie per time-of-Click Überprüfung von Webadressen (URLs) in [e-Mail-Nachrichten](#how-atp-safe-links-works-with-email) und [Office-Dokumenten](#how-atp-safe-links-works-with-office-documents)bereitstellen. Der Schutz wird mithilfe von [ATP-Richtlinien für sichere Links](set-up-atp-safe-links-policies.md) definiert, die von ihrem Office 365-Sicherheitsteam festgelegt werden. 
  
Sobald Ihre ATP-Richtlinien für sichere Links vorhanden sind, können Office 365 globale Administratoren, Sicherheitsadministratoren und Sicherheits Leser [Berichte zu Advanced Threat Protection anzeigen](view-reports-for-atp.md). Anhand der Informationen in diesen Berichten kann Ihr Sicherheitsteam weitere Schritte Unternehmen, um die Sicherheitsvorfälle in Ihrer Organisation zu schützen.

Wenn [ATP neue Features hinzugefügt werden](office-365-atp.md#new-features-in-office-365-atp), kann ihr Office 365-sicherheitsTEAM die ATP-Richtlinien für sichere Links in Ihrer Organisation hinzufügen oder bearbeiten. Darüber hinaus können Sie Änderungen und Verbesserungen bemerken, wie etwa unsere neu überarbeiteten [Warn Seiten](atp-safe-links-warning-pages.md) und das systemeigene Link Rendering in Outlook.
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a>Funktionsweise von ATP-sicheren Links mit URLs in e-Mails

Auf hoher Ebene funktioniert der ATP Safe Links Protection für URLs in e-Mails (gehostet in Office 365, nicht lokal):
  
1. Personen erhalten e-Mail-Nachrichten, von denen einige URLs enthalten.
    
2. Alle e-Mail-Nachrichten durchlaufen Exchange Online Protection, wobei IP-und Umschlag Filter, Signaturen-basierter Schadsoftware-Schutz, Antispam-und Antischadsoftware-Filter angewendet werden. 
    
3. E-Mail-Nachrichten werden in den Posteingängen eingehen.
    
4. Ein Benutzer meldet sich bei Office 365 an und wechselt in den e-Mail-Posteingang.
    
5. Der Benutzer öffnet eine e-Mail-Nachricht und klickt auf eine URL in der e-Mail-Nachricht.
    
6. Die ATP-Funktion für sichere Links überprüft die URL sofort vor dem Öffnen der Website. Die URL wird als blockiert, bösartig oder sicher identifiziert.
    
    - Wenn es sich bei der URL um eine Website handelt, die in einer [benutzerdefinierten Liste "nicht umschreiben"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) für eine Richtlinie enthalten ist, die für den Benutzer gilt, wird die Website geöffnet. 
    
    - Wenn die URL einer Website entspricht, die in der [Liste der benutzerdefinierten blockiertEn URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md)der Organisation enthalten ist, wird eine [Warnmeldung](atp-safe-links-warning-pages.md) angezeigt. 
    
    - Wenn es sich bei der URL um eine Website handelt, die als bösartig festgelegt wurde, wird eine [Warnmeldung](atp-safe-links-warning-pages.md) angezeigt. 
    
    - Wenn die URL zu einer herunterladbaren Datei wechselt und die [ATP-Richtlinien](set-up-atp-safe-links-policies.md) Ihrer Organisation für die Überprüfung solcher Inhalte konfiguriert sind, wird die herunterladbare Datei überprüft. 
    
    - Wenn die URL als sicher festgelegt ist, wird die Website geöffnet.
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a>Funktionsweise von ATP-sicheren Links mit URLs in Office-Dokumenten

Auf hoher Ebene funktioniert der ATP Safe Links Protection für URLs in Office 365 proPlus-Anwendungen (aktuelle Versionen von Word, Excel und PowerPoint auf Windows oder Mac, Office-Apps auf iOS-oder Android-Geräten, Visio unter Windows, OneNote Online und Office Online):
  
1. Benutzer haben Office 365 proPlus auf Ihrem Computer, Smartphone oder Tablet installiert. (Oder Sie verwenden Office Online in Ihrem Browser.)
    
2. Ein Benutzer öffnet ein Word-, Excel-, PowerPoint-oder Visio-Projekt und meldet sich mit seinem Geschäfts-oder Schulkonto bei Office 365 Enterprise an. Das Dokument enthält URLs.
    
3. Wenn der Benutzer auf eine URL im Dokument klickt, wird der Link vom ATP Safe Links-Dienst überprüft.
    
  - Wenn es sich bei der URL um eine Website handelt, die in einer [benutzerdefinierten Liste "nicht umschreiben"](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) für eine Richtlinie enthalten ist, die für den Benutzer gilt, wird dieser Benutzer zur Website geleitet. 
    
  - Wenn die URL einer Website entspricht, die in der [Liste der benutzerdefinierten blockiertEn URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md)der Organisation enthalten ist, wird der Benutzer zu einer [Warnungsseite](atp-safe-links-warning-pages.md)geleitet.
    
  - Wenn es sich bei der URL um eine Website handelt, die als bösartig festgelegt wurde, wird der Benutzer zu einer [Warnungsseite](atp-safe-links-warning-pages.md)geleitet.
    
  - Wenn die URL zu einer herunterladbaren Datei wechselt und die [ATP-Richtlinien für sichere Links](set-up-atp-safe-links-policies.md) für solche Downloads konfiguriert sind, wird die herunterladbare Datei überprüft. 
    
  - Wenn die URL als sicher betrachtet wird, wird der Benutzer zur Website geleitet.

## <a name="how-to-get-atp-safe-links-protection"></a>How to Get ATP Safe Links Schutz

Stellen Sie zunächst sicher, dass Ihr Abonnement [Advanced Threat Protection](office-365-atp.md)enthält. ATP ist in Abonnements wie [microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5 usw. enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement verfügt, das nicht Office 365 ATP enthält, können Sie möglicherweise ATP als Add-on erwerben. Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 
  
Stellen Sie als nächstes sicher, dass Ihre ATP-Richtlinien für sichere Links definiert sind. (Weitere Informationen finden Sie unter [Einrichten von Office 365 ATP-Richtlinien für sichere Links](set-up-atp-safe-links-policies.md).) ATP-Features für sichere Links sind aktiv, wenn:
  
- **Die Richtlinien für ATP-sichere Links sind** für e-Mails und für Word-, Excel-, PowerPoint-und Visio-Dokumente eingerichtet. (Weitere Informationen finden Sie unter [Einrichten von Richtlinien für sichere Links in Office 365](set-up-atp-safe-links-policies.md).)

- **Office 365-Client-apps sind für die Verwendung der modernen Authentifizierung konfiguriert** . (Dies ist für den sicheren Schutz von ATP-Links in Office-Dokumenten). (Siehe [moderne Authentifizierung für Office 2016](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).) 
    
- Benutzer haben sich mit Ihrem Geschäfts-oder Schulkonto **bei Office 365 angemeldet** . (Siehe [Anmelden bei Office oder office 365](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)
    
- **Die E-Mail Ihrer Organisation durchläuft Exchange Online Protection**.  

Um ATP-Richtlinien zu definieren (oder zu bearbeiten), muss Ihnen eine entsprechende Rolle zugewiesen werden. Einige Beispiele werden in der folgenden Tabelle beschrieben:

|Rolle  |Wo/wie zugewiesen  |
|---------|---------|
|Office 365 globaler Administrator |Die Person, die sich für den Kauf von Office 365 registriert, ist standardmäßig globaler Administrator. (Weitere Informationen finden Sie unter [Informationen zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) .)         |
|Sicherheitsadministrator |Azure Active Directory Admin Center ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Exchange Online-Organisationsverwaltung |Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-make-sure-atp-safe-links-protection-is-in-place"></a>So stellen Sie sicher, dass ATP Safe Links Protection vorhanden ist

Als globaler Administrator oder Sicherheitsadministrator sollten Sie die Richtlinien für die [ATP Safe Links](set-up-atp-safe-links-policies.md)überprüfen. Richtlinien für ATP-sichere Links legen fest, ob Schutz nur für Hyperlinks in e-Mail-Nachrichten oder auch für URLs in Office-Dokumenten gilt.

Nachdem die Richtlinien für sichere Links für ATP feststehen, kann das Sicherheitsteam Ihrer Organisation sehen, wie die Verwendung von ATP Safe Links Protection für Ihre Organisation funktioniert, indem Sie [Berichte zu Advanced Threat Protection anzeigen](view-reports-for-atp.md). 

## <a name="example-scenarios"></a>Beispielszenarien
  
In der folgenden Tabelle werden einige Beispielszenarien beschrieben, in denen der ATP-Schutz für sichere Links möglicherweise nicht vorhanden ist. (In allen diesen Fällen wird davon ausgegangen, dass die Organisation Office 365 Enterprise E5 hat.)
  
|**Beispielszenario**|**Gilt in diesem Fall ATP Safe Links Protection?**|
|:-----|:-----|
|Jean ist Mitglied einer Gruppe mit ATP-Richtlinien für sichere Links für URLs in e-Mails und Office-Dokumenten. Jean öffnet eine PowerPoint-Präsentation, die jemand gesendet hat, und klickt dann auf eine URL in der Präsentation.  <br/> |Ja. Die festgelegten Richtlinien für ATP-sichere Links gelten für Jean es Group, Jean es e-Mail und Word, Excel, PowerPoint oder Visio Documents, die Jean öffnet, solange Jean mit Office 365 proPlus auf Windows-, iOS-oder Android-Geräten angemeldet ist.  <br/> |
|In der Organisation von Chris haben keine globalen oder Sicherheitsadministratoren eine ATP-Richtlinie für sichere Links definiert. Chris erhält eine e-Mail, die eine URL zu einer böswilligen Website enthält. Chris ist nicht bewusst, dass die URL bösartig ist und auf den Link klickt.  <br/> |Nein. Die Standardrichtlinie, die URLs für alle in der Organisation abdeckt, muss definiert werden, damit Schutz vorhanden ist.  <br/> |
|In der Organisation von Pat haben weder globale noch Sicherheitsadministratoren eine ATP-Richtlinie für sichere Links definiert oder bearbeitet. Pat öffnet ein Word-Dokument und klickt auf eine URL in der Datei.  <br/> |Nein. eine Richtlinie, die Office-Dokumente enthält, muss definiert werden, damit ein Schutz vorhanden ist. Weitere Informationen finden Sie unter [Einrichten von ATP-Richtlinien für sichere Links in Office 365](set-up-atp-safe-links-policies.md).<br/> |
|Lees Organisation hat eine ATP-Richtlinie für sichere Links `http://tailspintoys.com` , die als blockierte Website aufgeführt wurde. Lee erhält eine e-Mail-Nachricht, die `http://tailspintoys.com/aboutus/trythispage`eine URL enthält. Lee klickt auf die URL.<br/> |Es hängt davon ab, ob die gesamte Website und alle zugehörigen Unterseiten in der Liste der blockierten URLs enthalten sind. Weitere Informationen finden Sie unter [Einrichten einer benutzerdefinierten Liste blockiertEr URLs mit sicheren ATP-Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).<br/> |
|Jamie, Jeans Kollegen, sendet eine e-Mail an Jean, ohne zu wissen, dass die e-Mail eine bösartige URL enthält.  <br/> |Es hängt davon ab, ob die ATP-Richtlinien für sichere Links für e-Mails definiert sind, die innerhalb der Organisation gesendet werden. Weitere Informationen finden Sie unter [Einrichten von ATP-Richtlinien für sichere Links in Office 365](set-up-atp-safe-links-policies.md).<br/> |


  

