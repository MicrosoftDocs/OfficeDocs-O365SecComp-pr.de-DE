---
title: Einrichten von Lasten importierte Dateien in Office 365 erweiterte eDiscovery hinzu
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
ms.assetid: 0e0a9d04-294f-4f54-8bf1-b32d81345126
description: 'Überprüfen Sie die Schritte aus, um die letzten definierten laden oder einen Batch von Dateien mit früherer ausführen Relevanz Schulung in Office 365 erweiterte eDiscovery importierte Dateien hinzugefügt.  '
ms.openlocfilehash: 2c986578b969b671351930fd6939a90e3a821dc2
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529974"
---
# <a name="set-up-loads-to-add-imported-files-in-office-365-advanced-ediscovery"></a><span data-ttu-id="5b791-103">Einrichten von Lasten importierte Dateien in Office 365 erweiterte eDiscovery hinzu</span><span class="sxs-lookup"><span data-stu-id="5b791-103">Set up loads to add imported files in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="5b791-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="5b791-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="5b791-p102">Im erweiterten eDiscovery ist eine Last einen neuen Batch von Dateien in eine Anfrage hinzugefügt. Standardmäßig wird ein Hardwaregerät definiert und alle importierte Dateien hinzugefügt. Bevor Sie Relevanz Schulungen durchführen, müssen die Last importierte Dateien hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5b791-p102">In Advanced eDiscovery, a load is a new batch of files added to a case. By default, one load is defined and all imported files are added to it. Before performing Relevance training, imported files must be added to the load.</span></span> 
  
<span data-ttu-id="5b791-109">Berücksichtigen Sie die folgenden Szenarien:</span><span class="sxs-lookup"><span data-stu-id="5b791-109">Consider the following scenarios:</span></span>
  
- <span data-ttu-id="5b791-p103">Neue Dateien bekanntermaßen ähnlich wie bei der vorherigen Dateien auf die Groß-/Kleinschreibung Datenbank geladen werden, oder der vorherigen Laden der Dateien einer zufällig ausgewählten Satz aus der Auflistung der Datei wurde. Fügen Sie in diesem Fall die importierten Dateien das Laden der aktuellen Datei hinzu.</span><span class="sxs-lookup"><span data-stu-id="5b791-p103">New files are known to be similar to the previous files loaded to the case database, or the previous load of files was a random set from the file collection. In this instance, add the imported files to the current file load.</span></span>
    
- <span data-ttu-id="5b791-p104">Neue Dateien unterscheiden sich von vorherigen Unterhaltungen (beispielsweise aus einer anderen Quelle), oder Sie haben keine Vorkenntnisse, dass sie ähnliche oder auf den vorherigen Lasten unterschiedliche sind. Fügen Sie in diesem Szenario die importierten Dateien zu einer neuen Datei laden. Erweiterte eDiscovery dies als einen parallelen Lasten Szenario erkennt, ruft einen Ausgleich Prozess, sperrt Relevanz Schulung und Batch Berechnungen, bis die Ermittlung abgeschlossen ist, und die neue Last integriert und geschult ist.</span><span class="sxs-lookup"><span data-stu-id="5b791-p104">New files are different from previous ones (for example, from a different source), or you have no prior knowledge that they're similar or different to the previous loads. In this scenario, add the imported files to a new file load. Advanced eDiscovery recognizes this as a Rolling loads scenario, invokes a Catch-up process, locks Relevance training and Batch calculations until Catch-up is completed, and the new load is integrated and trained.</span></span> 
    
## <a name="adding-imported-files-to-the-current-load"></a><span data-ttu-id="5b791-115">Importierte Dateien hinzufügen, um die aktuelle Auslastung</span><span class="sxs-lookup"><span data-stu-id="5b791-115">Adding imported files to the current load</span></span>

