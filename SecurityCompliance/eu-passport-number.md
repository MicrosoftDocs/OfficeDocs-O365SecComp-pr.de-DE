---
title: EU-Passport-Nummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Passport-Nummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 3ab92e87607f41cffa8c15f1179a4eef5369cb29
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32256823"
---
# <a name="eu-passport-number"></a><span data-ttu-id="95180-104">EU-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="95180-104">EU Passport Number</span></span>

<span data-ttu-id="95180-105">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Passport-Nummer erkennt.</span><span class="sxs-lookup"><span data-stu-id="95180-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="95180-106">Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="95180-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="95180-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="95180-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="95180-108">Format</span><span class="sxs-lookup"><span data-stu-id="95180-108">Format</span></span>

<span data-ttu-id="95180-109">Ein Buchstabe gefolgt von einem optionalen Leerzeichen und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-110">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-110">Pattern</span></span>

<span data-ttu-id="95180-111">Eine Kombination aus einem Buchstaben, sieben Ziffern und einem Leerzeichen:</span><span class="sxs-lookup"><span data-stu-id="95180-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="95180-112">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="95180-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="95180-113">Ein Leerzeichen (optional)</span><span class="sxs-lookup"><span data-stu-id="95180-113">One space (optional)</span></span>
    
- <span data-ttu-id="95180-114">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95180-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-115">Checksum</span></span>

<span data-ttu-id="95180-116">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="95180-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-117">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-117">Definition</span></span>

<span data-ttu-id="95180-118">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-119">Der reguläre Ausdruck `Regex_austria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-120">Ein Schlüsselwort `Keywords_austria_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-121">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-121">Keywords</span></span>

<span data-ttu-id="95180-122">| |</span><span class="sxs-lookup"><span data-stu-id="95180-122"></span></span>
|<span data-ttu-id="95180-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-124">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-124">passport number</span></span>  <br/> <span data-ttu-id="95180-125">Österreichische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-125">austrian passport number</span></span>  <br/> <span data-ttu-id="95180-126">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-126">passport no</span></span>  <br/> <span data-ttu-id="95180-127">Reisepass</span><span class="sxs-lookup"><span data-stu-id="95180-127">reisepass</span></span>  <br/> <span data-ttu-id="95180-128">österreichisch Reisepass</span><span class="sxs-lookup"><span data-stu-id="95180-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="95180-129">Belgien</span><span class="sxs-lookup"><span data-stu-id="95180-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="95180-130">Format</span><span class="sxs-lookup"><span data-stu-id="95180-130">Format</span></span>

<span data-ttu-id="95180-131">Zwei Buchstaben, gefolgt von sechs Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-132">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-132">Pattern</span></span>

<span data-ttu-id="95180-133">Zwei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-134">Checksum</span></span>

<span data-ttu-id="95180-135">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="95180-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-136">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-136">Definition</span></span>

<span data-ttu-id="95180-137">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-138">Der reguläre Ausdruck `Regex_belgium_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-139">Ein Schlüsselwort `Keywords_belgium_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-140">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-140">Keywords</span></span>

<span data-ttu-id="95180-141">| |</span><span class="sxs-lookup"><span data-stu-id="95180-141"></span></span>
|<span data-ttu-id="95180-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-143">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-143">passport number</span></span>  <br/> <span data-ttu-id="95180-144">belgische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-144">belgian passport number</span></span>  <br/> <span data-ttu-id="95180-145">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-145">passport no</span></span>  <br/> <span data-ttu-id="95180-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="95180-146">paspoort</span></span>  <br/> <span data-ttu-id="95180-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="95180-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="95180-148">Reisepass kein</span><span class="sxs-lookup"><span data-stu-id="95180-148">reisepass kein</span></span>  <br/> <span data-ttu-id="95180-149">Reisepass</span><span class="sxs-lookup"><span data-stu-id="95180-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="95180-150">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="95180-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="95180-151">Format</span><span class="sxs-lookup"><span data-stu-id="95180-151">Format</span></span>

