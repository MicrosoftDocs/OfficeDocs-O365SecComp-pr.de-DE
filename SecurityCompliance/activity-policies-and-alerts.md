---
title: Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 367f25d3-10a0-4a91-bdae-70ebb7a79c98
description: Definieren Sie Aktivitätsrichtlinien mit Office 365 Cloud App Security, um Warnungen einzurichten, die ausgelöst werden, wenn bestimmte Aktivitäten zu häufig stattfinden. Durch das Einrichten von Richtlinien zum Auslösen von Warnungen können Sie über bestimmte Aktivitäten benachrichtigt werden und diese überwachen.
ms.openlocfilehash: cfa58182ea35551ca3a3807c23e09c9f87c7be82
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30219765"
---
# <a name="activity-policies-and-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="29e08-104">Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="29e08-104">Activity policies and alerts in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="29e08-105">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="29e08-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="29e08-106">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="29e08-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="29e08-107">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="29e08-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="29e08-108">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="29e08-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="29e08-109">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="29e08-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="29e08-110">Planung starten</span><span class="sxs-lookup"><span data-stu-id="29e08-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="29e08-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="29e08-111">You are here!</span></span>  <br/> [<span data-ttu-id="29e08-112">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="29e08-112">Next step</span></span>](anomaly-detection-policies-in-ocas.md) <br/> |[<span data-ttu-id="29e08-113">Verwendung beginnen</span><span class="sxs-lookup"><span data-stu-id="29e08-113">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="29e08-p102">Mit Office 365 Cloud App Security lösen erweiterte Cloud-Verwaltungsrichtlinien Warnungen für bestimmte Aktivitäten aus, die passieren oder zu häufig auftreten. Nehmen Sie beispielsweise an, ein Benutzer versucht, sich bei Office 365 anzumelden und schlägt in einer Minute 70-mal fehl. Nehmen wir an, dass ein anderer Benutzer 7.000-Dateien herunterlädt oder anscheinend aus Kanada angemeldet ist, wenn sich dieser Benutzer an einem anderen Standort befinden soll. Oder schlimmer noch: angenommen, das Konto eines Benutzers wurde kompromittiert, und ein Angreifer verwendet dieses Konto, um auf Cloud-apps und vertrauliche Daten Ihrer Organisation zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="29e08-p102">With Office 365 Cloud App Security, advanced cloud management policies trigger alerts for specific activities that happen or happen too frequently. For example, suppose a user tries to sign in to Office 365 and fails 70 times in one minute. Suppose that another user downloads 7,000 files, or appears to be signed in from Canada, when that user is supposed to be in another location. Or worse, suppose that someone's account has been compromised, and an attacker is using that account to access your organization's cloud apps and sensitive data.</span></span>
  
<span data-ttu-id="29e08-p103">Wenn Sie ein [globaler Administrator oder Sicherheitsadministrator](permissions-in-the-security-and-compliance-center.md)sind, Benachrichtigen Sie Aktivitäts Warnungen, wenn Ereignisse wie diese auftreten. Sie können dann bestimmte Aktionen ausführen, beispielsweise das Anhalten eines Benutzerkontos, bis Sie untersuchen können, was passiert ist.</span><span class="sxs-lookup"><span data-stu-id="29e08-p103">If you are a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), activity alerts notify you when events like these occur. You can then take specific actions, such as suspending a user account until you can investigate what happened.</span></span>
  
> [!NOTE]
> <span data-ttu-id="29e08-p104">Office 365 Cloud App-Sicherheitsrichtlinien unterscheiden sich von [Warnungsrichtlinien im office 365 &amp; Security Compliance Center](alert-policies.md). Die in diesem Artikel beschriebenen Aktivitätsrichtlinien sind im Sicherheitsportal der Office 365 Cloud App definiert und können Ihnen dabei helfen, die Cloud-Umgebung Ihrer Organisation besser zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="29e08-p104">Office 365 Cloud App Security policies are different from [alert policies in the Office 365 Security &amp; Compliance Center](alert-policies.md). The activity policies described in this article are defined in the Office 365 Cloud App Security portal, and can help you better manage your organization's cloud environment.</span></span> 
  
## <a name="before-you-begin"></a><span data-ttu-id="29e08-122">Bevor Sie beginnen</span><span class="sxs-lookup"><span data-stu-id="29e08-122">Before you begin</span></span>

