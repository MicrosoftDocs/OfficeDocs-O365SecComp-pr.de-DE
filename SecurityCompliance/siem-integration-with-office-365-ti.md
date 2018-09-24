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
ms.openlocfilehash: 057d8ac101b96f37846ac751645934279d45dc88
ms.sourcegitcommit: 17c7e18d7d00135b1af40cbea117c9a817a41117
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2018
ms.locfileid: "24972257"
---
# <a name="siem-integration-with-office-365-threat-intelligence-and-advanced-threat-protection"></a>Integration mit Office 365 Bedrohungsanalyse und erweiterte Threat Protection SIEM

Wenn Ihre Organisation einen Server Security Vorfall und Event Management (SIEM) verwendet wird, können Sie Office 365 Bedrohungsanalyse und erweiterte Schutz mit Ihrem Server SIEM integrieren. SIEM-Integration können Sie Informationen wie Malware entdeckt erweiterte Schutz für Office 365 und Bedrohungsanalyse, der SIEM-Server-Berichte anzeigen. Um SIEM Integration einzurichten, verwenden Sie die [Aktivität-Verwaltungs-API für Office 365](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference). 

Office 365-Aktivität Verwaltungs-API werden Informationen zu Benutzer, Admin, System, und Richtlinienaktionen und Ereignisse aus Office 365 und Azure Active Directory-Aktivitätsprotokolle Ihrer Organisation abgerufen. [Office 365 erweiterte Threat Protection und Bedrohungsanalyse Schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-intelligence-schema) arbeitet mit Bedrohungsanalyse und/oder erweiterte Threat Protection, so dass, wenn Ihre Organisation erweiterte Threat Protection aber nicht Bedrohungsanalyse (oder umgekehrt) verfügt, Sie können Verwenden Sie weiterhin mit derselben API für Ihre SIEM-Server-Integration. 

Der SIEM-Server oder einem anderen ähnlichen System sollte die **audit.general** Arbeitslast auf Access Erkennungsereignisse abrufen. Informationen finden Sie weitere [Einstieg in Office 365-Management-APIs](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis). 

> [!IMPORTANT]
> Sie müssen ein globaler Office 365-Administrator sein, oder die Administrator Sicherheitsrolle im Compliance Center & Sicherheit SIEM-Integration mit Office 365 Bedrohungsanalyse und erweiterte Schutz eingerichtet haben.<br/>Überwachungsprotokollierung muss für die Office 365-Umgebung aktiviert werden. Hilfe hierzu finden Sie unter [Aktivieren von Office 365 Such-Protokoll aktiviert oder deaktiviert](turn-audit-log-search-on-or-off.md).

## <a name="related-topics"></a>Verwandte Themen

[Informationen zu Bedrohungen in Office 365](office-365-ti.md)

[Office 365 Advanced Threat Protection](office-365-atp.md)

[Smart-Berichte und Einblicke in die Office 365-Sicherheit &amp; Compliance Center](reports-and-insights-in-security-and-compliance.md)
  
[Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md)
  