<span data-ttu-id="95180-152">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="95180-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-153">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-153">Pattern</span></span>

 <span data-ttu-id="95180-154">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="95180-155">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-155">Checksum</span></span>

<span data-ttu-id="95180-156">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-157">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-157">Definition</span></span>

<span data-ttu-id="95180-158">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-159">Der reguläre Ausdruck `Regex_bulgaria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-160">Ein Schlüsselwort `Keywords_bulgaria_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-161">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-161">Keywords</span></span>

<span data-ttu-id="95180-162">| |</span><span class="sxs-lookup"><span data-stu-id="95180-162"></span></span>
|<span data-ttu-id="95180-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-164">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-164">passport number</span></span>  <br/> <span data-ttu-id="95180-165">Bulgarische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="95180-166">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-166">passport no</span></span>  <br/> <span data-ttu-id="95180-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="95180-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="95180-168">Kroatien</span><span class="sxs-lookup"><span data-stu-id="95180-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="95180-169">Format</span><span class="sxs-lookup"><span data-stu-id="95180-169">Format</span></span>

<span data-ttu-id="95180-170">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="95180-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-171">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-171">Pattern</span></span>

 <span data-ttu-id="95180-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="95180-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-173">Checksum</span></span>

<span data-ttu-id="95180-174">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-175">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-175">Definition</span></span>

<span data-ttu-id="95180-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-177">Der reguläre Ausdruck `Regex_croatia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-178">Ein Schlüsselwort `Keywords_croatia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-179">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-179">Keywords</span></span>

<span data-ttu-id="95180-180">| |</span><span class="sxs-lookup"><span data-stu-id="95180-180"></span></span>
|<span data-ttu-id="95180-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-182">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-182">passport number</span></span>  <br/> <span data-ttu-id="95180-183">Kroatische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-183">croatian passport number</span></span>  <br/> <span data-ttu-id="95180-184">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-184">passport no</span></span>  <br/> <span data-ttu-id="95180-185">Broj putovnice</span><span class="sxs-lookup"><span data-stu-id="95180-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="95180-186">Zypern</span><span class="sxs-lookup"><span data-stu-id="95180-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="95180-187">Format</span><span class="sxs-lookup"><span data-stu-id="95180-187">Format</span></span>

<span data-ttu-id="95180-188">Ein Buchstabe, gefolgt von 6-8 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="95180-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-189">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-189">Pattern</span></span>

<span data-ttu-id="95180-190">Ein Buchstabe gefolgt von sechs bis acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-191">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-191">Checksum</span></span>

<span data-ttu-id="95180-192">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-193">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-193">Definition</span></span>

<span data-ttu-id="95180-194">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-195">Der reguläre Ausdruck `Regex_cyprus_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-196">Ein Schlüsselwort `Keywords_cyprus_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-197">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-197">Keywords</span></span>

<span data-ttu-id="95180-198">| |</span><span class="sxs-lookup"><span data-stu-id="95180-198"></span></span>
|<span data-ttu-id="95180-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-200">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-200">passport number</span></span>  <br/> <span data-ttu-id="95180-201">Zypern-Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="95180-202">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-202">passport no</span></span>  <br/> <span data-ttu-id="95180-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="95180-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="95180-204">Tschechien</span><span class="sxs-lookup"><span data-stu-id="95180-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="95180-205">Format</span><span class="sxs-lookup"><span data-stu-id="95180-205">Format</span></span>

<span data-ttu-id="95180-206">Acht Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="95180-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-207">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-207">Pattern</span></span>

<span data-ttu-id="95180-208">Acht Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="95180-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-209">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-209">Checksum</span></span>

<span data-ttu-id="95180-210">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-211">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-211">Definition</span></span>

<span data-ttu-id="95180-212">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-213">Der reguläre Ausdruck `Regex_czech_republic_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-214">Ein Schlüsselwort `Keywords_czech_republic_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-215">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-215">Keywords</span></span>

