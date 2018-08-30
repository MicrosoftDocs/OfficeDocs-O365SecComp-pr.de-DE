---
title: Legen Sie Text ignorieren-Option für die Analyse in Office 365 erweiterte eDiscovery
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
ms.assetid: 44055727-56e8-42d7-9dc3-fb942f3901cc
description: 'Erfahren Sie, wie die Regel, um bestimmten Text ignoriert wird, wenn mit den Modulen analysieren und Prozess in Office 365 erweiterte eDiscovery definieren.  '
ms.openlocfilehash: eb7e7052979087b7dba98aac3b0c9ab75ec0d02a
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529494"
---
# <a name="set-ignore-text-option-for-analyze-in-office-365-advanced-ediscovery"></a><span data-ttu-id="00210-103">Legen Sie Text ignorieren-Option für die Analyse in Office 365 erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="00210-103">Set Ignore Text option for Analyze in Office 365 Advanced eDiscovery</span></span>

> [!NOTE]
> <span data-ttu-id="00210-p101">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="00210-p101">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
<span data-ttu-id="00210-p102">Das Feature ignorieren Text angewendet werden soll, auf alle oder auf die folgenden erweiterten eDiscovery-Module: Analysieren (in der Nähe Duplikate, E-Mail-Threads Designs) und Relevanz. Ignorierte Text wird nicht angezeigt, in der Dateien werden in Relevanz angezeigt, und die Analysis-Berechnungen verwirft des ignorierten Texts.</span><span class="sxs-lookup"><span data-stu-id="00210-p102">The Ignore Text feature can be applied to all or any of the following Advanced eDiscovery modules: Analyze (Near-duplicates, Email Threads, Themes) and Relevance. Ignored text will not appear in files displayed in Relevance, and the analysis/calculations will discard the ignored text.</span></span>
  
<span data-ttu-id="00210-p103">Wenn das Feature Text ignorieren für Module zuvor definiert wurde, die bereits ausgeführt haben, wird die Einstellung Text ignorieren geändert wird, wird nun geschützt werden. Das Feature ignorieren Text für das Modul Relevanz kann jedoch weiterhin jederzeit geändert werden.</span><span class="sxs-lookup"><span data-stu-id="00210-p103">If the Ignore Text feature was previously defined for modules that have already run, the Ignore Text setting will now be protected from being modified. However, the Ignore Text feature for the Relevance module can still be changed at any time.</span></span>
  
## <a name="how-ignore-text-filters-are-applied"></a><span data-ttu-id="00210-110">Anwenden von Filtern für Text ignorieren</span><span class="sxs-lookup"><span data-stu-id="00210-110">How Ignore Text filters are applied</span></span>

<span data-ttu-id="00210-p104">Mehrere Text ignorieren Filter werden in der Reihenfolge angewendet, dass sie eingegeben wurden. Zum Ändern der Reihenfolge, in der sie angewendet werden, müssen sie gelöscht und in der gewünschten Reihenfolge erneut eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="00210-p104">Multiple Ignore Text filters are applied in the order that they were entered. To change the order in which they are applied, they must be deleted and re-entered in the desired order.</span></span>
  
<span data-ttu-id="00210-113">Beispiel: bei der Textinhalt ist: "DAVE BOB ALICE CAROL EVE", die im folgenden sind Beispiele für ignorieren Texteinträge und die Ergebnisse:</span><span class="sxs-lookup"><span data-stu-id="00210-113">For example, if the text content is: "DAVE BOB ALICE CAROL EVE", the following are samples of Ignore Text entries and the results:</span></span>
  
||||
|:-----|:-----|:-----|
|<span data-ttu-id="00210-114">**Texteinträge ignorieren**</span><span class="sxs-lookup"><span data-stu-id="00210-114">**Ignore Text entries**</span></span> <br/> |**==\>** <br/> |<span data-ttu-id="00210-115">**Ergebnisse**</span><span class="sxs-lookup"><span data-stu-id="00210-115">**Results**</span></span> <br/> |
|<span data-ttu-id="00210-116">"ALICE", "BOB CAROL"</span><span class="sxs-lookup"><span data-stu-id="00210-116">"ALICE", "BOB CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="00210-117">"DAVE EVE"</span><span class="sxs-lookup"><span data-stu-id="00210-117">"DAVE EVE"</span></span>  <br/> |
|<span data-ttu-id="00210-118">"ALICE", "BOB ALICE CAROL"</span><span class="sxs-lookup"><span data-stu-id="00210-118">"ALICE", "BOB ALICE CAROL"</span></span>  <br/> |==\>  <br/> |<span data-ttu-id="00210-119">"DAVE BOB CAROL EVE"</span><span class="sxs-lookup"><span data-stu-id="00210-119">"DAVE BOB CAROL EVE"</span></span>  <br/> |
   
