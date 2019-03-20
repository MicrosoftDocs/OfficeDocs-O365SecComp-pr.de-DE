---
title: Verwenden des Bedrohungs-Explorers &amp; im Security Compliance Center
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/10/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 82ac9922-939c-41be-9c8a-7c75b0a4e27d
ms.collection:
- M365-security-compliance
description: Informationen zu Explorer (auch als Bedrohungs-Explorer bezeichnet) &amp; im Security Compliance Center.
ms.openlocfilehash: 0c86792d8ed84b43b28bde31004dc95d2fa2b547
ms.sourcegitcommit: 0f93b37c39d807dec91f118aa671a3430c47a9ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2019
ms.locfileid: "30693614"
---
# <a name="use-threat-explorer-in-the-security-amp-compliance-center"></a><span data-ttu-id="fc5f6-103">Verwenden des Bedrohungs-Explorers &amp; im Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="fc5f6-103">Use Threat Explorer in the Security &amp; Compliance Center</span></span>

<span data-ttu-id="fc5f6-104">Wenn Ihre Organisation [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md)enthält und Sie über die erforderlichen Berechtigungen verfügen, können Sie Threat Explorer verwenden, um Bedrohungen zu identifizieren und zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-104">If your organization has [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md), and you have the necessary permissions, you can use Threat Explorer to identify and analyze threats.</span></span> <span data-ttu-id="fc5f6-105">Sie können beispielsweise infizierte e-Mails identifizieren und löschen, die übermittelt wurden, oder Malware, die von den Office 365-Sicherheitsfeatures abgefangen wurde.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-105">For example, you can identify and delete malicious email that was delivered, or see malware that was caught by Office 365 security features.</span></span> <span data-ttu-id="fc5f6-106">Threat Explorer (auch als Explorer bezeichnet) ist ein leistungsstarkes Near-Real-Time-Tool, mit dessen Hilfe Sicherheitsteams untersuchen und auf Bedrohungen &amp; im Security Compliance Center reagieren können.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-106">Threat Explorer (also referred to as Explorer) is a powerful near real-time tool to help Security Operations teams investigate and respond to threats in the Security &amp; Compliance Center.</span></span>
  
