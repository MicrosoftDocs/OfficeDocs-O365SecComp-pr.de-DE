---
title: Verwenden von Office 365 Advanced eDiscovery Utilities
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Erfahren Sie mehr über die Dienstprogramme in Office 365 Advanced eDiscovery, einschließlich Case Log, Clear Data, Process Errors, Modify Relevance und Transparency Analysis.  '
ms.openlocfilehash: bd100883804b300e77abcc8a2224cf1a59b53475
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32265357"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a><span data-ttu-id="9a82d-103">Verwenden von Office 365 Advanced eDiscovery Utilities</span><span class="sxs-lookup"><span data-stu-id="9a82d-103">Use Office 365 Advanced eDiscovery utilities</span></span>

> [!NOTE]
> <span data-ttu-id="9a82d-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="9a82d-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="9a82d-106">Die in Advanced eDiscovery angezeigten und verfügbaren Dienstprogramme hängen von Kontext-und Benutzerrollen ab.</span><span class="sxs-lookup"><span data-stu-id="9a82d-106">The utilities that are displayed and available in Advanced eDiscovery depend on context and user roles.</span></span>
  
## <a name="case-log"></a><span data-ttu-id="9a82d-107">Fallprotokoll</span><span class="sxs-lookup"><span data-stu-id="9a82d-107">Case log</span></span>

<span data-ttu-id="9a82d-108">Das Fallprotokoll enthält eine detaillierte Liste der Anwendungs Verarbeitungsaktivitäten, die zum Nachverfolgen, zur Problembehandlung und zum Beheben von Fehlern und Warnungen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9a82d-108">The Case log provides a detailed list of application processing activities, which can be used for tracking, troubleshooting, and for addressing errors and warnings.</span></span> <span data-ttu-id="9a82d-109">Das Protokoll kann lokal auf dem Host oder Server generiert und gespeichert oder direkt an eine e-Mail-Adresse gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9a82d-109">The log can be generated and stored locally on the host or server, or sent directly to an email address.</span></span>
  
<span data-ttu-id="9a82d-110">Die Protokolldatei kann auch auf den Clientcomputer heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="9a82d-110">The log file can also be downloaded to the client's computer.</span></span> <span data-ttu-id="9a82d-111">Die Client Download Option kann gemäß der Konfiguration und der Benutzerrolle aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="9a82d-111">The client download option may be enabled or disabled according to configuration and user role.</span></span>
  
1. <span data-ttu-id="9a82d-112">Klicken Sie in der Menüleiste auf das **Zahnrad** Symbol.</span><span class="sxs-lookup"><span data-stu-id="9a82d-112">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="9a82d-113">Wählen Sie auf der Registerkarte **Einstellungen und Dienstprogramme \> \*\* die Option \*\* \> Case Log Setup**aus.</span><span class="sxs-lookup"><span data-stu-id="9a82d-113">In the **Settings and utilities \> Utilities** tab, select **Case log \> Setup**.</span></span>
    
3. <span data-ttu-id="9a82d-114">Wählen Sie die **Protokollebene** wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="9a82d-114">Select the **Log level** as follows:</span></span> 
    
  - <span data-ttu-id="9a82d-115">**Standard**: enthält die grundlegenden Protokolldaten.</span><span class="sxs-lookup"><span data-stu-id="9a82d-115">**Standard**: Includes the basic log data.</span></span> <span data-ttu-id="9a82d-116">Diese Option ist in der Regel für die Überwachung erforderlich und sollte verwendet werden, sofern nicht anders empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9a82d-116">This option is usually necessary for monitoring, and should be used unless recommended otherwise.</span></span>
    
  - <span data-ttu-id="9a82d-117">**Minimal**: wird für sehr große Fälle verwendet und gibt nur die neuesten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="9a82d-117">**Minimal**: Used for very large cases, and returns only the latest data.</span></span>
    
4. <span data-ttu-id="9a82d-118">Klicken Sie auf **Fallprotokoll ausführen**.</span><span class="sxs-lookup"><span data-stu-id="9a82d-118">Click **Run Case log**.</span></span> <span data-ttu-id="9a82d-119">Das Protokoll wird generiert, und path wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a82d-119">The log is generated and path is displayed.</span></span> <span data-ttu-id="9a82d-120">Die Vorgangsfortschritts Informationen für den aktuellen und den letzten Vorgang werden im Bereich Vorgangsstatus angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a82d-120">The task progress information for the current and last task is displayed in the Task status pane.</span></span>
    
