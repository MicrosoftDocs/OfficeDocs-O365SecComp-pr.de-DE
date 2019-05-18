---
title: EU-Führerscheinnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn der vertrauliche Informationstyp des EU-Führerscheins für die Lizenznummer erkannt wird. Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.
ms.openlocfilehash: f1a95ecbaf6b6d1ac189290dd6d076cfd91ab30f
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152977"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="b0749-104">EU-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-104">EU Driver's License Number</span></span>

<span data-ttu-id="b0749-105">In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn der vertrauliche Informationstyp des EU-Führerscheins für die Lizenznummer erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="b0749-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="b0749-106">Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="b0749-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="b0749-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="b0749-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="b0749-108">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-108">Format</span></span>

<span data-ttu-id="b0749-109">Acht Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-110">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-110">Pattern</span></span>

<span data-ttu-id="b0749-111">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0749-112">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-112">Checksum</span></span>

<span data-ttu-id="b0749-113">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-114">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-114">Definition</span></span>

<span data-ttu-id="b0749-115">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-116">Der reguläre Ausdruck `Regex_austria_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-117">Ein Schlüsselwort `Keywords_austria_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="b0749-118">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-118">Keywords</span></span>

<span data-ttu-id="b0749-119">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-119"></span></span>
|<span data-ttu-id="b0749-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-121">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-121">dl#</span></span>  <br/> <span data-ttu-id="b0749-122">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-122">driver license</span></span>  <br/> <span data-ttu-id="b0749-123">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-123">driver license number</span></span>  <br/> <span data-ttu-id="b0749-124">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-124">driver licence</span></span>  <br/> <span data-ttu-id="b0749-125">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-125">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-126">drivers license</span></span>  <br/> <span data-ttu-id="b0749-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="b0749-127">driver's licence</span></span>  <br/> <span data-ttu-id="b0749-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-128">driver's license</span></span>  <br/> <span data-ttu-id="b0749-129">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-129">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-130">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="b0749-131">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-131">driving license number</span></span>  <br/> <span data-ttu-id="b0749-132">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-132">dlno#</span></span>  <br/> <span data-ttu-id="b0749-133">fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="b0749-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="b0749-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="b0749-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="b0749-135">Belgien</span><span class="sxs-lookup"><span data-stu-id="b0749-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="b0749-136">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-136">Format</span></span>

<span data-ttu-id="b0749-137">10 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-138">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-138">Pattern</span></span>

<span data-ttu-id="b0749-139">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0749-140">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-140">Checksum</span></span>

<span data-ttu-id="b0749-141">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-142">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-142">Definition</span></span>

<span data-ttu-id="b0749-143">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-144">Der reguläre Ausdruck `Regex_belgium_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-145">Ein Schlüsselwort `Keywords_belgium_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="b0749-146">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-146">Keywords</span></span>

<span data-ttu-id="b0749-147">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-147"></span></span>
|<span data-ttu-id="b0749-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-149">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-149">dl#</span></span>  <br/> <span data-ttu-id="b0749-150">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-150">driver license</span></span>  <br/> <span data-ttu-id="b0749-151">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-151">driver license number</span></span>  <br/> <span data-ttu-id="b0749-152">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-152">driver licence</span></span>  <br/> <span data-ttu-id="b0749-153">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-153">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-154">drivers license</span></span>  <br/> <span data-ttu-id="b0749-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-155">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-156">driver's license</span></span>  <br/> <span data-ttu-id="b0749-157">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-157">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-158">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-158">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-159">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-159">dlno#</span></span>  <br/> <span data-ttu-id="b0749-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="b0749-160">rijbewijs</span></span>  <br/> <span data-ttu-id="b0749-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="b0749-162">führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="b0749-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="b0749-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="b0749-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="b0749-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="b0749-166">Fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="b0749-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="b0749-167">Fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="b0749-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="b0749-168">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="b0749-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="b0749-169">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-169">Format</span></span>

<span data-ttu-id="b0749-170">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-171">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-171">Pattern</span></span>

<span data-ttu-id="b0749-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0749-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-173">Checksum</span></span>

<span data-ttu-id="b0749-174">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-175">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-175">Definition</span></span>

<span data-ttu-id="b0749-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-177">Der reguläre Ausdruck `Regex_bulgaria_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-178">Ein Schlüsselwort `Keywords_bulgaria_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="b0749-179">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-179">Keywords</span></span>

<span data-ttu-id="b0749-180">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-180"></span></span>
|<span data-ttu-id="b0749-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-182">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-182">dl#</span></span>  <br/> <span data-ttu-id="b0749-183">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-183">driver license</span></span>  <br/> <span data-ttu-id="b0749-184">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-184">driver license number</span></span>  <br/> <span data-ttu-id="b0749-185">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-185">driver licence</span></span>  <br/> <span data-ttu-id="b0749-186">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-186">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-187">drivers license</span></span>  <br/> <span data-ttu-id="b0749-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-188">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-189">driver's license</span></span>  <br/> <span data-ttu-id="b0749-190">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-190">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-191">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-191">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-192">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-192">driving license number</span></span>  <br/> <span data-ttu-id="b0749-193">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-193">dlno#</span></span>  <br/> <span data-ttu-id="b0749-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="b0749-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="b0749-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="b0749-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="b0749-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="b0749-196">сумпс</span></span>  <br/> <span data-ttu-id="b0749-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="b0749-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="b0749-198">Kroatien</span><span class="sxs-lookup"><span data-stu-id="b0749-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="b0749-199">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-199">Format</span></span>

<span data-ttu-id="b0749-200">Acht Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-201">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-201">Pattern</span></span>

<span data-ttu-id="b0749-202">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0749-203">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-203">Checksum</span></span>

