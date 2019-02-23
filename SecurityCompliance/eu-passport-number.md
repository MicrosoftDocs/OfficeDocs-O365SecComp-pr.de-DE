---
title: EU-Passport-Nummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Passport-Nummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: c46f683bd1baf651bcf13c1766dfff3cb953b341
ms.sourcegitcommit: f57b4001ef1327f0ea622e716a4d7d78f1769b49
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/23/2019
ms.locfileid: "30218265"
---
# <a name="eu-passport-number"></a><span data-ttu-id="26d68-104">EU-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="26d68-104">EU Passport Number</span></span>

<span data-ttu-id="26d68-p102">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Passport-Nummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="26d68-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="26d68-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="26d68-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="26d68-108">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-108">Format</span></span>

<span data-ttu-id="26d68-109">Ein Buchstabe gefolgt von einem optionalen Leerzeichen und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-110">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-110">Pattern</span></span>

<span data-ttu-id="26d68-111">Eine Kombination aus einem Buchstaben, sieben Ziffern und einem Leerzeichen:</span><span class="sxs-lookup"><span data-stu-id="26d68-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="26d68-112">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="26d68-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="26d68-113">Ein Leerzeichen (optional)</span><span class="sxs-lookup"><span data-stu-id="26d68-113">One space (optional)</span></span>
    
- <span data-ttu-id="26d68-114">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="26d68-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-115">Checksum</span></span>

<span data-ttu-id="26d68-116">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="26d68-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-117">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-117">Definition</span></span>

<span data-ttu-id="26d68-118">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-119">Der reguläre Ausdruck `Regex_austria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-120">Ein Schlüsselwort `Keywords_austria_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-121">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-121">Keywords</span></span>

<span data-ttu-id="26d68-122">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-122"></span></span>
|<span data-ttu-id="26d68-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-124">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-124">passport number</span></span>  <br/> <span data-ttu-id="26d68-125">Österreichische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-125">austrian passport number</span></span>  <br/> <span data-ttu-id="26d68-126">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-126">passport no</span></span>  <br/> <span data-ttu-id="26d68-127">Reisepass</span><span class="sxs-lookup"><span data-stu-id="26d68-127">reisepass</span></span>  <br/> <span data-ttu-id="26d68-128">österreichisch Reisepass</span><span class="sxs-lookup"><span data-stu-id="26d68-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="26d68-129">Belgien</span><span class="sxs-lookup"><span data-stu-id="26d68-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="26d68-130">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-130">Format</span></span>

<span data-ttu-id="26d68-131">Zwei Buchstaben, gefolgt von sechs Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-132">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-132">Pattern</span></span>

<span data-ttu-id="26d68-133">Zwei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-134">Checksum</span></span>

<span data-ttu-id="26d68-135">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="26d68-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-136">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-136">Definition</span></span>

<span data-ttu-id="26d68-137">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-138">Der reguläre Ausdruck `Regex_belgium_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-139">Ein Schlüsselwort `Keywords_belgium_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-140">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-140">Keywords</span></span>

<span data-ttu-id="26d68-141">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-141"></span></span>
|<span data-ttu-id="26d68-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-143">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-143">passport number</span></span>  <br/> <span data-ttu-id="26d68-144">belgische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-144">belgian passport number</span></span>  <br/> <span data-ttu-id="26d68-145">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-145">passport no</span></span>  <br/> <span data-ttu-id="26d68-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="26d68-146">paspoort</span></span>  <br/> <span data-ttu-id="26d68-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="26d68-148">Reisepass kein</span><span class="sxs-lookup"><span data-stu-id="26d68-148">reisepass kein</span></span>  <br/> <span data-ttu-id="26d68-149">Reisepass</span><span class="sxs-lookup"><span data-stu-id="26d68-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="26d68-150">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="26d68-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="26d68-151">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-151">Format</span></span>

<span data-ttu-id="26d68-152">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="26d68-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-153">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-153">Pattern</span></span>

 <span data-ttu-id="26d68-154">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="26d68-155">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-155">Checksum</span></span>

<span data-ttu-id="26d68-156">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-157">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-157">Definition</span></span>

