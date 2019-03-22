---
title: Automatisierte Untersuchung und Antwort (AIR) mit Office 365 Threat Intelligence
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 03/21/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Erfahren Sie mehr über automatisierte Ermittlungs-und Antwortfunktionen in Office 365 Advanced Threat Protection.
ms.openlocfilehash: c2d5acd0bf26dc28b30f26488adf47de2c834fb6
ms.sourcegitcommit: a56128c7be5d59e976851c27301031e19fa1997d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2019
ms.locfileid: "30736335"
---
# <a name="automated-investigation-and-response-air-with-office-365-threat-intelligence"></a><span data-ttu-id="73f6e-103">Automatisierte Untersuchung und Antwort (AIR) mit Office 365 Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="73f6e-103">Automated Investigation and Response (AIR) with Office 365 Threat Intelligence</span></span>

<span data-ttu-id="73f6e-104">Automatisierte Untersuchung und Antwort (AIR) (demnächst in [Office 365 Threat Investigation and Response Capabilities](office-365-ti.md)) ermöglicht es Ihnen, automatisierte Untersuchungen und Korrekturen zu bekannten Bedrohungen durchzuführen, die es heute gibt.</span><span class="sxs-lookup"><span data-stu-id="73f6e-104">Automated Investigation and Response (AIR) (coming soon to [Office 365 Threat investigation and response capabilities](office-365-ti.md)) enables you to run automated investigation and remediation to well-known threats that exist today.</span></span> <span data-ttu-id="73f6e-105">Lesen Sie diesen Artikel, um einen Überblick über die Luft zu erhalten und zu erfahren, wie Sie Ihr Unternehmen dabei unterstützen, Bedrohungen effektiver und effizienter zu verringern.</span><span class="sxs-lookup"><span data-stu-id="73f6e-105">Read this article to get an overview of AIR and how it can help your organization mitigate threats more effectively and efficiently.</span></span> <span data-ttu-id="73f6e-106">Weitere Informationen dazu, wann AIR verfügbar ist, finden Sie im [Microsoft 365-Fahrplan](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="73f6e-106">Tolearn more about when AIR will be available, see the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>

## <a name="alerts"></a><span data-ttu-id="73f6e-107">Warnungen</span><span class="sxs-lookup"><span data-stu-id="73f6e-107">Alerts</span></span>

<span data-ttu-id="73f6e-108">[Warnungen](alert-policies.md#viewing-alerts) stellen Auslöser für Sicherheitsoperationen-Team Workflows für Vorfalls Reaktionen dar.</span><span class="sxs-lookup"><span data-stu-id="73f6e-108">[Alerts](alert-policies.md#viewing-alerts) represent triggers for Security Operations team workflows for incident response.</span></span> <span data-ttu-id="73f6e-109">Das Priorisieren des richtigen Warnungs Satzes zur Untersuchung und sicherstellen, dass keine Bedrohungen unadressiert sind, ist eine Herausforderung.</span><span class="sxs-lookup"><span data-stu-id="73f6e-109">Prioritizing the right set of alerts for investigation while making sure no threats are unaddressed is challenging.</span></span> <span data-ttu-id="73f6e-110">Wenn Untersuchungen zu Warnungen manuell durchgeführt werden, müssen Sicherheits Betriebsteams Entitäten (z. b. Inhalte, Geräte und Benutzer), die von Bedrohungen bedroht sind, aufspüren und korrelieren.</span><span class="sxs-lookup"><span data-stu-id="73f6e-110">When investigations into alerts are performed manually, Security Operations teams must hunt and correlate entities (e.g. content, devices and users) at risk from threats.</span></span> <span data-ttu-id="73f6e-111">Solche Aufgaben und Workflows sind sehr zeitaufwändig und beinhalten mehrere Tools und Systeme.</span><span class="sxs-lookup"><span data-stu-id="73f6e-111">Such tasks and workflows are very time consuming and involve multiple tools and systems.</span></span> <span data-ttu-id="73f6e-112">Mit AIR werden Untersuchungen und Reaktionszeiten zu wichtigen Sicherheits-und Bedrohungs Verwaltungswarnungen automatisiert, die ihre Sicherheitsantwort-Manuskripte automatisch auslösen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-112">With AIR, investigation and response are automated into key security and threat management alerts that trigger your security response playbooks automatically.</span></span> 

<span data-ttu-id="73f6e-113">zum anzeigen von benachrichtigungen wählen sie im Office 365 Security & Compliance Center **alerts** > **anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="73f6e-113">To view alerts, in the Office 365 Security & Compliance Center, choose **Alerts** > **View alerts**.</span></span>

![Warnungen, die auf Untersuchungen verweisen](media/air-alerts-page-details.png) 

<span data-ttu-id="73f6e-115">Wählen Sie eine Warnung aus, um die Details anzuzeigen, und verwenden Sie dann den Link **untersuchUng anzeigen** , um zur entsprechenden [Untersuchung](#investigation-graph)zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="73f6e-115">Select an alert to view its details, and from there, use the **View investigation** link to go to the corresponding [investigation](#investigation-graph).</span></span>

## <a name="security-playbooks"></a><span data-ttu-id="73f6e-116">Sicherheits Manuskripte</span><span class="sxs-lookup"><span data-stu-id="73f6e-116">Security playbooks</span></span>

<span data-ttu-id="73f6e-117">Sicherheits Manuskripte sind Back-End-Richtlinien, die im Mittelpunkt der Automatisierung in Microsoft Threat Protection stehen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-117">Security playbooks are back-end policies that are at the heart of automation in Microsoft Threat Protection.</span></span> <span data-ttu-id="73f6e-118">Die in AIR bereitgestellten Sicherheits Manuskripte basieren auf allgemeinen Sicherheitsszenarien in der Praxis.</span><span class="sxs-lookup"><span data-stu-id="73f6e-118">The security playbooks provided in AIR are based on common real-world security scenarios.</span></span> <span data-ttu-id="73f6e-119">Ein Sicherheits Textbuch wird automatisch gestartet, wenn in Ihrer Organisation eine Warnung ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="73f6e-119">A security playbook is launched automatically when an alert is triggered within your organization.</span></span> <span data-ttu-id="73f6e-120">Sobald die Warnung ausgelöst wird, wird das zugehörige Textbuch automatisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73f6e-120">Once the alert triggers, the associated playbook is run automatically.</span></span> <span data-ttu-id="73f6e-121">Das Textbuch führt eine Untersuchung durch, untersucht alle zugehörigen Metadaten (einschließlich e-Mail-Nachrichten, Benutzer, betreffs, Absender usw.), und empfiehlt anhand der Ergebnisse eine Reihe von Aktionen, die das Sicherheitsteam Ihrer Organisation ausführen kann, um die Bedrohung.</span><span class="sxs-lookup"><span data-stu-id="73f6e-121">The playbook runs an investigation, looking at all the associated metadata (including email messages, users, subjects, senders, etc.) and, based on its findings, recommends a set of actions that your organization's security team can take to control and mitigate the threat.</span></span> 

<span data-ttu-id="73f6e-122">Die Sicherheits Manuskripte, die Sie mit AIR erhalten, wurden entwickelt, um die häufigsten Bedrohungen zu bewältigen, denen Organisationen heute gegenüberstehen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-122">The security playbooks you'll get with AIR are designed to tackle the most frequent threats that organizations face today.</span></span> <span data-ttu-id="73f6e-123">Sie basieren auf Eingaben aus Sicherheits-und Vorfall Reaktions Teams, einschließlich derer, die bei der Verteidigung von Microsoft-Objekten helfen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-123">They're based on input from Security Operations and Incident Response teams, including those who help defend Microsoft assets.</span></span>

### <a name="security-playbooks-are-rolling-out-in-phases"></a><span data-ttu-id="73f6e-124">Sicherheits Manuskripte werden phasenweise ausgeführt</span><span class="sxs-lookup"><span data-stu-id="73f6e-124">Security playbooks are rolling out in phases</span></span>

<span data-ttu-id="73f6e-125">Als Teil von AIR werden Sicherheits Manuskripte phasenweise ausgeführt</span><span class="sxs-lookup"><span data-stu-id="73f6e-125">As part of AIR, security playbooks are rolling out in phases</span></span>

- <span data-ttu-id="73f6e-126">**Phase 1 (April 2019)**: Manuskripte bieten Empfehlungen, die Sicherheitsadministratoren überarbeiten und genehmigen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-126">**Phase 1 (April 2019)**: Playbooks include recommendations that security administrators review and approve.</span></span> 

- <span data-ttu-id="73f6e-127">**Phase 2 (juni 2019)**: Sicherheitsadministratoren haben die Möglichkeit, Sicherheits-Textbuch zu ermöglichen, automatisch Maßnahmen ohne administrative Interaktion zu ergreifen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-127">**Phase 2 (June 2019)**: Security administrators will have the option to allow security playbooks to take action automatically, without administrative interaction.</span></span>

<span data-ttu-id="73f6e-128">Phase 1 umfasst die folgenden Manuskripte:</span><span class="sxs-lookup"><span data-stu-id="73f6e-128">Phase 1 will include the following playbooks:</span></span>
- <span data-ttu-id="73f6e-129">Vom Benutzer gemeldete Phishing-Nachricht</span><span class="sxs-lookup"><span data-stu-id="73f6e-129">User-reported phish message</span></span>
- <span data-ttu-id="73f6e-130">URL Klick Urteil ändern und ATP Safe Links Block außer Kraft setzen</span><span class="sxs-lookup"><span data-stu-id="73f6e-130">URL click verdict change and ATP Safe Links block override</span></span>
- <span data-ttu-id="73f6e-131">Malware ZAP</span><span class="sxs-lookup"><span data-stu-id="73f6e-131">Malware ZAP</span></span>
- <span data-ttu-id="73f6e-132">Phishing ZAP</span><span class="sxs-lookup"><span data-stu-id="73f6e-132">Phish ZAP</span></span>
- <span data-ttu-id="73f6e-133">Manuelle Untersuchungen (mit Explorer)</span><span class="sxs-lookup"><span data-stu-id="73f6e-133">Manual investigations (using Explorer)</span></span>

<span data-ttu-id="73f6e-134">Für Phase 2 sind mehrere Manuskripte geplant.</span><span class="sxs-lookup"><span data-stu-id="73f6e-134">Several more playbooks are planned for Phase 2.</span></span>

### <a name="playbooks-include-investigation-and-recommendations"></a><span data-ttu-id="73f6e-135">Manuskripte schließen Untersuchungen und Empfehlungen ein</span><span class="sxs-lookup"><span data-stu-id="73f6e-135">Playbooks include investigation and recommendations</span></span>

<span data-ttu-id="73f6e-136">Jedes Textbuch umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="73f6e-136">Each playbook includes:</span></span> 
- <span data-ttu-id="73f6e-137">eine Stamm Ermittlung,</span><span class="sxs-lookup"><span data-stu-id="73f6e-137">a root investigation,</span></span> 
- <span data-ttu-id="73f6e-138">Schritte zum Aufspüren anderer potenzieller Bedrohungen und</span><span class="sxs-lookup"><span data-stu-id="73f6e-138">steps to hunt down other potential threats, and</span></span> 
- <span data-ttu-id="73f6e-139">Empfohlene Bedrohungs Korrektur.</span><span class="sxs-lookup"><span data-stu-id="73f6e-139">recommended threat remediation.</span></span>

<span data-ttu-id="73f6e-140">Jeder allgemeine Schritt enthält viele unter Schritte, die ausgeführt werden, um eine umfassende, detaillierte und umfassende Antwort auf Bedrohungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-140">Each high-level step includes many sub-steps that are executed to provide a deep, detailed, and exhaustive response to threats.</span></span>

## <a name="example-user-reported-phish-message"></a><span data-ttu-id="73f6e-141">Beispiel: vom Benutzer gemeldete Phishing-Nachricht</span><span class="sxs-lookup"><span data-stu-id="73f6e-141">Example: User-reported phish message</span></span>

<span data-ttu-id="73f6e-142">Wenn ein Benutzer in Ihrer Organisation eine e-Mail-Nachricht sendet und ihn über das [Add-in Berichtnachricht für Outlook oder Outlook Web Access](enable-the-report-message-add-in.md)an Microsoft meldet.</span><span class="sxs-lookup"><span data-stu-id="73f6e-142">When a user in your organization submits an email message and reports it to Microsoft by using the [Report Message add-in for Outlook or Outlook Web Access](enable-the-report-message-add-in.md).</span></span> <span data-ttu-id="73f6e-143">Dies löst eine System basierte Informationswarnung aus, die das Ermittlungs Manuskript automatisch startet.</span><span class="sxs-lookup"><span data-stu-id="73f6e-143">This triggers a system-based informational alert that automatically launches the investigation playbook.</span></span>

<span data-ttu-id="73f6e-144">Während der Stamm Untersuchung werden verschiedene Aspekte der e-Mail ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="73f6e-144">During the root investigation phase, various aspects of the email are assessed.</span></span> <span data-ttu-id="73f6e-145">Zu diesen zählen:</span><span class="sxs-lookup"><span data-stu-id="73f6e-145">These include:</span></span>
- <span data-ttu-id="73f6e-146">Eine Bestimmung darüber, welche Art von Bedrohung es sein könnte;</span><span class="sxs-lookup"><span data-stu-id="73f6e-146">A determination about what type of threat it might be;</span></span>
- <span data-ttu-id="73f6e-147">Wer hat Sie gesendet?</span><span class="sxs-lookup"><span data-stu-id="73f6e-147">Who sent it;</span></span>
- <span data-ttu-id="73f6e-148">Absender der e-Mail (Sendeinfrastruktur)</span><span class="sxs-lookup"><span data-stu-id="73f6e-148">Where the email was sent from (sending infrastructure);</span></span>
- <span data-ttu-id="73f6e-149">Ob andere Instanzen der e-Mail zugestellt oder blockiert wurden;</span><span class="sxs-lookup"><span data-stu-id="73f6e-149">Whether other instances of the email were delivered or blocked;</span></span>
- <span data-ttu-id="73f6e-150">Eine Bewertung durch unsere Analysten;</span><span class="sxs-lookup"><span data-stu-id="73f6e-150">An assessment from our analysts;</span></span>
- <span data-ttu-id="73f6e-151">Gibt an, ob die e-Mail bekannten Kampagnen zugeordnet ist;</span><span class="sxs-lookup"><span data-stu-id="73f6e-151">Whether the email is associated with any known campaigns;</span></span>
- <span data-ttu-id="73f6e-152">und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="73f6e-152">and more.</span></span>

<span data-ttu-id="73f6e-153">Nach Abschluss der Stamm Ermittlung enthält das Textbuch eine Liste der empfohlenen Aktionen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-153">After the root investigation is complete, the playbook provides a list of recommended actions to take.</span></span>
  
<span data-ttu-id="73f6e-154">Als nächstes werden mehrere Jagd Schritte ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="73f6e-154">Next, several hunting steps are executed:</span></span>

- <span data-ttu-id="73f6e-155">Ähnliche e-Mails in anderen e-Mail-Clustern werden durchsucht.</span><span class="sxs-lookup"><span data-stu-id="73f6e-155">Similar email messages in other email clusters are searched.</span></span>
- <span data-ttu-id="73f6e-156">Das Signal wird für andere Plattformen wie [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection)freigegeben.</span><span class="sxs-lookup"><span data-stu-id="73f6e-156">The signal is shared with other platforms, such as [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection).</span></span>
- <span data-ttu-id="73f6e-157">Es wird festgelegt, ob Benutzer auf die verdächtige e-Mail-Nachricht geklickt haben.</span><span class="sxs-lookup"><span data-stu-id="73f6e-157">A determination is made on whether any users have clicked through on the suspicious email message.</span></span>
- <span data-ttu-id="73f6e-158">Eine Überprüfung erfolgt in Office 365 [EoP](eop/exchange-online-protection-eop.md) und [ATP](office-365-atp.md) , um festzustellen, ob andere ähnliche Nachrichten von Benutzern gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-158">A check is done across Office 365 [EOP](eop/exchange-online-protection-eop.md) and [ATP](office-365-atp.md) to see if there are any other similar messages reported by users.</span></span>
- <span data-ttu-id="73f6e-159">Es wird überprüft, ob ein Benutzer kompromittiert wurde.</span><span class="sxs-lookup"><span data-stu-id="73f6e-159">A check is done to see if a user has been compromised.</span></span> <span data-ttu-id="73f6e-160">Diese Überprüfung nutzt Signale in [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) und [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), korreliert alle zugehörigen Ereignisse oder Warnungen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-160">This check leverages signals across [Microsoft Cloud App Security](https://docs.microsoft.com/cloud-app-security) and [Azure Active Directory](https://docs.microsoft.com/azure/active-directory), correlating any related events or alerts.</span></span> 

<span data-ttu-id="73f6e-161">Während der Jagd Phase werden Risiken und Bedrohungen verschiedenen Jagd Stufen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="73f6e-161">During the hunting phase, risks and threats are assigned to various hunting steps.</span></span>  

<span data-ttu-id="73f6e-162">Sanierung ist die letzte Phase des Manuskripts.</span><span class="sxs-lookup"><span data-stu-id="73f6e-162">Remediation is the final phase of the playbook.</span></span> <span data-ttu-id="73f6e-163">Während dieser Phase werden Behebungsschritte auf der Grundlage von theinvestigation-und-Jagd Phasen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73f6e-163">During this phase, remediation steps are taken, based on theinvestigation and hunting phases.</span></span>  

## <a name="getting-started"></a><span data-ttu-id="73f6e-164">Erste Schritte</span><span class="sxs-lookup"><span data-stu-id="73f6e-164">Getting started</span></span>

<span data-ttu-id="73f6e-165">Um auf ihre Untersuchungen zuzugreifen, wechseln Sie als globaler Office 365-Administrator oder Sicherheitsadministrator zum Office 365 Security &[https://protection.office.com](https://protection.office.com)Compliance Center (), und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="73f6e-165">To access your investigations, as an Office 365 global administrator or security administrator, Go to the Office 365 Security & Compliance Center ([https://protection.office.com](https://protection.office.com)) and sign in.</span></span> <span data-ttu-id="73f6e-166">Führen Sie dann einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="73f6e-166">Then, do one of the following:</span></span>

- <span data-ttu-id="73f6e-167">Navigieren Sie im linken Navigationsbereich zu **Threat Management** > **Investigations**.</span><span class="sxs-lookup"><span data-stu-id="73f6e-167">In the left navigation, go to **Threat management** > **Investigations**.</span></span>

    <span data-ttu-id="73f6e-168">oder</span><span class="sxs-lookup"><span data-stu-id="73f6e-168">or</span></span>

- <span data-ttu-id="73f6e-169">Besuchen Sie das Threat Management Dashboard (im Security & Compliance Center, navigieren Sie zu **Threat Management** > **Dashboard**).</span><span class="sxs-lookup"><span data-stu-id="73f6e-169">Visit the Threat management dashboard (In the Security & Compliance Center, go to **Threat management** > **Dashboard**).</span></span>

![AIR-Widgets](media/air-widgets.png)

<span data-ttu-id="73f6e-171">Ihre AIR-Widgets werden am oberen Rand des [Sicherheits Dashboards](security-dashboard.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73f6e-171">Your AIR widgets will appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="73f6e-172">Wählen Sie ein Widget aus, um loszulegen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-172">Select a widget to get started.</span></span>

### <a name="automated-investigations"></a><span data-ttu-id="73f6e-173">Automatisierte Untersuchungen</span><span class="sxs-lookup"><span data-stu-id="73f6e-173">Automated investigations</span></span>

<span data-ttu-id="73f6e-174">Auf der Seite automatisierte Untersuchungen werden die Ermittlungen Ihrer Organisation und ihre aktuellen Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73f6e-174">The automated investigations page shows your organization's investigations and their current states.</span></span>

![Haupt Untersuchungs Seite für Luft](media/air-maininvestigationpage.png) 
  
<span data-ttu-id="73f6e-176">Sie können:</span><span class="sxs-lookup"><span data-stu-id="73f6e-176">You can:</span></span>
- <span data-ttu-id="73f6e-177">Navigieren Sie direkt zu einer Untersuchung (Wählen Sie eine **ERMITTLUNGS-ID**aus).</span><span class="sxs-lookup"><span data-stu-id="73f6e-177">Navigate directly to an investigation (select an **Investigation ID**).</span></span>
- <span data-ttu-id="73f6e-178">Anwenden von Filtern</span><span class="sxs-lookup"><span data-stu-id="73f6e-178">Apply filters.</span></span> <span data-ttu-id="73f6e-179">Wählen Sie **unter**Untersuchungs, **Zeitspanne**, **Status**oder eine Kombination aus.</span><span class="sxs-lookup"><span data-stu-id="73f6e-179">Choose from **Investigation Type**, **Time range**, **Status**, or a combination of these.</span></span>
- <span data-ttu-id="73f6e-180">Exportieren Sie die Daten in eine CSV-Datei.</span><span class="sxs-lookup"><span data-stu-id="73f6e-180">Export the data to a CSV file.</span></span>

### <a name="investigation-graph"></a><span data-ttu-id="73f6e-181">Untersuchung Graph</span><span class="sxs-lookup"><span data-stu-id="73f6e-181">Investigation graph</span></span>

<span data-ttu-id="73f6e-182">Wenn Sie eine bestimmte Untersuchung öffnen, wird die Seite Untersuchungs Graph angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73f6e-182">When you open a specific investigation, you see the investigation graph page.</span></span> <span data-ttu-id="73f6e-183">Auf dieser Seite werden alle Entitäten angezeigt: e-Mail-Nachrichten, Benutzer (und ihre Aktivitäten) und Geräte, die als Teil der ausgelösten Warnung automatisch untersuchtwurden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-183">This page shows all the different entities: email messages, users (and their activities), and devices that were automatically investigated as part of the alert that was triggered.</span></span>

![Seite "AIR Investigation Graph"](media/air-investigationgraphpage.png)

<span data-ttu-id="73f6e-185">Sie können:</span><span class="sxs-lookup"><span data-stu-id="73f6e-185">You can:</span></span>
- <span data-ttu-id="73f6e-186">Erhalten Sie einen visuellen Überblick über die aktuelle Untersuchung.</span><span class="sxs-lookup"><span data-stu-id="73f6e-186">Get a visual overview of the current investigation.</span></span>
- <span data-ttu-id="73f6e-187">Zeigen Sie eine Zusammenfassung der Untersuchungen an.</span><span class="sxs-lookup"><span data-stu-id="73f6e-187">View a summary of the investigation timings.</span></span>
- <span data-ttu-id="73f6e-188">Wählen Sie einen Knoten in der Visualisierung aus, um Details für diesen Knoten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-188">Select a node in the visualization to view details for that node.</span></span>
- <span data-ttu-id="73f6e-189">Wählen Sie oben eine Registerkarte aus, um Details für diese Registerkarte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-189">Select a tab across the top to view details for that tab.</span></span>

### <a name="alert-investigation"></a><span data-ttu-id="73f6e-190">Warnungs Ermittlung</span><span class="sxs-lookup"><span data-stu-id="73f6e-190">Alert investigation</span></span>

<span data-ttu-id="73f6e-191">Auf der Registerkarte **Benachrichtigungen** für eine Untersuchung werden alle für die Untersuchung relevanten Warnungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="73f6e-191">On the **Alerts** tab for an investigation, you can see all of the alerts relevant to the investigation.</span></span> <span data-ttu-id="73f6e-192">Details sind die Warnung, die die Untersuchung ausgelöst hat, sowie andere Warnungen, wie beispielsweise riskante Anmeldungen, Massendownloads usw., die mit der Untersuchung in Beziehung stehen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-192">Details include the alert that triggered the investigation and other alerts, such as risky sign-in, mass download, etc., that are correlated to the investigation.</span></span> <span data-ttu-id="73f6e-193">Auf dieser Seite kann ein Sicherheitsanalytiker auch zusätzliche Details zu einzelnen Warnungen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-193">From this page, a security analyst can also view additional details on individual alerts.</span></span>

![Seite "Luft Warnungen"](media/air-investigationalertspage.png)

<span data-ttu-id="73f6e-195">Sie können:</span><span class="sxs-lookup"><span data-stu-id="73f6e-195">You can:</span></span>
- <span data-ttu-id="73f6e-196">Erhalten Sie eine visuelle Übersicht über die aktuelle Auslöse Warnung und alle zugehörigen Warnungen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-196">Get a visual overview of the current triggering alert and any associated alerts.</span></span>
- <span data-ttu-id="73f6e-197">Wählen Sie in der Liste eine Warnung aus, um eine Fly-Out-Seite mit vollständigen Warnungsdetails zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-197">Select an alert in the list to open a fly-out page that shows full alert details.</span></span>

### <a name="email-investigation"></a><span data-ttu-id="73f6e-198">E-Mail-Untersuchung</span><span class="sxs-lookup"><span data-stu-id="73f6e-198">Email investigation</span></span>

<span data-ttu-id="73f6e-199">Auf der Registerkarte **e-Mail-Nachricht** für eine Untersuchung werden alle e-Mail-Cluster angezeigt, die im Rahmen der Untersuchung identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-199">On the **Email** tab for an investigation, you can see all the email clusters identified as part of the investigation.</span></span> 

<span data-ttu-id="73f6e-200">Angesichts der schieren Menge an e-Mails, die Benutzer in einer Organisation senden und empfangen, wird der Prozess der</span><span class="sxs-lookup"><span data-stu-id="73f6e-200">Given the sheer volume of email that users in an organization send and receive, the process of</span></span> 
- <span data-ttu-id="73f6e-201">Gruppieren von e-Mail-Nachrichten basierend auf ähnlichen Attributen aus einem Nachrichtenkopf, einem Text, einer URL und einer Anlage</span><span class="sxs-lookup"><span data-stu-id="73f6e-201">clustering email messages based on similar attributes from a message header, body, URL and attachment;</span></span> 
- <span data-ttu-id="73f6e-202">Trennen von böswilligen e-Mails von der guten e-Mail; und</span><span class="sxs-lookup"><span data-stu-id="73f6e-202">separating malicious email from the good email; and</span></span> 
- <span data-ttu-id="73f6e-203">Ausführen von Aktionen für böswillige e-Mail-Nachrichten</span><span class="sxs-lookup"><span data-stu-id="73f6e-203">taking action on malicious email messages</span></span> 

<span data-ttu-id="73f6e-204">kann viele Stunden in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-204">can take many hours.</span></span> <span data-ttu-id="73f6e-205">Mit AIR wird dieser Prozess automatisiert, und das Sicherheitsteam des Unternehmens spart Zeit und Aufwand.</span><span class="sxs-lookup"><span data-stu-id="73f6e-205">AIR now automates this process, saving your organization's security team time and effort.</span></span> 

<span data-ttu-id="73f6e-206">Betrachten Sie als Beispiel die folgende Abbildung.</span><span class="sxs-lookup"><span data-stu-id="73f6e-206">As an example, consider the following image.</span></span> <span data-ttu-id="73f6e-207">Der erste Cluster von drei e-Mail-Nachrichten wurde als Phishing eingestuft.</span><span class="sxs-lookup"><span data-stu-id="73f6e-207">The first cluster of three email messages were deemed to be phish.</span></span> <span data-ttu-id="73f6e-208">Es wurde ein weiterer Cluster ähnlicher Nachrichten mit derselben IP-Adresse und einem anderen Betreff gefunden, der als bösartig eingestuft wurde, da einige von Ihnen bei der Ersterkennung als Phishing identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-208">Another cluster of similar messages with the same IP and subject was found and is considered to be malicious, as some of them were identified as phish during initial detection.</span></span> 

![Seite zur Untersuchung der Luft e-Mail](media/air-investigationemailpage.png)

<span data-ttu-id="73f6e-210">Sie können:</span><span class="sxs-lookup"><span data-stu-id="73f6e-210">You can:</span></span>
- <span data-ttu-id="73f6e-211">Erhalten Sie eine visuelle Übersicht über die aktuellen Cluster Ergebnisse und Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-211">Get a visual overview of the current clustering results and threats found.</span></span>
- <span data-ttu-id="73f6e-212">Klicken Sie auf eine Cluster Entität oder eine Bedrohungsliste, um eine Fly-Out-Seite zu öffnen, auf der die vollständigen Warnungsdetails angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-212">Click a cluster entity or a threat list to open a fly-out page that shows the full alert details.</span></span>

![Untersuchung per e-Mail mit Flyout-Details](media/air-investigationemailpageflyoutdetails.png)

### <a name="user-investigation"></a><span data-ttu-id="73f6e-214">Benutzer Ermittlung</span><span class="sxs-lookup"><span data-stu-id="73f6e-214">User investigation</span></span>

<span data-ttu-id="73f6e-215">Auf der Registerkarte **Benutzer** werden alle Benutzer angezeigt, die im Rahmen der Untersuchung identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-215">On the **Users** tab, you can see all the users identified as part of the investigation.</span></span> 

<span data-ttu-id="73f6e-216">In der folgenden Abbildung hat AIR beispielsweise Indikatoren für Kompromisse und Anomalien basierend auf einer neuen Posteingangsregel ermittelt, die erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="73f6e-216">For example, in the following image, AIR has identified indicators of compromise and anomalies based on a new inbox rule that was created.</span></span> <span data-ttu-id="73f6e-217">Weitere Details (Evidence) der Untersuchung sind über detaillierte Ansichten auf dieser Registerkarte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="73f6e-217">Additional details (evidence) of the investigation are available through detailed views within this tab.</span></span>

![Seite "Luft Ermittlungs Benutzer"](media/air-investigationuserspage.png)

<span data-ttu-id="73f6e-219">Sie können:</span><span class="sxs-lookup"><span data-stu-id="73f6e-219">You can:</span></span>
- <span data-ttu-id="73f6e-220">Erhalten Sie eine visuelle Übersicht über die identifizierten Benutzer Ergebnisse und Risiken.</span><span class="sxs-lookup"><span data-stu-id="73f6e-220">Get a visual overview of identified user results and risks found.</span></span>
- <span data-ttu-id="73f6e-221">Wählen Sie einen Benutzer aus, um eine Fly-Out-Seite mit den vollständigen Warnungsdetails zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-221">Select a user to open a fly-out page that shows the full alert details.</span></span>

### <a name="machine-investigation"></a><span data-ttu-id="73f6e-222">Computeruntersuchungen</span><span class="sxs-lookup"><span data-stu-id="73f6e-222">Machine investigation</span></span>

<span data-ttu-id="73f6e-223">Auf der Registerkarte **Computer** werden alle Computer angezeigt, die im Rahmen der Untersuchung identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-223">On the **Machines** tab, you can see all the machines identified as part of the investigation.</span></span> 

![Seite "Luft Untersuchungsgerät"](media/air-investigationmachinepage.png)

<span data-ttu-id="73f6e-225">Im Rahmen der Untersuchung korreliert AIR e-Mail-Bedrohungen mit Geräten.</span><span class="sxs-lookup"><span data-stu-id="73f6e-225">As part of the investigation, AIR correlates email threats to devices.</span></span> <span data-ttu-id="73f6e-226">Eine Untersuchung übergibt beispielsweise einen Dateihash an [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) , um zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-226">For example, an investigation passes a file hash across to [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/windows-defender-advanced-threat-protection) to investigate.</span></span> <span data-ttu-id="73f6e-227">Dies ermöglicht eine automatisierte Untersuchung der relevanten Computer für Ihre Benutzer und hilft dabei, sicherzustellen, dass Bedrohungen sowohl in der Cloud als auch über Ihre Geräte adressiert werden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-227">This allows for automated investigation of relevant machines for your users and helps to ensure that threats are addressed both in the cloud and across your devices.</span></span> 

<span data-ttu-id="73f6e-228">Sie können:</span><span class="sxs-lookup"><span data-stu-id="73f6e-228">You can:</span></span>
- <span data-ttu-id="73f6e-229">Erhalten Sie eine visuelle Übersicht über die aktuellen Computer und Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-229">Get a visual overview of the current machines and threats found.</span></span>
- <span data-ttu-id="73f6e-230">Wählen Sie einen Computer aus, um eine Ansicht zu öffnen, die in die zugehörigen [Windows Defender ATP](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection)-Untersuchungen eingeht.</span><span class="sxs-lookup"><span data-stu-id="73f6e-230">Select a machine to open a view that into the related [Windows Defender ATP investigations](https://docs.microsoft.com/windows/security/threat-protection/windows-defender-atp/automated-investigations-windows-defender-advanced-threat-protection).</span></span>

### <a name="entity-investigation"></a><span data-ttu-id="73f6e-231">Entitäts Untersuchung</span><span class="sxs-lookup"><span data-stu-id="73f6e-231">Entity investigation</span></span>

<span data-ttu-id="73f6e-232">Auf der Registerkarte **Entitäten** werden alle Computer angezeigt, die im Rahmen der Untersuchung identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-232">On the **Entities** tab, you can see all the machines identified as part of the investigation.</span></span> 

<span data-ttu-id="73f6e-233">Hier sehen Sie die untersuchten Entitäten.</span><span class="sxs-lookup"><span data-stu-id="73f6e-233">Here, you can see the investigated entities.</span></span> <span data-ttu-id="73f6e-234">Sie können Details der Entitätstypen wie e-Mail-Nachrichten, Cluster, IP-Adressen, Benutzer und vieles mehr anzeigen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-234">You can see details of the types of entities, such as email messages, clusters, IP addresses, users, and more.</span></span> <span data-ttu-id="73f6e-235">Sie können auch sehen, wie viele Entitäten analysiert wurden und welche Bedrohungen jeweils zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-235">You can also see how many entities were analyzed, and the threats that were associated with each.</span></span> 

![Seite "AIR Investigation Entities"](media/air-investigationentitiespage.png)

<span data-ttu-id="73f6e-237">Sie können:</span><span class="sxs-lookup"><span data-stu-id="73f6e-237">You can:</span></span>
- <span data-ttu-id="73f6e-238">Erhalten Sie eine visuelle Übersicht über die gefundenen Ermittlungs Entitäten und-Bedrohungen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-238">Get a visual overview of the investigation entities and threats found.</span></span>
- <span data-ttu-id="73f6e-239">Wählen Sie eine Entität aus, um eine Fly-Out-Seite zu öffnen, die die Details der zugehörigen Entität anzeigt.</span><span class="sxs-lookup"><span data-stu-id="73f6e-239">Select an entity to open a fly-out page that shows the related entity detail.</span></span>

![Details zu AIR Investigation Entities](media/air-investigationsentitiespagedetails.png)

### <a name="playbook-log"></a><span data-ttu-id="73f6e-241">Textbuch-Protokoll</span><span class="sxs-lookup"><span data-stu-id="73f6e-241">Playbook log</span></span>

<span data-ttu-id="73f6e-242">Auf der Registerkarte **Protokoll** werden alle Schritte für das Textbuch angezeigt, die während der Untersuchung aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="73f6e-242">On the **Log** tab, you can see all the playbook steps that have occurred during the investigation.</span></span> <span data-ttu-id="73f6e-243">Das Protokoll erfasst eine vollständige Bestandsaufnahme aller Aktionen, die von Office 365 Threat Intelligence-Funktionen als Teil von AIR ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-243">The log captures a complete inventory of all actions completed by Office 365 Threat Intelligence capabilities as part of AIR.</span></span> <span data-ttu-id="73f6e-244">Es bietet eine übersichtliche Ansicht aller Schritte, einschließlich der Aktion selbst, einer Beschreibung und der Dauer des aktuellen vom Anfang bis zum Ende.</span><span class="sxs-lookup"><span data-stu-id="73f6e-244">It provides a clear view of all the steps taken, including the Action itself, a description and the duration of the actual from start to finish.</span></span> 

![Seite "AIR Investigation log"](media/air-investigationlogpage.png)

<span data-ttu-id="73f6e-246">Sie können:</span><span class="sxs-lookup"><span data-stu-id="73f6e-246">You can:</span></span>
- <span data-ttu-id="73f6e-247">Sehen Sie sich eine visuelle Übersicht über die Schritte des Manuskripts an.</span><span class="sxs-lookup"><span data-stu-id="73f6e-247">Get see a visual overview of the playbook steps taken.</span></span>
- <span data-ttu-id="73f6e-248">Exportieren Sie die Ergebnisse in eine CSV-Datei.</span><span class="sxs-lookup"><span data-stu-id="73f6e-248">Export the results to a CSV file.</span></span>
- <span data-ttu-id="73f6e-249">Filtern Sie die Ansicht.</span><span class="sxs-lookup"><span data-stu-id="73f6e-249">Filter the view.</span></span>

### <a name="recommended-actions"></a><span data-ttu-id="73f6e-250">Empfohlene Aktionen</span><span class="sxs-lookup"><span data-stu-id="73f6e-250">Recommended actions</span></span>

<span data-ttu-id="73f6e-251">Auf der Registerkarte **Aktionen** werden alle Text Handlung-Aktionen angezeigt, die nach Abschluss der Untersuchung zur Korrektur empfohlen werden.</span><span class="sxs-lookup"><span data-stu-id="73f6e-251">On the **Actions** tab, you can see all the playbook actions that are recommended for remediation after the investigation has completed.</span></span> 

<span data-ttu-id="73f6e-252">Aktionen erfassen eine vollständige Liste aller Schritte, die Microsoft am Ende einer Untersuchung empfiehlt.</span><span class="sxs-lookup"><span data-stu-id="73f6e-252">Actions capture a complete list of all the steps Microsoft recommends you take at the end of a investigation.</span></span> <span data-ttu-id="73f6e-253">Sie können Korrekturaktionen durchführen, indem Sie eine oder mehrere Aktionen auswählen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-253">You can take remediation actions here by selecting one or more actions.</span></span> <span data-ttu-id="73f6e-254">Wenn \*\*\*\* Sie auf Genehmigen klicken, kann die Korrektur beginnen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-254">Clicking **Approve** will allow remediation to begin.</span></span> <span data-ttu-id="73f6e-255">(Möglicherweise sind entsprechende Berechtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="73f6e-255">(Appropriate permissions might be required.</span></span> <span data-ttu-id="73f6e-256">Beispielsweise kann ein Sicherheits Lesegerät Aktionen anzeigen, aber nicht genehmigen.)</span><span class="sxs-lookup"><span data-stu-id="73f6e-256">For example, a Security Reader can view actions but not approve them.)</span></span>  

![Seite "AIR Investigations Action"](media/air-investigationactionspage.png)

<span data-ttu-id="73f6e-258">Sie können:</span><span class="sxs-lookup"><span data-stu-id="73f6e-258">You can:</span></span>
- <span data-ttu-id="73f6e-259">Erhalten Sie eine visuelle Übersicht über die vom Textbuch empfohlenen Aktionen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-259">Get a visual overview of the playbook-recommended actions.</span></span>
- <span data-ttu-id="73f6e-260">Wählen Sie eine einzelne Aktion oder mehrere Aktionen aus.</span><span class="sxs-lookup"><span data-stu-id="73f6e-260">Select a single action or multiple actions.</span></span>
- <span data-ttu-id="73f6e-261">Genehmigen empfohlener Aktionen.</span><span class="sxs-lookup"><span data-stu-id="73f6e-261">Approve recommended actions.</span></span> <span data-ttu-id="73f6e-262">(Diese werden sofort mit Kommentaren gestartet.)</span><span class="sxs-lookup"><span data-stu-id="73f6e-262">(These are started immediately with comments.)</span></span>
- <span data-ttu-id="73f6e-263">Exportieren Sie die Ergebnisse in eine CSV-Datei.</span><span class="sxs-lookup"><span data-stu-id="73f6e-263">Export the results to a CSV file.</span></span>
- <span data-ttu-id="73f6e-264">Filtern Sie die Ansicht.</span><span class="sxs-lookup"><span data-stu-id="73f6e-264">Filter the view.</span></span>

## <a name="how-to-get-air"></a><span data-ttu-id="73f6e-265">So erhalten Sie AIR</span><span class="sxs-lookup"><span data-stu-id="73f6e-265">How to get AIR</span></span>

<span data-ttu-id="73f6e-266">Derzeit ist AIR in der Vorschau.</span><span class="sxs-lookup"><span data-stu-id="73f6e-266">Currently, AIR is in preview.</span></span> <span data-ttu-id="73f6e-267">Bei der Veröffentlichung wird AIR in die folgenden Abonnements aufgenommen:</span><span class="sxs-lookup"><span data-stu-id="73f6e-267">When released, AIR will be included in the following subscriptions:</span></span>

- <span data-ttu-id="73f6e-268">Microsoft 365 Enterprise E5</span><span class="sxs-lookup"><span data-stu-id="73f6e-268">Microsoft 365 Enterprise E5</span></span>
- <span data-ttu-id="73f6e-269">Office 365 Enterprise E5</span><span class="sxs-lookup"><span data-stu-id="73f6e-269">Office 365 Enterprise E5</span></span>
- <span data-ttu-id="73f6e-270">Microsoft Threat Protection</span><span class="sxs-lookup"><span data-stu-id="73f6e-270">Microsoft Threat Protection</span></span>
- <span data-ttu-id="73f6e-271">Office 365 Advanced Threat Protection-Plan 2</span><span class="sxs-lookup"><span data-stu-id="73f6e-271">Office 365 Advanced Threat Protection Plan 2</span></span>

<span data-ttu-id="73f6e-272">Weitere Informationen zur Verfügbarkeit von Funktionen finden Sie in der [Microsoft 365-Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span><span class="sxs-lookup"><span data-stu-id="73f6e-272">To learn more about feature availability, visit the [Microsoft 365 Roadmap](https://www.microsoft.com/microsoft-365/roadmap).</span></span>
