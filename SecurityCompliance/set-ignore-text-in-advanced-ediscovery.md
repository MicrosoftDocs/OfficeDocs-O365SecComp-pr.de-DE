---
title: Option Text ignorieren festlegen für Analyse in Office 365 Advanced eDiscovery
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 9/14/2017
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MOE150
- MET150
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Erfahren Sie, wie Sie die Regel definieren, um bestimmten Text zu ignorieren, wenn Sie die Analyse-und Prozessmodule in Office 365 Advanced eDiscovery verwenden.  '
ms.openlocfilehash: 70d9879f1cb6b3def06ff978fc2f7fa8f20a92f0
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34156677"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a><span data-ttu-id="95327-103">Option Text ignorieren festlegen für Analyse in Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="95327-103">Set Ignore Text option for Analyze in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="95327-p101">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="95327-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="95327-106">Das Feature Text ignorieren kann auf alle oder alle der folgenden erweiterten eDiscovery-Module angewendet werden: analysieren (nahe Duplikate, e-Mail-Threads, Designs) und Relevanz.</span><span class="sxs-lookup"><span data-stu-id="95327-106">The Ignore Text feature can be applied to all or any of the following Advanced eDiscovery modules: Analyze (Near-duplicates, Email Threads, Themes) and Relevance.</span></span> <span data-ttu-id="95327-107">Der ignorierte Text wird nicht in den für Relevanz angezeigten Dateien angezeigt, und die Analyse/Berechnungen verwerfen den ignorierten Text.</span><span class="sxs-lookup"><span data-stu-id="95327-107">Ignored text will not appear in files displayed in Relevance, and the analysis/calculations will discard the ignored text.</span></span>
  
<span data-ttu-id="95327-108">Wenn das Feature Text ignorieren zuvor für Module definiert wurde, die bereits ausgeführt wurden, wird die Einstellung Text ignorieren jetzt vor der Änderung geschützt.</span><span class="sxs-lookup"><span data-stu-id="95327-108">If the Ignore Text feature was previously defined for modules that have already run, the Ignore Text setting will now be protected from being modified.</span></span> <span data-ttu-id="95327-109">Die Funktion Text ignorieren für das Modul Relevanz kann jedoch jederzeit noch geändert werden.</span><span class="sxs-lookup"><span data-stu-id="95327-109">However, the Ignore Text feature for the Relevance module can still be changed at any time.</span></span>
  
## <a name="how-ignore-text-filters-are-applied"></a><span data-ttu-id="95327-110">Wie ignorieren von Text Filtern angewendet wird</span><span class="sxs-lookup"><span data-stu-id="95327-110">How Ignore Text filters are applied</span></span>

<span data-ttu-id="95327-111">Mehrere Text Filter ignorieren werden in der Reihenfolge angewendet, in der Sie eingegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="95327-111">Multiple Ignore Text filters are applied in the order that they were entered.</span></span> <span data-ttu-id="95327-112">Um die Reihenfolge zu ändern, in der Sie angewendet werden, müssen Sie gelöscht und in der gewünschten Reihenfolge erneut eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="95327-112">To change the order in which they are applied, they must be deleted and re-entered in the desired order.</span></span>
  
<span data-ttu-id="95327-113">Wenn es sich beispielsweise um den Textinhalt handelt: "Dave Bob Alice Carol Eve", im folgenden finden Sie Beispiele für Ignore-Texteinträge und die Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="95327-113">For example, if the text content is: "DAVE BOB ALICE CAROL EVE", the following are samples of Ignore Text entries and the results:</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="95327-114">**Text Einträge ignorieren**</span><span class="sxs-lookup"><span data-stu-id="95327-114">**Ignore Text entries**</span></span> <br/> |**==\>** <br/> |<span data-ttu-id="95327-115">**Ergebnisse**</span><span class="sxs-lookup"><span data-stu-id="95327-115">**Results**</span></span> <br/> |
|<span data-ttu-id="95327-116">"Alice", "Bob Carol"</span><span class="sxs-lookup"><span data-stu-id="95327-116">"ALICE", "BOB CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="95327-117">"Dave Eve"</span><span class="sxs-lookup"><span data-stu-id="95327-117">"DAVE EVE"</span></span>  <br/> |
|<span data-ttu-id="95327-118">"Alice", "Bob Alice Carol"</span><span class="sxs-lookup"><span data-stu-id="95327-118">"ALICE", "BOB ALICE CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="95327-119">"Dave Bob Carol Eve"</span><span class="sxs-lookup"><span data-stu-id="95327-119">"DAVE BOB CAROL EVE"</span></span>  <br/> |
   
