---
title: USt-ID-Nummer
ms.author: stephow
author: stephow-MSFT
manager: laurawi
ms.date: 8/17/2018
ms.audience: Admin
ms.topic: reference
ms.service: O365-seccomp
ms.collection: M365-security-compliance
localization_priority: Normal
description: In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie sucht, wenn Sie den vertraulichen Informationstyp der EU-Steuernummer erkennt. Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.
ms.openlocfilehash: 4914ff078695519c2a298190d82c86a6abebceb9
ms.sourcegitcommit: 0017dc6a5f81c165d9dfd88be39a6bb17856582e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32255523"
---
# <a name="eu-tax-identification-number"></a><span data-ttu-id="0ef00-104">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-104">EU Tax Identification Number</span></span>

<span data-ttu-id="0ef00-105">In diesem Thema wird gezeigt, was eine Data Loss Prevention (DLP)-Richtlinie bei der Erkennung des vertraulichen Informationstyps "TIN" (EU Tax Identification Number) sucht.</span><span class="sxs-lookup"><span data-stu-id="0ef00-105">This topic shows what a data loss prevention (DLP) policy looks for when it detects the EU Tax Identification Number (TIN) sensitive information type.</span></span> <span data-ttu-id="0ef00-106">Dieser vertrauliche Informationstyp definiert verschiedene Muster, Schlüsselwörter und andere Nachweise für jedes Land.</span><span class="sxs-lookup"><span data-stu-id="0ef00-106">This sensitive information type defines different patterns, keywords, and other evidence for each country.</span></span>
  
## <a name="austria"></a><span data-ttu-id="0ef00-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="0ef00-107">Austria</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-108">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-108">Format</span></span>

<span data-ttu-id="0ef00-109">Neun Ziffern mit optionalem Bindestrich und Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="0ef00-109">Nine digits with optional hyphen and forward slash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-110">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-110">Pattern</span></span>

<span data-ttu-id="0ef00-111">Neun Ziffern mit optionalem Bindestrich und Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="0ef00-111">Nine digits with optional hyphen and forward slash:</span></span>
  
-  <span data-ttu-id="0ef00-112">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-112">Two digits</span></span> 
    
- <span data-ttu-id="0ef00-113">Ein Bindestrich (optional)</span><span class="sxs-lookup"><span data-stu-id="0ef00-113">A hyphen (optional)</span></span>
    
- <span data-ttu-id="0ef00-114">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-114">Three digits</span></span>
    
- <span data-ttu-id="0ef00-115">Ein Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="0ef00-115">A forward slash (optional)</span></span>
    
- <span data-ttu-id="0ef00-116">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-116">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-117">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-117">Checksum</span></span>

<span data-ttu-id="0ef00-118">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-118">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-119">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-119">Definition</span></span>

<span data-ttu-id="0ef00-120">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-120">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-121">Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-121">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-122">Ein Schlüsselwort `Keywords_austria_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-122">A keyword from  `Keywords_austria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-123">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-123">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-124">Die Funktion `Func_austria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-124">The function  `Func_austria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
          <Match idRef="Keywords_austria_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_austria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-125">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-125">Keywords</span></span>

#### <a name="keywordsaustriaeutaxfilenumber"></a><span data-ttu-id="0ef00-126">Keywords_austria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-126">Keywords_austria_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-127">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-127">tax number</span></span>
  
<span data-ttu-id="0ef00-128">number</span><span class="sxs-lookup"><span data-stu-id="0ef00-128">number</span></span>
  
<span data-ttu-id="0ef00-129">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-129">tax registration number</span></span>
  
<span data-ttu-id="0ef00-130">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-130">tax id</span></span>
  
<span data-ttu-id="0ef00-131">St.Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-131">st.nr.</span></span>
  
<span data-ttu-id="0ef00-132">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-132">steuernummer</span></span>
  
## <a name="belgium"></a><span data-ttu-id="0ef00-133">Belgien</span><span class="sxs-lookup"><span data-stu-id="0ef00-133">Belgium</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-134">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-134">Format</span></span>

<span data-ttu-id="0ef00-135">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-135">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-136">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-136">Pattern</span></span>

<span data-ttu-id="0ef00-137">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0ef00-137">11 digits:</span></span>
  
- <span data-ttu-id="0ef00-138">Zwei Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-138">Two digits</span></span>
    
- <span data-ttu-id="0ef00-139">"0" oder "1"</span><span class="sxs-lookup"><span data-stu-id="0ef00-139">A "0" or "1"</span></span>
    
- <span data-ttu-id="0ef00-140">Eine Ziffer</span><span class="sxs-lookup"><span data-stu-id="0ef00-140">One digit</span></span>
    
- <span data-ttu-id="0ef00-141">"0" oder "1" oder "2" oder "3"</span><span class="sxs-lookup"><span data-stu-id="0ef00-141">A "0" or "1" or "2" or "3"</span></span> 
    
- <span data-ttu-id="0ef00-142">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-142">Six digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-143">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-143">Checksum</span></span>

<span data-ttu-id="0ef00-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-144">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-145">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-145">Definition</span></span>

<span data-ttu-id="0ef00-146">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-146">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-147">Der reguläre Ausdruck `Regex_belgium_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-147">The regular expression  `Regex_belgium_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-148">Ein Schlüsselwort `Keywords_belgium_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-148">A keyword from  `Keywords_belgium_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_belgium_eu_tax_file_number" />
          <Match idRef="Keywords_belgium_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-149">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-149">Keywords</span></span>

#### <a name="keywordsbelgiumeutaxfilenumber"></a><span data-ttu-id="0ef00-150">Keywords_belgium_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-150">Keywords_belgium_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-151">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-151">tax number</span></span>
  
<span data-ttu-id="0ef00-152">nationale Registrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-152">national registration number</span></span>
  
<span data-ttu-id="0ef00-153">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-153">tax registration number</span></span>
  
<span data-ttu-id="0ef00-154">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-154">tax id</span></span>
  
<span data-ttu-id="0ef00-155">NIF</span><span class="sxs-lookup"><span data-stu-id="0ef00-155">nif</span></span>
  
<span data-ttu-id="0ef00-156">NIF</span><span class="sxs-lookup"><span data-stu-id="0ef00-156">nif#</span></span>
  
<span data-ttu-id="0ef00-157">Numéro de Registre National</span><span class="sxs-lookup"><span data-stu-id="0ef00-157">numéro de registre national</span></span>
  
<span data-ttu-id="0ef00-158">Numéro d'identification Fiscale</span><span class="sxs-lookup"><span data-stu-id="0ef00-158">numéro d'identification fiscale</span></span>
  
## <a name="bulgaria"></a><span data-ttu-id="0ef00-159">Bulgarien</span><span class="sxs-lookup"><span data-stu-id="0ef00-159">Bulgaria</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-160">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-160">Format</span></span>

<span data-ttu-id="0ef00-161">Zehn Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-161">Ten digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-162">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-162">Pattern</span></span>

<span data-ttu-id="0ef00-163">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-163">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-164">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-164">Checksum</span></span>

<span data-ttu-id="0ef00-165">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-165">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-166">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-166">Definition</span></span>

<span data-ttu-id="0ef00-167">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-167">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-168">Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-168">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-169">Ein Schlüsselwort `Keywords_bulgaria_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-169">A keyword from  `Keywords_bulgaria_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-170">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-170">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-171">Die Funktion `Func_bulgaria_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-171">The function  `Func_bulgaria_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
          <Match idRef="Keywords_bulgaria_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_bulgaria_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-172">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-172">Keywords</span></span>

#### <a name="keywordsbulgariaeutaxfilenumber"></a><span data-ttu-id="0ef00-173">Keywords_bulgaria_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-173">Keywords_bulgaria_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-174">BUCN</span><span class="sxs-lookup"><span data-stu-id="0ef00-174">bucn</span></span>
  
<span data-ttu-id="0ef00-175">einheitliche Zivil Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-175">uniform civil number</span></span>
  
<span data-ttu-id="0ef00-176">BUCN</span><span class="sxs-lookup"><span data-stu-id="0ef00-176">bucn#</span></span>
  
<span data-ttu-id="0ef00-177">uniformcivilnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-177">uniformcivilnumber#</span></span>
  
<span data-ttu-id="0ef00-178">einheitliche Civil ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-178">uniform civil id</span></span>
  
<span data-ttu-id="0ef00-179">einheitliches ziviles Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-179">uniform civil no</span></span>
  
<span data-ttu-id="0ef00-180">EGN</span><span class="sxs-lookup"><span data-stu-id="0ef00-180">egn</span></span>
  
<span data-ttu-id="0ef00-181">Bulgarische einheitliche Zivil Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-181">bulgarian uniform civil number</span></span>
  
<span data-ttu-id="0ef00-182">uniformcivilno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-182">uniformcivilno#</span></span>
  
<span data-ttu-id="0ef00-183">EGN</span><span class="sxs-lookup"><span data-stu-id="0ef00-183">egn#</span></span>
  
<span data-ttu-id="0ef00-184">униформ граждански номер</span><span class="sxs-lookup"><span data-stu-id="0ef00-184">униформ граждански номер</span></span>
  
<span data-ttu-id="0ef00-185">униформ-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-185">униформ id</span></span>
  
<span data-ttu-id="0ef00-186">униформ-граждански-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-186">униформ граждански id</span></span>
  
<span data-ttu-id="0ef00-187">униформ граждански не</span><span class="sxs-lookup"><span data-stu-id="0ef00-187">униформ граждански не</span></span>
  
## <a name="croatia"></a><span data-ttu-id="0ef00-188">Kroatien</span><span class="sxs-lookup"><span data-stu-id="0ef00-188">Croatia</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-189">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-189">Format</span></span>

<span data-ttu-id="0ef00-190">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-190">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-191">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-191">Pattern</span></span>

<span data-ttu-id="0ef00-192">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0ef00-192">11 digits:</span></span>
  
- <span data-ttu-id="0ef00-193">Zehn Ziffern, zufällig gewählt</span><span class="sxs-lookup"><span data-stu-id="0ef00-193">Ten digits, randomly chosen</span></span>
    
- <span data-ttu-id="0ef00-194">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0ef00-194">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-195">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-195">Checksum</span></span>

<span data-ttu-id="0ef00-196">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-196">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-197">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-197">Definition</span></span>

<span data-ttu-id="0ef00-198">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-198">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-199">Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-199">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-200">Ein Schlüsselwort `Keywords_croatia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-200">A keyword from  `Keywords_croatia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-201">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-201">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-202">Die Funktion `Func_croatia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-202">The function  `Func_croatia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
          <Match idRef="Keywords_croatia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_croatia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-203">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-203">Keywords</span></span>

#### <a name="keywordscroatiaeutaxfilenumber"></a><span data-ttu-id="0ef00-204">Keywords_croatia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-204">Keywords_croatia_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-205">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-205">tax number</span></span>
  
<span data-ttu-id="0ef00-206">Steuer</span><span class="sxs-lookup"><span data-stu-id="0ef00-206">tax</span></span>
  
<span data-ttu-id="0ef00-207">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-207">tax id</span></span>
  
<span data-ttu-id="0ef00-208">oid</span><span class="sxs-lookup"><span data-stu-id="0ef00-208">oid</span></span>
  
<span data-ttu-id="0ef00-209">OID</span><span class="sxs-lookup"><span data-stu-id="0ef00-209">oid#</span></span>
  
<span data-ttu-id="0ef00-210">porezni Broj</span><span class="sxs-lookup"><span data-stu-id="0ef00-210">porezni broj</span></span>
  
## <a name="cyprus"></a><span data-ttu-id="0ef00-211">Zypern</span><span class="sxs-lookup"><span data-stu-id="0ef00-211">Cyprus</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-212">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-212">Format</span></span>

