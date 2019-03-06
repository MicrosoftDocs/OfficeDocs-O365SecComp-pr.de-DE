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
ms.sourcegitcommit: ed822a776d3419853453583e882f3c61ca26d4b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2019
ms.locfileid: "30410930"
---
# <a name="eu-passport-number"></a><span data-ttu-id="7eb03-104">EU-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-104">EU Passport Number</span></span>

<span data-ttu-id="7eb03-105">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Passport-Nummer erkennt.</span><span class="sxs-lookup"><span data-stu-id="7eb03-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="7eb03-106">Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="7eb03-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="7eb03-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="7eb03-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-108">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-108">Format</span></span>

<span data-ttu-id="7eb03-109">Ein Buchstabe gefolgt von einem optionalen Leerzeichen und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-110">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-110">Pattern</span></span>

<span data-ttu-id="7eb03-111">Eine Kombination aus einem Buchstaben, sieben Ziffern und einem Leerzeichen:</span><span class="sxs-lookup"><span data-stu-id="7eb03-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="7eb03-112">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="7eb03-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="7eb03-113">Ein Leerzeichen (optional)</span><span class="sxs-lookup"><span data-stu-id="7eb03-113">One space (optional)</span></span>
    
- <span data-ttu-id="7eb03-114">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7eb03-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-115">Checksum</span></span>

<span data-ttu-id="7eb03-116">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="7eb03-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-117">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-117">Definition</span></span>

<span data-ttu-id="7eb03-118">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-119">Der reguläre Ausdruck `Regex_austria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-120">Ein Schlüsselwort `Keywords_austria_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-121">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-121">Keywords</span></span>

<span data-ttu-id="7eb03-122">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-122"></span></span>
|<span data-ttu-id="7eb03-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-124">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-124">passport number</span></span>  <br/> <span data-ttu-id="7eb03-125">Österreichische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-125">austrian passport number</span></span>  <br/> <span data-ttu-id="7eb03-126">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-126">passport no</span></span>  <br/> <span data-ttu-id="7eb03-127">Reisepass</span><span class="sxs-lookup"><span data-stu-id="7eb03-127">reisepass</span></span>  <br/> <span data-ttu-id="7eb03-128">österreichisch Reisepass</span><span class="sxs-lookup"><span data-stu-id="7eb03-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="7eb03-129">Belgien</span><span class="sxs-lookup"><span data-stu-id="7eb03-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-130">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-130">Format</span></span>

<span data-ttu-id="7eb03-131">Zwei Buchstaben, gefolgt von sechs Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-132">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-132">Pattern</span></span>

<span data-ttu-id="7eb03-133">Zwei Buchstaben, gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-134">Checksum</span></span>

<span data-ttu-id="7eb03-135">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="7eb03-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-136">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-136">Definition</span></span>

<span data-ttu-id="7eb03-137">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-138">Der reguläre Ausdruck `Regex_belgium_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-139">Ein Schlüsselwort `Keywords_belgium_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-140">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-140">Keywords</span></span>

<span data-ttu-id="7eb03-141">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-141"></span></span>
|<span data-ttu-id="7eb03-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-143">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-143">passport number</span></span>  <br/> <span data-ttu-id="7eb03-144">belgische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-144">belgian passport number</span></span>  <br/> <span data-ttu-id="7eb03-145">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-145">passport no</span></span>  <br/> <span data-ttu-id="7eb03-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="7eb03-146">paspoort</span></span>  <br/> <span data-ttu-id="7eb03-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="7eb03-148">Reisepass kein</span><span class="sxs-lookup"><span data-stu-id="7eb03-148">reisepass kein</span></span>  <br/> <span data-ttu-id="7eb03-149">Reisepass</span><span class="sxs-lookup"><span data-stu-id="7eb03-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="7eb03-150">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="7eb03-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-151">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-151">Format</span></span>

