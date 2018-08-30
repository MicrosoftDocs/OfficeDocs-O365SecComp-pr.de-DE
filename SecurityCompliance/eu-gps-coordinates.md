---
title: EU-GPS-Koordinaten
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/14/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: fdf2aebc-d5a4-4138-b10f-4a81dd70415a
description: Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center enthält viele Arten von vertraulichen Informationen, die Sie in Ihrer DLP-Richtlinien verwendet werden. In diesem Thema wird den Typ der EU GPS-Koordinaten vertraulichen Informationen.
ms.openlocfilehash: 89fb8420e479b9f793fc2be9aa3a9a9fd5741691
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529369"
---
# <a name="eu-gps-coordinates"></a><span data-ttu-id="e6b53-104">EU-GPS-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="e6b53-104">EU GPS Coordinates</span></span>

<span data-ttu-id="e6b53-p102">Verhinderung von Datenverlust (DLP) in die Office 365-Sicherheit &amp; Compliance Center enthält viele Arten von vertraulichen Informationen, die Sie in Ihrer DLP-Richtlinien verwendet werden. In diesem Thema wird den Typ der EU GPS-Koordinaten vertraulichen Informationen.</span><span class="sxs-lookup"><span data-stu-id="e6b53-p102">Data loss prevention (DLP) in the Office 365 Security &amp; Compliance Center includes many sensitive information types that are ready for you to use in your DLP policies. This topic describes the EU GPS Coordinates sensitive information type.</span></span>
  
## <a name="austria"></a><span data-ttu-id="e6b53-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="e6b53-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="e6b53-108">Format</span><span class="sxs-lookup"><span data-stu-id="e6b53-108">Format</span></span>

<span data-ttu-id="e6b53-109">Koordinaten für Städte in Österreich im Bereich sind: Breitengrad aus 46.526 48.816 und Längengrad von 9,6 zu 16.945.</span><span class="sxs-lookup"><span data-stu-id="e6b53-109">Coordinates for cities in Austria are in range: Latitude from 46.526 to 48.816 and longitude from 9.6 to 16.945.</span></span>
  
### <a name="pattern"></a><span data-ttu-id="e6b53-110">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-110">Pattern</span></span>

<span data-ttu-id="e6b53-111">Für jede Koordinate, die Kombination von bis zu 6 Ziffern und ein Dezimaltrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="e6b53-111">For each coordinate, combination of up to 6 digits and a decimal point.</span></span>
  
- <span data-ttu-id="e6b53-112">Bis zu 6 Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-112">Up to 6 digits</span></span>
    
- <span data-ttu-id="e6b53-113">Ein Dezimalkomma nach erste oder zweite Stelle.</span><span class="sxs-lookup"><span data-stu-id="e6b53-113">A decimal point after first or second digit.</span></span>
    
### <a name="checksum"></a><span data-ttu-id="e6b53-114">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-114">Checksum</span></span>

<span data-ttu-id="e6b53-115">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-115">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-116">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-116">Definition</span></span>

<span data-ttu-id="e6b53-117">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-117">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-118">Der reguläre Ausdruck `Regex_austria_eu_gps_data_1` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-118">The regular expression  `Regex_austria_eu_gps_data_1` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e6b53-119">Ein Schlüsselwort aus `Keywords_austria_eu_gps_data` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-119">A keyword from  `Keywords_austria_eu_gps_data` is found.</span></span> 
    
<span data-ttu-id="e6b53-120">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-120">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-121">Der reguläre Ausdruck `Regex_austria_eu_gps_data_1` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-121">The regular expression  `Regex_austria_eu_gps_data_1` finds content that matches the pattern.</span></span> 
    
<span data-ttu-id="e6b53-122">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-122">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-123">Der reguläre Ausdruck `Regex_austria_eu_gps_data_2` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-123">The regular expression  `Regex_austria_eu_gps_data_2` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="e6b53-124">Ein Schlüsselwort aus `Keywords_austria_eu_gps_data` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-124">A keyword from  `Keywords_austria_eu_gps_data` is found.</span></span> 
    
<span data-ttu-id="e6b53-125">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-125">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-126">Der reguläre Ausdruck `Regex_austria_eu_gps_data_2` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-126">The regular expression  `Regex_austria_eu_gps_data_2` finds content that matches the pattern.</span></span> 
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_gps_data_1" />
          <Match idRef="Keywords_austria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_austria_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_gps_data_2" />
          <Match idRef="Keywords_austria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_austria_eu_gps_data_2" />
        </Pattern>