<span data-ttu-id="0ef00-213">Acht Ziffern und ein Buchstabe im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-213">Eight digits and one letter in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-214">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-214">Pattern</span></span>

<span data-ttu-id="0ef00-215">Acht Ziffern und ein Buchstabe:</span><span class="sxs-lookup"><span data-stu-id="0ef00-215">Eight digits and one letter:</span></span>
  
-  <span data-ttu-id="0ef00-216">Ein "0"</span><span class="sxs-lookup"><span data-stu-id="0ef00-216">A "0"</span></span> 
    
- <span data-ttu-id="0ef00-217">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0ef00-217">Seven digits</span></span>
    
- <span data-ttu-id="0ef00-218">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0ef00-218">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-219">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-219">Checksum</span></span>

<span data-ttu-id="0ef00-220">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-220">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-221">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-221">Definition</span></span>

<span data-ttu-id="0ef00-222">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-222">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-223">Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-223">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-224">Ein Schlüsselwort `Keywords_cyprus_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-224">A keyword from  `Keywords_cyprus_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-225">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-225">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-226">Die Funktion `Func_cyprus_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-226">The function  `Func_cyprus_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
          <Match idRef="Keywords_cyprus_eu_tax_file_number" />
        </Pattern>
Pattern confidenceLevel="75">
          <IdMatch idRef="Func_cyprus_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-227">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-227">Keywords</span></span>

#### <a name="keywordscypruseutaxfilenumber"></a><span data-ttu-id="0ef00-228">Keywords_cyprus_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-228">Keywords_cyprus_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-229">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-229">tax number</span></span>
  
<span data-ttu-id="0ef00-230">Steuer</span><span class="sxs-lookup"><span data-stu-id="0ef00-230">tax</span></span>
  
<span data-ttu-id="0ef00-231">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-231">tax id</span></span>
  
<span data-ttu-id="0ef00-232">USt-ID-Code</span><span class="sxs-lookup"><span data-stu-id="0ef00-232">tax identification code</span></span>
  
<span data-ttu-id="0ef00-233">TIC</span><span class="sxs-lookup"><span data-stu-id="0ef00-233">tic</span></span>
  
<span data-ttu-id="0ef00-234">TIC</span><span class="sxs-lookup"><span data-stu-id="0ef00-234">tic#</span></span>
  
<span data-ttu-id="0ef00-235">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0ef00-235">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="0ef00-236">φορολογική ταυτότητα</span><span class="sxs-lookup"><span data-stu-id="0ef00-236">φορολογική ταυτότητα</span></span>
  
<span data-ttu-id="0ef00-237">κωδικός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0ef00-237">κωδικός φορολογικού μητρώου</span></span>
  
## <a name="czech-republic"></a><span data-ttu-id="0ef00-238">Tschechien</span><span class="sxs-lookup"><span data-stu-id="0ef00-238">Czech Republic</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-239">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-239">Format</span></span>

<span data-ttu-id="0ef00-240">Neun oder zehn Ziffern mit optionalem Backslash</span><span class="sxs-lookup"><span data-stu-id="0ef00-240">Nine or ten digits with an optional backslash</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-241">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-241">Pattern</span></span>

<span data-ttu-id="0ef00-242">Neun oder zehn Ziffern mit einem optionalen umgekehrten Schrägstrich:</span><span class="sxs-lookup"><span data-stu-id="0ef00-242">Nine or ten digits with an optional backslashl:</span></span>
  
- <span data-ttu-id="0ef00-243">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-243">Six digits</span></span> 
    
- <span data-ttu-id="0ef00-244">Ein umgekehrter Schrägstrich (optional)</span><span class="sxs-lookup"><span data-stu-id="0ef00-244">A backslash (optional)</span></span>
    
- <span data-ttu-id="0ef00-245">Drei oder vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-245">Three or four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-246">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-246">Checksum</span></span>

<span data-ttu-id="0ef00-247">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-247">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-248">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-248">Definition</span></span>

<span data-ttu-id="0ef00-249">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-249">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-250">Der reguläre Ausdruck `Regex_czech_republic_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-250">The regular expression  `Regex_czech_republic_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-251">Ein Schlüsselwort `Keywords_czech_republic_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-251">A keyword from  `Keywords_czech_republic_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_czech_republic_eu_tax_file_number" />
          <Match idRef="Keywords_czech_republic_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-252">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-252">Keywords</span></span>

#### <a name="keywordsczechrepubliceutaxfilenumber"></a><span data-ttu-id="0ef00-253">Keywords_czech_republic_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-253">Keywords_czech_republic_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-254">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-254">tax number</span></span>
  
<span data-ttu-id="0ef00-255">Steuer</span><span class="sxs-lookup"><span data-stu-id="0ef00-255">tax</span></span>
  
<span data-ttu-id="0ef00-256">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-256">tax id</span></span>
  
<span data-ttu-id="0ef00-257">persönliche Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-257">personal number</span></span>
  
<span data-ttu-id="0ef00-258">Daňové číslo</span><span class="sxs-lookup"><span data-stu-id="0ef00-258">daňové číslo</span></span>
  
<span data-ttu-id="0ef00-259">Osobní číslo</span><span class="sxs-lookup"><span data-stu-id="0ef00-259">osobní číslo</span></span>
  
## <a name="denmark"></a><span data-ttu-id="0ef00-260">Dänemark</span><span class="sxs-lookup"><span data-stu-id="0ef00-260">Denmark</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-261">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-261">Format</span></span>

<span data-ttu-id="0ef00-262">Zehn Ziffern mit einem Bindestrich</span><span class="sxs-lookup"><span data-stu-id="0ef00-262">Ten digits containing a hyphen</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-263">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-263">Pattern</span></span>

<span data-ttu-id="0ef00-264">Zehn Ziffern, die einen Bindestrich enthalten:</span><span class="sxs-lookup"><span data-stu-id="0ef00-264">Ten digits containing a hyphenl:</span></span>
  
-  <span data-ttu-id="0ef00-265">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="0ef00-265">Six digits that correspond to the birth date (DDMMYY)</span></span> 
    
- <span data-ttu-id="0ef00-266">Ein Bindestrich </span><span class="sxs-lookup"><span data-stu-id="0ef00-266">A hyphen</span></span>
    
- <span data-ttu-id="0ef00-267">Vier Ziffern, die einer Sequenznummer entsprechen, wobei die erste Ziffer dem Jahrhundert der Geburt entspricht und die letzte Ziffer dem Geschlecht des einzelnen entspricht (ungerade für männlich und sogar für weiblich)</span><span class="sxs-lookup"><span data-stu-id="0ef00-267">Four digits that correspond to a sequence number where the first digit corresponds to the century of birth and the last digit corresponds to the individual's gender (odd for male and even for female)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-268">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-268">Checksum</span></span>

<span data-ttu-id="0ef00-269">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-269">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-270">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-270">Definition</span></span>

<span data-ttu-id="0ef00-271">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-271">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-272">Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-272">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-273">Ein Schlüsselwort `Keywords_denmark_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-273">A keyword from  `Keywords_denmark_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-274">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-274">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-275">Die Funktion `Func_denmark_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-275">The function  `Func_denmark_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
          <Match idRef="Keywords_denmark_eu_tax_file_number" />
        </Pattern> 
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_denmark_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-276">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-276">Keywords</span></span>

#### <a name="keywordsdenmarkeutaxfilenumber"></a><span data-ttu-id="0ef00-277">Keywords_denmark_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-277">Keywords_denmark_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-278">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-278">tax number</span></span>
  
<span data-ttu-id="0ef00-279">Steuer</span><span class="sxs-lookup"><span data-stu-id="0ef00-279">tax</span></span>
  
<span data-ttu-id="0ef00-280">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-280">tax id</span></span>
  
<span data-ttu-id="0ef00-281">CPR-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-281">cpr number</span></span>
  
<span data-ttu-id="0ef00-282">CPR</span><span class="sxs-lookup"><span data-stu-id="0ef00-282">cpr#</span></span>
  
<span data-ttu-id="0ef00-283">Skate Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-283">skat nummer</span></span>
  
<span data-ttu-id="0ef00-284">Skat-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-284">skat id</span></span>
  
## <a name="estonia"></a><span data-ttu-id="0ef00-285">Estland</span><span class="sxs-lookup"><span data-stu-id="0ef00-285">Estonia</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-286">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-286">Format</span></span>

<span data-ttu-id="0ef00-287">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-287">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-288">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-288">Pattern</span></span>

<span data-ttu-id="0ef00-289">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0ef00-289">11 digits:</span></span>
  
-  <span data-ttu-id="0ef00-290">Eine Ziffer, die dem Geschlecht und dem Jahrhundert der Geburt entspricht, wobei eine ungerade Zahl männliche und die gerade Zahl angibt, wie folgt: 1,2 für das 19. Jahrhundert; 3, 4 für das 20. Jahrhundert; und 5, 6 für das 21. Jahrhundert</span><span class="sxs-lookup"><span data-stu-id="0ef00-290">One digit that corresponds to gender and century of birth where an odd number indicates male and the even number indicates female as follows: 1, 2 for the 19th century; 3, 4 for the 20th century; and 5, 6 for the 21st century</span></span> 
    
- <span data-ttu-id="0ef00-291">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="0ef00-291">Six digits that correspond to birth date (YYMMDD)</span></span>
    
- <span data-ttu-id="0ef00-292">Drei Ziffern, die einer Seriennummer entsprechen, die Personen trennt, die am selben Datum geboren wurden</span><span class="sxs-lookup"><span data-stu-id="0ef00-292">Three digits that correspond to a serial number separating persons born on the same date</span></span>
    
- <span data-ttu-id="0ef00-293">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0ef00-293">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-294">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-294">Checksum</span></span>

<span data-ttu-id="0ef00-295">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-295">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-296">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-296">Definition</span></span>

<span data-ttu-id="0ef00-297">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-297">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-298">Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-298">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-299">Ein Schlüsselwort `Keywords_estonia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-299">A keyword from  `Keywords_estonia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-300">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-300">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-301">Die Funktion `Func_estonia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-301">The function  `Func_estonia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
          <Match idRef="Keywords_estonia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_estonia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-302">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-302">Keywords</span></span>

#### <a name="keywordsestoniaeutaxfilenumber"></a><span data-ttu-id="0ef00-303">Keywords_estonia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-303">Keywords_estonia_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-304">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-304">tax number</span></span>
  
<span data-ttu-id="0ef00-305">Steuer</span><span class="sxs-lookup"><span data-stu-id="0ef00-305">tax</span></span>
  
<span data-ttu-id="0ef00-306">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-306">tax id</span></span>
  
<span data-ttu-id="0ef00-307">persönlicher Code</span><span class="sxs-lookup"><span data-stu-id="0ef00-307">personal code</span></span>
  
<span data-ttu-id="0ef00-308">maksunumber</span><span class="sxs-lookup"><span data-stu-id="0ef00-308">maksunumber</span></span>
  
<span data-ttu-id="0ef00-309">maksu-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-309">maksu id</span></span>
  
<span data-ttu-id="0ef00-310">Isikukood</span><span class="sxs-lookup"><span data-stu-id="0ef00-310">isikukood</span></span>
  
## <a name="finland"></a><span data-ttu-id="0ef00-311">Finnland</span><span class="sxs-lookup"><span data-stu-id="0ef00-311">Finland</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-312">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-312">Format</span></span>

<span data-ttu-id="0ef00-313">Eine 11-stellige Kombination aus Ziffern, Buchstaben und Plus-und Minuszeichen</span><span class="sxs-lookup"><span data-stu-id="0ef00-313">An 11-character combination of digits, letters, and plus and minus sign</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-314">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-314">Pattern</span></span>