<span data-ttu-id="b0749-204">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-205">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-205">Definition</span></span>

<span data-ttu-id="b0749-206">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-207">Der reguläre Ausdruck `Regex_croatia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-208">Ein Schlüsselwort `Keywords_croatia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="b0749-209">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-209">Keywords</span></span>

<span data-ttu-id="b0749-210">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-210"></span></span>
|<span data-ttu-id="b0749-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-212">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-212">dl#</span></span>  <br/> <span data-ttu-id="b0749-213">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-213">driver license</span></span>  <br/> <span data-ttu-id="b0749-214">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-214">driver license number</span></span>  <br/> <span data-ttu-id="b0749-215">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-215">driver licence</span></span>  <br/> <span data-ttu-id="b0749-216">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-216">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-217">drivers license</span></span>  <br/> <span data-ttu-id="b0749-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-218">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-219">driver's license</span></span>  <br/> <span data-ttu-id="b0749-220">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-220">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-221">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-221">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-222">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-222">driving license number</span></span>  <br/> <span data-ttu-id="b0749-223">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-223">dlno#</span></span>  <br/> <span data-ttu-id="b0749-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="b0749-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="b0749-225">Zypern</span><span class="sxs-lookup"><span data-stu-id="b0749-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="b0749-226">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-226">Format</span></span>

<span data-ttu-id="b0749-227">12 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-228">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-228">Pattern</span></span>

<span data-ttu-id="b0749-229">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0749-230">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-230">Checksum</span></span>

<span data-ttu-id="b0749-231">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-232">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-232">Definition</span></span>

<span data-ttu-id="b0749-233">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-234">Der reguläre Ausdruck `Regex_cyprus_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-235">Ein Schlüsselwort `Keywords_cyprus_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-236">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-236">Keywords</span></span>

<span data-ttu-id="b0749-237">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-237"></span></span>
|<span data-ttu-id="b0749-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-239">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-239">dl#</span></span>  <br/> <span data-ttu-id="b0749-240">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-240">driver license</span></span>  <br/> <span data-ttu-id="b0749-241">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-241">driver license number</span></span>  <br/> <span data-ttu-id="b0749-242">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-242">driver licence</span></span>  <br/> <span data-ttu-id="b0749-243">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-243">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-244">drivers license</span></span>  <br/> <span data-ttu-id="b0749-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-245">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-246">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-246">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-247">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-247">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-248">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-248">driving license number</span></span>  <br/> <span data-ttu-id="b0749-249">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-249">dlno#</span></span>  <br/> <span data-ttu-id="b0749-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="b0749-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="b0749-251">Tschechien</span><span class="sxs-lookup"><span data-stu-id="b0749-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="b0749-252">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-252">Format</span></span>

<span data-ttu-id="b0749-253">Zwei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-254">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-254">Pattern</span></span>

<span data-ttu-id="b0749-255">Acht Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="b0749-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="b0749-256">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="b0749-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="b0749-257">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="b0749-257">A space (optional)</span></span>
    
- <span data-ttu-id="b0749-258">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-259">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-259">Checksum</span></span>

<span data-ttu-id="b0749-260">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-261">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-261">Definition</span></span>

<span data-ttu-id="b0749-262">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-263">Der reguläre Ausdruck `Regex_czech_republic_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-264">Ein Schlüsselwort `Keywords_czech_republic_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="b0749-265">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-265">Keywords</span></span>

<span data-ttu-id="b0749-266">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-266"></span></span>
|<span data-ttu-id="b0749-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-268">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-268">dl#</span></span>  <br/> <span data-ttu-id="b0749-269">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-269">driver license</span></span>  <br/> <span data-ttu-id="b0749-270">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-270">driver license number</span></span>  <br/> <span data-ttu-id="b0749-271">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-271">driver licence</span></span>  <br/> <span data-ttu-id="b0749-272">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-272">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-273">drivers license</span></span>  <br/> <span data-ttu-id="b0749-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-274">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-275">driver's license</span></span>  <br/> <span data-ttu-id="b0749-276">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-276">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-277">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-277">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-278">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-278">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-279">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-279">driving license number</span></span>  <br/> <span data-ttu-id="b0749-280">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-280">dlno#</span></span>  <br/> <span data-ttu-id="b0749-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="b0749-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="b0749-282">Dänemark</span><span class="sxs-lookup"><span data-stu-id="b0749-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="b0749-283">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-283">Format</span></span>

<span data-ttu-id="b0749-284">Acht Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-285">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-285">Pattern</span></span>

<span data-ttu-id="b0749-286">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0749-287">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-287">Checksum</span></span>

<span data-ttu-id="b0749-288">Ja</span><span class="sxs-lookup"><span data-stu-id="b0749-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-289">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-289">Definition</span></span>

<span data-ttu-id="b0749-290">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-291">Der reguläre Ausdruck `Regex_denmark_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-292">Ein Schlüsselwort `Keywords_denmark_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="b0749-293">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-293">Keywords</span></span>

<span data-ttu-id="b0749-294">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-294"></span></span>
|<span data-ttu-id="b0749-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-296">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-296">dl#</span></span>  <br/> <span data-ttu-id="b0749-297">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-297">driver license</span></span>  <br/> <span data-ttu-id="b0749-298">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-298">driver license number</span></span>  <br/> <span data-ttu-id="b0749-299">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-299">driver licence</span></span>  <br/> <span data-ttu-id="b0749-300">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-300">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-301">drivers license</span></span>  <br/> <span data-ttu-id="b0749-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-302">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-303">driver's license</span></span>  <br/> <span data-ttu-id="b0749-304">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-304">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-305">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-305">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-306">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-306">driving license number</span></span>  <br/> <span data-ttu-id="b0749-307">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-307">dlno#</span></span>  <br/> <span data-ttu-id="b0749-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="b0749-308">kørekort</span></span>  <br/> <span data-ttu-id="b0749-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="b0749-310">Estland</span><span class="sxs-lookup"><span data-stu-id="b0749-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="b0749-311">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-311">Format</span></span>