<span data-ttu-id="95180-216">| |</span><span class="sxs-lookup"><span data-stu-id="95180-216"></span></span>
|<span data-ttu-id="95180-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-218">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-218">passport number</span></span>  <br/> <span data-ttu-id="95180-219">Tschechische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-219">czech passport number</span></span>  <br/> <span data-ttu-id="95180-220">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-220">passport no</span></span>  <br/> <span data-ttu-id="95180-221">Cestovní Pas</span><span class="sxs-lookup"><span data-stu-id="95180-221">cestovní pas</span></span>  <br/> <span data-ttu-id="95180-222">Pas</span><span class="sxs-lookup"><span data-stu-id="95180-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="95180-223">Dänemark</span><span class="sxs-lookup"><span data-stu-id="95180-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="95180-224">Format</span><span class="sxs-lookup"><span data-stu-id="95180-224">Format</span></span>

<span data-ttu-id="95180-225">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="95180-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-226">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-226">Pattern</span></span>

 <span data-ttu-id="95180-227">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="95180-228">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-228">Checksum</span></span>

<span data-ttu-id="95180-229">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-230">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-230">Definition</span></span>

<span data-ttu-id="95180-231">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-232">Der reguläre Ausdruck `Regex_denmark_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-233">Ein Schlüsselwort `Keywords_denmark_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-234">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-234">Keywords</span></span>

<span data-ttu-id="95180-235">| |</span><span class="sxs-lookup"><span data-stu-id="95180-235"></span></span>
|<span data-ttu-id="95180-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-237">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-237">passport number</span></span>  <br/> <span data-ttu-id="95180-238">dänische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-238">danish passport number</span></span>  <br/> <span data-ttu-id="95180-239">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-239">passport no</span></span>  <br/> <span data-ttu-id="95180-240">Pas</span><span class="sxs-lookup"><span data-stu-id="95180-240">pas</span></span>  <br/> <span data-ttu-id="95180-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="95180-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="95180-242">Estland</span><span class="sxs-lookup"><span data-stu-id="95180-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="95180-243">Format</span><span class="sxs-lookup"><span data-stu-id="95180-243">Format</span></span>

<span data-ttu-id="95180-244">Ein Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-245">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-245">Pattern</span></span>

<span data-ttu-id="95180-246">Ein Buchstabe gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-247">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-247">Checksum</span></span>

<span data-ttu-id="95180-248">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-249">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-249">Definition</span></span>

<span data-ttu-id="95180-250">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-251">Der reguläre Ausdruck `Regex_estonia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-252">Ein Schlüsselwort `Keywords_estonia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-253">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-253">Keywords</span></span>

<span data-ttu-id="95180-254">| |</span><span class="sxs-lookup"><span data-stu-id="95180-254"></span></span>
|<span data-ttu-id="95180-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-256">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-256">passport number</span></span>  <br/> <span data-ttu-id="95180-257">Estnische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-257">estonian passport number</span></span>  <br/> <span data-ttu-id="95180-258">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-258">passport no</span></span>  <br/> <span data-ttu-id="95180-259">Eesti kodaniku-Durchlauf</span><span class="sxs-lookup"><span data-stu-id="95180-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="95180-260">Finnland</span><span class="sxs-lookup"><span data-stu-id="95180-260">Finland</span></span>

<span data-ttu-id="95180-261">Weitere Informationen finden Sie im Abschnitt "Finland Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95180-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="95180-262">Frankreich</span><span class="sxs-lookup"><span data-stu-id="95180-262">France</span></span>

<span data-ttu-id="95180-263">Weitere Informationen finden Sie im Abschnitt "Frankreich Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95180-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="95180-264">Deutschland</span><span class="sxs-lookup"><span data-stu-id="95180-264">Germany</span></span>

<span data-ttu-id="95180-265">Weitere Informationen finden Sie im Abschnitt "Deutschland Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95180-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="95180-266">Griechenland</span><span class="sxs-lookup"><span data-stu-id="95180-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="95180-267">Format</span><span class="sxs-lookup"><span data-stu-id="95180-267">Format</span></span>

<span data-ttu-id="95180-268">Zwei Buchstaben, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-269">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-269">Pattern</span></span>