<span data-ttu-id="0ef00-315">Eine 11-stellige Kombination aus Ziffern, Buchstaben und Plus-und Minuszeichen:</span><span class="sxs-lookup"><span data-stu-id="0ef00-315">An 11-character combination of digits, letters, and plus and minus sign:</span></span>
  
- <span data-ttu-id="0ef00-316">Sechs Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-316">Six digits</span></span>
    
- <span data-ttu-id="0ef00-317">Eine der folgenden Optionen: ein Pluszeichen, ein Minuszeichen oder der Buchstabe "A" (ohne Beachtung der Groß-/Kleinschreibung), wobei das Pluszeichen zwischen 1800-1899, das Minuszeichen zwischen 1900-1999 und "A" als geboren 2000 und nach</span><span class="sxs-lookup"><span data-stu-id="0ef00-317">One of the following: a plus sign, a minus sign, or the letter "A" (not case sensitive) where the plus sign means born between 1800-1899, the minus sign means born between 1900-1999, and "A" means born 2000 and after</span></span>
    
- <span data-ttu-id="0ef00-318">Drei Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-318">Three digits</span></span>
    
- <span data-ttu-id="0ef00-319">Ein Buchstaben oder eine Zahl</span><span class="sxs-lookup"><span data-stu-id="0ef00-319">One letter or one number</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-320">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-320">Checksum</span></span>

<span data-ttu-id="0ef00-321">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-321">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-322">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-322">Definition</span></span>

<span data-ttu-id="0ef00-323">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-323">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-324">Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-324">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-325">Ein Schlüsselwort `Keywords_finland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-325">A keyword from  `Keywords_finland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-326">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-326">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-327">Die Funktion `Func_finland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-327">The function  `Func_finland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
          <Match idRef="Keywords_finland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_finland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-328">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-328">Keywords</span></span>

#### <a name="keywordsfinlandeutaxfilenumber"></a><span data-ttu-id="0ef00-329">Keywords_finland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-329">Keywords_finland_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-330">identification number</span><span class="sxs-lookup"><span data-stu-id="0ef00-330">identification number</span></span>
  
<span data-ttu-id="0ef00-331">persönliche ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-331">personal id</span></span>
  
<span data-ttu-id="0ef00-332">Identitätsnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-332">identity number</span></span>
  
<span data-ttu-id="0ef00-333">nationale finnische ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-333">finnish national id number</span></span>
  
<span data-ttu-id="0ef00-334">personalidnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-334">personalidnumber#</span></span>
  
<span data-ttu-id="0ef00-335">national identification number</span><span class="sxs-lookup"><span data-stu-id="0ef00-335">national identification number</span></span>
  
<span data-ttu-id="0ef00-336">ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-336">id number</span></span>
  
<span data-ttu-id="0ef00-337">nationale ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-337">national id no.</span></span>
  
<span data-ttu-id="0ef00-338">nationale ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-338">national id number</span></span>
  
<span data-ttu-id="0ef00-339">ID Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-339">id no</span></span>
  
<span data-ttu-id="0ef00-340">tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="0ef00-340">tunnistenumero</span></span>
  
<span data-ttu-id="0ef00-341">henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="0ef00-341">henkilötunnus</span></span>
  
<span data-ttu-id="0ef00-342">yksilöllinen henkilökohtainen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="0ef00-342">yksilöllinen henkilökohtainen tunnistenumero</span></span>
  
<span data-ttu-id="0ef00-343">ainutlaatuinen henkilökohtainen tunnus</span><span class="sxs-lookup"><span data-stu-id="0ef00-343">ainutlaatuinen henkilökohtainen tunnus</span></span>
  
<span data-ttu-id="0ef00-344">identiteetti numero</span><span class="sxs-lookup"><span data-stu-id="0ef00-344">identiteetti numero</span></span>
  
<span data-ttu-id="0ef00-345">Suomen der Kok henkilötunnus</span><span class="sxs-lookup"><span data-stu-id="0ef00-345">suomen kansallinen henkilötunnus</span></span>
  
<span data-ttu-id="0ef00-346">henkilötunnusnumero #</span><span class="sxs-lookup"><span data-stu-id="0ef00-346">henkilötunnusnumero#</span></span>
  
<span data-ttu-id="0ef00-347">kansallisen tunnistenumero</span><span class="sxs-lookup"><span data-stu-id="0ef00-347">kansallisen tunnistenumero</span></span>
  
<span data-ttu-id="0ef00-348">tunnusnumero</span><span class="sxs-lookup"><span data-stu-id="0ef00-348">tunnusnumero</span></span>
  
<span data-ttu-id="0ef00-349">der Kok tunnus numero</span><span class="sxs-lookup"><span data-stu-id="0ef00-349">kansallinen tunnus numero</span></span>
  
## <a name="france"></a><span data-ttu-id="0ef00-350">Frankreich</span><span class="sxs-lookup"><span data-stu-id="0ef00-350">France</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-351">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-351">Format</span></span>

<span data-ttu-id="0ef00-352">13 Ziffern für Einzelpersonen und neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="0ef00-352">13 digits for individuals and nine digits for entities</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-353">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-353">Pattern</span></span>

<span data-ttu-id="0ef00-354">13 Ziffern für Einzelpersonen:</span><span class="sxs-lookup"><span data-stu-id="0ef00-354">13 digits for individuals:</span></span>
  
- <span data-ttu-id="0ef00-355">Eine Ziffer, die 0, 1, 2 oder 3 sein muss</span><span class="sxs-lookup"><span data-stu-id="0ef00-355">One digit that must be 0, 1, 2, or 3</span></span>
    
- <span data-ttu-id="0ef00-356">12 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-356">12 digits</span></span>
    
<span data-ttu-id="0ef00-357">Neun Ziffern für Entitäten</span><span class="sxs-lookup"><span data-stu-id="0ef00-357">Nine digits for entities</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-358">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-358">Checksum</span></span>

<span data-ttu-id="0ef00-359">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-359">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-360">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-360">Definition</span></span>

<span data-ttu-id="0ef00-361">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-361">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-362">Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-362">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-363">Ein Schlüsselwort `Keywords_france_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-363">A keyword from  `Keywords_france_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-364">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-364">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-365">Die Funktion `Func_france_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-365">The function  `Func_france_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
          <Match idRef="Keywords_france_eu_tax_file_number" />
        </Pattern>
 <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_france_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-366">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-366">Keywords</span></span>

#### <a name="keywordsfranceeutaxfilenumber"></a><span data-ttu-id="0ef00-367">Keywords_france_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-367">Keywords_france_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-368">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-368">tax identification number</span></span>
  
<span data-ttu-id="0ef00-369">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-369">tax number</span></span>
  
<span data-ttu-id="0ef00-370">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-370">tax id</span></span>
  
<span data-ttu-id="0ef00-371">Numéro d'identification Fiscale</span><span class="sxs-lookup"><span data-stu-id="0ef00-371">numéro d'identification fiscale</span></span>
  
## <a name="germany"></a><span data-ttu-id="0ef00-372">Deutschland</span><span class="sxs-lookup"><span data-stu-id="0ef00-372">Germany</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-373">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-373">Format</span></span>

<span data-ttu-id="0ef00-374">11 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-374">11 digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-375">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-375">Pattern</span></span>

<span data-ttu-id="0ef00-376">11 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0ef00-376">11 digits :</span></span>
  
-  <span data-ttu-id="0ef00-377">Zehn Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-377">Ten digits</span></span> 
    
- <span data-ttu-id="0ef00-378">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0ef00-378">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-379">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-379">Checksum</span></span>

<span data-ttu-id="0ef00-380">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-380">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-381">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-381">Definition</span></span>

<span data-ttu-id="0ef00-382">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-382">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-383">Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-383">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-384">Ein Schlüsselwort `Keywords_germany_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-384">A keyword from  `Keywords_germany_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-385">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-385">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-386">Die Funktion `Func_germany_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-386">The function  `Func_germany_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
          <Match idRef="Keywords_germany_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_germany_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-387">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-387">Keywords</span></span>

#### <a name="keywordsgermanyeutaxfilenumber"></a><span data-ttu-id="0ef00-388">Keywords_germany_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-388">Keywords_germany_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-389">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-389">tax number</span></span>
  
<span data-ttu-id="0ef00-390">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-390">tax no.</span></span>
  
<span data-ttu-id="0ef00-391">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-391">taxno#</span></span>
  
<span data-ttu-id="0ef00-392">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-392">taxnumber#</span></span>
  
<span data-ttu-id="0ef00-393">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0ef00-393">taxnumber</span></span>
  
<span data-ttu-id="0ef00-394">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-394">tax id</span></span>
  
<span data-ttu-id="0ef00-395">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-395">taxid#</span></span>
  
<span data-ttu-id="0ef00-396">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-396">tax identification number</span></span>
  
<span data-ttu-id="0ef00-397">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-397">tax identification no.</span></span>
  
<span data-ttu-id="0ef00-398">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-398">steuernummer</span></span>
  
<span data-ttu-id="0ef00-399">Ingo-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-399">steuer id</span></span>
  
<span data-ttu-id="0ef00-400">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-400">steueridentifikationsnummer</span></span>
  
## <a name="greece"></a><span data-ttu-id="0ef00-401">Griechenland</span><span class="sxs-lookup"><span data-stu-id="0ef00-401">Greece</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-402">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-402">Format</span></span>

<span data-ttu-id="0ef00-403">Neun Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-403">Nine digits without spaces and delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-404">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-404">Pattern</span></span>

<span data-ttu-id="0ef00-405">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-405">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-406">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-406">Checksum</span></span>

<span data-ttu-id="0ef00-407">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-407">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-408">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-408">Definition</span></span>

<span data-ttu-id="0ef00-409">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-409">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-410">Der reguläre Ausdruck `Regex_greece_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-410">The regular expression  `Regex_greece_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-411">Ein Schlüsselwort `Keywords_greece_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-411">A keyword from  `Keywords_greece_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_greece_eu_tax_file_number" />
          <Match idRef="Keywords_greece_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-412">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-412">Keywords</span></span>

#### <a name="keywordsgreeceeutaxfilenumber"></a><span data-ttu-id="0ef00-413">Keywords_greece_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-413">Keywords_greece_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-414">AFM</span><span class="sxs-lookup"><span data-stu-id="0ef00-414">afm</span></span>
  
<span data-ttu-id="0ef00-415">Zinn</span><span class="sxs-lookup"><span data-stu-id="0ef00-415">tin</span></span>
  
<span data-ttu-id="0ef00-416">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-416">tax id no.</span></span>
  
<span data-ttu-id="0ef00-417">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-417">tax id no</span></span>
  
<span data-ttu-id="0ef00-418">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-418">tax identification number</span></span>
  
<span data-ttu-id="0ef00-419">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-419">tax registry number</span></span>
  
<span data-ttu-id="0ef00-420">Steuerregistrierungsnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-420">tax registry no.</span></span>
  
<span data-ttu-id="0ef00-421">AFM</span><span class="sxs-lookup"><span data-stu-id="0ef00-421">afm#</span></span>
  
<span data-ttu-id="0ef00-422">Zinn</span><span class="sxs-lookup"><span data-stu-id="0ef00-422">tin#</span></span>
  
<span data-ttu-id="0ef00-423">taxidno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-423">taxidno#</span></span>
  
<span data-ttu-id="0ef00-424">taxregistryno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-424">taxregistryno#</span></span>
  
<span data-ttu-id="0ef00-425">αριθμός φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0ef00-425">αριθμός φορολογικού μητρώου</span></span>
  
<span data-ttu-id="0ef00-426">aφμ</span><span class="sxs-lookup"><span data-stu-id="0ef00-426">aφμ</span></span>
  
<span data-ttu-id="0ef00-427">aφμ αριθμός</span><span class="sxs-lookup"><span data-stu-id="0ef00-427">aφμ αριθμός</span></span>
  
