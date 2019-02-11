---
title: Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Definieren Sie die Aktivität Richtlinien mit Office 365-Cloud-App-Sicherheit, um Benachrichtigungen einrichten ausgelöst, wenn bestimmte Aktivitäten auftreten oder zu häufig vorkommen. Durch das Einrichten von Richtlinien für Warnungen ausgelöst, benachrichtigt werden können und bestimmte Vorgänge überwachen.
ms.openlocfilehash: af364e7ff96f6d18b60d3267c5992d4c5533ea8c
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29604092"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="3a871-104">Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="3a871-104">Activity policies and alerts in Office 365 Cloud App Security</span></span>

<span data-ttu-id="3a871-105">Office 365 Advanced Security Management ist jetzt Office 365-Cloud-App-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="3a871-105">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="3a871-106">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="3a871-106">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="3a871-107">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="3a871-107">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="3a871-108">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="3a871-108">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="3a871-109">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="3a871-109">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="3a871-110">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="3a871-110">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="3a871-111">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="3a871-111">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="3a871-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="3a871-112">You are here!</span></span>  <br/> [<span data-ttu-id="3a871-113">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="3a871-113">Next step</span></span>](anomaly-detection-policies-in-ocas.md) <br/> |[<span data-ttu-id="3a871-114">Starten Sie die Nutzung</span><span class="sxs-lookup"><span data-stu-id="3a871-114">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="3a871-p102">Mit Office 365 Cloud App-Sicherheit auslösen erweiterte Cloud Informationsverwaltungsrichtlinien Warnungen für bestimmte Aktivitäten, die auftreten oder zu häufig vorkommen. Nehmen wir beispielsweise bei ein Benutzer versucht, sich bei Office 365 anmelden und ein Fehler auftritt, 70 Mal in einer Minute. Angenommen Sie, ein anderer Benutzer 7.000 Dateien Downloads oder angezeigt wird, in Kanada angemeldet sein, wenn der Benutzer an einem anderen Standort werden soll. Oder schlechter, nehmen Sie an, dass die Person Konto gefährdet, und ein Angreifer dieses Konto Zugriff auf die Cloud apps Ihrer Organisation und vertrauliche Daten verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a871-p102">With Office 365 Cloud App Security, advanced cloud management policies trigger alerts for specific activities that happen or happen too frequently. For example, suppose a user tries to sign in to Office 365 and fails 70 times in one minute. Suppose that another user downloads 7,000 files, or appears to be signed in from Canada, when that user is supposed to be in another location. Or worse, suppose that someone's account has been compromised, and an attacker is using that account to access your organization's cloud apps and sensitive data.</span></span>
  
<span data-ttu-id="3a871-p103">Wenn Sie ein [globaler Administrator oder Sicherheitsadministrator](permissions-in-the-security-and-compliance-center.md)sind, benachrichtigen Aktivität Benachrichtigungen, dass Sie, wenn Ereignisse wie diese auftreten. Sie können dann übernehmen bestimmte Aktionen, wie beispielsweise ein Benutzerkonto aussetzen, bis Sie untersuchen können, was passiert ist.</span><span class="sxs-lookup"><span data-stu-id="3a871-p103">If you are a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), activity alerts notify you when events like these occur. You can then take specific actions, such as suspending a user account until you can investigate what happened.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3a871-p104">Office 365 Cloud App-Sicherheitsrichtlinien unterscheiden sich von [Warnen Richtlinien in die Office 365-Sicherheit &amp; Compliance Center](alert-policies.md). Cloud-Umgebung Ihrer Organisation verwalten der Aktivität in diesem Artikel beschriebenen Richtlinien sind in der Cloud App Sicherheit in Office 365-Portal definiert und können Ihnen helfen.</span><span class="sxs-lookup"><span data-stu-id="3a871-p104">Office 365 Cloud App Security policies are different from [alert policies in the Office 365 Security &amp; Compliance Center](alert-policies.md). The activity policies described in this article are defined in the Office 365 Cloud App Security portal, and can help you better manage your organization's cloud environment.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="3a871-123">Bevor Sie beginnen:</span><span class="sxs-lookup"><span data-stu-id="3a871-123">Before you begin</span></span>