<span data-ttu-id="95180-270">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-271">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-271">Checksum</span></span>

<span data-ttu-id="95180-272">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-273">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-273">Definition</span></span>

<span data-ttu-id="95180-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-275">Der reguläre Ausdruck `Regex_greece_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-276">Ein Schlüsselwort `Keywords_greece_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-277">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-277">Keywords</span></span>

<span data-ttu-id="95180-278">| |</span><span class="sxs-lookup"><span data-stu-id="95180-278"></span></span>
|<span data-ttu-id="95180-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-280">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-280">passport number</span></span>  <br/> <span data-ttu-id="95180-281">griechische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-281">greek passport number</span></span>  <br/> <span data-ttu-id="95180-282">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-282">passport no</span></span>  <br/> <span data-ttu-id="95180-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="95180-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="95180-284">Ungarn</span><span class="sxs-lookup"><span data-stu-id="95180-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="95180-285">Format</span><span class="sxs-lookup"><span data-stu-id="95180-285">Format</span></span>

<span data-ttu-id="95180-286">Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-287">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-287">Pattern</span></span>

<span data-ttu-id="95180-288">Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-289">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-289">Checksum</span></span>

<span data-ttu-id="95180-290">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-291">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-291">Definition</span></span>

<span data-ttu-id="95180-292">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-293">Der reguläre Ausdruck `Regex_hungary_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-294">Ein Schlüsselwort `Keywords_hungary_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-295">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-295">Keywords</span></span>

<span data-ttu-id="95180-296">| |</span><span class="sxs-lookup"><span data-stu-id="95180-296"></span></span>
|<span data-ttu-id="95180-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-298">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-298">passport number</span></span>  <br/> <span data-ttu-id="95180-299">ungarische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="95180-300">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-300">passport no</span></span>  <br/> <span data-ttu-id="95180-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="95180-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="95180-302">Irland</span><span class="sxs-lookup"><span data-stu-id="95180-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="95180-303">Format</span><span class="sxs-lookup"><span data-stu-id="95180-303">Format</span></span>

<span data-ttu-id="95180-304">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-305">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-305">Pattern</span></span>

<span data-ttu-id="95180-306">Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="95180-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="95180-307">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="95180-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="95180-308">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95180-309">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-309">Checksum</span></span>

<span data-ttu-id="95180-310">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-311">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-311">Definition</span></span>

<span data-ttu-id="95180-312">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-313">Der reguläre Ausdruck `Regex_ireland_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-314">Ein Schlüsselwort `Keywords_ireland_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-315">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-315">Keywords</span></span>

<span data-ttu-id="95180-316">| |</span><span class="sxs-lookup"><span data-stu-id="95180-316"></span></span>
|<span data-ttu-id="95180-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-318">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-318">passport number</span></span>  <br/> <span data-ttu-id="95180-319">irische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-319">irish passport number</span></span>  <br/> <span data-ttu-id="95180-320">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-320">passport no</span></span>  <br/> <span data-ttu-id="95180-321">Pas</span><span class="sxs-lookup"><span data-stu-id="95180-321">pas</span></span>  <br/> <span data-ttu-id="95180-322">Pass</span><span class="sxs-lookup"><span data-stu-id="95180-322">passport</span></span>  <br/> <span data-ttu-id="95180-323">Passeport</span><span class="sxs-lookup"><span data-stu-id="95180-323">passeport</span></span>  <br/> <span data-ttu-id="95180-324">Passeport numero</span><span class="sxs-lookup"><span data-stu-id="95180-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="95180-325">Italien</span><span class="sxs-lookup"><span data-stu-id="95180-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="95180-326">Format</span><span class="sxs-lookup"><span data-stu-id="95180-326">Format</span></span>

<span data-ttu-id="95180-327">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-328">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-328">Pattern</span></span>

<span data-ttu-id="95180-329">Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="95180-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="95180-330">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="95180-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="95180-331">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95180-332">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-332">Checksum</span></span>

<span data-ttu-id="95180-333">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="95180-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-334">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-334">Definition</span></span>

