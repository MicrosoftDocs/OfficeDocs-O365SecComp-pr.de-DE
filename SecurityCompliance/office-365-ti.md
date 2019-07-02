---
title: Untersuchung von und Antwort auf Bedrohungen in Office 365
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/18/2019
audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Sie mithilfe von Threat Intelligence-Funktionen in Office 365 Advanced Threat Protection Sicherheitsrisiken in Ihrer Organisation erforschen, auf Schadsoftware, Phishing und andere Angriffe reagieren können, die Office 365 in Ihrem Namen erkannt hat, und nach Bedrohungen suchen. Indikatoren.
ms.openlocfilehash: c8b0815368e80151f8ee55161b9bcbaa98065228
ms.sourcegitcommit: b9d8a43cb3afcdc8820bc9470c5707eff8fc6616
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2019
ms.locfileid: "34852809"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="8a667-103">Untersuchung von und Antwort auf Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="8a667-103">Office 365 threat investigation and response</span></span>

<span data-ttu-id="8a667-104">Untersuchung und Antwortfunktionen für Bedrohungen in [Office 365 Advanced Threat Protection](office-365-atp.md) helfen Sicherheitsanalysten und Administratoren, die Office 365 Benutzer Ihrer Organisation zu schützen, indem Sie:</span><span class="sxs-lookup"><span data-stu-id="8a667-104">Threat investigation and response capabilities in [Office 365 Advanced Threat Protection](office-365-atp.md) help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="8a667-105">Einfaches identifizieren, überwachen und verstehen von Angriffen</span><span class="sxs-lookup"><span data-stu-id="8a667-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="8a667-106">Unterstützung bei der schnellen Adressierung von Bedrohungen in Exchange Online, SharePoint Online, OneDrive für Unternehmen und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8a667-106">Helping to quickly address threats in Exchange Online, SharePoint Online, OneDrive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="8a667-107">Bereitstellen von Einblicken und wissen, um Angriffe gegen Ihre Organisation zu verhindern</span><span class="sxs-lookup"><span data-stu-id="8a667-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="8a667-108">Automatische Untersuchung und Reaktion auf kritische e-Mail-basierte Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="8a667-108">Automated investigation and response for critical email based threats</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="8a667-109">**Office 365 Advanced Threat Protection und Threat-Untersuchung und-Reaktion (bisher als Office 365 Threat Intelligence bezeichnet) sind jetzt Office 365 Advanced Threat Protection Plan 2**, zusammen mit zusätzlichen Funktionen zum Schutz vor Bedrohungen, die in in enthalten sind. bestimmte Abonnements wie [Microsoft 365 E5](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 E5, Office 365 A5 usw. Wenn Ihre Organisation über ein Abonnement verfügt, das nicht Office 365 ATP umfasst, können Sie ATP als Add-on möglicherweise erwerben.</span><span class="sxs-lookup"><span data-stu-id="8a667-109">**Office 365 Advanced Threat Protection and Threat Investigation and Response (previously known as Office 365 Threat Intelligence) are now Office 365 Advanced Threat Protection Plan 2**, along with additional threat protection capabilities included in in certain subscriptions, such as [Microsoft 365 E5](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 E5, Office 365 A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="8a667-110">Weitere Informationen finden Sie unter [Office 365 Advanced Threat Protection-Pläne und-Preise](https://products.office.com/exchange/advance-threat-protection) und der [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="8a667-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="8a667-111">Was ändert sich?</span><span class="sxs-lookup"><span data-stu-id="8a667-111">What's changing?</span></span>

<span data-ttu-id="8a667-112">Früher wurde Office 365 Threat Intelligence in Abonnements wie Office 365 E5 aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="8a667-112">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 E5.</span></span> <span data-ttu-id="8a667-113">Dies ist nach wie vor der Fall, da die Funktionen zur Untersuchung und Reaktion von Bedrohungen nun Teil Office 365 Advanced Threat Protection Plan 2 sind (und dies ist in Office 365 E5 enthalten).</span><span class="sxs-lookup"><span data-stu-id="8a667-113">This is still the case, as threat investigation and response capabilities are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 E5).</span></span> 