<span data-ttu-id="b0749-312">Zwei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-313">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-313">Pattern</span></span>

<span data-ttu-id="b0749-314">Zwei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="b0749-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="b0749-315">Die Buchstaben "et" (unterscheidet nicht zwischen Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="b0749-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="b0749-316">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-317">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-317">Checksum</span></span>

<span data-ttu-id="b0749-318">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-319">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-319">Definition</span></span>

<span data-ttu-id="b0749-320">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-321">Der reguläre Ausdruck `Regex_estonia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-322">Ein Schlüsselwort `Keywords_estonia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-323">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-323">Keywords</span></span>

<span data-ttu-id="b0749-324">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-324"></span></span>
|<span data-ttu-id="b0749-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-326">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-326">dl#</span></span>  <br/> <span data-ttu-id="b0749-327">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-327">driver license</span></span>  <br/> <span data-ttu-id="b0749-328">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-328">driver license number</span></span>  <br/> <span data-ttu-id="b0749-329">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-329">driver license number</span></span>  <br/> <span data-ttu-id="b0749-330">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-330">driver licence</span></span>  <br/> <span data-ttu-id="b0749-331">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-331">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-332">drivers license</span></span>  <br/> <span data-ttu-id="b0749-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-333">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-334">driver's license</span></span>  <br/> <span data-ttu-id="b0749-335">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-335">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-336">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-336">driving license number</span></span>  <br/> <span data-ttu-id="b0749-337">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-337">dlno#</span></span>  <br/> <span data-ttu-id="b0749-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b0749-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="b0749-339">Finnland</span><span class="sxs-lookup"><span data-stu-id="b0749-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="b0749-340">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-340">Format</span></span>

<span data-ttu-id="b0749-341">10 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="b0749-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-342">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-342">Pattern</span></span>

<span data-ttu-id="b0749-343">10 Ziffern mit einem Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="b0749-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="b0749-344">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-344">Six digits</span></span> 
    
- <span data-ttu-id="b0749-345">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="b0749-345">A hyphen</span></span>
    
-  <span data-ttu-id="b0749-346">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="b0749-347">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-347">Checksum</span></span>

<span data-ttu-id="b0749-348">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-349">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-349">Definition</span></span>

<span data-ttu-id="b0749-350">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-351">Der reguläre Ausdruck `Regex_finland_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-352">Ein Schlüsselwort `Keywords_finland_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-353">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-353">Keywords</span></span>

<span data-ttu-id="b0749-354">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-354"></span></span>
|<span data-ttu-id="b0749-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-356">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-356">dl#</span></span>  <br/> <span data-ttu-id="b0749-357">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-357">driver license</span></span>  <br/> <span data-ttu-id="b0749-358">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-358">driver license number</span></span>  <br/> <span data-ttu-id="b0749-359">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-359">driver licence</span></span>  <br/> <span data-ttu-id="b0749-360">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-360">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-361">drivers license</span></span>  <br/> <span data-ttu-id="b0749-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-362">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-363">driver's license</span></span>  <br/> <span data-ttu-id="b0749-364">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-364">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-365">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-365">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-366">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-366">driving license number</span></span>  <br/> <span data-ttu-id="b0749-367">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-367">dlno#</span></span>  <br/> <span data-ttu-id="b0749-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="b0749-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="b0749-369">Frankreich</span><span class="sxs-lookup"><span data-stu-id="b0749-369">France</span></span>

<span data-ttu-id="b0749-370">Ausführliche Informationen finden Sie im Abschnitt "französische Führerscheinnummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b0749-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="b0749-371">Deutschland</span><span class="sxs-lookup"><span data-stu-id="b0749-371">Germany</span></span>

<span data-ttu-id="b0749-372">Ausführliche Informationen finden Sie im Abschnitt "Deutsche Führerscheinnummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b0749-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="b0749-373">Griechenland</span><span class="sxs-lookup"><span data-stu-id="b0749-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="b0749-374">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-374">Format</span></span>

<span data-ttu-id="b0749-375">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-376">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-376">Pattern</span></span>

 <span data-ttu-id="b0749-377">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="b0749-378">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-378">Checksum</span></span>

<span data-ttu-id="b0749-379">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-380">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-380">Definition</span></span>

<span data-ttu-id="b0749-381">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-382">Der reguläre Ausdruck `Regex_greece_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-383">Ein Schlüsselwort `Keywords_greece_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-384">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-384">Keywords</span></span>

<span data-ttu-id="b0749-385">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-385"></span></span>
|<span data-ttu-id="b0749-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-387">dlL</span><span class="sxs-lookup"><span data-stu-id="b0749-387">dlL#</span></span>  <br/> <span data-ttu-id="b0749-388">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-388">driver license</span></span>  <br/> <span data-ttu-id="b0749-389">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-389">driver license number</span></span>  <br/> <span data-ttu-id="b0749-390">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-390">driver licence</span></span>  <br/> <span data-ttu-id="b0749-391">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-391">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-392">drivers license</span></span>  <br/> <span data-ttu-id="b0749-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-393">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-394">driver's license</span></span>  <br/> <span data-ttu-id="b0749-395">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-395">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-396">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-396">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-397">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-397">driving license number</span></span>  <br/> <span data-ttu-id="b0749-398">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-398">dlno#</span></span>  <br/> <span data-ttu-id="b0749-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="b0749-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="b0749-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="b0749-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="b0749-401">Ungarn</span><span class="sxs-lookup"><span data-stu-id="b0749-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="b0749-402">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-402">Format</span></span>

<span data-ttu-id="b0749-403">Zwei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-404">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-404">Pattern</span></span>

<span data-ttu-id="b0749-405">Zwei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="b0749-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="b0749-406">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="b0749-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="b0749-407">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-408">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-408">Checksum</span></span>

<span data-ttu-id="b0749-409">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-410">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-410">Definition</span></span>

<span data-ttu-id="b0749-411">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-412">Der reguläre Ausdruck `Regex_hungary_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-413">Ein Schlüsselwort `Keywords_hungary_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-414">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-414">Keywords</span></span>

