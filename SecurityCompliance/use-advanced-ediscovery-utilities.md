---
title: Verwenden Sie Office 365 erweiterte eDiscovery Hilfsprogramme
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
ms.assetid: 66ca9993-75f4-4724-aea2-5a0719b660c1
description: 'Erfahren Sie mehr über die Dienstprogramme in Office 365 erweiterte eDiscovery, einschließlich Groß-/Kleinschreibung Anmeldung, Daten löschen, Fehler verarbeiten, Relevanz und Transparenz Analysis ändern.  '
ms.openlocfilehash: a68c98dd353971fcaa13fdc6b8e12bcf00c2faf0
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22528934"
---
# <a name="use-office-365-advanced-ediscovery-utilities"></a><span data-ttu-id="310c6-103">Verwenden Sie Office 365 erweiterte eDiscovery Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="310c6-103">Use Office 365 Advanced eDiscovery utilities</span></span>

> [!NOTE]
> <span data-ttu-id="310c6-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="310c6-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="310c6-106">Die Dienstprogramme, die angezeigt und in erweiterten eDiscovery verfügbar sind, hängt von Rollen Kontext und Benutzer.</span><span class="sxs-lookup"><span data-stu-id="310c6-106">The utilities that are displayed and available in Advanced eDiscovery depend on context and user roles.</span></span>
  
## <a name="case-log"></a><span data-ttu-id="310c6-107">Groß-/Kleinschreibung Protokoll</span><span class="sxs-lookup"><span data-stu-id="310c6-107">Case log</span></span>

<span data-ttu-id="310c6-p102">Groß-/Kleinschreibung Protokoll enthält eine ausführliche Liste der Anwendung Verarbeitungsaktivitäten, die für die Überwachung, Problembehandlung und zum Umgang mit Fehlern und Warnungen verwendet werden kann. Das Protokoll kann generiert und lokal auf dem Host oder Server gespeichert werden, oder direkt an eine e-Mail-Adresse gesendet.</span><span class="sxs-lookup"><span data-stu-id="310c6-p102">The Case log provides a detailed list of application processing activities, which can be used for tracking, troubleshooting, and for addressing errors and warnings. The log can be generated and stored locally on the host or server, or sent directly to an email address.</span></span>
  
<span data-ttu-id="310c6-p103">Die Protokolldatei kann auch auf dem Clientcomputer heruntergeladen werden. Die Option zum Herunterladen Client kann aktiviert oder deaktiviert entsprechend der Konfiguration und der Rolle werden.</span><span class="sxs-lookup"><span data-stu-id="310c6-p103">The log file can also be downloaded to the client's computer. The client download option may be enabled or disabled according to configuration and user role.</span></span>
  
1. <span data-ttu-id="310c6-112">Klicken Sie in der Menüleiste auf das Symbol **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="310c6-112">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="310c6-113">In der **Einstellungen und Dienstprogramme \> Dienstprogramme** Registerkarte **Groß-/Kleinschreibung Log \> Setup**.</span><span class="sxs-lookup"><span data-stu-id="310c6-113">In the **Settings and utilities \> Utilities** tab, select **Case log \> Setup**.</span></span>
    
3. <span data-ttu-id="310c6-114">Wählen Sie die **Protokollebene** wie folgt:</span><span class="sxs-lookup"><span data-stu-id="310c6-114">Select the **Log level** as follows:</span></span> 
    
  - <span data-ttu-id="310c6-p104">**Standard**: enthält die grundlegenden Protokolldaten. Diese Option ist in der Regel erforderlich für die Überwachung und sollte verwendet werden, es sei denn, andernfalls empfohlen.</span><span class="sxs-lookup"><span data-stu-id="310c6-p104">**Standard**: Includes the basic log data. This option is usually necessary for monitoring, and should be used unless recommended otherwise.</span></span>
    
  - <span data-ttu-id="310c6-117">**Minimale**: sehr große Umstände verwendet und gibt nur die neuesten Daten zurück.</span><span class="sxs-lookup"><span data-stu-id="310c6-117">**Minimal**: Used for very large cases, and returns only the latest data.</span></span>
    
