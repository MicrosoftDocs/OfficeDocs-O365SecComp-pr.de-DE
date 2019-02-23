---
title: Einrichten von Lasten zum Hinzufügen von importierten Dateien in Office 365 Advanced eDiscovery
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Lesen Sie die Schritte zum Hinzufügen von importierten Dateien zur zuletzt definierten Last oder zum letzten Batch von Dateien, bevor Sie die Relevanz-Schulung in Office 365 Advanced eDiscovery ausführen.  '
ms.openlocfilehash: 8c5101628b468719f8aa4f81a4c73cbbb226105f
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30215985"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a><span data-ttu-id="1bd04-103">Einrichten von Lasten zum Hinzufügen von importierten Dateien in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1bd04-103">Set up loads to add imported files in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="1bd04-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="1bd04-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="1bd04-p102">In Advanced eDiscovery ist eine Auslastung ein neuer Batch von Dateien, die zu einem Fall hinzugefügt werden. Standardmäßig wird eine Auslastung definiert, und alle importierten Dateien werden ihr hinzugefügt. Vor der Durchführung der Relevanz-Schulung müssen importierte Dateien der Belastung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p102">In Advanced eDiscovery, a load is a new batch of files added to a case. By default, one load is defined and all imported files are added to it. Before performing Relevance training, imported files must be added to the load.</span></span> 
  
<span data-ttu-id="1bd04-109">Berücksichtigen Sie die folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="1bd04-109">Consider the following scenarios:</span></span>
  
- <span data-ttu-id="1bd04-p103">Neue Dateien sind bekanntermaßen vergleichbar mit den vorherigen Dateien, die in die Case-Datenbank geladen wurden, oder die frühere Datei Last war ein Zufalls Satz aus der file-Auflistung. Fügen Sie in dieser Instanz die importierten Dateien der aktuellen Datei Auslastung hinzu.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p103">New files are known to be similar to the previous files loaded to the case database, or the previous load of files was a random set from the file collection. In this instance, add the imported files to the current file load.</span></span>
    
- <span data-ttu-id="1bd04-p104">Neue Dateien unterscheiden sich von den vorherigen (beispielsweise aus einer anderen Quelle), oder Sie haben keine Vorkenntnisse, dass Sie ähnlich oder unterschiedlich zu den vorherigen Lasten sind. Fügen Sie in diesem Szenario die importierten Dateien einem neuen Datei Ladevorgang hinzu. Advanced eDiscovery erkennt dies als Roll laden Szenario, Ruft einen Aufholprozess ab, sperrt Relevanz Schulungen und Batch Berechnungen, bis das Catch-up abgeschlossen ist, und die neue Last ist integriert und geschult.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p104">New files are different from previous ones (for example, from a different source), or you have no prior knowledge that they're similar or different to the previous loads. In this scenario, add the imported files to a new file load. Advanced eDiscovery recognizes this as a Rolling loads scenario, invokes a Catch-up process, locks Relevance training and Batch calculations until Catch-up is completed, and the new load is integrated and trained.</span></span> 
    
## <a name="adding-imported-files-to-the-current-load"></a><span data-ttu-id="1bd04-115">Hinzufügen von importierten Dateien zur aktuellen Auslastung</span><span class="sxs-lookup"><span data-stu-id="1bd04-115">Adding imported files to the current load</span></span>

<span data-ttu-id="1bd04-p105">Alle importierten Dateien müssen zu einer zu verarbeitenden Ladung in Advanced eDiscovery hinzugefügt werden. Importierte Dateien werden der zuletzt definierten Last hinzugefügt. Wenn Sie später weitere Dateien importieren, müssen Sie auch der Lade hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p105">All imported files must be added to a load to be processed in Advanced eDiscovery. Imported files are added to the last defined load. If you import additional files later, they also must be added to the load.</span></span>
  
