---
title: Suche und Kategorien
ms.author: chrfox
author: chrfox
manager: laurawi
ms.date: 6/13/2018
ms.audience: ITPro
ms.topic: article
ms.service: o365-administration
localization_priority: Normal
search.appverid:
- MET150
ms.assetid: 22f5adad-1bc0-460d-94a9-8732929f5b99
description: In erweiterte eDiscovery ermöglicht das Modul Such- und Kategorien suchen, Vorschau anzeigen und organisieren die Dokumente in Ihrem Fall. In diesem Modul wird derzeit Beta.
ms.openlocfilehash: fde887e496e9a40aa88d841053a0c66e48f04200
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529531"
---
# <a name="search-and-tagging"></a><span data-ttu-id="cf04b-104">Suche und Kategorien</span><span class="sxs-lookup"><span data-stu-id="cf04b-104">Search and Tagging</span></span>

<span data-ttu-id="cf04b-p102">In erweiterte eDiscovery ermöglicht das Modul Such- und Kategorien suchen, Vorschau anzeigen und organisieren die Dokumente in Ihrem Fall. In diesem Modul wird derzeit Beta.</span><span class="sxs-lookup"><span data-stu-id="cf04b-p102">In Advanced eDiscovery, the Search and Tagging module enables you to search, preview, and organize the documents in your case. Currently, this module is in beta.</span></span>

