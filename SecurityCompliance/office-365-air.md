---
title: Automatisches untersuchen und reagieren auf Bedrohungen in Office 365
keywords: Luft, autoIR, ATP, automatisiert, Untersuchung, Antwort, Behebung, Bedrohungen, erweitert, Bedrohung, Schutz
ms.author: deniseb
author: denisebmsft
manager: dansimp
ms.date: 09/04/2019
audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.collection: M365-security-compliance
description: Erste Schritte mit automatisierten Ermittlungs-und Antwortfunktionen in Office 365 Advanced Threat Protection-Plan 2.
ms.openlocfilehash: 2c64ea936170524811839db7c593d67bfe11a928
ms.sourcegitcommit: 4a2bde56178609e75c1ad7ecad2db5e049fc0c45
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/05/2019
ms.locfileid: "36762023"
---
# <a name="automatically-investigate-and-respond-to-threats-in-office-365"></a><span data-ttu-id="ee01c-104">Automatisches untersuchen und reagieren auf Bedrohungen in Office 365</span><span class="sxs-lookup"><span data-stu-id="ee01c-104">Automatically investigate and respond to threats in Office 365</span></span>

## <a name="overview"></a><span data-ttu-id="ee01c-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="ee01c-105">Overview</span></span>

<span data-ttu-id="ee01c-106">[Office 365 Advanced Threat Protection](office-365-atp.md) Plan 2 enthält automatisierte Ermittlungs-und Antwortfunktionen (Air), mit denen Sie die Zeit und den Aufwand für Sicherheitsvorgänge im Umgang mit Warnungen und Bedrohungen speichern können.</span><span class="sxs-lookup"><span data-stu-id="ee01c-106">[Office 365 Advanced Threat Protection](office-365-atp.md) Plan 2 includes automated investigation and response (AIR) capabilities that can save your security operations team time and effort in dealing with alerts and threats.</span></span> <span data-ttu-id="ee01c-107">Lesen Sie diesen Artikel, um mit der Verwendung von Air-Funktionen in Office 365 zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="ee01c-107">Read this article to get started using AIR capabilities in Office 365.</span></span> <span data-ttu-id="ee01c-108">Weitere Informationen zur Funktionsweise von Air finden Sie unter [Automatische Untersuchung und Antwort (Air) mit Office 365](automated-investigation-response-office.md).</span><span class="sxs-lookup"><span data-stu-id="ee01c-108">To learn more about how AIR works, see [Automated Investigation and Response (AIR) with Office 365](automated-investigation-response-office.md).</span></span>

<span data-ttu-id="ee01c-109">Wenn bestimmte Warnungen ausgelöst werden, werden ein oder mehrere Sicherheits-Textbuch initiiert, und die automatische Untersuchung beginnt.</span><span class="sxs-lookup"><span data-stu-id="ee01c-109">With AIR, when certain alerts are triggered, one or more security playbooks initiate, and automated investigation begins.</span></span> <span data-ttu-id="ee01c-110">Während und nach einem automatisierten Ermittlungsprozess können Administratoren und Sicherheitsteams folgende Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="ee01c-110">During and after an automated investigation process, your administrators and security operations team can:</span></span>