## <a name="clear-data"></a><span data-ttu-id="9a82d-121">Daten löschen</span><span class="sxs-lookup"><span data-stu-id="9a82d-121">Clear data</span></span>

<span data-ttu-id="9a82d-122">Wenn es erforderlich ist, Falldaten zu löschen oder neu zu initialisieren, muss die Datenbankinstanz initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="9a82d-122">If it is necessary to delete or reinitialize case data, the database instance must be initialized.</span></span> <span data-ttu-id="9a82d-123">Mit dem Dienstprogramm löschen werden alle angegebenen Einträge aus der falldatenbank, den Textdateien, dem Fallordner und den akkumulierten Ergebnissen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9a82d-123">The Clear data utility deletes all specified entries from the case database, text files, case folder, and accumulated results.</span></span> <span data-ttu-id="9a82d-124">Die Funktion kann nur von einem Administrator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9a82d-124">The function can only be performed by an administrator.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="9a82d-125">Diese Aktion ist nicht umkehrbar und löscht alle Relevanz-Tagging und Analysen des Experten.</span><span class="sxs-lookup"><span data-stu-id="9a82d-125">This action is not reversible and will clear all Relevance tagging and analysis performed by the expert.</span></span> <span data-ttu-id="9a82d-126">Speichern Sie bei Bedarf eine Sicherung der Daten.</span><span class="sxs-lookup"><span data-stu-id="9a82d-126">Save a backup of data, if necessary.</span></span> <span data-ttu-id="9a82d-127">Verwenden Sie diese Option mit äußerster Vorsicht.</span><span class="sxs-lookup"><span data-stu-id="9a82d-127">Use this option with extreme care.</span></span> <span data-ttu-id="9a82d-128">Das Löschen von gekennzeichneten und bewerteten Dateien kann sich auf die Relevanz auswirken.</span><span class="sxs-lookup"><span data-stu-id="9a82d-128">Deleting tagged and ranked files can impact the Relevance results.</span></span> 
  
1. <span data-ttu-id="9a82d-129">Klicken Sie in der Menüleiste auf das **Zahnrad** Symbol.</span><span class="sxs-lookup"><span data-stu-id="9a82d-129">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="9a82d-130">Wählen Sie auf der Registerkarte **Einstellungen und Dienstprogramme \> \*\* die Option \*\* \> Daten Einrichtung löschen**aus.</span><span class="sxs-lookup"><span data-stu-id="9a82d-130">In the **Settings and utilities \> Utilities** tab, select **Clear data \> Setup**.</span></span>
    
3. <span data-ttu-id="9a82d-131">Wählen Sie eine Option für die zu initialisierenden Informationen aus:</span><span class="sxs-lookup"><span data-stu-id="9a82d-131">Select an option for the information to initialize:</span></span>
    
  - <span data-ttu-id="9a82d-132">**Relevanz**: Löscht alle in Relevanz gemachten arbeiten, einschließlich der Definition von Lasten und der Zuordnung von Dateien zu Lasten.</span><span class="sxs-lookup"><span data-stu-id="9a82d-132">**Relevance**: Deletes all work done in Relevance, including definition of loads and association of files to loads.</span></span> <span data-ttu-id="9a82d-133">Es werden alle Beispiele und Markierungen gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9a82d-133">It deletes all samples and tagging.</span></span>
    
  - <span data-ttu-id="9a82d-134">**Near-Duplikate und e-Mail-Threads**: Löscht alle Analyseinformationen von Near-Duplikaten und e-Mail-Threads.</span><span class="sxs-lookup"><span data-stu-id="9a82d-134">**Near-duplicates and email threads**: Deletes all analysis information of near-duplicates and email threads.</span></span>
    
  - <span data-ttu-id="9a82d-135">**Designs**: löscht themenbezogene Daten.</span><span class="sxs-lookup"><span data-stu-id="9a82d-135">**Themes**: Deletes themes-related data.</span></span>
    
  - <span data-ttu-id="9a82d-136">**Export Verlauf**: Löscht Verlaufsinformationen zu Export Batches.</span><span class="sxs-lookup"><span data-stu-id="9a82d-136">**Export history**: Deletes history information of Export batches.</span></span>
    
