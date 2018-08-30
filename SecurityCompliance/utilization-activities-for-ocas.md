---
title: Auslastung Aktivitäten nach der Einführung der Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: conceptual
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 86f414ad-81de-4703-b40a-c6615bbe9108
description: Nachdem Sie Office 365-Cloud-App-Sicherheit eingeführt und eingerichtet haben, sollten Sie sicherstellen, dass Ihre Konfiguration korrekt ist und dass Sie, für die regelmäßige Überprüfung bereit sind bestimmte Aufgaben ausführen.
ms.openlocfilehash: bc8cfad8eb9d9444066c3193ec2978e9ffd9f56a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529220"
---
# <a name="utilization-activities-after-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="d88a8-103">Auslastung Aktivitäten nach der Einführung der Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d88a8-103">Utilization activities after rolling out Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="d88a8-104">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="d88a8-104">****Evaluation** \>**</span></span>|<span data-ttu-id="d88a8-105">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="d88a8-105">****Planning** \>**</span></span>|<span data-ttu-id="d88a8-106">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="d88a8-106">****Deployment** \>**</span></span>|<span data-ttu-id="d88a8-107">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="d88a8-107">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="d88a8-108">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="d88a8-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="d88a8-109">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="d88a8-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="d88a8-110">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="d88a8-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="d88a8-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="d88a8-111">You are here!</span></span>  <br/> [<span data-ttu-id="d88a8-112">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="d88a8-112">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |
   