<span data-ttu-id="7eb03-152">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7eb03-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-153">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-153">Pattern</span></span>

 <span data-ttu-id="7eb03-154">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7eb03-155">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-155">Checksum</span></span>

<span data-ttu-id="7eb03-156">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-157">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-157">Definition</span></span>

<span data-ttu-id="7eb03-158">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-159">Der reguläre Ausdruck `Regex_bulgaria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-160">Ein Schlüsselwort `Keywords_bulgaria_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-161">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-161">Keywords</span></span>

<span data-ttu-id="7eb03-162">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-162"></span></span>
|<span data-ttu-id="7eb03-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-164">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-164">passport number</span></span>  <br/> <span data-ttu-id="7eb03-165">Bulgarische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="7eb03-166">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-166">passport no</span></span>  <br/> <span data-ttu-id="7eb03-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="7eb03-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="7eb03-168">Kroatien</span><span class="sxs-lookup"><span data-stu-id="7eb03-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-169">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-169">Format</span></span>

<span data-ttu-id="7eb03-170">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7eb03-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-171">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-171">Pattern</span></span>

 <span data-ttu-id="7eb03-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7eb03-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-173">Checksum</span></span>

<span data-ttu-id="7eb03-174">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-175">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-175">Definition</span></span>

<span data-ttu-id="7eb03-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-177">Der reguläre Ausdruck `Regex_croatia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-178">Ein Schlüsselwort `Keywords_croatia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-179">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-179">Keywords</span></span>

<span data-ttu-id="7eb03-180">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-180"></span></span>
|<span data-ttu-id="7eb03-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-182">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-182">passport number</span></span>  <br/> <span data-ttu-id="7eb03-183">Kroatische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-183">croatian passport number</span></span>  <br/> <span data-ttu-id="7eb03-184">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-184">passport no</span></span>  <br/> <span data-ttu-id="7eb03-185">Broj putovnice</span><span class="sxs-lookup"><span data-stu-id="7eb03-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="7eb03-186">Zypern</span><span class="sxs-lookup"><span data-stu-id="7eb03-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-187">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-187">Format</span></span>

<span data-ttu-id="7eb03-188">Ein Buchstabe, gefolgt von 6-8 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7eb03-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-189">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-189">Pattern</span></span>

<span data-ttu-id="7eb03-190">Ein Buchstabe gefolgt von sechs bis acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-191">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-191">Checksum</span></span>

<span data-ttu-id="7eb03-192">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-193">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-193">Definition</span></span>

<span data-ttu-id="7eb03-194">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-195">Der reguläre Ausdruck `Regex_cyprus_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-196">Ein Schlüsselwort `Keywords_cyprus_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-197">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-197">Keywords</span></span>

<span data-ttu-id="7eb03-198">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-198"></span></span>
|<span data-ttu-id="7eb03-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-200">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-200">passport number</span></span>  <br/> <span data-ttu-id="7eb03-201">Zypern-Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="7eb03-202">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-202">passport no</span></span>  <br/> <span data-ttu-id="7eb03-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="7eb03-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="7eb03-204">Tschechien</span><span class="sxs-lookup"><span data-stu-id="7eb03-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-205">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-205">Format</span></span>

<span data-ttu-id="7eb03-206">Acht Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7eb03-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-207">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-207">Pattern</span></span>

<span data-ttu-id="7eb03-208">Acht Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7eb03-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-209">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-209">Checksum</span></span>

<span data-ttu-id="7eb03-210">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-211">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-211">Definition</span></span>

<span data-ttu-id="7eb03-212">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-213">Der reguläre Ausdruck `Regex_czech_republic_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-214">Ein Schlüsselwort `Keywords_czech_republic_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-215">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-215">Keywords</span></span>

