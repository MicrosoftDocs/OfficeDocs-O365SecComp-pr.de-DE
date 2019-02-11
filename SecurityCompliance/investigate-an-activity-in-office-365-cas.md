---
title: Untersuchen einer Aktivität in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Mit Office 365 Cloud App-Sicherheit können Sie sehen, was passiert in Ihrer Office 365-Umgebung von über suchen und bearbeitenden Aktivitäten und Konten. '
ms.openlocfilehash: e463323cf28738e1d54fcdb65ed0d15290c79994
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603656"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="34593-103">Untersuchen einer Aktivität in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="34593-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="34593-104">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="34593-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="34593-105">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="34593-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="34593-106">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="34593-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="34593-107">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="34593-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="34593-108">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="34593-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="34593-109">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="34593-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="34593-110">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="34593-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="34593-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="34593-111">You are here!</span></span>  <br/> [<span data-ttu-id="34593-112">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="34593-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="34593-p101">Office 365 funktioniert Cloud App-Sicherheit mit Ihrem [Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md). Mit Office 365 Cloud App-Sicherheit können als globaler Administrator oder Sicherheitsadministrator, die Seite Aktivität-Protokoll Sie finden Sie unter potenzielle Probleme in wie Ihre Organisation die Office 365 verwendet.</span><span class="sxs-lookup"><span data-stu-id="34593-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="34593-115">Wie Sie auf der Seite Aktivität Protokoll abrufen</span><span class="sxs-lookup"><span data-stu-id="34593-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="34593-116">Klicken Sie auf das Portal Cloud App-Sicherheit ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) und zur Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="34593-116">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
  
2. <span data-ttu-id="34593-117">Wählen Sie in der Navigationsleiste oben auf dem Bildschirm, **untersuchen** \> **Aktivitätsprotokolls**.</span><span class="sxs-lookup"><span data-stu-id="34593-117">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="34593-118">![Wählen Sie im Portal O365 CAS überprüfen.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="34593-118">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="34593-119">Überprüfen und Untersuchen von Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="34593-119">Review and investigate activities</span></span>

<span data-ttu-id="34593-p102">Auf der Seite Aktivität Protokoll sehen Sie eine Liste der verschiedenen Aktivitäten, die stattfinden innerhalb Ihrer Organisation mithilfe von Office 365. Filter können im oberen Bereich des Bildschirms Sie um auf einen bestimmten Objekttyp Aktivität oder einen bestimmten Benutzer zu konzentrieren. Das folgende Bild zeigt beispielsweise Informationen zu einer Organisation Office 365 Administratorkonto Kennwort ändern:</span><span class="sxs-lookup"><span data-stu-id="34593-p102">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![Wählen Sie in Office 365 Cloud App-Sicherheit, untersuchen \> Aktivitätsprotokolls.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="34593-p103">Wie Sie jedes Element in der Aktivitätsprotokolls betrachten, können Sie die Auslassungspunkte, um andere zugehörigen Aktivitäten suchen klicken. Beispielsweise können Sie andere Aktivitäten des gleichen Typs aus dieselbe IP-Adresse oder aus demselben Land/Region anzeigen.</span><span class="sxs-lookup"><span data-stu-id="34593-p103">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="34593-p104">Sie können Informationen zu viele andere Arten von Aktivitäten zu anzeigen. Beispielsweise sind hier einige der Aktionen, die Sie im Protokoll Aktivität anzeigen können:</span><span class="sxs-lookup"><span data-stu-id="34593-p104">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="34593-128">Mitglieder hinzugefügt oder entfernt aus Gruppen</span><span class="sxs-lookup"><span data-stu-id="34593-128">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="34593-129">Änderungen in Benutzerlizenzen</span><span class="sxs-lookup"><span data-stu-id="34593-129">Changes in user licenses</span></span>
    
- <span data-ttu-id="34593-130">Dateien oder Ordner freigegebene intern oder extern</span><span class="sxs-lookup"><span data-stu-id="34593-130">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="34593-131">Erstellte oder gelöschte Websites oder Websitesammlungen</span><span class="sxs-lookup"><span data-stu-id="34593-131">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="34593-132">E-Mail-Weiterleitung von Regeln</span><span class="sxs-lookup"><span data-stu-id="34593-132">Email forwarding rules</span></span>
    
<span data-ttu-id="34593-133">Verwendung gibt die Seite Aktivität-Protokoll zu kennen lernen mit wie Personen in Ihrer Organisation Office 365 und was verwenden, erhalten sie möglicherweise haben Sie dabei.</span><span class="sxs-lookup"><span data-stu-id="34593-133">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="34593-134">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="34593-134">Next steps</span></span>

- [<span data-ttu-id="34593-135">Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="34593-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="34593-136">Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="34593-136">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