> [!NOTE]
> <span data-ttu-id="d88a8-p101">Office 365-Cloud-App-Sicherheit ist in Office 365 Enterprise E5 verfügbar. Wenn in Ihrer Organisation ein weiteres Abonnement von Office 365 Enterprise verwendet wird, kann Office 365-Cloud-App-Sicherheit als Add-on erworben werden. (Als ein globaler Administrator in der Office 365-Verwaltungskonsole, wählen Sie **Abrechnung** \> **Hinzufügen Abonnements**.) Weitere Informationen finden Sie unter [Office 365-Plattformdienstbeschreibung: Sicherheit in Office 365 &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) und [gekauft oder bearbeiten Sie ein Add-on für Office 365 für Unternehmen](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="d88a8-p101">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
<span data-ttu-id="d88a8-116">Nachdem Sie einrichten und Office 365-Cloud-App-Sicherheit konfiguriert haben, sollten Sie bestimmte Aufgaben Auslastung als globaler Office 365-Administrator oder Sicherheitsadministrator für Ihre Organisation ausführen.</span><span class="sxs-lookup"><span data-stu-id="d88a8-116">After you have set up and configured Office 365 Cloud App Security, you'll want to perform certain utilization tasks as an Office 365 global administrator or security administrator for your organization.</span></span> 

<span data-ttu-id="d88a8-p102">Durch Ausführen dieser Aufgaben müssen Sie sicherstellen, dass Office 365-Cloud-App-Sicherheit ordnungsgemäß konfiguriert ist, Ihre Richtlinien auf dem aktuellen Stand sind und Ihrer Organisation Wert von Office 365 erkennt. Verwenden Sie diesen Artikel als Leitfaden, die Ihnen bei der Planung für diese Aufgaben unterstützen.</span><span class="sxs-lookup"><span data-stu-id="d88a8-p102">By performing these tasks, you'll help ensure that Office 365 Cloud App Security is configured correctly, your policies are up to date, and your organization realizes value from Office 365. Use this article as a guide to help you plan for these tasks.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d88a8-p103">Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der Aufgaben in diesem Artikel beschrieben werden. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="d88a8-p103">You must be a global administrator or security administrator to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
    
## <a name="activities-after-the-initial-configuration-and-rollout-of-office-365-cloud-app-security"></a><span data-ttu-id="d88a8-121">Aktivitäten nach der Erstkonfiguration und Einführung von Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d88a8-121">Activities after the initial configuration and rollout of Office 365 Cloud App Security</span></span>

<span data-ttu-id="d88a8-122">Nach Office 365-Cloud-App-Sicherheit, konfiguriert und, als ein globaler Administrator oder Sicherheitsadministratoren eingeführt, müssen Sie mehrere Faktoren berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="d88a8-122">After Office 365 Cloud App Security is configured and rolled out, as a global administrator or security administrators, you have several things to consider:</span></span>
  
- <span data-ttu-id="d88a8-123">Was müssen Aufgaben der IT-Abteilungskalender hinzugefügt werden?</span><span class="sxs-lookup"><span data-stu-id="d88a8-123">What tasks need to be added to the IT department calendar?</span></span>
    
- <span data-ttu-id="d88a8-124">Wie können Sie sicherstellen, dass Office 365-Cloud-App-Sicherheit für die Verwendung der richtigen Richtlinien über einen Zeitraum konfiguriert ist?</span><span class="sxs-lookup"><span data-stu-id="d88a8-124">How can you make sure Office 365 Cloud App Security is configured to use the right set of policies over time?</span></span>
    
- <span data-ttu-id="d88a8-125">Welche Arten von zusammenfassende Informationen sollten Sie die hinauf Management IT senden?</span><span class="sxs-lookup"><span data-stu-id="d88a8-125">What kinds of summary information should you send up the IT management chain?</span></span>
    
<span data-ttu-id="d88a8-126">In der folgenden Tabelle werden kurz zusammengefasst, die laufende Aufgaben vorgestellt, die Sie ausführen möchten und periodischen Aufgaben, die Sie berücksichtigen sollten, Ihre IT-Abteilung Kalender hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d88a8-126">The following table briefly summarizes the ongoing tasks you'll want to perform and periodic tasks you should consider adding to your IT department's calendar.</span></span>
  
|<span data-ttu-id="d88a8-127">**Laufende Vorgänge**</span><span class="sxs-lookup"><span data-stu-id="d88a8-127">**Ongoing tasks**</span></span>|<span data-ttu-id="d88a8-128">**Periodische Aufgaben**</span><span class="sxs-lookup"><span data-stu-id="d88a8-128">**Periodic tasks**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d88a8-129">Überwachen der e-Mail-Konten, die an denen Sie Warnhinweise senden</span><span class="sxs-lookup"><span data-stu-id="d88a8-129">Monitor the email accounts to which you are sending alert messages</span></span>  <br/>  <span data-ttu-id="d88a8-130">Überwachen der Branche Sicherheit im Internet-Newsfeeds die aktuellsten Informationen zu neuen im Internet-Angriffen</span><span class="sxs-lookup"><span data-stu-id="d88a8-130">Monitor industry cybersecurity news feeds for the latest information about new cyber attacks</span></span>  <br/>  <span data-ttu-id="d88a8-131">Handeln Sie aufgrund von Sicherheitshinweise zum Identifizieren und beheben Sie Sicherheitsvorfälle und Risiken</span><span class="sxs-lookup"><span data-stu-id="d88a8-131">Act on security alerts to identify and address security incidents and risks</span></span>  <br/>  <span data-ttu-id="d88a8-132">Zusammenfassen von jedem Sicherheitsvorfall und Auflösung in einem zentralen Protokoll</span><span class="sxs-lookup"><span data-stu-id="d88a8-132">Summarize each security incident and resolution in a central log</span></span>  <br/> | <span data-ttu-id="d88a8-133">Führen Sie monatliche oder vierteljährlich angezeigt Bewertungen von Office 365-Cloud-App-Sicherheit Warnungen zu ins Auge fällt Bildschirmdarstellung auftreten und Analysieren von trends</span><span class="sxs-lookup"><span data-stu-id="d88a8-133">Perform monthly or quarterly reviews of Office 365 Cloud App Security alerts to spot anomalies and analyze trends</span></span>  <br/>  <span data-ttu-id="d88a8-134">Führen Sie monatlich oder vierteljährlich prüft Ihre vorhandenen Office 365-Cloud-App-Sicherheit Richtlinien zum Einschließen von Verbesserungen in Office 365-Cloud-App-Sicherheit und Adresse neue Cyber und Trends bei der Sicherheit im Internet</span><span class="sxs-lookup"><span data-stu-id="d88a8-134">Perform monthly or quarterly reviews of your existing Office 365 Cloud App Security policies to include enhancements in Office 365 Cloud App Security and address new cyberattacks and trends in cybersecurity</span></span>  <br/> |
   
<span data-ttu-id="d88a8-135">Je nach Größe Ihrer Organisation und Interesse an und Überwachen einer Lohnskala Sicherheit können Sie eine monatliche Zusammenfassung für Ihre IT-Management-Kette kompilieren, die enthält:</span><span class="sxs-lookup"><span data-stu-id="d88a8-135">Depending on your organization's size and interest in monitoring and maintaining a security stature, you can compile a monthly summary for your IT management chain that includes:</span></span>
  
- <span data-ttu-id="d88a8-136">Die verschiedenen Typen von Sicherheitsvorfälle identifiziert mit Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d88a8-136">The different types of security incidents identified with Office 365 Cloud App Security</span></span>
    
- <span data-ttu-id="d88a8-137">Zusammenfassende Informationen aus der zentralen Protokoll der handelt, wie die Anzahl der Vorfälle erkannt</span><span class="sxs-lookup"><span data-stu-id="d88a8-137">Summary information from your central log of the security incidents, such as number of incidents detected</span></span>
    
- <span data-ttu-id="d88a8-138">Warnung Trends und wie sie behoben wurden</span><span class="sxs-lookup"><span data-stu-id="d88a8-138">Alert trends and how they were addressed</span></span>
    
- <span data-ttu-id="d88a8-139">Die neuesten Trends Sicherheit im Internet</span><span class="sxs-lookup"><span data-stu-id="d88a8-139">The latest cybersecurity trends</span></span>
    
- <span data-ttu-id="d88a8-140">Empfehlungen für die Änderung der Office 365 Cloud App Sicherheitsrichtlinien und deren Einfluss auf die Endbenutzer</span><span class="sxs-lookup"><span data-stu-id="d88a8-140">Recommendations for Office 365 Cloud App Security policy changes and their impact on end users</span></span>
    
## <a name="activities-after-time-has-passed-since-rolling-out-office-365-cloud-app-security"></a><span data-ttu-id="d88a8-141">Aktivitäten, nachdem Zeit vergangen ist, seit der Einführung der Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d88a8-141">Activities after time has passed since rolling out Office 365 Cloud App Security</span></span>

<span data-ttu-id="d88a8-142">Wenn ein längeren Zeitraum verstrichen ursprünglich konfiguriert oder Ihre Office 365 Cloud App-Sicherheitsrichtlinien verwaltet, führen Sie die folgenden Schritte aus, um wieder zu einer Konfiguration abzurufen, die angezeigt, die Sicherheitsziele des Unternehmens und der aktuellen Funktionen der Office 365-Cloud-App-Sicherheit:</span><span class="sxs-lookup"><span data-stu-id="d88a8-142">If a protracted amount of time has passed since you initially configured or maintained your Office 365 Cloud App Security policies, take the following steps to get back to a configuration that reflects your organization's security goals and the current capabilities of Office 365 Cloud App Security:</span></span>
  
1. <span data-ttu-id="d88a8-143">Bestimmen Sie das Datum der letzten konfigurationsänderung für Office 365-Cloud-App-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="d88a8-143">Determine the date of the last configuration change for Office 365 Cloud App Security.</span></span>
    
2. <span data-ttu-id="d88a8-p104">Grundlegendes zu Ihrer aktuellen Konfiguration von Office 365-Cloud-App-Sicherheit, und passen Sie diese Richtlinien nach Bedarf. Stellen Sie beispielsweise sicher, dass Sie immer wissen, wo Benachrichtigungen per e-Mail gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="d88a8-p104">Understand your current Office 365 Cloud App Security configuration and adjust those policies as needed. For example, make sure you know where alerts are being sent via email.</span></span>
    
3. <span data-ttu-id="d88a8-146">Finden Sie unter [Was ist neu in Office 365-Cloud-App-Sicherheit](new-in-office-365-cas.md) für Produkt Änderungen, da Sie zuletzt über Office 365-Cloud-App-Sicherheit konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="d88a8-146">See [what's new in Office 365 Cloud App Security](new-in-office-365-cas.md) for product changes since you last configured Office 365 Cloud App Security.</span></span> 
    
4. <span data-ttu-id="d88a8-147">Durchführen einer Analyse der Office 365 Cloud App-Sicherheitswarnungen und Protokollen zur ins Auge fällt Bildschirmdarstellung auftreten und Trends analysieren.</span><span class="sxs-lookup"><span data-stu-id="d88a8-147">Perform an analysis of Office 365 Cloud App Security alerts and logs to spot anomalies and analyze trends.</span></span>
    
5. <span data-ttu-id="d88a8-148">Überprüfen Sie die Sicherheit im Internet Branchentrends sollten Sie die neuesten Sicherheitsrisiken vertraut.</span><span class="sxs-lookup"><span data-stu-id="d88a8-148">Check industry cybersecurity trends to become aware of the latest security threats.</span></span>
    
6. <span data-ttu-id="d88a8-p105">Führen Sie eine Analyse der Änderungen, die der aktuelle Satz von Office 365 Cloud App-Sicherheitsrichtlinien getroffen werden müssen. Integrieren von Office 365-Cloud-App-Sicherheit featureänderungen, aktuelle Bildschirmdarstellung auftreten und Sicherheit im Internet Trends. Empfehlen Sie Änderungen zu vorhandenen Richtlinien oder zum Erstellen eines neuen Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="d88a8-p105">Perform an analysis of the changes that need to be made to the current set of Office 365 Cloud App Security policies. Incorporate Office 365 Cloud App Security feature changes, current anomalies, and cybersecurity trends. Recommend changes to existing policies or the creation of new policies.</span></span>
    
7. <span data-ttu-id="d88a8-p106">Erstellen Sie einen Plan für die Implementierung der Richtlinie ändert. Kommunikation (Kontakte knüpfen) die Konsequenzen der vorgeschlagenen Änderungen an Ihre Endbenutzer nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="d88a8-p106">Make a plan for implementing the policy changes. Communicate (socialize) the consequences of the proposed changes with your end users as needed.</span></span>
    
8. <span data-ttu-id="d88a8-154">Implementieren Sie die Sicherheit in Office 365 Cloud App-Richtlinie ändert.</span><span class="sxs-lookup"><span data-stu-id="d88a8-154">Implement the Office 365 Cloud App Security policy changes.</span></span>
    
9. <span data-ttu-id="d88a8-155">Überwachen Sie der Endbenutzer Feedback und Office 365-Cloud-App-Sicherheit Benachrichtigungen, und passen Sie Richtlinien über einen Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="d88a8-155">Monitor end user feedback and Office 365 Cloud App Security alerts and adjust policies over time.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="d88a8-156">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d88a8-156">Next steps</span></span>

- [<span data-ttu-id="d88a8-157">Untersuchen Sie eine Aktivität</span><span class="sxs-lookup"><span data-stu-id="d88a8-157">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="d88a8-158">Anhalten oder Wiederherstellen eines Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="d88a8-158">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- [<span data-ttu-id="d88a8-159">Verwalten von app-Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="d88a8-159">Manage app permissions</span></span>](manage-app-permissions-in-ocas.md)
    
- [<span data-ttu-id="d88a8-160">Überprüfen der app Discovery Ergebnisse in Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="d88a8-160">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="d88a8-161">Anzeigen einer Liste mit unterstützten [Web Datenverkehr Protokolle und Datenquellen](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="d88a8-161">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    

