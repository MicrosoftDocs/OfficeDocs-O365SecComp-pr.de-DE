---
title: Funktionsweise von DLP zwischen der Sicherheit &amp; Compliance Center und Exchange-Verwaltungskonsole
ms.author: stephow
author: stephow-msft
manager: laurawi
ms.date: 8/4/2017
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a7e4342a-a0a1-4b43-b166-3d7eecf5d2fd
description: Hier erfahren Sie, wie in das Wertpapier DLP &amp; Compliance Center arbeitet mit DLP und Transport Rules in der Exchange-Verwaltungskonsole.
ms.openlocfilehash: bc7494f504c2c0ffa668562d6e64b9f29992e24f
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529728"
---
# <a name="how-dlp-works-between-the-security-amp-compliance-center-and-exchange-admin-center"></a><span data-ttu-id="6646f-103">Funktionsweise von DLP zwischen der Sicherheit &amp; Compliance Center und Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="6646f-103">How DLP works between the Security &amp; Compliance Center and Exchange Admin Center</span></span>

<span data-ttu-id="6646f-104">In Office 365 können Sie eine Data Loss Prevention (DLP) Richtlinie in zwei verschiedenen Admin Center erstellen:</span><span class="sxs-lookup"><span data-stu-id="6646f-104">In Office 365, you can create a data loss prevention (DLP) policy in two different admin centers:</span></span>
  