4. <span data-ttu-id="9a82d-137">Klicken Sie auf **Daten löschen**.</span><span class="sxs-lookup"><span data-stu-id="9a82d-137">Click **Clear data**.</span></span> <span data-ttu-id="9a82d-138">Die Falldaten werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="9a82d-138">The case data is cleared.</span></span> <span data-ttu-id="9a82d-139">Die Vorgangsfortschritts Informationen für den aktuellen und den letzten Vorgang werden im Bereich **Vorgangsstatus** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a82d-139">The task progress information for the current and last task is displayed in the **Task status** pane.</span></span> 
    
## <a name="modify-relevance"></a><span data-ttu-id="9a82d-140">Relevanz ändern</span><span class="sxs-lookup"><span data-stu-id="9a82d-140">Modify Relevance</span></span>

<span data-ttu-id="9a82d-141">In diesem Abschnitt wird beschrieben, wie Sie ein Relevanz-Beispiel überspringen oder zurücksetzen.</span><span class="sxs-lookup"><span data-stu-id="9a82d-141">This section describes how to skip or roll back a Relevance sample.</span></span>
  
1. <span data-ttu-id="9a82d-142">Klicken Sie in der Menüleiste auf das **Zahnrad** Symbol.</span><span class="sxs-lookup"><span data-stu-id="9a82d-142">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="9a82d-143">Wählen Sie auf der Registerkarte \*\*Einstellungen und Dienstprogramme \> \*\* die Option **Relevanz ändern**aus.</span><span class="sxs-lookup"><span data-stu-id="9a82d-143">In the **Settings and utilities \> Utilities** tab, select **Modify relevance**.</span></span>
    
3. <span data-ttu-id="9a82d-144">Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="9a82d-144">Select from the options:</span></span> 
    
  - <span data-ttu-id="9a82d-145">**Aktuelle Beispiel überspringen-für aktuellen Benutzer**: Dieses Tag, als **Skip**, alle untagged-Dateien im Open Case-Beispiel des Benutzers, der das Hilfsprogramm ausführt.</span><span class="sxs-lookup"><span data-stu-id="9a82d-145">**Skip current sample - for current user**: This will tag, as **Skip**, all untagged files in the open case sample of the user running the utility.</span></span> <span data-ttu-id="9a82d-146">Die Relevanz-Verarbeitung wird nicht für Dateien ausgeführt, die als **Skip**gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="9a82d-146">Relevance processing will not be performed on files tagged as **Skip**.</span></span>
    
  - <span data-ttu-id="9a82d-147">**Aktuelle Sample-alle geöffneten Samples überspringen**: Dieses Tag, als **Skip**, alle nicht markierten Dateien in allen geöffneten Beispielen für alle Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9a82d-147">**Skip current sample - all open samples**: This will tag, as **Skip**, all untagged files in all open samples for all users.</span></span> <span data-ttu-id="9a82d-148">Diese Option wird nicht empfohlen, wenn Benutzer derzeit Beispiele markieren.</span><span class="sxs-lookup"><span data-stu-id="9a82d-148">This option is not recommended if users are currently tagging samples.</span></span>
    
  - <span data-ttu-id="9a82d-149">**Letztes Beispiel zurück**setzen: das Beispiel für die letzte abgeschlossene Relevanz wird zurückgesetzt, unabhängig davon, ob es vor oder nach dem Prozess "berechnen" vorliegt.</span><span class="sxs-lookup"><span data-stu-id="9a82d-149">**Roll back last sample**: The last completed Relevance training sample will be rolled back, regardless of whether it is before or after the "Calculate" process.</span></span> <span data-ttu-id="9a82d-150">Das Rollback eines catch-up-Beispiels ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9a82d-150">Rollback of a catch-up sample is not allowed.</span></span>
    
4. <span data-ttu-id="9a82d-151">Klicken \*\*\*\* Sie auf Ausführen, um auszuführen.</span><span class="sxs-lookup"><span data-stu-id="9a82d-151">Click **Execute** to run.</span></span> 
    
## <a name="transparency-analysis"></a><span data-ttu-id="9a82d-152">Transparenz Analyse</span><span class="sxs-lookup"><span data-stu-id="9a82d-152">Transparency analysis</span></span>

