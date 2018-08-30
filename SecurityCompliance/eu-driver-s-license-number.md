---
title: EU Führerscheinnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für Wenn vertrauliche Informationen vom Typ der EU-Treiber Lizenz Zahl erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 065684249f9766d567c63e6b8170d36f56692e45
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529414"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="db08d-104">EU Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-104">EU Driver's License Number</span></span>

<span data-ttu-id="db08d-p102">In diesem Thema wird eine Data Loss Prevention (DLP) Richtlinie sieht für Wenn vertrauliche Informationen vom Typ der EU-Treiber Lizenz Zahl erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="db08d-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="db08d-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="db08d-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="db08d-108">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-108">Format</span></span>

<span data-ttu-id="db08d-109">Acht Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-110">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-110">Pattern</span></span>

<span data-ttu-id="db08d-111">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="db08d-112">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-112">Checksum</span></span>

<span data-ttu-id="db08d-113">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-114">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-114">Definition</span></span>

<span data-ttu-id="db08d-115">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-116">Der reguläre Ausdruck `Regex_austria_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-117">Ein Schlüsselwort aus `Keywords_austria_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="db08d-118">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-118">Keywords</span></span>

<span data-ttu-id="db08d-119">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-119"></span></span>
|<span data-ttu-id="db08d-120">**Keywords_austria_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-121">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-121">dl#</span></span>  <br/> <span data-ttu-id="db08d-122">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-122">driver license</span></span>  <br/> <span data-ttu-id="db08d-123">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-123">driver license number</span></span>  <br/> <span data-ttu-id="db08d-124">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-124">driver licence</span></span>  <br/> <span data-ttu-id="db08d-125">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-125">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-126">drivers license</span></span>  <br/> <span data-ttu-id="db08d-127">des Treibers-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-127">driver's licence</span></span>  <br/> <span data-ttu-id="db08d-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-128">driver's license</span></span>  <br/> <span data-ttu-id="db08d-129">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-129">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-130">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="db08d-131">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-131">driving license number</span></span>  <br/> <span data-ttu-id="db08d-132">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-132">dlno#</span></span>  <br/> <span data-ttu-id="db08d-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="db08d-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="db08d-134">Fuhrerschein Republik osterreich</span><span class="sxs-lookup"><span data-stu-id="db08d-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="db08d-135">Belgien</span><span class="sxs-lookup"><span data-stu-id="db08d-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="db08d-136">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-136">Format</span></span>

<span data-ttu-id="db08d-137">10 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-138">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-138">Pattern</span></span>

<span data-ttu-id="db08d-139">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="db08d-140">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-140">Checksum</span></span>

<span data-ttu-id="db08d-141">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-142">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-142">Definition</span></span>

<span data-ttu-id="db08d-143">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-144">Der reguläre Ausdruck `Regex_belgium_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-145">Ein Schlüsselwort aus `Keywords_belgium_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="db08d-146">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-146">Keywords</span></span>

<span data-ttu-id="db08d-147">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-147"></span></span>
|<span data-ttu-id="db08d-148">**Keywords__belgium_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-149">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-149">dl#</span></span>  <br/> <span data-ttu-id="db08d-150">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-150">driver license</span></span>  <br/> <span data-ttu-id="db08d-151">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-151">driver license number</span></span>  <br/> <span data-ttu-id="db08d-152">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-152">driver licence</span></span>  <br/> <span data-ttu-id="db08d-153">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-153">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-154">drivers license</span></span>  <br/> <span data-ttu-id="db08d-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-155">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-156">driver's license</span></span>  <br/> <span data-ttu-id="db08d-157">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-157">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-158">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-158">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-159">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-159">dlno#</span></span>  <br/> <span data-ttu-id="db08d-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="db08d-160">rijbewijs</span></span>  <br/> <span data-ttu-id="db08d-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="db08d-162">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="db08d-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="db08d-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="db08d-165">Führerschein-Nr.</span><span class="sxs-lookup"><span data-stu-id="db08d-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="db08d-166">Fuehrerschein-Nr.</span><span class="sxs-lookup"><span data-stu-id="db08d-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="db08d-167">Fuehrerschein-Nr.</span><span class="sxs-lookup"><span data-stu-id="db08d-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="db08d-168">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="db08d-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="db08d-169">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-169">Format</span></span>

<span data-ttu-id="db08d-170">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-171">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-171">Pattern</span></span>

<span data-ttu-id="db08d-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="db08d-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-173">Checksum</span></span>

<span data-ttu-id="db08d-174">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-175">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-175">Definition</span></span>

<span data-ttu-id="db08d-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-177">Der reguläre Ausdruck `Regex_bulgaria_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-178">Ein Schlüsselwort aus `Keywords_bulgaria_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="db08d-179">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-179">Keywords</span></span>

<span data-ttu-id="db08d-180">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-180"></span></span>
|<span data-ttu-id="db08d-181">**Keywords_bulgaria_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-182">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-182">dl#</span></span>  <br/> <span data-ttu-id="db08d-183">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-183">driver license</span></span>  <br/> <span data-ttu-id="db08d-184">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-184">driver license number</span></span>  <br/> <span data-ttu-id="db08d-185">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-185">driver licence</span></span>  <br/> <span data-ttu-id="db08d-186">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-186">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-187">drivers license</span></span>  <br/> <span data-ttu-id="db08d-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-188">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-189">driver's license</span></span>  <br/> <span data-ttu-id="db08d-190">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-190">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-191">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-191">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-192">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-192">driving license number</span></span>  <br/> <span data-ttu-id="db08d-193">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-193">dlno#</span></span>  <br/> <span data-ttu-id="db08d-194">СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МПС</span><span class="sxs-lookup"><span data-stu-id="db08d-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="db08d-195">СВИДЕТЕЛСТВО ЗА УПРАВЛЕНИЕ НА МОТОРНО ПРЕВОЗНО СРЕДСТВО</span><span class="sxs-lookup"><span data-stu-id="db08d-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="db08d-196">СУМПС</span><span class="sxs-lookup"><span data-stu-id="db08d-196">сумпс</span></span>  <br/> <span data-ttu-id="db08d-197">ШОФЬОРСКА КНИЖКА</span><span class="sxs-lookup"><span data-stu-id="db08d-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="db08d-198">Kroatien</span><span class="sxs-lookup"><span data-stu-id="db08d-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="db08d-199">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-199">Format</span></span>