<span data-ttu-id="00210-120">Die zweite ignorieren Texteingabe ist nicht implementiert, da die Zeichenfolge als solche nicht gefunden wird, nachdem der erste ignorieren Text angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="00210-120">The second Ignore Text entry is not implemented because the string is not found as such AFTER the first Ignore Text has been applied.</span></span>
  
## <a name="use-regular-expressions-when-defining-ignore-text"></a><span data-ttu-id="00210-121">Verwenden Sie reguläre Ausdrücke beim Definieren der Text ignorieren</span><span class="sxs-lookup"><span data-stu-id="00210-121">Use regular expressions when defining Ignore Text</span></span>

<span data-ttu-id="00210-p105">Reguläre Ausdrücke werden für die Verwendung unterstützt, wenn Text ignorieren definieren. Es folgen Beispiele für die Syntax für reguläre Ausdrücke und Verwendung:</span><span class="sxs-lookup"><span data-stu-id="00210-p105">Regular expressions are supported for use when defining Ignore Text. The following are examples of regular expression syntax and usage:</span></span>
  
- <span data-ttu-id="00210-124">So entfernen Sie (ignorieren) Text vom Anfang bis zum Ende einer Zeile:</span><span class="sxs-lookup"><span data-stu-id="00210-124">To remove (ignore) text from Begin until the end of a line:</span></span>
    
     `Begin(.*)$`
    
    <span data-ttu-id="00210-125">Dabei ist "Begin" das erste Auftreten des diese Zeichenfolge in der Zeile.</span><span class="sxs-lookup"><span data-stu-id="00210-125">where "Begin" is the initial occurrence of this string in the line.</span></span>
    
    <span data-ttu-id="00210-126">Zum Beispiel für den folgenden Text:</span><span class="sxs-lookup"><span data-stu-id="00210-126">For example, for the following text:</span></span>
    
    <span data-ttu-id="00210-127">**"Dies ist ersten Satz und die erste Zeile**</span><span class="sxs-lookup"><span data-stu-id="00210-127">**"This is first sentence and first line**</span></span>
    
    <span data-ttu-id="00210-128">**Dies ist die zweite Satz und zweiten Zeile"**</span><span class="sxs-lookup"><span data-stu-id="00210-128">**This is second sentence and second line"**</span></span>
    
    <span data-ttu-id="00210-129">der reguläre Ausdruck first(.\*) $ führt zu:</span><span class="sxs-lookup"><span data-stu-id="00210-129">the Regular Expression first(.\*)$ will result in:</span></span>
    
    <span data-ttu-id="00210-130">**"Dies ist**</span><span class="sxs-lookup"><span data-stu-id="00210-130">**"This is**</span></span>
    
    <span data-ttu-id="00210-131">**Dies ist die zweite Satz und zweiten Zeile"**</span><span class="sxs-lookup"><span data-stu-id="00210-131">**This is second sentence and second line"**</span></span>
    
- <span data-ttu-id="00210-132">So entfernen Sie Haftungsausschluss und rechtliche Anweisungen automatisch am Ende des e-Mail-Threads eingefügt:</span><span class="sxs-lookup"><span data-stu-id="00210-132">To remove disclaimers and legal statements automatically inserted at the end of email threads:</span></span>
    
     `Begin(.|\s)*End`
    
    <span data-ttu-id="00210-133">wobei "Begin" und "End" eindeutige Zeichenfolgen am Anfang und Ende eines Absatzes umbrochenen Text sind.</span><span class="sxs-lookup"><span data-stu-id="00210-133">where "Begin" and "End" are unique strings at the beginning and end of a wrapped text paragraph.</span></span> 
    
    <span data-ttu-id="00210-134">Im folgende reguläre Ausdruck entfernt beispielsweise Haftungsausschluss und rechtliche Anweisungen, die in der e-Mail-Thread zwischen den Zeichenfolgen Begin- und End wurden:</span><span class="sxs-lookup"><span data-stu-id="00210-134">For example, the following regular expression will remove disclaimers and legal statements that were in the email thread between the Begin and End strings:</span></span>
    
    <span data-ttu-id="00210-135">**Diese Nachricht enthält vertrauliche Informationen (. | \s)\*, wenn die Überprüfung erforderlich ist, fordern Sie eine harte Kopie-Version**</span><span class="sxs-lookup"><span data-stu-id="00210-135">**This message contains confidential information (.|\s)\*If verification is required please request a hard-copy version**</span></span>
    
