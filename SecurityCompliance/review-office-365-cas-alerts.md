---
title: Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Verwenden Sie die Seite Warnungen in Office 365-Cloud-App-Sicherheit, zum Anzeigen von potenzieller Problemen und Ausführen einer Aktion. Sie können schließen oder Beheben von Benachrichtigungen, und Sie bei Bedarf anhalten ein Benutzerkontos.
ms.openlocfilehash: ff20b913553414d796f9653108ac9b8a3d84cb74
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603676"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="77688-104">Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="77688-104">Review and take action on alerts in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="77688-105">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="77688-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="77688-106">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="77688-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="77688-107">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="77688-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="77688-108">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="77688-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="77688-109">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="77688-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="77688-110">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="77688-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="77688-111">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="77688-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="77688-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="77688-112">You are here!</span></span>  <br/> [<span data-ttu-id="77688-113">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="77688-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="77688-114">Sie können die Seite Warnungen in Office 365-Cloud-App-Sicherheit verwenden, potenzielle Probleme anzeigen und, falls erforderlich, Aktion.</span><span class="sxs-lookup"><span data-stu-id="77688-114">You can use the Alerts page in Office 365 Cloud App Security to view potential issues and, if needed, take action.</span></span>
  
> [!NOTE]
> <span data-ttu-id="77688-p102">Sie müssen ein globaler Administrator oder Sicherheitsadministrator zum Ausführen der Aufgaben in diesem Artikel werden. Finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="77688-p102">You must be a global administrator or security administrator to perform the tasks in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-to-get-to-the-alerts-page"></a><span data-ttu-id="77688-117">Wie Sie auf der Seite Warnungen abrufen</span><span class="sxs-lookup"><span data-stu-id="77688-117">How to get to the Alerts page</span></span>

1. <span data-ttu-id="77688-118">Klicken Sie auf das Portal Cloud App-Sicherheit ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) und zur Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="77688-118">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="77688-119">Wählen Sie in der Navigationsleiste oben auf dem Bildschirm **Benachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="77688-119">In the navigation bar across the top of the screen, choose **Alerts**.</span></span><br/><span data-ttu-id="77688-120">![Klicken Sie auf der Seite Warnungen finden Sie unter Benachrichtigungen, die ausgelöst wurden und Aktionen.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span><span class="sxs-lookup"><span data-stu-id="77688-120">![On the Alerts page, you can see alerts that were triggered and any actions taken.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span></span>
  
## <a name="review-and-handle-alerts"></a><span data-ttu-id="77688-121">Überprüfen und Handle Warnungen</span><span class="sxs-lookup"><span data-stu-id="77688-121">Review and handle alerts</span></span>

<span data-ttu-id="77688-p103">Benachrichtigungen können Sie die Aktivitäten in der Office 365-Cloud-Umgebung zu identifizieren, die Sie möglicherweise weiter zu untersuchen. Sie könnten auch neue Richtlinien erstellen oder Bearbeiten von vorhandenen Richtlinien basierend auf der Warnungen an, die Sie sehen. Wenn Sie einen Administrator Anmelden von einem seltsam Standort angezeigt wird, können Sie eine Richtlinie, die verhindert, dass Administratoren anmelden bei Office 365 aus bestimmten Positionen einrichten.</span><span class="sxs-lookup"><span data-stu-id="77688-p103">Alerts help you identify activities in your Office 365 cloud environment that you might want to investigate further. You might also decide to create new policies or edit existing policies based on the alerts you see. For example, if you see an administrator logging on from a strange location, you may decide to set up a policy that prevents administrators from signing in to Office 365 from certain locations.</span></span>
  
> [!TIP]
> <span data-ttu-id="77688-125">Sie können Benachrichtigungen nach **Kategorie** oder nach **Schweregrad** filtern, sodass Sie zuerst die wichtigsten verwalten können.</span><span class="sxs-lookup"><span data-stu-id="77688-125">You can filter the alerts by **Category** or by **Severity** so you can manage the most important ones first.</span></span> 
  
<span data-ttu-id="77688-p104">Untersuchen Sie für jede Warnung was ihm verursachten, sodass Sie entscheiden können, welche Aktion. Weitere Details zu einer Warnung angezeigt und auszuführende Aktion wie etwa Auflösen der Warnung oder Anhalten eines Benutzerkontos wählen Sie die Benachrichtigung zu eine Seite zu öffnen aus. Auf der Detailseite können Sie überprüfen die Aktivitätsprotokolls sowie die Konten und Benutzer, die im Zusammenhang mit der Benachrichtigung, und wie die folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="77688-p104">For each alert, look into what caused it so you can decide what action to take. To see more details about an alert and to take action, such as resolving the alert or suspending a users account, choose the alert to open a details page. On the details page, you can review the activity log, accounts, and users that are related to the alert, and take actions such as the following:</span></span>
  
- <span data-ttu-id="77688-p105">**Schließen** Wenn die Benachrichtigung falsch positives Ergebnis war, schließen Sie es. Sie können optional hinzufügen ein Kommentars erläutert, warum es geschlossen.</span><span class="sxs-lookup"><span data-stu-id="77688-p105">**Dismiss** If the alert was a false positive, dismiss it. You can optionally add a comment explaining why you dismissed it.</span></span> 
    
- <span data-ttu-id="77688-p106">**Warnung auflösen** Wenn die Warnung ausgelöst wurde, indem eine Aktivität, die Sie kennen keine Bedrohung ist, lösen. Sie können optional einen Kommentar erläutert, warum Sie gelöst hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="77688-p106">**Resolve alert** If the alert was triggered by an activity that you know isn't a threat, resolve it. You can optionally add a comment explaining why you resolved it.</span></span> 
    
- <span data-ttu-id="77688-133">**Anhalten** Wenn Sie nicht autorisierten Anmeldung, ins auf einem Konto an, beispielsweise eine Person Anmelden aus einem anderen Land vermute, wenn Sie diese Person kennen physisch an einer Niederlassung befindet, können Sie [Unterbrechen Sie das Konto](suspend-or-restore-an-account-in-ocas.md) , während Sie untersuchen, was passiert.</span><span class="sxs-lookup"><span data-stu-id="77688-133">**Suspend** If you suspect unauthorized sign ins on an account, for example, someone signing in from another country when you know that person is physically at a local office, you can [suspend the account](suspend-or-restore-an-account-in-ocas.md) while you investigate what's going on.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="77688-134">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="77688-134">Next steps</span></span>

- [<span data-ttu-id="77688-135">Untersuchen Sie eine Aktivität</span><span class="sxs-lookup"><span data-stu-id="77688-135">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="77688-136">Anhalten oder Wiederherstellen eines Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="77688-136">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- <span data-ttu-id="77688-137">Anzeigen einer Liste mit unterstützten [Web Datenverkehr Protokolle und Datenquellen](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="77688-137">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="77688-138">Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="77688-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

