---
title: Suche und Tagging
ms.author: chrfox
author: chrfox
manager: laurawi
ms.audience: ITPro
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: In Advanced eDiscovery können Sie mithilfe des Such-und Markierungs Moduls die Dokumente in Ihrem Fall suchen, in der Vorschau anzeigen und organisieren. Dieses Modul befindet sich derzeit in der Beta Version.
ms.openlocfilehash: 58913a01f30b4169470592f5fc271e3ce785ac5d
ms.sourcegitcommit: a80bd8626720fabdf592b84e4424cd3a83d08280
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30222964"
---
# <a name="search-and-tagging"></a><span data-ttu-id="419b3-104">Suche und Tagging</span><span class="sxs-lookup"><span data-stu-id="419b3-104">Search and Tagging</span></span>

<span data-ttu-id="419b3-p102">In Advanced eDiscovery können Sie mithilfe des Such-und Markierungs Moduls die Dokumente in Ihrem Fall suchen, in der Vorschau anzeigen und organisieren. Dieses Modul befindet sich derzeit in der Beta Version. Eine kurze Übersicht über das Suchen und markieren finden Sie unter [Verwalten von Daten mit erweitertem eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) -Video.</span><span class="sxs-lookup"><span data-stu-id="419b3-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta. For a brief demonstration of searching and tagging, see the [Manage your data with Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) video.</span></span>

> [!NOTE]
> <span data-ttu-id="419b3-p103">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="419b3-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="419b3-110">Durchsuchen der Dokumente in Ihrem Fall</span><span class="sxs-lookup"><span data-stu-id="419b3-110">Search the documents in your case</span></span>

<span data-ttu-id="419b3-p104">Nachdem Sie Dokumente in einem erweiterten eDiscovery-Fall verarbeitet haben (und optional das Modul Analyze oder Relevance ausführen), können Sie die Suche und das Tagging verwenden, um Dokumente zu durchsuchen und Sie dann zu organisieren, indem Sie fallspezifische Tags (auch als Bezeichnungen bezeichnet) anwenden. Sie können eine Suchabfrage mithilfe der bereitgestellten Bedingungs Karten oder mithilfe einer KQL-artigen Abfragesprache in der Schlüsselwort-Bedingungs Karte definieren. Allgemeine KQL-Syntax wie AND, OR, NOT und NEAR (n) werden unterstützt, ebenso wie nachgestellte mehrstellige Platzhalterzeichen (\*).</span><span class="sxs-lookup"><span data-stu-id="419b3-p104">After you have processed documents in an Advanced eDiscovery case (and optionally run the Analyze or Relevance module), you can use the Search and Tagging to search documents and then organize them by applying case-specific tags (also called labels). You can define a search query using the provided condition cards or by using a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*).</span></span> 

<span data-ttu-id="419b3-p105">In der folgenden Tabelle sind die Eigenschaften aufgeführt, die Sie mithilfe einer KQL-Schlüsselwortabfrage suchen können. Alternativ können Sie eine Bedingungs Karte für im Advanced eDiscovery Search Tool verwenden, um einer Suchabfrage eine Bedingung (für ausgewählte Eigenschaften) hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="419b3-p105">The following table lists the properties that you can search for using a KQL keyword query. Alternatively, you can use a condition card for in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query.</span></span>