<span data-ttu-id="db08d-200">Acht Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-201">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-201">Pattern</span></span>

<span data-ttu-id="db08d-202">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="db08d-203">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-203">Checksum</span></span>

<span data-ttu-id="db08d-204">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-205">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-205">Definition</span></span>

<span data-ttu-id="db08d-206">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-207">Der reguläre Ausdruck `Regex_croatia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-208">Ein Schlüsselwort aus `Keywords_croatia_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="db08d-209">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-209">Keywords</span></span>

<span data-ttu-id="db08d-210">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-210"></span></span>
|<span data-ttu-id="db08d-211">**Keywords_croatia_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-212">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-212">dl#</span></span>  <br/> <span data-ttu-id="db08d-213">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-213">driver license</span></span>  <br/> <span data-ttu-id="db08d-214">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-214">driver license number</span></span>  <br/> <span data-ttu-id="db08d-215">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-215">driver licence</span></span>  <br/> <span data-ttu-id="db08d-216">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-216">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-217">drivers license</span></span>  <br/> <span data-ttu-id="db08d-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-218">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-219">driver's license</span></span>  <br/> <span data-ttu-id="db08d-220">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-220">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-221">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-221">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-222">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-222">driving license number</span></span>  <br/> <span data-ttu-id="db08d-223">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-223">dlno#</span></span>  <br/> <span data-ttu-id="db08d-224">Vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="db08d-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="db08d-225">Zypern</span><span class="sxs-lookup"><span data-stu-id="db08d-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="db08d-226">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-226">Format</span></span>

<span data-ttu-id="db08d-227">12 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-228">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-228">Pattern</span></span>

<span data-ttu-id="db08d-229">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="db08d-230">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-230">Checksum</span></span>

<span data-ttu-id="db08d-231">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-232">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-232">Definition</span></span>

<span data-ttu-id="db08d-233">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-234">Der reguläre Ausdruck `Regex_cyprus_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-235">Ein Schlüsselwort aus `Keywords_cyprus_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-236">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-236">Keywords</span></span>

<span data-ttu-id="db08d-237">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-237"></span></span>
|<span data-ttu-id="db08d-238">**Keywords_cyprus_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-239">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-239">dl#</span></span>  <br/> <span data-ttu-id="db08d-240">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-240">driver license</span></span>  <br/> <span data-ttu-id="db08d-241">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-241">driver license number</span></span>  <br/> <span data-ttu-id="db08d-242">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-242">driver licence</span></span>  <br/> <span data-ttu-id="db08d-243">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-243">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-244">drivers license</span></span>  <br/> <span data-ttu-id="db08d-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-245">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-246">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-246">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-247">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-247">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-248">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-248">driving license number</span></span>  <br/> <span data-ttu-id="db08d-249">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-249">dlno#</span></span>  <br/> <span data-ttu-id="db08d-250">ΆΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="db08d-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="db08d-251">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="db08d-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="db08d-252">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-252">Format</span></span>

<span data-ttu-id="db08d-253">Zwei Buchstaben gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-254">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-254">Pattern</span></span>

<span data-ttu-id="db08d-255">Acht Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="db08d-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="db08d-256">Zwei Buchstaben (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="db08d-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="db08d-257">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="db08d-257">A space (optional)</span></span>
    
- <span data-ttu-id="db08d-258">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-259">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-259">Checksum</span></span>

<span data-ttu-id="db08d-260">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-261">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-261">Definition</span></span>

<span data-ttu-id="db08d-262">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-263">Der reguläre Ausdruck `Regex_czech_republic_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-264">Ein Schlüsselwort aus `Keywords_czech_republic_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="db08d-265">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-265">Keywords</span></span>

<span data-ttu-id="db08d-266">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-266"></span></span>
|<span data-ttu-id="db08d-267">**Keywords_czech_republic_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-268">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-268">dl#</span></span>  <br/> <span data-ttu-id="db08d-269">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-269">driver license</span></span>  <br/> <span data-ttu-id="db08d-270">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-270">driver license number</span></span>  <br/> <span data-ttu-id="db08d-271">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-271">driver licence</span></span>  <br/> <span data-ttu-id="db08d-272">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-272">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-273">drivers license</span></span>  <br/> <span data-ttu-id="db08d-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-274">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-275">driver's license</span></span>  <br/> <span data-ttu-id="db08d-276">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-276">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-277">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-277">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-278">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-278">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-279">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-279">driving license number</span></span>  <br/> <span data-ttu-id="db08d-280">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-280">dlno#</span></span>  <br/> <span data-ttu-id="db08d-281">Řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="db08d-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="db08d-282">Dänemark</span><span class="sxs-lookup"><span data-stu-id="db08d-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="db08d-283">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-283">Format</span></span>

<span data-ttu-id="db08d-284">Acht Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-285">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-285">Pattern</span></span>

<span data-ttu-id="db08d-286">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="db08d-287">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-287">Checksum</span></span>

<span data-ttu-id="db08d-288">Ja</span><span class="sxs-lookup"><span data-stu-id="db08d-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-289">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-289">Definition</span></span>

<span data-ttu-id="db08d-290">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-291">Der reguläre Ausdruck `Regex_denmark_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-292">Ein Schlüsselwort aus `Keywords_denmark_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="db08d-293">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-293">Keywords</span></span>

