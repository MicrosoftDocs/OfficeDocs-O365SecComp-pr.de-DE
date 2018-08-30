---
title: Festlegen von Optionen für die Analyse in Office 365 erweiterte eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
ms.audience: Admin
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: f6cd6588-f6b6-424a-a9ab-3782b842faee
description: 'Überprüfen Sie die Schritte zum Einrichten von Optionen für die Analyse-Prozess in Office 365 erweiterte eDiscovery, einschließlich in Ihrer Nähe Duplikate, e-Mail-Threads und Designs.  '
ms.openlocfilehash: a0ebbadb180321a3094cb1056ed8e0e6500ee66a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529442"
---
# <a name="set-analyze-options-in-office-365-advanced-ediscovery"></a><span data-ttu-id="eec6a-103">Festlegen von Optionen für die Analyse in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="eec6a-103">Set Analyze options in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="eec6a-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="eec6a-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="eec6a-106">Erweiterte eDiscovery legen Sie die Optionen Analyse vor dem Ausführen der Analyse.</span><span class="sxs-lookup"><span data-stu-id="eec6a-106">In Advanced eDiscovery, set the Analyze options prior to running Analyze.</span></span>
  
## <a name="set-analyze-options"></a><span data-ttu-id="eec6a-107">Festlegen von Optionen für die Analyse</span><span class="sxs-lookup"><span data-stu-id="eec6a-107">Set Analyze options</span></span>

<span data-ttu-id="eec6a-p102">Open **Vorbereiten \> analysieren** \> **Setup**. Das folgende Fenster wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p102">Open **Prepare \> Analyze** \> **Setup**. The following window is displayed.</span></span>
  
![Analyseoptionen festlegen](media/c3ec7a92-8484-4812-b98c-aa3eb740e5b7.png)
  
 <span data-ttu-id="eec6a-p103">**In Ihrer Nähe Duplikate und e-Mail-Threads** Aktivieren Kontrollkästchen Sie dieses, wenn Sie die Analyse ausführen möchten. Es ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p103">**Near-duplicates and email threads** Check this box if you want to run the analysis. It is selected by default.</span></span> 
  
 <span data-ttu-id="eec6a-113">**Dokument Ähnlichkeit** Geben Sie den Schwellenwert Near-Duplikate, oder übernehmen Sie den Standardwert von 65 %.</span><span class="sxs-lookup"><span data-stu-id="eec6a-113">**Document similarity**Enter the Near-duplicates threshold value or accept the default of 65%.</span></span> 
  
 <span data-ttu-id="eec6a-p104">**Designs** Kontrollkästchen Sie dieses, um alle Dateien zu verarbeiten und Designs zuweisen. Standardmäßig ist dieses Kontrollkästchen nicht aktiviert. Geben Sie die folgenden Optionen aus, wenn Sie Designs Verarbeitung ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p104">**Themes**Check this box to process all files and assign themes to them. By default, this check box is not selected. Enter the following options if you want to perform Themes processing.</span></span>
  
- <span data-ttu-id="eec6a-p105">**Maximale Anzahl von Designs** Geben Sie ein, oder wählen Sie einen Wert für die Anzahl der Designs zu erstellen. Der Standardwert ist 200.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p105">**Max number of themes**Enter or select a value for the number of themes to create. The default is 200.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="eec6a-p106">Erhöhung der Anzahl der Designs wirkt sich auf Leistung als auch die Möglichkeit eines Designs, verallgemeinern. Je höher die Anzahl der Designs, die eine genauere sind. Beispielsweise, wenn eine Reihe von 50 Designs ein Design wie "Basketball, beleben, geschoren Lakers" enthalten 300 Designs separate Designs enthalten können: "Beleben", "Geschoren", "Lakers". Wenn Sie keine zur Förderung des Bekanntheitsgrads des Designs "Basketball" hatte und verwenden Sie diese Funktion für ECA, konnte das Design anzeigen "Basketball" nützlich sein. Wenn die Verarbeitung zu viele Designs hatten, Sie jedoch möglicherweise noch nie das Wort "Basketball" angezeigt und können nicht kennen, beleben und geschoren gute Basketball Designs sind, um zu prüfen, anstatt Elemente, die auf startet und für haarstrich verwendet.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p106">Increasing the number of themes affects performance, as well as the ability of a theme to generalize. The higher the number of themes, the more granular they are. For example, if a set of 50 themes include a theme such as "Basketball, Spurs, Clippers, Lakers"; 300 themes may include separate themes: "Spurs", "Clippers", "Lakers". If you had no awareness of the theme "Basketball" and use this feature for ECA, seeing the theme "Basketball" could be useful. But, if the processing had too many themes, you may never see the word "Basketball" and may not know that Spurs and Clippers are good Basketball themes to review, rather than items that go on boots and used for hair.</span></span> 
  