|<span data-ttu-id="419b3-116">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="419b3-116">**Property**</span></span>|<span data-ttu-id="419b3-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="419b3-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="419b3-118">**caselabel**</span><span class="sxs-lookup"><span data-stu-id="419b3-118">**caselabel**</span></span> <br/> | <span data-ttu-id="419b3-119">Der Name des Tags, das erstellt/angewendet wird, wenn ein Dokument markiert wird.</span><span class="sxs-lookup"><span data-stu-id="419b3-119">The name of the tag created/applied when a document is tagged.</span></span> <br/> |
|<span data-ttu-id="419b3-120">**Custodian**</span><span class="sxs-lookup"><span data-stu-id="419b3-120">**custodian**</span></span> <br/> | <span data-ttu-id="419b3-121">Die einem Dokument zugeordnete Depotbank; Einschränkungen vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="419b3-121">The custodian associated with a document; subject to limitations.</span></span> <br/> |
|<span data-ttu-id="419b3-122">**Datum**</span><span class="sxs-lookup"><span data-stu-id="419b3-122">**date**</span></span> <br/> | <span data-ttu-id="419b3-123">Sendedatum für e-Mail; das geänderte Datum für Website Dokumente.</span><span class="sxs-lookup"><span data-stu-id="419b3-123">Sent date for email; the modified date for site documents.</span></span> <br/> |
|<span data-ttu-id="419b3-124">**FileID**</span><span class="sxs-lookup"><span data-stu-id="419b3-124">**fileid**</span></span> <br/> | <span data-ttu-id="419b3-125">Die Datei-ID innerhalb der Anfrage.</span><span class="sxs-lookup"><span data-stu-id="419b3-125">The File ID within the case.</span></span> <br/> |
|<span data-ttu-id="419b3-126">**filetype**</span><span class="sxs-lookup"><span data-stu-id="419b3-126">**filetype**</span></span> <br/> | <span data-ttu-id="419b3-127">Die systemeigene Dateierweiterung.</span><span class="sxs-lookup"><span data-stu-id="419b3-127">The native file extension.</span></span> <br/> |
|<span data-ttu-id="419b3-128">**fileclass**</span><span class="sxs-lookup"><span data-stu-id="419b3-128">**fileclass**</span></span> <br/> | <span data-ttu-id="419b3-129">E-Mail, Dokument oder Anlage.</span><span class="sxs-lookup"><span data-stu-id="419b3-129">Email, document, or attachment.</span></span> <br/> |
|<span data-ttu-id="419b3-130">**senderauthor**</span><span class="sxs-lookup"><span data-stu-id="419b3-130">**senderauthor**</span></span> <br/> | <span data-ttu-id="419b3-131">Der Absender für e-Mail; der Autor für Website Dokumente.</span><span class="sxs-lookup"><span data-stu-id="419b3-131">The sender for email; the author for site documents.</span></span> <br/> |
|<span data-ttu-id="419b3-132">**Größe**</span><span class="sxs-lookup"><span data-stu-id="419b3-132">**size**</span></span> <br/> | <span data-ttu-id="419b3-133">Die Größe der Datei in KB.</span><span class="sxs-lookup"><span data-stu-id="419b3-133">The size of the file in KB.</span></span> <br/> |
|<span data-ttu-id="419b3-134">**Betreff erstellt**</span><span class="sxs-lookup"><span data-stu-id="419b3-134">**subjecttitle**</span></span> <br/> | <span data-ttu-id="419b3-135">Betreff für e-Mail; der Titel für Website Dokumente.</span><span class="sxs-lookup"><span data-stu-id="419b3-135">The subject for email; the title for site documents.</span></span> <br/> |
|<span data-ttu-id="419b3-136">**bcc**</span><span class="sxs-lookup"><span data-stu-id="419b3-136">**bcc**</span></span> <br/> | <span data-ttu-id="419b3-137">Das Feld Bcc einer e-Mail.</span><span class="sxs-lookup"><span data-stu-id="419b3-137">The Bcc field of an email.</span></span> <br/> |
|<span data-ttu-id="419b3-138">**cc**</span><span class="sxs-lookup"><span data-stu-id="419b3-138">**cc**</span></span> <br/> | <span data-ttu-id="419b3-139">Das Feld Cc einer e-Mail.</span><span class="sxs-lookup"><span data-stu-id="419b3-139">The Cc field of an email.</span></span> <br/> |
|<span data-ttu-id="419b3-140">**Teilnehmer**</span><span class="sxs-lookup"><span data-stu-id="419b3-140">**participants**</span></span> <br/> | <span data-ttu-id="419b3-141">Die e-Mail-Adresse aller Teilnehmer in einem e-Mail-Thread, einschließlich fehlender Links.</span><span class="sxs-lookup"><span data-stu-id="419b3-141">The email address of all participants in an email thread, including for missing links.</span></span> <br/> |
|<span data-ttu-id="419b3-142">**empfangen**</span><span class="sxs-lookup"><span data-stu-id="419b3-142">**received**</span></span> <br/> | <span data-ttu-id="419b3-143">Das Datum, an dem eine e-Mail empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="419b3-143">The date an email was received.</span></span> <br/> |
|<span data-ttu-id="419b3-144">**Empfänger**</span><span class="sxs-lookup"><span data-stu-id="419b3-144">**recipients**</span></span> <br/> | <span data-ttu-id="419b3-145">Empfänger einer e-Mail, die in den Feldern "an", "CC" oder "Bcc" enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="419b3-145">Recipients of an email, included on the To, Cc, or Bcc fields.</span></span> <br/> |
|<span data-ttu-id="419b3-146">**sender**</span><span class="sxs-lookup"><span data-stu-id="419b3-146">**sender**</span></span> <br/> | <span data-ttu-id="419b3-147">Der Absender einer e-Mail.</span><span class="sxs-lookup"><span data-stu-id="419b3-147">The sender of an email.</span></span> <br/> |
|<span data-ttu-id="419b3-148">**LastModifiedDate**</span><span class="sxs-lookup"><span data-stu-id="419b3-148">**lastmodifieddate**</span></span> <br/> | <span data-ttu-id="419b3-149">Das Datum der letzten Änderung eines Website Dokuments.</span><span class="sxs-lookup"><span data-stu-id="419b3-149">The last modified date of a site document.</span></span> <br/> |
|<span data-ttu-id="419b3-150">**gesendet**</span><span class="sxs-lookup"><span data-stu-id="419b3-150">**sent**</span></span> <br/> | <span data-ttu-id="419b3-151">Das gesendete Datum einer e-Mail.</span><span class="sxs-lookup"><span data-stu-id="419b3-151">The sent date of an email.</span></span> <br/> |
|<span data-ttu-id="419b3-152">**An**</span><span class="sxs-lookup"><span data-stu-id="419b3-152">**to**</span></span> <br/> | <span data-ttu-id="419b3-153">Der Empfänger, der im Feld "an" einer e-Mail aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="419b3-153">The recipient listed in the To field of an email.</span></span> <br/> |
|<span data-ttu-id="419b3-154">**Autor**</span><span class="sxs-lookup"><span data-stu-id="419b3-154">**author**</span></span> <br/> | <span data-ttu-id="419b3-155">Der Autor eines Website Dokuments.</span><span class="sxs-lookup"><span data-stu-id="419b3-155">The author of a site document.</span></span> <br/> |
|<span data-ttu-id="419b3-156">**title**</span><span class="sxs-lookup"><span data-stu-id="419b3-156">**title**</span></span> <br/> | <span data-ttu-id="419b3-157">Der Titel eines Website Dokuments.</span><span class="sxs-lookup"><span data-stu-id="419b3-157">The title of a site document.</span></span> <br/> |
|<span data-ttu-id="419b3-158">**dominanttheme**\*</span><span class="sxs-lookup"><span data-stu-id="419b3-158">**dominanttheme**\*</span></span> <br/> | <span data-ttu-id="419b3-159">Das vorherrschende Design eines Elements.</span><span class="sxs-lookup"><span data-stu-id="419b3-159">The dominant theme of an item.</span></span> <br/> |
|<span data-ttu-id="419b3-160">**themesliste**\*</span><span class="sxs-lookup"><span data-stu-id="419b3-160">**themeslist**\*</span></span> <br/> | <span data-ttu-id="419b3-161">Designs, die einem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="419b3-161">Themes that are associated with an item.</span></span> <br/> |
|<span data-ttu-id="419b3-162">**readpercentile_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="419b3-162">**readpercentile_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="419b3-163">Das Lese-Perzentil eines Elements für das von [issuenum] definierte Problem.</span><span class="sxs-lookup"><span data-stu-id="419b3-163">The read percentile of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="419b3-164">**relevancescore_ [issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="419b3-164">**relevancescore_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="419b3-165">Die Relevanz eines Elements für das von [issuenum] definierte Problem.</span><span class="sxs-lookup"><span data-stu-id="419b3-165">The relevance score of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="419b3-166">**relevancetag_ [Tagname]**\*\*</span><span class="sxs-lookup"><span data-stu-id="419b3-166">**relevancetag_[tagname]**\*\*</span></span> <br/> | <span data-ttu-id="419b3-167">Wenn ein Element für die Relevanz manuell markiert wurde, wird es durch [Tagname] definiert.</span><span class="sxs-lookup"><span data-stu-id="419b3-167">If an item has been manually tagged for relevance, the tag defined by  [tagname].</span></span> <br/> |
|||

<span data-ttu-id="419b3-168">\*Nur verfügbar, wenn das Designmodul ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="419b3-168">\* Only available if the Themes module has been run.</span></span>

<span data-ttu-id="419b3-169">\*\*Nur verfügbar, wenn das Relevance-Modul ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="419b3-169">\*\* Only available if the Relevance module has been run.</span></span>

<span data-ttu-id="419b3-p106">Alternativ können Sie eine Bedingungs Karte im Tool für die erweiterte eDiscovery-Suche verwenden, um einer Suchabfrage eine Bedingung (für ausgewählte Eigenschaften) hinzuzufügen. Der folgende Screenshot zeigt die Bedingungen, die einer Abfrage hinzugefügt werden können. Die Spalte **Group** gibt an, ob die Eigenschaft auf e-Mails, Website Dokumente oder beides angewendet wird (angegeben durch den *allgemeinen*Wert). In dieser Spalte werden auch die durchsuchbaren Eigenschaften identifiziert, die nach der Ausführung des Relevance-Moduls verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="419b3-p106">Alternatively, you can use a condition card in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query. The following screenshot shows the conditions that can be added to a query. The **Group** column indicates whether the property applies to email, site documents, or both (indicated by the value *Common*). This column also identifies the searchable properties that are available after you run the Relevance module.</span></span>

![Suchbedingungen im Tool für die erweiterte eDiscovery-Suche](media/AeDSearchConditions.png)

<span data-ttu-id="419b3-175">Weitere Informationen zu durchsuchbaren Eigenschaften finden Sie unter [Stichwortabfragen und Suchbedingungen](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="419b3-175">For more information about searchable properties, see [Keyword queries and search conditions](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="419b3-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="419b3-176">See also</span></span>

[<span data-ttu-id="419b3-177">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="419b3-177">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="419b3-178">Bedeutung der Bewertung</span><span class="sxs-lookup"><span data-stu-id="419b3-178">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="419b3-179">Tagging und Bewertung</span><span class="sxs-lookup"><span data-stu-id="419b3-179">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="419b3-180">Tagging-und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="419b3-180">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="419b3-181">Nachverfolgen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="419b3-181">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="419b3-182">Entscheiden basierend auf den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="419b3-182">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="419b3-183">Testen der Relevanz-Analyse</span><span class="sxs-lookup"><span data-stu-id="419b3-183">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

