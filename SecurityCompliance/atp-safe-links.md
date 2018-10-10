---
title: ATP-sichere Links in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: Admin
ms.topic: overview
f1_keywords:
- "197503"
ms.service: o365-administration
localization_priority: Normal
ms.collection: Strat_O365_IP
search.appverid:
- MET150
- MOE150
- ZVO160
- ZXL160
- ZPP160
- ZWD160
ms.assetid: dd6a1fef-ec4a-4cf4-a25a-bb591c5811e3
description: Die sichere Links-Funktion bietet Zeit des klicken Sie auf Überprüfung von Hyperlinks in Office-Dokumenten und e-Mail-Nachrichten. Verwenden Sie sichere Links, um Ihre Organisation vor Phishing und anderen Angriffen zu schützen.
ms.openlocfilehash: 75703cbe6b6a5a5d102570288bb20e6814d095fc
ms.sourcegitcommit: 099bbfb1d16b251fd5cf18ec6515faaf9a989176
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25454372"
---
# <a name="office-365-atp-safe-links"></a>ATP-sichere Links in Office 365

## <a name="overview-of-office-365-atp-safe-links"></a>Übersicht über Office 365 ATP sichere Links

Office 365 ATP sichere Links (sichere Verknüpfungen ATP) (zusammen mit [Office 365 ATP sichere Anlagen](atp-safe-attachments.md)) ist ein Satz von Sicherheitsfunktionen als Teil von [Office 365 erweiterte Schutz](office-365-atp.md) für Unternehmen entwickelt. Sichere Links ATP können Schützen Ihrer Organisation durch Bereitstellen der Uhrzeit der klicken Sie auf Überprüfung der Webadressen (URLs) in [e-Mail-Nachrichten](#how-atp-safe-links-works-with-email) und [Office-Dokumenten](#how-atp-safe-links-works-with-office-documents). Schutz wird definiert, über die [sichere Links ATP Richtlinien](set-up-atp-safe-links-policies.md) , die vom Office 365 Security Team festgelegt werden. 
  
Nach dem Ihrer Richtlinien ATP sichere Links vorhanden sind, können globale Office 365-Administratoren, Sicherheitsadministratoren und Sicherheit Leser [für erweiterte Schutz-Berichte anzeigen](view-reports-for-atp.md). Die Informationen in diesen Berichten kann weitere Schritte sind erforderlich zum Schutz Ihrer Organisation oder Recherchieren sicherheitsrelevante Vorfälle Security Team helfen.
         
### <a name="how-atp-safe-links-works-with-urls-in-email"></a>Funktionsweise der ATP sichere Links mit URLs in e-Mail

Auf allgemeiner Ebene funktioniert ATP sichere Links Schutz für URLs in e-Mails (in Office 365 nicht lokalen gehostet):
  
1. Personen empfangen von e-Mail-Nachrichten, von die einige URLs enthalten.
    
2. Alle e-Mail-Nachrichten wird über Exchange Online Protection, wobei filtert Internetprotokoll (IP) und Umschlag, Signatur-basierte Malware Protection, Anti-Spam- und Anti-Malware Filter angewendet werden. 
    
3. E-Mail-Eingang im Posteingang von Personen.
    
4. Ein Benutzer meldet sich bei Office 365 und wechselt zu ihren e-Mail-Posteingang.
    
5. Der Benutzer wird eine e-Mail-Nachricht geöffnet, und klickt auf eine URL in der e-Mail-Nachricht.
    
6. Das Feature ATP sichere Links überprüft die URL unmittelbar vor dem Öffnen der Website. Die URL ist als blockiert, bösartiger oder sicheren identifiziert.
    
    - Ist die URL zu einer Website, die in einer [benutzerdefinierten Liste für "Nicht rewrite" URLs](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) für eine Richtlinie enthalten ist, die für den Benutzer gilt, wird die Website geöffnet. 
    
    - Ist die URL zu einer Website, die in der Organisation [benutzerdefinierte Liste der blockierten URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md)enthalten ist, wird eine [Warnung Seite](atp-safe-links-warning-pages.md) geöffnet. 
    
    - Ist die URL zu einer Website, die festgestellt wurde, dass bösartige werden, wird eine [Warnung Seite](atp-safe-links-warning-pages.md) geöffnet. 
    
    - Wenn die URL zu einer Datei zum Herunterladen wechselt und Ihrer Organisation [ATP sichere Links Richtlinien](set-up-atp-safe-links-policies.md) um solche Inhalte scannen konfiguriert sind, wird die herunterladbare Datei überprüft. 
    
    - Wenn die URL, zu schützen, bestimmt wird, wird die Website geöffnet.
    
### <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a>Funktionsweise der ATP sichere Links mit URLs in Office-Dokumenten

Auf allgemeiner Ebene funktioniert ATP sichere Links Schutz für URLs in Office 365 ProPlus-Anwendungen (aktuellen Versionen von Word, Excel und PowerPoint unter Windows oder Mac, Office-apps auf IOS- oder Android-Geräte, Visio auf Windows, OneNote Online und Office Online):
  
1. Personen installiert Office 365 ProPlus auf ihren Computer, Smartphone oder Tablet. (Oder verwenden in ihrem Browser Office Online.)
    
2. Ein Benutzer öffnet ein Word, Excel, PowerPoint oder Visio und meldet sich bei Office 365 Enterprise über ihr Konto arbeiten oder Schule. Das Dokument enthält URLs.
    
3. Wenn der Benutzer auf eine URL im Dokument klickt, wird der Link vom Dienst ATP sichere Links überprüft.
    
  - Ist die URL zu einer Website, die in einer [benutzerdefinierten Liste für "Nicht rewrite" URLs](set-up-a-custom-do-not-rewrite-urls-list-with-atp.md) für eine Richtlinie enthalten ist, die für den Benutzer gilt, wird der Benutzer zu der Website weitergeleitet. 
    
  - Ist die URL zu einer Website, die in der Organisation [benutzerdefinierte Liste der blockierten URLs](set-up-a-custom-blocked-urls-list-wtih-atp.md)enthalten ist, wird der Benutzer zu einer [Seite Warnung](atp-safe-links-warning-pages.md)vorgenommen.
    
  - Ist die URL zu einer Website, die festgestellt wurde, dass bösartige werden, wird der Benutzer zu einer [Seite Warnung](atp-safe-links-warning-pages.md)vorgenommen.
    
  - Wenn die URL zu einer Datei zum Herunterladen wechselt und die [sichere Links ATP Richtlinien](set-up-atp-safe-links-policies.md) zum Scannen solche Downloads konfiguriert sind, wird die herunterladbare Datei überprüft. 
    
  - Wenn die URL als sicher angesehen wird, wird der Benutzer auf der Website ausgeführt.

## <a name="how-to-get-atp-safe-links-protection"></a>Wie sichere Links ATP Protection abrufen

Sichere ATP-Links-Features sind Teil der [Erweiterte Schutz](office-365-atp.md), die in Office 365 Enterprise E5, Microsoft 365 Business und Microsoft 365 Enterprise enthalten ist. Wenn in Ihrer Organisation ein weiteres Abonnement von Office 365 Enterprise verwendet wird, kann der erweiterte Schutz als Add-on erworben werden. Weitere Informationen finden Sie unter [Office 365-Plattformdienstbeschreibung: Sicherheit in Office 365 &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) und [gekauft oder bearbeiten Sie ein Add-on für Office 365 für Unternehmen](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).
  
Die sichere ATP-Links-Features sind in den aktiven:
  
- Für e-Mail und für Word, Excel, PowerPoint und Visio-Dokumenten **ATP sichere Links Richtlinien eingerichtet werden** . (Siehe [ATP sichere Links Richtlinien in Office 365 einrichten](set-up-atp-safe-links-policies.md).)

- **Apps für Office 365-Clients sind so konfiguriert, dass moderne-Authentifizierung verwenden**. (Siehe [modernen Authentifizierung für Office 2016](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).) 
    
- Über ihr Konto arbeiten oder Schule **Benutzer in Office 365 angemeldet haben** . (Siehe [Office oder Office 365 anmelden](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)
    
- **E-Mail von Ihrer Organisation in Office 365 gehostet wird**, nicht in einem lokalen Server. 
    
### <a name="how-to-make-sure-atp-safe-links-protection-is-in-place"></a>Wie stellen Sie sicher, dass sichere Links ATP Schutz ist vorhanden

[Anzeigen von Berichten für erweiterte Schutz](view-reports-for-atp.md)ist eine gute Möglichkeit, finden Sie unter wie ATP sichere Links Schutz für Ihre Organisation arbeitet wird. Darüber hinaus als globaler Administrator oder Sicherheitsadministrator, müssen Sie Ihre [ATP sichere Links Richtlinien](set-up-atp-safe-links-policies.md)zu überprüfen. Sichere Links ATP Richtlinien bestimmen, ob Schutz auf Hyperlinks in e-Mail-Nachrichten nur oder URLs in Office-Dokumenten sowie angewendet wird.

### <a name="example-scenarios-where-atp-safe-links-protection-might-or-might-not-be-in-place"></a>Beispielszenarien, in dem sicheren Links ATP Protection möglicherweise oder ist möglicherweise nicht vorhanden
  
In der folgenden Tabelle werden einige Beispielszenarien, in dem sicheren Links ATP Protection möglicherweise oder möglicherweise nicht direkt, beschrieben. (In allen Fällen wird davon ausgegangen, dass die Organisation über Office 365 Enterprise E5 verfügt.)
  
|**Beispielszenario**|**In diesem Fall wird ATP sichere Links Protection werden angewendet?**|
|:-----|:-----|
|Jean ist ein Mitglied einer Gruppe mit sicheren Links ATP Richtlinien zu URLs in e-Mail- und Office-Dokumenten. Jean öffnet einer PowerPoint-Präsentation, die ein Benutzer gesendet, und klickt dann auf eine URL in der Präsentation.  <br/> |Ja. Die sichere Links ATP-Richtlinien, die definiert sind gelten für Jean Gruppe, Jeans e-Mails, die und Word, Excel, PowerPoint oder Visio-Dokumenten, die Jean geöffnet wurde, solange Jean angemeldet ist, und über Office 365 ProPlus bei Windows, IOS- oder Android-Geräte.  <br/> |
|In der Organisation, nicht globale oder Sicherheit Chris sind Administratoren ATP sichere Links Richtlinien noch definiert. Chris erhält eine e-Mail, die eine URL zu eine bösartige Website enthält. Chris nicht bekannt ist die URL böswilligen und klickt auf die Verknüpfung.  <br/> |Nein. In der Reihenfolge für den Schutz vorhanden sein muss die Standardrichtlinie, die URLs für alle Benutzer in der Organisation behandelt definiert werden.  <br/> |
|In Pats Organisation, nicht globalen oder Sicherheit haben Administratoren definiert oder Richtlinien ATP sichere Links noch bearbeitet. Pat öffnet ein Word-Dokument und eine URL in der Datei klickt.  <br/> |In der Reihenfolge für den Schutz vorhanden sein muss No. A-Richtlinie, die Office-Dokumenten definiert werden. Finden Sie unter [sichere Links ATP Richtlinien in Office 365 einrichten](set-up-atp-safe-links-policies.md).<br/> |
|Kelly Organisation verfügt über eine sichere Links ATP-Richtlinie, die hat `http://tailspintoys.com` als eine blockierte Website aufgeführt. Kelly erhält eine e-Mail-Nachricht, die eine URL zu enthält `http://tailspintoys.com/aboutus/trythispage`. Kelly klickt auf die URL.<br/> |Das hängt davon ab, ob die gesamte Website und alle ihre Unterseiten, in der Liste der enthalten sind URLs blockiert. Finden Sie unter [Einrichten einer benutzerdefinierten blockierte URLs Liste verwenden ATP sichere Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).<br/> |
|Frau Jeans Kollegen, sendet eine e-Mail an Jean, nicht bekannt, dass die e-Mail, eine böswillige URL enthält angezeigt wird.  <br/> |Das hängt davon ab, gibt an, ob sichere Links ATP Richtlinien für e-Mail innerhalb der Organisation gesendet definiert sind. Finden Sie unter [sichere Links ATP Richtlinien in Office 365 einrichten](set-up-atp-safe-links-policies.md).<br/> |

## <a name="new-features-are-continually-being-added-to-atp-safe-links"></a>Neue Features werden ständig ATP sichere Links hinzugefügt wird

Wir entwickeln sicherer Links ATP neue Features hinzufügen. In einigen Fällen Ruft ein neues Feature für sichere Links ATP Richtlinien geprüft und aktualisiert werden. Es folgen einige Beispiele:
  
- Verspätete Oktober 2017 ab, ist sicherer Links ATP erweitertem Schutz um URLs in e-Mail-als auch URLs in Office 365 ProPlus-Dokumenten, beispielsweise Word, Excel, PowerPoint und Visio auf Windows als auch Office apps auf iOS und Android-Geräte zuweisen. (Stellen Sie sicher, dass Sie [Modernen für Office-Authentifizierung](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016)verwenden.)
    
- März 2018 ab, ist sicherer Links ATP Schutz erweitert, um auf zwischen Personen innerhalb einer Organisation gesendeten e-Mails anwenden. (Stellen Sie sicher [Überprüfen](set-up-atp-safe-links-policies.md)und Bearbeiten Ihrer Richtlinien ATP sichere Links.)
 
- In der zweiten Hälfte des 2018 beginnen, ist sicherer Links ATP Schutz erweitert, um URLs in Office Online (Online Word, Excel Online, Online PowerPoint und OneNote Online) und Office 365 ProPlus auf einem Mac gilt (Stellen Sie sicher [Überprüfen](set-up-atp-safe-links-policies.md)und Bearbeiten Ihrer Richtlinien ATP sichere Links.)

- Anfang im September 2018, [Office 365 ATP Warnung Seiten](atp-safe-links-warning-pages.md) Feature ein neues Farbschema, Weitere Informationen und die Möglichkeit, die auf einer Website trotz fortgesetzt werden, wenn Warnungen und Empfehlungen. 
 
- Im Oktober 2018 beginnen und anschließend in den nächsten Monaten einführen, umgeschrieben Wenn Personen mit Outlook Web Application (OWA) oder Outlook, ATP sichere Links rendert ursprünglichen URLs nicht URLs. (Wir Aufrufen dieser systemeigene Link Sichtbarkeit.)

   
## <a name="related-topics"></a>Verwandte Themen

[Office 365 Advanced Threat Protection](office-365-atp.md)
  
[Einrichten von sicheren Links ATP Richtlinien in Office 365](set-up-atp-safe-links-policies.md)
  
[ATP sichere Anlagen in Office 365](atp-safe-attachments.md)
  
[ATP-Antiphishingfunktionen in Office 365](atp-anti-phishing.md)
  
[Anzeigen der Berichte zu Advanced Threat Protection](view-reports-for-atp.md)
  

