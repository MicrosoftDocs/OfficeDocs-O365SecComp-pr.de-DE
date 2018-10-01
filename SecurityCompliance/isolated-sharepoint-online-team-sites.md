---
title: Isolierte SharePoint Online-Teamwebsites
ms.author: josephd
author: JoeDavies-MSFT
manager: laurawi
ms.date: 12/15/2017
ms.audience: ITPro
ms.topic: overview
ms.service: o365-solutions
localization_priority: Priority
ms.collection:
- Ent_O365
- Strat_O365_Enterprise
ms.custom:
- Ent_Solutions
ms.assetid: 71250a04-fd2d-4c3c-a32b-b8a838b19a54
description: 'Zusammenfassung: Informationen zu Verwendungszwecken für isolierte SharePoint Online-Teamwebsites.'
ms.openlocfilehash: 74995273d531ef756ac169491105fb8c8f7eccb5
ms.sourcegitcommit: e0f016aca7befc8806233a492ee916cbe646094f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/27/2018
ms.locfileid: "25345787"
---
# <a name="isolated-sharepoint-online-team-sites"></a><span data-ttu-id="ae26d-103">Isolierte SharePoint Online-Teamwebsites</span><span class="sxs-lookup"><span data-stu-id="ae26d-103">Isolated SharePoint Online team sites</span></span>

 <span data-ttu-id="ae26d-104">**Zusammenfassung:** Informationen zu Verwendungszwecken für isolierte SharePoint Online-Teamwebsites.</span><span class="sxs-lookup"><span data-stu-id="ae26d-104">**Summary:** Learn about the uses for isolated SharePoint Online team sites.</span></span>
  
<span data-ttu-id="ae26d-p101">SharePoint Online-Teamwebsites sind eine einfache Möglichkeit, um schnell einen Ort für die Zusammenarbeit an Notizen, Dokumenten, Artikeln, einem Kalender und anderen Ressourcen in Microsoft Office 365 zu erstellen. SharePoint Online-Teamwebsites basieren auf einer Office 365-Gruppe und haben ein vereinfachtes Verwaltungsmodell, um die offene Zusammenarbeit mit einer privaten Menge von Gruppenmitgliedern oder der gesamten Organisation zu ermöglichen. Über eine standardmäßige SharePoint Online-Teamwebsite können Mitglieder der Office 365-Gruppe andere Benutzer einladen und Berechtigungseinstellungen steuern.</span><span class="sxs-lookup"><span data-stu-id="ae26d-p101">SharePoint Online team sites are an easy way to quickly create a space for collaboration of notes, documents, articles, a calendar, and other resources in Microsoft Office 365. SharePoint Online team sites are based on an Office 365 group and have a simplified administration model to allow open collaboration with a private set of group members or the entire organization. A default SharePoint Online team site allows members of the Office 365 group to invite other users and control permissions settings.</span></span>
  
<span data-ttu-id="ae26d-p102">In einigen Fällen möchten Sie vielleicht jedoch eine SharePoint Online-Teamwebsite für die Zusammenarbeit erstellen, bei der die Berechtigungen der Website strenger über Gruppenmitgliedschaft und SharePoint Online-Berechtigungsebenen gesteuert werden, die nur von SharePoint-Administratoren verwaltet werden. Wir bezeichnen dies als eine isolierte Website, die auf die Gruppe der Benutzer beschränkt ist, die entweder auf der Website zusammenarbeiten, ihren Inhalt anzeigen oder diese verwalten. Eine isolierte Website kann z. B. in folgenden Fällen erforderlich sein:</span><span class="sxs-lookup"><span data-stu-id="ae26d-p102">However, in some cases, you want to create a SharePoint Online team site for collaboration where the permissions of that site are more tightly controlled through group membership and SharePoint Online permission levels, which are only managed by SharePoint administrators. We call this an isolated site, which is isolated to the set of users that are either collaborating, viewing its contents, or administering the site. You might need an isolated site for the following:</span></span>
  
- <span data-ttu-id="ae26d-111">Für ein geheimes Projekt innerhalb Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="ae26d-111">A secret project within your organization.</span></span>
    
- <span data-ttu-id="ae26d-112">Als Speicherort für das besonders vertrauliche oder wertvolle geistige Eigentum Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="ae26d-112">The location for highly-sensitive or valuable intellectual property for your organization.</span></span>
    
- <span data-ttu-id="ae26d-113">Für die Ressourcen im Zusammenhang mit einer Klage, die von Ihrer Organisation erhoben oder die gegen sie geführt wird.</span><span class="sxs-lookup"><span data-stu-id="ae26d-113">The resources for a legal action taken by your organization or that to which it is being subjected.</span></span>
    
- <span data-ttu-id="ae26d-114">Zum Freigeben eines Office 365-Abonnements für mehrere Organisationen, zwischen denen es zwar einige Überschneidungen gibt, die jedoch größtenteils als eigenständige Geschäftseinheiten existieren.</span><span class="sxs-lookup"><span data-stu-id="ae26d-114">To share an Office 365 subscription between multiple organizations that have some overlap, but for the most part exist as separate business entities.</span></span>
    
<span data-ttu-id="ae26d-115">Dies sind die Anforderungen einer isolierten-Website:</span><span class="sxs-lookup"><span data-stu-id="ae26d-115">Here are the requirements of an isolated site:</span></span>
  
