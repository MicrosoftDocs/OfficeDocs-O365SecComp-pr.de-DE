---
title: Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 97e9c3d9-df89-458e-924b-369becee5532
description: Verwenden Sie die Seite "Benachrichtigungen" in Office 365 Cloud App Security, um potenzielle Probleme anzuzeigen und Maßnahmen zu ergreifen. Sie können Benachrichtigungen schließen oder auflösen und gegebenenfalls ein Benutzerkonto anhalten.
ms.openlocfilehash: 6c2f9788cb238e86abc347a3a118eb08fa84e971
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30213165"
---
# <a name="review-and-take-action-on-alerts-in-office-365-cloud-app-security"></a><span data-ttu-id="751fd-104">Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="751fd-104">Review and take action on alerts in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="751fd-105">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="751fd-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="751fd-106">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="751fd-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="751fd-107">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="751fd-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="751fd-108">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="751fd-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="751fd-109">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="751fd-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="751fd-110">Planung starten</span><span class="sxs-lookup"><span data-stu-id="751fd-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="751fd-111">Starten der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="751fd-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="751fd-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="751fd-112">You are here!</span></span>  <br/> [<span data-ttu-id="751fd-113">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="751fd-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="751fd-114">Sie können die Seite "Benachrichtigungen" in Office 365 Cloud App Security verwenden, um potenzielle Probleme anzuzeigen und gegebenenfalls Maßnahmen zu ergreifen.</span><span class="sxs-lookup"><span data-stu-id="751fd-114">You can use the Alerts page in Office 365 Cloud App Security to view potential issues and, if needed, take action.</span></span>
  
