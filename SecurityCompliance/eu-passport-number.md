---
title: EU Reisepassnummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/16/2018
ms.audience: Admin
ms.topic: reference
ms.service: o365-administration
localization_priority: Normal
ms.assetid: 8c00df57-9fb3-459c-ba87-40480c87bd55
description: In diesem Thema dargestellt was eine Data Loss Prevention (DLP)-Richtlinie für den Typ der EU Reisepassnummer vertrauliche Daten erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 7a7fc1ff826aab4096c46535686eb0fd68173c6f
ms.sourcegitcommit: 7e2a0185cadea7f3a6afc5ddc445eac2e1ce22eb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2019
ms.locfileid: "25840324"
---
# <a name="eu-passport-number"></a><span data-ttu-id="40cd2-104">EU Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-104">EU Passport Number</span></span>

<span data-ttu-id="40cd2-p102">In diesem Thema dargestellt was eine Data Loss Prevention (DLP)-Richtlinie für den Typ der EU Reisepassnummer vertrauliche Daten erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="40cd2-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="40cd2-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="40cd2-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-108">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-108">Format</span></span>

<span data-ttu-id="40cd2-109">Einen Buchstaben gefolgt von einem optionalen Leerzeichen und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-110">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-110">Pattern</span></span>

<span data-ttu-id="40cd2-111">Eine Kombination von einem Buchstaben, sieben Ziffern und ein Leerzeichen:</span><span class="sxs-lookup"><span data-stu-id="40cd2-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="40cd2-112">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="40cd2-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="40cd2-113">Ein Leerzeichen (optional)</span><span class="sxs-lookup"><span data-stu-id="40cd2-113">One space (optional)</span></span>
    
- <span data-ttu-id="40cd2-114">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="40cd2-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-115">Checksum</span></span>

<span data-ttu-id="40cd2-116">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="40cd2-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-117">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-117">Definition</span></span>

<span data-ttu-id="40cd2-118">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-119">Der reguläre Ausdruck `Regex_austria_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-120">Ein Schlüsselwort aus `Keywords_austria_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-121">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-121">Keywords</span></span>

<span data-ttu-id="40cd2-122">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-122"></span></span>
|<span data-ttu-id="40cd2-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-124">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-124">passport number</span></span>  <br/> <span data-ttu-id="40cd2-125">österreichische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-125">austrian passport number</span></span>  <br/> <span data-ttu-id="40cd2-126">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-126">passport no</span></span>  <br/> <span data-ttu-id="40cd2-127">Reisepass</span><span class="sxs-lookup"><span data-stu-id="40cd2-127">reisepass</span></span>  <br/> <span data-ttu-id="40cd2-128">Österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="40cd2-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="40cd2-129">Belgien</span><span class="sxs-lookup"><span data-stu-id="40cd2-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-130">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-130">Format</span></span>

<span data-ttu-id="40cd2-131">Zwei Buchstaben gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-132">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-132">Pattern</span></span>

<span data-ttu-id="40cd2-133">Zwei Buchstaben und gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-134">Checksum</span></span>

<span data-ttu-id="40cd2-135">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="40cd2-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-136">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-136">Definition</span></span>

<span data-ttu-id="40cd2-137">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-138">Der reguläre Ausdruck `Regex_belgium_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-139">Ein Schlüsselwort aus `Keywords_belgium_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-140">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-140">Keywords</span></span>

<span data-ttu-id="40cd2-141">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-141"></span></span>
|<span data-ttu-id="40cd2-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-143">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-143">passport number</span></span>  <br/> <span data-ttu-id="40cd2-144">belgische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-144">belgian passport number</span></span>  <br/> <span data-ttu-id="40cd2-145">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-145">passport no</span></span>  <br/> <span data-ttu-id="40cd2-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="40cd2-146">paspoort</span></span>  <br/> <span data-ttu-id="40cd2-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="40cd2-148">Kein Reisepass</span><span class="sxs-lookup"><span data-stu-id="40cd2-148">reisepass kein</span></span>  <br/> <span data-ttu-id="40cd2-149">Reisepass</span><span class="sxs-lookup"><span data-stu-id="40cd2-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="40cd2-150">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="40cd2-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-151">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-151">Format</span></span>