<span data-ttu-id="5b791-p105">Eine Auslastung im erweiterten eDiscovery verarbeitet werden müssen alle importierte Dateien hinzugefügt werden. Importierte Dateien werden die letzten definierten Last hinzugefügt. Wenn Sie später weitere Dateien importieren, müssen sie auch die Last hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5b791-p105">All imported files must be added to a load to be processed in Advanced eDiscovery. Imported files are added to the last defined load. If you import additional files later, they also must be added to the load.</span></span>
  
1. <span data-ttu-id="5b791-119">In der **Relevanz \> Relevanz Setup** **Lasten**wählen Sie Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="5b791-119">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
    ![Relevanzeinrichtungslasten (Registerkarte)](media/278aac7f-655f-462f-852a-6baa5d818768.png)
  
2. <span data-ttu-id="5b791-p106">**Include-Dateien**: Wählen Sie eine Option für Dateien hinzu. In der Standardeinstellung Dateien hinzufügen, um die aktuelle Auslastung der Auffüllung "Alle Dateien" basiert.</span><span class="sxs-lookup"><span data-stu-id="5b791-p106">**Include files**: Select an option for files to include. By default, adding files to the current load is based on the "All files" population.</span></span>
    
    > [!TIP]
    > <span data-ttu-id="5b791-p107">Laden Sie alle verfügbare culled Dateien in Relevanz. Wenn Sie nur eine Teilmenge der verfügbaren Dateien laden möchten, zuerst finden Sie mit der Unterstützung von wie Laden Teilmengen Relevanz Schulung beeinträchtigen kann.</span><span class="sxs-lookup"><span data-stu-id="5b791-p107">Load all available culled files into Relevance. If you plan to load only a subset of the available files, please first consult with Support, as loading subsets can adversely affect Relevance training.</span></span> 
  
3. <span data-ttu-id="5b791-125">Wählen Sie in **Management wird geladen**eine Auslastung.</span><span class="sxs-lookup"><span data-stu-id="5b791-125">In **Loads management**, select a load.</span></span>
    
4. <span data-ttu-id="5b791-p108">Klicken Sie auf **Dateien hinzufügen**. Die Dateien werden an die Last hinzugefügt und ein Bestätigungsdialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b791-p108">Click **Add files**. The files are added to the load and a confirmation message is displayed.</span></span> 
    
5. <span data-ttu-id="5b791-128">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b791-128">Click **OK**.</span></span>
    
<span data-ttu-id="5b791-129">Die Dateien können nun im erweiterten eDiscovery Relevanz für die Dateien Schulung bearbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="5b791-129">The files can now be processed in Advanced eDiscovery Relevance for training the files.</span></span>
  
## <a name="editing-a-load-name-within-a-case"></a><span data-ttu-id="5b791-130">Bearbeiten einer Last Name innerhalb einer Anfrage</span><span class="sxs-lookup"><span data-stu-id="5b791-130">Editing a load name within a case</span></span>

<span data-ttu-id="5b791-131">Wenn die Last Name ändern, wird empfohlen, einen Namen zu verwenden, der an die Groß-/Kleinschreibung relevant ist.</span><span class="sxs-lookup"><span data-stu-id="5b791-131">If changing the load name, it is recommended to use a name that is significant to the case.</span></span>
  
1. <span data-ttu-id="5b791-132">In der **Relevanz \> Relevanz Setup** **Lasten**wählen Sie Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="5b791-132">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="5b791-p109">Wählen Sie einen, und klicken Sie auf das Symbol **Bearbeiten** , aus der Liste **Lasten Management** . Das Load-Fenster bearbeiten wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b791-p109">From the **Loads management** list, select a load and click the **Edit** icon. The Edit load window is displayed.</span></span> 
    
3. <span data-ttu-id="5b791-135">Geben Sie die Änderungen, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b791-135">Enter the changes, and then click **OK**.</span></span>
    
## <a name="adding-imported-files-to-a-new-load"></a><span data-ttu-id="5b791-136">Importierte Dateien hinzufügen, um ein neues laden</span><span class="sxs-lookup"><span data-stu-id="5b791-136">Adding imported files to a new load</span></span>

