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
ms.service: o365-administration
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
description: Die sichere Links-Funktion bietet Zeit des klicken Sie auf Überprüfung von Hyperlinks in Office-Dokumenten und e-Mail-Nachrichten. Verwenden Sie sichere Links, um Ihre Organisation vor Phishing und anderen Angriffen zu schützen.
ms.openlocfilehash: 77b7ac4af8cd9ad27f18af6fd55588e320da69ac
ms.sourcegitcommit: efccf5b4f22d34a9674bc55ebf3d88bc8bda2972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2019
ms.locfileid: "29995346"
---
# <a name="office-365-atp-safe-links"></a>ATP-sichere Links in Office 365

## <a name="overview-of-office-365-atp-safe-links"></a>Übersicht über Office 365 ATP sichere Links

> [!IMPORTANT]
> In diesem Artikel wird für Unternehmenskunden vorgesehen. Wenn Sie eine Suche nach Informationen zu sicheren Links in Outlook Privatbenutzer sind, finden Sie unter [Outlook.com erweiterte Sicherheit](https://support.office.com/article/advanced-outlook-com-security-for-office-365-subscribers-882d2243-eab9-4545-a58a-b36fee4a46e2).

Sichere Links zu Office 365 ATP (Teil der [Erweiterte Schutz](office-365-atp.md)) können Schützen Ihrer Organisation durch Bereitstellen der Uhrzeit der klicken Sie auf Überprüfung der Webadressen (URLs) in [e-Mail-Nachrichten](#how-atp-safe-links-works-with-email) und [Office-Dokumenten](#how-atp-safe-links-works-with-office-documents). Schutz wird definiert, über die [sichere Links ATP Richtlinien](set-up-atp-safe-links-policies.md) , die vom Office 365 Security Team festgelegt werden. 
  
Nach dem Ihrer Richtlinien ATP sichere Links vorhanden sind, können globale Office 365-Administratoren, Sicherheitsadministratoren und Sicherheit Leser [für erweiterte Schutz-Berichte anzeigen](view-reports-for-atp.md). Die Informationen in diesen Berichten kann weitere Schritte sind erforderlich zum Schutz Ihrer Organisation oder Recherchieren sicherheitsrelevante Vorfälle Security Team helfen.

Als [neue Features ATP hinzugefügt werden](office-365-atp.md#new-features-are-continually-being-added-to-atp)kann Ihrer Organisation ATP sichere Links Richtlinien Ihre Office 365 Security Team hinzufügen oder bearbeiten. Darüber hinaus können Sie Änderungen und Verbesserungen, wie unsere neu überarbeiteten [Warnung Seiten](atp-safe-links-warning-pages.md) und systemeigene Link Rendern in Outlook fest.
         
## <a name="how-atp-safe-links-works-with-urls-in-email"></a>Funktionsweise der ATP sichere Links mit URLs in e-Mail

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
    
## <a name="how-atp-safe-links-works-with-urls-in-office-documents"></a>Funktionsweise der ATP sichere Links mit URLs in Office-Dokumenten

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

Stellen Sie zunächst sicher, dass Ihr Abonnement [Erweiterte Threat Protection](office-365-atp.md)umfasst. ATP ist in Abonnements, wie beispielsweise [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5 usw. enthalten. Wenn Ihre Organisation über ein Office 365-Abonnement, die nicht in Office 365 ATP enthalten ist umfasst, können Sie potenziell ATP als Add-on erwerben. Weitere Informationen finden Sie unter [Erweiterte Threat Protection von Office 365-Pläne und zu Preisen](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 erweiterte Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description). 
  
Im nächsten Schritt stellen Sie sicher, dass alle Richtlinien ATP sichere Links definiert sind. (Finden Sie unter [Einrichten von Richtlinien für sichere Links zu Office 365 ATP](set-up-atp-safe-links-policies.md).) Sichere ATP-Links-Features sind in den aktiv:
  
- Für e-Mail und für Word, Excel, PowerPoint und Visio-Dokumenten **ATP sichere Links Richtlinien eingerichtet werden** . (Siehe [ATP sichere Links Richtlinien in Office 365 einrichten](set-up-atp-safe-links-policies.md).)

- **Apps für Office 365-Clients sind so konfiguriert, dass moderne-Authentifizierung verwenden** (Dies ist für sichere Links ATP Schutz in Office-Dokumente). (Siehe [modernen Authentifizierung für Office 2016](https://docs.microsoft.com/office365/enterprise/modern-auth-for-office-2013-and-2016).) 
    
- Über ihr Konto arbeiten oder Schule **Benutzer in Office 365 angemeldet haben** . (Siehe [Office oder Office 365 anmelden](https://support.office.com/article/b9582171-fd1f-4284-9846-bdd72bb28426).)
    
- **Ihres Unternehmens e-Mails über Exchange Online Protection übergibt**.  

Um ATP Richtlinien definieren (oder bearbeiten), müssen Sie eine der in der folgenden Tabelle beschriebenen Rollen zugewiesen werden:

|Rolle  |WHERE/wie zugewiesen.  |
|---------|---------|
|Office 365 globaler Administrator |Die Person, die zum Erwerben von Office 365 angemeldet ist ein globaler Administrator in der Standardeinstellung. (Siehe [zu Office 365-Administratorrollen](https://docs.microsoft.com/office365/admin/add-users/about-admin-roles) , um mehr zu erfahren.)         |
|Sicherheitsadministrator |Azure Active Directory-Verwaltungskonsole ([https://aad.portal.azure.com](https://aad.portal.azure.com))|
|Verwaltung von Exchange Online-Organisation |Exchange-Verwaltungskonsole ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) <br>oder <br>  PowerShell-Cmdlets (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)) |
    
## <a name="how-to-make-sure-atp-safe-links-protection-is-in-place"></a>Wie stellen Sie sicher, dass sichere Links ATP Schutz ist vorhanden

Als globaler Administrator oder Sicherheitsadministrator unbedingt Ihre [ATP sichere Links Richtlinien](set-up-atp-safe-links-policies.md)zu überprüfen. Sichere Links ATP Richtlinien bestimmen, ob Schutz auf Hyperlinks in e-Mail-Nachrichten nur oder URLs in Office-Dokumenten sowie angewendet wird.

Security-Team Ihrer Organisation kann sehen, nachdem ATP sichere Links Richtlinien vorhanden sind, finden Sie unter wie ATP sichere Links Schutz ist für Ihre Organisation durch [Anzeigen von Berichten für erweiterte Schutz](view-reports-for-atp.md)ist funktionsfähig. 

## <a name="example-scenarios"></a>Beispielszenarien
  
In der folgenden Tabelle werden einige Beispielszenarien, in dem sicheren Links ATP Protection möglicherweise oder möglicherweise nicht direkt, beschrieben. (In allen Fällen wird davon ausgegangen, dass die Organisation über Office 365 Enterprise E5 verfügt.)
  
|**Beispielszenario**|**In diesem Fall wird ATP sichere Links Protection werden angewendet?**|
|:-----|:-----|
|Jean ist ein Mitglied einer Gruppe mit sicheren Links ATP Richtlinien zu URLs in e-Mail- und Office-Dokumenten. Jean öffnet einer PowerPoint-Präsentation, die ein Benutzer gesendet, und klickt dann auf eine URL in der Präsentation.  <br/> |Ja. Die sichere Links ATP-Richtlinien, die definiert sind gelten für Jean Gruppe, Jeans e-Mails, die und Word, Excel, PowerPoint oder Visio-Dokumenten, die Jean geöffnet wurde, solange Jean angemeldet ist, und über Office 365 ProPlus bei Windows, IOS- oder Android-Geräte.  <br/> |
|In der Organisation, nicht globale oder Sicherheit Chris sind Administratoren ATP sichere Links Richtlinien noch definiert. Chris erhält eine e-Mail, die eine URL zu eine bösartige Website enthält. Chris nicht bekannt ist die URL böswilligen und klickt auf die Verknüpfung.  <br/> |Nein. In der Reihenfolge für den Schutz vorhanden sein muss die Standardrichtlinie, die URLs für alle Benutzer in der Organisation behandelt definiert werden.  <br/> |
|In Pats Organisation, nicht globalen oder Sicherheit haben Administratoren definiert oder Richtlinien ATP sichere Links noch bearbeitet. Pat öffnet ein Word-Dokument und eine URL in der Datei klickt.  <br/> |In der Reihenfolge für den Schutz vorhanden sein muss No. A-Richtlinie, die Office-Dokumenten definiert werden. Finden Sie unter [sichere Links ATP Richtlinien in Office 365 einrichten](set-up-atp-safe-links-policies.md).<br/> |
|Kelly Organisation verfügt über eine sichere Links ATP-Richtlinie, die hat `http://tailspintoys.com` als eine blockierte Website aufgeführt. Kelly erhält eine e-Mail-Nachricht, die eine URL zu enthält `http://tailspintoys.com/aboutus/trythispage`. Kelly klickt auf die URL.<br/> |Das hängt davon ab, ob die gesamte Website und alle ihre Unterseiten, in der Liste der enthalten sind URLs blockiert. Finden Sie unter [Einrichten einer benutzerdefinierten blockierte URLs Liste verwenden ATP sichere Links](set-up-a-custom-blocked-urls-list-wtih-atp.md).<br/> |
|Frau Jeans Kollegen, sendet eine e-Mail an Jean, nicht bekannt, dass die e-Mail, eine böswillige URL enthält angezeigt wird.  <br/> |Das hängt davon ab, gibt an, ob sichere Links ATP Richtlinien für e-Mail innerhalb der Organisation gesendet definiert sind. Finden Sie unter [sichere Links ATP Richtlinien in Office 365 einrichten](set-up-atp-safe-links-policies.md).<br/> |


  