<span data-ttu-id="40cd2-152">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-153">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-153">Pattern</span></span>

 <span data-ttu-id="40cd2-154">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="40cd2-155">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-155">Checksum</span></span>

<span data-ttu-id="40cd2-156">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-157">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-157">Definition</span></span>

<span data-ttu-id="40cd2-158">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-159">Der reguläre Ausdruck `Regex_bulgaria_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-160">Ein Schlüsselwort aus `Keywords_bulgaria_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-161">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-161">Keywords</span></span>

<span data-ttu-id="40cd2-162">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-162"></span></span>
|<span data-ttu-id="40cd2-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-164">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-164">passport number</span></span>  <br/> <span data-ttu-id="40cd2-165">Bulgarisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="40cd2-166">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-166">passport no</span></span>  <br/> <span data-ttu-id="40cd2-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="40cd2-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="40cd2-168">Kroatien</span><span class="sxs-lookup"><span data-stu-id="40cd2-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-169">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-169">Format</span></span>

<span data-ttu-id="40cd2-170">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-171">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-171">Pattern</span></span>

 <span data-ttu-id="40cd2-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="40cd2-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-173">Checksum</span></span>

<span data-ttu-id="40cd2-174">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-175">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-175">Definition</span></span>

<span data-ttu-id="40cd2-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-177">Der reguläre Ausdruck `Regex_croatia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-178">Ein Schlüsselwort aus `Keywords_croatia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-179">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-179">Keywords</span></span>

<span data-ttu-id="40cd2-180">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-180"></span></span>
|<span data-ttu-id="40cd2-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-182">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-182">passport number</span></span>  <br/> <span data-ttu-id="40cd2-183">Kroatisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-183">croatian passport number</span></span>  <br/> <span data-ttu-id="40cd2-184">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-184">passport no</span></span>  <br/> <span data-ttu-id="40cd2-185">Broj putovnice</span><span class="sxs-lookup"><span data-stu-id="40cd2-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="40cd2-186">Zypern</span><span class="sxs-lookup"><span data-stu-id="40cd2-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-187">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-187">Format</span></span>

<span data-ttu-id="40cd2-188">Einen Buchstaben gefolgt von 6 bis 8 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-189">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-189">Pattern</span></span>

<span data-ttu-id="40cd2-190">Ein Zeichen, gefolgt von sechs bis acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-191">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-191">Checksum</span></span>

<span data-ttu-id="40cd2-192">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-193">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-193">Definition</span></span>

<span data-ttu-id="40cd2-194">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-195">Der reguläre Ausdruck `Regex_cyprus_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-196">Ein Schlüsselwort aus `Keywords_cyprus_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-197">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-197">Keywords</span></span>

<span data-ttu-id="40cd2-198">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-198"></span></span>
|<span data-ttu-id="40cd2-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-200">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-200">passport number</span></span>  <br/> <span data-ttu-id="40cd2-201">Zypern Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="40cd2-202">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-202">passport no</span></span>  <br/> <span data-ttu-id="40cd2-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="40cd2-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="40cd2-204">Tschechien</span><span class="sxs-lookup"><span data-stu-id="40cd2-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-205">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-205">Format</span></span>

<span data-ttu-id="40cd2-206">Acht Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-207">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-207">Pattern</span></span>

<span data-ttu-id="40cd2-208">Acht Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-209">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-209">Checksum</span></span>

<span data-ttu-id="40cd2-210">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-211">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-211">Definition</span></span>

<span data-ttu-id="40cd2-212">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-213">Der reguläre Ausdruck `Regex_czech_republic_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-214">Ein Schlüsselwort aus `Keywords_czech_republic_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-215">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-215">Keywords</span></span>

