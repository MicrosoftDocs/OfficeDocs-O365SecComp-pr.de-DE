---
title: EU-Führerscheinnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Treiber Lizenznummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: be9497c325866a670dff8d82b5170f4ca947c4ad
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255773"
---
# <a name="eu-drivers-license-number"></a><span data-ttu-id="7a854-104">EU-Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-104">EU Driver's License Number</span></span>

<span data-ttu-id="7a854-105">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Treiber Lizenznummer erkennt.</span><span class="sxs-lookup"><span data-stu-id="7a854-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Driver's License Number sensitive information type.</span></span> <span data-ttu-id="7a854-106">Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="7a854-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="7a854-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="7a854-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="7a854-108">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-108">Format</span></span>

<span data-ttu-id="7a854-109">Acht Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-109">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-110">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-110">Pattern</span></span>

<span data-ttu-id="7a854-111">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-111">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a854-112">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-112">Checksum</span></span>

<span data-ttu-id="7a854-113">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-113">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-114">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-114">Definition</span></span>

<span data-ttu-id="7a854-115">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-115">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-116">Der reguläre Ausdruck `Regex_austria_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-116">The regular expression  `Regex_austria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-117">Ein Schlüsselwort `Keywords_austria_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-117">A keyword from  `Keywords_austria_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_driver's_license_number" />
          <Match idRef="Keywords_austria_eu_driver's_license_number" />
        </Pattern>
    </Entity>

```

### <a name="keywords"></a><span data-ttu-id="7a854-118">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-118">Keywords</span></span>

<span data-ttu-id="7a854-119">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-119"></span></span>
|<span data-ttu-id="7a854-120">**Keywords_austria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-120">**Keywords_austria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-121">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-121">dl#</span></span>  <br/> <span data-ttu-id="7a854-122">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-122">driver license</span></span>  <br/> <span data-ttu-id="7a854-123">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-123">driver license number</span></span>  <br/> <span data-ttu-id="7a854-124">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-124">driver licence</span></span>  <br/> <span data-ttu-id="7a854-125">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-125">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-126">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-126">drivers license</span></span>  <br/> <span data-ttu-id="7a854-127">driver's licence</span><span class="sxs-lookup"><span data-stu-id="7a854-127">driver's licence</span></span>  <br/> <span data-ttu-id="7a854-128">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-128">driver's license</span></span>  <br/> <span data-ttu-id="7a854-129">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-129">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-130">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-130">driver's licence number</span></span>  <br/>  <span data-ttu-id="7a854-131">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-131">driving license number</span></span>  <br/> <span data-ttu-id="7a854-132">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-132">dlno#</span></span>  <br/> <span data-ttu-id="7a854-133">Fuhrerschein</span><span class="sxs-lookup"><span data-stu-id="7a854-133">fuhrerschein</span></span>  <br/> <span data-ttu-id="7a854-134">Fuhrerschein Republik Osterreich</span><span class="sxs-lookup"><span data-stu-id="7a854-134">fuhrerschein republik osterreich</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="7a854-135">Belgien</span><span class="sxs-lookup"><span data-stu-id="7a854-135">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="7a854-136">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-136">Format</span></span>

<span data-ttu-id="7a854-137">10 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-137">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-138">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-138">Pattern</span></span>

<span data-ttu-id="7a854-139">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-139">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a854-140">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-140">Checksum</span></span>

<span data-ttu-id="7a854-141">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-141">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-142">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-142">Definition</span></span>

<span data-ttu-id="7a854-143">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-143">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-144">Der reguläre Ausdruck `Regex_belgium_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-144">The regular expression  `Regex_belgium_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-145">Ein Schlüsselwort `Keywords_belgium_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-145">A keyword from  `Keywords_belgium_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_driver's_license_number" />
          <Match idRef="Keywords_belgium_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="7a854-146">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-146">Keywords</span></span>

<span data-ttu-id="7a854-147">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-147"></span></span>
|<span data-ttu-id="7a854-148">**Keywords__belgium_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-148">**Keywords__belgium_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-149">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-149">dl#</span></span>  <br/> <span data-ttu-id="7a854-150">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-150">driver license</span></span>  <br/> <span data-ttu-id="7a854-151">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-151">driver license number</span></span>  <br/> <span data-ttu-id="7a854-152">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-152">driver licence</span></span>  <br/> <span data-ttu-id="7a854-153">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-153">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-154">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-154">drivers license</span></span>  <br/> <span data-ttu-id="7a854-155">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-155">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-156">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-156">driver's license</span></span>  <br/> <span data-ttu-id="7a854-157">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-157">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-158">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-158">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-159">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-159">dlno#</span></span>  <br/> <span data-ttu-id="7a854-160">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="7a854-160">rijbewijs</span></span>  <br/> <span data-ttu-id="7a854-161">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-161">rijbewijsnummer</span></span>  <br/> <span data-ttu-id="7a854-162">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-162">führerscheinnummer</span></span>  <br/> <span data-ttu-id="7a854-163">fuhrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-163">fuhrerscheinnummer</span></span>  <br/> <span data-ttu-id="7a854-164">fuehrerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-164">fuehrerscheinnummer</span></span>  <br/> <span data-ttu-id="7a854-165">Führerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="7a854-165">führerschein- nr</span></span>  <br/> <span data-ttu-id="7a854-166">Fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="7a854-166">fuehrerschein- Nr</span></span>  <br/> <span data-ttu-id="7a854-167">Fuehrerschein-Nr</span><span class="sxs-lookup"><span data-stu-id="7a854-167">fuehrerschein- nr</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="7a854-168">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="7a854-168">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="7a854-169">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-169">Format</span></span>

<span data-ttu-id="7a854-170">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-171">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-171">Pattern</span></span>

<span data-ttu-id="7a854-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-172">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a854-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-173">Checksum</span></span>

<span data-ttu-id="7a854-174">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-175">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-175">Definition</span></span>

<span data-ttu-id="7a854-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-177">Der reguläre Ausdruck `Regex_bulgaria_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-177">The regular expression  `Regex_bulgaria_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-178">Ein Schlüsselwort `Keywords_bulgaria_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-178">A keyword from  `Keywords_bulgaria_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
             <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_driver's_license_number" />
          <Match idRef="Keywords_bulgaria_eu_driver's_license_number" />
        </Pattern> 
</Entity>    

```

### <a name="keywords"></a><span data-ttu-id="7a854-179">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-179">Keywords</span></span>

<span data-ttu-id="7a854-180">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-180"></span></span>
|<span data-ttu-id="7a854-181">**Keywords_bulgaria_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-181">**Keywords_bulgaria_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-182">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-182">dl#</span></span>  <br/> <span data-ttu-id="7a854-183">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-183">driver license</span></span>  <br/> <span data-ttu-id="7a854-184">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-184">driver license number</span></span>  <br/> <span data-ttu-id="7a854-185">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-185">driver licence</span></span>  <br/> <span data-ttu-id="7a854-186">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-186">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-187">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-187">drivers license</span></span>  <br/> <span data-ttu-id="7a854-188">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-188">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-189">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-189">driver's license</span></span>  <br/> <span data-ttu-id="7a854-190">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-190">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-191">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-191">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-192">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-192">driving license number</span></span>  <br/> <span data-ttu-id="7a854-193">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-193">dlno#</span></span>  <br/> <span data-ttu-id="7a854-194">свидетелство за управление на мпс</span><span class="sxs-lookup"><span data-stu-id="7a854-194">свидетелство за управление на мпс</span></span>  <br/> <span data-ttu-id="7a854-195">свидетелство за управление на моторно превозно средство</span><span class="sxs-lookup"><span data-stu-id="7a854-195">свидетелство за управление на моторно превозно средство</span></span>  <br/> <span data-ttu-id="7a854-196">сумпс</span><span class="sxs-lookup"><span data-stu-id="7a854-196">сумпс</span></span>  <br/> <span data-ttu-id="7a854-197">шофьорска книжка</span><span class="sxs-lookup"><span data-stu-id="7a854-197">шофьорска книжка</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="7a854-198">Kroatien</span><span class="sxs-lookup"><span data-stu-id="7a854-198">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="7a854-199">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-199">Format</span></span>

<span data-ttu-id="7a854-200">Acht Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-200">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-201">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-201">Pattern</span></span>

<span data-ttu-id="7a854-202">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-202">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a854-203">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-203">Checksum</span></span>

<span data-ttu-id="7a854-204">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-204">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-205">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-205">Definition</span></span>

<span data-ttu-id="7a854-206">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-206">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-207">Der reguläre Ausdruck `Regex_croatia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-207">The regular expression  `Regex_croatia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-208">Ein Schlüsselwort `Keywords_croatia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-208">A keyword from  `Keywords_croatia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_driver's_license_number" />
          <Match idRef="Keywords_croatia_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="7a854-209">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-209">Keywords</span></span>