<span data-ttu-id="29e08-123">Stellen Sie Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="29e08-123">Make sure that:</span></span>
  
- <span data-ttu-id="29e08-124">Ihre Organisation verfügt über [Office 365 Cloud App Security](office-365-cas-overview.md), und der Dienst ist [aktiviert](turn-on-office-365-cas.md).</span><span class="sxs-lookup"><span data-stu-id="29e08-124">Your organization has [Office 365 Cloud App Security](office-365-cas-overview.md), and the service is [turned on](turn-on-office-365-cas.md).</span></span>
    
- <span data-ttu-id="29e08-125">Die [Überwachungsprotokollierung](turn-audit-log-search-on-or-off.md) ist für ihre Office 365-Umgebung aktiviert.</span><span class="sxs-lookup"><span data-stu-id="29e08-125">[Audit logging](turn-audit-log-search-on-or-off.md) is turned on for your Office 365 environment.</span></span> 
    
- <span data-ttu-id="29e08-126">Sie sind ein globaler Administrator oder Sicherheitsadministrator für Office 365.</span><span class="sxs-lookup"><span data-stu-id="29e08-126">You are a global administrator or security administrator for Office 365.</span></span>
    
## <a name="create-a-new-activity-policy"></a><span data-ttu-id="29e08-127">Erstellen einer neuen Aktivitätsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="29e08-127">Create a new activity policy</span></span>

