---
title: Nutzungsaktivitäten nach der Einführung von Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 01/28/2019
ms.audience: ITPro
ms.topic: conceptual
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: Nachdem Sie Office 365 Cloud App Security eingerichtet und bereitgestellt haben, sollten Sie bestimmte Aufgaben ausführen, um sicherzustellen, dass Ihre Konfiguration korrekt ist und dass Sie für regelmäßige Besprechungen vorbereitet sind.
ms.openlocfilehash: 232de4df1d1eb4debdddcee2c1d8672d1aeb4b21
ms.sourcegitcommit: e7a776a04ef6ed5e287a33cfdc36aa2d72862b55
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/29/2019
ms.locfileid: "30999948"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="9f5e6-103">Nutzungsaktivitäten nach der Einführung von Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9f5e6-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="9f5e6-104">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9f5e6-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="9f5e6-105">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9f5e6-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="9f5e6-106">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="9f5e6-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="9f5e6-107">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9f5e6-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="9f5e6-108">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="9f5e6-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="9f5e6-109">Planung starten</span><span class="sxs-lookup"><span data-stu-id="9f5e6-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="9f5e6-110">Starten der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="9f5e6-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="9f5e6-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="9f5e6-111">You are here!</span></span>  <br/> [<span data-ttu-id="9f5e6-112">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="9f5e6-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="9f5e6-113">Office 365 Cloud App Security ist in Office 365 Enterprise E5 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-113">Office 365 Cloud App Security is available in Office 365 Enterprise E5.</span></span> <span data-ttu-id="9f5e6-114">Wenn Ihre Organisation ein anderes Office 365 Enterprise-Abonnement verwendet, kann Office 365 Cloud App Security als Add-on erworben werden.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-114">If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on.</span></span> <span data-ttu-id="9f5e6-115">(klicken sie als globaler administrator im Microsoft 365 admin center auf **abrechnungs** \> **abonnements hinzufügen**.) Weitere Informationen finden Sie unter [office 365 Platform Service Description: office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) und [kaufen oder Bearbeiten eines add-ons für Office 365 for Business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="9f5e6-115">(As a global administrator, in the Microsoft 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://docs.microsoft.com/office365/servicedescriptions/office-365-platform-service-description/office-365-securitycompliance-center) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="9f5e6-116">Nachdem Sie Office 365 Cloud App Security eingerichtet und konfiguriert haben, sollten Sie bestimmte Nutzungs Aufgaben als globaler Office 365-Administrator oder Sicherheitsadministrator für Ihre Organisation ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="9f5e6-117">Durch Ausführen dieser Aufgaben können Sie sicherstellen, dass die Office 365 Cloud App-Sicherheit ordnungsgemäß konfiguriert ist, Ihre Richtlinien auf dem neuesten Stand sind und Ihre Organisation Wert aus Office 365 realisiert.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-117">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365.</span></span> <span data-ttu-id="9f5e6-118">Verwenden Sie diesen Artikel als Leitfaden für die Planung dieser Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-118">Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="9f5e6-119">Sie müssen ein globaler Administrator oder Sicherheitsadministrator sein, um die in diesem Artikel beschriebenen Aufgaben ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-119">You must be a global administrator or security administrator to perform the tasks described in this article.</span></span> <span data-ttu-id="9f5e6-120">Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="9f5e6-120">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="9f5e6-121">Aktivitäten nach der Erstkonfiguration und der Einführung von Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9f5e6-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="9f5e6-122">Nachdem Office 365 Cloud App Security konfiguriert und bereitgestellt wurde, müssen Sie als globaler Administrator oder Sicherheitsadministrator mehrere Punkte berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="9f5e6-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="9f5e6-123">Welche Aufgaben müssen dem IT-Abteilungskalender hinzugefügt werden?</span><span class="sxs-lookup"><span data-stu-id="9f5e6-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="9f5e6-124">Wie können Sie sicherstellen, dass die Office 365 Cloud App-Sicherheit so konfiguriert ist, dass Sie den richtigen Richtliniensatz im Laufe der Zeit verwendet?</span><span class="sxs-lookup"><span data-stu-id="9f5e6-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="9f5e6-125">Welche Arten von Zusammenfassungsinformationen sollten Sie an die IT-Verwaltungs Kette senden?</span><span class="sxs-lookup"><span data-stu-id="9f5e6-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="9f5e6-126">In der folgenden Tabelle werden die laufenden Aufgaben kurz zusammengefasst, die Sie ausführen möchten, sowie periodische Aufgaben, die Sie in Betracht ziehen sollten, zum Kalender Ihrer IT-Abteilung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="9f5e6-127">**Laufende Aufgaben**</span><span class="sxs-lookup"><span data-stu-id="9f5e6-127">**Ongoing tasks**</span></span>|<span data-ttu-id="9f5e6-128">**Periodische Aufgaben**</span><span class="sxs-lookup"><span data-stu-id="9f5e6-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9f5e6-129">Überwachen der e-Mail-Konten, an die Sie Warnmeldungen senden</span><span class="sxs-lookup"><span data-stu-id="9f5e6-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="9f5e6-130">Überwachen von Branchen-Cyber Nachrichten Feeds für die neuesten Informationen zu neuen Cyber-Angriffen</span><span class="sxs-lookup"><span data-stu-id="9f5e6-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="9f5e6-131">Sicherheitswarnungen zur Identifizierung und Behandlung von Sicherheitsvorfällen und-Risiken</span><span class="sxs-lookup"><span data-stu-id="9f5e6-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="9f5e6-132">Zusammenfassen aller Sicherheitsvorfälle und-Lösungen in einem zentralen Protokoll</span><span class="sxs-lookup"><span data-stu-id="9f5e6-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="9f5e6-133">Durchführen von monatlichen oder vierteljährlichen Bewertungen von Sicherheitswarnungen in Office 365 Cloud App zum Erkennen von Anomalien und Analysieren von Trends</span><span class="sxs-lookup"><span data-stu-id="9f5e6-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="9f5e6-134">Durchführen von monatlichen oder vierteljährlichen Überprüfungen Ihrer vorhandenen Office 365 Cloud App-Sicherheitsrichtlinien, um Verbesserungen in der Cloud-App-Sicherheit in Office 365 und neue Cyberattacken und-Trends in Cyber zu berücksichtigen</span><span class="sxs-lookup"><span data-stu-id="9f5e6-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="9f5e6-135">Abhängig von der Größe Ihrer Organisation und dem Interesse an Überwachung und Verwaltung einer Sicherheitsstufe können Sie eine monatliche Zusammenfassung für Ihre IT-Verwaltungs Kette erstellen, die Folgendes umfasst:</span><span class="sxs-lookup"><span data-stu-id="9f5e6-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="9f5e6-136">Die verschiedenen Typen von Sicherheitsvorfällen, die mit Office 365 Cloud App Security identifiziert wurden</span><span class="sxs-lookup"><span data-stu-id="9f5e6-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="9f5e6-137">Zusammenfassende Informationen aus dem zentralen Protokoll der Sicherheitsvorfälle, wie die Anzahl der erkannten Vorfälle</span><span class="sxs-lookup"><span data-stu-id="9f5e6-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="9f5e6-138">Warnungs Trends und ihre Adressierung</span><span class="sxs-lookup"><span data-stu-id="9f5e6-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="9f5e6-139">Die neuesten Cyber-Trends</span><span class="sxs-lookup"><span data-stu-id="9f5e6-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="9f5e6-140">Empfehlungen für Änderungen der Sicherheitsrichtlinien für Office 365 Cloud APP und deren Auswirkungen auf Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="9f5e6-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="9f5e6-141">Aktivitäten nach der Einführung des Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9f5e6-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="9f5e6-142">Wenn seit der anfänglichen Konfiguration oder Wartung Ihrer Office 365 Cloud App-Sicherheitsrichtlinien eine lange Zeit vergangen ist, führen Sie die folgenden Schritte aus, um zu einer Konfiguration zurückzukehren, die die Sicherheitsziele ihrer Organisation und die aktuellen Funktionen widerspiegelt. von Office 365 Cloud App Security:</span><span class="sxs-lookup"><span data-stu-id="9f5e6-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="9f5e6-143">Bestimmen Sie das Datum der letzten Konfigurationsänderung für Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="9f5e6-144">Verstehen Sie Ihre aktuelle Office 365 Cloud App-Sicherheitskonfiguration, und passen Sie diese Richtlinien nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-144">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed.</span></span> <span data-ttu-id="9f5e6-145">Stellen Sie beispielsweise sicher, dass Sie wissen, wo Warnungen per e-Mail gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-145">For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="9f5e6-146">Unter [What es New in office 365 Cloud App Security](new-in-office-365-cas.md) für Produktänderungen seit der letzten Konfiguration von Office 365 Cloud App Security.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="9f5e6-147">Führen Sie eine Analyse der Sicherheitswarnungen und Protokolle der Office 365 Cloud App aus, um Anomalien zu erkennen und Trends zu analysieren.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="9f5e6-148">Überprüfen Sie Branchen Cyber Trends, um sich über die neuesten Sicherheitsbedrohungen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="9f5e6-149">Führen Sie eine Analyse der Änderungen aus, die an den aktuellen Sicherheitsrichtlinien von Office 365 Cloud App vorgenommen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-149">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies.</span></span> <span data-ttu-id="9f5e6-150">Integrieren von Office 365 Cloud App-Sicherheitsfeatures, aktuellen Anomalien und Cyber-Trends.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-150">Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends.</span></span> <span data-ttu-id="9f5e6-151">Empfehlen Sie Änderungen an vorhandenen Richtlinien oder die Erstellung neuer Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-151">Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="9f5e6-152">Planen Sie die Implementierung der Richtlinienänderungen.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-152">Make a plan for implementing the policy changes.</span></span> <span data-ttu-id="9f5e6-153">Kommunizieren Sie die Folgen der vorgeschlagenen Änderungen bei Bedarf mit Ihren Endbenutzern.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-153">Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="9f5e6-154">Implementieren der Änderungen der Sicherheitsrichtlinien für die Office 365 Cloud-app.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="9f5e6-155">ÜberWachen von Endbenutzer-Feedback und Office 365 Cloud App-Sicherheitswarnungen und Anpassen von Richtlinien im Laufe der Zeit.</span><span class="sxs-lookup"><span data-stu-id="9f5e6-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="9f5e6-156">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="9f5e6-156">Next steps</span></span>

- [<span data-ttu-id="9f5e6-157">Untersuchen einer Aktivität</span><span class="sxs-lookup"><span data-stu-id="9f5e6-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="9f5e6-158">Anhalten oder Wiederherstellen eines Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="9f5e6-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="9f5e6-159">Verwalten von OAuth-apps</span><span class="sxs-lookup"><span data-stu-id="9f5e6-159">Manage OAuth apps</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="9f5e6-160">Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="9f5e6-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="9f5e6-161">Anzeigen einer Liste unterstützter [Webdatenverkehr-Protokolle und Datenquellen](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="9f5e6-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

