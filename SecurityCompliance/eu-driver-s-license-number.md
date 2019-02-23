---
title: EU-Führerscheinnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: c3923cd3-ec84-435f-bf41-cadc37996a4b
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Treiber Lizenznummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 86be7b52aed7581fd62ab595ac2c4b63ab33aab3
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30217745"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="a37f7-104">EU-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-104">EU Driver's License Number</span></span>

<span data-ttu-id="a37f7-p102">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Treiber Lizenznummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="a37f7-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="a37f7-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="a37f7-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-108">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-108">Format</span></span>

<span data-ttu-id="a37f7-109">Acht Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-110">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-110">Pattern</span></span>

<span data-ttu-id="a37f7-111">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a37f7-112">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-112">Checksum</span></span>

<span data-ttu-id="a37f7-113">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-114">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-114">Definition</span></span>

<span data-ttu-id="a37f7-115">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-116">Der reguläre Ausdruck `Regex_austria_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-117">Ein Schlüsselwort `Keywords_austria_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="a37f7-118">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-118">Keywords</span></span>

<span data-ttu-id="a37f7-119">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-119"></span></span>
|<span data-ttu-id="a37f7-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-121">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-121">dl#</span></span>  <br/> <span data-ttu-id="a37f7-122">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-122">driver license</span></span>  <br/> <span data-ttu-id="a37f7-123">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-123">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-124">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-124">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-125">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-125">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-126">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-127">Führerschein</span><span class="sxs-lookup"><span data-stu-id="a37f7-127">driver's licence</span></span>  <br/> <span data-ttu-id="a37f7-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-128">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-129">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-129">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-130">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="a37f7-131">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-131">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-132">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-133">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="a37f7-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="a37f7-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="a37f7-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="a37f7-135">Belgien</span><span class="sxs-lookup"><span data-stu-id="a37f7-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-136">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-136">Format</span></span>

<span data-ttu-id="a37f7-137">10 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-138">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-138">Pattern</span></span>

<span data-ttu-id="a37f7-139">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a37f7-140">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-140">Checksum</span></span>

<span data-ttu-id="a37f7-141">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-142">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-142">Definition</span></span>

<span data-ttu-id="a37f7-143">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-144">Der reguläre Ausdruck `Regex_belgium_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-145">Ein Schlüsselwort `Keywords_belgium_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a37f7-146">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-146">Keywords</span></span>

<span data-ttu-id="a37f7-147">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-147"></span></span>
|<span data-ttu-id="a37f7-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-149">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-149">dl#</span></span>  <br/> <span data-ttu-id="a37f7-150">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-150">driver license</span></span>  <br/> <span data-ttu-id="a37f7-151">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-151">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-152">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-152">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-153">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-153">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-154">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-155">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-156">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-157">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-157">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-158">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-158">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-159">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="a37f7-160">rijbewijs</span></span>  <br/> <span data-ttu-id="a37f7-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="a37f7-162">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="a37f7-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="a37f7-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="a37f7-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="a37f7-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="a37f7-166">Fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="a37f7-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="a37f7-167">Fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="a37f7-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="a37f7-168">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="a37f7-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-169">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-169">Format</span></span>

<span data-ttu-id="a37f7-170">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-171">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-171">Pattern</span></span>

<span data-ttu-id="a37f7-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a37f7-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-173">Checksum</span></span>

<span data-ttu-id="a37f7-174">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-175">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-175">Definition</span></span>

<span data-ttu-id="a37f7-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-177">Der reguläre Ausdruck `Regex_bulgaria_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-178">Ein Schlüsselwort `Keywords_bulgaria_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="a37f7-179">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-179">Keywords</span></span>

<span data-ttu-id="a37f7-180">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-180"></span></span>
|<span data-ttu-id="a37f7-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-182">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-182">dl#</span></span>  <br/> <span data-ttu-id="a37f7-183">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-183">driver license</span></span>  <br/> <span data-ttu-id="a37f7-184">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-184">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-185">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-185">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-186">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-186">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-187">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-188">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-189">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-190">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-190">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-191">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-191">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-192">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-192">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-193">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="a37f7-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="a37f7-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="a37f7-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="a37f7-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="a37f7-196">сумпс</span></span>  <br/> <span data-ttu-id="a37f7-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="a37f7-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="a37f7-198">Kroatien</span><span class="sxs-lookup"><span data-stu-id="a37f7-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-199">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-199">Format</span></span>

<span data-ttu-id="a37f7-200">Acht Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-201">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-201">Pattern</span></span>

<span data-ttu-id="a37f7-202">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a37f7-203">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-203">Checksum</span></span>

