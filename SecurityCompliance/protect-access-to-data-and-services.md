---
title: Zugriffsschutz für Daten und Dienste in Office 365
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 4/17/2018
ms.audience: Admin
ms.topic: hub-page
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a6ef28a4-2447-4b43-aae2-f5af6d53c68e
description: Zielseite zum Schutz des Zugriffs auf O365-Daten und-Dienste
ms.openlocfilehash: 95933c5a7bc95f9fd70e8f3470055b57193971d4
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213535"
---
# <a name="protect-access-to-data-and-services-in-office-365"></a>Zugriffsschutz für Daten und Dienste in Office 365

Der Schutz des Zugriffs auf Ihre Office 365-Daten und-Dienste ist entscheidend für die Abwehr von Cyber-Angriffen und Schutz vor Datenverlust. Der gleiche Schutz kann auf andere SaaS-Anwendungen in Ihrer Umgebung und sogar auf lokale Anwendungen angewendet werden, die mit Azure Active Directory-Anwendungs Proxy veröffentlicht werden.
  
## <a name="step-1-review-recommendations"></a>Schritt 1: Überprüfungen von Empfehlungen

Empfohlene Funktionen zum Schutz von Identitäten und Geräten, die auf Office 365, andere SaaS-Dienste und lokale Anwendungen zugreifen, die mit dem Azure AD-Anwendungsproxy veröffentlicht werden.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Weitere Sprachen](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-configure-mfa"></a>Schritt 2: Konfigurieren von MFA

Verwenden Sie diese Ressourcen, um sich an MFA zu orientieren, zu entscheiden, welche Version für Sie geeignet ist, und dann MFA für Ihre Umgebung zu planen und bereitzustellen.
  
- [Was ist Azure Multi-Factor Authentication?](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [Wählen Sie die Azure Multi-Factor Authentication Solution für Sie aus.](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [So erhalten Sie die Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [Planen der mehrstufigen Authentifizierung für Office 365-Bereitstellungen](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [Einrichten der mehrstufigen Authentifizierung für Office 365-Benutzer](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [Planen der Bereitstellung von MFA, Cloud oder lokal](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [Konfigurieren von Azure-Einstellungen für mehrstufige Authentifizierung](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a>Schritt 3: Erzwingen von MFA mit Azure AD Conditional Access Rules

Wenn Sie Azure AD MFA verwenden, erstellen Sie eine Regel für bedingten Zugriff für den Zugriff auf Office 365 und andere SaaS-apps in Ihrer Umgebung.
  
- [Bedingter Zugriff in Azure Active Directory](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a>Schritt 4: Konfigurieren von privileged Access Management

Privileged Access Management ermöglicht eine granulare Zugriffssteuerung über privilegierte Verwaltungsaufgaben in Office 365.  Es kann dazu beitragen, Ihre Organisation vor Verstößen zu schützen, die vorhandene privilegierte Administratorkonten mit ständigem Zugriff auf vertrauliche Daten oder Zugriff auf wichtige Konfigurationseinstellungen verwenden können.

- [Übersicht über die Verwaltung privilegierter Zugriffsrechte](privileged-access-management-overview.md)
- [Konfigurieren von Privileged Access Management](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a>Schritt 5: Konfigurieren von SharePoint-Gerätezugriffs Richtlinien

Gerätezugriffs Richtlinien für SharePoint Online und OneDrive for Business werden zum Schutz vertraulicher, klassifizierter und regulierter Daten empfohlen. In Kürze können Gerätezugriffs Richtlinien auf einzelne Teamwebsites angewendet werden.
  
- [Steuern des Zugriffs von nicht verwalteten Geräten](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a>Schritt 6: Konfigurieren der APP und des Datenschutzes für Geräte

Sie können Anwendungen auf mobilen Geräten verwalten, unabhängig davon, ob die Geräte für die Verwaltung mobiler Geräte registriert sind. Dies schützt vor versehentlichem Datenverlust in Office 365, einschließlich e-Mails und Dateien.
  
- Für iOS und Android: [Schützen von App-Daten mithilfe von App-Schutzrichtlinien mit Microsoft InTune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)
    
Konfigurieren Sie Windows Information Protection (WIP) für Windows 10, um versehentliche Datenverluste zu vermeiden.
  
- Für verwaltete Geräte: [Erstellen eines Windows Information Protection (WIP) mit einer Registrierungsrichtlinie mithilfe des Azure-Portals für Microsoft InTune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)
    
- Für nicht verwaltete Geräte: [Erstellen und Bereitstellen von Windows Information Protection (WIP)-app-Schutzrichtlinie mit InTune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)
    
## <a name="step-7-manage-devices-with-intune"></a>Schritt 7: Verwalten von Geräten mit InTune

Durch die Verwaltung von Geräten können Sie sicherstellen, dass Sie fehlerfrei und kompatibel sind, bevor Sie den Zugriff auf Ressourcen in Ihrer Umgebung ermöglichen. Gerätebasierte bedingte Zugriffsregeln helfen sicherzustellen, dass Angreifer keinen Zugriff auf Ihre Ressourcen von nicht verwalteten Geräten aus erhalten.
  
- [Registrieren von Geräten für die Verwaltung in InTune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a>Schritt 8: Konfigurieren zusätzlicher InTune-Richtlinien und Regeln für den bedingten Zugriff für Ihre Umgebung

Verwenden Sie diese empfohlenen Konfigurationen als Ausgangspunkt für Enterprise scale-oder ausgefeilte Access-Sicherheitsszenarien.
  
- [Sichere e-Mail-Richtlinien und-Konfigurationen](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

