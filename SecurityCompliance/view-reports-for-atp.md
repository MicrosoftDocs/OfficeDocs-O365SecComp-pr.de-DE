---
title: Anzeigen von Berichten für Office 365 Advanced Threat Protection
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 02/13/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: e47e838c-d99e-4c0b-b9aa-e66c4fae902f
ms.collection:
- M365-security-compliance
description: Informationen zum Suchen und Verwenden von Berichten für Office 365 Advanced Threat Protection im Security &amp; Compliance Center.
ms.openlocfilehash: c2c1e1134d72bc8c786e0dd783d22adcebeed79b
ms.sourcegitcommit: 1c73c2f83703af0a30a5b0633db00d8e0e6b39b5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/25/2019
ms.locfileid: "30242107"
---
# <a name="view-reports-for-office-365-advanced-threat-protection"></a><span data-ttu-id="16810-103">Anzeigen von Berichten für Office 365 Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="16810-103">View reports for Office 365 Advanced Threat Protection</span></span>

<span data-ttu-id="16810-p101">Wenn Ihre Organisation [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) besitzt und Sie über die [erforderlichen Berechtigungen](#what-permissions-are-needed-to-view-these-reports)verfügen, können Sie im Security &amp; Compliance Center mehrere ATP-Berichte verwenden. (Wechseln Sie zum **Dashboard** **Berichte** \> .)</span><span class="sxs-lookup"><span data-stu-id="16810-p101">If your organization has [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) and you have the [necessary permissions](#what-permissions-are-needed-to-view-these-reports), you can use several ATP reports in the Security &amp; Compliance Center. (Go to **Reports** \> **Dashboard**.)</span></span>
  
![Mit dem &amp; Security Compliance Center-Dashboard können Sie erkennen, wo Advanced Threat Protection funktioniert.](media/6b213d34-adbb-44af-8549-be9a7e2db087.png)
  
<span data-ttu-id="16810-p102">Zu den ATP-Berichten gehören der Bericht über den [Status von Bedrohungsschutz](#threat-protection-status-report), der [Bericht ATP-Dateitypen](#atp-file-types-report)und der Bericht zur Verteilung der ATP-nach [richten](#atp-message-disposition-report). Dieser Artikel beschreibt die ATP-Berichte und enthält Links zu [weiteren Berichten, die Sie anzeigen können](#additional-reports-to-view).</span><span class="sxs-lookup"><span data-stu-id="16810-p102">ATP reports include the [Threat Protection Status report](#threat-protection-status-report), the [ATP File Types report](#atp-file-types-report), and the [ATP Message Disposition report](#atp-message-disposition-report). This article describes the ATP reports and includes links to [additional reports to view](#additional-reports-to-view).</span></span>
  
## <a name="threat-protection-status-report"></a><span data-ttu-id="16810-109">Status Bericht zum BedrohungsSchutz</span><span class="sxs-lookup"><span data-stu-id="16810-109">Threat Protection Status report</span></span>

<span data-ttu-id="16810-p103">Der **Status** Bericht zu Bedrohungen ist eine einzelne Ansicht, in der Informationen zu böswilligen Inhalten und bösartigen e-Mails zusammengeführt werden, die von [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) und [Office 365 ATP](office-365-atp.md)erkannt und blockiert wurden. Der Bericht bietet eine aggregierte Anzahl von eindeutigen e-Mail-Nachrichten mit bösartigen Inhalten (Dateien oder Websiteadressen (URLs)), die vom Antischadsoftware-Modul blockiert wurden, [Zero-Hour Auto Purge (zap)](zero-hour-auto-purge.md)und ATP-Funktionen wie ATP- [sichere Links](atp-safe-links.md), [ATP-Safe ](atp-safe-attachments.md)Und [ATP-Phishing-Funktionen](atp-anti-phishing.md).</span><span class="sxs-lookup"><span data-stu-id="16810-p103">The **Threat Protection Status** report is a single view that brings together information about malicious content and malicious email detected and blocked by [Exchange Online Protection](eop/exchange-online-protection-overview.md) (EOP) and [Office 365 ATP](office-365-atp.md). The report provides an aggregated count of unique email messages with malicious content (files or website addresses (URLs)) blocked by the anti-malware engine, [zero-hour auto purge (ZAP)](zero-hour-auto-purge.md), and ATP features, such as [ATP Safe Links](atp-safe-links.md), [ATP Safe Attachments](atp-safe-attachments.md), and [ATP anti-phishing capabilities](atp-anti-phishing.md).</span></span>

> [!NOTE]
> <span data-ttu-id="16810-p104">Ein Bericht über den BedrohungsSchutz steht Kunden zur Verfügung, die entweder [Office 365 ATP](office-365-atp.md) oder [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EoP) haben; die Informationen, die im Status Bericht zur Gefahrenabwehr für ATP-Kunden angezeigt werden, enthalten jedoch wahrscheinlich unterschiedliche Daten als die EOP-Kunden. Beispielsweise enthält der Status Bericht über Bedrohungen für ATP-Kundeninformationen zu [schädlichen Dateien, die in SharePoint Online, OneDrive oder Microsoft Teams erkannt](atp-for-spo-odb-and-teams.md)wurden. Diese Informationen sind spezifisch für ATP, sodass Kunden, die über EOP, jedoch nicht über ATP verfügen, diese Details nicht in Ihrem Status Bericht über den BedrohungsSchutz sehen.</span><span class="sxs-lookup"><span data-stu-id="16810-p104">A Threat Protection Status report is available to customers who have either [Office 365 ATP](office-365-atp.md) or [Exchange Online Protection](eop/exchange-online-protection-eop.md) (EOP); however, the information that is displayed in the Threat Protection Status report for ATP customers will likely contain different data than what EOP customers might see. For example, the Threat Protection Status report for ATP customers will contain information about [malicious files detected in SharePoint Online, OneDrive, or Microsoft Teams](atp-for-spo-odb-and-teams.md). Such information is specific to ATP, so customers who have EOP but not ATP will not see those details in their Threat Protection Status report.</span></span>
  
<span data-ttu-id="16810-115">Zum Anzeigen des Statusberichts zum Bedrohungsschutz wechseln Sie im [Security &amp; Compliance Center](https://protection.office.com)zu **Status des Threat Protection**- **Dashboards** \> für **Berichte** \> .</span><span class="sxs-lookup"><span data-stu-id="16810-115">To view the Threat Protection Status report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **Threat Protection Status**.</span></span>
  
![Status Bericht zum ATP-BedrohungsSchutz](media/6bdd41eb-62e0-423b-9fd4-d1d5baf0cbd5.png)
  
<span data-ttu-id="16810-117">Wenn Sie einen detaillierten Status für einen Tag erhalten möchten, bewegen Sie den Mauszeiger über das Diagramm.</span><span class="sxs-lookup"><span data-stu-id="16810-117">To get detailed status for a day, hover over the graph.</span></span>
  
![Status Daten für den ATP-BedrohungsSchutz für einen Tag](media/d5c2c6ad-c002-4985-a032-c866e46fdea8.png)
  
<span data-ttu-id="16810-p105">Standardmäßig werden im Bericht über den Status des BedrohungsSchutzes Daten für die letzten sieben Tage angezeigt. Sie können jedoch **Filter** auswählen und den Datums Umfang ändern, um Daten für bis zu 90 Tage anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="16810-p105">By default, the Threat Protection Status report shows data for the past seven days. However, you can choose **Filters** and change the date range to view data for up to 90 days.</span></span> 
  
![Status Filter für ATP-BedrohungsSchutz](media/4f703369-642b-402b-9758-b9c828283410.png)
  
<span data-ttu-id="16810-122">Sie können auch das Menü **Daten anzeigen** , um zu ändern, welche Informationen im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="16810-122">You can also use the **View data by** menu to change what information is displayed in the report.</span></span> 
  
![Anzeigeoptionen für den Status Bericht zum ATP-BedrohungsSchutz](media/4959bf8c-d192-4542-b00b-184e101e7513.png)
  
## <a name="atp-file-types-report"></a><span data-ttu-id="16810-124">Bericht "ATP-Dateitypen"</span><span class="sxs-lookup"><span data-stu-id="16810-124">ATP File Types report</span></span>

<span data-ttu-id="16810-125">Der Bericht **ATP-Dateitypen** zeigt Ihnen den Typ der Dateien an, die von [ATP Safe Attachments](atp-safe-attachments.md)als bösartig erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="16810-125">The **ATP File Types** report shows you the type of files detected as malicious by [ATP Safe Attachments](atp-safe-attachments.md).</span></span>
  
<span data-ttu-id="16810-126">Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu **Berichte** \> **-Dashboard** \> - **ATP-Dateitypen**.</span><span class="sxs-lookup"><span data-stu-id="16810-126">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP File Types**.</span></span>
  
![Bericht "ATP-Dateitypen"](media/6e3f5d33-79aa-4b2d-938c-6ef135d9e54c.png)
  
<span data-ttu-id="16810-128">Wenn Sie den Mauszeiger über einen bestimmten Tag bewegen, sehen Sie die Aufschlüsselung der Arten von bösartigen Dateien, die durch [ATP Safe Attachments](atp-safe-attachments.md) und [Anti-Spam &amp; Anti-Malware Protection in Office 365](anti-spam-and-anti-malware-protection.md)erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="16810-128">When you hover over a particular day, you can see the breakdown of types of malicious files that were detected by [ATP Safe Attachments](atp-safe-attachments.md) and [anti-spam &amp; anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
![ATP-Dateitypen Berichtsdaten für einen Tag](media/10d18428-699a-41d2-a73e-be3a8214ada1.png)
  
## <a name="atp-message-disposition-report"></a><span data-ttu-id="16810-130">Bericht zur ATP-Nachrichten Disposition</span><span class="sxs-lookup"><span data-stu-id="16810-130">ATP Message Disposition report</span></span>

<span data-ttu-id="16810-131">Der Bericht zur Bereitstellung von ATP-Nachrichten zeigt Ihnen die Aktionen an, die für e-Mail- **Nachricht** ausgeführt wurden, die als bösartige Inhalte erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="16810-131">The **ATP Message Disposition** report shows you the actions that were taken for email messages that were detected as having malicious content.</span></span> 
  
<span data-ttu-id="16810-132">Um diesen Bericht anzuzeigen, wechseln Sie [im &amp; Security Compliance Center](https://protection.office.com)zu **Berichte** \> **-Dashboard** \> **ATP Message Disposition**.</span><span class="sxs-lookup"><span data-stu-id="16810-132">To view this report, in the [Security &amp; Compliance Center](https://protection.office.com), go to **Reports** \> **Dashboard** \> **ATP Message Disposition**.</span></span>
  
![Bericht zur ATP-Nachrichten Disposition](media/b0ff65c4-53d3-496d-bafa-8937a5eb69e5.png)
  
<span data-ttu-id="16810-134">Wenn Sie auf einen Balken im Diagramm zeigen, können Sie sehen, welche Aktionen für erkannte e-Mails für diesen Tag ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="16810-134">When you hover over a bar in the chart, you can see what actions were taken for detected email for that day.</span></span>
  
![ATP-Nachrichten Disposition-Berichtsdaten für einen Tag](media/68d2beb8-4b30-48c4-8ba6-5e8ab88ae456.png)
  
## <a name="additional-reports-to-view"></a><span data-ttu-id="16810-136">Zusätzliche Berichte zum Anzeigen</span><span class="sxs-lookup"><span data-stu-id="16810-136">Additional reports to view</span></span>

<span data-ttu-id="16810-137">Zusätzlich zu den in diesem Artikel beschriebenen ATP-Berichten stehen mehrere weitere Berichte zur Verfügung, wie in der folgenden Tabelle beschrieben:</span><span class="sxs-lookup"><span data-stu-id="16810-137">In addition to the ATP reports described in this article, several other reports are available, as described in the following table:</span></span>

|<span data-ttu-id="16810-138">Berichtstyp</span><span class="sxs-lookup"><span data-stu-id="16810-138">Report type</span></span>  |<span data-ttu-id="16810-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="16810-139">Learn more</span></span>  |
|---------|---------|
|<span data-ttu-id="16810-140">**E-Mail-Sicherheitsberichte**, wie beispielsweise ein Bericht über Top-Absender und-Empfänger, ein spoof-e-Mail-Bericht und ein Spam Erkennungs Bericht.</span><span class="sxs-lookup"><span data-stu-id="16810-140">**Email security reports**, such as a Top Senders and Recipients report, a Spoof Mail report, and a Spam Detections report.</span></span> | [<span data-ttu-id="16810-141">Anzeigen von e-Mail-Sicherheits &amp; Berichten im Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="16810-141">View email security reports in the Security &amp; Compliance Center</span></span>](view-email-security-reports.md)        |
|<span data-ttu-id="16810-142">**Explorer** (auch als Bedrohungs-Explorer bezeichnet, ist dies in [Office 365 Threat Intelligence](office-365-ti.md)enthalten)</span><span class="sxs-lookup"><span data-stu-id="16810-142">**Explorer** (also referred to as Threat Explorer, this is included in [Office 365 Threat Intelligence](office-365-ti.md))</span></span>     | [<span data-ttu-id="16810-143">Verwenden des Explorers im Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="16810-143">Use Explorer in the Security &amp; Compliance Center</span></span>](use-explorer-in-security-and-compliance.md)        |
|<span data-ttu-id="16810-p106">**EoP und ATP-Ergebnisse** (Hierbei handelt es sich um einen benutzerdefinierten Bericht, den Sie mithilfe von PowerShell generieren). Dieser Bericht enthält Informationen wie Domäne, Datum, Ereignistyp, Richtung, Aktion und Nachrichtenanzahl.</span><span class="sxs-lookup"><span data-stu-id="16810-p106">**EOP and ATP results** (This is a custom report you generate by using PowerShell). This report contains information, such as Domain, Date, Event Type, Direction, Action, and Message Count.</span></span>  | [<span data-ttu-id="16810-146">Get-MailTrafficATPReport-Cmdlet-Referenz</span><span class="sxs-lookup"><span data-stu-id="16810-146">Get-MailTrafficATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-mailtrafficatpreport?view=exchange-ps) |
|<span data-ttu-id="16810-p107">**EoP und ATP-Ermittlungen** (Hierbei handelt es sich um einen benutzerdefinierten Bericht, den Sie mithilfe von PowerShell generieren). Dieser Bericht enthält Details zu schädlichen Dateien oder URLs, Phishing-versuchen, Identitätswechsel und anderen potenziellen Bedrohungen in e-Mails oder Dateien.</span><span class="sxs-lookup"><span data-stu-id="16810-p107">**EOP and ATP detections** (This is a custom report you generate by using PowerShell). This report contains details about malicious files or URLs, phishing attempts, impersonation, and other potential threats in email or files.</span></span>   | [<span data-ttu-id="16810-149">Get-MailDetailATPReport-Cmdlet-Referenz</span><span class="sxs-lookup"><span data-stu-id="16810-149">Get-MailDetailATPReport cmdlet reference</span></span>](https://docs.microsoft.com/powershell/module/exchange/advanced-threat-protection/get-maildetailatpreport?view=exchange-ps)        |

  
## <a name="what-permissions-are-needed-to-view-the-atp-reports"></a><span data-ttu-id="16810-150">Welche Berechtigungen sind erforderlich, um die ATP-Berichte anzuzeigen?</span><span class="sxs-lookup"><span data-stu-id="16810-150">What permissions are needed to view the ATP reports?</span></span>

<span data-ttu-id="16810-151">Um die in diesem Artikel beschriebenen Berichte anzuzeigen und zu verwenden, **müssen Sie eine entsprechende Rolle sowohl für das Security &amp; Compliance Center als auch für das Exchange Admin Center zugewiesen haben**.</span><span class="sxs-lookup"><span data-stu-id="16810-151">In order to view and use the reports described in this article, **you must have an appropriate role assigned for both the Security &amp; Compliance Center and the Exchange Admin Center**.</span></span>

- <span data-ttu-id="16810-152">Für das Security &amp; Compliance Center muss eine der folgenden Rollen zugewiesen sein:</span><span class="sxs-lookup"><span data-stu-id="16810-152">For the Security &amp; Compliance Center, you must have one of the following roles assigned:</span></span>
    - <span data-ttu-id="16810-153">Organisationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="16810-153">Organization Management</span></span>
    - <span data-ttu-id="16810-154">Sicherheits Administrator (kann im Azure Active Directory Admin Center[https://aad.portal.azure.com](https://aad.portal.azure.com)zugewiesen werden)</span><span class="sxs-lookup"><span data-stu-id="16810-154">Security Administrator (this can be assigned in the Azure Active Directory admin center ([https://aad.portal.azure.com](https://aad.portal.azure.com)))</span></span>
    - <span data-ttu-id="16810-155">Sicherheits Leser</span><span class="sxs-lookup"><span data-stu-id="16810-155">Security Reader</span></span>

- <span data-ttu-id="16810-156">Für Exchange Online müssen Sie über eine der folgenden Rollen verfügen, die entweder in der Exchange-Verwaltungskonsole[https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)() oder mit PowerShell-Cmdlets zugewiesen sind (siehe [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span><span class="sxs-lookup"><span data-stu-id="16810-156">For Exchange Online, you must have one of the following roles assigned in either the Exchange admin center ([https://outlook.office365.com/ecp](https://outlook.office365.com/ecp)) or with PowerShell cmdlets (See [Exchange Online PowerShell](https://docs.microsoft.com/powershell/exchange/exchange-online/exchange-online-powershell?view=exchange-ps)):</span></span>
    - <span data-ttu-id="16810-157">Organisationsverwaltung</span><span class="sxs-lookup"><span data-stu-id="16810-157">Organization Management</span></span>
    - <span data-ttu-id="16810-158">Organisationsverwaltung mit Leserechten</span><span class="sxs-lookup"><span data-stu-id="16810-158">View-only Organization Management</span></span>
    - <span data-ttu-id="16810-159">Rolle „Empfänger mit Leserechten“</span><span class="sxs-lookup"><span data-stu-id="16810-159">View-Only Recipients role</span></span>
    - <span data-ttu-id="16810-160">Verwaltung der Richtlinientreue</span><span class="sxs-lookup"><span data-stu-id="16810-160">Compliance Management</span></span>

<span data-ttu-id="16810-161">Weitere Informationen finden Sie in den folgenden Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="16810-161">To learn more, see the following resources:</span></span>

- [<span data-ttu-id="16810-162">Berechtigungen im Office 365 Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="16810-162">Permissions in the Office 365 Security &amp; Compliance Center</span></span>](permissions-in-the-security-and-compliance-center.md)

- [<span data-ttu-id="16810-163">Featureberechtigungen in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="16810-163">Feature permissions in Exchange Online</span></span>](https://docs.microsoft.com/exchange/permissions-exo/feature-permissions)
   
## <a name="what-if-the-reports-arent-showing-data"></a><span data-ttu-id="16810-164">Was geschieht, wenn die Berichte keine Daten anzeigen?</span><span class="sxs-lookup"><span data-stu-id="16810-164">What if the reports aren't showing data?</span></span>

<span data-ttu-id="16810-p108">Wenn in ihren ATP-Berichten keine Daten angezeigt werden, überprüfen Sie, ob Ihre Richtlinien ordnungsgemäß eingerichtet sind. Ihre Organisation muss über [ATP Safe Links Policies](set-up-atp-safe-links-policies.md) und [ATP Safe Attachments-Richtlinien](set-up-atp-safe-attachments-policies.md) verfügen, die für den ATP-Schutz definiert sind. Weitere Informationen finden Sie unter [Anti-Spam and Anti-Malware Protection in Office 365](anti-spam-and-anti-malware-protection.md).</span><span class="sxs-lookup"><span data-stu-id="16810-p108">If you are not seeing data in your ATP reports, double-check that your policies are set up correctly. Your organization must have [ATP Safe Links policies](set-up-atp-safe-links-policies.md) and [ATP Safe Attachments policies](set-up-atp-safe-attachments-policies.md) defined in order for ATP protection to be in place. Also see [Anti-spam and anti-malware protection in Office 365](anti-spam-and-anti-malware-protection.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="16810-168">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="16810-168">Related topics</span></span>

[<span data-ttu-id="16810-169">Berichte und Einblicke im Office 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="16810-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="16810-170">Erstellen eines Zeitplans für einen Bericht im &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="16810-170">Create a schedule for a report in the Security &amp; Compliance Center</span></span>](create-a-schedule-for-a-report.md)
  
[<span data-ttu-id="16810-171">Einrichten und Herunterladen eines benutzerdefinierten Berichts im Security &amp; Compliance Center</span><span class="sxs-lookup"><span data-stu-id="16810-171">Set up and download a custom report in the Security &amp; Compliance Center</span></span>](set-up-and-download-a-custom-report.md)
  

