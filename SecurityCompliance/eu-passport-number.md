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
ms.openlocfilehash: 71acc39b885c057e1771ec13b2f3c25017ac1bb6
ms.sourcegitcommit: 36c5466056cdef6ad2a8d9372f2bc009a30892bb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/27/2018
ms.locfileid: "22529535"
---
# <a name="eu-passport-number"></a><span data-ttu-id="923b6-104">EU Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-104">EU Passport Number</span></span>

<span data-ttu-id="923b6-p102">In diesem Thema dargestellt was eine Data Loss Prevention (DLP)-Richtlinie für den Typ der EU Reisepassnummer vertrauliche Daten erkannt. Dieses Typs vertrauliche Informationen definiert unterschiedliche Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="923b6-p102">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Passport Number sensitive information type. This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="923b6-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="923b6-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="923b6-108">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-108">Format</span></span>

<span data-ttu-id="923b6-109">Einen Buchstaben gefolgt von einem optionalen Leerzeichen und sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-109">One letter followed by an optional space and seven digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-110">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-110">Pattern</span></span>

<span data-ttu-id="923b6-111">Eine Kombination von einem Buchstaben, sieben Ziffern und ein Leerzeichen:</span><span class="sxs-lookup"><span data-stu-id="923b6-111">A combination of one letter, seven digits, and one space:</span></span>
  
- <span data-ttu-id="923b6-112">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="923b6-112">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="923b6-113">Ein Leerzeichen (optional)</span><span class="sxs-lookup"><span data-stu-id="923b6-113">One space (optional)</span></span>
    
- <span data-ttu-id="923b6-114">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-114">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="923b6-115">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-115">Checksum</span></span>

<span data-ttu-id="923b6-116">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="923b6-116">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-117">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-117">Definition</span></span>

<span data-ttu-id="923b6-118">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-118">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-119">Der reguläre Ausdruck `Regex_austria_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-119">The regular expression  `Regex_austria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-120">Ein Schlüsselwort aus `Keywords_austria_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-120">A keyword from  `Keywords_austria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_austria_eu_passport_number" />
          <Match idRef="Keywords_austria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-121">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-121">Keywords</span></span>

<span data-ttu-id="923b6-122">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-122"></span></span>
|<span data-ttu-id="923b6-123">**Keywords_austria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-123">**Keywords_austria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-124">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-124">passport number</span></span>  <br/> <span data-ttu-id="923b6-125">österreichische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-125">austrian passport number</span></span>  <br/> <span data-ttu-id="923b6-126">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-126">passport no</span></span>  <br/> <span data-ttu-id="923b6-127">Reisepass</span><span class="sxs-lookup"><span data-stu-id="923b6-127">reisepass</span></span>  <br/> <span data-ttu-id="923b6-128">Österreichisch reisepass</span><span class="sxs-lookup"><span data-stu-id="923b6-128">österreichisch reisepass</span></span>  <br/> |
   
## <a name="belgium"></a><span data-ttu-id="923b6-129">Belgien</span><span class="sxs-lookup"><span data-stu-id="923b6-129">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="923b6-130">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-130">Format</span></span>

<span data-ttu-id="923b6-131">Zwei Buchstaben gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-131">Two letters followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-132">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-132">Pattern</span></span>

<span data-ttu-id="923b6-133">Zwei Buchstaben und gefolgt von sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-133">Two letters and followed by six digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-134">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-134">Checksum</span></span>

<span data-ttu-id="923b6-135">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="923b6-135">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-136">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-136">Definition</span></span>

<span data-ttu-id="923b6-137">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-137">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-138">Der reguläre Ausdruck `Regex_belgium_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-138">The regular expression  `Regex_belgium_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-139">Ein Schlüsselwort aus `Keywords_belgium_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-139">A keyword from  `Keywords_belgium_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium__eu_passport_number" />
          <Match idRef="Keywords_belgium_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-140">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-140">Keywords</span></span>

<span data-ttu-id="923b6-141">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-141"></span></span>
|<span data-ttu-id="923b6-142">**Keywords_belgium_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-142">**Keywords_belgium_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-143">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-143">passport number</span></span>  <br/> <span data-ttu-id="923b6-144">belgische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-144">belgian passport number</span></span>  <br/> <span data-ttu-id="923b6-145">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-145">passport no</span></span>  <br/> <span data-ttu-id="923b6-146">paspoort</span><span class="sxs-lookup"><span data-stu-id="923b6-146">paspoort</span></span>  <br/> <span data-ttu-id="923b6-147">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-147">paspoortnummer</span></span>  <br/> <span data-ttu-id="923b6-148">Kein Reisepass</span><span class="sxs-lookup"><span data-stu-id="923b6-148">reisepass kein</span></span>  <br/> <span data-ttu-id="923b6-149">Reisepass</span><span class="sxs-lookup"><span data-stu-id="923b6-149">reisepass</span></span>  <br/> |
   
## <a name="bulgaria"></a><span data-ttu-id="923b6-150">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="923b6-150">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="923b6-151">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-151">Format</span></span>

<span data-ttu-id="923b6-152">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-152">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-153">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-153">Pattern</span></span>

 <span data-ttu-id="923b6-154">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-154">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="923b6-155">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-155">Checksum</span></span>

<span data-ttu-id="923b6-156">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-156">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-157">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-157">Definition</span></span>