<span data-ttu-id="7a854-210">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-210"></span></span>
|<span data-ttu-id="7a854-211">**Keywords_croatia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-211">**Keywords_croatia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-212">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-212">dl#</span></span>  <br/> <span data-ttu-id="7a854-213">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-213">driver license</span></span>  <br/> <span data-ttu-id="7a854-214">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-214">driver license number</span></span>  <br/> <span data-ttu-id="7a854-215">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-215">driver licence</span></span>  <br/> <span data-ttu-id="7a854-216">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-216">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-217">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-217">drivers license</span></span>  <br/> <span data-ttu-id="7a854-218">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-218">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-219">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-219">driver's license</span></span>  <br/> <span data-ttu-id="7a854-220">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-220">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-221">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-221">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-222">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-222">driving license number</span></span>  <br/> <span data-ttu-id="7a854-223">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-223">dlno#</span></span>  <br/> <span data-ttu-id="7a854-224">vozačka dozvola</span><span class="sxs-lookup"><span data-stu-id="7a854-224">vozačka dozvola</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="7a854-225">Zypern</span><span class="sxs-lookup"><span data-stu-id="7a854-225">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="7a854-226">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-226">Format</span></span>

<span data-ttu-id="7a854-227">12 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-227">12 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-228">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-228">Pattern</span></span>

<span data-ttu-id="7a854-229">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-229">12 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a854-230">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-230">Checksum</span></span>

<span data-ttu-id="7a854-231">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-231">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-232">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-232">Definition</span></span>

<span data-ttu-id="7a854-233">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-233">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-234">Der reguläre Ausdruck `Regex_cyprus_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-234">The regular expression  `Regex_cyprus_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-235">Ein Schlüsselwort `Keywords_cyprus_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-235">A keyword from  `Keywords_cyprus_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_driver's_license_number" />
          <Match idRef="Keywords_cyprus_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-236">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-236">Keywords</span></span>

<span data-ttu-id="7a854-237">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-237"></span></span>
|<span data-ttu-id="7a854-238">**Keywords_cyprus_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-238">**Keywords_cyprus_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-239">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-239">dl#</span></span>  <br/> <span data-ttu-id="7a854-240">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-240">driver license</span></span>  <br/> <span data-ttu-id="7a854-241">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-241">driver license number</span></span>  <br/> <span data-ttu-id="7a854-242">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-242">driver licence</span></span>  <br/> <span data-ttu-id="7a854-243">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-243">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-244">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-244">drivers license</span></span>  <br/> <span data-ttu-id="7a854-245">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-245">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-246">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-246">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-247">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-247">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-248">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-248">driving license number</span></span>  <br/> <span data-ttu-id="7a854-249">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-249">dlno#</span></span>  <br/> <span data-ttu-id="7a854-250">άδεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="7a854-250">άδεια οδήγησης</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="7a854-251">Tschechien</span><span class="sxs-lookup"><span data-stu-id="7a854-251">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="7a854-252">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-252">Format</span></span>

<span data-ttu-id="7a854-253">Zwei Buchstaben gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-253">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-254">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-254">Pattern</span></span>

<span data-ttu-id="7a854-255">Acht Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7a854-255">Eight letters and digits:</span></span>
  
- <span data-ttu-id="7a854-256">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="7a854-256">Two letters (not case-sensitive)</span></span>
    
- <span data-ttu-id="7a854-257">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="7a854-257">A space (optional)</span></span>
    
- <span data-ttu-id="7a854-258">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-258">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-259">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-259">Checksum</span></span>

<span data-ttu-id="7a854-260">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-260">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-261">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-261">Definition</span></span>

<span data-ttu-id="7a854-262">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-262">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-263">Der reguläre Ausdruck `Regex_czech_republic_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-263">The regular expression  `Regex_czech_republic_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-264">Ein Schlüsselwort `Keywords_czech_republic_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-264">A keyword from  `Keywords_czech_republic_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_driver's_license_number" />
          <Match idRef="Keywords_czech_republic_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="7a854-265">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-265">Keywords</span></span>

<span data-ttu-id="7a854-266">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-266"></span></span>
|<span data-ttu-id="7a854-267">**Keywords_czech_republic_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-267">**Keywords_czech_republic_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-268">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-268">dl#</span></span>  <br/> <span data-ttu-id="7a854-269">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-269">driver license</span></span>  <br/> <span data-ttu-id="7a854-270">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-270">driver license number</span></span>  <br/> <span data-ttu-id="7a854-271">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-271">driver licence</span></span>  <br/> <span data-ttu-id="7a854-272">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-272">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-273">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-273">drivers license</span></span>  <br/> <span data-ttu-id="7a854-274">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-274">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-275">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-275">driver's license</span></span>  <br/> <span data-ttu-id="7a854-276">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-276">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-277">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-277">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-278">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-278">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-279">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-279">driving license number</span></span>  <br/> <span data-ttu-id="7a854-280">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-280">dlno#</span></span>  <br/> <span data-ttu-id="7a854-281">řidičský prúkaz</span><span class="sxs-lookup"><span data-stu-id="7a854-281">řidičský prúkaz</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="7a854-282">Dänemark</span><span class="sxs-lookup"><span data-stu-id="7a854-282">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="7a854-283">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-283">Format</span></span>

<span data-ttu-id="7a854-284">Acht Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-284">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-285">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-285">Pattern</span></span>

<span data-ttu-id="7a854-286">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-286">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a854-287">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-287">Checksum</span></span>

<span data-ttu-id="7a854-288">Ja</span><span class="sxs-lookup"><span data-stu-id="7a854-288">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-289">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-289">Definition</span></span>

<span data-ttu-id="7a854-290">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-290">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-291">Der reguläre Ausdruck `Regex_denmark_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-291">The regular expression  `Regex_denmark_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-292">Ein Schlüsselwort `Keywords_denmark_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-292">A keyword from  `Keywords_denmark_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_driver's_license_number" />
          <Match idRef="Keywords_denmark_eu_driver's_license_number" />
        </Pattern>
</Entity>

```

### <a name="keywords"></a><span data-ttu-id="7a854-293">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-293">Keywords</span></span>

