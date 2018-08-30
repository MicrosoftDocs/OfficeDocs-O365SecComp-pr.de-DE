---
title: Anzeigen der Berichtr zur Verhinderung von Datenverlust
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 6/7/2018
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 41eb4324-c513-4fa5-91c8-8fbd8aaba83b
description: Mit der DLP-Berichte in Office 365 können Sie schnell die Anzahl der DLP-Richtlinie entspricht, überschreibt oder falsch positive Ergebnisse anzeigen; sehen Sie, ob sie über einen Zeitraum nach oben oder unten Trend sind; Filtern Sie den Bericht auf unterschiedliche Weise. und weitere Details durch Auswählen eines Punkts in einer Zeile im Diagramm anzeigen.
ms.openlocfilehash: 379e66fc3f2611cf338739d030c2b1d48e7416d8
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "23013909"
---
# <a name="view-the-reports-for-data-loss-prevention"></a><span data-ttu-id="40c36-103">Anzeigen der Berichtr zur Verhinderung von Datenverlust</span><span class="sxs-lookup"><span data-stu-id="40c36-103">View the reports for data loss prevention</span></span>

<span data-ttu-id="40c36-p101">Nachdem Sie Ihre Data Loss Prevention (DLP) Richtlinien erstellen, sollten Sie sicherstellen, dass sie als Sie für die direkte Verwendung und hilft Ihnen, kompatibel bleiben arbeiten. Mit der DLP-Berichte in die Office 365-Sicherheit &amp; Compliance Center, Sie können schnell anzeigen:</span><span class="sxs-lookup"><span data-stu-id="40c36-p101">After you create your data loss prevention (DLP) policies, you'll want to verify that they're working as you intended and helping you to stay compliant. With the DLP reports in the Office 365 Security &amp; Compliance Center, you can quickly view:</span></span>
  
- <span data-ttu-id="40c36-p102">**DLP-richtlinienübereinstimmungen** In diesem Bericht werden die Anzahl der Übereinstimmungen mit DLP-Richtlinie über einen Zeitraum. Sie können den Bericht nach Datum, Position, Richtlinie oder Aktion filtern. Sie können diesen Bericht verwenden:</span><span class="sxs-lookup"><span data-stu-id="40c36-p102">**DLP policy matches** This report shows the count of DLP policy matches over time. You can filter the report by date, location, policy, or action. You can use this report to:</span></span> 
    
  - <span data-ttu-id="40c36-p103">Feinabstimmung oder verfeinern Ihrer DLP-Richtlinien, wie Sie sie im Testmodus ausführen. Sie können die Regel anzeigen, die den Inhalt abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="40c36-p103">Tune or refine your DLP policies as you run them in test mode. You can view the specific rule that matched the content.</span></span>
    
  - <span data-ttu-id="40c36-111">Sie können sich auf bestimmte Zeiträume konzentrieren und so mehr über die Gründe für Spitzen und Trends erfahren.</span><span class="sxs-lookup"><span data-stu-id="40c36-111">Focus on specific time periods and understand the reasons for spikes and trends.</span></span>
    
  - <span data-ttu-id="40c36-112">Entdecken von Geschäftsprozessen, die Ihre Organisation DLP-Richtlinien verletzen.</span><span class="sxs-lookup"><span data-stu-id="40c36-112">Discover business processes that violate your organization's DLP policies.</span></span>
    
  - <span data-ttu-id="40c36-113">Verstehen Sie alle geschäftliche Relevanz des DLP-Richtlinien von sehen, welche Aktionen auf Inhalte angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="40c36-113">Understand any business impact of the DLP policies by seeing what actions are being applied to content.</span></span>
    
  - <span data-ttu-id="40c36-114">Sie können die Einhaltung einer bestimmten DLP-Richtlinie durch Anzeigen von Übereinstimmungen für diese Richtlinie überprüfen.</span><span class="sxs-lookup"><span data-stu-id="40c36-114">Verify compliance with a specific DLP policy by showing any matches for that policy.</span></span>
    
  - <span data-ttu-id="40c36-115">Anzeigen einer Liste der wichtigsten Benutzer, und wiederholen Sie die Benutzer, die auf Vorfälle in Ihrer Organisation beitragen.</span><span class="sxs-lookup"><span data-stu-id="40c36-115">View a list of top users and repeat users who are contributing to incidents in your organization.</span></span>
    
  - <span data-ttu-id="40c36-116">Hier wird eine Liste der oberen Arten von vertraulichen Informationen in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="40c36-116">View a list of the top types of sensitive information in your organization.</span></span>
    
