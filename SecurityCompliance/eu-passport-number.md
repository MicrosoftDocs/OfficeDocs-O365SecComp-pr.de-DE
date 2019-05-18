---
title: EU-Passport-Nummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn der vertrauliche Informationstyp EU-Passport-Nummern erkannt wird. Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.
ms.openlocfilehash: fa3be04dec0f71a2568e046abd6b0af3e20181c5
ms.sourcegitcommit: 9d67cb52544321a430343d39eb336112c1a11d35
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/17/2019
ms.locfileid: "34152967"
---
# <a name="eu-passport-number"></a><span data-ttu-id="3ac0b-104">EU-Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-104">EU Passport Number</span></span>

<span data-ttu-id="3ac0b-105">In diesem Thema wird gezeigt, was eine DLP-Richtlinie (Data Loss Prevention) sucht, wenn der vertrauliche Informationstyp EU-Passport-Nummern erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type.</span></span> <span data-ttu-id="3ac0b-106">Dieser Typ vertraulicher Informationen definiert unterschiedliche Muster, Stichwörter und andere Beweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="3ac0b-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="3ac0b-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-108">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-108">Format</span></span>

<span data-ttu-id="3ac0b-109">Ein Buchstabe, gefolgt von einem optionalen Leerzeichen und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-110">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-110">Pattern</span></span>

<span data-ttu-id="3ac0b-111">Eine Kombination aus einem Buchstaben, sieben Ziffern und einem Leerzeichen:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="3ac0b-112">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="3ac0b-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="3ac0b-113">Ein Leerzeichen (optional)</span><span class="sxs-lookup"><span data-stu-id="3ac0b-113">One space (optional)</span></span>
    
- <span data-ttu-id="3ac0b-114">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ac0b-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-115">Checksum</span></span>

<span data-ttu-id="3ac0b-116">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="3ac0b-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-117">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-117">Definition</span></span>

<span data-ttu-id="3ac0b-118">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-119">Der reguläre Ausdruck `Regex_austria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-120">Ein Schlüsselwort `Keywords_austria_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-121">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-121">Keywords</span></span>

<span data-ttu-id="3ac0b-122">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-122"></span></span>
|<span data-ttu-id="3ac0b-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-124">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-124">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-125">Österreichische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-125">austrian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-126">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-126">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-127">Reisepass</span><span class="sxs-lookup"><span data-stu-id="3ac0b-127">reisepass</span></span>  <br/> <span data-ttu-id="3ac0b-128">österreichisch Reisepass</span><span class="sxs-lookup"><span data-stu-id="3ac0b-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="3ac0b-129">Belgien</span><span class="sxs-lookup"><span data-stu-id="3ac0b-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-130">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-130">Format</span></span>

<span data-ttu-id="3ac0b-131">Zwei Buchstaben, gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-132">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-132">Pattern</span></span>

<span data-ttu-id="3ac0b-133">Zwei Buchstaben und gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-134">Checksum</span></span>

<span data-ttu-id="3ac0b-135">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="3ac0b-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-136">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-136">Definition</span></span>

<span data-ttu-id="3ac0b-137">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-138">Der reguläre Ausdruck `Regex_belgium_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-139">Ein Schlüsselwort `Keywords_belgium_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-140">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-140">Keywords</span></span>

<span data-ttu-id="3ac0b-141">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-141"></span></span>
|<span data-ttu-id="3ac0b-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-143">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-143">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-144">belgische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-144">belgian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-145">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-145">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="3ac0b-146">paspoort</span></span>  <br/> <span data-ttu-id="3ac0b-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="3ac0b-148">Reisepass kein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-148">reisepass kein</span></span>  <br/> <span data-ttu-id="3ac0b-149">Reisepass</span><span class="sxs-lookup"><span data-stu-id="3ac0b-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="3ac0b-150">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="3ac0b-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-151">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-151">Format</span></span>

<span data-ttu-id="3ac0b-152">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-153">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-153">Pattern</span></span>

 <span data-ttu-id="3ac0b-154">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-155">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-155">Checksum</span></span>

<span data-ttu-id="3ac0b-156">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-157">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-157">Definition</span></span>

