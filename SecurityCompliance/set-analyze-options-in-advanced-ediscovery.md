---
title: Festlegen von Analyseoptionen in Office 365 Advanced eDiscovery
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
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Lesen Sie die Schritte zum Einrichten von Optionen für den Analyseprozess in Office 365 Advanced eDiscovery, einschließlich near-Duplicates, e-Mail-Threads und Designs.  '
ms.openlocfilehash: 12bbe4043803c165a58adac80b72d03afd48adc7
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218225"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="9d455-103">Festlegen von Analyseoptionen in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9d455-103">Set Analyze options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="9d455-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="9d455-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="9d455-106">Legen Sie in Advanced eDiscovery die Analyseoptionen vor dem Durchführen von ANALYZE fest.</span><span class="sxs-lookup"><span data-stu-id="9d455-106">In Advanced eDiscovery, set the Analyze options prior to running Analyze.</span></span>
  
## <a name="set-analyze-options"></a><span data-ttu-id="9d455-107">Festlegen von Analyseoptionen</span><span class="sxs-lookup"><span data-stu-id="9d455-107">Set Analyze options</span></span>

<span data-ttu-id="9d455-p102">Öffnen **Sie \> Prepare analyze** \> **Setup**. Das folgende Fenster wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d455-p102">Open **Prepare \> Analyze** \> **Setup**. The following window is displayed.</span></span>
  