- <span data-ttu-id="6646f-p101">In der **Sicherheit &amp; Compliance Center**, können Sie eine einzelne DLP-Richtlinie zum Schutz von Inhalten in SharePoint, OneDrive und Exchange erstellen. Wenn möglich, sollten Sie eine DLP-Richtlinie erstellen. Weitere Informationen finden Sie unter [DLP in das Wertpapier &amp; Compliance Center](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="6646f-p101">In the **Security &amp; Compliance Center**, you can create a single DLP policy to help protect content in SharePoint, OneDrive, and Exchange. When possible, we recommend that you create a DLP policy here. For more information, see [DLP in the Security &amp; Compliance Center](data-loss-prevention-policies.md).</span></span>
    
- <span data-ttu-id="6646f-p102">In der **Exchange-Verwaltungskonsole**können Sie eine DLP-Richtlinie zum Schutz von Inhalten nur in Exchange erstellen. Mit dieser Richtlinie können Exchange-Transportregeln, dies ist Weitere Optionen für die Verarbeitung von e-Mail. Weitere Informationen finden Sie unter [DLP in der Exchange-Verwaltungskonsole](https://go.microsoft.com/fwlink/?linkid=852311).</span><span class="sxs-lookup"><span data-stu-id="6646f-p102">In the **Exchange Admin Center**, you can create a DLP policy to help protect content only in Exchange. This policy can use Exchange transport rules, so it has more options specific to handling email. For more information, see [DLP in the Exchange Admin Center](https://go.microsoft.com/fwlink/?linkid=852311).</span></span>
    
<span data-ttu-id="6646f-111">DLP-Richtlinien in diesen Admin erstellten Arbeitsplätze nebeneinander - in diesem Thema wird erläutert, wie.</span><span class="sxs-lookup"><span data-stu-id="6646f-111">DLP polices created in these admin centers work side by side - this topic explains how.</span></span>
  
![DLP-Seiten auf Sicherheit und Compliance Center und Exchange-Verwaltungskonsole](media/d3eaa7e7-3b16-457b-bd9c-26707f7b584f.png)
  
## <a name="how-dlp-in-the-security-amp-compliance-center-works-with-dlp-and-transport-rules-in-the-exchange-admin-center"></a><span data-ttu-id="6646f-113">Wie DLP in das Wertpapier &amp; Compliance Center arbeitet mit DLP und Transport Rules in der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="6646f-113">How DLP in the Security &amp; Compliance Center works with DLP and transport rules in the Exchange Admin Center</span></span>

<span data-ttu-id="6646f-p103">Nach der Erstellung einer DLP-Richtlinie in das Wertpapier &amp; Compliance Center, die Richtlinie für alle Standorte in der Richtlinie enthalten bereitgestellt wird. Wenn die Richtlinie Exchange Online enthält, wird der Richtlinie synchronisierter vorhanden und genau die gleiche Weise wie eine DLP-Richtlinie in der Exchange-Verwaltungskonsole erstellt erzwungen.</span><span class="sxs-lookup"><span data-stu-id="6646f-p103">After you create a DLP policy in the Security &amp; Compliance Center, the policy is deployed to all of the locations included in the policy. If the policy includes Exchange Online, the policy's synced there and enforced in exactly the same way as a DLP policy created in the Exchange admin center.</span></span> 
  
<span data-ttu-id="6646f-p104">Wenn Sie die DLP-Richtlinien in der Exchange-Verwaltungskonsole erstellt haben, diese Richtlinien funktionieren weiterhin, Anzeigemodus alle Richtlinien für e-Mail, die Sie in das Wertpapier erstellen &amp; Compliance Center. Aber beachten Sie, dass in der Exchange-Verwaltungskonsole erstellte Regeln Vorrang haben. Alle Exchange-Transportregeln werden zuerst verarbeitet, und klicken Sie dann die DLP-Regeln aus der Sicherheit &amp; Compliance Center verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="6646f-p104">If you've created DLP policies in the Exchange admin center, those policies will continue to work side by side with any policies for email that you create in the Security &amp; Compliance Center. But note that rules created in the Exchange admin center take precedence. All Exchange transport rules are processed first, and then the DLP rules from the Security &amp; Compliance Center are processed.</span></span>
  
<span data-ttu-id="6646f-119">Dies bedeutet, dass:</span><span class="sxs-lookup"><span data-stu-id="6646f-119">This means that:</span></span>
  
- <span data-ttu-id="6646f-120">Nachrichten, die vom Exchange-Transportregeln blockiert sind wird nicht durch eine in das Wertpapier erstellten DLP-Regeln überprüft abrufen &amp; Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="6646f-120">Messages that are blocked by Exchange transport rules won't get scanned by DLP rules created in the Security &amp; Compliance Center.</span></span>
    
- <span data-ttu-id="6646f-121">Wenn eine Exchange-Transportregel eine Nachricht in einer Weise ändert, die aufgrund eine DLP-Richtlinie in das Wertpapier match &amp; Compliance Center – beispielsweise das Hinzufügen von externen Benutzern - und dann die DLP-Regeln erkennt dies und erzwingen die Richtlinie wie gewünscht.</span><span class="sxs-lookup"><span data-stu-id="6646f-121">If an Exchange transport rule modifies a message in a way that causes it to match a DLP policy in the Security &amp; Compliance Center - such as adding external users - then the DLP rules will detect this and enforce the policy as needed.</span></span>
    
<span data-ttu-id="6646f-122">Beachten Sie, dass der Exchange-Transportregeln, die die Aktion "Beenden der Verarbeitung" verwenden, die Verarbeitung von DLP keine Auswirkung auf Regeln für die auch in das Wertpapier &amp; Compliance Center - wird noch verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="6646f-122">Also note that Exchange transport rules that use the "stop processing" action don't affect the processing of DLP rules in the Security &amp; Compliance Center - they'll still be processed.</span></span>
  
## <a name="policy-tips-in-the-security-amp-compliance-center-vs-the-exchange-admin-center"></a><span data-ttu-id="6646f-123">Richtlinie in das Wertpapier Tipps &amp; Compliance Center im Vergleich mit der Exchange-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="6646f-123">Policy tips in the Security &amp; Compliance Center vs. the Exchange Admin Center</span></span>

<span data-ttu-id="6646f-p105">Tipps zu Richtlinien können arbeiten entweder mit DLP-Richtlinien und e-Mail Flussregeln erstellt, in der Exchange-Verwaltungskonsole oder mit DLP-Richtlinien in das Wertpapier erstellt &amp; Compliance Center, jedoch nicht beide. Dies ist, da diese Richtlinien werden an unterschiedlichen Standorten gespeichert, aber richtlinientipps können nur von einem einzigen Standort zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6646f-p105">Policy tips can work either with DLP policies and mail flow rules created in the Exchange Admin Center, or with DLP policies created in the Security &amp; Compliance Center, but not both. This is because these policies are stored in different locations, but policy tips can draw only from a single location.</span></span>
  
<span data-ttu-id="6646f-p106">Wenn Sie in der Exchange-Verwaltungskonsole eine beliebige richtlinientipps richtlinientipps konfiguriert haben, die Sie in das Wertpapier konfigurieren &amp; Compliance Center wird nicht angezeigt, für die Benutzer in Outlook im Web und Outlook 2013 und höher, bis Sie die Tipps in der Exchange-Verwaltungskonsole deaktivieren. Dadurch wird sichergestellt, dass Ihre aktuellen Exchange-Transportregeln funktionsfähig weiterhin, bis Sie entscheiden, ob die Sicherheit zu wechseln &amp; Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="6646f-p106">If you've configured policy tips in the Exchange Admin Center, any policy tips that you configure in the Security &amp; Compliance Center won't appear to users in Outlook on the web and Outlook 2013 and later until you turn off the tips in the Exchange Admin Center. This ensures that your current Exchange transport rules will continue to work until you choose to switch over to the Security &amp; Compliance Center.</span></span>
  
<span data-ttu-id="6646f-128">Notiz, die während der richtlinientipps nur von einem einzigen Standort, zeichnen können e-Mail-Benachrichtigungen werden immer gesendet, selbst wenn Sie sowohl die Sicherheit DLP-Richtlinien verwenden, &amp; Compliance Center und der Exchange-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="6646f-128">Note that while policy tips can draw only from a single location, email notifications are always sent, even if you're using DLP policies in both the Security &amp; Compliance Center and the Exchange Admin Center.</span></span>
  

