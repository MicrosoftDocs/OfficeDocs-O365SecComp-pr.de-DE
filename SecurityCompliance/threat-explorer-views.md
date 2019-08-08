---
title: Ansichten im Threat Explorer und Echt Zeit Erkennungen
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 08/07/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid: ''
ms.collection:
- M365-security-compliance
description: Erfahren Sie mehr über die verschiedenen Arten von Ansichten, die in Threat Explorer und in Echtzeit erkannt werden können.
ms.openlocfilehash: 82476f9af3b703904fff40c8347f2848cf919dfc
ms.sourcegitcommit: 7a0cb7e1da39fc485fc29e7325b843d16b9808af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/07/2019
ms.locfileid: "36230389"
---
# <a name="views-in-threat-explorer-and-real-time-detections"></a><span data-ttu-id="3d109-103">Ansichten im Threat Explorer und Echt Zeit Erkennungen</span><span class="sxs-lookup"><span data-stu-id="3d109-103">Views in Threat Explorer and real-time detections</span></span>

![Sicherheitsrisiken-Explorer](media/ThreatExplorerFirstOpened.png)

<span data-ttu-id="3d109-105">[Bedrohungs-Explorer](use-explorer-in-security-and-compliance.md) (und der Bericht über Echt Zeit Erkennungen) ist ein leistungsfähiges, near-Echt Zeit Tool zur Untersuchung und Reaktion von Sicherheitsteams auf Bedrohungen &amp; im Security Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="3d109-105">[Threat Explorer](use-explorer-in-security-and-compliance.md) (and the real-time detections report) is a powerful, near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span> <span data-ttu-id="3d109-106">Explorer (und der Bericht über Echt Zeit Erkennungen) zeigt Informationen zu mutmaßlicher Schadsoftware und Phishing in e-Mails und Dateien in Office 365 sowie andere Sicherheitsrisiken und Risiken für Ihre Organisation an.</span><span class="sxs-lookup"><span data-stu-id="3d109-106">Explorer (and the real-time detections report) displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span> 

- <span data-ttu-id="3d109-107">Wenn Sie [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) Plan 2 haben, haben Sie den Explorer.</span><span class="sxs-lookup"><span data-stu-id="3d109-107">If you have [Office 365 Advanced Threat Protection](office-365-atp.md) (ATP) Plan 2, then you have Explorer.</span></span>
- <span data-ttu-id="3d109-108">Wenn Sie Office 365 ATP-Plan 1 haben, haben Sie Echt Zeit Erkennungen.</span><span class="sxs-lookup"><span data-stu-id="3d109-108">If you have Office 365 ATP Plan 1, then you have real-time detections.</span></span>

<span data-ttu-id="3d109-109">Wenn Sie Explorer zum ersten Mal öffnen (oder den Bericht über Echt Zeit Erkennungen), werden in der Standardansicht e-Mail-Malwareerkennungen für die letzten 7 Tage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d109-109">When you first open Explorer (or the real-time detections report), the default view shows email malware detections for the past 7 days.</span></span> <span data-ttu-id="3d109-110">In diesem Bericht können auch ATP-Erkennungen angezeigt werden, beispielsweise bösartige URLs, die von [sicheren Links](atp-safe-links.md)erkannt wurden, sowie bösartige Dateien, die durch [sichere Anlagen](atp-safe-attachments.md)erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="3d109-110">This report can also show ATP detections, such as malicious URLs detected by [Safe Links](atp-safe-links.md), and malicious files detected by [Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="3d109-111">Dieser Bericht kann geändert werden, um Daten für die letzten 30 Tage anzuzeigen (es sei denn, Sie verwenden ein Testabonnement).</span><span class="sxs-lookup"><span data-stu-id="3d109-111">This report can be modified to show data for the past 30 days (unless you are using a trial subscription).</span></span> <span data-ttu-id="3d109-112">Testabonnements enthalten nur Daten für die letzten sieben Tage.</span><span class="sxs-lookup"><span data-stu-id="3d109-112">Trial subscriptions will include data for the past seven days only.</span></span>

<span data-ttu-id="3d109-113">Verwenden Sie das Menü **Ansicht** , um zu ändern, welche Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3d109-113">Use the **View** menu to change what information is displayed.</span></span> <span data-ttu-id="3d109-114">Mithilfe von QuickInfos können Sie bestimmen, welche Ansicht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3d109-114">Tooltips help you determine which view to use.</span></span>
  
