---
title: Häufig gestellte Fragen zur delegierten Verwaltung
ms.author: krowley
author: kccross
manager: laurawi
ms.date: 12/9/2016
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
ms.custom: TN2DMC
localization_priority: Normal
ms.assetid: d6a87ce8-2c22-433a-b430-5eab14f6afdc
description: Dieses Thema liefert häufig gestellte Fragen und Antworten für Microsoft-Partner und Wiederverkäufer, die delegierte Office 365-Verwaltungsaufgaben ausführen möchten, einschließlich der Verwaltung von Exchange Online Protection (EOP) für andere Mandanten (Unternehmen).
ms.openlocfilehash: b6096e835f90a0d5f22a39a5df76e52f1a25a79d
ms.sourcegitcommit: 22bca85c3c6d946083d3784f72e886c068d49f4a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2018
ms.locfileid: "22027492"
---
# <a name="delegated-administration-faq"></a><span data-ttu-id="500cb-103">Häufig gestellte Fragen zur delegierten Verwaltung</span><span class="sxs-lookup"><span data-stu-id="500cb-103">Delegated administration FAQ</span></span>

<span data-ttu-id="500cb-104">Dieses Thema liefert häufig gestellte Fragen und Antworten für Microsoft-Partner und Wiederverkäufer, die delegierte Office 365-Verwaltungsaufgaben ausführen möchten, einschließlich der Verwaltung von Exchange Online Protection (EOP) für andere Mandanten (Unternehmen).</span><span class="sxs-lookup"><span data-stu-id="500cb-104">This topic provides frequently asked questions and answers for Microsoft partners and resellers who want to perform delegated Office 365 administration tasks, including the ability to manage Exchange Online Protection (EOP) for other tenants (companies).</span></span>
  
 <span data-ttu-id="500cb-105">**F. Ich bin Wiederverkäufer und muss die Mandanten meines Kunden verwalten. Wie funktioniert das?**</span><span class="sxs-lookup"><span data-stu-id="500cb-105">**Q. I'm a reseller and I need to manage my customer's tenants; how does this work?**</span></span>
  
<span data-ttu-id="500cb-p101">A. Wenn Sie ein Microsoft-Partner oder Wiederverkäufer sind und sich als Microsoft Advisor-Partner registriert haben, können Sie die Berechtigung beantragen, deren Mandanten im Office 365 Admin Center zu verwalten. Dies wird als delegierte Administration bezeichnet und ermöglicht Ihnen die Verwaltung des Office 365-Mandanten (einschließlich EOP-Einstellungen), als wären Sie ein Administrator in ihrer Organisation. Die Schritte für die delegierte Verwaltung sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="500cb-p101">A. If you are a Microsoft partner or reseller, and you've signed up to be a Microsoft advisor, you can request permission to administer their tenant within the Office 365 admin center. This is known as delegated administration, and it allows you to manage their Office 365 tenant (including EOP settings) as if you were an administrator within their organization. The steps for performing delegated administration are as follows:</span></span>
  
