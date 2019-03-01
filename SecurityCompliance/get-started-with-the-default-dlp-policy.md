---
title: Erste Schritte mit der standardmäßigen DLP-Richtlinie
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/10/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: e0ada764-6422-4b44-9472-513bed04837b
description: Bevor Sie Ihre erste DLP-Richtlinie (Data Loss Prevention, Datenverlust) erstellen, hilft DLP, Ihre vertraulichen Informationen mit einer Standardrichtlinie zu schützen. Diese Standardrichtlinie und ihre Empfehlung (siehe unten) helfen Ihnen, Ihre vertraulichen Inhalte zu schützen, indem Sie benachrichtigt werden, wenn e-Mails oder Dokumente, die eine Kreditkartennummer enthalten, für eine andere Person außerhalb Ihrer Organisation freigegeben wurden.
ms.openlocfilehash: 3182abcc825c8e27da83ebfb64ed8b2cba6ebcb3
ms.sourcegitcommit: 48fa456981b5c52ab8aeace173c8366b9f36723b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/28/2019
ms.locfileid: "30341316"
---
# <a name="get-started-with-the-default-dlp-policy"></a><span data-ttu-id="1e445-104">Erste Schritte mit der standardmäßigen DLP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1e445-104">Get started with the default DLP policy</span></span>

<span data-ttu-id="1e445-p102">Bevor Sie Ihre erste DLP-Richtlinie (Data Loss Prevention, Datenverlust) erstellen, hilft DLP, Ihre vertraulichen Informationen mit einer Standardrichtlinie zu schützen. Diese Standardrichtlinie und ihre Empfehlung (siehe unten) helfen Ihnen, Ihre vertraulichen Inhalte zu schützen, indem Sie benachrichtigt werden, wenn e-Mails oder Dokumente, die eine Kreditkartennummer enthalten, für eine andere Person außerhalb Ihrer Organisation freigegeben wurden. Diese Empfehlung wird auf der **Start** Seite des Security &amp; Compliance Centers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e445-p102">Before you even create your first data loss prevention (DLP) policy, DLP is helping to protect your sensitive information with a default policy. This default policy and its recommendation (shown below) help keep your sensitive content secure by notifying you when email or documents containing a credit card number were shared with someone outside your organization. You'll see this recommendation on the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="1e445-p103">Sie können dieses Widget verwenden, um schnell anzuzeigen, wann und wie viele vertrauliche Informationen freigegeben wurden, und dann die standardmäßige DLP-Richtlinie in nur einem oder zwei Klicken verfeinern. Sie können die Standard-DLP-Richtlinie auch jederzeit bearbeiten, da Sie vollständig anpassbar ist. Beachten Sie, dass wenn die Empfehlung zunächst nicht angezeigt wird, klicken Sie unten im Abschnitt **Empfohlene für Sie** auf **+ mehr** .</span><span class="sxs-lookup"><span data-stu-id="1e445-p103">You can use this widget to quickly view when and how much sensitive information was shared, and then refine the default DLP policy in just a click or two. You can also edit the default DLP policy at any time because it's fully customizable. Note that if you don't see the recommendation at first, try clicking **+More** at the bottom of the **Recommended for you** section.</span></span> 
  
![Widget mit dem Namen weiter schützen freigegebene Inhalte](media/2bae6dbc-cc92-4f35-b54c-c36e60226b5b.png)
  
## <a name="view-the-report-and-refine-the-default-dlp-policy"></a><span data-ttu-id="1e445-112">Anzeigen des Berichts und verfeinern der standardmäßigen DLP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1e445-112">View the report and refine the default DLP policy</span></span>

<span data-ttu-id="1e445-113">Wenn das Widget zeigt, dass Benutzer vertrauliche Informationen für Personen außerhalb Ihrer Organisation freigegeben haben, wählen Sie unten die Option **DLP-Richtlinie verfeinern** aus.</span><span class="sxs-lookup"><span data-stu-id="1e445-113">When the widget shows you that users have shared sensitive information with people outside your organization, choose **Refine DLP policy** at the bottom.</span></span> 
  