![Ansicht im Menü "Bedrohungs-Explorer"](media/ThreatExplorerViewMenu.png)

<span data-ttu-id="3d109-116">Nachdem Sie eine Ansicht ausgewählt haben, können Sie Filter anwenden und Abfragen einrichten, um eine weitere Analyse durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="3d109-116">Once you have selected a view, you can apply filters and set up queries to conduct further analysis.</span></span> <span data-ttu-id="3d109-117">Die folgenden Abschnitte bieten eine kurze Übersicht über die verschiedenen Ansichten, die in Explorer verfügbar sind (oder Echt Zeit Erkennungen).</span><span class="sxs-lookup"><span data-stu-id="3d109-117">The following sections provide a brief overview of the various views available in Explorer (or real-time detections).</span></span>  

## <a name="email--malware"></a><span data-ttu-id="3d109-118">E-Mail-#a0 Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="3d109-118">Email > Malware</span></span>

<span data-ttu-id="3d109-119">Wenn Sie diesen Bericht anzeigen möchten, wählen Sie im Explorer (oder Echtzeiterkennung) die Option**e-Mail-** > **Schadsoftware** **anzeigen** > aus.</span><span class="sxs-lookup"><span data-stu-id="3d109-119">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Malware**.</span></span> <span data-ttu-id="3d109-120">In dieser Ansicht werden Informationen zu e-Mail-Nachrichten angezeigt, die als mit Schadsoftware gekennzeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="3d109-120">This view shows information about email messages that were identified as containing malware.</span></span>  

![Anzeigen von Daten zu e-Mails, die als Schadsoftware identifiziert wurden](media/ExplorerEmailMalwareMenu.png) 

<span data-ttu-id="3d109-122">Klicken Sie auf **Absender** , um die Liste der Anzeigeoptionen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3d109-122">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="3d109-123">Verwenden Sie diese Liste, um Daten nach Absender, Empfänger, Absenderdomäne, Betreff, Erkennungstechnologie, Schutzstatus und vielem mehr anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d109-123">Use this list to view data by sender, recipients, sender domain, subject, detection technology, protection status, and more.</span></span> 

<span data-ttu-id="3d109-124">Um beispielsweise zu sehen, welche Aktionen bei erkannten e-Mail-Nachrichten durchgeführt wurden, wählen Sie in der Liste **Schutzstatus** aus.</span><span class="sxs-lookup"><span data-stu-id="3d109-124">For example, to see what actions were taken on detected email messages, choose **Protection status** in the list.</span></span> <span data-ttu-id="3d109-125">Wählen Sie eine Option aus, und klicken Sie dann auf die Schaltfläche Aktualisieren, um diesen Filter auf Ihren Bericht anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="3d109-125">Select an option, and then click the Refresh button to apply that filter to your report.</span></span>

![Bedrohungsschutz-Status Optionen für Threat Explorer](media/ThreatExplorerProtectionStatusOptions.png)

<span data-ttu-id="3d109-127">Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="3d109-127">Below the chart, view more details about specific messages.</span></span> <span data-ttu-id="3d109-128">Wenn Sie ein Element in der Liste auswählen, wird ein Ausklappbereich geöffnet, in dem Sie weitere Informationen zum ausgewählten Element erhalten.</span><span class="sxs-lookup"><span data-stu-id="3d109-128">When you select an item in the list, a fly-out pane opens, where you can learn more about the item you selected.</span></span> 

![Threat Explorer mit geöffnetem Flyout](media/ThreatExplorerMalwareItemSelectedFlyout.png)

## <a name="email--phish"></a><span data-ttu-id="3d109-130">E-Mail #a0 Phishing</span><span class="sxs-lookup"><span data-stu-id="3d109-130">Email > Phish</span></span>

<span data-ttu-id="3d109-131">Wenn Sie diesen Bericht anzeigen möchten, wählen Sie im Explorer (oder Echtzeiterkennung) die Option**e-Mail-** > **Phishing** **anzeigen** > aus.</span><span class="sxs-lookup"><span data-stu-id="3d109-131">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Phish**.</span></span> <span data-ttu-id="3d109-132">Diese Ansicht zeigt e-Mail-Nachrichten, die als Phishing-Versuche identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="3d109-132">This view shows email messages identified as phishing attempts.</span></span>  

![Anzeigen von Daten zu e-Mails, die als Phishing-Versuche identifiziert wurden](media/ThreatExplorerEmailPhish.png) 