4. <span data-ttu-id="310c6-p105">Klicken Sie auf **Protokoll Fall ausführen**. Das Protokoll wird generiert und Pfad wird angezeigt. Die Aufgabe Fortschrittsinformationen für den aktuellen und dem letzten Vorgang wird im Aufgabenbereich Status angezeigt.</span><span class="sxs-lookup"><span data-stu-id="310c6-p105">Click **Run Case log**. The log is generated and path is displayed. The task progress information for the current and last task is displayed in the Task status pane.</span></span>
    
## <a name="clear-data"></a><span data-ttu-id="310c6-121">Daten löschen</span><span class="sxs-lookup"><span data-stu-id="310c6-121">Clear data</span></span>

<span data-ttu-id="310c6-p106">Wenn es erforderlich ist, löschen oder erneuten Initialisieren der Groß-/Kleinschreibung Daten, muss die Datenbankinstanz initialisiert werden. Das Dienstprogramm Daten löschen Löscht alle angegebenen Einträge aus der Datenbank der Groß-/Kleinschreibung, Textdateien, Groß-/Kleinschreibung Ordner und kumulierten Ergebnisse. Die Funktion kann nur von einem Administrator ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="310c6-p106">If it is necessary to delete or reinitialize case data, the database instance must be initialized. The Clear data utility deletes all specified entries from the case database, text files, case folder, and accumulated results. The function can only be performed by an administrator.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="310c6-p107">Diese Aktion kann nicht rückgängig gemacht und löscht alle Kategorien Relevanz und Analysen, die von der Experte durchgeführt. Speichern Sie eine Sicherung der Daten, falls erforderlich. Verwenden Sie diese Option mit größter Vorsicht. Löschen von Dateien mit Tags und Rangfolge kann die Ergebnisse der Relevanz beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="310c6-p107">This action is not reversible and will clear all Relevance tagging and analysis performed by the expert. Save a backup of data, if necessary. Use this option with extreme care. Deleting tagged and ranked files can impact the Relevance results.</span></span> 
  
1. <span data-ttu-id="310c6-129">Klicken Sie in der Menüleiste auf das Symbol **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="310c6-129">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="310c6-130">In der **Einstellungen und Dienstprogramme \> Dienstprogramme** Registerkarte **Daten löschen \> Setup**.</span><span class="sxs-lookup"><span data-stu-id="310c6-130">In the **Settings and utilities \> Utilities** tab, select **Clear data \> Setup**.</span></span>
    
3. <span data-ttu-id="310c6-131">Wählen Sie eine Option für die Informationen nicht initialisiert werden:</span><span class="sxs-lookup"><span data-stu-id="310c6-131">Select an option for the information to initialize:</span></span>
    
  - <span data-ttu-id="310c6-p108">**Relevanz**: Löscht alle Arbeit in Relevanz, einschließlich Definition Lasten und Zuordnung von Dateien und lädt. Es löscht alle Beispiele und Kategorien.</span><span class="sxs-lookup"><span data-stu-id="310c6-p108">**Relevance**: Deletes all work done in Relevance, including definition of loads and association of files to loads. It deletes all samples and tagging.</span></span>
    
  - <span data-ttu-id="310c6-134">**In Ihrer Nähe Duplikate und e-Mail-Threads**: Löscht alle Analyseinformationen in Ihrer Nähe Duplikate und e-Mail-Threads.</span><span class="sxs-lookup"><span data-stu-id="310c6-134">**Near-duplicates and email threads**: Deletes all analysis information of near-duplicates and email threads.</span></span>
    
  - <span data-ttu-id="310c6-135">**Designs**: Löscht Daten im Zusammenhang mit Designs.</span><span class="sxs-lookup"><span data-stu-id="310c6-135">**Themes**: Deletes themes-related data.</span></span>
    
  - <span data-ttu-id="310c6-136">**Historie exportieren**: Verlaufsinformationen der Export Batches löscht.</span><span class="sxs-lookup"><span data-stu-id="310c6-136">**Export history**: Deletes history information of Export batches.</span></span>
    
