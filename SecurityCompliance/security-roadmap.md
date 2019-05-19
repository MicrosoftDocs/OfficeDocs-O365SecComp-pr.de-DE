---
title: Office 365 Security Roadmap – die wichtigsten Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/08/2018
audience: Admin
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
description: 'Die wichtigsten Empfehlungen aus dem Cyber-Team von Microsoft für die Implementierung von Sicherheitsfunktionen zum Schutz Ihrer Office 365 Umgebung. '
ms.openlocfilehash: 12aa5833757901ba78a0716480cb34b5b60675a5
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34157637"
---
# <a name="office-365-security-roadmap---top-priorities-for-the-first-30-days-90-days-and-beyond"></a>Office 365 Security Roadmap – die wichtigsten Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus

Dieser Artikel enthält die wichtigsten Empfehlungen des Cyber-Teams von Microsoft für die Implementierung von Sicherheitsfunktionen zum Schutz Ihrer Office 365 Umgebung. Dieser Artikel wird von einer Microsoft Ignite-Sitzung angepasst – [sichere Office 365 wie ein Cyber pro: die wichtigsten Prioritäten für die ersten 30 Tage, 90 Tage und darüber hinaus](https://www.youtube.com/watch?v=luignzNyR-o). Diese Sitzung wurde von Mark Simos und Matt Kemelhar, Enterprise Cyber Architects, entwickelt und präsentiert.
  
Inhalt dieses Artikels:
  
- [Roadmap-Ergebnisse](security-roadmap.md#Roadmap)
    
- [30 Tage – leistungsstarke schnell Gewinne](security-roadmap.md#Thirdaydays)
    
- [90 Tage – erweiterter Schutz](security-roadmap.md#Ninetydays)
    
- [Über](security-roadmap.md#Beyond)
    
## <a name="roadmap-outcomes"></a>Roadmap-Ergebnisse
<a name="Roadmap"> </a>

Diese Empfehlungen für die Roadmap werden in einer logischen Reihenfolge in drei Phasen mit den folgenden Zielen bereitgestellt.

|||
|:-----|:-----|
| |Ergebnisse
|30 Tage|Schnelle Konfiguration:  <br/> • Grundlegender Administrator Schutz  <br/> • Protokollierung und Analyse  <br/> • Grundlegende Identitätsschutz  <br/> Mandanten Konfiguration  <br/>  Vorbereiten von Beteiligten  <br/> |
|90 Tage|Erweiterte Schutzfunktionen:  <br/> • Administratorkonten  <br/>  • Daten &amp; Benutzerkonten  <br/>  Sichtbarkeit in Compliance, Bedrohung und Benutzeranforderungen  <br/>  Anpassen und Implementieren von Standardrichtlinien und-Schutz  <br/> |
|Über|Anpassen und verfeinern wichtiger Richtlinien und Steuerelemente  <br/> Erweitern von Schutzeinrichtungen zu lokalen Abhängigkeiten  <br/> Integration in Geschäfts-und Sicherheitsprozesse (rechtliche, Insider-Bedrohungen usw.)  <br/> |
  

   
## <a name="30-days--powerful-quick-wins"></a>30 Tage – leistungsstarke schnell Gewinne
<a name="Thirdaydays"> </a>

Die folgenden Maßnahmen können schnell umgesetzt werden und führen lediglich zu geringen Beeinträchtigungen für die Benutzer.
  
|||
|:-----|:-----|
|Bereich  <br/> |Aufgaben  <br/> |
|Sicherheitsverwaltung  <br/> |• Prüfen Sie Secure Score, und notieren Sie sich [https://securescore.office.com](https://securescore.office.com)Ihre aktuelle Punktzahl ().  <br/>  • Aktivieren Sie die Überwachungsprotokollierung für Office 365. Weitere Informationen finden Sie unter [Durchsuchen des Überwachungsprotokolls](search-the-audit-log-in-security-and-compliance.md).  <br/> • [Konfigurieren Sie Ihren Office 365 Mandanten für mehr Sicherheit](tenant-wide-setup-for-increased-security.md) .  <br/>  • Regelmäßige Überprüfung von Dashboards und Berichten im Microsoft 365 Security Center und in der Cloud-App-Sicherheit.  <br/> |
|Bedrohungsschutz  <br/> |[Verbinden Sie Office 365 mit der Microsoft Cloud-App-Sicherheit](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) , um die Überwachung mithilfe der standardmäßigen Bedrohungs Erkennungsrichtlinien für anomale Verhaltensweisen zu starten. Es dauert sieben Tage, um einen Basisplan für die Anomalie-Erkennung zu erstellen.  <br><br/>  Implementieren des Schutzes für Administratorkonten:  <br/> • Verwenden Sie dedizierte Administratorkonten für Administratoraktivitäten.  <br/>  • Mehrstufige Authentifizierung (MFA) für Administratorkonten erzwingen.  <br/>  • Verwenden Sie ein [hochsicheres Windows 10-Gerät](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) für Administratoraktivitäten.  <br/> |
|Identitäts- und Zugriffsverwaltung  <br/> |• [Azure Active Directory Identity Protection aktivieren](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).  <br/> • Für Verbund Identitäts Umgebungen erzwingen Sie die Kontosicherheit (Kennwortlänge, Alter, Komplexität usw.).  <br/> |
|Schutz von Daten  <br/> | Lesen Sie die Empfehlungen zum Beispiel für Informationsschutz. Informationsschutz erfordert eine Koordination in Ihrer Organisation. Finden Sie den Einstieg mit den folgenden Ressourcen:  <br/> • [Office 365 Informationsschutz für dsgvo](http://aka.ms/o365gdpr) <br/> • [Sichere SharePoint Online Websites und Dateien](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (einschließlich Freigabe, Klassifizierung, Verhinderung von Datenverlust und Azure Information Protection)  <br/> |
   
## <a name="90-days--enhanced-protections"></a>90 Tage – erweiterter Schutz
<a name="Ninetydays"> </a>

Die folgenden Maßnahmen erfordern etwas mehr Zeit für Planung und Implementierung, stärken die Sicherheit Ihres Unternehmens jedoch erheblich. 
  
|||
|:-----|:-----|
|Bereich  <br/> |Vorgang  <br/> |
|Sicherheitsverwaltung  <br/> | • Check Secure Score für empfohlene Aktionen für Ihre Umgebung ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Weiterhin regelmäßige Überprüfung von Dashboards und Berichten im Microsoft 365 Security Center, in der Cloud-App-Sicherheit und in Siem-Tools.  <br/>  • Suchen und Implementieren von Softwareupdates  <br/>  • Durchführung von Angriffssimulationen für Spear-Phishing-, Password-Spray-und Brute-Force-Kennwortangriffe mithilfe von [Attack Simulator](https://support.office.com/article/attack-simulator-office-365-da5845db-c578-4a41-b2cb-5a09689a551b) (im Lieferumfang von [Office 365 Threat Intelligence](office-365-ti.md)enthalten).  <br/>  • Suchen Sie nach Freigabe Risiken, indem Sie die integrierten Berichte in der Cloud-App-Sicherheit (auf der Registerkarte untersuchen) überprüfen.  <br/>  • Überprüfen Sie den Status von [Compliance-Manager](meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md) auf Vorschriften, die für Ihre Organisation gelten (beispielsweise dsgvo, NIST 800-171).  <br/> |
|Bedrohungsschutz  <br/> | Implementieren Sie erweiterte Schutzbestimmungen für Administratorkonten:  <br/>  • Konfigurieren von [rechten Zugriffs](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) Arbeitsstationen (PAWs) für Administratoraktivitäten.  <br/>  • Konfigurieren [Azure AD privilegierten Identitätsverwaltung](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).  <br/>  • Konfigurieren Sie ein Siem-Tool (Security Information and Event Management) zum Erfassen von Protokollierungsdaten aus Office 365, Cloud-App-Sicherheit und anderen Diensten, einschließlich AD FS. Im Office 365 Überwachungsprotokoll werden Daten für nur 90 Tage gespeichert. Durch das Erfassen dieser Daten im Siem-Tool können Sie Daten für einen längeren Zeitraum speichern.  <br/> |
|Identitäts- und Zugriffsverwaltung  <br/> | • Aktivieren und Erzwingen von MFA für alle Benutzer.  <br/>  • Implementieren Sie eine Reihe von [bedingten Zugriff und zugehöriger Richtlinien](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations). |
|Schutz von Daten  <br/> | Anpassen und Implementieren von Richtlinien für den Informationsschutz Diese Ressourcen umfassen Beispiele:  <br/> • [Office 365 Informationsschutz für dsgvo](http://aka.ms/o365gdpr) <br/> • [Sichere SharePoint Online Websites und Dateien](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) <br/> <br> Verwenden von Richtlinien zur Verhinderung von Datenverlust und Überwachungstools in Office 365 für in Office 365 gespeicherte Daten (anstelle von Cloud-App-Sicherheit) <br><br>Verwenden Sie die Cloud-App-Sicherheit mit Office 365 für erweiterte Warnungsfunktionen (außer Verhinderung von Datenverlust).  <br/> |
   
## <a name="beyond"></a>Über
<a name="Beyond"> </a>

Dies sind wichtige Sicherheitsmaßnahmen, die auf früheren Arbeiten aufbauen. 
  
|||
|:-----|:-----|
|Bereich  <br/> |Vorgang  <br/> |
|Sicherheitsverwaltung  <br/> |• Weiter Planung der nächsten Aktionen mit Secure Score ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Weiterhin regelmäßige Überprüfung von Dashboards und Berichten im Microsoft 365 Security Center, in der Cloud-App-Sicherheit und in Siem-Tools.  <br/>  • Weiter suchen und Implementieren von Softwareupdates.  <br/>  • Integration von eDiscovery in ihre rechtlichen und Bedrohungs Reaktionsprozesse.  <br/> |
|Bedrohungsschutz  <br/> | • Implementierung von [Secure privileged Access](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) (Spa) für Identitäts Komponenten lokal (AD, AD FS).  <br/>  • Verwenden Sie die Cloud-App-Sicherheit, um Insiderbedrohungen zu überwachen.  <br/>  • Entdecken Sie Shadow IT Saas-Nutzung mithilfe der Cloud-App-Sicherheit.  <br/> |
|Identitäts- und Zugriffsverwaltung  <br/> | • Optimieren von Richtlinien und Betriebsprozessen  <br/>  • Verwenden Sie Azure AD Identitätsschutz, um Insider-Bedrohungen zu identifizieren.  |
|Schutz von Daten  <br/> | Verfeinern von Richtlinien für den Informationsschutz:  <br/>  • Microsoft 365 und Office 365 Vertraulichkeits Bezeichnungen und Datenverlust Verhinderung (DLP) oder Azure Information Protection.  <br/>  • Sicherheitsrichtlinien und Warnungen in der Cloud-app.  <br/> |
   
Siehe auch: [Vorgehensweise zum minimieren schneller Cyberangriffe wie Petja und WannaCrypt](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/). 
  

