---
title: Office 365-Sicherheitsbewertung
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: Admin
ms.topic: overview
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Fragen Sie sich, wie sicher Ihre Organisation wirklich in Office 365 ist? Secure Score steht Ihnen zur Verfügung. Secure Score analysiert die Sicherheit Ihrer Organisation basierend auf Ihren regulären Aktivitäten und Sicherheitseinstellungen in Office 365 und weist eine Bewertung zu.
ms.openlocfilehash: dd0dc87910853eba9f2ec3ec6752e857462b46e5
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32262457"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="a7b05-105">Office 365-Sicherheitsbewertung</span><span class="sxs-lookup"><span data-stu-id="a7b05-105">Office 365 Secure Score</span></span>

<span data-ttu-id="a7b05-106">**Zusammenfassung** Fragen Sie sich, wie sicher Ihre Organisation wirklich in Office 365 ist?</span><span class="sxs-lookup"><span data-stu-id="a7b05-106">**Summary** Ever wonder how secure your organization really is in Office 365?</span></span> <span data-ttu-id="a7b05-107">Secure Score steht Ihnen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="a7b05-107">Secure Score is here to help.</span></span> <span data-ttu-id="a7b05-108">Secure Score analysiert die Sicherheit Ihrer Organisation basierend auf Ihren regulären Aktivitäten und Sicherheitseinstellungen in Office 365 und weist eine Bewertung zu.</span><span class="sxs-lookup"><span data-stu-id="a7b05-108">Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score.</span></span> <span data-ttu-id="a7b05-109">Lesen Sie diesen Artikel, um einen Überblick über die sichere Bewertung und ihre Verwendung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a7b05-109">Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="a7b05-110">So gelangen Sie zu Secure Score</span><span class="sxs-lookup"><span data-stu-id="a7b05-110">How to get to Secure Score</span></span>