> [!NOTE]
> <span data-ttu-id="cf04b-p103">Erweiterte eDiscovery erfordert eine Office 365 E3 mit das Add-on erweiterte Compliance oder ein Abonnement E5 für Ihre Organisation. Wenn Sie nicht, Planen haben und erweiterte eDiscovery ausprobieren möchten, können Sie die [Melden Sie sich für eine Testversion von Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span><span class="sxs-lookup"><span data-stu-id="cf04b-p103">Advanced eDiscovery requires an Office 365 E3 with the Advanced Compliance add-on or an E5 subscription for your organization. If you don't have that plan and want to try Advanced eDiscovery, you can [sign up for a trial of Office 365 Enterprise E5](https://go.microsoft.com/fwlink/p/?LinkID=698279).</span></span> 
  
## <a name="search-the-documents-in-your-case"></a><span data-ttu-id="cf04b-109">Suchen Sie die Dokumente in Ihrem Fall</span><span class="sxs-lookup"><span data-stu-id="cf04b-109">Search the documents in your case</span></span>

<span data-ttu-id="cf04b-p104">Nachdem Sie Dokumente in erweiterten eDiscovery verarbeitet und optional das Modul Analyse oder der Relevanz-Modul ausgeführt werden, Sie suchen können und Verwenden von Kategorien, die Dokumente im Fall durchsuchen und Organisieren Case-spezifische Tags. Sie können Definieren von Abfragen mit dem angegebenen Bedingung Karten oder über eine KQL-ähnliche Abfragesprache in den Schlüsselwörtern Bedingung Karte. Allgemeine KQL-Syntax wie AND, OR, NOT und NEAR(n) sind die unterstützten sowie nachstehende mehrere Zeichen Platzhalterzeichen (\*). Diese Eigenschaften werden in der Abfrage-Eigenschaftenname unterstützt:</span><span class="sxs-lookup"><span data-stu-id="cf04b-p104">Once you have processed documents in Advanced eDiscovery and optionally run the Analyze module or the Relevance module, you can use Search and Tagging to search through the documents in the case and organize them using case-specific tags. You can define your queries using the provided condition cards, or through a KQL-like query language in the Keywords condition card. Common KQL syntax, such as AND, OR, NOT, and NEAR(n) are supported, as well as trailing multi-character wildcard (\*). These properties are supported in the query language property name:</span></span>

- <span data-ttu-id="cf04b-114">Caselabel: Tags erstellt/angewendet in der Suche und Kategorien für diesen Fall</span><span class="sxs-lookup"><span data-stu-id="cf04b-114">caselabel: tags created/applied in Search and Tagging for this case</span></span> 
- <span data-ttu-id="cf04b-115">Verwalter: im Fall - eingeschränkt zugewiesen Verwalter</span><span class="sxs-lookup"><span data-stu-id="cf04b-115">custodians: custodians assigned in the case - subject to limitations</span></span>
- <span data-ttu-id="cf04b-116">Datum: Datum für e-Mail gesendet, Änderungsdatum für Dokumente</span><span class="sxs-lookup"><span data-stu-id="cf04b-116">date: sent date for email, modified date for documents</span></span>
- <span data-ttu-id="cf04b-117">FileID: Datei mit der ID innerhalb der Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="cf04b-117">fileid: file ID within the case</span></span>
- <span data-ttu-id="cf04b-118">FileType: systemeigene Erweiterung</span><span class="sxs-lookup"><span data-stu-id="cf04b-118">filetype: native file extension</span></span>
- <span data-ttu-id="cf04b-119">Fileclass: e-Mail, Dokument oder Anlage</span><span class="sxs-lookup"><span data-stu-id="cf04b-119">fileclass: email, document, or attachment</span></span>
- <span data-ttu-id="cf04b-120">Senderauthor: Absender-e-Mails, Autor für Dokumente</span><span class="sxs-lookup"><span data-stu-id="cf04b-120">senderauthor: sender for emails, author for documents</span></span>
- <span data-ttu-id="cf04b-121">Größe: Größe der Datei in KB</span><span class="sxs-lookup"><span data-stu-id="cf04b-121">size: size of the file in KB</span></span>
- <span data-ttu-id="cf04b-122">Betreff: Betreff für e-Mails, Titel für Dokumente</span><span class="sxs-lookup"><span data-stu-id="cf04b-122">subjecttitle: subject for emails, title for documents</span></span>
- <span data-ttu-id="cf04b-123">bcc</span><span class="sxs-lookup"><span data-stu-id="cf04b-123">bcc</span></span>
- <span data-ttu-id="cf04b-124">cc</span><span class="sxs-lookup"><span data-stu-id="cf04b-124">cc</span></span>
- <span data-ttu-id="cf04b-125">Teilnehmer: e-Mail-Adressen von allen Teilnehmern in einer e-Mail-Thread, einschließlich für fehlende Links</span><span class="sxs-lookup"><span data-stu-id="cf04b-125">participants: Email addresses of all participants in an email thread, including for missing links</span></span>
- <span data-ttu-id="cf04b-126">empfangen: Empfangsdatum</span><span class="sxs-lookup"><span data-stu-id="cf04b-126">received: received date</span></span>
- <span data-ttu-id="cf04b-127">Empfänger: e-Mail-Namen der Empfänger oder Adressen (an, cc, Bcc)</span><span class="sxs-lookup"><span data-stu-id="cf04b-127">recipients: email recipient names or addresses (to, cc, bcc)</span></span>
- <span data-ttu-id="cf04b-128">sender</span><span class="sxs-lookup"><span data-stu-id="cf04b-128">sender</span></span>
- <span data-ttu-id="cf04b-129">LastModifiedDate: letzte Änderung eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="cf04b-129">lastmodifieddate: last modified date of a document</span></span>
- <span data-ttu-id="cf04b-130">gesendet: Datum der eine e-Mail gesendet</span><span class="sxs-lookup"><span data-stu-id="cf04b-130">sent: sent date of an email</span></span>
- <span data-ttu-id="cf04b-131">bis</span><span class="sxs-lookup"><span data-stu-id="cf04b-131">to</span></span>
- <span data-ttu-id="cf04b-132">Autor: Autor einer e-Mail</span><span class="sxs-lookup"><span data-stu-id="cf04b-132">author: author of an email</span></span>
- <span data-ttu-id="cf04b-133">Title: Titel eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="cf04b-133">title: title of a document</span></span>
- <span data-ttu-id="cf04b-134">Dominanttheme: dominanten Design eines Elements\*</span><span class="sxs-lookup"><span data-stu-id="cf04b-134">dominanttheme: dominant theme of an item\*</span></span>
- <span data-ttu-id="cf04b-135">Themeslist: Designs, die einem Element zugeordnet sind.\*</span><span class="sxs-lookup"><span data-stu-id="cf04b-135">themeslist: themes that are associated with an item\*</span></span>
- <span data-ttu-id="cf04b-136">Readpercentile_ [Issuenum]: Lesen Quantil eines Elements für Problem [Issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="cf04b-136">readpercentile_[issuenum]: read percentile of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="cf04b-137">Relevancescore_ [Issuenum]: Relevanz Bewertung eines Elements für Problem [Issuenum]\*\*</span><span class="sxs-lookup"><span data-stu-id="cf04b-137">relevancescore_[issuenum]: relevance score of an item for issue [issuenum]\*\*</span></span>
- <span data-ttu-id="cf04b-138">Relevancetag_ [Issuenum]: Wenn ein Element manuell für Relevanz, dessen Tag für [Issuenum] markiert wurde.\*\*</span><span class="sxs-lookup"><span data-stu-id="cf04b-138">relevancetag_[issuenum]: if an item has been manually tagged for relevance, its tag for [issuenum]\*\*</span></span>

<span data-ttu-id="cf04b-139">\*Nur verfügbar, wenn das Modul Designs ausgeführt wurde \* \* nur verfügbar, wenn das Modul Relevanz ausgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="cf04b-139">\* Only available if the Themes module has been run \*\* Only available if the Relevance module has been run</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf04b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf04b-140">See also</span></span>

[<span data-ttu-id="cf04b-141">Office 365 Erweiterte eDiscovery</span><span class="sxs-lookup"><span data-stu-id="cf04b-141">Office 365 Advanced eDiscovery</span></span>](office-365-advanced-ediscovery.md)
  
[<span data-ttu-id="cf04b-142">Grundlegendes zur Bewertung in Relevanz</span><span class="sxs-lookup"><span data-stu-id="cf04b-142">Understanding Assessment in Relevance</span></span>](assessment-in-relevance-in-advanced-ediscovery.md)
  
[<span data-ttu-id="cf04b-143">Kategorien und Bewertung</span><span class="sxs-lookup"><span data-stu-id="cf04b-143">Tagging and Assessment</span></span>](tagging-and-assessment-in-advanced-ediscovery.md)
  
[<span data-ttu-id="cf04b-144">Kategorien und Relevanz-Schulung</span><span class="sxs-lookup"><span data-stu-id="cf04b-144">Tagging and Relevance training</span></span>](tagging-and-relevance-training-in-advanced-ediscovery.md)
  
[<span data-ttu-id="cf04b-145">Nachverfolgen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="cf04b-145">Tracking Relevance analysis</span></span>](track-relevance-analysis-in-advanced-ediscovery.md)
  
[<span data-ttu-id="cf04b-146">Entscheiden je nach den Ergebnissen</span><span class="sxs-lookup"><span data-stu-id="cf04b-146">Deciding based on the results</span></span>](decision-based-on-the-results-in-advanced-ediscovery.md)
  
[<span data-ttu-id="cf04b-147">Testen der Relevanz Analyse</span><span class="sxs-lookup"><span data-stu-id="cf04b-147">Testing Relevance analysis</span></span>](test-relevance-analysis-in-advanced-ediscovery.md)