<span data-ttu-id="3ac0b-158">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-159">Der reguläre Ausdruck `Regex_bulgaria_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-160">Ein Schlüsselwort `Keywords_bulgaria_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-161">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-161">Keywords</span></span>

<span data-ttu-id="3ac0b-162">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-162"></span></span>
|<span data-ttu-id="3ac0b-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-164">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-164">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-165">Bulgarische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-166">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-166">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-167">номер на паспорта</span><span class="sxs-lookup"><span data-stu-id="3ac0b-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="3ac0b-168">Kroatien</span><span class="sxs-lookup"><span data-stu-id="3ac0b-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-169">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-169">Format</span></span>

<span data-ttu-id="3ac0b-170">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-171">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-171">Pattern</span></span>

 <span data-ttu-id="3ac0b-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-173">Checksum</span></span>

<span data-ttu-id="3ac0b-174">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-175">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-175">Definition</span></span>

<span data-ttu-id="3ac0b-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-177">Der reguläre Ausdruck `Regex_croatia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-178">Ein Schlüsselwort `Keywords_croatia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-179">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-179">Keywords</span></span>

<span data-ttu-id="3ac0b-180">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-180"></span></span>
|<span data-ttu-id="3ac0b-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-182">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-182">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-183">Kroatische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-183">croatian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-184">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-184">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-185">Broj putovnice</span><span class="sxs-lookup"><span data-stu-id="3ac0b-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="3ac0b-186">Zypern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-187">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-187">Format</span></span>

<span data-ttu-id="3ac0b-188">Ein Buchstabe, gefolgt von 6-8 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-189">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-189">Pattern</span></span>

<span data-ttu-id="3ac0b-190">Ein Buchstabe, gefolgt von sechs bis acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-191">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-191">Checksum</span></span>

<span data-ttu-id="3ac0b-192">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-193">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-193">Definition</span></span>

<span data-ttu-id="3ac0b-194">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-195">Der reguläre Ausdruck `Regex_cyprus_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-196">Ein Schlüsselwort `Keywords_cyprus_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-197">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-197">Keywords</span></span>

<span data-ttu-id="3ac0b-198">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-198"></span></span>
|<span data-ttu-id="3ac0b-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-200">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-200">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-201">Zypern-Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="3ac0b-202">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-202">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-203">αριθμό διαβατηρίου</span><span class="sxs-lookup"><span data-stu-id="3ac0b-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="3ac0b-204">Tschechien</span><span class="sxs-lookup"><span data-stu-id="3ac0b-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-205">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-205">Format</span></span>

<span data-ttu-id="3ac0b-206">Acht Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-207">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-207">Pattern</span></span>

<span data-ttu-id="3ac0b-208">Acht Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-209">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-209">Checksum</span></span>

<span data-ttu-id="3ac0b-210">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-211">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-211">Definition</span></span>

<span data-ttu-id="3ac0b-212">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-213">Der reguläre Ausdruck `Regex_czech_republic_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-214">Ein Schlüsselwort `Keywords_czech_republic_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-215">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-215">Keywords</span></span>

<span data-ttu-id="3ac0b-216">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-216"></span></span>
|<span data-ttu-id="3ac0b-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-218">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-218">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-219">Tschechische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-219">czech passport number</span></span>  <br/> <span data-ttu-id="3ac0b-220">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-220">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-221">Cestovní Pas</span><span class="sxs-lookup"><span data-stu-id="3ac0b-221">cestovní pas</span></span>  <br/> <span data-ttu-id="3ac0b-222">Pas</span><span class="sxs-lookup"><span data-stu-id="3ac0b-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="3ac0b-223">Dänemark</span><span class="sxs-lookup"><span data-stu-id="3ac0b-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-224">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-224">Format</span></span>

<span data-ttu-id="3ac0b-225">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-226">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-226">Pattern</span></span>

 <span data-ttu-id="3ac0b-227">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-228">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-228">Checksum</span></span>

<span data-ttu-id="3ac0b-229">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-230">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-230">Definition</span></span>