<span data-ttu-id="5b791-137">Nach dem Starten Relevanz Schulungen oder Batch Berechnung ausführen, sollten Sie zum Importieren und einen weiteren Satz von Dateien zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5b791-137">After starting Relevance training or performing Batch calculation, you may want to import and process an additional set of files.</span></span> 
  
<span data-ttu-id="5b791-p110">Bei der Ermittlung können Sie erstellen, markieren und analysieren den Ermittlung Satz. Erweiterte eDiscovery vergleicht seine Bewertung Relevant und nicht Relevant Dateien in die neue Last auf diejenigen in vorherigen wird geladen. Basierend auf den Ergebnissen, werden Sie aufgefordert, Synchronisieren beim treffen Falls erforderlich, und erweiterten eDiscovery Empfehlungen basierend auf den aufgelaufenen Relevanz Informationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5b791-p110">During Catch-up, you can create, tag, and analyze the Catch-up set. Advanced eDiscovery compares its assessment of Relevant and Non-Relevant files in the new load to those in previous loads. Based on the results, you are prompted to make Catch-up decisions, if necessary, and Advanced eDiscovery provides recommendations based on the accrued Relevance information.</span></span> 
  
<span data-ttu-id="5b791-141">Paralleles wird geladen, und dieser Funktionalität hängt wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5b791-141">Rolling Loads and Catch-up functionality varies as follows:</span></span> 
  
- <span data-ttu-id="5b791-142">Wenn Sie eine neue Dateilast nach Batch Berechnung importieren, bestimmt erweiterte eDiscovery, inwieweit die Dateien in eine der folgenden Kategorien fallen:</span><span class="sxs-lookup"><span data-stu-id="5b791-142">When you import a new file load after Batch calculation, Advanced eDiscovery determines to what extent the files fall into one of the following categories:</span></span>
    
  - <span data-ttu-id="5b791-143">Ähnlich wie (homogene): ein neues, benutzerdefiniertes Round Relevanz Schulungen ist nicht erforderlich, und die Kenntnisse aus der vorherigen Last aufgelaufene kann angewendet werden "wie gesehen" auf die neue Load.</span><span class="sxs-lookup"><span data-stu-id="5b791-143">Similar (homogeneous): A new, custom round of Relevance training is not required and the knowledge accrued from the previous load can be applied "as is" to the new load.</span></span> 
    
  - <span data-ttu-id="5b791-144">DISTINCT (heterogenen): ein neues, benutzerdefiniertes Round Relevanz Schulungen erforderlich ist und die Kenntnisse aus der vorherigen Last aufgelaufene kann nicht angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5b791-144">Distinct (heterogeneous): A new, custom round of Relevance training is required, and the knowledge accrued from the previous load cannot be applied.</span></span> 
    
    <span data-ttu-id="5b791-145">Diese Begriffe beziehen sich auf die Ebene der Ähnlichkeit von Dateien zwischen Lasten und nicht innerhalb der wird geladen.</span><span class="sxs-lookup"><span data-stu-id="5b791-145">These terms refer to the level of similarity of files between loads and not within the loads.</span></span> 
    
- <span data-ttu-id="5b791-p111">Beim Importieren eines neuen Datei laden während der Relevanz Schulung (vor dem Batch Berechnung) kann synchronisieren Sie Relevanz Schulungen auf den Dateisatz united weiter. Erweiterte eDiscovery wird nicht schätzen Sie, ob die neue Last ähnelt oder die vorherige Ladung voneinander ist. Es einfach sammelt Informationen über die neuen Last und ermöglicht die Relevanz Schulungen auf den neuen und vorherigen fortgesetzt von Dateien festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5b791-p111">When importing a new file load during Relevance training (before Batch calculation), Catch-up enables you to continue Relevance training on the united file set. Advanced eDiscovery does not estimate whether the new load is similar to or distinct from the previous load. It simply collects information about the new load and enables Relevance training to continue on the new and previous sets of files.</span></span> 
    
