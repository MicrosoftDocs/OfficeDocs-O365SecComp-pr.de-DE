---
title: Suche und Kategorien
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: ''
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: In erweiterte eDiscovery ermöglicht das Modul Such- und Kategorien suchen, Vorschau anzeigen und organisieren die Dokumente in Ihrem Fall. In diesem Modul wird derzeit Beta.
ms.openlocfilehash: 013e559ca55e9a877dfb2f8747c4696f81e1e095
ms.sourcegitcommit: 25f1028643d8a20d17306e8b09cafea46eaf7a58
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2019
ms.locfileid: "29666145"
---
# <a name="search-and-tagging"></a><span data-ttu-id="786ac-104">Suche und Kategorien</span><span class="sxs-lookup"><span data-stu-id="786ac-104">Search and Tagging</span></span>

<span data-ttu-id="786ac-p102">In erweiterte eDiscovery ermöglicht das Modul Such- und Kategorien suchen, Vorschau anzeigen und organisieren die Dokumente in Ihrem Fall. In diesem Modul wird derzeit Beta. Eine kurze Demo der Suche und Kategorien finden Sie unter das [Verwalten von Daten mit erweiterten eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) -Video.</span><span class="sxs-lookup"><span data-stu-id="786ac-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta. For a brief demonstration of searching and tagging, see the [Manage your data with Advanced eDiscovery](https://www.youtube.com/watch?v=VaPYL3DHP6I) video.</span></span>

> [!NOTE]
> <span data-ttu-id="786ac-p103">Für Advanced eDiscovery ist ein Office 365 E3-Abonnement mit dem Add-On für erweiterte Compliance oder ein E5-Abonnement für Ihre Organisation erforderlich. Wenn Sie nicht über diesen Plan verfügen und Advanced eDiscovery ausprobieren möchten, können Sie sich [für eine Testversion von Office 365 Enterprise E5 anmelden](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="786ac-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="786ac-110">Suchen Sie die Dokumente in Ihrem Fall</span><span class="sxs-lookup"><span data-stu-id="786ac-110">Search the documents in your case</span></span>

<span data-ttu-id="786ac-p104">Nachdem Sie verarbeitet Dokumente in einem erweiterten eDiscovery-Fall (und optional das Modul Analyze oder Relevanz ausgeführt), können Sie die Such- und Tagging Dokumente durchsuchen, und ordnen Sie diese dann durch Anwenden von Groß-/Kleinschreibung-spezifischen Tags (auch als Etiketten bezeichnet). Sie können eine Suchabfrage mithilfe der angegebenen Bedingung Karten definiert oder mithilfe einer KQL-ähnliche Abfragesprache in den Schlüsselwörtern Bedingung Karte. Allgemeine KQL-Syntax wie AND, OR, NOT und NEAR(n) sind die unterstützten sowie nachstehende mehrere Zeichen Platzhalterzeichen (\*).</span><span class="sxs-lookup"><span data-stu-id="786ac-p104">After you have processed documents in an Advanced eDiscovery case (and optionally run the Analyze or Relevance module), you can use the Search and Tagging to search documents and then organize them by applying case-specific tags (also called labels). You can define a search query using the provided condition cards or by using a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*).</span></span> 

<span data-ttu-id="786ac-p105">Die folgende Tabelle enthält die Eigenschaften, die Sie für die Verwendung einer KQL-Abfrage-Schlüsselwort suchen können. Alternativ können Sie eine Bedingung (für ausgewählte Eigenschaften) auf eine Suchabfrage hinzufügen eine Bedingung-Karte finden Sie in der erweiterten eDiscovery Such-Tool verwenden.</span><span class="sxs-lookup"><span data-stu-id="786ac-p105">The following table lists the properties that you can search for using a KQL keyword query. Alternatively, you can use a condition card for in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query.</span></span>