<span data-ttu-id="3d109-134">Klicken Sie auf **Absender** , um die Liste der Anzeigeoptionen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3d109-134">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="3d109-135">Verwenden Sie diese Liste, um Daten nach Absender, Empfänger, Absenderdomäne, Absender-IP, URL-Domäne, Klick Urteil und vieles mehr anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d109-135">Use this list to view data by sender, recipients, sender domain, sender IP, URL domain, click verdict, and more.</span></span> 

<span data-ttu-id="3d109-136">Um beispielsweise zu sehen, welche Aktionen durchgeführt wurden, als Personen auf URLs geklickt haben, die als Phishing-Versuche identifiziert wurden, wählen Sie in der Liste **auf Urteil klicken** , wählen Sie eine oder mehrere Optionen aus, und klicken Sie dann auf die Schaltfläche Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3d109-136">For example, to see what actions were taken when people clicked on URLs that were identified as phishing attempts, choose **Click verdict** in the list, select one or more options, and then click the Refresh button.</span></span>

![Klicken Sie auf Urteils Optionen für den Phish-Bericht](media/ThreatExplorerEmailPhishClickVerdictOptions.png)

<span data-ttu-id="3d109-138">Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Nachrichten, URL-Klicks, URLs und e-Mail-Ursprung an.</span><span class="sxs-lookup"><span data-stu-id="3d109-138">Below the chart, view more details about specific messages, URL clicks, URLs, and email origin.</span></span> 

![Als Phishing erkannte URLs in e-Mail-Nachrichten](media/ThreatExplorerEmailPhishURLs.png)

<span data-ttu-id="3d109-140">Wenn Sie ein Element in der Liste auswählen, beispielsweise eine erkannte URL, wird ein Ausklappbereich geöffnet, in dem Sie weitere Informationen zum ausgewählten Element erhalten.</span><span class="sxs-lookup"><span data-stu-id="3d109-140">When you select an item in the list, such as a URL that was detected, a fly-out pane opens, where you can learn more about the item you selected.</span></span> 

![Details zu einer erkannten URL](media/ThreatExplorerEmailPhishURLDetails.png)

## <a name="email--submissions"></a><span data-ttu-id="3d109-142">E-Mail #a0 Übermittlungen</span><span class="sxs-lookup"><span data-stu-id="3d109-142">Email > Submissions</span></span>

<span data-ttu-id="3d109-143">Um diesen Bericht anzuzeigen, wählen Sie im Explorer (oder Echtzeiterkennung) die Option \*\*\*\* > **e-Mail-** > **Übermittlungen**anzeigen aus.</span><span class="sxs-lookup"><span data-stu-id="3d109-143">To view this report, in Explorer (or real-time detections), choose **View** > **Email** > **Submissions**.</span></span> <span data-ttu-id="3d109-144">In dieser Ansicht werden e-Mails angezeigt, die Benutzer als Junk-e-Mail, nicht als Junk oder als Phishing-e-Mails gemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="3d109-144">This view shows email that users have reported as junk, not junk, or phishing email.</span></span> 

![Von Benutzern gemeldete e-Mail-Nachrichten](media/ThreatExplorerEmailUserReportedViewOptions.png) 

<span data-ttu-id="3d109-146">Klicken Sie auf **Absender** , um die Liste der Anzeigeoptionen zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3d109-146">Click **Sender** to open your list of viewing options.</span></span> <span data-ttu-id="3d109-147">Verwenden Sie diese Liste, um Informationen nach Absender, Empfänger, Berichtstyp anzuzeigen (die Bestimmung des Benutzers, dass es sich bei der e-Mail um Junk-e-Mails handelte, nicht um Junk-oder Phishing-Zwecke) und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="3d109-147">Use this list to view information by sender, recipients, report type (the user's determination that the email was junk, not junk, or phish), and more.</span></span> 

<span data-ttu-id="3d109-148">Wenn Sie beispielsweise Informationen zu e-Mail-Nachrichten anzeigen möchten, die als Phishing-Versuche gemeldet wurden, klicken Sie auf **Absender** > **Berichtstyp**, wählen Sie **Phishing**aus, und klicken Sie dann auf die Schaltfläche Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3d109-148">For example, to view information about email messages that were reported as phishing attempts, click **Sender** > **Report type**, select **Phish**, and then click the Refresh button.</span></span>

![Für den Berichtstyp Filter ausgewählter Phishing-Typ](media/ThreatExplorerEmailUserReportedPhishSelected.png)