<span data-ttu-id="923b6-158">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-158">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-159">Der reguläre Ausdruck `Regex_bulgaria_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-159">The regular expression  `Regex_bulgaria_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-160">Ein Schlüsselwort aus `Keywords_bulgaria_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-160">A keyword from  `Keywords_bulgaria_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_bulgaria_eu_passport_number" />
          <Match idRef="Keywords_bulgaria_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-161">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-161">Keywords</span></span>

<span data-ttu-id="923b6-162">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-162"></span></span>
|<span data-ttu-id="923b6-163">**Keywords_bulgaria_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-163">**Keywords_bulgaria_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-164">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-164">passport number</span></span>  <br/> <span data-ttu-id="923b6-165">Bulgarisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-165">bulgarian passport number</span></span>  <br/> <span data-ttu-id="923b6-166">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-166">passport no</span></span>  <br/> <span data-ttu-id="923b6-167">НОМЕР НА ПАСПОРТА</span><span class="sxs-lookup"><span data-stu-id="923b6-167">номер на паспорта</span></span>  <br/> |
   
## <a name="croatia"></a><span data-ttu-id="923b6-168">Kroatien</span><span class="sxs-lookup"><span data-stu-id="923b6-168">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="923b6-169">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-169">Format</span></span>

<span data-ttu-id="923b6-170">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-170">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-171">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-171">Pattern</span></span>

 <span data-ttu-id="923b6-172">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-172">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="923b6-173">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-173">Checksum</span></span>

<span data-ttu-id="923b6-174">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-174">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-175">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-175">Definition</span></span>

<span data-ttu-id="923b6-176">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-176">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-177">Der reguläre Ausdruck `Regex_croatia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-177">The regular expression  `Regex_croatia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-178">Ein Schlüsselwort aus `Keywords_croatia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-178">A keyword from  `Keywords_croatia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_croatia_eu_passport_number" />
          <Match idRef="Keywords_croatia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-179">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-179">Keywords</span></span>

<span data-ttu-id="923b6-180">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-180"></span></span>
|<span data-ttu-id="923b6-181">**Keywords_croatia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-181">**Keywords_croatia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-182">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-182">passport number</span></span>  <br/> <span data-ttu-id="923b6-183">Kroatisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-183">croatian passport number</span></span>  <br/> <span data-ttu-id="923b6-184">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-184">passport no</span></span>  <br/> <span data-ttu-id="923b6-185">Broj putovnice</span><span class="sxs-lookup"><span data-stu-id="923b6-185">broj putovnice</span></span>  <br/> |
   
## <a name="cyprus"></a><span data-ttu-id="923b6-186">Zypern</span><span class="sxs-lookup"><span data-stu-id="923b6-186">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="923b6-187">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-187">Format</span></span>

<span data-ttu-id="923b6-188">Einen Buchstaben gefolgt von 6 bis 8 Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-188">One letter followed by 6-8 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-189">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-189">Pattern</span></span>

<span data-ttu-id="923b6-190">Ein Zeichen, gefolgt von sechs bis acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-190">One letter followed by six to eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-191">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-191">Checksum</span></span>

<span data-ttu-id="923b6-192">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-192">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-193">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-193">Definition</span></span>

<span data-ttu-id="923b6-194">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-194">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-195">Der reguläre Ausdruck `Regex_cyprus_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-195">The regular expression  `Regex_cyprus_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-196">Ein Schlüsselwort aus `Keywords_cyprus_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-196">A keyword from  `Keywords_cyprus_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_cyprus_eu_passport_number" />
          <Match idRef="Keywords_cyprus_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-197">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-197">Keywords</span></span>

<span data-ttu-id="923b6-198">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-198"></span></span>
|<span data-ttu-id="923b6-199">**Keywords_cyprus_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-199">**Keywords_cyprus_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-200">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-200">passport number</span></span>  <br/> <span data-ttu-id="923b6-201">Zypern Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-201">cyprus passport number</span></span>  <br/> <span data-ttu-id="923b6-202">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-202">passport no</span></span>  <br/> <span data-ttu-id="923b6-203">ΑΡΙΘΜΌ ΔΙΑΒΑΤΗΡΊΟΥ</span><span class="sxs-lookup"><span data-stu-id="923b6-203">αριθμό διαβατηρίου</span></span>  <br/> |
   
## <a name="czech-republic"></a><span data-ttu-id="923b6-204">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="923b6-204">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="923b6-205">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-205">Format</span></span>

<span data-ttu-id="923b6-206">Acht Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-206">Eight digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-207">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-207">Pattern</span></span>

<span data-ttu-id="923b6-208">Acht Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-208">Eight digits without spaces or delimiters</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-209">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-209">Checksum</span></span>

<span data-ttu-id="923b6-210">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-210">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-211">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-211">Definition</span></span>

<span data-ttu-id="923b6-212">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-212">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-213">Der reguläre Ausdruck `Regex_czech_republic_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-213">The regular expression  `Regex_czech_republic_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-214">Ein Schlüsselwort aus `Keywords_czech_republic_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-214">A keyword from  `Keywords_czech_republic_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_passport_number" />
          <Match idRef="Keywords_czech_republic_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-215">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-215">Keywords</span></span>

<span data-ttu-id="923b6-216">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-216"></span></span>
|<span data-ttu-id="923b6-217">**Keywords_czech_republic_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-217">**Keywords_czech_republic_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-218">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-218">passport number</span></span>  <br/> <span data-ttu-id="923b6-219">Tschechische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-219">czech passport number</span></span>  <br/> <span data-ttu-id="923b6-220">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-220">passport no</span></span>  <br/> <span data-ttu-id="923b6-221">Cestovní pas</span><span class="sxs-lookup"><span data-stu-id="923b6-221">cestovní pas</span></span>  <br/> <span data-ttu-id="923b6-222">PAS</span><span class="sxs-lookup"><span data-stu-id="923b6-222">pas</span></span>  <br/> |
   
