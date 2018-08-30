---
title: Anhalten oder Wiederherstellen eines Benutzerkontos in Office 365-Cloud-App-Sicherheit
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
ms.assetid: 5f02d20f-b9aa-4b2f-ad2d-506a4a3c4540
description: 'Governance Aktionen, die Sie ergreifen können, werden mit Office 365 Cloud App-Sicherheit unterbrechen oder Fortsetzen eines Benutzerkontos. '
ms.openlocfilehash: a5c75edefc6ddb87b5676c4253aafe04817f6a1d
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529044"
---
# <a name="suspend-or-restore-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="48189-103">Anhalten oder Wiederherstellen eines Benutzerkontos in Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="48189-103">Suspend or restore a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="48189-104">Office 365 Advanced Security Management ist jetzt Office 365-Cloud-App-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="48189-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="48189-105">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="48189-105">****Evaluation** \>**</span></span>|<span data-ttu-id="48189-106">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="48189-106">****Planning** \>**</span></span>|<span data-ttu-id="48189-107">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="48189-107">****Deployment** \>**</span></span>|<span data-ttu-id="48189-108">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="48189-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="48189-109">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="48189-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="48189-110">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="48189-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="48189-111">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="48189-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="48189-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="48189-112">You are here!</span></span>  <br/> [<span data-ttu-id="48189-113">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="48189-113">Next steps</span></span>](suspend-or-restore-an-account-in-ocas.md#nextsteps) <br/> |
   
<span data-ttu-id="48189-p101">Nehmen Sie an, dass Sie eine Benachrichtigung, dass eine der Benutzerkonten für Office 365 Ihrer Organisation gefährdet. Oder nehmen Sie an, dass Sie eine Benachrichtigung erhalten haben, die angibt, dass etwas mit einem Benutzerkonto falsch ist. Mit Office 365 Cloud App-Sicherheit können anhalten ein Benutzerkontos und einem späteren Zeitpunkt wiederherstellen, nachdem Sie die Benachrichtigungen erhalten Sie untersucht haben.</span><span class="sxs-lookup"><span data-stu-id="48189-p101">Suppose that you receive an alert that one of your organization's user accounts for Office 365 has been compromised. Or, suppose that you've received an alert that indicates something is wrong with a user account. With Office 365 Cloud App Security, you can suspend a user account and later restore it after you have investigated the alerts you receive.</span></span>
  
