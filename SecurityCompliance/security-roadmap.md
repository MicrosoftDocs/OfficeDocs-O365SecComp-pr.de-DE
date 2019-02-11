---
title: Sicherheits-Roadmap für Office 365 - Top-Prioritäten für den ersten 30 Tagen 90 Tage und darüber hinaus
ms.author: bcarter
author: BrendaCarter
manager: laurawi
ms.date: 10/08/2018
ms.audience: Admin
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
ms.collection:
- Ent_O365
- Strat_O365_IP
search.appverid:
- MET150
ms.assetid: 28c86a1c-e4dd-4aad-a2a6-c768a21cb352
description: 'Obere Recommendations vom Microsoft Sicherheit im Internet-Team für die Implementierung von Sicherheitsfunktionen zum Schutz Ihrer Office 365-Umgebung. '
ms.openlocfilehash: 58767ea9a2b825d1583d9135f9d8edcb0d20d7c2
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "25450080"
---
# <a name="office-365-security-roadmap---top-priorities-for-the-first-30-days-90-days-and-beyond"></a>Sicherheits-Roadmap für Office 365 - Top-Prioritäten für den ersten 30 Tagen 90 Tage und darüber hinaus

Dieser Artikel enthält die oberen Empfehlung von Microsoft Sicherheit im Internet Team für die Implementierung von Sicherheitsfunktionen zum Schutz Ihrer Office 365-Umgebung. Dieser Artikel basiert auf einer Microsoft Ignite-Sitzung – [Secure Office 365 wie Sicherheit im Internet und pro: Top-Prioritäten für den ersten 30 Tagen 90 Tage und darüber hinaus](https://www.youtube.com/watch?v=luignzNyR-o). In dieser Sitzung wurde entwickelt und präsentiert von Mark Simos und Matt Kemelhar, Enterprise Sicherheit im Internet konstruiert.
  
Inhalt dieses Artikels:
  
- [Wegweiser für Ergebnisse](security-roadmap.md#Roadmap)
    
- [30 Tage – Leistungsstarke quick Wins](security-roadmap.md#Thirdaydays)
    
- [90 Tage – erweiterte Schutzebenen](security-roadmap.md#Ninetydays)
    
- [Über etwas hinaus](security-roadmap.md#Beyond)
    
## <a name="roadmap-outcomes"></a>Wegweiser für Ergebnisse
<a name="Roadmap"> </a>

Diese Roadmap Recommendations werden über drei Phasen in einer logischen Reihenfolge für die folgenden Ziele bereitgestellt.

|||
|:-----|:-----|
| |Ergebnisse
|30 Tage|Schnelle Konfiguration:  <br/> • Einfache Admin Schutzebenen  <br/> • Protokollierung und-Analyse  <br/> • Grundlegende Identität Schutzebenen  <br/> Mandantenkonfiguration  <br/>  Vorbereiten der beteiligten  <br/> |
|90 Tage|Erweiterte Schutz:  <br/> • Administratorkonten  <br/>  • Daten &amp; von Benutzerkonten  <br/>  Einblick in Compliance, Bedrohung und benutzeranforderungen  <br/>  Anpassen und Implementieren von Standardrichtlinien und Schutzebenen  <br/> |
|Über etwas hinaus|Passen Sie an und verfeinern Sie Hauptrichtlinien und Steuerelemente  <br/> Erweitern Sie lokale Abhängigkeiten Mauer  <br/> Integrieren Sie in Geschäfts- und sicherheitsanforderungen Prozesse (Legal, Bedrohung von innen usw.).  <br/> |
  

   
## <a name="30-days--powerful-quick-wins"></a>30 Tage – Leistungsstarke quick Wins
<a name="Thirdaydays"> </a>

Die folgenden Maßnahmen können schnell umgesetzt werden und führen lediglich zu geringen Beeinträchtigungen für die Benutzer.
  
|||
|:-----|:-----|
|Bereich  <br/> |Aufgaben  <br/> |
|Sicherheitsverwaltung  <br/> |• Secure Score überprüfen, und beachten Sie Ihr aktuelles Ergebnis ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Aktivieren überwachungsprotokollierung für Office 365. Finden Sie unter [Suchen Sie das Überwachungsprotokoll in die Office 365-Sicherheit &amp; Compliance Center](search-the-audit-log-in-security-and-compliance.md).<br/> • [Konfiguration Ihrer Office 365-Mandanten, um eine höhere Sicherheit](tenant-wide-setup-for-increased-security.md) .  <br/>  • Dashboards und Berichte im Office 365-Sicherheit und Compliance Center und Cloud App-Sicherheit regelmäßig überprüfen.  <br/> |
|Bedrohungsschutz  <br/> |[Verbinden von Office 365 zu Microsoft Cloud App-Sicherheit](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security) zu starten, verwenden die Bedrohung Erkennung Standardrichtlinien für abweichenden Verhaltensweisen monitoring. Erstellen Sie einen Basisplan für Normalbetriebswerte sieben Tage benötigt.<br><br/>  Schutz für Administratorkonten zu implementieren:  <br/> • Verwendung dedizierter Admin accounts für Admin-Aktivität fest.  <br/>  • Multi-Factor Authentication (mehrstufiger Authentifizierung das) für Administratorkonten zu erzwingen.  <br/>  • Verwenden Sie eine [hohe Sicherheit Windows 10 Gerät](https://docs.microsoft.com/windows-hardware/design/device-experiences/oem-highly-secure) für Admin-Aktivität fest.  <br/> |
|Identitäts- und Zugriffsverwaltung  <br/> |• [Azure Active Directory-Identitätsschutz aktivieren](https://docs.microsoft.com/azure/active-directory/active-directory-identityprotection-enable).  <br/> • Identitätsverbund Umgebungen Erzwingen der Konto-Sicherheit (Kennwortlänge, Alter, Komplexität usw.).  <br/> |
|Schutz von Daten
  <br/> | Überprüfen Sie Beispiel Informationen Protection Recommendations. Schutz für Ihre Informationen erfordert Koordination in Ihrer Organisation. Erste Schritte mit den folgenden Ressourcen:<br/> • [Office 365 Information Protection für GDPR](http://aka.ms/o365gdpr) <br/> • [Secure SharePoint Online-Websites und Dateien](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) (einschließlich der Freigabe, Klassifizierung, Verhinderung von Datenverlust und Azure Information Protection)  <br/> |
   
## <a name="90-days--enhanced-protections"></a>90 Tage – erweiterte Schutzebenen
<a name="Ninetydays"> </a>

Die folgenden Maßnahmen erfordern etwas mehr Zeit für Planung und Implementierung, stärken die Sicherheit Ihres Unternehmens jedoch erheblich. 
  
|||
|:-----|:-----|
|Bereich  <br/> |Aufgabe  <br/> |
|Sicherheitsverwaltung  <br/> | • Secure Score empfohlenen Aktionen für Ihre Umgebung überprüfen ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Weiterhin Dashboards und Berichte in der Office 365-Sicherheit und Compliance Center, Cloud App-Sicherheit und Tools SIEM regelmäßig zu überprüfen.  <br/>  • Gesucht und Implementieren von Softwareupdates.  <br/>  • Leiten Angriff Simulationen für Spear Phishing, Kennwort Sprühende und Password Brute-Force-Angriffe mit [Angriff Simulator](https://support.office.com/article/attack-simulator-office-365-da5845db-c578-4a41-b2cb-5a09689a551b) (im Lieferumfang von [Office 365 Bedrohungsanalyse](office-365-ti.md)enthalten).  <br/>  • Erscheinungsbild für die Freigabe Risiko durch die Überprüfung der integrierte Berichte in der Cloud App-Sicherheit (auf der Registerkarte überprüfen).  <br/>  • Überprüfen [Compliance Manager](meet-data-protection-and-regulatory-reqs-using-microsoft-cloud.md) Status für Vorschriften zu überprüfen, die für Ihre Organisation (beispielsweise GDPR, NIST 800 171) gelten.  <br/> |
|Bedrohungsschutz  <br/> | Erweiterter Schutz für Administratorkonten zu implementieren:  <br/>  • Konfigurieren [Privilegierten Zugriff Arbeitsstationen](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/privileged-access-workstations) (Pfoten) für Admin-Aktivität fest.  <br/>  • Konfigurieren der [Identitätsverwaltung Azure AD-Berechtigungen](https://docs.microsoft.com/azure/active-directory/active-directory-privileged-identity-management-configure).  <br/>  • Konfigurieren einer Sicherheit und Ereignissen (SIEM) Verwaltungstool Erfassen von Protokollierungsdaten aus Office 365, Cloud App-Sicherheit und andere Dienste, einschließlich AD FS. Das Office 365-Überwachungsprotokoll werden Daten nur 90 Tage lang gespeichert. Erfassen diese Daten im SIEM-Tool können Sie zum Speichern von Daten für einen längeren Zeitraum.<br/> |
|Identitäts- und Zugriffsverwaltung  <br/> | • Bei aktivierter mehrstufiger Authentifizierung das für alle Benutzer zu erzwingen.  <br/>  • Implementieren Sie eine Reihe von [bedingten Zugriff und verwandten Richtlinien](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations). |
|Schutz von Daten
  <br/> | Anpassen und Protection Informationsrichtlinien implementieren. Diese Ressourcen enthalten Beispiele:<br/> • [Office 365 Information Protection für GDPR](http://aka.ms/o365gdpr) <br/> • [Secure SharePoint Online-Websites und Dateien](https://docs.microsoft.com/Office365/enterprise/secure-sharepoint-online-sites-and-files) <br/> <br> Verwenden Sie Richtlinien zur Verhinderung von Datenverlust und Überwachungstools in Office 365 für Daten, die in Office 365 (anstatt Cloud App-Sicherheit) gespeichert. <br><br>Verwenden Sie Cloud App-Sicherheit mit Office 365, um die erweiterten Funktionen (außer Verhinderung von Datenverlust) Warnungen.  <br/> |
   
## <a name="beyond"></a>Über etwas hinaus
<a name="Beyond"> </a>

Dies sind wichtige Sicherheitsmaßnahmen, die auf vorherigen Arbeit zu erstellen. 
  
|||
|:-----|:-----|
|Bereich  <br/> |Aufgabe  <br/> |
|Sicherheitsverwaltung  <br/> |• Die Planung von nächsten Aktionen mithilfe von Secure Score fortsetzen möchten ( [https://securescore.office.com](https://securescore.office.com)).  <br/>  • Weiterhin Dashboards und Berichte in der Office 365-Sicherheit und Compliance Center, Cloud App-Sicherheit und Tools SIEM regelmäßig zu überprüfen.  <br/>  • Weiterhin gesucht und Implementieren von Softwareupdates.  <br/>  • Integration von eDiscovery in Ihrer Legal und Bedrohung Antwort Prozesse.  <br/> |
|Bedrohungsschutz  <br/> | • Implementieren [Systemzugriff Secure](https://docs.microsoft.com/windows-server/identity/securing-privileged-access/securing-privileged-access) (SPA) für Identity-Komponenten (AD, AD FS) lokal.  <br/>  • Verwendung Cloud App-Sicherheit zum Überwachen von Insider Bedrohungen.  <br/>  • Ermittlung der Schatten IT SaaS Verwendung mithilfe von Cloud-App-Sicherheit.  <br/> |
|Identitäts- und Zugriffsverwaltung  <br/> | • Verfeinern Information Protection Richtlinien:  <br/>  • Azure Information Protection und Office 365 Verhinderung von Datenverlust (DLP).  <br/>  • Cloud App-Sicherheitsrichtlinien und Benachrichtigungen.  <br/> |
|Schutz von Daten
  <br/> | • Verfeinern Richtlinien und betriebliche Prozesse.  <br/>  • Verwenden Sie zum Identifizieren der Bedrohungen Insider Azure AD-Schutz.  <br/> |
   
Siehe auch: [wie Sie eine schnelle Cyber wie Petya und WannaCrypt zu verringern](https://cloudblogs.microsoft.com/microsoftsecure/2018/02/21/how-to-mitigate-rapid-cyberattacks-such-as-petya-and-wannacrypt/). 
  