## <a name="denmark"></a><span data-ttu-id="923b6-223">Dänemark</span><span class="sxs-lookup"><span data-stu-id="923b6-223">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="923b6-224">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-224">Format</span></span>

<span data-ttu-id="923b6-225">Neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-225">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-226">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-226">Pattern</span></span>

 <span data-ttu-id="923b6-227">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-227">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="923b6-228">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-228">Checksum</span></span>

<span data-ttu-id="923b6-229">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-229">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-230">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-230">Definition</span></span>

<span data-ttu-id="923b6-231">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-231">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-232">Der reguläre Ausdruck `Regex_denmark_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-232">The regular expression  `Regex_denmark_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-233">Ein Schlüsselwort aus `Keywords_denmark_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-233">A keyword from  `Keywords_denmark_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_denmark_eu_passport_number" />
          <Match idRef="Keywords_denmark_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-234">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-234">Keywords</span></span>

<span data-ttu-id="923b6-235">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-235"></span></span>
|<span data-ttu-id="923b6-236">**Keywords_denmark_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-236">**Keywords_denmark_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-237">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-237">passport number</span></span>  <br/> <span data-ttu-id="923b6-238">Dänische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-238">danish passport number</span></span>  <br/> <span data-ttu-id="923b6-239">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-239">passport no</span></span>  <br/> <span data-ttu-id="923b6-240">PAS</span><span class="sxs-lookup"><span data-stu-id="923b6-240">pas</span></span>  <br/> <span data-ttu-id="923b6-241">pasnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-241">pasnummer</span></span>  <br/> |
   
## <a name="estonia"></a><span data-ttu-id="923b6-242">Estland</span><span class="sxs-lookup"><span data-stu-id="923b6-242">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="923b6-243">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-243">Format</span></span>

<span data-ttu-id="923b6-244">Einen Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-244">One letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-245">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-245">Pattern</span></span>

<span data-ttu-id="923b6-246">Einen Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-246">One letter followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-247">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-247">Checksum</span></span>

<span data-ttu-id="923b6-248">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-248">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-249">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-249">Definition</span></span>

<span data-ttu-id="923b6-250">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-250">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-251">Der reguläre Ausdruck `Regex_estonia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-251">The regular expression  `Regex_estonia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-252">Ein Schlüsselwort aus `Keywords_estonia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-252">A keyword from  `Keywords_estonia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_estonia_eu_passport_number" />
          <Match idRef="Keywords_estonia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-253">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-253">Keywords</span></span>

<span data-ttu-id="923b6-254">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-254"></span></span>
|<span data-ttu-id="923b6-255">**Keywords_estonia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-255">**Keywords_estonia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-256">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-256">passport number</span></span>  <br/> <span data-ttu-id="923b6-257">Estnisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-257">estonian passport number</span></span>  <br/> <span data-ttu-id="923b6-258">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-258">passport no</span></span>  <br/> <span data-ttu-id="923b6-259">übergeben Sie Eesti kodaniku</span><span class="sxs-lookup"><span data-stu-id="923b6-259">eesti kodaniku pass</span></span>  <br/> |
   
## <a name="finland"></a><span data-ttu-id="923b6-260">Finnland</span><span class="sxs-lookup"><span data-stu-id="923b6-260">Finland</span></span>

<span data-ttu-id="923b6-261">Weitere Informationen hierzu finden Sie im Abschnitt "Finnland Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="923b6-261">For details, see the section "Finland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="france"></a><span data-ttu-id="923b6-262">Frankreich</span><span class="sxs-lookup"><span data-stu-id="923b6-262">France</span></span>

<span data-ttu-id="923b6-263">Weitere Informationen hierzu finden Sie im Abschnitt "Französische Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="923b6-263">For details, see the section "France Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="germany"></a><span data-ttu-id="923b6-264">Deutschland</span><span class="sxs-lookup"><span data-stu-id="923b6-264">Germany</span></span>

<span data-ttu-id="923b6-265">Weitere Informationen hierzu finden Sie im Abschnitt "Deutschland Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="923b6-265">For details, see the section "Germany Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="greece"></a><span data-ttu-id="923b6-266">Griechenland</span><span class="sxs-lookup"><span data-stu-id="923b6-266">Greece</span></span>

### <a name="format"></a><span data-ttu-id="923b6-267">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-267">Format</span></span>

<span data-ttu-id="923b6-268">Zwei Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-268">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-269">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-269">Pattern</span></span>

<span data-ttu-id="923b6-270">Zwei Buchstaben gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-270">Two letters followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-271">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-271">Checksum</span></span>

<span data-ttu-id="923b6-272">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-272">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-273">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-273">Definition</span></span>

