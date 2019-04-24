---
title: Exportieren von Dokumenten aus einem Arbeitssatz
ms.author: markjjo
author: markjjo
manager: laurawi
ms.date: ''
ms.audience: Admin
ms.topic: article
ms.service: O365-seccomp
localization_priority: Normal
ms.collection: M365-security-compliance
search.appverid:
- MOE150
- MET150
ms.assetid: ''
description: ''
ms.openlocfilehash: 815b92b13ed09d8aec64f5207f1c82d910e2dce0
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32252048"
---
# <a name="export-documents-from-a-working-set"></a><span data-ttu-id="6ed13-102">Exportieren von Dokumenten aus einem Arbeitssatz</span><span class="sxs-lookup"><span data-stu-id="6ed13-102">Export documents from a working set</span></span>

<span data-ttu-id="6ed13-103">Das Exportieren von Inhalten aus einem Arbeitssatz kann über drei verschiedene Methoden erfolgen:</span><span class="sxs-lookup"><span data-stu-id="6ed13-103">Exporting content from a working set can be accomplished via 3 different methods:</span></span>

## <a name="download"></a><span data-ttu-id="6ed13-104">Download</span><span class="sxs-lookup"><span data-stu-id="6ed13-104">Download</span></span>

<span data-ttu-id="6ed13-105">Download bietet eine einfache Möglichkeit zum Herunterladen von Inhalten aus einem Workingset im systemeigenen Format.</span><span class="sxs-lookup"><span data-stu-id="6ed13-105">Download offers a simple way to download content from a working set in Native format.</span></span> <span data-ttu-id="6ed13-106">Es nutzt die Datentransfer Funktionen des Browsers, sodass eine Browser Ansage angezeigt wird, sobald ein Download bereit ist.</span><span class="sxs-lookup"><span data-stu-id="6ed13-106">It leverages the browser’s data transfer features so a browser prompt will appear once a download is ready.</span></span> <span data-ttu-id="6ed13-107">Dateien, die mit dieser Methode heruntergeladen werden, werden in eine Containerdatei gepackt und sind Dateien auf Elementebene.</span><span class="sxs-lookup"><span data-stu-id="6ed13-107">Files downloaded using this method will be zipped into a container file and will be item level files.</span></span> <span data-ttu-id="6ed13-108">Wenn Sie eine Anlage auswählen, erhalten Sie daher automatisch eine e-Mail mit der enthaltenen Anlage.</span><span class="sxs-lookup"><span data-stu-id="6ed13-108">This means that if you select an attachment, you will automatically receive the email with the attachment included.</span></span> <span data-ttu-id="6ed13-109">Wenn Sie eine Excel-Kalkulationstabelle auswählen, die in ein Word-Dokument eingebettet wurde, erhalten Sie auch das Word-Dokument mit der eingebetteten Excel-Kalkulationstabelle.</span><span class="sxs-lookup"><span data-stu-id="6ed13-109">Similarly, if you select an excel spreadsheet that was embedded in a word document, you will receive the word document with the excel spreadsheet embedded.</span></span> <span data-ttu-id="6ed13-110">HeruntergeLadene Elemente behalten das Datum der letzten Änderung bei, das als Dateieigenschaft angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="6ed13-110">Downloaded items will preserve the last modified date which can be viewed as a file property.</span></span>

<span data-ttu-id="6ed13-111">Um Inhalte aus einem Arbeitssatz herunterzuladen, wählen Sie zunächst die Dateien aus, die Sie herunterladen möchten, und klicken Sie dann im Menü Aktionen auf "herunterladen".</span><span class="sxs-lookup"><span data-stu-id="6ed13-111">To download content from a working set, start by selecting the files you want to download then select “Download” under the Actions menu.</span></span>

![Screenshot einer Computerbeschreibung, die automatisch generiert wird](../media/eDiscoDownload.png)

## <a name="export"></a><span data-ttu-id="6ed13-113">Exportieren</span><span class="sxs-lookup"><span data-stu-id="6ed13-113">Export</span></span>

<span data-ttu-id="6ed13-114">Der Export ermöglicht Benutzern das Anpassen der Inhalte, die im Downloadpaket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6ed13-114">Export allows users to customize the content that is included in the download package.</span></span> <span data-ttu-id="6ed13-115">Es bietet eine Konfigurationsseite mit den folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="6ed13-115">It provides a configuration page with the following settings:</span></span>

### <a name="metadata-file"></a><span data-ttu-id="6ed13-116">MetaDatendatei</span><span class="sxs-lookup"><span data-stu-id="6ed13-116">Metadata file</span></span>

> <span data-ttu-id="6ed13-117">Dies kann als ihre "Datei laden" angesehen werden, die Metadaten enthält, die mit den exportierten Dateien verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="6ed13-117">This can be considered your “load file” that contains metadata associated with the files you exported.</span></span> <span data-ttu-id="6ed13-118">Eine Liste der Felder, die in der Metadatendatei zur \[Verfügung stehen, finden Sie unter Link\].</span><span class="sxs-lookup"><span data-stu-id="6ed13-118">For a list of fields available in the metadata file, see \[link\].</span></span> <span data-ttu-id="6ed13-119">Diese Datei kann i. d. r. von 3<sup>RD</sup> -Anbieter Tools nachgeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed13-119">This file can typically be ingested by 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="tag-data"></a><span data-ttu-id="6ed13-120">Tag-Daten</span><span class="sxs-lookup"><span data-stu-id="6ed13-120">Tag data</span></span>

> <span data-ttu-id="6ed13-121">Dieser Inhalt würde als Felder in der Metadatendatei hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed13-121">This content would be added as fields in the metadata file.</span></span> <span data-ttu-id="6ed13-122">Sie enthält alle Tag-Informationen, die in Arbeitsmappen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="6ed13-122">It contains all of the tag information applied in working sets.</span></span>