- <span data-ttu-id="ae26d-116">Nur SharePoint Online-Administratoren können Aufgaben der Websiteverwaltung ausführen; hierzu gehören die Gruppenmitgliedschaft für den Zugriff auf die Website und das Konfigurieren von benutzerdefinierten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="ae26d-116">Only SharePoint Online administrators can perform site administration, which includes group membership for access to the site and configuring custom permissions.</span></span>
    
- <span data-ttu-id="ae26d-117">Mitglieder der Website können keine anderen Mitglieder zur Teamwebsite einladen.</span><span class="sxs-lookup"><span data-stu-id="ae26d-117">Members of the site cannot invite other members to the team site.</span></span>
    
- <span data-ttu-id="ae26d-p103">Benutzer, die kein Mitglied der isolierten Website sind, können keinen Zugriff auf die Website anfordern. Wenn sie versuchen, auf eine der Website zugeordnete URL zuzugreifen, wird eine Webseite mit der Meldung angezeigt, dass der Zugriff verweigert wurde.</span><span class="sxs-lookup"><span data-stu-id="ae26d-p103">Users who are not members of the isolated site cannot request access to the site. They will receive an access denied web page when they attempt to access any URL associated with the site.</span></span>
    
<span data-ttu-id="ae26d-p104">Der Nachteil beim Anfordern einer zentralen Zugriffssteuerung und von benutzerdefinierten Berechtigungen von SharePoint Online-Administratoren besteht darin, dass die Website isoliert bleibt. Beispielsweise können aktuelle Mitglieder weder absichtlich noch versehentlich andere Benutzer innerhalb des Office 365-Abonnements, die kein Mitglied der Website sein sollten, einladen oder benutzerdefinierte Berechtigungen für diese konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ae26d-p104">The tradeoff of requiring centralized access control and custom permissions by SharePoint Online administrators is that the site remains isolated over time. For example, current members cannot, either intentionally or accidentally, invite or configure custom permissions for other users within the Office 365 subscription who should not be members of the site.</span></span>
  
<span data-ttu-id="ae26d-122">Eine isolierte Website kann mit anderen Features wie z. B. den folgenden verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="ae26d-122">An isolated site can be used with other features, such as:</span></span>
  
- <span data-ttu-id="ae26d-123">Information Rights Management, um sicherzustellen, dass die Ressourcen auf der Website verschlüsselt bleiben, auch wenn sie lokal heruntergeladen und auf eine andere Website hochgeladen werden, die der gesamten Organisation zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="ae26d-123">Information Rights Management to ensure that the resources on the site remain encrypted, even if they are downloaded locally and uploaded to another site that is available to the entire organization.</span></span>
    
- <span data-ttu-id="ae26d-124">Verhinderung von Datenverlust, um Benutzer daran zu hindern, die Ressourcen der Website (z. B. Dateien) per E-Mail zu senden.</span><span class="sxs-lookup"><span data-stu-id="ae26d-124">Data loss prevention to prevent users from sending the resources of the site, such as files, in email.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="ae26d-125">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ae26d-125">Next steps</span></span>

<span data-ttu-id="ae26d-126">Wenn Sie eine isolierte SharePoint Online-Teamwebsite in einem Testabonnement ausprobieren möchten, finden Sie eine schrittweise Anleitung unter [Isolierte SharePoint Online-Teamwebsite in Ihrer Office 365-Entwicklungs-/Testumgebung](isolated-sharepoint-online-team-site-dev-test-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ae26d-126">To try out an isolated SharePoint Online team site in a trial subscription, see the step-by-step instructions in [Isolated SharePoint Online team site dev/test environment](isolated-sharepoint-online-team-site-dev-test-environment.md).</span></span>
  
<span data-ttu-id="ae26d-127">Wenn Sie eine isolierte SharePoint Online-Teamwebsite in der Produktion bereitstellen möchten, lesen Sie die schrittweisen Überlegungen zum Entwurf unter [Entwerfen einer isolierten SharePoint Online-Teamwebsite](design-an-isolated-sharepoint-online-team-site.md).</span><span class="sxs-lookup"><span data-stu-id="ae26d-127">When you are ready to deploy an isolated SharePoint Online team site in production, see the step-by-step design considerations in [Design an isolated SharePoint Online team site](design-an-isolated-sharepoint-online-team-site.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae26d-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae26d-128">See Also</span></span>

[<span data-ttu-id="ae26d-129">Entwerfen einer isolierten SharePoint Online-Teamwebsite</span><span class="sxs-lookup"><span data-stu-id="ae26d-129">Design an isolated SharePoint Online team site</span></span>](design-an-isolated-sharepoint-online-team-site.md)
  
[<span data-ttu-id="ae26d-130">Verwalten einer isolierten SharePoint Online-Teamwebsite</span><span class="sxs-lookup"><span data-stu-id="ae26d-130">Manage an isolated SharePoint Online team site</span></span>](manage-an-isolated-sharepoint-online-team-site.md)

[<span data-ttu-id="ae26d-131">Bereitstellen einer isolierten SharePoint Online-Teamwebsite</span><span class="sxs-lookup"><span data-stu-id="ae26d-131">Deploy an isolated SharePoint Online team site</span></span>](deploy-an-isolated-sharepoint-online-team-site.md)