<span data-ttu-id="95327-120">Der zweite Ignore-Texteintrag ist nicht implementiert, da die Zeichenfolge nicht als solches gefunden wird, nachdem der erste Text ignoriert wurde.</span><span class="sxs-lookup"><span data-stu-id="95327-120">The second Ignore Text entry is not implemented because the string is not found as such AFTER the first Ignore Text has been applied.</span></span>
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a><span data-ttu-id="95327-121">Verwenden regulärer Ausdrücke beim Definieren von Text ignorieren</span><span class="sxs-lookup"><span data-stu-id="95327-121">Use regular expressions when defining Ignore Text</span></span>

<span data-ttu-id="95327-122">Reguläre Ausdrücke werden für die Verwendung beim Definieren von Ignore-Text unterstützt.</span><span class="sxs-lookup"><span data-stu-id="95327-122">Regular expressions are supported for use when defining Ignore Text.</span></span> <span data-ttu-id="95327-123">Im folgenden finden Sie Beispiele für Syntax und Verwendung von regulären Ausdrücken:</span><span class="sxs-lookup"><span data-stu-id="95327-123">The following are examples of regular expression syntax and usage:</span></span>
  
- <span data-ttu-id="95327-124">So entfernen Sie Text von Anfang bis zum Ende einer Zeile (ignorieren):</span><span class="sxs-lookup"><span data-stu-id="95327-124">To remove (ignore) text from Begin until the end of a line:</span></span>
    
     `Begin(.*)$`
    
    <span data-ttu-id="95327-125">wobei "BEGIN" das erste Vorkommen dieser Zeichenfolge in der Linie ist.</span><span class="sxs-lookup"><span data-stu-id="95327-125">where "Begin" is the initial occurrence of this string in the line.</span></span>
    
    <span data-ttu-id="95327-126">Beispielsweise für den folgenden Text:</span><span class="sxs-lookup"><span data-stu-id="95327-126">For example, for the following text:</span></span>
    
    <span data-ttu-id="95327-127">**"Dies ist der erste Satz und die erste Textreihe.**</span><span class="sxs-lookup"><span data-stu-id="95327-127">**"This is first sentence and first line**</span></span>
    
    <span data-ttu-id="95327-128">**Dies ist der zweite Satz und die zweite Reihe "**</span><span class="sxs-lookup"><span data-stu-id="95327-128">**This is second sentence and second line"**</span></span>
    
    <span data-ttu-id="95327-129">der reguläre Ausdruck zuerst (.\*) $ führt zu:</span><span class="sxs-lookup"><span data-stu-id="95327-129">the Regular Expression first(.\*)$ will result in:</span></span>
    
    <span data-ttu-id="95327-130">**"Dies ist**</span><span class="sxs-lookup"><span data-stu-id="95327-130">**"This is**</span></span>
    
    <span data-ttu-id="95327-131">**Dies ist der zweite Satz und die zweite Reihe "**</span><span class="sxs-lookup"><span data-stu-id="95327-131">**This is second sentence and second line"**</span></span>
    