<span data-ttu-id="7a854-294">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-294"></span></span>
|<span data-ttu-id="7a854-295">**Keywords_denmark_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-295">**Keywords_denmark_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-296">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-296">dl#</span></span>  <br/> <span data-ttu-id="7a854-297">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-297">driver license</span></span>  <br/> <span data-ttu-id="7a854-298">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-298">driver license number</span></span>  <br/> <span data-ttu-id="7a854-299">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-299">driver licence</span></span>  <br/> <span data-ttu-id="7a854-300">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-300">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-301">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-301">drivers license</span></span>  <br/> <span data-ttu-id="7a854-302">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-302">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-303">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-303">driver's license</span></span>  <br/> <span data-ttu-id="7a854-304">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-304">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-305">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-305">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-306">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-306">driving license number</span></span>  <br/> <span data-ttu-id="7a854-307">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-307">dlno#</span></span>  <br/> <span data-ttu-id="7a854-308">kørekort</span><span class="sxs-lookup"><span data-stu-id="7a854-308">kørekort</span></span>  <br/> <span data-ttu-id="7a854-309">kørekortnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-309">kørekortnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="7a854-310">Estland</span><span class="sxs-lookup"><span data-stu-id="7a854-310">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="7a854-311">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-311">Format</span></span>

<span data-ttu-id="7a854-312">Zwei Buchstaben gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-312">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-313">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-313">Pattern</span></span>

<span data-ttu-id="7a854-314">Zwei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7a854-314">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="7a854-315">Die Buchstaben "ET" (Groß-/Kleinschreibung wird nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="7a854-315">The letters "ET" (not case-sensitive)</span></span> 
    
- <span data-ttu-id="7a854-316">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-316">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-317">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-317">Checksum</span></span>

<span data-ttu-id="7a854-318">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-318">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-319">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-319">Definition</span></span>

<span data-ttu-id="7a854-320">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-320">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-321">Der reguläre Ausdruck `Regex_estonia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-321">The regular expression  `Regex_estonia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-322">Ein Schlüsselwort `Keywords_estonia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-322">A keyword from  `Keywords_estonia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_driver's_license_number" />
          <Match idRef="Keywords_estonia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-323">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-323">Keywords</span></span>

<span data-ttu-id="7a854-324">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-324"></span></span>
|<span data-ttu-id="7a854-325">**Keywords_estonia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-325">**Keywords_estonia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-326">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-326">dl#</span></span>  <br/> <span data-ttu-id="7a854-327">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-327">driver license</span></span>  <br/> <span data-ttu-id="7a854-328">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-328">driver license number</span></span>  <br/> <span data-ttu-id="7a854-329">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-329">driver license number</span></span>  <br/> <span data-ttu-id="7a854-330">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-330">driver licence</span></span>  <br/> <span data-ttu-id="7a854-331">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-331">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-332">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-332">drivers license</span></span>  <br/> <span data-ttu-id="7a854-333">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-333">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-334">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-334">driver's license</span></span>  <br/> <span data-ttu-id="7a854-335">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-335">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-336">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-336">driving license number</span></span>  <br/> <span data-ttu-id="7a854-337">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-337">dlno#</span></span>  <br/> <span data-ttu-id="7a854-338">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="7a854-338">permis de conduire</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="7a854-339">Finnland</span><span class="sxs-lookup"><span data-stu-id="7a854-339">Finland</span></span>

### <a name="format"></a><span data-ttu-id="7a854-340">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-340">Format</span></span>

<span data-ttu-id="7a854-341">10 Ziffern, die einen Bindestrich enthalten</span><span class="sxs-lookup"><span data-stu-id="7a854-341">10 digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-342">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-342">Pattern</span></span>

<span data-ttu-id="7a854-343">10 Ziffern mit einem Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="7a854-343">10 digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="7a854-344">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-344">Six digits</span></span> 
    
- <span data-ttu-id="7a854-345">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="7a854-345">A hyphen</span></span>
    
-  <span data-ttu-id="7a854-346">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-346">Four digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="7a854-347">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-347">Checksum</span></span>

<span data-ttu-id="7a854-348">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-348">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-349">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-349">Definition</span></span>

<span data-ttu-id="7a854-350">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-350">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-351">Der reguläre Ausdruck `Regex_finland_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-351">The regular expression  `Regex_finland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-352">Ein Schlüsselwort `Keywords_finland_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-352">A keyword from  `Keywords_finland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_finland_eu_driver's_license_number" />
          <Match idRef="Keywords_finland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-353">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-353">Keywords</span></span>

<span data-ttu-id="7a854-354">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-354"></span></span>
|<span data-ttu-id="7a854-355">**Keywords_finland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-355">**Keywords_finland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-356">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-356">dl#</span></span>  <br/> <span data-ttu-id="7a854-357">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-357">driver license</span></span>  <br/> <span data-ttu-id="7a854-358">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-358">driver license number</span></span>  <br/> <span data-ttu-id="7a854-359">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-359">driver licence</span></span>  <br/> <span data-ttu-id="7a854-360">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-360">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-361">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-361">drivers license</span></span>  <br/> <span data-ttu-id="7a854-362">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-362">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-363">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-363">driver's license</span></span>  <br/> <span data-ttu-id="7a854-364">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-364">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-365">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-365">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-366">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-366">driving license number</span></span>  <br/> <span data-ttu-id="7a854-367">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-367">dlno#</span></span>  <br/> <span data-ttu-id="7a854-368">ajokortti</span><span class="sxs-lookup"><span data-stu-id="7a854-368">ajokortti</span></span>  <br/> |
   
## <a name="france"></a><span data-ttu-id="7a854-369">Frankreich</span><span class="sxs-lookup"><span data-stu-id="7a854-369">France</span></span>

<span data-ttu-id="7a854-370">Weitere Informationen finden Sie im Abschnitt "Frankreich Driver es License Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7a854-370">For details, see the section "France Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="7a854-371">Deutschland</span><span class="sxs-lookup"><span data-stu-id="7a854-371">Germany</span></span>

<span data-ttu-id="7a854-372">Weitere Informationen finden Sie im Abschnitt "German Driver es License Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7a854-372">For details, see the section "German Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="7a854-373">Griechenland</span><span class="sxs-lookup"><span data-stu-id="7a854-373">Greece</span></span>

### <a name="format"></a><span data-ttu-id="7a854-374">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-374">Format</span></span>

<span data-ttu-id="7a854-375">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-375">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-376">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-376">Pattern</span></span>

 <span data-ttu-id="7a854-377">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-377">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7a854-378">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-378">Checksum</span></span>

<span data-ttu-id="7a854-379">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-379">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-380">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-380">Definition</span></span>