1. <span data-ttu-id="29e08-128">Wechseln Sie als globaler Administrator oder Sicherheitsadministrator zum Sicherheitsportal der Cloud-app ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="29e08-128">As a global administrator or security administrator, go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> <br><span data-ttu-id="29e08-129">Dadurch gelangen Sie zur Seite Office 365 Cloud App Security Policies.</span><span class="sxs-lookup"><span data-stu-id="29e08-129">This takes you to the Office 365 Cloud App Security Policies page.</span></span><br><span data-ttu-id="29e08-130">![Wenn Sie zum Office 365 Cloud App Security Portal wechseln, beginnen Sie mit der Seite Richtlinien](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span><span class="sxs-lookup"><span data-stu-id="29e08-130">![When you go to the Office 365 Cloud App Security portal, you start with the Policies page](media/5cb8833c-4e08-438c-bab3-91b5106f6f3f.png)</span></span>
  
2. <span data-ttu-id="29e08-131">Klicken Sie auf **Richtlinie erstellen**, und wählen Sie dann **Aktivitätsrichtlinie**aus.</span><span class="sxs-lookup"><span data-stu-id="29e08-131">Click **Create policy**, and then select **Activity policy**.</span></span><br><span data-ttu-id="29e08-132">![Wenn Sie eine Richtlinie in O365-CAS erstellen, können Sie zwischen Aktivitätsrichtlinien und Erkennungsrichtlinien für Anomalien wählen.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span><span class="sxs-lookup"><span data-stu-id="29e08-132">![When you create a policy in O365 CAS, you can choose between Activity policies and Anomaly Detection policies.](media/79f34535-ddf9-4a5b-a0a3-8766bf9c174c.png)</span></span>
  
3. <span data-ttu-id="29e08-p105">Geben Sie auf der Seite **Aktivitätsrichtlinie erstellen** den Namen und die **Beschreibung**der **Richtlinie** an. Wenn Sie die Richtlinie auf einer Standardvorlage basieren möchten, wählen Sie eine in der Liste **Richtlinienvorlage** aus, oder erstellen Sie Ihre eigene Richtlinie, ohne eine Vorlage zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="29e08-p105">On the **Create activity policy** page, specify the **Policy name** and **Description**. To base your policy on a default template, choose one in the **Policy template** list, or create your own policy without using a template.</span></span><br><span data-ttu-id="29e08-135">![Sie können Aktivitätsrichtlinien mit Office 365 Cloud App Security erstellen.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span><span class="sxs-lookup"><span data-stu-id="29e08-135">![You can create activity policies with Office 365 Cloud App Security.](media/4083a76f-7074-4d6a-8200-6d76d49259d7.png)</span></span>
  
4. <span data-ttu-id="29e08-p106">Wählen Sie einen **Richtlinien Schweregrad** (niedrig, Mittel oder hoch) aus, der misst, wie schwerwiegend es für Sie ist, wenn diese Richtlinie eine Warnung auslöst. Dadurch können Sie Warnungen filtern, wenn Sie Sie später überprüfen.</span><span class="sxs-lookup"><span data-stu-id="29e08-p106">Choose a **Policy severity** (Low, Medium, or High) that measures how serious it is to you if this policy triggers an alert. This will help you filter alerts when you're reviewing them later.</span></span> 
    
5. <span data-ttu-id="29e08-p107">Wählen Sie eine **Kategorie** für diese Richtlinie aus. Dadurch können Sie Warnungen Filtern und sortieren, die ausgelöst wurden, oder Gruppenrichtlinien, wenn Sie Sie überprüfen, um Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="29e08-p107">Choose a **Category** for this policy. This will help you filter and sort alerts that have been triggered, or to group policies when you're reviewing them to make changes.</span></span> 
    
6. <span data-ttu-id="29e08-140">Wählen Sie **Aktivitäts Filter** aus, um andere Aktionen oder Metriken einzurichten, die eine Warnung basierend auf dieser Richtlinie auslösen.</span><span class="sxs-lookup"><span data-stu-id="29e08-140">Choose **Activity filters** to set up other actions or metrics that will trigger an alert based on this policy.</span></span> 
    
7. <span data-ttu-id="29e08-141">Geben Sie unter **Vorgangs Übereinstimmungsparameter**an, ob eine Richtlinienverletzung ausgelöst wird, wenn eine einzelne Aktivität mit den Filtern übereinstimmt oder ob eine angegebene Anzahl von wiederholten Aktivitäten vor dem Auslösen der Warnung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="29e08-141">Under **Activity match parameters**, specify whether a policy violation will be triggered when a single activity matches the filters, or if a specified number of repeated activities is required before the alert triggers.</span></span><br><span data-ttu-id="29e08-142">Wenn Sie **wiederholte Aktivität**auswählen, geben Sie die Anzahl der Aktivitäten, den Zeitrahmen und an, ob eine Verletzung für einen Benutzer innerhalb einer bestimmten app oder für denselben Benutzer mit einer beliebigen App gezählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="29e08-142">If you select **Repeated activity**, specify the number of activities, the time frame, and whether a violation will count for a user within a specific app or for the same user with any app.</span></span>
    
8. <span data-ttu-id="29e08-143">Optional können Sie **Alert erstellen** auswählen, um zusätzliche Benachrichtigungen für den Empfang von Benachrichtigungen von dieser Richtlinie zu erstellen (per e-Mail, Textnachricht oder beides).</span><span class="sxs-lookup"><span data-stu-id="29e08-143">Optionally, you can select **Create alert** to create additional alerts to receive notifications from this policy (via email, text message, or both).</span></span><br><span data-ttu-id="29e08-144">\*\*Stellen Sie sicher, dass Ihr e-Mail-Anbieter `no-reply@cloudappsecurity.com`e-Mails, die gesendet werden, nicht blockiert \*\*.</span><span class="sxs-lookup"><span data-stu-id="29e08-144">**Make sure that your email provider doesn't block emails sent from `no-reply@cloudappsecurity.com`**.</span></span> 
  
9. <span data-ttu-id="29e08-145">Wählen Sie die **Aktionen** aus, die ausgeführt werden sollen, wenn eine Warnung ausgelöst wird, um den Benutzer anzuhalten, oder wenn der Benutzer sich erneut bei Office 365-Apps anmelden muss.</span><span class="sxs-lookup"><span data-stu-id="29e08-145">Choose the **Actions** that should be taken when an alert is triggered to suspend the user or require the user to sign in again to Office 365 apps.</span></span> 
    
10. <span data-ttu-id="29e08-146">Klicken Sie auf **Erstellen** , um die Erstellung der Richtlinie abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="29e08-146">Choose **Create** to finish creating your policy.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="29e08-147">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="29e08-147">Next steps</span></span>

- [<span data-ttu-id="29e08-148">Erkennungsrichtlinien für Anomalien</span><span class="sxs-lookup"><span data-stu-id="29e08-148">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="29e08-149">Integrieren Ihres SIEM-Servers</span><span class="sxs-lookup"><span data-stu-id="29e08-149">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="29e08-150">Überarbeiten und Aktionen für Warnungen</span><span class="sxs-lookup"><span data-stu-id="29e08-150">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="29e08-151">Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung</span><span class="sxs-lookup"><span data-stu-id="29e08-151">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

