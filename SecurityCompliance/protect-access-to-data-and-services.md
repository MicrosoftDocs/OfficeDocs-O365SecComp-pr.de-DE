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
# <a name="protect-access-to-data-and-services-in-office-365"></a><span data-ttu-id="90055-103">Zugriffsschutz für Daten und Dienste in Office 365</span><span class="sxs-lookup"><span data-stu-id="90055-103">Protect access to data and services in Office 365</span></span>

<span data-ttu-id="90055-p101">Der Schutz des Zugriffs auf Ihre Office 365-Daten und-Dienste ist entscheidend für die Abwehr von Cyber-Angriffen und Schutz vor Datenverlust. Der gleiche Schutz kann auf andere SaaS-Anwendungen in Ihrer Umgebung und sogar auf lokale Anwendungen angewendet werden, die mit Azure Active Directory-Anwendungs Proxy veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="90055-p101">Protecting access to your Office 365 data and services is crucial to defending against cyber-attacks and guarding against data loss. The same protections can be applied to other SaaS applications in your environment and even to on-premises applications published with Azure Active Directory Application Proxy.</span></span>
  
## <a name="step-1-review-recommendations"></a><span data-ttu-id="90055-106">Schritt 1: Überprüfungen von Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="90055-106">Step 1: Review recommendations</span></span>

<span data-ttu-id="90055-107">Empfohlene Funktionen zum Schutz von Identitäten und Geräten, die auf Office 365, andere SaaS-Dienste und lokale Anwendungen zugreifen, die mit dem Azure AD-Anwendungsproxy veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="90055-107">Recommended capabilities for protecting identities and devices that access Office 365, other SaaS services, and on-premises applications published with Azure AD Application Proxy.</span></span>
  
<span data-ttu-id="90055-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [Weitere Sprachen](https://www.microsoft.com/download/details.aspx?id=55032)</span><span class="sxs-lookup"><span data-stu-id="90055-108">[PDF](https://go.microsoft.com/fwlink/p/?linkid=841656) | [Visio](https://go.microsoft.com/fwlink/p/?linkid=841657) | [More languages](https://www.microsoft.com/download/details.aspx?id=55032)</span></span>
  
## <a name="step-2-configure-mfa"></a><span data-ttu-id="90055-109">Schritt 2: Konfigurieren von MFA</span><span class="sxs-lookup"><span data-stu-id="90055-109">Step 2: Configure MFA</span></span>

<span data-ttu-id="90055-110">Verwenden Sie diese Ressourcen, um sich an MFA zu orientieren, zu entscheiden, welche Version für Sie geeignet ist, und dann MFA für Ihre Umgebung zu planen und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="90055-110">Use these resources to orient yourself to MFA, decide which version is right for you, and then plan and deploy MFA for your environment.</span></span>
  
- [<span data-ttu-id="90055-111">Was ist Azure Multi-Factor Authentication?</span><span class="sxs-lookup"><span data-stu-id="90055-111">What is Azure multi-factor authentication?</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication)
    
- [<span data-ttu-id="90055-112">Wählen Sie die Azure Multi-Factor Authentication Solution für Sie aus.</span><span class="sxs-lookup"><span data-stu-id="90055-112">Choose the Azure multi-factor authentication solution for you</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="90055-113">So erhalten Sie die Azure Multi-Factor Authentication</span><span class="sxs-lookup"><span data-stu-id="90055-113">How to get Azure multi-factor authentication</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-versions-plans)
    