<span data-ttu-id="26d68-158">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-159">Der reguläre Ausdruck `Regex_bulgaria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-160">Ein Schlüsselwort `Keywords_bulgaria_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-161">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-161">Keywords</span></span>

<span data-ttu-id="26d68-162">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-162"></span></span>
|<span data-ttu-id="26d68-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-164">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-164">passport number</span></span>  <br/> <span data-ttu-id="26d68-165">Bulgarische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="26d68-166">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-166">passport no</span></span>  <br/> <span data-ttu-id="26d68-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="26d68-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="26d68-168">Kroatien</span><span class="sxs-lookup"><span data-stu-id="26d68-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="26d68-169">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-169">Format</span></span>

<span data-ttu-id="26d68-170">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="26d68-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-171">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-171">Pattern</span></span>

 <span data-ttu-id="26d68-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="26d68-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-173">Checksum</span></span>

<span data-ttu-id="26d68-174">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-175">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-175">Definition</span></span>

<span data-ttu-id="26d68-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-177">Der reguläre Ausdruck `Regex_croatia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-178">Ein Schlüsselwort `Keywords_croatia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-179">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-179">Keywords</span></span>

<span data-ttu-id="26d68-180">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-180"></span></span>
|<span data-ttu-id="26d68-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-182">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-182">passport number</span></span>  <br/> <span data-ttu-id="26d68-183">Kroatische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-183">croatian passport number</span></span>  <br/> <span data-ttu-id="26d68-184">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-184">passport no</span></span>  <br/> <span data-ttu-id="26d68-185">Broj putovnice</span><span class="sxs-lookup"><span data-stu-id="26d68-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="26d68-186">Zypern</span><span class="sxs-lookup"><span data-stu-id="26d68-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="26d68-187">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-187">Format</span></span>

<span data-ttu-id="26d68-188">Ein Buchstabe, gefolgt von 6-8 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="26d68-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-189">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-189">Pattern</span></span>

<span data-ttu-id="26d68-190">Ein Buchstabe gefolgt von sechs bis acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-191">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-191">Checksum</span></span>

<span data-ttu-id="26d68-192">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-193">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-193">Definition</span></span>

<span data-ttu-id="26d68-194">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-195">Der reguläre Ausdruck `Regex_cyprus_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-196">Ein Schlüsselwort `Keywords_cyprus_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-197">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-197">Keywords</span></span>

<span data-ttu-id="26d68-198">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-198"></span></span>
|<span data-ttu-id="26d68-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-200">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-200">passport number</span></span>  <br/> <span data-ttu-id="26d68-201">Zypern-Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="26d68-202">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-202">passport no</span></span>  <br/> <span data-ttu-id="26d68-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="26d68-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="26d68-204">Tschechien</span><span class="sxs-lookup"><span data-stu-id="26d68-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="26d68-205">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-205">Format</span></span>

<span data-ttu-id="26d68-206">Acht Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="26d68-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-207">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-207">Pattern</span></span>

<span data-ttu-id="26d68-208">Acht Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="26d68-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-209">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-209">Checksum</span></span>

<span data-ttu-id="26d68-210">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-211">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-211">Definition</span></span>

<span data-ttu-id="26d68-212">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-213">Der reguläre Ausdruck `Regex_czech_republic_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-214">Ein Schlüsselwort `Keywords_czech_republic_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-215">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-215">Keywords</span></span>

<span data-ttu-id="26d68-216">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-216"></span></span>
|<span data-ttu-id="26d68-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-218">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-218">passport number</span></span>  <br/> <span data-ttu-id="26d68-219">Tschechische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-219">czech passport number</span></span>  <br/> <span data-ttu-id="26d68-220">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-220">passport no</span></span>  <br/> <span data-ttu-id="26d68-221">Cestovní Pas</span><span class="sxs-lookup"><span data-stu-id="26d68-221">cestovní pas</span></span>  <br/> <span data-ttu-id="26d68-222">Pas</span><span class="sxs-lookup"><span data-stu-id="26d68-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="26d68-223">Dänemark</span><span class="sxs-lookup"><span data-stu-id="26d68-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="26d68-224">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-224">Format</span></span>

<span data-ttu-id="26d68-225">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="26d68-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-226">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-226">Pattern</span></span>

 <span data-ttu-id="26d68-227">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="26d68-228">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-228">Checksum</span></span>

<span data-ttu-id="26d68-229">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-230">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-230">Definition</span></span>

