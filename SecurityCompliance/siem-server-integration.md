---
title: SIEM-Server Integration mit Microsoft 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: O365-seccomp
localization_priority: Normal
ms.collection:
- M365-security-compliance
ms.custom:
- Ent_Solutions
- SIEM
description: 'Zusammenfassung: Lesen Sie diesen Artikel, um einen Überblick über die SIEM-Server Integration mit Microsoft 365 zu erhalten.'
ms.openlocfilehash: 905f6fc9b6fd62748e25c27d6e5cdbedacc0f806
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693644"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a>SIEM-Server Integration mit Microsoft 365-Diensten und-Anwendungen

## <a name="overview"></a>Übersicht

Wenn Ihre Organisation einen SIEM-Server (Security Information and Event Management) verwendet, oder wenn Sie planen, einen SIEM-Server in Kürze zu erhalten, Fragen Sie sich vielleicht, wie sich dies in Microsoft 365, einschließlich Office 365 Enterprise, integrieren lässt. Ob Sie einen SIEM-Server benötigen, hängt von vielen Faktoren wie den Sicherheitsanforderungen Ihrer Organisation ab. Microsoft 365 bietet eine Vielzahl von Sicherheitsfunktionen; Wenn Ihre Organisation jedoch Inhalte und Anwendungen in lokalen und in der Cloud hat (wie bei einer hybriden Cloud-Bereitstellung), können Sie einen SIEM-Server für zusätzlichen Schutz hinzufügen. Wenn Ihre Organisation besonders strenge Sicherheitsanforderungen erfüllt, müssen Sie möglicherweise einen SIEM-Server zu Ihrer Umgebung hinzufügen.

## <a name="siem-server-integration-microsoft-365"></a>SIEM-Server Integration Microsoft 365

Ein SIEM-Server kann Daten aus einer Vielzahl von Microsoft 365-Diensten und-Anwendungen empfangen. In der folgenden Tabelle sind mehrere Microsoft 365-Dienste und-Anwendungen zusammen mit SIEM-Server Eingaben aufgeführt und weitere Informationen zur SIEM-Server Integration. 

| Microsoft 365-Dienst oder-Anwendung | SIEM-Server Eingaben | Ressourcen für weitere Informationen |
| --- | --- | --- |
| [Office 365 Advanced Threat Protection](office-365-atp.md) <br/>   oder   <br/>[Informationen zu Bedrohungen in Office 365](office-365-ti.md) | Überwachungsprotokolle | [SIEM-Integration in Office 365 Advanced Threat Protection](siem-integration-with-office-365-ti.md) |
| [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | Protokoll Integration | [SIEM-Integration in Microsoft Cloud-App-Sicherheit](https://docs.microsoft.com/cloud-app-security/siem) |
| [Office 365 Cloud App Security](office-365-cas-overview.md) | Protokoll Integration | [Integrieren Ihres SIEM-Servers in Office 365 Cloud App Security](integrate-your-siem-server-with-office-365-cas.md) |
| [Windows Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/) | Protokoll Integration | [Benachrichtigungen an Ihre SIEM-Tools](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| [Azure-Sicherheits Center](https://docs.microsoft.com/azure/security-center/security-center-intro) (BedrohungsSchutz und BedrohungsErkennung) | Warnungen | [Azure Security Data Export to SIEM-Pipeline Configuration-Preview](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [Azure Active Directory Identity Protection](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | Überwachungsprotokolle | [Integrieren von Azure Active Directory-Überwachungsprotokollen](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [Erweiterte Azure-BedrohungsAnalyse](https://docs.microsoft.com/azure/security/azure-threat-detection) | Protokoll Integration | [ATA SIEM-Protokoll Referenz](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a>Überwachungsprotokollierung muss aktiviert sein

Stellen Sie sicher, dass die Überwachungsprotokollierung aktiviert ist, bevor Sie die SIEM-Server Integration konfigurieren. 

- Für SharePoint Online, OneDrive for Business und Azure Active Directory [ist die Überwachungsprotokollierung im Security _AMP_ Compliance Center aktiviert](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).

- Für Exchange Online [wird die Überwachungsprotokollierung mit Windows PowerShell aktiviert](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).
 
## <a name="see-also"></a>Siehe auch

[Cloudakzeptanz und Hybridlösungen](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[Testumgebungsanleitungen (TLGs) zur Cloudakzeptanz](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