<span data-ttu-id="40cd2-216">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-216"></span></span>
|<span data-ttu-id="40cd2-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-218">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-218">passport number</span></span>  <br/> <span data-ttu-id="40cd2-219">Tschechische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-219">czech passport number</span></span>  <br/> <span data-ttu-id="40cd2-220">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-220">passport no</span></span>  <br/> <span data-ttu-id="40cd2-221">Cestovní pas</span><span class="sxs-lookup"><span data-stu-id="40cd2-221">cestovní pas</span></span>  <br/> <span data-ttu-id="40cd2-222">PAS</span><span class="sxs-lookup"><span data-stu-id="40cd2-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="40cd2-223">Dänemark</span><span class="sxs-lookup"><span data-stu-id="40cd2-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-224">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-224">Format</span></span>

<span data-ttu-id="40cd2-225">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-226">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-226">Pattern</span></span>

 <span data-ttu-id="40cd2-227">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="40cd2-228">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-228">Checksum</span></span>

<span data-ttu-id="40cd2-229">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-230">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-230">Definition</span></span>

<span data-ttu-id="40cd2-231">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-232">Der reguläre Ausdruck `Regex_denmark_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-233">Ein Schlüsselwort aus `Keywords_denmark_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-234">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-234">Keywords</span></span>

<span data-ttu-id="40cd2-235">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-235"></span></span>
|<span data-ttu-id="40cd2-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-237">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-237">passport number</span></span>  <br/> <span data-ttu-id="40cd2-238">Dänische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-238">danish passport number</span></span>  <br/> <span data-ttu-id="40cd2-239">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-239">passport no</span></span>  <br/> <span data-ttu-id="40cd2-240">PAS</span><span class="sxs-lookup"><span data-stu-id="40cd2-240">pas</span></span>  <br/> <span data-ttu-id="40cd2-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="40cd2-242">Estland</span><span class="sxs-lookup"><span data-stu-id="40cd2-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-243">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-243">Format</span></span>

<span data-ttu-id="40cd2-244">Einen Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-245">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-245">Pattern</span></span>

<span data-ttu-id="40cd2-246">Einen Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-247">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-247">Checksum</span></span>

<span data-ttu-id="40cd2-248">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-249">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-249">Definition</span></span>

<span data-ttu-id="40cd2-250">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-251">Der reguläre Ausdruck `Regex_estonia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-252">Ein Schlüsselwort aus `Keywords_estonia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-253">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-253">Keywords</span></span>

<span data-ttu-id="40cd2-254">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-254"></span></span>
|<span data-ttu-id="40cd2-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-256">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-256">passport number</span></span>  <br/> <span data-ttu-id="40cd2-257">Estnisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-257">estonian passport number</span></span>  <br/> <span data-ttu-id="40cd2-258">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-258">passport no</span></span>  <br/> <span data-ttu-id="40cd2-259">übergeben Sie Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="40cd2-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="40cd2-260">Finnland</span><span class="sxs-lookup"><span data-stu-id="40cd2-260">Finland</span></span>

<span data-ttu-id="40cd2-261">Weitere Informationen hierzu finden Sie im Abschnitt "Finnland Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="40cd2-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="40cd2-262">Frankreich</span><span class="sxs-lookup"><span data-stu-id="40cd2-262">France</span></span>

<span data-ttu-id="40cd2-263">Weitere Informationen hierzu finden Sie im Abschnitt "Französische Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="40cd2-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="40cd2-264">Deutschland</span><span class="sxs-lookup"><span data-stu-id="40cd2-264">Germany</span></span>

<span data-ttu-id="40cd2-265">Weitere Informationen hierzu finden Sie im Abschnitt "Deutschland Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="40cd2-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="40cd2-266">Griechenland</span><span class="sxs-lookup"><span data-stu-id="40cd2-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-267">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-267">Format</span></span>

<span data-ttu-id="40cd2-268">Zwei Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-269">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-269">Pattern</span></span>