> [!NOTE]
> <span data-ttu-id="751fd-p102">Sie müssen ein globaler Administrator oder Sicherheitsadministrator sein, um die Aufgaben in diesem Artikel ausführen zu können. Weitere Informationen finden Sie unter [Permissions &amp; in the Office 365 Security Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="751fd-p102">You must be a global administrator or security administrator to perform the tasks in this article. See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="how-to-get-to-the-alerts-page"></a><span data-ttu-id="751fd-117">So gelangen Sie zur Seite "Benachrichtigungen"</span><span class="sxs-lookup"><span data-stu-id="751fd-117">How to get to the Alerts page</span></span>

1. <span data-ttu-id="751fd-118">Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="751fd-118">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="751fd-119">Klicken Sie in der Navigationsleiste am oberen Rand des Bildschirms auf **Benachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="751fd-119">In the navigation bar across the top of the screen, choose **Alerts**.</span></span><br/><span data-ttu-id="751fd-120">![Auf der Seite Warnungen werden Warnungen angezeigt, die ausgelöst wurden, und alle ausgeführten Aktionen.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span><span class="sxs-lookup"><span data-stu-id="751fd-120">![On the Alerts page, you can see alerts that were triggered and any actions taken.](media/3b53d4c9-4b13-435d-8547-8c0f9ae6b914.png)</span></span>
  
## <a name="review-and-handle-alerts"></a><span data-ttu-id="751fd-121">Überarbeiten und behandeln von Warnungen</span><span class="sxs-lookup"><span data-stu-id="751fd-121">Review and handle alerts</span></span>

<span data-ttu-id="751fd-p103">Warnungen helfen Ihnen dabei, Aktivitäten in Ihrer Office 365-Cloud-Umgebung zu identifizieren, die Sie möglicherweise weiter untersuchen möchten. Sie können auch beschließen, neue Richtlinien zu erstellen oder vorhandene Richtlinien basierend auf den Warnungen zu bearbeiten, die Ihnen angezeigt werden. Wenn ein Administrator sich beispielsweise an einem seltsamen Ort anmeldet, können Sie eine Richtlinie einrichten, die verhindert, dass Administratoren sich an bestimmten Standorten bei Office 365 anmelden.</span><span class="sxs-lookup"><span data-stu-id="751fd-p103">Alerts help you identify activities in your Office 365 cloud environment that you might want to investigate further. You might also decide to create new policies or edit existing policies based on the alerts you see. For example, if you see an administrator logging on from a strange location, you may decide to set up a policy that prevents administrators from signing in to Office 365 from certain locations.</span></span>
  
> [!TIP]
> <span data-ttu-id="751fd-125">Sie können die Warnungen nach **Kategorie** oder nach **Schweregrad** filtern, damit Sie die wichtigsten zuerst verwalten können.</span><span class="sxs-lookup"><span data-stu-id="751fd-125">You can filter the alerts by **Category** or by **Severity** so you can manage the most important ones first.</span></span> 
  
<span data-ttu-id="751fd-p104">Untersuchen Sie für jede Warnung, was Sie verursacht hat, damit Sie entscheiden können, welche Aktion ausgeführt werden soll. Wenn Sie weitere Details zu einer Warnung anzeigen und Maßnahmen ergreifen möchten, wie beispielsweise das Auflösen der Warnung oder das Anhalten eines Benutzerkontos, wählen Sie die Warnung aus, um eine Detailseite zu öffnen. Auf der Seite Details können Sie das Aktivitätsprotokoll, die Konten und Benutzer, die mit der Benachrichtigung verbunden sind, überwachen und folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="751fd-p104">For each alert, look into what caused it so you can decide what action to take. To see more details about an alert and to take action, such as resolving the alert or suspending a users account, choose the alert to open a details page. On the details page, you can review the activity log, accounts, and users that are related to the alert, and take actions such as the following:</span></span>
  
- <span data-ttu-id="751fd-p105">**Entlassen** Wenn die Warnung falsch positiv war, schließen Sie Sie. Sie können optional einen Kommentar hinzufügen, der erklärt, warum Sie ihn entlassen haben.</span><span class="sxs-lookup"><span data-stu-id="751fd-p105">**Dismiss** If the alert was a false positive, dismiss it. You can optionally add a comment explaining why you dismissed it.</span></span> 
    
- <span data-ttu-id="751fd-p106">**Warnung auflösen** Wenn die Warnung durch eine Aktivität ausgelöst wurde, von der Sie wissen, dass es sich nicht um eine Bedrohung handelt, beheben Sie Sie. Sie können optional einen Kommentar hinzufügen, der erklärt, warum Sie ihn aufgelöst haben.</span><span class="sxs-lookup"><span data-stu-id="751fd-p106">**Resolve alert** If the alert was triggered by an activity that you know isn't a threat, resolve it. You can optionally add a comment explaining why you resolved it.</span></span> 
    
- <span data-ttu-id="751fd-133">**Anhalten** Wenn Sie vermuten, dass unbefugte Benutzer sich für ein Konto anmelden, beispielsweise jemanden, der sich in einem anderen Land anmeldet, wenn Sie wissen, dass sich diese Person physisch in einem lokalen Büro befindet, können Sie [das Konto anhalten](suspend-or-restore-an-account-in-ocas.md) , während Sie untersuchen, was vor sich geht.</span><span class="sxs-lookup"><span data-stu-id="751fd-133">**Suspend** If you suspect unauthorized sign ins on an account, for example, someone signing in from another country when you know that person is physically at a local office, you can [suspend the account](suspend-or-restore-an-account-in-ocas.md) while you investigate what's going on.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="751fd-134">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="751fd-134">Next steps</span></span>

- [<span data-ttu-id="751fd-135">Untersuchen einer Aktivität</span><span class="sxs-lookup"><span data-stu-id="751fd-135">Investigate an activity</span></span>](investigate-an-activity-in-office-365-cas.md)
    
- [<span data-ttu-id="751fd-136">Anhalten oder Wiederherstellen eines Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="751fd-136">Suspend or restore a user account</span></span>](suspend-or-restore-an-account-in-ocas.md)
    
- <span data-ttu-id="751fd-137">Anzeigen einer Liste unterstützter [Webdatenverkehr-Protokolle und Datenquellen](web-traffic-logs-and-data-sources-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="751fd-137">View a list of supported [Web traffic logs and data sources](web-traffic-logs-and-data-sources-for-ocas.md)</span></span>
    
- <span data-ttu-id="751fd-138">Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="751fd-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

