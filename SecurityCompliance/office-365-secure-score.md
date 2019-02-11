---
title: Office 365 Secure Score
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/25/2019
ms.audience: Admin
ms.topic: overview
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: c9e7160f-2c34-4bd0-a548-5ddcc862eaef
description: Haben Sie sich je gefragt, wie sicher Ihre Organisation wirklich in Office 365 ist? Sichere Faktor ist hier helfen. Sichere Faktor Sicherheit Ihrer Organisation basierend auf Ihren regulären Aktivitäten und Sicherheitseinstellungen in Office 365 analysiert und weist eine Bewertung.
ms.openlocfilehash: bc0379e40b09e63e5fded1b1a289d40c306def91
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29559088"
---
# <a name="office-365-secure-score"></a><span data-ttu-id="cbbbb-105">Office 365 Secure Score</span><span class="sxs-lookup"><span data-stu-id="cbbbb-105">Office 365 Secure Score</span></span>

<span data-ttu-id="cbbbb-p102">**Zusammenfassung** Haben Sie sich je gefragt, wie sicher Ihre Organisation wirklich in Office 365 ist? Sichere Faktor ist hier helfen. Sichere Faktor Sicherheit Ihrer Organisation basierend auf Ihren regulären Aktivitäten und Sicherheitseinstellungen in Office 365 analysiert und weist eine Bewertung. Lesen Sie diesen Artikel, um einen Überblick über Secure Score und wie Sie es verwenden können.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-p102">**Summary** Ever wonder how secure your organization really is in Office 365? Secure Score is here to help. Secure Score analyzes your organization's security  based on your regular activities and security settings in Office 365, and assigns a score. Read this article to get an overview of Secure Score and how you can use it.</span></span>
  
## <a name="how-to-get-to-secure-score"></a><span data-ttu-id="cbbbb-110">Wie Sie Secure integritätsbewertung abrufen</span><span class="sxs-lookup"><span data-stu-id="cbbbb-110">How to get to Secure Score</span></span>

