---
title: Häufig gestellte Fragen zur delegierten Verwaltung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: d6a87ce8-2c22-433a-b430-5eab14f6afdc
description: Dieses Thema liefert häufig gestellte Fragen und Antworten für Microsoft-Partner und Wiederverkäufer, die delegierte Office 365-Verwaltungsaufgaben ausführen möchten, einschließlich der Verwaltung von Exchange Online Protection (EOP) für andere Mandanten (Unternehmen).
ms.openlocfilehash: 41f2e8f0ed48273ff1934ca4f2306f29f92b1ff1
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256193"
---
# <a name="delegated-administration-faq"></a><span data-ttu-id="d2d38-103">Häufig gestellte Fragen zur delegierten Verwaltung</span><span class="sxs-lookup"><span data-stu-id="d2d38-103">Delegated administration FAQ</span></span>

<span data-ttu-id="d2d38-104">Dieses Thema liefert häufig gestellte Fragen und Antworten für Microsoft-Partner und Wiederverkäufer, die delegierte Office 365-Verwaltungsaufgaben ausführen möchten, einschließlich der Verwaltung von Exchange Online Protection (EOP) für andere Mandanten (Unternehmen).</span><span class="sxs-lookup"><span data-stu-id="d2d38-104">This topic provides frequently asked questions and answers for Microsoft partners and resellers who want to perform delegated Office 365 administration tasks, including the ability to manage Exchange Online Protection (EOP) for other tenants (companies).</span></span>
  
 <span data-ttu-id="d2d38-105">**F. Ich bin Wiederverkäufer und muss die Mandanten meines Kunden verwalten. Wie funktioniert das?**</span><span class="sxs-lookup"><span data-stu-id="d2d38-105">**Q. I'm a reseller and I need to manage my customer's tenants; how does this work?**</span></span>
  
<span data-ttu-id="d2d38-106">A.</span><span class="sxs-lookup"><span data-stu-id="d2d38-106">A.</span></span> <span data-ttu-id="d2d38-107">Wenn Sie Microsoft-Partner oder-Händler sind und sich als Microsoft Advisor angemeldet haben, können Sie die Berechtigung zum Verwalten des Mandanten innerhalb des Admin Centers anfordern.</span><span class="sxs-lookup"><span data-stu-id="d2d38-107">If you are a Microsoft partner or reseller, and you've signed up to be a Microsoft advisor, you can request permission to administer their tenant within the admin center.</span></span> <span data-ttu-id="d2d38-108">Dies wird als delegierte Administration bezeichnet und ermöglicht Ihnen die Verwaltung des Office 365-Mandanten (einschließlich EOP-Einstellungen), als wären Sie ein Administrator in ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="d2d38-108">This is known as delegated administration, and it allows you to manage their Office 365 tenant (including EOP settings) as if you were an administrator within their organization.</span></span> <span data-ttu-id="d2d38-109">Die Schritte für die delegierte Verwaltung sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d2d38-109">The steps for performing delegated administration are as follows:</span></span>
  