<span data-ttu-id="7eb03-216">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-216"></span></span>
|<span data-ttu-id="7eb03-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-218">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-218">passport number</span></span>  <br/> <span data-ttu-id="7eb03-219">Tschechische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-219">czech passport number</span></span>  <br/> <span data-ttu-id="7eb03-220">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-220">passport no</span></span>  <br/> <span data-ttu-id="7eb03-221">Cestovní Pas</span><span class="sxs-lookup"><span data-stu-id="7eb03-221">cestovní pas</span></span>  <br/> <span data-ttu-id="7eb03-222">Pas</span><span class="sxs-lookup"><span data-stu-id="7eb03-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="7eb03-223">Dänemark</span><span class="sxs-lookup"><span data-stu-id="7eb03-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-224">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-224">Format</span></span>

<span data-ttu-id="7eb03-225">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7eb03-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-226">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-226">Pattern</span></span>

 <span data-ttu-id="7eb03-227">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7eb03-228">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-228">Checksum</span></span>

<span data-ttu-id="7eb03-229">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-230">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-230">Definition</span></span>

<span data-ttu-id="7eb03-231">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-232">Der reguläre Ausdruck `Regex_denmark_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-233">Ein Schlüsselwort `Keywords_denmark_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-234">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-234">Keywords</span></span>

<span data-ttu-id="7eb03-235">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-235"></span></span>
|<span data-ttu-id="7eb03-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-237">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-237">passport number</span></span>  <br/> <span data-ttu-id="7eb03-238">dänische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-238">danish passport number</span></span>  <br/> <span data-ttu-id="7eb03-239">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-239">passport no</span></span>  <br/> <span data-ttu-id="7eb03-240">Pas</span><span class="sxs-lookup"><span data-stu-id="7eb03-240">pas</span></span>  <br/> <span data-ttu-id="7eb03-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="7eb03-242">Estland</span><span class="sxs-lookup"><span data-stu-id="7eb03-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-243">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-243">Format</span></span>

<span data-ttu-id="7eb03-244">Ein Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-245">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-245">Pattern</span></span>

<span data-ttu-id="7eb03-246">Ein Buchstabe gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-247">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-247">Checksum</span></span>

<span data-ttu-id="7eb03-248">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-249">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-249">Definition</span></span>

<span data-ttu-id="7eb03-250">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-251">Der reguläre Ausdruck `Regex_estonia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-252">Ein Schlüsselwort `Keywords_estonia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-253">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-253">Keywords</span></span>

<span data-ttu-id="7eb03-254">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-254"></span></span>
|<span data-ttu-id="7eb03-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-256">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-256">passport number</span></span>  <br/> <span data-ttu-id="7eb03-257">Estnische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-257">estonian passport number</span></span>  <br/> <span data-ttu-id="7eb03-258">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-258">passport no</span></span>  <br/> <span data-ttu-id="7eb03-259">Eesti kodaniku-Durchlauf</span><span class="sxs-lookup"><span data-stu-id="7eb03-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="7eb03-260">Finnland</span><span class="sxs-lookup"><span data-stu-id="7eb03-260">Finland</span></span>

<span data-ttu-id="7eb03-261">Weitere Informationen finden Sie im Abschnitt "Finland Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7eb03-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="7eb03-262">Frankreich</span><span class="sxs-lookup"><span data-stu-id="7eb03-262">France</span></span>

<span data-ttu-id="7eb03-263">Weitere Informationen finden Sie im Abschnitt "Frankreich Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7eb03-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="7eb03-264">Deutschland</span><span class="sxs-lookup"><span data-stu-id="7eb03-264">Germany</span></span>

<span data-ttu-id="7eb03-265">Weitere Informationen finden Sie im Abschnitt "Deutschland Passport Number" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7eb03-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="7eb03-266">Griechenland</span><span class="sxs-lookup"><span data-stu-id="7eb03-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-267">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-267">Format</span></span>

<span data-ttu-id="7eb03-268">Zwei Buchstaben, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-269">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-269">Pattern</span></span>

<span data-ttu-id="7eb03-270">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-271">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-271">Checksum</span></span>

<span data-ttu-id="7eb03-272">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-273">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-273">Definition</span></span>