<span data-ttu-id="923b6-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-275">Der reguläre Ausdruck `Regex_greece_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-275">The regular expression  `Regex_greece_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-276">Ein Schlüsselwort aus `Keywords_greece_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-276">A keyword from  `Keywords_greece_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_passport_number" />
          <Match idRef="Keywords_greece_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-277">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-277">Keywords</span></span>

<span data-ttu-id="923b6-278">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-278"></span></span>
|<span data-ttu-id="923b6-279">**Keywords_greece_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-279">**Keywords_greece_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-280">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-280">passport number</span></span>  <br/> <span data-ttu-id="923b6-281">Griechische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-281">greek passport number</span></span>  <br/> <span data-ttu-id="923b6-282">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-282">passport no</span></span>  <br/> <span data-ttu-id="923b6-283">ΔΙΑΒΑΤΗΡΙΟ</span><span class="sxs-lookup"><span data-stu-id="923b6-283">διαβατηριο</span></span>  <br/> |
   
## <a name="hungary"></a><span data-ttu-id="923b6-284">Ungarn</span><span class="sxs-lookup"><span data-stu-id="923b6-284">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="923b6-285">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-285">Format</span></span>

<span data-ttu-id="923b6-286">Zwei Buchstaben gefolgt von sechs oder sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-286">Two letters followed by six or seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-287">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-287">Pattern</span></span>

<span data-ttu-id="923b6-288">Zwei Buchstaben gefolgt von sechs oder sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-288">Two letters followed by six or seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-289">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-289">Checksum</span></span>

<span data-ttu-id="923b6-290">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-290">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-291">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-291">Definition</span></span>

<span data-ttu-id="923b6-292">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-292">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-293">Der reguläre Ausdruck `Regex_hungary_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-293">The regular expression  `Regex_hungary_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-294">Ein Schlüsselwort aus `Keywords_hungary_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-294">A keyword from  `Keywords_hungary_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_hungary_eu_passport_number" />
          <Match idRef="Keywords_hungary_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-295">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-295">Keywords</span></span>

<span data-ttu-id="923b6-296">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-296"></span></span>
|<span data-ttu-id="923b6-297">**Keywords_hungary_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-297">**Keywords_hungary_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-298">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-298">passport number</span></span>  <br/> <span data-ttu-id="923b6-299">Ungarisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-299">hungarian passport number</span></span>  <br/> <span data-ttu-id="923b6-300">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-300">passport no</span></span>  <br/> <span data-ttu-id="923b6-301">Útlevél száma</span><span class="sxs-lookup"><span data-stu-id="923b6-301">útlevél száma</span></span>  <br/> |
   
## <a name="ireland"></a><span data-ttu-id="923b6-302">Irland</span><span class="sxs-lookup"><span data-stu-id="923b6-302">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="923b6-303">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-303">Format</span></span>

<span data-ttu-id="923b6-304">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-304">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-305">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-305">Pattern</span></span>

<span data-ttu-id="923b6-306">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="923b6-306">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="923b6-307">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="923b6-307">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="923b6-308">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-308">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="923b6-309">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-309">Checksum</span></span>

<span data-ttu-id="923b6-310">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-310">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-311">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-311">Definition</span></span>

<span data-ttu-id="923b6-312">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-312">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-313">Der reguläre Ausdruck `Regex_ireland_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-313">The regular expression  `Regex_ireland_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-314">Ein Schlüsselwort aus `Keywords_ireland_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-314">A keyword from  `Keywords_ireland_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_ireland_eu_passport_number" />
          <Match idRef="Keywords_ireland_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-315">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-315">Keywords</span></span>

<span data-ttu-id="923b6-316">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-316"></span></span>
|<span data-ttu-id="923b6-317">**Keywords_ireland_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-317">**Keywords_ireland_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-318">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-318">passport number</span></span>  <br/> <span data-ttu-id="923b6-319">Irland Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-319">irish passport number</span></span>  <br/> <span data-ttu-id="923b6-320">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-320">passport no</span></span>  <br/> <span data-ttu-id="923b6-321">PAS</span><span class="sxs-lookup"><span data-stu-id="923b6-321">pas</span></span>  <br/> <span data-ttu-id="923b6-322">passport</span><span class="sxs-lookup"><span data-stu-id="923b6-322">passport</span></span>  <br/> <span data-ttu-id="923b6-323">passeport</span><span class="sxs-lookup"><span data-stu-id="923b6-323">passeport</span></span>  <br/> <span data-ttu-id="923b6-324">Passeport numero</span><span class="sxs-lookup"><span data-stu-id="923b6-324">passeport numero</span></span>  <br/> |
   
## <a name="italy"></a><span data-ttu-id="923b6-325">Italien</span><span class="sxs-lookup"><span data-stu-id="923b6-325">Italy</span></span>

### <a name="format"></a><span data-ttu-id="923b6-326">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-326">Format</span></span>

<span data-ttu-id="923b6-327">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-327">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-328">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-328">Pattern</span></span>

<span data-ttu-id="923b6-329">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="923b6-329">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="923b6-330">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="923b6-330">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="923b6-331">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-331">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="923b6-332">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-332">Checksum</span></span>

<span data-ttu-id="923b6-333">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="923b6-333">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-334">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-334">Definition</span></span>

<span data-ttu-id="923b6-335">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-335">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-336">Der reguläre Ausdruck `Regex_italy_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-336">The regular expression  `Regex_italy_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-337">Ein Schlüsselwort aus `Keywords_italy_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-337">A keyword from  `Keywords_italy_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_italy_eu_passport_number" />
          <Match idRef="Keywords_italy_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-338">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-338">Keywords</span></span>

<span data-ttu-id="923b6-339">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-339"></span></span>
|<span data-ttu-id="923b6-340">**Keywords_italy_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-340">**Keywords_italy_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-341">Italienische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-341">italian passport number</span></span>  <br/> <span data-ttu-id="923b6-342">Repubblica Italiana passaporto</span><span class="sxs-lookup"><span data-stu-id="923b6-342">repubblica italiana passaporto</span></span>  <br/> <span data-ttu-id="923b6-343">passaporto</span><span class="sxs-lookup"><span data-stu-id="923b6-343">passaporto</span></span>  <br/> <span data-ttu-id="923b6-344">Passaporto italiana</span><span class="sxs-lookup"><span data-stu-id="923b6-344">passaporto italiana</span></span>  <br/> <span data-ttu-id="923b6-345">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-345">passport number</span></span>  <br/> <span data-ttu-id="923b6-346">Italiana Passaporto numero</span><span class="sxs-lookup"><span data-stu-id="923b6-346">italiana passaporto numero</span></span>  <br/> <span data-ttu-id="923b6-347">Passaporto numero</span><span class="sxs-lookup"><span data-stu-id="923b6-347">passaporto numero</span></span>  <br/> <span data-ttu-id="923b6-348">Numéro Passeport italien</span><span class="sxs-lookup"><span data-stu-id="923b6-348">numéro passeport italien</span></span>  <br/> <span data-ttu-id="923b6-349">Numéro passeport</span><span class="sxs-lookup"><span data-stu-id="923b6-349">numéro passeport</span></span>  <br/> |
   