<span data-ttu-id="0ef00-428">φορολογικού μητρώου νο.</span><span class="sxs-lookup"><span data-stu-id="0ef00-428">φορολογικού μητρώου νο.</span></span>
  
<span data-ttu-id="0ef00-429">τον αριθμό φορολογικού μητρώου</span><span class="sxs-lookup"><span data-stu-id="0ef00-429">τον αριθμό φορολογικού μητρώου</span></span>
  
## <a name="hungary"></a><span data-ttu-id="0ef00-430">Ungarn</span><span class="sxs-lookup"><span data-stu-id="0ef00-430">Hungary</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-431">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-431">Format</span></span>

<span data-ttu-id="0ef00-432">Zehn Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-432">Ten digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-433">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-433">Pattern</span></span>

<span data-ttu-id="0ef00-434">Zehn Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0ef00-434">Ten digits:</span></span>
  
-  <span data-ttu-id="0ef00-435">Eine Ziffer, die "8" sein muss</span><span class="sxs-lookup"><span data-stu-id="0ef00-435">One digit that must be "8"</span></span> 
    
- <span data-ttu-id="0ef00-436">Fünf Ziffern, die der Anzahl von Tagen zwischen dem Datum 01/01/1867 und dem Geburtsdatum des einzelnen entsprechen</span><span class="sxs-lookup"><span data-stu-id="0ef00-436">Five digits that correspond to the number of days between the date 01/01/1867 and the date of the birth of the individual</span></span>
    
- <span data-ttu-id="0ef00-437">Drei Ziffern, die der Zahl entsprechen, die von Wahrscheinlichkeit zur Unterscheidung von Individuen generiert wurde, die am selben Tag geboren wurden</span><span class="sxs-lookup"><span data-stu-id="0ef00-437">Three digits that correspond to the number generated by chance to differentiate individuals born on the same day</span></span>
    
- <span data-ttu-id="0ef00-438">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0ef00-438">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-439">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-439">Checksum</span></span>

<span data-ttu-id="0ef00-440">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-440">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-441">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-441">Definition</span></span>

<span data-ttu-id="0ef00-442">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-442">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-443">Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-443">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-444">Ein Schlüsselwort `Keywords_hungary_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-444">A keyword from  `Keywords_hungary_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-445">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-445">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-446">Die Funktion `Func_hungary_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-446">The function  `Func_hungary_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
          <Match idRef="Keywords_hungary_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_hungary_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-447">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-447">Keywords</span></span>

#### <a name="keywordshungaryeutaxfilenumber"></a><span data-ttu-id="0ef00-448">Keywords_hungary_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-448">Keywords_hungary_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-449">ungarische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-449">hungarian tax identification number</span></span>
  
<span data-ttu-id="0ef00-450">ungarische Dose</span><span class="sxs-lookup"><span data-stu-id="0ef00-450">hungarian tin</span></span>
  
<span data-ttu-id="0ef00-451">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-451">tax id number</span></span>
  
<span data-ttu-id="0ef00-452">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-452">vat number</span></span>
  
<span data-ttu-id="0ef00-453">Finanzamt Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-453">tax authority no</span></span>
  
<span data-ttu-id="0ef00-454">USt-ID-Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-454">tax id tax identity number</span></span>
  
<span data-ttu-id="0ef00-455">taxidnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-455">taxidnumber#</span></span>
  
<span data-ttu-id="0ef00-456">Zinn</span><span class="sxs-lookup"><span data-stu-id="0ef00-456">tin#</span></span>
  
<span data-ttu-id="0ef00-457">hungatiantin #</span><span class="sxs-lookup"><span data-stu-id="0ef00-457">hungatiantin#</span></span>
  
<span data-ttu-id="0ef00-458">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-458">tax identification no</span></span>
  
<span data-ttu-id="0ef00-459">taxidno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-459">taxidno#</span></span>
  
<span data-ttu-id="0ef00-460">adóazonosító szám</span><span class="sxs-lookup"><span data-stu-id="0ef00-460">adóazonosító szám</span></span>
  
<span data-ttu-id="0ef00-461">adószám</span><span class="sxs-lookup"><span data-stu-id="0ef00-461">adószám</span></span>
  
<span data-ttu-id="0ef00-462">adóhatóság szám</span><span class="sxs-lookup"><span data-stu-id="0ef00-462">adóhatóság szám</span></span>
  
## <a name="ireland"></a><span data-ttu-id="0ef00-463">Irland</span><span class="sxs-lookup"><span data-stu-id="0ef00-463">Ireland</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-464">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-464">Format</span></span>

<span data-ttu-id="0ef00-465">Sieben Ziffern, gefolgt von einem Buchstaben ohne Leerzeichen und Trennzeichen</span><span class="sxs-lookup"><span data-stu-id="0ef00-465">Seven digits followed by a letter with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-466">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-466">Pattern</span></span>

<span data-ttu-id="0ef00-467">Sieben Ziffern gefolgt von einem Buchstaben:</span><span class="sxs-lookup"><span data-stu-id="0ef00-467">Seven digits followed by a letter:</span></span>
  
-  <span data-ttu-id="0ef00-468">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0ef00-468">Seven digits</span></span> 
    
- <span data-ttu-id="0ef00-469">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0ef00-469">One letter (not case-sensitive)</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-470">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-470">Checksum</span></span>

<span data-ttu-id="0ef00-471">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-471">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-472">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-472">Definition</span></span>

<span data-ttu-id="0ef00-473">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-473">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-474">Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-474">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-475">Ein Schlüsselwort `Keywords_ireland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-475">A keyword from  `Keywords_ireland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-476">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-476">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-477">Die Funktion `Func_ireland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-477">The function  `Func_ireland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
          <Match idRef="Keywords_ireland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_ireland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-478">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-478">Keywords</span></span>

#### <a name="keywordsirelandeutaxfilenumber"></a><span data-ttu-id="0ef00-479">Keywords_ireland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-479">Keywords_ireland_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-480">öffentlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-480">public service no</span></span>
  
<span data-ttu-id="0ef00-481">persönlicher öffentlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-481">personal public service no</span></span>
  
<span data-ttu-id="0ef00-482">PPS Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-482">pps no</span></span>
  
<span data-ttu-id="0ef00-483">persönlicher Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-483">personal service no</span></span>
  
<span data-ttu-id="0ef00-484">PPS-Dienst Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-484">pps service no</span></span>
  
<span data-ttu-id="0ef00-485">ppsno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-485">ppsno#</span></span>
  
<span data-ttu-id="0ef00-486">Irisch PPS Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-486">irish pps no</span></span>
  
<span data-ttu-id="0ef00-487">publicserviceno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-487">publicserviceno#</span></span>
  
<span data-ttu-id="0ef00-488">persönliche öffentliche Dienstnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-488">personal public service number</span></span>
  
<span data-ttu-id="0ef00-489">uimhir phearsanta seirbhíse poiblí</span><span class="sxs-lookup"><span data-stu-id="0ef00-489">uimhir phearsanta seirbhíse poiblí</span></span>
  
<span data-ttu-id="0ef00-490">PPS-uimh</span><span class="sxs-lookup"><span data-stu-id="0ef00-490">pps uimh</span></span>
  
<span data-ttu-id="0ef00-491">uimhir aitheantais phearsanta</span><span class="sxs-lookup"><span data-stu-id="0ef00-491">uimhir aitheantais phearsanta</span></span>
  
## <a name="italy"></a><span data-ttu-id="0ef00-492">Italien</span><span class="sxs-lookup"><span data-stu-id="0ef00-492">Italy</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-493">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-493">Format</span></span>

<span data-ttu-id="0ef00-494">16 Buchstaben und Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-494">16 letters and digits in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-495">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-495">Pattern</span></span>

<span data-ttu-id="0ef00-496">16 Buchstaben und Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0ef00-496">16 letters and digits:</span></span>
  
-  <span data-ttu-id="0ef00-497">Drei Buchstaben, die den ersten drei Konsonanten im Familiennamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="0ef00-497">Three letters that correspond to the first three consonants in the family name</span></span> 
    
- <span data-ttu-id="0ef00-498">Drei Buchstaben, die dem ersten, dritten und vierten Konsonanten im Vornamen entsprechen</span><span class="sxs-lookup"><span data-stu-id="0ef00-498">Three letters that correspond to the first, third, and fourth consonants in the first name</span></span>
    
- <span data-ttu-id="0ef00-499">Zwei Ziffern, die den letzten Ziffern des Geburtsjahrs entsprechen</span><span class="sxs-lookup"><span data-stu-id="0ef00-499">Two digits that correspond to the last digits of the birth year</span></span>
    
- <span data-ttu-id="0ef00-500">Eine Ziffer, die dem Geburtsmonat entspricht – Buchstaben werden in alphabetischer Reihenfolge verwendet, aber nur die Buchstaben A bis E, H, L, M, P, R bis T werden verwendet (also Januar ist A und Oktober ist R)</span><span class="sxs-lookup"><span data-stu-id="0ef00-500">One digit that corresponds to the month of birth—letters are used in alphabetical order, but only the letters A to E, H, L, M, P, R to T are used (thus, January is A and October is R)</span></span>
    
- <span data-ttu-id="0ef00-501">Zwei Ziffern, die dem Tag des Geburtsmonats entsprechen, wobei 40 zum Geburtstag hinzugefügt wird, damit Frauen von Männern unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-501">Two digits that correspond to the day of the month of birth where 40 is added to the day of birth for females to differentiate from males</span></span>
    
- <span data-ttu-id="0ef00-502">Vier Ziffern, die einer Ortskennzahl für die Gemeinde entsprechen, in der die Person geboren wurde – landesweite Codes werden für fremde Länder verwendet</span><span class="sxs-lookup"><span data-stu-id="0ef00-502">Four digits that correspond to an area code specific to the municipality where the person was born—country-wide codes are used for foreign countries</span></span>
    
- <span data-ttu-id="0ef00-503">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0ef00-503">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-504">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-504">Checksum</span></span>

<span data-ttu-id="0ef00-505">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-505">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-506">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-506">Definition</span></span>

<span data-ttu-id="0ef00-507">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-507">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-508">Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-508">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-509">Ein Schlüsselwort `Keywords_italy_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-509">A keyword from  `Keywords_italy_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-510">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-510">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-511">Die Funktion `Func_italy_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-511">The function  `Func_italy_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
          <Match idRef="Keywords_italy_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_italy_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-512">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-512">Keywords</span></span>

#### <a name="keywordsitalyeutaxfilenumber"></a><span data-ttu-id="0ef00-513">Keywords_italy_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-513">Keywords_italy_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-514">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-514">tax number</span></span>
  
<span data-ttu-id="0ef00-515">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-515">tax no.</span></span>
  
<span data-ttu-id="0ef00-516">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-516">taxno#</span></span>
  
<span data-ttu-id="0ef00-517">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-517">taxnumber#</span></span>
  
<span data-ttu-id="0ef00-518">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0ef00-518">taxnumber</span></span>
  
<span data-ttu-id="0ef00-519">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-519">tax id</span></span>
  
<span data-ttu-id="0ef00-520">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-520">taxid#</span></span>
  
<span data-ttu-id="0ef00-521">Fiskal Code</span><span class="sxs-lookup"><span data-stu-id="0ef00-521">fiscal code</span></span>
  
<span data-ttu-id="0ef00-522">Geschäftsjahr</span><span class="sxs-lookup"><span data-stu-id="0ef00-522">codice fiscale</span></span>
  
## <a name="latvia"></a><span data-ttu-id="0ef00-523">Lettland</span><span class="sxs-lookup"><span data-stu-id="0ef00-523">Latvia</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-524">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-524">Format</span></span>

<span data-ttu-id="0ef00-525">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-525">11 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-526">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-526">Pattern</span></span>

<span data-ttu-id="0ef00-527">11 Ziffern im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-527">11 digits in the specified pattern</span></span>
  
-  <span data-ttu-id="0ef00-528">Sechs Ziffern, die dem Geburtsdatum entsprechen (TTMMJJ)</span><span class="sxs-lookup"><span data-stu-id="0ef00-528">Six digits that correspond to the date of birth (DDMMYY)</span></span> 
    
- <span data-ttu-id="0ef00-529">Eine Ziffer, die dem Jahrhundert der Geburt entspricht, wobei "0" dem 19. Jahrhundert entspricht, "1" entspricht dem 20. Jahrhundert, und "2" entspricht dem 21. Jahrhundert</span><span class="sxs-lookup"><span data-stu-id="0ef00-529">One digit that corresponds to the century of birth where "0" corresponds to 19th century, "1" corresponds to 20th century, and "2"corresponds to 21st century</span></span>
    
- <span data-ttu-id="0ef00-530">Vier Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-530">Four digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-531">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-531">Checksum</span></span>

<span data-ttu-id="0ef00-532">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-532">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-533">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-533">Definition</span></span>

<span data-ttu-id="0ef00-534">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-534">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-535">Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-535">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-536">Ein Schlüsselwort `Keywords_latvia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-536">A keyword from  `Keywords_latvia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-537">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-537">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-538">Die Funktion `Func_latvia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-538">The function  `Func_latvia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
          <Match idRef="Keywords_latvia_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_latvia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-539">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-539">Keywords</span></span>