- <span data-ttu-id="5b791-149">Wenn vorhanden mehrere Probleme in Relevanz Schulung sowie Probleme nach Batch Berechnung sind, wird der Prozess der Ermittlung einmal für alle Probleme ausgeführt, und die Ergebnisse werden berechnet und für jedes Problem angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b791-149">When there are multiple issues in Relevance training as well as issues after Batch calculation, the Catch-up process is performed once for all issues, and the results are calculated and displayed for each issue.</span></span>
    
> [!NOTE]
> <span data-ttu-id="5b791-p112">Der Umfang der Stichprobe synchronisieren kann variieren. Es hängt von der Größe der neuen Last relativ zum Laden vorherigen und für die Anzahl der Beispiele, die vor dem Hinzufügen des neuen Laden abgeschlossen. Im Beispiel synchronisieren ist in der Regel eine Reihe von 200 bis 2.000 Dateien aus der neuen laden.</span><span class="sxs-lookup"><span data-stu-id="5b791-p112">The size of the Catch-up sample may vary. It depends on the size of the new load relative to the previous loads, and on the number of samples completed before adding the new load. The Catch-up sample is typically a set of 200 to 2,000 files from the new load.</span></span> 
  
> [!TIP]
> <span data-ttu-id="5b791-p113">Ermittlung andere Aufgaben beendet und erfordert einzelne Datei markieren und überprüfen. Daher können Sie führt zu mehr Verarbeitungsaufwand reduzieren, wenn Sie neue Dateien in großen Batches hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5b791-p113">Catch-up stops any other tasks and requires individual file tagging and review. Therefore, you can reduce overhead when you add new files in large batches.</span></span> 
  
## <a name="adding-a-new-file-load-using-catch-up-and-rolling-loads"></a><span data-ttu-id="5b791-155">Lädt ein neue Datei Laden von hervorgehobene und paralleles hinzufügen</span><span class="sxs-lookup"><span data-stu-id="5b791-155">Adding a new file load using Catch-up and Rolling loads</span></span>

1. <span data-ttu-id="5b791-156">In der **Relevanz \> Relevanz Setup** **Lasten**wählen Sie Registerkarte.</span><span class="sxs-lookup"><span data-stu-id="5b791-156">In the **Relevance \> Relevance setup** tab, select **Loads**.</span></span>
    
2. <span data-ttu-id="5b791-p114">Klicken Sie unter **Lasten Management**, klicken Sie auf die **+** Symbol, um eine Auslastung hinzuzufügen. Ein Bestätigungsdialogfeld wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b791-p114">Under **Loads management**, click the **+** icon to add a load. A confirmation message is displayed.</span></span> 
    
3. <span data-ttu-id="5b791-p115">Klicken Sie auf **Ja,** um den Vorgang fortzusetzen. Klicken Sie im Dialogfeld **neue hinzufügen laden** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5b791-p115">Click **Yes** to continue. The **Add new load** dialog is displayed.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="5b791-161">Sie können ein neues Laden nur hinzufügen, wenn Aktionen auf die vorherige Load durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="5b791-161">You can only add a new load if actions were performed to the previous load.</span></span> 
  
4. <span data-ttu-id="5b791-p116">Klicken Sie im Dialogfeld **neue hinzufügen laden** Typinformationen in **Laden Name** und **Beschreibung** , und klicken Sie dann auf **OK**. Erweiterte eDiscovery Fügt ein neues laden.</span><span class="sxs-lookup"><span data-stu-id="5b791-p116">In the **Add new load** dialog, type information in **Load name** and **Description** and then click **OK**. Advanced eDiscovery adds a new load.</span></span>
    
5. <span data-ttu-id="5b791-p117">Klicken Sie auf **Dateien hinzufügen**, um die neue Load-Datei zu importieren. Diese Auslastung werden alle neue Dateien hinzugefügt. Nach dem Import der Dateien erweiterte eDiscovery erkennt das Szenario der parallelen Lasten und synchronisieren im nächsten Schritt angibt.</span><span class="sxs-lookup"><span data-stu-id="5b791-p117">To import the new load file, click **Add files**. All new files are added to this load. After Advanced eDiscovery imports the files, it recognizes the Rolling loads scenario and indicates Catch-up as the next step.</span></span>
    