<span data-ttu-id="7eb03-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-275">Der reguläre Ausdruck `Regex_greece_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-276">Ein Schlüsselwort `Keywords_greece_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-277">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-277">Keywords</span></span>

<span data-ttu-id="7eb03-278">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-278"></span></span>
|<span data-ttu-id="7eb03-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-280">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-280">passport number</span></span>  <br/> <span data-ttu-id="7eb03-281">griechische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-281">greek passport number</span></span>  <br/> <span data-ttu-id="7eb03-282">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-282">passport no</span></span>  <br/> <span data-ttu-id="7eb03-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="7eb03-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="7eb03-284">Ungarn</span><span class="sxs-lookup"><span data-stu-id="7eb03-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-285">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-285">Format</span></span>

<span data-ttu-id="7eb03-286">Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-287">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-287">Pattern</span></span>

<span data-ttu-id="7eb03-288">Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-289">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-289">Checksum</span></span>

<span data-ttu-id="7eb03-290">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-291">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-291">Definition</span></span>

<span data-ttu-id="7eb03-292">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-293">Der reguläre Ausdruck `Regex_hungary_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-294">Ein Schlüsselwort `Keywords_hungary_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-295">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-295">Keywords</span></span>

<span data-ttu-id="7eb03-296">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-296"></span></span>
|<span data-ttu-id="7eb03-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-298">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-298">passport number</span></span>  <br/> <span data-ttu-id="7eb03-299">ungarische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="7eb03-300">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-300">passport no</span></span>  <br/> <span data-ttu-id="7eb03-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="7eb03-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="7eb03-302">Irland</span><span class="sxs-lookup"><span data-stu-id="7eb03-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-303">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-303">Format</span></span>

<span data-ttu-id="7eb03-304">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-305">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-305">Pattern</span></span>

<span data-ttu-id="7eb03-306">Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7eb03-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="7eb03-307">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="7eb03-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="7eb03-308">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7eb03-309">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-309">Checksum</span></span>

<span data-ttu-id="7eb03-310">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-311">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-311">Definition</span></span>

<span data-ttu-id="7eb03-312">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-313">Der reguläre Ausdruck `Regex_ireland_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-314">Ein Schlüsselwort `Keywords_ireland_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-315">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-315">Keywords</span></span>

<span data-ttu-id="7eb03-316">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-316"></span></span>
|<span data-ttu-id="7eb03-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-318">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-318">passport number</span></span>  <br/> <span data-ttu-id="7eb03-319">irische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-319">irish passport number</span></span>  <br/> <span data-ttu-id="7eb03-320">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-320">passport no</span></span>  <br/> <span data-ttu-id="7eb03-321">Pas</span><span class="sxs-lookup"><span data-stu-id="7eb03-321">pas</span></span>  <br/> <span data-ttu-id="7eb03-322">Pass</span><span class="sxs-lookup"><span data-stu-id="7eb03-322">passport</span></span>  <br/> <span data-ttu-id="7eb03-323">Passeport</span><span class="sxs-lookup"><span data-stu-id="7eb03-323">passeport</span></span>  <br/> <span data-ttu-id="7eb03-324">Passeport numero</span><span class="sxs-lookup"><span data-stu-id="7eb03-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="7eb03-325">Italien</span><span class="sxs-lookup"><span data-stu-id="7eb03-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-326">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-326">Format</span></span>

<span data-ttu-id="7eb03-327">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-328">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-328">Pattern</span></span>

<span data-ttu-id="7eb03-329">Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7eb03-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="7eb03-330">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="7eb03-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="7eb03-331">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7eb03-332">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-332">Checksum</span></span>

<span data-ttu-id="7eb03-333">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="7eb03-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-334">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-334">Definition</span></span>