#### <a name="keywordslatviaeutaxfilenumber"></a><span data-ttu-id="0ef00-540">Keywords_latvia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-540">Keywords_latvia_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-541">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-541">tax number</span></span>
  
<span data-ttu-id="0ef00-542">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-542">tax no.</span></span>
  
<span data-ttu-id="0ef00-543">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-543">taxno#</span></span>
  
<span data-ttu-id="0ef00-544">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-544">taxnumber#</span></span>
  
<span data-ttu-id="0ef00-545">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0ef00-545">taxnumber</span></span>
  
<span data-ttu-id="0ef00-546">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-546">tax id</span></span>
  
<span data-ttu-id="0ef00-547">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-547">taxid#</span></span>
  
<span data-ttu-id="0ef00-548">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-548">tax identification number</span></span>
  
<span data-ttu-id="0ef00-549">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-549">tax identification no.</span></span>
  
<span data-ttu-id="0ef00-550">nodokļa numurs</span><span class="sxs-lookup"><span data-stu-id="0ef00-550">nodokļa numurs</span></span>
  
<span data-ttu-id="0ef00-551">nodokļu identifikācijas numurs</span><span class="sxs-lookup"><span data-stu-id="0ef00-551">nodokļu identifikācijas numurs</span></span>
  
<span data-ttu-id="0ef00-552">nodokļu identifikācija numurs</span><span class="sxs-lookup"><span data-stu-id="0ef00-552">nodokļu identifikācija numurs</span></span>
  
## <a name="lithuania"></a><span data-ttu-id="0ef00-553">Litauen</span><span class="sxs-lookup"><span data-stu-id="0ef00-553">Lithuania</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-554">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-554">Format</span></span>

<span data-ttu-id="0ef00-555">11 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-555">11 digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-556">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-556">Pattern</span></span>

<span data-ttu-id="0ef00-557">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-557">11 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-558">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-558">Checksum</span></span>

<span data-ttu-id="0ef00-559">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-559">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-560">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-560">Definition</span></span>

<span data-ttu-id="0ef00-561">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-561">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-562">Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-562">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-563">Ein Schlüsselwort `Keywords_lithuania_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-563">A keyword from  `Keywords_lithuania_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-564">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-564">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-565">Die Funktion `Func_lithuania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-565">The function  `Func_lithuania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
          <Match idRef="Keywords_lithuania_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_lithuania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-566">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-566">Keywords</span></span>

#### <a name="keywordslithuaniaeutaxfilenumber"></a><span data-ttu-id="0ef00-567">Keywords_lithuania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-567">Keywords_lithuania_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-568">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-568">tax number</span></span>
  
<span data-ttu-id="0ef00-569">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-569">tax no.</span></span>
  
<span data-ttu-id="0ef00-570">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-570">tax no#</span></span>
  
<span data-ttu-id="0ef00-571">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-571">taxnumber#</span></span>
  
<span data-ttu-id="0ef00-572">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0ef00-572">taxnumber</span></span>
  
<span data-ttu-id="0ef00-573">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-573">tax id</span></span>
  
<span data-ttu-id="0ef00-574">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-574">taxid#</span></span>
  
<span data-ttu-id="0ef00-575">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-575">tax identification number</span></span>
  
<span data-ttu-id="0ef00-576">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-576">tax identification no.</span></span>
  
<span data-ttu-id="0ef00-577">mokesčių-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-577">mokesčių id</span></span>
  
<span data-ttu-id="0ef00-578">mokesčių Numeris</span><span class="sxs-lookup"><span data-stu-id="0ef00-578">mokesčių numeris</span></span>
  
<span data-ttu-id="0ef00-579">mokesčių identifikavimas Numeris</span><span class="sxs-lookup"><span data-stu-id="0ef00-579">mokesčių identifikavimas numeris</span></span>
  
## <a name="luxemburg"></a><span data-ttu-id="0ef00-580">Luxemburg</span><span class="sxs-lookup"><span data-stu-id="0ef00-580">Luxemburg</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-581">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-581">Format</span></span>

<span data-ttu-id="0ef00-582">13 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-582">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-583">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-583">Pattern</span></span>

<span data-ttu-id="0ef00-584">13 Ziffern:</span><span class="sxs-lookup"><span data-stu-id="0ef00-584">13 digits:</span></span>
  
-  <span data-ttu-id="0ef00-585">11 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-585">11 digits</span></span> 
    
- <span data-ttu-id="0ef00-586">Zwei Prüfziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-586">Two check digits</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-587">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-587">Checksum</span></span>

<span data-ttu-id="0ef00-588">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-588">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-589">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-589">Definition</span></span>

<span data-ttu-id="0ef00-590">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-590">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-591">Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-591">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-592">Ein Schlüsselwort `Keywords_luxemburg_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-592">A keyword from  `Keywords_luxemburg_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-593">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-593">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-594">Die Funktion `Func_luxemburg_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-594">The function  `Func_luxemburg_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
          <Match idRef="Keywords_luxemburg_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_luxemburg_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-595">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-595">Keywords</span></span>

#### <a name="keywordsluxemburgeutaxfilenumber"></a><span data-ttu-id="0ef00-596">Keywords_luxemburg_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-596">Keywords_luxemburg_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-597">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-597">tax number</span></span>
  
<span data-ttu-id="0ef00-598">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-598">tax no.</span></span>
  
<span data-ttu-id="0ef00-599">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-599">taxno#</span></span>
  
<span data-ttu-id="0ef00-600">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-600">taxnumber#</span></span>
  
<span data-ttu-id="0ef00-601">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0ef00-601">taxnumber</span></span>
  
<span data-ttu-id="0ef00-602">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-602">tax id</span></span>
  
<span data-ttu-id="0ef00-603">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-603">taxid#</span></span>
  
<span data-ttu-id="0ef00-604">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-604">tax identification number</span></span>
  
<span data-ttu-id="0ef00-605">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-605">tax identification no.</span></span>
  
<span data-ttu-id="0ef00-606">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-606">steuernummer</span></span>
  
<span data-ttu-id="0ef00-607">Ingo-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-607">steuer id</span></span>
  
<span data-ttu-id="0ef00-608">Steueridentifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-608">steueridentifikationsnummer</span></span>
  
## <a name="malta"></a><span data-ttu-id="0ef00-609">Malta</span><span class="sxs-lookup"><span data-stu-id="0ef00-609">Malta</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-610">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-610">Format</span></span>

<span data-ttu-id="0ef00-611">Für maltesische Staatsangehörige: 7 Ziffern und ein Buchstabe im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-611">For Maltese nationals: 7 digits and one letter in the specified pattern</span></span>
  
<span data-ttu-id="0ef00-612">Nicht maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-612">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-613">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-613">Pattern</span></span>

<span data-ttu-id="0ef00-614">Maltesische Staatsangehörige: 7 Ziffern und ein Buchstabe</span><span class="sxs-lookup"><span data-stu-id="0ef00-614">Maltese nationals: 7 digits and one letter</span></span>
  
-  <span data-ttu-id="0ef00-615">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0ef00-615">Seven digits</span></span> 
    
