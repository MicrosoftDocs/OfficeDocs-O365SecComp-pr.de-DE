---
title: Konfigurieren Ihres Office 365-Mandanten für höhere Sicherheit
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/11/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid: MET150
ms.assetid: 8d274fe3-db51-4107-ba64-865e7155b355
description: Führt Sie durch die empfohlene Konfiguration für Mandantenweite Einstellungen, die sich auf die Sicherheit Ihrer Office 365-Umgebung auswirken. Ihre Sicherheitsanforderungen erfordern möglicherweise mehr oder weniger Sicherheit. Verwenden Sie diese Empfehlungen als Ausgangspunkt.
ms.openlocfilehash: f9d0eb9cec597c44781539fa9231c5bf2b3cfe16
ms.sourcegitcommit: c7989a8ead235aaebb2503abbde598f2c26c0056
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/14/2019
ms.locfileid: "33979471"
---
# <a name="configure-your-office-365-tenant-for-increased-security"></a>Konfigurieren Ihres Office 365-Mandanten für höhere Sicherheit

In diesem Thema werden Sie durch die empfohlene Konfiguration für Mandantenweite Einstellungen geleitet, die sich auf die Sicherheit Ihrer Office 365-Umgebung auswirken. Ihre Sicherheitsanforderungen erfordern möglicherweise mehr oder weniger Sicherheit. Verwenden Sie diese Empfehlungen als Ausgangspunkt.
  
## <a name="check-office-365-secure-score"></a>Überprüfen von Office 365 Secure Score

Office 365 Secure Score analysiert die Sicherheit Ihrer Office 365-Organisation basierend auf Ihren regulären Aktivitäten und Sicherheitseinstellungen und weist eine Bewertung zu. Notieren Sie sich zunächst Ihre aktuelle Bewertung. Wenn Sie einige Mandantenweite Einstellungen anpassen, erhöht sich Ihre Punktzahl. Das Ziel besteht nicht darin, die maximale Punktzahl zu erreichen, sondern sich über Möglichkeiten zum Schutz Ihrer Umgebung zu informieren, die sich nicht negativ auf die Produktivität Ihrer Benutzer auswirken. Siehe [Microsoft Secure Score](microsoft-secure-score.md).
  
## <a name="tune-threat-management-policies-in-the-microsoft-365-security-center"></a>Optimieren von Richtlinien zur Gefahren Verwaltung im Microsoft 365-Sicherheitscenter

Das Microsoft 365-Sicherheitscenter enthält Funktionen zum Schutz Ihrer Umgebung. Sie enthält auch Berichte und Dashboards, die Sie verwenden können, um Maßnahmen zu überwachen und zu ergreifen. Einige Bereiche verfügen über Standardrichtlinien Konfigurationen. Einige Bereiche schließen keine Standardrichtlinien oder-Regeln ein. Besuchen Sie diese Richtlinien unter Threat Management, um die Einstellungen für die Bedrohungs Verwaltung für eine sicherere Umgebung zu optimieren. 
  