<span data-ttu-id="40cd2-270">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-271">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-271">Checksum</span></span>

<span data-ttu-id="40cd2-272">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-273">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-273">Definition</span></span>

<span data-ttu-id="40cd2-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-275">Der reguläre Ausdruck `Regex_greece_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-276">Ein Schlüsselwort aus `Keywords_greece_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-277">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-277">Keywords</span></span>

<span data-ttu-id="40cd2-278">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-278"></span></span>
|<span data-ttu-id="40cd2-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-280">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-280">passport number</span></span>  <br/> <span data-ttu-id="40cd2-281">Griechische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-281">greek passport number</span></span>  <br/> <span data-ttu-id="40cd2-282">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-282">passport no</span></span>  <br/> <span data-ttu-id="40cd2-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="40cd2-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="40cd2-284">Ungarn</span><span class="sxs-lookup"><span data-stu-id="40cd2-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-285">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-285">Format</span></span>

<span data-ttu-id="40cd2-286">Zwei Buchstaben gefolgt von sechs oder sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-287">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-287">Pattern</span></span>

<span data-ttu-id="40cd2-288">Zwei Buchstaben gefolgt von sechs oder sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-289">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-289">Checksum</span></span>

<span data-ttu-id="40cd2-290">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-291">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-291">Definition</span></span>

<span data-ttu-id="40cd2-292">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-293">Der reguläre Ausdruck `Regex_hungary_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-294">Ein Schlüsselwort aus `Keywords_hungary_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-295">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-295">Keywords</span></span>

<span data-ttu-id="40cd2-296">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-296"></span></span>
|<span data-ttu-id="40cd2-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-298">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-298">passport number</span></span>  <br/> <span data-ttu-id="40cd2-299">Ungarisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="40cd2-300">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-300">passport no</span></span>  <br/> <span data-ttu-id="40cd2-301">Útlevél száma</span><span class="sxs-lookup"><span data-stu-id="40cd2-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="40cd2-302">Irland</span><span class="sxs-lookup"><span data-stu-id="40cd2-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-303">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-303">Format</span></span>

<span data-ttu-id="40cd2-304">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-305">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-305">Pattern</span></span>

<span data-ttu-id="40cd2-306">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="40cd2-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="40cd2-307">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="40cd2-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="40cd2-308">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="40cd2-309">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-309">Checksum</span></span>

<span data-ttu-id="40cd2-310">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-311">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-311">Definition</span></span>

<span data-ttu-id="40cd2-312">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-313">Der reguläre Ausdruck `Regex_ireland_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-314">Ein Schlüsselwort aus `Keywords_ireland_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-315">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-315">Keywords</span></span>

<span data-ttu-id="40cd2-316">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-316"></span></span>
|<span data-ttu-id="40cd2-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-318">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-318">passport number</span></span>  <br/> <span data-ttu-id="40cd2-319">Irland Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-319">irish passport number</span></span>  <br/> <span data-ttu-id="40cd2-320">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-320">passport no</span></span>  <br/> <span data-ttu-id="40cd2-321">PAS</span><span class="sxs-lookup"><span data-stu-id="40cd2-321">pas</span></span>  <br/> <span data-ttu-id="40cd2-322">passport</span><span class="sxs-lookup"><span data-stu-id="40cd2-322">passport</span></span>  <br/> <span data-ttu-id="40cd2-323">passeport</span><span class="sxs-lookup"><span data-stu-id="40cd2-323">passeport</span></span>  <br/> <span data-ttu-id="40cd2-324">Passeport numero</span><span class="sxs-lookup"><span data-stu-id="40cd2-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="40cd2-325">Italien</span><span class="sxs-lookup"><span data-stu-id="40cd2-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-326">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-326">Format</span></span>

<span data-ttu-id="40cd2-327">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-328">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-328">Pattern</span></span>

<span data-ttu-id="40cd2-329">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="40cd2-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="40cd2-330">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="40cd2-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="40cd2-331">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="40cd2-332">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-332">Checksum</span></span>