- [<span data-ttu-id="90055-114">Planen der mehrstufigen Authentifizierung für Office 365-Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="90055-114">Plan for multi-factor authentication for Office 365 deployments</span></span>](https://support.office.com/article/043807b2-21db-4d5c-b430-c8a6dee0e6ba)
    
- [<span data-ttu-id="90055-115">Einrichten der mehrstufigen Authentifizierung für Office 365-Benutzer</span><span class="sxs-lookup"><span data-stu-id="90055-115">Set up multi-factor authentication for Office 365 users</span></span>](https://support.office.com/article/8f0454b2-f51a-4d9c-bcde-2c48e41621c6)
    
- [<span data-ttu-id="90055-116">Planen der Bereitstellung von MFA, Cloud oder lokal</span><span class="sxs-lookup"><span data-stu-id="90055-116">Plan where to deploy MFA, Cloud or on-premises</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started)
    
- [<span data-ttu-id="90055-117">Konfigurieren von Azure-Einstellungen für mehrstufige Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="90055-117">Configure Azure multi-factor authentication settings</span></span>](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-whats-next)
    
## <a name="step-3-enforce-mfa-with-azure-ad-conditional-access-rules"></a><span data-ttu-id="90055-118">Schritt 3: Erzwingen von MFA mit Azure AD Conditional Access Rules</span><span class="sxs-lookup"><span data-stu-id="90055-118">Step 3: Enforce MFA with Azure AD conditional access rules</span></span>

<span data-ttu-id="90055-119">Wenn Sie Azure AD MFA verwenden, erstellen Sie eine Regel für bedingten Zugriff für den Zugriff auf Office 365 und andere SaaS-apps in Ihrer Umgebung.</span><span class="sxs-lookup"><span data-stu-id="90055-119">If you are using Azure AD MFA, create a conditional access rule to require MFA for access to Office 365 and other SaaS apps in your environment.</span></span>
  
- [<span data-ttu-id="90055-120">Bedingter Zugriff in Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="90055-120">Conditional access in Azure Active Directory</span></span>](https://docs.microsoft.com/azure/active-directory/active-directory-conditional-access-azure-portal)
    
## <a name="step-4-configure-privileged-access-management"></a><span data-ttu-id="90055-121">Schritt 4: Konfigurieren von privileged Access Management</span><span class="sxs-lookup"><span data-stu-id="90055-121">Step 4: Configure privileged access management</span></span>

<span data-ttu-id="90055-p102">Privileged Access Management ermöglicht eine granulare Zugriffssteuerung über privilegierte Verwaltungsaufgaben in Office 365.  Es kann dazu beitragen, Ihre Organisation vor Verstößen zu schützen, die vorhandene privilegierte Administratorkonten mit ständigem Zugriff auf vertrauliche Daten oder Zugriff auf wichtige Konfigurationseinstellungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="90055-p102">Privileged access management allows granular access control over privileged admin tasks in Office 365.  It can help protect your organization from breaches that may use existing privileged admin accounts with standing access to sensitive data or access to critical configuration settings.</span></span>

- [<span data-ttu-id="90055-124">Übersicht über die Verwaltung privilegierter Zugriffsrechte</span><span class="sxs-lookup"><span data-stu-id="90055-124">Overview of privileged access management</span></span>](privileged-access-management-overview.md)
- [<span data-ttu-id="90055-125">Konfigurieren von Privileged Access Management</span><span class="sxs-lookup"><span data-stu-id="90055-125">Configure privileged access management</span></span>](privileged-access-management-configuration.md)

## <a name="step-5-configure-sharepoint-device-access-policies"></a><span data-ttu-id="90055-126">Schritt 5: Konfigurieren von SharePoint-Gerätezugriffs Richtlinien</span><span class="sxs-lookup"><span data-stu-id="90055-126">Step 5: Configure SharePoint device access policies</span></span>

<span data-ttu-id="90055-p103">Gerätezugriffs Richtlinien für SharePoint Online und OneDrive for Business werden zum Schutz vertraulicher, klassifizierter und regulierter Daten empfohlen. In Kürze können Gerätezugriffs Richtlinien auf einzelne Teamwebsites angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="90055-p103">Device access policies for SharePoint Online and OneDrive for Business are recommended for protecting sensitive, classified, and regulated data. Coming soon is the ability to apply device access policies to individual team sites.</span></span>
  
- [<span data-ttu-id="90055-129">Steuern des Zugriffs von nicht verwalteten Geräten</span><span class="sxs-lookup"><span data-stu-id="90055-129">Control access from unmanaged devices</span></span>](https://support.office.com/article/Control-access-from-unmanaged-devices-5ae550c4-bd20-4257-847b-5c20fb053622?ui=en-US&amp;rs=en-US&amp;ad=US)
    
## <a name="step-6-configure-app-and-data-protection-for-devices"></a><span data-ttu-id="90055-130">Schritt 6: Konfigurieren der APP und des Datenschutzes für Geräte</span><span class="sxs-lookup"><span data-stu-id="90055-130">Step 6: Configure app and data protection for devices</span></span>

<span data-ttu-id="90055-p104">Sie können Anwendungen auf mobilen Geräten verwalten, unabhängig davon, ob die Geräte für die Verwaltung mobiler Geräte registriert sind. Dies schützt vor versehentlichem Datenverlust in Office 365, einschließlich e-Mails und Dateien.</span><span class="sxs-lookup"><span data-stu-id="90055-p104">You can manage applications on mobile devices regardless of whether the devices are enrolled for mobile device management. This protects against accidental leakage of data in Office 365, including mail and files.</span></span>
  
- <span data-ttu-id="90055-133">Für iOS und Android: [Schützen von App-Daten mithilfe von App-Schutzrichtlinien mit Microsoft InTune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span><span class="sxs-lookup"><span data-stu-id="90055-133">For iOS and Android: [Protect app data using app protection policies with Microsoft Intune](https://docs.microsoft.com/intune-classic/deploy-use/protect-app-data-using-mobile-app-management-policies-with-microsoft-intune)</span></span>
    
<span data-ttu-id="90055-134">Konfigurieren Sie Windows Information Protection (WIP) für Windows 10, um versehentliche Datenverluste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="90055-134">For Windows 10, configure Windows Information Protection (WIP) to prevent accidental data leaks.</span></span>
  
- <span data-ttu-id="90055-135">Für verwaltete Geräte: [Erstellen eines Windows Information Protection (WIP) mit einer Registrierungsrichtlinie mithilfe des Azure-Portals für Microsoft InTune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span><span class="sxs-lookup"><span data-stu-id="90055-135">For managed devices: [Create a Windows Information Protection (WIP) with enrollment policy using the Azure portal for Microsoft Intune](https://docs.microsoft.com/windows/threat-protection/windows-information-protection/create-wip-policy-using-intune-azure)</span></span>
    
- <span data-ttu-id="90055-136">Für nicht verwaltete Geräte: [Erstellen und Bereitstellen von Windows Information Protection (WIP)-app-Schutzrichtlinie mit InTune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span><span class="sxs-lookup"><span data-stu-id="90055-136">For un-managed devices: [Create and deploy Windows Information Protection (WIP) app protection policy with Intune](https://docs.microsoft.com/intune/windows-information-protection-policy-create)</span></span>
    
## <a name="step-7-manage-devices-with-intune"></a><span data-ttu-id="90055-137">Schritt 7: Verwalten von Geräten mit InTune</span><span class="sxs-lookup"><span data-stu-id="90055-137">Step 7: Manage devices with Intune</span></span>

<span data-ttu-id="90055-p105">Durch die Verwaltung von Geräten können Sie sicherstellen, dass Sie fehlerfrei und kompatibel sind, bevor Sie den Zugriff auf Ressourcen in Ihrer Umgebung ermöglichen. Gerätebasierte bedingte Zugriffsregeln helfen sicherzustellen, dass Angreifer keinen Zugriff auf Ihre Ressourcen von nicht verwalteten Geräten aus erhalten.</span><span class="sxs-lookup"><span data-stu-id="90055-p105">Managing devices allows you to ensure that they are healthy and compliant before allowing them access to resources in your environment. Device based conditional access rules help ensure attackers can't gain access to your resources from unmanaged devices.</span></span>
  
- [<span data-ttu-id="90055-140">Registrieren von Geräten für die Verwaltung in InTune</span><span class="sxs-lookup"><span data-stu-id="90055-140">Enroll devices for management in Intune</span></span>](https://docs.microsoft.com/intune-classic/deploy-use/enroll-devices-in-microsoft-intune)
    
## <a name="step-8-configure-additional-intune-policies-and-conditional-access-rules-for-your-environment"></a><span data-ttu-id="90055-141">Schritt 8: Konfigurieren zusätzlicher InTune-Richtlinien und Regeln für den bedingten Zugriff für Ihre Umgebung</span><span class="sxs-lookup"><span data-stu-id="90055-141">Step 8: Configure additional Intune policies and conditional access rules for your environment</span></span>

<span data-ttu-id="90055-142">Verwenden Sie diese empfohlenen Konfigurationen als Ausgangspunkt für Enterprise scale-oder ausgefeilte Access-Sicherheitsszenarien.</span><span class="sxs-lookup"><span data-stu-id="90055-142">Use these recommended configurations as a starting point for enterprise scale or sophisticated access security scenarios.</span></span>
  
- [<span data-ttu-id="90055-143">Sichere e-Mail-Richtlinien und-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="90055-143">Secure email policies and configurations</span></span>](https://docs.microsoft.com/azure/active-directory/secure-email-introduction)
    