<span data-ttu-id="7a854-381">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-381">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-382">Der reguläre Ausdruck `Regex_greece_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-382">The regular expression  `Regex_greece_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-383">Ein Schlüsselwort `Keywords_greece_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-383">A keyword from  `Keywords_greece_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_driver's_license_number" />
          <Match idRef="Keywords_greece_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-384">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-384">Keywords</span></span>

<span data-ttu-id="7a854-385">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-385"></span></span>
|<span data-ttu-id="7a854-386">**Keywords_greece_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-386">**Keywords_greece_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-387">DlL</span><span class="sxs-lookup"><span data-stu-id="7a854-387">dlL#</span></span>  <br/> <span data-ttu-id="7a854-388">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-388">driver license</span></span>  <br/> <span data-ttu-id="7a854-389">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-389">driver license number</span></span>  <br/> <span data-ttu-id="7a854-390">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-390">driver licence</span></span>  <br/> <span data-ttu-id="7a854-391">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-391">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-392">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-392">drivers license</span></span>  <br/> <span data-ttu-id="7a854-393">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-393">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-394">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-394">driver's license</span></span>  <br/> <span data-ttu-id="7a854-395">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-395">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-396">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-396">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-397">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-397">driving license number</span></span>  <br/> <span data-ttu-id="7a854-398">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-398">dlno#</span></span>  <br/> <span data-ttu-id="7a854-399">δεια οδήγησης</span><span class="sxs-lookup"><span data-stu-id="7a854-399">δεια οδήγησης</span></span>  <br/> <span data-ttu-id="7a854-400">Adeia odigisis</span><span class="sxs-lookup"><span data-stu-id="7a854-400">Adeia odigisis</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="7a854-401">Ungarn</span><span class="sxs-lookup"><span data-stu-id="7a854-401">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="7a854-402">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-402">Format</span></span>

<span data-ttu-id="7a854-403">Zwei Buchstaben gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-403">Two letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-404">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-404">Pattern</span></span>

<span data-ttu-id="7a854-405">Zwei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7a854-405">Two letters and six digits:</span></span>
  
-  <span data-ttu-id="7a854-406">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="7a854-406">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="7a854-407">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-407">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-408">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-408">Checksum</span></span>

<span data-ttu-id="7a854-409">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-409">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-410">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-410">Definition</span></span>

<span data-ttu-id="7a854-411">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-411">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-412">Der reguläre Ausdruck `Regex_hungary_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-412">The regular expression  `Regex_hungary_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-413">Ein Schlüsselwort `Keywords_hungary_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-413">A keyword from  `Keywords_hungary_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_driver's_license_number" />
          <Match idRef="Keywords_hungary_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-414">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-414">Keywords</span></span>

<span data-ttu-id="7a854-415">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-415"></span></span>
|<span data-ttu-id="7a854-416">**Keywords_hungary_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-416">**Keywords_hungary_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-417">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-417">dl#</span></span>  <br/> <span data-ttu-id="7a854-418">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-418">driver license</span></span>  <br/> <span data-ttu-id="7a854-419">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-419">driver license number</span></span>  <br/> <span data-ttu-id="7a854-420">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-420">driver licence</span></span>  <br/> <span data-ttu-id="7a854-421">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-421">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-422">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-422">drivers license</span></span>  <br/> <span data-ttu-id="7a854-423">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-423">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-424">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-424">driver's license</span></span>  <br/> <span data-ttu-id="7a854-425">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-425">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-426">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-426">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-427">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-427">driving license number</span></span>  <br/> <span data-ttu-id="7a854-428">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-428">dlno#</span></span>  <br/> <span data-ttu-id="7a854-429">vezetoi engedely</span><span class="sxs-lookup"><span data-stu-id="7a854-429">vezetoi engedely</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="7a854-430">Irland</span><span class="sxs-lookup"><span data-stu-id="7a854-430">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="7a854-431">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-431">Format</span></span>

<span data-ttu-id="7a854-432">Sechs Ziffern gefolgt von vier Buchstaben</span><span class="sxs-lookup"><span data-stu-id="7a854-432">Six digits followed by four letters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-433">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-433">Pattern</span></span>

<span data-ttu-id="7a854-434">Sechs Ziffern und vier Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="7a854-434">Six digits and four letters:</span></span>
  
- <span data-ttu-id="7a854-435">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-435">Six digits</span></span>
    