![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="fc5f6-108">Um Explorer zu verwenden, wechseln Sie &amp; im Security Compliance Center zu **Threat Management** \> **Explorer**.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-108">To use Explorer, in the Security &amp; Compliance Center, go to **Threat management** \> **Explorer**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc5f6-109">Office 365 Threat Intelligence ist jetzt Office 365 Advanced Threat Protection Plan 2, zusammen mit zusätzlichen Funktionen zum Schutz vor Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-109">Office 365 Threat Intelligence is now Office 365 Advanced Threat Protection Plan 2, along with additional threat protection capabilities.</span></span> <span data-ttu-id="fc5f6-110">Weitere Informationen finden Sie unter [office 365 Advanced Threat Protection-Pläne und Preise](https://products.office.com/exchange/advance-threat-protection) und die [Office 365 Advanced Threat Protection-Dienstbeschreibung](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span><span class="sxs-lookup"><span data-stu-id="fc5f6-110">To learn more, see [Office 365 Advanced Threat Protection plans and pricing](https://products.office.com/exchange/advance-threat-protection) and the [Office 365 Advanced Threat Protection Service Description](https://docs.microsoft.com/office365/servicedescriptions/office-365-advanced-threat-protection-service-description).</span></span>
      
## <a name="explorer-overview"></a><span data-ttu-id="fc5f6-111">Übersicht über den Explorer</span><span class="sxs-lookup"><span data-stu-id="fc5f6-111">Explorer overview</span></span>

<span data-ttu-id="fc5f6-112">Der Explorer zeigt Informationen zu mutmaßlicher Schadsoftware und Phishing in e-Mails und Dateien in Office 365 sowie andere Sicherheitsbedrohungen und-Risiken für Ihre Organisation an.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-112">Explorer displays information about suspected malware and phish in email and files in Office 365, as well as other security threats and risks to your organization.</span></span> <span data-ttu-id="fc5f6-113">Wenn Sie Explorer zuerst öffnen, werden in der Standardansicht e-Mail-Malware-Entdeckungen für die letzten 7 Tage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-113">When you first open Explorer, the default view shows email malware detections for the past 7 days.</span></span> <span data-ttu-id="fc5f6-114">Der Explorer kann auch Sicherheitsschutz Features in Office 365, einschließlich [sicherer Links](atp-safe-links.md) und [sicherer Anlagen](atp-safe-attachments.md) , anzeigen und so geändert werden, dass Daten für die letzten 30 Tage angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-114">Explorer can also show security protection features in Office 365, including [Safe Links](atp-safe-links.md) and [Safe Attachments](atp-safe-attachments.md) and can be modified to show data for the past 30 days.</span></span> <span data-ttu-id="fc5f6-115">Wenn Sie über ein Test-Abonnement für Office 365 Advanced Threat Protection Plan 2 oder Office 365 E5 verfügen, werden nur Erkennungs-und e-Mail-Daten für die letzten 7 Tage angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-115">If you have a trial subcription for Office 365 Advanced Threat Protection Plan 2 or Office 365 E5, you will only see detections and email data for the past 7 days.</span></span>
  
![Explorer zeigt Informationen zu Top-Schadsoftware und zu den Ziel Benutzern](media/8e8c1582-d6f4-4521-8591-686a1cb01f7e.png)
  
<span data-ttu-id="fc5f6-117">Verwenden Sie das Menü Ansicht, um zu ändern, welche Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-117">Use the View menu to change what information is displayed.</span></span>
  
![Das Menü "Ansicht" für Explorer](media/2bb34f58-555f-4967-ba55-740334ef1f8e.png)
  
<span data-ttu-id="fc5f6-119">Der Explorer verfügt über mehrere Filterungs-und Abfragefunktionen, mit denen Sie Details wie die wichtigsten Zielbenutzer, die wichtigsten Malware Familien, die Erkennungstechnologie und vieles mehr eingehen können.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-119">Explorer has several filtering and querying capabilities that enable you to drill into details, such as top targeted users, top malware families, detection technology and more.</span></span> <span data-ttu-id="fc5f6-120">Jede Art von Bericht bietet eine Vielzahl von Möglichkeiten zum Anzeigen und Durchsuchen von Daten.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-120">Each kind of report offers a variety of ways to view and explore data.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc5f6-121">Verwenden Sie keine Platzhalterzeichen wie ein Sternchen (\*) oder ein Fragezeichen (?) mit Explorer.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-121">Do not use wildcard characters, such as an asterisk (\*) or a question mark (?), with Explorer.</span></span> <span data-ttu-id="fc5f6-122">Wenn Sie im Feld Betreff für e-Mail-Nachrichten suchen, führt der Explorer eine partielle Übereinstimmung aus und liefert Ergebnisse, die der Platzhaltersuche ähneln.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-122">When you search on the Subject field for email messages, Explorer will perform partial matching and yield results similar to a wildcard search.</span></span>

## <a name="email--malware"></a><span data-ttu-id="fc5f6-123">E \> -Mail-Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="fc5f6-123">Email \> Malware</span></span>

<span data-ttu-id="fc5f6-124">In dieser Ansicht werden e-Mail-Nachrichten mit Schadsoftware angezeigt.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-124">This view shows email messages identified as containing malware.</span></span>  

<span data-ttu-id="fc5f6-125">Anzeigen von Informationen im Diagramm anhand der Schadsoftware-Familie, der Absenderdomäne, der Absender-IP-Adresse, des Schutzstatus (Aktionen, die von ihren Threat Protection-Features und-Richtlinien in Office 365 ausgeführt wurden) und der Erkennungstechnologie (wie die Schadsoftware erkannt wurde).</span><span class="sxs-lookup"><span data-stu-id="fc5f6-125">View information in the chart by malware family, sender domain, sender IP, protection status (actions taken by your threat protection features and policies in Office 365), and detection technology (how the malware was detected).</span></span>  

![Anzeigen von Daten zu erkannter Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)         

<span data-ttu-id="fc5f6-127">Sehen Sie sich unter dem Diagrammdetails zu den häufigsten Schadsoftware-Familien, die wichtigsten Zielbenutzer und weitere Details zu bestimmten Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-127">Below the chart, view details about top malware families, top targeted users, and more details about specific messages.</span></span> 

## <a name="email--phish"></a><span data-ttu-id="fc5f6-128">E \> -Mail-Phishing</span><span class="sxs-lookup"><span data-stu-id="fc5f6-128">Email \> Phish</span></span>

<span data-ttu-id="fc5f6-129">Diese Ansicht zeigt e-Mail-Nachrichten an, die als Phishing-Versuche identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-129">This view shows email messages identified as phishing attempts.</span></span>  

<span data-ttu-id="fc5f6-130">Anzeigen von Informationen nach Absenderdomäne, Absender-IP und Schutzstatus (Aktionen, die von ihren Funktionen zum Schutz vor Bedrohungen in Office 365 ausgeführt werden).</span><span class="sxs-lookup"><span data-stu-id="fc5f6-130">View information by sender domain, sender IP, and protection status (actions taken by your threat protection features and policies in Office 365).</span></span> 

![Anzeigen von Daten über e-Mails, die als Phishing-Versuche identifiziert wurden](media/2e3f97fa-2b99-47f9-afd6-216d10633c50.png) 

<span data-ttu-id="fc5f6-132">Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-132">Below the chart, view more details about specific messages.</span></span> 

## <a name="email--user-reported"></a><span data-ttu-id="fc5f6-133">E \> -Mail-Benutzer gemeldet</span><span class="sxs-lookup"><span data-stu-id="fc5f6-133">Email \> User-reported</span></span>

<span data-ttu-id="fc5f6-134">In dieser Ansicht werden e-Mails angezeigt, die von Benutzern als Junk-e-Mail oder Phishing-Nachricht gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-134">This view shows email that users have reported as junk, not junk, or phishing email.</span></span>  

<span data-ttu-id="fc5f6-135">Informationen nach Berichtstyp anzeigen (die Bestimmung des Benutzers, dass es sich bei der e-Mail um Junk-e-Mail, nicht um Junk oder Phishing handelt) und nach Zustellungs Grund (Gründe dafür, warum e-Mails an einen bestimmten Speicherort gesendet wurden, beispielsweise eine Spamfilter Richtlinie, eine Nachrichtenfluss Regel, eine Liste blockierter Absender, eine Liste sicherer Absender, usw.).</span><span class="sxs-lookup"><span data-stu-id="fc5f6-135">View information by report type (the user's determination that the email was junk, not junk, or phish), and by delivery reason (reasons why email went to a specific location, such as a spam filter policy, a mail flow rule, a blocked-senders list, a safe-senders list, etc.).</span></span>  

![Anzeigen von Daten über e-Mail-Benutzer, die als Junk, nicht als Junk oder Phishing gemeldet wurden](media/255acd04-0d07-4b29-82af-5060a60c20ab.png)  

<span data-ttu-id="fc5f6-137">Zeigen Sie unterhalb des Diagramms weitere Details zu bestimmten e-Mail-Nachrichten wie Betreff, die IP-Adresse des Absenders, der Benutzer, der die Nachricht als Junk, nicht Junk oder Phishing gemeldet hat, und vieles mehr an.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-137">Below the chart, view more details about specific email messages, such as subject line, the sender's IP address, the user that reported the message as junk, not junk, or phish, and more.</span></span> 

## <a name="email--all-mail"></a><span data-ttu-id="fc5f6-138">Alle \> e-Mails senden</span><span class="sxs-lookup"><span data-stu-id="fc5f6-138">Email \> All mail</span></span>

<span data-ttu-id="fc5f6-139">Diese Ansichten zeigen eine Übersicht über e-Mail-Aktivitäten, einschließlich e-Mails, die aufgrund von Phishing oder Schadsoftware als böswillig identifiziert wurden, sowie für alle nicht-böswilligen e-Mails (normale e-Mail, Spam und Massensendungen).</span><span class="sxs-lookup"><span data-stu-id="fc5f6-139">This views shows an all-up view of email activity, including email identified as malicious due to phishing or malware, as well all non-malicious mail (normal email, spam, and bulk mail).</span></span> 

> [!NOTE]
> <span data-ttu-id="fc5f6-140">Wenn Sie eine Fehlermeldung erhalten, die zu **viele anzuzeigende Daten**liest, fügen Sie einen Filter hinzu, und schränken Sie gegebenenfalls den angezeigten Datums Umfang ein.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-140">If you get an error that reads **Too much data to display**, add a filter and, if necessary, narrow the date range you're viewing.</span></span> 

<span data-ttu-id="fc5f6-141">Wenn Sie einen Filter anwenden möchten, wählen Sie **Absender**aus, wählen Sie ein Element in der Liste aus, und klicken Sie dann auf die Schaltfläche Aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-141">To apply a filter, choose **Sender**, select an item in the list, and then click the Refresh button.</span></span> <span data-ttu-id="fc5f6-142">In unserem Beispiel wurde die **Erkennungstechnologie** als Filter verwendet (es stehen mehrere Optionen zur Verfügung).</span><span class="sxs-lookup"><span data-stu-id="fc5f6-142">In our example, we used **Detection technology** as a filter (there are several options available).</span></span> <span data-ttu-id="fc5f6-143">Anzeigen von Informationen nach Absender, Absenderdomäne, Empfänger, Betreff, Anlage Dateiname, Schadsoftware-Familie, Schutzstatus (Aktionen, die von ihren Threat Protection-Features und-Richtlinien in Office 365 ausgeführt werden), Erkennungstechnologie (wie die Schadsoftware erkannt wurde) und mehr.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-143">View information by sender, sender's domain, recipients, subject, attachment filename, malware family, protection status (actions taken by your threat protection features and policies in Office 365), detection technology (how the malware was detected), and more.</span></span> 

![Anzeigen von Daten zu erkannten e-Mails anhand der Erkennungstechnologie](media/0c032eb3-6021-4174-9f06-ff8f30c245ca.png) 

<span data-ttu-id="fc5f6-145">Zeigen Sie unter dem Diagramm weitere Details zu bestimmten e-Mail-Nachrichten an, beispielsweise Betreff, Empfänger, Absender, Status usw.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-145">Below the chart, view more details about specific email messages, such as subject line, recipient, sender, status, and so on.</span></span> 

## <a name="content--malware"></a><span data-ttu-id="fc5f6-146">Inhalts \> -Schadsoftware</span><span class="sxs-lookup"><span data-stu-id="fc5f6-146">Content \> Malware</span></span>

<span data-ttu-id="fc5f6-147">Diese Ansicht zeigt Dateien, die von Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business und Microsoft Teams als bösartig identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-147">This view shows files that were identified as malicious by Office 365 Advanced Threat Protection in SharePoint Online, OneDrive for Business, and Microsoft Teams.</span></span>

<span data-ttu-id="fc5f6-148">Anzeigen von Informationen nach Malwarefamilie, Erkennungstechnologie (wie die Malware erkannt wurde) und Arbeitslast (OneDrive, SharePoint oder Teams).</span><span class="sxs-lookup"><span data-stu-id="fc5f6-148">View information by malware family, detection technology (how the malware was detected), and workload (OneDrive, SharePoint, or Teams).</span></span> 

![Anzeigen von Daten zu erkannter Schadsoftware](media/d11dc568-b091-4159-b261-df13d76b520b.png)  

<span data-ttu-id="fc5f6-150">Zeigen Sie unter dem Diagramm weitere Details zu bestimmten Dateien an, beispielsweise Dateiname der Anlage, Arbeitsauslastung, Dateigröße, wer die Datei zuletzt geändert hat, und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-150">Below the chart, view more details about specific files, such as attachment filename, workload, file size, who last modified the file, and more.</span></span> 
  
## <a name="new-click-to-filter-capabilities"></a><span data-ttu-id="fc5f6-151">(Neu!) Click-to-Filter-Funktionen</span><span class="sxs-lookup"><span data-stu-id="fc5f6-151">(New!) Click-to-filter capabilities</span></span>

<span data-ttu-id="fc5f6-152">Neu in Explorer ist die Möglichkeit zum Filtern.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-152">New to Explorer is the ability to click to filter.</span></span> <span data-ttu-id="fc5f6-153">Wenn Sie in der Legende auf ein Element klicken, wird dieses Element zu einem Filter für den Bericht.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-153">When you click an item in the legend, that item becomes a filter for the report.</span></span> <span data-ttu-id="fc5f6-154">Nehmen wir beispielsweise an, dass Sie die Malware Ansicht im Explorer betrachten:</span><span class="sxs-lookup"><span data-stu-id="fc5f6-154">For example, suppose we are looking at the Malware view in Explorer:</span></span>
  
![Wechseln Sie zu Threat \> Management Explorer](media/cab32fa2-66f1-4ad5-bc1d-2bac4dbeb48c.png)
  
<span data-ttu-id="fc5f6-156">Wenn Sie in diesem Diagramm auf **ATP-Detonation** klicken, wird eine Ansicht wie die folgende angezeigt:</span><span class="sxs-lookup"><span data-stu-id="fc5f6-156">Clicking **ATP Detonation** in this chart results in a view like this:</span></span> 
  
![Explorer gefiltert, um nur die Ergebnisse der ATO-Detonation anzuzeigen](media/7241d7dd-27bc-467d-9db8-6e806c49df14.png)
  
<span data-ttu-id="fc5f6-158">In dieser Ansicht betrachten wir nun Daten für Dateien, die von [Office 365 ATP Safe Attachments](atp-safe-attachments.md)gezündet wurden.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-158">In this view, we are now looking at data for files that were detonated by [Office 365 ATP Safe Attachments](atp-safe-attachments.md).</span></span> <span data-ttu-id="fc5f6-159">Unter dem Diagramm können Details zu bestimmten e-Mail-Nachrichten mit Anlagen angezeigt werden, die von sicheren ATP-Anlagen erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-159">Below the chart, we can see details about specific email messages that had attachments that were detected by ATP Safe Attachments.</span></span>
  
![Spezifische Details zu e-Mail-Nachrichten mit erkannten Anlagen](media/c91fb05c-d1d4-4085-acc6-f7008a415c2a.png)
  
<span data-ttu-id="fc5f6-161">Durch Auswählen eines oder mehrerer Elemente wird das Menü " **Aktionen** " aktiviert, das verschiedene Auswahlmöglichkeiten für die ausgewählten Elemente bietet.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-161">Selecting one or more items activates the **Actions** menu, which offers several choices from which to choose for the selected item(s).</span></span> 
  
![Durch Auswählen eines Elements wird das Menü "Aktionen" aktiviert.](media/95f127a4-1b2a-4a76-88b9-096e3ba27d1b.png)
  
<span data-ttu-id="fc5f6-163">Die Möglichkeit, mit einem Klick zu filtern und zu bestimmten Details zu navigieren, kann Ihnen viel Zeit bei der Untersuchung von Bedrohungen ersparen.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-163">The ability to filter in a click and navigate to specific details can save you a lot of time in investigating threats.</span></span>
  
## <a name="how-do-i-get-explorer"></a><span data-ttu-id="fc5f6-164">Wie erhalte ich einen Explorer?</span><span class="sxs-lookup"><span data-stu-id="fc5f6-164">How do I get Explorer?</span></span>

<span data-ttu-id="fc5f6-165">Der Explorer ist in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md)enthalten.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-165">Explorer is included in [Office 365 Advanced Threat Protection Plan 2](office-365-ti.md).</span></span> 

<span data-ttu-id="fc5f6-166">Sie müssen über die entsprechenden Berechtigungen verfügen, beispielsweise solche, die einem Sicherheitsadministrator oder einem Sicherheits Leser erteilt wurden, um den Explorer anzuzeigen und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc5f6-166">You must have appropriate permissions, such as those granted to a security administrator or security reader, in order to view and use Explorer.</span></span> <span data-ttu-id="fc5f6-167">Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="fc5f6-167">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span>
  
## <a name="related-topics"></a><span data-ttu-id="fc5f6-168">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="fc5f6-168">Related topics</span></span>

[<span data-ttu-id="fc5f6-169">Berichte und Einblicke im Office 365 &amp; Security Compliance Center</span><span class="sxs-lookup"><span data-stu-id="fc5f6-169">Reports and insights in the Office 365 Security &amp; Compliance Center</span></span>](reports-and-insights-in-security-and-compliance.md)
  
[<span data-ttu-id="fc5f6-170">Suchen und untersuchen von gelieferten Schad-e-Mails (Office 365 Threat Invesitgation und Response)</span><span class="sxs-lookup"><span data-stu-id="fc5f6-170">Find and investigate malicious email that was delivered (Office 365 Threat Invesitgation and Response)</span></span>](investigate-malicious-email-that-was-delivered.md)
  
[<span data-ttu-id="fc5f6-171">Antispam- und Antischadsoftwareschutz in Office 365</span><span class="sxs-lookup"><span data-stu-id="fc5f6-171">Anti-spam and anti-malware protection in Office 365</span></span>](anti-spam-and-anti-malware-protection.md)
  

