---
title: Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security
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
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Überprüfen der APP-Ermittlungsberichte in Office 365 Cloud-App-Sicherheit kann Ihnen helfen, mehr darüber zu erfahren, wie Personen in Ihrer Organisation Cloud-Apps verwenden. Nachdem Sie die APP-Ermittlungsberichte mithilfe von Protokolldateien aus Ihren Firewalls und Proxys erstellt haben, überarbeiten Sie die Ergebnisse im Dashboard App Discovery.
ms.openlocfilehash: fa5ab7c6cd734feb26878cf1a97f7ce708aa1478
ms.sourcegitcommit: 8679937354c1d8870ecd41519a59d2d7468c23c4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2019
ms.locfileid: "30087334"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="81192-104">Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="81192-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="81192-105">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="81192-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="81192-106">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="81192-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="81192-107">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="81192-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="81192-108">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="81192-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="81192-109">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="81192-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="81192-110">Planung starten</span><span class="sxs-lookup"><span data-stu-id="81192-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="81192-111">Starten der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="81192-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="81192-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="81192-112">You are here!</span></span>  <br/> [<span data-ttu-id="81192-113">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="81192-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="81192-p102">Das Cloud Discovery-Dashboard arbeitet mit den Webtraffic-Protokollen Ihrer Organisation zusammen, um detaillierte Informationen zur Verwendung von Cloud-apps bereitzustellen. Wenn Sie globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser sind und Ihre Organisation [App-Ermittlungsberichte in Office 365 Cloud App Security erstellt](create-app-discovery-reports-in-ocas.md)hat, können Sie mithilfe des Cloud Discovery-Dashboards Einblicke in die Benutzer in Ihrem die Organisation verwendet Office 365 und andere Cloud-apps. (Das Cloud Discovery-Dashboard wird auch als Produktivitäts-App-Erkennung bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="81192-p102">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage. If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps. (The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="81192-117">Mit dem Cloud Discovery Dashboard können Sie detaillierte Informationen dazu anzeigen, wie Personen in Ihrer Organisation Office 365 und andere apps verwenden.</span><span class="sxs-lookup"><span data-stu-id="81192-117">The Cloud Discovery dashboard enables you to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![Das Cloud Discovery-Dashboard wurde aktualisiert](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="81192-119">Wechseln zum Dashboard für die Cloud-Suche</span><span class="sxs-lookup"><span data-stu-id="81192-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="81192-120">Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="81192-120">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="81192-121">Wechseln **Sie zu Discover** \> **Cloud Discovery Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="81192-121">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="81192-122">Anzeigen der wichtigsten Benutzer, IP-Adressen, Apps und Risikostufen</span><span class="sxs-lookup"><span data-stu-id="81192-122">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="81192-123">Das Cloud Discovery Dashboard bietet Ihnen eine übersichtliche Übersicht über apps, die in Ihrer Organisation mit Office 365 verwendet werden, mit offenen Warnungen, Top-Benutzern und Risikostufen.</span><span class="sxs-lookup"><span data-stu-id="81192-123">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![Cloud Discovery dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="81192-125">Sehen Sie sich auf der Registerkarte **Dashboard** die allgemeine Cloud-App-Verwendung in Ihrer Organisation im Abschnitt Übersicht am oberen Rand des Bildschirms an.</span><span class="sxs-lookup"><span data-stu-id="81192-125">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="81192-126">In den **Office 365-Kategorien** finden Sie apps, die in Ihrer Organisation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81192-126">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="81192-127">Sehen Sie sich das Widget " **erkannte apps** " an, um die Verwendung von Office 365 und anderen apps in dieser Ansicht anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="81192-127">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="81192-128">Sehen Sie sich das Widget **Top users** and **Top IP Address** an, um diejenigen zu identifizieren, die Office 365 und Cloud-apps am meisten in Ihrer Organisation verwenden.</span><span class="sxs-lookup"><span data-stu-id="81192-128">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="81192-129">Sehen Sie, wo die apps, die Personen verwenden, nach geographischem Standort mithilfe der Standort Karte für **apps** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="81192-129">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="81192-p103">Sehen Sie sich über dem Kartenbereich die Risikobewertung der erkannten apps in der Übersicht **Risikostufen** an. Sie können Risiken anhand der gleichen Gruppen und Kategorien anzeigen, die Sie im Bereich **erkannte apps** verwendet haben. Sie können beispielsweise sehen, wie viel Datenverkehr in jeder Gruppierung aus hoch-, Mittel-oder risikoarmen apps stammt.</span><span class="sxs-lookup"><span data-stu-id="81192-p103">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview. You can look at risks by the same groups and categories that you used in the **Discovered apps** area. For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="81192-133">Tiefer in die Informationen einTauchen</span><span class="sxs-lookup"><span data-stu-id="81192-133">Dive deeper into the information</span></span>

<span data-ttu-id="81192-134">Sie können die Cloud-Ermittlung verwenden, um apps, Unterdomänen, IP-Adressen und Benutzer genauer zu betrachten.</span><span class="sxs-lookup"><span data-stu-id="81192-134">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="81192-135">Wählen Sie im Dashboard Cloud Discovery die Registerkarte **entdeckte apps** aus.</span><span class="sxs-lookup"><span data-stu-id="81192-135">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="81192-136">Verwenden Sie den Abschnitt Filter, um apps nach Name, Kategorie, Verwendungsebene oder Datum der letzten Anzeige anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="81192-136">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="81192-137">Hovern Sie in der Ergebnisliste nach einem APP-Namen, um den Link **Unterdomänen anzeigen anzuzeigen** .</span><span class="sxs-lookup"><span data-stu-id="81192-137">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span><br/> <span data-ttu-id="81192-138">![Hover neben einer APP, um einen Link zum Anzeigen von Unterdomänen Details anzuzeigen](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span><span class="sxs-lookup"><span data-stu-id="81192-138">![Hover next to an app to reveal a link to view subdomain details](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span></span><br/><span data-ttu-id="81192-139">Detaillierte Informationen über die ausgewählte App werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="81192-139">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="81192-140">Um Details zu IP-Adressen anzuzeigen, wählen Sie die Registerkarte **IP-Adressen** .</span><span class="sxs-lookup"><span data-stu-id="81192-140">To view details about IP addresses, choose the **IP addresses** tab.</span></span><br/><span data-ttu-id="81192-141">![Cloud Discovery zeigt detaillierte Informationen zu IP-Adressen](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span><span class="sxs-lookup"><span data-stu-id="81192-141">![Cloud Discovery shows detailed information about IP addresses](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span></span><br/><span data-ttu-id="81192-142">Wählen Sie in der Ergebnisliste eine einzelne IP-Adresse aus, um detailliertere Informationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="81192-142">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="81192-143">Um Details zu Office 365-Benutzern in Ihrer Organisation anzuzeigen, wählen Sie die Registerkarte **Benutzer** aus.</span><span class="sxs-lookup"><span data-stu-id="81192-143">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span><br/><span data-ttu-id="81192-144">![Cloud Discovery-Benutzerinformationen](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span><span class="sxs-lookup"><span data-stu-id="81192-144">![Cloud Discovery - users info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span></span>
  
## <a name="exclude-entities"></a><span data-ttu-id="81192-145">Entitäten ausschließen</span><span class="sxs-lookup"><span data-stu-id="81192-145">Exclude entities</span></span>

<span data-ttu-id="81192-146">Sie können bestimmte Systembenutzer oder IP-Adressen ausschließen, um sich auf genauere Informationen zu konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="81192-146">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="81192-147">Wählen Sie **Einstellungen** \> für die **Cloud-Erkennung**aus.</span><span class="sxs-lookup"><span data-stu-id="81192-147">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="81192-148">Wählen Sie **Entitäten ausschließen**aus.</span><span class="sxs-lookup"><span data-stu-id="81192-148">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="81192-149">Wählen Sie **Ausgeschlossene Benutzer** oder **ausgeschlossene IP-Adressen**aus.</span><span class="sxs-lookup"><span data-stu-id="81192-149">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="81192-150">Geben Sie die Benutzer oder IP-Adressen an, und geben Sie im Feld **Kommentare** Informationen dazu ein, warum Sie diese Benutzer oder IP-Adressen ausschließen.</span><span class="sxs-lookup"><span data-stu-id="81192-150">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="81192-151">Wählen Sie **Add** aus.</span><span class="sxs-lookup"><span data-stu-id="81192-151">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="81192-152">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="81192-152">Next steps</span></span>

- [<span data-ttu-id="81192-153">Überarbeiten und Aktionen für Warnungen</span><span class="sxs-lookup"><span data-stu-id="81192-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="81192-154">Erstellen von App-Ermittlungs Berichten</span><span class="sxs-lookup"><span data-stu-id="81192-154">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="81192-155">Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="81192-155">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

