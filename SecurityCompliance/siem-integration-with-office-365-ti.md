---
title: SIEM-Integration in Office 365 Advanced Threat Protection
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
ms.date: 03/11/2019
ms.collection:
- M365-security-compliance
description: Integrieren Sie den SIEM-Server Ihrer Organisation in Office 365 Advanced Threat Protection und zugehörige Bedrohungs Ereignisse in die Office 365 Activity Management-API.
ms.openlocfilehash: fa9dcda0556684b748068cbe5ee848ba443d7667
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260683"
---
# <a name="siem-integration-with-office-365-advanced-threat-protection"></a>SIEM-Integration in Office 365 Advanced Threat Protection

Wenn Ihre Organisation einen SIEM-Server (Security Incident and Event Management) verwendet, können Sie Office 365 Advanced Threat Protection mit Ihrem SIEM-Server integrieren. Mit der SIEM-Integration können Sie in ihren SIEM-Server Berichten Informationen anzeigen, wie Malware oder Phishing, die von Office 365 Advanced Protection erkannt wurden. Um SIEM-Integration einzurichten, verwenden Sie die [Office 365 Activity Management-API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

Die Office 365 Activity Management-API ruft Informationen zu Benutzer-, Administrator-, System-und Richtlinienaktionen und-Ereignissen aus den Office 365-und Azure Active Directory-Aktivitätsprotokollen Ihrer Organisation ab. Das [office 365 Advanced Threat Protection-Schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) funktioniert mit Advanced Threat Protection, wenn Ihre Organisation also den Office 365 Advanced Threat Protection Plan 1 oder Plan 2 oder Office 365 E5 hat, können Sie diese API auch weiterhin für Ihre Siem-Server Integration verwenden. 

Der SIEM-Server oder ein anderes ähnliches System sollte die **Überwachung Abfragen. allgemeine** Arbeitslast für den Zugriff auf Erkennungsereignisse. Weitere Informationen finden Sie unter [Erste Schritte mit Office 365-Verwaltungs-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). Darüber hinaus sind die folgenden Werte von **AuditLogRecordType** für Office 365-ATP-Ereignisse relevant:

### <a name="enum-auditlogrecordtype---type-edmint32"></a>Enum: AuditLogRecordType - Typ: Edm.Int32

#### <a name="auditlogrecordtype"></a>AuditLogRecordType

|Wert|Elementname|Beschreibung|
|:-----|:-----|:-----|
|28|ThreatIntelligence|Phishing- und Schadsoftwareereignisse aus Exchange Online Protection und Office 365 Advanced Threat Protection.|
|41|ThreatIntelligenceUrl|ATP-sichere Links-Zeit Block-und Block Außerkraftsetzungs Ereignisse von Office 365 Advanced Threat Protection.|
|47|ThreatIntelligenceAtpContent|Phishing-und Schadsoftware-Ereignisse für Dateien in SharePoint Online, OneDrive for Business und Microsoft Teams aus Office 365 Advanced Threat Protection.|

> [!IMPORTANT]
> Sie müssen ein globaler Office 365-Administrator sein oder über die Sicherheitsadministrator Rolle verfügen, die dem Security & Compliance Center zugewiesen ist, um die Integration von SIEM in Office 365 Advanced Threat Protection einzurichten.<br/>Die Überwachungsprotokollierung muss für Ihre Office 365-Umgebung aktiviert sein. Hilfe zu diesem Thema finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Verwandte Themen

[Office 365 Bedrohungs Ermittlung und-Antwort](office-365-ti.md)

[Office 365 Advanced Threat Protection](office-365-atp.md)

[Intelligente Berichte und Einblicke im Office 365 &amp; Security Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
  
