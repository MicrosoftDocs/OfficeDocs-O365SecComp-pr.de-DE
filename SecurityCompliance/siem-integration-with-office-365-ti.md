---
title: Siem-Integration mit Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: dansimp
audience: ITPro
ms.topic: overview
ms.service: O365-seccomp
localization_priority: None
search.appverid:
- MET150
- MOE150
ms.assetid: eb56b69b-3170-4086-82cf-ba40a530fa1b
ms.date: 03/11/2019
ms.collection:
- M365-security-compliance
description: Integrieren Sie den Siem-Server Ihrer Organisation mit Office 365 Advanced Threat Protection und den zugehörigen Threat-Ereignissen in die API für die Office 365-Aktivitätsverwaltung.
ms.openlocfilehash: 4bfc82be273bb4581aa49bbbbdab613bd87b1b89
ms.sourcegitcommit: 32ecff689ae32c59a39b7633ca0f36a304e7516e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2019
ms.locfileid: "35600902"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a><span data-ttu-id="9d5b3-103">Siem-Integration mit Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="9d5b3-103">SIEM integration with Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="9d5b3-104">Wenn Ihre Organisation einen Siem-Server (Security Incident and Event Management) verwendet, können Sie Office 365 Advanced Threat Protection mit Ihrem Siem-Server integrieren.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-104">If your organization is using a security incident and event management (SIEM) server, you can integrate Office 365 Advanced Threat Protection with your SIEM server.</span></span> <span data-ttu-id="9d5b3-105">Mit der Siem-Integration können Sie in ihren Siem-Server Berichten Informationen wie Malware oder Phishing anzeigen, die von Office 365 Advanced Protection erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-105">SIEM integration enables you to view information, such as malware or phish detected by Office 365 Advanced Protection, in your SIEM server reports.</span></span> <span data-ttu-id="9d5b3-106">Um Siem-Integration einzurichten, verwenden Sie die [Office 365-Aktivitäts Verwaltungs-API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span><span class="sxs-lookup"><span data-stu-id="9d5b3-106">To set up SIEM integration, you use the [Office 365 Activity Management API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference).</span></span> 

<span data-ttu-id="9d5b3-107">Die API für die Office 365 Aktivitätsverwaltung Ruft Informationen zu Benutzer-, Verwaltungs-, System-und Richtlinienaktionen und Ereignissen aus den Office 365-und Azure Active Directory-Aktivitätsprotokollen Ihrer Organisation ab.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-107">The Office 365 Activity Management API retrieves information about user, admin, system, and policy actions and events from your organization's Office 365 and Azure Active Directory activity logs.</span></span> <span data-ttu-id="9d5b3-108">Das [Office 365 Advanced Threat Protection-Schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) funktioniert mit Advanced Threat Protection, wenn Ihre Organisation also über die Office 365 Advanced Threat Protection Plan 1 oder Plan 2 oder Office 365 E5 verfügt, können Sie die gleiche API für Ihre Siem-Server Integration weiterhin verwenden.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-108">The [Office 365 Advanced Threat Protection schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) works with Advanced Threat Protection, so if your organization has the Office 365 Advanced Threat Protection Plan 1 or Plan 2 or Office 365 E5, you can still use that same API for your SIEM server integration.</span></span> 

<span data-ttu-id="9d5b3-109">Der Siem-Server oder ein ähnliches System sollten die **Audit. allgemeine** Arbeitsauslastung für den Zugriff auf Erkennungsereignisse Abfragen.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-109">The SIEM server or other similar system should poll the **audit.general** workload to access detection events.</span></span> <span data-ttu-id="9d5b3-110">Weitere Informationen finden Sie unter [Erste Schritte mit Office 365-Verwaltungs-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span><span class="sxs-lookup"><span data-stu-id="9d5b3-110">To learn more see [Get started with Office 365 Management APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis).</span></span> <span data-ttu-id="9d5b3-111">Darüber hinaus sind die folgenden Werte von **AuditLogRecordType** für Office 365 ATP-Ereignisse relevant:</span><span class="sxs-lookup"><span data-stu-id="9d5b3-111">In addition, the following values of **AuditLogRecordType** are relevant for Office 365 ATP events:</span></span>

### <a name="enum-auditlogrecordtype---type-edmint32"></a><span data-ttu-id="9d5b3-112">Enum: AuditLogRecordType - Typ: Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="9d5b3-112">Enum: AuditLogRecordType - Type: Edm.Int32</span></span>

#### <a name="auditlogrecordtype"></a><span data-ttu-id="9d5b3-113">AuditLogRecordType</span><span class="sxs-lookup"><span data-stu-id="9d5b3-113">AuditLogRecordType</span></span>

|<span data-ttu-id="9d5b3-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9d5b3-114">Value</span></span>|<span data-ttu-id="9d5b3-115">Elementname</span><span class="sxs-lookup"><span data-stu-id="9d5b3-115">Member name</span></span>|<span data-ttu-id="9d5b3-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d5b3-116">Description</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9d5b3-117">28</span><span class="sxs-lookup"><span data-stu-id="9d5b3-117">28</span></span>|<span data-ttu-id="9d5b3-118">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="9d5b3-118">ThreatIntelligence</span></span>|<span data-ttu-id="9d5b3-119">Phishing- und Schadsoftwareereignisse aus Exchange Online Protection und Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-119">Phishing and malware events from Exchange Online Protection and Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="9d5b3-120">41</span><span class="sxs-lookup"><span data-stu-id="9d5b3-120">41</span></span>|<span data-ttu-id="9d5b3-121">ThreatIntelligenceUrl</span><span class="sxs-lookup"><span data-stu-id="9d5b3-121">ThreatIntelligenceUrl</span></span>|<span data-ttu-id="9d5b3-122">ATP-sichere Links Time-of-Block-und Block Außerkraftsetzungs Ereignisse von Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-122">ATP Safe Links time-of-block and block override events from Office 365 Advanced Threat Protection.</span></span>|
|<span data-ttu-id="9d5b3-123">47</span><span class="sxs-lookup"><span data-stu-id="9d5b3-123">47</span></span>|<span data-ttu-id="9d5b3-124">ThreatIntelligenceAtpContent</span><span class="sxs-lookup"><span data-stu-id="9d5b3-124">ThreatIntelligenceAtpContent</span></span>|<span data-ttu-id="9d5b3-125">Phishing-und Schadsoftware-Ereignisse für Dateien in SharePoint Online, OneDrive für Unternehmen und Microsoft Teams aus Office 365 Advanced Threat Protection.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-125">Phishing and malware events for files in SharePoint Online, OneDrive for Business, and Microsoft Teams from Office 365 Advanced Threat Protection.</span></span>|

> [!IMPORTANT]
> <span data-ttu-id="9d5b3-126">Sie müssen ein Office 365 globaler Administrator sein oder der Sicherheitsadministrator Rolle für das Security #a0 Compliance Center zugewiesen sein, um Siem-Integration mit Office 365 Advanced Threat Protection einzurichten.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-126">You must be an Office 365 global administrator or have the security administrator role assigned for the Security & Compliance Center to set up SIEM integration with Office 365 Advanced Threat Protection.</span></span><br/><span data-ttu-id="9d5b3-127">Die Überwachungsprotokollierung muss für Ihre Office 365 Umgebung aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="9d5b3-127">Audit logging must be turned on for your Office 365 environment.</span></span> <span data-ttu-id="9d5b3-128">Informationen dazu finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="9d5b3-128">To get help with this, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d5b3-129">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9d5b3-129">Related topics</span></span>

[<span data-ttu-id="9d5b3-130">Untersuchung und Reaktion der Office 365 Bedrohung</span><span class="sxs-lookup"><span data-stu-id="9d5b3-130">Office 365 Threat Investigation and Response</span></span>](office-365-ti.md)

[<span data-ttu-id="9d5b3-131">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="9d5b3-131">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)

[<span data-ttu-id="9d5b3-132">Intelligente Berichte und Einblicke im Office 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="9d5b3-132">Smart reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="9d5b3-133">Berechtigungen im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="9d5b3-133">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
  
