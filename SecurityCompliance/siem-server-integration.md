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
# <a name="siem-server-integration-with-microsoft-365-services-and-applications"></a><span data-ttu-id="e2b76-103">SIEM-Server-Integration mit Microsoft-365-Diensten und Clientanwendungen</span><span class="sxs-lookup"><span data-stu-id="e2b76-103">SIEM server integration with Microsoft 365 services and applications</span></span>

## <a name="overview"></a><span data-ttu-id="e2b76-104">Übersicht</span><span class="sxs-lookup"><span data-stu-id="e2b76-104">Overview</span></span>

<span data-ttu-id="e2b76-p101">Wenn Ihre Organisation einen Server Sicherheitsinformationen und Ereignis Management (SIEM) verwendet wird, oder wenn Sie beabsichtigen, einen Server SIEM bald erhalten möchten, Sie vielleicht, wie, die in Ihrer Microsoft 365, einschließlich Office 365 Enterprise integriert werden. Ob Sie einen Server SIEM benötigen, hängt von vielen Faktoren ab, wie etwa sicherheitsanforderungen Ihrer Organisation. Microsoft 365 bietet eine Vielzahl von Sicherheitsfeatures; jedoch wenn Ihre Organisation Inhalte und-Anwendungen lokal und in der Cloud (wie bei einer hybridbereitstellung Cloud) verfügt, sollten Sie das Hinzufügen eines Servers SIEM für extra Schutz. Oder, wenn Ihre Organisation vor allem strenge sicherheitsanforderungen, die erfüllt sein müssen verfügt, sollten Sie Ihre Umgebung einen SIEM Server hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e2b76-p101">If your organization is using a Security Information and Event Management (SIEM) server, or if you are planning to get a SIEM server soon, you might be wondering how that'll integrate with your Microsoft 365, including Office 365 Enterprise. Whether you need a SIEM server depends on many factors, such as your organization's security requirements. Microsoft 365 offers a variety of security features; however, if your organization has content and applications on premises and in the cloud (as in the case of a hybrid cloud deployment), you might consider adding a SIEM server for extra protection. Or, if your organization has particularly stringent security requirements you must meet, you might consider adding a SIEM server to your environment.</span></span>

## <a name="siem-server-integration-microsoft-365"></a><span data-ttu-id="e2b76-109">SIEM 365 Microsoft Server-integration</span><span class="sxs-lookup"><span data-stu-id="e2b76-109">SIEM server integration Microsoft 365</span></span>

<span data-ttu-id="e2b76-p102">Ein Server SIEM empfangen von Daten aus einer Vielzahl von Microsoft-365-Dienste und Anwendungen. Die folgende Tabelle enthält verschiedene Microsoft-365-Dienste und Anwendungen zusammen mit SIEM Server Eingaben und, wo Sie weitere Informationen zu SIEM-Server-Integration.</span><span class="sxs-lookup"><span data-stu-id="e2b76-p102">A SIEM server can receive data from a wide variety of Microsoft 365 services and applications. The following table lists several Microsoft 365 services and applications along with SIEM server inputs and where to go to learn more about SIEM server integration.</span></span> 