```

### <a name="keywords"></a><span data-ttu-id="e6b53-127">Keywords</span><span class="sxs-lookup"><span data-stu-id="e6b53-127">Keywords</span></span>

#### <a name="keywordsaustriaeugpsdata"></a><span data-ttu-id="e6b53-128">Keywords_austria_eu_gps_data</span><span class="sxs-lookup"><span data-stu-id="e6b53-128">Keywords_austria_eu_gps_data</span></span>

<span data-ttu-id="e6b53-129">GPS-tracker</span><span class="sxs-lookup"><span data-stu-id="e6b53-129">gps tracker</span></span>
  
<span data-ttu-id="e6b53-130">GPS-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="e6b53-130">gps coordinates</span></span>
  
<span data-ttu-id="e6b53-131">Speicherort</span><span class="sxs-lookup"><span data-stu-id="e6b53-131">location</span></span>
  
<span data-ttu-id="e6b53-132">Schema</span><span class="sxs-lookup"><span data-stu-id="e6b53-132">map</span></span>
  
<span data-ttu-id="e6b53-133">Breitengrad</span><span class="sxs-lookup"><span data-stu-id="e6b53-133">latitude</span></span>
  
<span data-ttu-id="e6b53-134">Längengrad</span><span class="sxs-lookup"><span data-stu-id="e6b53-134">longitude</span></span>
  
<span data-ttu-id="e6b53-135">GPS-Tracker</span><span class="sxs-lookup"><span data-stu-id="e6b53-135">GPS-Tracker</span></span>
  
<span data-ttu-id="e6b53-136">GPS-Koordinaten</span><span class="sxs-lookup"><span data-stu-id="e6b53-136">GPS-Koordinaten</span></span>
  
<span data-ttu-id="e6b53-137">Standort-Karte</span><span class="sxs-lookup"><span data-stu-id="e6b53-137">Standort Karte</span></span>
  
<span data-ttu-id="e6b53-138">Breitengrad</span><span class="sxs-lookup"><span data-stu-id="e6b53-138">Breitengrad</span></span>
  
<span data-ttu-id="e6b53-139">Längengrad</span><span class="sxs-lookup"><span data-stu-id="e6b53-139">Längengrad</span></span>
  
## <a name="belgium"></a><span data-ttu-id="e6b53-140">Belgien</span><span class="sxs-lookup"><span data-stu-id="e6b53-140">Belgium</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-141">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-141">Pattern</span></span>

-  <span data-ttu-id="e6b53-142">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-142">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-143">Checksum</span></span>

<span data-ttu-id="e6b53-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-145">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-145">Definition</span></span>

<span data-ttu-id="e6b53-146">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-147">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-147">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-148">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-148">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75>">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_gps_data_1" />
          <Match idRef="Keywords_belgium_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
          <Match idRef="Keywords_belgium_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="bulgaria"></a><span data-ttu-id="e6b53-149">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="e6b53-149">Bulgaria</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-150">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-150">Pattern</span></span>

-  <span data-ttu-id="e6b53-151">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-151">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-152">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-152">Checksum</span></span>

<span data-ttu-id="e6b53-153">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-153">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-154">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-154">Definition</span></span>

<span data-ttu-id="e6b53-155">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-155">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-156">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-156">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-157">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-157">A keyword from is found.</span></span>
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75>
</Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_belgium_eu_gps_data_2" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_1" />
          <Match idRef="Keywords_bulgaria_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_gps_data_2" />
          <Match idRef="Keywords_bulgaria_eu_gps_data" />
        </Pattern>
</Entity>
```

## <a name="croatia"></a><span data-ttu-id="e6b53-158">Kroatien</span><span class="sxs-lookup"><span data-stu-id="e6b53-158">Croatia</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-159">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-159">Pattern</span></span>

-  <span data-ttu-id="e6b53-160">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-160">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-161">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-161">Checksum</span></span>

<span data-ttu-id="e6b53-162">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-162">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-163">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-163">Definition</span></span>

