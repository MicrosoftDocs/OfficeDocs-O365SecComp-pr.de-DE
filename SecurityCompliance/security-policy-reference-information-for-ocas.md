---
title: Sicherheitsrichtlinien-Referenzinformationen für Office 365 Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 2/26/2018
ms.audience: ITPro
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aef6c88f-7f47-40ef-9503-2b400e3bc6fd
description: Erhalten Sie Hilfe zu Office 365-Aktivitätsrichtlinien und Erkennungsrichtlinien für Anomalien.
ms.openlocfilehash: db44b6cbf5b8c2783cba9862107120d2c33c1559
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32264627"
---
# <a name="security-policy-reference-information-for-office-365-cloud-app-security"></a><span data-ttu-id="f70e7-103">Sicherheitsrichtlinien-Referenzinformationen für Office 365 Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="f70e7-103">Security policy reference information for Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="f70e7-104">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="f70e7-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="f70e7-105">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="f70e7-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="f70e7-106">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="f70e7-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="f70e7-107">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="f70e7-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="f70e7-108">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="f70e7-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="f70e7-109">Planung starten</span><span class="sxs-lookup"><span data-stu-id="f70e7-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |<span data-ttu-id="f70e7-110">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="f70e7-110">You are here!</span></span>  <br/> [<span data-ttu-id="f70e7-111">Nächster Schritt</span><span class="sxs-lookup"><span data-stu-id="f70e7-111">Next step</span></span>](review-office-365-cas-alerts.md) <br/> |[<span data-ttu-id="f70e7-112">Verwendung beginnen</span><span class="sxs-lookup"><span data-stu-id="f70e7-112">Start utilizing</span></span>](utilization-activities-for-ocas.md) <br/> |
   
<span data-ttu-id="f70e7-113">Wenn Sie ein globaler Administrator oder Sicherheitsadministrator sind, können Sie mit Office 365 Cloud App Security zwei Arten von Richtlinien für Ihre Organisation definieren oder bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="f70e7-113">With Office 365 Cloud App Security, if you are a global administrator or security administrator, you can define or edit two kinds of policies for your organization:</span></span>
  
- <span data-ttu-id="f70e7-114">**[Aktivitätsrichtlinien](activity-policies-and-alerts.md)** , die Sie definieren.</span><span class="sxs-lookup"><span data-stu-id="f70e7-114">**[Activity policies](activity-policies-and-alerts.md)** that you define.</span></span> <span data-ttu-id="f70e7-115">Diese Richtlinien basieren auf Aktivitäten, die Sie als verdächtig definieren, beispielsweise für Benutzer, die sich mit Administratoranmeldeinformationen in anderen Regionen/Ländern außerhalb der für Ihre Organisation üblichen oder einer extremen Anzahl von Anmeldeversuchen für einen Benutzer innerhalb einer Stunde anmelden möchten. .</span><span class="sxs-lookup"><span data-stu-id="f70e7-115">These policies are based on activities that you define as suspicious, such as users attempting to sign in with admin credentials in other regions/countries outside what's normal for your organization, or an extreme number of sign-in attempts for a user within an hour.</span></span> <span data-ttu-id="f70e7-116">Weitere Informationen finden Sie unter [Aktivitätsrichtlinien und Warnungen in Office 365 Cloud App Security](activity-policies-and-alerts.md).</span><span class="sxs-lookup"><span data-stu-id="f70e7-116">To learn more, see [Activity policies and alerts in Office 365 Cloud App Security](activity-policies-and-alerts.md).</span></span>
    
- <span data-ttu-id="f70e7-117">**[Anomalie-Erkennungsrichtlinien](anomaly-detection-policies-in-ocas.md)** , die mit Office 365 Cloud App Security sofort verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f70e7-117">**[Anomaly detection policies](anomaly-detection-policies-in-ocas.md)** that are available "out of the box" with Office 365 Cloud App Security.</span></span> <span data-ttu-id="f70e7-118">Diese Richtlinien basieren auf automatischen Algorithmen, die verdächtige Aktivitäten aufspüren.</span><span class="sxs-lookup"><span data-stu-id="f70e7-118">These policies are based on automatic algorithms that detect suspicious activity.</span></span> <span data-ttu-id="f70e7-119">Diese Standardrichtlinien achten auf Anomalien und lösen automatisch Warnungen aus.</span><span class="sxs-lookup"><span data-stu-id="f70e7-119">These default policies watch for anomalies and trigger alerts automatically.</span></span> <span data-ttu-id="f70e7-120">Weitere Informationen finden Sie unter [Anomalie Detection Policies in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="f70e7-120">To learn more, see [Anomaly detection policies in Office 365 Cloud App Security](anomaly-detection-policies-in-ocas.md).</span></span>
    

