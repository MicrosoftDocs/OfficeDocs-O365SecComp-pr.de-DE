---
title: Office 365 Bedrohungs Ermittlung und-Antwort
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/18/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 32405da5-bee1-4a4b-82e5-8399df94c512
ms.collection:
- M365-security-compliance
description: Erfahren Sie, wie Threat Intelligence-Funktionen in Office 365 Advanced Threat Protection Sie bei der Suche nach Bedrohungen für Ihre Organisation unterstützen, auf Schadsoftware, Phishing und andere Angriffe reagieren, die Office 365 in Ihrem Namen erkannt hat, und nach Bedrohungen suchen Indikatoren.
ms.openlocfilehash: 6f7e6e0a49bb4035458af2e9d7e45fd954a1f9fc
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265397"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="639f2-103">Office 365 Bedrohungs Ermittlung und-Antwort</span><span class="sxs-lookup"><span data-stu-id="639f2-103">Office 365 threat investigation and response</span></span>

<span data-ttu-id="639f2-104">Untersuchung und Antwortfunktionen für Bedrohungen in [office 365 Advanced Threat Protection](office-365-atp.md) helfen Sicherheitsanalysten und Administratoren, die Office 365-Benutzer Ihrer Organisation zu schützen, indem Sie:</span><span class="sxs-lookup"><span data-stu-id="639f2-104">Threat investigation and response capabilities in [Office 365 Advanced Threat Protection](office-365-atp.md) help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="639f2-105">Das erkennen, überwachen und verstehen von Angriffen ist einfach.</span><span class="sxs-lookup"><span data-stu-id="639f2-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="639f2-106">UnterStützung bei der schnellen Behebung von Bedrohungen in Exchange Online, SharePoint Online, OneDrive for Business und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="639f2-106">Helping to quickly address threats in Exchange Online, SharePoint Online, OneDrive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="639f2-107">Bereitstellen von Einblicken und Wissen zur Abwehr von Angriffen auf Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="639f2-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="639f2-108">Automatisierte Untersuchung und Antwort für kritische e-Mail-basierte Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="639f2-108">Automated investigation and response for critical email based threats</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="639f2-109">**Office 365 Advanced Threat Protection und Threat Investigation and Response (bisher bekannt als office 365 Threat Intelligence) sind jetzt office 365 Advanced Threat Protection Plan 2**, zusammen mit zusätzlichen Funktionen zum Schutz vor Bedrohungen, die in in enthalten sind. bestimmte Abonnements wie [microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5 usw. Wenn Ihre Organisation über ein Abonnement verfügt, das nicht Office 365 ATP umfasst, können Sie möglicherweise ATP als Add-on erwerben.</span><span class="sxs-lookup"><span data-stu-id="639f2-109">**Office 365 Advanced Threat Protection and Threat Investigation and Response (previously known as Office 365 Threat Intelligence) are now Office 365 Advanced Threat Protection Plan 2**, along with additional threat protection capabilities included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="639f2-110">Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="639f2-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="639f2-111">Was ändert sich?</span><span class="sxs-lookup"><span data-stu-id="639f2-111">What's changing?</span></span>

<span data-ttu-id="639f2-112">Zuvor war Office 365 Threat Intelligence in Abonnements wie Office 365 Enterprise E5 enthalten.</span><span class="sxs-lookup"><span data-stu-id="639f2-112">Formerly, Office 365 Threat Intelligence was included in subscriptions, such as Office 365 Enterprise E5.</span></span> <span data-ttu-id="639f2-113">Dies ist weiterhin der Fall, da Bedrohungs Untersuchungs-und-Antwortfunktionen jetzt Bestandteil von Office 365 Advanced Threat Protection Plan 2 (und dies ist in Office 365 Enterprise E5 enthalten).</span><span class="sxs-lookup"><span data-stu-id="639f2-113">This is still the case, as threat investigation and response capabilities are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="639f2-114">Außerdem war Office 365 Threat Intelligence früher als Add-on für Office 365 für Geschäftskunden erhältlich.</span><span class="sxs-lookup"><span data-stu-id="639f2-114">In addition, Office 365 Threat Intelligence was formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="639f2-115">Diese Funktionen sind jetzt in Office 365 Advanced Threat Protection Plan 2 (zusammen mit allen Features in Office 365 Advanced Threat Protection Plan 1) enthalten.</span><span class="sxs-lookup"><span data-stu-id="639f2-115">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (along with all the features in Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="639f2-116">Weitere Informationen finden Sie unter [Office 365 Advanced Threat Protection Plans and Pricing](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="639f2-116">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="639f2-117">Dies ist das folgende:</span><span class="sxs-lookup"><span data-stu-id="639f2-117">Here's what all this means:</span></span>

- <span data-ttu-id="639f2-118">**Wenn Ihre Organisation bereits über Office 365 Enterprise E5 verfügt**, verfügen Sie bereits über Advanced Threat Protection Plan 2, dazu gehören Untersuchungen und Reaktionsmöglichkeiten für Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="639f2-118">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span>

- <span data-ttu-id="639f2-119">**Wenn Ihre Organisation zuvor office 365 Threat Intelligence (aber nicht office 365 Advanced Threat Protection) als Add-on** für ein anderes Office 365-Abonnement hatte, haben Sie jetzt Office 365 Advanced Threat Protection Plan 2, und dies umfasst Untersuchung und Reaktionsmöglichkeiten für Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="639f2-119">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 2, and this includes threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="639f2-120">**Wenn Ihre Organisation zuvor office 365 Advanced Threat Protection (aber nicht office 365 Threat Intelligence) als Add-on** für ein anderes Office 365-Abonnement hatte, haben Sie jetzt Office 365 Advanced Threat Protection Plan 1.</span><span class="sxs-lookup"><span data-stu-id="639f2-120">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will now have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="639f2-121">Hierzu gehört auch Office 365 Advanced Threat Protection Plan 1 (nicht jedoch Bedrohungen für die Untersuchung und Antwort).</span><span class="sxs-lookup"><span data-stu-id="639f2-121">This includes Office 365 Advanced Threat Protection Plan 1, (but not threat investigation and response capabilities).</span></span>

<span data-ttu-id="639f2-122">Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span><span class="sxs-lookup"><span data-stu-id="639f2-122">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigation-and-response-capabilities"></a><span data-ttu-id="639f2-123">Erste Schritte mit den Möglichkeiten zur Bedrohungsanalyse und-Antwort</span><span class="sxs-lookup"><span data-stu-id="639f2-123">Get started with threat investigation and response capabilities</span></span>

<span data-ttu-id="639f2-124">Verwenden Sie die folgenden Ressourcen, um mehr über die Möglichkeiten der Bedrohung bei der Untersuchung und Antwort in Office 365 zu erfahren, und wie Sie Sie verwenden können, um die Sicherheit von Personen in Ihrer Organisation zu schützen.</span><span class="sxs-lookup"><span data-stu-id="639f2-124">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="639f2-125">[Erste Schritte bei der Bedrohungsanalyse und-Antwort](get-started-with-ti.md) (dazu gehören Informationen zu den erforderlichen Rollen)</span><span class="sxs-lookup"><span data-stu-id="639f2-125">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="639f2-126">Informationen zu Threat Tracker – neu und bemerkenswert</span><span class="sxs-lookup"><span data-stu-id="639f2-126">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)

- [<span data-ttu-id="639f2-127">Automatisierte Untersuchung und Antwort (AIR) mit Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="639f2-127">Automated Investigation and Response (AIR) with Office 365 Threat Intelligence</span></span>](automated-investigation-response-office.md)

- [<span data-ttu-id="639f2-128">Verwenden des Bedrohungs-Explorers &amp; im Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="639f2-128">Use Threat Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)
    
- [<span data-ttu-id="639f2-129">Suchen und Untersuchen von bösartigen E-Mails, die zugestellt wurden</span><span class="sxs-lookup"><span data-stu-id="639f2-129">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="639f2-130">Verwenden des anGriffs Simulators</span><span class="sxs-lookup"><span data-stu-id="639f2-130">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="639f2-131">Integrieren von Bedrohungs Ermittlung und-Antwort mit Windows Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="639f2-131">Integrate Threat Investigation and Response with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="639f2-132">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="639f2-132">Related topics</span></span>

[<span data-ttu-id="639f2-133">Ansichten des Sicherheitsrisiken-Explorers</span><span class="sxs-lookup"><span data-stu-id="639f2-133">Threat Explorer views</span></span>](threat-explorer-views.md)

[<span data-ttu-id="639f2-134">Schutz vor Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="639f2-134">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="639f2-135">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="639f2-135">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="639f2-136">Berechtigungen im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="639f2-136">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 