<span data-ttu-id="e6b53-164">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-164">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-165">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-165">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-166">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-166">A keyword from is found.</span></span>
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_gps_data_1" />
          <Match idRef="Keywords_croatia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_croatia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_gps_data_2" />
          <Match idRef="Keywords_croatia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_croatia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="cyprus"></a><span data-ttu-id="e6b53-167">Zypern</span><span class="sxs-lookup"><span data-stu-id="e6b53-167">Cyprus</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-168">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-168">Pattern</span></span>

-  <span data-ttu-id="e6b53-169">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-169">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-170">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-170">Checksum</span></span>

<span data-ttu-id="e6b53-171">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-171">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-172">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-172">Definition</span></span>

<span data-ttu-id="e6b53-173">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-173">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-174">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-174">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-175">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-175">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_1" />
          <Match idRef="Keywords_cyprus_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_2" />
          <Match idRef="Keywords_cyprus_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_cyprus_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="czech-republic"></a><span data-ttu-id="e6b53-176">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="e6b53-176">Czech Republic</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-177">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-177">Pattern</span></span>

-  <span data-ttu-id="e6b53-178">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-178">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-179">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-179">Checksum</span></span>

<span data-ttu-id="e6b53-180">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-180">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-181">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-181">Definition</span></span>

<span data-ttu-id="e6b53-182">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-182">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
<span data-ttu-id="e6b53-183">Eine DLP-Richtlinie ist % sicher, dass diese Art von vertraulichen Informationen festgestellt wurde "If"; innerhalb einer Nähe von Zeichen:</span><span class="sxs-lookup"><span data-stu-id="e6b53-183">A DLP policy is % confident that it's detected this type of sensitive information if, within a proximity of characters:</span></span>
  
- <span data-ttu-id="e6b53-184">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-184">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-185">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-185">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_1" />
          <Match idRef="Keywords_czech_republic_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_2" />
          <Match idRef="Keywords_czech_republic_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_czech_republic_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="denmark"></a><span data-ttu-id="e6b53-186">Dänemark</span><span class="sxs-lookup"><span data-stu-id="e6b53-186">Denmark</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-187">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-187">Pattern</span></span>

-  <span data-ttu-id="e6b53-188">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-188">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-189">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-189">Checksum</span></span>

<span data-ttu-id="e6b53-190">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-190">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-191">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-191">Definition</span></span>

<span data-ttu-id="e6b53-192">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-192">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-193">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-193">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-194">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-194">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_gps_data_1" />
          <Match idRef="Keywords_denmark_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_denmark_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_gps_data_2" />
          <Match idRef="Keywords_denmark_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_denmark_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="estonia"></a><span data-ttu-id="e6b53-195">Estland</span><span class="sxs-lookup"><span data-stu-id="e6b53-195">Estonia</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-196">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-196">Pattern</span></span>

-  <span data-ttu-id="e6b53-197">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-197">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-198">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-198">Checksum</span></span>

<span data-ttu-id="e6b53-199">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-199">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-200">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-200">Definition</span></span>

<span data-ttu-id="e6b53-201">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-202">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-202">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-203">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-203">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_gps_data_1" />
          <Match idRef="Keywords_estonia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_estonia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_gps_data_2" />
          <Match idRef="Keywords_estonia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_estonia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="finland"></a><span data-ttu-id="e6b53-204">Finnland</span><span class="sxs-lookup"><span data-stu-id="e6b53-204">Finland</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-205">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-205">Pattern</span></span>

-  <span data-ttu-id="e6b53-206">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-206">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-207">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-207">Checksum</span></span>

<span data-ttu-id="e6b53-208">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-208">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-209">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-209">Definition</span></span>

<span data-ttu-id="e6b53-210">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-210">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-211">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-211">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-212">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-212">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_gps_data_1" />
          <Match idRef="Keywords_finland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_finland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_gps_data_2" />
          <Match idRef="Keywords_finland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_finland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="france"></a><span data-ttu-id="e6b53-213">Frankreich</span><span class="sxs-lookup"><span data-stu-id="e6b53-213">France</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-214">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-214">Pattern</span></span>

-  <span data-ttu-id="e6b53-215">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-215">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-216">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-216">Checksum</span></span>

<span data-ttu-id="e6b53-217">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-217">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-218">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-218">Definition</span></span>