| <span data-ttu-id="e2b76-112">Microsoft-365-Dienst oder die Anwendung</span><span class="sxs-lookup"><span data-stu-id="e2b76-112">Microsoft 365 Service or Application</span></span> | <span data-ttu-id="e2b76-113">SIEM Server Eingaben</span><span class="sxs-lookup"><span data-stu-id="e2b76-113">SIEM server inputs</span></span> | <span data-ttu-id="e2b76-114">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2b76-114">Resources to learn more</span></span> |
| --- | --- | --- |
| [<span data-ttu-id="e2b76-115">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e2b76-115">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md) <br/>   <span data-ttu-id="e2b76-116">oder</span><span class="sxs-lookup"><span data-stu-id="e2b76-116">or</span></span>   <br/>[<span data-ttu-id="e2b76-117">Informationen zu Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="e2b76-117">Office 365 Threat Intelligence</span></span>](office-365-ti.md) | <span data-ttu-id="e2b76-118">Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="e2b76-118">Audit logs</span></span> | [<span data-ttu-id="e2b76-119">Integration mit Office 365 Bedrohungsanalyse und erweiterte Threat Protection SIEM</span><span class="sxs-lookup"><span data-stu-id="e2b76-119">SIEM integration with Office 365 Threat Intelligence and Advanced Threat Protection</span></span>](siem-integration-with-office-365-ti.md) |
| [<span data-ttu-id="e2b76-120">Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="e2b76-120">Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/what-is-cloud-app-security) | <span data-ttu-id="e2b76-121">Protokoll-integration</span><span class="sxs-lookup"><span data-stu-id="e2b76-121">Log integration</span></span> | [<span data-ttu-id="e2b76-122">SIEM-Integration mit Microsoft Cloud App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="e2b76-122">SIEM integration with Microsoft Cloud App Security</span></span>](https://docs.microsoft.com/cloud-app-security/siem) |
| [<span data-ttu-id="e2b76-123">Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="e2b76-123">Office 365 Cloud App Security</span></span>](office-365-cas-overview.md) | <span data-ttu-id="e2b76-124">Protokoll-integration</span><span class="sxs-lookup"><span data-stu-id="e2b76-124">Log integration</span></span> | [<span data-ttu-id="e2b76-125">Integrieren Ihres SIEM-Servers in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="e2b76-125">Integrate your SIEM server with Office 365 Cloud App Security</span></span>](integrate-your-siem-server-with-office-365-cas.md) |
| [<span data-ttu-id="e2b76-126">Windows Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="e2b76-126">Windows Defender Advanced Threat Protection</span></span>](https://docs.microsoft.com/windows/security/threat-protection/) | <span data-ttu-id="e2b76-127">Protokoll-integration</span><span class="sxs-lookup"><span data-stu-id="e2b76-127">Log integration</span></span> | [<span data-ttu-id="e2b76-128">Ziehen Sie Warnungen zu Ihrer SIEM-tools</span><span class="sxs-lookup"><span data-stu-id="e2b76-128">Pull alerts to your SIEM tools</span></span>](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/configure-siem-windows-defender-advanced-threat-protection) |
| <span data-ttu-id="e2b76-129">[Azure-Sicherheitscenter](https://docs.microsoft.com/azure/security-center/security-center-intro) (Erkennung und Schutz vor Angriffen)</span><span class="sxs-lookup"><span data-stu-id="e2b76-129">[Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-intro) (Threat Protection and Threat Detection)</span></span> | <span data-ttu-id="e2b76-130">Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="e2b76-130">Alerts</span></span> | [<span data-ttu-id="e2b76-131">Exportieren von Azure Security-Daten in SIEM - Pipelinekonfiguration - Vorschau</span><span class="sxs-lookup"><span data-stu-id="e2b76-131">Azure Security data export to SIEM - Pipeline Configuration - Preview</span></span>](https://docs.microsoft.com/azure/security-center/security-center-export-data-to-siem) |
| [<span data-ttu-id="e2b76-132">Azure Active Directory-Schutz</span><span class="sxs-lookup"><span data-stu-id="e2b76-132">Azure Active Directory Identity Protection</span></span>](https://docs.microsoft.com/azure/active-directory/identity-protection/overview) | <span data-ttu-id="e2b76-133">Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="e2b76-133">Audit logs</span></span> | [<span data-ttu-id="e2b76-134">Integrieren von Azure Active Directory-Überwachungsprotokolle</span><span class="sxs-lookup"><span data-stu-id="e2b76-134">Integrate Azure Active Directory audit logs</span></span>](https://docs.microsoft.com/azure/security/security-azure-log-integration-ad) |
| [<span data-ttu-id="e2b76-135">Azure erweiterte Bedrohung Analytics</span><span class="sxs-lookup"><span data-stu-id="e2b76-135">Azure Advanced Threat Analytics</span></span>](https://docs.microsoft.com/azure/security/azure-threat-detection) | <span data-ttu-id="e2b76-136">Protokoll-integration</span><span class="sxs-lookup"><span data-stu-id="e2b76-136">Log integration</span></span> | [<span data-ttu-id="e2b76-137">ATA SIEM-Protokoll (engl.)</span><span class="sxs-lookup"><span data-stu-id="e2b76-137">ATA SIEM log reference</span></span>](https://docs.microsoft.com/advanced-threat-analytics/cef-format-sa) |

## <a name="audit-logging-must-be-turned-on"></a><span data-ttu-id="e2b76-138">Überwachungsprotokollierung muss aktiviert sein</span><span class="sxs-lookup"><span data-stu-id="e2b76-138">Audit logging must be turned on</span></span>

<span data-ttu-id="e2b76-139">Stellen Sie sicher, dass die überwachungsprotokollierung vor dem Konfigurieren der SIEM-Server-Integration aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e2b76-139">Make sure audit logging is turned on before you configure SIEM server integration.</span></span> 

- <span data-ttu-id="e2b76-140">Für SharePoint Online, OneDrive for Business und Azure Active Directory [überwachungsprotokollierung im Compliance Center & Sicherheit aktiviert ist](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span><span class="sxs-lookup"><span data-stu-id="e2b76-140">For SharePoint Online, OneDrive for Business, and Azure Active Directory, [audit logging is turned on in the Security & Compliance Center](https://docs.microsoft.com/office365/securitycompliance/turn-audit-log-search-on-or-off).</span></span>

- <span data-ttu-id="e2b76-141">Für Exchange Online, [überwachungsprotokollierung mit Windows PowerShell aktiviert ist](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span><span class="sxs-lookup"><span data-stu-id="e2b76-141">For Exchange Online, [audit logging is turned on with Windows PowerShell](https://docs.microsoft.com/office365/securitycompliance/enable-mailbox-auditing).</span></span>
 
## <a name="see-also"></a><span data-ttu-id="e2b76-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2b76-142">See Also</span></span>

[<span data-ttu-id="e2b76-143">Cloudakzeptanz und Hybridlösungen</span><span class="sxs-lookup"><span data-stu-id="e2b76-143">Cloud adoption and hybrid solutions</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-and-hybrid-solutions)
  
[<span data-ttu-id="e2b76-144">Testumgebungsanleitungen (TLGs) zur Cloudakzeptanz</span><span class="sxs-lookup"><span data-stu-id="e2b76-144">Cloud adoption Test Lab Guides (TLGs)</span></span>](https://docs.microsoft.com/office365/enterprise/cloud-adoption-test-lab-guides-tlgs)