6. <span data-ttu-id="5b791-167">Klicken Sie auf **Synchronisieren** Sie unten im Dialogfeld, um das Szenario ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5b791-167">Click **Catch-up** at the bottom of the dialog to run the scenario.</span></span> 
    
    <span data-ttu-id="5b791-168">Ein einzelner Satz zu synchronisieren, in der Regel mit 200 bis 2.000 Dateien aus der neuen Load wird für alle Probleme zum gleichzeitigen Datei tagging zulassen erstellt.</span><span class="sxs-lookup"><span data-stu-id="5b791-168">A single Catch-up set, typically containing 200 to 2,000 files from the new load, is created for all issues to allow concurrent file tagging.</span></span>
    
    <span data-ttu-id="5b791-169">Details dienen, ob Lasten ähnliche oder unterschiedliche sind, gibt an, ob erweiterte eDiscovery zusammenführen oder teilen die Lasten automatisch und Informationen im Hinblick auf Verarbeitung im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="5b791-169">Details are provided about whether loads are similar or distinct, whether Advanced eDiscovery merged or split the loads automatically, and information regarding processing in the next step.</span></span>
    
    <span data-ttu-id="5b791-p118">Sie können Dateien markieren und führen Sie einen Vorgang berechnen. Die Kategorien Relevanz zu ermitteln, ob Lasten ähnliche oder unterschiedliche sind aktiviert und ermöglicht das Fortsetzen des neuen Satz von Dateien.</span><span class="sxs-lookup"><span data-stu-id="5b791-p118">You can then tag files and run a calculate operation. The tagging enables Relevance to determine if loads are similar or distinct and enables you to continue working on the new set of files.</span></span>
    
7. <span data-ttu-id="5b791-172">Nach der Ermittlung Satz überprüft werden, anzeigen **Relevanz \> nachverfolgen** für die Ermittlung Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="5b791-172">After the Catch-up set is reviewed, view **Relevance \> Track** for the Catch-up results.</span></span> 
    
1. <span data-ttu-id="5b791-173">Wenn das Laden der neuen Datei während der Relevanz Schulung hinzugefügt wurde ist eine (d. h., das Problem nicht noch Batch Berechnung durchlaufen hat), **Weiter Schulung** im nächsten Schritt, unabhängig von den Ergebnissen synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="5b791-173">If the new file load was added during Relevance training (meaning, the issue has not yet gone through Batch calculation), **Continue training** is the next step, regardless of the Catch-up results.</span></span> 
    
    <span data-ttu-id="5b791-p119">Die neuen und vorherigen geladen werden als ein Hardwaregerät verarbeitet, und Relevanz Schulung in der united Satz fortgesetzt. Sie sind jetzt mit diesem Verfahren abgeschlossen und Relevanz Schulung fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5b791-p119">The new and previous loads are processed as one load and Relevance training continues on the united set. You are now finished with this procedure and can continue Relevance training.</span></span> 
    
2. <span data-ttu-id="5b791-176">Wenn die neue Auslastung nach Batch Berechnung hinzugefügt wurde, fahren Sie mit den folgenden Schritten.</span><span class="sxs-lookup"><span data-stu-id="5b791-176">If the new load was added after Batch calculation, proceed to the following steps.</span></span>
    
8. <span data-ttu-id="5b791-177">Für neue Lasten nach Batch Berechnung hinzugefügt bestimmt die erweiterte eDiscovery ist die neue Last ähnelt oder vom vorherigen geladen wird, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5b791-177">For new loads added after Batch calculation, Advanced eDiscovery determines if the new load is similar to or distinct from previous loads, as follows:</span></span>
    