<span data-ttu-id="3d109-150">Zeigen Sie unter dem Diagramm weitere Details zu bestimmten e-Mail-Nachrichten an, beispielsweise Betreffzeile, die IP-Adresse des Absenders, den Benutzer, der die Nachricht als Junk-e-Mail, nicht Junk oder Phishing gemeldet hat, und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="3d109-150">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

![Nachrichten, die als Phishing-Versuche gemeldet wurden](media/ThreatExplorerEmailPhishUserReportedPhishDetails.png)

<span data-ttu-id="3d109-152">Wählen Sie ein Element in der Liste aus, um weitere Details anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d109-152">Select an item in the list to view additional details.</span></span>

## <a name="email--all-email"></a><span data-ttu-id="3d109-153">E-Mail #a0 alle e-Mails</span><span class="sxs-lookup"><span data-stu-id="3d109-153">Email > All email</span></span>

<span data-ttu-id="3d109-154">Um diesen Bericht anzuzeigen, wählen Sie im Explorer die Option**e-Mail** > **alle e-Mails** **anzeigen** > aus.</span><span class="sxs-lookup"><span data-stu-id="3d109-154">To view this report, in Explorer, choose **View** > **Email** > **All mail**.</span></span> <span data-ttu-id="3d109-155">Diese Ansichten zeigen eine Gesamtansicht der e-Mail-Aktivität an, einschließlich e-Mails, die aufgrund von Phishing oder Schadsoftware als bösartig eingestuft wurden, sowie alle nicht-böswilligen e-Mails (normale e-Mail, Spam und Massen-e-Mails).</span><span class="sxs-lookup"><span data-stu-id="3d109-155">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="3d109-156">Wenn Sie eine Fehlermeldung erhalten, die zu **viele anzuzeigende Daten**liest, fügen Sie einen Filter hinzu, und verringern Sie ggf. den von Ihnen angezeigten Datumsbereich.</span><span class="sxs-lookup"><span data-stu-id="3d109-156">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="3d109-157">Wenn Sie einen Filter anwenden möchten, wählen Sie **Absender**aus, wählen Sie ein Element in der Liste aus, und klicken Sie dann auf die Schaltfläche Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="3d109-157">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="3d109-158">In unserem Beispiel haben wir die **Erkennungstechnologie** als Filter verwendet (es stehen verschiedene Optionen zur Verfügung).</span><span class="sxs-lookup"><span data-stu-id="3d109-158">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="3d109-159">Anzeigen von Informationen nach Absender, Domäne des Absenders, Empfänger, Betreff, Anlagendateiname, Malwarefamilie, Schutzstatus (Aktionen, die von den Bedrohungen geschützt sind, und Richtlinien in Office 365), Erkennungstechnologie (wie die Schadsoftware erkannt wurde) und Weitere.</span><span class="sxs-lookup"><span data-stu-id="3d109-159">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Anzeigen von Daten zu erkannten e-Mails anhand von Erkennungstechnologien](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="3d109-161">Zeigen Sie unter dem Diagramm weitere Details zu bestimmten e-Mail-Nachrichten an, beispielsweise Betreff, Empfänger, Absender, Status usw.</span><span class="sxs-lookup"><span data-stu-id="3d109-161">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="3d109-162">Inhalte #a0 Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="3d109-162">Content > Malware</span></span>

<span data-ttu-id="3d109-163">Wenn Sie diesen Bericht anzeigen möchten, wählen Sie im Explorer (oder Echtzeiterkennung) die Option**Inhalts** > **Malware** **anzeigen** > aus.</span><span class="sxs-lookup"><span data-stu-id="3d109-163">To view this report, in Explorer (or real-time detections), choose **View** > **Content** > **Malware**.</span></span> <span data-ttu-id="3d109-164">In dieser Ansicht werden Dateien angezeigt, die von [Office 365 Advanced Threat Protection in SharePoint Online, OneDrive für Unternehmen und Microsoft Teams](atp-for-spo-odb-and-teams.md)als bösartig identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="3d109-164">This view shows files that were identified as malicious by [Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business, and Microsoft Teams](atp-for-spo-odb-and-teams.md).</span></span>

<span data-ttu-id="3d109-165">Anzeigen von Informationen nach Malwarefamilie, Erkennungstechnologie (wie die Schadsoftware erkannt wurde) und Arbeitsauslastung (OneDrive, SharePoint oder Teams).</span><span class="sxs-lookup"><span data-stu-id="3d109-165">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Anzeigen von Daten zu erkannter Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="3d109-167">Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Dateien an, beispielsweise Anlagendateiname, Arbeitsauslastung, Dateigröße, wer die Datei zuletzt geändert hat und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="3d109-167">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="click-to-filter-capabilities"></a><span data-ttu-id="3d109-168">Click-to-Filter-Funktionen</span><span class="sxs-lookup"><span data-stu-id="3d109-168">Click-to-filter capabilities</span></span>

<span data-ttu-id="3d109-169">Mit Explorer (und Echtzeiterkennung) können Sie einen Filter in einem Klick anwenden.</span><span class="sxs-lookup"><span data-stu-id="3d109-169">With Explorer (and real-time detections), you can apply a filter in a click.</span></span> <span data-ttu-id="3d109-170">Klicken Sie auf ein Element in der Legende, und dieses Element wird zum Filter für den Bericht.</span><span class="sxs-lookup"><span data-stu-id="3d109-170">Click an item in the legend, and that item becomes a filter for the report.</span></span> <span data-ttu-id="3d109-171">Nehmen wir beispielsweise an, dass wir uns die Malware-Ansicht im Explorer ansehen:</span><span class="sxs-lookup"><span data-stu-id="3d109-171">For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="3d109-173">Wenn Sie in diesem Diagramm auf **ATP-Detonation** klicken, wird eine Ansicht wie die folgende angezeigt:</span><span class="sxs-lookup"><span data-stu-id="3d109-173">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorer gefiltert, um nur ATP-detonations Ergebnisse anzuzeigen](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="3d109-175">In dieser Ansicht betrachten wir nun Daten für Dateien, die von [Office 365 ATP-Sicherheitsanlagen](atp-safe-attachments.md)gezündet wurden.</span><span class="sxs-lookup"><span data-stu-id="3d109-175">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="3d109-176">Unter dem Diagramm können Details zu bestimmten e-Mail-Nachrichten mit Anlagen angezeigt werden, die durch ATP-sichere Anlagen erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="3d109-176">Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Spezifische Details zu e-Mail-Nachrichten mit erkannten Anlagen](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="3d109-178">Wenn Sie ein oder mehrere Elemente auswählen, wird das Menü **Aktionen** aktiviert, das mehrere Auswahlmöglichkeiten für die ausgewählten Elemente bietet.</span><span class="sxs-lookup"><span data-stu-id="3d109-178">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![Durch die Auswahl eines Elements wird das Menü Aktionen aktiviert.](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="3d109-180">Die Möglichkeit, mit einem Klick zu filtern und zu bestimmten Details zu navigieren, kann Ihnen viel Zeit bei der Untersuchung von Bedrohungen sparen.</span><span class="sxs-lookup"><span data-stu-id="3d109-180">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>

## <a name="queries-and-filters"></a><span data-ttu-id="3d109-181">Abfragen und Filter</span><span class="sxs-lookup"><span data-stu-id="3d109-181">Queries and filters</span></span>

<span data-ttu-id="3d109-182">Explorer (sowie der Bericht über Echt Zeit Erkennungen) verfügt über mehrere leistungsstarke Filter und Abfragefunktionen, mit denen Sie Details eingehen können, beispielsweise Top-Zielbenutzer, Top-Malware Familien, Erkennungstechnologien und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="3d109-182">Explorer (as well as the real-time detections report) has several powerful filters and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="3d109-183">Jede Art von Bericht bietet eine Vielzahl von Möglichkeiten zum Anzeigen und Durchsuchen von Daten.</span><span class="sxs-lookup"><span data-stu-id="3d109-183">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d109-184">Verwenden Sie in der Abfrage Leiste für Explorer (oder Echtzeiterkennung) keine Platzhalterzeichen, beispielsweise ein Sternchen oder ein Fragezeichen.</span><span class="sxs-lookup"><span data-stu-id="3d109-184">Do not use wildcard characters, such as an asterisk or a question mark, in the query bar for Explorer (or real-time detections).</span></span> <span data-ttu-id="3d109-185">Wenn Sie im **Feld Betreff** nach e-Mail-Nachrichten suchen, führt der Explorer (oder Echt Zeit Erkennungsvorgang) partielle Übereinstimmungen und Ergebnis Ergebnisse aus, die einer Platzhaltersuche ähneln.</span><span class="sxs-lookup"><span data-stu-id="3d109-185">When you search on the **Subject field** for email messages, Explorer (or real-time detections) will perform partial matching and yield results similar to a wildcard search.</span></span>