|<span data-ttu-id="786ac-116">**Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="786ac-116">**Property**</span></span>|<span data-ttu-id="786ac-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="786ac-117">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="786ac-118">**caselabel**</span><span class="sxs-lookup"><span data-stu-id="786ac-118">**caselabel**</span></span> <br/> | <span data-ttu-id="786ac-119">Der Name des Tags erstellt/angewendet, wenn ein Dokument markiert ist.</span><span class="sxs-lookup"><span data-stu-id="786ac-119">The name of the tag created/applied when a document is tagged.</span></span> <br/> |
|<span data-ttu-id="786ac-120">**Verwaltungsberechtigter**</span><span class="sxs-lookup"><span data-stu-id="786ac-120">**custodian**</span></span> <br/> | <span data-ttu-id="786ac-121">Der Verwaltungsberechtigte mit einem Dokument verknüpften; eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="786ac-121">The custodian associated with a document; subject to limitations.</span></span> <br/> |
|<span data-ttu-id="786ac-122">**Datum**</span><span class="sxs-lookup"><span data-stu-id="786ac-122">**date**</span></span> <br/> | <span data-ttu-id="786ac-123">Datum für e-Mail gesendet. das Änderungsdatum für websitedokumente.</span><span class="sxs-lookup"><span data-stu-id="786ac-123">Sent date for email; the modified date for site documents.</span></span> <br/> |
|<span data-ttu-id="786ac-124">**"FileID"**</span><span class="sxs-lookup"><span data-stu-id="786ac-124">**fileid**</span></span> <br/> | <span data-ttu-id="786ac-125">Die Datei-ID in der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="786ac-125">The File ID within the case.</span></span> <br/> |
|<span data-ttu-id="786ac-126">**FileType**</span><span class="sxs-lookup"><span data-stu-id="786ac-126">**filetype**</span></span> <br/> | <span data-ttu-id="786ac-127">Die systemeigene Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="786ac-127">The native file extension.</span></span> <br/> |
|<span data-ttu-id="786ac-128">**fileclass**</span><span class="sxs-lookup"><span data-stu-id="786ac-128">**fileclass**</span></span> <br/> | <span data-ttu-id="786ac-129">E-Mail, Dokument oder Anlage.</span><span class="sxs-lookup"><span data-stu-id="786ac-129">Email, document, or attachment.</span></span> <br/> |
|<span data-ttu-id="786ac-130">**senderauthor**</span><span class="sxs-lookup"><span data-stu-id="786ac-130">**senderauthor**</span></span> <br/> | <span data-ttu-id="786ac-131">Der Absender für e-Mail; der Autor für websitedokumente.</span><span class="sxs-lookup"><span data-stu-id="786ac-131">The sender for email; the author for site documents.</span></span> <br/> |
|<span data-ttu-id="786ac-132">**Größe**</span><span class="sxs-lookup"><span data-stu-id="786ac-132">**size**</span></span> <br/> | <span data-ttu-id="786ac-133">Die Größe der Datei in KB.</span><span class="sxs-lookup"><span data-stu-id="786ac-133">The size of the file in KB.</span></span> <br/> |
|<span data-ttu-id="786ac-134">**Betreff**</span><span class="sxs-lookup"><span data-stu-id="786ac-134">**subjecttitle**</span></span> <br/> | <span data-ttu-id="786ac-135">Der Betreff der e-Mail; der Titel für die websitedokumente.</span><span class="sxs-lookup"><span data-stu-id="786ac-135">The subject for email; the title for site documents.</span></span> <br/> |
|<span data-ttu-id="786ac-136">**bcc**</span><span class="sxs-lookup"><span data-stu-id="786ac-136">**bcc**</span></span> <br/> | <span data-ttu-id="786ac-137">Das Feld Bcc der e-Mail.</span><span class="sxs-lookup"><span data-stu-id="786ac-137">The Bcc field of an email.</span></span> <br/> |
|<span data-ttu-id="786ac-138">**cc**</span><span class="sxs-lookup"><span data-stu-id="786ac-138">**cc**</span></span> <br/> | <span data-ttu-id="786ac-139">Das Feld Cc der e-Mail.</span><span class="sxs-lookup"><span data-stu-id="786ac-139">The Cc field of an email.</span></span> <br/> |
|<span data-ttu-id="786ac-140">**Teilnehmer**</span><span class="sxs-lookup"><span data-stu-id="786ac-140">**participants**</span></span> <br/> | <span data-ttu-id="786ac-141">Die e-Mail-Adresse von allen Teilnehmern in einer e-Mail-Thread, einschließlich für fehlende Links.</span><span class="sxs-lookup"><span data-stu-id="786ac-141">The email address of all participants in an email thread, including for missing links.</span></span> <br/> |
|<span data-ttu-id="786ac-142">**empfangen**</span><span class="sxs-lookup"><span data-stu-id="786ac-142">**received**</span></span> <br/> | <span data-ttu-id="786ac-143">Das Datum, an das eine e-Mail-Nachricht empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="786ac-143">The date an email was received.</span></span> <br/> |
|<span data-ttu-id="786ac-144">**Empfänger**</span><span class="sxs-lookup"><span data-stu-id="786ac-144">**recipients**</span></span> <br/> | <span data-ttu-id="786ac-145">Empfänger einer e-Mail, die auf an, Cc oder Bcc Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="786ac-145">Recipients of an email, included on the To, Cc, or Bcc fields.</span></span> <br/> |
|<span data-ttu-id="786ac-146">**sender**</span><span class="sxs-lookup"><span data-stu-id="786ac-146">**sender**</span></span> <br/> | <span data-ttu-id="786ac-147">Der Absender der e-Mail.</span><span class="sxs-lookup"><span data-stu-id="786ac-147">The sender of an email.</span></span> <br/> |
|<span data-ttu-id="786ac-148">**LastModifiedDate**</span><span class="sxs-lookup"><span data-stu-id="786ac-148">**lastmodifieddate**</span></span> <br/> | <span data-ttu-id="786ac-149">Datum der ein Dokument auf der Website wird von der letzten Änderung.</span><span class="sxs-lookup"><span data-stu-id="786ac-149">The last modified date of a site document.</span></span> <br/> |
|<span data-ttu-id="786ac-150">**gesendet**</span><span class="sxs-lookup"><span data-stu-id="786ac-150">**sent**</span></span> <br/> | <span data-ttu-id="786ac-151">Das Absendedatum der e-Mail.</span><span class="sxs-lookup"><span data-stu-id="786ac-151">The sent date of an email.</span></span> <br/> |
|<span data-ttu-id="786ac-152">**An**</span><span class="sxs-lookup"><span data-stu-id="786ac-152">**to**</span></span> <br/> | <span data-ttu-id="786ac-153">Der Empfänger in das Feld an der eine e-Mail-Nachricht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="786ac-153">The recipient listed in the To field of an email.</span></span> <br/> |
|<span data-ttu-id="786ac-154">**Autor**</span><span class="sxs-lookup"><span data-stu-id="786ac-154">**author**</span></span> <br/> | <span data-ttu-id="786ac-155">Der Autor des ein Dokument auf der Website.</span><span class="sxs-lookup"><span data-stu-id="786ac-155">The author of a site document.</span></span> <br/> |
|<span data-ttu-id="786ac-156">**title**</span><span class="sxs-lookup"><span data-stu-id="786ac-156">**title**</span></span> <br/> | <span data-ttu-id="786ac-157">Der Titel eines Dokuments für die Website.</span><span class="sxs-lookup"><span data-stu-id="786ac-157">The title of a site document.</span></span> <br/> |
|<span data-ttu-id="786ac-158">**dominanttheme**\*</span><span class="sxs-lookup"><span data-stu-id="786ac-158">**dominanttheme**\*</span></span> <br/> | <span data-ttu-id="786ac-159">Das dominante Design eines Elements.</span><span class="sxs-lookup"><span data-stu-id="786ac-159">The dominant theme of an item.</span></span> <br/> |
|<span data-ttu-id="786ac-160">**themeslist**\*</span><span class="sxs-lookup"><span data-stu-id="786ac-160">**themeslist**\*</span></span> <br/> | <span data-ttu-id="786ac-161">Designs, die einem Element zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="786ac-161">Themes that are associated with an item.</span></span> <br/> |
|<span data-ttu-id="786ac-162">**Readpercentile_ [Issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="786ac-162">**readpercentile_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="786ac-163">Das Lesen Quantil eines Elements, für das Problem durch [Issuenum] definiert.</span><span class="sxs-lookup"><span data-stu-id="786ac-163">The read percentile of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="786ac-164">**Relevancescore_ [Issuenum]**\*\*</span><span class="sxs-lookup"><span data-stu-id="786ac-164">**relevancescore_[issuenum]**\*\*</span></span> <br/> | <span data-ttu-id="786ac-165">Die Relevanz Bewertung eines Elements, für das Problem durch [Issuenum] definiert.</span><span class="sxs-lookup"><span data-stu-id="786ac-165">The relevance score of an item, for the issue defined by [issuenum].</span></span> <br/> |
|<span data-ttu-id="786ac-166">**Relevancetag_ [Tagname]**\*\*</span><span class="sxs-lookup"><span data-stu-id="786ac-166">**relevancetag_[tagname]**\*\*</span></span> <br/> | <span data-ttu-id="786ac-167">Wenn ein Element wurde markiert wurde manuell für Relevanz, das Tag durch [Tagname] definiert.</span><span class="sxs-lookup"><span data-stu-id="786ac-167">If an item has been manually tagged for relevance, the tag defined by  [tagname].</span></span> <br/> |
|||

<span data-ttu-id="786ac-168">\*Nur verfügbar, wenn das Modul Designs ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="786ac-168">\* Only available if the Themes module has been run.</span></span>

<span data-ttu-id="786ac-169">\*\*Nur verfügbar, wenn das Modul Relevanz ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="786ac-169">\*\* Only available if the Relevance module has been run.</span></span>

<span data-ttu-id="786ac-p106">Alternativ können Sie eine Karte Bedingung in der erweiterten eDiscovery Such-Tool verwenden, so eine Suchabfrage eine Bedingung (für ausgewählte Eigenschaften) hinzu. Der folgende Screenshot zeigt die Bedingungen, die einer Abfrage hinzugefügt werden können. Die **Gruppe** -Spalte gibt an, ob die Eigenschaft auf e-Mail, Dokumente oder beides (angegeben durch den Wert *Allgemeine*) angewendet wird. Diese Spalte identifiziert auch die durchsuchbaren Eigenschaften, die nach dem Ausführen des Relevanz Moduls verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="786ac-p106">Alternatively, you can use a condition card in the Advanced eDiscovery Search tool to add a condition (for selected properties) to a search query. The following screenshot shows the conditions that can be added to a query. The **Group** column indicates whether the property applies to email, site documents, or both (indicated by the value *Common*). This column also identifies the searchable properties that are available after you run the Relevance module.</span></span>

![Suchkriterien im erweiterten eDiscovery Such-tool](media/AeDSearchConditions.png)

<span data-ttu-id="786ac-175">Weitere Informationen zu durchsuchbare Eigenschaften finden Sie unter [Stichwortabfragen und Suchkriterien](keyword-queries-and-search-conditions.md).</span><span class="sxs-lookup"><span data-stu-id="786ac-175">For more information about searchable properties, see [Keyword queries and search conditions](keyword-queries-and-search-conditions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="786ac-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="786ac-176">See also</span></span>

[<span data-ttu-id="786ac-177">Office 365 Advanced eDiscovery</span><span class="sxs-lookup"><span data-stu-id="786ac-177">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="786ac-178">Grundlegendes zur Bewertung in Relevanz</span><span class="sxs-lookup"><span data-stu-id="786ac-178">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="786ac-179">Kategorien und Bewertung</span><span class="sxs-lookup"><span data-stu-id="786ac-179">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="786ac-180">Kategorien und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="786ac-180">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="786ac-181">Nachverfolgen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="786ac-181">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="786ac-182">Entscheiden je nach den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="786ac-182">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="786ac-183">Testen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="786ac-183">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