<span data-ttu-id="26d68-231">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-232">Der reguläre Ausdruck `Regex_denmark_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-233">Ein Schlüsselwort `Keywords_denmark_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-234">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-234">Keywords</span></span>

<span data-ttu-id="26d68-235">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-235"></span></span>
|<span data-ttu-id="26d68-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-237">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-237">passport number</span></span>  <br/> <span data-ttu-id="26d68-238">dänische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-238">danish passport number</span></span>  <br/> <span data-ttu-id="26d68-239">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-239">passport no</span></span>  <br/> <span data-ttu-id="26d68-240">Pas</span><span class="sxs-lookup"><span data-stu-id="26d68-240">pas</span></span>  <br/> <span data-ttu-id="26d68-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="26d68-242">Estland</span><span class="sxs-lookup"><span data-stu-id="26d68-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="26d68-243">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-243">Format</span></span>

<span data-ttu-id="26d68-244">Ein Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-245">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-245">Pattern</span></span>

<span data-ttu-id="26d68-246">Ein Buchstabe gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-247">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-247">Checksum</span></span>

<span data-ttu-id="26d68-248">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-249">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-249">Definition</span></span>

<span data-ttu-id="26d68-250">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-251">Der reguläre Ausdruck `Regex_estonia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-252">Ein Schlüsselwort `Keywords_estonia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-253">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-253">Keywords</span></span>

<span data-ttu-id="26d68-254">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-254"></span></span>
|<span data-ttu-id="26d68-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-256">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-256">passport number</span></span>  <br/> <span data-ttu-id="26d68-257">Estnische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-257">estonian passport number</span></span>  <br/> <span data-ttu-id="26d68-258">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-258">passport no</span></span>  <br/> <span data-ttu-id="26d68-259">Eesti kodaniku-Durchlauf</span><span class="sxs-lookup"><span data-stu-id="26d68-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="26d68-260">Finnland</span><span class="sxs-lookup"><span data-stu-id="26d68-260">Finland</span></span>

<span data-ttu-id="26d68-261">Weitere Informationen finden Sie im Abschnitt "Finland Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="26d68-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="26d68-262">Frankreich</span><span class="sxs-lookup"><span data-stu-id="26d68-262">France</span></span>

<span data-ttu-id="26d68-263">Weitere Informationen finden Sie im Abschnitt "Frankreich Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="26d68-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="26d68-264">Deutschland</span><span class="sxs-lookup"><span data-stu-id="26d68-264">Germany</span></span>

<span data-ttu-id="26d68-265">Weitere Informationen finden Sie im Abschnitt "Deutschland Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="26d68-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="26d68-266">Griechenland</span><span class="sxs-lookup"><span data-stu-id="26d68-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="26d68-267">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-267">Format</span></span>

<span data-ttu-id="26d68-268">Zwei Buchstaben, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-269">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-269">Pattern</span></span>

<span data-ttu-id="26d68-270">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-271">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-271">Checksum</span></span>

<span data-ttu-id="26d68-272">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-273">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-273">Definition</span></span>

<span data-ttu-id="26d68-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-275">Der reguläre Ausdruck `Regex_greece_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-276">Ein Schlüsselwort `Keywords_greece_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-277">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-277">Keywords</span></span>

<span data-ttu-id="26d68-278">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-278"></span></span>
|<span data-ttu-id="26d68-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-280">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-280">passport number</span></span>  <br/> <span data-ttu-id="26d68-281">griechische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-281">greek passport number</span></span>  <br/> <span data-ttu-id="26d68-282">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-282">passport no</span></span>  <br/> <span data-ttu-id="26d68-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="26d68-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="26d68-284">Ungarn</span><span class="sxs-lookup"><span data-stu-id="26d68-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="26d68-285">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-285">Format</span></span>

<span data-ttu-id="26d68-286">Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-287">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-287">Pattern</span></span>

<span data-ttu-id="26d68-288">Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-289">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-289">Checksum</span></span>

<span data-ttu-id="26d68-290">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-291">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-291">Definition</span></span>