1. <span data-ttu-id="5b791-p120">Lädt ähneln gefunden: keine weiteren Relevanz Schulung erforderlich ist. Das Dashboard zeigt die empfohlenen nächsten Schritt wird ausgeführt ** Berechnung Batch ** erneut aus, um die Relevanz der Ergebnisse für die neue Auslastung berechnen. Lädt gefunden ähnlich, sein, damit die vorherigen Analyse Klassifizierung auf die neuen Dateien ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5b791-p120">If loads were found to be similar: No additional Relevance training is necessary. The dashboard shows the recommended next step is to run ** Batch calculation ** again to calculate Relevance scores for the new load. Loads were found to be similar, so the previous classifier analysis can be run on the new files.</span></span> 
    
2. <span data-ttu-id="5b791-p121">Wenn Lasten gefunden wurden, eindeutig sein: mehr Relevanz Schulungen erforderlich ist und im nächsten Schritt wird die Entscheidung synchronisieren. Wählen Sie eine Entscheidung Ermittlung wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="5b791-p121">If loads were found to be distinct: More Relevance training is necessary and the next step is Catch-up decision. Select a Catch-up decision as follows:</span></span>
    
    <span data-ttu-id="5b791-p122">Wenn Sie **Zusammenführen Lasten**auswählen, werden erweiterte eDiscovery vorherige und neue Lasten für die Schulung ein miteinander verbunden. Obwohl die erstmalige laden durchlaufen Batch Berechnung haben, ist Weitere Schulungen erforderlich. Schulung von neuen und vorherigen Lasten zusammen fortgesetzt werden. Batch Berechnung wird dann erneut ausführen und die Ergebnisse der vorherigen Batch Berechnung ignoriert werden soll. Wählen Sie die Auswahl dieser Option, wenn Relevanz Bewertungen für vorhandenen Lasten, beispielsweise neu berechnet werden können bei der Überprüfung der vorhandenen Datei Lasten nicht gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="5b791-p122">If you select **Merge loads**, Advanced eDiscovery merges previous and new loads for the training set. Although the first load went through Batch calculation, more training is needed. Continue training new and previous loads together. Batch calculation will then run again and the previous Batch calculation scores should be ignored. Choose this selection when Relevance scores for existing loads can be recalculated, for example, when review of existing file loads has not started.</span></span>
    
    <span data-ttu-id="5b791-p123">Wenn Sie **geteilte lädt**auswählen, Relevanz Schulung nur auf die neue Last weiter aus. In diesem Fall werden vorherige Batch Berechnung Bewertungen bleiben unverändert. Wählen Sie diese Option bei vorhandene Relevanz Bewertungen für vorhandenen Lasten, beispielsweise nicht neu berechnet wird, wenn die Überprüfung der vorhandenen Lasten bereits gestartet wurde. Relevanz Bewertungen von diesem Punkt an separat verwaltet werden und können nicht zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5b791-p123">If you select **Split loads**, continue Relevance training only on the new load. In this instance, previous Batch calculation scores will remain as is. Choose this option when existing Relevance scores for existing loads cannot be recalculated, for example, if review of existing loads has already started. Relevance scores are managed separately from this point onward and cannot be merged.</span></span>
    
3. <span data-ttu-id="5b791-192">Klicken Sie auf **Weiter Schulung**.</span><span class="sxs-lookup"><span data-stu-id="5b791-192">Click **Continue training**.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5b791-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5b791-193">See also</span></span>

[<span data-ttu-id="5b791-194">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="5b791-194">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="5b791-195">Definieren von Problemen und Zuweisen von Benutzern</span><span class="sxs-lookup"><span data-stu-id="5b791-195">Defining issues and assigning users</span></span>](define-issues-and-assign-users.md)
  
[<span data-ttu-id="5b791-196">Schlüsselwörter hervorgehoben definieren und erweiterte Optionen</span><span class="sxs-lookup"><span data-stu-id="5b791-196">Defining highlighted keywords and advanced options</span></span>](define-highlighted-keywords-and-advanced-options.md)

