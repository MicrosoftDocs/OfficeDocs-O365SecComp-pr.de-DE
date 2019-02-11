---
title: Erstellen von App-Ermittlungsberichten mit Office 365 Cloud App Security
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
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Erstellen von Berichten mit Office 365 Cloud App-Sicherheit, mit denen Sie zu verstehen, wie Benutzern in Ihrer Organisation Office 365 und andere apps verwendet werden.
ms.openlocfilehash: 543a194ec9d441a4feea97b8ad49022094565d7a
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "29603716"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="e80c0-103">Erstellen von App-Ermittlungsberichten mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="e80c0-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

<span data-ttu-id="e80c0-104">Office 365 Advanced Security Management ist jetzt Office 365-Cloud-App-Sicherheit.</span><span class="sxs-lookup"><span data-stu-id="e80c0-104">Office 365 Advanced Security Management is now Office 365 Cloud App Security.</span></span>
  
|<span data-ttu-id="e80c0-105">Auswertung **\>**</span><span class="sxs-lookup"><span data-stu-id="e80c0-105">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="e80c0-106">Planen der **\>**</span><span class="sxs-lookup"><span data-stu-id="e80c0-106">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="e80c0-107">Bereitstellung **\>**</span><span class="sxs-lookup"><span data-stu-id="e80c0-107">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="e80c0-108">Auslastung \*\*\*</span><span class="sxs-lookup"><span data-stu-id="e80c0-108">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="e80c0-109">Starten Sie auswerten</span><span class="sxs-lookup"><span data-stu-id="e80c0-109">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="e80c0-110">Starten der Planung</span><span class="sxs-lookup"><span data-stu-id="e80c0-110">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="e80c0-111">Starten Sie Bereitstellen von</span><span class="sxs-lookup"><span data-stu-id="e80c0-111">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="e80c0-112">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="e80c0-112">You are here!</span></span>  <br/> [<span data-ttu-id="e80c0-113">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e80c0-113">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="e80c0-p101">Office 365-Cloud-App-Sicherheit können globale Administratoren Sicherheitsadministratoren und Sicherheit Leser Einblick in die Clouddienste, die Benutzern in einer Organisation verwendet werden. Beispielsweise können Sie sehen, in dem Benutzer speichern und Zusammenarbeit an Dokumenten und wie viele Daten hochgeladen werden, apps oder Diensten, die außerhalb von Office 365 sind.</span><span class="sxs-lookup"><span data-stu-id="e80c0-p101">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using. For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="e80c0-116">Um ein app-Discovery-Bericht generiert werden soll, Sie die Protokolldateien für Web-Datenverkehr vom Firewalls und -Proxys manuell hochladen, und klicken Sie dann Office 365-Cloud-App-Sicherheit analysiert und analysiert die Dateien für den Bericht.</span><span class="sxs-lookup"><span data-stu-id="e80c0-116">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e80c0-p102">Sie müssen ein globaler Administrator Sicherheitsadministrator oder Sicherheit Reader zum Ausführen der Aufgaben in diesem Artikel beschriebenen sein. Weitere Informationen finden Sie unter [Berechtigungen in der Office 365-Sicherheit &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="e80c0-p102">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article. To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="e80c0-119">Erstellen eines Berichts mit app-Ermittlung</span><span class="sxs-lookup"><span data-stu-id="e80c0-119">Create a report with app discovery</span></span>

<span data-ttu-id="e80c0-120">Um ein app-Discovery-Bericht erstellen, geben Sie die Hersteller-Datenquelle für die Protokolldateien, die Sie analysiert haben, wählen die Protokolldateien, und klicken Sie dann den Bericht anfordern möchten.</span><span class="sxs-lookup"><span data-stu-id="e80c0-120">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e80c0-121">Verwenden Sie die Web-Datenverkehr-Protokolldateien, die Zeiten, in denen die optimale Darstellung der Verwendung in Ihrer Organisation zu erhalten, um Datenverkehr enthalten.</span><span class="sxs-lookup"><span data-stu-id="e80c0-121">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="e80c0-122">Erfassen Sie Ihre [Web-Datenverkehr Protokolle und Datenquellen für Office 365-Cloud-App-Sicherheit](web-traffic-logs-and-data-sources-for-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="e80c0-122">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="e80c0-123">Klicken Sie auf das Portal Cloud App-Sicherheit ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) und zur Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="e80c0-123">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> 
       
3. <span data-ttu-id="e80c0-124">Wählen Sie **Discover** \> **erstellt einen neuen Bericht**.</span><span class="sxs-lookup"><span data-stu-id="e80c0-124">Choose **Discover** \> **Create new report**.</span></span> <br><span data-ttu-id="e80c0-125">![Wählen Sie im Office 365 CAS-Portal Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span><span class="sxs-lookup"><span data-stu-id="e80c0-125">![In the Office 365 CAS portal, choose Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span></span><br>
  
4. <span data-ttu-id="e80c0-126">Geben Sie einen Namen und eine Beschreibung für den Bericht, und wählen Sie dann die Datenquelle für die Web-Datenverkehr Protokolle in der Liste **Datenquelle** aus.</span><span class="sxs-lookup"><span data-stu-id="e80c0-126">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> <br><span data-ttu-id="e80c0-127">![Wählen Sie in Office 365-CAS Discover \> erstellen neuen Bericht](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span><span class="sxs-lookup"><span data-stu-id="e80c0-127">![In O365 CAS, choose Discover \> Create new report](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span></span><br><span data-ttu-id="e80c0-p103">Wenn eine Datenquelle, die Sie verwenden möchten, nicht aufgeführt ist, können Sie anfordern, dass er hinzugefügt werden. Wählen Sie **andere** für die **Datenquelle**aus, und geben Sie den Namen der Datenquelle, die Sie hochladen möchten. Wir überprüfen Sie das Protokoll und informiert Sie, wenn die Unterstützung für die Datenquelle hinzugefügt werden, die es generiert.</span><span class="sxs-lookup"><span data-stu-id="e80c0-p103">If a data source that you'd like to use is not listed, you can request that it be added. Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload. We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
5. <span data-ttu-id="e80c0-p104">Navigieren Sie zum Speicherort der Protokolldateien, die Sie gesammelt, und wählen Sie die Dateien. Die Protokolldateien müssen von der Datenquelle erstellt worden sein, die Sie für den Bericht ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="e80c0-p104">Browse to the location of the log files you collected and select the files. The log files must have been generated by the data source that you chose for the report.</span></span>
    
6. <span data-ttu-id="e80c0-133">Klicken Sie auf **Erstellen** , um dem Bericht erstellen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e80c0-133">Click **Create** to start the report creation process.</span></span> 
    
7. <span data-ttu-id="e80c0-p105">Um den Status des Berichts angezeigt wird, klicken Sie auf **die Momentaufnahme Berichte verwalten**. Wenn ein Bericht bereit ist, sehen Sie die Option **Bericht anzeigen** .</span><span class="sxs-lookup"><span data-stu-id="e80c0-p105">To see the status of the report, click **Manage snapshot reports**. When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="e80c0-136">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e80c0-136">Next steps</span></span>

- [<span data-ttu-id="e80c0-137">Lesen und Ausführen einer Aktion Warnungen</span><span class="sxs-lookup"><span data-stu-id="e80c0-137">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="e80c0-138">Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="e80c0-138">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="e80c0-139">Überprüfen der [Auslastung Aktivitäten für Office 365-Cloud-App-Sicherheit](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="e80c0-139">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