<span data-ttu-id="e6b53-219">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-219">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-220">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-220">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-221">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-221">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_gps_data_1" />
          <Match idRef="Keywords_france_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_france_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_france_eu_gps_data_2" />
          <Match idRef="Keywords_france_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_france_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="germany"></a><span data-ttu-id="e6b53-222">Deutschland</span><span class="sxs-lookup"><span data-stu-id="e6b53-222">Germany</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-223">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-223">Pattern</span></span>

-  <span data-ttu-id="e6b53-224">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-224">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-225">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-225">Checksum</span></span>

<span data-ttu-id="e6b53-226">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-226">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-227">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-227">Definition</span></span>

<span data-ttu-id="e6b53-228">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-228">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-229">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-229">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-230">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-230">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_gps_data_1" />
          <Match idRef="Keywords_germany_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_germany_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_germany_eu_gps_data_2" />
          <Match idRef="Keywords_germany_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_germany_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="greece"></a><span data-ttu-id="e6b53-231">Griechenland</span><span class="sxs-lookup"><span data-stu-id="e6b53-231">Greece</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-232">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-232">Pattern</span></span>

-  <span data-ttu-id="e6b53-233">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-233">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-234">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-234">Checksum</span></span>

<span data-ttu-id="e6b53-235">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-235">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-236">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-236">Definition</span></span>

<span data-ttu-id="e6b53-237">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-237">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-238">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-238">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-239">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-239">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_gps_data_1" />
          <Match idRef="Keywords_greece_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_greece_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_gps_data_2" />
          <Match idRef="Keywords_greece_eu_gps_data" />
        </Pattern>
</Entity>
```

## <a name="hungary"></a><span data-ttu-id="e6b53-240">Ungarn</span><span class="sxs-lookup"><span data-stu-id="e6b53-240">Hungary</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-241">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-241">Pattern</span></span>

-  <span data-ttu-id="e6b53-242">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-242">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-243">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-243">Checksum</span></span>

<span data-ttu-id="e6b53-244">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-244">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-245">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-245">Definition</span></span>

<span data-ttu-id="e6b53-246">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-246">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-247">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-247">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-248">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-248">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_gps_data_1" />
          <Match idRef="Keywords_hungary_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_hungary_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_gps_data_2" />
          <Match idRef="Keywords_hungary_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_hungary_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="ireland"></a><span data-ttu-id="e6b53-249">Irland</span><span class="sxs-lookup"><span data-stu-id="e6b53-249">Ireland</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-250">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-250">Pattern</span></span>

-  <span data-ttu-id="e6b53-251">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-251">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-252">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-252">Checksum</span></span>

<span data-ttu-id="e6b53-253">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-253">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-254">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-254">Definition</span></span>

<span data-ttu-id="e6b53-255">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-255">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-256">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-256">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-257">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-257">A keyword from is found.</span></span>
    
```
 
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_gps_data_1" />
          <Match idRef="Keywords_ireland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_ireland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_gps_data_2" />
          <Match idRef="Keywords_ireland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_ireland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="italy"></a><span data-ttu-id="e6b53-258">Italien</span><span class="sxs-lookup"><span data-stu-id="e6b53-258">Italy</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-259">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-259">Pattern</span></span>

-  <span data-ttu-id="e6b53-260">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-260">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-261">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-261">Checksum</span></span>

<span data-ttu-id="e6b53-262">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-262">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-263">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-263">Definition</span></span>

<span data-ttu-id="e6b53-264">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-264">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-265">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-265">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-266">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-266">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_gps_data_1" />
          <Match idRef="Keywords_italy_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_italy_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_gps_data_2" />
          <Match idRef="Keywords_italy_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_italy_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="latvia"></a><span data-ttu-id="e6b53-267">Lettland</span><span class="sxs-lookup"><span data-stu-id="e6b53-267">Latvia</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-268">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-268">Pattern</span></span>

-  <span data-ttu-id="e6b53-269">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-269">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-270">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-270">Checksum</span></span>

<span data-ttu-id="e6b53-271">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-271">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-272">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-272">Definition</span></span>

<span data-ttu-id="e6b53-273">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-273">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-274">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-274">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-275">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-275">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_gps_data_1" />
          <Match idRef="Keywords_latvia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_latvia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_gps_data_2" />
          <Match idRef="Keywords_latvia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_latvia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="lithuania"></a><span data-ttu-id="e6b53-276">Litauen</span><span class="sxs-lookup"><span data-stu-id="e6b53-276">Lithuania</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-277">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-277">Pattern</span></span>