<span data-ttu-id="b0749-415">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-415"></span></span>
|<span data-ttu-id="b0749-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-417">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-417">dl#</span></span>  <br/> <span data-ttu-id="b0749-418">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-418">driver license</span></span>  <br/> <span data-ttu-id="b0749-419">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-419">driver license number</span></span>  <br/> <span data-ttu-id="b0749-420">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-420">driver licence</span></span>  <br/> <span data-ttu-id="b0749-421">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-421">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-422">drivers license</span></span>  <br/> <span data-ttu-id="b0749-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-423">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-424">driver's license</span></span>  <br/> <span data-ttu-id="b0749-425">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-425">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-426">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-426">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-427">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-427">driving license number</span></span>  <br/> <span data-ttu-id="b0749-428">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-428">dlno#</span></span>  <br/> <span data-ttu-id="b0749-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="b0749-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="b0749-430">Irland</span><span class="sxs-lookup"><span data-stu-id="b0749-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="b0749-431">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-431">Format</span></span>

<span data-ttu-id="b0749-432">Sechs Ziffern, gefolgt von vier Buchstaben</span><span class="sxs-lookup"><span data-stu-id="b0749-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-433">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-433">Pattern</span></span>

<span data-ttu-id="b0749-434">Sechs Ziffern und vier Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="b0749-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="b0749-435">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-435">Six digits</span></span>
    
- <span data-ttu-id="b0749-436">Vier Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="b0749-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-437">Checksum</span></span>

<span data-ttu-id="b0749-438">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-439">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-439">Definition</span></span>

<span data-ttu-id="b0749-440">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-441">Der reguläre Ausdruck `Regex_ireland_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-442">Ein Schlüsselwort `Keywords_ireland_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-443">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-443">Keywords</span></span>

<span data-ttu-id="b0749-444">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-444"></span></span>
|<span data-ttu-id="b0749-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-446">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-446">dl#</span></span>  <br/> <span data-ttu-id="b0749-447">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-447">driver license</span></span>  <br/> <span data-ttu-id="b0749-448">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-448">driver license number</span></span>  <br/> <span data-ttu-id="b0749-449">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-449">driver licence</span></span>  <br/> <span data-ttu-id="b0749-450">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-450">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-451">drivers license</span></span>  <br/> <span data-ttu-id="b0749-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-452">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-453">driver's license</span></span>  <br/> <span data-ttu-id="b0749-454">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-454">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-455">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-455">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-456">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-456">driving license number</span></span>  <br/> <span data-ttu-id="b0749-457">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-457">dlno#</span></span>  <br/> <span data-ttu-id="b0749-458">ceadúnas tiomána</span><span class="sxs-lookup"><span data-stu-id="b0749-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="b0749-459">Italien</span><span class="sxs-lookup"><span data-stu-id="b0749-459">Italy</span></span>

<span data-ttu-id="b0749-460">Ausführliche Informationen finden Sie im Abschnitt "Italien-Führerscheinnummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b0749-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="b0749-461">Lettland</span><span class="sxs-lookup"><span data-stu-id="b0749-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="b0749-462">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-462">Format</span></span>

<span data-ttu-id="b0749-463">Drei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-464">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-464">Pattern</span></span>

<span data-ttu-id="b0749-465">Drei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="b0749-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="b0749-466">Drei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="b0749-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="b0749-467">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-468">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-468">Checksum</span></span>

<span data-ttu-id="b0749-469">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-470">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-470">Definition</span></span>

<span data-ttu-id="b0749-471">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-472">Der reguläre Ausdruck `Regex_latvia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-473">Ein Schlüsselwort `Keywords_latvia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-474">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-474">Keywords</span></span>

<span data-ttu-id="b0749-475">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-475"></span></span>
|<span data-ttu-id="b0749-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-477">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-477">dl#</span></span>  <br/> <span data-ttu-id="b0749-478">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-478">driver license</span></span>  <br/> <span data-ttu-id="b0749-479">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-479">driver license number</span></span>  <br/> <span data-ttu-id="b0749-480">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-480">driver licence</span></span>  <br/> <span data-ttu-id="b0749-481">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-481">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-482">drivers license</span></span>  <br/> <span data-ttu-id="b0749-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-483">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-484">driver's license</span></span>  <br/> <span data-ttu-id="b0749-485">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-485">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-486">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-486">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-487">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-487">driving license number</span></span>  <br/> <span data-ttu-id="b0749-488">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-488">dlno#</span></span>  <br/> <span data-ttu-id="b0749-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="b0749-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="b0749-490">Litauen</span><span class="sxs-lookup"><span data-stu-id="b0749-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="b0749-491">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-491">Format</span></span>

<span data-ttu-id="b0749-492">Acht Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-493">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-493">Pattern</span></span>

 <span data-ttu-id="b0749-494">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="b0749-495">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-495">Checksum</span></span>

<span data-ttu-id="b0749-496">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-497">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-497">Definition</span></span>