<span data-ttu-id="a7b05-111">Wenn Ihre Organisation über ein Abonnement mit [office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 business](https://docs.microsoft.com/microsoft-365/business/)oder Office 365 Business Premium verfügt und Sie über die [erforderlichen Berechtigungen](#required-permissions)verfügen, können Sie die sichere Bewertung Ihrer Organisation anzeigen, indem Sie [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="a7b05-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="a7b05-112">Alternativ können Sie das Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) besuchen, in dem Sie ein sicheres Bewertungs-Widget finden, das Ihnen Ihre aktuelle Bewertung liefert.</span><span class="sxs-lookup"><span data-stu-id="a7b05-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![Widget "Secure Score"](media/SecureScoreWidget-o365.png)

<span data-ttu-id="a7b05-114">Das Widget enthält einen Link zu Ihrem Secure Score Dashboard.</span><span class="sxs-lookup"><span data-stu-id="a7b05-114">The widget includes a link to your Secure Score dashboard.</span></span>

![Secure Score Dashboard](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="a7b05-116">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="a7b05-116">How it works</span></span>

<span data-ttu-id="a7b05-117">Secure Score bestimmt, welche Office 365-Dienste Sie verwenden (beispielsweise OneDrive, SharePoint und Exchange), dann werden Ihre Einstellungen und Aktivitäten mit einer von Microsoft erstellten Baseline verglichen.</span><span class="sxs-lookup"><span data-stu-id="a7b05-117">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft.</span></span> <span data-ttu-id="a7b05-118">Sie erhalten eine Bewertung, die darauf basiert, wie gut Ihre Organisation mit bewährten Sicherheitsmethoden ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="a7b05-118">You'll get a score based on how well aligned your organization is with security best practices.</span></span> <span data-ttu-id="a7b05-119">Außerdem erhalten Sie Empfehlungen zu den Schritten, die Sie zur Verbesserung der Bewertung Ihrer Organisation ergreifen können.</span><span class="sxs-lookup"><span data-stu-id="a7b05-119">You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![Aktions Warteschlange im Office 365 Secure Score Tool](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="a7b05-121">Secure Score berechnet Ihre Punktzahl basierend auf den von Ihnen erworbenen Diensten.</span><span class="sxs-lookup"><span data-stu-id="a7b05-121">Secure Score calculates your score based on the services you purchased.</span></span> <span data-ttu-id="a7b05-122">Wenn Sie beispielsweise nur einen Exchange Online-Plan erworben haben, werden Sie nicht für SharePoint Online-Sicherheitsfeatures gewertet.</span><span class="sxs-lookup"><span data-stu-id="a7b05-122">For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features.</span></span> <span data-ttu-id="a7b05-123">Der Nenner der Bewertung ist die Summe aller Basispläne für die Steuerelemente, die für die von Ihnen erworbenen Produkte gelten.</span><span class="sxs-lookup"><span data-stu-id="a7b05-123">The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased.</span></span> <span data-ttu-id="a7b05-124">Der Zähler ist die Summe aller Steuerelemente, für die Sie die Aktionen zur Erfüllung dieses Steuerelements abgeschlossen oder teilweise abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="a7b05-124">The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="a7b05-125">Erweitern Sie eine Aktion, um zu erfahren, welche Schritte durchgeführt werden sollen, welche Bedrohungen Sie schützen und wie viele Punkte Ihre Punktzahl erhöhen wird, wenn Sie die Empfehlung befolgen.</span><span class="sxs-lookup"><span data-stu-id="a7b05-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Erweiterte Aktion im Office 365 Secure Score Tool](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="a7b05-127">Um die Auswirkungen ihrer Aktionen auf die Sicherheit Ihrer Organisation anzuzeigen, wählen Sie die Registerkarte **Score Analyzer** aus, und überprüfen Sie Ihren Verlauf.</span><span class="sxs-lookup"><span data-stu-id="a7b05-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Score Analyzer-Registerkarte des Office 365 Secure Score Tool](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="a7b05-129">Unterhalb des Diagramms sehen Sie eine Liste der Bewertungen und Aktionen nach Kategorie.</span><span class="sxs-lookup"><span data-stu-id="a7b05-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![Diagramm auf der Registerkarte Score Analyzer mit ausgewähltem Datenpunkt](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="a7b05-131">Aktionen, die als **[nicht erzielt]** bezeichnet werden, sind diejenigen, die Sie für Ihre Organisation ausführen können, aber weil Sie nicht mit Secure Score verbunden sind, werden Sie nicht gewertet.</span><span class="sxs-lookup"><span data-stu-id="a7b05-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="a7b05-132">Klicken Sie auf der Seite **Score Analyzer** auf einen Datenpunkt für einen bestimmten Tag, und führen Sie einen Bildlauf nach unten durch, um die abgeschlossenen und unvollständigen Aktionen für diesen Tag anzuzeigen, um zu erfahren, was geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a7b05-132">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed.</span></span> <span data-ttu-id="a7b05-133">Die Bewertung wird einmal pro Tag berechnet (um 1:00 Uhr PST).</span><span class="sxs-lookup"><span data-stu-id="a7b05-133">The score is calculated once per day (around 1:00 AM PST).</span></span> <span data-ttu-id="a7b05-134">Wenn Sie eine Änderung an einer gemessenen Aktion vornehmen, wird die Partitur automatisch am nächsten Tag aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a7b05-134">If you make a change to a measured action, the score will automatically update the next day.</span></span> <span data-ttu-id="a7b05-135">Es dauert bis zu 48 Stunden, bis eine Änderung in ihrer Bewertung reflektiert wird.</span><span class="sxs-lookup"><span data-stu-id="a7b05-135">It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="a7b05-136">Secure Score drückt nicht aus, wie wahrscheinlich Sie verletzt werden.</span><span class="sxs-lookup"><span data-stu-id="a7b05-136">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="a7b05-137">Er gibt an, in welchem Maße Sie Features übernommen haben, die das Risiko von Verstößen kompensieren können.</span><span class="sxs-lookup"><span data-stu-id="a7b05-137">It expresses the extent to which you have adopted features that can offset the risk of being breached.</span></span> <span data-ttu-id="a7b05-138">Kein Dienst kann garantieren, dass Sie nicht verletzt werden, und die Secure Score sollte nicht als Garantie interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7b05-138">No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="a7b05-139">Wie Secure Score hilft</span><span class="sxs-lookup"><span data-stu-id="a7b05-139">How Secure Score helps</span></span>

<span data-ttu-id="a7b05-140">Mit Secure Score können Sie zur Verbesserung der Sicherheit Ihrer Organisation beitragen, indem Sie die integrierten Sicherheitsfunktionen in Office 365 verwenden (viele von denen Sie bereits erworben haben, aber möglicherweise nicht wissen).</span><span class="sxs-lookup"><span data-stu-id="a7b05-140">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of).</span></span> <span data-ttu-id="a7b05-141">Wenn Sie mehr über diese Features erfahren, können Sie sich beruhigen, dass Sie die richtigen Schritte Unternehmen, um Ihre Organisation vor Bedrohungen zu schützen.</span><span class="sxs-lookup"><span data-stu-id="a7b05-141">Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="a7b05-142">Aber nehmen Sie nicht einfach unser Wort dafür.</span><span class="sxs-lookup"><span data-stu-id="a7b05-142">But don't just take our word for it.</span></span> <span data-ttu-id="a7b05-143">Kunden, die Secure Score verwenden, haben Ihre Punktzahl fünfmal höher gestiegen als Kunden, die Sie nicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="a7b05-143">Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it.</span></span> <span data-ttu-id="a7b05-144">(Die Aufstockung ihrer Bewertung entspricht den Sicherheitsfeatures, die in ihren Organisationen verwendet werden.)</span><span class="sxs-lookup"><span data-stu-id="a7b05-144">(The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="a7b05-145">Secure Score drückt nicht aus, wie wahrscheinlich Sie verletzt werden.</span><span class="sxs-lookup"><span data-stu-id="a7b05-145">Secure Score does not express an absolute measure of how likely you are to get breached.</span></span> <span data-ttu-id="a7b05-146">Er gibt an, in welchem Umfang Sie Steuerelemente übernommen haben, die das Risiko von Verstößen kompensieren können.</span><span class="sxs-lookup"><span data-stu-id="a7b05-146">It expresses the extent to which you have adopted controls which can offset the risk of being breached.</span></span> <span data-ttu-id="a7b05-147">Kein Dienst kann garantieren, dass Sie nicht verletzt werden, und Secure Score sollte nicht als Garantie interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7b05-147">No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="a7b05-148">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="a7b05-148">Required permissions</span></span>

<span data-ttu-id="a7b05-149">Sie müssen eine der folgenden Rollen in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles)besitzen, um das Dashboard für sichere Bewertungen anzeigen und verwenden zu können:</span><span class="sxs-lookup"><span data-stu-id="a7b05-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in [Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles#available-roles):</span></span>
- <span data-ttu-id="a7b05-150">Globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="a7b05-150">Global Administrator</span></span>
- <span data-ttu-id="a7b05-151">Rechnungs Administrator</span><span class="sxs-lookup"><span data-stu-id="a7b05-151">Billing Administrator</span></span>
- <span data-ttu-id="a7b05-152">Benutzer Administrator</span><span class="sxs-lookup"><span data-stu-id="a7b05-152">User Administrator</span></span>
- <span data-ttu-id="a7b05-153">Kenn Wort Administrator</span><span class="sxs-lookup"><span data-stu-id="a7b05-153">Password Administrator</span></span>
- <span data-ttu-id="a7b05-154">Sicherheitsadministrator</span><span class="sxs-lookup"><span data-stu-id="a7b05-154">Security Administrator</span></span>
- <span data-ttu-id="a7b05-155">Sicherheits Leser</span><span class="sxs-lookup"><span data-stu-id="a7b05-155">Security Reader</span></span>
- <span data-ttu-id="a7b05-156">Exchange-Administrator</span><span class="sxs-lookup"><span data-stu-id="a7b05-156">Exchange Administrator</span></span>
- <span data-ttu-id="a7b05-157">SharePoint-Administrator</span><span class="sxs-lookup"><span data-stu-id="a7b05-157">SharePoint Administrator</span></span>

 <span data-ttu-id="a7b05-158">Benutzer, denen keine Administratorrolle zugewiesen ist, können nicht auf Secure Score zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a7b05-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7b05-159">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="a7b05-159">Related topics</span></span>

[<span data-ttu-id="a7b05-160">Übersicht über das Sicherheits Dashboard</span><span class="sxs-lookup"><span data-stu-id="a7b05-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="a7b05-161">Welches Abonnement habe ich?</span><span class="sxs-lookup"><span data-stu-id="a7b05-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)