- <span data-ttu-id="0ef00-616">Ein Buchstabe (ohne Berücksichtigung der Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0ef00-616">One letter (not case-sensitive)</span></span>
    
<span data-ttu-id="0ef00-617">Nicht maltesische Staatsangehörige und maltesische Entitäten: 9 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-617">Non-Maltese nationals and Maltese entities: 9 digits</span></span>
  
-  <span data-ttu-id="0ef00-618">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-618">Nine digits</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="0ef00-619">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-619">Checksum</span></span>

<span data-ttu-id="0ef00-620">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-620">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-621">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-621">Definition</span></span>

<span data-ttu-id="0ef00-622">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-622">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-623">Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-623">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-624">Ein Schlüsselwort `Keywords_malta_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-624">A keyword from  `Keywords_malta_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-625">Eine DLP-Richtlinie ist zu 65 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-625">A DLP policy is 65% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-626">Die Funktion `Func_malta_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-626">The function  `Func_malta_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_malta_eu_tax_file_number" />
          <Match idRef="Keywords_malta_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="65">
          <IdMatch idRef="Regex_malta_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-627">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-627">Keywords</span></span>

#### <a name="keywordsmaltaeutaxfilenumber"></a><span data-ttu-id="0ef00-628">Keywords_malta_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-628">Keywords_malta_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-629">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-629">tax number</span></span>
  
<span data-ttu-id="0ef00-630">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-630">tax no.</span></span>
  
<span data-ttu-id="0ef00-631">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-631">taxno#</span></span>
  
<span data-ttu-id="0ef00-632">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-632">taxnumber#</span></span>
  
<span data-ttu-id="0ef00-633">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0ef00-633">taxnumber</span></span>
  
<span data-ttu-id="0ef00-634">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-634">tax id</span></span>
  
<span data-ttu-id="0ef00-635">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-635">taxid#</span></span>
  
<span data-ttu-id="0ef00-636">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-636">tax identification number</span></span>
  
<span data-ttu-id="0ef00-637">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-637">tax identification no.</span></span>
  
<span data-ttu-id="0ef00-638">numru tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="0ef00-638">numru tat-taxxa</span></span>
  
<span data-ttu-id="0ef00-639">ID tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="0ef00-639">id tat-taxxa</span></span>
  
<span data-ttu-id="0ef00-640">numru ta ' identifikazzjoni tat-Taxxa</span><span class="sxs-lookup"><span data-stu-id="0ef00-640">numru ta 'identifikazzjoni tat-taxxa</span></span>
  
## <a name="netherlands"></a><span data-ttu-id="0ef00-641">Niederlande</span><span class="sxs-lookup"><span data-stu-id="0ef00-641">Netherlands</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-642">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-642">Format</span></span>

<span data-ttu-id="0ef00-643">Neun Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-643">Nine digits without spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-644">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-644">Pattern</span></span>

<span data-ttu-id="0ef00-645">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-645">Nine digits</span></span> 
  
### <a name="checksum"></a><span data-ttu-id="0ef00-646">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-646">Checksum</span></span>

<span data-ttu-id="0ef00-647">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-647">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-648">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-648">Definition</span></span>

<span data-ttu-id="0ef00-649">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-649">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-650">Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-650">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-651">Ein Schlüsselwort `Keywords_netherlands_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-651">A keyword from  `Keywords_netherlands_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-652">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-652">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-653">Die Funktion `Func_netherlands_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-653">The function  `Func_netherlands_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
          <Match idRef="Keywords_netherlands_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_netherlands_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-654">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-654">Keywords</span></span>

#### <a name="keywordsnetherlandseutaxfilenumber"></a><span data-ttu-id="0ef00-655">Keywords_netherlands_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-655">Keywords_netherlands_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-656">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-656">netherlands tax identification number</span></span>
  
<span data-ttu-id="0ef00-657">niederländische Steueridentifikation</span><span class="sxs-lookup"><span data-stu-id="0ef00-657">netherlands tax identification</span></span>
  
<span data-ttu-id="0ef00-658">USt-ID-Nummer Niederlande</span><span class="sxs-lookup"><span data-stu-id="0ef00-658">netherland's tax identification number</span></span>
  
<span data-ttu-id="0ef00-659">niederländische Steueridentifikation</span><span class="sxs-lookup"><span data-stu-id="0ef00-659">netherland's tax identification</span></span>
  
<span data-ttu-id="0ef00-660">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-660">tax identification number</span></span>
  
<span data-ttu-id="0ef00-661">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-661">dutch tax id</span></span>
  
<span data-ttu-id="0ef00-662">niederländische Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-662">dutch tax identification number</span></span>
  
<span data-ttu-id="0ef00-663">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-663">tax id</span></span>
  
<span data-ttu-id="0ef00-664">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-664">tax id#</span></span>
  
<span data-ttu-id="0ef00-665">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-665">tax number</span></span>
  
<span data-ttu-id="0ef00-666">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-666">tax no#</span></span>
  
<span data-ttu-id="0ef00-667">Steuer</span><span class="sxs-lookup"><span data-stu-id="0ef00-667">tax#</span></span>
  
<span data-ttu-id="0ef00-668">Zinn</span><span class="sxs-lookup"><span data-stu-id="0ef00-668">tin</span></span>
  
<span data-ttu-id="0ef00-669">Zinn</span><span class="sxs-lookup"><span data-stu-id="0ef00-669">tin#</span></span>
  
<span data-ttu-id="0ef00-670">Niederlande Zinn</span><span class="sxs-lookup"><span data-stu-id="0ef00-670">netherlands tin</span></span>
  
<span data-ttu-id="0ef00-671">Zinn der Niederlande</span><span class="sxs-lookup"><span data-stu-id="0ef00-671">netherland's tin</span></span>
  
<span data-ttu-id="0ef00-672">Nederlands identificatienummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-672">nederlands belasting identificatienummer</span></span>
  
<span data-ttu-id="0ef00-673">identificatienummer van belastend</span><span class="sxs-lookup"><span data-stu-id="0ef00-673">identificatienummer van belasting</span></span>
  
<span data-ttu-id="0ef00-674">identificatienummer-Belastungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-674">identificatienummer belasting</span></span>
  
<span data-ttu-id="0ef00-675">Nederlands identificatie</span><span class="sxs-lookup"><span data-stu-id="0ef00-675">nederlands belasting identificatie</span></span>
  
<span data-ttu-id="0ef00-676">Nederlands-Nummer-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-676">nederlands belasting id nummer</span></span>
  
<span data-ttu-id="0ef00-677">Nederlands belastingnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-677">nederlands belastingnummer</span></span>
  
<span data-ttu-id="0ef00-678">BTW Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-678">btw nummer</span></span>
  
<span data-ttu-id="0ef00-679">Nederlandse identificatie</span><span class="sxs-lookup"><span data-stu-id="0ef00-679">nederlandse belasting identificatie</span></span>
  
## <a name="poland"></a><span data-ttu-id="0ef00-680">Polen</span><span class="sxs-lookup"><span data-stu-id="0ef00-680">Poland</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-681">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-681">Format</span></span>

<span data-ttu-id="0ef00-682">Elf Ziffern ohne Leerzeichen</span><span class="sxs-lookup"><span data-stu-id="0ef00-682">Eleven digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-683">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-683">Pattern</span></span>

<span data-ttu-id="0ef00-684">Elf Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-684">Eleven digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-685">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-685">Checksum</span></span>

<span data-ttu-id="0ef00-686">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-686">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-687">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-687">Definition</span></span>

<span data-ttu-id="0ef00-688">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-688">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-689">Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-689">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-690">Ein Schlüsselwort `Keywords_poland_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-690">A keyword from  `Keywords_poland_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-691">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-691">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-692">Die Funktion `Func_poland_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-692">The function  `Func_poland_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
          <Match idRef="Keywords_poland_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_poland_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-693">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-693">Keywords</span></span>

#### <a name="keywordspolandeutaxfilenumber"></a><span data-ttu-id="0ef00-694">Keywords_poland_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-694">Keywords_poland_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-695">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-695">tax number</span></span>
  
<span data-ttu-id="0ef00-696">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-696">tax no.</span></span>
  
<span data-ttu-id="0ef00-697">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-697">taxno#</span></span>
  
<span data-ttu-id="0ef00-698">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-698">taxnumber#</span></span>
  
<span data-ttu-id="0ef00-699">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0ef00-699">taxnumber</span></span>
  
<span data-ttu-id="0ef00-700">NIP</span><span class="sxs-lookup"><span data-stu-id="0ef00-700">nip</span></span>
  
<span data-ttu-id="0ef00-701">NIP</span><span class="sxs-lookup"><span data-stu-id="0ef00-701">nip#</span></span>
  
<span data-ttu-id="0ef00-702">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-702">tax id</span></span>
  
<span data-ttu-id="0ef00-703">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-703">tax id#</span></span>
  
<span data-ttu-id="0ef00-704">NIP-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-704">nip id</span></span>
  
<span data-ttu-id="0ef00-705">NIP-ID #</span><span class="sxs-lookup"><span data-stu-id="0ef00-705">nip id#</span></span>
  
<span data-ttu-id="0ef00-706">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-706">tax identification number</span></span>
  
<span data-ttu-id="0ef00-707">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-707">tax identification no.</span></span>
  
<span data-ttu-id="0ef00-708">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-708">vat number</span></span>
  
<span data-ttu-id="0ef00-709">USt-IdNr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-709">vat no.</span></span>
  
<span data-ttu-id="0ef00-710">vatno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-710">vatno#</span></span>
  
<span data-ttu-id="0ef00-711">USt-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-711">vat id</span></span>
  
<span data-ttu-id="0ef00-712">USt-ID #</span><span class="sxs-lookup"><span data-stu-id="0ef00-712">vat id#</span></span>
  
<span data-ttu-id="0ef00-713">Numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="0ef00-713">numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="0ef00-714">Polski Numer identyfikacji podatkowej</span><span class="sxs-lookup"><span data-stu-id="0ef00-714">polski numer identyfikacji podatkowej</span></span>
  
<span data-ttu-id="0ef00-715">numeridentyfikacjipodatkowej #</span><span class="sxs-lookup"><span data-stu-id="0ef00-715">numeridentyfikacjipodatkowej#</span></span>
  
## <a name="portugal"></a><span data-ttu-id="0ef00-716">Portugal</span><span class="sxs-lookup"><span data-stu-id="0ef00-716">Portugal</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-717">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-717">Format</span></span>

<span data-ttu-id="0ef00-718">Neun Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-718">Nine digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-719">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-719">Pattern</span></span>

<span data-ttu-id="0ef00-720">Neun Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-720">Nine digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-721">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-721">Checksum</span></span>

<span data-ttu-id="0ef00-722">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-722">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-723">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-723">Definition</span></span>

<span data-ttu-id="0ef00-724">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-724">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-725">Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-725">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-726">Ein Schlüsselwort `Keywords_portugal_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-726">A keyword from  `Keywords_portugal_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-727">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-727">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-728">Die Funktion `Func_portugal_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-728">The function  `Func_portugal_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
          <Match idRef="Keywords_portugal_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_portugal_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-729">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-729">Keywords</span></span>

#### <a name="keywordsportugaleutaxfilenumber"></a><span data-ttu-id="0ef00-730">Keywords_portugal_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-730">Keywords_portugal_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-731">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-731">tax number</span></span>
  
<span data-ttu-id="0ef00-732">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-732">tax no.</span></span>
  
<span data-ttu-id="0ef00-733">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-733">taxno#</span></span>
  
<span data-ttu-id="0ef00-734">taxnumber #</span><span class="sxs-lookup"><span data-stu-id="0ef00-734">taxnumber#</span></span>
  
<span data-ttu-id="0ef00-735">taxnumber</span><span class="sxs-lookup"><span data-stu-id="0ef00-735">taxnumber</span></span>
  
<span data-ttu-id="0ef00-736">NIF</span><span class="sxs-lookup"><span data-stu-id="0ef00-736">nif</span></span>
  
<span data-ttu-id="0ef00-737">NIF</span><span class="sxs-lookup"><span data-stu-id="0ef00-737">nif#</span></span>
  
<span data-ttu-id="0ef00-738">Numero Fiscal</span><span class="sxs-lookup"><span data-stu-id="0ef00-738">numero fiscal</span></span>
  
<span data-ttu-id="0ef00-739">número de identificação Fiscal</span><span class="sxs-lookup"><span data-stu-id="0ef00-739">número de identificação fiscal</span></span>
  
## <a name="romania"></a><span data-ttu-id="0ef00-740">Rumänien</span><span class="sxs-lookup"><span data-stu-id="0ef00-740">Romania</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-741">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-741">Format</span></span>

<span data-ttu-id="0ef00-742">13 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-742">13 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-743">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-743">Pattern</span></span>

<span data-ttu-id="0ef00-744">13 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-744">13 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-745">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-745">Checksum</span></span>

<span data-ttu-id="0ef00-746">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-746">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-747">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-747">Definition</span></span>

<span data-ttu-id="0ef00-748">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-748">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-749">Der reguläre Ausdruck `Regex_romania_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-749">The regular expression  `Regex_romania_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-750">Ein Schlüsselwort `Keywords_romania_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-750">A keyword from  `Keywords_romania_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_romania_eu_tax_file_number" />
          <Match idRef="Keywords_romania_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-751">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-751">Keywords</span></span>

#### <a name="keywordsromaniaeutaxfilenumber"></a><span data-ttu-id="0ef00-752">Keywords_romania_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-752">Keywords_romania_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-753">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-753">tax id</span></span>
  
<span data-ttu-id="0ef00-754">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-754">tax id number</span></span>
  
<span data-ttu-id="0ef00-755">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-755">tax file no</span></span>
  
<span data-ttu-id="0ef00-756">tax file number</span><span class="sxs-lookup"><span data-stu-id="0ef00-756">tax file number</span></span>
  
<span data-ttu-id="0ef00-757">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-757">tax no</span></span>
  
<span data-ttu-id="0ef00-758">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-758">tax number</span></span>
  
<span data-ttu-id="0ef00-759">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-759">taxid#</span></span>
  
<span data-ttu-id="0ef00-760">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-760">taxno#</span></span>
  
<span data-ttu-id="0ef00-761">ID – UL-taxei</span><span class="sxs-lookup"><span data-stu-id="0ef00-761">id-ul taxei</span></span>
  
<span data-ttu-id="0ef00-762">numărul de identificare fiscală</span><span class="sxs-lookup"><span data-stu-id="0ef00-762">numărul de identificare fiscală</span></span>
  
## <a name="slovakia"></a><span data-ttu-id="0ef00-763">Slowakei</span><span class="sxs-lookup"><span data-stu-id="0ef00-763">Slovakia</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-764">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-764">Format</span></span>

<span data-ttu-id="0ef00-765">10 Ziffern ohne Leerzeichen oder Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-765">10 digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-766">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-766">Pattern</span></span>

<span data-ttu-id="0ef00-767">10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-767">10 digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-768">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-768">Checksum</span></span>

<span data-ttu-id="0ef00-769">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="0ef00-769">Not applicable</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-770">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-770">Definition</span></span>

<span data-ttu-id="0ef00-771">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-771">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-772">Der reguläre Ausdruck `Regex_slovakia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-772">The regular expression  `Regex_slovakia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-773">Ein Schlüsselwort `Keywords_slovakia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-773">A keyword from  `Keywords_slovakia_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Regex_slovakia_eu_tax_file_number" />
          <Match idRef="Keywords_slovakia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-774">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-774">Keywords</span></span>

#### <a name="keywordsslovakiaeutaxfilenumber"></a><span data-ttu-id="0ef00-775">Keywords_slovakia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-775">Keywords_slovakia_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-776">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-776">tax id</span></span>
  
<span data-ttu-id="0ef00-777">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-777">tax id number</span></span>
  
<span data-ttu-id="0ef00-778">Tin-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-778">tin id</span></span>
  
<span data-ttu-id="0ef00-779">Tin Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-779">tin no</span></span>
  
<span data-ttu-id="0ef00-780">Slowakische Tin-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-780">slovakian tin id</span></span>
  
<span data-ttu-id="0ef00-781">Zinn</span><span class="sxs-lookup"><span data-stu-id="0ef00-781">tin</span></span>
  
<span data-ttu-id="0ef00-782">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-782">tax file no</span></span>
  
<span data-ttu-id="0ef00-783">tax file number</span><span class="sxs-lookup"><span data-stu-id="0ef00-783">tax file number</span></span>
  
<span data-ttu-id="0ef00-784">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-784">tax no</span></span>
  
<span data-ttu-id="0ef00-785">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-785">tax number</span></span>
  
<span data-ttu-id="0ef00-786">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-786">taxid#</span></span>
  
<span data-ttu-id="0ef00-787">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-787">taxno#</span></span>
  
<span data-ttu-id="0ef00-788">Daňové identifikačné číslo</span><span class="sxs-lookup"><span data-stu-id="0ef00-788">daňové identifikačné číslo</span></span>
  
<span data-ttu-id="0ef00-789">Daňové číslo</span><span class="sxs-lookup"><span data-stu-id="0ef00-789">daňové číslo</span></span>
  
<span data-ttu-id="0ef00-790">Daňové číslo SÚBORU</span><span class="sxs-lookup"><span data-stu-id="0ef00-790">daňové číslo súboru</span></span>
  
## <a name="slovenia"></a><span data-ttu-id="0ef00-791">Slowenien</span><span class="sxs-lookup"><span data-stu-id="0ef00-791">Slovenia</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-792">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-792">Format</span></span>

<span data-ttu-id="0ef00-793">Acht Ziffern ohne Leerzeichen oder Begrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-793">Eight digits with no spaces or delimiters</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-794">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-794">Pattern</span></span>

<span data-ttu-id="0ef00-795">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-795">Eight digits</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-796">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-796">Checksum</span></span>

<span data-ttu-id="0ef00-797">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-797">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-798">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-798">Definition</span></span>

<span data-ttu-id="0ef00-799">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-799">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-800">Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-800">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-801">Ein Schlüsselwort `Keywords_slovenia_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-801">A keyword from  `Keywords_slovenia_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-802">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-802">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-803">Die Funktion `Func_slovenia_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-803">The function  `Func_slovenia_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_nation_eu_tax_file_number" />
          <Match idRef="Keywords_nation_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_slovenia_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-804">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-804">Keywords</span></span>

#### <a name="keywordssloveniaeutaxfilenumber"></a><span data-ttu-id="0ef00-805">Keywords_slovenia_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-805">Keywords_slovenia_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-806">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-806">tax id</span></span>
  
<span data-ttu-id="0ef00-807">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-807">tax id number</span></span>
  
<span data-ttu-id="0ef00-808">Tin-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-808">tin id</span></span>
  
<span data-ttu-id="0ef00-809">Tin Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-809">tin no</span></span>
  
<span data-ttu-id="0ef00-810">slowenische Tin-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-810">slovenian tin id</span></span>
  
<span data-ttu-id="0ef00-811">Zinn</span><span class="sxs-lookup"><span data-stu-id="0ef00-811">tin</span></span>
  
<span data-ttu-id="0ef00-812">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-812">tax file no</span></span>
  
<span data-ttu-id="0ef00-813">tax file number</span><span class="sxs-lookup"><span data-stu-id="0ef00-813">tax file number</span></span>
  
<span data-ttu-id="0ef00-814">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-814">tax no</span></span>
  
<span data-ttu-id="0ef00-815">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-815">tax number</span></span>
  
<span data-ttu-id="0ef00-816">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-816">taxid#</span></span>
  
<span data-ttu-id="0ef00-817">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-817">taxno#</span></span>
  
<span data-ttu-id="0ef00-818">identifikacijska številka beim Davka</span><span class="sxs-lookup"><span data-stu-id="0ef00-818">identifikacijska številka davka</span></span>
  
<span data-ttu-id="0ef00-819">davčna številka</span><span class="sxs-lookup"><span data-stu-id="0ef00-819">davčna številka</span></span>
  
<span data-ttu-id="0ef00-820">številka davčne datoteke</span><span class="sxs-lookup"><span data-stu-id="0ef00-820">številka davčne datoteke</span></span>
  
## <a name="spain"></a><span data-ttu-id="0ef00-821">Spanien</span><span class="sxs-lookup"><span data-stu-id="0ef00-821">Spain</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-822">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-822">Format</span></span>

<span data-ttu-id="0ef00-823">Sieben oder acht Ziffern und ein oder zwei Buchstaben im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-823">Seven or eight digits and one or two letters in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-824">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-824">Pattern</span></span>

<span data-ttu-id="0ef00-825">Spanische natürliche Personen mit einem nationalen spanischen Identitätsausweis:</span><span class="sxs-lookup"><span data-stu-id="0ef00-825">Spanish Natural Persons with a Spain National Identity Card:</span></span>
  
-  <span data-ttu-id="0ef00-826">Acht Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-826">Eight digits</span></span> 
    
- <span data-ttu-id="0ef00-827">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="0ef00-827">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="0ef00-828">Nicht residente Spanier ohne nationalen Personalausweis</span><span class="sxs-lookup"><span data-stu-id="0ef00-828">Non-resident Spaniards without a Spain National Identity Card</span></span>
  
- <span data-ttu-id="0ef00-829">Ein Großbuchstabe "L" (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0ef00-829">One uppercase letter "L" (case-sensitive)</span></span>
    
- <span data-ttu-id="0ef00-830">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0ef00-830">Seven digits</span></span>
    
- <span data-ttu-id="0ef00-831">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="0ef00-831">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="0ef00-832">Residente Spanier unter 14 Jahren ohne National Ausweis für Spanien:</span><span class="sxs-lookup"><span data-stu-id="0ef00-832">Resident Spaniards under the age of 14 years without a Spain National Identity Card :</span></span>
  
- <span data-ttu-id="0ef00-833">Ein Großbuchstabe "K" (Groß-/Kleinschreibung beachten)</span><span class="sxs-lookup"><span data-stu-id="0ef00-833">One uppercase letter"K" (case-sensitive)</span></span>
    
-  <span data-ttu-id="0ef00-834">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0ef00-834">Seven digits</span></span> 
    
- <span data-ttu-id="0ef00-835">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="0ef00-835">One uppercase letter (case-sensitive)</span></span>
    
<span data-ttu-id="0ef00-836">Ausländer mit der IdentifikationsNummer eines ausLänders</span><span class="sxs-lookup"><span data-stu-id="0ef00-836">Foreigners with a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="0ef00-837">Ein Großbuchstabe, der "X", "Y" oder "Z" ist (Groß-/Kleinschreibung)</span><span class="sxs-lookup"><span data-stu-id="0ef00-837">One uppercase letter that is "X", "Y", or "Z" (case-sensitive)</span></span> 
    
- <span data-ttu-id="0ef00-838">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0ef00-838">Seven digits</span></span>
    
- <span data-ttu-id="0ef00-839">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="0ef00-839">One uppercase letter (case-sensitive)</span></span> 
    
<span data-ttu-id="0ef00-840">Ausländer ohne IdentifikationsNummer eines ausLänders</span><span class="sxs-lookup"><span data-stu-id="0ef00-840">Foreigners without a Foreigner's Identification Number</span></span>
  
- <span data-ttu-id="0ef00-841">Ein Großbuchstabe, der "M" (Groß-/Kleinschreibung beachtet) ist</span><span class="sxs-lookup"><span data-stu-id="0ef00-841">One uppercase letter that is "M" (case-sensitive)</span></span> 
    
- <span data-ttu-id="0ef00-842">Sieben Ziffern </span><span class="sxs-lookup"><span data-stu-id="0ef00-842">Seven digits</span></span>
    
- <span data-ttu-id="0ef00-843">Ein Großbuchstabe (Groß-/Kleinschreibung beachtet)</span><span class="sxs-lookup"><span data-stu-id="0ef00-843">One uppercase letter (case-sensitive)</span></span> 
    
### <a name="checksum"></a><span data-ttu-id="0ef00-844">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-844">Checksum</span></span>

<span data-ttu-id="0ef00-845">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-845">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-846">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-846">Definition</span></span>

<span data-ttu-id="0ef00-847">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-847">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-848">Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-848">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-849">Ein Schlüsselwort `Keywords_spain_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-849">A keyword from  `Keywords_spain_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-850">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-850">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-851">Die Funktion `Func_spain_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-851">The function  `Func_spain_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
          <Match idRef="Keywords_spain_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_spain_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-852">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-852">Keywords</span></span>

#### <a name="keywordsspaineutaxfilenumber"></a><span data-ttu-id="0ef00-853">Keywords_spain_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-853">Keywords_spain_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-854">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-854">tax id</span></span>
  
<span data-ttu-id="0ef00-855">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-855">tax id number</span></span>
  
<span data-ttu-id="0ef00-856">CIF-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-856">cif id</span></span>
  
<span data-ttu-id="0ef00-857">CIF Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-857">cif no</span></span>
  
<span data-ttu-id="0ef00-858">spanische CIF-ID</span><span class="sxs-lookup"><span data-stu-id="0ef00-858">spanish cif id</span></span>
  
<span data-ttu-id="0ef00-859">CIF</span><span class="sxs-lookup"><span data-stu-id="0ef00-859">cif</span></span>
  
<span data-ttu-id="0ef00-860">Steuerdatei Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-860">tax file no</span></span>
  
<span data-ttu-id="0ef00-861">spanische CIF-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-861">spanish cif number</span></span>
  
<span data-ttu-id="0ef00-862">tax file number</span><span class="sxs-lookup"><span data-stu-id="0ef00-862">tax file number</span></span>
  
<span data-ttu-id="0ef00-863">Spanisch (CIF) Nein</span><span class="sxs-lookup"><span data-stu-id="0ef00-863">spanish cif no</span></span>
  
<span data-ttu-id="0ef00-864">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-864">tax no</span></span>
  
<span data-ttu-id="0ef00-865">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-865">tax number</span></span>
  
<span data-ttu-id="0ef00-866">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-866">taxid#</span></span>
  
<span data-ttu-id="0ef00-867">taxno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-867">taxno#</span></span>
  
<span data-ttu-id="0ef00-868">CIFID #</span><span class="sxs-lookup"><span data-stu-id="0ef00-868">cifid#</span></span>
  
<span data-ttu-id="0ef00-869">spanishcifid #</span><span class="sxs-lookup"><span data-stu-id="0ef00-869">spanishcifid#</span></span>
  
<span data-ttu-id="0ef00-870">spanishcifno #</span><span class="sxs-lookup"><span data-stu-id="0ef00-870">spanishcifno#</span></span>
  
<span data-ttu-id="0ef00-871">número de contribuyente</span><span class="sxs-lookup"><span data-stu-id="0ef00-871">número de contribuyente</span></span>
  
<span data-ttu-id="0ef00-872">número de Impuesto Corporativo</span><span class="sxs-lookup"><span data-stu-id="0ef00-872">número de impuesto corporativo</span></span>
  
<span data-ttu-id="0ef00-873">número de Identificación Fiscal</span><span class="sxs-lookup"><span data-stu-id="0ef00-873">número de identificación fiscal</span></span>
  
<span data-ttu-id="0ef00-874">CIF-número</span><span class="sxs-lookup"><span data-stu-id="0ef00-874">cif número</span></span>
  
<span data-ttu-id="0ef00-875">cifnúmero #</span><span class="sxs-lookup"><span data-stu-id="0ef00-875">cifnúmero#</span></span>
  
## <a name="sweden"></a><span data-ttu-id="0ef00-876">Schweden</span><span class="sxs-lookup"><span data-stu-id="0ef00-876">Sweden</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-877">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-877">Format</span></span>

<span data-ttu-id="0ef00-878">Zehn Ziffern und ein Symbol im angegebenen Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-878">Ten digits and a symbol in the specified pattern</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-879">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-879">Pattern</span></span>

<span data-ttu-id="0ef00-880">Zehn Ziffern und ein Symbol:</span><span class="sxs-lookup"><span data-stu-id="0ef00-880">Ten digits and a symbol:</span></span>
  
-  <span data-ttu-id="0ef00-881">Sechs Ziffern, die dem Geburtsdatum entsprechen (JJMMTT)</span><span class="sxs-lookup"><span data-stu-id="0ef00-881">Six digits that correspond to the birth date (YYMMDD)</span></span> 
    
- <span data-ttu-id="0ef00-882">Ein Pluszeichen, Minuszeichen oder umgekehrter Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="0ef00-882">A plus sign, minus sign, or backslash</span></span>
    
- <span data-ttu-id="0ef00-883">Drei Ziffern, die die Identifizierungsnummer eindeutig machen, wobei:</span><span class="sxs-lookup"><span data-stu-id="0ef00-883">Three digits that make the identification number unique where:</span></span> 
    
  - <span data-ttu-id="0ef00-884">Für Zahlen, die vor 1990 ausgegeben wurden, kennzeichnen die siebte und die achte Ziffer den Geburtsort oder die im Ausland geborenen Personen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-884">For numbers issued before 1990, the seventh and eighth digit identify the county of birth or foreign-born people</span></span>
    
  - <span data-ttu-id="0ef00-885">Die Ziffer in der neunten Position gibt an, dass Geschlecht entweder ungerade für männlich oder sogar für weiblich ist.</span><span class="sxs-lookup"><span data-stu-id="0ef00-885">The digit in the ninth position indicates gender by either odd for male or even for female</span></span>
    
- <span data-ttu-id="0ef00-886">Eine Prüfziffer</span><span class="sxs-lookup"><span data-stu-id="0ef00-886">One check digit</span></span>
    
### <a name="checksum"></a><span data-ttu-id="0ef00-887">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-887">Checksum</span></span>

<span data-ttu-id="0ef00-888">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-888">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-889">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-889">Definition</span></span>

<span data-ttu-id="0ef00-890">Eine DLP-Richtlinie ist zu 85 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-890">A DLP policy is 85% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-891">Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-891">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-892">Ein Schlüsselwort `Keywords_sweden_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-892">A keyword from  `Keywords_sweden_eu_tax_file_number` is found.</span></span> 
    
<span data-ttu-id="0ef00-893">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-893">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-894">Die Funktion `Func_sweden_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-894">The function  `Func_sweden_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="85">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
          <Match idRef="Keywords_sweden_eu_tax_file_number" />
        </Pattern>
<Pattern confidenceLevel="75">
          <IdMatch idRef="Func_sweden_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-895">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-895">Keywords</span></span>

#### <a name="keywordsswedeneutaxfilenumber"></a><span data-ttu-id="0ef00-896">Keywords_sweden_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-896">Keywords_sweden_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-897">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-897">tax id</span></span>
  
<span data-ttu-id="0ef00-898">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-898">tax id no.</span></span>
  
<span data-ttu-id="0ef00-899">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-899">tax id number</span></span>
  
<span data-ttu-id="0ef00-900">tax identification</span><span class="sxs-lookup"><span data-stu-id="0ef00-900">tax identification</span></span>
  
<span data-ttu-id="0ef00-901">USt-Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-901">tax identification#</span></span>
  
<span data-ttu-id="0ef00-902">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-902">tax no.</span></span>
  
<span data-ttu-id="0ef00-903">Steuer</span><span class="sxs-lookup"><span data-stu-id="0ef00-903">tax#</span></span>
  
<span data-ttu-id="0ef00-904">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-904">taxid#</span></span>
  
<span data-ttu-id="0ef00-905">Steuerdatei</span><span class="sxs-lookup"><span data-stu-id="0ef00-905">tax file</span></span>
  
<span data-ttu-id="0ef00-906">Steuerdatei Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-906">tax file no.</span></span>
  
<span data-ttu-id="0ef00-907">persönliche ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-907">personal id number</span></span>
  
<span data-ttu-id="0ef00-908">Skate ID Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-908">skatt id nummer</span></span>
  
<span data-ttu-id="0ef00-909">Skate Identifikation</span><span class="sxs-lookup"><span data-stu-id="0ef00-909">skatt identifikation</span></span>
  
<span data-ttu-id="0ef00-910">PERSONNUMMER</span><span class="sxs-lookup"><span data-stu-id="0ef00-910">personnummer</span></span>
  
## <a name="uk"></a><span data-ttu-id="0ef00-911">UK</span><span class="sxs-lookup"><span data-stu-id="0ef00-911">UK</span></span>

### <a name="format"></a><span data-ttu-id="0ef00-912">Format</span><span class="sxs-lookup"><span data-stu-id="0ef00-912">Format</span></span>

<span data-ttu-id="0ef00-913">Eindeutige Steuerzahler-Referenz (UTR): 10 Ziffern ohne Leerzeichen und Abgrenzungen</span><span class="sxs-lookup"><span data-stu-id="0ef00-913">Unique Taxpayer Reference (UTR): 10 digits without spaces and delimiters</span></span>
  
<span data-ttu-id="0ef00-914">Nationale Versicherungsnummer (NINO): Weitere Informationen finden Sie im Abschnitt "U.K.</span><span class="sxs-lookup"><span data-stu-id="0ef00-914">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="0ef00-915">National Insurance Number (NINO) "in [dem, wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0ef00-915">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="pattern"></a><span data-ttu-id="0ef00-916">Muster</span><span class="sxs-lookup"><span data-stu-id="0ef00-916">Pattern</span></span>

<span data-ttu-id="0ef00-917">Eindeutige Steuerzahler-Referenz (UTR): 10 Ziffern</span><span class="sxs-lookup"><span data-stu-id="0ef00-917">Unique Taxpayer Reference (UTR): 10 digits</span></span>
  
<span data-ttu-id="0ef00-918">Nationale Versicherungsnummer (NINO): Weitere Informationen finden Sie im Abschnitt "U.K.</span><span class="sxs-lookup"><span data-stu-id="0ef00-918">National Insurance Number (NINO): For details, see the section "U.K.</span></span> <span data-ttu-id="0ef00-919">National Insurance Number (NINO) "in [dem, wonach die Typen von vertraulichen Informationen suchen](what-the-sensitive-information-types-look-for.md).</span><span class="sxs-lookup"><span data-stu-id="0ef00-919">National Insurance Number (NINO)" in [What the sensitive information types look for](what-the-sensitive-information-types-look-for.md).</span></span>
  
### <a name="checksum"></a><span data-ttu-id="0ef00-920">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="0ef00-920">Checksum</span></span>

<span data-ttu-id="0ef00-921">Ja</span><span class="sxs-lookup"><span data-stu-id="0ef00-921">Yes</span></span>
  
### <a name="definition"></a><span data-ttu-id="0ef00-922">Definition</span><span class="sxs-lookup"><span data-stu-id="0ef00-922">Definition</span></span>

<span data-ttu-id="0ef00-923">Eine DLP-Richtlinie ist zu 75 % sicher, dass diese Art von vertraulichen Informationen erkannt wurde, wenn Folgendes innerhalb von 300 Zeichen zutrifft:</span><span class="sxs-lookup"><span data-stu-id="0ef00-923">A DLP policy is 75% confident that it's detected this type of sensitive information if, within a proximity of 300 characters:</span></span>
  
- <span data-ttu-id="0ef00-924">Die Funktion `Func_uk_eu_tax_file_number` sucht nach Inhalten, die mit dem Muster übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="0ef00-924">The function  `Func_uk_eu_tax_file_number` finds content that matches the pattern.</span></span> 
    
- <span data-ttu-id="0ef00-925">Ein Schlüsselwort `Keywords_uk_eu_tax_file_number` aus wurde gefunden.</span><span class="sxs-lookup"><span data-stu-id="0ef00-925">A keyword from  `Keywords_uk_eu_tax_file_number` is found.</span></span> 
    
```
 <!-- EU Tax File Number -->
<Entity id="e09c07d3-66e5-4783-989d-49ac62748f5f" patternsProximity="300" recommendedConfidence="75">
        <Pattern confidenceLevel="75">
          <IdMatch idRef="Func_uk_eu_tax_file_number" />
          <Match idRef="Keywords_uk_eu_tax_file_number" />
        </Pattern>
</Entity>
```

### <a name="keywords"></a><span data-ttu-id="0ef00-926">Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="0ef00-926">Keywords</span></span>

#### <a name="keywordsukeutaxfilenumber"></a><span data-ttu-id="0ef00-927">Keywords_uk_eu_tax_file_number</span><span class="sxs-lookup"><span data-stu-id="0ef00-927">Keywords_uk_eu_tax_file_number</span></span>

<span data-ttu-id="0ef00-928">tax id</span><span class="sxs-lookup"><span data-stu-id="0ef00-928">tax id</span></span>
  
<span data-ttu-id="0ef00-929">USt-ID-Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-929">tax id no.</span></span>
  
<span data-ttu-id="0ef00-930">USt-ID-Nummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-930">tax id number</span></span>
  
<span data-ttu-id="0ef00-931">tax identification</span><span class="sxs-lookup"><span data-stu-id="0ef00-931">tax identification</span></span>
  
<span data-ttu-id="0ef00-932">USt-Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-932">tax identification#</span></span>
  
<span data-ttu-id="0ef00-933">Steuernummer</span><span class="sxs-lookup"><span data-stu-id="0ef00-933">tax no.</span></span>
  
<span data-ttu-id="0ef00-934">Steuer</span><span class="sxs-lookup"><span data-stu-id="0ef00-934">tax#</span></span>
  
<span data-ttu-id="0ef00-935">getaxit #</span><span class="sxs-lookup"><span data-stu-id="0ef00-935">taxid#</span></span>
  
<span data-ttu-id="0ef00-936">Steuerdatei</span><span class="sxs-lookup"><span data-stu-id="0ef00-936">tax file</span></span>
  
<span data-ttu-id="0ef00-937">Steuerdatei Nr.</span><span class="sxs-lookup"><span data-stu-id="0ef00-937">tax file no.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0ef00-938">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ef00-938">See also</span></span>

[<span data-ttu-id="0ef00-939">Wonach die Typen von vertraulichen Informationen suchen</span><span class="sxs-lookup"><span data-stu-id="0ef00-939">What the sensitive information types look for</span></span>](what-the-sensitive-information-types-look-for.md)

