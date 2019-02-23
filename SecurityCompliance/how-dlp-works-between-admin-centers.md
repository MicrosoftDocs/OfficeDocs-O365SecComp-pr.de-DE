---
title: FunktionsWeise von DLP zwischen Security &amp; Compliance Center und Exchange Admin Center
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Erfahren Sie, wie DLP im &amp; Security Compliance Center mit DLP-und Transportregeln im Exchange Admin Center funktioniert.
ms.openlocfilehash: 531a45308594d03dc219f50d989a08236b8b5e20
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215645"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a><span data-ttu-id="681bd-103">FunktionsWeise von DLP zwischen Security &amp; Compliance Center und Exchange Admin Center</span><span class="sxs-lookup"><span data-stu-id="681bd-103">How DLP works between the Security &amp; Compliance Center and Exchange Admin Center</span></span>

<span data-ttu-id="681bd-104">In Office 365 können Sie eine DLP-Richtlinie (Data Loss Prevention, Datenverlust-Verhinderung) in zwei verschiedenen Verwaltungs Centern erstellen:</span><span class="sxs-lookup"><span data-stu-id="681bd-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="681bd-p101">Im \*\* &amp; Security Compliance Center\*\*können Sie eine einzelne DLP-Richtlinie zum Schutz von Inhalten in SharePoint, OneDrive und Exchange erstellen. Wenn möglich, empfehlen wir, dass Sie hier eine DLP-Richtlinie erstellen. Weitere Informationen finden Sie unter [DLP im Security &amp; Compliance Center](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="681bd-p101">In the **Security &amp; Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security &amp; Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="681bd-p102">In der **Exchange-Verwaltungskonsole**können Sie eine DLP-Richtlinie zum Schutz von Inhalten nur in Exchange erstellen. Diese Richtlinie kann Exchange-Transportregeln verwenden, sodass Sie mehr Optionen für die e-Mail-Verarbeitung hat. Weitere Informationen finden Sie unter [DLP im Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="681bd-p102">In the **Exchange Admin Center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange transport rules, so it has more options specific to handling email. For more information, see [DLP in the Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="681bd-111">In diesen Verwaltungs Centern erstellte DLP-Richtlinien arbeiten nebeneinander – in diesem Thema wird erläutert, wie.</span><span class="sxs-lookup"><span data-stu-id="681bd-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![DLP-Seiten im Security and Compliance Center und Exchange Admin Center](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a><span data-ttu-id="681bd-113">FunktionsWeise von DLP im &amp; Security Compliance Center mit DLP-und Transportregeln im Exchange Admin Center</span><span class="sxs-lookup"><span data-stu-id="681bd-113">How DLP in the Security &amp; Compliance Center works with DLP and transport rules in the Exchange Admin Center</span></span>

<span data-ttu-id="681bd-p103">Nachdem Sie im Security &amp; Compliance Center eine DLP-Richtlinie erstellt haben, wird die Richtlinie für alle in der Richtlinie enthaltenen Standorte bereitgestellt. Wenn die Richtlinie Exchange Online enthält, wird die Richtlinie dort synchronisiert und auf genau dieselbe Weise erzwungen wie eine im Exchange Admin Center erstellte DLP-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="681bd-p103">After you create a DLP policy in the Security &amp; Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="681bd-p104">Wenn Sie DLP-Richtlinien in der Exchange-Verwaltungskonsole erstellt haben, funktionieren diese Richtlinien weiterhin mit allen Richtlinien für e-Mails, die Sie im Security &amp; Compliance Center erstellen. Beachten Sie jedoch, dass Regeln, die in der Exchange-Verwaltungskonsole erstellt wurden, Vorrang haben. Alle Exchange-Transportregeln werden zuerst verarbeitet, und anschließend werden die DLP-Regeln &amp; aus dem Security Compliance Center verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="681bd-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security &amp; Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange transport rules are processed first, and then the DLP rules from the Security &amp; Compliance Center are processed.</span></span>
  
<span data-ttu-id="681bd-119">Dies führt dazu, dass:</span><span class="sxs-lookup"><span data-stu-id="681bd-119">This means that:</span></span>
  
- <span data-ttu-id="681bd-120">Nachrichten, die durch Exchange-Transportregeln blockiert werden, werden nicht von im Security &amp; Compliance Center erstellten DLP-Regeln gescannt.</span><span class="sxs-lookup"><span data-stu-id="681bd-120">Messages that are blocked by Exchange transport rules won't get scanned by DLP rules created in the Security &amp; Compliance Center.</span></span>
    
- <span data-ttu-id="681bd-121">Wenn eine Nachricht in einer Exchange-Transportregel so geändert wird, dass Sie eine DLP-Richtlinie im Security &amp; Compliance Center (beispielsweise Hinzufügen externer Benutzer) abstimmt, werden die DLP-Regeln dies erkennen und die Richtlinie nach Bedarf erzwingen.</span><span class="sxs-lookup"><span data-stu-id="681bd-121">If an Exchange transport rule modifies a message in a way that causes it to match a DLP policy in the Security &amp; Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="681bd-122">Beachten Sie, dass Exchange-Transportregeln, die die Aktion "Verarbeitung beenden" verwenden, keine Auswirkungen auf die Verarbeitung von &amp; DLP-Regeln im Security Compliance Center haben – Sie werden weiterhin verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="681bd-122">Also note that Exchange transport rules that use the "stop processing" action don't affect the processing of DLP rules in the Security &amp; Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="681bd-123">Richtlinien Tipps im Security &amp; Compliance Center im Vergleich zur Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="681bd-123">Policy tips in the Security &amp; Compliance Center vs. the Exchange Admin Center</span></span>

<span data-ttu-id="681bd-p105">Richtlinien Tipps können entweder mit DLP-Richtlinien und Nachrichtenfluss Regeln im Exchange Admin Center oder mit im Security &amp; Compliance Center erstellten DLP-Richtlinien funktionieren, jedoch nicht mit beiden. Der Grund hierfür liegt darin, dass diese Richtlinien an unterschiedlichen Speicherorten gespeichert werden, Richtlinien Tipps können jedoch nur von einem Speicherort aus erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="681bd-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange Admin Center, or with DLP policies created in the Security &amp; Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="681bd-p106">Wenn Sie im Exchange Admin Center Richtlinien Tipps konfiguriert haben, werden alle Richtlinien Tipps, die Sie im Security &amp; Compliance Center konfigurieren, nicht für Benutzer in Outlook im Web und Outlook 2013 und höher angezeigt, bis Sie die Tipps im Exchange Admin Center deaktiviert haben. Dadurch wird sichergestellt, dass Ihre aktuellen Exchange-Transportregeln weiterhin funktionieren, bis Sie sich für das Security &amp; Compliance Center entscheiden.</span><span class="sxs-lookup"><span data-stu-id="681bd-p106">If you've configured policy tips in the Exchange Admin Center, any policy tips that you configure in the Security &amp; Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange Admin Center. This ensures that your current Exchange transport rules will continue to work until you choose to switch over to the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="681bd-128">Beachten Sie, dass während Richtlinien Tipps nur von einem einzigen Ort aus gezeichnet werden können, e-Mail-Benachrichtigungen auch dann immer gesendet werden, wenn Sie &amp; DLP-Richtlinien sowohl im Security Compliance Center als auch im Exchange Admin Center verwenden.</span><span class="sxs-lookup"><span data-stu-id="681bd-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security &amp; Compliance Center and the Exchange Admin Center.</span></span>
  