<span data-ttu-id="95180-335">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-336">Der reguläre Ausdruck `Regex_italy_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-337">Ein Schlüsselwort `Keywords_italy_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-338">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-338">Keywords</span></span>

<span data-ttu-id="95180-339">| |</span><span class="sxs-lookup"><span data-stu-id="95180-339"></span></span>
|<span data-ttu-id="95180-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-341">italienische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-341">italian passport number</span></span>  <br/> <span data-ttu-id="95180-342">Repubblica Italiana Passa Porto</span><span class="sxs-lookup"><span data-stu-id="95180-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="95180-343">Passa Porto</span><span class="sxs-lookup"><span data-stu-id="95180-343">passaporto</span></span>  <br/> <span data-ttu-id="95180-344">Passa Porto Italiana</span><span class="sxs-lookup"><span data-stu-id="95180-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="95180-345">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-345">passport number</span></span>  <br/> <span data-ttu-id="95180-346">Italiana Passa Porto numero</span><span class="sxs-lookup"><span data-stu-id="95180-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="95180-347">Passa Porto numero</span><span class="sxs-lookup"><span data-stu-id="95180-347">passaporto numero</span></span>  <br/> <span data-ttu-id="95180-348">Numéro Passeport Italien</span><span class="sxs-lookup"><span data-stu-id="95180-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="95180-349">Numéro Passeport</span><span class="sxs-lookup"><span data-stu-id="95180-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="95180-350">Lettland</span><span class="sxs-lookup"><span data-stu-id="95180-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="95180-351">Format</span><span class="sxs-lookup"><span data-stu-id="95180-351">Format</span></span>

<span data-ttu-id="95180-352">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-353">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-353">Pattern</span></span>

<span data-ttu-id="95180-354">Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="95180-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="95180-355">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="95180-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="95180-356">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95180-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-357">Checksum</span></span>

<span data-ttu-id="95180-358">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-359">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-359">Definition</span></span>

<span data-ttu-id="95180-360">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-361">Der reguläre Ausdruck `Regex_latvia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-362">Ein Schlüsselwort `Keywords_latvia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-363">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-363">Keywords</span></span>

<span data-ttu-id="95180-364">| |</span><span class="sxs-lookup"><span data-stu-id="95180-364"></span></span>
|<span data-ttu-id="95180-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-366">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-366">passport number</span></span>  <br/> <span data-ttu-id="95180-367">Lettische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-367">latvian passport number</span></span>  <br/> <span data-ttu-id="95180-368">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-368">passport no</span></span>  <br/> <span data-ttu-id="95180-369">Pase numurs</span><span class="sxs-lookup"><span data-stu-id="95180-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="95180-370">Litauen</span><span class="sxs-lookup"><span data-stu-id="95180-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="95180-371">Format</span><span class="sxs-lookup"><span data-stu-id="95180-371">Format</span></span>

<span data-ttu-id="95180-372">Acht Ziffern oder Buchstaben ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-373">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-373">Pattern</span></span>

<span data-ttu-id="95180-374">Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="95180-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-375">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-375">Checksum</span></span>

<span data-ttu-id="95180-376">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="95180-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-377">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-377">Definition</span></span>

<span data-ttu-id="95180-378">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-379">Der reguläre Ausdruck `Regex_lithuania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-380">Ein Schlüsselwort `Keywords_lithuania_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-381">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-381">Keywords</span></span>

<span data-ttu-id="95180-382">| |</span><span class="sxs-lookup"><span data-stu-id="95180-382"></span></span>
|<span data-ttu-id="95180-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-384">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-384">passport number</span></span>  <br/> <span data-ttu-id="95180-385">lithunian-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="95180-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="95180-386">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-386">passport no</span></span>  <br/> <span data-ttu-id="95180-387">Paso Numeris</span><span class="sxs-lookup"><span data-stu-id="95180-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="95180-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="95180-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="95180-389">Format</span><span class="sxs-lookup"><span data-stu-id="95180-389">Format</span></span>

<span data-ttu-id="95180-390">Acht Ziffern oder Buchstaben ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-391">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-391">Pattern</span></span>

<span data-ttu-id="95180-392">Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="95180-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-393">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-393">Checksum</span></span>

<span data-ttu-id="95180-394">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-395">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-395">Definition</span></span>

<span data-ttu-id="95180-396">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-397">Der reguläre Ausdruck `Regex_nation_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-398">Ein Schlüsselwort `Keywords_nation_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-399">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-399">Keywords</span></span>