<span data-ttu-id="3ac0b-231">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-232">Der reguläre Ausdruck `Regex_denmark_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-233">Ein Schlüsselwort `Keywords_denmark_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-234">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-234">Keywords</span></span>

<span data-ttu-id="3ac0b-235">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-235"></span></span>
|<span data-ttu-id="3ac0b-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-237">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-237">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-238">dänische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-238">danish passport number</span></span>  <br/> <span data-ttu-id="3ac0b-239">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-239">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-240">Pas</span><span class="sxs-lookup"><span data-stu-id="3ac0b-240">pas</span></span>  <br/> <span data-ttu-id="3ac0b-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="3ac0b-242">Estland</span><span class="sxs-lookup"><span data-stu-id="3ac0b-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-243">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-243">Format</span></span>

<span data-ttu-id="3ac0b-244">Ein Buchstabe, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-245">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-245">Pattern</span></span>

<span data-ttu-id="3ac0b-246">Ein Buchstabe, gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-247">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-247">Checksum</span></span>

<span data-ttu-id="3ac0b-248">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-249">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-249">Definition</span></span>

<span data-ttu-id="3ac0b-250">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-251">Der reguläre Ausdruck `Regex_estonia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-252">Ein Schlüsselwort `Keywords_estonia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-253">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-253">Keywords</span></span>

<span data-ttu-id="3ac0b-254">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-254"></span></span>
|<span data-ttu-id="3ac0b-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-256">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-256">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-257">Estnische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-257">estonian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-258">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-258">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-259">Eesti kodaniku Pass</span><span class="sxs-lookup"><span data-stu-id="3ac0b-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="3ac0b-260">Finnland</span><span class="sxs-lookup"><span data-stu-id="3ac0b-260">Finland</span></span>