- <span data-ttu-id="7a854-436">Vier Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="7a854-436">Four letters (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-437">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-437">Checksum</span></span>

<span data-ttu-id="7a854-438">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-438">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-439">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-439">Definition</span></span>

<span data-ttu-id="7a854-440">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-440">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-441">Der reguläre Ausdruck `Regex_ireland_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-441">The regular expression  `Regex_ireland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-442">Ein Schlüsselwort `Keywords_ireland_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-442">A keyword from  `Keywords_ireland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_driver's_license_number" />
          <Match idRef="Keywords_ireland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-443">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-443">Keywords</span></span>

<span data-ttu-id="7a854-444">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-444"></span></span>
|<span data-ttu-id="7a854-445">**Keywords_ireland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-445">**Keywords_ireland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-446">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-446">dl#</span></span>  <br/> <span data-ttu-id="7a854-447">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-447">driver license</span></span>  <br/> <span data-ttu-id="7a854-448">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-448">driver license number</span></span>  <br/> <span data-ttu-id="7a854-449">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-449">driver licence</span></span>  <br/> <span data-ttu-id="7a854-450">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-450">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-451">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-451">drivers license</span></span>  <br/> <span data-ttu-id="7a854-452">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-452">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-453">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-453">driver's license</span></span>  <br/> <span data-ttu-id="7a854-454">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-454">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-455">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-455">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-456">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-456">driving license number</span></span>  <br/> <span data-ttu-id="7a854-457">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-457">dlno#</span></span>  <br/> <span data-ttu-id="7a854-458">Ceadúnas Tiomána</span><span class="sxs-lookup"><span data-stu-id="7a854-458">ceadúnas tiomána</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="7a854-459">Italien</span><span class="sxs-lookup"><span data-stu-id="7a854-459">Italy</span></span>

<span data-ttu-id="7a854-460">Weitere Informationen finden Sie im Abschnitt "Italy Driver es License Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7a854-460">For details, see the section "Italy Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="latvia"></a><span data-ttu-id="7a854-461">Lettland</span><span class="sxs-lookup"><span data-stu-id="7a854-461">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="7a854-462">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-462">Format</span></span>

<span data-ttu-id="7a854-463">Drei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-463">Three letters followed by six digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-464">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-464">Pattern</span></span>

<span data-ttu-id="7a854-465">Drei Buchstaben und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7a854-465">Three letters and six digits:</span></span>
  
-  <span data-ttu-id="7a854-466">Drei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="7a854-466">Three letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="7a854-467">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-467">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-468">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-468">Checksum</span></span>

<span data-ttu-id="7a854-469">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-469">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-470">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-470">Definition</span></span>

<span data-ttu-id="7a854-471">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-471">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-472">Der reguläre Ausdruck `Regex_latvia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-472">The regular expression  `Regex_latvia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-473">Ein Schlüsselwort `Keywords_latvia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-473">A keyword from  `Keywords_latvia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_driver's_license_number" />
          <Match idRef="Keywords_latvia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-474">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-474">Keywords</span></span>

<span data-ttu-id="7a854-475">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-475"></span></span>
|<span data-ttu-id="7a854-476">**Keywords_latvia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-476">**Keywords_latvia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-477">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-477">dl#</span></span>  <br/> <span data-ttu-id="7a854-478">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-478">driver license</span></span>  <br/> <span data-ttu-id="7a854-479">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-479">driver license number</span></span>  <br/> <span data-ttu-id="7a854-480">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-480">driver licence</span></span>  <br/> <span data-ttu-id="7a854-481">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-481">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-482">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-482">drivers license</span></span>  <br/> <span data-ttu-id="7a854-483">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-483">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-484">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-484">driver's license</span></span>  <br/> <span data-ttu-id="7a854-485">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-485">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-486">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-486">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-487">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-487">driving license number</span></span>  <br/> <span data-ttu-id="7a854-488">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-488">dlno#</span></span>  <br/> <span data-ttu-id="7a854-489">autovadītāja apliecība</span><span class="sxs-lookup"><span data-stu-id="7a854-489">autovadītāja apliecība</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="7a854-490">Litauen</span><span class="sxs-lookup"><span data-stu-id="7a854-490">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="7a854-491">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-491">Format</span></span>

<span data-ttu-id="7a854-492">Acht Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-492">Eight digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-493">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-493">Pattern</span></span>

 <span data-ttu-id="7a854-494">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-494">Eight digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7a854-495">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-495">Checksum</span></span>

<span data-ttu-id="7a854-496">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-496">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-497">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-497">Definition</span></span>

<span data-ttu-id="7a854-498">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-498">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-499">Der reguläre Ausdruck `Regex_lithuania_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-499">The regular expression  `Regex_lithuania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-500">Ein Schlüsselwort `Keywords_lithuania_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-500">A keyword from  `Keywords_lithuania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_driver's_license_number" />
          <Match idRef="Keywords_lithuania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-501">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-501">Keywords</span></span>

<span data-ttu-id="7a854-502">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-502"></span></span>
|<span data-ttu-id="7a854-503">**Keywords_lithuania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-503">**Keywords_lithuania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-504">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-504">dl#</span></span>  <br/> <span data-ttu-id="7a854-505">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-505">driver license</span></span>  <br/> <span data-ttu-id="7a854-506">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-506">driver license number</span></span>  <br/> <span data-ttu-id="7a854-507">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-507">driver licence</span></span>  <br/> <span data-ttu-id="7a854-508">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-508">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-509">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-509">drivers license</span></span>  <br/> <span data-ttu-id="7a854-510">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-510">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-511">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-511">driver's license</span></span>  <br/> <span data-ttu-id="7a854-512">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-512">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-513">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-513">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-514">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-514">driving license number</span></span>  <br/> <span data-ttu-id="7a854-515">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-515">dlno#</span></span>  <br/> <span data-ttu-id="7a854-516">Vairuotojo pažymėjimas</span><span class="sxs-lookup"><span data-stu-id="7a854-516">vairuotojo pažymėjimas</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="7a854-517">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="7a854-517">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="7a854-518">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-518">Format</span></span>

<span data-ttu-id="7a854-519">Sechs Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-519">Six digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-520">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-520">Pattern</span></span>

 <span data-ttu-id="7a854-521">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-521">Six digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7a854-522">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-522">Checksum</span></span>

<span data-ttu-id="7a854-523">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-523">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-524">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-524">Definition</span></span>

<span data-ttu-id="7a854-525">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-525">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-526">Der reguläre Ausdruck `Regex_luxemburg_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-526">The regular expression  `Regex_luxemburg_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-527">Ein Schlüsselwort `Keywords_luxemburg_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-527">A keyword from  `Keywords_luxemburg_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_luxemburg_eu_driver's_license_number" />
          <Match idRef="Keywords_luxemburg_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-528">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-528">Keywords</span></span>

<span data-ttu-id="7a854-529">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-529"></span></span>
|<span data-ttu-id="7a854-530">**Keywords_luxemburg_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-530">**Keywords_luxemburg_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-531">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-531">dl#</span></span>  <br/> <span data-ttu-id="7a854-532">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-532">driver license</span></span>  <br/> <span data-ttu-id="7a854-533">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-533">driver license number</span></span>  <br/> <span data-ttu-id="7a854-534">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-534">driver licence</span></span>  <br/> <span data-ttu-id="7a854-535">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-535">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-536">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-536">drivers license</span></span>  <br/> <span data-ttu-id="7a854-537">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-537">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-538">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-538">driver's license</span></span>  <br/> <span data-ttu-id="7a854-539">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-539">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-540">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-540">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-541">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-541">driving license number</span></span>  <br/> <span data-ttu-id="7a854-542">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-542">dlno#</span></span>  <br/> <span data-ttu-id="7a854-543">Fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="7a854-543">fahrerlaubnis</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="7a854-544">Malta</span><span class="sxs-lookup"><span data-stu-id="7a854-544">Malta</span></span>

### <a name="format"></a><span data-ttu-id="7a854-545">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-545">Format</span></span>

<span data-ttu-id="7a854-546">Kombination aus zwei Zeichen und sechs Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-546">Combination of two characters and six digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-547">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-547">Pattern</span></span>

<span data-ttu-id="7a854-548">Kombination aus zwei Zeichen und sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7a854-548">Combination of two characters and six digits:</span></span>
  
- <span data-ttu-id="7a854-549">Zwei Zeichen (Ziffern oder Buchstaben, keine Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="7a854-549">Two characters (digits or letters, not case-sensitive)</span></span>
    
- <span data-ttu-id="7a854-550">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="7a854-550">A space (optional)</span></span>
    
- <span data-ttu-id="7a854-551">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-551">Three digits</span></span>
    
- <span data-ttu-id="7a854-552">Ein Leerzeichen (optional) </span><span class="sxs-lookup"><span data-stu-id="7a854-552">A space (optional)</span></span>
    
- <span data-ttu-id="7a854-553">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-553">Three digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-554">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-554">Checksum</span></span>

<span data-ttu-id="7a854-555">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-555">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-556">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-556">Definition</span></span>

<span data-ttu-id="7a854-557">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-557">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-558">Der reguläre Ausdruck `Regex_malta_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-558">The regular expression  `Regex_malta_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-559">Ein Schlüsselwort `Keywords_malta_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-559">A keyword from  `Keywords_malta_eu_driver's_license_number` is found.</span></span> 
    
```
<!-- EU Driver's License Number -->
 <Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_driver's_license_number" />
          <Match idRef="Keywords_malta_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-560">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-560">Keywords</span></span>

<span data-ttu-id="7a854-561">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-561"></span></span>
|<span data-ttu-id="7a854-562">**Keywords_malta_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-562">**Keywords_malta_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-563">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-563">dl#</span></span>  <br/> <span data-ttu-id="7a854-564">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-564">driver license</span></span>  <br/> <span data-ttu-id="7a854-565">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-565">driver license number</span></span>  <br/> <span data-ttu-id="7a854-566">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-566">driver licence</span></span>  <br/> <span data-ttu-id="7a854-567">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-567">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-568">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-568">drivers license</span></span>  <br/> <span data-ttu-id="7a854-569">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-569">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-570">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-570">driver's license</span></span>  <br/> <span data-ttu-id="7a854-571">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-571">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-572">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-572">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-573">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-573">driving license number</span></span>  <br/> <span data-ttu-id="7a854-574">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-574">dlno#</span></span>  <br/> <span data-ttu-id="7a854-575">Liċenzja TAS-Sewqan</span><span class="sxs-lookup"><span data-stu-id="7a854-575">liċenzja tas-sewqan</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="7a854-576">Niederlande</span><span class="sxs-lookup"><span data-stu-id="7a854-576">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="7a854-577">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-577">Format</span></span>

<span data-ttu-id="7a854-578">10 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-578">10 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-579">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-579">Pattern</span></span>

<span data-ttu-id="7a854-580">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-580">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a854-581">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-581">Checksum</span></span>

<span data-ttu-id="7a854-582">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-582">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-583">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-583">Definition</span></span>

<span data-ttu-id="7a854-584">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-584">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-585">Der reguläre Ausdruck `Regex_netherlands_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-585">The regular expression  `Regex_netherlands_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-586">Ein Schlüsselwort `Keywords_netherlands_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-586">A keyword from  `Keywords_netherlands_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_driver's_license_number" />
          <Match idRef="Keywords_netherlands_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-587">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-587">Keywords</span></span>

<span data-ttu-id="7a854-588">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-588"></span></span>
|<span data-ttu-id="7a854-589">**Keywords_netherlands_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-589">**Keywords_netherlands_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-590">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-590">dl#</span></span>  <br/> <span data-ttu-id="7a854-591">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-591">driver license</span></span>  <br/> <span data-ttu-id="7a854-592">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-592">driver license number</span></span>  <br/> <span data-ttu-id="7a854-593">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-593">driver licence</span></span>  <br/> <span data-ttu-id="7a854-594">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-594">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-595">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-595">drivers license</span></span>  <br/> <span data-ttu-id="7a854-596">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-596">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-597">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-597">driver's license</span></span>  <br/> <span data-ttu-id="7a854-598">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-598">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-599">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-599">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-600">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-600">driving license number</span></span>  <br/> <span data-ttu-id="7a854-601">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-601">dlno#</span></span>  <br/> <span data-ttu-id="7a854-602">permis de conduire</span><span class="sxs-lookup"><span data-stu-id="7a854-602">permis de conduire</span></span>  <br/> <span data-ttu-id="7a854-603">rijbewijs</span><span class="sxs-lookup"><span data-stu-id="7a854-603">rijbewijs</span></span>  <br/> <span data-ttu-id="7a854-604">rijbewijsnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-604">rijbewijsnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="7a854-605">Polen</span><span class="sxs-lookup"><span data-stu-id="7a854-605">Poland</span></span>

### <a name="format"></a><span data-ttu-id="7a854-606">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-606">Format</span></span>

<span data-ttu-id="7a854-607">14 Ziffern mit 2 Schrägstrichen</span><span class="sxs-lookup"><span data-stu-id="7a854-607">14 digits containing 2 forward slashes</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-608">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-608">Pattern</span></span>

<span data-ttu-id="7a854-609">14 Ziffern und 2 Schrägstriche:</span><span class="sxs-lookup"><span data-stu-id="7a854-609">14 digits and 2 forward slashes:</span></span>
  
-  <span data-ttu-id="7a854-610">Fünf Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-610">Five digits</span></span> 
    
- <span data-ttu-id="7a854-611">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="7a854-611">A forward slash</span></span>
    
- <span data-ttu-id="7a854-612">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-612">Two digits</span></span>
    
- <span data-ttu-id="7a854-613">Ein Schrägstrich </span><span class="sxs-lookup"><span data-stu-id="7a854-613">A forward slash</span></span>
    
- <span data-ttu-id="7a854-614">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-614">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-615">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-615">Checksum</span></span>

<span data-ttu-id="7a854-616">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-616">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-617">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-617">Definition</span></span>

<span data-ttu-id="7a854-618">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-618">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-619">Der reguläre Ausdruck `Regex_poland_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-619">The regular expression  `Regex_poland_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-620">Ein Schlüsselwort `Keywords_poland_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-620">A keyword from  `Keywords_poland_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_poland_eu_driver's_license_number" />
          <Match idRef="Keywords_poland_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-621">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-621">Keywords</span></span>

<span data-ttu-id="7a854-622">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-622"></span></span>
|<span data-ttu-id="7a854-623">**Keywords_poland_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-623">**Keywords_poland_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-624">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-624">dl#</span></span>  <br/> <span data-ttu-id="7a854-625">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-625">driver license</span></span>  <br/> <span data-ttu-id="7a854-626">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-626">driver license number</span></span>  <br/> <span data-ttu-id="7a854-627">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-627">driver licence</span></span>  <br/> <span data-ttu-id="7a854-628">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-628">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-629">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-629">drivers license</span></span>  <br/> <span data-ttu-id="7a854-630">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-630">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-631">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-631">driver's license</span></span>  <br/> <span data-ttu-id="7a854-632">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-632">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-633">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-633">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-634">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-634">driving license number</span></span>  <br/> <span data-ttu-id="7a854-635">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-635">dlno#</span></span>  <br/> <span data-ttu-id="7a854-636">Prawo jazdy</span><span class="sxs-lookup"><span data-stu-id="7a854-636">prawo jazdy</span></span>  <br/> |
   
## <a name="portugal"></a><span data-ttu-id="7a854-637">Portugal</span><span class="sxs-lookup"><span data-stu-id="7a854-637">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="7a854-638">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-638">Format</span></span>

<span data-ttu-id="7a854-639">Zwei Buchstaben gefolgt von sieben Zahlen im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-639">Two letters followed by a seven numbers in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-640">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-640">Pattern</span></span>

<span data-ttu-id="7a854-641">Zwei Buchstaben gefolgt von sieben Zahlen mit Sonderzeichen:</span><span class="sxs-lookup"><span data-stu-id="7a854-641">Two letters followed by seven numbers with special characters:</span></span>
  
-  <span data-ttu-id="7a854-642">Zwei Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="7a854-642">Two letters (not case-sensitive)</span></span> 
    
- <span data-ttu-id="7a854-643">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="7a854-643">A hyphen</span></span>
    
- <span data-ttu-id="7a854-644">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-644">Six digits</span></span>
    
- <span data-ttu-id="7a854-645">Ein Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="7a854-645">A space</span></span>
    
- <span data-ttu-id="7a854-646">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="7a854-646">One digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-647">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-647">Checksum</span></span>

<span data-ttu-id="7a854-648">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-648">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-649">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-649">Definition</span></span>

<span data-ttu-id="7a854-650">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-650">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-651">Der reguläre Ausdruck `Regex_portugal_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-651">The regular expression  `Regex_portugal_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-652">Ein Schlüsselwort `Keywords_portugal_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-652">A keyword from  `Keywords_portugal_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_driver's_license_number" />
          <Match idRef="Keywords_portugal_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-653">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-653">Keywords</span></span>

<span data-ttu-id="7a854-654">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-654"></span></span>
|<span data-ttu-id="7a854-655">**Keywords_portugal_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-655">**Keywords_portugal_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-656">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-656">dl#</span></span>  <br/> <span data-ttu-id="7a854-657">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-657">driver license</span></span>  <br/> <span data-ttu-id="7a854-658">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-658">driver license number</span></span>  <br/> <span data-ttu-id="7a854-659">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-659">driver licence</span></span>  <br/> <span data-ttu-id="7a854-660">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-660">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-661">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-661">drivers license</span></span>  <br/> <span data-ttu-id="7a854-662">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-662">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-663">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-663">driver's license</span></span>  <br/> <span data-ttu-id="7a854-664">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-664">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-665">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-665">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-666">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-666">driving license number</span></span>  <br/> <span data-ttu-id="7a854-667">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-667">dlno#</span></span>  <br/> <span data-ttu-id="7a854-668">Carteira de motorista</span><span class="sxs-lookup"><span data-stu-id="7a854-668">carteira de motorista</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="7a854-669">Rumänien</span><span class="sxs-lookup"><span data-stu-id="7a854-669">Romania</span></span>

### <a name="format"></a><span data-ttu-id="7a854-670">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-670">Format</span></span>

<span data-ttu-id="7a854-671">Ein Zeichen, gefolgt von acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-671">One character followed by eight digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-672">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-672">Pattern</span></span>

<span data-ttu-id="7a854-673">Ein Zeichen, gefolgt von acht Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7a854-673">One character followed by eight digits:</span></span>
  
-  <span data-ttu-id="7a854-674">Ein Buchstabe (ohne Unterscheidung von Groß-/Kleinschreibung) oder Ziffer</span><span class="sxs-lookup"><span data-stu-id="7a854-674">One letter (not case-sensitive) or digit</span></span> 
    
- <span data-ttu-id="7a854-675">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-675">Eight digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-676">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-676">Checksum</span></span>

<span data-ttu-id="7a854-677">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-677">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-678">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-678">Definition</span></span>

<span data-ttu-id="7a854-679">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-679">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-680">Der reguläre Ausdruck `Regex_romania_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-680">The regular expression  `Regex_romania_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-681">Ein Schlüsselwort `Keywords_romania_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-681">A keyword from  `Keywords_romania_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_driver's_license_number" />
          <Match idRef="Keywords_romania_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-682">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-682">Keywords</span></span>

<span data-ttu-id="7a854-683">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-683"></span></span>
|<span data-ttu-id="7a854-684">**Keywords_romania_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-684">**Keywords_romania_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-685">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-685">dl#</span></span>  <br/> <span data-ttu-id="7a854-686">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-686">driver license</span></span>  <br/> <span data-ttu-id="7a854-687">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-687">driver license number</span></span>  <br/> <span data-ttu-id="7a854-688">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-688">driver licence</span></span>  <br/> <span data-ttu-id="7a854-689">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-689">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-690">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-690">drivers license</span></span>  <br/> <span data-ttu-id="7a854-691">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-691">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-692">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-692">driver's license</span></span>  <br/> <span data-ttu-id="7a854-693">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-693">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-694">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-694">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-695">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-695">driving license number</span></span>  <br/> <span data-ttu-id="7a854-696">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-696">dlno#</span></span>  <br/> <span data-ttu-id="7a854-697">permis de conducere</span><span class="sxs-lookup"><span data-stu-id="7a854-697">permis de conducere</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="7a854-698">Slowakei</span><span class="sxs-lookup"><span data-stu-id="7a854-698">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="7a854-699">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-699">Format</span></span>

<span data-ttu-id="7a854-700">Ein Zeichen, gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-700">One character followed by seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-701">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-701">Pattern</span></span>

<span data-ttu-id="7a854-702">Ein Zeichen, gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-702">One character followed by seven digits</span></span>
  
- <span data-ttu-id="7a854-703">Ein Buchstabe (ohne Unterscheidung von Groß-/Kleinschreibung) oder Ziffer</span><span class="sxs-lookup"><span data-stu-id="7a854-703">One letter (not case-sensitive) or digit</span></span>
    
-  <span data-ttu-id="7a854-704">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-704">Seven digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="7a854-705">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-705">Checksum</span></span>

<span data-ttu-id="7a854-706">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-706">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-707">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-707">Definition</span></span>

<span data-ttu-id="7a854-708">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-708">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-709">Der reguläre Ausdruck `Regex_slovakia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-709">The regular expression  `Regex_slovakia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-710">Ein Schlüsselwort `Keywords_slovakia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-710">A keyword from  `Keywords_slovakia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovaknia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovakia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-711">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-711">Keywords</span></span>

<span data-ttu-id="7a854-712">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-712"></span></span>
|<span data-ttu-id="7a854-713">**Keywords_slovakia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-713">**Keywords_slovakia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-714">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-714">dl#</span></span>  <br/> <span data-ttu-id="7a854-715">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-715">driver license</span></span>  <br/> <span data-ttu-id="7a854-716">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-716">driver license number</span></span>  <br/> <span data-ttu-id="7a854-717">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-717">driver licence</span></span>  <br/> <span data-ttu-id="7a854-718">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-718">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-719">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-719">drivers license</span></span>  <br/> <span data-ttu-id="7a854-720">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-720">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-721">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-721">driver's license</span></span>  <br/> <span data-ttu-id="7a854-722">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-722">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-723">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-723">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-724">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-724">driving license number</span></span>  <br/> <span data-ttu-id="7a854-725">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-725">dlno#</span></span>  <br/> <span data-ttu-id="7a854-726">vodičský preukaz</span><span class="sxs-lookup"><span data-stu-id="7a854-726">vodičský preukaz</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="7a854-727">Slowenien</span><span class="sxs-lookup"><span data-stu-id="7a854-727">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="7a854-728">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-728">Format</span></span>

<span data-ttu-id="7a854-729">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7a854-729">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-730">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-730">Pattern</span></span>

<span data-ttu-id="7a854-731">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-731">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7a854-732">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-732">Checksum</span></span>

<span data-ttu-id="7a854-733">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-733">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-734">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-734">Definition</span></span>

<span data-ttu-id="7a854-735">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-735">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-736">Der reguläre Ausdruck `Regex_slovenia_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-736">The regular expression  `Regex_slovenia_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-737">Ein Schlüsselwort `Keywords_slovenia_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-737">A keyword from  `Keywords_slovenia_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_driver's_license_number" />
          <Match idRef="Keywords_slovenia_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-738">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-738">Keywords</span></span>

<span data-ttu-id="7a854-739">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-739"></span></span>
|<span data-ttu-id="7a854-740">**Keywords_slovenia_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-740">**Keywords_slovenia_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-741">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-741">dl#</span></span>  <br/> <span data-ttu-id="7a854-742">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-742">driver license</span></span>  <br/> <span data-ttu-id="7a854-743">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-743">driver license number</span></span>  <br/> <span data-ttu-id="7a854-744">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-744">driver licence</span></span>  <br/> <span data-ttu-id="7a854-745">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-745">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-746">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-746">drivers license</span></span>  <br/> <span data-ttu-id="7a854-747">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-747">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-748">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-748">driver's license</span></span>  <br/> <span data-ttu-id="7a854-749">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-749">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-750">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-750">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-751">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-751">driving license number</span></span>  <br/> <span data-ttu-id="7a854-752">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-752">dlno#</span></span>  <br/> <span data-ttu-id="7a854-753">vozniško Dovoljenje</span><span class="sxs-lookup"><span data-stu-id="7a854-753">vozniško dovoljenje</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="7a854-754">Spanien</span><span class="sxs-lookup"><span data-stu-id="7a854-754">Spain</span></span>

### <a name="format"></a><span data-ttu-id="7a854-755">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-755">Format</span></span>

<span data-ttu-id="7a854-756">Acht Ziffern gefolgt von einem Zeichen</span><span class="sxs-lookup"><span data-stu-id="7a854-756">Eight digits followed by one character</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-757">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-757">Pattern</span></span>

<span data-ttu-id="7a854-758">Acht Ziffern gefolgt von einem Zeichen:</span><span class="sxs-lookup"><span data-stu-id="7a854-758">Eight digits followed by one character:</span></span>
  
-  <span data-ttu-id="7a854-759">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-759">Eight digits</span></span> 
    
- <span data-ttu-id="7a854-760">Eine Ziffer oder ein Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="7a854-760">One digit or letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-761">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-761">Checksum</span></span>

<span data-ttu-id="7a854-762">Ja</span><span class="sxs-lookup"><span data-stu-id="7a854-762">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-763">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-763">Definition</span></span>

<span data-ttu-id="7a854-764">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-764">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-765">Die Funktion `Func_spain_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-765">The function  `Func_spain_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-766">Ein Schlüsselwort `Keywords_spain_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-766">A keyword from  `Keywords_spain_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_driver's_license_number" />
          <Match idRef="Keywords_spain_eu_driver's_license_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7a854-767">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-767">Keywords</span></span>

<span data-ttu-id="7a854-768">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-768"></span></span>
|<span data-ttu-id="7a854-769">**Keywords_spain_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-769">**Keywords_spain_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-770">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-770">dlno#</span></span>  <br/> <span data-ttu-id="7a854-771">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-771">dl#</span></span>  <br/> <span data-ttu-id="7a854-772">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-772">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-773">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-773">driver licence</span></span>  <br/> <span data-ttu-id="7a854-774">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-774">driver license</span></span>  <br/> <span data-ttu-id="7a854-775">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-775">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-776">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-776">drivers license</span></span>  <br/> <span data-ttu-id="7a854-777">driver's licence</span><span class="sxs-lookup"><span data-stu-id="7a854-777">driver's licence</span></span>  <br/> <span data-ttu-id="7a854-778">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-778">driver's license</span></span>  <br/> <span data-ttu-id="7a854-779">Führerschein</span><span class="sxs-lookup"><span data-stu-id="7a854-779">driving licence</span></span>  <br/> <span data-ttu-id="7a854-780">driving license</span><span class="sxs-lookup"><span data-stu-id="7a854-780">driving license</span></span>  <br/> <span data-ttu-id="7a854-781">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-781">driver licence number</span></span>  <br/> <span data-ttu-id="7a854-782">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-782">driver license number</span></span>  <br/> <span data-ttu-id="7a854-783">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-783">drivers licence number</span></span>  <br/> <span data-ttu-id="7a854-784">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-784">drivers license number</span></span>  <br/> <span data-ttu-id="7a854-785">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-785">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-786">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-786">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-787">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-787">driving licence number</span></span>  <br/> <span data-ttu-id="7a854-788">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-788">driving license number</span></span>  <br/> <span data-ttu-id="7a854-789">Fahrerlaubnis</span><span class="sxs-lookup"><span data-stu-id="7a854-789">driving permit</span></span>  <br/> <span data-ttu-id="7a854-790">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-790">driving permit number</span></span>  <br/> <span data-ttu-id="7a854-791">Permiso de conducción</span><span class="sxs-lookup"><span data-stu-id="7a854-791">permiso de conducción</span></span>  <br/> <span data-ttu-id="7a854-792">Permiso conducción</span><span class="sxs-lookup"><span data-stu-id="7a854-792">permiso conducción</span></span>  <br/> <span data-ttu-id="7a854-793">número licencia Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-793">número licencia conducir</span></span>  <br/> <span data-ttu-id="7a854-794">número de carnet de Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-794">número de carnet de conducir</span></span>  <br/> <span data-ttu-id="7a854-795">número Carnet Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-795">número carnet conducir</span></span>  <br/> <span data-ttu-id="7a854-796">licencia Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-796">licencia conducir</span></span>  <br/> <span data-ttu-id="7a854-797">número de Permiso de Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-797">número de permiso de conducir</span></span>  <br/> <span data-ttu-id="7a854-798">número de Permiso Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-798">número de permiso conducir</span></span>  <br/> <span data-ttu-id="7a854-799">número Permiso Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-799">número permiso conducir</span></span>  <br/> <span data-ttu-id="7a854-800">Permiso Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-800">permiso conducir</span></span>  <br/> <span data-ttu-id="7a854-801">licencia de Manejo</span><span class="sxs-lookup"><span data-stu-id="7a854-801">licencia de manejo</span></span>  <br/> <span data-ttu-id="7a854-802">El Carnet de Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-802">el carnet de conducir</span></span>  <br/> <span data-ttu-id="7a854-803">Carnet Conducir</span><span class="sxs-lookup"><span data-stu-id="7a854-803">carnet conducir</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="7a854-804">Schweden</span><span class="sxs-lookup"><span data-stu-id="7a854-804">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="7a854-805">Format</span><span class="sxs-lookup"><span data-stu-id="7a854-805">Format</span></span>

<span data-ttu-id="7a854-806">Zehn Ziffern mit einem Bindestrich</span><span class="sxs-lookup"><span data-stu-id="7a854-806">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7a854-807">Muster</span><span class="sxs-lookup"><span data-stu-id="7a854-807">Pattern</span></span>

<span data-ttu-id="7a854-808">Zehn Ziffern mit einem Bindestrich:</span><span class="sxs-lookup"><span data-stu-id="7a854-808">Ten digits containing a hyphen:</span></span>
  
-  <span data-ttu-id="7a854-809">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-809">Six digits</span></span> 
    
- <span data-ttu-id="7a854-810">Ein Bindestrich</span><span class="sxs-lookup"><span data-stu-id="7a854-810">A hyphen</span></span>
    
- <span data-ttu-id="7a854-811">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="7a854-811">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7a854-812">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7a854-812">Checksum</span></span>

<span data-ttu-id="7a854-813">Nein</span><span class="sxs-lookup"><span data-stu-id="7a854-813">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7a854-814">Definition</span><span class="sxs-lookup"><span data-stu-id="7a854-814">Definition</span></span>

<span data-ttu-id="7a854-815">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7a854-815">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7a854-816">Der reguläre Ausdruck `Regex_sweden_eu_driver's_license_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7a854-816">The regular expression  `Regex_sweden_eu_driver's_license_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7a854-817">Ein Schlüsselwort `Keywords_sweden_eu_driver's_license_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7a854-817">A keyword from  `Keywords_sweden_eu_driver's_license_number` is found.</span></span> 
    
```
 <!-- EU Driver's License Number -->
<Entity id="b8fe86d1-c056-453b-bfaa-9fe698699ecc" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_sweden_eu_driver's_license_number" />
          <Match idRef="Keywords_sweden_eu_driver's_license_number" />
        </Pattern>
</Entity> 
```

### <a name="keywords"></a><span data-ttu-id="7a854-818">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7a854-818">Keywords</span></span>

<span data-ttu-id="7a854-819">| |</span><span class="sxs-lookup"><span data-stu-id="7a854-819"></span></span>
|<span data-ttu-id="7a854-820">**Keywords_sweden_eu_driver's_license_number**</span><span class="sxs-lookup"><span data-stu-id="7a854-820">**Keywords_sweden_eu_driver's_license_number**</span></span>|
|:-----|
|<span data-ttu-id="7a854-821">DL</span><span class="sxs-lookup"><span data-stu-id="7a854-821">dl#</span></span>  <br/> <span data-ttu-id="7a854-822">driver license</span><span class="sxs-lookup"><span data-stu-id="7a854-822">driver license</span></span>  <br/> <span data-ttu-id="7a854-823">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-823">driver license number</span></span>  <br/> <span data-ttu-id="7a854-824">Treiber Lizenz</span><span class="sxs-lookup"><span data-stu-id="7a854-824">driver licence</span></span>  <br/> <span data-ttu-id="7a854-825">Treiber lic.</span><span class="sxs-lookup"><span data-stu-id="7a854-825">drivers lic.</span></span>  <br/> <span data-ttu-id="7a854-826">drivers license</span><span class="sxs-lookup"><span data-stu-id="7a854-826">drivers license</span></span>  <br/> <span data-ttu-id="7a854-827">drivers licence</span><span class="sxs-lookup"><span data-stu-id="7a854-827">drivers licence</span></span>  <br/> <span data-ttu-id="7a854-828">driver's license</span><span class="sxs-lookup"><span data-stu-id="7a854-828">driver's license</span></span>  <br/> <span data-ttu-id="7a854-829">Treiber Lizenznummer</span><span class="sxs-lookup"><span data-stu-id="7a854-829">driver's license number</span></span>  <br/> <span data-ttu-id="7a854-830">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-830">driver's licence number</span></span>  <br/> <span data-ttu-id="7a854-831">Führerscheinnummer</span><span class="sxs-lookup"><span data-stu-id="7a854-831">driving license number</span></span>  <br/> <span data-ttu-id="7a854-832">dlno #</span><span class="sxs-lookup"><span data-stu-id="7a854-832">dlno#</span></span>  <br/> <span data-ttu-id="7a854-833">körkort</span><span class="sxs-lookup"><span data-stu-id="7a854-833">körkort</span></span>  <br/> |
   
## <a name="uk"></a><span data-ttu-id="7a854-834">UK</span><span class="sxs-lookup"><span data-stu-id="7a854-834">UK</span></span>

<span data-ttu-id="7a854-835">Weitere Informationen finden Sie im Abschnitt "U.K.</span><span class="sxs-lookup"><span data-stu-id="7a854-835">For details, see the section "U.K.</span></span> <span data-ttu-id="7a854-836">Lizenznummer des Treibers "in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7a854-836">Driver's License Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7a854-837">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a854-837">See also</span></span>

[<span data-ttu-id="7a854-838">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="7a854-838">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