<span data-ttu-id="95180-400">| |</span><span class="sxs-lookup"><span data-stu-id="95180-400"></span></span>
|<span data-ttu-id="95180-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-402">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-402">passport number</span></span>  <br/> <span data-ttu-id="95180-403">Lettische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-403">latvian passport number</span></span>  <br/> <span data-ttu-id="95180-404">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-404">passport no</span></span>  <br/> <span data-ttu-id="95180-405">Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="95180-406">Malta</span><span class="sxs-lookup"><span data-stu-id="95180-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="95180-407">Format</span><span class="sxs-lookup"><span data-stu-id="95180-407">Format</span></span>

<span data-ttu-id="95180-408">Sieben Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="95180-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-409">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-409">Pattern</span></span>

 <span data-ttu-id="95180-410">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="95180-411">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-411">Checksum</span></span>

<span data-ttu-id="95180-412">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-413">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-413">Definition</span></span>

<span data-ttu-id="95180-414">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-415">Der reguläre Ausdruck `Regex_malta_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-416">Ein Schlüsselwort `Keywords_malta_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-417">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-417">Keywords</span></span>

<span data-ttu-id="95180-418">| |</span><span class="sxs-lookup"><span data-stu-id="95180-418"></span></span>
|<span data-ttu-id="95180-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-420">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-420">passport number</span></span>  <br/> <span data-ttu-id="95180-421">Maltesische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-421">maltese passport number</span></span>  <br/> <span data-ttu-id="95180-422">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-422">passport no</span></span>  <br/> <span data-ttu-id="95180-423">numru Tal-Passaport</span><span class="sxs-lookup"><span data-stu-id="95180-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="95180-424">Niederlande</span><span class="sxs-lookup"><span data-stu-id="95180-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="95180-425">Format</span><span class="sxs-lookup"><span data-stu-id="95180-425">Format</span></span>

<span data-ttu-id="95180-426">Neun Buchstaben oder Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="95180-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-427">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-427">Pattern</span></span>

<span data-ttu-id="95180-428">Neun Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-429">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-429">Checksum</span></span>

<span data-ttu-id="95180-430">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="95180-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-431">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-431">Definition</span></span>

<span data-ttu-id="95180-432">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-433">Der reguläre Ausdruck `Regex_netherlands_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-434">Ein Schlüsselwort `Keywords_netherlands_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-435">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-435">Keywords</span></span>

<span data-ttu-id="95180-436">| |</span><span class="sxs-lookup"><span data-stu-id="95180-436"></span></span>
|<span data-ttu-id="95180-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-438">niederländische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-438">dutch passport number</span></span>  <br/> <span data-ttu-id="95180-439">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-439">passport number</span></span>  <br/> <span data-ttu-id="95180-440">niederländische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="95180-441">Nederlanden paspoort Nummer</span><span class="sxs-lookup"><span data-stu-id="95180-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="95180-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="95180-442">paspoort</span></span>  <br/> <span data-ttu-id="95180-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="95180-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="95180-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="95180-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="95180-445">Polen</span><span class="sxs-lookup"><span data-stu-id="95180-445">Poland</span></span>

<span data-ttu-id="95180-446">Weitere Informationen finden Sie im Abschnitt "polnische Passnummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95180-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="95180-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="95180-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="95180-448">Format</span><span class="sxs-lookup"><span data-stu-id="95180-448">Format</span></span>

<span data-ttu-id="95180-449">Ein Buchstaben, gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-450">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-450">Pattern</span></span>

<span data-ttu-id="95180-451">Ein Buchstabe gefolgt von sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="95180-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="95180-452">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="95180-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="95180-453">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95180-454">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-454">Checksum</span></span>

