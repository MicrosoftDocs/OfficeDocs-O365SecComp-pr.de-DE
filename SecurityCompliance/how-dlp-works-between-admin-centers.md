---
title: Funktionsweise von DLP zwischen dem Security & Compliance Center und Exchange Admin Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 04/19/2019
ms.audience: Admin
ms.topic: conceptual
ms.service: O365-seccomp
ms.collection:
- M365-security-compliance
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Erfahren Sie, wie DLP im Security & Compliance Center mit DLP-und Nachrichtenfluss Regeln (Transportregeln) in der Exchange-Verwaltungskonsole arbeitet.
ms.openlocfilehash: efe8fb733417275a259a472db3444b8f6cad1f92
ms.sourcegitcommit: e23b84ef4eee9cccec7205826b71ddfe9aaac2f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2019
ms.locfileid: "33362033"
---
# <a name="how-dlp-works-between-the-security--compliance-center-and-exchange-admin-center"></a><span data-ttu-id="45c66-103">Funktionsweise von DLP zwischen dem Security & Compliance Center und Exchange Admin Center</span><span class="sxs-lookup"><span data-stu-id="45c66-103">How DLP works between the Security & Compliance Center and Exchange admin center</span></span>

<span data-ttu-id="45c66-104">In Office 365 können Sie eine DLP-Richtlinie (Data Loss Prevention, Datenverlust-Verhinderung) in zwei verschiedenen Verwaltungs Centern erstellen:</span><span class="sxs-lookup"><span data-stu-id="45c66-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="45c66-105">Im **Security _AMP_ Compliance Center**können Sie eine einzelne DLP-Richtlinie zum Schutz von Inhalten in SharePoint, OneDrive, Exchange und jetzt Microsoft Teams erstellen.</span><span class="sxs-lookup"><span data-stu-id="45c66-105">In the **Security & Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, Exchange, and now Microsoft Teams.</span></span> <span data-ttu-id="45c66-106">Wenn möglich, empfehlen wir, dass Sie hier eine DLP-Richtlinie erstellen.</span><span class="sxs-lookup"><span data-stu-id="45c66-106">When possible, we recommend that you create a DLP policy here.</span></span> <span data-ttu-id="45c66-107">Weitere Informationen finden Sie unter [DLP im Security _AMP_ Compliance Center](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="45c66-107">For more information, see [DLP in the Security & Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="45c66-108">In der **Exchange-Verwaltungskonsole**können Sie eine DLP-Richtlinie zum Schutz von Inhalten nur in Exchange erstellen.</span><span class="sxs-lookup"><span data-stu-id="45c66-108">In the **Exchange admin center**, you can create a DLP policy to help protect content only in Exchange.</span></span> <span data-ttu-id="45c66-109">Diese Richtlinie kann Exchange-Nachrichtenfluss Regeln (auch als Transportregeln bezeichnet) verwenden, sodass Sie mehr Optionen für die e-Mail-Verarbeitung hat.</span><span class="sxs-lookup"><span data-stu-id="45c66-109">This policy can use Exchange mail flow rules (also known as transport rules), so it has more options specific to handling email.</span></span> <span data-ttu-id="45c66-110">Weitere Informationen finden Sie unter [DLP im Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="45c66-110">For more information, see [DLP in the Exchange admin center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="45c66-111">In diesen Verwaltungs Centern erstellte DLP-Richtlinien arbeiten nebeneinander – in diesem Thema wird erläutert, wie.</span><span class="sxs-lookup"><span data-stu-id="45c66-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![DLP-Seiten im Security and Compliance Center und Exchange Admin Center](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security--compliance-center-works-with-dlp-and-mail-flow-rules-in-the-exchange-admin-center"></a><span data-ttu-id="45c66-113">FunktionsWeise von DLP im Security & Compliance Center mit DLP-und Nachrichtenfluss Regeln im Exchange Admin Center</span><span class="sxs-lookup"><span data-stu-id="45c66-113">How DLP in the Security & Compliance Center works with DLP and mail flow rules in the Exchange admin center</span></span>

<span data-ttu-id="45c66-114">Nachdem Sie im Security & Compliance Center eine DLP-Richtlinie erstellt haben, wird die Richtlinie für alle in der Richtlinie enthaltenen Standorte bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="45c66-114">After you create a DLP policy in the Security & Compliance Center, the policy is deployed to all of the locations included in the policy.</span></span> <span data-ttu-id="45c66-115">Wenn die Richtlinie Exchange Online enthält, wird die Richtlinie dort synchronisiert und auf genau dieselbe Weise erzwungen wie eine im Exchange Admin Center erstellte DLP-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="45c66-115">If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="45c66-116">Wenn Sie DLP-Richtlinien in der Exchange-Verwaltungskonsole erstellt haben, funktionieren diese Richtlinien weiterhin mit allen Richtlinien für e-Mails, die Sie im Security & Compliance Center erstellen.</span><span class="sxs-lookup"><span data-stu-id="45c66-116">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security & Compliance Center.</span></span> <span data-ttu-id="45c66-117">Beachten Sie jedoch, dass Regeln, die in der Exchange-Verwaltungskonsole erstellt wurden, Vorrang haben.</span><span class="sxs-lookup"><span data-stu-id="45c66-117">But note that rules created in the Exchange admin center take precedence.</span></span> <span data-ttu-id="45c66-118">Alle Exchange-Nachrichtenfluss Regeln werden zuerst verarbeitet, und anschließend werden die DLP-Regeln aus dem Security & Compliance Center verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="45c66-118">All Exchange mail flow rules are processed first, and then the DLP rules from the Security & Compliance Center are processed.</span></span>
  
<span data-ttu-id="45c66-119">Dies führt dazu, dass:</span><span class="sxs-lookup"><span data-stu-id="45c66-119">This means that:</span></span>
  
- <span data-ttu-id="45c66-120">Nachrichten, die durch Exchange-Nachrichtenfluss Regeln blockiert werden, werden nicht von DLP-Regeln überprüft, die im Security & Compliance Center erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="45c66-120">Messages that are blocked by Exchange mail flow rules won't get scanned by DLP rules created in the Security & Compliance Center.</span></span>
    
- <span data-ttu-id="45c66-121">Wenn eine Nachricht in einer Exchange-Nachrichtenfluss Regel so geändert wird, dass Sie eine DLP-Richtlinie im Security & Compliance Center (beispielsweise Hinzufügen externer Benutzer) abstimmt, werden die DLP-Regeln dies erkennen und die Richtlinie nach Bedarf erzwingen.</span><span class="sxs-lookup"><span data-stu-id="45c66-121">If an Exchange mail flow rule modifies a message in a way that causes it to match a DLP policy in the Security & Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="45c66-122">Beachten Sie, dass Exchange-Nachrichtenfluss Regeln, die die Aktion "Verarbeitung beenden" verwenden, keine Auswirkungen auf die Verarbeitung von DLP-Regeln im Security & Compliance Center haben – Sie werden weiterhin verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="45c66-122">Also note that Exchange mail flow rules that use the "stop processing" action don't affect the processing of DLP rules in the Security & Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security--compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="45c66-123">Richtlinien Tipps im Security & Compliance Center im Vergleich zur Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="45c66-123">Policy tips in the Security & Compliance Center vs. the Exchange admin center</span></span>

<span data-ttu-id="45c66-124">Richtlinien Tipps können entweder mit DLP-Richtlinien und Nachrichtenfluss Regeln funktionieren, die im Exchange Admin Center erstellt wurden, oder mit DLP-Richtlinien, die im Security & Compliance Center erstellt wurden, aber nicht in beiden.</span><span class="sxs-lookup"><span data-stu-id="45c66-124">Policy tips can work either with DLP policies and mail flow rules created in the Exchange admin center, or with DLP policies created in the Security & Compliance Center, but not both.</span></span> <span data-ttu-id="45c66-125">Der Grund hierfür liegt darin, dass diese Richtlinien an unterschiedlichen Speicherorten gespeichert werden, Richtlinien Tipps können jedoch nur von einem Speicherort aus erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="45c66-125">This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="45c66-126">Wenn Sie im Exchange Admin Center Richtlinien Tipps konfiguriert haben, werden alle Richtlinien Tipps, die Sie im Security & Compliance Center konfigurieren, nicht Benutzern in Outlook im Web und Outlook 2013 und höher angezeigt, bis Sie die Tipps im Exchange Admin Center deaktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="45c66-126">If you've configured policy tips in the Exchange admin center, any policy tips that you configure in the Security & Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange admin center.</span></span> <span data-ttu-id="45c66-127">Dadurch wird sichergestellt, dass Ihre aktuellen Exchange-Nachrichtenfluss Regeln weiterhin funktionieren, bis Sie sich für das Security & Compliance Center entscheiden.</span><span class="sxs-lookup"><span data-stu-id="45c66-127">This ensures that your current Exchange mail flow rules will continue to work until you choose to switch over to the Security & Compliance Center.</span></span>
  
<span data-ttu-id="45c66-128">Beachten Sie, dass während Richtlinien Tipps nur von einem einzigen Ort aus gezeichnet werden können, e-Mail-Benachrichtigungen auch dann immer gesendet werden, wenn Sie DLP-Richtlinien sowohl im Security & Compliance Center als auch im Exchange Admin Center verwenden.</span><span class="sxs-lookup"><span data-stu-id="45c66-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security & Compliance Center and the Exchange admin center.</span></span>
  

