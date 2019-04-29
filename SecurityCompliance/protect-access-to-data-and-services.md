---
title: Schutz von Benutzer- und Gerätezugriff
ms.author: bcarter
author: brendacarter
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
ms.openlocfilehash: e1b529a641d25f82521c40d0df9d091e0ebb5d90
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33403003"
---
# <a name="protect-user-and-device-access"></a>Schutz von Benutzer- und Gerätezugriff

Der Schutz des Zugriffs auf Ihre Office 365-Daten und-Dienste ist entscheidend für die Abwehr von Cyber-Angriffen und Schutz vor Datenverlust. Der gleiche Schutz kann auf andere SaaS-Anwendungen in Ihrer Umgebung und sogar auf lokale Anwendungen angewendet werden, die mit Azure Active Directory-Anwendungs Proxy veröffentlicht werden.
  
## <a name="step-1-review-recommendations"></a>Schritt 1: Überprüfungen von Empfehlungen

Empfohlene Funktionen zum Schutz von Identitäten und Geräten, die auf Office 365, andere SaaS-Dienste und lokale Anwendungen zugreifen, die mit dem Azure AD-Anwendungsproxy veröffentlicht werden.
  
[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Weitere Sprachen](https://www.microsoft.com/download/details.aspx?id=55032)
  
## <a name="step-2-protect-administrator-accounts-and-access"></a>Schritt 2: Schützen von Administratorkonten und Zugriff
Die administrativen Konten, die Sie zum Verwalten Ihrer Office 365-Umgebung verwenden, verfügen über erhöhte Berechtigungen. Dies sind wertvolle Ziele für Hacker und Cyber-Kriminelle. 

Beginnen Sie mit der Verwendung von Administratorkonten nur für die Verwaltung. Administratoren sollten über ein separates Benutzerkonto für reguläre, nicht administrative Verwendung verfügen und Ihr Administratorkonto nur verwenden, wenn dies erforderlich ist, um eine Aufgabe zu erledigen, die Ihrer Job-Funktion zugeordnet ist.

Schützen Sie Ihre Administratorkonten durch mehrstufige Authentifizierung und bedingten Zugriff. Weitere Informationen finden Sie unter [Schützen von Administratorkonten](https://docs.microsoft.com/en-us/microsoft-365/enterprise/identity-access-prerequisites#protecting-administrator-accounts). 

Konfigurieren Sie als nächstes die privilegierte Zugriffsverwaltung in Office 365. Privileged Access Management ermöglicht eine granulare Zugriffssteuerung über privilegierte Verwaltungsaufgaben in Office 365. Es kann dazu beitragen, Ihre Organisation vor Verstößen zu schützen, die vorhandene privilegierte Administratorkonten mit ständigem Zugriff auf vertrauliche Daten oder Zugriff auf wichtige Konfigurationseinstellungen verwenden können.

- [Übersicht über die Verwaltung privilegierter Zugriffsrechte](privileged-access-management-overview.md)
- [Konfigurieren von Privileged Access Management](privileged-access-management-configuration.md)

Eine weitere wichtige Empfehlung besteht darin, Workstations zu verwenden, die speziell für administrative Aufgaben konfiguriert wurden. Hierbei handelt es sich um dedizierte Geräte, die nur für Verwaltungsaufgaben verwendet werden. Weitere Informationen finden Sie unter [Sichern des privilegierten Zugriffs](https://docs.microsoft.com/en-us/windows-server/identity/securing-privileged-access/securing-privileged-access).

Schließlich können Sie die Auswirkungen von versehentlichem mangelndem Verwaltungszugriff verringern, indem Sie zwei oder mehr Notfall Zugriffskonten in Ihrem Mandanten erstellen. Weitere Informationen finden Sie unter [Manage Emergency Access Accounts in Azure AD](https://docs.microsoft.com/en-us/azure/active-directory/users-groups-roles/directory-emergency-access). 

## <a name="step-3-configure-recommended-identity-and-device-access-policies"></a>Schritt 3: Konfigurieren der empfohlenen Identitäts-und Gerätezugriffs Richtlinien
Multi-Factor Authentication (MFA)-und Conditional Access-Richtlinien sind leistungsstarke Tools für die Minderung von kompromittierten Konten und nicht autorisiertem Zugriff. Es wird empfohlen, eine Reihe von Richtlinien zu implementieren, die gemeinsam getestet wurden. Weitere Informationen, einschließlich Bereitstellungsschritte, finden Sie unter [Identity and Device Access Configurations](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-policies-configurations).

 Diese Richtlinien implementieren die folgenden Funktionen:
- Mehrstufige Authentifizierung
- Bedingter Zugriff
- InTune-App-Schutz (app-und Datenschutz für Geräte)
- InTune-Geräte Konformität
- Azure AD Identity Protection

Die Implemetning InTune-Geräte Konformität erfordert die Geräteregistrierung. Durch die Verwaltung von Geräten können Sie sicherstellen, dass Sie fehlerfrei und kompatibel sind, bevor Sie den Zugriff auf Ressourcen in Ihrer Umgebung ermöglichen. Weitere Informationen finden Sie unter [Registrieren von Geräten für die Verwaltung in InTune](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)

## <a name="step-4-configure-sharepoint-device-access-policies"></a>Schritt 4: Konfigurieren von SharePoint-Gerätezugriffs Richtlinien

Microsoft empfiehlt, dass Sie Inhalte in SharePoint-Websites mit vertraulichen und hoch regulierten Inhalten mit Gerätezugriffs Steuerungen schützen. Weitere Informationen finden Sie unter [Richtlinien Empfehlungen zum Sichern von SharePoint-Websites und-Dateien](https://docs.microsoft.com/en-us/microsoft-365/enterprise/sharepoint-file-access-policies).



    