4. <span data-ttu-id="310c6-p109">Klicken Sie auf **Daten löschen**. Die Groß-/Kleinschreibung Daten ist deaktiviert. Die Aufgabe Fortschrittsinformationen für den aktuellen und dem letzten Vorgang wird im Bereich **Aufgabenstatus** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="310c6-p109">Click **Clear data**. The case data is cleared. The task progress information for the current and last task is displayed in the **Task status** pane.</span></span> 
    
## <a name="modify-relevance"></a><span data-ttu-id="310c6-140">Ändern der Relevanz</span><span class="sxs-lookup"><span data-stu-id="310c6-140">Modify Relevance</span></span>

<span data-ttu-id="310c6-141">In diesem Abschnitt wird beschrieben, wie übersprungen oder Zurücksetzen einer Stichprobe Relevanz.</span><span class="sxs-lookup"><span data-stu-id="310c6-141">This section describes how to skip or roll back a Relevance sample.</span></span>
  
1. <span data-ttu-id="310c6-142">Klicken Sie in der Menüleiste auf das Symbol **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="310c6-142">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="310c6-143">In der **Einstellungen und Dienstprogramme \> Dienstprogramme** Registerkarte, wählen Sie **Relevanz ändern**.</span><span class="sxs-lookup"><span data-stu-id="310c6-143">In the **Settings and utilities \> Utilities** tab, select **Modify relevance**.</span></span>
    
3. <span data-ttu-id="310c6-144">Wählen Sie die Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="310c6-144">Select from the options:</span></span> 
    
  - <span data-ttu-id="310c6-p110">**Aktuelle Skip-Beispiel – für aktuellen Benutzer**: Dies wird markieren, als **Überspringen**, alle Dateien ohne Tags im open Groß-/Kleinschreibung Beispiel des Benutzers, der das Dienstprogramm. Verarbeitung der Relevanz wird nicht auf Dateien als **Überspringen**markierte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="310c6-p110">**Skip current sample - for current user**: This will tag, as **Skip**, all untagged files in the open case sample of the user running the utility. Relevance processing will not be performed on files tagged as **Skip**.</span></span>
    
  - <span data-ttu-id="310c6-p111">**Für die aktuelle Skip - alle geöffneten Beispiele**: Dies wird markieren, als **Überspringen**, alle Dateien ohne Tags in allen geöffneten Beispiele für alle Benutzer. Diese Option wird nicht empfohlen, wenn der Benutzer derzeit Beispiele für Kategorien sind.</span><span class="sxs-lookup"><span data-stu-id="310c6-p111">**Skip current sample - all open samples**: This will tag, as **Skip**, all untagged files in all open samples for all users. This option is not recommended if users are currently tagging samples.</span></span>
    
  - <span data-ttu-id="310c6-p112">**Rollback der letzten Beispiel**: das letzte Relevanz Training-Beispiel ein Rollback wird, unabhängig davon, ob sie vor oder nach der "Berechnen" Prozess ist abgeschlossen. Rollback der hervorgehobene Beispiel ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="310c6-p112">**Roll back last sample**: The last completed Relevance training sample will be rolled back, regardless of whether it is before or after the "Calculate" process. Rollback of a catch-up sample is not allowed.</span></span>
    
4. <span data-ttu-id="310c6-151">Klicken Sie auf **Execute** ausführen.</span><span class="sxs-lookup"><span data-stu-id="310c6-151">Click **Execute** to run.</span></span> 
    
## <a name="transparency-analysis"></a><span data-ttu-id="310c6-152">Transparenz Analyse</span><span class="sxs-lookup"><span data-stu-id="310c6-152">Transparency analysis</span></span>