<span data-ttu-id="1e445-p104">Der ausführliche Bericht zeigt Ihnen, wann und wie viele Inhalte mit Kreditkartennummern in den letzten 30 Tagen freigegeben wurden. Beachten Sie, dass Regel Übereinstimmungen bis zu 48 Stunden dauern können, bis Sie im Widget angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1e445-p104">The detailed report shows you when and how much content containing credit card numbers was shared in the past 30 days. Note that rule matches can take up to 48 hours to show up in the widget.</span></span>
  
<span data-ttu-id="1e445-116">Zum Schutz der vertraulichen Informationen, die standardmäßige DLP-Richtlinie:</span><span class="sxs-lookup"><span data-stu-id="1e445-116">To help protect the sensitive information, the default DLP policy:</span></span>
  
- <span data-ttu-id="1e445-117">Erkennt, wenn Inhalte in Exchange, SharePoint und OneDrive, die mindestens eine Kreditkartennummer enthalten, für Personen außerhalb Ihrer Organisation freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1e445-117">Detects when content in Exchange, SharePoint, and OneDrive that contains at least one credit card number is shared with people outside your organization.</span></span>
    
- <span data-ttu-id="1e445-p105">Zeigt einen richtlinientipp an und sendet eine e-Mail-Benachrichtigung an Benutzer, wenn Sie versuchen, diese vertraulichen Informationen für Personen außerhalb Ihrer Organisation freizugeben. Weitere Informationen zu diesen Optionen finden Sie unter [Senden von e-Mail-Benachrichtigungen und Anzeigen von Richtlinien Tipps für DLP-Richtlinien](use-notifications-and-policy-tips.md).</span><span class="sxs-lookup"><span data-stu-id="1e445-p105">Shows a policy tip and sends an email notification to users when they attempt to share this sensitive information with people outside your organization. For more information on these options, see [Send email notifications and show policy tips for DLP policies](use-notifications-and-policy-tips.md).</span></span>
    
- <span data-ttu-id="1e445-p106">Generiert detaillierte Aktivitätsberichte, mit denen Sie nachverfolgen können, wer die Inhalte für Personen außerhalb Ihrer Organisation freigegeben hat. Sie können die [DLP-Berichte](view-the-dlp-reports.md) und [Überwachungsprotokolldaten](search-the-audit-log-in-security-and-compliance.md) (bei **Aktivitäts** = -**DLP**) verwenden, um diese Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="1e445-p106">Generates detailed activity reports so that you can track things like who shared the content with people outside your organization and when they did it. You can use the [DLP reports](view-the-dlp-reports.md) and [audit log data](search-the-audit-log-in-security-and-compliance.md) (where **Activity** = **DLP**) to see this information.</span></span>
    
<span data-ttu-id="1e445-122">Um die standardmäßige DLP-Richtlinie schnell zu verfeinern, haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="1e445-122">To quickly refine the default DLP policy, you can choose to have it:</span></span>
  
- <span data-ttu-id="1e445-123">Senden Sie einen Vorfall Bericht per e-Mail, wenn Benutzer diese vertraulichen Informationen für Personen außerhalb Ihrer Organisation freigeben.</span><span class="sxs-lookup"><span data-stu-id="1e445-123">Send you an incident report email when users share this sensitive information with people outside your organization.</span></span>
    
- <span data-ttu-id="1e445-124">Fügen Sie dem e-Mail-Vorfall Bericht weitere Benutzer hinzu.</span><span class="sxs-lookup"><span data-stu-id="1e445-124">Add other users to the email incident report.</span></span>
    
- <span data-ttu-id="1e445-125">Blockieren des Zugriffs auf den Inhalt, der die vertraulichen Informationen enthält, aber es dem Benutzer ermöglichen, zu überschreiben und freizugeben oder zu senden, wenn Sie dies benötigen.</span><span class="sxs-lookup"><span data-stu-id="1e445-125">Block access to the content containing the sensitive information, but allow the user to override and share or send if they need to.</span></span>
    
<span data-ttu-id="1e445-126">Weitere Informationen zu Vorfall Berichten oder zum Einschränken des Zugriffs finden Sie unter [Übersicht über Richtlinien zur Verhinderung von Datenverlust](data-loss-prevention-policies.md).</span><span class="sxs-lookup"><span data-stu-id="1e445-126">For more information on incident reports or restricting access, see [Overview of data loss prevention policies](data-loss-prevention-policies.md).</span></span>
  
