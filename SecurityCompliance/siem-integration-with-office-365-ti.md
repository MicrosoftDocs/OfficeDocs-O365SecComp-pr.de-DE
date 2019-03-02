---
title: SIEM-Integration mit Office 365 Threat Intelligence und Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
ms.collection:
- M365-security-compliance
description: Integrieren Sie den SIEM-Server Ihrer Organisation mit Office 365 Threat Intelligence und Advanced Threat Protection mit der Office 365 Activity Management-API.
ms.openlocfilehash: 68d2b4387c1af2363fbb67d0671edeaaa4dc652d
ms.sourcegitcommit: 7adfd8eda038cf25449bdf3df78b5e2fcc1999e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/01/2019
ms.locfileid: "30357436"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a><span data-ttu-id="c45d8-103">SIEM-Integration mit Office 365 Threat Intelligence und Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="c45d8-103">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>

<span data-ttu-id="c45d8-p101">Wenn Ihre Organisation einen SIEM-Server (Security Incident and Event Management) verwendet, können Sie Office 365 Threat Intelligence und Advanced Threat Protection mit Ihrem SIEM-Server integrieren. Mit der SIEM-Integration können Sie Informationen, wie Malware, die von Office 365 Advanced Protection and Threat Intelligence erkannt wurden, in ihren SIEM-Server Berichten anzeigen. Um SIEM-Integration einzurichten, verwenden Sie die [Office 365 Activity Management-API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="c45d8-p101">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Threat Intelligence and Advanced Threat Protection with your SIEM server. SIEM integration enables you to view information, such as malware detected by Office 365 Advanced Protection and Threat Intelligence, in your SIEM server reports. To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="c45d8-p102">Die Office 365 Activity Management-API ruft Informationen zu Benutzer-, Administrator-, System-und Richtlinienaktionen und-Ereignissen aus den Office 365-und Azure Active Directory-Aktivitätsprotokollen Ihrer Organisation ab. Das [Microsoft Office 365 Advanced Threat Protection-und Threat Intelligence-Schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) funktioniert mit Threat Intelligence und/oder Advanced Threat Protection, wenn Ihre Organisation also fortschrittlichen Bedrohungsschutz, aber keine Bedrohungs Intelligenz (oder umgekehrt) besitzt, können Sie Verwenden Sie die gleiche API für Ihre SIEM-Server Integration.</span><span class="sxs-lookup"><span data-stu-id="c45d8-p102">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs. The [Office 365 Advanced Threat Protection and Threat Intelligence schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Threat Intelligence and/or Advanced Threat Protection, so if your organization has Advanced Threat Protection but not Threat Intelligence (or vice versa), you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="c45d8-p103">Der SIEM-Server oder ein anderes ähnliches System sollte die **Überwachung Abfragen. allgemeine** Arbeitslast für den Zugriff auf Erkennungsereignisse. Weitere Informationen finden Sie unter [Erste Schritte mit Office 365-Verwaltungs-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="c45d8-p103">The SIEM server or other similar system should poll the **audit.general** workload to access detection events. To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="c45d8-111">Sie müssen ein globaler Office 365-Administrator sein oder über die Sicherheitsadministrator Rolle verfügen, die dem Security & Compliance Center zugewiesen ist, um die Integration von SIEM in Office 365 Advanced Threat Protection einzurichten.</span><span class="sxs-lookup"><span data-stu-id="c45d8-111">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="c45d8-p104">Die Überwachungsprotokollierung muss für Ihre Office 365-Umgebung aktiviert sein. Hilfe zu diesem Thema finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="c45d8-p104">Audit logging must be turned on for your Office 365 environment. To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c45d8-114">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="c45d8-114">Related topics</span></span>

[<span data-ttu-id="c45d8-115">Informationen zu Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="c45d8-115">Office 365 Threat Intelligence</span></span>](office-365-ti.md)

[<span data-ttu-id="c45d8-116">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="c45d8-116">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="c45d8-117">Intelligente Berichte und Einblicke im Office 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="c45d8-117">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="c45d8-118">Berechtigungen im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="c45d8-118">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  