<span data-ttu-id="26d68-292">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-293">Der reguläre Ausdruck `Regex_hungary_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-294">Ein Schlüsselwort `Keywords_hungary_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-295">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-295">Keywords</span></span>

<span data-ttu-id="26d68-296">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-296"></span></span>
|<span data-ttu-id="26d68-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-298">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-298">passport number</span></span>  <br/> <span data-ttu-id="26d68-299">ungarische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="26d68-300">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-300">passport no</span></span>  <br/> <span data-ttu-id="26d68-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="26d68-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="26d68-302">Irland</span><span class="sxs-lookup"><span data-stu-id="26d68-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="26d68-303">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-303">Format</span></span>

<span data-ttu-id="26d68-304">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-305">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-305">Pattern</span></span>

<span data-ttu-id="26d68-306">Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="26d68-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="26d68-307">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="26d68-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="26d68-308">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="26d68-309">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-309">Checksum</span></span>

<span data-ttu-id="26d68-310">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-311">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-311">Definition</span></span>

<span data-ttu-id="26d68-312">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-313">Der reguläre Ausdruck `Regex_ireland_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-314">Ein Schlüsselwort `Keywords_ireland_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-315">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-315">Keywords</span></span>

<span data-ttu-id="26d68-316">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-316"></span></span>
|<span data-ttu-id="26d68-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-318">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-318">passport number</span></span>  <br/> <span data-ttu-id="26d68-319">irische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-319">irish passport number</span></span>  <br/> <span data-ttu-id="26d68-320">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-320">passport no</span></span>  <br/> <span data-ttu-id="26d68-321">Pas</span><span class="sxs-lookup"><span data-stu-id="26d68-321">pas</span></span>  <br/> <span data-ttu-id="26d68-322">passport</span><span class="sxs-lookup"><span data-stu-id="26d68-322">passport</span></span>  <br/> <span data-ttu-id="26d68-323">Passeport</span><span class="sxs-lookup"><span data-stu-id="26d68-323">passeport</span></span>  <br/> <span data-ttu-id="26d68-324">Passeport numero</span><span class="sxs-lookup"><span data-stu-id="26d68-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="26d68-325">Italien</span><span class="sxs-lookup"><span data-stu-id="26d68-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="26d68-326">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-326">Format</span></span>

<span data-ttu-id="26d68-327">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-328">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-328">Pattern</span></span>

<span data-ttu-id="26d68-329">Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="26d68-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="26d68-330">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="26d68-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="26d68-331">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="26d68-332">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-332">Checksum</span></span>

<span data-ttu-id="26d68-333">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="26d68-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-334">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-334">Definition</span></span>

<span data-ttu-id="26d68-335">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-336">Der reguläre Ausdruck `Regex_italy_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-337">Ein Schlüsselwort `Keywords_italy_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-338">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-338">Keywords</span></span>

<span data-ttu-id="26d68-339">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-339"></span></span>
|<span data-ttu-id="26d68-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-341">italienische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-341">italian passport number</span></span>  <br/> <span data-ttu-id="26d68-342">Repubblica Italiana Passa Porto</span><span class="sxs-lookup"><span data-stu-id="26d68-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="26d68-343">Passa Porto</span><span class="sxs-lookup"><span data-stu-id="26d68-343">passaporto</span></span>  <br/> <span data-ttu-id="26d68-344">Passa Porto Italiana</span><span class="sxs-lookup"><span data-stu-id="26d68-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="26d68-345">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-345">passport number</span></span>  <br/> <span data-ttu-id="26d68-346">Italiana Passa Porto numero</span><span class="sxs-lookup"><span data-stu-id="26d68-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="26d68-347">Passa Porto numero</span><span class="sxs-lookup"><span data-stu-id="26d68-347">passaporto numero</span></span>  <br/> <span data-ttu-id="26d68-348">Numéro Passeport Italien</span><span class="sxs-lookup"><span data-stu-id="26d68-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="26d68-349">Numéro Passeport</span><span class="sxs-lookup"><span data-stu-id="26d68-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="26d68-350">Lettland</span><span class="sxs-lookup"><span data-stu-id="26d68-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="26d68-351">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-351">Format</span></span>

<span data-ttu-id="26d68-352">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-353">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-353">Pattern</span></span>

<span data-ttu-id="26d68-354">Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="26d68-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="26d68-355">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="26d68-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="26d68-356">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="26d68-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-357">Checksum</span></span>

<span data-ttu-id="26d68-358">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-359">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-359">Definition</span></span>

<span data-ttu-id="26d68-360">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-361">Der reguläre Ausdruck `Regex_latvia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-362">Ein Schlüsselwort `Keywords_latvia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-363">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-363">Keywords</span></span>

