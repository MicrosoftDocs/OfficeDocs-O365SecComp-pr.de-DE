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
description: Überprüfen von app-Discovery-Berichten in Advanced Security Management kann Ihnen weitere Informationen zur Verwendung von Personen in Ihrer Organisation Cloud-apps. Nachdem Sie die app-Discovery-Berichte mithilfe von Protokolldateien von Firewalls und Proxys erstellt haben, überprüfen Sie die Ergebnisse in das app-Discovery-Dashboard.
ms.openlocfilehash: 6195c9aae7ae5e398ac555cc820de04dee05d4fd
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603746"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="d958b-104">Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="d958b-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="d958b-105">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="d958b-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="d958b-106">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="d958b-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="d958b-107">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="d958b-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="d958b-108">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="d958b-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="d958b-109">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="d958b-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="d958b-110">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="d958b-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="d958b-111">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="d958b-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="d958b-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="d958b-112">You are here!</span></span>  <br/> [<span data-ttu-id="d958b-113">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d958b-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="d958b-p102">Das Cloud-Discovery-Dashboard funktioniert mit Ihrer Organisation Web Datenverkehr Protokolle mit detaillierten Informationen zur Verwendung von Cloud-app. Wenn Sie ein globaler Administrator, Sicherheitsadministrator oder Sicherheit-Reader sind und Ihre Organisation hat die [app-Discovery-Berichte in Office 365-Cloud-App-Sicherheit erstellt](create-app-discovery-reports-in-ocas.md), können Sie das Dashboard Cloud Discovery Einblick in festlegen, wie Benutzer Ihrer Office 365 und anderen apps Cloud Organisation verwenden. (Das Cloud-Discovery-Dashboard ist auch bekannt als Produktivität App Discovery).</span><span class="sxs-lookup"><span data-stu-id="d958b-p102">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage. If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps. (The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="d958b-117">Das Cloud-Discovery-Dashboard können Sie ausführliche Informationen wie Benutzern in Ihrer Organisation Office 365 und andere apps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d958b-117">The Cloud Discovery dashboard enables you to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![Wurde aktualisiert, das Cloud-Discovery-dashboard](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="d958b-119">Wechseln Sie zu dem Cloud-Discovery-dashboard</span><span class="sxs-lookup"><span data-stu-id="d958b-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="d958b-120">Klicken Sie auf das Portal Cloud App-Sicherheit ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) und zur Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="d958b-120">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span>
    
2. <span data-ttu-id="d958b-121">Wechseln Sie zu **Discover** \> **Cloud Discovery-Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="d958b-121">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="d958b-122">Finden Sie unter der Top-Benutzer, IP-Adressen, apps und Risikoebenen</span><span class="sxs-lookup"><span data-stu-id="d958b-122">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="d958b-123">Das Cloud-Discovery-Dashboard enthält eine Übersicht auf einen Blick von apps, die in Ihrer Organisation, alle geöffneten Benachrichtigungen, Top-Benutzer und Risikoebenen mit Office 365 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d958b-123">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![Cloud-Discovery-dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="d958b-125">Klicken Sie auf der Registerkarte **Dashboard** betrachten Sie am oberen Rand des Bildschirms die gesamte Cloud app-Verwendung in Ihrer Organisation im Abschnitt Übersicht.</span><span class="sxs-lookup"><span data-stu-id="d958b-125">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="d958b-126">Finden Sie in der **Office 365-Kategorien** für apps, die in Ihrer Organisation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d958b-126">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="d958b-127">Sehen Sie sich das Widget **ermittelte apps** Verwendung von Office 365 und andere apps in dieser Ansicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d958b-127">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="d958b-128">Sehen Sie sich das Widget **Top-Benutzer** und **Top IP-Adressen** , die identifizieren, die Office 365 verwenden und cloud-apps in den in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="d958b-128">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="d958b-129">Finden Sie unter apps, die Benutzern verwendet werden, wo nach dem geografischen Standort befinden, mithilfe der Zuordnung **Hauptsitz Apps** .</span><span class="sxs-lookup"><span data-stu-id="d958b-129">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="d958b-p103">Sehen Sie über dem Bereich Maps sich die Risiko Bewertung der erkannten apps in der Übersicht über die **Risikoebenen** . Sie können betrachten Sie Risiken nach den Gruppen und Kategorien, die Sie im Bereich **ermittelte apps** verwendet. Beispielsweise können Sie sehen, wie viel Datenverkehr in jeder Gruppierung hoch, Mittel oder niedrig riskante apps stammt.</span><span class="sxs-lookup"><span data-stu-id="d958b-p103">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview. You can look at risks by the same groups and categories that you used in the **Discovered apps** area. For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="d958b-133">Detaillierte Informationen zu der information</span><span class="sxs-lookup"><span data-stu-id="d958b-133">Dive deeper into the information</span></span>

<span data-ttu-id="d958b-134">Cloud-Erkennung können Sie um einen genaueren Einblick in apps, Unterdomänen, IP-Adressen und Benutzer zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="d958b-134">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="d958b-135">Wählen Sie in der Cloud-Discovery-Dashboard der Registerkarte **ermittelte apps** .</span><span class="sxs-lookup"><span data-stu-id="d958b-135">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="d958b-136">Verwenden Sie den Abschnitt Filter, um apps nach Name, Kategorie, Auslastung oder Datum der letzten gesehen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d958b-136">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="d958b-137">Zeigen Sie in der Liste der Ergebnisse durch eine app-Name auf den Link **Anzeigen Unterdomänen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d958b-137">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span><br/> <span data-ttu-id="d958b-138">![Bewegen Sie den Mauszeiger neben einer app aus, um einen Link zur Detailansicht Unterdomäne anzuzeigen](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span><span class="sxs-lookup"><span data-stu-id="d958b-138">![Hover next to an app to reveal a link to view subdomain details](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)</span></span><br/><span data-ttu-id="d958b-139">Ausführliche Informationen über die gewählte app wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d958b-139">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="d958b-140">Um Details zu IP-Adressen anzuzeigen, wählen Sie die Registerkarte **IP-Adressen** .</span><span class="sxs-lookup"><span data-stu-id="d958b-140">To view details about IP addresses, choose the **IP addresses** tab.</span></span><br/><span data-ttu-id="d958b-141">![Cloud-Discovery zeigt detaillierte Informationen zu IP-Adressen](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span><span class="sxs-lookup"><span data-stu-id="d958b-141">![Cloud Discovery shows detailed information about IP addresses](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)</span></span><br/><span data-ttu-id="d958b-142">Wählen Sie in der Liste der Ergebnisse eine einzelne IP-Adresse Ausführlichere Informationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d958b-142">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="d958b-143">Um Details zu Office 365-Benutzer in Ihrer Organisation anzuzeigen, wählen Sie die Registerkarte **Benutzer** .</span><span class="sxs-lookup"><span data-stu-id="d958b-143">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span><br/><span data-ttu-id="d958b-144">![Cloud-Discovery - Benutzer-info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span><span class="sxs-lookup"><span data-stu-id="d958b-144">![Cloud Discovery - users info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)</span></span>
  
## <a name="exclude-entities"></a><span data-ttu-id="d958b-145">Ausschließen von Entitäten</span><span class="sxs-lookup"><span data-stu-id="d958b-145">Exclude entities</span></span>

<span data-ttu-id="d958b-146">Sie können bestimmte Benutzer oder die IP-Adressen, um auf bestimmte Informationen konzentrieren ausschließen.</span><span class="sxs-lookup"><span data-stu-id="d958b-146">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="d958b-147">**Auswählen von** \> **Cloud Discovery-Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="d958b-147">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="d958b-148">Wählen Sie die **Entitäten ausschließen**.</span><span class="sxs-lookup"><span data-stu-id="d958b-148">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="d958b-149">Wählen Sie **Ausgeschlossene Benutzer** oder **Ausgeschlossene IP-Adressen**.</span><span class="sxs-lookup"><span data-stu-id="d958b-149">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="d958b-150">Geben Sie den Benutzer oder die IP-Adressen, und geben Sie in das Feld **Kommentare** Informationen, warum Sie die Benutzer oder die IP-Adressen ausschließen.</span><span class="sxs-lookup"><span data-stu-id="d958b-150">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="d958b-151">Wählen Sie **Add** aus.</span><span class="sxs-lookup"><span data-stu-id="d958b-151">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="d958b-152">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d958b-152">Next steps</span></span>

- [<span data-ttu-id="d958b-153">Lesen und Ausführen einer Aktion Warnungen</span><span class="sxs-lookup"><span data-stu-id="d958b-153">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="d958b-154">Erstellen von Berichten für app-Ermittlung</span><span class="sxs-lookup"><span data-stu-id="d958b-154">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="d958b-155">Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="d958b-155">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

