---
title: Überprüfen der app Discovery Ergebnisse in Office 365-Cloud-App-Sicherheit
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 3/19/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: aac65513-e75e-4c82-a668-9a6604dd9f9d
description: Überprüfen von app-Discovery-Berichten in Advanced Security Management kann Ihnen weitere Informationen zur Verwendung von Personen in Ihrer Organisation Cloud-apps. Nachdem Sie die app-Discovery-Berichte mithilfe von Protokolldateien von Firewalls und Proxys erstellt haben, überprüfen Sie die Ergebnisse in das app-Discovery-Dashboard.
ms.openlocfilehash: 188ef87920b26069e7d99057662b3812be22e46c
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528857"
---
# <a name="review-app-discovery-findings-in-office-365-cloud-app-security"></a><span data-ttu-id="c2ade-104">Überprüfen der app Discovery Ergebnisse in Office 365-Cloud-App-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="c2ade-104">Review app discovery findings in Office 365 Cloud App Security</span></span>
  
|<span data-ttu-id="c2ade-105">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="c2ade-105">****Evaluation** \>**</span></span>|<span data-ttu-id="c2ade-106">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="c2ade-106">****Planning** \>**</span></span>|<span data-ttu-id="c2ade-107">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="c2ade-107">****Deployment** \>**</span></span>|<span data-ttu-id="c2ade-108">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="c2ade-108">****Utilization****</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="c2ade-109">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="c2ade-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="c2ade-110">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="c2ade-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="c2ade-111">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="c2ade-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="c2ade-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="c2ade-112">You are here!</span></span>  <br/> [<span data-ttu-id="c2ade-113">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c2ade-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="c2ade-p102">Das Cloud-Discovery-Dashboard funktioniert mit Ihrer Organisation Web Datenverkehr Protokolle mit detaillierten Informationen zur Verwendung von Cloud-app. Wenn Sie ein globaler Administrator, Sicherheitsadministrator oder Sicherheit-Reader sind und Ihre Organisation hat die [app-Discovery-Berichte in Office 365-Cloud-App-Sicherheit erstellt](create-app-discovery-reports-in-ocas.md), können Sie das Dashboard Cloud Discovery Einblick in festlegen, wie Benutzer Ihrer Office 365 und anderen apps Cloud Organisation verwenden. (Das Cloud-Discovery-Dashboard ist auch bekannt als Produktivität App Discovery).</span><span class="sxs-lookup"><span data-stu-id="c2ade-p102">The Cloud Discovery dashboard works with your organization's web traffic logs to provide detailed information about cloud app usage. If you're a global administrator, security administrator, or security reader, and your organization has [created app discovery reports in Office 365 Cloud App Security](create-app-discovery-reports-in-ocas.md), you can use the Cloud Discovery dashboard to gain insight into how people in your organization are using Office 365 and other cloud apps. (The Cloud Discovery dashboard is also known as Productivity App Discovery.)</span></span>
  
 <span data-ttu-id="c2ade-117">**Ab März 2018, das Cloud-Discovery-Dashboard verfügt über neue Features** , mit denen leichter wie Benutzern in Ihrer Organisation Office 365 und andere apps verwendet werden detaillierte Informationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c2ade-117">**As of March 2018, the Cloud Discovery dashboard has new features** that make it easier to view detailed information about how people in your organization are using Office 365 and other apps.</span></span> 
  
![Wurde aktualisiert, das Cloud-Discovery-dashboard](media/12712681-c0b3-4cb3-b7fd-2cf2ad4e825f.png)
     
## <a name="go-to-the-cloud-discovery-dashboard"></a><span data-ttu-id="c2ade-119">Wechseln Sie zu dem Cloud-Discovery-dashboard</span><span class="sxs-lookup"><span data-stu-id="c2ade-119">Go to the Cloud Discovery dashboard</span></span>

1. <span data-ttu-id="c2ade-p103">Wechseln Sie zu [https://protection.office.com](https://protection.office.com) und melden Sie sich über Ihr Konto arbeiten oder Schule für Office 365. (Dadurch gelangen Sie zu der Sicherheit &amp; Compliance Center.)</span><span class="sxs-lookup"><span data-stu-id="c2ade-p103">Go to [https://protection.office.com](https://protection.office.com) and sign in using your work or school account for Office 365. (This takes you to the Security &amp; Compliance Center.)</span></span> 
    
2. <span data-ttu-id="c2ade-122">In das Wertpapier &amp; Compliance Center, wählen Sie **Warnungen** \> **Verwalten erweiterte Warnungen**.</span><span class="sxs-lookup"><span data-stu-id="c2ade-122">In the Security &amp; Compliance Center, choose **Alerts** \> **Manage advanced alerts**.</span></span>
    
    <span data-ttu-id="c2ade-123">(Falls die Office 365-Cloud-App-Sicherheit noch nicht aktiviert, und Sie sind ein globaler Administrator, [Office 365-Cloud-App-Sicherheit zu aktivieren](turn-on-office-365-cas.md).)</span><span class="sxs-lookup"><span data-stu-id="c2ade-123">(If Office 365 Cloud App Security is not yet enabled, and you are a global administrator, [turn on Office 365 Cloud App Security](turn-on-office-365-cas.md).)</span></span>
    
3. <span data-ttu-id="c2ade-124">Wählen Sie, **Wechseln Sie zu Office 365-Cloud-App-Sicherheit**.</span><span class="sxs-lookup"><span data-stu-id="c2ade-124">Choose **Go to Office 365 Cloud App Security**.</span></span>
    
4. <span data-ttu-id="c2ade-125">Wechseln Sie zu **Discover** \> **Cloud Discovery-Dashboard**.</span><span class="sxs-lookup"><span data-stu-id="c2ade-125">Go to **Discover** \> **Cloud Discovery dashboard**.</span></span>
    
## <a name="see-your-top-users-ip-addresses-apps-and-risk-levels"></a><span data-ttu-id="c2ade-126">Finden Sie unter der Top-Benutzer, IP-Adressen, apps und Risikoebenen</span><span class="sxs-lookup"><span data-stu-id="c2ade-126">See your top users, IP addresses, apps, and risk levels</span></span>

<span data-ttu-id="c2ade-127">Das Cloud-Discovery-Dashboard enthält eine Übersicht auf einen Blick von apps, die in Ihrer Organisation, alle geöffneten Benachrichtigungen, Top-Benutzer und Risikoebenen mit Office 365 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2ade-127">The Cloud Discovery dashboard gives you an at-a-glance overview of apps that are used with Office 365 in your organization, any open alerts, top users, and risk levels.</span></span>
  
![Cloud-Discovery-dashboaard](media/06696946-fbdf-4781-b5b8-2ac074fcb2a1.png)
  
1. <span data-ttu-id="c2ade-129">Klicken Sie auf der Registerkarte **Dashboard** betrachten Sie am oberen Rand des Bildschirms die gesamte Cloud app-Verwendung in Ihrer Organisation im Abschnitt Übersicht.</span><span class="sxs-lookup"><span data-stu-id="c2ade-129">On the **Dashboard** tab, look at the overall cloud app use in your organization in the overview section across the top of the screen.</span></span> 
    
2. <span data-ttu-id="c2ade-130">Finden Sie in der **Office 365-Kategorien** für apps, die in Ihrer Organisation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2ade-130">See the **Office 365 categories** for apps that are used in your organization.</span></span> 
    
3. <span data-ttu-id="c2ade-131">Sehen Sie sich das Widget **ermittelte apps** Verwendung von Office 365 und andere apps in dieser Ansicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c2ade-131">Look at the **Discovered apps** widget to see usage of Office 365 and other apps in this view.</span></span> 
    
4. <span data-ttu-id="c2ade-132">Sehen Sie sich das Widget **Top-Benutzer** und **Top IP-Adressen** , die identifizieren, die Office 365 verwenden und cloud-apps in den in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="c2ade-132">Look at the **Top users** and **Top IP addresses** widget to identify those who use Office 365 and cloud apps the most in your organization.</span></span> 
    
5. <span data-ttu-id="c2ade-133">Finden Sie unter apps, die Benutzern verwendet werden, wo nach dem geografischen Standort befinden, mithilfe der Zuordnung **Hauptsitz Apps** .</span><span class="sxs-lookup"><span data-stu-id="c2ade-133">See where the apps people are using are by geographical location by using the **Apps headquarters location** map.</span></span> 
    
6. <span data-ttu-id="c2ade-p104">Sehen Sie über dem Bereich Maps sich die Risiko Bewertung der erkannten apps in der Übersicht über die **Risikoebenen** . Sie können betrachten Sie Risiken nach den Gruppen und Kategorien, die Sie im Bereich **ermittelte apps** verwendet. Beispielsweise können Sie sehen, wie viel Datenverkehr in jeder Gruppierung hoch, Mittel oder niedrig riskante apps stammt.</span><span class="sxs-lookup"><span data-stu-id="c2ade-p104">Above the maps area, take a look at the risk score of the discovered apps in the **Risk levels** overview. You can look at risks by the same groups and categories that you used in the **Discovered apps** area. For example, you can see how much traffic in each grouping is from high, medium, or low risk apps.</span></span> 
    
## <a name="dive-deeper-into-the-information"></a><span data-ttu-id="c2ade-137">Detaillierte Informationen zu der information</span><span class="sxs-lookup"><span data-stu-id="c2ade-137">Dive deeper into the information</span></span>

<span data-ttu-id="c2ade-138">Cloud-Erkennung können Sie um einen genaueren Einblick in apps, Unterdomänen, IP-Adressen und Benutzer zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="c2ade-138">You can use Cloud Discovery to take a deeper look at apps, subdomains, IP addresses, and users.</span></span>
  
1. <span data-ttu-id="c2ade-139">Wählen Sie in der Cloud-Discovery-Dashboard der Registerkarte **ermittelte apps** .</span><span class="sxs-lookup"><span data-stu-id="c2ade-139">In the Cloud Discovery dashboard, choose the **Discovered apps** tab.</span></span> 
    
2. <span data-ttu-id="c2ade-140">Verwenden Sie den Abschnitt Filter, um apps nach Name, Kategorie, Auslastung oder Datum der letzten gesehen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c2ade-140">Use the filters section to view apps by name, category, usage level, or last seen date.</span></span>
    
3. <span data-ttu-id="c2ade-141">Zeigen Sie in der Liste der Ergebnisse durch eine app-Name auf den Link **Anzeigen Unterdomänen** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c2ade-141">In the list of results, hover by an app name to reveal the **View sub-domains** link.</span></span> 
    
    ![Bewegen Sie den Mauszeiger neben einer app aus, um einen Link zur Detailansicht Unterdomäne anzuzeigen](media/4a212215-8a2c-46fd-9ef9-89e4064658a6.png)
  
    <span data-ttu-id="c2ade-143">Ausführliche Informationen über die gewählte app wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c2ade-143">Detailed information about the selected app will appear.</span></span>
    
4. <span data-ttu-id="c2ade-144">Um Details zu IP-Adressen anzuzeigen, wählen Sie die Registerkarte **IP-Adressen** .</span><span class="sxs-lookup"><span data-stu-id="c2ade-144">To view details about IP addresses, choose the **IP addresses** tab.</span></span> 
    
    ![Cloud-Discovery zeigt detaillierte Informationen zu IP-Adressen](media/0c742bf6-da9e-4d22-8656-a27a5007d5d5.png)
  
    <span data-ttu-id="c2ade-146">Wählen Sie in der Liste der Ergebnisse eine einzelne IP-Adresse Ausführlichere Informationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c2ade-146">In the list of results, select an individual IP address to view more detailed information.</span></span>
    
5. <span data-ttu-id="c2ade-147">Um Details zu Office 365-Benutzer in Ihrer Organisation anzuzeigen, wählen Sie die Registerkarte **Benutzer** .</span><span class="sxs-lookup"><span data-stu-id="c2ade-147">To view details about Office 365 users within your organization, choose the **Users** tab.</span></span> 
    
    ![Cloud-Discovery - Benutzer-info](media/2d9c2d85-01e6-4057-8020-d9a68f26bbac.png)
  
## <a name="exclude-entities"></a><span data-ttu-id="c2ade-149">Ausschließen von Entitäten</span><span class="sxs-lookup"><span data-stu-id="c2ade-149">Exclude entities</span></span>

<span data-ttu-id="c2ade-150">Sie können bestimmte Benutzer oder die IP-Adressen, um auf bestimmte Informationen konzentrieren ausschließen.</span><span class="sxs-lookup"><span data-stu-id="c2ade-150">You can exclude certain system users or IP addresses in order to focus on more specific information.</span></span>
  
1. <span data-ttu-id="c2ade-151">**Auswählen von** \> **Cloud Discovery-Einstellungen**.</span><span class="sxs-lookup"><span data-stu-id="c2ade-151">Choose **Settings** \> **Cloud Discovery settings**.</span></span>
    
2. <span data-ttu-id="c2ade-152">Wählen Sie die **Entitäten ausschließen**.</span><span class="sxs-lookup"><span data-stu-id="c2ade-152">Choose **Exclude entities**.</span></span>
    
3. <span data-ttu-id="c2ade-153">Wählen Sie **Ausgeschlossene Benutzer** oder **Ausgeschlossene IP-Adressen**.</span><span class="sxs-lookup"><span data-stu-id="c2ade-153">Choose either **Excluded users** or **Excluded IP addresses**.</span></span>
    
4. <span data-ttu-id="c2ade-154">Geben Sie den Benutzer oder die IP-Adressen, und geben Sie in das Feld **Kommentare** Informationen, warum Sie die Benutzer oder die IP-Adressen ausschließen.</span><span class="sxs-lookup"><span data-stu-id="c2ade-154">Specify the users or IP addresses, and in the **Comments** box, type information about why you are excluding those users or IP addresses.</span></span> 
    
5. <span data-ttu-id="c2ade-155">Wählen Sie **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c2ade-155">Choose **Add**.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="c2ade-156">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c2ade-156">Next steps</span></span>

- [<span data-ttu-id="c2ade-157">Lesen und Ausführen einer Aktion Warnungen</span><span class="sxs-lookup"><span data-stu-id="c2ade-157">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="c2ade-158">Erstellen von Berichten für app-Ermittlung</span><span class="sxs-lookup"><span data-stu-id="c2ade-158">Create app discovery reports</span></span>](create-app-discovery-reports-in-ocas.md)
    
- <span data-ttu-id="c2ade-159">Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="c2ade-159">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