<span data-ttu-id="7eb03-335">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-336">Der reguläre Ausdruck `Regex_italy_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-337">Ein Schlüsselwort `Keywords_italy_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-338">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-338">Keywords</span></span>

<span data-ttu-id="7eb03-339">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-339"></span></span>
|<span data-ttu-id="7eb03-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-341">italienische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-341">italian passport number</span></span>  <br/> <span data-ttu-id="7eb03-342">Repubblica Italiana Passa Porto</span><span class="sxs-lookup"><span data-stu-id="7eb03-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="7eb03-343">Passa Porto</span><span class="sxs-lookup"><span data-stu-id="7eb03-343">passaporto</span></span>  <br/> <span data-ttu-id="7eb03-344">Passa Porto Italiana</span><span class="sxs-lookup"><span data-stu-id="7eb03-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="7eb03-345">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-345">passport number</span></span>  <br/> <span data-ttu-id="7eb03-346">Italiana Passa Porto numero</span><span class="sxs-lookup"><span data-stu-id="7eb03-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="7eb03-347">Passa Porto numero</span><span class="sxs-lookup"><span data-stu-id="7eb03-347">passaporto numero</span></span>  <br/> <span data-ttu-id="7eb03-348">Numéro Passeport Italien</span><span class="sxs-lookup"><span data-stu-id="7eb03-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="7eb03-349">Numéro Passeport</span><span class="sxs-lookup"><span data-stu-id="7eb03-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="7eb03-350">Lettland</span><span class="sxs-lookup"><span data-stu-id="7eb03-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-351">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-351">Format</span></span>

<span data-ttu-id="7eb03-352">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-353">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-353">Pattern</span></span>

<span data-ttu-id="7eb03-354">Zwei Buchstaben oder Ziffern gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7eb03-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="7eb03-355">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="7eb03-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="7eb03-356">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7eb03-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-357">Checksum</span></span>

<span data-ttu-id="7eb03-358">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-359">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-359">Definition</span></span>

<span data-ttu-id="7eb03-360">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-361">Der reguläre Ausdruck `Regex_latvia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-362">Ein Schlüsselwort `Keywords_latvia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-363">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-363">Keywords</span></span>

<span data-ttu-id="7eb03-364">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-364"></span></span>
|<span data-ttu-id="7eb03-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-366">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-366">passport number</span></span>  <br/> <span data-ttu-id="7eb03-367">Lettische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-367">latvian passport number</span></span>  <br/> <span data-ttu-id="7eb03-368">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-368">passport no</span></span>  <br/> <span data-ttu-id="7eb03-369">Pase numurs</span><span class="sxs-lookup"><span data-stu-id="7eb03-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="7eb03-370">Litauen</span><span class="sxs-lookup"><span data-stu-id="7eb03-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-371">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-371">Format</span></span>

<span data-ttu-id="7eb03-372">Acht Ziffern oder Buchstaben ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-373">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-373">Pattern</span></span>

<span data-ttu-id="7eb03-374">Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="7eb03-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-375">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-375">Checksum</span></span>

<span data-ttu-id="7eb03-376">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="7eb03-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-377">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-377">Definition</span></span>

<span data-ttu-id="7eb03-378">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-379">Der reguläre Ausdruck `Regex_lithuania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-380">Ein Schlüsselwort `Keywords_lithuania_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-381">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-381">Keywords</span></span>

<span data-ttu-id="7eb03-382">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-382"></span></span>
|<span data-ttu-id="7eb03-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-384">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-384">passport number</span></span>  <br/> <span data-ttu-id="7eb03-385">lithunian-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="7eb03-386">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-386">passport no</span></span>  <br/> <span data-ttu-id="7eb03-387">Paso Numeris</span><span class="sxs-lookup"><span data-stu-id="7eb03-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="7eb03-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="7eb03-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-389">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-389">Format</span></span>

<span data-ttu-id="7eb03-390">Acht Ziffern oder Buchstaben ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-391">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-391">Pattern</span></span>

<span data-ttu-id="7eb03-392">Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="7eb03-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-393">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-393">Checksum</span></span>

<span data-ttu-id="7eb03-394">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-395">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-395">Definition</span></span>

<span data-ttu-id="7eb03-396">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-397">Der reguläre Ausdruck `Regex_nation_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-398">Ein Schlüsselwort `Keywords_nation_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-399">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-399">Keywords</span></span>