<span data-ttu-id="26d68-364">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-364"></span></span>
|<span data-ttu-id="26d68-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-366">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-366">passport number</span></span>  <br/> <span data-ttu-id="26d68-367">Lettische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-367">latvian passport number</span></span>  <br/> <span data-ttu-id="26d68-368">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-368">passport no</span></span>  <br/> <span data-ttu-id="26d68-369">Pase numurs</span><span class="sxs-lookup"><span data-stu-id="26d68-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="26d68-370">Litauen</span><span class="sxs-lookup"><span data-stu-id="26d68-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="26d68-371">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-371">Format</span></span>

<span data-ttu-id="26d68-372">Acht Ziffern oder Buchstaben ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-373">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-373">Pattern</span></span>

<span data-ttu-id="26d68-374">Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="26d68-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-375">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-375">Checksum</span></span>

<span data-ttu-id="26d68-376">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="26d68-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-377">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-377">Definition</span></span>

<span data-ttu-id="26d68-378">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-379">Der reguläre Ausdruck `Regex_lithuania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-380">Ein Schlüsselwort `Keywords_lithuania_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-381">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-381">Keywords</span></span>

<span data-ttu-id="26d68-382">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-382"></span></span>
|<span data-ttu-id="26d68-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-384">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-384">passport number</span></span>  <br/> <span data-ttu-id="26d68-385">lithunian-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="26d68-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="26d68-386">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-386">passport no</span></span>  <br/> <span data-ttu-id="26d68-387">Paso Numeris</span><span class="sxs-lookup"><span data-stu-id="26d68-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="26d68-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="26d68-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="26d68-389">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-389">Format</span></span>

<span data-ttu-id="26d68-390">Acht Ziffern oder Buchstaben ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-391">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-391">Pattern</span></span>

<span data-ttu-id="26d68-392">Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="26d68-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-393">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-393">Checksum</span></span>

<span data-ttu-id="26d68-394">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-395">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-395">Definition</span></span>

<span data-ttu-id="26d68-396">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-397">Der reguläre Ausdruck `Regex_nation_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-398">Ein Schlüsselwort `Keywords_nation_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-399">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-399">Keywords</span></span>

<span data-ttu-id="26d68-400">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-400"></span></span>
|<span data-ttu-id="26d68-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-402">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-402">passport number</span></span>  <br/> <span data-ttu-id="26d68-403">Lettische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-403">latvian passport number</span></span>  <br/> <span data-ttu-id="26d68-404">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-404">passport no</span></span>  <br/> <span data-ttu-id="26d68-405">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="26d68-406">Malta</span><span class="sxs-lookup"><span data-stu-id="26d68-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="26d68-407">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-407">Format</span></span>

<span data-ttu-id="26d68-408">Sieben Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="26d68-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-409">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-409">Pattern</span></span>

 <span data-ttu-id="26d68-410">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="26d68-411">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-411">Checksum</span></span>

<span data-ttu-id="26d68-412">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-413">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-413">Definition</span></span>

<span data-ttu-id="26d68-414">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-415">Der reguläre Ausdruck `Regex_malta_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-416">Ein Schlüsselwort `Keywords_malta_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-417">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-417">Keywords</span></span>

<span data-ttu-id="26d68-418">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-418"></span></span>
|<span data-ttu-id="26d68-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-420">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-420">passport number</span></span>  <br/> <span data-ttu-id="26d68-421">Maltesische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-421">maltese passport number</span></span>  <br/> <span data-ttu-id="26d68-422">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-422">passport no</span></span>  <br/> <span data-ttu-id="26d68-423">numru Tal-Passaport</span><span class="sxs-lookup"><span data-stu-id="26d68-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="26d68-424">Niederlande</span><span class="sxs-lookup"><span data-stu-id="26d68-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="26d68-425">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-425">Format</span></span>

<span data-ttu-id="26d68-426">Neun Buchstaben oder Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="26d68-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-427">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-427">Pattern</span></span>

<span data-ttu-id="26d68-428">Neun Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-429">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-429">Checksum</span></span>

<span data-ttu-id="26d68-430">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="26d68-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-431">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-431">Definition</span></span>

<span data-ttu-id="26d68-432">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-433">Der reguläre Ausdruck `Regex_netherlands_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-434">Ein Schlüsselwort `Keywords_netherlands_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-435">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-435">Keywords</span></span>