- [<span data-ttu-id="ee01c-111">Anzeigen der Details einer Untersuchung</span><span class="sxs-lookup"><span data-stu-id="ee01c-111">View the details of an investigation</span></span>](#view-details-of-an-investigation)

- [<span data-ttu-id="ee01c-112">Überprüfen und Genehmigen von Aktionen als Ergebnis einer Untersuchung</span><span class="sxs-lookup"><span data-stu-id="ee01c-112">Review and approve actions as a result of an investigation</span></span>](#review-and-approve-actions) 

- [<span data-ttu-id="ee01c-113">Anzeigen von Details zu einer Warnung im Zusammenhang mit einer Untersuchung</span><span class="sxs-lookup"><span data-stu-id="ee01c-113">View details about an alert related to an investigation</span></span>](#view-details-about-an-alert-related-to-an-investigation)

> [!NOTE]
> <span data-ttu-id="ee01c-114">Sie müssen ein globaler Administrator, Sicherheitsadministrator, Sicherheits Operator oder Sicherheits Leser sein, um die in diesem Artikel beschriebenen Aufgaben ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ee01c-114">You must be a global administrator, security administrator, security operator, or security reader to perform the tasks described in this article.</span></span> <span data-ttu-id="ee01c-115">Weitere Informationen finden Sie unter [Microsoft 365 Security Center: Roles and Permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span><span class="sxs-lookup"><span data-stu-id="ee01c-115">To learn more, see [Microsoft 365 security center: roles and permissions](https://docs.microsoft.com/office365/securitycompliance/microsoft-security-and-compliance#required-licenses-and-permissions).</span></span>

## <a name="view-details-of-an-investigation"></a><span data-ttu-id="ee01c-116">Anzeigen von Details einer Untersuchung</span><span class="sxs-lookup"><span data-stu-id="ee01c-116">View details of an investigation</span></span>

1. <span data-ttu-id="ee01c-117">Wechseln Sie als Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser zu und melden [https://protection.office.com](https://protection.office.com) Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="ee01c-117">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="ee01c-118">Sie gelangen auf das Sicherheits #a0 Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="ee01c-118">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="ee01c-119">Führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="ee01c-119">Do one of the following:</span></span>

    - <span data-ttu-id="ee01c-120">Wechseln Sie zu **Threat Management** > **Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="ee01c-120">Go to **Threat management** > **Dashboard**.</span></span> <span data-ttu-id="ee01c-121">Dadurch gelangen Sie zum [Sicherheits Dashboard](security-dashboard.md).</span><span class="sxs-lookup"><span data-stu-id="ee01c-121">This takes you to the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="ee01c-122">Die Air-Widgets werden am oberen Rand des [Sicherheits Dashboards](security-dashboard.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ee01c-122">Your AIR widgets appear across the top of the [Security Dashboard](security-dashboard.md).</span></span> <span data-ttu-id="ee01c-123">Wählen Sie ein Widget aus, beispielsweise **Zusammenfassung der Untersuchungen**.</span><span class="sxs-lookup"><span data-stu-id="ee01c-123">Select a widget, such as **Investigations summary**.</span></span>

    - <span data-ttu-id="ee01c-124">Wechseln Sie zu **Threat Management** > **Investigations**.</span><span class="sxs-lookup"><span data-stu-id="ee01c-124">Go to **Threat management** > **Investigations**.</span></span> 

    <span data-ttu-id="ee01c-125">Mit beiden Methoden gelangen Sie zu einer Liste von Untersuchungen.</span><span class="sxs-lookup"><span data-stu-id="ee01c-125">Either method takes you to a list of investigations.</span></span>

    ![Haupt Untersuchungs Seite für Air](media/air-maininvestigationpage.png) 

3. <span data-ttu-id="ee01c-127">Wählen Sie in der Liste der Untersuchungen ein Element in der Spalte **ID** aus.</span><span class="sxs-lookup"><span data-stu-id="ee01c-127">In the list of investigations, select an item in the **ID** column.</span></span> <span data-ttu-id="ee01c-128">Dadurch wird die Seite Ermittlungs Details geöffnet, beginnend mit dem unter Such Diagramm.</span><span class="sxs-lookup"><span data-stu-id="ee01c-128">This opens investigation details page, starting with the investigation graph.</span></span>

    ![Seite "Luft Untersuchungs Diagramm"](media/air-investigationgraphpage.png)

4. <span data-ttu-id="ee01c-130">Verwenden Sie die verschiedenen Registerkarten, um mehr über die Untersuchung zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="ee01c-130">Use the various tabs to learn more about the investigation.</span></span>

## <a name="review-and-approve-actions"></a><span data-ttu-id="ee01c-131">Überprüfen und Genehmigen von Aktionen</span><span class="sxs-lookup"><span data-stu-id="ee01c-131">Review and approve actions</span></span>

<span data-ttu-id="ee01c-132">In Office 365 führen automatisierte Untersuchungen normalerweise zu einer oder mehreren empfohlenen Aktionen.</span><span class="sxs-lookup"><span data-stu-id="ee01c-132">In Office 365, automated investigations typically result in one or more recommended actions.</span></span> <span data-ttu-id="ee01c-133">Es werden jedoch keine Aktionen ausgeführt, bis Sie vom Sicherheits Betriebsteam genehmigt wurden.</span><span class="sxs-lookup"><span data-stu-id="ee01c-133">However, no actions are taken until they are approved by your security operations team.</span></span> <span data-ttu-id="ee01c-134">Verwenden Sie das folgende Verfahren, um Aktionen zu überprüfen und zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="ee01c-134">Use the following procedure to review and approve actions.</span></span>

1. <span data-ttu-id="ee01c-135">Wechseln Sie als Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser zu und melden [https://protection.office.com](https://protection.office.com) Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="ee01c-135">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> 

2. <span data-ttu-id="ee01c-136">Wechseln Sie zu **Threat Management** > **Investigations**.</span><span class="sxs-lookup"><span data-stu-id="ee01c-136">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="ee01c-137">Wählen Sie in der Liste der Untersuchungen ein Element in der Spalte **ID** aus.</span><span class="sxs-lookup"><span data-stu-id="ee01c-137">In the list of investigations, select an item in the **ID** column.</span></span> 

3. <span data-ttu-id="ee01c-138">Wählen Sie in der Ansicht Ermittlungs Details die Registerkarte **Aktionen** aus. Alle Aktionen, für die eine Genehmigung aussteht, werden hier aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ee01c-138">On the investigation details view, select the **Actions** tab. Any actions that are pending approval are listed here.</span></span>

4. <span data-ttu-id="ee01c-139">W?hlen Sie ein Element in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="ee01c-139">Select an item in the list.</span></span>

5. <span data-ttu-id="ee01c-140">Wählen Sie **genehmigen** aus, um die empfohlene Aktion zu ergreifen (oder **ablehnen** , um die Untersuchung ohne Aktion zu schließen).</span><span class="sxs-lookup"><span data-stu-id="ee01c-140">Select **Approve** to take the recommended action (or **Reject** to close the investigation without taking action).</span></span>

## <a name="view-details-about-an-alert-related-to-an-investigation"></a><span data-ttu-id="ee01c-141">Anzeigen von Details zu einer Warnung im Zusammenhang mit einer Untersuchung</span><span class="sxs-lookup"><span data-stu-id="ee01c-141">View details about an alert related to an investigation</span></span>

<span data-ttu-id="ee01c-142">Bestimmte Arten von Warnungen lösen eine automatische Untersuchung in Office 365 aus.</span><span class="sxs-lookup"><span data-stu-id="ee01c-142">Certain kinds of alerts trigger automated investigation in Office 365.</span></span> <span data-ttu-id="ee01c-143">Weitere Informationen finden Sie unter [Alerts](automated-investigation-response-office.md#alerts).</span><span class="sxs-lookup"><span data-stu-id="ee01c-143">To learn more, see [Alerts](automated-investigation-response-office.md#alerts).</span></span> <span data-ttu-id="ee01c-144">Verwenden Sie das folgende Verfahren, um Details zu einer Warnung anzuzeigen, die einer automatisierten Untersuchung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ee01c-144">Use the following procedure to view details about an alert that is associated with an automated investigation.</span></span>

1. <span data-ttu-id="ee01c-145">Wechseln Sie als Office 365 globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser zu und melden [https://protection.office.com](https://protection.office.com) Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="ee01c-145">As an Office 365 global administrator, security administrator, or security reader, go to [https://protection.office.com](https://protection.office.com) and sign in.</span></span> <span data-ttu-id="ee01c-146">Sie gelangen auf das Sicherheits #a0 Compliance Center.</span><span class="sxs-lookup"><span data-stu-id="ee01c-146">This takes you to the the Security & Compliance Center.</span></span>

2. <span data-ttu-id="ee01c-147">Wechseln Sie zu **Threat Management** > **Investigations**.</span><span class="sxs-lookup"><span data-stu-id="ee01c-147">Go to **Threat management** > **Investigations**.</span></span>

3. <span data-ttu-id="ee01c-148">Wählen Sie in der Liste der Untersuchungen ein Element in der Spalte **ID** aus.</span><span class="sxs-lookup"><span data-stu-id="ee01c-148">In the list of investigations, select an item in the **ID** column.</span></span> 

4. <span data-ttu-id="ee01c-149">Wenn Details zu einer Untersuchung geöffnet sind, wählen Sie die Registerkarte **Benachrichtigungen** aus. Alle Warnungen, die die Untersuchung ausgelöst haben, werden hier aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="ee01c-149">With details of an investigation open, select the **Alerts** tab. Any alerts that triggered the investigation are listed here.</span></span>

5. <span data-ttu-id="ee01c-150">W?hlen Sie ein Element in der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="ee01c-150">Select an item in the list.</span></span> <span data-ttu-id="ee01c-151">Ein Flyout mit Details zur Warnung und Links zu zusätzlichen Informationen und Aktionen wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="ee01c-151">A flyout opens, with details about the alert and links to additional information and actions.</span></span>

6. <span data-ttu-id="ee01c-152">Überprüfen Sie die Informationen im Flyout, und nehmen Sie abhängig von der jeweiligen Warnung eine Aktion vor, beispielsweise zum **Auflösen**, unter **drücken**oder **Benachrichtigen von Benutzern**.</span><span class="sxs-lookup"><span data-stu-id="ee01c-152">Review the information on the flyout, and, depending on the particular alert, take an action, such as **Resolve**, **Suppress**, or **Notify users**.</span></span> 

## <a name="use-the-office-365-management-activity-api-for-custom-or-third-party-reporting-solutions"></a><span data-ttu-id="ee01c-153">Verwenden der API für die Office 365-Verwaltungsaktivität für benutzerdefinierte oder Drittanbieter-Berichtslösungen</span><span class="sxs-lookup"><span data-stu-id="ee01c-153">Use the Office 365 Management Activity API for custom or third-party reporting solutions</span></span>

<span data-ttu-id="ee01c-154">Wenn Ihre Organisation eine benutzerdefinierte Berichtslösung oder eine Drittanbieter-Berichtslösung verwendet, können Sie Informationen zu automatisierten Untersuchungen in dieser Lösung mithilfe der API für die Office 365-Verwaltungsaktivität anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ee01c-154">If your organization is using a custom reporting solution, or a third-party reporting solution, you can view information about automated investigations in that solution by using the Office 365 Management Activity API.</span></span>

<span data-ttu-id="ee01c-155">Verwenden Sie die folgenden Ressourcen, um dies einzurichten:</span><span class="sxs-lookup"><span data-stu-id="ee01c-155">Use the following resources to set this up:</span></span>

|<span data-ttu-id="ee01c-156">Ressource</span><span class="sxs-lookup"><span data-stu-id="ee01c-156">Resource</span></span>  |<span data-ttu-id="ee01c-157">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee01c-157">Description</span></span>  |
|---------|---------|
|<span data-ttu-id="ee01c-158">[Übersicht über die Office 365-Verwaltungs-APIs](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview).</span><span class="sxs-lookup"><span data-stu-id="ee01c-158">[Office 365 Management APIs overview](https://docs.microsoft.com/office/office-365-management-api/office-365-management-apis-overview)</span></span>     |<span data-ttu-id="ee01c-159">Die Office 365-Verwaltungsaktivitäts-API bietet Informationen über verschiedene Benutzer-, Verwaltungs-, System- und Richtlinienaktionen und -ereignisse aus Office 365 und Azure Active Directory-Aktivitätsprotokollen.</span><span class="sxs-lookup"><span data-stu-id="ee01c-159">The Office 365 Management Activity API provides information about various user, admin, system, and policy actions and events from Office 365 and Azure Active Directory activity logs.</span></span>         |
|[<span data-ttu-id="ee01c-160">Erste Schritte mit den Office 365-Verwaltungs-APIs</span><span class="sxs-lookup"><span data-stu-id="ee01c-160">Get started with Office 365 Management APIs</span></span>](https://docs.microsoft.com/office/office-365-management-api/get-started-with-office-365-management-apis)     |<span data-ttu-id="ee01c-161">Die Office 365-Verwaltungs-API verwendet Azure AD, um Authentifizierungsdienste für Ihre Anwendung bereitzustellen, um auf Office 365 Daten zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee01c-161">The Office 365 Management API uses Azure AD to provide authentication services for your application to access Office 365 data.</span></span> <span data-ttu-id="ee01c-162">Führen Sie die Schritte in diesem Artikel aus, um dies einzurichten.</span><span class="sxs-lookup"><span data-stu-id="ee01c-162">Follow the steps in this article to set this up.</span></span>          |
|[<span data-ttu-id="ee01c-163">Office 365-Verwaltungsaktivitäts-API – Referenz</span><span class="sxs-lookup"><span data-stu-id="ee01c-163">Office 365 Management Activity API reference</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-reference)     |<span data-ttu-id="ee01c-164">Sie können die Office 365-Verwaltungs Aktivitäts-API verwenden, um Informationen zu Benutzer-, Verwaltungs-, System-und Richtlinienaktionen und-Ereignissen aus Office 365-und Azure AD-Aktivitätsprotokollen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ee01c-164">You can use the Office 365 Management Activity API to retrieve information about user, admin, system, and policy actions and events from Office 365 and Azure AD activity logs.</span></span> <span data-ttu-id="ee01c-165">Lesen Sie diesen Artikel, um mehr über die Funktionsweise zu erfahren.</span><span class="sxs-lookup"><span data-stu-id="ee01c-165">Read this article to learn more about how this works.</span></span>        |
|[<span data-ttu-id="ee01c-166">Office 365-Verwaltungsaktivitäts-API –Schema</span><span class="sxs-lookup"><span data-stu-id="ee01c-166">Office 365 Management Activity API schema</span></span>](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema)     |<span data-ttu-id="ee01c-167">Erhalten Sie einen Überblick über das [allgemeine Schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) und das [Office 365 ATP-und Threat-Ermittlungs-und-Antwortschema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) , um sich über bestimmte Arten von Daten zu informieren, die über die API für die Office 365-Verwaltungsaktivität verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ee01c-167">Get an overview of the [Common schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#common-schema) and the [Office 365 ATP and threat investigation and response schema](https://docs.microsoft.com/office/office-365-management-api/office-365-management-activity-api-schema#office-365-advanced-threat-protection-and-threat-investigation-and-response-schema) to learn about specific kinds of data available through the Office 365 Management Activity API.</span></span>         |

## <a name="next-steps"></a><span data-ttu-id="ee01c-168">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ee01c-168">Next steps</span></span>

[<span data-ttu-id="ee01c-169">Weitere Informationen zu Warnungen</span><span class="sxs-lookup"><span data-stu-id="ee01c-169">Learn more about alerts</span></span>](alert-policies.md)

[<span data-ttu-id="ee01c-170">Manuelles Suchen und untersuchen schädlicher e-Mails, die in Office 365 bereitgestellt wurden</span><span class="sxs-lookup"><span data-stu-id="ee01c-170">Manually find and investigate malicious email that was delivered in Office 365</span></span>](investigate-malicious-email-that-was-delivered.md)

[<span data-ttu-id="ee01c-171">Informationen zu Air in Microsoft Defender ATP</span><span class="sxs-lookup"><span data-stu-id="ee01c-171">Learn about AIR in Microsoft Defender ATP</span></span>](https://docs.microsoft.com/windows/security/threat-protection/microsoft-defender-atp/automated-investigations)

[<span data-ttu-id="ee01c-172">Besuchen Sie die Microsoft 365-Roadmap, um zu sehen, was bald kommt und wie Sie Rollen</span><span class="sxs-lookup"><span data-stu-id="ee01c-172">Visit the Microsoft 365 Roadmap to see what's coming soon and rolling out</span></span>](https://www.microsoft.com/microsoft-365/roadmap?filters=)