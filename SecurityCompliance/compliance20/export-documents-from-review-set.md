---
title: Exportieren von Dokumenten aus einem Prüfdateisatz
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 14efa58305e1963aa43c0c94fb208e5391c87119
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34155067"
---
# <a name="export-documents-from-a-review-set"></a><span data-ttu-id="8200f-102">Exportieren von Dokumenten aus einem Prüfdateisatz</span><span class="sxs-lookup"><span data-stu-id="8200f-102">Export documents from a review set</span></span>

<span data-ttu-id="8200f-103">Das Exportieren von Inhalten aus einem Überprüfungs Satzes kann über drei verschiedene Methoden erfolgen:</span><span class="sxs-lookup"><span data-stu-id="8200f-103">Exporting content from a review set can be accomplished via 3 different methods:</span></span>

## <a name="download"></a><span data-ttu-id="8200f-104">Download</span><span class="sxs-lookup"><span data-stu-id="8200f-104">Download</span></span>

<span data-ttu-id="8200f-105">Download bietet eine einfache Möglichkeit zum Herunterladen von Inhalten aus einer Überprüfungsgruppe im systemeigenen Format.</span><span class="sxs-lookup"><span data-stu-id="8200f-105">Download offers a simple way to download content from a review set in Native format.</span></span> <span data-ttu-id="8200f-106">Es nutzt die Datentransfer Funktionen des Browsers, sodass nach dem Download eine Browser Ansage angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8200f-106">It leverages the browser’s data transfer features so a browser prompt will appear once a download is ready.</span></span> <span data-ttu-id="8200f-107">Mit dieser Methode heruntergeladene Dateien werden in eine Containerdatei gezippt und werden Dateien auf Elementebene sein.</span><span class="sxs-lookup"><span data-stu-id="8200f-107">Files downloaded using this method will be zipped into a container file and will be item level files.</span></span> <span data-ttu-id="8200f-108">Wenn Sie also eine Anlage auswählen, erhalten Sie automatisch die e-Mail-Adresse, die mit der Anlage eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8200f-108">This means that if you select an attachment, you will automatically receive the email with the attachment included.</span></span> <span data-ttu-id="8200f-109">Wenn Sie eine Excel-Kalkulationstabelle auswählen, die in ein Word-Dokument eingebettet wurde, erhalten Sie das Word-Dokument mit eingebettetem Excel-Arbeitsblatt.</span><span class="sxs-lookup"><span data-stu-id="8200f-109">Similarly, if you select an excel spreadsheet that was embedded in a word document, you will receive the word document with the excel spreadsheet embedded.</span></span> <span data-ttu-id="8200f-110">Durch heruntergeladene Elemente wird das Datum der letzten Änderung beibehalten, das als Dateieigenschaft angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="8200f-110">Downloaded items will preserve the last modified date which can be viewed as a file property.</span></span>

<span data-ttu-id="8200f-111">Um Inhalte aus einem Überprüfungs herunterzuladen, wählen Sie zunächst die Dateien aus, die Sie herunterladen möchten, und klicken Sie dann im Menü Aktionen auf "herunterladen".</span><span class="sxs-lookup"><span data-stu-id="8200f-111">To download content from a review set, start by selecting the files you want to download then select “Download” under the Actions menu.</span></span>

![Screenshot einer automatisch generierten Computerbeschreibung](../media/eDiscoDownload.png)

## <a name="export"></a><span data-ttu-id="8200f-113">Exportieren</span><span class="sxs-lookup"><span data-stu-id="8200f-113">Export</span></span>

<span data-ttu-id="8200f-114">Mit dem Export können Benutzer die Inhalte anpassen, die im Downloadpaket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8200f-114">Export allows users to customize the content that is included in the download package.</span></span> <span data-ttu-id="8200f-115">Es stellt eine Konfigurationsseite mit den folgenden Einstellungen bereit:</span><span class="sxs-lookup"><span data-stu-id="8200f-115">It provides a configuration page with the following settings:</span></span>

### <a name="metadata-file"></a><span data-ttu-id="8200f-116">Metadaten-Datei</span><span class="sxs-lookup"><span data-stu-id="8200f-116">Metadata file</span></span>

> <span data-ttu-id="8200f-117">Dies kann als ihre "Laden Datei" betrachtet werden, die Metadaten enthält, die den exportierten Dateien zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="8200f-117">This can be considered your “load file” that contains metadata associated with the files you exported.</span></span> <span data-ttu-id="8200f-118">Eine Liste der in der Metadatendatei verfügbaren Felder \[finden\]Sie unter Link.</span><span class="sxs-lookup"><span data-stu-id="8200f-118">For a list of fields available in the metadata file, see \[link\].</span></span> <span data-ttu-id="8200f-119">Diese Datei kann normalerweise von drei<sup>Remote</sup> Tools von Drittanbietern aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="8200f-119">This file can typically be ingested by 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="tag-data"></a><span data-ttu-id="8200f-120">Tag-Daten</span><span class="sxs-lookup"><span data-stu-id="8200f-120">Tag data</span></span>

> <span data-ttu-id="8200f-121">Dieser Inhalt würde als Felder in der Metadatendatei hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8200f-121">This content would be added as fields in the metadata file.</span></span> <span data-ttu-id="8200f-122">Sie enthält alle in Überprüfungs Sätzen angewendeten Tag-Informationen.</span><span class="sxs-lookup"><span data-stu-id="8200f-122">It contains all of the tag information applied in review sets.</span></span>