> [!NOTE]
> <span data-ttu-id="48189-p102">Office 365-Cloud-App-Sicherheit ist in Office 365 Enterprise E5 verfügbar. Wenn in Ihrer Organisation ein weiteres Abonnement von Office 365 Enterprise verwendet wird, kann Office 365-Cloud-App-Sicherheit als Add-on erworben werden. (Als ein globaler Administrator in der Office 365-Verwaltungskonsole, wählen Sie **Abrechnung** \> **Hinzufügen Abonnements**.) Weitere Informationen finden Sie unter [Office 365-Plattformdienstbeschreibung: Sicherheit in Office 365 &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) und [gekauft oder bearbeiten Sie ein Add-on für Office 365 für Unternehmen](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span><span class="sxs-lookup"><span data-stu-id="48189-p102">Office 365 Cloud App Security is available in Office 365 Enterprise E5. If your organization is using another Office 365 Enterprise subscription, Office 365 Cloud App Security can be purchased as an add-on. (As a global administrator, in the Office 365 admin center, choose **Billing** \> **Add subscriptions**.) For more information, see [Office 365 Platform Service Description: Office 365 Security &amp; Compliance Center](https://technet.microsoft.com/en-us/library/dn933793.aspx) and [Buy or edit an add-on for Office 365 for business](https://support.office.com/article/4e7b57d6-b93b-457d-aecd-0ea58bff07a6).</span></span> 
  
## <a name="to-suspend-a-user-account-in-office-365-cloud-app-security"></a><span data-ttu-id="48189-120">Anhalten ein Benutzerkontos in Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="48189-120">To suspend a user account in Office 365 Cloud App Security</span></span>

<span data-ttu-id="48189-p103">Wenn Sie ein Benutzerkonto anhalten, verhindern, dass Sie den Benutzer erneut anmelden. Es ist identisch mit der Bearbeitung des Benutzerkontos direkt in Office 365 für festzulegen, dass der Anmeldestatus **- Anmeldung blockiert**.</span><span class="sxs-lookup"><span data-stu-id="48189-p103">When you suspend a user account, you prevent the user from signing in again. It's the same as editing the user account directly in Office 365 to set the Sign-in status to **Sign-in blocked**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="48189-p104">Wenn Sie einen Benutzer aus anmelden bei Office 365, indem ihre Anmeldestatus, bearbeiten oder unterbrechen sie blockieren Beachten Sie, dass es eine Stunde oder dies wirksam auf allen Geräten und Clients ([Bearbeiten oder ändern ein Benutzers in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)) des Benutzers übernehmen kann. Wenn der Benutzer zu Office 365 angemeldet ist, wird der Block wirksam wird, wenn Office 365 erneut anmelden müssen.</span><span class="sxs-lookup"><span data-stu-id="48189-p104">If you block a user from signing in to Office 365, either by suspending them or by editing their sign-in status, be aware that it can take an hour or so to take effect on all of the user's devices and clients ([Edit or change a user in Office 365](https://support.office.com/article/42BB3F17-8F9D-4182-B434-5F1C8024E614#SingleUserPreview)). If the user is signed in to Office 365, the block will take effect whenever Office 365 requires them to sign in again.</span></span> 
  
1. <span data-ttu-id="48189-p105">Als [globaler Administrator oder Sicherheitsadministrator](permissions-in-the-security-and-compliance-center.md), wechseln Sie zur [https://protection.office.com](https://protection.office.com) und melden Sie sich mit Ihrem Konto arbeiten oder Schule. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.)</span><span class="sxs-lookup"><span data-stu-id="48189-p105">As a [global administrator or security administrator](permissions-in-the-security-and-compliance-center.md), go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="48189-127">In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="48189-127">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
3. <span data-ttu-id="48189-128">Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="48189-128">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
    ![In das Wertpapier &amp; Compliance Center, wählen Sie erweiterte Benachrichtigungen verwalten, fahren Sie mit Office 365-Cloud-App-Sicherheit](media/958632d4-03e3-4ade-8e22-d5509db6fca7.png)
  
4. <span data-ttu-id="48189-130">Wählen Sie in der Navigationsleiste oben auf dem Bildschirm **Benachrichtigungen**.</span><span class="sxs-lookup"><span data-stu-id="48189-130">In the navigation bar across the top of the screen, choose **Alerts**.</span></span>
    
5. <span data-ttu-id="48189-131">Doppelklicken Sie in der Spalte **Warnung** auf eine Warnung, die für ein bestimmtes Benutzerkonto relevant ist.</span><span class="sxs-lookup"><span data-stu-id="48189-131">In the **Alert** column, double-click an alert that pertains to a specific user account.</span></span> 
    
6. <span data-ttu-id="48189-132">Wählen Sie unter **Konten**in der Spalte **Status** Einstellungen ![einstellungssymbol](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend-Benutzer**.</span><span class="sxs-lookup"><span data-stu-id="48189-132">Under **Accounts**, in the **Status** column, choose Settings ![settings icon](media/e01b75cc-b28f-4b83-8f86-b1b13dc27ab2.png) \> **Suspend user**.</span></span>
    
## <a name="to-restore-a-user-account"></a><span data-ttu-id="48189-133">Wiederherstellen ein Benutzerkontos</span><span class="sxs-lookup"><span data-stu-id="48189-133">To restore a user account</span></span>

<span data-ttu-id="48189-134">Finden Sie unter [Wiederherstellen eines Benutzers in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span><span class="sxs-lookup"><span data-stu-id="48189-134">See [Restore a user in Office 365](https://support.office.com/article/2c261e42-5dd1-48b0-845f-2a016d29cfc1)</span></span>
  
## <a name="next-steps"></a><span data-ttu-id="48189-135">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="48189-135">Next steps</span></span>

- [<span data-ttu-id="48189-136">Lesen Sie und führen Sie einer Aktion Warnungen in Office 365-Cloud-App-Sicherheit aus</span><span class="sxs-lookup"><span data-stu-id="48189-136">Review and take action on alerts in Office 365 Cloud App Security</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="48189-137">Verwalten von app-Berechtigungen, die mit Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="48189-137">Manage app permissions using Office 365 Cloud App Security</span></span>](manage-app-permissions-in-ocas.md)
    
- <span data-ttu-id="48189-138">Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="48189-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

