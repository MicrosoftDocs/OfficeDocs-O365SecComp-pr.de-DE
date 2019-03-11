---
title: Office 365 Bedrohungs Ermittlung und-Antwort
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/09/2019
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
description: Erfahren Sie, wie Threat Intelligence-Funktionen in Advanced Threat Protection Sie bei der Suche nach Bedrohungen für Ihre Organisation unterstützen, auf Schadsoftware, Phishing und andere Angriffe reagieren können, die Office 365 in Ihrem Namen erkannt hat, und nach Bedrohungs Indikatoren suchen.
ms.openlocfilehash: 1d076ed6ca48b8423ad92d5ea71bd87167b8519a
ms.sourcegitcommit: 74ad22a5c6c3c9d9324f0f97070909e323a4e9cf
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/11/2019
ms.locfileid: "30523999"
---
# <a name="office-365-threat-investigation-and-response"></a><span data-ttu-id="03210-103">Office 365 Bedrohungs Ermittlung und-Antwort</span><span class="sxs-lookup"><span data-stu-id="03210-103">Office 365 Threat Investigation and Response</span></span>

<span data-ttu-id="03210-104">Untersuchung und Antwortfunktionen für Bedrohungen in Office 365 Advanced Threat Protection helfen Sicherheitsanalysten und Administratoren, die Office 365-Benutzer Ihrer Organisation zu schützen, indem Sie:</span><span class="sxs-lookup"><span data-stu-id="03210-104">Threat investigation and response capabilities in Office 365 Advanced Threat Protection help security analysts and administrators protect their organization's Office 365 users by:</span></span>
  
1. <span data-ttu-id="03210-105">Das erkennen, überwachen und verstehen von Angriffen ist einfach.</span><span class="sxs-lookup"><span data-stu-id="03210-105">Making it easy to identify, monitor and understand attacks</span></span>
    
2. <span data-ttu-id="03210-106">UnterStützung bei der schnellen Behebung von Bedrohungen in Exchange Online, SharePoint Online, einem Laufwerk für Unternehmen und Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="03210-106">Helping to quickly address threats in Exchange Online, SharePoint Online, One Drive for Business and Microsoft Teams</span></span>
    
3. <span data-ttu-id="03210-107">Bereitstellen von Einblicken und Wissen zur Abwehr von Angriffen auf Ihre Organisation</span><span class="sxs-lookup"><span data-stu-id="03210-107">Providing insights and knowledge to help prevent attacks against their organization</span></span>

4. <span data-ttu-id="03210-108">Automatisierte Untersuchung und Antwort für kritische e-Mail-basierte Bedrohungen</span><span class="sxs-lookup"><span data-stu-id="03210-108">Automated investigation and response for critical email based threats</span></span>
    