<span data-ttu-id="8a667-114">Darüber hinaus war Office 365 Threat Intelligence früher als Add-on für Office 365 für Unternehmen-Kunden erhältlich.</span><span class="sxs-lookup"><span data-stu-id="8a667-114">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="8a667-115">Diese Funktionen sind nun in Office 365 Advanced Threat Protection Plan 2 enthalten (zusammen mit allen Features in Office 365 Advanced Threat Protection-Plan 1).</span><span class="sxs-lookup"><span data-stu-id="8a667-115">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (along with all the features in Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="8a667-116">Weitere Informationen finden Sie unter [Office 365 Advanced Threat Protection-Pläne und-Preise](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="8a667-116">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="8a667-117">Dies bedeutet Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8a667-117">Here's what all this means:</span></span>

- <span data-ttu-id="8a667-118">**Wenn Ihre Organisation bereits über Office 365 E5 verfügt**, verfügen Sie bereits über Advanced Threat Protection Plan 2, und dies umfasst die Untersuchung und Antwortfunktionen für Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="8a667-118">**If your organization already has Office 365 E5**, then you already have Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span>

- <span data-ttu-id="8a667-119">**Wenn Ihre Organisation zuvor Office 365 Threat Intelligence (aber nicht Office 365 Advanced Threat Protection) als Add-on** zu einem anderen Office 365 Abonnement verwendet hat, haben Sie nun Office 365 Advanced Threat Protection Plan 2, dazu gehören Funktionen für die Ermittlung und Reaktion auf Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="8a667-119">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="8a667-120">**Wenn Ihre Organisation zuvor Office 365 Advanced Threat Protection (aber nicht Office 365 Threat Intelligence) als Add-on** zu einem anderen Office 365-Abonnement hatte, haben Sie nun Office 365 Advanced Threat Protection Plan 1.</span><span class="sxs-lookup"><span data-stu-id="8a667-120">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="8a667-121">Hierzu gehören Office 365 Advanced Threat Protection-Plan 1 (aber keine Bedrohungs Ermittlungs-und-Antwortfunktionen).</span><span class="sxs-lookup"><span data-stu-id="8a667-121">This includes Office 365 Advanced Threat Protection Plan 1, (but not threat investigation and response capabilities).</span></span>

<span data-ttu-id="8a667-122">Weitere Informationen finden Sie unter [Office 365 Advanced Threat Protection-Pläne und-Preise](https://products.office.com/exchange/advance-threat-protection) und der [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span><span class="sxs-lookup"><span data-stu-id="8a667-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigation-and-response-capabilities"></a><span data-ttu-id="8a667-123">Erste Schritte mit Funktionen zur Ermittlung und Reaktion auf Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="8a667-123">Get started with threat investigation and response capabilities</span></span>

<span data-ttu-id="8a667-124">Verwenden Sie die folgenden Ressourcen, um mehr über die Funktionen zur Untersuchung und Reaktion auf Bedrohungen in Office 365 zu erfahren, und wie Sie Sie verwenden können, um Personen in Ihrer Organisation sicherer zu halten.</span><span class="sxs-lookup"><span data-stu-id="8a667-124">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="8a667-125">[Erste Schritte mit der Untersuchung und Reaktion auf Bedrohungen](get-started-with-ti.md) (Dies umfasst Informationen zu erforderlichen Rollen)</span><span class="sxs-lookup"><span data-stu-id="8a667-125">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="8a667-126">Informationen zu Threat Tracker – neu und bemerkenswert</span><span class="sxs-lookup"><span data-stu-id="8a667-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)

- [<span data-ttu-id="8a667-127">Sparen Sie Zeit und Aufwand mit automatisierten Untersuchungen und Antwortfunktionen (Air)</span><span class="sxs-lookup"><span data-stu-id="8a667-127">Save time and effort with Automated Investigation and Response (AIR) capabilities</span></span>](automated-investigation-response-office.md)

- [<span data-ttu-id="8a667-128">Verwenden Sie Threat Explorer (oder Echtzeiterkennung), um bösartige Inhalte in e-Mails und Dateien zu identifizieren und zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="8a667-128">Use Threat Explorer (or real-time detections) to identify and investigate malicious content in email and files</span></span>](threat-explorer.md)
    
- [<span data-ttu-id="8a667-129">Suchen und Untersuchen von bösartigen E-Mails, die zugestellt wurden</span><span class="sxs-lookup"><span data-stu-id="8a667-129">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="8a667-130">Verwenden des Angriffs Simulators zur Simulation von Angriffen und zur Sensibilisierung der Benutzer</span><span class="sxs-lookup"><span data-stu-id="8a667-130">Use Attack Simulator to simulate attacks and increase user awareness</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="8a667-131">Integrieren der Funktionen zur Ermittlung und Reaktion von Bedrohungen mit Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8a667-131">Integrate Threat Investigation and Response capabilities with Microsoft Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="8a667-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="8a667-132">Related topics</span></span>

[<span data-ttu-id="8a667-133">Ansichten des Sicherheitsrisiken-Explorers</span><span class="sxs-lookup"><span data-stu-id="8a667-133">Threat Explorer views</span></span>](threat-explorer-views.md)

[<span data-ttu-id="8a667-134">Schutz vor Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="8a667-134">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="8a667-135">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="8a667-135">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="8a667-136">Berechtigungen im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="8a667-136">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 