1. <span data-ttu-id="1bd04-119">Wählen Sie auf der Registerkarte **Relevanz \> Relevanz Setup** die Option **Lasten**aus.</span><span class="sxs-lookup"><span data-stu-id="1bd04-119">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
    ![Relevanzeinrichtungslasten (Registerkarte)](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. <span data-ttu-id="1bd04-p106">**Include Files**: Wählen Sie eine Option für die einzuschließenden Dateien aus. Das Hinzufügen von Dateien zur aktuellen Auslastung basiert standardmäßig auf der Auffüllung "alle Dateien".</span><span class="sxs-lookup"><span data-stu-id="1bd04-p106">**Include files**: Select an option for files to include. By default, adding files to the current load is based on the "All files" population.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="1bd04-p107">Laden Sie alle verfügbaren gekeulten Dateien in Relevanz. Wenn Sie nur eine Teilmenge der verfügbaren Dateien laden möchten, konsultieren Sie zunächst den Support, da das Laden von Teilmengen sich negativ auf die Relevanz-Schulung auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p107">Load all available culled files into Relevance. If you plan to load only a subset of the available files, please first consult with Support, as loading subsets can adversely affect Relevance training.</span></span> 
  
3. <span data-ttu-id="1bd04-125">Wählen Sie unter **Lasten Verwaltung**eine Last aus.</span><span class="sxs-lookup"><span data-stu-id="1bd04-125">In **Loads management**, select a load.</span></span>
    
4. <span data-ttu-id="1bd04-p108">Klicken Sie auf **Dateien hinzufügen**. Die Dateien werden dem Ladevorgang hinzugefügt, und eine Bestätigungsmeldung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p108">Click **Add files**. The files are added to the load and a confirmation message is displayed.</span></span> 
    
5. <span data-ttu-id="1bd04-128">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1bd04-128">Click **OK**.</span></span>
    
<span data-ttu-id="1bd04-129">Die Dateien können nun in Advanced eDiscovery-Relevanz für das Training der Dateien verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1bd04-129">The files can now be processed in Advanced eDiscovery Relevance for training the files.</span></span>
  
## <a name="editing-a-load-name-within-a-case"></a><span data-ttu-id="1bd04-130">Bearbeiten eines Lade namens in einem Fall</span><span class="sxs-lookup"><span data-stu-id="1bd04-130">Editing a load name within a case</span></span>

<span data-ttu-id="1bd04-131">Wenn Sie den ladenamen ändern, empfiehlt es sich, einen für den Fall bedeutsamen Namen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1bd04-131">If changing the load name, it is recommended to use a name that is significant to the case.</span></span>
  
1. <span data-ttu-id="1bd04-132">Wählen Sie auf der Registerkarte **Relevanz \> Relevanz Setup** die Option **Lasten**aus.</span><span class="sxs-lookup"><span data-stu-id="1bd04-132">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="1bd04-p109">Wählen Sie in der Liste **Lasten Verwaltung** eine Lade aus, und klicken Sie auf das Symbol **Bearbeiten** . Das fensterladen bearbeiten wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p109">From the **Loads management** list, select a load and click the **Edit** icon. The Edit load window is displayed.</span></span> 
    
3. <span data-ttu-id="1bd04-135">Geben Sie die Änderungen ein, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1bd04-135">Enter the changes, and then click **OK**.</span></span>
    
## <a name="adding-imported-files-to-a-new-load"></a><span data-ttu-id="1bd04-136">Hinzufügen von importierten Dateien zu einer neuen Ladung</span><span class="sxs-lookup"><span data-stu-id="1bd04-136">Adding imported files to a new load</span></span>

<span data-ttu-id="1bd04-137">Nachdem Sie das Relevanz-Training gestartet oder die Batch Berechnung ausgeführt haben, können Sie einen zusätzlichen Satz von Dateien importieren und verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1bd04-137">After starting Relevance training or performing Batch calculation, you may want to import and process an additional set of files.</span></span> 
  
<span data-ttu-id="1bd04-p110">Während des catch-up können Sie den catch-up-Satz erstellen, taggen und analysieren. Advanced eDiscovery vergleicht die Bewertung relevanter und nicht relevanter Dateien in der neuen Last mit denen in früheren Lasten. Basierend auf den Ergebnissen werden Sie aufgefordert, ggf. Nachhol Entscheidungen vorzunehmen, und erweiterte eDiscovery bietet Empfehlungen basierend auf den gesammelten Relevanzinformationen.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p110">During Catch-up, you can create, tag, and analyze the Catch-up set. Advanced eDiscovery compares its assessment of Relevant and Non-Relevant files in the new load to those in previous loads. Based on the results, you are prompted to make Catch-up decisions, if necessary, and Advanced eDiscovery provides recommendations based on the accrued Relevance information.</span></span> 
  
<span data-ttu-id="1bd04-141">Die Roll laden und die Catch-up-Funktionalität unterscheiden sich wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1bd04-141">Rolling Loads and Catch-up functionality varies as follows:</span></span> 
  
- <span data-ttu-id="1bd04-142">Wenn Sie eine neue Datei Auslastung nach der Batch Berechnung importieren, bestimmt Advanced eDiscovery, in welchem Umfang die Dateien in eine der folgenden Kategorien fallen:</span><span class="sxs-lookup"><span data-stu-id="1bd04-142">When you import a new file load after Batch calculation, Advanced eDiscovery determines to what extent the files fall into one of the following categories:</span></span>
    
  - <span data-ttu-id="1bd04-143">Ähnlich (homogen): eine neue, benutzerdefinierte Round-of-Relevance-Schulung ist nicht erforderlich, und das von der vorherigen Auslastung erworbene Wissen kann auf die neue Belastung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1bd04-143">Similar (homogeneous): A new, custom round of Relevance training is not required and the knowledge accrued from the previous load can be applied "as is" to the new load.</span></span> 
    
  - <span data-ttu-id="1bd04-144">Distinct (heterogenes): eine neue, benutzerdefinierte Round-of-Relevance-Schulung ist erforderlich, und das vom vorherigen Laden erworbene Wissen kann nicht angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="1bd04-144">Distinct (heterogeneous): A new, custom round of Relevance training is required, and the knowledge accrued from the previous load cannot be applied.</span></span> 
    
    <span data-ttu-id="1bd04-145">Diese Begriffe beziehen sich auf den Grad der Ähnlichkeit von Dateien zwischen Lasten und nicht innerhalb der Lasten.</span><span class="sxs-lookup"><span data-stu-id="1bd04-145">These terms refer to the level of similarity of files between loads and not within the loads.</span></span> 
    
- <span data-ttu-id="1bd04-p111">Beim Importieren eines neuen Datei Ladevorgangs während des Relevanz-Trainings (vor der Batch Berechnung) können Sie die Relevanz-Schulung im United-Dateisatz fortsetzen. Erweiterte eDiscovery schätzt nicht, ob die neue Auslastung der vorherigen Belastung ähnelt oder nicht. Sie sammelt lediglich Informationen über die neue Auslastung und ermöglicht die Fortsetzung der Relevanz-Schulung für die neuen und früheren Dateigruppen.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p111">When importing a new file load during Relevance training (before Batch calculation), Catch-up enables you to continue Relevance training on the united file set. Advanced eDiscovery does not estimate whether the new load is similar to or distinct from the previous load. It simply collects information about the new load and enables Relevance training to continue on the new and previous sets of files.</span></span> 
    
- <span data-ttu-id="1bd04-149">Wenn mehrere Probleme in Relevanz und Probleme nach der Batch Berechnung auftreten, wird der Aufholprozess für alle Probleme einmal ausgeführt, und die Ergebnisse werden für jedes Problem berechnet und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1bd04-149">When there are multiple issues in Relevance training as well as issues after Batch calculation, the Catch-up process is performed once for all issues, and the results are calculated and displayed for each issue.</span></span>
    
> [!NOTE]
> <span data-ttu-id="1bd04-p112">Die Größe des catch-up-Beispiels kann variieren. Es hängt von der Größe der neuen Last im Verhältnis zu den vorherigen Lasten und der Anzahl der vor dem Hinzufügen der neuen Last abgeschlossenen Beispiele ab. Das Catch-up-Beispiel ist in der Regel eine Reihe von 200 bis 2.000-Dateien aus der neuen Lade.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p112">The size of the Catch-up sample may vary. It depends on the size of the new load relative to the previous loads, and on the number of samples completed before adding the new load. The Catch-up sample is typically a set of 200 to 2,000 files from the new load.</span></span> 
  
> [!TIP]
> <span data-ttu-id="1bd04-p113">Catch-up beendet alle anderen Aufgaben und erfordert einzelne Dateikennzeichnung und-Überprüfungen. Daher können Sie den Aufwand reduzieren, wenn Sie neue Dateien in größeren Batches hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p113">Catch-up stops any other tasks and requires individual file tagging and review. Therefore, you can reduce overhead when you add new files in large batches.</span></span> 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a><span data-ttu-id="1bd04-155">Hinzufügen einer neuen Datei Last mit catch-up und Rolling Loads</span><span class="sxs-lookup"><span data-stu-id="1bd04-155">Adding a new file load using Catch-up and Rolling loads</span></span>

1. <span data-ttu-id="1bd04-156">Wählen Sie auf der Registerkarte **Relevanz \> Relevanz Setup** die Option **Lasten**aus.</span><span class="sxs-lookup"><span data-stu-id="1bd04-156">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="1bd04-p114">Klicken Sie unter **Lasten Verwaltung**auf **+** das Symbol, um eine Last hinzuzufügen. Eine Bestätigungsmeldung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p114">Under **Loads management**, click the **+** icon to add a load. A confirmation message is displayed.</span></span> 
    
3. <span data-ttu-id="1bd04-p115">Klicken Sie auf **Ja** , um fortzufahren. Das Dialogfeld **neuen Ladevorgang hinzufügen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p115">Click **Yes** to continue. The **Add new load** dialog is displayed.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="1bd04-161">Sie können nur dann eine neue Ladung hinzufügen, wenn Aktionen zur vorherigen Belastung ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="1bd04-161">You can only add a new load if actions were performed to the previous load.</span></span> 
  
4. <span data-ttu-id="1bd04-p116">Geben Sie im Dialogfeld **neuen Ladevorgang hinzufügen** Informationen in **Laden Name** und **Beschreibung** ein, und klicken Sie dann auf **OK**. Advanced eDiscovery fügt eine neue Auslastung hinzu.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p116">In the **Add new load** dialog, type information in **Load name** and **Description** and then click **OK**. Advanced eDiscovery adds a new load.</span></span>
    
5. <span data-ttu-id="1bd04-p117">Klicken Sie auf **Dateien hinzufügen**, um die neue Ladedatei zu importieren. Alle neuen Dateien werden dieser Belastung hinzugefügt. Nachdem die Dateien von Advanced eDiscovery importiert wurden, erkennt es das Szenario "Rolling Loads" und zeigt als nächster Schritt catch-up an.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p117">To import the new load file, click **Add files**. All new files are added to this load. After Advanced eDiscovery imports the files, it recognizes the Rolling loads scenario and indicates Catch-up as the next step.</span></span>
    
6. <span data-ttu-id="1bd04-167">Klicken Sie unten im Dialogfeld auf **catch-up** , um das Szenario auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1bd04-167">Click **Catch-up** at the bottom of the dialog to run the scenario.</span></span> 
    
    <span data-ttu-id="1bd04-168">Ein einzelner catch-up-Satz, der normalerweise 200 bis 2.000-Dateien aus der neuen Lade enthält, wird für alle Probleme erstellt, um die gleichzeitige Dateikennzeichnung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1bd04-168">A single Catch-up set, typically containing 200 to 2,000 files from the new load, is created for all issues to allow concurrent file tagging.</span></span>
    
    <span data-ttu-id="1bd04-169">Details dazu, ob Lasten ähnlich oder unterschiedlich sind, ob Advanced eDiscovery die Lasten automatisch zusammengeführt oder geteilt hat, sowie Informationen zur Verarbeitung im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="1bd04-169">Details are provided about whether loads are similar or distinct, whether Advanced eDiscovery merged or split the loads automatically, and information regarding processing in the next step.</span></span>
    
    <span data-ttu-id="1bd04-p118">Anschließend können Sie Dateien markieren und einen Berechnungsvorgang ausführen. Das Tagging ermöglicht die Relevanz, um zu bestimmen, ob Lasten ähnlich oder unterschiedlich sind, und ermöglicht es Ihnen, weiterhin an den neuen Dateien zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p118">You can then tag files and run a calculate operation. The tagging enables Relevance to determine if loads are similar or distinct and enables you to continue working on the new set of files.</span></span>
    
7. <span data-ttu-id="1bd04-172">Nach der Überprüfung des catch-up-Satzes zeigen Sie die **Relevanz \> -Spur** für die Catch-up-Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="1bd04-172">After the Catch-up set is reviewed, view **Relevance \> Track** for the Catch-up results.</span></span> 
    
1. <span data-ttu-id="1bd04-173">Wenn die neue Datei Auslastung während des Relevance-Trainings hinzugefügt wurde (was bedeutet, dass das Problem noch nicht durch die Batch Berechnung durchgeführt wurde), ist die **Weiterbildung** der nächste Schritt, unabhängig von den catch-up-Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="1bd04-173">If the new file load was added during Relevance training (meaning, the issue has not yet gone through Batch calculation), **Continue training** is the next step, regardless of the Catch-up results.</span></span> 
    
    <span data-ttu-id="1bd04-p119">Die neue und frühere Lasten werden verarbeitet, während eine Last-und Relevanz-Schulung auf dem United-Set fortgesetzt wird. Sie sind jetzt fertig mit diesem Verfahren und können die Relevanz-Schulung fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p119">The new and previous loads are processed as one load and Relevance training continues on the united set. You are now finished with this procedure and can continue Relevance training.</span></span> 
    
2. <span data-ttu-id="1bd04-176">Wenn die neue Ladung nach der Batch Berechnung hinzugefügt wurde, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="1bd04-176">If the new load was added after Batch calculation, proceed to the following steps.</span></span>
    
8. <span data-ttu-id="1bd04-177">Für neue Lasten, die nach der Batch Berechnung hinzugefügt werden, bestimmt Advanced eDiscovery, ob die neue Last ähnlich oder unterscheidet sich von früheren Lasten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="1bd04-177">For new loads added after Batch calculation, Advanced eDiscovery determines if the new load is similar to or distinct from previous loads, as follows:</span></span>
    
1. <span data-ttu-id="1bd04-p120">Wenn Lasten ähnlich sind, ist keine zusätzliche Relevanz erforderlich. Im Dashboard wird der Empfohlene nächste Schritt angezeigt: \* \* Batch Berechnung \* \* erneut ausführen, um die Relevanz für die neue Auslastung zu berechnen. Es wurde festgestellt, dass Lasten ähnlich sind, sodass die frühere Klassifizierungsanalyse für die neuen Dateien ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p120">If loads were found to be similar: No additional Relevance training is necessary. The dashboard shows the recommended next step is to run \*\* Batch calculation \*\* again to calculate Relevance scores for the new load. Loads were found to be similar, so the previous classifier analysis can be run on the new files.</span></span> 
    
2. <span data-ttu-id="1bd04-p121">Wenn Lasten unterschiedlich festgestellt wurden: mehr Relevanz Training ist erforderlich, und der nächste Schritt ist catch-up Entscheidung. Wählen Sie eine Aufhol Entscheidung wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="1bd04-p121">If loads were found to be distinct: More Relevance training is necessary and the next step is Catch-up decision. Select a Catch-up decision as follows:</span></span>
    
    <span data-ttu-id="1bd04-p122">Wenn Sie **Lasten zusammenführen**auswählen, werden von Advanced eDiscovery frühere und neue Lasten für den Trainingssatz zusammengeführt. Obwohl der erste Ladevorgang die Batch Berechnung durchführte, ist mehr Schulung erforderlich. Trainieren Sie neue und frühere Lasten zusammen. Die Batch Berechnung wird dann erneut ausgeführt, und die vorherigen Batch Berechnungsergebnisse sollten ignoriert werden. Wählen Sie diese Option aus, wenn die Relevanz für vorhandene Lasten neu berechnet werden kann, beispielsweise wenn die Überprüfungen vorhandener Datei Lasten nicht gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p122">If you select **Merge loads**, Advanced eDiscovery merges previous and new loads for the training set. Although the first load went through Batch calculation, more training is needed. Continue training new and previous loads together. Batch calculation will then run again and the previous Batch calculation scores should be ignored. Choose this selection when Relevance scores for existing loads can be recalculated, for example, when review of existing file loads has not started.</span></span>
    
    <span data-ttu-id="1bd04-p123">Wenn Sie geTeilte **Lasten**auswählen, wird die Relevanz-Schulung nur für die neue Last fortgesetzt. In dieser Instanz bleiben frühere Batch Berechnungsergebnisse unverändert. Wählen Sie diese Option aus, wenn vorhandene Relevanzwerte für vorhandene Lasten nicht neu berechnet werden können, beispielsweise wenn die Überprüfungen vorhandener Lasten bereits begonnen haben. Relevanz-Ergebnisse werden ab diesem Zeitpunkt separat verwaltet und können nicht zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1bd04-p123">If you select **Split loads**, continue Relevance training only on the new load. In this instance, previous Batch calculation scores will remain as is. Choose this option when existing Relevance scores for existing loads cannot be recalculated, for example, if review of existing loads has already started. Relevance scores are managed separately from this point onward and cannot be merged.</span></span>
    
3. <span data-ttu-id="1bd04-192">Klicken Sie auf **Training fortfahren**.</span><span class="sxs-lookup"><span data-stu-id="1bd04-192">Click **Continue training**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1bd04-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1bd04-193">See also</span></span>

[<span data-ttu-id="1bd04-194">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="1bd04-194">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="1bd04-195">Definieren von Problemen und Zuweisen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="1bd04-195">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="1bd04-196">Definieren hervorgehobener Schlüsselwörter und erweiterte Optionen</span><span class="sxs-lookup"><span data-stu-id="1bd04-196">Defining highlighted keywords and advanced options</span></span>](define-highlighted-keywords-and-advanced-options.md)