<span data-ttu-id="a37f7-204">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-205">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-205">Definition</span></span>

<span data-ttu-id="a37f7-206">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-207">Der reguläre Ausdruck `Regex_croatia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-208">Ein Schlüsselwort `Keywords_croatia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a37f7-209">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-209">Keywords</span></span>

<span data-ttu-id="a37f7-210">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-210"></span></span>
|<span data-ttu-id="a37f7-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-212">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-212">dl#</span></span>  <br/> <span data-ttu-id="a37f7-213">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-213">driver license</span></span>  <br/> <span data-ttu-id="a37f7-214">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-214">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-215">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-215">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-216">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-216">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-217">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-218">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-219">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-220">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-220">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-221">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-221">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-222">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-222">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-223">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="a37f7-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="a37f7-225">Zypern</span><span class="sxs-lookup"><span data-stu-id="a37f7-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-226">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-226">Format</span></span>

<span data-ttu-id="a37f7-227">12 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-228">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-228">Pattern</span></span>

<span data-ttu-id="a37f7-229">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a37f7-230">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-230">Checksum</span></span>

<span data-ttu-id="a37f7-231">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-232">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-232">Definition</span></span>

<span data-ttu-id="a37f7-233">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-234">Der reguläre Ausdruck `Regex_cyprus_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-235">Ein Schlüsselwort `Keywords_cyprus_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-236">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-236">Keywords</span></span>

<span data-ttu-id="a37f7-237">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-237"></span></span>
|<span data-ttu-id="a37f7-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-239">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-239">dl#</span></span>  <br/> <span data-ttu-id="a37f7-240">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-240">driver license</span></span>  <br/> <span data-ttu-id="a37f7-241">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-241">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-242">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-242">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-243">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-243">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-244">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-245">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-246">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-246">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-247">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-247">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-248">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-248">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-249">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="a37f7-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="a37f7-251">Tschechien</span><span class="sxs-lookup"><span data-stu-id="a37f7-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-252">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-252">Format</span></span>

<span data-ttu-id="a37f7-253">Zwei Buchstaben gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-254">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-254">Pattern</span></span>

<span data-ttu-id="a37f7-255">Acht Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="a37f7-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="a37f7-256">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="a37f7-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="a37f7-257">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="a37f7-257">A space (optional)</span></span>
    
- <span data-ttu-id="a37f7-258">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-259">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-259">Checksum</span></span>

<span data-ttu-id="a37f7-260">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-261">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-261">Definition</span></span>

<span data-ttu-id="a37f7-262">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-263">Der reguläre Ausdruck `Regex_czech_republic_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-264">Ein Schlüsselwort `Keywords_czech_republic_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a37f7-265">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-265">Keywords</span></span>

<span data-ttu-id="a37f7-266">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-266"></span></span>
|<span data-ttu-id="a37f7-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-268">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-268">dl#</span></span>  <br/> <span data-ttu-id="a37f7-269">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-269">driver license</span></span>  <br/> <span data-ttu-id="a37f7-270">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-270">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-271">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-271">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-272">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-272">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-273">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-274">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-275">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-276">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-276">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-277">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-277">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-278">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-278">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-279">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-279">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-280">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="a37f7-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="a37f7-282">Dänemark</span><span class="sxs-lookup"><span data-stu-id="a37f7-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-283">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-283">Format</span></span>

<span data-ttu-id="a37f7-284">Acht Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-285">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-285">Pattern</span></span>

<span data-ttu-id="a37f7-286">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a37f7-287">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-287">Checksum</span></span>

<span data-ttu-id="a37f7-288">Ja</span><span class="sxs-lookup"><span data-stu-id="a37f7-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-289">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-289">Definition</span></span>

<span data-ttu-id="a37f7-290">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-291">Der reguläre Ausdruck `Regex_denmark_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-292">Ein Schlüsselwort `Keywords_denmark_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="a37f7-293">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-293">Keywords</span></span>

<span data-ttu-id="a37f7-294">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-294"></span></span>
|<span data-ttu-id="a37f7-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-296">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-296">dl#</span></span>  <br/> <span data-ttu-id="a37f7-297">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-297">driver license</span></span>  <br/> <span data-ttu-id="a37f7-298">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-298">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-299">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-299">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-300">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-300">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-301">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-302">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-303">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-304">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-304">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-305">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-305">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-306">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-306">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-307">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="a37f7-308">kørekort</span></span>  <br/> <span data-ttu-id="a37f7-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="a37f7-310">Estland</span><span class="sxs-lookup"><span data-stu-id="a37f7-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-311">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-311">Format</span></span>

