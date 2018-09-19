---
title: Zugriffsschutz für Daten und Dienste in Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Zielseite zum Schutz des Zugriffs auf Office 365-Daten und-Dienste
ms.openlocfilehash: 652a14c5f1f29187aeac51355e7a924c9378806f
ms.sourcegitcommit: 15dfa0c83aa88816c18e30a44a49e36e733d952c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/19/2018
ms.locfileid: "24011277"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a>Zugriffsschutz für Daten und Dienste in Office 365

Schutz des Zugriffs auf Ihre Office 365-Daten und-Dienste ist entscheidend für die Verteidigung gegen im Internet-Angriffen und zum Schutz vor Datenverlust. Die gleichen Schutzmechanismen in andere Anwendungen SaaS in Ihrer Umgebung angewendet werden können und auch für lokale-Clientanwendungen veröffentlicht mit Azure Active Directory-Anwendungsproxy.
  
## <a name="step-1-review-recommendations"></a>Schritt 1: Sich über Empfehlungen

Empfohlene Funktionen zum Schutz von Identitäten und Geräten, die auf Office 365, andere SaaS-Dienste und lokale Anwendungen zugreifen, die mit dem Azure AD-Anwendungsproxy veröffentlicht werden.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Weitere Sprachen](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>Schritt 2: Konfigurieren von mehrstufiger Authentifizierung das

Verwenden Sie diese Ressourcen zum orientieren sich selbst zu mehrstufiger Authentifizierung das Sie entscheiden, welche Version für Sie geeignet ist, und klicken Sie dann planen Sie, und Bereitstellen Sie mehrstufiger Authentifizierung das für Ihre Umgebung.
  
- [Was ist Azure Multi-Factor Authentication?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Wählen Sie die Azure Multi-Factor Authentication-Lösung für Sie](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Gewusst wie: Abrufen von Azure Multi-Factor authentication](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Plan für die mehrstufige Authentifizierung für Office 365-Bereitstellungen](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Einrichten der mehrstufigen Authentifizierung für Office 365-Benutzer](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [Planen Sie, wo mehrstufiger Authentifizierung das, Cloud oder lokale Bereitstellung](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Konfigurieren von Einstellungen für Azure Multi-Factor authentication](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>Schritt 3: Erzwingen Sie mehrstufiger Authentifizierung das mit bedingten Zugriffsregeln Azure AD

Bei Verwendung von Azure AD mehrstufiger Authentifizierung das Erstellen einer Regel zur bedingten Access mehrstufiger Authentifizierung das für den Zugriff auf Office 365 und anderen SaaS-apps in Ihrer Umgebung erforderlich, um.
  
- [Bedingte Zugriff in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a>Schritt 4: Konfigurieren der Verwaltung von Systemzugriff

Access privilegierten Management ermöglicht die Differenzierte Sicherung Access Steuerung privilegierten Administratoraufgaben in Office 365.  Es kann Schützen Ihrer Organisation aus Verstöße, die vorhandenen privilegierten Administratorkonten stehende Zugriff auf vertrauliche Daten oder Zugriff auf wichtige Konfigurationseinstellungen verwenden können.

- [Übersicht über die Berechtigungen Management zugreifen](privileged-access-management-overview.md)
- [Konfigurieren der Verwaltung von Systemzugriff](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a>Schritt 5: Konfigurieren Sie Richtlinien für SharePoint-Gerät

Gerät Zugriffsrichtlinien für SharePoint Online und OneDrive für Unternehmen werden empfohlen, für den Schutz von vertraulicher, geheime und regulierten Daten. In Kürze ist die Möglichkeit, Geräte Zugriffsrichtlinien einzelne Teamwebsites zuzuweisenden.
  
- [Steuern des Zugriffs von nicht verwalteten Geräten](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a>Schritt 6: Konfigurieren der app und den Datenschutz für Geräte

Sie können Anwendungen auf mobilen Geräten, unabhängig davon, ob die Geräte, für die Verwaltung von mobilen Geräten registriert sind verwalten. Dies schützt vor versehentlichen Datenlecks von Daten in Office 365, einschließlich e-Mail-Nachrichten und Dateien.
  
- Für iOS und Android: [Protect app-Daten mithilfe von Richtlinien für die app Schutz mit Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
Konfigurieren Sie für Windows-10 Windows Informationen Schutz (WIP), um versehentliche Datenlecks zu verhindern.
  
- Für verwaltete Geräte: [Erstellen einer Windows Informationen Schutz (WIP) mit Registrierungsrichtlinien mithilfe des Azure Portals für Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- Für nicht-verwalteten Geräten: [Erstellen und Bereitstellen von Windows Informationen Schutz (WIP) app Protection Richtlinie mit Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-7-manage-devices-with-intune"></a>Schritt 7: Verwalten von Geräten mit Intune

Verwalten von Geräten können Sie sicherstellen, dass sie fehlerfrei und kompatibel sind, bevor sie Zugriff auf Ressourcen in Ihrer Umgebung. Gerät basierend bedingten Regeln können Sie sicherstellen, dass Angreifer keinen Zugriff auf Ihre Ressourcen von nicht verwalteten Geräten erhalten Zugriff.
  
- [Geräte für die Verwaltung in Intune registrieren](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>Schritt 8: Konfigurieren Sie zusätzliche Intune Richtlinien und bedingte Zugriffsregeln für Ihre Umgebung

Verwenden Sie diese als Ausgangspunkt für unternehmensweite oder Sicherheitsszenarien anspruchsvolle Access Konfigurationen empfohlen.
  
- [Sichere e-Mail-Richtlinien und-Konfigurationen](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

