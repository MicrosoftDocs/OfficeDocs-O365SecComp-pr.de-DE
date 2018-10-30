---
title: Server-Integration mit Microsoft 365 SIEM
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.date: 10/29/2018
ms.service: o365-solutions
localization_priority: Normal
ms.collection: Ent_O365
ms.custom:
- Ent_Solutions
- SIEM
description: 'Zusammenfassung: Lesen Sie diesen Artikel, um eine Übersicht über SIEM-Server-Integration in Microsoft 365 erhalten.'
ms.openlocfilehash: bd512ca6d75928712e3444581a78610a0869123d
ms.sourcegitcommit: 63ed467fc3e1ab1ab9ee122df97c64737169834e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/30/2018
ms.locfileid: "25842681"
---
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a>SIEM-Server-Integration mit Microsoft-365-Diensten und Clientanwendungen

## <a name="overview"></a>Übersicht

Wenn Ihre Organisation einen Server Sicherheitsinformationen und Ereignis Management (SIEM) verwendet wird, oder wenn Sie beabsichtigen, einen Server SIEM bald erhalten möchten, Sie vielleicht, wie, die in Ihrer Microsoft 365, einschließlich Office 365 Enterprise integriert werden. Ob Sie einen Server SIEM benötigen, hängt von vielen Faktoren ab, wie etwa sicherheitsanforderungen Ihrer Organisation. Microsoft 365 bietet eine Vielzahl von Sicherheitsfeatures; jedoch wenn Ihre Organisation Inhalte und-Anwendungen lokal und in der Cloud (wie bei einer hybridbereitstellung Cloud) verfügt, sollten Sie das Hinzufügen eines Servers SIEM für extra Schutz. Oder, wenn Ihre Organisation vor allem strenge sicherheitsanforderungen, die erfüllt sein müssen verfügt, sollten Sie Ihre Umgebung einen SIEM Server hinzufügen.

## <a name="siem-server-integration-microsoft-365"></a>SIEM 365 Microsoft Server-integration

Ein Server SIEM empfangen von Daten aus einer Vielzahl von Microsoft-365-Dienste und Anwendungen. Die folgende Tabelle enthält verschiedene Microsoft-365-Dienste und Anwendungen zusammen mit SIEM Server Eingaben und, wo Sie weitere Informationen zu SIEM-Server-Integration. 

| Microsoft-365-Dienst oder die Anwendung | SIEM Server Eingaben | Weitere Ressourcen |
| --- | --- | --- |
| [Office 365 Advanced Threat Protection](office-365-atp.md) <br/>   oder   <br/>[Informationen zu Bedrohungen in Office 365](office-365-ti.md) | Überwachungsprotokolle | [Integration mit Office 365 Bedrohungsanalyse und erweiterte Threat Protection SIEM](siem-integration-with-office-365-ti.md) |
| [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | Protokoll-integration | [SIEM-Integration mit Microsoft Cloud App-Sicherheit](https://docs.microsoft.com/cloud-app-security/siem) |
| [Office 365 Cloud App Security](office-365-cas-overview.md) | Protokoll-integration | [Integrieren Ihres SIEM-Servers in Office 365 Cloud App Security](integrate-your-siem-server-with-office-365-cas.md) |
| [Windows Defender Advanced Threat Protection](https://docs.microsoft.com/windows/security/threat-protection/) | Protokoll-integration | [Ziehen Sie Warnungen zu Ihrer SIEM-tools](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| [Azure-Sicherheitscenter](https://docs.microsoft.com/azure/security-center/security-center-intro) (Erkennung und Schutz vor Angriffen) | Benachrichtigungen | [Exportieren von Azure Security-Daten in SIEM - Pipelinekonfiguration - Vorschau](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [Azure Active Directory-Schutz](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | Überwachungsprotokolle | [Integrieren von Azure Active Directory-Überwachungsprotokolle](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [Azure erweiterte Bedrohung Analytics](https://docs.microsoft.com/azure/security/azure-threat-detection) | Protokoll-integration | [ATA SIEM-Protokoll (engl.)](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a>Überwachungsprotokollierung muss aktiviert sein

Stellen Sie sicher, dass die überwachungsprotokollierung vor dem Konfigurieren der SIEM-Server-Integration aktiviert ist. 

- Für SharePoint Online, OneDrive for Business und Azure Active Directory [überwachungsprotokollierung im Compliance Center & Sicherheit aktiviert ist](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).

- Für Exchange Online, [überwachungsprotokollierung mit Windows PowerShell aktiviert ist](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).
 
## <a name="see-also"></a>Siehe auch

[Cloudakzeptanz und Hybridlösungen](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[Testumgebungsanleitungen (TLGs) zur Cloudakzeptanz](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)