<span data-ttu-id="7eb03-400">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-400"></span></span>
|<span data-ttu-id="7eb03-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-402">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-402">passport number</span></span>  <br/> <span data-ttu-id="7eb03-403">Lettische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-403">latvian passport number</span></span>  <br/> <span data-ttu-id="7eb03-404">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-404">passport no</span></span>  <br/> <span data-ttu-id="7eb03-405">Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="7eb03-406">Malta</span><span class="sxs-lookup"><span data-stu-id="7eb03-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-407">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-407">Format</span></span>

<span data-ttu-id="7eb03-408">Sieben Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7eb03-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-409">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-409">Pattern</span></span>

 <span data-ttu-id="7eb03-410">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="7eb03-411">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-411">Checksum</span></span>

<span data-ttu-id="7eb03-412">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-413">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-413">Definition</span></span>

<span data-ttu-id="7eb03-414">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-415">Der reguläre Ausdruck `Regex_malta_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-416">Ein Schlüsselwort `Keywords_malta_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-417">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-417">Keywords</span></span>

<span data-ttu-id="7eb03-418">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-418"></span></span>
|<span data-ttu-id="7eb03-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-420">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-420">passport number</span></span>  <br/> <span data-ttu-id="7eb03-421">Maltesische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-421">maltese passport number</span></span>  <br/> <span data-ttu-id="7eb03-422">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-422">passport no</span></span>  <br/> <span data-ttu-id="7eb03-423">numru Tal-Passaport</span><span class="sxs-lookup"><span data-stu-id="7eb03-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="7eb03-424">Niederlande</span><span class="sxs-lookup"><span data-stu-id="7eb03-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-425">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-425">Format</span></span>

<span data-ttu-id="7eb03-426">Neun Buchstaben oder Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7eb03-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-427">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-427">Pattern</span></span>

<span data-ttu-id="7eb03-428">Neun Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-429">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-429">Checksum</span></span>

<span data-ttu-id="7eb03-430">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="7eb03-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-431">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-431">Definition</span></span>

<span data-ttu-id="7eb03-432">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-433">Der reguläre Ausdruck `Regex_netherlands_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-434">Ein Schlüsselwort `Keywords_netherlands_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-435">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-435">Keywords</span></span>

<span data-ttu-id="7eb03-436">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-436"></span></span>
|<span data-ttu-id="7eb03-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-438">niederländische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-438">dutch passport number</span></span>  <br/> <span data-ttu-id="7eb03-439">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-439">passport number</span></span>  <br/> <span data-ttu-id="7eb03-440">niederländische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="7eb03-441">Nederlanden paspoort Nummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="7eb03-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="7eb03-442">paspoort</span></span>  <br/> <span data-ttu-id="7eb03-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="7eb03-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="7eb03-445">Polen</span><span class="sxs-lookup"><span data-stu-id="7eb03-445">Poland</span></span>

<span data-ttu-id="7eb03-446">Weitere Informationen finden Sie im Abschnitt "polnische Passnummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7eb03-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="7eb03-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="7eb03-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-448">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-448">Format</span></span>

<span data-ttu-id="7eb03-449">Ein Buchstaben, gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-450">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-450">Pattern</span></span>

<span data-ttu-id="7eb03-451">Ein Buchstabe gefolgt von sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7eb03-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="7eb03-452">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="7eb03-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="7eb03-453">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7eb03-454">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-454">Checksum</span></span>

<span data-ttu-id="7eb03-455">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-456">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-456">Definition</span></span>