<span data-ttu-id="95180-455">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-456">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-456">Definition</span></span>

<span data-ttu-id="95180-457">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-458">Der reguläre Ausdruck `Regex_portugal_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-459">Ein Schlüsselwort `Keywords_portugal_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-460">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-460">Keywords</span></span>

<span data-ttu-id="95180-461">| |</span><span class="sxs-lookup"><span data-stu-id="95180-461"></span></span>
|<span data-ttu-id="95180-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-463">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-463">passport number</span></span>  <br/> <span data-ttu-id="95180-464">portugiesische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="95180-465">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-465">passport no</span></span>  <br/> <span data-ttu-id="95180-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="95180-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="95180-467">Rumänien</span><span class="sxs-lookup"><span data-stu-id="95180-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="95180-468">Format</span><span class="sxs-lookup"><span data-stu-id="95180-468">Format</span></span>

<span data-ttu-id="95180-469">Acht oder neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="95180-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-470">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-470">Pattern</span></span>

<span data-ttu-id="95180-471">Acht oder neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-472">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-472">Checksum</span></span>

<span data-ttu-id="95180-473">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-474">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-474">Definition</span></span>

<span data-ttu-id="95180-475">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-476">Der reguläre Ausdruck `Regex_romania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-477">Ein Schlüsselwort `Keywords_romania_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-478">Keywords</span></span>

<span data-ttu-id="95180-479">| |</span><span class="sxs-lookup"><span data-stu-id="95180-479"></span></span>
|<span data-ttu-id="95180-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-481">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-481">passport number</span></span>  <br/> <span data-ttu-id="95180-482">rumänische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-482">romanian passport number</span></span>  <br/> <span data-ttu-id="95180-483">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-483">passport no</span></span>  <br/> <span data-ttu-id="95180-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="95180-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="95180-485">Slowakei</span><span class="sxs-lookup"><span data-stu-id="95180-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="95180-486">Format</span><span class="sxs-lookup"><span data-stu-id="95180-486">Format</span></span>

<span data-ttu-id="95180-487">Eine Ziffer oder ein Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-488">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-488">Pattern</span></span>

<span data-ttu-id="95180-489">Eine Ziffer oder ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="95180-490">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-490">Checksum</span></span>

<span data-ttu-id="95180-491">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-492">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-492">Definition</span></span>

<span data-ttu-id="95180-493">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-494">Der reguläre Ausdruck `Regex_slovakia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-495">Ein Schlüsselwort `Keywords_slovakia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-496">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-496">Keywords</span></span>

<span data-ttu-id="95180-497">| |</span><span class="sxs-lookup"><span data-stu-id="95180-497"></span></span>
|<span data-ttu-id="95180-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-499">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-499">passport number</span></span>  <br/> <span data-ttu-id="95180-500">Slowakische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="95180-501">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-501">passport no</span></span>  <br/> <span data-ttu-id="95180-502">číslo Pasu</span><span class="sxs-lookup"><span data-stu-id="95180-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="95180-503">Slowenien</span><span class="sxs-lookup"><span data-stu-id="95180-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="95180-504">Format</span><span class="sxs-lookup"><span data-stu-id="95180-504">Format</span></span>

<span data-ttu-id="95180-505">Zwei Buchstaben, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-506">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-506">Pattern</span></span>

<span data-ttu-id="95180-507">Zwei Buchstaben, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="95180-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="95180-508">Der Buchstabe "P"</span><span class="sxs-lookup"><span data-stu-id="95180-508">The letter "P"</span></span>
    
- <span data-ttu-id="95180-509">Ein Großbuchstabe</span><span class="sxs-lookup"><span data-stu-id="95180-509">One uppercase letter</span></span>
    
- <span data-ttu-id="95180-510">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95180-511">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-511">Checksum</span></span>

<span data-ttu-id="95180-512">Nein</span><span class="sxs-lookup"><span data-stu-id="95180-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-513">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-513">Definition</span></span>

<span data-ttu-id="95180-514">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-515">Der reguläre Ausdruck `Regex_slovenia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-516">Ein Schlüsselwort `Keywords_slovenia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-517">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-517">Keywords</span></span>

