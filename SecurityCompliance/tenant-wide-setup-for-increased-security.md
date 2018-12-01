---
title: Konfigurieren Ihres Office 365-Mandanten für höhere Sicherheit
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/11/2018
ms.audience: ITPro
ms.topic: get-started-article
ms.service: o365-administration
localization_priority: Normal
search.appverid: MET150
ms.assetid: 8d274fe3-db51-4107-ba64-865e7155b355
description: Führt Sie durch die empfohlene Konfiguration für den Mandanten geltende Einstellungen, die sich auf die Sicherheit Ihrer Office 365-Umgebung auswirken. Ihre sicherheitsanforderungen erfordern möglicherweise mehr oder weniger Sicherheit. Verwenden Sie diesen Empfehlungen als Ausgangspunkt.
ms.openlocfilehash: af34d4b70c5cc1122dab840f9b4af8e2fe3c3a30
ms.sourcegitcommit: c34f1a0d560117153fc9a7b8da8994bc6fc53791
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/30/2018
ms.locfileid: "27118111"
---
# <a name="configure-your-office-365-tenant-for-increased-security"></a>Konfigurieren Ihres Office 365-Mandanten für höhere Sicherheit

In diesem Thema führt Sie durch die empfohlene Konfiguration für den Mandanten geltende Einstellungen, die sich auf die Sicherheit Ihrer Office 365-Umgebung auswirken. Ihre sicherheitsanforderungen erfordern möglicherweise mehr oder weniger Sicherheit. Verwenden Sie diesen Empfehlungen als Ausgangspunkt.
  
## <a name="check-office-365-secure-score"></a>Überprüfen Sie sichere Bewertung der Office 365

Office 365 Secure Faktor Sicherheit Ihrer Office 365-Organisation basierend auf Ihren regulären Aktivitäten und Sicherheitseinstellungen analysiert und weist eine Bewertung. Beginnen Sie mit dem Offlineschalten von Notieren Sie Ihr aktuelles Ergebnis. Einige Mandanten geltende Einstellungen anpassen, erhöhen Sie Ihre Punktzahl. Ziel ist es nicht für die max Bewertung zu erzielen, aber für Verkaufschancen zum Schutz Ihrer Umgebung beachten, die sich negativ auf nicht Produktivität für Ihre Benutzer auswirken. Finden Sie unter [Einführung in die Office 365 sichere Bewertung](office-365-secure-score.md).
  
## <a name="tune-threat-management-policies-in-the-office-365-security-amp-compliance-center"></a>Optimieren der Bedrohung Informationsverwaltungsrichtlinien in die Office 365-Sicherheit &amp; Compliance Center

Die Office 365-Sicherheit &amp; Compliance Center umfasst Funktionen, die Ihre Umgebung zu schützen. Darüber hinaus Berichte und Dashboards, überwachen und Ausführen einer Aktion verwendet werden können. Einige Bereiche im Lieferumfang von Standardkonfigurationen Richtlinie. Einige Bereiche enthalten nicht Standardrichtlinien oder Regeln. Besuchen Sie diese Richtlinien unter Threat Management Threat Management Einstellungen für eine sicherere Umgebung zu optimieren. 
  