1. <span data-ttu-id="500cb-110">Registrieren Sie sich als [Microsoft Office 365 Advisor](https://aka.ms/cloudbenefits).</span><span class="sxs-lookup"><span data-stu-id="500cb-110">Sign up to be a [Microsoft Office 365 Advisor](https://aka.ms/cloudbenefits).</span></span>
    
2. <span data-ttu-id="500cb-p102">Registrieren Sie sich für die delegierte Verwaltung in Office 365. Bevor Sie mit der Verwaltung eines Kundenkontos beginnen können, muss der Kunde Sie als delegierten Administrator autorisieren. Um die Genehmigung des Kunden einzuholen, [senden Sie ihm zuerst ein Angebot für die delegierte Verwaltung](https://go.microsoft.com/fwlink/?LinkId=396829). (Sie können Ihrem Kunden die delegierte Verwaltung auch später anbieten.)</span><span class="sxs-lookup"><span data-stu-id="500cb-p102">Sign up for Office 365 delegated administration. Before you can start administering a customer's account, they must authorize you as a delegated administrator. To obtain their approval, you first [send them an offer for delegated administration](https://go.microsoft.com/fwlink/?LinkId=396829). (You can also offer delegated administration to your customer at a later time.)</span></span> 
    
3. <span data-ttu-id="500cb-115">Erstellen Sie das Konto für die delegierte Verwaltung mithilfe der unter [Hinzufügen oder Löschen eines delegierten Administrators](https://go.microsoft.com/fwlink/?LinkId=396831) aufgeführten Schritte.</span><span class="sxs-lookup"><span data-stu-id="500cb-115">Create the delegated admin account using the steps documented in [Add or delete a delegated admin](https://go.microsoft.com/fwlink/?LinkId=396831).</span></span>
    
<span data-ttu-id="500cb-116">Rufen Sie die Website [Partner: Ihr Geschäft voranbringen und Verwalten Ihres Office 365-Partnerkontos](https://go.microsoft.com/fwlink/?LinkId=301485) auf, um weitere Informationen zum Einrichten der delegierten Verwaltung in Office 365 zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="500cb-116">Visit [Partners: Build your business and administer your Office 365 partner account](https://go.microsoft.com/fwlink/?LinkId=301485) for more information about how to set up Office 365 delegated administration.</span></span> 
  
 <span data-ttu-id="500cb-117">**F. Ich bin Kunde und kein Wiederverkäufer. Wie kann ich mich als delegierten Administrator für meine Untermandanten einrichten?**</span><span class="sxs-lookup"><span data-stu-id="500cb-117">**Q. I'm a customer, not a reseller, how can set up delegated administrator for my sub-tenants?**</span></span>
  
<span data-ttu-id="500cb-p103">A. Die delegierte Verwaltung ist derzeit nur für Wiederverkäufer und Partner verfügbar. Wir haben jedoch ein Beispielskript für Windows PowerShell bereitgestellt, mit dessen Hilfe Sie Richtlinie auf Ihre Untermandanten (Unternehmen) anwenden können. Weitere Informationen finden Sie unter [Beispielskript für das Anwenden von EOP-Einstellungen für mehrere Mandanten](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span><span class="sxs-lookup"><span data-stu-id="500cb-p103">A. Delegated administration is only available for resellers and partners at this time. However, we've provided a sample Windows PowerShell script that will help you apply policies to your sub-tenants (companies). For more information, see [Sample script for applying EOP settings to multiple tenants](sample-script-for-applying-eop-settings-to-multiple-tenants.md).</span></span>
  
 <span data-ttu-id="500cb-122">**F. Kann ich verhindern, dass der Administrator für meine Untermandanten meine Richtlinie ändert?**</span><span class="sxs-lookup"><span data-stu-id="500cb-122">**Q. Can I prevent my sub-tenant admin from modifying my policy?**</span></span>
  
<span data-ttu-id="500cb-p104">A. Office 365 unterstützt diese Funktion derzeit nicht.</span><span class="sxs-lookup"><span data-stu-id="500cb-p104">A. Office 365 does not currently have this capability.</span></span>
  
 <span data-ttu-id="500cb-125">**F. Ist eine konsolidierte Berichterstellung über meine Untermandanten hinweg möglich?**</span><span class="sxs-lookup"><span data-stu-id="500cb-125">**Q. Can I get consolidated reporting across all of my sub-tenants?**</span></span>
  
<span data-ttu-id="500cb-p105">A. Eine konsolidierte Berichterstellung über die von Ihnen verwalteten Unternehmen hinweg ist derzeit für die Office 365 Admin Center-Berichte nicht verfügbar. Dies ist jedoch über die Remote-Windows PowerShell oder den [Webdienst für die Berichterstellung](https://go.microsoft.com/fwlink/?LinkId=279926) möglich.</span><span class="sxs-lookup"><span data-stu-id="500cb-p105">A. Consolidated reporting across the companies you manage is not available for the Office 365 admin center reports at this time. However, this can be done via remote Windows PowerShell or the [reporting web service](https://go.microsoft.com/fwlink/?LinkId=279926).</span></span> 
  