- <span data-ttu-id="eec6a-p107">**Vorgeschlagene Designs** Sie können Designs Wörter zum Steuern der Verarbeitung Designs vorschlagen. Erweiterte eDiscovery wird den Schwerpunkt auf folgenden vorgeschlagenen Wörter und versuchen, eine oder mehrere relevante Designs, basierend auf der Einstellung "Maximale Anzahl der Designs" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p107">**Suggested themes**You can suggest theme words to control Themes processing. Advanced eDiscovery will focus on these suggested words and try to create one or more relevant themes, based on the "Max number of themes" settings.</span></span> 
    
    <span data-ttu-id="eec6a-p108">Beispielsweise wird das vorgeschlagene Wort "Computer", und Sie als die "maximale Anzahl der Designs" "2" angegeben, erweiterte eDiscovery versuchen, zwei Designs zu generieren, die sich auf das Wort "Computer" beziehen. Zwei Designs können beispielsweise "Computersoftware" und "Computerhardware" sein.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p108">For example, if the suggested word is "computer", and you specified "2" as the "Max number of Themes", Advanced eDiscovery will try to generate two themes that relate to the word "computer". The two themes might be "computer software" and "computer hardware", for example.</span></span> 
    
    ![Vorgeschlagenes Design hinzufügen](media/06e9ffd3-a76c-423b-b450-9e465eb9a02f.png)
  
1. <span data-ttu-id="eec6a-129">Zum Anzeigen, hinzufügen oder Bearbeiten der vorgeschlagenen Designs, klicken Sie auf **Ändern**.</span><span class="sxs-lookup"><span data-stu-id="eec6a-129">To view, add, or edit suggested themes, click **Modify**.</span></span>
    
2. <span data-ttu-id="eec6a-p109">Klicken Sie auf **Hinzufügen**, in der Systemsteuerung **vorgeschlagene Designs** ![Symbol hinzufügen](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) Symbol, um ein Design hinzuzufügen. Fügen Sie in der Systemsteuerung **Hinzufügen vorgeschlagenen Design** Wörter durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p109">In the **Suggested themes** panel, click the **Add**![add icon](media/c2dd8b3a-5a22-412c-a7fa-143f5b2b5612.png) icon to add a theme. In the **Add suggested theme** panel, add the words, separated by commas.</span></span> 
    
3. <span data-ttu-id="eec6a-132">**Anzahl der Designs**wählen Sie einen Wert für die Anzahl der Designs zu bestimmen, die erweiterte eDiscovery versucht, diese Wörter generieren (der Standardwert ist 1 Design).</span><span class="sxs-lookup"><span data-stu-id="eec6a-132">In **Number of themes**, select a value to determine the number of themes Advanced eDiscovery will try to generate for these words (default is 1 theme).</span></span>
    
