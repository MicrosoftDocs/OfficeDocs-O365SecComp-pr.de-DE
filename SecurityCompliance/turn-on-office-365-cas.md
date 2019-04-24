---
title: Aktivieren der Office 365 Cloud-App-Sicherheit
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
ms.assetid: ba919c73-d021-404d-9850-eec57e78678c
description: In diesem Artikel erfahren Sie, wie Sie die Sicherheit von Office 365 Cloud-Apps aktivieren, die von Cloud App Security in Microsoft Azure unterstützt wird.
ms.openlocfilehash: 1227545b1e4d1521dc1820342f09aabdf16ec2c6
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264127"
---
# <a name="turn-on-office-365-cloud-app-security"></a><span data-ttu-id="8037d-103">Aktivieren der Office 365 Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="8037d-103">Turn on Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="8037d-104">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="8037d-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="8037d-105">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="8037d-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="8037d-106">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="8037d-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="8037d-107">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8037d-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="8037d-108">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="8037d-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="8037d-109">Planung starten</span><span class="sxs-lookup"><span data-stu-id="8037d-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="8037d-110">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="8037d-110">You are here!</span></span>  <br/> [<span data-ttu-id="8037d-111">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="8037d-111">Next step</span></span>](activity-policies-and-alerts.md) <br/> |[<span data-ttu-id="8037d-112">Verwendung beginnen</span><span class="sxs-lookup"><span data-stu-id="8037d-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
  
## <a name="turn-on-office-365-cloud-app-security"></a><span data-ttu-id="8037d-113">Aktivieren der Office 365 Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="8037d-113">Turn on Office 365 Cloud App Security</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8037d-114">Sie müssen ein globaler Administrator oder Sicherheitsadministrator sein, um die folgende Aufgabe ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="8037d-114">You must be a global administrator or security administrator to perform the following task.</span></span> <span data-ttu-id="8037d-115">Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="8037d-115">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> <span data-ttu-id="8037d-116">Damit Office 365 Cloud App Security korrekt funktioniert, **muss die Überwachungsprotokollierung** für ihre Office 365-Umgebung aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="8037d-116">In order for Office 365 Cloud App Security to work correct, **audit logging must be turned on** for your Office 365 environment.</span></span> <span data-ttu-id="8037d-117">Weitere Informationen finden Sie unter [Turn Office 365 Audit Log Search on or off](turn-audit-log-search-on-or-off.md).</span><span class="sxs-lookup"><span data-stu-id="8037d-117">For more information, see [Turn Office 365 audit log search on or off](turn-audit-log-search-on-or-off.md).</span></span> 
  
1. <span data-ttu-id="8037d-118">Gehen Sie als globaler Administrator oder Sicherheitsadministrator zu und [https://protection.office.com](https://security.microsoft.com) melden Sie sich mit Ihrem Arbeits-oder Schulkonto für Office 365 an.</span><span class="sxs-lookup"><span data-stu-id="8037d-118">As a global administrator or security administrator, go to [https://protection.office.com](https://security.microsoft.com) and sign in using your work or school account for Office 365.</span></span> <span data-ttu-id="8037d-119">(Dadurch gelangen Sie zum Security &amp; Compliance Center.)</span><span class="sxs-lookup"><span data-stu-id="8037d-119">(This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="8037d-120">Wechseln Sie zu **Warnungen** \> **Verwalten erweiterter Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="8037d-120">Go to **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="8037d-121">Wählen Sie **Office 365 Cloud App Security**aktivieren aus.</span><span class="sxs-lookup"><span data-stu-id="8037d-121">Select **Turn on Office 365 Cloud App Security**.</span></span>
    
4. <span data-ttu-id="8037d-122">Wählen Sie **Gehe zu Office 365 Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="8037d-122">Choose **Go to Office 365 Cloud App Security**.</span></span><br/><span data-ttu-id="8037d-123">![Wählen Sie im &amp; Security Compliance Center erweiterte Warnungen verwalten aus, um zu Office 365 Cloud App Security zu wechseln.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="8037d-123">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br/><span data-ttu-id="8037d-124">Dadurch gelangen Sie zum Office 365 Cloud App-Sicherheitsportal, in dem Sie Berichte anzeigen und Richtlinien erstellen oder bearbeiten können.</span><span class="sxs-lookup"><span data-stu-id="8037d-124">This takes you to the Office 365 Cloud App Security portal, where you can view reports and create or edit your policies.</span></span>

<span data-ttu-id="8037d-125">Nachdem Sie Office 365 Cloud App Security aktiviert haben, können Sie zum Cloud App Security Portal navigieren, indem [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) Sie sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="8037d-125">After you have turned on Office 365 Cloud App Security, you can go to the Cloud App Security portal by visiting [https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com) and signing in.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8037d-126">Wenn Sie Office 365 Cloud App Security aktivieren, werden Überwachungsinformationen zu Ihren Office 365-Benutzerkonten und Benutzeraktivitäten an [Microsoft Cloud App Security](https://aka.ms/whatiscas)übertragen.</span><span class="sxs-lookup"><span data-stu-id="8037d-126">When you turn on Office 365 Cloud App Security, auditing information about your Office 365 user accounts and user activities is transferred to [Microsoft Cloud App Security](https://aka.ms/whatiscas).</span></span> <span data-ttu-id="8037d-127">Dadurch kann Office 365 erweiterte Warnungen, Filterung und andere Features bereitstellen, damit Sie Informationen abrufen und Maßnahmen zu verdächtigen Aktivitäten ergreifen können.</span><span class="sxs-lookup"><span data-stu-id="8037d-127">This allows Office 365 to provide advanced alerts, filtering, and other features so you can get information and take action about suspicious activities.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="8037d-128">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="8037d-128">Next steps</span></span>

- [<span data-ttu-id="8037d-129">Aktivitätsrichtlinien</span><span class="sxs-lookup"><span data-stu-id="8037d-129">Activity policies</span></span>](activity-policies-and-alerts.md)
    
- [<span data-ttu-id="8037d-130">Erkennungsrichtlinien für Anomalien</span><span class="sxs-lookup"><span data-stu-id="8037d-130">Anomaly detection policies</span></span>](anomaly-detection-policies-in-ocas.md)
    
- [<span data-ttu-id="8037d-131">Integrieren Ihres SIEM-Servers</span><span class="sxs-lookup"><span data-stu-id="8037d-131">Integrate your SIEM server</span></span>](integrate-your-siem-server-with-office-365-cas.md)
    
- [<span data-ttu-id="8037d-132">Gruppieren Ihrer IP-Adressen zur Vereinfachung der Verwaltung</span><span class="sxs-lookup"><span data-stu-id="8037d-132">Group your IP addresses to simplify management</span></span>](group-your-ip-addresses-in-ocas.md)
    