|Bereich ***|Enthält eine standardmäßige Richtlinie ***|Empfehlung ***|
|:-----|:-----|:-----|
|**Anti-phishing** <br/> |Ja  <br/> | Wenn Sie eine benutzerdefinierte Domäne verfügen, erstellen Sie eine Anti-Phishing-Richtlinie zum Schutz der e-Mail-Konten Ihrer wichtigsten Benutzer, wie Ihre CEO und zum Schutz Ihrer Domäne. Überprüfen Sie [Richten Sie eine Anti-Phishing-Richtlinie](set-up-anti-phishing-policies.md) , und erstellen Sie eine Richtlinie unter Verwendung des Beispiels als Leitfaden: "Beispiel: Anti-Phishing-Richtlinie eines Benutzers und einer Domäne zu schützen."|
|**Antischadsoftware-Modul** <br/> |Ja  <br/> | Bearbeiten der Standardrichtlinie:  <br/> • Allgemeine Anlage Typen Filter – wählen Sie aus  <br/><br>  Sie können auch benutzerdefinierte Malware Filterrichtlinien erstellen und anwenden auf bestimmte Benutzer, Gruppen oder Domänen in Ihrer Organisation.  <br/> <br> Weitere Informationen:  <br/> • [Anti-Malware protection](https://technet.microsoft.com/en-us/library/jj200669%28v=exchg.150%29.aspx) <br/> • [Konfigurieren Antischadsoftware - Richtlinien](https://technet.microsoft.com/en-us/library/jj200745%28v=exchg.150%29.aspx) <br/> |
|**Sichere Anlagen in ATP** <br/> |Nein  <br/> | Schützen von Dateien in SharePoint, OneDrive und Microsoft-Teams, auf der Hauptseite für sichere Anlagen durch Aktivieren des Kontrollkästchens:  <br/>  • Schalten ATP für SharePoint, OneDrive und Microsoft-Teams  <br/> <br> Hinzufügen einer neuen Richtlinie für sichere Anlage mit diesen Einstellungen:  <br/>  • Blockieren – die aktuellen und zukünftigen-e-Mails und Anlagen mit gefundene Malware blockieren (Wählen Sie diese Option)  <br/>  • Enable umleiten – (Aktivieren Sie dieses Kontrollkästchen, und geben Sie eine e-Mail-Adresse, beispielsweise ein Konto Admin und Quarantäne)  <br/>  • Die obige Auswahl anwenden, wenn schadsoftwareprüfung für Anlagen Timeout oder Fehler tritt auf, (Aktivieren Sie dieses Kontrollkästchen)  <br/>  • Auf angewendet – die Domäne des Empfängers ist (Wählen Sie Ihre Domäne)  <br/>  <br>Weitere Informationen: [Einrichten von Richtlinien für Office 365 ATP sichere Anlagen](set-up-atp-safe-attachments-policies.md) <br/> |
|**ATP-sichere Links** <br/> |Ja  <br/> | Fügen Sie diese Einstellung auf die Standardrichtlinie für die gesamte Organisation:  <br/> • Verwendung sicherer Links in: Office 365 ProPlus, Office für iOS und Android (Wählen Sie diese Option aus).  <br/> <br>Empfohlene Richtlinien für bestimmte Empfänger:  <br/>  • URLs umgeschrieben werden und mit einer Liste bekannter bösartiger links abgeglichen werden, wenn Benutzer auf den Link klickt (Wählen Sie diese Option aus).  <br/>  • Verwenden sichere Anlagen zu überprüfenden Bücher (Aktivieren Sie dieses Kontrollkästchen).  <br/>  • Auf angewendet – die Domäne des Empfängers ist (Wählen Sie Ihre Domäne).  <br/> <br> Weitere Informationen: [Office 365 ATP sichere Links](atp-safe-links.md).  <br/> |
|**Anti-Spam (Mail-Filterung)** <br/> |Ja  <br/> | Was für die Überwachung:  <br/>  • Zu viel spam – wählen Sie die benutzerdefinierte Einstellungen und bearbeiten die Standardrichtlinie für Spam-Filter.  <br/>  • Spoofing Intelligence – Absender, die Ihre Domäne spoofing sind überprüfen. Blockieren oder Zulassen von diesen Absendern.<br/>  <br>Weitere Informationen: [Office 365 E-Mail Anti-Spam-Schutz](anti-spam-protection.md).  <br/> |
|**DKIM (DomainKeys identifiziert Mail)** <br/> |Ja  <br/> |DKIM ist ein Authentifizierungsprozess, der, die schützen kann Absender und Empfänger aus gefälscht (gefälschten) und Phishing-e-Mail. Ihres Mandanten umfasst eine Standardsignatur für Ihre Domäne. Erstellen Sie eine zusätzliche DKIM-Signatur, wenn Sie benutzerdefinierte Domänen zu Ihrem Mandanten hinzufügen.<br/> <br>Verwenden Sie die Anweisungen in diesem Artikel so konfigurieren Sie eine neue DKIM-Signatur, einschließlich CNAME, DMARC und SPF-Datensätze: [Verwendung DKIM überprüfen Sie ausgehende e-Mail-Nachrichten, die von Ihrer benutzerdefinierten Domäne in Office 365 gesendet](https://docs.microsoft.com/office365/SecurityCompliance/use-dkim-to-validate-outbound-email).  <br/> |
   
## <a name="view-dashboards-and-reports-in-the-security-amp-compliance-center"></a>Anzeigen von Dashboards und Berichte in das Wertpapier &amp; Compliance Center

Besuchen Sie diese Berichte und Dashboards erfahren Sie mehr über die Integrität der Umgebung. Die Daten in dieser Berichte werden umfassendere wie Ihre Organisation die Office 365-Dienste verwendet werden. Jetzt mit änderbare überwachen und Ausführen einer Aktion auf vertraut sein. Weitere Informationen finden Sie unter: [Berichte in die Office 365-Sicherheit &amp; Compliance Center](reports-in-security-and-compliance.md).
  
|Dashboard ***|****Beschreibung****|
|:-----|:-----|
|Threat Management dashboard  <br/> |Über die Sicherheit im Abschnitt Verwaltung von Bedrohung &amp; Compliance center, verwenden Sie das Dashboard, siehe Bedrohungen, die bereits bearbeitet wurden und als ein praktisches Tool zum Melden sich an Entscheidungsträger auf was Bedrohungsanalyse bereits geschehen ist zum Sichern Ihrer Business.  <br/> |
|Threat explorer  <br/> |Dies ist auch über die Sicherheit im Abschnitt Verwaltung von Bedrohung &amp; Compliance Center. Wenn Sie sind Untersuchen von oder Angriff mit Ihrem Office 365-Mandanten auftritt, verwenden Sie den Bedrohung Explorer Bedrohungen analysieren. Threat Explorer zeigt die Lautstärke Angriffe über einen Zeitraum ein, und Sie können diese Bedrohungsfamilien und Angreifer Infrastruktur Daten analysieren. Sie können auch keine verdächtigen e-Mails für die Liste Vorfälle markieren.  <br/> |
|Berichte – Dashboard  <br/> |Im Abschnitt Berichte über die Sicherheit &amp; Compliance Center Audit Anzeigen von Berichten für Ihre Exchange Online und SharePoint Online-Organisationen. Sie können auch auf Azure Active Directory (AD)-Anmeldung Benutzerberichte, Benutzeraktivität meldet, und der Azure AD-Überwachungsprotokolle melden Sie sich von der Seite "Berichte anzeigen".  <br/> |
   
![Sicherheit &amp; Compliance Center-Dashboard](media/870ab776-36d2-49c7-b615-93b2bc42fce5.png)
  
## <a name="configure-additional-exchange-online-tenant-wide-settings"></a>Konfigurieren Sie zusätzliche Einstellungen für Exchange Online-Mandanten geltende

Viele der Steuerelemente für Sicherheit und Schutz in der Exchange-Verwaltungskonsole sind auch in die Sicherheit und Compliance Center enthalten. Sie müssen nicht an beiden Stellen diese konfigurieren. Hier sind einige zusätzliche Einstellungen, die empfohlen werden. 
  
|Bereich ***|Enthält eine standardmäßige Richtlinie ***|Empfehlung ***|
|:-----|:-----|:-----|
|**E-Mail-Fluss** (Transportregeln)  <br/> |Nein  <br/> | Fügen Sie eine e-Mail-Flussregel zum Schutz gegen Ransomware hinzu. Finden Sie unter "Gewusst wie: Verwenden der Exchange-Transportregeln zum Nachverfolgen oder Blockieren von e-Mails mit Dateierweiterungen von Ransomware verwendet" in diesem Blogartikel: [Umgang mit Ransomware](https://blogs.technet.microsoft.com/office365security/how-to-deal-with-ransomware/).<br><br/> Erstellen einer Transportregel, um die automatische Weiterleitung von e-Mails an externe Domänen zu verhindern. Weitere Informationen finden Sie unter [Verursachten Client externe Weiterleiten von Regeln mit Score sichern](https://blogs.technet.microsoft.com/office365security/mitigating-client-external-forwarding-rules-with-secure-score/).<br/> <br>Weitere Informationen: [E-Mail-Fluss Regeln (Transportregeln) in Exchange Online](https://technet.microsoft.com/en-us/library/jj919238%28v=exchg.150%29.aspx) <br/> |
|**Aktivieren der modernen Authentifizierung** <br/> |Nein  <br/> | Moderne Authentifizierung in Office 365 ist eine Voraussetzung für die Verwendung von Multi-Factor Authentication (mehrstufiger Authentifizierung das). Mehrstufiger Authentifizierung das wird empfohlen, für den sicheren Zugriff auf die Cloudressourcen, einschließlich e-Mail.<br/>  <br>Finden Sie unter folgenden Themen:  <br/> • [Aktivieren oder Deaktivieren der modernen Authentifizierung in Exchange Online](https://support.office.com/article/58018196-f918-49cd-8238-56f57f38d662) <br/> • [Skype für Business Online: Aktivieren Ihres Mandanten für moderne Authentifizierung](https://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx) <br/>  <br>Moderne Authentifizierung ist für Office 2016 Clients, SharePoint Online und OneDrive für Unternehmen standardmäßig aktiviert.  <br/>  <br>Weitere Informationen: [mithilfe von Office 365 modernen Authentifizierung mit Office-Clients](https://support.office.com/article/776c0036-66fd-41cb-8928-5495c0f9168a) <br/> |
   
## <a name="configure-tenant-wide-sharing-policies-in-sharepoint-admin-center"></a>Konfigurieren von Mandanten geltende Freigaberichtlinien im SharePoint Administrationscenter

Microsoft-Empfehlungen zum Konfigurieren von SharePoint-Teamwebsites zur Erhöhung der Sicherheitsstufen, beginnend mit grundlegenden Schutz. Weitere Informationen finden Sie unter [Secure SharePoint Online-Websites und Dateien](https://docs.microsoft.com/microsoft-365-enterprise/secure-sharepoint-online-sites-and-files)
  
SharePoint-Teamwebsites, die auf der Ebene der Baseline konfiguriert zulassen Freigeben von Dateien mit externen Benutzern über anonymen Zugriff Links. Diese Methode wird empfohlen, anstelle von Dateien in e-Mail-Nachricht senden. 
  
Konfigurieren Sie zur Unterstützung der Ziele für geplante Protection Mandanten geltende Freigaberichtlinien wie hier empfohlen. Freigeben von Einstellungen für einzelne Websites kann restriktiver als diese Richtlinie Mandanten geltende, aber nicht mehr permissive sein. 
  
|Bereich ***|Enthält eine standardmäßige Richtlinie ***|Empfehlung ***|
|:-----|:-----|:-----|
|**Freigabe** (SharePoint Online und OneDrive für Unternehmen)  <br/> |Ja  <br/> | Externe Freigabe ist standardmäßig aktiviert. Diese Einstellungen werden empfohlen:<br/>  • Ermöglichen Freigabe an externe Benutzer authentifiziert und Verwenden von anonymen Zugriff Links (Standardeinstellung).  <br/>  • Anonymen Zugriff Links ablaufen in so viele Tage. Geben Sie eine Zahl bei Bedarf, beispielsweise 30 Tage.<br/>  • Link Standardtyp – wählen Sie intern (Personen in der Organisation nur). Benutzer, die von anonymen Links freigeben möchten, müssen diese Option Freigabe im Menü auswählen.<br/>  <br>Weitere Informationen: [Übersicht über die externe Freigabe](https://support.office.com/article/c8a462eb-0723-4b0b-8d0a-70feafe4be85) <br/> |
   
SharePoint Administrationscenter und OneDrive for Business-Verwaltungskonsole zählen die gleichen Einstellungen. Die Einstellungen im entweder Administrationscenter beziehen sich sowohl auf.
  
## <a name="configure-settings-in-azure-active-directory"></a>Konfigurieren von Einstellungen in Azure Active Directory

Achten Sie darauf, dass diese zwei Bereiche in Azure Active Directory für den Mandanten geltende Installationsvorgang für sicherere Umgebung finden Sie auf.
  
### <a name="configure-named-locations-under-conditional-access"></a>Konfigurieren von benannten Speicherorten (unter bedingten Zugriff)

Wenn Ihre Organisation Büros mit sicheren Netzwerkzugriff enthält, fügen die vertrauenswürdigen IP-Adressbereiche Azure Active Directory als benannte Speicherorte hinzu. Dieses Feature wird die Anzahl der gemeldeten falsch positive Ergebnisse für Risikoereignisse-Anmeldung verringert. 
  
Weitere Informationen: [benannte Speicherorten in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-named-locations)
  
### <a name="block-apps-that-dont-support-modern-authentication"></a>Apps blockieren, die moderne Authentifizierung nicht unterstützen

Mehrstufige Authentifizierung erfordert apps, die moderne-Authentifizierung unterstützen. Apps, die moderne Authentifizierung nicht unterstützen können nicht mithilfe von bedingten Zugriffsregeln blockiert werden.
  
Für sichere Umgebungen unbedingt Deaktivieren der Authentifizierung für apps, die moderne Authentifizierung nicht unterstützen. Sie können in Azure Active Directory ein Steuerelement dazu, die bald verfügbar ist.
  
Verwenden Sie eine der folgenden Methoden in der Zwischenzeit dazu für SharePoint Online und OneDrive für Unternehmen:
  
- Verwenden von PowerShell, finden Sie unter [apps blockieren, die moderne Authentifizierung nicht verwenden](https://docs.microsoft.com/intune-classic/deploy-use/block-apps-with-no-modern-authentication).
    
- Konfigurieren Sie dies im SharePoint Administrationscenter auf der "Gerät Datenzugriffsseite –"Steuern des Zugriffs von apps, die moderne Authentifizierung nicht verwenden." Wählen Sie Block. 
    
## <a name="get-started-with-cloud-app-security-or-office-365-cloud-app-security"></a>Erste Schritte mit der Cloud App-Sicherheit oder Office 365-Cloud-App-Sicherheit

Verwenden Sie Office 365-Cloud-App-Sicherheit für Risiko, für die Warnung auf verdächtige Aktivitäten ausgewertet werden soll und automatisch Maßnahmen ergreifen. Office 365 E5 Plan benötigt.
  
Oder verwenden Sie Microsoft Cloud App-Sicherheit um tieferen Einblick auch nach der Zugriff gewährt wird, umfassende Steuerelemente und verbesserten Schutz für alle Ihre Cloudanwendungen, einschließlich Office 365 zu erhalten. 
  
Da diese Lösung den Plan zur Abstimmung E5 empfiehlt, wird empfohlen, dass Sie mit der Cloud App-Sicherheit starten, damit Sie diese mit einer anderen Anwendung SaaS in Ihrer Umgebung verwenden können. Beginnen Sie mit Standardrichtlinien und Einstellungen.
  
Weitere Informationen:
  
- [Bereitstellen von Cloud App Security](https://docs.microsoft.com/cloud-app-security/getting-started-with-cloud-app-security)
    
- [Weitere Informationen zu Microsoft Cloud App Security](https://www.microsoft.com/en-us/cloud-platform/cloud-app-security)
    
- [Übersicht über Office 365 Cloud App Security](office-365-cas-overview.md)
    
![Cloud App Security-Dashboard](media/1fb2aa65-54b8-4746-9f5e-c187d339e9f5.png)
  
## <a name="additional-resources"></a>Zusätzliche Ressourcen

Diese Artikel und Leitfäden bieten zusätzliche ausführlichen Informationen für Ihre Office 365-Umgebung zu sichern:
  
- [Microsoft Security Guidance für politischen Kampagnen, gemeinnützige Organisationen, und andere agilen Organisationen](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-security-guidance) (Sie können diese Empfehlung in einer Umgebung vor allem nur-Cloud-Umgebungen verwenden) 
    
- [Empfohlene Sicherheitsrichtlinien und Konfigurationen für Identitäten und Geräte](https://docs.microsoft.com/microsoft-365-enterprise/microsoft-365-policies-configurations) (diese wird Folgendes Hilfe für AD FS-Umgebungen) 
    