<span data-ttu-id="40cd2-333">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="40cd2-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-334">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-334">Definition</span></span>

<span data-ttu-id="40cd2-335">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-336">Der reguläre Ausdruck `Regex_italy_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-337">Ein Schlüsselwort aus `Keywords_italy_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-338">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-338">Keywords</span></span>

<span data-ttu-id="40cd2-339">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-339"></span></span>
|<span data-ttu-id="40cd2-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-341">Italienische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-341">italian passport number</span></span>  <br/> <span data-ttu-id="40cd2-342">Repubblica Italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="40cd2-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="40cd2-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="40cd2-343">passaporto</span></span>  <br/> <span data-ttu-id="40cd2-344">Passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="40cd2-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="40cd2-345">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-345">passport number</span></span>  <br/> <span data-ttu-id="40cd2-346">Italiana Passaporto numero</span><span class="sxs-lookup"><span data-stu-id="40cd2-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="40cd2-347">Passaporto numero</span><span class="sxs-lookup"><span data-stu-id="40cd2-347">passaporto numero</span></span>  <br/> <span data-ttu-id="40cd2-348">Numéro Passeport italien</span><span class="sxs-lookup"><span data-stu-id="40cd2-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="40cd2-349">Numéro passeport</span><span class="sxs-lookup"><span data-stu-id="40cd2-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="40cd2-350">Lettland</span><span class="sxs-lookup"><span data-stu-id="40cd2-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-351">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-351">Format</span></span>

<span data-ttu-id="40cd2-352">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-353">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-353">Pattern</span></span>

<span data-ttu-id="40cd2-354">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="40cd2-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="40cd2-355">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="40cd2-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="40cd2-356">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="40cd2-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-357">Checksum</span></span>

<span data-ttu-id="40cd2-358">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-359">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-359">Definition</span></span>

<span data-ttu-id="40cd2-360">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-361">Der reguläre Ausdruck `Regex_latvia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-362">Ein Schlüsselwort aus `Keywords_latvia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-363">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-363">Keywords</span></span>

<span data-ttu-id="40cd2-364">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-364"></span></span>
|<span data-ttu-id="40cd2-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-366">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-366">passport number</span></span>  <br/> <span data-ttu-id="40cd2-367">Lettisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-367">latvian passport number</span></span>  <br/> <span data-ttu-id="40cd2-368">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-368">passport no</span></span>  <br/> <span data-ttu-id="40cd2-369">Pase numurs</span><span class="sxs-lookup"><span data-stu-id="40cd2-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="40cd2-370">Litauen</span><span class="sxs-lookup"><span data-stu-id="40cd2-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-371">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-371">Format</span></span>

<span data-ttu-id="40cd2-372">Acht Ziffern oder Buchstaben ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-373">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-373">Pattern</span></span>