### <a name="text-files"></a><span data-ttu-id="8200f-123">Textdateien</span><span class="sxs-lookup"><span data-stu-id="8200f-123">Text files</span></span>

> <span data-ttu-id="8200f-124">Text Dateien können für jede Datei generiert werden, die aus einem Überprüfungs Satz exportiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8200f-124">Text files can be generated for each file exported from a review set.</span></span> <span data-ttu-id="8200f-125">Häufig sind diese Dateien für Service Partner erforderlich, wenn Sie Daten in Drittanbieter-Tools<sup></sup> nach Downstream aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="8200f-125">Often times these files are required by service partners as part of ingesting data into 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="redacted-files"></a><span data-ttu-id="8200f-126">Behandelte Dateien</span><span class="sxs-lookup"><span data-stu-id="8200f-126">Redacted files</span></span>

> <span data-ttu-id="8200f-127">Wenn während der Überprüfung redigierte PDFs generiert werden, stehen diese Dateien während des Exports zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="8200f-127">If redacted PDFs are generated during review, these files are available during export.</span></span> <span data-ttu-id="8200f-128">Benutzer können entscheiden, ob Sie systemeigene Dateien exportieren oder natives ersetzen möchten, bei denen die in PDFs gebrannt wurden.</span><span class="sxs-lookup"><span data-stu-id="8200f-128">Users can decide whether to export native files only or to replace natives that have redactions with the burned in PDFs.</span></span>

### <a name="export-location"></a><span data-ttu-id="8200f-129">Exportspeicherort</span><span class="sxs-lookup"><span data-stu-id="8200f-129">Export Location</span></span>

> <span data-ttu-id="8200f-130">Exportierte Inhalte werden entweder an ein von Microsoft bereitgestelltes Azure-BLOB zugestellt, oder das BLOB eines Kunden kann verwendet werden, wenn die Details beim Export angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8200f-130">Exported content is delivered to either a Microsoft provided Azure blob or a customer’s blob can be used if the details are provided at export.</span></span>

## <a name="export-structure"></a><span data-ttu-id="8200f-131">Export Struktur</span><span class="sxs-lookup"><span data-stu-id="8200f-131">Export Structure</span></span>

<span data-ttu-id="8200f-132">Wenn Inhalte aus einem Überprüfungs Satzes exportiert werden, ist der Inhalt in der folgenden Struktur organisiert.</span><span class="sxs-lookup"><span data-stu-id="8200f-132">When content is exported from a review set, the content is organized in the following structure.</span></span>

  - <span data-ttu-id="8200f-133">Stammordner – Download-ID</span><span class="sxs-lookup"><span data-stu-id="8200f-133">Root folder – Download ID</span></span>
    
      - <span data-ttu-id="8200f-134">Exportieren\_der\_Datei "file. CSV = Metadata"</span><span class="sxs-lookup"><span data-stu-id="8200f-134">Export\_load\_file.csv = metadata file</span></span>
    
      - <span data-ttu-id="8200f-135">Summary. txt = eine Zusammenfassungsdatei mit Export Statistiken</span><span class="sxs-lookup"><span data-stu-id="8200f-135">Summary.txt = a summary file with export statistics</span></span>
    
      - <span data-ttu-id="8200f-136">Input\_oder Native\_files = enthält alle systemeigenen Dateien</span><span class="sxs-lookup"><span data-stu-id="8200f-136">Input\_or native\_files = contains all native files</span></span>
    
      - <span data-ttu-id="8200f-137">Error\_files = enthält alle Fehler Dateien, die im Export enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="8200f-137">Error\_files = contains any error files included in the export</span></span>
        
          - <span data-ttu-id="8200f-138">ExtractionError – eine CSV-Datei, die alle verfügbaren Metadaten von Dateien enthält, die nicht ordnungsgemäß aus übergeordneten Dateien extrahiert wurden</span><span class="sxs-lookup"><span data-stu-id="8200f-138">ExtractionError – a csv that contains any available metadata of files that were not properly extracted from parent files</span></span>
        
          - <span data-ttu-id="8200f-139">ProcessingError – Inhalte mit Verarbeitungsfehlern.</span><span class="sxs-lookup"><span data-stu-id="8200f-139">ProcessingError – content with processing errors.</span></span> <span data-ttu-id="8200f-140">Dieser Inhalt ist eine Elementebene, was bedeutet, dass bei einer Anlage ein Verarbeitungsfehler auftritt, wird die e-Mail-Nachricht, die die Anlage enthält, in diesen Ordner aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="8200f-140">This content is item level meaning if an attachment experienced a processing error, the email that contains the attachment will be included in this folder.</span></span>
    
      - <span data-ttu-id="8200f-141">Extrahierte\_Text\_Dateien = enthält alle extrahierten Textdateien, die bei der Verarbeitung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8200f-141">Extracted\_text\_files = contains all of the extracted text files generated at processing.</span></span>

## <a name="review-set"></a><span data-ttu-id="8200f-142">Überprüfungsgruppe</span><span class="sxs-lookup"><span data-stu-id="8200f-142">review set</span></span>

<span data-ttu-id="8200f-143">Inhalte können zu anderen Überprüfungs Sätzen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8200f-143">Content can be added to another review set.</span></span>