<span data-ttu-id="b0749-498">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-499">Der reguläre Ausdruck `Regex_lithuania_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-500">Ein Schlüsselwort `Keywords_lithuania_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-501">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-501">Keywords</span></span>

<span data-ttu-id="b0749-502">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-502"></span></span>
|<span data-ttu-id="b0749-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-504">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-504">dl#</span></span>  <br/> <span data-ttu-id="b0749-505">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-505">driver license</span></span>  <br/> <span data-ttu-id="b0749-506">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-506">driver license number</span></span>  <br/> <span data-ttu-id="b0749-507">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-507">driver licence</span></span>  <br/> <span data-ttu-id="b0749-508">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-508">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-509">drivers license</span></span>  <br/> <span data-ttu-id="b0749-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-510">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-511">driver's license</span></span>  <br/> <span data-ttu-id="b0749-512">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-512">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-513">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-513">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-514">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-514">driving license number</span></span>  <br/> <span data-ttu-id="b0749-515">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-515">dlno#</span></span>  <br/> <span data-ttu-id="b0749-516">Vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="b0749-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="b0749-517">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="b0749-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="b0749-518">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-518">Format</span></span>

<span data-ttu-id="b0749-519">Sechs Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-520">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-520">Pattern</span></span>

 <span data-ttu-id="b0749-521">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="b0749-522">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-522">Checksum</span></span>

<span data-ttu-id="b0749-523">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-524">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-524">Definition</span></span>

<span data-ttu-id="b0749-525">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-526">Der reguläre Ausdruck `Regex_luxemburg_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-527">Ein Schlüsselwort `Keywords_luxemburg_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-528">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-528">Keywords</span></span>

<span data-ttu-id="b0749-529">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-529"></span></span>
|<span data-ttu-id="b0749-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-531">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-531">dl#</span></span>  <br/> <span data-ttu-id="b0749-532">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-532">driver license</span></span>  <br/> <span data-ttu-id="b0749-533">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-533">driver license number</span></span>  <br/> <span data-ttu-id="b0749-534">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-534">driver licence</span></span>  <br/> <span data-ttu-id="b0749-535">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-535">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-536">drivers license</span></span>  <br/> <span data-ttu-id="b0749-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-537">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-538">driver's license</span></span>  <br/> <span data-ttu-id="b0749-539">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-539">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-540">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-540">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-541">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-541">driving license number</span></span>  <br/> <span data-ttu-id="b0749-542">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-542">dlno#</span></span>  <br/> <span data-ttu-id="b0749-543">fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="b0749-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="b0749-544">Malta</span><span class="sxs-lookup"><span data-stu-id="b0749-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="b0749-545">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-545">Format</span></span>

<span data-ttu-id="b0749-546">Kombination aus zwei Zeichen und sechs Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-547">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-547">Pattern</span></span>

<span data-ttu-id="b0749-548">Kombination aus zwei Zeichen und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="b0749-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="b0749-549">Zwei Zeichen (Ziffern oder Buchstaben, bei denen die Groß-/Kleinschreibung nicht beachtet wird)</span><span class="sxs-lookup"><span data-stu-id="b0749-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="b0749-550">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="b0749-550">A space (optional)</span></span>
    
- <span data-ttu-id="b0749-551">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-551">Three digits</span></span>
    
- <span data-ttu-id="b0749-552">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="b0749-552">A space (optional)</span></span>
    
- <span data-ttu-id="b0749-553">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-554">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-554">Checksum</span></span>

<span data-ttu-id="b0749-555">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-556">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-556">Definition</span></span>

<span data-ttu-id="b0749-557">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-558">Der reguläre Ausdruck `Regex_malta_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-559">Ein Schlüsselwort `Keywords_malta_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-560">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-560">Keywords</span></span>

<span data-ttu-id="b0749-561">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-561"></span></span>
|<span data-ttu-id="b0749-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-563">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-563">dl#</span></span>  <br/> <span data-ttu-id="b0749-564">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-564">driver license</span></span>  <br/> <span data-ttu-id="b0749-565">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-565">driver license number</span></span>  <br/> <span data-ttu-id="b0749-566">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-566">driver licence</span></span>  <br/> <span data-ttu-id="b0749-567">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-567">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-568">drivers license</span></span>  <br/> <span data-ttu-id="b0749-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-569">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-570">driver's license</span></span>  <br/> <span data-ttu-id="b0749-571">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-571">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-572">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-572">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-573">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-573">driving license number</span></span>  <br/> <span data-ttu-id="b0749-574">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-574">dlno#</span></span>  <br/> <span data-ttu-id="b0749-575">Liċenzja TAS-Sewqan</span><span class="sxs-lookup"><span data-stu-id="b0749-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="b0749-576">Niederlande</span><span class="sxs-lookup"><span data-stu-id="b0749-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="b0749-577">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-577">Format</span></span>

<span data-ttu-id="b0749-578">10 Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-579">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-579">Pattern</span></span>

<span data-ttu-id="b0749-580">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0749-581">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-581">Checksum</span></span>

<span data-ttu-id="b0749-582">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-583">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-583">Definition</span></span>

<span data-ttu-id="b0749-584">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-585">Der reguläre Ausdruck `Regex_netherlands_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-586">Ein Schlüsselwort `Keywords_netherlands_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-587">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-587">Keywords</span></span>