<span data-ttu-id="26d68-436">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-436"></span></span>
|<span data-ttu-id="26d68-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-438">niederländische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-438">dutch passport number</span></span>  <br/> <span data-ttu-id="26d68-439">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-439">passport number</span></span>  <br/> <span data-ttu-id="26d68-440">niederländische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="26d68-441">Nederlanden paspoort Nummer</span><span class="sxs-lookup"><span data-stu-id="26d68-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="26d68-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="26d68-442">paspoort</span></span>  <br/> <span data-ttu-id="26d68-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="26d68-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="26d68-445">Polen</span><span class="sxs-lookup"><span data-stu-id="26d68-445">Poland</span></span>

<span data-ttu-id="26d68-446">Weitere Informationen finden Sie im Abschnitt "polnische Passnummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="26d68-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="26d68-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="26d68-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="26d68-448">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-448">Format</span></span>

<span data-ttu-id="26d68-449">Ein Buchstaben, gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-450">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-450">Pattern</span></span>

<span data-ttu-id="26d68-451">Ein Buchstabe gefolgt von sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="26d68-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="26d68-452">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="26d68-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="26d68-453">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="26d68-454">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-454">Checksum</span></span>

<span data-ttu-id="26d68-455">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-456">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-456">Definition</span></span>

<span data-ttu-id="26d68-457">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-458">Der reguläre Ausdruck `Regex_portugal_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-459">Ein Schlüsselwort `Keywords_portugal_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-460">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-460">Keywords</span></span>

<span data-ttu-id="26d68-461">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-461"></span></span>
|<span data-ttu-id="26d68-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-463">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-463">passport number</span></span>  <br/> <span data-ttu-id="26d68-464">portugiesische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="26d68-465">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-465">passport no</span></span>  <br/> <span data-ttu-id="26d68-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="26d68-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="26d68-467">Rumänien</span><span class="sxs-lookup"><span data-stu-id="26d68-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="26d68-468">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-468">Format</span></span>

<span data-ttu-id="26d68-469">Acht oder neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="26d68-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-470">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-470">Pattern</span></span>

<span data-ttu-id="26d68-471">Acht oder neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-472">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-472">Checksum</span></span>

<span data-ttu-id="26d68-473">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-474">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-474">Definition</span></span>

<span data-ttu-id="26d68-475">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-476">Der reguläre Ausdruck `Regex_romania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-477">Ein Schlüsselwort `Keywords_romania_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-478">Keywords</span></span>

<span data-ttu-id="26d68-479">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-479"></span></span>
|<span data-ttu-id="26d68-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-481">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-481">passport number</span></span>  <br/> <span data-ttu-id="26d68-482">rumänische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-482">romanian passport number</span></span>  <br/> <span data-ttu-id="26d68-483">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-483">passport no</span></span>  <br/> <span data-ttu-id="26d68-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="26d68-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="26d68-485">Slowakei</span><span class="sxs-lookup"><span data-stu-id="26d68-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="26d68-486">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-486">Format</span></span>

<span data-ttu-id="26d68-487">Eine Ziffer oder ein Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-488">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-488">Pattern</span></span>

<span data-ttu-id="26d68-489">Eine Ziffer oder ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="26d68-490">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-490">Checksum</span></span>

<span data-ttu-id="26d68-491">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-492">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-492">Definition</span></span>

<span data-ttu-id="26d68-493">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-494">Der reguläre Ausdruck `Regex_slovakia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-495">Ein Schlüsselwort `Keywords_slovakia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-496">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-496">Keywords</span></span>

<span data-ttu-id="26d68-497">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-497"></span></span>
|<span data-ttu-id="26d68-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-499">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-499">passport number</span></span>  <br/> <span data-ttu-id="26d68-500">Slowakische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="26d68-501">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-501">passport no</span></span>  <br/> <span data-ttu-id="26d68-502">číslo Pasu</span><span class="sxs-lookup"><span data-stu-id="26d68-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="26d68-503">Slowenien</span><span class="sxs-lookup"><span data-stu-id="26d68-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="26d68-504">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-504">Format</span></span>

<span data-ttu-id="26d68-505">Zwei Buchstaben, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-506">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-506">Pattern</span></span>

<span data-ttu-id="26d68-507">Zwei Buchstaben, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="26d68-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="26d68-508">Der Buchstabe "P"</span><span class="sxs-lookup"><span data-stu-id="26d68-508">The letter "P"</span></span>
    
- <span data-ttu-id="26d68-509">Ein Großbuchstabe</span><span class="sxs-lookup"><span data-stu-id="26d68-509">One uppercase letter</span></span>
    
- <span data-ttu-id="26d68-510">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="26d68-511">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-511">Checksum</span></span>

<span data-ttu-id="26d68-512">Nein</span><span class="sxs-lookup"><span data-stu-id="26d68-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-513">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-513">Definition</span></span>

<span data-ttu-id="26d68-514">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-515">Der reguläre Ausdruck `Regex_slovenia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-516">Ein Schlüsselwort `Keywords_slovenia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-517">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-517">Keywords</span></span>

