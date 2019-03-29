---
title: Sperren oder Wiederherstellen eines Benutzerkontos in Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 12/03/2018
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Mit Office 365 Cloud App Security können Sie ein Benutzerkonto anhalten oder aufheben. '
ms.openlocfilehash: 10da1385f850fadf077b4e3f9e3a00e9e4629fdd
ms.sourcegitcommit: 1658be51e2c21ed23bc4467a98af74300a45b975
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/26/2019
ms.locfileid: "30862447"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="ce96a-103">Sperren oder Wiederherstellen eines Benutzerkontos in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="ce96a-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

|<span data-ttu-id="ce96a-104">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="ce96a-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="ce96a-105">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="ce96a-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="ce96a-106">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="ce96a-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="ce96a-107">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="ce96a-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="ce96a-108">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="ce96a-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="ce96a-109">Planung starten</span><span class="sxs-lookup"><span data-stu-id="ce96a-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="ce96a-110">Starten der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ce96a-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="ce96a-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="ce96a-111">You are here!</span></span>  <br/> [<span data-ttu-id="ce96a-112">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ce96a-112">Next steps</span></span>](#next-steps)<br/> |
   
<span data-ttu-id="ce96a-113">Angenommen, Sie erhalten eine Warnung, dass eines der Benutzerkonten Ihrer Organisation für Office 365 kompromittiert wurde.</span><span class="sxs-lookup"><span data-stu-id="ce96a-113">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised.</span></span> <span data-ttu-id="ce96a-114">Oder nehmen wir an, Sie haben eine Warnung erhalten, die angibt, dass mit einem Benutzerkonto ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="ce96a-114">Or, suppose that you've received an alert that indicates something is wrong with a user account.</span></span> <span data-ttu-id="ce96a-115">Mit Office 365 Cloud App Security können Sie ein Benutzerkonto anhalten und später wiederherstellen, nachdem Sie die empfangenen Warnungen untersucht haben.</span><span class="sxs-lookup"><span data-stu-id="ce96a-115">With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ce96a-116">Office 365 Cloud App Security ist in Office 365 Enterprise E5 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ce96a-116">Office 365 Cloud App Security is available in Office 365 Enterprise E5.</span></span> <span data-ttu-id="ce96a-117">Wenn Ihre Organisation ein anderes Office 365 Enterprise-Abonnement verwendet, kann Office 365 Cloud App Security als Add-on erworben werden.</span><span class="sxs-lookup"><span data-stu-id="ce96a-117">If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on.</span></span> <span data-ttu-id="ce96a-118">(klicken sie als globaler administrator im Office 365 admin center auf **abrechnungs** \> **abonnements hinzufügen**.) Weitere Informationen finden Sie unter [office 365 Platform Service Description: office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) und [kaufen oder Bearbeiten eines add-ons für Office 365 for Business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="ce96a-118">(As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="ce96a-119">So unterbrechen Sie ein Benutzerkonto in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="ce96a-119">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="ce96a-120">Wenn Sie ein Benutzerkonto anhalten, verhindern Sie, dass der Benutzer sich erneut anmeldet.</span><span class="sxs-lookup"><span data-stu-id="ce96a-120">When you suspend a user account, you prevent the user from signing in again.</span></span> <span data-ttu-id="ce96a-121">Dies entspricht dem Bearbeiten des Benutzerkontos direkt in Office 365, um den Anmeldestatus auf " **angemeldet**" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="ce96a-121">It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ce96a-122">Wenn Sie verhindern möchten, dass ein Benutzer sich bei Office 365 anmeldet, indem Sie ihn anhalten oder den Anmeldestatus bearbeiten, beachten Sie, dass es eine Stunde dauern kann, bis alle Benutzer Geräte und-Clients wirksam werden ([Bearbeiten oder Ändern eines Benutzers in office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)).</span><span class="sxs-lookup"><span data-stu-id="ce96a-122">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)).</span></span> <span data-ttu-id="ce96a-123">Wenn der Benutzer bei Office 365 angemeldet ist, wird der Block wirksam, wenn sich Office 365 erneut anmelden muss.</span><span class="sxs-lookup"><span data-stu-id="ce96a-123">If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="ce96a-124">Gehen Sie als [globaler Administrator oder Sicherheitsadministrator](permissions-in-the-security-and-compliance-center.md)zu und [https://protection.office.com](https://protection.office.com) melden Sie sich mit Ihrem Geschäfts-oder Schulkonto an.</span><span class="sxs-lookup"><span data-stu-id="ce96a-124">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account.</span></span> <span data-ttu-id="ce96a-125">(Dadurch gelangen Sie zum Security &amp; Compliance Center.)</span><span class="sxs-lookup"><span data-stu-id="ce96a-125">(This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="ce96a-126">Wählen Sie im &amp; Security Compliance Center **Alerts** \> **Manage Advanced Alerts**aus.</span><span class="sxs-lookup"><span data-stu-id="ce96a-126">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="ce96a-127">Wählen Sie **Gehe zu Office 365 Cloud App Security**.</span><span class="sxs-lookup"><span data-stu-id="ce96a-127">Choose **Go to Office 365 Cloud App Security**.</span></span><br><span data-ttu-id="ce96a-128">![Wählen Sie im &amp; Security Compliance Center erweiterte Warnungen verwalten aus, um zu Office 365 Cloud App Security zu wechseln.](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span><span class="sxs-lookup"><span data-stu-id="ce96a-128">![In the Security &amp; Compliance Center, choose Manage Advanced Alerts to go to Office 365 Cloud App Security](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)</span></span><br>
  
4. <span data-ttu-id="ce96a-129">Klicken Sie in der Navigationsleiste am oberen Rand des Bildschirms auf **Benachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="ce96a-129">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="ce96a-130">Doppelklicken Sie in der Spalte **Warnung** auf eine Warnung, die sich auf ein bestimmtes Benutzerkonto bezieht.</span><span class="sxs-lookup"><span data-stu-id="ce96a-130">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="ce96a-131">Wählen Sie unter **Konten**in der Spalte **Status** die Option ![Einstellungs Einstellungen](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> Symbol **Benutzer anhalten**aus.</span><span class="sxs-lookup"><span data-stu-id="ce96a-131">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="ce96a-132">So stellen Sie ein Benutzerkonto wieder her</span><span class="sxs-lookup"><span data-stu-id="ce96a-132">To restore a user account</span></span>

<span data-ttu-id="ce96a-133">Weitere Informationen finden Sie unter [Wiederherstellen eines Benutzers in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span><span class="sxs-lookup"><span data-stu-id="ce96a-133">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="ce96a-134">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="ce96a-134">Next steps</span></span>

- [<span data-ttu-id="ce96a-135">Überprüfen und Ergreifen entsprechender Maßnahmen bei Warnungen in Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="ce96a-135">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="ce96a-136">Verwalten von OAuth-Apps mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="ce96a-136">Manage OAuth apps using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="ce96a-137">Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="ce96a-137">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