<span data-ttu-id="7eb03-457">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-458">Der reguläre Ausdruck `Regex_portugal_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-459">Ein Schlüsselwort `Keywords_portugal_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-460">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-460">Keywords</span></span>

<span data-ttu-id="7eb03-461">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-461"></span></span>
|<span data-ttu-id="7eb03-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-463">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-463">passport number</span></span>  <br/> <span data-ttu-id="7eb03-464">portugiesische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="7eb03-465">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-465">passport no</span></span>  <br/> <span data-ttu-id="7eb03-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="7eb03-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="7eb03-467">Rumänien</span><span class="sxs-lookup"><span data-stu-id="7eb03-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-468">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-468">Format</span></span>

<span data-ttu-id="7eb03-469">Acht oder neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="7eb03-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-470">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-470">Pattern</span></span>

<span data-ttu-id="7eb03-471">Acht oder neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-472">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-472">Checksum</span></span>

<span data-ttu-id="7eb03-473">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-474">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-474">Definition</span></span>

<span data-ttu-id="7eb03-475">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-476">Der reguläre Ausdruck `Regex_romania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-477">Ein Schlüsselwort `Keywords_romania_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-478">Keywords</span></span>

<span data-ttu-id="7eb03-479">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-479"></span></span>
|<span data-ttu-id="7eb03-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-481">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-481">passport number</span></span>  <br/> <span data-ttu-id="7eb03-482">rumänische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-482">romanian passport number</span></span>  <br/> <span data-ttu-id="7eb03-483">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-483">passport no</span></span>  <br/> <span data-ttu-id="7eb03-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="7eb03-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="7eb03-485">Slowakei</span><span class="sxs-lookup"><span data-stu-id="7eb03-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-486">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-486">Format</span></span>

<span data-ttu-id="7eb03-487">Eine Ziffer oder ein Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-488">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-488">Pattern</span></span>

<span data-ttu-id="7eb03-489">Eine Ziffer oder ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="7eb03-490">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-490">Checksum</span></span>

<span data-ttu-id="7eb03-491">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-492">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-492">Definition</span></span>

<span data-ttu-id="7eb03-493">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-494">Der reguläre Ausdruck `Regex_slovakia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-495">Ein Schlüsselwort `Keywords_slovakia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-496">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-496">Keywords</span></span>

<span data-ttu-id="7eb03-497">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-497"></span></span>
|<span data-ttu-id="7eb03-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-499">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-499">passport number</span></span>  <br/> <span data-ttu-id="7eb03-500">Slowakische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="7eb03-501">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-501">passport no</span></span>  <br/> <span data-ttu-id="7eb03-502">číslo Pasu</span><span class="sxs-lookup"><span data-stu-id="7eb03-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="7eb03-503">Slowenien</span><span class="sxs-lookup"><span data-stu-id="7eb03-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-504">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-504">Format</span></span>

<span data-ttu-id="7eb03-505">Zwei Buchstaben, gefolgt von sieben Ziffern, ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-506">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-506">Pattern</span></span>

<span data-ttu-id="7eb03-507">Zwei Buchstaben, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="7eb03-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="7eb03-508">Der Buchstabe "P"</span><span class="sxs-lookup"><span data-stu-id="7eb03-508">The letter "P"</span></span>
    
- <span data-ttu-id="7eb03-509">Ein Großbuchstabe</span><span class="sxs-lookup"><span data-stu-id="7eb03-509">One uppercase letter</span></span>
    
- <span data-ttu-id="7eb03-510">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7eb03-511">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-511">Checksum</span></span>

<span data-ttu-id="7eb03-512">Nein</span><span class="sxs-lookup"><span data-stu-id="7eb03-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-513">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-513">Definition</span></span>

<span data-ttu-id="7eb03-514">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-515">Der reguläre Ausdruck `Regex_slovenia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-516">Ein Schlüsselwort `Keywords_slovenia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-517">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-517">Keywords</span></span>

