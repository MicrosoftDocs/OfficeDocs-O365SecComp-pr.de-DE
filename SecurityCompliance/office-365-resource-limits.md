---
title: Office 365-Ressourcengrenzwerte
ms.author: robmazz
author: robmazz
manager: laurawi
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.collection:
- Strat_O365_IP
- M365-security-compliance
description: 'Zusammenfassung: Informationen zu Ressourcen Grenzwerten für die verschiedenen Anwendungen in Office 365.'
ms.openlocfilehash: d4315923ea1ab09e2e7651fb2fcaddb085871d4d
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262407"
---
# <a name="resource-limits"></a><span data-ttu-id="fae65-103">Ressourcenbeschränkungen</span><span class="sxs-lookup"><span data-stu-id="fae65-103">Resource Limits</span></span>

<span data-ttu-id="fae65-104">Ressourcengrenzwerte werden mithilfe von Kontingenten (Limits) und Einschränkung erzwungen.</span><span class="sxs-lookup"><span data-stu-id="fae65-104">Resource limits are enforced using quotas (limits) and throttling.</span></span> <span data-ttu-id="fae65-105">Azure Active Directory und die einzelnen Office 365-Dienste verwenden beides.</span><span class="sxs-lookup"><span data-stu-id="fae65-105">Azure Active Directory and the individual Office 365 services use both.</span></span> <span data-ttu-id="fae65-106">Grenzwertesind Dienst spezifisch und ändern sich im Lauf der Zeit, wenn neue Funktionen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fae65-106">Limits are service-specific and change over time as new capabilities are added.</span></span> <span data-ttu-id="fae65-107">Details zu den aktuellen Grenzwerten für die verschiedenen Dienste finden Sie in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="fae65-107">For details on the current limits for the various services, see the following topics:</span></span>
- [<span data-ttu-id="fae65-108">Grenzwerte und Einschränkungen des Azure Active Directory-Diensts</span><span class="sxs-lookup"><span data-stu-id="fae65-108">Azure Active Directory service limits and restrictions</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn764971.aspx)
- [<span data-ttu-id="fae65-109">Exchange Online-Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="fae65-109">Exchange Online Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-limits.aspx)
- [<span data-ttu-id="fae65-110">Beschränkungen von Exchange Online Protection</span><span class="sxs-lookup"><span data-stu-id="fae65-110">Exchange Online Protection Limits</span></span>](https://technet.microsoft.com/en-us/library/exchange-online-protection-limits.aspx)
- [<span data-ttu-id="fae65-111">Grenzen und Grenzen von SharePoint Online-Software</span><span class="sxs-lookup"><span data-stu-id="fae65-111">SharePoint Online software boundaries and limits</span></span>](https://support.office.com/article/SharePoint-Online-software-boundaries-and-limits-8F34FF47-B749-408B-ABC0-B605E1F6D498)
- [<span data-ttu-id="fae65-112">Skype for Business-Grenzwerte</span><span class="sxs-lookup"><span data-stu-id="fae65-112">Skype for Business Limits</span></span>](https://technet.microsoft.com/en-us/library/skype-for-business-online-limits.aspx)
- [<span data-ttu-id="fae65-113">Jammern-REST-API und Raten Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="fae65-113">Yammer REST API and Rate Limits</span></span>](https://developer.yammer.com/docs/rest-api-rate-limits)
- [<span data-ttu-id="fae65-114">Dateigrößenbeschränkungen in Sway</span><span class="sxs-lookup"><span data-stu-id="fae65-114">File Size Limits in Sway</span></span>](https://support.office.com/article/File-size-limits-in-Sway-4db21bc6-b42b-499f-9272-66e089db109f)

<span data-ttu-id="fae65-115">Zusätzlich zu diesen Grenzwerten werden in Azure Active Directory und Office 365 mehrere Einschränkungs Mechanismen verwendet.</span><span class="sxs-lookup"><span data-stu-id="fae65-115">In addition to these limits, several throttling mechanisms are used throughout Azure Active Directory and Office 365.</span></span> <span data-ttu-id="fae65-116">Die Einschränkung innerhalb des Diensts ist besonders wichtig, da die Netzwerkressourcen in Microsoft-Rechenzentren für die breite Palette von Kunden optimiert sind, die die Dienste nutzen.</span><span class="sxs-lookup"><span data-stu-id="fae65-116">Throttling within the service is especially important, given that network resources in Microsoft's datacenters are optimized for the broad set of customers that use the services.</span></span> <span data-ttu-id="fae65-117">Zu den Einschränkungs Mechanismen gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fae65-117">Throttling mechanisms include:</span></span>
- <span data-ttu-id="fae65-118">Azure Active Directory und Office 365 verfügen über Einschränkungen auf Benutzerebene, die die Anzahl von Transaktionen oder gleichzeitigen anrufen (durch Skripts oder Code) begrenzen, die von einem einzelnen Benutzer ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="fae65-118">Azure Active Directory and Office 365 feature user-level throttling, which limit the number of transactions or concurrent calls (by script or code) that can be performed by a single user.</span></span>
- <span data-ttu-id="fae65-119">Jedem Mandanten wird bei der Mandanten Erstellung eine standardmäßige PowerShell-Einschränkungsrichtlinie zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="fae65-119">A default PowerShell throttling policy is assigned to each tenant at tenant creation.</span></span> <span data-ttu-id="fae65-120">Diese Einstellungen wirken sich auf andere Elemente aus, wie beispielsweise die maximale Anzahl gleichzeitiger PowerShell-Sitzungen, die von einem einzelnen Administrator geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="fae65-120">These settings affect other items, such as the maximum number of simultaneous PowerShell sessions that can be opened by a single administrator.</span></span>
- <span data-ttu-id="fae65-121">Jeder Exchange Online-Kunde verfügt über eine Standardrichtlinie für Exchange-webDienste (EWS), die für EWS-Client Vorgänge optimiert ist, sowie eine Drosselung, die für alle Outlook-Clients gilt.</span><span class="sxs-lookup"><span data-stu-id="fae65-121">Each Exchange Online customer has a default Exchange Web Services (EWS) policy that is tuned for EWS client operations, and throttling that applies to all Outlook clients.</span></span>