- <span data-ttu-id="40c36-p104">**DLP-Vorfälle** In diesem Bericht werden auch Richtlinie Übereinstimmungen im Laufe der Zeit ein, wie die Richtlinie Bericht übereinstimmt. Die Richtlinie entspricht jedoch Bericht zeigt Übereinstimmungen auf einer Regelebene. Wenn eine e-Mail-Nachricht auf drei verschiedene Regeln entspricht, entspricht die Richtlinie beispielsweise Bericht zeigt drei verschiedene Zeilenelemente. Im Gegensatz dazu zeigt der Bericht Vorfälle Übereinstimmungen auf einer Elementebene; Beispielsweise zeigt Übereinstimmung eine e-Mail mit drei verschiedene Regeln, der Bericht Vorfälle ein einzelnes Line-Element für diesen Teil des Inhalts.</span><span class="sxs-lookup"><span data-stu-id="40c36-p104">**DLP incidents** This report also shows policy matches over time, like the policy matches report. However, the policy matches report shows matches at a rule level; for example, if an email matched three different rules, the policy matches report shows three different line items. By contrast, the incidents report shows matches at an item level; for example, if an email matched three different rules, the incidents report shows a single line item for that piece of content.</span></span> 
    
  <span data-ttu-id="40c36-p105">Da die Zahlen im Bericht unterschiedlich aggregiert werden, ist der Richtlinie Übereinstimmungen Bericht besser zum Identifizieren von Übereinstimmungen mit bestimmten Regeln und Feinabstimmung DLP-Richtlinien. Der Bericht Vorfälle ist besser geeignet, die bestimmte Teile des Inhalts, die für die DLP-Richtlinien problematisch sind identifiziert.</span><span class="sxs-lookup"><span data-stu-id="40c36-p105">Because the report counts are aggregated differently, the policy matches report is better for identifying matches with specific rules and fine tuning DLP policies. The incidents report is better for identifying specific pieces of content that are problematic for your DLP policies.</span></span>
    
- <span data-ttu-id="40c36-p106">**Falsch positive Ergebnisse DLP und überschreibt** Wenn DLP-Richtlinie Benutzern ermöglicht das Überschreiben oder ein falsch positives Ergebnis angeben, wird in diesem Bericht Anzahl der solche Instanzen im Zeitverlauf. Sie können den Bericht nach Datum, Standort oder Richtlinie filtern. Sie können diesen Bericht verwenden:</span><span class="sxs-lookup"><span data-stu-id="40c36-p106">**DLP false positives and overrides** If your DLP policy allows users to override it or report a false positive, this report shows a count of such instances over time. You can filter the report by date, location, or policy. You can use this report to:</span></span> 
    
  - <span data-ttu-id="40c36-125">Feinabstimmung oder Ihrer DLP-Richtlinien verfeinern, indem Sie sehen, welche Richtlinien eine hohe Anzahl von falsch positive Ergebnisse entstehen.</span><span class="sxs-lookup"><span data-stu-id="40c36-125">Tune or refine your DLP policies by seeing which policies incur a high number of false positives.</span></span>
    
  - <span data-ttu-id="40c36-126">Zeigen Sie die Nachweise von Benutzern gesendet werden, wenn sie einen richtlinientipp beheben, indem Sie die Richtlinie zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="40c36-126">View the justifications submitted by users when they resolve a policy tip by overriding the policy.</span></span>
    
  - <span data-ttu-id="40c36-127">Entdecken Sie die DLP-Richtlinien Konflikt mit gültigen Geschäftsprozesse durch eine hohe Anzahl von Benutzer tätigen, in dem außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="40c36-127">Discover where DLP policies conflict with valid business processes by incurring a high number of user overrides.</span></span>
    
<span data-ttu-id="40c36-p107">Alle DLP-Berichte können Daten aus der letzten vier Monat Zeitraum anzeigen. Die aktuellsten Daten dauert bis zu 24 Stunden in den Berichten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="40c36-p107">All DLP reports can show data from the most recent four-month time period. The most recent data can take up to 24 hours to appear in the reports.</span></span>
  
<span data-ttu-id="40c36-130">Sie finden diese Berichte in das Wertpapier &amp; Compliance Center \> **Berichte** \> **Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="40c36-130">You can find these reports in the Security &amp; Compliance Center \> **Reports** \> **Dashboard**.</span></span>
  
![DLP-richtlinienübereinstimmungen Bericht](media/117d20c9-d379-403f-ad68-1f5cd6c4e5cf.png)
  
## <a name="view-the-justification-submitted-by-a-user-for-an-override"></a><span data-ttu-id="40c36-132">Zeigen Sie die Ausrichtung eines Benutzers für eine Außerkraftsetzung übermittelten an</span><span class="sxs-lookup"><span data-stu-id="40c36-132">View the justification submitted by a user for an override</span></span>