<span data-ttu-id="95180-518">| |</span><span class="sxs-lookup"><span data-stu-id="95180-518"></span></span>
|<span data-ttu-id="95180-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-520">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-520">passport number</span></span>  <br/> <span data-ttu-id="95180-521">slowenische Passnummer</span><span class="sxs-lookup"><span data-stu-id="95180-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="95180-522">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-522">passport no</span></span>  <br/> <span data-ttu-id="95180-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="95180-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="95180-524">Spanien</span><span class="sxs-lookup"><span data-stu-id="95180-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="95180-525">Format</span><span class="sxs-lookup"><span data-stu-id="95180-525">Format</span></span>

<span data-ttu-id="95180-526">Eine acht-oder neunstellige Kombination aus Buchstaben und Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="95180-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="95180-527">Muster</span><span class="sxs-lookup"><span data-stu-id="95180-527">Pattern</span></span>

<span data-ttu-id="95180-528">Eine Kombination aus Buchstaben und Zahlen mit acht oder neun Zeichen:</span><span class="sxs-lookup"><span data-stu-id="95180-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="95180-529">Zwei Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="95180-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="95180-530">Eine Ziffer oder ein Buchstabe (optional)</span><span class="sxs-lookup"><span data-stu-id="95180-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="95180-531">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="95180-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="95180-532">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="95180-532">Checksum</span></span>

<span data-ttu-id="95180-533">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="95180-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="95180-534">Definition</span><span class="sxs-lookup"><span data-stu-id="95180-534">Definition</span></span>

<span data-ttu-id="95180-535">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="95180-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="95180-536">Der reguläre Ausdruck `Regex_spain_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="95180-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="95180-537">Ein Schlüsselwort `Keywords_spain_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="95180-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="95180-538">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="95180-538">Keywords</span></span>

<span data-ttu-id="95180-539">| |</span><span class="sxs-lookup"><span data-stu-id="95180-539"></span></span>
|<span data-ttu-id="95180-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="95180-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="95180-541">Pass</span><span class="sxs-lookup"><span data-stu-id="95180-541">passport</span></span>  <br/> <span data-ttu-id="95180-542">Spanien Passport</span><span class="sxs-lookup"><span data-stu-id="95180-542">spain passport</span></span>  <br/> <span data-ttu-id="95180-543">Passport-Buch</span><span class="sxs-lookup"><span data-stu-id="95180-543">passport book</span></span>  <br/> <span data-ttu-id="95180-544">passport number</span><span class="sxs-lookup"><span data-stu-id="95180-544">passport number</span></span>  <br/> <span data-ttu-id="95180-545">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="95180-545">passport no</span></span>  <br/> <span data-ttu-id="95180-546">Libreta Pasaporte</span><span class="sxs-lookup"><span data-stu-id="95180-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="95180-547">número Pasaporte</span><span class="sxs-lookup"><span data-stu-id="95180-547">número pasaporte</span></span>  <br/> <span data-ttu-id="95180-548">ESPAÑA PASAPORTE</span><span class="sxs-lookup"><span data-stu-id="95180-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="95180-549">Pasaporte</span><span class="sxs-lookup"><span data-stu-id="95180-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="95180-550">Schweden</span><span class="sxs-lookup"><span data-stu-id="95180-550">Sweden</span></span>

<span data-ttu-id="95180-551">Weitere Informationen finden Sie im Abschnitt "schwedische Passport-Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95180-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="95180-552">UK</span><span class="sxs-lookup"><span data-stu-id="95180-552">UK</span></span>

<span data-ttu-id="95180-553">Weitere Informationen finden Sie im Abschnitt "U.S./U.K.</span><span class="sxs-lookup"><span data-stu-id="95180-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="95180-554">Passport-Nummer "in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="95180-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="95180-555">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95180-555">See also</span></span>

[<span data-ttu-id="95180-556">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="95180-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