<span data-ttu-id="26d68-518">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-518"></span></span>
|<span data-ttu-id="26d68-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-520">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-520">passport number</span></span>  <br/> <span data-ttu-id="26d68-521">slowenische Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="26d68-522">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-522">passport no</span></span>  <br/> <span data-ttu-id="26d68-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="26d68-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="26d68-524">Spanien</span><span class="sxs-lookup"><span data-stu-id="26d68-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="26d68-525">Format</span><span class="sxs-lookup"><span data-stu-id="26d68-525">Format</span></span>

<span data-ttu-id="26d68-526">Eine acht-oder neunstellige Kombination aus Buchstaben und Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="26d68-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="26d68-527">Muster</span><span class="sxs-lookup"><span data-stu-id="26d68-527">Pattern</span></span>

<span data-ttu-id="26d68-528">Eine Kombination aus Buchstaben und Zahlen mit acht oder neun Zeichen:</span><span class="sxs-lookup"><span data-stu-id="26d68-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="26d68-529">Zwei Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="26d68-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="26d68-530">Eine Ziffer oder ein Buchstabe (optional)</span><span class="sxs-lookup"><span data-stu-id="26d68-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="26d68-531">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="26d68-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="26d68-532">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="26d68-532">Checksum</span></span>

<span data-ttu-id="26d68-533">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="26d68-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="26d68-534">Definition</span><span class="sxs-lookup"><span data-stu-id="26d68-534">Definition</span></span>

<span data-ttu-id="26d68-535">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="26d68-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="26d68-536">Der reguläre Ausdruck `Regex_spain_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="26d68-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="26d68-537">Ein Schlüsselwort `Keywords_spain_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="26d68-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="26d68-538">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="26d68-538">Keywords</span></span>

<span data-ttu-id="26d68-539">| |</span><span class="sxs-lookup"><span data-stu-id="26d68-539"></span></span>
|<span data-ttu-id="26d68-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="26d68-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="26d68-541">passport</span><span class="sxs-lookup"><span data-stu-id="26d68-541">passport</span></span>  <br/> <span data-ttu-id="26d68-542">Spanien Passport</span><span class="sxs-lookup"><span data-stu-id="26d68-542">spain passport</span></span>  <br/> <span data-ttu-id="26d68-543">Passport-Buch</span><span class="sxs-lookup"><span data-stu-id="26d68-543">passport book</span></span>  <br/> <span data-ttu-id="26d68-544">Passnummer</span><span class="sxs-lookup"><span data-stu-id="26d68-544">passport number</span></span>  <br/> <span data-ttu-id="26d68-545">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="26d68-545">passport no</span></span>  <br/> <span data-ttu-id="26d68-546">Libreta Pasaporte</span><span class="sxs-lookup"><span data-stu-id="26d68-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="26d68-547">número Pasaporte</span><span class="sxs-lookup"><span data-stu-id="26d68-547">número pasaporte</span></span>  <br/> <span data-ttu-id="26d68-548">ESPAÑA PASAPORTE</span><span class="sxs-lookup"><span data-stu-id="26d68-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="26d68-549">Pasaporte</span><span class="sxs-lookup"><span data-stu-id="26d68-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="26d68-550">Schweden</span><span class="sxs-lookup"><span data-stu-id="26d68-550">Sweden</span></span>

<span data-ttu-id="26d68-551">Weitere Informationen finden Sie im Abschnitt "schwedische Passport-Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="26d68-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="26d68-552">UK</span><span class="sxs-lookup"><span data-stu-id="26d68-552">UK</span></span>

<span data-ttu-id="26d68-p103">Weitere Informationen finden Sie im Abschnitt "U.S./UK Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="26d68-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="26d68-555">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26d68-555">See also</span></span>

[<span data-ttu-id="26d68-556">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="26d68-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