- <span data-ttu-id="95327-132">So entfernen Sie Haftungsausschlüsse und rechtliche Anweisungen, die am Ende der e-Mail-Threads automatisch eingefügt werden:</span><span class="sxs-lookup"><span data-stu-id="95327-132">To remove disclaimers and legal statements automatically inserted at the end of email threads:</span></span>
    
     `Begin(.|\s)*End`
    
    <span data-ttu-id="95327-133">wobei "BEGIN" und "End" eindeutige Zeichenfolgen am Anfang und am Ende eines umgebrochenen Textabsatzes sind.</span><span class="sxs-lookup"><span data-stu-id="95327-133">where "Begin" and "End" are unique strings at the beginning and end of a wrapped text paragraph.</span></span> 
    
    <span data-ttu-id="95327-134">Beispielsweise werden im folgenden regulären Ausdruck Haftungsausschlüsse und rechtliche Anweisungen entfernt, die sich im e-Mail-Thread zwischen den Zeichenfolgen BEGIN und End befanden:</span><span class="sxs-lookup"><span data-stu-id="95327-134">For example, the following regular expression will remove disclaimers and legal statements that were in the email thread between the Begin and End strings:</span></span>
    
    <span data-ttu-id="95327-135">**Diese Nachricht enthält vertrauliche Informationen (. | \s)\*wenn eine Überprüfung erforderlich ist, fordern Sie eine Hardcopy-Version an.**</span><span class="sxs-lookup"><span data-stu-id="95327-135">**This message contains confidential information (.|\s)\*If verification is required please request a hard-copy version**</span></span>
    