-  <span data-ttu-id="e6b53-278">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-278">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-279">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-279">Checksum</span></span>

<span data-ttu-id="e6b53-280">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-280">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-281">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-281">Definition</span></span>

<span data-ttu-id="e6b53-282">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-282">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-283">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-283">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-284">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-284">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_1" />
          <Match idRef="Keywords_lithuania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_2" />
          <Match idRef="Keywords_lithuania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_lithuania_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="luxemburg"></a><span data-ttu-id="e6b53-285">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="e6b53-285">Luxemburg</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-286">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-286">Pattern</span></span>

-  <span data-ttu-id="e6b53-287">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-287">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-288">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-288">Checksum</span></span>

<span data-ttu-id="e6b53-289">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-289">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-290">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-290">Definition</span></span>

<span data-ttu-id="e6b53-291">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-291">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-292">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-292">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-293">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-293">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_1" />
          <Match idRef="Keywords_luxemburg_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_2" />
          <Match idRef="Keywords_luxemburg_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_luxemburg_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="malta"></a><span data-ttu-id="e6b53-294">Malta</span><span class="sxs-lookup"><span data-stu-id="e6b53-294">Malta</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-295">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-295">Pattern</span></span>

-  <span data-ttu-id="e6b53-296">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-296">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-297">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-297">Checksum</span></span>

<span data-ttu-id="e6b53-298">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-298">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-299">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-299">Definition</span></span>

<span data-ttu-id="e6b53-300">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-301">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-301">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-302">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-302">A keyword from is found.</span></span>
    