|Bereich * * * *|Enthält eine Standardrichtlinie * * * *|Empfehlung * * * *|
|:-----|:-----|:-----|
|**AntiPhishing** <br/> |Ja  <br/> | Wenn Sie über eine benutzerdefinierte Domäne verfügen, erstellen Sie eine Richtlinie zum Schutz vor Phishing, um die e-Mail-Konten Ihrer wertvollsten Benutzer wie ihren CEO zu schützen und Ihre Domäne zu schützen. Review [richten Sie eine Anti-Phishing-Richtlinie](set-up-anti-phishing-policies.md) ein, und erstellen Sie eine Richtlinie mit dem Beispiel als Leitfaden: "Beispiel: Anti-Phishing-Richtlinie zum Schutz eines Benutzers und einer Domäne."|
|**Antischadsoftware-Engine** <br/> |Ja  <br/> | Bearbeiten Sie die Standardrichtlinie:  <br/> &ensp;&ensp;• Filter für gängige Anlagentypen – wählen Sie ein aus  <br/><br>  Sie können auch benutzerdefinierte Filterrichtlinien für Schadsoftware erstellen und diese auf bestimmte Benutzer, Gruppen oder Domänen in Ihrer Organisation anwenden.  <br/> <br> Weitere Informationen:  <br/> &ensp;&ensp;• [Schutz](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx) vor Schadsoftware <br/> &ensp;&ensp;• [Konfigurieren von Antischadsoftware-Richtlinien](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |
|**Sichere Anlagen in ATP** <br/> |Nein  <br/> | Schützen Sie auf der Hauptseite für sichere Anlagendateien in SharePoint, OneDrive und Microsoft Teams, indem Sie dieses Kontrollkästchen aktivieren:  <br/>  &ensp;&ensp;• Aktivieren von ATP für SharePoint, OneDrive und Microsoft Teams  <br/> <br> Fügen Sie eine neue Richtlinie für sichere Anlagen mit den folgenden Einstellungen hinzu:  <br/>  &ensp;&ensp;• Blockieren – Blockieren der aktuellen und zukünftigen e-Mails und Anlagen mit erkannter Schadsoftware (Wählen Sie diese Option)  <br/>  &ensp;&ensp;• Umleitung aktivieren – (markieren Sie dieses Kontrollkästchen, und geben Sie eine e-Mail-Adresse ein, beispielsweise ein Administrator-oder Quarantäne Konto).  <br/>  &ensp;&ensp;• Die obige Auswahl anwenden, wenn bei der Malware-Überprüfung auf Anlagen ein Timeout oder Fehler auftritt (aktivieren Sie dieses Kontrollkästchen)  <br/>  &ensp;&ensp;• Angewendet auf – die Empfängerdomäne lautet (Wählen Sie Ihre Domäne aus)  <br/>  <br>Weitere Informationen: [Einrichten von Office 365 ATP Safe Attachments Policies](set-up-atp-safe-attachments-policies.md) <br/> |
|**ATP-sichere Links** <br/> |Ja  <br/> | Diese Einstellung der Standardrichtlinie für die gesamte Organisation hinzufügen:  <br/> &ensp;&ensp;• Verwenden Sie sichere Links in: Office 365 ProPlus, Office für IOS und Android (Wählen Sie diese Option aus).  <br/> <br>Empfohlene Richtlinie für bestimmte Empfänger:  <br/>  &ensp;&ensp;• URLs werden umgeschrieben und anhand einer Liste bekannter böswilliger Links überprüft, wenn der Benutzer auf den Link klickt (Wählen Sie diese Option aus).  <br/>  &ensp;&ensp;• Verwenden Sie sichere Anlagen zum Überprüfen von herunterladbaren Inhalten (aktivieren Sie dieses Kontrollkästchen).  <br/>  &ensp;&ensp;• Angewendet auf – die Empfängerdomäne lautet (Wählen Sie Ihre Domäne aus) aus.  <br/> <br> Weitere Informationen: [Office 365 ATP Safe Links](atp-safe-links.md).  <br/> |
|**Antispam (e-Mail-Filterung)** <br/> |Ja  <br/> | Zu überwachen für:  <br/>  &ensp;&ensp;• Zu viel Spam – wählen Sie die benutzerdefinierten Einstellungen aus, und bearbeiten Sie die standardmäßige Spamfilter Richtlinie.  <br/>  &ensp;&ensp;• Spoof Intelligence – Überprüfungen von Absendern, die Ihre Domäne Spoofing. Blockieren oder zulassen dieser Absender.  <br/>  <br>Weitere Informationen: [Office 365 e-Mail-](anti-spam-protection.md)Antispamschutz.  <br/> |
|***E-Mail-Authentifizierung*** <br/> |Ja  <br/> |Die e-Mail-Authentifizierung verwendet ein DNS (Domain Name System) zum Hinzufügen von überprüfbaren Informationen zu e-Mail-Nachrichten über den Absender einer e-Mail. Office 365 richtet die e-Mail-Authentifizierung für die Standarddomäne ein (onmicrosoft.com), aber Office 365-Administratoren können auch e-Mail-Authentifizierung für benutzerdefinierte Domänen verwenden. Es werden drei Authentifizierungsmethoden verwendet: <br/> <br> &ensp;&ensp;• Sender Policy Framework (SPF).<br/>&ensp;&ensp;&ensp;&ensp;– Informationen zur Einrichtung finden Sie unter [Set up SPF in Office 365, um Spoofing zu verhindern](set-up-spf-in-office-365-to-help-prevent-spoofing.md). <br/> &ensp;&ensp;• DomainKeys Identified Mail (DKIM). <br/> &ensp;&ensp;&ensp;&ensp;-Siehe [Verwenden von DKIM für e-Mails in Ihrer benutzerdefinierten Domäne in Office 365](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email). <br>&ensp;&ensp;&ensp;&ensp;-Nachdem Sie DKIM konfiguriert haben, aktivieren Sie es im Sicherheitscenter.<br/> &ensp;&ensp;• Domänenbasierte Nachrichtenauthentifizierung,-Berichterstellung und-Konformität (DMARC). <br/> &ensp;&ensp;&ensp;&ensp;-Für DMARC-Setup [verwenden Sie DMARC, um e-Mails in Office 365 zu überprüfen](use-dmarc-to-validate-email.md).<br/>  <br/>
|

> [!NOTE]
> Für nicht standardmäßige Bereitstellungen von SPF, hybridbereitstellungen und Problembehandlung: [wie Office 365 das SPF (Sender Policy Framework) verwendet, um Spoofing zu verhindern](how-office-365-uses-spf-to-prevent-spoofing.md).

## <a name="view-dashboards-and-reports-in-the-security-and-compliance-centers"></a>Anzeigen von Dashboards und Berichten im Security and Compliance Center

Besuchen Sie diese Berichte und Dashboards, um mehr über die Integrität Ihrer Umgebung zu erfahren. Die Daten in diesen Berichten werden reicher, da Ihre Organisation Office 365-Dienste verwendet. Im Moment sollten Sie mit dem, was Sie überwachen und Maßnahmen ergreifen können, vertraut sein. Weitere Informationen finden Sie unter: [Reports in Microsoft 365 Security and Compliance Centers](reports-in-security-and-compliance.md).
  
|Dashboard * * * *|****Beschreibung****|
|:-----|:-----|
|Risikomanagement-Dashboard  <br/> |Verwenden Sie im Abschnitt "Bedrohungs Verwaltung" des Sicherheitscenters dieses Dashboard, um bereits behandelte Bedrohungen anzuzeigen, und als handliches Tool für die Berichterstellung an geschäftliche Entscheidungsträger, welche Bedrohungen Untersuchungen und Reaktionsmöglichkeiten bereits ausgeführt haben. Sichern Sie Ihr Unternehmen.  <br/> |
|Bedrohungs-Explorer  <br/> |Dies befindet sich auch im Abschnitt Bedrohungs Verwaltung des Sicherheitscenters. Wenn Sie einen Angriff auf Ihren Office 365-Mandanten untersuchen oder auftreten, verwenden Sie den Bedrohungs-Explorer, um Bedrohungen zu analysieren. Der Bedrohungs-Explorer zeigt den Umfang der Angriffe über die Zeit an, und Sie können diese Daten anhand von Bedrohungs Familien, der Angreifer-Infrastruktur und vieles mehr analysieren. Sie können auch verdächtige e-Mails für die Vorfall Liste kennzeichnen.  <br/> |
|Berichte – Dashboard  <br/> |Zeigen Sie im Abschnitt Berichte des Sicherheitscenters Überwachungsberichte für Ihre SharePoint Online-und Exchange Online-Organisationen an. Sie können auf der Seite Berichte anzeigen auch auf Azure Active Directory (Azure AD)-Benutzeranmelde Berichte, Benutzer Aktivitätsberichte und das Azure AD-Überwachungsprotokoll zugreifen.  <br/> |
   
![Sicherheitscenter-Dashboard](media/870ab776-36d2-49c7-b615-93b2bc42fce5.png)
  
## <a name="configure-additional-exchange-online-tenant-wide-settings"></a>Konfigurieren zusätzlicher Mandanten weiter Einstellungen für Exchange Online

Viele der Steuerelemente für Sicherheit und Schutz in der Exchange-Verwaltungskonsole sind auch im Sicherheitscenter enthalten. Sie müssen diese nicht an beiden Stellen konfigurieren. Hier sind ein paar zusätzliche Einstellungen, die empfohlen werden. 
  
|Bereich * * * *|Enthält eine Standardrichtlinie * * * *|Empfehlung * * * *|
|:-----|:-----|:-----|
|**Nachrichtenfluss** (Nachrichtenfluss Regeln, auch als Transportregeln bezeichnet)|Nein|Hinzufügen einer e-Mail-Fluss Regel zum Schutz vor Ransomware. Weitere Informationen finden Sie unter "Verwenden von Exchange-Transport Regeln zum Nachverfolgen oder Blockieren von e-Mails mit Dateierweiterungen, die von Ransomware verwendet werden" in diesem Blog Artikel: [How to Deal with Ransomware](https://blogs.technet.microsoft.com/office365security/how-to-deal-with-ransomware/). <br><br/> Lesen Sie die folgenden Themen: <br/>•[Schutz vor Ransomware](https://docs.microsoft.com/office365/admin/security-and-compliance/secure-your-business-data?view=o365-worldwide#ransomware)<br/>•[Schutz vor Schadsoftware und Ransomware in Office 365](office-365-malware-and-ransomware-protection.md)<br/><br/>  Erstellen Sie eine Nachrichtenfluss Regel, um die automatische Weiterleitung von e-Mails an externe Domänen zu verhindern. Weitere Informationen finden Sie unter [mildernde Client External Forwarding Rules with Secure Score](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/). <br/><br/> Weitere Informationen: [Nachrichtenfluss Regeln (Transportregeln) in Exchange Online](https://technet.microsoft.com/en-us/library/jj919238%28v=exchg.150%29.aspx)|
|**Aktivieren der modernen Authentifizierung**|Nein|Die moderne Authentifizierung in Office 365 ist eine Voraussetzung für die Verwendung der mehrstufigen Authentifizierung (Multi-Factor Authentication, MFA). MFA wird empfohlen, um den Zugriff auf Cloud-Ressourcen, einschließlich e-Mails, zu sichern. <br/><br/> Lesen Sie die folgenden Themen:  <br/>• [Aktivieren oder Deaktivieren der modernen Authentifizierung in Exchange Online](https://support.office.com/article/58018196-f918-49cd-8238-56f57f38d662) <br/>• [Skype for Business Online: Aktivieren des Mandanten für die moderne Authentifizierung](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx) <br/><br/> Die moderne Authentifizierung ist standardmäßig für Office 2016-Clients, SharePoint Online und OneDrive for Business aktiviert. <br/><br/> Weitere Informationen: [Verwenden der modernen Authentifizierung von Office 365 mit Office-Clients](https://support.office.com/article/776c0036-66fd-41cb-8928-5495c0f9168a)|
   
## <a name="configure-tenant-wide-sharing-policies-in-sharepoint-admin-center"></a>Konfigurieren von Mandanten weiten Freigaberichtlinien im SharePoint Admin Center

Microsoft-Empfehlungen für die Konfiguration von SharePoint-Teamwebsites mit höheren Schutzebenen, beginnend mit Basisschutz. Weitere Informationen finden Sie unter [Secure SharePoint Online Sites and Files](https://docs.microsoft.com/microsoft-365-enterprise/secure-sharepoint-online-sites-and-files)
  
Auf der Basisebene konfigurierte SharePoint-Teamwebsites ermöglichen die Freigabe von Dateien für externe Benutzer mithilfe von Links für anonymen Zugriff. Dieser Ansatz wird empfohlen, anstatt Dateien per e-Mail zu senden. 
  
Zur Unterstützung der Ziele für den grundlegenden Schutz konfigurieren Sie Mandantenweite Freigaberichtlinien wie hier empfohlen. Freigabeeinstellungen für einzelne Websites können restriktiver sein als diese Mandantenweite Richtlinie. 
  
|Bereich * * * *|Enthält eine Standardrichtlinie * * * *|Empfehlung * * * *|
|:-----|:-----|:-----|
|**Freigabe** (SharePoint Online und OneDrive for Business)|Ja|Die externe Freigabe ist standardmäßig aktiviert. Diese Einstellungen werden empfohlen: <br/>• Zulassen der Freigabe für authentifizierte externe Benutzer und Verwenden von anonymen Zugriffs Links (Standardeinstellung). <br/>  • Anonyme Zugriffs links laufen in dieser Anzahl von Tagen ab. Geben Sie, falls gewünscht, eine Zahl wie 30 Tage ein. <br/>• Standard Linktyp – wählen Sie Internal (nur Personen in der Organisation) aus. Benutzer, die die Verwendung anonymer Links freigeben möchten, müssen diese Option im Menü Freigabe auswählen. <br/><br/> Weitere Informationen: [Übersicht über die externe Freigabe](https://support.office.com/article/c8a462eb-0723-4b0b-8d0a-70feafe4be85)|
   
Das SharePoint Admin Center und das OneDrive for Business Admin Center bieten dieselben Einstellungen. Die Einstellungen im Admin Center gelten für beide.
  
## <a name="configure-settings-in-azure-active-directory"></a>Konfigurieren von Einstellungen in Azure Active Directory

Besuchen Sie diese beiden Bereiche in Azure Active Directory, um das Mandantenweite Setup für sicherere Umgebungen abzuschließen.
  
### <a name="configure-named-locations-under-conditional-access"></a>Konfigurieren von benannten Speicherorten (unter bedingter Zugriff)

Wenn Ihre Organisation Büros mit sicherem Netzwerkzugriff umfasst, fügen Sie die vertrauenswürdigen IP-Adressbereiche Azure Active Directory als benannte Speicherorte hinzu. Mit dieser Funktion können Sie die Anzahl der gemeldeten falsch positive Ergebnisse bei Anmelde Risikoereignissen reduzieren. 
  
Siehe: [benannte Standorte in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-named-locations)
  
### <a name="block-apps-that-dont-support-modern-authentication"></a>Blockieren von apps, die die moderne Authentifizierung nicht unterstützen

Für die mehrstufige Authentifizierung sind apps erforderlich, die die moderne Authentifizierung unterstützen. Apps, die die moderne Authentifizierung nicht unterstützen, können nicht mithilfe von Regeln für den bedingten Zugriff blockiert werden.
  
Für sichere Umgebungen müssen Sie die Authentifizierung für apps deaktivieren, die die moderne Authentifizierung nicht unterstützen. Sie können dies in Azure Active Directory mit einem Steuerelement ausführen, das in Kürze verfügbar ist.
  
Verwenden Sie in der Zwischenzeit eine der folgenden Methoden für SharePoint Online und OneDrive for Business:
  
- Verwenden Sie PowerShell, siehe [Blockieren von apps, die nicht die moderne Authentifizierung verwenden](https://docs.microsoft.com/intune-classic/deploy-use/block-apps-with-no-modern-authentication).
    
- Konfigurieren Sie dies im SharePoint Admin Center auf der Seite "Geräte Zugriff", und Steuern Sie den Zugriff von apps, die keine moderne Authentifizierung verwenden. Wählen Sie Block aus. 
    
## <a name="get-started-with-cloud-app-security-or-office-365-cloud-app-security"></a>Erste Schritte mit Cloud App Security oder Office 365 Cloud App Security

Verwenden Sie die Office 365 Cloud App Security, um Risiken auszuwerten, um verdächtige Aktivitäten zu warnen und automatisch Maßnahmen zu ergreifen. Erfordert Office 365 E5-Plan.
  
Oder verwenden Sie die Microsoft Cloud App Security, um auch nach erfolgtem Zugriff eine tiefere Transparenz zu erzielen, umfassende Steuerelemente und einen verbesserten Schutz für alle Ihre Cloud-Anwendungen, einschließlich Office 365. 
  
Da diese Lösung den EMS E5-Plan empfiehlt, empfehlen wir Ihnen, mit der Cloud-App-Sicherheit zu beginnen, damit Sie diese mit anderen SaaS-Anwendungen in Ihrer Umgebung verwenden können. Beginnen Sie mit Standardrichtlinien und-Einstellungen.
  
Weitere Informationen:
  
- [Bereitstellen von Cloud App Security](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)
    
- [Weitere Informationen zu Microsoft Cloud App Security](https://www.microsoft.com/cloud-platform/cloud-app-security)
    
- [Was ist Cloud App Security?](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security)
    
![Cloud App Security-Dashboard](media/1fb2aa65-54b8-4746-9f5e-c187d339e9f5.png)
  
## <a name="additional-resources"></a>Zusätzliche Ressourcen

Diese Artikel und Leitfäden enthalten zusätzliche normative Informationen zum Sichern Ihrer Office 365-Umgebung:
  
- [Microsoft-Sicherheitsrichtlinien für politische Kampagnen, gemeinnützige Organisationen und andere Agile Unternehmen](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance) (Sie können diese Empfehlung in jeder Umgebung verwenden, insbesondere in reinen Cloud-Umgebungen) 
    
- [Empfohlene Sicherheitsrichtlinien und-Konfigurationen für Identitäten und Geräte](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-365-policies-configurations) (diese Empfehlungen bieten Unterstützung für AD FS-Umgebungen) 
    