<span data-ttu-id="db08d-294">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-294"></span></span>
|<span data-ttu-id="db08d-295">**Keywords_denmark_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-296">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-296">dl#</span></span>  <br/> <span data-ttu-id="db08d-297">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-297">driver license</span></span>  <br/> <span data-ttu-id="db08d-298">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-298">driver license number</span></span>  <br/> <span data-ttu-id="db08d-299">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-299">driver licence</span></span>  <br/> <span data-ttu-id="db08d-300">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-300">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-301">drivers license</span></span>  <br/> <span data-ttu-id="db08d-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-302">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-303">driver's license</span></span>  <br/> <span data-ttu-id="db08d-304">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-304">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-305">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-305">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-306">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-306">driving license number</span></span>  <br/> <span data-ttu-id="db08d-307">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-307">dlno#</span></span>  <br/> <span data-ttu-id="db08d-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="db08d-308">kørekort</span></span>  <br/> <span data-ttu-id="db08d-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="db08d-310">Estland</span><span class="sxs-lookup"><span data-stu-id="db08d-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="db08d-311">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-311">Format</span></span>

<span data-ttu-id="db08d-312">Zwei Buchstaben gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-313">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-313">Pattern</span></span>

<span data-ttu-id="db08d-314">Zwei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="db08d-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="db08d-315">Die Buchstaben "ET" (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="db08d-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="db08d-316">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-317">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-317">Checksum</span></span>

<span data-ttu-id="db08d-318">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-319">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-319">Definition</span></span>

<span data-ttu-id="db08d-320">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-321">Der reguläre Ausdruck `Regex_estonia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-322">Ein Schlüsselwort aus `Keywords_estonia_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-323">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-323">Keywords</span></span>

<span data-ttu-id="db08d-324">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-324"></span></span>
|<span data-ttu-id="db08d-325">**Keywords_estonia_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-326">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-326">dl#</span></span>  <br/> <span data-ttu-id="db08d-327">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-327">driver license</span></span>  <br/> <span data-ttu-id="db08d-328">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-328">driver license number</span></span>  <br/> <span data-ttu-id="db08d-329">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-329">driver license number</span></span>  <br/> <span data-ttu-id="db08d-330">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-330">driver licence</span></span>  <br/> <span data-ttu-id="db08d-331">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-331">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-332">drivers license</span></span>  <br/> <span data-ttu-id="db08d-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-333">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-334">driver's license</span></span>  <br/> <span data-ttu-id="db08d-335">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-335">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-336">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-336">driving license number</span></span>  <br/> <span data-ttu-id="db08d-337">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-337">dlno#</span></span>  <br/> <span data-ttu-id="db08d-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="db08d-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="db08d-339">Finnland</span><span class="sxs-lookup"><span data-stu-id="db08d-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="db08d-340">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-340">Format</span></span>

<span data-ttu-id="db08d-341">10 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="db08d-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-342">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-342">Pattern</span></span>

<span data-ttu-id="db08d-343">10 Ziffern, die einen Bindestrich enthält:</span><span class="sxs-lookup"><span data-stu-id="db08d-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="db08d-344">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-344">Six digits</span></span> 
    
- <span data-ttu-id="db08d-345">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="db08d-345">A hyphen</span></span>
    
-  <span data-ttu-id="db08d-346">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="db08d-347">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-347">Checksum</span></span>

<span data-ttu-id="db08d-348">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-349">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-349">Definition</span></span>

<span data-ttu-id="db08d-350">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-351">Der reguläre Ausdruck `Regex_finland_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-352">Ein Schlüsselwort aus `Keywords_finland_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-353">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-353">Keywords</span></span>

<span data-ttu-id="db08d-354">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-354"></span></span>
|<span data-ttu-id="db08d-355">**Keywords_finland_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-356">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-356">dl#</span></span>  <br/> <span data-ttu-id="db08d-357">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-357">driver license</span></span>  <br/> <span data-ttu-id="db08d-358">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-358">driver license number</span></span>  <br/> <span data-ttu-id="db08d-359">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-359">driver licence</span></span>  <br/> <span data-ttu-id="db08d-360">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-360">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-361">drivers license</span></span>  <br/> <span data-ttu-id="db08d-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-362">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-363">driver's license</span></span>  <br/> <span data-ttu-id="db08d-364">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-364">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-365">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-365">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-366">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-366">driving license number</span></span>  <br/> <span data-ttu-id="db08d-367">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-367">dlno#</span></span>  <br/> <span data-ttu-id="db08d-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="db08d-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="db08d-369">Frankreich</span><span class="sxs-lookup"><span data-stu-id="db08d-369">France</span></span>

<span data-ttu-id="db08d-370">Weitere Informationen hierzu finden Sie im Abschnitt "Französische Führerscheinnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="db08d-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="db08d-371">Deutschland</span><span class="sxs-lookup"><span data-stu-id="db08d-371">Germany</span></span>

<span data-ttu-id="db08d-372">Weitere Informationen hierzu finden Sie im Abschnitt "Deutsche Führerscheinnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="db08d-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="db08d-373">Griechenland</span><span class="sxs-lookup"><span data-stu-id="db08d-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="db08d-374">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-374">Format</span></span>

<span data-ttu-id="db08d-375">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-376">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-376">Pattern</span></span>

 <span data-ttu-id="db08d-377">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="db08d-378">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-378">Checksum</span></span>

<span data-ttu-id="db08d-379">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-380">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-380">Definition</span></span>