```
<Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_gps_data_1" />
          <Match idRef="Keywords_malta_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_gps_data_2" />
          <Match idRef="Keywords_malta_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="netherlands"></a><span data-ttu-id="e6b53-303">Niederlande</span><span class="sxs-lookup"><span data-stu-id="e6b53-303">Netherlands</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-304">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-304">Pattern</span></span>

-  <span data-ttu-id="e6b53-305">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-305">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-306">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-306">Checksum</span></span>

<span data-ttu-id="e6b53-307">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-307">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-308">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-308">Definition</span></span>

<span data-ttu-id="e6b53-309">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-309">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-310">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-310">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-311">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-311">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_1" />
          <Match idRef="Keywords_netherlands_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_2" />
          <Match idRef="Keywords_netherlands_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_netherlands_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="poland"></a><span data-ttu-id="e6b53-312">Polen</span><span class="sxs-lookup"><span data-stu-id="e6b53-312">Poland</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-313">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-313">Pattern</span></span>

-  <span data-ttu-id="e6b53-314">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-314">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-315">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-315">Checksum</span></span>

<span data-ttu-id="e6b53-316">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-316">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-317">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-317">Definition</span></span>

<span data-ttu-id="e6b53-318">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-318">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-319">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-319">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-320">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-320">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_gps_data_1" />
          <Match idRef="Keywords_poland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_poland_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_gps_data_2" />
          <Match idRef="Keywords_poland_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_poland_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="portugal"></a><span data-ttu-id="e6b53-321">Portugal</span><span class="sxs-lookup"><span data-stu-id="e6b53-321">Portugal</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-322">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-322">Pattern</span></span>

-  <span data-ttu-id="e6b53-323">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-323">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-324">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-324">Checksum</span></span>

<span data-ttu-id="e6b53-325">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-325">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-326">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-326">Definition</span></span>

<span data-ttu-id="e6b53-327">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-327">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-328">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-328">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-329">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-329">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_gps_data_1" />
          <Match idRef="Keywords_portugal_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_portugal_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_gps_data_2" />
          <Match idRef="Keywords_portugal_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_portugal_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="romania"></a><span data-ttu-id="e6b53-330">Rumänien</span><span class="sxs-lookup"><span data-stu-id="e6b53-330">Romania</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-331">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-331">Pattern</span></span>

-  <span data-ttu-id="e6b53-332">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-332">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-333">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-333">Checksum</span></span>

<span data-ttu-id="e6b53-334">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-334">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-335">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-335">Definition</span></span>

<span data-ttu-id="e6b53-336">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-336">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-337">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-337">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-338">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-338">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_gps_data_1" />
          <Match idRef="Keywords_romania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_romania_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_gps_data_2" />
          <Match idRef="Keywords_romania_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_romania_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="slovakia"></a><span data-ttu-id="e6b53-339">Slowakei</span><span class="sxs-lookup"><span data-stu-id="e6b53-339">Slovakia</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-340">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-340">Pattern</span></span>

-  <span data-ttu-id="e6b53-341">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-341">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-342">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-342">Checksum</span></span>

<span data-ttu-id="e6b53-343">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-343">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-344">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-344">Definition</span></span>

<span data-ttu-id="e6b53-345">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-345">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-346">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-346">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-347">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-347">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_1" />
          <Match idRef="Keywords_slovakia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_2" />
          <Match idRef="Keywords_slovakia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovakia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="slovenia"></a><span data-ttu-id="e6b53-348">Slowenien</span><span class="sxs-lookup"><span data-stu-id="e6b53-348">Slovenia</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-349">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-349">Pattern</span></span>

-  <span data-ttu-id="e6b53-350">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-350">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-351">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-351">Checksum</span></span>

<span data-ttu-id="e6b53-352">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-352">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-353">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-353">Definition</span></span>

<span data-ttu-id="e6b53-354">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-354">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-355">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-355">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-356">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-356">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_1" />
          <Match idRef="Keywords_slovenia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_2" />
          <Match idRef="Keywords_slovenia_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_slovenia_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="spain"></a><span data-ttu-id="e6b53-357">Spanien</span><span class="sxs-lookup"><span data-stu-id="e6b53-357">Spain</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-358">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-358">Pattern</span></span>

-  <span data-ttu-id="e6b53-359">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-359">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-360">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-360">Checksum</span></span>

<span data-ttu-id="e6b53-361">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-361">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-362">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-362">Definition</span></span>

<span data-ttu-id="e6b53-363">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-363">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-364">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-364">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-365">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-365">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_gps_data_1" />
          <Match idRef="Keywords_spain_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_spain_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_gps_data_2" />
          <Match idRef="Keywords_spain_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_spain_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="sweden"></a><span data-ttu-id="e6b53-366">Schweden</span><span class="sxs-lookup"><span data-stu-id="e6b53-366">Sweden</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-367">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-367">Pattern</span></span>

-  <span data-ttu-id="e6b53-368">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-368">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-369">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-369">Checksum</span></span>

<span data-ttu-id="e6b53-370">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-370">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-371">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-371">Definition</span></span>

<span data-ttu-id="e6b53-372">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-372">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-373">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-373">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-374">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-374">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_gps_data_1" />
          <Match idRef="Keywords_sweden_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_sweden_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_gps_data_2" />
          <Match idRef="Keywords_sweden_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_sweden_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="uk"></a><span data-ttu-id="e6b53-375">GROßBRITANNIEN</span><span class="sxs-lookup"><span data-stu-id="e6b53-375">UK</span></span>

### <a name="pattern"></a><span data-ttu-id="e6b53-376">Muster</span><span class="sxs-lookup"><span data-stu-id="e6b53-376">Pattern</span></span>

-  <span data-ttu-id="e6b53-377">Ziffern</span><span class="sxs-lookup"><span data-stu-id="e6b53-377">digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="e6b53-378">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="e6b53-378">Checksum</span></span>

<span data-ttu-id="e6b53-379">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="e6b53-379">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="e6b53-380">Definition</span><span class="sxs-lookup"><span data-stu-id="e6b53-380">Definition</span></span>

<span data-ttu-id="e6b53-381">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="e6b53-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="e6b53-382">Der reguläre Ausdruck sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="e6b53-382">The regular expression finds content that matches the pattern.</span></span>
    
- <span data-ttu-id="e6b53-383">Ein Schlüsselwort gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="e6b53-383">A keyword from is found.</span></span>
    
```
 <Entity id="42ac9f40-0912-4ae3-b5e6-08967192dec0" patternsProximity="300" recommendedConfidence="75">
<Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_gps_data_1" />
          <Match idRef="Keywords_uk_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_uk_eu_gps_data_1" />
        </Pattern>
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_uk_eu_gps_data_2" />
          <Match idRef="Keywords_uk_eu_gps_data" />
        </Pattern>
        <Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_uk_eu_gps_data_2" />
        </Pattern>
</Entity>
```

## <a name="see-also"></a><span data-ttu-id="e6b53-384">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6b53-384">See also</span></span>

[<span data-ttu-id="e6b53-385">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="e6b53-385">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