<span data-ttu-id="b0749-588">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-588"></span></span>
|<span data-ttu-id="b0749-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-590">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-590">dl#</span></span>  <br/> <span data-ttu-id="b0749-591">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-591">driver license</span></span>  <br/> <span data-ttu-id="b0749-592">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-592">driver license number</span></span>  <br/> <span data-ttu-id="b0749-593">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-593">driver licence</span></span>  <br/> <span data-ttu-id="b0749-594">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-594">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-595">drivers license</span></span>  <br/> <span data-ttu-id="b0749-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-596">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-597">driver's license</span></span>  <br/> <span data-ttu-id="b0749-598">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-598">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-599">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-599">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-600">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-600">driving license number</span></span>  <br/> <span data-ttu-id="b0749-601">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-601">dlno#</span></span>  <br/> <span data-ttu-id="b0749-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="b0749-602">permis de conduire</span></span>  <br/> <span data-ttu-id="b0749-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="b0749-603">rijbewijs</span></span>  <br/> <span data-ttu-id="b0749-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="b0749-605">Polen</span><span class="sxs-lookup"><span data-stu-id="b0749-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="b0749-606">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-606">Format</span></span>

<span data-ttu-id="b0749-607">14 Ziffern mit 2 Schrägstrichen</span><span class="sxs-lookup"><span data-stu-id="b0749-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-608">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-608">Pattern</span></span>

<span data-ttu-id="b0749-609">14 Ziffern und 2 Schrägstriche:</span><span class="sxs-lookup"><span data-stu-id="b0749-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="b0749-610">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-610">Five digits</span></span> 
    
- <span data-ttu-id="b0749-611">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="b0749-611">A forward slash</span></span>
    
- <span data-ttu-id="b0749-612">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-612">Two digits</span></span>
    
- <span data-ttu-id="b0749-613">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="b0749-613">A forward slash</span></span>
    
- <span data-ttu-id="b0749-614">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-615">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-615">Checksum</span></span>

<span data-ttu-id="b0749-616">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-617">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-617">Definition</span></span>

<span data-ttu-id="b0749-618">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-619">Der reguläre Ausdruck `Regex_poland_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-620">Ein Schlüsselwort `Keywords_poland_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-621">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-621">Keywords</span></span>

<span data-ttu-id="b0749-622">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-622"></span></span>
|<span data-ttu-id="b0749-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-624">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-624">dl#</span></span>  <br/> <span data-ttu-id="b0749-625">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-625">driver license</span></span>  <br/> <span data-ttu-id="b0749-626">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-626">driver license number</span></span>  <br/> <span data-ttu-id="b0749-627">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-627">driver licence</span></span>  <br/> <span data-ttu-id="b0749-628">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-628">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-629">drivers license</span></span>  <br/> <span data-ttu-id="b0749-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-630">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-631">driver's license</span></span>  <br/> <span data-ttu-id="b0749-632">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-632">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-633">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-633">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-634">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-634">driving license number</span></span>  <br/> <span data-ttu-id="b0749-635">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-635">dlno#</span></span>  <br/> <span data-ttu-id="b0749-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="b0749-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="b0749-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="b0749-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="b0749-638">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-638">Format</span></span>

<span data-ttu-id="b0749-639">Zwei Buchstaben, gefolgt von sieben Zahlen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-640">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-640">Pattern</span></span>

<span data-ttu-id="b0749-641">Zwei Buchstaben, gefolgt von sieben Zahlen mit Sonderzeichen:</span><span class="sxs-lookup"><span data-stu-id="b0749-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="b0749-642">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="b0749-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="b0749-643">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="b0749-643">A hyphen</span></span>
    
- <span data-ttu-id="b0749-644">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-644">Six digits</span></span>
    
- <span data-ttu-id="b0749-645">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-645">A space</span></span>
    
- <span data-ttu-id="b0749-646">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="b0749-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-647">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-647">Checksum</span></span>

<span data-ttu-id="b0749-648">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-649">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-649">Definition</span></span>

<span data-ttu-id="b0749-650">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-651">Der reguläre Ausdruck `Regex_portugal_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-652">Ein Schlüsselwort `Keywords_portugal_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-653">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-653">Keywords</span></span>

<span data-ttu-id="b0749-654">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-654"></span></span>
|<span data-ttu-id="b0749-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-656">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-656">dl#</span></span>  <br/> <span data-ttu-id="b0749-657">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-657">driver license</span></span>  <br/> <span data-ttu-id="b0749-658">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-658">driver license number</span></span>  <br/> <span data-ttu-id="b0749-659">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-659">driver licence</span></span>  <br/> <span data-ttu-id="b0749-660">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-660">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-661">drivers license</span></span>  <br/> <span data-ttu-id="b0749-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-662">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-663">driver's license</span></span>  <br/> <span data-ttu-id="b0749-664">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-664">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-665">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-665">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-666">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-666">driving license number</span></span>  <br/> <span data-ttu-id="b0749-667">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-667">dlno#</span></span>  <br/> <span data-ttu-id="b0749-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="b0749-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="b0749-669">Rumänien</span><span class="sxs-lookup"><span data-stu-id="b0749-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="b0749-670">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-670">Format</span></span>

<span data-ttu-id="b0749-671">Ein Zeichen gefolgt von acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-672">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-672">Pattern</span></span>

<span data-ttu-id="b0749-673">Ein Zeichen gefolgt von acht Ziffern:</span><span class="sxs-lookup"><span data-stu-id="b0749-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="b0749-674">Ein Buchstabe (ohne Unterscheidung nach Groß-/Kleinschreibung) oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="b0749-675">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-676">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-676">Checksum</span></span>

<span data-ttu-id="b0749-677">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-678">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-678">Definition</span></span>