<span data-ttu-id="cbbbb-111">Wenn Ihre Organisation verfügt ein Abonnement, die [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/)oder Office 365 Business Premium enthält und Sie über die [erforderlichen Berechtigungen](#required-permissions)verfügen, können Sie Ihrer Organisation sichere Score Vorsichtsmaßnahmen anzeigen. [https://securescore.office.com](https://securescore.office.com).</span><span class="sxs-lookup"><span data-stu-id="cbbbb-111">If your organization has a subscription that includes [Office 365 Enterprise](https://docs.microsoft.com/office365/enterprise/), [Microsoft 365 Business](https://docs.microsoft.com/microsoft-365/business/), or Office 365 Business Premium, and you have the [necessary permissions](#required-permissions), you can view your organization's secure score by visiting [https://securescore.office.com](https://securescore.office.com).</span></span> 

<span data-ttu-id="cbbbb-112">Alternativ können Sie die Sicherheit & Compliance Center besuchen ([https://protection.office.com](https://protection.office.com)), in der Sie ein Secure Score-Widget finden, die Sie mit Ihr aktuelles Ergebnis bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-112">Alternatively, you can visit the Security & Compliance Center ([https://protection.office.com](https://protection.office.com)), where you'll find a Secure Score widget that provides you with your current score.</span></span>

![Sichere Score widget](media/SecureScoreWidget-o365.png)

<span data-ttu-id="cbbbb-114">Das Widget enthält einen Link zum Dashboard Score sichern.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-114">The widget includes a link to your Secure Score dashboard.</span></span>

![Sichere Score-dashboard](media/SecureScore-WelcomeScreen.png)
  
## <a name="how-it-works"></a><span data-ttu-id="cbbbb-116">Funktionsweise</span><span class="sxs-lookup"><span data-stu-id="cbbbb-116">How it works</span></span>

<span data-ttu-id="cbbbb-p103">Sichere Score bestimmt, welche Office 365-Dienste (beispielsweise OneDrive, SharePoint und Exchange) dann verwendeten verglichen Ihrer Einstellungen und die Aktivitäten aus, die einen Basisplan von Microsoft hergestellt wird. Sie erhalten einen Faktor basierend auf wie gut ausgerichtet mit bewährten Methoden für die Sicherheit Ihrer Organisation ist. Sie erhalten auch Empfehlungen zu den erforderlichen Schritten, die Sie ergreifen können, um Ihr Unternehmen zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-p103">Secure Score determines what Office 365 services you're using (such as OneDrive, SharePoint, and Exchange) then compares your settings and activities to a baseline established by Microsoft. You'll get a score based on how well aligned your organization is with security best practices. You'll also get recommendations on steps you can take to improve your organization's score.</span></span> 
  
![Aktionen Warteschlange im Office 365 Secure Score-tool](media/SecureScore-ActionsToTake.png)
  
<span data-ttu-id="cbbbb-p104">Sichere Score berechnet Ihr Ergebnis basierend auf den Diensten, die Sie erworben haben. Angenommen, wenn Sie nur einen Exchange Online-Plan erworben haben, werden nicht Sie für SharePoint Online-Sicherheitsfeatures bewertet werden. Die als Nenner für die Bewertung ist die Summe der alle Baselines für die Steuerelemente, die für die Produkte gelten, die Sie erworben haben. Der Zähler ist die Summe aller Steuerelemente, für die Sie abgeschlossen, oder teilweise abgeschlossen, die Aktionen für das jeweilige Steuerelement zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-p104">Secure Score calculates your score based on the services you purchased. For example, if you only purchased an Exchange Online plan, you won't be scored for SharePoint Online security features. The denominator of the score is the sum of all the baselines for the controls that apply to the products you purchased. The numerator is the sum of all the controls for which you completed, or partially completed, the actions to fulfill that control.</span></span>

<span data-ttu-id="cbbbb-125">Erweitern Sie eine Aktion, um zu erfahren, welche Schritte an, die Gefahren, die geschützt werden müssen Sie aus, und zeigt, wie viele Ihre Punktzahl erhöht wird, nachdem Sie die Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-125">Expand an action to learn about what steps to take, the threats it'll help protect you from, and how many points your score will increase once you follow the recommendation.</span></span>
  
![Erweiterte Aktion im Office 365 Secure Score-tool](media/SecureScore-DetailedActionToTake.png)
  
<span data-ttu-id="cbbbb-127">Um die Auswirkungen von Ihren Aktionen auf Sicherheit Ihrer Organisation anzuzeigen, wählen Sie die Registerkarte **Score Analyzer** , und überprüfen Sie den Verlauf.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-127">To see the impact of your actions on your organization's security, select the **Score Analyzer** tab and review your history.</span></span> 
  
![Faktor Analyzer Registerkarte des Office 365 Secure Score-Tools](media/SecureScore-ScoreAnalyzer-7days.png)
  
<span data-ttu-id="cbbbb-129">Unter dem Diagramm sehen Sie eine Liste der Faktoren und Aktionen nach Kategorie.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-129">Below the chart, you'll see a list of scores and actions by category.</span></span> 
  
![Diagramm auf der Score Analyzer Registerkarte zeigt einen Datenpunkt ausgewählt](media/SecureScore-Analyzer-breakdownbelowchart.png)
 
<span data-ttu-id="cbbbb-131">Aktionen, die als **[Nicht bewertet]** sind gekennzeichnet sind, die Sie für Ihre Organisation ausführen können, aber, da sie nicht sichere Score verbunden sind, werden sie nicht bewertet.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-131">Actions that are labeled as **[Not Scored]** are ones you can perform for your organization, but because they are not connected to Secure Score, they are not scored.</span></span>  

<span data-ttu-id="cbbbb-p105">Klicken Sie auf der Seite **Score Analyzer** auf einen Datenpunkt für einen bestimmten Tag, und klicken Sie dann einen Bildlauf nach unten zu finden, die für diesen Tag zu erfahren, welche Aktionen abgeschlossenen und unvollständigen geändert. Die Bewertung wird einmal pro Tag (etwa 1:00 Uhr PST) berechnet. Wenn Sie eine Änderung an einer gemessene Aktion vornehmen, wird die Bewertung den nächsten Tag automatisch aktualisiert. Es dauert bis zu 48 Stunden für eine Änderung in Ihr Ergebnis übernommen werden.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-p105">On the **Score Analyzer** page, click a data point for a specific day, then scroll down to see the completed and incomplete actions for that day to find out what changed. The score is calculated once per day (around 1:00 AM PST). If you make a change to a measured action, the score will automatically update the next day. It takes up to 48 hours for a change to be reflected in your score.</span></span>

<span data-ttu-id="cbbbb-p106">Sichere Score ist nicht express eine absolute Maßeinheit des wie wahrscheinlich generiertes abgerufen werden sollen. Dieser drückt des Umfang an dem Features eingeführt haben, die das Risiko wird generiertes versetzt werden können. Kein Dienst kann sicherstellen, dass Sie nicht verletzt werden, und die Bewertung Secure nicht als keinerlei Garantie interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-p106">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted features that can offset the risk of being breached. No service can guarantee that you will not be breached, and the Secure Score should not be interpreted as a guarantee in any way.</span></span>
 
## <a name="how-secure-score-helps"></a><span data-ttu-id="cbbbb-139">Schutzmechanismen in Secure Score</span><span class="sxs-lookup"><span data-stu-id="cbbbb-139">How Secure Score helps</span></span>

<span data-ttu-id="cbbbb-p107">Mit Secure Faktor können Sie verbessern Sicherheitsstatus Ihrer Organisation mithilfe der integrierten Sicherheitsfeatures in Office 365 (von denen Sie bereits erworben haben aber möglicherweise nicht bekannt). Weitere Informationen zu diesen Features kann ermöglichen Ihnen Gewissheit, dass Sie die richtigen Maßnahmen für Ihre Organisation vor Angriffen zu schützen einnehmen.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-p107">With Secure Score, you can help improve your organization's security posture by using the built-in security features in Office 365 (many of which you already purchased but might not be aware of). Learning more about these features can help give you peace of mind that you're taking the right steps to protect your organization from threats.</span></span>
  
<span data-ttu-id="cbbbb-p108">Aber nicht einfach Probieren Sie es. Kunden, die mithilfe von Secure Score haben ihre Score fünfmaliges mehr als Kunden zu erhöhen, die sie nutzen sind nicht sichtbar. (Die Anhebung der dem Faktor entspricht mit den Sicherheitsfunktionen in ihren Organisationen verwendet wird.)</span><span class="sxs-lookup"><span data-stu-id="cbbbb-p108">But don't just take our word for it. Customers who are using Secure Score have seen their score increase five times more than customers who aren't using it. (The increase in their score corresponds with the security features being used in their organizations.)</span></span>
  
> [!NOTE]
> <span data-ttu-id="cbbbb-p109">Sichere Score ist nicht express eine absolute Maßeinheit des wie wahrscheinlich generiertes abgerufen werden sollen. Dieser drückt des Umfang an dem Steuerelemente eingeführt haben die generiertes wird das Risiko offset können. Kein Dienst kann sicherstellen, dass Sie nicht verletzt werden, und Secure Score nicht als keinerlei Garantie interpretiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-p109">Secure Score does not express an absolute measure of how likely you are to get breached. It expresses the extent to which you have adopted controls which can offset the risk of being breached. No service can guarantee that you will not be breached, and Secure Score should not be interpreted as a guarantee in any way.</span></span> 
  
## <a name="required-permissions"></a><span data-ttu-id="cbbbb-148">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="cbbbb-148">Required permissions</span></span>

<span data-ttu-id="cbbbb-149">Zum Anzeigen und verwenden Sie das Dashboard Score Secure, müssen Sie eine der folgenden Rollen in Azure Active Directory zugewiesen werden:</span><span class="sxs-lookup"><span data-stu-id="cbbbb-149">In order to view and use your Secure Score dashboard, you must be assigned one of the following roles in Azure Active Directory:</span></span>
- <span data-ttu-id="cbbbb-150">Globaler Administrator</span><span class="sxs-lookup"><span data-stu-id="cbbbb-150">Global Administrator</span></span>
- <span data-ttu-id="cbbbb-151">Abrechnungsadministrator</span><span class="sxs-lookup"><span data-stu-id="cbbbb-151">Billing Administrator</span></span>
- <span data-ttu-id="cbbbb-152">Benutzeradministrator</span><span class="sxs-lookup"><span data-stu-id="cbbbb-152">User Administrator</span></span>
- <span data-ttu-id="cbbbb-153">Kennwort-Administrator</span><span class="sxs-lookup"><span data-stu-id="cbbbb-153">Password Administrator</span></span>
- <span data-ttu-id="cbbbb-154">Sicherheitsadministrator</span><span class="sxs-lookup"><span data-stu-id="cbbbb-154">Security Administrator</span></span>
- <span data-ttu-id="cbbbb-155">Sicherheit-Reader</span><span class="sxs-lookup"><span data-stu-id="cbbbb-155">Security Reader</span></span>
- <span data-ttu-id="cbbbb-156">Exchange-Administrator</span><span class="sxs-lookup"><span data-stu-id="cbbbb-156">Exchange Administrator</span></span>
- <span data-ttu-id="cbbbb-157">SharePoint-Administrator</span><span class="sxs-lookup"><span data-stu-id="cbbbb-157">SharePoint Administrator</span></span>

 <span data-ttu-id="cbbbb-158">Benutzer, die Admin-Rolle zugewiesen sind nicht auf Secure Score zugreifen.</span><span class="sxs-lookup"><span data-stu-id="cbbbb-158">Users who aren't assigned an admin role won't be able to access Secure Score.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cbbbb-159">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="cbbbb-159">Related topics</span></span>

[<span data-ttu-id="cbbbb-160">Übersicht über die Sicherheit-dashboard</span><span class="sxs-lookup"><span data-stu-id="cbbbb-160">Security dashboard overview</span></span>](security-dashboard.md)

[<span data-ttu-id="cbbbb-161">Welches Abonnement habe ich?</span><span class="sxs-lookup"><span data-stu-id="cbbbb-161">What subscription do I have?</span></span>](https://docs.microsoft.com/office365/admin/admin-overview/what-subscription-do-i-have?view=o365-worldwide)