<span data-ttu-id="40c36-133">Wenn DLP-Richtlinie außer Kraft setzen, Benutzer zulässt, können Sie das false positive Ergebnis verwenden und Überschreiben des Berichts, um den Text von Benutzern in den richtlinientipp übermittelt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="40c36-133">If your DLP policy allows users to override it, you can use the false positive and override report to view the text submitted by users in the policy tip.</span></span>
  
![Begründung Feld in den Details der DLP falsch positives Ergebnis und Außerkraftsetzung Bericht](media/e11e3126-026d-4e77-a16d-74a0686d1fa3.png)
  
## <a name="take-action-on-insights-and-recommendations"></a><span data-ttu-id="40c36-135">Ausführen einer Aktion auf Insights und Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="40c36-135">Take action on insights and recommendations</span></span>

<span data-ttu-id="40c36-136">Berichte können anzeigen, Insights und Empfehlungen, in dem können Sie auf das rote Symbol finden Sie unter Details zur Ermittlung möglicher Probleme und mögliche Abhilfemaßnahmen übernehmen klicken.</span><span class="sxs-lookup"><span data-stu-id="40c36-136">Reports can show insights and recommendations where you can click the red warning icon to see details about potential issues and take possible remedial action.</span></span>
  
![Durch Klicken auf ein Insights-Symbol, um Details und Aktionen finden Sie unter](media/51782036-7299-4960-8175-75c2b1637159.png)
  
## <a name="find-the-cmdlets-for-the-dlp-reports"></a><span data-ttu-id="40c36-138">Hier finden Sie die Cmdlets für die DLP-Berichte</span><span class="sxs-lookup"><span data-stu-id="40c36-138">Find the cmdlets for the DLP reports</span></span>

<span data-ttu-id="40c36-139">Die meisten der Cmdlets für die Sicherheit zu verwendenden &amp; Compliance Center, müssen Sie:</span><span class="sxs-lookup"><span data-stu-id="40c36-139">To use most of the cmdlets for the Security &amp; Compliance Center, you need to:</span></span>
  
1. [<span data-ttu-id="40c36-140">Verbinden mit der Office 365-Sicherheit &amp; Compliance Center mit remote-PowerShell</span><span class="sxs-lookup"><span data-stu-id="40c36-140">Connect to the Office 365 Security &amp; Compliance Center using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799771&amp;clcid=0x409)
    
2. <span data-ttu-id="40c36-141">Verwenden Sie eine der folgenden [Sicherheit in Office 365 &amp; Compliance Center Cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span><span class="sxs-lookup"><span data-stu-id="40c36-141">Use any of these [Office 365 Security &amp; Compliance Center cmdlets](http://go.microsoft.com/fwlink/?LinkID=799772&amp;clcid=0x409)</span></span>
    
<span data-ttu-id="40c36-p108">DLP-Berichte müssen jedoch Daten aus über Office 365, einschließlich Exchange Online ziehen. Aus diesem Grund stehen die Cmdlets für die DLP-Berichte in Exchange Online Powershell – nicht in Security &amp; Compliance Center Powershell. Aus diesem Grund müssen für die Verwendung von Cmdlets für die DLP-Berichte:</span><span class="sxs-lookup"><span data-stu-id="40c36-p108">However, DLP reports need pull data from across Office 365, including Exchange Online. For this reason, the cmdlets for the DLP reports are available in Exchange Online Powershell—not in Security &amp; Compliance Center Powershell. Therefore, to use the cmdlets for the DLP reports, you need to:</span></span>
  
1. [<span data-ttu-id="40c36-145">Connect to Exchange Online using remote PowerShell</span><span class="sxs-lookup"><span data-stu-id="40c36-145">Connect to Exchange Online using remote PowerShell</span></span>](http://go.microsoft.com/fwlink/?LinkID=799773&amp;clcid=0x409)
    
2. <span data-ttu-id="40c36-146">Verwenden Sie eine dieser Cmdlets für die DLP-Berichte:</span><span class="sxs-lookup"><span data-stu-id="40c36-146">Use any of these cmdlets for the DLP reports:</span></span>
    
      - [<span data-ttu-id="40c36-147">Get-DlpDetectionsReport</span><span class="sxs-lookup"><span data-stu-id="40c36-147">Get-DlpDetectionsReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799774&amp;clcid=0x409)
    
      - [<span data-ttu-id="40c36-148">Get-DlpDetailReport</span><span class="sxs-lookup"><span data-stu-id="40c36-148">Get-DlpDetailReport</span></span>](http://go.microsoft.com/fwlink/?LinkID=799775&amp;clcid=0x409)
    