<span data-ttu-id="a37f7-312">Zwei Buchstaben gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-313">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-313">Pattern</span></span>

<span data-ttu-id="a37f7-314">Zwei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="a37f7-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a37f7-315">Die Buchstaben "ET" (Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="a37f7-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a37f7-316">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-317">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-317">Checksum</span></span>

<span data-ttu-id="a37f7-318">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-319">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-319">Definition</span></span>

<span data-ttu-id="a37f7-320">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-321">Der reguläre Ausdruck `Regex_estonia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-322">Ein Schlüsselwort `Keywords_estonia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-323">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-323">Keywords</span></span>

<span data-ttu-id="a37f7-324">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-324"></span></span>
|<span data-ttu-id="a37f7-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-326">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-326">dl#</span></span>  <br/> <span data-ttu-id="a37f7-327">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-327">driver license</span></span>  <br/> <span data-ttu-id="a37f7-328">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-328">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-329">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-329">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-330">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-330">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-331">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-331">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-332">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-333">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-334">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-335">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-335">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-336">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-336">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-337">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-338">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a37f7-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="a37f7-339">Finnland</span><span class="sxs-lookup"><span data-stu-id="a37f7-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-340">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-340">Format</span></span>

<span data-ttu-id="a37f7-341">10 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="a37f7-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-342">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-342">Pattern</span></span>

<span data-ttu-id="a37f7-343">10 Ziffern mit einem Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="a37f7-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a37f7-344">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-344">Six digits</span></span> 
    
- <span data-ttu-id="a37f7-345">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="a37f7-345">A hyphen</span></span>
    
-  <span data-ttu-id="a37f7-346">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a37f7-347">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-347">Checksum</span></span>

<span data-ttu-id="a37f7-348">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-349">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-349">Definition</span></span>

<span data-ttu-id="a37f7-350">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-351">Der reguläre Ausdruck `Regex_finland_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-352">Ein Schlüsselwort `Keywords_finland_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-353">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-353">Keywords</span></span>

<span data-ttu-id="a37f7-354">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-354"></span></span>
|<span data-ttu-id="a37f7-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-356">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-356">dl#</span></span>  <br/> <span data-ttu-id="a37f7-357">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-357">driver license</span></span>  <br/> <span data-ttu-id="a37f7-358">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-358">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-359">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-359">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-360">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-360">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-361">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-362">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-363">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-364">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-364">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-365">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-365">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-366">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-366">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-367">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="a37f7-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="a37f7-369">Frankreich</span><span class="sxs-lookup"><span data-stu-id="a37f7-369">France</span></span>

<span data-ttu-id="a37f7-370">Weitere Informationen finden Sie im Abschnitt "Frankreich Driver es License Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a37f7-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="a37f7-371">Deutschland</span><span class="sxs-lookup"><span data-stu-id="a37f7-371">Germany</span></span>

<span data-ttu-id="a37f7-372">Weitere Informationen finden Sie im Abschnitt "German Driver es License Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a37f7-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="a37f7-373">Griechenland</span><span class="sxs-lookup"><span data-stu-id="a37f7-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-374">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-374">Format</span></span>

<span data-ttu-id="a37f7-375">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-376">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-376">Pattern</span></span>

 <span data-ttu-id="a37f7-377">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a37f7-378">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-378">Checksum</span></span>

<span data-ttu-id="a37f7-379">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-380">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-380">Definition</span></span>

<span data-ttu-id="a37f7-381">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-382">Der reguläre Ausdruck `Regex_greece_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-383">Ein Schlüsselwort `Keywords_greece_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-384">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-384">Keywords</span></span>

<span data-ttu-id="a37f7-385">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-385"></span></span>
|<span data-ttu-id="a37f7-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-387">DlL</span><span class="sxs-lookup"><span data-stu-id="a37f7-387">dlL#</span></span>  <br/> <span data-ttu-id="a37f7-388">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-388">driver license</span></span>  <br/> <span data-ttu-id="a37f7-389">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-389">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-390">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-390">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-391">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-391">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-392">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-393">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-394">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-395">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-395">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-396">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-396">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-397">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-397">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-398">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="a37f7-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="a37f7-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="a37f7-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="a37f7-401">Ungarn</span><span class="sxs-lookup"><span data-stu-id="a37f7-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-402">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-402">Format</span></span>

<span data-ttu-id="a37f7-403">Zwei Buchstaben gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-404">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-404">Pattern</span></span>

<span data-ttu-id="a37f7-405">Zwei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="a37f7-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="a37f7-406">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="a37f7-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a37f7-407">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-408">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-408">Checksum</span></span>

<span data-ttu-id="a37f7-409">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-410">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-410">Definition</span></span>

<span data-ttu-id="a37f7-411">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-412">Der reguläre Ausdruck `Regex_hungary_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-413">Ein Schlüsselwort `Keywords_hungary_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-414">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-414">Keywords</span></span>

<span data-ttu-id="a37f7-415">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-415"></span></span>
|<span data-ttu-id="a37f7-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-417">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-417">dl#</span></span>  <br/> <span data-ttu-id="a37f7-418">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-418">driver license</span></span>  <br/> <span data-ttu-id="a37f7-419">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-419">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-420">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-420">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-421">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-421">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-422">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-423">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-424">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-425">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-425">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-426">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-426">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-427">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-427">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-428">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="a37f7-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="a37f7-430">Irland</span><span class="sxs-lookup"><span data-stu-id="a37f7-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-431">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-431">Format</span></span>

<span data-ttu-id="a37f7-432">Sechs Ziffern gefolgt von vier Buchstaben</span><span class="sxs-lookup"><span data-stu-id="a37f7-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-433">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-433">Pattern</span></span>

<span data-ttu-id="a37f7-434">Sechs Ziffern und vier Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="a37f7-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="a37f7-435">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-435">Six digits</span></span>
    
- <span data-ttu-id="a37f7-436">Vier Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="a37f7-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-437">Checksum</span></span>

<span data-ttu-id="a37f7-438">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-439">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-439">Definition</span></span>

<span data-ttu-id="a37f7-440">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-441">Der reguläre Ausdruck `Regex_ireland_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-442">Ein Schlüsselwort `Keywords_ireland_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-443">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-443">Keywords</span></span>

<span data-ttu-id="a37f7-444">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-444"></span></span>
|<span data-ttu-id="a37f7-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-446">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-446">dl#</span></span>  <br/> <span data-ttu-id="a37f7-447">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-447">driver license</span></span>  <br/> <span data-ttu-id="a37f7-448">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-448">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-449">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-449">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-450">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-450">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-451">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-452">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-453">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-454">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-454">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-455">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-455">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-456">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-456">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-457">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-458">Ceadúnas Tiomána</span><span class="sxs-lookup"><span data-stu-id="a37f7-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="a37f7-459">Italien</span><span class="sxs-lookup"><span data-stu-id="a37f7-459">Italy</span></span>

<span data-ttu-id="a37f7-460">Weitere Informationen finden Sie im Abschnitt "Italy Driver es License Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a37f7-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="a37f7-461">Lettland</span><span class="sxs-lookup"><span data-stu-id="a37f7-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-462">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-462">Format</span></span>

<span data-ttu-id="a37f7-463">Drei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-464">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-464">Pattern</span></span>

<span data-ttu-id="a37f7-465">Drei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="a37f7-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="a37f7-466">Drei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="a37f7-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a37f7-467">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-468">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-468">Checksum</span></span>

<span data-ttu-id="a37f7-469">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-470">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-470">Definition</span></span>

<span data-ttu-id="a37f7-471">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-472">Der reguläre Ausdruck `Regex_latvia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-473">Ein Schlüsselwort `Keywords_latvia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-474">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-474">Keywords</span></span>

<span data-ttu-id="a37f7-475">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-475"></span></span>
|<span data-ttu-id="a37f7-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-477">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-477">dl#</span></span>  <br/> <span data-ttu-id="a37f7-478">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-478">driver license</span></span>  <br/> <span data-ttu-id="a37f7-479">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-479">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-480">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-480">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-481">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-481">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-482">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-483">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-484">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-485">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-485">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-486">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-486">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-487">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-487">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-488">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="a37f7-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="a37f7-490">Litauen</span><span class="sxs-lookup"><span data-stu-id="a37f7-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-491">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-491">Format</span></span>

<span data-ttu-id="a37f7-492">Acht Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-493">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-493">Pattern</span></span>

 <span data-ttu-id="a37f7-494">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a37f7-495">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-495">Checksum</span></span>

<span data-ttu-id="a37f7-496">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-497">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-497">Definition</span></span>

<span data-ttu-id="a37f7-498">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-499">Der reguläre Ausdruck `Regex_lithuania_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-500">Ein Schlüsselwort `Keywords_lithuania_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-501">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-501">Keywords</span></span>

<span data-ttu-id="a37f7-502">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-502"></span></span>
|<span data-ttu-id="a37f7-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-504">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-504">dl#</span></span>  <br/> <span data-ttu-id="a37f7-505">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-505">driver license</span></span>  <br/> <span data-ttu-id="a37f7-506">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-506">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-507">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-507">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-508">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-508">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-509">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-510">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-511">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-512">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-512">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-513">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-513">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-514">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-514">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-515">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-516">Vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="a37f7-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="a37f7-517">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="a37f7-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-518">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-518">Format</span></span>

<span data-ttu-id="a37f7-519">Sechs Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-520">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-520">Pattern</span></span>

 <span data-ttu-id="a37f7-521">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="a37f7-522">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-522">Checksum</span></span>

<span data-ttu-id="a37f7-523">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-524">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-524">Definition</span></span>

<span data-ttu-id="a37f7-525">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-526">Der reguläre Ausdruck `Regex_luxemburg_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-527">Ein Schlüsselwort `Keywords_luxemburg_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-528">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-528">Keywords</span></span>

<span data-ttu-id="a37f7-529">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-529"></span></span>
|<span data-ttu-id="a37f7-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-531">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-531">dl#</span></span>  <br/> <span data-ttu-id="a37f7-532">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-532">driver license</span></span>  <br/> <span data-ttu-id="a37f7-533">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-533">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-534">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-534">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-535">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-535">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-536">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-537">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-538">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-539">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-539">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-540">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-540">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-541">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-541">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-542">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-543">Fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="a37f7-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="a37f7-544">Malta</span><span class="sxs-lookup"><span data-stu-id="a37f7-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-545">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-545">Format</span></span>

<span data-ttu-id="a37f7-546">Kombination aus zwei Zeichen und sechs Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-547">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-547">Pattern</span></span>

<span data-ttu-id="a37f7-548">Kombination aus zwei Zeichen und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="a37f7-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="a37f7-549">Zwei Zeichen (Ziffern oder Buchstaben, keine Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="a37f7-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="a37f7-550">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="a37f7-550">A space (optional)</span></span>
    
- <span data-ttu-id="a37f7-551">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-551">Three digits</span></span>
    
- <span data-ttu-id="a37f7-552">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="a37f7-552">A space (optional)</span></span>
    
- <span data-ttu-id="a37f7-553">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-554">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-554">Checksum</span></span>

<span data-ttu-id="a37f7-555">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-556">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-556">Definition</span></span>

<span data-ttu-id="a37f7-557">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-558">Der reguläre Ausdruck `Regex_malta_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-559">Ein Schlüsselwort `Keywords_malta_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-560">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-560">Keywords</span></span>

<span data-ttu-id="a37f7-561">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-561"></span></span>
|<span data-ttu-id="a37f7-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-563">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-563">dl#</span></span>  <br/> <span data-ttu-id="a37f7-564">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-564">driver license</span></span>  <br/> <span data-ttu-id="a37f7-565">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-565">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-566">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-566">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-567">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-567">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-568">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-569">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-570">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-571">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-571">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-572">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-572">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-573">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-573">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-574">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-575">Liċenzja TAS-Sewqan</span><span class="sxs-lookup"><span data-stu-id="a37f7-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="a37f7-576">Niederlande</span><span class="sxs-lookup"><span data-stu-id="a37f7-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-577">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-577">Format</span></span>

<span data-ttu-id="a37f7-578">10 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-579">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-579">Pattern</span></span>

<span data-ttu-id="a37f7-580">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a37f7-581">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-581">Checksum</span></span>

<span data-ttu-id="a37f7-582">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-583">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-583">Definition</span></span>

<span data-ttu-id="a37f7-584">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-585">Der reguläre Ausdruck `Regex_netherlands_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-586">Ein Schlüsselwort `Keywords_netherlands_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-587">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-587">Keywords</span></span>

<span data-ttu-id="a37f7-588">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-588"></span></span>
|<span data-ttu-id="a37f7-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-590">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-590">dl#</span></span>  <br/> <span data-ttu-id="a37f7-591">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-591">driver license</span></span>  <br/> <span data-ttu-id="a37f7-592">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-592">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-593">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-593">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-594">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-594">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-595">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-596">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-597">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-598">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-598">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-599">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-599">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-600">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-600">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-601">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-602">
permis de conduire</span><span class="sxs-lookup"><span data-stu-id="a37f7-602">permis de conduire</span></span>  <br/> <span data-ttu-id="a37f7-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="a37f7-603">rijbewijs</span></span>  <br/> <span data-ttu-id="a37f7-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="a37f7-605">Polen</span><span class="sxs-lookup"><span data-stu-id="a37f7-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-606">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-606">Format</span></span>

<span data-ttu-id="a37f7-607">14 Ziffern mit 2 Schrägstrichen</span><span class="sxs-lookup"><span data-stu-id="a37f7-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-608">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-608">Pattern</span></span>

<span data-ttu-id="a37f7-609">14 Ziffern und 2 Schrägstriche:</span><span class="sxs-lookup"><span data-stu-id="a37f7-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="a37f7-610">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-610">Five digits</span></span> 
    
- <span data-ttu-id="a37f7-611">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="a37f7-611">A forward slash</span></span>
    
- <span data-ttu-id="a37f7-612">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-612">Two digits</span></span>
    
- <span data-ttu-id="a37f7-613">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="a37f7-613">A forward slash</span></span>
    
- <span data-ttu-id="a37f7-614">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-615">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-615">Checksum</span></span>

<span data-ttu-id="a37f7-616">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-617">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-617">Definition</span></span>

<span data-ttu-id="a37f7-618">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-619">Der reguläre Ausdruck `Regex_poland_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-620">Ein Schlüsselwort `Keywords_poland_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-621">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-621">Keywords</span></span>

<span data-ttu-id="a37f7-622">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-622"></span></span>
|<span data-ttu-id="a37f7-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-624">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-624">dl#</span></span>  <br/> <span data-ttu-id="a37f7-625">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-625">driver license</span></span>  <br/> <span data-ttu-id="a37f7-626">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-626">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-627">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-627">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-628">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-628">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-629">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-630">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-631">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-632">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-632">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-633">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-633">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-634">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-634">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-635">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="a37f7-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="a37f7-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="a37f7-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-638">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-638">Format</span></span>

<span data-ttu-id="a37f7-639">Zwei Buchstaben gefolgt von sieben Zahlen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-640">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-640">Pattern</span></span>

<span data-ttu-id="a37f7-641">Zwei Buchstaben gefolgt von sieben Zahlen mit Sonderzeichen:</span><span class="sxs-lookup"><span data-stu-id="a37f7-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="a37f7-642">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="a37f7-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="a37f7-643">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="a37f7-643">A hyphen</span></span>
    
- <span data-ttu-id="a37f7-644">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-644">Six digits</span></span>
    
- <span data-ttu-id="a37f7-645">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="a37f7-645">A space</span></span>
    
- <span data-ttu-id="a37f7-646">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="a37f7-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-647">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-647">Checksum</span></span>

<span data-ttu-id="a37f7-648">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-649">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-649">Definition</span></span>

<span data-ttu-id="a37f7-650">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-651">Der reguläre Ausdruck `Regex_portugal_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-652">Ein Schlüsselwort `Keywords_portugal_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-653">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-653">Keywords</span></span>

<span data-ttu-id="a37f7-654">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-654"></span></span>
|<span data-ttu-id="a37f7-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-656">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-656">dl#</span></span>  <br/> <span data-ttu-id="a37f7-657">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-657">driver license</span></span>  <br/> <span data-ttu-id="a37f7-658">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-658">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-659">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-659">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-660">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-660">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-661">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-662">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-663">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-664">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-664">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-665">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-665">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-666">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-666">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-667">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="a37f7-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="a37f7-669">Rumänien</span><span class="sxs-lookup"><span data-stu-id="a37f7-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-670">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-670">Format</span></span>

<span data-ttu-id="a37f7-671">Ein Zeichen, gefolgt von acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-672">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-672">Pattern</span></span>

<span data-ttu-id="a37f7-673">Ein Zeichen, gefolgt von acht Ziffern:</span><span class="sxs-lookup"><span data-stu-id="a37f7-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="a37f7-674">Ein Buchstabe (ohne Unterscheidung von Groß-/Kleinschreibung) oder Ziffer</span><span class="sxs-lookup"><span data-stu-id="a37f7-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="a37f7-675">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-676">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-676">Checksum</span></span>

<span data-ttu-id="a37f7-677">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-678">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-678">Definition</span></span>

<span data-ttu-id="a37f7-679">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-680">Der reguläre Ausdruck `Regex_romania_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-681">Ein Schlüsselwort `Keywords_romania_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-682">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-682">Keywords</span></span>

<span data-ttu-id="a37f7-683">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-683"></span></span>
|<span data-ttu-id="a37f7-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-685">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-685">dl#</span></span>  <br/> <span data-ttu-id="a37f7-686">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-686">driver license</span></span>  <br/> <span data-ttu-id="a37f7-687">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-687">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-688">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-688">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-689">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-689">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-690">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-691">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-692">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-693">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-693">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-694">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-694">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-695">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-695">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-696">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="a37f7-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="a37f7-698">Slowakei</span><span class="sxs-lookup"><span data-stu-id="a37f7-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-699">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-699">Format</span></span>

<span data-ttu-id="a37f7-700">Ein Zeichen, gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-701">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-701">Pattern</span></span>

<span data-ttu-id="a37f7-702">Ein Zeichen, gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="a37f7-703">Ein Buchstabe (ohne Unterscheidung von Groß-/Kleinschreibung) oder Ziffer</span><span class="sxs-lookup"><span data-stu-id="a37f7-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="a37f7-704">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="a37f7-705">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-705">Checksum</span></span>

<span data-ttu-id="a37f7-706">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-707">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-707">Definition</span></span>

<span data-ttu-id="a37f7-708">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-709">Der reguläre Ausdruck `Regex_slovakia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-710">Ein Schlüsselwort `Keywords_slovakia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-711">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-711">Keywords</span></span>

<span data-ttu-id="a37f7-712">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-712"></span></span>
|<span data-ttu-id="a37f7-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-714">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-714">dl#</span></span>  <br/> <span data-ttu-id="a37f7-715">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-715">driver license</span></span>  <br/> <span data-ttu-id="a37f7-716">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-716">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-717">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-717">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-718">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-718">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-719">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-720">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-721">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-722">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-722">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-723">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-723">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-724">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-724">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-725">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="a37f7-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="a37f7-727">Slowenien</span><span class="sxs-lookup"><span data-stu-id="a37f7-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-728">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-728">Format</span></span>

<span data-ttu-id="a37f7-729">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="a37f7-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-730">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-730">Pattern</span></span>

<span data-ttu-id="a37f7-731">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="a37f7-732">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-732">Checksum</span></span>

<span data-ttu-id="a37f7-733">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-734">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-734">Definition</span></span>

<span data-ttu-id="a37f7-735">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-736">Der reguläre Ausdruck `Regex_slovenia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-737">Ein Schlüsselwort `Keywords_slovenia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-738">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-738">Keywords</span></span>

<span data-ttu-id="a37f7-739">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-739"></span></span>
|<span data-ttu-id="a37f7-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-741">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-741">dl#</span></span>  <br/> <span data-ttu-id="a37f7-742">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-742">driver license</span></span>  <br/> <span data-ttu-id="a37f7-743">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-743">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-744">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-744">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-745">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-745">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-746">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-747">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-748">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-749">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-749">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-750">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-750">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-751">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-751">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-752">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-753">vozniško Dovoljenje</span><span class="sxs-lookup"><span data-stu-id="a37f7-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="a37f7-754">Spanien</span><span class="sxs-lookup"><span data-stu-id="a37f7-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-755">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-755">Format</span></span>

<span data-ttu-id="a37f7-756">Acht Ziffern gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="a37f7-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-757">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-757">Pattern</span></span>

<span data-ttu-id="a37f7-758">Acht Ziffern gefolgt von einem Zeichen:</span><span class="sxs-lookup"><span data-stu-id="a37f7-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="a37f7-759">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-759">Eight digits</span></span> 
    
- <span data-ttu-id="a37f7-760">Eine Ziffer oder ein Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="a37f7-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-761">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-761">Checksum</span></span>

<span data-ttu-id="a37f7-762">Ja</span><span class="sxs-lookup"><span data-stu-id="a37f7-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-763">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-763">Definition</span></span>

<span data-ttu-id="a37f7-764">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-765">Die Funktion `Func_spain_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-766">Ein Schlüsselwort `Keywords_spain_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="a37f7-767">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-767">Keywords</span></span>

<span data-ttu-id="a37f7-768">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-768"></span></span>
|<span data-ttu-id="a37f7-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-770">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-771">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-771">dl#</span></span>  <br/> <span data-ttu-id="a37f7-772">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-772">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-773">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-773">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-774">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-774">driver license</span></span>  <br/> <span data-ttu-id="a37f7-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-775">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-776">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-777">Führerschein</span><span class="sxs-lookup"><span data-stu-id="a37f7-777">driver's licence</span></span>  <br/> <span data-ttu-id="a37f7-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-778">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-779">driving licence
</span><span class="sxs-lookup"><span data-stu-id="a37f7-779">driving licence</span></span>  <br/> <span data-ttu-id="a37f7-780">Führerschein</span><span class="sxs-lookup"><span data-stu-id="a37f7-780">driving license</span></span>  <br/> <span data-ttu-id="a37f7-781">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-781">driver licence number</span></span>  <br/> <span data-ttu-id="a37f7-782">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-782">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-783">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-783">drivers licence number</span></span>  <br/> <span data-ttu-id="a37f7-784">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-784">drivers license number</span></span>  <br/> <span data-ttu-id="a37f7-785">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-785">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-786">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-786">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-787">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-787">driving licence number</span></span>  <br/> <span data-ttu-id="a37f7-788">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-788">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-789">Fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="a37f7-789">driving permit</span></span>  <br/> <span data-ttu-id="a37f7-790">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-790">driving permit number</span></span>  <br/> <span data-ttu-id="a37f7-791">Permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="a37f7-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="a37f7-792">Permiso conducción</span><span class="sxs-lookup"><span data-stu-id="a37f7-792">permiso conducción</span></span>  <br/> <span data-ttu-id="a37f7-793">número licencia Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="a37f7-794">número de carnet de Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="a37f7-795">número Carnet Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="a37f7-796">licencia Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-796">licencia conducir</span></span>  <br/> <span data-ttu-id="a37f7-797">número de Permiso de Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="a37f7-798">número de Permiso Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="a37f7-799">número Permiso Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="a37f7-800">Permiso Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-800">permiso conducir</span></span>  <br/> <span data-ttu-id="a37f7-801">licencia de Manejo</span><span class="sxs-lookup"><span data-stu-id="a37f7-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="a37f7-802">El Carnet de Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="a37f7-803">Carnet Conducir</span><span class="sxs-lookup"><span data-stu-id="a37f7-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="a37f7-804">Schweden</span><span class="sxs-lookup"><span data-stu-id="a37f7-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="a37f7-805">Format</span><span class="sxs-lookup"><span data-stu-id="a37f7-805">Format</span></span>

<span data-ttu-id="a37f7-806">Zehn Ziffern mit einem Bindestrich</span><span class="sxs-lookup"><span data-stu-id="a37f7-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="a37f7-807">Muster</span><span class="sxs-lookup"><span data-stu-id="a37f7-807">Pattern</span></span>

<span data-ttu-id="a37f7-808">Zehn Ziffern mit einem Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="a37f7-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="a37f7-809">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-809">Six digits</span></span> 
    
- <span data-ttu-id="a37f7-810">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="a37f7-810">A hyphen</span></span>
    
- <span data-ttu-id="a37f7-811">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="a37f7-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="a37f7-812">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="a37f7-812">Checksum</span></span>

<span data-ttu-id="a37f7-813">Nein</span><span class="sxs-lookup"><span data-stu-id="a37f7-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="a37f7-814">Definition</span><span class="sxs-lookup"><span data-stu-id="a37f7-814">Definition</span></span>

<span data-ttu-id="a37f7-815">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="a37f7-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="a37f7-816">Der reguläre Ausdruck `Regex_sweden_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="a37f7-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="a37f7-817">Ein Schlüsselwort `Keywords_sweden_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="a37f7-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="a37f7-818">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="a37f7-818">Keywords</span></span>

<span data-ttu-id="a37f7-819">| |</span><span class="sxs-lookup"><span data-stu-id="a37f7-819"></span></span>
|<span data-ttu-id="a37f7-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="a37f7-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="a37f7-821">dl#</span><span class="sxs-lookup"><span data-stu-id="a37f7-821">dl#</span></span>  <br/> <span data-ttu-id="a37f7-822">driver license</span><span class="sxs-lookup"><span data-stu-id="a37f7-822">driver license</span></span>  <br/> <span data-ttu-id="a37f7-823">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-823">driver license number</span></span>  <br/> <span data-ttu-id="a37f7-824">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="a37f7-824">driver licence</span></span>  <br/> <span data-ttu-id="a37f7-825">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="a37f7-825">drivers lic.</span></span>  <br/> <span data-ttu-id="a37f7-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="a37f7-826">drivers license</span></span>  <br/> <span data-ttu-id="a37f7-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="a37f7-827">drivers licence</span></span>  <br/> <span data-ttu-id="a37f7-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="a37f7-828">driver's license</span></span>  <br/> <span data-ttu-id="a37f7-829">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-829">driver's license number</span></span>  <br/> <span data-ttu-id="a37f7-830">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-830">driver's licence number</span></span>  <br/> <span data-ttu-id="a37f7-831">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="a37f7-831">driving license number</span></span>  <br/> <span data-ttu-id="a37f7-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="a37f7-832">dlno#</span></span>  <br/> <span data-ttu-id="a37f7-833">körkort</span><span class="sxs-lookup"><span data-stu-id="a37f7-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="a37f7-834">UK</span><span class="sxs-lookup"><span data-stu-id="a37f7-834">UK</span></span>

<span data-ttu-id="a37f7-p103">Weitere Informationen finden Sie im Abschnitt "UK Driver es License Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="a37f7-p103">For details, see the section "U.K. Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a37f7-837">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a37f7-837">See also</span></span>

[<span data-ttu-id="a37f7-838">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="a37f7-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