<span data-ttu-id="db08d-381">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-382">Der reguläre Ausdruck `Regex_greece_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-383">Ein Schlüsselwort aus `Keywords_greece_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-384">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-384">Keywords</span></span>

<span data-ttu-id="db08d-385">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-385"></span></span>
|<span data-ttu-id="db08d-386">**Keywords_greece_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-387">DlL-</span><span class="sxs-lookup"><span data-stu-id="db08d-387">dlL#</span></span>  <br/> <span data-ttu-id="db08d-388">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-388">driver license</span></span>  <br/> <span data-ttu-id="db08d-389">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-389">driver license number</span></span>  <br/> <span data-ttu-id="db08d-390">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-390">driver licence</span></span>  <br/> <span data-ttu-id="db08d-391">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-391">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-392">drivers license</span></span>  <br/> <span data-ttu-id="db08d-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-393">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-394">driver's license</span></span>  <br/> <span data-ttu-id="db08d-395">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-395">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-396">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-396">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-397">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-397">driving license number</span></span>  <br/> <span data-ttu-id="db08d-398">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-398">dlno#</span></span>  <br/> <span data-ttu-id="db08d-399">ΔΕΙΑ ΟΔΉΓΗΣΗΣ</span><span class="sxs-lookup"><span data-stu-id="db08d-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="db08d-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="db08d-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="db08d-401">Ungarn</span><span class="sxs-lookup"><span data-stu-id="db08d-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="db08d-402">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-402">Format</span></span>

<span data-ttu-id="db08d-403">Zwei Buchstaben gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-404">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-404">Pattern</span></span>

<span data-ttu-id="db08d-405">Zwei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="db08d-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="db08d-406">Zwei Buchstaben (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="db08d-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="db08d-407">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-408">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-408">Checksum</span></span>

<span data-ttu-id="db08d-409">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-410">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-410">Definition</span></span>

<span data-ttu-id="db08d-411">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-412">Der reguläre Ausdruck `Regex_hungary_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-413">Ein Schlüsselwort aus `Keywords_hungary_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-414">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-414">Keywords</span></span>

<span data-ttu-id="db08d-415">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-415"></span></span>
|<span data-ttu-id="db08d-416">**Keywords_hungary_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-417">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-417">dl#</span></span>  <br/> <span data-ttu-id="db08d-418">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-418">driver license</span></span>  <br/> <span data-ttu-id="db08d-419">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-419">driver license number</span></span>  <br/> <span data-ttu-id="db08d-420">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-420">driver licence</span></span>  <br/> <span data-ttu-id="db08d-421">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-421">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-422">drivers license</span></span>  <br/> <span data-ttu-id="db08d-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-423">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-424">driver's license</span></span>  <br/> <span data-ttu-id="db08d-425">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-425">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-426">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-426">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-427">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-427">driving license number</span></span>  <br/> <span data-ttu-id="db08d-428">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-428">dlno#</span></span>  <br/> <span data-ttu-id="db08d-429">Vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="db08d-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="db08d-430">Irland</span><span class="sxs-lookup"><span data-stu-id="db08d-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="db08d-431">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-431">Format</span></span>

<span data-ttu-id="db08d-432">Sechs Ziffern, gefolgt von vier Buchstaben</span><span class="sxs-lookup"><span data-stu-id="db08d-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-433">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-433">Pattern</span></span>

<span data-ttu-id="db08d-434">Sechs Ziffern und vier Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="db08d-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="db08d-435">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-435">Six digits</span></span>
    