1. <span data-ttu-id="d2d38-110">Registrieren Sie sich als [Microsoft Office 365 Advisor](https://aka.ms/cloudbenefits).</span><span class="sxs-lookup"><span data-stu-id="d2d38-110">Sign up to be a [Microsoft Office 365 Advisor](https://aka.ms/cloudbenefits).</span></span>
    
2. <span data-ttu-id="d2d38-p102">Registrieren Sie sich für die delegierte Verwaltung in Office 365. Bevor Sie mit der Verwaltung eines Kundenkontos beginnen können, muss der Kunde Sie als delegierten Administrator autorisieren. Um die Genehmigung des Kunden einzuholen, [senden Sie ihm zuerst ein Angebot für die delegierte Verwaltung](https://go.microsoft.com/fwlink/?LinkId=396829). (Sie können Ihrem Kunden die delegierte Verwaltung auch später anbieten.)</span><span class="sxs-lookup"><span data-stu-id="d2d38-p102">Sign up for Office 365 delegated administration. Before you can start administering a customer's account, they must authorize you as a delegated administrator. To obtain their approval, you first [send them an offer for delegated administration](https://go.microsoft.com/fwlink/?LinkId=396829). (You can also offer delegated administration to your customer at a later time.)</span></span> 
    
3. <span data-ttu-id="d2d38-115">Erstellen Sie das Konto für die delegierte Verwaltung mithilfe der unter [Hinzufügen oder Löschen eines delegierten Administrators](https://go.microsoft.com/fwlink/?LinkId=396831) aufgeführten Schritte.</span><span class="sxs-lookup"><span data-stu-id="d2d38-115">Create the delegated admin account using the steps documented in [Add or delete a delegated admin](https://go.microsoft.com/fwlink/?LinkId=396831).</span></span>
    
<span data-ttu-id="d2d38-116">Rufen Sie die Website [Partner: Ihr Geschäft voranbringen und Verwalten Ihres Office 365-Partnerkontos](https://go.microsoft.com/fwlink/?LinkId=301485) auf, um weitere Informationen zum Einrichten der delegierten Verwaltung in Office 365 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d2d38-116">Visit [Partners: Build your business and administer your Office 365 partner account](https://go.microsoft.com/fwlink/?LinkId=301485) for more information about how to set up Office 365 delegated administration.</span></span> 
  
 <span data-ttu-id="d2d38-117">**F. Ich bin Kunde und kein Wiederverkäufer. Wie kann ich mich als delegierten Administrator für meine Untermandanten einrichten?**</span><span class="sxs-lookup"><span data-stu-id="d2d38-117">**Q. I'm a customer, not a reseller, how can set up delegated administrator for my sub-tenants?**</span></span>
  
<span data-ttu-id="d2d38-p103">A. Die delegierte Verwaltung ist derzeit nur für Wiederverkäufer und Partner verfügbar. Wir haben jedoch ein Beispielskript für Windows PowerShell bereitgestellt, mit dessen Hilfe Sie Richtlinie auf Ihre Untermandanten (Unternehmen) anwenden können. Weitere Informationen finden Sie unter [Beispielskript für das Anwenden von EOP-Einstellungen für mehrere Mandanten](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span><span class="sxs-lookup"><span data-stu-id="d2d38-p103">A. Delegated administration is only available for resellers and partners at this time. However, we've provided a sample Windows PowerShell script that will help you apply policies to your sub-tenants (companies). For more information, see [Sample script for applying EOP settings to multiple tenants](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span></span>
  
 <span data-ttu-id="d2d38-122">**F. Kann ich verhindern, dass der Administrator für meine Untermandanten meine Richtlinie ändert?**</span><span class="sxs-lookup"><span data-stu-id="d2d38-122">**Q. Can I prevent my sub-tenant admin from modifying my policy?**</span></span>
  
<span data-ttu-id="d2d38-p104">A. Office 365 unterstützt diese Funktion derzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="d2d38-p104">A. Office 365 does not currently have this capability.</span></span>
  
 <span data-ttu-id="d2d38-125">**F. Ist eine konsolidierte Berichterstellung über meine Untermandanten hinweg möglich?**</span><span class="sxs-lookup"><span data-stu-id="d2d38-125">**Q. Can I get consolidated reporting across all of my sub-tenants?**</span></span>
  
<span data-ttu-id="d2d38-126">A.</span><span class="sxs-lookup"><span data-stu-id="d2d38-126">A.</span></span> <span data-ttu-id="d2d38-127">Die konsolidierte Berichterstellung für die von Ihnen verwalteten Unternehmen ist derzeit nicht für die Micrsoft 365 Admin Center-Berichte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d2d38-127">Consolidated reporting across the companies you manage is not available for the Micrsoft 365 admin center reports at this time.</span></span> <span data-ttu-id="d2d38-128">Dies ist jedoch über die Remote-Windows PowerShell oder den [Webdienst für die Berichterstellung](https://go.microsoft.com/fwlink/?LinkId=279926) möglich.</span><span class="sxs-lookup"><span data-stu-id="d2d38-128">However, this can be done via remote Windows PowerShell or the [reporting web service](https://go.microsoft.com/fwlink/?LinkId=279926).</span></span> 
  