<span data-ttu-id="3a871-124">Stellen Sie Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="3a871-124">Make sure that:</span></span>
  
- <span data-ttu-id="3a871-125">Ihre Organisation verfügt [Office 365-Cloud-App-Sicherheit](office-365-cas-overview.md), und der Dienst ist [aktiviert](turn-on-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="3a871-125">Your organization has [Office 365 Cloud App Security](office-365-cas-overview.md), and the service is [turned on](turn-on-office-365-cas.md).</span></span>
    
- <span data-ttu-id="3a871-126">[Protokollierung](turn-audit-log-search-on-or-off.md) ist für Ihre Office 365-Umgebung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3a871-126">[Audit logging](turn-audit-log-search-on-or-off.md) is turned on for your Office 365 environment.</span></span> 
    
- <span data-ttu-id="3a871-127">Sie sind ein globaler Administrator oder Sicherheitsadministrator für Office 365.</span><span class="sxs-lookup"><span data-stu-id="3a871-127">You are a global administrator or security administrator for Office 365.</span></span>
    
## <a name="create-a-new-activity-policy"></a><span data-ttu-id="3a871-128">Erstellen einer neuen Richtlinie Aktivität</span><span class="sxs-lookup"><span data-stu-id="3a871-128">Create a new activity policy</span></span>

1. <span data-ttu-id="3a871-129">Als globaler Administrator oder Sicherheitsadministrator, wechseln Sie zum Portal Cloud App-Sicherheit ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) und zur Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="3a871-129">As a global administrator or security administrator, go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> <br><span data-ttu-id="3a871-130">Dadurch gelangen Sie zur Seite Office 365 Cloud App-Sicherheitsrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="3a871-130">This takes you to the Office 365 Cloud App Security Policies page.</span></span><br><span data-ttu-id="3a871-131">![Wenn Sie das Cloud-App Sicherheit in Office 365-Portal aufrufen, beginnen Sie mit der Seite Richtlinien](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span><span class="sxs-lookup"><span data-stu-id="3a871-131">![When you go to the Office 365 Cloud App Security portal, you start with the Policies page](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span></span>
  
2. <span data-ttu-id="3a871-132">Klicken Sie auf **Richtlinie erstellen**, und wählen Sie dann auf **Richtlinie Aktivität**.</span><span class="sxs-lookup"><span data-stu-id="3a871-132">Click **Create policy**, and then select **Activity policy**.</span></span><br><span data-ttu-id="3a871-133">![Wenn Sie eine Richtlinie in O365 CAS erstellen, können Sie zwischen Aktivität und Normalbetriebswerte Richtlinien auswählen.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span><span class="sxs-lookup"><span data-stu-id="3a871-133">![When you create a policy in O365 CAS, you can choose between Activity policies and Anomaly Detection policies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span></span>
  
3. <span data-ttu-id="3a871-p105">Geben Sie auf der Seite **die Aktivität Richtlinie erstellen** den **Richtliniennamen** und eine **Beschreibung**ein. Um die Richtlinie auf eine entsprechende Standardvorlage basieren soll, wählen Sie in der Liste **Vorlagen für Gruppenrichtlinien** , oder erstellen Sie eine eigene Richtlinie ohne eine Vorlage.</span><span class="sxs-lookup"><span data-stu-id="3a871-p105">On the **Create activity policy** page, specify the **Policy name** and **Description**. To base your policy on a default template, choose one in the **Policy template** list, or create your own policy without using a template.</span></span><br><span data-ttu-id="3a871-136">![Sie können mit Office 365-Cloud-App-Sicherheit Aktivität Richtlinien erstellen.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span><span class="sxs-lookup"><span data-stu-id="3a871-136">![You can create activity policies with Office 365 Cloud App Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span></span>
  
4. <span data-ttu-id="3a871-p106">Wählen Sie eine **Richtlinie Schweregrad** (niedrig, Mittel oder hoch), mit denen gemessen, wie schwerwiegend für Sie ist, wenn diese Richtlinie eine Warnung ausgelöst wird. So können Sie Warnungen gefiltert werden, wenn Sie später überprüfen möchten.</span><span class="sxs-lookup"><span data-stu-id="3a871-p106">Choose a **Policy severity** (Low, Medium, or High) that measures how serious it is to you if this policy triggers an alert. This will help you filter alerts when you're reviewing them later.</span></span> 
    
5. <span data-ttu-id="3a871-p107">Wählen Sie eine **Kategorie** für diese Richtlinie. Dies hilft Ihnen filtern und Sortieren Warnungen, die ausgelöst wurden, oder wenn Sie diese Änderungen vornehmen können Sie feststellen, Gruppenrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="3a871-p107">Choose a **Category** for this policy. This will help you filter and sort alerts that have been triggered, or to group policies when you're reviewing them to make changes.</span></span> 
    
6. <span data-ttu-id="3a871-141">Wählen Sie **über Benutzeraktivität – Filter** einrichten, andere Aktionen oder Metriken, die eine Warnung basierend auf dieser Richtlinie ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="3a871-141">Choose **Activity filters** to set up other actions or metrics that will trigger an alert based on this policy.</span></span> 
    
7. <span data-ttu-id="3a871-142">Klicken Sie unter **Aktivität Parametern entsprechen**Geben Sie an, ob eine Richtlinie Verletzung ausgelöst wird, wenn eine einzelne Aktivität die Filter entspricht, oder ob eine angegebene Anzahl von Aktivitäten wiederholt erforderlich ist, bevor die Warnung löst.</span><span class="sxs-lookup"><span data-stu-id="3a871-142">Under **Activity match parameters**, specify whether a policy violation will be triggered when a single activity matches the filters, or if a specified number of repeated activities is required before the alert triggers.</span></span><br><span data-ttu-id="3a871-143">Wenn Sie **wiederholt Aktivität**auswählen, geben Sie die Anzahl der Aktivitäten, den Zeitrahmen und gibt an, ob eine Verletzung für einen Benutzer in eine bestimmte app oder für den gleichen Benutzer mit einer beliebigen app zählen wird.</span><span class="sxs-lookup"><span data-stu-id="3a871-143">If you select **Repeated activity**, specify the number of activities, the time frame, and whether a violation will count for a user within a specific app or for the same user with any app.</span></span>
    
8. <span data-ttu-id="3a871-144">Optional können Sie **Create-Benachrichtigung** , die zusätzliche Benachrichtigungen Erhalt von Benachrichtigungen aus dieser Richtlinie (per e-Mail, Textnachricht oder beides) erstellen auswählen.</span><span class="sxs-lookup"><span data-stu-id="3a871-144">Optionally, you can select **Create alert** to create additional alerts to receive notifications from this policy (via email, text message, or both).</span></span><br><span data-ttu-id="3a871-145">\*\*Stellen Sie sicher, dass Ihre e-Mail-Anbieter von gesendeten e-Mails nicht blockiert `no-reply@cloudappsecurity.com` \*\*.</span><span class="sxs-lookup"><span data-stu-id="3a871-145">**Make sure that your email provider doesn't block emails sent from `no-reply@cloudappsecurity.com`**.</span></span> 
  
9. <span data-ttu-id="3a871-146">Wählen Sie die **Aktionen** , die ausgeführt werden sollte, wenn eine Warnung ausgegeben wird, zu der Benutzer muss der Benutzer erneut anmelden für Office 365-apps.</span><span class="sxs-lookup"><span data-stu-id="3a871-146">Choose the **Actions** that should be taken when an alert is triggered to suspend the user or require the user to sign in again to Office 365 apps.</span></span> 
    
10. <span data-ttu-id="3a871-147">Wählen Sie **Create** zum Abschließen der Erstellung der Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="3a871-147">Choose **Create** to finish creating your policy.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="3a871-148">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="3a871-148">Next steps</span></span>

- [<span data-ttu-id="3a871-149">Anomalie Erkennungsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="3a871-149">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="3a871-150">Integrieren von Ihrem Server SIEM</span><span class="sxs-lookup"><span data-stu-id="3a871-150">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="3a871-151">Lesen und Ausführen einer Aktion Warnungen</span><span class="sxs-lookup"><span data-stu-id="3a871-151">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="3a871-152">Gruppieren Sie Ihre IP-Adressen zur Vereinfachung der Verwaltung</span><span class="sxs-lookup"><span data-stu-id="3a871-152">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