<span data-ttu-id="9a82d-153">Das Dienstprogramm für die Transparenz Analyse ermöglicht eine detaillierte Ansicht der Dateien und ihre zugewiesene Relevanz.</span><span class="sxs-lookup"><span data-stu-id="9a82d-153">The Transparency analysis utility enables a detailed view of files and their assigned Relevance score.</span></span> <span data-ttu-id="9a82d-154">Der Bericht kann als Plausibilitätsprüfung oder zum Vergleichen der Relevanz einer von einem menschlichen Prüfer definierten Datei im Vergleich zu der Relevanz verwendet werden, die von Advanced eDiscovery zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="9a82d-154">The report can be used as a sanity check or to compare the relevance of a file defined by a human reviewer as compared to the relevance assigned by Advanced eDiscovery.</span></span> 
  
<span data-ttu-id="9a82d-155">Zusätzlich zu den Relevanz-Bewertungen berechnet und weist Advanced eDiscovery Schlüsselwort Gewichte auf, die den Stichwort Kontext berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="9a82d-155">In addition to Relevance scores, Advanced eDiscovery calculates and assigns keyword weights that consider the keyword context.</span></span> <span data-ttu-id="9a82d-156">Das gleiche Wort in einer Datei kann je nach Kontext und Speicherort mit unterschiedlichen gewichten versehen werden.</span><span class="sxs-lookup"><span data-stu-id="9a82d-156">The same word in a file can be assigned different weights, depending on context and location.</span></span> <span data-ttu-id="9a82d-157">Jedes Schlüsselwort wird mit einer zunehmenden Farbintensität von gelb bis dunkel Orange und unterschiedlichen Grautönen gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="9a82d-157">Each keyword is marked using an increasing scale of color intensity ranging from yellow to dark orange and varying shades of gray.</span></span> <span data-ttu-id="9a82d-158">Die Farbcodierung wird verwendet, um den relativen positiven oder negativen Beitrag des Wortes zum Relevanzwert visuell anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9a82d-158">Color coding is used to visually indicate the word's relative positive or negative contribution to the Relevance score.</span></span> 
  
<span data-ttu-id="9a82d-159">In einem Szenario mit mehreren Problemen kann für jedes Problem ein Bericht zur Transparenz Analyse generiert werden.</span><span class="sxs-lookup"><span data-stu-id="9a82d-159">In a multiple-issue case scenario, a Transparency analysis report can be generated for each issue.</span></span>
  
1. <span data-ttu-id="9a82d-160">Klicken Sie in der Menüleiste auf das **Zahnrad** Symbol.</span><span class="sxs-lookup"><span data-stu-id="9a82d-160">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="9a82d-161">Wählen Sie auf der Registerkarte **Einstellungen und Dienstprogramme \> \*\* die Option \*\* \> Transparenz analyseeinrichtung**aus.</span><span class="sxs-lookup"><span data-stu-id="9a82d-161">In the **Settings and utilities \> Utilities** tab, select **Transparency analysis \> Setup**.</span></span>
    
3. <span data-ttu-id="9a82d-162">Geben Sie in \* \* Datei-ID \* \* die Datei-ID der zu verarbeitenden Datei ein.</span><span class="sxs-lookup"><span data-stu-id="9a82d-162">In \*\* File ID \*\*, enter the file ID of the file to process.</span></span>
    
4. <span data-ttu-id="9a82d-163">Wählen Sie in der Liste **Problem** das entsprechende Problem aus.</span><span class="sxs-lookup"><span data-stu-id="9a82d-163">In the **Issue** list, select the pertinent issue.</span></span> 
    
5. <span data-ttu-id="9a82d-164">Klicken Sie auf **Transparenz Analyse**.</span><span class="sxs-lookup"><span data-stu-id="9a82d-164">Click **Transparency analysis**.</span></span> <span data-ttu-id="9a82d-165">Nach Abschluss des Vorgangs wird der Bericht zur Transparenz Analyse für die Datei angezeigt, der zeigt, wie die markierten Schlüsselwortfarben mit dem Gesamtergebnis der Relevanz korrelieren.</span><span class="sxs-lookup"><span data-stu-id="9a82d-165">Upon completion, the Transparency analysis report for the file is displayed, which shows how the marked keyword colors correlate to the overall Relevance score.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9a82d-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a82d-166">See also</span></span>

[<span data-ttu-id="9a82d-167">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="9a82d-167">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="9a82d-168">Definieren von Fall-und Mandanten Einstellungen</span><span class="sxs-lookup"><span data-stu-id="9a82d-168">Defining case and tenant settings</span></span>](define-case-and-tenant-settings-in-advanced-ediscovery.md)