<span data-ttu-id="1e445-127">Wenn Sie diese Optionen später ändern möchten, können Sie die Standard-DLP-Richtlinie jederzeit bearbeiten – weitere Informationen finden Sie im nächsten Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="1e445-127">If you want to change these options later, you can edit the default DLP policy at any time - see the next section.</span></span>
  
![Einstellungen für das benannte Widget weiter schützen von freigegebenen Inhalten](media/dad30a84-2715-4c0a-a5c5-44d85492363e.png)
  
## <a name="edit-the-default-dlp-policy"></a><span data-ttu-id="1e445-129">Bearbeiten der standardmäßigen DLP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1e445-129">Edit the default DLP policy</span></span>

<span data-ttu-id="1e445-130">Diese Richtlinie heißt **default Office 365 DLP Policy** und wird unter **Data Loss Prevention** auf der Seite **Richtlinie** des Security &amp; Compliance Centers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e445-130">This policy is named **Default Office 365 DLP policy** and appears under **Data loss prevention** on the **Policy** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="1e445-p107">Diese Richtlinie ist vollständig anpassbar, genauso wie alle DLP-Richtlinien, die Sie selbst neu erstellen. Sie können die Richtlinie auch deaktivieren oder löschen, damit Ihre Benutzer keine Richtlinien Tipps oder e-Mail-Benachrichtigungen mehr erhalten.</span><span class="sxs-lookup"><span data-stu-id="1e445-p107">This policy is fully customizable, the same as any DLP policy that you create yourself from scratch. You can also turn off or delete the policy, so that your users no longer receive policy tips or email notifications.</span></span>
  
![DLP-Richtlinie namens "Standard Office 365 DLP-Richtlinie"](media/260731e8-4d57-4c98-abec-07b052ec48d5.png)
  
## <a name="when-the-widget-does-and-does-not-appear"></a><span data-ttu-id="1e445-134">Wenn das Widget nicht angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="1e445-134">When the widget does and does not appear</span></span>

<span data-ttu-id="1e445-135">Das Widget **Weitere Schutz freigegebene Inhalte** wird im Abschnitt **Empfohlene für Sie** auf der **Start** Seite des Security &amp; Compliance Centers angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e445-135">The widget named **Further protect shared content** appears in the **Recommended for you** section of the **Home** page of the Security &amp; Compliance Center.</span></span> 
  
<span data-ttu-id="1e445-136">Dieses Widget wird nur angezeigt, wenn:</span><span class="sxs-lookup"><span data-stu-id="1e445-136">This widget appears only when:</span></span>
  
- <span data-ttu-id="1e445-p108">Im Security &amp; Compliance Center oder Exchange Admin Center gibt es keine Richtlinien zur Verhinderung von Datenverlust. Dieses Widget soll Ihnen die ersten Schritte mit DLP erleichtern, sodass es nicht angezeigt wird, wenn Sie bereits über DLP-Richtlinien verfügen.</span><span class="sxs-lookup"><span data-stu-id="1e445-p108">There are no data loss prevention policies in the Security &amp; Compliance Center or Exchange admin center. This widget is intended to help you get started with DLP, so it doesn't appear if you already have DLP policies.</span></span>
    
- <span data-ttu-id="1e445-139">Inhalte, die mindestens eine Kreditkarte enthalten, wurden in den letzten 30 Tagen für eine andere Person außerhalb Ihrer Organisation freigegeben.</span><span class="sxs-lookup"><span data-stu-id="1e445-139">Content containing least one credit card has been shared with someone outside your organization in the past 30 days.</span></span>
    
<span data-ttu-id="1e445-140">Beachten Sie, dass Regel Übereinstimmungen bis zu 48 Stunden dauern können, um für das Widget verfügbar zu sein, daher kann es bis zu zwei Tage dauern, bis die Empfehlung angezeigt wird, nachdem vertrauliche Informationen extern freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="1e445-140">Note that rule matches can take up to 48 hours to be available to the widget, so after sensitive information shared externally is detected, it may take up to two days for the recommendation to appear.</span></span>
  
<span data-ttu-id="1e445-141">Nachdem Sie das Widget zum Verfeinern der standardmäßigen DLP-Richtlinie verwendet haben, wird das Widget auf der **Homepage** ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="1e445-141">Finally, after you use the widget to refine the default DLP policy, the widget disappears from the **Home** page.</span></span> 
  

