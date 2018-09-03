---
title: Integration mit Office 365 Bedrohungsanalyse und erweiterte Threat Protection SIEM
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: o365-administration
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
description: Integrieren von Ihrer Organisation SIEM Server mit Office 365 Bedrohungsanalyse und erweiterte Schutz mit Office 365-Aktivität Verwaltungs-API.
ms.openlocfilehash: 40c84b9d7b7ec4c9b15383e3ffbbabf839294def
ms.sourcegitcommit: e7b87fae103a858981bdbcdf7ec55afa4751ad05
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2018
ms.locfileid: "23782142"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a><span data-ttu-id="18183-103">Integration mit Office 365 Bedrohungsanalyse und erweiterte Threat Protection SIEM</span><span class="sxs-lookup"><span data-stu-id="18183-103">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>

<span data-ttu-id="18183-p101">Wenn Ihre Organisation einen Server Security Vorfall und Event Management (SIEM) verwendet wird, können Sie Office 365 Bedrohungsanalyse und erweiterte Schutz mit Ihrem Server SIEM integrieren. SIEM-Integration können Sie Informationen wie Malware entdeckt erweiterte Schutz für Office 365 und Bedrohungsanalyse, der SIEM-Server-Berichte anzeigen. Um SIEM Integration einzurichten, verwenden Sie die [Aktivität-Verwaltungs-API für Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="18183-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence and Advanced Threat Protection with your SIEM server. SIEM integration enables you to view information, such as malware detected by Office 365 Advanced Protection and Threat Intelligence, in your SIEM server reports. To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="18183-p102">Office 365-Aktivität Verwaltungs-API werden Informationen zu Benutzer, Admin, System, und Richtlinienaktionen und Ereignisse aus Office 365 und Azure Active Directory-Aktivitätsprotokolle Ihrer Organisation abgerufen. [Office 365 erweiterte Threat Protection und Bedrohungsanalyse Schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) arbeitet mit Bedrohungsanalyse und/oder erweiterte Threat Protection, so dass, wenn Ihre Organisation erweiterte Threat Protection aber nicht Bedrohungsanalyse (oder umgekehrt) verfügt, Sie können Verwenden Sie weiterhin mit derselben API für Ihre SIEM-Server-Integration.</span><span class="sxs-lookup"><span data-stu-id="18183-p102">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs. The [Office 365 Advanced Threat Protection and Threat Intelligence schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Threat Intelligence and/or Advanced Threat Protection, so if your organization has Advanced Threat Protection but not Threat Intelligence (or vice versa), you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="18183-p103">Der SIEM-Server oder einem anderen ähnlichen System sollte die **audit.general** Arbeitslast auf Access Erkennungsereignisse abrufen. Informationen finden Sie weitere [Einstieg in Office 365-Management-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="18183-p103">The SIEM server or other similar system should poll the **audit.general** workload to access detection events. To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="18183-111">Sie müssen ein globaler Office 365-Administrator sein, oder die Administrator Sicherheitsrolle im Compliance Center & Sicherheit SIEM-Integration mit Office 365 Bedrohungsanalyse und erweiterte Schutz eingerichtet haben.</span><span class="sxs-lookup"><span data-stu-id="18183-111">You must be an Office 365 global administrator or have the security administrator role assigned in the Security & Compliance Center to set up SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection.</span></span></br><span data-ttu-id="18183-p104">Überwachungsprotokollierung muss für die Office 365-Umgebung aktiviert werden. Hilfe hierzu finden Sie unter [Aktivieren von Office 365 Such-Protokoll aktiviert oder deaktiviert](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="18183-p104">Audit logging must be turned on for your Office 365 environment. To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="18183-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="18183-114">Related topics</span></span>

[<span data-ttu-id="18183-115">Informationen zu Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="18183-115">Office 365 Threat Intelligence</span></span>](office-365-ti.md)

[<span data-ttu-id="18183-116">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="18183-116">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="18183-117">Smart-Berichte und Einblicke in die Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="18183-117">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="18183-118">Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="18183-118">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