- <span data-ttu-id="00210-136">So entfernen Sie einen Haftungsausschluss (einschließlich Sonderzeichen)</span><span class="sxs-lookup"><span data-stu-id="00210-136">To remove a disclaimer (including special characters):</span></span> 
    
    <span data-ttu-id="00210-137">Zum Beispiel für den folgenden Text (mit der Haftungsausschluss hier dargestellt durch x):</span><span class="sxs-lookup"><span data-stu-id="00210-137">For example, for the following text (with the disclaimer represented here by x's):</span></span> 
    
    <span data-ttu-id="00210-138">**/\*\ Diese Nachricht enthält vertrauliche Informationen. Xxxx-xxxx**</span><span class="sxs-lookup"><span data-stu-id="00210-138">**/\*\ This message contains confidential information. xxxx xxxx**</span></span>
    
    <span data-ttu-id="00210-139">**Xxxx Xxxx Xxxx Xxxx Xxxx-Xxxx-xxxx**</span><span class="sxs-lookup"><span data-stu-id="00210-139">**xxxx xxxx xxxx xxxx xxxx xxxx xxxx**</span></span>
    
    <span data-ttu-id="00210-140">\**Xxxx-Xxxx, wenn die Überprüfung erforderlich ist, fordern Sie eine harte Kopie Version. /\*\**</span><span class="sxs-lookup"><span data-stu-id="00210-140">\**xxxx xxxx If verification is required, please request a hard-copy version. /\*\**</span></span>
    
    <span data-ttu-id="00210-141">der reguläre Ausdruck, den oben genannten Haftungsausschluss entfernen sollte sein:</span><span class="sxs-lookup"><span data-stu-id="00210-141">the regular expression to remove the above disclaimer should be:</span></span> 
    
    <span data-ttu-id="00210-142">**\/\\*\\Diese Nachricht enthält vertrauliche Informationen\.(. | \s)\* , wenn die Überprüfung erforderlich ist, fordern Sie eine harte Kopie Version\.\/\\*\\**</span><span class="sxs-lookup"><span data-stu-id="00210-142">**\/\\*\\ This message contains confidential information\.(.|\s)\* If verification is required please request a hard-copy version\. \/\\*\\**</span></span>
    
- <span data-ttu-id="00210-143">Regeln für den regulären Ausdruck:</span><span class="sxs-lookup"><span data-stu-id="00210-143">Regular expression rules:</span></span>
    
  - <span data-ttu-id="00210-144">Alle Zeichen, die nicht Teil des Alphabets mit Ausnahme aufhören, "_" sind und "-" muss vorangestellt werden "\".</span><span class="sxs-lookup"><span data-stu-id="00210-144">Any characters that are not part of the alphabet except for space(s), "_" and "-" must be preceded by "\".</span></span>
    
  - <span data-ttu-id="00210-145">Feld reguläre eExpression kann unbegrenzte Länge sein.</span><span class="sxs-lookup"><span data-stu-id="00210-145">The regular eExpression field can be unlimited length.</span></span>
    
> [!TIP]
> <span data-ttu-id="00210-146">Eine Erläuterung und Informationen zur Syntax von regulären Ausdrücken finden Sie unter: [Regulären Ausdruck Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="00210-146">For an explanation and detailed syntax of regular expressions, see: [Regular Expression Language - Quick Reference](https://msdn.microsoft.com/en-us/library/az24scfc%28v=vs.110%29.aspx).</span></span> 
  
## <a name="define-ignore-text-rule"></a><span data-ttu-id="00210-147">Definieren der Regel Text ignorieren</span><span class="sxs-lookup"><span data-stu-id="00210-147">Define Ignore Text rule</span></span>

1. <span data-ttu-id="00210-148">In der **verwalten \> Analyze \> analysieren Optionen** Registerkarte im Abschnitt **Text ignoriert wird** , klicken Sie auf die **+** Symbol, um eine Regel hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="00210-148">In the **Manage \> Analyze \> Analyze options** tab, in the **Ignore Text** section, click the **+** icon to add a rule.</span></span> 
    
2. <span data-ttu-id="00210-149">Geben Sie im Dialogfeld **Ignorieren Text hinzufügen** im Feld **Name** einen Namen für die Regel Text ignoriert wird.</span><span class="sxs-lookup"><span data-stu-id="00210-149">In the **Add Ignore Text** dialog, in the **Name** field, type a name for the Ignore Text rule.</span></span> 
    
    ![Ignorierten Text hinzufügen](media/98e5129b-2667-4692-86fa-2d0117187a7f.png)
  
3. <span data-ttu-id="00210-p106">Geben Sie in das **Textfeld** den Text ignoriert werden soll. Das Textfeld ermöglicht eine unbegrenzte Anzahl von Zeichen.</span><span class="sxs-lookup"><span data-stu-id="00210-p106">In the **Text** box, type the text to be ignored. The text field allows an unlimited number of characters.</span></span> 
    
    > [!TIP]
    > <span data-ttu-id="00210-153">Wie im obigen Fenster angezeigt wird, klicken Sie auf **Glühbirne** um allgemeine Syntax Richtlinien für die Regel ignorieren Text anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="00210-153">As shown in the window above, click **light bulb** to see common syntax guidelines for the Ignore Text rule.</span></span> 
  
4. <span data-ttu-id="00210-154">Wählen Sie bei Bedarf das Kontrollkästchen **Groß-/Kleinschreibung beachten** .</span><span class="sxs-lookup"><span data-stu-id="00210-154">Select the **Case sensitive** check box, if desired.</span></span> 
    
5. <span data-ttu-id="00210-155">Wählen Sie in der Liste **Übernehmen für** die erweiterte eDiscovery-Module in der Definition die angewendet.</span><span class="sxs-lookup"><span data-stu-id="00210-155">In the **Apply to** list, select the Advanced eDiscovery modules in which to apply the definition.</span></span> 
    
6. <span data-ttu-id="00210-p107">Wenn Sie einen Testlauf auf Beispieltext möchten, geben Sie in das Textfeld **Eingabe** Beispieltext ein, und klicken Sie auf **Testen**. Die Ergebnisse werden in das Textfeld **Ausgabe** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00210-p107">If you want a test run on sample text, type sample text in the **Input** text box and click **Test**. The results are displayed in the **Output** text box.</span></span> 
    
7. <span data-ttu-id="00210-p108">Klicken Sie auf **OK** , um die Regel ignorieren Text zu speichern. Die definierte Text ignorieren Regel wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="00210-p108">Click **OK** to save the Ignore Text rule. The defined Ignore Text rule is displayed.</span></span> 
    
    ![Set hat Textname ignoriert](media/3a788ac3-4a1c-46c9-89bd-7ff32d68ce23.png)
  
## <a name="see-also"></a><span data-ttu-id="00210-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00210-161">See also</span></span>

[<span data-ttu-id="00210-162">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="00210-162">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="00210-163">Grundlegendes zu Dokument Ähnlichkeit</span><span class="sxs-lookup"><span data-stu-id="00210-163">Understanding document similarity</span></span>](understand-document-similarity-in-advanced-ediscovery.md)
  
[<span data-ttu-id="00210-164">Festlegen von Optionen für Analyse</span><span class="sxs-lookup"><span data-stu-id="00210-164">Setting Analyze options</span></span>](set-analyze-options-in-advanced-ediscovery.md)
  
[<span data-ttu-id="00210-165">Analysieren der Einstellung Erweiterte Einstellungen</span><span class="sxs-lookup"><span data-stu-id="00210-165">Setting Analyze advanced settings</span></span>](set-analyze-advanced-settings-in-advanced-ediscovery.md)
  
[<span data-ttu-id="00210-166">Anzeigen von Ergebnissen der Analyse</span><span class="sxs-lookup"><span data-stu-id="00210-166">Viewing Analyze results</span></span>](view-analyze-results-in-advanced-ediscovery.md)