4. <span data-ttu-id="eec6a-133">Klicken Sie auf **Speichern** , und schließen Sie das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="eec6a-133">Click **Save** and then close the dialogue.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="eec6a-p110">Die Gesamtzahl der Designs enthält vorgeschlagene Designs. Die gesamte vorgeschlagene Designs darf die gesamten Designs nicht überschreiten. Wenn viele vorgeschlagene Designs relativ zur Erstellung der gesamten Designs vorhanden sind, werden nur ein Paar "Roman" Designs, da die meisten der Designs vorgeschlagene Designs zugewiesen wird, werden vom System erkannt.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p110">The total number of themes includes Suggested Themes. The total Suggested Themes cannot exceed the total themes. If there are many Suggested Themes relative to the total themes, only a few "novel" themes will be detected by the system because most of the themes will be dedicated to Suggested Themes.</span></span> 
  
- <span data-ttu-id="eec6a-137">**Modus** Wählen Sie aus der Dropdownliste ein **Designs** -Option aus:</span><span class="sxs-lookup"><span data-stu-id="eec6a-137">**Mode** From the drop-down list, select a **Themes** option:</span></span> 
    
  - <span data-ttu-id="eec6a-138">**Erstellen und Anwenden von Modell**: berechnet Designs von Modellen aus einem Segment der Dateien und dann verteilt zwischen diesen Dateien.</span><span class="sxs-lookup"><span data-stu-id="eec6a-138">**Create and apply model**: Calculates themes by models from a segment of the files and then distributes files among them.</span></span>
    
  - <span data-ttu-id="eec6a-p111">**Create-Modell**: ein Designs-Modell aus einem Segment der Dateien berechnet. Der übernehmen Prozess der Division von Dateien ist separat zu einem späteren Zeitpunkt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p111">**Create model**: Calculates a themes model from a segment of the files. The Apply process of dividing files is done separately at another time.</span></span>
    
  - <span data-ttu-id="eec6a-p112">**Apply-Modell**: Diese Option wird nur angezeigt, wenn ein Modell wurde bereits zuvor erstellt und noch nicht angewendet. Dadurch werden die Dateien basierend auf der Designs dividiert.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p112">**Apply model**: This option is only shown if a model was created previously and not yet applied. This will divide the files based on the themes.</span></span>
    
<span data-ttu-id="eec6a-143">Sie können auch [Set Text ignorieren](set-ignore-text-in-advanced-ediscovery.md) , und [Legen Sie Analyze Erweiterte Einstellungen](set-analyze-advanced-settings-in-advanced-ediscovery.md) für die Analyse.</span><span class="sxs-lookup"><span data-stu-id="eec6a-143">You can also [set ignore text](set-ignore-text-in-advanced-ediscovery.md) and [set Analyze advanced settings](set-analyze-advanced-settings-in-advanced-ediscovery.md) for Analyze.</span></span> 
  
<span data-ttu-id="eec6a-p113">Nachdem Sie diese Optionen festgelegt haben, klicken Sie auf **Analyze** ausführen. [Analysieren der Ansicht Ergebnisse](view-analyze-results-in-advanced-ediscovery.md) werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eec6a-p113">After you've set these options, click **Analyze** to run. [View Analyze results](view-analyze-results-in-advanced-ediscovery.md) are displayed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eec6a-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eec6a-146">See also</span></span>

[<span data-ttu-id="eec6a-147">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="eec6a-147">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="eec6a-148">Grundlegendes zu Dokument Ähnlichkeit</span><span class="sxs-lookup"><span data-stu-id="eec6a-148">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="eec6a-149">Legen Sie Text ignorieren</span><span class="sxs-lookup"><span data-stu-id="eec6a-149">Set Ignore text </span></span>](set-ignore-text-in-advanced-ediscovery.md)
  
[<span data-ttu-id="eec6a-150">Analysieren erweiterter Einstellungen festlegen</span><span class="sxs-lookup"><span data-stu-id="eec6a-150">Set Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="eec6a-151">Anzeigen von Ergebnisse der Analyse</span><span class="sxs-lookup"><span data-stu-id="eec6a-151">View Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

