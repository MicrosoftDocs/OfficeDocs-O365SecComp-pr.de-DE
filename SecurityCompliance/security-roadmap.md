---
title: Office 365 Security Roadmap – die wichtigsten Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/08/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
- M365-security-compliance
search.appverid:
- MET150
ms.assetid: 28c86a1c-e4dd-4aad-a2a6-c768a21cb352
description: 'Die wichtigsten Empfehlungen des Microsoft-Cyber-Teams für die Implementierung von Sicherheitsfunktionen zum Schutz Ihrer Office 365-Umgebung. '
ms.openlocfilehash: feb11c90272fc639aacb0a49cc3272627df18af6
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30220805"
---
# <a name="office-365-security-roadmap---top-priorities-for-the-first-30-days-90-days-and-beyond"></a>Office 365 Security Roadmap – die wichtigsten Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus

Dieser Artikel enthält die wichtigsten Empfehlungen des Microsoft-Cyber-Teams für die Implementierung von Sicherheitsfunktionen zum Schutz Ihrer Office 365-Umgebung. Dieser Artikel wurde von einer Microsoft Ignite-Sitzung angepasst – [Secure Office 365 wie ein Cyber pro: die wichtigsten Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus](https://www.youtube.com/watch?v=luignzNyR-o). Diese Sitzung wurde von Mark Simos und Matt Kemelhar, Enterprise Cyber Architects, entwickelt und präsentiert.
  
Inhalt dieses Artikels:
  
- [Roadmap-Ergebnisse](security-roadmap.md#Roadmap)
    
- [30 Tage – leistungsstarke schnell Gewinne](security-roadmap.md#Thirdaydays)
    
- [90 Tage – erweiterter Schutz](security-roadmap.md#Ninetydays)
    
- [Über](security-roadmap.md#Beyond)
    
## <a name="roadmap-outcomes"></a>Roadmap-Ergebnisse
<a name="Roadmap"> </a>

Diese Roadmap-Empfehlungen werden in drei Phasen in einer logischen Reihenfolge mit den folgenden Zielen durchlaufen.

|||
|:-----|:-----|
| |Ergebnisse
|30 Tage|Schnelle Konfiguration:  <br/> • Grundlegende Administrator Schutzfunktionen  <br/> • Protokollierung und Analyse  <br/> • Grundlegende Identitätsschutz  <br/> Mandanten Konfiguration  <br/>  Vorbereiten von Beteiligten  <br/> |
|90 Tage|Erweiterte Schutzfunktionen:  <br/> • Administratorkonten  <br/>  • Daten &amp; Benutzerkonten  <br/>  Transparenz bei Compliance-, Bedrohungs-und Benutzeranforderungen  <br/>  Anpassen und Implementieren von Standardrichtlinien und-Schutz  <br/> |
|Über|Anpassen und verfeinern wichtiger Richtlinien und Steuerelemente  <br/> Erweitern von Schutzmaßnahmen auf lokale Abhängigkeiten  <br/> Integration in Geschäfts-und Sicherheitsprozesse (rechtliches, Insider Risiko usw.)  <br/> |
  

   
## <a name="30-days--powerful-quick-wins"></a>30 Tage – leistungsstarke schnell Gewinne
<a name="Thirdaydays"> </a>

Die folgenden Maßnahmen können schnell umgesetzt werden und führen lediglich zu geringen Beeinträchtigungen für die Benutzer.
  
|||
|:-----|:-----|
|Bereich  <br/> |Tasks  <br/> |
|Sicherheitsverwaltung  <br/> |• Überprüfen Sie die sichere Bewertung, und notieren [https://securescore.office.com](https://securescore.office.com)Sie sich Ihre aktuelle Bewertung ().  <br/>  • Aktivieren Sie die Überwachungsprotokollierung für Office 365. Weitere Informationen finden Sie unter [Durchsuchen des Überwachungsprotokolls &amp; im Office 365 Security Compliance Center](search-the-audit-log-in-security-and-compliance.md).<br/> • [Konfigurieren Sie Ihren Office 365-Mandanten für mehr Sicherheit](tenant-wide-setup-for-increased-security.md) .  <br/>  • Regelmäßiges Überarbeiten von Dashboards und Berichten im Office 365 Security and Compliance Center und Cloud App Security.  <br/> |
|Bedrohungsschutz  <br/> |[Verbinden Sie Office 365 mit Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) , um die Überwachung mithilfe der standardmäßigen Bedrohungs Erkennungsrichtlinien für anomale Verhaltensweisen zu starten. Es dauert sieben Tage, um eine Baseline für die Anomalie-Erkennung zu erstellen.<br><br/>  Implementieren des Schutzes für Administratorkonten:  <br/> • Verwenden von dedizierten Administratorkonten für Administratoraktivitäten.  <br/>  • Erzwingen der mehrstufigen Authentifizierung (Multi-Factor Authentication, MFA) für Administratorkonten.  <br/>  • Verwenden Sie ein [hochsicheres Windows 10-Gerät](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) für Administratoraktivitäten.  <br/> |
|Identitäts- und Zugriffsverwaltung  <br/> |• [Azure Active Directory-Identitätsschutz aktivieren](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).  <br/> • Für Verbund Identitäts Umgebungen erzwingen Sie Kontosicherheit (Kennwortlänge, Alter, Komplexität usw.).  <br/> |
|Schutz von Daten
  <br/> | Lesen Sie die Beispiel Empfehlungen zum Informationsschutz. Der Informationsschutz erfordert eine koordinierte Organisation. Erste Schritte mit den folgenden Ressourcen:<br/> • [Office 365 Information Protection für dsgvo](http://aka.ms/o365gdpr) <br/> • [Sichere SharePoint Online-Websites und-Dateien](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (einschließlich Freigabe, Klassifizierung, Verhinderung von Datenverlust und Azure Information Protection)  <br/> |
   
## <a name="90-days--enhanced-protections"></a>90 Tage – erweiterter Schutz
<a name="Ninetydays"> </a>

Die folgenden Maßnahmen erfordern etwas mehr Zeit für Planung und Implementierung, stärken die Sicherheit Ihres Unternehmens jedoch erheblich. 
  
|||
|:-----|:-----|
|Bereich  <br/> |Aufgabe  <br/> |
|Sicherheitsverwaltung  <br/> | • Überprüfen der sicheren Bewertung für empfohlene Aktionen für Ihre [https://securescore.office.com](https://securescore.office.com)Umgebung ().  <br/>  • Regelmäßiges Überarbeiten von Dashboards und Berichten im Office 365 Security and Compliance Center, Cloud App Security und SIEM Tools.  <br/>  • Suchen und Implementieren von Softwareupdates.  <br/>  • Durchführen von Angriffssimulationen für Spear-Phishing, Kenn Wort Spray und Brute-Force [](https://support.office.com/article/attack-simulator-office-365-da5845db-c578-4a41-b2cb-5a09689a551b) -Kennwortangriffe mithilfe des anGriffs Simulators (im Lieferumfang von [Office 365 Threat Intelligence](office-365-ti.md)).  <br/>  • Suchen Sie nach Freigabe Risiko, indem Sie die integrierten Berichte in Cloud App Security (auf der Registerkarte untersuchen) überprüfen.  <br/>  • Überprüfen Sie [Compliance Manager](meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md) , um den Status der Vorschriften zu überprüfen, die für Ihre Organisation gelten (wie DSGVO, NIST 800-171).  <br/> |
|Bedrohungsschutz  <br/> | Implementieren erweiterter Schutz für Administratorkonten:  <br/>  • Konfigurieren von [privilegierten Zugriffs](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) Arbeitsstationen (Pfoten) für Administratoraktivitäten.  <br/>  • Konfigurieren von [Azure AD privilegEd Identity Management](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).  <br/>  • Konfigurieren eines Tools für Security Information and Event Management (SIEM) zum Erfassen von Protokollierungsdaten aus Office 365, Cloud-App-Sicherheit und anderen Diensten, einschließlich AD FS. Das Office 365-Überwachungsprotokoll speichert Daten nur für 90 Tage. Durch das Erfassen dieser Daten in SIEM-Tool können Sie Daten über einen längeren Zeitraum speichern.<br/> |
|Identitäts- und Zugriffsverwaltung  <br/> | • Aktivieren und Erzwingen von MFA für alle Benutzer.  <br/>  • Implementieren Sie eine Reihe von [bedingten Zugriffs-und zugehörigen Richtlinien](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations). |
|Schutz von Daten
  <br/> | Anpassen und Implementieren von Informationsschutz Richtlinien. Diese Ressourcen sind Beispiele:<br/> • [Office 365 Information Protection für dsgvo](http://aka.ms/o365gdpr) <br/> • [Sichere SharePoint Online-Websites und-Dateien](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) <br/> <br> Verwenden Sie Richtlinien zur Verhinderung von Datenverlust und Überwachungstools in Office 365 für in Office 365 (anstelle von Cloud App Security) gespeicherte Daten. <br><br>Verwenden von Cloud-App-Sicherheit mit Office 365 für erweiterte Warnungsfunktionen (außer Verhinderung von Datenverlust).  <br/> |
   
## <a name="beyond"></a>Über
<a name="Beyond"> </a>

Dies sind wichtige Sicherheitsmaßnahmen, die auf früheren Arbeiten aufbauen. 
  
|||
|:-----|:-----|
|Bereich  <br/> |Aufgabe  <br/> |
|Sicherheitsverwaltung  <br/> |• Weiter Planen der nächsten Aktionen mit Secure Score ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Regelmäßiges Überarbeiten von Dashboards und Berichten im Office 365 Security and Compliance Center, Cloud App Security und SIEM Tools.  <br/>  • Suchen und Implementieren von Softwareupdates.  <br/>  • Integrieren Sie eDiscovery in ihre Rechts-und Bedrohungs-Reaktionsprozesse.  <br/> |
|Bedrohungsschutz  <br/> | • Implementierung des [Secure privilegEd Access](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) (Spa) für Identitäts Komponenten (AD, AD FS).  <br/>  • Verwenden der Cloud-App-Sicherheit zum Überwachen von Insiderbedrohungen.  <br/>  • Discover Shadow IT SaaS-Nutzung mithilfe von Cloud App Security.  <br/> |
|Identitäts- und Zugriffsverwaltung  <br/> | • Datenschutzrichtlinien verfeinern:  <br/>  • Azure Information Protection und Office 365 Data Loss Prevention (DLP).  <br/>  • Sicherheitsrichtlinien und Warnungen zur Cloud-app.  <br/> |
|Schutz von Daten
  <br/> | • Verfeinern von Richtlinien und Betriebsprozessen  <br/>  • Verwenden Sie Azure AD Identity Protection, um Insider-Bedrohungen zu identifizieren.  <br/> |
   
Siehe auch: [Vorgehensweise zum Verringern von schnellen Cyberattacken wie Petja und WannaCrypt](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/). 
  