<span data-ttu-id="40cd2-374">Acht Ziffern oder Buchstaben (ohne Beachtung von Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="40cd2-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-375">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-375">Checksum</span></span>

<span data-ttu-id="40cd2-376">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="40cd2-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-377">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-377">Definition</span></span>

<span data-ttu-id="40cd2-378">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-379">Der reguläre Ausdruck `Regex_lithuania_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-380">Ein Schlüsselwort aus `Keywords_lithuania_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-381">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-381">Keywords</span></span>

<span data-ttu-id="40cd2-382">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-382"></span></span>
|<span data-ttu-id="40cd2-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-384">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-384">passport number</span></span>  <br/> <span data-ttu-id="40cd2-385">Lithunian Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="40cd2-386">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-386">passport no</span></span>  <br/> <span data-ttu-id="40cd2-387">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="40cd2-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="40cd2-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="40cd2-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-389">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-389">Format</span></span>

<span data-ttu-id="40cd2-390">Acht Ziffern oder Buchstaben ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-391">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-391">Pattern</span></span>

<span data-ttu-id="40cd2-392">Acht Ziffern oder Buchstaben (ohne Beachtung von Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="40cd2-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-393">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-393">Checksum</span></span>

<span data-ttu-id="40cd2-394">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-395">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-395">Definition</span></span>

<span data-ttu-id="40cd2-396">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-397">Der reguläre Ausdruck `Regex_nation_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-398">Ein Schlüsselwort aus `Keywords_nation_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-399">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-399">Keywords</span></span>

<span data-ttu-id="40cd2-400">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-400"></span></span>
|<span data-ttu-id="40cd2-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-402">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-402">passport number</span></span>  <br/> <span data-ttu-id="40cd2-403">Lettisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-403">latvian passport number</span></span>  <br/> <span data-ttu-id="40cd2-404">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-404">passport no</span></span>  <br/> <span data-ttu-id="40cd2-405">Passnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="40cd2-406">Malta</span><span class="sxs-lookup"><span data-stu-id="40cd2-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-407">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-407">Format</span></span>

<span data-ttu-id="40cd2-408">Sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-409">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-409">Pattern</span></span>

 <span data-ttu-id="40cd2-410">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="40cd2-411">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-411">Checksum</span></span>

<span data-ttu-id="40cd2-412">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-413">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-413">Definition</span></span>

<span data-ttu-id="40cd2-414">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-415">Der reguläre Ausdruck `Regex_malta_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-416">Ein Schlüsselwort aus `Keywords_malta_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-417">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-417">Keywords</span></span>

<span data-ttu-id="40cd2-418">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-418"></span></span>
|<span data-ttu-id="40cd2-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-420">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-420">passport number</span></span>  <br/> <span data-ttu-id="40cd2-421">Maltesisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-421">maltese passport number</span></span>  <br/> <span data-ttu-id="40cd2-422">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-422">passport no</span></span>  <br/> <span data-ttu-id="40cd2-423">Numru Tal-passaport</span><span class="sxs-lookup"><span data-stu-id="40cd2-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="40cd2-424">Niederlande</span><span class="sxs-lookup"><span data-stu-id="40cd2-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-425">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-425">Format</span></span>

<span data-ttu-id="40cd2-426">Neun Buchstaben oder Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-427">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-427">Pattern</span></span>

<span data-ttu-id="40cd2-428">Neun Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-429">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-429">Checksum</span></span>

<span data-ttu-id="40cd2-430">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="40cd2-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-431">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-431">Definition</span></span>

<span data-ttu-id="40cd2-432">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-433">Der reguläre Ausdruck `Regex_netherlands_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-434">Ein Schlüsselwort aus `Keywords_netherlands_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-435">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-435">Keywords</span></span>

<span data-ttu-id="40cd2-436">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-436"></span></span>
|<span data-ttu-id="40cd2-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-438">Niederländische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-438">dutch passport number</span></span>  <br/> <span data-ttu-id="40cd2-439">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-439">passport number</span></span>  <br/> <span data-ttu-id="40cd2-440">Niederlande Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="40cd2-441">Nederlanden Paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="40cd2-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="40cd2-442">paspoort</span></span>  <br/> <span data-ttu-id="40cd2-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="40cd2-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="40cd2-445">Polen</span><span class="sxs-lookup"><span data-stu-id="40cd2-445">Poland</span></span>

<span data-ttu-id="40cd2-446">Weitere Informationen hierzu finden Sie im Abschnitt "Polen Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="40cd2-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="40cd2-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="40cd2-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-448">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-448">Format</span></span>

<span data-ttu-id="40cd2-449">Ein Zeichen, gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-450">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-450">Pattern</span></span>

<span data-ttu-id="40cd2-451">Einen Buchstaben gefolgt von sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="40cd2-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="40cd2-452">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="40cd2-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="40cd2-453">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="40cd2-454">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-454">Checksum</span></span>

<span data-ttu-id="40cd2-455">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-456">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-456">Definition</span></span>

<span data-ttu-id="40cd2-457">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-458">Der reguläre Ausdruck `Regex_portugal_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-459">Ein Schlüsselwort aus `Keywords_portugal_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-460">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-460">Keywords</span></span>

<span data-ttu-id="40cd2-461">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-461"></span></span>
|<span data-ttu-id="40cd2-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-463">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-463">passport number</span></span>  <br/> <span data-ttu-id="40cd2-464">Portugiesisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-464">portuguese passport number</span></span>  <br/> <span data-ttu-id="40cd2-465">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-465">passport no</span></span>  <br/> <span data-ttu-id="40cd2-466">Número passaporte</span><span class="sxs-lookup"><span data-stu-id="40cd2-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="40cd2-467">Rumänien</span><span class="sxs-lookup"><span data-stu-id="40cd2-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-468">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-468">Format</span></span>

<span data-ttu-id="40cd2-469">Acht oder neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-470">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-470">Pattern</span></span>

<span data-ttu-id="40cd2-471">Acht oder neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-472">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-472">Checksum</span></span>

<span data-ttu-id="40cd2-473">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-474">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-474">Definition</span></span>

<span data-ttu-id="40cd2-475">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-476">Der reguläre Ausdruck `Regex_romania_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-477">Ein Schlüsselwort aus `Keywords_romania_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-478">Keywords</span></span>

<span data-ttu-id="40cd2-479">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-479"></span></span>
|<span data-ttu-id="40cd2-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-481">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-481">passport number</span></span>  <br/> <span data-ttu-id="40cd2-482">Rumänisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-482">romanian passport number</span></span>  <br/> <span data-ttu-id="40cd2-483">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-483">passport no</span></span>  <br/> <span data-ttu-id="40cd2-484">Numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="40cd2-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="40cd2-485">Slowakei</span><span class="sxs-lookup"><span data-stu-id="40cd2-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-486">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-486">Format</span></span>

<span data-ttu-id="40cd2-487">Eine Ziffern oder Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-488">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-488">Pattern</span></span>

<span data-ttu-id="40cd2-489">Eine Ziffern oder Buchstaben (ohne Beachtung von Groß-/Kleinschreibung) gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="40cd2-490">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-490">Checksum</span></span>

<span data-ttu-id="40cd2-491">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-492">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-492">Definition</span></span>

<span data-ttu-id="40cd2-493">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-494">Der reguläre Ausdruck `Regex_slovakia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-495">Ein Schlüsselwort aus `Keywords_slovakia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-496">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-496">Keywords</span></span>

<span data-ttu-id="40cd2-497">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-497"></span></span>
|<span data-ttu-id="40cd2-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-499">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-499">passport number</span></span>  <br/> <span data-ttu-id="40cd2-500">Slowakische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="40cd2-501">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-501">passport no</span></span>  <br/> <span data-ttu-id="40cd2-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="40cd2-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="40cd2-503">Slowenien</span><span class="sxs-lookup"><span data-stu-id="40cd2-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-504">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-504">Format</span></span>

<span data-ttu-id="40cd2-505">Zwei Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-506">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-506">Pattern</span></span>

<span data-ttu-id="40cd2-507">Zwei Buchstaben gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="40cd2-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="40cd2-508">Der Buchstabe "P"</span><span class="sxs-lookup"><span data-stu-id="40cd2-508">The letter "P"</span></span>
    
- <span data-ttu-id="40cd2-509">Einen Großbuchstaben</span><span class="sxs-lookup"><span data-stu-id="40cd2-509">One uppercase letter</span></span>
    
- <span data-ttu-id="40cd2-510">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="40cd2-511">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-511">Checksum</span></span>

<span data-ttu-id="40cd2-512">Nein</span><span class="sxs-lookup"><span data-stu-id="40cd2-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-513">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-513">Definition</span></span>

<span data-ttu-id="40cd2-514">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-515">Der reguläre Ausdruck `Regex_slovenia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-516">Ein Schlüsselwort aus `Keywords_slovenia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-517">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-517">Keywords</span></span>

<span data-ttu-id="40cd2-518">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-518"></span></span>
|<span data-ttu-id="40cd2-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-520">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-520">passport number</span></span>  <br/> <span data-ttu-id="40cd2-521">Slowenisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="40cd2-522">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-522">passport no</span></span>  <br/> <span data-ttu-id="40cd2-523">Številka Potnega lista</span><span class="sxs-lookup"><span data-stu-id="40cd2-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="40cd2-524">Spanien</span><span class="sxs-lookup"><span data-stu-id="40cd2-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="40cd2-525">Format</span><span class="sxs-lookup"><span data-stu-id="40cd2-525">Format</span></span>

<span data-ttu-id="40cd2-526">Eine acht oder neun Zeichen Kombination von Buchstaben und Zahlen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="40cd2-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="40cd2-527">Muster</span><span class="sxs-lookup"><span data-stu-id="40cd2-527">Pattern</span></span>

<span data-ttu-id="40cd2-528">Eine Kombination der acht oder neun Zeichen Buchstaben und Zahlen:</span><span class="sxs-lookup"><span data-stu-id="40cd2-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="40cd2-529">Zwei Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="40cd2-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="40cd2-530">Eine Ziffern oder Buchstaben (optional)</span><span class="sxs-lookup"><span data-stu-id="40cd2-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="40cd2-531">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="40cd2-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="40cd2-532">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="40cd2-532">Checksum</span></span>

<span data-ttu-id="40cd2-533">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="40cd2-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="40cd2-534">Definition</span><span class="sxs-lookup"><span data-stu-id="40cd2-534">Definition</span></span>

<span data-ttu-id="40cd2-535">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="40cd2-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="40cd2-536">Der reguläre Ausdruck `Regex_spain_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="40cd2-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="40cd2-537">Ein Schlüsselwort aus `Keywords_spain_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="40cd2-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="40cd2-538">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="40cd2-538">Keywords</span></span>

<span data-ttu-id="40cd2-539">| |</span><span class="sxs-lookup"><span data-stu-id="40cd2-539"></span></span>
|<span data-ttu-id="40cd2-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="40cd2-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="40cd2-541">passport</span><span class="sxs-lookup"><span data-stu-id="40cd2-541">passport</span></span>  <br/> <span data-ttu-id="40cd2-542">Spanien passport</span><span class="sxs-lookup"><span data-stu-id="40cd2-542">spain passport</span></span>  <br/> <span data-ttu-id="40cd2-543">Passport-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="40cd2-543">passport book</span></span>  <br/> <span data-ttu-id="40cd2-544">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="40cd2-544">passport number</span></span>  <br/> <span data-ttu-id="40cd2-545">Passport keine</span><span class="sxs-lookup"><span data-stu-id="40cd2-545">passport no</span></span>  <br/> <span data-ttu-id="40cd2-546">Libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="40cd2-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="40cd2-547">Número pasaporte</span><span class="sxs-lookup"><span data-stu-id="40cd2-547">número pasaporte</span></span>  <br/> <span data-ttu-id="40cd2-548">España pasaporte</span><span class="sxs-lookup"><span data-stu-id="40cd2-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="40cd2-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="40cd2-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="40cd2-550">Schweden</span><span class="sxs-lookup"><span data-stu-id="40cd2-550">Sweden</span></span>

<span data-ttu-id="40cd2-551">Weitere Informationen hierzu finden Sie im Abschnitt "Schwedische Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="40cd2-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="40cd2-552">GROßBRITANNIEN</span><span class="sxs-lookup"><span data-stu-id="40cd2-552">UK</span></span>

<span data-ttu-id="40cd2-p103">Weitere Informationen hierzu finden Sie im Abschnitt "US / Großbritannien Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="40cd2-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40cd2-555">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40cd2-555">See also</span></span>

[<span data-ttu-id="40cd2-556">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="40cd2-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

