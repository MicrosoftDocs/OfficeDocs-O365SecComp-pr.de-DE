---
title: Untersuchen einer Aktivität in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Mit Office 365 Cloud App Security können Sie sehen, was in Ihrer Office 365-Umgebung geschieht, indem Sie nach Aktivitäten und Konten suchen. '
ms.openlocfilehash: 0cc3860d953b40b0b0c247af6fb2b157d1abb235
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32254833"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="665f5-103">Untersuchen einer Aktivität in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="665f5-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="665f5-104">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="665f5-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="665f5-105">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="665f5-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="665f5-106">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="665f5-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="665f5-107">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="665f5-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="665f5-108">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="665f5-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="665f5-109">Planung starten</span><span class="sxs-lookup"><span data-stu-id="665f5-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="665f5-110">Starten der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="665f5-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="665f5-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="665f5-111">You are here!</span></span>  <br/> [<span data-ttu-id="665f5-112">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="665f5-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="665f5-113">Office 365 Cloud App Security funktioniert mit Ihrem [office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md).</span><span class="sxs-lookup"><span data-stu-id="665f5-113">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md).</span></span> <span data-ttu-id="665f5-114">Mit Office 365 Cloud App Security als globaler Administrator oder Sicherheitsadministrator können Sie die Seite Aktivitätsprotokoll verwenden, um potenzielle Probleme bei der Verwendung von Office 365 in Ihrer Organisation anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="665f5-114">With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="665f5-115">So gelangen Sie zur Seite "Aktivitätsprotokoll"</span><span class="sxs-lookup"><span data-stu-id="665f5-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="665f5-116">Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="665f5-116">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="665f5-117">Wählen Sie in der Navigationsleiste am oberen Rand des Bildschirms **Aktivitätsprotokoll**über **prüfen** \> aus.</span><span class="sxs-lookup"><span data-stu-id="665f5-117">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="665f5-118">![Wählen Sie im O365-CAS-Portal untersuchen aus.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="665f5-118">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="665f5-119">Überprüfen und untersuchen von Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="665f5-119">Review and investigate activities</span></span>

<span data-ttu-id="665f5-120">Auf der Aktivitätsprotokoll Seite finden Sie eine Liste der verschiedenen Aktivitäten, die in Ihrer Organisation mithilfe von Office 365 durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="665f5-120">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365.</span></span> <span data-ttu-id="665f5-121">Sie können Filter am oberen Rand des Bildschirms verwenden, um sich auf einen bestimmten Aktivitätstyp oder einen bestimmten Benutzer zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="665f5-121">You can use filters across the top of the screen to focus on a specific type of activity or a specific user.</span></span> <span data-ttu-id="665f5-122">Die folgende Abbildung zeigt beispielsweise Informationen zur Kennwortänderung der Office 365-Administratorkonten einer Organisation:</span><span class="sxs-lookup"><span data-stu-id="665f5-122">For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![Wählen Sie in Office 365 Cloud App Security die \> Option Aktivitätsprotokoll untersuchen aus.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="665f5-124">Wenn Sie sich jedes Element im Aktivitätsprotokoll ansehen, können Sie auf die Ellipsen klicken, um nach anderen verwandten Aktivitäten zu suchen.</span><span class="sxs-lookup"><span data-stu-id="665f5-124">As you look at each item in the Activity log, you can click the ellipses to find other related activities.</span></span> <span data-ttu-id="665f5-125">Sie können beispielsweise andere Aktivitäten desselben Typs, von derselben IP-Adresse oder aus demselben Land/derselben Region anzeigen.</span><span class="sxs-lookup"><span data-stu-id="665f5-125">For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="665f5-126">Sie können auch Informationen zu vielen anderen Arten von Aktivitäten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="665f5-126">You can view information about many other kinds of activities, too.</span></span> <span data-ttu-id="665f5-127">Hier sind einige der Aktivitäten, die Sie im Aktivitätsprotokoll anzeigen können:</span><span class="sxs-lookup"><span data-stu-id="665f5-127">For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="665f5-128">Mitglieder, die zu Gruppen hinzugefügt oder daraus entfernt wurden</span><span class="sxs-lookup"><span data-stu-id="665f5-128">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="665f5-129">Änderungen bei Benutzerlizenzen</span><span class="sxs-lookup"><span data-stu-id="665f5-129">Changes in user licenses</span></span>
    
- <span data-ttu-id="665f5-130">Intern oder extern freigegebene Dateien oder Ordner</span><span class="sxs-lookup"><span data-stu-id="665f5-130">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="665f5-131">Erstellte oder gelöschte Websites oder Websitesammlungen</span><span class="sxs-lookup"><span data-stu-id="665f5-131">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="665f5-132">Regeln für die e-Mail-Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="665f5-132">Email forwarding rules</span></span>
    
<span data-ttu-id="665f5-133">Auf der Aktivitätsprotokoll Seite erfahren Sie, wie Personen in Ihrer Organisation Office 365 verwenden und welche Probleme Sie möglicherweise auf dem Weg haben.</span><span class="sxs-lookup"><span data-stu-id="665f5-133">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="665f5-134">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="665f5-134">Next steps</span></span>

- [<span data-ttu-id="665f5-135">Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="665f5-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="665f5-136">Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="665f5-136">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