### <a name="text-files"></a><span data-ttu-id="6ed13-123">Textdateien</span><span class="sxs-lookup"><span data-stu-id="6ed13-123">Text files</span></span>

> <span data-ttu-id="6ed13-124">Text Dateien können für jede aus einem Arbeitssatz exportierte Datei generiert werden.</span><span class="sxs-lookup"><span data-stu-id="6ed13-124">Text files can be generated for each file exported from a working set.</span></span> <span data-ttu-id="6ed13-125">Häufig werden diese Dateien von den Dienst Partnern im Rahmen der Einnahme von Daten in 3 Dritt<sup></sup> Anbieter Tools (Downstream) benötigt.</span><span class="sxs-lookup"><span data-stu-id="6ed13-125">Often times these files are required by service partners as part of ingesting data into 3<sup>rd</sup> party tools downstream.</span></span>

### <a name="redacted-files"></a><span data-ttu-id="6ed13-126">Gehandelte Dateien</span><span class="sxs-lookup"><span data-stu-id="6ed13-126">Redacted files</span></span>

> <span data-ttu-id="6ed13-127">Wenn während der Überprüfungen redigierte PDFs generiert werden, sind diese Dateien während des Exports verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6ed13-127">If redacted PDFs are generated during review, these files are available during export.</span></span> <span data-ttu-id="6ed13-128">Benutzer können entscheiden, ob Sie nur systemeigene Dateien exportieren oder natives ersetzen möchten, die mit den gebrannten PDFs in der PDF-Datei ausgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="6ed13-128">Users can decide whether to export native files only or to replace natives that have redactions with the burned in PDFs.</span></span>

### <a name="export-location"></a><span data-ttu-id="6ed13-129">Exportspeicherort</span><span class="sxs-lookup"><span data-stu-id="6ed13-129">Export Location</span></span>

> <span data-ttu-id="6ed13-130">Exportierte Inhalte werden entweder an ein von Microsoft bereitgestelltes Azure-BLOB oder an ein Kunden-BLOB übermittelt, wenn die Details beim Export bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed13-130">Exported content is delivered to either a Microsoft provided Azure blob or a customer’s blob can be used if the details are provided at export.</span></span>

## <a name="export-structure"></a><span data-ttu-id="6ed13-131">Export Struktur</span><span class="sxs-lookup"><span data-stu-id="6ed13-131">Export Structure</span></span>

<span data-ttu-id="6ed13-132">Beim Exportieren von Inhalten aus einem Arbeitssatz wird der Inhalt in der folgenden Struktur organisiert.</span><span class="sxs-lookup"><span data-stu-id="6ed13-132">When content is exported from a working set, the content is organized in the following structure.</span></span>

  - <span data-ttu-id="6ed13-133">Stammordner – Download-ID</span><span class="sxs-lookup"><span data-stu-id="6ed13-133">Root folder – Download ID</span></span>
    
      - <span data-ttu-id="6ed13-134">Export\_laden\_Datei. CSV = Metadatendatei</span><span class="sxs-lookup"><span data-stu-id="6ed13-134">Export\_load\_file.csv = metadata file</span></span>
    
      - <span data-ttu-id="6ed13-135">Summary. txt = eine Zusammenfassungsdatei mit Export Statistiken</span><span class="sxs-lookup"><span data-stu-id="6ed13-135">Summary.txt = a summary file with export statistics</span></span>
    
      - <span data-ttu-id="6ed13-136">Eingabe\_-oder\_systemeigene Dateien = enthält alle systemeigenen Dateien</span><span class="sxs-lookup"><span data-stu-id="6ed13-136">Input\_or native\_files = contains all native files</span></span>
    
      - <span data-ttu-id="6ed13-137">Error\_files = enthält alle Fehler Dateien, die im Export enthalten sind</span><span class="sxs-lookup"><span data-stu-id="6ed13-137">Error\_files = contains any error files included in the export</span></span>
        
          - <span data-ttu-id="6ed13-138">ExtractionError – eine CSV-Datei, die alle verfügbaren Metadaten von Dateien enthält, die nicht ordnungsgemäß aus übergeordneten Dateien extrahiert wurden</span><span class="sxs-lookup"><span data-stu-id="6ed13-138">ExtractionError – a csv that contains any available metadata of files that were not properly extracted from parent files</span></span>
        
          - <span data-ttu-id="6ed13-139">ProcessingError – Inhalte mit Verarbeitungsfehlern.</span><span class="sxs-lookup"><span data-stu-id="6ed13-139">ProcessingError – content with processing errors.</span></span> <span data-ttu-id="6ed13-140">Dieser Inhalt ist auf Elementebene Bedeutung wenn bei einer Anlage ein Verarbeitungsfehler auftritt, wird die e-Mail mit der Anlage in diesen Ordner aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="6ed13-140">This content is item level meaning if an attachment experienced a processing error, the email that contains the attachment will be included in this folder.</span></span>
    
      - <span data-ttu-id="6ed13-141">Extrahierte\_Text\_Dateien = enthält alle extrahierten Textdateien, die bei der Verarbeitung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="6ed13-141">Extracted\_text\_files = contains all of the extracted text files generated at processing.</span></span>

## <a name="working-set"></a><span data-ttu-id="6ed13-142">Arbeitsseiten</span><span class="sxs-lookup"><span data-stu-id="6ed13-142">Working Set</span></span>

<span data-ttu-id="6ed13-143">Inhalte können einer anderen Arbeitsmappe hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="6ed13-143">Content can be added to another working set.</span></span>