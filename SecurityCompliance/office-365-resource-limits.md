---
title: Grenzwerte für Office 365-Ressource
ms.author: robmazz
author: robmazz
manager: laurawi
ms.date: 8/21/2018
audience: ITPro
ms.topic: article
ms.service: Office 365 Administration
localization_priority: None
search.appverid:
- MET150
ms.collection: Strat_O365_Enterprise
description: 'Zusammenfassung: Informationen zu Ressourcen für die verschiedenen Komponenten von Office 365 beschränkt.'
ms.openlocfilehash: a2e7ef42f9bf224363f3b10a5e450d6127f11585
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22530116"
---
# <a name="resource-limits"></a><span data-ttu-id="55002-103">Ressourcengrenzen</span><span class="sxs-lookup"><span data-stu-id="55002-103">Resource Limits</span></span>

<span data-ttu-id="55002-p101">Verwenden von Kontingenten (Grenzwerte) und der Einschränkung ist Ressourcengrenzen durchgesetzt. Azure Active Directory und der einzelnen Office 365-Dienste verwenden beide. Grenzwerte für dienstspezifische werden und mit der Zeit ändern, wie die neuen Funktionen hinzugefügt werden. Ausführliche auf die aktuellen Grenzwerte für die verschiedenen Dienste finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="55002-p101">Resource limits are enforced using quotas (limits) and throttling. Azure Active Directory and the individual Office 365 services use both. Limits are service-specific and change over time as new capabilities are added. For details on the current limits for the various services, see the following topics:</span></span>
- [<span data-ttu-id="55002-108">Azure Active Directory Service Grenzen und Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="55002-108">Azure Active Directory service limits and restrictions</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [<span data-ttu-id="55002-109">Exchange Online-Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="55002-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [<span data-ttu-id="55002-110">Beschränkungen von Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="55002-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="55002-111">SharePoint Online softwarebeschränkungen und-Grenzen</span><span class="sxs-lookup"><span data-stu-id="55002-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="55002-112">Skype für Business-Grenzwerte</span><span class="sxs-lookup"><span data-stu-id="55002-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="55002-113">Yammer-REST-API und Rate-Grenzwerte</span><span class="sxs-lookup"><span data-stu-id="55002-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="55002-114">Maximale Dateigröße in Schlingern</span><span class="sxs-lookup"><span data-stu-id="55002-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="55002-p102">Zusätzlich zu diesen Grenzwerten werden mehrere einschränkungsmechanismen in der gesamten Azure Active Directory und Office 365 verwendet. Innerhalb des Dienstes Einschränkung ist besonders wichtig, wenn die Ressourcen des Umkreisnetzwerks in Microsoft Rechenzentren für die Breite Palette von Kunden optimiert sind, die die Dienste zu verwenden. Einschränkungsmechanismen umfassen:</span><span class="sxs-lookup"><span data-stu-id="55002-p102">In addition to these limits, several throttling mechanisms are used throughout Azure Active Directory and Office 365. Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services. Throttling mechanisms include:</span></span>
- <span data-ttu-id="55002-118">Azure Active Directory und Office 365-Features auf Benutzerebene Einschränkung, die die Anzahl der Transaktionen oder gleichzeitige Anrufe (durch Code- oder Skriptblock), die von einem einzelnen Benutzer ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="55002-118">Azure Active Directory and Office 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="55002-p103">Jeder Mandant bei der Erstellung des Mandanten wird eine standardmäßige Einschränkungsrichtlinie PowerShell zugewiesen. Diese Einstellungen wirken sich auf anderen Elementen, wie die maximale Anzahl von gleichzeitigen PowerShell-Sitzungen, die von einem Administrator der einzelnen geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="55002-p103">A default PowerShell throttling policy is assigned to each tenant at tenant creation. These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="55002-121">Jeder Exchange Online-Kunden ist eine Standardrichtlinie für die Exchange-Webdienste (EWS), die für EWS-Client-Vorgänge optimiert ist, und, die Einschränkung gilt für alle Outlook-Clients.</span><span class="sxs-lookup"><span data-stu-id="55002-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