<span data-ttu-id="b0749-679">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-680">Der reguläre Ausdruck `Regex_romania_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-681">Ein Schlüsselwort `Keywords_romania_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-682">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-682">Keywords</span></span>

<span data-ttu-id="b0749-683">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-683"></span></span>
|<span data-ttu-id="b0749-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-685">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-685">dl#</span></span>  <br/> <span data-ttu-id="b0749-686">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-686">driver license</span></span>  <br/> <span data-ttu-id="b0749-687">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-687">driver license number</span></span>  <br/> <span data-ttu-id="b0749-688">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-688">driver licence</span></span>  <br/> <span data-ttu-id="b0749-689">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-689">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-690">drivers license</span></span>  <br/> <span data-ttu-id="b0749-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-691">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-692">driver's license</span></span>  <br/> <span data-ttu-id="b0749-693">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-693">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-694">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-694">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-695">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-695">driving license number</span></span>  <br/> <span data-ttu-id="b0749-696">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-696">dlno#</span></span>  <br/> <span data-ttu-id="b0749-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="b0749-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="b0749-698">Slowakei</span><span class="sxs-lookup"><span data-stu-id="b0749-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="b0749-699">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-699">Format</span></span>

<span data-ttu-id="b0749-700">Ein Zeichen gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-701">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-701">Pattern</span></span>

<span data-ttu-id="b0749-702">Ein Zeichen gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="b0749-703">Ein Buchstabe (ohne Unterscheidung nach Groß-/Kleinschreibung) oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="b0749-704">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="b0749-705">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-705">Checksum</span></span>

<span data-ttu-id="b0749-706">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-707">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-707">Definition</span></span>

<span data-ttu-id="b0749-708">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-709">Der reguläre Ausdruck `Regex_slovakia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-710">Ein Schlüsselwort `Keywords_slovakia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-711">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-711">Keywords</span></span>

<span data-ttu-id="b0749-712">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-712"></span></span>
|<span data-ttu-id="b0749-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-714">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-714">dl#</span></span>  <br/> <span data-ttu-id="b0749-715">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-715">driver license</span></span>  <br/> <span data-ttu-id="b0749-716">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-716">driver license number</span></span>  <br/> <span data-ttu-id="b0749-717">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-717">driver licence</span></span>  <br/> <span data-ttu-id="b0749-718">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-718">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-719">drivers license</span></span>  <br/> <span data-ttu-id="b0749-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-720">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-721">driver's license</span></span>  <br/> <span data-ttu-id="b0749-722">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-722">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-723">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-723">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-724">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-724">driving license number</span></span>  <br/> <span data-ttu-id="b0749-725">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-725">dlno#</span></span>  <br/> <span data-ttu-id="b0749-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="b0749-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="b0749-727">Slowenien</span><span class="sxs-lookup"><span data-stu-id="b0749-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="b0749-728">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-728">Format</span></span>

<span data-ttu-id="b0749-729">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-730">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-730">Pattern</span></span>

<span data-ttu-id="b0749-731">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="b0749-732">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-732">Checksum</span></span>

<span data-ttu-id="b0749-733">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-734">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-734">Definition</span></span>

<span data-ttu-id="b0749-735">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-736">Der reguläre Ausdruck `Regex_slovenia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-737">Ein Schlüsselwort `Keywords_slovenia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-738">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-738">Keywords</span></span>

<span data-ttu-id="b0749-739">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-739"></span></span>
|<span data-ttu-id="b0749-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-741">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-741">dl#</span></span>  <br/> <span data-ttu-id="b0749-742">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-742">driver license</span></span>  <br/> <span data-ttu-id="b0749-743">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-743">driver license number</span></span>  <br/> <span data-ttu-id="b0749-744">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-744">driver licence</span></span>  <br/> <span data-ttu-id="b0749-745">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-745">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-746">drivers license</span></span>  <br/> <span data-ttu-id="b0749-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-747">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-748">driver's license</span></span>  <br/> <span data-ttu-id="b0749-749">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-749">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-750">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-750">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-751">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-751">driving license number</span></span>  <br/> <span data-ttu-id="b0749-752">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-752">dlno#</span></span>  <br/> <span data-ttu-id="b0749-753">vozniško dovoljenje</span><span class="sxs-lookup"><span data-stu-id="b0749-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="b0749-754">Spanien</span><span class="sxs-lookup"><span data-stu-id="b0749-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="b0749-755">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-755">Format</span></span>

<span data-ttu-id="b0749-756">Acht Ziffern, gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="b0749-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-757">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-757">Pattern</span></span>

<span data-ttu-id="b0749-758">Acht Ziffern, gefolgt von einem Zeichen:</span><span class="sxs-lookup"><span data-stu-id="b0749-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="b0749-759">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-759">Eight digits</span></span> 
    
- <span data-ttu-id="b0749-760">Eine Ziffer oder ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="b0749-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-761">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-761">Checksum</span></span>

<span data-ttu-id="b0749-762">Ja</span><span class="sxs-lookup"><span data-stu-id="b0749-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-763">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-763">Definition</span></span>

<span data-ttu-id="b0749-764">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-765">Die- `Func_spain_eu_driver's_license_number` Funktion sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-766">Ein Schlüsselwort `Keywords_spain_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="b0749-767">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-767">Keywords</span></span>

