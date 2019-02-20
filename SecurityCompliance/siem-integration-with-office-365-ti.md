---
title: SIEM-Integration mit Office 365 Threat Intelligence und Advanced Threat Protection
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
description: Integrieren Sie den SIEM-Server Ihrer Organisation mit Office 365 Threat Intelligence und Advanced Threat Protection mit der Office 365 Activity Management-API.
ms.openlocfilehash: 854f763b72dfac1a5dc1442b1d9d123ed5439257
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087244"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>SIEM-Integration mit Office 365 Threat Intelligence und Advanced Threat Protection

Wenn Ihre Organisation einen SIEM-Server (Security Incident and Event Management) verwendet, können Sie Office 365 Threat Intelligence und Advanced Threat Protection mit Ihrem SIEM-Server integrieren. Mit der SIEM-Integration können Sie Informationen, wie Malware, die von Office 365 Advanced Protection and Threat Intelligence erkannt wurden, in ihren SIEM-Server Berichten anzeigen. Um SIEM-Integration einzurichten, verwenden Sie die [Office 365 Activity Management-API](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

Die Office 365 Activity Management-API ruft Informationen zu Benutzer-, Administrator-, System-und Richtlinienaktionen und-Ereignissen aus den Office 365-und Azure Active Directory-Aktivitätsprotokollen Ihrer Organisation ab. Das [Microsoft Office 365 Advanced Threat Protection-und Threat Intelligence-Schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) funktioniert mit Threat Intelligence und/oder Advanced Threat Protection, wenn Ihre Organisation also fortschrittlichen Bedrohungsschutz, aber keine Bedrohungs Intelligenz (oder umgekehrt) besitzt, können Sie Verwenden Sie die gleiche API für Ihre SIEM-Server Integration. 

Der SIEM-Server oder ein anderes ähnliches System sollte die **Überwachung Abfragen. allgemeine** Arbeitslast für den Zugriff auf Erkennungsereignisse. Weitere Informationen finden Sie unter [Erste Schritte mit Office 365-Verwaltungs-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). 

> [!IMPORTANT]
> Sie müssen ein globaler Office 365-Administrator sein oder über die Sicherheitsadministrator Rolle verfügen, die dem Security & Compliance Center zugewiesen ist, um die Integration von SIEM in Office 365 Advanced Threat Protection einzurichten.<br/>Die Überwachungsprotokollierung muss für Ihre Office 365-Umgebung aktiviert sein. Hilfe zu diesem Thema finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Verwandte Themen

[Informationen zu Bedrohungen in Office 365](office-365-ti.md)

[Office 365 Advanced Threat Protection](office-365-atp.md)

[Intelligente Berichte und Einblicke im Office 365 &amp; Security Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Berechtigungen im Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
  