![Analyseoptionen festlegen](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 <span data-ttu-id="9d455-p103">**Near-Duplikate und e-Mail-Threads** Aktivieren Sie dieses Kontrollkästchen, wenn Sie die Analyse ausführen möchten. Sie ist standardmäßig ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9d455-p103">**Near-duplicates and email threads** Check this box if you want to run the analysis. It is selected by default.</span></span> 
  
 <span data-ttu-id="9d455-113">**Dokument Ähnlichkeit** Geben Sie den Schwellenwert für Near-Duplicates ein, oder übernehmen Sie den Standard von 65%.</span><span class="sxs-lookup"><span data-stu-id="9d455-113">**Document similarity**Enter the Near-duplicates threshold value or accept the default of 65%.</span></span> 
  
 <span data-ttu-id="9d455-p104">**Designs** Aktivieren Sie dieses Kontrollkästchen, um alle Dateien zu verarbeiten und Ihnen Designs zuzuweisen. Dieses Kontrollkästchen ist standardmäßig nicht aktiviert. Geben Sie die folgenden Optionen ein, wenn Sie die Bearbeitung von Designs durchführen möchten.</span><span class="sxs-lookup"><span data-stu-id="9d455-p104">**Themes**Check this box to process all files and assign themes to them. By default, this check box is not selected. Enter the following options if you want to perform Themes processing.</span></span>
  
- <span data-ttu-id="9d455-p105">**Maximale Anzahl von Designs** Geben Sie einen Wert für die Anzahl der zu erstellende Designs ein, oder wählen Sie ihn aus. Der Standardwert ist 200.</span><span class="sxs-lookup"><span data-stu-id="9d455-p105">**Max number of themes**Enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="9d455-p106">Das Erhöhen der Anzahl von Designs wirkt sich auf die Leistung und die Möglichkeit, ein Design zu verallgemeinern. Je höher die Anzahl der Designs ist, desto detaillierter sind Sie. Wenn beispielsweise ein Satz von 50 Designs ein Design wie "Basketball, Spurs, Clippers, Lakers" enthält, 300 Designs können separate Designs aufweisen: "Spurs", "Clippers", "Lakers". Wenn Sie kein Bewusstsein für das Thema "Basketball" hatten und dieses Feature für ECA verwenden, könnte das Thema "Basketball" nützlich sein. Aber wenn die Verarbeitung zu viele Designs hatte, werden Sie möglicherweise nie das Wort "Basketball" sehen und wissen möglicherweise nicht, dass Spurs und Clippers gute Basketball Designs sind, anstatt Elemente, die auf Stiefel gehen und für Haare verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d455-p106">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
- <span data-ttu-id="9d455-p107">**Vorgeschlagene Designs** Sie können Design Wörter vorschlagen, um die Verarbeitung von Designs zu steuern. Advanced eDiscovery konzentriert sich auf diese vorgeschlagenen Wörter und versucht, ein oder mehrere relevante Designs basierend auf den Einstellungen für "maximale Anzahl von Designs" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9d455-p107">**Suggested themes**You can suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="9d455-p108">Wenn das vorgeschlagene Wort beispielsweise "Computer" lautet und Sie "2" als "maximale Anzahl von Designs" angegeben haben, versucht Advanced eDiscovery, zwei Designs zu generieren, die sich auf das Wort "Computer" beziehen. Die beiden Designs können beispielsweise "Computer Software" und "Computer Hardware" sein.</span><span class="sxs-lookup"><span data-stu-id="9d455-p108">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span> 
    
    ![Vorgeschlagenes Design hinzufügen](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. <span data-ttu-id="9d455-129">Klicken Sie auf **ändern**, um vorgeschlagene Designs anzuzeigen, hinzuzufügen oder zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9d455-129">To view, add, or edit suggested themes, click **Modify**.</span></span>
    
2. <span data-ttu-id="9d455-p109">Klicken Sie im Bereich **vorgeschlagene Designs** auf das \*\*\*\*![Symbol hinzufügen](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) Symbol hinzufügen, um ein Design hinzuzufügen. Fügen Sie im Bereich **vorgeschlagene Design hinzufügen** die Wörter durch Kommata getrennt hinzu.</span><span class="sxs-lookup"><span data-stu-id="9d455-p109">In the **Suggested themes** panel, click the **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icon to add a theme. In the **Add suggested theme** panel, add the words, separated by commas.</span></span> 
    
3. <span data-ttu-id="9d455-132">Wählen Sie unter **Anzahl der Designs**einen Wert aus, um die Anzahl der Designs zu ermitteln, die die erweiterte eDiscovery für diese Wörter generieren soll (standardmäßig 1 Design).</span><span class="sxs-lookup"><span data-stu-id="9d455-132">In **Number of themes**, select a value to determine the number of themes Advanced eDiscovery will try to generate for these words (default is 1 theme).</span></span>
    
4. <span data-ttu-id="9d455-133">Klicken Sie auf **Speichern** , und schließen Sie dann den Dialog.</span><span class="sxs-lookup"><span data-stu-id="9d455-133">Click **Save** and then close the dialogue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="9d455-p110">Die Gesamtzahl der Designs enthält vorgeschlagene Designs. Die insgesamt vorgeschlagenen Designs dürfen die Gesamtdesigns nicht überschreiten. Wenn es viele vorgeschlagene Designs im Verhältnis zu den Gesamtdesigns gibt, werden nur einige "Roman"-Designs vom System erkannt, da die meisten der Designs für vorgeschlagene Designs vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="9d455-p110">The total number of themes includes Suggested Themes. The total Suggested Themes cannot exceed the total themes. If there are many Suggested Themes relative to the total themes, only a few "novel" themes will be detected by the system because most of the themes will be dedicated to Suggested Themes.</span></span> 
  
- <span data-ttu-id="9d455-137">**Modus** Wählen Sie in der Dropdownliste eine **Designs** -Option aus:</span><span class="sxs-lookup"><span data-stu-id="9d455-137">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="9d455-138">**Modell erstellen und anwenden**: berechnet Designs anhand von Modellen aus einem Segment der Dateien und verteilt dann Dateien darunter.</span><span class="sxs-lookup"><span data-stu-id="9d455-138">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="9d455-p111">**Modell erstellen**: berechnet ein Design Modell aus einem Segment der Dateien. Der Prozess der Aufteilung von Dateien erfolgt separat zu einem anderen Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="9d455-p111">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="9d455-p112">**Modell anwenden**: diese Option wird nur angezeigt, wenn ein Modell zuvor erstellt und noch nicht angewendet wurde. Dadurch werden die Dateien basierend auf den Designs unterteilt.</span><span class="sxs-lookup"><span data-stu-id="9d455-p112">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
<span data-ttu-id="9d455-143">Sie können auch [Text ignorieren festlegen](set-ignore-text-in-advanced-ediscovery.md) und [Erweiterte Einstellungen](set-analyze-advanced-settings-in-advanced-ediscovery.md) für analyze analysieren festlegen.</span><span class="sxs-lookup"><span data-stu-id="9d455-143">You can also [set ignore text](set-ignore-text-in-advanced-ediscovery.md) and [set Analyze advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for Analyze.</span></span> 
  
<span data-ttu-id="9d455-p113">Nachdem Sie diese Optionen festgelegt haben, klicken Sie auf **analyze** to Run. Die [Ansicht Analyseergebnisse](view-analyze-results-in-advanced-ediscovery.md) werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d455-p113">After you've set these options, click **Analyze** to run. [View Analyze results](view-analyze-results-in-advanced-ediscovery.md) are displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9d455-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d455-146">See also</span></span>

[<span data-ttu-id="9d455-147">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9d455-147">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="9d455-148">Grundlegendes zur Dokument Ähnlichkeit</span><span class="sxs-lookup"><span data-stu-id="9d455-148">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9d455-149">Text ignorieren festlegen</span><span class="sxs-lookup"><span data-stu-id="9d455-149">Set Ignore text </span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9d455-150">Analysieren erweiterter Einstellungen festlegen</span><span class="sxs-lookup"><span data-stu-id="9d455-150">Set Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="9d455-151">Ergebnisse analysieren</span><span class="sxs-lookup"><span data-stu-id="9d455-151">View Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