<span data-ttu-id="b0749-768">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-768"></span></span>
|<span data-ttu-id="b0749-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-770">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-770">dlno#</span></span>  <br/> <span data-ttu-id="b0749-771">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-771">dl#</span></span>  <br/> <span data-ttu-id="b0749-772">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-772">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-773">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-773">driver licence</span></span>  <br/> <span data-ttu-id="b0749-774">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-774">driver license</span></span>  <br/> <span data-ttu-id="b0749-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-775">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-776">drivers license</span></span>  <br/> <span data-ttu-id="b0749-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="b0749-777">driver's licence</span></span>  <br/> <span data-ttu-id="b0749-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-778">driver's license</span></span>  <br/> <span data-ttu-id="b0749-779">Führerschein</span><span class="sxs-lookup"><span data-stu-id="b0749-779">driving licence</span></span>  <br/> <span data-ttu-id="b0749-780">driving license</span><span class="sxs-lookup"><span data-stu-id="b0749-780">driving license</span></span>  <br/> <span data-ttu-id="b0749-781">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-781">driver licence number</span></span>  <br/> <span data-ttu-id="b0749-782">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-782">driver license number</span></span>  <br/> <span data-ttu-id="b0749-783">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-783">drivers licence number</span></span>  <br/> <span data-ttu-id="b0749-784">Lizenznummer für Treiber</span><span class="sxs-lookup"><span data-stu-id="b0749-784">drivers license number</span></span>  <br/> <span data-ttu-id="b0749-785">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-785">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-786">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-786">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-787">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-787">driving licence number</span></span>  <br/> <span data-ttu-id="b0749-788">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-788">driving license number</span></span>  <br/> <span data-ttu-id="b0749-789">Führerschein</span><span class="sxs-lookup"><span data-stu-id="b0749-789">driving permit</span></span>  <br/> <span data-ttu-id="b0749-790">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-790">driving permit number</span></span>  <br/> <span data-ttu-id="b0749-791">Permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="b0749-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="b0749-792">permiso conducción</span><span class="sxs-lookup"><span data-stu-id="b0749-792">permiso conducción</span></span>  <br/> <span data-ttu-id="b0749-793">número licencia Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="b0749-794">número de carnet de Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="b0749-795">número Carnet Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="b0749-796">licencia Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-796">licencia conducir</span></span>  <br/> <span data-ttu-id="b0749-797">número de Permiso de Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="b0749-798">número de Permiso Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="b0749-799">número Permiso Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="b0749-800">Permiso Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-800">permiso conducir</span></span>  <br/> <span data-ttu-id="b0749-801">licencia de Manejo</span><span class="sxs-lookup"><span data-stu-id="b0749-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="b0749-802">El Carnet de Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="b0749-803">Carnet Conducir</span><span class="sxs-lookup"><span data-stu-id="b0749-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="b0749-804">Schweden</span><span class="sxs-lookup"><span data-stu-id="b0749-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="b0749-805">Format</span><span class="sxs-lookup"><span data-stu-id="b0749-805">Format</span></span>

<span data-ttu-id="b0749-806">Zehn Ziffern mit einem Bindestrich</span><span class="sxs-lookup"><span data-stu-id="b0749-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="b0749-807">Muster</span><span class="sxs-lookup"><span data-stu-id="b0749-807">Pattern</span></span>

<span data-ttu-id="b0749-808">Zehn Ziffern mit einem Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="b0749-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="b0749-809">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-809">Six digits</span></span> 
    
- <span data-ttu-id="b0749-810">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="b0749-810">A hyphen</span></span>
    
- <span data-ttu-id="b0749-811">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="b0749-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="b0749-812">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="b0749-812">Checksum</span></span>

<span data-ttu-id="b0749-813">Nein</span><span class="sxs-lookup"><span data-stu-id="b0749-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="b0749-814">Definition</span><span class="sxs-lookup"><span data-stu-id="b0749-814">Definition</span></span>

<span data-ttu-id="b0749-815">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="b0749-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="b0749-816">Der reguläre Ausdruck `Regex_sweden_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="b0749-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="b0749-817">Ein Schlüsselwort `Keywords_sweden_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="b0749-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="b0749-818">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="b0749-818">Keywords</span></span>

<span data-ttu-id="b0749-819">| |</span><span class="sxs-lookup"><span data-stu-id="b0749-819"></span></span>
|<span data-ttu-id="b0749-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="b0749-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="b0749-821">DL</span><span class="sxs-lookup"><span data-stu-id="b0749-821">dl#</span></span>  <br/> <span data-ttu-id="b0749-822">driver license</span><span class="sxs-lookup"><span data-stu-id="b0749-822">driver license</span></span>  <br/> <span data-ttu-id="b0749-823">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="b0749-823">driver license number</span></span>  <br/> <span data-ttu-id="b0749-824">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="b0749-824">driver licence</span></span>  <br/> <span data-ttu-id="b0749-825">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="b0749-825">drivers lic.</span></span>  <br/> <span data-ttu-id="b0749-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="b0749-826">drivers license</span></span>  <br/> <span data-ttu-id="b0749-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="b0749-827">drivers licence</span></span>  <br/> <span data-ttu-id="b0749-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="b0749-828">driver's license</span></span>  <br/> <span data-ttu-id="b0749-829">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-829">driver's license number</span></span>  <br/> <span data-ttu-id="b0749-830">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-830">driver's licence number</span></span>  <br/> <span data-ttu-id="b0749-831">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="b0749-831">driving license number</span></span>  <br/> <span data-ttu-id="b0749-832">dlno#</span><span class="sxs-lookup"><span data-stu-id="b0749-832">dlno#</span></span>  <br/> <span data-ttu-id="b0749-833">körkort</span><span class="sxs-lookup"><span data-stu-id="b0749-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="b0749-834">UK</span><span class="sxs-lookup"><span data-stu-id="b0749-834">UK</span></span>

<span data-ttu-id="b0749-835">Ausführliche Informationen finden Sie im Abschnitt "U.K.</span><span class="sxs-lookup"><span data-stu-id="b0749-835">For details, see the section "U.K.</span></span> <span data-ttu-id="b0749-836">Nummer des Führerscheins "in [dem, wonach die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="b0749-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b0749-837">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0749-837">See also</span></span>

[<span data-ttu-id="b0749-838">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="b0749-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