<span data-ttu-id="7eb03-518">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-518"></span></span>
|<span data-ttu-id="7eb03-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-520">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-520">passport number</span></span>  <br/> <span data-ttu-id="7eb03-521">slowenische Passnummer</span><span class="sxs-lookup"><span data-stu-id="7eb03-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="7eb03-522">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-522">passport no</span></span>  <br/> <span data-ttu-id="7eb03-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="7eb03-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="7eb03-524">Spanien</span><span class="sxs-lookup"><span data-stu-id="7eb03-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="7eb03-525">Format</span><span class="sxs-lookup"><span data-stu-id="7eb03-525">Format</span></span>

<span data-ttu-id="7eb03-526">Eine acht-oder neunstellige Kombination aus Buchstaben und Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="7eb03-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="7eb03-527">Muster</span><span class="sxs-lookup"><span data-stu-id="7eb03-527">Pattern</span></span>

<span data-ttu-id="7eb03-528">Eine Kombination aus Buchstaben und Zahlen mit acht oder neun Zeichen:</span><span class="sxs-lookup"><span data-stu-id="7eb03-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="7eb03-529">Zwei Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="7eb03-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="7eb03-530">Eine Ziffer oder ein Buchstabe (optional)</span><span class="sxs-lookup"><span data-stu-id="7eb03-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="7eb03-531">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="7eb03-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="7eb03-532">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="7eb03-532">Checksum</span></span>

<span data-ttu-id="7eb03-533">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="7eb03-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="7eb03-534">Definition</span><span class="sxs-lookup"><span data-stu-id="7eb03-534">Definition</span></span>

<span data-ttu-id="7eb03-535">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="7eb03-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="7eb03-536">Der reguläre Ausdruck `Regex_spain_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="7eb03-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="7eb03-537">Ein Schlüsselwort `Keywords_spain_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="7eb03-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="7eb03-538">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="7eb03-538">Keywords</span></span>

<span data-ttu-id="7eb03-539">| |</span><span class="sxs-lookup"><span data-stu-id="7eb03-539"></span></span>
|<span data-ttu-id="7eb03-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="7eb03-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="7eb03-541">Pass</span><span class="sxs-lookup"><span data-stu-id="7eb03-541">passport</span></span>  <br/> <span data-ttu-id="7eb03-542">Spanien Passport</span><span class="sxs-lookup"><span data-stu-id="7eb03-542">spain passport</span></span>  <br/> <span data-ttu-id="7eb03-543">Passport-Buch</span><span class="sxs-lookup"><span data-stu-id="7eb03-543">passport book</span></span>  <br/> <span data-ttu-id="7eb03-544">passport number</span><span class="sxs-lookup"><span data-stu-id="7eb03-544">passport number</span></span>  <br/> <span data-ttu-id="7eb03-545">Passport-Nr.</span><span class="sxs-lookup"><span data-stu-id="7eb03-545">passport no</span></span>  <br/> <span data-ttu-id="7eb03-546">Libreta Pasaporte</span><span class="sxs-lookup"><span data-stu-id="7eb03-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="7eb03-547">número Pasaporte</span><span class="sxs-lookup"><span data-stu-id="7eb03-547">número pasaporte</span></span>  <br/> <span data-ttu-id="7eb03-548">ESPAÑA PASAPORTE</span><span class="sxs-lookup"><span data-stu-id="7eb03-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="7eb03-549">Pasaporte</span><span class="sxs-lookup"><span data-stu-id="7eb03-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="7eb03-550">Schweden</span><span class="sxs-lookup"><span data-stu-id="7eb03-550">Sweden</span></span>

<span data-ttu-id="7eb03-551">Weitere Informationen finden Sie im Abschnitt "schwedische Passport-Nummer" in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7eb03-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="7eb03-552">UK</span><span class="sxs-lookup"><span data-stu-id="7eb03-552">UK</span></span>

<span data-ttu-id="7eb03-553">Weitere Informationen finden Sie im Abschnitt "U.S./U.K.</span><span class="sxs-lookup"><span data-stu-id="7eb03-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="7eb03-554">Passport-Nummer "in [was die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="7eb03-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7eb03-555">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7eb03-555">See also</span></span>

[<span data-ttu-id="7eb03-556">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="7eb03-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