> [!IMPORTANT]
> <span data-ttu-id="03210-109">**Office 365 Bedrohungs Ermittlung und-Antworten (bisher bekannt als office 365 Threat Intelligence) ist jetzt Bestandteil von Advanced Threat Protection Plan 2 in office 365**, der in bestimmten Abonnements wie [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home)enthalten ist. [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5 usw. Wenn Ihre Organisation über ein Abonnement verfügt, das nicht Office 365 ATP umfasst, können Sie möglicherweise ATP als Add-on erwerben.</span><span class="sxs-lookup"><span data-stu-id="03210-109">**Office 365 THreat Investigation and Responses (previously known as Office 365 Threat Intelligence) is now part of in Office 365 Advanced Threat Protection Plan 2**, which is included in in certain subscriptions, such as [Microsoft 365 Enterprise](https://www.microsoft.com/microsoft-365/enterprise/home), [Microsoft 365 Business](https://www.microsoft.com/microsoft-365/business), Office 365 Enterprise E5, Office 365 Education A5, etc. If your organization has a subscription that does not include Office 365 ATP, you can potentially purchase ATP as an add-on.</span></span> <span data-ttu-id="03210-110">Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span><span class="sxs-lookup"><span data-stu-id="03210-110">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp).</span></span> 
  
## <a name="whats-changing"></a><span data-ttu-id="03210-111">Was ändert sich?</span><span class="sxs-lookup"><span data-stu-id="03210-111">What's changing?</span></span>

<span data-ttu-id="03210-112">Früher waren Office 365 Threat Investigation and Response-Funktionen in Abonnements enthalten, wie Office 365 Enterprise E5.</span><span class="sxs-lookup"><span data-stu-id="03210-112">Formerly, Office 365 Threat investigation and responses capabilities were included in subscriptions, such as Office 365 Enterprise E5.</span></span> <span data-ttu-id="03210-113">Dies ist immer noch der Fall, und jetzt sind diese Features jetzt Bestandteil von Office 365 Advanced Threat Protection Plan 2 (und dies ist in Office 365 Enterprise E5 enthalten).</span><span class="sxs-lookup"><span data-stu-id="03210-113">This is still the case, and now these features are now part of Office 365 Advanced Threat Protection Plan 2 (and this is included in Office 365 Enterprise E5).</span></span> 

<span data-ttu-id="03210-114">Darüber hinaus waren Office 365 Threat Investigation and Response capbailities früher als Add-on für Office 365 für Geschäftskunden erhältlich.</span><span class="sxs-lookup"><span data-stu-id="03210-114">In addition, Office 365 Threat investigation and response capbailities were formerly available for purchase as an add-on for Office 365 for business customers.</span></span> <span data-ttu-id="03210-115">Diese Funktionen sind jetzt in Office 365 Advanced Threat Protection Plan 2 enthalten (dazu gehört auch Office 365 Advanced Threat Protection Plan 1).</span><span class="sxs-lookup"><span data-stu-id="03210-115">Now, these capabilities are included in Office 365 Advanced Threat Protection Plan 2 (which also includes Office 365 Advanced Threat Protection Plan 1).</span></span> <span data-ttu-id="03210-116">Weitere Informationen finden Sie unter [Office 365 Advanced Threat Protection Plans and Pricing](https://products.office.com/exchange/advance-threat-protection).</span><span class="sxs-lookup"><span data-stu-id="03210-116">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection).</span></span>

<span data-ttu-id="03210-117">Dies ist das folgende:</span><span class="sxs-lookup"><span data-stu-id="03210-117">Here's what all this means:</span></span>

- <span data-ttu-id="03210-118">**Wenn Ihre Organisation bereits über Office 365 Enterprise E5 verfügt**, verfügen Sie bereits über Advanced Threat Protection Plan 2, dazu gehören Untersuchungen und reaktionsMöglichkeiten für Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="03210-118">**If your organization already has Office 365 Enterprise E5**, then you already have Advanced Threat Protection Plan 2, and this includes Threat investigation and response capabilities.</span></span>

- <span data-ttu-id="03210-119">**Wenn Ihre Organisation zuvor office 365 Threat Intelligence (aber nicht office 365 Advanced Threat Protection) als Add-on** für ein anderes Office 365-Abonnement hatte, haben sie Office 365 Advanced Threat Protection Plan 2.</span><span class="sxs-lookup"><span data-stu-id="03210-119">**If your organization previously had Office 365 Threat Intelligence (but not Office 365 Advanced Threat Protection) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 2.</span></span> <span data-ttu-id="03210-120">Hierzu gehören Advanced Threat Protection Plan 1 und Threat Investigation and Response Capabilities.</span><span class="sxs-lookup"><span data-stu-id="03210-120">This includes Advanced Threat Protection Plan 1 and Threat investigation and response capabilities.</span></span> 

- <span data-ttu-id="03210-121">**Wenn Ihre Organisation zuvor office 365 Advanced Threat Protection (aber nicht office 365 Threat Intelligence) als Add-on** für ein anderes Office 365-Abonnement hatte, haben sie Office 365 Advanced Threat Protection Plan 1.</span><span class="sxs-lookup"><span data-stu-id="03210-121">**If your organization previously had Office 365 Advanced Threat Protection (but not Office 365 Threat Intelligence) as an add-on** to another Office 365 subscription, then you will have Office 365 Advanced Threat Protection Plan 1.</span></span> <span data-ttu-id="03210-122">Dies umfasst erweiterte BedrohungsSchutz (nicht jedoch Bedrohungs-investigaiton und Reaktionsfunktionen).</span><span class="sxs-lookup"><span data-stu-id="03210-122">This includes Advanced Threat Protection (but not Threat investigaiton and response capabilities).</span></span>

<span data-ttu-id="03210-123">Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span><span class="sxs-lookup"><span data-stu-id="03210-123">For more information, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-advanced-threat-protection-service-description#whats-new-in-office-365-advanced-threat-protection-atp)</span></span>

## <a name="get-started-with-threat-investigaiton-and-response-capabilities"></a><span data-ttu-id="03210-124">Erste Schritte mit Bedrohungs-investigaiton und Reaktionsfunktionen</span><span class="sxs-lookup"><span data-stu-id="03210-124">Get started with threat investigaiton and response capabilities</span></span>

<span data-ttu-id="03210-125">Verwenden Sie die folgenden Ressourcen, um mehr über die Möglichkeiten der Bedrohung bei der Untersuchung und Antwort in Office 365 zu erfahren, und wie Sie Sie verwenden können, um die Sicherheit von Personen in Ihrer Organisation zu schützen.</span><span class="sxs-lookup"><span data-stu-id="03210-125">Use the following resources to learn more about threat investigation and response capabilities in Office 365, and how you can use it to keep people in your organization safer.</span></span>
  
- <span data-ttu-id="03210-126">[Erste Schritte bei der Bedrohungsanalyse und-Antwort](get-started-with-ti.md) (dazu gehören Informationen zu den erforderlichen Rollen)</span><span class="sxs-lookup"><span data-stu-id="03210-126">[Get started with Threat Investigation and Response](get-started-with-ti.md) (this includes information about required roles)</span></span> 
    
- [<span data-ttu-id="03210-127">Informationen zu Threat Tracker – neu und bemerkenswert</span><span class="sxs-lookup"><span data-stu-id="03210-127">Learn about Threat Trackers - New and Noteworthy</span></span>](threat-trackers.md)
    
- [<span data-ttu-id="03210-128">Suchen und untersuchen von übermittelten Schad-e-Mails</span><span class="sxs-lookup"><span data-stu-id="03210-128">Find and investigate malicious email that was delivered</span></span>](investigate-malicious-email-that-was-delivered.md)
    
- [<span data-ttu-id="03210-129">Verwenden des anGriffs Simulators</span><span class="sxs-lookup"><span data-stu-id="03210-129">Use Attack Simulator</span></span>](attack-simulator.md)
    
- [<span data-ttu-id="03210-130">Integrieren von Bedrohungs Ermittlung und-Antwort mit Windows Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="03210-130">Integrate Threat Investigation and Response with Windows Defender Advanced Threat Protection</span></span>](integrate-office-365-ti-with-wdatp.md)
    
## <a name="related-topics"></a><span data-ttu-id="03210-131">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="03210-131">Related topics</span></span>

[<span data-ttu-id="03210-132">Schutz vor Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="03210-132">Protect against threats in Office 365</span></span>](protect-against-threats.md)
  
[<span data-ttu-id="03210-133">Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="03210-133">Office 365 Advanced Threat Protection</span></span>](office-365-atp.md)
  
[<span data-ttu-id="03210-134">Berechtigungen im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="03210-134">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)
 