## <a name="latvia"></a><span data-ttu-id="923b6-350">Lettland</span><span class="sxs-lookup"><span data-stu-id="923b6-350">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="923b6-351">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-351">Format</span></span>

<span data-ttu-id="923b6-352">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-352">Two letters or digits followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-353">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-353">Pattern</span></span>

<span data-ttu-id="923b6-354">Zwei Buchstaben oder Ziffern, gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="923b6-354">Two letters or digits followed by seven digits:</span></span>
  
- <span data-ttu-id="923b6-355">Zwei Ziffern oder Buchstaben (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="923b6-355">Two digits or letters (not case sensitive)</span></span>
    
- <span data-ttu-id="923b6-356">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-356">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="923b6-357">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-357">Checksum</span></span>

<span data-ttu-id="923b6-358">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-358">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-359">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-359">Definition</span></span>

<span data-ttu-id="923b6-360">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-360">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-361">Der reguläre Ausdruck `Regex_latvia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-361">The regular expression  `Regex_latvia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-362">Ein Schlüsselwort aus `Keywords_latvia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-362">A keyword from  `Keywords_latvia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_latvia_eu_passport_number" />
          <Match idRef="Keywords_latvia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-363">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-363">Keywords</span></span>

<span data-ttu-id="923b6-364">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-364"></span></span>
|<span data-ttu-id="923b6-365">**Keywords_latvia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-365">**Keywords_latvia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-366">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-366">passport number</span></span>  <br/> <span data-ttu-id="923b6-367">Lettisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-367">latvian passport number</span></span>  <br/> <span data-ttu-id="923b6-368">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-368">passport no</span></span>  <br/> <span data-ttu-id="923b6-369">Pase numurs</span><span class="sxs-lookup"><span data-stu-id="923b6-369">pase numurs</span></span>  <br/> |
   
## <a name="lithuania"></a><span data-ttu-id="923b6-370">Litauen</span><span class="sxs-lookup"><span data-stu-id="923b6-370">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="923b6-371">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-371">Format</span></span>

<span data-ttu-id="923b6-372">Acht Ziffern oder Buchstaben ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-372">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-373">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-373">Pattern</span></span>

<span data-ttu-id="923b6-374">Acht Ziffern oder Buchstaben (ohne Beachtung von Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="923b6-374">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-375">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-375">Checksum</span></span>

<span data-ttu-id="923b6-376">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="923b6-376">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-377">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-377">Definition</span></span>

<span data-ttu-id="923b6-378">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-378">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-379">Der reguläre Ausdruck `Regex_lithuania_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-379">The regular expression  `Regex_lithuania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-380">Ein Schlüsselwort aus `Keywords_lithuania_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-380">A keyword from  `Keywords_lithuania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_lithuania_eu_passport_number" />
          <Match idRef="Keywords_lithuania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-381">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-381">Keywords</span></span>

<span data-ttu-id="923b6-382">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-382"></span></span>
|<span data-ttu-id="923b6-383">**Keywords_lithuania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-383">**Keywords_lithuania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-384">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-384">passport number</span></span>  <br/> <span data-ttu-id="923b6-385">Lithunian Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-385">lithunian passport number</span></span>  <br/> <span data-ttu-id="923b6-386">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-386">passport no</span></span>  <br/> <span data-ttu-id="923b6-387">Paso numeris</span><span class="sxs-lookup"><span data-stu-id="923b6-387">paso numeris</span></span>  <br/> |
   
## <a name="luxemburg"></a><span data-ttu-id="923b6-388">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="923b6-388">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="923b6-389">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-389">Format</span></span>

<span data-ttu-id="923b6-390">Acht Ziffern oder Buchstaben ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-390">Eight digits or letters with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-391">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-391">Pattern</span></span>

<span data-ttu-id="923b6-392">Acht Ziffern oder Buchstaben (ohne Beachtung von Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="923b6-392">Eight digits or letters (not case sensitive)</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-393">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-393">Checksum</span></span>

<span data-ttu-id="923b6-394">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-394">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-395">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-395">Definition</span></span>

<span data-ttu-id="923b6-396">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-396">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-397">Der reguläre Ausdruck `Regex_nation_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-397">The regular expression  `Regex_nation_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-398">Ein Schlüsselwort aus `Keywords_nation_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-398">A keyword from  `Keywords_nation_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_nation_eu_passport_number" />
          <Match idRef="Keywords_nation_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-399">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-399">Keywords</span></span>

<span data-ttu-id="923b6-400">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-400"></span></span>
|<span data-ttu-id="923b6-401">**Keywords_nation_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-401">**Keywords_nation_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-402">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-402">passport number</span></span>  <br/> <span data-ttu-id="923b6-403">Lettisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-403">latvian passport number</span></span>  <br/> <span data-ttu-id="923b6-404">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-404">passport no</span></span>  <br/> <span data-ttu-id="923b6-405">Passnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-405">passnummer</span></span>  <br/> |
   
## <a name="malta"></a><span data-ttu-id="923b6-406">Malta</span><span class="sxs-lookup"><span data-stu-id="923b6-406">Malta</span></span>

### <a name="format"></a><span data-ttu-id="923b6-407">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-407">Format</span></span>

<span data-ttu-id="923b6-408">Sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-408">Seven digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-409">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-409">Pattern</span></span>

 <span data-ttu-id="923b6-410">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-410">Seven digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="923b6-411">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-411">Checksum</span></span>

<span data-ttu-id="923b6-412">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-412">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-413">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-413">Definition</span></span>

<span data-ttu-id="923b6-414">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-414">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-415">Der reguläre Ausdruck `Regex_malta_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-415">The regular expression  `Regex_malta_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-416">Ein Schlüsselwort aus `Keywords_malta_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-416">A keyword from  `Keywords_malta_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_malta_eu_passport_number" />
          <Match idRef="Keywords_malta_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-417">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-417">Keywords</span></span>

<span data-ttu-id="923b6-418">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-418"></span></span>
|<span data-ttu-id="923b6-419">**Keywords_malta_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-419">**Keywords_malta_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-420">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-420">passport number</span></span>  <br/> <span data-ttu-id="923b6-421">Maltesisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-421">maltese passport number</span></span>  <br/> <span data-ttu-id="923b6-422">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-422">passport no</span></span>  <br/> <span data-ttu-id="923b6-423">Numru Tal-passaport</span><span class="sxs-lookup"><span data-stu-id="923b6-423">numru tal-passaport</span></span>  <br/> |
   
## <a name="netherlands"></a><span data-ttu-id="923b6-424">Niederlande</span><span class="sxs-lookup"><span data-stu-id="923b6-424">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="923b6-425">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-425">Format</span></span>

<span data-ttu-id="923b6-426">Neun Buchstaben oder Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-426">Nine letters or digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-427">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-427">Pattern</span></span>

<span data-ttu-id="923b6-428">Neun Buchstaben oder Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-428">Nine letters or digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-429">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-429">Checksum</span></span>

<span data-ttu-id="923b6-430">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="923b6-430">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-431">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-431">Definition</span></span>

<span data-ttu-id="923b6-432">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-432">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-433">Der reguläre Ausdruck `Regex_netherlands_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-433">The regular expression  `Regex_netherlands_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-434">Ein Schlüsselwort aus `Keywords_netherlands_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-434">A keyword from  `Keywords_netherlands_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_netherlands_eu_passport_number" />
          <Match idRef="Keywords_netherlands_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-435">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-435">Keywords</span></span>

<span data-ttu-id="923b6-436">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-436"></span></span>
|<span data-ttu-id="923b6-437">**Keywords_netherlands_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-437">**Keywords_netherlands_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-438">Niederländische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-438">dutch passport number</span></span>  <br/> <span data-ttu-id="923b6-439">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-439">passport number</span></span>  <br/> <span data-ttu-id="923b6-440">Niederlande Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-440">netherlands passport number</span></span>  <br/> <span data-ttu-id="923b6-441">Nederlanden Paspoort nummer</span><span class="sxs-lookup"><span data-stu-id="923b6-441">nederlanden paspoort nummer</span></span>  <br/> <span data-ttu-id="923b6-442">paspoort</span><span class="sxs-lookup"><span data-stu-id="923b6-442">paspoort</span></span>  <br/> <span data-ttu-id="923b6-443">Nederlanden paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-443">nederlanden paspoortnummer</span></span>  <br/> <span data-ttu-id="923b6-444">paspoortnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-444">paspoortnummer</span></span>  <br/> |
   
## <a name="poland"></a><span data-ttu-id="923b6-445">Polen</span><span class="sxs-lookup"><span data-stu-id="923b6-445">Poland</span></span>

<span data-ttu-id="923b6-446">Weitere Informationen hierzu finden Sie im Abschnitt "Polen Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="923b6-446">For details, see the section "Poland Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="portugal"></a><span data-ttu-id="923b6-447">Portugal</span><span class="sxs-lookup"><span data-stu-id="923b6-447">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="923b6-448">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-448">Format</span></span>

<span data-ttu-id="923b6-449">Ein Zeichen, gefolgt von sechs Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-449">One letter followed by six digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-450">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-450">Pattern</span></span>

<span data-ttu-id="923b6-451">Einen Buchstaben gefolgt von sechs Ziffern:</span><span class="sxs-lookup"><span data-stu-id="923b6-451">One letter followed by six digits:</span></span>
  
- <span data-ttu-id="923b6-452">Ein Buchstabe (ohne Beachtung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="923b6-452">One letter (not case sensitive)</span></span>
    
- <span data-ttu-id="923b6-453">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-453">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="923b6-454">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-454">Checksum</span></span>

<span data-ttu-id="923b6-455">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-455">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-456">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-456">Definition</span></span>

<span data-ttu-id="923b6-457">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-457">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-458">Der reguläre Ausdruck `Regex_portugal_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-458">The regular expression  `Regex_portugal_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-459">Ein Schlüsselwort aus `Keywords_portugal_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-459">A keyword from  `Keywords_portugal_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_portugal_eu_passport_number" />
          <Match idRef="Keywords_portugal_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-460">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-460">Keywords</span></span>

<span data-ttu-id="923b6-461">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-461"></span></span>
|<span data-ttu-id="923b6-462">**Keywords_portugal_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-462">**Keywords_portugal_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-463">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-463">passport number</span></span>  <br/> <span data-ttu-id="923b6-464">Portugiesische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-464">portugese passport number</span></span>  <br/> <span data-ttu-id="923b6-465">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-465">passport no</span></span>  <br/> <span data-ttu-id="923b6-466">Número passaporte</span><span class="sxs-lookup"><span data-stu-id="923b6-466">número do passaporte</span></span>  <br/> |
   
## <a name="romania"></a><span data-ttu-id="923b6-467">Rumänien</span><span class="sxs-lookup"><span data-stu-id="923b6-467">Romania</span></span>

### <a name="format"></a><span data-ttu-id="923b6-468">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-468">Format</span></span>

<span data-ttu-id="923b6-469">Acht oder neun Ziffern ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-469">Eight or nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-470">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-470">Pattern</span></span>

<span data-ttu-id="923b6-471">Acht oder neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-471">Eight or nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-472">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-472">Checksum</span></span>

<span data-ttu-id="923b6-473">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-473">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-474">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-474">Definition</span></span>

<span data-ttu-id="923b6-475">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-475">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-476">Der reguläre Ausdruck `Regex_romania_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-476">The regular expression  `Regex_romania_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-477">Ein Schlüsselwort aus `Keywords_romania_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-477">A keyword from  `Keywords_romania_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_passport_number" />
          <Match idRef="Keywords_romania_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-478">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-478">Keywords</span></span>

<span data-ttu-id="923b6-479">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-479"></span></span>
|<span data-ttu-id="923b6-480">**Keywords_romania_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-480">**Keywords_romania_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-481">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-481">passport number</span></span>  <br/> <span data-ttu-id="923b6-482">Rumänisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-482">romanian passport number</span></span>  <br/> <span data-ttu-id="923b6-483">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-483">passport no</span></span>  <br/> <span data-ttu-id="923b6-484">Numărul pașaportului</span><span class="sxs-lookup"><span data-stu-id="923b6-484">numărul pașaportului</span></span>  <br/> |
   
## <a name="slovakia"></a><span data-ttu-id="923b6-485">Slowakei</span><span class="sxs-lookup"><span data-stu-id="923b6-485">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="923b6-486">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-486">Format</span></span>

<span data-ttu-id="923b6-487">Eine Ziffern oder Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-487">One digit or letter followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-488">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-488">Pattern</span></span>

<span data-ttu-id="923b6-489">Eine Ziffern oder Buchstaben (ohne Beachtung von Groß-/Kleinschreibung) gefolgt von sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-489">One digit or letter (not case sensitive) followed by seven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="923b6-490">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-490">Checksum</span></span>

<span data-ttu-id="923b6-491">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-491">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-492">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-492">Definition</span></span>

<span data-ttu-id="923b6-493">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-493">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-494">Der reguläre Ausdruck `Regex_slovakia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-494">The regular expression  `Regex_slovakia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-495">Ein Schlüsselwort aus `Keywords_slovakia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-495">A keyword from  `Keywords_slovakia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_passport_number" />
          <Match idRef="Keywords_slovakia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-496">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-496">Keywords</span></span>

<span data-ttu-id="923b6-497">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-497"></span></span>
|<span data-ttu-id="923b6-498">**Keywords_slovakia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-498">**Keywords_slovakia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-499">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-499">passport number</span></span>  <br/> <span data-ttu-id="923b6-500">Slowakische Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-500">slovakian passport number</span></span>  <br/> <span data-ttu-id="923b6-501">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-501">passport no</span></span>  <br/> <span data-ttu-id="923b6-502">Číslo pasu</span><span class="sxs-lookup"><span data-stu-id="923b6-502">číslo pasu</span></span>  <br/> |
   
## <a name="slovenia"></a><span data-ttu-id="923b6-503">Slowenien</span><span class="sxs-lookup"><span data-stu-id="923b6-503">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="923b6-504">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-504">Format</span></span>

<span data-ttu-id="923b6-505">Zwei Buchstaben gefolgt von sieben Ziffern ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-505">Two letters followed by seven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-506">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-506">Pattern</span></span>

<span data-ttu-id="923b6-507">Zwei Buchstaben gefolgt von sieben Ziffern:</span><span class="sxs-lookup"><span data-stu-id="923b6-507">Two letters followed by seven digits:</span></span>
  
- <span data-ttu-id="923b6-508">Der Buchstabe "P"</span><span class="sxs-lookup"><span data-stu-id="923b6-508">The letter "P"</span></span>
    
- <span data-ttu-id="923b6-509">Einen Großbuchstaben</span><span class="sxs-lookup"><span data-stu-id="923b6-509">One uppercase letter</span></span>
    
- <span data-ttu-id="923b6-510">Sieben Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-510">Seven digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="923b6-511">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-511">Checksum</span></span>

<span data-ttu-id="923b6-512">Nein</span><span class="sxs-lookup"><span data-stu-id="923b6-512">No</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-513">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-513">Definition</span></span>

<span data-ttu-id="923b6-514">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-514">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-515">Der reguläre Ausdruck `Regex_slovenia_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-515">The regular expression  `Regex_slovenia_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-516">Ein Schlüsselwort aus `Keywords_slovenia_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-516">A keyword from  `Keywords_slovenia_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovenia_eu_passport_number" />
          <Match idRef="Keywords_slovenia_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-517">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-517">Keywords</span></span>

<span data-ttu-id="923b6-518">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-518"></span></span>
|<span data-ttu-id="923b6-519">**Keywords_slovenia_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-519">**Keywords_slovenia_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-520">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-520">passport number</span></span>  <br/> <span data-ttu-id="923b6-521">Slowenisch Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-521">slovenian passport number</span></span>  <br/> <span data-ttu-id="923b6-522">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-522">passport no</span></span>  <br/> <span data-ttu-id="923b6-523">Številka Potnega lista</span><span class="sxs-lookup"><span data-stu-id="923b6-523">številka potnega lista</span></span>  <br/> |
   
## <a name="spain"></a><span data-ttu-id="923b6-524">Spanien</span><span class="sxs-lookup"><span data-stu-id="923b6-524">Spain</span></span>

### <a name="format"></a><span data-ttu-id="923b6-525">Format</span><span class="sxs-lookup"><span data-stu-id="923b6-525">Format</span></span>

<span data-ttu-id="923b6-526">Eine acht oder neun Zeichen Kombination von Buchstaben und Zahlen ohne Leerzeichen oder Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="923b6-526">An eight- or nine-character combination of letters and numbers with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="923b6-527">Muster</span><span class="sxs-lookup"><span data-stu-id="923b6-527">Pattern</span></span>

<span data-ttu-id="923b6-528">Eine Kombination der acht oder neun Zeichen Buchstaben und Zahlen:</span><span class="sxs-lookup"><span data-stu-id="923b6-528">An eight- or nine-character combination of letters and numbers:</span></span>
  
-  <span data-ttu-id="923b6-529">Zwei Ziffern oder Buchstaben</span><span class="sxs-lookup"><span data-stu-id="923b6-529">Two digits or letters</span></span> 
    
- <span data-ttu-id="923b6-530">Eine Ziffern oder Buchstaben (optional)</span><span class="sxs-lookup"><span data-stu-id="923b6-530">One digit or letter (optional)</span></span>
    
- <span data-ttu-id="923b6-531">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="923b6-531">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="923b6-532">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="923b6-532">Checksum</span></span>

<span data-ttu-id="923b6-533">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="923b6-533">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="923b6-534">Definition</span><span class="sxs-lookup"><span data-stu-id="923b6-534">Definition</span></span>

<span data-ttu-id="923b6-535">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="923b6-535">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="923b6-536">Der reguläre Ausdruck `Regex_spain_eu_passport_number` sucht nach Inhalten, die dem Muster entspricht.</span><span class="sxs-lookup"><span data-stu-id="923b6-536">The regular expression  `Regex_spain_eu_passport_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="923b6-537">Ein Schlüsselwort aus `Keywords_spain_eu_passport_number` gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="923b6-537">A keyword from  `Keywords_spain_eu_passport_number` is found.</span></span> 
    
```
 <!-- EU Passport Number -->
<Entity id="21883626-6245-4f3d-9b61-5cbb43e625ee" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_spain_eu_passport_number" />
          <Match idRef="Keywords_spain_eu_passport_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="923b6-538">Keywords</span><span class="sxs-lookup"><span data-stu-id="923b6-538">Keywords</span></span>

<span data-ttu-id="923b6-539">| |</span><span class="sxs-lookup"><span data-stu-id="923b6-539"></span></span>
|<span data-ttu-id="923b6-540">**Keywords_spain_eu_passport_number**</span><span class="sxs-lookup"><span data-stu-id="923b6-540">**Keywords_spain_eu_passport_number**</span></span>|
|:-----|
|<span data-ttu-id="923b6-541">passport</span><span class="sxs-lookup"><span data-stu-id="923b6-541">passport</span></span>  <br/> <span data-ttu-id="923b6-542">Spanien passport</span><span class="sxs-lookup"><span data-stu-id="923b6-542">spain passport</span></span>  <br/> <span data-ttu-id="923b6-543">Passport-Adressbuch</span><span class="sxs-lookup"><span data-stu-id="923b6-543">passport book</span></span>  <br/> <span data-ttu-id="923b6-544">Reisepassnummer</span><span class="sxs-lookup"><span data-stu-id="923b6-544">passport number</span></span>  <br/> <span data-ttu-id="923b6-545">Passport keine</span><span class="sxs-lookup"><span data-stu-id="923b6-545">passport no</span></span>  <br/> <span data-ttu-id="923b6-546">Libreta pasaporte</span><span class="sxs-lookup"><span data-stu-id="923b6-546">libreta pasaporte</span></span>  <br/> <span data-ttu-id="923b6-547">Número pasaporte</span><span class="sxs-lookup"><span data-stu-id="923b6-547">número pasaporte</span></span>  <br/> <span data-ttu-id="923b6-548">España pasaporte</span><span class="sxs-lookup"><span data-stu-id="923b6-548">españa pasaporte</span></span>  <br/> <span data-ttu-id="923b6-549">pasaporte</span><span class="sxs-lookup"><span data-stu-id="923b6-549">pasaporte</span></span>  <br/> |
   
## <a name="sweden"></a><span data-ttu-id="923b6-550">Schweden</span><span class="sxs-lookup"><span data-stu-id="923b6-550">Sweden</span></span>

<span data-ttu-id="923b6-551">Weitere Informationen hierzu finden Sie im Abschnitt "Schwedische Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="923b6-551">For details, see the section "Sweden Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="uk"></a><span data-ttu-id="923b6-552">GROßBRITANNIEN</span><span class="sxs-lookup"><span data-stu-id="923b6-552">UK</span></span>

<span data-ttu-id="923b6-p103">Weitere Informationen hierzu finden Sie im Abschnitt "US / Großbritannien Reisepassnummer" in [welche Arten der vertraulichen Informationen gesucht](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="923b6-p103">For details, see the section "U.S. / U.K. Passport Number" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="923b6-555">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="923b6-555">See also</span></span>

[<span data-ttu-id="923b6-556">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="923b6-556">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