- <span data-ttu-id="db08d-436">Vier Buchstaben (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="db08d-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-437">Checksum</span></span>

<span data-ttu-id="db08d-438">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-439">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-439">Definition</span></span>

<span data-ttu-id="db08d-440">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-441">Der reguläre Ausdruck `Regex_ireland_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-442">Ein Schlüsselwort aus `Keywords_ireland_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-443">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-443">Keywords</span></span>

<span data-ttu-id="db08d-444">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-444"></span></span>
|<span data-ttu-id="db08d-445">**Keywords_ireland_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-446">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-446">dl#</span></span>  <br/> <span data-ttu-id="db08d-447">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-447">driver license</span></span>  <br/> <span data-ttu-id="db08d-448">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-448">driver license number</span></span>  <br/> <span data-ttu-id="db08d-449">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-449">driver licence</span></span>  <br/> <span data-ttu-id="db08d-450">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-450">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-451">drivers license</span></span>  <br/> <span data-ttu-id="db08d-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-452">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-453">driver's license</span></span>  <br/> <span data-ttu-id="db08d-454">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-454">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-455">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-455">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-456">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-456">driving license number</span></span>  <br/> <span data-ttu-id="db08d-457">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-457">dlno#</span></span>  <br/> <span data-ttu-id="db08d-458">Ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="db08d-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="db08d-459">Italien</span><span class="sxs-lookup"><span data-stu-id="db08d-459">Italy</span></span>

<span data-ttu-id="db08d-460">Weitere Informationen hierzu finden Sie im Abschnitt "Italien Führerscheinnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="db08d-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="db08d-461">Lettland</span><span class="sxs-lookup"><span data-stu-id="db08d-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="db08d-462">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-462">Format</span></span>

<span data-ttu-id="db08d-463">Drei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-464">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-464">Pattern</span></span>

<span data-ttu-id="db08d-465">Drei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="db08d-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="db08d-466">Drei Buchstaben (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="db08d-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="db08d-467">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-468">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-468">Checksum</span></span>

<span data-ttu-id="db08d-469">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-470">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-470">Definition</span></span>

<span data-ttu-id="db08d-471">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-472">Der reguläre Ausdruck `Regex_latvia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-473">Ein Schlüsselwort aus `Keywords_latvia_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-474">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-474">Keywords</span></span>

<span data-ttu-id="db08d-475">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-475"></span></span>
|<span data-ttu-id="db08d-476">**Keywords_latvia_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-477">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-477">dl#</span></span>  <br/> <span data-ttu-id="db08d-478">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-478">driver license</span></span>  <br/> <span data-ttu-id="db08d-479">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-479">driver license number</span></span>  <br/> <span data-ttu-id="db08d-480">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-480">driver licence</span></span>  <br/> <span data-ttu-id="db08d-481">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-481">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-482">drivers license</span></span>  <br/> <span data-ttu-id="db08d-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-483">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-484">driver's license</span></span>  <br/> <span data-ttu-id="db08d-485">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-485">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-486">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-486">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-487">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-487">driving license number</span></span>  <br/> <span data-ttu-id="db08d-488">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-488">dlno#</span></span>  <br/> <span data-ttu-id="db08d-489">Autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="db08d-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="db08d-490">Litauen</span><span class="sxs-lookup"><span data-stu-id="db08d-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="db08d-491">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-491">Format</span></span>

<span data-ttu-id="db08d-492">Acht Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-493">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-493">Pattern</span></span>

 <span data-ttu-id="db08d-494">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="db08d-495">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-495">Checksum</span></span>

<span data-ttu-id="db08d-496">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-497">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-497">Definition</span></span>

<span data-ttu-id="db08d-498">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-499">Der reguläre Ausdruck `Regex_lithuania_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-500">Ein Schlüsselwort aus `Keywords_lithuania_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-501">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-501">Keywords</span></span>

<span data-ttu-id="db08d-502">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-502"></span></span>
|<span data-ttu-id="db08d-503">**Keywords_lithuania_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-504">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-504">dl#</span></span>  <br/> <span data-ttu-id="db08d-505">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-505">driver license</span></span>  <br/> <span data-ttu-id="db08d-506">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-506">driver license number</span></span>  <br/> <span data-ttu-id="db08d-507">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-507">driver licence</span></span>  <br/> <span data-ttu-id="db08d-508">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-508">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-509">drivers license</span></span>  <br/> <span data-ttu-id="db08d-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-510">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-511">driver's license</span></span>  <br/> <span data-ttu-id="db08d-512">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-512">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-513">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-513">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-514">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-514">driving license number</span></span>  <br/> <span data-ttu-id="db08d-515">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-515">dlno#</span></span>  <br/> <span data-ttu-id="db08d-516">Vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="db08d-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="db08d-517">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="db08d-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="db08d-518">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-518">Format</span></span>

<span data-ttu-id="db08d-519">Sechs Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-520">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-520">Pattern</span></span>

 <span data-ttu-id="db08d-521">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="db08d-522">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-522">Checksum</span></span>

<span data-ttu-id="db08d-523">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-524">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-524">Definition</span></span>

<span data-ttu-id="db08d-525">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-526">Der reguläre Ausdruck `Regex_luxemburg_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-527">Ein Schlüsselwort aus `Keywords_luxemburg_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-528">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-528">Keywords</span></span>

<span data-ttu-id="db08d-529">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-529"></span></span>
|<span data-ttu-id="db08d-530">**Keywords_luxemburg_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-531">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-531">dl#</span></span>  <br/> <span data-ttu-id="db08d-532">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-532">driver license</span></span>  <br/> <span data-ttu-id="db08d-533">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-533">driver license number</span></span>  <br/> <span data-ttu-id="db08d-534">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-534">driver licence</span></span>  <br/> <span data-ttu-id="db08d-535">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-535">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-536">drivers license</span></span>  <br/> <span data-ttu-id="db08d-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-537">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-538">driver's license</span></span>  <br/> <span data-ttu-id="db08d-539">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-539">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-540">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-540">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-541">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-541">driving license number</span></span>  <br/> <span data-ttu-id="db08d-542">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-542">dlno#</span></span>  <br/> <span data-ttu-id="db08d-543">Fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="db08d-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="db08d-544">Malta</span><span class="sxs-lookup"><span data-stu-id="db08d-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="db08d-545">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-545">Format</span></span>

<span data-ttu-id="db08d-546">Kombination von zwei Zeichen und sechs Ziffern in dem angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-547">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-547">Pattern</span></span>

<span data-ttu-id="db08d-548">Kombination von zwei Zeichen und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="db08d-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="db08d-549">Zwei Zeichen (Ziffern oder Buchstaben, nicht die Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="db08d-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="db08d-550">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="db08d-550">A space (optional)</span></span>
    
- <span data-ttu-id="db08d-551">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-551">Three digits</span></span>
    
- <span data-ttu-id="db08d-552">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="db08d-552">A space (optional)</span></span>
    
- <span data-ttu-id="db08d-553">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-554">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-554">Checksum</span></span>

<span data-ttu-id="db08d-555">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-556">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-556">Definition</span></span>

<span data-ttu-id="db08d-557">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-558">Der reguläre Ausdruck `Regex_malta_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-559">Ein Schlüsselwort aus `Keywords_malta_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-560">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-560">Keywords</span></span>

<span data-ttu-id="db08d-561">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-561"></span></span>
|<span data-ttu-id="db08d-562">**Keywords_malta_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-563">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-563">dl#</span></span>  <br/> <span data-ttu-id="db08d-564">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-564">driver license</span></span>  <br/> <span data-ttu-id="db08d-565">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-565">driver license number</span></span>  <br/> <span data-ttu-id="db08d-566">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-566">driver licence</span></span>  <br/> <span data-ttu-id="db08d-567">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-567">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-568">drivers license</span></span>  <br/> <span data-ttu-id="db08d-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-569">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-570">driver's license</span></span>  <br/> <span data-ttu-id="db08d-571">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-571">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-572">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-572">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-573">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-573">driving license number</span></span>  <br/> <span data-ttu-id="db08d-574">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-574">dlno#</span></span>  <br/> <span data-ttu-id="db08d-575">Liċenzja Aufgaben-sewqan</span><span class="sxs-lookup"><span data-stu-id="db08d-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="db08d-576">Niederlande</span><span class="sxs-lookup"><span data-stu-id="db08d-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="db08d-577">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-577">Format</span></span>

<span data-ttu-id="db08d-578">10 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-579">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-579">Pattern</span></span>

<span data-ttu-id="db08d-580">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="db08d-581">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-581">Checksum</span></span>

<span data-ttu-id="db08d-582">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-583">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-583">Definition</span></span>

<span data-ttu-id="db08d-584">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-585">Der reguläre Ausdruck `Regex_netherlands_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-586">Ein Schlüsselwort aus `Keywords_netherlands_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-587">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-587">Keywords</span></span>

<span data-ttu-id="db08d-588">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-588"></span></span>
|<span data-ttu-id="db08d-589">**Keywords_netherlands_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-590">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-590">dl#</span></span>  <br/> <span data-ttu-id="db08d-591">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-591">driver license</span></span>  <br/> <span data-ttu-id="db08d-592">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-592">driver license number</span></span>  <br/> <span data-ttu-id="db08d-593">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-593">driver licence</span></span>  <br/> <span data-ttu-id="db08d-594">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-594">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-595">drivers license</span></span>  <br/> <span data-ttu-id="db08d-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-596">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-597">driver's license</span></span>  <br/> <span data-ttu-id="db08d-598">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-598">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-599">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-599">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-600">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-600">driving license number</span></span>  <br/> <span data-ttu-id="db08d-601">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-601">dlno#</span></span>  <br/> <span data-ttu-id="db08d-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="db08d-602">permis de conduire</span></span>  <br/> <span data-ttu-id="db08d-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="db08d-603">rijbewijs</span></span>  <br/> <span data-ttu-id="db08d-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="db08d-605">Polen</span><span class="sxs-lookup"><span data-stu-id="db08d-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="db08d-606">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-606">Format</span></span>

<span data-ttu-id="db08d-607">14 Stellen mit 2 Schrägstriche</span><span class="sxs-lookup"><span data-stu-id="db08d-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-608">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-608">Pattern</span></span>

<span data-ttu-id="db08d-609">14 Ziffern und 2 Schrägstriche:</span><span class="sxs-lookup"><span data-stu-id="db08d-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="db08d-610">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-610">Five digits</span></span> 
    
- <span data-ttu-id="db08d-611">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="db08d-611">A forward slash</span></span>
    
- <span data-ttu-id="db08d-612">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-612">Two digits</span></span>
    
- <span data-ttu-id="db08d-613">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="db08d-613">A forward slash</span></span>
    
- <span data-ttu-id="db08d-614">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-615">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-615">Checksum</span></span>

<span data-ttu-id="db08d-616">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-617">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-617">Definition</span></span>

<span data-ttu-id="db08d-618">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-619">Der reguläre Ausdruck `Regex_poland_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-620">Ein Schlüsselwort aus `Keywords_poland_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-621">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-621">Keywords</span></span>

<span data-ttu-id="db08d-622">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-622"></span></span>
|<span data-ttu-id="db08d-623">**Keywords_poland_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-624">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-624">dl#</span></span>  <br/> <span data-ttu-id="db08d-625">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-625">driver license</span></span>  <br/> <span data-ttu-id="db08d-626">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-626">driver license number</span></span>  <br/> <span data-ttu-id="db08d-627">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-627">driver licence</span></span>  <br/> <span data-ttu-id="db08d-628">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-628">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-629">drivers license</span></span>  <br/> <span data-ttu-id="db08d-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-630">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-631">driver's license</span></span>  <br/> <span data-ttu-id="db08d-632">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-632">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-633">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-633">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-634">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-634">driving license number</span></span>  <br/> <span data-ttu-id="db08d-635">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-635">dlno#</span></span>  <br/> <span data-ttu-id="db08d-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="db08d-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="db08d-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="db08d-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="db08d-638">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-638">Format</span></span>

<span data-ttu-id="db08d-639">Zwei Buchstaben gefolgt von einem sieben Zahlen in dem angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-640">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-640">Pattern</span></span>

<span data-ttu-id="db08d-641">Zwei Buchstaben gefolgt von sieben Ziffern mit Sonderzeichen:</span><span class="sxs-lookup"><span data-stu-id="db08d-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="db08d-642">Zwei Buchstaben (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="db08d-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="db08d-643">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="db08d-643">A hyphen</span></span>
    
- <span data-ttu-id="db08d-644">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-644">Six digits</span></span>
    
- <span data-ttu-id="db08d-645">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-645">A space</span></span>
    
- <span data-ttu-id="db08d-646">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="db08d-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-647">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-647">Checksum</span></span>

<span data-ttu-id="db08d-648">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-649">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-649">Definition</span></span>

<span data-ttu-id="db08d-650">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-651">Der reguläre Ausdruck `Regex_portugal_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-652">Ein Schlüsselwort aus `Keywords_portugal_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-653">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-653">Keywords</span></span>

<span data-ttu-id="db08d-654">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-654"></span></span>
|<span data-ttu-id="db08d-655">**Keywords_portugal_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-656">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-656">dl#</span></span>  <br/> <span data-ttu-id="db08d-657">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-657">driver license</span></span>  <br/> <span data-ttu-id="db08d-658">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-658">driver license number</span></span>  <br/> <span data-ttu-id="db08d-659">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-659">driver licence</span></span>  <br/> <span data-ttu-id="db08d-660">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-660">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-661">drivers license</span></span>  <br/> <span data-ttu-id="db08d-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-662">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-663">driver's license</span></span>  <br/> <span data-ttu-id="db08d-664">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-664">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-665">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-665">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-666">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-666">driving license number</span></span>  <br/> <span data-ttu-id="db08d-667">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-667">dlno#</span></span>  <br/> <span data-ttu-id="db08d-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="db08d-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="db08d-669">Rumänien</span><span class="sxs-lookup"><span data-stu-id="db08d-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="db08d-670">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-670">Format</span></span>

<span data-ttu-id="db08d-671">Ein Zeichen, gefolgt von acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-672">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-672">Pattern</span></span>

<span data-ttu-id="db08d-673">Ein Zeichen, gefolgt von acht Stellen:</span><span class="sxs-lookup"><span data-stu-id="db08d-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="db08d-674">Eine (nicht Groß-/Kleinschreibung) Buchstabe oder Zahl</span><span class="sxs-lookup"><span data-stu-id="db08d-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="db08d-675">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-676">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-676">Checksum</span></span>

<span data-ttu-id="db08d-677">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-678">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-678">Definition</span></span>

<span data-ttu-id="db08d-679">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-680">Der reguläre Ausdruck `Regex_romania_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-681">Ein Schlüsselwort aus `Keywords_romania_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-682">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-682">Keywords</span></span>

<span data-ttu-id="db08d-683">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-683"></span></span>
|<span data-ttu-id="db08d-684">**Keywords_romania_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-685">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-685">dl#</span></span>  <br/> <span data-ttu-id="db08d-686">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-686">driver license</span></span>  <br/> <span data-ttu-id="db08d-687">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-687">driver license number</span></span>  <br/> <span data-ttu-id="db08d-688">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-688">driver licence</span></span>  <br/> <span data-ttu-id="db08d-689">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-689">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-690">drivers license</span></span>  <br/> <span data-ttu-id="db08d-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-691">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-692">driver's license</span></span>  <br/> <span data-ttu-id="db08d-693">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-693">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-694">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-694">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-695">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-695">driving license number</span></span>  <br/> <span data-ttu-id="db08d-696">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-696">dlno#</span></span>  <br/> <span data-ttu-id="db08d-697">Permis de conducere</span><span class="sxs-lookup"><span data-stu-id="db08d-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="db08d-698">Slowakei</span><span class="sxs-lookup"><span data-stu-id="db08d-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="db08d-699">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-699">Format</span></span>

<span data-ttu-id="db08d-700">Ein Zeichen, gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-701">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-701">Pattern</span></span>

<span data-ttu-id="db08d-702">Ein Zeichen, gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="db08d-703">Eine (nicht Groß-/Kleinschreibung) Buchstabe oder Zahl</span><span class="sxs-lookup"><span data-stu-id="db08d-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="db08d-704">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="db08d-705">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-705">Checksum</span></span>

<span data-ttu-id="db08d-706">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-707">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-707">Definition</span></span>

<span data-ttu-id="db08d-708">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-709">Der reguläre Ausdruck `Regex_slovakia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-710">Ein Schlüsselwort aus `Keywords_slovakia_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-711">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-711">Keywords</span></span>

<span data-ttu-id="db08d-712">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-712"></span></span>
|<span data-ttu-id="db08d-713">**Keywords_slovakia_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-714">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-714">dl#</span></span>  <br/> <span data-ttu-id="db08d-715">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-715">driver license</span></span>  <br/> <span data-ttu-id="db08d-716">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-716">driver license number</span></span>  <br/> <span data-ttu-id="db08d-717">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-717">driver licence</span></span>  <br/> <span data-ttu-id="db08d-718">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-718">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-719">drivers license</span></span>  <br/> <span data-ttu-id="db08d-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-720">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-721">driver's license</span></span>  <br/> <span data-ttu-id="db08d-722">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-722">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-723">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-723">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-724">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-724">driving license number</span></span>  <br/> <span data-ttu-id="db08d-725">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-725">dlno#</span></span>  <br/> <span data-ttu-id="db08d-726">Vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="db08d-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="db08d-727">Slowenien</span><span class="sxs-lookup"><span data-stu-id="db08d-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="db08d-728">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-728">Format</span></span>

<span data-ttu-id="db08d-729">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-730">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-730">Pattern</span></span>

<span data-ttu-id="db08d-731">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="db08d-732">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-732">Checksum</span></span>

<span data-ttu-id="db08d-733">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-734">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-734">Definition</span></span>

<span data-ttu-id="db08d-735">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-736">Der reguläre Ausdruck `Regex_slovenia_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-737">Ein Schlüsselwort aus `Keywords_slovenia_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-738">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-738">Keywords</span></span>

<span data-ttu-id="db08d-739">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-739"></span></span>
|<span data-ttu-id="db08d-740">**Keywords_slovenia_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-741">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-741">dl#</span></span>  <br/> <span data-ttu-id="db08d-742">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-742">driver license</span></span>  <br/> <span data-ttu-id="db08d-743">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-743">driver license number</span></span>  <br/> <span data-ttu-id="db08d-744">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-744">driver licence</span></span>  <br/> <span data-ttu-id="db08d-745">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-745">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-746">drivers license</span></span>  <br/> <span data-ttu-id="db08d-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-747">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-748">driver's license</span></span>  <br/> <span data-ttu-id="db08d-749">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-749">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-750">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-750">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-751">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-751">driving license number</span></span>  <br/> <span data-ttu-id="db08d-752">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-752">dlno#</span></span>  <br/> <span data-ttu-id="db08d-753">Vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="db08d-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="db08d-754">Spanien</span><span class="sxs-lookup"><span data-stu-id="db08d-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="db08d-755">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-755">Format</span></span>

<span data-ttu-id="db08d-756">Acht Ziffern, gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="db08d-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-757">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-757">Pattern</span></span>

<span data-ttu-id="db08d-758">Acht Ziffern, gefolgt von einem Zeichen:</span><span class="sxs-lookup"><span data-stu-id="db08d-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="db08d-759">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-759">Eight digits</span></span> 
    
- <span data-ttu-id="db08d-760">Eine Ziffern oder Buchstaben (nicht Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="db08d-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-761">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-761">Checksum</span></span>

<span data-ttu-id="db08d-762">Ja</span><span class="sxs-lookup"><span data-stu-id="db08d-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-763">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-763">Definition</span></span>

<span data-ttu-id="db08d-764">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-765">Die Funktion `Func_spain_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-766">Ein Schlüsselwort aus `Keywords_spain_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="db08d-767">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-767">Keywords</span></span>

<span data-ttu-id="db08d-768">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-768"></span></span>
|<span data-ttu-id="db08d-769">**Keywords_spain_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-770">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-770">dlno#</span></span>  <br/> <span data-ttu-id="db08d-771">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-771">dl#</span></span>  <br/> <span data-ttu-id="db08d-772">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-772">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-773">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-773">driver licence</span></span>  <br/> <span data-ttu-id="db08d-774">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-774">driver license</span></span>  <br/> <span data-ttu-id="db08d-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-775">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-776">drivers license</span></span>  <br/> <span data-ttu-id="db08d-777">des Treibers-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-777">driver's licence</span></span>  <br/> <span data-ttu-id="db08d-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-778">driver's license</span></span>  <br/> <span data-ttu-id="db08d-779">driving licence
</span><span class="sxs-lookup"><span data-stu-id="db08d-779">driving licence</span></span>  <br/> <span data-ttu-id="db08d-780">gesteuerte Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-780">driving license</span></span>  <br/> <span data-ttu-id="db08d-781">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-781">driver licence number</span></span>  <br/> <span data-ttu-id="db08d-782">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-782">driver license number</span></span>  <br/> <span data-ttu-id="db08d-783">Treiber Lizenz Anzahl</span><span class="sxs-lookup"><span data-stu-id="db08d-783">drivers licence number</span></span>  <br/> <span data-ttu-id="db08d-784">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-784">drivers license number</span></span>  <br/> <span data-ttu-id="db08d-785">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-785">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-786">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-786">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-787">Anzahl der lenken-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-787">driving licence number</span></span>  <br/> <span data-ttu-id="db08d-788">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-788">driving license number</span></span>  <br/> <span data-ttu-id="db08d-789">gesteuerter zulassen</span><span class="sxs-lookup"><span data-stu-id="db08d-789">driving permit</span></span>  <br/> <span data-ttu-id="db08d-790">Anzahl der steuernde zulassen</span><span class="sxs-lookup"><span data-stu-id="db08d-790">driving permit number</span></span>  <br/> <span data-ttu-id="db08d-791">Permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="db08d-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="db08d-792">Permiso conducción</span><span class="sxs-lookup"><span data-stu-id="db08d-792">permiso conducción</span></span>  <br/> <span data-ttu-id="db08d-793">Número Licencia conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="db08d-794">Número de Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="db08d-795">Número Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="db08d-796">Licencia conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-796">licencia conducir</span></span>  <br/> <span data-ttu-id="db08d-797">Número de Permiso de conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="db08d-798">Número de Permiso conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="db08d-799">Número Permiso conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="db08d-800">Permiso conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-800">permiso conducir</span></span>  <br/> <span data-ttu-id="db08d-801">Licencia de sein</span><span class="sxs-lookup"><span data-stu-id="db08d-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="db08d-802">El Carnet de conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="db08d-803">Carnet conducir</span><span class="sxs-lookup"><span data-stu-id="db08d-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="db08d-804">Schweden</span><span class="sxs-lookup"><span data-stu-id="db08d-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="db08d-805">Format</span><span class="sxs-lookup"><span data-stu-id="db08d-805">Format</span></span>

<span data-ttu-id="db08d-806">Zehn Ziffern, die einen Bindestrich enthält</span><span class="sxs-lookup"><span data-stu-id="db08d-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="db08d-807">Muster</span><span class="sxs-lookup"><span data-stu-id="db08d-807">Pattern</span></span>

<span data-ttu-id="db08d-808">Zehn Ziffern, die einen Bindestrich enthält:</span><span class="sxs-lookup"><span data-stu-id="db08d-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="db08d-809">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-809">Six digits</span></span> 
    
- <span data-ttu-id="db08d-810">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="db08d-810">A hyphen</span></span>
    
- <span data-ttu-id="db08d-811">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="db08d-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="db08d-812">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="db08d-812">Checksum</span></span>

<span data-ttu-id="db08d-813">Nein</span><span class="sxs-lookup"><span data-stu-id="db08d-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="db08d-814">Definition</span><span class="sxs-lookup"><span data-stu-id="db08d-814">Definition</span></span>

<span data-ttu-id="db08d-815">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="db08d-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="db08d-816">Der reguläre Ausdruck `Regex_sweden_eu_driver's_license_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="db08d-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="db08d-817">Ein Schlüsselwort aus `Keywords_sweden_eu_driver's_license_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="db08d-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="db08d-818">Keywords</span><span class="sxs-lookup"><span data-stu-id="db08d-818">Keywords</span></span>

<span data-ttu-id="db08d-819">| |</span><span class="sxs-lookup"><span data-stu-id="db08d-819"></span></span>
|<span data-ttu-id="db08d-820">**Keywords_sweden_eu_driver'S_license_number**</span><span class="sxs-lookup"><span data-stu-id="db08d-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="db08d-821">dl#</span><span class="sxs-lookup"><span data-stu-id="db08d-821">dl#</span></span>  <br/> <span data-ttu-id="db08d-822">driver license</span><span class="sxs-lookup"><span data-stu-id="db08d-822">driver license</span></span>  <br/> <span data-ttu-id="db08d-823">Anzahl der Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-823">driver license number</span></span>  <br/> <span data-ttu-id="db08d-824">Treiber-Lizenz</span><span class="sxs-lookup"><span data-stu-id="db08d-824">driver licence</span></span>  <br/> <span data-ttu-id="db08d-825">Treiber Lic.</span><span class="sxs-lookup"><span data-stu-id="db08d-825">drivers lic.</span></span>  <br/> <span data-ttu-id="db08d-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="db08d-826">drivers license</span></span>  <br/> <span data-ttu-id="db08d-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="db08d-827">drivers licence</span></span>  <br/> <span data-ttu-id="db08d-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="db08d-828">driver's license</span></span>  <br/> <span data-ttu-id="db08d-829">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="db08d-829">driver's license number</span></span>  <br/> <span data-ttu-id="db08d-830">Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="db08d-830">driver's licence number</span></span>  <br/> <span data-ttu-id="db08d-831">Führerscheinnummer ein</span><span class="sxs-lookup"><span data-stu-id="db08d-831">driving license number</span></span>  <br/> <span data-ttu-id="db08d-832">Dlno #</span><span class="sxs-lookup"><span data-stu-id="db08d-832">dlno#</span></span>  <br/> <span data-ttu-id="db08d-833">körkort</span><span class="sxs-lookup"><span data-stu-id="db08d-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="db08d-834">GROßBRITANNIEN</span><span class="sxs-lookup"><span data-stu-id="db08d-834">UK</span></span>

<span data-ttu-id="db08d-p103">Weitere Informationen hierzu finden Sie im Abschnitt "Großbritannien Führerscheinnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="db08d-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="db08d-837">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db08d-837">See also</span></span>

[<span data-ttu-id="db08d-838">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="db08d-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

