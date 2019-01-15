---
title: Untersuchen einer Aktivität in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 15fa4545-28b4-4dd4-bf85-88e0926bd5fc
description: 'Mit Office 365 Cloud App-Sicherheit können Sie sehen, was passiert in Ihrer Office 365-Umgebung von über suchen und bearbeitenden Aktivitäten und Konten. '
ms.openlocfilehash: d988a86c5ceaa2ec46bc27f1aaff540fa3e0b3b4
ms.sourcegitcommit: 9034809b6f308bedc3b8ddcca8242586b5c30f94
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2019
ms.locfileid: "28014897"
---
# <a name="investigate-an-activity-in-office-365-cloud-app-security"></a><span data-ttu-id="61c1a-103">Untersuchen einer Aktivität in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="61c1a-103">Investigate an activity in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="61c1a-104">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="61c1a-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="61c1a-105">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="61c1a-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="61c1a-106">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="61c1a-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="61c1a-107">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="61c1a-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="61c1a-108">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="61c1a-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="61c1a-109">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="61c1a-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="61c1a-110">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="61c1a-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="61c1a-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="61c1a-111">You are here!</span></span>  <br/> [<span data-ttu-id="61c1a-112">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="61c1a-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="61c1a-p101">Office 365 funktioniert Cloud App-Sicherheit mit Ihrem [Office 365-Überwachungsprotokoll](detailed-properties-in-the-office-365-audit-log.md). Mit Office 365 Cloud App-Sicherheit können als globaler Administrator oder Sicherheitsadministrator, die Seite Aktivität-Protokoll Sie finden Sie unter potenzielle Probleme in wie Ihre Organisation die Office 365 verwendet.</span><span class="sxs-lookup"><span data-stu-id="61c1a-p101">Office 365 Cloud App Security works with your [Office 365 audit log](detailed-properties-in-the-office-365-audit-log.md). With Office 365 Cloud App Security, as a global administrator or security administrator, you can use the Activity log page to see potential issues in how your organization is using Office 365.</span></span>
  
## <a name="how-to-get-to-the-activity-log-page"></a><span data-ttu-id="61c1a-115">Wie Sie auf der Seite Aktivität Protokoll abrufen</span><span class="sxs-lookup"><span data-stu-id="61c1a-115">How to get to the Activity log page</span></span>

1. <span data-ttu-id="61c1a-p102">Als globaler Administrator oder Sicherheitsadministrator, wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. (Siehe [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span><span class="sxs-lookup"><span data-stu-id="61c1a-p102">As a global administrator or security administrator, go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (See [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).)</span></span>
    
2. <span data-ttu-id="61c1a-118">In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="61c1a-118">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="61c1a-119">Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="61c1a-119">Choose **Go to Office 365 Cloud App Security**.</span></span><br/><span data-ttu-id="61c1a-120">![In das Wertpapier &amp; Compliance Center, wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="61c1a-120">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span>
  
4. <span data-ttu-id="61c1a-121">Wählen Sie in der Navigationsleiste oben auf dem Bildschirm, **untersuchen** \> **Aktivitätsprotokolls**.</span><span class="sxs-lookup"><span data-stu-id="61c1a-121">In the navigation bar across the top of the screen, choose **Investigate** \> **Activity log**.</span></span><br/><span data-ttu-id="61c1a-122">![Wählen Sie im Portal O365 CAS überprüfen.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span><span class="sxs-lookup"><span data-stu-id="61c1a-122">![In the O365 CAS portal, choose Investigate.](media/8c7b87c9-71a6-4952-adb2-185e941ffe9a.png)</span></span>
  
## <a name="review-and-investigate-activities"></a><span data-ttu-id="61c1a-123">Überprüfen und Untersuchen von Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="61c1a-123">Review and investigate activities</span></span>

<span data-ttu-id="61c1a-p103">Auf der Seite Aktivität Protokoll sehen Sie eine Liste der verschiedenen Aktivitäten, die stattfinden innerhalb Ihrer Organisation mithilfe von Office 365. Filter können im oberen Bereich des Bildschirms Sie um auf einen bestimmten Objekttyp Aktivität oder einen bestimmten Benutzer zu konzentrieren. Das folgende Bild zeigt beispielsweise Informationen zu einer Organisation Office 365 Administratorkonto Kennwort ändern:</span><span class="sxs-lookup"><span data-stu-id="61c1a-p103">On the Activity log page, you can see a list of various activities that are taking place within your organization using Office 365. You can use filters across the top of the screen to focus on a specific type of activity or a specific user. For example, the following image shows information about an organization's Office 365 admin account's password change:</span></span>
  
![Wählen Sie in Office 365 Cloud App-Sicherheit, untersuchen \> Aktivitätsprotokolls.](media/5d54600c-59cd-4f33-b4f0-29b75c37baae.png)
  
<span data-ttu-id="61c1a-p104">Wie Sie jedes Element in der Aktivitätsprotokolls betrachten, können Sie die Auslassungspunkte, um andere zugehörigen Aktivitäten suchen klicken. Beispielsweise können Sie andere Aktivitäten des gleichen Typs aus dieselbe IP-Adresse oder aus demselben Land/Region anzeigen.</span><span class="sxs-lookup"><span data-stu-id="61c1a-p104">As you look at each item in the Activity log, you can click the ellipses to find other related activities. For example, you can view other activities of the same type, from the same IP address, or from the same country/region.</span></span>
  
<span data-ttu-id="61c1a-p105">Sie können Informationen zu viele andere Arten von Aktivitäten zu anzeigen. Beispielsweise sind hier einige der Aktionen, die Sie im Protokoll Aktivität anzeigen können:</span><span class="sxs-lookup"><span data-stu-id="61c1a-p105">You can view information about many other kinds of activities, too. For example, here are some of the activities you can view in the Activity log:</span></span>
  
- <span data-ttu-id="61c1a-132">Mitglieder hinzugefügt oder entfernt aus Gruppen</span><span class="sxs-lookup"><span data-stu-id="61c1a-132">Members added to or removed from groups</span></span>
    
- <span data-ttu-id="61c1a-133">Änderungen in Benutzerlizenzen</span><span class="sxs-lookup"><span data-stu-id="61c1a-133">Changes in user licenses</span></span>
    
- <span data-ttu-id="61c1a-134">Dateien oder Ordner freigegebene intern oder extern</span><span class="sxs-lookup"><span data-stu-id="61c1a-134">Files or folders shared internally or externally</span></span>
    
- <span data-ttu-id="61c1a-135">Erstellte oder gelöschte Websites oder Websitesammlungen</span><span class="sxs-lookup"><span data-stu-id="61c1a-135">Created or deleted sites or site collections</span></span>
    
- <span data-ttu-id="61c1a-136">E-Mail-Weiterleitung von Regeln</span><span class="sxs-lookup"><span data-stu-id="61c1a-136">Email forwarding rules</span></span>
    
<span data-ttu-id="61c1a-137">Verwendung gibt die Seite Aktivität-Protokoll zu kennen lernen mit wie Personen in Ihrer Organisation Office 365 und was verwenden, erhalten sie möglicherweise haben Sie dabei.</span><span class="sxs-lookup"><span data-stu-id="61c1a-137">Use the Activity log page to get acquainted with how people in your organization are using Office 365 and what issues they might be having along the way.</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="61c1a-138">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="61c1a-138">Next steps</span></span>

- [<span data-ttu-id="61c1a-139">Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="61c1a-139">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- <span data-ttu-id="61c1a-140">Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="61c1a-140">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

