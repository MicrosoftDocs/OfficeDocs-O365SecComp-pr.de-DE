---
title: Set analyze Advanced Settings in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: a797682f-ad85-4c08-a354-3850ba2237ee
description: 'In diesem Artikel erfahren Sie, wie Sie erweiterte Einstellungen wie near-Duplicates, e-Mail-Threads und Designs für den Analyseprozess in Office 365 Advanced eDiscovery konfigurieren. '
ms.openlocfilehash: d8dfb9f3ecfcda0f267dfccdc716eda40fe450b2
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32260858"
---
# <a name="set-analyze-advanced-settings-in-office-365-advanced-ediscovery"></a><span data-ttu-id="483db-103">Set analyze Advanced Settings in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="483db-103">Set Analyze advanced settings in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="483db-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="483db-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="483db-106">Advanced eDiscovery bietet erweiterte Standardparameter für die Analyse von Modul Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="483db-106">Advanced eDiscovery provides default advanced parameters for Analyze module settings.</span></span> <span data-ttu-id="483db-107">Im folgenden Verfahren werden Einstellungen beschrieben, die angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="483db-107">The following procedure describes settings that can be specified.</span></span>
  
1. <span data-ttu-id="483db-108">Klicken Sie auf der Registerkarte **Setup Analyse \> \> vorbereiten** auf **Erweiterte Einstellungen** (am unteren Rand der Seite).</span><span class="sxs-lookup"><span data-stu-id="483db-108">In the **Prepare \> Analyze \> Setup** tab, click **Advanced settings** (at the bottom of the page).</span></span> <span data-ttu-id="483db-109">Der folgende Bereich wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="483db-109">The following panel is displayed.</span></span> 
    
    ![Erweiterte Einstellungen für ANALYZE festlegen](media/c9ea3017-e19a-456b-a742-c3d07121a3f6.png)
  
2. <span data-ttu-id="483db-111">Wählen Sie in den **Parametern near-Duplicates und Email Threads**die folgenden Werte aus:</span><span class="sxs-lookup"><span data-stu-id="483db-111">In **Near-duplicates and Email threads parameters**, select values for the following as necessary:</span></span>
    
  - <span data-ttu-id="483db-112">**Mindestanzahl von Wörtern**: Mindestanzahl für Wörter, unter der eine Datei nicht für die nahezu doppelt vorhandene Analyse übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="483db-112">**Minimum number of words**: Minimum number for words, below which a file is not submitted for Near-duplicate analysis.</span></span> 
    
  - <span data-ttu-id="483db-113">**Maximale Anzahl von Wörtern**: maximale Anzahl für Wörter, über die eine Datei nicht für die nahezu doppelt vorhandene Analyse übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="483db-113">**Maximum number of words**: Maximum number for words, above which a file is not submitted for Near-duplicate analysis.</span></span>
    
  - <span data-ttu-id="483db-114">**E-Mail-Ähnlichkeit**: minimale Ähnlichkeits Stufe für zwei e-Mails, die als ähnlich betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="483db-114">**Email similarity**: Minimal level of resemblance for two emails to be considered similar.</span></span> <span data-ttu-id="483db-115">Der Wert ist immer gleich oder größer als die Dokument Ähnlichkeit.</span><span class="sxs-lookup"><span data-stu-id="483db-115">Value is always equal to, or larger than document similarity.</span></span> <span data-ttu-id="483db-116">Der Standardwert ist 90%.</span><span class="sxs-lookup"><span data-stu-id="483db-116">Default is 90%.</span></span>
    
3. <span data-ttu-id="483db-117">Aktivieren Sie unter **Designs-Parameter**das Kontrollkästchen **Zahlen in Design Analyse einbeziehen** , um Zahlen bei der Verarbeitung von Designs während der Analyse einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="483db-117">In **Themes parameters**, select the **Include numbers in theme analysis** check box to include numbers in the processing of Themes during Analyze.</span></span> 
    
4. <span data-ttu-id="483db-118">Klicken Sie auf **Speichern**.</span><span class="sxs-lookup"><span data-stu-id="483db-118">Click **Save**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="483db-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="483db-119">See also</span></span>

[<span data-ttu-id="483db-120">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="483db-120">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="483db-121">Grundlegendes zur Dokument Ähnlichkeit</span><span class="sxs-lookup"><span data-stu-id="483db-121">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="483db-122">Festlegen von Analyseoptionen</span><span class="sxs-lookup"><span data-stu-id="483db-122">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="483db-123">Festlegen des Texts ignorieren</span><span class="sxs-lookup"><span data-stu-id="483db-123">Setting ignore text</span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="483db-124">Anzeigen von Analyseergebnissen</span><span class="sxs-lookup"><span data-stu-id="483db-124">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