<span data-ttu-id="310c6-p113">Das Transparenz Analysis-Dienstprogramm ermöglicht eine detaillierte Ansicht der Dateien und dem zugeordneten Relevanz Faktor. Der Bericht kann als Überprüfung oder zum Vergleichen von eigenständigen der Relevanz einer Datei, die durch ein Prüfer im Vergleich zu der Relevanz von erweiterten eDiscovery zugewiesenen definiert verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="310c6-p113">The Transparency analysis utility enables a detailed view of files and their assigned Relevance score. The report can be used as a sanity check or to compare the relevance of a file defined by a human reviewer as compared to the relevance assigned by Advanced eDiscovery.</span></span> 
  
<span data-ttu-id="310c6-p114">Zusätzlich zur Relevanz Faktoren erweiterte eDiscovery berechnet und weist Schlüsselwort Weights, die den Kontext Schlüsselwort berücksichtigen. Dasselbe Wort in einer Datei kann unterschiedliche Breiten, je nach Kontext und den Speicherort zugewiesen werden. Jedes Schlüsselwort ist eine zunehmende Skalierung der Farbintensität von Gelb bis hin zu dunkelorange und varying Graustufen mit gekennzeichnet. Farbe codieren wird verwendet, um visuell anzugeben, das Wort's relative positiven oder negativen Beitrag zum Ergebnis Relevanz.</span><span class="sxs-lookup"><span data-stu-id="310c6-p114">In addition to Relevance scores, Advanced eDiscovery calculates and assigns keyword weights that consider the keyword context. The same word in a file can be assigned different weights, depending on context and location. Each keyword is marked using an increasing scale of color intensity ranging from yellow to dark orange and varying shades of gray. Color coding is used to visually indicate the word's relative positive or negative contribution to the Relevance score.</span></span> 
  
<span data-ttu-id="310c6-159">In einem Szenario mit mehreren Problem Groß-/Kleinschreibung kann ein Analysebericht Transparenz für jedes Problem generiert werden.</span><span class="sxs-lookup"><span data-stu-id="310c6-159">In a multiple-issue case scenario, a Transparency analysis report can be generated for each issue.</span></span>
  
1. <span data-ttu-id="310c6-160">Klicken Sie in der Menüleiste auf das Symbol **Cogwheel** .</span><span class="sxs-lookup"><span data-stu-id="310c6-160">In the menu bar, click the **Cogwheel** icon.</span></span> 
    
2. <span data-ttu-id="310c6-161">In der **Einstellungen und Dienstprogramme \> Dienstprogramme** Registerkarte **Transparenz Analysis \> Setup**.</span><span class="sxs-lookup"><span data-stu-id="310c6-161">In the **Settings and utilities \> Utilities** tab, select **Transparency analysis \> Setup**.</span></span>
    
3. <span data-ttu-id="310c6-162">In ** Datei ID **, geben Sie die Datei-ID der Datei zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="310c6-162">In ** File ID **, enter the file ID of the file to process.</span></span>
    
4. <span data-ttu-id="310c6-163">Wählen Sie in der Liste **Problem** das Problem relevant sind.</span><span class="sxs-lookup"><span data-stu-id="310c6-163">In the **Issue** list, select the pertinent issue.</span></span> 
    
5. <span data-ttu-id="310c6-p115">Klicken Sie auf **Transparenz Analyse**. Nach Abschluss des Vorgangs wird die zeigt, wie die Schlüsselwortfarben im markierten die allgemeine Relevanz Bewertung entsprechen der Analysebericht Transparenz für die Datei angezeigt.</span><span class="sxs-lookup"><span data-stu-id="310c6-p115">Click **Transparency analysis**. Upon completion, the Transparency analysis report for the file is displayed, which shows how the marked keyword colors correlate to the overall Relevance score.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="310c6-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="310c6-166">See also</span></span>

[<span data-ttu-id="310c6-167">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="310c6-167">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="310c6-168">Definieren von Groß-/Kleinschreibung und Mandanten-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="310c6-168">Defining case and tenant settings</span></span>](define-case-and-tenant-settings-in-advanced-ediscovery.md)