- <span data-ttu-id="95327-136">So entfernen Sie einen Haftungsausschluss (einschließlich Sonderzeichen):</span><span class="sxs-lookup"><span data-stu-id="95327-136">To remove a disclaimer (including special characters):</span></span> 
    
    <span data-ttu-id="95327-137">Beispielsweise für den folgenden Text (mit dem Haftungsausschluss, der hier von x dargestellt wird):</span><span class="sxs-lookup"><span data-stu-id="95327-137">For example, for the following text (with the disclaimer represented here by x's):</span></span> 
    
    <span data-ttu-id="95327-138">**/\*\ Diese Nachricht enthält vertrauliche Informationen. xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="95327-138">**/\*\ This message contains confidential information. xxxx xxxx**</span></span>
    
    <span data-ttu-id="95327-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span><span class="sxs-lookup"><span data-stu-id="95327-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span></span>
    
    <span data-ttu-id="95327-140">\**xxxx xxxx wenn eine Überprüfung erforderlich ist, fordern Sie bitte eine Hardcopy-Version an. /\*\**</span><span class="sxs-lookup"><span data-stu-id="95327-140">\**xxxx xxxx If verification is required, please request a hard-copy version. /\*\**</span></span>
    
    <span data-ttu-id="95327-141">der reguläre Ausdruck zum Entfernen des obigen Haftungsausschlusses sollte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="95327-141">the regular expression to remove the above disclaimer should be:</span></span> 
    
    <span data-ttu-id="95327-142">**\/\\*\\Diese Nachricht enthält vertrauliche\.Informationen (. | \s)\* wenn eine Überprüfung erforderlich ist, fordern Sie eine Hardcopy\. -Version an.\/\\*\\**</span><span class="sxs-lookup"><span data-stu-id="95327-142">**\/\\*\\ This message contains confidential information\.(.|\s)\* If verification is required please request a hard-copy version\. \/\\*\\**</span></span>
    
- <span data-ttu-id="95327-143">Regeln für reguläre Ausdrücke:</span><span class="sxs-lookup"><span data-stu-id="95327-143">Regular expression rules:</span></span>
    
  - <span data-ttu-id="95327-144">Alle Zeichen, die nicht Teil des Alphabets sind, mit Ausnahme von Leerzeichen, "_" und "-" muss vorangestellt werden\".</span><span class="sxs-lookup"><span data-stu-id="95327-144">Any characters that are not part of the alphabet except for space(s), "_" and "-" must be preceded by "\".</span></span>
    
  - <span data-ttu-id="95327-145">Das reguläre eExpression-Feld kann unbegrenzte Länge aufweisen.</span><span class="sxs-lookup"><span data-stu-id="95327-145">The regular eExpression field can be unlimited length.</span></span>
    
> [!TIP]
> <span data-ttu-id="95327-146">Eine Erklärung und ausführliche Syntax für reguläre Ausdrücke finden Sie unter: [Regular Expression Language-Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="95327-146">For an explanation and detailed syntax of regular expressions, see: [Regular Expression Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span></span> 
  
## <a name="define-ignore-text-rule"></a><span data-ttu-id="95327-147">Definieren von Ignore-Text Regel</span><span class="sxs-lookup"><span data-stu-id="95327-147">Define Ignore Text rule</span></span>

1. <span data-ttu-id="95327-148">Klicken Sie auf der Registerkarte analysiere **+** \*\* \> \> Analyseoptionen verwalten\*\* im Abschnitt **Text ignorieren** auf das Symbol, um eine Regel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="95327-148">In the **Manage \> Analyze \> Analyze options** tab, in the **Ignore Text** section, click the **+** icon to add a rule.</span></span> 
    
2. <span data-ttu-id="95327-149">Geben Sie im Dialogfeld **Text ignorieren hinzufügen** in das Feld **Name** einen Namen für die Regel Text ignorieren ein.</span><span class="sxs-lookup"><span data-stu-id="95327-149">In the **Add Ignore Text** dialog, in the **Name** field, type a name for the Ignore Text rule.</span></span> 
    
    ![Ignorierten Text hinzufügen](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. <span data-ttu-id="95327-151">Geben Sie \*\*\*\* in das Textfeld den zu ignorierenden Text ein.</span><span class="sxs-lookup"><span data-stu-id="95327-151">In the **Text** box, type the text to be ignored.</span></span> <span data-ttu-id="95327-152">Das Textfeld erlaubt eine unbegrenzte Anzahl von Zeichen.</span><span class="sxs-lookup"><span data-stu-id="95327-152">The text field allows an unlimited number of characters.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="95327-153">Klicken Sie wie im obigen Fenster gezeigt auf \*\*\*\* Glühbirne, um allgemeine Syntax Richtlinien für die Regel Text ignorieren anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="95327-153">As shown in the window above, click **light bulb** to see common syntax guidelines for the Ignore Text rule.</span></span> 
  
4. <span data-ttu-id="95327-154">Aktivieren Sie bei Bedarf das Kontrollkästchen **groß** -/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="95327-154">Select the **Case sensitive** check box, if desired.</span></span> 
    
5. <span data-ttu-id="95327-155">Wählen Sie in der Liste **übernehmen für** die erweiterten eDiscovery-Module aus, in denen die Definition angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="95327-155">In the **Apply to** list, select the Advanced eDiscovery modules in which to apply the definition.</span></span> 
    
6. <span data-ttu-id="95327-156">Wenn Sie einen Testlauf für Beispieltext ausführen möchten, geben Sie Beispieltext in das **Eingabe** Textfeld ein, und klicken Sie auf **Testen**.</span><span class="sxs-lookup"><span data-stu-id="95327-156">If you want a test run on sample text, type sample text in the **Input** text box and click **Test**.</span></span> <span data-ttu-id="95327-157">Die Ergebnisse werden im Textfeld **Ausgabe** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95327-157">The results are displayed in the **Output** text box.</span></span> 
    
7. <span data-ttu-id="95327-158">Klicken Sie auf **OK** , um die Regel Text ignorieren zu speichern.</span><span class="sxs-lookup"><span data-stu-id="95327-158">Click **OK** to save the Ignore Text rule.</span></span> <span data-ttu-id="95327-159">Die definierte Regel Ignore Text wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95327-159">The defined Ignore Text rule is displayed.</span></span> 
    
    ![Ignorierten Textnamen festlegen](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a><span data-ttu-id="95327-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95327-161">See also</span></span>

[<span data-ttu-id="95327-162">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="95327-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="95327-163">Grundlegendes zur Dokument Ähnlichkeit</span><span class="sxs-lookup"><span data-stu-id="95327-163">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="95327-164">Festlegen von Analyseoptionen</span><span class="sxs-lookup"><span data-stu-id="95327-164">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="95327-165">Einstellungen für die erweiterte Analyse Einstellung</span><span class="sxs-lookup"><span data-stu-id="95327-165">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="95327-166">Anzeigen von Analyseergebnissen</span><span class="sxs-lookup"><span data-stu-id="95327-166">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