<span data-ttu-id="3ac0b-261">Ausführliche Informationen finden Sie im Abschnitt "Finnland-Passport-Nummer" unter [was die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3ac0b-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="3ac0b-262">Frankreich</span><span class="sxs-lookup"><span data-stu-id="3ac0b-262">France</span></span>

<span data-ttu-id="3ac0b-263">Ausführliche Informationen finden Sie im Abschnitt "französische Passport-Nummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3ac0b-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="3ac0b-264">Deutschland</span><span class="sxs-lookup"><span data-stu-id="3ac0b-264">Germany</span></span>

<span data-ttu-id="3ac0b-265">Ausführliche Informationen finden Sie im Abschnitt "Deutschland Passport-Nummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3ac0b-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="3ac0b-266">Griechenland</span><span class="sxs-lookup"><span data-stu-id="3ac0b-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-267">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-267">Format</span></span>

<span data-ttu-id="3ac0b-268">Zwei Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-269">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-269">Pattern</span></span>

<span data-ttu-id="3ac0b-270">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-271">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-271">Checksum</span></span>

<span data-ttu-id="3ac0b-272">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-273">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-273">Definition</span></span>

<span data-ttu-id="3ac0b-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-275">Der reguläre Ausdruck `Regex_greece_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-276">Ein Schlüsselwort `Keywords_greece_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-277">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-277">Keywords</span></span>

<span data-ttu-id="3ac0b-278">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-278"></span></span>
|<span data-ttu-id="3ac0b-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-280">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-280">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-281">griechische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-281">greek passport number</span></span>  <br/> <span data-ttu-id="3ac0b-282">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-282">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-283">διαβατηριο</span><span class="sxs-lookup"><span data-stu-id="3ac0b-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="3ac0b-284">Ungarn</span><span class="sxs-lookup"><span data-stu-id="3ac0b-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-285">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-285">Format</span></span>

<span data-ttu-id="3ac0b-286">Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-287">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-287">Pattern</span></span>

<span data-ttu-id="3ac0b-288">Zwei Buchstaben, gefolgt von sechs oder sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-289">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-289">Checksum</span></span>

<span data-ttu-id="3ac0b-290">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-291">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-291">Definition</span></span>

<span data-ttu-id="3ac0b-292">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-293">Der reguläre Ausdruck `Regex_hungary_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-294">Ein Schlüsselwort `Keywords_hungary_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-295">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-295">Keywords</span></span>

<span data-ttu-id="3ac0b-296">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-296"></span></span>
|<span data-ttu-id="3ac0b-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-298">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-298">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-299">ungarische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-300">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-300">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-301">útlevél száma</span><span class="sxs-lookup"><span data-stu-id="3ac0b-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="3ac0b-302">Irland</span><span class="sxs-lookup"><span data-stu-id="3ac0b-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-303">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-303">Format</span></span>

<span data-ttu-id="3ac0b-304">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-305">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-305">Pattern</span></span>

<span data-ttu-id="3ac0b-306">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="3ac0b-307">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="3ac0b-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="3ac0b-308">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ac0b-309">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-309">Checksum</span></span>

<span data-ttu-id="3ac0b-310">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-311">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-311">Definition</span></span>

<span data-ttu-id="3ac0b-312">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-313">Der reguläre Ausdruck `Regex_ireland_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-314">Ein Schlüsselwort `Keywords_ireland_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-315">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-315">Keywords</span></span>

<span data-ttu-id="3ac0b-316">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-316"></span></span>
|<span data-ttu-id="3ac0b-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-318">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-318">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-319">irische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-319">irish passport number</span></span>  <br/> <span data-ttu-id="3ac0b-320">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-320">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-321">Pas</span><span class="sxs-lookup"><span data-stu-id="3ac0b-321">pas</span></span>  <br/> <span data-ttu-id="3ac0b-322">Pass</span><span class="sxs-lookup"><span data-stu-id="3ac0b-322">passport</span></span>  <br/> <span data-ttu-id="3ac0b-323">Passeport</span><span class="sxs-lookup"><span data-stu-id="3ac0b-323">passeport</span></span>  <br/> <span data-ttu-id="3ac0b-324">Passeport numero</span><span class="sxs-lookup"><span data-stu-id="3ac0b-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="3ac0b-325">Italien</span><span class="sxs-lookup"><span data-stu-id="3ac0b-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-326">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-326">Format</span></span>

<span data-ttu-id="3ac0b-327">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-328">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-328">Pattern</span></span>

<span data-ttu-id="3ac0b-329">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="3ac0b-330">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="3ac0b-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="3ac0b-331">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ac0b-332">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-332">Checksum</span></span>

<span data-ttu-id="3ac0b-333">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="3ac0b-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-334">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-334">Definition</span></span>

<span data-ttu-id="3ac0b-335">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-336">Der reguläre Ausdruck `Regex_italy_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-337">Ein Schlüsselwort `Keywords_italy_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-338">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-338">Keywords</span></span>

<span data-ttu-id="3ac0b-339">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-339"></span></span>
|<span data-ttu-id="3ac0b-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-341">italienische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-341">italian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-342">Repubblica Italiana Passa Porto</span><span class="sxs-lookup"><span data-stu-id="3ac0b-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="3ac0b-343">Passa Porto</span><span class="sxs-lookup"><span data-stu-id="3ac0b-343">passaporto</span></span>  <br/> <span data-ttu-id="3ac0b-344">Passa Porto Italiana</span><span class="sxs-lookup"><span data-stu-id="3ac0b-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="3ac0b-345">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-345">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-346">Italiana Passa Porto numero</span><span class="sxs-lookup"><span data-stu-id="3ac0b-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="3ac0b-347">Passa Porto numero</span><span class="sxs-lookup"><span data-stu-id="3ac0b-347">passaporto numero</span></span>  <br/> <span data-ttu-id="3ac0b-348">Numéro Passeport Italien</span><span class="sxs-lookup"><span data-stu-id="3ac0b-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="3ac0b-349">Numéro Passeport</span><span class="sxs-lookup"><span data-stu-id="3ac0b-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="3ac0b-350">Lettland</span><span class="sxs-lookup"><span data-stu-id="3ac0b-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-351">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-351">Format</span></span>

<span data-ttu-id="3ac0b-352">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-353">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-353">Pattern</span></span>

<span data-ttu-id="3ac0b-354">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="3ac0b-355">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="3ac0b-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="3ac0b-356">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ac0b-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-357">Checksum</span></span>

<span data-ttu-id="3ac0b-358">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-359">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-359">Definition</span></span>

<span data-ttu-id="3ac0b-360">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-361">Der reguläre Ausdruck `Regex_latvia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-362">Ein Schlüsselwort `Keywords_latvia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-363">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-363">Keywords</span></span>

<span data-ttu-id="3ac0b-364">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-364"></span></span>
|<span data-ttu-id="3ac0b-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-366">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-366">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-367">Lettische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-367">latvian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-368">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-368">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-369">Pase numurs</span><span class="sxs-lookup"><span data-stu-id="3ac0b-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="3ac0b-370">Litauen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-371">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-371">Format</span></span>

<span data-ttu-id="3ac0b-372">Acht Ziffern oder Buchstaben ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-373">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-373">Pattern</span></span>

<span data-ttu-id="3ac0b-374">Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="3ac0b-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-375">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-375">Checksum</span></span>

<span data-ttu-id="3ac0b-376">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="3ac0b-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-377">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-377">Definition</span></span>

<span data-ttu-id="3ac0b-378">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-379">Der reguläre Ausdruck `Regex_lithuania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-380">Ein Schlüsselwort `Keywords_lithuania_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-381">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-381">Keywords</span></span>

<span data-ttu-id="3ac0b-382">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-382"></span></span>
|<span data-ttu-id="3ac0b-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-384">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-384">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-385">lithunian Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-386">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-386">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-387">Paso Numeris</span><span class="sxs-lookup"><span data-stu-id="3ac0b-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="3ac0b-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="3ac0b-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-389">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-389">Format</span></span>

<span data-ttu-id="3ac0b-390">Acht Ziffern oder Buchstaben ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-391">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-391">Pattern</span></span>

<span data-ttu-id="3ac0b-392">Acht Ziffern oder Buchstaben (Groß-/Kleinschreibung nicht beachtet)</span><span class="sxs-lookup"><span data-stu-id="3ac0b-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-393">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-393">Checksum</span></span>

<span data-ttu-id="3ac0b-394">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-395">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-395">Definition</span></span>

<span data-ttu-id="3ac0b-396">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-397">Der reguläre Ausdruck `Regex_nation_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-398">Ein Schlüsselwort `Keywords_nation_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-399">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-399">Keywords</span></span>

<span data-ttu-id="3ac0b-400">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-400"></span></span>
|<span data-ttu-id="3ac0b-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-402">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-402">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-403">Lettische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-403">latvian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-404">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-404">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-405">passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="3ac0b-406">Malta</span><span class="sxs-lookup"><span data-stu-id="3ac0b-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-407">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-407">Format</span></span>

<span data-ttu-id="3ac0b-408">Sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-409">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-409">Pattern</span></span>

 <span data-ttu-id="3ac0b-410">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-411">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-411">Checksum</span></span>

<span data-ttu-id="3ac0b-412">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-413">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-413">Definition</span></span>

<span data-ttu-id="3ac0b-414">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-415">Der reguläre Ausdruck `Regex_malta_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-416">Ein Schlüsselwort `Keywords_malta_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-417">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-417">Keywords</span></span>

<span data-ttu-id="3ac0b-418">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-418"></span></span>
|<span data-ttu-id="3ac0b-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-420">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-420">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-421">Maltesische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-421">maltese passport number</span></span>  <br/> <span data-ttu-id="3ac0b-422">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-422">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-423">numru Tal-Passaport</span><span class="sxs-lookup"><span data-stu-id="3ac0b-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="3ac0b-424">Niederlande</span><span class="sxs-lookup"><span data-stu-id="3ac0b-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-425">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-425">Format</span></span>

<span data-ttu-id="3ac0b-426">Neun Buchstaben oder Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-427">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-427">Pattern</span></span>

<span data-ttu-id="3ac0b-428">Neun Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-429">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-429">Checksum</span></span>

<span data-ttu-id="3ac0b-430">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="3ac0b-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-431">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-431">Definition</span></span>

<span data-ttu-id="3ac0b-432">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-433">Der reguläre Ausdruck `Regex_netherlands_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-434">Ein Schlüsselwort `Keywords_netherlands_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-435">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-435">Keywords</span></span>

<span data-ttu-id="3ac0b-436">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-436"></span></span>
|<span data-ttu-id="3ac0b-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-438">niederländische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-438">dutch passport number</span></span>  <br/> <span data-ttu-id="3ac0b-439">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-439">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-440">niederländische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="3ac0b-441">Nederlanden paspoort Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="3ac0b-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="3ac0b-442">paspoort</span></span>  <br/> <span data-ttu-id="3ac0b-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="3ac0b-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="3ac0b-445">Polen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-445">Poland</span></span>

<span data-ttu-id="3ac0b-446">Ausführliche Informationen finden Sie im Abschnitt "Polen-Passport-Nummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3ac0b-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="3ac0b-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="3ac0b-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-448">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-448">Format</span></span>

<span data-ttu-id="3ac0b-449">Ein Buchstabe, gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-450">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-450">Pattern</span></span>

<span data-ttu-id="3ac0b-451">Ein Buchstabe, gefolgt von sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="3ac0b-452">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="3ac0b-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="3ac0b-453">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ac0b-454">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-454">Checksum</span></span>

<span data-ttu-id="3ac0b-455">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-456">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-456">Definition</span></span>

<span data-ttu-id="3ac0b-457">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-458">Der reguläre Ausdruck `Regex_portugal_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-459">Ein Schlüsselwort `Keywords_portugal_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-460">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-460">Keywords</span></span>

<span data-ttu-id="3ac0b-461">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-461"></span></span>
|<span data-ttu-id="3ac0b-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-463">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-463">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-464">portugiesische Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="3ac0b-465">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-465">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-466">número do passaporte</span><span class="sxs-lookup"><span data-stu-id="3ac0b-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="3ac0b-467">Rumänien</span><span class="sxs-lookup"><span data-stu-id="3ac0b-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-468">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-468">Format</span></span>

<span data-ttu-id="3ac0b-469">Acht oder neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-470">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-470">Pattern</span></span>

<span data-ttu-id="3ac0b-471">Acht oder neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-472">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-472">Checksum</span></span>

<span data-ttu-id="3ac0b-473">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-474">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-474">Definition</span></span>

<span data-ttu-id="3ac0b-475">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-476">Der reguläre Ausdruck `Regex_romania_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-477">Ein Schlüsselwort `Keywords_romania_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-478">Keywords</span></span>

<span data-ttu-id="3ac0b-479">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-479"></span></span>
|<span data-ttu-id="3ac0b-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-481">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-481">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-482">rumänische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-482">romanian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-483">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-483">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-484">numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="3ac0b-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="3ac0b-485">Slowakei</span><span class="sxs-lookup"><span data-stu-id="3ac0b-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-486">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-486">Format</span></span>

<span data-ttu-id="3ac0b-487">Eine Ziffer oder ein Buchstabe, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-488">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-488">Pattern</span></span>

<span data-ttu-id="3ac0b-489">Eine Ziffer oder ein Buchstabe (ohne Groß-/Kleinschreibung), gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="3ac0b-490">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-490">Checksum</span></span>

<span data-ttu-id="3ac0b-491">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-492">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-492">Definition</span></span>

<span data-ttu-id="3ac0b-493">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-494">Der reguläre Ausdruck `Regex_slovakia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-495">Ein Schlüsselwort `Keywords_slovakia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-496">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-496">Keywords</span></span>

<span data-ttu-id="3ac0b-497">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-497"></span></span>
|<span data-ttu-id="3ac0b-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-499">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-499">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-500">Slowakische Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-501">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-501">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-502">číslo Pasu</span><span class="sxs-lookup"><span data-stu-id="3ac0b-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="3ac0b-503">Slowenien</span><span class="sxs-lookup"><span data-stu-id="3ac0b-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-504">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-504">Format</span></span>

<span data-ttu-id="3ac0b-505">Zwei Buchstaben, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-506">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-506">Pattern</span></span>

<span data-ttu-id="3ac0b-507">Zwei Buchstaben, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="3ac0b-508">Der Buchstabe "P"</span><span class="sxs-lookup"><span data-stu-id="3ac0b-508">The letter "P"</span></span>
    
- <span data-ttu-id="3ac0b-509">Ein Großbuchstabe</span><span class="sxs-lookup"><span data-stu-id="3ac0b-509">One uppercase letter</span></span>
    
- <span data-ttu-id="3ac0b-510">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ac0b-511">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-511">Checksum</span></span>

<span data-ttu-id="3ac0b-512">Nein</span><span class="sxs-lookup"><span data-stu-id="3ac0b-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-513">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-513">Definition</span></span>

<span data-ttu-id="3ac0b-514">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-515">Der reguläre Ausdruck `Regex_slovenia_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-516">Ein Schlüsselwort `Keywords_slovenia_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-517">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-517">Keywords</span></span>

<span data-ttu-id="3ac0b-518">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-518"></span></span>
|<span data-ttu-id="3ac0b-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-520">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-520">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-521">slowenische Passnummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="3ac0b-522">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-522">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-523">številka potnega lista</span><span class="sxs-lookup"><span data-stu-id="3ac0b-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="3ac0b-524">Spanien</span><span class="sxs-lookup"><span data-stu-id="3ac0b-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="3ac0b-525">Format</span><span class="sxs-lookup"><span data-stu-id="3ac0b-525">Format</span></span>

<span data-ttu-id="3ac0b-526">Eine Kombination aus Buchstaben und Zahlen mit acht oder neun Zeichen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="3ac0b-527">Muster</span><span class="sxs-lookup"><span data-stu-id="3ac0b-527">Pattern</span></span>

<span data-ttu-id="3ac0b-528">Eine Kombination aus Buchstaben und Zahlen aus acht oder neun Zeichen:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="3ac0b-529">Zwei Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="3ac0b-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="3ac0b-530">Eine Ziffer oder ein Buchstabe (optional)</span><span class="sxs-lookup"><span data-stu-id="3ac0b-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="3ac0b-531">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="3ac0b-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="3ac0b-532">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="3ac0b-532">Checksum</span></span>

<span data-ttu-id="3ac0b-533">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="3ac0b-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="3ac0b-534">Definition</span><span class="sxs-lookup"><span data-stu-id="3ac0b-534">Definition</span></span>

<span data-ttu-id="3ac0b-535">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="3ac0b-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="3ac0b-536">Der reguläre Ausdruck `Regex_spain_eu_passport_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="3ac0b-537">Ein Schlüsselwort `Keywords_spain_eu_passport_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="3ac0b-538">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="3ac0b-538">Keywords</span></span>

<span data-ttu-id="3ac0b-539">| |</span><span class="sxs-lookup"><span data-stu-id="3ac0b-539"></span></span>
|<span data-ttu-id="3ac0b-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="3ac0b-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="3ac0b-541">Pass</span><span class="sxs-lookup"><span data-stu-id="3ac0b-541">passport</span></span>  <br/> <span data-ttu-id="3ac0b-542">Spanien-Passport</span><span class="sxs-lookup"><span data-stu-id="3ac0b-542">spain passport</span></span>  <br/> <span data-ttu-id="3ac0b-543">Passport-Buch</span><span class="sxs-lookup"><span data-stu-id="3ac0b-543">passport book</span></span>  <br/> <span data-ttu-id="3ac0b-544">passport number</span><span class="sxs-lookup"><span data-stu-id="3ac0b-544">passport number</span></span>  <br/> <span data-ttu-id="3ac0b-545">Passport-Nummer</span><span class="sxs-lookup"><span data-stu-id="3ac0b-545">passport no</span></span>  <br/> <span data-ttu-id="3ac0b-546">Libreta Pasaporte</span><span class="sxs-lookup"><span data-stu-id="3ac0b-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="3ac0b-547">número Pasaporte</span><span class="sxs-lookup"><span data-stu-id="3ac0b-547">número pasaporte</span></span>  <br/> <span data-ttu-id="3ac0b-548">ESPAÑA PASAPORTE</span><span class="sxs-lookup"><span data-stu-id="3ac0b-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="3ac0b-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="3ac0b-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="3ac0b-550">Schweden</span><span class="sxs-lookup"><span data-stu-id="3ac0b-550">Sweden</span></span>

<span data-ttu-id="3ac0b-551">Ausführliche Informationen finden Sie im Abschnitt "schwedische Passport-Nummer" unter [was die Typen für vertrauliche Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3ac0b-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="3ac0b-552">UK</span><span class="sxs-lookup"><span data-stu-id="3ac0b-552">UK</span></span>

<span data-ttu-id="3ac0b-553">Ausführliche Informationen finden Sie im Abschnitt "U.S./U.K.</span><span class="sxs-lookup"><span data-stu-id="3ac0b-553">For details, see the section "U.S. / U.K.</span></span> <span data-ttu-id="3ac0b-554">Passport-Nummer "in [dem, wonach die Typen vertraulicher Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="3ac0b-554">Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3ac0b-555">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ac0b-555">See also</span></span>

[<span data-ttu-id="3ac0b-556">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="3ac0b-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

