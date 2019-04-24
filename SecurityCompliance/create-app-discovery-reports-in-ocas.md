---
title: Erstellen von App-Ermittlungsberichten mit Office 365 Cloud App Security
ms.author: deniseb
author: denisebmsft
manager: laurawi
ms.date: 1/28/2019
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
- MOE150
ms.assetid: 3e68e691-1fc4-4d3e-a2c0-d3134eb64055
description: Erstellen Sie Berichte mit Office 365 Cloud App Security, mit denen Sie verstehen können, wie Personen in Ihrer Organisation Office 365 und andere apps verwenden.
ms.openlocfilehash: 23165a52a09e5bcde46ee3ab2110dc17d0faf7f4
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32259638"
---
# <a name="create-app-discovery-reports-using-office-365-cloud-app-security"></a><span data-ttu-id="495e8-103">Erstellen von App-Ermittlungsberichten mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="495e8-103">Create app discovery reports using Office 365 Cloud App Security</span></span>

|<span data-ttu-id="495e8-104">Auswertung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="495e8-104">\*\*\*\*Evaluation\*\* \>\*\*</span></span>|<span data-ttu-id="495e8-105">Planung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="495e8-105">\*\*\*\*Planning\*\* \>\*\*</span></span>|<span data-ttu-id="495e8-106">Bereitstellung \* *\>*\*</span><span class="sxs-lookup"><span data-stu-id="495e8-106">\*\*\*\*Deployment\*\* \>\*\*</span></span>|<span data-ttu-id="495e8-107">Auslastung \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="495e8-107">\*\*\*\*Utilization\*\*\*\*</span></span>|
|:-----|:-----|:-----|:-----|
|[<span data-ttu-id="495e8-108">Evaluierung starten</span><span class="sxs-lookup"><span data-stu-id="495e8-108">Start evaluating</span></span>](office-365-cas-overview.md) <br/> |[<span data-ttu-id="495e8-109">Planung starten</span><span class="sxs-lookup"><span data-stu-id="495e8-109">Start planning</span></span>](get-ready-for-office-365-cas.md) <br/> |[<span data-ttu-id="495e8-110">Starten der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="495e8-110">Start deploying</span></span>](turn-on-office-365-cas.md) <br/> |<span data-ttu-id="495e8-111">Sie sind hier!</span><span class="sxs-lookup"><span data-stu-id="495e8-111">You are here!</span></span>  <br/> [<span data-ttu-id="495e8-112">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="495e8-112">Next steps</span></span>](#next-steps) <br/> |
   
<span data-ttu-id="495e8-113">Office 365 Cloud App Security unterstützt globale Administratoren, Sicherheitsadministratoren und Sicherheits Leser bei der Nutzung von Cloud-Diensten, die in einer Organisation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="495e8-113">Office 365 Cloud App Security helps global administrators, security administrators, and security readers gain insight into the cloud services people in an organization are using.</span></span> <span data-ttu-id="495e8-114">So können Sie beispielsweise sehen, wo Benutzer Dokumente speichern und zusammenarbeiten und wie viele Daten in Apps oder Dienste hochgeladen werden, die sich außerhalb von Office 365 befinden.</span><span class="sxs-lookup"><span data-stu-id="495e8-114">For example, you can see where users are storing and collaborating on documents and how much data is being uploaded to apps or services that are outside of Office 365.</span></span>
  
<span data-ttu-id="495e8-115">Wenn Sie einen app-Ermittlungsbericht generieren möchten, laden Sie Ihre Webprotokolldateien manuell aus Ihren Firewalls und Proxys hoch, und anschließend werden die Dateien für Ihren Bericht von der Office 365 Cloud App Security analysiert und analysiert.</span><span class="sxs-lookup"><span data-stu-id="495e8-115">To generate an app discovery report, you manually upload your web traffic log files from your firewalls and proxies, and then Office 365 Cloud App Security parses and analyzes those files for your report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="495e8-116">Sie müssen ein globaler Administrator, Sicherheitsadministrator oder Sicherheits Leser sein, um die in diesem Artikel beschriebenen Aufgaben ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="495e8-116">You must be a global administrator, security administrator, or security reader to perform the tasks described in this article.</span></span> <span data-ttu-id="495e8-117">Weitere Informationen finden Sie unter [Permissions in the Office 365 &amp; Security Compliance Center](permissions-in-the-security-and-compliance-center.md).</span><span class="sxs-lookup"><span data-stu-id="495e8-117">To learn more, see [Permissions in the Office 365 Security &amp; Compliance Center](permissions-in-the-security-and-compliance-center.md).</span></span> 
  
## <a name="create-a-report-with-app-discovery"></a><span data-ttu-id="495e8-118">Erstellen eines Berichts mit der APP-Ermittlung</span><span class="sxs-lookup"><span data-stu-id="495e8-118">Create a report with app discovery</span></span>

<span data-ttu-id="495e8-119">Wenn Sie einen app-Ermittlungsbericht erstellen möchten, identifizieren Sie die Herstellerdaten Quelle für die Protokolldateien, die Sie analysieren möchten, wählen Sie die Protokolldateien aus, und fordern Sie den Bericht an.</span><span class="sxs-lookup"><span data-stu-id="495e8-119">To create an app discovery report, you identify the vendor data source for the log files that you want to have analyzed, select the log files, and then request the report.</span></span>
  
> [!NOTE]
> <span data-ttu-id="495e8-120">Verwenden Sie Webdatenverkehr-Protokolldateien, die Spitzenauslastungszeiten enthalten, um die optimale Darstellung der Nutzung in Ihrer Organisation zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="495e8-120">Use web traffic log files that include peak traffic periods to get the best representation of usage in your organization.</span></span> 
  
1. <span data-ttu-id="495e8-121">Sammeln Sie Ihre [Webtraffic-Protokolle und Datenquellen für Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span><span class="sxs-lookup"><span data-stu-id="495e8-121">Collect your [web traffic logs and data sources for Office 365 Cloud App Security](web-traffic-logs-and-data-sources-for-ocas.md).</span></span>
    
2. <span data-ttu-id="495e8-122">Wechseln Sie zum Cloud App Security Portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)), und melden Sie sich an.</span><span class="sxs-lookup"><span data-stu-id="495e8-122">Go to the Cloud App Security portal ([https://portal.cloudappsecurity.com](https://portal.cloudappsecurity.com)) and sign in.</span></span> 
       
3. <span data-ttu-id="495e8-123">Wählen Sie **Discover** \> **Create New Report**aus.</span><span class="sxs-lookup"><span data-stu-id="495e8-123">Choose **Discover** \> **Create new report**.</span></span> <br><span data-ttu-id="495e8-124">![Wählen Sie im Office 365-CAS-Portal Discover aus.](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span><span class="sxs-lookup"><span data-stu-id="495e8-124">![In the Office 365 CAS portal, choose Discover](media/73b5299f-94b5-49dd-a00f-154d188eb2c5.png)</span></span><br>
  
4. <span data-ttu-id="495e8-125">Geben Sie einen Namen und eine Beschreibung für den Bericht an, und wählen Sie dann in der Liste **Datenquelle** die Datenquelle für die Webdatenverkehr aus.</span><span class="sxs-lookup"><span data-stu-id="495e8-125">Specify a name and description for your report, and then select the data source for your web traffic logs in the **Data source** list.</span></span> <br><span data-ttu-id="495e8-126">![Wählen Sie in O365-CAS \> die Option Discover Create New Report aus.](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span><span class="sxs-lookup"><span data-stu-id="495e8-126">![In O365 CAS, choose Discover \> Create new report](media/22e660f0-5eb2-49fa-9fea-f88a5809a07b.png)</span></span><br><span data-ttu-id="495e8-127">Wenn eine Datenquelle, die Sie verwenden möchten, nicht aufgeführt wird, können Sie diese hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="495e8-127">If a data source that you'd like to use is not listed, you can request that it be added.</span></span> <span data-ttu-id="495e8-128">Wählen Sie **andere** für **Datenquelle**aus, und geben Sie dann den Namen der Datenquelle ein, die Sie hochladen möchten.</span><span class="sxs-lookup"><span data-stu-id="495e8-128">Select **Other** for **Data source**, and then type the name of the data source that you're trying to upload.</span></span> <span data-ttu-id="495e8-129">Wir überarbeiten das Protokoll und informieren Sie, ob die Unterstützung für die Datenquelle hinzugefügt wird, die Sie generiert hat.</span><span class="sxs-lookup"><span data-stu-id="495e8-129">We'll review the log, and let you know if we add support for the data source that generated it.</span></span> 
  
5. <span data-ttu-id="495e8-130">Navigieren Sie zum Speicherort der gesammelten Protokolldateien, und wählen Sie die Dateien aus.</span><span class="sxs-lookup"><span data-stu-id="495e8-130">Browse to the location of the log files you collected and select the files.</span></span> <span data-ttu-id="495e8-131">Die Protokolldateien müssen von der Datenquelle generiert worden sein, die Sie für den Bericht ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="495e8-131">The log files must have been generated by the data source that you chose for the report.</span></span>
    
6. <span data-ttu-id="495e8-132">Klicken Sie auf **Erstellen** , um den Berichterstellungsprozess zu starten.</span><span class="sxs-lookup"><span data-stu-id="495e8-132">Click **Create** to start the report creation process.</span></span> 
    
7. <span data-ttu-id="495e8-133">Klicken Sie auf **Snapshot-Berichte verwalten**, um den Status des Berichts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="495e8-133">To see the status of the report, click **Manage snapshot reports**.</span></span> <span data-ttu-id="495e8-134">Wenn ein Bericht fertig ist, wird die Option **Bericht anzeigen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="495e8-134">When a report is ready, you'll see the **View report** option.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="495e8-135">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="495e8-135">Next steps</span></span>

- [<span data-ttu-id="495e8-136">Überarbeiten und Aktionen für Warnungen</span><span class="sxs-lookup"><span data-stu-id="495e8-136">Review and take action on alerts</span></span>](review-office-365-cas-alerts.md)
    
- [<span data-ttu-id="495e8-137">Erstellen von App-Ermittlungsergebnissen mit Office 365 Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="495e8-137">Review app discovery findings in Office 365 Cloud App Security</span></span>](review-app-discovery-findings-in-ocas.md)
    
- <span data-ttu-id="495e8-138">Überwachen Ihrer [Nutzungsaktivitäten für Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span><span class="sxs-lookup"><span data-stu-id="495e8-138">Review your [utilization activities for Office 365 Cloud App Security](utilization-activities-for-ocas.md)</span></span>
    

